# TryHackMe - Learn the Linux Fundamentals Part 2

## 📌 Introduction
Ce rapport résume les notions vues dans la room **Learn the Linux Fundamentals Part 2** sur TryHackMe.

---

## 1️⃣ Introduction
- Application des connaissances vues dans la partie 1.
- Passage à l’utilisation de **SSH** pour se connecter à une machine distante.
- Objectifs :
  - Utiliser des **flags** et **arguments** avec les commandes.
  - Approfondir la gestion du **système de fichiers** (copier, déplacer, supprimer).
  - Comprendre les **permissions** sur Linux.
  - Exécuter des scripts et binaires.

---

## 2️⃣ Accès à la machine via SSH
- **SSH (Secure Shell)** permet une connexion sécurisée à distance.
- Utilisation de l’adresse IP et des identifiants fournis.
- Syntaxe :  
  ```bash
  ssh utilisateur@IP
  ```
- Connexion avec le compte `tryhackme`.

---

## 3️⃣ Flags et Switches
- Les **flags** modifient le comportement d’une commande.
- Exemple avec `ls` :
  - `ls -a` : affiche aussi les fichiers cachés.
  - `ls -lh` : affichage détaillé en taille lisible.
  - `ls --help` : liste les options disponibles.
- **man** : affiche la documentation d’une commande.
  ```bash
  man ls
  ```

---

## 4️⃣ Interaction avancée avec le système de fichiers
Commandes nouvelles :
- `touch` → créer un fichier.
- `mkdir` → créer un dossier.
- `cp` → copier fichiers/dossiers.
- `mv` → déplacer ou renommer.
- `rm` → supprimer fichiers/dossiers.
- `file` → afficher le type d’un fichier.

Exemple :
```bash
cp fichier1 fichier2
mv fichier.txt /home/user/
```

---

## 5️⃣ Permissions sur Linux
- Permissions = contrôle sur lecture (**r**), écriture (**w**) et exécution (**x**).
- Chaque fichier/dossier appartient à :
  - un **utilisateur**,
  - un **groupe**.
- `ls -lh` : voir les permissions et propriétaires.
- `su` : changer d’utilisateur.

---

## 6️⃣ Répertoires communs
- `/etc` → fichiers de configuration système.
- `/var` → logs, données variables.
- `/root` → home du super-utilisateur.
- `/tmp` → fichiers temporaires.

---

## 7️⃣ Conclusion
Compétences acquises :
- Connexion et utilisation de **SSH**.
- Maîtrise des **flags** et **arguments**.
- Gestion avancée des fichiers (copie, suppression, déplacement).
- Compréhension des **permissions** et changement d’utilisateur.
- Connaissance des répertoires critiques.

---

✅ **Room complétée avec succès**.
