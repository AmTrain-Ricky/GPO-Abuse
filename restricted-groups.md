# Restricted Groups
Add a principal to a local computer group.

## File Path
`\Machine\Microsoft\Windows NT\SecEdit\GptTmpl.inf`

## File Template
```
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
- `S-1-5-21-1078383433-4142403703-1311514137-1105` is the SID of the principal to add

## Tested On
- Server 2016