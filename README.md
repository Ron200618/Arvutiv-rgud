# Arvutivõrgud — Portfolio

Kogumik arvutivõrkude kursuse/laborite materjale (dokumentatsioon + vastused + ekraanipildid). Fookus on OSI mudeli mõistmisel ja praktilisel võrguteenuste seadistamisel, eelkõige **pfSense**, **Checkmk**, **Graylog** ja **Ansible** abil.

## Mida see repo sisaldab?

### 1) Teooria: OSI mudel (kordamine)
- **Füüsiline kiht (L1):** bittide edastus meediumil, signaalimine, ribalaius vs kiirus, latentsus, throughput, IEEE standardid (802.3/802.11), T568A/T568B.
- **Andmelüli kiht (L2):** Ethernet kaadrid, **MAC-aadressid**, unicast/broadcast/multicast, switchi töö (MAC tabel), cut-through vs store-and-forward, broadcast domeen.
- **Võrgukiht (L3):** **IPv4**, paketipäis (src/dst, TTL, checksum, protocol), **MTU**, unicast/multicast/broadcast aadressid, **NAT**, default gateway, ARP, marsruutimistabelid (staatiline vs dünaamiline).
- **Transpordikiht (L4):** **TCP vs UDP**, TCP sessiooni loomine (3-way handshake), portide vahemikud ja tuntud pordid (nt 22/53/80/443).
- **Sessiooni/Esitus/Rakendus (L5–L7):** sessioonihaldus, andmete vormindus/krüpto/tihendus, rakendusprotokollide roll.

### 2) Praktika: pfSense (tulemüür, NAT, DHCP, VPN)
- **Tulemüüri reeglid mitmes LAN-is:** erinevate võrkude interneti/teenuste lubamine-keelamine (HTTP/HTTPS, ICMP, SSH) ja segmentimine.
- **Sisu blokeerimine:** näited, kuidas piirata ligipääsu (nt Facebook/Youtube) ja lubada ainult kindlat saiti.
- **Port forwarding / NAT:** avaliku aadressi kaudu sisemise veebiserveri kättesaadavaks tegemine.
- **Võrkude vaheline suhtlus:** 3 LAN-i reeglistik, mis lubab/keelab liiklust võrkude vahel.
- **DHCP:** erinevad alamvõrgud, DHCP vahemike planeerimine, erandid ning **staatilised DHCP liisingud**.
- **IPsec site-to-site tunnel:** kahe võrgu ühendamine krüpteeritud tunneliga.

### 3) Monitooring: Checkmk
- **Checkmk server + agent:** infrastruktuuri monitoorimine (ressursid, teenused, uptime, trendid).
- **Teenuste monitooring:** näited Nginx ja MariaDB jälgimisest.
- **pfSense monitooring SNMP abil:** SNMP teenuse lubamine, vajalikud pordid (UDP/161, UDP/162) ja hosti lisamine Checkmk-s.

### 4) Logihaldus / SIEM: Graylog
- **Tsentraliseeritud logide kogumine:** logid Linuxi serveritest ja pfSense’ist ühte kohta.
- **Miks kasulik:** kiirem tõrkeotsing, parem nähtavus ja turvasündmuste avastamine (nt ebaõnnestunud sisselogimised, tulemüüri blokeeringud).

### 5) Automatiseerimine: Ansible
- Näited Ansible seadistustest ja mõistetest (nt `host_key_checking = False`), eesmärgiga muuta administreerimine automatiseerituks.
- Masshalduse idee: koguda/luua ühtne ülevaade hostidest ja kasutada seda automatiseerimisel.

### 6) Kaablid ja tööriistad
- Ülevaade võrgukaablitest (keerdpaar, koaksiaal, fiiber), nende kasutusaladest ja plussidest/miinustest.
- RJ45/keystone valik ning tööriistad (krimpimistangid, kaablikoorija, punch-down, testijad) + testimise põhimõtted.

## Miks see on kasulik?
- **Õppimiseks ja kordamiseks:** OSI mudeli ning põhiprotokollide (Ethernet, IPv4, TCP/UDP, ARP, NAT) kiireks meenutamiseks.
- **Praktiline „hands-on” kogemus:** tulemüüri reeglid, segmentimine, DHCP, NAT/port forwarding ja IPsec on tüüpilised reaalse võrgu teemad.
- **Ops töövoog:** monitooring (Checkmk) + logihaldus (Graylog) annavad hea baasi IT-taristu halduseks ja probleemide ennetamiseks.
- **Automatiseerimine:** Ansible vähendab käsitööd ning aitab skaleerida haldust.

## Tehnoloogiad / märksõnad
**pfSense, Firewall rules, NAT, Port Forwarding, DHCP, IPsec VPN, SNMP, Checkmk, Graylog, Ansible, OSI model, Ethernet, IPv4, TCP/UDP**

---

> Märkus: Repo sisaldab palju ekraanipilte ja kursuseülesannete dokumentatsiooni. See README on kokkuvõte/„portfolio” vaade, et oleks kiirelt arusaadav, mida siin tehti ja mida see näitab.
