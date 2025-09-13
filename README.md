# Konrad – Konsole Random Scheme

**Konrad** ist ein kleines Bash-Wrapper-Script für KDEs **Konsole**, das bei jedem Start automatisch ein zufälliges Farbschema auswählt.  
Es ist **kein Plugin**, sondern läuft als eigenständiges Binary (Shell-Script).  

## Funktionsweise
- Sucht alle `*.colorscheme` Dateien in:
  - `~/.local/share/konsole/`
  - `/usr/share/konsole/`
- Liest den Anzeigenamen aus der `[General]`-Sektion (`Name=...`)
- Wählt zufällig eines dieser Schemen aus
- Wendet es mit `konsoleprofile colors=<Name>` auf den aktuellen Tab an
- Startet danach die gewohnte Shell (`$SHELL`)

## Installation
1. Script nach `~/.local/bin/konsole-random-scheme` (oder `/usr/local/bin/`) kopieren:
   ```bash
   chmod +x ~/.local/bin/konsole-random-scheme
   ```
2. Sicherstellen, dass das Binary im `$PATH` liegt.
3. Optional einen Alias setzen, z. B. in `~/.bashrc`:
   ```bash
   alias konrad="konsole -e konsole-random-scheme"
   ```

## Nutzung
```bash
konrad
```
oder direkt  
```bash
konsole -e konsole-random-scheme
```

Jedes neue Fenster oder jeder neue Tab bekommt so ein anderes zufälliges Farbschema.

## Hinweise
- Wenn keine `*.colorscheme`-Dateien gefunden werden, fällt das Script einfach zurück in die Standard-Shell.
- Bestehende Systemeinstellungen von KDE werden nicht überschrieben.  
- Du kannst jederzeit eigene `.colorscheme`-Dateien hinzufügen.
