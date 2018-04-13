# User Rights Assignment
Assign granular rights to a principal outside of group membership.

## File Path
`\Machine\Microsoft\Windows NT\SecEdit\GptTmpl.inf`

## File Template
```
[Unicode]
Unicode=yes
[Version]
signature="$CHICAGO$"
Revision=1
[Privilege Rights]
SeRemoteInteractiveLogonRight = *S-1-5-21-1078383433-4142403703-1311514137-1105
SeTakeOwnershipPrivilege = *S-1-5-21-1078383433-4142403703-1311514137-1105
SeLoadDriverPrivilege = *S-1-5-21-1078383433-4142403703-1311514137-1105
SeDebugPrivilege = *S-1-5-21-1078383433-4142403703-1311514137-1105
```

## Tested On
- Server 2016