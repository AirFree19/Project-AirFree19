# Project-AirFree19
CO2 sensor + Window sensor


<p align="center">
  <img width="370" height="125" src="https://github.com/AirFree19/Project-AirFree19/blob/main/Argazkiak/Captura.png">
</p>

# HELBURUA
Covid-19aren aurrean bizitzen ari garen situazioa errexteko, 20 minuturo 5 minutu leihoak irekitzeko IoT sistema bat eratuko dugu. Honen helburua CO2 sentsore batekin airean dagoen hainbat datu jasoko dira eta datu hauei esker, jakingo dugu noiz ireki edo itsi ditzazkegun leihoak. Bestalde, datu guztiak Raspberry-Pi batera bidali eta honek Alexa gailuarekin (NodeRed erabilita) leihoetan eta CO2 sentsorea bertatik konfiguratzeko aukera izango dugu. Jarraian, proiektuaren krokix bat gehituko da.

# ERABILI DEN MATERIALA

## ESP32 Beetle
ESP32 Soc txipen familia baten izena da, kostu txikikoa eta energia kontsumokoa, Wi-Fi eta Bluetooth teknologia dual integratuarekin.
<p align="">
  <img width="150" height="150" src="https://images-na.ssl-images-amazon.com/images/I/61%2BqvvB9jmL._AC_SX522_.jpg">
</p>

## ESP8266 NodeMCU
ESP8266 Wi-Fi kostu txikiko txipa da, stack TCP/IP osoa eta mikrokontrolagailua dituena.
<p align="">
  <img width="150" height="150" src="https://electronilab.co/wp-content/uploads/2016/02/NodeMCU-%E2%80%93-Board-de-desarrollo-con-m%C3%B3dulo-ESP8266-WiFi-y-Lua-1.jpg">
</p>

## Litio bateria
Litio ioien bateria, Li-Ion bateria ere deitua, energia elektrikoa biltegiratzeko diseinatutako bi edo hiru energia gelaxkako gailu bat da.

![](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSknJpL85TrrIiIRkXitM55FZY-IamVMxsvAA&usqp=CAU)

## Magnetic Reed
Mihi-etengailu edo reed switch edo errele reed bat eremu magnetiko batek aktibatutako etengailu elektriko bat da.
 
