## Summary

### Gas Optimization

no | Issue |Instances||
|-|:-|:-:|:-:|
| [G-01] | Avoid contract existence checks by using low level calls | 13 - more than | - |
| [G-02] | Internal functions only called once can be inlined to save gas | 6 | - |
| [G-03] | keccak256() should only need to be called on a specific string literal once | 1 | - |
| [G-04] | Optimize Names to save Gas | 5 | - |
| [G-05] | USE A MORE RECENT VERSION OF SOLIDITY | All files - 39 | - |
| [G-06] | Using PRIVATE rather than PUBLIC FOR Constants/Immutable, Saves Gas | 6 | - |
| [G-07] | Require()/Revert() string longer than 32 bytes cost extra gas | 10 | - |
| [G-08] | SPLITTING  REQUIRE() STATEMENTS THAT USE  && SAVES GAS | 4 | - |
| [G-09] | Setting the constructor to payable | 4 | - |
| [G-10] | Before transfer of  some functions, we should check some variables for possible gas save | 2 | - |
| [G-11] | Require() or revert() statements that check input arguments should be at the top of the function | 7 | - |
| [G-12] | Bytes constants are more efficient than String constants | 6 | - |
| [G-13] | Don't compare boolean expressions to boolean literals | 1 | - |
| [G-14] | State varaibles only set in the Constructor should be declared Immutable | 2 | - |
| [G-15] | Using storage instead of memory for structs/arrays saves gas | 5 | - |
| [G-16] | Duplicated require()/if() checks should be refactored to a modifier or function  | 1 | - |
| [G-17] | Use constants instead of type(uintx).max | 5 | - |
| [G-18] | A modifier used only once and not being inherited should be inlined to save gas | 3 | - |
| [G-19] | abi.encode() is less efficient than  abi.encodepacked() | 1 | - |
| [G-20] | Do not calculate constant | 1 | - |
| [G-21] | Structs can be packed into fewer storage slots by editing time variables | 1 | - |
| [G-22] | require() Should Be Used Instead Of assert() | 1 | - |
| [G-23] | Use assembly to emit events | 4 | - |
| [G-24] | Use hardcode address instead address(this) | 4 | - |
| [G-25] | Use assembly for math (add, sub, mul, div) | 3 | - |
| [G-26] | Use assembly to calculate hashes to save gas | 5 | - |
| [G-27] | State variable read in a loop | 3 | - |
| [G-28] | Shorten the array rather than copying to a new one | 2 | - |
| [G-29] | bytes.concat() can be used in place of abi.encodePacked | 2 | - |
| [G-30] | Use of emit inside a loop | 1 | - |
| [G-31] | Using assembly to check for zero can save gas | 3 | - |
| [G-32] | Use assembly to validate msg.sender | 3 | - |
| [G-33] | Pre-increment and pre-decrement are cheaper than +1 ,-1 | 3 | - |
| [G-34] | Consider Using Solady's Gas Optimized Lib for Math | 34 | - |


## Gas Optimizations  

## [G-01] Avoid contract existence checks by using low level calls		

Prior to 0.8.10 the compiler inserted extra code, including EXTCODESIZE (100 gas), to check for contract existence for external function calls. In more recent solidity versions, the compiler will not insert these checks if the external call has a return value. Similar behavior can be achieved in earlier versions by using low-level calls, since low level calls never check for contract existence.							


```solidity
file: /contracts/contracts/ActivePool.sol

60        address _authorityAddress = address(AuthNoOwner(cdpManagerAddress).authority());

186            ICollSurplusPool(_account).increaseTotalSurplusCollShares(_shares);

272        uint256 oldRate = collateral.getPooledEthByShares(DECIMAL_PRECISION);

278            receiver.onFlashLoan(msg.sender, token, amount, fee, data) == FLASH_SUCCESS_VALUE,

303            collateral.getPooledEthByShares(DECIMAL_PRECISION) == oldRate,

337        return collateral.balanceOf(address(this));

391        ICdpManagerData(cdpManagerAddress).syncGlobalAccountingAndGracePeriod(); // Accrue State First

418        ICdpManagerData(cdpManagerAddress).syncGlobalAccountingAndGracePeriod(); // Accrue State First

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L60


```solidity
file: /contracts/contracts/BorrowerOperations.sol

