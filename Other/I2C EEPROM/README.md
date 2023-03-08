# I2C EEPROM Speichermodul

I2C EEPROM Speichermodul AT24C256 für Arduino

Spezifikation:
- Chip: AT24C256
- Stromversorgung: 2,7 - 5,5 V
- Versorgunganzeige: LED
- Abmessung: 37 x 12mm
- Stromaufnahme: ca. 5mA
- Temperautiurbereich: -40° to +85°C
- I2C-Adresse: einstellbar 0x50 bis 0x57

Sonstiges:
- Bezugsquelle eBay
- Bezeichnung _AT24C256 Serial EEPROM I2C Interface_

Für Projekte mit Display werden gerne Strings mit dem F() Macro in den Flash Speicher abgelegt. Dies ist aber ggf. nur bedingt hilfreich, da es für große Projekte knapp wird mit dem freien Flash Speicher.

Das im AVR eingebaute EEPROM bringt Linderung, aber mit zunehmender Größe reicht auch dieser Speicherbereich nicht aus, da der EEPROM Speicher des AVRs eher klein gehalten ist.

Abhilfe versprechen I2C EEPROMs, z.B EEPROMs der Atmel AT24Cxx Familie. Da es sich um ein I2C Interface handelt, ist eine Grove-kompatible Anschaltung schnell gemacht. 

Grove Stecker | Arduino Uno | IC2 Speichermodul
------------- | ----------- | -----------------
Pin 1         | GND         | GND
Pin 2         | 5V          | VCC
Pin 3         | A4          | SDA
Pin 4         | A5          | SCL
>Tab: I2C Steckplatz am Grove Base Shield V2

### Nützliche Links
- http://github.com/CombiesGit/I2C_EEPROM
- [Projekt I2C EEPROM](http://forum.arduino.cc/index.php?topic=369667.0)
