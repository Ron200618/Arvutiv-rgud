Graylog
Logi on organisatsiooni süsteemides ja võrkudes toimuvate sündmuste kirje. Logid koosnevad sissekannetest ja iga sissekanne sisaldab infot kindla sündmuse kohta, mis on toimunud süsteemis või võrgus. Algselt kasutati logisid peamiselt vigade leidmiseks. Praegu on logidel organisatsioonis mitmeid funktsioone. Näiteks võrgu ja süsteemi jõudluse parandamine, kasutajate tegevuste salvestamine ja kasulike andmete edastamine pahatahtliku tegevuse uurimisel.
 
Keskne logihaldus tähendab mitmest seadmest logide kogumist ühte kesksesse masinasse. Tulemusena säästetakse administraatori aega, sest ei pea igast masinast eraldi logisid otsima, vaid saab logiserverist kõigi kohta teabe kätte. Lihtsam on teha ka saadud sündmuste põhjal analüüsi.

# Eesmärk: Luua tsentraliseeritud logihalduslahendus, mis kogub sündmuste kirjeid erinevat tüüpi seadmetest. 

# Sissejuhatus: Miks on logihaldus vajalik? 
Logi on organisatsiooni süsteemides ja võrkudes toimuvate sündmuste kirje. Logid koosnevad sissekannetest ja iga sissekanne sisaldab infot kindla sündmuse kohta, mis on toimunud süsteemis või võrgus. 
Tänapäeval on logidel mitu kriitilist funktsiooni: 
Vigade leidmine: Algne ja peamine kasutusala süsteemirikete diagnoosimiseks. 
Jõudluse parandamine: Võrgu ja süsteemi pudelikaelade tuvastamine. 
Turvalisus: Kasulike andmete edastamine pahatahtliku tegevuse uurimisel ja kasutajate tegevuste salvestamine. 
Keskne logihaldus tähendab logide kogumist mitmest seadmest ühte kesksesse masinasse. See säästab administraatori aega, sest teavet ei pea otsima igast masinast eraldi, ning võimaldab teostada sündmuste põhjal põhjalikku analüüsi. 

# lõõ´pp tulemus
Selle laboritöö käigus loodi edukalt tsentraliseeritud logihaldussüsteem (SIEM). 
Tulemus: Kõik olulised võrguseadmed (Linuxi serverid ja pfSense tulemüür) saadavad oma logid ühte kesksesse punkti (Graylog). 
Kasu: See võimaldab administraatoril saada reaalajas ülevaate võrgus toimuvast, tuvastada kiiresti turvaintsidente (nt ebaõnnestunud sisselogimised või tulemüüri blokeeringud) ja hoida kokku aega, vältides vajadust logida igasse seadmesse eraldi. 

<img width="572" height="447" alt="image" src="https://github.com/user-attachments/assets/60ad6352-f69a-43fa-850b-147ab8ba6021" />

<img width="570" height="416" alt="image" src="https://github.com/user-attachments/assets/16f4b2f3-fe24-44bf-a8d5-e2c812504ba7" />

<img width="569" height="94" alt="image" src="https://github.com/user-attachments/assets/62d93ad4-9a5f-4380-98e4-a594ae3ca209" />

<img width="595" height="525" alt="image" src="https://github.com/user-attachments/assets/a1a512b8-f8f3-4724-b930-3e88b81499d5" />
LINUXISE SUUNAMINE
<img width="565" height="369" alt="image" src="https://github.com/user-attachments/assets/329522da-ec60-4fe3-a673-7fd64fa2f8bb" />

<img width="582" height="473" alt="image" src="https://github.com/user-attachments/assets/5620573d-013c-4e6e-a6d6-2531f999810c" />

