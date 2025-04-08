# Chapter 4: Basic Git Workflow in Termux

Now that Git and GitHub are set up in Termux, let’s walk through a basic Git workflow.

---

## Step 1: Create a New Local Repository
```bash
mkdir myrepo
cd myrepo
git init
```
This initializes a new Git repo in the `myrepo` folder.

---

## Step 2: Add a File
```bash
echo "# My First Repo" > README.md
```

---

## Step 3: Stage the File
```bash
git add README.md
```

---

## Step 4: Commit the File
```bash
git commit -m "Initial commit"
```

---

## Step 5: Add Remote Repository
Go to GitHub and create a new repo. Then connect it:
```bash
git remote add origin git@github.com:yourusername/myrepo.git
```

---

## Step 6: Push to GitHub
```bash
git push -u origin master
```
*If your default branch is `main`, replace `master` with `main`.*

---

## Notes:
- Use `git status` to view file changes
- Use `git log` to view commit history

This completes your basic Git workflow from Termux!

---

# Chapter 5: Pushing & Managing Repositories from Termux

Now let's see how to manage changes and keep your GitHub repository updated using Termux.

---

## 1. Edit an Existing File
Use a terminal editor to change a file:
```bash
nano README.md
```
Make edits, save (`Ctrl + O`, `Enter`) and exit (`Ctrl + X`).

---

## 2. Add a New File
```bash
echo "This is a new tutorial file." > tutorial.txt
git add tutorial.txt
git commit -m "Added tutorial file"
git push
```

---

## 3. Update a File
After editing any tracked file:
```bash
git add <filename>
git commit -m "Updated content in <filename>"
git push
```

---

## 4. Delete a File
To remove a file from both local and remote:
```bash
git rm oldfile.txt
git commit -m "Removed unused file"
git push
```

---

## 5. Rename a File
```bash
git mv oldname.txt newname.txt
git commit -m "Renamed file"
git push
```

With these commands, you can fully manage your repository on the go!

---

# Chapter 6: Advanced Git Operations in Termux

For users who want more control over their workflow, here are some advanced Git commands.

---

## View Commit History
```bash
git log --oneline
```

---

## Undo Uncommitted Changes
```bash
git restore <filename>
```

---

## Undo the Last Commit (Keep Changes)
```bash
git reset --soft HEAD~1
```

---

## Set Up Git Aliases
```bash
git config --global alias.co checkout
git config --global alias.br branch
git config --global alias.cm commit
git config --global alias.st status
```
Use like:
```bash
git co main
```

---

## Tag a Release Version
```bash
git tag v1.0
git push origin v1.0
```

---

## Stash Uncommitted Work Temporarily
```bash
git stash
# Do something else
git stash pop
```

---

## Revert a Specific Commit
```bash
git revert <commit-id>
```

These tools give you more control and flexibility in your Git workflow using Termux.

---

# Chapter 7: Hosting and Collaborating on GitHub from Termux

In this chapter, you'll learn how to collaborate on open-source projects, sync forks, and host content using GitHub Pages — all from Termux.

---

## 1. Fork a Repository and Clone It
On GitHub, click the **Fork** button on any repo. Then clone your fork:
```bash
git clone git@github.com:yourusername/forked-repo.git
cd forked-repo
```

---

## 2. Create a New Branch
It's best to create a new branch for changes:
```bash
git checkout -b feature-branch
```

---

## 3. Make Your Changes
Edit or add files. Then:
```bash
git add .
git commit -m "Describe your changes"
git push origin feature-branch
```

---

## 4. Open a Pull Request
On GitHub, open your fork, and click **Compare & pull request**. Add a title and description, then submit.

---

## 5. Sync Your Fork with Original Repo
If the original project updates, sync your fork:
```bash
git remote add upstream https://github.com/original/repo.git
git fetch upstream
git checkout main
git merge upstream/main
git push origin main
```

---

## 6. Host a Website with GitHub Pages
You can host static sites directly from GitHub:

### Steps:
1. Create `index.html`
2. Push it to `gh-pages` branch:
```bash
git checkout -b gh-pages
git add index.html
git commit -m "Add homepage"
git push origin gh-pages
```

### Access URL:
```
https://yourusername.github.io/repo-name
```

---

GitHub + Termux is a powerful combo for open-source collaboration and even site hosting — right from your mobile device!
