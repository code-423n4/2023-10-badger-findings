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
## [L-02] Unchecked Transfer
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

## [L-03] Approve front running attack in EBTCToken contract
## Impact
Losses to Users: The main linked impact is upon users who may be victim to front running. 
Users might be affected by economic shortfall while users' transactions get front-run by hackers, making them to pay more gas fees or get incorrect prices.
There is no way to safely decrease or increase the amount of the token as the owner can only be the contract.
The recipient can exploit this by pretending to be the sender and sending token as the sender to themselves, the attacker or malicious recipient. 
Also, if the sender updates the amount they are trying to send then the malicious recipient can withdraw both amounts from the sender's account.
Hencefotrh a front-running attack on the ERC20 token.
Hence the function can front-run by manipulating the approve function.

## Proof of Concept
**Vulnerable approve function**
```sol
// ln 129-132
    function approve(address spender, uint256 amount) external override returns (bool) {
        _approve(msg.sender, spender, amount);
        return true;
    }
```
**Exploit approve function**
```sol
// SPDX-License-Identifier: MIT

pragma solidity >=0.8.17;

import "./EBTCToken.sol";

contract tEBTCToken {

   EBTCToken public x1;

   constructor(EBTCToken _x1) {

      x1 = EBTCToken(_x1);

   }

   function testApprove(EBTCToken _x1) external payable {
      
      x1.approve(address(0xPublicSpenderAddress), uint256(1e18));

   }

   }
```
**Vulnerable transferFrom function with approve**
```sol
// ln 134-150
    function transferFrom(
        address sender,
        address recipient,
        uint256 amount
    ) external override returns (bool) {
        _requireValidRecipient(recipient);
        _transfer(sender, recipient, amount);


        uint256 cachedAllowance = _allowances[sender][msg.sender];
        if (cachedAllowance != type(uint256).max) {
            require(cachedAllowance >= amount, "ERC20: transfer amount exceeds allowance");
            unchecked {
                _approve(sender, msg.sender, cachedAllowance - amount);
            }
        }
        return true;
    }
```
**Exploit transferFrom with approve function**
```sol
// SPDX-License-Identifier: MIT

pragma solidity >=0.8.17;

import "./EBTCToken.sol";

contract tEBTCToken {

   EBTCToken public x1;

   constructor(EBTCToken _x1) {

      x1 = EBTCToken(_x1);

   }

   function testTransfer(EBTCToken _x1) external payable {
      
      x1.transferFrom(address(0xPublicSpenderAddress), address(_x1), uint256(1e18));

   }

   }
```
**Vulnerable permit function**
```sol
// ln 199-221
    function permit(
        address owner,
        address spender,
        uint256 amount,
        uint256 deadline,
        uint8 v,
        bytes32 r,
        bytes32 s
    ) external override {
        require(deadline >= block.timestamp, "EBTC: expired deadline");
        bytes32 digest = keccak256(
            abi.encodePacked(
                "\x19\x01",
                domainSeparator(),
                keccak256(
                    abi.encode(_PERMIT_TYPEHASH, owner, spender, amount, _nonces[owner]++, deadline)
                )
            )
        );
        address recoveredAddress = ecrecover(digest, v, r, s);
        require(recoveredAddress == owner, "EBTC: invalid signature");
        _approve(owner, spender, amount);
    }
```
**Exploit permit with approve function**
```sol
// SPDX-License-Identifier: MIT

pragma solidity >=0.8.17;

import "./EBTCToken.sol";

contract tEBTCToken {

   EBTCToken public x1;

   bytes32 r = bytes32("0x10000000000000000000000000000");
   bytes32 s = bytes32("0x7FFFFFFFFFFFFFFFFFFFFFFFFFFFFFFF5D576E7357A4501DDFE92F46681B20A0");
   uint8 v = uint8(27);

   constructor(EBTCToken _x1) {

      x1 = EBTCToken(_x1);

   }

   function testPermit(EBTCToken _x1) external payable {
      
      x1.permit(
         address(_x1),
         address(0xPublicSpenderAddress),
         uint256(1e18),
         uint256(1e14),
         uint8(27),
         bytes32("0x10000000000000000000000000000"),
         bytes32("0x7FFFFFFFFFFFFFFFFFFFFFFFFFFFFFFF5D576E7357A4501DDFE92F46681B20A0"));
   }

   }
```

