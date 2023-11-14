## [L-01] _safeMint() should be used rather than _mint() wherever possible
_mint() is [discouraged](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/d4d8d2ed9798cc3383912a23b5e8d5cb602f7d4b/contracts/token/ERC721/ERC721.sol#L271) in favor of _safeMint() which ensures that the recipient is either an EOA or implements IERC721Receiver. Both open [OpenZeppelin](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/d4d8d2ed9798cc3383912a23b5e8d5cb602f7d4b/contracts/token/ERC721/ERC721.sol#L238-L250) and [solmate](https://github.com/Rari-Capital/solmate/blob/4eaf6b68202e36f67cab379768ac6be304c8ebde/src/tokens/ERC721.sol#L180) have versions of this function so that NFTs aren’t lost if they’re minted to contracts that cannot transfer them back out.

```solidity
File:  packages/contracts/contracts/EBTCToken.sol
87   _mint(_account, _amount);
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L87


## [L‑02] Use Ownable2Step instead of Ownable
Ownable2Step and Ownable2StepUpgradeable prevent the contract ownership from mistakenly being transferred to an address that cannot handle it (e.g. due to a typo in the address), by requiring that the recipient of the owner permissions actively accept via a contract call of its own.

```solidity
File:  packages/contracts/contracts/BorrowerOperations.sol
13  import "./Dependencies/Ownable.sol";
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L13

## [L-03] no check if the burn amount is zero or not
if the amount is zero so the unhecked block will divided zero on 3 and we use gas for nothing ! if we set zero we may pass the _burn checks, i know it is passed by only permit but it's better to avoid this happen because it's seting by human and it means it can be set with 0 balance to burn !

```solidity
File:  packages/contracts/contracts/BorrowerOperations.sol
798  ebtcToken.burn(_account, _debt);

1103  ebtcToken.burn(feeRecipientAddress, amount);
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L798


## [L-04] External calls in an un-bounded for-loop may result in a DOS
Consider limiting the number of iterations in for-loops that make external calls.

[reffrence](https://solodit.xyz/issues/l-01-external-calls-in-an-un-bounded-for-loop-may-result-in-a-dos-code4rena-llama-llama-git)

```solidity
File:  packages/contracts/contracts/Governor.sol
46       for (uint256 i = 0; i < users.length(); i++) {
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L46


## [L-05] `require()` should be used instead of `assert()`
[Reffrence](https://solodit.xyz/issues/l-01-code4rena-phuture-finance-phuture-finance-contest-git)

```solidity
File:  packages/contracts/contracts/LiquidationLibrary.sol
564   assert(toLiquidator < _totalColToSend); // Assert is correct here for Echidna
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L564


## [L-06] Void constructor:
 Calls to base contract constructors that are unimplemented leads to misplaced assumptions. Check if the constructor is implemented or remove call if not. (see [here](https://github.com/crytic/slither/wiki/Detector-Documentation#void-constructor))


```solidity
File:  packages/contracts/contracts/LeverageMacroDelegateTarget.sol
    constructor(
        address _borrowerOperationsAddress,
        address _activePool,
        address _cdpManager,
        address _ebtc,
        address _coll,
        address _sortedCdps
    )
        LeverageMacroBase(
            _borrowerOperationsAddress,
            _activePool,
            _cdpManager,
            _ebtc,
            _coll,
            _sortedCdps,
            false // Do not sweep to caller
        )
    {
        // Approves are done via `execute` since this is a contract you delegatecall into
    }
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L41-L60


```solidity
File:  packages/contracts/contracts/LiquidationLibrary.sol
    constructor(
        address _borrowerOperationsAddress,
        address _collSurplusPool,
        address _ebtcToken,
        address _sortedCdps,
        address _activePool,
        address _priceFeed,
        address _collateral
    )
        CdpManagerStorage(
            address(0),
            address(0),
            _borrowerOperationsAddress,
            _collSurplusPool,
            _ebtcToken,
            _sortedCdps,
            _activePool,
            _priceFeed,
            _collateral
        )
    {}
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L14-L34

## [L-07] AuthorityUpdated emits wrong user address
In the Auth.setAuthority function the AuthorityUpdated is emitted ([Link](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L49)).

It is defined as:
[Link](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L12)

```solidity
12   event AuthorityUpdated(address indexed user, Authority indexed newAuthority);
```
So the first parameter should be the user address.

When the event is emitted the first parameter is msg.sender. The issue is that the user address and msg.sender can be different. So the event in some cases contains wrong information.

### same issue here

```solidity
File:  packages/contracts/contracts/Dependencies/Auth.sol
55  emit OwnershipTransferred(msg.sender, newOwner);
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L55


```solidity
File:  packages/contracts/contracts/Dependencies/AuthNoOwner.sol
50  emit AuthorityUpdated(msg.sender, Authority(newAuthority));
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L50


## [N-01] For modern and more readable code; update import usages

Solidity code is also cleaner in another way that might not be noticeable: the struct Point. We were importing it previously with global import but not using it. The Point struct polluted the source code with an unnecessary object we were not using because we did not need it.  
This was breaking the rule of modularity and modular programming: only import what you need Specific imports with curly braces allow us to apply this rule better.  

### Recommendation  
`import {contract1 , contract2} from "filename.sol";`