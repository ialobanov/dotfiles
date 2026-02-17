# ghostty

## Windows
```powershell
mkdir $env:USERPROFILE\ghostty\; vim $env:USERPROFILE\ghostty\config

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

background-opacity = 0.96
background-blur-radius = 20

font-family = "JetBrainsMono Nerd Font Mono"
font-size = 24

window-padding-x = 20
window-vsync = true
adjust-cursor-thickness = 13
cursor-color = "#FFC300"
cursor-style-blink = true
window-inherit-working-directory = false
working-directory = "home"
macos-titlebar-style = tabs
```

Color for 3 & 11

```shell
zed /Applications/Ghostty.app/Contents/Resources/ghostty/themes/Whimsy
```
