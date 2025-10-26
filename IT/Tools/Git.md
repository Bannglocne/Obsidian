# Configuration
Levels:
	- System (all users): `git config --system`
	- Global (current user): `git config --global`
	- Local (current repo): `git config --local`
```shell
git config --global user.name "Your Name"
git config --global user.email "you@example.com"

git config --list
git config user.name
git config --global --unset user.name
```

Default Branch Name (`main`)
```bash
git config --global init.defaultBranch main
```

# Git Command
## Help
```bash
git help <command> # See Help for a Specific Command
git <command> -h # See a Quick Summary
git help --all # List All Git Commands
git help -g # List Guides and Concepts
```

## Get Started
```bash
mkdir myproject
cd myproject
git init
ls
git status
```

- **Staging**: Tell Git which file we want to include in our next commit
```bash
git add index.html
git add -all
git add -A
git status

git restore --staged index.html
```

- **Commit**: Save point in your project.
```bash
git commit -m "message"
git commit -a - m "message"

git commit --allow-empty -m "Start project" # Empty commit
git commit --no-edit # Use previous commit message
git commit --amend --no-edit # Quickly add staged changes to last commit keep message
```

## Tag
Mark important point in project history
```bash
git tag -a <tagname> -m "message" 
```

```bash
git tag <tagname> <commit-hash> # For specific commit
git tag # List tag
git show <tagname> # Tag details

git push origin <tagname> # Push to remote
git push --tags # Push all

git tag -d <tagname> # Delete tag
git push origin --delete tag <tagname> # Delete a tag from the remote repository

git tag -f <tagname> <new-commit-hash> # Update or Replace tag
git push --force origin <tagname>
```

## Stash
Save uncommitted changes and return to a clean working directory

- Stash all tracked files (To stash untracked files: `git stash -u` or `--include-untracked`)
```bash
git stash push -m "message"
git stash list
git stash show
```

```bash
git stash apply # Restore most recent stashed changes

git stash apply stash@{n} # Apply a Specific Stash
git stash pop # Apply the latest stash and remove it from the stack

git stash drop stash@{n} # Delete a specific stash when we no longer need it
git stash clear # Clear all stashes

git stash branch new-feature stash@{n} # Create a new branch and apply a stash to it:
```

## History
```bash
git log # Show full commit history
git log --oneline # Show a summary of commits
git log --stat # Show Files Changed Per Commit
git log --graph # Show a Branch Graph

git log --author="ziecnhazuize" # Show Commits by Author
git log --since="2 weeks ago" # Show Recent Commits

git show <commit> # Show details of a specific commit
```

```bash
git diff # See what different between working directory and the last commit
git diff --staged # See what different between staged files and the last commit
git diff <commit1> <commit2> # Compare Two Commits
```

## Branch
A separate workspace where you can make changes and try new ideas without affecting the main project.
```shell
git branch <branch-name> # Creating a new branch
git branch # Listing all branches
git checkout <branch-name> # Switching between branches
git branch -d <branch-name> # Deleteing a branch
```

```shell
git merge <branch-name> # Merge a branch into your current branch
git merge --no-ff <branch-name> # Always create a merge commit
git merge --squash <branch-name> # Combine changes into a single commit
git merge --abort # Abort a merge in progress
```

# GitHub
## Security SSH
```shell
eval $(ssh-agent -s) # First-Time SSH Key Setup
ssh-keygen -t rsa -b 4096 -C "your@email.com" # Generating an SSH Key Pair
ssh-add ~/.ssh/id_rsa # Adding Your Key to the SSH Agent
clip < ~/.ssh/id_rsa.pub # Copying Your Public Key
```

## Pull & Push
```shell
git fetch
git status
```