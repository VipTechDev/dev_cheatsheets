```// 👉 Getting Started with Git and GitHub
// Module 2 Cheat Sheet: Git Commands and Managing GitHub Projects

// 👉 Staging & Committing
git add sample.md                  // Stage a specific file
git add .                          // Stage all changes
git commit -m "Your message"       // Commit staged changes

// 👉 Branching & Switching
git branch <new-branch>            // Create a new branch
git checkout <existing-branch>     // Switch to a branch
git checkout main                  // Switch to main branch

// 👉 Cloning & Initializing
git clone <repository-url>         // Clone a remote repo
git init <directory>               // Initialize a new local repo

// 👉 Configuration
git config --global user.email "your.email@example.com"
git config --global user.name "Your Name"

// 👉 Remote Management
git remote add origin <URL>        // Add remote origin
git remote add upstream <URL>      // Add upstream remote
git remote rename origin new-origin
git remote -v                      // View remotes

// 👉 Fetching & Pulling
git fetch <remote> <branch>        // Fetch changes
git fetch upstream master:upstream-master
git pull origin main               // Pull and merge from origin
git pull upstream main             // Pull from upstream
git pull origin main --allow-unrelated-histories // Merge separate histories

// 👉 Pushing
git push origin your_branch_name   // Push changes
git push -u origin main            // Push and set upstream

// 👉 Merging & Reverting
git merge feature_branch           // Merge branch into current
git merge upstream/master          // Merge upstream changes
git revert HEAD                    // Undo last commit safely
git reset HEAD~1                   // Undo last commit (unstage)

// 👉 Status & Logs
git status                         // Show working directory state
git log -p filename                // Show commit history with diffs
git diff example.txt               // Compare changes

// 👉 Advanced & Utilities
git am <patchfile.patch>           // Apply emailed patch
git format-patch -n <num>          // Prepare patch series
git request-pull origin/main your-branch
git rerere                         // Reuse resolved merge conflicts
git daemon --reuseaddr --verbose   // Allow anonymous repo access
git http-backend                   // Git-over-HTTP server
git instaweb -p 8080               // Web front-end for repo
git send-email --to=recipient@example.com path/to/patchfile.patch
git shell                          // Restricted shell for Git users
git --version                      // Show Git version
