# Nutzung einer z21/Z21
## Wieviele Geräte/Decoder kann die z21 verwalten
Die genaue Anzahl ist unbekannt. Roco gibt teilweise eine maximale Anzahl von 10 Geräten per WLAN an.
Jedes Endgerät (z21-App/WLan-Maus) und jeder Decoder, der per WLAN kommuniziert, zählt als ein Gerät.

Rocrail kann als Software-Lösung dienen, um diese Einschränkung zu umgehen.

# Hardware
## Unterstützung ESP32
Der (Standard)-ESP32 wird für viele Dinge unterstützt. Erzeugung von DCC
Signalen fehlt jedoch z.B. noch.

Nicht unterstützt werden z.B. die ESP32-S2, ESP32-C3 oder ESP-C6.

# Fragen bei der Nutzung
## Config-File ist fehlerhaft und nun keine Verbindung zu dem ESP mehr.
** Lösung 1 (falls Verbindung über USB möglich) **
Über die serielle Schnittstelle kann das Config-File gelöscht werden:
"debug" eingeben und anschließen "D" eingeben. Nach dem Neustart baut der
ESP ein Access Point auf


** Lösung 2 (falls Kontrolle über die Stromversorgung) **
Durch die folgende Befehle, kann ein Access Point aktiviert werden und anschließend das Config-File korrigiert werden:

* ESP für 20 Sekunden einschalten
* danach ausschalten
* Einschalten und nach ca. 6 Sekunden wieder ausschalten<br>(er sollte mindestens 2 Sekunden laufen, darf aber nicht länger als 10 Sekunden laufen)
* Einschalten
* Nach ein paar Sekunden sosllte das WLAN-Netz "Hallo World" verfügbar sein