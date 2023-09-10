<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://github.com/esp32pcb/hodiny/blob/main/cas%20vecer.jpg">
  <source media="(prefers-color-scheme: light)" srcset="https://github.com/esp32pcb/hodiny/blob/main/hodiny%20svitici%20light.jpg">
  <img alt="Shows an illustrated sun in light mode and a moon with stars in dark mode." src="https://user-images.githubusercontent.com/25423296/163456779-a8556205-d0a5-45e2-ac17-42d089e3c3f8.png">
</picture>

# HODINY NA MATICOVEM DISPLEJI RIZENE SNTP Z INTERNETU 
## hodiny na led displeji 32x8 s max7219

## co zatim umi?
- nastaveni wifi pomoci mobilni aplikace ESPTOUCH SMARTCONFIG
- upgrade firmware pres OTA
- nastaveni intensity displeje podle okolniho svetla
- cas je rizeny z SNTP
- datum a kdo ma svatek co 1 minutu
- pokud je pridan [senzor HDC1080](https://github.com/esp32pcb/hodiny/blob/main/senzorHDC1080_1.jpg) na I2C sbernici tak zobrazuje take teplotu a vlhkost

## sestaveni
PCB si muzete koupit na e-shopu v [HADEXu](https://www.hadex.cz/m303-vyvojova-deska-s-esp32-vroom-32-24ghz-wifi--bluetooth)

v Hadexu si kupte i [displej](https://www.hadex.cz/m504a-led-matrix-matice-8x8x4-s-max7219---cervena).

video k sestaveni hodin najdete na [youtube](https://www.youtube.com/playlist?list=PLUCHvT3VSIT8nw8vogFUVakzei5OW-S98)

[senzor HDC1080](https://github.com/esp32pcb/hodiny/blob/main/senzorHDC1080_1.jpg) koupíte u tady.

## wifi
- po spusteni hodin poprve je wifi prednastavena na SSID "IOT" a password "12345678".
  Pokud si nastavite mobilni hotspot s temito parametry tak se hodiny pripoji a zacnou ukazovat cas, datum a svatky.
## nastaveni wifi
- wifi se nastavuje pomoci aplikace ESPTOUCH SMARTCONFIG, ktera je jak pro android a tak pro iphone
- pripojite se mobilem na 2,4 Gb sit na ktere budou pripojeny take vase hodiny. Musi byt 2.4 Gb! 5Gb ESP neumi!

- Neni li v okoli znama wifi sit zustanou hodiny tmave a svítí led v pravém horním rohu. Pozdejsi verze uz maji napis "wifi?"
- stisknete tlacitko G35 na dobu delsi nez 5 sekund. na displeji projede napis "mobil - start smart config"
- spustite aplikaci ESPTOUCH SMARTCONFIG, vyplnite heslo k vasi wifi a stisknete connect.
- hned aktualizujte firmware pro nejnovejsi software

## aktualizace firmware
Po připojení na WiFi si zkuste aktualizovat firmware.
Tlacitko G34 držte déle než 5s a aktualizace se spustí.

FW verze 
- 1.10 změna chování u startu hodin. Po zapnutí se na displeji zobrazí text "wifi?"
  
- 1.1 startovací verze.

## kontakt
esp32hodiny@gmail.com




