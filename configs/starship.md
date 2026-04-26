# Starship

## Windows
```powershell
$env:USERPROFILE\starship.toml
```

## UNIX
```shell
~/.config/starship.toml
```

## Config
```toml
[character]
success_symbol = '[➜](bold green) '
error_symbol = '[✗](bold red) '

[directory]
truncation_length = 0
read_only	= '🔒'
read_only_style	= 'red'

[git_status]
style = 'bold green'
up_to_date = '✓($style)'

[cmd_duration]
disabled = true
```
