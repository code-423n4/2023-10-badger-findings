## L-1 _PERMIT_POSITION_MANAGER_TYPEHASH hash generation and comment discrepancy

https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L31-L35

// keccak256("permitPositionManagerApproval(address borrower,address positionManager,uint8 status,uint256 nonce,uint256 deadline)"); 
    bytes32 private constant _PERMIT_POSITION_MANAGER_TYPEHASH =
        keccak256(
            "PermitPositionManagerApproval(address borrower,address positionManager,uint8 status,uint256 nonce,uint256 deadline)"
        );

The comment for the typehash of the position manager and the actual code are different. The keccack256 hash in the comment and the hash in the code act on different arguments which will cause the output to be different. The difference in the arguments is in the capitalisation of the first letter.

### Recommended Mitigation
Change the hash argument to "PermitPositionManagerApproval(address borrower,address positionManager,uint8 status,uint256 nonce,uint256 deadline)".

## L-2 Chainlink feed timeouts are immutable in PriceFeed but can be changed.
https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/PriceFeed.sol#L31-L33

Based on a [conversation](https://x.com/NonseOdion/status/1710950601301893320?s=20) with [ChainlinkGod](https://twitter.com/ChainLinkGod), a prominent advocate of Chainlink, on Twitter, the timeout (heartbeat) of price feeds can be changed. If this occurs it means the PriceFeed contract will be using invalid timeout values and it'll remain in that state since they are immutable. Thus it won't be able to know the right time to put the Chainlink price feeds in frozen states.

### Recommended Mitigation
Allow the heartbeats to be set by Governance. Since they aren't values enforced at the contract level.

## L-3 The status values for the PriceFeed status enums are used wrongly according to their dictionary meanings

The status values include:
```chainlinkWorking,
usingFallbackChainlinkUntrusted,
bothOraclesUntrusted,
usingFallbackChainlinkFrozen,
usingChainlinkFallbackUntrusted 
```

When the public `status` variable of PriceFeed is called, and it returns any status starting with "using", it should mean that the price returned by the PriceFeed was from the oracle mentioned after `using` while the other is untrusted or frozen. E.g if it returns `usingFallbackChainlinkFrozen`, it should mean the price returned was from Fallback while Chainlink is frozen. But sometimes it returns the lastGoodPrice instead of the latest price from that oracle.

E.g 

https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/PriceFeed.sol#L120C3-L123

```
                if (_fallbackIsFrozen(fallbackResponse)) {
                    _changeStatus(Status.usingFallbackChainlinkUntrusted);
                    return lastGoodPrice;
                }

```
From the snippet above the lastGoodPrice is returned but the status is updated to `usingFallbackChainlinkUntrusted`. To anyone that calls `status` after fetching a price to know the oracle used, he'll be told it was from fallback oracle but it's actually the `lastGoodPrice`. There's also no guarantee that when the status is `usingFallbackChainlinkUntrusted`, the price will be returned from the Fallback oracle either.
