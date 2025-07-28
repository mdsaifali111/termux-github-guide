# Chapter 7: Termux Automation Projects

📁 **Filename:** `7-termux-automation.md`

## 🎯 Overview

Learn how to automate tasks using Termux with tools like `crontab`, `termux-job-scheduler`, and auto-scripting techniques. This chapter helps you build simple automation projects such as scheduled SMS sending, periodic system scans, backups, and notifications.

---

## 📚 Table of Contents

1. Introduction to Automation in Termux
2. Installing Required Packages
3. Scheduling with Crontab
4. Using `termux-job-scheduler`
5. Automating SMS Sending
6. Scheduling Scripts
7. Auto-Backup Example
8. Security Notes
9. Practice Projects

---

## 1️⃣ Introduction to Automation in Termux

Termux supports many Linux utilities, which means you can use automation tools like `cron`, `at`, or `termux-job-scheduler` to run scripts or commands at scheduled times.

## 2️⃣ Install Required Packages

```bash
pkg update && pkg upgrade
pkg install termux-api
pkg install cronie
pkg install nano
```

Enable cron:

```bash
mkdir -p ~/.termux/boot
crond
```

## 3️⃣ Setup Crontab Scheduler

Use crontab to schedule tasks:

```bash
crontab -e
```

Example to run a script every day at 8 AM:

```bash
0 8 * * * bash ~/scripts/daily-task.sh
```

## 4️⃣ Using `termux-job-scheduler`

You can automate with this Termux-specific tool too.

```bash
termux-job-scheduler -s ~/scripts/mytask.sh -p -n 1 -t 60000
```

Flags:

* `-s`: script file
* `-p`: persist after boot
* `-n`: unique job ID
* `-t`: interval in ms

## 5️⃣ Automate SMS Sending

Install SMS plugin:

```bash
termux-sms-send -n 9876543210 'Hello! This is a scheduled message.'
```

Create a script:

```bash
nano ~/scripts/sms.sh
```

```bash
#!/bin/bash
date=$(date)
echo "Sending SMS at $date" >> ~/logs/sms.log
termux-sms-send -n 9876543210 "Scheduled message sent at $date"
```

Make it executable:

```bash
chmod +x ~/scripts/sms.sh
```

## 6️⃣ Schedule Your Script with Cron

```bash
crontab -e
```

Add:

```bash
0 12 * * * bash ~/scripts/sms.sh
```

This will send the message every day at noon.

## 7️⃣ Auto-Backup Example

```bash
nano ~/scripts/backup.sh
```

```bash
#!/bin/bash
tar -czvf ~/backups/home-$(date +%F).tar.gz ~/
```

Make it executable:

```bash
chmod +x ~/scripts/backup.sh
```

Schedule it:

```bash
crontab -e
```

Add:

```bash
30 2 * * * bash ~/scripts/backup.sh
```

## 8️⃣ Security Tips

* Don’t expose automation scripts with sensitive data.
* Use Termux storage permission properly.
* Protect SMS-related scripts from abuse.

## 9️⃣ Practice Projects

* ✅ Daily wallpaper change script
* ✅ Automatic notes sync to cloud
* ✅ Daily motivational message via SMS

---

## 🔗 Useful Commands Summary

```bash
crontab -e            # Edit cron jobs
crond                 # Start cron daemon
termux-job-scheduler  # Schedule jobs with Termux API
termux-sms-send       # Send SMS from Termux
```

---

🧠 **Next Chapter:** Network Scanning Projects → [View Chapter 8](8-network-scanning-projects.md)
