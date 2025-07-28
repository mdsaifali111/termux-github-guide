# 📘 Chapter 2: Basic Linux Commands (Termux)

This chapter covers essential Linux commands that you'll frequently use in Termux for file navigation, management, and basic package operations.

---

## 📂 File & Folder Navigation Commands

| Command       | Description                                                     |
| ------------- | --------------------------------------------------------------- |
| `pwd`         | Print the current working directory                             |
| `ls`          | List files and folders in the current directory                 |
| `ls -la`      | List all files with detailed information including hidden files |
| `cd <folder>` | Change directory to the specified folder                        |
| `cd ..`       | Go back one directory level                                     |
| `clear`       | Clear the terminal screen                                       |

---

## 📁 File & Folder Operations

| Command                     | Description                                  |
| --------------------------- | -------------------------------------------- |
| `mkdir <folder>`            | Create a new folder                          |
| `touch <file>`              | Create a new empty file                      |
| `cp <source> <destination>` | Copy file or folder                          |
| `mv <source> <destination>` | Move or rename file/folder                   |
| `rm <file>`                 | Delete a file                                |
| `rm -rf <folder>`           | Delete a folder and its contents recursively |
| `cat <file>`                | View contents of a file                      |
| `nano <file>`               | Edit a file in terminal text editor          |
| `exit`                      | Exit Termux session                          |

---

## 📦 Package Management (Using `pkg`)

| Command                   | Description                    |
| ------------------------- | ------------------------------ |
| `pkg update`              | Update Termux package list     |
| `pkg upgrade`             | Upgrade all installed packages |
| `pkg install <package>`   | Install a specific package     |
| `pkg uninstall <package>` | Uninstall a package            |
| `pkg list-installed`      | List all installed packages    |
| `pkg search <package>`    | Search for a package           |

---

## 🔐 User & Permissions (Basic Awareness)

| Command           | Description                        |
| ----------------- | ---------------------------------- |
| `whoami`          | Show current user                  |
| `id`              | Show user ID and group information |
| `chmod +x <file>` | Make a script or file executable   |

---

## 📎 Useful Tips

* Always keep Termux updated using:

```bash
pkg update && pkg upgrade -y
```

* Combine commands using `&&` to run them in sequence.

```bash
pkg update && pkg upgrade && pkg install git
```

---

✅ **Next Chapter:** Git + GitHub Advanced
