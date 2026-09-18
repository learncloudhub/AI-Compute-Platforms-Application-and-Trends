# The Ultimate Git Command Reference Manual

A comprehensive, organized guide to Git commands, concepts, plumbing, and advanced workflows.

---

## 🚀 1. Setup & Configuration
Configure Git settings, user identity, global preferences, and default behaviors.

*   **`git config --global user.name "<name>"`**
    *   **Usage:** Sets the author name linked to your commit history across all local repositories.
    *   **Example:** `git config --global user.name "Alice Dev"`
*   **`git config --global user.email "<email>"`**
    *   **Usage:** Sets the email address linked to your commit history. Must match your remote hosting profile.
    *   **Example:** `git config --global user.email "alice@example.com"`
*   **`git config --global core.editor "<editor>"`**
    *   **Usage:** Configures the default text editor for commit messages and merges.
    *   **Example:** `git config --global core.editor "code --wait"`
*   **`git config --global alias.<short> <command>`**
    *   **Usage:** Creates custom shortcuts (aliases) for frequently used commands.
    *   **Example:** `git config --global alias.co checkout`
*   **`git config --list`**
    *   **Usage:** Displays all active configuration settings from system, global, and local files.
    *   **Example:** `git config --list`

---

## 📂 2. Starting a Repository
Create local tracking systems or clone remote workbases.

*   **`git init`**
    *   **Usage:** Initializes an empty, local Git repository in the current working directory.
    *   **Example:** `git init`
*   **`git clone <url>`**
    *   **Usage:** Downloads an existing repository, its branch trees, and full historical log to your machine.
    *   **Example:** `git clone https://github.com/user/project.git`
*   **`git clone <url> <directory>`**
    *   **Usage:** Clones a remote repository directly into a custom-named target directory.
    *   **Example:** `git clone https://github.com/user/project.git my-app`

---

## 📝 3. Staging & Basic Snapshotting
Track local file changes, prepare modifications, and build file histories.

*   **`git status`**
    *   **Usage:** Checks state of files (tracked, untracked, staged, unstaged, modified).
    *   **Example:** `git status`
*   **`git status -s`**
    *   **Usage:** Displays a short, compact view of modifications.
    *   **Example:** `git status -s`
*   **`git add <file>`**
    *   **Usage:** Moves a single file's modifications into the staging area.
    *   **Example:** `git add index.js`
*   **`git add .`**
    *   **Usage:** Stages all changes, new creations, and deletions across the entire directory structure.
    *   **Example:** `git add .`
*   **`git add -p`**
    *   **Usage:** Interactive staging. Lets you review changes piece-by-piece ("hunks") before committing.
    *   **Example:** `git add -p`
*   **`git commit -m "<message>"`**
    *   **Usage:** Saves the staged snapshot permanently into your local commit timeline.
    *   **Example:** `git commit -m "feat: Add core auth logic"`
*   **`git commit -am "<message>"`**
    *   **Usage:** Bypasses staging for modified files, staging and committing them in a single stroke.
    *   **Example:** `git commit -am "fix: Resolve page crash on refresh"`

---

## 🌿 4. Branching & Context Switching
Navigate multiple feature paths, manage isolation contexts, and view branch lists.

*   **`git branch`**
    *   **Usage:** Lists all active local branches in your current repository workspace.
    *   **Example:** `git branch`
*   **`git branch -a`**
    *   **Usage:** Shows both your local tracking branches and all cached remote tracking branches.
    *   **Example:** `git branch -a`
*   **`git branch <branch-name>`**
    *   **Usage:** Spawns a new independent pointer at your current commit milestone without switching contexts.
    *   **Example:** `git branch feature-ui`
*   **`git switch <branch-name>`**
    *   **Usage:** Switches your working context to an existing target branch.
    *   **Example:** `git switch main`
*   **`git switch -c <branch-name>`**
    *   **Usage:** Spawns a new branch and instantly pivots your active directory context over to it.
    *   **Example:** `git switch -c hotfix-api`
*   **`git checkout <branch-name>`**
    *   **Usage:** Older command to switch branches (alternative to `git switch`).
    *   **Example:** `git checkout main`
*   **`git checkout -b <branch-name>`**
    *   **Usage:** Older shortcut command to create a new branch and check it out.
    *   **Example:** `git checkout -b feature-payment`
*   **`git branch -d <branch-name>`**
    *   **Usage:** Deletes a local branch if it has already been safely merged to your parent branch.
    *   **Example:** `git branch -d feature-ui`
*   **`git branch -D <branch-name>`**
    *   **Usage:** Forcefully deletes a branch, throwing away any unmerged changes permanently.
    *   **Example:** `git branch -D incomplete-work`
*   **`git branch -m <new-name>`**
    *   **Usage:** Renames your currently active local branch.
    *   **Example:** `git branch -m main-branch`

---

