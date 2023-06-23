# initial:

```shell
 git init
```

#add ssh key for github commit
```shell
ssh-keygen -t rsa -C "your email"
cd ~/.ssh
vim id_rsa.pub
#copy all key into github
```

# add remote repository(have ssh key in your system):

```shell
    git remote add <local name> <remote repository name on github>
```

# add file:

```shell
git add -A <file-name> (parameter '-A' means to cache stage)
```

# commit files:

```shell
git commit -a -m "<your statement>"
```

# push to remote repository:

```
git push -u <local name> <branch>
```

#pull new update from github if local one is old while project is updated from other computers (pls commit and push at once and pull before modify)
```shell
git pull
```

