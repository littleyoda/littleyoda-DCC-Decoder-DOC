Ein Hinweis vorab: 
Fertige Dekoder oder Bausätze biete ich aus rechtlichen Gründen nicht an. Platinen könnt ihr, so lange der Vorrat reicht, bei mir gegen Unkostenbeitrag + Porto erhalten und ich bin gerne bereit euch Bezugsquellen für die einzelnen Bauteile zu nennen, wenn es hier Probleme gibt.

Hier einige Beispiele

# Weichendecoder
Ein einfacher Weichendecoder, der zwei Weichenmotoren ansteuern kann.
Die Befehle werden entweder per DCC von den Schienen empfangen oder per WLAN von einer Z21.

[Weitere Informationen](USECASE_Weichendekoder)

[Konfigfile](https://github.com/littleyoda/littleyoda-DCC-Decoder/tree/master/Config-Templates/WeichenDecoder)

# Lokdekoder 1
Ein einfacher Lokdekoder, der eine fertige [H-Bridge](Begriff-H-Bridge) nutzt.
Die Befehle werden entweder per DCC von den Schienen empfangen oder per WLAN von einer Z21.

[Weitere Informationen](http://spurg.open4me.de/wordpress/786/Lokdekoder)

# Lokdekoder (DRV8870)
Ein einfacher Lokdekoder, der einen [DRV8870](http://www.ti.com/product/DRV8870) als [H-Bridge](Begriff-H-Bridge) nutzt.
Bedingt durch die Bauform des DRV8870 nicht so ganz einfach zu löten.

[Mehr Informationen](USECASE_Lokdekoder_DRV8870)

# Lokdekoder (BTS7960)
ein einfacher Lokdekoder, der eine BTS7960 Platine als [H-Bridge](Begriff-H-Bridge) nutzt.  
[Mehr Informationen](USECASE_Lokdekoder_BTS7960) 

# WLAN nach DCC Decoder
Ein Deocder, der ein DCC Signal generiert, mit denen klassische DCC-Decoder betrieben werden kann.
Sinnvoll, wenn man auf die Funktionalität von klassischen DCC-Decodern (Sound, ...) nicht verzichten will, aber DCC über Schienen nicht nutzen will.

[Mehr Informationen](USECASE_DCC_Generator)<br>
[L298N-Bridge](USECASE_DCC_Generator_L298N)<br>
[DRV8870](USECASE_DCC_Generator_DRV8870)

# Entwicklungsgeschichte
Eine Übersicht über die verschiedenen Entwicklungsstränge, die im Laufe der Zeit entstanden sind:
[Entwicklungsstränge](https://raw.githubusercontent.com/wiki/littleyoda/littleyoda-DCC-Decoder/img/Entwicklungsgeschichte.svg?sanitize=true)
Für einige Entwicklungsschritte sind weitere Informationen verlinkt.