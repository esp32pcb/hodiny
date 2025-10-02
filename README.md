<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://github.com/esp32pcb/hodiny/blob/main/cas%20vecer.jpg">
  <source media="(prefers-color-scheme: light)" srcset="https://github.com/esp32pcb/hodiny/blob/main/hodiny%20svitici%20light.jpg">
  <img alt="Shows an illustrated sun in light mode and a moon with stars in dark mode." src="https://user-images.githubusercontent.com/25423296/163456779-a8556205-d0a5-45e2-ac17-42d089e3c3f8.png">
</picture>

# HODINY NA MATICOVEM DISPLEJI RIZENE SNTP Z INTERNETU 
## hodiny na led displeji 32x8 s max7219

## co zatim umi?
- nejnovejsi firmware [1.5x](https://fota.vipro.cz/flash_full_fw.html) umi diakritiku, ceske a slovenske svatky. Pomoci webove stranky nastavit zatim intenzitu displeje, ale pridame tam do budoucna i eventy, kam si bude moci zapsat vyznamne udalosti (narozeniny atd.)
- nastaveni wifi pomoci mobilni aplikace ESPTOUCH SMARTCONFIG. funguje take [ESP CONFIG](https://play.google.com/store/apps/details?id=com.techbot.smart_config)
- upgrade firmware pres OTA
- nastaveni intensity displeje podle okolniho svetla ( na to je tam ta ledka )
- cas je rizeny z SNTP
- datum a kdo ma svatek co 1 minutu
- pokud je pridan [senzor HDC1080](https://github.com/esp32pcb/hodiny/blob/main/senzorHDC1080_1.jpg) na I2C sbernici tak zobrazuje take teplotu a vlhkost
- stopky - [časomíra](https://youtu.be/6PLG5gm5gp4) 0-99s po milisekundách 

# chcete si programovat sami?
## stáhněte si program pro arduino hodiny a experimentujte podle vlastních potřeb

Pro všechny nadšence a DIY (Do-It-Yourself) kutily mám vzrušující zprávu! Na adrese https://github.com/esp32pcb/arduino-clock je nyní k dispozici program pro naše Arduino hodiny. Tento program vám umožní experimentovat a přizpůsobit hodiny dle vašich specifických potřeb a představ.

V tomto repozitáři naleznete veškeré potřebné zdrojové kódy a instrukce, jak hodiny nastavit a modifikovat. To vám otevírá dveře k neomezeným možnostem – od změny zobrazovaných informací až po integraci nových senzorů a funkcí.

Důležité Upozornění:
Je třeba mít na paměti, že jakmile provedete změny v programu a nahrajete je do hodin, nebude již možné se vrátit k původnímu softwaru hodin, který byl nainstalován při nákupu. Před prováděním jakýchkoli změn si prosím pečlivě přečtěte instrukce a ujistěte se, že rozumíte všem krokům procesu.

Tento krok je součástí našeho závazku podporovat komunitu nadšenců a umožnit každému, aby se podílel na rozvoji a inovacích. Těším se na vaše vlastní projekty a nápady, jak hodiny dále vylepšit!


## Zjisteni stranky hodin na prohlizeci
- po upgrade firmware se po restartu objevi na displeji hodin ip stranky kterou mate zadat do prohlizece kterym se pripojujete na internet.
  Podminka na pripojeni je, ze musite byt pocitacem nebo mobilem pripoeni na stejne siti.
  Napr. displej po restartu ukaze IP: 192.168.1.5 tak na prohlizeci zadate 192.168.1.5, Protoze nepouzivame https, prohlizec upozorni, ze stranky jsou neduveryhodne tak se neleknete dejte pripojit.
  Pak se nactou stranky z esp32.

## Vylepseni hodin
- pridana diakritika a ovladani hodin prez webove rozhrani
- pridano animovani cisel


## sestaveni
v Hadexu nebo tady si kupte celou [stavebnici](https://www.hadex.cz/m304-stavebnice-hodiny-s-esp32-vroom-32-24ghz-wifi--bluetooth) .

video k sestaveni hodin najdete na [youtube](https://www.youtube.com/playlist?list=PLUCHvT3VSIT8nw8vogFUVakzei5OW-S98)

[senzor HDC1080](https://github.com/esp32pcb/hodiny/blob/main/senzorHDC1080_1.jpg) koupíte tady.

Pokud si stavebnici koupite u mne (kontakt je dole) tak [senzor teploty a vlhkosti](https://github.com/esp32pcb/hodiny/blob/main/senzorHDC1080_1.jpg) dostanete jako bonus zdarma.

## wifi
- po spusteni hodin poprve je wifi prednastavena na SSID "IOT" a password "12345678".
  Pokud si nastavite mobilni hotspot s temito parametry tak se hodiny pripoji a zacnou ukazovat cas, datum a svatky.
## nastaveni wifi
- wifi se nastavuje pomoci aplikace [ESP CONFIG](https://play.google.com/store/apps/details?id=com.techbot.smart_config), ktera je jak pro android a tak pro iphone
- pripojite se mobilem na 2,4 Gb sit na ktere budou pripojeny take vase hodiny. Musi byt 2.4 Gb! 5Gb ESP neumi!

- Neni li v okoli znama wifi sit zustanou hodiny tmave a svítí led v pravém horním rohu. Pozdejsi verze uz maji napis "wifi?"
- stisknete tlacitko G35 na dobu delsi nez 5 sekund. na displeji projede napis "mobil - start smart config"
- spustite aplikaci ESPTOUCH SMARTCONFIG, vyplnite heslo k vasi wifi a stisknete connect.
- hned aktualizujte firmware pro nejnovejsi software

## aktualizace firmware
Po připojení na WiFi si zkuste aktualizovat firmware.
Tlacitko G34 držte déle než 5s a aktualizace se spustí.


----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# nove FW verze s diakritikou a webovym rozhranim 

## pred stazenim techto fw je potreba projit prez kompletni preinstalaci firmware 
### jak na to?
- pripojite hodiny k pocitaci kde je chrome
- webovy flashovaci program najdete na [strance](https://fota.vipro.cz/flash_full_fw.html)
- pokud vam program nenajde pripojene hodiny je treba stahnout a nainstalovat driver pro CP2102
- potom znovu pripojit hodiny a dat conect
- nezapomenout nastavit "erase flash"
- program automaticky vymaze a znovu nainstaluje cele hodiny. zrusi se cele nastaveni.
- je portreba znovu nastavit wifi podle navodu.
- pote si pomoci tlacitka G34 upradujte nejnovejsi verzi.
- [video jak na to](https://youtu.be/ImiZ511ttPk)

## jak se dostat na webove rozhrani hodin
- po restartu hodin se na displeji ukaze IP adresa kde naleznete webove stranky hodin. napr. IP: 192.168.1.23.
- spustite svuj oblibeny webovy prohlizec a do adresniho radku zadate jenom 192.168.1.23.
- prohlizec sice nahlasi, ze stranky jsou nezabezpecene ale klidne se na ne pripojte.
- muzete si prochazet nastaveni (casem se budou pridavat funkce)
- naleznete tam take browser, kdo to umi muze si editovat webove stranky, napr menit barvy atd.
- pokud cokoliv zkazite tak si muzete znovu upgradovat firmware pomoci G34 a stranky se obnovi do puvodniho stavu.
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
## FW s diakritikou a webovym rozhranim
30.9.2025
- 1.54  fix resetovani hodin kdyz neni pripojen senzor hdc1080

17.9.2025
- 1.53  vylepsene info na displeji po upgrade a startu na dipleji. 

16.9.2025
- 1.5x   uplne novy firmware ktery obsahuje diakritiku, a je mozne si prez web na esp32  nastavit zatim intenzitu displeje. Cely webovy flashovaci program najdete na [strance](https://fota.vipro.cz/flash_full_fw.html)
- je tam zaroven popis jak na to. Nezpomente si pak klasickym zp;sobem stahnout nejnovejsi FW

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
## stary FW ktery jde upgradovat standardne prez tlacitko G34. Pro novejsi se musi preinstalovat cele hodiny viz navod vyse.
22.8.2024
- 1.32  uprava regulace jasu podle okolniho osvetleni. Ted jde plynule a reaguje okamzite. Pri mereni vlhkosti neukazuje obcas 100%. (pokud by nekomu ukazovalo, tak prosim dejte vedet. na mych kouscich uz to nedela)

11.4.2024
- 1.31  přidána časomíra od 0-99s, rozlišení milisekundy - jak [nastavit](https://youtu.be/hgDsx6DGCJs)

26.10.2023
- 1.20 animovane cisla pri zmene hodin popripade po ukazani datumu a teploty viz [youtube](https://www.youtube.com/playlist?list=PLUCHvT3VSIT8nw8vogFUVakzei5OW-S98)

12.08.2023
- 1.10 změna chování u startu hodin. Po zapnutí se na displeji zobrazí text "wifi?"
  
- 1.1 startovací verze.

## podivejte se na novou verzi hodin s [ESP32-s3 N16/R8](https://github.com/esp32pcb/hodiny_v2/wiki)

## kontakt
Marcel Juchelka
esp32hodiny@gmail.com
tel.: +420 733 255 252




