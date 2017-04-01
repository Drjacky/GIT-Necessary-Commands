Create an empty Git repository or reinitialize an existing one
```
git init
```
__________
Specifies intentionally untracked files to ignore
```
touch .gitignore
nano gitignore

/FolderNameToIgnore
```
__________
Add file contents to the index
```
git add -A . && git commit -m "yourMessage"
```

(
git add -A is equivalent to  git add .; git add -u
git add -A stages All
git add . stages new and modified, without deleted
git add -u stages modified and deleted, without new
)
__________
Your full name to be recorded in any newly created commits
```
git config user.name "Dr.jacky"
```
Verify the setting
```
git config user.name
```
To set your username for every repository
```
git config --global user.name "Dr.jacky"
```
Verify the setting
```
git config --global user.name
```
__________
Show information about files in the index and the working tree
```
git ls-files file_name --error-unmatch; echo $?
```
will exit with 1 if file is not tracked
__________
Remove files/folder from the working tree and from the index
```
git rm -r --cached myFolder
```
__________
Show commit logs
```
git log
```
__________
List the contents of a commit:
```
git log
git ls-tree --name-only -r     commit_sha
```
__________
To change .git folder path to somewhere else:
```
nano .bashrc
nano /etc/environment

GIT_DIR=/      path to where you want .git folder to be
GIT_WORK_TREE=/       path to project source codes
```
OR
```
git --git-dir=/to/be/ --work-tree=.
```
__________
If you commit and then realize you forgot to stage the changes in a file you wanted to add to this commit, you can do something like this:
```
git commit -m 'initial commit'
git add forgotten_file
git commit --amend
```
__________
Add a single file contents to the index
```
git add hello.html
git commit -m "First Commit"
```
Add Folder:
```
git add <folder>/*
```
__________
List/Content of changes, but not commited yet (working tree status):
```
git status
```
```
git diff --cached
```
```
git diff --staged
```
_______________________________________________________

To rollback to a specific commit:
```
git reset --hard commit_sha
```
