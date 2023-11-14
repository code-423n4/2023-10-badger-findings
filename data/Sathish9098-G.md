# GAS OPTIMIZATIONS

##

## [G-1] Optimizing storage usage with packed structs

### Saves ``8000 GAS`` , ``4 SLOT``

Each slot saved can avoid an extra Gsset (20000 gas) for the first setting of the struct.

Subsequent reads as well as writes have smaller gas savings.

### [G-1.1] user,isCollIncrease,isDebtIncrease can be packed with same slot : Saves ``2 SLOT`` , ``4000 GAS``

https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L97-L104

```diff
FILE: Breadcrumbs2023-10-badger/packages/contracts/contracts/BorrowerOperations.sol

 struct MoveTokensParams {
        address user;
+        bool isCollIncrease;
+        bool isDebtIncrease;
        uint256 collSharesChange;
        uint256 collAddUnderlying; // ONLY for isCollIncrease=true
-        bool isCollIncrease;
        uint256 netDebtChange;
-        bool isDebtIncrease;
    }

```

### [G-1.2]  roundEthBtcId , roundStEthEthId , success can be packed with same slot : Saves 1 SLOT , 2000 GAS

https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Interfaces/IPriceFeed.sol#L17-L24

```diff
FILE: 2023-10-badger/packages/contracts/contracts/Interfaces/IPriceFeed.sol

 struct ChainlinkResponse {
        uint80 roundEthBtcId;
        uint80 roundStEthEthId;
+        bool success;
        uint256 answer;
        uint256 timestampEthBtc;
        uint256 timestampStEthEth;
-        bool success;
    }


```

### [G-1.3]  timestamp , success can be packed with same slot : Saves ``1 SLOT`` , ``2000 GAS``

https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Interfaces/IPriceFeed.sol#L26-L30

```diff
FILE: 2023-10-badger/packages/contracts/contracts/Interfaces/IPriceFeed.sol

  struct FallbackResponse {
        uint256 answer;
-        uint256 timestamp;
+        uint248 timestamp;
        bool success;
    }

```

##

## [G-2] State variables can be packed into fewer storage slots

### Saves ``2000 GAS`` , ``1 SLOT``

The EVM works with 32 byte words. Variables less than 32 bytes can be declared next to eachother in storage and this will pack the values together into a single 32 byte storage slot (if the values combined are <= 32 bytes). If the variables packed together are retrieved together in functions we will effectively save ~2000 gas with every subsequent SLOAD for that storage slot. This is due to us incurring a Gwarmaccess (100 gas) versus a Gcoldsload (2100 gas).

### [G-2.1]  ``minuteDecayFactor`` and ``redemptionsPaused`` can be packed within same slot : Saves ``2000 GAS`` , ``1 SLOT``

https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L143-L148


``minuteDecayFactor`` value is not exceeds the ``MAX_MINUTE_DECAY_FACTOR = 999999999999999999`` because this check ``_minuteDecayFactor <= MAX_MINUTE_DECAY_FACTOR`` in ``setMinuteDecayFactor() `` function. So we can downcast this to ``uint248`` so down casting is safe.

```solidity
        require(
            _minuteDecayFactor <= MAX_MINUTE_DECAY_FACTOR,
            "CDPManager: new minute decay factor out of range"
        );

```

```diff
FILE: 2023-10-badger/packages/contracts/contracts/CdpManagerStorage.sol

 bool public redemptionsPaused;
    /*
     * Half-life of 12h. 12h = 720 min
     * (1/2) = d^720 => d = (1/2)^(1/720)
     */
-    uint256 public minuteDecayFactor = 999037758833783000;
+    uint248 public minuteDecayFactor = 999037758833783000;
    uint256 public constant MIN_MINUTE_DECAY_FACTOR = 1; // Non-zero
    uint256 public constant MAX_MINUTE_DECAY_FACTOR = 999999999999999999; // Corresponds to a very fast decay rate, but not too extreme

```

