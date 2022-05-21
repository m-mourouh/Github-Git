## Terms
. Directory -> folder
. CLI -> command line interface
. cd -> change directory
. respository -> project or the place where your project is kept
. Github -> website to host your respositories online

## Git commands 1
. clone : Bring a repository that is hosted somewhere like Github into your local machine

. add : Track your files and changes in Git

. commit : save your files in Git

. push : upload commits to a remote repo, like Github

. pull : download changes from remote repo to your local machine , the opposite of push

## Github
. in commits red => deleted , green => added , w/b => no chages

## Git commands 2 (existing repo that we clonned)
`git clone url` : to clone the repo 
`ls -la` : shows the all file and floder inclding the hidden ones (.git tracks the history of repo commits).
. git status -> shows all files that were created , updated or deleted 
. track files : git add . | git add <filename> | git add index.html
. commit or save code locally : git commit -m 'message 1' -m 'description' 
## SSH KEYS 
. to push your code to github you need to prove to github u're the owner 
. generate ssh key : ssh-keygen -t <encription-type> -b <length> -C 'eamil'
. Read the pub file : cat id_rsa.pub and copy it then add it to you github account 
. eval "$(ssh-agent -s)"
. ssh-add ~/.ssh/id_ed25519
# push changs to respo 
. git push origin <branche-name>(main|master)
origin = stands for location of the repo

# unexisted repo 
. git init : to intialize empty Git repository
. git status : see details 
. git add <..> : tack files 
. git commit -m 'msg1' -m 'msg2' : save code locally
. create an empty respo in github 
. git remote add origin url : connect to the repo
. git remote -v : see the connected repos
. git push origin master | git push -u origin master (-u : upstream . it makes it deafult so next time we will write only git push)

# Branching 
. git branch : shows the branches 
. git checkout <brache> : switchs between  branches
. git checkout -b <branch> : create new branch 
. git push -u origin <branch> : upload changes to the branch 
. # git diff : shows changes u made
. (branch-1)# git diff <branch-2> : compares btw tow branches 
. (branch-1)# git merge <branch-2> :merge the braches 
#if there are some merge conflicts you should fix them manaully
. git branch -d <branch>  #delete brach after merge

# PR or Pull request 
Pull requests let you tell others about changes you've pushed to a branch in a repository on GitHub. Once a pull request is opened, you can discuss and review the potential changes with collaborators and add follow-up commits before your changes are merged into the base branch.

- pull down the changes to the local machine
-> git pull origin <branch>
- if set-upstream is set , u can write only
-> git pull

#stage or unstage => means tracked or no

# Undoing Git
-> git reset | git reset <filename> #undo all or one file
-> git reset HEAD~1 #HEAD is pointer to last commit (undo one commit back)
-> git log #shwo all commits 
-> git reset <commit-hash> #pointe to specified commit in git 
-> git reset --hard <commit-hash> #point to specified commit in git and get all changes 
