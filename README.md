# Konrad

**Konrad** ist eine modifizierte Version der KDE-Konsole (*konsole*), die beim Start automatisch ein zufälliges Farbschema lädt.  
Es handelt sich **nicht** um ein Plugin, sondern um ein eigenständiges Binary. Die Farbschemata liegen als normale Schema-Dateien im Dateisystem.

## Features
- Startet wie die normale KDE-Konsole
- Wählt bei jedem Start ein zufälliges Farbschema
- Verwendet Standard-Konsole-Schema-Dateien (`konsole-random-scheme`)

## Installation
1. Binary `konrad` ins `$PATH` legen (z. B. `/usr/local/bin/`).
2. Farbschemata ins KDE-Schema-Verzeichnis kopieren:
   - Systemweit: `/usr/share/konsole/`
   - Benutzerbezogen: `~/.local/share/konsole/`

## Nutzung
Einfach im Terminal starten:
```bash
konrad
