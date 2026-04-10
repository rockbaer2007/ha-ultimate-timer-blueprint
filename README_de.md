# ⏱️ Ultimate Timer V3

[![Open in Home Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https://raw.githubusercontent.com/rockbaer2007/ha-ultimate-timer-blueprint/main/blueprints/automation/ultimate_timer_v3.yaml)

![GitHub release](https://img.shields.io/github/v/release/rockbaer2007/ha-ultimate-timer-blueprint)
![GitHub stars](https://img.shields.io/github/stars/rockbaer2007/ha-ultimate-timer-blueprint?style=social)

> Ein leistungsstarker, multi-instanzfähiger Timer-Blueprint für Home Assistant mit Watchdog-Funktion und flexibel einstellbarem Tages-Reset.

---

## 🚀 Features

- ⏱️ Timer mit `hh:mm:ss` Format  
- ▶️ Start-Trigger (Taster-Prinzip)  
- ⏹️ Optionaler Stop-Trigger  
- 📡 Statusanzeige „läuft“  
- 🎯 Ergebnis-Status nach Ablauf  
- 🌙 Konfigurierbare tägliche Reset-Zeit  
- 🔁 Multi-Instance fähig  
- 🛡️ Schutz vor Race Conditions  
- 🔄 Restart-sicher (`mode: restart`)  

---

## 📦 Installation

### Option 1: Manuell

1. Blueprint-Datei herunterladen  
2. In dein Home Assistant Verzeichnis kopieren:

```
config/blueprints/automation/
```

3. Blueprints in Home Assistant neu laden  

---

### Option 2: Direkt importieren (empfohlen)

Klicke auf den Button, um den Blueprint direkt zu importieren:

[![Open in Home Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https://raw.githubusercontent.com/rockbaer2007/ha-ultimate-timer-blueprint/main/blueprints/automation/ultimate_timer_v3.yaml)

Oder diesen Link manuell einfügen:

```
https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https://raw.githubusercontent.com/rockbaer2007/ha-ultimate-timer-blueprint/main/blueprints/automation/ultimate_timer_v3.yaml
```

---

## 🔧 Benötigte Helper

Erstelle folgende `input_boolean` Helper:

- Start Trigger  
- Stop Trigger (optional)  
- Running Status  
- Done Status  

### Beispiel:

```yaml
input_boolean:
  pool_timer_start:
  pool_timer_stop:
  pool_timer_running:
  pool_timer_done:
```

---

## ⚙️ Konfiguration

Beim Erstellen einer Automation aus dem Blueprint:

| Feld | Beschreibung |
|------|------------|
| Start Trigger | Startet den Timer |
| Stop Trigger | Optionaler Stop |
| Dauer | hh:mm:ss |
| Running | Zeigt laufenden Timer |
| Done | Wird nach Ablauf gesetzt |
| Reset Zeit | Täglicher Reset |

---

## 🧠 Funktionsweise

1. Start-Trigger → Timer startet  
2. Running → EIN  
3. Nach Ablauf → Done = EIN  
4. Reset-Zeit → alles wieder AUS  

---

## 💡 Beispiel (Teich / Pumpenlaufzeit)

- Pumpe startet → Timer wird gestartet  
- Nach z. B. 5 Stunden → Abschaltung  
- Am nächsten Tag automatisch wieder freigegeben  

---

## 🧩 Multi-Instance Nutzung

Mehrere Timer parallel möglich:

- `pool_timer_*`  
- `garten_timer_*`  
- `teich_timer_*`  

---

## 🛠️ Beispiele

- `/examples/example_setup.yaml`  
- `/examples/lovelace.yaml`  
- `/examples/button.yaml`  

---

## 🖥️ Dashboard Beispiel

Beispiel für Lovelace UI zur Steuerung:

```
/examples/lovelace.yaml
/examples/button.yaml
```

---

## 📜 Lizenz

MIT Lizenz

---

## 🤝 Mitwirken

Beiträge sind willkommen:

- Issues erstellen  
- Verbesserungen vorschlagen  
- Features einreichen  

---

## ⭐ Support

Wenn dir das Projekt gefällt, gib ihm ein ⭐ auf GitHub
