### [L-01] Two-step ownership is good when changing owners

Auth.sol transferOwnership transfers the authority of an owner without having a two-step process. It is desirable to have a two-step process when changing the authority to prevent any mistakes. 

```
  function isAuthorized(address user, bytes4 functionSig) internal view virtual returns (bool) {
        Authority auth = authority; // Memoizing authority saves us a warm SLOAD, around 100 gas.

        // Checking if the caller is the owner only after calling the authority saves gas in most cases, but be
        // aware that this makes protected functions uncallable even to the owner if the authority is out of order.
        return
            (address(auth) != address(0) && auth.canCall(user, address(this), functionSig)) ||
            user == owner;
    }
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol

### [L-02] Check for 0 address input in constructors and important state changes

Check for 0 address input when changing addresses in important state changes as well as constructors, to prevent wrong address changes that may be irreversible, or would waste a lot of gas if redeployed.

```
    constructor(address _owner, Authority _authority) {
        // Check owner is zero address
        owner = _owner;
        authority = _authority;

        emit OwnershipTransferred(msg.sender, _owner);
        emit AuthorityUpdated(msg.sender, _authority);
    }
```

### [L-03] closedStatus is checked twice when removing a cdp

`_removeCdp()` checks that cdpStatus is not nonExistent or Active. `_removeCdp()` is internal and only called in `_closeCdp()`. `_closeCdp()` also checks that the closedStatus is not nonExistent or Active. Since `_removeCdp()` is only called through `_closeCdp()` and not anywhere else, the check should only be in `_removeCdp()` and not in `_closeCdp()`. 

```
    function _closeCdpWithoutRemovingSortedCdps(bytes32 _cdpId, Status closedStatus) internal {
        require(
            closedStatus != Status.nonExistent && closedStatus != Status.active,
            "CdpManagerStorage: close non-exist or non-active CDP!"
        );
```

```
    function _removeCdp(bytes32 _cdpId, uint256 cdpIdsArrayLength) internal {
        Status cdpStatus = Cdps[_cdpId].status;
        // It’s set in caller function `_closeCdp`
        require(
            cdpStatus != Status.nonExistent && cdpStatus != Status.active,
            "CdpManagerStorage: remove non-exist or non-active CDP!"
        );
```

Have the require() check only in `_removeCdp()`.

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L410

### [L-04] The TIMEOUT for ETH-BTC and STETH-ETH feed is different from Chainlink

In Chainlink, the heartbeat for eth-btc is about ~1 hour and the steth-eth heartbeat is about ~1 day.

In the protocol, the heartbeat for eth-btc is 1.33 hours and the steth-eth heartbeat is about 25 hours.

```
    // Maximum time period allowed since Chainlink's latest round data timestamp, beyond which Chainlink is considered frozen.
    uint256 public constant TIMEOUT_ETH_BTC_FEED = 4800; // 1 hours & 20min: 60 * 80
    uint256 public constant TIMEOUT_STETH_ETH_FEED = 90000; // 25 hours: 60 * 60 * 25
```

Consider using the same heartbeat time as chainlink. 

https://data.chain.link/ethereum/mainnet/crypto-other/eth-btc
https://data.chain.link/base/base/crypto-eth/steth-eth

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L561

### [L-05] Consider checking the min/max price of the returned price.

In the event of a flash crash (ETH goes down to 0), the ETH/BTC feed will return a minAnswer price instead of the actual price. Since the price feed is extremely important for CDPs, make sure that the protocol accounts for flash crashes and reports the actual price instead of a min price. 

https://docs.chain.link/data-feeds#check-the-latest-answer-against-reasonable-limits

### [N-01] Fallback caller is spelled incorrectly

PriceFeed.sol spells the new fallback caller as `newFallbackCaler`, which is missing an l. Spell it as `newFallbackCaller` instead.

```
 IFallbackCaller newFallbackCaler = IFallbackCaller(_fallbackCaller);
        FallbackResponse memory fallbackResponse;
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L358

### [N-02] There can be alternative pathings to fetch the StEth/Btc price

 The STETH-ETH-BTC route currently uses steth-eth and eth-btc route. stETH/ETH Chainlink oracle has an extremely long heartbeat, which is 24 hours, but a low deviation threshold at 0.5%.

Another pathing would be the stETH-USD-BTC route to fetch the stETH-BTC price since both stETH-USD and USD-BTC feed has a 1 hour heartbeat with low deviation threshold at 1% and 0.5%.

Depending on the protocol to favour either deviation threshold or timeout, other pathings can be considered.

https://data.chain.link/ethereum/mainnet/crypto-usd/steth-usd
https://data.chain.link/ethereum/mainnet/crypto-usd/btc-usd
