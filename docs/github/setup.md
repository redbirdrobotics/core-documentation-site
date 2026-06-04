---
# File: docs/github/setup.md
title: "GitHub Setup Guide"
nav_category: "GitHub"
nav_order: 25
---

# GitHub Desktop Setup Guide

This guide will help you set up GitHub for all Redbird Robotics projects. We recommend using **GitHub Desktop** for simplicity, but advanced users can optionally use Git Bash. Use the quick links to skip to the portions you need info on.

- [Installing GitHub Desktop](#installing)
- [Setting Up GitHub Desktop](#setting-up)
- [Cloning Repositories](#cloning)
- [Committing Changes](#committing)
- [Pushing and Pulling Work](#pushing-pulling)
- [Creating Repositories](#creating)
- [Creating Pull Requests and Merging Work](#prs)

---

# Installing GitHub Desktop {#installing}

You can get a quick link to installing GitHub Desktop through [the official download site](https://desktop.github.com/download/). This page provides the download for both the Windows and MacOS versions of GitHub Desktop.

![GitHub Desktop download site]({{site.baseurl}}/assets/images/github-setup/github-desktop-download-site.png)

Select the option that relates to you and download the program. Once downloaded, follow through with the installation as with any other program. Once it's done pull up the program to begin setup.

---

# Setting Up GitHub Desktop {#setting-up}

## 1. First Time Launching

Once the program is installed and opened for the first time you screen will prompt you to "Sign in to GitHub.com". This requires you to have had a GitHub account set up prior but if you haven't created one you will have the opportunity in the following steps.

![GitHub Deskop first time launch screen](/assets/images/github-setup/first-time-launch.png)

Press the "Sign in" button to proceed to the next step.

## 2. Signing In

Once you press the button a browser window will pop up. If you have already signed into GitHub on that browser before you will be prompted to continue with that account.

![GitHub sign into account page](/assets/images/github-setup/logging-in.png)

Proceed with this account if it's the correct one otherwise, if it's not the right one select the other option. If you don't have an account showing up, create an account. Follow [this guide](https://redbirdrobotics.github.io/core-documentation-site/docs/github/new.html) for more details about account creation.

## 3. Requesting Access to Account

Once you've signed in, GitHub will ask you if you want to "Authorize" GitHub Desktop to have access to your account. Just press Authorize to continue.

![GitHub request for access to account](/assets/images/github-setup/requesting-access.png)

Once you've authorized the application it will change to a new screen telling you it's safe to close the window and to proceed on the application.

## 4. Setting Up Git

Back on the GitHub Desktop Application, you may be prompted to set up Git. I was, this is what it looked like for me.

![configuring git on GitHub Desktop](/assets/images/github-setup/configuring-git.png)

All this information needs to be is your name and email that are used on your GitHub account. They should automatically populate like they have for me so you shouldn't need to do anything otherwise.

## 5. And It's Done

Once the program's finished it's own work you should be shown the front page for GitHub Desktop. This marks the end of the initial setup for GitHub desktop.

![github desktop front page](/assets/images/github-setup/gh-desktop-start-page.png)

## 6. Brief Room Tour

To the left of the page you will see "Your repositories" which are all of the repositories you've created, accessed, or been given access to.

To the right are the options to Create a new repo, Cloning one from a link or your list, or options from uploading or creating them from a local file. You will mostly only be using the top two options for the majority of your time using Git and GitHub.

# Using GitHub - Cloning Repositories {#cloning}

# Using GitHub - Committing Changes {#committing}

# Using GitHub - Pushing and Pulling Work {#pushing-pulling}

# Using GitHub - Creating Repositories {#creating}

# Using GitHub - Pull Requests and Merging {#prs}

## 1. Create a GitHub Account

1. Go to [https://github.com](https://github.com)  
2. Click **Sign up** and follow the instructions.  
3. Use your **personal email** if possible — your university email will disappear when you leave college, its nice to have a way to see your work once you're done.  
4. Choose a username that is **professional and consistent**, e.g., `first-last` or `first_last`.

---

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

# Test Path

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
