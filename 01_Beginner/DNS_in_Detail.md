# TryHackMe - DNS in Detail

## 📄 Description
Cette room explique le fonctionnement du **Domain Name System (DNS)**, qui permet de traduire les noms de domaine lisibles par l’homme (ex. `tryhackme.com`) en adresses IP compréhensibles par les machines.  
On y apprend la structure hiérarchique des domaines, les différents types d’enregistrements DNS, et le processus complet d’une requête DNS.

---

## 🎯 Objectifs
- Comprendre le rôle du DNS dans la navigation Internet.
- Identifier la hiérarchie d’un nom de domaine (TLD, second-level domain, subdomain).
- Connaître les principaux types d’enregistrements DNS.
- Comprendre le cheminement d’une requête DNS depuis un poste client jusqu’au serveur autoritaire.
- Savoir effectuer des requêtes DNS pour extraire des informations.

---

## 🛠️ Outils et concepts
- **Adresse IP** : identifiant unique d’un appareil sur un réseau (IPv4 ou IPv6).
- **Nom de domaine** : adresse lisible par l’homme qui pointe vers une IP via le DNS.
- **TLD (Top-Level Domain)** : extension (.com, .org, .fr…).
- **Second-Level Domain** : partie du nom avant le TLD (`tryhackme` dans `tryhackme.com`).
- **Subdomain** : sous-partie du domaine (`admin` dans `admin.tryhackme.com`).
- **Types d’enregistrements DNS** :
  - `A` : IPv4
  - `AAAA` : IPv6
  - `CNAME` : alias pointant vers un autre domaine
  - `MX` : serveur de messagerie
  - `TXT` : informations textuelles (SPF, vérifications…)
- **Serveurs DNS** :
  - **Recursive DNS Server**
  - **Root DNS Server**
  - **TLD Server**
  - **Authoritative Server**
- **TTL (Time To Live)** : durée pendant laquelle une réponse DNS est considérée valide.

---

## 📌 Résumé du contenu

### 1. Introduction au DNS
- Permet de retenir un nom de domaine au lieu d’une adresse IP complexe.
- Fonctionne comme un “annuaire” d’Internet.

### 2. Hiérarchie des noms de domaine
- **TLD** : extension (ex. `.com`, `.org`, `.edu`).
- **Second-Level Domain** : nom principal (ex. `tryhackme`).
- **Subdomain** : préfixe séparé par un point (ex. `admin.tryhackme.com`).
- Contraintes de longueur et de caractères autorisés.

### 3. Types d’enregistrements DNS
- `A` → IPv4
- `AAAA` → IPv6
- `CNAME` → redirection vers un autre domaine
- `MX` → serveurs de mails avec priorité
- `TXT` → stockage d’informations textuelles (SPF, vérification de domaine…)

### 4. Processus d’une requête DNS
1. Vérification du cache local.
2. Envoi au **serveur DNS récursif**.
3. Si non trouvé, contact du **Root DNS Server**.
4. Redirection vers le **TLD Server** approprié.
5. Obtention de la réponse finale depuis le **serveur autoritaire**.
6. Retour au client avec mise en cache selon le TTL.

### 5. Partie pratique
- Utilisation d’un outil en ligne pour récupérer :
  - `CNAME` : `shops.myshopify.com`
  - `TXT` : `THM{7012BBA60997F35A9516C2E16D2944FF}`
  - `MX Priority` : 30
  - `A record` : `10.10.10.10`

---

## 📚 Ce que j’ai appris
- Structure hiérarchique complète des noms de domaine.
- Rôle et utilité de chaque type d’enregistrement DNS.
- Compréhension du cheminement complet d’une requête DNS.
- Comment extraire manuellement des enregistrements DNS (`A`, `MX`, `CNAME`, `TXT`).
- Importance du **TTL** dans les performances et la propagation DNS.

---

_Room complétée le : JJ/MM/AAAA_