**Manual POC**
**Approve Function**
The approve() function takes control of the current funds even if the customer already utilised it or didn't, hence no chance to elevate or reduce funds by a particular value holistically but only in the case that the token possessor is the smart contract, not the account address.
Which potentially leads to misconduct by a token recipient when the malicious recipient attempt the transfer of particular tokens out of the victim's account who is sending it.
At the same time, it is possible that the sender makes a decision to update the amount and calls an extra approve transaction, and then the recipient is able to see this transaction prior to it's being mined and has the ability to take the tokens from the two transactions, hence, illegally taking tokens from the pending and non pending transactions. 
This is called front-running attack within the ERC20 Approve method.
The method approve is possibly front-run by misuising the _approve method.

**transferFrom with Approve function**
The transferFrom() functions can trump the current available fund even if the sender has previously sent it or not, hence there isn't a method to send more or send less funds by a specific amount atomically as the token possessor needs to be smart contract, and not a user address.
This can be misused by the token recipient when he/she attempts to transfer certain tokens from the spender's account.
In the mean time, if the spender makes a decision to update the value and calls a second approve transaction, the recipient can see the pending transaction and can take tokens from the pending transactions, hence, getting tokens from the two transactions. 
Known as a front-running attack within the ERC20 Approve method.
The method transferFrom is misused in a front-run by misusing the _approve method.

**Permit with approve function**
The permit function trumps the existing allowance even if the spender used it before or not, hence having no chance to increment or decrement the allowance with a certain value atomically but only in the case that the token owner is the smart contract.
Which can be manipulated by one token receiver whilst they attempt to extract tokens from the sender's account address.
All the while, let us say the sender tries to update the amount and sends a second permit or approve transfer, the receiver would see the transfer prior to its mining and can take tokens from the two transactions, hence, taking tokens from the two transfers. Being a front-running attack on the ERC20 Approve method.
The method permit is potentially front-run by manipulating the _approve method.

## Tools Used
VS Code.
## Recommended Mitigation Steps
Just utilise the approve method of the ERC/BEP standard to update the allowed value to 0 or from 0 (wait until the transaction is committed and approved).
Token possessor must confirm the first transaction has been mined from N to 0, that is, that the sender did not transfer a part of N allowed tokens prior to the first transaction was committed. 
These checks are doable utilising complicated blockchain explorers like `[Etherscan.io](https://etherscan.io/)`
Alternative ways to avoid the vulnerability is to approve token transfers solely to smart contracts that are verified code which do not contain business logic for carrying front running attacks also to accounts owned by users you know well.
## [L-04] Public burn in the EBTCToken contract
## Impact
The contract was found to be using public or an external burn function. The function was missing access control to prevent another user from burning their tokens. Also, the burn function was found to be using a different address than msg.sender.

Unauthorised Token Destruction: If an attacker could call the burn function without proper authorization, they could potentially destroy tokens at will. This could lead to a decrease in the total supply of tokens, affecting the token's value and the overall economy of the token.

Loss of Funds: If an attacker could manipulate the _amount parameter of the burn function, they could potentially burn more tokens than they should be able to. This could result in users losing their tokens without any transaction or approval.

Disruption of Operations: If the burn function is used in other operations (like in a staking mechanism), an exploit could disrupt these operations. This could lead to a loss of service and potential financial loss for users.

## Proof of Concept
**Vulnerable burn function**
```sol
// ln 95-98
    function burn(address _account, uint256 _amount) external override {
        _requireCallerIsBOorCdpMOrAuth();
        _burn(_account, _amount);
    }
```
**Exploit burn**
```sol
// SPDX-License-Identifier: MIT

pragma solidity >=0.8.17;

import "./EBTCToken.sol";

contract tEBTCToken {

   EBTCToken public x1;

   constructor(EBTCToken _x1) {

      x1 = EBTCToken(_x1);

   }

   function testBurn(EBTCToken _x1) external payable {

      x1.burn(address(_x1), uint256(1e18));

   }

   }
```

