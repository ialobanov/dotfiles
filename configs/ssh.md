# SSH

Windows:

```powershell
$env:USERPROFILE\.ssh\config
```


UNIX:

```sh
~/.ssh/config
```


Configuration:

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
