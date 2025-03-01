# Git & GitHub CLI Complete Guide

## Repository Overview
This repository contains a beginner-friendly, step-by-step guide on using **Git and GitHub** via the command line. It is designed for absolute beginners who want to learn how to manage version control efficiently. The guide covers installation, setup, repository management, commits, pushing, pulling, branching, merging, undoing mistakes, and more!

## Step 1. Install Git

If you don't have Git installed, follow these steps:
- **Windows:** Download and install Git from [git-scm.com](https://git-scm.com/).
- **Mac:** Open Terminal and run:
  ```sh
  brew install git
  ```
- **Linux:** Open Terminal and run:
  ```sh
  sudo apt install git  # For Debian-based systems
  sudo yum install git  # For RedHat-based systems
  ```

## Step 2. Set Up Git (One-Time Setup)

After installing Git, configure your identity:
```sh
  git config --global user.name "Your Name"
  git config --global user.email "your-email@example.com"
```
To check if it's set correctly:
```sh
  git config --global --list
```

## Step 3. Create a New Git Project

1. Open Terminal or Command Prompt.
2. Navigate to your project folder:
   ```sh
   cd path/to/your/project
   ```
3. Initialize Git in the folder:
   ```sh
   git init
   ```
   This creates a hidden `.git` folder where Git tracks changes.

## Step 4. Add and Save Files

1. Check which files changed:
   ```sh
   git status
   ```
2. Add files to be saved (staged):
   ```sh
   git add filename.txt  # Add a specific file
   git add .             # Add all files in the folder
   ```
3. Save your changes (commit):
   ```sh
   git commit -m "Your message here"
   ```
   Example:
   ```sh
   git commit -m "Added homepage design"
   ```

## Step 5. Connect to GitHub

1. Go to [GitHub](https://github.com) and create an account.
2. Create a new repository (repo) on GitHub.
3. Copy the repository URL (e.g., `https://github.com/your-username/repo-name.git`).
4. Link your local project to GitHub:
   ```sh
   git remote add origin https://github.com/your-username/repo-name.git
   ```
5. Check if it's linked correctly:
   ```sh
   git remote -v
   ```

## Step 6. Upload Your Code to GitHub

1. Upload your commits to GitHub:
   ```sh
   git push -u origin main
   ```
   If your branch is called `master`, use:
   ```sh
   git push -u origin master
   ```
2. If asked, enter your GitHub username and password.

## Step 7. Download (Clone) a GitHub Repository

If you want to copy a project from GitHub to your computer:
```sh
  git clone https://github.com/username/repository.git
```

## Step 8. Get Latest Updates from GitHub

If your project is already linked to GitHub and you want the latest changes:
```sh
  git pull origin main
```

## Step 9. Work with Branches

Branches allow you to work on different versions of your project.
- Create a new branch:
  ```sh
  git branch new-feature
  ```
- Switch to the new branch:
  ```sh
  git checkout new-feature
  ```
- Merge a branch into main:
  ```sh
  git checkout main
  git merge new-feature
  ```
- Push the branch to GitHub:
  ```sh
  git push -u origin new-feature
  ```

## Step 10. Undo Mistakes

- Undo last commit (keep changes):
  ```sh
  git reset --soft HEAD~1
  ```
- Undo last commit (delete changes):
  ```sh
  git reset --hard HEAD~1
  ```
- Restore a deleted file:
  ```sh
  git checkout -- filename.txt
  ```

## Conclusion
This guide helps you get started with Git and GitHub using simple commands. Keep practicing to get more comfortable!
