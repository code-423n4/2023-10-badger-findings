&nbsp;

## \[G-1\] Avoiding the creation of an intermediate variable `cachedSystemDebt` and updating the `systemDebt`

an additional read operation is performed to load the `systemDebt` value into the `cachedSystemDebt` variable. This read operation incurs a gas cost. This cost is typically around 2100 gas for a simple storage variable.

```diff
function increaseSystemDebt(uint256 _amount) external override {
        _requireCallerIsBOorCdpM();


-    uint256 cachedSystemDebt = systemDebt + _amount;
+    systemDebt =systemDebt + _amount;
  

-      systemDebt = cachedSystemDebt;
-     emit ActivePoolEBTCDebtUpdated(cachedSystemDebt);
+     emit ActivePoolEBTCDebtUpdated(systemDebt);
    }
```

&nbsp;https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L194C5-L202C1

```diff
function decreaseSystemDebt(uint256 _amount) external override {
        _requireCallerIsBOorCdpM();


-    uint256 cachedSystemDebt = systemDebt - _amount;
+    systemDebt -= _amount;
  

-      systemDebt = cachedSystemDebt;
-     emit ActivePoolEBTCDebtUpdated(cachedSystemDebt);
+     emit ActivePoolEBTCDebtUpdated(systemDebt);
    }
```

&nbsp;https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L207C4-L214C6

```
function increaseSystemCollShares(uint256 _value) external override {
        _requireCallerIsBorrowerOperations();

+        systemCollShares += _value;
-       uint256 cachedSystemCollShares = systemCollShares + _value;
-       systemCollShares = cachedSystemCollShares;
-       emit SystemCollSharesUpdated(cachedSystemCollShares);
+       emit SystemCollSharesUpdated(systemCollShares);
    }
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L242C5-L249C1

## \[G-2\] Avoid duplicate `msg.sender` use assembly to check `msg.sender`

You can use assembly to optimize the `require` statement to avoid duplicate `msg.sender` checks and save some gas.

using assembly to optimize this `require` might save around 100 to 200 gas.

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L228C9-L231C11

```
require(
            msg.sender == borrowerOperationsAddress || msg.sender == cdpManagerAddress,
            "ActivePool: Caller is neither BorrowerOperations nor CdpManager"
        );
```

Here's how you can optimize the `require` statement using assembly:

```
require(
    assembly {
        let sender := msg.sender
        let borrowerOp := sload(borrowerOperationsAddress.slot)
        let cdpManager := sload(cdpManagerAddress.slot)
        iszero(or(eq(sender, borrowerOp), eq(sender, cdpManager)))
    },
    "ActivePool: Caller is neither BorrowerOperations nor CdpManager"
);
```

In this optimized code, assembly is used to load the `borrowerOperationsAddress` and `cdpManagerAddress` directly from storage and then check if `msg.sender` is neither of these two addresses. This reduces the need to check `msg.sender` twice and can potentially save gas.

&nbsp;

```
require(
            msg.sender == borrowerOperationsAddress ||
                msg.sender == cdpManagerAddress ||
                isAuthorized(msg.sender, msg.sig),
            "EBTC: Caller is neither BorrowerOperations nor CdpManager nor authorized"
        );
    }
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L315C9-L321C6

## \[G-3\] Use hardcode address instead address(this)

Instead of using address(

), it is more gas-efficient to pre-calculate and use the hardcoded address. Foundry’s script.sol and solmate’s LibRlp.sol contracts can help achieve this.

References: https://book.getfoundry.sh/reference/forge-std/compute-create-address

```
collateral.balanceOf(address(this)) >= collateral.getPooledEthByShares(systemCollShares),
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L295

```
collateral.sharesOf(address(this)) >= systemCollShares,
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L299

```
return collateral.balanceOf(address(this));
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L337

```
uint256 balance = IERC20(token).balanceOf(address(this));
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L376

```
uint256 balance = IERC20(token).balanceOf(address(this));
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L145

```
return keccak256(abi.encode(typeHash, name, version, _chainID(), address(this)));
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L240

```
_recipient != address(0) && _recipient != address(this),
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L297

```
constructor(address _owner) RolesAuthority(_owner, Authority(address(this))) {}
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L36

```
address(this),
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L131

```
initialCdpIndex = sortedCdps.cdpCountOf(address(this));
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L143

```
IERC3156FlashBorrower(address(this)),
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L149

```
IERC3156FlashBorrower(address(this)),
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L156

```
bytes32 cdpId = sortedCdps.cdpOfOwnerByIndex(address(this), initialCdpIndex);
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L173

```
address(this),
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L131

