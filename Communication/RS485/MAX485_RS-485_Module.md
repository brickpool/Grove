# MAX485 RS-485 Modul
TTL zu RS-485 Modul f�r Arduino f�r die RS-485-Kommunikation.

![alt text][Produktabbildung]
>Abb: Produktabbildung

Spezifikation:
- Chip: Maxim MAX485
- Zwei Schraubanschluss mit 5,08 mm Rasterma�
- 2 x 4 Pin STiftleiste im Rasterma� 2,54
- Betriebsspannung: 5V
- Abmessung: 46 (mm) x 12 (mm)

Sonstiges:
- Bezugsquelle eBay
- Kennzeichnung: LC Electronis

Die Datenleitungen A und B sind als Schraubklemme rausgef�hrt. Zus�tzlich sind diese mit VCC und GND als 4 Pol Stiftleiste herausgef�hrt. Ein Abschlu�widerstand vcon 120 Ohm ist nicht on Board. View Anschl�sse sind auf der TTL-Seite f�r das Senden und  Empfangen der Daten (TTL TX/RX) und zwei Steuerleitungen (TTL RTS/CTS), die laut Beschreibung vom Mikrocontroller gesteuert werden sollen.

Mit Hilfe eines High-Speed FETs kann das Umschalten der Steuerleitung automatisiert werden. N�hres hierzu ist unter anderem in c't Sonderheft Raspberry PI von 2017 beschrieben. 

```
                      ___       
                .----|___|----------------------o--------(V
                |     10k                       |    
                |    .-----------------------.  |    |J|
RX)-------------)---<| o RO            VCC o |--' .--o o--.
                o--o-| o RE   RS-485     A o |----'  ___  |
                |  '-| o DE   Modul      B o |------|___|-'
    .-----------)--->| o DI            GND o |--.    120
    |           |    '-----------------------'  |
    |   ___   |-+                               |
TX)-o--|___|->|                                 |
        10k   |-+                               |
                '-------------------------------o--------(G
```
>Abb: Schaltung

Grove | Bezeichnung
--- | ---
Pin 1 | RX
Pin 2 | TX
Pin 3 | V 
Pin 4 | G

J ist ein Jumper um ggf. den RS485-Bus mit einem 120-Ohm Widerstand zu terminieren. 

Dioe Anschl�sse f�r A und B stehen �ber die Schraubklemme zur Verf�gung.

### N�tzliche Links
http://github.com/franzs/raspberry_pi_rs485
http://www.heise.de/ct/ausgabe/2017-17-Stromverbrauch-analysieren-mit-Raspi-und-Smart-Meter-3787264.html
http://www.google.de/search?hl=de&tbo=p&tbm=bks&q=isbn:3957881870

[Produktabbildung]: http://github.com/brickpool/grove/blob/master/Communication/RS485/MAX485_RS-485_Module.jpg "MAX485 RS-485 Modul"
