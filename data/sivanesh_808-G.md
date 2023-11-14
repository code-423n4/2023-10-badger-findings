### G-01: Rearrange the Struct to save slot 

#### Description:
Rearranging the structure of the `MoveTokensParams` struct can lead to significant gas savings in smart contracts. Each slot saved in the struct can potentially avoid an extra SSTORE operation, which costs around 20,000 gas for the first setting of the struct.


#### File:
[BorrowerOperations.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol)

#### Code Snippet:
**Before Rearrangement:**
```solidity
struct MoveTokensParams {
    address user;
    uint256 collSharesChange;
    uint256 collAddUnderlying; // ONLY for isCollIncrease=true
    bool isCollIncrease;
    uint256 netDebtChange;
    bool isDebtIncrease;
}
```

**After Rearrangement:**
```solidity
struct MoveTokensParams {
    uint256 collSharesChange;
    uint256 collAddUnderlying;
    uint256 netDebtChange;
    address user;
    bool isCollIncrease;
    bool isDebtIncrease;
    // potentially more bools or small fields here
}
```

#### Gas Savings Analysis:
- **Slot Savings**: The rearranged structure saves 2 slots.
- **Gas Savings**: With each slot potentially saving 20,000 gas on the first setting, the total gas savings could be up to 40,000 gas.

#### GitHub Link:
[BorrowerOperations.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol)



#### File:
[IPriceFeed.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPriceFeed.sol#L17C5-L24C6)



#### Code Snippet:
**Before Rearrangement:**
```solidity
struct ChainlinkResponse {
    uint80 roundEthBtcId;
    uint80 roundStEthEthId;
    uint256 answer;
    uint256 timestampEthBtc;
    uint256 timestampStEthEth;
    bool success;
}
```

**After Rearrangement:**
```solidity
struct ChainlinkResponse {
    uint80 roundEthBtcId;
    uint80 roundStEthEthId;
    bool success;
    uint256 answer;
    uint256 timestampEthBtc;
    uint256 timestampStEthEth;        
}
```

#### Gas Savings Analysis:
- **Slot Savings**: The rearranged structure saves 1 slot.
- **Gas Savings**: This could lead to a potential saving of up to 20,000 gas for the initial storage operation.



#### GitHub Link:
[IPriceFeed.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPriceFeed.sol#L17C5-L24C6)




___________________________________________________________________________________________________________

### G-02: Struct can tight pack

### File : 

[IPriceFeed.sol#L26-L30](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPriceFeed.sol#L26C5-L30C6)

#### Description:

In the current FallbackResponse struct, the timestamp variable is declared as uint256, which occupies a complete storage slot of 256 bits. Given that timestamps generally represent time in seconds since the Unix epoch, the range provided by a uint240 is excessively large, covering a period significantly longer than 100 years. This over-allocation of storage is inefficient in terms of gas usage and contract storage.



- **Code**:
    ```solidity
    struct FallbackResponse {
        
        uint256 answer;
      - uint256 timestamp;
      + uint248 timestamp; // Downcasted from uint256
        bool success;
    }
    ```

### Expected Savings

- **Storage Slots**: The proposed change will save 1 storage slot by utilizing `uint240` for the `timestamp` instead of `uint256`.


### Source Code Reference


- GitHub Link: [IPriceFeed.sol#L26-L30](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPriceFeed.sol#L26C5-L30C6)


_____________________________________________________________________________________________________________________________________

### [G-03] State Variables Can Be Tightly Packed 

#### File: 
[IPriceFeed](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPriceFeed.sol)

#### Description:
In the `IPriceFeed` contract, the `minuteDecayFactor` variable is declared as `uint256`. However, this size may be larger than necessary for its intended use. A smaller data type, such as `uint248`, could be sufficient depending on the maximum value `minuteDecayFactor` is expected to hold. This change would allow for more efficient use of storage space.

#### Code:
```solidity
uint256 public constant SECONDS_IN_ONE_MINUTE = 60;
uint256 public constant MIN_REDEMPTION_FEE_FLOOR = (DECIMAL_PRECISION * 5) / 1000; // 0.5%
uint256 public redemptionFeeFloor = MIN_REDEMPTION_FEE_FLOOR;
bool public redemptionsPaused;

// Suggested Change: Downcast minuteDecayFactor to uint248
+ uint248 public minuteDecayFactor = 999037758833783000;
- uint256 public minuteDecayFactor = 999037758833783000;

uint256 public constant MIN_MINUTE_DECAY_FACTOR = 1; // Non-zero
uint256 public constant MAX_MINUTE_DECAY_FACTOR = 999999999999999999; // Very fast decay rate

uint256 internal immutable deploymentStartTime;
```

#### GitHub Link: 
[IPriceFeed.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPriceFeed.sol)


__________________________________________________________________________________________________________


### [G-04] Unused state variables can save slot 

### Description : unused state variables can lead to unnecessary gas consumption. This occurs because every state variable occupies storage, which is a costly resource on the Ethereum blockchain.


### File : RolesAuthority.sol

### Code:
```solidity

30. EnumerableSet.Bytes32Set internal enabledFunctionSigsPublic;

```

#### GitHub Link: 
[RolesAuthority.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L30)

### File : Governor.sol

### Code:
```solidity

17. bytes32 NO_ROLES = bytes32(0);


```

#### GitHub Link: 
[Governor.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L17)
