## [G-01] Use named imports instead of plain `import file.sol
## Summary
Using import declarations of the form `import {<identifier_name>} from 'some/file.sol'` avoids polluting the symbol namespace making flattened files smaller, and speeds up compilation.
## Vulnerability Details

## Impact
Instances (95):
````solidity
packages\contracts\contracts\Dependencies\EbtcBase.sol

5: import "./BaseMath.sol";
6: import "./EbtcMath.sol";
7: import "../Interfaces/IActivePool.sol";
8: import "../Interfaces/IPriceFeed.sol";
9: import "../Interfaces/IEbtcBase.sol";
10: import "../Dependencies/ICollateralToken.sol";
````
````solidity
packages\contracts\contracts\Dependencies\ERC3156FlashLender.sol

5: import "../Interfaces/IERC3156FlashLender.sol";
6: import "../Interfaces/IWETH.sol";
````
````solidity
packages\contracts\contracts\Dependencies\RolesAuthority.sol

6: import "./EnumerableSet.sol";
````
````solidity
packages\contracts\contracts\Interfaces\IActivePool.sol

5: import "./IPool.sol";
````
````solidity
packages\contracts\contracts\Interfaces\IBorrowerOperations.sol

4: import "./IPositionManagers.sol";
````
````solidity
packages\contracts\contracts\Interfaces\ICdpManager.sol

5: import "./IEbtcBase.sol";
6: import "./ICdpManagerData.sol";
````
````solidity
packages\contracts\contracts\Interfaces\ICdpManagerData.sol

5: import "./ICollSurplusPool.sol";
6: import "./IEBTCToken.sol";
7: import "./ISortedCdps.sol";
8: import "./IActivePool.sol";
9: import "./IRecoveryModeGracePeriod.sol";
10: import "../Dependencies/ICollateralTokenOracle.sol";
````
````solidity
packages\contracts\contracts\Interfaces\IEbtcBase.sol

5: import "./IPriceFeed.sol";
````
````solidity
packages\contracts\contracts\Interfaces\IEBTCToken.sol

5: import "../Dependencies/IERC20.sol";
6: import "../Dependencies/IERC2612.sol";
````
````solidity
packages\contracts\contracts\Interfaces\IERC3156FlashLender.sol

5: import "./IERC3156FlashBorrower.sol";
````
````solidity
packages\contracts\contracts\ActivePool.sol

5: import "./Interfaces/IActivePool.sol";
6: import "./Interfaces/ICollSurplusPool.sol";
7: import "./Dependencies/ICollateralToken.sol";
8: import "./Interfaces/ICdpManagerData.sol";
9: import "./Dependencies/ERC3156FlashLender.sol";
10: import "./Dependencies/SafeERC20.sol";
11: import "./Dependencies/ReentrancyGuard.sol";
12: import "./Dependencies/AuthNoOwner.sol";
13: import "./Dependencies/BaseMath.sol";
````
````solidity
packages\contracts\contracts\BorrowerOperations.sol

5: import "./Interfaces/IBorrowerOperations.sol";
6: import "./Interfaces/ICdpManager.sol";
7: import "./Interfaces/ICdpManagerData.sol";
8: import "./Interfaces/IEBTCToken.sol";
9: import "./Interfaces/ICollSurplusPool.sol";
10: import "./Interfaces/ISortedCdps.sol";
11: import "./Dependencies/EbtcBase.sol";
12: import "./Dependencies/ReentrancyGuard.sol";
13: import "./Dependencies/Ownable.sol";
14: import "./Dependencies/AuthNoOwner.sol";
15: import "./Dependencies/ERC3156FlashLender.sol";
16: import "./Dependencies/PermitNonce.sol";
````
````solidity
packages\contracts\contracts\CdpManager.sol

