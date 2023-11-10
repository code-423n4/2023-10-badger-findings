# Gas Optimization: consider removing redundant checks in SortedCdps.reInsert()

**Context:** [SortedCdps.sol#L506-L508](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L506-L508)

**Description:**
`reInsert` currently uses a check to ensure `contains(_id)` (the List contains the id) even though it should be already checked in `_remove(_id)` method, same for the other check to ensure `_newNICR > 0` that should be already checked in `_insert(_id, _newNICR, _prevId, _nextId)`.

**Recommendation:**
Consider removing those redundant checks to improve gas efficiency.

```diff
diff --git a/packages/contracts/contracts/SortedCdps.sol b/packages/contracts/contracts/SortedCdps.sol
index 0fd34e7..1e3b413 100644
--- a/packages/contracts/contracts/SortedCdps.sol
+++ b/packages/contracts/contracts/SortedCdps.sol
@@ -502,10 +502,6 @@ contract SortedCdps is ISortedCdps {
         bytes32 _nextId
     ) external override {
         _requireCallerIsBOorCdpM();
-        // List must contain the node
-        require(contains(_id), "SortedCdps: List does not contain the id");
-        // NICR must be non-zero
-        require(_newNICR > 0, "SortedCdps: NICR must be positive");
 
         // Remove node from the list
         _remove(_id);
```
- Tests PASS
`yarn && forge build && forge test`
`Ran 39 test suites: 229 tests passed, 0 failed, 0 skipped (229 total tests)`

`yarn test`
```
  607 passing (34m)
  40 pending

Done in 2020.92s.
```

- Gas Report:

**Before**
```haskell
| contracts/SortedCdps.sol:SortedCdps contract |                 |        |        |         |         |
|----------------------------------------------|-----------------|--------|--------|---------|---------|
| Deployment Cost                              | Deployment Size |        |        |         |         |
| 1462626                                      | 7742            |        |        |         |         |
| Function Name                                | min             | avg    | median | max     | # calls |
| reInsert                                     | 39763           | 847382 | 760486 | 1835084 | 1304    |
```

**After**
```haskell
| contracts/SortedCdps.sol:SortedCdps contract |                 |        |        |         |         |
|----------------------------------------------|-----------------|--------|--------|---------|---------|
| Deployment Cost                              | Deployment Size |        |        |         |         |
| 1447405                                      | 7666            |        |        |         |         |
| Function Name                                | min             | avg    | median | max     | # calls |
| reInsert                                     | 39556           | 847285 | 762740 | 1834283 | 1303    |

```