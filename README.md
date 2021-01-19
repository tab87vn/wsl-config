# wsl-config

## Install WSL
- Enable WSL: `dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart`
- Update to WSL2: `dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart`
- Set WSL2 as default: `wsl --set-default-version 2`

## Misc
- Set default user: `ubuntu-18.04.exe config --default-user tbui  
- Set default wsl distro: `.\wslconfig.exe /s ubuntu-18.04`

## Change location of WSL distros
- Stop WSL: `wsl --shutdown`
- Backup distro: `wsl --export distro-name d:\path\to\backup.tar`
- Stop distro: `wsl --unregister distro-name`
- Import distro: `wsl --import distro-name e:\path-to-distro-dir d:\path\to\backup.tar`

## Set background color
In `.zshrc`:
- `eval ``dircolors /mnt/e/workspace/git/dircolors-solarized/dircolors.256dark``
- `export LS_COLORS="$LS_COLORS:ow=1;34:tw=1;34:"`
