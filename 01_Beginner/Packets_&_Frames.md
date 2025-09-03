# TryHackMe - Packets and Frames

## 📄 Description
Cette room explique la différence entre un **packet** et une **frame** dans le modèle OSI, ainsi que le rôle des protocoles TCP et UDP pour la communication entre appareils.  
Elle couvre également le fonctionnement du **TCP Three-Way Handshake**, la gestion des **ports**, et inclut plusieurs exercices pratiques.

---

## 🎯 Objectifs
- Comprendre la différence entre un **packet** et une **frame**.
- Connaître la structure et le rôle des en-têtes réseau.
- Comprendre le fonctionnement de **TCP** et de son *three-way handshake*.
- Découvrir **UDP** et ses différences avec TCP.
- Comprendre l’utilisation et la gestion des **ports**.
- Mettre en pratique avec des exercices interactifs.

---

## 🛠️ Outils et concepts
- **Packet** : unité de données au niveau *Layer 3 – Network* avec en-tête IP.
- **Frame** : unité de données au niveau *Layer 2 – Data Link* contenant des informations comme l’adresse MAC.
- **Encapsulation** : ajout d’informations (en-têtes) lors de la transmission des données.
- **TCP (Transmission Control Protocol)** : protocole orienté connexion, fiable, utilisant un *three-way handshake* (SYN, SYN/ACK, ACK).
- **UDP (User Datagram Protocol)** : protocole sans connexion (*stateless*), plus rapide mais moins fiable.
- **Ports** : points d’accès numériques permettant d’identifier les applications/services (ex. HTTP → 80, HTTPS → 443, SSH → 22).

---

## 📌 Résumé du contenu

### **Packets et Frames**
- Un **packet** contient l’adresse IP source et destination, et est utilisé au niveau *Layer 3 (Network)*.
- Une **frame** encapsule un packet avec des infos de niveau *Layer 2 (Data Link)*, comme l’adresse MAC.
- Analogie : le packet = lettre, la frame = enveloppe.
- Exemples de champs dans un packet : TTL (Time to Live), Checksum, Source/Destination Address.

---

### **TCP – Transmission Control Protocol**
- Protocole fiable, orienté connexion.
- Nécessite un **three-way handshake** :
  1. **SYN** : demande de connexion.
  2. **SYN/ACK** : confirmation et synchronisation.
  3. **ACK** : validation finale.
- Avantages : fiabilité, retransmission des données perdues.
- Inconvénients : plus lent, plus consommateur de ressources.
- Clôture de connexion via **FIN/ACK**.

---

### **UDP – User Datagram Protocol**
- Protocole *stateless* (pas d’établissement de connexion).
- Avantages : rapidité, moins de surcharge.
- Inconvénients : aucune garantie de livraison, pertes possibles.
- Utilisé pour : streaming, VoIP, jeux en ligne.

---

### **Ports**
- Identifient les services ou applications sur un appareil.
- **Common ports** (0–1024) :
  - 21 : FTP  
  - 22 : SSH  
  - 80 : HTTP  
  - 443 : HTTPS  
  - 445 : SMB  
  - 3389 : RDP
- Les ports permettent à plusieurs services de fonctionner sur une même machine.

---

## 📚 Ce que j’ai appris
- Différence entre **packet** et **frame** et leur rôle dans le modèle OSI.
- Fonctionnement de l’**encapsulation** des données.
- Mécanisme du **TCP Three-Way Handshake** et son importance.
- Cas d’usage et limites d’**UDP** comparé à TCP.
- Rôle des **ports** dans la communication réseau et principaux ports utilisés.
- Utilisation pratique des concepts via les exercices (TCP handshake, connexion à un port).

---

_Room complétée le : 03/09/2025_
