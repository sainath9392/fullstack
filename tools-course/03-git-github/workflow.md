# Git Workflow - Simple Guide

This document describes a simple Git workflow for initializing, committing, branching, and pushing changes.

---

## 1. Configure Git (First Time Only)

```bash
git config --global user.name "Your Name"
git config --global user.email "your_email@example.com"
git config --list
```

---

## 2. Initialize Repository

```bash
cd /path/to/project
git init
git status
```

---

## 3. Add & Commit Changes

```bash
git add .                 # Add all files to staging
git commit -m "Initial commit"
```

---

## 4. Connect to Remote Repository

```bash
git remote add origin git@github.com:username/repo.git
git remote -v
```

---

## 5. Push Changes

```bash
git branch -M main        # Rename branch to main if needed
git push -u origin main
```

---

## 6. Branching

### Create and switch to a new branch
```bash
git checkout -b feature-branch
```

### Switch to an existing branch
```bash
git checkout main
```

### Modern alternative
```bash
git switch -c feature-branch   # create and switch
git switch main                 # switch only
```

---

## 7. Useful Commands

| Command | Description |
|---------|-------------|
| git status | Check current changes |
| git log | View commit history |
| git diff | Show changes before commit |
| git pull | Pull latest changes from remote |
| git fetch | Fetch updates from remote without merging |
| git clone URL | Clone a repository |

---

✅ This workflow helps you manage Git repositories efficiently.