5: import "./Interfaces/ICdpManager.sol";
6: import "./Interfaces/ICollSurplusPool.sol";
7: import "./Interfaces/IEBTCToken.sol";
8: import "./Interfaces/ISortedCdps.sol";
9: import "./Dependencies/ICollateralTokenOracle.sol";
10: import "./CdpManagerStorage.sol";
11: import "./Dependencies/Proxy.sol";
````
````solidity
packages\contracts\contracts\CdpManagerStorage.sol

5: import "./Interfaces/ICdpManager.sol";
6: import "./Interfaces/ICollSurplusPool.sol";
7: import "./Interfaces/IEBTCToken.sol";
8: import "./Interfaces/ISortedCdps.sol";
9: import "./Dependencies/EbtcBase.sol";
10: import "./Dependencies/ReentrancyGuard.sol";
11: import "./Dependencies/ICollateralTokenOracle.sol";
12: import "./Dependencies/AuthNoOwner.sol";
````
````solidity
packages\contracts\contracts\CollSurplusPool.sol

5: import "./Interfaces/ICollSurplusPool.sol";
6: import "./Dependencies/ICollateralToken.sol";
7: import "./Dependencies/SafeERC20.sol";
8: import "./Dependencies/ReentrancyGuard.sol";
9: import "./Dependencies/AuthNoOwner.sol";
10: import "./Interfaces/IActivePool.sol";
````
````solidity
packages\contracts\contracts\EBTCDeployer.sol

5: import "./Dependencies/Create3.sol";
6: import "./Dependencies/Ownable.sol";
````
````solidity
packages\contracts\contracts\HintHelpers.sol

5: import "./Interfaces/ICdpManager.sol";
6: import "./Interfaces/ISortedCdps.sol";
7: import "./Dependencies/EbtcBase.sol";
````
````solidity
packages\contracts\contracts\LeverageMacroBase.sol

4: import "./Interfaces/IBorrowerOperations.sol";
5: import "./Interfaces/IERC3156FlashLender.sol";
6: import "./Interfaces/IEBTCToken.sol";
7: import "./Interfaces/ICdpManager.sol";
8: import "./Interfaces/ISortedCdps.sol";
9: import "./Interfaces/IPriceFeed.sol";
10: import "./Dependencies/ICollateralToken.sol";
12: import "./Dependencies/SafeERC20.sol";
````
````solidity
packages\contracts\contracts\LeverageMacroFactory.sol

5: import "./Dependencies/ICollateralToken.sol";
6: import "./Interfaces/IEBTCToken.sol";
````
````solidity
packages\contracts\contracts\LiquidationLibrary.sol

4: import "./Interfaces/ICdpManagerData.sol";
5: import "./Interfaces/ICollSurplusPool.sol";
6: import "./Interfaces/IEBTCToken.sol";
7: import "./Interfaces/ISortedCdps.sol";
8: import "./Dependencies/ICollateralTokenOracle.sol";
9: import "./CdpManagerStorage.sol";
````
````solidity
packages\contracts\contracts\PriceFeed.sol

5: import "./Interfaces/IPriceFeed.sol";
6: import "./Interfaces/IFallbackCaller.sol";
7: import "./Dependencies/AggregatorV3Interface.sol";
8: import "./Dependencies/BaseMath.sol";
9: import "./Dependencies/EbtcMath.sol";
10: import "./Dependencies/AuthNoOwner.sol";
````
````solidity
packages\contracts\contracts\SortedCdps.sol

