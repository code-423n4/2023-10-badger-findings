## [L-01] Lengthy numerals
Utilising big numerals that have a lot of precisions is within the file and this can be bettered by utilising scientific numerals.
The number 525600000 is seen on line 60.
**Locations**
```sol
// contracts/Dependencies/EbtcMath.sol#L60-L60
// Ln 60
if (_minutes > 525600000) {
```
**Remediation**
Change the number 525600000 to scientific notation of `5256e5`.