# Arvutivõrgud — portfoolio

Kogumik arvutivõrkude kursuse/laborite materjale (dokumentatsioon + vastused + ekraanipildid). Fookus on OSI mudeli mõistmisel ja praktilisel võrguteenuste seadistamisel, eelkõige **pfSense**, **Checkmk**, **Graylog** ja **Ansible** abil.

## Mida see repositoorium sisaldab?

### 1) Teooria: OSI mudel (kordamine)
- **Füüsiline kiht (L1):** bittide edastus meediumil, signaalimine, ribalaius vs kiirus, latentsus, läbilaskevõime (throughput), IEEE standardid (802.3/802.11), T568A/T568B.
- **Andmelüli kiht (L2):** Etherneti kaadrid, **MAC-aadressid**, ainuedastus/leviedastus/multiedastus, lüliti (switch) töö (MAC-tabel), cut-through vs store-and-forward, leviedastus-domeen.
- **Võrgukiht (L3):** **IPv4**, paketipäis (lähte-/sihtaadress, TTL, kontrollsumma, protokoll), **MTU**, unicast/multicast/broadcast aadressid, **NAT**, vaikelüüs (default gateway), ARP, marsruutimistabelid (staatiline vs dünaamiline).
- **Transpordikiht (L4):** **TCP vs UDP**, TCP sessiooni loomine (3-sammuline „handshake”), portide vahemikud ja tuntud pordid (nt 22/53/80/443).
- **Sessiooni-/esitus-/rakenduskiht (L5–L7):** sessioonihaldus, andmete vormindus/krüpto/tihendus, rakendusprotokollide roll.

### 2) Praktika: pfSense (tulemüür, NAT, DHCP, VPN)
- **Tulemüüri reeglid mitmes LAN-is:** erinevate võrkude interneti/teenuste lubamine-keelamine (HTTP/HTTPS, ICMP, SSH) ja segmentimine.
- **Sisu blokeerimine:** näited, kuidas piirata ligipääsu (nt Facebook/Youtube) ja lubada ainult kindlat saiti.
- **Portide suunamine / NAT:** avaliku aadressi kaudu sisemise veebiserveri kättesaadavaks tegemine.
- **Võrkude vaheline suhtlus:** 3 LAN-i reeglistik, mis lubab/keelab liiklust võrkude vahel.
- **DHCP:** erinevad alamvõrgud, DHCP vahemike planeerimine, erandid ning **staatilised DHCP liisingud**.
- **IPsec site-to-site tunnel:** kahe võrgu ühendamine krüpteeritud tunneliga.

### 3) Monitooring: Checkmk
- **Checkmk server + agent:** infrastruktuuri monitoorimine (ressursid, teenused, käideldavus/uptime, trendid).
- **Teenuste monitooring:** näited Nginx’i ja MariaDB jälgimisest.
- **pfSense monitooring SNMP abil:** SNMP teenuse lubamine, vajalikud pordid (UDP/161, UDP/162) ja hosti lisamine Checkmk-s.

### 4) Logihaldus / SIEM: Graylog
- **Tsentraliseeritud logide kogumine:** logid Linuxi serveritest ja pfSense’ist ühte kohta.
- **Miks kasulik:** kiirem tõrkeotsing, parem nähtavus ja turvasündmuste avastamine (nt ebaõnnestunud sisselogimised, tulemüüri blokeeringud).

### 5) Automatiseerimine: Ansible
- Näited Ansible seadistustest ja mõistetest (nt `host_key_checking = False`), eesmärgiga muuta administreerimine automatiseerituks.
- Masshalduse idee: koguda/luua ühtne ülevaade hostidest ja kasutada seda automatiseerimisel.

### 6) Kaablid ja tööriistad
- Ülevaade võrgukaablitest (keerdpaar, koaksiaal, fiiberoptiline), nende kasutusaladest ja plussidest/miinustest.
- RJ45/keystone valik ning tööriistad (krimpimistangid, kaablikoorija, punch-down tööriist, testijad) + testimise põhimõtted.

## Miks see on kasulik?
- **Õppimiseks ja kordamiseks:** OSI mudeli ning põhiprotokollide (Ethernet, IPv4, TCP/UDP, ARP, NAT) kiireks meenutamiseks.
- **Praktiline „hands-on” kogemus:** tulemüüri reeglid, segmentimine, DHCP, NAT/portide suunamine ja IPsec on tüüpilised päris võrgu teemad.
- **Ops töövoog:** monitooring (Checkmk) + logihaldus (Graylog) annavad hea baasi IT-taristu halduseks ja probleemide ennetamiseks.
- **Automatiseerimine:** Ansible vähendab käsitööd ning aitab skaleerida haldust.

## Tehnoloogiad / märksõnad
**pfSense, tulemüüri reeglid, NAT, portide suunamine, DHCP, IPsec VPN, SNMP, Checkmk, Graylog, Ansible, OSI mudel, Ethernet, IPv4, TCP/UDP**

---

> Märkus: Repo sisaldab palju ekraanipilte ja kursuseülesannete dokumentatsiooni. See README on kokkuvõttev „portfoolio” vaade, et oleks kiiresti arusaadav, mida siin tehti ja miks see oluline on.
