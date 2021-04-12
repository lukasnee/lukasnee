
# Git
Useful aliases (command shortcuts) you can add:
```shell
git config --global alias.ll 'log --pretty=oneline --abbrev-commit'
git config --global alias.llme 'll --author="<YOUR NAME>"'
git config --global alias.ds 'diff --stat'
git config --global alias.ss 'show --stat'
git config --global alias.cm 'commit -m'
git config --global alias.cane 'commit --amend --no-edit'
git config --global alias.fa 'fetch --all'
git config --global alias.llg 'll --graph'
git config --global alias.me 'config --global user.name'
git config --global alias.co 'checkout'
git config --global alias.cob 'co -b'
git config --global alias.rc 'rebase --continue'
```
> Usage example: `$ git llg` is synonymous to `$ git log --pretty=oneline --abbrev-commit --graph`

# VScode

If you use Windows + Visual Studio Code + Git Bash this is a very useful vscode task:

## Installation
1. Open VScode
2. Press `F1`, type `open user tasks` and press ENTER
3. Insert code below and save.
## Usage
1. Press `ctrl + p`
2. Type `task git` to find the new task and press ENTER - cheers!
```shell
{
    // See https://go.microsoft.com/fwlink/?LinkId=733558
    // for the documentation about the tasks.json format
    "version": "2.0.0",
    "tasks": [
        {
            "label": "Open Git Bash in terminal view",
            "type": "shell",
            "windows": {
                "command": "powershell",
                "args": ["git-cmd.exe --command=\"usr/bin/bash.exe\" -l -i "]
            },
            "presentation": {
                "echo": false,
                "focus": true,
                "panel": "dedicated",
            }
        }
    
    ]
}
```
# Shell Tricks
Generate a random data file of given size in bytes  
```shell
$ head -c 1024 /dev/urandom > 1KB.dat
```
