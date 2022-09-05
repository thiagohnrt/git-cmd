# GIT Command
- [Getting Started - Setup](#git-setup)
  - [Install Git](#install-git)
  - [Identify](#identify)
- [Repository](#repository)
  - [Create a new repository](#create-a-new-repository)
  - [Push an existing repository](#push-an-existing-repository)
  - [Clone repository with branch](#clone-repository-with-branch)
- [Branch](#branch)
  - [Update branch](#update-branch)
  - [Commit and push](#commit-and-push)
  - [Create new branch from current branch](#create-new-branch-from-current-branch)
  - [Rename branch](#rename-branch)
  - [Merge branch](#merge-branch)
  - [Reset pushed commit](#reset-pushed-commit)
  - [Delete branch](#celete-branch)
    - [Local](#local)
    - [Remote](#remote)
  - [Branch list](#branch-list)
  - [Commit History](#commit-history)

# Git Setup

### Install Git

https://git-scm.com/downloads<br/>
https://git-scm.com/book/en/v2/Getting-Started-Installing-Git

### Identify
```
git config --global user.name "Thiago Honorato"
git config --global user.email thiagohonorato@example.com
```

# Repository
### Create a new repository
```
git init
git add <path|file_name>
git commit -m "message"
git branch -M <branch_name>
git remote add origin <repository>
git push -u origin <branch_name>
```
### Push an existing repository
```
git remote add origin <repository>
git branch -M <branch_name>
git push -u origin <branch_name>
```
### Clone repository with branch
```
git clone -b <branch_name> <repository>
```
# Branch
### Update branch
```
git pull origin <branch_name>
```
### Commit and push
```
git add <path|file_name>
git commit -m "message"
git push origin <branch_name>
```
### Create new branch from current branch
```
git checkout -b <branch_name>
```
### Rename branch
```
git branch -m <old_branch> <new_branch>
git branch -M "<new_branch>" (other way)

git push -u origin <new_branch>
```
### Merge branch
```
git checkout <branch_main>
git merge <branch_with_feature>
```
### Reset pushed commit
```
git reset --hard <commit_id>
git push -f origin <branch_name>
```
### Delete branch
#### Local
```
git branch <branch_name> -d
```
#### Remote
```
git push origin -d <branch_name>
```
### Branch list
```
git branch -l
```
### Commit history
```
git log
git log --pretty=oneline (other way)
```
