# DCC Generator mit Hilfe einer L298N-Platine

Dieses Dokument beschreibt wohl den einfachsten Aufbau eines [DCC Generators](index.md).

## Schaltplan / Aufbau

Die aktuelle Schaltung besteht aus einem NodeMCU (D1 oder ähnliches würde natürlich auch gehen), einer L298N Motor Platine, einem NPN-Transitor (2N2222A), zwei 1k Ohm Widerstände und einem Akku-Pack.

![](../../img/L298nDCC.png)

Natürlich können auch andere H-Bridge genutzt werden. Hier muss ggf. noch eine unabhängig 5V Versorgung hinzugefügt werden.


![](https://www.open4me.de/my-content/20170708_DCC_Generator.jpg)

## Ansteuerung

Die Lösung kann über 2 Wege gesteuert werden:

* Der Decoder kann sich über WLAN mit einer Z21 verbinden und von dort die Befehle erhalten.
* Der Decoder kann eine Z21 simulieren und ein WLAN-Netz aufspannen.
   Anschließend kann man den Decoder direkt und ohne die Notwendigkeit einer Z21 ansteuern. Die Z21-App oder die WLAN-Maus kann zur Steuerung genutzt werden.



## Nutzungsbeispeile
Zoltan hat diesen Ansatz in seiner Harzkamel eingebaut.

Im Garten Bahn Forum hat er den Einbau [dokumentiert](http://www.gbforum.de/viewtopic.php?f=17&t=1087).

[![Harzkamel](https://img.youtube.com/vi/voZzVlcHkOM/0.jpg)](https://www.youtube.com/watch?v=voZzVlcHkOM)

![](../../img/DCC_Generator1.jpg)
*Copyright by Zoltan Egyed*
![](../..//img/DCC_Generator2.jpg)
*Copyright by Zoltan Egyed*

Bestandteile:
- Nodemcu-Board
- L293D-Platine
- Widerstände + Transistor
- 4 16850 Akkus
- ESU LokSound 4 XL 
 
## Technischer Hintergrund

siehe [DCC Generator](index.md)