## 🔀 5. Merging, Rebasing & Integrating
Combine divergent branch histories, pick commits, and resolve linear flows.

*   **`git merge <branch>`**
    *   **Usage:** Joins the history of the target branch directly into your active branch.
    *   **Example:** `git merge feature-ui`
*   **`git merge --abort`**
    *   **Usage:** Stops a conflicted merge and resets the workspace back to its pre-merge state.
    *   **Example:** `git merge --abort`
*   **`git rebase <branch>`**
    *   **Usage:** Rewrites history by moving the base of your active branch onto the tip of the target branch.
    *   **Example:** `git rebase main`
*   **`git rebase -i <commit-hash>`**
    *   **Usage:** Launches interactive rebase to squash, edit, reword, or drop past commits.
    *   **Example:** `git rebase -i HEAD~3`
*   **`git rebase --continue`**
    *   **Usage:** Resumes a rebase flow after you have resolved manual code merge conflicts.
    *   **Example:** `git rebase --continue`
*   **`git cherry-pick <commit-hash>`**
    *   **Usage:** Copies a specific individual commit from another branch and appends it to your current active branch.
    *   **Example:** `git cherry-pick a1b2c3d`

---

## 🌐 6. Remote Synchronizations
Link your local repository to external platforms (GitHub, GitLab) and share updates.

*   **`git remote -v`**
    *   **Usage:** Lists configured remote connections along with their underlying tracking URLs.
    *   **Example:** `git remote -v`
*   **`git remote add origin <url>`**
    *   **Usage:** Maps an external server path to the local reference named 'origin'.
    *   **Example:** `git remote add origin https://github.com/user/project.git`
*   **`git remote remove <name>`**
    *   **Usage:** Drops an external server path association from your configuration tracker.
    *   **Example:** `git remote remove origin`
*   **`git fetch`**
    *   **Usage:** Downloads all metadata, histories, and files from remotes without modifying your working branch.
    *   **Example:** `git fetch`
*   **`git pull`**
    *   **Usage:** Fetches updates from the remote and immediately merges them into your current local branch.
    *   **Example:** `git pull`
*   **`git push origin <branch>`**
    *   **Usage:** Uploads local commits to the remote version of the specified branch.
    *   **Example:** `git push origin main`
*   **`git push -u origin <branch>`**
    *   **Usage:** Pushes the branch and sets it as the default tracking branch for future pushes and pulls.
    *   **Example:** `git push -u origin feature-auth`
*   **`git push origin --delete <branch>`**
    *   **Usage:** Removes a branch completely from the remote repository server.
    *   **Example:** `git push origin --delete feature-auth`

---

## 🔍 7. Inspection, History & Verification
Audit commits, find bugs, trace file changes, and read project histories.

*   **`git log`**
    *   **Usage:** Displays the entire structural timeline of your branch commits in descending order.
    *   **Example:** `git log`
*   **`git log --oneline`**
    *   **Usage:** Compresses the commit history log down to single-line summaries with short hashes.
    *   **Example:** `git log --oneline`
*   **`git log --graph --oneline --all`**
    *   **Usage:** Renders a visual ASCII branch tree graph of all local and remote branches.
    *   **Example:** `git log --graph --oneline --all`
*   **`git log -n <number>`**
    *   **Usage:** Caps log output to a specific quantity of recent commits.
    *   **Example:** `git log -n 5`
*   **`git log --author="<name>"`**
    *   **Usage:** Filters out commit histories to show entries from a specific contributor.
    *   **Example:** `git log --author="John"`
*   **`git diff`**
    *   **Usage:** Compares your unstaged local working directory adjustments against the staging index.
    *   **Example:** `git diff`
*   **`git diff --staged`**
    *   **Usage:** Evaluates all staged alterations ready for commit against the current HEAD state.
    *   **Example:** `git diff --staged`
*   **`git diff <branch-1> <branch-2>`**
    *   **Usage:** Displays full differences across lines between two independent tracking branches.
    *   **Example:** `git diff main feature-dev`
*   **`git show <commit-hash>`**
    *   **Usage:** Displays metadata details and line-by-line file changes of a target commit.
    *   **Example:** `git show f5e4d3c`
*   **`git blame <file>`**
    *   **Usage:** Annotates each line of a target file with details of the person and commit that wrote it.
    *   **Example:** `git blame components/Auth.js`
*   **`git reflog`**
    *   **Usage:** Keeps a strict internal local index log of every point mutation, check-out, and reset. Essential for disaster recovery.
    *   **Example:** `git reflog`

---

## 🧹 8. Undoing Changes & Fixing Mistakes
Discard errors, roll back commit states, unstage mistakes, and wipe code states.

*   **`git restore <file>`**
    *   **Usage:** Cleans out unstaged modifications from a file, matching it back to the index head.
    *   **Example:** `git restore config.json`
