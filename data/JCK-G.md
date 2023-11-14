## Gas Optimizations

| Number | Issue | Instances | Total gas saved |
|--------|-------|-----------|-----------------|
|[G-01]|  Pack structs by putting data types that can fit together next to each other |  8  | 16000 |
|[G-02]|  Possible Optimization 1 |  8  |  |
|[G-03]|  Possible Optimization 2 |  3  |  |
|[G-04]|  Possible Optimizations in ARCDVestingVault. |  3  |  |
|[G-05]|  Possible Optimizations |  1  |  |
|[G-06]|  Possible Optimization in ActivePool.sol |  2  |  |
|[G-07]|  Possible Optimization in accept() function  |  1  |  |
|[G-08]|  Possible Optimizations |  12  |  |
|[G-09]|  Don’t cache calls that are only used once |  1  |  |
|[G-10]|  public functions not called by the contract should be declared external instead |  26  |  |
|[G-11]|  Do not calculate constants |  8  |  |
|[G-12]|  State variables which are not modified within functions should be set as constant or immutable for values set at deployment |  11  | 110000 |
|[G-13]|  Use assembly in place of abi.decode to extract calldata values more efficiently |  4  |  |
|[G-14]|  Use assembly to emit an event |  88  | 3344 |
|[G-15]|  Use hardcoded address instead of address(this) |  25  |  |
|[G-16]|  Use assembly to write address storage values |  6  | 444 |
|[G-17]|  Use uint256(1)/uint256(2) instead for true and false boolean states |  22  | 376200 |
|[G-18]|  Use assembly to validate msg.sender |  19  | 228 |
|[G-19]|  Use assembly for loops |  8  |  |
|[G-20]|  abi.encode() is less efficient than abi.encodepacked() |  4  |  |
|[G-21]|  Using delete statement can save gas |  3  |  |
|[G-22]|  Use nested if/require statements instead of && |  19  | 570 |
|[G-23]|  Counting down in for statements is more gas efficient |  13  |  |
|[G-24]|  Create immutable variable to avoid an external call |  3  |  |
|[G-25]|  Avoid Unnecessary Public Variables |  14  | 308000 |


## [G-01] Pack structs by putting data types that can fit together next to each other

As the solidity EVM works with 32 bytes, variables less than 32 bytes should be packed inside a struct so that they can be stored in the same slot. This saves gas when writing to storage ~20000 gas

```solidity
file: main/packages/contracts/contracts/BorrowerOperations.sol

97   struct MoveTokensParams {
        address user;
        uint256 collSharesChange;
        uint256 collAddUnderlying; // ONLY for isCollIncrease=true
        bool isCollIncrease;
        uint256 netDebtChange;
        bool isDebtIncrease;
    }

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L97-L104


```solidity
file: main/packages/contracts/contracts/LeverageMacroBase.sol

268   struct SwapOperation {
        // Swap Data
        address tokenForSwap;
        address addressForApprove;
        uint256 exactApproveAmount;
        address addressForSwap;
        bytes calldataForSwap;
        SwapCheck[] swapChecks; // Empty to skip
    }

322   struct AdjustCdpOperation {
        bytes32 _cdpId;
        uint256 _stEthBalanceDecrease;
        uint256 _EBTCChange;
        bool _isDebtIncrease;
        bytes32 _upperHint;
        bytes32 _lowerHint;
        uint256 _stEthBalanceIncrease;
    }


```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L268-L276

```solidity
file: main/packages/contracts/contracts/SimplifiedDiamondLike.sol

99    struct Operation {
        address to; // Target to call
        bool checkSuccess; // If false we will ignore a revert
        uint128 value; // How much ETH to send
        uint128 gas; // How much gas to send
        bool capGas; // true to use above "gas" setting or we send gasleft()
        OperationType opType; // See `OperationType`
        bytes data; // Calldata to send (funsig + data)
    }

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L99-L107

```solidity
file:  main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol

118   struct LiquidationLocals {
        bytes32 cdpId;
        uint256 partialAmount; // used only for partial liquidation, default 0 means full liquidation
        uint256 price;
        uint256 ICR;
        bytes32 upperPartialHint;
        bytes32 lowerPartialHint;
        bool recoveryModeAtStart;
        uint256 TCR;
        uint256 totalSurplusCollShares;
        uint256 totalCollSharesToSend;
        uint256 totalDebtToBurn;
        uint256 totalDebtToRedistribute;
        uint256 totalLiquidatorRewardCollShares;
    }

134   struct LiquidationRecoveryModeLocals {
        uint256 entireSystemDebt;
        uint256 entireSystemColl;
        uint256 totalDebtToBurn;
        uint256 totalCollSharesToSend;
        uint256 totalSurplusCollShares;
        bytes32 cdpId;
        uint256 price;
        uint256 ICR;
        uint256 totalDebtToRedistribute;
        uint256 totalLiquidatorRewardCollShares;
    }

165  struct SingleRedemptionInputs {
        bytes32 cdpId;
        uint256 maxEBTCamount;
        uint256 price;
        bytes32 upperPartialRedemptionHint;
        bytes32 lowerPartialRedemptionHint;
        uint256 partialRedemptionHintNICR;
    }

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L118-L132

```solidity
file: main/packages/contracts/contracts/Interfaces/IPriceFeed.sol

17   struct ChainlinkResponse {
        uint80 roundEthBtcId;
        uint80 roundStEthEthId;
        uint256 answer;
        uint256 timestampEthBtc;
        uint256 timestampStEthEth;
        bool success;
    }

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPriceFeed.sol#L17-24

## [G-02] Possible Optimization 1

In the _closeCdpWithoutRemovingSortedCdps and _removeStake functions, the Cdps[_cdpId] mapping inside _closeCdpWithoutRemovingSortedCdps function  is updated 4 time. and inside the _removeStake function updated towice. This can be optimized to a single update, which would save gas.

```solidity
file:  contracts/contracts/CdpManagerStorage.sol

260       function _closeCdpWithoutRemovingSortedCdps(bytes32 _cdpId, Status closedStatus) internal {
        require(
            closedStatus != Status.nonExistent && closedStatus != Status.active,
            "CdpManagerStorage: close non-exist or non-active CDP!"
        );

        uint256 cdpIdsArrayLength = CdpIds.length;
        _requireMoreThanOneCdpInSystem(cdpIdsArrayLength);

        _removeStake(_cdpId);

        Cdps[_cdpId].status = closedStatus;
        Cdps[_cdpId].coll = 0;
        Cdps[_cdpId].debt = 0;
        Cdps[_cdpId].liquidatorRewardShares = 0;

        cdpDebtRedistributionIndex[_cdpId] = 0;
        cdpStEthFeePerUnitIndex[_cdpId] = 0;

        _removeCdp(_cdpId, cdpIdsArrayLength);
    }
    
    
410   function _removeStake(bytes32 _cdpId) internal {
        uint256 _newTotalStakes = totalStakes - Cdps[_cdpId].stake;
        totalStakes = _newTotalStakes;
        Cdps[_cdpId].stake = 0;
        emit TotalStakesUpdated(_newTotalStakes);
    }

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L260-L280

In the claimSurplusCollShares functions, the balances[_account] mapping inside claimSurplusCollShares function  is updated towice. This can be optimized to a single update, which would save gas.


```solidity
file:  contracts/contracts/CollSurplusPool.sol
 
89       function claimSurplusCollShares(address _account) external override {
        _requireCallerIsBorrowerOperations();
        uint256 claimableColl = balances[_account];
        require(claimableColl > 0, "CollSurplusPool: No collateral available to claim");

        balances[_account] = 0;
        emit SurplusCollSharesUpdated(_account, 0);

        uint256 cachedTotalSurplusCollShares = totalSurplusCollShares;

        require(cachedTotalSurplusCollShares >= claimableColl, "!CollSurplusPoolBal");
        // Safe per the check above
        unchecked {
            totalSurplusCollShares = cachedTotalSurplusCollShares - claimableColl;
        }
        emit CollSharesTransferred(_account, claimableColl);

        // NOTE: No need for safe transfer if the collateral asset is standard. Make sure this is the case!
        collateral.transferShares(_account, claimableColl);
    }

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L89-L108


