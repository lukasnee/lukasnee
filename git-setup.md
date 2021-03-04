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
```
> Usage example: `$ git llg` is synonymous to `$ git log --pretty=oneline --abbrev-commit --graph`
