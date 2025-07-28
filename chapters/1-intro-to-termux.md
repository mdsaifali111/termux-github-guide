# 📘 Chapter 1: Introduction to Termux + GitHub Integration

Welcome to the **CodeSaif Termux GitHub Integration Guide** — a beginner-friendly guide to help you learn how to use Termux with GitHub for downloading and uploading code.

---

## 🚀 What You’ll Learn

* Basic Linux & GitHub commands in Termux
* How to clone GitHub repositories
* How to push your own code to GitHub

---

## ✅ Requirements

| Requirement        | Description                                          |
| ------------------ | ---------------------------------------------------- |
| 📱 Android Phone   | With Termux App Installed                            |
| 🌐 Internet        | Stable Internet Connection                           |
| 💻 GitHub Account  | Signup at [GitHub](https://github.com/signup)        |
| 🔧 Basic Knowledge | Very basic command-line knowledge (we’ll guide you!) |

---

## 📂 Folder Navigation Basics

Use these commands to move around in the Termux file system:

| Command           | Purpose                     |
| ----------------- | --------------------------- |
| `ls`              | List files in a directory   |
| `cd`              | Change directory            |
| `cd ..`           | Move up one level           |
| `mkdir <folder>`  | Make a new folder           |
| `rm -rf <folder>` | Delete a folder recursively |

---

## 🔗 GitHub Account Setup (Required)

Create a GitHub account: [https://github.com/signup](https://github.com/signup)

Then install Git inside Termux:

```bash
pkg update && pkg upgrade -y
pkg install git -y
```

Configure Git with your GitHub credentials:

```bash
git config --global user.name "YourName"
git config --global user.email "youremail@example.com"
```

---

## ⚙️ Test Git Clone

Let’s try cloning a public GitHub repository:

```bash
git clone https://github.com/mdsaifali111/termux-github-guide.git
cd termux-github-guide
ls
```

You should see the contents of the repo printed in the terminal.

---

✅ **You’ve successfully completed Chapter 1!**

In the next chapter, we’ll guide you on how to upload (push) your own code to GitHub using Termux.

---

📌 **Join our community:** [t.me/codesaif\_group](https://t.me/codesaif_group)

🛠️ **Made by:** [CodeSaif](https://github.com/mdsaifali111)
