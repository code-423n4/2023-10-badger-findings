## Make only the _borrower or _positionManager to call the `permitPositionManagerApproval()` function.

- So in the `permitPositionManagerApproval()` function, It's to grant approval for a positionManager, Suppose the (_borrower,_positionManager) calls the `permitPositionManagerApproval()` function with the parameters, Anyone who watches the mempool could frontrun the function call, Ofcourse this is not a medium or any critical issue but when someone else frontruns the function call, the nonce will be incremented and when the actual (_borrower,_positionManager) call gets processed it'll return him the error `"BorrowerOperations: Invalid signature"`. I mean he might not know the approval was granted to the positionManager already because of the frontrun call. As i have mentioned this is not a big issue but its better to have a require in the function that only the _borrower or _positionManager address can call so no one else will be able to mess as said above.

```
require(msg.sender == _borrower); // or _positionManager
```

https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L706