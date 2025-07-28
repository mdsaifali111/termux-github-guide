# Chapter 9: Real Tools Projects — YouTube Downloader, Instagram Info Tool, ZIP Bruteforce Demo

---

## 📁 File: `9-real-tools-projects.md`

Welcome to the final chapter of your Termux Mastery Guide! In this chapter, you'll learn how to build some practical tools that use real-world APIs, scraping, and basic automation.

---

## 🎯 Goals

* Learn to create terminal-based tools.
* Understand API usage and automation in Termux.
* Practice scripting with practical examples.

---

## 🔧 Project 1: YouTube Downloader (Using `yt-dlp`)

### 🔹 Step 1: Install `yt-dlp`

```bash
pkg update && pkg upgrade
pkg install python ffmpeg -y
pip install yt-dlp
```

### 🔹 Step 2: Download a Video

```bash
yt-dlp "https://www.youtube.com/watch?v=YOUR_VIDEO_ID"
```

### 🔹 Optional: Download as MP3

```bash
yt-dlp -x --audio-format mp3 "https://www.youtube.com/watch?v=YOUR_VIDEO_ID"
```

---

## 🔍 Project 2: Instagram Info Tool (Without Login)

### 🔹 Step 1: Install Required Packages

```bash
pkg install python
pip install requests bs4
```

### 🔹 Step 2: Create Script

```bash
touch insta-info.py && nano insta-info.py
```

Paste this code:

```python
import requests
from bs4 import BeautifulSoup

username = input("Enter Instagram username: ")
url = f"https://www.instagram.com/{username}/"
headers = {"User-Agent": "Mozilla/5.0"}

r = requests.get(url, headers=headers)
soup = BeautifulSoup(r.text, "html.parser")

info = soup.find("meta", property="og:description")
if info:
    print("\n🔎 Info:", info["content"])
else:
    print("❌ Couldn't fetch info.")
```

### 🔹 Run It

```bash
python insta-info.py
```

---

## 🔓 Project 3: ZIP Password Brute Force (For Educational Purposes)

### ⚠️ Use only on your own test files. This is for ethical learning only.

### 🔹 Step 1: Install Tool

```bash
pkg install python unzip -y
pip install zipfile36
```

### 🔹 Step 2: Create Script

```bash
touch zip-cracker.py && nano zip-cracker.py
```

Paste this code:

```python
import zipfile

zip_file = "secret.zip"
wordlist = "wordlist.txt"

with open(wordlist, "r") as f:
    for line in f:
        pwd = line.strip()
        try:
            with zipfile.ZipFile(zip_file) as zf:
                zf.extractall(pwd=pwd.encode())
                print("✅ Password Found:", pwd)
                break
        except:
            print("❌ Trying:", pwd)
```

### 🔹 Run the Brute Force

```bash
python zip-cracker.py
```

---

## ✅ Recap

In this chapter, you’ve built:

* A YouTube downloader using `yt-dlp`
* An Instagram info scraper using `requests` and `bs4`
* A ZIP password brute-force script

These projects combine multiple skills: scripting, automation, and tool building.

---

✅ **Next Suggestion:** Build a GitHub-hosted Termux Tools Collection!

📁 File Saved As: `9-real-tools-projects.md`

---

🔗 Previous Chapters:

* [Chapter 8: API & Bot Projects](./8-api-bot-projects.md)
* [Chapter 7: Termux Automation Projects](./7-termux-automation.md)
* [...see all in your GitHub repo](./README.md)

---

🎉 Congratulations! You’ve completed your Termux Guide. Now you can update, style, or publish it on GitHub Pages or use `.me` domain to teach others!

**👨‍💻 Developer:** [CodeSaif](https://t.me/codesaif_group)
