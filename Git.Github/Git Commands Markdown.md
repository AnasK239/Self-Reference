# Git CLI Commands with Comments

---
## Basic Commands

```bash
rm -rf .git/  # DELETE THE ENTIRE REPO

mkdir <dir-name>  # Makes a new directory

ls -al  # Shows all present files in the directory

cd <dir-name>  # Change directory

echo "Hello git" >> file.txt  # Add a text file containing the message

cd ..  # Go back to the previous directory
```
---
## Initializing and Tracking

```bash
git init  # Initialize the directory as a git directory to be tracked (initial status: untracked)

git status  # Show tracked/untracked files
# U: Untracked
# M: Modified (Git doesn’t have a snapshot of the latest change)

git add <file>  # STAGING: Make a blob (send to the preparation area to be tracked)

git commit -m "Version 1.0"  # Saves a snapshot to Git for version control

git ls-files  # Shows all files in the index/staging area (also shows how many files are tracked)

git add *  # Adds everything to the staging

git add *.txt  # Add only all text files

git ls-files -s  # Shows files in the staging/indexing area and their SHA hash

git cat-file -t <SHA hash>  # Tells you the type of object that has this SHA hash

git cat-file -p <SHA hash>  # Provides more information
```
---
## Viewing Changes

```bash
git log  # Shows all commit logs

git status -s  # Summary of file status

git diff  # Shows the difference between the WORKING TREE change and the INDEX (not the repository commit)

git diff --staged  # Shows the diff between the staging area and the last committed snapshot
```
---
## Working with HEAD

```bash
# The HEAD points to the snapshot currently in use in the working tree!

git show  # Shows the changes done in a specified commit

git rm --cached <file>  # Remove the tracked status of the file (makes it untracked)

git restore <file>  # Restores the latest version of a file from the staging area/index

git restore --staged <file>  # Removes the latest index

git commit -am "message"  # Adds the file to the staging area and commits it at the same time

git commit --amend  # Allows you to change the last commit message

git reset HEAD~x  # Moves HEAD back by x commits and updates the staging area

git reset HEAD~x --hard  # Moves HEAD back by x commits and updates the working tree

git diff SHA1..SHA2  # Shows the diff between two commits

git reflog  # Shows the changes done to the HEAD pointer

git reset HEAD@{x}  # Fast forward HEAD to the x location and updates the index
```
---
## Tagging

```bash
git tag -a <version X> -m "your message"  # Tags your latest commit with version X

git show <version X>  # Shows all information about version X
```
---
## Branching

```bash
git branch <branch-name>  # Creates an alternate branch

git branch  # Shows all branches

git switch <branch-name>  # Moves the HEAD to this branch

git merge <branch-name>  # Merges all modifications to the master branch

git branch --merge  # Shows branches merged into master

git branch -d <branch-name>  # Deletes a branch
```
---
### Handling Branch Diversion (Non-linear Paths)

```bash
# Merge handles conflicts by creating a new commit node.
# Rebase linearizes the branch.
```
---
## Remote Repositories

```bash
git clone <url>  # Clone a remote/local repository

git remote  # Shows info about the remote repo

git remote -v  # Shows fetch/pull details from the origin repo

git merge <origin/branch>  # Merge changes from remote to local

git fetch <remote-branch>  # Fetch updates from the remote branch

git push <branch-name>  # Push local changes to remote

git push -u <origin> <local-branch>  # Creates a remote branch if it doesn’t exist and pushes local changes

git pull  # Sync downstream changes from remote and merge

git branch -vv  # Show tracking info for local and remote branches

git log --oneline --all  # Show all commits (local & remote)

git merge <remote-name>/<branch-name>  # Merge remote branch into local
```
---
## Adding Images to README

```markdown
![image alt](image_url)
```
---
## Reverting Changes

Revert Changes and Delete Commit

```bash
git reset --hard HEAD~1
git push origin <branch-name> --force
```

 Revert Changes and Keep Commit

```bash
git revert <commit-hash>
git push origin <branch-name>
```

Revert Multiple Commits

```bash
git revert --no-commit <commit-hash1> <commit-hash2> ...
git commit -m "Revert multiple commits"
git push origin <branch-name>