*   **`git restore --staged <file>`**
    *   **Usage:** Unstages a file, returning it back to an unstaged but modified state.
    *   **Example:** `git restore --staged config.json`
*   **`git reset <file>`**
    *   **Usage:** Legacy method to remove a file out of the staging index while preserving local modifications.
    *   **Example:** `git reset styles.css`
*   **`git reset --soft <commit-hash>`**
    *   **Usage:** Rolls the timeline pointer backward to a past commit, keeping all changes staged in your current working index.
    *   **Example:** `git reset --soft HEAD~1`
*   **`git reset --mixed <commit-hash>`**
    *   **Usage:** Default reset option. Rewinds your commit timeline, unstaging your files while retaining work tree code adjustments.
    *   **Example:** `git reset HEAD~1`
*   **`git reset --hard <commit-hash>`**
    *   **Usage:** **Warning:** Destructive reset. Rewinds your commit timeline and wipes out all local working directory adjustments and staged files.
    *   **Example:** `git reset --hard HEAD~1`
*   **`git commit --amend -m "<new-message>"`**
    *   **Usage:** Modifies the message or file composition of your most recent unpushed commit.
    *   **Example:** `git commit --amend -m "chore: Update config properly"`
*   **`git revert <commit-hash>`**
    *   **Usage:** Creates a brand-new, safe commit that applies the exact inverse changes of a targeted past error commit.
    *   **Example:** `git revert b2c3d4e`
*   **`git clean -df`**
    *   **Usage:** Forcefully sweeps out all untracked untracked file entries and folders from the local workspace.
    *   **Example:** `git clean -df`

---

## 📦 9. Stashing & Shelving
Temporarily shelf current working states to jump context tasks without committing.

*   **`git stash`**
    *   **Usage:** Saves active uncommitted changes (both staged and unstaged) to a temporary shelf.
    *   **Example:** `git stash`
*   **`git stash save "<message>"`**
    *   **Usage:** Shelves active uncommitted changes with a custom descriptive tag message.
    *   **Example:** `git stash save "Work on navbar layout"`
*   **`git stash list`**
    *   **Usage:** Shows all currently shelved snapshots stacked up in memory storage.
    *   **Example:** `git stash list`
*   **`git stash pop`**
    *   **Usage:** Applies the top (most recent) item on your stash stack back to your workspace and removes it from the stash.
    *   **Example:** `git stash pop`
*   **`git stash apply`**
    *   **Usage:** Re-applies the top item on the stash stack without deleting it from your stash records.
    *   **Example:** `git stash apply`
*   **`git stash drop`**
    *   **Usage:** Permanently discards the top stashed item from your stack without applying it.
    *   **Example:** `git stash drop`
*   **`git stash clear`**
    *   **Usage:** Wipes out every single item inside your active stash stack storage.
    *   **Example:** `git stash clear`

---

## 🏷️ 10. Tagging & Releases
Mark major release points and milestone commits with semantic labels.

*   **`git tag`**
    *   **Usage:** Lists all tags defined within the repository workspace.
    *   **Example:** `git tag`
*   **`git tag <tag-name>`**
    *   **Usage:** Attaches a lightweight tag pointer onto your current active commit milestone.
    *   **Example:** `git tag v1.0.0-light`
*   **`git tag -a <tag-name> -m "<message>"`**
    *   **Usage:** Generates an annotated release tag requiring its own message, metadata, and history validation.
    *   **Example:** `git tag -a v1.0.0 -m "Production release version 1.0.0"`
*   **`git push origin <tag-name>`**
    *   **Usage:** Explicitly uploads a specific tag milestone onto your remote server asset list.
    *   **Example:** `git push origin v1.0.0`
*   **`git push origin --tags`**
    *   **Usage:** Pushes all local tags to the remote repository server at once.
    *   **Example:** `git push origin --tags`
*   **`git tag -d <tag-name>`**
    *   **Usage:** Deletes a specific tag from your local repository configuration.
    *   **Example:** `git tag -d v1.0.0`

---

## 🛠️ 11. Advanced Plumbing & Maintenance
Debug problems, optimize local setups, and verify integrity.

*   **`git bisect start`**
    *   **Usage:** Initiates a binary search debugging sequence to track down which historical commit introduced a code regression bug.
    *   **Example:** `git bisect start`
*   **`git gc`**
    *   **Usage:** Runs garbage collection to compress your file history tree and clean up detached file elements.
    *   **Example:** `git gc`
*   **`git fsck`**
    *   **Usage:** File System Check. Verifies structural integrity of the database, locating broken pointer links or orphan objects.
    *   **Example:** `git fsck`
*   **`git archive --format=zip HEAD > project.zip`**
    *   **Usage:** Packages the current active branch source code files into a clean distribution zip folder, skipping Git internal folders.
    *   **Example:** `git archive --format=zip HEAD > project.zip`
