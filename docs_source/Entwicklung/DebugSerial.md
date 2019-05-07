# Debug über die serielle Schnittstelle

Wenn man den ESP8266 über ein USB-Kabel mit dem Computer verbindet, kann auf dem ESP8266 über die serielle Schnittstelle zugegriffen werden. Als Baudrate ist 115200 einzustellen.

Im laufenden Betrieb werden zum einen die Logmeldeungen über die serielle Schnittstelle ausgegeben, zum anderen stehen verschiedene Befehle im Debugmodus zur Verfügung. 

Der Debugsmodus wird durch das Senden der Zeichenfolge **'debug'** aktiviert. Anschließend können die Befehle über einzelne Buchstaben ausgelöst werdem. Groß- und Kleinschreibung sind relevant.

Folgende Befehle sind implementiert:

'd': 
Zeigt diverse Informationen über den ESP8266 inkl. Speicher und Wifi-Status an.
	
'r': 
Startet den ESP8266 neu. Dieser Weg funktioniert nicht, wenn der ESP8266 gerade neu geflasht wurde.

'D':
löscht das aktuelle Konfig-File. Nach dem Neustarten des ESP8266 ist er wieder über das WLAN-Netz "Hallo World" und der IP-Adresse 192.168.4.1 erreichbar.

'a':
Aktiviert den AccessPoint-Modus unabhängig vom Konfig-File. Die genutzte IP-Adresse kann über die 'd'-Funktion angezeigt werden.

'c':
Anzeige des Konfig-Files