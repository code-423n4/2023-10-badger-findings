https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L438

  for (uint256 i; i < length; ++i) {
here we can do uncheck ++i;


https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L449
  for (uint i = 0; i < _len; ++i) {
here we can do uncheck ++i;

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L432
for (uint256 i = 0; i < _len; ++i) {

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L137
 for (uint256 i = 0; i < _sigs.length; ++i) {
do a constant to _sigs.length and do uncheck ++i;

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L122
   for (uint8 i = 0; i < roleIds.length; i++) {
do a constant to roleIds.length and do uncheck ++i;


https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L107
 for (uint8 i = 0; i < type(uint8).max; i++) {
do a constant to type(uint8).max and do uncheck ++i;

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L98
 for (uint8 i = 0; i < type(uint8).max; i++) {
do a constant to type(uint8).max and do uncheck ++i;

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L84
 for (uint8 i = 0; i < type(uint8).max; i++) {
do a constant to type(uint8).max and do uncheck ++i;

 https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L82
 uint256 j = 0;
donot need to assign j.

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L78
 count += 1;
do count=count+1;

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L76
 for (uint8 i = 0; i < type(uint8).max; i++) {
do a constant to type(uint8).max and do uncheck ++i;

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L57
 for (uint256 i = 0; i < _usrs.length; i++) {
do a constant to _usrs.length and do uncheck ++i;

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L54
uint256 j = 0;
donot need to assign j.

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L50
 count += 1;
use instead count=count+1;

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L46
for (uint256 i = 0; i < users.length(); i++) {
do a constant to users.length and do uncheck ++i;









