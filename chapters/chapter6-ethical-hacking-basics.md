# Chapter 6: Ethical Hacking Basics — Nmap, Whois, Termux Tools

**📁 File Name:** `chapter6-ethical-hacking-basics.md`

---

## 🧠 Overview

This chapter introduces you to basic ethical hacking tools in Termux. These tools are used for information gathering, reconnaissance, and network scanning — the first step in penetration testing.

---

## 🔧 Tools Covered

* `nmap`
* `whois`
* Common Termux-based Hacking Tools

---

## 🔍 Step-by-Step Guide

### 1. 📥 Installing Required Packages

```bash
pkg update && pkg upgrade -y
pkg install nmap -y
pkg install whois -y
pkg install git -y
```

---

### 2. 🔎 Using `nmap` — Network Mapper

Nmap is used to discover hosts and services on a network.

**🖥️ Scan a single IP:**

```bash
nmap 192.168.1.1
```

**🌐 Scan a range of IPs:**

```bash
nmap 192.168.1.1-100
```

**📦 Scan for open ports and services:**

```bash
nmap -sV 192.168.1.1
```

**🔬 Aggressive Scan:**

```bash
nmap -A 192.168.1.1
```

---

### 3. 🌍 Using `whois` — Domain Information

**🧾 Example:**

```bash
whois example.com
```

This command gives details about the domain ownership, registrar, creation/expiry date, etc.

---

### 4. 🚀 Termux Ethical Hacking Tools (GitHub)

Here are some beginner-friendly tools you can clone and use:

#### a) **RED\_HAWK** — Information gathering tool

```bash
git clone https://github.com/Tuhinshubhra/RED_HAWK
cd RED_HAWK
php rhawk.php
```

#### b) **ReconDog** — All-in-one toolkit

```bash
git clone https://github.com/s0md3v/ReconDog
cd ReconDog
python recondog.py
```

#### c) **Hakku Framework** — Basic penetration testing tool

```bash
git clone https://github.com/4shadoww/hakkuframework.git
cd hakkuframework
chmod +x hakku
./hakku
```

---

## 🧑‍💻 Practice Tips

* Try scanning your local Wi-Fi router IP with nmap.
* Use `whois` on popular websites.
* Clone at least one GitHub tool and test its features.

---

## 🔐 Ethical Reminder

All these tools are for **educational** and **legal** use only. Do **not** scan or attack devices you don’t own or have permission to test.

---

## 📌 Next Up

Chapter 7: **Termux Automation Projects** → Scheduled Tasks, Auto SMS, Crontab Basics

---

✅ Save this file as: `chapter6-ethical-hacking-basics.md`
