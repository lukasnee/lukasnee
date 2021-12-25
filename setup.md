
# Git
Useful aliases (command shortcuts) you can add:
```shell
git config --global alias.me 'config --global user.name'
git config --global alias.lme 'll --author="<ENTER_YOUR_NAME>"'
git config --global alias.s 'status'
git config --global alias.l "log --pretty=format:'%C(yellow)%h %C(blue)%as%<(9,trunc) %C(magenta)%cL %C(auto)%d %C(cyan)%s'"
git config --global alias.ll "log --pretty=format:'%C(yellow)%h %C(blue)%as%<(9,trunc) %C(magenta)%cL %C(auto)%d %C(cyan)%s %C(white)%b %C(red)%N'"
git config --global alias.lg 'l --graph'
git config --global alias.llg 'll --graph'
git config --global alias.cm 'commit -m'
git config --global alias.ca 'commit --amend'
git config --global alias.cane 'ca --no-edit'
git config --global alias.co 'checkout'
git config --global alias.cob 'co -b'
git config --global alias.ds 'diff --stat'
git config --global alias.ss 'show --stat'
git config --global alias.fa 'fetch --all'
git config --global alias.rc 'rebase --continue'
git config --global alias.suri 'submodule update --recurse --init'
git config --global alias.l5 'lg -t'
git config --global alias.lgmh 'lg origin/master HEAD'

```
> Usage example: `$ git cane` is synonymous to `$ commit --amend --no-edit`

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
## User/keybindings.json

> win full path: `C:\Users\<USERNAME>\AppData\Roaming\Code\User\keybindings.json`


```json
[
    { "key": "ctrl+alt+`", "command": "workbench.action.focusActiveEditorGroup" },
    { "key": "ctrl+k e", "command": "workbench.explorer.fileView.focus" },
    
    { "key": "ctrl+shift+alt+b", "command": "workbench.action.tasks.test" },
    
    { "key": "shift+space i","command": "editor.action.indentationToSpaces" },
    { "key": "shift+space s", "command": "git.stageSelectedRanges", "when": "isInDiffEditor" },
    { "key": "shift+space u", "command": "git.unstageSelectedRanges", "when": "isInDiffEditor" },
    { "key": "shift+space p", "command": "workbench.action.problems.focus" },
    { "key": "shift+space t", "command": "workbench.action.toggleMaximizedPanel"},
    
    { "key": "alt+k", "command": "workbench.action.terminal.resizePaneUp" },
    { "key": "alt+j", "command": "workbench.action.terminal.resizePaneDown" },
    { "key": "alt+h", "command": "workbench.action.terminal.resizePaneLeft" },
    { "key": "alt+l", "command": "workbench.action.terminal.resizePaneRight" },
    { "key": "shift+space b", "command": "workbench.action.tasks.runTask", "args": "Build All (Release)" },
    
    // User/tasks.json
    {
        "key": "shift+space g",
        "command": "workbench.action.tasks.runTask",
        "args": "Open Git Bash in terminal view 1"
    },
    {
        "key": "shift+space 1",
        "command": "workbench.action.tasks.runTask",
        "args": "Open Git Bash in terminal view 1"
    },
    {
        "key": "shift+space 2",
        "command": "workbench.action.tasks.runTask",
        "args": "Open Git Bash in terminal view 2"
    },
    {
        "key": "shift+space 3",
        "command": "workbench.action.tasks.runTask",
        "args": "Open Git Bash in terminal view 3"
    }
]
```

## User/tasks.json

> win full path: `C:\Users\<USERNAME>\AppData\Roaming\Code\User\tasks.json`

```json
{
    // See https://go.microsoft.com/fwlink/?LinkId=733558
    // for the documentation about the tasks.json format
    "version": "2.0.0",
    "tasks": [
        {
            "label": "Open Git Bash in terminal view 1",
            "type": "shell",
            "dependsOn" : [ "Open Git Bash in terminal view" ],
            "windows": {
                "command": "powershell",
                "args": ["git-cmd.exe --command=\"usr/bin/bash.exe\" -l -i "]
            },
            "presentation": {
                "echo": false,
                "focus": true,
                "panel": "new",
                "group": "git"
            }
        },
        {
            "label": "Open Git Bash in terminal view 2",
            "type": "shell",
            "windows": {
                "command": "powershell",
                "args": ["git-cmd.exe --command=\"usr/bin/bash.exe\" -l -i "]
            },
            "presentation": {
                "echo": false,
                "focus": true,
                "panel": "new",
                "group": "git"
            }
        },
        {
            "label": "Open Git Bash in terminal view 3",
            "type": "shell",
            "windows": {
                "command": "powershell",
                "args": ["git-cmd.exe --command=\"usr/bin/bash.exe\" -l -i "]
            },
            "presentation": {
                "echo": false,
                "focus": true,
                "panel": "new",
                "group": "git"
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
