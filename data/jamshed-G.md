&nbsp;

## \[G‑01\] Save gas by preventing zero amount in mint() and burn()[](https://github.com/code-423n4/2023-09-maia/blob/main/src/token/ERC20hTokenRoot.sol#L57C4-L72C6)

```
function mint(address _account, uint256 _amount) external override {
        _requireCallerIsBOorCdpMOrAuth();
        _mint(_account, _amount);
    }

    /// @notice Burn existing tokens
    /// @dev Internal system function - only callable by BorrowerOperations or CDPManager
    /// @dev Governance can also expand the list of approved burners to enable other systems to burn tokens
    /// @param _account The address to burn tokens from
    /// @param _amount The amount of tokens to burn
    function burn(address _account, uint256 _amount) external override {
        _requireCallerIsBOorCdpMOrAuth();
        _burn(_account, _amount);
    }

    /// @notice Burn existing tokens from caller
    /// @dev Internal system function - only callable by BorrowerOperations or CDPManager
    /// @dev Governance can also expand the list of approved burners to enable other systems to burn tokens
    /// @param _amount The amount of tokens to burn
    function burn(uint256 _amount) external {
        _requireCallerIsBOorCdpMOrAuth();
        _burn(msg.sender, _amount);
    }
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L85C3-L107C6

## \[G-02\] Use hardcode address instead `address(this)`

Instead of using `address(this)`, it is more gas-efficient to pre-calculate and use the hardcoded `address`. Foundry’s script.sol and solmate’s `LibRlp.sol` contracts can help achieve this.

References: <ins>https://book.getfoundry.sh/reference/forge-std/compute-create-address</ins>

<ins>https://twitter.com/transmissions11/status/1518507047943245824</ins>[](https://github.com/code-423n4/2023-09-maia/blob/main/src/VirtualAccount.sol#L61C5-L63C6)

```
collateral.transferFrom(address(receiver), address(this), amountWithFee);
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L283

```
require(
            collateral.balanceOf(address(this)) >= collateral.getPooledEthByShares(systemCollShares),
            "ActivePool: Must repay Balance"
        );
        require(
            collateral.sharesOf(address(this)) >= systemCollShares,
            "ActivePool: Must repay Share"
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L294C8-L300C43

```
uint256 balance = IERC20(token).balanceOf(address(this));
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L376

```
return keccak256(abi.encode(typeHash, name, version, _chainID(), address(this)));
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L682

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L145

## \[G-03\] Use assembly to validate `msg.sender`

We can use assembly to efficiently validate msg.sender for the didPay and uniswapV3SwapCallback functions with the least amount of opcodes necessary. Additionally, we can use xor() instead of iszero(eq()), saving 3 gas. We can also potentially save gas on the unhappy path by using scratch space to store the error selector, potentially avoiding memory expansion costs.[](https://github.com/code-423n4/2023-09-maia/blob/main/src/factories/ArbitrumBranchBridgeAgentFactory.sol#L85)

```
msg.sender == borrowerOperationsAddress,
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L221

```
msg.sender == borrowerOperationsAddress || msg.sender == cdpManagerAddress,
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L229

```
require(msg.sender == cdpManagerAddress, "ActivePool: Caller is not CdpManager");
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L236

```
function _requireCallerIsCdpManager() internal view {
        require(msg.sender == cdpManagerAddress, "CollSurplusPool: Caller is not CdpManager");
    }

    function _requireCallerIsActivePool() internal view {
        require(msg.sender == activePoolAddress, "CollSurplusPool: Caller is not Active Pool");
    }
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L119C3-L125C6

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L661

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L308

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L316

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L324

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L721

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L715

## \[G-04\] Amounts should be checked for 0 before calling a transfer

It is considered a best practice to verify for zero values before executing any transfers within smart contract functions. This approach helps prevent unnecessary external calls and can effectively reduce gas costs.

This practice is particularly crucial when dealing with the transfer of tokens or ether, as sending these assets to an address with a zero value will result in the loss of those assets.

In Solidity, you can determine whether a value is zero by utilizing the == operator. Here's an example demonstrating how to check for a zero value before performing a transfer:

```
//example 
function transfer(address payable recipient, uint256 amount) public {
    require(amount > 0, "Amount must be greater than zero");
    recipient.transfer(amount);
}
```

```
IERC20(token).safeTransfer(cachedFeeRecipientAddress, amount);
```

&nbsp;https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L381

```
IERC20(token).safeTransfer(feeRecipientAddress, amount);
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L148

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L259

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L267

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L282

