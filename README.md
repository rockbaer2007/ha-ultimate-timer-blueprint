# ⏱️ Ultimate Timer V3

[![Open in Home Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https://raw.githubusercontent.com/rockbaer2007/ha-ultimate-timer-blueprint/main/blueprints/automation/ultimate_timer_v3.yaml)

![GitHub release](https://img.shields.io/github/v/release/rockbaer2007/ha-ultimate-timer-blueprint)
![GitHub stars](https://img.shields.io/github/stars/rockbaer2007/ha-ultimate-timer-blueprint?style=social)

> A powerful multi-instance timer blueprint for Home Assistant with watchdog functionality and flexible daily reset.

# ⏱️ Ultimate Timer V3 (Home Assistant Blueprint)

A powerful, reusable and multi-instance safe timer blueprint for Home Assistant.

Designed for real-world automation use cases like:
- Pool pumps
- Garden irrigation
- Pond systems
- Runtime limiting (watchdog)
- Delayed actions

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

1. Copy the blueprint YAML file
2. Place it into:
https://github.com/rockbaer2007/ha-ultimate-timer-blueprint

### Option 2: Import Blueprint

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


input_boolean.pool_timer_start
input_boolean.pool_timer_stop
input_boolean.pool_timer_running
input_boolean.pool_timer_done


---

## ⚙️ Configuration

When creating an automation from the blueprint:

| Field | Description |
|------|------------|
| Start Trigger | Button to start timer |
| Stop Trigger | Optional stop |
| Duration | hh:mm:ss |
| Running | Indicates active timer |
| Done | Set when finished |
| Reset Time | Daily reset (optional) |

---

## 🧠 How It Works

1. Start trigger → timer begins
2. Running state → ON
3. After duration → Done = ON
4. Daily reset → all OFF

---

## 💡 Example Use Case (Pond Pump Runtime Limit)

- Pump starts → trigger timer
- After 5 hours → system shuts down
- Reset next day automatically

---

## 🧩 Multi-Instance Support

You can create multiple independent timers:

- `pool_timer_*`
- `garden_timer_*`
- `pond_timer_*`

---

## 🛠️ Example

See `/examples/example_setup.yaml`

---

## 📜 License

MIT License

---

## 🤝 Contributing

Feel free to:
- open issues
- submit improvements
- suggest features

---

## ⭐ Support

If you like this project, give it a star ⭐

