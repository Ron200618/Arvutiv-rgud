1. Mille eest vastutab transpordi kiht?
2. Mis on TCP ning mida see võimaldab ja tagab? Selgita, millal seda kasutatakse ning too näiteid.
3. Mis on UDP ning kuidas see erineb TCP'st? Selgita, millal seda kasutatakse ning too näiteid.
4. Kirjelda TCP päise informatsiooni, mis on pordi numbrite eesmärk, mis on järjekorra (sequence) numbri eesmärk, mis on kontroll bittide eesmärk, mis on window size jne.
5. Kirjelda UDP päise informatsiooni.
6. Kuidas alustab TCP kahe arvuti vahelist sessiooni? Kirjelda kõik sammud selle loomiseks. Mis üldse on see "sessioon" ning miks see luuakse?
7. Mis on hästi tuntud (well-known), registreeritud ja privaatsete/dünaamiliste portide vahe? Mis vahemikud on defineeritud iga pordi tüübi jaoks?
8. Mille tüüpi rakenduste jaoks on mõeldud järgnevad pordid: 20,21,22,25,67,68,53,80,443

# 1. Mille eest vastutab transpordi kiht? 
Transpordi kiht vastutab selle eest, et paketid liiguksid õigetele rakendustele. Võite ette kujutada, kui palju tuleb ja läheb välja võrgu liiklust ühest võrgus olevast seadmest. Kuidas teab seade millisele rakendusele mis liiklus suunata? Selle eest transpordi kiht hoolitsebki. 
 
# 2. Mis on TCP ning mida see võimaldab ja tagab? Selgita, millal seda kasutatakse ning too näiteid. 
TCP-d peetakse usaldusväärseks, täisfunktsionaalsusega transpordikihi protokolliks, mis tagab kõigi andmete sihtkohta jõudmise. TCP lisab andmetele info, mis tagab andmete kindla kohale toimetamise. 
 
Kasutatakse kui saadetakse andmeid teiselt seadmelt teise. 

# 3. Mis on UDP ning kuidas see erineb TCP'st? Selgita, millal seda kasutatakse ning too näiteid. 
UDP on lihtsam transpordi kihi protokoll kui TCP. See ei paku veakindlust ega voo kontrolli, mis tähendab, et tal on vaja vähem informatsiooni päises. Kuna saatja ja vastuvõtja ei pea terviklikkust tagama, on võimalik UDP datagramme töödelda kiiremini kui TCP segmente. 
 
UDP on ebaturvalisem ja ühenduseta 
TCP on turvaline ja vajab ühendust 

# 4. Kirjelda TCP päise informatsiooni, mis on pordi numbrite eesmärk, mis on järjekorra (sequence) numbri eesmärk, mis on kontroll bittide eesmärk, mis on window size jne. 
 
Porti numbrite eesmärkiks, on, et info jõuaks ilusti kohale ja tervikuna, 
 
32-bitine väli, mida kasutatakse andmete uuesti kokkupanekuks. 

# 5. Kirjelda UDP päise informatsiooni. 

 
6-bitine väli. Sisaldab “koode”, mis kirjeldavad antud segmendi eesmärki. 
 
16-bitine väli. Kasutatakse korraga aktsepteeritavate baitide arvu näitamiseks. 

# 6. Kuidas alustab TCP kahe arvuti vahelist sessiooni? Kirjelda kõik sammud selle loomiseks. Mis üldse on see "sessioon" ning miks see luuakse? 
SYN (Synchronize Sequence Numbers): Host A soovib kinnitada, et host B on suhtlemiseks saadaval ja saadab seetõttu sünkroniseerimis paketi (SYN paketi). See pakett sisaldab üksikasjalikku teavet, nagu näiteks järjestus number, mis on vajalik selleks, et mõlemad osapooled saaksid andmeid korrektselt edastada ja vastu võtta.  
 
SYN, ACK (Synchronize, Acknowledge): Pärast SYN paketi vastu võtmist kontrollib host B oma ressursse ning veendub, et soovitud port on avatud ja võimeline teenust pakkuma. Kui kõik on korras, saadab host B vastuseks SYN-ACK paketi. See pakett kinnitab, et host B on aktiivne, port on avatud, ning ta on valmis alustama andmevahetust host A-ga. Paketis on ka  
oma järjestus number ning kinnitus host A poolt saadetud järjestus numbri kohta. 
 
ACK (Acknowledge): Pärast SYN-ACK paketi saamist saadab host A host B-le kinnituspaketi (ACK paketi). See pakett kinnitab, et host A on saanud host B poolt saadetud järjestus numbri ning on valmis andmevahetuseks. ACK paketi saatmisega lõpetatakse kolmekäiguline käepigistus (Three-Way Handshake), mis tähendab, et mõlemad süsteemid on nüüd valmis andmeid edastama ja vastu võtma antud pordil.	 
See on selleks et andmeid saata omavahel. 

# 7. Mis on hästi tuntud (well-known), registreeritud ja privaatsete/dünaamiliste portide vahe? Mis vahemikud on defineeritud iga pordi tüübi jaoks? 

Vastavalt portide määramise ja kasutamise standarditele (tavaliselt määratletud IANA (Internet Assigned Numbers Authority) poolt). Iga kategooria portide vahemik määratleb, kuidas ja kus neid kasutatakse, sõltuvalt teenuse või protokolli vajadustest. 

 

HTTP (veebiteenus) – Port 80 

HTTPS (turvaline veebiteenus) – Port 443 

FTP (failiedastus) – Port 21 

SSH (secure shell) – Port 22 

DNS (domeeninimede süsteem) – Port 53 

# 8. Mille tüüpi rakenduste jaoks on mõeldud järgnevad pordid: 20,21,22,25,67,68,53,80,443 

Port 20 
FTP Data (protocol)
Andmeedastus FTP kaudu (Kasutus)


Port 21 
FTP Command (protocol)
FTP juhtimine (Kasutus)


Port 22 
SSH (protocol)
Turvaline kaugjuurdepääs (Kasutus)


Port 25 
SMTP (protocol)
E-posti saatmine (Kasutus)


Port 67 
DHCP Server (protocol)
IP aadresside automaatne määramine (Kasutus)


Port 68 
DHCP Client (protocol)
DHCP serverilt IP aadressi saamine (Kasutus)


Port 53 
DNS (protocol)
Domeeninimede tõlkimine IP aadressideks (Kasutus)


Port 80 
HTTP (protocol)
Veebilehtede sirvimine (Kasutus)


Port 443 
HTTPS (protocol)
Turvaline veebisirvimine (Kasutus)
