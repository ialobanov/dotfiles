# zprofile

## UNIX

```sh
~/.zprofile
```

## Config

```sh
# initialize homebrew environment (for Apple Silicon)
eval "$(/opt/homebrew/bin/brew shellenv)"
# set up ssh agent for Bitwarden
export SSH_AUTH_SOCK=/Users/ivan/.bitwarden-ssh-agent.sock
# fzf
export FZF_DEFAULT_OPTS='--no-height --no-reverse'

# Fix Ansible "A worker was found in a dead state" on macOS
export OBJC_DISABLE_INITIALIZE_FORK_SAFETY=YES
export OS_ACTIVITY_MODE=disable

# proxy
#export http_proxy=http://127.0.0.1:10888
#export https_proxy=$http_proxy
```
