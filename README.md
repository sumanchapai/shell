Created to contain general purpose shell scripts

## Installation

Clone repo and add the bin folder from the repo to your `$PATH`.
In bash, add the line (or its equivalent) in `./.bashrc` or
`./bash_profile` or a separate file where you're managing your paths.

```
PATH=$PATH:repolocation/bin
```

## Usage

### `filelines`

`filelines` is supposed to find number of lines for a list of
file names and their sum. Directories are ignored. Usage as follows:

```
ls -a | filelines 

22 README.md
Total: 22
```
Note that `-a` option means to include all files (including hidden).

```
fd --maxdepth 2 --exclude dotbot . ~/dotfiles | filelines

3 /Users/suman/dotfiles/README.md
30 /Users/suman/dotfiles/bash_config/aliases
37 /Users/suman/dotfiles/bash_config/functions
6 /Users/suman/dotfiles/bash_config/paths
13 /Users/suman/dotfiles/bash_config/variables
26 /Users/suman/dotfiles/bash_profile
3 /Users/suman/dotfiles/dart.vim
15 /Users/suman/dotfiles/fish/abbr.fish
101 /Users/suman/dotfiles/fish/aliases.fish
26 /Users/suman/dotfiles/fish/config.fish
204 /Users/suman/dotfiles/fish/functions.fish
14 /Users/suman/dotfiles/fish/paths.fish
9 /Users/suman/dotfiles/fish/variables.fish
3548 /Users/suman/dotfiles/git-completion.bash
586 /Users/suman/dotfiles/git-prompt.sh
17 /Users/suman/dotfiles/gitconfig
1 /Users/suman/dotfiles/haskeline
15 /Users/suman/dotfiles/install
25 /Users/suman/dotfiles/install.conf.yaml
1 /Users/suman/dotfiles/markdown.vim
58 /Users/suman/dotfiles/skhdrc
20 /Users/suman/dotfiles/tmux.conf
1 /Users/suman/dotfiles/vim.vim
230 /Users/suman/dotfiles/vimrc
30 /Users/suman/dotfiles/yabairc
Total: 5019
```
In the above example, `fd` is used. You could use
`find` command as well. Or even a simple txt file that contains the
names of the files would want to count lines of. If you had a
`files-to-count.txt` you would do
```
cat files-to-count.txt | filelines
```