##

## [G-3] Remove or replace unused state variables

### Saves ``40000 GAS`` with ``2 instances``

Saves a storage slot. If the variable is assigned a non-zero value, saves ``Gsset (20000 gas)``. If it's assigned a zero value, saves ``Gsreset (2900 gas)``. If the variable remains unassigned, there is no gas savings unless the variable is public, in which case the compiler-generated non-payable getter deployment cost is saved. If the state variable is overriding an interface's public function, mark the variable as constant or immutable so that it does not use a storage slot.

```solidity
FILE: 2023-10-badger/packages/contracts/contracts/Dependencies/RolesAuthority.sol

30: EnumerableSet.Bytes32Set internal enabledFunctionSigsPublic;

```
https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L30

```solidity
FILE: 2023-10-badger/packages/contracts/contracts/Governor.sol

17: bytes32 NO_ROLES = bytes32(0);

```
https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Governor.sol#L17

##

## [G-4] ``systemCollShares`` should be cached 

### Saves ``100 GAS`` ,``1 SLOD``

https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/ActivePool.sol#L294-L300

```diff
FILE: Breadcrumbs2023-10-badger/packages/contracts/contracts/ActivePool.sol

+ uint256 systemCollShares_ = systemCollShares;
 require(
-            collateral.balanceOf(address(this)) >= collateral.getPooledEthByShares(systemCollShares),
+            collateral.balanceOf(address(this)) >= collateral.getPooledEthByShares(systemCollShares_ ),
            "ActivePool: Must repay Balance"
        );
        require(
-            collateral.sharesOf(address(this)) >= systemCollShares,
+            collateral.sharesOf(address(this)) >= systemCollShares_ ,
            "ActivePool: Must repay Share"
        );


```

### [G-5] ``lastRedemptionTimestamp`` should be cached 

### Saves ``400 GAS`` , ``4 SLOD``

https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L689-L699


```diff
FILE: 2023-10-badger/packages/contracts/contracts/CdpManager.sol

 function _updateLastRedemptionTimestamp() internal {
+  uint256 lastRedemptionTimestamp_ = lastRedemptionTimestamp ;
-        uint256 timePassed = block.timestamp > lastRedemptionTimestamp
+        uint256 timePassed = block.timestamp > lastRedemptionTimestamp_ 
-            ? block.timestamp - lastRedemptionTimestamp
+            ? block.timestamp - lastRedemptionTimestamp_ 
            : 0;

        if (timePassed >= SECONDS_IN_ONE_MINUTE) {
            // Using the effective elapsed time that is consumed so far to update lastRedemptionTimestamp
            // instead block.timestamp for consistency with _calcDecayedBaseRate()
-            lastRedemptionTimestamp += _minutesPassedSinceLastRedemption() * SECONDS_IN_ONE_MINUTE;
+            lastRedemptionTimestamp = lastRedemptionTimestamp_ + _minutesPassedSinceLastRedemption() * SECONDS_IN_ONE_MINUTE;
            emit LastRedemptionTimestampUpdated(block.timestamp);
        }
    }


 function _minutesPassedSinceLastRedemption() internal view returns (uint256) {

+  uint256 lastRedemptionTimestamp_ = lastRedemptionTimestamp ;
        return
-            block.timestamp > lastRedemptionTimestamp
+            block.timestamp > lastRedemptionTimestamp_ 
-                ? ((block.timestamp - lastRedemptionTimestamp) / SECONDS_IN_ONE_MINUTE)
+                ? ((block.timestamp - lastRedemptionTimestamp_ ) / SECONDS_IN_ONE_MINUTE)
                : 0;
    }


```

## 

## [G-6]  ``Cdps[_redeemColFromCdp.cdpId].debt`` should be cached 

### Saves ``100 GAS``

