## **Protocol Overview**

- eBTC is a decentralized synthetic Bitcoin asset on the Ethereum network, backed by Lido's Staked Ether and uses  immutable smart contracts to minimize counterparty risk. It aims to be the most decentralized synthetic BTC in DeFi and allows anyone to borrow BTC at no cost. This elimates the need for bridging BTC to the ethereum blockchain.

- The dollar value of locked stETH is always greater than that of eBTC and eBTC tokens to be fully redeemable for stETH - these helps the protocol maintain price parity with BTC.

- Users can obtain eBTC by depositing stETH as collateral into smart contracts, creating individual collateral debt positions (CDPs) that adhere to a predetermined minimum collateralization ratio. The tokens are freely exchangeable and can be sent or received by anyone with an Ethereum address. 

- The system is self-regulating, with the constant increase in user demand for and supply of stETH helping to maintain stability. By regularly monitoring and updating the stETH:BTC price using a decentralized data feed, CDPs that fall below 110% minimum collateralization ratio are liquidated.

## **Codebase Analysis**

- The Badger eBTC codebase is a fork of the Liquity project and is large, well-structured and its contracts are written to conform to the ERC20 standard. The codebase comprises a total of 39 contracts and about 5805 SLoC, uses mostly inheritance, includes 6 external calls to stETH token and Chainlink oracle, 17 interfaces, and 16 structs. The provided tests have a line coverage of about 99%. The protocol will be deployed to the Ethereum mainnet.
- The contracts in scope are divided into 5 categories.
  >   i. **The core protocol contracts** - There 10 contracts in this category which perform a host of functions including managing the stETH accounting and eBTC minting, creating and managing CDP operations, handling oracle pricefeed and distributing protocol roles.
  >   ii. **The helper contracts** - The one contract in scope is `HintHelpers.sol` which provides needed information to facilitate offchain integration.
  >   iii. **The leverage macro & smartwallet contracts** - host a total of 5 contracts through which leverage macros are deployed either as a clone, a reference or via a delegate call. There's also a multi purpose smart contract wallet which executes just like the DSProxy.
  >   iv. **The modified dependency contracts** - The protocol modifies a number of solmate and Dappsys dependencies. Auth, AuthNoOwner, ReentrancyGuard, EbtcMath are some of the modified contracts,
  >   v. **The core interfaces** - These are interface for the core contracts.

## **Architecture Review**

- The protocol's architecture is complex. All the needed protocol logic are stored within the contracts, eliminating the need for a separate database. in a sense, the Ethereum network serves as the protocol backend.
- The two main contracts, `BorrowerOperations.sol` and `CdpManager.sol`, manage user-facing functions and internal system logic, controlling CDP state updates and token movements. All balances and contract data are public.
- The stETH:BTC price data is fetched dynamically as needed vie tha `PiceFeed.sol` contract using the Chainlink reference as the primary source and another as secondary. To protect against stale prices, the pricefeed implements the frozen, broken and `PriceChangeAboveMax` failure fallback logic.
- eBTC relies on a sorted doubly-linked list of CDPs ordered by individual collateralization ratio (ICR). This list is critical for gas-efficient redemption and liquidation sequences targeting CDPs in ascending order of ICR. The list is found in SortedCdps.sol.
- Important functions are protected by restrictive modifiers which ensure that the can be called by only the permitted parties. Certain functions are also subject to governacne controlled by the modified solmate dependency `AuthNoOwner.sol`. The authority contract is the Governor.

## **Protocol Risks**

- **Centralization and governance privileges** - Some functions are controlled by governance and their actions can positively/negatively affect the protocol.
- **Ethereum ecosystem** - High gas fees, network DOS and potential changes in the Ethereum protocol can affect the protocol's operations.
- **Smart contract vulnerabilities** - Compromised contracts can also affect protocol's functionality.
- **Oracle** - Decimals, stale prices, broken oracles and so can affect token pricing.
- **Upgrade Risk** - stETH can be rugged via an ugrade.
- **Forks and external dependencies** - Any unaddressed issues in the inherited contracts puts the protocol at risk of being exploited.
- Other economic issues, extreme price movements, human errors, brute force hacks, and so on.

## **Approach to Audit**
- First, we reviewed the provided documents and videos, ran the contracts through slither and trimmed the generated reports of known issues and falso positives. Next, we manually reviewed the codebase, ran provided tests, tested out various attack vectors. We also tried to breaking the protocol's invariants. After this was done, we studied the protocol's previous audits and similar protocol types, compared the differences between the previous and new commits, and filtered out any what was considered as known. We rounded up the process by generating the needed reports.

## **FInal Thoughts & Recommendations**
- For a protocol of its size, it's well organized. The codebase was well written and commented, the provided documentation, videos, audit resources are probably some of the best on C4. The provided forge test line coverage is 99% which is very commendable. 
- On the flip side, some of the codebase implementations can be gas intensive e.g use of the require/revert error strings. Some depreciated ERC20 functions, `approve`, `transfer`, `transferfrom` which is not a risk since the only tokens being used are standard ERC20 tokens, but doing this is not really good practive. 
- Also, there's an uncomfortable number of "known" issues in the system. On one hand, it's not far fetched for a protocol of this size, at this development stage. On the other hand, each unmitigated "known" issue is a potential disaster waiting to be happen.
- Finally for recommendations,  there's not much that can we can make that probably hasn't been made from the previous 3 audits. Mitigate "known" issues. Diversify oracle by implementing the alternative to Chainlink. Refactor some of the larger functions e.g `getRedemptionHints` to reduce their cyclomatic complexity and make them easier to understand. Implement constant audits/upgrades and so on.




### Time spent:
40 hours