# 🕸️ How Websites Work - TryHackMe Report

## 📌 Room Overview
Cette room introduit le fonctionnement des sites web, leur structure (Front-End et Back-End), ainsi que certaines failles web courantes comme l'exposition de données sensibles et l'injection HTML.

---

## 📂 Structure du rapport
1. **Comment fonctionnent les sites web**
2. **HTML**
3. **JavaScript**
4. **Sensitive Data Exposure**
5. **HTML Injection**

---

## 1️⃣ Comment fonctionnent les sites web
- Un site web repose sur deux grandes parties :
  - **Front-End** (client-side) : ce que le navigateur affiche et interprète.
  - **Back-End** (server-side) : traitement des requêtes et génération des réponses.
- Processus :
  1. Le navigateur envoie une requête HTTP au serveur web.
  2. Le serveur traite et renvoie une réponse contenant le contenu demandé.
  3. Le navigateur rend la page à l'utilisateur.

---

## 2️⃣ HTML
- **HTML** (HyperText Markup Language) définit la structure des pages web.
- Éléments clés :
  - `<!DOCTYPE html>` : spécifie le type de document.
  - `<html>` : élément racine.
  - `<head>` : métadonnées, titre, liens CSS/JS.
  - `<body>` : contenu affiché.
- Balises courantes : `<h1>`, `<p>`, `<img>`, `<button>`.
- Attributs : `id`, `class`, `src`, etc.
- Exemple : ajout d’une image ou correction d’un lien cassé.

---

## 3️⃣ JavaScript
- Langage côté client pour ajouter de l’interactivité.
- Peut modifier dynamiquement le contenu d'une page :
```javascript
document.getElementById("demo").innerHTML = "Hack the Planet";
```
- Événements courants : `onclick`, `onhover`.
- Exemple :
```html
<button onclick='document.getElementById("demo").innerHTML = "Button Clicked";'>Click Me!</button>
```

---

## 4️⃣ Sensitive Data Exposure
- Problème : données sensibles présentes dans le code source HTML (ex : mots de passe en clair, liens privés).
- Exemple trouvé : identifiants de test (`admin:password123`) dans un commentaire HTML.
- Risque : un attaquant peut exploiter ces infos pour accéder à des zones protégées.

---

## 5️⃣ HTML Injection
- Vulnérabilité due au manque de filtrage des entrées utilisateur.
- L’attaquant injecte du HTML ou du JavaScript dans un champ non sécurisé.
- Exemple d’exploitation :
```html
<a href="http://hacker.com">Cliquez ici</a>
```
- Risques : modification de l'apparence, redirection vers un site malveillant, phishing.
- **Protection** :
  - Valider et filtrer les entrées.
  - Échapper les caractères spéciaux (`<`, `>`, etc.).

---

## 🎯 Ce que j’ai appris
- Différence entre **Front-End** et **Back-End**.
- Structure HTML et utilisation de JavaScript pour manipuler le DOM.
- Identifier des fuites d’informations dans le code source.
- Comprendre et exploiter une injection HTML basique.
- Mesures de prévention contre ces vulnérabilités.

---

📅 **Date** : 2025-09-03  
🏷 **TryHackMe Room** : [How Websites Work](https://tryhackme.com/room/howwebsiteswork)
