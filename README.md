Create an empty Git repository or reinitialize an existing one
```
git init
```
__________
Specifies intentionally untracked files to ignore
```
touch .gitignore
```
__________

nano gitignore

/out

git add -A . && git commit -m "yourMessage"


(
git add -A is equivalent to  git add .; git add -u:::::
git add -A stages All
git add . stages new and modified, without deleted
git add -u stages modified and deleted, without new
)



To set your username for a specific repository : 
git config user.name "Billy Everyteen"
# Set a new name
git config user.name
# Verify the setting

To set your username for every repository
git config --global user.name "Billy Everyteen"
# Verify the setting
git config --global user.name
Billy Everyteen


__________

git ls-files file_name --error-unmatch; echo $?
will exit with 1 if file is not tracked
__________



to remove a folder from repo:

git rm -r --cached myFolder


to list all files in a commmit:
git log
git ls-tree --name-only -r     sha1 of commit


_________
to change .git folder to somewhere else:
nano .bashrc
nano /etc/environment

add
GIT_DIR=/      path to where you want .git folder to be
GIT_WORK_TREE=/       path to project source codes


OR


git --git-dir=/to/be/ --work-tree=.


__________________________________________________
edit a commit:
git commit --amend

vaghti ke ye taghyire dobare too ye file ee midi ke commit karde budi, age khasti too hamun comment dobare befrestish, dastoore bala, save mikoni, khodesh commit mikone dige.
____________________
Add single file:
git add hello.html
git commit -m "First Commit"

Add Folder:
git add <folder>/*
______________________________
List/Content of changes, but not commited yet:
git status
git diff --cached   OR      git diff --staged
_______________________________________________________

To rollback to a specific commit:

git reset --hard commit_sha
