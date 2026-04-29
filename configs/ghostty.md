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
window-save-state = always
font-family = "JetBrainsMonoNL Nerd Font Mono"
font-size = 24
window-padding-x = 20
window-vsync = true
cursor-style-blink = true
window-inherit-working-directory = false
tab-inherit-working-directory = false
working-directory = "home"
macos-titlebar-style = transparent
macos-window-buttons = hidden
```
