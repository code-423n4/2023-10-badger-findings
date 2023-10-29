## [L-01] Lengthy numerals
Utilising big numerals that have a lot of precisions is within the file and this can be bettered by utilising scientific numerals.

**Locations**
```sol
// The number 525600000 is seen on line 60.
// contracts/Dependencies/EbtcMath.sol#L60-L60
if (_minutes > 525600000) {

// The number 525600000 is seen on line 61.
// contracts/Dependencies/EbtcMath.sol#L61-L61
_minutes = 525600000;

// The number 1030000000000000000 is seen on line 19.
// contracts/Dependencies/EbtcBase.sol#L19-L19
    uint256 public constant LICR = 1030000000000000000; // 103%

// The number 1100000000000000000 is seen on line 22.
// contracts/Dependencies/EbtcBase.sol#L22-L22
    uint256 public constant MCR = 1100000000000000000; // 110%

// The number 1250000000000000000 is seen on line 25.
// contracts/Dependencies/EbtcBase.sol#L25-L25
    uint256 public constant CCR = 1250000000000000000; // 125%
```
**Remediation**
Change the number 525600000 to scientific notation of `5256e5`.
Change the number 1030000000000000000 to scientific notation of `103e16`.
Change the number 1100000000000000000 to scientific notation of `11e17`.
Change the number 1250000000000000000 to scientific notation of `125e16`.