# ⏱️ Ultimate Timer V3

[![Open in Home Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https://raw.githubusercontent.com/rockbaer2007/ha-ultimate-timer-blueprint/main/blueprints/automation/ultimate_timer_v3.yaml)

![GitHub release](https://img.shields.io/github/v/release/rockbaer2007/ha-ultimate-timer-blueprint)
![GitHub stars](https://img.shields.io/github/stars/rockbaer2007/ha-ultimate-timer-blueprint?style=social)

> A powerful multi-instance timer blueprint for Home Assistant with watchdog functionality and flexible daily reset.

---

## 🚀 Features

- ⏱️ Timer with `hh:mm:ss` format  
- ▶️ Start trigger (button style)  
- ⏹️ Optional stop trigger  
- 📡 Running state indicator  
- 🎯 Completion state output  
- 🌙 Configurable daily reset time  
- 🔁 Multi-instance safe  
- 🛡️ Race condition safe  
- 🔄 Restart-safe (`mode: restart`)  

---

## 📦 Installation

### Option 1: Manual

1. Download the blueprint file  
2. Copy it to your Home Assistant config directory:
   config/blueprints/automation/


3. Reload blueprints in Home Assistant  

---

### Option 2: Import Blueprint (recommended)

Click the button below to import the blueprint directly into Home Assistant:

[![Open in Home Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https://raw.githubusercontent.com/rockbaer2007/ha-ultimate-timer-blueprint/main/blueprints/automation/ultimate_timer_v3.yaml)

Or paste this URL manually:
https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https://raw.githubusercontent.com/rockbaer2007/ha-ultimate-timer-blueprint/main/blueprints/automation/ultimate_timer_v3.yaml


---

## 🔧 Required Helpers

Create the following `input_boolean` helpers:

- Start trigger  
- Stop trigger (optional)  
- Running state  
- Done state  

Example:

```yaml
input_boolean:
  pool_timer_start:
  pool_timer_stop:
  pool_timer_running:
  pool_timer_done:

| Field         | Description            |
| ------------- | ---------------------- |
| Start Trigger | Button to start timer  |
| Stop Trigger  | Optional stop          |
| Duration      | hh:mm:ss               |
| Running       | Indicates active timer |
| Done          | Set when finished      |
| Reset Time    | Daily reset (optional) |

...yaml

   
