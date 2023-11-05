# Summary

Some optimizations were benchmarked via the protocol's tests. Optimizations that were not benchmarked are explained properly. The following command was used to run the tests for the benchmarks below: `forge test` and the gas report was generated using `forge test --gas-report`

## Gas Optimizations

| Number        | Issue                                                                                          | Instances |
| ------------- | :--------------------------------------------------------------------------------------------- | :-------: |
| [G-01](#g-01) | State variables that are used multiple times in a function should be cached in stack variables |     4     |
| [G-02](#g-02) | Structs can be packed into fewer storage slots                                                 |     1     |
| [G-03](#g-03) | State variables can be packed into fewer storage slots                                         |     1     |
| [G-04](#g-04) | Use do while loops instead of for loops                                                        |     8     |
| [G-05](#g-05) | Use nested if statements instead of &&                                                         |     9     |
| [G-06](#g-06) | Use hardcode address instead of address(this)                                                  |     9     |
| [G-07](#g-07) | Do not calculate constants                                                                     |     2     |
| [G-08](#g-08) | Use assembly to compute hashes to save gas                                                     |     4     |
| [G-09](#g-09) | Use constants instead of type(uintx).max                                                       |     3     |

<a name='g-01'></a>

## [G-01] State variables that are used multiple times in a function should be cached in stack variables

_The following instances are missed in the 4naly3er report_

When performing multiple operations on a state variable in a function, it is recommended to cache it first. Either multiple reads or multiple writes to a state variable can save gas by caching it on the stack. Caching of a state variable replaces each Gwarmaccess `100 gas` with a much cheaper stack read. Other less obvious fixes/optimizations include having local memory caches of state variable structs, or having local caches of state variable contracts/addresses. Saves 100 gas per instance.

Total Instances: `4`

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L299C12-L299C68

Gas savings for `ActivePool.flashLoan`, obtained via protocol's tests:

|        | Min | Avg   | Median | Max    | # calls |
| ------ | --- | ----- | ------ | ------ | ------- |
| Before | 809 | 78383 | 42717  | 324532 | 13      |
| After  | 809 | 78355 | 42717  | 324431 | 13      |

```solidity
File: packages/contracts/contracts/ActivePool.sol

//@audit  systemCollShares at line 295
299:  collateral.sharesOf(address(this)) >= systemCollShares,

```

```diff
diff --git a/packages/contracts/contracts/ActivePool.sol b/packages/contracts/contracts/ActivePool.sol
index 40b6a1f..180e5e4 100644
--- a/packages/contracts/contracts/ActivePool.sol
+++ b/packages/contracts/contracts/ActivePool.sol
@@ -291,12 +291,13 @@ contract ActivePool is IActivePool, ERC3156FlashLender, ReentrancyGuard, BaseMat

         // NOTE: This check effectively prevents running 2 FL at the same time
         //  You technically could, but you'd be having to repay any amount below systemCollShares to get Fl2 to not revert
+        int256 _sc = systemCollShares;
         require(
-            collateral.balanceOf(address(this)) >= collateral.getPooledEthByShares(systemCollShares),
+            collateral.balanceOf(address(this)) >= collateral.getPooledEthByShares(_sc),
             "ActivePool: Must repay Balance"
         );
         require(
-            collateral.sharesOf(address(this)) >= systemCollShares,
+            collateral.sharesOf(address(this)) >= _sc,
             "ActivePool: Must repay Share"
         );
         require(


```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L454

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

//@audit  totalStakesSnapshot at line 453
//@audit  totalCollateralSnapshot at line 443
454: stake = (_coll * totalStakesSnapshot) / totalCollateralSnapshot;

```

```diff
diff --git a/packages/contracts/contracts/CdpManagerStorage.sol b/packages/contracts/contracts/CdpManagerStorage.sol
index cd11ee4..73c1985 100644
--- a/packages/contracts/contracts/CdpManagerStorage.sol
+++ b/packages/contracts/contracts/CdpManagerStorage.sol
@@ -440,7 +440,9 @@ contract CdpManagerStorage is EbtcBase, ReentrancyGuard, ICdpManagerData, AuthNo
     // Calculate a new stake based on the snapshots of the totalStakes and totalCollateral taken at the last liquidation
     function _computeNewStake(uint256 _coll) internal view returns (uint256) {
         uint256 stake;
-        if (totalCollateralSnapshot == 0) {
+        uint256 _totalCollateralSnapshot = totalCollateralSnapshot;
+        uint256 _totalStakesSnapshot = totalStakesSnapshot;
+        if (_totalCollateralSnapshot == 0) {
             stake = _coll;
         } else {
             /*
@@ -450,8 +452,8 @@ contract CdpManagerStorage is EbtcBase, ReentrancyGuard, ICdpManagerData, AuthNo
              * so if all cdps were closed/liquidated,
              * rewards would’ve been emptied and totalCollateralSnapshot would be zero too.
              */
-            require(totalStakesSnapshot > 0, "CdpManagerStorage: zero totalStakesSnapshot!");
-            stake = (_coll * totalStakesSnapshot) / totalCollateralSnapshot;
+            require(_totalStakesSnapshot > 0, "CdpManagerStorage: zero totalStakesSnapshot!");
+            stake = (_coll * _totalStakesSnapshot) / _totalCollateralSnapshot;
         }
         return stake;
     }


```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L351C8-L351C29

Gas savings for `PricsFeed.fetchprice`, obtained via protocol's tests:

|        | Min   | Avg   | Median | Max   | # calls |
| ------ | ----- | ----- | ------ | ----- | ------- |
| Before | 17330 | 30705 | 20697  | 63959 | 6       |
| After  | 17333 | 29718 | 19656  | 65547 | 6       |

```solidity
File: packages/contracts/contracts/PriceFeed.sol

//@audit  lastGoodPrice at line 114,122,135,142,155,162,204,212,251,260,267,278,283,298,318,323,342
351: return lastGoodPrice;

```

```diff
diff --git a/packages/contracts/contracts/PriceFeed.sol b/packages/contracts/contracts/PriceFeed.sol
index ef244d4..ebb4e81 100644
--- a/packages/contracts/contracts/PriceFeed.sol
+++ b/packages/contracts/contracts/PriceFeed.sol
@@ -103,6 +103,7 @@ contract PriceFeed is BaseMath, IPriceFeed, AuthNoOwner {
             chainlinkResponse.roundStEthEthId
         );
         FallbackResponse memory fallbackResponse = _getCurrentFallbackResponse();
+        uint256 _lgp = lastGoodPrice;

         // --- CASE 1: System fetched last price from Chainlink  ---
         if (status == Status.chainlinkWorking) {
@@ -111,7 +112,7 @@ contract PriceFeed is BaseMath, IPriceFeed, AuthNoOwner {
                 // If Fallback is broken then both oracles are untrusted, so return the last good price
                 if (_fallbackIsBroken(fallbackResponse)) {
                     _changeStatus(Status.bothOraclesUntrusted);
-                    return lastGoodPrice;
+                    return _lgp;
                 }
                 /*
                  * If Fallback is only frozen but otherwise returning valid data, return the last good price.
@@ -119,7 +120,7 @@ contract PriceFeed is BaseMath, IPriceFeed, AuthNoOwner {
                  */
                 if (_fallbackIsFrozen(fallbackResponse)) {
                     _changeStatus(Status.usingFallbackChainlinkUntrusted);
-                    return lastGoodPrice;
+                    return _lgp;
                 }

                 // If Chainlink is broken and Fallback is working, switch to Fallback and return current Fallback price
@@ -132,14 +133,14 @@ contract PriceFeed is BaseMath, IPriceFeed, AuthNoOwner {
                 // If Fallback is broken too, remember Fallback broke, and return last good price
                 if (_fallbackIsBroken(fallbackResponse)) {
                     _changeStatus(Status.usingChainlinkFallbackUntrusted);
-                    return lastGoodPrice;
+                    return _lgp;
                 }

                 // If Fallback is frozen or working, remember Chainlink froze, and switch to Fallback
                 _changeStatus(Status.usingFallbackChainlinkFrozen);

                 if (_fallbackIsFrozen(fallbackResponse)) {
-                    return lastGoodPrice;
+                    return _lgp;
                 }

                 // If Fallback is working, use it
@@ -152,14 +153,14 @@ contract PriceFeed is BaseMath, IPriceFeed, AuthNoOwner {
                 // We don't trust CL for now given this large price differential
                 if (_fallbackIsBroken(fallbackResponse)) {
                     _changeStatus(Status.bothOraclesUntrusted);
-                    return lastGoodPrice;
+                    return _lgp;
                 }

                 // If Fallback is frozen, switch to Fallback and return last good price
                 // We don't trust CL for now given this large price differential
                 if (_fallbackIsFrozen(fallbackResponse)) {
                     _changeStatus(Status.usingFallbackChainlinkUntrusted);
-                    return lastGoodPrice;
+                    return _lgp;
                 }

                 /*
@@ -201,7 +202,7 @@ contract PriceFeed is BaseMath, IPriceFeed, AuthNoOwner {

             if (_fallbackIsBroken(fallbackResponse)) {
                 _changeStatus(Status.bothOraclesUntrusted);
-                return lastGoodPrice;
+                return _lgp;
             }

             /*
@@ -209,7 +210,7 @@ contract PriceFeed is BaseMath, IPriceFeed, AuthNoOwner {
              * Fallback may need to be tipped to return current data.
              */
             if (_fallbackIsFrozen(fallbackResponse)) {
-                return lastGoodPrice;
+                return _lgp;
             }

             // Otherwise, use Fallback price
@@ -248,7 +249,7 @@ contract PriceFeed is BaseMath, IPriceFeed, AuthNoOwner {
             }

             // Otherwise, return the last good price - both oracles are still untrusted (no status change)
-            return lastGoodPrice;
+            return _lgp;
         }

         // --- CASE 4: Using Fallback, and Chainlink is frozen ---
@@ -257,14 +258,14 @@ contract PriceFeed is BaseMath, IPriceFeed, AuthNoOwner {
                 // If both Oracles are broken, return last good price
                 if (_fallbackIsBroken(fallbackResponse)) {
                     _changeStatus(Status.bothOraclesUntrusted);
-                    return lastGoodPrice;
+                    return _lgp;
                 }

                 // If Chainlink is broken, remember it and switch to using Fallback
                 _changeStatus(Status.usingFallbackChainlinkUntrusted);

                 if (_fallbackIsFrozen(fallbackResponse)) {
-                    return lastGoodPrice;
+                    return _lgp;
                 }

                 // If Fallback is working, return Fallback current price
@@ -275,12 +276,12 @@ contract PriceFeed is BaseMath, IPriceFeed, AuthNoOwner {
                 // if Chainlink is frozen and Fallback is broken, remember Fallback broke, and return last good price
                 if (_fallbackIsBroken(fallbackResponse)) {
                     _changeStatus(Status.usingChainlinkFallbackUntrusted);
-                    return lastGoodPrice;
+                    return _lgp;
                 }

                 // If both are frozen, just use lastGoodPrice
                 if (_fallbackIsFrozen(fallbackResponse)) {
-                    return lastGoodPrice;
+                    return _lgp;
                 }

                 // if Chainlink is frozen and Fallback is working, keep using Fallback (no status change)
@@ -295,7 +296,7 @@ contract PriceFeed is BaseMath, IPriceFeed, AuthNoOwner {

             // If Chainlink is live and Fallback is frozen, just use last good price (no status change) since we have no basis for comparison
             if (_fallbackIsFrozen(fallbackResponse)) {
-                return lastGoodPrice;
+                return _lgp;
             }

             // If Chainlink is live and Fallback is working, compare prices. Switch to Chainlink
@@ -315,12 +316,12 @@ contract PriceFeed is BaseMath, IPriceFeed, AuthNoOwner {
             // If Chainlink breaks, now both oracles are untrusted
             if (_chainlinkIsBroken(chainlinkResponse, prevChainlinkResponse)) {
                 _changeStatus(Status.bothOraclesUntrusted);
-                return lastGoodPrice;
+                return _lgp;
             }

             // If Chainlink is frozen, return last good price (no status change)
             if (_chainlinkIsFrozen(chainlinkResponse)) {
-                return lastGoodPrice;
+                return _lgp;
             }

             // If Chainlink and Fallback are both live, unbroken and similar price, switch back to chainlinkWorking and return Chainlink price
@@ -348,7 +349,7 @@ contract PriceFeed is BaseMath, IPriceFeed, AuthNoOwner {
         }

         /// @audit This should never be used, but we added it for the Certora Prover
-        return lastGoodPrice;
+        return _lgp;
     }


```

<a name='g-02'></a>

## [G-02] Structs can be packed into fewer storage slots

Each slot saved can avoid an extra Gsset (20000 gas) for the first setting of the struct.

### `user` can be packed with `isCollIncrease`, `isDebtIncrease` . Saves `4000 GAS` , `2 SLOT`

Total Instances: `1`

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L97C5-L104C6

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

97:struct MoveTokensParams {
98:        address user;
99:        uint256 collSharesChange;
100:        uint256 collAddUnderlying; // ONLY for isCollIncrease=true
101:        bool isCollIncrease;
102:        uint256 netDebtChange;
103:        bool isDebtIncrease;
104:    }

```

```diff
diff --git a/packages/contracts/contracts/BorrowerOperations.sol b/packages/contracts/contracts/BorrowerOperations.sol
index db7a32e..66fb9cb 100644
--- a/packages/contracts/contracts/BorrowerOperations.sol
+++ b/packages/contracts/contracts/BorrowerOperations.sol
@@ -96,11 +96,12 @@ contract BorrowerOperations is

     struct MoveTokensParams {
         address user;
+        bool isCollIncrease;
+        bool isDebtIncrease;
         uint256 collSharesChange;
         uint256 collAddUnderlying; // ONLY for isCollIncrease=true
-        bool isCollIncrease;
         uint256 netDebtChange;
-        bool isDebtIncrease;
+
     }

     // --- Dependency setters ---
@@ -426,11 +427,12 @@ contract BorrowerOperations is
         {
             MoveTokensParams memory _varMvTokens = MoveTokensParams(
                 msg.sender,
+                vars.isCollIncrease,
+                _isDebtIncrease,
                 vars.collSharesChange,
                 (vars.isCollIncrease ? _stEthBalanceIncrease : 0),
-                vars.isCollIncrease,
-                _debtChange,
-                _isDebtIncrease
+                _debtChange
+
             );
             _processTokenMovesFromAdjustment(_varMvTokens);
         }

```

<a name='g-03'></a>

## [G-03] State variables can be packed into fewer storage slots

The EVM works with 32 byte words. Variables less than 32 bytes can be declared next to eachother in storage and this will pack the values together into a single 32 byte storage slot (if the values combined are <= 32 bytes). If the variables packed together are retrieved together in functions we will effectively save ~2000 gas with every subsequent SLOAD for that storage slot. This is due to us incurring a `Gwarmaccess (100 gas)` versus a `Gcoldsload (2100 gas)`.

Total Instances: `1`

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L143C1-L166C44

### Pack `redemptionsPaused`, `lastRedemptionTimestamp` into one storage slot to save 1 SLOTs (~2000 gas)

**Note: In order to do this optimization we will need to reduce the `uint` type for `lastRedemptionTimestamp` to `uint128`. This `uint` type should be large enough to hold timestamp values.**

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

143:    bool public redemptionsPaused;
144:    /*
145:     * Half-life of 12h. 12h = 720 min
146:     * (1/2) = d^720 => d = (1/2)^(1/720)
147:     */
148:    uint256 public minuteDecayFactor = 999037758833783000;
149:    uint256 public constant MIN_MINUTE_DECAY_FACTOR = 1; // Non-zero
150:    uint256 public constant MAX_MINUTE_DECAY_FACTOR = 999999999999999999; // Corresponds to a very fast decay rate, but not too extreme
151:
152:    uint256 internal immutable deploymentStartTime;
153:
154:    /*
155:     * BETA: 18 digit decimal. Parameter by which to divide the redeemed fraction,
156:     * in order to calc the new base rate from a redemption.
157:     * Corresponds to (1 / ALPHA) in the Liquity white paper.
158:     */
159:    uint256 public beta = 2;
160:
161:    uint256 public baseRate;
162:
163:    uint256 public stakingRewardSplit;
164:
165:    // The timestamp of the latest fee operation (redemption or new EBTC issuance)
166:    uint256 public lastRedemptionTimestamp;

```

```diff
diff --git a/packages/contracts/contracts/CdpManager.sol b/packages/contracts/contracts/CdpManager.sol
index 71b82b2..59cb106 100644
--- a/packages/contracts/contracts/CdpManager.sol
+++ b/packages/contracts/contracts/CdpManager.sol
@@ -687,15 +687,15 @@ contract CdpManager is CdpManagerStorage, ICdpManager, Proxy {

     // Update the last fee operation time only if time passed >= decay interval. This prevents base rate griefing.
     function _updateLastRedemptionTimestamp() internal {
-        uint256 timePassed = block.timestamp > lastRedemptionTimestamp
-            ? block.timestamp - lastRedemptionTimestamp
+        uint128 timePassed = uint128(block.timestamp) > lastRedemptionTimestamp
+            ? uint128(block.timestamp) - lastRedemptionTimestamp
             : 0;

-        if (timePassed >= SECONDS_IN_ONE_MINUTE) {
+        if (timePassed >= uint128(SECONDS_IN_ONE_MINUTE)) {
             // Using the effective elapsed time that is consumed so far to update lastRedemptionTimestamp
             // instead block.timestamp for consistency with _calcDecayedBaseRate()
-            lastRedemptionTimestamp += _minutesPassedSinceLastRedemption() * SECONDS_IN_ONE_MINUTE;
-            emit LastRedemptionTimestampUpdated(block.timestamp);
+            lastRedemptionTimestamp += _minutesPassedSinceLastRedemption() * uint128(SECONDS_IN_ONE_MINUTE);
+            emit LastRedemptionTimestampUpdated(uint128(block.timestamp));
         }
     }

@@ -706,10 +706,10 @@ contract CdpManager is CdpManagerStorage, ICdpManager, Proxy {
         return (baseRate * decayFactor) / DECIMAL_PRECISION;
     }

-    function _minutesPassedSinceLastRedemption() internal view returns (uint256) {
+    function _minutesPassedSinceLastRedemption() internal view returns (uint128) {
         return
-            block.timestamp > lastRedemptionTimestamp
-                ? ((block.timestamp - lastRedemptionTimestamp) / SECONDS_IN_ONE_MINUTE)
+            uint128(block.timestamp) > lastRedemptionTimestamp
+                ? ((uint128(block.timestamp) - lastRedemptionTimestamp) / uint128(SECONDS_IN_ONE_MINUTE))
                 : 0;
     }

diff --git a/packages/contracts/contracts/CdpManagerStorage.sol b/packages/contracts/contracts/CdpManagerStorage.sol
index cd11ee4..37c76b0 100644
--- a/packages/contracts/contracts/CdpManagerStorage.sol
+++ b/packages/contracts/contracts/CdpManagerStorage.sol
@@ -141,6 +141,8 @@ contract CdpManagerStorage is EbtcBase, ReentrancyGuard, ICdpManagerData, AuthNo
     uint256 public constant MIN_REDEMPTION_FEE_FLOOR = (DECIMAL_PRECISION * 5) / 1000; // 0.5%
     uint256 public redemptionFeeFloor = MIN_REDEMPTION_FEE_FLOOR;
     bool public redemptionsPaused;
+        // The timestamp of the latest fee operation (redemption or new EBTC issuance)
+    uint128 public lastRedemptionTimestamp;
     /*
      * Half-life of 12h. 12h = 720 min
      * (1/2) = d^720 => d = (1/2)^(1/720)
@@ -162,8 +164,7 @@ contract CdpManagerStorage is EbtcBase, ReentrancyGuard, ICdpManagerData, AuthNo

     uint256 public stakingRewardSplit;

-    // The timestamp of the latest fee operation (redemption or new EBTC issuance)
-    uint256 public lastRedemptionTimestamp;
+

     mapping(bytes32 => Cdp) public Cdps;

diff --git a/packages/contracts/contracts/TestContracts/CDPManagerTester.sol b/packages/contracts/contracts/TestContracts/CDPManagerTester.sol
index 6b80647..43d3f6c 100644
--- a/packages/contracts/contracts/TestContracts/CDPManagerTester.sol
+++ b/packages/contracts/contracts/TestContracts/CDPManagerTester.sol
@@ -80,7 +80,7 @@ contract CdpManagerTester is CdpManager {
     }

     function setLastFeeOpTimeToNow() external {
-        lastRedemptionTimestamp = block.timestamp;
+        lastRedemptionTimestamp = uint128(block.timestamp);
     }


```

<a name='g-04'></a>

## [G-04] Use do while loops instead of for loops

A do while loop will cost less gas since the condition is not being checked for the first iteration. Other optimizations, such as caching length, precrementing, redundant initialisation with default value and using unchecked blocks are also included for further optimisation.

Total Instances: `8`

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L46
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L57
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L76
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L84
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L98
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L107
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L122
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L137C13-L137C57

Gas savings for `Governor.getUsersByRole`, obtained via protocol's tests:

|        | Min   | Avg   | Median | Max   | # calls |
| ------ | ----- | ----- | ------ | ----- | ------- |
| Before | 10785 | 10785 | 10785  | 10785 | 1       |
| After  | 7897  | 7897  | 7897   | 7897  | 1       |

The gas savings for `Governor.getRolesForUser`,`Governor.getRolesFromByteMap`,`Governor.getByteMapFromRoles`and `Governor.getEnabledFunctionsInTarget` are not specified as they are not included in test

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

46:  for (uint256 i = 0; i < users.length(); i++) {

57:  for (uint256 i = 0; i < _usrs.length; i++) {

76:  for (uint8 i = 0; i < type(uint8).max; i++) {

84:  for (uint8 i = 0; i < type(uint8).max; i++) {

98:  for (uint8 i = 0; i < type(uint8).max; i++) {

107: for (uint8 i = 0; i < type(uint8).max; i++) {

122: for (uint8 i = 0; i < roleIds.length; i++) {

137: for (uint256 i = 0; i < _sigs.length; ++i) {

```

```diff
diff --git a/packages/contracts/contracts/Governor.sol b/packages/contracts/contracts/Governor.sol
index 0195952..6c56f99 100644
--- a/packages/contracts/contracts/Governor.sol
+++ b/packages/contracts/contracts/Governor.sol
@@ -43,25 +43,35 @@ contract Governor is RolesAuthority {
     function getUsersByRole(uint8 role) external view returns (address[] memory usersWithRole) {
         // Search over all users: O(n) * 2
         uint256 count;
-        for (uint256 i = 0; i < users.length(); i++) {
+        uint256 i;
+        uint256 users_length = users.length();
+        do{
             address user = users.at(i);
             bool _canCall = doesUserHaveRole(user, role);
             if (_canCall) {
                 count += 1;
             }
-        }
+            unchecked{
+                ++i;
+            }
+        }while(i < users_length);
         if (count > 0) {
             uint256 j = 0;
             usersWithRole = new address[](count);
             address[] memory _usrs = users.values();
-            for (uint256 i = 0; i < _usrs.length; i++) {
+            uint256 i;
+            uint256 _usrs_length = _usrs.length;
+            do{
                 address user = _usrs[i];
                 bool _canCall = doesUserHaveRole(user, role);
                 if (_canCall) {
                     usersWithRole[j] = user;
                     j++;
                 }
-            }
+                unchecked{
+                    ++i;
+                }
+            }while(i<_usrs_length);
         }
     }

@@ -73,20 +83,28 @@ contract Governor is RolesAuthority {
     function getRolesForUser(address user) external view returns (uint8[] memory rolesForUser) {
         // Enumerate over all possible roles and check if enabled
         uint256 count;
-        for (uint8 i = 0; i < type(uint8).max; i++) {
+        uint8 i;
+        do {
             if (doesUserHaveRole(user, i)) {
                 count += 1;
             }
-        }
+            unchecked{
+                ++i;
+            }
+        }while(i<255);
         if (count > 0) {
             uint256 j = 0;
             rolesForUser = new uint8[](count);
-            for (uint8 i = 0; i < type(uint8).max; i++) {
-                if (doesUserHaveRole(user, i)) {
-                    rolesForUser[j] = i;
+            uint8 k;
+            do {
+                if (doesUserHaveRole(user, k)) {
+                    rolesForUser[j] = k;
                     j++;
                 }
-            }
+                unchecked{
+                    ++k;
+                }
+            }while(k<255);
         }
     }

@@ -95,22 +113,31 @@ contract Governor is RolesAuthority {
     /// @return roleIds An array of role IDs extracted from the byte map.
     function getRolesFromByteMap(bytes32 byteMap) public pure returns (uint8[] memory roleIds) {
         uint256 count;
-        for (uint8 i = 0; i < type(uint8).max; i++) {
+        uint8 i;
+        do {
             bool roleEnabled = (uint256(byteMap >> i) & 1) != 0;
             if (roleEnabled) {
                 count += 1;
             }
-        }
+            unchecked{
+                    ++i;
+                }
+
+        }while(i<255);
         if (count > 0) {
             uint256 j = 0;
             roleIds = new uint8[](count);
-            for (uint8 i = 0; i < type(uint8).max; i++) {
-                bool roleEnabled = (uint256(byteMap >> i) & 1) != 0;
+            uint8 k;
+            do{
+                bool roleEnabled = (uint256(byteMap >> k) & 1) != 0;
                 if (roleEnabled) {
-                    roleIds[j] = i;
+                    roleIds[j] = k;
                     j++;
                 }
-            }
+                unchecked{
+                    ++k;
+                }
+            }while(k<255);
         }
     }

@@ -119,9 +146,14 @@ contract Governor is RolesAuthority {
     /// @return A bytes32 value encoding the roles.
     function getByteMapFromRoles(uint8[] memory roleIds) public pure returns (bytes32) {
         bytes32 _data;
-        for (uint8 i = 0; i < roleIds.length; i++) {
+        uint8 i;
+        uint256 _roleIds_length =  roleIds.length;
+        do {
             _data |= bytes32(1 << uint256(roleIds[i]));
-        }
+            unchecked{
+                ++i;
+            }
+        }while(i< _roleIds_length);
         return _data;
     }

@@ -134,9 +166,14 @@ contract Governor is RolesAuthority {
         bytes32[] memory _sigs = enabledFunctionSigsByTarget[_target].values();
         if (_sigs.length > 0) {
             _funcs = new bytes4[](_sigs.length);
-            for (uint256 i = 0; i < _sigs.length; ++i) {
+            uint256 i;
+            uint256 _sigs_length = _sigs.length;
+            do {
                 _funcs[i] = bytes4(_sigs[i]);
-            }
+                unchecked{
+                    ++i;
+                }
+            }while(i<_sigs_length);
         }
     }

```

<a name='g-05'></a>

## [G-05] Use nested if statements instead of &&

If the if statement has a logical AND and is not followed by an else statement, it can be replaced with 2 if statements.

```
contract NestedIfTest {

    //Execution cost: 22334 gas
    function funcBad(uint256 input) public pure returns (string memory) {
       if (input<10 && input>0 && input!=6){
           return "If condition passed";
       }

   }

    //Execution cost: 22294 gas
    function funcGood(uint256 input) public pure returns (string memory) {
    if (input<10) {
        if (input>0){
            if (input!=6){
                return "If condition passed";
            }
        }
    }
   }
}

```

Total Instances: `9`

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L393

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol
393: if (!_isDebtIncrease && _debtChange > 0) {
```

```diff
diff --git a/packages/contracts/contracts/BorrowerOperations.sol b/packages/contracts/contracts/BorrowerOperations.sol
index db7a32e..202607f 100644
--- a/packages/contracts/contracts/BorrowerOperations.sol
+++ b/packages/contracts/contracts/BorrowerOperations.sol
@@ -390,10 +390,13 @@ contract BorrowerOperations is
         );

         // When the adjustment is a debt repayment, check it's a valid amount, that the caller has enough EBTC, and that the resulting debt is >0
-        if (!_isDebtIncrease && _debtChange > 0) {
+        if (!_isDebtIncrease) {
+            if(_debtChange > 0){
             _requireValidDebtRepayment(vars.debt, vars.netDebtChange);
             _requireSufficientEbtcTokenBalance(msg.sender, vars.netDebtChange);
             _requireNonZeroDebt(vars.debt - vars.netDebtChange);
+            }
+
         }

         (vars.newCollShares, vars.newDebt) = _getNewCdpAmounts(

```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L158
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L756
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L760
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L790C17-L790C85
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L819

```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

158: liquidationValues.totalCollToSendToLiquidator == 0 &&

756:  if (vars.cdpId != bytes32(0) && Cdps[vars.cdpId].status == Status.active) {

760:  !vars.backToNormalMode &&

790: } else if (vars.backToNormalMode && _checkICRAgainstMCR(vars.ICR)) {

819: if (vars.cdpId != bytes32(0) && Cdps[vars.cdpId].status == Status.active) {

```

```diff
diff --git a/packages/contracts/contracts/LiquidationLibrary.sol b/packages/contracts/contracts/LiquidationLibrary.sol
index 0faf2cc..d48b4a7 100644
--- a/packages/contracts/contracts/LiquidationLibrary.sol
+++ b/packages/contracts/contracts/LiquidationLibrary.sol
@@ -154,18 +154,17 @@ contract LiquidationLibrary is CdpManagerStorage {
                 liquidationValues.debtToBurn,
                 liquidationValues.totalCollToSendToLiquidator
             ) = _liquidateCDPPartially(_liqState);
-            if (
-                liquidationValues.totalCollToSendToLiquidator == 0 &&
-                liquidationValues.debtToBurn == 0
-            ) {
+            if (liquidationValues.totalCollToSendToLiquidator == 0) {
+                if (liquidationValues.debtToBurn == 0) {
+                    (
+                        liquidationValues.debtToBurn,
+                        liquidationValues.totalCollToSendToLiquidator,
+                        liquidationValues.debtToRedistribute,
+                        liquidationValues.liquidatorCollSharesReward,
+                        liquidationValues.collSurplus
+                    ) = _liquidateCdpInGivenMode(_liqState, _recoveryState);
+                }
                 // retry with fully liquidation
-                (
-                    liquidationValues.debtToBurn,
-                    liquidationValues.totalCollToSendToLiquidator,
-                    liquidationValues.debtToRedistribute,
-                    liquidationValues.liquidatorCollSharesReward,
-                    liquidationValues.collSurplus
-                ) = _liquidateCdpInGivenMode(_liqState, _recoveryState);
             }
         }

@@ -753,47 +752,54 @@ contract LiquidationLibrary is CdpManagerStorage {
         for (vars.i = _start; ; ) {
             vars.cdpId = _cdpArray[vars.i];
             // only for active cdps
-            if (vars.cdpId != bytes32(0) && Cdps[vars.cdpId].status == Status.active) {
-                vars.ICR = getSyncedICR(vars.cdpId, _price);
-
-                if (
-                    !vars.backToNormalMode &&
-                    (_checkICRAgainstMCR(vars.ICR) || canLiquidateRecoveryMode(vars.ICR, _TCR))
-                ) {
-                    vars.price = _price;
-                    _syncAccounting(vars.cdpId);
-                    _getLiquidationValuesRecoveryMode(
-                        _price,
-                        vars.entireSystemDebt,
-                        vars.entireSystemColl,
-                        vars,
-                        singleLiquidation
-                    );
-
-                    // Update aggregate trackers
-                    vars.entireSystemDebt = vars.entireSystemDebt - singleLiquidation.debtToBurn;
-                    vars.entireSystemColl =
-                        vars.entireSystemColl -
-                        singleLiquidation.totalCollToSendToLiquidator -
-                        singleLiquidation.collSurplus;
-
-                    // Add liquidation values to their respective running totals
-                    totals = _addLiquidationValuesToTotals(totals, singleLiquidation);
-
-                    _TCR = _computeTCRWithGivenSystemValues(
-                        vars.entireSystemColl,
-                        vars.entireSystemDebt,
-                        _price
-                    );
-                    vars.backToNormalMode = _TCR < CCR ? false : true;
-                    _liqFlags[vars.i] = true;
-                } else if (vars.backToNormalMode && _checkICRAgainstMCR(vars.ICR)) {
-                    _syncAccounting(vars.cdpId);
-                    _getLiquidationValuesNormalMode(_price, _TCR, vars, singleLiquidation);
-
-                    // Add liquidation values to their respective running totals
-                    totals = _addLiquidationValuesToTotals(totals, singleLiquidation);
-                    _liqFlags[vars.i] = true;
+            if (vars.cdpId != bytes32(0)) {
+                if (Cdps[vars.cdpId].status == Status.active) {
+                    vars.ICR = getSyncedICR(vars.cdpId, _price);
+
+                    if (!vars.backToNormalMode) {
+                        if (
+                            _checkICRAgainstMCR(vars.ICR) || canLiquidateRecoveryMode(vars.ICR, _TCR)
+                        ) {
+                            vars.price = _price;
+                            _syncAccounting(vars.cdpId);
+                            _getLiquidationValuesRecoveryMode(
+                                _price,
+                                vars.entireSystemDebt,
+                                vars.entireSystemColl,
+                                vars,
+                                singleLiquidation
+                            );
+
+                            // Update aggregate trackers
+                            vars.entireSystemDebt =
+                                vars.entireSystemDebt -
+                                singleLiquidation.debtToBurn;
+                            vars.entireSystemColl =
+                                vars.entireSystemColl -
+                                singleLiquidation.totalCollToSendToLiquidator -
+                                singleLiquidation.collSurplus;
+
+                            // Add liquidation values to their respective running totals
+                            totals = _addLiquidationValuesToTotals(totals, singleLiquidation);
+
+                            _TCR = _computeTCRWithGivenSystemValues(
+                                vars.entireSystemColl,
+                                vars.entireSystemDebt,
+                                _price
+                            );
+                            vars.backToNormalMode = _TCR < CCR ? false : true;
+                            _liqFlags[vars.i] = true;
+                        }
+                    } else if (vars.backToNormalMode) {
+                        if (_checkICRAgainstMCR(vars.ICR)) {
+                            _syncAccounting(vars.cdpId);
+                            _getLiquidationValuesNormalMode(_price, _TCR, vars, singleLiquidation);
+
+                            // Add liquidation values to their respective running totals
+                            totals = _addLiquidationValuesToTotals(totals, singleLiquidation);
+                            _liqFlags[vars.i] = true;
+                        }
+                    }
                 }
                 // In Normal Mode skip cdps with ICR >= MCR
             }
@@ -816,15 +822,17 @@ contract LiquidationLibrary is CdpManagerStorage {
         for (vars.i = _start; ; ) {
             vars.cdpId = _cdpArray[vars.i];
             // only for active cdps
-            if (vars.cdpId != bytes32(0) && Cdps[vars.cdpId].status == Status.active) {
-                vars.ICR = getSyncedICR(vars.cdpId, _price);
+            if (vars.cdpId != bytes32(0)) {
+                if (Cdps[vars.cdpId].status == Status.active) {
+                    vars.ICR = getSyncedICR(vars.cdpId, _price);

-                if (_checkICRAgainstMCR(vars.ICR)) {
-                    _syncAccounting(vars.cdpId);
-                    _getLiquidationValuesNormalMode(_price, _TCR, vars, singleLiquidation);
+                    if (_checkICRAgainstMCR(vars.ICR)) {
+                        _syncAccounting(vars.cdpId);
+                        _getLiquidationValuesNormalMode(_price, _TCR, vars, singleLiquidation);

-                    // Add liquidation values to their respective running totals
-                    totals = _addLiquidationValuesToTotals(totals, singleLiquidation);
+                        // Add liquidation values to their respective running totals
+                        totals = _addLiquidationValuesToTotals(totals, singleLiquidation);
+                    }
                 }
             }
             ++vars.i;

```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L512
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L765
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L796

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

512:         if (_newIndex > _oldIndex && totalStakes > 0) {

765:  if (_newIndex > _oldIndex && totalStakes > 0) {

796:  if (_cdpPerUnitIdx != _systemStEthFeePerUnitIndex && _cdpPerUnitIdx > 0) {

```

```diff

diff --git a/packages/contracts/contracts/CdpManagerStorage.sol b/packages/contracts/contracts/CdpManagerStorage.sol
index cd11ee4..88bb9a0 100644
--- a/packages/contracts/contracts/CdpManagerStorage.sol
+++ b/packages/contracts/contracts/CdpManagerStorage.sol
@@ -509,14 +509,16 @@ contract CdpManagerStorage is EbtcBase, ReentrancyGuard, ICdpManagerData, AuthNo
     function _syncGlobalAccounting() internal {
         (uint256 _oldIndex, uint256 _newIndex) = _readStEthIndex();
         _syncStEthIndex(_oldIndex, _newIndex);
-        if (_newIndex > _oldIndex && totalStakes > 0) {
-            (
-                uint256 _feeTaken,
-                uint256 _newFeePerUnit,
-                uint256 _perUnitError
-            ) = _calcSyncedGlobalAccounting(_newIndex, _oldIndex);
-            _takeSplitAndUpdateFeePerUnit(_feeTaken, _newFeePerUnit, _perUnitError);
-            _updateSystemSnapshotsExcludeCollRemainder(0);
+        if (_newIndex > _oldIndex) {
+            if (totalStakes > 0) {
+                (
+                    uint256 _feeTaken,
+                    uint256 _newFeePerUnit,
+                    uint256 _perUnitError
+                ) = _calcSyncedGlobalAccounting(_newIndex, _oldIndex);
+                _takeSplitAndUpdateFeePerUnit(_feeTaken, _newFeePerUnit, _perUnitError);
+                _updateSystemSnapshotsExcludeCollRemainder(0);
+            }
         }
     }

@@ -762,17 +764,19 @@ contract CdpManagerStorage is EbtcBase, ReentrancyGuard, ICdpManagerData, AuthNo
         uint256 _newIndex,
         uint256 _oldIndex
     ) internal view returns (uint256, uint256, uint256) {
-        if (_newIndex > _oldIndex && totalStakes > 0) {
-            /// @audit-ok We don't take the fee if we had a negative rebase
-            (
-                uint256 _feeTaken,
-                uint256 _deltaFeePerUnit,
-                uint256 _perUnitError
-            ) = calcFeeUponStakingReward(_newIndex, _oldIndex);
-
-            // calculate new split per stake unit
-            uint256 _newPerUnit = systemStEthFeePerUnitIndex + _deltaFeePerUnit;
-            return (_feeTaken, _newPerUnit, _perUnitError);
+        if (_newIndex > _oldIndex) {
+            if (totalStakes > 0) {
+                /// @audit-ok We don't take the fee if we had a negative rebase
+                (
+                    uint256 _feeTaken,
+                    uint256 _deltaFeePerUnit,
+                    uint256 _perUnitError
+                ) = calcFeeUponStakingReward(_newIndex, _oldIndex);
+
+                // calculate new split per stake unit
+                uint256 _newPerUnit = systemStEthFeePerUnitIndex + _deltaFeePerUnit;
+                return (_feeTaken, _newPerUnit, _perUnitError);
+            }
         } else {
             return (0, systemStEthFeePerUnitIndex, systemStEthFeePerUnitIndexError);
         }
@@ -793,13 +797,15 @@ contract CdpManagerStorage is EbtcBase, ReentrancyGuard, ICdpManagerData, AuthNo
         uint256 _newCollShare = Cdps[_cdpId].coll;

         // processing split fee to be applied
-        if (_cdpPerUnitIdx != _systemStEthFeePerUnitIndex && _cdpPerUnitIdx > 0) {
-            (
-                uint256 _feeSplitDistributed,
-                uint256 _newCollShareAfter
-            ) = getAccumulatedFeeSplitApplied(_cdpId, _systemStEthFeePerUnitIndex);
-            _feeSplitApplied = _feeSplitDistributed;
-            _newCollShare = _newCollShareAfter;
+        if (_cdpPerUnitIdx != _systemStEthFeePerUnitIndex) {
+            if (_cdpPerUnitIdx > 0) {
+                (
+                    uint256 _feeSplitDistributed,
+                    uint256 _newCollShareAfter
+                ) = getAccumulatedFeeSplitApplied(_cdpId, _systemStEthFeePerUnitIndex);
+                _feeSplitApplied = _feeSplitDistributed;
+                _newCollShare = _newCollShareAfter;
+            }
         }

         // processing redistributed debt to be applied


```

<a name='g-06'></a>

## [G-06] Use hardcode address instead of address(this)

It can be more gas-efficient to use a hardcoded address instead of the address(this) expression.

The reason for this is that using address(this) requires an additional EXTCODESIZE operation to retrieve the contract's address from its bytecode, which can increase the gas cost of your contract. By pre-calculating and using a hardcoded address, you can avoid this additional operation and reduce the overall gas cost of your contract.

Here's an example of how you can use a hardcoded address instead of address(this):

```solidity
contract MyContract {
    address public myAddress = 0x1234567890123456789012345678901234567890;

    function doSomething() public {
        // Use myAddress instead of address(this)
        require(msg.sender == myAddress, "Caller is not authorized");

        // Do something
    }
}
```

Total Instances: `9`

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L283
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L295
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L299
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L337
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L376

```solidity
File: packages/contracts/contracts/ActivePool.sol

283:        collateral.transferFrom(address(receiver), address(this), amountWithFee);

295:             collateral.balanceOf(address(this)) >= collateral.getPooledEthByShares(systemCollShares),

299:  collateral.sharesOf(address(this)) >= systemCollShares,

337:  return collateral.balanceOf(address(this));

376:  uint256 balance = IERC20(token).balanceOf(address(this));

```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L682C9-L682C90

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

682: return keccak256(abi.encode(typeHash, name, version, _chainID(), address(this)));

```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L145

```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

145: uint256 balance = IERC20(token).balanceOf(address(this));

```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L240
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L297

```solidity
File: packages/contracts/contracts/EBTCToken.sol

240:  return keccak256(abi.encode(typeHash, name, version, _chainID(), address(this)));

297:  _recipient != address(0) && _recipient != address(this),

```

<a name='g-07'></a>

## [G-07] Do not calculate constants

Due to how constant variables are implemented (replacements at compile-time), an expression assigned to a constant variable is recomputed each time that the variable is used, which wastes some gas.

Total Instances: `2`

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L32C5-L35C11

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

32: bytes32 private constant _PERMIT_POSITION_MANAGER_TYPEHASH =
33:        keccak256(
34:            "PermitPositionManagerApproval(address borrower,address positionManager,uint8 status,uint256 nonce,uint256 deadline)"
35:        );

```

```diff

diff --git a/packages/contracts/contracts/BorrowerOperations.sol b/packages/contracts/contracts/BorrowerOperations.sol
index db7a32e..9cc19b3 100644
--- a/packages/contracts/contracts/BorrowerOperations.sol
+++ b/packages/contracts/contracts/BorrowerOperations.sol
@@ -29,10 +29,8 @@ contract BorrowerOperations is
     string public constant NAME = "BorrowerOperations";

     // keccak256("permitPositionManagerApproval(address borrower,address positionManager,uint8 status,uint256 nonce,uint256 deadline)");
-    bytes32 private constant _PERMIT_POSITION_MANAGER_TYPEHASH =
-        keccak256(
-            "PermitPositionManagerApproval(address borrower,address positionManager,uint8 status,uint256 nonce,uint256 deadline)"
-        );
+
+    bytes32 private constant _PERMIT_POSITION_MANAGER_TYPEHASH = 0x676cf0f6853f58d289a0461496b722a5c98983d00ee3ab1842ec5c7cb21fd711;

     // keccak256("EIP712Domain(string name,string version,uint256 chainId,address verifyingContract)");
     bytes32 private constant _TYPE_HASH =

```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L21

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

21:  uint128 public constant UNSET_TIMESTAMP = type(uint128).max;

```

```diff

diff --git a/packages/contracts/contracts/CdpManagerStorage.sol b/packages/contracts/contracts/CdpManagerStorage.sol
index cd11ee4..79e3c9d 100644
--- a/packages/contracts/contracts/CdpManagerStorage.sol
+++ b/packages/contracts/contracts/CdpManagerStorage.sol
@@ -18,7 +18,7 @@ import "./Dependencies/AuthNoOwner.sol";
 /// @dev and shared functions are added here in CdpManagerStorage to de-dup code
 contract CdpManagerStorage is EbtcBase, ReentrancyGuard, ICdpManagerData, AuthNoOwner {
     // NOTE: No packing cause it's the last var, no need for u64
-    uint128 public constant UNSET_TIMESTAMP = type(uint128).max;
+    uint128 private constant UNSET_TIMESTAMP = 340282366920938463463374607431768211455;
     uint128 public constant MINIMUM_GRACE_PERIOD = 15 minutes;

     uint128 public lastGracePeriodStartTimestamp = UNSET_TIMESTAMP; // use max to signify


```

<a name='g-08'></a>

## [G-08] Use assembly to compute hashes to save gas

If the arguments to the encode call can fit into the scratch space (two words or fewer), then it's more efficient to use assembly to generate the hash (**80 gas**):

`keccak256(abi.encodePacked(x, y))` -> `assembly {mstore(0x00, a); mstore(0x20, b); let hash := keccak256(0x00, 0x40); }`

Total Instances: `4`

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L128
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L129

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

128:         bytes32 hashedName = keccak256(bytes(NAME));

129:         bytes32 hashedVersion = keccak256(bytes(_VERSION));

```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L71C1-L71C54
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L72

```solidity
File: packages/contracts/contracts/EBTCToken.sol

71:         bytes32 hashedName = keccak256(bytes(_NAME));

72:         bytes32 hashedVersion = keccak256(bytes(_VERSION));

```

<a name='g-09'></a>

## [G-09] Use constants instead of type(uintx).max

It's generally more gas-efficient to use constants instead of type(uintX).max when you need to set the maximum value of an unsigned integer type.

The reason for this is that the type(uintX).max expression involves a computation at runtime, whereas a constant is evaluated at compile-time. This means that using type(uintX).max can result in additional gas costs for each transaction that involves the expression.

By using a constant instead of type(uintX).max, you can avoid these additional gas costs and make your code more efficient.

Here's an example of how you can use a constant instead of type(uintX).max:

```solidity
contract MyContract {
    uint120 constant MAX_VALUE = 2**120 - 1;

    function doSomething(uint120 value) public {
        require(value <= MAX_VALUE, "Value exceeds maximum");

        // Do something
    }
}
```

In the above example, we have a contract with a constant MAX_VALUE that represents the maximum value of a uint120. When the doSomething function is called with a value parameter, it checks whether the value is less than or equal to MAX_VALUE using the <= operator.

By using a constant instead of type(uint120).max, we can make our code more efficient and reduce the gas cost of our contract.

It's important to note that using constants can make your code more readable and maintainable, since the value is defined in one place and can be easily updated if necessary. However, constants should be used with caution and only when their value is known at compile-time.

Total Instances: `3`

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L378

```solidity
File: packages/contracts/contracts/CdpManager.sol

378: _maxIterations = type(uint256).max;

```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L21

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

21:  uint128 public constant UNSET_TIMESTAMP = type(uint128).max;

```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L143

```solidity
File: packages/contracts/contracts/EBTCToken.sol

143:  if (cachedAllowance != type(uint256).max) {

```
