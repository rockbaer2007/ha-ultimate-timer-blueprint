# ⏱️ Ultimate Timer V3.2.2 FINAL

[![Open in Home Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https://raw.githubusercontent.com/rockbaer2007/ha-ultimate-timer-blueprint/main/blueprints/automation/ultimate_timer_v3_2_2.yaml)

![GitHub release](https://img.shields.io/github/v/release/rockbaer2007/ha-ultimate-timer-blueprint)
![GitHub stars](https://img.shields.io/github/stars/rockbaer2007/ha-ultimate-timer-blueprint?style=social)
![HACS](https://img.shields.io/badge/HACS-Custom-blue)

🇩🇪 [German Version](README_de.md)

> A powerful hybrid timer blueprint for Home Assistant with reliable STOP handling and MQTT support.

---

## 🚀 Features

- ⏱️ Timer with `hh:mm:ss` format  
- ▶️ Start trigger (button behavior)  
- ⏹️ Reliable stop trigger (instant OFF)  
- 📡 Running state indicator  
- 🎯 Done state output  
- 🌙 Daily reset time  
- 🔁 Multi-instance safe  
- 🔀 Hybrid mode (Helper or MQTT)  
- 🛡️ No race conditions (parallel mode)  

---

## 🔄 Upgrade Notice

### V3.2 → V3.2.2 FINAL

A critical issue has been fixed:

- ❌ Running could remain ON after STOP  
- ✅ Now always turns OFF correctly  

👉 Strongly recommended to update

---

## 📦 Installation

### Option 1: Manual

Copy to:

```
config/blueprints/automation/
```

---

### Option 2: Import

[![Open in Home Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https://raw.githubusercontent.com/rockbaer2007/ha-ultimate-timer-blueprint/main/blueprints/automation/ultimate_timer_v3_2_2.yaml)

---

## ⚙️ Configuration

| Field | Description |
|------|------------|
| Start Trigger | Starts timer |
| Stop Trigger | Stops timer |
| Duration | hh:mm:ss |
| Running | Active state |
| Done | Finished state |
| Reset Time | Daily reset |

---

## 🧠 How It Works

1. Start → Timer starts  
2. Running → ON  
3. Stop → Running OFF immediately  
4. Timeout → Done = ON  
5. Reset → everything OFF  

---

## 💡 Use Cases

- Pump runtime limiter  
- Irrigation  
- Watchdog automation  
- Delayed shutdown  

---

## 📸 Preview

![Preview](docs/preview.png)

---

## 📜 License

MIT License

---

## ⭐ Support

If you like this project, give it a star ⭐
