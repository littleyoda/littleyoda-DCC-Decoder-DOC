# DCC Generierung

In diesem Fall erzeugt der ESP8266 mit Hilfe einer [H-Bridge](Begriff-H-Bridge) ein DCC-Signal mit welchem ein normaler DCC-Decoder angesteuert werden kann.

Die Befehle können z.B. per WLAN an den ESP8266 verschickt werden und dieser generiert ein DCC-Signal für eine H-Bridge. Mit diesem DCC-Signal wird dann ein klassischer DCC-Decoder angesteuert, der dann den Motor regelt.

Z21 App oder Wlan-Maus => WLAN => ESP8266 => H-Bridge => DCC-Signal => DCC-Decoder => Motor / Sound

Es ist darauf zu achten, dass die H-Bridge ausreichend dimensioniert ist. Im Spassbahn-Forum gab es die Diskussion, ob die H-Bridge überhaupt so stark sein muss oder ob es nicht ausreichen würde, den Decoder über den PowerPack-Eingang zu versorgen und eine "schwache" H-Bridge zu nutzen. (Diesen Test überlasse ich gerne anderen Personen)

Die Lösung kann über 2 Wege gesteuert werden:

* Der Decoder kann sich über WLAN mit einer Z21 verbinden und von dort die Befehle erhalten.
	Die Lok erhält sich in diesem Fall praktisch wie eine Lok, die ihre Befehle über die Schienen erhält.
* Der Decoder kann eine Z21 simulieren und ein WLAN-Netz aufspannen.
   Anschließend kann man den Decoder direkt und ohne die Notwendigkeit einer Z21 ansteuern. Die Z21-App oder die WLAN-Maus kann zur Steuerung genutzt werden.
 

## Warum dieser Ansatz?

Zwei Gründe (wovon ich aber nur den ersten wirklich teile)

1. Nutzung von Sound
   Obwohl es auch möglich wäre, Sound über den ESP8266 abzuspielen, ist die Nutzung eines klassischen DCC-Sounddecoder doch sehr viel einfacher.

2. bessere Qualität der Motoransteuerung
   Bei der Nutzung einer einfachen H-Bridge zur Motorsteuerung wird meistens nur ein einfaches lastunabhängiges PWM-Signal generiert. Hier sind die DCC-Decoder deutlich weiter.


## Funktionsumfang
Generiert ein DCC-Signal mit

- 128 Fahrstufen
- 28 Funktionstasten
    
## Anwendungsfälle
[L298N](DCC_Generator_L298N)
[DRV8870](DCC_Generator_DRV8870)


## Technischer Hintergrund

### SPI 
Das Signal wird im ESP8266 über den SPI-Ausgang erzeugt. Dieser Ausgang hat einen Hardware-Buffer, so dass sichergestellt ist, dass das DCC-Timing eingehalten wird. Es wird also immer ein DCC-Paket erzeugt, in das notwendige SPI-Format gewandelt und anschließend in den Hardware-Buffer geschrieben. Bei den ersten Tests stellt sich heraus, dass die SPI-Library beim Senden so lange blockiert, bis das Paket komplett verschickt wurde. Außerdem belegte die Library direkt drei GPIO für MISO, MOSI, SCK. Aus diesem Grund wurde die SPI-Library an die Bedürfnisse dieses Frameworks angepasst. Jetzt wird im einfachsten Fall nur noch ein Pin (13 bzw. D7) genutzt. Dieser Pin ist fest, da er der einzige nutzbare Pin mit Hardware-mäßiger SPI Unterstützung ist.

### "Halbes" DCC
An D7 liegt aber nur eine Art "positive Halbwelle" des DCC-Signales an. 
Da das DCC-Signal aber eine Wechselspannung ist, wird auch noch eine "negative Halbwelle" benötigt. Diese Halbwelle wird aus dem Signal von D7 durch einen Transistor erzeugt, der das Signal invertiert (siehe zweites Signal).
Es werden DCC-Paketen für die Geschwindigkeit und Richtung erzeugt, sowie Pakete für den Zustand von F0 bis F28.


## Prototypen

Da Julian Zimmermann, der diesen Ansatz im Spassbahn-Forum [vorgestellt](http://www.spassbahn.de/forum/index.php?thread/11462-spa%C3%9Flan-topfschlagen-im-minenfeld/&postID=117854) hatte, keine Zeit hatte ihn zu verfeinern und mich die technische Seite interessierte, habe ich ihn um die Sourcen gebeten, damit ich es in mein Framework integrieren kann. Nach einigen frustrierenden Abenden habe ich einen Prototypen zum laufen gebracht: Der Motorblock reagierte endlich auf die generierten DCC-Befehle.

[Entwicklungsgeschichte](http://gartenbahntechnik.de/viewtopic.php?f=22&t=418)

Aus diesem Prototypen haben sich die oben genannten Schaltungen entwickelt.
