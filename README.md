<picture>
 <source media="(prefers-color-scheme: dark)" srcset="https://github.com/esp32pcb/hodiny/blob/main/cas%20vecer.jpg">
</picture>

# HODINY NA MATICOVEM DISPLEJI RIZENE SNTP Z INTERNETU 
## hodiny na led displeji 32x8 s max7219

## co zatim umi?
- moznost nastaveni wifi pomoci aplikace ESPTOUCH SMARTCONFIG
- upgrade firmware PRES OTA
- nastaveni intensity displeje podle okolniho svetla
- ukazuji cas z SNTP
- ukazuji datum co 1 minutu
- pokud je pridan senzor HDC1080 na I2C sbernici tak zobrazuje take teplotu a vlhkost


## wifi
- po spusteni hodin poprve je prednastavena wifi na SSID "IOT" a password "12345678".
  Pokud si nastavite mobilni hotspot s temito parametry tak se hodiny pripoji a zacnou ukazovat cas.
## nastaveni wifi
- wifi se nastavuje pomoci aplikace ESPTOUCH SMARTCONFIG, ktera je jak pro android a tak pro iphone
- pripojite se na 2,4 Gb sit. Musi byt 2.4 Gb! 5Gb ESP neumi!

- Neni li v okoli znama wifi zustanou hodiny tmave
- stisknete tlacitko P35 na dobu 5 sekund. na displeji projede napis "mobil - start smart config"
- spustite tuto aplikaci, vyplnite heslo k vasi wifi a stisknete connect.

