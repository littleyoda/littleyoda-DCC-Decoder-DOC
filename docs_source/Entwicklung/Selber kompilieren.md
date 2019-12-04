## Entwicklungsumgebung
Sofern euch die [fertig kompilierten Dateien](https://github.com/littleyoda/littleyoda-DCC-Decoder/releases) nicht reichen oder ihr selber entwickelt möchtet, benötigt ihr eine Entwicklungsumgebung.

Die [ArduinoIDE](Entwicklung Arduino.md) reicht für das kompilieren dieses Frameworks zwar aus, wirklich Spaß damit ein Projekt dieser Größe zu bearbeiten macht es aber nicht. Zwischenzeitlich habe ich [Eclipse](Entwicklung Arduino)
als Entwicklungsumgebung empfohlen.

Leider ist die Nutzung von Libaries in verschiedenen Versionen unter Eclipse schwierig, so dass ich mittlerweile [PlatformIO](Entwicklung PlatformIO.md) empfehle.

Für Personen, die die Sourcen einfach mal kompilieren wollen, reicht ggf. auch der [PlatonformIO CLI](Entwicklung PlatformIO CLI.md) Ansatz. Hierbei können die Sourcen auf der Kommandozeile kompiliert werden.

## Framework und Libraries Versionen
Bei den notwendigen Libaries verweise ich auf die [PlatformIO-Config](https://github.com/littleyoda/littleyoda-DCC-Decoder/blob/master/platformio.ini).
Aus dieser Datei kann entnommen werden in welcher Version das Arduino-ESP8266 (z.B. 2.4.2) und in welchen Versionen die Libaries vorliegen müssen.

