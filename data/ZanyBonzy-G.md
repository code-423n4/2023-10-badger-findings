### 1.  It is cheaper to emit only once after the loop has finished.

   SortedCdps.sol [L451](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SortedCdps.sol#L451)
   ```
    for (uint i = 0; i < _len; ++i) {
               delete data.nodes[_ids[i]];
               emit NodeRemoved(_ids[i]); //@gas 
           }
   ```

### 2. Multiple address/ID mappings can be combined into a single mapping of an address/ID to a struct, where appropriate

EBTCtoken.sol [L50](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/EBTCToken.sol#L50)
```
    // User data for EBTC token
    mapping(address => uint256) private _balances;
    mapping(address => mapping(address => uint256)) private _allowances;
```

RolesAuthority.sol [L32](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L32)
```
    mapping(address => bytes32) public getUserRoles;

    mapping(address => mapping(bytes4 => CapabilityFlag)) public capabilityFlag;

    mapping(address => mapping(bytes4 => bytes32)) public getRolesWithCapability;
```

### 3. Structs can be packed into fewer storage slots by truncating timestamp bytes for uint32 at the expense of breaking the protocol after the year 2106

IPricFeed.sol [L17](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Interfaces/IPriceFeed.sol#L17)
```
struct ChainlinkResponse {
        uint80 roundEthBtcId;
        uint80 roundStEthEthId;
        uint256 answer;
        uint256 timestampEthBtc; //@note
        uint256 timestampStEthEth; //@note
        bool success;
    }
```

IPricFeed.sol [L26](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Interfaces/IPriceFeed.sol#L26)
```
 struct FallbackResponse {
        uint256 answer;
        uint256 timestamp; //@note
        bool success;
    }

```

### 4. "" has the same value as new bytes(0) but costs less gas

SortedCdps.sol [L306](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SortedCdps.sol#L306)
```
 if (maxArraySize == 0) {
            return (new bytes32[](0), 0, dummyId);  
        }
```
### 5. Consider splitting `require()` statements that use && to save gas

PriceFeed.sol [80](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/PriceFeed.sol#L80)
```
require(
            !_chainlinkIsBroken(chainlinkResponse, prevChainlinkResponse) &&
                !_chainlinkIsFrozen(chainlinkResponse),
            "PriceFeed: Chainlink must be working and current"
        );
```
CdpManager.sol [L763](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L763)
```
require(
            _maxFeePercentage >= redemptionFeeFloor && _maxFeePercentage <= DECIMAL_PRECISION,
            "Max fee percentage must be between redemption fee floor and 100%"
        )
```

EBTCTOKEN.sol [L296](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/EBTCToken.sol#L296), [300](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/EBTCToken.sol#L301)
```
require(
            _recipient != address(0) && _recipient != address(this),
            "EBTC: Cannot transfer tokens directly to the EBTC token contract or the zero address"
        );
```

```
require(
            _recipient != cdpManagerAddress && _recipient != borrowerOperationsAddress,
            "EBTC: Cannot transfer tokens directly to the CdpManager or BorrowerOps"
        );
```
CdpManagerStorage.sol [261](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L261), [466](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L466), [653](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L653)

```
 require(
            closedStatus != Status.nonExistent && closedStatus != Status.active,
            "CdpManagerStorage: close non-exist or non-active CDP!"
        );
```
```
require(
            cdpStatus != Status.nonExistent && cdpStatus != Status.active,
            "CdpManagerStorage: remove non-exist or non-active CDP!"
        );
```
```
require(
            CdpOwnersArrayLength > 1 && sortedCdps.getSize() > 1,
            "CdpManager: Only one cdp in the system"
        );
```
BorrowerOperations.sol [L734](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L734)

```
        require(
            recoveredAddress != address(0) && recoveredAddress == _borrower,
            "BorrowerOperations: Invalid signature"
        );
```
### 6. array[index] += amount costs less gas than array[index] = array[index] + amount

CollSurplusPool.sol [L80](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CollSurplusPool.sol#L80C1-L84C1)
   ```
    -    uint256 newAmount = balances[_account] + _amount;
    -    balances[_account] = newAmount;
    +    uint256 newAmount
    +    balances[_account] += _amount;
    +    newAmount = balances[_account];
   ```
### 7. x = x +/- y costs less gas  x +=/-= y than for basic-typed state variables
Governor.sol [L50](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Governor.sol#L50), [L77](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Governor.sol#L77), [L101](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Governor.sol#L101)

```
 if (_canCall) {
                 count += 1;
             }
```
```
        if (doesUserHaveRole(user, i)) {
                count += 1;
            }
```
```
            if (roleEnabled) {
                count += 1;
            }
```

ActivePool.sol [L107](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/ActivePool.sol#L107), [L140](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/ActivePool.sol#L140), [163](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/ActivePool.sol#L163), [L355](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/ActivePool.sol#L355)

```
 unchecked {
            // Can use unchecked due to above
            cachedSystemCollShares -= _shares; // Updating here avoids an SLOAD
        }
```

```
unchecked {
            // Safe per the check above
            cachedSystemCollShares -= _shares;
        }
```

```
unchecked {
            // Safe per the check above
            cachedSystemCollShares -= _shares;
        }
```

```
        unchecked {
            cachedFeeRecipientCollShares -= _shares;
        }

```

### 8. All in-scope contracts' constructors can be marked payable as payable functions cost less gas to execute;

### 9. <array>.length should not be looked up in every loop of a for-loop

Governor.sol [76](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Governor.sol#L76), [84](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Governor.sol#L84), [98](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Governor.sol#L98), [107](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Governor.sol#L107)

```
        for (uint8 i = 0; i < type(uint8).max; i++)
```
```
        for (uint8 i = 0; i < type(uint8).max; i++)
```
```
        for (uint8 i = 0; i < type(uint8).max; i++)
```
```
        for (uint8 i = 0; i < type(uint8).max; i++)
```

### 10. ++i/--i costs less gas than i++/i--, especially when it's used in loops 

CdpManager.sol [L429](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L429)
```
_maxIterations--; 
```

### 11. Use private rather than public for constants & immutables

ActivePool.sol [26](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/ActivePool.sol#L26), [27](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/ActivePool.sol#L6), [28](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/ActivePool.sol#L6)

```
    address public immutable borrowerOperationsAddress;  
    address public immutable cdpManagerAddress;
    address public immutable collSurplusPoolAddress;
```
CdpManagerStorage.sol [126](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L126), [132](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L132)
```
    address public immutable borrowerOperationsAddress;
`  ...
    address public immutable liquidationLibrary;
```
CollSurplusPool.sol [21](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CollSurplusPool.sol#L21), [22](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CollSurplusPool.sol#L22), [23](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CollSurplusPool.sol#L23), [24](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CollSurplusPool.sol#L24)
```
    address public immutable borrowerOperationsAddress;
    address public immutable cdpManagerAddress;
    address public immutable activePoolAddress;
    address public immutable feeRecipientAddress;
```
EBTCToken.sol [55](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/EBTCToken.sol#L55), [56](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/EBTCToken.sol#L56)
```
    address public immutable cdpManagerAddress;
    address public immutable borrowerOperationsAddress;
```

SortedCdps.sol [54](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SortedCdps.sol#L54), [58](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SortedCdps.sol#L58)
```
    address public immutable borrowerOperationsAddress;

   ...

    uint256 public immutable maxSize;
```
LeverageMacroFactory.sol [12](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LeverageMacroFactory.sol#L12), [13](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LeverageMacroFactory.sol#L13), [14](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LeverageMacroFactory.sol#L14), [15](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LeverageMacroFactory.sol#L15), [16](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LeverageMacroFactory.sol#L16), [17](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LeverageMacroFactory.sol#L17)
```
    address public immutable borrowerOperations;
    address public immutable activePool;
    address public immutable cdpManager;
    address public immutable ebtcToken;
    address public immutable stETH;
    address public immutable sortedCdps;
```

SimplifiedDiamondLike.sol [44](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SimplifiedDiamondLike.sol#L44)
```
   address public immutable owner;
```
