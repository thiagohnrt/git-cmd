# GIT Command
- [Getting Started - Setup](#git-setup)
  - [Install Git](#install-git)
  - [Identify](#identify)
  - [SSH keys](#ssh-keys)
  - [File .gitconfig](#file-gitconfig)
- [Repository](#repository)
  - [Create a new repository](#create-a-new-repository)
  - [Push an existing repository](#push-an-existing-repository)
  - [Clone repository with branch](#clone-repository-with-branch)
- [Branch](#branch)
  - [Update branch](#update-branch)
  - [Commit and push](#commit-and-push)
  - [Create new branch from current branch](#create-new-branch-from-current-branch)
  - [Rename local branch](#rename-local-branch)
  - [Merge branch](#merge-branch)
  - [Cherry pick commit](#cherry-pick-commit)
  - [Reset pushed commit](#reset-pushed-commit)
  - [Revert pull request](#revert-pull-request)
  - [Delete branch](#delete-branch)
    - [Local](#local)
    - [Remote](#remote)
    - [Delete all local branches except the current one](#delete-all-local-branches-except-the-current-one)
  - [Branch list](#branch-list)
  - [Commit History](#commit-history)
  - [Change Commit Message](#change-commit-message)
  - [Undo the last commit, keeping the changes](#undo-the-last-commit-keeping-the-changes)
- [Configuration](#config)
  - [List configuration](#list-configuration)
  - [Filename too long](#filename-too-long)


# Git Setup

### Install Git

<a href="https://git-scm.com/downloads">Download 🡥</a><br/>
<a href="https://git-scm.com/book/en/v2/Getting-Started-Installing-Git">Getting Started Installing Git 🡥</a>

### Identify
```
git config --global user.name "Thiago Honorato"
git config --global user.email thiagohonorato@example.com
```

### SSH keys

#### Checking for existing SSH keys
```
ls -al ~/.ssh
```

#### Generating a new SSH key
```
ssh-keygen -t ed25519 -C "thiagohonorato@example.com"
```

> Note: If you are using a legacy system that doesn't support the Ed25519 algorithm, use:
> ```
> $ ssh-keygen -t rsa -b 4096 -C "thiagohonorato@example.com"
> ```

### File .gitconfig
```
git config --global core.editor code
git config --global --edit
```
![VS Code .gitconfig](/img/vscode_gitconfig.png "VS Code .gitconfig file")

<a href="https://gist.github.com/thiagohnrt/264c1760666a92ba85b804b4172f650b" target="_blank">Gist .gitconfig 🡥</a>

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
### Rename local branch
```
git branch -m <old_branch> <new_branch>
git branch -M "<new_branch>" (other way)
```
### Merge branch
```
git checkout <branch_main>
git merge <branch_with_feature>
```
### Cherry pick commit
Apply change from one branch to another.
```
git switch <branch_with_change>
git log
// copy commit id
git switch <branch_destiny>
git cherry-pick <commit_id>
git push origin <branch_destiny>
```
### Reset pushed commit
```
git reset --hard <commit_id>
git push -f origin <branch_name>
```
### Revert pull request
```
git revert -m 1 <merge_id>
git push origin <branch_name>
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
#### Delete all local branches except the current one
```
git branch | grep -v "^\*" | xargs git branch -D
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
### Change Commit Message
Run the following command to amend (change) the message of the latest commit:
```
git commit --amend -m "New commit message."
```
### Undo the last commit, keeping the changes
```
git reset --soft HEAD~1
```
# Config
### List configuration
List all variables set in config file, along with their values.
```
git config --list
```
To show the actual path where this setting is applied
```
git config --list --show-origin
```
### Filename too long
```
git config --system core.longpaths true
```
