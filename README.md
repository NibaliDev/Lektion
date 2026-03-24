# Git & GitHub — Complete Beginner's Guide

---

## Part 1: Installing Git

### 🪟 Windows
1. Go to **https://git-scm.com/download/win** — the download starts automatically
2. Run the `.exe` installer
3. During setup, keep defaults **except**:
   - PATH: select **"Git from the command line and also from 3rd-party software"**
   - Line endings: **"Checkout Windows-style, commit Unix-style"**
4. Open Command Prompt and verify:
```bash
git --version
```

---

### 🍎 macOS
**Option 1 — Homebrew (recommended):**
```bash
brew install git
```
**Option 2 — No Homebrew:**  
Open Terminal and type `git` — macOS will prompt you to install it automatically.

---

### 🐧 Linux

**Ubuntu / Debian:**
```bash
sudo apt-get update
sudo apt-get install git
```

**Fedora / RHEL:**
```bash
sudo dnf install git
```

---

### ⚙️ First-Time Setup (all platforms)
After installing, set your identity — required before your first commit:
```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

---

## Part 2: Using GitHub

### 1. Create an Account
Go to **https://github.com** and sign up for a free account.

---

### 2. Create a New Repository
1. Click the **"+"** icon in the top right → **"New repository"**
2. Give it a name (e.g. `my-project`)
3. Choose **Public** or **Private**
4. Check **"Add a README file"**
5. Click **"Create repository"**

---

### 3. Clone a Repository (download it to your computer)
```bash
git clone https://github.com/username/my-project.git
cd my-project
```

---

### 4. Basic Daily Workflow

#### Check what has changed
```bash
git status
```

#### Stage your changes
```bash
git add .            # stage all changes
git add file.py      # stage a specific file
```

#### Commit your changes
```bash
git commit -m "Your message describing what you changed"
```

#### Push to GitHub
```bash
git push
```

#### Pull latest changes from GitHub
```bash
git pull
```

---

### 5. Branching
Branches let you work on features without affecting the main code.

```bash
git branch feature-login       # create a new branch
git checkout feature-login     # switch to it
# or do both in one command:
git checkout -b feature-login
```

Push a branch to GitHub:
```bash
git push -u origin feature-login
```

---

### 6. Pull Requests (PR)
A Pull Request is how you propose merging your branch into `main` on GitHub.

1. Push your branch to GitHub
2. Go to your repository on GitHub
3. Click **"Compare & pull request"**
4. Add a description and click **"Create pull request"**
5. After review, click **"Merge pull request"**

---

### 7. Common Commands Cheat Sheet

| Command | Description |
|---|---|
| `git init` | Initialize a new local repo |
| `git clone <url>` | Clone a remote repo |
| `git status` | Show changed files |
| `git add .` | Stage all changes |
| `git commit -m "msg"` | Commit staged changes |
| `git push` | Push commits to GitHub |
| `git pull` | Pull latest from GitHub |
| `git branch` | List branches |
| `git checkout -b <name>` | Create and switch to branch |
| `git merge <branch>` | Merge a branch into current |
| `git log --oneline` | View commit history |

---

### 8. Connecting Local Repo to GitHub
If you already have a local project and want to push it to GitHub:

```bash
git init
git add .
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/username/my-project.git
git push -u origin main
```

---

## Useful Links
- Git documentation: https://git-scm.com/doc
- GitHub documentation: https://docs.github.com
- GitHub Desktop (GUI app): https://desktop.github.com