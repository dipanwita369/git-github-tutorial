# Git Branching

Branching is a powerful feature in Git that allows developers to work on different features or fixes without affecting the main project.

---

## What is a Branch

A branch is a separate line of development in a repository.

The default branch is usually called:
```bash
main
```
Developers create new branches to work on:

- new features
- bug fixes
- experiments

---

## Why Branching is Important

Branching helps developers:

- work on multiple features simultaneously
- avoid breaking the main project
- collaborate safely with other developers

---

## Check Current Branch

Use the following command to see the current branch.

```bash
git branch
```

The current branch will have a star (*) next to it.

Example output:
```
* main
```

## Create a New Branch

Create a new branch using:

```bash
git branch feature-login
```
This creates a new branch for a feature named `feature-login`.

But you are still on the `main` branch.

## Switch to Another Branch

To start working on the new branch, switch to it using:

```bash
git checkout feature-login
```
Now the current branch becomes:

```
* login-feature
```
Any changes you make will be saved in the `login-feature` branch, not in the `main` branch.

## Create and Switch Branch in One Command

Instead of creating and switching separately, Git provides a shortcut:
```bash
git checkout -b signup-feature
```
This command will:

1. Create a new branch called `signup-feature`

2. Immediately switch to that branch

## View All Branches

To see all branches in the repository:
```bash
git branch
```
Example output:
```
main
login-feature
signup-feature
```
The branch with `*` is the active branch.


## Example Development Workflow

A typical development process:

1. Start from the main branch

2. Create a new branch for a feature

3. Work on that feature

4. Commit changes in that branch

5. Later merge the branch into main

Example:
```
main
│
├── login-feature
│
└── signup-feature
```
Each branch contains its own development work.

---

# Git Merge and Delete Branch

After completing work in a feature branch, developers usually merge that branch into the main branch.

Once the branch is merged, it is often deleted because it is no longer needed.

---

## Example Scenario

Suppose the repository has the following branches:
```
main  
login-feature
```
The developer created the `login-feature` branch to implement a login system.

All development work and commits were done in the `login-feature` branch.

Now the feature is complete and we want to merge it into `main`.


## Step 1: Check Current Branch

First check which branch you are currently on.

```bash
git branch
```

Example output:

```
* login-feature
  main
```

The `*` symbol indicates the current branch.


## Step 2: Switch to Main Branch

Before merging, switch to the `main` branch.

```bash
git checkout main
```

Now the active branch becomes:

```
* main
  login-feature
```


## Step 3: Merge the Feature Branch

Merge the `login-feature` branch into `main`.

```bash
git merge login-feature
```

Git will combine all changes from the `login-feature` branch into `main`.


## Step 4: Check Commit History

You can verify the merge using:

```bash
git log
```

The commit history will now include the commits from `login-feature`.


## Step 5: Delete the Branch

After merging, the feature branch is usually deleted.

```bash
git branch -d login-feature
```

Now the repository will only contain:

```
* main
```


## Example Workflow

Before merge:

```
main
│
└── login-feature
     └── login feature development
```

After merge:

```
main
│
└── login feature included
```

The `login-feature` branch can now be deleted.

