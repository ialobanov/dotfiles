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
format = """
$hostname\
$memory_usage\
$time\
$directory\
$git_branch\
$git_status\
$lua\
$fill\
$battery\
$jobs\
$new_line
$docker_context\
$character"""

[line_break]
disabled = true

[hostname]
ssh_only = false
format = '[$hostname]($style)'
style = 'bold blue'

[memory_usage]
disabled = false
threshold = -1
symbol = ''
format = '$symbol [\[${ram}\]]($style) '
style = 'bold green'

[directory]
truncation_length = 0
truncate_to_repo = false
read_only_style = 'bold red'
read_only = '🔒'
format = ' [$read_only]($read_only_style)[$path]($style) '
fish_style_pwd_dir_length = 0
use_logical_path = false

[git_branch]
symbol = ' '
truncation_length = 255
truncation_symbol = ''

[git_status]
conflicted = ' '
ahead = '⇡${count} '
behind = '⇣${count} '
diverged = '⇕⇡${ahead_count}⇣${behind_count} '
untracked = ''
stashed = ''
modified = ''
staged = ''
renamed = ''
deleted = ''
up_to_date = '󰗠'
style = 'bold green'

[time]
disabled = false
format = '[$time]($style)'
time_format = '%H:%M'
style = 'bold yellow'
[lua]
format = 'via [$symbol($version )]($style)'
symbol = ' '

[fill]
symbol = ' '

[jobs]
symbol = ' '
style = 'red'
number_threshold = 1
format = '[$symbol]($style)'

[docker_context]
format = 'via [🐋 $context](blue bold)'

[battery]
full_symbol = '🔋 '
charging_symbol = '⚡️ '
discharging_symbol = '💀 '

[[battery.display]]
threshold = 10
style = 'red'
discharging_symbol = '󰂎 '

[[battery.display]]
threshold = 80
style = 'yellow'
discharging_symbol = '󰁽 '

[character]
disabled = false
success_symbol = '[➜](bold green)'
error_symbol = '[➜](bold red)'
vimcmd_symbol = '[⮜](bold green)'
vimcmd_replace_one_symbol = '[⮜](bold purple)'
vimcmd_replace_symbol = '[⮜](bold purple)'
vimcmd_visual_symbol = '[⮜](bold yellow)'
```
