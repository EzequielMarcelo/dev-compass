# Most Used Git Commands

My git command quick reference guide organized by category.

## 1. Initial Configuration
```sh
# Set global username and email
git config --global user.name "Your Name"
git config --global user.email "youremail@example.com"
```
```sh
# Set username and email only for this repository
git config user.name "Your Name"
git config user.email "youremail@example.com"
```
```sh
# Check current configuration
git config --list
```

## 2. Initialize and Clone Repositories
```sh
# Initialize a new Git repository (with working directory)
git init
```
```sh
# Initialize a new bare Git repository (without working directory)
# Typically used on remote servers or as a shared repository
git init --bare
```
```sh
# Clone an existing repository
git clone https://github.com/user/repository.git
```

## 3. Add and Commit Changes
```sh
# Add a specific file
git add file.txt   
```
```sh
# Add all modified files
git add .    
```
```sh    
# Create a commit
git commit -m "Commit message"
```
```sh
# Rename the last commit message
git commit --amend -m "New commit message"
```
```sh
# Save without changing the last commit message
git commit --amend --no-edit
```

## 4. Push and Pull Changes
```sh
# Push changes to the remote repository
git push origin main
```
```sh
git fetch
```
```sh
# Pull and merge changes from the remote repository
git pull origin main
```

## 5. Working with Branches
```sh
# Create a new branch
git branch new-branch
```
```sh
# Switch to another branch
git checkout new-branch
```
```sh
# Create and switch to a new branch
git checkout -b new-branch
```
```sh
# List all branches
git branch
```
```sh
# Merge another branch into the current one
git merge other-branch
```

## 6. Undoing Changes
```sh
# Discard changes before staging
git checkout -- file.txt
```
```sh
# Unstage a file
git reset file.txt
```
```sh
# Undo the last commit but keep the changes
git reset --soft 
```
```sh
# Undo the last commit and discard changes
git reset --hard 
```

## 8. Stop Tracking Files
```sh
# Stop tracking a specific file
git rm -r --cached filename
```
```sh
# Stop tracking all files (keep them locally)
git rm -r --cached .
```

## 9. Remote Repositories
```sh
# Add a remote repository
git remote add origin https://github.com/user/repository.git
```
```sh
# Show configured remote repositories
git remote -v
```
```sh
# Change the URL of the remote repository
git remote set-url origin <NEW_GIT_URL_HERE>
```

## 10. Tags
```sh
# Create a new tag
git tag -a v1.0 -m "Version 1.0"
```
```sh
# List all tags
git tag
```
```sh
# Push all tags to the remote repository
git push origin --tags
```
```sh
# Delete a local tag
git tag -d tag-name
```
```sh
# Delete a remote tag
git push -d origin 1.0.0
```

## 11. Help
```sh
# Use git help <command> to view detailed documentation for any command:
git help commit
```