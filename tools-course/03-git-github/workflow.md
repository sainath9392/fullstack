# Git Workflow - Notes & Observations

This document contains a simple Git workflow along with **personal observations and tips** from practical use.

---

## 1. Configure Git (First Time Only)

```bash
git config --global user.name "Your Name"
git config --global user.email "your_email@example.com"
git config --list
```

**Observations:**
- Always configure your name and email before committing.  
- Check configuration with `git config --list` to avoid wrong author info.  
- If using multiple machines, you can override per-repository with `git config user.name "Other Name"`.

---

## 2. Initialize Repository

```bash
cd /path/to/project
git init
git status
```

**Observations:**
- `git init` only needs to be run once per project.  
- `git status` is very useful to see untracked files and staged changes.  
- The `.git` folder is hidden in your project root; it stores all Git metadata.

---

## 3. Add & Commit Changes

```bash
git add .                 # Add all files to staging
git commit -m "Initial commit"
```

**Observations:**
- `git add .` stages all changes, but sometimes it’s safer to add files individually (`git add filename`) to avoid committing unwanted files.  
- Commit messages should be **clear and concise**; good messages make history easier to understand.  
- Always commit small, logical changes rather than large unrelated changes.

---

## 4. Connect to Remote Repository

```bash
git remote add origin git@github.com:username/repo.git
git remote -v
```

**Observations:**
- Use SSH keys for secure authentication instead of HTTPS to avoid repeatedly entering your password.  
- `git remote -v` is useful to verify the remote URL.  
- If the remote already exists, you can update it using `git remote set-url origin <new-url>`.

---

## 5. Push Changes

```bash
git branch -M main        # Rename branch to main if needed
git push -u origin main
```

**Observations:**
- `-u` sets upstream tracking so that next `git push` or `git pull` can be done without specifying the branch.  
- Renaming the default branch to `main` is now standard practice.  

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

**Observations:**
- Branching allows parallel development without affecting `main`.  
- Always make meaningful branch names (`feature/login`, `bugfix/navbar`).  
- `git switch` is simpler and less error-prone than `git checkout`.

---

## 7. Useful Commands

| Command | Description | Observation |
|---------|-------------|-------------|
| git status | Check current changes | Use frequently to avoid accidental commits |
| git log | View commit history | Helps track history and debug issues |
| git diff | Show changes before commit | Great for reviewing changes |
| git pull | Pull latest changes from remote | Keep your branch updated |
| git fetch | Fetch updates from remote without merging | Safe way to check remote changes |
| git clone URL | Clone a repository | Use SSH for easier authentication |

---

## ✅ Key Personal Observations

- Regular commits keep work manageable and help track progress.  
- Always check `git status` before adding or committing files.  
- Clear commit messages and branch names improve collaboration.  
- Using SSH keys with GitHub/GitLab avoids repeated authentication issues.  
- Branching workflow (`feature`, `bugfix`, `release`) keeps code organized.

