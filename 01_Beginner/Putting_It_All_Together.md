# Putting It All Together

Ce rapport documente ma progression sur la room **Putting It All Together** de TryHackMe.  
L'objectif est de comprendre l'ensemble du processus qui se produit lorsqu'on visite un site web, ainsi que les composants et étapes impliqués.

---

## 📌 Tâche 1 - Putting It All Together
Résumé visuel du processus complet :
1. Requête envoyée depuis le navigateur.
2. Résolution DNS pour obtenir l'adresse IP du serveur.
3. Connexion au serveur web via HTTP/HTTPS.
4. Le serveur retourne les fichiers (HTML, CSS, JS, images…).
5. Le navigateur interprète et affiche la page.

![Task 1](images/task1.png)

---

## 📌 Tâche 2 - Other Components
Présentation de composants additionnels qui optimisent ou sécurisent la navigation :
- **Load Balancers** : distribuent la charge entre plusieurs serveurs et effectuent des vérifications de santé (*health checks*).
- **CDN (Content Delivery Networks)** : distribuent les fichiers statiques depuis un serveur proche géographiquement.
- **Databases** : stockent et fournissent des données dynamiques.
- **WAF (Web Application Firewall)** : filtrent et bloquent les requêtes malveillantes avant qu'elles n'atteignent le serveur.

![Task 2](images/task2.png)

---

## 📌 Tâche 3 - How Web Servers Work
- **Web Server** : logiciel qui écoute les requêtes HTTP et délivre du contenu web (Apache, Nginx, IIS…).  
- **Virtual Hosts** : permettent d'héberger plusieurs sites sur un même serveur.
- **Static vs Dynamic Content** :
  - *Static* : contenu qui ne change pas (images, fichiers CSS…).
  - *Dynamic* : contenu généré à la volée (blogs, résultats de recherche…).
- **Backend Languages** : PHP, Python, Ruby, Node.js…

![Task 3](images/task3.png)

---

## 📌 Tâche 4 - Quiz
Mise en pratique sous forme de puzzle : replacer les étapes du fonctionnement d'un site web dans le bon ordre pour obtenir le flag.

![Task 4](images/task4.png)
![Quiz Order](images/task4_quiz.png)

---

## 📌 Ce que j’ai appris
- Le chemin complet d’une requête web, de l’utilisateur jusqu’au serveur et retour.
- L’importance des DNS dans la résolution d’adresse IP.
- Le rôle des load balancers, CDN et WAF dans la performance et la sécurité.
- Les différences entre contenu statique et dynamique.
- La distinction entre front-end et back-end, et leur interaction.
