---
# File: github/github-setup.md
title: "GitHub Setup Guide"
nav_order: 20
---

# GitHub Setup Guide

Welcome! This guide will help you set up GitHub for all Redbird Robotics projects. We recommend using **GitHub Desktop** for simplicity, but advanced users can optionally use Git Bash.

---

## 1. Create a GitHub Account

1. Go to [https://github.com](https://github.com)  
2. Click **Sign up** and follow the instructions.  
3. Use your **personal email** if possible — your university email will disappear when you leave college, its nice to have a way to see your work once you're done.  
4. Choose a username that is **professional and consistent**, e.g., `first-last` or `first_last`.

---

## 2. Install GitHub Desktop

1. Download GitHub Desktop: [https://desktop.github.com](https://desktop.github.com)  
2. Install and open the application.  
3. Sign in with your GitHub account.  
4. Select **“Clone a repository”** when prompted.

> GitHub Desktop handles Git for you — you do not need Git Bash unless you want to use the command line.

---

## 3. Configure Git (Desktop handles most of this)

1. In GitHub Desktop, go to **File → Options → Git**  
2. Make sure your **Name** and **Email** match your GitHub account. your username is not used here
3. Optional: Set your preferred editor (VS Code is recommended).

---

## 4. Clone a Repository

1. From GitHub Desktop, click **File → Clone Repository → URL**  
2. Paste the repo URL (provided by your team lead, or by going to the repo on GitHub, hitting code, and copying the HTTPS URL)
3. Choose a **local folder** to store the project. we recommend creating a dedicated folder for all redbird related projects  
4. Click **Clone**

> After cloning, you now have a local copy of the repository that syncs with GitHub.

---

## 5. Making Changes

1. Open the repository folder in your editor or CAD software.  
2. Make changes to files (code, CAD, or documentation).  
3. In GitHub Desktop, you will see **Changes** listed.  
4. Write a descriptive **commit message** and click **Commit to `branch-name`**.  

> Good commit messages help teammates understand your changes, e.g., “Fixed claw mate in arm assembly” or “Updated motor driver code.”

---

## 6. Pushing Changes

1. After committing, click **Push origin** in GitHub Desktop to upload your changes to GitHub.  
2. If someone else has pushed changes since you last pulled, GitHub Desktop will prompt you to **pull first**.

---

## 7. Branching Workflow

1. Always work in a **branch**, never directly on `main`. Leave main for "stable versions" or working prototypes of your projects, and branch to work on individual features.
2. Create a branch for your feature or part:  
   - Example: `claw-assembly` or `motor-code`  
3. Make your changes in that branch, then create a **Pull Request** (PR) on GitHub to merge into `main`.  
4. PRs allow other team members to review changes before merging.

---

## 8. Optional: Using Git Bash

If you want to use the command line, here are the basics:

```bash
# Clone a repo
git clone <repo-url>

# Check current branch
git status

# Create a new branch
git checkout -b feature-branch

# Stage changes
git add <file> (or . for all changed files)

# Commit changes
git commit -m "Descriptive message"

# Push to GitHub
git push origin feature-branch

# Pull latest changes from main
git pull origin main
```

> Only use Git Bash if you’re comfortable with the commands. GitHub Desktop handles all of this visually.

## 9. Best Practices

- Pull before starting work on the assembly or code. this helps prevent conflicts with independent work.
- Commit often, but make messages clear and descriptive.
- Work on separate files or subassemblies to minimize merge conflicts.
- Communicate when making major assembly edits — only one person edits the assembly at a time if possible.