&nbsp;

## \[G-05\] Use assembly to emit events

We can use assembly to emit events efficiently by utilizing scratch space and the free memory pointer. This will allow us to potentially avoid memory expansion costs. Note: In order to do this optimization safely, we will need to cache and restore the free memory pointer.

&nbsp;

&nbsp;

```
emit SystemCollSharesUpdated(cachedSystemCollShares);
        emit CollSharesTransferred(_account, _shares);
```

&nbsp;https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L112C9-L113C55

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L22C8-L23C55

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L49

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L55

## \[G-06\] uint8 is not always cheaper than uint256

The EVM only operates on 32 bytes/ 256 bits at a time. This means that if you use uint8, EVM has to first convert it uint256 to work on it and the conversion costs extra gas! You may wonder, What were the devs thinking? Why did they create smaller variables then? The answer lies in packing. In solidity, you can pack multiple small variables into one slot, but if you are defining a lone variable and can’t pack it, it’s optimal to use a uint256 rather than uint8.[](https://github.com/code-423n4/2023-09-maia/blob/main/src/factories/ERC20hTokenBranchFactory.sol#L96)

```
struct Role {
        uint8 roleId;
        string roleName;
    }
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L19

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L30C5-L32C64

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L76

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L700C2-L701C32

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L612C8-L613C32

## \[G-07\] Usage of "UINTS", "INTS" smaller than 32 Bytes (256 bits) results in Increased Gas Consumption.

📌 Using Elements that are: Lower than 32 Bytes = Higher Gas Usage BECAUSE "EVM operates on 32 Bytes at a time & if the element is smaller than that, the EVM must use more operations in order to reduce the size of the element from 32 bytes to the desired size"[](https://github.com/code-423n4/2023-09-maia/blob/main/src/factories/ERC20hTokenBranchFactory.sol#L14)

```
uint16 public feeBps = 3; // may be subject to future adjustments through protocol governance
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L14

## \[G-08\] When possible, use assembly instead of `unchecked{}`

You can also use unchecked{} for even more gas savings but this will not check to see if i overflows. For best gas savings, use inline assembly, however, this limits the functionality you can achieve.

> All contest

## \[G-09\] DEFAULT VALUE ASSIGNMENT TO VARIABLES CAN BE OMITTED TO SAVE GAS

Inside the `for` loop where the default value of `0` assigned to the `i` variable. Since `i` is by default initialzied to `0` it is not required explicitly assign the `0` value to `i` variable inside the `for` loops. This will save gas.[](https://github.com/code-423n4/2023-09-maia/blob/main/src/BranchPort.sol#L257)

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L46

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L57

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L76

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L98

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L107

## [](https://github.com/code-423n4/2023-09-maia/blob/main/src/RootBridgeAgentExecutor.sol#L281)

## \[G-10\] Make fewer external calls.

Every call to an external contract costs a decent amount of gas. For optimization of gas usage, It’s better to call one function and have it return all the data you need rather than calling a separate function for every piece of data. This might go against the best coding practices for other languages, but solidity is special.

## [](https://github.com/code-423n4/2023-09-maia/blob/main/src/BranchBridgeAgent.sol#L53C4-L84C32)

## \[G-11\] Use bytes32 rather than string/bytes.

If you can fit your data in 32 bytes, then you should use bytes32 datatype rather than bytes or strings as it is much cheaper in solidity. Basically, Any fixed size variable in solidity is cheaper than variable size.

```
string public constant NAME = "ActivePool";
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L24

```
string public constant NAME = "BorrowerOperations";
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L29

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L19

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L28C4-L31C44

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L19

## \[G-12\] `bytes` constants are more eficient than `string` constans

If the data can fit in 32 bytes, the bytes32 data type can be used instead of bytes or strings, as it is less robust in terms of robustness.

```
string internal constant _VERSION = "1";
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L41

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L19

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L28C4-L31C44

&nbsp;

## \[G-13\] Use solidity version 0.8.19 to gain some gas boost

> Upgrade to the latest solidity version 0.8.19 to get additional gas savings.
> 
> All contests
> 
> ...  
> See latest release for reference: https://blog.soliditylang.org/2023/02/22/solidity-0.8.19-release-announcement/

## \[G-14\] Use constants instead of type(uintx).max

it's generally more gas-efficient to use constants instead of type(uintX).max when you need to set the maximum value of an unsigned integer type.

The reason for this is that the type(uintX).max expression involves a computation at runtime, whereas a constant is evaluated at compile-time. This means that using type(uintX).max can result in additional gas costs for each transaction that involves the expression.

By using a constant instead of type(uintX).max, you can avoid these additional gas costs and make your code more efficient.

Here's an example of how you can use a constant instead of type(uintX).max:

```
contract MyContract {
    uint120 constant MAX_VALUE = 2**120 - 1;
    
    function doSomething(uint120 value) public {
        require(value <= MAX_VALUE, "Value exceeds maximum");
        
        // Do something
    }
}
```

In the above example, we have a contract with a constant MAX\_VALUE that represents the maximum value of a uint120. When the doSomething function is called with a value parameter, it checks whether the value is less than or equal to MAX\_VALUE using the <= operator.

By using a constant instead of type(uint120).max, we can make our code more efficient and reduce the gas cost of our contract.

It's important to note that using constants can make your code more readable and maintainable, since the value is defined in one place and can be easily updated if necessary. However, constants should be used with caution and only when their value is known at compile-time.

```
_maxIterations = type(uint256).max;
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L378

```
uint128 public constant UNSET_TIMESTAMP = type(uint128).max;
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L21

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L76

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L84

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L98

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L107

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L7

## \[G-15\] If statements that use && can be refactored into nested if statements

```
if (
                liquidationValues.totalCollToSendToLiquidator == 0 &&
                liquidationValues.debtToBurn == 0
            ) {
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L158

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L819

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L512

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L765

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L796

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L330

## \[G-16\]use Mappings Instead of Arrays

Mappings, are useful when you need to store and access data based on a key, rather than an index. Mappings have a lower gas cost for read and write operations, especially when the size of the mapping is large, since Solidity can perform these operations based on the key directly, without needing to iterate over the entire data structure.

```
bytes32[] public CdpIds;
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L205

## \[G-17\] Splitting `require()` statements that use `&&`saves gas - (saves 8 gas per `&&`)

Instead of using the `&&` operator in a single require statement to check multiple conditions, using multiple require statements with 1 condition per require statement will save 8 GAS per `&&`.

&nbsp;

```
require(
            closedStatus != Status.nonExistent && closedStatus != Status.active,
            "CdpManagerStorage: close non-exist or non-active CDP!"
        );
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L261

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L653

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L296C5-L303C11

### \[G-18\] Using `private` rather than `public` for constants, saves gas

If needed, the value can be read from the verified contract source code. Savings are due to the compiler not having to create non-payable getter functions for deployment calldata, and not adding another entry to the method ID table

```
uint256 public constant TIMEOUT_ETH_BTC_FEED = 4800; // 1 hours & 20min: 60 * 80
    uint256 public constant TIMEOUT_STETH_ETH_FEED = 90000; // 25 hours: 60 * 60 * 25

    // Maximum deviation allowed between two consecutive Chainlink oracle prices. 18-digit precision.
    uint256 public constant MAX_PRICE_DEVIATION_FROM_PREVIOUS_ROUND = 5e17; // 50%

    /*
     * The maximum relative price difference between two oracle responses allowed in order for the PriceFeed
     * to return to using the Chainlink oracle. 18-digit precision.
     */
    uint256 public constant MAX_PRICE_DIFFERENCE_BETWEEN_ORACLES = 5e16; // 5%
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L32C4-L42C79

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L9C5-L11C97

## \[G-19\] Make 3 event parameters indexed when possible

events are used to emit information about state changes in a contract. When defining an event, it's important to consider the gas cost of emitting the event, as well as the efficiency of searching for events in the Ethereum blockchain.

Making event parameters indexed can help reduce the gas cost of emitting events and improve the efficiency of searching for events. When an event parameter is marked as indexed, its value is stored in a separate data structure called the event topic, which allows for more efficient searching of events.

```
event FeeRecipientAddressChanged(address indexed _feeRecipientAddress);
    event StakingRewardSplitSet(uint256 _stakingRewardSplit);
    event RedemptionFeeFloorSet(uint256 _redemptionFeeFloor);
    event MinuteDecayFactorSet(uint256 _minuteDecayFactor);
    event BetaSet(uint256 _beta);
    event RedemptionsPaused(bool _paused);
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L16C4-L21C43

> all contest

## \[G-20\] Use enum

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ReentrancyGuard.sol#L8C3-L9C42