![](https://robu.in/wp-content/uploads/2017/09/y213-magnetic-reed-switch-2-14mm-open-nadieleczone-1701-04-nadieleczone@2.jpg)

## Airearen kalitatea sentsorea(Metriful MS430)
Metriful sentsorea CO2 sentsore bezala lan egingo du. Berez ez dauka CO2 sentsore bat baina dauzkan sentsorei esker hanbit kalkulo egin ondoren CO2 kantitatearen aproximazio bat lortu dezake.

![](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSwblSzBO-Mvk6_2urAxk1zS9GUyYxrpQ1_Eg&usqp=CAU)

## Iman txikiak
Neodimio-imana lur arraroen iman mota erabiliena da.
<p align="">
  <img width="150" height="150" src="https://cdn-tienda.bricogeek.com/615-thickbox_default/iman-de-neodimio-cubo.jpg">
</p>


## Raspberry
Raspberry Pi 1, 2, 3 eta 3+ modeloetan oinarrituta. Nodo Zentrala izango da.

<p align="">
  <img width="150" height="150" src="https://cdn-tienda.bricogeek.com/5860-thickbox_default/raspberry-pi-4-model-b-4-gb.jpg">
</p>

## Alexa
Alexa Amazonek sortutako ahots bidezko laguntzaile birtuala da.

![](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQpdzqa4x0bZ604yki8ZzIau0i9Gh8POd7MLw&usqp=CAU)

# PROIEKTUAREN MONTAKETA
Proiektuaren montaketarekin hasteko, lehendabizi hainbat probak egin ziren bai Beetle-arekin eta bai Magnetic Reed-arekin. Proba hauek ondo atera ziren momentuan lehenengo PCB-ak sortzen hasi ziren. Lehenengo PCB hau Beetle- bat, erresistentzia bat eta azkenik Magnetic Reed-a egongo liratezke. Hiruak batera Leihoetako sentsore bat sortzen dute. Hortaz aparte, switch bat ezarri zen, dispositiboa nahi dugun baikotzean itzaltzeko aukera izateko. (Bi sentsoreak bateria bat eramango dute karkaxa generalean)


<p align="center">
  <img width="280" height="280" src="https://github.com/AirFree19/Project-AirFree19/blob/main/Argazkiak/Leihoak%20sensor.jpg">
</p>
<p align="center">1. Leihoko sentsoreen eskema proteusean.


<p align="center">
  <img width="280" height="280" src="https://github.com/AirFree19/Project-AirFree19/blob/main/Argazkiak/IMG_20210204_082434.jpg">
</p>
<p align="center">2. Leihoko sentsoreen plaka.

Leihoetan bukatzean, CO2 sentsorearekin eta ESP8266-arekin hasi izan genezakeen. Honekin, baita ere, probak egin izan behar genituen. Proba hauek konkluienteak izan zirenean, honen PCB sortu egin zen. Kasu honetan PCB-ak soilik bi elementu eramango zituen, Metrifula(sentsorea) eta ESP8266.


<p align="center">
  <img width="280" height="280" src="https://github.com/AirFree19/Project-AirFree19/blob/main/Argazkiak/CO2%20Sensor.PNG">
</p>
<p align="center">3. CO2-sentsoreen eskema proteusean.


<p align="center">
  <img width="280" height="280" src="https://github.com/AirFree19/Project-AirFree19/blob/main/Argazkiak/IMG_20210204_082351.jpg">
</p>
<p align="center">4. CO2 sentsorearen plaka.

Plakak egiteko, argazkietan ikusten diren bezala, lehendabizi Proteusean disenatu ziren, ondoren CircuitCam-en bidez LPKFn imprimatu . Plakak operatibo utzi ondoren Arduino-arekin eta NodeRed-ekin martxan jartzeko prest geuden. Bitartean Kampoko karkasak disenatzen hasi ginen.
### Beetle

<p align="center">
  <img width="280" height="280" src="https://github.com/AirFree19/Project-AirFree19/blob/main/Argazkiak/IMG_20210205_103856.jpg">
</p>
<p align="center">5. Leihoetako Karkaxa.


### CO2 Sentsorea

<p align="center">
  <img width="280" height="280" src="https://github.com/AirFree19/Project-AirFree19/blob/main/Argazkiak/IMG_20210205_103911.jpg">
</p>
<p align="center">6. NodeMCU eta Metriful.

Hauek aparte imanei beste karkasa batzuk sortu dizkiogu, batez ere estetika hobetzeko.

<p align="center">
  <img width="280" height="280" src="https://github.com/AirFree19/Project-AirFree19/blob/main/Argazkiak/IMG_20210205_104511.jpg">
</p>
<p align="center">7. Imanentzako Karkaxa.

<p align="center">
  <img width="280" height="280" src="https://github.com/AirFree19/Project-AirFree19/blob/main/Argazkiak/IMG_20210205_104514.jpg">
</p>
<p align="center">8. Imanentzako Karkaxa.

# FUNTZIONAMENDUA
Funtzinamendua hiru ataletan banatu daiteke:

Lehendabizi Beetle-ak aurkituko ditugu. Hauek leihoetan ezarriko dira eta leihoa ze egoeran dagoen esango digute. Hori egiteko NodeRed bitartez Rapberry-arekin konektatuta egongo da, hau da, Wifi bidez. Hau esan nahi du oso kontsumo handia eukiko duela eta arazo hori konpontzeko BeetleSleep programa ezarri diogu. BeetleSleep-eri esker lor dezakegu gure Beetle-ak soilik piztuta egotea seinale bat bidale behar duenean horrela gure kontsumoa murrizten eta bateriaren bizitza luzatuz.

Ondoren ESP8266 eta Metriful dauzkagu. Hauek Beetle-a bezala NodeRed bitartez Raspberry-arekin konektatzen dira baina kasu honetan kontsumoa ez da arazo bat, gure etxeko korrontera konektatuta egongo delako.

Azkenik Alexa aurki diezadakegu. Gure sistema osoa NodeRed-etik pasatzen da Alexan ikusi ahal izateko. Besteak bezala NodeRed-era konexioa dauka Raspberry-arekin harremanetan jartzeko eta horri esker Sentsireak bidaltzen duten seinaleak Alexan ikusgarriak dira.

# MARTXAN JARTZEA ETA DOIKETAK
Lehenengo pausoa gure Beetle-ei programa ezartzea izango litzateke. Programa Beetle-etan sartu ondoren, lehen inprimatutako PCB plaketan erresistentzia, switch-a eta Beetle-a bertan soldatzea izango litzateke hurrengo pausoa. Azkenik Beetle-ekin bukatzeko bateria PCB-an dauzkagun pinetan konektatu eta karkaxan sartu

Ondoren ESP8266 hasiko ginen. Hauei progroma sartu eta Metriful-arekin PCB-an soldatu behar izango genuke. Hauek soldatu eta gero karkaxan sartu beharko genikiztuen eta korrontera konektatu.

Azkenik Alexa eta NodeRed-ekin aurkituko gera. NodeRed-en gure lehioetan nahi dugun denbora edota nahi dugun CO2 minimoa ezarri beharko genuke. Hori egin ondoroen Alexan Silk ireki eta Dashboard ikusiko genituzke (IP-a sartu beharko genuke).

# AURREKONTUA

Elementua | Balioa | Kantitatea | Prezioa Unitateko | Balio totala €-tan
------------ | ------------ | ------------- | ------------- | -------------
ESP32 Beetle | 3,5V-6,5V | 2 | 14,29€ | 28,56€
ESP8266 NodeMCU | 3,3V-3,6V | 1 | 2,55€ | 2,55€
Metriful | 1,8-5V | 1 | 34,93€ | 34,93€
Bateria | 6,4V  1,5Ah | 2 | 9,28€ | 18,56€
Alexa | --- | 1 | 77,69€ | 77,69€
Erresistentziak | 48K | 2 | 0,12€ | 0,24€
PCB xafla | Aurpegi bat | 3 | 5,9€ | 17,7€
Magnetic Reed | --- | 2 | 0,62€ | 1,24€
Raspberry | 5,1V | 1 | 36,44€ | 36,44€
Karkaxa | --- | 5 | 5,00€ | 25,00€
Imanak | --- | 4 | 0,32€ | 1,28€
 | | | | Totala: | 244,13€

# ONDORIOAK
* Hasiera batean ESPNow sistema erabiltzen hasi ginen, baina ez genuen lortu ondo jutea(Arduino karpetan egongo da norbaitek probatu nahi badu)

* Paintailaren bat ezarri nahi genion baina azkeneean Alexan ikustea erabaki genuen

* Led bat eta bozeragailu bat ezarri nahi genizkion baina azkenean Alexak alertak egitea erabaki zen.


 





