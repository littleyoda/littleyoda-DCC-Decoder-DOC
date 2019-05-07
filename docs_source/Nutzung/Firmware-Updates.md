Sollte irgendwann mal der Bedarf bestehen die Software, die auf dem ESP8266 läuft, zu aktualisieren, braucht man nicht den Weg zu beschreiten, der unter [Erste Schritte](Erste-Schritte) erklärt war, vielmehr kann die Firmware direkt über einen Browser aktualisiert werden.

Die hochgeladenen Dateien (config.json, CSS-Datein) bleiben bei diesem Prozess unverändert!

Folgende Schritte sind notwendig:
- [Download](https://github.com/littleyoda/littleyoda-DCC-Decoder/releases) der aktuellen Firmware (Bin-Datei)
- Über einen Browser auf den ESP826 zugreifen
    - http://ip-addr/firmware also z.B. http://192.168.0.111/firmware
    - Sofern die Zugangsdaten in den Sourcen nicht geändert wurden, lauten der Username admin und das Password ebenfalls admin
- Auf Durchsuchen klicken und die Bin-Datei auswählen
- Anschließend auf Update klicken
- ca. 30 Sekunden warten
- Anschließend sollte man den Firmware Stand unter http://ip-addr/log prüfen.

Nur wenn dieser Ansatz nicht funktioniert, muss man auf den Weg über das Flash-Programm zurückgreifen.
