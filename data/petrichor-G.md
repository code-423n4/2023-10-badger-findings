# GAS OPTIMIZATION

# SUMMARY
|      |  issue  |  instance  |
|------|---------|------------|
|[G‑01]|Optimize External Calls with Assembly for Memory Efficiency|115|
|[G‑02]|Use assembly to validate msg.sender |22|
|[G‑03]|Avoid contract existence checks by using low level calls|19|
|[G‑04]| >= costs less gas than >|14|
|[G‑05]|Amounts should be checked for 0 before calling a transfer|6|
|[G‑06]|Functions guaranteed to revert when called by normal users can be marked payable|11|
|[G‑07]|Structs can be modified to fit in fewer storage slots|17|
|[G‑08]| Use constants instead of type(uintx).max|19|
|[G‑09]|Using storage instead of memory for structs/arrays saves gas|38|
|[G‑10]|Can Make The Variable Outside The Loop To Save Gas |4|
|[G‑11]|Use Modifiers Instead of Functions To Save Gas|9|
|[G‑12]| bytes constants are more eficient than string constans|12|
|[G‑13]|Use assembly to hash instead of solidity|8|
|[G‑14]|internal functions only called once can be inlined to save gas|20|
|[G‑15]|Use nested if statements instead of &&|15|
|[G‑16]|Do-While loops are cheaper than for loops|3|
|[G‑17]|Use hardcode address instead address(this)|17|
|[G‑18]|Not using the named return variables when a function returns, wastes deployment gas|7|
|[G‑19]|Unnecessary computation|3|
|[G‑20]|Pre-increment and pre-decrement are cheaper than +1 ,-1|6|
|[G‑21]|Structs can be packed to use fewer storage slots|3|
|[G‑22]|abi.encode() is less efficient than abi.encodePacked()|2|
|[G‑23]|Use assembly in place of abi.decode to extract calldata values more efficiently|4|
|[G‑24]|Use of += is cheaper for mappings|2|
|[G‑25]|Use assembly to write address storage values|6|
|[G‑26]|Splitting  Require() Statements That Use  && Saves |9|
|[G‑27]|Sort Solidity operations using short-circuit mode|2|
|[G‑28]|Avoid updating storage when the value hasn't changed|12|
|[G‑29]| Multiple Address/id Mappings Can Be Combined Into A Single Mapping Of An Address/id To A Struct, Where Appropriate|2|
|[G‑30]| Use assembly to emit an event|81|
|[G‑31]|Use assembly to perform efficient back-to-back calls|17|
|[G‑32]|When possible, use assembly instead of unchecked{++i}|2|
|[G‑33]| Cache external calls outside of loop to avoid re-calling function on each iteration|1|
|[G‑34]|Expressions for constant values such as a call to¬†keccak256(), should use immutable rather than constant|4|





## [G-01] Optimize External Calls with Assembly for Memory Efficiency

Each such call involves creating a new memory location to store the data being passed, thus incurring memory expansion costs.
Inline assembly allows for optimized memory usage by re-using already allocated memory spaces or using the scratch space for smaller datasets. This can result in notable gas savings, especially for contracts that make frequent external calls.
Additionally, using inline assembly enables important safety checks like verifying if the target address has code deployed to it using extcodesize(addr) before making the call, mitigating risks associated with contract interactions.






```solidity
File:  packages/contracts/contracts/HintHelpers.sol
72              vars.currentCdpId = sortedCdps.getPrev(vars.currentCdpId);
                vars.currentCdpUser = sortedCdps.getOwnerAddress(vars.currentCdpId);


90   uint256 currentCdpDebt = cdpManager.getSyncedCdpDebt(vars.currentCdpId);

116             vars.currentCdpId = sortedCdps.getPrev(vars.currentCdpId);
                vars.currentCdpUser = sortedCdps.getOwnerAddress(vars.currentCdpId);

141   uint256 newCollShare = cdpManager.getSyncedCdpCollShares(vars.currentCdpId);

169  uint256 arrayLength = cdpManager.getActiveCdpsCount();

175  hint = sortedCdps.getLast();

185         bytes32 _cId = cdpManager.getIdFromCdpIdsArray(arrayIndex);
            uint256 currentNICR = cdpManager.getSyncedNominalICR(_cId);    

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L116-L117


```solidity
File:  packages/contracts/contracts/LeverageMacroBase.sol
143  initialCdpIndex = sortedCdps.cdpCountOf(address(this));

