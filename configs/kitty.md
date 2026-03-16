# Kitty

## UNIX

```sh
vim ~/.config/kitty/kitty.conf
```

## Config

```ini
# vim:fileencoding=utf-8:foldmethod=marker
# font
font_family family='JetBrainsMono Nerd Font Mono'
font_size 24.0
bold_font auto
italic_font auto
bold_italic_font auto
# appearance
window_padding_width 6
remember_window_position yes
background_opacity 0.9
background_blur 45
sync_to_monitor yes
tab_bar_style fade
tab_title_max_length 30
dim_opacity 0.4
macos_quit_when_last_window_closed yes
confirm_os_window_close 0
hide_window_decorations titlebar-only
# behaviour
enable_audio_bell no
macos_dock_badge_on_bell no
# maps
mouse_map right press ungrabbed paste_from_clipboard
copy_on_select yes
map cmd+м paste_from_clipboard
map f1 combine : clear_terminal scrollback active : send_text normal,application \f
map f2 load_config_file
# theme
include current-theme.conf
```

## Theme

```sh
vim ~/.config/kitty/current-theme.conf
```

```ini
## name: Cherry
## author: nullxception
## license: GPLv3
## upstream: https://github.com/nullxception/cherry-kde/raw/main/kitty/cherry.conf

foreground #bdc3df
background #1f1f2a
selection_foreground #1f1f2a
selection_background #bdc3df

cursor #bdc3df
cursor_text_color #1f1f2a
url_color #85b6ff

tab_bar_background #1f1f2a
active_tab_foreground #bdc3df
active_tab_background #5d6980
inactive_tab_foreground #4d576b
inactive_tab_background #1f1f2a

color0  #5d6980
color1  #ff568e
color2  #64de83
color3  #FFC300
color4  #73a9ff
color5  #946ff7
color6  #62c6da
color7  #dedeff
color8  #53536b
color9  #ff69a2
color10 #73de8a
color11 #FFC300
color12 #85b6ff
color13 #a481f7
color14 #71c2d9
color15 #ebebff
```
