# Git Cheat Sheet

## How to edit a Git commit message
```
git commit --amend -c <commit ID>
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

## How to correct the last commit message
```git
git commit --amend
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

## Random Branch Naming Tools
* [City Name Generator] (http://www.mithrilandmages.com/utilities/CityNames.php)

