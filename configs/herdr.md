# hedrd

## UNIX

```sh
vim ~/.config/hedrd/hedrd.toml
```

## Config

```toml
onboarding = false

[theme]
name = "dracula"
auto_switch = false

[ui]
status_indicators = "dots"
sidebar_width = 16
hide_tab_bar_when_single_tab = true
pane_gaps = false

[ui.sound]
enabled = false

[ui.toast]
delivery = "terminal"

[keys]
switch_workspace = "prefix+1..9"
previous_workspace = "prefix+up"
next_workspace = "prefix+down"
clear_pane = "f1"

[session]
resume_agents_on_restore = true
```
