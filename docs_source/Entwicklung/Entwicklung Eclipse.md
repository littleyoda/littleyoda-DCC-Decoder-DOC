# Eclipse
## Eclipse mit Sloeber 
* [Java installieren](https://java.com/de/download/)
* [Eclipse mit Sloeber](http://eclipse.baeyens.it/) installieren

    Fertige Pakete zum installieren: [Linux](http://eclipse.baeyens.it/stable.php?OS=Linux) [Windows](http://eclipse.baeyens.it/stable.php?OS=Windows)
## Eclipse für den esp8266 konfiguieren
- Eclipse starten
- Windows/Preferences
- Unter [Selber kompilieren] sind die im folgenden benötigen Versionsnummern und Libaries dokumentiert.
- In dem Preferences-Dialog unter "Arduino/Platforms and Boards" die Option "esp8266/esp8266/<Version>" auswählen und Apply klicken. 
- In dem Preferences-Dialog unter "Arduino/Library Mangeer" die notwendigen Libraries in den passenden Versionen auswählen und Apply klicken
    
## Projekt auschecken
TODO

## Projekteinstellungen
- Projekt auswählen
- Unter Properties:
	- "C/C++ General"
	- "Paths and Symbols"
	- Tab "Source Location"
	- Ersten Eintrag auswählen
	- "Edit Filter"
	- Und über ADD, den folgenden Eintrag hinzufügen
	- "libraries/ArduinoJson/fuzzing/"
- Unter Arduino/"Add a library to the selected Projekt
 	Hier müssen die folgenden Library aktiviert werden:
	![](/img/EU_Libs1.png)
