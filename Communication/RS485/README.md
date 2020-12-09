# MAX485 RS-485 Modul
TTL zu RS-485 Modul für Arduino für die RS-485-Kommunikation.

![alt text][Produktabbildung]
>Abb: Produktabbildung

Spezifikation:
- Chip: Maxim MAX485
- Zwei Schraubanschluss mit 5,08 mm Rastermaß
- 2 x 4 Pin Stiftleiste im Rastermaß 2,54
- Betriebsspannung: 5V
- Abmessung: 46 (mm) x 12 (mm)

Sonstiges:
- Bezugsquelle eBay
- Kennzeichnung: LC Electronis

Die Datenleitungen A und B sind als Schraubklemme rausgeführt. Zusätzlich sind diese mit VCC und GND als 4 Pol Stiftleiste herausgeführt. Ein Abschlußwiderstand von 120 Ohm ist nicht bei jedem Boards vorhanden (laut c't Sonderheft). Vier Anschlüsse sind auf der TTL-Seite: zwei für das Senden und Empfangen der Daten (TTL DI/RO) und zwei für die Steuerung (TTL DE/RE), welche vom Mikrocontroller gesteuert werden sollen.

Mit Hilfe eines High-Speed FETs kann das Umschalten der Steuerleitung automatisiert werden. Näheres hierzu ist unter anderem im c't _Sonderheft Raspberry PI_ von 2017 beschrieben. 

```
                      ___       
                .----|___|----------------------o--------(V
                |     10k                       |    
                |    .-----------------------.  |   |JP1|
RX)-------------)---<| o RO            VCC o |--' .--o o--.
                o--o-| o RE   RS-485     B o |----'  ___  |
                |  '-| o DE   Modul      A o |------|___|-'
    .-----------)--->| o DI            GND o |--.    120
    |           |    '-----------------------'  |
    |   ___   |-+                               |
TX)-o--|___|->|                                 |
        10k   |-+                               |
                '-------------------------------o--------(G
```
>Abb: Schaltung

Grove Stecker | Arduino Uno | RS-485 Modul
--- | --- | ---
Pin 1 | GND | G
Pin 2 | VCC | V
Pin 3 | D1 | TX
Pin 4 | D0 | RX
>Tab: UART Steckplatz am Grove Base Shield V2

__JP1__ ist ein Jumper um ggf. den RS485-Bus mit einem 120-Ohm Widerstand zu terminieren. 

Die Anschlüsse für A und B stehen über die Schraubklemme zur Verfügung.

![alt text][Platine]
>Abb: Platine

### Nützliche Links
- http://github.com/franzs/raspberry_pi_rs485
- http://www.heise.de/ct/ausgabe/2017-17-Stromverbrauch-analysieren-mit-Raspi-und-Smart-Meter-3787264.html
- [ISBN:3957881870](http://www.google.de/search?hl=de&tbo=p&tbm=bks&q=isbn:3957881870)

[Produktabbildung]:https://github.com/brickpool/grove/blob/master/Communication/RS485/MAX485_RS-485_Module.jpg "MAX485 RS-485 Modul"
[Platine]:https://github.com/brickpool/Grove/blob/master/Communication/RS485/MAX485_RS-485_Module_Leiterplatte.png
