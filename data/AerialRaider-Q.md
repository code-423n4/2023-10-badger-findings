Suggestions for for the ActivePool.sol contract:
Access Modifiers: There are multiple functions where the contract checks if the caller is the borrowerOperationsAddress or cdpManagerAddress. This can be abstracted into a modifier.

Error Messages: Make error messages informative. Instead of just saying "!ActivePoolBal", explain what went wrong, like "ActivePool: Insufficient collateral balance".

Here is an example of how you might implement some of these improvements by abstracting repeated access control checks into modifiers and ensuring informative revert messages:


// SPDX-License-Identifier: MIT
pragma solidity 0.8.17;

// ... other imports ...

contract ActivePool is IActivePool, ERC3156FlashLender, ReentrancyGuard, BaseMath, AuthNoOwner {
    // ... existing code ...

    // --- Access Control Modifiers ---
    modifier onlyBorrowerOperationsOrCdpManager() {
        require(
            msg.sender == borrowerOperationsAddress || msg.sender == cdpManagerAddress,
            "ActivePool: Caller is not authorized"
        );
        _;
    }

    modifier onlyCdpManager() {
        require(msg.sender == cdpManagerAddress, "ActivePool: Caller is not CdpManager");
        _;
    }

    // ... existing code ...

    function transferSystemCollShares(address _account, uint256 _shares) public override onlyBorrowerOperationsOrCdpManager {
        uint256 cachedSystemCollShares = systemCollShares;
        require(cachedSystemCollShares >= _shares, "ActivePool: Insufficient collateral balance");
        // ... rest of the function ...
    }

    // ... rest of the code ...
}