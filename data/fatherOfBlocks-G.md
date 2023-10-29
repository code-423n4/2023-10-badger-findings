**/packages/contracts/contracts/CdpManager.sol**
- L332 - Instead of validating redemptionsPaused == false, you could validate !redemptionsPaused.


**/packages/contracts/contracts/LiquidationLibrary.sol**
- L100/695/788 - It could be validated more simply like this: bool _recoveryModeAtStart = _TCR < CCR;
