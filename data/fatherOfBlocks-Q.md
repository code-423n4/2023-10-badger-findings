**/packages/contracts/contracts/HintHelpers.sol**
- L182 - abi.encodePacked() should not be used with dynamic types when passing the result to a hash function such as keccak256()
Use abi.encode() instead which will pad items to 32 bytes, which will prevent hash collisions (e.g. abi.encodePacked(0x123,0x456) => 0x123456 => abi.encodePacked(0x1,0x23456), but abi.encode(0x123,0x456) => 0x0...1230...456). “Unless there is a compelling reason, abi.encode should be preferred”. If there is only one argument to abi.encodePacked() it can often be cast to bytes() or bytes32() instead.
If all arguments are strings and or bytes, bytes.concat() should be used instead.

- L145 - Divisions are made by the input _price and it is not validated if the value is != 0, therefore it should be previously validated to avoid generating unhandled exceptions.


**/packages/contracts/contracts/LeverageMacroBase.sol**
- L452/453/454/455/456 - Requires are created but without an error message, it would be beneficial for these to have it so that the user can better understand what is happening in the state of the contract.


**/packages/contracts/contracts/SimplifiedDiamondLike.sol**
- L52/56/67/77/154 - Requires are created but without an error message, it would be beneficial for these to have it so that the user can better understand what is happening in the state of the contract.


**/packages/contracts/contracts/Dependencies/EbtcBase.sol**
- L108 - Division is performed by the input _amount and it is not validated if the value is != 0, therefore it should be previously validated to avoid generating unhandled exceptions.


**/packages/contracts/contracts/Dependencies/EbtcMath.sol**
- L78/98/116 - There is commented code that should be eliminated to avoid confusion and generate unnecessary lines.


**/packages/contracts/contracts/LiquidationLibrary.sol**
- L555/558/579 - Divisions are made by the input _price and it is not validated if the value is != 0, therefore it should be previously validated so as not to generate unhandled exceptions.


**/packages/contracts/contracts/EBTCToken.sol**
- L209/210 - abi.encodePacked() should not be used with dynamic types when passing the result to a hash function such as keccak256()
Use abi.encode() instead which will pad items to 32 bytes, which will prevent hash collisions (e.g. abi.encodePacked(0x123,0x456) => 0x123456 => abi.encodePacked(0x1,0x23456), but abi.encode(0x123,0x456) => 0x0...1230...456). “Unless there is a compelling reason, abi.encode should be preferred”. If there is only one argument to abi.encodePacked() it can often be cast to bytes() or bytes32() instead.
If all arguments are strings and or bytes, bytes.concat() should be used instead.


**/packages/contracts/contracts/BorrowerOperations.sol**
- L717/718 - abi.encodePacked() should not be used with dynamic types when passing the result to a hash function such as keccak256()
Use abi.encode() instead which will pad items to 32 bytes, which will prevent hash collisions (e.g. abi.encodePacked(0x123,0x456) => 0x123456 => abi.encodePacked(0x1,0x23456), but abi.encode(0x123,0x456) => 0x0...1230...456). “Unless there is a compelling reason, abi.encode should be preferred”. If there is only one argument to abi.encodePacked() it can often be cast to bytes() or bytes32() instead.
If all arguments are strings and or bytes, bytes.concat() should be used instead.
