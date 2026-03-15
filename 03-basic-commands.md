# Git Basic Commands

---

## Initialize Repository

The 'git init' command creates a new Git repository in the current folder.

```bash
git init

After running this command, Git starts tracking the project files.

## Check Repository Status

The git status command shows the current state of the repository.

```bash
git status

It displays:

1. modified files

2. staged files

3. untracked files

## Add Files to Staging Area

The git add command adds files to the staging area before committing.

Add a specific file:

```bash
git add filename.txt

Add all files in the folder:

```bash
git add .

The staging area allows you to choose which changes will be included in the next commit.

## Commit Changes

The git commit command saves the staged changes to the repository history.

```bash
git commit -m "Initial commit"

The -m flag allows you to write a short commit message describing the changes.

The message explains what changes were made.

## View Commit History

The git log command shows the history of commits in the repository.

```bash
git log

It displays:

- commit ID

- author

- date

- commit message
This helps track the development history of the project.

## Clone a Repository

The git clone command copies an existing repository from GitHub to your local computer.

```bash
git clone repository_url

Example:

```bash
git clone https://github.com/username/project-name.git

## Push Changes to GitHub

The git push command uploads your local commits to a remote repository.

```bash 
git push origin main

This updates the repository on GitHub.

## Pull Latest Changes

The git pull command downloads the latest changes from the remote repository.

```bash
git pull origin main

This keeps your local repository updated.