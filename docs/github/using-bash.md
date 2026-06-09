---
# File: docs/github/using-bash.md
title: "Using Git Bash"
parent: GitHub
nav_order: 5
---

# Using Git with Git Bash

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
