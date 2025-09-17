---
# TryHackMe – Networking Core Protocols  
📡 Exploration des protocoles fondamentaux de communication applicative

## 📄 Description
Cette room introduit les principaux protocoles utilisés quotidiennement sur Internet : DNS, HTTP(S), FTP, SMTP, POP3, IMAP et Telnet.  
Elle montre comment chacun fonctionne, quels ports ils utilisent et comment interagir directement avec eux via des outils simples comme `telnet`, `ftp` ou `curl`.

## 🎯 Objectifs
- Comprendre le rôle et le fonctionnement des protocoles applicatifs de base.  
- Identifier les ports par défaut de chaque service.  
- Manipuler manuellement les services pour comprendre leur logique.  
- Relever les risques de sécurité liés à l’absence de chiffrement.

## 🛠️ Outils et concepts
- **DNS** : Résolution de noms (A, AAAA, MX, CNAME).  
- **HTTP / HTTPS** : Accès web et méthodes (GET, POST, PUT, DELETE).  
- **FTP** : Transfert de fichiers.  
- **SMTP** : Envoi d’emails.  
- **POP3** : Récupération de mails.  
- **IMAP** : Synchronisation et gestion distante des mails.  
- **Telnet** : Connexion brute sur un port TCP pour tester un service.  
- **Wireshark / tshark** : Observation des échanges.

## 📚 Résumé du contenu

### 🔹 DNS
- Résout les domaines en adresses IP.  
- Ports : 53 (UDP/TCP).  
- Enregistrements : `A` (IPv4), `AAAA` (IPv6), `MX` (mail), `CNAME` (alias).  
- Commandes utiles : `nslookup`, `dig`.

### 🔹 HTTP / HTTPS
- Ports : 80 (HTTP), 443 (HTTPS).  
- Méthodes : `GET`, `POST`, `PUT`, `DELETE`.  
- Exemple via Telnet :  
  ```http
  GET /index.html HTTP/1.1
  Host: target.thm
  ```

### 🔹 FTP
- Port : 21 (TCP).  
- Commandes : `USER`, `PASS`, `LIST`, `RETR`, `STOR`.  
- Ex : connexion anonyme pour télécharger un fichier.

### 🔹 SMTP
- Port : 25 (TCP).  
- Commandes : `HELO`, `MAIL FROM`, `RCPT TO`, `DATA`.  
- Permet d’envoyer un email en clair via telnet.

### 🔹 POP3
- Port : 110 (TCP).  
- Commandes : `USER`, `PASS`, `LIST`, `RETR`, `QUIT`.  
- Permet de télécharger et lire les mails.

### 🔹 IMAP
- Port : 143 (TCP).  
- Commandes : `LOGIN`, `SELECT`, `FETCH`, `LOGOUT`.  
- Permet de gérer les emails directement sur le serveur.

### 🔹 Telnet
- Port par défaut : 23 (TCP).  
- Utilisé ici comme outil pour tester les protocoles en clair.  
- ⚠️ Non sécurisé, remplacé en production par SSH.

## 📌 Ports et services
- **23/TCP** → Telnet  
- **53/UDP-TCP** → DNS  
- **80/TCP** → HTTP  
- **443/TCP** → HTTPS  
- **21/TCP** → FTP  
- **25/TCP** → SMTP  
- **110/TCP** → POP3  
- **143/TCP** → IMAP  

## ✅ Ce que j’ai appris
- Comprendre comment chaque protocole de base fonctionne.  
- DNS est indispensable pour traduire les noms de domaine.  
- HTTP/HTTPS structurent les échanges web.  
- FTP, SMTP, POP3 et IMAP expliquent le transfert et la gestion des emails et fichiers.  
- Telnet est un excellent outil d’expérimentation, mais non sécurisé.  
- Les échanges non chiffrés révèlent facilement identifiants et flags dans Wireshark.

## 🔑 Mots-clés
DNS, HTTP, HTTPS, FTP, SMTP, POP3, IMAP, Telnet, TCP/IP, ports, protocoles, email, Wireshark

## 📚 Ressources
- [RFC 1035 – DNS](https://www.rfc-editor.org/rfc/rfc1035)  
- [RFC 2616 – HTTP/1.1](https://www.rfc-editor.org/rfc/rfc2616)  
- [RFC 959 – FTP](https://www.rfc-editor.org/rfc/rfc959)  
- [RFC 5321 – SMTP](https://www.rfc-editor.org/rfc/rfc5321)  
- [RFC 1939 – POP3](https://www.rfc-editor.org/rfc/rfc1939)  
- [RFC 3501 – IMAP](https://www.rfc-editor.org/rfc/rfc3501)  
- [Wireshark Documentation](https://www.wireshark.org/docs/)  

---
