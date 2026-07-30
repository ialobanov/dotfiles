# SSH

## UNIX

```sh
mkdir -p ~/.ssh && vi ~/.ssh/config
```

## Windows

```powershell
if (!(Test-Path "$env:USERPROFILE\.ssh")) { New-Item -Path "$env:USERPROFILE\.ssh" -ItemType Directory -Force }
vim $env:USERPROFILE\.ssh\config
```

## Configuration

```ini
# main ssh configuration

# specific overrides
Host 10.24.0.* hl-*
    StrictHostKeyChecking off
    UserKnownHostsFile /dev/null

# global settings
Host *
    PreferredAuthentications publickey,password,keyboard-interactive
    StrictHostKeyChecking accept-new
    UserKnownHostsFile ~/.ssh/known_hosts
    UpdateHostKeys yes
    IdentityFile none
    SetEnv TERM=xterm-256color
```
