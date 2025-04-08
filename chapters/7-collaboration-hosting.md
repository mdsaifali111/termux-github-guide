Chapter 7: Hosting and Collaborating on GitHub from Termux

In this final chapter, you’ll learn how to collaborate on GitHub and host projects like websites directly from your Termux terminal.


---

1. Forking a Repository

If you want to contribute to someone else's project:

Go to the repository on GitHub.

Click Fork to create a copy under your account.


Clone your fork using SSH:

git clone git@github.com:yourusername/forked-repo.git
cd forked-repo


---

2. Creating a New Branch

Working on a new feature or bugfix? Create a new branch:

git checkout -b new-feature

After making changes:

git add .
git commit -m "Added new feature"
git push origin new-feature

Open GitHub and create a Pull Request to propose your changes.


---

3. Syncing Your Fork with Upstream Repository

If the original repo gets updated, sync your fork:

git remote add upstream https://github.com/original/repo.git
git fetch upstream
git checkout main
git merge upstream/main
git push origin main


---

4. Hosting with GitHub Pages

If you have HTML files, you can host them with GitHub Pages:

Switch to a branch named gh-pages:


git checkout --orphan gh-pages
git rm -rf .
echo "<h1>My Site</h1>" > index.html
git add index.html
git commit -m "Initial GitHub Pages site"
git push origin gh-pages

Visit your website at:

https://yourusername.github.io/repo


---

5. Collaborating in Teams

If you’re working in teams:

Add collaborators under the GitHub repo settings.

Use git pull frequently to stay updated.

Use branches and pull requests to manage contributions.



---

Now you’re ready to fully contribute, collaborate, and host projects with GitHub — all from your Android device using Termux. Congratulations on completing the guide!

