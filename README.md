# Create a new repository on the command line
```
git init
git add <path|file_name>
git commit -m "message"
git branch -M <branch_name>
git remote add origin <repository>
git push -u origin <branch_name>
```
# Push an existing repository from the command line
```
git remote add origin <repository>
git branch -M <branch_name>
git push -u origin <branch_name>
```
# Clone repository with branch
```
git clone -b <branch_name> <repository>
```
# Update branch
```
git pull origin <branch_name>
```
# Commit and push
```
git add <path|file_name>
git commit -m "message"
git push origin <branch_name>
```
# Create new branch from current branch
```
git checkout -b <branch_name>
```
# Rename branch
```
git branch -m <branch> <new_branch_name>
```
