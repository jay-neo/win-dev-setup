<h1 align="center">Windows Terminal Setup</h1>

### To create user profile
```pwsh
notepad $PROFILE.CurrentUserCurrentHost
```
```
. $env:USERPROFILE\.config\powershell\user_profile.ps1
```

👉 [dot config folder](https://github.com/jay-neo/.config)

### To change execution policy of Powershell
```pwsh
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
```

### [git](https://git-scm.com/download/win)
```pwsh
winget install --id Git.Git -e --source winget
```


### [scoop](https://scoop.sh/)
```pwsh
iwr -useb get.scoop.sh | iex
```


### [neovim gcc](hhttps://github.com/neovim/neovim)
```pwsh
scoop install neovim gcc
```

### [nvm](https://github.com/nvm-sh/nvm)
```pwsh
scoop install nvm
```

### [yarn](https://yarnpkg.com/)
```pwsh
scoop install yarn
```


### [Github Cli](https://cli.github.com/)
```pwsh
scoop install gh
```


### [Oh My Posh](https://ohmyposh.dev/docs/installation/windows)
```pwsh
Install-Module oh-my-posh -Scope CurrentUser -Force
```


### [Terminal Icons](https://github.com/devblackops/Terminal-Icons)
```pwsh
Import-Module Terminal-Icons -Repository PSGallery -Force
```


### [z directory jumper](https://github.com/rupa/z)
```pwsh
Install-Module -Name z -Force
```


### [PS ReadLine Module](https://github.com/PowerShell/PSReadLine)
```pwsh
Install-Module -Name PSReadLine -AllowPrerelease -Scope CurrentUser -Force -SkipPublisherCheck
Set-PSReadLineOption -PredictionSource History
Set-PSReadLineOption -PredictionViewStyle ListView
```
PS Readline Default Location:
`C:\Users\Acer\AppData\Roaming\Microsoft\Windows\PowerShell\PSReadLine`
```pwsh
notepad (Get-PSReadlineOption).HistorySavePath
```
