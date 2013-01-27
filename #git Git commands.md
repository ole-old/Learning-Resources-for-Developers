#git Git commands.md

Git helps us to be smarter programmers when we are alone and stronger when we work together.

# Basics of working locally


## start a git repository in the current folder
git init

This creates a .git folder in the current directory.


## prepare to commit file(s)
git add {filename or directory}
git add {filename or directory}


## See which files have changed and which files are queued for commit
git status


## commit files
git commit -m "{your commit message here}"


## Delete a file
git rm {file name}

for a directory...

git rm -r {directory name}


## Delete all missing files (as seen in a git status)
This one is in case you deleted a file not using "git rm {file}"
from http://stackoverflow.com/questions/1402776/how-do-i-commit-all-deleted-files-in-git

git add -u


## rename a file
git mv {original file name} {new file name}
git commit -m "Renamed a file :)"


## See history
git log

... or for a graphical user interface ....
gitk



# Working with branches locally

## see available branches
git branch

## create a new branch from the current branch and switch to it
git branch {new branch name}
git checkout {new branch name}

## go back to specific commit and create a new branch from it
git checkout {hash of the commit}
git branch {new branch name}
git checkout {new branch name}



# Working with remote repositories

## clone a remote repository to your local machine
git clone {url of the repository}

Example using HTTP... 

git clone https://github.com/open-learning-exchange/BeLL-School-Library.git

Example using using SSH...

git clone git@github.com:open-learning-exchange/BeLL-School-Library.git


## Pull remote commits to local repository
git pull


## Push local commits to remote repository
git push {name of remote server} {name of local branch}

When tracking is set up correctly (often automatically) you can just do "git push".  Note that you may need to do a git pull and resolve merge conflicts before you can git push.


## checkout a remote branch
Show the remote branches...

git branch -a

Now pick one and check it out...

git checkout {remote repository name}/{name of branch}
git branch {name of branch}
git checkout {name of branch}

Example...

git checkout origin/some-branch-name
git branch {name of branch}
git checkout {name of branch}


## push a local branch to a remote git repository
git push -u {remote repository name} {name of local branch}

Exampple...
git push -u origin experimental






