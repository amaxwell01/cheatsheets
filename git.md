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
