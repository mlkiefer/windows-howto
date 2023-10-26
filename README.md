# Software
you can use winget to install packages

## Platform tools
### RancherDesktop
Kubernetes in windows
```shell
winget install suse.RancherDesktop
```
disable the traefik ingress to use a native ingress controller

### OpenTofu
Replacement for terraform
```shell
winget install OpenTofu.Tofu.Alpha
```

### KeePass
Password safe
```shell
winget install KeePassXCTeam.KeePassXC
```

## Tools for making Windows halfway bearable
### Powershell
Password safe
```shell
winget install microsoft.powershell
```

### PowerToys
Password safe
```shell
winget install microsoft.powertoys
```

### MSys2
Development tools (includes zsh)
```shell
winget install msys2.msys2
```
* open an msys terminal
* install zsh `pacman -S msys/zsh`
* set the home dir to the windows home dir: `nano /etc/nsswitch.conf`, change the entry to `db_home: windows cygwin desc` 
* In PyCharm set `C:\msys64\usr\bin\zsh.exe` as the terminal path

Make a link for running zsh in the start menu:
In this repo's directory run `cp bin/zsh.lnk ~/AppData/Roaming/Microsoft/Windows/Start\ Menu`

# Settings
## environment variables (i.e. PATH)
You can edit environment variables by Win-R `sysdm.cpl` > "Advanced" > "Environment Variables"
Add some paths to PATH:
* C:\Program Files\Git\bin
* C:\msys64\usr\bin
Restart PyCharm afterward to make this effective
