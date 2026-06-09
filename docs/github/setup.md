---
# File: docs/github/setup.md
title: "GitHub Setup Guide"
parent: GitHub
nav_order: 2
---

# GitHub Desktop Setup Guide

This guide will help you set up GitHub for all Redbird Robotics projects. We recommend using **GitHub Desktop** for simplicity, but advanced users can optionally use Git Bash. Use the quick links to skip to the portions you need info on.

- [GitHub Desktop](#desktop)
- [Git Bash](#bash)

> Git Bash allows you to use written commands to use Git, for most users it is recommended to only use the GitHub Desktop as it makes using Git a lot easier and more intuitive. As a general rule, unless you're confident with [Command Line Interfaces](https://en.wikipedia.org/wiki/Command-line_interface), avoid Git Bash.

---

# Installing GitHub Desktop {#desktop}

You can get a quick link to installing GitHub Desktop through [the official download site](https://desktop.github.com/download/). This page provides the download for both the Windows and MacOS versions of GitHub Desktop.

![GitHub Desktop download site]({{site.baseurl}}/assets/images/github-setup/github-desktop-download-site.png)

Select the option that relates to you and download the program. Once downloaded, follow through with the installation as with any other program. Once it's done pull up the program to begin setup.

---

# Setting Up GitHub Desktop

## 1. First Time Launching

Once the program is installed and opened for the first time you screen will prompt you to "Sign in to GitHub.com". This requires you to have had a GitHub account set up prior but if you haven't created one you will have the opportunity in the following steps.

![GitHub Deskop first time launch screen]({{site.baseurl}}/assets/images/github-setup/first-time-launch.png)

Press the "Sign in" button to proceed to the next step.

## 2. Signing In

Once you press the button a browser window will pop up. If you have already signed into GitHub on that browser before you will be prompted to continue with that account.

![GitHub sign into account page]({{site.baseurl}}/assets/images/github-setup/logging-in.png)

Proceed with this account if it's the correct one otherwise, if it's not the right one select the other option. If you don't have an account showing up, create an account. Follow [the Quick Start checklist](https://redbirdrobotics.github.io/core-documentation-site/docs/github/quick-start.html) for a concise first-day walkthrough.

## 3. Requesting Access to Account

Once you've signed in, GitHub will ask you if you want to "Authorize" GitHub Desktop to have access to your account. Just press Authorize to continue.

![GitHub request for access to account]({{site.baseurl}}/assets/images/github-setup/requesting-access.png)

Once you've authorized the application it will change to a new screen telling you it's safe to close the window and to proceed on the application.

## 4. Setting Up Git

Back on the GitHub Desktop Application, you may be prompted to set up Git. I was, this is what it looked like for me.

![configuring git on GitHub Desktop]({{site.baseurl}}/assets/images/github-setup/configuring-git.png)

All this information needs to be is your name and email that are used on your GitHub account. They should automatically populate like they have for me so you shouldn't need to do anything otherwise.

## 5. And It's Done

Once the program's finished it's own work you should be shown the front page for GitHub Desktop. This marks the end of the initial setup for GitHub desktop.

![github desktop front page]({{site.baseurl}}/assets/images/github-setup/gh-desktop-start-page.png)

## 6. Brief Room Tour

To the left of the page you will see "Your repositories" which are all of the repositories you've created, accessed, or been given access to.

To the right are the options to Create a new repo, Cloning one from a link or your list, or options from uploading or creating them from a local file. You will mostly only be using the top two options for the majority of your time using Git and GitHub.

# Next Steps

Now that you've finished setting up GitHub, you can should go to one of or all of the following pages to get started:

- [Git Concepts]({{site.baseurl}}/docs/github/concepts.md) to learn some common terminology.
- [Git Using GitHub Desktop]({{site.baseurl}}/docs/github/using-desktop.md) to learn your way around GitHub Desktop.
- [Git Standards]({{site.baseurl}}/docs/standards/git.md) to learn our Git usage standards for commits and contribution.

# Installing Git Bash

> Again, as a general warning, this is only a good idea for those comforable with Linux-like commands.
