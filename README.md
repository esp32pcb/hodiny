<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://github.com/esp32pcb/hodiny/blob/main/cas%20vecer.jpg">
  <source media="(prefers-color-scheme: light)" srcset="https://github.com/esp32pcb/hodiny/blob/main/hodiny%20svitici%20light.jpg">
</picture>

# HODINY NA MATICOVEM DISPLEJI RIZENE SNTP Z INTERNETU 
## hodiny na led displeji 32x8 s max7219

## co zatim umi?
- moznost nastaveni wifi pomoci aplikace ESPTOUCH SMARTCONFIG
- upgrade firmware PRES OTA
- nastaveni intensity displeje podle okolniho svetla
- cas z SNTP
- datum co 1 minutu
- kdo ma svatek 
- pokud je pridan senzor HDC1080 na I2C sbernici tak zobrazuje take teplotu a vlhkost

## sestaveni
video k sestaveni hodin najdete na [youtube](https://www.youtube.com/playlist?list=PLUCHvT3VSIT8nw8vogFUVakzei5OW-S98)

## wifi
- po spusteni hodin poprve je wifi prednastavena na SSID "IOT" a password "12345678".
  Pokud si nastavite mobilni hotspot s temito parametry tak se hodiny pripoji a zacnou ukazovat cas, datum a svatky.
## nastaveni wifi
- wifi se nastavuje pomoci aplikace ESPTOUCH SMARTCONFIG, ktera je jak pro android a tak pro iphone
- pripojite se mobilem na 2,4 Gb sit na ktere budou pripojeny take vase hodiny. Musi byt 2.4 Gb! 5Gb ESP neumi!

- Neni li v okoli znama wifi sit zustanou hodiny tmave a svítí led v pravém horním rohu. Pozdejsi verze uz maji napis "wifi?"
- stisknete tlacitko G35 na dobu delsi nez 5 sekund. na displeji projede napis "mobil - start smart config"
- spustite aplikaci ESPTOUCH SMARTCONFIG, vyplnite heslo k vasi wifi a stisknete connect.
- hned aktualizujte firmware

## aktualizace firmware
Po připojení na WiFi si zkuste aktualizovat firmware.
Tlacitko G34 držte déle než 5s a aktualizace se spustí.

FW verze 
- 1.10 změna chování u startu hodin. Po zapnutí se na displeji zobrazí text "wifi?"
  
- 1.1 startovací verze.

## kontakt
esp32hodiny@gmail.com