364        vars.collShares = cdpManager.getCdpCollShares(_cdpId);

367        uint256 _cdpStEthBalance = collateral.getPooledEthByShares(vars.collShares);

372        vars.oldICR = EbtcMath._computeCR(_cdpStEthBalance, vars.debt, vars.price);

465        uint256 _netCollAsShares = collateral.getSharesByPooledEth(vars.netStEthBalance);

466        uint256 _liquidatorRewardShares = collateral.getSharesByPooledEth(LIQUIDATOR_REWARD);

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L364

```solidity

The contest have more low level calls .

```

## [G-02] Internal functions only called once can be inlined to save gas

Not inlining costs 20 to 40 gas because of two extra JUMP instructions and additional stack operations needed for function calls.


```solidity
file: /contracts/contracts/ActivePool.sol
 
219    function _requireCallerIsBorrowerOperations() internal view {

235    function _requireCallerIsCdpManager() internal view {    

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L219


```solidity
file: /contracts/BorrowerOperations.sol

744    function _getCollSharesChangeFromStEthChange(
        uint256 _collReceived,
        uint256 _requestedCollWithdrawal
    ) internal view returns (uint256 collSharesChange, bool isCollIncrease) {


769    function _processTokenMovesFromAdjustment(MoveTokensParams memory _varMvTokens) internal {

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L744-L747


```solidity
file: /contracts/contracts/CdpManager.sol

135    function _redeemCollateralFromCdp(
        SingleRedemptionInputs memory _redeemColFromCdp
    ) internal returns (SingleRedemptionValues memory singleRedemption) {

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L135-L137


```solidity
file: /contracts/contracts/LiquidationLibrary.sol

466    function _reInsertPartialLiquidation(
        LiquidationLocals memory _partialState,
        uint256 _newNICR,
        uint256 _oldDebt,
        uint256 _oldColl
    ) internal {

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L466-L471



## [G-03] keccak256() should only need to be called on a specific string literal once

It should be saved to an immutable variable, and the variable used instead. If the hash is being used as a part of a function selector, the cast to bytes4 should also only be done once


```solidity
file: /contracts/contracts/EBTCToken.sol
///@audit the ' _NAME ' and ' _VERSION ' are use in another file in keccak.
/@audit the file: contracts/BorrowerOperations.sol#L128-L129

71        bytes32 hashedName = keccak256(bytes(_NAME));
72        bytes32 hashedVersion = keccak256(bytes(_VERSION));

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L71-L72


## [G-04] Optimize Names to save Gas

public/external function names and public member variable names can be optimized to save gas. See this link for an example of how it works. Below are the interfaces/abstract contracts that can be optimized so that the most frequently-called functions use the least amount of gas possible during method lookup. Method IDs that have two leading zero bytes can save 128 gas each during deployment, and renaming functions to have lower method IDs will save 22 gas per call, per sorted position shifted.


```solidity
file: /contracts/contracts/ActivePool.sol

22  contract ActivePool is IActivePool, ERC3156FlashLender, ReentrancyGuard, BaseMath, AuthNoOwner {

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L22


```solidity
file: /contracts/contracts/BorrowerOperations.sol

21  contract BorrowerOperations is
    EbtcBase,
    ReentrancyGuard,
    IBorrowerOperations,
    ERC3156FlashLender,
    AuthNoOwner,
    PermitNonce
28  {

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L21-L28

```solidity
file: /contracts/contracts/CdpManagerStorage.sol

19contract CdpManagerStorage is EbtcBase, ReentrancyGuard, ICdpManagerData, AuthNoOwner {

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L19


```solidity
file: /contracts/contracts/CollSurplusPool.

16  contract CollSurplusPool is ICollSurplusPool, ReentrancyGuard, AuthNoOwner {

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L16


```solidity
file: /contracts/contracts/EBTCToken.sol

26  contract EBTCToken is IEBTCToken, AuthNoOwner, PermitNonce {

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L26 


## [G-05] USE A MORE RECENT VERSION OF SOLIDITY

Use 0.8.23 version of solidity instead of  0.8.17 , new version will be more efficeint.

```solidity
file: All files

All file of this Contest have  0.8.17 version of soldity which should be change.

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts


## [G-06] Using PRIVATE rather than PUBLIC FOR Constants/Immutable, Saves Gas        

If needed, the value can be read from the verified contract source code. Savings are due to the compiler not having to create non-payable getter functions for deployment calldata, and not adding another entry to the method ID table

```solidity
file: /contracts/contracts/CdpManagerStorage.sol

21    uint128 public constant UNSET_TIMESTAMP = type(uint128).max;

22    uint128 public constant MINIMUM_GRACE_PERIOD = 15 minutes;

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L21-L22


```solidity
file: /contracts/contracts/PriceFeed.sol

42    uint256 public constant MAX_PRICE_DIFFERENCE_BETWEEN_ORACLES = 5e16; // 5%

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L42


```solidity
file: /contracts/contracts/SortedCdps.sol

80    bytes32 public constant dummyId =
        0x0000000000000000000000000000000000000000000000000000000000000000;

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L80-L81


```solidity
file: /contracts/Dependencies/EbtcMath.sol

6    uint256 internal constant DECIMAL_PRECISION = 1e18;

7    uint256 public constant MAX_TCR = type(uint256).max;

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L6-L7


## [G-07] Require()/Revert() string longer than 32 bytes cost extra gas  

Each extra memory word of bytes past the original 32 incurs an MSTORE which costs 3 gas

when these strings get longer than 32 bytes, they cost more gas
Use shorter require()/revert() strings

```solidity
file: /contracts/contracts/ActivePool.sol

137        require(cachedSystemCollShares >= _shares, "ActivePool: Insufficient collateral shares");


162        require(cachedSystemCollShares >= _shares, "ActivePool: Insufficient collateral shares");



220        require(
            msg.sender == borrowerOperationsAddress,
            "ActivePool: Caller is not BorrowerOperations"
223        );


228        require(
            msg.sender == borrowerOperationsAddress || msg.sender == cdpManagerAddress,
            "ActivePool: Caller is neither BorrowerOperations nor CdpManager"
231        );


377        require(amount <= balance, "ActivePool: Attempt to sweep more than balance");

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L137


```solidity
file: /contracts/contracts/BorrowerOperations.sol
 
145        require(locked == OPEN, "BorrowerOperations: Reentrancy in nonReentrant call");

        require(
            ReentrancyGuard(address(cdpManager)).locked() == OPEN,
            "CdpManager: Reentrancy in nonReentrant call"
        );

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L145-L150


```solidity
file: /contracts/contracts/CdpManager.sol

743        require(
            callerBalance >= _amount,
            "CdpManager: Requested redemption amount must be <= user's EBTC token balance"
        );

        require(
            callerBalance <= _totalSupply,
            "CdpManager: redeemer's EBTC balance exceeds total supply!"
        );

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L743-L750


```solidity
file: /contracts/LiquidationLibrary.sol

909        require(
            _entireColl >= MIN_NET_STETH_BALANCE,
            "LiquidationLibrary: Coll remaining in partially liquidated CDP must be >= minimum"
        );

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L909-L912


## [G-08] SPLITTING  REQUIRE() STATEMENTS THAT USE  && SAVES GAS

Instead of using operator && on a single require. Using a two require can save more gas.


```solidity
//expensive
require(version == 1 && index == 2);

//cheaper
require(version == 1);
require(index == 2 == bytes1(0));

```
Instances:

```solidity
file: /contracts/contracts/BorrowerOperations.sol

734        require(
            recoveredAddress != address(0) && recoveredAddress == _borrower,
            "BorrowerOperations: Invalid signature"
        );

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L734-L737


```solidity
file: /contracts/contracts/CdpManager.sol

762        require(
            _maxFeePercentage >= redemptionFeeFloor && _maxFeePercentage <= DECIMAL_PRECISION,
            "Max fee percentage must be between redemption fee floor and 100%"
       

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L762-L765


```solidity
file: /contracts/contracts/EBTCToken.sol

296      require(
            _recipient != address(0) && _recipient != address(this),
            "EBTC: Cannot transfer tokens directly to the EBTC token contract or the zero address"
        );

300        require(
            _recipient != cdpManagerAddress && _recipient != borrowerOperationsAddress,
            "EBTC: Cannot transfer tokens directly to the CdpManager or BorrowerOps"
        );

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L296-L303


## [G-09] Setting the constructor to payable

You can cut out 10 opcodes in the creation-time EVM bytecode if you declare a constructor payable. Making the constructor payable eliminates the need for an initial check of msg.value == 0 and saves 13 gas on deployment with no security risks.

```solidity
file: /contracts/contracts/ActivePool.sol

46    constructor(

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L46


```solidity
file: /contracts/BorrowerOperations.sol

107    constructor(

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L107


```solidity
file: /contracts/CollSurplusPool.sol

42    constructor(

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L42


```solidity
file: /contracts/contracts/Governor.sol

36    constructor(address _owner) RolesAuthority(_owner, Authority(address(this))) {}

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L36



## [G-10] Before transfer of  some functions, we should check some variables for possible gas save

Before transfer, we should check for amount being 0 so the function doesn't run when its not gonna do anything:

```solidity
file: /contracts/BorrowerOperations.sol

785        collateral.transferFrom(msg.sender, address(activePool), _stEthBalance);

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L785


```solidity
file: /contracts/contracts/EBTCToken.so

140        _transfer(sender, recipient, amount);

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L140


## [G-11] Require() or revert() statements that check input arguments should be at the top of the function  

Checks that involve constants should come before checks that involve state variables, function calls, and calculations. By doing these checks first, the function is able to revert before wasting a Gcoldsload (2100 gas*) in a function that may ultimately revert in the unhappy case.

```solidity
file: /contracts/contracts/ActivePool.sol

294        require(
            collateral.balanceOf(address(this)) >= collateral.getPooledEthByShares(systemCollShares),
            "ActivePool: Must repay Balance"
        );

298        require(
            collateral.sharesOf(address(this)) >= systemCollShares,
            "ActivePool: Must repay Share"
        );

302        require(
            collateral.getPooledEthByShares(DECIMAL_PRECISION) == oldRate,
            "ActivePool: Should keep same collateral share rate"
        );

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L294-L305


```solidity
file: /contracts/contracts/BorrowerOperations.sol

371      require(
            _stEthBalanceDecrease <= _cdpStEthBalance,
            "BorrowerOperations: Cannot withdraw greater stEthBalance than the value in Cdp"
        );


463        require(vars.netStEthBalance > 0, "BorrowerOperations: zero collateral for openCdp()!");


541    require(
            vars.netStEthBalance + LIQUIDATOR_REWARD == _stEthBalance,
            "BorrowerOperations: deposited collateral mismatch!"
        );

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L368-L371


```solidity
file: /contracts/contracts/CdpManager.sol

431        require(totals.collSharesDrawn > 0, "CdpManager: Unable to redeem any amount");

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L431


## [G-12]  Bytes constants are more efficient than String constants

If data can fit into 32 bytes, then you should use bytes32 datatype rather than bytes or strings as it is cheaper in solidity.

```solidity
file: /contracts/contracts/ActivePool.sol

24    string public constant NAME = "ActivePool";

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L24


```solidity
file: /contracts/contracts/BorrowerOperations.sol

29    string public constant NAME = "BorrowerOperations";

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L29


```solidity
file: /contracts/contracts/EBTCToken.sol

28    string internal constant _NAME = "EBTC Stablecoin";

29    string internal constant _SYMBOL = "EBTC";

30    string internal constant _VERSION = "1";

31    uint8 internal constant _DECIMALS = 18;

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L28-L31


## [G-13] Don't compare boolean expressions to boolean literals

There is no need to verify that == true or == false when the variable checked upon is a boolean as well.

if (<x> == true) => if (<x>), if (<x> == false) => if (!<x>)

```solidity
file: /contracts/contracts/CdpManager.sol

332        require(redemptionsPaused == false, "CdpManager: Redemptions Paused");

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L332


## [G-14] State varaibles only set in the Constructor should be declared Immutable

Avoids a Gsset (20000 gas) in the constructor, and replaces the first access in each transaction (Gcoldsload - 2100 gas) and each access thereafter (Gwarmacces - 100 gas) with a PUSH32 (3 gas).

While strings are not value types, and therefore cannot be immutable/constant if not hard-coded outside of the constructor, the same behavior can be achieved by making the current contract abstract with virtual functions for the string accessors, and having a child contract override the functions with the hard-coded implementation-specific values.

```solidity
file: /contracts/contracts/ActivePool.sol

57        feeRecipientAddress = _feeRecipientAddress;

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L57


```solidity
file: /contracts/contracts/BorrowerOperations.sol

121        feeRecipientAddress = _feeRecipientAddress;

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L121


## [G-15] Using storage instead of memory for structs/arrays saves gas

When fetching data from a storage location, assigning the data to a memory variable causes all fields of the struct/array to be read from storage, which incurs a Gcoldsload (2100 gas) for each field of the struct/array. If the fields are read from the new memory variable, they incur an additional MLOAD rather than a cheap stack read. Instead of declearing the variable with the memory keyword, declaring the variable with the storage keyword and caching any fields that need to be re-read in stack variables, will be much cheaper, only incuring the Gcoldsload for the fields actually read. The only time it makes sense to read the whole struct/array into a memory variable, is if the full struct/array is being returned by the function, is being passed to a function that requires memory, or if the array/struct is being read from another memory array/struct

```solidity
file: /contracts/contracts/LiquidationLibrary.sol

751        bool[] memory _liqFlags = new bool[](_cnt);

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L751


```solidity
file: /contracts/contracts/Governor.sol

56            address[] memory _usrs = users.values();

14        bytes32[] memory _sigs = enabledFunctionSigsByTarget[_target].values();

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L56


```solidity
file: /contracts/contracts/SortedCdps.sol

275            (bytes32[] memory _allCdps, , ) = _getCdpsOf(owner, dummyId, 0, _ownedCount);

310        bytes32[] memory userCdps = new bytes32[](maxArraySize);

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L275


## [G-16] Duplicated require()/if() checks should be refactored to a modifier or function   

 to reduce code duplication and improve readability.
•  Modifiers can be used to perform additional checks on the function inputs or state before it is executed. By defining a modifier to perform a specific check, we can reuse it across multiple functions that require the same check.
• A function can also be used to perform a specific check and return a boolean value indicating whether the check has passed or failed. This can be useful when the check is more complex and cannot be performed easily in a modifier.

```solidity
file: /contracts/contracts/ActivePool.sol
 
162        require(cachedSystemCollShares >= _shares, "ActivePool: Insufficient collateral shares");

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L162



## [G-17] Use constants instead of type(uintx).max

type(uint120).max or type(uint128).max, etc. it uses more gas in the distribution process and also for each transaction than constant usage.

```solidity
file: /contracts/BorrowerOperations.sol

1133        return type(uint112).max;

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1133


```solidity
file: /contracts/contracts/CdpManager.sol

378            _maxIterations = type(uint256).max;

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L378


```solidity
file: /contracts/contracts/Governor.sol

76        for (uint8 i = 0; i < type(uint8).max; i++) {

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L76


```solidity
file: /contracts/contracts/SortedCdps.sol

90            _size = type(uint256).max;

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L90


```solidity
file: /contracts/contracts/CdpManagerStorage.sol

21    uint128 public constant UNSET_TIMESTAMP = type(uint128).max;

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L21


## [G-18] A modifier used only once and not being inherited should be inlined to save gas

```solidity
file: /contracts/contracts/BorrowerOperations.sol

144    modifier nonReentrantSelfAndCdpM() {

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L144


```solidity
file: /contracts/contracts/CdpManagerStorage.sol

241    modifier nonReentrantSelfAndBOps() {

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L241


```solidity
file: /contracts/contracts/Dependencies/Auth.sol

26    modifier requiresAuth() virtual {

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L26

## [G-19] abi.encode() is less efficient than  abi.encodepacked()

In terms of efficiency, abi.encodePacked() is generally considered to be more gas-efficient than abi.encode(), because it skips the step of adding function signatures and other metadata to the encoded data. However, this comes at the cost of reduced safety, as abi.encodePacked() does not perform any type checking or padding of data.

```solidity
file: /contracts/contracts/BorrowerOperations.sol

682        return keccak256(abi.encode(typeHash, name, version, _chainID(), address(this)));

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L682

## [G-20] Do not calculate constant

When you define a constant in Solidity, the compiler can calculate its value at compile-time and replace all references to the constant with its computed value. This can be helpful for readability and reducing the size of the compiled code, but it can also increase gas usage at runtime.

```solidity
file: /contracts/contracts/CdpManagerStorage.sol

141    uint256 public constant MIN_REDEMPTION_FEE_FLOOR = (DECIMAL_PRECISION * 5) / 1000; // 0.5%

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L141


## [G-21] Structs can be packed into fewer storage slots by editing time variables

The following structures could be optimized moving the position of certain values in order to save a lot slots:

Enums are represented by integers; the possibility listed first by 0, the next by 1, and so forth.
An enum type just acts like uintN, where N is the smallest legal value large enough to accomodate all the possibilities.

Refference: https://ethdebug.github.io/solidity-data-representation

```solidity 
file: /contracts/contracts/BorrowerOperations.sol

///@audit the ' bool isCollIncrease; ' variable should be rewrite on the botom , near to '  bool isDebtIncrease; ' variable

97    struct MoveTokensParams {
        address user;
        uint256 collSharesChange;
        uint256 collAddUnderlying; // ONLY for isCollIncrease=true
        bool isCollIncrease;
        uint256 netDebtChange;
        bool isDebtIncrease;
    }

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L97-L104


## [G-22] require() Should Be Used Instead Of assert()


```solidity
file: /contracts/contracts/LiquidationLibrary.sol

564        assert(toLiquidator < _totalColToSend); // Assert is correct here for Echidna

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L564


## [G-23] Use assembly to emit events

We can use assembly to emit events efficiently by utilizing scratch space and the free memory pointer. This will allow us to potentially avoid memory expansion costs. Note: In order to do this optimization safely, we will need to cache and restore the free memory pointer.


```solidity
file: /contracts/contracts/ActivePool.sol

65        emit FeeRecipientAddressChanged(_feeRecipientAddress);


112        emit SystemCollSharesUpdated(cachedSystemCollShares);

113        emit CollSharesTransferred(_account, _shares);

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L65


```solidity
file: /contracts/contracts/BorrowerOperations.sol

641        emit PositionManagerApprovalSet(_borrower, _positionManager, _approval);

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L641


## [G-24] Use hardcode address instead address(this)
 
 Instead of using address(this), it is more gas-efficient to pre-calculate and use the hardcoded address. Foundry’s script.sol and solmate’s LibRlp.sol contracts can help achieve this.
References: https://book.getfoundry.sh/reference/forge-std/compute-create-address

an example :
```solidity
contract MyContract {
    address constant public CONTRACT_ADDRESS = 0x1234567890123456789012345678901234567890;
    
    function getContractAddress() public view returns (address) {
        return CONTRACT_ADDRESS;
    }
}
```
Instances:

```solidity
file: /contracts/contracts/ActivePool.sol

283        collateral.transferFrom(address(receiver), address(this), amountWithFee);

295            collateral.balanceOf(address(this)) >= collateral.getPooledEthByShares(systemCollShares),

337        return collateral.balanceOf(address(this));

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L283


```solidity
file: /contracts/contracts/BorrowerOperations.sol

682        return keccak256(abi.encode(typeHash, name, version, _chainID(), address(this)));

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L682

## [G-25] Use assembly for math (add, sub, mul, div)

Use assembly for math instead of Solidity. You can check for overflow/underflow in assembly to ensure safety. If using Solidity versions < 0.8.0 and you are using Safemath, you can gain significant gas savings by using assembly to calculate values and checking for overflow/underflow.


```solidity
file: /contracts/contracts/ActivePool.sol

271        uint256 amountWithFee = amount + fee;

321        return (amount * feeBps) / MAX_BPS;

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L271

```solidity
file: /contracts/contracts/Dependencies/EbtcMath.sol

76                n = n / 2;

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L76


## [G-26] Use assembly to calculate hashes to save gas

Using assembly to calculate hashes can save 80 gas per instance


```solidity
file: /contracts/contracts/BorrowerOperations.sol

128        bytes32 hashedName = keccak256(bytes(NAME));

129        bytes32 hashedVersion = keccak256(bytes(_VERSION));

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L128-L129


```solidity
file: /contracts/contracts/EBTCToken.sol

240        return keccak256(abi.encode(typeHash, name, version, _chainID(), address(this)));

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L240


```solidty
file: /contracts/contracts/HintHelpers.sol

182            latestRandomSeed = uint256(keccak256(abi.encodePacked(latestRandomSeed)));

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L182

```solidity
file: /contracts/contracts/SimplifiedDiamondLike.sol

39    bytes32 constant DIAMOND_STORAGE_POSITION = keccak256("diamond.standard.diamond.storage");

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L39


## [G-27] State variable read in a loop

State variable reads and writes are more expensive than local variable reads and writes. Therefore, it is recommended to replace state variable reads and writes within loops with local variable reads and writes.


```solidity
file: /contracts/contracts/SortedCdps.sol
//@audit ' data ' is state var.

256            _currentCdpId = data.nodes[_currentCdpId].prevId;

630            prevId = data.nodes[prevId].nextId;

631            nextId = data.nodes[prevId].nextId;

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L256

## [G-28] Shorten the array rather than copying to a new one

Inline-assembly can be used to shorten the array by changing the length slot, so that the entries don't have to be copied to a new, shorter array

```solidity
file: /contracts/contracts/SortedCdps.sol

310        bytes32[] memory userCdps = new bytes32[](maxArraySize);

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L310


```solidity
file: /contracts/CdpManager.sol

496        bytes32[] memory _toRemoveIds = new bytes32[](_total);

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L496


## [G-29] bytes.concat() can be used in place of abi.encodePacked

Given concatenation is not going to be used for hashing bytes.concat is the preferred method to use as its more gas efficient

```solidity
file: /contracts/contracts/BorrowerOperations.sol

718            abi.encodePacked(

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L718


```solidity
file: /contracts/contracts/EBTCToken.sol

210            abi.encodePacked(

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L210


## [G-30] Use of emit inside a loop

Emitting an event inside a loop performs a Loop N times, where N is the loop length. Consider refactoring the code to emit the event only once at the end of loop. Gas savings should be multiplied by the average loop length.

```solidity
file: /contracts/contracts/SortedCdps.sol

451            emit NodeRemoved(_ids[i]);

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L451


## [G-31] Using assembly to check for zero can save gas

Using assembly to check for zero can save gas by allowing more direct access to the evm and reducing some of the overhead associated with high-level operations in solidity.

```solidity
file: /contracts/contracts/BorrowerOperations.sol

831        require(status == 0, "BorrowerOperations: Cdp is active or has been previously closed");

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L831


```solidity
file: /contracts/contracts/CdpManager.sol

159        if (newDebt == 0) {

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L159


```solidity
file: /contracts/contracts/LiquidationLibrary.sol

157        if (
                liquidationValues.totalCollToSendToLiquidator == 0 &&
                liquidationValues.debtToBurn == 0
            ) {

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L157-L160


## [G-32] Use assembly to validate msg.sender

We can use assembly to efficiently validate msg.sender for the didPay and uniswapV3SwapCallback functions with the least amount of opcodes necessary. Additionally, we can use xor() instead of iszero(eq()), saving 3 gas. We can also potentially save gas on the unhappy path by using scratch space to store the error selector, potentially avoiding memory expansion costs.]

```solidity
file: /contracts/contracts/ActivePool.sol

229            msg.sender == borrowerOperationsAddress || msg.sender == cdpManagerAddress,

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L229


```solidity
file: /contracts/contracts/CdpManagerStorage.sol

661            msg.sender == borrowerOperationsAddress,

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L661


```solidity
file: /contracts/contracts/EBTCToken.sol

316            msg.sender == borrowerOperationsAddress ||
                msg.sender == cdpManagerAddress ||
                isAuthorized(msg.sender, msg.sig),

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L316-L318



## [G-33] Pre-increment and pre-decrement are cheaper than +1 ,-1

```solidity
file: /contracts/contracts/CdpManager.sol

421                    _numCdpsFullyRedeemed = _numCdpsFullyRedeemed + 1;

499            _cnt = _cnt - 1;

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L421


```solidity
file: /contracts/contracts/SortedCdps.sol

193                    _currentIndex = _currentIndex + 1;

251                _ownedCount = _ownedCount + 1;

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L193



## [G-34] Consider Using Solady's Gas Optimized Lib for Math

Utilizing gas-optimized math functions from libraries like Solady can lead to more efficient smart contracts. This is particularly beneficial in contracts where these operations are frequently used.

```solidity
file: /contracts/contracts/CdpManager.sol

706        return (baseRate * decayFactor) / DECIMAL_PRECISION;

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L706


```solidity
file: /contracts/contracts/LiquidationLibrary.sol

365        uint _debtToColl = (_totalDebtToBurn * DECIMAL_PRECISION) / _recoveryState.price;

592            uint256 _debtToRepay = (_incentiveColl * _price) / LICR;

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L365


```solidity
file: /contracts/contracts/CdpManagerStorage.sol

557       uint256 deltaIndex = _newIndex - _prevIndex;
        uint256 deltaIndexFees = (deltaIndex * stakingRewardSplit) / MAX_REWARD_SPLIT;

        // we take the fee for all CDPs immediately which is scaled by index precision
        uint256 _deltaFeeSplit = deltaIndexFees * getSystemCollShares();
        uint256 _cachedAllStakes = totalStakes;
        // return the values to update the global fee accumulator
        uint256 _feeTaken = collateral.getSharesByPooledEth(_deltaFeeSplit) / DECIMAL_PRECISION;
        uint256 _deltaFeeSplitShare = (_feeTaken * DECIMAL_PRECISION) +
            systemStEthFeePerUnitIndexError;
        uint256 _deltaFeePerUnit = _deltaFeeSplitShare / _cachedAllStakes;
        uint256 _perUnitError = _deltaFeeSplitShare - (_deltaFeePerUnit * _cachedAllStakes);

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L557-L568
