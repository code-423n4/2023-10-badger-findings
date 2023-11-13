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