transfer and transferFrom can lose funds in your smart contract if the transaction fails
Unsafe ERC20 operations


https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/ActivePool.sol#L274

https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/ActivePool.sol#L283

https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/ActivePool.sol#L286

transfer and transferFrom can be exploited

Recommendation:
use safeTransferFrom which reverts in case of failure