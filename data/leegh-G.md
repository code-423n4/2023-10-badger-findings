## [G-01] Redundant require check.
One ```require``` statement's conditiion is already included in another ```require``` statement, and thus can be removed.
```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

394:            _requireValidDebtRepayment(vars.debt, vars.netDebtChange); // @audit: included in L396
395:            _requireSufficientEbtcTokenBalance(msg.sender, vars.netDebtChange);
396:            _requireNonZeroDebt(vars.debt - vars.netDebtChange);

454:        _requireAtLeastMinNetStEthBalance(vars.netStEthBalance);
463:        require(vars.netStEthBalance > 0, "BorrowerOperations: zero collateral for openCdp()!"); // @audit: included in L454
```
[[L394-L396](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L394-L396), [L454-L463](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L454-L463)]



## [G-02] Unnecessary intialization of local variables.
```solidity
1038:        uint256 newCollShares = _collShares; // @audit: L1041 overrides this initialization
1039:        uint256 newDebt = _debt; // @audit: L1044 overrides this initialization
1040:
1041:        newCollShares = _isCollIncrease
1042:            ? _collShares + _collSharesChange
1043:            : _collShares - _collSharesChange;
1044:        newDebt = _isDebtIncrease ? _debt + _debtChange : _debt - _debtChange;
```
[[L1038-L1044](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1038-L1044)]

## [G-03] Transfer tokens after approve operation to save gas when approve operation reverts. 
```solidity
File: packages/contracts/contracts/EBTCToken.sol

140:        _transfer(sender, recipient, amount); // @audit: move `transfer` before return, after `approve`
141:
142:        uint256 cachedAllowance = _allowances[sender][msg.sender];
143:        if (cachedAllowance != type(uint256).max) {
144:            require(cachedAllowance >= amount, "ERC20: transfer amount exceeds 14:allowance");
145:            unchecked {
146:                _approve(sender, msg.sender, cachedAllowance - amount);
147:            }
148:        }
149:        return true;
```
[[L140-L149](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L140-L149)]