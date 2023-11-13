# Redundant Check

## Redundant Check at `cdpManager::_openCdp`
`vars.netStEthBalance` is always greater than or equal 2e.


```C++
        // @info vars.netStEthBalance >= 2e
        _requireAtLeastMinNetStEthBalance(vars.netStEthBalance);
        // @audit Redundant Check for netStEthBalance
        require(vars.netStEthBalance > 0, "BorrowerOperations: zero collateral for openCdp()!");
```
### [Related code](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L439-L472)

## Redundant Check at `EBTCToken::_requireValidRecipient`

```C++
    function _requireValidRecipient(address _recipient) internal view {
        require(
            _recipient != address(0) && _recipient != address(this),
            "EBTC: Cannot transfer tokens directly to the EBTC token contract or the zero address"
        );
        require(
            _recipient != cdpManagerAddress && _recipient != borrowerOperationsAddress,
            "EBTC: Cannot transfer tokens directly to the CdpManager or BorrowerOps"
        );
    }
```
### [Related code](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/EBTCToken.sol#L295C42-L311)

## Redundant value setting

```C++
        uint256 liquidatorRewardShares = cdpManager.getCdpLiquidatorRewardShares(_cdpId);
```

`Cdps[_cdpId].liquidatorRewardShares` is always equals `collateral.getSharesByPooledEth(LIQUIDATOR_REWARD)`, there is no need to get it from the struct.

## Should Prevent Zero Amount Transfer Attack

There is a restriction on transferring an amount of zero. It should be evaluated that the current allowance is greater than or equal to the maximum of the amount and 1, thereby necessitating the approval to be non-zero.

```C++
    function transferFrom(
        address sender,
        address recipient,
        uint256 amount
    ) external override returns (bool) {
        _requireValidRecipient(recipient);
        _transfer(sender, recipient, amount);

        uint256 cachedAllowance = _allowances[sender][msg.sender];
        // if (cachedAllowance != type(uint256).max) {
        // @audit add zero allowance check ,
        if (cachedAllowance != type(uint256).max && cachedAllowance != 0) {
            require(cachedAllowance >= amount, "ERC20: transfer amount exceeds allowance");
            unchecked {
                _approve(sender, msg.sender, cachedAllowance - amount);
            }
        }
        return true;
    }
```
### [Related code](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/EBTCToken.sol#L134-L150)

[openzeppelin zero transfer attacks](https://blog.openzeppelin.com/how-to-ensure-web3-users-are-safe-from-zero-transfer-attacks)


