## Summary

### Low Issues

Total of **1 issue**:

|ID|Issue|
|:--:|:---|
| [L-01] | Missing Zero Address Check for `_authorityAddress` in `EBTCToken` Constructor |

---

## Low Issues
### [L-01] - Missing Zero Address Check for `_authorityAddress` in `EBTCToken` Constructor

- https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L66
- https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L55-L63

The lack of a zero address check for the `_authorityAddress` parameter in the `EBTCToken` constructor was identified as a vulnerability through a formal verification contest using the `authNoOwnerInitializedAndAddressSetInConstructor()` rule. This rule is designed to ensure that `_authorityInitialized` is `true` only when `_authority` is set to a non-zero address in `AuthNoOwner` contract.

```
invariant authNoOwnerInitializedAndAddressSetInConstructor() ghostAuthorityInitialized == (ghostAuthority != 0) 
    filtered { f -> f.selector == 0 } {
    preserved {
        require(false);
    }
}
```
In the initial `EBTCToken` contract, this rule was violated, suggesting that `_authority` could be set to the zero address while `_authorityInitialized` was `true`. This issue was not found in other contracts such as `ActivePool.sol` and `CollSurplusPool.sol`. 

An additional point of concern is the `setAuthority()` function in the `AuthNoOwner` contract. This function is intended to set a new `_authority` address. However, if `_authority` is initially set to the zero address due to the absence of a zero address check in the constructor, it would be impossible to change the `_authority` later, as the `setAuthority()` function requires the current `_authority` to authorize the change. This limitation poses a significant risk to the contract's flexibility and security.

***Recommendation***: It is advised to implement a zero address check for `_authorityAddress` in the `EBTCToken` constructor or within the `_initializeAuthority` function. The proposed fix involves adding the following check before initializing the authority:

```solidity
require(_authorityAddress != address(0), "EBTCToken: zero authority!");
_initializeAuthority(_authorityAddress);
```
