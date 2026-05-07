1. Kirjelda võrgukihi olulisust võrguliikluses ning mis on ta peamised ülesanded
2. Töö välja 3 IP protokolli põhilist omadust (karakteristika).
3. Kirjelda IPv4 paketis järgnevaid väljasi:
    * Lähteaadress
    * Sihtaadress
    * Diferentseeritud teenused
    * TTL (Time to Live)
    * Kontrollsumma
    * Protokoll
4. Mis on MTU? Mis on tavajuhtudel MTU suurus kohtvõrkudes?
5. Miks on MTU oluline IP protokolli jaoks?
6.  Kirjelda, mis vahe on ainuedastus(unicast), multiedastus(multicast) ja leviedastus(broadcast) liiklusel ja IPv4 aadressidel nende liikluste puhul
7. Mis on ja miks on vaja NAT teenust? Kuidas jälgib ruuter NAT teenuse ühendusi?
8. Mis on vaikelüüs (default gateway)? Nimeta 2 seadet, mis võivad võrgus käituda kui vaikelüüs.
9. Kuidas teab host, et kas sihtaadress asub meiega samas kohtvõrgus (ühes IPv4 vahemikus) või mitte ning paketi edastamise eest vastutab kommutaator(switch) või ruuter?
10. Mis on ARP ning milleks on see vajalik?
11. Ruuter teeb edastamisotsuseid kasutades marsruutimis tabelit. Mis on ühe tabeli kirjes vaja minimaalselt kirjeldada, et pakett jõuaks sihtaadressini?
12. Mis tüüpi kirjed võivad olla marsruutimis tabelis (3)?
13. Mis vahe on staatilistel ja dünaamilistel marsruutimis kirjetel?

# 1. Kirjelda võrgukihi olulisust võrguliikluses ning mis on ta peamised ülesanded 
Võrgukiht pakub teenuseid, mis võimaldavad lõppseadmetel andmeid erinevate võrkude vahel vahetada. Peamised võrgukihi protokollid on IP versioon 4 (IPv4) ja IP versioon 6 (IPv6). 

# 2. Töö välja 3 IP protokolli põhilist omadust (karakteristika)
Ühendusetu - Sihtkohaga ei looda ühendust enne kui pakett teele saadetakse.  
“Parim pingutus” - IP on oma olemuselt ebausaldusväärne, kuna pakettide kohaletoimetamine pole garanteeritud.  
Meediast sõltumatu - Töö ei sõltu andmekandjast (nt vask, fiiberoptiline või traadita side). 

# 3. Kirjelda IPv4 paketis järgnevaid väljasi: 
    * Lähteaadress 
 Paketi saatja IP-aadress 
 
    * Sihtaadress 
 Paketi vastuvõtja IP-aadress. 
 
    * Diferentseeritud teenused 
 Pakette on võimalik jagada erinevatesse teenusteklassidesse, mida siis vastavalt klassile koheldakse erinevalt. Mõnedel pakettidel on vaja väikest viivitust, kuid teiste puhul kohale jõudmise usaldusväärsust 
 
    * TTL (Time to Live) 
Näitab, mitu hüpet (üheks hüppeks nimetatakse ühte marsruuteri läbimist) saab pakett veel teha, et sihtkohta kohale jõuda. Iga hüppega vähendatakse loendurit ühe võrra. Kui väärtus jõuab nullini, siis pakett visatakse minema 
    * Kontrollsumma 
. Arvutatakse ainult IP päise põhjal. Kuna "aega elada" väli iga hüppega muutub, siis on vajalik peale igat hüpet see uuesti arvutada. Kontrollib, kas saadu on sama, mis saadetu. 
 
    * Protokoll 
