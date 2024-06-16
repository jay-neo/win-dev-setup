<h1 align="center">Windows <i>pwsh</i> Setup</h1>

### To change execution policy of Powershell

```pwsh
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
```

### To create a new user profile in `pwsh`

Open the following file

```pwsh
notepad $PROFILE.CurrentUserCurrentHost
```

then append this command

```txt
. $env:USERPROFILE\.config\powershell\user_profile.ps1
```

next configure `powershell` folder in `~/.config/` path in your system
👉 [.config repository](https://github.com/jay-neo/.config)

### [PS ReadLine Module](https://github.com/PowerShell/PSReadLine)

Installation:

```pwsh
Install-Module -Name PSReadLine -AllowPrerelease -Scope CurrentUser -Force -SkipPublisherCheck
Set-PSReadLineOption -PredictionSource History
Set-PSReadLineOption -PredictionViewStyle ListView
```

PS Readline Default Location:
`C:\Users\<user>\AppData\Roaming\Microsoft\Windows\PowerShell\PSReadLine`

Open PS Readline History File

```pwsh
notepad (Get-PSReadlineOption).HistorySavePath
```
