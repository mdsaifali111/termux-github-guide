# Chapter 8: API & Bot Projects

In this chapter, we’ll explore how to use APIs and bots with Termux to create useful tools like Telegram bots, IP finders, and weather fetchers. These mini-projects will boost your practical skills and can be part of real-world automation.

---

## 📌 Overview

* **Goal**: Learn how to use APIs and create bots in Termux.
* **Projects Covered**:

  * Telegram bot integration
  * IP Finder tool using IP API
  * Weather fetcher using Weather APIs

---

## 1. Telegram Bot with Termux

### 🛠️ Prerequisites

* A Telegram account
* BotFather (Telegram bot to create bots)
* Python installed in Termux (`pkg install python`)
* `python-telegram-bot` library (`pip install python-telegram-bot`)

### 🔧 Create a Bot

1. Search **BotFather** on Telegram.
2. Use `/newbot` to create your bot.
3. Save the token it gives you.

### 🧠 Simple Python Bot Code

```python
from telegram.ext import Updater, CommandHandler

def start(update, context):
    update.message.reply_text("Hello! I’m your Termux bot.")

def main():
    updater = Updater("<YOUR_BOT_TOKEN>", use_context=True)
    dp = updater.dispatcher
    dp.add_handler(CommandHandler("start", start))
    updater.start_polling()
    updater.idle()

if __name__ == '__main__':
    main()
```

### ▶️ Run the bot

```bash
python bot.py
```

---

## 2. IP Finder using API

### 🧰 Tools Required

* Python
* Requests module (`pip install requests`)

### 🌐 Code Example

```python
import requests
ip = input("Enter IP Address: ")
res = requests.get(f"https://ipinfo.io/{ip}/json")
data = res.json()
for key, value in data.items():
    print(f"{key}: {value}")
```

### ✅ Run it

```bash
python ip_finder.py
```

---

## 3. Weather Fetcher using API

### 🔗 API Used: [OpenWeatherMap](https://openweathermap.org/api)

* Get your free API key by registering.

### 🌦️ Python Code

```python
import requests

city = input("Enter city: ")
api_key = "<YOUR_API_KEY>"
url = f"https://api.openweathermap.org/data/2.5/weather?q={city}&appid={api_key}&units=metric"

res = requests.get(url)
data = res.json()
if data.get('main'):
    print(f"Temp: {data['main']['temp']}°C")
    print(f"Weather: {data['weather'][0]['description']}")
else:
    print("City not found!")
```

### ▶️ Run it

```bash
python weather.py
```

---

## 🔚 Summary

* You now know how to:

  * Build a Telegram bot
  * Fetch IP location info
  * Get live weather using APIs

These small tools are great for automation and can be extended for advanced features.

---

📁 **File Name:** `8-api-bot-projects.md`
