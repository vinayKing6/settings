#initial
    git init
#add remote repository(have ssh key in your system)
    git remote add <local name> <remote repository name on github>
#add file
    git add -A <file-name> (parameter '-A' means to cache stage)
#commit files
    git commit -a -m "<your statement>"
#push to remote repository
    git push -u <local name> <branch>
