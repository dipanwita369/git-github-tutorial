# Install Git

Git must be installed on your computer before using version control.

---

## Check if Git is Already Installed

Open terminal or command prompt and run:

```bash
git --version

## Configure Git (First Time Setup)

After installing Git, you need to configure your username and email.  
This information is attached to every commit you make.

### Set Username and Email

```bash
git config --global user.name "Your Name"
git config --global user.email "your_email@example.com"

**Check Configuration**

```bash
git config --list