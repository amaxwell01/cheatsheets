# Git Cheat Sheet

## How to edit a Git commit message
```
git rebase -i HEAD~1
git commit --amend -c <commit ID>
```

## How to correct the last commit message
```git
git commit --amend
```

## Git/Github configuration
```
git config --global color.ui true
git config --global user.name "Andrew Maxwell"
git config --global user.email "amaxwell01@gmail.com"
ssh-keygen -t rsa -C "amaxwell01@gmail.com"
```
## Add it to your GitHub ssh account page
```
cat ~/.ssh/id_rsa.pub | clipboard
```

## Test if it works:
```
ssh -T git@github.com
```
## How to do a git svn dcommit dry run
```
git diff git-svn HEAD
```

## How to view local branches
```git
git branch
```

## How to view all branches, including remote branches
```git
git branch -a
```


## Check to see which branches are merged into HEAD
```git
git branch --merged
git branch --no-merged
```

## How to delete a branch locally
```git
git branch -d <name_of_branch>
```

## How to delete a branch (even if not merged)
```git
git branch -D <name_of_branch>
```

### How to delete a remote branch
```git
git push origin :<name_of_remote_branch>
```

## How to clear the cache for a specific file/folder
```git
git rm -r --cached <name_of_file_or_folder>
```

## Random Branch Naming Tools
* [City Name Generator] (http://www.mithrilandmages.com/utilities/CityNames.php)

## How to fix all attributes after sycing Google Drive with Git to a new machine
```
git checkout .
```
warning: Watch out; if you really *have* changed any files, the changes will be lost.)


## Git Tags
How to create a tag
```
git tag [name_of_tag]
```

How to push up tags
```
git push --tags
```

How to view the changes of a file
```
gitk [name_of_file]
```

How to view all changes by a specific user
```
git log --stat --author=andrew
```

How to view all changes to a specific file by a specific user
```
git log --author=andrew [name_of_file]
gitk --author=andrew [name_of_file]
```
