My git Aliases
==============


this go on ~/.gitconfig
`
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
	`