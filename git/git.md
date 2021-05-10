Working with Git on the command line can be daunting. To help with that, we’ve put together a list of common Git commands, what each one means, and how to use them. Our hope is that this makes Git easier to use on a daily basis.

## git init

>    This command turns a directory into an empty Git repository. This is the first step in creating a      repository. After running git init, adding and  committing files/directories is possible. 


Usage:

```
# change directory to codebase
$ cd /file/path/to/code

# make directory a git repository
$ git init
```

## git add
```
# To add all files not staged:
$ git add .

# To stage a specific file:
$ git add index.html

# To stage an entire directory:
$ git add css
```
## git commit
```
# Adding a commit with message
$ git commit -m "Commit message in quotes"
```
## git status
```
$ git status
```
## git config
```
# Running git config globally
$ git config --global user.email "rakib@emailaddress.com"
$ git config --global user.name "Rakib01"

# Running git config on the current repository settings
$ git config user.email "rakib@emailaddress.com"
$ git config user.name "Rakib01"
```
## git branch
```
# Create a new branch
$ git branch <branch_name>

# List all remote or local branches
$ git branch -a

# Delete a branch
$ git branch -d <branch_name>
```

## git checkout
```
# Checkout an existing branch
$ git checkout <branch_name>

# Checkout and create a new branch with that name
$ git checkout -b <new_branch>
```
## git merge
```
# Merge changes into current branch
$ git merge <branch_name>
```
## git remote
```
# Add remote repository
$ git remote <command> <remote_name> <remote_URL>

# List named remote repositories
$ git remote -v
```
## git clone
```
$ git clone <remote_URL>
```
## git pull
```
$ git pull <branch_name> <remote_URL/remote_name>
```
## git push
```
$ git push <remote_URL/remote_name> <branch>

# Push all local branches to remote repository
$ git push —all
```
## git stash
```
# Store current work with untracked files
$ git stash -u

# Bring stashed work back to the working directory
$ git stash pop
```
## git log
```
# Show entire git log
$ git log

# Show git log with date pameters
$ git log --<after/before/since/until>=<date>

# Show git log based on commit author
$ git log --<author>="Author Name"
```
## git rm
```
# To remove a file from the working index (cached):
$ git rm --cached <file name>

# To delete a file (force):
$ git rm -f <file name>

# To remove an entire directory from the working index (cached):
$ git rm -r --cached <directory name>

# To delete an entire directory (force):
$ git rm -r -f <file name>
```
