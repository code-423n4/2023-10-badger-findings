# _fallbackIsFrozen makes a call to fallbackCaller.fallbackTimeout() without checking that fallbackCaller is non-zero


## Github Links
https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/PriceFeed.sol#L490

## Description
if the PriceFeed contract function _fallbackIsFrozen, a call is made to [fallbackCaller.fallbackTimeout()](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/PriceFeed.sol#L490) without checking that fallbackCaller is non-zero. This is unsafe since a zero address fallback is an acceptable state in the system (and is checked for in other places in the code, such as [here](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/PriceFeed.sol#L224)). Currently all calls to _fallbackIsFrozen are preceded by a check that fallback is not broken (which eliminates the zero value fallback case), however relying on an external check is unsafe and may be overlooked in future development. 


## Impact
If _fallbackIsFrozen is called when fallbackCaller is zero, if will revert, potentially reverting many of the main protocol operations that indirectly use _fallbackIsFrozen.

## Tools Used
Foundry

## Recommended Mitigation Steps
At a minimum the documentation for _fallbackIsFrozen should mention that it should not be called without a prior check that _fallbackIsBroken is false. For an even safer approach,
add a check at the start of the function to return true is fallbackCaller is zero (The logic being that if you reach _fallbackIsFrozen when fallbackCaller is zero it's better to consider the fallback frozen than to fail the entire transaction).
```
if (address(fallbackCaller) == address(0)) {
    return true;
}
return
            _fallbackResponse.timestamp > 0 &&
            _responseTimeout(_fallbackResponse.timestamp, fallbackCaller.fallbackTimeout());      
```


# Inaccurate error message on _requireBorrowerOrPositionManagerAndUpdateManagerApproval

## Github Links
https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L972

## Description
The error message issued when _requireBorrowerOrPositionManagerAndUpdateManagerApproval fails is "BorrowerOperations: Only borrower account or approved position manager can OpenCdp on borrower's behalf". However this test is used for actions other than OpenCdp (such as [closeCdp](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L555) and others). 

## Recommended Mitigation Steps
Change message to something like "BorrowerOperations: Only borrower account or approved position manager can perform cdp operations on borrower's behalf"



# No Reentrancy check for closeCdp

## Github Links
https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L553C46-L553C46

## Description
The function closeCdp in BorrowerOperations is [not protected](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L553) using the nonReentrantSelfAndCdpM modifier although it bears the same reentrancy risk as other functions (such as openCdp) that are protected by nonReentrantSelfAndCdpM.


## Impact
Reentrancy in the closeCdp function might enable a bad actor to close a CDP multiple times and drain the pool collateral. 


## Tools Used
Foundry

## Recommended Mitigation Steps
Add the nonReentrantSelfAndCdpM modifier to closeCdp:
```
 function closeCdp(bytes32 _cdpId) external override nonReentrantSelfAndCdpM {
```