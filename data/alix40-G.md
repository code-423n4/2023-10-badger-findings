On line 404, in file SortedCdps.sol
[link](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L404) 

```solidity
data.size = data.size + 1;
``` 

Could be changed to:

```solidity
data.size++
```
This could save gas, and due to the insert function, being used a lot this could reduce gas costs significantly long term


The same Issue is also found on line 489 in file SortedCdps.sol
[link](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SortedCdps.sol#L489C1-L490C1)

```solidity
data.size = data.size - 1;
```
could be changed to:

```solidity
data.size--
```

