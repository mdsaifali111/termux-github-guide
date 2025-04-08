# Chapter 3: Setting Up Git & GitHub in Termux

This chapter helps you configure Git in Termux and connect it securely to GitHub using SSH.

---

## Step 1: Install Git
Install Git using the package manager:
```bash
pkg install git
```

---

## Step 2: Configure Git Identity
Set your name and email to be used in commits:
```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

To check your config:
```bash
git config --list
```

---

## Step 3: Generate SSH Key
SSH is the most secure and recommended way to connect to GitHub.
```bash
ssh-keygen -t ed25519 -C "you@example.com"
```
- Press Enter to accept default file location.
- Set a passphrase (optional).

---

## Step 4: Copy Public SSH Key
```bash
cat ~/.ssh/id_ed25519.pub
```
Copy the full output.

---

## Step 5: Add Key to GitHub
1. Login to GitHub
2. Go to: **Settings > SSH and GPG Keys**
3. Click **New SSH Key**
4. Paste the copied key
5. Save

---

## Step 6: Test the Connection
```bash
ssh -T git@github.com
```
Expected output:
```
Hi your-username! You've successfully authenticated, but GitHub does not provide shell access.
```

Your Termux is now connected to GitHub via SSH. You're ready to push and pull from repos!
