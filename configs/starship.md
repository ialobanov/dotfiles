# Starship

## Windows
```powershell
vim $env:USERPROFILE\starship.toml
```

## UNIX
```shell
vim ~/.config/starship.toml
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
conflicted = '🏳'
ahead = '🏎💨'
behind = '😰'
diverged = '😵'
up_to_date = '✓($style)'
untracked = '🤷'
stashed = '📦'
modified = '📝'
staged = '[++\($count\)](green)'
renamed = '👅'
deleted = '🗑'
```
