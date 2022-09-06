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
