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

### Make and Delete Branch
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
### Check Differences
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

#### pull

```
$ git pull
```

```
$ git pull origin {branch name}
```

