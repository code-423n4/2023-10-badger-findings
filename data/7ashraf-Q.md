
# Possible division by zero
## Instances
CDPManager.sol #621-622
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L621

LiquidationLibrary.sol #555
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L555

LiquidationLibrary.sol #558
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L558

LiquidationLibrary.sol #579
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L579

Need to validate ```_redeemColFromCdp``` to avoid  division by 0 risk
CdpManager.sol #135
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L135

## Description 
by tracing the function calls, after calling decrease system debt to zero, a zero value may be passed to the function

## Mitigation
Add a ```require value > 0``` statement before diding by ```value```

# Check if cpd exists first 
## Instances
* LiquidationLibrary.sol #400
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L400

* LiquidationLibrary.sol #455
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L455

* CdpManager.sol #419
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L419

* CdpManager.sol#432
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L432

* LiquidationLibrary.sol #472
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L472

* LiquidationLibrary.sol #754
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L754

* CdpManager.sol #336
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L336

* CdpManager.sol #334
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L334
# Should check if borrower and position manager exist first

## Instances
* BorrowerOperations.sol #635  
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L635
* BorrowerOperations.sol #647
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L647
* BorrowerOperations.sol #653
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L653

# Unsafe subtraction
## Instances
* BorrowerOperations.sol #1062
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1060C9-L1062C56
```
systemStEthBalance = _isCollIncrease
            ? systemStEthBalance + _stEthBalanceChange
            : systemStEthBalance - _stEthBalanceChange;
```
* CdpManager.sol #156
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L156

* CdpManager.sol #157
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L157


## Mitigation
Add ```require val1 >= val2;``` statement





# Function vulnerable to reentrancy
## Instances
BorrowerOperations.sol #533
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L553C36-L553C36


# In-accurate and non-descriptive emit and error messages
## Instances
* Emit initialized instead of updated
CdpManager.sol #925
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L925

* Inaccurate error message, should use less than or equal 
LiquidationLibrary.sol #904
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L904

* Emit CdpManagerStorage is deployed
CdpManager.sol #217
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L217

* Should emit burn event or mint event instead of transferring from or to address(0)
EbtcToken.sol #282
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L282
EbtcToken.sol #267
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L267

* Should emit an event upon storing and updating
PriceFeed.sol #561
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L561
PriceFeed.sol #571
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L571

* Invalid message emitted should be initialized instead of changed
ActivePool.sol #65
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L65

* Write a valid error message 
ActivePool.sol #104
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L104

* Emit CdpManager initialization
CdpManager.sol #30
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L30

* Emit cdp closed rather than updated
CdpManager.sol #179
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L179







# Add else block
## Description
Should add an else block specifying what should happen if the condition does not apply and emit the correct error message.
## Instances
* CdpManagerStorage.sol #55
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L52

* CdpManagerStorage.sol #66
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L66

# Empty catch block 
## Instances 
PriceFeed.sol # 597
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L597


# Unnecessary require block
## Instances 
BorrowerOperations.sol #517
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L517

## Description
the check of cdp non-existent is already present in the insert method called above




# Prevent allowance of 0 
## Instances 
EbtcToken.sol #285
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L285
## Mitigation
Add ```require amount > 0``` statement






# Add Governeror to: (ensure not system block)
## Instances
LeaverageMacroBase.sol #450
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L450



# Add comments to explain assembly code 
## Instances
SimplifiedDiamondLike.sol #189
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L189



# Consider allowing fee recipient to be able to claim coll shares
ActivePool.sol #346
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L346






# General
* No transfer of authority in CpdManager
* Protocol not pausable
* Consider adding a list of authorized addresses or wards on the protocol












