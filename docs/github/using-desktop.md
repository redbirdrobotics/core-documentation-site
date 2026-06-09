---
# File: docs/github/using-desktop.md
title: "Using GitHub Desktop"
parent: GitHub
nav_order: 4
---

# Using Git with GitHub Desktop

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
