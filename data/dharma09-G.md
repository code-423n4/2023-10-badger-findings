## Summary

The findings from the bot should be reviewed as they contain some solid issues The following findings were missed by the bot(in some cases,bot has identified some instances but missed others, I try to explain whenever this happens)

Gas estimates are done using the opcodes involved since most of this functions were not covered by tests


## Gas Optimizations


| |Issue|Instances||
|-|:-|:-:|:-:|
|[GAS-01](#GAS-01)|Use uint256(1)/uint256(2) instead for true and false boolean states|4|
|[GAS-02](#GAS-02)|Structs can be packed into fewer storage slots|1|
|[GAS-03](#GAS-03)|State variables only set in the constructor should be declared immutable|3|
|[GAS-04](#GAS-04)|Cache state variables with stack variables|2|
|[GAS-05](#GAS-05)|Use assembly for back to back external call|3|
|[GAS-06](#GAS-06)|mark constant for enum variable|1|
|[GAS-07](#GAS-07)|Do not emit block.timestamp in event|1|
|[GAS-08](#GAS-08)|if function check Use only once then  its better to use inline |2|
|[GAS-09](#GAS-09)|Move the declaration of user outside the loop to reduce SLOAD (storage load) operations, as storage reads can be expensive in terms of gas.|1|
|[GAS-10](#GAS-10)|Consider activating via-ir for deploying||
| [GAS-11](#GAS-11) | Reduce gas usage by moving to Solidity 0.8.19 or later | 39 |
| [GAS-12](#GAS-12) | `abi.encode` is more efficient than `abi.encodePacked` | 3 |
| [GAS-13](#GAS-3) | Use assembly to check for `address(0)` | 29 |
| [GAS-14](#GAS-4) | With assembly, .call (bool success) transfer can be done gas-optimized | 5 |
| [GAS-15](#GAS-5) | Use assembly to emit events | 88 |
| [GAS-16](#GAS-6) | `array[index] += amount` is cheaper than `array[index] = array[index] + amount` (or related variants) | 2 |
| [GAS-17](#GAS-7) | Redundant event fields can be removed | 3 |
| [GAS-18](#GAS-9) | <array>.length should not be looked up in every loop of a for-loop | 5 |
| [GAS-19](#GAS-10) | State variables should be cached in stack variables rather than re-reading them from storage | 2 |
| [GAS-20](#GAS-11) | Use calldata instead of memory for function arguments that do not get mutated | 6 |
| [GAS-21](#GAS-12) | For Operations that will not overflow, you could use unchecked | 67 |
| [GAS-22](#GAS-13) | Don't compare boolean expressions to boolean literals | 1 |
| [GAS-23](#GAS-14) | Use Custom Errors | 87 |
| [GAS-24](#GAS-15) | Multiplication/division by two should use bit shifting | 5 |
| [GAS-25](#GAS-16) | Use of emit inside a loop | 1 |
| [GAS-26](#GAS-17) | >=/ <= costs less gas than >/< | 126 |
| [GAS-27](#GAS-18) | Use hardcode address instead of address(this)  | 27 |
| [GAS-28](#GAS-19) | Don't initialize variables with default value | 19 |
| [GAS-29](#GAS-20) | Long revert strings | 55 |
| [GAS-30](#GAS-21) | Constructors can be marked payable | 19 |
| [GAS-31](#GAS-22) | `++i` costs less gas than `i++`, especially when it's used in `for`-loops (`--i`/`i--` too) | 13 |
| [GAS-32](#GAS-23) | Using `private` rather than `public` for constants, saves gas | 31 |
| [GAS-33](#GAS-24) | Use shift Right/Left instead of division/multiplication if possible | 3 |
| [GAS-34](#GAS-25) | Usage of smaller uint/int types causes overhead | 43 |
| [GAS-35](#GAS-26) | `++i/i++` should be `unchecked{++i}/unchecked{i++}` when it is not possible for them to overflow, as is the case when used in forand whileloops | 13 |
| [GAS-36](#GAS-27) | Use != 0 instead of > 0 for unsigned integer comparison | 53 |
| [GAS-37](#GAS-28) | `internal` functions not called by the contract should be removed | 8 |




### [G-01] Use uint256(1)/uint256(2) instead for true and false boolean states

Use uint256(1) and uint256(2) for true/false to avoid a Gwarmaccess (100 gas), and to avoid Gsset (20000 gas) when changing from ‘false’ to ‘true’, after having been ‘true’ in the past. See [source](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/58f635312aa21f947cae5f8578638a85aa2519f5/contracts/security/ReentrancyGuard.sol#L23-L27).

Instances of this issue:

[[143]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L143)

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

143:     bool public redemptionsPaused;

```

,[[14]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L14)

```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

14:     bool private _authorityInitialized;

```

,[[15]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L15)

```solidity
File: packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol

15:     bool public flashLoansPaused;

```

,[[35]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L35)

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

35:     bool internal immutable willSweep;

```

### [G-02] Structs can be packed into fewer storage slots

Each slot saved can avoid an extra Gsset (**20000 gas**) for the first setting of the struct. Subsequent reads as well as writes have smaller gas savings.

- https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L97C4-L104C6

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol
97:  struct MoveTokensParams { //@audit Struct should pack
        address user; 
        uint256 collSharesChange;
        uint256 collAddUnderlying; // ONLY for isCollIncrease=true
        bool isCollIncrease;
        uint256 netDebtChange;
        bool isDebtIncrease;
    }
// struct MoveTokensParams { //@audit Struct should pack
//        address user; 
//        bool isDebtIncrease;
//        bool isCollIncrease;
//        uint256 collSharesChange;
//        uint256 collAddUnderlying; // ONLY for isCollIncrease=true
//        uint256 netDebtChange;
//    }
```

### [G-03] State variables only set in the constructor should be declared `immutable`

Accessing state variables within a function involves an SLOAD operation, but `immutable` variables can be accessed directly without the need of it, thus reducing gas costs. As these state variables are assigned only in the constructor, consider declaring them `immutable`.

- https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L57

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol
57: address public feeRecipientAddress;
```

- https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L176

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol
176: uint256 public totalCollateralSnapshot; //@audit Mark Immutable

    /*
     * systemDebtRedistributionIndex track the sums of accumulated socialized liquidations per unit staked.
     * During its lifetime, each stake earns:
     *
     * A systemDebt increase  of ( stake * [systemDebtRedistributionIndex - systemDebtRedistributionIndex(0)] )
     *
     * Where systemDebtRedistributionIndex(0) are snapshots of systemDebtRedistributionIndex
     * for the active Cdp taken at the instant the stake was made
     */
 187: uint256 public systemDebtRedistributionIndex;
```

### [G-04] Cache state variables with stack variables

Caching of a state variable replaces each Gwarmaccess (**100 gas**) with a cheaper stack read. Other less obvious fixes/optimizations include having local memory caches of state variable structs, or having local caches of state variable contracts/addresses.

- https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L441

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol
441: function _computeNewStake(uint256 _coll) internal view returns (uint256) {
        uint256 stake;
        if (totalCollateralSnapshot == 0) {
            stake = _coll;
        } else {
            /*
             * The following check holds true because:
             * - The system always contains >= 1 cdp
             * - When we close or liquidate a cdp, we redistribute the pending rewards,
             * so if all cdps were closed/liquidated,
             * rewards would’ve been emptied and totalCollateralSnapshot would be zero too.
             */
            require(totalStakesSnapshot > 0, "CdpManagerStorage: zero totalStakesSnapshot!");
            stake = (_coll * totalStakesSnapshot) / totalCollateralSnapshot; //@audit cache totalStakesSnapshot
        }
        return stake;
```

- https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L295

```solidity
File: packages/contracts/contracts/ActivePool.sol
295: require(
            collateral.balanceOf(address(this)) >= collateral.getPooledEthByShares(systemCollShares),
            "ActivePool: Must repay Balance"
        );
        require(
            collateral.sharesOf(address(this)) >= systemCollShares, //@audit save in memory
            "ActivePool: Must repay Share"
        );
        require(    
            collateral.getPooledEthByShares(DECIMAL_PRECISION) == oldRate,
            "ActivePool: Should keep same collateral share rate"
        );
```

- https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1100

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol
1099: // Send both fee and amount to FEE_RECIPIENT, to burn allowance per EIP-3156
1100:        ebtcToken.transferFrom(address(receiver), feeRecipientAddress, fee + amount); //@audit feeRecipientAddress

        // Burn amount, from FEE_RECIPIENT
        ebtcToken.burn(feeRecipientAddress, amount);
```

### [G-05] Use assembly for back to back external call

- https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L363

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol
363: vars.debt = cdpManager.getCdpDebt(_cdpId); //@audit Use assembly for back-to-back external call
364:        vars.collShares = cdpManager.getCdpCollShares(_cdpId);
```

- https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L465

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol
465: uint256 _netCollAsShares = collateral.getSharesByPooledEth(vars.netStEthBalance); //@audit use assembly for back-to-back external call
466:        uint256 _liquidatorRewardShares = collateral.getSharesByPooledEth(LIQUIDATOR_REWARD);
```

- https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L220

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol
220: uint256 ebtcBal = ebtcToken.balanceOf(address(this)); //@audit Back-to-back external call
221: uint256 collateralBal = stETH.sharesOf(address(this));
```

### [G-06] mark constant for enum variable

- https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L148

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol
148: uint256 public minuteDecayFactor = 999037758833783000; //@audit Use constant
```

### [G-07] Do not emit block.timestamp in event

- https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L542

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol
539: function _syncStEthIndex(uint256 _oldIndex, uint256 _newIndex) internal {
        if (_newIndex != _oldIndex) {
            stEthIndex = _newIndex;
            emit StEthIndexUpdated(_oldIndex, _newIndex, block.timestamp); //@audit Do not emit block.timestamp
        }
    }
```

### [G-08] if function check Use only once then  its better to use inline

- https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L652

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol
652: function _requireMoreThanOneCdpInSystem(uint256 CdpOwnersArrayLength) internal view {
        require(
            CdpOwnersArrayLength > 1 && sortedCdps.getSize() > 1, //@audit
            "CdpManager: Only one cdp in the system"
        );
    }
```

- https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L291

no need to cache length use only once

```diff
File: packages/contracts/contracts/LeverageMacroBase.sol
291: function _handleOperation(LeverageMacroOperation memory operation) internal {
-        uint256 beforeSwapsLength = operation.swapsBefore.length;
-        if (beforeSwapsLength > 0) { //@audit No need to cache length if used once
+        if (operation.swapsBefore.length > 0) {
            _doSwaps(operation.swapsBefore);
        }
```

### [G-09] Move the declaration of user outside the loop to reduce SLOAD (storage load) operations, as storage reads can be expensive in terms of gas.

Optimize gas usage by avoiding variable declarations inside loops

- https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L46C8-L55C27

```solidity
File: packages/contracts/contracts/Governor.sol
43: function getUsersByRole(uint8 role) external view returns (address[] memory usersWithRole) {
        // Search over all users: O(n) * 2
        uint256 count;
        for (uint256 i = 0; i < users.length(); i++) {
            address user = users.at(i); //@audit Move the declaration of user outside the loop to reduce SLOAD (storage load) operations, as storage reads can be expensive in terms of gas.
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
                address user = _usrs[i]; //@audit make variable outside loop
                bool _canCall = doesUserHaveRole(user, role);
                if (_canCall) {
                    usersWithRole[j] = user;
                    j++;
                }
            }
        }
    }
```

### [G-10] Consider activating `via-ir` for deploying

The IR-based code generator was developed to make code generation more performant by enabling optimization passes that can be applied across functions.

It is possible to activate the IR-based code generator through the command line by using the flag `--via-ir` or by including the option `{"viaIR": true}`.

Keep in mind that compiling with this option may take longer. However, you can simply test it before deploying your code. If you find that it provides better performance, you can add the `--via-ir` flag to your deploy command.

 ### <a name="GAS-11"></a>[GAS-11] Reduce gas usage by moving to Solidity 0.8.19 or later

<details>
<summary>There are 39 instances of this issue:</summary>

---

```solidity
File: packages/contracts/contracts/ActivePool.sol

3: pragma solidity 0.8.17;

```

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

3: pragma solidity 0.8.17;

```

```solidity
File: packages/contracts/contracts/CdpManager.sol

3: pragma solidity 0.8.17;

```

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

3: pragma solidity 0.8.17;

```

```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

3: pragma solidity 0.8.17;

```

```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

2: pragma solidity 0.8.17;

```

```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

2: pragma solidity 0.8.17;

```

```solidity
File: packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol

3: pragma solidity 0.8.17;

```

```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

3: pragma solidity 0.8.17;

```

```solidity
File: packages/contracts/contracts/Dependencies/EbtcMath.sol

3: pragma solidity 0.8.17;

```

```solidity
File: packages/contracts/contracts/Dependencies/ReentrancyGuard.sol

2: pragma solidity 0.8.17;

```

```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

2: pragma solidity 0.8.17;

```

```solidity
File: packages/contracts/contracts/EBTCToken.sol

3: pragma solidity 0.8.17;

```

```solidity
File: packages/contracts/contracts/Governor.sol

2: pragma solidity 0.8.17;

```

```solidity
File: packages/contracts/contracts/HintHelpers.sol

3: pragma solidity 0.8.17;

```

```solidity
File: packages/contracts/contracts/Interfaces/IActivePool.sol

3: pragma solidity 0.8.17;

```

```solidity
File: packages/contracts/contracts/Interfaces/IBorrowerOperations.sol

3: pragma solidity 0.8.17;

```

```solidity
File: packages/contracts/contracts/Interfaces/ICdpManager.sol

3: pragma solidity 0.8.17;

```

```solidity
File: packages/contracts/contracts/Interfaces/ICdpManagerData.sol

3: pragma solidity 0.8.17;

```

```solidity
File: packages/contracts/contracts/Interfaces/ICollSurplusPool.sol

3: pragma solidity 0.8.17;

```

```solidity
File: packages/contracts/contracts/Interfaces/IEBTCToken.sol

3: pragma solidity 0.8.17;

```

```solidity
File: packages/contracts/contracts/Interfaces/IERC3156FlashBorrower.sol

3: pragma solidity 0.8.17;

```

```solidity
File: packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol

3: pragma solidity 0.8.17;

```

```solidity
File: packages/contracts/contracts/Interfaces/IEbtcBase.sol

3: pragma solidity 0.8.17;

```

```solidity
File: packages/contracts/contracts/Interfaces/IFallbackCaller.sol

3: pragma solidity 0.8.17;

```

```solidity
File: packages/contracts/contracts/Interfaces/IPermitNonce.sol

3: pragma solidity 0.8.17;

```

```solidity
File: packages/contracts/contracts/Interfaces/IPool.sol

3: pragma solidity 0.8.17;

```

```solidity
File: packages/contracts/contracts/Interfaces/IPositionManagers.sol

3: pragma solidity 0.8.17;

```

```solidity
File: packages/contracts/contracts/Interfaces/IPriceFeed.sol

3: pragma solidity 0.8.17;

```

```solidity
File: packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol

2: pragma solidity 0.8.17;

```

```solidity
File: packages/contracts/contracts/Interfaces/ISortedCdps.sol

3: pragma solidity 0.8.17;

```

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

2: pragma solidity 0.8.17;

```

```solidity
File: packages/contracts/contracts/LeverageMacroDelegateTarget.sol

2: pragma solidity 0.8.17;

```

```solidity
File: packages/contracts/contracts/LeverageMacroFactory.sol

2: pragma solidity 0.8.17;

```

```solidity
File: packages/contracts/contracts/LeverageMacroReference.sol

2: pragma solidity 0.8.17;

```

```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

3: pragma solidity 0.8.17;

```

```solidity
File: packages/contracts/contracts/PriceFeed.sol

3: pragma solidity 0.8.17;

```

```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

2: pragma solidity 0.8.17;

```

```solidity
File: packages/contracts/contracts/SortedCdps.sol

3: pragma solidity 0.8.17;

```
[[3]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L3)
,[[3]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L3)
,[[3]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L3)
,[[3]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L3)
,[[3]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L3)
,[[2]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L2)
,[[2]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L2)
,[[3]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L3)
,[[3]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L3)
,[[3]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L3)
,[[2]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ReentrancyGuard.sol#L2)
,[[2]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L2)
,[[3]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L3)
,[[2]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L2)
,[[3]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L3)
,[[3]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IActivePool.sol#L3)
,[[3]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L3)
,[[3]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol#L3)
,[[3]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L3)
,[[3]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICollSurplusPool.sol#L3)
,[[3]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IEBTCToken.sol#L3)
,[[3]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IERC3156FlashBorrower.sol#L3)
,[[3]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol#L3)
,[[3]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IEbtcBase.sol#L3)
,[[3]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IFallbackCaller.sol#L3)
,[[3]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPermitNonce.sol#L3)
,[[3]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPool.sol#L3)
,[[3]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPositionManagers.sol#L3)
,[[3]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPriceFeed.sol#L3)
,[[2]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol#L2)
,[[3]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L3)
,[[2]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L2)
,[[2]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L2)
,[[2]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L2)
,[[2]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L2)
,[[3]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L3)
,[[3]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L3)
,[[2]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L2)
,[[3]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L3)
,
</details>


 ### <a name="GAS-12"></a>[GAS-12] `abi.encode` is more efficient than `abi.encodePacked`
`abi.encode` uses less gas than `abi.encodePacked`: the gas saved depends on the number of arguments, with an average of ~90 per argument. Test available here.


Instances of this issue:

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

718:             abi.encodePacked(

```

```solidity
File: packages/contracts/contracts/EBTCToken.sol

210:             abi.encodePacked(

```

```solidity
File: packages/contracts/contracts/HintHelpers.sol

182:             latestRandomSeed = uint256(keccak256(abi.encodePacked(latestRandomSeed)));

```
[[718]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L718)
,[[210]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L210)
,[[182]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L182)
,
 ### <a name="GAS-13"></a>[GAS-13] Use assembly to check for `address(0)`
*Saves 6 gas per instance*

<details>
<summary>There are 29 instances of this issue:</summary>

---

```solidity
File: packages/contracts/contracts/ActivePool.sol

61:         if (_authorityAddress != address(0)) {

394:             _feeRecipientAddress != address(0),

```

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

124:         if (_authorityAddress != address(0)) {

735:             recoveredAddress != address(0) && recoveredAddress == _borrower,

1142:             _feeRecipientAddress != address(0),

```

```solidity
File: packages/contracts/contracts/CdpManager.sol

369:             while (currentBorrower != address(0) && getSyncedICR(_cId, totals.price) < MCR) {

389:             currentBorrower != address(0) && totals.remainingDebtToRedeem > 0 && _maxIterations > 0

497:         while (_cnt > 0 && _id != bytes32(0)) {

```

```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

55:         if (_authorityAddress != address(0)) {

```

```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

38:             (address(auth) != address(0) && auth.canCall(user, address(this), functionSig)) ||

```

```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

35:         return (address(auth) != address(0) && auth.canCall(user, address(this), functionSig));

56:         require(address(_authority) == address(0), "Auth: authority is non-zero");

```

```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

75:             return bytes32(0) != getUserRoles[user] & getRolesWithCapability[target][functionSig];

158:             if (getUserRoles[user] == bytes32(0)) {

```

```solidity
File: packages/contracts/contracts/EBTCToken.sol

247:         require(sender != address(0), "EBTCToken: zero sender!");

248:         require(recipient != address(0), "EBTCToken: zero recipient!");

263:         require(account != address(0), "EBTCToken: mint to zero recipient!");

271:         require(account != address(0), "EBTCToken: burn from zero account!");

286:         require(owner != address(0), "EBTCToken: zero approve owner!");

287:         require(spender != address(0), "EBTCToken: zero approve spender!");

297:             _recipient != address(0) && _recipient != address(this),

```

```solidity
File: packages/contracts/contracts/HintHelpers.sol

69:                 vars.currentCdpUser != address(0) &&

85:                 vars.currentCdpUser != address(0) &&

```

```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

756:             if (vars.cdpId != bytes32(0) && Cdps[vars.cdpId].status == Status.active) {

819:             if (vars.cdpId != bytes32(0) && Cdps[vars.cdpId].status == Status.active) {

```

```solidity
File: packages/contracts/contracts/PriceFeed.sol

224:             if (address(fallbackCaller) == address(0)) {

363:         if (_fallbackCaller != address(0)) {

587:         if (address(fallbackCaller) != address(0)) {

```

```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

187:         require(facet != address(0), "Diamond: Function does not exist");

```
[[61]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L61)
,[[394]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L394)
,[[124]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L124)
,[[735]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L735)
,[[1142]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1142)
,[[369]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L369)
,[[389]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L389)
,[[497]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L497)
,[[55]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L55)
,[[38]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L38)
,[[35]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L35)
,[[56]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L56)
,[[75]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L75)
,[[158]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L158)
,[[247]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L247)
,[[248]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L248)
,[[263]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L263)
,[[271]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L271)
,[[286]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L286)
,[[287]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L287)
,[[297]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L297)
,[[69]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L69)
,[[85]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L85)
,[[756]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L756)
,[[819]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L819)
,[[224]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L224)
,[[363]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L363)
,[[587]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L587)
,[[187]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L187)
,
</details>


 ### <a name="GAS-14"></a>[GAS-14] With assembly, .call (bool success) transfer can be done gas-optimized
When using assembly language, it is possible to call the transfer function of an Ethereum contract in a gas-optimized way by using the .call function with specific input parameters. The .call function takes a number of input parameters, including the address of the contract to call, the amount of Ether to transfer, and a specification of the gas limit for the call. By specifying a lower gas limit than the default, it is possible to reduce the gas cost of the transfer.


Instances of this issue:

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

419:             swapData.calldataForSwap

```

```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

60:         s.callbackHandler[sig] = handler;

130:         ds.settings.callbackEnabledForCall = _enabled;

179:             require(ds.settings.callbackEnabledForCall, "Only Enabled Callbacks");

186:         address facet = ds.callbackHandler[msg.sig];

```
[[419]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L419)
,[[60]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L60)
,[[130]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L130)
,[[179]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L179)
,[[186]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L186)
,
 ### <a name="GAS-15"></a>[GAS-15] Use assembly to emit events
We can use assembly to emit events efficiently by utilizing `scratch space` and the `free memory pointer`. This will allow us to potentially avoid memory expansion costs. Note: In order to do this optimization safely, we will need to cache and restore the free memory pointer.

<details>
<summary>There are 88 instances of this issue:</summary>

---

```solidity
File: packages/contracts/contracts/ActivePool.sol

65:         emit FeeRecipientAddressChanged(_feeRecipientAddress);

112:         emit SystemCollSharesUpdated(cachedSystemCollShares);

113:         emit CollSharesTransferred(_account, _shares);

145:         emit SystemCollSharesUpdated(cachedSystemCollShares);

146:         emit CollSharesTransferred(_account, totalShares);

173:         emit SystemCollSharesUpdated(cachedSystemCollShares);

174:         emit FeeRecipientClaimableCollSharesIncreased(cachedFeeRecipientCollShares, _shares);

200:         emit ActivePoolEBTCDebtUpdated(cachedSystemDebt);

213:         emit ActivePoolEBTCDebtUpdated(cachedSystemDebt);

247:         emit SystemCollSharesUpdated(cachedSystemCollShares);

307:         emit FlashLoanSuccess(address(receiver), token, amount, fee);

360:         emit FeeRecipientClaimableCollSharesDecreased(cachedFeeRecipientCollShares, _shares);

383:         emit SweepTokenSuccess(token, amount, cachedFeeRecipientAddress);

399:         emit FeeRecipientAddressChanged(_feeRecipientAddress);

412:         emit FlashFeeSet(msg.sender, _oldFee, _newFee);

421:         emit FlashLoansPaused(msg.sender, _paused);

```

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

136:         emit FeeRecipientAddressChanged(_feeRecipientAddress);

641:         emit PositionManagerApprovalSet(_borrower, _positionManager, _approval);

1105:         emit FlashLoanSuccess(address(receiver), token, amount, fee);

1149:         emit FeeRecipientAddressChanged(_feeRecipientAddress);

1162:         emit FlashFeeSet(msg.sender, _oldFee, _newFee);

1171:         emit FlashLoansPaused(msg.sender, _paused);

```

```solidity
File: packages/contracts/contracts/CdpManager.sol

55:         emit StakingRewardSplitSet(stakingRewardSplit);

179:                 emit CdpUpdated(

220:             emit CdpUpdated(

466:         emit Redemption(

545:         emit CdpUpdated(_cdpId, _borrower, msg.sender, _debt, _coll, 0, 0, 0, CdpOperation.closeCdp);

630:         emit BaseRateUpdated(newBaseRate);

681:         emit BaseRateUpdated(decayedBaseRate);

698:             emit LastRedemptionTimestampUpdated(block.timestamp);

782:         emit StakingRewardSplitSet(_stakingRewardSplit);

801:         emit RedemptionFeeFloorSet(_redemptionFeeFloor);

824:         emit MinuteDecayFactorSet(_minuteDecayFactor);

836:         emit BetaSet(_beta);

848:         emit RedemptionsPaused(_paused);

925:         emit CdpUpdated(

961:         emit CdpUpdated(

```

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

50:         emit TCRNotified(_tcr);

55:             emit GracePeriodStart();

64:         emit TCRNotified(_tcr);

69:             emit GracePeriodEnd();

119:         emit GracePeriodDurationSet(_gracePeriod);

300:         emit SystemSnapshotsUpdated(_totalStakesSnapshot, _totalCollateralSnapshot);

340:         emit CdpDebtRedistributionIndexUpdated(_cdpId, _systemDebtRedistributionIndex);

390:             emit CdpUpdated(

414:         emit TotalStakesUpdated(_newTotalStakes);

425:         emit TotalStakesUpdated(_newTotalStakes);

481:         emit CdpArrayIndexUpdated(idToMove, index);

542:             emit StEthIndexUpdated(_oldIndex, _newIndex, block.timestamp);

587:         emit CollateralFeePerUnitUpdated(_oldPerUnit, _newPerUnit, _feeTaken);

602:         emit CdpFeeSplitApplied(

```

```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

83:         emit SurplusCollSharesUpdated(_account, newAmount);

95:         emit SurplusCollSharesUpdated(_account, 0);

104:         emit CollSharesTransferred(_account, claimableColl);

150:         emit SweepTokenSuccess(token, amount, feeRecipientAddress);

```

```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

22:         emit OwnershipTransferred(msg.sender, _owner);

23:         emit AuthorityUpdated(msg.sender, _authority);

49:         emit AuthorityUpdated(msg.sender, newAuthority);

55:         emit OwnershipTransferred(msg.sender, newOwner);

```

```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

50:         emit AuthorityUpdated(msg.sender, Authority(newAuthority));

62:         emit AuthorityUpdated(address(this), Authority(newAuthority));

```

```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

101:         emit PublicCapabilityUpdated(target, functionSig, enabled);

129:         emit RoleCapabilityUpdated(role, target, functionSig, enabled);

140:         emit CapabilityBurned(target, functionSig);

163:         emit UserRoleUpdated(user, role, enabled);

```

```solidity
File: packages/contracts/contracts/EBTCToken.sol

259:         emit Transfer(sender, recipient, amount);

267:         emit Transfer(address(0), account, amount);

282:         emit Transfer(account, address(0), amount);

290:         emit Approval(owner, spender, amount);

```

```solidity
File: packages/contracts/contracts/Governor.sol

157:         emit RoleNameSet(role, roleName);

```

```solidity
File: packages/contracts/contracts/LeverageMacroFactory.sol

56:         emit DeployNewMacro(_owner, addy);

```

```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

238:         emit CdpUpdated(

281:         emit CdpLiquidated(

312:         emit CdpUpdated(

367:         emit CdpLiquidated(

437:             emit CdpPartiallyLiquidated(

490:         emit CdpUpdated(

516:         emit Liquidation(totalDebtToBurn, totalCollSharesToSend, totalLiquidatorRewardCollShares);

891:         emit SystemDebtRedistributionIndexUpdated(systemDebtRedistributionIndex);

```

```solidity
File: packages/contracts/contracts/PriceFeed.sol

67:         emit FallbackCallerChanged(address(0), _fallbackCallerAddress);

378:                     emit FallbackCallerChanged(oldFallbackCaller, _fallbackCaller);

381:                 emit UnhealthyFallbackCaller(_fallbackCaller, block.timestamp);

387:             emit FallbackCallerChanged(oldFallbackCaller, _fallbackCaller);

548:         emit PriceFeedStatusChanged(_status);

555:         emit LastGoodPriceUpdated(_currentPrice);

```

```solidity
File: packages/contracts/contracts/SortedCdps.sol

405:         emit NodeAdded(_id, _NICR);

451:             emit NodeRemoved(_ids[i]);

490:         emit NodeRemoved(_id);

```
[[65]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L65)
,[[136]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L136)
,[[55]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L55)
,[[50]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L50)
,[[55]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L55)
,[[83]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L83)
,[[22]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L22)
,[[50]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L50)
,[[259]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L259)
,[[157]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L157)
,[[56]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L56)
,[[891]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L891)
,[[67]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L67)
,[[405]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L405)
,
</details>


 ### <a name="GAS-16"></a>[GAS-16] `array[index] += amount` is cheaper than `array[index] = array[index] + amount` (or related variants)
When updating a value in an array with arithmetic, using `array[index] += amount` is cheaper than `array[index] = array[index] + amount`.
This is because you avoid an additonal `mload` when the array is stored in memory, and an `sload` when the array is stored in storage.
This can be applied for any arithmetic operation including `+=`, `-=`,`/=`,`*=`,`^=`,`&=`, `%=`, `<<=`,`>>=`, and `>>>=`.
This optimization can be particularly significant if the pattern occurs during a loop.

*Saves 28 gas for a storage array, 38 for a memory array*


Instances of this issue:

```solidity
File: packages/contracts/contracts/EBTCToken.sol

258:         _balances[recipient] = _balances[recipient] + amount;

266:         _balances[account] = _balances[account] + amount;

```
[[258]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L258)
,[[266]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L266)
,
 ### <a name="GAS-17"></a>[GAS-17] Redundant event fields can be removed
Some parameters (block.timestamp and block.number) are added to event information by default so re-adding them wastes gas, as they are already included.


Instances of this issue:

```solidity
File: packages/contracts/contracts/CdpManager.sol

698:             emit LastRedemptionTimestampUpdated(block.timestamp);

```

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

542:             emit StEthIndexUpdated(_oldIndex, _newIndex, block.timestamp);

```

```solidity
File: packages/contracts/contracts/PriceFeed.sol

381:                 emit UnhealthyFallbackCaller(_fallbackCaller, block.timestamp);

```
[[698]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L698)
,[[542]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L542)
,[[381]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L381)

 ### <a name="GAS-19"></a>[GAS-19] <array>.length should not be looked up in every loop of a for-loop
If not cached, the solidity compiler will always read the length of the array during each iteration. That is, if it is a storage array, this is an extra sload operation (100 additional extra gas for each iteration except for the first) and if it is a memory array, this is an extra mload operation (3 additional gas for each iteration except for the first).


Instances of this issue:

```solidity
File: packages/contracts/contracts/Governor.sol

46:         for (uint256 i = 0; i < users.length(); i++) {

57:             for (uint256 i = 0; i < _usrs.length; i++) {

122:         for (uint8 i = 0; i < roleIds.length; i++) {

137:             for (uint256 i = 0; i < _sigs.length; ++i) {

```

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

292:         uint256 beforeSwapsLength = operation.swapsBefore.length;

```
[[46]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L46)
,[[57]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L57)
,[[122]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L122)
,[[137]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L137)
,[[292]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L292)

 ### <a name="GAS-20"></a>[GAS-20] State variables should be cached in stack variables rather than re-reading them from storage
The instances below point to the second+ access of a state variable within a function. Caching of a state variable replaces each Gwarmaccess (100 gas) with a much cheaper stack read. Other less obvious fixes/optimizations include having local memory caches of state variable structs, or having local caches of state variable contracts/addresses.

*Saves 100 gas per instance*


Instances of this issue:

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

1103:         ebtcToken.burn(feeRecipientAddress, amount);

```

```solidity
File: packages/contracts/contracts/PriceFeed.sol

384:             address oldFallbackCaller = address(fallbackCaller);

```
[[1103]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1103)
,[[384]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L384)

 ### <a name="GAS-21"></a>[GAS-21] Use calldata instead of memory for function arguments that do not get mutated
Mark data types as `calldata` instead of `memory` where possible. This makes it so that the data is not automatically loaded into memory. If the data passed into the function does not need to be changed (like updating values in an array), it can be passed in as `calldata`. The one exception to this is if the argument must later be passed into another function that takes an argument that specifies `memory` storage.


Instances of this issue:

```solidity
File: packages/contracts/contracts/CdpManager.sol

126:     function batchLiquidateCdps(bytes32[] memory _cdpArray) external override {

```

```solidity
File: packages/contracts/contracts/Governor.sol

120:     function getByteMapFromRoles(uint8[] memory roleIds) public pure returns (bytes32) {

154:     function setRoleName(uint8 role, string memory roleName) external requiresAuth {

```

```solidity
File: packages/contracts/contracts/Interfaces/ISortedCdps.sol

16:     function batchRemove(bytes32[] memory _ids) external;

```

```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

679:     function batchLiquidateCdps(bytes32[] memory _cdpArray) external nonReentrantSelfAndBOps {

```

```solidity
File: packages/contracts/contracts/SortedCdps.sol

419:     function batchRemove(bytes32[] memory _ids) external override {

```
[[126]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L126)
,[[120]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L120)
,[[154]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L154)
,[[16]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L16)
,[[679]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L679)
,[[419]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L419)




 ### <a name="GAS-23"></a>[GAS-23] Don't compare boolean expressions to boolean literals
true and false are constants and it is more expensive comparing a boolean against them than directly checking the returned boolean value. `if (<x> == true)` => `if (<x>)`, `if (<x> == false)` => `if (!<x>)`


Instances of this issue:

```solidity
File: packages/contracts/contracts/CdpManager.sol

332:         require(redemptionsPaused == false, "CdpManager: Redemptions Paused");

```
[[332]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L332)
,
 ### <a name="GAS-24"></a>[GAS-24] Use Custom Errors
[Source](https://blog.soliditylang.org/2021/04/21/custom-errors/)
Instead of using error strings, to reduce deployment and runtime cost, you should use Custom Errors. This would save both deployment and runtime cost.

<details>
<summary>There are 87 instances of this issue:</summary>

---

```solidity
File: packages/contracts/contracts/ActivePool.sol

104:         require(cachedSystemCollShares >= _shares, "!ActivePoolBal");

137:         require(cachedSystemCollShares >= _shares, "ActivePool: Insufficient collateral shares");

162:         require(cachedSystemCollShares >= _shares, "ActivePool: Insufficient collateral shares");

236:         require(msg.sender == cdpManagerAddress, "ActivePool: Caller is not CdpManager");

267:         require(amount > 0, "ActivePool: 0 Amount");

269:         require(amount <= maxFlashLoan(token), "ActivePool: Too much");

318:         require(token == address(collateral), "ActivePool: collateral Only");

319:         require(!flashLoansPaused, "ActivePool: Flash Loans Paused");

374:         require(token != address(collateral), "ActivePool: Cannot Sweep Collateral");

377:         require(amount <= balance, "ActivePool: Attempt to sweep more than balance");

407:         require(_newFee <= MAX_FEE_BPS, "ERC3156FlashLender: _newFee should <= MAX_FEE_BPS");

```

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

145:         require(locked == OPEN, "BorrowerOperations: Reentrancy in nonReentrant call");

463:         require(vars.netStEthBalance > 0, "BorrowerOperations: zero collateral for openCdp()!");

715:         require(_deadline >= block.timestamp, "BorrowerOperations: Position manager permit expired");

826:         require(status == 1, "BorrowerOperations: Cdp does not exist or is closed");

831:         require(status == 0, "BorrowerOperations: Cdp is active or has been previously closed");

835:         require(_debtChange > 0, "BorrowerOperations: Debt increase requires non-zero debtChange");

918:         require(_newICR >= CCR, "BorrowerOperations: Operation must leave cdp with ICR >= CCR");

936:         require(_debt > 0, "BorrowerOperations: Debt must be non-zero");

1083:         require(amount > 0, "BorrowerOperations: 0 Amount");

1085:         require(amount <= maxFlashLoan(token), "BorrowerOperations: Too much");

1115:         require(token == address(ebtcToken), "BorrowerOperations: EBTC Only");

1116:         require(!flashLoansPaused, "BorrowerOperations: Flash Loans Paused");

1155:         require(_newFee <= MAX_FEE_BPS, "ERC3156FlashLender: _newFee should <= MAX_FEE_BPS");

```

```solidity
File: packages/contracts/contracts/CdpManager.sol

332:         require(redemptionsPaused == false, "CdpManager: Redemptions Paused");

431:         require(totals.collSharesDrawn > 0, "CdpManager: Unable to redeem any amount");

502:         require(_toRemoveIds[0] == _start, "CdpManager: batchRemoveSortedCdpIds check start error");

626:         require(newBaseRate > 0, "CdpManager: new baseRate is zero!"); // Base rate is always non-zero after redemption

672:         require(redemptionFee < _ETHDrawn, "CdpManager: Fee would eat up all returned collateral");

678:         require(decayedBaseRate <= DECIMAL_PRECISION, "CdpManager: baseRate too large!"); // The baseRate can decay to 0

754:         require(_amount > 0, "CdpManager: Amount must be greater than zero");

758:         require(_TCR >= MCR, "CdpManager: Cannot redeem when TCR < MCR");

```

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

242:         require(locked == OPEN, "CdpManager: Reentrancy in nonReentrant call");

453:             require(totalStakesSnapshot > 0, "CdpManagerStorage: zero totalStakesSnapshot!");

475:         require(index <= idxLast, "CdpManagerStorage: CDP indexing overflow!");

556:         require(_newIndex > _prevIndex, "CDPManager: only take fee with bigger new index");

584:         require(activePool.getSystemCollShares() > _feeTaken, "CDPManager: fee split is too big");

649:         require(Cdps[_cdpId].status == Status.active, "CdpManager: Cdp does not exist or is closed");

```

```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

92:         require(claimableColl > 0, "CollSurplusPool: No collateral available to claim");

99:         require(cachedTotalSurplusCollShares >= claimableColl, "!CollSurplusPoolBal");

120:         require(msg.sender == cdpManagerAddress, "CollSurplusPool: Caller is not CdpManager");

124:         require(msg.sender == activePoolAddress, "CollSurplusPool: Caller is not Active Pool");

143:         require(token != address(collateral), "CollSurplusPool: Cannot Sweep Collateral");

146:         require(amount <= balance, "CollSurplusPool: Attempt to sweep more than balance");

```

```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

27:         require(isAuthorized(msg.sender, msg.sig), "Auth: UNAUTHORIZED");

```

```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

17:         require(isAuthorized(msg.sender, msg.sig), "Auth: UNAUTHORIZED");

56:         require(address(_authority) == address(0), "Auth: authority is non-zero");

57:         require(!_authorityInitialized, "Auth: authority already initialized");

```

```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

109:         require(feePercentage <= _maxFeePercentage, "Fee exceeded provided maximum");

```

```solidity
File: packages/contracts/contracts/Dependencies/ReentrancyGuard.sol

14:         require(locked == OPEN, "ReentrancyGuard: Reentrancy in nonReentrant call");

```

```solidity
File: packages/contracts/contracts/EBTCToken.sol

144:             require(cachedAllowance >= amount, "ERC20: transfer amount exceeds allowance");

165:         require(cachedAllowances >= subtractedValue, "ERC20: decreased allowance below zero");

208:         require(deadline >= block.timestamp, "EBTC: expired deadline");

219:         require(recoveredAddress == owner, "EBTC: invalid signature");

247:         require(sender != address(0), "EBTCToken: zero sender!");

248:         require(recipient != address(0), "EBTCToken: zero recipient!");

251:         require(cachedSenderBalances >= amount, "ERC20: transfer amount exceeds balance");

263:         require(account != address(0), "EBTCToken: mint to zero recipient!");

271:         require(account != address(0), "EBTCToken: burn from zero account!");

274:         require(cachedBalance >= amount, "ERC20: burn amount exceeds balance");

286:         require(owner != address(0), "EBTCToken: zero approve owner!");

287:         require(spender != address(0), "EBTCToken: zero approve spender!");

324:         require(msg.sender == cdpManagerAddress, "EBTC: Caller is not CdpManager");

```

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

40:         revert("Must be overridden");

45:         require(owner() == msg.sender, "Must be owner");

249:             require(check.value >= valueToCheck, "!LeverageMacroReference: gte post check");

251:             require(check.value <= valueToCheck, "!LeverageMacroReference: let post check");

253:             require(check.value == valueToCheck, "!LeverageMacroReference: equal post check");

255:             revert("Operator not found");

352:         require(initiator == address(this), "LeverageMacroReference: wrong initiator for flashloan");

421:         require(success, "Call has failed");

```

```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

56:         require(_partialAmount != 0, "LiquidationLibrary: use `liquidate` for 100%");

710:         require(totals.totalDebtInSequence > 0, "LiquidationLibrary: nothing to liquidate");

```

```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

111:         require(msg.sender == owner, "Must be owner");

179:             require(ds.settings.callbackEnabledForCall, "Only Enabled Callbacks");

187:         require(facet != address(0), "Diamond: Function does not exist");

```

```solidity
File: packages/contracts/contracts/SortedCdps.sol

352:         require(cdpManager.getCdpStatus(_id) == 0, "SortedCdps: new id is NOT nonExistent!");

365:         require(!isFull(), "SortedCdps: List is full");

367:         require(!contains(_id), "SortedCdps: List already contains the node");

369:         require(_id != dummyId, "SortedCdps: Id cannot be zero");

371:         require(_NICR > 0, "SortedCdps: NICR must be positive");

422:         require(_len > 1, "SortedCdps: batchRemove() only apply to multiple cdpIds!");

433:             require(contains(_ids[i]), "SortedCdps: List does not contain the id");

458:         require(contains(_id), "SortedCdps: List does not contain the id");

506:         require(contains(_id), "SortedCdps: List does not contain the id");

508:         require(_newNICR > 0, "SortedCdps: NICR must be positive");

715:         require(msg.sender == address(cdpManager), "SortedCdps: Caller is not the CdpManager");

```
[[104]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L104)
,[[145]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L145)
,[[332]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L332)
,[[242]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L242)
,[[92]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L92)
,[[27]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L27)
,[[17]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L17)
,[[109]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L109)
,[[14]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ReentrancyGuard.sol#L14)
,[[144]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L144)
,[[40]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L40)
,[[56]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L56)
,[[111]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L111)
</details>


 ### <a name="GAS-25"></a>[GAS-25] Multiplication/division by two should use bit shifting
X * 2 is equivalent to X << 1 and X / 2 is the same as X >> 1.
 The MUL and DIV opcodes cost 5 gas, whereas SHL and SHR only cost 3 gas.


Instances of this issue:

```solidity
File: packages/contracts/contracts/Dependencies/EbtcMath.sol

38:         decProd = (prod_xy + (DECIMAL_PRECISION / 2)) / DECIMAL_PRECISION;

76:                 n = n / 2;

81:                 n = (n - 1) / 2;

```

```solidity
File: packages/contracts/contracts/PriceFeed.sol

804:                 EbtcMath.DECIMAL_PRECISION) / 10 ** (_decimalDenominator * 2);

```

```solidity
File: packages/contracts/contracts/SortedCdps.sol

61:     uint256 constant BLOCK_SHIFT = 64; // 8 * 8; Puts the block value after the address

```
[[38]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L38)
,[[76]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L76)
,[[81]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L81)
,[[804]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L804)
,[[61]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L61)
,
 ### <a name="GAS-26"></a>[GAS-26] Use of emit inside a loop
Emitting an event inside a loop performs a LOG op N times, where N is the loop length. Consider refactoring the code to emit the event only once at the end of loop. Gas savings should be multiplied by the average loop length.


Instances of this issue:

```solidity
File: packages/contracts/contracts/SortedCdps.sol

449:         for (uint i = 0; i < _len; ++i) {

```
[[449]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L449)
,
 ### <a name="GAS-27"></a>[GAS-27] >=/ <= costs less gas than >/<
The compiler uses opcodes GT and ISZERO for solidity code that uses >, but only requires LT for >=,which saves 3 gas

<details>
<summary>There are 126 instances of this issue:</summary>

---

```solidity
File: packages/contracts/contracts/ActivePool.sol

104:         require(cachedSystemCollShares >= _shares, "!ActivePoolBal");

137:         require(cachedSystemCollShares >= _shares, "ActivePool: Insufficient collateral shares");

162:         require(cachedSystemCollShares >= _shares, "ActivePool: Insufficient collateral shares");

267:         require(amount > 0, "ActivePool: 0 Amount");

351:             cachedFeeRecipientCollShares >= _shares,

```

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

393:         if (!_isDebtIncrease && _debtChange > 0) {

463:         require(vars.netStEthBalance > 0, "BorrowerOperations: zero collateral for openCdp()!");

475:             In recovery move, ICR must be greater than CCR

479:             Additionally, the new system TCR after the Cdps addition must be >CCR

715:         require(_deadline >= block.timestamp, "BorrowerOperations: Position manager permit expired");

835:         require(_debtChange > 0, "BorrowerOperations: Debt increase requires non-zero debtChange");

912:             _newICR >= MCR,

918:         require(_newICR >= CCR, "BorrowerOperations: Operation must leave cdp with ICR >= CCR");

918:         require(_newICR >= CCR, "BorrowerOperations: Operation must leave cdp with ICR >= CCR");

923:             _newICR >= _oldICR,

930:             _newTCR >= CCR,

936:         require(_debt > 0, "BorrowerOperations: Debt must be non-zero");

941:             _stEthBalance >= MIN_NET_STETH_BALANCE,

1083:         require(amount > 0, "BorrowerOperations: 0 Amount");

```

```solidity
File: packages/contracts/contracts/CdpManager.sol

389:             currentBorrower != address(0) && totals.remainingDebtToRedeem > 0 && _maxIterations > 0

389:             currentBorrower != address(0) && totals.remainingDebtToRedeem > 0 && _maxIterations > 0

431:         require(totals.collSharesDrawn > 0, "CdpManager: Unable to redeem any amount");

436:         } else if (_numCdpsFullyRedeemed > 1) {

497:         while (_cnt > 0 && _id != bytes32(0)) {

626:         require(newBaseRate > 0, "CdpManager: new baseRate is zero!"); // Base rate is always non-zero after redemption

690:         uint256 timePassed = block.timestamp > lastRedemptionTimestamp

694:         if (timePassed >= SECONDS_IN_ONE_MINUTE) {

711:             block.timestamp > lastRedemptionTimestamp

744:             callerBalance >= _amount,

754:         require(_amount > 0, "CdpManager: Amount must be greater than zero");

758:         require(_TCR >= MCR, "CdpManager: Cannot redeem when TCR < MCR");

763:             _maxFeePercentage >= redemptionFeeFloor && _maxFeePercentage <= DECIMAL_PRECISION,

790:             _redemptionFeeFloor >= MIN_REDEMPTION_FEE_FLOOR,

809:             _minuteDecayFactor >= MIN_MINUTE_DECAY_FACTOR,

```

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

113:             _gracePeriod >= MINIMUM_GRACE_PERIOD,

315:         if (_debtIndexDiff > 0) {

362:         if (_feeSplitDistributed > 0 || _debtIndexDelta > 0) {

362:         if (_feeSplitDistributed > 0 || _debtIndexDelta > 0) {

369:             if (_feeSplitDistributed > 0) {

380:             if (_debtIndexDelta > 0) {

453:             require(totalStakesSnapshot > 0, "CdpManagerStorage: zero totalStakesSnapshot!");

512:         if (_newIndex > _oldIndex && totalStakes > 0) {

512:         if (_newIndex > _oldIndex && totalStakes > 0) {

556:         require(_newIndex > _prevIndex, "CDPManager: only take fee with bigger new index");

636:         if (_scaledCdpColl > _feeSplitDistributed) {

654:             CdpOwnersArrayLength > 1 && sortedCdps.getSize() > 1,

765:         if (_newIndex > _oldIndex && totalStakes > 0) {

765:         if (_newIndex > _oldIndex && totalStakes > 0) {

796:         if (_cdpPerUnitIdx != _systemStEthFeePerUnitIndex && _cdpPerUnitIdx > 0) {

829:         if (pendingDebtRedistributed > 0) {

879:         if (_feeTaken > 0) {

900:             block.timestamp > cachedLastGracePeriodStartTimestamp + recoveryModeGracePeriodDuration;

```

```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

92:         require(claimableColl > 0, "CollSurplusPool: No collateral available to claim");

99:         require(cachedTotalSurplusCollShares >= claimableColl, "!CollSurplusPoolBal");

```

```solidity
File: packages/contracts/contracts/Dependencies/EbtcMath.sol

25:         return (_a >= _b) ? _a : _b;

60:         if (_minutes > 525600000) {

73:         while (n > 1) {

89:         return (_a >= _b) ? (_a - _b) : (_b - _a);

93:         if (_debt > 0) {

109:         if (_debt > 0) {

```

```solidity
File: packages/contracts/contracts/EBTCToken.sol

144:             require(cachedAllowance >= amount, "ERC20: transfer amount exceeds allowance");

165:         require(cachedAllowances >= subtractedValue, "ERC20: decreased allowance below zero");

208:         require(deadline >= block.timestamp, "EBTC: expired deadline");

251:         require(cachedSenderBalances >= amount, "ERC20: transfer amount exceeds balance");

274:         require(cachedBalance >= amount, "ERC20: burn amount exceeds balance");

```

```solidity
File: packages/contracts/contracts/Governor.sol

53:         if (count > 0) {

81:         if (count > 0) {

99:             bool roleEnabled = (uint256(byteMap >> i) & 1) != 0;

104:         if (count > 0) {

108:                 bool roleEnabled = (uint256(byteMap >> i) & 1) != 0;

135:         if (_sigs.length > 0) {

```

```solidity
File: packages/contracts/contracts/HintHelpers.sol

86:                 vars.remainingEbtcToRedeem > 0 &&

93:                 if (currentCdpDebt > vars.remainingEbtcToRedeem) {

```

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

128:         if (operation.amountToTransferIn > 0) {

223:         if (ebtcBal > 0) {

227:         if (collateralBal > 0) {

249:             require(check.value >= valueToCheck, "!LeverageMacroReference: gte post check");

293:         if (beforeSwapsLength > 0) {

307:         if (afterSwapsLength > 0) {

```

```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

80:         if (_ICR >= MCR) {

94:                 block.timestamp >

195:             if (_outputState.totalSurplusCollShares > 0) {

261:             if (_collSurplus > 0) {

266:             if (_debtToRedistribute > 0) {

289:             _cappedColl > _debtToColl ? (_cappedColl - _debtToColl) : 0

336:             if (_collSurplus > 0) {

342:             if (_debtToRedistribute > 0) {

358:         _recoveryState.entireSystemDebt = _recoveryState.entireSystemDebt > _totalDebtToBurn

361:         _recoveryState.entireSystemColl = _recoveryState.entireSystemColl > _totalColToSend

375:             _cappedColl > _debtToColl ? (_cappedColl - _debtToColl) : 0

444:                 _cappedColl > _debtToColl ? (_cappedColl - _debtToColl) : 0

476:         if (_partialState.ICR > LICR) {

479:                 "LiquidationLibrary: !_newICR>=_ICR"

525:         if (totalDebtToRedistribute > 0) {

553:         if (_ICR > LICR) {

555:             _incentiveColl = (_totalDebtToBurn * (_ICR > MCR ? MCR : _ICR)) / _price;

578:         if (_ICR > LICR) {

579:             _incentiveColl = (_totalDebtToBurn * (_ICR > MCR ? MCR : _ICR)) / _price;

710:         require(totals.totalDebtInSequence > 0, "LiquidationLibrary: nothing to liquidate");

713:         if (totals.totalCollSurplus > 0) {

910:             _entireColl >= MIN_NET_STETH_BALANCE,

911:             "LiquidationLibrary: Coll remaining in partially liquidated CDP must be >= minimum"

```

```solidity
File: packages/contracts/contracts/PriceFeed.sol

421:             _response.timestampEthBtc > block.timestamp ||

423:             _response.timestampStEthEth > block.timestamp

457:         uint256 percentDeviation = maxPrice > 0

462:         return percentDeviation > MAX_PRICE_DEVIATION_FROM_PREVIOUS_ROUND;

471:         if (_response.timestamp == 0 || _response.timestamp > block.timestamp) {

489:             _fallbackResponse.timestamp > 0 &&

494:         return block.timestamp - _timestamp > _timeout;

794:         uint256 _decimalDenominator = _stEthEthDecimals > _ethBtcDecimals

797:         uint256 _scaledDecimal = _stEthEthDecimals > _ethBtcDecimals

```

```solidity
File: packages/contracts/contracts/SortedCdps.sol

202:             if (maxNodes > 0 && i >= maxNodes) {

202:             if (maxNodes > 0 && i >= maxNodes) {

259:             if (maxNodes > 0 && i >= maxNodes) {

259:             if (maxNodes > 0 && i >= maxNodes) {

274:         if (_ownedCount > 0) {

330:             if (maxNodes > 0 && i >= maxNodes) {

330:             if (maxNodes > 0 && i >= maxNodes) {

371:         require(_NICR > 0, "SortedCdps: NICR must be positive");

422:         require(_len > 1, "SortedCdps: batchRemove() only apply to multiple cdpIds!");

460:         if (data.size > 1) {

508:         require(_newNICR > 0, "SortedCdps: NICR must be positive");

601:             return data.head == _nextId && _NICR >= cdpManager.getCachedNominalICR(_nextId);

610:                 _NICR >= cdpManager.getCachedNominalICR(_nextId);

621:         if (data.head == _startId && _NICR >= cdpManager.getCachedNominalICR(_startId)) {

683:             if (!contains(prevId) || _NICR > cdpManager.getCachedNominalICR(prevId)) {

```
[[104]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L104)
,[[393]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L393)
,[[389]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L389)
,[[92]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L92)
,[[25]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L25)
,[[144]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L144)
,[[53]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L53)
,[[128]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L128)
,[[80]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L80)
,[[421]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L421)
,[[202]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L202)

,
</details>


 ### <a name="GAS-28"></a>[GAS-28] Use hardcode address instead of address(this) 
Instead of using address(this), it is more gas-efficient to pre-calculate and use the hardcoded address. Foundry’s script.sol and solmate’s LibRlp.sol contracts can help achieve this. References: https://book.getfoundry.sh/reference/forge-std/compute-create-address

<details>
<summary>There are 27 instances of this issue:</summary>

---

```solidity
File: packages/contracts/contracts/ActivePool.sol

283:         collateral.transferFrom(address(receiver), address(this), amountWithFee);

295:             collateral.balanceOf(address(this)) >= collateral.getPooledEthByShares(systemCollShares),

299:             collateral.sharesOf(address(this)) >= systemCollShares,

337:         return collateral.balanceOf(address(this));

376:         uint256 balance = IERC20(token).balanceOf(address(this));

```

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

682:         return keccak256(abi.encode(typeHash, name, version, _chainID(), address(this)));

```

```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

145:         uint256 balance = IERC20(token).balanceOf(address(this));

```

```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

38:             (address(auth) != address(0) && auth.canCall(user, address(this), functionSig)) ||

45:         require(msg.sender == owner || authority.canCall(msg.sender, address(this), msg.sig));

```

```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

35:         return (address(auth) != address(0) && auth.canCall(user, address(this), functionSig));

41:         require(_authority.canCall(msg.sender, address(this), msg.sig));

62:         emit AuthorityUpdated(address(this), Authority(newAuthority));

```

```solidity
File: packages/contracts/contracts/EBTCToken.sol

240:         return keccak256(abi.encode(typeHash, name, version, _chainID(), address(this)));

297:             _recipient != address(0) && _recipient != address(this),

```

```solidity
File: packages/contracts/contracts/Governor.sol

36:     constructor(address _owner) RolesAuthority(_owner, Authority(address(this))) {}

```

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

131:                 address(this),

143:             initialCdpIndex = sortedCdps.cdpCountOf(address(this));

149:                 IERC3156FlashBorrower(address(this)),

156:                 IERC3156FlashBorrower(address(this)),

173:             bytes32 cdpId = sortedCdps.cdpOfOwnerByIndex(address(this), initialCdpIndex);

220:         uint256 ebtcBal = ebtcToken.balanceOf(address(this));

221:         uint256 collateralBal = stETH.sharesOf(address(this));

352:         require(initiator == address(this), "LeverageMacroReference: wrong initiator for flashloan");

441:                     IERC20(swapChecks[i].tokenToCheck).balanceOf(address(this)) >

456:         require(addy != address(this)); // If it could call this it could fake the forwarded caller

```

```solidity
File: packages/contracts/contracts/LeverageMacroDelegateTarget.sol

64:         address _owner = IOwnerLike(address(this)).owner();

```

```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

77:         require(msg.sender == address(this)); // Must call this via `execute` to explicitly set the flag

```
[[283]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L283)
,[[682]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L682)
,[[145]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L145)
,[[38]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L38)
,[[35]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L35)
,[[240]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L240)
,[[36]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L36)
,[[131]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L131)
,[[64]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L64)
,[[77]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L77)
,
</details>


 ### <a name="GAS-29"></a>[GAS-29] Don't initialize variables with default value

<details>
<summary>There are 19 instances of this issue:</summary>

---

```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

35:     uint256 public constant BORROWING_FEE_FLOOR = 0; // 0.5%

```

```solidity
File: packages/contracts/contracts/Governor.sol

46:         for (uint256 i = 0; i < users.length(); i++) {

54:             uint256 j = 0;

57:             for (uint256 i = 0; i < _usrs.length; i++) {

76:         for (uint8 i = 0; i < type(uint8).max; i++) {

82:             uint256 j = 0;

84:             for (uint8 i = 0; i < type(uint8).max; i++) {

98:         for (uint8 i = 0; i < type(uint8).max; i++) {

105:             uint256 j = 0;

107:             for (uint8 i = 0; i < type(uint8).max; i++) {

122:         for (uint8 i = 0; i < roleIds.length; i++) {

137:             for (uint256 i = 0; i < _sigs.length; ++i) {

```

```solidity
File: packages/contracts/contracts/HintHelpers.sol

105:                         partialRedemptionHintNICR = 0; //reset to 0 as there is no partial redemption in this case

```

```solidity
File: packages/contracts/contracts/SortedCdps.sol

182:         uint _currentIndex = 0;

245:         uint _ownedCount = 0;

246:         uint i = 0;

311:         uint i = 0;

432:         for (uint256 i = 0; i < _len; ++i) {

449:         for (uint i = 0; i < _len; ++i) {

```
[[35]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L35)
,[[46]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L46)
,[[105]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L105)
</details>


 ### <a name="GAS-30"></a>[GAS-30] Long revert strings

<details>
<summary>There are 55 instances of this issue:</summary>

---

```solidity
File: packages/contracts/contracts/ActivePool.sol

137:         require(cachedSystemCollShares >= _shares, "ActivePool: Insufficient collateral shares");

162:         require(cachedSystemCollShares >= _shares, "ActivePool: Insufficient collateral shares");

236:         require(msg.sender == cdpManagerAddress, "ActivePool: Caller is not CdpManager");

374:         require(token != address(collateral), "ActivePool: Cannot Sweep Collateral");

377:         require(amount <= balance, "ActivePool: Attempt to sweep more than balance");

407:         require(_newFee <= MAX_FEE_BPS, "ERC3156FlashLender: _newFee should <= MAX_FEE_BPS");

```

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

145:         require(locked == OPEN, "BorrowerOperations: Reentrancy in nonReentrant call");

463:         require(vars.netStEthBalance > 0, "BorrowerOperations: zero collateral for openCdp()!");

715:         require(_deadline >= block.timestamp, "BorrowerOperations: Position manager permit expired");

826:         require(status == 1, "BorrowerOperations: Cdp does not exist or is closed");

831:         require(status == 0, "BorrowerOperations: Cdp is active or has been previously closed");

835:         require(_debtChange > 0, "BorrowerOperations: Debt increase requires non-zero debtChange");

918:         require(_newICR >= CCR, "BorrowerOperations: Operation must leave cdp with ICR >= CCR");

936:         require(_debt > 0, "BorrowerOperations: Debt must be non-zero");

1116:         require(!flashLoansPaused, "BorrowerOperations: Flash Loans Paused");

1155:         require(_newFee <= MAX_FEE_BPS, "ERC3156FlashLender: _newFee should <= MAX_FEE_BPS");

```

```solidity
File: packages/contracts/contracts/CdpManager.sol

431:         require(totals.collSharesDrawn > 0, "CdpManager: Unable to redeem any amount");

502:         require(_toRemoveIds[0] == _start, "CdpManager: batchRemoveSortedCdpIds check start error");

626:         require(newBaseRate > 0, "CdpManager: new baseRate is zero!"); // Base rate is always non-zero after redemption

672:         require(redemptionFee < _ETHDrawn, "CdpManager: Fee would eat up all returned collateral");

754:         require(_amount > 0, "CdpManager: Amount must be greater than zero");

758:         require(_TCR >= MCR, "CdpManager: Cannot redeem when TCR < MCR");

```

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

242:         require(locked == OPEN, "CdpManager: Reentrancy in nonReentrant call");

453:             require(totalStakesSnapshot > 0, "CdpManagerStorage: zero totalStakesSnapshot!");

475:         require(index <= idxLast, "CdpManagerStorage: CDP indexing overflow!");

556:         require(_newIndex > _prevIndex, "CDPManager: only take fee with bigger new index");

649:         require(Cdps[_cdpId].status == Status.active, "CdpManager: Cdp does not exist or is closed");

```

```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

92:         require(claimableColl > 0, "CollSurplusPool: No collateral available to claim");

120:         require(msg.sender == cdpManagerAddress, "CollSurplusPool: Caller is not CdpManager");

124:         require(msg.sender == activePoolAddress, "CollSurplusPool: Caller is not Active Pool");

143:         require(token != address(collateral), "CollSurplusPool: Cannot Sweep Collateral");

146:         require(amount <= balance, "CollSurplusPool: Attempt to sweep more than balance");

```

```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

57:         require(!_authorityInitialized, "Auth: authority already initialized");

```

```solidity
File: packages/contracts/contracts/Dependencies/ReentrancyGuard.sol

14:         require(locked == OPEN, "ReentrancyGuard: Reentrancy in nonReentrant call");

```

```solidity
File: packages/contracts/contracts/EBTCToken.sol

144:             require(cachedAllowance >= amount, "ERC20: transfer amount exceeds allowance");

165:         require(cachedAllowances >= subtractedValue, "ERC20: decreased allowance below zero");

251:         require(cachedSenderBalances >= amount, "ERC20: transfer amount exceeds balance");

263:         require(account != address(0), "EBTCToken: mint to zero recipient!");

271:         require(account != address(0), "EBTCToken: burn from zero account!");

274:         require(cachedBalance >= amount, "ERC20: burn amount exceeds balance");

```

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

249:             require(check.value >= valueToCheck, "!LeverageMacroReference: gte post check");

251:             require(check.value <= valueToCheck, "!LeverageMacroReference: let post check");

253:             require(check.value == valueToCheck, "!LeverageMacroReference: equal post check");

352:         require(initiator == address(this), "LeverageMacroReference: wrong initiator for flashloan");

```

```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

56:         require(_partialAmount != 0, "LiquidationLibrary: use `liquidate` for 100%");

710:         require(totals.totalDebtInSequence > 0, "LiquidationLibrary: nothing to liquidate");

```

```solidity
File: packages/contracts/contracts/SortedCdps.sol

352:         require(cdpManager.getCdpStatus(_id) == 0, "SortedCdps: new id is NOT nonExistent!");

367:         require(!contains(_id), "SortedCdps: List already contains the node");

371:         require(_NICR > 0, "SortedCdps: NICR must be positive");

422:         require(_len > 1, "SortedCdps: batchRemove() only apply to multiple cdpIds!");

433:             require(contains(_ids[i]), "SortedCdps: List does not contain the id");

458:         require(contains(_id), "SortedCdps: List does not contain the id");

506:         require(contains(_id), "SortedCdps: List does not contain the id");

508:         require(_newNICR > 0, "SortedCdps: NICR must be positive");

715:         require(msg.sender == address(cdpManager), "SortedCdps: Caller is not the CdpManager");

```
,[[407]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L407)
,[[145]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L145)
,[[431]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L431)
,[[242]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L242)
,[[92]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L92)
,[[57]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L57)
,[[14]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ReentrancyGuard.sol#L14)
,[[144]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L144)
,[[249]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L249)
,[[56]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L56)
,[[352]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L352)
</details>


 ### <a name="GAS-31"></a>[GAS-31] Constructors can be marked payable
 Payable functions cost less gas to execute, since the compiler does not have to add extra checks to ensure that a payment was not provided. A constructor can safely be marked as payable, since only the deployer would be able to pass funds, and the project itself would not pass any funds.

<details>
<summary>There are 19 instances of this issue:</summary>

---

```solidity
File: packages/contracts/contracts/ActivePool.sol

46:     constructor(

```

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

107:     constructor(

```

```solidity
File: packages/contracts/contracts/CdpManager.sol

30:     constructor(

```

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

217:     constructor(

```

```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

42:     constructor(

```

```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

18:     constructor(address _owner, Authority _authority) {

```

```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

52:     constructor(address _activePoolAddress, address _priceFeedAddress, address _collateralAddress) {

```

```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

20:     constructor(address _owner, Authority _authority) Auth(_owner, _authority) {}

```

```solidity
File: packages/contracts/contracts/EBTCToken.sol

61:     constructor(

```

```solidity
File: packages/contracts/contracts/Governor.sol

36:     constructor(address _owner) RolesAuthority(_owner, Authority(address(this))) {}

```

```solidity
File: packages/contracts/contracts/HintHelpers.sol

27:     constructor(

```

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

51:     constructor(

```

```solidity
File: packages/contracts/contracts/LeverageMacroDelegateTarget.sol

41:     constructor(

```

```solidity
File: packages/contracts/contracts/LeverageMacroFactory.sol

21:     constructor(

```

```solidity
File: packages/contracts/contracts/LeverageMacroReference.sol

17:     constructor(

```

```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

14:     constructor(

```

```solidity
File: packages/contracts/contracts/PriceFeed.sol

57:     constructor(

```

```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

44:     constructor(address _owner) {

```

```solidity
File: packages/contracts/contracts/SortedCdps.sol

88:     constructor(uint256 _size, address _cdpManagerAddress, address _borrowerOperationsAddress) {

```
[[46]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L46)
,[[107]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L107)
,[[30]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L30)
,[[217]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L217)
,[[42]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L42)
,[[18]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L18)
,[[52]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L52)
,[[20]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L20)
,[[61]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L61)
,[[36]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L36)
,[[27]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L27)
,[[51]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L51)
,[[41]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L41)
,[[21]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L21)
,[[17]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L17)
,[[14]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L14)
,[[57]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L57)
,[[44]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L44)
,[[88]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L88)
,
</details>


 ### <a name="GAS-32"></a>[GAS-32] `++i` costs less gas than `i++`, especially when it's used in `for`-loops (`--i`/`i--` too)
*Saves 5 gas per loop*

<details>
<summary>There are 13 instances of this issue:</summary>

---

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

727:                         _nonces[_borrower]++,

```

```solidity
File: packages/contracts/contracts/EBTCToken.sol

214:                     abi.encode(_PERMIT_TYPEHASH, owner, spender, amount, _nonces[owner]++, deadline)

```

```solidity
File: packages/contracts/contracts/Governor.sol

46:         for (uint256 i = 0; i < users.length(); i++) {

57:             for (uint256 i = 0; i < _usrs.length; i++) {

62:                     j++;

76:         for (uint8 i = 0; i < type(uint8).max; i++) {

84:             for (uint8 i = 0; i < type(uint8).max; i++) {

87:                     j++;

98:         for (uint8 i = 0; i < type(uint8).max; i++) {

107:             for (uint8 i = 0; i < type(uint8).max; i++) {

111:                     j++;

122:         for (uint8 i = 0; i < roleIds.length; i++) {

```

```solidity
File: packages/contracts/contracts/HintHelpers.sol

195:             i++;

```
[[727]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L727)
,[[214]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L214)
,[[46]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L46)
,[[57]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L57)
,[[62]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L62)
,[[76]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L76)
,[[84]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L84)
,[[87]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L87)
,[[98]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L98)
,[[107]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L107)
,[[111]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L111)
,[[122]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L122)
,[[195]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L195)

</details>


 ### <a name="GAS-33"></a>[GAS-33] Using `private` rather than `public` for constants, saves gas
If needed, the values can be read from the verified contract source code, or if there are multiple values there can be a single getter function that [returns a tuple](https://github.com/code-423n4/2022-08-frax/blob/90f55a9ce4e25bceed3a74290b854341d8de6afa/src/contracts/FraxlendPair.sol#L156-L178) of the values of all currently-public constants. Saves **3406-3606 gas** in deployment gas due to the compiler not having to create non-payable getter functions for deployment calldata, not having to store the bytes of the value outside of where it's used, and not adding another entry to the method ID table

<details>
<summary>There are 31 instances of this issue:</summary>

---

```solidity
File: packages/contracts/contracts/ActivePool.sol

24:     string public constant NAME = "ActivePool";

```

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

29:     string public constant NAME = "BorrowerOperations";

```

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

21:     uint128 public constant UNSET_TIMESTAMP = type(uint128).max;

22:     uint128 public constant MINIMUM_GRACE_PERIOD = 15 minutes;

122:     string public constant NAME = "CdpManager";

139:     uint256 public constant SECONDS_IN_ONE_MINUTE = 60;

141:     uint256 public constant MIN_REDEMPTION_FEE_FLOOR = (DECIMAL_PRECISION * 5) / 1000; // 0.5%

149:     uint256 public constant MIN_MINUTE_DECAY_FACTOR = 1; // Non-zero

150:     uint256 public constant MAX_MINUTE_DECAY_FACTOR = 999999999999999999; // Corresponds to a very fast decay rate, but not too extreme

```

```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

19:     string public constant NAME = "CollSurplusPool";

```

```solidity
File: packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol

9:     uint256 public constant MAX_BPS = 10_000;

10:     uint256 public constant MAX_FEE_BPS = 1_000; // 10%

11:     bytes32 public constant FLASH_SUCCESS_VALUE = keccak256("ERC3156FlashBorrower.onFlashLoan");

```

```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

19:     uint256 public constant LICR = 1030000000000000000; // 103%

22:     uint256 public constant MCR = 1100000000000000000; // 110%

25:     uint256 public constant CCR = 1250000000000000000; // 125%

28:     uint256 public constant LIQUIDATOR_REWARD = 2e17;

31:     uint256 public constant MIN_NET_STETH_BALANCE = 2e18;

33:     uint256 public constant PERCENT_DIVISOR = 200; // dividing by 200 yields 0.5%

35:     uint256 public constant BORROWING_FEE_FLOOR = 0; // 0.5%

37:     uint256 public constant STAKING_REWARD_SPLIT = 5_000; // taking 50% cut from staking reward

39:     uint256 public constant MAX_REWARD_SPLIT = 10_000;

```

```solidity
File: packages/contracts/contracts/Dependencies/EbtcMath.sol

7:     uint256 public constant MAX_TCR = type(uint256).max;

```

```solidity
File: packages/contracts/contracts/HintHelpers.sol

12:     string public constant NAME = "HintHelpers";

```

```solidity
File: packages/contracts/contracts/PriceFeed.sol

22:     string public constant NAME = "PriceFeed";

32:     uint256 public constant TIMEOUT_ETH_BTC_FEED = 4800; // 1 hours & 20min: 60 * 80

33:     uint256 public constant TIMEOUT_STETH_ETH_FEED = 90000; // 25 hours: 60 * 60 * 25

36:     uint256 public constant MAX_PRICE_DEVIATION_FROM_PREVIOUS_ROUND = 5e17; // 50%

42:     uint256 public constant MAX_PRICE_DIFFERENCE_BETWEEN_ORACLES = 5e16; // 5%

```

```solidity
File: packages/contracts/contracts/SortedCdps.sol

52:     string public constant NAME = "SortedCdps";

80:     bytes32 public constant dummyId =

```
[[24]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L24)
,[[29]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L29)
,[[21]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L21)
,[[19]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L19)
,[[9]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L9)
,[[19]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L19)
,[[12]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L12)
,[[22]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L22)
,[[52]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L52)

</details>


 ### <a name="GAS-34"></a>[GAS-34] Use shift Right/Left instead of division/multiplication if possible


Instances of this issue:

```solidity
File: packages/contracts/contracts/Dependencies/EbtcMath.sol

37: 

75:                 x = decMul(x, x);

80:                 x = decMul(x, x);

```
[[37]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L37)
,[[75]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L75)
,[[80]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L80)

 ### <a name="GAS-35"></a>[GAS-35] Usage of smaller uint/int types causes overhead
When using a smaller int/uint type it first needs to be converted to it's 258 bit counterpart to be operated, this increases the gass cost and thus should be avoided. However it does make sense to use smaller int/uint values within structs provided you pack the struct properly.

<details>
<summary>There are 43 instances of this issue:</summary>

---

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

34:             "PermitPositionManagerApproval(address borrower,address positionManager,uint8 status,uint256 nonce,uint256 deadline)"

711:         uint8 v,

```

```solidity
File: packages/contracts/contracts/CdpManager.sol

550:     function _addCdpIdToArray(bytes32 _cdpId) internal returns (uint128 index) {

```

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

21:     uint128 public constant UNSET_TIMESTAMP = type(uint128).max;

22:     uint128 public constant MINIMUM_GRACE_PERIOD = 15 minutes;

24:     uint128 public lastGracePeriodStartTimestamp = UNSET_TIMESTAMP; // use max to signify

25:     uint128 public recoveryModeGracePeriodDuration = MINIMUM_GRACE_PERIOD;

111:     function setGracePeriod(uint128 _gracePeriod) external requiresAuth {

471:         uint128 index = Cdps[_cdpId].arrayIndex;

897:         uint128 cachedLastGracePeriodStartTimestamp = lastGracePeriodStartTimestamp;

```

```solidity
File: packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol

14:     uint16 public feeBps = 3; // may be subject to future adjustments through protocol governance

```

```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

38:     function doesUserHaveRole(address user, uint8 role) public view virtual returns (bool) {

43:         uint8 role,

107:         uint8 role,

147:     function setUserRole(address user, uint8 role, bool enabled) public virtual requiresAuth {

```

```solidity
File: packages/contracts/contracts/EBTCToken.sol

31:     uint8 internal constant _DECIMALS = 18;

204:         uint8 v,

```

```solidity
File: packages/contracts/contracts/Governor.sol

20:         uint8 roleId;

32:     event RoleNameSet(uint8 indexed role, string indexed name);

43:     function getUsersByRole(uint8 role) external view returns (address[] memory usersWithRole) {

76:         for (uint8 i = 0; i < type(uint8).max; i++) {

84:             for (uint8 i = 0; i < type(uint8).max; i++) {

98:         for (uint8 i = 0; i < type(uint8).max; i++) {

107:             for (uint8 i = 0; i < type(uint8).max; i++) {

122:         for (uint8 i = 0; i < roleIds.length; i++) {

146:     function getRoleName(uint8 role) external view returns (string memory roleName) {

154:     function setRoleName(uint8 role, string memory roleName) external requiresAuth {

```

```solidity
File: packages/contracts/contracts/Interfaces/ICdpManagerData.sol

103:         uint128 arrayIndex;

```

```solidity
File: packages/contracts/contracts/Interfaces/IPositionManagers.sol

37:         uint8 v,

```

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

502:         uint16 _maxCopy,

```

```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

88:             uint128 cachedLastGracePeriodStartTimestamp = lastGracePeriodStartTimestamp;

```

```solidity
File: packages/contracts/contracts/PriceFeed.sol

612:         uint8 ethBtcDecimals;

613:         uint8 stEthEthDecimals;

615:         try ETH_BTC_CL_FEED.decimals() returns (uint8 decimals) {

623:         try STETH_ETH_CL_FEED.decimals() returns (uint8 decimals) {

700:         uint8 ethBtcDecimals;

701:         uint8 stEthEthDecimals;

703:         try ETH_BTC_CL_FEED.decimals() returns (uint8 decimals) {

711:         try STETH_ETH_CL_FEED.decimals() returns (uint8 decimals) {

791:         uint8 _ethBtcDecimals,

792:         uint8 _stEthEthDecimals

```

```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

102:         uint128 value; // How much ETH to send

103:         uint128 gas; // How much gas to send

```
[[34]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L34)
,[[550]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L550)
,[[21]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L21)
,[[14]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L14)
,[[38]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L38)
,[[31]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L31)
,[[204]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L204)
,[[20]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L20)
,[[103]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L103)
,[[37]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPositionManagers.sol#L37)
,[[502]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L502)
,[[88]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L88)
,[[612]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L612)
,[[103]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L103)
</details>


 ### <a name="GAS-36"></a>[GAS-36] `++i/i++` should be `unchecked{++i}/unchecked{i++}` when it is not possible for them to overflow, as is the case when used in forand whileloops
The unchecked keyword is new in solidity version 0.8.0, so this only applies to that version or higher, which these instances are. This saves 30-40 gas per loop

<details>
<summary>There are 13 instances of this issue:</summary>

---

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

727:                         _nonces[_borrower]++,

```

```solidity
File: packages/contracts/contracts/EBTCToken.sol

214:                     abi.encode(_PERMIT_TYPEHASH, owner, spender, amount, _nonces[owner]++, deadline)

```

```solidity
File: packages/contracts/contracts/Governor.sol

46:         for (uint256 i = 0; i < users.length(); i++) {

57:             for (uint256 i = 0; i < _usrs.length; i++) {

62:                     j++;

76:         for (uint8 i = 0; i < type(uint8).max; i++) {

84:             for (uint8 i = 0; i < type(uint8).max; i++) {

87:                     j++;

98:         for (uint8 i = 0; i < type(uint8).max; i++) {

107:             for (uint8 i = 0; i < type(uint8).max; i++) {

111:                     j++;

122:         for (uint8 i = 0; i < roleIds.length; i++) {

```

```solidity
File: packages/contracts/contracts/HintHelpers.sol

195:             i++;

```
[[727]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L727)
,[[214]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L214)
,[[46]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L46)
,[[57]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L57)
,[[62]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L62)
,[[76]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L76)
,[[84]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L84)
,[[87]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L87)
,[[98]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L98)
,[[107]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L107)
,[[111]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L111)
,[[122]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L122)
,[[195]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L195)
,
</details>


 ### <a name="GAS-37"></a>[GAS-37] Use != 0 instead of > 0 for unsigned integer comparison

<details>
<summary>There are 53 instances of this issue:</summary>

---

```solidity
File: packages/contracts/contracts/ActivePool.sol

267:         require(amount > 0, "ActivePool: 0 Amount");

```

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

393:         if (!_isDebtIncrease && _debtChange > 0) {

463:         require(vars.netStEthBalance > 0, "BorrowerOperations: zero collateral for openCdp()!");

835:         require(_debtChange > 0, "BorrowerOperations: Debt increase requires non-zero debtChange");

936:         require(_debt > 0, "BorrowerOperations: Debt must be non-zero");

1083:         require(amount > 0, "BorrowerOperations: 0 Amount");

```

```solidity
File: packages/contracts/contracts/CdpManager.sol

389:             currentBorrower != address(0) && totals.remainingDebtToRedeem > 0 && _maxIterations > 0

389:             currentBorrower != address(0) && totals.remainingDebtToRedeem > 0 && _maxIterations > 0

431:         require(totals.collSharesDrawn > 0, "CdpManager: Unable to redeem any amount");

497:         while (_cnt > 0 && _id != bytes32(0)) {

626:         require(newBaseRate > 0, "CdpManager: new baseRate is zero!"); // Base rate is always non-zero after redemption

754:         require(_amount > 0, "CdpManager: Amount must be greater than zero");

```

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

315:         if (_debtIndexDiff > 0) {

362:         if (_feeSplitDistributed > 0 || _debtIndexDelta > 0) {

362:         if (_feeSplitDistributed > 0 || _debtIndexDelta > 0) {

369:             if (_feeSplitDistributed > 0) {

380:             if (_debtIndexDelta > 0) {

453:             require(totalStakesSnapshot > 0, "CdpManagerStorage: zero totalStakesSnapshot!");

512:         if (_newIndex > _oldIndex && totalStakes > 0) {

765:         if (_newIndex > _oldIndex && totalStakes > 0) {

796:         if (_cdpPerUnitIdx != _systemStEthFeePerUnitIndex && _cdpPerUnitIdx > 0) {

829:         if (pendingDebtRedistributed > 0) {

879:         if (_feeTaken > 0) {

```

```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

92:         require(claimableColl > 0, "CollSurplusPool: No collateral available to claim");

```

```solidity
File: packages/contracts/contracts/Dependencies/EbtcMath.sol

93:         if (_debt > 0) {

109:         if (_debt > 0) {

```

```solidity
File: packages/contracts/contracts/Governor.sol

53:         if (count > 0) {

81:         if (count > 0) {

104:         if (count > 0) {

135:         if (_sigs.length > 0) {

```

```solidity
File: packages/contracts/contracts/HintHelpers.sol

86:                 vars.remainingEbtcToRedeem > 0 &&

87:                 _maxIterations-- > 0

```

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

128:         if (operation.amountToTransferIn > 0) {

223:         if (ebtcBal > 0) {

227:         if (collateralBal > 0) {

293:         if (beforeSwapsLength > 0) {

307:         if (afterSwapsLength > 0) {

```

```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

195:             if (_outputState.totalSurplusCollShares > 0) {

261:             if (_collSurplus > 0) {

266:             if (_debtToRedistribute > 0) {

336:             if (_collSurplus > 0) {

342:             if (_debtToRedistribute > 0) {

525:         if (totalDebtToRedistribute > 0) {

710:         require(totals.totalDebtInSequence > 0, "LiquidationLibrary: nothing to liquidate");

713:         if (totals.totalCollSurplus > 0) {

```

```solidity
File: packages/contracts/contracts/PriceFeed.sol

457:         uint256 percentDeviation = maxPrice > 0

489:             _fallbackResponse.timestamp > 0 &&

```

```solidity
File: packages/contracts/contracts/SortedCdps.sol

202:             if (maxNodes > 0 && i >= maxNodes) {

259:             if (maxNodes > 0 && i >= maxNodes) {

274:         if (_ownedCount > 0) {

330:             if (maxNodes > 0 && i >= maxNodes) {

371:         require(_NICR > 0, "SortedCdps: NICR must be positive");

508:         require(_newNICR > 0, "SortedCdps: NICR must be positive");

```
[[267]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L267)
,[[393]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L393)
,[[389]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L389)
,[[389]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L389)
,[[315]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L315)
,[[92]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L92)
,[[93]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L93)
,[[53]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L53)
,[[86]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L86)
,[[87]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L87)
,[[128]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L128)
,[[195]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L195)
,[[457]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L457)
,[[202]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L202)

</details>


 ### <a name="GAS-38"></a>[GAS-38] `internal` functions not called by the contract should be removed
If the functions are required by an interface, the contract should inherit from that interface and use the `override` keyword

<details>
<summary>There are 8 instances of this issue:</summary>

---

```solidity
File: packages/contracts/contracts/Dependencies/EbtcMath.sol

20:     function _min(uint256 _a, uint256 _b) internal pure returns (uint256) {

24:     function _max(uint256 _a, uint256 _b) internal pure returns (uint256) {

59:     function _decPow(uint256 _base, uint256 _minutes) internal pure returns (uint256) {

88:     function _getAbsoluteDifference(uint256 _a, uint256 _b) internal pure returns (uint256) {

92:     function _computeNominalCR(uint256 _collShares, uint256 _debt) internal pure returns (uint256) {

104:     function _computeCR(

```

```solidity
File: packages/contracts/contracts/EBTCToken.sol

306:     function _requireCallerIsBorrowerOperations() internal view {

323:     function _requireCallerIsCdpM() internal view {

```
[[20]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L20)
,[[24]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L24)
,[[59]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L59)
,[[88]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L88)
,[[92]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L92)
,[[104]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L104)
,[[306]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L306)
,[[323]](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L323)

</details>

