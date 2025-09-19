---
# TryHackMe – Wireshark: The Basics  
📡 Premiers pas avec l’analyse réseau via Wireshark

## 📄 Description
Cette room introduit **Wireshark**, un outil d’analyse de paquets réseau permettant d’ouvrir, lire et interpréter des fichiers de capture (PCAP).  
Elle couvre les bases : interface, navigation dans les paquets, filtres d’affichage, suivi de flux, et export d’objets.

## 🎯 Objectifs
- Comprendre les cas d’usage de Wireshark.  
- Apprendre à naviguer entre les paquets et couches OSI.  
- Utiliser les filtres (capture vs display filters).  
- Suivre des conversations réseau (Follow Stream).  
- Exporter des objets (fichiers, flux HTTP).  

## 🛠️ Outils et concepts
- **Wireshark** : outil open-source d’analyse réseau.  
- **PCAP/PCAPNG** : formats de fichiers de capture.  
- **Filtres** :  
  - *Capture filters* (BPF) → appliqués avant capture.  
  - *Display filters* → appliqués après capture.  
- **OSI Layers** : Frame, Ethernet, IP, TCP/UDP, Application.  
- **Follow TCP Stream** : reconstitue la conversation client/serveur.  
- **Export Objects** : récupération des fichiers transférés (HTTP, SMB, etc.).  

## 📚 Résumé du contenu

### 🔹 Introduction
- Wireshark est utilisé pour diagnostiquer des problèmes réseau, analyser des protocoles, ou enquêter sur des intrusions.  
- La room fournit deux fichiers : `http1.pcapng` (démonstrations) et `Exercise.pcapng` (questions).  

### 🔹 Interface
- **Packet List** → résumé des paquets (source, dest, protocole).  
- **Packet Details** → décomposition par couches OSI.  
- **Packet Bytes** → hexadécimal + ASCII.  
- **Display filter bar** → applique des filtres.  

### 🔹 Packet Dissection
- Exemple d’un paquet HTTP :  
  - Frame → infos générales.  
  - Ethernet → MAC src/dst.  
  - IP → adresses src/dst.  
  - TCP → ports, flags, séquence.  
  - Application → HTTP request/response.  

### 🔹 Packet Navigation
- Aller directement à un paquet (`Ctrl+G`).  
- Rechercher (`Ctrl+F`) par texte, hex, ou filtre.  
- Marquer des paquets ou ajouter des commentaires.  
- Exporter : paquets sélectionnés ou objets (HTTP, SMB, etc.).  

### 🔹 Packet Filtering
- **Exemples display filters** :  
  - `http`  
  - `dns`  
  - `ip.addr == 10.10.10.5`  
  - `tcp.port == 80`  
  - `tls`  
  - `frame contains "password"`  
- `Follow TCP Stream` pour reconstituer échanges complets.  

### 🔹 Exercices notables
- Identification du fichier utilisé (`http1.pcapng` / `Exercise.pcapng`).  
- Exemple de filtre appliqué : `http`.  
- Total de paquets affichés dans un filtre : `1089`.  
- Exemple de contenu application : `eXtensible Markup Language`.  

## 📌 Ports et services (observés dans les captures)
- **80/TCP** → HTTP  
- **53/UDP** → DNS  
- **443/TCP** → TLS (mentionné dans le contexte, mais pas analysé en clair ici)  

## ✅ Ce que j’ai appris
- Utiliser Wireshark pour décoder et interpréter des paquets.  
- Différencier **capture filters** et **display filters**.  
- Naviguer efficacement dans une capture avec numéros de paquets, recherche et commentaires.  
- Reconstituer un échange avec **Follow Stream**.  
- Exporter objets (fichiers HTTP) pour analyser les données transmises.  

## 🔑 Mots-clés
Wireshark, PCAP, Packet Analysis, Display Filters, Capture Filters, Follow Stream, HTTP, DNS, TCP/IP, Export Objects  

## 📚 Ressources
- [Wireshark Official Docs](https://www.wireshark.org/docs/)  
- [Wireshark Display Filter Reference](https://www.wireshark.org/docs/dfref/)  
- [TryHackMe Room – Wireshark: The Basics](https://tryhackme.com)  

---