5: import "./Interfaces/ISortedCdps.sol";
6: import "./Interfaces/ICdpManager.sol";
7: import "./Interfaces/IBorrowerOperations.sol";
````
## [G-02] Setting the `constructor` to `payable`
Saves ~13 gas per instance.
## Proof Of Concept
````solidity
packages/contracts/contracts/ActivePool.sol
46:    constructor(
````
[https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/ActivePool.sol#L46](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/ActivePool.sol#L46)
````solidity
packages/contracts/contracts/BorrowerOperations.sol
107:    constructor(
````
[https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L107](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L107)
````solidity
packages/contracts/contracts/CdpManager.sol
30:    constructor(
````
[https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L30](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L30)
````solidity
packages/contracts/contracts/CdpManagerStorage.sol
217:    constructor(
````
[https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L217](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L217)
````solidity
packages/contracts/contracts/CollSurplusPool.sol
42:    constructor(
````
[https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CollSurplusPool.sol#L42](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CollSurplusPool.sol#L42)
````solidity
packages/contracts/contracts/Governor.sol
36:    constructor(address _owner) RolesAuthority(_owner, Authority(address(this))) {}
````
[https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Governor.sol#L36](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Governor.sol#L36)
````solidity
packages/contracts/contracts/HintHelpers.sol
27:    constructor(
````
[https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/HintHelpers.sol#L27](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/HintHelpers.sol#L27)
````solidity
packages/contracts/contracts/LeverageMacroBase.sol
51:    constructor(
````
[https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LeverageMacroBase.sol#L51](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LeverageMacroBase.sol#L51)
````solidity
packages/contracts/contracts/LeverageMacroDelegateTarget.sol
41:    constructor(
````
[https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L41](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L41)
````solidity
packages/contracts/contracts/LeverageMacroFactory.sol
21:    constructor(
````
[https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LeverageMacroFactory.sol#L21](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LeverageMacroFactory.sol#L21)
````solidity
packages/contracts/contracts/LeverageMacroReference.sol
17:    constructor(
````
[https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LeverageMacroReference.sol#L17](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LeverageMacroReference.sol#L17)
````solidity
packages/contracts/contracts/LiquidationLibrary.sol
14:    constructor(
````
[https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LiquidationLibrary.sol#L14](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LiquidationLibrary.sol#L14)
````solidity
packages/contracts/contracts/PriceFeed.sol
57:    constructor(
````
[https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/PriceFeed.sol#L57](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/PriceFeed.sol#L57)
````solidity
packages/contracts/contracts/SimplifiedDiamondLike.sol
44:    constructor(address _owner) {
````
[https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SimplifiedDiamondLike.sol#L44](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SimplifiedDiamondLike.sol#L44)
````solidity
packages/contracts/contracts/SortedCdps.sol
88:    constructor(uint256 _size, address _cdpManagerAddress, address _borrowerOperationsAddress) {
````
[https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SortedCdps.sol#L88](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SortedCdps.sol#L88)
````solidity
packages/contracts/contracts/Dependencies/Auth.sol
18:    constructor(address _owner, Authority _authority) {
````
[https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/Auth.sol#L18](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/Auth.sol#L18)
````solidity
packages/contracts/contracts/Dependencies/EbtcBase.sol
52:    constructor(address _activePoolAddress, address _priceFeedAddress, address _collateralAddress) {
````
[https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/EbtcBase.sol#L52](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/EbtcBase.sol#L52)
````solidity
packages/contracts/contracts/Dependencies/RolesAuthority.sol
20:    constructor(address _owner, Authority _authority) Auth(_owner, _authority) {}
````
[https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L20](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L20)
## [G-03] The `owner` can be declared inside the `constructor`
## Relevant GitHub Links
[https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/Auth.sol#L18](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/Auth.sol#L18)

[https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Governor.sol#L36](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Governor.sol#L36)

[https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L20](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L20)

[https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SimplifiedDiamondLike.sol#L44](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SimplifiedDiamondLike.sol#L44)
## Summary
Inside the `constructor`, it is possible to declare the `owner`.
## Impact
Optimization
## Tools Used
Manual code review
## Recommendations
You can make this change :

packages/contracts/contracts/Dependencies/Auth.sol
````diff
- constructor(address _owner, Authority _authority) {
+ constructor(Authority _authority) {
-        owner = _owner;
+        owner = msg.sender;
         authority = _authority;

-        emit OwnershipTransferred(msg.sender, _owner);
+        emit OwnershipTransferred(msg.sender, owner);
         emit AuthorityUpdated(msg.sender, _authority);
    }
````