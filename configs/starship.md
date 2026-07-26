# Starship

## Windows
```powershell
$env:USERPROFILE\starship.toml
```

## UNIX
```shell
vim ~/.config/starship.toml
```

## Config
```toml
# ~/.config/starship.toml
command_timeout = 1000

[character]
success_symbol = '[➜](bold green)'
error_symbol = '[➜](green)'

[directory]
truncation_length = 0
read_only = '🔒'
read_only_style = 'red'

[git_status]
style = 'bold green'
up_to_date = '✓($style)'

[cmd_duration]
disabled = true
```
