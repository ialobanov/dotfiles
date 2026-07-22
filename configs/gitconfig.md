# .gitconfig

## UNIX

Create:

```sh
vim $HOME/.gitconfig
```

Add configuration:

```ini
[user]
  name = ialobanov
  email = ivan.a.lobanov@gmail.com

[core]
  autocrlf = input
  editor = nvim

[alias]
  che = checkout
  cm = commit
  br = branch
  lg = log --color --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit
  last = log -1 HEAD

[init]
  defaultBranch = main

[pull]
  rebase = true

[fetch]
  prune = true

[includeIf "gitdir:/Users/ivan/Solidsoft/"]
  path = /Users/ivan/.gitconfig-work
```

## Windows

Create:

```powershell
vim $env:USERPROFILE\.ginconfig
```

Add configuration:

```ini
[user]
  name = ialobanov
  email = ivan.a.lobanov@gmail.com

[core]
  editor = nvim
  sshCommand = C:/Windows/System32/OpenSSH/ssh.exe # for windows

[alias]
  che = checkout
  cm = commit
  br = branch
  lg = log --color --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit
  last = log -1 HEAD

[init]
  defaultBranch = main

[pull]
  rebase = true

[fetch]
  prune = true

[includeIf "gitdir:C:/Users/Ivan/Solidsoft/"]
  path = C:/Users/Ivan/.gitconfig-work
```