**Here's a step-by-step guide on how to do it using web3.js, assuming you're working in a Node.js environment:**

1. Install the necessary dependencies:
   Make sure you have Node.js installed, and then create a new Node.js project and install web3.js.

   ```bash
   npm init -y
   npm install web3
   ```

2. Create a JavaScript file (e.g., `burnToken.js`) and require the web3.js library:

   ```javascript
   const Web3 = require('web3');
   const web3 = new Web3('YOUR_ETHEREUM_NODE_URL'); // Replace with your Ethereum node URL
   const accountAddress = 'YOUR_SENDER_ADDRESS'; // Replace with your Ethereum address

   // Import the ABI (Application Binary Interface) of the EBTCToken contract
   const ebtctokenAbi = [ /* Paste the ABI here */ ];
   const ebtctokenContractAddress = 'YOUR_EBTCTOKEN_CONTRACT_ADDRESS'; // Replace with the contract address

   // Create a new contract instance
   const ebtctokenContract = new web3.eth.Contract(ebtctokenAbi, ebtctokenContractAddress);

   // Function to call the burn function
   async function burnTokens(account, amount) {
     try {
       // Replace with the appropriate call to _requireCallerIsBOorCdpMOrAuth() if needed
       // Use web3.js to send a transaction to the burn function
       const gasPrice = 'YOUR_GAS_PRICE'; // Replace with the desired gas price
       const gasLimit = 'YOUR_GAS_LIMIT'; // Replace with the desired gas limit

       const transaction = ebtctokenContract.methods.burn(account, amount).send({
         from: accountAddress,
         gasPrice: web3.utils.toWei(gasPrice, 'gwei'),
         gas: gasLimit,
       });

       const receipt = await transaction;
       console.log('Transaction receipt:', receipt);
     } catch (error) {
       console.error('Error burning tokens:', error);
     }
   }

   // Call the burnTokens function with the desired parameters
   burnTokens('ADDRESS_TO_BURN_FROM', AMOUNT_TO_BURN);
   ```

3. Replace the placeholders in the code:
   - Replace `'YOUR_ETHEREUM_NODE_URL'` with the URL of your Ethereum node.
   - Replace `'YOUR_SENDER_ADDRESS'` with the Ethereum address that will send the transaction.
   - Replace the `ebtctokenAbi` array with the ABI of your EBTCToken contract.
   - Replace `'YOUR_EBTCTOKEN_CONTRACT_ADDRESS'` with the address of the EBTCToken contract.
   - Define the `burnTokens` function to handle the burning of tokens.
   - Set the gas price and gas limit according to your requirements.
   - Replace `'ADDRESS_TO_BURN_FROM'` and `AMOUNT_TO_BURN` with the recipient address and the amount of tokens to burn.

4. Run the JavaScript file using Node.js:

   ```bash
   node burnToken.js
   ```

This script will send a transaction to the `burn` function in your EBTCToken contract, effectively burning tokens from the specified account. Make sure to handle errors and manage your private key securely when dealing with real tokens and contracts on the Ethereum network.
## Tools Used
VS Code.
## Recommended Mitigation Steps
Consider adding access control modifiers to the burn function to prevent another user from burning their tokens. The burn function should use msg.sender in the _from argument.
## [L-05] Deprecated safe approve function in the LeverageReferenceMacroBase contract
## Impact
The OpenZeppelin's safeApprove() function is obsolete and not to be adopted because of its vulnerability that is the same as the approve() function flaw called front running or sandwich hacks.
Losses to Users: The main linked impact is upon users who may be victim to front running. 
Users might be affected by economic shortfall while users' transactions get front-run by hackers, making them to pay more gas fees or get incorrect prices.
There is no way to safely decrease or increase the amount of the token as the owner can only be the contract.
The recipient can exploit this by pretending to be the sender and sending token as the sender to themselves, the attacker or malicious recipient. 
Also, if the sender updates the amount they are trying to send then the malicious recipient can withdraw both amounts from the sender's account.
Henceforth a front-running attack on the ERC20 token.
Hence the function can front-run by manipulating the approve function.

