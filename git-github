# Git & GitHub Basic Commands

Git is a powerful version control system used to track changes and collaborate on projects efficiently.  
This document provides a comprehensive list of essential Git & GitHub commands for development and DevOps workflows.

---

## Initialization & Configuration
Basic commands to set up Git on your system, configure identity, and start or clone repositories.

| Command | Description |
|--------|-------------|
| `git init` | Initialize a new Git repository |
| `git clone <repo-url>` | Clone a repository |
| `git config --global user.name "<your-name>"` | Set global username |
| `git config --global user.email "<your-email>"` | Set global email |
| `git config --list` | Display config settings |

---

## Working With Files
Commands used to track, untrack, restore, delete, and manage files inside your Git working directory and staging area.

| Command | Description |
|--------|-------------|
| `git status` | Show file status |
| `git add <file>` | Add file to staging |
| `git add .` | Add all files to staging |
| `git reset <file>` | Unstage a file |
| `git rm <file>` | Delete a file and stage removal |
| `git restore <file>` | Restore file from last commit |
| `git restore --staged <file>` | Unstage changes |
| `git mv <old> <new>` | Move or rename a file |

---

## Commit Operations
Commands related to creating commits, viewing commit history, and inspecting detailed changes.

| Command | Description |
|--------|-------------|
| `git commit -m "<message>"` | Commit staged changes |
| `git commit -am "<message>"` | Add & commit tracked files |
| `git log` | View commit history |
| `git log --oneline` | Short commit log |
| `git show <commit>` | Show details of a commit |

---

## Branching
Commands to create, switch, merge, and delete branches for parallel development workflows.

| Command | Description |
|--------|-------------|
| `git branch` | List branches |
| `git branch <name>` | Create a new branch |
| `git checkout <branch>` | Switch to a branch |
| `git checkout -b <name>` | Create and switch |
| `git switch <branch>` | Switch to a branch |
| `git merge <branch>` | Merge a branch into current |
| `git branch -d <branch>` | Delete a branch |

---

## Pushing & Pulling
Commands used to sync changes with remote repositories—push your updates or fetch/pull others’ work.

| Command | Description |
|--------|-------------|
| `git remote -v` | Show remote URLs |
| `git remote add origin <url>` | Add a remote |
| `git push -u origin <branch>` | Push and set upstream |
| `git push` | Push changes |
| `git pull` | Pull latest changes |
| `git fetch` | Fetch updates only |
| `git push --force-with-lease` | Safe force push |
| `git pull --ff-only` | Fast-forward only pull |

---

## Reset & Revert
Commands that manipulate commit history or undo changes without losing your working directory state.

| Command | Description |
|--------|-------------|
| `git reset --soft <commit>` | Move HEAD, keep staged changes |
| `git reset --hard <commit>` | Reset and remove local changes |
| `git revert <commit>` | Undo commit with a new commit |
| `git checkout <commit>` | Checkout any commit |
| `git checkout HEAD~1` | Move to previous commit |

---

## Cleanup
Commands to remove untracked files, reset your workspace, and clean up unnecessary changes safely.

| Command | Description |
|--------|-------------|
| `git clean -n` | Preview files to be deleted |
| `git clean -f` | Delete untracked files |
| `git clean -fd` | Delete untracked files & directories |
| `git reset --hard` | Discard all local changes |

---

## GitHub CLI Commands
Commands from GitHub CLI (gh) to interact with GitHub directly—creating repos, PRs, issues, and authentication.

| Command | Description |
|--------|-------------|
| `gh auth login` | Authenticate to GitHub |
| `gh repo create` | Create a new repository |
| `gh issue list` | List issues |
| `gh pr create` | Create a pull request |
| `gh pr merge <id>` | Merge a pull request |

---

## Rebase
Commands for rewriting commit history by moving or reorganizing commits, typically used for cleaner branch histories.

| Command | Description |
|--------|-------------|
| `git rebase <branch>` | Rebase current branch onto another |
| `git rebase --continue` | Continue after resolving conflicts |
| `git rebase --abort` | Abort rebase |
| `git rebase --skip` | Skip current patch |
| `git rebase -i <commit>` | Interactive rebase |
| `git pull --rebase` | Pull with rebase |
| `git rebase --onto <newbase> <upstream> <branch>` | Advanced rebase operation |
| `git reflog` | View reference logs for recovery |

---

## Stash Commands
Commands to temporarily save uncommitted changes so you can work on something else and restore them later.

| Command | Description |
|--------|-------------|
| `git stash` | Save uncommitted changes |
| `git stash list` | Show all stashes |
| `git stash apply` | Reapply latest stash |
| `git stash pop` | Apply and remove latest stash |
| `git stash drop` | Delete a specific stash |

---

## Tagging (Release Management)
Commands for creating, managing, and pushing tags used in release versions and milestones.

| Command | Description |
|--------|-------------|
| `git tag` | List tags |
| `git tag <tag>` | Create a lightweight tag |
| `git tag -a <tag> -m "<msg>"` | Create an annotated tag |
| `git push origin <tag>` | Push a single tag |
| `git push --tags` | Push all tags |
| `git tag -d <tag>` | Delete local tag |
| `git push origin --delete <tag>` | Delete remote tag |

---

## Cherry-pick
Commands to pick specific commits from one branch and apply them on another without merging everything.

| Command | Description |
|--------|-------------|
| `git cherry-pick <commit>` | Apply a specific commit |
| `git cherry-pick --abort` | Abort cherry-pick |
| `git cherry-pick --continue` | Continue after conflict |

---

## Submodules
Commands to include external repositories inside your project and keep them updated.

| Command | Description |
|--------|-------------|
| `git submodule add <repo> <path>` | Add a submodule |
| `git submodule update --init` | Initialize submodules |
| `git submodule sync` | Synchronize submodule URLs |

---

## Inspect & Search
Commands used to analyze repository changes, find who modified what, and search within codebases.

| Command | Description |
|--------|-------------|
| `git blame <file>` | Show who modified each line |
| `git grep "<text>"` | Search text inside repository |
| `git shortlog -sn` | Show contributor commit counts |

---

## Additional Useful Tips

```bash
git add -p        # Interactive staging
git diff          # View unstaged changes
git diff --staged # View staged changes