In the _insert functions, the data.nodes[_id] mapping inside _insert function  is updated 4 time. This can be optimized to a single update, which would save gas.

```solidity
file:  contracts/contracts/SortedCdps.sol

363       function _insert(bytes32 _id, uint256 _NICR, bytes32 _prevId, bytes32 _nextId) internal {
        // List must not be full
        require(!isFull(), "SortedCdps: List is full");
        // List must not already contain node
        require(!contains(_id), "SortedCdps: List already contains the node");
        // Node id must not be null
        require(_id != dummyId, "SortedCdps: Id cannot be zero");
        // NICR must be non-zero
        require(_NICR > 0, "SortedCdps: NICR must be positive");

        bytes32 prevId = _prevId;
        bytes32 nextId = _nextId;

        if (!_validInsertPosition(_NICR, prevId, nextId)) {
            // Sender's hint was not a valid insert position
            // Use sender's hint to find a valid insert position
            (prevId, nextId) = _findInsertPosition(_NICR, prevId, nextId);
        }

        if (prevId == dummyId && nextId == dummyId) {
            // Insert as head and tail
            data.head = _id;
            data.tail = _id;
        } else if (prevId == dummyId) {
            // Insert before `prevId` as the head
            data.nodes[_id].nextId = data.head;
            data.nodes[data.head].prevId = _id;
            data.head = _id;
        } else if (nextId == dummyId) {
            // Insert after `nextId` as the tail
            data.nodes[_id].prevId = data.tail;
            data.nodes[data.tail].nextId = _id;
            data.tail = _id;
        } else {
            // Insert at insert position between `prevId` and `nextId`
            data.nodes[_id].nextId = nextId;
            data.nodes[_id].prevId = prevId;
            data.nodes[prevId].nextId = _id;
            data.nodes[nextId].prevId = _id;
        }

        data.size = data.size + 1;
        emit NodeAdded(_id, _NICR);
    }


```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L363-L406

In the setRoleCapability functions, the enabledFunctionSigsByTarget[target] mapping inside setRoleCapability function  is updated 3 time. This can be optimized to a single update, which would save gas.

```solidity
file:  contracts/contracts/Dependencies/RolesAuthority.sol

106      function setRoleCapability(
        uint8 role,
        address target,
        bytes4 functionSig,
        bool enabled
    ) public virtual requiresAuth {
        if (enabled) {
            getRolesWithCapability[target][functionSig] |= bytes32(1 << role);
            enabledFunctionSigsByTarget[target].add(bytes32(functionSig));

            if (!targets.contains(target)) {
                targets.add(target);
            }
        } else {
            getRolesWithCapability[target][functionSig] &= ~bytes32(1 << role);
            enabledFunctionSigsByTarget[target].remove(bytes32(functionSig));

            // If no enabled function signatures exist for this target, remove target
            if (enabledFunctionSigsByTarget[target].length() == 0) {
                targets.remove(target);
            }
        }

        emit RoleCapabilityUpdated(role, target, functionSig, enabled);
    }

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L106-L130

In the setUserRole functions, the  getUserRoles[user] mapping inside setUserRole function  is updated 3 time. This can be optimized to a single update, which would save gas

```solidity
file:  contracts/contracts/Dependencies/RolesAuthority.sol

