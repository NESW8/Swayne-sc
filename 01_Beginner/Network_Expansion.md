# TryHackMe - Network Expansion

## 📄 Description
Cette room couvre les concepts permettant d’étendre et de sécuriser un réseau, notamment :
- Le **transfert de port** (port forwarding)
- Le rôle et les types de **pare-feu**
- Les bases des **VPN**
- Les équipements réseau LAN : **routeurs** et **switches**
- Un simulateur pratique de trafic réseau

---

## 🎯 Objectifs
- Comprendre le principe du **port forwarding** et pourquoi il est nécessaire pour rendre un service accessible depuis l’extérieur.
- Découvrir comment un **pare-feu** filtre le trafic et ses différentes catégories.
- Apprendre le fonctionnement et les avantages d’un **VPN**.
- Différencier le rôle d’un **routeur** et d’un **switch**, et introduire la notion de **VLAN**.
- Mettre en pratique avec un **simulateur réseau** pour observer le trajet des paquets.

---

## 🛠️ Outils et concepts
- **Port Forwarding** : configuration au niveau du routeur pour rendre un service interne (ex. serveur web sur port 80) accessible depuis l’extérieur via l’adresse IP publique.
- **Pare-feu (Firewall)** :
  - **Stateful** : inspecte la connexion dans son ensemble, plus dynamique.
  - **Stateless** : applique des règles fixes paquet par paquet.
- **VPN (Virtual Private Network)** :
  - Chiffre les données et crée un tunnel sécurisé entre réseaux distants.
  - Protocoles : PPP, PPTP, IPSec.
- **Routeur** : connecte plusieurs réseaux et choisit le chemin du trafic (couche 3).
- **Switch** : connecte plusieurs appareils dans un réseau local (couche 2 ou 3), transmet les trames via les adresses MAC.
- **VLAN (Virtual Local Area Network)** : segmentation logique du réseau pour plus de sécurité et de gestion.
- **ARP, TCP handshake, filtrage par protocole et port** : observés dans le simulateur.

---

## 📌 Résumé du contenu

### 1. Port Forwarding
- Permet à un appareil extérieur d’accéder à un service hébergé sur un réseau interne.
- Exemple : un serveur web interne en **192.168.1.10:80** rendu accessible via **82.62.51.70:80**.
- Configuré au **routeur**.

### 2. Pare-feu
- Rôle : autoriser ou bloquer du trafic selon IP source/destination, port, protocole.
- **Stateful** : analyse la connexion complète.
- **Stateless** : analyse chaque paquet indépendamment.
- Peut filtrer TCP, UDP ou les deux.

### 3. VPN
- Crée un réseau privé virtuel sur un réseau public.
- Avantages : connexion de réseaux distants, confidentialité, anonymat.
- Protocoles vus :
  - **PPP** : authentifie et chiffre.
  - **PPTP** : simple, peu sécurisé.
  - **IPSec** : très sécurisé, plus complexe.

### 4. Routeur vs Switch
- **Routeur** : choisit le chemin entre réseaux (couche 3).
- **Switch** : relie les appareils d’un même réseau (couche 2 ou 3).
- **VLAN** : isole logiquement les groupes d’appareils.

### 5. Simulateur Réseau
- Visualisation du trajet d’un paquet TCP.
- Observation des étapes : routage, ARP, handshake TCP.
- Application pratique des filtres pare-feu et règles de routage.

---

## 📚 Ce que j’ai appris
- Configurer et comprendre le rôle du **port forwarding**.
- Différences entre un pare-feu **stateful** et **stateless**.
- Les avantages et protocoles des **VPN**.
- Différencier **routeurs** et **switches** et comprendre les **VLAN**.
- Lecture et interprétation des journaux réseau pour suivre le chemin d’un paquet.

---

_Room complétée le : 03/09/2025_
