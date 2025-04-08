Chapter 5: Pushing & Managing Repositories from Termux

In this chapter, you'll learn how to effectively manage your GitHub repositories using Termux — including pushing updates, editing files, and removing unwanted ones.


---

1. Editing an Existing File

Use a text editor like nano to edit any file.

nano README.md

Make your changes, save with Ctrl + X, then Y, then Enter.

Stage and commit the update:

git add README.md
git commit -m "Updated README with more details"
git push


---

2. Adding a New File

Create a new file:

echo "My new tutorial content" > tutorial.txt

Stage and push it:

git add tutorial.txt
git commit -m "Added tutorial file"
git push


---

3. Deleting a File from the Repository

To delete a file, use:

git rm filename.txt

Then commit and push:

git commit -m "Removed unused file"
git push

Example:

git rm cheatsheet.ps
git commit -m "Deleted old cheatsheet.ps file"
git push


---

4. Checking Repository Status

To see which files are modified, added, or deleted:

git status

This helps you track what changes need to be committed or ignored.


---

5. View Commit History

To see the log of changes:

git log --oneline

This shows short commit messages and helps track your repo history.


---

You now know how to manage your repositories efficiently from your Android phone using Termux!

