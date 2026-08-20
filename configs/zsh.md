# zsh

## .zshenv

```sh
vi $HOME/.zshenv
```

```sh
export XDG_CONFIG_HOME="${XDG_CONFIG_HOME:-$HOME/.config}"
[[ -d "$XDG_CONFIG_HOME/zsh" ]] && export ZDOTDIR="$XDG_CONFIG_HOME/zsh"
```

## .zprofile

```sh
vi $HOME/.config/zsh/.zprofile
```

```sh
# ~/.config/zsh/.zprofile

# initialize homebrew environment (for Apple Silicon)
eval "$(/opt/homebrew/bin/brew shellenv)"

# set up ssh agent for bitwarden
export SSH_AUTH_SOCK=/Users/ivan/.bitwarden-ssh-agent.sock

# fix ansible "a worker was found in a dead state" on macos
export OBJC_DISABLE_INITIALIZE_FORK_SAFETY=YES
export OS_ACTIVITY_MODE=disable
```

## .zshrc

```sh
vi $HOME/.config/zsh/.zshrc
```

```sh
# ~/.config/zsh/.zshrc

# history
if [[ -z "$HISTFILE" ]]; then
    HISTFILE="$ZDOTDIR/.zsh_history"
fi
SAVEHIST=20001
HISTSIZE=30000
setopt EXTENDED_HISTORY
setopt HIST_BEEP
setopt HIST_EXPIRE_DUPS_FIRST
setopt HIST_FIND_NO_DUPS
setopt HIST_IGNORE_DUPS
setopt HIST_IGNORE_SPACE
setopt HIST_REDUCE_BLANKS
setopt INC_APPEND_HISTORY

# completion
autoload -Uz compinit
compinit

# interactive tool configurations
export FZF_DEFAULT_OPTS='--no-height --no-reverse'

# alias
alias vim='nvim'
alias v='nvim'
alias hosts='sudo vim /etc/hosts'
alias sudo='sudo '
alias cle='clear'
alias fe='yazi'
alias ll='eza -laF --smart-group --icons=always'
alias g='git '
alias gst='git status'
alias gll='git pull'
alias gp='git push'
alias gco='git commit -am '
alias gf='git diff'
alias bat='bat --theme=TwoDark '
alias sshk='kitty +kitten ssh '
alias vkh='nvim .ssh/known_hosts'
alias sr='source $XDG_CONFIG_HOME/zsh/.zshrc'

# functions
gsh() {
    git add . &&
    git commit -m "." &&
    git push &&
    clear
}

ssv() {
    cd "$HOME/solidsoft/projects/solidwall-vault/" || return
    git add .
    { git commit -m "Update vault" || true; } &&
    git push
    cd - &&
    clear
}

myv() {
    cd "$HOME/projects/my-vault/" || return
    git add .
    { git commit -m "Update vault" || true; } &&
    git push
    cd - &&
    clear
}

ua() {
    brew update &&
    brew upgrade -y &&
    brew cleanup
}

# prompt
source <(fzf --zsh)
eval "$(starship init zsh)"
eval "$(zoxide init zsh)"

# proxy
export http_proxy=http://10.24.0.254:10888
export https_proxy=$http_proxy
export HTTP_PROXY="$http_proxy"
export HTTPS_PROXY="$https_proxy"
export no_proxy="10.24.0.0/24,.yandex.net,.solidwall.io"
export NO_PROXY="$no_proxy"
```

## brew

```sh
touch .hushlogin
source $HOME/.zprofile
brew -y install eza fzf zoxide gnu-tar starship neovim
brew install --cask kitty font-jetbrains-mono-nerd-font stats
```
