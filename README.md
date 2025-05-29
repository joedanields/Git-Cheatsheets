# 🚀 Ultimate Git Guide & Cheat Sheet

A comprehensive guide to mastering Git — from beginner to advanced — with detailed commands, workflows, cheat sheets, and best practices.

---

## 📘 Table of Contents

1. [Git Basics](#git-basics)
2. [Common Git Commands](#common-git-commands)
3. [Branching](#branching)
4. [Remote Repositories](#remote-repositories)
5. [Merging and Rebasing](#merging-and-rebasing)
6. [Stashing](#stashing)
7. [Tagging](#tagging)
8. [Undoing Changes](#undoing-changes)
9. [Logs and History](#logs-and-history)
10. [Working with `.gitignore`](#working-with-gitignore)
11. [Advanced Git](#advanced-git)
12. [Cheat Sheet Summary](#cheat-sheet-summary)
13. [Best Practices](#best-practices)
14. [Troubleshooting Git](#troubleshooting-git)
15. [GUI Tools for Git](#gui-tools-for-git)

---

## ⚙️ Git Basics

```bash
# Initialize a Git repository
$ git init

# Clone a repository
$ git clone <repository-url>

# Check repository status
$ git status

# Add files to staging
$ git add <filename>
$ git add .

# Commit changes
$ git commit -m "Your message"
```

---

## 🔁 Common Git Commands

```bash
# List all branches
$ git branch

# Switch to a branch
$ git checkout <branch-name>

# Create and switch to a branch
$ git checkout -b <branch-name>

# Delete a branch
$ git branch -d <branch-name>

# Rename current branch
$ git branch -m <new-branch-name>
```

---

## 🌿 Branching

```bash
# Show branches with last commit
$ git branch -v

# List remote branches
$ git branch -r

# Track remote branch
$ git checkout --track origin/<branch-name>
```

---

## 🌍 Remote Repositories

```bash
# Add a remote
$ git remote add origin <url>

# View remote URLs
$ git remote -v

# Push to remote
$ git push origin <branch>

# Pull from remote
$ git pull origin <branch>

# Set upstream branch
$ git push -u origin <branch>
```

---

## 🔀 Merging and Rebasing

```bash
# Merge branch into current
$ git merge <branch-name>

# Rebase current branch onto another
$ git rebase <branch-name>

# Abort merge/rebase
$ git merge --abort
$ git rebase --abort

# Resolve conflicts manually, then:
$ git add .
$ git rebase --continue
```

---

## 💾 Stashing

```bash
# Save uncommitted changes
$ git stash

# List stashes
$ git stash list

# Apply last stash
$ git stash apply

# Apply and drop stash
$ git stash pop

# Drop specific stash
$ git stash drop stash@{1}

# Clear all stashes
$ git stash clear
```

---

## 🏷️ Tagging

```bash
# Create a lightweight tag
$ git tag v1.0

# Create an annotated tag
$ git tag -a v1.0 -m "Version 1.0"

# List tags
$ git tag

# Show tag details
$ git show v1.0

# Push tags to remote
$ git push origin --tags
```

---

## 🧹 Undoing Changes

```bash
# Unstage a file
$ git reset <file>

# Undo last commit (keep changes)
$ git reset --soft HEAD~1

# Undo last commit and changes
$ git reset --hard HEAD~1

# Revert a commit (safe undo)
$ git revert <commit-hash>

# Clean untracked files
$ git clean -f
```

---

## 📜 Logs and History

```bash
# View commit history
$ git log

# Compact history
$ git log --oneline

# Pretty graph
$ git log --oneline --graph --all

# Who changed what
$ git blame <file>

# Show file history
$ git log <file>
```

---

## 📄 Working with `.gitignore`

Examples of common patterns:

```
# Node modules
node_modules/

# Logs
*.log

# OS-specific
.DS_Store
Thumbs.db

# Environment files
.env
```

---

## 🚀 Advanced Git

```bash
# Reflog: see all HEAD changes
$ git reflog

# Amend last commit (e.g., change message)
$ git commit --amend

# Squash commits interactively
$ git rebase -i HEAD~n

# Bisect for bug hunting
$ git bisect start
$ git bisect bad
$ git bisect good <commit>
```

---

## 🔥 Cheat Sheet Summary

| Task          | Command                  |
| ------------- | ------------------------ |
| Init repo     | `git init`               |
| Clone repo    | `git clone <url>`        |
| Add all files | `git add .`              |
| Commit        | `git commit -m "msg"`    |
| New branch    | `git checkout -b branch` |
| Push          | `git push origin branch` |
| Pull          | `git pull origin branch` |
| Merge         | `git merge branch`       |
| Rebase        | `git rebase branch`      |
| Stash         | `git stash`              |
| Tag           | `git tag v1.0`           |

---

## ✅ Best Practices

* ✅ Use meaningful commit messages.
* ✅ Branch for each feature.
* ✅ Pull before you push.
* ✅ Review before merging.
* ✅ Use `.gitignore` smartly.
* ✅ Tag stable versions.
* ✅ Never commit secrets.

---

## 🧰 Troubleshooting Git

```bash
# Force push (use with caution!)
$ git push -f origin <branch>

# Remove untracked files/directories
$ git clean -fd

# Detach HEAD fix
$ git checkout main
```

---

## 🖥 GUI Tools for Git

* [GitHub Desktop](https://desktop.github.com/)
* [Sourcetree](https://www.sourcetreeapp.com/)
* [GitKraken](https://www.gitkraken.com/)
* [VSCode Git Integration](https://code.visualstudio.com/)

---

> Made with ❤️ for developers who want to master Git!
