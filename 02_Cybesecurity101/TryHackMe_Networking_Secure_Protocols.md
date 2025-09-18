---
# TryHackMe – Networking Secure Protocols  
🔒 Sécurisation des communications réseau avec TLS, SSH et VPN

## 📄 Description
Cette room explique comment sécuriser les protocoles réseaux de base vus précédemment (HTTP, SMTP, POP3, IMAP, FTP, Telnet).  
Elle met en avant l’utilisation de **TLS/SSL**, de **SSH** et des **VPN** pour garantir la confidentialité, l’intégrité et l’authenticité des communications.

## 🎯 Objectifs
- Comprendre le rôle de TLS et des certificats.  
- Apprendre la différence entre protocoles en clair (HTTP, FTP, SMTP…) et leurs versions sécurisées (HTTPS, FTPS, SMTPS…).  
- Découvrir SSH comme remplacement sécurisé de Telnet.  
- Comprendre l’usage des tunnels SSH et VPN pour protéger le trafic.  
- Observer le chiffrement réseau avec Wireshark.  

## 🛠️ Outils et concepts
- **TLS (Transport Layer Security)** : chiffrement des communications, héritier de SSL.  
- **Certificats & CA** : rôle des autorités de certification pour vérifier l’authenticité.  
- **HTTPS, SMTPS, POP3S, IMAPS** : versions sécurisées des protocoles.  
- **SSH** : connexion distante sécurisée (port 22), authentification par mot de passe ou clé publique.  
- **SFTP & FTPS** : transferts de fichiers sécurisés.  
- **VPN (Virtual Private Network)** : tunnels chiffrés reliant réseaux distants.  
- **Wireshark** : observation du trafic chiffré et déchiffré avec clés SSL.

## 📚 Résumé du contenu

### 🔹 TLS et Certificats
- TLS succède à SSL.  
- Garantit confidentialité, intégrité, authenticité.  
- Certificats émis par une **CA** (Certificate Authority).  
- ⚠️ Les certificats auto-signés ne prouvent pas l’authenticité.  

### 🔹 HTTPS
- HTTP sur port **443/TCP** avec TLS.  
- Processus : **handshake TCP → handshake TLS → échange de données chiffrées**.  
- Le contenu est illisible sans la clé privée (contrairement à HTTP).  

### 🔹 SMTPS, POP3S, IMAPS
- Ajout de TLS aux protocoles mail :  
  - SMTPS → ports 465 / 587.  
  - POP3S → port 995.  
  - IMAPS → port 993.  
- Empêchent la récupération des identifiants en clair.  

### 🔹 SSH
- Remplace **Telnet (port 23)** par **SSH (port 22)**.  
- Fonctionnalités :  
  - Authentification par clé publique.  
  - Tunnel chiffré pour applications (ex : X11 forwarding).  
  - Intégrité et confidentialité des sessions.  

### 🔹 SFTP et FTPS
- **SFTP** → s’appuie sur SSH (port 22).  
- **FTPS** → utilise TLS (port 990 généralement).  
- ⚠️ À ne pas confondre : même objectif (transfert sécurisé), mais implémentation différente.  

### 🔹 VPN
- Crée un tunnel sécurisé entre plusieurs sites distants.  
- Le trafic passe dans le tunnel chiffré, protégé de l’interception.  
- Permet aussi de masquer l’IP publique réelle (ex : accès depuis un autre pays).  

## 📌 Ports et services
- **443/TCP** → HTTPS  
- **465, 587/TCP** → SMTPS  
- **995/TCP** → POP3S  
- **993/TCP** → IMAPS  
- **22/TCP** → SSH / SFTP  
- **990/TCP** → FTPS  

## ✅ Ce que j’ai appris
- Différence entre protocoles en clair et sécurisés.  
- TLS est le standard actuel pour sécuriser les échanges.  
- SSH est indispensable pour l’administration à distance.  
- VPN permet d’interconnecter des réseaux en toute sécurité.  
- Wireshark peut montrer la différence entre trafic lisible (HTTP) et illisible (HTTPS).  

## 🔑 Mots-clés
TLS, SSL, HTTPS, SMTPS, POP3S, IMAPS, SSH, SFTP, FTPS, VPN, chiffrement, authentification, Wireshark

## 📚 Ressources
- [RFC 5246 – TLS 1.2](https://www.rfc-editor.org/rfc/rfc5246)  
- [RFC 8446 – TLS 1.3](https://www.rfc-editor.org/rfc/rfc8446)  
- [RFC 4251 – SSH Protocol](https://www.rfc-editor.org/rfc/rfc4251)  
- [Wireshark TLS Analysis](https://wiki.wireshark.org/TLS)  
- [OpenVPN Documentation](https://openvpn.net/community-resources/)  

---
