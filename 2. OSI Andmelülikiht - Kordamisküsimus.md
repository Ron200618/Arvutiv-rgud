1. Mis on andmelülikihi üldine ülesanne võrguliikluses?
2. Kuidas nimetatakse protokolliandmeüksuseid (PDU) siin tasemel?
3. Mis aadresse kasutades suheldakse siin võrgu tasemel? Kirjelda selle aadressi omadusi.
4. Millised seadmed (min 2) töötavad sellel kihil?
5. Mis funktsiooni täidab LLC alamkiht? Mis funktsiooni täidab MAC alamkiht?
6. Kirjelda, mis väljad on ühes ethernet kaadris ning mis nende väljade olulisus/eesmärk on?
7. Kirjelda ainuedastus (unicast), leviedastus (broadcast) ning multiedastus (multicast) liikluse erinevusi? Kuidas erinevad iga suhtluse puhul aadressid siin tasemel?
8. Mille abil edastab kommutaator (switch) andmeid? Kuidas ta seda teeb - kirjelda täpsemalt.
9. Mis on leviedastus domeen?
10. Kuidas on võimalik leviedastusdomeene eraldada? Mis seadmed ei edastada leviedastus sõnumeid?
11. Kuidas töötab Cut-Through Switching?
12. Kuidas töötab Store-And-Forward switching?

# 1. Mis on andmelülikihi üldine ülesanne võrguliikluses? 
Andmelüli kiht vastutab andmete ettevalmistamise eest füüsilise kihi jaoks. Enne kui seade hakkab andmeid üle võrgu saatma, jaotatakse andmed (enamasti IP paketid, nendest hiljem..) Etherneti kaadriteks. 

# 2. Kuidas nimetatakse protokolliandmeüksuseid (PDU) siin tasemel? 
Etherneti kaadriteks. 

# 3. Mis aadresse kasutades suheldakse siin võrgu tasemel? Kirjelda selle aadressi omadusi. 
MAC aadressid Ethernetil põhinevas LAN võrgus on kõik seadmed ühendatud tüüpiliselt ühise kommutaatori (switchi) külge. MAC aadresse kasutatakse, et seadmeid identifitseerida siin võrgu (andmelüli kihi) tasemel. MAC aadress on 6 baidine (48 bitti) mida väljendatakse 12 kuueteistkümnend süsteemi arvuga. Iga toode mis omab võrguliidest peab registreerima IEEE-ga, et saada endale organisatsiooni põhine unikaalne identifikaator. Tootja lisab vastavalt igale tootele ise unikaalse lõpu. 
 
# 4. Millised seadmed (min 2) töötavad sellel kihil? 
Kommutaatorid ja Arvuti 

 # 5. Mis funktsiooni täidab LLC alamkiht? Mis funktsiooni täidab MAC alamkiht? 
see osa, mis kohaldab meediumipöörduse juhtimist ja toetab topoloogiast sõltuvaid funktsioone. 

▫MAC-alamkiht kasutab füüsilise kihi teenuseid ning annab teenuseid loogilise lüli juhtimise alamkihile.

# 6. Kirjelda, mis väljad on ühes ethernet kaadris ning mis nende väljade olulisus/eesmärk on? 
Ethernetis on erinevad aadressid kasutusel ainuedastus(unicast), leviedastus(broadcast) ning multiedastus(multicast) suhtluste jaoks 

# 7. Kirjelda ainuedastus (unicast), leviedastus (broadcast) ning multiedastus (multicast) liikluse erinevusi? Kuidas erinevad iga suhtluse puhul aadressid siin tasemel? 
Ainuedastus (unicast) MAC aadressi kasutatakse kui kaadrit saadetakse ühelt seadmelt teisele siht seadmele. 
 
Leviedastus (broadcast) MAC aadressi kasutatakse kui kaadrit on vaja saata igale seadmele võrgus. Selle omadused on:  
● Selle sihtaadress on alati FF:FF:FF:FF:FF:FF
● See saadetakse välja igast kommutaatori (switch) pordist, v.a kust ta pärines 
● Ruuter sellist sõnumit ei edasta 
 
Multiedastus (multicast) MAC aadressi kasutatakse kui kaadrit saadetakse kindlale grupile (kuid mittekõigile) ühes võrgus. Kasutusel üldiselt teatud ruuteri ning kommutaatori protokollide teenuste poolt. 
 
# 8. Mille abil edastab kommutaator (switch) andmeid? Kuidas ta seda teeb - kirjelda täpsemalt. 
Läbi arvuti võrgukaarti MAC aadresi 
 
Kommunkaator otsustab sihtaadresi põhjal temale saabunud kaadri edastamise. Kui sihtsaadressiks on leviedastus- või multiedastusaadres siis saadetakse kaader kõikidesse portidesse.

# 9. Mis on leviedastus domeen? 
Võrguosa, mis on omavahel ühendatud ainult OSI esimese ja teisi kihi seadmetega. Sellega suhtlevad masinad omavahel otse. 
 
# 10. Kuidas on võimalik leviedastusdomeene eraldada? Mis seadmed ei edastada  leviedastus sõnumeid? 
Eemaldata kolmanda kihi võrguseadmega on võimalik leviedasusdomeene eraldada. 

# 11. Kuidas töötab Cut-Through Switching?
on pakettkommutatsioonisüsteemide meetod, kus kommutaator alustab kaadri (või paketi) edastamist enne kogu kaadri vastuvõtmist, tavaliselt kohe, kui sihtkoha aadress ja väljuv liides on kindlaks määratud. 

# 12. Kuidas töötab Store-And-Forward switching? 
telekommunikatsioonitehnika, mille puhul teave saadetakse vahejaama, kus seda hoitakse ja saadetakse hiljem lõppsihtkohta või teise vahejaama. Vahejaam ehk võrguühenduse kontekstis sõlm kontrollib enne sõnumi edastamist selle terviklikkust. Üldiselt kasutatakse seda tehnikat katkendliku ühendusega võrkudes, eriti kõnnumaal või keskkondades, mis nõuavad suurt liikuvust. 
