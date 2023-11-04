## [G-01] DEFINE CONSTRUCTOR AS PAYABLE
**Impact**
Developers can save around 10 opcodes and some gas if the constructors are defined as payable.
However, it should be noted that it comes with risks because payable constructors can accept ETH during deployment.
**Remediation**
It is suggested to mark the constructors as payable to save some gas. Make sure it does not lead to any adverse effects in case an upgrade pattern is involved.
**Locations**
```txt
contracts/LeverageMacroReference.sol#L17-L42
contracts/LeverageMacroBase.sol#L51-L68
contracts/CdpManagerStorage.sol#L217-L237
contracts/BorrowerOperations.sol#L107-L137
contracts/contracts/EBTCToken.sol#L61-L78
contracts/contracts/ActivePool.sol#L46-L66
contracts/LiquidationLibrary.sol#L14-L34
contracts/contracts/Governor.sol#L36-L36
contracts/SimplifiedDiamondLike.sol#L44-L46
contracts/LeverageMacroDelegateTarget.sol#L41-L60
contracts/CdpManager.sol#L30-L60
contracts/LeverageMacroFactory.sol#L21-L35
contracts/Dependencies/RolesAuthority.sol#L20-L20
contracts/Dependencies/EbtcBase.sol#L52-L56
```