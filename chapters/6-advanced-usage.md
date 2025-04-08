Chapter 6: Advanced Git Operations in Termux

Once you're comfortable with the basics, it's time to explore some advanced Git commands that enhance your workflow directly from Termux.


---

1. Viewing Commit History (Detailed)

git log

Shows full commit messages, authors, and timestamps.

To see a simplified version:

git log --oneline


---

2. Undoing Local Changes

To discard changes made to a file:

git checkout -- filename.txt


---

3. Undo Last Commit (Keep Changes)

If you want to undo your last commit but keep the changes staged:

git reset --soft HEAD~1

To undo commit and unstage changes:

git reset --mixed HEAD~1

To undo everything (even local file changes):

git reset --hard HEAD~1


---

4. Creating Aliases for Common Commands

Make your work faster by using aliases:

git config --global alias.co checkout
git config --global alias.br branch
git config --global alias.cm "commit -m"

Now you can use:

git co main
git br
git cm "Updated files"


---

5. Tagging Releases

Create a tag for a version release:

git tag v1.0
git push origin v1.0


---

6. Stashing Uncommitted Work

Temporarily save your uncommitted changes:

git stash

To re-apply them later:

git stash pop


---

7. Reverting a Specific Commit

Undo a previous commit without changing commit history:

git revert <commit-id>

Get the <commit-id> using:

git log --oneline


---

Mastering these commands will help you maintain clean, efficient, and professional repositories using Termux on the go!