```diff
FILE: 2023-10-badger/packages/contracts/contracts/CdpManager.sol

 + uint256 debt_ = Cdps[_redeemColFromCdp.cdpId].debt ;
singleRedemption.debtToRedeem = EbtcMath._min(
            _redeemColFromCdp.maxEBTCamount,
-            Cdps[_redeemColFromCdp.cdpId].debt /// @audit Redeem everything
+            debt_  /// @audit Redeem everything
        );

        singleRedemption.collSharesDrawn = collateral.getSharesByPooledEth(
            (singleRedemption.debtToRedeem * DECIMAL_PRECISION) / _redeemColFromCdp.price
        );

        // Repurposing this struct here to avoid stack too deep.
        CdpDebtAndCollShares memory _oldDebtAndColl = CdpDebtAndCollShares(
-            Cdps[_redeemColFromCdp.cdpId].debt,
+            debt_,
            Cdps[_redeemColFromCdp.cdpId].coll
        );

```
##

## [G-7] ``getUserRoles[user]`` should  be cached 

### Saves 100 GAS

https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L154-L160

```diff
FILE: Breadcrumbs2023-10-badger/packages/contracts/contracts/Dependencies/RolesAuthority.sol

} else {
+  bytes32 user_ = getUserRoles[user] ;
-            getUserRoles[user] &= ~bytes32(1 << role);
+            user_ &= ~bytes32(1 << role);

            // Remove user if no more roles
-            if (getUserRoles[user] == bytes32(0)) {
+            if (user_ == bytes32(0)) {
                users.remove(user);
            }

```

##

## [G-8] The result of ``sortedCdps.nonExistId()`` call should be cached rather than re-calling the function 

The instances below point to the second+ call of the function within a single function

### Saves 1 external call and ``2100 GAS ``

https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L277-L285

```solidity

function _isValidFirstRedemptionHint(
        bytes32 _firstRedemptionHint,
        uint256 _price
    ) internal view returns (bool) {
+  bytes32 nonExistId_ = sortedCdps.nonExistId() ;
        if (
-            _firstRedemptionHint == sortedCdps.nonExistId() ||
+            _firstRedemptionHint == nonExistId_ ||
            !sortedCdps.contains(_firstRedemptionHint) ||
            getSyncedICR(_firstRedemptionHint, _price) < MCR
        ) {
            return false;
        }

        bytes32 nextCdp = sortedCdps.getNext(_firstRedemptionHint);
-        return nextCdp == sortedCdps.nonExistId() || getSyncedICR(nextCdp, _price) < MCR;
+        return nextCdp == nonExistId_ || getSyncedICR(nextCdp, _price) < MCR;
    }

```

##

## [G-9] Emit memory or constant variables instead of state variables 

Emitting memory or constant variables instead of state variables in Solidity events can be a useful optimization technique, particularly in the context of gas efficiency and contract optimization

```diff
FILE: Breadcrumbs2023-10-badger/packages/contracts/contracts/CdpManager.sol

 53:  stakingRewardSplit = STAKING_REWARD_SPLIT;
54:        // Emit initial value for analytics
- 55:        emit StakingRewardSplitSet(stakingRewardSplit);
+ 55:        emit StakingRewardSplitSet(STAKING_REWARD_SPLIT);

```

##

## [G-10] Multiple address/ID mappings can be combined into a single mapping of an address/ID to a struct, where appropriate

Saves a storage slot for the mapping. Depending on the circumstances and sizes of types, can avoid a Gsset (20000 gas) per mapping combined. Reads and subsequent writes can also be cheaper when a function requires both values and they both fit in the same storage slot. Finally, if both fields are accessed in the same function, can save ~42 gas per access due to not having to recalculate the key’s keccak256 hash (Gkeccak256 - 30 gas) and that calculation’s associated stack operations.

```diff
FILE: 2023-10-badger/packages/contracts/contracts/Dependencies/RolesAuthority.sol

32: mapping(address => bytes32) public getUserRoles;
36: mapping(address => mapping(bytes4 => bytes32)) public getRolesWithCapability;

```
https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L32-L36














