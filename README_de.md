# ⏱️ Ultimate Timer V3.2.2 FINAL

[![Open in Home Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https://raw.githubusercontent.com/rockbaer2007/ha-ultimate-timer-blueprint/main/blueprints/automation/ultimate_timer_v3_2_2.yaml)

![GitHub release](https://img.shields.io/github/v/release/rockbaer2007/ha-ultimate-timer-blueprint)
![GitHub stars](https://img.shields.io/github/stars/rockbaer2007/ha-ultimate-timer-blueprint?style=social)

🇬🇧 [English Version](README.md)

> Leistungsstarker Hybrid-Timer für Home Assistant mit zuverlässiger STOP-Logik und MQTT Unterstützung.

---

## 🚀 Features

- ⏱️ Timer im Format `hh:mm:ss`  
- ▶️ Start-Trigger (Taster)  
- ⏹️ STOP funktioniert zuverlässig  
- 📡 Running Status  
- 🎯 Done Status  
- 🌙 täglicher Reset  
- 🔁 Multi-Instance fähig  
- 🔀 Helper oder MQTT  
- 🛡️ keine Race Conditions  

---

## 🔄 Update Hinweis

### V3.2 → V3.2.2 FINAL

Ein kritischer Fehler wurde behoben:

- ❌ Running blieb nach STOP aktiv  
- ✅ Jetzt immer korrekt AUS  

👉 Update wird dringend empfohlen

---

## 📦 Installation

### Manuell

```
config/blueprints/automation/
```

---

### Direkt importieren

[![Open in Home Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https://raw.githubusercontent.com/rockbaer2007/ha-ultimate-timer-blueprint/main/blueprints/automation/ultimate_timer_v3_2_2.yaml)

---

## ⚙️ Konfiguration

| Feld | Beschreibung |
|------|------------|
| Start | Timer starten |
| Stop | Timer stoppen |
| Dauer | hh:mm:ss |
| Running | Aktiv |
| Done | Fertig |
| Reset | täglich |

---

## 🧠 Funktionsweise

1. Start → Timer läuft  
2. Running → EIN  
3. Stop → sofort AUS  
4. Ablauf → Done = EIN  
5. Reset → alles AUS  

---

## 💡 Einsatz

- Teich / Pool Pumpen  
- Bewässerung  
- Watchdog  
- Verzögerungen  

---

## 📸 Vorschau

![Preview](docs/preview.png)

---

## 📜 Lizenz

MIT Lizenz

---

## ⭐ Support

Wenn dir das Projekt gefällt, gib ihm ein ⭐
