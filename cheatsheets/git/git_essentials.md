# 🐙 Essential Git Commands

## 🔄 Basic Workflow (Saving your work)
\`\`\`bash
git status            # Check the status of modified files
git add .             # Stage ALL modifications
git commit -m "msg"   # Create a save with a clear descriptive message
git push origin main  # Send changes to GitHub (or master)
\`\`\`

## 🔀 Branches (Working on a new feature)
\`\`\`bash
git branch            # List all local branches
git checkout -b feature-darkmode # Create AND switch to the new branch
git checkout main     # Switch back to the main branch
\`\`\`

## ⏪ Oops! (Fixing mistakes)
\`\`\`bash
git restore file.js          # Discard local changes in a file (before git add)
## ⏩ Stashing & Remotes (Advanced)
\`\`\`bash
git stash                    # Temporarily save uncommitted changes
git stash pop                 # Restore stashed changes
git remote -v                 # List remote repositories
git fetch                     # Download objects and refs from another repository
git pull                      # Fetch and merge changes from remote
git push                      # Push local changes to remote
\`\`\`
