# 📘 Chapter 4: Git & GitHub in Termux

> 📁 File Name: `04_git_github_termux.md`

## 📌 Introduction

Git is a version control system, and GitHub is a remote platform to host and manage code repositories. Learning to use Git in Termux allows you to manage your coding projects and collaborate with others.

---

## 🧰 Git Installation in Termux

```bash
pkg update && pkg upgrade
pkg install git -y
```

---

## ⚙️ Git Configuration

Replace with your actual GitHub username and email.

```bash
git config --global user.name "YourName"
git config --global user.email "youremail@example.com"
```

Check configuration:

```bash
git config --list
```

---

## 🔄 Git Basic Commands

| Command                       | Description                             |
| ----------------------------- | --------------------------------------- |
| `git init`                    | Initialize a new Git repository         |
| `git status`                  | Show current repo status                |
| `git add <file>`              | Add specific file to staging area       |
| `git add .`                   | Add all files to staging area           |
| `git commit -m "message"`     | Commit changes with a message           |
| `git log`                     | View commit history                     |
| `git remote add origin <url>` | Link local repo with remote GitHub repo |
| `git push -u origin main`     | Push code to GitHub (first time)        |
| `git pull`                    | Fetch and merge changes from GitHub     |

---

## 🔗 Cloning a GitHub Repository

```bash
git clone https://github.com/mdsaifali111/termux-github-guide.git
cd termux-github-guide
ls
```

---

## 📝 Creating New Repo and Push from Termux

1. Create a new folder:

```bash
mkdir myproject && cd myproject
```

2. Initialize Git:

```bash
git init
```

3. Add and commit files:

```bash
echo "# My Project" >> README.md
git add .
git commit -m "initial commit"
```

4. Connect to GitHub repo:

```bash
git remote add origin https://github.com/yourusername/myproject.git
git branch -M main
git push -u origin main
```

---

## ✅ Summary

* Install Git in Termux
* Configure GitHub credentials
* Learn basic Git commands
* Push/pull your code from GitHub using Termux

Next: `05_advanced_git_operations.md` ➡️
