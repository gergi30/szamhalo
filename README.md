# Szamhalo ELTE IK
Számítógépes hálózatok definíciók kidolgozás 2016-17/1 

###Tartalomjegyzék
* [1.előadás](https://github.com/gergi30/szamhalo/blob/master/README.md#1-előadás-24-kérdés)
* [2.előadás](https://github.com/gergi30/szamhalo#2-előadás-x-kérdés)

##1. előadás (24 kérdés)

###Hány réteget különböztet meg az ISO/OSI referencia modell? Sorolja fel őket.
Hét féle réteget különböztet meg.

1. Fizikai
2. Adatkapcsolati
3. Hálózati
4. Szállítói
5. Ülés
6. Megjelenítési
7. Alkalmazási

###Hány réteget különböztet meg a Tannenbaum-féle hibrid rétegmodell? sorolja fel őket.
Öt féle réteget különböztet meg.

1. Fizikai
2. Adatkapcsolati
3. Hálózati
4. Szállítói
5. Alkalmazási

###Mi az "Open System Interconnection Reference Model" (ISO OSI), hogyan specifikáljuk az egyes rétegeket?
Röviden OSI referencia modell, amely egy 7-rétegű standard, koncepcionális modellt definiál kommunikációs hálózatok belső funkcionalitásaihoz.
Rétegek jellemzése:
* Szolgáltatás,
* Intefész,
* Protokoll
szerint.

###Mi a feladata és mik a főbb funkcionalitásai az ISO OSI modell fizikai rétegének?
Fizikai réteg:
* Szolgáltatás
  * Információt visz át két fizikailag összekötött eszköz között
  * Definiálja az eszköz és a fizikai átviteli közeg kapcsolatát
* Interfész
  * Specifikálja egy bit átvitelét
* Protokoll
  * Egy bit kódolásának sémája
  * Feszültség szintek
  * Jelek időzítése
* Példák
  * koaxiális kábel, 
  * optikai kábel,
  * rádió frekvenciás adó

###Mi a feladata és mik a főbb funkcionalitásai az ISO/OSI modell adatkapcsolati rétegének?
Adatkapcsolati réteg:
* Szolgáltatás
  * Adatok keretekre tördelésezés: határok a csomagok között
  * Közeghozzáférés vezérlés (MAC)
  * Per-hop megbízhatóság és folyamvezérlés
* Interfész
  * Keret küldése két közös médiumra kötött eszköz között
* Protokoll
  * Fizikai címzés (pl. MAC address, IP address)
* Példák
  * ethernet, 
  * wifi,
  * infiniBand

###Mi a feladata és mik a főbb funkcionalitásai az ISO/OSI modell hálózati rétegének?
Hálózati réteg:
* Szolgáltatás
  * Csomagtovábbítás
  * Útvonalválasztás
  * Csomag fragmentálás kezelése
  * Csomag ütemezés
  * Puffer kezelés
* Interfész
  * Csomag küldése egy adott végpontnak
* Protokoll
  * Globálisan egyedi címeket definiálása
  * Routing táblák karbantartása
* Példák
  *  Internet Protocol (IPv4), IPv6

###Mi a feladata az ISO/OSI modell ülés (session) rétegének?
Ülés (session) réteg:
* Szolgáltatás
  * kapcsolat menedzsment: felépítés, fenntarás és bontás
  * munkamenet típusának meghatározása
  * szinkronizációs pont menedzsment (checkpoint)
* Interfész
  * Attól függ…
* Protokoll
  * Token menedzsment
  * Szinkronizációs checkpoints beszúrás

###Mik a főbb funkcionalitásai az ISO/OSI modell megjelenítési rétegének?
Megjelenítési réteg:
* Szolgáltatás
  * Adatkonverzió különböző reprezentációk között
  * Pl. big endian to little endian
  * Pl. Ascii to Unicode
* Interfész
  * Attól függ…
* Protokoll
  * Adatformátumokat definiál
  * Transzformációs szabályokat alkalmaz

###Mit jelent a hálózatok esetén az adatok burkolása? 
Minden egyes réteg a saját fejlécét illeszti hozzá az aktuális csomaghoz végezetül pedig az IPdatagramm-hoz az Eternet-fejléc mellé egy Eternet lábléc is kerül (Eternet keret) ezzel a módszerrel az átviteli adatot „becsomagolva”.

###Mit jelent a legjobb szándék (best effort) elv a hálózati kommunikációban?
Kommunikáció a „legjobb szándék” (angolul best effort) elv szerint
* ha egy csomag nem éri el a célt, akkor törlődik
* az alkalmazás újraküldi ilyen esetekben

###Mit jelent a "Black-box" megközelítés a kapcsolatokra?
„Black box” megközelítés a kapcsolatokhoz
* a Black Box-okat később Gateway-eknek és Router-eknek keresztelték át
* csomaginformációk nem kerülnek megőrzésre
* nincs folyam-felügyelet

###Mi az a PAN?
Personal Area Network (magánhálózat) nagyon alacsony kiterjedésű hálózat, amely létrejöhet perifériák és gép, valamint gép és gép között, a lényeg, hogy ~1m-es a processzorközi távolság

###Mi az a WAN? 
Wide Area Network (nagykiterjedésű hálózat), amely nagyobb területet fed le, jellemzően országok, kontinensek közötti kommunikációt valósít meg.  ~100-1000km-es a processzorközi távolság

###Sorolja fel az internet 5 (előadáson elhangzott) jellemzőjét.
* rendszerfüggetlenség;
* nincs központi felügyelet;
* építőelemei a LAN-ok;
* globális;
* olyan szolgáltatásokat nyújt, mint a World Wide Web, e-mail vagy fájlátvitel.

###Definiálja a hálózati sávszélességet? 
Az adat átviteléhez elérhető vagy felhasznált kommunikációs erőforrás mérésére szolgáló mennyiség, amelyet bit per másodpercben szoktak kifejezni.

###Definiálja az átviteli késleltetést.
Az az időtartam, amely egy csomag összes bitjének az átviteli csatornára tételéhez szükséges. Jelölése: 𝑑𝑇.

###Definiálja a propagációs késést.
Az az időtartam, amely a jelnek szükséges ahhoz, hogy a küldőtől megérkezzen a címzetthez. Jelölése: d.

###Mi a hálózati hoszt?
Olyan eszköz, amely egy számítógépes hálózattal áll összeköttetésben. Egy hoszt információkat oszthat meg, szolgáltatást és alkalmazásokat biztosíthat a hálózat további csomópontjainak. (Továbbiakban csak hosztként hivatkozunk rá.)

###Mi az átviteli csatorna?
Az a közeg, amelyen a kommunikáció folyik a résztvevő hosztok között. Ez a közeg lehet egy koaxális kábel, a levegő, optikai kábel, stb. 

###Mi a fő különbség a csomagkapcsolt és az áramkörkapcsolt hálózatok között?
Csomagkapcsoltnál egy csatornán megy át többféle(minden) csomag, áramkör kapcsoltnál sok csatorna van és ezeket kapcsoljuk áramköri elemekkel egymáshoz.
![kapcsolat](https://github.com/gergi30/szamhalo/blob/master/kapcsolat.png)

###Adjon egy valós példát adatok beburkolására (pl. az előadáson látott Internet példa)!
-[ethernet header | IP header | TCP header | HTTP header | WEB PAGE | ethernet tailer]-

###Mit értünk Internet homokóra alatt? Miért nehéz az IPv6-ra való átállás?
Az internet homokóra az egyes rétegekben alkalmazott protokollok számát jelképezni. A hálózati rétegben nagyon kevés van, az IPv4 a legelterjedtebb és minden eszközt át kellene állítani IPv6-ra, hogy megfeleloen muködjön.

###Jellemezze egy mondatban a tűzfalakat, proxykat és NAT dobozokat!
Absztrakciós rétegek. 
* Tuzfal: Alkalmazásréteg fejlécét vizsgálhatja 
* Proxyk: Alkalmazás végpontot szimulál 
* NAT: Megtöri a végpont végpont elérhetoséget a hálózatban

###A Hálózati réteg funkcióit milyen síkok (planes) mentén csoportosíthatjuk még?
Control plane/Vezérlési sík: IP-BGP-RIP-OSPF

##2. előadás (x kérdés)
