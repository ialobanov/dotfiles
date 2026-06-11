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
window_margin_width 10
remember_window_position yes
#background_opacity 0.9
background_blur 64
sync_to_monitor yes
cursor_blink_interval -1
hide_window_decorations titlebar-only

#tabs
active_tab_font_style normal
inactive_tab_font_style normal
tab_bar_margin_width 6.0
tab_bar_style powerline
tab_separator ""
tab_powerline_style angled
tab_title_max_length 28
tab_title_template " {fmt.fg.darkcyan}{index}{fmt.fg.tab} {title} "
#tab_bar_margin_color #5a5ab0
tab_bar_background none

# behaviour
macos_quit_when_last_window_closed yes
confirm_os_window_close 0
enable_audio_bell no
macos_dock_badge_on_bell no
paste_actions quote-urls-at-prompt,replace-dangerous-control-codes,confirm-if-large

# maps
mouse_map right press ungrabbed paste_from_clipboard
copy_on_select yes
map cmd+м paste_from_clipboard
map f1 combine : clear_terminal scrollback active : send_text normal,application \f
map f2 load_config_file

# tabs maps
map Cmd+1 goto_tab 1
map Cmd+2 goto_tab 2
map Cmd+3 goto_tab 3
map Cmd+4 goto_tab 4
map Cmd+5 goto_tab 5
map Cmd+6 goto_tab 6
map Cmd+7 goto_tab 7
map Cmd+8 goto_tab 8
map Cmd+9 goto_tab 9

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
