## 🧠 Git & GitHub Project Cheat Sheet  
Staging, Branching, Cloning, Configuration, Remotes, Pulling, Pushing, Merging, Logs, and Utilities

---

### 📥 Staging & Committing  
```bash
git add sample.md # Stage a specific file  
git add . # Stage all changes  
git commit -m "Your message" # Commit staged changes  
```  
✅ Stage changes and commit with a clear message.

---

### 🌿 Branching & Switching  
```bash
git branch <new-branch> # Create a new branch  
git checkout <existing-branch> # Switch to a branch  
git checkout main # Switch to main branch  
```  
✅ Use branches to isolate features and switch contexts.

---

### 📦 Cloning & Initializing  
```bash
git clone <repository-url> # Clone a remote repo  
git init <directory> # Initialize a new local repo  
```  
✅ Start fresh or sync with an existing project.

---

### ⚙️ Configuration  
```bash
git config --global user.email "your.email@example.com"  
git config --global user.name "Your Name"  
```  
✅ Set your identity for commits.

---

### 🌐 Remote Management  
```bash
git remote add origin <URL> # Add remote origin  
git remote add upstream <URL> # Add upstream remote  
git remote rename origin new-origin  
git remote -v # View remotes  
```  
✅ Connect and manage remote repositories.

---

### 🔄 Fetching & Pulling  
```bash
git fetch <remote> <branch> # Fetch changes  
git fetch upstream master:upstream-master  
git pull origin main # Pull and merge from origin  
git pull upstream main # Pull from upstream  
git pull origin main --allow-unrelated-histories  
```  
✅ Sync your local repo with remote updates.

---

### 🚀 Pushing  
```bash
git push origin your_branch_name # Push changes  
git push -u origin main # Push and set upstream  
```  
✅ Share your work with the remote repo.

---

### 🔀 Merging & Reverting  
```bash
git merge feature_branch # Merge branch into current  
git merge upstream/master # Merge upstream changes  
git revert HEAD # Undo last commit safely  
git reset HEAD~1 # Undo last commit (unstage)  
```  
✅ Integrate changes or roll back safely.

---

### 📋 Status & Logs  
```bash
git status # Show working directory state  
git log -p filename # Show commit history with diffs  
git diff example.txt # Compare changes  
```  
✅ Inspect your repo’s current state and history.

---

### 🛠️ Advanced & Utilities  
```bash
git am <patchfile.patch> # Apply emailed patch  
git format-patch -n <num> # Prepare patch series  
git request-pull origin/main your-branch  
git rerere # Reuse resolved merge conflicts  
git daemon --reuseaddr --verbose # Allow anonymous repo access  
git http-backend # Git-over-HTTP server  
git instaweb -p 8080 # Web front-end for repo  
git send-email --to=recipient@example.com path/to/patchfile.patch  
git shell # Restricted shell for Git users  
git --version # Show Git version  
```  
✅ Explore advanced workflows and Git utilities.

