# Git

## Development Flow

## Git Command List

### Clone
```
$ git clone {url}
```
### Check Branch
check current branch
```
$ git branch
```
check all branch
```
$ git branch -a
```

### Branch Operation
#### make
make new branch from current branch
```
$ git branch {branch name}
```
chage current branch
```
$ git checkout {branch name}
```
make new branch and change current branch to the new branch
```
$ git checkout -b {branch name}
```
#### delete
delete branch
```
$ git branch -d {branch name}
```
delete branch with force
```
$ git branch -D {branch name}
```
push deleted branch to remote repository
```
$ git push origin :{deleted branch name}
```
#### fetch
```
$ git fetch origin {branch name}
```
#### merge
merge current branch from {branch name}
```
$ git merge {branch name}
```
recover from merge
```
git merge --no-ff {branch name}
```
#### pull
pull includes fetch and merge
```
$ git pull
```

```
$ git pull origin {branch name}
```
### Check
#### check differences
check differences in local repository.
```
$ git status
```

check file differences in local repository.

```
$ git diff
```
```
$ git diff {file path}
```

#### check log (commits)
```
$ git log
```
```
$ git log --oneline --graph --decorate
```

### Stage
add new or modified file to staging
```
$ git add {file path}
```
add deleted file to staging
```
$ git rm {file path}
```
cansel staging file
```
$ git rm --cached {file path}
```

#### commit
```
$ git commit
```
```
$ git commit -m "{comment}"
```


#### push

```
$ git push
```

```
$ git push origin {branch name}
```

### Repository
#### check
check differences between local and remote repository
```
$ git remote prune —dry-run origin
```
#### sync
sync local and remote repository. This command will change only local repository.
```
$ git remote prune
```
