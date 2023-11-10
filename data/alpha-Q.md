In RolesAuthority::canCall we see the following code
```
return bytes32(0) != getUserRoles[user] & getRolesWithCapability[target][functionSig];
```

In Solidity the & operator will be executed before != but this might not always be clear and might be different in other languages. I suggest adding braces around getUserRoles[user] & getRolesWithCapability[target][functionSig] to clarify operator precedence.