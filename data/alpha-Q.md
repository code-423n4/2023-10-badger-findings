1. Use braces around operators with uncertain precedence
In RolesAuthority::canCall we see the following code
```
File: package/contracts/contracts/Dependencies/RolesAuthority.sol
function canCall(
        address user,
        address target,
        bytes4 functionSig
    ) public view virtual override returns (bool) {
return bytes32(0) != getUserRoles[user] & getRolesWithCapability[target][functionSig];
```

In Solidity the & operator will be executed before != but this might not always be clear and might be different in other languages. I suggest adding braces around getUserRoles[user] & getRolesWithCapability[target][functionSig] to clarify operator precedence.

2. More check for save storage
In the RolesAuthority::setRoleCapability method, a require condition should be added at the beginning to ensure that the functionSig is not invoked for the CapabilityFlag.Burned and CapabilityFlag.Public cases:

```
File: package/contracts/contracts/Dependencies/RolesAuthority.sol
function setRoleCapability(
        uint8 role,
        address target,
        bytes4 functionSig,
        bool enabled
    ) public virtual requiresAuth {
require(capabilityFlag[target][functionSig] == CapabilityFlag.None,"xxx");
```
This condition serves to protect the owner from setting roles as burned or public, thus preventing unnecessary storage wastage.