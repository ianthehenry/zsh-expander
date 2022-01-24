# zsh-expander

zsh-expander is a `zle` widget ("zsh plugin") that allows you to write custom expansions and select them with `fzf`. For example:

```
$ git revise .c<TAB>
```

Will let you select a git commit to [revise](https://github.com/mystor/git-revise).

It depends on `fzf` and `perl`.

This is different from typical zsh completion because it's entirely predictable and works for any command: completions are only based on the trigger word that you type, not the completion script for the command you happen to be running. It is also *much* faster than builtin shell completion.

Currently the triggers are hardcoded:

- `.b` git branches
- `.c` git commits
- `.d` dirty git files
- `.f` any file/directory, recursively

But a future version will make them configurable.

This isn't really... released yet. This is just me trying to clean up my `.zshrc`.
