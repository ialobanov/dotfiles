# tmux

## UNIX

```~~
mkdir -p $HOME/.config/tmux
vim %HOME/.config/tmux/tmux.conf
~~ ```

```~~
tmux-source $HOEM/.config/tmux/tmux.conf
~~ ```

```ini
set -g default-terminal "xterm-256color"
set -ga terminal-overrides ",xterm-256color:Tc"
set -g base-index 1
setw -g pane-base-index 1

set -g mouse on
set -g mode-keys vi

# Reload settings
bind r source-file ~/.config/tmux/tmux.conf \; display "Reloaded!"

# action key
unbind C-b
set-option -g prefix C-p
set-option -g repeat-time 0
set-option -g focus-events on

set-option -g status-justify "left"

set -g status-right ""
set -g status-style "fg=green,bg=#1e3859"
set -g window-status-format "#I:#W"
set -g window-status-current-format " [#I:#W] "
set -g window-status-style "fg=colour244,bg=default"
set -g window-status-current-style "fg=green,bg=colour240"

set -g set-titles off
set -g mode-style "fg=default,bg=default,reverse"
```
``````