```
IERC20(swapChecks[i].tokenToCheck).balanceOf(address(this)) >
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L441

```
require(addy != address(this)); // If it could call this it could fake the forwarded caller
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L456

```
address _owner = IOwnerLike(address(this)).owner();
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L64

```
require(msg.sender == address(this)); // Must call this via `execute` to explicitly set the flag
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L77

```
require(msg.sender == owner || authority.canCall(msg.sender, address(this), msg.sig));
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L45

```
(address(auth) != address(0) && auth.canCall(user, address(this), functionSig)) ||
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L38

```
return (address(auth) != address(0) && auth.canCall(user, address(this), functionSig));
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L35

```
require(_authority.canCall(msg.sender, address(this), msg.sig));
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L41

```
emit AuthorityUpdated(address(this), Authority(newAuthority));
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L62

## \[G-4\] Use assembly for math (add, sub, mul, div)

```
return (amount * feeBps) / MAX_BPS;
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L321

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1118

## \[G‑5\] Use a more recent version of solidity

```
pragma solidity 0.8.17;
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L3

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L3

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L3

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L3

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L3

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L2

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L3

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L3

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L2

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L2

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L2

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L2

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L2

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L2

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L2

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L3

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L3

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L3

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ReentrancyGuard.sol#L2

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L2

## \[G-6\] From a gas optimization perspective, declaring the variable as `public` is generally more gas-efficient than using the `getter` function.

When you declare a state variable as `public`, the Solidity compiler automatically generates a getter function for that variable. This getter function allows you to access the value of the variable directly from outside the contract. Using this auto-generated getter is usually more gas-efficient than writing a custom getter function, as it avoids the overhead of function call execution.

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L74C3-L76C6

```
function getSystemCollShares() external view override returns (uint256) {
        return systemCollShares;
    }
```

&nbsp;https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L82C4-L84C6

```
function getSystemDebt() external view override returns (uint256) {
        return systemDebt;
    }
```

&nbsp;https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L89C5-L91C6

```
function getFeeRecipientClaimableCollShares() external view override returns (uint256) {
        return feeRecipientCollShares;
    }
```

&nbsp;

## <ins>\[G-7\] Use bytes datatype for constants instead of strings</ins>

Use a fixed size bytes datatype like bytes4 in place of string.

Instances of this issue :

```
function version() external pure override returns (string memory) {
        return _VERSION;
    }
```

&nbsp;https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L687C1-L689C6

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L349

```
function symbol() external pure override returns (string memory) {
        return _SYMBOL;
    }
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L337C4-L339C6

