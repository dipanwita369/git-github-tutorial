# Clone a Repository from GitHub

Cloning a repository means creating a copy of a remote repository on your local computer.

Developers use cloning when they want to download a project from GitHub and work on it locally.

---

## What is Git Clone

The `git clone` command copies an entire repository including:

- Source code
- Commit history
- Branches
- Configuration files

---

## Basic Syntax

```bash
git clone repository_url
```
Example

```bash
git clone https://github.com/username/project-name.git
```
After running the command, Git will download the project to your computer.

# Step-by-Step Process
## Step 1: Copy Repository URL

Open the repository on GitHub.

Click Code and copy the HTTPS URL.

Example:
```bash
https://github.com/username/project-name.git
```
## Step 2: Open Terminal

Navigate to the folder where you want to store the project.

Example:
```bash
cd Desktop
```
## Step 3: Run Clone Command
```bash
git clone https://github.com/username/project-name.git
```
Git will create a new folder with the project files.

## Example Folder Structure After Cloning
```
project-name
│
├── README.md
├── src
├── docs
└── files
```
## Move Into the Project Folder

After cloning, go inside the project folder.
 ```bash
cd project-name
Check Repository Status
```

You can check the repository status.
```bash
git status
```