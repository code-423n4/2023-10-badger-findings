# [QA-01] Lack of 2-step ownership transfer

[File: Auth.sol](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/Auth.sol#L52)
```
 function transferOwnership(address newOwner) public virtual requiresAuth {
        owner = newOwner;

        emit OwnershipTransferred(msg.sender, newOwner);
    }
```

A single step ownership change is risky due to the fact that the new owner address could be wrong.

Instead, consider using a contract like Ownable2Step, which provides a two-step ownership.


# [QA-02] `_openCdpCallback()` does not emit event

[File: LeverageMacroBase.sol](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LeverageMacroBase.sol#L463)
```
  * Open CDP and Emit event
```

According to comment - function `_openCdpCallback()` should emit an event. However, there's no event emitted by `_openCdpCallback()`.


# [QA-03] Unused code should be removed

[File: EbtcBase.sol](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/EbtcBase.sol#L35)
```
uint256 public constant BORROWING_FEE_FLOOR = 0; // 0.5%
```

Code-base does not use `BORROWING_FEE_FLOOR` constant. The calculation of fee floor is being performed in `_calcRedemptionRate()` in `CdpManager.sol`.

# [N-01] Typos

[File: ERC3156FlashLender.sol](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L13)
```
// Functions to modify these variables must be included in implementing contracts if desired
```

`impelemnting` should be changed to `implementing`

# [N-02] Redundant comments
Avoid inserting comments to the code-base, which does not provide any context

[File: SimplifiedDiamondLike.sol](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SimplifiedDiamondLike.sol#L161)
```
 // PHP is my favourite language
```

# [N-02] Constants should be upper-cased

[File: SortedCdps.sol](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SortedCdps.sol#L80)
```
bytes32 public constant dummyId =
```

It's a good coding practice to type constants names as uppercase, so `dummyId` should be `DUMMY_ID`.


# [N-03] Incorrect comment in `sweepToken()` from `CollSurplusPool.sol`

[File: CollSurplusPool.sol](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CollSurplusPool.sol#L139)
```
/// @notice because recipient are fixed, this function is safe to be called by anyone
    /// @param token The token to be swept
    /// @param amount The token value to be swept
    function sweepToken(address token, uint256 amount) public nonReentrant requiresAuth {
```

According to comment section, `this function is safe to be called by anyone`, which implies that this function should be called by anyone. However, function users `requiresAuth` modifier, which checks authorization.
This function - because of this modifier, cannot be called by anyone. 


# [N-04] Grammar errors
[File: CollSurplusPool.sol](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CollSurplusPool.sol#L139)
```
/// @notice because recipient are fixed, this function is safe to be called by anyone
```

`recipient are fixed` should be changed to `recipient is fixed`.

[File: BorrowerOperations.sol](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L697)
```
/// @notice This function set given _approval for specified _borrower and _positionManager
```

`This function set` should be changed to `This function sets`.



# [N-05] Improper comment in `BorrowerOperations.sol`

[File: BorrowerOperations.sol](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L580)
```
// By definition we are not in RM, notify CDPManager to ensure "Glass is on"
```

"Glass is on" should be changed to "Grace period is on"