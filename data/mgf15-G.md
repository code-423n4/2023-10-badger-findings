
## **G-1** | Possible Optimizations in increaseSystemDebt and decreaseSystemDebt 


By using assembly, we can directly interact with the storage slot of the stored variable, allowing us to efficiently write and read address values in storage.

```diff

diff --git a/ActivePool.sol b/aActivePool.sol
index 40b6a1f..345d3dd 100644
--- a/ActivePool.sol
+++ b/aActivePool.sol
@@ -193,10 +197,13 @@ contract ActivePool is IActivePool, ERC3156FlashLender, ReentrancyGuard, BaseMat
 
     function increaseSystemDebt(uint256 _amount) external override {
         _requireCallerIsBOorCdpM();
-
+        
         uint256 cachedSystemDebt = systemDebt + _amount;
-
-        systemDebt = cachedSystemDebt;
+        //@audit use assembly to update storge
+        assembly{
+            sstore(systemDebt.slot,cachedSystemDebt)
+        }
+        //systemDebt = cachedSystemDebt;
         emit ActivePoolEBTCDebtUpdated(cachedSystemDebt);
     }
 
@@ -206,10 +213,13 @@ contract ActivePool is IActivePool, ERC3156FlashLender, ReentrancyGuard, BaseMat
 
     function decreaseSystemDebt(uint256 _amount) external override {
         _requireCallerIsBOorCdpM();
-
-        uint256 cachedSystemDebt = systemDebt - _amount;
-
-        systemDebt = cachedSystemDebt;
+        uint256 cachedSystemDebt;
+        unchecked{
+            cachedSystemDebt = systemDebt - _amount;
+        }
+        assembly{
+            sstore(systemDebt.slot,cachedSystemDebt)
+        }
         emit ActivePoolEBTCDebtUpdated(cachedSystemDebt);
     }

```

> Gas diff

```diff

 |----------------------------------------------|-----------------|-------|--------|--------|---------|
 | Deployment Cost                              | Deployment Size |       |        |        |         |
 | Function Name                                | min             | avg   | median | max    | # calls |
-| increaseSystemDebt                           | 1777            | 2746  | 1777   | 21677  | 3078    |
+| increaseSystemDebt                           | 1785            | 2640  | 1785   | 21685  | 3489    |
```


## **G-2** | struct can be packed

Each slot saved can avoid an extra Gsset (20000 gas) for the first setting of the struct. Subsequent reads as well as writes have smaller gas savings.

to 

[link](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L97-L104)
```solidity 
    struct MoveTokensParams {
        address user;
        bool isDebtIncrease;
        uint256 collSharesChange;
        uint256 collAddUnderlying; // ONLY for isCollIncrease=true
        bool isCollIncrease;
        uint256 netDebtChange;
        
    }

```
## **G-3** | use assembly to write address 

```diff
diff --git a/ActivePool.sol b/aActivePool.sol
index 40b6a1f..345d3dd 100644
--- a/ActivePool.sol
+++ b/aActivePool.sol
@@ -50,11 +50,15 @@ contract ActivePool is IActivePool, ERC3156FlashLender, ReentrancyGuard, BaseMat
         address _collSurplusAddress,
         address _feeRecipientAddress
     ) {
+        //@audit use assembly to write address 
+        assembly{
+            sstore(feeRecipientAddress.slot,_feeRecipientAddress)
+        }
         borrowerOperationsAddress = _borrowerOperationsAddress;
         cdpManagerAddress = _cdpManagerAddress;
         collateral = ICollateralToken(_collTokenAddress);
         collSurplusPoolAddress = _collSurplusAddress;
-        feeRecipientAddress = _feeRecipientAddress;
+        //feeRecipientAddress = _feeRecipientAddress;
 
         // TEMP: read authority to avoid signature change
         address _authorityAddress = address(AuthNoOwner(cdpManagerAddress).authority());
```

## **G-4** |  Use do while loops instead of for loops

A do while loop will cost less gas since the condition is not being checked for the first iteration. 
```diff
diff --git a/Governor.sol b/aGovernor.sol
index 0195952..4263f50 100644
--- a/Governor.sol
+++ b/aGovernor.sol
@@ -43,25 +43,40 @@ contract Governor is RolesAuthority {
     function getUsersByRole(uint8 role) external view returns (address[] memory usersWithRole) {
         // Search over all users: O(n) * 2
         uint256 count;
-        for (uint256 i = 0; i < users.length(); i++) {
+        //@audit use do while 
+        uint256 i;
+        uint256 len = users.length();
+        do{
+        //for (uint256 i = 0; i < users.length(); i++) {
             address user = users.at(i);
             bool _canCall = doesUserHaveRole(user, role);
             if (_canCall) {
                 count += 1;
             }
-        }
+            unchecked{
+                ++i;
+            }
+        }while(i<len);
         if (count > 0) {
-            uint256 j = 0;
+            //uint256 j = 0;
             usersWithRole = new address[](count);
             address[] memory _usrs = users.values();
-            for (uint256 i = 0; i < _usrs.length; i++) {
+            uint256 j;
+            uint256 i = 0;
+            do{
+            //for (uint256 i = 0; i < _usrs.length; i++) {
                 address user = _usrs[i];
                 bool _canCall = doesUserHaveRole(user, role);
                 if (_canCall) {
                     usersWithRole[j] = user;
-                    j++;
+                    unchecked{
+                        ++j;
+                    }
                 }
-            }
+                unchecked{
+                    ++i;
+                }
+            }while(i<_usrs.length);
         }
     }
```

> Gas Diff 

```diff
 |------------------------------------------|-----------------|--------|--------|--------|---------|
 | Deployment Cost                          | Deployment Size |        |        |        |         |
 | Function Name                            | min             | avg    | median | max    | # calls |
-| getUsersByRole                           | 145426          | 145426 | 145426 | 145426 | 1       |
+| getUsersByRole                           | 123563          | 123563 | 123563 | 123563 | 1       |

```

## **G-5** | Possible Optimizations in function setFeeBps

```diff
diff --git a/ActivePool.sol b/aActivePool.sol
index 40b6a1f..345d3dd 100644
--- a/ActivePool.sol
+++ b/aActivePool.sol
@@ -408,7 +418,11 @@ contract ActivePool is IActivePool, ERC3156FlashLender, ReentrancyGuard, BaseMat
 
         // set new flash fee
         uint256 _oldFee = feeBps;
-        feeBps = uint16(_newFee);
+        uint16 _fee = uint16(_newFee);
+        assembly{
+            sstore(feeBps.slot,_fee)
+        }
+        //feeBps = uint16(_newFee);
         emit FlashFeeSet(msg.sender, _oldFee, _newFee);
     }
```

> Gas diff

```diff
 | contracts/ActivePool.sol:ActivePool contract |                 |       |        |        |         |
 |----------------------------------------------|-----------------|-------|--------|--------|---------|
 | Deployment Cost                              | Deployment Size |       |        |        |         |
 | Function Name                                | min             | avg   | median | max    | # calls |
-| setFeeBps                                    | 50078           | 50078 | 50078  | 50078  | 1       |
+| setFeeBps                                    | 47244           | 47244 | 47244  | 47244  | 1       |

```