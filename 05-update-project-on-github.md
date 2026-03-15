# Update Files on GitHub

After uploading a project to GitHub, you may need to update files.  
Git allows developers to modify files and upload the updated version.

---

## Step 1: Make Changes in Your Project

Open your project in your code editor.

Example changes:
- Fix a bug
- Add new features
- Update documentation

Example: Edit the file `README.md`.

---

## Step 2: Check Repository Status

After making changes, check the status.

```bash
git status
```
Git will show which files have been modified.

Example output:

```modified: README.md```

### Step 3: Add Modified Files

Add the updated files to the staging area.

```bash
git add .
```

You can also add a specific file:

```bash
git add README.md
```

## Step 4: Commit the Changes

Save the changes in Git history.

```bash
git commit -m "Updated README documentation"
```

A commit message should describe what changes were made.

## Step 5: Push Changes to GitHub

Upload the changes to GitHub.

```bash
git push
```
The updated files will now appear on GitHub.

## Example Workflow

Typical workflow when updating a project:

1. Edit file
2. Check status
3. Add changes
4. Commit changes
5. Push to GitHub