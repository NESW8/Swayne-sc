# TryHackMe – Networking Essentials  
📡 Comprendre les protocoles fondamentaux qui assurent la connectivité réseau au quotidien

---

## 📄 Description
Cette room explore les protocoles et mécanismes essentiels qui permettent aux ordinateurs et périphériques de communiquer sur un réseau.  
On y découvre le rôle de **DHCP, ARP, ICMP, le routage, NAT** ainsi que des démonstrations pratiques avec `ping`, `traceroute` et `telnet`.

---

## 🎯 Objectifs
- Comprendre le fonctionnement du protocole DHCP et son processus DORA.  
- Identifier l’importance d’ARP dans la résolution des adresses IP vers MAC.  
- Utiliser ICMP pour diagnostiquer les problèmes de connectivité.  
- Découvrir les bases du routage et des protocoles courants (OSPF, BGP, RIP, EIGRP).  
- Comprendre le rôle du NAT dans l’accès Internet des réseaux privés.  
- Manipuler des services simples via **telnet** pour illustrer les échanges TCP.

---

## 🛠️ Outils et concepts
- **DHCP (Dynamic Host Configuration Protocol)** : attribution automatique d’adresses IP.  
- **ARP (Address Resolution Protocol)** : correspondance entre IP et adresse MAC.  
- **ICMP (Internet Control Message Protocol)** : diagnostic via `ping` et `traceroute`.  
- **Routage** : acheminement des paquets via des protocoles comme OSPF, BGP, RIP, EIGRP.  
- **NAT (Network Address Translation)** : traduction des IP privées vers une IP publique.  
- **Telnet** : client TCP basique, utilisé ici pour illustrer des connexions manuelles.  
- **Outils CLI** : `ping`, `traceroute`, `tcpdump`, `tshark`, `arp`, `telnet`.

---

## 📚 Résumé du contenu

### 🔹 DHCP : automatisation des adresses
- Processus **DORA** : Discover → Offer → Request → Acknowledge.  
- Le client démarre en envoyant une requête en broadcast (`255.255.255.255`).  
- Le serveur attribue une IP, un masque de sous-réseau, une passerelle et un DNS.

### 🔹 ARP : liaison entre IP et MAC
- Permet de retrouver l’adresse MAC d’une machine connaissant son IP.  
- Requête ARP envoyée en broadcast (`ff:ff:ff:ff:ff:ff`), réponse en unicast.  
- Exemple : IP `192.168.66.1` correspond à MAC `44:df:65:d8:fe:6c`.

### 🔹 ICMP : diagnostic
- `ping` : envoi d’**Echo Request** et réception d’**Echo Reply**.  
- `traceroute` : découverte des routeurs intermédiaires via la valeur TTL.  
- Exemple : 40 octets envoyés, affichage du RTT (min/avg/max).

### 🔹 Routage
- Protocoles rencontrés :  
  - **OSPF** : open standard, calcule le chemin le plus court.  
  - **EIGRP** : propriétaire Cisco.  
  - **BGP** : utilisé pour l’interconnexion des réseaux Internet.  
  - **RIP** : ancien protocole basé sur le nombre de sauts.

### 🔹 NAT : accès Internet
- Traduction d’adresses internes vers une IP publique unique.  
- Exemple : `192.168.0.129:15401` → `212.3.4.5:19273`.  
- Permet à des milliers d’utilisateurs de partager une seule IP publique.

### 🔹 Telnet : interactions TCP manuelles
- Utilisé pour se connecter à des services simples :  
  - Port 7 (echo)  
  - Port 13 (daytime)  
  - Port 80 (HTTP avec envoi manuel d’une requête GET).  
- Exemple observé : serveur `lighttpd/1.4.63`, flag récupéré `THM{TELNET_MASTER}`.

---

## 📌 Ports et services
- **67/68 (UDP)** : DHCP.  
- **ARP** : sans port (couche 2).  
- **ICMP** : sans port (couche 3).  
- **7/TCP** : Echo.  
- **13/TCP** : Daytime.  
- **80/TCP** : HTTP (test avec Telnet).

---

## ✅ Ce que j’ai appris
- Le DHCP évite la configuration manuelle et simplifie l’accès réseau.  
- ARP est indispensable pour que les machines puissent communiquer sur un LAN.  
- ICMP (`ping`, `traceroute`) est fondamental pour diagnostiquer la connectivité.  
- Le routage est la clé de l’interconnexion entre réseaux locaux et Internet.  
- Le NAT permet l’économie d’adresses IPv4 et la connectivité d’énormes réseaux privés.  
- `telnet` reste utile en démonstration pour visualiser des échanges TCP bruts.  

---

## 🔑 Mots-clés
DHCP, ARP, ICMP, NAT, OSPF, BGP, RIP, EIGRP, ping, traceroute, telnet, routage, TCP/IP, réseau

---

## 📚 Ressources
- [RFC 2131 – DHCP](https://datatracker.ietf.org/doc/html/rfc2131)  
- [RFC 826 – ARP](https://datatracker.ietf.org/doc/html/rfc826)  
- [RFC 792 – ICMP](https://datatracker.ietf.org/doc/html/rfc792)  
- [Introduction au routage – Cisco](https://www.cisco.com/c/en/us/solutions/enterprise-networks/what-is-routing.html)  
- [Documentation Wireshark](https://www.wireshark.org/docs/)  

---