## Proof of Concept
**Vulnerable SafeApprove function**
```sol
// ln 398-431
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
**Manual POC**
**Safe Approve Function**
The safeApprove() function takes control of the current funds even if the customer already utilised it or didn't, hence no chance to elevate or reduce funds by a particular value holistically but only in the case that the token possessor is the smart contract, not the account address.
Which potentially leads to misconduct by a token recipient when the malicious recipient attempt the transfer of particular tokens out of the victim's account who is sending it.
At the same time, it is possible that the sender makes a decision to update the amount and calls an extra approve transaction, and then the recipient is able to see this transaction prior to it's being mined and has the ability to take the tokens from the two transactions, hence, illegally taking tokens from the pending and non pending transactions. 
This is called front-running attack within the ERC20 safeApprove method.
The method safeApprove is possibly front-run by misusing the _doSwap method.

To create a web3 POC for the deprecated `safeApprove` function in the `LeverageMacroBase` contract within the `_doSwap` function, you need to use the appropriate Ethereum libraries and contract interfaces. 
Below is a simplified example in JavaScript using web3.js to demonstrate how you can interact with the contract and its functions. 
Make sure to replace the placeholders with the actual contract address and ABI.

```javascript
const Web3 = require('web3');
const { abi } = require('./LeverageMacroBase.sol'); // Replace with the actual ABI file
const contractAddress = '0xYourContractAddress'; // Replace with the actual contract address
const senderAddress = '0xYourSenderAddress'; // Replace with your Ethereum address
const senderPrivateKey = '0xYourPrivateKey'; // Replace with your private key

const web3 = new Web3('https://mainnet.infura.io/v3/your-infura-project-id'); // Replace with your Infura endpoint

async function executeSwap() {
  try {
    const contract = new web3.eth.Contract(abi, contractAddress);

    // SwapOperation parameters (replace with actual values)
    const swapData = {
      addressForSwap: '0xSwapTargetAddress',
      tokenForSwap: '0xTokenForSwapAddress',
      addressForApprove: '0xApproveAddress',
      exactApproveAmount: '1000000000000000000', // 1 ETH in wei
      calldataForSwap: '0xYourCalldataForSwap',
      swapChecks: '0xYourSwapChecks',
    };

    const gas = 2000000; // Adjust the gas limit accordingly

    // Ensure call is safe
    // Block all system contracts
    // You'll need to implement the _ensureNotSystem function

    // Exact approve
    // Approve can be given anywhere because this is a router, and after the call, we will delete all approvals
    await contract.methods.safeApprove(
      swapData.addressForApprove,
      swapData.exactApproveAmount
    ).send({
      from: senderAddress,
      gas,
    });

    // Call and perform swap
    const tx = await contract.methods._doSwap(swapData).send({
      from: senderAddress,
      gas,
    });

    // Check if the transaction was successful
    if (tx.status) {
      console.log('Swap successful');
    } else {
      console.log('Swap failed');
    }

    // Approve back to 0
    await contract.methods.safeApprove(swapData.addressForApprove, '0').send({
      from: senderAddress,
      gas,
    });

    // Do the balance checks after the call to the aggregator
    // You'll need to implement the _doSwapChecks function
  } catch (error) {
    console.error('Error:', error);
  }
}

executeSwap();
```

Please make sure to replace the placeholders with actual values and customize the gas limit and any additional functions like `_ensureNotSystem` and `_doSwapChecks` based on your specific contract implementation. Also, ensure that you have an Ethereum account with enough balance to cover gas costs and securely manage your private key.

## Tools Used
VS Code.
## Recommended Mitigation Steps
One should adopt the safeIncreaseAllowance() or safeDecreaseAllowance rather than safeApprove().
Just utilise the safeApprove method of the ERC/BEP standard to update the allowed value to 0 or from 0 (wait until the transaction is committed and approved).
Token possessor must confirm the first transaction has been mined from N to 0, that is, that the sender did not transfer a part of N allowed tokens prior to the first transaction was committed. 
These checks are doable utilising complicated blockchain explorers like `[Etherscan.io](https://etherscan.io/)`
Alternative ways to avoid the vulnerability is to approve token transfers solely to smart contracts that are verified code which do not contain business logic for carrying front running attacks also to accounts owned by users you know well.