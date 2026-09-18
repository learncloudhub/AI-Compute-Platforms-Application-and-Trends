# Git Useful Commands Cheat Sheet

A quick-reference cheat sheet of essential Git commands with clear explanations and real-world examples.

---

## 🚀 Setup & Initialization

### `git init`
* **Usage:** Run inside an empty project folder to start tracking it with Git.
* **Example:** `git init`

### `git clone <url>`
* **Usage:** Downloads an entire existing repository from GitHub to your computer.
* **Example:** `git clone https://github.com/user/repo.git`

### `git config --global user.name "<name>"`
* **Usage:** Sets the author name for your project commits globally.
* **Example:** `git config --global user.name "John Doe"`

### `git config --global user.email "<email>"`
* **Usage:** Sets the author email for your project commits globally.
* **Example:** `git config --global user.email "john@example.com"`

---

## 📝 Staging & Committing Changes

### `git status`
* **Usage:** Shows modified files and checks what is ready to be committed.
* **Example:** `git status`

### `git add <file>`
* **Usage:** Stages a single specific file for the next commit snapshot.
* **Example:** `git add index.html`

### `git add .`
* **Usage:** Stages all new, modified, and deleted files in the directory at once.
* **Example:** `git add .`

### `git commit -m "<message>"`
* **Usage:** Saves your staged changes permanently to history with a short description.
* **Example:** `git commit -m "Fix login button layout"`

### `git commit -am "<message>"`
* **Usage:** Shortcuts the process by staging tracked files and committing them in one step.
* **Example:** `git commit -am "Update readme text"`

---

## 🌿 Branching & Merging

### `git branch`
* **Usage:** Lists all existing branches in your local repository.
* **Example:** `git branch`

### `git switch <branch>`
* **Usage:** Moves your working directory over to a different branch.
* **Example:** `git switch feature-login`

### `git switch -c <branch>`
* **Usage:** Creates a completely new branch and immediately switches you onto it.
* **Example:** `git switch -c feature-payment`

### `git merge <branch>`
* **Usage:** Integrates changes from a specified branch into your currently active branch.
* **Example:** `git merge feature-login`

### `git branch -d <branch>`
* **Usage:** Deletes a local branch that you have already safely merged.
* **Example:** `git branch -d feature-login`

---

## 🌐 Remote Syncing

### `git remote add origin <url>`
* **Usage:** Links your local repository to a remote server target like GitHub.
* **Example:** `git remote add origin https://github.com/user/repo.git`

### `git push origin <branch>`
* **Usage:** Uploads your local branch commits up to the remote repository.
* **Example:** `git push origin main`

### `git pull`
* **Usage:** Fetches updates from the remote server and merges them into your current branch.
* **Example:** `git pull`

---

## 🔍 Viewing History & Differences

### `git log --oneline`
* **Usage:** Displays a clean, condensed history list of your past commits.
* **Example:** `git log --oneline`

### `git diff`
* **Usage:** Shows the exact line-by-line differences in your unstaged files.
* **Example:** `git diff`

### `git diff --staged`
* **Usage:** Shows line-by-line changes made to files that are staged but not committed.
* **Example:** `git diff --staged`

### `git blame <file>`
* **Usage:** Shows who wrote or edited each specific line of code inside a file.
* **Example:** `git blame server.js`

---

## 🧹 Cleaning Up & Fixing Mistakes

### `git restore <file>`
* **Usage:** Discards uncommitted modifications in a file, reverting it to the last commit.
* **Example:** `git restore app.js`

### `git reset <file>`
* **Usage:** Unstages a file from the staging area but leaves its actual code changes intact.
* **Example:** `git reset style.css`

### `git reset --hard`
* **Usage:** Wipes out all local changes and completely resets your workspace to the last commit.
* **Example:** `git reset --hard`

### `git commit --amend -m "<message>"`
* **Usage:** Rewrites the message or adds missed files to your very last unpushed commit.
* **Example:** `git commit --amend -m "Corrected typo in header"`

### `git stash`
* **Usage:** Temporarily shelves your current dirty work so you can switch tasks cleanly.
* **Example:** `git stash`

### `git stash pop`
* **Usage:** Brings back the hidden changes you previously put away on your stash shelf.
* **Example:** `git stash pop`
