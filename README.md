# Szamhalo ELTE IK
Számítógépes hálózatok definíciók kidolgozás 2016-17/1 

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

###Definiálja a hálózati sávszélességet? 

###Definiálja az átviteli késleltetést.

###Definiálja a propagációs késést.

###Mi a hálózati hoszt?

###Mi az átviteli csatorna?

###Mi a fő különbség a csomagkapcsolt és az áramkörkapcsolt hálózatok között?

###Adjon egy valós példát adatok beburkolására (pl. az előadáson látott Internet példa)!

###Mit értünk Internet homokóra alatt? Miért nehéz az IPv6-ra való átállás?

###Jellemezze egy mondatban a tűzfalakat, proxykat és NAT dobozokat!

###A Hálózati réteg funkcióit milyen síkok (planes) mentén csoportosíthatjuk még?
