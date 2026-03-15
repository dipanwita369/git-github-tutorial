# Upload a Project to GitHub

This guide explains how to upload a local project to GitHub using Git.

---

## Step 1: Create or Open Your Project

First create a project folder on your computer.

Example:

project-folder

Inside it you may have files like:

- index.html
- style.css
- script.js

Open this folder in your code editor(ex. VS Code).



## Step 2: Initialize Git Repository

Open terminal in the project folder and run:

```bash
git init
```

This creates a new Git repository and starts tracking the project.

## Step 3: Check Project Status

Use the following command to see untracked files.

```bash
git status
```

Git will show all files that are not yet tracked.

## Step 4: Add Files to Staging Area

Add all files to staging.
```bash
git add .
```

This prepares files for commit.

## Step 5: Commit the Files

Now save the changes to the repository history.

```bash
git commit -m "Initial project commit"
```

A commit records the current version of the project.

## Step 6: Create a Repository on GitHub

Go to GitHub and create a new repository.

Steps:

- Click New Repository

- Enter repository name

- Choose Public or Private

- Click Create Repository

Do not add README if your project already has files.

## Step 7: Connect Local Repository to GitHub

Copy the repository URL from GitHub.

Example:

```bash
https://github.com/username/project-name.git
```

Then run:

```bash
git remote add origin https://github.com/username/project-name.git
```
This connects your local repository to GitHub.

## Step 8: Set Main Branch

```bash
git branch -M main
```

This ensures the branch name is main.

## Step 9: Push Project to GitHub

Upload the project to GitHub.

```bash
git push -u origin main
```
Now your project will appear on GitHub.

## Step 10: Verify Upload

Open your repository on GitHub.

You should see all your project files.

## Complete Workflow

The typical developer workflow:

1. Create project
2. Initialize Git
3. Add files
4. Commit changes
5. Create GitHub repository
6. Connect repository
7. Push code

## Preview in VS Code

Press:

Ctrl + Shift + V

You will see the Markdown preview.