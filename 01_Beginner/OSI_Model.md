# TryHackMe - OSI Model

## 📄 Description
Cette room présente le **modèle OSI (Open Systems Interconnection)**, une norme internationale qui divise la communication réseau en **7 couches**.  
Chaque couche a un rôle spécifique, allant de la transmission physique des données jusqu’aux applications utilisées par l’utilisateur final.  
La room se termine par un mini-jeu interactif simulant l’ouverture de portes par étage pour illustrer la communication entre couches.

---

## 🎯 Objectifs
- Comprendre la structure et le rôle des 7 couches du modèle OSI.
- Identifier les protocoles et équipements associés à chaque couche.
- Comprendre l’importance de la séparation des couches en réseau.
- Appliquer les connaissances via un exercice pratique.

---

## 🛠️ Outils et concepts
- **OSI Model** : Physical, Data Link, Network, Transport, Session, Presentation, Application.
- **Protocoles et exemples** :
  - **Couche 1 – Physical** : câbles, hubs, fibre optique.
  - **Couche 2 – Data Link** : Ethernet, ARP, adresses MAC.
  - **Couche 3 – Network** : IP, ICMP, routeurs.
  - **Couche 4 – Transport** : TCP, UDP, ports.
  - **Couche 5 – Session** : gestion de session, NetBIOS.
  - **Couche 6 – Presentation** : SSL/TLS, chiffrement, compression.
  - **Couche 7 – Application** : HTTP, DNS, SMTP.
- **Concepts clés** : encapsulation, adressage, protocoles, interaction inter-couches.

---

## 📌 Résumé du contenu
Le **modèle OSI** est un cadre de référence qui divise la communication réseau en 7 couches :  
1. **Physical** – Transmission brute de bits via un support physique.  
2. **Data Link** – Encapsulation des données en *frames*, adressage MAC, détection/correction d’erreurs locales.  
3. **Network** – Routage et adressage IP pour acheminer les *packets*.  
4. **Transport** – Segmentation, contrôle de flux, fiabilité via TCP ou rapidité via UDP.  
5. **Session** – Établissement, gestion et fermeture des sessions de communication.  
6. **Presentation** – Formatage, chiffrement, compression des données.  
7. **Application** – Interface avec l’utilisateur, services applicatifs (web, mail, DNS…).

Chaque couche ne communique qu’avec celle située directement au-dessus et en dessous.  
L’intérêt principal de cette architecture est de **standardiser** les échanges et permettre l’interopérabilité entre matériels et logiciels.

---

## 🕹️ Partie pratique – OSI Game
Le jeu final illustre le fonctionnement des couches :  
- Chaque **étage** correspond à une couche OSI.  
- L’objectif est d’ouvrir les **portes** dans l’ordre correct en partant de la couche Application (7) vers Physical (1) pour l’envoi, et inversement pour la réception.  
- Cette analogie montre que les données passent **de couche en couche** jusqu’à atteindre leur destination, chaque étape ayant une fonction précise.

---

## 📚 Ce que j’ai appris
- Le rôle précis de chacune des **7 couches OSI**.
- Les protocoles associés à chaque couche.
- La logique d’encapsulation et de décapsulation des données.
- L’importance d’une architecture standardisée pour la communication réseau.
- Une visualisation claire grâce au jeu des portes et étages.

---

_Room complétée le : 02/09/2025_
