# QA Report

## Low Findings
### L01 - Loop conditions in `_descendList` and `_ascendList` contain incorrect termination condition
The first loop condition when [ascending](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SortedCdps.sol#L642) and [descending](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SortedCdps.sol#L619) the sorted cdp list is unnecessary or incorrect, but it is unclear that it causes any problems

I believe this is the correct logic:

```diff
diff --git a/packages/contracts/contracts/SortedCdps.sol b/packages/contracts/contracts/SortedCdps.sol
index 0fd34e7..f37cdc4 100644
--- a/packages/contracts/contracts/SortedCdps.sol
+++ b/packages/contracts/contracts/SortedCdps.sol
@@ -626,7 +626,7 @@ contract SortedCdps is ISortedCdps {
         bytes32 nextId = data.nodes[prevId].nextId;

         // Descend the list until we reach the end or until we find a valid insert position
-        while (prevId != dummyId && !_validInsertPosition(_NICR, prevId, nextId)) {
+        while (nextId != dummyId && !_validInsertPosition(_NICR, prevId, nextId)) {
             prevId = data.nodes[prevId].nextId;
             nextId = data.nodes[prevId].nextId;
         }
@@ -649,7 +649,7 @@ contract SortedCdps is ISortedCdps {
         bytes32 prevId = data.nodes[nextId].prevId;

         // Ascend the list until we reach the end or until we find a valid insertion point
-        while (nextId != dummyId && !_validInsertPosition(_NICR, prevId, nextId)) {
+        while (prevId != dummyId && !_validInsertPosition(_NICR, prevId, nextId)) {
             nextId = data.nodes[nextId].prevId;
             prevId = data.nodes[nextId].prevId;
         }
```

However, removing the first condition also is perfectly valid as the necessary logic for loop termination is redundantly captured in `_validInsertPosition`.  The following logic also works:

```diff
diff --git a/packages/contracts/contracts/SortedCdps.sol b/packages/contracts/contracts/SortedCdps.sol
index 0fd34e7..7da9745 100644
--- a/packages/contracts/contracts/SortedCdps.sol
+++ b/packages/contracts/contracts/SortedCdps.sol
@@ -626,7 +626,7 @@ contract SortedCdps is ISortedCdps {
         bytes32 nextId = data.nodes[prevId].nextId;

         // Descend the list until we reach the end or until we find a valid insert position
-        while (prevId != dummyId && !_validInsertPosition(_NICR, prevId, nextId)) {
+        while (!_validInsertPosition(_NICR, prevId, nextId)) {
             prevId = data.nodes[prevId].nextId;
             nextId = data.nodes[prevId].nextId;
         }
@@ -649,7 +649,7 @@ contract SortedCdps is ISortedCdps {
         bytes32 prevId = data.nodes[nextId].prevId;

         // Ascend the list until we reach the end or until we find a valid insertion point
-        while (nextId != dummyId && !_validInsertPosition(_NICR, prevId, nextId)) {
+        while (!_validInsertPosition(_NICR, prevId, nextId)) {
             nextId = data.nodes[nextId].prevId;
             prevId = data.nodes[nextId].prevId;
         }
```

If this is not correct, the test cases do not reflect the need for this condition, as all three instances pass the tests.
## Non-Critical Findings

### NC01 - Unnecessary containment check for EnumerableSet

In `RolesAuthority.sol` there are a couple checks to see if an EnumerableSet contains an item before adding it to the set. This is unnecessary as `add` in EnumerableSet will also check for containment.

[L116](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L116) in `setRoleCapability`:
```js
            if (!targets.contains(target)) {//@audit This is a redundant check as targets is an EnumerableSet and targets.add will check containment 
                targets.add(target);
            }
```

[L151](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L151) in `setUserRole`:
```js
            if (!users.contains(user)) {//@audit This is a redundant check as users is an EnumerableSet and users.add will check containment
                users.add(user);
            }
```

[L65](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/EnumerableSet.sol#L65) in `EnumerableSet` shows that `add` checks for the value in the set:

```js
    /**
     * @dev Add a value to a set. O(1).
     *
     * Returns true if the value was added to the set, that is if it was not
     * already present.
     */
    function _add(Set storage set, bytes32 value) private returns (bool) {
        if (!_contains(set, value)) {
            set._values.push(value);
            // The value is stored at length-1, but we add 1 to all indexes
            // and use 0 as a sentinel value
            set._indexes[value] = set._values.length;
            return true;
        } else {
            return false;
        }
    }
```

#### Fix
```diff
diff --git a/packages/contracts/contracts/Dependencies/RolesAuthority.sol b/packages/contracts/contracts/Dependencies/RolesAuthority.sol
index 14fbbf3..49cdba5 100644
--- a/packages/contracts/contracts/Dependencies/RolesAuthority.sol
+++ b/packages/contracts/contracts/Dependencies/RolesAuthority.sol
@@ -112,10 +112,7 @@ contract RolesAuthority is IRolesAuthority, Auth, Authority {
         if (enabled) {
             getRolesWithCapability[target][functionSig] |= bytes32(1 << role);
             enabledFunctionSigsByTarget[target].add(bytes32(functionSig));
-
-            if (!targets.contains(target)) {
-                targets.add(target);
-            }
+            targets.add(target);
         } else {
             getRolesWithCapability[target][functionSig] &= ~bytes32(1 << role);
             enabledFunctionSigsByTarget[target].remove(bytes32(functionSig));
@@ -147,10 +144,7 @@ contract RolesAuthority is IRolesAuthority, Auth, Authority {
     function setUserRole(address user, uint8 role, bool enabled) public virtual requiresAuth {
         if (enabled) {
             getUserRoles[user] |= bytes32(1 << role);
-
-            if (!users.contains(user)) {
-                users.add(user);
-            }
+            users.add(user);
         } else {
             getUserRoles[user] &= ~bytes32(1 << role);

```



### NC02 - Redundant check in `_openCdp`

The following check in  [L463](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L463) of `_openCdp` is unneeded:

```js
require(vars.netStEthBalance > 0, "BorrowerOperations: zero collateral for openCdp()!");
```

As the check in [L454](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L454), `_requireAtLeastMinNetStEthBalance(vars.netStEthBalance)` covers it already (defined on [L939](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L939)): 

```js
    function _requireAtLeastMinNetStEthBalance(uint256 _stEthBalance) internal pure {
        require(
            _stEthBalance >= MIN_NET_STETH_BALANCE,
            "BorrowerOperations: Cdp's net stEth balance must not fall below minimum"
        );
    }
```

`MIN_NET_STETH_BALANCE` is defined in `EbtcBase.sol`, [L31](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/EbtcBase.sol#L31):

```js
    uint256 public constant MIN_NET_STETH_BALANCE = 2e18;
```
#### fix
```diff
diff --git a/packages/contracts/contracts/BorrowerOperations.sol b/packages/contracts/contracts/BorrowerOperations.sol
index db7a32e..ed822cd 100644
--- a/packages/contracts/contracts/BorrowerOperations.sol
+++ b/packages/contracts/contracts/BorrowerOperations.sol
@@ -459,9 +459,6 @@ contract BorrowerOperations is
         vars.price = priceFeed.fetchPrice();
         vars.debt = _debt;

-        // Sanity check
-        require(vars.netStEthBalance > 0, "BorrowerOperations: zero collateral for openCdp()!");
-
         uint256 _netCollAsShares = collateral.getSharesByPooledEth(vars.netStEthBalance);
         uint256 _liquidatorRewardShares = collateral.getSharesByPooledEth(LIQUIDATOR_REWARD);
```
