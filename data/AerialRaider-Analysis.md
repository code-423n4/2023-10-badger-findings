Here are the changes I'd suggest to optimize the code:

Consolidated Collateral Share Transfer: I consolidated the collateral share transfer logic in the _transferCollShares function. This function handles the transfer of shares and their accounting in one place, reducing redundancy.

Removed Redundant Checks: I removed redundant checks and simplified the conditions where possible. For example, there was no need to check if the amount to transfer shares is greater than zero, as it's already checked by the caller.

Optimized State Updates: I made sure that state variables are updated after emitting events. This change helps prevent unnecessary state changes and can save gas.

Consolidated Requires: I consolidated multiple require statements with similar error messages to make the code more concise.

Added Comments for Clarity: I added comments to explain the purpose of certain functions and provide context for readers.

Consistent Formatting and Naming: I ensured consistent naming and formatting throughout the code to improve readability and maintain a clean code style.

Optimized Balance Checks: In the flashLoan function, I avoided multiple balance checks and stored the old balance in a variable to reduce gas consumption.

Removed Unused Imports: I removed some unused import statements to clean up the code.

### Time spent:
4 hours