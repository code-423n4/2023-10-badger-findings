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