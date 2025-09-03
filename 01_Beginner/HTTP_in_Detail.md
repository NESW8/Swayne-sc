# HTTP in Detail — TryHackMe Report

## 📜 Introduction
Cette room explique en profondeur le protocole HTTP et sa version sécurisée HTTPS, utilisés pour la communication entre un navigateur et un serveur web.  
Elle couvre :
- Les bases de HTTP/HTTPS
- Les requêtes et réponses
- Les méthodes HTTP
- Les codes de statut
- Les en-têtes (*headers*)
- Les cookies et leur rôle
- La mise en pratique avec des requêtes complètes

---

## 📂 Contenu par tâches

### 1️⃣ What is HTTP(S)?
- **HTTP** (*HyperText Transfer Protocol*) : protocole de communication pour transférer des pages web et des ressources (HTML, images, vidéos, etc.).  
- **HTTPS** (*HyperText Transfer Protocol Secure*) : version sécurisée chiffrée via TLS/SSL, garantissant confidentialité et intégrité des données.

### 2️⃣ Requests and Responses
- Structure d’une URL : `schéma://utilisateur:motdepasse@hôte:port/chemin?paramètres#fragment`  
- Une requête HTTP inclut : méthode, chemin, version, en-têtes, corps (facultatif).
- La réponse HTTP contient : version, code de statut, en-têtes, corps (contenu renvoyé).

### 3️⃣ HTTP Methods
- **GET** : récupérer des données.
- **POST** : envoyer des données et créer de nouvelles ressources.
- **PUT** : mettre à jour des données.
- **DELETE** : supprimer une ressource.

### 4️⃣ HTTP Status Codes
- **2xx** : succès (200 OK, 201 Created…).
- **3xx** : redirection (301 Moved Permanently, 302 Found…).
- **4xx** : erreur côté client (400 Bad Request, 401 Unauthorized, 403 Forbidden, 404 Not Found…).
- **5xx** : erreur côté serveur (500 Internal Server Error, 503 Service Unavailable…).

### 5️⃣ Headers
**Request headers** (envoyés par le client) :
- `Host` : nom du site demandé.
- `User-Agent` : info sur le navigateur.
- `Content-Length` : taille du corps envoyé.
- `Accept-Encoding` : formats de compression acceptés.

**Response headers** (envoyés par le serveur) :
- `Set-Cookie` : enregistre un cookie côté client.
- `Cache-Control` : gestion du cache.
- `Content-Type` : type du contenu renvoyé (HTML, JSON…).

### 6️⃣ Cookies
- Fichiers stockés côté client contenant des données de session ou de personnalisation.
- Envoyés par le serveur via `Set-Cookie` et renvoyés au serveur par le client dans `Cookie`.

### 7️⃣ Making Requests (Pratique)
- Exercices de création de requêtes HTTP avec différentes méthodes et paramètres pour obtenir des flags.

---

## 📌 Termes & concepts importants
- **HTTP / HTTPS** : protocoles de communication web.
- **URL** : adresse unique d’une ressource.
- **Header** : métadonnées dans une requête ou réponse.
- **Method** : action demandée au serveur.
- **Status Code** : résultat de la requête.
- **Cookie** : données stockées côté client.
- **TLS/SSL** : chiffrement et sécurisation des communications.

---

## 🎯 Ce que j’ai appris
- Différencier HTTP et HTTPS et comprendre leur fonctionnement.
- Lire et comprendre une requête et une réponse HTTP complètes.
- Identifier les méthodes HTTP les plus courantes (GET, POST, PUT, DELETE).
- Reconnaître les principaux codes de statut HTTP et leur signification.
- Comprendre le rôle des en-têtes dans les échanges client/serveur.
- Utiliser et interpréter les cookies pour la gestion de session.
- Construire des requêtes HTTP manuellement pour interagir avec un serveur.
