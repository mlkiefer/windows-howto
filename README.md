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

### Windows Terminal
A decent terminal app
```shell
winget install Microsoft.WindowsTerminal
```

### AutoDarkMode
Switches your screen to dark mode at night
```shell
winget install Armin2208.WindowsAutoNightMode
```

### Shortcut for killing WSL
After hibernating, WSL seems to get into a state where one of its processes `vmmem` hogs a lot of memory and CPU. Killing wsl seems to be the only option so far, e.g by running `taskkill /F /IM wslservice.exe`. You can use the link "Kill WSL" in `bin` to make this more smooth.

# Settings
## environment variables (i.e. PATH)
You can edit environment variables by Win-R `sysdm.cpl` > "Advanced" > "Environment Variables"
Add some paths to PATH:
* C:\Program Files\Git\bin
* C:\msys64\usr\bin
Restart PyCharm afterward to make this effective
