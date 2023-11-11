

## Gas Optimization 


| No | Instance | Description |

| [G-01] | Manages system-level internal accounting and stETH tokens.|
| [G-02] | Entry point to Open, Adjust, and Close Cdps as well as delegate positionManagers.|
| [G-03] | 	Cdp operations and entry point for non-borrower operations on Cdps (Liquidations, Redemptions).|
| [G-04] | 	Contains liquidation-related functions. Split off due to maximum contract size, delegateCalled by CdpManager.|
| [G-05] | 	Shared storage variables between CdpManager and Liquidation Library, and common functions.|
| [G-06] |  Isolated storage of excess collateral owed to users from liquidations or redemptions. Not considered part of system for accounting.|
| [G-07] |  ERC20 EbtcToken, with permit approvals and extensible minting.|
| [G-08] | Roles-based authorization contract, adapted and expanded from solmate Authority. Expanded with more convenience view functions and ability to permanently burn capabilities.|
| [G-09] | riceFeed with primary and secondary oracles and state machine to switch between them and handle failure cases. |

| [G-10]| 	Data storage for the doubly-linked list of Cdps. Sorting of Cdps is used to enforce redemptions from lowest ICR to highest ICR.|

| [G-11] | Generate approximate locations for proper linked list insertion locations for Cdps.|

| [G-12] common base implementation of the LeverageMacro.|

| [G-13] LeverageMacro variant for use with delegateCall with compatible smart wallets.|

| [G-14] 	Factory for deploying LeverageMacroReference.|

| [G-15] LeverageMacro variant for use as a zap with an individual owner.|

| [G-16]  Smart wallet with custom callback handler support.|

| [G-17] Inherited by contracts consuming authorization rules of Governor.|

| [G-18] 	Inherited by contracts consuming authorization rules of Governor. Removes owner address that has global 'admin' permission from Auth.|

| [G-19] Base for standardized flash loans|

| [G-20] Common definition and base functions for system contracts.|

| [G-21] More common math functions for system contracts.|

| [G-22] Simple, optimized reentrancy guard.|

| [G-23] Role-based authorization from solmate. Expanded functionality for use with Governor.|

| [G-24] ActivePool interface|

| [G-25] BorrowerOperations primary interface|

| [G-26] CdpManager primary interface|

| [G-27] CdpManagerStorage interface. Contains structs, events, and common functions between CdpManager and LiquidationLibrary| 

| [G-28] EbtcBase interface.|

| [G-29] EBTCToken interface, expands IERC20 and IERC2612.|





## Description  or Summary 



### [G-01] Manages system-level internal accounting and stETH tokens.

```solidity
file: packages/contracts/contracts/ActivePool.sol
```
ollateral.transferShares(_account, _shares);

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L183
```



### [G-02] Entry point to Open, Adjust, and Close Cdps as well as delegate positionManagers.

```solidity
file: packages/contracts/contracts/BorrowerOperations.sol
```
 currentCdpId = sortedCdps.getNext(currentCdpId);
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/MultiCdpGetter.sol#L100
```


### [G-03] 	Cdp operations and entry point for non-borrower operations on Cdps (Liquidations, Redemptions).

```solidity
file: packages/contracts/contracts/CdpManager.sol
```
   singleRedemption.debtToRedeem = EbtcMath._min(
            _redeemColFromCdp.maxEBTCamount,
            Cdps[_redeemColFromCdp.cdpId].debt 
        );
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L140-L143
```



### [G-04] 	Contains liquidation-related functions. Split off due to maximum contract size, delegateCalled by CdpManager.

```solidity
file: packages/contracts/contracts/LiquidationLibrary.sol
```
  function liquidate(bytes32 _cdpId) external nonReentrantSelfAndBOps {
        _liquidateIndividualCdpSetup(_cdpId, 0, _cdpId, _cdpId);
    }
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L40-L42
```


### [G-05] Shared storage variables between CdpManager and Liquidation Library, and common functions.|

```solidity
file: packages/contracts/contracts/CdpManagerStorage.sol
```
    Cdp storage _cdp = Cdps[_cdpId];
    uint prevCollShares = _cdp.coll;
    uint256 prevDebt = _cdp.debt;
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L363-L366
```



### [G-06] Isolated storage of excess collateral owed to users from liquidations or redemptions. Not considered part of system for accounting.|

```solidity
file:   packages/contracts/contracts/CollSurplusPool.sol
```
  uint256 claimableColl = balances[_account];
        require(claimableColl > 0, "CollSurplusPool: No collateral available to claim");
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L89-L92
```





### [G-07] ERC20 EbtcToken, with permit approvals and extensible minting.|

```solidity
file: packages/contracts/contracts/EBTCToken.sol
```
     require(sender != address(0), "EBTCToken: zero sender!");
        require(recipient != address(0), "EBTCToken: zero recipient!");

        uint256 cachedSenderBalances = _balances[sender];
        require(cachedSenderBalances >= amount, "ERC20: transfer amount exceeds balance");

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L247-251
```


### [G-08] Roles-based authorization contract, adapted and expanded from solmate Authority. Expanded with more convenience view functions and ability to permanently burn capabilities.|

```solidity 
file: packages/contracts/contracts/Governor.sol
```
    function getRolesForUser(address user) external view returns (uint8[] memory rolesForUser) {
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L73
```


### [G-09] riceFeed with primary and secondary oracles and state machine to switch between them and handle failure cases.

```solidity
file: packages/contracts/contracts/PriceFeed.sol
```
 uint256 public constant MAX_PRICE_DIFFERENCE_BETWEEN_ORACLES = 5e16;
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L42
```


### [G-10] 	Data storage for the doubly-linked list of Cdps. Sorting of Cdps is used to enforce redemptions from lowest ICR to highest ICR.





```solidity
file:packages/contracts/contracts/SortedCdps.sol

