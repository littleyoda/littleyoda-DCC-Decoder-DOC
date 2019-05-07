# H-Bridge
Eine H-Bridge dient der Ansteuerung von Gleichstorm-Motoren.
Vereinfacht ausgedrückt sorgt sie dafür, dass die Polarität umgekehrt werden kann, der Motor sich also vorwärts und rückwärts drehen kann.

In Rahmen dieses Projektes, habe ich mit folgenden H-Bridges "gespielt":

## Chips
### [L293D](http://www.ti.com/lit/ds/symlink/l293.pdf)

Ist für 0,6A (1,2A Peak) ausgelegt. Ich nutze sie für meinen Weichendekoder. Mit [50 Cent (*)](http://s.click.aliexpress.com/e/3rzjiqJEi?4) unschlagbar billigt, aber der Chip verzeiht keine Fehler. Wenn die Ausgänge etwas zu lange aktiv sind, gibt sie schon mal Rauchzeichen von sich.

### [DRV8870](http://www.ti.com/product/DRV8870)
Diese H-Bridge ist für 2A (3,6A Peak) ausgelegt. Ich nutze sie für meinen Lokdekoder. Mit einem Preis von knapp 2€ nicht ganz so preiswert. Als [SMD-Bauteil](https://de.wikipedia.org/wiki/Surface-mounted_device) ist der Chip nicht einfach zu löten. Die größte Herausforderung ist, dass es unter dem Chip eine Metallfläche gibt, die für die  Wärmeableitung zuständig ist und normalerweise auf die Platine gelötet werden muss. Dieses ist jedoch mit Hobbymitteln nicht wirklich möglich. 

## Fertige Platinen
 
### [L298N](http://s.click.aliexpress.com/e/ynAieqV%22)
Diese Platine wurde im Test des DCC-Signal-Generators genutzt und trieb erfolgreichen einen Playmobil-Motorblock an.

### [BTS7960](http://s.click.aliexpress.com/e/zNrbMFE)
Diese Platine habe ich im Lokdekoder für eine Piko-Lok mit zwei Motoren genutzt.
