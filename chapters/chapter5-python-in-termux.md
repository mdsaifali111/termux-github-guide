# 📘 Chapter 5: Python in Termux

**Filename:** `chapter5-python-in-termux.md`

## 🐍 Introduction

Python is a versatile and beginner-friendly programming language. Using Python in Termux allows you to automate tasks, run scripts, and even build small projects directly on your mobile device.

---

## 📥 Install Python in Termux

Run the following command to install Python:

```bash
pkg update && pkg upgrade -y
pkg install python -y
```

To check if Python is installed:

```bash
python --version
```

You should see output like:

```
Python 3.x.x
```

---

## 🧪 Run Python Shell

Simply type:

```bash
python
```

You will enter the Python interactive shell where you can run Python commands.

To exit the shell:

```python
exit()
```

---

## 💾 Create and Run Python Script

1. Create a Python script file:

```bash
touch hello.py
```

2. Edit the file using nano or any text editor:

```bash
nano hello.py
```

3. Add sample code:

```python
print("Hello from Termux!")
```

4. Save and exit nano (Press `CTRL + X`, then `Y`, then `Enter`)

5. Run the script:

```bash
python hello.py
```

You should see:

```
Hello from Termux!
```

---

## 📦 Install Python Packages

You can install third-party Python packages using `pip` (Python’s package manager):

```bash
pip install requests
```

Example usage:

```python
import requests
res = requests.get("https://api.github.com")
print(res.json())
```

---

## 🔧 Create Simple Python Project

### Project: Random Quote Generator

1. Create file:

```bash
nano quote.py
```

2. Paste this code:

```python
import random
quotes = [
  "Be yourself; everyone else is already taken.",
  "So many books, so little time.",
  "You only live once, but if you do it right, once is enough."
]
print(random.choice(quotes))
```

3. Save and run:

```bash
python quote.py
```

---

## ✅ Summary

| Command                 | Purpose                |
| ----------------------- | ---------------------- |
| `pkg install python`    | Install Python         |
| `python`                | Start Python shell     |
| `python file.py`        | Run Python script      |
| `pip install <package>` | Install Python package |

---

Next → `chapter6-git-in-termux.md`

⬅️ Previous → `chapter4-shell-tools-utilities.md`
