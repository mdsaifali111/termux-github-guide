Termux + GitHub: Complete Guide

A beginner-friendly, mobile-first Git + GitHub workflow powered entirely via Termux on Android. This guide walks you through GitHub concepts and practical use in 7 easy chapters.

Table of Contents

1. Introduction to Termux


2. Introduction to GitHub


3. Setting Up Git & GitHub in Termux


4. Basic Git Workflow in Termux


5. Pushing & Managing Repositories from Termux


6. Advanced Git Operations in Termux


7. Hosting & Collaborating on GitHub via Termux



Chapter 1: Introduction to Termux

Termux is a terminal emulator and Linux environment app for Android. It allows you to:

Run full Linux command-line utilities

Use apt package manager

Install Git, Python, Node.js, and more

Perform real development work on your mobile device


Installation

pkg update && pkg upgrade
pkg install git nano curl wget

Chapter 2: Introduction to GitHub

GitHub is a web-based platform for version control using Git. With GitHub, you can:

Host repositories online

Collaborate with others

Track changes and issues

Contribute to open-source


You’ll interact with GitHub using git commands via Termux.

Chapter 3: Setting Up Git & GitHub in Termux

1. Install Git

pkg install git

2. Configure Git

git config --global user.name "Your Name"
git config --global user.email "you@example.com"

3. Generate SSH Key

ssh-keygen -t ed25519 -C "you@example.com"

Copy your public key:

cat ~/.ssh/id_ed25519.pub

Add it to GitHub:

Go to Settings → SSH & GPG Keys → New SSH Key

Paste the key and save


4. Test SSH Connection

ssh -T git@github.com

Chapter 4: Basic Git Workflow in Termux

1. Create New Repo

mkdir myrepo
cd myrepo
git init

2. Add Files & Commit

echo "# My Repo" > README.md
git add .
git commit -m "Initial commit"

3. Push to GitHub

git remote add origin git@github.com:username/repo.git
git push -u origin master

Chapter 5: Pushing & Managing Repositories from Termux

1. Edit Existing File

nano README.md

Update content, save changes.

2. Add New File

echo "My new content" > tutorial.txt
git add tutorial.txt
git commit -m "Added tutorial file"
git push

3. Delete File

git rm oldfile.txt
git commit -m "Removed unused file"
git push

Chapter 6: Advanced Git Operations in Termux

View logs:

git log --oneline

Undo changes:

git checkout -- filename

Undo commit:

git reset --soft HEAD~1

Set aliases:

git config --global alias.co checkout

Tag a release:

git tag v1.0 && git push origin v1.0

Stash work:

git stash && git stash pop

Revert commit:

git revert <commit>


Chapter 7: Hosting and Collaborating on GitHub from Termux

Fork a repo and clone

git clone git@github.com:you/forked-repo.git

Create new branch

git checkout -b new-feature

Push and open pull request

Sync fork with upstream

git remote add upstream https://github.com/original/repo.git
git fetch upstream
git checkout main
git merge upstream/main
git push origin main

Host websites with GitHub Pages

Push to gh-pages branch

URL: https://yourusername.github.io/repo


Thanks for Reading!

This guide is 100% mobile-optimized. Clone, edit, and commit code anytime — from your Android phone using Termux.

Happy Hacking!

