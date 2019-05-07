# Weichendecoder
Motiviert durch die hohen Kosten von Weichendecodern und dem Interesse an dem ESP8266-Mikroprozessor habe ich begonnen einen Weichendecoder selber zu bauen.

Die aktuelle Version findet Platz auf einer 5 x 5 cm großen Platinen und kann die Befehle entweder per DCC über die Schienen oder aber via WLAN die Befehle direkt von der Z21 erhalten. Alternativ ist der Weichendekoder auch via Browser steuerbar. Ansteuerbar sind jeweils zwei LGB/PIKO/EPL Weichen.

Der Decoder kann entweder über Schienenstorm oder aber über eine externe Stromquelle versorgt werden. Die Spannung sollte zwischen 7 und 24V betragen.

## Aktueller Entwicklungsststand
Die Platine ist jetzt schon mehr als 1 1/2 Jahre (Stand: Jan 2018) im Einsatz. Hat den Forst von zwei Wintern überlebt.
 
## Hardware
Hauptkomponenten sind ein ESP8266 zur Steuerung und ein Motortreiber vom Typ L293D.
<table border="1">
<tbody>
<tr>
<td>Artikel</td>
<td>Anzahl</td>
<td>Gesamtpreis €</td>
<td></td>
</tr>
<tr>
<td>Platine</td>
<td>1</td>
<td>1,50</td>
<td></td>
</tr>
<tr>
<td>NodeMCU V2</td>
<td>1</td>
<td>2,90</td>
<td><a href="https://de.aliexpress.com/item/1pcs-Wireless-module-NodeMcu-Lua-WIFI-Internet-of-Things-development-board-based-ESP8266-CP2102-with-pcb/32698749571.html">Link</a></td>
</tr>
<tr>
<td>L293D</td>
<td>1</td>
<td>0,35</td>
<td><a href="http://s.click.aliexpress.com/e/3rzjiqJEi">Link</a></td>
</tr>
<tr>
<td>B80C1500</td>
<td>1</td>
<td>0,30</td>
<td><a href="http://s.click.aliexpress.com/e/urNrByrjM">Link</a></td>
</tr>
<tr>
<td>Anschlüsse</td>
<td>4</td>
<td>0,27</td>
<td><a href="http://s.click.aliexpress.com/e/urNrByrjM">Link</a></td>
</tr>
<tr>
<td>Spannungsregler</td>
<td>1</td>
<td>0,60</td>
<td><a href="https://de.aliexpress.com/item/1pcs-good-quality-Mini-3A-DC-DC-Adjustable-Step-down-Converter-Standard-Power-module-LM2596-A3/32698729438.html?ws_ab_test=searchweb0_0,searchweb201602_2_10091_10090_10088_10089,searchweb201603_1&amp;btsid=d7cc2775-c2be-451b-8f62-6a39a2e16713">Link</a></td>
</tr>
<tr>
<td>6N136</td>
<td>1</td>
<td>0,37</td>
<td><a href="http://s.click.aliexpress.com/e/RJ6IaeQrF">Link</a></td>
</tr>
<tr>
<td>1N4004</td>
<td>1</td>
<td>0,04</td>
<td><a href="http://s.click.aliexpress.com/e/yNbuzVBia">Link</a></td>
</tr>
<tr>
<td>220uF 35V</td>
<td>1</td>
<td>0,04</td>
<td><a href="http://s.click.aliexpress.com/e/E2JMfqrVz">Link</a></td>
</tr>
<tr>
<td>1,5 Kohm</td>
<td>1</td>
<td>0,01</td>
<td></td>
</tr>
<tr>
<td>10 Kohm</td>
<td>5</td>
<td>0,05</td>
<td></td>
</tr>
<tr>
<td>15 pin Buchsenleiste</td>
<td>2</td>
<td>0,24</td>
<td><a href="http://s.click.aliexpress.com/e/AqNRZnyV3">Link</a></td>
</tr>
<tr>
<td>Sockel 16 pin</td>
<td>1</td>
<td>0,09</td>
<td><a href="http://s.click.aliexpress.com/e/znQfauRnq">Link</a></td>
</tr>
<tr>
<td>Gehäuse 85x58x35</td>
<td>1</td>
<td>1,50</td>
<td><a href="http://rover.ebay.com/rover/1/707-53477-19255-0/1?icep_ff3=2&amp;pub=5575156058&amp;toolid=10001&amp;campid=5337967688&amp;customid=&amp;icep_item=252125751584&amp;ipn=psmain&amp;icep_vectorid=229487&amp;kwid=902099&amp;mtid=824&amp;kw=lg">Link</a></td>
</tr>
</tbody>
</table>

<kbd>[![Schaltplan](https://www.open4me.de/wp-content/uploads/weiche.jpg)](http://www.open4me.de/wp-content/uploads/weiche.pdf)</kbd>

<kbd>[![Platine](https://www.open4me.de/wp-content/uploads/Weiche_5x5_Leiterplatte-288x300.png)](http://www.open4me.de/wp-content/uploads/Weiche_5x5_Leiterplatte.png)</kbd>

