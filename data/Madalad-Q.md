# QA Report

## Low Risk
| |Issue|Instances|
|:-:|:-|:-:|
|[[L-01]](#l-01-potential-dos-if-constantimmutable-address-becomes-blacklisted)|Potential DOS if `constant`/`immutable` address becomes blacklisted|1|
|[[L-02]](#l-02-chainlink-aggregators-return-the-incorrect-price-if-it-drops-below-minanswer)|Chainlink aggregators return the incorrect price if it drops below `minAnswer`|3|
|[[L-03]](#l-03-fee-on-transferrebasing-tokens-not-properly-accounted-for)|Fee on transfer/rebasing tokens not properly accounted for|3|
|[[L-04]](#l-04-user-facing-functions-should-have-address0-checks)|User facing functions should have `address(0)` checks|38|
|[[L-05]](#l-05-missing-address0-checks-when-assigning-to-address-state-variables)|Missing `address(0)` checks when assigning to `address` state variables|1|
|[[L-06]](#l-06-approval-may-revert-if-current-allowance-is-non-zero)|Approval may revert if current allowance is non-zero|1|
|[[L-07]](#l-07-use-require-instead-of-assert)|Use `require` instead of `assert`|1|
|[[L-08]](#l-08-missing-contract-existence-check-for-yul-call)|Missing contract existence check for yul `call`|3|
|[[L-09]](#l-09-lack-of-two-step-update-for-critical-functions)|Lack of two-step update for critical functions|17|
|[[L-10]](#l-10-contract-deployment-is-vulnerable-to-block-re-orgs)|Contract deployment is vulnerable to block re-orgs|1|
|[[L-11]](#l-11-division-before-multiplications-leads-to-precision-loss)|Division before multiplications leads to precision loss|1|
|[[L-12]](#l-12-numbers-downcast-to-address-may-result-in-collisions)|Numbers downcast to `address` may result in collisions|1|
|[[L-13]](#l-13-decimals-is-not-part-of-the-erc20-standard)|`decimals()` is not part of the ERC20 standard|4|
|[[L-14]](#l-14-erc20-may-revert-on-zero-transfer)|ERC20 may revert on zero transfer|7|
|[[L-15]](#l-15-soliditys-ecrecover-is-vulnerable-to-signature-malleability)|Solidity's `ecrecover` is vulnerable to signature malleability|2|
|[[L-16]](#l-16-consider-bounding-input-array-length)|Consider bounding input array length|6|
|[[L-17]](#l-17-functions-that-do-not-handle-msgvalue-should-not-be-payable)|Functions that do not handle `msg.value` should not be `payable`|1|
|[[L-18]](#l-18-functions-transferring-tokens-that-may-have-hooks-are-missing-reentrancy-guards)|Functions transferring tokens that may have hooks are missing reentrancy guards|7|
|[[L-19]](#l-19-incorrect-bips-value-used)|Incorrect bips value used|1|
|[[L-20]](#l-20-some-tokens-do-not-consider-typeuint256max-as-an-infinite-approval)|Some tokens do not consider `type(uint256).max` as an infinite approval|6|
|[[L-21]](#l-21-cap-state-variables-at-reasonable-values)|Cap state variables at reasonable values|4|
|[[L-22]](#l-22-checks-effects-interactions-pattern-not-followed)|Checks-Effects-Interactions pattern not followed|4|
|[[L-23]](#l-23-some-tokens-may-revert-on-large-approvals)|Some tokens may revert on large approvals|1|
|[[L-24]](#l-24-some-tokens-may-revert-on-large-transfers)|Some tokens may revert on large transfers|10|
|[[L-25]](#l-25-nft-contract-redefines-_mint_safemint-but-not-both)|NFT contract redefines `_mint()`/`_safeMint()`, but not both|1|
|[[L-26]](#l-26-minting-to-address-zero-should-be-prevented)|Minting to address zero should be prevented|1|
|[[L-27]](#l-27-potential-division-by-zero)|Potential division by zero|3|
|[[L-28]](#l-28-possible-loss-of-precision)|Possible loss of precision|30|
|[[L-29]](#l-29-safeapprove-is-deprecated)|`safeApprove` is deprecated|2|
|[[L-30]](#l-30-use-safetransfer-instead-of-transfer-for-token-transfers)|Use `safeTransfer` instead of `transfer` for token transfers|6|
|[[L-31]](#l-31-subtraction-may-underflow-if-result-of-multiplication-is-too-large)|Subtraction may underflow if result of multiplication is too large|2|
|[[L-32]](#l-32-removeresolve-open-todos)|Remove/Resolve open TODOs|1|
|[[L-33]](#l-33-downcasting-uint-or-int-may-result-in-overflow)|Downcasting `uint` or `int` may result in overflow|1|
|[[L-34]](#l-34-use-of-approve-is-discouraged)|Use of `approve` is discouraged|8|
|[[L-35]](#l-35-missing-address0-checks-in-constructorinitialize)|Missing `address(0)` checks in constructor/initialize|16|

Total issues: 35

Total instances: 195

## Non-Critical
| |Issue|Instances|
|:-:|:-|:-:|
|[[N-01]](#n-01-cast-to-bytes-or-bytes32-explicitly-instead-of-using-abiencodepacked)|Cast to `bytes` or `bytes32` explicitly instead of using `abi.encodePacked`|1|
|[[N-02]](#n-02-not-using-the-named-return-variable-anywhere-in-the-function-is-confusing)|Not using the named return variable anywhere in the function is confusing|8|
|[[N-03]](#n-03-use-modifiers-for-address-checks)|Use modifiers for address checks|21|
|[[N-04]](#n-04-inline-assembly-should-contain-extensive-comments)|Inline assembly should contain extensive comments|1|
|[[N-05]](#n-05-consider-adding-denylist)|Consider adding denylist|1|
|[[N-06]](#n-06-functions-missing-empty-bytes-check)|Functions missing empty `bytes` check|52|
|[[N-07]](#n-07-comparisons-should-place-constants-on-the-left-hand-side)|Comparisons should place constants on the left hand side|35|
|[[N-08]](#n-08-use-enum-values-instead-of-constant-array-indexes)|Use enum values instead of constant array indexes|2|
|[[N-09]](#n-09-variable-names-for-constant-variables-should-be-in-constant_case)|Variable names for `constant` variables should be in CONSTANT_CASE|1|
|[[N-10]](#n-10-do-not-calculate-constants)|Do not calculate constants|1|
|[[N-11]](#n-11-contract-name-not-following-solidity-style-guide)|Contract name not following Solidity style guide|1|
|[[N-12]](#n-12-missing-contract-natspec)|Missing contract NatSpec|2|
|[[N-13]](#n-13-contracts-should-expose-an-interface)|Contracts should expose an `interface`|9|
|[[N-14]](#n-14-contract-does-not-follow-suggested-layout-ordering)|Contract does not follow suggested layout ordering|3|
|[[N-15]](#n-15-control-structures-do-not-follow-the-solidity-style-guide)|Control structures do not follow the Solidity style guide|7|
|[[N-16]](#n-16-complex-casting)|Complex casting|1|
|[[N-17]](#n-17-duplicated-requirerevert-checks-should-be-refactored-to-a-modifier-or-function)|Duplicated `require`/`revert` checks should be refactored to a modifier or function|4|
|[[N-18]](#n-18-redundant-else-block)|Redundant `else` block|8|
|[[N-19]](#n-19-events-may-be-emitted-out-of-order-due-to-reentrancy)|Events may be emitted out of order due to reentrancy|17|
|[[N-20]](#n-20-event-missing-msgsender-parameter)|Event missing `msg.sender` parameter|54|
|[[N-21]](#n-21-events-should-use-parameters)|Events should use parameters|2|
|[[N-22]](#n-22-use-indexed-for-event-parameters)|Use `indexed` for event parameters|26|
|[[N-23]](#n-23-avoid-function-calls-within-for-loops)|Avoid function calls within for loops|6|
|[[N-24]](#n-24-function-names-should-use-mixedcase)|Function names should use mixedCase|5|
|[[N-25]](#n-25-functions-that-alter-state-should-emit-events)|Functions that alter state should emit events|6|
|[[N-26]](#n-26-function-order-doesnt-follow-solidity-style-guide)|Function order doesn't follow Solidity style guide|15|
|[[N-27]](#n-27-high-cyclomatic-complexity-in-functions)|High Cyclomatic Complexity in Functions|12|
|[[N-28]](#n-28-address-parameters-should-be-sanitized)|`address` parameters should be sanitized|82|
|[[N-29]](#n-29-use-ternary-expressions-over-ifelse-where-possible)|Use ternary expressions over `if`/`else` where possible|4|
|[[N-30]](#n-30-variable-names-for-immutable-variables-should-be-in-constant_case)|Variable names for `immutable` variables should be in CONSTANT_CASE|44|
|[[N-31]](#n-31-visibility-should-be-explicitly-set-rather-than-defaulting-to-internal)|Visibility should be explicitly set rather than defaulting to `internal`|6|
|[[N-32]](#n-32-imports-could-be-organized-more-systematically)|Imports could be organized more systematically|11|
|[[N-33]](#n-33-place-interface-files-into-a-dedicated-folder)|Place `interface` files into a dedicated folder|13|
|[[N-34]](#n-34-complex-functions-should-include-comments)|Complex functions should include comments|2|
|[[N-35]](#n-35-place-library-files-into-a-dedicated-folder)|Place `library` files into a dedicated folder|1|
|[[N-36]](#n-36-lines-too-long)|Lines too long|269|
|[[N-37]](#n-37-use-bit-shifts-to-improve-readability)|Use bit shifts to improve readability|1|
|[[N-38]](#n-38-use-constants-rather-than-magic-numbers)|Use constants rather than magic numbers|6|
|[[N-39]](#n-39-functions-prone-to-reentrancy-should-use-nonreentrant)|Functions prone to reentrancy should use `nonReentrant`|7|
|[[N-40]](#n-40-import-specific-identifiers-rather-than-the-whole-file)|Import specific identifiers rather than the whole file|96|
|[[N-41]](#n-41-multiple-addressid-mappings-can-be-combined-into-a-single-mapping-of-an-addressid-to-a-struct-for-readability)|Multiple address/ID mappings can be combined into a single mapping of an address/ID to a struct, for readability|9|
|[[N-42]](#n-42-use-named-function-calls)|Use named function calls|104|
|[[N-43]](#n-43-use-named-parameters-for-mappings)|Use named parameters for mappings|14|
|[[N-44]](#n-44-natspec-notice-missing-from-contract)|NatSpec `@notice` missing from contract|14|
|[[N-45]](#n-45-event-declarations-missing-natspec)|Event declarations missing NatSpec|47|
|[[N-46]](#n-46-natspec-notice-missing-from-function)|NatSpec `@notice` missing from function|122|
|[[N-47]](#n-47-natspec-author-missing)|NatSpec `@author` missing|16|
|[[N-48]](#n-48-natspec-dev-missing)|NatSpec `@dev` missing|10|
|[[N-49]](#n-49-functions-missing-natspec)|Functions missing NatSpec|139|
|[[N-50]](#n-50-natspec-param-missing)|NatSpec `@param` missing|49|
|[[N-51]](#n-51-natspec-return-missing)|NatSpec `@return` missing|23|
|[[N-52]](#n-52-natspec-title-missing)|NatSpec `@title` missing|10|
|[[N-53]](#n-53-non-external-function-names-should-begin-with-an-underscore)|Non-external function names should begin with an underscore|4|
|[[N-54]](#n-54-non-external-variable-names-should-begin-with-an-underscore)|Non-external variable names should begin with an underscore|17|
|[[N-55]](#n-55-consider-adding-emergency-pause-functionality)|Consider adding emergency pause functionality|3|
|[[N-56]](#n-56-execution-at-deadlines-should-be-allowed)|Execution at deadlines should be allowed|19|
|[[N-57]](#n-57-avoid-overly-complicated-arithmetic)|Avoid overly complicated arithmetic|1|
|[[N-58]](#n-58-use-existing-ownable-implementation)|Use existing `Ownable` implementation|1|
|[[N-59]](#n-59-function-parameters-should-be-named-using-mixedcase)|Function parameters should be named using mixedCase|1|
|[[N-60]](#n-60-avoid-polymorphic-functions)|Avoid polymorphic functions|6|
|[[N-61]](#n-61-public-functions-not-called-internally-should-be-declared-external)|`public` functions not called internally should be declared `external`|28|
|[[N-62]](#n-62-pure-function-accesses-storage)|`pure` function accesses storage|1|
|[[N-63]](#n-63-use-the-latest-solidity-version-0820-for-l2s)|Use the latest Solidity version (<0.8.20 for L2s)|39|
|[[N-64]](#n-64-redundant-boolean-literal-comparison)|Redundant boolean literal comparison|1|
|[[N-65]](#n-65-redundant-getter-functions)|Redundant getter functions|1|
|[[N-66]](#n-66-adding-a-return-statement-when-the-function-defines-a-named-return-variable-is-redundant)|Adding a `return` statement when the function defines a named return variable is redundant|13|
|[[N-67]](#n-67-use-descriptive-reason-strings-for-requirerevert)|Use descriptive reason strings for `require`/`revert`|12|
|[[N-68]](#n-68-use-a-struct-instead-of-returning-multiple-values)|Use a `struct` instead of returning multiple values|39|
|[[N-69]](#n-69-use-scientific-notationunderscores-for-large-values)|Use scientific notation/underscores for large values|3|
|[[N-70]](#n-70-events-regarding-variable-changes-should-emit-both-old-and-new-values)|Events regarding variable changes should emit both old and new values|8|
|[[N-71]](#n-71-setter-does-not-check-that-value-is-changed)|Setter does not check that value is changed|17|
|[[N-72]](#n-72-use-single-file-for-all-system-wide-constants)|Use single file for all system-wide constants|40|
|[[N-73]](#n-73-state-variable-declaration-should-include-comments)|State variable declaration should include comments|81|
|[[N-74]](#n-74-structs-enums-events-and-errors-should-be-named-using-capwords-style)|Structs, enums, events and errors should be named using CapWords style|4|
|[[N-75]](#n-75-overflows-in-unchecked-blocks)|Overflows in unchecked blocks|1|
|[[N-76]](#n-76-use-uint256-over-uint)|Use `uint256` over `uint`|31|
|[[N-77]](#n-77-unclear-error-messages)|Unclear error messages|2|
|[[N-78]](#n-78-large-numeric-literals-should-use-underscores)|Large numeric literals should use underscores|8|
|[[N-79]](#n-79-use-inline-comments-for-unnamed-variables)|Use inline comments for unnamed variables|1|
|[[N-80]](#n-80-remove-unused-imports)|Remove unused imports|22|
|[[N-81]](#n-81-unused-local-variable)|Unused local variable|2|
|[[N-82]](#n-82-unused-state-variables)|Unused state variables|8|
|[[N-83]](#n-83-unused-struct-definitions)|Unused `struct` definitions|2|
|[[N-84]](#n-84-use-bytesconcat-over-abiencodepacked)|Use `bytes.concat` over `abi.encodePacked`|3|
|[[N-85]](#n-85-use-delete-rather-than-assigning-to-0)|Use `delete` rather than assigning to `0`|11|
|[[N-86]](#n-86-use-descriptive-constant-rather-than-0-for-function-arguments)|Use descriptive constant rather than `0` for function arguments|33|
|[[N-87]](#n-87-no-need-to-initialize-variables-to-their-default-value)|No need to initialize variables to their default value|12|
|[[N-88]](#n-88-non-constant-state-variables-should-be-named-using-mixedcase)|Non `constant` state variables should be named using mixedCase|2|
|[[N-89]](#n-89-certain-variables-should-be-mutable)|Certain variables should be mutable|1|
|[[N-90]](#n-90-avoid-extraneous-whitespace)|Avoid extraneous whitespace|5|
|[[N-91]](#n-91-top-level-declarations-should-be-separated-by-two-blank-lines)|Top level declarations should be separated by two blank lines|66|
|[[N-92]](#n-92-large-or-complicated-code-bases-should-implement-invariant-tests)|Large or complicated code bases should implement invariant tests|1|
|[[N-93]](#n-93-tests-should-have-full-coverage)|Tests should have full coverage|1|
|[[N-94]](#n-94-codebase-should-go-through-formal-verification)|Codebase should go through formal verification|1|

Total issues: 94

Total instances: 1952

# Low Risk Issues
## [L-01] Potential DOS if `constant`/`immutable` address becomes blacklisted

Certain ERC20 tokens such as USDT and USDC implement a blacklist, meaning once
a certain address is added to the blacklist, all transfers from or to that
address will revert.

In the following instances, a token transfer is made to a `constant` or
`immutable` address. Should this address become blacklisted in the token
contract, then the call would always revert, causing a DOS on the function.
If the function is critical to the operation of the protocol, then this
scenario can have a very high impact.

Consider implementing the pull over push pattern: use on chain accounting to 
keep track of how much each user is owed, and allow them to initiate a withdrawal
in a separate transaction so that core protocol operations are not interrupted in the
case of a failed transfer.

<details>
<summary>Instances: 1</summary>

```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

148:         IERC20(token).safeTransfer(feeRecipientAddress, amount);

```
[L148](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L148)

</details>

&nbsp;
## [L-02] Chainlink aggregators return the incorrect price if it drops below `minAnswer`

Chainlink aggregators have a built in circuit breaker if the price of an asset
goes outside of a predetermined price band. The result is that if an asset
experiences a huge drop in value (i.e. LUNA crash) the price of the oracle will
continue to return the `minAnswer` instead of the actual price of the asset. See
[Chainlink's docs](https://docs.chain.link/data-feeds#check-the-latest-answer-against-reasonable-limits)
for more info.

Chainlink's `latestRoundData` pulls the associated aggregator and requests round
data from it. ChainlinkAggregators have `minAnswer` and `maxAnswer` circuit
breakers built into them. This means that if the price of the asset drops below
the `minAnswer`, the protocol will continue to value the token at `minAnswer`
instead of it's actual value. This will allow users to exploit certain parts of
the protocol.

This discrepency could cause major issues within the protocol and potentially
lead to loss of funds. This is exactly what happened to 
[Venus on BSC when LUNA imploded](https://rekt.news/venus-blizz-rekt/).

**Recommendation:** add a check to revert if the price received from the oracle is
out of bounds.

<details>
<summary>Instances: 3</summary>

```solidity
File: packages/contracts/contracts/PriceFeed.sol

634:         try ETH_BTC_CL_FEED.latestRoundData() returns (
635:             uint80 roundId,
636:             int256 answer,
637:             uint256,
638:             /* startedAt */
639:             uint256 timestamp,
640:             uint80 /* answeredInRound */
641:         ) {

650:         try STETH_ETH_CL_FEED.latestRoundData() returns (
651:             uint80 roundId,
652:             int256 answer,
653:             uint256,
654:             /* startedAt */
655:             uint256 timestamp,
656:             uint80 /* answeredInRound */
657:         ) {

```
[L634](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L634), [L650](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L650)

</details>

&nbsp;
## [L-03] Fee on transfer/rebasing tokens not properly accounted for

When transferring tokens from another account to `address(this)`, the amount of
tokens received by the contract is not necessarily equal to the `amount`
parameter. This can be the case for:
    - fee on transfer tokens: e.g. PAXG
        - a fee is taken out of each transfer from the `amount` and sent to a
        predetermined fee recipient, meaning the `to` address receives fewer
        tokens
    - rebasing tokens: e.g. stETH
        - user token balances are algorithmically altered automatically,
        meaning balances change without any action being taken

If it is assumed that a contracts balance of a particular token is equal to the
`amount` parameter used in `transferFrom`, this can be violated and lead to
unexpected issues.

**Recommendation:** implement an allowlist for ERC20 tokens, or redesign functions
to account for obscure tokens.

<details>
<summary>Instances: 3</summary>

```solidity
File: packages/contracts/contracts/ActivePool.sol

283:         collateral.transferFrom(address(receiver), address(this), amountWithFee);

```
[L283](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L283)

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

785:         collateral.transferFrom(msg.sender, address(activePool), _stEthBalance);

```
[L785](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L785)

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

129:             IERC20(operation.tokenToTransferIn).safeTransferFrom(
130:                 msg.sender,
131:                 address(this),
132:                 operation.amountToTransferIn
133:             );

```
[L129](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L129)

</details>

&nbsp;
## [L-04] User facing functions should have `address(0)` checks

Parameters of type address in your functions should be checked to ensure that they
are not assigned the null address (address(0x0)). Failure to validate these
parameters can lead to transaction reverts, wasted gas, the need for transaction
resubmission, and may even require redeployment of contracts within the protocol
in certain situations. Implement checks for address(0x0) to avoid these potential
issues.

<details>
<summary>Instances: 38</summary>

```solidity
File: packages/contracts/contracts/ActivePool.sol

100:     function transferSystemCollShares(address _account, uint256 _shares) public override {

129:     function transferSystemCollSharesAndLiquidatorReward(
130:         address _account,
131:         uint256 _shares,
132:         uint256 _liquidatorRewardShares
133:     ) external override {

261:     function flashLoan(
262:         IERC3156FlashBorrower receiver,
263:         address token,
264:         uint256 amount,
265:         bytes calldata data
266:     ) external override returns (bool) {

371:     function sweepToken(address token, uint256 amount) public nonReentrant requiresAuth {

```
[L100](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L100), [L129](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L129), [L261](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L261), [L371](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L371)

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

187:     function openCdpFor(
188:         uint256 _debt,
189:         bytes32 _upperHint,
190:         bytes32 _lowerHint,
191:         uint256 _stEthBalance,
192:         address _borrower
193:     ) external override nonReentrantSelfAndCdpM returns (bytes32) {

628:     function setPositionManagerApproval(
629:         address _positionManager,
630:         PositionManagerApproval _approval
631:     ) external override {

647:     function revokePositionManagerApproval(address _positionManager) external override {

653:     function renouncePositionManagerApproval(address _borrower) external override {

706:     function permitPositionManagerApproval(
707:         address _borrower,
708:         address _positionManager,
709:         PositionManagerApproval _approval,
710:         uint256 _deadline,
711:         uint8 v,
712:         bytes32 r,
713:         bytes32 s
714:     ) external override {

1077:     function flashLoan(
1078:         IERC3156FlashBorrower receiver,
1079:         address token,
1080:         uint256 amount,
1081:         bytes calldata data
1082:     ) external override returns (bool) {

```
[L187](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L187), [L628](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L628), [L647](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L647), [L653](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L653), [L706](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L706), [L1077](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1077)

```solidity
File: packages/contracts/contracts/CdpManager.sol

538:     function closeCdp(
539:         bytes32 _cdpId,
540:         address _borrower,
541:         uint256 _debt,
542:         uint256 _coll
543:     ) external override {

905:     function initializeCdp(
906:         bytes32 _cdpId,
907:         uint256 _debt,
908:         uint256 _coll,
909:         uint256 _liquidatorRewardShares,
910:         address _borrower
911:     ) external {

946:     function updateCdp(
947:         bytes32 _cdpId,
948:         address _borrower,
949:         uint256 _coll,
950:         uint256 _debt,
951:         uint256 _newColl,
952:         uint256 _newDebt
953:     ) external {

```
[L538](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L538), [L905](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L905), [L946](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L946)

```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

77:     function increaseSurplusCollShares(address _account, uint256 _amount) external override {

89:     function claimSurplusCollShares(address _account) external override {

142:     function sweepToken(address token, uint256 amount) public nonReentrant requiresAuth {

```
[L77](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L77), [L89](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L89), [L142](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L142)

```solidity
File: packages/contracts/contracts/EBTCToken.sol

85:     function mint(address _account, uint256 _amount) external override {

95:     function burn(address _account, uint256 _amount) external override {

119:     function transfer(address recipient, uint256 amount) external override returns (bool) {

129:     function approve(address spender, uint256 amount) external override returns (bool) {

134:     function transferFrom(
135:         address sender,
136:         address recipient,
137:         uint256 amount
138:     ) external override returns (bool) {

152:     function increaseAllowance(
153:         address spender,
154:         uint256 addedValue
155:     ) external override returns (bool) {

160:     function decreaseAllowance(
161:         address spender,
162:         uint256 subtractedValue
163:     ) external override returns (bool) {

199:     function permit(
200:         address owner,
201:         address spender,
202:         uint256 amount,
203:         uint256 deadline,
204:         uint8 v,
205:         bytes32 r,
206:         bytes32 s
207:     ) external override {

```
[L85](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L85), [L95](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L95), [L119](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L119), [L129](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L129), [L134](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L134), [L152](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L152), [L160](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L160), [L199](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L199)

```solidity
File: packages/contracts/contracts/SortedCdps.sol

344:     function insert(
345:         address owner,
346:         uint256 _NICR,
347:         bytes32 _prevId,
348:         bytes32 _nextId
349:     ) external override returns (bytes32) {

```
[L344](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L344)

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

118:     function doOperation(
119:         FlashLoanType flType,
120:         uint256 borrowAmount,
121:         LeverageMacroOperation calldata operation,
122:         PostOperationCheck postCheckType,
123:         PostCheckParams calldata checkParams
124:     ) external {

234:     function sweepToken(address token, uint256 amount) public {

344:     function onFlashLoan(
345:         address initiator,
346:         address token,
347:         uint256 amount,
348:         uint256 fee,
349:         bytes calldata data
350:     ) external returns (bytes32) {

```
[L118](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L118), [L234](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L234), [L344](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L344)

```solidity
File: packages/contracts/contracts/LeverageMacroFactory.sol

43:     function deployNewMacro(address _owner) public returns (address) {

```
[L43](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L43)

```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

51:     function setFallbackHandler(bytes4 sig, address handler) external {

110:     function execute(Operation[] calldata ops) external payable {

```
[L51](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L51), [L110](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L110)

```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

42:     function setAuthority(Authority newAuthority) public virtual {

52:     function transferOwnership(address newOwner) public virtual requiresAuth {

```
[L42](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L42), [L52](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L52)

```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

38:     function setAuthority(address newAuthority) public virtual {

```
[L38](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L38)

```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

85:     function setPublicCapability(
86:         address target,
87:         bytes4 functionSig,
88:         bool enabled
89:     ) public virtual requiresAuth {

106:     function setRoleCapability(
107:         uint8 role,
108:         address target,
109:         bytes4 functionSig,
110:         bool enabled
111:     ) public virtual requiresAuth {

133:     function burnCapability(address target, bytes4 functionSig) public virtual requiresAuth {

147:     function setUserRole(address user, uint8 role, bool enabled) public virtual requiresAuth {

```
[L85](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L85), [L106](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L106), [L133](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L133), [L147](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L147)

</details>

&nbsp;
## [L-05] Missing `address(0)` checks when assigning to `address` state variables

<details>
<summary>Instances: 1</summary>

```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

53:         owner = newOwner;

```
[L53](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L53)

</details>

&nbsp;
## [L-06] Approval may revert if current allowance is non-zero

Some tokens (like USDT) do not work when changing the allowance from an
existing non-zero allowance value. They must first be approved by zero and then
the actual allowance must be approved.

**Recommendation:** add an approval with amount 0 before approving the desired
amount, or use `safeApprove` from OpenZeppelin's
[SafeERC20](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/token/ERC20/utils/SafeERC20.sol)
library.

<details>
<summary>Instances: 1</summary>

```solidity
File: packages/contracts/contracts/LeverageMacroReference.sol

53:         ebtcToken.approve(address(borrowerOperations), type(uint256).max);

```
[L53](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L53)

</details>

&nbsp;
## [L-07] Use `require` instead of `assert`

Prior to Solidity 0.8.0, pressing a confirm consumes the remainder of the process's available gas instead of returning it, as request()/revert() did.

assert() and ruqire(); The big difference between the two is that the assert()function when false, uses up all the remaining gas and reverts all the changes made. Meanwhile, a require() function when false, also reverts back all the changes made to the contract but does refund all the remaining gas fees we offered to pay. This is the most common Solidity function used by developers for debugging and error handling.

Assertion() should be avoided even after solidity version 0.8.0, because its documentation states "The Assert function generates an error of type Panic(uint256). Code that works properly should never Panic, even on invalid external input. If this happens, you need to fix it in your contract. there's a mistake".

<details>
<summary>Instances: 1</summary>

```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

564:         assert(toLiquidator < _totalColToSend); // Assert is correct here for Echidna

```
[L564](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L564)

</details>

&nbsp;
## [L-08] Missing contract existence check for yul `call`

Low-level calls return success if there is no code present at the specified
address. Add a check to verify that `target.code.size > 0` (or in assembly,
use `extcodesize`).

<details>
<summary>Instances: 3</summary>

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

514:             _success := call(
515:                 _gas, // gas
516:                 _target, // recipient
517:                 _value, // ether value
518:                 add(_calldata, 0x20), // inloc
519:                 mload(_calldata), // inlen
520:                 0, // outloc
521:                 0 // outlen
522:             )

```
[L514](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L514)

```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

144:                 success := delegatecall(txGas, to, add(data, 0x20), mload(data), 0, 0)

149:                 success := call(txGas, to, value, add(data, 0x20), mload(data), 0, 0)

```
[L144](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L144), [L149](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L149)

</details>

&nbsp;
## [L-09] Lack of two-step update for critical functions

A copy-paste error or a typo may end up bricking protocol functionality, or sending
tokens to an address with no known private key. Consider implementing a two-step
procedure for critical functions, where the recipient is set as pending, and must
"accept" the assignment by making an affirmative call. A straight forward way of
doing this would be to have the target contracts implement
[EIP-165](https://eips.ethereum.org/EIPS/eip-165), and to have the "set" functions
ensure that the recipient is of the right interface type.

<details>
<summary>Instances: 17</summary>

```solidity
File: packages/contracts/contracts/ActivePool.sol

390:     function setFeeRecipientAddress(address _feeRecipientAddress) external requiresAuth {

404:     function setFeeBps(uint256 _newFee) external requiresAuth {

417:     function setFlashLoansPaused(bool _paused) external requiresAuth {

```
[L390](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L390), [L404](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L404), [L417](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L417)

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

1140:     function setFeeRecipientAddress(address _feeRecipientAddress) external requiresAuth {

1154:     function setFeeBps(uint256 _newFee) external requiresAuth {

1167:     function setFlashLoansPaused(bool _paused) external requiresAuth {

```
[L1140](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1140), [L1154](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1154), [L1167](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1167)

```solidity
File: packages/contracts/contracts/CdpManager.sol

773:     function setStakingRewardSplit(uint256 _stakingRewardSplit) external requiresAuth {

788:     function setRedemptionFeeFloor(uint256 _redemptionFeeFloor) external requiresAuth {

807:     function setMinuteDecayFactor(uint256 _minuteDecayFactor) external requiresAuth {

830:     function setBeta(uint256 _beta) external requiresAuth {

843:     function setRedemptionsPaused(bool _paused) external requiresAuth {

```
[L773](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L773), [L788](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L788), [L807](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L807), [L830](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L830), [L843](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L843)

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

111:     function setGracePeriod(uint128 _gracePeriod) external requiresAuth {

```
[L111](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L111)

```solidity
File: packages/contracts/contracts/Governor.sol

154:     function setRoleName(uint8 role, string memory roleName) external requiresAuth {

```
[L154](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L154)

```solidity
File: packages/contracts/contracts/PriceFeed.sol

358:     function setFallbackCaller(address _fallbackCaller) external requiresAuth {

```
[L358](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L358)

```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

85:     function setPublicCapability(
86:         address target,
87:         bytes4 functionSig,
88:         bool enabled
89:     ) public virtual requiresAuth {

106:     function setRoleCapability(
107:         uint8 role,
108:         address target,
109:         bytes4 functionSig,
110:         bool enabled
111:     ) public virtual requiresAuth {

147:     function setUserRole(address user, uint8 role, bool enabled) public virtual requiresAuth {

```
[L85](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L85), [L106](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L106), [L147](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L147)

</details>

&nbsp;
## [L-10] Contract deployment is vulnerable to block re-orgs

Block reorgs are common in EVM chains,
[even on mainnet](https://decrypt.co/101390/ethereum-beacon-chain-blockchain-reorg).
On other networks such as Polygon, reorgs can be a lot more
[extreme](https://protos.com/polygon-hit-by-157-block-reorg-despite-hard-fork-to-reduce-reorgs/).

Deploying a contract and cacheing the address, if a block reorg occurs, would cause
the cached address to point to an incorrect address, and due to how addresses are
calculated at deployment, this could be irreversible. Deploy contracts using
[create2](https://docs.openzeppelin.com/cli/2.8/deploying-with-create2) where possible to
mitigate this.

<details>
<summary>Instances: 1</summary>

```solidity
File: packages/contracts/contracts/LeverageMacroFactory.sol

44:         address addy = address(
45:             new LeverageMacroReference(
46:                 borrowerOperations,
47:                 activePool,
48:                 cdpManager,
49:                 ebtcToken,
50:                 stETH,
51:                 sortedCdps,
52:                 _owner
53:             )
54:         );

```
[L44](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L44)

</details>

&nbsp;
## [L-11] Division before multiplications leads to precision loss

Since Solidity cannot deal with decimal values, make sure to use multiplication before division to avoid precision loss due to rounding errors.

<details>
<summary>Instances: 1</summary>

```solidity
File: packages/contracts/contracts/PriceFeed.sol

800:         return
801:             (_scaledDecimal *
802:                 uint256(_ethBtcAnswer) *
803:                 uint256(_stEthEthAnswer) *
804:                 EbtcMath.DECIMAL_PRECISION) / 10 ** (_decimalDenominator * 2);

```
[L800](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L800)

</details>

&nbsp;
## [L-12] Numbers downcast to `address` may result in collisions

If a number is downcast to an address the upper bytes are truncated, which
may mean that more than one value will map to the address.

<details>
<summary>Instances: 1</summary>

```solidity
File: packages/contracts/contracts/SortedCdps.sol

125:         return address(uint160(_tmp));

```
[L125](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L125)

</details>

&nbsp;
## [L-13] `decimals()` is not part of the ERC20 standard

The `decimals()` function is not a part of the
[ERC-20 standard](https://eips.ethereum.org/EIPS/eip-20), and was addedlater as an
[optional extension](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/token/ERC20/extensions/IERC20Metadata.sol).
As such, some valid ERC20 tokens do not support this interface, so it is unsafe to
blindly cast all tokens to this interface, and then call this function.

<details>
<summary>Instances: 4</summary>

```solidity
File: packages/contracts/contracts/PriceFeed.sol

615:         try ETH_BTC_CL_FEED.decimals() returns (uint8 decimals) {

623:         try STETH_ETH_CL_FEED.decimals() returns (uint8 decimals) {

703:         try ETH_BTC_CL_FEED.decimals() returns (uint8 decimals) {

711:         try STETH_ETH_CL_FEED.decimals() returns (uint8 decimals) {

```
[L615](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L615), [L623](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L623), [L703](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L703), [L711](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L711)

</details>

&nbsp;
## [L-14] ERC20 may revert on zero transfer

In spite of the fact that EIP-20
[states](https://github.com/ethereum/EIPs/blob/46b9b698815abbfa628cd1097311deee77dd45c5/EIPS/eip-20.md?plain=1#L116)
that zero-valued transfers must be accepted, some tokens, such as LEND will
revert if this is attempted, which may cause transactions that involve other
tokens (such as batch operations) to fully revert. Consider skipping the
transfer if the amount is zero, which will also save gas.

<details>
<summary>Instances: 7</summary>

```solidity
File: packages/contracts/contracts/ActivePool.sol

274:         collateral.transfer(address(receiver), amount);

283:         collateral.transferFrom(address(receiver), address(this), amountWithFee);

286:         collateral.transfer(feeRecipientAddress, fee);

381:         IERC20(token).safeTransfer(cachedFeeRecipientAddress, amount);

```
[L274](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L274), [L283](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L283), [L286](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L286), [L381](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L381)

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

785:         collateral.transferFrom(msg.sender, address(activePool), _stEthBalance);

```
[L785](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L785)

```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

148:         IERC20(token).safeTransfer(feeRecipientAddress, amount);

```
[L148](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L148)

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

237:         IERC20(token).safeTransfer(msg.sender, amount);

```
[L237](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L237)

</details>

&nbsp;
## [L-15] Solidity's `ecrecover` is vulnerable to signature malleability

The built-in EVM precompile `ecrecover` is susceptible to signature malleability, which could lead to replay attacks.
References: https://swcregistry.io/docs/SWC-117, https://swcregistry.io/docs/SWC-121, and https://medium.com/cryptronics/signature-replay-vulnerabilities-in-smart-contracts-3b6f7596df57

While this is not immediately exploitable, this may become a vulnerability if used elsewhere.

Consider using [OpenZeppelin's ECDSA library](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/cryptography/ECDSA.sol) (which prevents this malleability) instead of the built-in function.

<details>
<summary>Instances: 2</summary>

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

733:         address recoveredAddress = ecrecover(digest, v, r, s);

```
[L733](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L733)

```solidity
File: packages/contracts/contracts/EBTCToken.sol

218:         address recoveredAddress = ecrecover(digest, v, r, s);

```
[L218](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L218)

</details>

&nbsp;
## [L-16] Consider bounding input array length

If the number of for loop iterations is unbounded, then it may lead to the
transaction to run out of gas. While the function will revert if it
eventually runs out of gas, it may be a nicer user experience to `require()`
that the length of the array is below some reasonable maximum, so that the
user doesn't have to use up a full transaction's gas only to see that the
transaction reverts.

<details>
<summary>Instances: 6</summary>

```solidity
File: packages/contracts/contracts/Governor.sol

46:         for (uint256 i = 0; i < users.length(); i++) {

57:             for (uint256 i = 0; i < _usrs.length; i++) {

76:         for (uint8 i = 0; i < type(uint8).max; i++) {

84:             for (uint8 i = 0; i < type(uint8).max; i++) {

98:         for (uint8 i = 0; i < type(uint8).max; i++) {

107:             for (uint8 i = 0; i < type(uint8).max; i++) {

```
[L46](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L46), [L57](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L57), [L76](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L76), [L84](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L84), [L98](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L98), [L107](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L107)

</details>

&nbsp;
## [L-17] Functions that do not handle `msg.value` should not be `payable`

If `msg.value` is unhandled, ether is not required to be sent with the function
call but it may be sent unintentionally. This can lead to loss of user funds as
the ether would become trapped in the contract.

Remove the `payable` keyword from the following functions.

<details>
<summary>Instances: 1</summary>

```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

110:     function execute(Operation[] calldata ops) external payable {

```
[L110](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L110)

</details>

&nbsp;
## [L-18] Functions transferring tokens that may have hooks are missing reentrancy guards

Even if the function follows the best practice of check-effects-interaction,
not using a reentrancy guard when there may be transfer hooks will open the
users of this protocol up to
[read-only reentrancies](https://chainsecurity.com/curve-lp-oracle-manipulation-post-mortem/).

Consider using a `nonReentrant` modifier from OpenZeppelin's
[ReentrancyGuard.sol](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/security/ReentrancyGuard.sol)
for the following functions.

<details>
<summary>Instances: 7</summary>

```solidity
File: packages/contracts/contracts/ActivePool.sol

261:     function flashLoan(
262:         IERC3156FlashBorrower receiver,
263:         address token,
264:         uint256 amount,
265:         bytes calldata data
266:     ) external override returns (bool) {

274:         collateral.transfer(address(receiver), amount);

283:         collateral.transferFrom(address(receiver), address(this), amountWithFee);

286:         collateral.transfer(feeRecipientAddress, fee);

```
[L261](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L261), [L274](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L274), [L283](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L283), [L286](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L286)

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

1077:     function flashLoan(
1078:         IERC3156FlashBorrower receiver,
1079:         address token,
1080:         uint256 amount,
1081:         bytes calldata data
1082:     ) external override returns (bool) {

1100:         ebtcToken.transferFrom(address(receiver), feeRecipientAddress, fee + amount);

```
[L1077](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1077), [L1100](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1100)

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

118:     function doOperation(
119:         FlashLoanType flType,
120:         uint256 borrowAmount,
121:         LeverageMacroOperation calldata operation,
122:         PostOperationCheck postCheckType,
123:         PostCheckParams calldata checkParams
124:     ) external {

129:             IERC20(operation.tokenToTransferIn).safeTransferFrom(
130:                 msg.sender,
131:                 address(this),
132:                 operation.amountToTransferIn
133:             );

214:     function sweepToCaller() public {

224:             ebtcToken.transfer(msg.sender, ebtcBal);

234:     function sweepToken(address token, uint256 amount) public {

237:         IERC20(token).safeTransfer(msg.sender, amount);

```
[L118](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L118), [L129](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L129), [L214](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L214), [L224](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L224), [L234](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L234), [L237](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L237)

</details>

&nbsp;
## [L-19] Incorrect bips value used

It is commonly known that 1 "bip" is one one-hundredth of one percent, or
`1 / 10_000`. Use the correct denominator when referring to units in "bips"
to avoid misleading users or entering erroneous values.

<details>
<summary>Instances: 1</summary>

```solidity
File: packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol

10:     uint256 public constant MAX_FEE_BPS = 1_000; // 10%

```
[L10](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L10)

</details>

&nbsp;
## [L-20] Some tokens do not consider `type(uint256).max` as an infinite approval

Some tokens such as
[COMP](https://github.com/compound-finance/compound-protocol/blob/a3214f67b73310d547e00fc578e8355911c9d376/contracts/Governance/Comp.sol#L89-L91)
downcast such approvals to uint96 and use that as a raw value rather than
interpreting it as an infinite approval. Eventually these approvals will reach
zero, at which point the calling contract will no longer function properly.

<details>
<summary>Instances: 6</summary>

```solidity
File: packages/contracts/contracts/LeverageMacroReference.sol

39:         ebtcToken.approve(_borrowerOperationsAddress, type(uint256).max);
40:         stETH.approve(_borrowerOperationsAddress, type(uint256).max);
41:         stETH.approve(_activePool, type(uint256).max);

53:         ebtcToken.approve(address(borrowerOperations), type(uint256).max);
54:         stETH.approve(address(borrowerOperations), type(uint256).max);
55:         stETH.approve(address(activePool), type(uint256).max);

```
[L39](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L39), [L53](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L53)

</details>

&nbsp;
## [L-21] Cap state variables at reasonable values

Consider adding maximum value checks to ensure that state variables
cannot be set to values that may excessively harm users.

<details>
<summary>Instances: 4</summary>

```solidity
File: packages/contracts/contracts/CdpManager.sol

835:         beta = _beta;

```
[L835](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L835)

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

118:         recoveryModeGracePeriodDuration = _gracePeriod;

```
[L118](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L118)

```solidity
File: packages/contracts/contracts/Governor.sol

155:         roleNames[role] = roleName;

```
[L155](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L155)

```solidity
File: packages/contracts/contracts/SortedCdps.sol

93:         maxSize = _size;

```
[L93](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L93)

</details>

&nbsp;
## [L-22] Checks-Effects-Interactions pattern not followed

The
[Checks-Effects-Interactions](https://fravoll.github.io/solidity-patterns/checks_effects_interactions.html)
pattern (CEI) is a best practice that reduces the attack surface for reentrancy
attacks.

To adhere to this pattern, place state variable updates before external calls
within functions.

<details>
<summary>Instances: 4</summary>

```solidity
File: packages/contracts/contracts/ActivePool.sol

346:     function claimFeeRecipientCollShares(uint256 _shares) external override requiresAuth {
347:         ICdpManagerData(cdpManagerAddress).syncGlobalAccountingAndGracePeriod(); // Calling this increases shares so do it first

359:         feeRecipientCollShares = cachedFeeRecipientCollShares;

390:     function setFeeRecipientAddress(address _feeRecipientAddress) external requiresAuth {
391:         ICdpManagerData(cdpManagerAddress).syncGlobalAccountingAndGracePeriod(); // Accrue State First

398:         feeRecipientAddress = _feeRecipientAddress;

```
[L346](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L346), [L359](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L359), [L390](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L390), [L398](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L398)

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

1140:     function setFeeRecipientAddress(address _feeRecipientAddress) external requiresAuth {

1146:         cdpManager.syncGlobalAccounting();

1148:         feeRecipientAddress = _feeRecipientAddress;

```
[L1140](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1140), [L1146](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1146), [L1148](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1148)

```solidity
File: packages/contracts/contracts/PriceFeed.sol

358:     function setFallbackCaller(address _fallbackCaller) external requiresAuth {

364:             try newFallbackCaler.getFallbackResponse() returns (
365:                 uint256 answer,
366:                 uint256 timestampRetrieved,
367:                 bool success
368:             ) {

372:                 if (
373:                     !_fallbackIsBroken(fallbackResponse) &&
374:                     !_responseTimeout(fallbackResponse.timestamp, newFallbackCaler.fallbackTimeout())
375:                 ) {

377:                     fallbackCaller = newFallbackCaler;

386:             fallbackCaller = newFallbackCaler;

```
[L358](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L358), [L364](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L364), [L372](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L372), [L377](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L377), [L386](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L386)

</details>

&nbsp;
## [L-23] Some tokens may revert on large approvals
Tokens such as
[COMP](https://github.com/compound-finance/compound-protocol/blob/a3214f67b73310d547e00fc578e8355911c9d376/contracts/Governance/Comp.sol#L78-L98)
or [UNI](https://github.com/Uniswap/governance/blob/master/contracts/Uni.sol#L141-L161)
will revert on approval if the `amount` exceeds `type(uint96).max`. Ensure that
the calls below can be broken up into smaller batches if necessary.

<details>
<summary>Instances: 1</summary>

```solidity
File: packages/contracts/contracts/LeverageMacroReference.sol

53:         ebtcToken.approve(address(borrowerOperations), type(uint256).max);

```
[L53](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L53)

</details>

&nbsp;
## [L-24] Some tokens may revert on large transfers

Tokens such as
[COMP](https://github.com/compound-finance/compound-protocol/blob/a3214f67b73310d547e00fc578e8355911c9d376/contracts/Governance/Comp.sol#L109-L142)
or [UNI](https://github.com/Uniswap/governance/blob/master/contracts/Uni.sol#L203-L236)
will revert on `transfer`/`transferFrom` when an address' balance reaches `type(uint96).max`.
Ensure that the calls below can be broken up into smaller batches if necessary.

<details>
<summary>Instances: 10</summary>

```solidity
File: packages/contracts/contracts/ActivePool.sol

274:         collateral.transfer(address(receiver), amount);

283:         collateral.transferFrom(address(receiver), address(this), amountWithFee);

286:         collateral.transfer(feeRecipientAddress, fee);

381:         IERC20(token).safeTransfer(cachedFeeRecipientAddress, amount);

```
[L274](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L274), [L283](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L283), [L286](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L286), [L381](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L381)

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

785:         collateral.transferFrom(msg.sender, address(activePool), _stEthBalance);

1100:         ebtcToken.transferFrom(address(receiver), feeRecipientAddress, fee + amount);

```
[L785](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L785), [L1100](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1100)

```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

148:         IERC20(token).safeTransfer(feeRecipientAddress, amount);

```
[L148](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L148)

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

129:             IERC20(operation.tokenToTransferIn).safeTransferFrom(
130:                 msg.sender,
131:                 address(this),
132:                 operation.amountToTransferIn
133:             );

224:             ebtcToken.transfer(msg.sender, ebtcBal);

237:         IERC20(token).safeTransfer(msg.sender, amount);

```
[L129](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L129), [L224](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L224), [L237](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L237)

</details>

&nbsp;
## [L-25] NFT contract redefines `_mint()`/`_safeMint()`, but not both

If one of the functions is re-implemented, or has new arguments, the other
should be as well. The `_mint` variant is supposed to skip
`onERC721Received` checks, whereas `_safeMint` does not. Not having both
points to a possible issue with spec-compatability.

<details>
<summary>Instances: 1</summary>

```solidity
File: packages/contracts/contracts/EBTCToken.sol

262:     function _mint(address account, uint256 amount) internal {

```
[L262](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L262)

</details>

&nbsp;
## [L-26] Minting to address zero should be prevented

Minting tokens to the zero address in Solidity is a potential pitfall that
should be carefully guarded against. The zero address (0x0) is generally
used as a default value and represents an uninitialized or null address.
Minting tokens to this address effectively burns them, making them
inaccessible and permanently removing them from the total supply. This
could lead to unintended token loss if performed accidentally. To prevent
this, it's important to include a check in the minting function to ensure
that the target address is not the zero address. Using a library like
OpenZeppelin's [`Address`](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/utils/Address.sol)
can provide utility functions like `requireNonZero`, which simplifies this
check and enhances the security of the minting function.

<details>
<summary>Instances: 1</summary>

```solidity
File: packages/contracts/contracts/EBTCToken.sol

85:     function mint(address _account, uint256 _amount) external override {

```
[L85](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L85)

</details>

&nbsp;
## [L-27] Potential division by zero

When dividing by a value that may be zero, add checks so that execution does
not unexpectedly revert.

<details>
<summary>Instances: 3</summary>

```solidity
File: packages/contracts/contracts/CdpManager.sol

624:         uint256 newBaseRate = decayedBaseRate + (redeemedEBTCFraction / beta);

```
[L624](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L624)

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

454:             stake = (_coll * totalStakesSnapshot) / totalCollateralSnapshot;

```
[L454](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L454)

```solidity
File: packages/contracts/contracts/PriceFeed.sol

534:         uint256 percentPriceDifference = ((maxPrice - minPrice) * EbtcMath.DECIMAL_PRECISION) /
535:             minPrice;

```
[L534](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L534)

</details>

&nbsp;
## [L-28] Possible loss of precision

Division by large numbers may result in precision loss due to rounding down,
or even the result being erroneously equal to zero. Consider adding checks on
the numerator to ensure precision loss is handled appropriately.

<details>
<summary>Instances: 30</summary>

```solidity
File: packages/contracts/contracts/ActivePool.sol

321:         return (amount * feeBps) / MAX_BPS;

```
[L321](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L321)

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

1118:         return (amount * feeBps) / MAX_BPS;

```
[L1118](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1118)

```solidity
File: packages/contracts/contracts/CdpManager.sol

145:         singleRedemption.collSharesDrawn = collateral.getSharesByPooledEth(
146:             (singleRedemption.debtToRedeem * DECIMAL_PRECISION) / _redeemColFromCdp.price
147:         );

621:         uint256 redeemedEBTCFraction = (collateral.getPooledEthByShares(_ETHDrawn) * _price) /
622:             _totalEBTCSupply;

624:         uint256 newBaseRate = decayedBaseRate + (redeemedEBTCFraction / beta);

671:         uint256 redemptionFee = (_redemptionRate * _ETHDrawn) / DECIMAL_PRECISION;

706:         return (baseRate * decayFactor) / DECIMAL_PRECISION;

710:         return
711:             block.timestamp > lastRedemptionTimestamp
712:                 ? ((block.timestamp - lastRedemptionTimestamp) / SECONDS_IN_ONE_MINUTE)
713:                 : 0;

```
[L145](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L145), [L621](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L621), [L624](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L624), [L671](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L671), [L706](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L706), [L710](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L710)

```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

278:         uint _debtToColl = (_totalDebtToBurn * DECIMAL_PRECISION) / _liqState.price;

365:         uint _debtToColl = (_totalDebtToBurn * DECIMAL_PRECISION) / _recoveryState.price;

435:             uint _debtToColl = (_partialDebt * DECIMAL_PRECISION) / _partialState.price;

555:             _incentiveColl = (_totalDebtToBurn * (_ICR > MCR ? MCR : _ICR)) / _price;

558:             _incentiveColl = (_totalDebtToBurn * LICR) / _price;

579:             _incentiveColl = (_totalDebtToBurn * (_ICR > MCR ? MCR : _ICR)) / _price;

592:             uint256 _debtToRepay = (_incentiveColl * _price) / LICR;

882:         uint256 EBTCDebtRewardPerUnitStaked = EBTCDebtNumerator / _totalStakes;

```
[L278](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L278), [L365](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L365), [L435](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L435), [L555](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L555), [L558](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L558), [L579](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L579), [L592](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L592), [L882](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L882)

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

316:             pendingEBTCDebtReward = (cdp.stake * _debtIndexDiff) / DECIMAL_PRECISION;

454:             stake = (_coll * totalStakesSnapshot) / totalCollateralSnapshot;

558:         uint256 deltaIndexFees = (deltaIndex * stakingRewardSplit) / MAX_REWARD_SPLIT;

564:         uint256 _feeTaken = collateral.getSharesByPooledEth(_deltaFeeSplit) / DECIMAL_PRECISION;

567:         uint256 _deltaFeePerUnit = _deltaFeeSplitShare / _cachedAllStakes;

637:             return (
638:                 _feeSplitDistributed,
639:                 (_scaledCdpColl - _feeSplitDistributed) / DECIMAL_PRECISION
640:             );

```
[L316](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L316), [L454](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L454), [L558](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L558), [L564](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L564), [L567](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L567), [L637](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L637)

```solidity
File: packages/contracts/contracts/PriceFeed.sol

457:         uint256 percentDeviation = maxPrice > 0
458:             ? ((maxPrice - minPrice) * EbtcMath.DECIMAL_PRECISION) / maxPrice
459:             : 0;

534:         uint256 percentPriceDifference = ((maxPrice - minPrice) * EbtcMath.DECIMAL_PRECISION) /
535:             minPrice;

```
[L457](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L457), [L534](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L534)

```solidity
File: packages/contracts/contracts/HintHelpers.sol

144:         uint256 collShareToReceive = collateral.getSharesByPooledEth(
145:             (maxRedeemableEBTC * DECIMAL_PRECISION) / _price
146:         );

```
[L144](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L144)

```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

108:         uint256 feePercentage = (_fee * DECIMAL_PRECISION) / _amount;

119:         return (_debt * _price) / DECIMAL_PRECISION;

```
[L108](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L108), [L119](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L119)

```solidity
File: packages/contracts/contracts/Dependencies/EbtcMath.sol

38:         decProd = (prod_xy + (DECIMAL_PRECISION / 2)) / DECIMAL_PRECISION;

94:             return (_collShares * NICR_PRECISION) / _debt;

110:             uint256 newCollRatio = (_stEthBalance * _price) / _debt;

```
[L38](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L38), [L94](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L94), [L110](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L110)

</details>

&nbsp;
## [L-29] `safeApprove` is deprecated

OpenZeppelin's `safeApprove` function has been
[deprecated](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/bfff03c0d2a59bcd8e2ead1da9aed9edf0080d05/contracts/token/ERC20/utils/SafeERC20.sol#L38-L45)
in favour of `safeIncreaseAllowance` and `safeDecreaseAllowance`. The
function may currently work, but if a bug is found in this version of
OpenZeppelin, and the version that you're forced to upgrade to no longer
has this function, you'll encounter unnecessary delays in porting and
testing replacement contracts.

<details>
<summary>Instances: 2</summary>

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

405:         IERC20(swapData.tokenForSwap).safeApprove(
406:             swapData.addressForApprove,
407:             swapData.exactApproveAmount
408:         );

427:         IERC20(swapData.tokenForSwap).safeApprove(swapData.addressForApprove, 0);

```
[L405](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L405), [L427](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L427)

</details>

&nbsp;
## [L-30] Use `safeTransfer` instead of `transfer` for token transfers

`SafeERC20` is a wrapper around ERC20 operations that throw on failure (when the token contract returns false). This prevents calls executing if a token transfer is unsuccessful. Simply add `using SafeERC20 for ERC20`.

<details>
<summary>Instances: 6</summary>

```solidity
File: packages/contracts/contracts/ActivePool.sol

274:         collateral.transfer(address(receiver), amount);

283:         collateral.transferFrom(address(receiver), address(this), amountWithFee);

286:         collateral.transfer(feeRecipientAddress, fee);

```
[L274](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L274), [L283](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L283), [L286](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L286)

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

785:         collateral.transferFrom(msg.sender, address(activePool), _stEthBalance);

1100:         ebtcToken.transferFrom(address(receiver), feeRecipientAddress, fee + amount);

```
[L785](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L785), [L1100](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1100)

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

224:             ebtcToken.transfer(msg.sender, ebtcBal);

```
[L224](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L224)

</details>

&nbsp;
## [L-31] Subtraction may underflow if result of multiplication is too large

The following expressions may underflow, as the subtrahend could be greater than the minuend in case the former is multiplied by a large number.

<details>
<summary>Instances: 2</summary>

```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

884:         lastEBTCDebtErrorRedistribution =
885:             EBTCDebtNumerator -
886:             (EBTCDebtRewardPerUnitStaked * _totalStakes);

```
[L884](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L884)

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

568:         uint256 _perUnitError = _deltaFeeSplitShare - (_deltaFeePerUnit * _cachedAllStakes);

```
[L568](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L568)

</details>

&nbsp;
## [L-32] Remove/Resolve open TODOs

<details>
<summary>Instances: 1</summary>

```solidity
File: packages/contracts/contracts/CdpManager.sol

79:     //    Cdp ICR     |       Liquidation Behavior (TODO gas compensation?)

```
[L79](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L79)

</details>

&nbsp;
## [L-33] Downcasting `uint` or `int` may result in overflow

Consider using OpenZeppelin's `SafeCast` library to prevent unexpected overflows.

<details>
<summary>Instances: 1</summary>

```solidity
File: packages/contracts/contracts/SortedCdps.sol

125:         return address(uint160(_tmp));

```
[L125](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L125)

</details>

&nbsp;
## [L-34] Use of `approve` is discouraged

OpenZeppelin recommends using `increaseAllowance` and `decreaseAllowance`
instead of `approve` to mitigate against the problem described
[here](https://github.com/ethereum/EIPs/issues/20#issuecomment-263524729).

Source: [OpenZeppelin docs](https://docs.openzeppelin.com/contracts/4.x/api/token/erc20#ERC20-increaseAllowance-address-uint256-),
OpenZeppelin [ERC20.sol](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/token/ERC20/ERC20.sol#L170-L216).

<details>
<summary>Instances: 8</summary>

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

405:         IERC20(swapData.tokenForSwap).safeApprove(
406:             swapData.addressForApprove,
407:             swapData.exactApproveAmount
408:         );

427:         IERC20(swapData.tokenForSwap).safeApprove(swapData.addressForApprove, 0);

```
[L405](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L405), [L427](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L427)

```solidity
File: packages/contracts/contracts/LeverageMacroReference.sol

39:         ebtcToken.approve(_borrowerOperationsAddress, type(uint256).max);
40:         stETH.approve(_borrowerOperationsAddress, type(uint256).max);
41:         stETH.approve(_activePool, type(uint256).max);

53:         ebtcToken.approve(address(borrowerOperations), type(uint256).max);
54:         stETH.approve(address(borrowerOperations), type(uint256).max);
55:         stETH.approve(address(activePool), type(uint256).max);

```
[L39](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L39), [L53](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L53)

</details>

&nbsp;
## [L-35] Missing `address(0)` checks in constructor/initialize

Failing to check for invalid parameters on deployment may result in an erroneous input and require an expensive redeployment.

<details>
<summary>Instances: 16</summary>

```solidity
File: packages/contracts/contracts/ActivePool.sol

46:     constructor(
47:         address _borrowerOperationsAddress,
48:         address _cdpManagerAddress,
49:         address _collTokenAddress,
50:         address _collSurplusAddress,
51:         address _feeRecipientAddress
52:     ) {

```
[L46](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L46)

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

107:     constructor(
108:         address _cdpManagerAddress,
109:         address _activePoolAddress,
110:         address _collSurplusPoolAddress,
111:         address _priceFeedAddress,
112:         address _sortedCdpsAddress,
113:         address _ebtcTokenAddress,
114:         address _feeRecipientAddress,
115:         address _collTokenAddress
116:     ) EbtcBase(_activePoolAddress, _priceFeedAddress, _collTokenAddress) {

```
[L107](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L107)

```solidity
File: packages/contracts/contracts/CdpManager.sol

30:     constructor(
31:         address _liquidationLibraryAddress,
32:         address _authorityAddress,
33:         address _borrowerOperationsAddress,
34:         address _collSurplusPoolAddress,
35:         address _ebtcTokenAddress,
36:         address _sortedCdpsAddress,
37:         address _activePoolAddress,
38:         address _priceFeedAddress,
39:         address _collTokenAddress
40:     )
41:         CdpManagerStorage(
42:             _liquidationLibraryAddress,
43:             _authorityAddress,
44:             _borrowerOperationsAddress,
45:             _collSurplusPoolAddress,
46:             _ebtcTokenAddress,
47:             _sortedCdpsAddress,
48:             _activePoolAddress,
49:             _priceFeedAddress,
50:             _collTokenAddress
51:         )
52:     {

```
[L30](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L30)

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

217:     constructor(
218:         address _liquidationLibraryAddress,
219:         address _authorityAddress,
220:         address _borrowerOperationsAddress,
221:         address _collSurplusPool,
222:         address _ebtcToken,
223:         address _sortedCdps,
224:         address _activePool,
225:         address _priceFeed,
226:         address _collateral
227:     ) EbtcBase(_activePool, _priceFeed, _collateral) {

```
[L217](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L217)

```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

42:     constructor(
43:         address _borrowerOperationsAddress,
44:         address _cdpManagerAddress,
45:         address _activePoolAddress,
46:         address _collTokenAddress
47:     ) {

```
[L42](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L42)

```solidity
File: packages/contracts/contracts/EBTCToken.sol

61:     constructor(
62:         address _cdpManagerAddress,
63:         address _borrowerOperationsAddress,
64:         address _authorityAddress
65:     ) {

```
[L61](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L61)

```solidity
File: packages/contracts/contracts/PriceFeed.sol

57:     constructor(
58:         address _fallbackCallerAddress,
59:         address _authorityAddress,
60:         address _collEthCLFeed,
61:         address _ethBtcCLFeed
62:     ) {

```
[L57](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L57)

```solidity
File: packages/contracts/contracts/SortedCdps.sol

88:     constructor(uint256 _size, address _cdpManagerAddress, address _borrowerOperationsAddress) {

```
[L88](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L88)

```solidity
File: packages/contracts/contracts/HintHelpers.sol

27:     constructor(
28:         address _sortedCdpsAddress,
29:         address _cdpManagerAddress,
30:         address _collateralAddress,
31:         address _activePoolAddress,
32:         address _priceFeedAddress
33:     ) EbtcBase(_activePoolAddress, _priceFeedAddress, _collateralAddress) {

```
[L27](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L27)

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

51:     constructor(
52:         address _borrowerOperationsAddress,
53:         address _activePool,
54:         address _cdpManager,
55:         address _ebtc,
56:         address _coll,
57:         address _sortedCdps,
58:         bool _sweepToCaller
59:     ) {

```
[L51](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L51)

```solidity
File: packages/contracts/contracts/LeverageMacroDelegateTarget.sol

41:     constructor(
42:         address _borrowerOperationsAddress,
43:         address _activePool,
44:         address _cdpManager,
45:         address _ebtc,
46:         address _coll,
47:         address _sortedCdps
48:     )
49:         LeverageMacroBase(
50:             _borrowerOperationsAddress,
51:             _activePool,
52:             _cdpManager,
53:             _ebtc,
54:             _coll,
55:             _sortedCdps,
56:             false // Do not sweep to caller
57:         )
58:     {

```
[L41](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L41)

```solidity
File: packages/contracts/contracts/LeverageMacroFactory.sol

21:     constructor(
22:         address _borrowerOperationsAddress,
23:         address _activePool,
24:         address _cdpManager,
25:         address _ebtc,
26:         address _coll,
27:         address _sortedCdps
28:     ) {

```
[L21](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L21)

```solidity
File: packages/contracts/contracts/LeverageMacroReference.sol

17:     constructor(
18:         address _borrowerOperationsAddress,
19:         address _activePool,
20:         address _cdpManager,
21:         address _ebtc,
22:         address _coll,
23:         address _sortedCdps,
24:         address _owner
25:     )
26:         LeverageMacroBase(
27:             _borrowerOperationsAddress,
28:             _activePool,
29:             _cdpManager,
30:             _ebtc,
31:             _coll,
32:             _sortedCdps,
33:             true // Sweep to caller since this is not supposed to hold funds
34:         )
35:     {

```
[L17](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L17)

```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

44:     constructor(address _owner) {

```
[L44](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L44)

```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

18:     constructor(address _owner, Authority _authority) {

```
[L18](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L18)

```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

52:     constructor(address _activePoolAddress, address _priceFeedAddress, address _collateralAddress) {

```
[L52](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L52)

</details>

&nbsp;

&nbsp;

# Non-Critical Issues
## [N-01] Cast to `bytes` or `bytes32` explicitly instead of using `abi.encodePacked`

Using a
[cast](https://ethereum.stackexchange.com/questions/30912/how-to-compare-strings-in-solidity#answer-82739)
on a single argument, rather than abi.encodePacked() makes the intended
operation more clear, leading to less reviewer confusion.

<details>
<summary>Instances: 1</summary>

```solidity
File: packages/contracts/contracts/HintHelpers.sol

182:             latestRandomSeed = uint256(keccak256(abi.encodePacked(latestRandomSeed)));

```
[L182](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L182)

</details>

&nbsp;
## [N-02] Not using the named return variable anywhere in the function is confusing

Consider changing the variable to be unnamed, or return it using its name.

<details>
<summary>Instances: 8</summary>

```solidity
File: packages/contracts/contracts/CdpManager.sol

570:     function getSystemDebt() public view returns (uint256 entireSystemDebt) {

```
[L570](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L570)

```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

544:     function _calculatePartialLiquidationSurplusAndCap(
545:         uint256 _ICR,
546:         uint256 _price,
547:         uint256 _totalDebtToBurn,
548:         uint256 _totalColToSend
549:     ) private view returns (uint256 toLiquidator, uint256 collSurplus, uint256 debtToRedistribute) {

```
[L544](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L544)

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

719:     function getPendingRedistributedDebt(
720:         bytes32 _cdpId
721:     ) public view returns (uint256 pendingEBTCDebtReward) {

```
[L719](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L719)

```solidity
File: packages/contracts/contracts/Governor.sol

146:     function getRoleName(uint8 role) external view returns (string memory roleName) {

```
[L146](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L146)

```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

67:     function getSystemCollShares() public view returns (uint256 entireSystemColl) {

75:     function _getSystemDebt() internal view returns (uint256 entireSystemDebt) {

83:     function _getTCRWithSystemDebtAndCollShares(
84:         uint256 _price
85:     ) internal view returns (uint256 TCR, uint256 _coll, uint256 _debt) {

```
[L67](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L67), [L75](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L75), [L83](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L83)

```solidity
File: packages/contracts/contracts/Interfaces/ICdpManagerData.sol

263:     function canLiquidateRecoveryMode(uint256 icr, uint256 tcr) external view returns (bool);

```
[L263](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L263)

</details>

&nbsp;
## [N-03] Use modifiers for address checks

Modifiers in Solidity can improve code readability and modularity by
encapsulating repetitive checks, such as address validity checks, into a
reusable construct. For example, an `onlyOwner` modifier can be used to
replace repetitive `require(msg.sender == owner)` checks across several
functions, reducing code redundancy and enhancing maintainability.

<details>
<summary>Instances: 21</summary>

```solidity
File: packages/contracts/contracts/ActivePool.sol

220:         require(
221:             msg.sender == borrowerOperationsAddress,
222:             "ActivePool: Caller is not BorrowerOperations"
223:         );

228:         require(
229:             msg.sender == borrowerOperationsAddress || msg.sender == cdpManagerAddress,
230:             "ActivePool: Caller is neither BorrowerOperations nor CdpManager"
231:         );

236:         require(msg.sender == cdpManagerAddress, "ActivePool: Caller is not CdpManager");

```
[L220](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L220), [L228](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L228), [L236](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L236)

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

964:         if (_borrower == msg.sender) {

```
[L964](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L964)

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

660:         require(
661:             msg.sender == borrowerOperationsAddress,
662:             "CdpManager: Caller is not the BorrowerOperations contract"
663:         );

```
[L660](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L660)

```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

113:         require(
114:             msg.sender == borrowerOperationsAddress,
115:             "CollSurplusPool: Caller is not Borrower Operations"
116:         );

120:         require(msg.sender == cdpManagerAddress, "CollSurplusPool: Caller is not CdpManager");

124:         require(msg.sender == activePoolAddress, "CollSurplusPool: Caller is not Active Pool");

```
[L113](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L113), [L120](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L120), [L124](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L124)

```solidity
File: packages/contracts/contracts/EBTCToken.sol

307:         require(
308:             msg.sender == borrowerOperationsAddress,
309:             "EBTCToken: Caller is not BorrowerOperations"
310:         );

315:         require(
316:             msg.sender == borrowerOperationsAddress ||
317:                 msg.sender == cdpManagerAddress ||
318:                 isAuthorized(msg.sender, msg.sig),
319:             "EBTC: Caller is neither BorrowerOperations nor CdpManager nor authorized"
320:         );

324:         require(msg.sender == cdpManagerAddress, "EBTC: Caller is not CdpManager");

```
[L307](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L307), [L315](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L315), [L324](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L324)

```solidity
File: packages/contracts/contracts/SortedCdps.sol

715:         require(msg.sender == address(cdpManager), "SortedCdps: Caller is not the CdpManager");

720:         require(
721:             msg.sender == borrowerOperationsAddress || msg.sender == address(cdpManager),
722:             "SortedCdps: Caller is neither BO nor CdpM"
723:         );

```
[L715](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L715), [L720](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L720)

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

45:         require(owner() == msg.sender, "Must be owner");

356:             require(
357:                 msg.sender == address(borrowerOperations),
358:                 "LeverageMacroReference: wrong lender for eBTC flashloan"
359:             );

362:             require(
363:                 msg.sender == address(activePool),
364:                 "LeverageMacroReference: wrong lender for stETH flashloan"
365:             );

```
[L45](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L45), [L356](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L356), [L362](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L362)

```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

52:         require(msg.sender == owner);

67:         require(msg.sender == owner);

77:         require(msg.sender == address(this)); // Must call this via `execute` to explicitly set the flag

111:         require(msg.sender == owner, "Must be owner");

```
[L52](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L52), [L67](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L67), [L77](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L77), [L111](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L111)

```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

45:         require(msg.sender == owner || authority.canCall(msg.sender, address(this), msg.sig));

```
[L45](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L45)

</details>

&nbsp;
## [N-04] Inline assembly should contain extensive comments
Due to assembly being a low-level language, comments should be used to improve
readability and reduce margin for error.

<details>
<summary>Instances: 1</summary>

```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

189:         assembly {
190:             calldatacopy(0, 0, calldatasize())
191:             let result := delegatecall(gas(), facet, 0, calldatasize(), 0, 0)
192:             returndatacopy(0, 0, returndatasize())
193:             switch result
194:             case 0 {
195:                 revert(0, returndatasize())
196:             }
197:             default {
198:                 return(0, returndatasize())
199:             }
200:         }

```
[L189](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L189)

</details>

&nbsp;
## [N-05] Consider adding denylist

A denylist helps to prevent malicious users from spending stolen ERC20 or
ERC721 tokens in the protocol.

<details>
<summary>Instances: 1</summary>

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

783:     function _activePoolAddColl(uint256 _stEthBalance, uint256 _sharesToTrack) internal {

```
[L783](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L783)

</details>

&nbsp;
## [N-06] Functions missing empty `bytes` check

Passing empty bytes to a function can cause unexpected behavior, such as
certain operations failing, producing incorrect results, or wasting gas.
It is recommended to check that all `bytes` parameters are not empty.

<details>
<summary>Instances: 52</summary>

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

168:     function openCdp(
169:         uint256 _debt,
170:         bytes32 _upperHint,
171:         bytes32 _lowerHint,
172:         uint256 _stEthBalance
173:     ) external override nonReentrantSelfAndCdpM returns (bytes32) {

187:     function openCdpFor(
188:         uint256 _debt,
189:         bytes32 _upperHint,
190:         bytes32 _lowerHint,
191:         uint256 _stEthBalance,
192:         address _borrower
193:     ) external override nonReentrantSelfAndCdpM returns (bytes32) {

203:     function addColl(
204:         bytes32 _cdpId,
205:         bytes32 _upperHint,
206:         bytes32 _lowerHint,
207:         uint256 _stEthBalanceIncrease
208:     ) external override nonReentrantSelfAndCdpM {

219:     function withdrawColl(
220:         bytes32 _cdpId,
221:         uint256 _stEthBalanceDecrease,
222:         bytes32 _upperHint,
223:         bytes32 _lowerHint
224:     ) external override nonReentrantSelfAndCdpM {

235:     function withdrawDebt(
236:         bytes32 _cdpId,
237:         uint256 _debt,
238:         bytes32 _upperHint,
239:         bytes32 _lowerHint
240:     ) external override nonReentrantSelfAndCdpM {

250:     function repayDebt(
251:         bytes32 _cdpId,
252:         uint256 _debt,
253:         bytes32 _upperHint,
254:         bytes32 _lowerHint
255:     ) external override nonReentrantSelfAndCdpM {

270:     function adjustCdp(
271:         bytes32 _cdpId,
272:         uint256 _stEthBalanceDecrease,
273:         uint256 _debtChange,
274:         bool _isDebtIncrease,
275:         bytes32 _upperHint,
276:         bytes32 _lowerHint
277:     ) external override nonReentrantSelfAndCdpM {

300:     function adjustCdpWithColl(
301:         bytes32 _cdpId,
302:         uint256 _stEthBalanceDecrease,
303:         uint256 _debtChange,
304:         bool _isDebtIncrease,
305:         bytes32 _upperHint,
306:         bytes32 _lowerHint,
307:         uint256 _stEthBalanceIncrease
308:     ) external override nonReentrantSelfAndCdpM {

553:     function closeCdp(bytes32 _cdpId) external override {

```
[L168](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L168), [L187](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L187), [L203](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L203), [L219](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L219), [L235](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L235), [L250](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L250), [L270](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L270), [L300](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L300), [L553](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L553)

```solidity
File: packages/contracts/contracts/CdpManager.sol

99:     function liquidate(bytes32 _cdpId) external override {

109:     function partiallyLiquidate(
110:         bytes32 _cdpId,
111:         uint256 _partialAmount,
112:         bytes32 _upperPartialHint,
113:         bytes32 _lowerPartialHint
114:     ) external override {

320:     function redeemCollateral(
321:         uint256 _debt,
322:         bytes32 _firstRedemptionHint,
323:         bytes32 _upperPartialRedemptionHint,
324:         bytes32 _lowerPartialRedemptionHint,
325:         uint256 _partialRedemptionHintNICR,
326:         uint256 _maxIterations,
327:         uint256 _maxFeePercentage
328:     ) external override nonReentrantSelfAndBOps {

514:     function syncAccounting(bytes32 _cdpId) external virtual override {

523:     function updateStakeAndTotalStakes(bytes32 _cdpId) external override returns (uint256) {

538:     function closeCdp(
539:         bytes32 _cdpId,
540:         address _borrower,
541:         uint256 _debt,
542:         uint256 _coll
543:     ) external override {

856:     function getCdpStatus(bytes32 _cdpId) external view override returns (uint256) {

863:     function getCdpStake(bytes32 _cdpId) external view override returns (uint256) {

871:     function getCdpDebt(bytes32 _cdpId) external view override returns (uint256) {

879:     function getCdpCollShares(bytes32 _cdpId) external view override returns (uint256) {

891:     function getCdpLiquidatorRewardShares(bytes32 _cdpId) external view override returns (uint256) {

905:     function initializeCdp(
906:         bytes32 _cdpId,
907:         uint256 _debt,
908:         uint256 _coll,
909:         uint256 _liquidatorRewardShares,
910:         address _borrower
911:     ) external {

946:     function updateCdp(
947:         bytes32 _cdpId,
948:         address _borrower,
949:         uint256 _coll,
950:         uint256 _debt,
951:         uint256 _newColl,
952:         uint256 _newDebt
953:     ) external {

```
[L99](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L99), [L109](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L109), [L320](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L320), [L514](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L514), [L523](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L523), [L538](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L538), [L856](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L856), [L863](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L863), [L871](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L871), [L879](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L879), [L891](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L891), [L905](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L905), [L946](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L946)

```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

40:     function liquidate(bytes32 _cdpId) external nonReentrantSelfAndBOps {

50:     function partiallyLiquidate(
51:         bytes32 _cdpId,
52:         uint256 _partialAmount,
53:         bytes32 _upperPartialHint,
54:         bytes32 _lowerPartialHint
55:     ) external nonReentrantSelfAndBOps {

```
[L40](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L40), [L50](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L50)

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

616:     function getAccumulatedFeeSplitApplied(
617:         bytes32 _cdpId,
618:         uint256 _systemStEthFeePerUnitIndex
619:     ) public view returns (uint256, uint256) {

673:     function getCachedNominalICR(bytes32 _cdpId) external view returns (uint256) {

684:     function getSyncedNominalICR(bytes32 _cdpId) external view returns (uint256) {

701:     function getCachedICR(bytes32 _cdpId, uint256 _price) public view returns (uint256) {

719:     function getPendingRedistributedDebt(
720:         bytes32 _cdpId
721:     ) public view returns (uint256 pendingEBTCDebtReward) {

728:     function hasPendingRedistributedDebt(bytes32 _cdpId) public view returns (bool) {

745:     function getSyncedDebtAndCollShares(
746:         bytes32 _cdpId
747:     ) public view returns (uint256 debt, uint256 coll) {

839:     function getSyncedCdpDebt(bytes32 _cdpId) public view returns (uint256) {

848:     function getSyncedCdpCollShares(bytes32 _cdpId) public view returns (uint256) {

864:     function getSyncedICR(bytes32 _cdpId, uint256 _price) public view returns (uint256) {

```
[L616](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L616), [L673](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L673), [L684](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L684), [L701](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L701), [L719](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L719), [L728](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L728), [L745](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L745), [L839](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L839), [L848](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L848), [L864](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L864)

```solidity
File: packages/contracts/contracts/EBTCToken.sol

199:     function permit(
200:         address owner,
201:         address spender,
202:         uint256 amount,
203:         uint256 deadline,
204:         uint8 v,
205:         bytes32 r,
206:         bytes32 s
207:     ) external override {

```
[L199](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L199)

```solidity
File: packages/contracts/contracts/SortedCdps.sol

123:     function getOwnerAddress(bytes32 cdpId) public pure override returns (address) {

155:     function cdpOfOwnerByIdx(
156:         address owner,
157:         uint256 index,
158:         bytes32 startNodeId,
159:         uint maxNodes
160:     ) external view override returns (bytes32, bool) {

227:     function getCdpCountOf(
228:         address owner,
229:         bytes32 startNodeId,
230:         uint maxNodes
231:     ) external view override returns (uint256, bytes32) {

286:     function getAllCdpsOf(
287:         address owner,
288:         bytes32 startNodeId,
289:         uint maxNodes
290:     ) external view override returns (bytes32[] memory, uint256, bytes32) {

344:     function insert(
345:         address owner,
346:         uint256 _NICR,
347:         bytes32 _prevId,
348:         bytes32 _nextId
349:     ) external override returns (bytes32) {

410:     function remove(bytes32 _id) external override {

498:     function reInsert(
499:         bytes32 _id,
500:         uint256 _newNICR,
501:         bytes32 _prevId,
502:         bytes32 _nextId
503:     ) external override {

519:     function contains(bytes32 _id) public view override returns (bool) {

567:     function getNext(bytes32 _id) external view override returns (bytes32) {

574:     function getPrev(bytes32 _id) external view override returns (bytes32) {

583:     function validInsertPosition(
584:         uint256 _NICR,
585:         bytes32 _prevId,
586:         bytes32 _nextId
587:     ) external view override returns (bool) {

666:     function findInsertPosition(
667:         uint256 _NICR,
668:         bytes32 _prevId,
669:         bytes32 _nextId
670:     ) external view override returns (bytes32, bytes32) {

```
[L123](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L123), [L155](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L155), [L227](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L227), [L286](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L286), [L344](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L344), [L410](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L410), [L498](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L498), [L519](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L519), [L567](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L567), [L574](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L574), [L583](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L583), [L666](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L666)

```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

51:     function setFallbackHandler(bytes4 sig, address handler) external {

```
[L51](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L51)

```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

50:     function isPublicCapability(address target, bytes4 functionSig) public view returns (bool) {

85:     function setPublicCapability(
86:         address target,
87:         bytes4 functionSig,
88:         bool enabled
89:     ) public virtual requiresAuth {

106:     function setRoleCapability(
107:         uint8 role,
108:         address target,
109:         bytes4 functionSig,
110:         bool enabled
111:     ) public virtual requiresAuth {

133:     function burnCapability(address target, bytes4 functionSig) public virtual requiresAuth {

```
[L50](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L50), [L85](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L85), [L106](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L106), [L133](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L133)

</details>

&nbsp;
## [N-07] Comparisons should place constants on the left hand side

This practise avoids
[typo errors](https://www.moserware.com/2008/01/constants-on-left-are-better-but-this.html).

<details>
<summary>Instances: 35</summary>

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

748:         if (_collReceived != 0) {

808:             _stEthBalanceIncrease == 0 || _stEthBalanceDecrease == 0,

819:             _stEthBalanceIncrease != 0 || _stEthBalanceDecrease != 0 || _debtChange != 0,

826:         require(status == 1, "BorrowerOperations: Cdp does not exist or is closed");

831:         require(status == 0, "BorrowerOperations: Cdp is active or has been previously closed");

847:             _stEthBalanceDecrease == 0,

```
[L748](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L748), [L808](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L808), [L819](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L819), [L826](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L826), [L831](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L831), [L847](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L847)

```solidity
File: packages/contracts/contracts/CdpManager.sol

159:         if (newDebt == 0) {

377:         if (_maxIterations == 0) {

434:         if (_numCdpsFullyRedeemed == 1) {

```
[L159](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L159), [L377](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L377), [L434](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L434)

```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

56:         require(_partialAmount != 0, "LiquidationLibrary: use `liquidate` for 100%");

144:         if (_liqState.partialAmount == 0) {

158:                 liquidationValues.totalCollToSendToLiquidator == 0 &&

159:                 liquidationValues.debtToBurn == 0

417:         if (newColl == 0) {

681:             _cdpArray.length != 0,

863:         if (_debt == 0) {

```
[L56](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L56), [L144](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L144), [L158](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L158), [L159](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L159), [L417](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L417), [L681](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L681), [L863](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L863)

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

443:         if (totalCollateralSnapshot == 0) {

624:             _cdpStEthFeePerUnitIndex == 0 ||

625:             _cdpCol == 0 ||

```
[L443](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L443), [L624](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L624), [L625](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L625)

```solidity
File: packages/contracts/contracts/PriceFeed.sol

420:             _response.timestampEthBtc == 0 ||

422:             _response.timestampStEthEth == 0 ||

471:         if (_response.timestamp == 0 || _response.timestamp > block.timestamp) {

475:         if (_response.answer == 0) {

532:         if (minPrice == 0) return false;

695:         if (_currentRoundEthBtcId == 0 || _currentRoundStEthEthId == 0) {

776:         if (_answer <= 0) return false;

777:         if (_roundId == 0) return false;

```
[L420](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L420), [L422](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L422), [L471](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L471), [L475](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L475), [L532](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L532), [L695](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L695), [L776](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L776), [L777](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L777)

```solidity
File: packages/contracts/contracts/SortedCdps.sol

89:         if (_size == 0) {

305:         if (maxArraySize == 0) {

352:         require(cdpManager.getCdpStatus(_id) == 0, "SortedCdps: new id is NOT nonExistent!");

537:         return data.size == 0;

```
[L89](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L89), [L305](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L305), [L352](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L352), [L537](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L537)

```solidity
File: packages/contracts/contracts/HintHelpers.sol

78:         if (_maxIterations == 0) {

171:         if (arrayLength == 0) {

```
[L78](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L78), [L171](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L171)

```solidity
File: packages/contracts/contracts/Dependencies/EbtcMath.sol

64:         if (_minutes == 0) {

```
[L64](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L64)

```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

124:             if (enabledFunctionSigsByTarget[target].length() == 0) {

```
[L124](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L124)

</details>

&nbsp;
## [N-08] Use enum values instead of constant array indexes

Create a commented enum value to use instead of constant array indexes to
make the code more readable and reduce margin for error.

<details>
<summary>Instances: 2</summary>

```solidity
File: packages/contracts/contracts/CdpManager.sol

502:         require(_toRemoveIds[0] == _start, "CdpManager: batchRemoveSortedCdpIds check start error");

```
[L502](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L502)

```solidity
File: packages/contracts/contracts/SortedCdps.sol

424:         bytes32 _firstPrev = data.nodes[_ids[0]].prevId;

```
[L424](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L424)

</details>

&nbsp;
## [N-09] Variable names for `constant` variables should be in CONSTANT_CASE

See the
[Solidity style guide](https://docs.soliditylang.org/en/v0.8.17/style-guide.html#local-and-state-variable-names)
for more info.

<details>
<summary>Instances: 1</summary>

```solidity
File: packages/contracts/contracts/SortedCdps.sol

80:     bytes32 public constant dummyId =
81:         0x0000000000000000000000000000000000000000000000000000000000000000;

```
[L80](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L80)

</details>

&nbsp;
## [N-10] Do not calculate constants

Due to how constant variables are implemented (replacements at compile-time),
an expression assigned to a constant variable is recomputed each time that
the variable is used, which wastes some gas.

<details>
<summary>Instances: 1</summary>

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

141:     uint256 public constant MIN_REDEMPTION_FEE_FLOOR = (DECIMAL_PRECISION * 5) / 1000; // 0.5%

```
[L141](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L141)

</details>

&nbsp;
## [N-11] Contract name not following Solidity style guide

See the [Solidity style guide](https://docs.soliditylang.org/en/v0.8.16/style-guide.html#contract-and-library-names)
for more details.

<details>
<summary>Instances: 1</summary>

```solidity
File: packages/contracts/contracts/EBTCToken.sol

26: contract EBTCToken is IEBTCToken, AuthNoOwner, PermitNonce {

```
[L26](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L26)

</details>

&nbsp;
## [N-12] Missing contract NatSpec

The [Solidity docs](https://docs.soliditylang.org/en/latest/natspec-format.html)
state that "it is recommended that Solidity contracts are fully annotated using
NatSpec for all public interfaces (everything in the ABI)".

<details>
<summary>Instances: 2</summary>

```solidity
File: packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol

8: abstract contract ERC3156FlashLender is IERC3156FlashLender {

```
[L8](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L8)

```solidity
File: packages/contracts/contracts/Dependencies/EbtcMath.sol

5: library EbtcMath {

```
[L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L5)

</details>

&nbsp;
## [N-13] Contracts should expose an `interface`

The contracts should expose an `interface` so that other projects can
more easily integrate with it, without having to develop their own
non-standard variants.

<details>
<summary>Instances: 9</summary>

```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

13: contract LiquidationLibrary is CdpManagerStorage {

```
[L13](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L13)

```solidity
File: packages/contracts/contracts/Governor.sol

13: contract Governor is RolesAuthority {

```
[L13](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L13)

```solidity
File: packages/contracts/contracts/HintHelpers.sol

11: contract HintHelpers is EbtcBase {

```
[L11](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L11)

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

26: contract LeverageMacroBase {

```
[L26](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L26)

```solidity
File: packages/contracts/contracts/LeverageMacroDelegateTarget.sol

40: contract LeverageMacroDelegateTarget is LeverageMacroBase {

```
[L40](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L40)

```solidity
File: packages/contracts/contracts/LeverageMacroFactory.sol

11: contract LeverageMacroFactory {

```
[L11](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L11)

```solidity
File: packages/contracts/contracts/LeverageMacroReference.sol

11: contract LeverageMacroReference is LeverageMacroBase {

```
[L11](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L11)

```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

25: contract SimplifiedDiamondLike {

```
[L25](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L25)

```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

10: contract AuthNoOwner {

```
[L10](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L10)

</details>

&nbsp;
## [N-14] Contract does not follow suggested layout ordering

Within a contract, the ordering should be:
1. Type declarations
2. State variables
3. Events
4. Modifiers
5. Functions
See the 
[Solidity style guide](https://docs.soliditylang.org/en/v0.8.16/style-guide.html#order-of-layout)
for more info.

<details>
<summary>Instances: 3</summary>

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

19: contract CdpManagerStorage is EbtcBase, ReentrancyGuard, ICdpManagerData, AuthNoOwner {

```
[L19](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L19)

```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

9: abstract contract Auth {

```
[L9](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L9)

```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

10: contract AuthNoOwner {

```
[L10](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L10)

</details>

&nbsp;
## [N-15] Control structures do not follow the Solidity style guide

According to the [Solidity style guide](https://docs.soliditylang.org/en/latest/style-guide.html#control-structures),
braces should open on the same line as the declaration, close on their own
line and the opening brace should be preceded by a single space.

<details>
<summary>Instances: 7</summary>

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

21: contract BorrowerOperations is
22:     EbtcBase,
23:     ReentrancyGuard,
24:     IBorrowerOperations,
25:     ERC3156FlashLender,
26:     AuthNoOwner,
27:     PermitNonce
28: {

```
[L21](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L21)

```solidity
File: packages/contracts/contracts/CdpManager.sol

30:     constructor(
31:         address _liquidationLibraryAddress,
32:         address _authorityAddress,
33:         address _borrowerOperationsAddress,
34:         address _collSurplusPoolAddress,
35:         address _ebtcTokenAddress,
36:         address _sortedCdpsAddress,
37:         address _activePoolAddress,
38:         address _priceFeedAddress,
39:         address _collTokenAddress
40:     )
41:         CdpManagerStorage(
42:             _liquidationLibraryAddress,
43:             _authorityAddress,
44:             _borrowerOperationsAddress,
45:             _collSurplusPoolAddress,
46:             _ebtcTokenAddress,
47:             _sortedCdpsAddress,
48:             _activePoolAddress,
49:             _priceFeedAddress,
50:             _collTokenAddress
51:         )
52:     {

```
[L30](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L30)

```solidity
File: packages/contracts/contracts/PriceFeed.sol

582:     function _getCurrentFallbackResponse()
583:         internal
584:         view
585:         returns (FallbackResponse memory fallbackResponse)
586:     {

606:     function _getCurrentChainlinkResponse()
607:         internal
608:         view
609:         returns (ChainlinkResponse memory chainlinkResponse)
610:     {

```
[L582](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L582), [L606](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L606)

```solidity
File: packages/contracts/contracts/HintHelpers.sol

48:     function getRedemptionHints(
49:         uint256 _EBTCamount,
50:         uint256 _price,
51:         uint256 _maxIterations
52:     )
53:         external
54:         view
55:         returns (
56:             bytes32 firstRedemptionHint,
57:             uint256 partialRedemptionHintNICR,
58:             uint256 truncatedEBTCamount,
59:             uint256 partialRedemptionNewColl
60:         )
61:     {

```
[L48](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L48)

```solidity
File: packages/contracts/contracts/LeverageMacroDelegateTarget.sol

41:     constructor(
42:         address _borrowerOperationsAddress,
43:         address _activePool,
44:         address _cdpManager,
45:         address _ebtc,
46:         address _coll,
47:         address _sortedCdps
48:     )
49:         LeverageMacroBase(
50:             _borrowerOperationsAddress,
51:             _activePool,
52:             _cdpManager,
53:             _ebtc,
54:             _coll,
55:             _sortedCdps,
56:             false // Do not sweep to caller
57:         )
58:     {

```
[L41](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L41)

```solidity
File: packages/contracts/contracts/LeverageMacroReference.sol

17:     constructor(
18:         address _borrowerOperationsAddress,
19:         address _activePool,
20:         address _cdpManager,
21:         address _ebtc,
22:         address _coll,
23:         address _sortedCdps,
24:         address _owner
25:     )
26:         LeverageMacroBase(
27:             _borrowerOperationsAddress,
28:             _activePool,
29:             _cdpManager,
30:             _ebtc,
31:             _coll,
32:             _sortedCdps,
33:             true // Sweep to caller since this is not supposed to hold funds
34:         )
35:     {

```
[L17](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L17)

</details>

&nbsp;
## [N-16] Complex casting

Complex casting should be avoided in Solidity contracts where possible to prevent
unintended consequences and ensure accurate data representation.
Performing multiple type casts in succession can lead to unexpected
truncation, rounding errors, or loss of precision, potentially
compromising the contract's functionality and reliability. Consider
adding comments to explain in detail why the casts are necessary, and any
implicit reasons why the cast does not introduce an overflow.

<details>
<summary>Instances: 1</summary>

```solidity
File: packages/contracts/contracts/SortedCdps.sol

114:         serialized |= bytes32(uint256(uint160(owner))) << ADDRESS_SHIFT;

```
[L114](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L114)

</details>

&nbsp;
## [N-17] Duplicated `require`/`revert` checks should be refactored to a modifier or function

The compiler will inline the function, which will avoid `JUMP` instructions
usually associated with functions.

<details>
<summary>Instances: 4</summary>

```solidity
File: packages/contracts/contracts/ActivePool.sol

137:         require(cachedSystemCollShares >= _shares, "ActivePool: Insufficient collateral shares");

162:         require(cachedSystemCollShares >= _shares, "ActivePool: Insufficient collateral shares");

```
[L137](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L137), [L162](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L162)

```solidity
File: packages/contracts/contracts/SortedCdps.sol

458:         require(contains(_id), "SortedCdps: List does not contain the id");

506:         require(contains(_id), "SortedCdps: List does not contain the id");

```
[L458](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L458), [L506](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L506)

```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

52:         require(msg.sender == owner);

67:         require(msg.sender == owner);

```
[L52](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L52), [L67](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L67)

```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

90:         require(
91:             capabilityFlag[target][functionSig] != CapabilityFlag.Burned,
92:             "RolesAuthority: Capability Burned"
93:         );

134:         require(
135:             capabilityFlag[target][functionSig] != CapabilityFlag.Burned,
136:             "RolesAuthority: Capability Burned"
137:         );

```
[L90](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L90), [L134](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L134)

</details>

&nbsp;
## [N-18] Redundant `else` block

One level of nesting can be removed by not having an else block when the if-block returns.

<details>
<summary>Instances: 8</summary>

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

666:         if (_chainID() == _CACHED_CHAIN_ID) {
667:             return _CACHED_DOMAIN_SEPARATOR;
668:         } else {
669:             return _buildDomainSeparator(_TYPE_HASH, _HASHED_NAME, _HASHED_VERSION);
670:         }

```
[L666](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L666)

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

636:         if (_scaledCdpColl > _feeSplitDistributed) {
637:             return (
638:                 _feeSplitDistributed,
639:                 (_scaledCdpColl - _feeSplitDistributed) / DECIMAL_PRECISION
640:             );
641:         } else {
642:             // extreme unlikely case to skip fee split on this CDP to avoid revert
643:             return (0, _cdpCol);
644:         }

765:         if (_newIndex > _oldIndex && totalStakes > 0) {
766:             /// @audit-ok We don't take the fee if we had a negative rebase
767:             (
768:                 uint256 _feeTaken,
769:                 uint256 _deltaFeePerUnit,
770:                 uint256 _perUnitError
771:             ) = calcFeeUponStakingReward(_newIndex, _oldIndex);

773:             // calculate new split per stake unit
774:             uint256 _newPerUnit = systemStEthFeePerUnitIndex + _deltaFeePerUnit;
775:             return (_feeTaken, _newPerUnit, _perUnitError);
776:         } else {
777:             return (0, systemStEthFeePerUnitIndex, systemStEthFeePerUnitIndexError);
778:         }

```
[L636](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L636), [L765](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L765), [L773](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L773)

```solidity
File: packages/contracts/contracts/EBTCToken.sol

183:         if (_chainID() == _CACHED_CHAIN_ID) {
184:             return _CACHED_DOMAIN_SEPARATOR;
185:         } else {
186:             return _buildDomainSeparator(_TYPE_HASH, _HASHED_NAME, _HASHED_VERSION);
187:         }

```
[L183](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L183)

```solidity
File: packages/contracts/contracts/SortedCdps.sol

187:             if (getOwnerAddress(_currentCdpId) == owner) {
188:                 // if the current index of the owner CDP matches specified index
189:                 if (_currentIndex == index) {
190:                     return (_currentCdpId, true);
191:                 } else {
192:                     // if not, increment the owner index as we've seen a CDP owned by them
193:                     _currentIndex = _currentIndex + 1;
194:                 }

596:         if (_prevId == dummyId && _nextId == dummyId) {
597:             // `(null, null)` is a valid insert position if the list is empty
598:             return isEmpty();
599:         } else if (_prevId == dummyId) {
600:             // `(null, _nextId)` is a valid insert position if `_nextId` is the head of the list
601:             return data.head == _nextId && _NICR >= cdpManager.getCachedNominalICR(_nextId);
602:         } else if (_nextId == dummyId) {
603:             // `(_prevId, null)` is a valid insert position if `_prevId` is the tail of the list
604:             return data.tail == _prevId && _NICR <= cdpManager.getCachedNominalICR(_prevId);
605:         } else {
606:             // `(_prevId, _nextId)` is a valid insert position if they are adjacent nodes and `_NICR` falls between the two nodes' NICRs
607:             return
608:                 data.nodes[_prevId].nextId == _nextId &&
609:                 cdpManager.getCachedNominalICR(_prevId) >= _NICR &&
610:                 _NICR >= cdpManager.getCachedNominalICR(_nextId);
611:         }

696:         if (prevId == dummyId && nextId == dummyId) {
697:             // No hint - descend list starting from head
698:             return _descendList(_NICR, data.head);
699:         } else if (prevId == dummyId) {
700:             // No `prevId` for hint - ascend list starting from `nextId`
701:             return _ascendList(_NICR, nextId);
702:         } else if (nextId == dummyId) {
703:             // No `nextId` for hint - descend list starting from `prevId`
704:             return _descendList(_NICR, prevId);
705:         } else {
706:             // Descend list starting from `prevId`
707:             return _descendList(_NICR, prevId);
708:         }

```
[L187](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L187), [L596](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L596), [L696](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L696)

```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

70:         if (flag == CapabilityFlag.Burned) {
71:             return false;
72:         } else if (flag == CapabilityFlag.Public) {
73:             return true;
74:         } else {
75:             return bytes32(0) != getUserRoles[user] & getRolesWithCapability[target][functionSig];
76:         }

```
[L70](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L70)

</details>

&nbsp;
## [N-19] Events may be emitted out of order due to reentrancy

To strictly conform to the Checks Effects Interactions pattern, it is
recommended to emit events before any external interactions.

<details>
<summary>Instances: 17</summary>

```solidity
File: packages/contracts/contracts/ActivePool.sol

261:     function flashLoan(
262:         IERC3156FlashBorrower receiver,
263:         address token,
264:         uint256 amount,
265:         bytes calldata data
266:     ) external override returns (bool) {

274:         collateral.transfer(address(receiver), amount);

283:         collateral.transferFrom(address(receiver), address(this), amountWithFee);

286:         collateral.transfer(feeRecipientAddress, fee);

307:         emit FlashLoanSuccess(address(receiver), token, amount, fee);

346:     function claimFeeRecipientCollShares(uint256 _shares) external override requiresAuth {
347:         ICdpManagerData(cdpManagerAddress).syncGlobalAccountingAndGracePeriod(); // Calling this increases shares so do it first

360:         emit FeeRecipientClaimableCollSharesDecreased(cachedFeeRecipientCollShares, _shares);

371:     function sweepToken(address token, uint256 amount) public nonReentrant requiresAuth {
372:         ICdpManagerData(cdpManagerAddress).syncGlobalAccountingAndGracePeriod(); // Accrue State First

381:         IERC20(token).safeTransfer(cachedFeeRecipientAddress, amount);

383:         emit SweepTokenSuccess(token, amount, cachedFeeRecipientAddress);

390:     function setFeeRecipientAddress(address _feeRecipientAddress) external requiresAuth {
391:         ICdpManagerData(cdpManagerAddress).syncGlobalAccountingAndGracePeriod(); // Accrue State First

399:         emit FeeRecipientAddressChanged(_feeRecipientAddress);

404:     function setFeeBps(uint256 _newFee) external requiresAuth {
405:         ICdpManagerData(cdpManagerAddress).syncGlobalAccountingAndGracePeriod(); // Accrue State First

412:         emit FlashFeeSet(msg.sender, _oldFee, _newFee);

417:     function setFlashLoansPaused(bool _paused) external requiresAuth {
418:         ICdpManagerData(cdpManagerAddress).syncGlobalAccountingAndGracePeriod(); // Accrue State First

421:         emit FlashLoansPaused(msg.sender, _paused);

```
[L261](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L261), [L274](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L274), [L283](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L283), [L286](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L286), [L307](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L307), [L346](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L346), [L360](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L360), [L371](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L371), [L381](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L381), [L383](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L383), [L390](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L390), [L399](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L399), [L404](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L404), [L412](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L412), [L417](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L417), [L421](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L421)

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

1077:     function flashLoan(
1078:         IERC3156FlashBorrower receiver,
1079:         address token,
1080:         uint256 amount,
1081:         bytes calldata data
1082:     ) external override returns (bool) {

1088:         ebtcToken.mint(address(receiver), amount);

1100:         ebtcToken.transferFrom(address(receiver), feeRecipientAddress, fee + amount);

1103:         ebtcToken.burn(feeRecipientAddress, amount);

1105:         emit FlashLoanSuccess(address(receiver), token, amount, fee);

1140:     function setFeeRecipientAddress(address _feeRecipientAddress) external requiresAuth {

1146:         cdpManager.syncGlobalAccounting();

1149:         emit FeeRecipientAddressChanged(_feeRecipientAddress);

1154:     function setFeeBps(uint256 _newFee) external requiresAuth {

1157:         cdpManager.syncGlobalAccounting();

1162:         emit FlashFeeSet(msg.sender, _oldFee, _newFee);

1167:     function setFlashLoansPaused(bool _paused) external requiresAuth {
1168:         cdpManager.syncGlobalAccounting();

1171:         emit FlashLoansPaused(msg.sender, _paused);

```
[L1077](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1077), [L1088](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1088), [L1100](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1100), [L1103](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1103), [L1105](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1105), [L1140](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1140), [L1146](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1146), [L1149](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1149), [L1154](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1154), [L1157](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1157), [L1162](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1162), [L1167](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1167), [L1171](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1171)

```solidity
File: packages/contracts/contracts/CdpManager.sol

135:     function _redeemCollateralFromCdp(
136:         SingleRedemptionInputs memory _redeemColFromCdp
137:     ) internal returns (SingleRedemptionValues memory singleRedemption) {

209:             sortedCdps.reInsert(
210:                 _redeemColFromCdp.cdpId,
211:                 newNICR,
212:                 _redeemColFromCdp.upperPartialRedemptionHint,
213:                 _redeemColFromCdp.lowerPartialRedemptionHint
214:             );

220:             emit CdpUpdated(
221:                 _redeemColFromCdp.cdpId,
222:                 ISortedCdps(sortedCdps).getOwnerAddress(_redeemColFromCdp.cdpId),
223:                 msg.sender,
224:                 _oldDebtAndColl.debt,
225:                 _oldDebtAndColl.collShares,
226:                 newDebt,
227:                 newColl,
228:                 Cdps[_redeemColFromCdp.cdpId].stake,
229:                 CdpOperation.redeemCollateral
230:             );

320:     function redeemCollateral(
321:         uint256 _debt,
322:         bytes32 _firstRedemptionHint,
323:         bytes32 _upperPartialRedemptionHint,
324:         bytes32 _lowerPartialRedemptionHint,
325:         uint256 _partialRedemptionHintNICR,
326:         uint256 _maxIterations,
327:         uint256 _maxFeePercentage
328:     ) external override nonReentrantSelfAndBOps {

442:             sortedCdps.batchRemove(_toRemoveIds);

466:         emit Redemption(
467:             _debt,
468:             totals.debtToRedeem,
469:             totals.collSharesDrawn,
470:             totals.feeCollShares,
471:             msg.sender
472:         );

```
[L135](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L135), [L209](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L209), [L220](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L220), [L320](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L320), [L442](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L442), [L466](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L466)

```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

295:     function _liquidateIndividualCdpSetupCDPInRecoveryMode(
296:         LiquidationRecoveryModeLocals memory _recoveryState
297:     ) private returns (LiquidationRecoveryModeLocals memory) {

337:                 collSurplusPool.increaseSurplusCollShares(_borrower, _collSurplus);

367:         emit CdpLiquidated(
368:             _recoveryState.cdpId,
369:             _borrower,
370:             _totalDebtToBurn,
371:             // please note this is the collateral share of the liquidated CDP
372:             _cappedColPortion,
373:             CdpOperation.liquidateInRecoveryMode,
374:             msg.sender,
375:             _cappedColl > _debtToColl ? (_cappedColl - _debtToColl) : 0
376:         );

466:     function _reInsertPartialLiquidation(
467:         LiquidationLocals memory _partialState,
468:         uint256 _newNICR,
469:         uint256 _oldDebt,
470:         uint256 _oldColl
471:     ) internal {

484:         sortedCdps.reInsert(
485:             _cdpId,
486:             _newNICR,
487:             _partialState.upperPartialHint,
488:             _partialState.lowerPartialHint
489:         );
490:         emit CdpUpdated(
491:             _cdpId,
492:             sortedCdps.getOwnerAddress(_cdpId),
493:             msg.sender,
494:             _oldDebt,
495:             _oldColl,
496:             Cdps[_cdpId].debt,
497:             Cdps[_cdpId].coll,
498:             Cdps[_cdpId].stake,
499:             CdpOperation.partiallyLiquidate
500:         );

```
[L295](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L295), [L337](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L337), [L367](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L367), [L466](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L466), [L484](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L484)

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

574:     function _takeSplitAndUpdateFeePerUnit(
575:         uint256 _feeTaken,
576:         uint256 _newPerUnit,
577:         uint256 _newErrorPerUnit
578:     ) internal {

585:         activePool.allocateSystemCollSharesToFeeRecipient(_feeTaken);

587:         emit CollateralFeePerUnitUpdated(_oldPerUnit, _newPerUnit, _feeTaken);

```
[L574](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L574), [L585](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L585), [L587](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L587)

```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

142:     function sweepToken(address token, uint256 amount) public nonReentrant requiresAuth {

148:         IERC20(token).safeTransfer(feeRecipientAddress, amount);

150:         emit SweepTokenSuccess(token, amount, feeRecipientAddress);

```
[L142](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L142), [L148](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L148), [L150](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L150)

```solidity
File: packages/contracts/contracts/PriceFeed.sol

358:     function setFallbackCaller(address _fallbackCaller) external requiresAuth {

364:             try newFallbackCaler.getFallbackResponse() returns (
365:                 uint256 answer,
366:                 uint256 timestampRetrieved,
367:                 bool success
368:             ) {

372:                 if (
373:                     !_fallbackIsBroken(fallbackResponse) &&
374:                     !_responseTimeout(fallbackResponse.timestamp, newFallbackCaler.fallbackTimeout())
375:                 ) {

378:                     emit FallbackCallerChanged(oldFallbackCaller, _fallbackCaller);

```
[L358](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L358), [L364](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L364), [L372](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L372), [L378](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L378)

</details>

&nbsp;
## [N-20] Event missing `msg.sender` parameter

When an action is triggered based on a user's action, not being able to
filter based on who triggered the action makes event processing a lot
more cumbersome. Including the `msg.sender` the events of these types of
action will make events much more useful to end users, especially when
`msg.sender` is not `tx.origin`.

<details>
<summary>Instances: 54</summary>

```solidity
File: packages/contracts/contracts/ActivePool.sol

113:         emit CollSharesTransferred(_account, _shares);

146:         emit CollSharesTransferred(_account, totalShares);

174:         emit FeeRecipientClaimableCollSharesIncreased(cachedFeeRecipientCollShares, _shares);

200:         emit ActivePoolEBTCDebtUpdated(cachedSystemDebt);

213:         emit ActivePoolEBTCDebtUpdated(cachedSystemDebt);

247:         emit SystemCollSharesUpdated(cachedSystemCollShares);

307:         emit FlashLoanSuccess(address(receiver), token, amount, fee);

360:         emit FeeRecipientClaimableCollSharesDecreased(cachedFeeRecipientCollShares, _shares);

383:         emit SweepTokenSuccess(token, amount, cachedFeeRecipientAddress);

399:         emit FeeRecipientAddressChanged(_feeRecipientAddress);

```
[L113](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L113), [L146](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L146), [L174](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L174), [L200](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L200), [L213](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L213), [L247](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L247), [L307](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L307), [L360](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L360), [L383](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L383), [L399](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L399)

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

641:         emit PositionManagerApprovalSet(_borrower, _positionManager, _approval);

1105:         emit FlashLoanSuccess(address(receiver), token, amount, fee);

1149:         emit FeeRecipientAddressChanged(_feeRecipientAddress);

```
[L641](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L641), [L1105](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1105), [L1149](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1149)

```solidity
File: packages/contracts/contracts/CdpManager.sol

630:         emit BaseRateUpdated(newBaseRate);

681:         emit BaseRateUpdated(decayedBaseRate);

698:             emit LastRedemptionTimestampUpdated(block.timestamp);

782:         emit StakingRewardSplitSet(_stakingRewardSplit);

801:         emit RedemptionFeeFloorSet(_redemptionFeeFloor);

824:         emit MinuteDecayFactorSet(_minuteDecayFactor);

836:         emit BetaSet(_beta);

848:         emit RedemptionsPaused(_paused);

```
[L630](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L630), [L681](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L681), [L698](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L698), [L782](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L782), [L801](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L801), [L824](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L824), [L836](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L836), [L848](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L848)

```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

516:         emit Liquidation(totalDebtToBurn, totalCollSharesToSend, totalLiquidatorRewardCollShares);

891:         emit SystemDebtRedistributionIndexUpdated(systemDebtRedistributionIndex);

```
[L516](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L516), [L891](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L891)

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

55:             emit GracePeriodStart();

69:             emit GracePeriodEnd();

119:         emit GracePeriodDurationSet(_gracePeriod);

300:         emit SystemSnapshotsUpdated(_totalStakesSnapshot, _totalCollateralSnapshot);

340:         emit CdpDebtRedistributionIndexUpdated(_cdpId, _systemDebtRedistributionIndex);

414:         emit TotalStakesUpdated(_newTotalStakes);

425:         emit TotalStakesUpdated(_newTotalStakes);

481:         emit CdpArrayIndexUpdated(idToMove, index);

542:             emit StEthIndexUpdated(_oldIndex, _newIndex, block.timestamp);

587:         emit CollateralFeePerUnitUpdated(_oldPerUnit, _newPerUnit, _feeTaken);

602:         emit CdpFeeSplitApplied(
603:             _cdpId,
604:             _oldPerUnitCdp,
605:             _systemStEthFeePerUnitIndex,
606:             _feeSplitDistributed,
607:             _newColl
608:         );

```
[L55](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L55), [L69](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L69), [L119](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L119), [L300](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L300), [L340](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L340), [L414](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L414), [L425](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L425), [L481](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L481), [L542](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L542), [L587](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L587), [L602](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L602)

```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

83:         emit SurplusCollSharesUpdated(_account, newAmount);

104:         emit CollSharesTransferred(_account, claimableColl);

150:         emit SweepTokenSuccess(token, amount, feeRecipientAddress);

```
[L83](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L83), [L104](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L104), [L150](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L150)

```solidity
File: packages/contracts/contracts/EBTCToken.sol

259:         emit Transfer(sender, recipient, amount);

267:         emit Transfer(address(0), account, amount);

282:         emit Transfer(account, address(0), amount);

290:         emit Approval(owner, spender, amount);

```
[L259](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L259), [L267](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L267), [L282](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L282), [L290](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L290)

```solidity
File: packages/contracts/contracts/Governor.sol

157:         emit RoleNameSet(role, roleName);

```
[L157](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L157)

```solidity
File: packages/contracts/contracts/PriceFeed.sol

387:             emit FallbackCallerChanged(oldFallbackCaller, _fallbackCaller);

548:         emit PriceFeedStatusChanged(_status);

555:         emit LastGoodPriceUpdated(_currentPrice);

```
[L387](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L387), [L548](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L548), [L555](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L555)

```solidity
File: packages/contracts/contracts/SortedCdps.sol

405:         emit NodeAdded(_id, _NICR);

451:             emit NodeRemoved(_ids[i]);

490:         emit NodeRemoved(_id);

```
[L405](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L405), [L451](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L451), [L490](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L490)

```solidity
File: packages/contracts/contracts/LeverageMacroFactory.sol

56:         emit DeployNewMacro(_owner, addy);

```
[L56](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L56)

```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

62:         emit AuthorityUpdated(address(this), Authority(newAuthority));

```
[L62](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L62)

```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

101:         emit PublicCapabilityUpdated(target, functionSig, enabled);

129:         emit RoleCapabilityUpdated(role, target, functionSig, enabled);

140:         emit CapabilityBurned(target, functionSig);

163:         emit UserRoleUpdated(user, role, enabled);

```
[L101](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L101), [L129](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L129), [L140](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L140), [L163](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L163)

</details>

&nbsp;
## [N-21] Events should use parameters

It is recommended that events make use of parameters so that they
convey all relevant information when emitted.

<details>
<summary>Instances: 2</summary>

```solidity
File: packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol

9:     event GracePeriodStart();
10:     event GracePeriodEnd();

```
[L9](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol#L9)

</details>

&nbsp;
## [N-22] Use `indexed` for event parameters

Index event fields make the field more quickly accessible to 
[off-chain tools](https://ethereum.stackexchange.com/questions/40396/can-somebody-please-explain-the-concept-of-event-indexing)
that parse events. This is especially useful when it comes to filtering based
on an address. However, note that each index field costs extra gas during
emission, so it's not necessarily best to index the maximum allowed per event
(three fields).

Where applicable, each event should use three `indexed` fields if there are three
or more fields, and gas usage is not particularly of concern for the events in
question. If there are fewer than three applicable fields, all of the applicable
fields should be indexed.

<details>
<summary>Instances: 26</summary>

```solidity
File: packages/contracts/contracts/Interfaces/IActivePool.sol

9:     event ActivePoolEBTCDebtUpdated(uint256 _EBTCDebt);
10:     event SystemCollSharesUpdated(uint256 _coll);

12:     event FeeRecipientClaimableCollSharesIncreased(uint256 _coll, uint256 _fee);
13:     event FeeRecipientClaimableCollSharesDecreased(uint256 _coll, uint256 _fee);

```
[L9](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IActivePool.sol#L9), [L12](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IActivePool.sol#L12)

```solidity
File: packages/contracts/contracts/Interfaces/ICdpManagerData.sol

17:     event StakingRewardSplitSet(uint256 _stakingRewardSplit);
18:     event RedemptionFeeFloorSet(uint256 _redemptionFeeFloor);
19:     event MinuteDecayFactorSet(uint256 _minuteDecayFactor);
20:     event BetaSet(uint256 _beta);

23:     event Liquidation(uint256 _liquidatedDebt, uint256 _liquidatedColl, uint256 _liqReward);

60:     event BaseRateUpdated(uint256 _baseRate);
61:     event LastRedemptionTimestampUpdated(uint256 _lastFeeOpTime);
62:     event TotalStakesUpdated(uint256 _newTotalStakes);
63:     event SystemSnapshotsUpdated(uint256 _totalStakesSnapshot, uint256 _totalCollateralSnapshot);
64:     event SystemDebtRedistributionIndexUpdated(uint256 _systemDebtRedistributionIndex);
65:     event CdpDebtRedistributionIndexUpdated(bytes32 _cdpId, uint256 _cdpDebtRedistributionIndex);
66:     event CdpArrayIndexUpdated(bytes32 _cdpId, uint256 _newIndex);
67:     event StEthIndexUpdated(uint256 _oldIndex, uint256 _newIndex, uint256 _updTimestamp);
68:     event CollateralFeePerUnitUpdated(uint256 _oldPerUnit, uint256 _newPerUnit, uint256 _feeTaken);
69:     event CdpFeeSplitApplied(
70:         bytes32 _cdpId,
71:         uint256 _oldPerUnitCdp,
72:         uint256 _newPerUnitCdp,
73:         uint256 _collReduced,
74:         uint256 _collLeft
75:     );

```
[L17](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L17), [L23](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L23), [L60](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L60)

```solidity
File: packages/contracts/contracts/Interfaces/IFallbackCaller.sol

7:     event FallbackTimeOutChanged(uint256 _oldTimeOut, uint256 _newTimeOut);

```
[L7](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IFallbackCaller.sol#L7)

```solidity
File: packages/contracts/contracts/Interfaces/IPool.sol

9:     event ETHBalanceUpdated(uint256 _newBalance);
10:     event EBTCBalanceUpdated(uint256 _newBalance);

```
[L9](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPool.sol#L9)

```solidity
File: packages/contracts/contracts/Interfaces/IPriceFeed.sol

7:     event LastGoodPriceUpdated(uint256 _lastGoodPrice);

```
[L7](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPriceFeed.sol#L7)

```solidity
File: packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol

6:     event TCRNotified(uint256 TCR); /// NOTE: Mostly for debugging to ensure synch

11:     event GracePeriodDurationSet(uint256 _recoveryModeGracePeriodDuration);

```
[L6](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol#L6), [L11](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol#L11)

```solidity
File: packages/contracts/contracts/Interfaces/ISortedCdps.sol

9:     event NodeAdded(bytes32 _id, uint _NICR);

```
[L9](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L9)

</details>

&nbsp;
## [N-23] Avoid function calls within for loops

Making function calls within loops in Solidity can lead to inefficient gas usage,
potential bottlenecks, and increased vulnerability to attacks. Each function call
or external call consumes gas, and when executed within a loop, the gas cost
multiplies, potentially causing the transaction to run out of gas or exceed block
gas limits. This can result in transaction failure or unpredictable behavior.

<details>
<summary>Instances: 6</summary>

```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

753:         for (vars.i = _start; ; ) {
754:             vars.cdpId = _cdpArray[vars.i];
755:             // only for active cdps
756:             if (vars.cdpId != bytes32(0) && Cdps[vars.cdpId].status == Status.active) {
757:                 vars.ICR = getSyncedICR(vars.cdpId, _price);

759:                 if (
760:                     !vars.backToNormalMode &&
761:                     (_checkICRAgainstMCR(vars.ICR) || canLiquidateRecoveryMode(vars.ICR, _TCR))
762:                 ) {
763:                     vars.price = _price;
764:                     _syncAccounting(vars.cdpId);
765:                     _getLiquidationValuesRecoveryMode(
766:                         _price,
767:                         vars.entireSystemDebt,
768:                         vars.entireSystemColl,
769:                         vars,
770:                         singleLiquidation
771:                     );

773:                     // Update aggregate trackers
774:                     vars.entireSystemDebt = vars.entireSystemDebt - singleLiquidation.debtToBurn;
775:                     vars.entireSystemColl =
776:                         vars.entireSystemColl -
777:                         singleLiquidation.totalCollToSendToLiquidator -
778:                         singleLiquidation.collSurplus;

780:                     // Add liquidation values to their respective running totals
781:                     totals = _addLiquidationValuesToTotals(totals, singleLiquidation);

783:                     _TCR = _computeTCRWithGivenSystemValues(
784:                         vars.entireSystemColl,
785:                         vars.entireSystemDebt,
786:                         _price
787:                     );
788:                     vars.backToNormalMode = _TCR < CCR ? false : true;
789:                     _liqFlags[vars.i] = true;
790:                 } else if (vars.backToNormalMode && _checkICRAgainstMCR(vars.ICR)) {
791:                     _syncAccounting(vars.cdpId);
792:                     _getLiquidationValuesNormalMode(_price, _TCR, vars, singleLiquidation);

794:                     // Add liquidation values to their respective running totals
795:                     totals = _addLiquidationValuesToTotals(totals, singleLiquidation);
796:                     _liqFlags[vars.i] = true;
797:                 }
798:                 // In Normal Mode skip cdps with ICR >= MCR
799:             }
800:             ++vars.i;
801:             if (vars.i == _cnt) {
802:                 break;
803:             }
804:         }

816:         for (vars.i = _start; ; ) {
817:             vars.cdpId = _cdpArray[vars.i];
818:             // only for active cdps
819:             if (vars.cdpId != bytes32(0) && Cdps[vars.cdpId].status == Status.active) {
820:                 vars.ICR = getSyncedICR(vars.cdpId, _price);

822:                 if (_checkICRAgainstMCR(vars.ICR)) {
823:                     _syncAccounting(vars.cdpId);
824:                     _getLiquidationValuesNormalMode(_price, _TCR, vars, singleLiquidation);

826:                     // Add liquidation values to their respective running totals
827:                     totals = _addLiquidationValuesToTotals(totals, singleLiquidation);
828:                 }
829:             }
830:             ++vars.i;
831:             if (vars.i == _cnt) {
832:                 break;
833:             }
834:         }

```
[L753](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L753), [L759](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L759), [L773](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L773), [L780](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L780), [L783](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L783), [L794](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L794), [L816](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L816), [L822](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L822), [L826](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L826)

```solidity
File: packages/contracts/contracts/SortedCdps.sol

432:         for (uint256 i = 0; i < _len; ++i) {
433:             require(contains(_ids[i]), "SortedCdps: List does not contain the id");
434:         }

```
[L432](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L432)

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

385:         for (uint256 i; i < swapLength; ) {
386:             _doSwap(swapData[i]);
387:             unchecked {
388:                 ++i;
389:             }
390:         }

438:             for (uint256 i; i < length; ++i) {
439:                 // > because if you don't want to check for 0, just don't have the check
440:                 require(
441:                     IERC20(swapChecks[i].tokenToCheck).balanceOf(address(this)) >
442:                         swapChecks[i].expectedMinOut,
443:                     "LeverageMacroReference: swap check failure!"
444:                 );
445:             }

```
[L385](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L385), [L438](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L438)

```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

114:         for (uint256 i; i < length; ) {
115:             _executeOne(ops[i]);

117:             unchecked {
118:                 ++i;
119:             }
120:         }

```
[L114](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L114), [L117](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L117)

</details>

&nbsp;
## [N-24] Function names should use mixedCase

See the
[Solidity style guide](https://docs.soliditylang.org/en/v0.8.17/style-guide.html#function-names)
for more info.

<details>
<summary>Instances: 5</summary>

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

659:     function DOMAIN_SEPARATOR() external view returns (bytes32) {

```
[L659](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L659)

```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

733:     function _getTotalFromBatchLiquidate_RecoveryMode(
734:         uint256 _price,
735:         uint256 _systemCollShares,
736:         uint256 _systemDebt,
737:         bytes32[] memory _cdpArray
738:     ) internal returns (LiquidationTotals memory totals) {

807:     function _getTotalsFromBatchLiquidate_NormalMode(
808:         uint256 _price,
809:         uint256 _TCR,
810:         bytes32[] memory _cdpArray
811:     ) internal returns (LiquidationTotals memory totals) {

```
[L733](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L733), [L807](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L807)

```solidity
File: packages/contracts/contracts/EBTCToken.sol

176:     function DOMAIN_SEPARATOR() external view returns (bytes32) {

```
[L176](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L176)

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

15:     function Cdps(bytes32) external view returns (ICdpManagerData.Cdp memory);

```
[L15](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L15)

</details>

&nbsp;
## [N-25] Functions that alter state should emit events

Events cause the passed arguments to be stored in the transaction's log,
which is a special data structure in the blockchain. Events notify external
users, such as a listening frontend website or client application, that
something has happened on the blockchain.

<details>
<summary>Instances: 6</summary>

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

168:     function openCdp(
169:         uint256 _debt,
170:         bytes32 _upperHint,
171:         bytes32 _lowerHint,
172:         uint256 _stEthBalance
173:     ) external override nonReentrantSelfAndCdpM returns (bytes32) {
174:         return _openCdp(_debt, _upperHint, _lowerHint, _stEthBalance, msg.sender);
175:     }

187:     function openCdpFor(
188:         uint256 _debt,
189:         bytes32 _upperHint,
190:         bytes32 _lowerHint,
191:         uint256 _stEthBalance,
192:         address _borrower
193:     ) external override nonReentrantSelfAndCdpM returns (bytes32) {
194:         return _openCdp(_debt, _upperHint, _lowerHint, _stEthBalance, _borrower);
195:     }

599:     function claimSurplusCollShares() external override {
600:         // send ETH from CollSurplus Pool to owner
601:         collSurplusPool.claimSurplusCollShares(msg.sender);
602:     }

```
[L168](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L168), [L187](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L187), [L599](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L599)

```solidity
File: packages/contracts/contracts/LeverageMacroDelegateTarget.sol

63:     function owner() public override returns (address) {
64:         address _owner = IOwnerLike(address(this)).owner();
65:         return _owner;
66:     }

```
[L63](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L63)

```solidity
File: packages/contracts/contracts/LeverageMacroFactory.sol

38:     function deployNewMacro() external returns (address) {
39:         return deployNewMacro(msg.sender);
40:     }

```
[L38](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L38)

```solidity
File: packages/contracts/contracts/LeverageMacroReference.sol

44:     function owner() public override returns (address) {
45:         return theOwner;
46:     }

```
[L44](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L44)

</details>

&nbsp;
## [N-26] Function order doesn't follow Solidity style guide

The [Solidity style guide](https://docs.soliditylang.org/en/v0.8.17/style-guide.html#order-of-functions)
states that functions should be laid out in the following order: `constructor`,
`receive`, `fallback`, `external`, `public`, `internal`, `private`. In the
following contracts, this is not the case.

<details>
<summary>Instances: 15</summary>

```solidity
File: packages/contracts/contracts/ActivePool.sol

22: contract ActivePool is IActivePool, ERC3156FlashLender, ReentrancyGuard, BaseMath, AuthNoOwner {

```
[L22](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L22)

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

21: contract BorrowerOperations is

```
[L21](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L21)

```solidity
File: packages/contracts/contracts/CdpManager.sol

16: contract CdpManager is CdpManagerStorage, ICdpManager, Proxy {

```
[L16](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L16)

```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

13: contract LiquidationLibrary is CdpManagerStorage {

```
[L13](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L13)

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

19: contract CdpManagerStorage is EbtcBase, ReentrancyGuard, ICdpManagerData, AuthNoOwner {

```
[L19](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L19)

```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

16: contract CollSurplusPool is ICollSurplusPool, ReentrancyGuard, AuthNoOwner {

```
[L16](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L16)

```solidity
File: packages/contracts/contracts/EBTCToken.sol

26: contract EBTCToken is IEBTCToken, AuthNoOwner, PermitNonce {

```
[L26](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L26)

```solidity
File: packages/contracts/contracts/Governor.sol

13: contract Governor is RolesAuthority {

```
[L13](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L13)

```solidity
File: packages/contracts/contracts/SortedCdps.sol

51: contract SortedCdps is ISortedCdps {

```
[L51](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L51)

```solidity
File: packages/contracts/contracts/HintHelpers.sol

11: contract HintHelpers is EbtcBase {

```
[L11](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L11)

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

26: contract LeverageMacroBase {

```
[L26](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L26)

```solidity
File: packages/contracts/contracts/LeverageMacroReference.sol

11: contract LeverageMacroReference is LeverageMacroBase {

```
[L11](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L11)

```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

25: contract SimplifiedDiamondLike {

```
[L25](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L25)

```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

10: contract AuthNoOwner {

```
[L10](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L10)

```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

16: contract EbtcBase is BaseMath, IEbtcBase {

```
[L16](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L16)

</details>

&nbsp;
## [N-27] High Cyclomatic Complexity in Functions

Functions with high cyclomatic complexity are harder to understand, test, and
maintain. Consider breaking down these blocks into more manageable units, by
splitting things into utility functions, by reducing nesting, and by using
early returns.

See [here](https://en.wikipedia.org/wiki/Cyclomatic_complexity) for more
information on cyclomatic complexity.

<details>
<summary>Instances: 12</summary>

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

328:     function _adjustCdpInternal(
329:         bytes32 _cdpId,
330:         uint256 _stEthBalanceDecrease,
331:         uint256 _debtChange,
332:         bool _isDebtIncrease,
333:         bytes32 _upperHint,
334:         bytes32 _lowerHint,
335:         uint256 _stEthBalanceIncrease
336:     ) internal {

439:     function _openCdp(
440:         uint256 _debt,
441:         bytes32 _upperHint,
442:         bytes32 _lowerHint,
443:         uint256 _stEthBalance,
444:         address _borrower
445:     ) internal returns (bytes32) {

```
[L328](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L328), [L439](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L439)

```solidity
File: packages/contracts/contracts/CdpManager.sol

135:     function _redeemCollateralFromCdp(
136:         SingleRedemptionInputs memory _redeemColFromCdp
137:     ) internal returns (SingleRedemptionValues memory singleRedemption) {

320:     function redeemCollateral(
321:         uint256 _debt,
322:         bytes32 _firstRedemptionHint,
323:         bytes32 _upperPartialRedemptionHint,
324:         bytes32 _lowerPartialRedemptionHint,
325:         uint256 _partialRedemptionHintNICR,
326:         uint256 _maxIterations,
327:         uint256 _maxFeePercentage
328:     ) external override nonReentrantSelfAndBOps {

```
[L135](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L135), [L320](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L320)

```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

295:     function _liquidateIndividualCdpSetupCDPInRecoveryMode(
296:         LiquidationRecoveryModeLocals memory _recoveryState
297:     ) private returns (LiquidationRecoveryModeLocals memory) {

733:     function _getTotalFromBatchLiquidate_RecoveryMode(
734:         uint256 _price,
735:         uint256 _systemCollShares,
736:         uint256 _systemDebt,
737:         bytes32[] memory _cdpArray
738:     ) internal returns (LiquidationTotals memory totals) {

```
[L295](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L295), [L733](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L733)

```solidity
File: packages/contracts/contracts/PriceFeed.sol

98:     function fetchPrice() external override returns (uint256) {

606:     function _getCurrentChainlinkResponse()
607:         internal
608:         view
609:         returns (ChainlinkResponse memory chainlinkResponse)
610:     {

687:     function _getPrevChainlinkResponse(
688:         uint80 _currentRoundEthBtcId,
689:         uint80 _currentRoundStEthEthId
690:     ) internal view returns (ChainlinkResponse memory prevChainlinkResponse) {

```
[L98](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L98), [L606](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L606), [L687](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L687)

```solidity
File: packages/contracts/contracts/SortedCdps.sol

363:     function _insert(bytes32 _id, uint256 _NICR, bytes32 _prevId, bytes32 _nextId) internal {

```
[L363](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L363)

```solidity
File: packages/contracts/contracts/HintHelpers.sol

48:     function getRedemptionHints(
49:         uint256 _EBTCamount,
50:         uint256 _price,
51:         uint256 _maxIterations
52:     )
53:         external
54:         view
55:         returns (
56:             bytes32 firstRedemptionHint,
57:             uint256 partialRedemptionHintNICR,
58:             uint256 truncatedEBTCamount,
59:             uint256 partialRedemptionNewColl
60:         )
61:     {

```
[L48](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L48)

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

118:     function doOperation(
119:         FlashLoanType flType,
120:         uint256 borrowAmount,
121:         LeverageMacroOperation calldata operation,
122:         PostOperationCheck postCheckType,
123:         PostCheckParams calldata checkParams
124:     ) external {

```
[L118](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L118)

</details>

&nbsp;
## [N-28] `address` parameters should be sanitized

Implement a zero address check in functions with `address` parameters to
prevent unexpected behaviour.

<details>
<summary>Instances: 82</summary>

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

187:     function openCdpFor(
188:         uint256 _debt,
189:         bytes32 _upperHint,
190:         bytes32 _lowerHint,
191:         uint256 _stEthBalance,
192:         address _borrower
193:     ) external override nonReentrantSelfAndCdpM returns (bytes32) {

608:     function getPositionManagerApproval(
609:         address _borrower,
610:         address _positionManager
611:     ) external view override returns (PositionManagerApproval) {

615:     function _getPositionManagerApproval(
616:         address _borrower,
617:         address _positionManager
618:     ) internal view returns (PositionManagerApproval) {

635:     function _setPositionManagerApproval(
636:         address _borrower,
637:         address _positionManager,
638:         PositionManagerApproval _approval
639:     ) internal {

790:     function _withdrawDebt(address _account, uint256 _debt) internal {

796:     function _repayDebt(address _account, uint256 _debt) internal {

824:     function _requireCdpisActive(ICdpManager _cdpManager, bytes32 _cdpId) internal view {

986:     function _getNewNominalICRFromCdpChange(
987:         AdjustCdpLocals memory vars,
988:         bool _isDebtIncrease
989:     ) internal pure returns (uint256) {

```
[L187](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L187), [L608](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L608), [L615](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L615), [L635](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L635), [L790](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L790), [L796](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L796), [L824](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L824), [L986](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L986)

```solidity
File: packages/contracts/contracts/CdpManager.sol

244:     function _closeCdpByRedemption(
245:         bytes32 _cdpId,
246:         uint256 _EBTC,
247:         uint256 _collSurplus,
248:         uint256 _liquidatorRewardShares,
249:         address _borrower
250:     ) internal {

538:     function closeCdp(
539:         bytes32 _cdpId,
540:         address _borrower,
541:         uint256 _debt,
542:         uint256 _coll
543:     ) external override {

737:     function _requireEbtcBalanceCoversRedemptionAndWithinSupply(
738:         address _redeemer,
739:         uint256 _amount,
740:         uint256 _totalSupply
741:     ) internal view {

905:     function initializeCdp(
906:         bytes32 _cdpId,
907:         uint256 _debt,
908:         uint256 _coll,
909:         uint256 _liquidatorRewardShares,
910:         address _borrower
911:     ) external {

946:     function updateCdp(
947:         bytes32 _cdpId,
948:         address _borrower,
949:         uint256 _coll,
950:         uint256 _debt,
951:         uint256 _newColl,
952:         uint256 _newDebt
953:     ) external {

```
[L244](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L244), [L538](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L538), [L737](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L737), [L905](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L905), [L946](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L946)

```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

135:     function _liquidateIndividualCdpSetupCDP(
136:         LiquidationLocals memory _liqState,
137:         LiquidationRecoveryModeLocals memory _recoveryState
138:     ) internal {

186:     function _liquidateCdpInGivenMode(
187:         LiquidationLocals memory _liqState,
188:         LiquidationRecoveryModeLocals memory _recoveryState
189:     ) private returns (uint256, uint256, uint256, uint256, uint256) {

223:     function _liquidateIndividualCdpSetupCDPInNormalMode(
224:         LiquidationLocals memory _liqState
225:     ) private returns (LiquidationLocals memory) {

295:     function _liquidateIndividualCdpSetupCDPInRecoveryMode(
296:         LiquidationRecoveryModeLocals memory _recoveryState
297:     ) private returns (LiquidationRecoveryModeLocals memory) {

608:     function _getLiquidationValuesNormalMode(
609:         uint256 _price,
610:         uint256 _TCR,
611:         LocalVariables_LiquidationSequence memory vars,
612:         LiquidationValues memory singleLiquidation
613:     ) internal {

642:     function _getLiquidationValuesRecoveryMode(
643:         uint256 _price,
644:         uint256 _systemDebt,
645:         uint256 _systemCollShares,
646:         LocalVariables_LiquidationSequence memory vars,
647:         LiquidationValues memory singleLiquidation
648:     ) internal {

839:     function _addLiquidationValuesToTotals(
840:         LiquidationTotals memory oldTotals,
841:         LiquidationValues memory singleLiquidation
842:     ) internal pure returns (LiquidationTotals memory newTotals) {

```
[L135](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L135), [L186](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L186), [L223](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L223), [L295](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L295), [L608](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L608), [L642](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L642), [L839](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L839)

```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

67:     function getSurplusCollShares(address _account) external view override returns (uint256) {

77:     function increaseSurplusCollShares(address _account, uint256 _amount) external override {

89:     function claimSurplusCollShares(address _account) external override {

```
[L67](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L67), [L77](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L77), [L89](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L89)

```solidity
File: packages/contracts/contracts/EBTCToken.sol

115:     function balanceOf(address account) external view override returns (uint256) {

125:     function allowance(address owner, address spender) external view override returns (uint256) {

225:     function nonces(address owner) external view override(IERC2612, PermitNonce) returns (uint256) {

```
[L115](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L115), [L125](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L125), [L225](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L225)

```solidity
File: packages/contracts/contracts/Governor.sol

131:     function getEnabledFunctionsInTarget(
132:         address _target
133:     ) public view returns (bytes4[] memory _funcs) {

```
[L131](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L131)

```solidity
File: packages/contracts/contracts/PriceFeed.sol

400:     function _chainlinkIsBroken(
401:         ChainlinkResponse memory _currentResponse,
402:         ChainlinkResponse memory _prevResponse
403:     ) internal view returns (bool) {

435:     function _chainlinkIsFrozen(ChainlinkResponse memory _response) internal view returns (bool) {

445:     function _chainlinkPriceChangeAboveMax(
446:         ChainlinkResponse memory _currentResponse,
447:         ChainlinkResponse memory _prevResponse
448:     ) internal pure returns (bool) {

485:     function _fallbackIsFrozen(
486:         FallbackResponse memory _fallbackResponse
487:     ) internal view returns (bool) {

526:     function _bothOraclesSimilarPrice(
527:         ChainlinkResponse memory _chainlinkResponse,
528:         FallbackResponse memory _fallbackResponse
529:     ) internal pure returns (bool) {

546:     function _changeStatus(Status _status) internal {

```
[L400](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L400), [L435](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L435), [L445](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L445), [L485](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L485), [L526](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L526), [L546](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L546)

```solidity
File: packages/contracts/contracts/SortedCdps.sol

105:     function toCdpId(
106:         address owner,
107:         uint256 blockHeight,
108:         uint256 nonce
109:     ) public pure returns (bytes32) {

140:     function cdpOfOwnerByIndex(
141:         address owner,
142:         uint256 index
143:     ) external view override returns (bytes32) {

155:     function cdpOfOwnerByIdx(
156:         address owner,
157:         uint256 index,
158:         bytes32 startNodeId,
159:         uint maxNodes
160:     ) external view override returns (bytes32, bool) {

216:     function cdpCountOf(address owner) external view override returns (uint256) {

227:     function getCdpCountOf(
228:         address owner,
229:         bytes32 startNodeId,
230:         uint maxNodes
231:     ) external view override returns (uint256, bytes32) {

270:     function getCdpsOf(address owner) external view override returns (bytes32[] memory cdps) {

286:     function getAllCdpsOf(
287:         address owner,
288:         bytes32 startNodeId,
289:         uint maxNodes
290:     ) external view override returns (bytes32[] memory, uint256, bytes32) {

344:     function insert(
345:         address owner,
346:         uint256 _NICR,
347:         bytes32 _prevId,
348:         bytes32 _nextId
349:     ) external override returns (bytes32) {

```
[L105](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L105), [L140](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L140), [L155](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L155), [L216](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L216), [L227](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L227), [L270](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L270), [L286](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L286), [L344](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L344)

```solidity
File: packages/contracts/contracts/HintHelpers.sol

133:     function _calculateCdpStateAfterPartialRedemption(
134:         LocalVariables_getRedemptionHints memory vars,
135:         uint256 currentCdpDebt,
136:         uint256 _price
137:     ) internal view returns (uint256, uint256) {

```
[L133](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L133)

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

498:     function excessivelySafeCall(
499:         address _target,
500:         uint256 _gas,
501:         uint256 _value,
502:         uint16 _maxCopy,
503:         bytes memory _calldata
504:     ) internal returns (bool, bytes memory) {

```
[L498](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L498)

```solidity
File: packages/contracts/contracts/LeverageMacroFactory.sol

43:     function deployNewMacro(address _owner) public returns (address) {

```
[L43](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L43)

```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

51:     function setFallbackHandler(bytes4 sig, address handler) external {

129:     function _setCallbackEnabledForCall(DiamondLikeStorage storage ds, bool _enabled) internal {

```
[L51](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L51), [L129](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L129)

```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

42:     function setAuthority(Authority newAuthority) public virtual {

52:     function transferOwnership(address newOwner) public virtual requiresAuth {

```
[L42](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L42), [L52](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L52)

```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

38:     function setAuthority(address newAuthority) public virtual {

55:     function _initializeAuthority(address newAuthority) internal {

```
[L38](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L38), [L55](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L55)

```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

50:     function isPublicCapability(address target, bytes4 functionSig) public view returns (bool) {

63:     function canCall(
64:         address user,
65:         address target,
66:         bytes4 functionSig
67:     ) public view virtual override returns (bool) {

106:     function setRoleCapability(
107:         uint8 role,
108:         address target,
109:         bytes4 functionSig,
110:         bool enabled
111:     ) public virtual requiresAuth {

```
[L50](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L50), [L63](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L63), [L106](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L106)

```solidity
File: packages/contracts/contracts/Interfaces/IActivePool.sol

23:     function transferSystemCollShares(address _account, uint256 _amount) external;

27:     function transferSystemCollSharesAndLiquidatorReward(
28:         address _account,
29:         uint256 _shares,
30:         uint256 _liquidatorRewardShares
31:     ) external;

41:     function setFeeRecipientAddress(address _feeRecipientAddress) external;

```
[L23](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IActivePool.sol#L23), [L27](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IActivePool.sol#L27), [L41](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IActivePool.sol#L41)

```solidity
File: packages/contracts/contracts/Interfaces/IBorrowerOperations.sol

27:     function openCdpFor(
28:         uint _EBTCAmount,
29:         bytes32 _upperHint,
30:         bytes32 _lowerHint,
31:         uint _collAmount,
32:         address _borrower
33:     ) external returns (bytes32);

```
[L27](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L27)

```solidity
File: packages/contracts/contracts/Interfaces/ICdpManager.sol

40:     function closeCdp(bytes32 _cdpId, address _borrower, uint256 _debt, uint256 _coll) external;

58:     function initializeCdp(
59:         bytes32 _cdpId,
60:         uint256 _debt,
61:         uint256 _coll,
62:         uint256 _liquidatorRewardShares,
63:         address _borrower
64:     ) external;

66:     function updateCdp(
67:         bytes32 _cdpId,
68:         address _borrower,
69:         uint256 _coll,
70:         uint256 _debt,
71:         uint256 _newColl,
72:         uint256 _newDebt
73:     ) external;

```
[L40](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol#L40), [L58](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol#L58), [L66](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol#L66)

```solidity
File: packages/contracts/contracts/Interfaces/ICollSurplusPool.sol

17:     function getSurplusCollShares(address _account) external view returns (uint256);

19:     function increaseSurplusCollShares(address _account, uint256 _amount) external;

21:     function claimSurplusCollShares(address _account) external;

```
[L17](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICollSurplusPool.sol#L17), [L19](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICollSurplusPool.sol#L19), [L21](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICollSurplusPool.sol#L21)

```solidity
File: packages/contracts/contracts/Interfaces/IEBTCToken.sol

11:     function mint(address _account, uint256 _amount) external;

13:     function burn(address _account, uint256 _amount) external;

```
[L11](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IEBTCToken.sol#L11), [L13](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IEBTCToken.sol#L13)

```solidity
File: packages/contracts/contracts/Interfaces/IERC3156FlashBorrower.sol

15:     function onFlashLoan(
16:         address initiator,
17:         address token,
18:         uint256 amount,
19:         uint256 fee,
20:         bytes calldata data
21:     ) external returns (bytes32);

```
[L15](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IERC3156FlashBorrower.sol#L15)

```solidity
File: packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol

15:     function maxFlashLoan(address token) external view returns (uint256);

21:     function flashFee(address token, uint256 amount) external view returns (uint256);

28:     function flashLoan(
29:         IERC3156FlashBorrower receiver,
30:         address token,
31:         uint256 amount,
32:         bytes calldata data
33:     ) external returns (bool);

```
[L15](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol#L15), [L21](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol#L21), [L28](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol#L28)

```solidity
File: packages/contracts/contracts/Interfaces/IPermitNonce.sol

9:     function nonces(address owner) external view returns (uint256);

```
[L9](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPermitNonce.sol#L9)

```solidity
File: packages/contracts/contracts/Interfaces/IPositionManagers.sol

18:     function getPositionManagerApproval(
19:         address _borrower,
20:         address _positionManager
21:     ) external view returns (PositionManagerApproval);

23:     function setPositionManagerApproval(
24:         address _positionManager,
25:         PositionManagerApproval _approval
26:     ) external;

28:     function revokePositionManagerApproval(address _positionManager) external;

30:     function renouncePositionManagerApproval(address _borrower) external;

32:     function permitPositionManagerApproval(
33:         address _borrower,
34:         address _positionManager,
35:         PositionManagerApproval _approval,
36:         uint _deadline,
37:         uint8 v,
38:         bytes32 r,
39:         bytes32 s
40:     ) external;

```
[L18](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPositionManagers.sol#L18), [L23](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPositionManagers.sol#L23), [L28](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPositionManagers.sol#L28), [L30](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPositionManagers.sol#L30), [L32](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPositionManagers.sol#L32)

```solidity
File: packages/contracts/contracts/Interfaces/ISortedCdps.sol

50:     function insert(
51:         address owner,
52:         uint256 _ICR,
53:         bytes32 _prevId,
54:         bytes32 _nextId
55:     ) external returns (bytes32);

61:     function cdpCountOf(address owner) external view returns (uint256);

63:     function getCdpCountOf(
64:         address owner,
65:         bytes32 startNodeId,
66:         uint maxNodes
67:     ) external view returns (uint256, bytes32);

69:     function getCdpsOf(address owner) external view returns (bytes32[] memory);

71:     function getAllCdpsOf(
72:         address owner,
73:         bytes32 startNodeId,
74:         uint maxNodes
75:     ) external view returns (bytes32[] memory, uint256, bytes32);

77:     function cdpOfOwnerByIndex(address owner, uint256 index) external view returns (bytes32);

79:     function cdpOfOwnerByIdx(
80:         address owner,
81:         uint256 index,
82:         bytes32 startNodeId,
83:         uint maxNodes
84:     ) external view returns (bytes32, bool);

```
[L50](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L50), [L61](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L61), [L63](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L63), [L69](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L69), [L71](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L71), [L77](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L77), [L79](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L79)

</details>

&nbsp;
## [N-29] Use ternary expressions over `if`/`else` where possible

Using ternary operators instead of `if`/`else` statements improves
readability and reduces the number of lines of code.

<details>
<summary>Instances: 4</summary>

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

666:         if (_chainID() == _CACHED_CHAIN_ID) {
667:             return _CACHED_DOMAIN_SEPARATOR;
668:         } else {
669:             return _buildDomainSeparator(_TYPE_HASH, _HASHED_NAME, _HASHED_VERSION);
670:         }

```
[L666](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L666)

```solidity
File: packages/contracts/contracts/SortedCdps.sol

437:         if (_firstPrev != dummyId) {
438:             data.nodes[_firstPrev].nextId = _lastNext;
439:         } else {
440:             data.head = _lastNext;
441:         }
442:         if (_lastNext != dummyId) {
443:             data.nodes[_lastNext].prevId = _firstPrev;
444:         } else {
445:             data.tail = _firstPrev;
446:         }

```
[L437](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L437)

```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

95:         if (enabled) {
96:             capabilityFlag[target][functionSig] = CapabilityFlag.Public;
97:         } else {
98:             capabilityFlag[target][functionSig] = CapabilityFlag.None;
99:         }

```
[L95](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L95)

</details>

&nbsp;
## [N-30] Variable names for `immutable` variables should be in CONSTANT_CASE

Names should consist of all capital letters, with underscores separating
words.

<details>
<summary>Instances: 44</summary>

```solidity
File: packages/contracts/contracts/ActivePool.sol

26:     address public immutable borrowerOperationsAddress;
27:     address public immutable cdpManagerAddress;
28:     address public immutable collSurplusPoolAddress;

34:     ICollateralToken public immutable collateral;

```
[L26](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L26), [L34](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L34)

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

53:     ICdpManager public immutable cdpManager;

55:     ICollSurplusPool public immutable collSurplusPool;

59:     IEBTCToken public immutable ebtcToken;

62:     ISortedCdps public immutable sortedCdps;

```
[L53](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L53), [L55](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L55), [L59](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L59), [L62](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L62)

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

126:     address public immutable borrowerOperationsAddress;

128:     ICollSurplusPool immutable collSurplusPool;

130:     IEBTCToken public immutable override ebtcToken;

132:     address public immutable liquidationLibrary;

135:     ISortedCdps public immutable sortedCdps;

152:     uint256 internal immutable deploymentStartTime;

```
[L126](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L126), [L128](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L128), [L130](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L130), [L132](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L132), [L135](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L135), [L152](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L152)

```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

21:     address public immutable borrowerOperationsAddress;
22:     address public immutable cdpManagerAddress;
23:     address public immutable activePoolAddress;
24:     address public immutable feeRecipientAddress;
25:     ICollateralToken public immutable collateral;

```
[L21](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L21)

```solidity
File: packages/contracts/contracts/EBTCToken.sol

55:     address public immutable cdpManagerAddress;
56:     address public immutable borrowerOperationsAddress;

```
[L55](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L55)

```solidity
File: packages/contracts/contracts/SortedCdps.sol

54:     address public immutable borrowerOperationsAddress;

56:     ICdpManager public immutable cdpManager;

58:     uint256 public immutable maxSize;

```
[L54](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L54), [L56](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L56), [L58](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L58)

```solidity
File: packages/contracts/contracts/HintHelpers.sol

14:     ISortedCdps public immutable sortedCdps;
15:     ICdpManager public immutable cdpManager;

```
[L14](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L14)

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

29:     IBorrowerOperations public immutable borrowerOperations;
30:     IActivePool public immutable activePool;
31:     ICdpCdps public immutable cdpManager;
32:     IEBTCToken public immutable ebtcToken;
33:     ISortedCdps public immutable sortedCdps;
34:     ICollateralToken public immutable stETH;
35:     bool internal immutable willSweep;

```
[L29](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L29)

```solidity
File: packages/contracts/contracts/LeverageMacroFactory.sol

12:     address public immutable borrowerOperations;
13:     address public immutable activePool;
14:     address public immutable cdpManager;
15:     address public immutable ebtcToken;
16:     address public immutable stETH;
17:     address public immutable sortedCdps;

```
[L12](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L12)

```solidity
File: packages/contracts/contracts/LeverageMacroReference.sol

12:     address internal immutable theOwner;

```
[L12](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L12)

```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

42:     address public immutable owner;

```
[L42](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L42)

```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

41:     IActivePool public immutable activePool;

43:     IPriceFeed public immutable override priceFeed;

46:     ICollateralToken public immutable collateral;

```
[L41](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L41), [L43](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L43), [L46](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L46)

</details>

&nbsp;
## [N-31] Visibility should be explicitly set rather than defaulting to `internal`

The default visibility for mappings and state variables is `internal`. Explicitly
defining visibility improves readability and reduces margin for error during
development, testing and auditing.

<details>
<summary>Instances: 6</summary>

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

128:     ICollSurplusPool immutable collSurplusPool;

```
[L128](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L128)

```solidity
File: packages/contracts/contracts/Governor.sol

17:     bytes32 NO_ROLES = bytes32(0);

```
[L17](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L17)

```solidity
File: packages/contracts/contracts/SortedCdps.sol

60:     uint256 constant ADDRESS_SHIFT = 96; // 8 * 12; Puts the address at leftmost bytes32 position
61:     uint256 constant BLOCK_SHIFT = 64; // 8 * 8; Puts the block value after the address

```
[L60](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L60)

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

37:     bytes32 constant FLASH_LOAN_SUCCESS = keccak256("ERC3156FlashBorrower.onFlashLoan");

```
[L37](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L37)

```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

39:     bytes32 constant DIAMOND_STORAGE_POSITION = keccak256("diamond.standard.diamond.storage");

```
[L39](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L39)

</details>

&nbsp;
## [N-32] Imports could be organized more systematically

The contract's interface should be imported first, followed by each of the
interfaces it uses, followed by all other files. The contracts below do not
follow this layout.

<details>
<summary>Instances: 11</summary>

```solidity
File: packages/contracts/contracts/ActivePool.sol

22: contract ActivePool is IActivePool, ERC3156FlashLender, ReentrancyGuard, BaseMath, AuthNoOwner {

```
[L22](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L22)

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

21: contract BorrowerOperations is
22:     EbtcBase,
23:     ReentrancyGuard,
24:     IBorrowerOperations,
25:     ERC3156FlashLender,
26:     AuthNoOwner,
27:     PermitNonce
28: {

```
[L21](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L21)

```solidity
File: packages/contracts/contracts/CdpManager.sol

16: contract CdpManager is CdpManagerStorage, ICdpManager, Proxy {

```
[L16](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L16)

```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

13: contract LiquidationLibrary is CdpManagerStorage {

```
[L13](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L13)

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

19: contract CdpManagerStorage is EbtcBase, ReentrancyGuard, ICdpManagerData, AuthNoOwner {

```
[L19](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L19)

```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

16: contract CollSurplusPool is ICollSurplusPool, ReentrancyGuard, AuthNoOwner {

```
[L16](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L16)

```solidity
File: packages/contracts/contracts/Governor.sol

13: contract Governor is RolesAuthority {

```
[L13](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L13)

```solidity
File: packages/contracts/contracts/PriceFeed.sol

21: contract PriceFeed is BaseMath, IPriceFeed, AuthNoOwner {

```
[L21](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L21)

```solidity
File: packages/contracts/contracts/HintHelpers.sol

11: contract HintHelpers is EbtcBase {

```
[L11](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L11)

```solidity
File: packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol

8: abstract contract ERC3156FlashLender is IERC3156FlashLender {

```
[L8](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L8)

```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

16: contract EbtcBase is BaseMath, IEbtcBase {

```
[L16](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L16)

</details>

&nbsp;
## [N-33] Place `interface` files into a dedicated folder

Using a separate folder for interfaces keeps the codebase organised and
helps to facilitate security audits as well as future development.

<details>
<summary>Instances: 13</summary>

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

14: interface ICdpCdps {

```
[L14](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L14)

```solidity
File: packages/contracts/contracts/LeverageMacroDelegateTarget.sol

6: interface IOwnerLike {

```
[L6](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L6)

```solidity
File: packages/contracts/contracts/Interfaces/ICollSurplusPool.sol

5: interface ICollSurplusPool {

```
[L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICollSurplusPool.sol#L5)

```solidity
File: packages/contracts/contracts/Interfaces/IEbtcBase.sol

7: interface IEbtcBase {

```
[L7](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IEbtcBase.sol#L7)

```solidity
File: packages/contracts/contracts/Interfaces/IERC3156FlashBorrower.sol

5: interface IERC3156FlashBorrower {

```
[L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IERC3156FlashBorrower.sol#L5)

```solidity
File: packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol

7: interface IERC3156FlashLender {

```
[L7](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol#L7)

```solidity
File: packages/contracts/contracts/Interfaces/IFallbackCaller.sol

5: interface IFallbackCaller {

```
[L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IFallbackCaller.sol#L5)

```solidity
File: packages/contracts/contracts/Interfaces/IPermitNonce.sol

5: interface IPermitNonce {

```
[L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPermitNonce.sol#L5)

```solidity
File: packages/contracts/contracts/Interfaces/IPool.sol

6: interface IPool {

```
[L6](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPool.sol#L6)

```solidity
File: packages/contracts/contracts/Interfaces/IPositionManagers.sol

5: interface IPositionManagers {

```
[L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPositionManagers.sol#L5)

```solidity
File: packages/contracts/contracts/Interfaces/IPriceFeed.sol

5: interface IPriceFeed {

```
[L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPriceFeed.sol#L5)

```solidity
File: packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol

5: interface IRecoveryModeGracePeriod {

```
[L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol#L5)

```solidity
File: packages/contracts/contracts/Interfaces/ISortedCdps.sol

6: interface ISortedCdps {

```
[L6](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L6)

</details>

&nbsp;
## [N-34] Complex functions should include comments

Large and/or complex functions should include comments to make them easier to
understand and reduce margin for error.

<details>
<summary>Instances: 2</summary>

```solidity
File: packages/contracts/contracts/Governor.sol

96:     function getRolesFromByteMap(bytes32 byteMap) public pure returns (uint8[] memory roleIds) {

```
[L96](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L96)

```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

134:     function _executeOne(Operation calldata op) internal {

```
[L134](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L134)

</details>

&nbsp;
## [N-35] Place `library` files into a dedicated folder

Using a separate folder for libraries keeps the codebase organised and
helps to facilitate security audits as well as future development.

<details>
<summary>Instances: 1</summary>

```solidity
File: packages/contracts/contracts/Dependencies/EbtcMath.sol

5: library EbtcMath {

```
[L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L5)

</details>

&nbsp;
## [N-36] Lines too long

[Solidity's style guide](https://docs.soliditylang.org/en/v0.8.10/style-guide.html#maximum-line-length) states lines should be kept within 79 characters.
 
Also, if lines exceed 164 characters then a horizontal scroll bar will be required when viewing the file on Github.

Extensions such as prettier are a simple solution.

<details>
<summary>Instances: 269</summary>

```solidity
File: packages/contracts/contracts/ActivePool.sol

16:  * @title The Active Pool holds the collateral and EBTC debt (only accounting but not EBTC tokens) for all active cdps.

39:     /// @dev Initializes the contract with the borrowerOperationsAddress, cdpManagerAddress, collateral token address, collSurplusAddress, and feeRecipientAddress

71:     /// @dev Not necessarily equal to the the contract's raw systemCollShares balance - tokens can be forcibly sent to contracts

79:     /// @dev The amount of EBTC debt in the pool. Like systemCollShares, this is not necessarily equal to the contract's EBTC token balance - tokens can be forcibly sent to contracts

118:     /// @notice Sends stETH to a specified account, drawing from both core shares and liquidator rewards shares

119:     /// @notice Liquidator reward shares are not tracked via internal accounting in the active pool and are assumed to be present in expected amount as part of the intended behavior of BorowerOperations and CdpManager

121:     /// @dev closeCdp() or liqudations result in the actor (borrower or liquidator respectively) receiving the liquidator reward shares

122:     /// @dev Redemptions result in the shares being sent to the coll surplus pool for claiming by the CDP owner

123:     /// @dev Note that funds in the coll surplus pool, just like liquidator reward shares, are not tracked as part of the system CR or coll of a CDP.

154:     /// @dev If the fee recipient address is changed while outstanding claimable coll is available, only the new fee recipient will be able to claim the outstanding coll

177:     /// @notice Helper function to transfer stETH shares to another address, ensuring to call hooks into other system pools if they are the recipient

191:     /// @dev Managed by system contracts - requires that the caller is either BorrowerOperations or CdpManager

204:     /// @dev Managed by system contracts - requires that the caller is either BorrowerOperations or CdpManager

239:     /// @notice Notify that stETH collateral shares have been recieved, updating internal accounting accordingly

268:         uint256 fee = flashFee(token, amount); // NOTE: Check for `token` is implicit in the requires above // also checks for paused

293:         //  You technically could, but you'd be having to repay any amount below systemCollShares to get Fl2 to not revert

342:     /// @notice Claim outstanding shares for fee recipient, updating internal accounting and transferring the shares.

343:     /// @dev Call permissinos are managed via authority for flexibility, rather than gating call to just feeRecipient.

347:         ICdpManagerData(cdpManagerAddress).syncGlobalAccountingAndGracePeriod(); // Calling this increases shares so do it first

```
[L16](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L16), [L39](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L39), [L71](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L71), [L79](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L79), [L118](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L118), [L119](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L119), [L121](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L121), [L122](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L122), [L123](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L123), [L154](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L154), [L177](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L177), [L191](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L191), [L204](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L204), [L239](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L239), [L268](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L268), [L293](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L293), [L342](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L342), [L343](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L343), [L347](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L347)

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

18: /// @title BorrowerOperations is mainly in charge of all end user interactions like Cdp open, adjust, close etc

31:     // keccak256("permitPositionManagerApproval(address borrower,address positionManager,uint8 status,uint256 nonce,uint256 deadline)");

34:             "PermitPositionManagerApproval(address borrower,address positionManager,uint8 status,uint256 nonce,uint256 deadline)"

43:     // Cache the domain separator as an immutable value, but also store the chain id that it corresponds to, in order to

64:     // Mapping of borrowers to approved position managers, by approval status: cdpOwner(borrower) -> positionManager -> PositionManagerApproval (None, OneTime, Persistent)

140:         @notice BorrowerOperations and CdpManager share reentrancy status by confirming the other's locked flag before beginning operation

141:         @dev This is an alternative to the more heavyweight solution of both being able to set the reentrancy flag on a 3rd contract.

160:     /// @notice Function that creates a Cdp for the caller with the requested debt, and the stETH received as collateral.

161:     /// @notice Successful execution is conditional mainly on the resulting collateralization ratio which must exceed minimum requirement, e.g., MCR.

162:     /// @notice Upon Cdp open, a separate gas stipend (denominated in stETH) will be allocated for possible liquidation.

164:     /// @param _upperHint The expected CdpId of neighboring higher ICR within SortedCdps, could be simply bytes32(0)

165:     /// @param _lowerHint The expected CdpId of neighboring lower ICR within SortedCdps, could be simply bytes32(0)

177:     /// @notice Function that creates a Cdp for the specified _borrower by caller with the requested debt, and the stETH received as collateral.

179:     /// @notice Successful execution is conditional mainly on the resulting collateralization ratio which must exceed minimum requirement, e.g., MCR.

180:     /// @notice Upon Cdp open, a separate gas stipend (denominated in stETH) will be allocated for possible liquidation.

182:     /// @param _upperHint The expected CdpId of neighboring higher ICR within SortedCdps, could be simply bytes32(0)

183:     /// @param _lowerHint The expected CdpId of neighboring lower ICR within SortedCdps, could be simply bytes32(0)

200:     /// @param _upperHint The expected CdpId of neighboring higher ICR within SortedCdps, could be simply bytes32(0)

201:     /// @param _lowerHint The expected CdpId of neighboring lower ICR within SortedCdps, could be simply bytes32(0)

202:     /// @param _stEthBalanceIncrease The total stETH collateral amount deposited (added) for the specified Cdp

214:     /// @notice Successful execution is conditional on whether the withdrawal would bring down the ICR or TCR to the minimum requirement, e.g., MCR or CCR

216:     /// @param _stEthBalanceDecrease The total stETH collateral amount withdrawn (reduced) for the specified Cdp

217:     /// @param _upperHint The expected CdpId of neighboring higher ICR within SortedCdps, could be simply bytes32(0)

218:     /// @param _lowerHint The expected CdpId of neighboring lower ICR within SortedCdps, could be simply bytes32(0)

228:     /// @notice Function that withdraws `_debt` amount of eBTC token from the specified Cdp, thus increasing its debt accounting

230:     /// @notice Successful execution is conditional on whether the withdrawal would bring down the ICR or TCR to the minimum requirement, e.g., MCR or CCR

233:     /// @param _upperHint The expected CdpId of neighboring higher ICR within SortedCdps, could be simply bytes32(0)

234:     /// @param _lowerHint The expected CdpId of neighboring lower ICR within SortedCdps, could be simply bytes32(0)

244:     /// @notice Function that repays the received eBTC token to the specified Cdp, thus reducing its debt accounting.

247:     /// @param _upperHint The expected CdpId of neighboring higher ICR within SortedCdps, could be simply bytes32(0)

248:     /// @param _lowerHint The expected CdpId of neighboring lower ICR within SortedCdps, could be simply bytes32(0)

262:     /// @notice If end user want to add collateral and change debt at the same time, use adjustCdpWithColl() instead

267:     /// @param _isDebtIncrease The flag (true or false) to indicate whether this is a eBTC token withdrawal (debt increase) or a repayment (debt reduce)

268:     /// @param _upperHint The expected CdpId of neighboring higher ICR within SortedCdps, could be simply bytes32(0)

269:     /// @param _lowerHint The expected CdpId of neighboring lower ICR within SortedCdps, could be simply bytes32(0)

291:     /// @notice or holding more safer position (repays eBTC token and adds stETH collateral) with the specified Cdp.

296:     /// @param _isDebtIncrease The flag (true or false) to indicate whether this is a eBTC token withdrawal (debt increase) or a repayment (debt reduce)

297:     /// @param _upperHint The expected CdpId of neighboring higher ICR within SortedCdps, could be simply bytes32(0)

298:     /// @param _lowerHint The expected CdpId of neighboring lower ICR within SortedCdps, could be simply bytes32(0)

299:     /// @param _stEthBalanceIncrease The total stETH collateral amount deposited (added) for the specified Cdp

324:      * It therefore expects either a positive _stEthBalanceIncrease, or a positive _stEthBalanceDecrease argument.

392:         // When the adjustment is a debt repayment, check it's a valid amount, that the caller has enough EBTC, and that the resulting debt is >0

451:         // ICR is based on the net stEth balance, i.e. the specified stEth balance amount - fixed liquidator incentive gas comp.

468:         // ICR is based on the net coll, i.e. the requested coll amount - fixed liquidator incentive gas comp.

533:             The static liqudiation incentive is stored in the gas pool and can be considered a deposit / voucher to be returned upon Cdp close, to the closer.

534:             The close can happen from the borrower closing their own Cdp, a full liquidation, or a redemption.

537:         // CEI: Move the collateral and liquidator gas compensation to the Active Pool. Track only net collateral for TCR purposes.

549:     /// @notice Function that allows the caller to repay all debt, withdraw collateral, and close the specified Cdp

596:     /// @notice Claim remaining collateral from a redemption or from a liquidation with ICR > MCR in Recovery Mode

597:     /// @notice when a Cdp has been fully redeemed from and closed, or liquidated in Recovery Mode with a collateralization ratio higher enough (like over MCR)

598:     /// @notice the borrower is allowed to claim their stETH collateral surplus that remains in the system if any

605:     /// @return PositionManagerApproval (None/OneTime/Persistent) status for given _borrower and _positionManager

607:     /// @param _positionManager The position manager address in question whether it gets valid approval from _borrower

624:     /// @notice Position managers with 'OneTIme' status will be able to take a single action on one Cdp. Approval will be automatically revoked after one Cdp-related action.

625:     /// @notice Similar to approving tokens, approving a position manager allows _stealing of all positions_ if given to a malicious account.

626:     /// @param _positionManager The position manager address which will get the specified approval from caller

627:     /// @param _approval PositionManagerApproval (None/OneTime/Persistent) status set to the specified _positionManager for caller's Cdp

645:     /// @notice Similar to approving tokens, approving a position manager allows _stealing of all positions_ if given to a malicious account.

646:     /// @param _positionManager The position manager address which will get all approval revoked by caller (a Cdp owner)

652:     /// @param _borrower The Cdp owner address which will have all approval to the caller (a PositionManager) revoked.

691:     /// @notice This function returns hash of the fully encoded EIP712 message for the permitPositionManagerApproval.

761:         // Debt increase: mint change value of new eBTC to user, increment ActivePool eBTC internal accounting

765:             // Debt decrease: burn change value of eBTC from user, decrement ActivePool eBTC internal accounting

770:             // Coll increase: send change value of stETH to Active Pool, increment ActivePool stETH internal accounting

773:             // Coll decrease: send change value of stETH to user, decrement ActivePool stETH internal accounting

782:     /// @dev These number of liquidator shares associated with each Cdp are stored in the Cdp, while the actual tokens float in the active pool

972:             "BorrowerOperations: Only borrower account or approved position manager can OpenCdp on borrower's behalf"

977:         /// @dev If the PositionManagerApproval was none, we should have failed with the check in _requireBorrowerOrPositionManagerAndUpdateManagerApproval

1084:         uint256 fee = flashFee(token, amount); // NOTE: Check for `eBTCToken` is implicit here // NOTE: Pause check is here

1122:     /// @param token The address of the token to get the maximum flash loan amount for, exclusively used here for eBTC token

```
[L18](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L18), [L31](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L31), [L34](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L34), [L43](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L43), [L64](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L64), [L140](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L140), [L141](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L141), [L160](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L160), [L161](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L161), [L162](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L162), [L164](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L164), [L165](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L165), [L177](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L177), [L179](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L179), [L180](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L180), [L182](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L182), [L183](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L183), [L200](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L200), [L201](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L201), [L202](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L202), [L214](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L214), [L216](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L216), [L217](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L217), [L218](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L218), [L228](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L228), [L230](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L230), [L233](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L233), [L234](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L234), [L244](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L244), [L247](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L247), [L248](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L248), [L262](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L262), [L267](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L267), [L268](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L268), [L269](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L269), [L291](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L291), [L296](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L296), [L297](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L297), [L298](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L298), [L299](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L299), [L324](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L324), [L392](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L392), [L451](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L451), [L468](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L468), [L533](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L533), [L534](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L534), [L537](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L537), [L549](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L549), [L596](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L596), [L597](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L597), [L598](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L598), [L605](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L605), [L607](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L607), [L624](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L624), [L625](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L625), [L626](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L626), [L627](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L627), [L645](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L645), [L646](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L646), [L652](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L652), [L691](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L691), [L761](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L761), [L765](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L765), [L770](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L770), [L773](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L773), [L782](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L782), [L972](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L972), [L977](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L977), [L1084](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1084), [L1122](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1122)

```solidity
File: packages/contracts/contracts/CdpManager.sol

13: /// @title CdpManager is mainly in charge of all Cdp related core processing like collateral & debt accounting, split fee calculation, redemption, etc

14: /// @notice Except for redemption, end user typically will interact with BorrowerOeprations for individual Cdp actions

95:     /// @notice Fully liquidate a single Cdp by ID. Cdp must meet the criteria for liquidation at the time of execution.

96:     /// @notice callable by anyone, attempts to liquidate the CdpId. Executes successfully if Cdp meets the conditions for liquidation (e.g. in Normal Mode, it liquidates if the Cdp's ICR < the system MCR).

122:     /// @notice Steps through the provided list and attempts to liquidate every Cdp, until it reaches the end or it runs out of gas.

132:     /// @notice // Redeem as much collateral as possible from given Cdp in exchange for EBTC up to specified maximum

155:         // Decrease the debt and collateral of the current Cdp according to the EBTC lot and corresponding ETH to send

196:              * If the provided hint is out of date, we bail since trying to reinsert without a good hint will almost

242:      * Any surplus stETH left in the cdp, is sent to the Coll surplus pool, and can be later claimed by the borrower.

267:     /// @notice Returns true if the CdpId specified is the lowest-ICR Cdp in the linked list that still has MCR > ICR

271:     /// @dev Returns true if the specified CdpId is not blank, exists in the list, has an ICR > MCR, and the next lower Cdp in the list is either blank or has an ICR < MCR.

291:     /// @notice Note that if _debt is very large, this function can run out of gas, specially if traversed cdps are small (meaning many small Cdps are redeemed against).

292:     /// @notice This can be easily avoided by splitting the total _debt in appropriate chunks and calling the function multiple times.

294:     /// @notice There is a optional parameter `_maxIterations` which can also be provided, so the loop through Cdps is capped (if it’s zero, it will be ignored).

295:     /// @notice This makes it easier to avoid OOG for the frontend, as only knowing approximately the average cost of an iteration is enough,

296:     /// @notice without needing to know the "topology" of the cdp list. It also avoids the need to set the cap in stone in the contract,

299:     /// @notice All Cdps that are redeemed from -- with the likely exception of the last one -- will end up with no debt left,

301:     /// @notice If the last Cdp does have some remaining debt & collateral (it has a valid meaningful ICR) then reinsertion of the CDP

304:     /// @notice A frontend should use HintHelper.getRedemptionHints() to calculate what the ICR of this Cdp will be after redemption,

305:     /// @notice and pass a hint for its position in the SortedCdps list along with the ICR value that the hint was found for.

311:     /// @notice In this case, the redemption will stop after the last completely redeemed Cdp and the sender will keep the

314:     /// @param _firstRedemptionHint The first CdpId to be considered for redemption, could get from HintHelper.getRedemptionHints()

315:     /// @param _upperPartialRedemptionHint The first CdpId to be considered for redemption, could get from HintHelper.getApproxHint(_partialRedemptionHintNICR) then SortedCdps.findInsertPosition(_partialRedemptionHintNICR)

316:     /// @param _lowerPartialRedemptionHint The first CdpId to be considered for redemption, could get from HintHelper.getApproxHint(_partialRedemptionHintNICR) then SortedCdps.findInsertPosition(_partialRedemptionHintNICR)

317:     /// @param _partialRedemptionHintNICR The new Nominal Collateral Ratio (NICR) of the last redeemed CDP after partial redemption, could get from HintHelper.getRedemptionHints()

318:     /// @param _maxIterations The maximum allowed iteration along the SortedCdps loop, if zero then there is no limit

445:         // Decay the baseRate due to time passed, and then increase it according to the size of this redemption.

515:         /// @audit Opening can cause invalid reordering of Cdps due to changing values without reInserting into sortedCdps

549:     // Push the owner's address to the Cdp owners list, and record the corresponding array index on the Cdp struct

579:     /// @return TCR The cached total collateralization ratio (TCR) of the system (does not take into account pending global state)

626:         require(newBaseRate > 0, "CdpManager: new baseRate is zero!"); // Base rate is always non-zero after redemption

678:         require(decayedBaseRate <= DECIMAL_PRECISION, "CdpManager: baseRate too large!"); // The baseRate can decay to 0

688:     // Update the last fee operation time only if time passed >= decay interval. This prevents base rate griefing.

726:     /// @return flag (true or false) whether the system would be in Recovery Mode for specified status parameters

919:         cdpStEthFeePerUnitIndex[_cdpId] = systemStEthFeePerUnitIndex; /// @audit We critically assume global accounting is synced here

```
[L13](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L13), [L14](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L14), [L95](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L95), [L96](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L96), [L122](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L122), [L132](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L132), [L155](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L155), [L196](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L196), [L242](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L242), [L267](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L267), [L271](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L271), [L291](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L291), [L292](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L292), [L294](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L294), [L295](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L295), [L296](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L296), [L299](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L299), [L301](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L301), [L304](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L304), [L305](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L305), [L311](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L311), [L314](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L314), [L315](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L315), [L316](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L316), [L317](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L317), [L318](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L318), [L445](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L445), [L515](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L515), [L549](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L549), [L579](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L579), [L626](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L626), [L678](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L678), [L688](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L688), [L726](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L726), [L919](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L919)

```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

12: /// @dev This contract shares same base and storage layout with CdpManager and is the delegatecall destination from CdpManager

36:     /// @notice Fully liquidate a single Cdp by ID. Cdp must meet the criteria for liquidation at the time of execution.

37:     /// @notice callable by anyone, attempts to liquidate the CdpId. Executes successfully if Cdp meets the conditions for liquidation (e.g. in Normal Mode, it liquidates if the Cdp's ICR < the system MCR).

74:         uint256 _ICR = getCachedICR(_cdpId, _price); // @audit syncAccounting already called, guarenteed to be synced

133:     // liquidate given CDP by repaying debt in full or partially if its ICR is below MCR or TCR in recovery mode.

134:     // For partial liquidation, caller should use HintHelper smart contract to get correct hints for reinsertion into sorted CDP list

237:         // I don't see an issue emitting the CdpUpdated() event up here and avoiding this extra cache, any objections?

311:         // I don't see an issue emitting the CdpUpdated() event up here and avoiding an extra cache of the values, any objections?

563:         /// @audit MUST be like so, else we have debt redistribution, which we assume cannot happen in partial

675:     /// @notice Steps through the provided list and attempts to liquidate every Cdp, until it reaches the end or it runs out of gas.

869:          * error correction, to keep the cumulative error low in the running totals systemDebtRedistributionIndex:

876:          * 5) Note: static analysis tools complain about this "division before multiplication", however, it is intended.

```
[L12](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L12), [L36](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L36), [L37](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L37), [L74](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L74), [L133](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L133), [L134](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L134), [L237](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L237), [L311](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L311), [L563](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L563), [L675](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L675), [L869](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L869), [L876](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L876)

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

15: /// @dev All features around Cdp management are split into separate parts to get around contract size limitations.

17: /// @dev Both CdpManager and LiquidationLibrary must maintain **the same storage layout**, so shared storage components

27:     /// @notice Start the recovery mode grace period, if the system is in RM and the grace period timestamp has not already been set

48:     /// @dev Specified TCR is emitted for notification pruposes regardless of whether the Grace Period timestamp is set

60:     /// @notice No input validation, calling function must confirm that the system is not in recovery mode to be valid

61:     /// @dev Specified TCR is emitted for notification pruposes regardless of whether the Grace Period timestamp is set

150:     uint256 public constant MAX_MINUTE_DECAY_FACTOR = 999999999999999999; // Corresponds to a very fast decay rate, but not too extreme

172:     // Snapshot of the value of totalStakes, taken immediately after the latest liquidation and split fee claim

175:     // Snapshot of the total collateral across the ActivePool, immediately after the latest liquidation and split fee claim

182:      * A systemDebt increase  of ( stake * [systemDebtRedistributionIndex - systemDebtRedistributionIndex(0)] )

197:     /* Global Fee accumulator (never decreasing) per stake unit in CDPManager, similar to systemDebtRedistributionIndex */

199:     /* Global Fee accumulator calculation error due to integer division, similar to redistribution calculation */

204:     // Array of all active cdp Ids - used to to compute an approximate hint off-chain, for the sorted list insertion

239:     /// @notice BorrowerOperations and CdpManager share reentrancy status by confirming the other's locked flag before beginning operation

240:     /// @dev This is an alternative to the more heavyweight solution of both being able to set the reentrancy flag on a 3rd contract.

291:      * The stETH as compensation must be excluded as it is always sent out at the very end of the liquidation sequence.

303:     /// @dev get the pending Cdp debt "reward" (i.e. the amount of extra debt assigned to the Cdp) from liquidation redistribution events, earned by their stake

323:      * A Cdp has pending redistributed debt if its snapshot is less than the current rewards per-unit-staked sum:

324:      * this indicates that redistributions have occured since the snapshot was made, and the user therefore has

440:     // Calculate a new stake based on the snapshots of the totalStakes and totalCollateral taken at the last liquidation

460:      * Remove a Cdp owner from the CdpOwners array, not preserving array order. Removing owner 'B' does the following:

549:     /// @return _feeTaken The fee split in collateral token which will be deduced from current total system collateral

550:     /// @return _deltaFeePerUnit The fee split increase per unit, used to added to `systemStEthFeePerUnitIndex`

551:     /// @return _perUnitError The fee split calculation error, used to update `systemStEthFeePerUnitIndexError`

611:     /// @notice Calculate the applied split fee(scaled by 1e18) and the resulting CDP collateral share after applied

613:     /// @param _systemStEthFeePerUnitIndex The fee-per-stake-unit value to be used in fee split calculation, could be result of calcFeeUponStakingReward()

668:     /// @notice Return the Nominal Collateral Ratio (NICR) of the specified Cdp as "cached view" (maybe outdated).

672:     /// @dev Use getSyncedNominalICR() instead if pending fee split and debt redistribution should be considered

683:     /// @return The Nominal Collateral Ratio (NICR) of the specified Cdp with fee split and debt redistribution considered.

697:     /// @notice Return the Individual Collateral Ratio (ICR) of the specified Cdp as "cached view" (maybe outdated).

716:     /// @notice Return the pending extra debt assigned to the Cdp from liquidation redistribution, calcualted by Cdp's stake

726:     /// @return Whether the debt redistribution tracking index of the specified Cdp is less than the global tracking one (meaning it might get pending debt redistribution)

740:     /// @notice Calculate the Cdps entire debt and coll, including pending debt redistributions and collateral reduction from split fee.

781:     /// @dev calculate pending state change to be applied for given CDP and global split index(typically already synced):

```
[L15](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L15), [L17](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L17), [L27](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L27), [L48](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L48), [L60](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L60), [L61](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L61), [L150](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L150), [L172](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L172), [L175](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L175), [L182](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L182), [L197](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L197), [L199](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L199), [L204](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L204), [L239](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L239), [L240](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L240), [L291](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L291), [L303](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L303), [L323](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L323), [L324](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L324), [L440](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L440), [L460](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L460), [L549](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L549), [L550](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L550), [L551](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L551), [L611](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L611), [L613](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L613), [L668](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L668), [L672](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L672), [L683](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L683), [L697](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L697), [L716](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L716), [L726](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L726), [L740](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L740), [L781](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L781)

```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

14: /// @dev While an owner could have multiple different sized Cdps, the remaining surplus colateral from all of its closed Cdp

36:      * @dev One-time initialization function. Can only be called by the owner as a security measure. Ownership is renounced after the function is called.

```
[L14](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L14), [L36](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L36)

```solidity
File: packages/contracts/contracts/EBTCToken.sol

16:  * https://github.com/OpenZeppelin/openzeppelin-contracts/blob/53516bc555a454862470e7860a9b5254db4d00f5/contracts/token/ERC20/ERC20Permit.sol

21:  * 1) Transfer protection: blocklist of addresses that are invalid recipients (i.e. core Ebtc contracts) in external transfer() and transferFrom() calls.

42:     // Cache the domain separator as an immutable value, but also store the chain id that it corresponds to, in order to

244:     // Warning: sanity checks (for sender and recipient) should have been done before calling these internal functions

```
[L16](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L16), [L21](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L21), [L42](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L42), [L244](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L244)

```solidity
File: packages/contracts/contracts/Governor.sol

9: /// @notice We have taken the tradeoff of additional storage usage for easier readabiliy without using off-chain / indexing services.

11: /// @author Modified from Solmate (https://github.com/transmissions11/solmate/blob/main/src/auth/authorities/RolesAuthority.sol)

```
[L9](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L9), [L11](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L11)

```solidity
File: packages/contracts/contracts/PriceFeed.sol

17:  * The PriceFeed uses Chainlink as primary oracle and allows for an optional fallback source. It contains logic for

19:  * Chainlink oracle. In addition, it contains the mechanism to add or remove the fallback oracle through governance.

31:     // Maximum time period allowed since Chainlink's latest round data timestamp, beyond which Chainlink is considered frozen.

96:     /// @dev Uses a main oracle (Chainlink) and a fallback oracle in case Chainlink fails. If both fail, it uses the last good price seen by eBTC.

97:     /// @dev The fallback oracle address can be swapped by the Authority. The fallback oracle must conform to the IFallbackCaller interface.

125:                 // If Chainlink is broken and Fallback is working, switch to Fallback and return current Fallback price

149:             // If Chainlink price has changed by > 50% between two consecutive rounds, compare it to Fallback's price

166:                  * If Fallback is live and both oracles have a similar price, conclude that Chainlink's large price deviation between

167:                  * two consecutive rounds was likely a legitmate market price movement, and so continue using Chainlink

173:                 // If Fallback is live but the oracles differ too much in price, conclude that Chainlink's initial price deviation was

190:             // If both Fallback and Chainlink are live, unbroken, and reporting similar prices, switch back to Chainlink

208:              * If Fallback is only frozen but otherwise returning valid data, just return the last good price.

275:                 // if Chainlink is frozen and Fallback is broken, remember Fallback broke, and return last good price

290:             // if Chainlink is live and Fallback is broken, remember Fallback broke, and return Chainlink price

296:             // If Chainlink is live and Fallback is frozen, just use last good price (no status change) since we have no basis for comparison

308:             // Otherwise if Chainlink is live but price not within 5% of Fallback, distrust Chainlink, and return Fallback price

326:             // If Chainlink and Fallback are both live, unbroken and similar price, switch back to chainlinkWorking and return Chainlink price

338:             // If Chainlink is live but deviated >50% from it's previous price and Fallback is still untrusted, switch

345:             // Otherwise if Chainlink is live and deviated <50% from it's previous price and Fallback is still untrusted,

394:     /// @dev Chainlink is considered broken if its current or previous round data is in any way bad. We check the previous round for two reasons.

396:     /// @dev 2. Chainlink is the PriceFeed's preferred primary oracle - having two consecutive valid round responses adds peace of mind when using or returning to Chainlink.

408:     /// @dev A response is considered bad if the success value reports failure, or if the timestamp is invalid (0 or in the future)

432:     /// @dev The oracle is considered frozen if either of the feed timestamps are older than the threshold specified by the static timeout thresholds

441:     /// @notice Checks if the price change between Chainlink oracle rounds is above the maximum threshold allowed

444:     /// @return A boolean indicating whether the price change from Chainlink oracle is above the maximum threshold allowed

474:         // Check for zero price (FallbackCaller must ensure that the price is not negative and return 0 if it is)

482:     /// @notice Checks if the fallback oracle is frozen by comparing the current timestamp with the timeout value.

497:     /// @notice Checks if both the Chainlink and fallback oracles are live, unbroken, and reporting similar prices.

521:     /// @notice Checks if the prices reported by the Chainlink and fallback oracles are similar, within the maximum deviation specified by MAX_PRICE_DIFFERENCE_BETWEEN_ORACLES.

530:         // Get the relative price difference between the oracles. Use the lower price as the denominator, i.e. the reference for the calculation.

538:          * Return true if the relative price difference is <= MAX_PRICE_DIFFERENCE_BETWEEN_ORACLES: if so, we assume both oracles are probably reporting

539:          * the honest market price, as it is unlikely that both have been broken/hacked and are still in-sync.

579:     /// @notice Retrieves the latest response from the fallback oracle. If the fallback oracle address is set to the zero address, it returns a failing struct.

604:     /// @notice Fetches Chainlink responses for the current round of data for both ETH-BTC and stETH-ETH price feeds.

605:     /// @return chainlinkResponse A struct containing data retrieved from the price feeds, including the round IDs, timestamps, aggregated price, and a success flag.

683:     /// @notice Fetches Chainlink responses for the previous round of data for both ETH-BTC and stETH-ETH price feeds.

686:     /// @return prevChainlinkResponse A struct containing data retrieved from the price feeds, including the round IDs, timestamps, aggregated price, and a success flag.

771:     /// @notice Returns if the CL feed is healthy or not, based on: negative value and null round id. For price aggregation

```
[L17](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L17), [L19](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L19), [L31](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L31), [L96](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L96), [L97](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L97), [L125](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L125), [L149](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L149), [L166](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L166), [L167](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L167), [L173](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L173), [L190](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L190), [L208](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L208), [L275](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L275), [L290](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L290), [L296](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L296), [L308](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L308), [L326](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L326), [L338](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L338), [L345](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L345), [L394](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L394), [L396](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L396), [L408](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L408), [L432](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L432), [L441](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L441), [L444](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L444), [L474](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L474), [L482](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L482), [L497](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L497), [L521](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L521), [L530](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L530), [L538](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L538), [L539](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L539), [L579](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L579), [L604](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L604), [L605](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L605), [L683](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L683), [L686](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L686), [L771](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L771)

```solidity
File: packages/contracts/contracts/SortedCdps.sol

18:  * NICRs are computed dynamically at runtime, and not stored on the Node. This is because NICRs of active Cdps

21:  * The list relies on the fact that liquidation events preserve ordering: a liquidation decreases the NICRs of all active Cdps,

37:  * - Ordering checks for insertion are performed by comparing an NICR argument to the current NICR, calculated at runtime.

40:  * - Public functions with parameters have been made internal to save gas, and given an external wrapper function for external access

100:     /// @dev Inspired https://github.com/balancer-labs/balancer-v2-monorepo/blob/18bd5fb5d87b451cc27fbd30b276d1fb2987b529/pkg/vault/contracts/PoolRegistry.sol

134:     /// @notice Find a specific CDP for a given owner, indexed by it's place in the linked list relative to other Cdps owned by the same address

148:     /// @dev a pagination-flavor search (from least ICR to biggest ICR) for CDP owned by given owner and specified index (starting at given CDP)

171:     /// @return cdpId The CDP Id if found, otherwise return current lastly-visited CDP as the startNode for next pagination

272:         // This roughly halves the amount of Cdps we can process before relying on pagination or off-chain methods

280:     /// @dev a pagination-flavor search retrieval of (from least ICR to biggest ICR) Cdps owned by given owner (starting at given CDP)

283:     /// @return all CdpIds of the specified owner found by search starting at the specified startNodeId for the specified maximum iteration count

292:         // This roughly halves the amount of Cdps we can process before relying on pagination or off-chain methods

309:         // Two-pass strategy, halving the amount of Cdps we can process before relying on pagination or off-chain methods

416:     /// @notice Strong trust assumption that the specified nodes are sorted in the same order as in the input array

606:             // `(_prevId, _nextId)` is a valid insert position if they are adjacent nodes and `_NICR` falls between the two nodes' NICRs

718:     /// @dev Asserts that the caller of the function is either the BorrowerOperations contract or the CdpManager

```
[L18](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L18), [L21](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L21), [L37](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L37), [L40](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L40), [L100](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L100), [L134](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L134), [L148](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L148), [L171](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L171), [L272](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L272), [L280](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L280), [L283](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L283), [L292](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L292), [L309](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L309), [L416](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L416), [L606](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L606), [L718](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L718)

```solidity
File: packages/contracts/contracts/HintHelpers.sol

9: /// @title HintHelpers mainly serves to provide handy information to facilitate offchain integration like redemption bots.

40:     /// @notice Get the redemption hints for the specified amount of eBTC, price and maximum number of iterations.

45:     /// @return partialRedemptionHintNICR The new Nominal Collateral Ratio (NICR) of the CDP after partial redemption.

100:                     // If the partial redemption would leave the CDP with less than the minimum allowed coll, bail out of partial redemption and return only the fully redeemable

105:                         partialRedemptionHintNICR = 0; //reset to 0 as there is no partial redemption in this case

155:     /* getApproxHint() - return address of a Cdp that is, on average, (length / numTrials) positions away in the 

158:     Note: The output address is worst-case O(n) positions away from the correct insert position, however, the function 

161:     Submitting numTrials = k * sqrt(length), with k = 15 makes it very, very likely that the ouput address will 

```
[L9](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L9), [L40](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L40), [L45](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L45), [L100](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L100), [L105](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L105), [L155](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L155), [L158](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L158), [L161](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L161)

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

21: /// - As a Clone / Proxy (Not done, prob you'd read `owner` from calldata when using clones-with-immutable-args)

24: /// @custom:known-issue Due to slippage some dust amounts for all intermediary tokens can be left, since there's no way to ask to sell all available

233:     /// @dev If you delegatecall into this, this will transfer the tokens to the caller of the DiamondLike (and not the contract)

404:         // Approve can be given anywhere because this is a router, and after call we will delete all approvals

413:         // But technically you could approve w/e you want here, this is fine because the contract is a router and will not hold user funds

426:         // val -> 0 -> 0 -> val means this is safe to repeat since even if full approve is unused, we always go back to 0 after

496:     /// @dev excessivelySafeCall to perform generic calls without getting gas bombed | useful if you don't care about return value

497:     /// @notice Credits to: https://github.com/nomad-xyz/ExcessivelySafeCall/blob/main/src/ExcessivelySafeCall.sol

```
[L21](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L21), [L24](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L24), [L233](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L233), [L404](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L404), [L413](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L413), [L426](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L426), [L496](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L496), [L497](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L497)

```solidity
File: packages/contracts/contracts/LeverageMacroDelegateTarget.sol

35:  *  You can perform a delegatecall to `sweepToCaller` after the operation to have the SC Wallet send you back the funds

36:  * @notice If you didn't get it, this is an advanced contract, please simulate the TX with Tenderly before using this

```
[L35](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L35), [L36](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L36)

```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

16:  *  Per solidity, hardcoded functions are switched into, meaning they cannot be overriden (although you could set a callbackHandler that cannot be reached)

22:  *  This ensures that nobody can call this contract unless the owner sets this to `true` via the scary `setAllowAnyCall`

75:     ///     Ensure you use the callback in the same call as you set it, or this may be used to attack this wallet

```
[L16](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L16), [L22](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L22), [L75](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L75)

```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

6: /// @notice Provides a flexible and updatable auth pattern which is completely separate from application logic.

35:         // Checking if the caller is the owner only after calling the authority saves gas in most cases, but be

36:         // aware that this makes protected functions uncallable even to the owner if the authority is out of order.

```
[L6](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L6), [L35](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L35), [L36](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L36)

```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

6: /// @notice Provides a flexible and updatable auth pattern which is completely separate from application logic.

33:         // Checking if the caller is the owner only after calling the authority saves gas in most cases, but be

34:         // aware that this makes protected functions uncallable even to the owner if the authority is out of order.

```
[L6](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L6), [L33](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L33), [L34](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L34)

```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

24:     // Critical system collateral ratio. If the system's total collateral ratio (TCR) falls below the CCR, Recovery Mode is triggered.

65:     /// @notice Entire system collateral = collateral allocated to system in ActivePool, using it's internal accounting

66:     /// @dev Collateral tokens stored in ActivePool for liquidator rewards, fees, or coll in CollSurplusPool, are not included

```
[L24](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L24), [L65](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L65), [L66](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L66)

```solidity
File: packages/contracts/contracts/Dependencies/EbtcMath.sol

12:      * - Making it “too low” could lead to an ICR equal to zero, due to truncation from Solidity floor division.

53:      * If a period of > 1000 years is ever used as an exponent in either of the above functions, the result will be

57:      * In function 2), the difference in tokens issued at 1000 years and any time > 1000 years, will be negligible

```
[L12](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L12), [L53](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L53), [L57](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L57)

```solidity
File: packages/contracts/contracts/Dependencies/ReentrancyGuard.sol

6: /// @author Modified from OpenZeppelin (https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/security/ReentrancyGuard.sol)

```
[L6](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ReentrancyGuard.sol#L6)

```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

10: /// @author Modified from Solmate (https://github.com/transmissions11/solmate/blob/main/src/auth/authorities/RolesAuthority.sol)

61:             - That capability is public, or the user has a role that has been granted the capability to call the function

```
[L10](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L10), [L61](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L61)

```solidity
File: packages/contracts/contracts/Interfaces/ICdpManagerData.sol

234:     function syncGlobalAccountingAndGracePeriod() external; // Accrues StEthFeeSplit and influences Grace Period

```
[L234](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L234)

</details>

&nbsp;
## [N-37] Use bit shifts to improve readability

Replace instances of long bit masks of a single bit with bit shifts.

<details>
<summary>Instances: 1</summary>

```solidity
File: packages/contracts/contracts/SortedCdps.sol

80:     bytes32 public constant dummyId =
81:         0x0000000000000000000000000000000000000000000000000000000000000000;

```
[L80](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L80)

</details>

&nbsp;
## [N-38] Use constants rather than magic numbers

Improves code readability and reduces margin for error.

<details>
<summary>Instances: 6</summary>

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

476:             CCR > MCR (125% vs 110%)

```
[L476](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L476)

```solidity
File: packages/contracts/contracts/PriceFeed.sol

798:             ? 10 ** (_stEthEthDecimals - _ethBtcDecimals)

799:             : 10 ** (_ethBtcDecimals - _stEthEthDecimals);

804:                 EbtcMath.DECIMAL_PRECISION) / 10 ** (_decimalDenominator * 2);

```
[L798](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L798), [L799](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L799), [L804](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L804)

```solidity
File: packages/contracts/contracts/Dependencies/EbtcMath.sol

60:         if (_minutes > 525600000) {

61:             _minutes = 525600000;

```
[L60](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L60), [L61](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L61)

</details>

&nbsp;
## [N-39] Functions prone to reentrancy should use `nonReentrant`

Functions that involve transferring ether, performing a low level call or
transferring ERC20 tokens with ERC777 hooks are prone to reentrancy. Although
it is sufficient to follow the CEI pattern, reentrancy guards such as
[OpenZeppelin's `nonReentrant`](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/security/ReentrancyGuard.sol#L55)
help to provide complete protection.

Moreover, reentrancy guards are more effective at protecting against
[read-only reentrancy](https://medium.com/@zokyo.io/read-only-reentrancy-attacks-understanding-the-threat-to-your-smart-contracts-99444c0a7334#:~:text=The%20read%2Donly%20reentrancy%20is,wrong%20values%20could%20be%20reported.),
where reentrancy vulnerabilities may be exploited to execute malicious actions
without altering contract state.

<details>
<summary>Instances: 7</summary>

```solidity
File: packages/contracts/contracts/ActivePool.sol

261:     function flashLoan(
262:         IERC3156FlashBorrower receiver,
263:         address token,
264:         uint256 amount,
265:         bytes calldata data
266:     ) external override returns (bool) {

274:         collateral.transfer(address(receiver), amount);

283:         collateral.transferFrom(address(receiver), address(this), amountWithFee);

286:         collateral.transfer(feeRecipientAddress, fee);

```
[L261](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L261), [L274](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L274), [L283](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L283), [L286](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L286)

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

1077:     function flashLoan(
1078:         IERC3156FlashBorrower receiver,
1079:         address token,
1080:         uint256 amount,
1081:         bytes calldata data
1082:     ) external override returns (bool) {

1100:         ebtcToken.transferFrom(address(receiver), feeRecipientAddress, fee + amount);

```
[L1077](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1077), [L1100](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1100)

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

118:     function doOperation(
119:         FlashLoanType flType,
120:         uint256 borrowAmount,
121:         LeverageMacroOperation calldata operation,
122:         PostOperationCheck postCheckType,
123:         PostCheckParams calldata checkParams
124:     ) external {

129:             IERC20(operation.tokenToTransferIn).safeTransferFrom(
130:                 msg.sender,
131:                 address(this),
132:                 operation.amountToTransferIn
133:             );

214:     function sweepToCaller() public {

224:             ebtcToken.transfer(msg.sender, ebtcBal);

234:     function sweepToken(address token, uint256 amount) public {

237:         IERC20(token).safeTransfer(msg.sender, amount);

```
[L118](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L118), [L129](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L129), [L214](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L214), [L224](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L224), [L234](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L234), [L237](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L237)

</details>

&nbsp;
## [N-40] Import specific identifiers rather than the whole file

Prefer import declarations that specify the symbol(s) using the form `import {SYMBOL} from "SomeContract.sol"` rather than importing the whole file.

This improves readability, makes flattened files smaller, and speeds up compilation.

<details>
<summary>Instances: 96</summary>

```solidity
File: packages/contracts/contracts/ActivePool.sol

5: import "./Interfaces/IActivePool.sol";

6: import "./Interfaces/ICollSurplusPool.sol";

7: import "./Dependencies/ICollateralToken.sol";

8: import "./Interfaces/ICdpManagerData.sol";

9: import "./Dependencies/ERC3156FlashLender.sol";

10: import "./Dependencies/SafeERC20.sol";

11: import "./Dependencies/ReentrancyGuard.sol";

12: import "./Dependencies/AuthNoOwner.sol";

13: import "./Dependencies/BaseMath.sol";

```
[L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L5), [L6](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L6), [L7](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L7), [L8](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L8), [L9](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L9), [L10](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L10), [L11](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L11), [L12](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L12), [L13](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L13)

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

5: import "./Interfaces/IBorrowerOperations.sol";

6: import "./Interfaces/ICdpManager.sol";

7: import "./Interfaces/ICdpManagerData.sol";

8: import "./Interfaces/IEBTCToken.sol";

9: import "./Interfaces/ICollSurplusPool.sol";

10: import "./Interfaces/ISortedCdps.sol";

11: import "./Dependencies/EbtcBase.sol";

12: import "./Dependencies/ReentrancyGuard.sol";

13: import "./Dependencies/Ownable.sol";

14: import "./Dependencies/AuthNoOwner.sol";

15: import "./Dependencies/ERC3156FlashLender.sol";

16: import "./Dependencies/PermitNonce.sol";

```
[L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L5), [L6](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L6), [L7](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L7), [L8](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L8), [L9](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L9), [L10](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L10), [L11](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L11), [L12](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L12), [L13](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L13), [L14](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L14), [L15](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L15), [L16](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L16)

```solidity
File: packages/contracts/contracts/CdpManager.sol

5: import "./Interfaces/ICdpManager.sol";

6: import "./Interfaces/ICollSurplusPool.sol";

7: import "./Interfaces/IEBTCToken.sol";

8: import "./Interfaces/ISortedCdps.sol";

9: import "./Dependencies/ICollateralTokenOracle.sol";

10: import "./CdpManagerStorage.sol";

11: import "./Dependencies/Proxy.sol";

```
[L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L5), [L6](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L6), [L7](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L7), [L8](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L8), [L9](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L9), [L10](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L10), [L11](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L11)

```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

4: import "./Interfaces/ICdpManagerData.sol";

5: import "./Interfaces/ICollSurplusPool.sol";

6: import "./Interfaces/IEBTCToken.sol";

7: import "./Interfaces/ISortedCdps.sol";

8: import "./Dependencies/ICollateralTokenOracle.sol";

9: import "./CdpManagerStorage.sol";

```
[L4](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L4), [L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L5), [L6](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L6), [L7](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L7), [L8](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L8), [L9](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L9)

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

5: import "./Interfaces/ICdpManager.sol";

6: import "./Interfaces/ICollSurplusPool.sol";

7: import "./Interfaces/IEBTCToken.sol";

8: import "./Interfaces/ISortedCdps.sol";

9: import "./Dependencies/EbtcBase.sol";

10: import "./Dependencies/ReentrancyGuard.sol";

11: import "./Dependencies/ICollateralTokenOracle.sol";

12: import "./Dependencies/AuthNoOwner.sol";

```
[L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L5), [L6](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L6), [L7](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L7), [L8](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L8), [L9](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L9), [L10](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L10), [L11](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L11), [L12](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L12)

```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

5: import "./Interfaces/ICollSurplusPool.sol";

6: import "./Dependencies/ICollateralToken.sol";

7: import "./Dependencies/SafeERC20.sol";

8: import "./Dependencies/ReentrancyGuard.sol";

9: import "./Dependencies/AuthNoOwner.sol";

10: import "./Interfaces/IActivePool.sol";

```
[L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L5), [L6](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L6), [L7](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L7), [L8](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L8), [L9](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L9), [L10](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L10)

```solidity
File: packages/contracts/contracts/EBTCToken.sol

5: import "./Interfaces/IEBTCToken.sol";

7: import "./Dependencies/AuthNoOwner.sol";

8: import "./Dependencies/PermitNonce.sol";

```
[L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L5), [L7](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L7), [L8](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L8)

```solidity
File: packages/contracts/contracts/PriceFeed.sol

5: import "./Interfaces/IPriceFeed.sol";

6: import "./Interfaces/IFallbackCaller.sol";

7: import "./Dependencies/AggregatorV3Interface.sol";

8: import "./Dependencies/BaseMath.sol";

9: import "./Dependencies/EbtcMath.sol";

10: import "./Dependencies/AuthNoOwner.sol";

```
[L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L5), [L6](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L6), [L7](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L7), [L8](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L8), [L9](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L9), [L10](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L10)

```solidity
File: packages/contracts/contracts/SortedCdps.sol

5: import "./Interfaces/ISortedCdps.sol";

6: import "./Interfaces/ICdpManager.sol";

7: import "./Interfaces/IBorrowerOperations.sol";

```
[L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L5), [L6](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L6), [L7](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L7)

```solidity
File: packages/contracts/contracts/HintHelpers.sol

5: import "./Interfaces/ICdpManager.sol";

6: import "./Interfaces/ISortedCdps.sol";

7: import "./Dependencies/EbtcBase.sol";

```
[L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L5), [L6](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L6), [L7](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L7)

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

4: import "./Interfaces/IBorrowerOperations.sol";

5: import "./Interfaces/IERC3156FlashLender.sol";

6: import "./Interfaces/IEBTCToken.sol";

7: import "./Interfaces/ICdpManager.sol";

8: import "./Interfaces/ISortedCdps.sol";

9: import "./Interfaces/IPriceFeed.sol";

10: import "./Dependencies/ICollateralToken.sol";

12: import "./Dependencies/SafeERC20.sol";

```
[L4](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L4), [L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L5), [L6](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L6), [L7](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L7), [L8](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L8), [L9](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L9), [L10](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L10), [L12](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L12)

```solidity
File: packages/contracts/contracts/LeverageMacroFactory.sol

5: import "./Dependencies/ICollateralToken.sol";

6: import "./Interfaces/IEBTCToken.sol";

```
[L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L5), [L6](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L6)

```solidity
File: packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol

5: import "../Interfaces/IERC3156FlashLender.sol";

6: import "../Interfaces/IWETH.sol";

```
[L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L5), [L6](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L6)

```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

5: import "./BaseMath.sol";

6: import "./EbtcMath.sol";

7: import "../Interfaces/IActivePool.sol";

8: import "../Interfaces/IPriceFeed.sol";

9: import "../Interfaces/IEbtcBase.sol";

10: import "../Dependencies/ICollateralToken.sol";

```
[L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L5), [L6](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L6), [L7](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L7), [L8](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L8), [L9](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L9), [L10](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L10)

```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

6: import "./EnumerableSet.sol";

```
[L6](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L6)

```solidity
File: packages/contracts/contracts/Interfaces/IActivePool.sol

5: import "./IPool.sol";

```
[L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IActivePool.sol#L5)

```solidity
File: packages/contracts/contracts/Interfaces/IBorrowerOperations.sol

4: import "./IPositionManagers.sol";

```
[L4](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L4)

```solidity
File: packages/contracts/contracts/Interfaces/ICdpManager.sol

5: import "./IEbtcBase.sol";

6: import "./ICdpManagerData.sol";

```
[L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol#L5), [L6](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol#L6)

```solidity
File: packages/contracts/contracts/Interfaces/ICdpManagerData.sol

5: import "./ICollSurplusPool.sol";

6: import "./IEBTCToken.sol";

7: import "./ISortedCdps.sol";

8: import "./IActivePool.sol";

9: import "./IRecoveryModeGracePeriod.sol";

10: import "../Dependencies/ICollateralTokenOracle.sol";

```
[L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L5), [L6](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L6), [L7](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L7), [L8](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L8), [L9](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L9), [L10](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L10)

```solidity
File: packages/contracts/contracts/Interfaces/IEbtcBase.sol

5: import "./IPriceFeed.sol";

```
[L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IEbtcBase.sol#L5)

```solidity
File: packages/contracts/contracts/Interfaces/IEBTCToken.sol

5: import "../Dependencies/IERC20.sol";

6: import "../Dependencies/IERC2612.sol";

```
[L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IEBTCToken.sol#L5), [L6](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IEBTCToken.sol#L6)

```solidity
File: packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol

5: import "./IERC3156FlashBorrower.sol";

```
[L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol#L5)

</details>

&nbsp;
## [N-41] Multiple address/ID mappings can be combined into a single mapping of an address/ID to a struct, for readability

<details>
<summary>Instances: 9</summary>

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

168:     mapping(bytes32 => Cdp) public Cdps;

190:     mapping(bytes32 => uint256) public cdpDebtRedistributionIndex;

202:     mapping(bytes32 => uint256) public cdpStEthFeePerUnitIndex;

```
[L168](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L168), [L190](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L190), [L202](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L202)

```solidity
File: packages/contracts/contracts/EBTCToken.sol

51:     mapping(address => uint256) private _balances;

52:     mapping(address => mapping(address => uint256)) private _allowances;

```
[L51](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L51), [L52](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L52)

```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

28:     mapping(address => EnumerableSet.Bytes32Set) internal enabledFunctionSigsByTarget;

32:     mapping(address => bytes32) public getUserRoles;

34:     mapping(address => mapping(bytes4 => CapabilityFlag)) public capabilityFlag;

36:     mapping(address => mapping(bytes4 => bytes32)) public getRolesWithCapability;

```
[L28](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L28), [L32](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L32), [L34](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L34), [L36](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L36)

</details>

&nbsp;
## [N-42] Use named function calls

When calling a function, use named parameters to improve readability and reduce
the chance of making mistakes. For example:
`_mint({account: msg.sender, amount: _amount})`

<details>
<summary>Instances: 104</summary>

```solidity
File: packages/contracts/contracts/ActivePool.sol

183:         collateral.transferShares(_account, _shares);

272:         uint256 oldRate = collateral.getPooledEthByShares(DECIMAL_PRECISION);

286:         collateral.transfer(feeRecipientAddress, fee);

294:         require(
295:             collateral.balanceOf(address(this)) >= collateral.getPooledEthByShares(systemCollShares),
296:             "ActivePool: Must repay Balance"
297:         );

302:         require(
303:             collateral.getPooledEthByShares(DECIMAL_PRECISION) == oldRate,
304:             "ActivePool: Should keep same collateral share rate"
305:         );

362:         collateral.transferShares(feeRecipientAddress, _shares);

```
[L183](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L183), [L272](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L272), [L286](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L286), [L294](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L294), [L302](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L302), [L362](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L362)

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

338:         address _borrower = sortedCdps.getOwnerAddress(_cdpId);

343:         cdpManager.syncAccounting(_cdpId);

363:         vars.debt = cdpManager.getCdpDebt(_cdpId);
364:         vars.collShares = cdpManager.getCdpCollShares(_cdpId);

422:             sortedCdps.reInsert(_cdpId, newNICR, _upperHint, _lowerHint);

466:         uint256 _liquidatorRewardShares = collateral.getSharesByPooledEth(LIQUIDATOR_REWARD);

497:                 cdpManager.notifyStartGracePeriod(newTCR);

500:                 cdpManager.notifyEndGracePeriod(newTCR);

509:             cdpManager.notifyEndGracePeriod(newTCR);

554:         address _borrower = sortedCdps.getOwnerAddress(_cdpId);

559:         cdpManager.syncAccounting(_cdpId);

564:         uint256 collShares = cdpManager.getCdpCollShares(_cdpId);
565:         uint256 debt = cdpManager.getCdpDebt(_cdpId);
566:         uint256 liquidatorRewardShares = cdpManager.getCdpLiquidatorRewardShares(_cdpId);

570:         uint256 newTCR = _getNewTCRFromCdpChange(
571:             collateral.getPooledEthByShares(collShares),
572:             false,
573:             debt,
574:             false,
575:             price
576:         );

581:         cdpManager.notifyEndGracePeriod(newTCR);

583:         cdpManager.closeCdp(_cdpId, _borrower, debt, collShares);

749:             collSharesChange = collateral.getSharesByPooledEth(_collReceived);

752:             collSharesChange = collateral.getSharesByPooledEth(_requestedCollWithdrawal);

786:         activePool.increaseSystemCollShares(_sharesToTrack);

791:         activePool.increaseSystemDebt(_debt);
792:         ebtcToken.mint(_account, _debt);

797:         activePool.decreaseSystemDebt(_debt);
798:         ebtcToken.burn(_account, _debt);

825:         uint256 status = _cdpManager.getCdpStatus(_cdpId);

830:         uint status = cdpManager.getCdpStatus(_cdpId);

957:         require(
958:             ebtcToken.balanceOf(_account) >= _debtRepayment,
959:             "BorrowerOperations: Caller doesnt have enough eBTC to make repayment"
960:         );

999:         uint256 newNICR = EbtcMath._computeNominalCR(newCollShares, newDebt);

1022:         uint256 newICR = EbtcMath._computeCR(
1023:             collateral.getPooledEthByShares(newCollShares),
1024:             newDebt,
1025:             _price
1026:         );

1057:         uint256 systemStEthBalance = collateral.getPooledEthByShares(_systemCollShares);

1065:         uint256 newTCR = EbtcMath._computeCR(systemStEthBalance, systemDebt, _price);

1103:         ebtcToken.burn(feeRecipientAddress, amount);

```
[L338](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L338), [L343](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L343), [L363](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L363), [L422](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L422), [L466](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L466), [L497](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L497), [L500](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L500), [L509](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L509), [L554](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L554), [L559](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L559), [L564](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L564), [L570](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L570), [L581](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L581), [L583](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L583), [L749](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L749), [L752](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L752), [L786](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L786), [L791](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L791), [L797](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L797), [L825](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L825), [L830](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L830), [L957](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L957), [L999](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L999), [L1022](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1022), [L1057](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1057), [L1065](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1065), [L1103](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1103)

```solidity
File: packages/contracts/contracts/CdpManager.sol

193:             uint256 newNICR = EbtcMath._computeNominalCR(newColl, newDebt);

201:             if (
202:                 newNICR != _redeemColFromCdp.partialRedemptionHintNICR ||
203:                 collateral.getPooledEthByShares(newColl) < MIN_NET_STETH_BALANCE
204:             ) {

254:         activePool.decreaseSystemDebt(_EBTC);

276:         if (
277:             _firstRedemptionHint == sortedCdps.nonExistId() ||
278:             !sortedCdps.contains(_firstRedemptionHint) ||
279:             getSyncedICR(_firstRedemptionHint, _price) < MCR
280:         ) {

284:         bytes32 nextCdp = sortedCdps.getNext(_firstRedemptionHint);

364:             currentBorrower = sortedCdps.getOwnerAddress(_firstRedemptionHint);

367:             currentBorrower = sortedCdps.getOwnerAddress(_cId);

370:                 _cId = sortedCdps.getPrev(_cId);
371:                 currentBorrower = sortedCdps.getOwnerAddress(_cId);

424:                 bytes32 _nextId = sortedCdps.getPrev(_cId);
425:                 address nextUserToCheck = sortedCdps.getOwnerAddress(_nextId);

435:             sortedCdps.remove(_firstRedeemed);

442:             sortedCdps.batchRemove(_toRemoveIds);

500:             _id = sortedCdps.getNext(_id);

556:         CdpIds.push(_cdpId);

621:         uint256 redeemedEBTCFraction = (collateral.getPooledEthByShares(_ETHDrawn) * _price) /
622:             _totalEBTCSupply;

625:         newBaseRate = EbtcMath._min(newBaseRate, DECIMAL_PRECISION); // cap baseRate at a maximum of 100%

704:         uint256 decayFactor = EbtcMath._decPow(minuteDecayFactor, minutesPassed);

742:         uint256 callerBalance = ebtcToken.balanceOf(_redeemer);

```
[L193](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L193), [L201](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L201), [L254](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L254), [L276](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L276), [L284](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L284), [L364](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L364), [L367](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L367), [L370](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L370), [L424](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L424), [L435](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L435), [L442](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L442), [L500](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L500), [L556](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L556), [L621](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L621), [L625](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L625), [L704](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L704), [L742](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L742)

```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

337:                 collSurplusPool.increaseSurplusCollShares(_borrower, _collSurplus);

422:         _requirePartialLiqCollSize(collateral.getPooledEthByShares(newColl));

429:             _reInsertPartialLiquidation(
430:                 _partialState,
431:                 EbtcMath._computeNominalCR(newColl, newDebt),
432:                 _debtAndColl.debt,
433:                 _debtAndColl.collShares
434:             );

436:             uint _cappedColl = collateral.getPooledEthByShares(_partialColl);
437:             emit CdpPartiallyLiquidated(
438:                 _cdpId,
439:                 sortedCdps.getOwnerAddress(_cdpId),
440:                 _partialDebt,
441:                 _partialColl,
442:                 CdpOperation.partiallyLiquidate,
443:                 msg.sender,
444:                 _cappedColl > _debtToColl ? (_cappedColl - _debtToColl) : 0
445:             );

490:         emit CdpUpdated(
491:             _cdpId,
492:             sortedCdps.getOwnerAddress(_cdpId),
493:             msg.sender,
494:             _oldDebt,
495:             _oldColl,
496:             Cdps[_cdpId].debt,
497:             Cdps[_cdpId].coll,
498:             Cdps[_cdpId].stake,
499:             CdpOperation.partiallyLiquidate
500:         );

533:         activePool.decreaseSystemDebt(totalDebtToBurn);

561:         toLiquidator = collateral.getSharesByPooledEth(_incentiveColl);

582:             toLiquidator = collateral.getSharesByPooledEth(_incentiveColl);

585:             _incentiveColl = collateral.getPooledEthByShares(_totalColToSend);

```
[L337](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L337), [L422](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L422), [L429](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L429), [L436](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L436), [L490](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L490), [L533](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L533), [L561](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L561), [L582](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L582), [L585](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L585)

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

93:         uint256 newTCR = EbtcMath._computeCR(
94:             collateral.getPooledEthByShares(systemCollShares),
95:             systemDebt,
96:             price
97:         );

257:         sortedCdps.remove(_cdpId);

494:         uint256 _totalColl = collateral.getPooledEthByShares(_systemCollShares);
495:         return EbtcMath._computeCR(_totalColl, _systemDebt, _price);

535:         return (stEthIndex, collateral.getPooledEthByShares(DECIMAL_PRECISION));

564:         uint256 _feeTaken = collateral.getSharesByPooledEth(_deltaFeeSplit) / DECIMAL_PRECISION;

585:         activePool.allocateSystemCollSharesToFeeRecipient(_feeTaken);

676:         uint256 NICR = EbtcMath._computeNominalCR(currentCollShares, currentEBTCDebt);

693:         uint256 NICR = EbtcMath._computeNominalCR(_newColl, _newDebt);

712:         uint256 _underlyingCollateral = collateral.getPooledEthByShares(currentCollShare);
713:         return EbtcMath._computeCR(_underlyingCollateral, currentDebt, _price);

```
[L93](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L93), [L257](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L257), [L494](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L494), [L535](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L535), [L564](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L564), [L585](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L585), [L676](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L676), [L693](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L693), [L712](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L712)

```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

107:         collateral.transferShares(_account, claimableColl);

```
[L107](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L107)

```solidity
File: packages/contracts/contracts/Governor.sol

47:             address user = users.at(i);

```
[L47](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L47)

```solidity
File: packages/contracts/contracts/SortedCdps.sol

352:         require(cdpManager.getCdpStatus(_id) == 0, "SortedCdps: new id is NOT nonExistent!");

601:             return data.head == _nextId && _NICR >= cdpManager.getCachedNominalICR(_nextId);

604:             return data.tail == _prevId && _NICR <= cdpManager.getCachedNominalICR(_prevId);

607:             return
608:                 data.nodes[_prevId].nextId == _nextId &&
609:                 cdpManager.getCachedNominalICR(_prevId) >= _NICR &&
610:                 _NICR >= cdpManager.getCachedNominalICR(_nextId);

621:         if (data.head == _startId && _NICR >= cdpManager.getCachedNominalICR(_startId)) {

644:         if (data.tail == _startId && _NICR <= cdpManager.getCachedNominalICR(_startId)) {

683:             if (!contains(prevId) || _NICR > cdpManager.getCachedNominalICR(prevId)) {

690:             if (!contains(nextId) || _NICR < cdpManager.getCachedNominalICR(nextId)) {

```
[L352](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L352), [L601](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L601), [L604](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L604), [L607](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L607), [L621](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L621), [L644](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L644), [L683](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L683), [L690](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L690)

```solidity
File: packages/contracts/contracts/HintHelpers.sol

101:                     if (
102:                         collateral.getPooledEthByShares(partialRedemptionNewColl) <
103:                         MIN_NET_STETH_BALANCE
104:                     ) {

176:         diff = EbtcMath._getAbsoluteDifference(_CR, cdpManager.getSyncedNominalICR(hint));

185:             bytes32 _cId = cdpManager.getIdFromCdpIdsArray(arrayIndex);
186:             uint256 currentNICR = cdpManager.getSyncedNominalICR(_cId);

189:             uint256 currentDiff = EbtcMath._getAbsoluteDifference(currentNICR, _CR);

204:         return EbtcMath._computeNominalCR(_coll, _debt);

217:         return EbtcMath._computeCR(_coll, _debt, _price);

```
[L101](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L101), [L176](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L176), [L185](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L185), [L189](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L189), [L204](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L204), [L217](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L217)

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

176:             ICdpManagerData.Cdp memory cdpInfo = cdpManager.Cdps(cdpId);

```
[L176](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L176)

```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

89:         uint256 _systemStEthBalance = collateral.getPooledEthByShares(systemCollShares);
90:         TCR = EbtcMath._computeCR(_systemStEthBalance, systemDebt, _price);

```
[L89](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L89)

```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

116:             if (!targets.contains(target)) {
117:                 targets.add(target);

125:                 targets.remove(target);

151:             if (!users.contains(user)) {
152:                 users.add(user);

159:                 users.remove(user);

```
[L116](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L116), [L125](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L125), [L151](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L151), [L159](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L159)

</details>

&nbsp;
## [N-43] Use named parameters for mappings

Consider using named parameters in mappings (e.g. `mapping(address account => uint256 balance)`) to improve readability. This feature is present since Solidity 0.8.18.

<details>
<summary>Instances: 14</summary>

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

65:     mapping(address => mapping(address => PositionManagerApproval)) public positionManagers;

```
[L65](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L65)

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

168:     mapping(bytes32 => Cdp) public Cdps;

190:     mapping(bytes32 => uint256) public cdpDebtRedistributionIndex;

202:     mapping(bytes32 => uint256) public cdpStEthFeePerUnitIndex;

```
[L168](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L168), [L190](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L190), [L202](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L202)

```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

30:     mapping(address => uint256) internal balances;

```
[L30](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L30)

```solidity
File: packages/contracts/contracts/EBTCToken.sol

51:     mapping(address => uint256) private _balances;

52:     mapping(address => mapping(address => uint256)) private _allowances;

```
[L51](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L51), [L52](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L52)

```solidity
File: packages/contracts/contracts/Governor.sol

30:     mapping(uint8 => string) internal roleNames;

```
[L30](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L30)

```solidity
File: packages/contracts/contracts/SortedCdps.sol

74:         mapping(bytes32 => Node) nodes; // Track the corresponding ids for each node in the list

```
[L74](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L74)

```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

34:         mapping(bytes4 => address) callbackHandler;

```
[L34](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L34)

```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

28:     mapping(address => EnumerableSet.Bytes32Set) internal enabledFunctionSigsByTarget;

32:     mapping(address => bytes32) public getUserRoles;

34:     mapping(address => mapping(bytes4 => CapabilityFlag)) public capabilityFlag;

36:     mapping(address => mapping(bytes4 => bytes32)) public getRolesWithCapability;

```
[L28](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L28), [L32](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L32), [L34](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L34), [L36](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L36)

</details>

&nbsp;
## [N-44] NatSpec `@notice` missing from contract

The `@notice` tag is used to explain the purpose of the contract/interface/library.

<details>
<summary>Instances: 14</summary>

```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

11: /// @title LiquidationLibrary mainly provide necessary logic to fulfill liquidation for eBTC Cdps.
12: /// @dev This contract shares same base and storage layout with CdpManager and is the delegatecall destination from CdpManager
13: contract LiquidationLibrary is CdpManagerStorage {

```
[L11](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L11)

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

14: /// @title CDP Manager storage and shared functions with LiquidationLibrary
15: /// @dev All features around Cdp management are split into separate parts to get around contract size limitations.
16: /// @dev Liquidation related functions are delegated to LiquidationLibrary contract code.
17: /// @dev Both CdpManager and LiquidationLibrary must maintain **the same storage layout**, so shared storage components
18: /// @dev and shared functions are added here in CdpManagerStorage to de-dup code
19: contract CdpManagerStorage is EbtcBase, ReentrancyGuard, ICdpManagerData, AuthNoOwner {

```
[L14](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L14)

```solidity
File: packages/contracts/contracts/EBTCToken.sol

10: /*
11:  *
12:  * Based upon OpenZeppelin's ERC20 contract:
13:  * https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/token/ERC20/ERC20.sol
14:  *
15:  * and their EIP2612 (ERC20Permit / ERC712) functionality:
16:  * https://github.com/OpenZeppelin/openzeppelin-contracts/blob/53516bc555a454862470e7860a9b5254db4d00f5/contracts/token/ERC20/ERC20Permit.sol
17:  *
18:  *
19:  * --- Functionality added specific to the EBTCToken ---
20:  *
21:  * 1) Transfer protection: blocklist of addresses that are invalid recipients (i.e. core Ebtc contracts) in external transfer() and transferFrom() calls.
22:  * The purpose is to protect users from losing tokens by mistakenly sending EBTC directly to a Liquity.
23:  * core contract, when they should rather call the right function.
24:  */

26: contract EBTCToken is IEBTCToken, AuthNoOwner, PermitNonce {

```
[L10](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L10), [L26](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L26)

```solidity
File: packages/contracts/contracts/PriceFeed.sol

12: /*
13:  * PriceFeed for mainnet deployment, it connects to two Chainlink's live feeds, ETH:BTC and
14:  * stETH:ETH, which are used to aggregate the price feed of stETH:BTC in conjuction.
15:  * It also allows for a fallback oracle to intervene in case that the primary Chainlink oracle fails.
16:  *
17:  * The PriceFeed uses Chainlink as primary oracle and allows for an optional fallback source. It contains logic for
18:  * switching oracles based on oracle failures, timeouts, and conditions for returning to the primary
19:  * Chainlink oracle. In addition, it contains the mechanism to add or remove the fallback oracle through governance.
20:  */
21: contract PriceFeed is BaseMath, IPriceFeed, AuthNoOwner {

```
[L12](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L12)

```solidity
File: packages/contracts/contracts/SortedCdps.sol

9: /*
10:  * A sorted doubly linked list with nodes sorted in descending order.
11:  *
12:  * Nodes map to active Cdps in the system by Id.
13:  * Nodes are ordered according to their current nominal individual collateral ratio (NICR),
14:  * which is like the ICR but without the price, i.e., just collateral / debt.
15:  *
16:  * The list optionally accepts insert position hints.
17:  *
18:  * NICRs are computed dynamically at runtime, and not stored on the Node. This is because NICRs of active Cdps
19:  * change dynamically as liquidation events occur.
20:  *
21:  * The list relies on the fact that liquidation events preserve ordering: a liquidation decreases the NICRs of all active Cdps,
22:  * but maintains their order. A node inserted based on current NICR will maintain the correct position,
23:  * relative to it's peers, as rewards accumulate, as long as it's raw collateral and debt have not changed.
24:  * Thus, Nodes remain sorted by current NICR.
25:  *
26:  * Nodes need only be re-inserted upon a CDP operation - when the owner adds or removes collateral or debt
27:  * to their position.
28:  *
29:  * The list is a modification of the following audited SortedDoublyLinkedList:
30:  * https://github.com/livepeer/protocol/blob/master/contracts/libraries/SortedDoublyLL.sol
31:  *
32:  *
33:  * Changes made in the Liquity implementation:
34:  *
35:  * - Keys have been removed from nodes
36:  *
37:  * - Ordering checks for insertion are performed by comparing an NICR argument to the current NICR, calculated at runtime.
38:  *   The list relies on the property that ordering by ICR is maintained as the stETH:BTC price varies.
39:  *
40:  * - Public functions with parameters have been made internal to save gas, and given an external wrapper function for external access
41:  *
42:  *
43:  * Changes made in the Ebtc implementation:
44:  *
45:  * - Positions are now indexed by Ids, not addresses. Functions to generate Ids are provided.
46:  *
47:  * - Added batchRemove functions to optimize redemptions.
48:  *
49:  * - Added more O(n) getter functions and pagination-flavor variants, intended for off-chain use.
50:  */
51: contract SortedCdps is ISortedCdps {

```
[L9](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L9)

```solidity
File: packages/contracts/contracts/HintHelpers.sol

9: /// @title HintHelpers mainly serves to provide handy information to facilitate offchain integration like redemption bots.
10: /// @dev It is strongly recommended to use HintHelper for redemption purpose
11: contract HintHelpers is EbtcBase {

```
[L9](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L9)

```solidity
File: packages/contracts/contracts/LeverageMacroFactory.sol

8: /**
9:  * @title Factory for deploying LeverageMacros
10:  */
11: contract LeverageMacroFactory {

```
[L8](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L8)

```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

12: /*
13:  * Base contract for CdpManager, BorrowerOperations. Contains global system constants and
14:  * common functions.
15:  */
16: contract EbtcBase is BaseMath, IEbtcBase {

```
[L12](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L12)

```solidity
File: packages/contracts/contracts/Interfaces/IBorrowerOperations.sol

6: // Common interface for the Cdp Manager.
7: interface IBorrowerOperations is IPositionManagers {

```
[L6](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L6)

```solidity
File: packages/contracts/contracts/Interfaces/ICdpManager.sol

8: // Common interface for the Cdp Manager.
9: interface ICdpManager is IEbtcBase, ICdpManagerData {

```
[L8](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol#L8)

```solidity
File: packages/contracts/contracts/Interfaces/ICdpManagerData.sol

12: // Common interface for the Cdp Manager.
13: interface ICdpManagerData is IRecoveryModeGracePeriod {

```
[L12](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L12)

```solidity
File: packages/contracts/contracts/Interfaces/IPool.sol

5: // Common interface for the Pools.
6: interface IPool {

```
[L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPool.sol#L5)

```solidity
File: packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol

4: // Interface for State Updates that can trigger RM Liquidations
5: interface IRecoveryModeGracePeriod {

```
[L4](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol#L4)

```solidity
File: packages/contracts/contracts/Interfaces/ISortedCdps.sol

5: // Common interface for the SortedCdps Doubly Linked List.
6: interface ISortedCdps {

```
[L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L5)

</details>

&nbsp;
## [N-45] Event declarations missing NatSpec

<details>
<summary>Instances: 47</summary>

```solidity
File: packages/contracts/contracts/Governor.sol

32:     event RoleNameSet(uint8 indexed role, string indexed name);

```
[L32](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L32)

```solidity
File: packages/contracts/contracts/LeverageMacroFactory.sol

19:     event DeployNewMacro(address indexed sender, address indexed newContractAddress);

```
[L19](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L19)

```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

10:     event OwnershipTransferred(address indexed user, address indexed newOwner);

12:     event AuthorityUpdated(address indexed user, Authority indexed newAuthority);

```
[L10](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L10), [L12](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L12)

```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

11:     event AuthorityUpdated(address indexed user, Authority indexed newAuthority);

```
[L11](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L11)

```solidity
File: packages/contracts/contracts/Interfaces/IActivePool.sol

10:     event SystemCollSharesUpdated(uint256 _coll);
11:     event FeeRecipientAddressChanged(address indexed _feeRecipientAddress);
12:     event FeeRecipientClaimableCollSharesIncreased(uint256 _coll, uint256 _fee);
13:     event FeeRecipientClaimableCollSharesDecreased(uint256 _coll, uint256 _fee);
14:     event FlashLoanSuccess(
15:         address indexed _receiver,
16:         address indexed _token,
17:         uint256 _amount,
18:         uint256 _fee
19:     );
20:     event SweepTokenSuccess(address indexed _token, uint256 _amount, address indexed _recipient);

```
[L10](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IActivePool.sol#L10)

```solidity
File: packages/contracts/contracts/Interfaces/IBorrowerOperations.sol

11:     event FlashLoanSuccess(
12:         address indexed _receiver,
13:         address indexed _token,
14:         uint256 _amount,
15:         uint256 _fee
16:     );

```
[L11](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L11)

```solidity
File: packages/contracts/contracts/Interfaces/ICdpManagerData.sol

17:     event StakingRewardSplitSet(uint256 _stakingRewardSplit);
18:     event RedemptionFeeFloorSet(uint256 _redemptionFeeFloor);
19:     event MinuteDecayFactorSet(uint256 _minuteDecayFactor);
20:     event BetaSet(uint256 _beta);
21:     event RedemptionsPaused(bool _paused);

23:     event Liquidation(uint256 _liquidatedDebt, uint256 _liquidatedColl, uint256 _liqReward);
24:     event Redemption(
25:         uint256 _debtToRedeemExpected,
26:         uint256 _debtToRedeemActual,
27:         uint256 _collSharesSent,
28:         uint256 _feeCollShares,
29:         address indexed _redeemer
30:     );
31:     event CdpUpdated(
32:         bytes32 indexed _cdpId,
33:         address indexed _borrower,
34:         address indexed _executor,
35:         uint256 _oldDebt,
36:         uint256 _oldCollShares,
37:         uint256 _debt,
38:         uint256 _collShares,
39:         uint256 _stake,
40:         CdpOperation _operation
41:     );
42:     event CdpLiquidated(
43:         bytes32 indexed _cdpId,
44:         address indexed _borrower,
45:         uint _debt,
46:         uint _collShares,
47:         CdpOperation _operation,
48:         address indexed _liquidator,
49:         uint _premiumToLiquidator
50:     );
51:     event CdpPartiallyLiquidated(
52:         bytes32 indexed _cdpId,
53:         address indexed _borrower,
54:         uint256 _debt,
55:         uint256 _collShares,
56:         CdpOperation operation,
57:         address indexed _liquidator,
58:         uint _premiumToLiquidator
59:     );
60:     event BaseRateUpdated(uint256 _baseRate);
61:     event LastRedemptionTimestampUpdated(uint256 _lastFeeOpTime);
62:     event TotalStakesUpdated(uint256 _newTotalStakes);
63:     event SystemSnapshotsUpdated(uint256 _totalStakesSnapshot, uint256 _totalCollateralSnapshot);
64:     event SystemDebtRedistributionIndexUpdated(uint256 _systemDebtRedistributionIndex);
65:     event CdpDebtRedistributionIndexUpdated(bytes32 _cdpId, uint256 _cdpDebtRedistributionIndex);
66:     event CdpArrayIndexUpdated(bytes32 _cdpId, uint256 _newIndex);
67:     event StEthIndexUpdated(uint256 _oldIndex, uint256 _newIndex, uint256 _updTimestamp);
68:     event CollateralFeePerUnitUpdated(uint256 _oldPerUnit, uint256 _newPerUnit, uint256 _feeTaken);
69:     event CdpFeeSplitApplied(
70:         bytes32 _cdpId,
71:         uint256 _oldPerUnitCdp,
72:         uint256 _newPerUnitCdp,
73:         uint256 _collReduced,
74:         uint256 _collLeft
75:     );

```
[L17](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L17), [L23](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L23)

```solidity
File: packages/contracts/contracts/Interfaces/ICollSurplusPool.sol

9:     event CollSharesTransferred(address indexed _to, uint256 _amount);

11:     event SweepTokenSuccess(address indexed _token, uint256 _amount, address indexed _recipient);

```
[L9](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICollSurplusPool.sol#L9), [L11](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICollSurplusPool.sol#L11)

```solidity
File: packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol

8:     event FlashFeeSet(address indexed _setter, uint256 _oldFee, uint256 _newFee);
9:     event MaxFlashFeeSet(address indexed _setter, uint256 _oldMaxFee, uint256 _newMaxFee);
10:     event FlashLoansPaused(address indexed _setter, bool _paused);

```
[L8](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol#L8)

```solidity
File: packages/contracts/contracts/Interfaces/IPool.sol

10:     event EBTCBalanceUpdated(uint256 _newBalance);
11:     event CollSharesTransferred(address indexed _to, uint256 _amount);

```
[L10](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPool.sol#L10)

```solidity
File: packages/contracts/contracts/Interfaces/IPositionManagers.sol

12:     event PositionManagerApprovalSet(
13:         address indexed _borrower,
14:         address indexed _positionManager,
15:         PositionManagerApproval _approval
16:     );

```
[L12](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPositionManagers.sol#L12)

```solidity
File: packages/contracts/contracts/Interfaces/IPriceFeed.sol

8:     event PriceFeedStatusChanged(Status newStatus);
9:     event FallbackCallerChanged(
10:         address indexed _oldFallbackCaller,
11:         address indexed _newFallbackCaller
12:     );
13:     event UnhealthyFallbackCaller(address indexed _fallbackCaller, uint256 timestamp);

```
[L8](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPriceFeed.sol#L8)

```solidity
File: packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol

6:     event TCRNotified(uint256 TCR); /// NOTE: Mostly for debugging to ensure synch

10:     event GracePeriodEnd();
11:     event GracePeriodDurationSet(uint256 _recoveryModeGracePeriodDuration);

```
[L6](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol#L6), [L10](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol#L10)

```solidity
File: packages/contracts/contracts/Interfaces/ISortedCdps.sol

10:     event NodeRemoved(bytes32 _id);

```
[L10](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L10)

</details>

&nbsp;
## [N-46] NatSpec `@notice` missing from function

The `@notice` tag is used to explain the purpose of the function.

<details>
<summary>Instances: 122</summary>

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

320:     /*
321:      * _adjustCdpInternal(): Alongside a debt change, this function can perform either
322:      * a collateral top-up or a collateral withdrawal.
323:      *
324:      * It therefore expects either a positive _stEthBalanceIncrease, or a positive _stEthBalanceDecrease argument.
325:      *
326:      * If both are positive, it will revert.
327:      */
328:     function _adjustCdpInternal(
329:         bytes32 _cdpId,
330:         uint256 _stEthBalanceDecrease,
331:         uint256 _debtChange,
332:         bool _isDebtIncrease,
333:         bytes32 _upperHint,
334:         bytes32 _lowerHint,
335:         uint256 _stEthBalanceIncrease
336:     ) internal {

742:     // --- Helper functions ---

744:     function _getCollSharesChangeFromStEthChange(
745:         uint256 _collReceived,
746:         uint256 _requestedCollWithdrawal
747:     ) internal view returns (uint256 collSharesChange, bool isCollIncrease) {

789:     /// @dev Mint specified debt tokens to account and change global debt accounting accordingly
790:     function _withdrawDebt(address _account, uint256 _debt) internal {

795:     // Burn the specified amount of EBTC from _account and decreases the total active debt
796:     function _repayDebt(address _account, uint256 _debt) internal {

801:     // --- 'Require' wrapper functions ---

803:     function _requireSingularCollChange(
804:         uint256 _stEthBalanceIncrease,
805:         uint256 _stEthBalanceDecrease
806:     ) internal pure {

985:     // Compute the new collateral ratio, considering the change in coll and debt. Assumes 0 pending rewards.
986:     function _getNewNominalICRFromCdpChange(
987:         AdjustCdpLocals memory vars,
988:         bool _isDebtIncrease
989:     ) internal pure returns (uint256) {

1003:     // Compute the new collateral ratio, considering the change in coll and debt. Assumes 0 pending rewards.
1004:     function _getNewICRFromCdpChange(
1005:         uint256 _collShares,
1006:         uint256 _debt,
1007:         uint256 _collSharesChange,
1008:         bool _isCollIncrease,
1009:         uint256 _debtChange,
1010:         bool _isDebtIncrease,
1011:         uint256 _price
1012:     ) internal view returns (uint256) {

```
[L320](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L320), [L742](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L742), [L744](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L744), [L789](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L789), [L795](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L795), [L801](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L801), [L803](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L803), [L985](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L985), [L1003](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1003)

```solidity
File: packages/contracts/contracts/CdpManager.sol

236:     /*
237:      * Called when a full redemption occurs, and closes the cdp.
238:      * The redeemer swaps (debt) EBTC for (debt)
239:      * worth of stETH, so the stETH liquidation reserve is all that remains.
240:      * In order to close the cdp, the stETH liquidation reserve is returned to the Cdp owner,
241:      * The debt recorded on the cdp's struct is zero'd elswhere, in _closeCdp.
242:      * Any surplus stETH left in the cdp, is sent to the Coll surplus pool, and can be later claimed by the borrower.
243:      */
244:     function _closeCdpByRedemption(
245:         bytes32 _cdpId,
246:         uint256 _EBTC,
247:         uint256 _collSurplus,
248:         uint256 _liquidatorRewardShares,
249:         address _borrower
250:     ) internal {

487:     // --- Helper functions ---

489:     function _getCdpIdsToRemove(
490:         bytes32 _start,
491:         uint256 _total,
492:         bytes32 _end
493:     ) internal view returns (bytes32[] memory) {

549:     // Push the owner's address to the Cdp owners list, and record the corresponding array index on the Cdp struct
550:     function _addCdpIdToArray(bytes32 _cdpId) internal returns (uint128 index) {

594:     // given an ETH:USD price, and the entire system coll and debt.
595:     function _checkPotentialRecoveryMode(
596:         uint256 _systemCollShares,
597:         uint256 _systemDebt,
598:         uint256 _price
599:     ) internal view returns (bool) {

606:     /*
607:      * This function has two impacts on the baseRate state variable:
608:      * 1) decays the baseRate based on time passed since last redemption or EBTC borrowing operation.
609:      * then,
610:      * 2) increases the baseRate based on the amount redeemed, as a proportion of total supply
611:      */
612:     function _updateBaseRateFromRedemption(
613:         uint256 _ETHDrawn,
614:         uint256 _price,
615:         uint256 _totalEBTCSupply
616:     ) internal returns (uint256) {

637:     /// @return current fee rate for redemption with base rate
638:     function getRedemptionRate() public view override returns (uint256) {

642:     /// @return current fee rate for redemption with decayed base rate
643:     function getRedemptionRateWithDecay() public view override returns (uint256) {

659:     /// @return redemption fee for the specified collateral amount
660:     /// @param _stETHToRedeem The total expected stETH amount to redeem
661:     function getRedemptionFeeWithDecay(
662:         uint256 _stETHToRedeem
663:     ) external view override returns (uint256) {

688:     // Update the last fee operation time only if time passed >= decay interval. This prevents base rate griefing.
689:     function _updateLastRedemptionTimestamp() internal {

716:     /// @return timestamp when this contract is deployed
717:     function getDeploymentStartTime() public view returns (uint256) {

735:     // --- 'require' wrapper functions ---

737:     function _requireEbtcBalanceCoversRedemptionAndWithinSupply(
738:         address _redeemer,
739:         uint256 _amount,
740:         uint256 _totalSupply
741:     ) internal view {

```
[L236](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L236), [L487](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L487), [L489](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L489), [L549](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L549), [L594](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L594), [L606](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L606), [L637](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L637), [L642](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L642), [L659](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L659), [L688](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L688), [L716](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L716), [L735](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L735), [L737](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L737)

```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

60:     // Single CDP liquidation function.
61:     function _liquidateIndividualCdpSetup(
62:         bytes32 _cdpId,
63:         uint256 _partialAmount,
64:         bytes32 _upperPartialHint,
65:         bytes32 _lowerPartialHint
66:     ) internal {

134:     // For partial liquidation, caller should use HintHelper smart contract to get correct hints for reinsertion into sorted CDP list
135:     function _liquidateIndividualCdpSetupCDP(
136:         LiquidationLocals memory _liqState,
137:         LiquidationRecoveryModeLocals memory _recoveryState
138:     ) internal {

185:     // this function would return the liquidated debt and collateral of the given CDP
186:     function _liquidateCdpInGivenMode(
187:         LiquidationLocals memory _liqState,
188:         LiquidationRecoveryModeLocals memory _recoveryState
189:     ) private returns (uint256, uint256, uint256, uint256, uint256) {

383:     // without emmiting events
384:     function _closeCdpByLiquidation(bytes32 _cdpId) private returns (uint256, uint256, uint256) {

396:     // This function would return the liquidated debt and collateral of the given CDP
397:     function _liquidateCDPPartially(
398:         LiquidationLocals memory _partialState
399:     ) private returns (uint256, uint256) {

465:     // Re-Insertion into SortedCdp list after partial liquidation
466:     function _reInsertPartialLiquidation(
467:         LiquidationLocals memory _partialState,
468:         uint256 _newNICR,
469:         uint256 _oldDebt,
470:         uint256 _oldColl
471:     ) internal {

543:     // Partial Liquidation Cap Logic
544:     function _calculatePartialLiquidationSurplusAndCap(
545:         uint256 _ICR,
546:         uint256 _price,
547:         uint256 _totalDebtToBurn,
548:         uint256 _totalColToSend
549:     ) private view returns (uint256 toLiquidator, uint256 collSurplus, uint256 debtToRedistribute) {

606:     // --- Batch liquidation functions ---

608:     function _getLiquidationValuesNormalMode(
609:         uint256 _price,
610:         uint256 _TCR,
611:         LocalVariables_LiquidationSequence memory vars,
612:         LiquidationValues memory singleLiquidation
613:     ) internal {

729:     /*
730:      * This function is used when the batch liquidation starts during Recovery Mode. However, it
731:      * handle the case where the system *leaves* Recovery Mode, part way through the liquidation processing
732:      */
733:     function _getTotalFromBatchLiquidate_RecoveryMode(
734:         uint256 _price,
735:         uint256 _systemCollShares,
736:         uint256 _systemDebt,
737:         bytes32[] memory _cdpArray
738:     ) internal returns (LiquidationTotals memory totals) {

837:     // --- Liquidation helper functions ---

839:     function _addLiquidationValuesToTotals(
840:         LiquidationTotals memory oldTotals,
841:         LiquidationValues memory singleLiquidation
842:     ) internal pure returns (LiquidationTotals memory newTotals) {

894:     // --- 'require' wrapper functions ---

896:     function _requirePartialLiqDebtSize(
897:         uint256 _partialDebt,
898:         uint256 _entireDebt,
899:         uint256 _price
900:     ) internal view {

```
[L60](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L60), [L134](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L134), [L185](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L185), [L383](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L383), [L396](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L396), [L465](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L465), [L543](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L543), [L606](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L606), [L608](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L608), [L729](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L729), [L837](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L837), [L839](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L839), [L894](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L894), [L896](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L896)

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

47:     /// @dev Internal notify called by Redemptions and Liquidations
48:     /// @dev Specified TCR is emitted for notification pruposes regardless of whether the Grace Period timestamp is set
49:     function _startGracePeriod(uint256 _tcr) internal {

85:     /// @dev Set RM grace period based on specified system collShares, system debt, and price
86:     /// @dev Variant for internal use in redemptions and liquidations
87:     function _syncGracePeriodForGivenValues(
88:         uint256 systemCollShares,
89:         uint256 systemDebt,
90:         uint256 price
91:     ) internal {

282:     /*
283:      * Updates snapshots of system total stakes and total collateral,
284:      * excluding a given collateral remainder from the calculation.
285:      * Used in a liquidation sequence.
286:      *
287:      * The calculation excludes a portion of collateral that is in the ActivePool:
288:      *
289:      * the total stETH liquidator reward compensation from the liquidation sequence
290:      *
291:      * The stETH as compensation must be excluded as it is always sent out at the very end of the liquidation sequence.
292:      */
293:     function _updateSystemSnapshotsExcludeCollRemainder(uint256 _collRemainder) internal {

303:     /// @dev get the pending Cdp debt "reward" (i.e. the amount of extra debt assigned to the Cdp) from liquidation redistribution events, earned by their stake
304:     function _getPendingRedistributedDebt(
305:         bytes32 _cdpId
306:     ) internal view returns (uint256 pendingEBTCDebtReward, uint256 _debtIndexDiff) {

322:     /*
323:      * A Cdp has pending redistributed debt if its snapshot is less than the current rewards per-unit-staked sum:
324:      * this indicates that redistributions have occured since the snapshot was made, and the user therefore has
325:      * pending debt
326:      */
327:     function _hasRedistributedDebt(bytes32 _cdpId) internal view returns (bool) {

335:     /// @dev Sync Cdp debt redistribution index to global value
336:     function _updateRedistributedDebtIndex(bytes32 _cdpId) internal {

343:     /// @dev Calculate the new collateral and debt values for a given CDP, based on pending state changes
344:     function _syncAccounting(bytes32 _cdpId) internal {

409:     // Remove borrower's stake from the totalStakes sum, and set their stake to 0
410:     function _removeStake(bytes32 _cdpId) internal {

418:     // and update totalStakes accordingly as well
419:     function _updateStakeAndTotalStakes(bytes32 _cdpId) internal returns (uint256) {

430:     // Update borrower's stake based on their latest collateral value
431:     function _updateStakeForCdp(bytes32 _cdpId) internal returns (uint256, uint256) {

440:     // Calculate a new stake based on the snapshots of the totalStakes and totalCollateral taken at the last liquidation
441:     function _computeNewStake(uint256 _coll) internal view returns (uint256) {

459:     /*
460:      * Remove a Cdp owner from the CdpOwners array, not preserving array order. Removing owner 'B' does the following:
461:      * [A B C D E] => [A E C D], and updates E's Cdp struct to point to its new array index.
462:      */
463:     function _removeCdp(bytes32 _cdpId, uint256 cdpIdsArrayLength) internal {

488:     // Calculate TCR given an price, and the entire system coll and debt.
489:     function _computeTCRWithGivenSystemValues(
490:         uint256 _systemCollShares,
491:         uint256 _systemDebt,
492:         uint256 _price
493:     ) internal view returns (uint256) {

532:     /// @return existing(old) local stETH index AND
533:     /// @return current(new) stETH index from collateral token
534:     function _readStEthIndex() internal view returns (uint256, uint256) {

538:     // Update the global index via collateral token
539:     function _syncStEthIndex(uint256 _oldIndex, uint256 _newIndex) internal {

573:     // and update global fee-per-unit accumulator
574:     function _takeSplitAndUpdateFeePerUnit(
575:         uint256 _feeTaken,
576:         uint256 _newPerUnit,
577:         uint256 _newErrorPerUnit
578:     ) internal {

591:     // and update its accumulator tracker accordingly
592:     function _applyAccumulatedFeeSplit(
593:         bytes32 _cdpId,
594:         uint256 _newColl,
595:         uint256 _feeSplitDistributed,
596:         uint256 _oldPerUnitCdp,
597:         uint256 _systemStEthFeePerUnitIndex
598:     ) internal {

647:     // -- Modifier functions --
648:     function _requireCdpIsActive(bytes32 _cdpId) internal view {

726:     /// @return Whether the debt redistribution tracking index of the specified Cdp is less than the global tracking one (meaning it might get pending debt redistribution)
727:     /// @param _cdpId The CdpId whose debt redistribution tracking index to be queried against the gloabl one
728:     function hasPendingRedistributedDebt(bytes32 _cdpId) public view returns (bool) {

732:     // Return the Cdps entire debt and coll struct
733:     function _getSyncedDebtAndCollShares(
734:         bytes32 _cdpId
735:     ) internal view returns (CdpDebtAndCollShares memory) {

757:     /// @dev calculate pending global state change to be applied:
758:     /// @return split fee taken (if any) AND
759:     /// @return new split index per stake unit AND
760:     /// @return new split index error
761:     function _calcSyncedGlobalAccounting(
762:         uint256 _newIndex,
763:         uint256 _oldIndex
764:     ) internal view returns (uint256, uint256, uint256) {

781:     /// @dev calculate pending state change to be applied for given CDP and global split index(typically already synced):
782:     /// @return new CDP collateral share after pending change applied
783:     /// @return new CDP debt after pending change applied
784:     /// @return split fee applied to given CDP
785:     /// @return redistributed debt applied to given CDP
786:     /// @return delta between debt redistribution index of given CDP and global tracking index
787:     function _calcSyncedAccounting(
788:         bytes32 _cdpId,
789:         uint256 _cdpPerUnitIdx,
790:         uint256 _systemStEthFeePerUnitIndex
791:     ) internal view returns (uint256, uint256, uint256, uint256, uint256) {

821:     /// @return CDP debt and pending redistribution from liquidation applied
822:     function _getSyncedCdpDebtAndRedistribution(
823:         bytes32 _cdpId
824:     ) internal view returns (uint256, uint256, uint256) {

886:     /// @param icr The ICR of a Cdp to check if liquidatable
887:     /// @param tcr The TCR of the eBTC system used to determine if Recovery Mode is triggered
888:     /// @return whether the Cdp of specified icr is liquidatable with specified tcr
889:     /// @dev The flag will only be set to true if enough time has passed since Grace Period starts
890:     function canLiquidateRecoveryMode(uint256 icr, uint256 tcr) public view returns (bool) {

894:     /// @dev Check if enough time has passed for grace period after enabled
895:     function _recoveryModeGracePeriodPassed() internal view returns (bool) {

```
[L47](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L47), [L85](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L85), [L282](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L282), [L303](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L303), [L322](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L322), [L335](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L335), [L343](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L343), [L409](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L409), [L418](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L418), [L430](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L430), [L440](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L440), [L459](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L459), [L488](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L488), [L532](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L532), [L538](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L538), [L573](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L573), [L591](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L591), [L647](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L647), [L726](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L726), [L732](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L732), [L757](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L757), [L781](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L781), [L821](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L821), [L886](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L886), [L894](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L894)

```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

60:     /// @return The current total collateral surplus available in this pool
61:     function getTotalSurplusCollShares() external view override returns (uint256) {

65:     /// @return The collateral surplus available for the specified owner _account
66:     /// @param _account The address of the owner whose surplus balance to be queried
67:     function getSurplusCollShares(address _account) external view override returns (uint256) {

110:     // --- 'require' functions ---

112:     function _requireCallerIsBorrowerOperations() internal view {

```
[L60](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L60), [L65](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L65), [L110](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L110), [L112](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L112)

```solidity
File: packages/contracts/contracts/EBTCToken.sol

109:     // --- External functions ---

111:     function totalSupply() external view override returns (uint256) {

223:     /// @dev Return current nonce for specified owner fOR EIP-2612 compatibility
224:     /// @param owner The address whose nonce to be queried
225:     function nonces(address owner) external view override(IERC2612, PermitNonce) returns (uint256) {

229:     // --- Internal operations ---

231:     function _chainID() private view returns (uint256) {

244:     // Warning: sanity checks (for sender and recipient) should have been done before calling these internal functions

246:     function _transfer(address sender, address recipient, uint256 amount) internal {

293:     // --- 'require' functions ---

295:     function _requireValidRecipient(address _recipient) internal view {

313:     /// @dev authority check last to short-circuit in the case of use by usual immutable addresses
314:     function _requireCallerIsBOorCdpMOrAuth() internal view {

```
[L109](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L109), [L111](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L111), [L223](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L223), [L229](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L229), [L231](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L231), [L244](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L244), [L246](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L246), [L293](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L293), [L295](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L295), [L313](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L313)

```solidity
File: packages/contracts/contracts/PriceFeed.sol

787:     // @return The aggregated calculated price for stETH:BTC
788:     function _formatClAggregateAnswer(
789:         int256 _ethBtcAnswer,
790:         int256 _stEthEthAnswer,
791:         uint8 _ethBtcDecimals,
792:         uint8 _stEthEthDecimals
793:     ) internal view returns (uint256) {

```
[L787](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L787)

```solidity
File: packages/contracts/contracts/SortedCdps.sol

148:     /// @dev a pagination-flavor search (from least ICR to biggest ICR) for CDP owned by given owner and specified index (starting at given CDP)
149:     /// @param owner address of CDP owner
150:     /// @param index index of CDP, ordered by position in linked list relative to Cdps of the same owner
151:     /// @param startNodeId the seach traversal will start at this given CDP instead of the tail of the list
152:     /// @param maxNodes the traversal will go through the list by this given maximum limit of number of Cdps
153:     /// @return CDP Id if found, else return last seen CDP
154:     /// @return True if CDP found, false otherwise
155:     function cdpOfOwnerByIdx(
156:         address owner,
157:         uint256 index,
158:         bytes32 startNodeId,
159:         uint maxNodes
160:     ) external view override returns (bytes32, bool) {

235:     /// @dev return the found CDP count owned by given owner with
236:     /// @dev current lastly-visited CDP as the startNode for next pagination
237:     function _cdpCountOf(
238:         address owner,
239:         bytes32 startNodeId,
240:         uint maxNodes
241:     ) internal view returns (uint256, bytes32) {

280:     /// @dev a pagination-flavor search retrieval of (from least ICR to biggest ICR) Cdps owned by given owner (starting at given CDP)
281:     /// @param startNodeId the traversal will start at this given CDP instead of the tail of the list
282:     /// @param maxNodes the traversal will go through the list by this given maximum limit of number of Cdps
283:     /// @return all CdpIds of the specified owner found by search starting at the specified startNodeId for the specified maximum iteration count
284:     /// @return found number of Cdp for the owner
285:     /// @return starting CdpId for next pagination within current SortedCdps
286:     function getAllCdpsOf(
287:         address owner,
288:         bytes32 startNodeId,
289:         uint maxNodes
290:     ) external view override returns (bytes32[] memory, uint256, bytes32) {

297:     /// @dev return EITHER the found Cdps (also the count) owned by given owner OR empty array with
298:     /// @dev current lastly-visited CDP as the startNode for next pagination
299:     function _getCdpsOf(
300:         address owner,
301:         bytes32 startNodeId,
302:         uint maxNodes,
303:         uint maxArraySize
304:     ) internal view returns (bytes32[] memory, uint256, bytes32) {

516:     /// @dev Checks if the list contains a given node Id
517:     /// @param _id The Id of the node
518:     /// @return true if the node exists, false otherwise
519:     function contains(bytes32 _id) public view override returns (bool) {

528:     /// @dev Checks if the list is full
529:     /// @return true if the list is full, false otherwise
530:     function isFull() public view override returns (bool) {

534:     /// @dev Checks if the list is empty
535:     /// @return true if the list is empty, false otherwise
536:     function isEmpty() public view override returns (bool) {

540:     /// @dev Returns the current size of the list
541:     /// @return The current size of the list
542:     function getSize() external view override returns (uint256) {

546:     /// @dev Returns the maximum size of the list
547:     /// @return The maximum size of the list
548:     function getMaxSize() external view override returns (uint256) {

552:     /// @dev Returns the first node in the list (node with the largest NICR)
553:     /// @return The Id of the first node
554:     function getFirst() external view override returns (bytes32) {

558:     /// @dev Returns the last node in the list (node with the smallest NICR)
559:     /// @return The Id of the last node
560:     function getLast() external view override returns (bytes32) {

564:     /// @dev Returns the next node (with a smaller NICR) in the list for a given node
565:     /// @param _id The Id of the node
566:     /// @return The Id of the next node
567:     function getNext(bytes32 _id) external view override returns (bytes32) {

571:     /// @dev Returns the previous node (with a larger NICR) in the list for a given node
572:     /// @param _id The Id of the node
573:     /// @return The Id of the previous node
574:     function getPrev(bytes32 _id) external view override returns (bytes32) {

578:     /// @dev Check if a pair of nodes is a valid insertion point for a new node with the given NICR
579:     /// @param _NICR Node's NICR
580:     /// @param _prevId Id of previous node for the insert position
581:     /// @param _nextId Id of next node for the insert position
582:     /// @return true if the position is valid, false otherwise
583:     function validInsertPosition(
584:         uint256 _NICR,
585:         bytes32 _prevId,
586:         bytes32 _nextId
587:     ) external view override returns (bool) {

614:     /// @dev Descend the list (larger NICRs to smaller NICRs) to find a valid insert position
615:     /// @param _NICR Node's NICR
616:     /// @param _startId Id of node to start descending the list from
617:     /// @return The previous node Id for the inserted node
618:     /// @return The next node Id for the inserted node
619:     function _descendList(uint256 _NICR, bytes32 _startId) internal view returns (bytes32, bytes32) {

637:     /// @dev Ascend the list (smaller NICRs to larger NICRs) to find a valid insert position
638:     /// @param _NICR Node's NICR
639:     /// @param _startId Id of node to start ascending the list from
640:     /// @return The previous node Id for the inserted node
641:     /// @return The next node Id for the inserted node
642:     function _ascendList(uint256 _NICR, bytes32 _startId) internal view returns (bytes32, bytes32) {

660:     /// @dev Find the insert position for a node with the given NICR
661:     /// @param _NICR Node's NICR
662:     /// @param _prevId Id of previous node for the insert position
663:     /// @param _nextId Id of next node for the insert position
664:     /// @return The previous node Id for the inserted node
665:     /// @return The next node Id for the inserted node
666:     function findInsertPosition(
667:         uint256 _NICR,
668:         bytes32 _prevId,
669:         bytes32 _nextId
670:     ) external view override returns (bytes32, bytes32) {

713:     /// @dev Asserts that the caller of the function is the CdpManager
714:     function _requireCallerIsCdpManager() internal view {

718:     /// @dev Asserts that the caller of the function is either the BorrowerOperations contract or the CdpManager
719:     function _requireCallerIsBOorCdpM() internal view {

```
[L148](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L148), [L235](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L235), [L280](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L280), [L297](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L297), [L516](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L516), [L528](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L528), [L534](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L534), [L540](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L540), [L546](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L546), [L552](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L552), [L558](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L558), [L564](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L564), [L571](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L571), [L578](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L578), [L614](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L614), [L637](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L637), [L660](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L660), [L713](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L713), [L718](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L718)

```solidity
File: packages/contracts/contracts/HintHelpers.sol

155:     /* getApproxHint() - return address of a Cdp that is, on average, (length / numTrials) positions away in the 
156:     sortedCdps list from the correct insert position of the Cdp to be inserted. 
157:     
158:     Note: The output address is worst-case O(n) positions away from the correct insert position, however, the function 
159:     is probabilistic. Input can be tuned to guarantee results to a high degree of confidence, e.g:
160: 
161:     Submitting numTrials = k * sqrt(length), with k = 15 makes it very, very likely that the ouput address will 
162:     be <= sqrt(length) positions away from the correct insert position.
163:     */
164:     function getApproxHint(
165:         uint256 _CR,
166:         uint256 _numTrials,
167:         uint256 _inputRandomSeed
168:     ) external view returns (bytes32 hint, uint256 diff, uint256 latestRandomSeed) {

```
[L155](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L155)

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

240:     /// @dev Assumes that
241:     ///     >= you prob use this one
242:     ///     <= if you don't need >= you go for lte
243:     ///     And if you really need eq, it's third
244:     function _doCheckValueType(CheckValueAndType memory check, uint256 valueToCheck) internal {

290:     /// @dev Must be memory since we had to decode it
291:     function _handleOperation(LeverageMacroOperation memory operation) internal {

381:     /// @dev Must be memory since we had to decode it
382:     function _doSwaps(SwapOperation[] memory swapData) internal {

393:     /// @dev Given a SwapOperation
394:     ///     Approves the `addressForApprove` for the exact amount
395:     ///     Calls `addressForSwap`
396:     ///     Resets the approval of `addressForApprove`
397:     ///     Performs validation via `_doSwapChecks`
398:     function _doSwap(SwapOperation memory swapData) internal {

433:     /// @dev Given `SwapCheck` performs validation on the state of this contract
434:     ///     A minOut Check
435:     function _doSwapChecks(SwapCheck[] memory swapChecks) internal {

449:     /// @dev Prevents doing arbitrary calls to protected targets
450:     function _ensureNotSystem(address addy) internal {

459:     /// @dev Must be memory since we had to decode it
460:     function _openCdpCallback(bytes memory data) internal {

473:     /// @dev Must be memory since we had to decode it
474:     function _closeCdpCallback(bytes memory data) internal {

481:     /// @dev Must be memory since we had to decode it
482:     function _adjustCdpCallback(bytes memory data) internal {

```
[L240](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L240), [L290](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L290), [L381](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L381), [L393](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L393), [L433](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L433), [L449](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L449), [L459](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L459), [L473](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L473), [L481](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L481)

```solidity
File: packages/contracts/contracts/LeverageMacroDelegateTarget.sol

62:     /// @dev Call self, since this is called via delegate call, and get owner
63:     function owner() public override returns (address) {

```
[L62](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L62)

```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

81:     /// === DIAMOND LIKE STORAGE === ///
82:     /// @dev Get pointer to storage
83:     function _getStorage() internal pure returns (DiamondLikeStorage storage ds) {

128:     /// @dev toggle callbackEnabledForCall in OurSetting
129:     function _setCallbackEnabledForCall(DiamondLikeStorage storage ds, bool _enabled) internal {

133:     /// @dev Execute one tx
134:     function _executeOne(Operation calldata op) internal {

```
[L81](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L81), [L128](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L128), [L133](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L133)

```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

58:     // --- Gas compensation functions ---

60:     function _calcNetStEthBalance(uint256 _stEthBalance) internal pure returns (uint256) {

114:     // _price is ETH/BTC
115:     function _convertDebtDenominationToBtc(
116:         uint256 _debt,
117:         uint256 _price
118:     ) internal pure returns (uint256) {

122:     /// @dev return true if given ICR is qualified for liquidation compared to configured threshold
123:     /// @dev this function ONLY checks numbers not check grace period switch for Recovery Mode
124:     function _checkICRAgainstLiqThreshold(uint256 _icr, uint _tcr) internal view returns (bool) {

133:     /// @dev return true if given ICR is qualified for liquidation compared to MCR
134:     function _checkICRAgainstMCR(uint256 _icr) internal view returns (bool) {

138:     /// @dev return true if given ICR is qualified for liquidation compared to TCR
139:     /// @dev typically used in Recovery Mode
140:     function _checkICRAgainstTCR(uint256 _icr, uint _tcr) internal view returns (bool) {

```
[L58](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L58), [L60](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L60), [L114](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L114), [L122](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L122), [L133](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L133), [L138](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L138)

```solidity
File: packages/contracts/contracts/Dependencies/EbtcMath.sol

28:     /*
29:      * Multiply two decimal numbers and use normal rounding rules:
30:      * -round product up if 19'th mantissa digit >= 5
31:      * -round product down if 19'th mantissa digit < 5
32:      *
33:      * Used only inside the exponentiation, _decPow().
34:      */
35:     function decMul(uint256 x, uint256 y) internal pure returns (uint256 decProd) {

41:     /*
42:      * _decPow: Exponentiation function for 18-digit decimal base, and integer exponent n.
43:      *
44:      * Uses the efficient "exponentiation by squaring" algorithm. O(log(n)) complexity.
45:      *
46:      * Called by two functions that represent time in units of minutes:
47:      * 1) CdpManager._calcDecayedBaseRate
48:      * 2) CommunityIssuance._getCumulativeIssuanceFraction
49:      *
50:      * The exponent is capped to avoid reverting due to overflow. The cap 525600000 equals
51:      * "minutes in 1000 years": 60 * 24 * 365 * 1000
52:      *
53:      * If a period of > 1000 years is ever used as an exponent in either of the above functions, the result will be
54:      * negligibly different from just passing the cap, since:
55:      *
56:      * In function 1), the decayed base rate will be 0 for 1000 years or > 1000 years
57:      * In function 2), the difference in tokens issued at 1000 years and any time > 1000 years, will be negligible
58:      */
59:     function _decPow(uint256 _base, uint256 _minutes) internal pure returns (uint256) {

103:     /// @dev Compute collateralization ratio, given stETH balance, price, and debt balance
104:     function _computeCR(
105:         uint256 _stEthBalance,
106:         uint256 _debt,
107:         uint256 _price
108:     ) internal pure returns (uint256) {

```
[L28](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L28), [L41](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L41), [L103](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L103)

```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

143:     /*//////////////////////////////////////////////////////////////
144:                        USER ROLE ASSIGNMENT LOGIC
145:     //////////////////////////////////////////////////////////////*/

147:     function setUserRole(address user, uint8 role, bool enabled) public virtual requiresAuth {

```
[L143](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L143), [L147](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L147)

```solidity
File: packages/contracts/contracts/Interfaces/IActivePool.sol

22:     // --- Functions ---
23:     function transferSystemCollShares(address _account, uint256 _amount) external;

```
[L22](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IActivePool.sol#L22)

```solidity
File: packages/contracts/contracts/Interfaces/IBorrowerOperations.sol

18:     // --- Functions ---

20:     function openCdp(
21:         uint256 _EBTCAmount,
22:         bytes32 _upperHint,
23:         bytes32 _lowerHint,
24:         uint256 _stEthBalance
25:     ) external returns (bytes32);

```
[L18](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L18), [L20](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L20)

```solidity
File: packages/contracts/contracts/Interfaces/ICdpManager.sol

10:     // --- Functions ---
11:     function getActiveCdpsCount() external view returns (uint256);

```
[L10](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol#L10)

```solidity
File: packages/contracts/contracts/Interfaces/ICollSurplusPool.sol

13:     // --- Contract setters ---

15:     function getTotalSurplusCollShares() external view returns (uint256);

```
[L13](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICollSurplusPool.sol#L13), [L15](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICollSurplusPool.sol#L15)

```solidity
File: packages/contracts/contracts/Interfaces/IEBTCToken.sol

9:     // --- Functions ---

11:     function mint(address _account, uint256 _amount) external;

```
[L9](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IEBTCToken.sol#L9), [L11](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IEBTCToken.sol#L11)

```solidity
File: packages/contracts/contracts/Interfaces/IERC3156FlashBorrower.sol

6:     /**
7:      * @dev Receive a flash loan.
8:      * @param initiator The initiator of the loan.
9:      * @param token The loan currency.
10:      * @param amount The amount of tokens lent.
11:      * @param fee The additional amount of tokens to repay.
12:      * @param data Arbitrary data structure, intended to contain user-defined parameters.
13:      * @return The keccak256 hash of "ERC3156FlashBorrower.onFlashLoan"
14:      */
15:     function onFlashLoan(
16:         address initiator,
17:         address token,
18:         uint256 amount,
19:         uint256 fee,
20:         bytes calldata data
21:     ) external returns (bytes32);

```
[L6](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IERC3156FlashBorrower.sol#L6)

```solidity
File: packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol

12:     /// @dev The amount of currency available to be lent.
13:     /// @param token The loan currency.
14:     /// @return The amount of `token` that can be borrowed.
15:     function maxFlashLoan(address token) external view returns (uint256);

17:     /// @dev The fee to be charged for a given loan.
18:     /// @param token The loan currency.
19:     /// @param amount The amount of tokens lent.
20:     /// @return The amount of `token` to be charged for the loan, on top of the returned principal.
21:     function flashFee(address token, uint256 amount) external view returns (uint256);

23:     /// @dev Initiate a flash loan.
24:     /// @param receiver The receiver of the tokens in the loan, and the receiver of the callback.
25:     /// @param token The loan currency.
26:     /// @param amount The amount of tokens lent.
27:     /// @param data Arbitrary data structure, intended to contain user-defined parameters.
28:     function flashLoan(
29:         IERC3156FlashBorrower receiver,
30:         address token,
31:         uint256 amount,
32:         bytes calldata data
33:     ) external returns (bool);

```
[L12](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol#L12), [L17](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol#L17), [L23](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol#L23)

```solidity
File: packages/contracts/contracts/Interfaces/IFallbackCaller.sol

12:     //       The system will assume an 18 decimal response for efficiency.
13:     function getFallbackResponse() external view returns (uint256, uint256, bool);

16:     // of storing in the `PriceFeed` contract is retrieve for the `FallbackCaller`
17:     function fallbackTimeout() external view returns (uint256);

19:     // --- Function External Setter ---

21:     function setFallbackTimeout(uint256 newFallbackTimeout) external;

```
[L12](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IFallbackCaller.sol#L12), [L16](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IFallbackCaller.sol#L16), [L19](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IFallbackCaller.sol#L19), [L21](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IFallbackCaller.sol#L21)

```solidity
File: packages/contracts/contracts/Interfaces/IPermitNonce.sol

6:     // --- Functions ---
7:     function increasePermitNonce() external returns (uint256);

```
[L6](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPermitNonce.sol#L6)

```solidity
File: packages/contracts/contracts/Interfaces/IPool.sol

13:     // --- Functions ---

15:     function getSystemCollShares() external view returns (uint256);

```
[L13](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPool.sol#L13), [L15](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPool.sol#L15)

```solidity
File: packages/contracts/contracts/Interfaces/IPriceFeed.sol

42:     // --- Function ---
43:     function fetchPrice() external returns (uint256);

```
[L42](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPriceFeed.sol#L42)

```solidity
File: packages/contracts/contracts/Interfaces/ISortedCdps.sol

12:     // --- Functions ---

14:     function remove(bytes32 _id) external;

```
[L12](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L12), [L14](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L14)

</details>

&nbsp;
## [N-47] NatSpec `@author` missing

The `@author` tag is used to credit the author of the contract.

<details>
<summary>Instances: 16</summary>

```solidity
File: packages/contracts/contracts/ActivePool.sol

22: contract ActivePool is IActivePool, ERC3156FlashLender, ReentrancyGuard, BaseMath, AuthNoOwner {

```
[L22](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L22)

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

21: contract BorrowerOperations is
22:     EbtcBase,
23:     ReentrancyGuard,
24:     IBorrowerOperations,
25:     ERC3156FlashLender,
26:     AuthNoOwner,
27:     PermitNonce
28: {

```
[L21](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L21)

```solidity
File: packages/contracts/contracts/CdpManager.sol

16: contract CdpManager is CdpManagerStorage, ICdpManager, Proxy {

```
[L16](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L16)

```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

13: contract LiquidationLibrary is CdpManagerStorage {

```
[L13](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L13)

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

19: contract CdpManagerStorage is EbtcBase, ReentrancyGuard, ICdpManagerData, AuthNoOwner {

```
[L19](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L19)

```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

16: contract CollSurplusPool is ICollSurplusPool, ReentrancyGuard, AuthNoOwner {

```
[L16](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L16)

```solidity
File: packages/contracts/contracts/EBTCToken.sol

26: contract EBTCToken is IEBTCToken, AuthNoOwner, PermitNonce {

```
[L26](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L26)

```solidity
File: packages/contracts/contracts/PriceFeed.sol

21: contract PriceFeed is BaseMath, IPriceFeed, AuthNoOwner {

```
[L21](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L21)

```solidity
File: packages/contracts/contracts/SortedCdps.sol

51: contract SortedCdps is ISortedCdps {

```
[L51](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L51)

```solidity
File: packages/contracts/contracts/HintHelpers.sol

11: contract HintHelpers is EbtcBase {

```
[L11](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L11)

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

26: contract LeverageMacroBase {

```
[L26](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L26)

```solidity
File: packages/contracts/contracts/LeverageMacroDelegateTarget.sol

40: contract LeverageMacroDelegateTarget is LeverageMacroBase {

```
[L40](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L40)

```solidity
File: packages/contracts/contracts/LeverageMacroFactory.sol

11: contract LeverageMacroFactory {

```
[L11](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L11)

```solidity
File: packages/contracts/contracts/LeverageMacroReference.sol

11: contract LeverageMacroReference is LeverageMacroBase {

```
[L11](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L11)

```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

25: contract SimplifiedDiamondLike {

```
[L25](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L25)

```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

16: contract EbtcBase is BaseMath, IEbtcBase {

```
[L16](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L16)

</details>

&nbsp;
## [N-48] NatSpec `@dev` missing

The `@dev` tag is used to explain extra details to developers.

<details>
<summary>Instances: 10</summary>

```solidity
File: packages/contracts/contracts/EBTCToken.sol

10: /*
11:  *
12:  * Based upon OpenZeppelin's ERC20 contract:
13:  * https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/token/ERC20/ERC20.sol
14:  *
15:  * and their EIP2612 (ERC20Permit / ERC712) functionality:
16:  * https://github.com/OpenZeppelin/openzeppelin-contracts/blob/53516bc555a454862470e7860a9b5254db4d00f5/contracts/token/ERC20/ERC20Permit.sol
17:  *
18:  *
19:  * --- Functionality added specific to the EBTCToken ---
20:  *
21:  * 1) Transfer protection: blocklist of addresses that are invalid recipients (i.e. core Ebtc contracts) in external transfer() and transferFrom() calls.
22:  * The purpose is to protect users from losing tokens by mistakenly sending EBTC directly to a Liquity.
23:  * core contract, when they should rather call the right function.
24:  */

26: contract EBTCToken is IEBTCToken, AuthNoOwner, PermitNonce {

```
[L10](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L10), [L26](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L26)

```solidity
File: packages/contracts/contracts/Governor.sol

8: /// @notice Role based Authority that supports up to 256 roles.
9: /// @notice We have taken the tradeoff of additional storage usage for easier readabiliy without using off-chain / indexing services.
10: /// @author BadgerDAO Expanded from Solmate RolesAuthority
11: /// @author Modified from Solmate (https://github.com/transmissions11/solmate/blob/main/src/auth/authorities/RolesAuthority.sol)
12: /// @author Modified from Dappsys (https://github.com/dapphub/ds-roles/blob/master/src/roles.sol)
13: contract Governor is RolesAuthority {

```
[L8](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L8)

```solidity
File: packages/contracts/contracts/PriceFeed.sol

12: /*
13:  * PriceFeed for mainnet deployment, it connects to two Chainlink's live feeds, ETH:BTC and
14:  * stETH:ETH, which are used to aggregate the price feed of stETH:BTC in conjuction.
15:  * It also allows for a fallback oracle to intervene in case that the primary Chainlink oracle fails.
16:  *
17:  * The PriceFeed uses Chainlink as primary oracle and allows for an optional fallback source. It contains logic for
18:  * switching oracles based on oracle failures, timeouts, and conditions for returning to the primary
19:  * Chainlink oracle. In addition, it contains the mechanism to add or remove the fallback oracle through governance.
20:  */
21: contract PriceFeed is BaseMath, IPriceFeed, AuthNoOwner {

```
[L12](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L12)

```solidity
File: packages/contracts/contracts/SortedCdps.sol

9: /*
10:  * A sorted doubly linked list with nodes sorted in descending order.
11:  *
12:  * Nodes map to active Cdps in the system by Id.
13:  * Nodes are ordered according to their current nominal individual collateral ratio (NICR),
14:  * which is like the ICR but without the price, i.e., just collateral / debt.
15:  *
16:  * The list optionally accepts insert position hints.
17:  *
18:  * NICRs are computed dynamically at runtime, and not stored on the Node. This is because NICRs of active Cdps
19:  * change dynamically as liquidation events occur.
20:  *
21:  * The list relies on the fact that liquidation events preserve ordering: a liquidation decreases the NICRs of all active Cdps,
22:  * but maintains their order. A node inserted based on current NICR will maintain the correct position,
23:  * relative to it's peers, as rewards accumulate, as long as it's raw collateral and debt have not changed.
24:  * Thus, Nodes remain sorted by current NICR.
25:  *
26:  * Nodes need only be re-inserted upon a CDP operation - when the owner adds or removes collateral or debt
27:  * to their position.
28:  *
29:  * The list is a modification of the following audited SortedDoublyLinkedList:
30:  * https://github.com/livepeer/protocol/blob/master/contracts/libraries/SortedDoublyLL.sol
31:  *
32:  *
33:  * Changes made in the Liquity implementation:
34:  *
35:  * - Keys have been removed from nodes
36:  *
37:  * - Ordering checks for insertion are performed by comparing an NICR argument to the current NICR, calculated at runtime.
38:  *   The list relies on the property that ordering by ICR is maintained as the stETH:BTC price varies.
39:  *
40:  * - Public functions with parameters have been made internal to save gas, and given an external wrapper function for external access
41:  *
42:  *
43:  * Changes made in the Ebtc implementation:
44:  *
45:  * - Positions are now indexed by Ids, not addresses. Functions to generate Ids are provided.
46:  *
47:  * - Added batchRemove functions to optimize redemptions.
48:  *
49:  * - Added more O(n) getter functions and pagination-flavor variants, intended for off-chain use.
50:  */
51: contract SortedCdps is ISortedCdps {

```
[L9](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L9)

```solidity
File: packages/contracts/contracts/LeverageMacroFactory.sol

8: /**
9:  * @title Factory for deploying LeverageMacros
10:  */
11: contract LeverageMacroFactory {

```
[L8](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L8)

```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

6: /// @notice Provides a flexible and updatable auth pattern which is completely separate from application logic.
7: /// @author Solmate (https://github.com/transmissions11/solmate/blob/main/src/auth/Auth.sol)
8: /// @author Modified from Dappsys (https://github.com/dapphub/ds-auth/blob/master/src/auth.sol)
9: abstract contract Auth {

```
[L6](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L6)

```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

6: /// @notice Provides a flexible and updatable auth pattern which is completely separate from application logic.
7: /// @author Modified by BadgerDAO to remove owner
8: /// @author Solmate (https://github.com/transmissions11/solmate/blob/main/src/auth/Auth.sol)
9: /// @author Modified from Dappsys (https://github.com/dapphub/ds-auth/blob/master/src/auth.sol)
10: contract AuthNoOwner {

```
[L6](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L6)

```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

12: /*
13:  * Base contract for CdpManager, BorrowerOperations. Contains global system constants and
14:  * common functions.
15:  */
16: contract EbtcBase is BaseMath, IEbtcBase {

```
[L12](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L12)

```solidity
File: packages/contracts/contracts/Dependencies/ReentrancyGuard.sol

4: /// @notice Gas optimized reentrancy protection for smart contracts.
5: /// @author Solmate (https://github.com/transmissions11/solmate/blob/main/src/utils/ReentrancyGuard.sol)
6: /// @author Modified from OpenZeppelin (https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/security/ReentrancyGuard.sol)
7: abstract contract ReentrancyGuard {

```
[L4](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ReentrancyGuard.sol#L4)

```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

8: /// @notice Role based Authority that supports up to 256 roles.
9: /// @author BadgerDAO
10: /// @author Modified from Solmate (https://github.com/transmissions11/solmate/blob/main/src/auth/authorities/RolesAuthority.sol)
11: /// @author Modified from Dappsys (https://github.com/dapphub/ds-roles/blob/master/src/roles.sol)
12: contract RolesAuthority is IRolesAuthority, Auth, Authority {

```
[L8](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L8)

</details>

&nbsp;
## [N-49] Functions missing NatSpec

<details>
<summary>Instances: 139</summary>

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

328:     function _adjustCdpInternal(

439:     function _openCdp(

615:     function _getPositionManagerApproval(

635:     function _setPositionManagerApproval(

673:     function _chainID() private view returns (uint256) {

677:     function _buildDomainSeparator(

744:     function _getCollSharesChangeFromStEthChange(

796:     function _repayDebt(address _account, uint256 _debt) internal {

803:     function _requireSingularCollChange(

813:     function _requireNonZeroAdjustment(

824:     function _requireCdpisActive(ICdpManager _cdpManager, bytes32 _cdpId) internal view {

829:     function _requireCdpIsNonExistent(bytes32 _cdpId) internal view {

834:     function _requireNonZeroDebtChange(uint _debtChange) internal pure {

838:     function _requireNotInRecoveryMode(uint256 _tcr) internal view {

845:     function _requireNoStEthBalanceDecrease(uint256 _stEthBalanceDecrease) internal pure {

852:     function _requireValidAdjustmentInCurrentMode(

910:     function _requireICRisNotBelowMCR(uint256 _newICR) internal pure {

917:     function _requireICRisNotBelowCCR(uint256 _newICR) internal pure {

921:     function _requireNoDecreaseOfICR(uint256 _newICR, uint256 _oldICR) internal pure {

928:     function _requireNewTCRisNotBelowCCR(uint256 _newTCR) internal pure {

935:     function _requireNonZeroDebt(uint256 _debt) internal pure {

939:     function _requireAtLeastMinNetStEthBalance(uint256 _stEthBalance) internal pure {

946:     function _requireValidDebtRepayment(uint256 _currentDebt, uint256 _debtRepayment) internal pure {

953:     function _requireSufficientEbtcTokenBalance(

963:     function _requireBorrowerOrPositionManagerAndUpdateManagerApproval(address _borrower) internal {

986:     function _getNewNominalICRFromCdpChange(

1004:     function _getNewICRFromCdpChange(

1030:     function _getNewCdpAmounts(

1049:     function _getNewTCRFromCdpChange(

```
[L328](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L328), [L439](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L439), [L615](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L615), [L635](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L635), [L673](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L673), [L677](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L677), [L744](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L744), [L796](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L796), [L803](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L803), [L813](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L813), [L824](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L824), [L829](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L829), [L834](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L834), [L838](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L838), [L845](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L845), [L852](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L852), [L910](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L910), [L917](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L917), [L921](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L921), [L928](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L928), [L935](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L935), [L939](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L939), [L946](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L946), [L953](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L953), [L963](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L963), [L986](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L986), [L1004](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1004), [L1030](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1030), [L1049](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1049)

```solidity
File: packages/contracts/contracts/CdpManager.sol

244:     function _closeCdpByRedemption(

489:     function _getCdpIdsToRemove(

550:     function _addCdpIdToArray(bytes32 _cdpId) internal returns (uint128 index) {

595:     function _checkPotentialRecoveryMode(

612:     function _updateBaseRateFromRedemption(

647:     function _calcRedemptionRate(uint256 _baseRate) internal view returns (uint256) {

655:     function _getRedemptionFee(uint256 _ETHDrawn) internal view returns (uint256) {

667:     function _calcRedemptionFee(

676:     function _decayBaseRate() internal {

689:     function _updateLastRedemptionTimestamp() internal {

702:     function _calcDecayedBaseRate() internal view returns (uint256) {

709:     function _minutesPassedSinceLastRedemption() internal view returns (uint256) {

737:     function _requireEbtcBalanceCoversRedemptionAndWithinSupply(

753:     function _requireAmountGreaterThanZero(uint256 _amount) internal pure {

757:     function _requireTCRisNotBelowMCR(uint256 _price, uint256 _TCR) internal view {

761:     function _requireValidMaxFeePercentage(uint256 _maxFeePercentage) internal view {

```
[L244](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L244), [L489](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L489), [L550](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L550), [L595](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L595), [L612](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L612), [L647](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L647), [L655](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L655), [L667](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L667), [L676](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L676), [L689](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L689), [L702](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L702), [L709](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L709), [L737](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L737), [L753](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L753), [L757](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L757), [L761](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L761)

```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

61:     function _liquidateIndividualCdpSetup(

135:     function _liquidateIndividualCdpSetupCDP(

186:     function _liquidateCdpInGivenMode(

223:     function _liquidateIndividualCdpSetupCDPInNormalMode(

295:     function _liquidateIndividualCdpSetupCDPInRecoveryMode(

384:     function _closeCdpByLiquidation(bytes32 _cdpId) private returns (uint256, uint256, uint256) {

397:     function _liquidateCDPPartially(

450:     function _partiallyReduceCdpDebt(

466:     function _reInsertPartialLiquidation(

503:     function _finalizeLiquidation(

544:     function _calculatePartialLiquidationSurplusAndCap(

570:     function _calculateFullLiquidationSurplusAndCap(

608:     function _getLiquidationValuesNormalMode(

642:     function _getLiquidationValuesRecoveryMode(

733:     function _getTotalFromBatchLiquidate_RecoveryMode(

807:     function _getTotalsFromBatchLiquidate_NormalMode(

839:     function _addLiquidationValuesToTotals(

862:     function _redistributeDebt(uint256 _debt) internal {

896:     function _requirePartialLiqDebtSize(

908:     function _requirePartialLiqCollSize(uint256 _entireColl) internal pure {

```
[L61](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L61), [L135](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L135), [L186](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L186), [L223](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L223), [L295](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L295), [L384](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L384), [L397](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L397), [L450](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L450), [L466](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L466), [L503](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L503), [L544](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L544), [L570](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L570), [L608](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L608), [L642](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L642), [L733](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L733), [L807](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L807), [L839](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L839), [L862](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L862), [L896](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L896), [L908](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L908)

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

73:     function _syncGracePeriod() internal {

255:     function _closeCdp(bytes32 _cdpId, Status closedStatus) internal {

260:     function _closeCdpWithoutRemovingSortedCdps(bytes32 _cdpId, Status closedStatus) internal {

293:     function _updateSystemSnapshotsExcludeCollRemainder(uint256 _collRemainder) internal {

327:     function _hasRedistributedDebt(bytes32 _cdpId) internal view returns (bool) {

410:     function _removeStake(bytes32 _cdpId) internal {

419:     function _updateStakeAndTotalStakes(bytes32 _cdpId) internal returns (uint256) {

431:     function _updateStakeForCdp(bytes32 _cdpId) internal returns (uint256, uint256) {

441:     function _computeNewStake(uint256 _coll) internal view returns (uint256) {

463:     function _removeCdp(bytes32 _cdpId, uint256 cdpIdsArrayLength) internal {

489:     function _computeTCRWithGivenSystemValues(

509:     function _syncGlobalAccounting() internal {

539:     function _syncStEthIndex(uint256 _oldIndex, uint256 _newIndex) internal {

574:     function _takeSplitAndUpdateFeePerUnit(

592:     function _applyAccumulatedFeeSplit(

648:     function _requireCdpIsActive(bytes32 _cdpId) internal view {

652:     function _requireMoreThanOneCdpInSystem(uint256 CdpOwnersArrayLength) internal view {

659:     function _requireCallerIsBorrowerOperations() internal view {

707:     function _calculateCR(

733:     function _getSyncedDebtAndCollShares(

```
[L73](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L73), [L255](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L255), [L260](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L260), [L293](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L293), [L327](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L327), [L410](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L410), [L419](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L419), [L431](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L431), [L441](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L441), [L463](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L463), [L489](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L489), [L509](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L509), [L539](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L539), [L574](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L574), [L592](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L592), [L648](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L648), [L652](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L652), [L659](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L659), [L707](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L707), [L733](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L733)

```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

112:     function _requireCallerIsBorrowerOperations() internal view {

119:     function _requireCallerIsCdpManager() internal view {

123:     function _requireCallerIsActivePool() internal view {

```
[L112](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L112), [L119](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L119), [L123](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L123)

```solidity
File: packages/contracts/contracts/EBTCToken.sol

111:     function totalSupply() external view override returns (uint256) {

115:     function balanceOf(address account) external view override returns (uint256) {

119:     function transfer(address recipient, uint256 amount) external override returns (bool) {

125:     function allowance(address owner, address spender) external view override returns (uint256) {

129:     function approve(address spender, uint256 amount) external override returns (bool) {

134:     function transferFrom(

152:     function increaseAllowance(

160:     function decreaseAllowance(

231:     function _chainID() private view returns (uint256) {

235:     function _buildDomainSeparator(

246:     function _transfer(address sender, address recipient, uint256 amount) internal {

262:     function _mint(address account, uint256 amount) internal {

270:     function _burn(address account, uint256 amount) internal {

285:     function _approve(address owner, address spender, uint256 amount) internal {

295:     function _requireValidRecipient(address _recipient) internal view {

306:     function _requireCallerIsBorrowerOperations() internal view {

323:     function _requireCallerIsCdpM() internal view {

```
[L111](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L111), [L115](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L115), [L119](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L119), [L125](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L125), [L129](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L129), [L134](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L134), [L152](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L152), [L160](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L160), [L231](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L231), [L235](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L235), [L246](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L246), [L262](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L262), [L270](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L270), [L285](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L285), [L295](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L295), [L306](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L306), [L323](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L323)

```solidity
File: packages/contracts/contracts/PriceFeed.sol

465:     function _fallbackIsBroken(FallbackResponse memory _response) internal view returns (bool) {

493:     function _responseTimeout(uint256 _timestamp, uint256 _timeout) internal view returns (bool) {

```
[L465](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L465), [L493](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L493)

```solidity
File: packages/contracts/contracts/SortedCdps.sol

363:     function _insert(bytes32 _id, uint256 _NICR, bytes32 _prevId, bytes32 _nextId) internal {

456:     function _remove(bytes32 _id) internal {

591:     function _validInsertPosition(

674:     function _findInsertPosition(

```
[L363](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L363), [L456](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L456), [L591](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L591), [L674](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L674)

```solidity
File: packages/contracts/contracts/HintHelpers.sol

164:     function getApproxHint(

```
[L164](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L164)

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

39:     function owner() public virtual returns (address) {

43:     function _assertOwner() internal {

```
[L39](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L39), [L43](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L43)

```solidity
File: packages/contracts/contracts/LeverageMacroReference.sol

44:     function owner() public override returns (address) {

```
[L44](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L44)

```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

32:     function isAuthorized(address user, bytes4 functionSig) internal view virtual returns (bool) {

42:     function setAuthority(Authority newAuthority) public virtual {

52:     function transferOwnership(address newOwner) public virtual requiresAuth {

```
[L32](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L32), [L42](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L42), [L52](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L52)

```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

22:     function authority() public view returns (Authority) {

26:     function authorityInitialized() public view returns (bool) {

30:     function isAuthorized(address user, bytes4 functionSig) internal view virtual returns (bool) {

38:     function setAuthority(address newAuthority) public virtual {

```
[L22](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L22), [L26](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L26), [L30](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L30), [L38](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L38)

```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

60:     function _calcNetStEthBalance(uint256 _stEthBalance) internal pure returns (uint256) {

79:     function _getCachedTCR(uint256 _price) internal view returns (uint256 TCR) {

83:     function _getTCRWithSystemDebtAndCollShares(

95:     function _checkRecoveryMode(uint256 _price) internal view returns (bool) {

99:     function _checkRecoveryModeForTCR(uint256 _tcr) internal view returns (bool) {

103:     function _requireUserAcceptsFee(

115:     function _convertDebtDenominationToBtc(

```
[L60](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L60), [L79](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L79), [L83](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L83), [L95](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L95), [L99](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L99), [L103](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L103), [L115](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L115)

```solidity
File: packages/contracts/contracts/Dependencies/EbtcMath.sol

20:     function _min(uint256 _a, uint256 _b) internal pure returns (uint256) {

24:     function _max(uint256 _a, uint256 _b) internal pure returns (uint256) {

35:     function decMul(uint256 x, uint256 y) internal pure returns (uint256 decProd) {

59:     function _decPow(uint256 _base, uint256 _minutes) internal pure returns (uint256) {

88:     function _getAbsoluteDifference(uint256 _a, uint256 _b) internal pure returns (uint256) {

92:     function _computeNominalCR(uint256 _collShares, uint256 _debt) internal pure returns (uint256) {

```
[L20](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L20), [L24](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L24), [L35](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L35), [L59](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L59), [L88](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L88), [L92](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L92)

```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

38:     function doesUserHaveRole(address user, uint8 role) public view virtual returns (bool) {

42:     function doesRoleHaveCapability(

50:     function isPublicCapability(address target, bytes4 functionSig) public view returns (bool) {

147:     function setUserRole(address user, uint8 role, bool enabled) public virtual requiresAuth {

```
[L38](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L38), [L42](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L42), [L50](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L50), [L147](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L147)

</details>

&nbsp;
## [N-50] NatSpec `@param` missing

`@param` tags are used to describe the purpose of each function parameter.

<details>
<summary>Instances: 49</summary>

```solidity
File: packages/contracts/contracts/ActivePool.sol

190:     /// @notice Increases the tracked EBTC debt of the system by a specified amount
191:     /// @dev Managed by system contracts - requires that the caller is either BorrowerOperations or CdpManager
192:     /// @param _amount: The amount to increase the system EBTC debt by
193: 
194:     function increaseSystemDebt(uint256 _amount) external override {

203:     /// @notice Decreases the tracked EBTC debt of the system by a specified amount
204:     /// @dev Managed by system contracts - requires that the caller is either BorrowerOperations or CdpManager
205:     /// @param _amount: The amount to decrease the system EBTC debt by
206: 
207:     function decreaseSystemDebt(uint256 _amount) external override {

```
[L190](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L190), [L203](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L203)

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

756:     /**
757:         @notice Process the token movements required by a Cdp adjustment.
758:         @notice Handles the cases of a debt increase / decrease, and/or a collateral increase / decrease.
759:      */
760:     function _processTokenMovesFromAdjustment(MoveTokensParams memory _varMvTokens) internal {

789:     /// @dev Mint specified debt tokens to account and change global debt accounting accordingly
790:     function _withdrawDebt(address _account, uint256 _debt) internal {

```
[L756](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L756), [L789](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L789)

```solidity
File: packages/contracts/contracts/CdpManager.sol

267:     /// @notice Returns true if the CdpId specified is the lowest-ICR Cdp in the linked list that still has MCR > ICR
268:     /// @dev Returns false if the specified CdpId hint is blank
269:     /// @dev Returns false if the specified CdpId hint doesn't exist in the list
270:     /// @dev Returns false if the ICR of the specified CdpId is < MCR
271:     /// @dev Returns true if the specified CdpId is not blank, exists in the list, has an ICR > MCR, and the next lower Cdp in the list is either blank or has an ICR < MCR.
272:     function _isValidFirstRedemptionHint(
273:         bytes32 _firstRedemptionHint,
274:         uint256 _price
275:     ) internal view returns (bool) {

```
[L267](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L267)

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

47:     /// @dev Internal notify called by Redemptions and Liquidations
48:     /// @dev Specified TCR is emitted for notification pruposes regardless of whether the Grace Period timestamp is set
49:     function _startGracePeriod(uint256 _tcr) internal {

59:     /// @notice Clear RM Grace Period timestamp if it has been set
60:     /// @notice No input validation, calling function must confirm that the system is not in recovery mode to be valid
61:     /// @dev Specified TCR is emitted for notification pruposes regardless of whether the Grace Period timestamp is set
62:     /// @dev Internal notify called by Redemptions and Liquidations
63:     function _endGracePeriod(uint256 _tcr) internal {

85:     /// @dev Set RM grace period based on specified system collShares, system debt, and price
86:     /// @dev Variant for internal use in redemptions and liquidations
87:     function _syncGracePeriodForGivenValues(
88:         uint256 systemCollShares,
89:         uint256 systemDebt,
90:         uint256 price
91:     ) internal {

303:     /// @dev get the pending Cdp debt "reward" (i.e. the amount of extra debt assigned to the Cdp) from liquidation redistribution events, earned by their stake
304:     function _getPendingRedistributedDebt(
305:         bytes32 _cdpId
306:     ) internal view returns (uint256 pendingEBTCDebtReward, uint256 _debtIndexDiff) {

335:     /// @dev Sync Cdp debt redistribution index to global value
336:     function _updateRedistributedDebtIndex(bytes32 _cdpId) internal {

343:     /// @dev Calculate the new collateral and debt values for a given CDP, based on pending state changes
344:     function _syncAccounting(bytes32 _cdpId) internal {

697:     /// @notice Return the Individual Collateral Ratio (ICR) of the specified Cdp as "cached view" (maybe outdated).
698:     /// @param _cdpId The CdpId whose ICR to be queried
699:     /// @return The Individual Collateral Ratio (ICR) of the specified Cdp.
700:     /// @dev Use getSyncedICR() instead if pending fee split and debt redistribution should be considered
701:     function getCachedICR(bytes32 _cdpId, uint256 _price) public view returns (uint256) {

757:     /// @dev calculate pending global state change to be applied:
758:     /// @return split fee taken (if any) AND
759:     /// @return new split index per stake unit AND
760:     /// @return new split index error
761:     function _calcSyncedGlobalAccounting(
762:         uint256 _newIndex,
763:         uint256 _oldIndex
764:     ) internal view returns (uint256, uint256, uint256) {

781:     /// @dev calculate pending state change to be applied for given CDP and global split index(typically already synced):
782:     /// @return new CDP collateral share after pending change applied
783:     /// @return new CDP debt after pending change applied
784:     /// @return split fee applied to given CDP
785:     /// @return redistributed debt applied to given CDP
786:     /// @return delta between debt redistribution index of given CDP and global tracking index
787:     function _calcSyncedAccounting(
788:         bytes32 _cdpId,
789:         uint256 _cdpPerUnitIdx,
790:         uint256 _systemStEthFeePerUnitIndex
791:     ) internal view returns (uint256, uint256, uint256, uint256, uint256) {

821:     /// @return CDP debt and pending redistribution from liquidation applied
822:     function _getSyncedCdpDebtAndRedistribution(
823:         bytes32 _cdpId
824:     ) internal view returns (uint256, uint256, uint256) {

```
[L47](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L47), [L59](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L59), [L85](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L85), [L303](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L303), [L335](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L335), [L343](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L343), [L697](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L697), [L757](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L757), [L781](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L781), [L821](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L821)

```solidity
File: packages/contracts/contracts/PriceFeed.sol

787:     // @return The aggregated calculated price for stETH:BTC
788:     function _formatClAggregateAnswer(
789:         int256 _ethBtcAnswer,
790:         int256 _stEthEthAnswer,
791:         uint8 _ethBtcDecimals,
792:         uint8 _stEthEthDecimals
793:     ) internal view returns (uint256) {

```
[L787](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L787)

```solidity
File: packages/contracts/contracts/SortedCdps.sol

221:     /// @notice a Pagination-flavor search for the count of Cdps owned by given owner
222:     /// @notice Starts from a given CdpId in the sorted list, and moves from lowest ICR to highest ICR
223:     /// @param startNodeId the count traversal will start at this given CDP instead of the tail of the list
224:     /// @param maxNodes the traversal will go through the list by this given maximum limit of number of Cdps
225:     /// @return count Number of active Cdps owned by the address in the segment of the list traversed
226:     /// @return last seen CDP for the startNode for next pagination
227:     function getCdpCountOf(
228:         address owner,
229:         bytes32 startNodeId,
230:         uint maxNodes
231:     ) external view override returns (uint256, bytes32) {

235:     /// @dev return the found CDP count owned by given owner with
236:     /// @dev current lastly-visited CDP as the startNode for next pagination
237:     function _cdpCountOf(
238:         address owner,
239:         bytes32 startNodeId,
240:         uint maxNodes
241:     ) internal view returns (uint256, bytes32) {

280:     /// @dev a pagination-flavor search retrieval of (from least ICR to biggest ICR) Cdps owned by given owner (starting at given CDP)
281:     /// @param startNodeId the traversal will start at this given CDP instead of the tail of the list
282:     /// @param maxNodes the traversal will go through the list by this given maximum limit of number of Cdps
283:     /// @return all CdpIds of the specified owner found by search starting at the specified startNodeId for the specified maximum iteration count
284:     /// @return found number of Cdp for the owner
285:     /// @return starting CdpId for next pagination within current SortedCdps
286:     function getAllCdpsOf(
287:         address owner,
288:         bytes32 startNodeId,
289:         uint maxNodes
290:     ) external view override returns (bytes32[] memory, uint256, bytes32) {

297:     /// @dev return EITHER the found Cdps (also the count) owned by given owner OR empty array with
298:     /// @dev current lastly-visited CDP as the startNode for next pagination
299:     function _getCdpsOf(
300:         address owner,
301:         bytes32 startNodeId,
302:         uint maxNodes,
303:         uint maxArraySize
304:     ) internal view returns (bytes32[] memory, uint256, bytes32) {

```
[L221](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L221), [L235](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L235), [L280](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L280), [L297](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L297)

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

117:     /// @notice Entry point for the Macro
118:     function doOperation(
119:         FlashLoanType flType,
120:         uint256 borrowAmount,
121:         LeverageMacroOperation calldata operation,
122:         PostOperationCheck postCheckType,
123:         PostCheckParams calldata checkParams
124:     ) external {

232:     /// @notice Transfer an arbitrary token back to you
233:     /// @dev If you delegatecall into this, this will transfer the tokens to the caller of the DiamondLike (and not the contract)
234:     function sweepToken(address token, uint256 amount) public {

240:     /// @dev Assumes that
241:     ///     >= you prob use this one
242:     ///     <= if you don't need >= you go for lte
243:     ///     And if you really need eq, it's third
244:     function _doCheckValueType(CheckValueAndType memory check, uint256 valueToCheck) internal {

290:     /// @dev Must be memory since we had to decode it
291:     function _handleOperation(LeverageMacroOperation memory operation) internal {

337:     /// @notice Convenience function to parse bytes into LeverageMacroOperation data
338:     function decodeFLData(bytes calldata data) public view returns (LeverageMacroOperation memory) {

343:     /// @notice Proper Flashloan Callback handler
344:     function onFlashLoan(
345:         address initiator,
346:         address token,
347:         uint256 amount,
348:         uint256 fee,
349:         bytes calldata data
350:     ) external returns (bytes32) {

381:     /// @dev Must be memory since we had to decode it
382:     function _doSwaps(SwapOperation[] memory swapData) internal {

393:     /// @dev Given a SwapOperation
394:     ///     Approves the `addressForApprove` for the exact amount
395:     ///     Calls `addressForSwap`
396:     ///     Resets the approval of `addressForApprove`
397:     ///     Performs validation via `_doSwapChecks`
398:     function _doSwap(SwapOperation memory swapData) internal {

433:     /// @dev Given `SwapCheck` performs validation on the state of this contract
434:     ///     A minOut Check
435:     function _doSwapChecks(SwapCheck[] memory swapChecks) internal {

449:     /// @dev Prevents doing arbitrary calls to protected targets
450:     function _ensureNotSystem(address addy) internal {

459:     /// @dev Must be memory since we had to decode it
460:     function _openCdpCallback(bytes memory data) internal {

473:     /// @dev Must be memory since we had to decode it
474:     function _closeCdpCallback(bytes memory data) internal {

481:     /// @dev Must be memory since we had to decode it
482:     function _adjustCdpCallback(bytes memory data) internal {

496:     /// @dev excessivelySafeCall to perform generic calls without getting gas bombed | useful if you don't care about return value
497:     /// @notice Credits to: https://github.com/nomad-xyz/ExcessivelySafeCall/blob/main/src/ExcessivelySafeCall.sol
498:     function excessivelySafeCall(
499:         address _target,
500:         uint256 _gas,
501:         uint256 _value,
502:         uint16 _maxCopy,
503:         bytes memory _calldata
504:     ) internal returns (bool, bytes memory) {

```
[L117](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L117), [L232](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L232), [L240](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L240), [L290](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L290), [L337](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L337), [L343](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L343), [L381](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L381), [L393](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L393), [L433](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L433), [L449](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L449), [L459](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L459), [L473](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L473), [L481](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L481), [L496](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L496)

```solidity
File: packages/contracts/contracts/LeverageMacroFactory.sol

42:     /// @notice Deploys a new macro for an owner, only they can operate the macro
43:     function deployNewMacro(address _owner) public returns (address) {

```
[L42](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L42)

```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

48:     /// === HARDCODED SETTERS === ///
49:     /// @notice Given a funsig and a implementation address
50:     ///     Set the handler to the logic we will delegatecall to
51:     function setFallbackHandler(bytes4 sig, address handler) external {

63:     /// @notice Do you want to allow any caller to call this contract?
64:     ///     This is a VERY DANGEROUS setting
65:     ///     Do not call this unless you know what you are doing
66:     function setAllowAnyCall(bool allowNonCallbacks) external {

109:     /// @notice Execute a list of operations in sequence
110:     function execute(Operation[] calldata ops) external payable {

128:     /// @dev toggle callbackEnabledForCall in OurSetting
129:     function _setCallbackEnabledForCall(DiamondLikeStorage storage ds, bool _enabled) internal {

133:     /// @dev Execute one tx
134:     function _executeOne(Operation calldata op) internal {

```
[L48](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L48), [L63](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L63), [L109](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L109), [L128](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L128), [L133](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L133)

```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

53:     /// @notice Changed constructor to initialize to allow flexiblity of constructor vs initializer use
54:     /// @notice sets authorityInitiailzed flag to ensure only one use of
55:     function _initializeAuthority(address newAuthority) internal {

```
[L53](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L53)

```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

122:     /// @dev return true if given ICR is qualified for liquidation compared to configured threshold
123:     /// @dev this function ONLY checks numbers not check grace period switch for Recovery Mode
124:     function _checkICRAgainstLiqThreshold(uint256 _icr, uint _tcr) internal view returns (bool) {

133:     /// @dev return true if given ICR is qualified for liquidation compared to MCR
134:     function _checkICRAgainstMCR(uint256 _icr) internal view returns (bool) {

138:     /// @dev return true if given ICR is qualified for liquidation compared to TCR
139:     /// @dev typically used in Recovery Mode
140:     function _checkICRAgainstTCR(uint256 _icr, uint _tcr) internal view returns (bool) {

```
[L122](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L122), [L133](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L133), [L138](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L138)

```solidity
File: packages/contracts/contracts/Dependencies/EbtcMath.sol

103:     /// @dev Compute collateralization ratio, given stETH balance, price, and debt balance
104:     function _computeCR(
105:         uint256 _stEthBalance,
106:         uint256 _debt,
107:         uint256 _price
108:     ) internal pure returns (uint256) {

```
[L103](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L103)

```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

58:     /**
59:         @notice A user can call a given function signature on a given target address if:
60:             - The capability has not been burned
61:             - That capability is public, or the user has a role that has been granted the capability to call the function
62:      */
63:     function canCall(
64:         address user,
65:         address target,
66:         bytes4 functionSig
67:     ) public view virtual override returns (bool) {

83:     /// @notice Set a capability flag as public, meaning any account can call it. Or revoke this capability.
84:     /// @dev A capability cannot be made public if it has been burned.
85:     function setPublicCapability(
86:         address target,
87:         bytes4 functionSig,
88:         bool enabled
89:     ) public virtual requiresAuth {

104:     /// @notice Grant a specified role the ability to call a function on a target.
105:     /// @notice Has no effect
106:     function setRoleCapability(
107:         uint8 role,
108:         address target,
109:         bytes4 functionSig,
110:         bool enabled
111:     ) public virtual requiresAuth {

132:     /// @notice Permanently burns a capability for a target.
133:     function burnCapability(address target, bytes4 functionSig) public virtual requiresAuth {

```
[L58](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L58), [L83](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L83), [L104](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L104), [L132](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L132)

</details>

&nbsp;
## [N-51] NatSpec `@return` missing

The `@return` tag is used to explain the functions return value.

<details>
<summary>Instances: 23</summary>

```solidity
File: packages/contracts/contracts/CdpManager.sol

267:     /// @notice Returns true if the CdpId specified is the lowest-ICR Cdp in the linked list that still has MCR > ICR
268:     /// @dev Returns false if the specified CdpId hint is blank
269:     /// @dev Returns false if the specified CdpId hint doesn't exist in the list
270:     /// @dev Returns false if the ICR of the specified CdpId is < MCR
271:     /// @dev Returns true if the specified CdpId is not blank, exists in the list, has an ICR > MCR, and the next lower Cdp in the list is either blank or has an ICR < MCR.
272:     function _isValidFirstRedemptionHint(
273:         bytes32 _firstRedemptionHint,
274:         uint256 _price
275:     ) internal view returns (bool) {

520:     /// @notice Update stake for the specified Cdp and total stake within the system.
521:     /// @dev Only BorrowerOperations is allowed to call this function
522:     /// @param _cdpId cdpId to update stake for
523:     function updateStakeAndTotalStakes(bytes32 _cdpId) external override returns (uint256) {

```
[L267](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L267), [L520](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L520)

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

303:     /// @dev get the pending Cdp debt "reward" (i.e. the amount of extra debt assigned to the Cdp) from liquidation redistribution events, earned by their stake
304:     function _getPendingRedistributedDebt(
305:         bytes32 _cdpId
306:     ) internal view returns (uint256 pendingEBTCDebtReward, uint256 _debtIndexDiff) {

821:     /// @return CDP debt and pending redistribution from liquidation applied
822:     function _getSyncedCdpDebtAndRedistribution(
823:         bytes32 _cdpId
824:     ) internal view returns (uint256, uint256, uint256) {

894:     /// @dev Check if enough time has passed for grace period after enabled
895:     function _recoveryModeGracePeriodPassed() internal view returns (bool) {

```
[L303](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L303), [L821](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L821), [L894](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L894)

```solidity
File: packages/contracts/contracts/EBTCToken.sol

223:     /// @dev Return current nonce for specified owner fOR EIP-2612 compatibility
224:     /// @param owner The address whose nonce to be queried
225:     function nonces(address owner) external view override(IERC2612, PermitNonce) returns (uint256) {

```
[L223](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L223)

```solidity
File: packages/contracts/contracts/PriceFeed.sol

93:     /// @notice Returns the latest price obtained from the Oracle
94:     /// @dev Called by eBTC functions that require a current price. Also callable permissionlessly.
95:     /// @dev Non-view function - it updates and stores the last good price seen by eBTC.
96:     /// @dev Uses a main oracle (Chainlink) and a fallback oracle in case Chainlink fails. If both fail, it uses the last good price seen by eBTC.
97:     /// @dev The fallback oracle address can be swapped by the Authority. The fallback oracle must conform to the IFallbackCaller interface.
98:     function fetchPrice() external override returns (uint256) {

```
[L93](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L93)

```solidity
File: packages/contracts/contracts/SortedCdps.sol

235:     /// @dev return the found CDP count owned by given owner with
236:     /// @dev current lastly-visited CDP as the startNode for next pagination
237:     function _cdpCountOf(
238:         address owner,
239:         bytes32 startNodeId,
240:         uint maxNodes
241:     ) internal view returns (uint256, bytes32) {

297:     /// @dev return EITHER the found Cdps (also the count) owned by given owner OR empty array with
298:     /// @dev current lastly-visited CDP as the startNode for next pagination
299:     function _getCdpsOf(
300:         address owner,
301:         bytes32 startNodeId,
302:         uint maxNodes,
303:         uint maxArraySize
304:     ) internal view returns (bytes32[] memory, uint256, bytes32) {

```
[L235](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L235), [L297](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L297)

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

337:     /// @notice Convenience function to parse bytes into LeverageMacroOperation data
338:     function decodeFLData(bytes calldata data) public view returns (LeverageMacroOperation memory) {

343:     /// @notice Proper Flashloan Callback handler
344:     function onFlashLoan(
345:         address initiator,
346:         address token,
347:         uint256 amount,
348:         uint256 fee,
349:         bytes calldata data
350:     ) external returns (bytes32) {

496:     /// @dev excessivelySafeCall to perform generic calls without getting gas bombed | useful if you don't care about return value
497:     /// @notice Credits to: https://github.com/nomad-xyz/ExcessivelySafeCall/blob/main/src/ExcessivelySafeCall.sol
498:     function excessivelySafeCall(
499:         address _target,
500:         uint256 _gas,
501:         uint256 _value,
502:         uint16 _maxCopy,
503:         bytes memory _calldata
504:     ) internal returns (bool, bytes memory) {

```
[L337](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L337), [L343](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L343), [L496](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L496)

```solidity
File: packages/contracts/contracts/LeverageMacroDelegateTarget.sol

62:     /// @dev Call self, since this is called via delegate call, and get owner
63:     function owner() public override returns (address) {

```
[L62](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L62)

```solidity
File: packages/contracts/contracts/LeverageMacroFactory.sol

37:     /// @notice Deploys a new macro for you
38:     function deployNewMacro() external returns (address) {

42:     /// @notice Deploys a new macro for an owner, only they can operate the macro
43:     function deployNewMacro(address _owner) public returns (address) {

```
[L37](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L37), [L42](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L42)

```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

81:     /// === DIAMOND LIKE STORAGE === ///
82:     /// @dev Get pointer to storage
83:     function _getStorage() internal pure returns (DiamondLikeStorage storage ds) {

```
[L81](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L81)

```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

64:     /// @notice Get the entire system collateral
65:     /// @notice Entire system collateral = collateral allocated to system in ActivePool, using it's internal accounting
66:     /// @dev Collateral tokens stored in ActivePool for liquidator rewards, fees, or coll in CollSurplusPool, are not included
67:     function getSystemCollShares() public view returns (uint256 entireSystemColl) {

71:     /**
72:         @notice Get the entire system debt
73:         @notice Entire system collateral = collateral stored in ActivePool, using their internal accounting
74:      */
75:     function _getSystemDebt() internal view returns (uint256 entireSystemDebt) {

122:     /// @dev return true if given ICR is qualified for liquidation compared to configured threshold
123:     /// @dev this function ONLY checks numbers not check grace period switch for Recovery Mode
124:     function _checkICRAgainstLiqThreshold(uint256 _icr, uint _tcr) internal view returns (bool) {

133:     /// @dev return true if given ICR is qualified for liquidation compared to MCR
134:     function _checkICRAgainstMCR(uint256 _icr) internal view returns (bool) {

138:     /// @dev return true if given ICR is qualified for liquidation compared to TCR
139:     /// @dev typically used in Recovery Mode
140:     function _checkICRAgainstTCR(uint256 _icr, uint _tcr) internal view returns (bool) {

```
[L64](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L64), [L71](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L71), [L122](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L122), [L133](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L133), [L138](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L138)

```solidity
File: packages/contracts/contracts/Dependencies/EbtcMath.sol

103:     /// @dev Compute collateralization ratio, given stETH balance, price, and debt balance
104:     function _computeCR(
105:         uint256 _stEthBalance,
106:         uint256 _debt,
107:         uint256 _price
108:     ) internal pure returns (uint256) {

```
[L103](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L103)

```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

58:     /**
59:         @notice A user can call a given function signature on a given target address if:
60:             - The capability has not been burned
61:             - That capability is public, or the user has a role that has been granted the capability to call the function
62:      */
63:     function canCall(
64:         address user,
65:         address target,
66:         bytes4 functionSig
67:     ) public view virtual override returns (bool) {

```
[L58](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L58)

</details>

&nbsp;
## [N-52] NatSpec `@title` missing

The `@title` tag is used to specify a title in order to make the contracts
purpose more clear.

<details>
<summary>Instances: 10</summary>

```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

16: contract CollSurplusPool is ICollSurplusPool, ReentrancyGuard, AuthNoOwner {

```
[L16](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L16)

```solidity
File: packages/contracts/contracts/EBTCToken.sol

26: contract EBTCToken is IEBTCToken, AuthNoOwner, PermitNonce {

```
[L26](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L26)

```solidity
File: packages/contracts/contracts/Governor.sol

13: contract Governor is RolesAuthority {

```
[L13](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L13)

```solidity
File: packages/contracts/contracts/PriceFeed.sol

21: contract PriceFeed is BaseMath, IPriceFeed, AuthNoOwner {

```
[L21](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L21)

```solidity
File: packages/contracts/contracts/SortedCdps.sol

51: contract SortedCdps is ISortedCdps {

```
[L51](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L51)

```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

9: abstract contract Auth {

```
[L9](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L9)

```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

10: contract AuthNoOwner {

```
[L10](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L10)

```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

16: contract EbtcBase is BaseMath, IEbtcBase {

```
[L16](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L16)

```solidity
File: packages/contracts/contracts/Dependencies/ReentrancyGuard.sol

7: abstract contract ReentrancyGuard {

```
[L7](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ReentrancyGuard.sol#L7)

```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

12: contract RolesAuthority is IRolesAuthority, Auth, Authority {

```
[L12](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L12)

</details>

&nbsp;
## [N-53] Non-external function names should begin with an underscore

According to the
[Solidity Style Guide](https://docs.soliditylang.org/en/latest/style-guide.html#underscore-prefix-for-non-external-functions-and-variables),
non-external function names should begin with an underscore.

<details>
<summary>Instances: 4</summary>

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

498:     function excessivelySafeCall(
499:         address _target,
500:         uint256 _gas,
501:         uint256 _value,
502:         uint16 _maxCopy,
503:         bytes memory _calldata
504:     ) internal returns (bool, bytes memory) {

```
[L498](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L498)

```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

32:     function isAuthorized(address user, bytes4 functionSig) internal view virtual returns (bool) {

```
[L32](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L32)

```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

30:     function isAuthorized(address user, bytes4 functionSig) internal view virtual returns (bool) {

```
[L30](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L30)

```solidity
File: packages/contracts/contracts/Dependencies/EbtcMath.sol

35:     function decMul(uint256 x, uint256 y) internal pure returns (uint256 decProd) {

```
[L35](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L35)

</details>

&nbsp;
## [N-54] Non-external variable names should begin with an underscore

According to the
[Solidity Style Guide](https://docs.soliditylang.org/en/latest/style-guide.html#underscore-prefix-for-non-external-functions-and-variables),
non-external variable names should begin with an underscore.

<details>
<summary>Instances: 17</summary>

```solidity
File: packages/contracts/contracts/ActivePool.sol

31:     uint256 internal systemCollShares; // deposited collateral tracker

32:     uint256 internal systemDebt;

33:     uint256 internal feeRecipientCollShares; // coll shares claimable by fee recipient

```
[L31](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L31), [L32](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L32), [L33](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L33)

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

128:     ICollSurplusPool immutable collSurplusPool;

152:     uint256 internal immutable deploymentStartTime;

```
[L128](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L128), [L152](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L152)

```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

28:     uint256 internal totalSurplusCollShares;

```
[L28](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L28)

```solidity
File: packages/contracts/contracts/Governor.sol

17:     bytes32 NO_ROLES = bytes32(0);

```
[L17](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L17)

```solidity
File: packages/contracts/contracts/SortedCdps.sol

60:     uint256 constant ADDRESS_SHIFT = 96; // 8 * 12; Puts the address at leftmost bytes32 position

61:     uint256 constant BLOCK_SHIFT = 64; // 8 * 8; Puts the block value after the address

```
[L60](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L60), [L61](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L61)

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

35:     bool internal immutable willSweep;

37:     bytes32 constant FLASH_LOAN_SUCCESS = keccak256("ERC3156FlashBorrower.onFlashLoan");

```
[L35](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L35), [L37](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L37)

```solidity
File: packages/contracts/contracts/LeverageMacroReference.sol

12:     address internal immutable theOwner;

```
[L12](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L12)

```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

39:     bytes32 constant DIAMOND_STORAGE_POSITION = keccak256("diamond.standard.diamond.storage");

```
[L39](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L39)

```solidity
File: packages/contracts/contracts/Dependencies/EbtcMath.sol

6:     uint256 internal constant DECIMAL_PRECISION = 1e18;

18:     uint256 internal constant NICR_PRECISION = 1e20;

```
[L6](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L6), [L18](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L18)

```solidity
File: packages/contracts/contracts/Dependencies/ReentrancyGuard.sol

8:     uint256 internal constant OPEN = 1;

9:     uint256 internal constant LOCKED = 2;

```
[L8](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ReentrancyGuard.sol#L8), [L9](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ReentrancyGuard.sol#L9)

</details>

&nbsp;
## [N-55] Consider adding emergency pause functionality

Implementing a system-wide pause mechanism makes in-progress hack mitigation
faster and less stressful. Inheriting OpenZeppelin's
[Pausable](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/security/Pausable.sol)
contract is a simple and safe way to do this. The following contracts all
handle ether/token transfers.

<details>
<summary>Instances: 3</summary>

```solidity
File: packages/contracts/contracts/ActivePool.sol

22: contract ActivePool is IActivePool, ERC3156FlashLender, ReentrancyGuard, BaseMath, AuthNoOwner {

```
[L22](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L22)

```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

16: contract CollSurplusPool is ICollSurplusPool, ReentrancyGuard, AuthNoOwner {

```
[L16](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L16)

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

26: contract LeverageMacroBase {

```
[L26](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L26)

</details>

&nbsp;
## [N-56] Execution at deadlines should be allowed

The equality condition must be considered to prevent unexpected behaviour.
Consider replacing `<` with `<=` or `>` with `>=`.

<details>
<summary>Instances: 19</summary>

```solidity
File: packages/contracts/contracts/ActivePool.sol

267:         require(amount > 0, "ActivePool: 0 Amount");

```
[L267](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L267)

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

463:         require(vars.netStEthBalance > 0, "BorrowerOperations: zero collateral for openCdp()!");

835:         require(_debtChange > 0, "BorrowerOperations: Debt increase requires non-zero debtChange");

936:         require(_debt > 0, "BorrowerOperations: Debt must be non-zero");

1083:         require(amount > 0, "BorrowerOperations: 0 Amount");

```
[L463](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L463), [L835](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L835), [L936](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L936), [L1083](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1083)

```solidity
File: packages/contracts/contracts/CdpManager.sol

431:         require(totals.collSharesDrawn > 0, "CdpManager: Unable to redeem any amount");

626:         require(newBaseRate > 0, "CdpManager: new baseRate is zero!"); // Base rate is always non-zero after redemption

754:         require(_amount > 0, "CdpManager: Amount must be greater than zero");

```
[L431](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L431), [L626](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L626), [L754](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L754)

```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

93:             require(
94:                 block.timestamp >
95:                     cachedLastGracePeriodStartTimestamp + recoveryModeGracePeriodDuration,
96:                 "LiquidationLibrary: Recovery mode grace period still in effect"
97:             );

710:         require(totals.totalDebtInSequence > 0, "LiquidationLibrary: nothing to liquidate");

```
[L93](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L93), [L710](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L710)

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

453:             require(totalStakesSnapshot > 0, "CdpManagerStorage: zero totalStakesSnapshot!");

556:         require(_newIndex > _prevIndex, "CDPManager: only take fee with bigger new index");

584:         require(activePool.getSystemCollShares() > _feeTaken, "CDPManager: fee split is too big");

653:         require(
654:             CdpOwnersArrayLength > 1 && sortedCdps.getSize() > 1,
655:             "CdpManager: Only one cdp in the system"
656:         );

```
[L453](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L453), [L556](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L556), [L584](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L584), [L653](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L653)

```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

92:         require(claimableColl > 0, "CollSurplusPool: No collateral available to claim");

```
[L92](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L92)

```solidity
File: packages/contracts/contracts/SortedCdps.sol

371:         require(_NICR > 0, "SortedCdps: NICR must be positive");

422:         require(_len > 1, "SortedCdps: batchRemove() only apply to multiple cdpIds!");

508:         require(_newNICR > 0, "SortedCdps: NICR must be positive");

```
[L371](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L371), [L422](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L422), [L508](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L508)

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

440:                 require(
441:                     IERC20(swapChecks[i].tokenToCheck).balanceOf(address(this)) >
442:                         swapChecks[i].expectedMinOut,
443:                     "LeverageMacroReference: swap check failure!"
444:                 );

```
[L440](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L440)

</details>

&nbsp;
## [N-57] Avoid overly complicated arithmetic

To maintain readability in code, particularly in Solidity which can involve
complex mathematical operations, it is often recommended to limit the number
of arithmetic operations to a maximum of 2-3 per line. Too many operations
in a single line can make the code difficult to read and understand, increase
the likelihood of mistakes, and complicate the process of debugging and
reviewing the code. Consider splitting such operations over more than one
line, take special care when dealing with division however.

<details>
<summary>Instances: 1</summary>

```solidity
File: packages/contracts/contracts/PriceFeed.sol

800:         return
801:             (_scaledDecimal *
802:                 uint256(_ethBtcAnswer) *
803:                 uint256(_stEthEthAnswer) *
804:                 EbtcMath.DECIMAL_PRECISION) / 10 ** (_decimalDenominator * 2);

```
[L800](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L800)

</details>

&nbsp;
## [N-58] Use existing `Ownable` implementation

It is recommended to use either
[OpenZeppelin's](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/access/Ownable.sol)
or [Solady's](https://github.com/Vectorized/solady/blob/main/src/auth/Ownable.sol)
Ownable implementation as both have been optimized and are usage-hardened,
so writing your own is both unnecessary and needlessly risky.

<details>
<summary>Instances: 1</summary>

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

13: import "./Dependencies/Ownable.sol";

```
[L13](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L13)

</details>

&nbsp;
## [N-59] Function parameters should be named using mixedCase

Underscore before of after function argument names is a common convention in
Solidity NOT a documentation requirement.

Function arguments should use mixedCase for better readability and consistency
with Solidity style guidelines. For example: initialSupply,
account, recipientAddress, senderAddress, newOwner. More information in
[documentation](https://docs.soliditylang.org/en/v0.8.20/style-guide.html#function-argument-names).

<details>
<summary>Instances: 1</summary>

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

652:     function _requireMoreThanOneCdpInSystem(uint256 CdpOwnersArrayLength) internal view {

```
[L652](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L652)

</details>

&nbsp;
## [N-60] Avoid polymorphic functions

The instances below point to one of two functions with the same name.
Polymorphic functions make security audits more time-consuming and
error-prone. Consider naming each function differently, in order to
make code navigation and analysis easier.

<details>
<summary>Instances: 6</summary>

```solidity
File: packages/contracts/contracts/EBTCToken.sol

95:     function burn(address _account, uint256 _amount) external override {

104:     function burn(uint256 _amount) external {

```
[L95](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L95), [L104](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L104)

```solidity
File: packages/contracts/contracts/LeverageMacroDelegateTarget.sol

7:     function owner() external view returns (address);

63:     function owner() public override returns (address) {

```
[L7](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L7), [L63](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L63)

```solidity
File: packages/contracts/contracts/LeverageMacroFactory.sol

38:     function deployNewMacro() external returns (address) {

43:     function deployNewMacro(address _owner) public returns (address) {

```
[L38](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L38), [L43](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L43)

</details>

&nbsp;
## [N-61] `public` functions not called internally should be declared `external`

Contracts
[are allowed](https://docs.soliditylang.org/en/latest/contracts.html#function-overriding)
to override their parents' functions and change the visibility from external to
public.

<details>
<summary>Instances: 28</summary>

```solidity
File: packages/contracts/contracts/ActivePool.sol

100:     function transferSystemCollShares(address _account, uint256 _shares) public override {

371:     function sweepToken(address token, uint256 amount) public nonReentrant requiresAuth {

```
[L100](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L100), [L371](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L371)

```solidity
File: packages/contracts/contracts/CdpManager.sol

717:     function getDeploymentStartTime() public view returns (uint256) {

```
[L717](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L717)

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

701:     function getCachedICR(bytes32 _cdpId, uint256 _price) public view returns (uint256) {

728:     function hasPendingRedistributedDebt(bytes32 _cdpId) public view returns (bool) {

864:     function getSyncedICR(bytes32 _cdpId, uint256 _price) public view returns (uint256) {

874:     function getSyncedTCR(uint256 _price) public view returns (uint256) {

890:     function canLiquidateRecoveryMode(uint256 icr, uint256 tcr) public view returns (bool) {

```
[L701](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L701), [L728](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L728), [L864](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L864), [L874](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L874), [L890](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L890)

```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

142:     function sweepToken(address token, uint256 amount) public nonReentrant requiresAuth {

```
[L142](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L142)

```solidity
File: packages/contracts/contracts/Governor.sol

96:     function getRolesFromByteMap(bytes32 byteMap) public pure returns (uint8[] memory roleIds) {

120:     function getByteMapFromRoles(uint8[] memory roleIds) public pure returns (bytes32) {

131:     function getEnabledFunctionsInTarget(
132:         address _target
133:     ) public view returns (bytes4[] memory _funcs) {

```
[L96](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L96), [L120](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L120), [L131](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L131)

```solidity
File: packages/contracts/contracts/SortedCdps.sol

130:     function nonExistId() public pure override returns (bytes32) {

```
[L130](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L130)

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

234:     function sweepToken(address token, uint256 amount) public {

```
[L234](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L234)

```solidity
File: packages/contracts/contracts/LeverageMacroReference.sol

44:     function owner() public override returns (address) {

```
[L44](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L44)

```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

42:     function setAuthority(Authority newAuthority) public virtual {

52:     function transferOwnership(address newOwner) public virtual requiresAuth {

```
[L42](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L42), [L52](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L52)

```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

22:     function authority() public view returns (Authority) {

26:     function authorityInitialized() public view returns (bool) {

38:     function setAuthority(address newAuthority) public virtual {

```
[L22](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L22), [L26](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L26), [L38](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L38)

```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

38:     function doesUserHaveRole(address user, uint8 role) public view virtual returns (bool) {

42:     function doesRoleHaveCapability(
43:         uint8 role,
44:         address target,
45:         bytes4 functionSig
46:     ) public view virtual returns (bool) {

50:     function isPublicCapability(address target, bytes4 functionSig) public view returns (bool) {

63:     function canCall(
64:         address user,
65:         address target,
66:         bytes4 functionSig
67:     ) public view virtual override returns (bool) {

85:     function setPublicCapability(
86:         address target,
87:         bytes4 functionSig,
88:         bool enabled
89:     ) public virtual requiresAuth {

106:     function setRoleCapability(
107:         uint8 role,
108:         address target,
109:         bytes4 functionSig,
110:         bool enabled
111:     ) public virtual requiresAuth {

133:     function burnCapability(address target, bytes4 functionSig) public virtual requiresAuth {

147:     function setUserRole(address user, uint8 role, bool enabled) public virtual requiresAuth {

```
[L38](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L38), [L42](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L42), [L50](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L50), [L63](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L63), [L85](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L85), [L106](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L106), [L133](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L133), [L147](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L147)

</details>

&nbsp;
## [N-62] `pure` function accesses storage

While the compiler currently flags functions like these as being pure, this is a
[bug](https://github.com/ethereum/solidity/issues/11573) which will be fixed in
a future version, so it's best to not use pure visibility, in order to not break
when this bug is fixed.

<details>
<summary>Instances: 1</summary>

```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

84:         bytes32 position = DIAMOND_STORAGE_POSITION;
85:         assembly {
86:             ds.slot := position
87:         }
88:     }

```
[L84](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L84)

</details>

&nbsp;
## [N-63] Use the latest Solidity version (<0.8.20 for L2s)

When deploying contracts, you should use the latest released version
of Solidity to make use of more newer features and security fixes.

<details>
<summary>Instances: 39</summary>

```solidity
File: packages/contracts/contracts/ActivePool.sol

3: pragma solidity 0.8.17;

```
[L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L3)

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

3: pragma solidity 0.8.17;

```
[L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L3)

```solidity
File: packages/contracts/contracts/CdpManager.sol

3: pragma solidity 0.8.17;

```
[L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L3)

```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

3: pragma solidity 0.8.17;

```
[L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L3)

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

3: pragma solidity 0.8.17;

```
[L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L3)

```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

3: pragma solidity 0.8.17;

```
[L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L3)

```solidity
File: packages/contracts/contracts/EBTCToken.sol

3: pragma solidity 0.8.17;

```
[L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L3)

```solidity
File: packages/contracts/contracts/Governor.sol

2: pragma solidity 0.8.17;

```
[L2](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L2)

```solidity
File: packages/contracts/contracts/PriceFeed.sol

3: pragma solidity 0.8.17;

```
[L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L3)

```solidity
File: packages/contracts/contracts/SortedCdps.sol

3: pragma solidity 0.8.17;

```
[L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L3)

```solidity
File: packages/contracts/contracts/HintHelpers.sol

3: pragma solidity 0.8.17;

```
[L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L3)

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

2: pragma solidity 0.8.17;

```
[L2](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L2)

```solidity
File: packages/contracts/contracts/LeverageMacroDelegateTarget.sol

2: pragma solidity 0.8.17;

```
[L2](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L2)

```solidity
File: packages/contracts/contracts/LeverageMacroFactory.sol

2: pragma solidity 0.8.17;

```
[L2](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L2)

```solidity
File: packages/contracts/contracts/LeverageMacroReference.sol

2: pragma solidity 0.8.17;

```
[L2](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L2)

```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

2: pragma solidity 0.8.17;

```
[L2](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L2)

```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

2: pragma solidity 0.8.17;

```
[L2](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L2)

```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

2: pragma solidity 0.8.17;

```
[L2](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L2)

```solidity
File: packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol

3: pragma solidity 0.8.17;

```
[L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L3)

```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

3: pragma solidity 0.8.17;

```
[L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L3)

```solidity
File: packages/contracts/contracts/Dependencies/EbtcMath.sol

3: pragma solidity 0.8.17;

```
[L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L3)

```solidity
File: packages/contracts/contracts/Dependencies/ReentrancyGuard.sol

2: pragma solidity 0.8.17;

```
[L2](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ReentrancyGuard.sol#L2)

```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

2: pragma solidity 0.8.17;

```
[L2](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L2)

```solidity
File: packages/contracts/contracts/Interfaces/IActivePool.sol

3: pragma solidity 0.8.17;

```
[L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IActivePool.sol#L3)

```solidity
File: packages/contracts/contracts/Interfaces/IBorrowerOperations.sol

3: pragma solidity 0.8.17;

```
[L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L3)

```solidity
File: packages/contracts/contracts/Interfaces/ICdpManager.sol

3: pragma solidity 0.8.17;

```
[L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol#L3)

```solidity
File: packages/contracts/contracts/Interfaces/ICdpManagerData.sol

3: pragma solidity 0.8.17;

```
[L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L3)

```solidity
File: packages/contracts/contracts/Interfaces/ICollSurplusPool.sol

3: pragma solidity 0.8.17;

```
[L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICollSurplusPool.sol#L3)

```solidity
File: packages/contracts/contracts/Interfaces/IEbtcBase.sol

3: pragma solidity 0.8.17;

```
[L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IEbtcBase.sol#L3)

```solidity
File: packages/contracts/contracts/Interfaces/IEBTCToken.sol

3: pragma solidity 0.8.17;

```
[L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IEBTCToken.sol#L3)

```solidity
File: packages/contracts/contracts/Interfaces/IERC3156FlashBorrower.sol

3: pragma solidity 0.8.17;

```
[L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IERC3156FlashBorrower.sol#L3)

```solidity
File: packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol

3: pragma solidity 0.8.17;

```
[L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol#L3)

```solidity
File: packages/contracts/contracts/Interfaces/IFallbackCaller.sol

3: pragma solidity 0.8.17;

```
[L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IFallbackCaller.sol#L3)

```solidity
File: packages/contracts/contracts/Interfaces/IPermitNonce.sol

3: pragma solidity 0.8.17;

```
[L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPermitNonce.sol#L3)

```solidity
File: packages/contracts/contracts/Interfaces/IPool.sol

3: pragma solidity 0.8.17;

```
[L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPool.sol#L3)

```solidity
File: packages/contracts/contracts/Interfaces/IPositionManagers.sol

3: pragma solidity 0.8.17;

```
[L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPositionManagers.sol#L3)

```solidity
File: packages/contracts/contracts/Interfaces/IPriceFeed.sol

3: pragma solidity 0.8.17;

```
[L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPriceFeed.sol#L3)

```solidity
File: packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol

2: pragma solidity 0.8.17;

```
[L2](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol#L2)

```solidity
File: packages/contracts/contracts/Interfaces/ISortedCdps.sol

3: pragma solidity 0.8.17;

```
[L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L3)

</details>

&nbsp;
## [N-64] Redundant boolean literal comparison

Write `<x>` instead of `<x> == true`, and `!<x>` instead of `<x> == false`.

<details>
<summary>Instances: 1</summary>

```solidity
File: packages/contracts/contracts/CdpManager.sol

332:         require(redemptionsPaused == false, "CdpManager: Redemptions Paused");

```
[L332](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L332)

</details>

&nbsp;
## [N-65] Redundant getter functions

Implementing a getter function on a `public` variable is redundant. Consider
changing the variables visibility or removing the function altogether.

<details>
<summary>Instances: 1</summary>

```solidity
File: packages/contracts/contracts/SortedCdps.sol

548:     function getMaxSize() external view override returns (uint256) {
549:         return maxSize;
550:     }

```
[L548](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L548)

</details>

&nbsp;
## [N-66] Adding a `return` statement when the function defines a named return variable is redundant

Consider changing the variable to an unnamed one, or removing the `return`
statement.

<details>
<summary>Instances: 13</summary>

```solidity
File: packages/contracts/contracts/CdpManager.sol

135:     function _redeemCollateralFromCdp(
136:         SingleRedemptionInputs memory _redeemColFromCdp
137:     ) internal returns (SingleRedemptionValues memory singleRedemption) {

206:                 return singleRedemption;

233:         return singleRedemption;

550:     function _addCdpIdToArray(bytes32 _cdpId) internal returns (uint128 index) {

562:         return index;

570:     function getSystemDebt() public view returns (uint256 entireSystemDebt) {
571:         return _getSystemDebt();

```
[L135](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L135), [L206](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L206), [L233](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L233), [L550](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L550), [L562](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L562), [L570](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L570)

```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

839:     function _addLiquidationValuesToTotals(
840:         LiquidationTotals memory oldTotals,
841:         LiquidationValues memory singleLiquidation
842:     ) internal pure returns (LiquidationTotals memory newTotals) {

859:         return newTotals;

```
[L839](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L839), [L859](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L859)

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

304:     function _getPendingRedistributedDebt(
305:         bytes32 _cdpId
306:     ) internal view returns (uint256 pendingEBTCDebtReward, uint256 _debtIndexDiff) {

310:             return (0, 0);

318:             return (0, 0);

719:     function getPendingRedistributedDebt(
720:         bytes32 _cdpId
721:     ) public view returns (uint256 pendingEBTCDebtReward) {

723:         return _pendingDebt;

```
[L304](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L304), [L310](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L310), [L318](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L318), [L719](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L719), [L723](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L723)

```solidity
File: packages/contracts/contracts/Governor.sol

146:     function getRoleName(uint8 role) external view returns (string memory roleName) {
147:         return roleNames[role];

```
[L146](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L146)

```solidity
File: packages/contracts/contracts/PriceFeed.sol

606:     function _getCurrentChainlinkResponse()
607:         internal
608:         view
609:         returns (ChainlinkResponse memory chainlinkResponse)
610:     {

620:             return chainlinkResponse;

628:             return chainlinkResponse;

647:             return chainlinkResponse;

663:             return chainlinkResponse;

677:             return chainlinkResponse;

687:     function _getPrevChainlinkResponse(
688:         uint80 _currentRoundEthBtcId,
689:         uint80 _currentRoundStEthEthId
690:     ) internal view returns (ChainlinkResponse memory prevChainlinkResponse) {

696:             return prevChainlinkResponse;

708:             return prevChainlinkResponse;

716:             return prevChainlinkResponse;

735:             return prevChainlinkResponse;

751:             return prevChainlinkResponse;

765:             return prevChainlinkResponse;

```
[L606](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L606), [L620](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L620), [L628](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L628), [L647](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L647), [L663](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L663), [L677](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L677), [L687](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L687), [L696](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L696), [L708](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L708), [L716](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L716), [L735](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L735), [L751](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L751), [L765](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L765)

```solidity
File: packages/contracts/contracts/HintHelpers.sol

164:     function getApproxHint(
165:         uint256 _CR,
166:         uint256 _numTrials,
167:         uint256 _inputRandomSeed
168:     ) external view returns (bytes32 hint, uint256 diff, uint256 latestRandomSeed) {

172:             return (sortedCdps.nonExistId(), 0, _inputRandomSeed);

```
[L164](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L164), [L172](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L172)

```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

67:     function getSystemCollShares() public view returns (uint256 entireSystemColl) {
68:         return (activePool.getSystemCollShares());

75:     function _getSystemDebt() internal view returns (uint256 entireSystemDebt) {
76:         return (activePool.getSystemDebt());

83:     function _getTCRWithSystemDebtAndCollShares(
84:         uint256 _price
85:     ) internal view returns (uint256 TCR, uint256 _coll, uint256 _debt) {

92:         return (TCR, systemCollShares, systemDebt);

```
[L67](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L67), [L75](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L75), [L83](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L83), [L92](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L92)

</details>

&nbsp;
## [N-67] Use descriptive reason strings for `require`/`revert`

Providing descriptive error strings is important to help user understand why
their transaction might have reverted, and also aids debugging.

<details>
<summary>Instances: 12</summary>

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

452:         require(addy != address(borrowerOperations));
453:         require(addy != address(sortedCdps));
454:         require(addy != address(activePool));
455:         require(addy != address(cdpManager));
456:         require(addy != address(this)); // If it could call this it could fake the forwarded caller

```
[L452](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L452)

```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

52:         require(msg.sender == owner);

56:         require(sig != 0x94b24d09);

67:         require(msg.sender == owner);

77:         require(msg.sender == address(this)); // Must call this via `execute` to explicitly set the flag

154:             require(success);

```
[L52](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L52), [L56](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L56), [L67](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L67), [L77](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L77), [L154](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L154)

```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

45:         require(msg.sender == owner || authority.canCall(msg.sender, address(this), msg.sig));

```
[L45](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L45)

```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

41:         require(_authority.canCall(msg.sender, address(this), msg.sig));

```
[L41](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L41)

</details>

&nbsp;
## [N-68] Use a `struct` instead of returning multiple values

Functions that return many variables can become difficult to read and maintain.
Using a struct to encapsulate these return values can improve code readability,
increase reusability, and reduce the likelihood of errors. Consider refactoring
functions that return more than three variables to use a struct instead.

<details>
<summary>Instances: 39</summary>

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

744:     function _getCollSharesChangeFromStEthChange(
745:         uint256 _collReceived,
746:         uint256 _requestedCollWithdrawal
747:     ) internal view returns (uint256 collSharesChange, bool isCollIncrease) {

1030:     function _getNewCdpAmounts(
1031:         uint256 _collShares,
1032:         uint256 _debt,
1033:         uint256 _collSharesChange,
1034:         bool _isCollIncrease,
1035:         uint256 _debtChange,
1036:         bool _isDebtIncrease
1037:     ) internal pure returns (uint256, uint256) {

```
[L744](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L744), [L1030](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1030)

```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

186:     function _liquidateCdpInGivenMode(
187:         LiquidationLocals memory _liqState,
188:         LiquidationRecoveryModeLocals memory _recoveryState
189:     ) private returns (uint256, uint256, uint256, uint256, uint256) {

384:     function _closeCdpByLiquidation(bytes32 _cdpId) private returns (uint256, uint256, uint256) {

397:     function _liquidateCDPPartially(
398:         LiquidationLocals memory _partialState
399:     ) private returns (uint256, uint256) {

544:     function _calculatePartialLiquidationSurplusAndCap(
545:         uint256 _ICR,
546:         uint256 _price,
547:         uint256 _totalDebtToBurn,
548:         uint256 _totalColToSend
549:     ) private view returns (uint256 toLiquidator, uint256 collSurplus, uint256 debtToRedistribute) {

570:     function _calculateFullLiquidationSurplusAndCap(
571:         uint256 _ICR,
572:         uint256 _price,
573:         uint256 _totalDebtToBurn,
574:         uint256 _totalColToSend
575:     ) private view returns (uint256 toLiquidator, uint256 collSurplus, uint256 debtToRedistribute) {

```
[L186](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L186), [L384](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L384), [L397](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L397), [L544](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L544), [L570](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L570)

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

304:     function _getPendingRedistributedDebt(
305:         bytes32 _cdpId
306:     ) internal view returns (uint256 pendingEBTCDebtReward, uint256 _debtIndexDiff) {

431:     function _updateStakeForCdp(bytes32 _cdpId) internal returns (uint256, uint256) {

534:     function _readStEthIndex() internal view returns (uint256, uint256) {

552:     function calcFeeUponStakingReward(
553:         uint256 _newIndex,
554:         uint256 _prevIndex
555:     ) public view returns (uint256, uint256, uint256) {

616:     function getAccumulatedFeeSplitApplied(
617:         bytes32 _cdpId,
618:         uint256 _systemStEthFeePerUnitIndex
619:     ) public view returns (uint256, uint256) {

745:     function getSyncedDebtAndCollShares(
746:         bytes32 _cdpId
747:     ) public view returns (uint256 debt, uint256 coll) {

761:     function _calcSyncedGlobalAccounting(
762:         uint256 _newIndex,
763:         uint256 _oldIndex
764:     ) internal view returns (uint256, uint256, uint256) {

787:     function _calcSyncedAccounting(
788:         bytes32 _cdpId,
789:         uint256 _cdpPerUnitIdx,
790:         uint256 _systemStEthFeePerUnitIndex
791:     ) internal view returns (uint256, uint256, uint256, uint256, uint256) {

822:     function _getSyncedCdpDebtAndRedistribution(
823:         bytes32 _cdpId
824:     ) internal view returns (uint256, uint256, uint256) {

```
[L304](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L304), [L431](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L431), [L534](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L534), [L552](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L552), [L616](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L616), [L745](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L745), [L761](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L761), [L787](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L787), [L822](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L822)

```solidity
File: packages/contracts/contracts/SortedCdps.sol

155:     function cdpOfOwnerByIdx(
156:         address owner,
157:         uint256 index,
158:         bytes32 startNodeId,
159:         uint maxNodes
160:     ) external view override returns (bytes32, bool) {

173:     function _cdpOfOwnerByIndex(
174:         address owner,
175:         uint256 index,
176:         bytes32 startNodeId,
177:         uint maxNodes
178:     ) internal view returns (bytes32, bool) {

227:     function getCdpCountOf(
228:         address owner,
229:         bytes32 startNodeId,
230:         uint maxNodes
231:     ) external view override returns (uint256, bytes32) {

237:     function _cdpCountOf(
238:         address owner,
239:         bytes32 startNodeId,
240:         uint maxNodes
241:     ) internal view returns (uint256, bytes32) {

286:     function getAllCdpsOf(
287:         address owner,
288:         bytes32 startNodeId,
289:         uint maxNodes
290:     ) external view override returns (bytes32[] memory, uint256, bytes32) {

299:     function _getCdpsOf(
300:         address owner,
301:         bytes32 startNodeId,
302:         uint maxNodes,
303:         uint maxArraySize
304:     ) internal view returns (bytes32[] memory, uint256, bytes32) {

619:     function _descendList(uint256 _NICR, bytes32 _startId) internal view returns (bytes32, bytes32) {

642:     function _ascendList(uint256 _NICR, bytes32 _startId) internal view returns (bytes32, bytes32) {

666:     function findInsertPosition(
667:         uint256 _NICR,
668:         bytes32 _prevId,
669:         bytes32 _nextId
670:     ) external view override returns (bytes32, bytes32) {

674:     function _findInsertPosition(
675:         uint256 _NICR,
676:         bytes32 _prevId,
677:         bytes32 _nextId
678:     ) internal view returns (bytes32, bytes32) {

```
[L155](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L155), [L173](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L173), [L227](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L227), [L237](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L237), [L286](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L286), [L299](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L299), [L619](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L619), [L642](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L642), [L666](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L666), [L674](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L674)

```solidity
File: packages/contracts/contracts/HintHelpers.sol

48:     function getRedemptionHints(
49:         uint256 _EBTCamount,
50:         uint256 _price,
51:         uint256 _maxIterations
52:     )
53:         external
54:         view
55:         returns (
56:             bytes32 firstRedemptionHint,
57:             uint256 partialRedemptionHintNICR,
58:             uint256 truncatedEBTCamount,
59:             uint256 partialRedemptionNewColl
60:         )
61:     {

133:     function _calculateCdpStateAfterPartialRedemption(
134:         LocalVariables_getRedemptionHints memory vars,
135:         uint256 currentCdpDebt,
136:         uint256 _price
137:     ) internal view returns (uint256, uint256) {

164:     function getApproxHint(
165:         uint256 _CR,
166:         uint256 _numTrials,
167:         uint256 _inputRandomSeed
168:     ) external view returns (bytes32 hint, uint256 diff, uint256 latestRandomSeed) {

```
[L48](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L48), [L133](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L133), [L164](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L164)

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

498:     function excessivelySafeCall(
499:         address _target,
500:         uint256 _gas,
501:         uint256 _value,
502:         uint16 _maxCopy,
503:         bytes memory _calldata
504:     ) internal returns (bool, bytes memory) {

```
[L498](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L498)

```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

83:     function _getTCRWithSystemDebtAndCollShares(
84:         uint256 _price
85:     ) internal view returns (uint256 TCR, uint256 _coll, uint256 _debt) {

```
[L83](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L83)

```solidity
File: packages/contracts/contracts/Interfaces/ICdpManagerData.sol

227:     function calcFeeUponStakingReward(
228:         uint256 _newIndex,
229:         uint256 _prevIndex
230:     ) external view returns (uint256, uint256, uint256);

236:     function getAccumulatedFeeSplitApplied(
237:         bytes32 _cdpId,
238:         uint256 _systemStEthFeePerUnitIndex
239:     ) external view returns (uint256, uint256);

259:     function getSyncedDebtAndCollShares(
260:         bytes32 _cdpId
261:     ) external view returns (uint256 debt, uint256 collShares);

```
[L227](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L227), [L236](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L236), [L259](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L259)

```solidity
File: packages/contracts/contracts/Interfaces/IFallbackCaller.sol

13:     function getFallbackResponse() external view returns (uint256, uint256, bool);

```
[L13](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IFallbackCaller.sol#L13)

```solidity
File: packages/contracts/contracts/Interfaces/ISortedCdps.sol

44:     function findInsertPosition(
45:         uint256 _ICR,
46:         bytes32 _prevId,
47:         bytes32 _nextId
48:     ) external view returns (bytes32, bytes32);

63:     function getCdpCountOf(
64:         address owner,
65:         bytes32 startNodeId,
66:         uint maxNodes
67:     ) external view returns (uint256, bytes32);

71:     function getAllCdpsOf(
72:         address owner,
73:         bytes32 startNodeId,
74:         uint maxNodes
75:     ) external view returns (bytes32[] memory, uint256, bytes32);

79:     function cdpOfOwnerByIdx(
80:         address owner,
81:         uint256 index,
82:         bytes32 startNodeId,
83:         uint maxNodes
84:     ) external view returns (bytes32, bool);

```
[L44](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L44), [L63](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L63), [L71](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L71), [L79](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L79)

</details>

&nbsp;
## [N-69] Use scientific notation/underscores for large values

e.g. `1e6` or `1_000_000` instead of `1000000`.

<details>
<summary>Instances: 3</summary>

```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

19:     uint256 public constant LICR = 1030000000000000000; // 103%

22:     uint256 public constant MCR = 1100000000000000000; // 110%

25:     uint256 public constant CCR = 1250000000000000000; // 125%

```
[L19](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L19), [L22](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L22), [L25](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L25)

</details>

&nbsp;
## [N-70] Events regarding variable changes should emit both old and new values

Change the event to emit both the old and new value to supply those monitoring
the event with full information.

<details>
<summary>Instances: 8</summary>

```solidity
File: packages/contracts/contracts/ActivePool.sol

399:         emit FeeRecipientAddressChanged(_feeRecipientAddress);

```
[L399](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L399)

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

1149:         emit FeeRecipientAddressChanged(_feeRecipientAddress);

```
[L1149](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1149)

```solidity
File: packages/contracts/contracts/CdpManager.sol

782:         emit StakingRewardSplitSet(_stakingRewardSplit);

801:         emit RedemptionFeeFloorSet(_redemptionFeeFloor);

824:         emit MinuteDecayFactorSet(_minuteDecayFactor);

836:         emit BetaSet(_beta);

848:         emit RedemptionsPaused(_paused);

```
[L782](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L782), [L801](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L801), [L824](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L824), [L836](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L836), [L848](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L848)

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

119:         emit GracePeriodDurationSet(_gracePeriod);

```
[L119](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L119)

</details>

&nbsp;
## [N-71] Setter does not check that value is changed

In setter functions, consider adding a check for whether the new value is
equal to the old value.

<details>
<summary>Instances: 17</summary>

```solidity
File: packages/contracts/contracts/ActivePool.sol

390:     function setFeeRecipientAddress(address _feeRecipientAddress) external requiresAuth {
391:         ICdpManagerData(cdpManagerAddress).syncGlobalAccountingAndGracePeriod(); // Accrue State First

393:         require(
394:             _feeRecipientAddress != address(0),
395:             "ActivePool: Cannot set fee recipient to zero address"
396:         );

398:         feeRecipientAddress = _feeRecipientAddress;
399:         emit FeeRecipientAddressChanged(_feeRecipientAddress);
400:     }

404:     function setFeeBps(uint256 _newFee) external requiresAuth {
405:         ICdpManagerData(cdpManagerAddress).syncGlobalAccountingAndGracePeriod(); // Accrue State First

407:         require(_newFee <= MAX_FEE_BPS, "ERC3156FlashLender: _newFee should <= MAX_FEE_BPS");

409:         // set new flash fee
410:         uint256 _oldFee = feeBps;
411:         feeBps = uint16(_newFee);
412:         emit FlashFeeSet(msg.sender, _oldFee, _newFee);
413:     }

417:     function setFlashLoansPaused(bool _paused) external requiresAuth {
418:         ICdpManagerData(cdpManagerAddress).syncGlobalAccountingAndGracePeriod(); // Accrue State First

420:         flashLoansPaused = _paused;
421:         emit FlashLoansPaused(msg.sender, _paused);
422:     }

```
[L390](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L390), [L393](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L393), [L398](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L398), [L404](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L404), [L407](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L407), [L409](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L409), [L417](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L417), [L420](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L420)

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

1140:     function setFeeRecipientAddress(address _feeRecipientAddress) external requiresAuth {
1141:         require(
1142:             _feeRecipientAddress != address(0),
1143:             "BorrowerOperations: Cannot set feeRecipient to zero address"
1144:         );

1146:         cdpManager.syncGlobalAccounting();

1148:         feeRecipientAddress = _feeRecipientAddress;
1149:         emit FeeRecipientAddressChanged(_feeRecipientAddress);
1150:     }

1154:     function setFeeBps(uint256 _newFee) external requiresAuth {
1155:         require(_newFee <= MAX_FEE_BPS, "ERC3156FlashLender: _newFee should <= MAX_FEE_BPS");

1157:         cdpManager.syncGlobalAccounting();

1159:         // set new flash fee
1160:         uint256 _oldFee = feeBps;
1161:         feeBps = uint16(_newFee);
1162:         emit FlashFeeSet(msg.sender, _oldFee, _newFee);
1163:     }

1167:     function setFlashLoansPaused(bool _paused) external requiresAuth {
1168:         cdpManager.syncGlobalAccounting();

1170:         flashLoansPaused = _paused;
1171:         emit FlashLoansPaused(msg.sender, _paused);
1172:     }

```
[L1140](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1140), [L1146](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1146), [L1148](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1148), [L1154](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1154), [L1157](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1157), [L1159](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1159), [L1167](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1167), [L1170](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1170)

```solidity
File: packages/contracts/contracts/CdpManager.sol

773:     function setStakingRewardSplit(uint256 _stakingRewardSplit) external requiresAuth {
774:         require(
775:             _stakingRewardSplit <= MAX_REWARD_SPLIT,
776:             "CDPManager: new staking reward split exceeds max"
777:         );

779:         syncGlobalAccountingAndGracePeriod();

781:         stakingRewardSplit = _stakingRewardSplit;
782:         emit StakingRewardSplitSet(_stakingRewardSplit);
783:     }

788:     function setRedemptionFeeFloor(uint256 _redemptionFeeFloor) external requiresAuth {
789:         require(
790:             _redemptionFeeFloor >= MIN_REDEMPTION_FEE_FLOOR,
791:             "CDPManager: new redemption fee floor is lower than minimum"
792:         );
793:         require(
794:             _redemptionFeeFloor <= DECIMAL_PRECISION,
795:             "CDPManager: new redemption fee floor is higher than maximum"
796:         );

798:         syncGlobalAccountingAndGracePeriod();

800:         redemptionFeeFloor = _redemptionFeeFloor;
801:         emit RedemptionFeeFloorSet(_redemptionFeeFloor);
802:     }

807:     function setMinuteDecayFactor(uint256 _minuteDecayFactor) external requiresAuth {
808:         require(
809:             _minuteDecayFactor >= MIN_MINUTE_DECAY_FACTOR,
810:             "CDPManager: new minute decay factor out of range"
811:         );
812:         require(
813:             _minuteDecayFactor <= MAX_MINUTE_DECAY_FACTOR,
814:             "CDPManager: new minute decay factor out of range"
815:         );

817:         syncGlobalAccountingAndGracePeriod();

819:         // decay first according to previous factor
820:         _decayBaseRate();

822:         // set new factor after decaying
823:         minuteDecayFactor = _minuteDecayFactor;
824:         emit MinuteDecayFactorSet(_minuteDecayFactor);
825:     }

830:     function setBeta(uint256 _beta) external requiresAuth {
831:         syncGlobalAccountingAndGracePeriod();

833:         _decayBaseRate();

835:         beta = _beta;
836:         emit BetaSet(_beta);
837:     }

843:     function setRedemptionsPaused(bool _paused) external requiresAuth {
844:         syncGlobalAccountingAndGracePeriod();
845:         _decayBaseRate();

847:         redemptionsPaused = _paused;
848:         emit RedemptionsPaused(_paused);
849:     }

```
[L773](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L773), [L779](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L779), [L781](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L781), [L788](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L788), [L798](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L798), [L800](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L800), [L807](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L807), [L817](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L817), [L819](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L819), [L822](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L822), [L830](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L830), [L833](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L833), [L835](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L835), [L843](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L843), [L847](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L847)

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

111:     function setGracePeriod(uint128 _gracePeriod) external requiresAuth {
112:         require(
113:             _gracePeriod >= MINIMUM_GRACE_PERIOD,
114:             "CdpManager: Grace period below minimum duration"
115:         );

117:         syncGlobalAccountingAndGracePeriod();
118:         recoveryModeGracePeriodDuration = _gracePeriod;
119:         emit GracePeriodDurationSet(_gracePeriod);
120:     }

```
[L111](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L111), [L117](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L117)

```solidity
File: packages/contracts/contracts/Governor.sol

154:     function setRoleName(uint8 role, string memory roleName) external requiresAuth {
155:         roleNames[role] = roleName;

157:         emit RoleNameSet(role, roleName);
158:     }

```
[L154](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L154), [L157](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L157)

```solidity
File: packages/contracts/contracts/PriceFeed.sol

358:     function setFallbackCaller(address _fallbackCaller) external requiresAuth {
359:         // health check-up before officially set it up
360:         IFallbackCaller newFallbackCaler = IFallbackCaller(_fallbackCaller);
361:         FallbackResponse memory fallbackResponse;

363:         if (_fallbackCaller != address(0)) {
364:             try newFallbackCaler.getFallbackResponse() returns (
365:                 uint256 answer,
366:                 uint256 timestampRetrieved,
367:                 bool success
368:             ) {
369:                 fallbackResponse.answer = answer;
370:                 fallbackResponse.timestamp = timestampRetrieved;
371:                 fallbackResponse.success = success;
372:                 if (
373:                     !_fallbackIsBroken(fallbackResponse) &&
374:                     !_responseTimeout(fallbackResponse.timestamp, newFallbackCaler.fallbackTimeout())
375:                 ) {
376:                     address oldFallbackCaller = address(fallbackCaller);
377:                     fallbackCaller = newFallbackCaler;
378:                     emit FallbackCallerChanged(oldFallbackCaller, _fallbackCaller);
379:                 }
380:             } catch {
381:                 emit UnhealthyFallbackCaller(_fallbackCaller, block.timestamp);
382:             }
383:         } else {
384:             address oldFallbackCaller = address(fallbackCaller);
385:             // NOTE: assume intentionally bricking fallback!!!
386:             fallbackCaller = newFallbackCaler;
387:             emit FallbackCallerChanged(oldFallbackCaller, _fallbackCaller);
388:         }
389:     }

```
[L358](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L358), [L363](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L363)

```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

42:     function setAuthority(Authority newAuthority) public virtual {
43:         // We check if the caller is the owner first because we want to ensure they can
44:         // always swap out the authority even if it's reverting or using up a lot of gas.
45:         require(msg.sender == owner || authority.canCall(msg.sender, address(this), msg.sig));

47:         authority = newAuthority;

49:         emit AuthorityUpdated(msg.sender, newAuthority);
50:     }

```
[L42](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L42), [L47](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L47), [L49](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L49)

```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

38:     function setAuthority(address newAuthority) public virtual {
39:         // We check if the caller is the owner first because we want to ensure they can
40:         // always swap out the authority even if it's reverting or using up a lot of gas.
41:         require(_authority.canCall(msg.sender, address(this), msg.sig));

43:         _authority = Authority(newAuthority);

45:         // Once authority is set once via any means, ensure it is initialized
46:         if (!_authorityInitialized) {
47:             _authorityInitialized = true;
48:         }

50:         emit AuthorityUpdated(msg.sender, Authority(newAuthority));
51:     }

```
[L38](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L38), [L43](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L43), [L45](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L45), [L50](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L50)

```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

85:     function setPublicCapability(
86:         address target,
87:         bytes4 functionSig,
88:         bool enabled
89:     ) public virtual requiresAuth {
90:         require(
91:             capabilityFlag[target][functionSig] != CapabilityFlag.Burned,
92:             "RolesAuthority: Capability Burned"
93:         );

95:         if (enabled) {
96:             capabilityFlag[target][functionSig] = CapabilityFlag.Public;
97:         } else {
98:             capabilityFlag[target][functionSig] = CapabilityFlag.None;
99:         }

101:         emit PublicCapabilityUpdated(target, functionSig, enabled);
102:     }

```
[L85](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L85), [L95](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L95), [L101](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L101)

</details>

&nbsp;
## [N-72] Use single file for all system-wide constants

<details>
<summary>Instances: 40</summary>

```solidity
File: packages/contracts/contracts/ActivePool.sol

24:     string public constant NAME = "ActivePool";

```
[L24](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L24)

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

29:     string public constant NAME = "BorrowerOperations";

32:     bytes32 private constant _PERMIT_POSITION_MANAGER_TYPEHASH =
33:         keccak256(
34:             "PermitPositionManagerApproval(address borrower,address positionManager,uint8 status,uint256 nonce,uint256 deadline)"
35:         );

38:     bytes32 private constant _TYPE_HASH =
39:         0x8b73c3c69bb8fe3d512ecc4cf759cc79239f7b179b0ffacaa9a75d522b39400f;

41:     string internal constant _VERSION = "1";

```
[L29](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L29), [L32](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L32), [L38](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L38), [L41](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L41)

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
[L21](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L21), [L122](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L122), [L139](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L139), [L141](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L141), [L149](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L149)

```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

19:     string public constant NAME = "CollSurplusPool";

```
[L19](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L19)

```solidity
File: packages/contracts/contracts/EBTCToken.sol

28:     string internal constant _NAME = "EBTC Stablecoin";
29:     string internal constant _SYMBOL = "EBTC";
30:     string internal constant _VERSION = "1";
31:     uint8 internal constant _DECIMALS = 18;

36:     bytes32 private constant _PERMIT_TYPEHASH =
37:         0x6e71edae12b1b97f4d1f60370fef10105fa2faae0126114a169c64845d6126c9;

39:     bytes32 private constant _TYPE_HASH =
40:         0x8b73c3c69bb8fe3d512ecc4cf759cc79239f7b179b0ffacaa9a75d522b39400f;

```
[L28](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L28), [L36](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L36), [L39](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L39)

```solidity
File: packages/contracts/contracts/PriceFeed.sol

22:     string public constant NAME = "PriceFeed";

32:     uint256 public constant TIMEOUT_ETH_BTC_FEED = 4800; // 1 hours & 20min: 60 * 80
33:     uint256 public constant TIMEOUT_STETH_ETH_FEED = 90000; // 25 hours: 60 * 60 * 25

36:     uint256 public constant MAX_PRICE_DEVIATION_FROM_PREVIOUS_ROUND = 5e17; // 50%

42:     uint256 public constant MAX_PRICE_DIFFERENCE_BETWEEN_ORACLES = 5e16; // 5%

```
[L22](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L22), [L32](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L32), [L36](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L36), [L42](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L42)

```solidity
File: packages/contracts/contracts/SortedCdps.sol

52:     string public constant NAME = "SortedCdps";

60:     uint256 constant ADDRESS_SHIFT = 96; // 8 * 12; Puts the address at leftmost bytes32 position
61:     uint256 constant BLOCK_SHIFT = 64; // 8 * 8; Puts the block value after the address

80:     bytes32 public constant dummyId =
81:         0x0000000000000000000000000000000000000000000000000000000000000000;

```
[L52](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L52), [L60](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L60), [L80](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L80)

```solidity
File: packages/contracts/contracts/HintHelpers.sol

12:     string public constant NAME = "HintHelpers";

```
[L12](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L12)

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

37:     bytes32 constant FLASH_LOAN_SUCCESS = keccak256("ERC3156FlashBorrower.onFlashLoan");

```
[L37](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L37)

```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

39:     bytes32 constant DIAMOND_STORAGE_POSITION = keccak256("diamond.standard.diamond.storage");

```
[L39](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L39)

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
[L19](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L19), [L22](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L22), [L25](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L25), [L28](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L28), [L31](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L31), [L33](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L33), [L35](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L35), [L37](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L37), [L39](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L39)

</details>

&nbsp;
## [N-73] State variable declaration should include comments

Comments describing the purpose of each state variable help to make code
more readable.

<details>
<summary>Instances: 81</summary>

```solidity
File: packages/contracts/contracts/ActivePool.sol

24:     string public constant NAME = "ActivePool";

26:     address public immutable borrowerOperationsAddress;

27:     address public immutable cdpManagerAddress;

28:     address public immutable collSurplusPoolAddress;

29:     address public feeRecipientAddress;

32:     uint256 internal systemDebt;

34:     ICollateralToken public immutable collateral;

```
[L24](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L24), [L26](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L26), [L27](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L27), [L28](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L28), [L29](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L29), [L32](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L32), [L34](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L34)

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

29:     string public constant NAME = "BorrowerOperations";

41:     string internal constant _VERSION = "1";

46:     uint256 private immutable _CACHED_CHAIN_ID;

48:     bytes32 private immutable _HASHED_NAME;

49:     bytes32 private immutable _HASHED_VERSION;

53:     ICdpManager public immutable cdpManager;

55:     ICollSurplusPool public immutable collSurplusPool;

57:     address public feeRecipientAddress;

59:     IEBTCToken public immutable ebtcToken;

69:     Used to hold, return and assign variables inside a function, in order to avoid the error:

```
[L29](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L29), [L41](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L41), [L46](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L46), [L48](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L48), [L49](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L49), [L53](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L53), [L55](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L55), [L57](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L57), [L59](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L59), [L69](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L69)

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

22:     uint128 public constant MINIMUM_GRACE_PERIOD = 15 minutes;

25:     uint128 public recoveryModeGracePeriodDuration = MINIMUM_GRACE_PERIOD;

122:     string public constant NAME = "CdpManager";

126:     address public immutable borrowerOperationsAddress;

128:     ICollSurplusPool immutable collSurplusPool;

130:     IEBTCToken public immutable override ebtcToken;

132:     address public immutable liquidationLibrary;

139:     uint256 public constant SECONDS_IN_ONE_MINUTE = 60;

142:     uint256 public redemptionFeeFloor = MIN_REDEMPTION_FEE_FLOOR;

143:     bool public redemptionsPaused;

152:     uint256 internal immutable deploymentStartTime;

161:     uint256 public baseRate;

163:     uint256 public stakingRewardSplit;

170:     uint256 public override totalStakes;

```
[L22](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L22), [L25](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L25), [L122](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L122), [L126](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L126), [L128](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L128), [L130](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L130), [L132](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L132), [L139](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L139), [L142](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L142), [L143](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L143), [L152](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L152), [L161](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L161), [L163](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L163), [L170](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L170)

```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

19:     string public constant NAME = "CollSurplusPool";

21:     address public immutable borrowerOperationsAddress;

22:     address public immutable cdpManagerAddress;

23:     address public immutable activePoolAddress;

24:     address public immutable feeRecipientAddress;

25:     ICollateralToken public immutable collateral;

```
[L19](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L19), [L21](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L21), [L22](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L22), [L23](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L23), [L24](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L24), [L25](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L25)

```solidity
File: packages/contracts/contracts/Governor.sol

17:     bytes32 NO_ROLES = bytes32(0);

```
[L17](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L17)

```solidity
File: packages/contracts/contracts/PriceFeed.sol

22:     string public constant NAME = "PriceFeed";

26:     AggregatorV3Interface public immutable STETH_ETH_CL_FEED;

```
[L22](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L22), [L26](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L26)

```solidity
File: packages/contracts/contracts/SortedCdps.sol

52:     string public constant NAME = "SortedCdps";

54:     address public immutable borrowerOperationsAddress;

56:     ICdpManager public immutable cdpManager;

58:     uint256 public immutable maxSize;

77:     Data public data;

79:     uint256 public nextCdpNonce;

80:     bytes32 public constant dummyId =

```
[L52](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L52), [L54](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L54), [L56](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L56), [L58](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L58), [L77](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L77), [L79](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L79), [L80](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L80)

```solidity
File: packages/contracts/contracts/HintHelpers.sol

12:     string public constant NAME = "HintHelpers";

14:     ISortedCdps public immutable sortedCdps;

15:     ICdpManager public immutable cdpManager;

161:     Submitting numTrials = k * sqrt(length), with k = 15 makes it very, very likely that the ouput address will 

```
[L12](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L12), [L14](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L14), [L15](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L15), [L161](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L161)

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

29:     IBorrowerOperations public immutable borrowerOperations;

30:     IActivePool public immutable activePool;

31:     ICdpCdps public immutable cdpManager;

32:     IEBTCToken public immutable ebtcToken;

33:     ISortedCdps public immutable sortedCdps;

34:     ICollateralToken public immutable stETH;

35:     bool internal immutable willSweep;

37:     bytes32 constant FLASH_LOAN_SUCCESS = keccak256("ERC3156FlashBorrower.onFlashLoan");

```
[L29](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L29), [L30](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L30), [L31](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L31), [L32](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L32), [L33](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L33), [L34](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L34), [L35](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L35), [L37](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L37)

```solidity
File: packages/contracts/contracts/LeverageMacroFactory.sol

12:     address public immutable borrowerOperations;

13:     address public immutable activePool;

14:     address public immutable cdpManager;

15:     address public immutable ebtcToken;

16:     address public immutable stETH;

17:     address public immutable sortedCdps;

```
[L12](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L12), [L13](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L13), [L14](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L14), [L15](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L15), [L16](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L16), [L17](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L17)

```solidity
File: packages/contracts/contracts/LeverageMacroReference.sol

12:     address internal immutable theOwner;

```
[L12](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L12)

```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

14:     address public owner;

16:     Authority public authority;

```
[L14](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L14), [L16](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L16)

```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

13:     Authority private _authority;

14:     bool private _authorityInitialized;

```
[L13](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L13), [L14](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L14)

```solidity
File: packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol

9:     uint256 public constant MAX_BPS = 10_000;

11:     bytes32 public constant FLASH_SUCCESS_VALUE = keccak256("ERC3156FlashBorrower.onFlashLoan");

15:     bool public flashLoansPaused;

```
[L9](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L9), [L11](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L11), [L15](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L15)

```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

39:     uint256 public constant MAX_REWARD_SPLIT = 10_000;

41:     IActivePool public immutable activePool;

43:     IPriceFeed public immutable override priceFeed;

```
[L39](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L39), [L41](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L41), [L43](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L43)

```solidity
File: packages/contracts/contracts/Dependencies/EbtcMath.sol

6:     uint256 internal constant DECIMAL_PRECISION = 1e18;

7:     uint256 public constant MAX_TCR = type(uint256).max;

```
[L6](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L6), [L7](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L7)

```solidity
File: packages/contracts/contracts/Dependencies/ReentrancyGuard.sol

8:     uint256 internal constant OPEN = 1;

9:     uint256 internal constant LOCKED = 2;

11:     uint256 public locked = OPEN;

```
[L8](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ReentrancyGuard.sol#L8), [L9](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ReentrancyGuard.sol#L9), [L11](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ReentrancyGuard.sol#L11)

</details>

&nbsp;
## [N-74] Structs, enums, events and errors should be named using CapWords style

See the [Solidity Style Guide](https://docs.soliditylang.org/en/latest/style-guide.html#struct-names)
for more info.

<details>
<summary>Instances: 4</summary>

```solidity
File: packages/contracts/contracts/Interfaces/IActivePool.sol

9:     event ActivePoolEBTCDebtUpdated(uint256 _EBTCDebt);

```
[L9](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IActivePool.sol#L9)

```solidity
File: packages/contracts/contracts/Interfaces/IPool.sol

9:     event ETHBalanceUpdated(uint256 _newBalance);
10:     event EBTCBalanceUpdated(uint256 _newBalance);

```
[L9](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPool.sol#L9)

```solidity
File: packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol

6:     event TCRNotified(uint256 TCR); /// NOTE: Mostly for debugging to ensure synch

```
[L6](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol#L6)

</details>

&nbsp;
## [N-75] Overflows in unchecked blocks

While integers with a large number of bits are unlikely to overflow on human time
scales, it is not strictly correct to use an `unchecked` block around them, because
_eventually_ they will overflow, and `unchecked` blocks are meant for cases where
it's mathematically impossible for an operation to trigger an overflow (e.g. a
prior `require()` statement prevents the overflow case)

<details>
<summary>Instances: 1</summary>

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

438:             for (uint256 i; i < length; ++i) {

```
[L438](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L438)

</details>

&nbsp;
## [N-76] Use `uint256` over `uint`

The variable size should be explicitly clarified. This improves readability and
prevents issues arising when encoding data with selectors if the alias is
mistakenly used within the signature string.

<details>
<summary>Instances: 31</summary>

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

830:         uint status = cdpManager.getCdpStatus(_cdpId);

```
[L830](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L830)

```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

278:         uint _debtToColl = (_totalDebtToBurn * DECIMAL_PRECISION) / _liqState.price;
279:         uint _cappedColl = collateral.getPooledEthByShares(_cappedColPortion + _liquidatorReward);

365:         uint _debtToColl = (_totalDebtToBurn * DECIMAL_PRECISION) / _recoveryState.price;
366:         uint _cappedColl = collateral.getPooledEthByShares(_cappedColPortion + _liquidatorReward);

435:             uint _debtToColl = (_partialDebt * DECIMAL_PRECISION) / _partialState.price;
436:             uint _cappedColl = collateral.getPooledEthByShares(_partialColl);

```
[L278](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L278), [L365](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L365), [L435](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L435)

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

353:         (
354:             uint256 _newColl,
355:             uint256 _newDebt,
356:             uint256 _feeSplitDistributed,
357:             uint _pendingDebt,
358:             uint256 _debtIndexDelta
359:         ) = _calcSyncedAccounting(_cdpId, _oldPerUnitCdp, _systemStEthFeePerUnitIndex);

365:             uint prevCollShares = _cdp.coll;

```
[L353](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L353), [L365](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L365)

```solidity
File: packages/contracts/contracts/SortedCdps.sol

155:     function cdpOfOwnerByIdx(
156:         address owner,
157:         uint256 index,
158:         bytes32 startNodeId,
159:         uint maxNodes
160:     ) external view override returns (bytes32, bool) {

173:     function _cdpOfOwnerByIndex(
174:         address owner,
175:         uint256 index,
176:         bytes32 startNodeId,
177:         uint maxNodes
178:     ) internal view returns (bytes32, bool) {

182:         uint _currentIndex = 0;
183:         uint i;

227:     function getCdpCountOf(
228:         address owner,
229:         bytes32 startNodeId,
230:         uint maxNodes
231:     ) external view override returns (uint256, bytes32) {

237:     function _cdpCountOf(
238:         address owner,
239:         bytes32 startNodeId,
240:         uint maxNodes
241:     ) internal view returns (uint256, bytes32) {

245:         uint _ownedCount = 0;
246:         uint i = 0;

286:     function getAllCdpsOf(
287:         address owner,
288:         bytes32 startNodeId,
289:         uint maxNodes
290:     ) external view override returns (bytes32[] memory, uint256, bytes32) {

299:     function _getCdpsOf(
300:         address owner,
301:         bytes32 startNodeId,
302:         uint maxNodes,
303:         uint maxArraySize
304:     ) internal view returns (bytes32[] memory, uint256, bytes32) {

311:         uint i = 0;
312:         uint _cdpRetrieved;

```
[L155](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L155), [L173](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L173), [L182](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L182), [L227](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L227), [L237](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L237), [L245](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L245), [L286](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L286), [L299](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L299), [L311](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L311)

```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

124:     function _checkICRAgainstLiqThreshold(uint256 _icr, uint _tcr) internal view returns (bool) {

140:     function _checkICRAgainstTCR(uint256 _icr, uint _tcr) internal view returns (bool) {

```
[L124](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L124), [L140](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L140)

```solidity
File: packages/contracts/contracts/Interfaces/IBorrowerOperations.sol

27:     function openCdpFor(
28:         uint _EBTCAmount,
29:         bytes32 _upperHint,
30:         bytes32 _lowerHint,
31:         uint _collAmount,
32:         address _borrower
33:     ) external returns (bytes32);

```
[L27](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L27)

```solidity
File: packages/contracts/contracts/Interfaces/ICdpManagerData.sol

42:     event CdpLiquidated(
43:         bytes32 indexed _cdpId,
44:         address indexed _borrower,
45:         uint _debt,
46:         uint _collShares,
47:         CdpOperation _operation,
48:         address indexed _liquidator,
49:         uint _premiumToLiquidator
50:     );
51:     event CdpPartiallyLiquidated(
52:         bytes32 indexed _cdpId,
53:         address indexed _borrower,
54:         uint256 _debt,
55:         uint256 _collShares,
56:         CdpOperation operation,
57:         address indexed _liquidator,
58:         uint _premiumToLiquidator
59:     );

```
[L42](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L42)

```solidity
File: packages/contracts/contracts/Interfaces/IPositionManagers.sol

32:     function permitPositionManagerApproval(
33:         address _borrower,
34:         address _positionManager,
35:         PositionManagerApproval _approval,
36:         uint _deadline,
37:         uint8 v,
38:         bytes32 r,
39:         bytes32 s
40:     ) external;

```
[L32](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPositionManagers.sol#L32)

```solidity
File: packages/contracts/contracts/Interfaces/ISortedCdps.sol

9:     event NodeAdded(bytes32 _id, uint _NICR);

63:     function getCdpCountOf(
64:         address owner,
65:         bytes32 startNodeId,
66:         uint maxNodes
67:     ) external view returns (uint256, bytes32);

71:     function getAllCdpsOf(
72:         address owner,
73:         bytes32 startNodeId,
74:         uint maxNodes
75:     ) external view returns (bytes32[] memory, uint256, bytes32);

79:     function cdpOfOwnerByIdx(
80:         address owner,
81:         uint256 index,
82:         bytes32 startNodeId,
83:         uint maxNodes
84:     ) external view returns (bytes32, bool);

```
[L9](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L9), [L63](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L63), [L71](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L71), [L79](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L79)

</details>

&nbsp;
## [N-77] Unclear error messages

Providing descriptive error strings is important to help user understand why
their transaction might have reverted, and also aids debugging.

<details>
<summary>Instances: 2</summary>

```solidity
File: packages/contracts/contracts/ActivePool.sol

104:         require(cachedSystemCollShares >= _shares, "!ActivePoolBal");

```
[L104](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L104)

```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

99:         require(cachedTotalSurplusCollShares >= claimableColl, "!CollSurplusPoolBal");

```
[L99](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L99)

</details>

&nbsp;
## [N-78] Large numeric literals should use underscores

<details>
<summary>Instances: 8</summary>

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

148:     uint256 public minuteDecayFactor = 999037758833783000;

150:     uint256 public constant MAX_MINUTE_DECAY_FACTOR = 999999999999999999; // Corresponds to a very fast decay rate, but not too extreme

```
[L148](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L148), [L150](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L150)

```solidity
File: packages/contracts/contracts/PriceFeed.sol

33:     uint256 public constant TIMEOUT_STETH_ETH_FEED = 90000; // 25 hours: 60 * 60 * 25

```
[L33](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L33)

```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

19:     uint256 public constant LICR = 1030000000000000000; // 103%

22:     uint256 public constant MCR = 1100000000000000000; // 110%

25:     uint256 public constant CCR = 1250000000000000000; // 125%

```
[L19](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L19), [L22](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L22), [L25](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L25)

```solidity
File: packages/contracts/contracts/Dependencies/EbtcMath.sol

60:         if (_minutes > 525600000) {
61:             _minutes = 525600000;

```
[L60](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L60)

</details>

&nbsp;
## [N-79] Use inline comments for unnamed variables

For example, write `function foo(uint256 x, uint256 /* y */)` instead
of `function foo(uint256 x, uint256)`.

<details>
<summary>Instances: 1</summary>

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

15:     function Cdps(bytes32) external view returns (ICdpManagerData.Cdp memory);

```
[L15](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L15)

</details>

&nbsp;
## [N-80] Remove unused imports

Unused imports should be removed to improve readability and reduce contract
bytecode size. Note that contracts referenced in comments/NatSpec but not utilised
by the contract need not be imported.

<details>
<summary>Instances: 22</summary>

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

7: import "./Interfaces/ICdpManagerData.sol";

13: import "./Dependencies/Ownable.sol";

```
[L7](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L7), [L13](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L13)

```solidity
File: packages/contracts/contracts/CdpManager.sol

6: import "./Interfaces/ICollSurplusPool.sol";

7: import "./Interfaces/IEBTCToken.sol";

9: import "./Dependencies/ICollateralTokenOracle.sol";

```
[L6](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L6), [L7](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L7), [L9](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L9)

```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

4: import "./Interfaces/ICdpManagerData.sol";

5: import "./Interfaces/ICollSurplusPool.sol";

6: import "./Interfaces/IEBTCToken.sol";

7: import "./Interfaces/ISortedCdps.sol";

8: import "./Dependencies/ICollateralTokenOracle.sol";

```
[L4](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L4), [L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L5), [L6](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L6), [L7](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L7), [L8](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L8)

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

5: import "./Interfaces/ICdpManager.sol";

11: import "./Dependencies/ICollateralTokenOracle.sol";

```
[L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L5), [L11](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L11)

```solidity
File: packages/contracts/contracts/SortedCdps.sol

7: import "./Interfaces/IBorrowerOperations.sol";

```
[L7](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L7)

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

7: import "./Interfaces/ICdpManager.sol";

9: import "./Interfaces/IPriceFeed.sol";

```
[L7](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L7), [L9](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L9)

```solidity
File: packages/contracts/contracts/LeverageMacroFactory.sol

5: import "./Dependencies/ICollateralToken.sol";

6: import "./Interfaces/IEBTCToken.sol";

```
[L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L5), [L6](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L6)

```solidity
File: packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol

6: import "../Interfaces/IWETH.sol";

```
[L6](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L6)

```solidity
File: packages/contracts/contracts/Interfaces/ICdpManagerData.sol

5: import "./ICollSurplusPool.sol";

7: import "./ISortedCdps.sol";

8: import "./IActivePool.sol";

10: import "../Dependencies/ICollateralTokenOracle.sol";

```
[L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L5), [L7](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L7), [L8](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L8), [L10](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L10)

</details>

&nbsp;
## [N-81] Unused local variable

<details>
<summary>Instances: 2</summary>

```solidity
File: packages/contracts/contracts/CdpManager.sol

922:         uint256 index = _addCdpIdToArray(_cdpId);

```
[L922](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L922)

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

465:         bytes32 _cdpId = borrowerOperations.openCdp(
466:             flData.eBTCToMint,
467:             flData._upperHint,
468:             flData._lowerHint,
469:             flData.stETHToDeposit
470:         );

```
[L465](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L465)

</details>

&nbsp;
## [N-82] Unused state variables

Consider moving the variable to a different file if it is intended to be used.

<details>
<summary>Instances: 8</summary>

```solidity
File: packages/contracts/contracts/Governor.sol

17:     bytes32 NO_ROLES = bytes32(0);

```
[L17](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L17)

```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

19:     uint256 public constant LICR = 1030000000000000000; // 103%

31:     uint256 public constant MIN_NET_STETH_BALANCE = 2e18;

33:     uint256 public constant PERCENT_DIVISOR = 200; // dividing by 200 yields 0.5%

35:     uint256 public constant BORROWING_FEE_FLOOR = 0; // 0.5%

37:     uint256 public constant STAKING_REWARD_SPLIT = 5_000; // taking 50% cut from staking reward

39:     uint256 public constant MAX_REWARD_SPLIT = 10_000;

```
[L19](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L19), [L31](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L31), [L33](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L33), [L35](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L35), [L37](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L37), [L39](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L39)

```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

30:     EnumerableSet.Bytes32Set internal enabledFunctionSigsPublic;

```
[L30](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L30)

</details>

&nbsp;
## [N-83] Unused `struct` definitions

In the below contracts structs are defined but never used.

<details>
<summary>Instances: 2</summary>

```solidity
File: packages/contracts/contracts/Governor.sol

24:     struct Capability {
25:         address target;
26:         bytes4 functionSig;
27:         uint8[] roles;
28:     }

```
[L24](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L24)

```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

28:     struct OurSettings {
29:         bool allowNonCallback;
30:         bool callbackEnabledForCall;
31:     }

```
[L28](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L28)

</details>

&nbsp;
## [N-84] Use `bytes.concat` over `abi.encodePacked`

Starting with version 0.8.4, Solidity has the bytes.concat() function, which
allows one to concatenate a list of bytes/strings, without extra padding.
Using this function rather than abi.encodePacked() makes the intended
operation more clear, leading to less reviewer confusion.

<details>
<summary>Instances: 3</summary>

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

717:         bytes32 digest = keccak256(
718:             abi.encodePacked(
719:                 "\x19\x01",
720:                 domainSeparator(),
721:                 keccak256(
722:                     abi.encode(
723:                         _PERMIT_POSITION_MANAGER_TYPEHASH,
724:                         _borrower,
725:                         _positionManager,
726:                         _approval,
727:                         _nonces[_borrower]++,
728:                         _deadline
729:                     )
730:                 )
731:             )
732:         );

```
[L717](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L717)

```solidity
File: packages/contracts/contracts/EBTCToken.sol

209:         bytes32 digest = keccak256(
210:             abi.encodePacked(
211:                 "\x19\x01",
212:                 domainSeparator(),
213:                 keccak256(
214:                     abi.encode(_PERMIT_TYPEHASH, owner, spender, amount, _nonces[owner]++, deadline)
215:                 )
216:             )
217:         );

```
[L209](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L209)

```solidity
File: packages/contracts/contracts/HintHelpers.sol

182:             latestRandomSeed = uint256(keccak256(abi.encodePacked(latestRandomSeed)));

```
[L182](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L182)

</details>

&nbsp;
## [N-85] Use `delete` rather than assigning to `0`

Using `delete` more closely aligns with the intention of the action, and draws more
attention towards the changing of state, which may lead to a more thorough audit of
its associated logic"

<details>
<summary>Instances: 11</summary>

```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

264:                 _collSurplus = 0;

```
[L264](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L264)

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

272:         Cdps[_cdpId].coll = 0;

273:         Cdps[_cdpId].debt = 0;

274:         Cdps[_cdpId].liquidatorRewardShares = 0;

276:         cdpDebtRedistributionIndex[_cdpId] = 0;

277:         cdpStEthFeePerUnitIndex[_cdpId] = 0;

413:         Cdps[_cdpId].stake = 0;

```
[L272](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L272), [L273](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L273), [L274](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L274), [L276](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L276), [L277](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L277), [L413](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L413)

```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

94:         balances[_account] = 0;

```
[L94](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L94)

```solidity
File: packages/contracts/contracts/HintHelpers.sol

105:                         partialRedemptionHintNICR = 0; //reset to 0 as there is no partial redemption in this case

106:                         partialRedemptionNewColl = 0;

109:                         vars.remainingEbtcToRedeem = 0;

```
[L105](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L105), [L106](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L106), [L109](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L109)

</details>

&nbsp;
## [N-86] Use descriptive constant rather than `0` for function arguments

Passing zero as a function argument can sometimes result in a security issue
(e.g. passing zero as the slippage parameter). Consider using a `constant`
variable with a descriptive name, so it's clear that the argument is
intentionally being used, and for the right reasons.

<details>
<summary>Instances: 33</summary>

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

209:         _adjustCdpInternal(_cdpId, 0, 0, false, _upperHint, _lowerHint, _stEthBalanceIncrease);

225:         _adjustCdpInternal(_cdpId, _stEthBalanceDecrease, 0, false, _upperHint, _lowerHint, 0);

241:         _adjustCdpInternal(_cdpId, 0, _debt, true, _upperHint, _lowerHint, 0);

256:         _adjustCdpInternal(_cdpId, 0, _debt, false, _upperHint, _lowerHint, 0);

278:         _adjustCdpInternal(
279:             _cdpId,
280:             _stEthBalanceDecrease,
281:             _debtChange,
282:             _isDebtIncrease,
283:             _upperHint,
284:             _lowerHint,
285:             0
286:         );

```
[L209](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L209), [L225](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L225), [L241](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L241), [L256](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L256), [L278](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L278)

```solidity
File: packages/contracts/contracts/CdpManager.sol

171:                 _closeCdpByRedemption(
172:                     _redeemColFromCdp.cdpId,
173:                     0,
174:                     newColl,
175:                     _liquidatorRewardShares,
176:                     _borrower
177:                 );

```
[L171](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L171)

```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

41:         _liquidateIndividualCdpSetup(_cdpId, 0, _cdpId, _cdpId);

101:         LiquidationLocals memory _liqState = LiquidationLocals(
102:             _cdpId,
103:             _partialAmount,
104:             _price,
105:             _ICR,
106:             _upperPartialHint,
107:             _lowerPartialHint,
108:             (_recoveryModeAtStart),
109:             _TCR,
110:             0,
111:             0,
112:             0,
113:             0,
114:             0
115:         );

117:         LiquidationRecoveryModeLocals memory _rs = LiquidationRecoveryModeLocals(
118:             systemDebt,
119:             systemColl,
120:             0,
121:             0,
122:             0,
123:             _cdpId,
124:             _price,
125:             _ICR,
126:             0,
127:             0
128:         );

418:             return (0, 0);

614:         LiquidationLocals memory _liqState = LiquidationLocals(
615:             vars.cdpId,
616:             0,
617:             _price,
618:             vars.ICR,
619:             vars.cdpId,
620:             vars.cdpId,
621:             (false),
622:             _TCR,
623:             0,
624:             0,
625:             0,
626:             0,
627:             0
628:         );

649:         LiquidationRecoveryModeLocals memory _recState = LiquidationRecoveryModeLocals(
650:             _systemDebt,
651:             _systemCollShares,
652:             0,
653:             0,
654:             0,
655:             vars.cdpId,
656:             _price,
657:             vars.ICR,
658:             0,
659:             0
660:         );

```
[L41](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L41), [L101](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L101), [L117](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L117), [L418](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L418), [L614](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L614), [L649](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L649)

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

310:             return (0, 0);

318:             return (0, 0);

628:             return (0, _cdpCol);

643:             return (0, _cdpCol);

777:             return (0, systemStEthFeePerUnitIndex, systemStEthFeePerUnitIndexError);

```
[L310](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L310), [L318](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L318), [L628](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L628), [L643](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L643), [L777](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L777)

```solidity
File: packages/contracts/contracts/SortedCdps.sol

144:         (bytes32 _cdpId, ) = _cdpOfOwnerByIndex(owner, index, dummyId, 0);

217:         (uint256 _cnt, ) = _cdpCountOf(owner, dummyId, 0);

273:         (uint _ownedCount, ) = _cdpCountOf(owner, dummyId, 0);

275:             (bytes32[] memory _allCdps, , ) = _getCdpsOf(owner, dummyId, 0, _ownedCount);

306:             return (new bytes32[](0), 0, dummyId);

```
[L144](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L144), [L217](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L217), [L273](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L273), [L275](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L275), [L306](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L306)

```solidity
File: packages/contracts/contracts/HintHelpers.sol

172:             return (sortedCdps.nonExistId(), 0, _inputRandomSeed);

```
[L172](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L172)

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

414:         (bool success, ) = excessivelySafeCall(
415:             swapData.addressForSwap,
416:             gasleft(),
417:             0,
418:             0,
419:             swapData.calldataForSwap
420:         );

427:         IERC20(swapData.tokenForSwap).safeApprove(swapData.addressForApprove, 0);

514:             _success := call(
515:                 _gas, // gas
516:                 _target, // recipient
517:                 _value, // ether value
518:                 add(_calldata, 0x20), // inloc
519:                 mload(_calldata), // inlen
520:                 0, // outloc
521:                 0 // outlen
522:             )

531:             returndatacopy(add(_returnData, 0x20), 0, _toCopy)

```
[L414](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L414), [L427](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L427), [L514](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L514), [L531](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L531)

```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

144:                 success := delegatecall(txGas, to, add(data, 0x20), mload(data), 0, 0)

149:                 success := call(txGas, to, value, add(data, 0x20), mload(data), 0, 0)

190:             calldatacopy(0, 0, calldatasize())
191:             let result := delegatecall(gas(), facet, 0, calldatasize(), 0, 0)
192:             returndatacopy(0, 0, returndatasize())

198:                 return(0, returndatasize())

```
[L144](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L144), [L149](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L149), [L190](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L190), [L198](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L198)

</details>

&nbsp;
## [N-87] No need to initialize variables to their default value

Since the variables are automatically set to 0 when created, it is redundant
to initialize it with 0 again.

<details>
<summary>Instances: 12</summary>

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
[L46](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L46), [L54](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L54), [L57](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L57), [L76](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L76), [L82](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L82), [L84](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L84), [L98](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L98), [L105](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L105), [L107](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L107), [L122](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L122), [L137](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L137)

```solidity
File: packages/contracts/contracts/SortedCdps.sol

432:         for (uint256 i = 0; i < _len; ++i) {

```
[L432](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L432)

</details>

&nbsp;
## [N-88] Non `constant` state variables should be named using mixedCase

See the
[Solidity style guide](https://docs.soliditylang.org/en/v0.8.17/style-guide.html#local-and-state-variable-names)
for more info.

<details>
<summary>Instances: 2</summary>

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

205:     bytes32[] public CdpIds;

```
[L205](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L205)

```solidity
File: packages/contracts/contracts/Governor.sol

17:     bytes32 NO_ROLES = bytes32(0);

```
[L17](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L17)

</details>

&nbsp;
## [N-89] Certain variables should be mutable

Certain variables such as fee recipients ought not to be `constant`/`immutable`
so that code is future proof, and resistant against private key loss/theft.

<details>
<summary>Instances: 1</summary>

```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

24:     address public immutable feeRecipientAddress;

```
[L24](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L24)

</details>

&nbsp;
## [N-90] Avoid extraneous whitespace

See the [Solidity style guide](https://docs.soliditylang.org/en/v0.8.16/style-guide.html#whitespace-in-expressions)
for more details.

<details>
<summary>Instances: 5</summary>

```solidity
File: packages/contracts/contracts/CdpManager.sol

553:         3e30 EBTC dwarfs the value of all wealth in the world ( which is < 1e15 USD). */

```
[L553](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L553)

```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

753:         for (vars.i = _start; ; ) {

816:         for (vars.i = _start; ; ) {

```
[L753](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L753), [L816](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L816)

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

385:         for (uint256 i; i < swapLength; ) {

```
[L385](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L385)

```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

114:         for (uint256 i; i < length; ) {

```
[L114](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L114)

</details>

&nbsp;
## [N-91] Top level declarations should be separated by two blank lines

See the [Solidity style guide](https://docs.soliditylang.org/en/v0.8.16/style-guide.html#blank-lines)
for more details.

<details>
<summary>Instances: 66</summary>

```solidity
File: packages/contracts/contracts/ActivePool.sol

3: pragma solidity 0.8.17;

5: import "./Interfaces/IActivePool.sol";

13: import "./Dependencies/BaseMath.sol";

15: /**
16:  * @title The Active Pool holds the collateral and EBTC debt (only accounting but not EBTC tokens) for all active cdps.
17:  *
18:  * @notice When a cdp is liquidated, it's collateral will be transferred from the Active Pool
19:  * @notice (destination may vary depending on the liquidation conditions).
20:  * @dev ActivePool also allows ERC3156 compatible flashloan of stETH token
21:  */
22: contract ActivePool is IActivePool, ERC3156FlashLender, ReentrancyGuard, BaseMath, AuthNoOwner {

```
[L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L3), [L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L5), [L13](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L13), [L15](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L15)

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

3: pragma solidity 0.8.17;

5: import "./Interfaces/IBorrowerOperations.sol";

16: import "./Dependencies/PermitNonce.sol";

18: /// @title BorrowerOperations is mainly in charge of all end user interactions like Cdp open, adjust, close etc
19: /// @notice End users could approve delegate via IPositionManagers for authorized actions on their behalf
20: /// @dev BorrowerOperations also allows ERC3156 compatible flashmint of eBTC token
21: contract BorrowerOperations is
22:     EbtcBase,
23:     ReentrancyGuard,
24:     IBorrowerOperations,
25:     ERC3156FlashLender,
26:     AuthNoOwner,
27:     PermitNonce
28: {

```
[L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L3), [L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L5), [L16](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L16), [L18](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L18)

```solidity
File: packages/contracts/contracts/CdpManager.sol

3: pragma solidity 0.8.17;

5: import "./Interfaces/ICdpManager.sol";

11: import "./Dependencies/Proxy.sol";

13: /// @title CdpManager is mainly in charge of all Cdp related core processing like collateral & debt accounting, split fee calculation, redemption, etc
14: /// @notice Except for redemption, end user typically will interact with BorrowerOeprations for individual Cdp actions
15: /// @dev CdpManager also handles liquidation through delegatecall to LiquidationLibrary
16: contract CdpManager is CdpManagerStorage, ICdpManager, Proxy {

```
[L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L3), [L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L5), [L11](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L11), [L13](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L13)

```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

3: pragma solidity 0.8.17;
4: import "./Interfaces/ICdpManagerData.sol";

9: import "./CdpManagerStorage.sol";

11: /// @title LiquidationLibrary mainly provide necessary logic to fulfill liquidation for eBTC Cdps.
12: /// @dev This contract shares same base and storage layout with CdpManager and is the delegatecall destination from CdpManager
13: contract LiquidationLibrary is CdpManagerStorage {

```
[L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L3), [L9](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L9), [L11](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L11)

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

3: pragma solidity 0.8.17;

5: import "./Interfaces/ICdpManager.sol";

12: import "./Dependencies/AuthNoOwner.sol";

14: /// @title CDP Manager storage and shared functions with LiquidationLibrary
15: /// @dev All features around Cdp management are split into separate parts to get around contract size limitations.
16: /// @dev Liquidation related functions are delegated to LiquidationLibrary contract code.
17: /// @dev Both CdpManager and LiquidationLibrary must maintain **the same storage layout**, so shared storage components
18: /// @dev and shared functions are added here in CdpManagerStorage to de-dup code
19: contract CdpManagerStorage is EbtcBase, ReentrancyGuard, ICdpManagerData, AuthNoOwner {

```
[L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L3), [L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L5), [L12](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L12), [L14](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L14)

```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

3: pragma solidity 0.8.17;

5: import "./Interfaces/ICollSurplusPool.sol";

10: import "./Interfaces/IActivePool.sol";

12: /// @notice CollSurplusPool holds stETH collateral for Cdp owner when redemption or liquidation happens
13: /// @notice only if there is a remaining portion of the closed Cdp for the owner to claim
14: /// @dev While an owner could have multiple different sized Cdps, the remaining surplus colateral from all of its closed Cdp
15: /// @dev is consolidated into one balance here
16: contract CollSurplusPool is ICollSurplusPool, ReentrancyGuard, AuthNoOwner {

```
[L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L3), [L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L5), [L10](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L10), [L12](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L12)

```solidity
File: packages/contracts/contracts/EBTCToken.sol

3: pragma solidity 0.8.17;

5: import "./Interfaces/IEBTCToken.sol";

8: import "./Dependencies/PermitNonce.sol";

10: /*
11:  *
12:  * Based upon OpenZeppelin's ERC20 contract:
13:  * https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/token/ERC20/ERC20.sol
14:  *
15:  * and their EIP2612 (ERC20Permit / ERC712) functionality:
16:  * https://github.com/OpenZeppelin/openzeppelin-contracts/blob/53516bc555a454862470e7860a9b5254db4d00f5/contracts/token/ERC20/ERC20Permit.sol
17:  *
18:  *
19:  * --- Functionality added specific to the EBTCToken ---
20:  *
21:  * 1) Transfer protection: blocklist of addresses that are invalid recipients (i.e. core Ebtc contracts) in external transfer() and transferFrom() calls.
22:  * The purpose is to protect users from losing tokens by mistakenly sending EBTC directly to a Liquity.
23:  * core contract, when they should rather call the right function.
24:  */

26: contract EBTCToken is IEBTCToken, AuthNoOwner, PermitNonce {

```
[L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L3), [L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L5), [L8](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L8), [L10](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L10), [L26](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L26)

```solidity
File: packages/contracts/contracts/Governor.sol

2: pragma solidity 0.8.17;

4: import {EnumerableSet} from "./Dependencies/EnumerableSet.sol";

6: import {RolesAuthority} from "./Dependencies/RolesAuthority.sol";

8: /// @notice Role based Authority that supports up to 256 roles.
9: /// @notice We have taken the tradeoff of additional storage usage for easier readabiliy without using off-chain / indexing services.
10: /// @author BadgerDAO Expanded from Solmate RolesAuthority
11: /// @author Modified from Solmate (https://github.com/transmissions11/solmate/blob/main/src/auth/authorities/RolesAuthority.sol)
12: /// @author Modified from Dappsys (https://github.com/dapphub/ds-roles/blob/master/src/roles.sol)
13: contract Governor is RolesAuthority {

```
[L2](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L2), [L4](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L4), [L6](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L6), [L8](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L8)

```solidity
File: packages/contracts/contracts/PriceFeed.sol

3: pragma solidity 0.8.17;

5: import "./Interfaces/IPriceFeed.sol";

10: import "./Dependencies/AuthNoOwner.sol";

12: /*
13:  * PriceFeed for mainnet deployment, it connects to two Chainlink's live feeds, ETH:BTC and
14:  * stETH:ETH, which are used to aggregate the price feed of stETH:BTC in conjuction.
15:  * It also allows for a fallback oracle to intervene in case that the primary Chainlink oracle fails.
16:  *
17:  * The PriceFeed uses Chainlink as primary oracle and allows for an optional fallback source. It contains logic for
18:  * switching oracles based on oracle failures, timeouts, and conditions for returning to the primary
19:  * Chainlink oracle. In addition, it contains the mechanism to add or remove the fallback oracle through governance.
20:  */
21: contract PriceFeed is BaseMath, IPriceFeed, AuthNoOwner {

```
[L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L3), [L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L5), [L10](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L10), [L12](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L12)

```solidity
File: packages/contracts/contracts/SortedCdps.sol

3: pragma solidity 0.8.17;

5: import "./Interfaces/ISortedCdps.sol";

7: import "./Interfaces/IBorrowerOperations.sol";

9: /*
10:  * A sorted doubly linked list with nodes sorted in descending order.
11:  *
12:  * Nodes map to active Cdps in the system by Id.
13:  * Nodes are ordered according to their current nominal individual collateral ratio (NICR),
14:  * which is like the ICR but without the price, i.e., just collateral / debt.
15:  *
16:  * The list optionally accepts insert position hints.
17:  *
18:  * NICRs are computed dynamically at runtime, and not stored on the Node. This is because NICRs of active Cdps
19:  * change dynamically as liquidation events occur.
20:  *
21:  * The list relies on the fact that liquidation events preserve ordering: a liquidation decreases the NICRs of all active Cdps,
22:  * but maintains their order. A node inserted based on current NICR will maintain the correct position,
23:  * relative to it's peers, as rewards accumulate, as long as it's raw collateral and debt have not changed.
24:  * Thus, Nodes remain sorted by current NICR.
25:  *
26:  * Nodes need only be re-inserted upon a CDP operation - when the owner adds or removes collateral or debt
27:  * to their position.
28:  *
29:  * The list is a modification of the following audited SortedDoublyLinkedList:
30:  * https://github.com/livepeer/protocol/blob/master/contracts/libraries/SortedDoublyLL.sol
31:  *
32:  *
33:  * Changes made in the Liquity implementation:
34:  *
35:  * - Keys have been removed from nodes
36:  *
37:  * - Ordering checks for insertion are performed by comparing an NICR argument to the current NICR, calculated at runtime.
38:  *   The list relies on the property that ordering by ICR is maintained as the stETH:BTC price varies.
39:  *
40:  * - Public functions with parameters have been made internal to save gas, and given an external wrapper function for external access
41:  *
42:  *
43:  * Changes made in the Ebtc implementation:
44:  *
45:  * - Positions are now indexed by Ids, not addresses. Functions to generate Ids are provided.
46:  *
47:  * - Added batchRemove functions to optimize redemptions.
48:  *
49:  * - Added more O(n) getter functions and pagination-flavor variants, intended for off-chain use.
50:  */
51: contract SortedCdps is ISortedCdps {

```
[L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L3), [L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L5), [L7](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L7), [L9](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L9)

```solidity
File: packages/contracts/contracts/HintHelpers.sol

3: pragma solidity 0.8.17;

5: import "./Interfaces/ICdpManager.sol";

7: import "./Dependencies/EbtcBase.sol";

9: /// @title HintHelpers mainly serves to provide handy information to facilitate offchain integration like redemption bots.
10: /// @dev It is strongly recommended to use HintHelper for redemption purpose
11: contract HintHelpers is EbtcBase {

```
[L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L3), [L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L5), [L7](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L7), [L9](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L9)

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

2: pragma solidity 0.8.17;

4: import "./Interfaces/IBorrowerOperations.sol";

12: import "./Dependencies/SafeERC20.sol";

14: interface ICdpCdps {

```
[L2](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L2), [L4](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L4), [L12](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L12), [L14](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L14)

```solidity
File: packages/contracts/contracts/LeverageMacroDelegateTarget.sol

2: pragma solidity 0.8.17;

4: import {LeverageMacroBase} from "./LeverageMacroBase.sol";
4: import {LeverageMacroBase} from "./LeverageMacroBase.sol";

6: interface IOwnerLike {

```
[L2](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L2), [L4](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L4), [L6](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L6)

```solidity
File: packages/contracts/contracts/LeverageMacroFactory.sol

2: pragma solidity 0.8.17;

4: import {LeverageMacroReference} from "./LeverageMacroReference.sol";

6: import "./Interfaces/IEBTCToken.sol";

8: /**
9:  * @title Factory for deploying LeverageMacros
10:  */
11: contract LeverageMacroFactory {

```
[L2](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L2), [L4](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L4), [L6](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L6), [L8](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L8)

```solidity
File: packages/contracts/contracts/LeverageMacroReference.sol

2: pragma solidity 0.8.17;

4: import {LeverageMacroBase} from "./LeverageMacroBase.sol";
4: import {LeverageMacroBase} from "./LeverageMacroBase.sol";

6: /**
7:  * @title Reference implementation of LeverageMacro
8:  * @notice Deploy a copy of this via `LeverageMacroFactory` to use it for yourself
9:  * @dev You can deploy a copy of this via a clone or similar to save users gas
10:  */
11: contract LeverageMacroReference is LeverageMacroBase {

```
[L2](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L2), [L4](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L4), [L6](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L6)

```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

2: pragma solidity 0.8.17;

4: /**
5:  * @title A multi-purpose Smart Contract Wallet
6:  * @notice `execute`s just like DSProxy
7:  * @notice handles callbacks via a DiamondLike Pattern
8:  * @notice CallbackOnly, only when toggled on, unless explicitly changed
9:  * @notice Due to the additional complexity, it's best used with a TX Simulator
10:  *
11:  * @dev Diamond Like Storage
12:  *  Because of risk of clash, we must place storage at a pseudo-random location (see DIAMOND EIP)
13:  *  Add to `OurSettings` to extend the eternal storage with custom fields
14:  *
15:  * @dev Hardcoded Functions
16:  *  Per solidity, hardcoded functions are switched into, meaning they cannot be overriden (although you could set a callbackHandler that cannot be reached)
17:  *  All other functions will reach the `fallback`
18:  *  This is basically a diamond, with an extra check for safety / extra control from the owner
19:  *
20:  * @dev Explicit Callback Handling
21:  *  All SimplifiedDiamondLike are deployed with `allowNonCallback` set to `false`
22:  *  This ensures that nobody can call this contract unless the owner sets this to `true` via the scary `setAllowAnyCall`
23:  *
24:  */
25: contract SimplifiedDiamondLike {

```
[L2](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L2), [L4](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L4)

```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

2: pragma solidity 0.8.17;

4: import {Authority} from "./Authority.sol";
4: import {Authority} from "./Authority.sol";

6: /// @notice Provides a flexible and updatable auth pattern which is completely separate from application logic.
7: /// @author Solmate (https://github.com/transmissions11/solmate/blob/main/src/auth/Auth.sol)
8: /// @author Modified from Dappsys (https://github.com/dapphub/ds-auth/blob/master/src/auth.sol)
9: abstract contract Auth {

```
[L2](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L2), [L4](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L4), [L6](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L6)

```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

2: pragma solidity 0.8.17;

4: import {Authority} from "./Authority.sol";
4: import {Authority} from "./Authority.sol";

6: /// @notice Provides a flexible and updatable auth pattern which is completely separate from application logic.
7: /// @author Modified by BadgerDAO to remove owner
8: /// @author Solmate (https://github.com/transmissions11/solmate/blob/main/src/auth/Auth.sol)
9: /// @author Modified from Dappsys (https://github.com/dapphub/ds-auth/blob/master/src/auth.sol)
10: contract AuthNoOwner {

```
[L2](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L2), [L4](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L4), [L6](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L6)

```solidity
File: packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol

3: pragma solidity 0.8.17;

5: import "../Interfaces/IERC3156FlashLender.sol";
6: import "../Interfaces/IWETH.sol";

8: abstract contract ERC3156FlashLender is IERC3156FlashLender {

```
[L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L3), [L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L5), [L8](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L8)

```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

3: pragma solidity 0.8.17;

5: import "./BaseMath.sol";

10: import "../Dependencies/ICollateralToken.sol";

12: /*
13:  * Base contract for CdpManager, BorrowerOperations. Contains global system constants and
14:  * common functions.
15:  */
16: contract EbtcBase is BaseMath, IEbtcBase {

```
[L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L3), [L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L5), [L10](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L10), [L12](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L12)

```solidity
File: packages/contracts/contracts/Dependencies/EbtcMath.sol

3: pragma solidity 0.8.17;

5: library EbtcMath {

```
[L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L3), [L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L5)

```solidity
File: packages/contracts/contracts/Dependencies/ReentrancyGuard.sol

2: pragma solidity 0.8.17;

4: /// @notice Gas optimized reentrancy protection for smart contracts.
5: /// @author Solmate (https://github.com/transmissions11/solmate/blob/main/src/utils/ReentrancyGuard.sol)
6: /// @author Modified from OpenZeppelin (https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/security/ReentrancyGuard.sol)
7: abstract contract ReentrancyGuard {

```
[L2](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ReentrancyGuard.sol#L2), [L4](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ReentrancyGuard.sol#L4)

```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

2: pragma solidity 0.8.17;

4: import {IRolesAuthority} from "./IRolesAuthority.sol";

6: import "./EnumerableSet.sol";

8: /// @notice Role based Authority that supports up to 256 roles.
9: /// @author BadgerDAO
10: /// @author Modified from Solmate (https://github.com/transmissions11/solmate/blob/main/src/auth/authorities/RolesAuthority.sol)
11: /// @author Modified from Dappsys (https://github.com/dapphub/ds-roles/blob/master/src/roles.sol)
12: contract RolesAuthority is IRolesAuthority, Auth, Authority {

```
[L2](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L2), [L4](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L4), [L6](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L6), [L8](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L8)

```solidity
File: packages/contracts/contracts/Interfaces/IActivePool.sol

3: pragma solidity 0.8.17;

5: import "./IPool.sol";
5: import "./IPool.sol";

7: interface IActivePool is IPool {

```
[L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IActivePool.sol#L3), [L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IActivePool.sol#L5), [L7](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IActivePool.sol#L7)

```solidity
File: packages/contracts/contracts/Interfaces/IBorrowerOperations.sol

3: pragma solidity 0.8.17;
4: import "./IPositionManagers.sol";
4: import "./IPositionManagers.sol";

6: // Common interface for the Cdp Manager.
7: interface IBorrowerOperations is IPositionManagers {

```
[L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L3), [L6](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L6)

```solidity
File: packages/contracts/contracts/Interfaces/ICdpManager.sol

3: pragma solidity 0.8.17;

5: import "./IEbtcBase.sol";
6: import "./ICdpManagerData.sol";

8: // Common interface for the Cdp Manager.
9: interface ICdpManager is IEbtcBase, ICdpManagerData {

```
[L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol#L3), [L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol#L5), [L8](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol#L8)

```solidity
File: packages/contracts/contracts/Interfaces/ICdpManagerData.sol

3: pragma solidity 0.8.17;

5: import "./ICollSurplusPool.sol";

10: import "../Dependencies/ICollateralTokenOracle.sol";

12: // Common interface for the Cdp Manager.
13: interface ICdpManagerData is IRecoveryModeGracePeriod {

```
[L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L3), [L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L5), [L10](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L10), [L12](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L12)

```solidity
File: packages/contracts/contracts/Interfaces/ICollSurplusPool.sol

3: pragma solidity 0.8.17;

5: interface ICollSurplusPool {

```
[L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICollSurplusPool.sol#L3), [L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICollSurplusPool.sol#L5)

```solidity
File: packages/contracts/contracts/Interfaces/IEbtcBase.sol

3: pragma solidity 0.8.17;

5: import "./IPriceFeed.sol";
5: import "./IPriceFeed.sol";

7: interface IEbtcBase {

```
[L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IEbtcBase.sol#L3), [L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IEbtcBase.sol#L5), [L7](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IEbtcBase.sol#L7)

```solidity
File: packages/contracts/contracts/Interfaces/IEBTCToken.sol

3: pragma solidity 0.8.17;

5: import "../Dependencies/IERC20.sol";
6: import "../Dependencies/IERC2612.sol";

8: interface IEBTCToken is IERC20, IERC2612 {

```
[L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IEBTCToken.sol#L3), [L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IEBTCToken.sol#L5), [L8](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IEBTCToken.sol#L8)

```solidity
File: packages/contracts/contracts/Interfaces/IERC3156FlashBorrower.sol

3: pragma solidity 0.8.17;

5: interface IERC3156FlashBorrower {

```
[L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IERC3156FlashBorrower.sol#L3), [L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IERC3156FlashBorrower.sol#L5)

```solidity
File: packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol

3: pragma solidity 0.8.17;

5: import "./IERC3156FlashBorrower.sol";
5: import "./IERC3156FlashBorrower.sol";

7: interface IERC3156FlashLender {

```
[L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol#L3), [L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol#L5), [L7](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol#L7)

```solidity
File: packages/contracts/contracts/Interfaces/IFallbackCaller.sol

3: pragma solidity 0.8.17;

5: interface IFallbackCaller {

```
[L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IFallbackCaller.sol#L3), [L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IFallbackCaller.sol#L5)

```solidity
File: packages/contracts/contracts/Interfaces/IPermitNonce.sol

3: pragma solidity 0.8.17;

5: interface IPermitNonce {

```
[L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPermitNonce.sol#L3), [L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPermitNonce.sol#L5)

```solidity
File: packages/contracts/contracts/Interfaces/IPool.sol

3: pragma solidity 0.8.17;

5: // Common interface for the Pools.
6: interface IPool {

```
[L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPool.sol#L3), [L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPool.sol#L5)

```solidity
File: packages/contracts/contracts/Interfaces/IPositionManagers.sol

3: pragma solidity 0.8.17;

5: interface IPositionManagers {

```
[L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPositionManagers.sol#L3), [L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPositionManagers.sol#L5)

```solidity
File: packages/contracts/contracts/Interfaces/IPriceFeed.sol

3: pragma solidity 0.8.17;

5: interface IPriceFeed {

```
[L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPriceFeed.sol#L3), [L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPriceFeed.sol#L5)

```solidity
File: packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol

2: pragma solidity 0.8.17;

4: // Interface for State Updates that can trigger RM Liquidations
5: interface IRecoveryModeGracePeriod {

```
[L2](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol#L2), [L4](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol#L4)

```solidity
File: packages/contracts/contracts/Interfaces/ISortedCdps.sol

3: pragma solidity 0.8.17;

5: // Common interface for the SortedCdps Doubly Linked List.
6: interface ISortedCdps {

```
[L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L3), [L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L5)

</details>

&nbsp;
## [N-92] Large or complicated code bases should implement invariant tests

Large code bases, or code with lots of inline-assembly, complicated math, or
complicated interactions between multiple contracts, should implement
[invariant fuzzing tests](https://medium.com/coinmonks/smart-contract-fuzzing-d9b88e0b0a05).
Invariant fuzzers such as Echidna require the test writer to
come up with invariants which should not be violated under any circumstances,
and the fuzzer tests various inputs and function calls to ensure that the
invariants always hold. Even code with 100% code coverage can still have bugs
due to the order of the operations a user performs, and invariant fuzzers,
with properly and extensively-written invariants, can close this testing gap
significantly.

&nbsp;
## [N-93] Tests should have full coverage

While 100% code coverage does not guarantee that there are no bugs, it often
will catch easy-to-find bugs, and will ensure that there are fewer regressions
when the code invariably has to be modified. Furthermore, in order to get full
coverage, code authors will often have to re-organize their code so that it is
more modular, so that each component can be tested separately, which reduces
interdependencies between modules and layers, and makes for code that is
easier to reason about and audit.

&nbsp;
## [N-94] Codebase should go through formal verification

Formal verification is the act of proving or disproving the correctness of
intended algorithms underlying a system with respect to a certain formal
specification/property/invariant, using formal methods of mathematics.

Some tools that are currently available to perform these tests on smart
contracts are [SMTChecker](https://docs.soliditylang.org/en/latest/smtchecker.html)
and [Certora Prover](https://www.certora.com/).

&nbsp;

&nbsp;
