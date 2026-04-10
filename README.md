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
