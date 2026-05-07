Ülesandeks on monitoorida pfSense ruuterit läbi SNMP protokolli. Dokumenteeri tehtud seadistused.

Soorita järgnevad tegevused:

1. Paigalda pfSense ruuterile check_mk agent (https://github.com/albertfont/checkmk_agent_pfsense)

2. Käivita pfSense ruuteris SNMP teenus. Services -> SNMP -> Enable

3. Luba tulemüüris WAN liidesel sisse tulevad UDP/161 ning UDP/162 ühendused. Luba ka WAN liidesel pingimine. Seda sammu ei peaks tegema kui teie monitooringu server asuks ruuteri LAN võrgus.

4. Check_mk haldusliideses lisa host ning luba SNMP koos selle parooliga. Pärast ühenduste testimist lisa kõik tuvastatud teenused monitooringu alla.

5. Testi töötamist. Ülesande vastusena lae dokumentatsioon ning tõestus töötavast lahendusest (näed kõikide teenuste/liideste kohta infot check_mk haldusliideses)

<img width="566" height="678" alt="image" src="https://github.com/user-attachments/assets/66583980-6468-43ab-8724-79b5e3d29ba3" />

<img width="567" height="445" alt="image" src="https://github.com/user-attachments/assets/299efd16-3b77-4505-a4d0-0d1d465d0672" />

<img width="570" height="804" alt="image" src="https://github.com/user-attachments/assets/c23ead93-4c99-4ddb-a7b5-4636bbc12abb" />

<img width="570" height="772" alt="image" src="https://github.com/user-attachments/assets/d5ef5ad2-0721-47b3-8a7c-585acf7c3a08" />
