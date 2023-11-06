### Redundant check
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L863
`_redistributeDebt` will never be called if debt = 0
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L525-L527
### BaseMath is not used
PriceFeed contract inherits from BaseMath but doesn't use it's single constant DECIMAL_PRECISION, so it's possible to remove it.
### Unused modifier
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L323
this modifier is not used in `EBTCTokem.sol`
### Double checking `recipient != address(0)`
Before transferring tokens we invoke `_requireValidRecipient`, where among many checks we check that recipient != address(0),
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L297
same check is made inside `_transfer` function
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L248
### Enforce beta is not zero
Authorized users can change `beta` value
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L830
if it's set to zero. we'll divide by zero here
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L624

### `arrayIndex` value is not deleted when we remove cpd
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L269-L274
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L471
When we remove cpd, we zero all it's values, but `arrayIndex` remains.
### UpdateManager?
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L963
`Borrower` can approve operations to the `PositionManager`, `UpdateManager` is not mentioned anywhere in the contract. `_requireBorrowerOrPositionManagerApproval` would be more clear.
### Hash value names inconsistency
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L33-L35
we use 
```  
      keccak256(
            "PermitPositionManagerApproval(address borrower,address positionManager,uint8 status,uint256 nonce,uint256 deadline)"
        );
```
but in `permitPositionManagerApproval` we use `approval` instead of `status`  
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L709

### Consider using enum values instead of numbers
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L826
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L831

`status == ICdpManagerData.Status.active`
`status == ICdpManagerData.Status.nonExistent`

### It would be more appropriate to use `syncGlobalAccountingAndGracePeriod`
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1146
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1157
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1168

Here we update global system parameters but we use `syncGlobalAccounting` which doesn't trigger recovery mode if TCR becomes less than CCR, unlike `syncGlobalAccountingAndGracePeriod`.

```
    function syncGlobalAccounting() external {
        _requireCallerIsBorrowerOperations();
        _syncGlobalAccounting();
    }
```
```
    function syncGlobalAccountingAndGracePeriod() public {
        _syncGlobalAccounting(); // Apply // Could trigger RM
        _syncGracePeriod(); // Synch Grace Period
    }
```



### Typos, wrong comments and naming
1. These comments are copy-pasted from Auth.sol, we don't check the owner here

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L33-L34
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L39-L40

2. Fee floor is actually 0%

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L35

3. Entire system debt

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L73

4. Memorizing typo

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L33

5. `sending EBTC directly to a Liquity`

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L22

6. _NICR would be more appropriate name

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L165

CR is associated with collateral ratio, however in this function we use NICR values to find a hint

7. Wrong pair names in comments

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L784
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L786
should be stETH-ETH feed

8. ETH-USD comment from Liquity

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L594

should be stETH-BTC