148  IERC3156FlashLender(address(borrowerOperations)).flashLoan(

155  IERC3156FlashLender(address(activePool)).flashLoan(

173  bytes32 cdpId = sortedCdps.cdpOfOwnerByIndex(address(this), initialCdpIndex);

187  ICdpManagerData.Cdp memory cdpInfo = cdpManager.Cdps(checkParams.cdpId);

199  ICdpManagerData.Cdp memory cdpInfo = cdpManager.Cdps(checkParams.cdpId);

220     uint256 ebtcBal = ebtcToken.balanceOf(address(this));
        uint256 collateralBal = stETH.sharesOf(address(this));

224   ebtcToken.transfer(msg.sender, ebtcBal);

228   stETH.transferShares(msg.sender, collateralBal);

237  IERC20(token).safeTransfer(msg.sender, amount);

405  IERC20(swapData.tokenForSwap).safeApprove(

427  IERC20(swapData.tokenForSwap).safeApprove(swapData.addressForApprove, 0);    
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L143


```solidity
File:  packages/contracts/contracts/LeverageMacroDelegateTarget.sol
64   address _owner = IOwnerLike(address(this)).owner();
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L64


```solidity
File:  packages/contracts/contracts/LeverageMacroReference.sol
39      ebtcToken.approve(_borrowerOperationsAddress, type(uint256).max);
        stETH.approve(_borrowerOperationsAddress, type(uint256).max);
        stETH.approve(_activePool, type(uint256).max);

57      ebtcToken.approve(address(borrowerOperations), type(uint256).max);
        stETH.approve(address(borrowerOperations), type(uint256).max);
        stETH.approve(address(activePool), type(uint256).max);        
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L39-L41





```solidity
File:  packages/contracts/contracts/Dependencies/RolesAuthority.sol
// @audit users is external
152  users.add(user);

159  users.remove(user);
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L152


```solidity
File:  packages/contracts/contracts/ActivePool.sol
183  collateral.transferShares(_account, _shares);

186  ICollSurplusPool(_account).increaseTotalSurplusCollShares(_shares);

272  uint256 oldRate = collateral.getPooledEthByShares(DECIMAL_PRECISION);

274  collateral.transfer(address(receiver), amount);

283  collateral.transferFrom(address(receiver), address(this), amountWithFee);

286   collateral.transfer(feeRecipientAddress, fee);

337  return collateral.balanceOf(address(this));

347  ICdpManagerData(cdpManagerAddress).syncGlobalAccountingAndGracePeriod(); // Calling this increases shares so do it first

362   collateral.transferShares(feeRecipientAddress, _shares);

372  ICdpManagerData(cdpManagerAddress).syncGlobalAccountingAndGracePeriod(); // Accrue State First

391  ICdpManagerData(cdpManagerAddress).syncGlobalAccountingAndGracePeriod(); // Accrue State First

405  ICdpManagerData(cdpManagerAddress).syncGlobalAccountingAndGracePeriod(); // Accrue State First

418  ICdpManagerData(cdpManagerAddress).syncGlobalAccountingAndGracePeriod(); // Accrue State First
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L183 


```solidity
File:  packages/contracts/contracts/BorrowerOperations.sol
338  address _borrower = sortedCdps.getOwnerAddress(_cdpId);

363     vars.debt = cdpManager.getCdpDebt(_cdpId);
        vars.collShares = cdpManager.getCdpCollShares(_cdpId);

422    sortedCdps.reInsert(_cdpId, newNICR, _upperHint, _lowerHint);

457    cdpManager.syncGlobalAccounting();

465     uint256 _netCollAsShares = collateral.getSharesByPooledEth(vars.netStEthBalance);
        uint256 _liquidatorRewardShares = collateral.getSharesByPooledEth(LIQUIDATOR_REWARD);

497  cdpManager.notifyStartGracePeriod(newTCR);

500  cdpManager.notifyEndGracePeriod(newTCR);

509  cdpManager.notifyEndGracePeriod(newTCR);

513  bytes32 _cdpId = sortedCdps.insert(_borrower, vars.NICR, _upperHint, _lowerHint);

554  address _borrower = sortedCdps.getOwnerAddress(_cdpId);

559   cdpManager.syncAccounting(_cdpId);

564     uint256 collShares = cdpManager.getCdpCollShares(_cdpId);
        uint256 debt = cdpManager.getCdpDebt(_cdpId);
        uint256 liquidatorRewardShares = cdpManager.getCdpLiquidatorRewardShares(_cdpId);

581     cdpManager.notifyEndGracePeriod(newTCR);

583    cdpManager.closeCdp(_cdpId, _borrower, debt, collShares);

601  collSurplusPool.claimSurplusCollShares(msg.sender);

749  collSharesChange = collateral.getSharesByPooledEth(_collReceived);

752  collSharesChange = collateral.getSharesByPooledEth(_requestedCollWithdrawal);

774  activePool.transferSystemCollShares(_varMvTokens.user, _varMvTokens.collSharesChange);

785     collateral.transferFrom(msg.sender, address(activePool), _stEthBalance);
        activePool.increaseSystemCollShares(_sharesToTrack);

791     activePool.increaseSystemDebt(_debt);
        ebtcToken.mint(_account, _debt);

797     activePool.decreaseSystemDebt(_debt);
        ebtcToken.burn(_account, _debt);        

830  uint status = cdpManager.getCdpStatus(_cdpId);

893  cdpManager.notifyStartGracePeriod(_vars.newTCR);

896  cdpManager.notifyEndGracePeriod(_vars.newTCR);

906  cdpManager.notifyEndGracePeriod(_vars.newTCR);

1057 uint256 systemStEthBalance = collateral.getPooledEthByShares(_systemCollShares);

1088  ebtcToken.mint(address(receiver), amount);

1100  ebtcToken.transferFrom(address(receiver), feeRecipientAddress, fee + amount);

1103   ebtcToken.burn(feeRecipientAddress, amount);

1146  cdpManager.syncGlobalAccounting();

1157  cdpManager.syncGlobalAccounting();

1168  cdpManager.syncGlobalAccounting();
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L338


```solidity
File: packages/contracts/contracts/CdpManager.sol
163  address _borrower = sortedCdps.getOwnerAddress(_redeemColFromCdp.cdpId);

254  activePool.decreaseSystemDebt(_EBTC);

257  collSurplusPool.increaseSurplusCollShares(_borrower, _collSurplus + _liquidatorRewardShares);

284  bytes32 nextCdp = sortedCdps.getNext(_firstRedemptionHint);

338  totals.price = priceFeed.fetchPrice();

364  currentBorrower = sortedCdps.getOwnerAddress(_firstRedemptionHint);

367  currentBorrower = sortedCdps.getOwnerAddress(_cId);

371  currentBorrower = sortedCdps.getOwnerAddress(_cId);

424       bytes32 _nextId = sortedCdps.getPrev(_cId);
          address nextUserToCheck = sortedCdps.getOwnerAddress(_nextId);

435  sortedCdps.remove(_firstRedeemed);

442  sortedCdps.batchRemove(_toRemoveIds);

475   ebtcToken.burn(msg.sender, totals.debtToRedeem);

478  activePool.decreaseSystemDebt(totals.debtToRedeem);

481  activePool.allocateSystemCollSharesToFeeRecipient(totals.feeCollShares);

484  activePool.transferSystemCollShares(msg.sender, totals.collSharesToRedeemer);

742  uint256 callerBalance = ebtcToken.balanceOf(_redeemer);
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L163


```solidity
File:  packages/contracts/contracts/CdpManagerStorage.sol
257   sortedCdps.remove(_cdpId);

494   uint256 _totalColl = collateral.getPooledEthByShares(_systemCollShares);

585   activePool.allocateSystemCollSharesToFeeRecipient(_feeTaken);

712   uint256 _underlyingCollateral = collateral.getPooledEthByShares(currentCollShare);

878   uint256 _systemCollShare = activePool.getSystemCollShares();

882   uint256 _systemDebt = activePool.getSystemDebt();
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L257


```solidity
File:  packages/contracts/contracts/CollSurplusPool.sol
107  collateral.transferShares(_account, claimableColl);
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L107



## [G‑02] Use assembly to validate msg.sender 
In Solidity, the msg.sender variable represents the address of the sender of a transaction. However, accessing msg.sender incurs a certain amount of gas cost. If gas optimization is a concern in your Solidity contract, you can use assembly code to validate the msg.sender value in a more gas-efficient manner.
We can use assembly to efficiently validate msg.sender with the least amount of opcodes necessary. 


```solidity
File:  packages/contracts/contracts/SimplifiedDiamondLike.sol
52  require(msg.sender == owner);

67   require(msg.sender == owner);

77   require(msg.sender == address(this)); // Must call this via `execute` to explicitly set the flag

111  require(msg.sender == owner, "Must be owner");
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L52


```solidity
File:  packages/contracts/contracts/SortedCdps.sol
715   require(msg.sender == address(cdpManager), "SortedCdps: Caller is not the CdpManager");

721   msg.sender == borrowerOperationsAddress || msg.sender == address(cdpManager),
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L715


```solidity
File:  packages/contracts/contracts/Dependencies/Auth.sol
45   require(msg.sender == owner || authority.canCall(msg.sender, address(this), msg.sig));
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L45


```solidity
File:  packages/contracts/contracts/ActivePool.sol
221   msg.sender == borrowerOperationsAddress,

229   msg.sender == borrowerOperationsAddress || msg.sender == cdpManagerAddress,

236   require(msg.sender == cdpManagerAddress, "ActivePool: Caller is not CdpManager");
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L221


```solidity
File:  packages/contracts/contracts/CdpManagerStorage.sol
661   msg.sender == borrowerOperationsAddress,
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L661


```solidity
File:  packages/contracts/contracts/CollSurplusPool.sol
114   msg.sender == borrowerOperationsAddress,

120   require(msg.sender == cdpManagerAddress, "CollSurplusPool: Caller is not CdpManager");

124   require(msg.sender == activePoolAddress, "CollSurplusPool: Caller is not Active Pool");
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L114


```solidity
File:  packages/contracts/contracts/EBTCToken.sol
308    msg.sender == borrowerOperationsAddress,

316             msg.sender == borrowerOperationsAddress ||
                msg.sender == cdpManagerAddress ||

324   require(msg.sender == cdpManagerAddress, "EBTC: Caller is not CdpManager");                
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L308


```solidity
File:  packages/contracts/contracts/LeverageMacroBase.sol
357     msg.sender == address(borrowerOperations),

363    msg.sender == address(activePool),
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L357





## [G‑03] Avoid contract existence checks by using low level calls

In Solidity, when interacting with other contracts, it's common to perform existence checks to ensure that the target contract exists before making function calls. However, these existence checks incur a certain amount of gas cost. To optimize gas usage, you can use low-level calls instead of high-level Solidity functions to interact with other contracts and avoid unnecessary existence checks.
Prior to 0.8.10 the compiler inserted extra code, including EXTCODESIZE (100 gas), to check for contract existence for external function calls. In more recent solidity versions, the compiler will not insert these checks if the external call has a return value. Similar behavior can be achieved in earlier versions by using low-level calls, since low level calls never check for contract existence.



```solidity
File:  packages/contracts/contracts/ActivePool.sol
60  address _authorityAddress = address(AuthNoOwner(cdpManagerAddress).authority());

186 ICollSurplusPool(_account).increaseTotalSurplusCollShares(_shares);

347  ICdpManagerData(cdpManagerAddress).syncGlobalAccountingAndGracePeriod(); // Calling this increases shares so do it first

372  ICdpManagerData(cdpManagerAddress).syncGlobalAccountingAndGracePeriod(); // Accrue State First

391  ICdpManagerData(cdpManagerAddress).syncGlobalAccountingAndGracePeriod(); // Accrue State First

405  ICdpManagerData(cdpManagerAddress).syncGlobalAccountingAndGracePeriod(); // Accrue State First

418  ICdpManagerData(cdpManagerAddress).syncGlobalAccountingAndGracePeriod(); // Accrue State First
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L60


```solidity
File:  packages/contracts/contracts/BorrowerOperations.sol
123   address _authorityAddress = address(AuthNoOwner(_cdpManagerAddress).authority());

147   ReentrancyGuard(address(cdpManager)).locked() == OPEN,
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L123


```solidity
File:  packages/contracts/contracts/CdpManager.sol
222  ISortedCdps(sortedCdps).getOwnerAddress(_redeemColFromCdp.cdpId),
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L222


```solidity
File:  packages/contracts/contracts/CdpManagerStorage.sol
392  ISortedCdps(sortedCdps).getOwnerAddress(_cdpId),
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L392


```solidity
File:  packages/contracts/contracts/CollSurplusPool.sol
52  feeRecipientAddress = IActivePool(activePoolAddress).feeRecipientAddress();

145 uint256 balance = IERC20(token).balanceOf(address(this));

148 IERC20(token).safeTransfer(feeRecipientAddress, amount);
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L52


```solidity
File:  packages/contracts/contracts/LeverageMacroBase.sol
405  IERC20(swapData.tokenForSwap).safeApprove(

427  IERC20(swapData.tokenForSwap).safeApprove(swapData.addressForApprove, 0);

441  IERC20(swapChecks[i].tokenToCheck).balanceOf(address(this)) >
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L405


```solidity
File:  packages/contracts/contracts/LeverageMacroDelegateTarget.sol
64   address _owner = IOwnerLike(address(this)).owner();
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L64




## [G-04] >= costs less gas than >


The compiler uses opcodes GT and ISZERO for solidity code that uses >, but only requires LT for >=, which saves 3 gas


```solidity
File:  packages/contracts/contracts/LiquidationLibrary.sol
476    if (_partialState.ICR > LICR) {

553    if (_ICR > LICR) {   

578    if (_ICR > LICR) {
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L476


```solidity
File:  packages/contracts/contracts/SortedCdps.sol
422   require(_len > 1, "SortedCdps: batchRemove() only apply to multiple cdpIds!");

460   if (data.size > 1) {    
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L422


```solidity
File:  packages/contracts/contracts/Dependencies/EbtcMath.sol
60   if (_minutes > 525600000) {
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L60

```solidity
File:  packages/contracts/contracts/CdpManagerStorage.sol
512   if (_newIndex > _oldIndex && totalStakes > 0) {

556   require(_newIndex > _prevIndex, "CDPManager: only take fee with bigger new index");

585   require(activePool.getSystemCollShares() > _feeTaken, "CDPManager: fee split is too big");

636    if (_scaledCdpColl > _feeSplitDistributed) {

654   CdpOwnersArrayLength > 1 && sortedCdps.getSize() > 1,

765   if (_newIndex > _oldIndex && totalStakes > 0) {
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L512




## [G-05] Amounts should be checked for 0 before calling a transfer

In Solidity, when transferring tokens or ether from one address to another, it is common to check if the transfer amount is greater than 0 before making the transfer. This check ensures that a valid transfer amount is specified and prevents unnecessary transfers of zero amounts. However, performing this check incurs additional gas cost. To optimize gas usage, you can avoid checking for zero amounts before calling the transfer function.
Checking non-zero transfer values can avoid an expensive external call and save gas.


```solidity
File:  packages/contracts/contracts/LeverageMacroBase.sol
237   IERC20(token).safeTransfer(msg.sender, amount);
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L237


```solidity
File:  packages/contracts/contracts/BorrowerOperations.sol
785   collateral.transferFrom(msg.sender, address(activePool), _stEthBalance);
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L785


```solidity
File:  packages/contracts/contracts/ActivePool.sol
381  IERC20(token).safeTransfer(cachedFeeRecipientAddress, amount);
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L381


```solidity
File:  packages/contracts/contracts/CollSurplusPool.sol
148  IERC20(token).safeTransfer(feeRecipientAddress, amount);
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L148


```solidity
File:  packages/contracts/contracts/EBTCToken.sol
121   _transfer(msg.sender, recipient, amount);

140    _transfer(sender, recipient, amount);
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L121




## [G-06] Functions guaranteed to revert when called by normal users can be marked payable

If a function modifier such as onlyOwner is used, the function will revert if a normal user tries to pay the function. Marking the function as payable will lower the gas cost 



```solidity
File:  packages/contracts/contracts/LeverageMacroBase.sol
118 function doOperation(
        FlashLoanType flType,
        uint256 borrowAmount,
        LeverageMacroOperation calldata operation,
        PostOperationCheck postCheckType,
        PostCheckParams calldata checkParams
    ) external {
        _assertOwner();

214     function sweepToCaller() public {
        _assertOwner();   

234     function sweepToken(address token, uint256 amount) public {
        _assertOwner();             
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L118-L125


```solidity
File:  packages/contracts/contracts/ActivePool.sol
157   function allocateSystemCollSharesToFeeRecipient(uint256 _shares) external override {

194   function increaseSystemDebt(uint256 _amount) external override {

207   function decreaseSystemDebt(uint256 _amount) external override {   

242   function increaseSystemCollShares(uint256 _value) external override {         
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L157


```solidity
File:  packages/contracts/contracts/EBTCToken.sol
85  function mint(address _account, uint256 _amount) external override {

95  function burn(address _account, uint256 _amount) external override {    

104  function burn(uint256 _amount) external {    
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L85





## [G-07] Structs can be modified to fit in fewer storage slots


Some member types can be safely modified, and as result, these struct will fit in fewer storage slots. Each slot saved can avoid an extra Gsset (20000 gas) for the first setting of the struct. Subsequent reads as well as writes have smaller gas savings.



```solidity
File:  packages/contracts/contracts/Interfaces/IPriceFeed.sol
    struct FallbackResponse {
        uint256 answer;
        uint256 timestamp;
        bool success;
    }
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPriceFeed.sol#L26-L30

```solidity
File:  packages/contracts/contracts/BorrowerOperations.sol
    struct AdjustCdpLocals {
        uint256 price;
        uint256 collSharesChange;
        uint256 netDebtChange;
        bool isCollIncrease;
        uint256 debt;
        uint256 collShares;
        uint256 oldICR;
        uint256 newICR;
        uint256 newTCR;
        uint256 newDebt;
        uint256 newCollShares;
        uint256 stake;
    }

    struct OpenCdpLocals {
        uint256 price;
        uint256 debt;
        uint256 netStEthBalance;
        uint256 ICR;
        uint256 NICR;
        uint256 stake;
        uint256 arrayIndex;
    }
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L72-L95


```solidity
File:  packages/contracts/contracts/Interfaces/ICdpManagerData.sol
97  struct Cdp {
        uint256 debt;
        uint256 coll;
        uint256 stake;
        uint256 liquidatorRewardShares;
        Status status;
        uint128 arrayIndex;
    }

113 struct CdpDebtAndCollShares {
        uint256 debt;
        uint256 collShares;
    }    
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L97-L104


```solidity
File:  packages/contracts/contracts/Interfaces/ICdpManagerData.sol
    struct Cdp {
        uint256 debt;
        uint256 coll;
        uint256 stake;
        uint256 liquidatorRewardShares;
        Status status;
        uint128 arrayIndex;
    }

    /*
     * --- Variable container structs for liquidations ---
     *
     * These structs are used to hold, return and assign variables inside the liquidation functions,
     * in order to avoid the error: "CompilerError: Stack too deep".
     **/

    struct CdpDebtAndCollShares {
        uint256 debt;
        uint256 collShares;
    }

    struct LiquidationLocals {
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

    struct LiquidationRecoveryModeLocals {
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

    struct LocalVariables_OuterLiquidationFunction {
        uint256 price;
        bool recoveryModeAtStart;
        uint256 liquidatedDebt;
        uint256 liquidatedColl;
    }

    struct LocalVariables_LiquidationSequence {
        uint256 i;
        uint256 ICR;
        bytes32 cdpId;
        bool backToNormalMode;
        uint256 entireSystemDebt;
        uint256 entireSystemColl;
        uint256 price;
        uint256 TCR;
    }

    struct SingleRedemptionInputs {
        bytes32 cdpId;
        uint256 maxEBTCamount;
        uint256 price;
        bytes32 upperPartialRedemptionHint;
        bytes32 lowerPartialRedemptionHint;
        uint256 partialRedemptionHintNICR;
    }

    struct LiquidationValues {
        uint256 entireCdpDebt;
        uint256 debtToBurn;
        uint256 totalCollToSendToLiquidator;
        uint256 debtToRedistribute;
        uint256 collSurplus;
        uint256 liquidatorCollSharesReward;
    }

    struct LiquidationTotals {
        uint256 totalDebtInSequence;
        uint256 totalDebtToBurn;
        uint256 totalCollToSendToLiquidator;
        uint256 totalDebtToRedistribute;
        uint256 totalCollSurplus;
        uint256 totalCollReward;
    }

    // --- Variable container structs for redemptions ---

    struct RedemptionTotals {
        uint256 remainingDebtToRedeem;
        uint256 debtToRedeem;
        uint256 collSharesDrawn;
        uint256 totalCollSharesSurplus;
        uint256 feeCollShares;
        uint256 collSharesToRedeemer;
        uint256 decayedBaseRate;
        uint256 price;
        uint256 systemDebtAtStart;
        uint256 systemCollSharesAtStart;
        uint256 tcrAtStart;
    }

    struct SingleRedemptionValues {
        uint256 debtToRedeem;
        uint256 collSharesDrawn;
        uint256 collSurplus;
        uint256 liquidatorRewardShares;
        bool cancelledPartial;
        bool fullRedemption;
    }
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L97-L215



## [G-08] Use constants instead of type(uintx).max

Using constants instead of type(uintx).max can save gas in some cases because constants are precomputed at compile-time and can be reused throughout the code, whereas type(uintx).max requires computation at runtime



```solidity
File:  packages/contracts/contracts/Governor.sol
78   for (uint8 i = 0; i < type(uint8).max; i++) {

84   for (uint8 i = 0; i < type(uint8).max; i++) {

98   for (uint8 i = 0; i < type(uint8).max; i++) {

107  for (uint8 i = 0; i < type(uint8).max; i++) {            
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L78


```solidity
File:  packages/contracts/contracts/HintHelpers.sol
79  _maxIterations = type(uint256).max;
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L79


```solidity
File:  packages/contracts/contracts/LeverageMacroReference.sol
39      ebtcToken.approve(_borrowerOperationsAddress, type(uint256).max);
        stETH.approve(_borrowerOperationsAddress, type(uint256).max);
        stETH.approve(_activePool, type(uint256).max);

53      ebtcToken.approve(address(borrowerOperations), type(uint256).max);
        stETH.approve(address(borrowerOperations), type(uint256).max);
        stETH.approve(address(activePool), type(uint256).max);        
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L39-L41


```solidity
File:  packages/contracts/contracts/BorrowerOperations.sol
1133   return type(uint112).max;
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1133


```solidity
File:  packages/contracts/contracts/CdpManager.sol
278  _maxIterations = type(uint256).max;
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L378


```solidity
File:  packages/contracts/contracts/CdpManagerStorage.sol
21  uint128 public constant UNSET_TIMESTAMP = type(uint128).max;
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L21


```solidity
File: packages/contracts/contracts/EBTCToken.sol
143  if (cachedAllowance != type(uint256).max) {
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L143



```solidity
File:  packages/contracts/contracts/SortedCdps.sol
90  _size = type(uint256).max;
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L90


```solidity
File:  packages/contracts/contracts/Dependencies/EbtcMath.sol
7  uint256 public constant MAX_TCR = type(uint256).max;
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L7




## [G-09] Using storage instead of memory for structs/arrays saves gas

 Instead of declearing the variable with the memory keyword, declaring the variable with the storage keyword and caching any fields that need to be re-read in stack variables, will be much cheaper, only incuring the Gcoldsload for the fields actually read. The only time it makes sense to read the whole struct/array into a memory variable, is if the full struct/array is being returned by the function, is being passed to a function that requires memory, or if the array/struct is being read from another memory array/struct






```solidity
File:  packages/contracts/contracts/HintHelpers.sol
62  LocalVariables_getRedemptionHints memory vars;

134 LocalVariables_getRedemptionHints memory vars,
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L62


```solidity
File:  packages/contracts/contracts/LeverageMacroBase.sol
176   ICdpManagerData.Cdp memory cdpInfo = cdpManager.Cdps(cdpId);

187   ICdpManagerData.Cdp memory cdpInfo = cdpManager.Cdps(checkParams.cdpId);

199   ICdpManagerData.Cdp memory cdpInfo = cdpManager.Cdps(checkParams.cdpId);

244   function _doCheckValueType(CheckValueAndType memory check, uint256 valueToCheck) internal {

291    function _handleOperation(LeverageMacroOperation memory operation) internal {
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L176


```solidity
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


```solidity
File:  packages/contracts/contracts/BorrowerOperations.sol
427  MoveTokensParams memory _varMvTokens = MoveTokensParams(

760  function _processTokenMovesFromAdjustment(MoveTokensParams memory _varMvTokens) internal {

856  AdjustCdpLocals memory _vars

987  AdjustCdpLocals memory vars,
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L427


```solidity
File:  packages/contracts/contracts/CdpManager.sol
136  SingleRedemptionInputs memory _redeemColFromCdp

150  CdpDebtAndCollShares memory _oldDebtAndColl = CdpDebtAndCollShares(

329   RedemptionTotals memory totals;

403   SingleRedemptionValues memory singleRedemption = _redeemCollateralFromCdp(
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L136


## [G-10] Can Make The Variable Outside The Loop To Save Gas 


By declaring the variable outside the loop, you can avoid the creation of multiple instances of the variable and reduce the gas cost of your contract.


```solidity
File:  packages/contracts/contracts/Governor.sol
47      address user = users.at(i);
48      bool _canCall = doesUserHaveRole(user, role);


58      address user = _usrs[i];
59      bool _canCall = doesUserHaveRole(user, role);
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L47-L48







## [G-11] Use Modifiers Instead of Functions To Save Gas

In Solidity, when designing contracts, it is common to use functions with conditional statements to enforce certain conditions or access controls. However, such conditional checks within functions can incur additional gas costs. To optimize gas usage, you can use modifiers instead of functions to apply conditions or access controls.


```solidity
File:  packages/contracts/contracts/EBTCToken.sol
    function _requireValidRecipient(address _recipient) internal view {
        require(
            _recipient != address(0) && _recipient != address(this),
            "EBTC: Cannot transfer tokens directly to the EBTC token contract or the zero address"
        );
        require(
            _recipient != cdpManagerAddress && _recipient != borrowerOperationsAddress,
            "EBTC: Cannot transfer tokens directly to the CdpManager or BorrowerOps"
        );
    }

    function _requireCallerIsBorrowerOperations() internal view {
        require(
            msg.sender == borrowerOperationsAddress,
            "EBTCToken: Caller is not BorrowerOperations"
        );
    }

    /// @dev authority check last to short-circuit in the case of use by usual immutable addresses
    function _requireCallerIsBOorCdpMOrAuth() internal view {
        require(
            msg.sender == borrowerOperationsAddress ||
                msg.sender == cdpManagerAddress ||
                isAuthorized(msg.sender, msg.sig),
            "EBTC: Caller is neither BorrowerOperations nor CdpManager nor authorized"
        );
    }

    function _requireCallerIsCdpM() internal view {
        require(msg.sender == cdpManagerAddress, "EBTC: Caller is not CdpManager");
    }
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L295-L325


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol
    function _assertOwner() internal {
        // Reference will compare to variable,
        require(owner() == msg.sender, "Must be owner");
    }
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L43-L46

```solidity
File:  packages/contracts/contracts/ActivePool.sol
/// @notice Checks if the caller is CdpManager
235  function _requireCallerIsCdpManager() internal view {

/// @notice Checks if the caller is either BorrowerOperations or CdpManager
227  function _requireCallerIsBOorCdpM() internal view {   


/// @notice Checks if the caller is BorrowerOperations
219  function _requireCallerIsBorrowerOperations() internal view {        
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L235








## [G-12] bytes constants are more eficient than string constans
In Solidity, bytes constants are more efficient than string constants in terms of gas usage and storage.
If the data can fit in 32 bytes, the bytes32 data type can be used instead of bytes or strings, as it is less robust in terms of robustness.


```solidity
File:  packages/contracts/contracts/EBTCToken.sol
    string internal constant _NAME = "EBTC Stablecoin";
    string internal constant _SYMBOL = "EBTC";
    string internal constant _VERSION = "1";
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L28-L30


```solidity
File:  packages/contracts/contracts/HintHelpers.sol
12   string public constant NAME = "HintHelpers";
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L12


```solidity
File:  packages/contracts/contracts/PriceFeed.sol
22  string public constant NAME = "PriceFeed";
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L22


```solidity
File:  packages/contracts/contracts/SortedCdps.sol
52   string public constant NAME = "SortedCdps";
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L52


```solidity
File:  packages/contracts/contracts/BorrowerOperations.sol
29  string public constant NAME = "BorrowerOperations";

41  string internal constant _VERSION = "1";
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L29


```solidity
File:  packages/contracts/contracts/ActivePool.sol
24  string public constant NAME = "ActivePool";
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L24


```solidity
File:  packages/contracts/contracts/CdpManagerStorage.sol
122   string public constant NAME = "CdpManager";
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L122

```solidity 
File:  packages/contracts/contracts/CollSurplusPool.sol
19  string public constant NAME = "CollSurplusPool";
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L19




## [G-13] Use assembly to hash instead of solidity

Using assembly to perform hashing operations instead of relying on Solidity's built-in hashing functions can result in gas savings in certain scenarios.


```solidity
File:  packages/contracts/contracts/EBTCToken.sol
209     bytes32 digest = keccak256(
            abi.encodePacked(
                "\x19\x01",
                domainSeparator(),
                keccak256(
                    abi.encode(_PERMIT_TYPEHASH, owner, spender, amount, _nonces[owner]++, deadline)
                )
            )
        );

240   return keccak256(abi.encode(typeHash, name, version, _chainID(), address(this)));        
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L209-L217


```solidity
File:  packages/contracts/contracts/HintHelpers.sol
182  latestRandomSeed = uint256(keccak256(abi.encodePacked(latestRandomSeed)));
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L182

```solidity
File:  packages/contracts/contracts/BorrowerOperations.sol
682   return keccak256(abi.encode(typeHash, name, version, _chainID(), address(this)));

717    bytes32 digest = keccak256(
            abi.encodePacked(
                "\x19\x01",
                domainSeparator(),
                keccak256(
                    abi.encode(
                        _PERMIT_POSITION_MANAGER_TYPEHASH,
                        _borrower,
                        _positionManager,
                        _approval,
                        _nonces[_borrower]++,
                        _deadline
                    )
                )
            )
        );


721             keccak256(
                    abi.encode(
                        _PERMIT_POSITION_MANAGER_TYPEHASH,
                        _borrower,
                        _positionManager,
                        _approval,
                        _nonces[_borrower]++,
                        _deadline
                    )
                )
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L682





## [G‑14] internal functions only called once can be inlined to save gas
Inlining internal functions that are only called once can result in gas savings in Solidity contracts.

Not inlining costs 20 to 40 gas because of two extra JUMP instructions and additional stack operations needed for function calls.


```solidity
File:  packages/contracts/contracts/BorrowerOperations.sol
760   function _processTokenMovesFromAdjustment(MoveTokensParams memory _varMvTokens) internal {

852       function _requireValidAdjustmentInCurrentMode(
        bool _isRecoveryMode,
        uint256 _stEthBalanceDecrease,
        bool _isDebtIncrease,
        AdjustCdpLocals memory _vars
    ) internal {                                                     
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L760


```solidity
File:  packages/contracts/contracts/CdpManager.sol
135      function _redeemCollateralFromCdp(
        SingleRedemptionInputs memory _redeemColFromCdp
    ) internal returns (SingleRedemptionValues memory singleRedemption) {

244      function _closeCdpByRedemption(
        bytes32 _cdpId,
        uint256 _EBTC,
        uint256 _collSurplus,
        uint256 _liquidatorRewardShares,
        address _borrower
    ) internal {

550   function _addCdpIdToArray(bytes32 _cdpId) internal returns (uint128 index) {

612      function _updateBaseRateFromRedemption(
        uint256 _ETHDrawn,
        uint256 _price,
        uint256 _totalEBTCSupply
    ) internal returns (uint256) {    

977    function _setCdpCollShares(bytes32 _cdpId, uint256 _newColl) internal {

984    function _setCdpDebt(bytes32 _cdpId, uint256 _newDebt) internal {                            
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L135


```solidity
File:  packages/contracts/contracts/CdpManagerStorage.sol
336   function _updateRedistributedDebtIndex(bytes32 _cdpId) internal {

410   function _removeStake(bytes32 _cdpId) internal {    

574   function _takeSplitAndUpdateFeePerUnit(
        uint256 _feeTaken,
        uint256 _newPerUnit,
        uint256 _newErrorPerUnit
    ) internal {  

592      function _applyAccumulatedFeeSplit(
        bytes32 _cdpId,
        uint256 _newColl,
        uint256 _feeSplitDistributed,
        uint256 _oldPerUnitCdp,
        uint256 _systemStEthFeePerUnitIndex
    ) internal {          
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L336


```solidity
File:  packages/contracts/contracts/LiquidationLibrary.sol
450     function _partiallyReduceCdpDebt(
        bytes32 _cdpId,
        uint256 _partialDebt,
        uint256 _partialColl
    ) internal {

466      function _reInsertPartialLiquidation(
        LiquidationLocals memory _partialState,
        uint256 _newNICR,
        uint256 _oldDebt,
        uint256 _oldColl
    ) internal {

642     function _getLiquidationValuesRecoveryMode(
        uint256 _price,
        uint256 _systemDebt,
        uint256 _systemCollShares,
        LocalVariables_LiquidationSequence memory vars,
        LiquidationValues memory singleLiquidation
    ) internal {

862    function _redistributeDebt(uint256 _debt) internal {                        
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L450


```solidity 
File:  packages/contracts/contracts/SimplifiedDiamondLike.sol
134  function _executeOne(Operation calldata op) internal {

174   function _fallback() internal {    
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L134


## [G-15] Use nested if statements instead of &&

If the if statement has a logical AND and is not followed by an else statement, it can be replaced with 2 if statements.




```solidity
File:  packages/contracts/contracts/PriceFeed.sol
226                if (
                    !_chainlinkIsBroken(chainlinkResponse, prevChainlinkResponse) &&
                    !_chainlinkIsFrozen(chainlinkResponse)
                ) {

372                if (
                    !_fallbackIsBroken(fallbackResponse) &&
                    !_responseTimeout(fallbackResponse.timestamp, newFallbackCaler.fallbackTimeout())
                ) {
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L226-L229

```solidity
File:  packages/contracts/contracts/SortedCdps.sol
202   if (maxNodes > 0 && i >= maxNodes) {

259   if (maxNodes > 0 && i >= maxNodes) {    

330   if (maxNodes > 0 && i >= maxNodes) {

621    if (data.head == _startId && _NICR >= cdpManager.getCachedNominalICR(_startId)) {

644   if (data.tail == _startId && _NICR <= cdpManager.getCachedNominalICR(_startId)) {
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L202


```solidity
File:  packages/contracts/contracts/BorrowerOperations.sol
393    if (!_isDebtIncrease && _debtChange > 0) {
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L393

```solidity
File:  packages/contracts/contracts/CdpManagerStorage.sol
512   if (_newIndex > _oldIndex && totalStakes > 0) {

796    if (_cdpPerUnitIdx != _systemStEthFeePerUnitIndex && _cdpPerUnitIdx > 0) {
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L512

```solidity
File:  packages/contracts/contracts/LiquidationLibrary.sol
157         if (
                liquidationValues.totalCollToSendToLiquidator == 0 &&
                liquidationValues.debtToBurn == 0
            ) {

756  if (vars.cdpId != bytes32(0) && Cdps[vars.cdpId].status == Status.active) {    

819  if (vars.cdpId != bytes32(0) && Cdps[vars.cdpId].status == Status.active) {                
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L157-L160



## [G-16] Do-While loops are cheaper than for loops

If you want to push optimization at the expense of creating slightly unconventional code, Solidity do-while loops are more gas efficient than for loops, even if you add an if-condition check for the case where the loop doesn’t execute at all.




```solidity
File:  packages/contracts/contracts/Governor.sol
        if (_sigs.length > 0) {
            _funcs = new bytes4[](_sigs.length);
            for (uint256 i = 0; i < _sigs.length; ++i) {
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L135-L137


```solidity
File:  packages/contracts/contracts/SortedCdps.sol
// @audit condition is in line 422
432  for (uint256 i = 0; i < _len; ++i) {

449  for (uint i = 0; i < _len; ++i) {    
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L432





## [G-17] Use hardcode address instead address(this)

it can be more gas-efficient to use a hardcoded address instead of the address(this) expression, especially if you need to use the same address multiple times in your contract.





```solidity
File:  packages/contracts/contracts/LeverageMacroBase.sol
131     address(this),

143  initialCdpIndex = sortedCdps.cdpCountOf(address(this));

149  IERC3156FlashBorrower(address(this)),

156  IERC3156FlashBorrower(address(this)),

173   bytes32 cdpId = sortedCdps.cdpOfOwnerByIndex(address(this), initialCdpIndex);

220   uint256 ebtcBal = ebtcToken.balanceOf(address(this));
221   uint256 collateralBal = stETH.sharesOf(address(this));

352     require(initiator == address(this), "LeverageMacroReference: wrong initiator for flashloan");

441  IERC20(swapChecks[i].tokenToCheck).balanceOf(address(this)) >

456  require(addy != address(this)); // If it could call this it could fake the forwarded caller
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L131



```solidity
File:  packages/contracts/contracts/ActivePool.sol
283   collateral.transferFrom(address(receiver), address(this), amountWithFee);

395   collateral.balanceOf(address(this)) >= collateral.getPooledEthByShares(systemCollShares),

299    collateral.sharesOf(address(this)) >= systemCollShares,

337    return collateral.balanceOf(address(this));

376   uint256 balance = IERC20(token).balanceOf(address(this));
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L283


## [G-18] Not using the named return variables when a function returns, wastes deployment gas

When a function returns multiple values without named return variables, it creates a temporary variable to hold the returned values, which can increase the deployment gas cost


```solidity
File:  packages/contracts/contracts/CdpManagerStorage.sol
306   ) internal view returns (uint256 pendingEBTCDebtReward, uint256 _debtIndexDiff) {

721   ) public view returns (uint256 pendingEBTCDebtReward) {    
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L306


```solidity
File:  packages/contracts/contracts/Governor.sol
146  function getRoleName(uint8 role) external view returns (string memory roleName) {
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L146

```solidity
File:  packages/contracts/contracts/CdpManager.sol
570   function getSystemDebt() public view returns (uint256 entireSystemDebt) {
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L570




```solidity
File:  packages/contracts/contracts/Dependencies/EbtcBase.sol
67    function getSystemCollShares() public view returns (uint256 entireSystemColl) {

75    function _getSystemDebt() internal view returns (uint256 entireSystemDebt) {    
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L67



## [G-19] Unnecessary computation

When emitting an event that includes a new and an old value, it is cheaper in gas to avoid caching the old value in memory. Instead, emit the event, then save the new value in storage.



There are 3 instances of this issue:
```solidity
File:  packages/contracts/contracts/ActivePool.sol
        uint256 _oldFee = feeBps;
        feeBps = uint16(_newFee);
        emit FlashFeeSet(msg.sender, _oldFee, _newFee);
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L410-L412


```solidity
File:  packages/contracts/contracts/BorrowerOperations.sol
        uint256 _oldFee = feeBps;
        feeBps = uint16(_newFee);
        emit FlashFeeSet(msg.sender, _oldFee, _newFee);
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1160-L1162


```solidity
File:  packages/contracts/contracts/PriceFeed.sol
            address oldFallbackCaller = address(fallbackCaller);
            // NOTE: assume intentionally bricking fallback!!!
            fallbackCaller = newFallbackCaler;
            emit FallbackCallerChanged(oldFallbackCaller, _fallbackCaller);
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L384-L387




## [G-20] Pre-increment and pre-decrement are cheaper than +1 ,-1

In certain cases, using pre-increment and pre-decrement operators (++i, --i) can be cheaper in terms of gas consumption compared to using the addition (+) and subtraction (-) operators with a value of 1 (+1, -1) in Solidity contracts.


```solidity
File:  packages/contracts/contracts/CdpManager.sol
421  _numCdpsFullyRedeemed = _numCdpsFullyRedeemed + 1;

499   _cnt = _cnt - 1;
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L421


```solidity
File:  packages/contracts/contracts/SortedCdps.sol
193  _currentIndex = _currentIndex + 1;

251  _ownedCount = _ownedCount + 1;

404   data.size = data.size + 1;
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L193


```solidity
File:  packages/contracts/contracts/CdpManagerStorage.sol
473  uint256 idxLast = length - 1;
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager



## [G-21] Structs can be packed to use fewer storage slots

The EVM works with 32 byte words. Variables less than 32 bytes can be declared next to each other in storage and this will pack the values together into a single 32 byte storage slot (if values combined are <= 32 bytes). If the variables packed together are retrieved together in functions (more likely with structs) we will effectively save ~2000 gas with every subsequent SLOAD for that storage slot. This is due to us incurring a Gwarmaccess (100 gas) versus a Gcoldsload (2100 gas).


```solidity
File:  packages/contracts/contracts/BorrowerOperations.sol
    struct MoveTokensParams {
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
File:  packages/contracts/contracts/SimplifiedDiamondLike.sol
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
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L99-107


```solidity
File:  packages/contracts/contracts/Interfaces/IPriceFeed.sol
17  struct ChainlinkResponse {
        uint80 roundEthBtcId;
        uint80 roundStEthEthId;
        uint256 answer;
        uint256 timestampEthBtc;
        uint256 timestampStEthEth;
        bool success;
    }
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPriceFeed.sol#L17


Storage.sol#L473

## [G-22] abi.encode() is less efficient than abi.encodePacked()

In terms of efficiency, abi.encodePacked() is generally considered to be more gas-efficient than abi.encode(), 


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol
152   abi.encode(operation)

159    abi.encode(operation)
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L152



## [G-23] Use assembly in place of abi.decode to extract calldata values more efficiently

Instead of using abi.decode, we can use assembly to decode our desired calldata values directly. This will allow us to avoid decoding calldata values that we will not use.


```solidity
File:  packages/contracts/contracts/LeverageMacroBase.sol
339  LeverageMacroOperation memory leverageMacroData = abi.decode(data, (LeverageMacroOperation));

461  OpenCdpOperation memory flData = abi.decode(data, (OpenCdpOperation));

475  CloseCdpOperation memory flData = abi.decode(data, (CloseCdpOperation));

483  AdjustCdpOperation memory flData = abi.decode(data, (AdjustCdpOperation));
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L339



## [G-24] Use of += is cheaper for mappings



```solidity
File:  packages/contracts/contracts/EBTCToken.sol
258   _balances[recipient] = _balances[recipient] + amount;

266   _balances[account] = _balances[account] + amount;
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L258




## [G-25] Use assembly to write address storage values

By using assembly to write to address storage values, you can bypass some of these operations and lower the gas cost of writing to storage. Assembly code allows you to directly access the Ethereum Virtual Machine (EVM) and perform low-level operations that are not possible in Solidity.


```solidity
File:  packages/contracts/contracts/BorrowerOperations.sol
121  feeRecipientAddress = _feeRecipientAddress;

1148 feeRecipientAddress = _feeRecipientAddress;
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L121

```solidity
File:  packages/contracts/contracts/Dependencies/Auth.sol
19  owner = _owner;

53  owner = newOwner;
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L19

```solidity
File: packages/contracts/contracts/ActivePool.sol
57   feeRecipientAddress = _feeRecipientAddress;

398  feeRecipientAddress = _feeRecipientAddress;
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L57






## [G-26] Splitting  Require() Statements That Use  && Saves 


Instead of using operator && on a single require. Using a two require can save more gas.

```solidity
File:  packages/contracts/contracts/BorrowerOperations.sol
734     require(
            recoveredAddress != address(0) && recoveredAddress == _borrower,
            "BorrowerOperations: Invalid signature"
        );
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L734-L737


```solidity 
File:  packages/contracts/contracts/CdpManager.sol
762      require(
            _maxFeePercentage >= redemptionFeeFloor && _maxFeePercentage <= DECIMAL_PRECISION,
            "Max fee percentage must be between redemption fee floor and 100%"
        );
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L762-L765


```solidity
File:  packages/contracts/contracts/CdpManagerStorage.sol
261     require(
            closedStatus != Status.nonExistent && closedStatus != Status.active,
            "CdpManagerStorage: close non-exist or non-active CDP!"
        );

466     require(
            cdpStatus != Status.nonExistent && cdpStatus != Status.active,
            "CdpManagerStorage: remove non-exist or non-active CDP!"
        );      


653     require(
            CdpOwnersArrayLength > 1 && sortedCdps.getSize() > 1,
            "CdpManager: Only one cdp in the system"
        );  

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L261


```solidity
File:  packages/contracts/contracts/EBTCToken.sol
296     require(
            _recipient != address(0) && _recipient != address(this),
            "EBTC: Cannot transfer tokens directly to the EBTC token contract or the zero address"
        );

300     require(
            _recipient != cdpManagerAddress && _recipient != borrowerOperationsAddress,
            "EBTC: Cannot transfer tokens directly to the CdpManager or BorrowerOps"
        );        
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L296-L303




```solidity
File:  packages/contracts/contracts/PriceFeed.sol
79          require(
            !_chainlinkIsBroken(chainlinkResponse, prevChainlinkResponse) &&
                !_chainlinkIsFrozen(chainlinkResponse),
            "PriceFeed: Chainlink must be working and current"
        );

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L79-L83


## [G-27] Sort Solidity operations using short-circuit mode

Short-circuiting is a solidity contract development model that uses OR/AND logic to sequence different cost operations. It puts low gas cost operations in the front and high gas cost operations in the back, so that if the front is low If the cost operation is feasible, you can skip (short-circuit) the subsequent high-cost Ethereum virtual machine operation.



```solidity
File:  packages/contracts/contracts/SortedCdps.sol
// @audit data is state access of state use more gas but cdpManager is IMMUTABLE
621   if (data.head == _startId && _NICR >= cdpManager.getCachedNominalICR(_startId)) {

644   if (data.tail == _startId && _NICR <= cdpManager.getCachedNominalICR(_startId)) {    
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L621




## [G‑28] Avoid updating storage when the value hasn't changed

Manipulating storage in solidity is gas-intensive. It can be optimized by avoiding unnecessary storage updates when the new value equals the existing value.



```solidity
File:  packages/contracts/contracts/CdpManagerStorage.sol
118  recoveryModeGracePeriodDuration = _gracePeriod;
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L118


```solidity
File:  packages/contracts/contracts/PriceFeed.sol
554  lastGoodPrice = _currentPrice;
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L554


```solidity
File:  packages/contracts/contracts/ActivePool.sol
110  systemCollShares = cachedSystemCollShares;

143  systemCollShares = cachedSystemCollShares;

168   systemCollShares = cachedSystemCollShares;

171   feeRecipientCollShares = cachedFeeRecipientCollShares;

199    systemDebt = cachedSystemDebt;

212    systemDebt = cachedSystemDebt;

246  systemCollShares = cachedSystemCollShares;

359  feeRecipientCollShares = cachedFeeRecipientCollShares;
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L110











## [G-29] Multiple Address/id Mappings Can Be Combined Into A Single Mapping Of An Address/id To A Struct, Where Appropriate

Saves a storage slot for the mapping. Depending on the circumstances and sizes of types, can avoid a Gsset (20000 gas) per mapping combined. Reads and subsequent writes can also be cheaper when a function requires both values and they both fit in the same storage slot. 


```solidity
File:  packages/contracts/contracts/Dependencies/RolesAuthority.sol
    mapping(address => bytes32) public getUserRoles;

    mapping(address => mapping(bytes4 => CapabilityFlag)) public capabilityFlag;

    mapping(address => mapping(bytes4 => bytes32)) public getRolesWithCapability;
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L32-L36


```solidity
File:  packages/contracts/contracts/EBTCToken.sol
51  mapping(address => uint256) private _balances;
52  mapping(address => mapping(address => uint256)) private _allowances;
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L51-L52




## [G-30] Use assembly to emit an event

To efficiently emit events, it's possible to utilize assembly by making use of scratch space and the free memory pointer. This approach has the advantage of potentially avoiding the costs associated with memory expansion.



```Solidity
File: contracts/contracts/CdpManagerStorage.sol

50:         emit TCRNotified(_tcr);
55:         emit GracePeriodStart();
64:         emit TCRNotified(_tcr);
69:         emit GracePeriodEnd();
414:        emit TotalStakesUpdated(_newTotalStakes);
425:        emit TotalStakesUpdated(_newTotalStakes);
481:        emit CdpArrayIndexUpdated(idToMove, index);
542:        emit StEthIndexUpdated(_oldIndex, _newIndex, block.timestamp);
587:        emit CollateralFeePerUnitUpdated(_oldPerUnit, _newPerUnit, _feeTaken);
602:        emit CdpFeeSplitApplied(
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L50

&nbsp;

```Solidity
File: contracts/contracts/LiquidationLibrary.sol

238:        emit CdpUpdated(
281:        emit CdpLiquidated(
312:        emit CdpUpdated(
367:        emit CdpLiquidated(
437:        emit CdpPartiallyLiquidated(
490:        emit CdpUpdated(
516:        emit Liquidation(totalDebtToBurn, totalCollSharesToSend, totalLiquidatorRewardCollShares);
```

&nbsp;https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L238

```Solidity
File: /contracts/contracts/CdpManager.sol

55:         emit StakingRewardSplitSet(stakingRewardSplit);
179:        emit CdpUpdated(
220:        emit CdpUpdated(
466:        emit Redemption(
545:        emit CdpUpdated(_cdpId, _borrower, msg.sender, _debt, _coll, 0, 0, 0, CdpOperation.closeCdp);
630:        emit BaseRateUpdated(newBaseRate);
681:        emit BaseRateUpdated(decayedBaseRate);
698:        emit LastRedemptionTimestampUpdated(block.timestamp);
782:        emit StakingRewardSplitSet(_stakingRewardSplit);
801:        emit RedemptionFeeFloorSet(_redemptionFeeFloor);
824:        emit MinuteDecayFactorSet(_minuteDecayFactor);
836:        emit BetaSet(_beta);
848:        emit RedemptionsPaused(_paused);
925:        emit CdpUpdated(
961:        emit CdpUpdated(
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L55

```Solidity
File: contracts/contracts/BorrowerOperations.sol

136:        emit FeeRecipientAddressChanged(_feeRecipientAddress);
641:        emit PositionManagerApprovalSet(_borrower, _positionManager, _approval);
1105:        emit FlashLoanSuccess(address(receiver), token, amount, fee);
1149:        emit FeeRecipientAddressChanged(_feeRecipientAddress);
1162:        emit FlashFeeSet(msg.sender, _oldFee, _newFee);
1171:        emit FlashLoansPaused(msg.sender, _paused);
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L136

```Solidity
File: packages/contracts/contracts/ActivePool.sol

65:         emit FeeRecipientAddressChanged(_feeRecipientAddress);
112:        emit SystemCollSharesUpdated(cachedSystemCollShares);
113:        emit CollSharesTransferred(_account, _shares);
145:        emit SystemCollSharesUpdated(cachedSystemCollShares);
146:        emit CollSharesTransferred(_account, totalShares);
173:        emit SystemCollSharesUpdated(cachedSystemCollShares);
174:        emit FeeRecipientClaimableCollSharesIncreased(cachedFeeRecipientCollShares, _shares);
200:        emit ActivePoolEBTCDebtUpdated(cachedSystemDebt);
213:        emit ActivePoolEBTCDebtUpdated(cachedSystemDebt);
247:        emit SystemCollSharesUpdated(cachedSystemCollShares);
307:        emit FlashLoanSuccess(address(receiver), token, amount, fee);
360:        emit FeeRecipientClaimableCollSharesDecreased(cachedFeeRecipientCollShares, _shares);
383:        emit SweepTokenSuccess(token, amount, cachedFeeRecipientAddress);
399:        emit FeeRecipientAddressChanged(_feeRecipientAddress);
412:        emit FlashFeeSet(msg.sender, _oldFee, _newFee);
421:        emit FlashLoansPaused(msg.sender, _paused);
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L65

```Solidity
File: contracts/Dependencies/Auth.sol

22:   emit OwnershipTransferred(msg.sender, _owner);
23:   emit AuthorityUpdated(msg.sender, _authority);

49:   emit AuthorityUpdated(msg.sender, newAuthority);
50:   emit OwnershipTransferred(msg.sender, newOwner);
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L22

```Solidity
file: contracts/Dependencies/AuthNoOwner.sol

50:   emit AuthorityUpdated(msg.sender, Authority(newAuthority));
62:   emit AuthorityUpdated(address(this), Authority(newAuthority));
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L50

&nbsp;

```Solidity
File: contracts/Dependencies/RolesAuthority.sol

101:        emit PublicCapabilityUpdated(target, functionSig, enabled);
129:        emit RoleCapabilityUpdated(role, target, functionSig, enabled);
140:        emit CapabilityBurned(target, functionSig);
163:        emit UserRoleUpdated(user, role, enabled);
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L101

```Solidity
File: contracts/contracts/PriceFeed.sol

378:                emit FallbackCallerChanged(oldFallbackCaller, _fallbackCaller);
381:                emit UnhealthyFallbackCaller(_fallbackCaller, block.timestamp);
387:                emit FallbackCallerChanged(oldFallbackCaller, _fallbackCaller);
542:                emit PriceFeedStatusChanged(_status);
555:               emit LastGoodPriceUpdated(_currentPrice);
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L378

```Solidity
157:        emit RoleNameSet(role, roleName);
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L157

```Solidity
File: contracts/contracts/EBTCToken.sol

259:        emit Transfer(sender, recipient, amount);
267:        emit Transfer(address(0), account, amount);
282:        emit Transfer(account, address(0), amount);
290:	    emit Approval(owner, spender, amount);
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L259

```Solidity
File: contracts/contracts/CollSurplusPool.sol

83:        emit SurplusCollSharesUpdated(_account, newAmount);
95:        emit SurplusCollSharesUpdated(_account, 0);
104:        emit CollSharesTransferred(_account, claimableColl);
150:        emit SweepTokenSuccess(token, amount, feeRecipientAddress);
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L83




## [G-31] Use assembly to perform efficient back-to-back calls


If a similar external call is performed back-to-back, we can use assembly to reuse any function signatures and function parameters that stay the same. In addition, we can also reuse the same memory space for each function call (scratch space + free memory pointer + zero slot), which can potentially allow us to avoid memory expansion costs.
There are 11 instances of this issue:

```solidity
File:  packages/contracts/contracts/Dependencies/RolesAuthority.sol
116    if (!targets.contains(target)) {
117       targets.add(target);

151    if (!users.contains(user)) {
152       users.add(user);
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L116-L117


```solidity
File:  packages/contracts/contracts/BorrowerOperations.sol
465     uint256 _netCollAsShares = collateral.getSharesByPooledEth(vars.netStEthBalance);
466     uint256 _liquidatorRewardShares = collateral.getSharesByPooledEth(LIQUIDATOR_REWARD);

564     uint256 collShares = cdpManager.getCdpCollShares(_cdpId);
        uint256 debt = cdpManager.getCdpDebt(_cdpId);
        uint256 liquidatorRewardShares = cdpManager.getCdpLiquidatorRewardShares(_cdpId);

581     cdpManager.notifyEndGracePeriod(newTCR);

583     cdpManager.closeCdp(_cdpId, _borrower, debt, collShares);    
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L465-L466


```solidity
File:  packages/contracts/contracts/CdpManager.sol
424             bytes32 _nextId = sortedCdps.getPrev(_cId);
                address nextUserToCheck = sortedCdps.getOwnerAddress(_nextId);

478     activePool.decreaseSystemDebt(totals.debtToRedeem);

        // Allocate the stETH fee to the FeeRecipient
        activePool.allocateSystemCollSharesToFeeRecipient(totals.feeCollShares);

        // CEI: Send the stETH drawn to the redeemer
        activePool.transferSystemCollShares(msg.sender, totals.collSharesToRedeemer);                
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L424-L425


```solidity
File:  packages/contracts/contracts/HintHelpers.sol
116             vars.currentCdpId = sortedCdps.getPrev(vars.currentCdpId);
                vars.currentCdpUser = sortedCdps.getOwnerAddress(vars.currentCdpId);

185         bytes32 _cId = cdpManager.getIdFromCdpIdsArray(arrayIndex);
            uint256 currentNICR = cdpManager.getSyncedNominalICR(_cId);                
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L116-L117


```solidity
File:  packages/contracts/contracts/LeverageMacroReference.sol
40      stETH.approve(_borrowerOperationsAddress, type(uint256).max);
        stETH.approve(_activePool, type(uint256).max);

54      stETH.approve(address(borrowerOperations), type(uint256).max);
        stETH.approve(address(activePool), type(uint256).max);        
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L40-L41










## [G-32] When possible, use assembly instead of unchecked{++i}

You can also use unchecked{++i;} for even more gas savings but this will not check to see if i overflows.


```solidity 
File:  packages/contracts/contracts/SimplifiedDiamondLike.sol
117         unchecked {
                ++i;
            }
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L117-L119


```solidity
File:  packages/contracts/contracts/LeverageMacroBase.sol
387         unchecked {
                ++i;
            }
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L387-L389





## [G-33] Cache external calls outside of loop to avoid re-calling function on each iteration




```solidity
File:  packages/contracts/contracts/Governor.sol
46        for (uint256 i = 0; i < users.length(); i++) {
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L46-47

```diff
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




## [G-34] Expressions for constant values such as a call to¬†keccak256(), should use immutable rather than constant

The reason for this is that constant variables are evaluated at runtime and their value is included in the bytecode of the contract. This means that any expensive operations performed as part of the constant expression, such as a call to keccak256(), will be executed every time the contract is deployed, even if the result is always the same. This can result in higher gas costs.




```solidity
File:  packages/contracts/contracts/BorrowerOperations.sol
32      bytes32 private constant _PERMIT_POSITION_MANAGER_TYPEHASH =
        keccak256(
            "PermitPositionManagerApproval(address borrower,address positionManager,uint8 status,uint256 nonce,uint256 deadline)"
        );
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L32-L35


```solidity
File:  packages/contracts/contracts/LeverageMacroBase.sol
37   bytes32 constant FLASH_LOAN_SUCCESS = keccak256("ERC3156FlashBorrower.onFlashLoan");
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L37


```solidity
File:  packages/contracts/contracts/SimplifiedDiamondLike.sol
39   bytes32 constant DIAMOND_STORAGE_POSITION = keccak256("diamond.standard.diamond.storage");
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L39


```solidity
File:  packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol
11  bytes32 public constant FLASH_SUCCESS_VALUE = keccak256("ERC3156FlashBorrower.onFlashLoan");
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L11