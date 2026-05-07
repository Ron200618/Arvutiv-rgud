Loo 3 LAN-i:

LAN1: 192.168.1.0/24

LAN2: 192.168.2.0/24

LAN3: 192.168.3.0/24



Teosta järgnevad tulemüüri reeglid:

LAN1:

Luba kõik liiklus internetti
Keela kõik liiklus LAN2 ja LAN3 võrkudesse
LAN2:

Luba ainult HTTPS ja DNS liiklus internetti
Luba ICMP liiklus LAN1, kuid keela kõik muu liiklus LAN1 ja LAN3 võrkudesse.
LAN3:

Keela kõik liiklus internetti
Luba kõik liiklus LAN1 ja LAN2 võrkudesse

# minu osa
LAN1:
● Luba kõik liiklus internetti
● Keela kõik liiklus LAN2 ja LAN3 võrkudesse
<img width="565" height="283" alt="image" src="https://github.com/user-attachments/assets/6f14d165-697b-41f1-b735-f62c04c4ab24" />

LAN2:
● Luba ainult HTTPS ja DNS liiklus internetti
● Luba ICMP liiklus LAN1, kuid keela kõik muu liiklus LAN1 ja LAN3 võrkudesse.
<img width="574" height="164" alt="image" src="https://github.com/user-attachments/assets/fa3aa7a5-a2a9-47fe-8b8f-c67f77334a9c" />


LAN3:
● Keela kõik liiklus internetti
● Luba kõik liiklus LAN1 ja LAN2 võrkudesse
<img width="564" height="107" alt="image" src="https://github.com/user-attachments/assets/fc67ac2a-f6a5-4598-9318-c31cfd4e799d" />
