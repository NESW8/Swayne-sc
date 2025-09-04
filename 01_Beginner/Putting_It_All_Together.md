# 🖥️ Putting It All Together - TryHackMe Report

## 📌 Room Overview
Cette room permet de mettre en pratique et de consolider les connaissances acquises dans les modules précédents, en reconstituant le cheminement complet d'une requête web et en identifiant les composants clés qui interviennent.

---

## 📂 Structure du rapport
1. **Processus complet d'accès à un site web**
2. **Composants supplémentaires**
3. **Fonctionnement des serveurs web**
4. **Mise en pratique - Quiz**

---

## 1️⃣ Processus complet d'accès à un site web
- L'utilisateur saisit une URL dans son navigateur.
- Le navigateur interroge le serveur DNS pour obtenir l'adresse IP associée.
- Une connexion HTTP ou HTTPS est établie avec le serveur web.
- Le serveur envoie les ressources nécessaires (HTML, CSS, JavaScript, images...).
- Le navigateur interprète et affiche la page pour l'utilisateur.

---

## 2️⃣ Composants supplémentaires
- **Load Balancer** : répartit la charge entre plusieurs serveurs pour optimiser les performances et éviter les pannes.
- **CDN (Content Delivery Network)** : met à disposition des copies de contenu statique depuis des serveurs géographiquement proches des utilisateurs.
- **Base de données** : stocke et fournit des informations dynamiques utilisées par les applications web.
- **WAF (Web Application Firewall)** : filtre et bloque les requêtes malveillantes.

---

## 3️⃣ Fonctionnement des serveurs web
- **Web Server** : logiciel (Apache, Nginx, IIS...) qui traite les requêtes HTTP/HTTPS.
- **Virtual Hosts** : permettent d’héberger plusieurs sites sur une même machine.
- **Contenu statique** : ressources fixes (images, feuilles CSS...).
- **Contenu dynamique** : contenu généré à la volée par des langages backend (PHP, Python, Node.js...).

---

## 4️⃣ Mise en pratique - Quiz
Un exercice interactif consistant à replacer dans l'ordre les étapes du chargement d'un site web, en appliquant les concepts vus précédemment.

---

## 🎯 Ce que j’ai appris
- Le cheminement complet d'une requête web et le rôle du DNS.
- L'importance des composants comme les CDN, load balancers et WAF dans la performance et la sécurité.
- Les différences entre contenu statique et dynamique.
- Comment les serveurs web gèrent et distribuent le contenu aux navigateurs.

---

📅 **Date** : 2025-09-04  

