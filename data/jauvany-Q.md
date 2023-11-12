#  LOW IMPACT VULNERABILITIES

## 1: More updated version of solidity can be used

Vulnerability details

### Context:

Using the more updated version of solidity can add new features and enhance security. Version 0.8.23 is the latest version of solidity. Which includes support for Shangai. If Optimism does not support PUSH0 at this moment, Version 0.8.19, which “contains a fix for a long-standing bug that can result in code that is only used in creation code to also be included in runtime bytecode”, can also be used. 

For reference, see https://github.com/ethereum/solidity/releases

### Proof of Concept

All contracts in scope

## Tools Used

Manual Analysis

**Recommended Mitigation Steps**

To be more secured and future-proofed, please consider using the more updated version of Solidity for all contracts in scope.


## 2: receive()/payable fallback() function does not authorize requests

Vulnerability details

### Context:

Having no access control on the ```function (e.g. require(msg.sender == address(weth)))``` means that someone may send Ether to the contract, and have no way to get anything back out, which is a loss of funds. If the concern is having to spend a small amount of gas to check the sender against an immutable address, the code should at least have a function to rescue mistakenlysent Ether. 

### Proof of Concept

> ***File: SimplifiedDiamondLike.sol***
```
160:    receive() external payable {
161:        // PHP is my favourite language
162:    }
```

### Tools Used

Manual Analysis

***Recommended Mitigation Steps***

The code should at least have a mechanism to rescue mistakenlysent Ether. 

## 3: Empty receive()/fallback() function

Vulnerability details

### Context:

If the intention is for Ether sent by a caller to be used for an actual purpose (i.e. the function is not just a WETH withdraw() handler), the function should call another function (e.g. call weth.deposit() and use the token on the caller's behalf) or at least emit an event to track that funds were sent directly to it.

### Proof of Concept

> ***File: SimplifiedDiamondLike.sol***
```
160:    receive() external payable {
161:        // PHP is my favourite language
162:    }
```

## Tools Used

Manual Analysis

***Recommended Mitigation Steps***

Function should not be empty

## 4: Missing checks for address(0x0) in the constructor/initializer

### Proof of Concept

> ***File: Sortedcdps.sol***

https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SortedCdps.sol#L96

```
96:	borrowerOperationsAddress = _borrowerOperationsAddress;
```

> ***File: EBTCToken.sol***

https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/EBTCToken.sol#L68-L69

```
68:	cdpManagerAddress = _cdpManagerAddress;
69:	borrowerOperationsAddress = _borrowerOperationsAddress;
```

> ***File: collsurpluspool.sol***

https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CollSurplusPool.sol#L48-L50

```
48:	borrowerOperationsAddress = _borrowerOperationsAddress;
49:	cdpManagerAddress = _cdpManagerAddress;
50: 	activePoolAddress = _activePoolAddress;
```

> ***File: cdpManagerStorage.sol***

https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L233

```
233:	borrowerOperationsAddress = _borrowerOperationsAddress;
```

> ***File: BorrowOperations.sol***

https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L121

```
121:	feeRecipientAddress = _feeRecipientAddress;
```

> ***File: ActivePool.sol***

https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/ActivePool.sol#L53-54
https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/ActivePool.sol#L56-57

```solidity
53:	borrowerOperationsAddress = _borrowerOperationsAddress;
54:	cdpManagerAddress = _cdpManagerAddress;

56:	collSurplusPoolAddress = _collSurplusAddress;
57:	feeRecipientAddress = _feeRecipientAddress;
```

### Tools Used

Manual Analysis
