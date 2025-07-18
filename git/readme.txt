# ------------------------------
# 1. Git Setup & Configuration
# ------------------------------
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
git config --list

# ------------------------------
# 2. Repository Initialization
# ------------------------------
git init
git clone <repo-url>
git clone https://github.com/user/repo.git

# ------------------------------
# 3. Basic Workflow
# ------------------------------
git status
git add <file>
git add .                           # Add all changes
git commit -m "Your commit message"
git push origin main                # Push to main branch
git pull origin main                # Pull from remote
git fetch                           # Download changes but don’t merge

# ------------------------------
# 4. Branching
# ------------------------------
git branch                          # List branches
git branch <branch-name>            # Create new branch
git checkout <branch-name>          # Switch to branch
git checkout -b <branch-name>       # Create & switch
git merge <branch-name>             # Merge into current branch
git branch -d <branch-name>         # Delete branch

# ------------------------------
# 5. Remote Repositories
# ------------------------------
git remote -v
git remote add origin <url>
git remote remove origin
git push -u origin main             # Set upstream tracking branch

# ------------------------------
# 6. Logs & History
# ------------------------------
git log
git log --oneline
git show <commit-id>
git diff                            # Unstaged changes
git diff --staged                   # Staged changes

# ------------------------------
# 7. Stashing
# ------------------------------
git stash                           # Save changes
git stash apply                     # Reapply latest stash
git stash list                      # Show stashed changes
git stash drop                      # Remove latest stash

# ------------------------------
# 8. Tagging
# ------------------------------
git tag                             # List tags
git tag <tag-name>                  # Create tag
git tag -a <tag-name> -m "message" # Annotated tag
git push origin <tag-name>          # Push tag

# ------------------------------
# 9. Undo & Reset
# ------------------------------
git reset --soft HEAD~1             # Undo commit, keep changes staged
git reset --mixed HEAD~1            # Undo commit, unstage changes
git reset --hard HEAD~1             # Undo commit, delete changes
git checkout -- <file>              # Discard changes in file

# ------------------------------
# 10. GitHub Authentication (via HTTPS)
# ------------------------------
git config --global credential.helper store
# First push will ask for token → saved permanently

# ------------------------------
# 11. GitHub CLI (gh)
# ------------------------------
gh auth login
gh repo clone <user>/<repo>
gh repo create
gh pr create
gh issue list
gh auth logout

