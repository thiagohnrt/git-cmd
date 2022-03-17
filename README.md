# Create a new repository
#### Create an empty Git repository
`git init`
#### Add file contents to the index
`git add <path|file_name>`
#### Record changes to the repository
`git commit -m "message"`
#### Renaming the branch
`git branch -M <branch_name>`
```
git remote add origin <repository>
git push -u origin <branch_name>
```
# Push an existing repository
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
git branch -m <old_branch> <new_branch>
git branch -M "<new_branch>" (other way)

git push -u origin <new_branch>
```
# Merge branch
```
git checkout <branch_main>
git merge <branch_with_feature>
```
# Reset pushed commit
```
git reset --hard <commit_id>
git push -f origin <branch_name>
```
# Delete branch
## Local
```
git branch <branch_name> -d
```
## Remote
```
git push origin -d <branch_name>
```
# Branch list
```
git branch -l
```
# Commit History
```
git log
git log --pretty=oneline (other way)
```
