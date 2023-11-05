## Make only the _borrower to call the `permitPositionManagerApproval()` function.

- So in the `permitPositionManagerApproval()` function, It's to grant approval for a positionManager, Suppose the _borrower calls the `permitPositionManagerApproval()` function with the parameters, Anyone who watches the mempool could frontrun the function call, Ofcourse this is not a medium or any critical issue but when someone else frontruns the function call, the nonce will be incremented and when the actual _borrowers call gets processed it'll return him the error `"BorrowerOperations: Invalid signature"`. I mean he might not know the approval was granted to the positionManager already because of the frontrun call. As i have mentioned this is not a big issue but its better to have a require in the function that only the _borrower address can call so no one else will be able to mess as said above.

```
require(msg.sender == _borrower);
```