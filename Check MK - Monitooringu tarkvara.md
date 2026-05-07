# Sissejuhatus: Mis on Checkmk ja milleks seda vaja on?

Mis on Checkmk?

Checkmk on üks maailma juhtivaid IT-taristu monitooringu (seire) lahendusi. See on tarkvara, mis töötab nagu süsteemiadministraatori "silmad ja kõrvad", jälgides ööpäevaringselt servereid, võrguseadmeid, rakendusi ja pilveteenuseid.

Checkmk koosneb kahest poolest:

Server: Kogub andmeid, analüüsib neid ja saadab häireid (Alerts).
Agent: Väike programm, mis paigaldatakse jälgitavasse masinasse (nt Linux või Windows server) ja mis saadab serverile infot (CPU kasutus, ketta maht, töötavad teenused).
Milleks on monitooringut vaja? (Eesmärgid)

Ilma monitooringuta tegutseb IT-osakond "pimeda juhina" – probleemidest saadakse teada alles siis, kui kasutajad hakkavad kaebama, et "internet on maas" või "koduleht ei tööta".

Checkmk kasutamise peamised eesmärgid on:

Proaktiivsus (Ennetamine):
Eesmärk on tuvastada probleemid enne, kui need muutuvad kriitiliseks.
Näide: Checkmk saadab hoiatuse, kui kõvaketas on 90% täis. Administraator jõuab ruumi vabastada enne, kui server seisma jääb.
Käideldavuse tagamine (Uptime):
Me peame teadma hetkega, kui mõni kriitiline teenus (nagu Nginx veebiserver või MariaDB andmebaas) lakkab töötamast, et see koheselt taaskäivitada.
Ressursiplaneerimine (Capacity Planning):
Checkmk joonistab graafikuid ajalooliste andmete põhjal.
Näide: Sa näed, et veebiserveri koormus kasvab igal kuul 10%. See aitab otsustada, millal on vaja lisada rohkem RAM-i või protsessorivõimsust.
Tsentraliseeritud ülevaade:
Selle asemel, et logida sisse kümnesse erinevasse serverisse ja kontrollida neid käsurealt (htop, df -h), näeb administraator kogu infra tervist ühel töölaual (Dashboard).
Miks me monitoorime Nginxi ja MariaDB-d?

Selles laboris paigaldame Checkmk agendi, et jälgida kahte konkreetset teenust:

Nginx: Meid huvitab mitte ainult see, kas protsess töötab, vaid ka see, kui palju päringuid (Requests per Second) see teenindab ja kas esineb veateateid.
MariaDB: Me tahame teada, kas andmebaas on kättesaadav, kui palju on aktiivseid ühendusi ja ega päringud pole liiga aeglased.

# Ülesanne:

1. Paigalda ubuntu virtuaalmasinale Check MK free/trial edition. OS põhine paigaldusjuhend asub lingil.

2. Paigalda eraldi ubuntu serverile Nginx ning MariaDB teenused.

3. Kasuta antud CheckMK juhendit, et lisada teenused monitooringu alla.


<img width="567" height="321" alt="image" src="https://github.com/user-attachments/assets/a2301db0-f5f2-440b-9806-4727001118d8" />

<img width="574" height="409" alt="image" src="https://github.com/user-attachments/assets/18ae97fb-486b-4a16-884f-5ec441bd73fa" />

<img width="566" height="500" alt="image" src="https://github.com/user-attachments/assets/493792f9-c11a-4508-832a-71124d6ce21b" />

<img width="567" height="555" alt="image" src="https://github.com/user-attachments/assets/3e7a6310-d220-481a-89e0-7b2979b684ad" />

<img width="570" height="434" alt="image" src="https://github.com/user-attachments/assets/b3e9edec-e970-49e1-b93c-e4c5c3185438" />
