# ghostty

## Windows
```powershell
mkdir -p $env:USERPROFILE\ghostty\.config\; vim $env:USERPROFILE\ghostty\config

```

## UNIX
```shell
mkdir -p $HOME/.config/ghostty && vim $HOME/.config/ghostty/config
```

## Config
```properties
term = xterm-256color
theme = Whimsy
shell-integration = zsh
window-save-state = always

font-family = "JetBrainsMonoNL NFM Bold"
font-style-bold = true
font-size = 26

window-padding-x = 20
window-vsync = true
cursor-color = "#FFC300"
cursor-style-blink = true
window-inherit-working-directory = false
tab-inherit-working-directory = false
working-directory = "home"
macos-titlebar-style = tabs
```
