# TryHackMe – Networking Concepts  
🌐 Bases essentielles des réseaux et protocoles

---

## 📄 Description
Cette room introduit les concepts fondamentaux du réseau, les modèles OSI et TCP/IP, ainsi que les protocoles essentiels comme TCP, UDP et Telnet. Elle pose les bases nécessaires pour comprendre comment les appareils communiquent sur un réseau et comment les paquets circulent.

---

## 🎯 Objectifs
- Comprendre le modèle **OSI** et ses 7 couches.  
- Découvrir le modèle **TCP/IP** et ses différences avec OSI.  
- Maîtriser les notions d’**adresses IP, sous-réseaux et routage**.  
- Comprendre les protocoles **TCP** (fiable) et **UDP** (rapide).  
- Explorer le concept d’**encapsulation des données**.  
- Expérimenter l’utilisation de **Telnet** pour interagir avec des services distants.

---

## 🛠️ Outils et concepts
- **OSI Model** : structure en 7 couches (physique → application).  
- **TCP/IP Model** : modèle en 4 couches (Link, Internet, Transport, Application).  
- **IP Addressing & Subnets** : IPv4, classes d’adresses, public vs privé, routage.  
- **TCP vs UDP** : 3-way handshake, fiabilité vs rapidité.  
- **Encapsulation** : ajout d’en-têtes (headers) à chaque couche réseau.  
- **Telnet** : protocole pour tester des connexions TCP.  

---

## 📚 Résumé du contenu

### 🔹 OSI Model
- **7 couches** :  
  1. Physique → Transmission des signaux  
  2. Data Link → MAC address, Ethernet, Wi-Fi  
  3. Réseau → Routage IP, ICMP  
  4. Transport → TCP, UDP, segmentation, contrôle des erreurs  
  5. Session → Gestion des connexions  
  6. Présentation → Encodage, chiffrement, compression  
  7. Application → Interfaces utilisateur (HTTP, SMTP, DNS…)

---

### 🔹 TCP/IP Model
- Plus **pratique et simplifié** → 4 couches.  
- Correspondance avec OSI :  
  - Application (couche 7,6,5 d’OSI)  
  - Transport (couche 4 d’OSI)  
  - Internet (couche 3 d’OSI)  
  - Link (couche 2 et 1 d’OSI)  

---

### 🔹 IP Addresses & Subnets
- **IPv4** = 4 octets → ex: `192.168.1.1`  
- **Privées** : 10.0.0.0/8, 172.16.0.0/12, 192.168.0.0/16  
- **Publiques** : utilisées sur Internet.  
- **Routage** : les routeurs transmettent les paquets vers la bonne destination.

---

### 🔹 TCP vs UDP
- **TCP** : fiable, utilise le 3-way handshake (SYN → SYN-ACK → ACK).  
- **UDP** : non-fiable, plus rapide, pas de confirmation (streaming, DNS, VoIP).  
- **Ports** : 1 → 65535 (0 réservé).  

---

### 🔹 Encapsulation
- Application Data → ajout d’un header transport (**TCP segment / UDP datagram**).  
- Ajout d’un header réseau (**IP packet**).  
- Ajout d’un header + trailer de la couche liaison (**Ethernet frame**).  
- Processus inversé à la réception.  

---

### 🔹 Telnet
- Permet de se connecter à un service via **TCP**.  
- Exemples :  
  - Port 7 → Echo server  
  - Port 13 → Daytime server (date et heure)  
  - Port 80 → HTTP (GET request)  

---

## 📌 Ports et services
- **7** : Echo  
- **13** : Daytime  
- **80** : HTTP (via Telnet)  
- **TCP** : fiable (handshake)  
- **UDP** : rapide (pas de handshake)  

---

## ✅ Ce que j’ai appris
- Différencier **OSI** et **TCP/IP** et comprendre leur utilité.  
- Identifier et classer les **adresses IP privées et publiques**.  
- Comprendre les **ports TCP/UDP** et leurs usages.  
- Expliquer le **3-way handshake** de TCP.  
- Visualiser l’**encapsulation** d’un paquet réseau.  
- Utiliser **Telnet** pour interagir avec des services simples.  

---

## 🔑 Mots-clés
OSI, TCP/IP, IP Address, Subnet, Routing, TCP, UDP, Ports, Encapsulation, Telnet  

---

## 📚 Ressources
- [RFC 1122 – Requirements for Internet Hosts](https://www.rfc-editor.org/rfc/rfc1122)  
- [RFC 791 – Internet Protocol (IPv4)](https://www.rfc-editor.org/rfc/rfc791)  
- [OSI Model Explained](https://www.cloudflare.com/learning/ddos/glossary/open-systems-interconnection-model-osi/)  
- [TCP vs UDP](https://www.imperva.com/learn/application-security/tcp-vs-udp/)  
