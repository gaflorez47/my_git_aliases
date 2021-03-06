My git Aliases
==============


`~/.gitconfig`


```bash
[color]
	ui = true
[alias]
    c = commit -m
    s = status
    p = pull --rebase
    ps = push
    a = add
    i = add -i
    r = reset .
    undo = reset --soft HEAD^
    sp = ! sh -c 'git stash save && git pull --rebase && git stash apply' --
    d = diff
    ss = stash save
    sc = stash clear
    sa = stash apply
    t = ! branchbrow="https://trello.com/search?q="`git branch | grep '^* ' | cut -c3-` && xdg-open $branchbrow >/dev/null
```

`.gitignore`

```
# Mac OS X hidden files
.DS_Store

# Vim swap files
.*.sw?

# Pow and Powder config
/.pow*

# RVM and rbenv
/.rvmrc
/.rbenv-version

# Bundler binstubs
/bin/

# Rubymine
```


`~/.bash_profile`

```bash
# enable color support of ls and also add handy aliases
if [ -x /usr/bin/dircolors ]; then
    test -r ~/.dircolors && eval "$(dircolors -b ~/.dircolors)" || eval "$(dircolors -b)"
    alias ls='ls --color=auto'
    #alias dir='dir --color=auto'
    #alias vdir='vdir --color=auto'

    alias grep='grep --color=auto'
    alias fgrep='fgrep --color=auto'
    alias egrep='egrep --color=auto'
fi
export CLICOLOR=1
export LSCOLORS=ExFxBxDxCxegedabagacad
# some more ls aliases
alias ll='ls -alF'
alias la='ls -A'
alias l='ls -CF'
export PATH="$HOME/.rbenv/bin:$PATH"
eval "$(rbenv init -)"

alias m="subl"
alias bi="bundle install"
alias be="bundle exec"
alias g="git"
alias copy='xclip -sel clip'

source /usr/share/bash-completion/completions/git
complete -o default -o nospace -F _git g

```

`Sublime keymap`

```
[
	{ "keys": ["ctrl+shift+r"], "command": "reveal_in_side_bar"}
]

```