```
function name() external pure override returns (string memory) {
        return _NAME;
    }
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L331C5-L333C6

## \[G-8\] Use double if statements instead of &&

If the if statement has a logical AND and is not followed by an else statement, it can be replaced with 2 if statements

```
if (!_isDebtIncrease && _debtChange > 0) {
```

&nbsp;https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L393C8-L393C51

```
if (
                    !_fallbackIsBroken(fallbackResponse) &&
                    !_responseTimeout(fallbackResponse.timestamp, newFallbackCaler.fallbackTimeout())
                ) {
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L372C17-L375C20

```
if (
            _checkHealthyCLResponse(chainlinkResponse.roundEthBtcId, ethBtcAnswer) &&
            _checkHealthyCLResponse(chainlinkResponse.roundStEthEthId, stEthEthAnswer)
        ) {
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L666C7-L669C12

```
if (
            _checkHealthyCLResponse(prevChainlinkResponse.roundEthBtcId, ethBtcAnswer) &&
            _checkHealthyCLResponse(prevChainlinkResponse.roundStEthEthId, stEthEthAnswer)
        ) {
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L754C8-L757C12

```
if (maxNodes > 0 && i >= maxNodes) {
```

&nbsp;https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L202

```
if (maxNodes > 0 && i >= maxNodes) {
```

&nbsp;https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L259

```
if (maxNodes > 0 && i >= maxNodes) {
```

&nbsp;https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L330

```
if (prevId == dummyId && nextId == dummyId) {
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L382

```
if (_prevId == dummyId && _nextId == dummyId) {
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L596

```
if (data.head == _startId && _NICR >= cdpManager.getCachedNominalICR(_startId)) {
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L621

```
if (data.tail == _startId && _NICR <= cdpManager.getCachedNominalICR(_startId)) {
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L644

```
if (prevId == dummyId && nextId == dummyId) {
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L696

## \[G‑9\] Usage of uints/ints smaller than 32 bytes (256 bits) incurs overhead

When using elements that are smaller than 32 bytes, your contract’s gas usage may be higher. This is because the EVM operates on 32 bytes at a time. Therefore, if the element is smaller than that, the EVM must use more operations in order to reduce the size of the element from 32 bytes to the desired size.

[https://docs.soliditylang.org/en/v0.8.11/internals/layout\_in\_storage.html](https://docs.soliditylang.org/en/v0.8.11/internals/layout_in_storage.html)

Each operation involving a uint8 costs an extra 22-28 gas (depending on whether the other operand is also a variable of type uint8) as compared to ones involving uint256, due to the compiler having to clear the higher bits of the memory word before operating on the uint8, as well as the associated stack operations of doing so. Use a larger size then downcast where needed.

```
uint8 v,
```

&nbsp;https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L711

```
function decimals() external pure override returns (uint8) {
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L343

```
uint8 roleId;
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L20

```
uint8[] roles;
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L27

```
mapping(uint8 => string) internal roleNames;
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L30

```
event RoleNameSet(uint8 indexed role, string indexed name);
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L32

```
function getRoleName(uint8 role) external view returns (string memory roleName) {
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L146

```
function setRoleName(uint8 role, string memory roleName) external requiresAuth {
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L154

```
uint8 ethBtcDecimals;
uint8 stEthEthDecimals;
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L612C9-L613C32

```
try ETH_BTC_CL_FEED.decimals() returns (uint8 decimals) {
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L615

```
try STETH_ETH_CL_FEED.decimals() returns (uint8 decimals) {
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L623

```
uint80 _currentRoundEthBtcId,
uint80 _currentRoundStEthEthId
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L688C6-L689C39

```
uint8 ethBtcDecimals;
uint8 stEthEthDecimals;
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L700C8-L701C32

```
try ETH_BTC_CL_FEED.decimals() returns (uint8 decimals) {
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L703

```
try STETH_ETH_CL_FEED.decimals() returns (uint8 decimals) {
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L711

```
uint8 _ethBtcDecimals,
uint8 _stEthEthDecimals
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L791C8-L792C32

```
uint16 public feeBps = 3; // may be subject to future adjustments through protocol governance
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L14

&nbsp;https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L722

```
abi.encode(
```

## \[G-10\] Splitting require() statements that use && saves gas

Instead of using the && operator in a single require statement to check multiple conditions, I suggest using multiple require statements with 1 condition per require statement (saving 3 gas per &).  
See this issue which describes the fact that there is a larger deployment gas cost, but with enough runtime calls, the change ends up being cheaper.

```
recoveredAddress != address(0) && recoveredAddress == _borrower,
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L735

```
_maxFeePercentage >= redemptionFeeFloor && _maxFeePercentage <= DECIMAL_PRECISION,
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L763

```
_recipient != address(0) && _recipient != address(this),
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L297

```
_recipient != cdpManagerAddress && _recipient != borrowerOperationsAddress,
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L301

```
require(
            !_chainlinkIsBroken(chainlinkResponse, prevChainlinkResponse) &&
                !_chainlinkIsFrozen(chainlinkResponse),
            "PriceFeed: Chainlink must be working and current"
        );
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L79C8-L83C11

```
return
            _checkICRAgainstMCR(_icr) ||
            (_checkICRAgainstTCR(_icr, _tcr) && _checkRecoveryModeForTCR(_tcr));
    }
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L128C8-L131C6

## \[G-11\] internal functions only called once can be inlined to save gas

Proof Of Concept

```
function _requireSingularCollChange(
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L803

```
function _requireNonZeroAdjustment(
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L813

```
function _requireValidAdjustmentInCurrentMode(
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L760

```
760   function _processTokenMovesFromAdjustment(MoveTokensParams memory _varMvTokens) internal {
```

&nbsp;https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L852

```
function _requireNoDecreaseOfICR(uint256 _newICR, uint256 _oldICR) internal pure {
```

&nbsp;https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L921C14-L921C37

```
function _requireValidDebtRepayment(uint256 _currentDebt, uint256 _debtRepayment) internal pure {
```

&nbsp;https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L946C14-L946C40

```
function _getNewNominalICRFromCdpChange(
```

&nbsp;https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L986C14-L986C44

```
function _getNewICRFromCdpChange(
```

&nbsp;https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1004C14-L1004C37

```
function _requireCallerIsBorrowerOperations() internal view {
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L112

```
function _requireCallerIsCdpManager() internal view {
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L119

```
function _requireCallerIsActivePool() internal view {
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L123C14-L123C39

```
function _requireCallerIsCdpM() internal view {
        require(msg.sender == cdpManagerAddress, "EBTC: Caller is not CdpManager");
    }
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L323C5-L325C6

## \[G‑12\] Using assembly to check for zero can save gas

Using assembly to check for zero can save gas by allowing more direct access to the evm and reducing some of the overhead associated with high-level operations in solidity.

```
if (newDebt == 0) {
```

&nbsp; https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L159

```
if (_maxIterations == 0) {
```

&nbsp;https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L377

```
if (
            _response.timestampEthBtc == 0 ||
            _response.timestampEthBtc > block.timestamp ||
            _response.timestampStEthEth == 0 ||
            _response.timestampStEthEth > block.timestamp
        ) {
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L419C8-L424C12

```
if (_response.timestamp == 0 || _response.timestamp > block.timestamp) {
```

&nbsp;https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L471

```
if (_response.answer == 0) {
```

&nbsp;https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L475

```
if (minPrice == 0) return false;
```

&nbsp;https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L532

```
if (_currentRoundEthBtcId == 0 || _currentRoundStEthEthId == 0) {
```

&nbsp;https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L695

```
if (_size == 0) {
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L89

```
if (_answer <= 0) return false;
        if (_roundId == 0) return false;
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L776C8-L777C41

```
if (maxArraySize == 0) {
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L305

```
require(cdpManager.getCdpStatus(_id) == 0, "SortedCdps: new id is NOT nonExistent!");
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L352

```
if (_maxIterations == 0) {
```

&nbsp;https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L78

```
if (arrayLength == 0) {
```

&nbsp;https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L171

```
if (_minutes == 0) {
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L64

```
if (n % 2 == 0) {
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L74

## \[G-13\] >= costs less gas than >

The compiler uses opcodes GT and ISZERO for solidity code that uses >, but only requires LT for >=, which saves 3 gas

There are 13 instances of this issue:

```
File:  packages/contracts/contracts/CdpManagerStorage.sol
512   if (_newIndex > _oldIndex && totalStakes > 0) {

556   require(_newIndex > _prevIndex, "CDPManager: only take fee with bigger new index");

585   require(activePool.getSystemCollShares() > _feeTaken, "CDPManager: fee split is too big");

636    if (_scaledCdpColl > _feeSplitDistributed) {

654   CdpOwnersArrayLength > 1 && sortedCdps.getSize() > 1,

765   if (_newIndex > _oldIndex && totalStakes > 0) {
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L512

```
File:  packages/contracts/contracts/LiquidationLibrary.sol
476    if (_partialState.ICR > LICR) {

553    if (_ICR > LICR) {   

578    if (_ICR > LICR) {
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L476

```
File:  packages/contracts/contracts/SortedCdps.sol
422   require(_len > 1, "SortedCdps: batchRemove() only apply to multiple cdpIds!");

460   if (data.size > 1) {    
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L422

```
File:  packages/contracts/contracts/Dependencies/EbtcMath.sol
60   if (_minutes > 525600000) {
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L60

&nbsp;

```
while (currentBorrower != address(0) && getSyncedICR(_cId, totals.price) < MCR) {
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L369

```
while (
            currentBorrower != address(0) && totals.remainingDebtToRedeem > 0 && _maxIterations > 0
        ) {
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L388C9-L390C12

```
while (prevId != dummyId && !_validInsertPosition(_NICR, prevId, nextId)) {
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L629

```
while (nextId != dummyId && !_validInsertPosition(_NICR, prevId, nextId)) {
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L652

```
while (
                vars.currentCdpUser != address(0) &&
                cdpManager.getSyncedICR(vars.currentCdpId, _price) < MCR
            ) {
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L68C13-L71C16

```
while (
                vars.currentCdpUser != address(0) &&
                vars.remainingEbtcToRedeem > 0 &&
                _maxIterations-- > 0
            ) {
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L84C12-L88C16

## \[G-14\] Parameter not used in the function

Remove the parameter \_initData in VariableInterestRate.getNewRate.\_initData because of it's not used in the function.

```
function batchLiquidateCdps(bytes32[] memory _cdpArray) external override {
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L126

## \[G-15\] Expressions for constant values such as a call to¬†keccak256(), should use immutable rather than constant

The reason for this is that constant variables are evaluated at runtime and their value is included in the bytecode of the contract. This means that any expensive operations performed as part of the constant expression, such as a call to keccak256(), will be executed every time the contract is deployed, even if the result is always the same. This can result in higher gas costs.

```
bytes32 constant MY_HASH = keccak256("my string");
```

Alternatively, we could use an immutable variable, like so:

```
bytes32 immutable MY_HASH = keccak256("my string");
```

There are 4 instances of this issue:

```
File:  packages/contracts/contracts/BorrowerOperations.sol
32      bytes32 private constant _PERMIT_POSITION_MANAGER_TYPEHASH =
        keccak256(
            "PermitPositionManagerApproval(address borrower,address positionManager,uint8 status,uint256 nonce,uint256 deadline)"
        );
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L32-L35

```
File:  packages/contracts/contracts/LeverageMacroBase.sol
37   bytes32 constant FLASH_LOAN_SUCCESS = keccak256("ERC3156FlashBorrower.onFlashLoan");
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L37

```
File:  packages/contracts/contracts/SimplifiedDiamondLike.sol
39   bytes32 constant DIAMOND_STORAGE_POSITION = keccak256("diamond.standard.diamond.storage");
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L39

```
File:  packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol
11  bytes32 public constant FLASH_SUCCESS_VALUE = keccak256("ERC3156FlashBorrower.onFlashLoan");
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L11

## \[G-16\] Public Functions To External

External call cost is less expensive than of public functions.  
Contracts are allowed to override their parents’ functions and change the visibility from external to public.  
The following functions could be set external to save gas and improve code quality. External call cost is less expensive than of public functions.

```
function getDeploymentStartTime() public view returns (uint256) {
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L717C14-L717C36

```
function sweepToken(address token, uint256 amount) public {
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L234

```
function doesRoleHaveCapability(
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L42C14-L42C36

```
function isPublicCapability(address target, bytes4 functionSig) public view returns (bool) {
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L50C14-L50C32

```
function canCall(
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L63C14-L63C21

## \[G-17\] Use assembly to validate msg.sender

We can use assembly to efficiently validate msg.sender for the didPay and uniswapV3SwapCallback functions with the least amount of opcodes necessary. Additionally, we can use xor() instead of iszero(eq()), saving 3 gas. We can also potentially save gas on the unhappy path by using scratch space to store the error selector, potentially avoiding memory expansion costs.

```
msg.sender == borrowerOperationsAddress,
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L114

```
require(msg.sender == cdpManagerAddress, "CollSurplusPool: Caller is not CdpManager");
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L120

```
require(msg.sender == activePoolAddress, "CollSurplusPool: Caller is not Active Pool");
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L124

```
msg.sender == borrowerOperationsAddress,
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L308

```
require(
            msg.sender == borrowerOperationsAddress ||
                msg.sender == cdpManagerAddress ||
                isAuthorized(msg.sender, msg.sig),
            "EBTC: Caller is neither BorrowerOperations nor CdpManager nor authorized"
        );
    }
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L315C9-L321C6

```
require(msg.sender == cdpManagerAddress, "EBTC: Caller is not CdpManager");
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L324

```
require(msg.sender == address(cdpManager), "SortedCdps: Caller is not the CdpManager");
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L715

```
msg.sender == borrowerOperationsAddress || msg.sender == address(cdpManager),
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L721

```
require(owner() == msg.sender, "Must be owner");
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L45

```
require(msg.sender == owner);
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L52

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L67

```
require(msg.sender == address(this)); // Must call this via `execute` to explicitly set the flag
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L77

```
require(msg.sender == owner, "Must be owner");
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L111

```
require(msg.sender == owner || authority.canCall(msg.sender, address(this), msg.sig));
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L45

## \[G-18\] Cache external calls outside of loop to avoid re-calling function on each iteration

Performing STATICCALLs that do not depend on variables incremented in loops should always try to be avoided within the loop. In the following instances, we are able to cache the external calls outside of the loop to save a STATICCALL (100 gas) per loop iteration.

There are 1 instances of this issue:

```
File:  packages/contracts/contracts/Governor.sol
46        for (uint256 i = 0; i < users.length(); i++) {
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L46-47

```
    function getUsersByRole(uint8 role) external view returns (address[] memory usersWithRole) {
        // Search over all users: O(n) * 2
        uint256 count;
        uint256 ulenght = users.length();
-       for (uint256 i = 0; i < users.length(); i++) {
+       for (uint256 i = 0; i < ulenght; i++) {    
            address user = users.at(i);
            bool _canCall = doesUserHaveRole(user, role);
            if (_canCall) {
                count += 1;
            }
        }
```

## \[G-19\] ABI.ENCODE() is less efficient than ABI.ENCODEPACKED()

Changing the abi.encode function to abi.encodePacked can save gas since the abi.encode function pads extra null bytes at the end of the call data, which is unnecessary. Also, in general, abi.encodePacked is more gas-efficient.

```
abi.encode(
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L722

```
return keccak256(abi.encode(typeHash, name, version, _chainID(), address(this)));
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L240

```
OpenCdpOperation memory flData = abi.decode(data, (OpenCdpOperation));
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L461

```
CloseCdpOperation memory flData = abi.decode(data, (CloseCdpOperation));
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L475

```
AdjustCdpOperation memory flData = abi.decode(data, (AdjustCdpOperation));
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L483

## \[G‑20\] Using private rather than public for constants, saves gas

If needed, the values can be read from the verified contract source code, or if there are multiple values there can be a single getter function that returns a tuple of the values of all currently-public constants. Saves 3406-3606 gas in deployment gas due to the compiler not having to create non-payable getter functions for deployment calldata, not having to store the bytes of the value outside of where it’s used, and not adding another entry to the method ID table.

```
uint256 public constant TIMEOUT_ETH_BTC_FEED = 4800; // 1 hours & 20min: 60 * 80
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L32

```
uint256 public constant TIMEOUT_STETH_ETH_FEED = 90000; // 25 hours: 60 * 60 * 25
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L33

```
uint256 public constant MAX_PRICE_DEVIATION_FROM_PREVIOUS_ROUND = 5e17; // 50%
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L36

```
uint256 public constant MAX_PRICE_DIFFERENCE_BETWEEN_ORACLES = 5e16; // 5%
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L42

&nbsp;https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L381

```
string public constant NAME = "HintHelpers";
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L12

```
ISortedCdps public immutable sortedCdps;
    ICdpManager public immutable cdpManager;
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L13C1-L16C1

```
address public immutable owner;
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L42

```
uint256 public constant MAX_BPS = 10_000;
    uint256 public constant MAX_FEE_BPS = 1_000; // 10%
    bytes32 public constant FLASH_SUCCESS_VALUE = keccak256("ERC3156FlashBorrower.onFlashLoan");
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L9C3-L11C97

```
uint256 public constant LICR = 1030000000000000000; // 103%


    // Minimum collateral ratio for individual cdps
    uint256 public constant MCR = 1100000000000000000; // 110%


    // Critical system collateral ratio. If the system's total collateral ratio (TCR) falls below the CCR, Recovery Mode is triggered.
    uint256 public constant CCR = 1250000000000000000; // 125%


    // Amount of stETH collateral to be locked in active pool on opening cdps
    uint256 public constant LIQUIDATOR_REWARD = 2e17;


    // Minimum amount of stETH collateral a CDP must have
    uint256 public constant MIN_NET_STETH_BALANCE = 2e18;


    uint256 public constant PERCENT_DIVISOR = 200; // dividing by 200 yields 0.5%


    uint256 public constant BORROWING_FEE_FLOOR = 0; // 0.5%


    uint256 public constant STAKING_REWARD_SPLIT = 5_000; // taking 50% cut from staking reward


    uint256 public constant MAX_REWARD_SPLIT = 10_000;


    IActivePool public immutable activePool;


    IPriceFeed public immutable override priceFeed;


    // the only collateral token allowed in CDP
    ICollateralToken public immutable collateral;
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L19C4-L46C50

```
uint256 public constant MAX_TCR = type(uint256).max;
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L7

## \[G-21\] Use of emit inside a loop

Emitting an event inside a loop performs a LOG op N times, where N is the loop length. Consider refactoring the code to emit the event only once at the end of loop. Gas savings should be multiplied by the average loop length.

There are 1 instances of this issue:

```
File:  packages/contracts/contracts/SortedCdps.sol
451   emit NodeRemoved(_ids[i]);
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L451

## \[G-22\] Superfluous event fields

block.number and block.timestamp are added to the event information by default, so adding them manually will waste additional gas.

Proof Of Concept

```
emit UnhealthyFallbackCaller(_fallbackCaller, block.timestamp);
```

## \[G-23\] Use Modifiers Instead of Functions To Save Gas

This with 0.8.9 compiler and optimization enabled. As you can see it's cheaper to deploy with a modifier, and it will save you about 30 gas. But sometimes modifiers increase code size of the contract.

```
function _assertOwner() internal {
        // Reference will compare to variable,
        require(owner() == msg.sender, "Must be owner");
    }
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L43C5-L46C6

## \[G‑24\] Using `constant`s instead of `enum` can save gas

`Enum` is expensive and it is <ins>more efficient to use constants</ins> instead. An illustrative example of this approach can be found in the <ins>ReentrancyGuard.sol</ins>.

```
enum FlashLoanType {
        stETH,
        eBTC,
        noFlashloan // Use this to not perform a FL and just `doOperation`
    }


    enum PostOperationCheck {
        openCdp,
        cdpStats,
        isClosed
    }


    enum Operator {
        skip,
        equal,
        gte,
        lte
    }
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L70C4-L87C6

```
enum OperationType {
        OpenCdpOperation,
        AdjustCdpOperation,
        CloseCdpOperation
    }
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L283C1-L288C6

```
enum OperationType {
        call,
        delegatecall
    }
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L94C4-L97C6

## \[G-25\] Multiple address mappings can be combined into a single mapping of an address to a struct, where appropriate

Saves a storage slot for the mapping. Depending on the circumstances and sizes of types, can avoid a Gsset (20000 gas) per mapping combined. Reads and subsequent writes can also be cheaper when a function requires both values and they both fit in the same storage slot. Finally, if both fields are accessed in the same function, can save ~42 gas per access due to not having to recalculate the key’s keccak256 hash (Gkeccak256 - 30 gas) and that calculation’s associated stack operations.

```
address public immutable borrowerOperations;
    address public immutable activePool;
    address public immutable cdpManager;
    address public immutable ebtcToken;
    address public immutable stETH;
    address public immutable sortedCdps;
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L12C1-L18C1

## \[G-26\] Extra declaration in named returns that don't use them

Using both named returns and a return statement isn’t necessary, this consumes extra gas as one more variable that is not used is declared .

```
function getSystemCollShares() public view returns (uint256 entireSystemColl) {
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L67C14-L67C33

```
function _getSystemDebt() internal view returns (uint256 entireSystemDebt) {
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L75

```
function _getCachedTCR(uint256 _price) internal view returns (uint256 TCR) {
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L79

```
function _getTCRWithSystemDebtAndCollShares(
        uint256 _price
    ) internal view returns (uint256 TCR, uint256 _coll, uint256 _debt) {
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L83C2-L85C74

## \[G-27\] `internal` functions not called by the contract should be removed

If the functions are required by an interface, the contract should inherit from that interface and use the `override` keyword

Note: missed from bots

```
function _requireUserAcceptsFee(
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L103C14-L103C37

```
function decMul(uint256 x, uint256 y) internal pure returns (uint256 decProd) {
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L35

## \[G-28\] Using storage instead of memory for structs/arrays saves gas

When fetching data from a storage location, assigning the data to a memory variable causes all fields of the struct/array to be read from storage, which incurs a Gcoldsload (2100 gas) for each field of the struct/array. If the fields are read from the new memory variable, they incur an additional MLOAD rather than a cheap stack read. Instead of declearing the variable with the memory keyword, declaring the variable with the storage keyword and caching any fields that need to be re-read in stack variables, will be much cheaper, only incuring the Gcoldsload for the fields actually read. The only time it makes sense to read the whole struct/array into a memory variable, is if the full struct/array is being returned by the function, is being passed to a function that requires memory, or if the array/struct is being read from another memory array/struct

There are 36 instances of this issue:

```
File:  packages/contracts/contracts/BorrowerOperations.sol
427  MoveTokensParams memory _varMvTokens = MoveTokensParams(

760  function _processTokenMovesFromAdjustment(MoveTokensParams memory _varMvTokens) internal {

856  AdjustCdpLocals memory _vars

987  AdjustCdpLocals memory vars,
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L427

```
File:  packages/contracts/contracts/CdpManager.sol
136  SingleRedemptionInputs memory _redeemColFromCdp

150  CdpDebtAndCollShares memory _oldDebtAndColl = CdpDebtAndCollShares(

329   RedemptionTotals memory totals;

403   SingleRedemptionValues memory singleRedemption = _redeemCollateralFromCdp(
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L136

```
File:  packages/contracts/contracts/HintHelpers.sol
62  LocalVariables_getRedemptionHints memory vars;

134 LocalVariables_getRedemptionHints memory vars,
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L62

```
File:  packages/contracts/contracts/LeverageMacroBase.sol
176   ICdpManagerData.Cdp memory cdpInfo = cdpManager.Cdps(cdpId);

187   ICdpManagerData.Cdp memory cdpInfo = cdpManager.Cdps(checkParams.cdpId);

199   ICdpManagerData.Cdp memory cdpInfo = cdpManager.Cdps(checkParams.cdpId);

244   function _doCheckValueType(CheckValueAndType memory check, uint256 valueToCheck) internal {

291    function _handleOperation(LeverageMacroOperation memory operation) internal {
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L176

```
File:  packages/contracts/contracts/PriceFeed.sol
73      ChainlinkResponse memory chainlinkResponse = _getCurrentChainlinkResponse();
74      ChainlinkResponse memory prevChainlinkResponse = _getPrevChainlinkResponse(

100     ChainlinkResponse memory chainlinkResponse = _getCurrentChainlinkResponse();
101     ChainlinkResponse memory prevChainlinkResponse = _getPrevChainlinkResponse(   

105  FallbackResponse memory fallbackResponse = _getCurrentFallbackResponse();

361  FallbackResponse memory fallbackResponse;

401   ChainlinkResponse memory _currentResponse,
402   ChainlinkResponse memory _prevResponse

412   function _badChainlinkResponse(ChainlinkResponse memory _response) internal view returns (bool) {

435  function _chainlinkIsFrozen(ChainlinkResponse memory _response) internal view returns (bool) {

446     ChainlinkResponse memory _currentResponse,
        ChainlinkResponse memory _prevResponse   

465    function _fallbackIsBroken(FallbackResponse memory _response) internal view returns (bool) {

486  FallbackResponse memory _fallbackResponse

504     ChainlinkResponse memory _chainlinkResponse,
        ChainlinkResponse memory _prevChainlinkResponse,
        FallbackResponse memory _fallbackResponse

527     ChainlinkResponse memory _chainlinkResponse,
        FallbackResponse memory _fallbackResponse     

562    FallbackResponse memory _fallbackResponse
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L73-L74

## \[G-29\] Can Make The Variable Outside The Loop To Save Gas

When you declare a variable inside a loop, Solidity creates a new instance of the variable for each iteration of the loop. This can lead to unnecessary gas costs, especially if the loop is executed frequently or iterates over a large number of elements.

By declaring the variable outside the loop, you can avoid the creation of multiple instances of the variable and reduce the gas cost of your contract. Here's an example:

```
contract MyContract {
    function sum(uint256[] memory values) public pure returns (uint256) {
        uint256 total = 0;
        
        for (uint256 i = 0; i < values.length; i++) {
            total += values[i];
        }
        
        return total;
    }
}
```

There are 4 instances of this issue:

```
File:  packages/contracts/contracts/Governor.sol
47      address user = users.at(i);
48      bool _canCall = doesUserHaveRole(user, role);

58      address user = _usrs[i];
59      bool _canCall = doesUserHaveRole(user, role);
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L47-L48

## \[G-30\] Use constants instead of type(uintx).max

Using constants instead of type(uintx).max can save gas in some cases because constants are precomputed at compile-time and can be reused throughout the code, whereas type(uintx).max requires computation at runtime

```
File:  packages/contracts/contracts/BorrowerOperations.sol
1133   return type(uint112).max;
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1133

```
File:  packages/contracts/contracts/CdpManager.sol
278  _maxIterations = type(uint256).max;
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L378

```
File:  packages/contracts/contracts/CdpManagerStorage.sol
21  uint128 public constant UNSET_TIMESTAMP = type(uint128).max;
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L21

```
File: packages/contracts/contracts/EBTCToken.sol
143  if (cachedAllowance != type(uint256).max) {
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L143

```
File:  packages/contracts/contracts/Governor.sol
78   for (uint8 i = 0; i < type(uint8).max; i++) {

84   for (uint8 i = 0; i < type(uint8).max; i++) {

98   for (uint8 i = 0; i < type(uint8).max; i++) {

107  for (uint8 i = 0; i < type(uint8).max; i++) {            
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L78

```
File:  packages/contracts/contracts/HintHelpers.sol
79  _maxIterations = type(uint256).max;
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L79

```
File:  packages/contracts/contracts/LeverageMacroReference.sol
39      ebtcToken.approve(_borrowerOperationsAddress, type(uint256).max);
        stETH.approve(_borrowerOperationsAddress, type(uint256).max);
        stETH.approve(_activePool, type(uint256).max);

53      ebtcToken.approve(address(borrowerOperations), type(uint256).max);
        stETH.approve(address(borrowerOperations), type(uint256).max);
        stETH.approve(address(activePool), type(uint256).max);        
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L39-L41

```
File:  packages/contracts/contracts/SortedCdps.sol
90  _size = type(uint256).max;
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L90

```
File:  packages/contracts/contracts/Dependencies/EbtcMath.sol
7  uint256 public constant MAX_TCR = type(uint256).max;
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L7

&nbsp;