147    function setUserRole(address user, uint8 role, bool enabled) public virtual requiresAuth {
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

In the setPublicCapability functions, the capabilityFlag[target] mapping inside setPublicCapability function  is updated 3 time. This can be optimized to a single update, which would save gas

```solidity
file:  contracts/contracts/Dependencies/RolesAuthority.sol

85    function setPublicCapability(
        address target,
        bytes4 functionSig,
        bool enabled
    ) public virtual requiresAuth {
        require(
            capabilityFlag[target][functionSig] != CapabilityFlag.Burned,
            "RolesAuthority: Capability Burned"
        );

        if (enabled) {
            capabilityFlag[target][functionSig] = CapabilityFlag.Public;
        } else {
            capabilityFlag[target][functionSig] = CapabilityFlag.None;
        }

        emit PublicCapabilityUpdated(target, functionSig, enabled);
    }
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L85-L102


In the setRoleCapability functions, the  getRolesWithCapability[target] mapping inside setRoleCapability function  is updated towice. This can be optimized to a single update, which would save gas

```solidity
file:  contracts/contracts/Dependencies/RolesAuthority.sol

106       function setRoleCapability(
        uint8 role,
        address target,
        bytes4 functionSig,
        bool enabled
    ) public virtual requiresAuth {
        if (enabled) {
            getRolesWithCapability[target][functionSig] |= bytes32(1 << role);
            enabledFunctionSigsByTarget[target].add(bytes32(functionSig));

            if (!targets.contains(target)) {
                targets.add(target);
            }
        } else {
            getRolesWithCapability[target][functionSig] &= ~bytes32(1 << role);
            enabledFunctionSigsByTarget[target].remove(bytes32(functionSig));

            // If no enabled function signatures exist for this target, remove target
            if (enabledFunctionSigsByTarget[target].length() == 0) {
                targets.remove(target);
            }
        }

        emit RoleCapabilityUpdated(role, target, functionSig, enabled);
    }

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L106-L130


Estimated gas saved:
This optimization reduces the number of storage operations from 4, 3 and 2 to 1 in every above functions. Given that a storage operation costs 20,000 gas, this optimization could save approximately 20,000 gas per call to these functions.

## [G-03] Possible Optimization 2

The getUsersByRole(), getRolesForUser() and getRolesFromByteMap() function can be optimized by removing the check   if (count > 0) {. This check is not necessary because in the for loop one is added to count in this case count is grather then zero there is no need for checking the count. Removing this check can save gas.

```solidity
file: contracts/contracts/Governor.sol

43     function getUsersByRole(uint8 role) external view returns (address[] memory usersWithRole) {
        // Search over all users: O(n) * 2
        uint256 count;
        for (uint256 i = 0; i < users.length(); i++) {
            address user = users.at(i);
            bool _canCall = doesUserHaveRole(user, role);
            if (_canCall) {
                count += 1;
            }
        }
        if (count > 0) {
            uint256 j = 0;
            usersWithRole = new address[](count);
            address[] memory _usrs = users.values();
            for (uint256 i = 0; i < _usrs.length; i++) {
                address user = _usrs[i];
                bool _canCall = doesUserHaveRole(user, role);
                if (_canCall) {
                    usersWithRole[j] = user;
                    j++;
                }
            }
        }
    }

73      function getRolesForUser(address user) external view returns (uint8[] memory rolesForUser) {
        // Enumerate over all possible roles and check if enabled
        uint256 count;
        for (uint8 i = 0; i < type(uint8).max; i++) {
            if (doesUserHaveRole(user, i)) {
                count += 1;
            }
        }
        if (count > 0) {
            uint256 j = 0;
            rolesForUser = new uint8[](count);
            for (uint8 i = 0; i < type(uint8).max; i++) {
                if (doesUserHaveRole(user, i)) {
                    rolesForUser[j] = i;
                    j++;
                }
            }
        }
    }

96      function getRolesFromByteMap(bytes32 byteMap) public pure returns (uint8[] memory roleIds) {
        uint256 count;
        for (uint8 i = 0; i < type(uint8).max; i++) {
            bool roleEnabled = (uint256(byteMap >> i) & 1) != 0;
            if (roleEnabled) {
                count += 1;
            }
        }
        if (count > 0) {
            uint256 j = 0;
            roleIds = new uint8[](count);
            for (uint8 i = 0; i < type(uint8).max; i++) {
                bool roleEnabled = (uint256(byteMap >> i) & 1) != 0;
                if (roleEnabled) {
                    roleIds[j] = i;
                    j++;
                }
            }
        }
    }


```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L43-L66

## [G-04] Possible Optimizations in ARCDVestingVault.

### Possible Optimization 1 in CdpManagerStorage.sol

In the _updateStakeForCdp function, there are multiple calls to Cdp storage _cdp = Cdps[_cdpId];. These calls could be optimized by declaring them once at the beginning of the function and reusing the reference. This would save the gas used by the function call.

```solidity
file: contracts/contracts/CdpManagerStorage.sol

432    Cdp storage _cdp = Cdps[_cdpId];

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L432

Estimated gas saved:
This optimization could save around 1000 to 2000 gas per transaction, depending on the gas cost of the function call.

### Possible Optimization 2 in LiquidationLibrary.sol

In the _partiallyReduceCdpDebt function, there are multiple calls to Cdp storage _cdp = Cdps[_cdpId];. These calls could be optimized by declaring them once at the beginning of the function and reusing the reference. This would save the gas used by the function call.

```solidity
file: contracts/contracts/LiquidationLibrary.sol

455  Cdp storage _cdp = Cdps[_cdpId];

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L455

Estimated gas saved:
This optimization could save around 1000 to 2000 gas per transaction, depending on the gas cost of the function call.

### Possible Optimization 3 in SimplifiedDiamondLike.sol

In the _fallback function, there are multiple calls to DiamondLikeStorage storage ds = _getStorage(); . These calls could be optimized by declaring them once at the beginning of the function and reusing the reference. This would save the gas used by the function call.

```solidity
file: contracts/contracts/SimplifiedDiamondLike.sol

175   DiamondLikeStorage storage ds = _getStorage(); 

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L175

Estimated gas saved:
This optimization could save around 1000 to 2000 gas per transaction, depending on the gas cost of the function call.

## [G-05] Possible Optimizations

### Possible Optimization 1

In the _getSyncedCdpDebtAndRedistribution function, the pendingDebtRedistributed is checked to be non-zero at the beginning of the function. However, the pendingDebtRedistributed is not used until after the _getPendingRedistributedDebt function call. Moving the zero check closer to the usage of the pendingDebtRedistributed could save gas in the case where _getPendingRedistributedDebt do operation, as the zero check would not have been performed.

```solidity
file:  contracts/contracts/CdpManagerStorage.sol

822      function _getSyncedCdpDebtAndRedistribution(
        bytes32 _cdpId
    ) internal view returns (uint256, uint256, uint256) {
        (uint256 pendingDebtRedistributed, uint256 _debtIndexDelta) = _getPendingRedistributedDebt(
            _cdpId
        );
        uint256 _newDebt = Cdps[_cdpId].debt;
        if (pendingDebtRedistributed > 0) {
            _newDebt = _newDebt + pendingDebtRedistributed;
        }
        return (_newDebt, pendingDebtRedistributed, _debtIndexDelta);
    }

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L822-L833

Estimated gas saved:
This optimization could save around 200 to 500 gas per transaction, depending on the gas cost of the _getPendingRedistributedDebt function call.

## [G-06] Possible Optimization in ActivePool.sol

In the constructor the _authorityAddress variable is updated before the _authorityAddress check with address zero . This means that even if the _authorityAddress check fails, the _authorityAddress variable will still have been updated, wasting gas. Moving the _authorityAddress update after the _authorityAddress check with address zero could save gas in the case where the minting cap check fails.


```solidity
file:  contracts/contracts/ActivePool.sol

60     address _authorityAddress = address(AuthNoOwner(cdpManagerAddress).authority());
        if (_authorityAddress != address(0)) {
            _initializeAuthority(_authorityAddress);
        }

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L60-L63


```solidity
file: contracts/contracts/BorrowerOperations.sol

123    address _authorityAddress = address(AuthNoOwner(_cdpManagerAddress).authority());
        if (_authorityAddress != address(0)) {
            _initializeAuthority(_authorityAddress);
        }
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L123-L126


Estimated gas saved:
This optimization could save around 5000 to 10000 gas per transaction, depending on the gas cost of the authority function call .


## [G-07] Possible Optimization in accept() function 

In the redeemCollateral()  function, the _firstRedemptionHint variable values is stored in this _cId variabgle . To save gas, it is recommended to use the cached value instead of repeatedly accessing _firstRedemptionHint. By utilizing the cached value, unnecessary memory operations can be avoided.

```solidity
file:  main/packages/contracts/contracts/CdpManager.sol

361        bytes32 _cId = _firstRedemptionHint;

        if (_isValidFirstRedemptionHint(_firstRedemptionHint, totals.price)) {
            currentBorrower = sortedCdps.getOwnerAddress(_firstRedemptionHint);
        } else {
            _cId = sortedCdps.getLast();
            currentBorrower = sortedCdps.getOwnerAddress(_cId);
            // Find the first cdp with ICR >= MCR
            while (currentBorrower != address(0) && getSyncedICR(_cId, totals.price) < MCR) {
                _cId = sortedCdps.getPrev(_cId);
                currentBorrower = sortedCdps.getOwnerAddress(_cId);
            }
        }
        
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L361-L373

### test only the redeemcollatreeal function

Before gas value:
[PASS] test_LiqPremiumWithCdpOvercollateralized_AboveMaxPremium(uint256) (runs: 45, μ: 1344687, ~: 1344759)
[PASS] test_LiqPremiumWithCdpOvercollateralized_BelowMaxPremium(uint256) (runs: 45, μ: 1066358, ~: 1072256)

After gas vlaue:
[PASS] test_LiqPremiumWithCdpOvercollateralized_AboveMaxPremium(uint256) (runs: 45, μ: 1344696, ~: 1344758)
[PASS] test_LiqPremiumWithCdpOvercollateralized_BelowMaxPremium(uint256) (runs: 45, μ: 1061977, ~: 1072239)


In the _partiallyReduceCdpDebt function, the _cdp.coll variable values is stored in this _coll variable and also the _cdp.debt variabgle value is stored in _debt variables  . To save gas, it is recommended to use the cached value instead of repeatedly accessing  _cdp.coll and _cdp.debt. By utilizing the cached value, unnecessary memory operations can be avoided.

```solidity
file: main/packages/contracts/contracts/LiquidationLibrary.sol

450    function _partiallyReduceCdpDebt(
        bytes32 _cdpId,
        uint256 _partialDebt,
        uint256 _partialColl
    ) internal {
        Cdp storage _cdp = Cdps[_cdpId];

        uint256 _coll = _cdp.coll;
        uint256 _debt = _cdp.debt;

        _cdp.coll = _coll - _partialColl;
        _cdp.debt = _debt - _partialDebt;
        _updateStakeAndTotalStakes(_cdpId);
    }

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L450-L463

## [G-08] Possible Optimizations

###  General Optimization

Reducing the number of state variable updates can save gas. In Ethereum, every storage operation costs a significant amount of gas. Therefore, optimizing the contract to minimize storage operations can lead to substantial gas savings.

### Possible Optimization CdpManagerStorage.sol

In the _closeCdpWithoutRemovingSortedCdps, removeStake, removeCdp and  getAccumulatedFeeSplitApplied functions, the aCdps[_cdpId] mapping is updated 2 or 4 time. This can be optimized to a single update, which would save gas.


```solidity
file:  main/packages/contracts/contracts/CdpManagerStorage.sol

260      function _closeCdpWithoutRemovingSortedCdps(bytes32 _cdpId, Status closedStatus) internal {
        require(
            closedStatus != Status.nonExistent && closedStatus != Status.active,
            "CdpManagerStorage: close non-exist or non-active CDP!"
        );

        uint256 cdpIdsArrayLength = CdpIds.length;
        _requireMoreThanOneCdpInSystem(cdpIdsArrayLength);

        _removeStake(_cdpId);

        Cdps[_cdpId].status = closedStatus;
        Cdps[_cdpId].coll = 0;
        Cdps[_cdpId].debt = 0;
        Cdps[_cdpId].liquidatorRewardShares = 0;

        cdpDebtRedistributionIndex[_cdpId] = 0;
        cdpStEthFeePerUnitIndex[_cdpId] = 0;

        _removeCdp(_cdpId, cdpIdsArrayLength);

    }

410  function _removeStake(bytes32 _cdpId) internal {
        uint256 _newTotalStakes = totalStakes - Cdps[_cdpId].stake;
        totalStakes = _newTotalStakes;
        Cdps[_cdpId].stake = 0;
        emit TotalStakesUpdated(_newTotalStakes);
    }

463   function _removeCdp(bytes32 _cdpId, uint256 cdpIdsArrayLength) internal {
        Status cdpStatus = Cdps[_cdpId].status;
        // It’s set in caller function `_closeCdp`
        require(
            cdpStatus != Status.nonExistent && cdpStatus != Status.active,
            "CdpManagerStorage: remove non-exist or non-active CDP!"
        );

        uint128 index = Cdps[_cdpId].arrayIndex;
        uint256 length = cdpIdsArrayLength;
        uint256 idxLast = length - 1;

        require(index <= idxLast, "CdpManagerStorage: CDP indexing overflow!");

        bytes32 idToMove = CdpIds[idxLast];

        CdpIds[index] = idToMove;
        Cdps[idToMove].arrayIndex = index;
        emit CdpArrayIndexUpdated(idToMove, index);

        CdpIds.pop();
    }

616      function getAccumulatedFeeSplitApplied(
        bytes32 _cdpId,
        uint256 _systemStEthFeePerUnitIndex
    ) public view returns (uint256, uint256) {
        uint256 _cdpStEthFeePerUnitIndex = cdpStEthFeePerUnitIndex[_cdpId];
        uint256 _cdpCol = Cdps[_cdpId].coll;

        if (
            _cdpStEthFeePerUnitIndex == 0 ||
            _cdpCol == 0 ||
            _cdpStEthFeePerUnitIndex == _systemStEthFeePerUnitIndex
        ) {
            return (0, _cdpCol);
        }

        uint256 _feeSplitDistributed = Cdps[_cdpId].stake *
            (_systemStEthFeePerUnitIndex - _cdpStEthFeePerUnitIndex);

        uint256 _scaledCdpColl = _cdpCol * DECIMAL_PRECISION;

        if (_scaledCdpColl > _feeSplitDistributed) {
            return (
                _feeSplitDistributed,
                (_scaledCdpColl - _feeSplitDistributed) / DECIMAL_PRECISION
            );
        } else {
            // extreme unlikely case to skip fee split on this CDP to avoid revert
            return (0, _cdpCol);
        }
    }

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L260-L280

Estimated gas saved:
This optimization reduces the number of storage operations from 4,2 to 1 in each functions. Given that a storage operation costs 20,000 gas, this optimization could save approximately 20,000 gas per call to these functions

### Possible Optimization CollSurplusPool.sol

In the increaseSurplusCollShares and claimSurplusCollShares function, the balances[_account]  mapping is updated twice. This can be optimized to a single update, which would save gas.

```solidity
file:  main/packages/contracts/contracts/CollSurplusPool.sol

77   function increaseSurplusCollShares(address _account, uint256 _amount) external override {
        _requireCallerIsCdpManager();

        uint256 newAmount = balances[_account] + _amount;
        balances[_account] = newAmount;

        emit SurplusCollSharesUpdated(_account, newAmount);
    }

89      function claimSurplusCollShares(address _account) external override {
        _requireCallerIsBorrowerOperations();
        uint256 claimableColl = balances[_account];
        require(claimableColl > 0, "CollSurplusPool: No collateral available to claim");

        balances[_account] = 0;
        emit SurplusCollSharesUpdated(_account, 0);


```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L77-L84

Estimated gas saved:
This optimization reduces the number of storage operations from 2 to 1 in each functions. Given that a storage operation costs 10,000 gas, this optimization could save approximately 10,000 gas per call to these functions

### Possible Optimization EBTCToken.sol

In the _transfer function, the  _balances[recipient]   mapping is updated twice. This can be optimized to a single update, which would save gas.

```solidity 
file:  main/packages/contracts/contracts/EBTCToken.sol

246   function _transfer(address sender, address recipient, uint256 amount) internal {
        require(sender != address(0), "EBTCToken: zero sender!");
        require(recipient != address(0), "EBTCToken: zero recipient!");

        uint256 cachedSenderBalances = _balances[sender];
        require(cachedSenderBalances >= amount, "ERC20: transfer amount exceeds balance");

        unchecked {
            // Safe because of the check above
            _balances[sender] = cachedSenderBalances - amount;
        }

        _balances[recipient] = _balances[recipient] + amount;
        emit Transfer(sender, recipient, amount);
    }

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L246-L260

Estimated gas saved:
This optimization reduces the number of storage operations from 2 to 1 in each functions. Given that a storage operation costs 10,000 gas, this optimization could save approximately 10,000 gas per call to these functions

### Possible Optimization EBTCToken.sol

In the _mint and _burn function, the _balances[account] mapping is updated twice. This can be optimized to a single update, which would save gas.

```solidity
file: main/packages/contracts/contracts/EBTCToken.sol

262   function _mint(address account, uint256 amount) internal {
        require(account != address(0), "EBTCToken: mint to zero recipient!");

        _totalSupply = _totalSupply + amount;
        _balances[account] = _balances[account] + amount;
        emit Transfer(address(0), account, amount);
    }

270    function _burn(address account, uint256 amount) internal {
        require(account != address(0), "EBTCToken: burn from zero account!");

        uint256 cachedBalance = _balances[account];
        require(cachedBalance >= amount, "ERC20: burn amount exceeds balance");

        unchecked {
            // Safe because of the check above
            _balances[account] = cachedBalance - amount;
        }

        _totalSupply = _totalSupply - amount;
        emit Transfer(account, address(0), amount);
    }

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L262-L268

Estimated gas saved:
This optimization reduces the number of storage operations from 2 to 1 in each functions. Given that a storage operation costs 5000 gas, this optimization could save approximately 5000 gas per call to these functions

### Possible Optimization RolesAuthority.sol

In the setRoleCapability function, the getRolesWithCapability[target] mapping is updated three time. This can be optimized to a single update, which would save gas.


```solidity
file:  main/packages/contracts/contracts/Dependencies/RolesAuthority.sol

106   function setRoleCapability(
        uint8 role,
        address target,
        bytes4 functionSig,
        bool enabled
    ) public virtual requiresAuth {
        if (enabled) {
            getRolesWithCapability[target][functionSig] |= bytes32(1 << role);
            enabledFunctionSigsByTarget[target].add(bytes32(functionSig));

            if (!targets.contains(target)) {
                targets.add(target);
            }
        } else {
            getRolesWithCapability[target][functionSig] &= ~bytes32(1 << role);
            enabledFunctionSigsByTarget[target].remove(bytes32(functionSig));

            // If no enabled function signatures exist for this target, remove target
            if (enabledFunctionSigsByTarget[target].length() == 0) {
                targets.remove(target);
            }
        }

        emit RoleCapabilityUpdated(role, target, functionSig, enabled);
    }

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L106-L130

Estimated gas saved:
This optimization reduces the number of storage operations from 3 to 1 in each functions. Given that a storage operation costs 20,000 gas, this optimization could save approximately 20,000 gas per call to these functions

### Possible Optimization RolesAuthority.sol

In the setUserRole function, the getUserRoles[user] mapping is updated three time. This can be optimized to a single update, which would save gas.


```solidity
file: main/packages/contracts/contracts/Dependencies/RolesAuthority.sol

147   function setUserRole(address user, uint8 role, bool enabled) public virtual requiresAuth {
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

Estimated gas saved:
This optimization reduces the number of storage operations from 3 to 1 in each functions. Given that a storage operation costs 10,000 gas, this optimization could save approximately 10,000 gas per call to these functions

### Possible Optimization RolesAuthority.sol

In the setPublicCapability function, the capabilityFlag[target][functionSig]  mapping is updated three time. This can be optimized to a single update, which would save gas.

```solidity
file:  main/packages/contracts/contracts/Dependencies/RolesAuthority.sol

85    function setPublicCapability(
        address target,
        bytes4 functionSig,
        bool enabled
    ) public virtual requiresAuth {
        require(
            capabilityFlag[target][functionSig] != CapabilityFlag.Burned,
            "RolesAuthority: Capability Burned"
        );

        if (enabled) {
            capabilityFlag[target][functionSig] = CapabilityFlag.Public;
        } else {
            capabilityFlag[target][functionSig] = CapabilityFlag.None;
        }

        emit PublicCapabilityUpdated(target, functionSig, enabled);
    }

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L85-L102


Estimated gas saved:
This optimization reduces the number of storage operations from 3 to 1 in each functions. Given that a storage operation costs 20,000 gas, this optimization could save approximately 20,000 gas per call to these functions

## [G-09] Don’t cache calls that are only used once

```solidity
file: main/packages/contracts/contracts/BorrowerOperations.sol
 
1056  uint256 _systemCollShares = getSystemCollShares();

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1056


## [G-10] public functions not called by the contract should be declared external instead

when a function is declared as public, it is generated with an internal and an external interface. This means the function can be called both internally (within the contract) and externally (by other contracts or accounts). However, if a public function is never called internally and is only expected to be invoked externally, it is more gas-efficient to explicitly declare it as external.

```solidity
file: main/packages/contracts/contracts/ActivePool.sol

371   function sweepToken(address token, uint256 amount) public nonReentrant requiresAuth {

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L371


```solidity
file:  main/packages/contracts/contracts/CdpManager.sol

570    function getSystemDebt() public view returns (uint256 entireSystemDebt) {

717    function getDeploymentStartTime() public view returns (uint256) {

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L570


```solidity
file: main/packages/contracts/contracts/CdpManagerStorage.sol

701   function getCachedICR(bytes32 _cdpId, uint256 _price) public view returns (uint256) {

719   function getPendingRedistributedDebt(
        bytes32 _cdpId
    ) public view returns (uint256 pendingEBTCDebtReward) {

728  function hasPendingRedistributedDebt(bytes32 _cdpId) public view returns (bool) {

864   function getSyncedICR(bytes32 _cdpId, uint256 _price) public view returns (uint256) {

874   function getSyncedTCR(uint256 _price) public view returns (uint256) {

890   function canLiquidateRecoveryMode(uint256 icr, uint256 tcr) public view returns (bool) {

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L701


```solidity
file: main/packages/contracts/contracts/CollSurplusPool.sol

142  function sweepToken(address token, uint256 amount) public nonReentrant requiresAuth {

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L142


```solidity
file:  main/packages/contracts/contracts/Governor.sol

96    function getRolesFromByteMap(bytes32 byteMap) public pure returns (uint8[] memory roleIds) {

120   function getByteMapFromRoles(uint8[] memory roleIds) public pure returns (bytes32) {

131   function getEnabledFunctionsInTarget(
        address _target
    ) public view returns (bytes4[] memory _funcs) {

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L96


```solidity
file: main/packages/contracts/contracts/LeverageMacroBase.sol

234   function sweepToken(address token, uint256 amount) public {

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L234

```solidity
file: main/packages/contracts/contracts/LeverageMacroReference.sol

44   function owner() public override returns (address) {
    
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L44


```solidity
file:  main/packages/contracts/contracts/SortedCdps.sol

130   function nonExistId() public pure override returns (bytes32) {

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L130


```solidity
file:  main/packages/contracts/contracts/Dependencies/Auth.sol

42  function setAuthority(Authority newAuthority) public virtual {

52  function transferOwnership(address newOwner) public virtual requiresAuth {

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L42


```solidity
file: main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol

38   function setAuthority(address newAuthority) public virtual {

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L38


```solidity
file: main/packages/contracts/contracts/Dependencies/RolesAuthority.sol

42   function doesRoleHaveCapability(
        uint8 role,
        address target,
        bytes4 functionSig
    ) public view virtual returns (bool) {

50    function isPublicCapability(address target, bytes4 functionSig) public view returns (bool) {

63  function canCall(
        address user,
        address target,
        bytes4 functionSig
    ) public view virtual override returns (bool) {
    
85  function setPublicCapability(
        address target,
        bytes4 functionSig,
        bool enabled
    ) public virtual requiresAuth {
    
106    function setRoleCapability(
        uint8 role,
        address target,
        bytes4 functionSig,
        bool enabled
    ) public virtual requiresAuth {
    
133  function burnCapability(address target, bytes4 functionSig) public virtual requiresAuth {

147  function setUserRole(address user, uint8 role, bool enabled) public virtual requiresAuth {

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L42-L46


## [G-11] Do not calculate constants

```solidity
file: main/packages/contracts/contracts/CdpManagerStorage.sol

141  uint256 public constant MIN_REDEMPTION_FEE_FLOOR = (DECIMAL_PRECISION * 5) / 1000; // 0.5%

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L141'

```solidity
file: main/packages/contracts/contracts/Dependencies/EbtcBase.sol

28    uint256 public constant LIQUIDATOR_REWARD = 2e17;

31   uint256 public constant MIN_NET_STETH_BALANCE = 2e18;

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L28

```solidity
file: main/packages/contracts/contracts/PriceFeed.sol

36   uint256 public constant MAX_PRICE_DEVIATION_FROM_PREVIOUS_ROUND = 5e17; // 50%

42   uint256 public constant MAX_PRICE_DIFFERENCE_BETWEEN_ORACLES = 5e16; // 5%

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L36

```solidity
file: main/packages/contracts/contracts/Dependencies/EbtcMath.sol

6  uint256 internal constant DECIMAL_PRECISION = 1e18;

7   uint256 public constant MAX_TCR = type(uint256).max;

18   uint256 internal constant NICR_PRECISION = 1e20;

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L6


## [G-12] State variables which are not modified within functions should be set as constant or immutable for values set at deployment

Cache such variables and perform operations on them, if operations include modifications to the state variable(s) then remember to equate the state variable to it’s cached counterpart at the end

```solidity
file: main/packages/contracts/contracts/CdpManagerStorage.sol

142   uint256 public redemptionFeeFloor = MIN_REDEMPTION_FEE_FLOOR;
 
143   bool public redemptionsPaused;

148   uint256 public minuteDecayFactor = 999037758833783000;

159   uint256 public beta = 2;

161   uint256 public baseRate;

166   uint256 public lastRedemptionTimestamp;

193   uint256 public lastEBTCDebtErrorRedistribution;

```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L142


```solidity
file: main/packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol
 
14   uint16 public feeBps = 3; // may be subject to future adjustments through protocol governance

15   bool public flashLoansPaused;

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L14


```solidity
file: main/packages/contracts/contracts/Dependencies/ReentrancyGuard.sol

11    uint256 public locked = OPEN;

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ReentrancyGuard.sol#L11

```solidity
file: main/packages/contracts/contracts/Dependencies/RolesAuthority.sol

30   EnumerableSet.Bytes32Set internal enabledFunctionSigsPublic;

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L30

## [G-13] Use assembly in place of abi.decode to extract calldata values more efficiently

Instead of using abi.decode, we can use assembly to decode our desired calldata values directly. This will allow us to avoid decoding calldata values that we will not use.

```solidity
file: main/packages/contracts/contracts/LeverageMacroBase.sol

339   LeverageMacroOperation memory leverageMacroData = abi.decode(data, (LeverageMacroOperation));

461   OpenCdpOperation memory flData = abi.decode(data, (OpenCdpOperation));

475   CloseCdpOperation memory flData = abi.decode(data, (CloseCdpOperation));

483   AdjustCdpOperation memory flData = abi.decode(data, (AdjustCdpOperation));

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L339


## [G-14] Use assembly to emit an event

```solidity
file: main/packages/contracts/contracts/ActivePool.sol

65   emit FeeRecipientAddressChanged(_feeRecipientAddress);

112  emit SystemCollSharesUpdated(cachedSystemCollShares);

113  emit CollSharesTransferred(_account, _shares);

145  emit SystemCollSharesUpdated(cachedSystemCollShares);

146  emit CollSharesTransferred(_account, totalShares);

173  emit SystemCollSharesUpdated(cachedSystemCollShares);

174  emit FeeRecipientClaimableCollSharesIncreased(cachedFeeRecipientCollShares, _shares);

200   emit ActivePoolEBTCDebtUpdated(cachedSystemDebt);

213   emit ActivePoolEBTCDebtUpdated(cachedSystemDebt);

247   emit SystemCollSharesUpdated(cachedSystemCollShares);

307   emit FlashLoanSuccess(address(receiver), token, amount, fee);

360   emit FeeRecipientClaimableCollSharesDecreased(cachedFeeRecipientCollShares, _shares);

383   emit SweepTokenSuccess(token, amount, cachedFeeRecipientAddress);

399   emit FeeRecipientAddressChanged(_feeRecipientAddress);

412   emit FlashFeeSet(msg.sender, _oldFee, _newFee);

421   emit FlashLoansPaused(msg.sender, _paused);

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L65

```solidity
file:  main/packages/contracts/contracts/BorrowerOperations.sol

136    emit FeeRecipientAddressChanged(_feeRecipientAddress);

641    emit PositionManagerApprovalSet(_borrower, _positionManager, _approval);

1105   emit FlashLoanSuccess(address(receiver), token, amount, fee);

1149   emit FeeRecipientAddressChanged(_feeRecipientAddress);

1162   emit FlashFeeSet(msg.sender, _oldFee, _newFee);

1171   emit FlashLoansPaused(msg.sender, _paused);

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L136


```solidity
file: main/packages/contracts/contracts/CdpManager.sol

55    emit StakingRewardSplitSet(stakingRewardSplit);

179   emit CdpUpdated(

220   emit CdpUpdated(

466   emit Redemption(

545   emit CdpUpdated(_cdpId, _borrower, msg.sender, _debt, _coll, 0, 0, 0, CdpOperation.closeCdp);

630   emit BaseRateUpdated(newBaseRate);

681   emit BaseRateUpdated(decayedBaseRate);

698   emit LastRedemptionTimestampUpdated(block.timestamp);

782   emit StakingRewardSplitSet(_stakingRewardSplit);

801   emit RedemptionFeeFloorSet(_redemptionFeeFloor);

824   emit MinuteDecayFactorSet(_minuteDecayFactor);

836   emit BetaSet(_beta);

848   emit RedemptionsPaused(_paused);

925   emit CdpUpdated(

961   emit CdpUpdated(

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L55

```solidity
file: main/packages/contracts/contracts/CdpManagerStorage.sol

50    emit TCRNotified(_tcr);

55    emit GracePeriodStart();

64    emit TCRNotified(_tcr);

69    emit GracePeriodEnd();

119   emit GracePeriodDurationSet(_gracePeriod);

300   emit SystemSnapshotsUpdated(_totalStakesSnapshot, _totalCollateralSnapshot);

340   emit CdpDebtRedistributionIndexUpdated(_cdpId, _systemDebtRedistributionIndex);

390   emit CdpUpdated(

414   emit TotalStakesUpdated(_newTotalStakes);

425   emit TotalStakesUpdated(_newTotalStakes);

481   emit CdpArrayIndexUpdated(idToMove, index);

542   emit StEthIndexUpdated(_oldIndex, _newIndex, block.timestamp);

587   emit CollateralFeePerUnitUpdated(_oldPerUnit, _newPerUnit, _feeTaken);

602   emit CdpFeeSplitApplied(

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L50

```solidity
file:  main/packages/contracts/contracts/CollSurplusPool.sol

83     emit SurplusCollSharesUpdated(_account, newAmount);

95     emit SurplusCollSharesUpdated(_account, 0);

104    emit CollSharesTransferred(_account, claimableColl);

150    emit SweepTokenSuccess(token, amount, feeRecipientAddress);

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L83


```solidity
file: main/packages/contracts/contracts/EBTCToken.sol

259    emit Transfer(sender, recipient, amount);

267    emit Transfer(address(0), account, amount);

282    emit Transfer(account, address(0), amount);

290     emit Approval(owner, spender, amount);

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L259

```solidity
file:  main/packages/contracts/contracts/Governor.sol

157   emit RoleNameSet(role, roleName);

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L157


```solidity
file: main/packages/contracts/contracts/LeverageMacroFactory.sol

56   emit DeployNewMacro(_owner, addy);

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L56


```solidity
file: main/packages/contracts/contracts/LiquidationLibrary.sol

238   emit CdpUpdated(

281   emit CdpLiquidated(

312   emit CdpUpdated(

367   emit CdpLiquidated(

437   emit CdpPartiallyLiquidated(

490   emit CdpUpdated(

516   emit Liquidation(totalDebtToBurn, totalCollSharesToSend, totalLiquidatorRewardCollShares);

891   emit SystemDebtRedistributionIndexUpdated(systemDebtRedistributionIndex);

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L238


```solidity
file: main/packages/contracts/contracts/PriceFeed.sol

67    emit FallbackCallerChanged(address(0), _fallbackCallerAddress);

378   emit FallbackCallerChanged(oldFallbackCaller, _fallbackCaller);

381   emit UnhealthyFallbackCaller(_fallbackCaller, block.timestamp);

387   emit FallbackCallerChanged(oldFallbackCaller, _fallbackCaller);

548   emit PriceFeedStatusChanged(_status);

555   emit LastGoodPriceUpdated(_currentPrice);

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L67


```solidity
file: main/packages/contracts/contracts/SortedCdps.sol

405   emit NodeAdded(_id, _NICR);

451   emit NodeRemoved(_ids[i]);

490   emit NodeRemoved(_id);

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L405


```solidity
file: main/packages/contracts/contracts/Dependencies/Auth.sol

22   emit OwnershipTransferred(msg.sender, _owner);

23   emit AuthorityUpdated(msg.sender, _authority);

49   emit AuthorityUpdated(msg.sender, newAuthority);

55   emit OwnershipTransferred(msg.sender, newOwner);

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L22


```solidity
file: main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol

50    emit AuthorityUpdated(msg.sender, Authority(newAuthority));

62    emit AuthorityUpdated(address(this), Authority(newAuthority));

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L50


```solidity
file: main/packages/contracts/contracts/Dependencies/RolesAuthority.sol

101    emit PublicCapabilityUpdated(target, functionSig, enabled);

129    emit RoleCapabilityUpdated(role, target, functionSig, enabled);

140    emit CapabilityBurned(target, functionSig);

163    emit UserRoleUpdated(user, role, enabled);

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L101


## [G-15] Use hardcoded address instead of address(this)
 
Instead of using address(this), it is more gas-efficient to pre-calculate and use the hardcoded address. Foundry’s script.sol and solmate’s LibRlp.sol contracts can help achieve.

```solidity
file: main/packages/contracts/contracts/ActivePool.sol

283   collateral.transferFrom(address(receiver), address(this), amountWithFee);

295   collateral.balanceOf(address(this)) >= collateral.getPooledEthByShares(systemCollShares),

299   collateral.sharesOf(address(this)) >= systemCollShares,

337   return collateral.balanceOf(address(this));

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L283

```solidity
file:  main/packages/contracts/contracts/BorrowerOperations.sol

682   return keccak256(abi.encode(typeHash, name, version, _chainID(), address(this)));

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L682

```solidity
file:  main/packages/contracts/contracts/CollSurplusPool.sol

145    uint256 balance = IERC20(token).balanceOf(address(this));

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L145


```solidity
file:  main/packages/contracts/contracts/EBTCToken.sol

240   return keccak256(abi.encode(typeHash, name, version, _chainID(), address(this)));

297   _recipient != address(0) && _recipient != address(this),

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L240


```solidity
file: main/packages/contracts/contracts/LeverageMacroBase.sol

131    address(this),

143    initialCdpIndex = sortedCdps.cdpCountOf(address(this));

149    IERC3156FlashBorrower(address(this)),

156    IERC3156FlashBorrower(address(this)),

173    bytes32 cdpId = sortedCdps.cdpOfOwnerByIndex(address(this), initialCdpIndex);

220    uint256 ebtcBal = ebtcToken.balanceOf(address(this));

221    uint256 collateralBal = stETH.sharesOf(address(this));

352    require(initiator == address(this), "LeverageMacroReference: wrong initiator for flashloan");

441    IERC20(swapChecks[i].tokenToCheck).balanceOf(address(this)) >

456    require(addy != address(this)); // If it could call this it could fake the forwarded caller

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L131 

```solidity
file: main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol

64   address _owner = IOwnerLike(address(this)).owner();

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L64


```solidity
file: main/packages/contracts/contracts/SimplifiedDiamondLike.sol
 
77   require(msg.sender == address(this)); // Must call this via `execute` to explicitly set the flag

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L77


```solidity
file: main/packages/contracts/contracts/Dependencies/Auth.sol

38   (address(auth) != address(0) && auth.canCall(user, address(this), functionSig)) ||

45   require(msg.sender == owner || authority.canCall(msg.sender, address(this), msg.sig));

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L38


```solidity
file:  main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol

35   return (address(auth) != address(0) && auth.canCall(user, address(this), functionSig));

41   require(_authority.canCall(msg.sender, address(this), msg.sig));

62   emit AuthorityUpdated(address(this), Authority(newAuthority));

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L35

## [G-16] Use assembly to write address storage values

```solidity
file: main/packages/contracts/contracts/ActivePool.sol

57   feeRecipientAddress = _feeRecipientAddress;

398  feeRecipientAddress = _feeRecipientAddress;

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L57


```solidity
file: main/packages/contracts/contracts/BorrowerOperations.sol

121    feeRecipientAddress = _feeRecipientAddress;

1148   feeRecipientAddress = _feeRecipientAddress;

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L121

```solidity
file: main/packages/contracts/contracts/Dependencies/Auth.sol

19   owner = _owner;

53   owner = newOwner;

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L19

## [G-17] Use uint256(1)/uint256(2) instead for true and false boolean states

Use uint256(1) and uint256(2) for true/false to avoid a Gwarmaccess (100 gas), and to avoid Gsset (20000 gas) when changing from ‘false’ to ‘true’, after having been ‘true’ in the past. see source:

```solidity
file: main/packages/contracts/contracts/CdpManagerStorage.sol

143  bool public redemptionsPaused;

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L143

```solidity
file: main/packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol

15   bool public flashLoansPaused;

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L15

```solidity
file: main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol

14   bool private _authorityInitialized;

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L14

```solidity
file: main/packages/contracts/contracts/LeverageMacroBase.sol

35   bool internal immutable willSweep;

58   bool _sweepToCaller

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L35

```solidity
file: main/packages/contracts/contracts/LiquidationLibrary.sol

100    bool _recoveryModeAtStart = _TCR < CCR ? true : false;

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L100


```solidity
file: main/packages/contracts/contracts/SimplifiedDiamondLike.sol

29    bool allowNonCallback;

30    bool callbackEnabledForCall;

101   bool checkSuccess; // If false we will ignore a revert

104   bool capGas; // true to use above "gas" setting or we send gasleft()

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L29

```solidity
file: main/packages/contracts/contracts/BorrowerOperations.sol

76   bool isCollIncrease;

101  bool isCollIncrease;

103  bool isDebtIncrease;

384  bool isRecoveryMode = _checkRecoveryModeForTCR(_getCachedTCR(vars.price));

481  bool isRecoveryMode = _checkRecoveryModeForTCR(_getCachedTCR(vars.price));

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L76


```solidity
file: main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol

125   bool recoveryModeAtStart;

149   bool recoveryModeAtStart;

158   bool backToNormalMode;

213   bool cancelledPartial;

214   bool fullRedemption;

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L125

```solidity
file: main/packages/contracts/contracts/Interfaces/IPriceFeed.sol

23    bool success;

29    bool success;

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPriceFeed.sol#L23


## [G-18] Use assembly to validate msg.sender

We can use assembly to efficiently validate msg.sender for the didPay and uniswapV3SwapCallback functions with the least amount of opcodes necessary. Additionally, we can use xor() instead of iszero(eq()), saving 3 gas. We can also potentially save gas on the unhappy path by using scratch space to store the error selector, potentially avoiding memory expansion costs.


```solidity
file: main/packages/contracts/contracts/BorrowerOperations.sol

964    if (_borrower == msg.sender) {

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L964


```solidity
file: main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol
 
17    require(isAuthorized(msg.sender, msg.sig), "Auth: UNAUTHORIZED");

41    require(_authority.canCall(msg.sender, address(this), msg.sig));

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L17

```solidity
file: main/packages/contracts/contracts/SimplifiedDiamondLike.sol

52   require(msg.sender == owner);

67   require(msg.sender == owner);

77   require(msg.sender == address(this)); // Must call this via `execute` to explicitly set the flag

111  require(msg.sender == owner, "Must be owner");

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L52

```solidity
file: main/packages/contracts/contracts/Dependencies/Auth.sol

27    require(isAuthorized(msg.sender, msg.sig), "Auth: UNAUTHORIZED");

45    require(msg.sender == owner || authority.canCall(msg.sender, address(this), msg.sig));

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L27

```solidity
file:  main/packages/contracts/contracts/SortedCdps.sol

715   require(msg.sender == address(cdpManager), "SortedCdps: Caller is not the CdpManager");'

720     require(
            msg.sender == borrowerOperationsAddress || msg.sender == address(cdpManager),
            "SortedCdps: Caller is neither BO nor CdpM"
        );

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L715

```solidity
file:  main/packages/contracts/contracts/EBTCToken.sol

315    require(
            msg.sender == borrowerOperationsAddress ||
                msg.sender == cdpManagerAddress ||
                isAuthorized(msg.sender, msg.sig),
            "EBTC: Caller is neither BorrowerOperations nor CdpManager nor authorized"
        );

324   require(msg.sender == cdpManagerAddress, "EBTC: Caller is not CdpManager");

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L315-L320

```solidity
file:  main/packages/contracts/contracts/CollSurplusPool.sol

114    msg.sender == borrowerOperationsAddress,

120    require(msg.sender == cdpManagerAddress, "CollSurplusPool: Caller is not CdpManager");

124    require(msg.sender == activePoolAddress, "CollSurplusPool: Caller is not Active Pool");

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L114

```solidity
file:  main/packages/contracts/contracts/ActivePool.sol

221    msg.sender == borrowerOperationsAddress,

229    msg.sender == borrowerOperationsAddress || msg.sender == cdpManagerAddress,

236    require(msg.sender == cdpManagerAddress, "ActivePool: Caller is not CdpManager");

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L221

## [G-19] Use assembly for loops

In the following instances, assembly is used for more gas efficient loops. The only memory slots that are manually used in the loops are scratch space (0x00-0x20), the free memory pointer (0x40), and the zero slot (0x60). This allows us to avoid using the free memory pointer to allocate new memory, which may result in memory expansion costs.

Note that in order to do this optimization safely we will need to cache and restore the free memory pointer after the loop. We will also set the zero slot (0x60) back to 0.


```solidity
file:  main/packages/contracts/contracts/Governor.sol

46    for (uint256 i = 0; i < users.length(); i++) {
            address user = users.at(i);
            bool _canCall = doesUserHaveRole(user, role);
            if (_canCall) {
                count += 1;
            }
        }

76    for (uint8 i = 0; i < type(uint8).max; i++) {
            if (doesUserHaveRole(user, i)) {
                count += 1;
            }
        }

98    for (uint8 i = 0; i < type(uint8).max; i++) {
            bool roleEnabled = (uint256(byteMap >> i) & 1) != 0;
            if (roleEnabled) {
                count += 1;
            }
        }

122   for (uint8 i = 0; i < roleIds.length; i++) {
            _data |= bytes32(1 << uint256(roleIds[i]));
        }

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L46-L52


```solidity
file: main/packages/contracts/contracts/LeverageMacroBase.sol

385   for (uint256 i; i < swapLength; ) {
            _doSwap(swapData[i]);
            unchecked {
                ++i;
            }
        }

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L385-L390


```solidity
file: main/packages/contracts/contracts/SimplifiedDiamondLike.sol

114   for (uint256 i; i < length; ) {
            _executeOne(ops[i]);

            unchecked {
                ++i;
            }
        }

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L114-L121


```solidity
file:  main/packages/contracts/contracts/SortedCdps.sol

432  for (uint256 i = 0; i < _len; ++i) {
            require(contains(_ids[i]), "SortedCdps: List does not contain the id");
        }

449    for (uint i = 0; i < _len; ++i) {
            delete data.nodes[_ids[i]];
            emit NodeRemoved(_ids[i]);
        }

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L432-L433

## [G-20] abi.encode() is less efficient than abi.encodepacked()

In terms of efficiency, abi.encodePacked() is generally considered to be more gas-efficient than abi.encode(), because it skips the step of adding function signatures and other metadata to the encoded data. However, this comes at the cost of reduced safety, as abi.encodePacked() does not perform any type checking or padding of data.

Refference: https://github.com/ConnorBlockchain/Solidity-Encode-Gas-Comparison

```solidity
file: main/packages/contracts/contracts/BorrowerOperations.sol

682    return keccak256(abi.encode(typeHash, name, version, _chainID(), address(this)));

722    abi.encode(

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L682


```solidity
file:  main/packages/contracts/contracts/LeverageMacroBase.sol

152    abi.encode(operation)

159    abi.encode(operation)

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L152

## [G-21] Using delete statement can save gas

```solidity
file: main/packages/contracts/contracts/CdpManagerStorage.sol

276    cdpDebtRedistributionIndex[_cdpId] = 0;

277    cdpStEthFeePerUnitIndex[_cdpId] = 0;

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L276


```solidity
file: main/packages/contracts/contracts/CollSurplusPool.sol

94    balances[_account] = 0;

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L94


## [G-22] Use nested if/require statements instead of &&

```solidity 
file:  main/packages/contracts/contracts/BorrowerOperations.sol

393    if (!_isDebtIncrease && _debtChange > 0) {

734   require(
            recoveredAddress != address(0) && recoveredAddress == _borrower,

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L393


```solidity
file:  main/packages/contracts/contracts/LiquidationLibrary.sol

756   if (vars.cdpId != bytes32(0) && Cdps[vars.cdpId].status == Status.active) {

819   if (vars.cdpId != bytes32(0) && Cdps[vars.cdpId].status == Status.active) {

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L756

```solidity
file: main/packages/contracts/contracts/SortedCdps.sol

202   if (maxNodes > 0 && i >= maxNodes) {

259   if (maxNodes > 0 && i >= maxNodes) {

330   if (maxNodes > 0 && i >= maxNodes) {

382   if (prevId == dummyId && nextId == dummyId) {

621   if (data.head == _startId && _NICR >= cdpManager.getCachedNominalICR(_startId)) {

644   if (data.tail == _startId && _NICR <= cdpManager.getCachedNominalICR(_startId)) {

696   if (prevId == dummyId && nextId == dummyId) {

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L202

```solidity
file: main/packages/contracts/contracts/CdpManagerStorage.sol

261   require(
            closedStatus != Status.nonExistent && closedStatus != Status.active,
            "CdpManagerStorage: close non-exist or non-active CDP!"
        );
466   require(
            cdpStatus != Status.nonExistent && cdpStatus != Status.active,
            "CdpManagerStorage: remove non-exist or non-active CDP!"
        );

512    if (_newIndex > _oldIndex && totalStakes > 0) {

653   require(
            CdpOwnersArrayLength > 1 && sortedCdps.getSize() > 1,
            "CdpManager: Only one cdp in the system"
        );

765   if (_newIndex > _oldIndex && totalStakes > 0) {

796   if (_cdpPerUnitIdx != _systemStEthFeePerUnitIndex && _cdpPerUnitIdx > 0) {

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L261-L264


```solidity
file:  main/packages/contracts/contracts/EBTCToken.sol

296    require(
            _recipient != address(0) && _recipient != address(this),
            "EBTC: Cannot transfer tokens directly to the EBTC token contract or the zero address"
        );

300    require(
            _recipient != cdpManagerAddress && _recipient != borrowerOperationsAddress,
            "EBTC: Cannot transfer tokens directly to the CdpManager or BorrowerOps"
        );

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L296-L299

## [G‑23] Counting down in for statements is more gas efficient

Counting down is more gas efficient than counting up because neither we are making zero variable to non-zero variable and also we will get gas refund in the last transaction when making non-zero to zero variable.


```solidity
file: main/packages/contracts/contracts/Governor.sol

46   for (uint256 i = 0; i < users.length(); i++) {

57   for (uint256 i = 0; i < _usrs.length; i++) {

76   for (uint8 i = 0; i < type(uint8).max; i++) {

84   for (uint8 i = 0; i < type(uint8).max; i++) {

98   for (uint8 i = 0; i < type(uint8).max; i++) {

107  for (uint8 i = 0; i < type(uint8).max; i++) {

122  for (uint8 i = 0; i < roleIds.length; i++) {

137  for (uint256 i = 0; i < _sigs.length; ++i) {

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L46


```solidity
file: main/packages/contracts/contracts/LeverageMacroBase.sol

385   for (uint256 i; i < swapLength; ) {

438   for (uint256 i; i < length; ++i) {

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L385


```solidity
file: main/packages/contracts/contracts/SimplifiedDiamondLike.sol

114   for (uint256 i; i < length; ) {

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L114


```solidity
file:  main/packages/contracts/contracts/SortedCdps.sol

432    for (uint256 i = 0; i < _len; ++i) {

449    for (uint i = 0; i < _len; ++i) {

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L432

### Test Code

```solidity

contract GasTest is DSTest {
    Contract0 c0;
    Contract1 c1;
    function setUp() public {
        c0 = new Contract0();
        c1 = new Contract1();
    }
    function testGas() public {
        c0.AddNum();
        c1.AddNum();
    }
}
contract Contract0 {
    uint256 num = 3;
    function AddNum() public {
        uint256 _num = num;
        for(uint i=0;i<=9;i++){
            _num = _num +1;
        }
        num = _num;
    }
}
contract Contract1 {
    uint256 num = 3;
    function AddNum() public {
        uint256 _num = num;
        for(uint i=9;i>=0;i--){
            _num = _num +1;
        }
        num = _num;
    }
}

```

## [G-24] Create immutable variable to avoid an external call

Instead of performing an external call to get the root address each time _enableNode is invoked, we can perform this external call once in the constructor and store the root as an immutable variable. Doing this will save 1 external call each time _enableNode is invoked.

```solidity
file: main/packages/contracts/contracts/PriceFeed.sol

360   IFallbackCaller newFallbackCaler = IFallbackCaller(_fallbackCaller);

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L360

```solidity
file: main/packages/contracts/contracts/Dependencies/Auth.sol

33    Authority auth = authority; // Memoizing authority saves us a warm SLOAD, around 100 gas.

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L33

```solidity
file: main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol

31   Authority auth = _authority; // Memoizing authority saves us a warm SLOAD, around 100 gas.

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L31



## [G-24] Avoid Unnecessary Public Variables

Public storage variables increase the contract's size due to the implicit generation of public getter functions. This makes the contract larger and could increase deployment and interaction costs.

If you do not require other contracts to read these variables, consider making them private or internal.

```solidity
file: main/packages/contracts/contracts/CdpManagerStorage.sol

24   uint128 public lastGracePeriodStartTimestamp = UNSET_TIMESTAMP; // use max to signify

25   uint128 public recoveryModeGracePeriodDuration = MINIMUM_GRACE_PERIOD;

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L24

```solidity
file: main/packages/contracts/contracts/BorrowerOperations.sol

57   address public feeRecipientAddress;

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L57

```solidity
file: main/packages/contracts/contracts/PriceFeed.sol

29   IFallbackCaller public fallbackCaller; 

45   uint256 public lastGoodPrice;

48   Status public status;

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L29

```solidity
file: main/packages/contracts/contracts/SortedCdps.sol

77  Data public data;

79  uint256 public nextCdpNonce;

80  bytes32 public constant dummyId =
        0x0000000000000000000000000000000000000000000000000000000000000000;

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L77

```solidity
file: main/packages/contracts/contracts/Dependencies/Auth.sol

14   address public owner;

16   Authority public authority;

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L14


```solidity
file: main/packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol

14    uint16 public feeBps = 3; // may be subject to future adjustments through protocol governance

15    bool public flashLoansPaused;

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L14


```solidity
file: main/packages/contracts/contracts/Dependencies/ReentrancyGuard.sol

11  uint256 public locked = OPEN;

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ReentrancyGuard.sol#L11