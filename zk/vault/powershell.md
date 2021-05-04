# Powerhsell stuff

## Shortcuts
- `Win`+`X`+`A`+`Left`+`Enter` Powershell Admin
- `Win`+`X`+`I` Powershell normal
- `Shift`+`RMB`> Open Powershell Here

## Profile
[Reference](https://ilovepowershell.com/2010/05/27/how-to-create-a-powershell-profile/)
- `$profile` Variable that holds Powershell position
- `new-item $profile -force` create profile if it does not exist
- `ii $profile` open profile
- Add the following to show only current folder
```powershell
Function Prompt { "$( ( Get-Location | Get-Item ).Name ) >" }
```


## Start Folder
https://stackoverflow.com/a/56115537

Right click powershell link
Open working folder