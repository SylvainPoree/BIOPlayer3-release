# Wichtigste Änderungen

- UI: Verbesserte Kennzeichnung der aktuell abgespielten Musik (Musiknote) in der Sitzung und in den Suchergebnissen.
- UI: Verbesserte visuelle Darstellung des Controllers.
- UI: Restlichen Code der oszillierenden Ladekugel im Fusion-Bildschirm entfernt.
- DEBUG: Unsichtbare Bereiche korrigiert, die Klicks auf dem Startbildschirm abfangen konnten: Flaggen und Schaltflächen können jetzt angeklickt werden, auch wenn Kiki oder -BIOPlayer- darüber liegen.
- FUNKTION: Verbesserte Wiederherstellung der Kennung: Ein fehlender Lizenzschlüssel wird automatisch erzeugt, wenn das Konto noch den temporären Wert `000-000-000` verwendet hat.
- TECH: Verbesserte Veröffentlichung der Update-Hinweise auf GitHub Pages, ohne Abhängigkeit von `rsync`.
- TECH: Windows-Installer nach Kanal getrennt: `BIOPlayer`, `BIOPlayer Beta` und `BIOPlayer Dev` können nun auf demselben Rechner nebeneinander installiert werden.
- UI: Das Windows-Herausgeberfeld wurde korrigiert: Es bleibt für alle Kanäle `BIOPlayer`.
