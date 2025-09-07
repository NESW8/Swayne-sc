
# Rapport : Learn the Linux Fundamentals Part 3

## 🎯 Objectif de la room
Ce module conclut la série **Linux Fundamentals** en abordant des outils et commandes courants pour une utilisation quotidienne de Linux.
Il met l'accent sur l'automatisation, la gestion des paquets, et la surveillance via les journaux système.

---

## 1. Connexion à la machine cible
- Connexion via **SSH** en utilisant l’adresse IP et les identifiants fournis.
- Utilisation de **l’AttackBox** pour interagir avec la machine distante.

---

## 2. Éditeurs de texte en terminal
### Nano
- Commande : `nano <nom_de_fichier>`
- Fonctionnalités : recherche, copier-coller, navigation par numéro de ligne, sauvegarde et sortie (`CTRL+X`).
  
### Vim
- Plus avancé : personnalisation, coloration syntaxique, fonctionne sur la plupart des systèmes.

---

## 3. Utilitaires réseau et gestion de fichiers
### Téléchargement de fichiers
- **wget** : `wget <URL>` pour télécharger un fichier depuis le web.

### Transfert de fichiers avec SCP (SSH)
- Commande : `scp <source> <utilisateur>@<IP>:<destination>`

### Serveur HTTP simple
- Python : `python3 -m http.server 8000`

---

## 4. Gestion des processus
- **ps**, **top**, **htop** pour voir les processus actifs.
- **kill** pour arrêter un processus : `kill <PID>`
- **systemctl** pour gérer les services.
- Gestion du premier plan / arrière-plan : `fg`, `bg`.

---

## 5. Automatisation avec cron
- Fichier crontab : `crontab -e`
- Exemple : Sauvegarde toutes les 12h  
  ```
  0 */12 * * * cp -R /home/user/Documents /var/backups/
  ```

---

## 6. Gestion des paquets (APT)
- Ajout d’un dépôt : `add-apt-repository <repo>` ou modification de `/etc/apt/sources.list`
- Mise à jour : `apt update`
- Installation : `apt install <package>`
- Suppression : `apt remove <package>`

---

## 7. Journaux système
- Localisation : `/var/log`
- **Apache2** : `access.log`, `error.log`
- **fail2ban** : surveille les tentatives d’attaque brute force.
- **ufw** : journal du pare-feu.

---

## ✅ Points clés retenus
- Maîtrise des éditeurs **Nano** et **Vim**.
- Utilisation de **wget**, **scp** et **serveurs HTTP**.
- Surveillance et gestion des **processus**.
- Automatisation via **cron**.
- Gestion de paquets avec **APT**.
- Lecture et analyse des **logs** pour la sécurité et la maintenance.
