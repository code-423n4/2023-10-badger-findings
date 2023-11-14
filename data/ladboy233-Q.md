| Issue Number | Description                                                         | Suggested Action                             |
|--------------|---------------------------------------------------------------------|----------------------------------------------|
| 1            | Function `flashFee` in `ActivePool` is not fully EIP 3156 compliant | Ensure compliance with EIP 3156              |
| 2            | Use of `increaseAllowance` / `decreaseAllowance` is deprecated in `EBTC.sol` token | Replace with secure alternatives             |
| 3            | Should validate if `ecrecover` returns address(0)                   | Implement validation for `ecrecover` return  |
| 4            | Address open `@todo` and `@audit` before deployment                 | Complete all TODOs and audits                |
| 5            | Rename `Governor` contract to `ACM` (Access Control Manager)        | Rename the contract as suggested             |


# function flashFee in ActivePool is not fully EIP 3156 complicant

According to https://code4rena.com/contests/2023-10-badger-ebtc-audit-certora-formal-verification-competition#top

> EIP Compliance
ActivePool: Should comply with EIP3156

according to https://eips.ethereum.org/EIPS/eip-3156

> The flashFee function MUST return the fee charged for a loan of amount token. If the token is not supported flashFee MUST revert.

so external implementation may replies on this function to validate whether flashloan is supported 

if the active pool collateral is stETH,

if we take a look at the stETH smart contract

https://etherscan.io/token/0xae7ab96520de3a18e5e111b5eaab095312d7fe84#readProxyContract

the implementation contract is https://etherscan.io/address/0x17144556fd3424edc8fc8a4c940b2d04936d17eb#code

when the admin of stETH paused the token, no transfer can be allowed and no flashloan can be borrowed

https://etherscan.io/address/0x17144556fd3424edc8fc8a4c940b2d04936d17eb#code#F27#L445

```solidity
 function _transferShares(address _sender, address _recipient, uint256 _sharesAmount) internal {
        require(_sender != address(0), "TRANSFER_FROM_ZERO_ADDR");
        require(_recipient != address(0), "TRANSFER_TO_ZERO_ADDR");
        require(_recipient != address(this), "TRANSFER_TO_STETH_CONTRACT");
        _whenNotStopped();

        uint256 currentSenderShares = shares[_sender];
        require(_sharesAmount <= currentSenderShares, "BALANCE_EXCEEDED");

        shares[_sender] = currentSenderShares.sub(_sharesAmount);
        shares[_recipient] = shares[_recipient].add(_sharesAmount);
    }
```

