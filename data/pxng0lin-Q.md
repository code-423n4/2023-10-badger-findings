## QA - Spelling errors in commentary
### BorrowOperations.sol
1. [L475 function `_openCDP(...)`](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L475): Incorrect spelling "In recovery **move**,..." should be "In recovery **mode**,...".
2. [L624 function `setPositionsManager(...)`](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L624): Grammatical error in "/// @notice Position managers with **'OneTIme'**..." should be "/// @notice Position managers with **'OneTime'**".

## QA - view can be restricted to pure
### EbtcBase.sol
1. [L134 function `_checkICRAgainstMCR(...)`](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/EbtcBase.sol#L134): View can be restricted to pure
2. [L140 function `_checkICRAgainstTCR(...)`](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/EbtcBase.sol#L140): View can be restricted to pure