```
  return _cdpOfOwnerByIndex(owner, index, startNodeId, maxNodes);
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L161
```







### [G-11] Generate approximate locations for proper linked list insertion locations for Cdps.

```solidity
file: packages/contracts/contracts/HintHelpers.sol
```
cdpManager.getSyncedICR(vars.currentCdpId, _price) < MCR
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L70
```




### [G-12] common base implementation of the LeverageMacro.

```solidity
file: packages/contracts/contracts/LeverageMacroBase.sol
```
        LeverageMacroOperation calldata operation,
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L121
```


### [G-13] LeverageMacro variant for use with delegateCall with compatible smart wallets.

```solidity
file: packages/contracts/contracts/LeverageMacroDelegateTarget.sol

```
        LeverageMacroBase(
            _borrowerOperationsAddress,
            _activePool,
            _cdpManager,
            _ebtc,
            _coll,
            _sortedCdps,
            true // Do not sweep to caller
        )
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L49-L57
```



### [G-14] 	Factory for deploying LeverageMacroReference.

```solidity
file: packages/contracts/contracts/LeverageMacroFactory.sol
```
    function deployNewMacro(address _owner) public returns (address) {
        address addy = address(
            new LeverageMacroReference(
                borrowerOperations,
                activePool,
                cdpManager,
                ebtcToken,
                stETH,
                sortedCdps,
                _owner
            )
        );
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L43-L54
```


### [G-15] LeverageMacro variant for use as a zap with an individual owner.

```solidity
file: 
packages/contracts/contracts/LeverageMacroReference.sol

```
 address external immutable theOwner;
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L12
```


### [G-16] Smart wallet with custom callback handler support.

```solidity
file: packages/contracts/contracts/SimplifiedDiamondLike.sol

```
  s.settings.allowNonCallback = allowNonCallbacks;
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L70
```



### [G-17] Inherited by contracts consuming authorization rules of Governor.

```solidity
file: packages/contracts/contracts/LeverageMacroReference.sol
```
      ebtcToken.approve(_borrowerOperationsAddress, type(uint256).max);
        stETH.approve(_borrowerOperationsAddress, type(uint256).max);
        stETH.approve(_activePool, type(uint256).max);
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L39-L41
```


### [G-18] 	Inherited by contracts consuming authorization rules of Governor. Removes owner address that has global 'admin' permission from Auth.

```solidiyt
file: packages/contracts/contracts/Dependencies/AuthNoOwner.sol
```
if (!_authorityInitialized) {
            _authorityInitialized = true;
        }

        emit AuthorityUpdated(msg.sender, Authority(newAuthority));
    }
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L46-L51
```

### [G-19] Base for standardized flash loans.

```solidity
file: packages/contracts/contracts/Dependencies/AuthNoOwner.sol
```
uint256 public constant MAX_BPS = 10_000;
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L9
```

### [G-20] Common definition and base functions for system contracts.|

```solidity
file: packages/contracts/contracts/Dependencies/EbtcBase.sol

```
  function _checkICRAgainstLiqThreshold(uint256 _icr, uint _tcr) internal view returns (bool) {
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L124
```

### [G-21] More common math functions for system contracts.

```solidity
file: packages/contracts/contracts/Dependencies/EbtcMath.sol
```
uint256 newCollRatio = (_stEthBalance * _price) / _debt;
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L110
```

### [G-22] Simple, optimized reentrancy guard.

```solidity
file: packages/contracts/contracts/Dependencies/ReentrancyGuard.sol
```
locked = OPEN;
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ReentrancyGuard.sol#L16
```



### [G-23] Role-based authorization from solmate. Expanded functionality for use with Governor.

```solidity
file: 
```
 function setUserRole(address user, uint8 role, bool enabled) public virtual requiresAuth {
        if (enabled) {
            getUserRoles[user] |= bytes32(1 << role);

            if (!users.contains(user)) {
                users.add(user);
            }
        } else {
            getUserRoles[user] &= ~bytes32(1 << role);

            // Remove user if no more roles
            if (getUserRoles[user] == bytes32(0)) {
                users.remove(user);
            }
        }

        emit UserRoleUpdated(user, role, enabled);
    }
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L147-L164
```


### [G-24] ActivePool interface

```solidity
file: 
```
interface IActivePool is IPool {
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IActivePool.sol#L7
```

### [G-25] BorrowerOperations primary interface.

```solidity
file: packages/contracts/contracts/Interfaces/IBorrowerOperations.sol
```
    event FlashLoanSuccess(
        address indexed _receiver,
        address indexed _token,
        uint256 _amount,
        uint256 _fee
    );

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#11-L15
```


### [G-26] CdpManager primary interface

```solidity
file: packages/contracts/contracts/Interfaces/ICdpManager.sol
```
interface ICdpManager is IEbtcBase, ICdpManagerData {
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol#L9
```


### [G-27] CdpManagerStorage interface. Contains structs, events, and common functions between CdpManager and LiquidationLibrary.

```solidity
file:   packages/contracts/contracts/Interfaces/ICdpManagerData.sol
```
    struct LocalVariables_OuterLiquidationFunction {
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L147
```


### [G-28] EbtcBase interface.

```solidity
file: packages/contracts/contracts/Interfaces/IEbtcBase.sol
```
interface IEbtcBase {
    function priceFeed() external view returns (IPriceFeed);
}
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IEbtcBase.sol#L7-L9
```

### [G-29] EBTCToken interface, expands IERC20 and IERC2612

```solidity
file: packages/contracts/contracts/Interfaces/IEBTCToken.sol
```
interface IEBTCToken is IERC20 {
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IEBTCToken.sol#L8
```