Der Funktionsumfang hängt natürlich primär von der genutzten Hardware ab. Im Prinzip wird aber folgendes unterstützt:

# Quelle
Befehle können, je nach Hardware, über die folgenden Wege empfangen werden:

- klassisch über ein DCC-Signal<br>(Schaltung mit Optokoppler ist notwendig)
- [z21-Zentrale](http://www.z21.eu/) drahtlos über WLAN.<br>
    Hierbei spielt es keine Rolle, wie die z/Z21 angesteuert wird (Z21-App, Multimaus, WLAN Maus, ...). Der Decoder kommuniziert mit der z/Z21 via WLAN und erhält so den aktuellen Zustand der Loks und Weichen.
- Über die WLAN-Maus oder über die Z21-App ohne(!) z21-Zentrale. <br>
 Hierbei simuliert der esp8266 eine z21 und die WLAN-Maus oder die Z21-App kommuniziert direkt mit dem Decoder.
* Webbrowser drahtlos via WLAN<br>Rudimentäre Unterstützung über jeden aktuellen Browser
* Rocrail<br>Nutzung von Rocrail als Zentrale
Andere Zentralen, die über einen Netzwerkanschluss verfügen, können relativ einfach hinzugefügt werden. Hierzu muss eine Klasse analog zur Klasse CmdReceiverZ21Wlan implementiert werden.

# Aktoren
* Ansteuerung von Weichenmotoren<br>Hiermit können die klassischen LGB oder PIKO Weichenmotoren angesteuert werden. Notwendig ist hierbei eine H-Bridge, wie z.B. L293D notwendig
* LED<br>Zur Zeit nur an oder aus. Hierbei ist ein Transistor oder ähnliches notwendig, da der esp8266 nicht auf ein direktes anschließen der LED ausgelegt ist.
* Servo<br>Ansteuerung von Servos. Keine spezielle Hardware notwendig
* DC Motoren<br>Ansteuerung von Motoren via PWM-Signal. Hierbei ist eine H-Bridge notwendig
* DCC Signal Generator<br>Hierbei wird ein DCC-Signal generiert; der ESP8266 verwandelt sich somit in eine kleine Art Minizentrale, die komplett in einem Zug eingebaut werden kann. Mit der Kombination Akku, ESP8266, H-Bridge und DCC-Decoder kann man einen autonomen Zug bauen, der weiterhin alle Vorzüge eines DCC-Decoders (z.B. Soundausgabe) bietet.