# 🧠 Git Cheat Sheet

## 📦 Setup
```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
git config --list

git init                      # Initialize repo
git clone <repo_url>          # Clone repo

git status                    # Check status
git add <file>                # Stage file
git add .                     # Stage all changes
git commit -m "message"       # Commit changes

git log                       # Full history
git log --oneline             # Compact history
git diff                      # Show changes

git branch                    # List branches
git branch <name>             # Create branch
git checkout <branch>         # Switch branch
git checkout -b <branch>      # Create + switch
git merge <branch>            # Merge into current


git remote -v                 # View remotes
git remote add origin <url>   # Add remote
git push -u origin main       # Push first time
git push                      # Push changes
git pull                      # Fetch + merge
git fetch                     # Fetch only

git restore <file>            # Discard changes
git reset <file>              # Unstage file
git reset --hard              # Reset everything (⚠️ destructive)
git revert <commit>           # Undo commit safely


git clean -fd                 # Remove untracked files


git tag                       # List tags
git tag <tag_name>            # Create tag
git push origin <tag_name>    # Push tag


git stash                     # Save changes
git stash pop                 # Apply + remove stash
git stash list                # List stashes


git checkout -- .             # Discard all local changes
git pull --rebase             # Cleaner history
git log --graph --oneline --all  # Visual history

# Git Note
To put your local project on git:
- create a repository
- follow the instructions on github
- create a .gitignore file before adding or commiting.
