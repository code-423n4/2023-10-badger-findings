## Summary

### Low Risk Issues

| |Issue|Instances|
|-|:-|:-:|
| [[L&#x2011;1](#l1-vulnerable-versions-of-packages-are-being-used)] | Vulnerable versions of packages are being used | 1 | 
| [[L&#x2011;2](#l2-missing-checks-for-address-0-when-assigning-values-to-address-state-variables)] | Missing checks for `address(0)` when assigning values to address state variables | 27 | 
| [[L&#x2011;3](#l3-for-loops-in-public-or-external-functions-should-be-avoided-due-to-high-gas-costs-and-possible-dos)] | For loops in public or external functions should be avoided due to high gas costs and possible DOS | 11 | 
| [[L&#x2011;4](#l4-missing-checks-in-constructor-initialize)] | Missing checks in constructor/initialize | 1 | 
| [[L&#x2011;5](#l5-external-calls-in-an-un-bounded-loop-may-result-in-a-dos)] | `external` calls in an un-bounded loop may result in a DOS | 14 | 
| [[L&#x2011;6](#l6-internal-function-calls-within-for-loops)] | `internal` Function calls within for loops | 17 | 
| [[L&#x2011;7](#l7-loss-of-precision)] | Loss of precision | 13 | 
| [[L&#x2011;8](#l8-require-should-be-used-instead-of-assert)] | `require()` should be used instead of `assert()` | 1 | 
| [[L&#x2011;9](#l9-consider-using-openzeppelin-s-safecast-library-to-prevent-unexpected-overflows-when-casting-from-various-type-int-uint-values)] | Consider using OpenZeppelin’s SafeCast library to prevent unexpected overflows when casting from various type int/uint values | 5 | 
| [[L&#x2011;10](#l10-setters-should-have-initial-value-check)] | Setters should have initial value check | 10 | 
| [[L&#x2011;11](#l11-sweeping-may-break-accounting-if-tokens-with-multiple-addresses-are-used)] | Sweeping may break accounting if tokens with multiple addresses are used | 3 | 
| [[L&#x2011;12](#l12-int-casting-block-timestamp-can-reduce-the-lifespan-of-a-contract)] | Int casting `block.timestamp` can reduce the lifespan of a contract | 1 | 
| [[L&#x2011;13](#l13-unused-empty-receive-fallback-function)] | Unused/empty `receive()`/`fallback()` function | 1 | 
| [[L&#x2011;14](#l14-consider-implementing-two-step-procedure-for-updating-protocol-addresses)] | Consider implementing two-step procedure for updating protocol addresses | 2 | 
| [[L&#x2011;15](#l15-safeapprove-is-deprecated)] | `safeApprove()` is deprecated | 2 | 
| [[L&#x2011;16](#l16-consider-using-descriptive-constant-s-when-passing-zero-as-a-function-argument)] | Consider using descriptive `constant`s when passing zero as a function argument | 9 | 
| [[L&#x2011;17](#l17-functions-calling-contracts-addresses-with-transfer-hooks-are-missing-reentrancy-guards)] | Functions calling contracts/addresses with transfer hooks are missing reentrancy guards | 5 | 
| [[L&#x2011;18](#l18-some-function-should-not-be-marked-as-payable)] | Some function should not be marked as payable | 3 | 
| [[L&#x2011;19](#l19-code-does-not-follow-the-best-practice-of-check-effects-interaction)] | Code does not follow the best practice of check-effects-interaction | 7 | 
| [[L&#x2011;20](#l20-prevent-re-setting-a-state-variable-with-the-same-value)] | prevent re-setting a state variable with the same value | 21 | 
| [[L&#x2011;21](#l21-some-tokens-may-not-consider-type-uint256-max-as-an-infinite-approval)] | Some tokens may not consider `type(uint256).max` as an infinite approval | 6 | 
| [[L&#x2011;22](#l22-missing-contract-existence-checks-before-yul-call)] | Missing contract-existence checks before yul `call()` | 4 | 
| [[L&#x2011;23](#l23-subtraction-may-underflow-if-multiplication-is-too-large)] | Subtraction may underflow if multiplication is too large | 2 | 

Total: 166 instances over 23 issues

### Non-critical Issues

| |Issue|Instances|
|-|:-|:-:|
| [[NC&#x2011;1](#nc1-state-variables-declarations-should-have-natspec-descriptions)] | State variables declarations should have NatSpec descriptions | 155 | 
| [[NC&#x2011;2](#nc2-consider-using-modifiers-for-address-control)] | Consider using modifiers for address control | 23 | 
| [[NC&#x2011;3](#nc3-assembly-blocks-should-have-extensive-comments)] | Assembly blocks should have extensive comments | 5 | 
| [[NC&#x2011;4](#nc4-contract-declarations-should-have-natspec-author-annotations)] | Contract declarations should have NatSpec `@author` annotations | 36 | 
| [[NC&#x2011;5](#nc5-avoid-the-use-of-sensitive-terms)] | Avoid the use of sensitive terms | 1 | 
| [[NC&#x2011;6](#nc6-variable-names-that-consist-of-all-capital-letters-should-be-reserved-for-constant-immutable-variables)] | Variable names that consist of all capital letters should be reserved for `constant`/`immutable` variables | 38 | 
| [[NC&#x2011;7](#nc7-common-functions-should-be-refactored-to-a-common-base-contract)] | Common functions should be refactored to a common base contract | 6 | 
| [[NC&#x2011;8](#nc8-overly-complicated-arithmetic)] | Overly complicated arithmetic | 2 | 
| [[NC&#x2011;9](#nc9-constant-redefined-elsewhere)] | Constant redefined elsewhere | 36 | 
| [[NC&#x2011;10](#nc10-constants-in-comparisons-should-appear-on-the-left-side)] | Constants in comparisons should appear on the left side | 145 | 
| [[NC&#x2011;11](#nc11-const-variable-names-don-t-follow-the-solidity-style-guide)] | `const` Variable names don\'t follow the Solidity style guide | 1 | 
| [[NC&#x2011;12](#nc12-natspec-documentation-for-contract-is-missing)] | NatSpec documentation for `contract` is missing | 24 | 
| [[NC&#x2011;13](#nc13-contract-does-not-follow-the-solidity-style-guide-s-suggested-layout-ordering)] | Contract does not follow the Solidity style guide's suggested layout ordering | 8 | 
| [[NC&#x2011;14](#nc14-control-structures-do-not-follow-the-solidity-style-guide)] | Control structures do not follow the Solidity Style Guide | 163 | 
| [[NC&#x2011;15](#nc15-default-address-0-can-be-returned)] | Default address(0) can be returned | 3 | 
| [[NC&#x2011;16](#nc16-consider-using-delete-rather-than-assigning-zero-to-clear-values)] | Consider using `delete` rather than assigning `zero` to clear values | 11 | 
| [[NC&#x2011;17](#nc17-dependence-on-external-protocols)] | Dependence on external protocols | 1 | 
| [[NC&#x2011;18](#nc18-else-block-not-required)] | `else`-block not required | 21 | 
| [[NC&#x2011;19](#nc19-empty-bytes-check-is-missing)] | Empty bytes check is missing | 131 | 
| [[NC&#x2011;20](#nc20-events-are-missing-sender-information)] | Events are missing sender information | 39 | 
| [[NC&#x2011;21](#nc21-events-may-be-emitted-out-of-order-due-to-reentrancy)] | Events may be emitted out of order due to reentrancy | 12 | 
| [[NC&#x2011;22](#nc22-explicitly-define-visibility-of-state-variables-to-prevent-misconceptions-on-what-can-access-the-variable)] | Explicitly define visibility of state variables to prevent misconceptions on what can access the variable | 6 | 
| [[NC&#x2011;23](#nc23-defining-all-external-public-functions-in-contract-interfaces)] | Defining All External/Public Functions in Contract Interfaces | 52 | 
| [[NC&#x2011;24](#nc24-natspec-documentation-for-function-is-missing)] | NatSpec documentation for `function` is missing | 264 | 
| [[NC&#x2011;25](#nc25-function-ordering-does-not-follow-the-solidity-style-guide)] | Function ordering does not follow the Solidity style guide | 16 | 
| [[NC&#x2011;26](#nc26-array-indicies-should-be-referenced-via-enum-s-rather-than-via-numeric-literals)] | Array indicies should be referenced via `enum`s rather than via numeric literals | 2 | 
| [[NC&#x2011;27](#nc27-hardcoded-string-that-is-repeatedly-used-can-be-replaced-with-a-constant)] | Hardcoded string that is repeatedly used can be replaced with a constant | 5 | 
| [[NC&#x2011;28](#nc28-duplicated-require-checks-should-be-refactored-to-a-modifier-or-function)] | Duplicated `require()` checks should be refactored to a modifier or function | 4 | 
| [[NC&#x2011;29](#nc29-some-if-statement-can-be-converted-to-a-ternary)] | Some if-statement can be converted to a ternary | 24 | 
| [[NC&#x2011;30](#nc30-imports-could-be-organized-more-systematically)] | Imports could be organized more systematically | 4 | 
| [[NC&#x2011;31](#nc31-import-declarations-should-import-specific-identifiers-rather-than-the-whole-file)] | Import declarations should import specific identifiers, rather than the whole file | 96 | 
| [[NC&#x2011;32](#nc32-inconsistent-spacing-in-comments)] | Inconsistent spacing in comments | 1 | 
| [[NC&#x2011;33](#nc33-incorrect-natspec-syntax)] | Incorrect NatSpec Syntax | 7 | 
| [[NC&#x2011;34](#nc34-interfaces-should-be-defined-in-separate-files-from-their-usage)] | Interfaces should be defined in separate files from their usage | 2 | 
| [[NC&#x2011;35](#nc35-internal-functions-not-called-by-the-contract-should-be-removed)] | `internal` functions not called by the contract should be removed | 6 | 
| [[NC&#x2011;36](#nc36-large-numeric-literals-should-use-underscores-for-readability)] | Large numeric literals should use underscores for readability | 10 | 
| [[NC&#x2011;37](#nc37-long-functions-should-be-refactored-into-multiple-smaller-functions)] | Long functions should be refactored into multiple, smaller, functions | 25 | 
| [[NC&#x2011;38](#nc38-long-lines-of-code)] | Long lines of code | 128 | 
| [[NC&#x2011;39](#nc39-file-is-missing-natspec)] | File is missing NatSpec | 15 | 
| [[NC&#x2011;40](#nc40-mixed-usage-of-int-uint-with-int256-uint256)] | Mixed usage of `int`/`uint` with `int256`/`uint256` | 40 | 
| [[NC&#x2011;41](#nc41-consider-using-named-mappings)] | Consider using named mappings | 18 | 
| [[NC&#x2011;42](#nc42-consider-using-later-versions-of-solidity-for-more-cappabilities)] | Consider using later versions of solidity for more cappabilities | 39 | 
| [[NC&#x2011;43](#nc43-some-error-strings-are-not-descriptive)] | Some error strings are not descriptive | 4 | 
| [[NC&#x2011;44](#nc44-events-that-mark-critical-parameter-changes-should-contain-both-the-old-and-the-new-value)] | Events that mark critical parameter changes should contain both the old and the new value | 30 | 
| [[NC&#x2011;45](#nc45-override-function-arguments-that-are-unused-should-have-the-variable-name-removed-or-commented-out-to-avoid-compiler-warnings)] | `override` function arguments that are unused should have the variable name removed or commented out to avoid compiler warnings | 3 | 
| [[NC&#x2011;46](#nc46-use-of-override-is-unnecessary)] | Use of `override` is unnecessary | 102 | 
| [[NC&#x2011;47](#nc47-natspec-param-is-missing)] | NatSpec `@param` is missing | 46 | 
| [[NC&#x2011;48](#nc48-functions-which-are-either-private-or-internal-should-have-a-preceding-in-their-name)] | Functions which are either private or internal should have a preceding _ in their name | 5 | 
| [[NC&#x2011;49](#nc49-private-and-internal-state-variables-should-have-a-preceding-in-their-name-unless-they-are-constants)] | Private and internal state variables should have a preceding _ in their name unless they are constants | 11 | 
| [[NC&#x2011;50](#nc50-public-functions-not-called-by-the-contract-should-be-declared-external-instead)] | `public` functions not called by the contract should be declared `external` instead | 17 | 
| [[NC&#x2011;51](#nc51-adding-a-return-statement-when-the-function-defines-a-named-return-variable-is-redundant)] | Adding a `return` statement when the function defines a named return variable, is redundant | 15 | 
| [[NC&#x2011;52](#nc52-require-revert-statements-should-have-descriptive-reason-strings)] | `require()` / `revert()` statements should have descriptive reason strings | 14 | 
| [[NC&#x2011;53](#nc53-setters-should-prevent-re-setting-of-the-same-value)] | Setters should prevent re-setting of the same value | 14 | 
| [[NC&#x2011;54](#nc54-natspec-return-argument-is-missing)] | NatSpec `@return` argument is missing | 23 | 
| [[NC&#x2011;55](#nc55-polymorphic-functions-make-security-audits-more-time-consuming-and-error-prone)] | Polymorphic functions make security audits more time-consuming and error-prone | 3 | 
| [[NC&#x2011;56](#nc56-large-multiples-of-ten-should-use-scientific-notation-e-g-1e6-rather-than-decimal-literals-e-g-1000000-for-readability)] | Large multiples of ten should use scientific notation (e.g. `1e6`) rather than decimal literals (e.g. `1000000`), for readability | 5 | 
| [[NC&#x2011;57](#nc57-consider-moving-msg-sender-checks-to-a-common-authorization-modifier)] | Consider moving `msg.sender` checks to a common authorization `modifier` | 18 | 
| [[NC&#x2011;58](#nc58-empty-receive-payable-fallback-function-does-not-authorize-requests)] | Empty `receive()`/`payable fallback()` function does not authorize requests | 1 | 
| [[NC&#x2011;59](#nc59-state-variables-should-have-natspec-comments)] | State variables should have `Natspec` comments | 155 | 
| [[NC&#x2011;60](#nc60-contracts-should-have-full-test-coverage)] | Contracts should have full test coverage | 1 | 
| [[NC&#x2011;61](#nc61-numeric-values-having-to-do-with-time-should-use-time-units-for-readability)] | Numeric values having to do with time should use time units for readability | 8 | 
| [[NC&#x2011;62](#nc62-contract-declarations-should-have-natspec-title-annotations)] | Contract declarations should have NatSpec `@title` annotations | 30 | 
| [[NC&#x2011;63](#nc63-open-todos)] | Open TODOs | 1 | 
| [[NC&#x2011;64](#nc64-top-level-pragma-declarations-should-be-separated-by-two-blank-lines)] | Top level pragma declarations should be separated by two blank lines | 41 | 
| [[NC&#x2011;65](#nc65-critical-functions-should-be-a-two-step-procedure)] | Critical functions should be a two step procedure | 17 | 
| [[NC&#x2011;66](#nc66-typos)] | Typos | 5 | 
| [[NC&#x2011;67](#nc67-uint-variables-should-have-the-bit-size-defined-explicitly)] | uint variables should have the bit size defined explicitly | 36 | 
| [[NC&#x2011;68](#nc68-uncommented-fields-in-a-struct)] | Uncommented fields in a struct | 26 | 
| [[NC&#x2011;69](#nc69-event-is-missing-indexed-fields)] | Event is missing `indexed` fields | 42 | 
| [[NC&#x2011;70](#nc70-unused-import)] | Unused Import | 19 | 
| [[NC&#x2011;71](#nc71-unused-parameter)] | Unused parameter | 9 | 
| [[NC&#x2011;72](#nc72-unused-internal-private-contract-variable)] | Unused `internal`/`private` contract variable | 2 | 
| [[NC&#x2011;73](#nc73-cast-to-bytes-or-bytes32-for-clearer-semantic-meaning)] | Cast to `bytes` or `bytes32` for clearer semantic meaning | 1 | 
| [[NC&#x2011;74](#nc74-use-bytes-concat-on-bytes-instead-of-abi-encodepacked-for-clearer-semantic-meaning)] | Use `bytes.concat()` on bytes instead of `abi.encodePacked()` for clearer semantic meaning | 2 | 
| [[NC&#x2011;75](#nc75-use-string-concat-on-strings-instead-of-abi-encodepacked-for-clearer-semantic-meaning)] | Use `string.concat()` on strings instead of `abi.encodePacked()` for clearer semantic meaning | 2 | 
| [[NC&#x2011;76](#nc76-constants-should-be-defined-rather-than-using-magic-numbers)] | Constants should be defined rather than using magic numbers | 6 | 
| [[NC&#x2011;77](#nc77-use-the-latest-solidity-prior-to-0-8-20-if-on-l2s-for-deployment)] | Use the latest solidity (prior to 0.8.20 if on L2s) for deployment | 39 | 
| [[NC&#x2011;78](#nc78-use-openzeppelin-s-or-solady-s-ownable-rather-than-re-inventing-the-wheel)] | Use OpenZeppelin's or Solady's Ownable, rather than re-inventing the wheel | 1 | 
| [[NC&#x2011;79](#nc79-use-openzeppelin-s-reentrancyguard-reentrancyguardupgradeable-rather-than-writing-your-own)] | Use OpenZeppelin's `ReentrancyGuard` / `ReentrancyGuardUpgradeable` rather than writing your own | 1 | 
| [[NC&#x2011;80](#nc80-use-a-single-file-for-system-wide-constants)] | Use a single file for system wide constants | 14 | 
| [[NC&#x2011;81](#nc81-consider-using-smtchecker)] | Consider using SMTChecker | 39 | 
| [[NC&#x2011;82](#nc82-variable-name-must-be-in-mixedcase)] | Variable name must be in mixedCase | 2 | 
| [[NC&#x2011;83](#nc83-whitespace-in-expressions)] | Whitespace in Expressions | 32 | 
| [[NC&#x2011;84](#nc84-complex-function-controle-flow)] | Complex function controle flow | 4 | 
| [[NC&#x2011;85](#nc85-consider-bounding-input-array-length)] | Consider bounding input array length | 3 | 
| [[NC&#x2011;86](#nc86-a-function-which-defines-named-returns-in-it-s-declaration-doesn-t-need-to-use-return)] | A function which defines named returns in it's declaration doesn't need to use return | 11 | 
| [[NC&#x2011;87](#nc87-contract-declarations-should-have-natspec-dev-annotations)] | Contract declarations should have NatSpec `@dev` annotations | 30 | 
| [[NC&#x2011;88](#nc88-contract-should-expose-an-interface)] | Contract should expose an `interface` | 81 | 
| [[NC&#x2011;89](#nc89-named-imports-of-parent-contracts-are-missing)] | Named imports of parent contracts are missing | 1 | 
| [[NC&#x2011;90](#nc90-contract-declarations-should-have-natspec-notice-annotations)] | Contract declarations should have NatSpec `@notice` annotations | 28 | 
| [[NC&#x2011;91](#nc91-do-not-use-underscore-in-struct-elements-names)] | Do not use UNDERSCORE in `struct` elements names | 3 | 
| [[NC&#x2011;92](#nc92-event-declarations-should-have-natspec-descriptions)] | `event` declarations should have NatSpec descriptions | 55 | 
| [[NC&#x2011;93](#nc93-events-should-use-parameters-to-convey-information)] | Events should use parameters to convey information | 2 | 
| [[NC&#x2011;94](#nc94-function-names-should-use-lowercamelcase)] | `function` names should use lowerCamelCase | 23 | 
| [[NC&#x2011;95](#nc95-expressions-for-constant-values-should-use-immutable-rather-than-constant)] | Expressions for constant values should use `immutable` rather than `constant` | 5 | 
| [[NC&#x2011;96](#nc96-struct-names-should-use-camelcase)] | `struct` names should use CamelCase | 3 | 
| [[NC&#x2011;97](#nc97-immutable-variable-names-don-t-follow-the-solidity-style-guide)] | `immutable` variable names don\'t follow the Solidity style guide | 44 | 
| [[NC&#x2011;98](#nc98-private-public-function-name-should-start-with-underscore)] | `private`/`public` function name should start with underscore | 5 | 
| [[NC&#x2011;99](#nc99-natspec-modifier-declarations-should-have-descriptions)] | NatSpec: `Modifier` declarations should have descriptions | 3 | 
| [[NC&#x2011;100](#nc100-pure-function-accesses-storage)] | `pure` function accesses storage | 1 | 
| [[NC&#x2011;101](#nc101-assembly-block-creates-dirty-bits)] | Assembly block creates dirty bits | 3 | 

Total: 2772 instances over 101 issues

## Low Risk Issues

### [L&#x2011;1] Vulnerable versions of packages are being used 
This project's specific package versions are vulnerable to the specific CVEs listed below. Consider switching to more recent versions of these packages that don't have these vulnerabilities


*There are 1 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: package.json


<details><summary>Vulnerabilities related to `@openzeppelin/contracts`:</summary>


- [CVE-2023-34459](https://github.com/OpenZeppelin/openzeppelin-contracts/security/advisories/GHSA-wprv-93r4-jj2p) :When the verifyMultiProof, verifyMultiProofCalldata, processMultiProof, or processMultiProofCalldata functions are in use, it is possible to construct merkle trees that allow forging a valid multiproof for an arbitrary set of leaves.
A contract may be vulnerable if it uses multiproofs for verification and the merkle tree that is processed includes a node with value 0 at depth 1(just under the root).This could happen inadvertently for balanced trees with 3 leaves or less, if the leaves are not hashed.This could happen deliberately if a malicious tree builder includes such a node in the tree.
A contract is not vulnerable if it uses single- leaf proving(verify, verifyCalldata, processProof, or processProofCalldata), or if it uses multiproofs with a known tree that has hashed leaves.Standard merkle trees produced or validated with the @openzeppelin/merkle-tree library are safe.


- [CVE-2023-34234](https://github.com/OpenZeppelin/openzeppelin-contracts/security/advisories/GHSA-5h3x-9wvq-w4m2) :By frontrunning the creation of a proposal, an attacker can become the proposer and gain the ability to cancel it. The attacker can do this repeatedly to try to prevent a proposal from being proposed at all.
This impacts the Governor contract in v4.9.0 only, and the GovernorCompatibilityBravo contract since v4.3.0.


- [CVE-2023-30541](https://github.com/OpenZeppelin/openzeppelin-contracts/security/advisories/GHSA-mx2q-35m2-x2rh) :A function in the implementation contract may be inaccessible if its selector clashes with one of the proxy's own selectors. Specifically, if the clashing function has a different signature with incompatible ABI encoding, the proxy could revert while attempting to decode the arguments from calldata.
The probability of an accidental clash is negligible, but one could be caused deliberately.


- [CVE-2023-30542](https://github.com/OpenZeppelin/openzeppelin-contracts/security/advisories/GHSA-93hq-5wgc-jc82) :The proposal creation entrypoint (propose) in GovernorCompatibilityBravo allows the creation of proposals with a signatures array shorter than the calldatas array. This causes the additional elements of the latter to be ignored, and if the proposal succeeds the corresponding actions would eventually execute without any calldata. The ProposalCreated event correctly represents what will eventually execute, but the proposal parameters as queried through getActions appear to respect the original intended calldata.
</details>
1: 


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//package.json#L1-L1) 


</details>


### [L&#x2011;2] Missing checks for `address(0)` when assigning values to address state variables 



*There are 27 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/ActivePool.sol

53:         borrowerOperationsAddress = _borrowerOperationsAddress;

54:         cdpManagerAddress = _cdpManagerAddress;

56:         collSurplusPoolAddress = _collSurplusAddress;

57:         feeRecipientAddress = _feeRecipientAddress;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L53-L53) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L54-L54), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L56-L56), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L57-L57)


```solidity

File: packages/contracts/contracts/BorrowerOperations.sol

121:         feeRecipientAddress = _feeRecipientAddress;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L121-L121) 


```solidity

File: packages/contracts/contracts/CdpManagerStorage.sol

229:         liquidationLibrary = _liquidationLibraryAddress;

233:         borrowerOperationsAddress = _borrowerOperationsAddress;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L229-L229) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L233-L233)


```solidity

File: packages/contracts/contracts/CollSurplusPool.sol

48:         borrowerOperationsAddress = _borrowerOperationsAddress;

49:         cdpManagerAddress = _cdpManagerAddress;

50:         activePoolAddress = _activePoolAddress;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L48-L48) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L49-L49), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L50-L50)


```solidity

File: packages/contracts/contracts/Dependencies/Auth.sol

19:         owner = _owner;

20:         authority = _authority;

47:         authority = newAuthority;

53:         owner = newOwner;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/Auth.sol#L19-L19) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/Auth.sol#L20-L20), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/Auth.sol#L47-L47), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/Auth.sol#L53-L53)


```solidity

File: packages/contracts/contracts/EBTCToken.sol

68:         cdpManagerAddress = _cdpManagerAddress;

69:         borrowerOperationsAddress = _borrowerOperationsAddress;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L68-L68) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L69-L69)


```solidity

File: packages/contracts/contracts/LeverageMacroFactory.sol

29:         borrowerOperations = _borrowerOperationsAddress;

30:         activePool = _activePool;

31:         cdpManager = _cdpManager;

32:         ebtcToken = _ebtc;

33:         stETH = _coll;

34:         sortedCdps = _sortedCdps;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroFactory.sol#L29-L29) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroFactory.sol#L30-L30), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroFactory.sol#L31-L31), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroFactory.sol#L32-L32), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroFactory.sol#L33-L33), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroFactory.sol#L34-L34)


```solidity

File: packages/contracts/contracts/LeverageMacroReference.sol

36:         theOwner = _owner;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroReference.sol#L36-L36) 


```solidity

File: packages/contracts/contracts/PriceFeed.sol

377:                     fallbackCaller = newFallbackCaler;

386:             fallbackCaller = newFallbackCaler;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L377-L377) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L386-L386)


```solidity

File: packages/contracts/contracts/SimplifiedDiamondLike.sol

45:         owner = _owner;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L45-L45) 


```solidity

File: packages/contracts/contracts/SortedCdps.sol

96:         borrowerOperationsAddress = _borrowerOperationsAddress;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L96-L96) 


</details>


### [L&#x2011;3] For loops in public or external functions should be avoided due to high gas costs and possible DOS 
In Solidity, for loops can potentially cause Denial of Service (DoS) attacks if not handled carefully. DoS attacks can occur when an attacker intentionally exploits the gas cost of a function, causing it to run out of gas or making it too expensive for other users to call. Below are some scenarios where for loops can lead to DoS attacks: Nested for loops can become exceptionally gas expensive and should be used sparingly


*There are 11 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/Governor.sol

43:     function getUsersByRole(uint8 role) external view returns (address[] memory usersWithRole) {
44:         // Search over all users: O(n) * 2
45:         uint256 count;
46:         for (uint256 i = 0; i < users.length(); i++) {

43:     function getUsersByRole(uint8 role) external view returns (address[] memory usersWithRole) {
44:         // Search over all users: O(n) * 2
45:         uint256 count;
46:         for (uint256 i = 0; i < users.length(); i++) {
47:             address user = users.at(i);
48:             bool _canCall = doesUserHaveRole(user, role);
49:             if (_canCall) {
50:                 count += 1;
51:             }
52:         }
53:         if (count > 0) {
54:             uint256 j = 0;
55:             usersWithRole = new address[](count);
56:             address[] memory _usrs = users.values();
57:             for (uint256 i = 0; i < _usrs.length; i++) {

73:     function getRolesForUser(address user) external view returns (uint8[] memory rolesForUser) {
74:         // Enumerate over all possible roles and check if enabled
75:         uint256 count;
76:         for (uint8 i = 0; i < type(uint8).max; i++) {

73:     function getRolesForUser(address user) external view returns (uint8[] memory rolesForUser) {
74:         // Enumerate over all possible roles and check if enabled
75:         uint256 count;
76:         for (uint8 i = 0; i < type(uint8).max; i++) {
77:             if (doesUserHaveRole(user, i)) {
78:                 count += 1;
79:             }
80:         }
81:         if (count > 0) {
82:             uint256 j = 0;
83:             rolesForUser = new uint8[](count);
84:             for (uint8 i = 0; i < type(uint8).max; i++) {

96:     function getRolesFromByteMap(bytes32 byteMap) public pure returns (uint8[] memory roleIds) {
97:         uint256 count;
98:         for (uint8 i = 0; i < type(uint8).max; i++) {

096:     function getRolesFromByteMap(bytes32 byteMap) public pure returns (uint8[] memory roleIds) {
097:         uint256 count;
098:         for (uint8 i = 0; i < type(uint8).max; i++) {
099:             bool roleEnabled = (uint256(byteMap >> i) & 1) != 0;
100:             if (roleEnabled) {
101:                 count += 1;
102:             }
103:         }
104:         if (count > 0) {
105:             uint256 j = 0;
106:             roleIds = new uint8[](count);
107:             for (uint8 i = 0; i < type(uint8).max; i++) {

120:     function getByteMapFromRoles(uint8[] memory roleIds) public pure returns (bytes32) {
121:         bytes32 _data;
122:         for (uint8 i = 0; i < roleIds.length; i++) {

131:     function getEnabledFunctionsInTarget(
132:         address _target
133:     ) public view returns (bytes4[] memory _funcs) {
134:         bytes32[] memory _sigs = enabledFunctionSigsByTarget[_target].values();
135:         if (_sigs.length > 0) {
136:             _funcs = new bytes4[](_sigs.length);
137:             for (uint256 i = 0; i < _sigs.length; ++i) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L43-L46) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L43-L57), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L73-L76), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L73-L84), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L96-L98), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L96-L107), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L120-L122), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L131-L137)


```solidity

File: packages/contracts/contracts/SimplifiedDiamondLike.sol

110:     function execute(Operation[] calldata ops) external payable {
111:         require(msg.sender == owner, "Must be owner");
112: 
113:         uint256 length = ops.length;
114:         for (uint256 i; i < length; ) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L110-L114) 


```solidity

File: packages/contracts/contracts/SortedCdps.sol

419:     function batchRemove(bytes32[] memory _ids) external override {
420:         _requireCallerIsCdpManager();
421:         uint256 _len = _ids.length;
422:         require(_len > 1, "SortedCdps: batchRemove() only apply to multiple cdpIds!");
423: 
424:         bytes32 _firstPrev = data.nodes[_ids[0]].prevId;
425:         bytes32 _lastNext = data.nodes[_ids[_len - 1]].nextId;
426: 
427:         require(
428:             _firstPrev != dummyId || _lastNext != dummyId,
429:             "SortedCdps: batchRemove() leave ZERO node left!"
430:         );
431: 
432:         for (uint256 i = 0; i < _len; ++i) {

419:     function batchRemove(bytes32[] memory _ids) external override {
420:         _requireCallerIsCdpManager();
421:         uint256 _len = _ids.length;
422:         require(_len > 1, "SortedCdps: batchRemove() only apply to multiple cdpIds!");
423: 
424:         bytes32 _firstPrev = data.nodes[_ids[0]].prevId;
425:         bytes32 _lastNext = data.nodes[_ids[_len - 1]].nextId;
426: 
427:         require(
428:             _firstPrev != dummyId || _lastNext != dummyId,
429:             "SortedCdps: batchRemove() leave ZERO node left!"
430:         );
431: 
432:         for (uint256 i = 0; i < _len; ++i) {
433:             require(contains(_ids[i]), "SortedCdps: List does not contain the id");
434:         }
435: 
436:         // orphan nodes in between to save gas
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
447: 
448:         // delete node & owner storages to get gas refund
449:         for (uint i = 0; i < _len; ++i) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L419-L432) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L419-L449)


</details>


### [L&#x2011;4] Missing checks in constructor/initialize 
There are some missing checks in these functions, and this could lead to unexpected scenarios. Consider always adding a sanity check for state variables.


*There are 1 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

//@audit _sweepToCaller,  are not checked
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

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L51-L59) 


</details>


### [L&#x2011;5] `external` calls in an un-bounded loop may result in a DOS 
Consider limiting the number of iterations in loops that make external calls


*There are 14 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/CdpManager.sol

370:                 _cId = sortedCdps.getPrev(_cId);

371:                 currentBorrower = sortedCdps.getOwnerAddress(_cId);

424:                 bytes32 _nextId = sortedCdps.getPrev(_cId);

425:                 address nextUserToCheck = sortedCdps.getOwnerAddress(_nextId);

500:             _id = sortedCdps.getNext(_id);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L370-L370) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L371-L371), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L424-L424), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L425-L425), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L500-L500)


```solidity

File: packages/contracts/contracts/HintHelpers.sol

72:                 vars.currentCdpId = sortedCdps.getPrev(vars.currentCdpId);

73:                 vars.currentCdpUser = sortedCdps.getOwnerAddress(vars.currentCdpId);

90:                 uint256 currentCdpDebt = cdpManager.getSyncedCdpDebt(vars.currentCdpId);

102:                         collateral.getPooledEthByShares(partialRedemptionNewColl) <

116:                 vars.currentCdpId = sortedCdps.getPrev(vars.currentCdpId);

117:                 vars.currentCdpUser = sortedCdps.getOwnerAddress(vars.currentCdpId);

185:             bytes32 _cId = cdpManager.getIdFromCdpIdsArray(arrayIndex);

186:             uint256 currentNICR = cdpManager.getSyncedNominalICR(_cId);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L72-L72) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L73-L73), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L90-L90), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L102-L102), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L116-L116), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L117-L117), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L185-L185), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L186-L186)


```solidity

File: packages/contracts/contracts/LeverageMacroBase.sol

441:                     IERC20(swapChecks[i].tokenToCheck).balanceOf(address(this)) >


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L441-L441) 


</details>


### [L&#x2011;6] `internal` Function calls within for loops 
Making function calls or external calls within loops in Solidity can lead to inefficient gas usage, potential bottlenecks, and increased vulnerability to attacks. Each function call or external call consumes gas, and when executed within a loop, the gas cost multiplies, potentially causing the transaction to run out of gas or exceed block gas limits. This can result in transaction failure or unpredictable behavior.


*There are 17 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/CdpManager.sol

403:                 SingleRedemptionValues memory singleRedemption = _redeemCollateralFromCdp(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L403-L403) 


```solidity

File: packages/contracts/contracts/Dependencies/EbtcMath.sol

75:                 x = decMul(x, x);

79:                 y = decMul(x, y);

80:                 x = decMul(x, x);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcMath.sol#L75-L75) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcMath.sol#L79-L79), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcMath.sol#L80-L80)


```solidity

File: packages/contracts/contracts/HintHelpers.sol

98:                     ) = _calculateCdpStateAfterPartialRedemption(vars, currentCdpDebt, _price);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L98-L98) 


```solidity

File: packages/contracts/contracts/LeverageMacroBase.sol

386:             _doSwap(swapData[i]);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L386-L386) 


```solidity

File: packages/contracts/contracts/LiquidationLibrary.sol

765:                     _getLiquidationValuesRecoveryMode(

781:                     totals = _addLiquidationValuesToTotals(totals, singleLiquidation);

792:                     _getLiquidationValuesNormalMode(_price, _TCR, vars, singleLiquidation);

795:                     totals = _addLiquidationValuesToTotals(totals, singleLiquidation);

824:                     _getLiquidationValuesNormalMode(_price, _TCR, vars, singleLiquidation);

827:                     totals = _addLiquidationValuesToTotals(totals, singleLiquidation);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L765-L765) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L781-L781), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L792-L792), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L795-L795), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L824-L824), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L827-L827)


```solidity

File: packages/contracts/contracts/SimplifiedDiamondLike.sol

115:             _executeOne(ops[i]);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L115-L115) 


```solidity

File: packages/contracts/contracts/SortedCdps.sol

187:             if (getOwnerAddress(_currentCdpId) == owner) {

250:             if (getOwnerAddress(_currentCdpId) == owner) {

320:             if (getOwnerAddress(_currentCdpId) == owner) {

433:             require(contains(_ids[i]), "SortedCdps: List does not contain the id");


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L187-L187) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L250-L250), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L320-L320), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L433-L433)


</details>


### [L&#x2011;7] Loss of precision 
Division by large numbers may result in the result being zero, due to solidity not supporting fractions. Consider requiring a minimum amount for the numerator to ensure that it is always larger than the denominator


*There are 13 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/CdpManager.sol

146:             (singleRedemption.debtToRedeem * DECIMAL_PRECISION) / _redeemColFromCdp.price

621:         uint256 redeemedEBTCFraction = (collateral.getPooledEthByShares(_ETHDrawn) * _price) /

624:         uint256 newBaseRate = decayedBaseRate + (redeemedEBTCFraction / beta);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L146-L146) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L621-L621), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L624-L624)


```solidity

File: packages/contracts/contracts/CdpManagerStorage.sol

567:         uint256 _deltaFeePerUnit = _deltaFeeSplitShare / _cachedAllStakes;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L567-L567) 


```solidity

File: packages/contracts/contracts/Dependencies/EbtcBase.sol

108:         uint256 feePercentage = (_fee * DECIMAL_PRECISION) / _amount;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L108-L108) 


```solidity

File: packages/contracts/contracts/HintHelpers.sol

145:             (maxRedeemableEBTC * DECIMAL_PRECISION) / _price


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L145-L145) 


```solidity

File: packages/contracts/contracts/LiquidationLibrary.sol

278:         uint _debtToColl = (_totalDebtToBurn * DECIMAL_PRECISION) / _liqState.price;

365:         uint _debtToColl = (_totalDebtToBurn * DECIMAL_PRECISION) / _recoveryState.price;

435:             uint _debtToColl = (_partialDebt * DECIMAL_PRECISION) / _partialState.price;

555:             _incentiveColl = (_totalDebtToBurn * (_ICR > MCR ? MCR : _ICR)) / _price;

558:             _incentiveColl = (_totalDebtToBurn * LICR) / _price;

579:             _incentiveColl = (_totalDebtToBurn * (_ICR > MCR ? MCR : _ICR)) / _price;

882:         uint256 EBTCDebtRewardPerUnitStaked = EBTCDebtNumerator / _totalStakes;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L278-L278) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L365-L365), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L435-L435), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L555-L555), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L558-L558), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L579-L579), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L882-L882)


</details>


### [L&#x2011;8] `require()` should be used instead of `assert()` 
Prior to solidity version 0.8.0, hitting an assert consumes the ** remainder of the transaction's available gas** rather than returning it, as `require()` / `revert()` do. `assert()` should be avoided even past solidity version 0.8.0 as its[documentation](https://docs.soliditylang.org/en/v0.8.14/control-structures.html#panic-via-assert-and-error-via-require) states that "The assert function creates an error of type Panic(uint256). ... Properly functioning code should never create a Panic, not even on invalid external input. If this happens, then there is a bug in your contract which you should fix".


*There are 1 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

564:         assert(toLiquidator < _totalColToSend); // Assert is correct here for Echidna


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L564-L564) 


</details>


### [L&#x2011;9] Consider using OpenZeppelin’s SafeCast library to prevent unexpected overflows when casting from various type int/uint values 



*There are 5 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/ActivePool.sol

//@audit `_newFee` is getting converted from `uint256` to `uint16`
411:         feeBps = uint16(_newFee);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L411-L411) 


```solidity

File: packages/contracts/contracts/BorrowerOperations.sol

//@audit `_newFee` is getting converted from `uint256` to `uint16`
1161:         feeBps = uint16(_newFee);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L1161-L1161) 


```solidity

File: packages/contracts/contracts/PriceFeed.sol

//@audit `_ethBtcAnswer` is getting converted from `int256` to `uint256`
802:                 uint256(_ethBtcAnswer) *

//@audit `_stEthEthAnswer` is getting converted from `int256` to `uint256`
803:                 uint256(_stEthEthAnswer) *


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L802-L802) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L803-L803)


```solidity

File: packages/contracts/contracts/SortedCdps.sol

//@audit `_tmp` is getting converted from `uint256` to `uint160`
125:         return address(uint160(_tmp));


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L125-L125) 


</details>


### [L&#x2011;10] Setters should have initial value check 
Setters should have initial value check to prevent assigning wrong value to the variable. Assginment of wrong value can lead to unexpected behavior of the contract.


*There are 10 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/ActivePool.sol

417:     function setFlashLoansPaused(bool _paused) external requiresAuth {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L417-L417) 


```solidity

File: packages/contracts/contracts/BorrowerOperations.sol

628:     function setPositionManagerApproval(

1167:     function setFlashLoansPaused(bool _paused) external requiresAuth {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L628-L628) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L1167-L1167)


```solidity

File: packages/contracts/contracts/CdpManager.sol

523:     function updateStakeAndTotalStakes(bytes32 _cdpId) external override returns (uint256) {

830:     function setBeta(uint256 _beta) external requiresAuth {

843:     function setRedemptionsPaused(bool _paused) external requiresAuth {

946:     function updateCdp(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L523-L523) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L830-L830), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L843-L843), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L946-L946)


```solidity

File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

38:     function setAuthority(address newAuthority) public virtual {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L38-L38) 


```solidity

File: packages/contracts/contracts/Governor.sol

154:     function setRoleName(uint8 role, string memory roleName) external requiresAuth {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L154-L154) 


```solidity

File: packages/contracts/contracts/LeverageMacroReference.sol

50:     function resetApprovals() external {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroReference.sol#L50-L50) 


</details>


### [L&#x2011;11] Sweeping may break accounting if tokens with multiple addresses are used 
There have been [cases](https://blog.openzeppelin.com/compound-tusd-integration-issue-retrospective/) in the past where a token mistakenly had two addresses that could control its balance, and transfers using one address impacted the balance of the other. To protect against this potential scenario, sweep functions should ensure that the balance of the non-sweepable token does not change after the transfer of the swept tokens.


*There are 3 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/ActivePool.sol

371:     function sweepToken(address token, uint256 amount) public nonReentrant requiresAuth {
372:         ICdpManagerData(cdpManagerAddress).syncGlobalAccountingAndGracePeriod(); // Accrue State First
373: 
374:         require(token != address(collateral), "ActivePool: Cannot Sweep Collateral");
375: 
376:         uint256 balance = IERC20(token).balanceOf(address(this));
377:         require(amount <= balance, "ActivePool: Attempt to sweep more than balance");
378: 
379:         address cachedFeeRecipientAddress = feeRecipientAddress; // Saves an SLOAD
380: 
381:         IERC20(token).safeTransfer(cachedFeeRecipientAddress, amount);
382: 
383:         emit SweepTokenSuccess(token, amount, cachedFeeRecipientAddress);
384:     }


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L371-L384) 


```solidity

File: packages/contracts/contracts/CollSurplusPool.sol

142:     function sweepToken(address token, uint256 amount) public nonReentrant requiresAuth {
143:         require(token != address(collateral), "CollSurplusPool: Cannot Sweep Collateral");
144: 
145:         uint256 balance = IERC20(token).balanceOf(address(this));
146:         require(amount <= balance, "CollSurplusPool: Attempt to sweep more than balance");
147: 
148:         IERC20(token).safeTransfer(feeRecipientAddress, amount);
149: 
150:         emit SweepTokenSuccess(token, amount, feeRecipientAddress);
151:     }


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L142-L151) 


```solidity

File: packages/contracts/contracts/LeverageMacroBase.sol

234:     function sweepToken(address token, uint256 amount) public {
235:         _assertOwner();
236: 
237:         IERC20(token).safeTransfer(msg.sender, amount);
238:     }


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L234-L238) 


</details>


### [L&#x2011;12] Int casting `block.timestamp` can reduce the lifespan of a contract 
Consider removing casting to ensure future functionality.


*There are 1 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

53:             lastGracePeriodStartTimestamp = uint128(block.timestamp);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L53-L53) 


</details>


### [L&#x2011;13] Unused/empty `receive()`/`fallback()` function 
If the intention is for the Ether to be used, the function should call another function or emit an event, otherwise it should revert.


*There are 1 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

160:     receive() external payable {
161:         // PHP is my favourite language
162:     }


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L160-L162) 


</details>


### [L&#x2011;14] Consider implementing two-step procedure for updating protocol addresses 
A copy-paste error or a typo may end up bricking protocol functionality, or sending tokens to an address with no known private key. Consider implementing a two-step procedure for updating protocol addresses, where the recipient is set as pending, and must 'accept' the assignment by making an affirmative call. A straight forward way of doing this would be to have the target contracts implement [EIP-165](https://eips.ethereum.org/EIPS/eip-165), and to have the 'set' functions ensure that the recipient is of the right interface type.


*There are 2 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

42:     function setAuthority(Authority newAuthority) public virtual {
43:         // We check if the caller is the owner first because we want to ensure they can
44:         // always swap out the authority even if it's reverting or using up a lot of gas.
45:         require(msg.sender == owner || authority.canCall(msg.sender, address(this), msg.sig));
46: 
47:         authority = newAuthority;
48: 
49:         emit AuthorityUpdated(msg.sender, newAuthority);
50:     }


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/Auth.sol#L42-L50) 


```solidity

File: packages/contracts/contracts/SimplifiedDiamondLike.sol

51:     function setFallbackHandler(bytes4 sig, address handler) external {
52:         require(msg.sender == owner);
53: 
54:         // NOTE: We prob don't need this due to how solidity works
55:         // "execute((address,bool,uint128,uint128,bool,uint8,bytes)[])": "94b24d09"
56:         require(sig != 0x94b24d09);
57: 
58:         DiamondLikeStorage storage s = _getStorage();
59: 
60:         s.callbackHandler[sig] = handler;
61:     }


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L51-L61) 


</details>


### [L&#x2011;15] `safeApprove()` is deprecated 
[Deprecated](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/bfff03c0d2a59bcd8e2ead1da9aed9edf0080d05/contracts/token/ERC20/utils/SafeERC20.sol#L38-L45) in favor of `safeIncreaseAllowance()` and `safeDecreaseAllowance()`. If only setting the initial allowance to the value that means infinite, `safeIncreaseAllowance()` can be used instead. The function may currently work, but if a bug is found in this version of OpenZeppelin, and the version that you're forced to upgrade to no longer has this function, you'll encounter unnecessary delays in porting and testing replacement contracts.


*There are 2 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

405:         IERC20(swapData.tokenForSwap).safeApprove(

427:         IERC20(swapData.tokenForSwap).safeApprove(swapData.addressForApprove, 0);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L405-L405) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L427-L427)


</details>


### [L&#x2011;16] Consider using descriptive `constant`s when passing zero as a function argument 
Passing zero as a function argument can sometimes result in a security issue (e.g. passing zero as the slippage parameter). Consider using a `constant` variable with a descriptive name, so it's clear that the argument is intentionally being used, and for the right reasons.


*There are 9 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

//@audit parameter number 7 starting from left
225:         _adjustCdpInternal(_cdpId, _stEthBalanceDecrease, 0, false, _upperHint, _lowerHint, 0);

//@audit parameter number 7 starting from left
241:         _adjustCdpInternal(_cdpId, 0, _debt, true, _upperHint, _lowerHint, 0);

//@audit parameter number 7 starting from left
256:         _adjustCdpInternal(_cdpId, 0, _debt, false, _upperHint, _lowerHint, 0);

//@audit parameter number 7 starting from left
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

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L225-L225) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L241-L241), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L256-L256), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L278-L286)


```solidity

File: packages/contracts/contracts/CdpManager.sol

//@audit parameter number 2 starting from left
171:                 _closeCdpByRedemption(
172:                     _redeemColFromCdp.cdpId,
173:                     0,
174:                     newColl,
175:                     _liquidatorRewardShares,
176:                     _borrower
177:                 );


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L171-L177) 


```solidity

File: packages/contracts/contracts/LeverageMacroBase.sol

//@audit parameter number 3 starting from left
414:         (bool success, ) = excessivelySafeCall(
415:             swapData.addressForSwap,
416:             gasleft(),
417:             0,
418:             0,
419:             swapData.calldataForSwap
420:         );

//@audit parameter number 4 starting from left
414:         (bool success, ) = excessivelySafeCall(
415:             swapData.addressForSwap,
416:             gasleft(),
417:             0,
418:             0,
419:             swapData.calldataForSwap
420:         );

//@audit parameter number 2 starting from left
427:         IERC20(swapData.tokenForSwap).safeApprove(swapData.addressForApprove, 0);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L414-L420) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L414-L420), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L427-L427)


```solidity

File: packages/contracts/contracts/LiquidationLibrary.sol

//@audit parameter number 2 starting from left
41:         _liquidateIndividualCdpSetup(_cdpId, 0, _cdpId, _cdpId);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L41-L41) 


</details>


### [L&#x2011;17] Functions calling contracts/addresses with transfer hooks are missing reentrancy guards 
Even if the function follows the best practice of check-effects-interaction, not using a reentrancy guard when there may be transfer hooks will open the users of this protocol up to [read-only reentrancies](https://chainsecurity.com/curve-lp-oracle-manipulation-post-mortem/) with no way to protect against it, except by block-listing the whole protocol.


*There are 5 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/ActivePool.sol

//@audit function `flashLoan()` is not protected against reentrancy
274:         collateral.transfer(address(receiver), amount);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L274-L274) 


```solidity

File: packages/contracts/contracts/BorrowerOperations.sol

//@audit function `flashLoan()` is not protected against reentrancy
1100:         ebtcToken.transferFrom(address(receiver), feeRecipientAddress, fee + amount);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L1100-L1100) 


```solidity

File: packages/contracts/contracts/LeverageMacroBase.sol

//@audit function `doOperation()` is not protected against reentrancy
129:             IERC20(operation.tokenToTransferIn).safeTransferFrom(

//@audit function `sweepToCaller()` is not protected against reentrancy
224:             ebtcToken.transfer(msg.sender, ebtcBal);

//@audit function `sweepToken()` is not protected against reentrancy
237:         IERC20(token).safeTransfer(msg.sender, amount);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L129-L129) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L224-L224), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L237-L237)


</details>


### [L&#x2011;18] Some function should not be marked as payable 
Some function should not be marked as payable, otherwise the ETH that mistakenly sent along with the function call is locked in the contract


*There are 3 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

110:     function execute(Operation[] calldata ops) external payable {
111:         require(msg.sender == owner, "Must be owner");
112: 
113:         uint256 length = ops.length;
114:         for (uint256 i; i < length; ) {
115:             _executeOne(ops[i]);
116: 
117:             unchecked {
118:                 ++i;
119:             }
120:         }
121: 
122:         // Toggle `callbackEnabledForCall` to false
123:         // NOTE: We could check calldata to see if this has to be done, but this is fine for a reference impl
124:         // Even if no-op, this ensures we never allow a callback if in that mode
125:         _setCallbackEnabledForCall(_getStorage(), false);
126:     }

160:     receive() external payable {
161:         // PHP is my favourite language
162:     }

164:     fallback() external payable {
165:         _fallback();
166:     }


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L110-L126) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L160-L162), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L164-L166)


</details>


### [L&#x2011;19] Code does not follow the best practice of check-effects-interaction 
Code should follow the best-practice of [check-effects-interaction](https://blockchain-academy.hs-mittweida.de/courses/solidity-coding-beginners-to-intermediate/lessons/solidity-11-coding-patterns/topic/checks-effects-interactions/), where state variables are updated before any external calls are made. Doing so prevents a large class of reentrancy bugs.


*There are 7 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/ActivePool.sol

//@audit the function `transferShares()` is called before the following assignment
359:         feeRecipientCollShares = cachedFeeRecipientCollShares;

//@audit the function `syncGlobalAccountingAndGracePeriod()` is called before the following assignment
398:         feeRecipientAddress = _feeRecipientAddress;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L359-L359) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L398-L398)


```solidity

File: packages/contracts/contracts/BorrowerOperations.sol

//@audit the function `syncGlobalAccounting()` is called before the following assignment
1148:         feeRecipientAddress = _feeRecipientAddress;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L1148-L1148) 


```solidity

File: packages/contracts/contracts/CdpManagerStorage.sol

//@audit the function `pop()` is called before the following assignment
479:         CdpIds[index] = idToMove;

//@audit the function `allocateSystemCollSharesToFeeRecipient()` is called before the following assignment
581:         systemStEthFeePerUnitIndex = _newPerUnit;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L479-L479) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L581-L581)


```solidity

File: packages/contracts/contracts/CollSurplusPool.sol

//@audit the function `transferShares()` is called before the following assignment
94:         balances[_account] = 0;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L94-L94) 


```solidity

File: packages/contracts/contracts/LeverageMacroReference.sol

//@audit the function `approve()` is called before the following assignment
36:         theOwner = _owner;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroReference.sol#L36-L36) 


</details>


### [L&#x2011;20] prevent re-setting a state variable with the same value 
Not only is wasteful in terms of gas, but this is especially problematic when an event is emitted and the old and new values set are the same, as listeners might not expect this kind of scenario.


*There are 21 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/ActivePool.sol

390:     function setFeeRecipientAddress(address _feeRecipientAddress) external requiresAuth {

404:     function setFeeBps(uint256 _newFee) external requiresAuth {

417:     function setFlashLoansPaused(bool _paused) external requiresAuth {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L390-L390) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L404-L404), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L417-L417)


```solidity

File: packages/contracts/contracts/BorrowerOperations.sol

628:     function setPositionManagerApproval(

1140:     function setFeeRecipientAddress(address _feeRecipientAddress) external requiresAuth {

1154:     function setFeeBps(uint256 _newFee) external requiresAuth {

1167:     function setFlashLoansPaused(bool _paused) external requiresAuth {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L628-L628) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L1140-L1140), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L1154-L1154), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L1167-L1167)


```solidity

File: packages/contracts/contracts/CdpManager.sol

523:     function updateStakeAndTotalStakes(bytes32 _cdpId) external override returns (uint256) {

773:     function setStakingRewardSplit(uint256 _stakingRewardSplit) external requiresAuth {

788:     function setRedemptionFeeFloor(uint256 _redemptionFeeFloor) external requiresAuth {

807:     function setMinuteDecayFactor(uint256 _minuteDecayFactor) external requiresAuth {

830:     function setBeta(uint256 _beta) external requiresAuth {

843:     function setRedemptionsPaused(bool _paused) external requiresAuth {

946:     function updateCdp(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L523-L523) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L773-L773), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L788-L788), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L807-L807), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L830-L830), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L843-L843), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L946-L946)


```solidity

File: packages/contracts/contracts/CdpManagerStorage.sol

111:     function setGracePeriod(uint128 _gracePeriod) external requiresAuth {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L111-L111) 


```solidity

File: packages/contracts/contracts/CollSurplusPool.sol

130:     function increaseTotalSurplusCollShares(uint256 _value) external override {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L130-L130) 


```solidity

File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

38:     function setAuthority(address newAuthority) public virtual {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L38-L38) 


```solidity

File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

85:     function setPublicCapability(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L85-L85) 


```solidity

File: packages/contracts/contracts/Governor.sol

154:     function setRoleName(uint8 role, string memory roleName) external requiresAuth {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L154-L154) 


```solidity

File: packages/contracts/contracts/LeverageMacroReference.sol

50:     function resetApprovals() external {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroReference.sol#L50-L50) 


```solidity

File: packages/contracts/contracts/PriceFeed.sol

358:     function setFallbackCaller(address _fallbackCaller) external requiresAuth {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L358-L358) 


</details>


### [L&#x2011;21] Some tokens may not consider `type(uint256).max` as an infinite approval 
Some tokens such as [COMP](https://github.com/compound-finance/compound-protocol/blob/a3214f67b73310d547e00fc578e8355911c9d376/contracts/Governance/Comp.sol#L89-L91) downcast such approvals to `uint96` and use that as a raw value rather than interpreting it as an infinite approval. Eventually these approvals will reach zero, at which point the calling contract will no longer function properly.


*There are 6 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/LeverageMacroReference.sol

39:         ebtcToken.approve(_borrowerOperationsAddress, type(uint256).max);

40:         stETH.approve(_borrowerOperationsAddress, type(uint256).max);

41:         stETH.approve(_activePool, type(uint256).max);

53:         ebtcToken.approve(address(borrowerOperations), type(uint256).max);

54:         stETH.approve(address(borrowerOperations), type(uint256).max);

55:         stETH.approve(address(activePool), type(uint256).max);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroReference.sol#L39-L39) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroReference.sol#L40-L40), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroReference.sol#L41-L41), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroReference.sol#L53-L53), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroReference.sol#L54-L54), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroReference.sol#L55-L55)


</details>


### [L&#x2011;22] Missing contract-existence checks before yul `call()` 
Low-level calls return success if there is no code present at the specified address. In addition to the zero-address checks, add a check to verify that `extcodesize()` is non-zero.


*There are 4 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

513:         assembly {
514:             _success := call(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L513-L514) 


```solidity

File: packages/contracts/contracts/SimplifiedDiamondLike.sol

143:             assembly {
144:                 success := delegatecall(txGas, to, add(data, 0x20), mload(data), 0, 0)

148:             assembly {
149:                 success := call(txGas, to, value, add(data, 0x20), mload(data), 0, 0)

189:         assembly {
190:             calldatacopy(0, 0, calldatasize())


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L143-L144) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L148-L149), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L189-L190)


</details>


### [L&#x2011;23] Subtraction may underflow if multiplication is too large 
 


*There are 2 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

568:         uint256 _perUnitError = _deltaFeeSplitShare - (_deltaFeePerUnit * _cachedAllStakes);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L568-L568) 


```solidity

File: packages/contracts/contracts/LiquidationLibrary.sol

885:             EBTCDebtNumerator -
886:             (EBTCDebtRewardPerUnitStaked * _totalStakes);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L885-L886) 


</details>


## Non-critical Issues

### [NC&#x2011;1] State variables declarations should have NatSpec descriptions 



*There are 155 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/ActivePool.sol

24:     string public constant NAME = "ActivePool";

26:     address public immutable borrowerOperationsAddress;

27:     address public immutable cdpManagerAddress;

28:     address public immutable collSurplusPoolAddress;

29:     address public feeRecipientAddress;

31:     uint256 internal systemCollShares; // deposited collateral tracker

32:     uint256 internal systemDebt;

33:     uint256 internal feeRecipientCollShares; // coll shares claimable by fee recipient

34:     ICollateralToken public immutable collateral;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L24-L24) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L26-L26), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L27-L27), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L28-L28), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L29-L29), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L31-L31), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L32-L32), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L33-L33), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L34-L34)


```solidity

File: packages/contracts/contracts/BorrowerOperations.sol

29:     string public constant NAME = "BorrowerOperations";

32:     bytes32 private constant _PERMIT_POSITION_MANAGER_TYPEHASH =

38:     bytes32 private constant _TYPE_HASH =

41:     string internal constant _VERSION = "1";

45:     bytes32 private immutable _CACHED_DOMAIN_SEPARATOR;

46:     uint256 private immutable _CACHED_CHAIN_ID;

48:     bytes32 private immutable _HASHED_NAME;

49:     bytes32 private immutable _HASHED_VERSION;

53:     ICdpManager public immutable cdpManager;

55:     ICollSurplusPool public immutable collSurplusPool;

57:     address public feeRecipientAddress;

59:     IEBTCToken public immutable ebtcToken;

62:     ISortedCdps public immutable sortedCdps;

65:     mapping(address => mapping(address => PositionManagerApproval)) public positionManagers;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L29-L29) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L32-L32), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L38-L38), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L41-L41), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L45-L45), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L46-L46), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L48-L48), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L49-L49), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L53-L53), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L55-L55), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L57-L57), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L59-L59), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L62-L62), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L65-L65)


```solidity

File: packages/contracts/contracts/CdpManagerStorage.sol

21:     uint128 public constant UNSET_TIMESTAMP = type(uint128).max;

22:     uint128 public constant MINIMUM_GRACE_PERIOD = 15 minutes;

24:     uint128 public lastGracePeriodStartTimestamp = UNSET_TIMESTAMP; // use max to signify

25:     uint128 public recoveryModeGracePeriodDuration = MINIMUM_GRACE_PERIOD;

122:     string public constant NAME = "CdpManager";

126:     address public immutable borrowerOperationsAddress;

128:     ICollSurplusPool immutable collSurplusPool;

130:     IEBTCToken public immutable override ebtcToken;

132:     address public immutable liquidationLibrary;

135:     ISortedCdps public immutable sortedCdps;

139:     uint256 public constant SECONDS_IN_ONE_MINUTE = 60;

141:     uint256 public constant MIN_REDEMPTION_FEE_FLOOR = (DECIMAL_PRECISION * 5) / 1000; // 0.5%

142:     uint256 public redemptionFeeFloor = MIN_REDEMPTION_FEE_FLOOR;

143:     bool public redemptionsPaused;

148:     uint256 public minuteDecayFactor = 999037758833783000;

149:     uint256 public constant MIN_MINUTE_DECAY_FACTOR = 1; // Non-zero

150:     uint256 public constant MAX_MINUTE_DECAY_FACTOR = 999999999999999999; // Corresponds to a very fast decay rate, but not too extreme

152:     uint256 internal immutable deploymentStartTime;

159:     uint256 public beta = 2;

161:     uint256 public baseRate;

163:     uint256 public stakingRewardSplit;

166:     uint256 public lastRedemptionTimestamp;

168:     mapping(bytes32 => Cdp) public Cdps;

170:     uint256 public override totalStakes;

173:     uint256 public totalStakesSnapshot;

176:     uint256 public totalCollateralSnapshot;

187:     uint256 public systemDebtRedistributionIndex;

190:     mapping(bytes32 => uint256) public cdpDebtRedistributionIndex;

193:     uint256 public lastEBTCDebtErrorRedistribution;

196:     uint256 public override stEthIndex;

198:     uint256 public override systemStEthFeePerUnitIndex;

200:     uint256 public override systemStEthFeePerUnitIndexError;

202:     mapping(bytes32 => uint256) public cdpStEthFeePerUnitIndex;

205:     bytes32[] public CdpIds;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L21-L21) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L22-L22), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L24-L24), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L25-L25), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L122-L122), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L126-L126), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L128-L128), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L130-L130), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L132-L132), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L135-L135), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L139-L139), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L141-L141), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L142-L142), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L143-L143), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L148-L148), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L149-L149), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L150-L150), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L152-L152), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L159-L159), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L161-L161), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L163-L163), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L166-L166), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L168-L168), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L170-L170), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L173-L173), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L176-L176), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L187-L187), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L190-L190), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L193-L193), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L196-L196), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L198-L198), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L200-L200), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L202-L202), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L205-L205)


```solidity

File: packages/contracts/contracts/CollSurplusPool.sol

19:     string public constant NAME = "CollSurplusPool";

21:     address public immutable borrowerOperationsAddress;

22:     address public immutable cdpManagerAddress;

23:     address public immutable activePoolAddress;

24:     address public immutable feeRecipientAddress;

25:     ICollateralToken public immutable collateral;

28:     uint256 internal totalSurplusCollShares;

30:     mapping(address => uint256) internal balances;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L19-L19) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L21-L21), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L22-L22), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L23-L23), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L24-L24), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L25-L25), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L28-L28), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L30-L30)


```solidity

File: packages/contracts/contracts/EBTCToken.sol

27:     uint256 private _totalSupply;

28:     string internal constant _NAME = "EBTC Stablecoin";

29:     string internal constant _SYMBOL = "EBTC";

30:     string internal constant _VERSION = "1";

31:     uint8 internal constant _DECIMALS = 18;

36:     bytes32 private constant _PERMIT_TYPEHASH =

39:     bytes32 private constant _TYPE_HASH =

44:     bytes32 private immutable _CACHED_DOMAIN_SEPARATOR;

45:     uint256 private immutable _CACHED_CHAIN_ID;

47:     bytes32 private immutable _HASHED_NAME;

48:     bytes32 private immutable _HASHED_VERSION;

51:     mapping(address => uint256) private _balances;

52:     mapping(address => mapping(address => uint256)) private _allowances;

55:     address public immutable cdpManagerAddress;

56:     address public immutable borrowerOperationsAddress;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L27-L27) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L28-L28), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L29-L29), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L30-L30), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L31-L31), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L36-L36), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L39-L39), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L44-L44), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L45-L45), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L47-L47), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L48-L48), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L51-L51), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L52-L52), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L55-L55), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L56-L56)


```solidity

File: packages/contracts/contracts/Governor.sol

17:     bytes32 NO_ROLES = bytes32(0);

30:     mapping(uint8 => string) internal roleNames;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L17-L17) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L30-L30)


```solidity

File: packages/contracts/contracts/PriceFeed.sol

22:     string public constant NAME = "PriceFeed";

25:     AggregatorV3Interface public immutable ETH_BTC_CL_FEED;

26:     AggregatorV3Interface public immutable STETH_ETH_CL_FEED;

29:     IFallbackCaller public fallbackCaller; // Wrapper contract that calls the fallback system

32:     uint256 public constant TIMEOUT_ETH_BTC_FEED = 4800; // 1 hours & 20min: 60 * 80

33:     uint256 public constant TIMEOUT_STETH_ETH_FEED = 90000; // 25 hours: 60 * 60 * 25

36:     uint256 public constant MAX_PRICE_DEVIATION_FROM_PREVIOUS_ROUND = 5e17; // 50%

42:     uint256 public constant MAX_PRICE_DIFFERENCE_BETWEEN_ORACLES = 5e16; // 5%

45:     uint256 public lastGoodPrice;

48:     Status public status;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L22-L22) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L25-L25), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L26-L26), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L29-L29), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L32-L32), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L33-L33), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L36-L36), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L42-L42), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L45-L45), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L48-L48)


```solidity

File: packages/contracts/contracts/SortedCdps.sol

52:     string public constant NAME = "SortedCdps";

54:     address public immutable borrowerOperationsAddress;

56:     ICdpManager public immutable cdpManager;

58:     uint256 public immutable maxSize;

60:     uint256 constant ADDRESS_SHIFT = 96; // 8 * 12; Puts the address at leftmost bytes32 position

61:     uint256 constant BLOCK_SHIFT = 64; // 8 * 8; Puts the block value after the address

77:     Data public data;

79:     uint256 public nextCdpNonce;

80:     bytes32 public constant dummyId =


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L52-L52) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L54-L54), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L56-L56), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L58-L58), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L60-L60), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L61-L61), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L77-L77), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L79-L79), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L80-L80)


```solidity

File: packages/contracts/contracts/HintHelpers.sol

12:     string public constant NAME = "HintHelpers";

14:     ISortedCdps public immutable sortedCdps;

15:     ICdpManager public immutable cdpManager;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L12-L12) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L14-L14), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L15-L15)


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

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L29-L29) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L30-L30), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L31-L31), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L32-L32), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L33-L33), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L34-L34), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L35-L35), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L37-L37)


```solidity

File: packages/contracts/contracts/LeverageMacroFactory.sol

12:     address public immutable borrowerOperations;

13:     address public immutable activePool;

14:     address public immutable cdpManager;

15:     address public immutable ebtcToken;

16:     address public immutable stETH;

17:     address public immutable sortedCdps;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroFactory.sol#L12-L12) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroFactory.sol#L13-L13), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroFactory.sol#L14-L14), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroFactory.sol#L15-L15), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroFactory.sol#L16-L16), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroFactory.sol#L17-L17)


```solidity

File: packages/contracts/contracts/LeverageMacroReference.sol

12:     address internal immutable theOwner;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroReference.sol#L12-L12) 


```solidity

File: packages/contracts/contracts/SimplifiedDiamondLike.sol

39:     bytes32 constant DIAMOND_STORAGE_POSITION = keccak256("diamond.standard.diamond.storage");

42:     address public immutable owner;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L39-L39) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L42-L42)


```solidity

File: packages/contracts/contracts/Dependencies/Auth.sol

14:     address public owner;

16:     Authority public authority;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/Auth.sol#L14-L14) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/Auth.sol#L16-L16)


```solidity

File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

13:     Authority private _authority;

14:     bool private _authorityInitialized;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L13-L13) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L14-L14)


```solidity

File: packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol

9:     uint256 public constant MAX_BPS = 10_000;

10:     uint256 public constant MAX_FEE_BPS = 1_000; // 10%

11:     bytes32 public constant FLASH_SUCCESS_VALUE = keccak256("ERC3156FlashBorrower.onFlashLoan");

14:     uint16 public feeBps = 3; // may be subject to future adjustments through protocol governance

15:     bool public flashLoansPaused;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L9-L9) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L10-L10), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L11-L11), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L14-L14), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L15-L15)


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

41:     IActivePool public immutable activePool;

43:     IPriceFeed public immutable override priceFeed;

46:     ICollateralToken public immutable collateral;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L19-L19) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L22-L22), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L25-L25), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L28-L28), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L31-L31), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L33-L33), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L35-L35), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L37-L37), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L39-L39), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L41-L41), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L43-L43), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L46-L46)


```solidity

File: packages/contracts/contracts/Dependencies/EbtcMath.sol

6:     uint256 internal constant DECIMAL_PRECISION = 1e18;

7:     uint256 public constant MAX_TCR = type(uint256).max;

18:     uint256 internal constant NICR_PRECISION = 1e20;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcMath.sol#L6-L6) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcMath.sol#L7-L7), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcMath.sol#L18-L18)


```solidity

File: packages/contracts/contracts/Dependencies/ReentrancyGuard.sol

8:     uint256 internal constant OPEN = 1;

9:     uint256 internal constant LOCKED = 2;

11:     uint256 public locked = OPEN;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/ReentrancyGuard.sol#L8-L8) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/ReentrancyGuard.sol#L9-L9), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/ReentrancyGuard.sol#L11-L11)


```solidity

File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

26:     EnumerableSet.AddressSet internal users;

27:     EnumerableSet.AddressSet internal targets;

28:     mapping(address => EnumerableSet.Bytes32Set) internal enabledFunctionSigsByTarget;

30:     EnumerableSet.Bytes32Set internal enabledFunctionSigsPublic;

32:     mapping(address => bytes32) public getUserRoles;

34:     mapping(address => mapping(bytes4 => CapabilityFlag)) public capabilityFlag;

36:     mapping(address => mapping(bytes4 => bytes32)) public getRolesWithCapability;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L26-L26) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L27-L27), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L28-L28), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L30-L30), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L32-L32), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L34-L34), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L36-L36)


</details>


### [NC&#x2011;2] Consider using modifiers for address control 
Modifiers in Solidity can improve code readability and modularity by encapsulating repetitive checks, such as address validity checks, into a reusable construct. For example, an `onlyOwner` modifier can be used to replace repetitive `require(msg.sender == owner)` checks across several functions, reducing code redundancy and enhancing maintainability. To implement, define a modifier with the check, then apply the modifier to relevant functions.


*There are 23 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/ActivePool.sol

221:             msg.sender == borrowerOperationsAddress,

229:             msg.sender == borrowerOperationsAddress || msg.sender == cdpManagerAddress,

229:             msg.sender == borrowerOperationsAddress || msg.sender == cdpManagerAddress,

236:         require(msg.sender == cdpManagerAddress, "ActivePool: Caller is not CdpManager");


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L221-L221) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L229-L229), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L229-L229), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L236-L236)


```solidity

File: packages/contracts/contracts/CdpManagerStorage.sol

661:             msg.sender == borrowerOperationsAddress,


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L661-L661) 


```solidity

File: packages/contracts/contracts/CollSurplusPool.sol

114:             msg.sender == borrowerOperationsAddress,

120:         require(msg.sender == cdpManagerAddress, "CollSurplusPool: Caller is not CdpManager");

124:         require(msg.sender == activePoolAddress, "CollSurplusPool: Caller is not Active Pool");


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L114-L114) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L120-L120), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L124-L124)


```solidity

File: packages/contracts/contracts/EBTCToken.sol

308:             msg.sender == borrowerOperationsAddress,

316:             msg.sender == borrowerOperationsAddress ||

317:                 msg.sender == cdpManagerAddress ||

324:         require(msg.sender == cdpManagerAddress, "EBTC: Caller is not CdpManager");


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L308-L308) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L316-L316), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L317-L317), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L324-L324)


```solidity

File: packages/contracts/contracts/SortedCdps.sol

715:         require(msg.sender == address(cdpManager), "SortedCdps: Caller is not the CdpManager");

721:             msg.sender == borrowerOperationsAddress || msg.sender == address(cdpManager),

721:             msg.sender == borrowerOperationsAddress || msg.sender == address(cdpManager),


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L715-L715) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L721-L721), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L721-L721)


```solidity

File: packages/contracts/contracts/LeverageMacroBase.sol

45:         require(owner() == msg.sender, "Must be owner");

363:                 msg.sender == address(activePool),

357:                 msg.sender == address(borrowerOperations),


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L45-L45) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L363-L363), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L357-L357)


```solidity

File: packages/contracts/contracts/SimplifiedDiamondLike.sol

52:         require(msg.sender == owner);

67:         require(msg.sender == owner);

77:         require(msg.sender == address(this)); // Must call this via `execute` to explicitly set the flag

111:         require(msg.sender == owner, "Must be owner");


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L52-L52) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L67-L67), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L77-L77), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L111-L111)


```solidity

File: packages/contracts/contracts/Dependencies/Auth.sol

45:         require(msg.sender == owner || authority.canCall(msg.sender, address(this), msg.sig));


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/Auth.sol#L45-L45) 


</details>


### [NC&#x2011;3] Assembly blocks should have extensive comments 
Assembly blocks are taking a lot more time to audit than normal Solidity code, and often have gotchas and side-effects that the Solidity versions of the same code do not. Consider adding more comments explaining what is being done in every step of the assembly code


*There are 5 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

513:         assembly {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L513-L513) 


```solidity

File: packages/contracts/contracts/SimplifiedDiamondLike.sol

85:         assembly {

189:         assembly {

148:             assembly {

143:             assembly {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L85-L85) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L189-L189), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L148-L148), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L143-L143)


</details>


### [NC&#x2011;4] Contract declarations should have NatSpec `@author` annotations 



*There are 36 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/ActivePool.sol

15: /**
16:  * @title The Active Pool holds the collateral and EBTC debt (only accounting but not EBTC tokens) for all active cdps.
17:  *
18:  * @notice When a cdp is liquidated, it's collateral will be transferred from the Active Pool
19:  * @notice (destination may vary depending on the liquidation conditions).
20:  * @dev ActivePool also allows ERC3156 compatible flashloan of stETH token
21:  */


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L15-L21) 


```solidity

File: packages/contracts/contracts/BorrowerOperations.sol

18: /// @title BorrowerOperations is mainly in charge of all end user interactions like Cdp open, adjust, close etc
19: /// @notice End users could approve delegate via IPositionManagers for authorized actions on their behalf
20: /// @dev BorrowerOperations also allows ERC3156 compatible flashmint of eBTC token
21: contract BorrowerOperations is


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L18-L21) 


```solidity

File: packages/contracts/contracts/CdpManager.sol

13: /// @title CdpManager is mainly in charge of all Cdp related core processing like collateral & debt accounting, split fee calculation, redemption, etc
14: /// @notice Except for redemption, end user typically will interact with BorrowerOeprations for individual Cdp actions
15: /// @dev CdpManager also handles liquidation through delegatecall to LiquidationLibrary
16: contract CdpManager is CdpManagerStorage, ICdpManager, Proxy {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L13-L16) 


```solidity

File: packages/contracts/contracts/LiquidationLibrary.sol

11: /// @title LiquidationLibrary mainly provide necessary logic to fulfill liquidation for eBTC Cdps.
12: /// @dev This contract shares same base and storage layout with CdpManager and is the delegatecall destination from CdpManager
13: contract LiquidationLibrary is CdpManagerStorage {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L11-L13) 


```solidity

File: packages/contracts/contracts/CdpManagerStorage.sol

14: /// @title CDP Manager storage and shared functions with LiquidationLibrary
15: /// @dev All features around Cdp management are split into separate parts to get around contract size limitations.
16: /// @dev Liquidation related functions are delegated to LiquidationLibrary contract code.
17: /// @dev Both CdpManager and LiquidationLibrary must maintain **the same storage layout**, so shared storage components
18: /// @dev and shared functions are added here in CdpManagerStorage to de-dup code
19: contract CdpManagerStorage is EbtcBase, ReentrancyGuard, ICdpManagerData, AuthNoOwner {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L14-L19) 


```solidity

File: packages/contracts/contracts/CollSurplusPool.sol

12: /// @notice CollSurplusPool holds stETH collateral for Cdp owner when redemption or liquidation happens
13: /// @notice only if there is a remaining portion of the closed Cdp for the owner to claim
14: /// @dev While an owner could have multiple different sized Cdps, the remaining surplus colateral from all of its closed Cdp
15: /// @dev is consolidated into one balance here
16: contract CollSurplusPool is ICollSurplusPool, ReentrancyGuard, AuthNoOwner {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L12-L16) 


```solidity

File: packages/contracts/contracts/EBTCToken.sol

26: contract EBTCToken is IEBTCToken, AuthNoOwner, PermitNonce {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L26-L26) 


```solidity

File: packages/contracts/contracts/PriceFeed.sol

21: contract PriceFeed is BaseMath, IPriceFeed, AuthNoOwner {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L21-L21) 


```solidity

File: packages/contracts/contracts/SortedCdps.sol

51: contract SortedCdps is ISortedCdps {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L51-L51) 


```solidity

File: packages/contracts/contracts/HintHelpers.sol

09: /// @title HintHelpers mainly serves to provide handy information to facilitate offchain integration like redemption bots.
10: /// @dev It is strongly recommended to use HintHelper for redemption purpose
11: contract HintHelpers is EbtcBase {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L9-L11) 


```solidity

File: packages/contracts/contracts/LeverageMacroBase.sol

14: interface ICdpCdps {

18: /// @title Base implementation of the LeverageMacro
19: /// @notice Do not use this contract as a end users
20: /// @dev You must extend this contract and override `owner()` to allow this to work:
21: /// - As a Clone / Proxy (Not done, prob you'd read `owner` from calldata when using clones-with-immutable-args)
22: /// - As a deployed copy (LeverageMacroReference)
23: /// - Via delegate call (LeverageMacroDelegateTarget)
24: /// @custom:known-issue Due to slippage some dust amounts for all intermediary tokens can be left, since there's no way to ask to sell all available
25: 


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L14-L14) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L18-L25)


```solidity

File: packages/contracts/contracts/LeverageMacroDelegateTarget.sol

6: interface IOwnerLike {

26: /**
27:  * @title Implementation of the LeverageMacro, meant to be called via a delegatecall by a SC Like Wallet
28:  * @notice The Caller MUST implement the `function owner() external view returns (address)`
29:  * @notice to use this contract:
30:  *      Add this logic address to `callbackHandler` for the function `onFlashLoan`
31:  *      Add the inteded allowances (see above)
32:  *      Toggle the `callbackEnabledForCall` for the current call, by adding a call to `enableCallbackForCall`
33:  *      Perform the operation
34:  * @notice NOTE: that tokens will remain in the SC Wallet
35:  *  You can perform a delegatecall to `sweepToCaller` after the operation to have the SC Wallet send you back the funds
36:  * @notice If you didn't get it, this is an advanced contract, please simulate the TX with Tenderly before using this
37:  * @dev Only one deployment of this reference contract must be performed as users will delegatecall to it
38:  *  This makes upgrades opt-in
39:  */


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L6-L6) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L26-L39)


```solidity

File: packages/contracts/contracts/LeverageMacroFactory.sol

08: /**
09:  * @title Factory for deploying LeverageMacros
10:  */


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroFactory.sol#L8-L10) 


```solidity

File: packages/contracts/contracts/LeverageMacroReference.sol

06: /**
07:  * @title Reference implementation of LeverageMacro
08:  * @notice Deploy a copy of this via `LeverageMacroFactory` to use it for yourself
09:  * @dev You can deploy a copy of this via a clone or similar to save users gas
10:  */


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroReference.sol#L6-L10) 


```solidity

File: packages/contracts/contracts/SimplifiedDiamondLike.sol

04: /**
05:  * @title A multi-purpose Smart Contract Wallet
06:  * @notice `execute`s just like DSProxy
07:  * @notice handles callbacks via a DiamondLike Pattern
08:  * @notice CallbackOnly, only when toggled on, unless explicitly changed
09:  * @notice Due to the additional complexity, it's best used with a TX Simulator
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


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L4-L24) 


```solidity

File: packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol

8: abstract contract ERC3156FlashLender is IERC3156FlashLender {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L8-L8) 


```solidity

File: packages/contracts/contracts/Dependencies/EbtcBase.sol

16: contract EbtcBase is BaseMath, IEbtcBase {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L16-L16) 


```solidity

File: packages/contracts/contracts/Dependencies/EbtcMath.sol

5: library EbtcMath {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcMath.sol#L5-L5) 


```solidity

File: packages/contracts/contracts/Interfaces/IActivePool.sol

7: interface IActivePool is IPool {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IActivePool.sol#L7-L7) 


```solidity

File: packages/contracts/contracts/Interfaces/IBorrowerOperations.sol

7: interface IBorrowerOperations is IPositionManagers {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L7-L7) 


```solidity

File: packages/contracts/contracts/Interfaces/ICdpManager.sol

9: interface ICdpManager is IEbtcBase, ICdpManagerData {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManager.sol#L9-L9) 


```solidity

File: packages/contracts/contracts/Interfaces/ICdpManagerData.sol

13: interface ICdpManagerData is IRecoveryModeGracePeriod {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L13-L13) 


```solidity

File: packages/contracts/contracts/Interfaces/ICollSurplusPool.sol

5: interface ICollSurplusPool {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICollSurplusPool.sol#L5-L5) 


```solidity

File: packages/contracts/contracts/Interfaces/IEbtcBase.sol

7: interface IEbtcBase {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IEbtcBase.sol#L7-L7) 


```solidity

File: packages/contracts/contracts/Interfaces/IEBTCToken.sol

8: interface IEBTCToken is IERC20, IERC2612 {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IEBTCToken.sol#L8-L8) 


```solidity

File: packages/contracts/contracts/Interfaces/IERC3156FlashBorrower.sol

5: interface IERC3156FlashBorrower {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IERC3156FlashBorrower.sol#L5-L5) 


```solidity

File: packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol

7: interface IERC3156FlashLender {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol#L7-L7) 


```solidity

File: packages/contracts/contracts/Interfaces/IFallbackCaller.sol

5: interface IFallbackCaller {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IFallbackCaller.sol#L5-L5) 


```solidity

File: packages/contracts/contracts/Interfaces/IPermitNonce.sol

5: interface IPermitNonce {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPermitNonce.sol#L5-L5) 


```solidity

File: packages/contracts/contracts/Interfaces/IPool.sol

6: interface IPool {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPool.sol#L6-L6) 


```solidity

File: packages/contracts/contracts/Interfaces/IPositionManagers.sol

5: interface IPositionManagers {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPositionManagers.sol#L5-L5) 


```solidity

File: packages/contracts/contracts/Interfaces/IPriceFeed.sol

5: interface IPriceFeed {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPriceFeed.sol#L5-L5) 


```solidity

File: packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol

5: interface IRecoveryModeGracePeriod {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol#L5-L5) 


```solidity

File: packages/contracts/contracts/Interfaces/ISortedCdps.sol

6: interface ISortedCdps {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ISortedCdps.sol#L6-L6) 


</details>


### [NC&#x2011;5] Avoid the use of sensitive terms 
Use [alternative variants](https://www.zdnet.com/article/mysql-drops-master-slave-and-blacklist-whitelist-terminology/), e.g. allowlist/denylist instead of whitelist/blacklist


*There are 1 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

157:      * Corresponds to (1 / ALPHA) in the Liquity white paper.


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L157-L157) 


</details>


### [NC&#x2011;6] Variable names that consist of all capital letters should be reserved for `constant`/`immutable` variables 



*There are 38 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

91:         uint256 ICR;

92:         uint256 NICR;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L91-L91) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L92-L92)


```solidity

File: packages/contracts/contracts/CdpManager.sol

246:         uint256 _EBTC,

757:     function _requireTCRisNotBelowMCR(uint256 _price, uint256 _TCR) internal view {

600:         uint256 TCR = _computeTCRWithGivenSystemValues(_systemCollShares, _systemDebt, _price);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L246-L246) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L757-L757), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L600-L600)


```solidity

File: packages/contracts/contracts/LiquidationLibrary.sol

545:         uint256 _ICR,

571:         uint256 _ICR,

610:         uint256 _TCR,

809:         uint256 _TCR,

74:         uint256 _ICR = getCachedICR(_cdpId, _price); // @audit syncAccounting already called, guarenteed to be synced

75:         (uint256 _TCR, uint256 systemColl, uint256 systemDebt) = _getTCRWithSystemDebtAndCollShares(

692:         (uint256 _TCR, uint256 systemColl, uint256 systemDebt) = _getTCRWithSystemDebtAndCollShares(

745:         uint256 _TCR = _computeTCRWithGivenSystemValues(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L545-L545) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L571-L571), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L610-L610), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L809-L809), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L74-L74), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L75-L75), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L692-L692), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L745-L745)


```solidity

File: packages/contracts/contracts/CdpManagerStorage.sol

676:         uint256 NICR = EbtcMath._computeNominalCR(currentCollShares, currentEBTCDebt);

693:         uint256 NICR = EbtcMath._computeNominalCR(_newColl, _newDebt);

703:         uint256 ICR = _calculateCR(currentCollShares, currentEBTCDebt, _price);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L676-L676) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L693-L693), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L703-L703)


```solidity

File: packages/contracts/contracts/Governor.sol

17:     bytes32 NO_ROLES = bytes32(0);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L17-L17) 


```solidity

File: packages/contracts/contracts/SortedCdps.sol

346:         uint256 _NICR,

363:     function _insert(bytes32 _id, uint256 _NICR, bytes32 _prevId, bytes32 _nextId) internal {

584:         uint256 _NICR,

592:         uint256 _NICR,

619:     function _descendList(uint256 _NICR, bytes32 _startId) internal view returns (bytes32, bytes32) {

642:     function _ascendList(uint256 _NICR, bytes32 _startId) internal view returns (bytes32, bytes32) {

667:         uint256 _NICR,

675:         uint256 _NICR,


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L346-L346) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L363-L363), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L584-L584), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L592-L592), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L619-L619), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L642-L642), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L667-L667), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L675-L675)


```solidity

File: packages/contracts/contracts/HintHelpers.sol

165:         uint256 _CR,


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L165-L165) 


```solidity

File: packages/contracts/contracts/Dependencies/EbtcBase.sol

79:     function _getCachedTCR(uint256 _price) internal view returns (uint256 TCR) {

85:     ) internal view returns (uint256 TCR, uint256 _coll, uint256 _debt) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L79-L79) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L85-L85)


```solidity

File: packages/contracts/contracts/Interfaces/ICdpManagerData.sol

122:         uint256 ICR;

126:         uint256 TCR;

142:         uint256 ICR;

156:         uint256 ICR;

162:         uint256 TCR;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L122-L122) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L126-L126), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L142-L142), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L156-L156), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L162-L162)


```solidity

File: packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol

6:     event TCRNotified(uint256 TCR); /// NOTE: Mostly for debugging to ensure synch


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol#L6-L6) 


```solidity

File: packages/contracts/contracts/Interfaces/ISortedCdps.sol

9:     event NodeAdded(bytes32 _id, uint _NICR);

39:         uint256 _ICR,

45:         uint256 _ICR,

52:         uint256 _ICR,


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ISortedCdps.sol#L9-L9) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ISortedCdps.sol#L39-L39), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ISortedCdps.sol#L45-L45), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ISortedCdps.sol#L52-L52)


</details>


### [NC&#x2011;7] Common functions should be refactored to a common base contract 
The functions below have the same implementation as is seen in other files. The functions should be refactored into functions of a common base contract


*There are 6 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/EBTCToken.sol

//@audit this function is already seen in `packages/contracts/contracts/EBTCToken.sol`
176:     function DOMAIN_SEPARATOR() external view returns (bytes32) {
177:         return domainSeparator();
178:     }

//@audit this function is already seen in `packages/contracts/contracts/EBTCToken.sol`
182:     function domainSeparator() public view override returns (bytes32) {
183:         if (_chainID() == _CACHED_CHAIN_ID) {
184:             return _CACHED_DOMAIN_SEPARATOR;
185:         } else {
186:             return _buildDomainSeparator(_TYPE_HASH, _HASHED_NAME, _HASHED_VERSION);
187:         }
188:     }

//@audit this function is already seen in `packages/contracts/contracts/EBTCToken.sol`
231:     function _chainID() private view returns (uint256) {
232:         return block.chainid;
233:     }

//@audit this function is already seen in `packages/contracts/contracts/EBTCToken.sol`
235:     function _buildDomainSeparator(
236:         bytes32 typeHash,
237:         bytes32 name,
238:         bytes32 version
239:     ) private view returns (bytes32) {
240:         return keccak256(abi.encode(typeHash, name, version, _chainID(), address(this)));
241:     }

//@audit this function is already seen in `packages/contracts/contracts/EBTCToken.sol`
349:     function version() external pure override returns (string memory) {
350:         return _VERSION;
351:     }


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L176-L178) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L182-L188), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L231-L233), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L235-L241), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L349-L351)


```solidity

File: packages/contracts/contracts/Interfaces/IBorrowerOperations.sol

//@audit this function is already seen in `packages/contracts/contracts/Interfaces/IBorrowerOperations.sol`
86:     function feeRecipientAddress() external view returns (address);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L86-L86) 


</details>


### [NC&#x2011;8] Overly complicated arithmetic 
To maintain readability in code, particularly in Solidity which can involve complex mathematical operations, it is often recommended to limit the number of arithmetic operations to a maximum of 2-3 per line. Too many operations in a single line can make the code difficult to read and understand, increase the likelihood of mistakes, and complicate the process of debugging and reviewing the code. Consider splitting such operations over more than one line, take special care when dealing with division however. Try to limit the number of arithmetic operations to a maximum of 3 per line.


*There are 2 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/PriceFeed.sol

797:         uint256 _scaledDecimal = _stEthEthDecimals > _ethBtcDecimals
798:             ? 10 ** (_stEthEthDecimals - _ethBtcDecimals)
799:             : 10 ** (_ethBtcDecimals - _stEthEthDecimals);

800:         return
801:             (_scaledDecimal *
802:                 uint256(_ethBtcAnswer) *
803:                 uint256(_stEthEthAnswer) *
804:                 EbtcMath.DECIMAL_PRECISION) / 10 ** (_decimalDenominator * 2);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L797-L799) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L800-L804)


</details>


### [NC&#x2011;9] Constant redefined elsewhere 
Consider defining in only one contract so that values cannot become out of sync when only one location is updated. A [cheap way](https://medium.com/coinmonks/gas-cost-of-solidity-library-functions-dbe0cedd4678) to store constants in a single location is to create an `internal constant` in a `library`. If the variable is a local cache of another contract's value, consider making the cache variable internal or private, which will require external users to query the contract with the source of truth, so that callers don't get out of sync.


*There are 36 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

//@audit The same constant is already defined on file : packages/contracts/contracts/ActivePool.sol
29:     string public constant NAME = "BorrowerOperations";


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L29-L29) 


```solidity

File: packages/contracts/contracts/CdpManagerStorage.sol

//@audit The same constant is already defined on file : packages/contracts/contracts/ActivePool.sol
122:     string public constant NAME = "CdpManager";

//@audit The same constant is already defined on file : packages/contracts/contracts/ActivePool.sol
126:     address public immutable borrowerOperationsAddress;

//@audit The same constant is already defined on file : packages/contracts/contracts/BorrowerOperations.sol
128:     ICollSurplusPool immutable collSurplusPool;

//@audit The same constant is already defined on file : packages/contracts/contracts/BorrowerOperations.sol
130:     IEBTCToken public immutable override ebtcToken;

//@audit The same constant is already defined on file : packages/contracts/contracts/BorrowerOperations.sol
135:     ISortedCdps public immutable sortedCdps;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L122-L122) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L126-L126), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L128-L128), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L130-L130), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L135-L135)


```solidity

File: packages/contracts/contracts/CollSurplusPool.sol

//@audit The same constant is already defined on file : packages/contracts/contracts/ActivePool.sol
19:     string public constant NAME = "CollSurplusPool";

//@audit The same constant is already defined on file : packages/contracts/contracts/ActivePool.sol
21:     address public immutable borrowerOperationsAddress;

//@audit The same constant is already defined on file : packages/contracts/contracts/ActivePool.sol
22:     address public immutable cdpManagerAddress;

//@audit The same constant is already defined on file : packages/contracts/contracts/ActivePool.sol
25:     ICollateralToken public immutable collateral;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L19-L19) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L21-L21), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L22-L22), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L25-L25)


```solidity

File: packages/contracts/contracts/EBTCToken.sol

//@audit The same constant is already defined on file : packages/contracts/contracts/BorrowerOperations.sol
30:     string internal constant _VERSION = "1";

//@audit The same constant is already defined on file : packages/contracts/contracts/BorrowerOperations.sol
39:     bytes32 private constant _TYPE_HASH =

//@audit The same constant is already defined on file : packages/contracts/contracts/BorrowerOperations.sol
44:     bytes32 private immutable _CACHED_DOMAIN_SEPARATOR;

//@audit The same constant is already defined on file : packages/contracts/contracts/BorrowerOperations.sol
45:     uint256 private immutable _CACHED_CHAIN_ID;

//@audit The same constant is already defined on file : packages/contracts/contracts/BorrowerOperations.sol
47:     bytes32 private immutable _HASHED_NAME;

//@audit The same constant is already defined on file : packages/contracts/contracts/BorrowerOperations.sol
48:     bytes32 private immutable _HASHED_VERSION;

//@audit The same constant is already defined on file : packages/contracts/contracts/ActivePool.sol
55:     address public immutable cdpManagerAddress;

//@audit The same constant is already defined on file : packages/contracts/contracts/ActivePool.sol
56:     address public immutable borrowerOperationsAddress;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L30-L30) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L39-L39), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L44-L44), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L45-L45), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L47-L47), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L48-L48), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L55-L55), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L56-L56)


```solidity

File: packages/contracts/contracts/PriceFeed.sol

//@audit The same constant is already defined on file : packages/contracts/contracts/ActivePool.sol
22:     string public constant NAME = "PriceFeed";


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L22-L22) 


```solidity

File: packages/contracts/contracts/SortedCdps.sol

//@audit The same constant is already defined on file : packages/contracts/contracts/ActivePool.sol
52:     string public constant NAME = "SortedCdps";

//@audit The same constant is already defined on file : packages/contracts/contracts/ActivePool.sol
54:     address public immutable borrowerOperationsAddress;

//@audit The same constant is already defined on file : packages/contracts/contracts/BorrowerOperations.sol
56:     ICdpManager public immutable cdpManager;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L52-L52) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L54-L54), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L56-L56)


```solidity

File: packages/contracts/contracts/HintHelpers.sol

//@audit The same constant is already defined on file : packages/contracts/contracts/ActivePool.sol
12:     string public constant NAME = "HintHelpers";

//@audit The same constant is already defined on file : packages/contracts/contracts/BorrowerOperations.sol
14:     ISortedCdps public immutable sortedCdps;

//@audit The same constant is already defined on file : packages/contracts/contracts/BorrowerOperations.sol
15:     ICdpManager public immutable cdpManager;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L12-L12) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L14-L14), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L15-L15)


```solidity

File: packages/contracts/contracts/LeverageMacroBase.sol

//@audit The same constant is already defined on file : packages/contracts/contracts/BorrowerOperations.sol
31:     ICdpCdps public immutable cdpManager;

//@audit The same constant is already defined on file : packages/contracts/contracts/BorrowerOperations.sol
32:     IEBTCToken public immutable ebtcToken;

//@audit The same constant is already defined on file : packages/contracts/contracts/BorrowerOperations.sol
33:     ISortedCdps public immutable sortedCdps;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L31-L31) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L32-L32), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L33-L33)


```solidity

File: packages/contracts/contracts/LeverageMacroFactory.sol

//@audit The same constant is already defined on file : packages/contracts/contracts/LeverageMacroBase.sol
12:     address public immutable borrowerOperations;

//@audit The same constant is already defined on file : packages/contracts/contracts/LeverageMacroBase.sol
13:     address public immutable activePool;

//@audit The same constant is already defined on file : packages/contracts/contracts/BorrowerOperations.sol
14:     address public immutable cdpManager;

//@audit The same constant is already defined on file : packages/contracts/contracts/BorrowerOperations.sol
15:     address public immutable ebtcToken;

//@audit The same constant is already defined on file : packages/contracts/contracts/LeverageMacroBase.sol
16:     address public immutable stETH;

//@audit The same constant is already defined on file : packages/contracts/contracts/BorrowerOperations.sol
17:     address public immutable sortedCdps;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroFactory.sol#L12-L12) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroFactory.sol#L13-L13), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroFactory.sol#L14-L14), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroFactory.sol#L15-L15), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroFactory.sol#L16-L16), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroFactory.sol#L17-L17)


```solidity

File: packages/contracts/contracts/Dependencies/EbtcBase.sol

//@audit The same constant is already defined on file : packages/contracts/contracts/LeverageMacroBase.sol
41:     IActivePool public immutable activePool;

//@audit The same constant is already defined on file : packages/contracts/contracts/ActivePool.sol
46:     ICollateralToken public immutable collateral;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L41-L41) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L46-L46)


</details>


### [NC&#x2011;10] Constants in comparisons should appear on the left side 



*There are 145 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/ActivePool.sol

//@audit `0`
267:         require(amount > 0, "ActivePool: 0 Amount");


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L267-L267) 


```solidity

File: packages/contracts/contracts/BorrowerOperations.sol

//@audit `0`
393:         if (!_isDebtIncrease && _debtChange > 0) {

//@audit `0`
463:         require(vars.netStEthBalance > 0, "BorrowerOperations: zero collateral for openCdp()!");

//@audit `0`
748:         if (_collReceived != 0) {

//@audit `0`
808:             _stEthBalanceIncrease == 0 || _stEthBalanceDecrease == 0,

//@audit `0`
808:             _stEthBalanceIncrease == 0 || _stEthBalanceDecrease == 0,

//@audit `0`
819:             _stEthBalanceIncrease != 0 || _stEthBalanceDecrease != 0 || _debtChange != 0,

//@audit `0`
819:             _stEthBalanceIncrease != 0 || _stEthBalanceDecrease != 0 || _debtChange != 0,

//@audit `0`
819:             _stEthBalanceIncrease != 0 || _stEthBalanceDecrease != 0 || _debtChange != 0,

//@audit `1`
826:         require(status == 1, "BorrowerOperations: Cdp does not exist or is closed");

//@audit `0`
831:         require(status == 0, "BorrowerOperations: Cdp is active or has been previously closed");

//@audit `0`
835:         require(_debtChange > 0, "BorrowerOperations: Debt increase requires non-zero debtChange");

//@audit `0`
847:             _stEthBalanceDecrease == 0,

//@audit `0`
936:         require(_debt > 0, "BorrowerOperations: Debt must be non-zero");

//@audit `0`
1083:         require(amount > 0, "BorrowerOperations: 0 Amount");


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L393-L393) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L463-L463), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L748-L748), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L808-L808), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L808-L808), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L819-L819), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L819-L819), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L819-L819), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L826-L826), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L831-L831), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L835-L835), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L847-L847), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L936-L936), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L1083-L1083)


```solidity

File: packages/contracts/contracts/CdpManager.sol

//@audit `0`
159:         if (newDebt == 0) {

//@audit `0`
377:         if (_maxIterations == 0) {

//@audit `1`
434:         if (_numCdpsFullyRedeemed == 1) {

//@audit `false`
332:         require(redemptionsPaused == false, "CdpManager: Redemptions Paused");

//@audit `0`
389:             currentBorrower != address(0) && totals.remainingDebtToRedeem > 0 && _maxIterations > 0

//@audit `0`
431:         require(totals.collSharesDrawn > 0, "CdpManager: Unable to redeem any amount");

//@audit `1`
436:         } else if (_numCdpsFullyRedeemed > 1) {

//@audit `0`
389:             currentBorrower != address(0) && totals.remainingDebtToRedeem > 0 && _maxIterations > 0

//@audit `0`
497:         while (_cnt > 0 && _id != bytes32(0)) {

//@audit `0`
626:         require(newBaseRate > 0, "CdpManager: new baseRate is zero!"); // Base rate is always non-zero after redemption

//@audit `0`
754:         require(_amount > 0, "CdpManager: Amount must be greater than zero");


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L159-L159) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L377-L377), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L434-L434), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L332-L332), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L389-L389), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L431-L431), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L436-L436), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L389-L389), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L497-L497), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L626-L626), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L754-L754)


```solidity

File: packages/contracts/contracts/LiquidationLibrary.sol

//@audit `0`
56:         require(_partialAmount != 0, "LiquidationLibrary: use `liquidate` for 100%");

//@audit `0`
144:         if (_liqState.partialAmount == 0) {

//@audit `0`
158:                 liquidationValues.totalCollToSendToLiquidator == 0 &&

//@audit `0`
159:                 liquidationValues.debtToBurn == 0

//@audit `0`
195:             if (_outputState.totalSurplusCollShares > 0) {

//@audit `0`
261:             if (_collSurplus > 0) {

//@audit `0`
266:             if (_debtToRedistribute > 0) {

//@audit `0`
336:             if (_collSurplus > 0) {

//@audit `0`
342:             if (_debtToRedistribute > 0) {

//@audit `0`
417:         if (newColl == 0) {

//@audit `0`
525:         if (totalDebtToRedistribute > 0) {

//@audit `0`
713:         if (totals.totalCollSurplus > 0) {

//@audit `0`
681:             _cdpArray.length != 0,

//@audit `0`
710:         require(totals.totalDebtInSequence > 0, "LiquidationLibrary: nothing to liquidate");

//@audit `0`
863:         if (_debt == 0) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L56-L56) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L144-L144), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L158-L158), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L159-L159), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L195-L195), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L261-L261), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L266-L266), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L336-L336), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L342-L342), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L417-L417), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L525-L525), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L713-L713), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L681-L681), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L710-L710), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L863-L863)


```solidity

File: packages/contracts/contracts/CdpManagerStorage.sol

//@audit `UNSET_TIMESTAMP`
52:         if (lastGracePeriodStartTimestamp == UNSET_TIMESTAMP) {

//@audit `UNSET_TIMESTAMP`
66:         if (lastGracePeriodStartTimestamp != UNSET_TIMESTAMP) {

//@audit `MINIMUM_GRACE_PERIOD`
113:             _gracePeriod >= MINIMUM_GRACE_PERIOD,

//@audit `0`
315:         if (_debtIndexDiff > 0) {

//@audit `0`
362:         if (_feeSplitDistributed > 0 || _debtIndexDelta > 0) {

//@audit `0`
362:         if (_feeSplitDistributed > 0 || _debtIndexDelta > 0) {

//@audit `0`
369:             if (_feeSplitDistributed > 0) {

//@audit `0`
380:             if (_debtIndexDelta > 0) {

//@audit `0`
443:         if (totalCollateralSnapshot == 0) {

//@audit `0`
453:             require(totalStakesSnapshot > 0, "CdpManagerStorage: zero totalStakesSnapshot!");

//@audit `0`
512:         if (_newIndex > _oldIndex && totalStakes > 0) {

//@audit `0`
624:             _cdpStEthFeePerUnitIndex == 0 ||

//@audit `0`
625:             _cdpCol == 0 ||

//@audit `1`
654:             CdpOwnersArrayLength > 1 && sortedCdps.getSize() > 1,

//@audit `1`
654:             CdpOwnersArrayLength > 1 && sortedCdps.getSize() > 1,

//@audit `0`
765:         if (_newIndex > _oldIndex && totalStakes > 0) {

//@audit `0`
796:         if (_cdpPerUnitIdx != _systemStEthFeePerUnitIndex && _cdpPerUnitIdx > 0) {

//@audit `0`
829:         if (pendingDebtRedistributed > 0) {

//@audit `0`
879:         if (_feeTaken > 0) {

//@audit `UNSET_TIMESTAMP`
899:             cachedLastGracePeriodStartTimestamp != UNSET_TIMESTAMP &&


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L52-L52) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L66-L66), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L113-L113), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L315-L315), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L362-L362), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L362-L362), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L369-L369), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L380-L380), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L443-L443), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L453-L453), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L512-L512), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L624-L624), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L625-L625), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L654-L654), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L654-L654), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L765-L765), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L796-L796), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L829-L829), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L879-L879), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L899-L899)


```solidity

File: packages/contracts/contracts/CollSurplusPool.sol

//@audit `0`
92:         require(claimableColl > 0, "CollSurplusPool: No collateral available to claim");


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L92-L92) 


```solidity

File: packages/contracts/contracts/Governor.sol

//@audit `0`
53:         if (count > 0) {

//@audit `0`
81:         if (count > 0) {

//@audit `0`
104:         if (count > 0) {

//@audit `0`
99:             bool roleEnabled = (uint256(byteMap >> i) & 1) != 0;

//@audit `0`
108:                 bool roleEnabled = (uint256(byteMap >> i) & 1) != 0;

//@audit `0`
135:         if (_sigs.length > 0) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L53-L53) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L81-L81), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L104-L104), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L99-L99), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L108-L108), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L135-L135)


```solidity

File: packages/contracts/contracts/PriceFeed.sol

//@audit `0`
422:             _response.timestampStEthEth == 0 ||

//@audit `0`
420:             _response.timestampEthBtc == 0 ||

//@audit `MAX_PRICE_DEVIATION_FROM_PREVIOUS_ROUND`
462:         return percentDeviation > MAX_PRICE_DEVIATION_FROM_PREVIOUS_ROUND;

//@audit `0`
457:         uint256 percentDeviation = maxPrice > 0

//@audit `0`
475:         if (_response.answer == 0) {

//@audit `0`
471:         if (_response.timestamp == 0 || _response.timestamp > block.timestamp) {

//@audit `0`
489:             _fallbackResponse.timestamp > 0 &&

//@audit `0`
532:         if (minPrice == 0) return false;

//@audit `MAX_PRICE_DIFFERENCE_BETWEEN_ORACLES`
541:         return percentPriceDifference <= MAX_PRICE_DIFFERENCE_BETWEEN_ORACLES;

//@audit `0`
695:         if (_currentRoundEthBtcId == 0 || _currentRoundStEthEthId == 0) {

//@audit `0`
695:         if (_currentRoundEthBtcId == 0 || _currentRoundStEthEthId == 0) {

//@audit `0`
776:         if (_answer <= 0) return false;

//@audit `0`
777:         if (_roundId == 0) return false;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L422-L422) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L420-L420), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L462-L462), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L457-L457), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L475-L475), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L471-L471), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L489-L489), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L532-L532), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L541-L541), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L695-L695), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L695-L695), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L776-L776), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L777-L777)


```solidity

File: packages/contracts/contracts/SortedCdps.sol

//@audit `0`
89:         if (_size == 0) {

//@audit `dummyId`
185:         while (_currentCdpId != dummyId) {

//@audit `dummyId`
181:         bytes32 _currentCdpId = (startNodeId == dummyId ? data.tail : startNodeId);

//@audit `0`
202:             if (maxNodes > 0 && i >= maxNodes) {

//@audit `dummyId`
248:         while (_currentCdpId != dummyId) {

//@audit `dummyId`
244:         bytes32 _currentCdpId = (startNodeId == dummyId ? data.tail : startNodeId);

//@audit `0`
259:             if (maxNodes > 0 && i >= maxNodes) {

//@audit `0`
274:         if (_ownedCount > 0) {

//@audit `0`
305:         if (maxArraySize == 0) {

//@audit `dummyId`
318:         while (_currentCdpId != dummyId) {

//@audit `dummyId`
316:         bytes32 _currentCdpId = (startNodeId == dummyId ? data.tail : startNodeId);

//@audit `0`
330:             if (maxNodes > 0 && i >= maxNodes) {

//@audit `0`
352:         require(cdpManager.getCdpStatus(_id) == 0, "SortedCdps: new id is NOT nonExistent!");

//@audit `dummyId`
369:         require(_id != dummyId, "SortedCdps: Id cannot be zero");

//@audit `0`
371:         require(_NICR > 0, "SortedCdps: NICR must be positive");

//@audit `dummyId`
382:         if (prevId == dummyId && nextId == dummyId) {

//@audit `dummyId`
382:         if (prevId == dummyId && nextId == dummyId) {

//@audit `dummyId`
386:         } else if (prevId == dummyId) {

//@audit `dummyId`
391:         } else if (nextId == dummyId) {

//@audit `dummyId`
437:         if (_firstPrev != dummyId) {

//@audit `dummyId`
442:         if (_lastNext != dummyId) {

//@audit `1`
422:         require(_len > 1, "SortedCdps: batchRemove() only apply to multiple cdpIds!");

//@audit `dummyId`
428:             _firstPrev != dummyId || _lastNext != dummyId,

//@audit `dummyId`
428:             _firstPrev != dummyId || _lastNext != dummyId,

//@audit `1`
460:         if (data.size > 1) {

//@audit `0`
508:         require(_newNICR > 0, "SortedCdps: NICR must be positive");

//@audit `dummyId`
520:         bool _exist = _id != dummyId && (data.head == _id || data.tail == _id);

//@audit `dummyId`
523:             _exist = _id != dummyId && (_node.nextId != dummyId && _node.prevId != dummyId);

//@audit `dummyId`
523:             _exist = _id != dummyId && (_node.nextId != dummyId && _node.prevId != dummyId);

//@audit `dummyId`
523:             _exist = _id != dummyId && (_node.nextId != dummyId && _node.prevId != dummyId);

//@audit `0`
537:         return data.size == 0;

//@audit `dummyId`
596:         if (_prevId == dummyId && _nextId == dummyId) {

//@audit `dummyId`
596:         if (_prevId == dummyId && _nextId == dummyId) {

//@audit `dummyId`
599:         } else if (_prevId == dummyId) {

//@audit `dummyId`
602:         } else if (_nextId == dummyId) {

//@audit `dummyId`
629:         while (prevId != dummyId && !_validInsertPosition(_NICR, prevId, nextId)) {

//@audit `dummyId`
652:         while (nextId != dummyId && !_validInsertPosition(_NICR, prevId, nextId)) {

//@audit `dummyId`
682:         if (prevId != dummyId) {

//@audit `dummyId`
689:         if (nextId != dummyId) {

//@audit `dummyId`
696:         if (prevId == dummyId && nextId == dummyId) {

//@audit `dummyId`
696:         if (prevId == dummyId && nextId == dummyId) {

//@audit `dummyId`
699:         } else if (prevId == dummyId) {

//@audit `dummyId`
702:         } else if (nextId == dummyId) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L89-L89) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L185-L185), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L181-L181), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L202-L202), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L248-L248), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L244-L244), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L259-L259), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L274-L274), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L305-L305), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L318-L318), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L316-L316), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L330-L330), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L352-L352), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L369-L369), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L371-L371), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L382-L382), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L382-L382), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L386-L386), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L391-L391), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L437-L437), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L442-L442), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L422-L422), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L428-L428), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L428-L428), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L460-L460), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L508-L508), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L520-L520), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L523-L523), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L523-L523), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L523-L523), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L537-L537), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L596-L596), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L596-L596), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L599-L599), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L602-L602), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L629-L629), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L652-L652), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L682-L682), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L689-L689), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L696-L696), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L696-L696), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L699-L699), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L702-L702)


```solidity

File: packages/contracts/contracts/HintHelpers.sol

//@audit `0`
78:         if (_maxIterations == 0) {

//@audit `0`
87:                 _maxIterations-- > 0

//@audit `0`
86:                 vars.remainingEbtcToRedeem > 0 &&

//@audit `0`
171:         if (arrayLength == 0) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L78-L78) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L87-L87), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L86-L86), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L171-L171)


```solidity

File: packages/contracts/contracts/LeverageMacroBase.sol

//@audit `0`
128:         if (operation.amountToTransferIn > 0) {

//@audit `0`
223:         if (ebtcBal > 0) {

//@audit `0`
227:         if (collateralBal > 0) {

//@audit `0`
293:         if (beforeSwapsLength > 0) {

//@audit `0`
307:         if (afterSwapsLength > 0) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L128-L128) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L223-L223), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L227-L227), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L293-L293), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L307-L307)


```solidity

File: packages/contracts/contracts/SimplifiedDiamondLike.sol

//@audit `0x94b24d09`
56:         require(sig != 0x94b24d09);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L56-L56) 


```solidity

File: packages/contracts/contracts/Dependencies/EbtcBase.sol

//@audit `CCR`
100:         return _tcr < CCR;

//@audit `MCR`
135:         return _icr < MCR;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L100-L100) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L135-L135)


```solidity

File: packages/contracts/contracts/Dependencies/EbtcMath.sol

//@audit `525600000`
60:         if (_minutes > 525600000) {

//@audit `0`
64:         if (_minutes == 0) {

//@audit `1`
73:         while (n > 1) {

//@audit `0`
74:             if (n % 2 == 0) {

//@audit `0`
93:         if (_debt > 0) {

//@audit `0`
109:         if (_debt > 0) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcMath.sol#L60-L60) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcMath.sol#L64-L64), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcMath.sol#L73-L73), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcMath.sol#L74-L74), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcMath.sol#L93-L93), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcMath.sol#L109-L109)


```solidity

File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

//@audit `0`
39:         return (uint256(getUserRoles[user]) >> role) & 1 != 0;

//@audit `0`
47:         return (uint256(getRolesWithCapability[target][functionSig]) >> role) & 1 != 0;

//@audit `0`
124:             if (enabledFunctionSigsByTarget[target].length() == 0) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L39-L39) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L47-L47), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L124-L124)


</details>


### [NC&#x2011;11] `const` Variable names don\'t follow the Solidity style guide 
For `constant` variable names, each word should use all capital letters, with underscores separating each word (CONSTANT_CASE)


*There are 1 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/SortedCdps.sol

80:     bytes32 public constant dummyId =


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L80-L80) 


</details>


### [NC&#x2011;12] NatSpec documentation for `contract` is missing 
It is recommended that Solidity contracts are fully annotated using NatSpec for all public interfaces (everything in the ABI). It is clearly stated in the Solidity official documentation. In complex projects such as Defi, the interpretation of all functions and their arguments and returns is important for code readability and auditability.[source](https://docs.soliditylang.org/en/v0.8.15/natspec-format.html)


*There are 24 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/EBTCToken.sol

26: contract EBTCToken is IEBTCToken, AuthNoOwner, PermitNonce {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L26-L26) 


```solidity

File: packages/contracts/contracts/PriceFeed.sol

21: contract PriceFeed is BaseMath, IPriceFeed, AuthNoOwner {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L21-L21) 


```solidity

File: packages/contracts/contracts/SortedCdps.sol

51: contract SortedCdps is ISortedCdps {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L51-L51) 


```solidity

File: packages/contracts/contracts/LeverageMacroBase.sol

14: interface ICdpCdps {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L14-L14) 


```solidity

File: packages/contracts/contracts/LeverageMacroDelegateTarget.sol

6: interface IOwnerLike {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L6-L6) 


```solidity

File: packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol

8: abstract contract ERC3156FlashLender is IERC3156FlashLender {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L8-L8) 


```solidity

File: packages/contracts/contracts/Dependencies/EbtcBase.sol

16: contract EbtcBase is BaseMath, IEbtcBase {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L16-L16) 


```solidity

File: packages/contracts/contracts/Dependencies/EbtcMath.sol

5: library EbtcMath {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcMath.sol#L5-L5) 


```solidity

File: packages/contracts/contracts/Interfaces/IActivePool.sol

7: interface IActivePool is IPool {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IActivePool.sol#L7-L7) 


```solidity

File: packages/contracts/contracts/Interfaces/IBorrowerOperations.sol

7: interface IBorrowerOperations is IPositionManagers {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L7-L7) 


```solidity

File: packages/contracts/contracts/Interfaces/ICdpManager.sol

9: interface ICdpManager is IEbtcBase, ICdpManagerData {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManager.sol#L9-L9) 


```solidity

File: packages/contracts/contracts/Interfaces/ICdpManagerData.sol

13: interface ICdpManagerData is IRecoveryModeGracePeriod {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L13-L13) 


```solidity

File: packages/contracts/contracts/Interfaces/ICollSurplusPool.sol

5: interface ICollSurplusPool {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICollSurplusPool.sol#L5-L5) 


```solidity

File: packages/contracts/contracts/Interfaces/IEbtcBase.sol

7: interface IEbtcBase {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IEbtcBase.sol#L7-L7) 


```solidity

File: packages/contracts/contracts/Interfaces/IEBTCToken.sol

8: interface IEBTCToken is IERC20, IERC2612 {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IEBTCToken.sol#L8-L8) 


```solidity

File: packages/contracts/contracts/Interfaces/IERC3156FlashBorrower.sol

5: interface IERC3156FlashBorrower {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IERC3156FlashBorrower.sol#L5-L5) 


```solidity

File: packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol

7: interface IERC3156FlashLender {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol#L7-L7) 


```solidity

File: packages/contracts/contracts/Interfaces/IFallbackCaller.sol

5: interface IFallbackCaller {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IFallbackCaller.sol#L5-L5) 


```solidity

File: packages/contracts/contracts/Interfaces/IPermitNonce.sol

5: interface IPermitNonce {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPermitNonce.sol#L5-L5) 


```solidity

File: packages/contracts/contracts/Interfaces/IPool.sol

6: interface IPool {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPool.sol#L6-L6) 


```solidity

File: packages/contracts/contracts/Interfaces/IPositionManagers.sol

5: interface IPositionManagers {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPositionManagers.sol#L5-L5) 


```solidity

File: packages/contracts/contracts/Interfaces/IPriceFeed.sol

5: interface IPriceFeed {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPriceFeed.sol#L5-L5) 


```solidity

File: packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol

5: interface IRecoveryModeGracePeriod {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol#L5-L5) 


```solidity

File: packages/contracts/contracts/Interfaces/ISortedCdps.sol

6: interface ISortedCdps {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ISortedCdps.sol#L6-L6) 


</details>


### [NC&#x2011;13] Contract does not follow the Solidity style guide's suggested layout ordering 
The [style guide](https://docs.soliditylang.org/en/v0.8.16/style-guide.html#order-of-layout) says that, within a contract, the ordering should be 1) Type declarations, 2) State variables, 3) Events, 4) Modifiers, and 5) Functions, but the contract(s) below do not follow this ordering


*There are 8 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

//@audit the structure definition is misplaced
72:     struct AdjustCdpLocals {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L72-L72) 


```solidity

File: packages/contracts/contracts/HintHelpers.sol

//@audit the structure definition is misplaced
19:     struct LocalVariables_getRedemptionHints {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L19-L19) 


```solidity

File: packages/contracts/contracts/LeverageMacroBase.sol

//@audit the structure definition is misplaced
89:     struct CheckValueAndType {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L89-L89) 


```solidity

File: packages/contracts/contracts/SimplifiedDiamondLike.sol

//@audit the structure definition is misplaced
99:     struct Operation {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L99-L99) 


```solidity

File: packages/contracts/contracts/Dependencies/Auth.sol

//@audit the variable definition is misplaced
14:     address public owner;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/Auth.sol#L14-L14) 


```solidity

File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

//@audit the variable definition is misplaced
13:     Authority private _authority;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L13-L13) 


```solidity

File: packages/contracts/contracts/Interfaces/ICdpManagerData.sol

//@audit the structure definition is misplaced
97:     struct Cdp {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L97-L97) 


```solidity

File: packages/contracts/contracts/Interfaces/IPriceFeed.sol

//@audit the structure definition is misplaced
17:     struct ChainlinkResponse {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPriceFeed.sol#L17-L17) 


</details>


### [NC&#x2011;14] Control structures do not follow the Solidity Style Guide 
See the [control structures](https://docs.soliditylang.org/en/latest/style-guide.html#control-structures) section of the Solidity Style Guide


*There are 163 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/ActivePool.sol

129:     function transferSystemCollSharesAndLiquidatorReward(

261:     function flashLoan(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L129-L129) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L261-L261)


```solidity

File: packages/contracts/contracts/BorrowerOperations.sol

168:     function openCdp(

187:     function openCdpFor(

203:     function addColl(

219:     function withdrawColl(

235:     function withdrawDebt(

250:     function repayDebt(

270:     function adjustCdp(

300:     function adjustCdpWithColl(

328:     function _adjustCdpInternal(

439:     function _openCdp(

608:     function getPositionManagerApproval(

615:     function _getPositionManagerApproval(

628:     function setPositionManagerApproval(

635:     function _setPositionManagerApproval(

677:     function _buildDomainSeparator(

706:     function permitPositionManagerApproval(

744:     function _getCollSharesChangeFromStEthChange(

803:     function _requireSingularCollChange(

813:     function _requireNonZeroAdjustment(

852:     function _requireValidAdjustmentInCurrentMode(

953:     function _requireSufficientEbtcTokenBalance(

986:     function _getNewNominalICRFromCdpChange(

1004:     function _getNewICRFromCdpChange(

1030:     function _getNewCdpAmounts(

1049:     function _getNewTCRFromCdpChange(

1077:     function flashLoan(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L168-L168) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L187-L187), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L203-L203), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L219-L219), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L235-L235), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L250-L250), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L270-L270), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L300-L300), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L328-L328), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L439-L439), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L608-L608), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L615-L615), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L628-L628), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L635-L635), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L677-L677), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L706-L706), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L744-L744), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L803-L803), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L813-L813), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L852-L852), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L953-L953), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L986-L986), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L1004-L1004), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L1030-L1030), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L1049-L1049), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L1077-L1077)


```solidity

File: packages/contracts/contracts/CdpManager.sol

109:     function partiallyLiquidate(

135:     function _redeemCollateralFromCdp(

244:     function _closeCdpByRedemption(

272:     function _isValidFirstRedemptionHint(

320:     function redeemCollateral(

489:     function _getCdpIdsToRemove(

538:     function closeCdp(

595:     function _checkPotentialRecoveryMode(

612:     function _updateBaseRateFromRedemption(

661:     function getRedemptionFeeWithDecay(

667:     function _calcRedemptionFee(

727:     function checkPotentialRecoveryMode(

737:     function _requireEbtcBalanceCoversRedemptionAndWithinSupply(

905:     function initializeCdp(

946:     function updateCdp(

276:         if (

388:         while (

201:             if (


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L109-L109) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L135-L135), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L244-L244), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L272-L272), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L320-L320), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L489-L489), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L538-L538), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L595-L595), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L612-L612), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L661-L661), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L667-L667), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L727-L727), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L737-L737), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L905-L905), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L946-L946), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L276-L276), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L388-L388), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L201-L201)


```solidity

File: packages/contracts/contracts/LiquidationLibrary.sol

50:     function partiallyLiquidate(

61:     function _liquidateIndividualCdpSetup(

135:     function _liquidateIndividualCdpSetupCDP(

186:     function _liquidateCdpInGivenMode(

223:     function _liquidateIndividualCdpSetupCDPInNormalMode(

295:     function _liquidateIndividualCdpSetupCDPInRecoveryMode(

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

896:     function _requirePartialLiqDebtSize(

157:             if (

759:                 if (


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L50-L50) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L61-L61), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L135-L135), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L186-L186), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L223-L223), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L295-L295), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L397-L397), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L450-L450), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L466-L466), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L503-L503), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L544-L544), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L570-L570), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L608-L608), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L642-L642), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L733-L733), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L807-L807), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L839-L839), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L896-L896), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L157-L157), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L759-L759)


```solidity

File: packages/contracts/contracts/CdpManagerStorage.sol

87:     function _syncGracePeriodForGivenValues(

304:     function _getPendingRedistributedDebt(

489:     function _computeTCRWithGivenSystemValues(

552:     function calcFeeUponStakingReward(

574:     function _takeSplitAndUpdateFeePerUnit(

592:     function _applyAccumulatedFeeSplit(

616:     function getAccumulatedFeeSplitApplied(

707:     function _calculateCR(

719:     function getPendingRedistributedDebt(

733:     function _getSyncedDebtAndCollShares(

745:     function getSyncedDebtAndCollShares(

761:     function _calcSyncedGlobalAccounting(

787:     function _calcSyncedAccounting(

822:     function _getSyncedCdpDebtAndRedistribution(

623:         if (


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L87-L87) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L304-L304), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L489-L489), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L552-L552), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L574-L574), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L592-L592), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L616-L616), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L707-L707), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L719-L719), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L733-L733), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L745-L745), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L761-L761), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L787-L787), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L822-L822), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L623-L623)


```solidity

File: packages/contracts/contracts/EBTCToken.sol

134:     function transferFrom(

152:     function increaseAllowance(

160:     function decreaseAllowance(

199:     function permit(

235:     function _buildDomainSeparator(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L134-L134) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L152-L152), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L160-L160), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L199-L199), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L235-L235)


```solidity

File: packages/contracts/contracts/Governor.sol

131:     function getEnabledFunctionsInTarget(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L131-L131) 


```solidity

File: packages/contracts/contracts/PriceFeed.sol

400:     function _chainlinkIsBroken(

445:     function _chainlinkPriceChangeAboveMax(

485:     function _fallbackIsFrozen(

503:     function _bothOraclesLiveAndUnbrokenAndSimilarPrice(

526:     function _bothOraclesSimilarPrice(

561:     function _storeFallbackPrice(

687:     function _getPrevChainlinkResponse(

788:     function _formatClAggregateAnswer(

419:         if (

509:         if (

666:         if (

754:         if (

191:             if (

239:             if (

327:             if (

226:                 if (

372:                 if (


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L400-L400) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L445-L445), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L485-L485), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L503-L503), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L526-L526), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L561-L561), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L687-L687), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L788-L788), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L419-L419), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L509-L509), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L666-L666), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L754-L754), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L191-L191), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L239-L239), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L327-L327), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L226-L226), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L372-L372)


```solidity

File: packages/contracts/contracts/SortedCdps.sol

105:     function toCdpId(

140:     function cdpOfOwnerByIndex(

155:     function cdpOfOwnerByIdx(

173:     function _cdpOfOwnerByIndex(

227:     function getCdpCountOf(

237:     function _cdpCountOf(

286:     function getAllCdpsOf(

299:     function _getCdpsOf(

344:     function insert(

498:     function reInsert(

583:     function validInsertPosition(

591:     function _validInsertPosition(

666:     function findInsertPosition(

674:     function _findInsertPosition(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L105-L105) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L140-L140), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L155-L155), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L173-L173), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L227-L227), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L237-L237), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L286-L286), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L299-L299), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L344-L344), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L498-L498), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L583-L583), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L591-L591), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L666-L666), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L674-L674)


```solidity

File: packages/contracts/contracts/HintHelpers.sol

48:     function getRedemptionHints(

133:     function _calculateCdpStateAfterPartialRedemption(

164:     function getApproxHint(

212:     function computeCR(

68:             while (

84:             while (

101:                     if (


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L48-L48) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L133-L133), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L164-L164), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L212-L212), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L68-L68), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L84-L84), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L101-L101)


```solidity

File: packages/contracts/contracts/LeverageMacroBase.sol

118:     function doOperation(

344:     function onFlashLoan(

498:     function excessivelySafeCall(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L118-L118) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L344-L344), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L498-L498)


```solidity

File: packages/contracts/contracts/Dependencies/EbtcBase.sol

83:     function _getTCRWithSystemDebtAndCollShares(

103:     function _requireUserAcceptsFee(

115:     function _convertDebtDenominationToBtc(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L83-L83) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L103-L103), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L115-L115)


```solidity

File: packages/contracts/contracts/Dependencies/EbtcMath.sol

104:     function _computeCR(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcMath.sol#L104-L104) 


```solidity

File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

42:     function doesRoleHaveCapability(

63:     function canCall(

85:     function setPublicCapability(

106:     function setRoleCapability(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L42-L42) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L63-L63), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L85-L85), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L106-L106)


```solidity

File: packages/contracts/contracts/Interfaces/IActivePool.sol

27:     function transferSystemCollSharesAndLiquidatorReward(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IActivePool.sol#L27-L27) 


```solidity

File: packages/contracts/contracts/Interfaces/IBorrowerOperations.sol

20:     function openCdp(

27:     function openCdpFor(

35:     function addColl(

42:     function withdrawColl(

49:     function withdrawDebt(

56:     function repayDebt(

65:     function adjustCdp(

74:     function adjustCdpWithColl(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L20-L20) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L27-L27), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L35-L35), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L42-L42), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L49-L49), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L56-L56), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L65-L65), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L74-L74)


```solidity

File: packages/contracts/contracts/Interfaces/ICdpManager.sol

17:     function partiallyLiquidate(

26:     function redeemCollateral(

58:     function initializeCdp(

66:     function updateCdp(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManager.sol#L17-L17) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManager.sol#L26-L26), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManager.sol#L58-L58), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManager.sol#L66-L66)


```solidity

File: packages/contracts/contracts/Interfaces/ICdpManagerData.sol

227:     function calcFeeUponStakingReward(

236:     function getAccumulatedFeeSplitApplied(

259:     function getSyncedDebtAndCollShares(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L227-L227) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L236-L236), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L259-L259)


```solidity

File: packages/contracts/contracts/Interfaces/IERC3156FlashBorrower.sol

15:     function onFlashLoan(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IERC3156FlashBorrower.sol#L15-L15) 


```solidity

File: packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol

28:     function flashLoan(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol#L28-L28) 


```solidity

File: packages/contracts/contracts/Interfaces/IPositionManagers.sol

18:     function getPositionManagerApproval(

23:     function setPositionManagerApproval(

32:     function permitPositionManagerApproval(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPositionManagers.sol#L18-L18) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPositionManagers.sol#L23-L23), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPositionManagers.sol#L32-L32)


```solidity

File: packages/contracts/contracts/Interfaces/ISortedCdps.sol

38:     function validInsertPosition(

44:     function findInsertPosition(

50:     function insert(

63:     function getCdpCountOf(

71:     function getAllCdpsOf(

79:     function cdpOfOwnerByIdx(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ISortedCdps.sol#L38-L38) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ISortedCdps.sol#L44-L44), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ISortedCdps.sol#L50-L50), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ISortedCdps.sol#L63-L63), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ISortedCdps.sol#L71-L71), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ISortedCdps.sol#L79-L79)


</details>


### [NC&#x2011;15] Default address(0) can be returned 
Allowing a function in Solidity to return the default address (address(0)) can be problematic as it can represent uninitialized or invalid addresses. If such an address is utilized in transfer operations or other sensitive actions, it could lead to loss of funds or unpredicted behavior. It's prudent to include checks in your functions to prevent the return of the zero address, enhancing contract security.


*There are 3 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/LeverageMacroDelegateTarget.sol

65:         return _owner;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L65-L65) 


```solidity

File: packages/contracts/contracts/LeverageMacroFactory.sol

58:         return addy;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroFactory.sol#L58-L58) 


```solidity

File: packages/contracts/contracts/LeverageMacroReference.sol

45:         return theOwner;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroReference.sol#L45-L45) 


</details>


### [NC&#x2011;16] Consider using `delete` rather than assigning `zero` to clear values 
The `delete` keyword more closely matches the semantics of what is being done, and draws more attention to the changing of state, which may lead to a more thorough audit of its associated logic


*There are 11 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

264:                 _collSurplus = 0;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L264-L264) 


```solidity

File: packages/contracts/contracts/CdpManagerStorage.sol

272:         Cdps[_cdpId].coll = 0;

273:         Cdps[_cdpId].debt = 0;

274:         Cdps[_cdpId].liquidatorRewardShares = 0;

276:         cdpDebtRedistributionIndex[_cdpId] = 0;

277:         cdpStEthFeePerUnitIndex[_cdpId] = 0;

413:         Cdps[_cdpId].stake = 0;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L272-L272) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L273-L273), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L274-L274), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L276-L276), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L277-L277), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L413-L413)


```solidity

File: packages/contracts/contracts/CollSurplusPool.sol

94:         balances[_account] = 0;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L94-L94) 


```solidity

File: packages/contracts/contracts/HintHelpers.sol

109:                         vars.remainingEbtcToRedeem = 0;

105:                         partialRedemptionHintNICR = 0; //reset to 0 as there is no partial redemption in this case

106:                         partialRedemptionNewColl = 0;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L109-L109) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L105-L105), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L106-L106)


</details>


### [NC&#x2011;17] Dependence on external protocols 
External protocols should be monitored as such dependencies may introduce vulnerabilities if a vulnerability is found /introduced in the external protocol


*There are 1 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/PriceFeed.sol

7: import "./Dependencies/AggregatorV3Interface.sol";


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L7-L7) 


</details>


### [NC&#x2011;18] `else`-block not required 
One level of nesting can be removed by not having an `else` block when the `if`-block returns:


*There are 21 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

666:         if (_chainID() == _CACHED_CHAIN_ID) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L666-L666) 


```solidity

File: packages/contracts/contracts/CdpManager.sol

159:         if (newDebt == 0) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L159-L159) 


```solidity

File: packages/contracts/contracts/LiquidationLibrary.sol

190:         if (_liqState.recoveryModeAtStart) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L190-L190) 


```solidity

File: packages/contracts/contracts/CdpManagerStorage.sol

315:         if (_debtIndexDiff > 0) {

636:         if (_scaledCdpColl > _feeSplitDistributed) {

765:         if (_newIndex > _oldIndex && totalStakes > 0) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L315-L315) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L636-L636), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L765-L765)


```solidity

File: packages/contracts/contracts/EBTCToken.sol

183:         if (_chainID() == _CACHED_CHAIN_ID) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L183-L183) 


```solidity

File: packages/contracts/contracts/PriceFeed.sol

666:         if (

754:         if (


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L666-L666) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L754-L754)


```solidity

File: packages/contracts/contracts/SortedCdps.sol

596:         if (_prevId == dummyId && _nextId == dummyId) {

696:         if (prevId == dummyId && nextId == dummyId) {

599:         } else if (_prevId == dummyId) {

699:         } else if (prevId == dummyId) {

602:         } else if (_nextId == dummyId) {

702:         } else if (nextId == dummyId) {

189:                 if (_currentIndex == index) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L596-L596) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L696-L696), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L599-L599), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L699-L699), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L602-L602), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L702-L702), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L189-L189)


```solidity

File: packages/contracts/contracts/LeverageMacroBase.sol

245:         if (check.operator == Operator.skip) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L245-L245) 


```solidity

File: packages/contracts/contracts/Dependencies/EbtcMath.sol

93:         if (_debt > 0) {

109:         if (_debt > 0) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcMath.sol#L93-L93) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcMath.sol#L109-L109)


```solidity

File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

70:         if (flag == CapabilityFlag.Burned) {

72:         } else if (flag == CapabilityFlag.Public) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L70-L70) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L72-L72)


</details>


### [NC&#x2011;19] Empty bytes check is missing 
When developing smart contracts in Solidity, it's crucial to validate the inputs of your functions. This includes ensuring that the bytes parameters are not empty, especially when they represent crucial data such as addresses, identifiers, or raw data that the contract needs to process.
Missing empty bytes checks can lead to unexpected behaviour in your contract.For instance, certain operations might fail, produce incorrect results, or consume unnecessary gas when performed with empty bytes.Moreover, missing input validation can potentially expose your contract to malicious activity, including exploitation of unhandled edge cases.
To mitigate these issues, always validate that bytes parameters are not empty when the logic of your contract requires it.


*There are 131 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

//@audit  ,_upperHint ,_lowerHint are not checked
168:     function openCdp(
169:         uint256 _debt,
170:         bytes32 _upperHint,
171:         bytes32 _lowerHint,
172:         uint256 _stEthBalance
173:     ) external override nonReentrantSelfAndCdpM returns (bytes32) {

//@audit  ,_upperHint ,_lowerHint are not checked
187:     function openCdpFor(
188:         uint256 _debt,
189:         bytes32 _upperHint,
190:         bytes32 _lowerHint,
191:         uint256 _stEthBalance,
192:         address _borrower
193:     ) external override nonReentrantSelfAndCdpM returns (bytes32) {

//@audit  ,_cdpId ,_upperHint ,_lowerHint are not checked
203:     function addColl(
204:         bytes32 _cdpId,
205:         bytes32 _upperHint,
206:         bytes32 _lowerHint,
207:         uint256 _stEthBalanceIncrease
208:     ) external override nonReentrantSelfAndCdpM {

//@audit  ,_cdpId ,_upperHint ,_lowerHint are not checked
219:     function withdrawColl(
220:         bytes32 _cdpId,
221:         uint256 _stEthBalanceDecrease,
222:         bytes32 _upperHint,
223:         bytes32 _lowerHint
224:     ) external override nonReentrantSelfAndCdpM {

//@audit  ,_cdpId ,_upperHint ,_lowerHint are not checked
235:     function withdrawDebt(
236:         bytes32 _cdpId,
237:         uint256 _debt,
238:         bytes32 _upperHint,
239:         bytes32 _lowerHint
240:     ) external override nonReentrantSelfAndCdpM {

//@audit  ,_cdpId ,_upperHint ,_lowerHint are not checked
250:     function repayDebt(
251:         bytes32 _cdpId,
252:         uint256 _debt,
253:         bytes32 _upperHint,
254:         bytes32 _lowerHint
255:     ) external override nonReentrantSelfAndCdpM {

//@audit  ,_cdpId ,_upperHint ,_lowerHint are not checked
270:     function adjustCdp(
271:         bytes32 _cdpId,
272:         uint256 _stEthBalanceDecrease,
273:         uint256 _debtChange,
274:         bool _isDebtIncrease,
275:         bytes32 _upperHint,
276:         bytes32 _lowerHint
277:     ) external override nonReentrantSelfAndCdpM {

//@audit  ,_cdpId ,_upperHint ,_lowerHint are not checked
300:     function adjustCdpWithColl(
301:         bytes32 _cdpId,
302:         uint256 _stEthBalanceDecrease,
303:         uint256 _debtChange,
304:         bool _isDebtIncrease,
305:         bytes32 _upperHint,
306:         bytes32 _lowerHint,
307:         uint256 _stEthBalanceIncrease
308:     ) external override nonReentrantSelfAndCdpM {

//@audit  ,_cdpId ,_upperHint ,_lowerHint are not checked
328:     function _adjustCdpInternal(
329:         bytes32 _cdpId,
330:         uint256 _stEthBalanceDecrease,
331:         uint256 _debtChange,
332:         bool _isDebtIncrease,
333:         bytes32 _upperHint,
334:         bytes32 _lowerHint,
335:         uint256 _stEthBalanceIncrease
336:     ) internal {

//@audit  ,_upperHint ,_lowerHint are not checked
439:     function _openCdp(
440:         uint256 _debt,
441:         bytes32 _upperHint,
442:         bytes32 _lowerHint,
443:         uint256 _stEthBalance,
444:         address _borrower
445:     ) internal returns (bytes32) {

//@audit  ,_cdpId are not checked
553:     function closeCdp(bytes32 _cdpId) external override {
554:         address _borrower = sortedCdps.getOwnerAddress(_cdpId);

//@audit  ,typeHash ,name ,version are not checked
677:     function _buildDomainSeparator(
678:         bytes32 typeHash,
679:         bytes32 name,
680:         bytes32 version
681:     ) private view returns (bytes32) {

//@audit  ,r ,s are not checked
706:     function permitPositionManagerApproval(
707:         address _borrower,
708:         address _positionManager,
709:         PositionManagerApproval _approval,
710:         uint256 _deadline,
711:         uint8 v,
712:         bytes32 r,
713:         bytes32 s
714:     ) external override {

//@audit  ,_cdpId are not checked
824:     function _requireCdpisActive(ICdpManager _cdpManager, bytes32 _cdpId) internal view {
825:         uint256 status = _cdpManager.getCdpStatus(_cdpId);

//@audit  ,_cdpId are not checked
829:     function _requireCdpIsNonExistent(bytes32 _cdpId) internal view {
830:         uint status = cdpManager.getCdpStatus(_cdpId);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L168-L173) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L187-L193), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L203-L208), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L219-L224), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L235-L240), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L250-L255), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L270-L277), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L300-L308), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L328-L336), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L439-L445), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L553-L554), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L677-L681), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L706-L714), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L824-L825), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L829-L830)


```solidity

File: packages/contracts/contracts/CdpManager.sol

//@audit  ,_cdpId are not checked
099:     function liquidate(bytes32 _cdpId) external override {
100:         _delegate(liquidationLibrary);

//@audit  ,_cdpId ,_upperPartialHint ,_lowerPartialHint are not checked
109:     function partiallyLiquidate(
110:         bytes32 _cdpId,
111:         uint256 _partialAmount,
112:         bytes32 _upperPartialHint,
113:         bytes32 _lowerPartialHint
114:     ) external override {

//@audit  ,_cdpId are not checked
244:     function _closeCdpByRedemption(
245:         bytes32 _cdpId,
246:         uint256 _EBTC,
247:         uint256 _collSurplus,
248:         uint256 _liquidatorRewardShares,
249:         address _borrower
250:     ) internal {

//@audit  ,_firstRedemptionHint ,_upperPartialRedemptionHint ,_lowerPartialRedemptionHint are not checked
320:     function redeemCollateral(
321:         uint256 _debt,
322:         bytes32 _firstRedemptionHint,
323:         bytes32 _upperPartialRedemptionHint,
324:         bytes32 _lowerPartialRedemptionHint,
325:         uint256 _partialRedemptionHintNICR,
326:         uint256 _maxIterations,
327:         uint256 _maxFeePercentage
328:     ) external override nonReentrantSelfAndBOps {

//@audit  ,_cdpId are not checked
514:     function syncAccounting(bytes32 _cdpId) external virtual override {
515:         /// @audit Opening can cause invalid reordering of Cdps due to changing values without reInserting into sortedCdps

//@audit  ,_cdpId are not checked
523:     function updateStakeAndTotalStakes(bytes32 _cdpId) external override returns (uint256) {
524:         _requireCallerIsBorrowerOperations();

//@audit  ,_cdpId are not checked
538:     function closeCdp(
539:         bytes32 _cdpId,
540:         address _borrower,
541:         uint256 _debt,
542:         uint256 _coll
543:     ) external override {

//@audit  ,_cdpId are not checked
550:     function _addCdpIdToArray(bytes32 _cdpId) internal returns (uint128 index) {
551:         /* Max array size is 2**128 - 1, i.e. ~3e30 cdps. No risk of overflow, since cdps have minimum EBTC

//@audit  ,_cdpId are not checked
856:     function getCdpStatus(bytes32 _cdpId) external view override returns (uint256) {
857:         return uint256(Cdps[_cdpId].status);

//@audit  ,_cdpId are not checked
863:     function getCdpStake(bytes32 _cdpId) external view override returns (uint256) {
864:         return Cdps[_cdpId].stake;

//@audit  ,_cdpId are not checked
871:     function getCdpDebt(bytes32 _cdpId) external view override returns (uint256) {
872:         return Cdps[_cdpId].debt;

//@audit  ,_cdpId are not checked
879:     function getCdpCollShares(bytes32 _cdpId) external view override returns (uint256) {
880:         return Cdps[_cdpId].coll;

//@audit  ,_cdpId are not checked
891:     function getCdpLiquidatorRewardShares(bytes32 _cdpId) external view override returns (uint256) {
892:         return Cdps[_cdpId].liquidatorRewardShares;

//@audit  ,_cdpId are not checked
905:     function initializeCdp(
906:         bytes32 _cdpId,
907:         uint256 _debt,
908:         uint256 _coll,
909:         uint256 _liquidatorRewardShares,
910:         address _borrower
911:     ) external {

//@audit  ,_cdpId are not checked
946:     function updateCdp(
947:         bytes32 _cdpId,
948:         address _borrower,
949:         uint256 _coll,
950:         uint256 _debt,
951:         uint256 _newColl,
952:         uint256 _newDebt
953:     ) external {

//@audit  ,_cdpId are not checked
977:     function _setCdpCollShares(bytes32 _cdpId, uint256 _newColl) internal {
978:         Cdps[_cdpId].coll = _newColl;

//@audit  ,_cdpId are not checked
984:     function _setCdpDebt(bytes32 _cdpId, uint256 _newDebt) internal {
985:         Cdps[_cdpId].debt = _newDebt;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L99-L100) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L109-L114), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L244-L250), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L320-L328), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L514-L515), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L523-L524), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L538-L543), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L550-L551), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L856-L857), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L863-L864), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L871-L872), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L879-L880), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L891-L892), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L905-L911), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L946-L953), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L977-L978), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L984-L985)


```solidity

File: packages/contracts/contracts/LiquidationLibrary.sol

//@audit  ,_cdpId are not checked
40:     function liquidate(bytes32 _cdpId) external nonReentrantSelfAndBOps {
41:         _liquidateIndividualCdpSetup(_cdpId, 0, _cdpId, _cdpId);

//@audit  ,_cdpId ,_upperPartialHint ,_lowerPartialHint are not checked
50:     function partiallyLiquidate(
51:         bytes32 _cdpId,
52:         uint256 _partialAmount,
53:         bytes32 _upperPartialHint,
54:         bytes32 _lowerPartialHint
55:     ) external nonReentrantSelfAndBOps {

//@audit  ,_cdpId ,_upperPartialHint ,_lowerPartialHint are not checked
61:     function _liquidateIndividualCdpSetup(
62:         bytes32 _cdpId,
63:         uint256 _partialAmount,
64:         bytes32 _upperPartialHint,
65:         bytes32 _lowerPartialHint
66:     ) internal {

//@audit  ,_cdpId are not checked
384:     function _closeCdpByLiquidation(bytes32 _cdpId) private returns (uint256, uint256, uint256) {
385:         // calculate entire debt to repay

//@audit  ,_cdpId are not checked
450:     function _partiallyReduceCdpDebt(
451:         bytes32 _cdpId,
452:         uint256 _partialDebt,
453:         uint256 _partialColl
454:     ) internal {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L40-L41) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L50-L55), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L61-L66), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L384-L385), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L450-L454)


```solidity

File: packages/contracts/contracts/CdpManagerStorage.sol

//@audit  ,_cdpId are not checked
255:     function _closeCdp(bytes32 _cdpId, Status closedStatus) internal {
256:         _closeCdpWithoutRemovingSortedCdps(_cdpId, closedStatus);

//@audit  ,_cdpId are not checked
260:     function _closeCdpWithoutRemovingSortedCdps(bytes32 _cdpId, Status closedStatus) internal {
261:         require(

//@audit  ,_cdpId are not checked
304:     function _getPendingRedistributedDebt(
305:         bytes32 _cdpId
306:     ) internal view returns (uint256 pendingEBTCDebtReward, uint256 _debtIndexDiff) {

//@audit  ,_cdpId are not checked
336:     function _updateRedistributedDebtIndex(bytes32 _cdpId) internal {
337:         uint256 _systemDebtRedistributionIndex = systemDebtRedistributionIndex;

//@audit  ,_cdpId are not checked
344:     function _syncAccounting(bytes32 _cdpId) internal {
345:         // Ensure global states like systemStEthFeePerUnitIndex get updated in a timely fashion

//@audit  ,_cdpId are not checked
410:     function _removeStake(bytes32 _cdpId) internal {
411:         uint256 _newTotalStakes = totalStakes - Cdps[_cdpId].stake;

//@audit  ,_cdpId are not checked
419:     function _updateStakeAndTotalStakes(bytes32 _cdpId) internal returns (uint256) {
420:         (uint256 newStake, uint256 oldStake) = _updateStakeForCdp(_cdpId);

//@audit  ,_cdpId are not checked
431:     function _updateStakeForCdp(bytes32 _cdpId) internal returns (uint256, uint256) {
432:         Cdp storage _cdp = Cdps[_cdpId];

//@audit  ,_cdpId are not checked
463:     function _removeCdp(bytes32 _cdpId, uint256 cdpIdsArrayLength) internal {
464:         Status cdpStatus = Cdps[_cdpId].status;

//@audit  ,_cdpId are not checked
592:     function _applyAccumulatedFeeSplit(
593:         bytes32 _cdpId,
594:         uint256 _newColl,
595:         uint256 _feeSplitDistributed,
596:         uint256 _oldPerUnitCdp,
597:         uint256 _systemStEthFeePerUnitIndex
598:     ) internal {

//@audit  ,_cdpId are not checked
616:     function getAccumulatedFeeSplitApplied(
617:         bytes32 _cdpId,
618:         uint256 _systemStEthFeePerUnitIndex
619:     ) public view returns (uint256, uint256) {

//@audit  ,_cdpId are not checked
673:     function getCachedNominalICR(bytes32 _cdpId) external view returns (uint256) {
674:         (uint256 currentEBTCDebt, uint256 currentCollShares) = getSyncedDebtAndCollShares(_cdpId);

//@audit  ,_cdpId are not checked
684:     function getSyncedNominalICR(bytes32 _cdpId) external view returns (uint256) {
685:         (uint256 _oldIndex, uint256 _newIndex) = _readStEthIndex();

//@audit  ,_cdpId are not checked
701:     function getCachedICR(bytes32 _cdpId, uint256 _price) public view returns (uint256) {
702:         (uint256 currentEBTCDebt, uint256 currentCollShares) = getSyncedDebtAndCollShares(_cdpId);

//@audit  ,_cdpId are not checked
719:     function getPendingRedistributedDebt(
720:         bytes32 _cdpId
721:     ) public view returns (uint256 pendingEBTCDebtReward) {

//@audit  ,_cdpId are not checked
728:     function hasPendingRedistributedDebt(bytes32 _cdpId) public view returns (bool) {
729:         return _hasRedistributedDebt(_cdpId);

//@audit  ,_cdpId are not checked
733:     function _getSyncedDebtAndCollShares(
734:         bytes32 _cdpId
735:     ) internal view returns (CdpDebtAndCollShares memory) {

//@audit  ,_cdpId are not checked
745:     function getSyncedDebtAndCollShares(
746:         bytes32 _cdpId
747:     ) public view returns (uint256 debt, uint256 coll) {

//@audit  ,_cdpId are not checked
787:     function _calcSyncedAccounting(
788:         bytes32 _cdpId,
789:         uint256 _cdpPerUnitIdx,
790:         uint256 _systemStEthFeePerUnitIndex
791:     ) internal view returns (uint256, uint256, uint256, uint256, uint256) {

//@audit  ,_cdpId are not checked
822:     function _getSyncedCdpDebtAndRedistribution(
823:         bytes32 _cdpId
824:     ) internal view returns (uint256, uint256, uint256) {

//@audit  ,_cdpId are not checked
839:     function getSyncedCdpDebt(bytes32 _cdpId) public view returns (uint256) {
840:         (uint256 _newDebt, , ) = _getSyncedCdpDebtAndRedistribution(_cdpId);

//@audit  ,_cdpId are not checked
848:     function getSyncedCdpCollShares(bytes32 _cdpId) public view returns (uint256) {
849:         (uint256 _oldIndex, uint256 _newIndex) = _readStEthIndex();

//@audit  ,_cdpId are not checked
864:     function getSyncedICR(bytes32 _cdpId, uint256 _price) public view returns (uint256) {
865:         uint256 _debt = getSyncedCdpDebt(_cdpId);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L255-L256) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L260-L261), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L304-L306), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L336-L337), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L344-L345), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L410-L411), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L419-L420), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L431-L432), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L463-L464), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L592-L598), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L616-L619), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L673-L674), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L684-L685), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L701-L702), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L719-L721), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L728-L729), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L733-L735), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L745-L747), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L787-L791), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L822-L824), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L839-L840), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L848-L849), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L864-L865)


```solidity

File: packages/contracts/contracts/EBTCToken.sol

//@audit  ,r ,s are not checked
199:     function permit(
200:         address owner,
201:         address spender,
202:         uint256 amount,
203:         uint256 deadline,
204:         uint8 v,
205:         bytes32 r,
206:         bytes32 s
207:     ) external override {

//@audit  ,typeHash ,name ,version are not checked
235:     function _buildDomainSeparator(
236:         bytes32 typeHash,
237:         bytes32 name,
238:         bytes32 version
239:     ) private view returns (bytes32) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L199-L207) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L235-L239)


```solidity

File: packages/contracts/contracts/SortedCdps.sol

//@audit  ,cdpId are not checked
123:     function getOwnerAddress(bytes32 cdpId) public pure override returns (address) {
124:         uint256 _tmp = uint256(cdpId) >> ADDRESS_SHIFT;

//@audit  ,startNodeId are not checked
155:     function cdpOfOwnerByIdx(
156:         address owner,
157:         uint256 index,
158:         bytes32 startNodeId,
159:         uint maxNodes
160:     ) external view override returns (bytes32, bool) {

//@audit  ,startNodeId are not checked
227:     function getCdpCountOf(
228:         address owner,
229:         bytes32 startNodeId,
230:         uint maxNodes
231:     ) external view override returns (uint256, bytes32) {

//@audit  ,startNodeId are not checked
286:     function getAllCdpsOf(
287:         address owner,
288:         bytes32 startNodeId,
289:         uint maxNodes
290:     ) external view override returns (bytes32[] memory, uint256, bytes32) {

//@audit  ,_prevId ,_nextId are not checked
344:     function insert(
345:         address owner,
346:         uint256 _NICR,
347:         bytes32 _prevId,
348:         bytes32 _nextId
349:     ) external override returns (bytes32) {

//@audit  ,_prevId ,_nextId are not checked
363:     function _insert(bytes32 _id, uint256 _NICR, bytes32 _prevId, bytes32 _nextId) internal {
364:         // List must not be full

//@audit  ,_id are not checked
410:     function remove(bytes32 _id) external override {
411:         _requireCallerIsCdpManager();

//@audit  ,_id ,_prevId ,_nextId are not checked
498:     function reInsert(
499:         bytes32 _id,
500:         uint256 _newNICR,
501:         bytes32 _prevId,
502:         bytes32 _nextId
503:     ) external override {

//@audit  ,_id are not checked
567:     function getNext(bytes32 _id) external view override returns (bytes32) {
568:         return data.nodes[_id].nextId;

//@audit  ,_id are not checked
574:     function getPrev(bytes32 _id) external view override returns (bytes32) {
575:         return data.nodes[_id].prevId;

//@audit  ,_prevId ,_nextId are not checked
583:     function validInsertPosition(
584:         uint256 _NICR,
585:         bytes32 _prevId,
586:         bytes32 _nextId
587:     ) external view override returns (bool) {

//@audit  ,_prevId ,_nextId are not checked
666:     function findInsertPosition(
667:         uint256 _NICR,
668:         bytes32 _prevId,
669:         bytes32 _nextId
670:     ) external view override returns (bytes32, bytes32) {

//@audit  ,_prevId ,_nextId are not checked
674:     function _findInsertPosition(
675:         uint256 _NICR,
676:         bytes32 _prevId,
677:         bytes32 _nextId
678:     ) internal view returns (bytes32, bytes32) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L123-L124) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L155-L160), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L227-L231), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L286-L290), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L344-L349), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L363-L364), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L410-L411), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L498-L503), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L567-L568), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L574-L575), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L583-L587), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L666-L670), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L674-L678)


```solidity

File: packages/contracts/contracts/LeverageMacroBase.sol

//@audit  ,data are not checked
338:     function decodeFLData(bytes calldata data) public view returns (LeverageMacroOperation memory) {
339:         LeverageMacroOperation memory leverageMacroData = abi.decode(data, (LeverageMacroOperation));

//@audit  ,data are not checked
344:     function onFlashLoan(
345:         address initiator,
346:         address token,
347:         uint256 amount,
348:         uint256 fee,
349:         bytes calldata data
350:     ) external returns (bytes32) {

//@audit  ,data are not checked
460:     function _openCdpCallback(bytes memory data) internal {
461:         OpenCdpOperation memory flData = abi.decode(data, (OpenCdpOperation));

//@audit  ,data are not checked
474:     function _closeCdpCallback(bytes memory data) internal {
475:         CloseCdpOperation memory flData = abi.decode(data, (CloseCdpOperation));

//@audit  ,data are not checked
482:     function _adjustCdpCallback(bytes memory data) internal {
483:         AdjustCdpOperation memory flData = abi.decode(data, (AdjustCdpOperation));

//@audit  ,_calldata are not checked
498:     function excessivelySafeCall(
499:         address _target,
500:         uint256 _gas,
501:         uint256 _value,
502:         uint16 _maxCopy,
503:         bytes memory _calldata
504:     ) internal returns (bool, bytes memory) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L338-L339) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L344-L350), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L460-L461), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L474-L475), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L482-L483), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L498-L504)


```solidity

File: packages/contracts/contracts/Dependencies/Auth.sol

//@audit  ,functionSig are not checked
32:     function isAuthorized(address user, bytes4 functionSig) internal view virtual returns (bool) {
33:         Authority auth = authority; // Memoizing authority saves us a warm SLOAD, around 100 gas.


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/Auth.sol#L32-L33) 


```solidity

File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

//@audit  ,functionSig are not checked
30:     function isAuthorized(address user, bytes4 functionSig) internal view virtual returns (bool) {
31:         Authority auth = _authority; // Memoizing authority saves us a warm SLOAD, around 100 gas.


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L30-L31) 


```solidity

File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

//@audit  ,functionSig are not checked
106:     function setRoleCapability(
107:         uint8 role,
108:         address target,
109:         bytes4 functionSig,
110:         bool enabled
111:     ) public virtual requiresAuth {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L106-L111) 


```solidity

File: packages/contracts/contracts/Interfaces/IBorrowerOperations.sol

//@audit  ,_upperHint ,_lowerHint are not checked
20:     function openCdp(
21:         uint256 _EBTCAmount,
22:         bytes32 _upperHint,
23:         bytes32 _lowerHint,
24:         uint256 _stEthBalance
25:     ) external returns (bytes32);
26: 
27:     function openCdpFor(
28:         uint _EBTCAmount,
29:         bytes32 _upperHint,
30:         bytes32 _lowerHint,
31:         uint _collAmount,
32:         address _borrower
33:     ) external returns (bytes32);
34: 
35:     function addColl(
36:         bytes32 _cdpId,
37:         bytes32 _upperHint,
38:         bytes32 _lowerHint,
39:         uint256 _stEthBalanceIncrease
40:     ) external;
41: 
42:     function withdrawColl(
43:         bytes32 _cdpId,
44:         uint256 _stEthBalanceDecrease,
45:         bytes32 _upperHint,
46:         bytes32 _lowerHint
47:     ) external;
48: 
49:     function withdrawDebt(
50:         bytes32 _cdpId,
51:         uint256 _amount,
52:         bytes32 _upperHint,
53:         bytes32 _lowerHint
54:     ) external;
55: 
56:     function repayDebt(
57:         bytes32 _cdpId,
58:         uint256 _amount,
59:         bytes32 _upperHint,
60:         bytes32 _lowerHint
61:     ) external;
62: 
63:     function closeCdp(bytes32 _cdpId) external;
64: 
65:     function adjustCdp(
66:         bytes32 _cdpId,
67:         uint256 _stEthBalanceDecrease,
68:         uint256 _debtChange,
69:         bool isDebtIncrease,
70:         bytes32 _upperHint,
71:         bytes32 _lowerHint
72:     ) external;
73: 
74:     function adjustCdpWithColl(
75:         bytes32 _cdpId,
76:         uint256 _stEthBalanceDecrease,
77:         uint256 _debtChange,
78:         bool isDebtIncrease,
79:         bytes32 _upperHint,
80:         bytes32 _lowerHint,
81:         uint256 _stEthBalanceIncrease
82:     ) external;
83: 
84:     function claimSurplusCollShares() external;
85: 
86:     function feeRecipientAddress() external view returns (address);
87: }
88: 

//@audit  ,_upperHint ,_lowerHint are not checked
27:     function openCdpFor(
28:         uint _EBTCAmount,
29:         bytes32 _upperHint,
30:         bytes32 _lowerHint,
31:         uint _collAmount,
32:         address _borrower
33:     ) external returns (bytes32);
34: 
35:     function addColl(
36:         bytes32 _cdpId,
37:         bytes32 _upperHint,
38:         bytes32 _lowerHint,
39:         uint256 _stEthBalanceIncrease
40:     ) external;
41: 
42:     function withdrawColl(
43:         bytes32 _cdpId,
44:         uint256 _stEthBalanceDecrease,
45:         bytes32 _upperHint,
46:         bytes32 _lowerHint
47:     ) external;
48: 
49:     function withdrawDebt(
50:         bytes32 _cdpId,
51:         uint256 _amount,
52:         bytes32 _upperHint,
53:         bytes32 _lowerHint
54:     ) external;
55: 
56:     function repayDebt(
57:         bytes32 _cdpId,
58:         uint256 _amount,
59:         bytes32 _upperHint,
60:         bytes32 _lowerHint
61:     ) external;
62: 
63:     function closeCdp(bytes32 _cdpId) external;
64: 
65:     function adjustCdp(
66:         bytes32 _cdpId,
67:         uint256 _stEthBalanceDecrease,
68:         uint256 _debtChange,
69:         bool isDebtIncrease,
70:         bytes32 _upperHint,
71:         bytes32 _lowerHint
72:     ) external;
73: 
74:     function adjustCdpWithColl(
75:         bytes32 _cdpId,
76:         uint256 _stEthBalanceDecrease,
77:         uint256 _debtChange,
78:         bool isDebtIncrease,
79:         bytes32 _upperHint,
80:         bytes32 _lowerHint,
81:         uint256 _stEthBalanceIncrease
82:     ) external;
83: 
84:     function claimSurplusCollShares() external;
85: 
86:     function feeRecipientAddress() external view returns (address);
87: }
88: 

//@audit  ,_cdpId ,_upperHint ,_lowerHint are not checked
35:     function addColl(
36:         bytes32 _cdpId,
37:         bytes32 _upperHint,
38:         bytes32 _lowerHint,
39:         uint256 _stEthBalanceIncrease
40:     ) external;
41: 
42:     function withdrawColl(
43:         bytes32 _cdpId,
44:         uint256 _stEthBalanceDecrease,
45:         bytes32 _upperHint,
46:         bytes32 _lowerHint
47:     ) external;
48: 
49:     function withdrawDebt(
50:         bytes32 _cdpId,
51:         uint256 _amount,
52:         bytes32 _upperHint,
53:         bytes32 _lowerHint
54:     ) external;
55: 
56:     function repayDebt(
57:         bytes32 _cdpId,
58:         uint256 _amount,
59:         bytes32 _upperHint,
60:         bytes32 _lowerHint
61:     ) external;
62: 
63:     function closeCdp(bytes32 _cdpId) external;
64: 
65:     function adjustCdp(
66:         bytes32 _cdpId,
67:         uint256 _stEthBalanceDecrease,
68:         uint256 _debtChange,
69:         bool isDebtIncrease,
70:         bytes32 _upperHint,
71:         bytes32 _lowerHint
72:     ) external;
73: 
74:     function adjustCdpWithColl(
75:         bytes32 _cdpId,
76:         uint256 _stEthBalanceDecrease,
77:         uint256 _debtChange,
78:         bool isDebtIncrease,
79:         bytes32 _upperHint,
80:         bytes32 _lowerHint,
81:         uint256 _stEthBalanceIncrease
82:     ) external;
83: 
84:     function claimSurplusCollShares() external;
85: 
86:     function feeRecipientAddress() external view returns (address);
87: }
88: 

//@audit  ,_cdpId ,_upperHint ,_lowerHint are not checked
42:     function withdrawColl(
43:         bytes32 _cdpId,
44:         uint256 _stEthBalanceDecrease,
45:         bytes32 _upperHint,
46:         bytes32 _lowerHint
47:     ) external;
48: 
49:     function withdrawDebt(
50:         bytes32 _cdpId,
51:         uint256 _amount,
52:         bytes32 _upperHint,
53:         bytes32 _lowerHint
54:     ) external;
55: 
56:     function repayDebt(
57:         bytes32 _cdpId,
58:         uint256 _amount,
59:         bytes32 _upperHint,
60:         bytes32 _lowerHint
61:     ) external;
62: 
63:     function closeCdp(bytes32 _cdpId) external;
64: 
65:     function adjustCdp(
66:         bytes32 _cdpId,
67:         uint256 _stEthBalanceDecrease,
68:         uint256 _debtChange,
69:         bool isDebtIncrease,
70:         bytes32 _upperHint,
71:         bytes32 _lowerHint
72:     ) external;
73: 
74:     function adjustCdpWithColl(
75:         bytes32 _cdpId,
76:         uint256 _stEthBalanceDecrease,
77:         uint256 _debtChange,
78:         bool isDebtIncrease,
79:         bytes32 _upperHint,
80:         bytes32 _lowerHint,
81:         uint256 _stEthBalanceIncrease
82:     ) external;
83: 
84:     function claimSurplusCollShares() external;
85: 
86:     function feeRecipientAddress() external view returns (address);
87: }
88: 

//@audit  ,_cdpId ,_upperHint ,_lowerHint are not checked
49:     function withdrawDebt(
50:         bytes32 _cdpId,
51:         uint256 _amount,
52:         bytes32 _upperHint,
53:         bytes32 _lowerHint
54:     ) external;
55: 
56:     function repayDebt(
57:         bytes32 _cdpId,
58:         uint256 _amount,
59:         bytes32 _upperHint,
60:         bytes32 _lowerHint
61:     ) external;
62: 
63:     function closeCdp(bytes32 _cdpId) external;
64: 
65:     function adjustCdp(
66:         bytes32 _cdpId,
67:         uint256 _stEthBalanceDecrease,
68:         uint256 _debtChange,
69:         bool isDebtIncrease,
70:         bytes32 _upperHint,
71:         bytes32 _lowerHint
72:     ) external;
73: 
74:     function adjustCdpWithColl(
75:         bytes32 _cdpId,
76:         uint256 _stEthBalanceDecrease,
77:         uint256 _debtChange,
78:         bool isDebtIncrease,
79:         bytes32 _upperHint,
80:         bytes32 _lowerHint,
81:         uint256 _stEthBalanceIncrease
82:     ) external;
83: 
84:     function claimSurplusCollShares() external;
85: 
86:     function feeRecipientAddress() external view returns (address);
87: }
88: 

//@audit  ,_cdpId ,_upperHint ,_lowerHint are not checked
56:     function repayDebt(
57:         bytes32 _cdpId,
58:         uint256 _amount,
59:         bytes32 _upperHint,
60:         bytes32 _lowerHint
61:     ) external;
62: 
63:     function closeCdp(bytes32 _cdpId) external;
64: 
65:     function adjustCdp(
66:         bytes32 _cdpId,
67:         uint256 _stEthBalanceDecrease,
68:         uint256 _debtChange,
69:         bool isDebtIncrease,
70:         bytes32 _upperHint,
71:         bytes32 _lowerHint
72:     ) external;
73: 
74:     function adjustCdpWithColl(
75:         bytes32 _cdpId,
76:         uint256 _stEthBalanceDecrease,
77:         uint256 _debtChange,
78:         bool isDebtIncrease,
79:         bytes32 _upperHint,
80:         bytes32 _lowerHint,
81:         uint256 _stEthBalanceIncrease
82:     ) external;
83: 
84:     function claimSurplusCollShares() external;
85: 
86:     function feeRecipientAddress() external view returns (address);
87: }
88: 

//@audit  ,_cdpId are not checked
63:     function closeCdp(bytes32 _cdpId) external;
64: 
65:     function adjustCdp(
66:         bytes32 _cdpId,
67:         uint256 _stEthBalanceDecrease,
68:         uint256 _debtChange,
69:         bool isDebtIncrease,
70:         bytes32 _upperHint,
71:         bytes32 _lowerHint
72:     ) external;
73: 
74:     function adjustCdpWithColl(
75:         bytes32 _cdpId,
76:         uint256 _stEthBalanceDecrease,
77:         uint256 _debtChange,
78:         bool isDebtIncrease,
79:         bytes32 _upperHint,
80:         bytes32 _lowerHint,
81:         uint256 _stEthBalanceIncrease
82:     ) external;
83: 
84:     function claimSurplusCollShares() external;
85: 
86:     function feeRecipientAddress() external view returns (address);
87: }
88: 

//@audit  ,_cdpId ,_upperHint ,_lowerHint are not checked
65:     function adjustCdp(
66:         bytes32 _cdpId,
67:         uint256 _stEthBalanceDecrease,
68:         uint256 _debtChange,
69:         bool isDebtIncrease,
70:         bytes32 _upperHint,
71:         bytes32 _lowerHint
72:     ) external;
73: 
74:     function adjustCdpWithColl(
75:         bytes32 _cdpId,
76:         uint256 _stEthBalanceDecrease,
77:         uint256 _debtChange,
78:         bool isDebtIncrease,
79:         bytes32 _upperHint,
80:         bytes32 _lowerHint,
81:         uint256 _stEthBalanceIncrease
82:     ) external;
83: 
84:     function claimSurplusCollShares() external;
85: 
86:     function feeRecipientAddress() external view returns (address);
87: }
88: 

//@audit  ,_cdpId ,_upperHint ,_lowerHint are not checked
74:     function adjustCdpWithColl(
75:         bytes32 _cdpId,
76:         uint256 _stEthBalanceDecrease,
77:         uint256 _debtChange,
78:         bool isDebtIncrease,
79:         bytes32 _upperHint,
80:         bytes32 _lowerHint,
81:         uint256 _stEthBalanceIncrease
82:     ) external;
83: 
84:     function claimSurplusCollShares() external;
85: 
86:     function feeRecipientAddress() external view returns (address);
87: }
88: 


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L20-L88) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L27-L88), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L35-L88), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L42-L88), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L49-L88), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L56-L88), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L63-L88), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L65-L88), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L74-L88)


```solidity

File: packages/contracts/contracts/Interfaces/ICdpManager.sol

//@audit  ,_cdpId are not checked
15:     function liquidate(bytes32 _cdpId) external;
16: 
17:     function partiallyLiquidate(
18:         bytes32 _cdpId,
19:         uint256 _partialAmount,
20:         bytes32 _upperPartialHint,
21:         bytes32 _lowerPartialHint
22:     ) external;
23: 
24:     function batchLiquidateCdps(bytes32[] calldata _cdpArray) external;
25: 
26:     function redeemCollateral(
27:         uint256 _EBTCAmount,
28:         bytes32 _firstRedemptionHint,
29:         bytes32 _upperPartialRedemptionHint,
30:         bytes32 _lowerPartialRedemptionHint,
31:         uint256 _partialRedemptionHintNICR,
32:         uint256 _maxIterations,
33:         uint256 _maxFee
34:     ) external;
35: 
36:     function updateStakeAndTotalStakes(bytes32 _cdpId) external returns (uint256);
37: 
38:     function syncAccounting(bytes32 _cdpId) external;
39: 
40:     function closeCdp(bytes32 _cdpId, address _borrower, uint256 _debt, uint256 _coll) external;
41: 
42:     function getRedemptionRate() external view returns (uint256);
43: 
44:     function getRedemptionRateWithDecay() external view returns (uint256);
45: 
46:     function getRedemptionFeeWithDecay(uint256 _stETHToRedeem) external view returns (uint256);
47: 
48:     function getCdpStatus(bytes32 _cdpId) external view returns (uint256);
49: 
50:     function getCdpStake(bytes32 _cdpId) external view returns (uint256);
51: 
52:     function getCdpDebt(bytes32 _cdpId) external view returns (uint256);
53: 
54:     function getCdpCollShares(bytes32 _cdpId) external view returns (uint256);
55: 
56:     function getCdpLiquidatorRewardShares(bytes32 _cdpId) external view returns (uint);
57: 
58:     function initializeCdp(
59:         bytes32 _cdpId,
60:         uint256 _debt,
61:         uint256 _coll,
62:         uint256 _liquidatorRewardShares,
63:         address _borrower
64:     ) external;
65: 
66:     function updateCdp(
67:         bytes32 _cdpId,
68:         address _borrower,
69:         uint256 _coll,
70:         uint256 _debt,
71:         uint256 _newColl,
72:         uint256 _newDebt
73:     ) external;
74: 
75:     function getCachedTCR(uint256 _price) external view returns (uint256);
76: 
77:     function checkRecoveryMode(uint256 _price) external view returns (bool);
78: }
79: 

//@audit  ,_cdpId ,_upperPartialHint ,_lowerPartialHint are not checked
17:     function partiallyLiquidate(
18:         bytes32 _cdpId,
19:         uint256 _partialAmount,
20:         bytes32 _upperPartialHint,
21:         bytes32 _lowerPartialHint
22:     ) external;
23: 
24:     function batchLiquidateCdps(bytes32[] calldata _cdpArray) external;
25: 
26:     function redeemCollateral(
27:         uint256 _EBTCAmount,
28:         bytes32 _firstRedemptionHint,
29:         bytes32 _upperPartialRedemptionHint,
30:         bytes32 _lowerPartialRedemptionHint,
31:         uint256 _partialRedemptionHintNICR,
32:         uint256 _maxIterations,
33:         uint256 _maxFee
34:     ) external;
35: 
36:     function updateStakeAndTotalStakes(bytes32 _cdpId) external returns (uint256);
37: 
38:     function syncAccounting(bytes32 _cdpId) external;
39: 
40:     function closeCdp(bytes32 _cdpId, address _borrower, uint256 _debt, uint256 _coll) external;
41: 
42:     function getRedemptionRate() external view returns (uint256);
43: 
44:     function getRedemptionRateWithDecay() external view returns (uint256);
45: 
46:     function getRedemptionFeeWithDecay(uint256 _stETHToRedeem) external view returns (uint256);
47: 
48:     function getCdpStatus(bytes32 _cdpId) external view returns (uint256);
49: 
50:     function getCdpStake(bytes32 _cdpId) external view returns (uint256);
51: 
52:     function getCdpDebt(bytes32 _cdpId) external view returns (uint256);
53: 
54:     function getCdpCollShares(bytes32 _cdpId) external view returns (uint256);
55: 
56:     function getCdpLiquidatorRewardShares(bytes32 _cdpId) external view returns (uint);
57: 
58:     function initializeCdp(
59:         bytes32 _cdpId,
60:         uint256 _debt,
61:         uint256 _coll,
62:         uint256 _liquidatorRewardShares,
63:         address _borrower
64:     ) external;
65: 
66:     function updateCdp(
67:         bytes32 _cdpId,
68:         address _borrower,
69:         uint256 _coll,
70:         uint256 _debt,
71:         uint256 _newColl,
72:         uint256 _newDebt
73:     ) external;
74: 
75:     function getCachedTCR(uint256 _price) external view returns (uint256);
76: 
77:     function checkRecoveryMode(uint256 _price) external view returns (bool);
78: }
79: 

//@audit  ,_firstRedemptionHint ,_upperPartialRedemptionHint ,_lowerPartialRedemptionHint are not checked
26:     function redeemCollateral(
27:         uint256 _EBTCAmount,
28:         bytes32 _firstRedemptionHint,
29:         bytes32 _upperPartialRedemptionHint,
30:         bytes32 _lowerPartialRedemptionHint,
31:         uint256 _partialRedemptionHintNICR,
32:         uint256 _maxIterations,
33:         uint256 _maxFee
34:     ) external;
35: 
36:     function updateStakeAndTotalStakes(bytes32 _cdpId) external returns (uint256);
37: 
38:     function syncAccounting(bytes32 _cdpId) external;
39: 
40:     function closeCdp(bytes32 _cdpId, address _borrower, uint256 _debt, uint256 _coll) external;
41: 
42:     function getRedemptionRate() external view returns (uint256);
43: 
44:     function getRedemptionRateWithDecay() external view returns (uint256);
45: 
46:     function getRedemptionFeeWithDecay(uint256 _stETHToRedeem) external view returns (uint256);
47: 
48:     function getCdpStatus(bytes32 _cdpId) external view returns (uint256);
49: 
50:     function getCdpStake(bytes32 _cdpId) external view returns (uint256);
51: 
52:     function getCdpDebt(bytes32 _cdpId) external view returns (uint256);
53: 
54:     function getCdpCollShares(bytes32 _cdpId) external view returns (uint256);
55: 
56:     function getCdpLiquidatorRewardShares(bytes32 _cdpId) external view returns (uint);
57: 
58:     function initializeCdp(
59:         bytes32 _cdpId,
60:         uint256 _debt,
61:         uint256 _coll,
62:         uint256 _liquidatorRewardShares,
63:         address _borrower
64:     ) external;
65: 
66:     function updateCdp(
67:         bytes32 _cdpId,
68:         address _borrower,
69:         uint256 _coll,
70:         uint256 _debt,
71:         uint256 _newColl,
72:         uint256 _newDebt
73:     ) external;
74: 
75:     function getCachedTCR(uint256 _price) external view returns (uint256);
76: 
77:     function checkRecoveryMode(uint256 _price) external view returns (bool);
78: }
79: 

//@audit  ,_cdpId are not checked
36:     function updateStakeAndTotalStakes(bytes32 _cdpId) external returns (uint256);
37: 
38:     function syncAccounting(bytes32 _cdpId) external;
39: 
40:     function closeCdp(bytes32 _cdpId, address _borrower, uint256 _debt, uint256 _coll) external;
41: 
42:     function getRedemptionRate() external view returns (uint256);
43: 
44:     function getRedemptionRateWithDecay() external view returns (uint256);
45: 
46:     function getRedemptionFeeWithDecay(uint256 _stETHToRedeem) external view returns (uint256);
47: 
48:     function getCdpStatus(bytes32 _cdpId) external view returns (uint256);
49: 
50:     function getCdpStake(bytes32 _cdpId) external view returns (uint256);
51: 
52:     function getCdpDebt(bytes32 _cdpId) external view returns (uint256);
53: 
54:     function getCdpCollShares(bytes32 _cdpId) external view returns (uint256);
55: 
56:     function getCdpLiquidatorRewardShares(bytes32 _cdpId) external view returns (uint);
57: 
58:     function initializeCdp(
59:         bytes32 _cdpId,
60:         uint256 _debt,
61:         uint256 _coll,
62:         uint256 _liquidatorRewardShares,
63:         address _borrower
64:     ) external;
65: 
66:     function updateCdp(
67:         bytes32 _cdpId,
68:         address _borrower,
69:         uint256 _coll,
70:         uint256 _debt,
71:         uint256 _newColl,
72:         uint256 _newDebt
73:     ) external;
74: 
75:     function getCachedTCR(uint256 _price) external view returns (uint256);
76: 
77:     function checkRecoveryMode(uint256 _price) external view returns (bool);
78: }
79: 

//@audit  ,_cdpId are not checked
38:     function syncAccounting(bytes32 _cdpId) external;
39: 
40:     function closeCdp(bytes32 _cdpId, address _borrower, uint256 _debt, uint256 _coll) external;
41: 
42:     function getRedemptionRate() external view returns (uint256);
43: 
44:     function getRedemptionRateWithDecay() external view returns (uint256);
45: 
46:     function getRedemptionFeeWithDecay(uint256 _stETHToRedeem) external view returns (uint256);
47: 
48:     function getCdpStatus(bytes32 _cdpId) external view returns (uint256);
49: 
50:     function getCdpStake(bytes32 _cdpId) external view returns (uint256);
51: 
52:     function getCdpDebt(bytes32 _cdpId) external view returns (uint256);
53: 
54:     function getCdpCollShares(bytes32 _cdpId) external view returns (uint256);
55: 
56:     function getCdpLiquidatorRewardShares(bytes32 _cdpId) external view returns (uint);
57: 
58:     function initializeCdp(
59:         bytes32 _cdpId,
60:         uint256 _debt,
61:         uint256 _coll,
62:         uint256 _liquidatorRewardShares,
63:         address _borrower
64:     ) external;
65: 
66:     function updateCdp(
67:         bytes32 _cdpId,
68:         address _borrower,
69:         uint256 _coll,
70:         uint256 _debt,
71:         uint256 _newColl,
72:         uint256 _newDebt
73:     ) external;
74: 
75:     function getCachedTCR(uint256 _price) external view returns (uint256);
76: 
77:     function checkRecoveryMode(uint256 _price) external view returns (bool);
78: }
79: 

//@audit  ,_cdpId are not checked
40:     function closeCdp(bytes32 _cdpId, address _borrower, uint256 _debt, uint256 _coll) external;
41: 
42:     function getRedemptionRate() external view returns (uint256);
43: 
44:     function getRedemptionRateWithDecay() external view returns (uint256);
45: 
46:     function getRedemptionFeeWithDecay(uint256 _stETHToRedeem) external view returns (uint256);
47: 
48:     function getCdpStatus(bytes32 _cdpId) external view returns (uint256);
49: 
50:     function getCdpStake(bytes32 _cdpId) external view returns (uint256);
51: 
52:     function getCdpDebt(bytes32 _cdpId) external view returns (uint256);
53: 
54:     function getCdpCollShares(bytes32 _cdpId) external view returns (uint256);
55: 
56:     function getCdpLiquidatorRewardShares(bytes32 _cdpId) external view returns (uint);
57: 
58:     function initializeCdp(
59:         bytes32 _cdpId,
60:         uint256 _debt,
61:         uint256 _coll,
62:         uint256 _liquidatorRewardShares,
63:         address _borrower
64:     ) external;
65: 
66:     function updateCdp(
67:         bytes32 _cdpId,
68:         address _borrower,
69:         uint256 _coll,
70:         uint256 _debt,
71:         uint256 _newColl,
72:         uint256 _newDebt
73:     ) external;
74: 
75:     function getCachedTCR(uint256 _price) external view returns (uint256);
76: 
77:     function checkRecoveryMode(uint256 _price) external view returns (bool);
78: }
79: 

//@audit  ,_cdpId are not checked
48:     function getCdpStatus(bytes32 _cdpId) external view returns (uint256);
49: 
50:     function getCdpStake(bytes32 _cdpId) external view returns (uint256);
51: 
52:     function getCdpDebt(bytes32 _cdpId) external view returns (uint256);
53: 
54:     function getCdpCollShares(bytes32 _cdpId) external view returns (uint256);
55: 
56:     function getCdpLiquidatorRewardShares(bytes32 _cdpId) external view returns (uint);
57: 
58:     function initializeCdp(
59:         bytes32 _cdpId,
60:         uint256 _debt,
61:         uint256 _coll,
62:         uint256 _liquidatorRewardShares,
63:         address _borrower
64:     ) external;
65: 
66:     function updateCdp(
67:         bytes32 _cdpId,
68:         address _borrower,
69:         uint256 _coll,
70:         uint256 _debt,
71:         uint256 _newColl,
72:         uint256 _newDebt
73:     ) external;
74: 
75:     function getCachedTCR(uint256 _price) external view returns (uint256);
76: 
77:     function checkRecoveryMode(uint256 _price) external view returns (bool);
78: }
79: 

//@audit  ,_cdpId are not checked
50:     function getCdpStake(bytes32 _cdpId) external view returns (uint256);
51: 
52:     function getCdpDebt(bytes32 _cdpId) external view returns (uint256);
53: 
54:     function getCdpCollShares(bytes32 _cdpId) external view returns (uint256);
55: 
56:     function getCdpLiquidatorRewardShares(bytes32 _cdpId) external view returns (uint);
57: 
58:     function initializeCdp(
59:         bytes32 _cdpId,
60:         uint256 _debt,
61:         uint256 _coll,
62:         uint256 _liquidatorRewardShares,
63:         address _borrower
64:     ) external;
65: 
66:     function updateCdp(
67:         bytes32 _cdpId,
68:         address _borrower,
69:         uint256 _coll,
70:         uint256 _debt,
71:         uint256 _newColl,
72:         uint256 _newDebt
73:     ) external;
74: 
75:     function getCachedTCR(uint256 _price) external view returns (uint256);
76: 
77:     function checkRecoveryMode(uint256 _price) external view returns (bool);
78: }
79: 

//@audit  ,_cdpId are not checked
52:     function getCdpDebt(bytes32 _cdpId) external view returns (uint256);
53: 
54:     function getCdpCollShares(bytes32 _cdpId) external view returns (uint256);
55: 
56:     function getCdpLiquidatorRewardShares(bytes32 _cdpId) external view returns (uint);
57: 
58:     function initializeCdp(
59:         bytes32 _cdpId,
60:         uint256 _debt,
61:         uint256 _coll,
62:         uint256 _liquidatorRewardShares,
63:         address _borrower
64:     ) external;
65: 
66:     function updateCdp(
67:         bytes32 _cdpId,
68:         address _borrower,
69:         uint256 _coll,
70:         uint256 _debt,
71:         uint256 _newColl,
72:         uint256 _newDebt
73:     ) external;
74: 
75:     function getCachedTCR(uint256 _price) external view returns (uint256);
76: 
77:     function checkRecoveryMode(uint256 _price) external view returns (bool);
78: }
79: 

//@audit  ,_cdpId are not checked
54:     function getCdpCollShares(bytes32 _cdpId) external view returns (uint256);
55: 
56:     function getCdpLiquidatorRewardShares(bytes32 _cdpId) external view returns (uint);
57: 
58:     function initializeCdp(
59:         bytes32 _cdpId,
60:         uint256 _debt,
61:         uint256 _coll,
62:         uint256 _liquidatorRewardShares,
63:         address _borrower
64:     ) external;
65: 
66:     function updateCdp(
67:         bytes32 _cdpId,
68:         address _borrower,
69:         uint256 _coll,
70:         uint256 _debt,
71:         uint256 _newColl,
72:         uint256 _newDebt
73:     ) external;
74: 
75:     function getCachedTCR(uint256 _price) external view returns (uint256);
76: 
77:     function checkRecoveryMode(uint256 _price) external view returns (bool);
78: }
79: 

//@audit  ,_cdpId are not checked
56:     function getCdpLiquidatorRewardShares(bytes32 _cdpId) external view returns (uint);
57: 
58:     function initializeCdp(
59:         bytes32 _cdpId,
60:         uint256 _debt,
61:         uint256 _coll,
62:         uint256 _liquidatorRewardShares,
63:         address _borrower
64:     ) external;
65: 
66:     function updateCdp(
67:         bytes32 _cdpId,
68:         address _borrower,
69:         uint256 _coll,
70:         uint256 _debt,
71:         uint256 _newColl,
72:         uint256 _newDebt
73:     ) external;
74: 
75:     function getCachedTCR(uint256 _price) external view returns (uint256);
76: 
77:     function checkRecoveryMode(uint256 _price) external view returns (bool);
78: }
79: 

//@audit  ,_cdpId are not checked
58:     function initializeCdp(
59:         bytes32 _cdpId,
60:         uint256 _debt,
61:         uint256 _coll,
62:         uint256 _liquidatorRewardShares,
63:         address _borrower
64:     ) external;
65: 
66:     function updateCdp(
67:         bytes32 _cdpId,
68:         address _borrower,
69:         uint256 _coll,
70:         uint256 _debt,
71:         uint256 _newColl,
72:         uint256 _newDebt
73:     ) external;
74: 
75:     function getCachedTCR(uint256 _price) external view returns (uint256);
76: 
77:     function checkRecoveryMode(uint256 _price) external view returns (bool);
78: }
79: 

//@audit  ,_cdpId are not checked
66:     function updateCdp(
67:         bytes32 _cdpId,
68:         address _borrower,
69:         uint256 _coll,
70:         uint256 _debt,
71:         uint256 _newColl,
72:         uint256 _newDebt
73:     ) external;
74: 
75:     function getCachedTCR(uint256 _price) external view returns (uint256);
76: 
77:     function checkRecoveryMode(uint256 _price) external view returns (bool);
78: }
79: 


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManager.sol#L15-L79) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManager.sol#L17-L79), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManager.sol#L26-L79), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManager.sol#L36-L79), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManager.sol#L38-L79), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManager.sol#L40-L79), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManager.sol#L48-L79), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManager.sol#L50-L79), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManager.sol#L52-L79), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManager.sol#L54-L79), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManager.sol#L56-L79), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManager.sol#L58-L79), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManager.sol#L66-L79)


```solidity

File: packages/contracts/contracts/Interfaces/ICdpManagerData.sol

//@audit  ,_cdpId are not checked
236:     function getAccumulatedFeeSplitApplied(
237:         bytes32 _cdpId,
238:         uint256 _systemStEthFeePerUnitIndex
239:     ) external view returns (uint256, uint256);
240: 
241:     function getCachedNominalICR(bytes32 _cdpId) external view returns (uint256);
242: 
243:     function getCachedICR(bytes32 _cdpId, uint256 _price) external view returns (uint256);
244: 
245:     function getSyncedCdpDebt(bytes32 _cdpId) external view returns (uint256);
246: 
247:     function getSyncedCdpCollShares(bytes32 _cdpId) external view returns (uint256);
248: 
249:     function getSyncedICR(bytes32 _cdpId, uint256 _price) external view returns (uint256);
250: 
251:     function getSyncedTCR(uint256 _price) external view returns (uint256);
252: 
253:     function getSyncedNominalICR(bytes32 _cdpId) external view returns (uint256);
254: 
255:     function getPendingRedistributedDebt(bytes32 _cdpId) external view returns (uint256);
256: 
257:     function hasPendingRedistributedDebt(bytes32 _cdpId) external view returns (bool);
258: 
259:     function getSyncedDebtAndCollShares(
260:         bytes32 _cdpId
261:     ) external view returns (uint256 debt, uint256 collShares);
262: 
263:     function canLiquidateRecoveryMode(uint256 icr, uint256 tcr) external view returns (bool);
264: }
265: 

//@audit  ,_cdpId are not checked
241:     function getCachedNominalICR(bytes32 _cdpId) external view returns (uint256);
242: 
243:     function getCachedICR(bytes32 _cdpId, uint256 _price) external view returns (uint256);
244: 
245:     function getSyncedCdpDebt(bytes32 _cdpId) external view returns (uint256);
246: 
247:     function getSyncedCdpCollShares(bytes32 _cdpId) external view returns (uint256);
248: 
249:     function getSyncedICR(bytes32 _cdpId, uint256 _price) external view returns (uint256);
250: 
251:     function getSyncedTCR(uint256 _price) external view returns (uint256);
252: 
253:     function getSyncedNominalICR(bytes32 _cdpId) external view returns (uint256);
254: 
255:     function getPendingRedistributedDebt(bytes32 _cdpId) external view returns (uint256);
256: 
257:     function hasPendingRedistributedDebt(bytes32 _cdpId) external view returns (bool);
258: 
259:     function getSyncedDebtAndCollShares(
260:         bytes32 _cdpId
261:     ) external view returns (uint256 debt, uint256 collShares);
262: 
263:     function canLiquidateRecoveryMode(uint256 icr, uint256 tcr) external view returns (bool);
264: }
265: 

//@audit  ,_cdpId are not checked
243:     function getCachedICR(bytes32 _cdpId, uint256 _price) external view returns (uint256);
244: 
245:     function getSyncedCdpDebt(bytes32 _cdpId) external view returns (uint256);
246: 
247:     function getSyncedCdpCollShares(bytes32 _cdpId) external view returns (uint256);
248: 
249:     function getSyncedICR(bytes32 _cdpId, uint256 _price) external view returns (uint256);
250: 
251:     function getSyncedTCR(uint256 _price) external view returns (uint256);
252: 
253:     function getSyncedNominalICR(bytes32 _cdpId) external view returns (uint256);
254: 
255:     function getPendingRedistributedDebt(bytes32 _cdpId) external view returns (uint256);
256: 
257:     function hasPendingRedistributedDebt(bytes32 _cdpId) external view returns (bool);
258: 
259:     function getSyncedDebtAndCollShares(
260:         bytes32 _cdpId
261:     ) external view returns (uint256 debt, uint256 collShares);
262: 
263:     function canLiquidateRecoveryMode(uint256 icr, uint256 tcr) external view returns (bool);
264: }
265: 

//@audit  ,_cdpId are not checked
245:     function getSyncedCdpDebt(bytes32 _cdpId) external view returns (uint256);
246: 
247:     function getSyncedCdpCollShares(bytes32 _cdpId) external view returns (uint256);
248: 
249:     function getSyncedICR(bytes32 _cdpId, uint256 _price) external view returns (uint256);
250: 
251:     function getSyncedTCR(uint256 _price) external view returns (uint256);
252: 
253:     function getSyncedNominalICR(bytes32 _cdpId) external view returns (uint256);
254: 
255:     function getPendingRedistributedDebt(bytes32 _cdpId) external view returns (uint256);
256: 
257:     function hasPendingRedistributedDebt(bytes32 _cdpId) external view returns (bool);
258: 
259:     function getSyncedDebtAndCollShares(
260:         bytes32 _cdpId
261:     ) external view returns (uint256 debt, uint256 collShares);
262: 
263:     function canLiquidateRecoveryMode(uint256 icr, uint256 tcr) external view returns (bool);
264: }
265: 

//@audit  ,_cdpId are not checked
247:     function getSyncedCdpCollShares(bytes32 _cdpId) external view returns (uint256);
248: 
249:     function getSyncedICR(bytes32 _cdpId, uint256 _price) external view returns (uint256);
250: 
251:     function getSyncedTCR(uint256 _price) external view returns (uint256);
252: 
253:     function getSyncedNominalICR(bytes32 _cdpId) external view returns (uint256);
254: 
255:     function getPendingRedistributedDebt(bytes32 _cdpId) external view returns (uint256);
256: 
257:     function hasPendingRedistributedDebt(bytes32 _cdpId) external view returns (bool);
258: 
259:     function getSyncedDebtAndCollShares(
260:         bytes32 _cdpId
261:     ) external view returns (uint256 debt, uint256 collShares);
262: 
263:     function canLiquidateRecoveryMode(uint256 icr, uint256 tcr) external view returns (bool);
264: }
265: 

//@audit  ,_cdpId are not checked
249:     function getSyncedICR(bytes32 _cdpId, uint256 _price) external view returns (uint256);
250: 
251:     function getSyncedTCR(uint256 _price) external view returns (uint256);
252: 
253:     function getSyncedNominalICR(bytes32 _cdpId) external view returns (uint256);
254: 
255:     function getPendingRedistributedDebt(bytes32 _cdpId) external view returns (uint256);
256: 
257:     function hasPendingRedistributedDebt(bytes32 _cdpId) external view returns (bool);
258: 
259:     function getSyncedDebtAndCollShares(
260:         bytes32 _cdpId
261:     ) external view returns (uint256 debt, uint256 collShares);
262: 
263:     function canLiquidateRecoveryMode(uint256 icr, uint256 tcr) external view returns (bool);
264: }
265: 

//@audit  ,_cdpId are not checked
253:     function getSyncedNominalICR(bytes32 _cdpId) external view returns (uint256);
254: 
255:     function getPendingRedistributedDebt(bytes32 _cdpId) external view returns (uint256);
256: 
257:     function hasPendingRedistributedDebt(bytes32 _cdpId) external view returns (bool);
258: 
259:     function getSyncedDebtAndCollShares(
260:         bytes32 _cdpId
261:     ) external view returns (uint256 debt, uint256 collShares);
262: 
263:     function canLiquidateRecoveryMode(uint256 icr, uint256 tcr) external view returns (bool);
264: }
265: 

//@audit  ,_cdpId are not checked
255:     function getPendingRedistributedDebt(bytes32 _cdpId) external view returns (uint256);
256: 
257:     function hasPendingRedistributedDebt(bytes32 _cdpId) external view returns (bool);
258: 
259:     function getSyncedDebtAndCollShares(
260:         bytes32 _cdpId
261:     ) external view returns (uint256 debt, uint256 collShares);
262: 
263:     function canLiquidateRecoveryMode(uint256 icr, uint256 tcr) external view returns (bool);
264: }
265: 

//@audit  ,_cdpId are not checked
257:     function hasPendingRedistributedDebt(bytes32 _cdpId) external view returns (bool);
258: 
259:     function getSyncedDebtAndCollShares(
260:         bytes32 _cdpId
261:     ) external view returns (uint256 debt, uint256 collShares);
262: 
263:     function canLiquidateRecoveryMode(uint256 icr, uint256 tcr) external view returns (bool);
264: }
265: 

//@audit  ,_cdpId are not checked
259:     function getSyncedDebtAndCollShares(
260:         bytes32 _cdpId
261:     ) external view returns (uint256 debt, uint256 collShares);
262: 
263:     function canLiquidateRecoveryMode(uint256 icr, uint256 tcr) external view returns (bool);
264: }
265: 


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L236-L265) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L241-L265), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L243-L265), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L245-L265), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L247-L265), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L249-L265), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L253-L265), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L255-L265), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L257-L265), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L259-L265)


```solidity

File: packages/contracts/contracts/Interfaces/IERC3156FlashBorrower.sol

//@audit  ,data are not checked
15:     function onFlashLoan(
16:         address initiator,
17:         address token,
18:         uint256 amount,
19:         uint256 fee,
20:         bytes calldata data
21:     ) external returns (bytes32);
22: }
23: 


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IERC3156FlashBorrower.sol#L15-L23) 


```solidity

File: packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol

//@audit  ,data are not checked
28:     function flashLoan(
29:         IERC3156FlashBorrower receiver,
30:         address token,
31:         uint256 amount,
32:         bytes calldata data
33:     ) external returns (bool);
34: }
35: 


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol#L28-L35) 


```solidity

File: packages/contracts/contracts/Interfaces/IPositionManagers.sol

//@audit  ,r ,s are not checked
32:     function permitPositionManagerApproval(
33:         address _borrower,
34:         address _positionManager,
35:         PositionManagerApproval _approval,
36:         uint _deadline,
37:         uint8 v,
38:         bytes32 r,
39:         bytes32 s
40:     ) external;
41: 
42:     function version() external view returns (string memory);
43: 
44:     function permitTypeHash() external view returns (bytes32);
45: 
46:     function domainSeparator() external view returns (bytes32);
47: }
48: 


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPositionManagers.sol#L32-L48) 


```solidity

File: packages/contracts/contracts/Interfaces/ISortedCdps.sol

//@audit  ,_id are not checked
14:     function remove(bytes32 _id) external;
15: 
16:     function batchRemove(bytes32[] memory _ids) external;
17: 
18:     function reInsert(bytes32 _id, uint256 _newICR, bytes32 _prevId, bytes32 _nextId) external;
19: 
20:     function contains(bytes32 _id) external view returns (bool);
21: 
22:     function isFull() external view returns (bool);
23: 
24:     function isEmpty() external view returns (bool);
25: 
26:     function getSize() external view returns (uint256);
27: 
28:     function getMaxSize() external view returns (uint256);
29: 
30:     function getFirst() external view returns (bytes32);
31: 
32:     function getLast() external view returns (bytes32);
33: 
34:     function getNext(bytes32 _id) external view returns (bytes32);
35: 
36:     function getPrev(bytes32 _id) external view returns (bytes32);
37: 
38:     function validInsertPosition(
39:         uint256 _ICR,
40:         bytes32 _prevId,
41:         bytes32 _nextId
42:     ) external view returns (bool);
43: 
44:     function findInsertPosition(
45:         uint256 _ICR,
46:         bytes32 _prevId,
47:         bytes32 _nextId
48:     ) external view returns (bytes32, bytes32);
49: 
50:     function insert(
51:         address owner,
52:         uint256 _ICR,
53:         bytes32 _prevId,
54:         bytes32 _nextId
55:     ) external returns (bytes32);
56: 
57:     function getOwnerAddress(bytes32 _id) external pure returns (address);
58: 
59:     function nonExistId() external view returns (bytes32);
60: 
61:     function cdpCountOf(address owner) external view returns (uint256);
62: 
63:     function getCdpCountOf(
64:         address owner,
65:         bytes32 startNodeId,
66:         uint maxNodes
67:     ) external view returns (uint256, bytes32);
68: 
69:     function getCdpsOf(address owner) external view returns (bytes32[] memory);
70: 
71:     function getAllCdpsOf(
72:         address owner,
73:         bytes32 startNodeId,
74:         uint maxNodes
75:     ) external view returns (bytes32[] memory, uint256, bytes32);
76: 
77:     function cdpOfOwnerByIndex(address owner, uint256 index) external view returns (bytes32);
78: 
79:     function cdpOfOwnerByIdx(
80:         address owner,
81:         uint256 index,
82:         bytes32 startNodeId,
83:         uint maxNodes
84:     ) external view returns (bytes32, bool);
85: }
86: 

//@audit  ,_id ,_prevId ,_nextId are not checked
18:     function reInsert(bytes32 _id, uint256 _newICR, bytes32 _prevId, bytes32 _nextId) external;
19: 
20:     function contains(bytes32 _id) external view returns (bool);
21: 
22:     function isFull() external view returns (bool);
23: 
24:     function isEmpty() external view returns (bool);
25: 
26:     function getSize() external view returns (uint256);
27: 
28:     function getMaxSize() external view returns (uint256);
29: 
30:     function getFirst() external view returns (bytes32);
31: 
32:     function getLast() external view returns (bytes32);
33: 
34:     function getNext(bytes32 _id) external view returns (bytes32);
35: 
36:     function getPrev(bytes32 _id) external view returns (bytes32);
37: 
38:     function validInsertPosition(
39:         uint256 _ICR,
40:         bytes32 _prevId,
41:         bytes32 _nextId
42:     ) external view returns (bool);
43: 
44:     function findInsertPosition(
45:         uint256 _ICR,
46:         bytes32 _prevId,
47:         bytes32 _nextId
48:     ) external view returns (bytes32, bytes32);
49: 
50:     function insert(
51:         address owner,
52:         uint256 _ICR,
53:         bytes32 _prevId,
54:         bytes32 _nextId
55:     ) external returns (bytes32);
56: 
57:     function getOwnerAddress(bytes32 _id) external pure returns (address);
58: 
59:     function nonExistId() external view returns (bytes32);
60: 
61:     function cdpCountOf(address owner) external view returns (uint256);
62: 
63:     function getCdpCountOf(
64:         address owner,
65:         bytes32 startNodeId,
66:         uint maxNodes
67:     ) external view returns (uint256, bytes32);
68: 
69:     function getCdpsOf(address owner) external view returns (bytes32[] memory);
70: 
71:     function getAllCdpsOf(
72:         address owner,
73:         bytes32 startNodeId,
74:         uint maxNodes
75:     ) external view returns (bytes32[] memory, uint256, bytes32);
76: 
77:     function cdpOfOwnerByIndex(address owner, uint256 index) external view returns (bytes32);
78: 
79:     function cdpOfOwnerByIdx(
80:         address owner,
81:         uint256 index,
82:         bytes32 startNodeId,
83:         uint maxNodes
84:     ) external view returns (bytes32, bool);
85: }
86: 

//@audit  ,_id are not checked
20:     function contains(bytes32 _id) external view returns (bool);
21: 
22:     function isFull() external view returns (bool);
23: 
24:     function isEmpty() external view returns (bool);
25: 
26:     function getSize() external view returns (uint256);
27: 
28:     function getMaxSize() external view returns (uint256);
29: 
30:     function getFirst() external view returns (bytes32);
31: 
32:     function getLast() external view returns (bytes32);
33: 
34:     function getNext(bytes32 _id) external view returns (bytes32);
35: 
36:     function getPrev(bytes32 _id) external view returns (bytes32);
37: 
38:     function validInsertPosition(
39:         uint256 _ICR,
40:         bytes32 _prevId,
41:         bytes32 _nextId
42:     ) external view returns (bool);
43: 
44:     function findInsertPosition(
45:         uint256 _ICR,
46:         bytes32 _prevId,
47:         bytes32 _nextId
48:     ) external view returns (bytes32, bytes32);
49: 
50:     function insert(
51:         address owner,
52:         uint256 _ICR,
53:         bytes32 _prevId,
54:         bytes32 _nextId
55:     ) external returns (bytes32);
56: 
57:     function getOwnerAddress(bytes32 _id) external pure returns (address);
58: 
59:     function nonExistId() external view returns (bytes32);
60: 
61:     function cdpCountOf(address owner) external view returns (uint256);
62: 
63:     function getCdpCountOf(
64:         address owner,
65:         bytes32 startNodeId,
66:         uint maxNodes
67:     ) external view returns (uint256, bytes32);
68: 
69:     function getCdpsOf(address owner) external view returns (bytes32[] memory);
70: 
71:     function getAllCdpsOf(
72:         address owner,
73:         bytes32 startNodeId,
74:         uint maxNodes
75:     ) external view returns (bytes32[] memory, uint256, bytes32);
76: 
77:     function cdpOfOwnerByIndex(address owner, uint256 index) external view returns (bytes32);
78: 
79:     function cdpOfOwnerByIdx(
80:         address owner,
81:         uint256 index,
82:         bytes32 startNodeId,
83:         uint maxNodes
84:     ) external view returns (bytes32, bool);
85: }
86: 

//@audit  ,_id are not checked
34:     function getNext(bytes32 _id) external view returns (bytes32);
35: 
36:     function getPrev(bytes32 _id) external view returns (bytes32);
37: 
38:     function validInsertPosition(
39:         uint256 _ICR,
40:         bytes32 _prevId,
41:         bytes32 _nextId
42:     ) external view returns (bool);
43: 
44:     function findInsertPosition(
45:         uint256 _ICR,
46:         bytes32 _prevId,
47:         bytes32 _nextId
48:     ) external view returns (bytes32, bytes32);
49: 
50:     function insert(
51:         address owner,
52:         uint256 _ICR,
53:         bytes32 _prevId,
54:         bytes32 _nextId
55:     ) external returns (bytes32);
56: 
57:     function getOwnerAddress(bytes32 _id) external pure returns (address);
58: 
59:     function nonExistId() external view returns (bytes32);
60: 
61:     function cdpCountOf(address owner) external view returns (uint256);
62: 
63:     function getCdpCountOf(
64:         address owner,
65:         bytes32 startNodeId,
66:         uint maxNodes
67:     ) external view returns (uint256, bytes32);
68: 
69:     function getCdpsOf(address owner) external view returns (bytes32[] memory);
70: 
71:     function getAllCdpsOf(
72:         address owner,
73:         bytes32 startNodeId,
74:         uint maxNodes
75:     ) external view returns (bytes32[] memory, uint256, bytes32);
76: 
77:     function cdpOfOwnerByIndex(address owner, uint256 index) external view returns (bytes32);
78: 
79:     function cdpOfOwnerByIdx(
80:         address owner,
81:         uint256 index,
82:         bytes32 startNodeId,
83:         uint maxNodes
84:     ) external view returns (bytes32, bool);
85: }
86: 

//@audit  ,_id are not checked
36:     function getPrev(bytes32 _id) external view returns (bytes32);
37: 
38:     function validInsertPosition(
39:         uint256 _ICR,
40:         bytes32 _prevId,
41:         bytes32 _nextId
42:     ) external view returns (bool);
43: 
44:     function findInsertPosition(
45:         uint256 _ICR,
46:         bytes32 _prevId,
47:         bytes32 _nextId
48:     ) external view returns (bytes32, bytes32);
49: 
50:     function insert(
51:         address owner,
52:         uint256 _ICR,
53:         bytes32 _prevId,
54:         bytes32 _nextId
55:     ) external returns (bytes32);
56: 
57:     function getOwnerAddress(bytes32 _id) external pure returns (address);
58: 
59:     function nonExistId() external view returns (bytes32);
60: 
61:     function cdpCountOf(address owner) external view returns (uint256);
62: 
63:     function getCdpCountOf(
64:         address owner,
65:         bytes32 startNodeId,
66:         uint maxNodes
67:     ) external view returns (uint256, bytes32);
68: 
69:     function getCdpsOf(address owner) external view returns (bytes32[] memory);
70: 
71:     function getAllCdpsOf(
72:         address owner,
73:         bytes32 startNodeId,
74:         uint maxNodes
75:     ) external view returns (bytes32[] memory, uint256, bytes32);
76: 
77:     function cdpOfOwnerByIndex(address owner, uint256 index) external view returns (bytes32);
78: 
79:     function cdpOfOwnerByIdx(
80:         address owner,
81:         uint256 index,
82:         bytes32 startNodeId,
83:         uint maxNodes
84:     ) external view returns (bytes32, bool);
85: }
86: 

//@audit  ,_prevId ,_nextId are not checked
38:     function validInsertPosition(
39:         uint256 _ICR,
40:         bytes32 _prevId,
41:         bytes32 _nextId
42:     ) external view returns (bool);
43: 
44:     function findInsertPosition(
45:         uint256 _ICR,
46:         bytes32 _prevId,
47:         bytes32 _nextId
48:     ) external view returns (bytes32, bytes32);
49: 
50:     function insert(
51:         address owner,
52:         uint256 _ICR,
53:         bytes32 _prevId,
54:         bytes32 _nextId
55:     ) external returns (bytes32);
56: 
57:     function getOwnerAddress(bytes32 _id) external pure returns (address);
58: 
59:     function nonExistId() external view returns (bytes32);
60: 
61:     function cdpCountOf(address owner) external view returns (uint256);
62: 
63:     function getCdpCountOf(
64:         address owner,
65:         bytes32 startNodeId,
66:         uint maxNodes
67:     ) external view returns (uint256, bytes32);
68: 
69:     function getCdpsOf(address owner) external view returns (bytes32[] memory);
70: 
71:     function getAllCdpsOf(
72:         address owner,
73:         bytes32 startNodeId,
74:         uint maxNodes
75:     ) external view returns (bytes32[] memory, uint256, bytes32);
76: 
77:     function cdpOfOwnerByIndex(address owner, uint256 index) external view returns (bytes32);
78: 
79:     function cdpOfOwnerByIdx(
80:         address owner,
81:         uint256 index,
82:         bytes32 startNodeId,
83:         uint maxNodes
84:     ) external view returns (bytes32, bool);
85: }
86: 

//@audit  ,_prevId ,_nextId are not checked
44:     function findInsertPosition(
45:         uint256 _ICR,
46:         bytes32 _prevId,
47:         bytes32 _nextId
48:     ) external view returns (bytes32, bytes32);
49: 
50:     function insert(
51:         address owner,
52:         uint256 _ICR,
53:         bytes32 _prevId,
54:         bytes32 _nextId
55:     ) external returns (bytes32);
56: 
57:     function getOwnerAddress(bytes32 _id) external pure returns (address);
58: 
59:     function nonExistId() external view returns (bytes32);
60: 
61:     function cdpCountOf(address owner) external view returns (uint256);
62: 
63:     function getCdpCountOf(
64:         address owner,
65:         bytes32 startNodeId,
66:         uint maxNodes
67:     ) external view returns (uint256, bytes32);
68: 
69:     function getCdpsOf(address owner) external view returns (bytes32[] memory);
70: 
71:     function getAllCdpsOf(
72:         address owner,
73:         bytes32 startNodeId,
74:         uint maxNodes
75:     ) external view returns (bytes32[] memory, uint256, bytes32);
76: 
77:     function cdpOfOwnerByIndex(address owner, uint256 index) external view returns (bytes32);
78: 
79:     function cdpOfOwnerByIdx(
80:         address owner,
81:         uint256 index,
82:         bytes32 startNodeId,
83:         uint maxNodes
84:     ) external view returns (bytes32, bool);
85: }
86: 

//@audit  ,_prevId ,_nextId are not checked
50:     function insert(
51:         address owner,
52:         uint256 _ICR,
53:         bytes32 _prevId,
54:         bytes32 _nextId
55:     ) external returns (bytes32);
56: 
57:     function getOwnerAddress(bytes32 _id) external pure returns (address);
58: 
59:     function nonExistId() external view returns (bytes32);
60: 
61:     function cdpCountOf(address owner) external view returns (uint256);
62: 
63:     function getCdpCountOf(
64:         address owner,
65:         bytes32 startNodeId,
66:         uint maxNodes
67:     ) external view returns (uint256, bytes32);
68: 
69:     function getCdpsOf(address owner) external view returns (bytes32[] memory);
70: 
71:     function getAllCdpsOf(
72:         address owner,
73:         bytes32 startNodeId,
74:         uint maxNodes
75:     ) external view returns (bytes32[] memory, uint256, bytes32);
76: 
77:     function cdpOfOwnerByIndex(address owner, uint256 index) external view returns (bytes32);
78: 
79:     function cdpOfOwnerByIdx(
80:         address owner,
81:         uint256 index,
82:         bytes32 startNodeId,
83:         uint maxNodes
84:     ) external view returns (bytes32, bool);
85: }
86: 

//@audit  ,_id are not checked
57:     function getOwnerAddress(bytes32 _id) external pure returns (address);
58: 
59:     function nonExistId() external view returns (bytes32);
60: 
61:     function cdpCountOf(address owner) external view returns (uint256);
62: 
63:     function getCdpCountOf(
64:         address owner,
65:         bytes32 startNodeId,
66:         uint maxNodes
67:     ) external view returns (uint256, bytes32);
68: 
69:     function getCdpsOf(address owner) external view returns (bytes32[] memory);
70: 
71:     function getAllCdpsOf(
72:         address owner,
73:         bytes32 startNodeId,
74:         uint maxNodes
75:     ) external view returns (bytes32[] memory, uint256, bytes32);
76: 
77:     function cdpOfOwnerByIndex(address owner, uint256 index) external view returns (bytes32);
78: 
79:     function cdpOfOwnerByIdx(
80:         address owner,
81:         uint256 index,
82:         bytes32 startNodeId,
83:         uint maxNodes
84:     ) external view returns (bytes32, bool);
85: }
86: 

//@audit  ,startNodeId are not checked
63:     function getCdpCountOf(
64:         address owner,
65:         bytes32 startNodeId,
66:         uint maxNodes
67:     ) external view returns (uint256, bytes32);
68: 
69:     function getCdpsOf(address owner) external view returns (bytes32[] memory);
70: 
71:     function getAllCdpsOf(
72:         address owner,
73:         bytes32 startNodeId,
74:         uint maxNodes
75:     ) external view returns (bytes32[] memory, uint256, bytes32);
76: 
77:     function cdpOfOwnerByIndex(address owner, uint256 index) external view returns (bytes32);
78: 
79:     function cdpOfOwnerByIdx(
80:         address owner,
81:         uint256 index,
82:         bytes32 startNodeId,
83:         uint maxNodes
84:     ) external view returns (bytes32, bool);
85: }
86: 

//@audit  ,startNodeId are not checked
71:     function getAllCdpsOf(
72:         address owner,
73:         bytes32 startNodeId,
74:         uint maxNodes
75:     ) external view returns (bytes32[] memory, uint256, bytes32);
76: 
77:     function cdpOfOwnerByIndex(address owner, uint256 index) external view returns (bytes32);
78: 
79:     function cdpOfOwnerByIdx(
80:         address owner,
81:         uint256 index,
82:         bytes32 startNodeId,
83:         uint maxNodes
84:     ) external view returns (bytes32, bool);
85: }
86: 

//@audit  ,startNodeId are not checked
79:     function cdpOfOwnerByIdx(
80:         address owner,
81:         uint256 index,
82:         bytes32 startNodeId,
83:         uint maxNodes
84:     ) external view returns (bytes32, bool);
85: }
86: 


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ISortedCdps.sol#L14-L86) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ISortedCdps.sol#L18-L86), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ISortedCdps.sol#L20-L86), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ISortedCdps.sol#L34-L86), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ISortedCdps.sol#L36-L86), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ISortedCdps.sol#L38-L86), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ISortedCdps.sol#L44-L86), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ISortedCdps.sol#L50-L86), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ISortedCdps.sol#L57-L86), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ISortedCdps.sol#L63-L86), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ISortedCdps.sol#L71-L86), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ISortedCdps.sol#L79-L86)


</details>


### [NC&#x2011;20] Events are missing sender information 
When an action is triggered based on a user's action, not being able to filter based on who triggered the action makes event processing a lot more cumbersome. Including the `msg.sender` the events of these types of action will make events much more useful to end users, especially when `msg.sender` is not `tx.origin`.


*There are 39 instances of this issue:*



<details>
<summary>see instances</summary>


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


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L65-L65) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L112-L112), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L113-L113), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L145-L145), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L146-L146), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L173-L173), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L174-L174), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L200-L200), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L213-L213), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L247-L247), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L307-L307), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L360-L360), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L383-L383), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L399-L399)


```solidity

File: packages/contracts/contracts/BorrowerOperations.sol

136:         emit FeeRecipientAddressChanged(_feeRecipientAddress);

1105:         emit FlashLoanSuccess(address(receiver), token, amount, fee);

1149:         emit FeeRecipientAddressChanged(_feeRecipientAddress);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L136-L136) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L1105-L1105), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L1149-L1149)


```solidity

File: packages/contracts/contracts/CdpManager.sol

55:         emit StakingRewardSplitSet(stakingRewardSplit);

782:         emit StakingRewardSplitSet(_stakingRewardSplit);

801:         emit RedemptionFeeFloorSet(_redemptionFeeFloor);

824:         emit MinuteDecayFactorSet(_minuteDecayFactor);

836:         emit BetaSet(_beta);

848:         emit RedemptionsPaused(_paused);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L55-L55) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L782-L782), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L801-L801), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L824-L824), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L836-L836), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L848-L848)


```solidity

File: packages/contracts/contracts/CdpManagerStorage.sol

119:         emit GracePeriodDurationSet(_gracePeriod);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L119-L119) 


```solidity

File: packages/contracts/contracts/CollSurplusPool.sol

83:         emit SurplusCollSharesUpdated(_account, newAmount);

95:         emit SurplusCollSharesUpdated(_account, 0);

104:         emit CollSharesTransferred(_account, claimableColl);

150:         emit SweepTokenSuccess(token, amount, feeRecipientAddress);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L83-L83) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L95-L95), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L104-L104), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L150-L150)


```solidity

File: packages/contracts/contracts/Governor.sol

157:         emit RoleNameSet(role, roleName);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L157-L157) 


```solidity

File: packages/contracts/contracts/PriceFeed.sol

67:         emit FallbackCallerChanged(address(0), _fallbackCallerAddress);

387:             emit FallbackCallerChanged(oldFallbackCaller, _fallbackCaller);

381:                 emit UnhealthyFallbackCaller(_fallbackCaller, block.timestamp);

378:                     emit FallbackCallerChanged(oldFallbackCaller, _fallbackCaller);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L67-L67) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L387-L387), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L381-L381), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L378-L378)


```solidity

File: packages/contracts/contracts/SortedCdps.sol

451:             emit NodeRemoved(_ids[i]);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L451-L451) 


```solidity

File: packages/contracts/contracts/LeverageMacroFactory.sol

56:         emit DeployNewMacro(_owner, addy);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroFactory.sol#L56-L56) 


```solidity

File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

101:         emit PublicCapabilityUpdated(target, functionSig, enabled);

129:         emit RoleCapabilityUpdated(role, target, functionSig, enabled);

140:         emit CapabilityBurned(target, functionSig);

163:         emit UserRoleUpdated(user, role, enabled);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L101-L101) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L129-L129), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L140-L140), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L163-L163)


</details>


### [NC&#x2011;21] Events may be emitted out of order due to reentrancy 
Ensure that events follow the best practice of check-effects-interaction, and are emitted before external calls


*There are 12 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/ActivePool.sol

307:         emit FlashLoanSuccess(address(receiver), token, amount, fee);

360:         emit FeeRecipientClaimableCollSharesDecreased(cachedFeeRecipientCollShares, _shares);

399:         emit FeeRecipientAddressChanged(_feeRecipientAddress);

412:         emit FlashFeeSet(msg.sender, _oldFee, _newFee);

421:         emit FlashLoansPaused(msg.sender, _paused);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L307-L307) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L360-L360), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L399-L399), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L412-L412), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L421-L421)


```solidity

File: packages/contracts/contracts/BorrowerOperations.sol

1105:         emit FlashLoanSuccess(address(receiver), token, amount, fee);

1149:         emit FeeRecipientAddressChanged(_feeRecipientAddress);

1162:         emit FlashFeeSet(msg.sender, _oldFee, _newFee);

1171:         emit FlashLoansPaused(msg.sender, _paused);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L1105-L1105) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L1149-L1149), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L1162-L1162), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L1171-L1171)


```solidity

File: packages/contracts/contracts/CdpManager.sol

220:             emit CdpUpdated(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L220-L220) 


```solidity

File: packages/contracts/contracts/LiquidationLibrary.sol

490:         emit CdpUpdated(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L490-L490) 


```solidity

File: packages/contracts/contracts/CdpManagerStorage.sol

587:         emit CollateralFeePerUnitUpdated(_oldPerUnit, _newPerUnit, _feeTaken);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L587-L587) 


</details>


### [NC&#x2011;22] Explicitly define visibility of state variables to prevent misconceptions on what can access the variable 
Such state variables should be marked as private as this is the default visibility


*There are 6 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

128:     ICollSurplusPool immutable collSurplusPool;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L128-L128) 


```solidity

File: packages/contracts/contracts/Governor.sol

17:     bytes32 NO_ROLES = bytes32(0);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L17-L17) 


```solidity

File: packages/contracts/contracts/SortedCdps.sol

60:     uint256 constant ADDRESS_SHIFT = 96; // 8 * 12; Puts the address at leftmost bytes32 position

61:     uint256 constant BLOCK_SHIFT = 64; // 8 * 8; Puts the block value after the address


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L60-L60) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L61-L61)


```solidity

File: packages/contracts/contracts/LeverageMacroBase.sol

37:     bytes32 constant FLASH_LOAN_SUCCESS = keccak256("ERC3156FlashBorrower.onFlashLoan");


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L37-L37) 


```solidity

File: packages/contracts/contracts/SimplifiedDiamondLike.sol

39:     bytes32 constant DIAMOND_STORAGE_POSITION = keccak256("diamond.standard.diamond.storage");


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L39-L39) 


</details>


### [NC&#x2011;23] Defining All External/Public Functions in Contract Interfaces 
It is preferable to have all the external and public function in an interface to make using them easier by developers. This helps ensure the whole API is extracted in a interface.


*There are 52 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/ActivePool.sol

371:     function sweepToken(address token, uint256 amount) public nonReentrant requiresAuth {
372:         ICdpManagerData(cdpManagerAddress).syncGlobalAccountingAndGracePeriod(); // Accrue State First

404:     function setFeeBps(uint256 _newFee) external requiresAuth {
405:         ICdpManagerData(cdpManagerAddress).syncGlobalAccountingAndGracePeriod(); // Accrue State First

417:     function setFlashLoansPaused(bool _paused) external requiresAuth {
418:         ICdpManagerData(cdpManagerAddress).syncGlobalAccountingAndGracePeriod(); // Accrue State First


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L371-L372) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L404-L405), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L417-L418)


```solidity

File: packages/contracts/contracts/BorrowerOperations.sol

659:     function DOMAIN_SEPARATOR() external view returns (bytes32) {
660:         return domainSeparator();

1154:     function setFeeBps(uint256 _newFee) external requiresAuth {
1155:         require(_newFee <= MAX_FEE_BPS, "ERC3156FlashLender: _newFee should <= MAX_FEE_BPS");

1167:     function setFlashLoansPaused(bool _paused) external requiresAuth {
1168:         cdpManager.syncGlobalAccounting();


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L659-L660) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L1154-L1155), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L1167-L1168)


```solidity

File: packages/contracts/contracts/CdpManager.sol

717:     function getDeploymentStartTime() public view returns (uint256) {
718:         return deploymentStartTime;

727:     function checkPotentialRecoveryMode(
728:         uint256 _systemCollShares,
729:         uint256 _systemDebt,
730:         uint256 _price
731:     ) external view returns (bool) {

773:     function setStakingRewardSplit(uint256 _stakingRewardSplit) external requiresAuth {
774:         require(

788:     function setRedemptionFeeFloor(uint256 _redemptionFeeFloor) external requiresAuth {
789:         require(

807:     function setMinuteDecayFactor(uint256 _minuteDecayFactor) external requiresAuth {
808:         require(

830:     function setBeta(uint256 _beta) external requiresAuth {
831:         syncGlobalAccountingAndGracePeriod();

843:     function setRedemptionsPaused(bool _paused) external requiresAuth {
844:         syncGlobalAccountingAndGracePeriod();


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L717-L718) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L727-L731), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L773-L774), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L788-L789), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L807-L808), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L830-L831), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L843-L844)


```solidity

File: packages/contracts/contracts/CdpManagerStorage.sol

111:     function setGracePeriod(uint128 _gracePeriod) external requiresAuth {
112:         require(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L111-L112) 


```solidity

File: packages/contracts/contracts/CollSurplusPool.sol

142:     function sweepToken(address token, uint256 amount) public nonReentrant requiresAuth {
143:         require(token != address(collateral), "CollSurplusPool: Cannot Sweep Collateral");


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L142-L143) 


```solidity

File: packages/contracts/contracts/EBTCToken.sol

176:     function DOMAIN_SEPARATOR() external view returns (bytes32) {
177:         return domainSeparator();


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L176-L177) 


```solidity

File: packages/contracts/contracts/Governor.sol

43:     function getUsersByRole(uint8 role) external view returns (address[] memory usersWithRole) {
44:         // Search over all users: O(n) * 2

73:     function getRolesForUser(address user) external view returns (uint8[] memory rolesForUser) {
74:         // Enumerate over all possible roles and check if enabled

96:     function getRolesFromByteMap(bytes32 byteMap) public pure returns (uint8[] memory roleIds) {
97:         uint256 count;

120:     function getByteMapFromRoles(uint8[] memory roleIds) public pure returns (bytes32) {
121:         bytes32 _data;

131:     function getEnabledFunctionsInTarget(
132:         address _target
133:     ) public view returns (bytes4[] memory _funcs) {

146:     function getRoleName(uint8 role) external view returns (string memory roleName) {
147:         return roleNames[role];

154:     function setRoleName(uint8 role, string memory roleName) external requiresAuth {
155:         roleNames[role] = roleName;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L43-L44) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L73-L74), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L96-L97), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L120-L121), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L131-L133), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L146-L147), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L154-L155)


```solidity

File: packages/contracts/contracts/PriceFeed.sol

358:     function setFallbackCaller(address _fallbackCaller) external requiresAuth {
359:         // health check-up before officially set it up


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L358-L359) 


```solidity

File: packages/contracts/contracts/SortedCdps.sol

105:     function toCdpId(
106:         address owner,
107:         uint256 blockHeight,
108:         uint256 nonce
109:     ) public pure returns (bytes32) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L105-L109) 


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

164:     function getApproxHint(
165:         uint256 _CR,
166:         uint256 _numTrials,
167:         uint256 _inputRandomSeed
168:     ) external view returns (bytes32 hint, uint256 diff, uint256 latestRandomSeed) {

203:     function computeNominalCR(uint256 _coll, uint256 _debt) external pure returns (uint256) {
204:         return EbtcMath._computeNominalCR(_coll, _debt);

212:     function computeCR(
213:         uint256 _coll,
214:         uint256 _debt,
215:         uint256 _price
216:     ) external pure returns (uint256) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L48-L61) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L164-L168), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L203-L204), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L212-L216)


```solidity

File: packages/contracts/contracts/LeverageMacroBase.sol

118:     function doOperation(
119:         FlashLoanType flType,
120:         uint256 borrowAmount,
121:         LeverageMacroOperation calldata operation,
122:         PostOperationCheck postCheckType,
123:         PostCheckParams calldata checkParams
124:     ) external {

214:     function sweepToCaller() public {
215:         _assertOwner();

234:     function sweepToken(address token, uint256 amount) public {
235:         _assertOwner();

338:     function decodeFLData(bytes calldata data) public view returns (LeverageMacroOperation memory) {
339:         LeverageMacroOperation memory leverageMacroData = abi.decode(data, (LeverageMacroOperation));


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L118-L124) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L214-L215), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L234-L235), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L338-L339)


```solidity

File: packages/contracts/contracts/LeverageMacroFactory.sol

38:     function deployNewMacro() external returns (address) {
39:         return deployNewMacro(msg.sender);

43:     function deployNewMacro(address _owner) public returns (address) {
44:         address addy = address(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroFactory.sol#L38-L39) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroFactory.sol#L43-L44)


```solidity

File: packages/contracts/contracts/LeverageMacroReference.sol

50:     function resetApprovals() external {
51:         _assertOwner();


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroReference.sol#L50-L51) 


```solidity

File: packages/contracts/contracts/SimplifiedDiamondLike.sol

51:     function setFallbackHandler(bytes4 sig, address handler) external {
52:         require(msg.sender == owner);

66:     function setAllowAnyCall(bool allowNonCallbacks) external {
67:         require(msg.sender == owner);

76:     function enableCallbackForCall() external {
77:         require(msg.sender == address(this)); // Must call this via `execute` to explicitly set the flag

110:     function execute(Operation[] calldata ops) external payable {
111:         require(msg.sender == owner, "Must be owner");


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L51-L52) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L66-L67), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L76-L77), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L110-L111)


```solidity

File: packages/contracts/contracts/Dependencies/Auth.sol

42:     function setAuthority(Authority newAuthority) public virtual {
43:         // We check if the caller is the owner first because we want to ensure they can

52:     function transferOwnership(address newOwner) public virtual requiresAuth {
53:         owner = newOwner;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/Auth.sol#L42-L43) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/Auth.sol#L52-L53)


```solidity

File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

22:     function authority() public view returns (Authority) {
23:         return _authority;

26:     function authorityInitialized() public view returns (bool) {
27:         return _authorityInitialized;

38:     function setAuthority(address newAuthority) public virtual {
39:         // We check if the caller is the owner first because we want to ensure they can


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L22-L23) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L26-L27), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L38-L39)


```solidity

File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

38:     function doesUserHaveRole(address user, uint8 role) public view virtual returns (bool) {
39:         return (uint256(getUserRoles[user]) >> role) & 1 != 0;

42:     function doesRoleHaveCapability(
43:         uint8 role,
44:         address target,
45:         bytes4 functionSig
46:     ) public view virtual returns (bool) {

50:     function isPublicCapability(address target, bytes4 functionSig) public view returns (bool) {
51:         return capabilityFlag[target][functionSig] == CapabilityFlag.Public;

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
134:         require(

147:     function setUserRole(address user, uint8 role, bool enabled) public virtual requiresAuth {
148:         if (enabled) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L38-L39) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L42-L46), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L50-L51), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L85-L89), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L106-L111), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L133-L134), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L147-L148)


</details>


### [NC&#x2011;24] NatSpec documentation for `function` is missing 
It is recommended that Solidity contracts are fully annotated using NatSpec for all public interfaces (everything in the ABI). It is clearly stated in the Solidity official documentation. In complex projects such as Defi, the interpretation of all functions and their arguments and returns is important for code readability and auditability.[source](https://docs.soliditylang.org/en/v0.8.15/natspec-format.html)


*There are 264 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

107:     constructor(

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

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L107-L107) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L328-L328), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L439-L439), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L615-L615), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L635-L635), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L673-L673), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L677-L677), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L744-L744), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L796-L796), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L803-L803), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L813-L813), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L824-L824), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L829-L829), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L834-L834), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L838-L838), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L845-L845), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L852-L852), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L910-L910), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L917-L917), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L921-L921), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L928-L928), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L935-L935), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L939-L939), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L946-L946), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L953-L953), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L963-L963), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L986-L986), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L1004-L1004), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L1030-L1030), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L1049-L1049)


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

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L244-L244) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L489-L489), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L550-L550), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L595-L595), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L612-L612), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L647-L647), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L655-L655), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L667-L667), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L676-L676), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L689-L689), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L702-L702), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L709-L709), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L737-L737), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L753-L753), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L757-L757), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L761-L761)


```solidity

File: packages/contracts/contracts/LiquidationLibrary.sol

14:     constructor(

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

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L14-L14) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L61-L61), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L135-L135), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L186-L186), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L223-L223), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L295-L295), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L384-L384), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L397-L397), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L450-L450), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L466-L466), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L503-L503), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L544-L544), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L570-L570), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L608-L608), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L642-L642), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L733-L733), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L807-L807), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L839-L839), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L862-L862), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L896-L896), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L908-L908)


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

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L73-L73) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L255-L255), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L260-L260), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L293-L293), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L327-L327), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L410-L410), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L419-L419), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L431-L431), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L441-L441), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L463-L463), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L489-L489), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L509-L509), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L539-L539), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L574-L574), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L592-L592), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L648-L648), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L652-L652), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L659-L659), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L707-L707), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L733-L733)


```solidity

File: packages/contracts/contracts/CollSurplusPool.sol

112:     function _requireCallerIsBorrowerOperations() internal view {

119:     function _requireCallerIsCdpManager() internal view {

123:     function _requireCallerIsActivePool() internal view {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L112-L112) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L119-L119), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L123-L123)


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

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L111-L111) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L115-L115), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L119-L119), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L125-L125), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L129-L129), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L134-L134), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L152-L152), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L160-L160), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L231-L231), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L235-L235), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L246-L246), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L262-L262), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L270-L270), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L285-L285), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L295-L295), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L306-L306), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L323-L323)


```solidity

File: packages/contracts/contracts/PriceFeed.sol

465:     function _fallbackIsBroken(FallbackResponse memory _response) internal view returns (bool) {

493:     function _responseTimeout(uint256 _timestamp, uint256 _timeout) internal view returns (bool) {

788:     function _formatClAggregateAnswer(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L465-L465) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L493-L493), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L788-L788)


```solidity

File: packages/contracts/contracts/SortedCdps.sol

363:     function _insert(bytes32 _id, uint256 _NICR, bytes32 _prevId, bytes32 _nextId) internal {

456:     function _remove(bytes32 _id) internal {

591:     function _validInsertPosition(

674:     function _findInsertPosition(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L363-L363) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L456-L456), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L591-L591), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L674-L674)


```solidity

File: packages/contracts/contracts/HintHelpers.sol

27:     constructor(

164:     function getApproxHint(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L27-L27) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L164-L164)


```solidity

File: packages/contracts/contracts/LeverageMacroBase.sol

15:     function Cdps(bytes32) external view returns (ICdpManagerData.Cdp memory);

39:     function owner() public virtual returns (address) {

43:     function _assertOwner() internal {

51:     constructor(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L15-L15) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L39-L39), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L43-L43), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L51-L51)


```solidity

File: packages/contracts/contracts/LeverageMacroDelegateTarget.sol

7:     function owner() external view returns (address);

41:     constructor(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L7-L7) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L41-L41)


```solidity

File: packages/contracts/contracts/LeverageMacroFactory.sol

21:     constructor(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroFactory.sol#L21-L21) 


```solidity

File: packages/contracts/contracts/LeverageMacroReference.sol

17:     constructor(

44:     function owner() public override returns (address) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroReference.sol#L17-L17) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroReference.sol#L44-L44)


```solidity

File: packages/contracts/contracts/SimplifiedDiamondLike.sol

44:     constructor(address _owner) {

164:     fallback() external payable {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L44-L44) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L164-L164)


```solidity

File: packages/contracts/contracts/Dependencies/Auth.sol

18:     constructor(address _owner, Authority _authority) {

32:     function isAuthorized(address user, bytes4 functionSig) internal view virtual returns (bool) {

42:     function setAuthority(Authority newAuthority) public virtual {

52:     function transferOwnership(address newOwner) public virtual requiresAuth {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/Auth.sol#L18-L18) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/Auth.sol#L32-L32), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/Auth.sol#L42-L42), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/Auth.sol#L52-L52)


```solidity

File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

22:     function authority() public view returns (Authority) {

26:     function authorityInitialized() public view returns (bool) {

30:     function isAuthorized(address user, bytes4 functionSig) internal view virtual returns (bool) {

38:     function setAuthority(address newAuthority) public virtual {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L22-L22) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L26-L26), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L30-L30), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L38-L38)


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

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L60-L60) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L79-L79), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L83-L83), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L95-L95), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L99-L99), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L103-L103), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L115-L115)


```solidity

File: packages/contracts/contracts/Dependencies/EbtcMath.sol

20:     function _min(uint256 _a, uint256 _b) internal pure returns (uint256) {

24:     function _max(uint256 _a, uint256 _b) internal pure returns (uint256) {

35:     function decMul(uint256 x, uint256 y) internal pure returns (uint256 decProd) {

59:     function _decPow(uint256 _base, uint256 _minutes) internal pure returns (uint256) {

88:     function _getAbsoluteDifference(uint256 _a, uint256 _b) internal pure returns (uint256) {

92:     function _computeNominalCR(uint256 _collShares, uint256 _debt) internal pure returns (uint256) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcMath.sol#L20-L20) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcMath.sol#L24-L24), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcMath.sol#L35-L35), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcMath.sol#L59-L59), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcMath.sol#L88-L88), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcMath.sol#L92-L92)


```solidity

File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

20:     constructor(address _owner, Authority _authority) Auth(_owner, _authority) {}

38:     function doesUserHaveRole(address user, uint8 role) public view virtual returns (bool) {

42:     function doesRoleHaveCapability(

50:     function isPublicCapability(address target, bytes4 functionSig) public view returns (bool) {

147:     function setUserRole(address user, uint8 role, bool enabled) public virtual requiresAuth {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L20-L20) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L38-L38), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L42-L42), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L50-L50), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L147-L147)


```solidity

File: packages/contracts/contracts/Interfaces/IActivePool.sol

23:     function transferSystemCollShares(address _account, uint256 _amount) external;

25:     function increaseSystemCollShares(uint256 _value) external;

27:     function transferSystemCollSharesAndLiquidatorReward(

33:     function allocateSystemCollSharesToFeeRecipient(uint256 _shares) external;

35:     function claimFeeRecipientCollShares(uint256 _shares) external;

37:     function feeRecipientAddress() external view returns (address);

39:     function getFeeRecipientClaimableCollShares() external view returns (uint256);

41:     function setFeeRecipientAddress(address _feeRecipientAddress) external;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IActivePool.sol#L23-L23) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IActivePool.sol#L25-L25), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IActivePool.sol#L27-L27), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IActivePool.sol#L33-L33), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IActivePool.sol#L35-L35), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IActivePool.sol#L37-L37), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IActivePool.sol#L39-L39), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IActivePool.sol#L41-L41)


```solidity

File: packages/contracts/contracts/Interfaces/IBorrowerOperations.sol

20:     function openCdp(

27:     function openCdpFor(

35:     function addColl(

42:     function withdrawColl(

49:     function withdrawDebt(

56:     function repayDebt(

63:     function closeCdp(bytes32 _cdpId) external;

65:     function adjustCdp(

74:     function adjustCdpWithColl(

84:     function claimSurplusCollShares() external;

86:     function feeRecipientAddress() external view returns (address);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L20-L20) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L27-L27), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L35-L35), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L42-L42), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L49-L49), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L56-L56), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L63-L63), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L65-L65), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L74-L74), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L84-L84), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L86-L86)


```solidity

File: packages/contracts/contracts/Interfaces/ICdpManager.sol

11:     function getActiveCdpsCount() external view returns (uint256);

13:     function getIdFromCdpIdsArray(uint256 _index) external view returns (bytes32);

15:     function liquidate(bytes32 _cdpId) external;

17:     function partiallyLiquidate(

24:     function batchLiquidateCdps(bytes32[] calldata _cdpArray) external;

26:     function redeemCollateral(

36:     function updateStakeAndTotalStakes(bytes32 _cdpId) external returns (uint256);

38:     function syncAccounting(bytes32 _cdpId) external;

40:     function closeCdp(bytes32 _cdpId, address _borrower, uint256 _debt, uint256 _coll) external;

42:     function getRedemptionRate() external view returns (uint256);

44:     function getRedemptionRateWithDecay() external view returns (uint256);

46:     function getRedemptionFeeWithDecay(uint256 _stETHToRedeem) external view returns (uint256);

48:     function getCdpStatus(bytes32 _cdpId) external view returns (uint256);

50:     function getCdpStake(bytes32 _cdpId) external view returns (uint256);

52:     function getCdpDebt(bytes32 _cdpId) external view returns (uint256);

54:     function getCdpCollShares(bytes32 _cdpId) external view returns (uint256);

56:     function getCdpLiquidatorRewardShares(bytes32 _cdpId) external view returns (uint);

58:     function initializeCdp(

66:     function updateCdp(

75:     function getCachedTCR(uint256 _price) external view returns (uint256);

77:     function checkRecoveryMode(uint256 _price) external view returns (bool);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManager.sol#L11-L11) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManager.sol#L13-L13), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManager.sol#L15-L15), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManager.sol#L17-L17), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManager.sol#L24-L24), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManager.sol#L26-L26), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManager.sol#L36-L36), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManager.sol#L38-L38), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManager.sol#L40-L40), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManager.sol#L42-L42), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManager.sol#L44-L44), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManager.sol#L46-L46), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManager.sol#L48-L48), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManager.sol#L50-L50), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManager.sol#L52-L52), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManager.sol#L54-L54), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManager.sol#L56-L56), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManager.sol#L58-L58), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManager.sol#L66-L66), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManager.sol#L75-L75), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManager.sol#L77-L77)


```solidity

File: packages/contracts/contracts/Interfaces/ICdpManagerData.sol

217:     function totalStakes() external view returns (uint256);

219:     function ebtcToken() external view returns (IEBTCToken);

221:     function systemStEthFeePerUnitIndex() external view returns (uint256);

223:     function systemStEthFeePerUnitIndexError() external view returns (uint256);

225:     function stEthIndex() external view returns (uint256);

227:     function calcFeeUponStakingReward(

232:     function syncGlobalAccounting() external; // Accrues StEthFeeSplit without influencing Grace Period

234:     function syncGlobalAccountingAndGracePeriod() external; // Accrues StEthFeeSplit and influences Grace Period

236:     function getAccumulatedFeeSplitApplied(

241:     function getCachedNominalICR(bytes32 _cdpId) external view returns (uint256);

243:     function getCachedICR(bytes32 _cdpId, uint256 _price) external view returns (uint256);

245:     function getSyncedCdpDebt(bytes32 _cdpId) external view returns (uint256);

247:     function getSyncedCdpCollShares(bytes32 _cdpId) external view returns (uint256);

249:     function getSyncedICR(bytes32 _cdpId, uint256 _price) external view returns (uint256);

251:     function getSyncedTCR(uint256 _price) external view returns (uint256);

253:     function getSyncedNominalICR(bytes32 _cdpId) external view returns (uint256);

255:     function getPendingRedistributedDebt(bytes32 _cdpId) external view returns (uint256);

257:     function hasPendingRedistributedDebt(bytes32 _cdpId) external view returns (bool);

259:     function getSyncedDebtAndCollShares(

263:     function canLiquidateRecoveryMode(uint256 icr, uint256 tcr) external view returns (bool);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L217-L217) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L219-L219), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L221-L221), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L223-L223), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L225-L225), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L227-L227), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L232-L232), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L234-L234), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L236-L236), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L241-L241), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L243-L243), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L245-L245), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L247-L247), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L249-L249), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L251-L251), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L253-L253), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L255-L255), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L257-L257), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L259-L259), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L263-L263)


```solidity

File: packages/contracts/contracts/Interfaces/ICollSurplusPool.sol

15:     function getTotalSurplusCollShares() external view returns (uint256);

17:     function getSurplusCollShares(address _account) external view returns (uint256);

19:     function increaseSurplusCollShares(address _account, uint256 _amount) external;

21:     function claimSurplusCollShares(address _account) external;

23:     function increaseTotalSurplusCollShares(uint256 _value) external;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICollSurplusPool.sol#L15-L15) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICollSurplusPool.sol#L17-L17), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICollSurplusPool.sol#L19-L19), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICollSurplusPool.sol#L21-L21), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICollSurplusPool.sol#L23-L23)


```solidity

File: packages/contracts/contracts/Interfaces/IEbtcBase.sol

8:     function priceFeed() external view returns (IPriceFeed);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IEbtcBase.sol#L8-L8) 


```solidity

File: packages/contracts/contracts/Interfaces/IEBTCToken.sol

11:     function mint(address _account, uint256 _amount) external;

13:     function burn(address _account, uint256 _amount) external;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IEBTCToken.sol#L11-L11) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IEBTCToken.sol#L13-L13)


```solidity

File: packages/contracts/contracts/Interfaces/IFallbackCaller.sol

13:     function getFallbackResponse() external view returns (uint256, uint256, bool);

17:     function fallbackTimeout() external view returns (uint256);

21:     function setFallbackTimeout(uint256 newFallbackTimeout) external;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IFallbackCaller.sol#L13-L13) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IFallbackCaller.sol#L17-L17), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IFallbackCaller.sol#L21-L21)


```solidity

File: packages/contracts/contracts/Interfaces/IPermitNonce.sol

7:     function increasePermitNonce() external returns (uint256);

9:     function nonces(address owner) external view returns (uint256);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPermitNonce.sol#L7-L7) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPermitNonce.sol#L9-L9)


```solidity

File: packages/contracts/contracts/Interfaces/IPool.sol

15:     function getSystemCollShares() external view returns (uint256);

17:     function getSystemDebt() external view returns (uint256);

19:     function increaseSystemDebt(uint256 _amount) external;

21:     function decreaseSystemDebt(uint256 _amount) external;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPool.sol#L15-L15) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPool.sol#L17-L17), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPool.sol#L19-L19), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPool.sol#L21-L21)


```solidity

File: packages/contracts/contracts/Interfaces/IPositionManagers.sol

18:     function getPositionManagerApproval(

23:     function setPositionManagerApproval(

28:     function revokePositionManagerApproval(address _positionManager) external;

30:     function renouncePositionManagerApproval(address _borrower) external;

32:     function permitPositionManagerApproval(

42:     function version() external view returns (string memory);

44:     function permitTypeHash() external view returns (bytes32);

46:     function domainSeparator() external view returns (bytes32);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPositionManagers.sol#L18-L18) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPositionManagers.sol#L23-L23), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPositionManagers.sol#L28-L28), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPositionManagers.sol#L30-L30), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPositionManagers.sol#L32-L32), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPositionManagers.sol#L42-L42), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPositionManagers.sol#L44-L44), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPositionManagers.sol#L46-L46)


```solidity

File: packages/contracts/contracts/Interfaces/IPriceFeed.sol

43:     function fetchPrice() external returns (uint256);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPriceFeed.sol#L43-L43) 


```solidity

File: packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol

13:     function notifyStartGracePeriod(uint256 tcr) external;

15:     function notifyEndGracePeriod(uint256 tcr) external;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol#L13-L13) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol#L15-L15)


```solidity

File: packages/contracts/contracts/Interfaces/ISortedCdps.sol

14:     function remove(bytes32 _id) external;

16:     function batchRemove(bytes32[] memory _ids) external;

18:     function reInsert(bytes32 _id, uint256 _newICR, bytes32 _prevId, bytes32 _nextId) external;

20:     function contains(bytes32 _id) external view returns (bool);

22:     function isFull() external view returns (bool);

24:     function isEmpty() external view returns (bool);

26:     function getSize() external view returns (uint256);

28:     function getMaxSize() external view returns (uint256);

30:     function getFirst() external view returns (bytes32);

32:     function getLast() external view returns (bytes32);

34:     function getNext(bytes32 _id) external view returns (bytes32);

36:     function getPrev(bytes32 _id) external view returns (bytes32);

38:     function validInsertPosition(

44:     function findInsertPosition(

50:     function insert(

57:     function getOwnerAddress(bytes32 _id) external pure returns (address);

59:     function nonExistId() external view returns (bytes32);

61:     function cdpCountOf(address owner) external view returns (uint256);

63:     function getCdpCountOf(

69:     function getCdpsOf(address owner) external view returns (bytes32[] memory);

71:     function getAllCdpsOf(

77:     function cdpOfOwnerByIndex(address owner, uint256 index) external view returns (bytes32);

79:     function cdpOfOwnerByIdx(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ISortedCdps.sol#L14-L14) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ISortedCdps.sol#L16-L16), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ISortedCdps.sol#L18-L18), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ISortedCdps.sol#L20-L20), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ISortedCdps.sol#L22-L22), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ISortedCdps.sol#L24-L24), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ISortedCdps.sol#L26-L26), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ISortedCdps.sol#L28-L28), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ISortedCdps.sol#L30-L30), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ISortedCdps.sol#L32-L32), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ISortedCdps.sol#L34-L34), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ISortedCdps.sol#L36-L36), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ISortedCdps.sol#L38-L38), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ISortedCdps.sol#L44-L44), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ISortedCdps.sol#L50-L50), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ISortedCdps.sol#L57-L57), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ISortedCdps.sol#L59-L59), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ISortedCdps.sol#L61-L61), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ISortedCdps.sol#L63-L63), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ISortedCdps.sol#L69-L69), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ISortedCdps.sol#L71-L71), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ISortedCdps.sol#L77-L77), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ISortedCdps.sol#L79-L79)


</details>


### [NC&#x2011;25] Function ordering does not follow the Solidity style guide 
According to the [Solidity style guide](https://docs.soliditylang.org/en/v0.8.17/style-guide.html#order-of-functions), functions should be laid out in the following order :`constructor()`, `receive()`, `fallback()`, `external`, `public`, `internal`, `private`, but the cases below do not follow this pattern


*There are 16 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/ActivePool.sol

129:     function transferSystemCollSharesAndLiquidatorReward(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L129-L129) 


```solidity

File: packages/contracts/contracts/BorrowerOperations.sol

553:     function closeCdp(bytes32 _cdpId) external override {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L553-L553) 


```solidity

File: packages/contracts/contracts/CdpManager.sol

320:     function redeemCollateral(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L320-L320) 


```solidity

File: packages/contracts/contracts/LiquidationLibrary.sol

450:     function _partiallyReduceCdpDebt(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L450-L450) 


```solidity

File: packages/contracts/contracts/CdpManagerStorage.sol

111:     function setGracePeriod(uint128 _gracePeriod) external requiresAuth {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L111-L111) 


```solidity

File: packages/contracts/contracts/CollSurplusPool.sol

130:     function increaseTotalSurplusCollShares(uint256 _value) external override {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L130-L130) 


```solidity

File: packages/contracts/contracts/EBTCToken.sol

199:     function permit(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L199-L199) 


```solidity

File: packages/contracts/contracts/Governor.sol

146:     function getRoleName(uint8 role) external view returns (string memory roleName) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L146-L146) 


```solidity

File: packages/contracts/contracts/SortedCdps.sol

140:     function cdpOfOwnerByIndex(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L140-L140) 


```solidity

File: packages/contracts/contracts/HintHelpers.sol

164:     function getApproxHint(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L164-L164) 


```solidity

File: packages/contracts/contracts/LeverageMacroBase.sol

51:     constructor(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L51-L51) 


```solidity

File: packages/contracts/contracts/LeverageMacroReference.sol

50:     function resetApprovals() external {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroReference.sol#L50-L50) 


```solidity

File: packages/contracts/contracts/SimplifiedDiamondLike.sol

110:     function execute(Operation[] calldata ops) external payable {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L110-L110) 


```solidity

File: packages/contracts/contracts/Dependencies/Auth.sol

42:     function setAuthority(Authority newAuthority) public virtual {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/Auth.sol#L42-L42) 


```solidity

File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

38:     function setAuthority(address newAuthority) public virtual {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L38-L38) 


```solidity

File: packages/contracts/contracts/Dependencies/EbtcBase.sol

67:     function getSystemCollShares() public view returns (uint256 entireSystemColl) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L67-L67) 


</details>


### [NC&#x2011;26] Array indicies should be referenced via `enum`s rather than via numeric literals 
Consider using an enum instead of hardcoding an index access to make the code easier to understand.


*There are 2 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/CdpManager.sol

//@audit `_toRemoveIds`
502:         require(_toRemoveIds[0] == _start, "CdpManager: batchRemoveSortedCdpIds check start error");


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L502-L502) 


```solidity

File: packages/contracts/contracts/SortedCdps.sol

//@audit `_ids`
424:         bytes32 _firstPrev = data.nodes[_ids[0]].prevId;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L424-L424) 


</details>


### [NC&#x2011;27] Hardcoded string that is repeatedly used can be replaced with a constant 
For better maintainability, please consider creating and using a constant for those strings instead of hardcoding 


*There are 5 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/ActivePool.sol

//@audit `ActivePool: Insufficient collateral shares` is used multiple time consider using a constant for it.
137:         require(cachedSystemCollShares >= _shares, "ActivePool: Insufficient collateral shares");


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L137-L137) 


```solidity

File: packages/contracts/contracts/CdpManager.sol

//@audit `CDPManager: new minute decay factor out of range` is used multiple time consider using a constant for it.
810:             "CDPManager: new minute decay factor out of range"


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L810-L810) 


```solidity

File: packages/contracts/contracts/SortedCdps.sol

//@audit `SortedCdps: NICR must be positive` is used multiple time consider using a constant for it.
371:         require(_NICR > 0, "SortedCdps: NICR must be positive");

//@audit `SortedCdps: List does not contain the id` is used multiple time consider using a constant for it.
458:         require(contains(_id), "SortedCdps: List does not contain the id");


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L371-L371) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L458-L458)


```solidity

File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

//@audit `RolesAuthority: Capability Burned` is used multiple time consider using a constant for it.
92:             "RolesAuthority: Capability Burned"


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L92-L92) 


</details>


### [NC&#x2011;28] Duplicated `require()` checks should be refactored to a modifier or function 
The compiler will inline the function, which will avoid `JUMP` instructions usually associated with functions


*There are 4 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/ActivePool.sol

137:         require(cachedSystemCollShares >= _shares, "ActivePool: Insufficient collateral shares");

407:         require(_newFee <= MAX_FEE_BPS, "ERC3156FlashLender: _newFee should <= MAX_FEE_BPS");


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L137-L137) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L407-L407)


```solidity

File: packages/contracts/contracts/SortedCdps.sol

458:         require(contains(_id), "SortedCdps: List does not contain the id");


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L458-L458) 


```solidity

File: packages/contracts/contracts/SimplifiedDiamondLike.sol

52:         require(msg.sender == owner);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L52-L52) 


</details>


### [NC&#x2011;29] Some if-statement can be converted to a ternary 
Improving code readability and compactness is an integral part of optimal programming practices. The use of ternary operators in place of if-else conditions is one such measure. Ternary operators allow us to write conditional statements in a more concise manner, thereby enhancing readability and simplicity. They follow the syntax `condition ? exprIfTrue : exprIfFalse`, which interprets as "if the condition is true, evaluate to `exprIfTrue`, else evaluate to `exprIfFalse`". By adopting this approach, we make our code more streamlined and intuitive, which could potentially aid in better understanding and maintenance of the codebase.


*There are 24 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/CdpManager.sol

377:         if (_maxIterations == 0) {
378:             _maxIterations = type(uint256).max;
379:         }


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L377-L379) 


```solidity

File: packages/contracts/contracts/LiquidationLibrary.sol

553:         if (_ICR > LICR) {
554:             // Cap at 10%
555:             _incentiveColl = (_totalDebtToBurn * (_ICR > MCR ? MCR : _ICR)) / _price;
556:         } else {

698:         if (vars.recoveryModeAtStart) {
699:             totals = _getTotalFromBatchLiquidate_RecoveryMode(
700:                 vars.price,
701:                 systemColl,
702:                 systemDebt,
703:                 _cdpArray
704:             );
705:         } else {

266:             if (_debtToRedistribute > 0) {
267:                 _totalDebtToBurn = _totalDebtToBurn - _debtToRedistribute;
268:             }

342:             if (_debtToRedistribute > 0) {
343:                 _totalDebtToBurn = _totalDebtToBurn - _debtToRedistribute;
344:             }

157:             if (
158:                 liquidationValues.totalCollToSendToLiquidator == 0 &&
159:                 liquidationValues.debtToBurn == 0
160:             ) {
161:                 // retry with fully liquidation
162:                 (
163:                     liquidationValues.debtToBurn,
164:                     liquidationValues.totalCollToSendToLiquidator,
165:                     liquidationValues.debtToRedistribute,
166:                     liquidationValues.liquidatorCollSharesReward,
167:                     liquidationValues.collSurplus
168:                 ) = _liquidateCdpInGivenMode(_liqState, _recoveryState);
169:             }


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L553-L556) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L698-L705), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L266-L268), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L342-L344), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L157-L169)


```solidity

File: packages/contracts/contracts/CdpManagerStorage.sol

404:         if (_oldPerUnitCdp != _systemStEthFeePerUnitIndex) {
405:             cdpStEthFeePerUnitIndex[_cdpId] = _systemStEthFeePerUnitIndex;
406:         }

829:         if (pendingDebtRedistributed > 0) {
830:             _newDebt = _newDebt + pendingDebtRedistributed;
831:         }

879:         if (_feeTaken > 0) {
880:             _systemCollShare = _systemCollShare - _feeTaken;
881:         }


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L404-L406) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L829-L831), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L879-L881)


```solidity

File: packages/contracts/contracts/Governor.sol

49:             if (_canCall) {
50:                 count += 1;
51:             }

77:             if (doesUserHaveRole(user, i)) {
78:                 count += 1;
79:             }

100:             if (roleEnabled) {
101:                 count += 1;
102:             }


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L49-L51) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L77-L79), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L100-L102)


```solidity

File: packages/contracts/contracts/SortedCdps.sol

89:         if (_size == 0) {
90:             _size = type(uint256).max;
91:         }

376:         if (!_validInsertPosition(_NICR, prevId, nextId)) {
377:             // Sender's hint was not a valid insert position
378:             // Use sender's hint to find a valid insert position
379:             (prevId, nextId) = _findInsertPosition(_NICR, prevId, nextId);
380:         }

437:         if (_firstPrev != dummyId) {
438:             data.nodes[_firstPrev].nextId = _lastNext;
439:         } else {

442:         if (_lastNext != dummyId) {
443:             data.nodes[_lastNext].prevId = _firstPrev;
444:         } else {

250:             if (getOwnerAddress(_currentCdpId) == owner) {
251:                 _ownedCount = _ownedCount + 1;
252:             }

683:             if (!contains(prevId) || _NICR > cdpManager.getCachedNominalICR(prevId)) {
684:                 // `prevId` does not exist anymore or now has a smaller NICR than the given NICR
685:                 prevId = dummyId;
686:             }

690:             if (!contains(nextId) || _NICR < cdpManager.getCachedNominalICR(nextId)) {
691:                 // `nextId` does not exist anymore or now has a larger NICR than the given NICR
692:                 nextId = dummyId;
693:             }


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L89-L91) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L376-L380), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L437-L439), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L442-L444), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L250-L252), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L683-L686), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L690-L693)


```solidity

File: packages/contracts/contracts/HintHelpers.sol

78:         if (_maxIterations == 0) {
79:             _maxIterations = type(uint256).max;
80:         }


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L78-L80) 


```solidity

File: packages/contracts/contracts/LeverageMacroBase.sol

140:         if (postCheckType == PostOperationCheck.openCdp) {
141:             // How to get owner
142:             // sortedCdps.existCdpOwners(_cdpId);
143:             initialCdpIndex = sortedCdps.cdpCountOf(address(this));
144:         }


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L140-L144) 


```solidity

File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

46:         if (!_authorityInitialized) {
47:             _authorityInitialized = true;
48:         }


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L46-L48) 


```solidity

File: packages/contracts/contracts/Dependencies/EbtcMath.sol

60:         if (_minutes > 525600000) {
61:             _minutes = 525600000;
62:         } // cap to avoid overflow


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcMath.sol#L60-L62) 


```solidity

File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

95:         if (enabled) {
96:             capabilityFlag[target][functionSig] = CapabilityFlag.Public;
97:         } else {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L95-L97) 


</details>


### [NC&#x2011;30] Imports could be organized more systematically 
The contract used interfaces should be imported first, followed by all other files. The examples below do not follow this layout.


*There are 4 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

11: import "./Dependencies/ICollateralTokenOracle.sol";


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L11-L11) 


```solidity

File: packages/contracts/contracts/CollSurplusPool.sol

10: import "./Interfaces/IActivePool.sol";


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L10-L10) 


```solidity

File: packages/contracts/contracts/LeverageMacroFactory.sol

5: import "./Dependencies/ICollateralToken.sol";


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroFactory.sol#L5-L5) 


```solidity

File: packages/contracts/contracts/Dependencies/EbtcBase.sol

7: import "../Interfaces/IActivePool.sol";


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L7-L7) 


</details>


### [NC&#x2011;31] Import declarations should import specific identifiers, rather than the whole file 
Using import declarations of the form `import {<identifier_name>} from "some/ file.sol"` avoids polluting the symbol namespace making flattened files smaller, and speeds up compilation


*There are 96 instances of this issue:*



<details>
<summary>see instances</summary>


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

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L5-L5) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L6-L6), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L7-L7), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L8-L8), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L9-L9), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L10-L10), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L11-L11), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L12-L12), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L13-L13)


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

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L5-L5) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L6-L6), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L7-L7), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L8-L8), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L9-L9), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L10-L10), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L11-L11), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L12-L12), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L13-L13), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L14-L14), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L15-L15), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L16-L16)


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

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L5-L5) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L6-L6), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L7-L7), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L8-L8), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L9-L9), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L10-L10), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L11-L11)


```solidity

File: packages/contracts/contracts/LiquidationLibrary.sol

4: import "./Interfaces/ICdpManagerData.sol";

5: import "./Interfaces/ICollSurplusPool.sol";

6: import "./Interfaces/IEBTCToken.sol";

7: import "./Interfaces/ISortedCdps.sol";

8: import "./Dependencies/ICollateralTokenOracle.sol";

9: import "./CdpManagerStorage.sol";


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L4-L4) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L5-L5), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L6-L6), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L7-L7), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L8-L8), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L9-L9)


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

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L5-L5) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L6-L6), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L7-L7), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L8-L8), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L9-L9), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L10-L10), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L11-L11), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L12-L12)


```solidity

File: packages/contracts/contracts/CollSurplusPool.sol

5: import "./Interfaces/ICollSurplusPool.sol";

6: import "./Dependencies/ICollateralToken.sol";

7: import "./Dependencies/SafeERC20.sol";

8: import "./Dependencies/ReentrancyGuard.sol";

9: import "./Dependencies/AuthNoOwner.sol";

10: import "./Interfaces/IActivePool.sol";


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L5-L5) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L6-L6), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L7-L7), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L8-L8), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L9-L9), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L10-L10)


```solidity

File: packages/contracts/contracts/EBTCToken.sol

5: import "./Interfaces/IEBTCToken.sol";

7: import "./Dependencies/AuthNoOwner.sol";

8: import "./Dependencies/PermitNonce.sol";


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L5-L5) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L7-L7), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L8-L8)


```solidity

File: packages/contracts/contracts/PriceFeed.sol

5: import "./Interfaces/IPriceFeed.sol";

6: import "./Interfaces/IFallbackCaller.sol";

7: import "./Dependencies/AggregatorV3Interface.sol";

8: import "./Dependencies/BaseMath.sol";

9: import "./Dependencies/EbtcMath.sol";

10: import "./Dependencies/AuthNoOwner.sol";


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L5-L5) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L6-L6), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L7-L7), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L8-L8), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L9-L9), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L10-L10)


```solidity

File: packages/contracts/contracts/SortedCdps.sol

5: import "./Interfaces/ISortedCdps.sol";

6: import "./Interfaces/ICdpManager.sol";

7: import "./Interfaces/IBorrowerOperations.sol";


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L5-L5) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L6-L6), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L7-L7)


```solidity

File: packages/contracts/contracts/HintHelpers.sol

5: import "./Interfaces/ICdpManager.sol";

6: import "./Interfaces/ISortedCdps.sol";

7: import "./Dependencies/EbtcBase.sol";


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L5-L5) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L6-L6), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L7-L7)


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

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L4-L4) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L5-L5), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L6-L6), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L7-L7), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L8-L8), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L9-L9), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L10-L10), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L12-L12)


```solidity

File: packages/contracts/contracts/LeverageMacroFactory.sol

5: import "./Dependencies/ICollateralToken.sol";

6: import "./Interfaces/IEBTCToken.sol";


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroFactory.sol#L5-L5) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroFactory.sol#L6-L6)


```solidity

File: packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol

5: import "../Interfaces/IERC3156FlashLender.sol";

6: import "../Interfaces/IWETH.sol";


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L5-L5) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L6-L6)


```solidity

File: packages/contracts/contracts/Dependencies/EbtcBase.sol

5: import "./BaseMath.sol";

6: import "./EbtcMath.sol";

7: import "../Interfaces/IActivePool.sol";

8: import "../Interfaces/IPriceFeed.sol";

9: import "../Interfaces/IEbtcBase.sol";

10: import "../Dependencies/ICollateralToken.sol";


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L5-L5) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L6-L6), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L7-L7), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L8-L8), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L9-L9), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L10-L10)


```solidity

File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

6: import "./EnumerableSet.sol";


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L6-L6) 


```solidity

File: packages/contracts/contracts/Interfaces/IActivePool.sol

5: import "./IPool.sol";


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IActivePool.sol#L5-L5) 


```solidity

File: packages/contracts/contracts/Interfaces/IBorrowerOperations.sol

4: import "./IPositionManagers.sol";


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L4-L4) 


```solidity

File: packages/contracts/contracts/Interfaces/ICdpManager.sol

5: import "./IEbtcBase.sol";

6: import "./ICdpManagerData.sol";


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManager.sol#L5-L5) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManager.sol#L6-L6)


```solidity

File: packages/contracts/contracts/Interfaces/ICdpManagerData.sol

5: import "./ICollSurplusPool.sol";

6: import "./IEBTCToken.sol";

7: import "./ISortedCdps.sol";

8: import "./IActivePool.sol";

9: import "./IRecoveryModeGracePeriod.sol";

10: import "../Dependencies/ICollateralTokenOracle.sol";


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L5-L5) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L6-L6), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L7-L7), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L8-L8), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L9-L9), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L10-L10)


```solidity

File: packages/contracts/contracts/Interfaces/IEbtcBase.sol

5: import "./IPriceFeed.sol";


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IEbtcBase.sol#L5-L5) 


```solidity

File: packages/contracts/contracts/Interfaces/IEBTCToken.sol

5: import "../Dependencies/IERC20.sol";

6: import "../Dependencies/IERC2612.sol";


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IEBTCToken.sol#L5-L5) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IEBTCToken.sol#L6-L6)


```solidity

File: packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol

5: import "./IERC3156FlashBorrower.sol";


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol#L5-L5) 


</details>


### [NC&#x2011;32] Inconsistent spacing in comments 
Some lines use `// x` and some use `//x`. The instances below point out the usages that don't follow the majority, within each file


*There are 1 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/HintHelpers.sol

105:                         partialRedemptionHintNICR = 0; //reset to 0 as there is no partial redemption in this case


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L105-L105) 


</details>


### [NC&#x2011;33] Incorrect NatSpec Syntax 
In Solidity, just like in most other programming languages, regular comments serve to make code more understandable for developers. These are usually denoted by `//` for single line comments, or `/* ... */` for multi-line comments, and are ignored by the compiler.
On the other hand, NatSpec comments in Solidity, denoted by `///` for single - line comments, or`/** ... */` for multi - line comments, serve a different purpose.Besides aiding developer comprehension, they also form a part of the contract's interface, as they can be parsed and used by tools such as automated documentation generators or IDEs to provide users with details about the contract's functions, parameters and behavior.NatSpec comments can also be retrieved via JSON interfaces, and as such, they're included in the contract's ABI.
Thus, using`///` and `/** ... */` appropriately ensures not only proper documentation for developers, but also helps create a richer and more informative interface for users and external tools interacting with your contract.


*There are 7 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/CdpManager.sol

132:     /// @notice // Redeem as much collateral as possible from given Cdp in exchange for EBTC up to specified maximum


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L132-L132) 


```solidity

File: packages/contracts/contracts/PriceFeed.sol

782:     // @notice Returns the price of stETH:BTC in 18 decimals denomination

783:     // @param _ethBtcAnswer CL price retrieve from ETH:BTC feed

784:     // @param _stEthEthAnswer CL price retrieve from stETH:BTC feed

785:     // @param _ethBtcDecimals ETH:BTC feed decimals

786:     // @param _stEthEthDecimals stETH:BTC feed decimalss

787:     // @return The aggregated calculated price for stETH:BTC


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L782-L782) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L783-L783), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L784-L784), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L785-L785), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L786-L786), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L787-L787)


</details>


### [NC&#x2011;34] Interfaces should be defined in separate files from their usage 
The interfaces below should be defined in separate files, so that it's easier for future projects to import them, and to avoid duplication later on if they need to be used elsewhere in the project


*There are 2 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

//@audit the interface `ICdpCdps` is declared in this file and used in it here:
31:     ICdpCdps public immutable cdpManager;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L31-L31) 


```solidity

File: packages/contracts/contracts/LeverageMacroDelegateTarget.sol

//@audit the interface `IOwnerLike` is declared in this file and used in it here:
64:         address _owner = IOwnerLike(address(this)).owner();


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L64-L64) 


</details>


### [NC&#x2011;35] `internal` functions not called by the contract should be removed 
If the functions are required by an interface, the contract should inherit from that interface and use the `override` keyword


*There are 6 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/EBTCToken.sol

306:     function _requireCallerIsBorrowerOperations() internal view {

323:     function _requireCallerIsCdpM() internal view {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L306-L306) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L323-L323)


```solidity

File: packages/contracts/contracts/Dependencies/EbtcBase.sol

95:     function _checkRecoveryMode(uint256 _price) internal view returns (bool) {

103:     function _requireUserAcceptsFee(

115:     function _convertDebtDenominationToBtc(

124:     function _checkICRAgainstLiqThreshold(uint256 _icr, uint _tcr) internal view returns (bool) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L95-L95) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L103-L103), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L115-L115), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L124-L124)


</details>


### [NC&#x2011;36] Large numeric literals should use underscores for readability 



*There are 10 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

148:     uint256 public minuteDecayFactor = 999037758833783000;

150:     uint256 public constant MAX_MINUTE_DECAY_FACTOR = 999999999999999999; // Corresponds to a very fast decay rate, but not too extreme

141:     uint256 public constant MIN_REDEMPTION_FEE_FLOOR = (DECIMAL_PRECISION * 5) / 1000; // 0.5%


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L148-L148) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L150-L150), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L141-L141)


```solidity

File: packages/contracts/contracts/PriceFeed.sol

32:     uint256 public constant TIMEOUT_ETH_BTC_FEED = 4800; // 1 hours & 20min: 60 * 80

33:     uint256 public constant TIMEOUT_STETH_ETH_FEED = 90000; // 25 hours: 60 * 60 * 25


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L32-L32) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L33-L33)


```solidity

File: packages/contracts/contracts/Dependencies/EbtcBase.sol

19:     uint256 public constant LICR = 1030000000000000000; // 103%

22:     uint256 public constant MCR = 1100000000000000000; // 110%

25:     uint256 public constant CCR = 1250000000000000000; // 125%


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L19-L19) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L22-L22), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L25-L25)


```solidity

File: packages/contracts/contracts/Dependencies/EbtcMath.sol

60:         if (_minutes > 525600000) {

61:             _minutes = 525600000;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcMath.sol#L60-L60) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcMath.sol#L61-L61)


</details>


### [NC&#x2011;37] Long functions should be refactored into multiple, smaller, functions 



*There are 25 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/ActivePool.sol

261:     function flashLoan(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L261-L261) 


```solidity

File: packages/contracts/contracts/BorrowerOperations.sol

328:     function _adjustCdpInternal(

439:     function _openCdp(

852:     function _requireValidAdjustmentInCurrentMode(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L328-L328) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L439-L439), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L852-L852)


```solidity

File: packages/contracts/contracts/CdpManager.sol

135:     function _redeemCollateralFromCdp(

272:     function _isValidFirstRedemptionHint(

320:     function redeemCollateral(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L135-L135) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L272-L272), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L320-L320)


```solidity

File: packages/contracts/contracts/LiquidationLibrary.sol

61:     function _liquidateIndividualCdpSetup(

135:     function _liquidateIndividualCdpSetupCDP(

223:     function _liquidateIndividualCdpSetupCDPInNormalMode(

295:     function _liquidateIndividualCdpSetupCDPInRecoveryMode(

397:     function _liquidateCDPPartially(

679:     function batchLiquidateCdps(bytes32[] memory _cdpArray) external nonReentrantSelfAndBOps {

733:     function _getTotalFromBatchLiquidate_RecoveryMode(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L61-L61) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L135-L135), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L223-L223), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L295-L295), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L397-L397), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L679-L679), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L733-L733)


```solidity

File: packages/contracts/contracts/CdpManagerStorage.sol

111:     function setGracePeriod(uint128 _gracePeriod) external requiresAuth {

344:     function _syncAccounting(bytes32 _cdpId) internal {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L111-L111) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L344-L344)


```solidity

File: packages/contracts/contracts/PriceFeed.sol

98:     function fetchPrice() external override returns (uint256) {

606:     function _getCurrentChainlinkResponse()

687:     function _getPrevChainlinkResponse(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L98-L98) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L606-L606), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L687-L687)


```solidity

File: packages/contracts/contracts/SortedCdps.sol

363:     function _insert(bytes32 _id, uint256 _NICR, bytes32 _prevId, bytes32 _nextId) internal {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L363-L363) 


```solidity

File: packages/contracts/contracts/HintHelpers.sol

48:     function getRedemptionHints(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L48-L48) 


```solidity

File: packages/contracts/contracts/LeverageMacroBase.sol

43:     function _assertOwner() internal {

118:     function doOperation(

244:     function _doCheckValueType(CheckValueAndType memory check, uint256 valueToCheck) internal {

291:     function _handleOperation(LeverageMacroOperation memory operation) internal {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L43-L43) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L118-L118), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L244-L244), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L291-L291)


</details>


### [NC&#x2011;38] Long lines of code 
Usually lines in source code are limited to [80](https://softwareengineering.stackexchange.com/questions/148677/why-is-80-characters-the-standard-limit-for-code-width) characters. Today's screens are much larger so it's reasonable to stretch this in some cases. The solidity style guide recommends a maximumum line length of [120 characters](https://docs.soliditylang.org/en/v0.8.17/style-guide.html#maximum-line-length), so the lines below should be split when they reach that length.


*There are 128 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/ActivePool.sol

39:     /// @dev Initializes the contract with the borrowerOperationsAddress, cdpManagerAddress, collateral token address, collSurplusAddress, and feeRecipientAddress

71:     /// @dev Not necessarily equal to the the contract's raw systemCollShares balance - tokens can be forcibly sent to contracts

79:     /// @dev The amount of EBTC debt in the pool. Like systemCollShares, this is not necessarily equal to the contract's EBTC token balance - tokens can be forcibly sent to contracts

119:     /// @notice Liquidator reward shares are not tracked via internal accounting in the active pool and are assumed to be present in expected amount as part of the intended behavior of BorowerOperations and CdpManager

121:     /// @dev closeCdp() or liqudations result in the actor (borrower or liquidator respectively) receiving the liquidator reward shares

123:     /// @dev Note that funds in the coll surplus pool, just like liquidator reward shares, are not tracked as part of the system CR or coll of a CDP.

154:     /// @dev If the fee recipient address is changed while outstanding claimable coll is available, only the new fee recipient will be able to claim the outstanding coll

177:     /// @notice Helper function to transfer stETH shares to another address, ensuring to call hooks into other system pools if they are the recipient

268:         uint256 fee = flashFee(token, amount); // NOTE: Check for `token` is implicit in the requires above // also checks for paused

293:         //  You technically could, but you'd be having to repay any amount below systemCollShares to get Fl2 to not revert

347:         ICdpManagerData(cdpManagerAddress).syncGlobalAccountingAndGracePeriod(); // Calling this increases shares so do it first


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L39-L39) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L71-L71), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L79-L79), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L119-L119), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L121-L121), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L123-L123), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L154-L154), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L177-L177), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L268-L268), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L293-L293), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L347-L347)


```solidity

File: packages/contracts/contracts/BorrowerOperations.sol

31:     // keccak256("permitPositionManagerApproval(address borrower,address positionManager,uint8 status,uint256 nonce,uint256 deadline)");

34:             "PermitPositionManagerApproval(address borrower,address positionManager,uint8 status,uint256 nonce,uint256 deadline)"

64:     // Mapping of borrowers to approved position managers, by approval status: cdpOwner(borrower) -> positionManager -> PositionManagerApproval (None, OneTime, Persistent)

140:         @notice BorrowerOperations and CdpManager share reentrancy status by confirming the other's locked flag before beginning operation

141:         @dev This is an alternative to the more heavyweight solution of both being able to set the reentrancy flag on a 3rd contract.

160:     /// @notice Function that creates a Cdp for the caller with the requested debt, and the stETH received as collateral.

161:     /// @notice Successful execution is conditional mainly on the resulting collateralization ratio which must exceed minimum requirement, e.g., MCR.

177:     /// @notice Function that creates a Cdp for the specified _borrower by caller with the requested debt, and the stETH received as collateral.

179:     /// @notice Successful execution is conditional mainly on the resulting collateralization ratio which must exceed minimum requirement, e.g., MCR.

214:     /// @notice Successful execution is conditional on whether the withdrawal would bring down the ICR or TCR to the minimum requirement, e.g., MCR or CCR

228:     /// @notice Function that withdraws `_debt` amount of eBTC token from the specified Cdp, thus increasing its debt accounting

230:     /// @notice Successful execution is conditional on whether the withdrawal would bring down the ICR or TCR to the minimum requirement, e.g., MCR or CCR

267:     /// @param _isDebtIncrease The flag (true or false) to indicate whether this is a eBTC token withdrawal (debt increase) or a repayment (debt reduce)

296:     /// @param _isDebtIncrease The flag (true or false) to indicate whether this is a eBTC token withdrawal (debt increase) or a repayment (debt reduce)

392:         // When the adjustment is a debt repayment, check it's a valid amount, that the caller has enough EBTC, and that the resulting debt is >0

451:         // ICR is based on the net stEth balance, i.e. the specified stEth balance amount - fixed liquidator incentive gas comp.

533:             The static liqudiation incentive is stored in the gas pool and can be considered a deposit / voucher to be returned upon Cdp close, to the closer.

537:         // CEI: Move the collateral and liquidator gas compensation to the Active Pool. Track only net collateral for TCR purposes.

597:     /// @notice when a Cdp has been fully redeemed from and closed, or liquidated in Recovery Mode with a collateralization ratio higher enough (like over MCR)

624:     /// @notice Position managers with 'OneTIme' status will be able to take a single action on one Cdp. Approval will be automatically revoked after one Cdp-related action.

625:     /// @notice Similar to approving tokens, approving a position manager allows _stealing of all positions_ if given to a malicious account.

627:     /// @param _approval PositionManagerApproval (None/OneTime/Persistent) status set to the specified _positionManager for caller's Cdp

645:     /// @notice Similar to approving tokens, approving a position manager allows _stealing of all positions_ if given to a malicious account.

782:     /// @dev These number of liquidator shares associated with each Cdp are stored in the Cdp, while the actual tokens float in the active pool

977:         /// @dev If the PositionManagerApproval was none, we should have failed with the check in _requireBorrowerOrPositionManagerAndUpdateManagerApproval

1084:         uint256 fee = flashFee(token, amount); // NOTE: Check for `eBTCToken` is implicit here // NOTE: Pause check is here

1122:     /// @param token The address of the token to get the maximum flash loan amount for, exclusively used here for eBTC token


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L31-L31) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L34-L34), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L64-L64), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L140-L140), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L141-L141), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L160-L160), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L161-L161), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L177-L177), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L179-L179), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L214-L214), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L228-L228), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L230-L230), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L267-L267), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L296-L296), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L392-L392), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L451-L451), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L533-L533), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L537-L537), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L597-L597), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L624-L624), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L625-L625), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L627-L627), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L645-L645), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L782-L782), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L977-L977), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L1084-L1084), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L1122-L1122)


```solidity

File: packages/contracts/contracts/CdpManager.sol

13: /// @title CdpManager is mainly in charge of all Cdp related core processing like collateral & debt accounting, split fee calculation, redemption, etc

96:     /// @notice callable by anyone, attempts to liquidate the CdpId. Executes successfully if Cdp meets the conditions for liquidation (e.g. in Normal Mode, it liquidates if the Cdp's ICR < the system MCR).

122:     /// @notice Steps through the provided list and attempts to liquidate every Cdp, until it reaches the end or it runs out of gas.

271:     /// @dev Returns true if the specified CdpId is not blank, exists in the list, has an ICR > MCR, and the next lower Cdp in the list is either blank or has an ICR < MCR.

291:     /// @notice Note that if _debt is very large, this function can run out of gas, specially if traversed cdps are small (meaning many small Cdps are redeemed against).

292:     /// @notice This can be easily avoided by splitting the total _debt in appropriate chunks and calling the function multiple times.

294:     /// @notice There is a optional parameter `_maxIterations` which can also be provided, so the loop through Cdps is capped (if itb�s zero, it will be ignored).

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

515:         /// @audit Opening can cause invalid reordering of Cdps due to changing values without reInserting into sortedCdps

579:     /// @return TCR The cached total collateralization ratio (TCR) of the system (does not take into account pending global state)

919:         cdpStEthFeePerUnitIndex[_cdpId] = systemStEthFeePerUnitIndex; /// @audit We critically assume global accounting is synced here


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L13-L13) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L96-L96), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L122-L122), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L271-L271), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L291-L291), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L292-L292), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L294-L294), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L295-L295), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L296-L296), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L299-L299), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L301-L301), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L304-L304), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L305-L305), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L311-L311), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L314-L314), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L315-L315), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L316-L316), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L317-L317), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L515-L515), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L579-L579), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L919-L919)


```solidity

File: packages/contracts/contracts/LiquidationLibrary.sol

12: /// @dev This contract shares same base and storage layout with CdpManager and is the delegatecall destination from CdpManager

37:     /// @notice callable by anyone, attempts to liquidate the CdpId. Executes successfully if Cdp meets the conditions for liquidation (e.g. in Normal Mode, it liquidates if the Cdp's ICR < the system MCR).

134:     // For partial liquidation, caller should use HintHelper smart contract to get correct hints for reinsertion into sorted CDP list

311:         // I don't see an issue emitting the CdpUpdated() event up here and avoiding an extra cache of the values, any objections?

675:     /// @notice Steps through the provided list and attempts to liquidate every Cdp, until it reaches the end or it runs out of gas.


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L12-L12) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L37-L37), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L134-L134), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L311-L311), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L675-L675)


```solidity

File: packages/contracts/contracts/CdpManagerStorage.sol

27:     /// @notice Start the recovery mode grace period, if the system is in RM and the grace period timestamp has not already been set

150:     uint256 public constant MAX_MINUTE_DECAY_FACTOR = 999999999999999999; // Corresponds to a very fast decay rate, but not too extreme

175:     // Snapshot of the total collateral across the ActivePool, immediately after the latest liquidation and split fee claim

197:     /* Global Fee accumulator (never decreasing) per stake unit in CDPManager, similar to systemDebtRedistributionIndex */

239:     /// @notice BorrowerOperations and CdpManager share reentrancy status by confirming the other's locked flag before beginning operation

240:     /// @dev This is an alternative to the more heavyweight solution of both being able to set the reentrancy flag on a 3rd contract.

303:     /// @dev get the pending Cdp debt "reward" (i.e. the amount of extra debt assigned to the Cdp) from liquidation redistribution events, earned by their stake

613:     /// @param _systemStEthFeePerUnitIndex The fee-per-stake-unit value to be used in fee split calculation, could be result of calcFeeUponStakingReward()

683:     /// @return The Nominal Collateral Ratio (NICR) of the specified Cdp with fee split and debt redistribution considered.

716:     /// @notice Return the pending extra debt assigned to the Cdp from liquidation redistribution, calcualted by Cdp's stake

726:     /// @return Whether the debt redistribution tracking index of the specified Cdp is less than the global tracking one (meaning it might get pending debt redistribution)

740:     /// @notice Calculate the Cdps entire debt and coll, including pending debt redistributions and collateral reduction from split fee.

781:     /// @dev calculate pending state change to be applied for given CDP and global split index(typically already synced):


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L27-L27) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L150-L150), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L175-L175), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L197-L197), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L239-L239), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L240-L240), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L303-L303), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L613-L613), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L683-L683), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L716-L716), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L726-L726), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L740-L740), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L781-L781)


```solidity

File: packages/contracts/contracts/CollSurplusPool.sol

14: /// @dev While an owner could have multiple different sized Cdps, the remaining surplus colateral from all of its closed Cdp

36:      * @dev One-time initialization function. Can only be called by the owner as a security measure. Ownership is renounced after the function is called.


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L14-L14) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L36-L36)


```solidity

File: packages/contracts/contracts/EBTCToken.sol

16:  * https://github.com/OpenZeppelin/openzeppelin-contracts/blob/53516bc555a454862470e7860a9b5254db4d00f5/contracts/token/ERC20/ERC20Permit.sol

21:  * 1) Transfer protection: blocklist of addresses that are invalid recipients (i.e. core Ebtc contracts) in external transfer() and transferFrom() calls.


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L16-L16) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L21-L21)


```solidity

File: packages/contracts/contracts/Governor.sol

9: /// @notice We have taken the tradeoff of additional storage usage for easier readabiliy without using off-chain / indexing services.

11: /// @author Modified from Solmate (https://github.com/transmissions11/solmate/blob/main/src/auth/authorities/RolesAuthority.sol)


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L9-L9) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L11-L11)


```solidity

File: packages/contracts/contracts/PriceFeed.sol

31:     // Maximum time period allowed since Chainlink's latest round data timestamp, beyond which Chainlink is considered frozen.

96:     /// @dev Uses a main oracle (Chainlink) and a fallback oracle in case Chainlink fails. If both fail, it uses the last good price seen by eBTC.

97:     /// @dev The fallback oracle address can be swapped by the Authority. The fallback oracle must conform to the IFallbackCaller interface.

166:                  * If Fallback is live and both oracles have a similar price, conclude that Chainlink's large price deviation between

173:                 // If Fallback is live but the oracles differ too much in price, conclude that Chainlink's initial price deviation was

296:             // If Chainlink is live and Fallback is frozen, just use last good price (no status change) since we have no basis for comparison

308:             // Otherwise if Chainlink is live but price not within 5% of Fallback, distrust Chainlink, and return Fallback price

326:             // If Chainlink and Fallback are both live, unbroken and similar price, switch back to chainlinkWorking and return Chainlink price

345:             // Otherwise if Chainlink is live and deviated <50% from it's previous price and Fallback is still untrusted,

394:     /// @dev Chainlink is considered broken if its current or previous round data is in any way bad. We check the previous round for two reasons.

396:     /// @dev 2. Chainlink is the PriceFeed's preferred primary oracle - having two consecutive valid round responses adds peace of mind when using or returning to Chainlink.

408:     /// @dev A response is considered bad if the success value reports failure, or if the timestamp is invalid (0 or in the future)

432:     /// @dev The oracle is considered frozen if either of the feed timestamps are older than the threshold specified by the static timeout thresholds

444:     /// @return A boolean indicating whether the price change from Chainlink oracle is above the maximum threshold allowed

521:     /// @notice Checks if the prices reported by the Chainlink and fallback oracles are similar, within the maximum deviation specified by MAX_PRICE_DIFFERENCE_BETWEEN_ORACLES.

530:         // Get the relative price difference between the oracles. Use the lower price as the denominator, i.e. the reference for the calculation.

538:          * Return true if the relative price difference is <= MAX_PRICE_DIFFERENCE_BETWEEN_ORACLES: if so, we assume both oracles are probably reporting

579:     /// @notice Retrieves the latest response from the fallback oracle. If the fallback oracle address is set to the zero address, it returns a failing struct.

605:     /// @return chainlinkResponse A struct containing data retrieved from the price feeds, including the round IDs, timestamps, aggregated price, and a success flag.

686:     /// @return prevChainlinkResponse A struct containing data retrieved from the price feeds, including the round IDs, timestamps, aggregated price, and a success flag.

771:     /// @notice Returns if the CL feed is healthy or not, based on: negative value and null round id. For price aggregation


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L31-L31) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L96-L96), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L97-L97), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L166-L166), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L173-L173), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L296-L296), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L308-L308), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L326-L326), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L345-L345), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L394-L394), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L396-L396), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L408-L408), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L432-L432), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L444-L444), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L521-L521), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L530-L530), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L538-L538), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L579-L579), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L605-L605), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L686-L686), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L771-L771)


```solidity

File: packages/contracts/contracts/SortedCdps.sol

21:  * The list relies on the fact that liquidation events preserve ordering: a liquidation decreases the NICRs of all active Cdps,

37:  * - Ordering checks for insertion are performed by comparing an NICR argument to the current NICR, calculated at runtime.

40:  * - Public functions with parameters have been made internal to save gas, and given an external wrapper function for external access

100:     /// @dev Inspired https://github.com/balancer-labs/balancer-v2-monorepo/blob/18bd5fb5d87b451cc27fbd30b276d1fb2987b529/pkg/vault/contracts/PoolRegistry.sol

134:     /// @notice Find a specific CDP for a given owner, indexed by it's place in the linked list relative to other Cdps owned by the same address

148:     /// @dev a pagination-flavor search (from least ICR to biggest ICR) for CDP owned by given owner and specified index (starting at given CDP)

171:     /// @return cdpId The CDP Id if found, otherwise return current lastly-visited CDP as the startNode for next pagination

280:     /// @dev a pagination-flavor search retrieval of (from least ICR to biggest ICR) Cdps owned by given owner (starting at given CDP)

283:     /// @return all CdpIds of the specified owner found by search starting at the specified startNodeId for the specified maximum iteration count

309:         // Two-pass strategy, halving the amount of Cdps we can process before relying on pagination or off-chain methods

606:             // `(_prevId, _nextId)` is a valid insert position if they are adjacent nodes and `_NICR` falls between the two nodes' NICRs


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L21-L21) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L37-L37), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L40-L40), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L100-L100), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L134-L134), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L148-L148), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L171-L171), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L280-L280), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L283-L283), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L309-L309), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L606-L606)


```solidity

File: packages/contracts/contracts/HintHelpers.sol

9: /// @title HintHelpers mainly serves to provide handy information to facilitate offchain integration like redemption bots.

100:                     // If the partial redemption would leave the CDP with less than the minimum allowed coll, bail out of partial redemption and return only the fully redeemable


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L9-L9) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L100-L100)


```solidity

File: packages/contracts/contracts/LeverageMacroBase.sol

24: /// @custom:known-issue Due to slippage some dust amounts for all intermediary tokens can be left, since there's no way to ask to sell all available

233:     /// @dev If you delegatecall into this, this will transfer the tokens to the caller of the DiamondLike (and not the contract)

413:         // But technically you could approve w/e you want here, this is fine because the contract is a router and will not hold user funds

426:         // val -> 0 -> 0 -> val means this is safe to repeat since even if full approve is unused, we always go back to 0 after

496:     /// @dev excessivelySafeCall to perform generic calls without getting gas bombed | useful if you don't care about return value


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L24-L24) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L233-L233), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L413-L413), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L426-L426), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L496-L496)


```solidity

File: packages/contracts/contracts/SimplifiedDiamondLike.sol

16:  *  Per solidity, hardcoded functions are switched into, meaning they cannot be overriden (although you could set a callbackHandler that cannot be reached)


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L16-L16) 


```solidity

File: packages/contracts/contracts/Dependencies/EbtcBase.sol

24:     // Critical system collateral ratio. If the system's total collateral ratio (TCR) falls below the CCR, Recovery Mode is triggered.

66:     /// @dev Collateral tokens stored in ActivePool for liquidator rewards, fees, or coll in CollSurplusPool, are not included


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L24-L24) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L66-L66)


```solidity

File: packages/contracts/contracts/Dependencies/ReentrancyGuard.sol

6: /// @author Modified from OpenZeppelin (https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/security/ReentrancyGuard.sol)


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/ReentrancyGuard.sol#L6-L6) 


```solidity

File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

10: /// @author Modified from Solmate (https://github.com/transmissions11/solmate/blob/main/src/auth/authorities/RolesAuthority.sol)

61:             - That capability is public, or the user has a role that has been granted the capability to call the function


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L10-L10) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L61-L61)


</details>


### [NC&#x2011;39] File is missing NatSpec 



*There are 15 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol

0: 


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L0-L0) 


```solidity

File: packages/contracts/contracts/Interfaces/IActivePool.sol

0: 


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IActivePool.sol#L0-L0) 


```solidity

File: packages/contracts/contracts/Interfaces/IBorrowerOperations.sol

0: 


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L0-L0) 


```solidity

File: packages/contracts/contracts/Interfaces/ICdpManager.sol

0: 


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManager.sol#L0-L0) 


```solidity

File: packages/contracts/contracts/Interfaces/ICdpManagerData.sol

0: 


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L0-L0) 


```solidity

File: packages/contracts/contracts/Interfaces/ICollSurplusPool.sol

0: 


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICollSurplusPool.sol#L0-L0) 


```solidity

File: packages/contracts/contracts/Interfaces/IEbtcBase.sol

0: 


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IEbtcBase.sol#L0-L0) 


```solidity

File: packages/contracts/contracts/Interfaces/IEBTCToken.sol

0: 


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IEBTCToken.sol#L0-L0) 


```solidity

File: packages/contracts/contracts/Interfaces/IFallbackCaller.sol

0: 


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IFallbackCaller.sol#L0-L0) 


```solidity

File: packages/contracts/contracts/Interfaces/IPermitNonce.sol

0: 


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPermitNonce.sol#L0-L0) 


```solidity

File: packages/contracts/contracts/Interfaces/IPool.sol

0: 


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPool.sol#L0-L0) 


```solidity

File: packages/contracts/contracts/Interfaces/IPositionManagers.sol

0: 


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPositionManagers.sol#L0-L0) 


```solidity

File: packages/contracts/contracts/Interfaces/IPriceFeed.sol

0: 


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPriceFeed.sol#L0-L0) 


```solidity

File: packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol

0: 


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol#L0-L0) 


```solidity

File: packages/contracts/contracts/Interfaces/ISortedCdps.sol

0: 


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ISortedCdps.sol#L0-L0) 


</details>


### [NC&#x2011;40] Mixed usage of `int`/`uint` with `int256`/`uint256` 
`int256`/`uint256` are the preferred type names (they're what are used for function signatures), so they should be used consistently


*There are 40 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

834:     function _requireNonZeroDebtChange(uint _debtChange) internal pure {

830:         uint status = cdpManager.getCdpStatus(_cdpId);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L834-L834) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L830-L830)


```solidity

File: packages/contracts/contracts/LiquidationLibrary.sol

278:         uint _debtToColl = (_totalDebtToBurn * DECIMAL_PRECISION) / _liqState.price;

279:         uint _cappedColl = collateral.getPooledEthByShares(_cappedColPortion + _liquidatorReward);

365:         uint _debtToColl = (_totalDebtToBurn * DECIMAL_PRECISION) / _recoveryState.price;

366:         uint _cappedColl = collateral.getPooledEthByShares(_cappedColPortion + _liquidatorReward);

435:             uint _debtToColl = (_partialDebt * DECIMAL_PRECISION) / _partialState.price;

436:             uint _cappedColl = collateral.getPooledEthByShares(_partialColl);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L278-L278) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L279-L279), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L365-L365), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L366-L366), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L435-L435), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L436-L436)


```solidity

File: packages/contracts/contracts/CdpManagerStorage.sol

357:             uint _pendingDebt,

365:             uint prevCollShares = _cdp.coll;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L357-L357) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L365-L365)


```solidity

File: packages/contracts/contracts/SortedCdps.sol

159:         uint maxNodes

177:         uint maxNodes

230:         uint maxNodes

240:         uint maxNodes

289:         uint maxNodes

302:         uint maxNodes,

303:         uint maxArraySize

182:         uint _currentIndex = 0;

183:         uint i;

245:         uint _ownedCount = 0;

246:         uint i = 0;

273:         (uint _ownedCount, ) = _cdpCountOf(owner, dummyId, 0);

293:         (uint _ownedCount, ) = _cdpCountOf(owner, startNodeId, maxNodes);

311:         uint i = 0;

312:         uint _cdpRetrieved;

449:         for (uint i = 0; i < _len; ++i) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L159-L159) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L177-L177), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L230-L230), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L240-L240), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L289-L289), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L302-L302), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L303-L303), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L182-L182), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L183-L183), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L245-L245), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L246-L246), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L273-L273), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L293-L293), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L311-L311), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L312-L312), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L449-L449)


```solidity

File: packages/contracts/contracts/Dependencies/EbtcBase.sol

124:     function _checkICRAgainstLiqThreshold(uint256 _icr, uint _tcr) internal view returns (bool) {

140:     function _checkICRAgainstTCR(uint256 _icr, uint _tcr) internal view returns (bool) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L124-L124) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L140-L140)


```solidity

File: packages/contracts/contracts/Interfaces/IBorrowerOperations.sol

28:         uint _EBTCAmount,

31:         uint _collAmount,


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L28-L28) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L31-L31)


```solidity

File: packages/contracts/contracts/Interfaces/ICdpManager.sol

56:     function getCdpLiquidatorRewardShares(bytes32 _cdpId) external view returns (uint);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManager.sol#L56-L56) 


```solidity

File: packages/contracts/contracts/Interfaces/ICdpManagerData.sol

45:         uint _debt,

46:         uint _collShares,

49:         uint _premiumToLiquidator

58:         uint _premiumToLiquidator


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L45-L45) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L46-L46), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L49-L49), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L58-L58)


```solidity

File: packages/contracts/contracts/Interfaces/IPositionManagers.sol

36:         uint _deadline,


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPositionManagers.sol#L36-L36) 


```solidity

File: packages/contracts/contracts/Interfaces/ISortedCdps.sol

9:     event NodeAdded(bytes32 _id, uint _NICR);

66:         uint maxNodes

74:         uint maxNodes

83:         uint maxNodes


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ISortedCdps.sol#L9-L9) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ISortedCdps.sol#L66-L66), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ISortedCdps.sol#L74-L74), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ISortedCdps.sol#L83-L83)


</details>


### [NC&#x2011;41] Consider using named mappings 
Consider using [named mappings](https://ethereum.stackexchange.com/a/145555) to make it easier to understand the purpose of each mapping


*There are 18 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

65:     mapping(address => mapping(address => PositionManagerApproval)) public positionManagers;

65:     mapping(address => mapping(address => PositionManagerApproval)) public positionManagers;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L65-L65) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L65-L65)


```solidity

File: packages/contracts/contracts/CdpManagerStorage.sol

168:     mapping(bytes32 => Cdp) public Cdps;

190:     mapping(bytes32 => uint256) public cdpDebtRedistributionIndex;

202:     mapping(bytes32 => uint256) public cdpStEthFeePerUnitIndex;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L168-L168) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L190-L190), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L202-L202)


```solidity

File: packages/contracts/contracts/CollSurplusPool.sol

30:     mapping(address => uint256) internal balances;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L30-L30) 


```solidity

File: packages/contracts/contracts/EBTCToken.sol

51:     mapping(address => uint256) private _balances;

52:     mapping(address => mapping(address => uint256)) private _allowances;

52:     mapping(address => mapping(address => uint256)) private _allowances;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L51-L51) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L52-L52), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L52-L52)


```solidity

File: packages/contracts/contracts/Governor.sol

30:     mapping(uint8 => string) internal roleNames;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L30-L30) 


```solidity

File: packages/contracts/contracts/SortedCdps.sol

74:         mapping(bytes32 => Node) nodes; // Track the corresponding ids for each node in the list


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L74-L74) 


```solidity

File: packages/contracts/contracts/SimplifiedDiamondLike.sol

34:         mapping(bytes4 => address) callbackHandler;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L34-L34) 


```solidity

File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

28:     mapping(address => EnumerableSet.Bytes32Set) internal enabledFunctionSigsByTarget;

32:     mapping(address => bytes32) public getUserRoles;

34:     mapping(address => mapping(bytes4 => CapabilityFlag)) public capabilityFlag;

34:     mapping(address => mapping(bytes4 => CapabilityFlag)) public capabilityFlag;

36:     mapping(address => mapping(bytes4 => bytes32)) public getRolesWithCapability;

36:     mapping(address => mapping(bytes4 => bytes32)) public getRolesWithCapability;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L28-L28) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L32-L32), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L34-L34), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L34-L34), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L36-L36), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L36-L36)


</details>


### [NC&#x2011;42] Consider using later versions of solidity for more cappabilities 
Consider using solidity 0.8.18 or later to benefit from multiple things including the named mappings [named mappings](https://ethereum.stackexchange.com/a/145555) to make it easier to understand the purpose of each mapping


*There are 39 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/ActivePool.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/BorrowerOperations.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/CdpManager.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/LiquidationLibrary.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/CdpManagerStorage.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/CollSurplusPool.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/EBTCToken.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/Governor.sol

2: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L2-L2) 


```solidity

File: packages/contracts/contracts/PriceFeed.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/SortedCdps.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/HintHelpers.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/LeverageMacroBase.sol

2: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L2-L2) 


```solidity

File: packages/contracts/contracts/LeverageMacroDelegateTarget.sol

2: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L2-L2) 


```solidity

File: packages/contracts/contracts/LeverageMacroFactory.sol

2: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroFactory.sol#L2-L2) 


```solidity

File: packages/contracts/contracts/LeverageMacroReference.sol

2: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroReference.sol#L2-L2) 


```solidity

File: packages/contracts/contracts/SimplifiedDiamondLike.sol

2: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L2-L2) 


```solidity

File: packages/contracts/contracts/Dependencies/Auth.sol

2: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/Auth.sol#L2-L2) 


```solidity

File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

2: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L2-L2) 


```solidity

File: packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/Dependencies/EbtcBase.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/Dependencies/EbtcMath.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcMath.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/Dependencies/ReentrancyGuard.sol

2: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/ReentrancyGuard.sol#L2-L2) 


```solidity

File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

2: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L2-L2) 


```solidity

File: packages/contracts/contracts/Interfaces/IActivePool.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IActivePool.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/Interfaces/IBorrowerOperations.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/Interfaces/ICdpManager.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManager.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/Interfaces/ICdpManagerData.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/Interfaces/ICollSurplusPool.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICollSurplusPool.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/Interfaces/IEbtcBase.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IEbtcBase.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/Interfaces/IEBTCToken.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IEBTCToken.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/Interfaces/IERC3156FlashBorrower.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IERC3156FlashBorrower.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/Interfaces/IFallbackCaller.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IFallbackCaller.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/Interfaces/IPermitNonce.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPermitNonce.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/Interfaces/IPool.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPool.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/Interfaces/IPositionManagers.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPositionManagers.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/Interfaces/IPriceFeed.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPriceFeed.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol

2: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol#L2-L2) 


```solidity

File: packages/contracts/contracts/Interfaces/ISortedCdps.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ISortedCdps.sol#L3-L3) 


</details>


### [NC&#x2011;43] Some error strings are not descriptive 
Consider adding more detail to these error strings


*There are 4 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/ActivePool.sol

//@audit This message need more details : !ActivePoolBal
104:         require(cachedSystemCollShares >= _shares, "!ActivePoolBal");


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L104-L104) 


```solidity

File: packages/contracts/contracts/LeverageMacroBase.sol

//@audit This message need more details : Must be owner
45:         require(owner() == msg.sender, "Must be owner");

//@audit This message need more details : Call has failed
421:         require(success, "Call has failed");


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L45-L45) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L421-L421)


```solidity

File: packages/contracts/contracts/SimplifiedDiamondLike.sol

//@audit This message need more details : Must be owner
111:         require(msg.sender == owner, "Must be owner");


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L111-L111) 


</details>


### [NC&#x2011;44] Events that mark critical parameter changes should contain both the old and the new value 
This should especially be done if the new value is not required to be different from the old value


*There are 30 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/Governor.sol

32:     event RoleNameSet(uint8 indexed role, string indexed name);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L32-L32) 


```solidity

File: packages/contracts/contracts/LeverageMacroFactory.sol

19:     event DeployNewMacro(address indexed sender, address indexed newContractAddress);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroFactory.sol#L19-L19) 


```solidity

File: packages/contracts/contracts/Dependencies/Auth.sol

12:     event AuthorityUpdated(address indexed user, Authority indexed newAuthority);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/Auth.sol#L12-L12) 


```solidity

File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

11:     event AuthorityUpdated(address indexed user, Authority indexed newAuthority);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L11-L11) 


```solidity

File: packages/contracts/contracts/Interfaces/IActivePool.sol

9:     event ActivePoolEBTCDebtUpdated(uint256 _EBTCDebt);

10:     event SystemCollSharesUpdated(uint256 _coll);

11:     event FeeRecipientAddressChanged(address indexed _feeRecipientAddress);

12:     event FeeRecipientClaimableCollSharesIncreased(uint256 _coll, uint256 _fee);

13:     event FeeRecipientClaimableCollSharesDecreased(uint256 _coll, uint256 _fee);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IActivePool.sol#L9-L9) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IActivePool.sol#L10-L10), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IActivePool.sol#L11-L11), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IActivePool.sol#L12-L12), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IActivePool.sol#L13-L13)


```solidity

File: packages/contracts/contracts/Interfaces/IBorrowerOperations.sol

10:     event FeeRecipientAddressChanged(address indexed _feeRecipientAddress);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L10-L10) 


```solidity

File: packages/contracts/contracts/Interfaces/ICdpManagerData.sol

16:     event FeeRecipientAddressChanged(address indexed _feeRecipientAddress);

17:     event StakingRewardSplitSet(uint256 _stakingRewardSplit);

18:     event RedemptionFeeFloorSet(uint256 _redemptionFeeFloor);

19:     event MinuteDecayFactorSet(uint256 _minuteDecayFactor);

20:     event BetaSet(uint256 _beta);

60:     event BaseRateUpdated(uint256 _baseRate);

61:     event LastRedemptionTimestampUpdated(uint256 _lastFeeOpTime);

62:     event TotalStakesUpdated(uint256 _newTotalStakes);

63:     event SystemSnapshotsUpdated(uint256 _totalStakesSnapshot, uint256 _totalCollateralSnapshot);

64:     event SystemDebtRedistributionIndexUpdated(uint256 _systemDebtRedistributionIndex);

65:     event CdpDebtRedistributionIndexUpdated(bytes32 _cdpId, uint256 _cdpDebtRedistributionIndex);

66:     event CdpArrayIndexUpdated(bytes32 _cdpId, uint256 _newIndex);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L16-L16) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L17-L17), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L18-L18), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L19-L19), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L20-L20), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L60-L60), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L61-L61), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L62-L62), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L63-L63), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L64-L64), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L65-L65), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L66-L66)


```solidity

File: packages/contracts/contracts/Interfaces/ICollSurplusPool.sol

8:     event SurplusCollSharesUpdated(address indexed _account, uint256 _newBalance);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICollSurplusPool.sol#L8-L8) 


```solidity

File: packages/contracts/contracts/Interfaces/IPool.sol

9:     event ETHBalanceUpdated(uint256 _newBalance);

10:     event EBTCBalanceUpdated(uint256 _newBalance);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPool.sol#L9-L9) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPool.sol#L10-L10)


```solidity

File: packages/contracts/contracts/Interfaces/IPositionManagers.sol

12:     event PositionManagerApprovalSet(
13:         address indexed _borrower,
14:         address indexed _positionManager,
15:         PositionManagerApproval _approval
16:     );


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPositionManagers.sol#L12-L16) 


```solidity

File: packages/contracts/contracts/Interfaces/IPriceFeed.sol

7:     event LastGoodPriceUpdated(uint256 _lastGoodPrice);

8:     event PriceFeedStatusChanged(Status newStatus);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPriceFeed.sol#L7-L7) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPriceFeed.sol#L8-L8)


```solidity

File: packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol

11:     event GracePeriodDurationSet(uint256 _recoveryModeGracePeriodDuration);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol#L11-L11) 


```solidity

File: packages/contracts/contracts/Interfaces/ISortedCdps.sol

9:     event NodeAdded(bytes32 _id, uint _NICR);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ISortedCdps.sol#L9-L9) 


</details>


### [NC&#x2011;45] `override` function arguments that are unused should have the variable name removed or commented out to avoid compiler warnings 



*There are 3 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/CdpManager.sol

//@audit _cdpId is not used
99:     function liquidate(bytes32 _cdpId) external override {

//@audit _cdpId is not used
//@audit _partialAmount is not used
//@audit _upperPartialHint is not used
//@audit _lowerPartialHint is not used
109:     function partiallyLiquidate(

//@audit _cdpArray is not used
126:     function batchLiquidateCdps(bytes32[] memory _cdpArray) external override {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L99-L99) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L109-L109), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L126-L126)


</details>


### [NC&#x2011;46] Use of `override` is unnecessary 
Starting with Solidity version [0.8.8](https://docs.soliditylang.org/en/v0.8.20/contracts.html#function-overriding), using the `override` keyword when the function solely overrides an interface function, and the function doesn't exist in multiple base contracts, is unnecessary.


*There are 102 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/ActivePool.sol

74:     function getSystemCollShares() external view override returns (uint256) {

82:     function getSystemDebt() external view override returns (uint256) {

89:     function getFeeRecipientClaimableCollShares() external view override returns (uint256) {

100:     function transferSystemCollShares(address _account, uint256 _shares) public override {

129:     function transferSystemCollSharesAndLiquidatorReward(
130:         address _account,
131:         uint256 _shares,
132:         uint256 _liquidatorRewardShares
133:     ) external override {

157:     function allocateSystemCollSharesToFeeRecipient(uint256 _shares) external override {

194:     function increaseSystemDebt(uint256 _amount) external override {

207:     function decreaseSystemDebt(uint256 _amount) external override {

242:     function increaseSystemCollShares(uint256 _value) external override {

261:     function flashLoan(
262:         IERC3156FlashBorrower receiver,
263:         address token,
264:         uint256 amount,
265:         bytes calldata data
266:     ) external override returns (bool) {

317:     function flashFee(address token, uint256 amount) public view override returns (uint256) {

328:     function maxFlashLoan(address token) public view override returns (uint256) {

346:     function claimFeeRecipientCollShares(uint256 _shares) external override requiresAuth {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L74-L74) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L82-L82), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L89-L89), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L100-L100), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L129-L133), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L157-L157), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L194-L194), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L207-L207), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L242-L242), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L261-L266), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L317-L317), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L328-L328), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L346-L346)


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

599:     function claimSurplusCollShares() external override {

608:     function getPositionManagerApproval(
609:         address _borrower,
610:         address _positionManager
611:     ) external view override returns (PositionManagerApproval) {

628:     function setPositionManagerApproval(
629:         address _positionManager,
630:         PositionManagerApproval _approval
631:     ) external override {

647:     function revokePositionManagerApproval(address _positionManager) external override {

653:     function renouncePositionManagerApproval(address _borrower) external override {

665:     function domainSeparator() public view override returns (bytes32) {

687:     function version() external pure override returns (string memory) {

693:     function permitTypeHash() external pure override returns (bytes32) {

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

1114:     function flashFee(address token, uint256 amount) public view override returns (uint256) {

1124:     function maxFlashLoan(address token) public view override returns (uint256) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L168-L173) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L187-L193), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L203-L208), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L219-L224), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L235-L240), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L250-L255), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L270-L277), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L300-L308), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L553-L553), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L599-L599), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L608-L611), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L628-L631), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L647-L647), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L653-L653), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L665-L665), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L687-L687), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L693-L693), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L706-L714), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L1077-L1082), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L1114-L1114), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L1124-L1124)


```solidity

File: packages/contracts/contracts/CdpManager.sol

66:     function getActiveCdpsCount() external view override returns (uint256) {

73:     function getIdFromCdpIdsArray(uint256 _index) external view override returns (bytes32) {

99:     function liquidate(bytes32 _cdpId) external override {

109:     function partiallyLiquidate(
110:         bytes32 _cdpId,
111:         uint256 _partialAmount,
112:         bytes32 _upperPartialHint,
113:         bytes32 _lowerPartialHint
114:     ) external override {

126:     function batchLiquidateCdps(bytes32[] memory _cdpArray) external override {

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

580:     function getCachedTCR(uint256 _price) external view override returns (uint256) {

589:     function checkRecoveryMode(uint256 _price) external view override returns (bool) {

638:     function getRedemptionRate() public view override returns (uint256) {

643:     function getRedemptionRateWithDecay() public view override returns (uint256) {

661:     function getRedemptionFeeWithDecay(
662:         uint256 _stETHToRedeem
663:     ) external view override returns (uint256) {

856:     function getCdpStatus(bytes32 _cdpId) external view override returns (uint256) {

863:     function getCdpStake(bytes32 _cdpId) external view override returns (uint256) {

871:     function getCdpDebt(bytes32 _cdpId) external view override returns (uint256) {

879:     function getCdpCollShares(bytes32 _cdpId) external view override returns (uint256) {

891:     function getCdpLiquidatorRewardShares(bytes32 _cdpId) external view override returns (uint256) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L66-L66) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L73-L73), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L99-L99), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L109-L114), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L126-L126), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L320-L328), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L514-L514), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L523-L523), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L538-L543), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L580-L580), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L589-L589), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L638-L638), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L643-L643), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L661-L663), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L856-L856), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L863-L863), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L871-L871), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L879-L879), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L891-L891)


```solidity

File: packages/contracts/contracts/CollSurplusPool.sol

61:     function getTotalSurplusCollShares() external view override returns (uint256) {

67:     function getSurplusCollShares(address _account) external view override returns (uint256) {

77:     function increaseSurplusCollShares(address _account, uint256 _amount) external override {

89:     function claimSurplusCollShares(address _account) external override {

130:     function increaseTotalSurplusCollShares(uint256 _value) external override {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L61-L61) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L67-L67), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L77-L77), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L89-L89), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L130-L130)


```solidity

File: packages/contracts/contracts/EBTCToken.sol

85:     function mint(address _account, uint256 _amount) external override {

95:     function burn(address _account, uint256 _amount) external override {

111:     function totalSupply() external view override returns (uint256) {

115:     function balanceOf(address account) external view override returns (uint256) {

119:     function transfer(address recipient, uint256 amount) external override returns (bool) {

125:     function allowance(address owner, address spender) external view override returns (uint256) {

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

182:     function domainSeparator() public view override returns (bytes32) {

199:     function permit(
200:         address owner,
201:         address spender,
202:         uint256 amount,
203:         uint256 deadline,
204:         uint8 v,
205:         bytes32 r,
206:         bytes32 s
207:     ) external override {

331:     function name() external pure override returns (string memory) {

337:     function symbol() external pure override returns (string memory) {

343:     function decimals() external pure override returns (uint8) {

349:     function version() external pure override returns (string memory) {

355:     function permitTypeHash() external pure override returns (bytes32) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L85-L85) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L95-L95), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L111-L111), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L115-L115), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L119-L119), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L125-L125), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L129-L129), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L134-L138), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L152-L155), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L160-L163), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L182-L182), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L199-L207), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L331-L331), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L337-L337), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L343-L343), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L349-L349), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L355-L355)


```solidity

File: packages/contracts/contracts/PriceFeed.sol

98:     function fetchPrice() external override returns (uint256) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L98-L98) 


```solidity

File: packages/contracts/contracts/SortedCdps.sol

123:     function getOwnerAddress(bytes32 cdpId) public pure override returns (address) {

130:     function nonExistId() public pure override returns (bytes32) {

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

410:     function remove(bytes32 _id) external override {

419:     function batchRemove(bytes32[] memory _ids) external override {

498:     function reInsert(
499:         bytes32 _id,
500:         uint256 _newNICR,
501:         bytes32 _prevId,
502:         bytes32 _nextId
503:     ) external override {

519:     function contains(bytes32 _id) public view override returns (bool) {

530:     function isFull() public view override returns (bool) {

536:     function isEmpty() public view override returns (bool) {

542:     function getSize() external view override returns (uint256) {

548:     function getMaxSize() external view override returns (uint256) {

554:     function getFirst() external view override returns (bytes32) {

560:     function getLast() external view override returns (bytes32) {

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

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L123-L123) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L130-L130), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L140-L143), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L155-L160), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L216-L216), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L227-L231), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L270-L270), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L286-L290), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L344-L349), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L410-L410), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L419-L419), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L498-L503), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L519-L519), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L530-L530), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L536-L536), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L542-L542), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L548-L548), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L554-L554), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L560-L560), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L567-L567), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L574-L574), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L583-L587), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L666-L670)


```solidity

File: packages/contracts/contracts/LeverageMacroDelegateTarget.sol

63:     function owner() public override returns (address) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L63-L63) 


```solidity

File: packages/contracts/contracts/LeverageMacroReference.sol

44:     function owner() public override returns (address) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroReference.sol#L44-L44) 


```solidity

File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

63:     function canCall(
64:         address user,
65:         address target,
66:         bytes4 functionSig
67:     ) public view virtual override returns (bool) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L63-L67) 


</details>


### [NC&#x2011;47] NatSpec `@param` is missing 



*There are 46 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

// @audit the @param _varMvTokens is missing

@notice Process the token movements required by a Cdp adjustment.
@notice Handles the cases of a debt increase / decrease, and/or a collateral increase / decrease.

// @audit the @param _account is missing
// @audit the @param _debt is missing

@dev Mint specified debt tokens to account and change global debt accounting accordingly


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L760-L1) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L790-L1)


```solidity

File: packages/contracts/contracts/CdpManager.sol

// @audit the @param _firstRedemptionHint is missing
// @audit the @param _price is missing

@notice Returns true if the CdpId specified is the lowest-ICR Cdp in the linked list that still has MCR > ICR
 @dev Returns false if the specified CdpId hint is blank
 @dev Returns false if the specified CdpId hint doesn't exist in the list
 @dev Returns false if the ICR of the specified CdpId is < MCR
 @dev Returns true if the specified CdpId is not blank, exists in the list, has an ICR > MCR, and the next lower Cdp in the list is either blank or has an ICR < MCR.


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L272-L1) 


```solidity

File: packages/contracts/contracts/CdpManagerStorage.sol

// @audit the @param _tcr is missing

@dev Internal notify called by Redemptions and Liquidations
 @dev Specified TCR is emitted for notification pruposes regardless of whether the Grace Period timestamp is set

// @audit the @param _tcr is missing

@notice Clear RM Grace Period timestamp if it has been set
 @notice No input validation, calling function must confirm that the system is not in recovery mode to be valid
 @dev Specified TCR is emitted for notification pruposes regardless of whether the Grace Period timestamp is set
 @dev Internal notify called by Redemptions and Liquidations

// @audit the @param systemCollShares is missing
// @audit the @param systemDebt is missing
// @audit the @param price is missing

@dev Set RM grace period based on specified system collShares, system debt, and price
 @dev Variant for internal use in redemptions and liquidations

// @audit the @param _cdpId is missing

@dev get the pending Cdp debt "reward" (i.e. the amount of extra debt assigned to the Cdp) from liquidation redistribution events, earned by their stake

// @audit the @param _cdpId is missing

@dev Sync Cdp debt redistribution index to global value

// @audit the @param _cdpId is missing

@dev Calculate the new collateral and debt values for a given CDP, based on pending state changes

// @audit the @param _price is missing

@notice Return the Individual Collateral Ratio (ICR) of the specified Cdp as "cached view" (maybe outdated).
 @param _cdpId The CdpId whose ICR to be queried
 @return The Individual Collateral Ratio (ICR) of the specified Cdp.
 @dev Use getSyncedICR() instead if pending fee split and debt redistribution should be considered

// @audit the @param _newIndex is missing
// @audit the @param _oldIndex is missing

@dev calculate pending global state change to be applied:
 @return split fee taken (if any) AND
 @return new split index per stake unit AND
 @return new split index error

// @audit the @param _cdpId is missing
// @audit the @param _cdpPerUnitIdx is missing
// @audit the @param _systemStEthFeePerUnitIndex is missing

@dev calculate pending state change to be applied for given CDP and global split index(typically already synced):
 @return new CDP collateral share after pending change applied
 @return new CDP debt after pending change applied
 @return split fee applied to given CDP
 @return redistributed debt applied to given CDP
 @return delta between debt redistribution index of given CDP and global tracking index

// @audit the @param _cdpId is missing

@return CDP debt and pending redistribution from liquidation applied


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L49-L1) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L63-L1), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L87-L1), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L304-L1), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L336-L1), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L344-L1), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L701-L1), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L761-L1), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L787-L1), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L822-L1)


```solidity

File: packages/contracts/contracts/SortedCdps.sol

// @audit the @param owner is missing

@notice a Pagination-flavor search for the count of Cdps owned by given owner
 @notice Starts from a given CdpId in the sorted list, and moves from lowest ICR to highest ICR
 @param startNodeId the count traversal will start at this given CDP instead of the tail of the list
 @param maxNodes the traversal will go through the list by this given maximum limit of number of Cdps
 @return count Number of active Cdps owned by the address in the segment of the list traversed
 @return last seen CDP for the startNode for next pagination

// @audit the @param owner is missing
// @audit the @param startNodeId is missing
// @audit the @param maxNodes is missing

@dev return the found CDP count owned by given owner with
 @dev current lastly-visited CDP as the startNode for next pagination

// @audit the @param owner is missing

@dev a pagination-flavor search retrieval of (from least ICR to biggest ICR) Cdps owned by given owner (starting at given CDP)
 @param startNodeId the traversal will start at this given CDP instead of the tail of the list
 @param maxNodes the traversal will go through the list by this given maximum limit of number of Cdps
 @return all CdpIds of the specified owner found by search starting at the specified startNodeId for the specified maximum iteration count
 @return found number of Cdp for the owner
 @return starting CdpId for next pagination within current SortedCdps

// @audit the @param owner is missing
// @audit the @param startNodeId is missing
// @audit the @param maxNodes is missing
// @audit the @param maxArraySize is missing

@dev return EITHER the found Cdps (also the count) owned by given owner OR empty array with
 @dev current lastly-visited CDP as the startNode for next pagination


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L227-L1) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L237-L1), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L286-L1), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L299-L1)


```solidity

File: packages/contracts/contracts/LeverageMacroBase.sol

// @audit the @param flType is missing
// @audit the @param borrowAmount is missing
// @audit the @param operation is missing
// @audit the @param postCheckType is missing
// @audit the @param checkParams is missing

@notice Entry point for the Macro

// @audit the @param token is missing
// @audit the @param amount is missing

@notice Transfer an arbitrary token back to you
 @dev If you delegatecall into this, this will transfer the tokens to the caller of the DiamondLike (and not the contract)

// @audit the @param check is missing
// @audit the @param valueToCheck is missing

@dev Assumes that
     >= you prob use this one
     <= if you don't need >= you go for lte
     And if you really need eq, it's third

// @audit the @param operation is missing

@dev Must be memory since we had to decode it

// @audit the @param data is missing

@notice Convenience function to parse bytes into LeverageMacroOperation data

// @audit the @param initiator is missing
// @audit the @param token is missing
// @audit the @param amount is missing
// @audit the @param fee is missing
// @audit the @param data is missing

@notice Proper Flashloan Callback handler

// @audit the @param swapData is missing

@dev Must be memory since we had to decode it

// @audit the @param swapData is missing

@dev Given a SwapOperation
     Approves the `addressForApprove` for the exact amount
     Calls `addressForSwap`
     Resets the approval of `addressForApprove`
     Performs validation via `_doSwapChecks`

// @audit the @param swapChecks is missing

@dev Given `SwapCheck` performs validation on the state of this contract
     A minOut Check

// @audit the @param addy is missing

@dev Prevents doing arbitrary calls to protected targets

// @audit the @param data is missing

@dev Must be memory since we had to decode it

// @audit the @param data is missing

@dev Must be memory since we had to decode it

// @audit the @param data is missing

@dev Must be memory since we had to decode it

// @audit the @param _target is missing
// @audit the @param _gas is missing
// @audit the @param _value is missing
// @audit the @param _maxCopy is missing
// @audit the @param _calldata is missing

@dev excessivelySafeCall to perform generic calls without getting gas bombed | useful if you don't care about return value
 @notice Credits to: https://github.com/nomad-xyz/ExcessivelySafeCall/blob/main/src/ExcessivelySafeCall.sol


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L118-L1) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L234-L1), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L244-L1), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L291-L1), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L338-L1), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L344-L1), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L382-L1), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L398-L1), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L435-L1), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L450-L1), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L460-L1), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L474-L1), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L482-L1), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L498-L1)


```solidity

File: packages/contracts/contracts/LeverageMacroFactory.sol

// @audit the @param _owner is missing

@notice Deploys a new macro for an owner, only they can operate the macro


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroFactory.sol#L43-L1) 


```solidity

File: packages/contracts/contracts/SimplifiedDiamondLike.sol

// @audit the @param sig is missing
// @audit the @param handler is missing

=== HARDCODED SETTERS === ///
 @notice Given a funsig and a implementation address
     Set the handler to the logic we will delegatecall to

// @audit the @param allowNonCallbacks is missing

@notice Do you want to allow any caller to call this contract?
     This is a VERY DANGEROUS setting
     Do not call this unless you know what you are doing

// @audit the @param ops is missing

@notice Execute a list of operations in sequence

// @audit the @param ds is missing
// @audit the @param _enabled is missing

@dev toggle callbackEnabledForCall in OurSetting

// @audit the @param op is missing

@dev Execute one tx


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L51-L1) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L66-L1), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L110-L1), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L129-L1), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L134-L1)


```solidity

File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

// @audit the @param newAuthority is missing

@notice Changed constructor to initialize to allow flexiblity of constructor vs initializer use
 @notice sets authorityInitiailzed flag to ensure only one use of


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L55-L1) 


```solidity

File: packages/contracts/contracts/Dependencies/EbtcBase.sol

// @audit the @param _icr is missing
// @audit the @param _tcr is missing

@dev return true if given ICR is qualified for liquidation compared to configured threshold
 @dev this function ONLY checks numbers not check grace period switch for Recovery Mode

// @audit the @param _icr is missing

@dev return true if given ICR is qualified for liquidation compared to MCR

// @audit the @param _icr is missing
// @audit the @param _tcr is missing

@dev return true if given ICR is qualified for liquidation compared to TCR
 @dev typically used in Recovery Mode


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L124-L1) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L134-L1), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L140-L1)


```solidity

File: packages/contracts/contracts/Dependencies/EbtcMath.sol

// @audit the @param _stEthBalance is missing
// @audit the @param _debt is missing
// @audit the @param _price is missing

@dev Compute collateralization ratio, given stETH balance, price, and debt balance


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcMath.sol#L104-L1) 


```solidity

File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

// @audit the @param user is missing
// @audit the @param target is missing
// @audit the @param functionSig is missing

@notice A user can call a given function signature on a given target address if:
- The capability has not been burned
- That capability is public, or the user has a role that has been granted the capability to call the function

// @audit the @param target is missing
// @audit the @param functionSig is missing
// @audit the @param enabled is missing

@notice Set a capability flag as public, meaning any account can call it. Or revoke this capability.
 @dev A capability cannot be made public if it has been burned.

// @audit the @param role is missing
// @audit the @param target is missing
// @audit the @param functionSig is missing
// @audit the @param enabled is missing

@notice Grant a specified role the ability to call a function on a target.
 @notice Has no effect

// @audit the @param target is missing
// @audit the @param functionSig is missing

@notice Permanently burns a capability for a target.


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L63-L1) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L85-L1), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L106-L1), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L133-L1)


</details>


### [NC&#x2011;48] Functions which are either private or internal should have a preceding _ in their name 
Add a preceding underscore to the function name, take care to refactor where there functions are called 


*There are 5 instances of this issue:*



<details>
<summary>see instances</summary>


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

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L498-L504) 


```solidity

File: packages/contracts/contracts/Dependencies/Auth.sol

18:     constructor(address _owner, Authority _authority) {

32:     function isAuthorized(address user, bytes4 functionSig) internal view virtual returns (bool) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/Auth.sol#L18-L18) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/Auth.sol#L32-L32)


```solidity

File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

30:     function isAuthorized(address user, bytes4 functionSig) internal view virtual returns (bool) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L30-L30) 


```solidity

File: packages/contracts/contracts/Dependencies/EbtcMath.sol

35:     function decMul(uint256 x, uint256 y) internal pure returns (uint256 decProd) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcMath.sol#L35-L35) 


</details>


### [NC&#x2011;49] Private and internal state variables should have a preceding _ in their name unless they are constants 
Add a preceding underscore to the state variable name, take care to refactor where there variables are read/wrote


*There are 11 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/ActivePool.sol

31:     uint256 internal systemCollShares; // deposited collateral tracker

32:     uint256 internal systemDebt;

33:     uint256 internal feeRecipientCollShares; // coll shares claimable by fee recipient


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L31-L31) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L32-L32), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L33-L33)


```solidity

File: packages/contracts/contracts/CollSurplusPool.sol

28:     uint256 internal totalSurplusCollShares;

30:     mapping(address => uint256) internal balances;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L28-L28) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L30-L30)


```solidity

File: packages/contracts/contracts/Governor.sol

17:     bytes32 NO_ROLES = bytes32(0);

30:     mapping(uint8 => string) internal roleNames;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L17-L17) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L30-L30)


```solidity

File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

26:     EnumerableSet.AddressSet internal users;

27:     EnumerableSet.AddressSet internal targets;

28:     mapping(address => EnumerableSet.Bytes32Set) internal enabledFunctionSigsByTarget;

30:     EnumerableSet.Bytes32Set internal enabledFunctionSigsPublic;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L26-L26) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L27-L27), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L28-L28), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L30-L30)


</details>


### [NC&#x2011;50] `public` functions not called by the contract should be declared `external` instead 
Contracts [are allowed](https://docs.soliditylang.org/en/latest/contracts.html#function-overriding) to override their parents' functions and change the visibility from `external` to `public`.


*There are 17 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/ActivePool.sol

371:     function sweepToken(address token, uint256 amount) public nonReentrant requiresAuth {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L371-L371) 


```solidity

File: packages/contracts/contracts/CdpManager.sol

570:     function getSystemDebt() public view returns (uint256 entireSystemDebt) {

717:     function getDeploymentStartTime() public view returns (uint256) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L570-L570) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L717-L717)


```solidity

File: packages/contracts/contracts/CdpManagerStorage.sol

701:     function getCachedICR(bytes32 _cdpId, uint256 _price) public view returns (uint256) {

719:     function getPendingRedistributedDebt(

728:     function hasPendingRedistributedDebt(bytes32 _cdpId) public view returns (bool) {

864:     function getSyncedICR(bytes32 _cdpId, uint256 _price) public view returns (uint256) {

874:     function getSyncedTCR(uint256 _price) public view returns (uint256) {

890:     function canLiquidateRecoveryMode(uint256 icr, uint256 tcr) public view returns (bool) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L701-L701) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L719-L719), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L728-L728), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L864-L864), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L874-L874), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L890-L890)


```solidity

File: packages/contracts/contracts/CollSurplusPool.sol

142:     function sweepToken(address token, uint256 amount) public nonReentrant requiresAuth {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L142-L142) 


```solidity

File: packages/contracts/contracts/Governor.sol

96:     function getRolesFromByteMap(bytes32 byteMap) public pure returns (uint8[] memory roleIds) {

120:     function getByteMapFromRoles(uint8[] memory roleIds) public pure returns (bytes32) {

131:     function getEnabledFunctionsInTarget(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L96-L96) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L120-L120), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L131-L131)


```solidity

File: packages/contracts/contracts/LeverageMacroBase.sol

234:     function sweepToken(address token, uint256 amount) public {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L234-L234) 


```solidity

File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

22:     function authority() public view returns (Authority) {

26:     function authorityInitialized() public view returns (bool) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L22-L22) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L26-L26)


```solidity

File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

50:     function isPublicCapability(address target, bytes4 functionSig) public view returns (bool) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L50-L50) 


</details>


### [NC&#x2011;51] Adding a `return` statement when the function defines a named return variable, is redundant 
Once the return variable has been assigned (or has its default value), there is no need to explicitly return it at the end of the function, since it's returned automatically.


*There are 15 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/CdpManager.sol

233:         return singleRedemption;

206:                 return singleRedemption;

562:         return index;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L233-L233) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L206-L206), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L562-L562)


```solidity

File: packages/contracts/contracts/LiquidationLibrary.sol

859:         return newTotals;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L859-L859) 


```solidity

File: packages/contracts/contracts/PriceFeed.sol

677:             return chainlinkResponse;

620:             return chainlinkResponse;

628:             return chainlinkResponse;

647:             return chainlinkResponse;

663:             return chainlinkResponse;

696:             return prevChainlinkResponse;

765:             return prevChainlinkResponse;

708:             return prevChainlinkResponse;

716:             return prevChainlinkResponse;

735:             return prevChainlinkResponse;

751:             return prevChainlinkResponse;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L677-L677) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L620-L620), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L628-L628), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L647-L647), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L663-L663), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L696-L696), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L765-L765), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L708-L708), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L716-L716), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L735-L735), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L751-L751)


</details>


### [NC&#x2011;52] `require()` / `revert()` statements should have descriptive reason strings 



*There are 14 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

40:         revert("Must be overridden");

452:         require(addy != address(borrowerOperations));

453:         require(addy != address(sortedCdps));

454:         require(addy != address(activePool));

455:         require(addy != address(cdpManager));

456:         require(addy != address(this)); // If it could call this it could fake the forwarded caller

255:             revert("Operator not found");


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L40-L40) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L452-L452), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L453-L453), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L454-L454), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L455-L455), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L456-L456), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L255-L255)


```solidity

File: packages/contracts/contracts/SimplifiedDiamondLike.sol

52:         require(msg.sender == owner);

56:         require(sig != 0x94b24d09);

67:         require(msg.sender == owner);

77:         require(msg.sender == address(this)); // Must call this via `execute` to explicitly set the flag

154:             require(success);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L52-L52) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L56-L56), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L67-L67), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L77-L77), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L154-L154)


```solidity

File: packages/contracts/contracts/Dependencies/Auth.sol

45:         require(msg.sender == owner || authority.canCall(msg.sender, address(this), msg.sig));


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/Auth.sol#L45-L45) 


```solidity

File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

41:         require(_authority.canCall(msg.sender, address(this), msg.sig));


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L41-L41) 


</details>


### [NC&#x2011;53] Setters should prevent re-setting of the same value 
This especially problematic when the setter also emits the same value, which may be confusing to offline parsers


*There are 14 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/ActivePool.sol

//@audit `feeRecipientAddress` and `_feeRecipientAddress` are never checked for the same value setting
390:     function setFeeRecipientAddress(address _feeRecipientAddress) external requiresAuth {
391:         ICdpManagerData(cdpManagerAddress).syncGlobalAccountingAndGracePeriod(); // Accrue State First
392: 
393:         require(
394:             _feeRecipientAddress != address(0),
395:             "ActivePool: Cannot set fee recipient to zero address"
396:         );
397: 
398:         feeRecipientAddress = _feeRecipientAddress;

//@audit `flashLoansPaused` and `_paused` are never checked for the same value setting
417:     function setFlashLoansPaused(bool _paused) external requiresAuth {
418:         ICdpManagerData(cdpManagerAddress).syncGlobalAccountingAndGracePeriod(); // Accrue State First
419: 
420:         flashLoansPaused = _paused;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L390-L398) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L417-L420)


```solidity

File: packages/contracts/contracts/BorrowerOperations.sol

//@audit `feeRecipientAddress` and `_feeRecipientAddress` are never checked for the same value setting
1140:     function setFeeRecipientAddress(address _feeRecipientAddress) external requiresAuth {
1141:         require(
1142:             _feeRecipientAddress != address(0),
1143:             "BorrowerOperations: Cannot set feeRecipient to zero address"
1144:         );
1145: 
1146:         cdpManager.syncGlobalAccounting();
1147: 
1148:         feeRecipientAddress = _feeRecipientAddress;

//@audit `flashLoansPaused` and `_paused` are never checked for the same value setting
1167:     function setFlashLoansPaused(bool _paused) external requiresAuth {
1168:         cdpManager.syncGlobalAccounting();
1169: 
1170:         flashLoansPaused = _paused;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L1140-L1148) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L1167-L1170)


```solidity

File: packages/contracts/contracts/CdpManager.sol

//@audit `stakingRewardSplit` and `_stakingRewardSplit` are never checked for the same value setting
773:     function setStakingRewardSplit(uint256 _stakingRewardSplit) external requiresAuth {
774:         require(
775:             _stakingRewardSplit <= MAX_REWARD_SPLIT,
776:             "CDPManager: new staking reward split exceeds max"
777:         );
778: 
779:         syncGlobalAccountingAndGracePeriod();
780: 
781:         stakingRewardSplit = _stakingRewardSplit;

//@audit `redemptionFeeFloor` and `_redemptionFeeFloor` are never checked for the same value setting
788:     function setRedemptionFeeFloor(uint256 _redemptionFeeFloor) external requiresAuth {
789:         require(
790:             _redemptionFeeFloor >= MIN_REDEMPTION_FEE_FLOOR,
791:             "CDPManager: new redemption fee floor is lower than minimum"
792:         );
793:         require(
794:             _redemptionFeeFloor <= DECIMAL_PRECISION,
795:             "CDPManager: new redemption fee floor is higher than maximum"
796:         );
797: 
798:         syncGlobalAccountingAndGracePeriod();
799: 
800:         redemptionFeeFloor = _redemptionFeeFloor;

//@audit `minuteDecayFactor` and `_minuteDecayFactor` are never checked for the same value setting
807:     function setMinuteDecayFactor(uint256 _minuteDecayFactor) external requiresAuth {
808:         require(
809:             _minuteDecayFactor >= MIN_MINUTE_DECAY_FACTOR,
810:             "CDPManager: new minute decay factor out of range"
811:         );
812:         require(
813:             _minuteDecayFactor <= MAX_MINUTE_DECAY_FACTOR,
814:             "CDPManager: new minute decay factor out of range"
815:         );
816: 
817:         syncGlobalAccountingAndGracePeriod();
818: 
819:         // decay first according to previous factor
820:         _decayBaseRate();
821: 
822:         // set new factor after decaying
823:         minuteDecayFactor = _minuteDecayFactor;

//@audit `beta` and `_beta` are never checked for the same value setting
830:     function setBeta(uint256 _beta) external requiresAuth {
831:         syncGlobalAccountingAndGracePeriod();
832: 
833:         _decayBaseRate();
834: 
835:         beta = _beta;

//@audit `redemptionsPaused` and `_paused` are never checked for the same value setting
843:     function setRedemptionsPaused(bool _paused) external requiresAuth {
844:         syncGlobalAccountingAndGracePeriod();
845:         _decayBaseRate();
846: 
847:         redemptionsPaused = _paused;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L773-L781) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L788-L800), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L807-L823), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L830-L835), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L843-L847)


```solidity

File: packages/contracts/contracts/CdpManagerStorage.sol

//@audit `recoveryModeGracePeriodDuration` and `_gracePeriod` are never checked for the same value setting
111:     function setGracePeriod(uint128 _gracePeriod) external requiresAuth {
112:         require(
113:             _gracePeriod >= MINIMUM_GRACE_PERIOD,
114:             "CdpManager: Grace period below minimum duration"
115:         );
116: 
117:         syncGlobalAccountingAndGracePeriod();
118:         recoveryModeGracePeriodDuration = _gracePeriod;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L111-L118) 


```solidity

File: packages/contracts/contracts/PriceFeed.sol

//@audit `fallbackCaller` and `newFallbackCaler` are never checked for the same value setting
358:     function setFallbackCaller(address _fallbackCaller) external requiresAuth {
359:         // health check-up before officially set it up
360:         IFallbackCaller newFallbackCaler = IFallbackCaller(_fallbackCaller);
361:         FallbackResponse memory fallbackResponse;
362: 
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

//@audit `fallbackCaller` and `newFallbackCaler` are never checked for the same value setting
358:     function setFallbackCaller(address _fallbackCaller) external requiresAuth {
359:         // health check-up before officially set it up
360:         IFallbackCaller newFallbackCaler = IFallbackCaller(_fallbackCaller);
361:         FallbackResponse memory fallbackResponse;
362: 
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

//@audit `status` and `_status` are never checked for the same value setting
546:     function _changeStatus(Status _status) internal {
547:         status = _status;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L358-L386) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L358-L377), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L546-L547)


```solidity

File: packages/contracts/contracts/Dependencies/Auth.sol

//@audit `authority` and `newAuthority` are never checked for the same value setting
42:     function setAuthority(Authority newAuthority) public virtual {
43:         // We check if the caller is the owner first because we want to ensure they can
44:         // always swap out the authority even if it's reverting or using up a lot of gas.
45:         require(msg.sender == owner || authority.canCall(msg.sender, address(this), msg.sig));
46: 
47:         authority = newAuthority;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/Auth.sol#L42-L47) 


</details>


### [NC&#x2011;54] NatSpec `@return` argument is missing 



*There are 23 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/CdpManager.sol

// @audit the @return is missing
@notice Returns true if the CdpId specified is the lowest-ICR Cdp in the linked list that still has MCR > ICR
 @dev Returns false if the specified CdpId hint is blank
 @dev Returns false if the specified CdpId hint doesn't exist in the list
 @dev Returns false if the ICR of the specified CdpId is < MCR
 @dev Returns true if the specified CdpId is not blank, exists in the list, has an ICR > MCR, and the next lower Cdp in the list is either blank or has an ICR < MCR.

// @audit the @return is missing
@notice Update stake for the specified Cdp and total stake within the system.
 @dev Only BorrowerOperations is allowed to call this function
 @param _cdpId cdpId to update stake for


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L272-L1) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L523-L1)


```solidity

File: packages/contracts/contracts/CdpManagerStorage.sol

// @audit the @return is missing
@dev get the pending Cdp debt "reward" (i.e. the amount of extra debt assigned to the Cdp) from liquidation redistribution events, earned by their stake

// @audit the @return is missing
@dev Check if enough time has passed for grace period after enabled


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L304-L1) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L895-L1)


```solidity

File: packages/contracts/contracts/EBTCToken.sol

// @audit the @return is missing
@dev Return current nonce for specified owner fOR EIP-2612 compatibility
 @param owner The address whose nonce to be queried


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L225-L1) 


```solidity

File: packages/contracts/contracts/PriceFeed.sol

// @audit the @return is missing
@notice Returns the latest price obtained from the Oracle
 @dev Called by eBTC functions that require a current price. Also callable permissionlessly.
 @dev Non-view function - it updates and stores the last good price seen by eBTC.
 @dev Uses a main oracle (Chainlink) and a fallback oracle in case Chainlink fails. If both fail, it uses the last good price seen by eBTC.
 @dev The fallback oracle address can be swapped by the Authority. The fallback oracle must conform to the IFallbackCaller interface.


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L98-L1) 


```solidity

File: packages/contracts/contracts/SortedCdps.sol

// @audit the @return is missing
@dev return the found CDP count owned by given owner with
 @dev current lastly-visited CDP as the startNode for next pagination

// @audit the @return is missing
@dev return EITHER the found Cdps (also the count) owned by given owner OR empty array with
 @dev current lastly-visited CDP as the startNode for next pagination


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L237-L1) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L299-L1)


```solidity

File: packages/contracts/contracts/LeverageMacroBase.sol

// @audit the @return is missing
@notice Convenience function to parse bytes into LeverageMacroOperation data

// @audit the @return is missing
@notice Proper Flashloan Callback handler

// @audit the @return is missing
@dev excessivelySafeCall to perform generic calls without getting gas bombed | useful if you don't care about return value
 @notice Credits to: https://github.com/nomad-xyz/ExcessivelySafeCall/blob/main/src/ExcessivelySafeCall.sol


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L338-L1) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L344-L1), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L498-L1)


```solidity

File: packages/contracts/contracts/LeverageMacroDelegateTarget.sol

// @audit the @return is missing
@dev Call self, since this is called via delegate call, and get owner


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L63-L1) 


```solidity

File: packages/contracts/contracts/LeverageMacroFactory.sol

// @audit the @return is missing
@notice Deploys a new macro for you

// @audit the @return is missing
@notice Deploys a new macro for an owner, only they can operate the macro


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroFactory.sol#L38-L1) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroFactory.sol#L43-L1)


```solidity

File: packages/contracts/contracts/SimplifiedDiamondLike.sol

// @audit the @return is missing
=== DIAMOND LIKE STORAGE === ///
 @dev Get pointer to storage


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L83-L1) 


```solidity

File: packages/contracts/contracts/Dependencies/EbtcBase.sol

// @audit the @return is missing
@notice Get the entire system collateral
 @notice Entire system collateral = collateral allocated to system in ActivePool, using it's internal accounting
 @dev Collateral tokens stored in ActivePool for liquidator rewards, fees, or coll in CollSurplusPool, are not included

// @audit the @return is missing
@notice Get the entire system debt
@notice Entire system collateral = collateral stored in ActivePool, using their internal accounting

// @audit the @return is missing
@dev return true if given ICR is qualified for liquidation compared to configured threshold
 @dev this function ONLY checks numbers not check grace period switch for Recovery Mode

// @audit the @return is missing
@dev return true if given ICR is qualified for liquidation compared to MCR

// @audit the @return is missing
@dev return true if given ICR is qualified for liquidation compared to TCR
 @dev typically used in Recovery Mode


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L67-L1) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L75-L1), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L124-L1), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L134-L1), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L140-L1)


```solidity

File: packages/contracts/contracts/Dependencies/EbtcMath.sol

// @audit the @return is missing
@dev Compute collateralization ratio, given stETH balance, price, and debt balance


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcMath.sol#L104-L1) 


```solidity

File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

// @audit the @return is missing
@notice A user can call a given function signature on a given target address if:
- The capability has not been burned
- That capability is public, or the user has a role that has been granted the capability to call the function


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L63-L1) 


```solidity

File: packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol

// @audit the @return is missing
@dev Initiate a flash loan.
 @param receiver The receiver of the tokens in the loan, and the receiver of the callback.
 @param token The loan currency.
 @param amount The amount of tokens lent.
 @param data Arbitrary data structure, intended to contain user-defined parameters.


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol#L28-L1) 


</details>


### [NC&#x2011;55] Polymorphic functions make security audits more time-consuming and error-prone 
The instances below point to one of two functions with the same name. Consider naming each function differently, in order to make code navigation and analysis easier.


*There are 3 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/EBTCToken.sol

104:     function burn(uint256 _amount) external {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L104-L104) 


```solidity

File: packages/contracts/contracts/LeverageMacroDelegateTarget.sol

63:     function owner() public override returns (address) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L63-L63) 


```solidity

File: packages/contracts/contracts/LeverageMacroFactory.sol

43:     function deployNewMacro(address _owner) public returns (address) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroFactory.sol#L43-L43) 


</details>


### [NC&#x2011;56] Large multiples of ten should use scientific notation (e.g. `1e6`) rather than decimal literals (e.g. `1000000`), for readability 
While the compiler knows to optimize away the exponentiation, it's still better coding practice to use idioms that do not require compiler optimization, if they exist


*There are 5 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

//@audit `1000`
141:     uint256 public constant MIN_REDEMPTION_FEE_FLOOR = (DECIMAL_PRECISION * 5) / 1000; // 0.5%


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L141-L141) 


```solidity

File: packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol

//@audit `10_000`
9:     uint256 public constant MAX_BPS = 10_000;

//@audit `1_000`
10:     uint256 public constant MAX_FEE_BPS = 1_000; // 10%


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L9-L9) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L10-L10)


```solidity

File: packages/contracts/contracts/Dependencies/EbtcBase.sol

//@audit `1100000000000000000`
22:     uint256 public constant MCR = 1100000000000000000; // 110%

//@audit `10_000`
39:     uint256 public constant MAX_REWARD_SPLIT = 10_000;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L22-L22) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L39-L39)


</details>


### [NC&#x2011;57] Consider moving `msg.sender` checks to a common authorization `modifier` 



*There are 18 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/ActivePool.sol

221:             msg.sender == borrowerOperationsAddress,

236:         require(msg.sender == cdpManagerAddress, "ActivePool: Caller is not CdpManager");

278:             receiver.onFlashLoan(msg.sender, token, amount, fee, data) == FLASH_SUCCESS_VALUE,


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L221-L221) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L236-L236), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L278-L278)


```solidity

File: packages/contracts/contracts/BorrowerOperations.sol

1092:             receiver.onFlashLoan(msg.sender, token, amount, fee, data) == FLASH_SUCCESS_VALUE,


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L1092-L1092) 


```solidity

File: packages/contracts/contracts/CdpManagerStorage.sol

661:             msg.sender == borrowerOperationsAddress,


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L661-L661) 


```solidity

File: packages/contracts/contracts/CollSurplusPool.sol

114:             msg.sender == borrowerOperationsAddress,

120:         require(msg.sender == cdpManagerAddress, "CollSurplusPool: Caller is not CdpManager");

124:         require(msg.sender == activePoolAddress, "CollSurplusPool: Caller is not Active Pool");


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L114-L114) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L120-L120), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L124-L124)


```solidity

File: packages/contracts/contracts/EBTCToken.sol

308:             msg.sender == borrowerOperationsAddress,

324:         require(msg.sender == cdpManagerAddress, "EBTC: Caller is not CdpManager");


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L308-L308) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L324-L324)


```solidity

File: packages/contracts/contracts/SortedCdps.sol

715:         require(msg.sender == address(cdpManager), "SortedCdps: Caller is not the CdpManager");


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L715-L715) 


```solidity

File: packages/contracts/contracts/LeverageMacroBase.sol

45:         require(owner() == msg.sender, "Must be owner");

363:                 msg.sender == address(activePool),

357:                 msg.sender == address(borrowerOperations),


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L45-L45) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L363-L363), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L357-L357)


```solidity

File: packages/contracts/contracts/SimplifiedDiamondLike.sol

52:         require(msg.sender == owner);

67:         require(msg.sender == owner);

77:         require(msg.sender == address(this)); // Must call this via `execute` to explicitly set the flag

111:         require(msg.sender == owner, "Must be owner");


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L52-L52) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L67-L67), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L77-L77), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L111-L111)


</details>


### [NC&#x2011;58] Empty `receive()`/`payable fallback()` function does not authorize requests 
If the intention is for the Ether to be used, the function should call another function, otherwise it should revert (e.g. `require(msg.sender == address(weth))`). Having no access control on the function means that someone may send Ether to the contract, and have no way to get anything back out, which is a loss of funds. If the concern is having to spend a small amount of gas to check the sender against an immutable address, the code should at least have a function to rescue unused Ether.


*There are 1 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

160:     receive() external payable {
161:         // PHP is my favourite language
162:     }


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L160-L162) 


</details>


### [NC&#x2011;59] State variables should have `Natspec` comments 
Consider adding some `Natspec` comments on critical state variables to explain what they are supposed to do: this will help for future code reviews.


*There are 155 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/ActivePool.sol

//@audit NAME need comments
24:     string public constant NAME = "ActivePool";

//@audit borrowerOperationsAddress need comments
26:     address public immutable borrowerOperationsAddress;

//@audit cdpManagerAddress need comments
27:     address public immutable cdpManagerAddress;

//@audit collSurplusPoolAddress need comments
28:     address public immutable collSurplusPoolAddress;

//@audit feeRecipientAddress need comments
29:     address public feeRecipientAddress;

//@audit systemCollShares need comments
31:     uint256 internal systemCollShares; // deposited collateral tracker

//@audit systemDebt need comments
32:     uint256 internal systemDebt;

//@audit feeRecipientCollShares need comments
33:     uint256 internal feeRecipientCollShares; // coll shares claimable by fee recipient

//@audit collateral need comments
34:     ICollateralToken public immutable collateral;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L24-L24) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L26-L26), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L27-L27), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L28-L28), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L29-L29), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L31-L31), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L32-L32), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L33-L33), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L34-L34)


```solidity

File: packages/contracts/contracts/BorrowerOperations.sol

//@audit NAME need comments
29:     string public constant NAME = "BorrowerOperations";

//@audit _PERMIT_POSITION_MANAGER_TYPEHASH need comments
32:     bytes32 private constant _PERMIT_POSITION_MANAGER_TYPEHASH =

//@audit _TYPE_HASH need comments
38:     bytes32 private constant _TYPE_HASH =

//@audit _VERSION need comments
41:     string internal constant _VERSION = "1";

//@audit _CACHED_DOMAIN_SEPARATOR need comments
45:     bytes32 private immutable _CACHED_DOMAIN_SEPARATOR;

//@audit _CACHED_CHAIN_ID need comments
46:     uint256 private immutable _CACHED_CHAIN_ID;

//@audit _HASHED_NAME need comments
48:     bytes32 private immutable _HASHED_NAME;

//@audit _HASHED_VERSION need comments
49:     bytes32 private immutable _HASHED_VERSION;

//@audit cdpManager need comments
53:     ICdpManager public immutable cdpManager;

//@audit collSurplusPool need comments
55:     ICollSurplusPool public immutable collSurplusPool;

//@audit feeRecipientAddress need comments
57:     address public feeRecipientAddress;

//@audit ebtcToken need comments
59:     IEBTCToken public immutable ebtcToken;

//@audit sortedCdps need comments
62:     ISortedCdps public immutable sortedCdps;

//@audit positionManagers need comments
65:     mapping(address => mapping(address => PositionManagerApproval)) public positionManagers;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L29-L29) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L32-L32), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L38-L38), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L41-L41), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L45-L45), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L46-L46), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L48-L48), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L49-L49), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L53-L53), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L55-L55), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L57-L57), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L59-L59), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L62-L62), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L65-L65)


```solidity

File: packages/contracts/contracts/CdpManagerStorage.sol

//@audit UNSET_TIMESTAMP need comments
21:     uint128 public constant UNSET_TIMESTAMP = type(uint128).max;

//@audit MINIMUM_GRACE_PERIOD need comments
22:     uint128 public constant MINIMUM_GRACE_PERIOD = 15 minutes;

//@audit lastGracePeriodStartTimestamp need comments
24:     uint128 public lastGracePeriodStartTimestamp = UNSET_TIMESTAMP; // use max to signify

//@audit recoveryModeGracePeriodDuration need comments
25:     uint128 public recoveryModeGracePeriodDuration = MINIMUM_GRACE_PERIOD;

//@audit NAME need comments
122:     string public constant NAME = "CdpManager";

//@audit borrowerOperationsAddress need comments
126:     address public immutable borrowerOperationsAddress;

//@audit collSurplusPool need comments
128:     ICollSurplusPool immutable collSurplusPool;

//@audit ebtcToken need comments
130:     IEBTCToken public immutable override ebtcToken;

//@audit liquidationLibrary need comments
132:     address public immutable liquidationLibrary;

//@audit sortedCdps need comments
135:     ISortedCdps public immutable sortedCdps;

//@audit SECONDS_IN_ONE_MINUTE need comments
139:     uint256 public constant SECONDS_IN_ONE_MINUTE = 60;

//@audit MIN_REDEMPTION_FEE_FLOOR need comments
141:     uint256 public constant MIN_REDEMPTION_FEE_FLOOR = (DECIMAL_PRECISION * 5) / 1000; // 0.5%

//@audit redemptionFeeFloor need comments
142:     uint256 public redemptionFeeFloor = MIN_REDEMPTION_FEE_FLOOR;

//@audit redemptionsPaused need comments
143:     bool public redemptionsPaused;

//@audit minuteDecayFactor need comments
148:     uint256 public minuteDecayFactor = 999037758833783000;

//@audit MIN_MINUTE_DECAY_FACTOR need comments
149:     uint256 public constant MIN_MINUTE_DECAY_FACTOR = 1; // Non-zero

//@audit MAX_MINUTE_DECAY_FACTOR need comments
150:     uint256 public constant MAX_MINUTE_DECAY_FACTOR = 999999999999999999; // Corresponds to a very fast decay rate, but not too extreme

//@audit deploymentStartTime need comments
152:     uint256 internal immutable deploymentStartTime;

//@audit beta need comments
159:     uint256 public beta = 2;

//@audit baseRate need comments
161:     uint256 public baseRate;

//@audit stakingRewardSplit need comments
163:     uint256 public stakingRewardSplit;

//@audit lastRedemptionTimestamp need comments
166:     uint256 public lastRedemptionTimestamp;

//@audit Cdps need comments
168:     mapping(bytes32 => Cdp) public Cdps;

//@audit totalStakes need comments
170:     uint256 public override totalStakes;

//@audit totalStakesSnapshot need comments
173:     uint256 public totalStakesSnapshot;

//@audit totalCollateralSnapshot need comments
176:     uint256 public totalCollateralSnapshot;

//@audit systemDebtRedistributionIndex need comments
187:     uint256 public systemDebtRedistributionIndex;

//@audit cdpDebtRedistributionIndex need comments
190:     mapping(bytes32 => uint256) public cdpDebtRedistributionIndex;

//@audit lastEBTCDebtErrorRedistribution need comments
193:     uint256 public lastEBTCDebtErrorRedistribution;

//@audit stEthIndex need comments
196:     uint256 public override stEthIndex;

//@audit systemStEthFeePerUnitIndex need comments
198:     uint256 public override systemStEthFeePerUnitIndex;

//@audit systemStEthFeePerUnitIndexError need comments
200:     uint256 public override systemStEthFeePerUnitIndexError;

//@audit cdpStEthFeePerUnitIndex need comments
202:     mapping(bytes32 => uint256) public cdpStEthFeePerUnitIndex;

//@audit CdpIds need comments
205:     bytes32[] public CdpIds;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L21-L21) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L22-L22), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L24-L24), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L25-L25), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L122-L122), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L126-L126), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L128-L128), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L130-L130), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L132-L132), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L135-L135), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L139-L139), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L141-L141), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L142-L142), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L143-L143), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L148-L148), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L149-L149), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L150-L150), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L152-L152), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L159-L159), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L161-L161), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L163-L163), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L166-L166), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L168-L168), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L170-L170), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L173-L173), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L176-L176), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L187-L187), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L190-L190), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L193-L193), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L196-L196), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L198-L198), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L200-L200), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L202-L202), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L205-L205)


```solidity

File: packages/contracts/contracts/CollSurplusPool.sol

//@audit NAME need comments
19:     string public constant NAME = "CollSurplusPool";

//@audit borrowerOperationsAddress need comments
21:     address public immutable borrowerOperationsAddress;

//@audit cdpManagerAddress need comments
22:     address public immutable cdpManagerAddress;

//@audit activePoolAddress need comments
23:     address public immutable activePoolAddress;

//@audit feeRecipientAddress need comments
24:     address public immutable feeRecipientAddress;

//@audit collateral need comments
25:     ICollateralToken public immutable collateral;

//@audit totalSurplusCollShares need comments
28:     uint256 internal totalSurplusCollShares;

//@audit balances need comments
30:     mapping(address => uint256) internal balances;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L19-L19) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L21-L21), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L22-L22), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L23-L23), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L24-L24), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L25-L25), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L28-L28), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L30-L30)


```solidity

File: packages/contracts/contracts/EBTCToken.sol

//@audit _totalSupply need comments
27:     uint256 private _totalSupply;

//@audit _NAME need comments
28:     string internal constant _NAME = "EBTC Stablecoin";

//@audit _SYMBOL need comments
29:     string internal constant _SYMBOL = "EBTC";

//@audit _VERSION need comments
30:     string internal constant _VERSION = "1";

//@audit _DECIMALS need comments
31:     uint8 internal constant _DECIMALS = 18;

//@audit _PERMIT_TYPEHASH need comments
36:     bytes32 private constant _PERMIT_TYPEHASH =

//@audit _TYPE_HASH need comments
39:     bytes32 private constant _TYPE_HASH =

//@audit _CACHED_DOMAIN_SEPARATOR need comments
44:     bytes32 private immutable _CACHED_DOMAIN_SEPARATOR;

//@audit _CACHED_CHAIN_ID need comments
45:     uint256 private immutable _CACHED_CHAIN_ID;

//@audit _HASHED_NAME need comments
47:     bytes32 private immutable _HASHED_NAME;

//@audit _HASHED_VERSION need comments
48:     bytes32 private immutable _HASHED_VERSION;

//@audit _balances need comments
51:     mapping(address => uint256) private _balances;

//@audit _allowances need comments
52:     mapping(address => mapping(address => uint256)) private _allowances;

//@audit cdpManagerAddress need comments
55:     address public immutable cdpManagerAddress;

//@audit borrowerOperationsAddress need comments
56:     address public immutable borrowerOperationsAddress;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L27-L27) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L28-L28), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L29-L29), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L30-L30), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L31-L31), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L36-L36), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L39-L39), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L44-L44), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L45-L45), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L47-L47), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L48-L48), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L51-L51), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L52-L52), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L55-L55), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L56-L56)


```solidity

File: packages/contracts/contracts/Governor.sol

//@audit NO_ROLES need comments
17:     bytes32 NO_ROLES = bytes32(0);

//@audit roleNames need comments
30:     mapping(uint8 => string) internal roleNames;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L17-L17) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L30-L30)


```solidity

File: packages/contracts/contracts/PriceFeed.sol

//@audit NAME need comments
22:     string public constant NAME = "PriceFeed";

//@audit ETH_BTC_CL_FEED need comments
25:     AggregatorV3Interface public immutable ETH_BTC_CL_FEED;

//@audit STETH_ETH_CL_FEED need comments
26:     AggregatorV3Interface public immutable STETH_ETH_CL_FEED;

//@audit fallbackCaller need comments
29:     IFallbackCaller public fallbackCaller; // Wrapper contract that calls the fallback system

//@audit TIMEOUT_ETH_BTC_FEED need comments
32:     uint256 public constant TIMEOUT_ETH_BTC_FEED = 4800; // 1 hours & 20min: 60 * 80

//@audit TIMEOUT_STETH_ETH_FEED need comments
33:     uint256 public constant TIMEOUT_STETH_ETH_FEED = 90000; // 25 hours: 60 * 60 * 25

//@audit MAX_PRICE_DEVIATION_FROM_PREVIOUS_ROUND need comments
36:     uint256 public constant MAX_PRICE_DEVIATION_FROM_PREVIOUS_ROUND = 5e17; // 50%

//@audit MAX_PRICE_DIFFERENCE_BETWEEN_ORACLES need comments
42:     uint256 public constant MAX_PRICE_DIFFERENCE_BETWEEN_ORACLES = 5e16; // 5%

//@audit lastGoodPrice need comments
45:     uint256 public lastGoodPrice;

//@audit status need comments
48:     Status public status;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L22-L22) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L25-L25), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L26-L26), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L29-L29), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L32-L32), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L33-L33), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L36-L36), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L42-L42), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L45-L45), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L48-L48)


```solidity

File: packages/contracts/contracts/SortedCdps.sol

//@audit NAME need comments
52:     string public constant NAME = "SortedCdps";

//@audit borrowerOperationsAddress need comments
54:     address public immutable borrowerOperationsAddress;

//@audit cdpManager need comments
56:     ICdpManager public immutable cdpManager;

//@audit maxSize need comments
58:     uint256 public immutable maxSize;

//@audit ADDRESS_SHIFT need comments
60:     uint256 constant ADDRESS_SHIFT = 96; // 8 * 12; Puts the address at leftmost bytes32 position

//@audit BLOCK_SHIFT need comments
61:     uint256 constant BLOCK_SHIFT = 64; // 8 * 8; Puts the block value after the address

//@audit data need comments
77:     Data public data;

//@audit nextCdpNonce need comments
79:     uint256 public nextCdpNonce;

//@audit dummyId need comments
80:     bytes32 public constant dummyId =


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L52-L52) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L54-L54), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L56-L56), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L58-L58), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L60-L60), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L61-L61), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L77-L77), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L79-L79), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L80-L80)


```solidity

File: packages/contracts/contracts/HintHelpers.sol

//@audit NAME need comments
12:     string public constant NAME = "HintHelpers";

//@audit sortedCdps need comments
14:     ISortedCdps public immutable sortedCdps;

//@audit cdpManager need comments
15:     ICdpManager public immutable cdpManager;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L12-L12) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L14-L14), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L15-L15)


```solidity

File: packages/contracts/contracts/LeverageMacroBase.sol

//@audit borrowerOperations need comments
29:     IBorrowerOperations public immutable borrowerOperations;

//@audit activePool need comments
30:     IActivePool public immutable activePool;

//@audit cdpManager need comments
31:     ICdpCdps public immutable cdpManager;

//@audit ebtcToken need comments
32:     IEBTCToken public immutable ebtcToken;

//@audit sortedCdps need comments
33:     ISortedCdps public immutable sortedCdps;

//@audit stETH need comments
34:     ICollateralToken public immutable stETH;

//@audit willSweep need comments
35:     bool internal immutable willSweep;

//@audit FLASH_LOAN_SUCCESS need comments
37:     bytes32 constant FLASH_LOAN_SUCCESS = keccak256("ERC3156FlashBorrower.onFlashLoan");


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L29-L29) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L30-L30), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L31-L31), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L32-L32), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L33-L33), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L34-L34), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L35-L35), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L37-L37)


```solidity

File: packages/contracts/contracts/LeverageMacroFactory.sol

//@audit borrowerOperations need comments
12:     address public immutable borrowerOperations;

//@audit activePool need comments
13:     address public immutable activePool;

//@audit cdpManager need comments
14:     address public immutable cdpManager;

//@audit ebtcToken need comments
15:     address public immutable ebtcToken;

//@audit stETH need comments
16:     address public immutable stETH;

//@audit sortedCdps need comments
17:     address public immutable sortedCdps;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroFactory.sol#L12-L12) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroFactory.sol#L13-L13), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroFactory.sol#L14-L14), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroFactory.sol#L15-L15), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroFactory.sol#L16-L16), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroFactory.sol#L17-L17)


```solidity

File: packages/contracts/contracts/LeverageMacroReference.sol

//@audit theOwner need comments
12:     address internal immutable theOwner;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroReference.sol#L12-L12) 


```solidity

File: packages/contracts/contracts/SimplifiedDiamondLike.sol

//@audit DIAMOND_STORAGE_POSITION need comments
39:     bytes32 constant DIAMOND_STORAGE_POSITION = keccak256("diamond.standard.diamond.storage");

//@audit owner need comments
42:     address public immutable owner;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L39-L39) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L42-L42)


```solidity

File: packages/contracts/contracts/Dependencies/Auth.sol

//@audit owner need comments
14:     address public owner;

//@audit authority need comments
16:     Authority public authority;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/Auth.sol#L14-L14) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/Auth.sol#L16-L16)


```solidity

File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

//@audit _authority need comments
13:     Authority private _authority;

//@audit _authorityInitialized need comments
14:     bool private _authorityInitialized;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L13-L13) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L14-L14)


```solidity

File: packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol

//@audit MAX_BPS need comments
9:     uint256 public constant MAX_BPS = 10_000;

//@audit MAX_FEE_BPS need comments
10:     uint256 public constant MAX_FEE_BPS = 1_000; // 10%

//@audit FLASH_SUCCESS_VALUE need comments
11:     bytes32 public constant FLASH_SUCCESS_VALUE = keccak256("ERC3156FlashBorrower.onFlashLoan");

//@audit feeBps need comments
14:     uint16 public feeBps = 3; // may be subject to future adjustments through protocol governance

//@audit flashLoansPaused need comments
15:     bool public flashLoansPaused;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L9-L9) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L10-L10), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L11-L11), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L14-L14), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L15-L15)


```solidity

File: packages/contracts/contracts/Dependencies/EbtcBase.sol

//@audit LICR need comments
19:     uint256 public constant LICR = 1030000000000000000; // 103%

//@audit MCR need comments
22:     uint256 public constant MCR = 1100000000000000000; // 110%

//@audit CCR need comments
25:     uint256 public constant CCR = 1250000000000000000; // 125%

//@audit LIQUIDATOR_REWARD need comments
28:     uint256 public constant LIQUIDATOR_REWARD = 2e17;

//@audit MIN_NET_STETH_BALANCE need comments
31:     uint256 public constant MIN_NET_STETH_BALANCE = 2e18;

//@audit PERCENT_DIVISOR need comments
33:     uint256 public constant PERCENT_DIVISOR = 200; // dividing by 200 yields 0.5%

//@audit BORROWING_FEE_FLOOR need comments
35:     uint256 public constant BORROWING_FEE_FLOOR = 0; // 0.5%

//@audit STAKING_REWARD_SPLIT need comments
37:     uint256 public constant STAKING_REWARD_SPLIT = 5_000; // taking 50% cut from staking reward

//@audit MAX_REWARD_SPLIT need comments
39:     uint256 public constant MAX_REWARD_SPLIT = 10_000;

//@audit activePool need comments
41:     IActivePool public immutable activePool;

//@audit priceFeed need comments
43:     IPriceFeed public immutable override priceFeed;

//@audit collateral need comments
46:     ICollateralToken public immutable collateral;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L19-L19) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L22-L22), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L25-L25), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L28-L28), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L31-L31), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L33-L33), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L35-L35), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L37-L37), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L39-L39), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L41-L41), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L43-L43), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L46-L46)


```solidity

File: packages/contracts/contracts/Dependencies/EbtcMath.sol

//@audit DECIMAL_PRECISION need comments
6:     uint256 internal constant DECIMAL_PRECISION = 1e18;

//@audit MAX_TCR need comments
7:     uint256 public constant MAX_TCR = type(uint256).max;

//@audit NICR_PRECISION need comments
18:     uint256 internal constant NICR_PRECISION = 1e20;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcMath.sol#L6-L6) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcMath.sol#L7-L7), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcMath.sol#L18-L18)


```solidity

File: packages/contracts/contracts/Dependencies/ReentrancyGuard.sol

//@audit OPEN need comments
8:     uint256 internal constant OPEN = 1;

//@audit LOCKED need comments
9:     uint256 internal constant LOCKED = 2;

//@audit locked need comments
11:     uint256 public locked = OPEN;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/ReentrancyGuard.sol#L8-L8) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/ReentrancyGuard.sol#L9-L9), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/ReentrancyGuard.sol#L11-L11)


```solidity

File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

//@audit users need comments
26:     EnumerableSet.AddressSet internal users;

//@audit targets need comments
27:     EnumerableSet.AddressSet internal targets;

//@audit enabledFunctionSigsByTarget need comments
28:     mapping(address => EnumerableSet.Bytes32Set) internal enabledFunctionSigsByTarget;

//@audit enabledFunctionSigsPublic need comments
30:     EnumerableSet.Bytes32Set internal enabledFunctionSigsPublic;

//@audit getUserRoles need comments
32:     mapping(address => bytes32) public getUserRoles;

//@audit capabilityFlag need comments
34:     mapping(address => mapping(bytes4 => CapabilityFlag)) public capabilityFlag;

//@audit getRolesWithCapability need comments
36:     mapping(address => mapping(bytes4 => bytes32)) public getRolesWithCapability;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L26-L26) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L27-L27), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L28-L28), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L30-L30), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L32-L32), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L34-L34), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L36-L36)


</details>


### [NC&#x2011;60] Contracts should have full test coverage 
While 100% code coverage does not guarantee that there are no bugs, it often will catch easy-to-find bugs, and will ensure that there are fewer regressions when the code invariably has to be modified. Furthermore, in order to get full coverage, code authors will often have to re-organize their code so that it is more modular, so that each component can be tested separately, which reduces interdependencies between modules and layers, and makes for code that is easier to reason about and audit.


*There are 1 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/ActivePool.sol

@audit Multiple files
1: 


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L1-L1) 


</details>


### [NC&#x2011;61] Numeric values having to do with time should use time units for readability 
There are [units](https://docs.soliditylang.org/en/latest/units-and-global-variables.html#time-units) for seconds, minutes, hours, days, and weeks, and since they're defined, they should be use


*There are 8 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/CdpManager.sol

//@audit the value  should use time units
697:             lastRedemptionTimestamp += _minutesPassedSinceLastRedemption() * SECONDS_IN_ONE_MINUTE;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L697-L697) 


```solidity

File: packages/contracts/contracts/CdpManagerStorage.sol

//@audit the value 60 should use time units
139:     uint256 public constant SECONDS_IN_ONE_MINUTE = 60;

//@audit the value 999037758833783000 should use time units
148:     uint256 public minuteDecayFactor = 999037758833783000;

//@audit the value 1 should use time units
149:     uint256 public constant MIN_MINUTE_DECAY_FACTOR = 1; // Non-zero

//@audit the value 999999999999999999 should use time units
150:     uint256 public constant MAX_MINUTE_DECAY_FACTOR = 999999999999999999; // Corresponds to a very fast decay rate, but not too extreme


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L139-L139) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L148-L148), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L149-L149), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L150-L150)


```solidity

File: packages/contracts/contracts/PriceFeed.sol

//@audit the value 4800 should use time units
32:     uint256 public constant TIMEOUT_ETH_BTC_FEED = 4800; // 1 hours & 20min: 60 * 80

//@audit the value 90000 should use time units
33:     uint256 public constant TIMEOUT_STETH_ETH_FEED = 90000; // 25 hours: 60 * 60 * 25


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L32-L32) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L33-L33)


```solidity

File: packages/contracts/contracts/Dependencies/EbtcMath.sol

//@audit the value 525600000 should use time units
61:             _minutes = 525600000;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcMath.sol#L61-L61) 


</details>


### [NC&#x2011;62] Contract declarations should have NatSpec `@title` annotations 



*There are 30 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

12: /// @notice CollSurplusPool holds stETH collateral for Cdp owner when redemption or liquidation happens
13: /// @notice only if there is a remaining portion of the closed Cdp for the owner to claim
14: /// @dev While an owner could have multiple different sized Cdps, the remaining surplus colateral from all of its closed Cdp
15: /// @dev is consolidated into one balance here
16: contract CollSurplusPool is ICollSurplusPool, ReentrancyGuard, AuthNoOwner {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L12-L16) 


```solidity

File: packages/contracts/contracts/EBTCToken.sol

26: contract EBTCToken is IEBTCToken, AuthNoOwner, PermitNonce {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L26-L26) 


```solidity

File: packages/contracts/contracts/Governor.sol

08: /// @notice Role based Authority that supports up to 256 roles.
09: /// @notice We have taken the tradeoff of additional storage usage for easier readabiliy without using off-chain / indexing services.
10: /// @author BadgerDAO Expanded from Solmate RolesAuthority
11: /// @author Modified from Solmate (https://github.com/transmissions11/solmate/blob/main/src/auth/authorities/RolesAuthority.sol)
12: /// @author Modified from Dappsys (https://github.com/dapphub/ds-roles/blob/master/src/roles.sol)
13: contract Governor is RolesAuthority {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L8-L13) 


```solidity

File: packages/contracts/contracts/PriceFeed.sol

21: contract PriceFeed is BaseMath, IPriceFeed, AuthNoOwner {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L21-L21) 


```solidity

File: packages/contracts/contracts/SortedCdps.sol

51: contract SortedCdps is ISortedCdps {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L51-L51) 


```solidity

File: packages/contracts/contracts/LeverageMacroBase.sol

14: interface ICdpCdps {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L14-L14) 


```solidity

File: packages/contracts/contracts/LeverageMacroDelegateTarget.sol

6: interface IOwnerLike {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L6-L6) 


```solidity

File: packages/contracts/contracts/Dependencies/Auth.sol

6: /// @notice Provides a flexible and updatable auth pattern which is completely separate from application logic.
7: /// @author Solmate (https://github.com/transmissions11/solmate/blob/main/src/auth/Auth.sol)
8: /// @author Modified from Dappsys (https://github.com/dapphub/ds-auth/blob/master/src/auth.sol)
9: abstract contract Auth {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/Auth.sol#L6-L9) 


```solidity

File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

06: /// @notice Provides a flexible and updatable auth pattern which is completely separate from application logic.
07: /// @author Modified by BadgerDAO to remove owner
08: /// @author Solmate (https://github.com/transmissions11/solmate/blob/main/src/auth/Auth.sol)
09: /// @author Modified from Dappsys (https://github.com/dapphub/ds-auth/blob/master/src/auth.sol)
10: contract AuthNoOwner {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L6-L10) 


```solidity

File: packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol

8: abstract contract ERC3156FlashLender is IERC3156FlashLender {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L8-L8) 


```solidity

File: packages/contracts/contracts/Dependencies/EbtcBase.sol

16: contract EbtcBase is BaseMath, IEbtcBase {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L16-L16) 


```solidity

File: packages/contracts/contracts/Dependencies/EbtcMath.sol

5: library EbtcMath {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcMath.sol#L5-L5) 


```solidity

File: packages/contracts/contracts/Dependencies/ReentrancyGuard.sol

4: /// @notice Gas optimized reentrancy protection for smart contracts.
5: /// @author Solmate (https://github.com/transmissions11/solmate/blob/main/src/utils/ReentrancyGuard.sol)
6: /// @author Modified from OpenZeppelin (https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/security/ReentrancyGuard.sol)
7: abstract contract ReentrancyGuard {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/ReentrancyGuard.sol#L4-L7) 


```solidity

File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

08: /// @notice Role based Authority that supports up to 256 roles.
09: /// @author BadgerDAO
10: /// @author Modified from Solmate (https://github.com/transmissions11/solmate/blob/main/src/auth/authorities/RolesAuthority.sol)
11: /// @author Modified from Dappsys (https://github.com/dapphub/ds-roles/blob/master/src/roles.sol)
12: contract RolesAuthority is IRolesAuthority, Auth, Authority {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L8-L12) 


```solidity

File: packages/contracts/contracts/Interfaces/IActivePool.sol

7: interface IActivePool is IPool {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IActivePool.sol#L7-L7) 


```solidity

File: packages/contracts/contracts/Interfaces/IBorrowerOperations.sol

7: interface IBorrowerOperations is IPositionManagers {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L7-L7) 


```solidity

File: packages/contracts/contracts/Interfaces/ICdpManager.sol

9: interface ICdpManager is IEbtcBase, ICdpManagerData {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManager.sol#L9-L9) 


```solidity

File: packages/contracts/contracts/Interfaces/ICdpManagerData.sol

13: interface ICdpManagerData is IRecoveryModeGracePeriod {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L13-L13) 


```solidity

File: packages/contracts/contracts/Interfaces/ICollSurplusPool.sol

5: interface ICollSurplusPool {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICollSurplusPool.sol#L5-L5) 


```solidity

File: packages/contracts/contracts/Interfaces/IEbtcBase.sol

7: interface IEbtcBase {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IEbtcBase.sol#L7-L7) 


```solidity

File: packages/contracts/contracts/Interfaces/IEBTCToken.sol

8: interface IEBTCToken is IERC20, IERC2612 {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IEBTCToken.sol#L8-L8) 


```solidity

File: packages/contracts/contracts/Interfaces/IERC3156FlashBorrower.sol

5: interface IERC3156FlashBorrower {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IERC3156FlashBorrower.sol#L5-L5) 


```solidity

File: packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol

7: interface IERC3156FlashLender {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol#L7-L7) 


```solidity

File: packages/contracts/contracts/Interfaces/IFallbackCaller.sol

5: interface IFallbackCaller {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IFallbackCaller.sol#L5-L5) 


```solidity

File: packages/contracts/contracts/Interfaces/IPermitNonce.sol

5: interface IPermitNonce {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPermitNonce.sol#L5-L5) 


```solidity

File: packages/contracts/contracts/Interfaces/IPool.sol

6: interface IPool {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPool.sol#L6-L6) 


```solidity

File: packages/contracts/contracts/Interfaces/IPositionManagers.sol

5: interface IPositionManagers {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPositionManagers.sol#L5-L5) 


```solidity

File: packages/contracts/contracts/Interfaces/IPriceFeed.sol

5: interface IPriceFeed {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPriceFeed.sol#L5-L5) 


```solidity

File: packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol

5: interface IRecoveryModeGracePeriod {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol#L5-L5) 


```solidity

File: packages/contracts/contracts/Interfaces/ISortedCdps.sol

6: interface ISortedCdps {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ISortedCdps.sol#L6-L6) 


</details>


### [NC&#x2011;63] Open TODOs 
TODOs may signal that a feature is missing or not ready for audit, consider resolving the issue and removing the TODO comment


*There are 1 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/CdpManager.sol

79:     //    Cdp ICR     |       Liquidation Behavior (TODO gas compensation?)


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L79-L79) 


</details>


### [NC&#x2011;64] Top level pragma declarations should be separated by two blank lines 



*There are 41 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/ActivePool.sol

3: pragma solidity 0.8.17;
4: 
5: import "./Interfaces/IActivePool.sol";


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L3-L5) 


```solidity

File: packages/contracts/contracts/BorrowerOperations.sol

3: pragma solidity 0.8.17;
4: 
5: import "./Interfaces/IBorrowerOperations.sol";


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L3-L5) 


```solidity

File: packages/contracts/contracts/CdpManager.sol

3: pragma solidity 0.8.17;
4: 
5: import "./Interfaces/ICdpManager.sol";


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L3-L5) 


```solidity

File: packages/contracts/contracts/LiquidationLibrary.sol

3: pragma solidity 0.8.17;
4: import "./Interfaces/ICdpManagerData.sol";


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L3-L4) 


```solidity

File: packages/contracts/contracts/CdpManagerStorage.sol

3: pragma solidity 0.8.17;
4: 
5: import "./Interfaces/ICdpManager.sol";


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L3-L5) 


```solidity

File: packages/contracts/contracts/CollSurplusPool.sol

3: pragma solidity 0.8.17;
4: 
5: import "./Interfaces/ICollSurplusPool.sol";


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L3-L5) 


```solidity

File: packages/contracts/contracts/EBTCToken.sol

3: pragma solidity 0.8.17;
4: 
5: import "./Interfaces/IEBTCToken.sol";


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L3-L5) 


```solidity

File: packages/contracts/contracts/Governor.sol

2: pragma solidity 0.8.17;
3: 
4: import {EnumerableSet} from "./Dependencies/EnumerableSet.sol";


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L2-L4) 


```solidity

File: packages/contracts/contracts/PriceFeed.sol

3: pragma solidity 0.8.17;
4: 
5: import "./Interfaces/IPriceFeed.sol";


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L3-L5) 


```solidity

File: packages/contracts/contracts/SortedCdps.sol

3: pragma solidity 0.8.17;
4: 
5: import "./Interfaces/ISortedCdps.sol";


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L3-L5) 


```solidity

File: packages/contracts/contracts/HintHelpers.sol

3: pragma solidity 0.8.17;
4: 
5: import "./Interfaces/ICdpManager.sol";


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L3-L5) 


```solidity

File: packages/contracts/contracts/LeverageMacroBase.sol

2: pragma solidity 0.8.17;
3: 
4: import "./Interfaces/IBorrowerOperations.sol";

12: import "./Dependencies/SafeERC20.sol";
13: 
14: interface ICdpCdps {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L2-L4) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L12-L14)


```solidity

File: packages/contracts/contracts/LeverageMacroDelegateTarget.sol

2: pragma solidity 0.8.17;
3: 
4: import {LeverageMacroBase} from "./LeverageMacroBase.sol";

4: import {LeverageMacroBase} from "./LeverageMacroBase.sol";
5: 
6: interface IOwnerLike {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L2-L4) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L4-L6)


```solidity

File: packages/contracts/contracts/LeverageMacroFactory.sol

2: pragma solidity 0.8.17;
3: 
4: import {LeverageMacroReference} from "./LeverageMacroReference.sol";


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroFactory.sol#L2-L4) 


```solidity

File: packages/contracts/contracts/LeverageMacroReference.sol

2: pragma solidity 0.8.17;
3: 
4: import {LeverageMacroBase} from "./LeverageMacroBase.sol";


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroReference.sol#L2-L4) 


```solidity

File: packages/contracts/contracts/Dependencies/Auth.sol

2: pragma solidity 0.8.17;
3: 
4: import {Authority} from "./Authority.sol";


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/Auth.sol#L2-L4) 


```solidity

File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

2: pragma solidity 0.8.17;
3: 
4: import {Authority} from "./Authority.sol";


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L2-L4) 


```solidity

File: packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol

3: pragma solidity 0.8.17;
4: 
5: import "../Interfaces/IERC3156FlashLender.sol";

6: import "../Interfaces/IWETH.sol";
7: 
8: abstract contract ERC3156FlashLender is IERC3156FlashLender {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L3-L5) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L6-L8)


```solidity

File: packages/contracts/contracts/Dependencies/EbtcBase.sol

3: pragma solidity 0.8.17;
4: 
5: import "./BaseMath.sol";


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L3-L5) 


```solidity

File: packages/contracts/contracts/Dependencies/EbtcMath.sol

3: pragma solidity 0.8.17;
4: 
5: library EbtcMath {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcMath.sol#L3-L5) 


```solidity

File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

2: pragma solidity 0.8.17;
3: 
4: import {IRolesAuthority} from "./IRolesAuthority.sol";


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L2-L4) 


```solidity

File: packages/contracts/contracts/Interfaces/IActivePool.sol

3: pragma solidity 0.8.17;
4: 
5: import "./IPool.sol";

5: import "./IPool.sol";
6: 
7: interface IActivePool is IPool {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IActivePool.sol#L3-L5) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IActivePool.sol#L5-L7)


```solidity

File: packages/contracts/contracts/Interfaces/IBorrowerOperations.sol

3: pragma solidity 0.8.17;
4: import "./IPositionManagers.sol";


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L3-L4) 


```solidity

File: packages/contracts/contracts/Interfaces/ICdpManager.sol

3: pragma solidity 0.8.17;
4: 
5: import "./IEbtcBase.sol";


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManager.sol#L3-L5) 


```solidity

File: packages/contracts/contracts/Interfaces/ICdpManagerData.sol

3: pragma solidity 0.8.17;
4: 
5: import "./ICollSurplusPool.sol";


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L3-L5) 


```solidity

File: packages/contracts/contracts/Interfaces/ICollSurplusPool.sol

3: pragma solidity 0.8.17;
4: 
5: interface ICollSurplusPool {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICollSurplusPool.sol#L3-L5) 


```solidity

File: packages/contracts/contracts/Interfaces/IEbtcBase.sol

3: pragma solidity 0.8.17;
4: 
5: import "./IPriceFeed.sol";

5: import "./IPriceFeed.sol";
6: 
7: interface IEbtcBase {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IEbtcBase.sol#L3-L5) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IEbtcBase.sol#L5-L7)


```solidity

File: packages/contracts/contracts/Interfaces/IEBTCToken.sol

3: pragma solidity 0.8.17;
4: 
5: import "../Dependencies/IERC20.sol";

6: import "../Dependencies/IERC2612.sol";
7: 
8: interface IEBTCToken is IERC20, IERC2612 {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IEBTCToken.sol#L3-L5) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IEBTCToken.sol#L6-L8)


```solidity

File: packages/contracts/contracts/Interfaces/IERC3156FlashBorrower.sol

3: pragma solidity 0.8.17;
4: 
5: interface IERC3156FlashBorrower {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IERC3156FlashBorrower.sol#L3-L5) 


```solidity

File: packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol

3: pragma solidity 0.8.17;
4: 
5: import "./IERC3156FlashBorrower.sol";

5: import "./IERC3156FlashBorrower.sol";
6: 
7: interface IERC3156FlashLender {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol#L3-L5) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol#L5-L7)


```solidity

File: packages/contracts/contracts/Interfaces/IFallbackCaller.sol

3: pragma solidity 0.8.17;
4: 
5: interface IFallbackCaller {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IFallbackCaller.sol#L3-L5) 


```solidity

File: packages/contracts/contracts/Interfaces/IPermitNonce.sol

3: pragma solidity 0.8.17;
4: 
5: interface IPermitNonce {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPermitNonce.sol#L3-L5) 


```solidity

File: packages/contracts/contracts/Interfaces/IPositionManagers.sol

3: pragma solidity 0.8.17;
4: 
5: interface IPositionManagers {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPositionManagers.sol#L3-L5) 


```solidity

File: packages/contracts/contracts/Interfaces/IPriceFeed.sol

3: pragma solidity 0.8.17;
4: 
5: interface IPriceFeed {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPriceFeed.sol#L3-L5) 


</details>


### [NC&#x2011;65] Critical functions should be a two step procedure 
Critical functions in Solidity contracts should follow a two-step procedure to enhance security, minimize human error, and ensure proper access control. By dividing sensitive operations into distinct phases, such as initiation and confirmation, developers can introduce a safeguard against unintended actions or unauthorized access.


*There are 17 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/ActivePool.sol

390:     function setFeeRecipientAddress(address _feeRecipientAddress) external requiresAuth {

404:     function setFeeBps(uint256 _newFee) external requiresAuth {

417:     function setFlashLoansPaused(bool _paused) external requiresAuth {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L390-L390) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L404-L404), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L417-L417)


```solidity

File: packages/contracts/contracts/BorrowerOperations.sol

1140:     function setFeeRecipientAddress(address _feeRecipientAddress) external requiresAuth {

1154:     function setFeeBps(uint256 _newFee) external requiresAuth {

1167:     function setFlashLoansPaused(bool _paused) external requiresAuth {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L1140-L1140) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L1154-L1154), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L1167-L1167)


```solidity

File: packages/contracts/contracts/CdpManager.sol

773:     function setStakingRewardSplit(uint256 _stakingRewardSplit) external requiresAuth {

788:     function setRedemptionFeeFloor(uint256 _redemptionFeeFloor) external requiresAuth {

807:     function setMinuteDecayFactor(uint256 _minuteDecayFactor) external requiresAuth {

830:     function setBeta(uint256 _beta) external requiresAuth {

843:     function setRedemptionsPaused(bool _paused) external requiresAuth {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L773-L773) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L788-L788), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L807-L807), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L830-L830), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L843-L843)


```solidity

File: packages/contracts/contracts/CdpManagerStorage.sol

111:     function setGracePeriod(uint128 _gracePeriod) external requiresAuth {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L111-L111) 


```solidity

File: packages/contracts/contracts/Governor.sol

154:     function setRoleName(uint8 role, string memory roleName) external requiresAuth {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L154-L154) 


```solidity

File: packages/contracts/contracts/PriceFeed.sol

358:     function setFallbackCaller(address _fallbackCaller) external requiresAuth {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L358-L358) 


```solidity

File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

85:     function setPublicCapability(

106:     function setRoleCapability(

147:     function setUserRole(address user, uint8 role, bool enabled) public virtual requiresAuth {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L85-L85) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L106-L106), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L147-L147)


</details>


### [NC&#x2011;66] Typos 
Modifiers in Solidity can improve code readability and modularity by encapsulating repetitive checks, such as address validity checks, into a reusable construct. For example, an `onlyOwner` modifier can be used to replace repetitive `require(msg.sender == owner)` checks across several functions, reducing code redundancy and enhancing maintainability. To implement, define a modifier with the check, then apply the modifier to relevant functions.


*There are 5 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/ActivePool.sol

//@audit `liqudations` is misspelled
118:     /// @notice Sends stETH to a specified account, drawing from both core shares and liquidator rewards shares
119:     /// @notice Liquidator reward shares are not tracked via internal accounting in the active pool and are assumed to be present in expected amount as part of the intended behavior of BorowerOperations and CdpManager
120:     /// @dev Liquidator reward shares are added when a cdp is opened, and removed when it is closed
121:     /// @dev closeCdp() or liqudations result in the actor (borrower or liquidator respectively) receiving the liquidator reward shares
122:     /// @dev Redemptions result in the shares being sent to the coll surplus pool for claiming by the CDP owner
123:     /// @dev Note that funds in the coll surplus pool, just like liquidator reward shares, are not tracked as part of the system CR or coll of a CDP.
124:     /// @dev Requires that the caller is either BorrowerOperations or CdpManager
125:     /// @param _account The address of the account to send systemCollShares and the liquidator reward to
126:     /// @param _shares The amount of systemCollShares to send
127:     /// @param _liquidatorRewardShares The amount of the liquidator reward shares to send
128: 

//@audit `recieved` is misspelled
239:     /// @notice Notify that stETH collateral shares have been recieved, updating internal accounting accordingly
240:     /// @param _value The amount of collateral to receive
241: 

//@audit `calcualted` is misspelled
312:     /// @notice Calculate the flash loan fee for a given token and amount loaned
313:     /// @param token The address of the token to calculate the fee for
314:     /// @param amount The amount of tokens to calculate the fee for
315:     /// @return The flashloan fee calcualted for given token and loan amount
316: 

//@audit `permissinos` is misspelled
342:     /// @notice Claim outstanding shares for fee recipient, updating internal accounting and transferring the shares.
343:     /// @dev Call permissinos are managed via authority for flexibility, rather than gating call to just feeRecipient.
344:     /// @dev Is likely safe as an open permission though caution should be taken.
345:     /// @param _shares The amount of shares to claim to feeRecipient


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L118-L128) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L239-L241), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L312-L316), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L342-L345)


```solidity

File: packages/contracts/contracts/BorrowerOperations.sol

//@audit `exclsuive` is misspelled
778:     /// @notice Send stETH to Active Pool and increase its recorded ETH balance
779:     /// @param _stEthBalance total balance of stETH to send, inclusive of coll and liquidatorRewardShares
780:     /// @param _sharesToTrack coll as shares (exclsuive of liquidator reward shares)
781:     /// @dev Liquidator reward shares are not considered as part of the system for CR purposes.
782:     /// @dev These number of liquidator shares associated with each Cdp are stored in the Cdp, while the actual tokens float in the active pool


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L778-L782) 


</details>


### [NC&#x2011;67] uint variables should have the bit size defined explicitly 
Instead of using uint to declare uint258, explicitly define uint258 to ensure there is no confusion


*There are 36 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

//@audit `_debtChange`
834:     function _requireNonZeroDebtChange(uint _debtChange) internal pure {

//@audit `status`
830:         uint status = cdpManager.getCdpStatus(_cdpId);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L834-L834) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L830-L830)


```solidity

File: packages/contracts/contracts/LiquidationLibrary.sol

//@audit `_debtToColl`
278:         uint _debtToColl = (_totalDebtToBurn * DECIMAL_PRECISION) / _liqState.price;

//@audit `_cappedColl`
279:         uint _cappedColl = collateral.getPooledEthByShares(_cappedColPortion + _liquidatorReward);

//@audit `_debtToColl`
365:         uint _debtToColl = (_totalDebtToBurn * DECIMAL_PRECISION) / _recoveryState.price;

//@audit `_cappedColl`
366:         uint _cappedColl = collateral.getPooledEthByShares(_cappedColPortion + _liquidatorReward);

//@audit `_debtToColl`
435:             uint _debtToColl = (_partialDebt * DECIMAL_PRECISION) / _partialState.price;

//@audit `_cappedColl`
436:             uint _cappedColl = collateral.getPooledEthByShares(_partialColl);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L278-L278) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L279-L279), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L365-L365), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L366-L366), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L435-L435), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L436-L436)


```solidity

File: packages/contracts/contracts/CdpManagerStorage.sol

//@audit `_pendingDebt`
357:             uint _pendingDebt,

//@audit `prevCollShares`
365:             uint prevCollShares = _cdp.coll;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L357-L357) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L365-L365)


```solidity

File: packages/contracts/contracts/SortedCdps.sol

//@audit `maxNodes`
159:         uint maxNodes

//@audit `maxNodes`
177:         uint maxNodes

//@audit `maxNodes`
230:         uint maxNodes

//@audit `maxNodes`
240:         uint maxNodes

//@audit `maxNodes`
289:         uint maxNodes

//@audit `maxNodes`
302:         uint maxNodes,

//@audit `maxArraySize`
303:         uint maxArraySize

//@audit `_currentIndex`
182:         uint _currentIndex = 0;

//@audit `_ownedCount`
245:         uint _ownedCount = 0;

//@audit `_ownedCount`
273:         (uint _ownedCount, ) = _cdpCountOf(owner, dummyId, 0);

//@audit `_ownedCount`
293:         (uint _ownedCount, ) = _cdpCountOf(owner, startNodeId, maxNodes);

//@audit `_cdpRetrieved`
312:         uint _cdpRetrieved;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L159-L159) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L177-L177), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L230-L230), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L240-L240), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L289-L289), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L302-L302), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L303-L303), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L182-L182), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L245-L245), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L273-L273), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L293-L293), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L312-L312)


```solidity

File: packages/contracts/contracts/Dependencies/EbtcBase.sol

//@audit `_tcr`
124:     function _checkICRAgainstLiqThreshold(uint256 _icr, uint _tcr) internal view returns (bool) {

//@audit `_tcr`
140:     function _checkICRAgainstTCR(uint256 _icr, uint _tcr) internal view returns (bool) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L124-L124) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L140-L140)


```solidity

File: packages/contracts/contracts/Interfaces/IBorrowerOperations.sol

//@audit `_EBTCAmount`
28:         uint _EBTCAmount,

//@audit `_collAmount`
31:         uint _collAmount,


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L28-L28) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L31-L31)


```solidity

File: packages/contracts/contracts/Interfaces/ICdpManager.sol

//@audit ``
56:     function getCdpLiquidatorRewardShares(bytes32 _cdpId) external view returns (uint);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManager.sol#L56-L56) 


```solidity

File: packages/contracts/contracts/Interfaces/ICdpManagerData.sol

//@audit `_debt`
45:         uint _debt,

//@audit `_collShares`
46:         uint _collShares,

//@audit `_premiumToLiquidator`
49:         uint _premiumToLiquidator

//@audit `_premiumToLiquidator`
58:         uint _premiumToLiquidator


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L45-L45) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L46-L46), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L49-L49), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L58-L58)


```solidity

File: packages/contracts/contracts/Interfaces/IPositionManagers.sol

//@audit `_deadline`
36:         uint _deadline,


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPositionManagers.sol#L36-L36) 


```solidity

File: packages/contracts/contracts/Interfaces/ISortedCdps.sol

//@audit `_NICR`
9:     event NodeAdded(bytes32 _id, uint _NICR);

//@audit `maxNodes`
66:         uint maxNodes

//@audit `maxNodes`
74:         uint maxNodes

//@audit `maxNodes`
83:         uint maxNodes


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ISortedCdps.sol#L9-L9) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ISortedCdps.sol#L66-L66), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ISortedCdps.sol#L74-L74), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ISortedCdps.sol#L83-L83)


</details>


### [NC&#x2011;68] Uncommented fields in a struct 
Consider adding comments for all the fields in a struct to improve the readability of the codebase.


*There are 26 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

//@audit Add explanational comments to the following items `price`, `collSharesChange`, `netDebtChange`, `isCollIncrease`, `collShares`, `oldICR`, `newICR`, `newTCR`, `newDebt`, `newCollShares`, `stake`, 
72:     struct AdjustCdpLocals {
73:         uint256 price;
74:         uint256 collSharesChange;
75:         uint256 netDebtChange;
76:         bool isCollIncrease;
77:         uint256 debt;
78:         uint256 collShares;
79:         uint256 oldICR;
80:         uint256 newICR;
81:         uint256 newTCR;
82:         uint256 newDebt;
83:         uint256 newCollShares;
84:         uint256 stake;
85:     }

//@audit Add explanational comments to the following items `price`, `netStEthBalance`, `NICR`, `stake`, `arrayIndex`, 
87:     struct OpenCdpLocals {
88:         uint256 price;
89:         uint256 debt;
90:         uint256 netStEthBalance;
91:         uint256 ICR;
92:         uint256 NICR;
93:         uint256 stake;
94:         uint256 arrayIndex;
95:     }

//@audit Add explanational comments to the following items `collSharesChange`, `isCollIncrease`, `netDebtChange`, 
097:     struct MoveTokensParams {
098:         address user;
099:         uint256 collSharesChange;
100:         uint256 collAddUnderlying; // ONLY for isCollIncrease=true
101:         bool isCollIncrease;
102:         uint256 netDebtChange;
103:         bool isDebtIncrease;
104:     }


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L72-L85) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L87-L95), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L97-L104)


```solidity

File: packages/contracts/contracts/Governor.sol

//@audit Add explanational comments to the following items `functionSig`, 
24:     struct Capability {
25:         address target;
26:         bytes4 functionSig;
27:         uint8[] roles;
28:     }


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L24-L28) 


```solidity

File: packages/contracts/contracts/HintHelpers.sol

//@audit Add explanational comments to the following items `remainingEbtcToRedeem`, `minNetDebtInBTC`, `currentCdpId`, `currentCdpUser`, 
19:     struct LocalVariables_getRedemptionHints {
20:         uint256 remainingEbtcToRedeem;
21:         uint256 minNetDebtInBTC;
22:         bytes32 currentCdpId;
23:         address currentCdpUser;
24:     }


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L19-L24) 


```solidity

File: packages/contracts/contracts/LeverageMacroBase.sol

//@audit Add explanational comments to the following items `operator`, 
89:     struct CheckValueAndType {
90:         uint256 value;
91:         Operator operator;
92:     }

//@audit Add explanational comments to the following items `expectedDebt`, `expectedCollateral`, `cdpId`, 
094:     struct PostCheckParams {
095:         CheckValueAndType expectedDebt;
096:         CheckValueAndType expectedCollateral;
097:         // Used only if cdpStats || isClosed
098:         bytes32 cdpId;
099:         // Used only to check status
100:         ICdpManagerData.Status expectedStatus; // NOTE: THIS IS SUPERFLUOUS
101:     }

//@audit Add explanational comments to the following items `tokenToTransferIn`, `amountToTransferIn`, 
259:     struct LeverageMacroOperation {
260:         address tokenToTransferIn;
261:         uint256 amountToTransferIn;
262:         SwapOperation[] swapsBefore; // Empty to skip
263:         SwapOperation[] swapsAfter; // Empty to skip
264:         OperationType operationType; // Open, Close, etc..
265:         bytes OperationData; // Generic Operation Data, which we'll decode to use
266:     }

//@audit Add explanational comments to the following items `tokenForSwap`, `exactApproveAmount`, `calldataForSwap`, 
268:     struct SwapOperation {
269:         // Swap Data
270:         address tokenForSwap;
271:         address addressForApprove;
272:         uint256 exactApproveAmount;
273:         address addressForSwap;
274:         bytes calldataForSwap;
275:         SwapCheck[] swapChecks; // Empty to skip
276:     }

//@audit Add explanational comments to the following items `tokenToCheck`, `expectedMinOut`, 
278:     struct SwapCheck {
279:         // Swap Slippage Check
280:         address tokenToCheck;
281:         uint256 expectedMinOut;
282:     }

//@audit Add explanational comments to the following items `eBTCToMint`, `_upperHint`, `_lowerHint`, `stETHToDeposit`, 
313:     struct OpenCdpOperation {
314:         // Open CDP For Data
315:         uint256 eBTCToMint;
316:         bytes32 _upperHint;
317:         bytes32 _lowerHint;
318:         uint256 stETHToDeposit;
319:     }

//@audit Add explanational comments to the following items `_cdpId`, `_stEthBalanceDecrease`, `_EBTCChange`, `_isDebtIncrease`, `_upperHint`, `_lowerHint`, `_stEthBalanceIncrease`, 
322:     struct AdjustCdpOperation {
323:         bytes32 _cdpId;
324:         uint256 _stEthBalanceDecrease;
325:         uint256 _EBTCChange;
326:         bool _isDebtIncrease;
327:         bytes32 _upperHint;
328:         bytes32 _lowerHint;
329:         uint256 _stEthBalanceIncrease;
330:     }

//@audit Add explanational comments to the following items `_cdpId`, 
333:     struct CloseCdpOperation {
334:         bytes32 _cdpId;
335:     }


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L89-L92) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L94-L101), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L259-L266), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L268-L276), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L278-L282), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L313-L319), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L322-L330), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L333-L335)


```solidity

File: packages/contracts/contracts/Interfaces/ICdpManagerData.sol

//@audit Add explanational comments to the following items `debt`, `coll`, `stake`, `liquidatorRewardShares`, `status`, `arrayIndex`, 
097:     struct Cdp {
098:         uint256 debt;
099:         uint256 coll;
100:         uint256 stake;
101:         uint256 liquidatorRewardShares;
102:         Status status;
103:         uint128 arrayIndex;
104:     }

//@audit Add explanational comments to the following items `debt`, `collShares`, 
113:     struct CdpDebtAndCollShares {
114:         uint256 debt;
115:         uint256 collShares;
116:     }

//@audit Add explanational comments to the following items `cdpId`, `price`, `ICR`, `upperPartialHint`, `lowerPartialHint`, `recoveryModeAtStart`, `TCR`, `totalSurplusCollShares`, `totalCollSharesToSend`, `totalDebtToBurn`, `totalDebtToRedistribute`, `totalLiquidatorRewardCollShares`, 
118:     struct LiquidationLocals {
119:         bytes32 cdpId;
120:         uint256 partialAmount; // used only for partial liquidation, default 0 means full liquidation
121:         uint256 price;
122:         uint256 ICR;
123:         bytes32 upperPartialHint;
124:         bytes32 lowerPartialHint;
125:         bool recoveryModeAtStart;
126:         uint256 TCR;
127:         uint256 totalSurplusCollShares;
128:         uint256 totalCollSharesToSend;
129:         uint256 totalDebtToBurn;
130:         uint256 totalDebtToRedistribute;
131:         uint256 totalLiquidatorRewardCollShares;
132:     }

//@audit Add explanational comments to the following items `entireSystemDebt`, `entireSystemColl`, `totalDebtToBurn`, `totalCollSharesToSend`, `totalSurplusCollShares`, `cdpId`, `price`, `ICR`, `totalDebtToRedistribute`, `totalLiquidatorRewardCollShares`, 
134:     struct LiquidationRecoveryModeLocals {
135:         uint256 entireSystemDebt;
136:         uint256 entireSystemColl;
137:         uint256 totalDebtToBurn;
138:         uint256 totalCollSharesToSend;
139:         uint256 totalSurplusCollShares;
140:         bytes32 cdpId;
141:         uint256 price;
142:         uint256 ICR;
143:         uint256 totalDebtToRedistribute;
144:         uint256 totalLiquidatorRewardCollShares;
145:     }

//@audit Add explanational comments to the following items `price`, `recoveryModeAtStart`, `liquidatedDebt`, `liquidatedColl`, 
147:     struct LocalVariables_OuterLiquidationFunction {
148:         uint256 price;
149:         bool recoveryModeAtStart;
150:         uint256 liquidatedDebt;
151:         uint256 liquidatedColl;
152:     }

//@audit Add explanational comments to the following items `i`, `ICR`, `cdpId`, `backToNormalMode`, `entireSystemDebt`, `entireSystemColl`, `price`, `TCR`, 
154:     struct LocalVariables_LiquidationSequence {
155:         uint256 i;
156:         uint256 ICR;
157:         bytes32 cdpId;
158:         bool backToNormalMode;
159:         uint256 entireSystemDebt;
160:         uint256 entireSystemColl;
161:         uint256 price;
162:         uint256 TCR;
163:     }

//@audit Add explanational comments to the following items `cdpId`, `maxEBTCamount`, `price`, `upperPartialRedemptionHint`, `lowerPartialRedemptionHint`, `partialRedemptionHintNICR`, 
165:     struct SingleRedemptionInputs {
166:         bytes32 cdpId;
167:         uint256 maxEBTCamount;
168:         uint256 price;
169:         bytes32 upperPartialRedemptionHint;
170:         bytes32 lowerPartialRedemptionHint;
171:         uint256 partialRedemptionHintNICR;
172:     }

//@audit Add explanational comments to the following items `entireCdpDebt`, `debtToBurn`, `totalCollToSendToLiquidator`, `debtToRedistribute`, `collSurplus`, `liquidatorCollSharesReward`, 
174:     struct LiquidationValues {
175:         uint256 entireCdpDebt;
176:         uint256 debtToBurn;
177:         uint256 totalCollToSendToLiquidator;
178:         uint256 debtToRedistribute;
179:         uint256 collSurplus;
180:         uint256 liquidatorCollSharesReward;
181:     }

//@audit Add explanational comments to the following items `totalDebtInSequence`, `totalDebtToBurn`, `totalCollToSendToLiquidator`, `totalDebtToRedistribute`, `totalCollSurplus`, `totalCollReward`, 
183:     struct LiquidationTotals {
184:         uint256 totalDebtInSequence;
185:         uint256 totalDebtToBurn;
186:         uint256 totalCollToSendToLiquidator;
187:         uint256 totalDebtToRedistribute;
188:         uint256 totalCollSurplus;
189:         uint256 totalCollReward;
190:     }

//@audit Add explanational comments to the following items `remainingDebtToRedeem`, `debtToRedeem`, `collSharesDrawn`, `totalCollSharesSurplus`, `feeCollShares`, `collSharesToRedeemer`, `decayedBaseRate`, `price`, `systemDebtAtStart`, `systemCollSharesAtStart`, `tcrAtStart`, 
194:     struct RedemptionTotals {
195:         uint256 remainingDebtToRedeem;
196:         uint256 debtToRedeem;
197:         uint256 collSharesDrawn;
198:         uint256 totalCollSharesSurplus;
199:         uint256 feeCollShares;
200:         uint256 collSharesToRedeemer;
201:         uint256 decayedBaseRate;
202:         uint256 price;
203:         uint256 systemDebtAtStart;
204:         uint256 systemCollSharesAtStart;
205:         uint256 tcrAtStart;
206:     }

//@audit Add explanational comments to the following items `debtToRedeem`, `collSharesDrawn`, `collSurplus`, `liquidatorRewardShares`, `cancelledPartial`, `fullRedemption`, 
208:     struct SingleRedemptionValues {
209:         uint256 debtToRedeem;
210:         uint256 collSharesDrawn;
211:         uint256 collSurplus;
212:         uint256 liquidatorRewardShares;
213:         bool cancelledPartial;
214:         bool fullRedemption;
215:     }


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L97-L104) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L113-L116), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L118-L132), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L134-L145), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L147-L152), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L154-L163), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L165-L172), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L174-L181), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L183-L190), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L194-L206), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L208-L215)


```solidity

File: packages/contracts/contracts/Interfaces/IPriceFeed.sol

//@audit Add explanational comments to the following items `roundEthBtcId`, `roundStEthEthId`, `answer`, `timestampEthBtc`, `timestampStEthEth`, `success`, 
17:     struct ChainlinkResponse {
18:         uint80 roundEthBtcId;
19:         uint80 roundStEthEthId;
20:         uint256 answer;
21:         uint256 timestampEthBtc;
22:         uint256 timestampStEthEth;
23:         bool success;
24:     }

//@audit Add explanational comments to the following items `answer`, `timestamp`, `success`, 
26:     struct FallbackResponse {
27:         uint256 answer;
28:         uint256 timestamp;
29:         bool success;
30:     }


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPriceFeed.sol#L17-L24) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPriceFeed.sol#L26-L30)


</details>


### [NC&#x2011;69] Event is missing `indexed` fields 
Index event fields make the field more quickly accessible to off-chain tools that parse events. However, note that each index field costs extra gas during emission, so it's not necessarily best to index the maximum allowed per event (three fields). Each event should use three indexed fields if there are three or more fields, and gas usage is not particularly of concern for the events in question. If there are fewer than three fields, all of the fields should be indexed.


*There are 42 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/Interfaces/IActivePool.sol

9:     event ActivePoolEBTCDebtUpdated(uint256 _EBTCDebt);

10:     event SystemCollSharesUpdated(uint256 _coll);

12:     event FeeRecipientClaimableCollSharesIncreased(uint256 _coll, uint256 _fee);

13:     event FeeRecipientClaimableCollSharesDecreased(uint256 _coll, uint256 _fee);

14:     event FlashLoanSuccess(

20:     event SweepTokenSuccess(address indexed _token, uint256 _amount, address indexed _recipient);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IActivePool.sol#L9-L9) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IActivePool.sol#L10-L10), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IActivePool.sol#L12-L12), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IActivePool.sol#L13-L13), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IActivePool.sol#L14-L14), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IActivePool.sol#L20-L20)


```solidity

File: packages/contracts/contracts/Interfaces/IBorrowerOperations.sol

11:     event FlashLoanSuccess(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L11-L11) 


```solidity

File: packages/contracts/contracts/Interfaces/ICdpManagerData.sol

17:     event StakingRewardSplitSet(uint256 _stakingRewardSplit);

18:     event RedemptionFeeFloorSet(uint256 _redemptionFeeFloor);

19:     event MinuteDecayFactorSet(uint256 _minuteDecayFactor);

20:     event BetaSet(uint256 _beta);

21:     event RedemptionsPaused(bool _paused);

23:     event Liquidation(uint256 _liquidatedDebt, uint256 _liquidatedColl, uint256 _liqReward);

24:     event Redemption(

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


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L17-L17) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L18-L18), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L19-L19), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L20-L20), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L21-L21), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L23-L23), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L24-L24), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L60-L60), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L61-L61), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L62-L62), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L63-L63), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L64-L64), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L65-L65), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L66-L66), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L67-L67), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L68-L68), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L69-L69)


```solidity

File: packages/contracts/contracts/Interfaces/ICollSurplusPool.sol

8:     event SurplusCollSharesUpdated(address indexed _account, uint256 _newBalance);

9:     event CollSharesTransferred(address indexed _to, uint256 _amount);

11:     event SweepTokenSuccess(address indexed _token, uint256 _amount, address indexed _recipient);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICollSurplusPool.sol#L8-L8) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICollSurplusPool.sol#L9-L9), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICollSurplusPool.sol#L11-L11)


```solidity

File: packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol

8:     event FlashFeeSet(address indexed _setter, uint256 _oldFee, uint256 _newFee);

9:     event MaxFlashFeeSet(address indexed _setter, uint256 _oldMaxFee, uint256 _newMaxFee);

10:     event FlashLoansPaused(address indexed _setter, bool _paused);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol#L8-L8) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol#L9-L9), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol#L10-L10)


```solidity

File: packages/contracts/contracts/Interfaces/IFallbackCaller.sol

7:     event FallbackTimeOutChanged(uint256 _oldTimeOut, uint256 _newTimeOut);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IFallbackCaller.sol#L7-L7) 


```solidity

File: packages/contracts/contracts/Interfaces/IPool.sol

9:     event ETHBalanceUpdated(uint256 _newBalance);

10:     event EBTCBalanceUpdated(uint256 _newBalance);

11:     event CollSharesTransferred(address indexed _to, uint256 _amount);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPool.sol#L9-L9) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPool.sol#L10-L10), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPool.sol#L11-L11)


```solidity

File: packages/contracts/contracts/Interfaces/IPositionManagers.sol

12:     event PositionManagerApprovalSet(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPositionManagers.sol#L12-L12) 


```solidity

File: packages/contracts/contracts/Interfaces/IPriceFeed.sol

7:     event LastGoodPriceUpdated(uint256 _lastGoodPrice);

8:     event PriceFeedStatusChanged(Status newStatus);

13:     event UnhealthyFallbackCaller(address indexed _fallbackCaller, uint256 timestamp);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPriceFeed.sol#L7-L7) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPriceFeed.sol#L8-L8), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPriceFeed.sol#L13-L13)


```solidity

File: packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol

6:     event TCRNotified(uint256 TCR); /// NOTE: Mostly for debugging to ensure synch

11:     event GracePeriodDurationSet(uint256 _recoveryModeGracePeriodDuration);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol#L6-L6) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol#L11-L11)


```solidity

File: packages/contracts/contracts/Interfaces/ISortedCdps.sol

9:     event NodeAdded(bytes32 _id, uint _NICR);

10:     event NodeRemoved(bytes32 _id);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ISortedCdps.sol#L9-L9) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ISortedCdps.sol#L10-L10)


</details>


### [NC&#x2011;70] Unused Import 
Some files/Items are imported but never used


*There are 19 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

//@audit `ICdpManagerData` is not used
7: import "./Interfaces/ICdpManagerData.sol";

//@audit `Ownable` is not used
13: import "./Dependencies/Ownable.sol";


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L7-L7) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L13-L13)


```solidity

File: packages/contracts/contracts/CdpManager.sol

//@audit `ICollSurplusPool` is not used
6: import "./Interfaces/ICollSurplusPool.sol";

//@audit `IEBTCToken` is not used
7: import "./Interfaces/IEBTCToken.sol";

//@audit `ICollateralTokenOracle` is not used
9: import "./Dependencies/ICollateralTokenOracle.sol";


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L6-L6) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L7-L7), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L9-L9)


```solidity

File: packages/contracts/contracts/LiquidationLibrary.sol

//@audit `ICollSurplusPool` is not used
5: import "./Interfaces/ICollSurplusPool.sol";

//@audit `IEBTCToken` is not used
6: import "./Interfaces/IEBTCToken.sol";

//@audit `ISortedCdps` is not used
7: import "./Interfaces/ISortedCdps.sol";

//@audit `ICollateralTokenOracle` is not used
8: import "./Dependencies/ICollateralTokenOracle.sol";


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L5-L5) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L6-L6), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L7-L7), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L8-L8)


```solidity

File: packages/contracts/contracts/CdpManagerStorage.sol

//@audit `ICollateralTokenOracle` is not used
11: import "./Dependencies/ICollateralTokenOracle.sol";


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L11-L11) 


```solidity

File: packages/contracts/contracts/SortedCdps.sol

//@audit `IBorrowerOperations` is not used
7: import "./Interfaces/IBorrowerOperations.sol";


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L7-L7) 


```solidity

File: packages/contracts/contracts/LeverageMacroBase.sol

//@audit `IPriceFeed` is not used
9: import "./Interfaces/IPriceFeed.sol";


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L9-L9) 


```solidity

File: packages/contracts/contracts/LeverageMacroFactory.sol

//@audit `ICollateralToken` is not used
5: import "./Dependencies/ICollateralToken.sol";

//@audit `IEBTCToken` is not used
6: import "./Interfaces/IEBTCToken.sol";


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroFactory.sol#L5-L5) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroFactory.sol#L6-L6)


```solidity

File: packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol

//@audit `IWETH` is not used
6: import "../Interfaces/IWETH.sol";


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L6-L6) 


```solidity

File: packages/contracts/contracts/Interfaces/ICdpManagerData.sol

//@audit `ICollSurplusPool` is not used
5: import "./ICollSurplusPool.sol";

//@audit `ISortedCdps` is not used
7: import "./ISortedCdps.sol";

//@audit `IActivePool` is not used
8: import "./IActivePool.sol";

//@audit `ICollateralTokenOracle` is not used
10: import "../Dependencies/ICollateralTokenOracle.sol";


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L5-L5) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L7-L7), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L8-L8), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L10-L10)


</details>


### [NC&#x2011;71] Unused parameter 



*There are 9 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/CdpManager.sol

//@audit `_cdpId` is not used
99:     function liquidate(bytes32 _cdpId) external override {

//@audit `_cdpId` is not used
110:         bytes32 _cdpId,

//@audit `_partialAmount` is not used
111:         uint256 _partialAmount,

//@audit `_upperPartialHint` is not used
112:         bytes32 _upperPartialHint,

//@audit `_lowerPartialHint` is not used
113:         bytes32 _lowerPartialHint

//@audit `_cdpArray` is not used
126:     function batchLiquidateCdps(bytes32[] memory _cdpArray) external override {

//@audit `_price` is not used
757:     function _requireTCRisNotBelowMCR(uint256 _price, uint256 _TCR) internal view {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L99-L99) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L110-L110), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L111-L111), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L112-L112), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L113-L113), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L126-L126), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L757-L757)


```solidity

File: packages/contracts/contracts/LeverageMacroBase.sol

//@audit `amount` is not used
347:         uint256 amount,

//@audit `fee` is not used
348:         uint256 fee,


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L347-L347) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L348-L348)


</details>


### [NC&#x2011;72] Unused `internal`/`private` contract variable 
If these serve no purpose, they should be safely removed


*There are 2 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/Governor.sol

//@audit the variable `NO_ROLES` is declared but never used
17:     bytes32 NO_ROLES = bytes32(0);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L17-L17) 


```solidity

File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

//@audit the variable `enabledFunctionSigsPublic` is declared but never used
30:     EnumerableSet.Bytes32Set internal enabledFunctionSigsPublic;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L30-L30) 


</details>


### [NC&#x2011;73] Cast to `bytes` or `bytes32` for clearer semantic meaning 
Using a [cast](https://ethereum.stackexchange.com/questions/30912/how-to-compare-strings-in-solidity#answer-82739) on a single argument, rather than `abi.encodePacked()` makes the intended operation more clear, leading to less reviewer confusion.


*There are 1 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/HintHelpers.sol

182:             latestRandomSeed = uint256(keccak256(abi.encodePacked(latestRandomSeed)));


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L182-L182) 


</details>


### [NC&#x2011;74] Use `bytes.concat()` on bytes instead of `abi.encodePacked()` for clearer semantic meaning 
Starting with version 0.8.4, Solidity has the `bytes.concat()` function, which allows one to concatenate a list of bytes/strings, without extra padding. Using this function rather than `abi.encodePacked()` makes the intended operation more clear, leading to less reviewer confusion.


*There are 2 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

718:             abi.encodePacked(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L718-L718) 


```solidity

File: packages/contracts/contracts/EBTCToken.sol

210:             abi.encodePacked(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L210-L210) 


</details>


### [NC&#x2011;75] Use `string.concat()` on strings instead of `abi.encodePacked()` for clearer semantic meaning 
Starting with version 0.8.12, Solidity has the `string.concat()` function, which allows one to concatenate a list of strings, without extra padding. Using this function rather than `abi.encodePacked()` makes the intended operation more clear, leading to less reviewer confusion.


*There are 2 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

718:             abi.encodePacked(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L718-L718) 


```solidity

File: packages/contracts/contracts/EBTCToken.sol

210:             abi.encodePacked(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L210-L210) 


</details>


### [NC&#x2011;76] Constants should be defined rather than using magic numbers 
Even [assembly](https://github.com/code-423n4/2022-05-opensea-seaport/blob/9d7ce4d08bf3c3010304a0476a785c70c0e90ae7/contracts/lib/TokenTransferrer.sol#L35-L39) can benefit from using readable constants instead of hex/numeric literals


*There are 6 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/PriceFeed.sol

//@audit Try to make a `constant` with `10` value
799:             : 10 ** (_ethBtcDecimals - _stEthEthDecimals);

//@audit Try to make a `constant` with `10` value
798:             ? 10 ** (_stEthEthDecimals - _ethBtcDecimals)

//@audit Try to make a `constant` with `10` value
804:                 EbtcMath.DECIMAL_PRECISION) / 10 ** (_decimalDenominator * 2);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L799-L799) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L798-L798), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L804-L804)


```solidity

File: packages/contracts/contracts/SimplifiedDiamondLike.sol

//@audit Try to make a `constant` with `0x94b24d09` value
56:         require(sig != 0x94b24d09);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L56-L56) 


```solidity

File: packages/contracts/contracts/Dependencies/EbtcMath.sol

//@audit Try to make a `constant` with `525600000` value
60:         if (_minutes > 525600000) {

//@audit Try to make a `constant` with `525600000` value
61:             _minutes = 525600000;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcMath.sol#L60-L60) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcMath.sol#L61-L61)


</details>


### [NC&#x2011;77] Use the latest solidity (prior to 0.8.20 if on L2s) for deployment 
```
When deploying contracts, you should use the latest released version of Solidity.Apart from exceptional cases, only the latest version receives security fixes.
```
https://docs.soliditylang.org/en/v0.8.20/


*There are 39 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/ActivePool.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/BorrowerOperations.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/CdpManager.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/LiquidationLibrary.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/CdpManagerStorage.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/CollSurplusPool.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/EBTCToken.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/Governor.sol

2: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L2-L2) 


```solidity

File: packages/contracts/contracts/PriceFeed.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/SortedCdps.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/HintHelpers.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/LeverageMacroBase.sol

2: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L2-L2) 


```solidity

File: packages/contracts/contracts/LeverageMacroDelegateTarget.sol

2: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L2-L2) 


```solidity

File: packages/contracts/contracts/LeverageMacroFactory.sol

2: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroFactory.sol#L2-L2) 


```solidity

File: packages/contracts/contracts/LeverageMacroReference.sol

2: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroReference.sol#L2-L2) 


```solidity

File: packages/contracts/contracts/SimplifiedDiamondLike.sol

2: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L2-L2) 


```solidity

File: packages/contracts/contracts/Dependencies/Auth.sol

2: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/Auth.sol#L2-L2) 


```solidity

File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

2: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L2-L2) 


```solidity

File: packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/Dependencies/EbtcBase.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/Dependencies/EbtcMath.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcMath.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/Dependencies/ReentrancyGuard.sol

2: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/ReentrancyGuard.sol#L2-L2) 


```solidity

File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

2: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L2-L2) 


```solidity

File: packages/contracts/contracts/Interfaces/IActivePool.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IActivePool.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/Interfaces/IBorrowerOperations.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/Interfaces/ICdpManager.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManager.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/Interfaces/ICdpManagerData.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/Interfaces/ICollSurplusPool.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICollSurplusPool.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/Interfaces/IEbtcBase.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IEbtcBase.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/Interfaces/IEBTCToken.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IEBTCToken.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/Interfaces/IERC3156FlashBorrower.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IERC3156FlashBorrower.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/Interfaces/IFallbackCaller.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IFallbackCaller.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/Interfaces/IPermitNonce.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPermitNonce.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/Interfaces/IPool.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPool.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/Interfaces/IPositionManagers.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPositionManagers.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/Interfaces/IPriceFeed.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPriceFeed.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol

2: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol#L2-L2) 


```solidity

File: packages/contracts/contracts/Interfaces/ISortedCdps.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ISortedCdps.sol#L3-L3) 


</details>


### [NC&#x2011;78] Use OpenZeppelin's or Solady's Ownable, rather than re-inventing the wheel 
Both implementations have been optimized and are usage-hardened, so writing your own is unnecessary


*There are 1 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

13: import "./Dependencies/Ownable.sol";


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L13-L13) 


</details>


### [NC&#x2011;79] Use OpenZeppelin's `ReentrancyGuard` / `ReentrancyGuardUpgradeable` rather than writing your own 
The OpenZeppelin version has been gas-optimized, and thoroughly test, so consider using it rather than writing your own


*There are 1 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/Dependencies/ReentrancyGuard.sol

13:     modifier nonReentrant() virtual {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/ReentrancyGuard.sol#L13-L13) 


</details>


### [NC&#x2011;80] Use a single file for system wide constants 
Consider grouping all the system constants under a single file. This finding shows only the first constant for each file.


*There are 14 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/ActivePool.sol

24:     string public constant NAME = "ActivePool";


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L24-L24) 


```solidity

File: packages/contracts/contracts/BorrowerOperations.sol

29:     string public constant NAME = "BorrowerOperations";


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L29-L29) 


```solidity

File: packages/contracts/contracts/CdpManagerStorage.sol

21:     uint128 public constant UNSET_TIMESTAMP = type(uint128).max;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L21-L21) 


```solidity

File: packages/contracts/contracts/CollSurplusPool.sol

19:     string public constant NAME = "CollSurplusPool";


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L19-L19) 


```solidity

File: packages/contracts/contracts/EBTCToken.sol

28:     string internal constant _NAME = "EBTC Stablecoin";


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L28-L28) 


```solidity

File: packages/contracts/contracts/PriceFeed.sol

22:     string public constant NAME = "PriceFeed";


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L22-L22) 


```solidity

File: packages/contracts/contracts/SortedCdps.sol

52:     string public constant NAME = "SortedCdps";


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L52-L52) 


```solidity

File: packages/contracts/contracts/HintHelpers.sol

12:     string public constant NAME = "HintHelpers";


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L12-L12) 


```solidity

File: packages/contracts/contracts/LeverageMacroBase.sol

37:     bytes32 constant FLASH_LOAN_SUCCESS = keccak256("ERC3156FlashBorrower.onFlashLoan");


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L37-L37) 


```solidity

File: packages/contracts/contracts/SimplifiedDiamondLike.sol

39:     bytes32 constant DIAMOND_STORAGE_POSITION = keccak256("diamond.standard.diamond.storage");


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L39-L39) 


```solidity

File: packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol

9:     uint256 public constant MAX_BPS = 10_000;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L9-L9) 


```solidity

File: packages/contracts/contracts/Dependencies/EbtcBase.sol

19:     uint256 public constant LICR = 1030000000000000000; // 103%


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L19-L19) 


```solidity

File: packages/contracts/contracts/Dependencies/EbtcMath.sol

6:     uint256 internal constant DECIMAL_PRECISION = 1e18;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcMath.sol#L6-L6) 


```solidity

File: packages/contracts/contracts/Dependencies/ReentrancyGuard.sol

8:     uint256 internal constant OPEN = 1;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/ReentrancyGuard.sol#L8-L8) 


</details>


### [NC&#x2011;81] Consider using SMTChecker 
The SMTChecker is a valuable tool for Solidity developers as it helps detect potential vulnerabilities and logical errors in the contract's code. By utilizing Satisfiability Modulo Theories (SMT) solvers, it can reason about the potential states a contract can be in, and therefore, identify conditions that could lead to undesirable behavior. This automatic formal verification can catch issues that might otherwise be missed in manual code reviews or standard testing, enhancing the overall contract's security and reliability.


*There are 39 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/ActivePool.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/BorrowerOperations.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/CdpManager.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/LiquidationLibrary.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/CdpManagerStorage.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/CollSurplusPool.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/EBTCToken.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/Governor.sol

2: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L2-L2) 


```solidity

File: packages/contracts/contracts/PriceFeed.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/SortedCdps.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/HintHelpers.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/LeverageMacroBase.sol

2: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L2-L2) 


```solidity

File: packages/contracts/contracts/LeverageMacroDelegateTarget.sol

2: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L2-L2) 


```solidity

File: packages/contracts/contracts/LeverageMacroFactory.sol

2: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroFactory.sol#L2-L2) 


```solidity

File: packages/contracts/contracts/LeverageMacroReference.sol

2: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroReference.sol#L2-L2) 


```solidity

File: packages/contracts/contracts/SimplifiedDiamondLike.sol

2: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L2-L2) 


```solidity

File: packages/contracts/contracts/Dependencies/Auth.sol

2: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/Auth.sol#L2-L2) 


```solidity

File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

2: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L2-L2) 


```solidity

File: packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/Dependencies/EbtcBase.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/Dependencies/EbtcMath.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcMath.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/Dependencies/ReentrancyGuard.sol

2: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/ReentrancyGuard.sol#L2-L2) 


```solidity

File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

2: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L2-L2) 


```solidity

File: packages/contracts/contracts/Interfaces/IActivePool.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IActivePool.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/Interfaces/IBorrowerOperations.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/Interfaces/ICdpManager.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManager.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/Interfaces/ICdpManagerData.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/Interfaces/ICollSurplusPool.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICollSurplusPool.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/Interfaces/IEbtcBase.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IEbtcBase.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/Interfaces/IEBTCToken.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IEBTCToken.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/Interfaces/IERC3156FlashBorrower.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IERC3156FlashBorrower.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/Interfaces/IFallbackCaller.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IFallbackCaller.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/Interfaces/IPermitNonce.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPermitNonce.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/Interfaces/IPool.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPool.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/Interfaces/IPositionManagers.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPositionManagers.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/Interfaces/IPriceFeed.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPriceFeed.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol

2: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol#L2-L2) 


```solidity

File: packages/contracts/contracts/Interfaces/ISortedCdps.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ISortedCdps.sol#L3-L3) 


</details>


### [NC&#x2011;82] Variable name must be in mixedCase 
Avoid using underscore for variable Names or parameters


*There are 2 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/Governor.sol

// @audit NO_ROLES
17:     bytes32 NO_ROLES = bytes32(0);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L17-L17) 


```solidity

File: packages/contracts/contracts/Dependencies/EbtcMath.sol

// @audit prod_xy
36:         uint256 prod_xy = x * y;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcMath.sol#L36-L36) 


</details>


### [NC&#x2011;83] Whitespace in Expressions 
See the [Whitespace in Expressions](https://docs.soliditylang.org/en/latest/style-guide.html#whitespace-in-expressions) section of the Solidity Style Guide


*There are 32 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/CdpManager.sol

//@audit remove the whiteSpace after the '(' char
552:         debt of liquidation reserve plus MIN_NET_DEBT.
553:         3e30 EBTC dwarfs the value of all wealth in the world ( which is < 1e15 USD). */
554: 


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L552-L554) 


```solidity

File: packages/contracts/contracts/LiquidationLibrary.sol

//@audit remove the whiteSpace before the ')' char
409:         (uint256 _partialColl, uint256 newColl, ) = _calculatePartialLiquidationSurplusAndCap(
410:             _partialState.ICR,

//@audit remove the whiteSpace before the ')' char
753:         for (vars.i = _start; ; ) {
754:             vars.cdpId = _cdpArray[vars.i];

//@audit remove the whiteSpace before the ';' char
753:         for (vars.i = _start; ; ) {
754:             vars.cdpId = _cdpArray[vars.i];

//@audit remove the whiteSpace before the ')' char
816:         for (vars.i = _start; ; ) {
817:             vars.cdpId = _cdpArray[vars.i];

//@audit remove the whiteSpace before the ';' char
816:         for (vars.i = _start; ; ) {
817:             vars.cdpId = _cdpArray[vars.i];


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L409-L410) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L753-L754), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L753-L754), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L816-L817), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L816-L817)


```solidity

File: packages/contracts/contracts/CdpManagerStorage.sol

//@audit remove the whiteSpace after the '(' char
181:      *
182:      * A systemDebt increase  of ( stake * [systemDebtRedistributionIndex - systemDebtRedistributionIndex(0)] )
183:      *

//@audit remove the whiteSpace before the ')' char
182:      * A systemDebt increase  of ( stake * [systemDebtRedistributionIndex - systemDebtRedistributionIndex(0)] )
183:      *

//@audit remove the whiteSpace before the ')' char
686:         (, uint256 _newGlobalSplitIdx, ) = _calcSyncedGlobalAccounting(_newIndex, _oldIndex);
687:         (uint256 _newColl, uint256 _newDebt, , uint256 _pendingDebt, ) = _calcSyncedAccounting(

//@audit remove the whiteSpace before the ')' char
687:         (uint256 _newColl, uint256 _newDebt, , uint256 _pendingDebt, ) = _calcSyncedAccounting(
688:             _cdpId,

//@audit remove the whiteSpace before the ',' char
687:         (uint256 _newColl, uint256 _newDebt, , uint256 _pendingDebt, ) = _calcSyncedAccounting(
688:             _cdpId,

//@audit remove the whiteSpace before the ')' char
722:         (uint256 _pendingDebt, ) = _getPendingRedistributedDebt(_cdpId);
723:         return _pendingDebt;

//@audit remove the whiteSpace before the ')' char
748:         (uint256 _newColl, uint256 _newDebt, , , ) = _calcSyncedAccounting(
749:             _cdpId,

//@audit remove the whiteSpace before the ',' char
748:         (uint256 _newColl, uint256 _newDebt, , , ) = _calcSyncedAccounting(
749:             _cdpId,

//@audit remove the whiteSpace before the ')' char
840:         (uint256 _newDebt, , ) = _getSyncedCdpDebtAndRedistribution(_cdpId);
841:         return _newDebt;

//@audit remove the whiteSpace before the ',' char
840:         (uint256 _newDebt, , ) = _getSyncedCdpDebtAndRedistribution(_cdpId);
841:         return _newDebt;

//@audit remove the whiteSpace before the ')' char
850:         (, uint256 _newGlobalSplitIdx, ) = _calcSyncedGlobalAccounting(_newIndex, _oldIndex);
851:         (uint256 _newColl, , , , ) = _calcSyncedAccounting(

//@audit remove the whiteSpace before the ')' char
851:         (uint256 _newColl, , , , ) = _calcSyncedAccounting(
852:             _cdpId,

//@audit remove the whiteSpace before the ',' char
851:         (uint256 _newColl, , , , ) = _calcSyncedAccounting(
852:             _cdpId,

//@audit remove the whiteSpace before the ')' char
876:         (uint256 _feeTaken, , ) = _calcSyncedGlobalAccounting(_newIndex, _oldIndex);
877: 

//@audit remove the whiteSpace before the ',' char
876:         (uint256 _feeTaken, , ) = _calcSyncedGlobalAccounting(_newIndex, _oldIndex);
877: 


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L181-L183) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L182-L183), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L686-L687), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L687-L688), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L687-L688), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L722-L723), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L748-L749), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L748-L749), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L840-L841), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L840-L841), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L850-L851), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L851-L852), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L851-L852), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L876-L877), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L876-L877)


```solidity

File: packages/contracts/contracts/SortedCdps.sol

//@audit remove the whiteSpace before the ')' char
144:         (bytes32 _cdpId, ) = _cdpOfOwnerByIndex(owner, index, dummyId, 0);
145:         return _cdpId;

//@audit remove the whiteSpace before the ')' char
217:         (uint256 _cnt, ) = _cdpCountOf(owner, dummyId, 0);
218:         return _cnt;

//@audit remove the whiteSpace before the ')' char
273:         (uint _ownedCount, ) = _cdpCountOf(owner, dummyId, 0);
274:         if (_ownedCount > 0) {

//@audit remove the whiteSpace before the ')' char
275:             (bytes32[] memory _allCdps, , ) = _getCdpsOf(owner, dummyId, 0, _ownedCount);
276:             cdps = _allCdps;

//@audit remove the whiteSpace before the ',' char
275:             (bytes32[] memory _allCdps, , ) = _getCdpsOf(owner, dummyId, 0, _ownedCount);
276:             cdps = _allCdps;

//@audit remove the whiteSpace before the ')' char
293:         (uint _ownedCount, ) = _cdpCountOf(owner, startNodeId, maxNodes);
294:         return _getCdpsOf(owner, startNodeId, maxNodes, _ownedCount);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L144-L145) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L217-L218), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L273-L274), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L275-L276), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L275-L276), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L293-L294)


```solidity

File: packages/contracts/contracts/LeverageMacroBase.sol

//@audit remove the whiteSpace before the ')' char
385:         for (uint256 i; i < swapLength; ) {
386:             _doSwap(swapData[i]);

//@audit remove the whiteSpace before the ')' char
414:         (bool success, ) = excessivelySafeCall(
415:             swapData.addressForSwap,


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L385-L386) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L414-L415)


```solidity

File: packages/contracts/contracts/SimplifiedDiamondLike.sol

//@audit remove the whiteSpace before the ')' char
114:         for (uint256 i; i < length; ) {
115:             _executeOne(ops[i]);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L114-L115) 


```solidity

File: packages/contracts/contracts/Dependencies/EbtcBase.sol

//@audit remove the whiteSpace before the ')' char
80:         (TCR, , ) = _getTCRWithSystemDebtAndCollShares(_price);
81:     }

//@audit remove the whiteSpace before the ',' char
80:         (TCR, , ) = _getTCRWithSystemDebtAndCollShares(_price);
81:     }


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L80-L81) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L80-L81)


</details>


### [NC&#x2011;84] Complex function controle flow 
Due to multiple if, loop and conditions the following functions has a very complex controle flow that could make auditing very difficult to cover all possible path\nTherefore, consider breaking down these blocks into more manageable units, by splitting things into utility functions, by reducing nesting, and by using early returns


*There are 4 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/CdpManager.sol

320:     function redeemCollateral(
321:         uint256 _debt,
322:         bytes32 _firstRedemptionHint,
323:         bytes32 _upperPartialRedemptionHint,
324:         bytes32 _lowerPartialRedemptionHint,
325:         uint256 _partialRedemptionHintNICR,
326:         uint256 _maxIterations,
327:         uint256 _maxFeePercentage
328:     ) external override nonReentrantSelfAndBOps {
329:         RedemptionTotals memory totals;
330: 
331:         // early check to ensure redemption is not paused
332:         require(redemptionsPaused == false, "CdpManager: Redemptions Paused");
333: 
334:         _requireValidMaxFeePercentage(_maxFeePercentage);
335: 
336:         _syncGlobalAccounting(); // Apply state, we will syncGracePeriod at end of function
337: 
338:         totals.price = priceFeed.fetchPrice();
339:         {
340:             (
341:                 uint256 tcrAtStart,
342:                 uint256 systemCollSharesAtStart,
343:                 uint256 systemDebtAtStart
344:             ) = _getTCRWithSystemDebtAndCollShares(totals.price);
345:             totals.tcrAtStart = tcrAtStart;
346:             totals.systemCollSharesAtStart = systemCollSharesAtStart;
347:             totals.systemDebtAtStart = systemDebtAtStart;
348:         }
349: 
350:         _requireTCRisNotBelowMCR(totals.price, totals.tcrAtStart);
351:         _requireAmountGreaterThanZero(_debt);
352: 
353:         _requireEbtcBalanceCoversRedemptionAndWithinSupply(
354:             msg.sender,
355:             _debt,
356:             totals.systemDebtAtStart
357:         );
358: 
359:         totals.remainingDebtToRedeem = _debt;
360:         address currentBorrower;
361:         bytes32 _cId = _firstRedemptionHint;
362: 
363:         if (_isValidFirstRedemptionHint(_firstRedemptionHint, totals.price)) {
364:             currentBorrower = sortedCdps.getOwnerAddress(_firstRedemptionHint);
365:         } else {
366:             _cId = sortedCdps.getLast();
367:             currentBorrower = sortedCdps.getOwnerAddress(_cId);
368:             // Find the first cdp with ICR >= MCR
369:             while (currentBorrower != address(0) && getSyncedICR(_cId, totals.price) < MCR) {
370:                 _cId = sortedCdps.getPrev(_cId);
371:                 currentBorrower = sortedCdps.getOwnerAddress(_cId);
372:             }
373:         }
374: 
375:         // Loop through the Cdps starting from the one with lowest collateral
376:         // ratio until _amount of EBTC is exchanged for collateral
377:         if (_maxIterations == 0) {
378:             _maxIterations = type(uint256).max;
379:         }
380: 
381:         bytes32 _firstRedeemed = _cId;
382:         bytes32 _lastRedeemed = _cId;
383:         uint256 _numCdpsFullyRedeemed;
384: 
385:         /**
386:             Core Redemption Loop
387:         */
388:         while (
389:             currentBorrower != address(0) && totals.remainingDebtToRedeem > 0 && _maxIterations > 0
390:         ) {
391:             // Save the address of the Cdp preceding the current one, before potentially modifying the list
392:             {
393:                 _syncAccounting(_cId); /// @audit This happens even if the re-insertion doesn't
394: 
395:                 SingleRedemptionInputs memory _redeemColFromCdp = SingleRedemptionInputs(
396:                     _cId,
397:                     totals.remainingDebtToRedeem,
398:                     totals.price,
399:                     _upperPartialRedemptionHint,
400:                     _lowerPartialRedemptionHint,
401:                     _partialRedemptionHintNICR
402:                 );
403:                 SingleRedemptionValues memory singleRedemption = _redeemCollateralFromCdp(
404:                     _redeemColFromCdp
405:                 );
406:                 // Partial redemption was cancelled (out-of-date hint, or new net debt < minimum),
407:                 // therefore we could not redeem from the last Cdp
408:                 if (singleRedemption.cancelledPartial) break;
409: 
410:                 totals.debtToRedeem = totals.debtToRedeem + singleRedemption.debtToRedeem;
411:                 totals.collSharesDrawn = totals.collSharesDrawn + singleRedemption.collSharesDrawn;
412:                 totals.remainingDebtToRedeem =
413:                     totals.remainingDebtToRedeem -
414:                     singleRedemption.debtToRedeem;
415:                 totals.totalCollSharesSurplus =
416:                     totals.totalCollSharesSurplus +
417:                     singleRedemption.collSurplus;
418: 
419:                 if (singleRedemption.fullRedemption) {
420:                     _lastRedeemed = _cId;
421:                     _numCdpsFullyRedeemed = _numCdpsFullyRedeemed + 1;
422:                 }
423: 
424:                 bytes32 _nextId = sortedCdps.getPrev(_cId);
425:                 address nextUserToCheck = sortedCdps.getOwnerAddress(_nextId);
426:                 currentBorrower = nextUserToCheck;
427:                 _cId = _nextId;
428:             }
429:             _maxIterations--;
430:         }
431:         require(totals.collSharesDrawn > 0, "CdpManager: Unable to redeem any amount");
432: 
433:         // remove from sortedCdps
434:         if (_numCdpsFullyRedeemed == 1) {
435:             sortedCdps.remove(_firstRedeemed);
436:         } else if (_numCdpsFullyRedeemed > 1) {
437:             bytes32[] memory _toRemoveIds = _getCdpIdsToRemove(
438:                 _lastRedeemed,
439:                 _numCdpsFullyRedeemed,
440:                 _firstRedeemed
441:             );
442:             sortedCdps.batchRemove(_toRemoveIds);
443:         }
444: 
445:         // Decay the baseRate due to time passed, and then increase it according to the size of this redemption.
446:         // Use the saved total EBTC supply value, from before it was reduced by the redemption.
447:         _updateBaseRateFromRedemption(
448:             totals.collSharesDrawn,
449:             totals.price,
450:             totals.systemDebtAtStart
451:         );
452: 
453:         // Calculate the ETH fee
454:         totals.feeCollShares = _getRedemptionFee(totals.collSharesDrawn);
455: 
456:         _requireUserAcceptsFee(totals.feeCollShares, totals.collSharesDrawn, _maxFeePercentage);
457: 
458:         totals.collSharesToRedeemer = totals.collSharesDrawn - totals.feeCollShares;
459: 
460:         _syncGracePeriodForGivenValues(
461:             totals.systemCollSharesAtStart - totals.collSharesDrawn - totals.totalCollSharesSurplus,
462:             totals.systemDebtAtStart - totals.debtToRedeem,
463:             totals.price
464:         );
465: 
466:         emit Redemption(
467:             _debt,
468:             totals.debtToRedeem,
469:             totals.collSharesDrawn,
470:             totals.feeCollShares,
471:             msg.sender
472:         );
473: 
474:         // Burn the total eBTC that is redeemed
475:         ebtcToken.burn(msg.sender, totals.debtToRedeem);
476: 
477:         // Update Active Pool eBTC debt internal accounting
478:         activePool.decreaseSystemDebt(totals.debtToRedeem);
479: 
480:         // Allocate the stETH fee to the FeeRecipient
481:         activePool.allocateSystemCollSharesToFeeRecipient(totals.feeCollShares);
482: 
483:         // CEI: Send the stETH drawn to the redeemer
484:         activePool.transferSystemCollShares(msg.sender, totals.collSharesToRedeemer);
485:     }


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L320-L485) 


```solidity

File: packages/contracts/contracts/PriceFeed.sol

098:     function fetchPrice() external override returns (uint256) {
099:         // Get current and previous price data from Chainlink, and current price data from Fallback
100:         ChainlinkResponse memory chainlinkResponse = _getCurrentChainlinkResponse();
101:         ChainlinkResponse memory prevChainlinkResponse = _getPrevChainlinkResponse(
102:             chainlinkResponse.roundEthBtcId,
103:             chainlinkResponse.roundStEthEthId
104:         );
105:         FallbackResponse memory fallbackResponse = _getCurrentFallbackResponse();
106: 
107:         // --- CASE 1: System fetched last price from Chainlink  ---
108:         if (status == Status.chainlinkWorking) {
109:             // If Chainlink is broken, try Fallback
110:             if (_chainlinkIsBroken(chainlinkResponse, prevChainlinkResponse)) {
111:                 // If Fallback is broken then both oracles are untrusted, so return the last good price
112:                 if (_fallbackIsBroken(fallbackResponse)) {
113:                     _changeStatus(Status.bothOraclesUntrusted);
114:                     return lastGoodPrice;
115:                 }
116:                 /*
117:                  * If Fallback is only frozen but otherwise returning valid data, return the last good price.
118:                  * Fallback may need to be tipped to return current data.
119:                  */
120:                 if (_fallbackIsFrozen(fallbackResponse)) {
121:                     _changeStatus(Status.usingFallbackChainlinkUntrusted);
122:                     return lastGoodPrice;
123:                 }
124: 
125:                 // If Chainlink is broken and Fallback is working, switch to Fallback and return current Fallback price
126:                 _changeStatus(Status.usingFallbackChainlinkUntrusted);
127:                 return _storeFallbackPrice(fallbackResponse);
128:             }
129: 
130:             // If Chainlink is frozen, try Fallback
131:             if (_chainlinkIsFrozen(chainlinkResponse)) {
132:                 // If Fallback is broken too, remember Fallback broke, and return last good price
133:                 if (_fallbackIsBroken(fallbackResponse)) {
134:                     _changeStatus(Status.usingChainlinkFallbackUntrusted);
135:                     return lastGoodPrice;
136:                 }
137: 
138:                 // If Fallback is frozen or working, remember Chainlink froze, and switch to Fallback
139:                 _changeStatus(Status.usingFallbackChainlinkFrozen);
140: 
141:                 if (_fallbackIsFrozen(fallbackResponse)) {
142:                     return lastGoodPrice;
143:                 }
144: 
145:                 // If Fallback is working, use it
146:                 return _storeFallbackPrice(fallbackResponse);
147:             }
148: 
149:             // If Chainlink price has changed by > 50% between two consecutive rounds, compare it to Fallback's price
150:             if (_chainlinkPriceChangeAboveMax(chainlinkResponse, prevChainlinkResponse)) {
151:                 // If Fallback is broken, both oracles are untrusted, and return last good price
152:                 // We don't trust CL for now given this large price differential
153:                 if (_fallbackIsBroken(fallbackResponse)) {
154:                     _changeStatus(Status.bothOraclesUntrusted);
155:                     return lastGoodPrice;
156:                 }
157: 
158:                 // If Fallback is frozen, switch to Fallback and return last good price
159:                 // We don't trust CL for now given this large price differential
160:                 if (_fallbackIsFrozen(fallbackResponse)) {
161:                     _changeStatus(Status.usingFallbackChainlinkUntrusted);
162:                     return lastGoodPrice;
163:                 }
164: 
165:                 /*
166:                  * If Fallback is live and both oracles have a similar price, conclude that Chainlink's large price deviation between
167:                  * two consecutive rounds was likely a legitmate market price movement, and so continue using Chainlink
168:                  */
169:                 if (_bothOraclesSimilarPrice(chainlinkResponse, fallbackResponse)) {
170:                     return _storeChainlinkPrice(chainlinkResponse.answer);
171:                 }
172: 
173:                 // If Fallback is live but the oracles differ too much in price, conclude that Chainlink's initial price deviation was
174:                 // an oracle failure. Switch to Fallback, and use Fallback price
175:                 _changeStatus(Status.usingFallbackChainlinkUntrusted);
176:                 return _storeFallbackPrice(fallbackResponse);
177:             }
178: 
179:             // If Chainlink is working and Fallback is broken, remember Fallback is broken
180:             if (_fallbackIsBroken(fallbackResponse)) {
181:                 _changeStatus(Status.usingChainlinkFallbackUntrusted);
182:             }
183: 
184:             // If Chainlink is working, return Chainlink current price (no status change)
185:             return _storeChainlinkPrice(chainlinkResponse.answer);
186:         }
187: 
188:         // --- CASE 2: The system fetched last price from Fallback ---
189:         if (status == Status.usingFallbackChainlinkUntrusted) {
190:             // If both Fallback and Chainlink are live, unbroken, and reporting similar prices, switch back to Chainlink
191:             if (
192:                 _bothOraclesLiveAndUnbrokenAndSimilarPrice(
193:                     chainlinkResponse,
194:                     prevChainlinkResponse,
195:                     fallbackResponse
196:                 )
197:             ) {
198:                 _changeStatus(Status.chainlinkWorking);
199:                 return _storeChainlinkPrice(chainlinkResponse.answer);
200:             }
201: 
202:             if (_fallbackIsBroken(fallbackResponse)) {
203:                 _changeStatus(Status.bothOraclesUntrusted);
204:                 return lastGoodPrice;
205:             }
206: 
207:             /*
208:              * If Fallback is only frozen but otherwise returning valid data, just return the last good price.
209:              * Fallback may need to be tipped to return current data.
210:              */
211:             if (_fallbackIsFrozen(fallbackResponse)) {
212:                 return lastGoodPrice;
213:             }
214: 
215:             // Otherwise, use Fallback price
216:             return _storeFallbackPrice(fallbackResponse);
217:         }
218: 
219:         // --- CASE 3: Both oracles were untrusted at the last price fetch ---
220:         if (status == Status.bothOraclesUntrusted) {
221:             /*
222:              * If there's no fallback, only use Chainlink
223:              */
224:             if (address(fallbackCaller) == address(0)) {
225:                 // If CL has resumed working
226:                 if (
227:                     !_chainlinkIsBroken(chainlinkResponse, prevChainlinkResponse) &&
228:                     !_chainlinkIsFrozen(chainlinkResponse)
229:                 ) {
230:                     _changeStatus(Status.usingChainlinkFallbackUntrusted);
231:                     return _storeChainlinkPrice(chainlinkResponse.answer);
232:                 }
233:             }
234: 
235:             /*
236:              * If both oracles are now live, unbroken and similar price, we assume that they are reporting
237:              * accurately, and so we switch back to Chainlink.
238:              */
239:             if (
240:                 _bothOraclesLiveAndUnbrokenAndSimilarPrice(
241:                     chainlinkResponse,
242:                     prevChainlinkResponse,
243:                     fallbackResponse
244:                 )
245:             ) {
246:                 _changeStatus(Status.chainlinkWorking);
247:                 return _storeChainlinkPrice(chainlinkResponse.answer);
248:             }
249: 
250:             // Otherwise, return the last good price - both oracles are still untrusted (no status change)
251:             return lastGoodPrice;
252:         }
253: 
254:         // --- CASE 4: Using Fallback, and Chainlink is frozen ---
255:         if (status == Status.usingFallbackChainlinkFrozen) {
256:             if (_chainlinkIsBroken(chainlinkResponse, prevChainlinkResponse)) {
257:                 // If both Oracles are broken, return last good price
258:                 if (_fallbackIsBroken(fallbackResponse)) {
259:                     _changeStatus(Status.bothOraclesUntrusted);
260:                     return lastGoodPrice;
261:                 }
262: 
263:                 // If Chainlink is broken, remember it and switch to using Fallback
264:                 _changeStatus(Status.usingFallbackChainlinkUntrusted);
265: 
266:                 if (_fallbackIsFrozen(fallbackResponse)) {
267:                     return lastGoodPrice;
268:                 }
269: 
270:                 // If Fallback is working, return Fallback current price
271:                 return _storeFallbackPrice(fallbackResponse);
272:             }
273: 
274:             if (_chainlinkIsFrozen(chainlinkResponse)) {
275:                 // if Chainlink is frozen and Fallback is broken, remember Fallback broke, and return last good price
276:                 if (_fallbackIsBroken(fallbackResponse)) {
277:                     _changeStatus(Status.usingChainlinkFallbackUntrusted);
278:                     return lastGoodPrice;
279:                 }
280: 
281:                 // If both are frozen, just use lastGoodPrice
282:                 if (_fallbackIsFrozen(fallbackResponse)) {
283:                     return lastGoodPrice;
284:                 }
285: 
286:                 // if Chainlink is frozen and Fallback is working, keep using Fallback (no status change)
287:                 return _storeFallbackPrice(fallbackResponse);
288:             }
289: 
290:             // if Chainlink is live and Fallback is broken, remember Fallback broke, and return Chainlink price
291:             if (_fallbackIsBroken(fallbackResponse)) {
292:                 _changeStatus(Status.usingChainlinkFallbackUntrusted);
293:                 return _storeChainlinkPrice(chainlinkResponse.answer);
294:             }
295: 
296:             // If Chainlink is live and Fallback is frozen, just use last good price (no status change) since we have no basis for comparison
297:             if (_fallbackIsFrozen(fallbackResponse)) {
298:                 return lastGoodPrice;
299:             }
300: 
301:             // If Chainlink is live and Fallback is working, compare prices. Switch to Chainlink
302:             // if prices are within 5%, and return Chainlink price.
303:             if (_bothOraclesSimilarPrice(chainlinkResponse, fallbackResponse)) {
304:                 _changeStatus(Status.chainlinkWorking);
305:                 return _storeChainlinkPrice(chainlinkResponse.answer);
306:             }
307: 
308:             // Otherwise if Chainlink is live but price not within 5% of Fallback, distrust Chainlink, and return Fallback price
309:             _changeStatus(Status.usingFallbackChainlinkUntrusted);
310:             return _storeFallbackPrice(fallbackResponse);
311:         }
312: 
313:         // --- CASE 5: Using Chainlink, Fallback is untrusted ---
314:         if (status == Status.usingChainlinkFallbackUntrusted) {
315:             // If Chainlink breaks, now both oracles are untrusted
316:             if (_chainlinkIsBroken(chainlinkResponse, prevChainlinkResponse)) {
317:                 _changeStatus(Status.bothOraclesUntrusted);
318:                 return lastGoodPrice;
319:             }
320: 
321:             // If Chainlink is frozen, return last good price (no status change)
322:             if (_chainlinkIsFrozen(chainlinkResponse)) {
323:                 return lastGoodPrice;
324:             }
325: 
326:             // If Chainlink and Fallback are both live, unbroken and similar price, switch back to chainlinkWorking and return Chainlink price
327:             if (
328:                 _bothOraclesLiveAndUnbrokenAndSimilarPrice(
329:                     chainlinkResponse,
330:                     prevChainlinkResponse,
331:                     fallbackResponse
332:                 )
333:             ) {
334:                 _changeStatus(Status.chainlinkWorking);
335:                 return _storeChainlinkPrice(chainlinkResponse.answer);
336:             }
337: 
338:             // If Chainlink is live but deviated >50% from it's previous price and Fallback is still untrusted, switch
339:             // to bothOraclesUntrusted and return last good price
340:             if (_chainlinkPriceChangeAboveMax(chainlinkResponse, prevChainlinkResponse)) {
341:                 _changeStatus(Status.bothOraclesUntrusted);
342:                 return lastGoodPrice;
343:             }
344: 
345:             // Otherwise if Chainlink is live and deviated <50% from it's previous price and Fallback is still untrusted,
346:             // return Chainlink price (no status change)
347:             return _storeChainlinkPrice(chainlinkResponse.answer);
348:         }
349: 
350:         /// @audit This should never be used, but we added it for the Certora Prover
351:         return lastGoodPrice;
352:     }


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L98-L352) 


```solidity

File: packages/contracts/contracts/SortedCdps.sol

674:     function _findInsertPosition(
675:         uint256 _NICR,
676:         bytes32 _prevId,
677:         bytes32 _nextId
678:     ) internal view returns (bytes32, bytes32) {
679:         bytes32 prevId = _prevId;
680:         bytes32 nextId = _nextId;
681: 
682:         if (prevId != dummyId) {
683:             if (!contains(prevId) || _NICR > cdpManager.getCachedNominalICR(prevId)) {
684:                 // `prevId` does not exist anymore or now has a smaller NICR than the given NICR
685:                 prevId = dummyId;
686:             }
687:         }
688: 
689:         if (nextId != dummyId) {
690:             if (!contains(nextId) || _NICR < cdpManager.getCachedNominalICR(nextId)) {
691:                 // `nextId` does not exist anymore or now has a larger NICR than the given NICR
692:                 nextId = dummyId;
693:             }
694:         }
695: 
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
709:     }


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L674-L709) 


```solidity

File: packages/contracts/contracts/LeverageMacroBase.sol

118:     function doOperation(
119:         FlashLoanType flType,
120:         uint256 borrowAmount,
121:         LeverageMacroOperation calldata operation,
122:         PostOperationCheck postCheckType,
123:         PostCheckParams calldata checkParams
124:     ) external {
125:         _assertOwner();
126: 
127:         // Call FL Here, then the stuff below needs to happen inside the FL
128:         if (operation.amountToTransferIn > 0) {
129:             IERC20(operation.tokenToTransferIn).safeTransferFrom(
130:                 msg.sender,
131:                 address(this),
132:                 operation.amountToTransferIn
133:             );
134:         }
135: 
136:         /**
137:          * SETUP FOR POST CALL CHECK
138:          */
139:         uint256 initialCdpIndex;
140:         if (postCheckType == PostOperationCheck.openCdp) {
141:             // How to get owner
142:             // sortedCdps.existCdpOwners(_cdpId);
143:             initialCdpIndex = sortedCdps.cdpCountOf(address(this));
144:         }
145: 
146:         // Take eBTC or stETH FlashLoan
147:         if (flType == FlashLoanType.eBTC) {
148:             IERC3156FlashLender(address(borrowerOperations)).flashLoan(
149:                 IERC3156FlashBorrower(address(this)),
150:                 address(ebtcToken),
151:                 borrowAmount,
152:                 abi.encode(operation)
153:             );
154:         } else if (flType == FlashLoanType.stETH) {
155:             IERC3156FlashLender(address(activePool)).flashLoan(
156:                 IERC3156FlashBorrower(address(this)),
157:                 address(stETH),
158:                 borrowAmount,
159:                 abi.encode(operation)
160:             );
161:         } else {
162:             // No leverage, just do the operation
163:             _handleOperation(operation);
164:         }
165: 
166:         /**
167:          * POST CALL CHECK FOR CREATION
168:          */
169:         if (postCheckType == PostOperationCheck.openCdp) {
170:             // How to get owner
171:             // sortedCdps.existCdpOwners(_cdpId);
172:             // initialCdpIndex is initialCdpIndex + 1
173:             bytes32 cdpId = sortedCdps.cdpOfOwnerByIndex(address(this), initialCdpIndex);
174: 
175:             // Check for param details
176:             ICdpManagerData.Cdp memory cdpInfo = cdpManager.Cdps(cdpId);
177:             _doCheckValueType(checkParams.expectedDebt, cdpInfo.debt);
178:             _doCheckValueType(checkParams.expectedCollateral, cdpInfo.coll);
179:             require(
180:                 cdpInfo.status == checkParams.expectedStatus,
181:                 "!LeverageMacroReference: openCDP status check"
182:             );
183:         }
184: 
185:         // Update CDP, Ensure the stats are as intended
186:         if (postCheckType == PostOperationCheck.cdpStats) {
187:             ICdpManagerData.Cdp memory cdpInfo = cdpManager.Cdps(checkParams.cdpId);
188: 
189:             _doCheckValueType(checkParams.expectedDebt, cdpInfo.debt);
190:             _doCheckValueType(checkParams.expectedCollateral, cdpInfo.coll);
191:             require(
192:                 cdpInfo.status == checkParams.expectedStatus,
193:                 "!LeverageMacroReference: adjustCDP status check"
194:             );
195:         }
196: 
197:         // Post check type: Close, ensure it has the status we want
198:         if (postCheckType == PostOperationCheck.isClosed) {
199:             ICdpManagerData.Cdp memory cdpInfo = cdpManager.Cdps(checkParams.cdpId);
200: 
201:             require(
202:                 cdpInfo.status == checkParams.expectedStatus,
203:                 "!LeverageMacroReference: closeCDP status check"
204:             );
205:         }
206: 
207:         // Sweep here if it's Reference, do not if it's delegate
208:         if (willSweep) {
209:             sweepToCaller();
210:         }
211:     }


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L118-L211) 


</details>


### [NC&#x2011;85] Consider bounding input array length 
The functions below take in an unbounded array, and make function calls for entries in the array. While the function will revert if it eventually runs out of gas, it may be a nicer user experience to `require()` that the length of the array is below some reasonable maximum, so that the user doesn't have to use up a full transaction's gas only to see that the transaction reverts.


*There are 3 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/Governor.sol

//@audit array name roleIds
120:     function getByteMapFromRoles(uint8[] memory roleIds) public pure returns (bytes32) {
121:         bytes32 _data;
122:         for (uint8 i = 0; i < roleIds.length; i++) {
123:             _data |= bytes32(1 << uint256(roleIds[i]));
124:         }
125:         return _data;
126:     }


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L120-L126) 


```solidity

File: packages/contracts/contracts/SortedCdps.sol

//@audit array name _ids
419:     function batchRemove(bytes32[] memory _ids) external override {
420:         _requireCallerIsCdpManager();
421:         uint256 _len = _ids.length;
422:         require(_len > 1, "SortedCdps: batchRemove() only apply to multiple cdpIds!");
423: 
424:         bytes32 _firstPrev = data.nodes[_ids[0]].prevId;
425:         bytes32 _lastNext = data.nodes[_ids[_len - 1]].nextId;
426: 
427:         require(
428:             _firstPrev != dummyId || _lastNext != dummyId,
429:             "SortedCdps: batchRemove() leave ZERO node left!"
430:         );
431: 
432:         for (uint256 i = 0; i < _len; ++i) {
433:             require(contains(_ids[i]), "SortedCdps: List does not contain the id");
434:         }
435: 
436:         // orphan nodes in between to save gas
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
447: 
448:         // delete node & owner storages to get gas refund
449:         for (uint i = 0; i < _len; ++i) {
450:             delete data.nodes[_ids[i]];
451:             emit NodeRemoved(_ids[i]);
452:         }
453:         data.size = data.size - _len;
454:     }


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L419-L454) 


```solidity

File: packages/contracts/contracts/SimplifiedDiamondLike.sol

//@audit array name ops
110:     function execute(Operation[] calldata ops) external payable {
111:         require(msg.sender == owner, "Must be owner");
112: 
113:         uint256 length = ops.length;
114:         for (uint256 i; i < length; ) {
115:             _executeOne(ops[i]);
116: 
117:             unchecked {
118:                 ++i;
119:             }
120:         }
121: 
122:         // Toggle `callbackEnabledForCall` to false
123:         // NOTE: We could check calldata to see if this has to be done, but this is fine for a reference impl
124:         // Even if no-op, this ensures we never allow a callback if in that mode
125:         _setCallbackEnabledForCall(_getStorage(), false);
126:     }


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L110-L126) 


</details>


### [NC&#x2011;86] A function which defines named returns in it's declaration doesn't need to use return 
Remove the return statement once ensuring it is safe to do so


*There are 11 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/CdpManager.sol

135:     function _redeemCollateralFromCdp(
136:         SingleRedemptionInputs memory _redeemColFromCdp
137:     ) internal returns (SingleRedemptionValues memory singleRedemption) {
138:         // Determine the remaining amount (lot) to be redeemed,
139:         // capped by the entire debt of the Cdp minus the liquidation reserve
140:         singleRedemption.debtToRedeem = EbtcMath._min(
141:             _redeemColFromCdp.maxEBTCamount,
142:             Cdps[_redeemColFromCdp.cdpId].debt /// @audit Redeem everything
143:         );
144: 
145:         singleRedemption.collSharesDrawn = collateral.getSharesByPooledEth(
146:             (singleRedemption.debtToRedeem * DECIMAL_PRECISION) / _redeemColFromCdp.price
147:         );
148: 
149:         // Repurposing this struct here to avoid stack too deep.
150:         CdpDebtAndCollShares memory _oldDebtAndColl = CdpDebtAndCollShares(
151:             Cdps[_redeemColFromCdp.cdpId].debt,
152:             Cdps[_redeemColFromCdp.cdpId].coll
153:         );
154: 
155:         // Decrease the debt and collateral of the current Cdp according to the EBTC lot and corresponding ETH to send
156:         uint256 newDebt = _oldDebtAndColl.debt - singleRedemption.debtToRedeem;
157:         uint256 newColl = _oldDebtAndColl.collShares - singleRedemption.collSharesDrawn;
158: 
159:         if (newDebt == 0) {
160:             // No debt remains, close Cdp
161:             // No debt left in the Cdp, therefore the cdp gets closed
162:             {
163:                 address _borrower = sortedCdps.getOwnerAddress(_redeemColFromCdp.cdpId);
164:                 uint256 _liquidatorRewardShares = Cdps[_redeemColFromCdp.cdpId]
165:                     .liquidatorRewardShares;
166: 
167:                 singleRedemption.collSurplus = newColl; // Collateral surplus processed on full redemption
168:                 singleRedemption.liquidatorRewardShares = _liquidatorRewardShares;
169:                 singleRedemption.fullRedemption = true;
170: 
171:                 _closeCdpByRedemption(
172:                     _redeemColFromCdp.cdpId,
173:                     0,
174:                     newColl,
175:                     _liquidatorRewardShares,
176:                     _borrower
177:                 );
178: 
179:                 emit CdpUpdated(
180:                     _redeemColFromCdp.cdpId,
181:                     _borrower,
182:                     msg.sender,
183:                     _oldDebtAndColl.debt,
184:                     _oldDebtAndColl.collShares,
185:                     0,
186:                     0,
187:                     0,
188:                     CdpOperation.redeemCollateral
189:                 );
190:             }
191:         } else {
192:             // Debt remains, reinsert Cdp
193:             uint256 newNICR = EbtcMath._computeNominalCR(newColl, newDebt);
194: 
195:             /*
196:              * If the provided hint is out of date, we bail since trying to reinsert without a good hint will almost
197:              * certainly result in running out of gas.
198:              *
199:              * If the resultant net coll of the partial is less than the minimum, we bail.
200:              */
201:             if (
202:                 newNICR != _redeemColFromCdp.partialRedemptionHintNICR ||
203:                 collateral.getPooledEthByShares(newColl) < MIN_NET_STETH_BALANCE
204:             ) {
205:                 singleRedemption.cancelledPartial = true;
206:                 return singleRedemption;
207:             }
208: 
209:             sortedCdps.reInsert(
210:                 _redeemColFromCdp.cdpId,
211:                 newNICR,
212:                 _redeemColFromCdp.upperPartialRedemptionHint,
213:                 _redeemColFromCdp.lowerPartialRedemptionHint
214:             );
215: 
216:             Cdps[_redeemColFromCdp.cdpId].debt = newDebt;
217:             Cdps[_redeemColFromCdp.cdpId].coll = newColl;
218:             _updateStakeAndTotalStakes(_redeemColFromCdp.cdpId);
219: 
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
231:         }
232: 
233:         return singleRedemption;
234:     }

550:     function _addCdpIdToArray(bytes32 _cdpId) internal returns (uint128 index) {
551:         /* Max array size is 2**128 - 1, i.e. ~3e30 cdps. No risk of overflow, since cdps have minimum EBTC
552:         debt of liquidation reserve plus MIN_NET_DEBT.
553:         3e30 EBTC dwarfs the value of all wealth in the world ( which is < 1e15 USD). */
554: 
555:         // Push the Cdpowner to the array
556:         CdpIds.push(_cdpId);
557: 
558:         // Record the index of the new Cdpowner on their Cdp struct
559:         index = uint128(CdpIds.length - 1);
560:         Cdps[_cdpId].arrayIndex = index;
561: 
562:         return index;
563:     }

570:     function getSystemDebt() public view returns (uint256 entireSystemDebt) {
571:         return _getSystemDebt();
572:     }


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L135-L234) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L550-L563), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L570-L572)


```solidity

File: packages/contracts/contracts/LiquidationLibrary.sol

839:     function _addLiquidationValuesToTotals(
840:         LiquidationTotals memory oldTotals,
841:         LiquidationValues memory singleLiquidation
842:     ) internal pure returns (LiquidationTotals memory newTotals) {
843:         // Tally all the values with their respective running totals
844:         newTotals.totalDebtInSequence =
845:             oldTotals.totalDebtInSequence +
846:             singleLiquidation.entireCdpDebt;
847:         newTotals.totalDebtToBurn = oldTotals.totalDebtToBurn + singleLiquidation.debtToBurn;
848:         newTotals.totalCollToSendToLiquidator =
849:             oldTotals.totalCollToSendToLiquidator +
850:             singleLiquidation.totalCollToSendToLiquidator;
851:         newTotals.totalDebtToRedistribute =
852:             oldTotals.totalDebtToRedistribute +
853:             singleLiquidation.debtToRedistribute;
854:         newTotals.totalCollSurplus = oldTotals.totalCollSurplus + singleLiquidation.collSurplus;
855:         newTotals.totalCollReward =
856:             oldTotals.totalCollReward +
857:             singleLiquidation.liquidatorCollSharesReward;
858: 
859:         return newTotals;
860:     }


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L839-L860) 


```solidity

File: packages/contracts/contracts/CdpManagerStorage.sol

719:     function getPendingRedistributedDebt(
720:         bytes32 _cdpId
721:     ) public view returns (uint256 pendingEBTCDebtReward) {
722:         (uint256 _pendingDebt, ) = _getPendingRedistributedDebt(_cdpId);
723:         return _pendingDebt;
724:     }


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L719-L724) 


```solidity

File: packages/contracts/contracts/Governor.sol

146:     function getRoleName(uint8 role) external view returns (string memory roleName) {
147:         return roleNames[role];
148:     }


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L146-L148) 


```solidity

File: packages/contracts/contracts/PriceFeed.sol

606:     function _getCurrentChainlinkResponse()
607:         internal
608:         view
609:         returns (ChainlinkResponse memory chainlinkResponse)
610:     {
611:         // Fetch decimals for both feeds:
612:         uint8 ethBtcDecimals;
613:         uint8 stEthEthDecimals;
614: 
615:         try ETH_BTC_CL_FEED.decimals() returns (uint8 decimals) {
616:             // If call to Chainlink succeeds, record the current decimal precision
617:             ethBtcDecimals = decimals;
618:         } catch {
619:             // If call to Chainlink aggregator reverts, return a zero response with success = false
620:             return chainlinkResponse;
621:         }
622: 
623:         try STETH_ETH_CL_FEED.decimals() returns (uint8 decimals) {
624:             // If call to Chainlink succeeds, record the current decimal precision
625:             stEthEthDecimals = decimals;
626:         } catch {
627:             // If call to Chainlink aggregator reverts, return a zero response with success = false
628:             return chainlinkResponse;
629:         }
630: 
631:         // Try to get latest prices data:
632:         int256 ethBtcAnswer;
633:         int256 stEthEthAnswer;
634:         try ETH_BTC_CL_FEED.latestRoundData() returns (
635:             uint80 roundId,
636:             int256 answer,
637:             uint256,
638:             /* startedAt */
639:             uint256 timestamp,
640:             uint80 /* answeredInRound */
641:         ) {
642:             ethBtcAnswer = answer;
643:             chainlinkResponse.roundEthBtcId = roundId;
644:             chainlinkResponse.timestampEthBtc = timestamp;
645:         } catch {
646:             // If call to Chainlink aggregator reverts, return a zero response with success = false
647:             return chainlinkResponse;
648:         }
649: 
650:         try STETH_ETH_CL_FEED.latestRoundData() returns (
651:             uint80 roundId,
652:             int256 answer,
653:             uint256,
654:             /* startedAt */
655:             uint256 timestamp,
656:             uint80 /* answeredInRound */
657:         ) {
658:             stEthEthAnswer = answer;
659:             chainlinkResponse.roundStEthEthId = roundId;
660:             chainlinkResponse.timestampStEthEth = timestamp;
661:         } catch {
662:             // If call to Chainlink aggregator reverts, return a zero response with success = false
663:             return chainlinkResponse;
664:         }
665: 
666:         if (
667:             _checkHealthyCLResponse(chainlinkResponse.roundEthBtcId, ethBtcAnswer) &&
668:             _checkHealthyCLResponse(chainlinkResponse.roundStEthEthId, stEthEthAnswer)
669:         ) {
670:             chainlinkResponse.answer = _formatClAggregateAnswer(
671:                 ethBtcAnswer,
672:                 stEthEthAnswer,
673:                 ethBtcDecimals,
674:                 stEthEthDecimals
675:             );
676:         } else {
677:             return chainlinkResponse;
678:         }
679: 
680:         chainlinkResponse.success = true;
681:     }

687:     function _getPrevChainlinkResponse(
688:         uint80 _currentRoundEthBtcId,
689:         uint80 _currentRoundStEthEthId
690:     ) internal view returns (ChainlinkResponse memory prevChainlinkResponse) {
691:         // If first round, early return
692:         // Handles revert from underflow in _currentRoundEthBtcId - 1
693:         // and _currentRoundStEthEthId - 1
694:         // Behavior should be indentical to following block if this revert was caught
695:         if (_currentRoundEthBtcId == 0 || _currentRoundStEthEthId == 0) {
696:             return prevChainlinkResponse;
697:         }
698: 
699:         // Fetch decimals for both feeds:
700:         uint8 ethBtcDecimals;
701:         uint8 stEthEthDecimals;
702: 
703:         try ETH_BTC_CL_FEED.decimals() returns (uint8 decimals) {
704:             // If call to Chainlink succeeds, record the current decimal precision
705:             ethBtcDecimals = decimals;
706:         } catch {
707:             // If call to Chainlink aggregator reverts, return a zero response with success = false
708:             return prevChainlinkResponse;
709:         }
710: 
711:         try STETH_ETH_CL_FEED.decimals() returns (uint8 decimals) {
712:             // If call to Chainlink succeeds, record the current decimal precision
713:             stEthEthDecimals = decimals;
714:         } catch {
715:             // If call to Chainlink aggregator reverts, return a zero response with success = false
716:             return prevChainlinkResponse;
717:         }
718: 
719:         // Try to get latest prices data from prev round:
720:         int256 ethBtcAnswer;
721:         int256 stEthEthAnswer;
722:         try ETH_BTC_CL_FEED.getRoundData(_currentRoundEthBtcId - 1) returns (
723:             uint80 roundId,
724:             int256 answer,
725:             uint256,
726:             /* startedAt */
727:             uint256 timestamp,
728:             uint80 /* answeredInRound */
729:         ) {
730:             ethBtcAnswer = answer;
731:             prevChainlinkResponse.roundEthBtcId = roundId;
732:             prevChainlinkResponse.timestampEthBtc = timestamp;
733:         } catch {
734:             // If call to Chainlink aggregator reverts, return a zero response with success = false
735:             return prevChainlinkResponse;
736:         }
737: 
738:         try STETH_ETH_CL_FEED.getRoundData(_currentRoundStEthEthId - 1) returns (
739:             uint80 roundId,
740:             int256 answer,
741:             uint256,
742:             /* startedAt */
743:             uint256 timestamp,
744:             uint80 /* answeredInRound */
745:         ) {
746:             stEthEthAnswer = answer;
747:             prevChainlinkResponse.roundStEthEthId = roundId;
748:             prevChainlinkResponse.timestampStEthEth = timestamp;
749:         } catch {
750:             // If call to Chainlink aggregator reverts, return a zero response with success = false
751:             return prevChainlinkResponse;
752:         }
753: 
754:         if (
755:             _checkHealthyCLResponse(prevChainlinkResponse.roundEthBtcId, ethBtcAnswer) &&
756:             _checkHealthyCLResponse(prevChainlinkResponse.roundStEthEthId, stEthEthAnswer)
757:         ) {
758:             prevChainlinkResponse.answer = _formatClAggregateAnswer(
759:                 ethBtcAnswer,
760:                 stEthEthAnswer,
761:                 ethBtcDecimals,
762:                 stEthEthDecimals
763:             );
764:         } else {
765:             return prevChainlinkResponse;
766:         }
767: 
768:         prevChainlinkResponse.success = true;
769:     }


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L606-L681) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L687-L769)


```solidity

File: packages/contracts/contracts/Dependencies/EbtcBase.sol

67:     function getSystemCollShares() public view returns (uint256 entireSystemColl) {
68:         return (activePool.getSystemCollShares());
69:     }

75:     function _getSystemDebt() internal view returns (uint256 entireSystemDebt) {
76:         return (activePool.getSystemDebt());
77:     }

83:     function _getTCRWithSystemDebtAndCollShares(
84:         uint256 _price
85:     ) internal view returns (uint256 TCR, uint256 _coll, uint256 _debt) {
86:         uint256 systemCollShares = getSystemCollShares();
87:         uint256 systemDebt = _getSystemDebt();
88: 
89:         uint256 _systemStEthBalance = collateral.getPooledEthByShares(systemCollShares);
90:         TCR = EbtcMath._computeCR(_systemStEthBalance, systemDebt, _price);
91: 
92:         return (TCR, systemCollShares, systemDebt);
93:     }


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L67-L69) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L75-L77), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L83-L93)


</details>


### [NC&#x2011;87] Contract declarations should have NatSpec `@dev` annotations 



*There are 30 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/EBTCToken.sol

26: contract EBTCToken is IEBTCToken, AuthNoOwner, PermitNonce {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L26-L26) 


```solidity

File: packages/contracts/contracts/Governor.sol

08: /// @notice Role based Authority that supports up to 256 roles.
09: /// @notice We have taken the tradeoff of additional storage usage for easier readabiliy without using off-chain / indexing services.
10: /// @author BadgerDAO Expanded from Solmate RolesAuthority
11: /// @author Modified from Solmate (https://github.com/transmissions11/solmate/blob/main/src/auth/authorities/RolesAuthority.sol)
12: /// @author Modified from Dappsys (https://github.com/dapphub/ds-roles/blob/master/src/roles.sol)
13: contract Governor is RolesAuthority {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L8-L13) 


```solidity

File: packages/contracts/contracts/PriceFeed.sol

21: contract PriceFeed is BaseMath, IPriceFeed, AuthNoOwner {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L21-L21) 


```solidity

File: packages/contracts/contracts/SortedCdps.sol

51: contract SortedCdps is ISortedCdps {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L51-L51) 


```solidity

File: packages/contracts/contracts/LeverageMacroBase.sol

14: interface ICdpCdps {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L14-L14) 


```solidity

File: packages/contracts/contracts/LeverageMacroDelegateTarget.sol

6: interface IOwnerLike {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L6-L6) 


```solidity

File: packages/contracts/contracts/LeverageMacroFactory.sol

08: /**
09:  * @title Factory for deploying LeverageMacros
10:  */


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroFactory.sol#L8-L10) 


```solidity

File: packages/contracts/contracts/Dependencies/Auth.sol

6: /// @notice Provides a flexible and updatable auth pattern which is completely separate from application logic.
7: /// @author Solmate (https://github.com/transmissions11/solmate/blob/main/src/auth/Auth.sol)
8: /// @author Modified from Dappsys (https://github.com/dapphub/ds-auth/blob/master/src/auth.sol)
9: abstract contract Auth {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/Auth.sol#L6-L9) 


```solidity

File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

06: /// @notice Provides a flexible and updatable auth pattern which is completely separate from application logic.
07: /// @author Modified by BadgerDAO to remove owner
08: /// @author Solmate (https://github.com/transmissions11/solmate/blob/main/src/auth/Auth.sol)
09: /// @author Modified from Dappsys (https://github.com/dapphub/ds-auth/blob/master/src/auth.sol)
10: contract AuthNoOwner {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L6-L10) 


```solidity

File: packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol

8: abstract contract ERC3156FlashLender is IERC3156FlashLender {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L8-L8) 


```solidity

File: packages/contracts/contracts/Dependencies/EbtcBase.sol

16: contract EbtcBase is BaseMath, IEbtcBase {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L16-L16) 


```solidity

File: packages/contracts/contracts/Dependencies/EbtcMath.sol

5: library EbtcMath {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcMath.sol#L5-L5) 


```solidity

File: packages/contracts/contracts/Dependencies/ReentrancyGuard.sol

4: /// @notice Gas optimized reentrancy protection for smart contracts.
5: /// @author Solmate (https://github.com/transmissions11/solmate/blob/main/src/utils/ReentrancyGuard.sol)
6: /// @author Modified from OpenZeppelin (https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/security/ReentrancyGuard.sol)
7: abstract contract ReentrancyGuard {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/ReentrancyGuard.sol#L4-L7) 


```solidity

File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

08: /// @notice Role based Authority that supports up to 256 roles.
09: /// @author BadgerDAO
10: /// @author Modified from Solmate (https://github.com/transmissions11/solmate/blob/main/src/auth/authorities/RolesAuthority.sol)
11: /// @author Modified from Dappsys (https://github.com/dapphub/ds-roles/blob/master/src/roles.sol)
12: contract RolesAuthority is IRolesAuthority, Auth, Authority {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L8-L12) 


```solidity

File: packages/contracts/contracts/Interfaces/IActivePool.sol

7: interface IActivePool is IPool {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IActivePool.sol#L7-L7) 


```solidity

File: packages/contracts/contracts/Interfaces/IBorrowerOperations.sol

7: interface IBorrowerOperations is IPositionManagers {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L7-L7) 


```solidity

File: packages/contracts/contracts/Interfaces/ICdpManager.sol

9: interface ICdpManager is IEbtcBase, ICdpManagerData {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManager.sol#L9-L9) 


```solidity

File: packages/contracts/contracts/Interfaces/ICdpManagerData.sol

13: interface ICdpManagerData is IRecoveryModeGracePeriod {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L13-L13) 


```solidity

File: packages/contracts/contracts/Interfaces/ICollSurplusPool.sol

5: interface ICollSurplusPool {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICollSurplusPool.sol#L5-L5) 


```solidity

File: packages/contracts/contracts/Interfaces/IEbtcBase.sol

7: interface IEbtcBase {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IEbtcBase.sol#L7-L7) 


```solidity

File: packages/contracts/contracts/Interfaces/IEBTCToken.sol

8: interface IEBTCToken is IERC20, IERC2612 {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IEBTCToken.sol#L8-L8) 


```solidity

File: packages/contracts/contracts/Interfaces/IERC3156FlashBorrower.sol

5: interface IERC3156FlashBorrower {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IERC3156FlashBorrower.sol#L5-L5) 


```solidity

File: packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol

7: interface IERC3156FlashLender {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol#L7-L7) 


```solidity

File: packages/contracts/contracts/Interfaces/IFallbackCaller.sol

5: interface IFallbackCaller {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IFallbackCaller.sol#L5-L5) 


```solidity

File: packages/contracts/contracts/Interfaces/IPermitNonce.sol

5: interface IPermitNonce {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPermitNonce.sol#L5-L5) 


```solidity

File: packages/contracts/contracts/Interfaces/IPool.sol

6: interface IPool {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPool.sol#L6-L6) 


```solidity

File: packages/contracts/contracts/Interfaces/IPositionManagers.sol

5: interface IPositionManagers {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPositionManagers.sol#L5-L5) 


```solidity

File: packages/contracts/contracts/Interfaces/IPriceFeed.sol

5: interface IPriceFeed {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPriceFeed.sol#L5-L5) 


```solidity

File: packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol

5: interface IRecoveryModeGracePeriod {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol#L5-L5) 


```solidity

File: packages/contracts/contracts/Interfaces/ISortedCdps.sol

6: interface ISortedCdps {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ISortedCdps.sol#L6-L6) 


</details>


### [NC&#x2011;88] Contract should expose an `interface` 
The `contract`s should expose an `interface` so that other projects can more easily integrate with it, without having to develop their own non-standard variants.


*There are 81 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/ActivePool.sol

371:     function sweepToken(address token, uint256 amount) public nonReentrant requiresAuth {

390:     function setFeeRecipientAddress(address _feeRecipientAddress) external requiresAuth {

404:     function setFeeBps(uint256 _newFee) external requiresAuth {

417:     function setFlashLoansPaused(bool _paused) external requiresAuth {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L371-L371) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L390-L390), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L404-L404), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L417-L417)


```solidity

File: packages/contracts/contracts/BorrowerOperations.sol

659:     function DOMAIN_SEPARATOR() external view returns (bytes32) {

1140:     function setFeeRecipientAddress(address _feeRecipientAddress) external requiresAuth {

1154:     function setFeeBps(uint256 _newFee) external requiresAuth {

1167:     function setFlashLoansPaused(bool _paused) external requiresAuth {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L659-L659) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L1140-L1140), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L1154-L1154), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L1167-L1167)


```solidity

File: packages/contracts/contracts/CdpManager.sol

570:     function getSystemDebt() public view returns (uint256 entireSystemDebt) {

717:     function getDeploymentStartTime() public view returns (uint256) {

727:     function checkPotentialRecoveryMode(

773:     function setStakingRewardSplit(uint256 _stakingRewardSplit) external requiresAuth {

788:     function setRedemptionFeeFloor(uint256 _redemptionFeeFloor) external requiresAuth {

807:     function setMinuteDecayFactor(uint256 _minuteDecayFactor) external requiresAuth {

830:     function setBeta(uint256 _beta) external requiresAuth {

843:     function setRedemptionsPaused(bool _paused) external requiresAuth {

905:     function initializeCdp(

946:     function updateCdp(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L570-L570) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L717-L717), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L727-L727), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L773-L773), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L788-L788), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L807-L807), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L830-L830), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L843-L843), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L905-L905), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L946-L946)


```solidity

File: packages/contracts/contracts/LiquidationLibrary.sol

40:     function liquidate(bytes32 _cdpId) external nonReentrantSelfAndBOps {

50:     function partiallyLiquidate(

679:     function batchLiquidateCdps(bytes32[] memory _cdpArray) external nonReentrantSelfAndBOps {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L40-L40) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L50-L50), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L679-L679)


```solidity

File: packages/contracts/contracts/CdpManagerStorage.sol

32:     function notifyStartGracePeriod(uint256 tcr) external {

42:     function notifyEndGracePeriod(uint256 tcr) external {

111:     function setGracePeriod(uint128 _gracePeriod) external requiresAuth {

504:     function syncGlobalAccounting() external {

527:     function syncGlobalAccountingAndGracePeriod() public {

552:     function calcFeeUponStakingReward(

616:     function getAccumulatedFeeSplitApplied(

673:     function getCachedNominalICR(bytes32 _cdpId) external view returns (uint256) {

684:     function getSyncedNominalICR(bytes32 _cdpId) external view returns (uint256) {

701:     function getCachedICR(bytes32 _cdpId, uint256 _price) public view returns (uint256) {

719:     function getPendingRedistributedDebt(

728:     function hasPendingRedistributedDebt(bytes32 _cdpId) public view returns (bool) {

745:     function getSyncedDebtAndCollShares(

839:     function getSyncedCdpDebt(bytes32 _cdpId) public view returns (uint256) {

848:     function getSyncedCdpCollShares(bytes32 _cdpId) public view returns (uint256) {

864:     function getSyncedICR(bytes32 _cdpId, uint256 _price) public view returns (uint256) {

874:     function getSyncedTCR(uint256 _price) public view returns (uint256) {

890:     function canLiquidateRecoveryMode(uint256 icr, uint256 tcr) public view returns (bool) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L32-L32) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L42-L42), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L111-L111), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L504-L504), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L527-L527), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L552-L552), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L616-L616), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L673-L673), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L684-L684), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L701-L701), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L719-L719), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L728-L728), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L745-L745), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L839-L839), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L848-L848), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L864-L864), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L874-L874), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L890-L890)


```solidity

File: packages/contracts/contracts/CollSurplusPool.sol

142:     function sweepToken(address token, uint256 amount) public nonReentrant requiresAuth {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L142-L142) 


```solidity

File: packages/contracts/contracts/EBTCToken.sol

104:     function burn(uint256 _amount) external {

176:     function DOMAIN_SEPARATOR() external view returns (bytes32) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L104-L104) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L176-L176)


```solidity

File: packages/contracts/contracts/Governor.sol

43:     function getUsersByRole(uint8 role) external view returns (address[] memory usersWithRole) {

73:     function getRolesForUser(address user) external view returns (uint8[] memory rolesForUser) {

96:     function getRolesFromByteMap(bytes32 byteMap) public pure returns (uint8[] memory roleIds) {

120:     function getByteMapFromRoles(uint8[] memory roleIds) public pure returns (bytes32) {

131:     function getEnabledFunctionsInTarget(

146:     function getRoleName(uint8 role) external view returns (string memory roleName) {

154:     function setRoleName(uint8 role, string memory roleName) external requiresAuth {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L43-L43) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L73-L73), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L96-L96), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L120-L120), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L131-L131), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L146-L146), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L154-L154)


```solidity

File: packages/contracts/contracts/PriceFeed.sol

358:     function setFallbackCaller(address _fallbackCaller) external requiresAuth {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L358-L358) 


```solidity

File: packages/contracts/contracts/SortedCdps.sol

105:     function toCdpId(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L105-L105) 


```solidity

File: packages/contracts/contracts/HintHelpers.sol

48:     function getRedemptionHints(

164:     function getApproxHint(

203:     function computeNominalCR(uint256 _coll, uint256 _debt) external pure returns (uint256) {

212:     function computeCR(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L48-L48) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L164-L164), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L203-L203), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L212-L212)


```solidity

File: packages/contracts/contracts/LeverageMacroBase.sol

39:     function owner() public virtual returns (address) {

118:     function doOperation(

214:     function sweepToCaller() public {

234:     function sweepToken(address token, uint256 amount) public {

338:     function decodeFLData(bytes calldata data) public view returns (LeverageMacroOperation memory) {

344:     function onFlashLoan(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L39-L39) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L118-L118), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L214-L214), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L234-L234), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L338-L338), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L344-L344)


```solidity

File: packages/contracts/contracts/LeverageMacroFactory.sol

38:     function deployNewMacro() external returns (address) {

43:     function deployNewMacro(address _owner) public returns (address) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroFactory.sol#L38-L38) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroFactory.sol#L43-L43)


```solidity

File: packages/contracts/contracts/LeverageMacroReference.sol

50:     function resetApprovals() external {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroReference.sol#L50-L50) 


```solidity

File: packages/contracts/contracts/SimplifiedDiamondLike.sol

51:     function setFallbackHandler(bytes4 sig, address handler) external {

66:     function setAllowAnyCall(bool allowNonCallbacks) external {

76:     function enableCallbackForCall() external {

110:     function execute(Operation[] calldata ops) external payable {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L51-L51) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L66-L66), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L76-L76), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L110-L110)


```solidity

File: packages/contracts/contracts/Dependencies/Auth.sol

42:     function setAuthority(Authority newAuthority) public virtual {

52:     function transferOwnership(address newOwner) public virtual requiresAuth {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/Auth.sol#L42-L42) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/Auth.sol#L52-L52)


```solidity

File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

22:     function authority() public view returns (Authority) {

26:     function authorityInitialized() public view returns (bool) {

38:     function setAuthority(address newAuthority) public virtual {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L22-L22) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L26-L26), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L38-L38)


```solidity

File: packages/contracts/contracts/Dependencies/EbtcBase.sol

67:     function getSystemCollShares() public view returns (uint256 entireSystemColl) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L67-L67) 


```solidity

File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

38:     function doesUserHaveRole(address user, uint8 role) public view virtual returns (bool) {

42:     function doesRoleHaveCapability(

50:     function isPublicCapability(address target, bytes4 functionSig) public view returns (bool) {

85:     function setPublicCapability(

106:     function setRoleCapability(

133:     function burnCapability(address target, bytes4 functionSig) public virtual requiresAuth {

147:     function setUserRole(address user, uint8 role, bool enabled) public virtual requiresAuth {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L38-L38) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L42-L42), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L50-L50), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L85-L85), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L106-L106), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L133-L133), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L147-L147)


</details>


### [NC&#x2011;89] Named imports of parent contracts are missing 



*There are 1 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

//@audit `ICdpManagerData`
19: contract CdpManagerStorage is EbtcBase, ReentrancyGuard, ICdpManagerData, AuthNoOwner {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L19-L19) 


</details>


### [NC&#x2011;90] Contract declarations should have NatSpec `@notice` annotations 



*There are 28 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

11: /// @title LiquidationLibrary mainly provide necessary logic to fulfill liquidation for eBTC Cdps.
12: /// @dev This contract shares same base and storage layout with CdpManager and is the delegatecall destination from CdpManager
13: contract LiquidationLibrary is CdpManagerStorage {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L11-L13) 


```solidity

File: packages/contracts/contracts/CdpManagerStorage.sol

14: /// @title CDP Manager storage and shared functions with LiquidationLibrary
15: /// @dev All features around Cdp management are split into separate parts to get around contract size limitations.
16: /// @dev Liquidation related functions are delegated to LiquidationLibrary contract code.
17: /// @dev Both CdpManager and LiquidationLibrary must maintain **the same storage layout**, so shared storage components
18: /// @dev and shared functions are added here in CdpManagerStorage to de-dup code
19: contract CdpManagerStorage is EbtcBase, ReentrancyGuard, ICdpManagerData, AuthNoOwner {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L14-L19) 


```solidity

File: packages/contracts/contracts/EBTCToken.sol

26: contract EBTCToken is IEBTCToken, AuthNoOwner, PermitNonce {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L26-L26) 


```solidity

File: packages/contracts/contracts/PriceFeed.sol

21: contract PriceFeed is BaseMath, IPriceFeed, AuthNoOwner {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L21-L21) 


```solidity

File: packages/contracts/contracts/SortedCdps.sol

51: contract SortedCdps is ISortedCdps {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L51-L51) 


```solidity

File: packages/contracts/contracts/HintHelpers.sol

09: /// @title HintHelpers mainly serves to provide handy information to facilitate offchain integration like redemption bots.
10: /// @dev It is strongly recommended to use HintHelper for redemption purpose
11: contract HintHelpers is EbtcBase {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L9-L11) 


```solidity

File: packages/contracts/contracts/LeverageMacroBase.sol

14: interface ICdpCdps {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L14-L14) 


```solidity

File: packages/contracts/contracts/LeverageMacroDelegateTarget.sol

6: interface IOwnerLike {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L6-L6) 


```solidity

File: packages/contracts/contracts/LeverageMacroFactory.sol

08: /**
09:  * @title Factory for deploying LeverageMacros
10:  */


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroFactory.sol#L8-L10) 


```solidity

File: packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol

8: abstract contract ERC3156FlashLender is IERC3156FlashLender {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L8-L8) 


```solidity

File: packages/contracts/contracts/Dependencies/EbtcBase.sol

16: contract EbtcBase is BaseMath, IEbtcBase {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L16-L16) 


```solidity

File: packages/contracts/contracts/Dependencies/EbtcMath.sol

5: library EbtcMath {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcMath.sol#L5-L5) 


```solidity

File: packages/contracts/contracts/Interfaces/IActivePool.sol

7: interface IActivePool is IPool {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IActivePool.sol#L7-L7) 


```solidity

File: packages/contracts/contracts/Interfaces/IBorrowerOperations.sol

7: interface IBorrowerOperations is IPositionManagers {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L7-L7) 


```solidity

File: packages/contracts/contracts/Interfaces/ICdpManager.sol

9: interface ICdpManager is IEbtcBase, ICdpManagerData {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManager.sol#L9-L9) 


```solidity

File: packages/contracts/contracts/Interfaces/ICdpManagerData.sol

13: interface ICdpManagerData is IRecoveryModeGracePeriod {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L13-L13) 


```solidity

File: packages/contracts/contracts/Interfaces/ICollSurplusPool.sol

5: interface ICollSurplusPool {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICollSurplusPool.sol#L5-L5) 


```solidity

File: packages/contracts/contracts/Interfaces/IEbtcBase.sol

7: interface IEbtcBase {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IEbtcBase.sol#L7-L7) 


```solidity

File: packages/contracts/contracts/Interfaces/IEBTCToken.sol

8: interface IEBTCToken is IERC20, IERC2612 {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IEBTCToken.sol#L8-L8) 


```solidity

File: packages/contracts/contracts/Interfaces/IERC3156FlashBorrower.sol

5: interface IERC3156FlashBorrower {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IERC3156FlashBorrower.sol#L5-L5) 


```solidity

File: packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol

7: interface IERC3156FlashLender {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol#L7-L7) 


```solidity

File: packages/contracts/contracts/Interfaces/IFallbackCaller.sol

5: interface IFallbackCaller {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IFallbackCaller.sol#L5-L5) 


```solidity

File: packages/contracts/contracts/Interfaces/IPermitNonce.sol

5: interface IPermitNonce {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPermitNonce.sol#L5-L5) 


```solidity

File: packages/contracts/contracts/Interfaces/IPool.sol

6: interface IPool {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPool.sol#L6-L6) 


```solidity

File: packages/contracts/contracts/Interfaces/IPositionManagers.sol

5: interface IPositionManagers {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPositionManagers.sol#L5-L5) 


```solidity

File: packages/contracts/contracts/Interfaces/IPriceFeed.sol

5: interface IPriceFeed {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPriceFeed.sol#L5-L5) 


```solidity

File: packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol

5: interface IRecoveryModeGracePeriod {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol#L5-L5) 


```solidity

File: packages/contracts/contracts/Interfaces/ISortedCdps.sol

6: interface ISortedCdps {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ISortedCdps.sol#L6-L6) 


</details>


### [NC&#x2011;91] Do not use UNDERSCORE in `struct` elements names 
For better maintainability, please consider creating and using a constant for those strings instead of hardcoding 


*There are 3 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

//@audit remove underscore from `_upperHint`, `_lowerHint`, 
313:     struct OpenCdpOperation {
314:         // Open CDP For Data
315:         uint256 eBTCToMint;
316:         bytes32 _upperHint;
317:         bytes32 _lowerHint;
318:         uint256 stETHToDeposit;
319:     }

//@audit remove underscore from `_cdpId`, `_stEthBalanceDecrease`, `_EBTCChange`, `_isDebtIncrease`, `_upperHint`, `_lowerHint`, `_stEthBalanceIncrease`, 
322:     struct AdjustCdpOperation {
323:         bytes32 _cdpId;
324:         uint256 _stEthBalanceDecrease;
325:         uint256 _EBTCChange;
326:         bool _isDebtIncrease;
327:         bytes32 _upperHint;
328:         bytes32 _lowerHint;
329:         uint256 _stEthBalanceIncrease;
330:     }

//@audit remove underscore from `_cdpId`, 
333:     struct CloseCdpOperation {
334:         bytes32 _cdpId;
335:     }


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L313-L319) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L322-L330), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L333-L335)


</details>


### [NC&#x2011;92] `event` declarations should have NatSpec descriptions 



*There are 55 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/Governor.sol

32:     event RoleNameSet(uint8 indexed role, string indexed name);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L32-L32) 


```solidity

File: packages/contracts/contracts/LeverageMacroFactory.sol

19:     event DeployNewMacro(address indexed sender, address indexed newContractAddress);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroFactory.sol#L19-L19) 


```solidity

File: packages/contracts/contracts/Dependencies/Auth.sol

10:     event OwnershipTransferred(address indexed user, address indexed newOwner);

12:     event AuthorityUpdated(address indexed user, Authority indexed newAuthority);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/Auth.sol#L10-L10) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/Auth.sol#L12-L12)


```solidity

File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

11:     event AuthorityUpdated(address indexed user, Authority indexed newAuthority);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L11-L11) 


```solidity

File: packages/contracts/contracts/Interfaces/IActivePool.sol

9:     event ActivePoolEBTCDebtUpdated(uint256 _EBTCDebt);

10:     event SystemCollSharesUpdated(uint256 _coll);

11:     event FeeRecipientAddressChanged(address indexed _feeRecipientAddress);

12:     event FeeRecipientClaimableCollSharesIncreased(uint256 _coll, uint256 _fee);

13:     event FeeRecipientClaimableCollSharesDecreased(uint256 _coll, uint256 _fee);

14:     event FlashLoanSuccess(

20:     event SweepTokenSuccess(address indexed _token, uint256 _amount, address indexed _recipient);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IActivePool.sol#L9-L9) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IActivePool.sol#L10-L10), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IActivePool.sol#L11-L11), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IActivePool.sol#L12-L12), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IActivePool.sol#L13-L13), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IActivePool.sol#L14-L14), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IActivePool.sol#L20-L20)


```solidity

File: packages/contracts/contracts/Interfaces/IBorrowerOperations.sol

10:     event FeeRecipientAddressChanged(address indexed _feeRecipientAddress);

11:     event FlashLoanSuccess(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L10-L10) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L11-L11)


```solidity

File: packages/contracts/contracts/Interfaces/ICdpManagerData.sol

16:     event FeeRecipientAddressChanged(address indexed _feeRecipientAddress);

17:     event StakingRewardSplitSet(uint256 _stakingRewardSplit);

18:     event RedemptionFeeFloorSet(uint256 _redemptionFeeFloor);

19:     event MinuteDecayFactorSet(uint256 _minuteDecayFactor);

20:     event BetaSet(uint256 _beta);

21:     event RedemptionsPaused(bool _paused);

23:     event Liquidation(uint256 _liquidatedDebt, uint256 _liquidatedColl, uint256 _liqReward);

24:     event Redemption(

31:     event CdpUpdated(

42:     event CdpLiquidated(

51:     event CdpPartiallyLiquidated(

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


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L16-L16) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L17-L17), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L18-L18), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L19-L19), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L20-L20), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L21-L21), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L23-L23), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L24-L24), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L31-L31), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L42-L42), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L51-L51), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L60-L60), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L61-L61), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L62-L62), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L63-L63), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L64-L64), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L65-L65), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L66-L66), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L67-L67), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L68-L68), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L69-L69)


```solidity

File: packages/contracts/contracts/Interfaces/ICollSurplusPool.sol

8:     event SurplusCollSharesUpdated(address indexed _account, uint256 _newBalance);

9:     event CollSharesTransferred(address indexed _to, uint256 _amount);

11:     event SweepTokenSuccess(address indexed _token, uint256 _amount, address indexed _recipient);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICollSurplusPool.sol#L8-L8) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICollSurplusPool.sol#L9-L9), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICollSurplusPool.sol#L11-L11)


```solidity

File: packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol

8:     event FlashFeeSet(address indexed _setter, uint256 _oldFee, uint256 _newFee);

9:     event MaxFlashFeeSet(address indexed _setter, uint256 _oldMaxFee, uint256 _newMaxFee);

10:     event FlashLoansPaused(address indexed _setter, bool _paused);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol#L8-L8) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol#L9-L9), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol#L10-L10)


```solidity

File: packages/contracts/contracts/Interfaces/IFallbackCaller.sol

7:     event FallbackTimeOutChanged(uint256 _oldTimeOut, uint256 _newTimeOut);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IFallbackCaller.sol#L7-L7) 


```solidity

File: packages/contracts/contracts/Interfaces/IPool.sol

9:     event ETHBalanceUpdated(uint256 _newBalance);

10:     event EBTCBalanceUpdated(uint256 _newBalance);

11:     event CollSharesTransferred(address indexed _to, uint256 _amount);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPool.sol#L9-L9) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPool.sol#L10-L10), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPool.sol#L11-L11)


```solidity

File: packages/contracts/contracts/Interfaces/IPositionManagers.sol

12:     event PositionManagerApprovalSet(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPositionManagers.sol#L12-L12) 


```solidity

File: packages/contracts/contracts/Interfaces/IPriceFeed.sol

7:     event LastGoodPriceUpdated(uint256 _lastGoodPrice);

8:     event PriceFeedStatusChanged(Status newStatus);

9:     event FallbackCallerChanged(

13:     event UnhealthyFallbackCaller(address indexed _fallbackCaller, uint256 timestamp);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPriceFeed.sol#L7-L7) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPriceFeed.sol#L8-L8), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPriceFeed.sol#L9-L9), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPriceFeed.sol#L13-L13)


```solidity

File: packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol

6:     event TCRNotified(uint256 TCR); /// NOTE: Mostly for debugging to ensure synch

10:     event GracePeriodEnd();

11:     event GracePeriodDurationSet(uint256 _recoveryModeGracePeriodDuration);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol#L6-L6) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol#L10-L10), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol#L11-L11)


```solidity

File: packages/contracts/contracts/Interfaces/ISortedCdps.sol

9:     event NodeAdded(bytes32 _id, uint _NICR);

10:     event NodeRemoved(bytes32 _id);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ISortedCdps.sol#L9-L9) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ISortedCdps.sol#L10-L10)


</details>


### [NC&#x2011;93] Events should use parameters to convey information 
For example, rather than using `event Paused()` and `event Unpaused()`, use `event PauseState(address indexed whoChangedIt, bool wasPaused, bool isNowPaused)`


*There are 2 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol

9:     event GracePeriodStart();

10:     event GracePeriodEnd();


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol#L9-L9) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol#L10-L10)


</details>


### [NC&#x2011;94] `function` names should use lowerCamelCase 
Here is an example of camelCase/lowerCamelCase and other types:
'helloWorld' is a CamelCase
'HelloWorld' is Not CamelCase (PascalCase)
'hello_world' is Not CamelCase (snake_case)
[For more details](https://khalilstemmler.com/blogs/camel-case-snake-case-pascal-case/)


*There are 23 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/ActivePool.sol

//@audit `` is not in CamelCase
46:     constructor(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L46-L46) 


```solidity

File: packages/contracts/contracts/BorrowerOperations.sol

//@audit `` is not in CamelCase
107:     constructor(

//@audit `DOMAIN_SEPARATOR` is not in CamelCase
659:     function DOMAIN_SEPARATOR() external view returns (bytes32) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L107-L107) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L659-L659)


```solidity

File: packages/contracts/contracts/CdpManager.sol

//@audit `` is not in CamelCase
30:     constructor(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L30-L30) 


```solidity

File: packages/contracts/contracts/LiquidationLibrary.sol

//@audit `` is not in CamelCase
14:     constructor(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L14-L14) 


```solidity

File: packages/contracts/contracts/CdpManagerStorage.sol

//@audit `` is not in CamelCase
217:     constructor(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L217-L217) 


```solidity

File: packages/contracts/contracts/CollSurplusPool.sol

//@audit `` is not in CamelCase
42:     constructor(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L42-L42) 


```solidity

File: packages/contracts/contracts/EBTCToken.sol

//@audit `` is not in CamelCase
61:     constructor(

//@audit `DOMAIN_SEPARATOR` is not in CamelCase
176:     function DOMAIN_SEPARATOR() external view returns (bytes32) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L61-L61) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L176-L176)


```solidity

File: packages/contracts/contracts/Governor.sol

//@audit `` is not in CamelCase
36:     constructor(address _owner) RolesAuthority(_owner, Authority(address(this))) {}


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L36-L36) 


```solidity

File: packages/contracts/contracts/PriceFeed.sol

//@audit `` is not in CamelCase
57:     constructor(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L57-L57) 


```solidity

File: packages/contracts/contracts/SortedCdps.sol

//@audit `` is not in CamelCase
88:     constructor(uint256 _size, address _cdpManagerAddress, address _borrowerOperationsAddress) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L88-L88) 


```solidity

File: packages/contracts/contracts/HintHelpers.sol

//@audit `` is not in CamelCase
27:     constructor(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L27-L27) 


```solidity

File: packages/contracts/contracts/LeverageMacroBase.sol

//@audit `Cdps` is not in CamelCase
15:     function Cdps(bytes32) external view returns (ICdpManagerData.Cdp memory);

//@audit `` is not in CamelCase
51:     constructor(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L15-L15) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L51-L51)


```solidity

File: packages/contracts/contracts/LeverageMacroDelegateTarget.sol

//@audit `` is not in CamelCase
41:     constructor(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L41-L41) 


```solidity

File: packages/contracts/contracts/LeverageMacroFactory.sol

//@audit `` is not in CamelCase
21:     constructor(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroFactory.sol#L21-L21) 


```solidity

File: packages/contracts/contracts/LeverageMacroReference.sol

//@audit `` is not in CamelCase
17:     constructor(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroReference.sol#L17-L17) 


```solidity

File: packages/contracts/contracts/SimplifiedDiamondLike.sol

//@audit `` is not in CamelCase
44:     constructor(address _owner) {

//@audit `` is not in CamelCase
160:     receive() external payable {

//@audit `` is not in CamelCase
164:     fallback() external payable {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L44-L44) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L160-L160), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L164-L164)


```solidity

File: packages/contracts/contracts/Dependencies/EbtcBase.sol

//@audit `` is not in CamelCase
52:     constructor(address _activePoolAddress, address _priceFeedAddress, address _collateralAddress) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L52-L52) 


```solidity

File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

//@audit `` is not in CamelCase
20:     constructor(address _owner, Authority _authority) Auth(_owner, _authority) {}


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L20-L20) 


</details>


### [NC&#x2011;95] Expressions for constant values should use `immutable` rather than `constant` 
While it does not save gas for some simple binary expressions because the compiler knows that developers often make this mistake, it's still best to use the right tool for the task at hand. There is a difference between `constant` variables and `immutable` variables, and they should each be used in their appropriate contexts. `constants` should be used for literal values written into the code, and `immutable` variables should be used for expressions, or values calculated in, or passed into the constructor.


*There are 5 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

32:     bytes32 private constant _PERMIT_POSITION_MANAGER_TYPEHASH =
33:         keccak256(
34:             "PermitPositionManagerApproval(address borrower,address positionManager,uint8 status,uint256 nonce,uint256 deadline)"
35:         );


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L32-L35) 


```solidity

File: packages/contracts/contracts/CdpManagerStorage.sol

141:     uint256 public constant MIN_REDEMPTION_FEE_FLOOR = (DECIMAL_PRECISION * 5) / 1000; // 0.5%


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L141-L141) 


```solidity

File: packages/contracts/contracts/LeverageMacroBase.sol

37:     bytes32 constant FLASH_LOAN_SUCCESS = keccak256("ERC3156FlashBorrower.onFlashLoan");


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L37-L37) 


```solidity

File: packages/contracts/contracts/SimplifiedDiamondLike.sol

39:     bytes32 constant DIAMOND_STORAGE_POSITION = keccak256("diamond.standard.diamond.storage");


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L39-L39) 


```solidity

File: packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol

11:     bytes32 public constant FLASH_SUCCESS_VALUE = keccak256("ERC3156FlashBorrower.onFlashLoan");


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L11-L11) 


</details>


### [NC&#x2011;96] `struct` names should use CamelCase 



*There are 3 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/HintHelpers.sol

//@audit `LocalVariables_getRedemptionHints` is not in CamelCase
19:     struct LocalVariables_getRedemptionHints {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L19-L19) 


```solidity

File: packages/contracts/contracts/Interfaces/ICdpManagerData.sol

//@audit `LocalVariables_OuterLiquidationFunction` is not in CamelCase
147:     struct LocalVariables_OuterLiquidationFunction {

//@audit `LocalVariables_LiquidationSequence` is not in CamelCase
154:     struct LocalVariables_LiquidationSequence {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L147-L147) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L154-L154)


</details>


### [NC&#x2011;97] `immutable` variable names don\'t follow the Solidity style guide 
For `immutable` variable names, each word should use all capital letters, with underscores separating each word (CONSTANT_CASE)


*There are 44 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/ActivePool.sol

26:     address public immutable borrowerOperationsAddress;

27:     address public immutable cdpManagerAddress;

28:     address public immutable collSurplusPoolAddress;

34:     ICollateralToken public immutable collateral;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L26-L26) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L27-L27), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L28-L28), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L34-L34)


```solidity

File: packages/contracts/contracts/BorrowerOperations.sol

53:     ICdpManager public immutable cdpManager;

55:     ICollSurplusPool public immutable collSurplusPool;

59:     IEBTCToken public immutable ebtcToken;

62:     ISortedCdps public immutable sortedCdps;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L53-L53) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L55-L55), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L59-L59), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L62-L62)


```solidity

File: packages/contracts/contracts/CdpManagerStorage.sol

126:     address public immutable borrowerOperationsAddress;

128:     ICollSurplusPool immutable collSurplusPool;

130:     IEBTCToken public immutable override ebtcToken;

132:     address public immutable liquidationLibrary;

135:     ISortedCdps public immutable sortedCdps;

152:     uint256 internal immutable deploymentStartTime;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L126-L126) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L128-L128), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L130-L130), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L132-L132), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L135-L135), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L152-L152)


```solidity

File: packages/contracts/contracts/CollSurplusPool.sol

21:     address public immutable borrowerOperationsAddress;

22:     address public immutable cdpManagerAddress;

23:     address public immutable activePoolAddress;

24:     address public immutable feeRecipientAddress;

25:     ICollateralToken public immutable collateral;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L21-L21) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L22-L22), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L23-L23), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L24-L24), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L25-L25)


```solidity

File: packages/contracts/contracts/EBTCToken.sol

55:     address public immutable cdpManagerAddress;

56:     address public immutable borrowerOperationsAddress;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L55-L55) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L56-L56)


```solidity

File: packages/contracts/contracts/SortedCdps.sol

54:     address public immutable borrowerOperationsAddress;

56:     ICdpManager public immutable cdpManager;

58:     uint256 public immutable maxSize;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L54-L54) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L56-L56), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L58-L58)


```solidity

File: packages/contracts/contracts/HintHelpers.sol

14:     ISortedCdps public immutable sortedCdps;

15:     ICdpManager public immutable cdpManager;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L14-L14) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L15-L15)


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

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L29-L29) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L30-L30), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L31-L31), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L32-L32), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L33-L33), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L34-L34), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L35-L35)


```solidity

File: packages/contracts/contracts/LeverageMacroFactory.sol

12:     address public immutable borrowerOperations;

13:     address public immutable activePool;

14:     address public immutable cdpManager;

15:     address public immutable ebtcToken;

16:     address public immutable stETH;

17:     address public immutable sortedCdps;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroFactory.sol#L12-L12) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroFactory.sol#L13-L13), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroFactory.sol#L14-L14), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroFactory.sol#L15-L15), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroFactory.sol#L16-L16), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroFactory.sol#L17-L17)


```solidity

File: packages/contracts/contracts/LeverageMacroReference.sol

12:     address internal immutable theOwner;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroReference.sol#L12-L12) 


```solidity

File: packages/contracts/contracts/SimplifiedDiamondLike.sol

42:     address public immutable owner;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L42-L42) 


```solidity

File: packages/contracts/contracts/Dependencies/EbtcBase.sol

41:     IActivePool public immutable activePool;

43:     IPriceFeed public immutable override priceFeed;

46:     ICollateralToken public immutable collateral;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L41-L41) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L43-L43), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L46-L46)


</details>


### [NC&#x2011;98] `private`/`public` function name should start with underscore 
According to solidity style guide, Private or Public function name should start with underscore.


*There are 5 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

//@audit `excessivelySafeCall` is not in CamelCase
498:     function excessivelySafeCall(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L498-L498) 


```solidity

File: packages/contracts/contracts/Dependencies/Auth.sol

//@audit `` is not in CamelCase
18:     constructor(address _owner, Authority _authority) {

//@audit `isAuthorized` is not in CamelCase
32:     function isAuthorized(address user, bytes4 functionSig) internal view virtual returns (bool) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/Auth.sol#L18-L18) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/Auth.sol#L32-L32)


```solidity

File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

//@audit `isAuthorized` is not in CamelCase
30:     function isAuthorized(address user, bytes4 functionSig) internal view virtual returns (bool) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L30-L30) 


```solidity

File: packages/contracts/contracts/Dependencies/EbtcMath.sol

//@audit `decMul` is not in CamelCase
35:     function decMul(uint256 x, uint256 y) internal pure returns (uint256 decProd) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcMath.sol#L35-L35) 


</details>


### [NC&#x2011;99] NatSpec: `Modifier` declarations should have descriptions 
It is recommended that Solidity contracts are fully annotated using NatSpec for all public interfaces (everything in the ABI). It is clearly stated in the Solidity official documentation. In complex projects such as Defi, the interpretation of all functions and their arguments and returns is important for code readability and auditability.[source](https://docs.soliditylang.org/en/v0.8.15/natspec-format.html)


*There are 3 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

26:     modifier requiresAuth() virtual {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/Auth.sol#L26-L26) 


```solidity

File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

16:     modifier requiresAuth() virtual {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L16-L16) 


```solidity

File: packages/contracts/contracts/Dependencies/ReentrancyGuard.sol

13:     modifier nonReentrant() virtual {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/ReentrancyGuard.sol#L13-L13) 


</details>


### [NC&#x2011;100] `pure` function accesses storage 
While the compiler currently flags functions like these as being `pure`, this is a [bug](https://github.com/ethereum/solidity/issues/11573) which will be fixed in a future version, so it's best to not use `pure` visibility, in order to not break when this bug is fixed.


*There are 1 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

83:     function _getStorage() internal pure returns (DiamondLikeStorage storage ds) {
84:         bytes32 position = DIAMOND_STORAGE_POSITION;
85:         assembly {
86:             ds.slot := position
87:         }
88:     }


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L83-L88) 


</details>


### [NC&#x2011;101] Assembly block creates dirty bits 
Writing data to the free memory pointer without later updating the free memory pointer will cause there to be dirty bits at that memory location. Not updating the free memory pointer will make it [harder](https://docs.soliditylang.org/en/latest/ir-breaking-changes.html#cleanup) for the optimizer to reason about whether the memory needs to be cleaned, which may lead to worse optimizations. Annotate the block with `assembly ("memory-safe") { ... }` if the memory's value can be discarded. If the memory needs to be saved, update the free memory pointer in addtion to using the annotation. See [this](https://docs.soliditylang.org/en/latest/assembly.html#memory-safety) link for other cases where the annotation can be used


*There are 3 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

513:         assembly {
514:             _success := call(
515:                 _gas, // gas
516:                 _target, // recipient
517:                 _value, // ether value
518:                 add(_calldata, 0x20), // inloc
519:                 mload(_calldata), // inlen
520:                 0, // outloc
521:                 0 // outlen
522:             )
523:             // limit our copy to 256 bytes
524:             _toCopy := returndatasize()
525:             if gt(_toCopy, _maxCopy) {
526:                 _toCopy := _maxCopy
527:             }
528:             // Store the length of the copied bytes
529:             mstore(_returnData, _toCopy)
530:             // copy the bytes from returndata[0:_toCopy]
531:             returndatacopy(add(_returnData, 0x20), 0, _toCopy)
532:         }


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L513-L532) 


```solidity

File: packages/contracts/contracts/SimplifiedDiamondLike.sol

148:             assembly {
149:                 success := call(txGas, to, value, add(data, 0x20), mload(data), 0, 0)
150:             }

143:             assembly {
144:                 success := delegatecall(txGas, to, add(data, 0x20), mload(data), 0, 0)
145:             }


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L148-L150) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L143-L145)


</details>
