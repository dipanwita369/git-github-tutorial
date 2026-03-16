# Git Merge Conflict 

A merge conflict occurs when Git cannot automatically merge changes from two branches.

This often happens when two developers modify the `same file` or `same line of code`.

let,

original file --> `print("Hello");`

Change in main file --> `print("Hello from main");`

Change in feature file --> `print("Hello from feature");`

when merging -->

```bash
git merge feature
```
Git cannot choose which line should remain . This creates a merge conflict.



In this example, we will use a `Python data analytics script`.


# Scenario

Suppose a team is working on a data analysis project.

The repository contains a Python script:

```
sales_analysis.py
```

This script analyzes a dataset using `pandas`.


# Original File (main branch)

```python
import pandas as pd

data = pd.read_csv("sales.csv")

total_sales = data["sales"].sum()

print("Total Sales:", total_sales)
```

Now two developers work on different branches.


# Developer 1 (main branch change)

The developer wants to calculate `average sales`.

```python
import pandas as pd

data = pd.read_csv("sales.csv")

average_sales = data["sales"].mean()

print("Average Sales:", average_sales)
```

# Developer 2 (feature branch: `sales-report`)

Another developer creates a branch:

```bash
git checkout -b sales-report
```

They modify the same code to calculate `maximum sales`.

```python
import pandas as pd

data = pd.read_csv("sales.csv")

max_sales = data["sales"].max()

print("Maximum Sales:", max_sales)
```


# Attempt to Merge

Now we try to merge the branch into main.

```bash
git checkout main
git merge sales-report
```

Git cannot decide which code should stay.

So a `merge conflict occurs`.


# Conflict Marked by Git

Git will modify the file like this:

```python
import pandas as pd

data = pd.read_csv("sales.csv")

<<<<<<< HEAD
average_sales = data["sales"].mean()
print("Average Sales:", average_sales)
=======
max_sales = data["sales"].max()
print("Maximum Sales:", max_sales)
>>>>>>> sales-report
```

Meaning:
```
| Symbol | Meaning |
|------|--------|
| HEAD | Code from current branch (main) |
| ======= | Separator |
| sales-report | Code from merging branch |
```

# Resolve the Conflict

The developer edits the file and keeps both analyses.

Final resolved version:

```python
import pandas as pd

data = pd.read_csv("sales.csv")

average_sales = data["sales"].mean()
max_sales = data["sales"].max()

print("Average Sales:", average_sales)
print("Maximum Sales:", max_sales)
```

The conflict markers must be removed.



# Mark Conflict as Resolved

Stage the file:

```bash
git add sales_analysis.py
```


# Complete the Merge

```bash
git commit
```

Git will create a merge commit.



# Workflow Summary

1. Two branches modify the same file
2. Git cannot merge automatically
3. Git marks the conflict in the file
4. Developer edits the file manually
5. Stage the file
6. Commit the merge

