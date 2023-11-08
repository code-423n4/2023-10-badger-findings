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
## Unchecked Transfer
## Impact
If the transferFrom does not go through or responds with 0 then sometimes the transfer does not roll back.
So when calling the transferFrom method one should check it in the code.

## Proof of Concept
**Vulnerable flash loan function**
```sol
// line 261-310
    function flashLoan(
        IERC3156FlashBorrower receiver,
        address token,
        uint256 amount,
        bytes calldata data
    ) external override returns (bool) {
        require(amount > 0, "ActivePool: 0 Amount");
        uint256 fee = flashFee(token, amount); // NOTE: Check for `token` is implicit in the requires above // also checks for paused
        require(amount <= maxFlashLoan(token), "ActivePool: Too much");


        uint256 amountWithFee = amount + fee;
        uint256 oldRate = collateral.getPooledEthByShares(DECIMAL_PRECISION);


        collateral.transfer(address(receiver), amount);


        // Callback
        require(
            receiver.onFlashLoan(msg.sender, token, amount, fee, data) == FLASH_SUCCESS_VALUE,
            "ActivePool: IERC3156: Callback failed"
        );


        // Transfer of (principal + Fee) from flashloan receiver
        collateral.transferFrom(address(receiver), address(this), amountWithFee);


        // Send earned fee to designated recipient
        collateral.transfer(feeRecipientAddress, fee);


        // Check new balance
        // NOTE: Invariant Check, technically breaks CEI but I think we must use it
        // NOTE: This means any balance > systemCollShares is stuck, this is also present in LUSD as is


        // NOTE: This check effectively prevents running 2 FL at the same time
        //  You technically could, but you'd be having to repay any amount below systemCollShares to get Fl2 to not revert
        require(
            collateral.balanceOf(address(this)) >= collateral.getPooledEthByShares(systemCollShares),
            "ActivePool: Must repay Balance"
        );
        require(
            collateral.sharesOf(address(this)) >= systemCollShares,
            "ActivePool: Must repay Share"
        );
        require(
            collateral.getPooledEthByShares(DECIMAL_PRECISION) == oldRate,
            "ActivePool: Should keep same collateral share rate"
        );


        emit FlashLoanSuccess(address(receiver), token, amount, fee);


        return true;
    }
```
**Exploit unchecked transfer flash loan**
```sol
// SPDX-License-Identifier: MIT

pragma solidity >=0.8.17;

import "./ActivePool.sol";

contract tActivePool {

   ActivePool public x1;

   address token = address(0x9Aa69Db8c53E504EF22615390EE9Eb72cb8bE498);

   constructor(ActivePool _x1) {

      x1 = ActivePool(_x1);

   }

   function testUncheck(ActivePool _x1) external payable {
      bytes calldata data = bytes("0x1e18");
      x1.flashLoan(
         address(_x1),
         address(0x9Aa69Db8c53E504EF22615390EE9Eb72cb8bE498),
         uint256(1e18),
         data);
   }

   }
```
The flashLoan function performs an unchecked transfer of amount to the receiver contract. 
An attacker can manipulate the receiver contract to exploit this vulnerability, for example, by implementing a malicious onFlashLoan function that doesn't return the expected FLASH_SUCCESS_VALUE. 
This allows the attacker to manipulate the flow of the flash loan and potentially exploit it.
## Tools Used
VS Code.
## Recommended Mitigation Steps
Utilise OpenZeppelin SafeERC20's safetransfer & safetransferFrom methods.
