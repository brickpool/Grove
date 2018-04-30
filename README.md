# Das Grove-System
Ausgabe Ab

April 2018

## Hintergrund
Im Arduino-Umfeld ist es üblich, dass mit wenigen Bauteilen schnell Projekte realisiert werden sollen. Die Verbindungsmöglichkeit mit konventioneller Hardware ist jedoch teilweise fehleranfällig und manchmal kommt Frust auf. Abhilfe schaffen Standards oder ein System. 

Das Grove-System ist so ein Ansatz. Es besteht aus verschiedenen vordefinierten Modulen (Sensoren, Aktoren, etc.). Viel wichtiger ist aber, dass durch das Plug-and-play-Prinzip und der Standardschnittstelle eine einfache und schnelle Verkabelung möglich ist. Diesbezüglich ist das Grove-System insbesondere für das schnelle und fehlerfreie Prototyping von Vorteil. 

Die Idee hinter dem Grove-System fand ich so gut, dass ich mich entschlossen habe, vorhandene Boards, die teilweise aus unterschiedlichen Quellen stammen (also nicht kompatibel sind), so anzupassen, dass diese sich in das Grove-System einfügen. 

### Vorteile
- Ohne lange Vorbereitung sind Module sofort einsetzbar
- Schnelles und fehlerfreies Zusammenfügen
- Fokusierung auf das Projekt bzw. die Softwareprogrammierung
- Kein Lötkolben und kein Steckbrett

### Nachteile
- Einschränkung bzgl. mancher Board
- Grove Module sind im Vergleich teuer
- Herstellung von Adaptern ist teilweise teurer als ein Board
- Shields passen üblichweise nicht ins System

## Das Grove-System im Kern
Ein Adapter verwandelt einen standardmäßiges Board mittels Grove-Stecker in ein Systemkompatibles Board. Anders, als sonst im Arduino Umfeld üblich, kommen ausschließlich Kabel und Stecker aus dem Grove-System zum Einsatz. 

### Kategorien
Jede Kategorie hat in der Regel ein oder zwei Datenleitungen, eine Verbindung zur Versorgungsspannung und eine Verbindung zu Masse.
- Sensoren
- Aktoren
- Display
- Kommunikation
- Sonstige

### Kabelsatz
Die Länge der Kabel beträgt typischerweise ca. 20 cm, wobei jedes Kabel immer vier Leitungen hat und jede Leitung eine definierte Farbe. Module, die nur eine Datenleitung nutzen, haben i.d.R. beim weißen Kabel die Bezeichnung NC (no connection). 

Pin | Farbe | Bezeichnung | Bedeutung | Beispiel
--- | --- | --- | --- | ---
1 | gelb | Leitung n | | Pin 1 | D0
2 | weiß | Leitung n+1 | Pin 2 | D1
3 | rot | V | Vers.-Spannung (VCC) | 3,3V
4 | schwarz | G | Masse (GND) | 0V
> Tab: Farbenlehre

Kabellängen
- 5 cm
- __20__ cm
- 30 cm
- 40 cm
- 50 cm

### Konnekoren
Damit man einheitliche verkabeln kann, hat im Grove-System jeder Stecker 4 Anschlüsse. Der 4-polige Stecker ist immer der gleiche. Der Pin-Abstand beträgt 2mm (ein echter Nachteil).

Schnittstelle | Beispiel (Pin 1-4)
--- | ---
Digital | D2,D3,V,G
Analoge Eingänge | A0,A1,V,G
Analoge Ausgänge (PWM) | ~D3,D4,V,G
UART | RX,TX,V,G
I2C-Bus | SCL,SDA,V,G
> Tab: Standardschnittstellen

### Platinengröße
Die zu den Modulen gehörenden Platinen besitzen standardisierte Abmessungen im Raster von 2 x 2cm. Aktuell sind fünf Größen definiert:

Größe | Abmessung
--- | ---
1X1 | 20x20 mm
1X2 | 20x40 mm
1X3 | 20x60 mm
2X2 | 40x40 mm
2X3 | 40x60 mm
> Tab: Modulabmessungen

## Links
- http://wiki.seeedstudio.com/Grove_System/
- http://www.exp-tech.de/seeed-grove-wiki