so the function [flashFee](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/ActivePool.sol#L317) should revert if the collateral is paused as well

```
   function flashFee(address token, uint256 amount) public view override returns (uint256) {
        require(token == address(collateral), "ActivePool: collateral Only");
        require(!flashLoansPaused, "ActivePool: Flash Loans Paused");
        require(ACTIVE_FLAG_POSITION.getStorageBool(), "collateral paused") // added code
        return (amount * feeBps) / MAX_BPS;
    }
```

reference implementation

https://etherscan.io/address/0x17144556fd3424edc8fc8a4c940b2d04936d17eb#code#F29#L19

```solidity
    function _whenNotStopped() internal view {
        require(ACTIVE_FLAG_POSITION.getStorageBool(), "CONTRACT_IS_STOPPED");
    }
```

# Use Of increase allowance / decrease allowance is deprecated and can bring security issue in EBTC.sol token

EBTC.sol still use [increaseAllowance / decreaseAllowance](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/EBTCToken.sol#L152)

Openzeppelin already deprecate increase allowance and decrease allowance in v5 release,

relevent discussion is in the thread below

https://github.com/OpenZeppelin/openzeppelin-contracts/issues/4583

some sound reason comment is here

https://github.com/OpenZeppelin/openzeppelin-contracts/issues/4583#issuecomment-1710297819

recommend remove the increase allowance / decrease allowance function as well

# Should validate if ecrecover return address(0)

> EBTCToken: Should comply with ERC20, ERC2612

ERC2612 is for signature permit,

per security consideration

https://eips.ethereum.org/EIPS/eip-2612

> Since the ecrecover precompile fails silently and just returns the zero address as signer when given malformed messages, it is important to ensure owner != address(0) to avoid permit from creating an approval to spend “zombie funds” belong to the zero address.

but in the current implementation, there is no check to ensure the recovered owner address from  ecrecover is not 0 in case when the invalid v, r, s is passed in in [EBTC permit function](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/EBTCToken.sol#L218)

```solidity
address recoveredAddress = ecrecover(digest, v, r, s);
require(recoveredAddress == owner, "EBTC: invalid signature");
```

while QA impact is more suited because even when owner address(0) is approved, 

[transfer ensure](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/EBTCToken.sol#L247) no token can be sent to address(0)

```solidity
function _transfer(address sender, address recipient, uint256 amount) internal {
	require(sender != address(0), "EBTCToken: zero sender!");
	require(recipient != address(0), "EBTCToken: zero recipient!");
```

it is still recommend to validate ecrecover return address(0) as invalid signature

# Address open @todo and @audit before deployment

there are a lot of open @todo and the @audit is for developer reference but it is another form of todo,

these to-do must be addressed before going into production

```solidity
packages/contracts/contracts/CdpManager.sol:
  140              _redeemColFromCdp.maxEBTCamount,
  141              _redeemColFromCdp.maxEBTCamount,
  142:             Cdps[_redeemColFromCdp.cdpId].debt /// @audit Redeem everything

  142          );
  143          );

  391              {
  392              {
  393:                 _syncAccounting(_cId); /// @audit This happens even if the re-insertion doesn't

  393  
  394  

  513      function syncAccounting(bytes32 _cdpId) external virtual override {
  514      function syncAccounting(bytes32 _cdpId) external virtual override {
  515:         /// @audit Opening can cause invalid reordering of Cdps due to changing values without reInserting into sortedCdps

  515          _requireCallerIsBorrowerOperations();
  516          _requireCallerIsBorrowerOperations();

  917  
  918  
  919:         cdpStEthFeePerUnitIndex[_cdpId] = systemStEthFeePerUnitIndex; /// @audit We critically assume global accounting is synced here
  919          _updateRedistributedDebtIndex(_cdpId);
  920          _updateRedistributedDebtIndex(_cdpId);

packages/contracts/contracts/CdpManagerStorage.sol:
  765          if (_newIndex > _oldIndex && totalStakes > 0) {
  766:             /// @audit-ok We don't take the fee if we had a negative rebase
  767              (

packages/contracts/contracts/LeverageMacroBase.sol:
  450      function _ensureNotSystem(address addy) internal {
  451:         /// @audit Check and add more if you think it's better
  452          require(addy != address(borrowerOperations));

packages/contracts/contracts/LiquidationLibrary.sol:
   73          // prepare local variables
   74:         uint256 _ICR = getCachedICR(_cdpId, _price); // @audit syncAccounting already called, guarenteed to be synced
   75          (uint256 _TCR, uint256 systemColl, uint256 systemDebt) = _getTCRWithSystemDebtAndCollShares(

  562  
  563:         /// @audit MUST be like so, else we have debt redistribution, which we assume cannot happen in partial
  564          assert(toLiquidator < _totalColToSend); // Assert is correct here for Echidna

packages/contracts/contracts/PriceFeed.sol:
  349  
  350:         /// @audit This should never be used, but we added it for the Certora Prover
  351          return lastGoodPrice;

packages/contracts/contracts/SyncedLiquidationSequencer.sol:
  73              for (uint256 i = 0; i < _n && _cdpId != _first; ++i) {
  74:                 uint256 _icr = cdpManager.getSyncedICR(_cdpId, _price); /// @audit This is view ICR and not real ICR
  75                  uint256 _cdpStatus = cdpManager.getCdpStatus(_cdpId);

packages/contracts/contracts/Dependencies/EbtcBase.sol:
  140      function _checkICRAgainstTCR(uint256 _icr, uint _tcr) internal view returns (bool) {
  141:         /// @audit is _icr <= _tcr more dangerous for overal system safety?
  142:         /// @audit Should we use _icr < CCR to allow any risky CDP being liquidated?
  143          return _icr <= _tcr;
```

For example, one of this open [to do](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/PriceFeed.sol#L351) is in PriceFeed.sol, where developer add returned price for prover but this code must be removed, if the code hit bypass the case 1,2,3 and 4,5 and hit this code block

this price is never validated for staleness and price deviation, consume this price can result in wrong valuation of the collateral

```solidity
/// @audit This should never be used, but we added it for the Certora Prover
return lastGoodPrice;
```

# rename Governor contract to ACM (access control manager)

The protocol use [this contract](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Governor.sol#L13) to manage access control in role based manner

```solidity
contract Governor is RolesAuthority {
```

but the contract names as "Governor", but it is not a traditional sense of government contract where it can execute arbitrary proposal, 

so recommend to rename Governor contract to ACM





