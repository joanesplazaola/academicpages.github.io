---
title: 'Python ikastaroa (I)'
lang: eu
date: 2019-02-15
permalink: /posts/2019/02/python-ikastaroa/
use_code: true
tags:
  - python
  - tutoriala
  - oinarriak
---

Hasierako post hauek, programazioari eskainiko dizkiogu, ondoren garatzen joango garen gaietan dezente erabiliko baitugu Python programazio lengoaia.

Sarrera hauek batez ere programazio munduan oso sakon sartu gabeko jendearentzat dira, oinarrizko python ikusiko dugu,
 eta zertarako balio dezakeen ikusiko dugu. Batez ere datuen zientziari eta ikasketa automatikoari buruz ariko garenez,
 alor horretan gehien erabiltzen den programazio lengoaia erabiliko dugu.
 
## Eta zertarako ikasi behar dut nik Python?
 
Aurrerago ikusiko dugun moduan, Python, programazio hizkuntzen artean hasteko errazenetarikoa da, eta nahiz eta oso sintaxi
ulergarria duen, oso da erabilgarria.

Agian, ikasi ostean zure laneko ataza mekanikoak automatiko bihurtzeko, zure web orrialdea sortzeko, argazkietan jendearen 
aurpegiak detektatzeko, YouTubetik bideo listak jeisteko, edota joku bat sortzeko gai izango zara, beste hainbat gauzaren artean,
ez da aukera txarra, ez?


## Honera arte helduz gero, ez dut irtenbiderik, ez?

![](/images/2019/maze.jpg)

Egia esan, ez. Jada ezin da atzera egin, bilatzaileko atzerako botoia blokeatuta aurkituko duzu, eta ez baduzu aurrera jarraitzen
birus bat sartuko zaizu ordenagailuan, badakizu, Python jakitearen abantailak.

Gutxika-gutxika hasiko gara, lehenik, ikasteko beharko dituzun tresnak deskargatuko ditugu, ez da oso astuna izango, lasai.

Nahiz eta mundu guztiak Linux erabili beharko lukeen (:P) , badakit mundua ez dela perfektua, eta Windows eta MacOS erabiltzen duen jendea
ere existitzen dela... Jarraian, tresnak instalatzeko hiru moduak azalduko ditut, eta dena ondo egin dugun aztertuko dugu amaieran.

Python erabili ahal izateko, Miniconda instalatuko dugu, datuen zientziarako erabiltzen diren tresna gehienak berarekin 
ekartzen baititu.

[Miniconda](https://conda.io/en/latest/miniconda.html)|ren orrialdera sartuz gero, bi bertsio daudela ikusiko dugu, Python 2.x
 eta Python 3.x (x dagoen tokian zenbaki bat egongo da, 3.7 adibidez), guk azkena aukeratuko dugu, 3.x-a.

Aipatutako hiru moduetan (Linux, MacOS eta Windowsen) orain arteko bidea bera da, hemen hasten da desberdintasuna.

### Miniconda instalatu (Linux)

Linuxen oso da sinplea Miniconda instalatzea, gure ordenagailuaren arkitekturaren arabera, 32-bit edo 64-biteko instalatzailea aukeratuko
dugu. Horretarako, terminala zabaldu, eta `lscpu` idatziko dugu.

Bertan, lehen lerroan, "Architecture" sarrera ageriko zaigu, "x86_32" balio izanez gero, sistema 32-bitekoa dela esan nahiko du, 
eta "x86_64" baliorekin berriz, 64-bitekoa dela.

Behin hori dakigunean, Linux-en azpian dagokigun instalatzailea jeitsiko dugu. 

Jaitsi ostean, fitxategi kudeatzailean fitxategia deskargatu den tokira joango gara, eta ezer aukeratu gabe, saguaren eskuineko
botoia klikatuz, "Open in Terminal" edota "Ireki terminalean" aukeratuko dugu.

Terminalean, `sh fitxategiaren_izena.sh` komandoaren bidez, fitxategia exekutatuko dugu. Nire kasuan horrela izango litzateke:

```bash
sh Miniconda3-latest-Linux-x86_64.sh
```

Enter tekla sakatuz, MiniCondaren instalazio menua ikusiko dugu, hainbat galderarekin.

1. “In order to continue the installation process, please review the license agreement.” jartzen duen tokian, Enter botoia sakatu.
2. Segi beheraino (irakurriz, noski) eta idatzi "Y" ados zaudela esateko.
3. Miniconda instalatuko den tokia adieraziko digu, mantendu nahiz gero, enter sakatu, bestela aldatu eta enter.
4. Hurrengoari ere dagoen moduan baieztatu, gure PATH globalean sartuko du Miniconda, eta edonon erabili ahal izango dugu.
5. Microsoft Visual Studio Code IDEa instalatu nahi dugun galdetuko digu, gustoko izanez gero, aukeratu, nik ez dut gomendatzen,
gero aipatuko dugu zein IDErekin egingo ditugun garapenak.
6. Amaitu da instalazioa! Orain itxi terminala, eta ireki berri bat.
7. Terminal berrian idatzi `source ~/.bashrc`, instalazioa aplikatzeko.
8. Dena ondo dagoen ikusteko, `conda -V` idatzi terminalean, `conda 4.6.3` moduko zerbait ikusi beharko litzateke.





### Miniconda instalatu (Windows)

Windowsen, instalazioa guztiz grafikoa da, eta oso sinplea. Lehenik, gure sistemaren arkitekturaren arabera, 32 edota 64-biteko
 instalatzailea aukeratuko dugu. Gurea zein den jakiteko, tutorial [honetako](https://support.wdc.com/knowledgebase/answer.aspx?ID=9405)
 pausuak jarraituko ditugu.

Behin hori dakigunean, Linux-en azpian dagokigun instalatzailea jeitsiko dugu. 

Jaitsi ostean, Windowseko beste edozein exekutagarriren antzera, bi klik eginaz exekutatuko dugu.


MiniCondaren instalazio menua ikusiko dugu, eta pausu hauek emango ditugu.

1. "Irakurri" lizentzia testua eta "I agree" klikatu.
2. Segi beheraino (irakurriz, noski) eta idatzi "Y" ados zaudela esateko.
3. Miniconda instalatuko den tokia adieraziko digu, mantendu nahiz gero, enter sakatu, bestela aldatu eta enter.
4. Hurrengoari ere dagoen moduan baieztatu, gure PATH globalean sartuko du Miniconda, eta edonon erabili ahal izango dugu.
5. Microsoft Visual Studio Code IDEa instalatu nahi dugun galdetuko digu, gustoko izanez gero, aukeratu, nik ez dut gomendatzen,
gero aipatuko dugu zein IDErekin egingo ditugun garapenak.
6. Amaitu da instalazioa! Orain itxi terminala, eta ireki berri bat.
7. Terminal berrian idatzi `source ~/.bashrc`, instalazioa aplikatzeko.
8. Dena ondo dagoen ikusteko, `conda -V` idatzi terminalean, `conda 4.6.3` moduko zerbait ikusi beharko litzateke.