Määrab ülemise kihi protokolli. See on vajalik, et teada, mis protokolli abil tuleb paketis olevaid andmeid interpreteerida. Selline kapseldamine võib esmapilgul tunduda raiskamisena, kuid tegelikult võib see olla väga vajalik, näiteks VPN (Virtual Private Network jaoks (vaatleme hiljem pikemalt), IPv6 paketi saatmiseks üle IPv4 võrgu.

# 4. Mis on MTU? Mis on tavajuhtudel MTU suurus kohtvõrkudes? 
Võrgunduses on maksimaalne edastusühik (MTU) mõõtühikuks, mis tähistab suurimat andmepaketti, mida võrguga ühendatud seade vastu võtab. 

MTU-d mõõdetakse baitides – "bait" võrdub 8 bitiga infot, mis tähendab 8 ühte ja nulli. Maksimaalne MTU suurus on 1500 baiti. 

# 5. Miks on MTU oluline IP protokolli jaoks? 
MTU on oluline, kuna see määrab võrgus edastatavate andmete maksimaalse suuruse ilma killustatuseta. 

# 6.  Kirjelda, mis vahe on ainuedastus(unicast), multiedastus(multicast) ja leviedastus(broadcast) liiklusel ja IPv4 aadressidel nende liikluste puhul 
Ainuedastus (Unicast) on andmeedastus, kus üks saatja saadab andmed ühele vastuvõtjale. Seda kasutatakse tavaliselt veebivaatamistes ja e-kirjades. IPv4 unicast aadress on tavaline IP aadress, nagu 192.168.1.1. 
Multiedastus (Multicast) tähendab, et üks saatja saadab andmed mitmele valitud vastuvõtjale. Seda kasutatakse näiteks videokonverentsides ja IPTV-s. IPv4 multicast aadressid jäävad vahemikku 224.0.0.0–233.255.255.255. 
Leviedastus (Broadcast) on andmeedastus, kus üks saatja saadab andmed kõigile seadmetele samas võrgus. Seda kasutatakse näiteks DHCP-s ja võrgu teenuseavaldustes. IPv4 broadcast aadress on 255.255.255.255 või võrgu broadcast aadress (nt 192.168.1.255). 
Kokkuvõttes: unicast on üks-ühele, multicast on üks-ühele-paljudele, ja broadcast on üks-ühele-kõigile võrgu seadmetele. 

#  7. Mis on ja miks on vaja NAT teenust? Kuidas jälgib ruuter NAT teenuse ühendusi? 
NAT protokoll vastutab selle eest, et mitu kohaliku hosti saaksid kasutada ühte avalikku IPv4 aadressi. 
Ruuter muudab lähteaadresi enda avalikuks aadressiks ning hoiab antud ühendusega seotud kohalikku privaatsest aadresi ja porti meeles enda NAT tabelis. 

# 8. Mis on vaikelüüs (default gateway)? Nimeta 2 seadet, mis võivad võrgus käituda kui vaikelüüs. 
Vaikelüüs (Default gateway): Määrab ruuteri (või seadme, mis suhtleb ruuteriga) aadressi. Vajalik, kui on vaja suhelda seadmega, mis ei ole samas võrgus, kus arvuti ise. 
DSl ruuuter või kaabli ruuter 

# 9. Kuidas teab host, et kas sihtaadress asub meiega samas kohtvõrgus (ühes IPv4 vahemikus) või mitte ning paketi edastamise eest vastutab kommutaator(switch) või ruuter? 
Host määrab, kas sihtaadress on samas kohtvõrgus, võrreldes oma IP aadressi ja alamvõrgu maski abil sihtaadressiga. Kui need kuuluvad samasse võrku, saadetakse paket otse ja kommutaator edastab selle. Kui sihtaadress on teises võrgus, suunatakse pakett vaikesuunajale (ruuterile), mis edastab selle järgmisesse võrku. 

# 10. Mis on ARP ning milleks on see vajalik? 
Aadressiteisenduse protokoll.Kui me soovime suhelda kasutades IPv4 protokolli (nagu me enamasti seda teeme), on meil vaja vastendada IP aadressid MAC aadressideks. Vaatame nüüd kuidas ARP töötab. 
 ARP teostab peamiselt kahte funktsiooni: 
● IPv4 aadresside lahendamine MAC-aadressideks  
● IPv4 ja MAC aadresside vastandamise tabeli pidamine 

# 11. Ruuter teeb edastamisotsuseid kasutades marsruutimis tabelit. Mis on ühe tabeli kirjes vaja minimaalselt kirjeldada, et pakett jõuaks sihtaadressini? 
Otse ühendatud kohaliku liidese IP aadress 

# 12. Mis tüüpi kirjed võivad olla marsruutimis tabelis (3)? 
Staatilised marsruutimis kirjed 
- OSPF protokoll (Dünaamiline kirje) 
- EIGRP protokoll (Dünaamiline kirje)

# 13. Mis vahe on staatilistel ja dünaamilistel marsruutimis kirjetel? 
Staatilised: Administraator määrab käsitsi, püsivad ja ei muutu automaatselt. 

Dünaamilised: Loodud automaatselt marsruutimisprotokollide abil, kohanduvad võrgu muudatustega. 
