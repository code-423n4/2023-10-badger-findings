# GAS OPTIMIZATIONS

##

## [G-1] Optimizing storage usage with packed structs

Each slot saved can avoid an extra Gsset (20000 gas) for the first setting of the struct.

Subsequent reads as well as writes have smaller gas savings.

### user,isCollIncrease,isDebtIncrease can be packed with same slot : Saves ``2 SLOT`` , ``4000 GAS``

https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L97-L104

```diff
FILE: Breadcrumbs2023-10-badger/packages/contracts/contracts/BorrowerOperations.sol

 struct MoveTokensParams {
        address user;
+        bool isCollIncrease;
+        bool isDebtIncrease;
        uint256 collSharesChange;
        uint256 collAddUnderlying; // ONLY for isCollIncrease=true
-        bool isCollIncrease;
        uint256 netDebtChange;
-        bool isDebtIncrease;
    }

```

###  roundEthBtcId , roundStEthEthId , success can be packed with same slot : Saves 1 SLOT , 2000 GAS

https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Interfaces/IPriceFeed.sol#L17-L24

```diff
FILE: 2023-10-badger/packages/contracts/contracts/Interfaces/IPriceFeed.sol

 struct ChainlinkResponse {
        uint80 roundEthBtcId;
        uint80 roundStEthEthId;
+        bool success;
        uint256 answer;
        uint256 timestampEthBtc;
        uint256 timestampStEthEth;
-        bool success;
    }


```

###  timestamp , success can be packed with same slot : Saves ``1 SLOT`` , ``2000 GAS``

https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Interfaces/IPriceFeed.sol#L26-L30

```diff
FILE: 2023-10-badger/packages/contracts/contracts/Interfaces/IPriceFeed.sol

  struct FallbackResponse {
        uint256 answer;
-        uint256 timestamp;
+        uint248 timestamp;
        bool success;
    }

```






