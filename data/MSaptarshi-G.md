# [1]While importing use names of the contracts:
`import "./Dependencies/ReentrancyGuard.sol";`
Instead use this :
`import {ReentrancyGuard} from "./Dependencies/ReentrancyGuard.sol";`

# [2] This line is only initializing fee variable which doesn't have much need 
`uint256 fee = flashFee(token, amount); `