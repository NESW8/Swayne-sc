# Learn the Linux Fundamentals Part 1

## 📌 Introduction
Ce rapport résume les notions vues dans la room **"Learn the Linux Fundamentals Part 1"** sur TryHackMe.  
Il couvre les bases de Linux, les commandes essentielles, la navigation dans le système de fichiers et l'utilisation des opérateurs shell.

---

## 1️⃣ Introduction à Linux
- Linux est un système d'exploitation open-source largement utilisé dans les serveurs, systèmes embarqués, superordinateurs, etc.
- Objectifs de cette partie :
  - Exécuter vos premières commandes Linux.
  - Apprendre des commandes essentielles.
  - Naviguer dans le système de fichiers.
  - Utiliser les opérateurs shell.

---

## 2️⃣ Historique et utilisations de Linux
- Utilisations :
  - Sites web
  - Tableaux de bord de voitures
  - Systèmes de caisse (POS)
  - Infrastructures critiques
- Linux regroupe plusieurs distributions basées sur UNIX (Ubuntu, Debian, etc.)
- Première version sortie en **1991**.

---

## 3️⃣ Interagir avec sa première machine Linux
- Utilisation d'une machine Ubuntu dans le navigateur via TryHackMe.
- Détails fournis :
  - Adresse IP
  - Durée de session
  - Commandes disponibles via un terminal.

---

## 4️⃣ Premières commandes
- `echo` : afficher du texte.
- `whoami` : connaître l'utilisateur actuel.

**Exemples :**
```bash
echo "Hello Friend!"
whoami
```

---

## 5️⃣ Navigation dans le système de fichiers
Commandes clés :
- `ls` → Lister le contenu d'un répertoire.
- `cd` → Changer de répertoire.
- `cat` → Afficher le contenu d'un fichier.
- `pwd` → Afficher le chemin complet du répertoire courant.

**Exemple :**
```bash
ls Pictures
cd Documents
cat todo.txt
pwd
```

---

## 6️⃣ Recherche de fichiers
- `find` : rechercher des fichiers selon leur nom ou extension.
- `grep` : rechercher du texte dans un fichier.

**Exemple :**
```bash
find -name passwords.txt
grep "81.143.211.90" access.log
```

---

## 7️⃣ Introduction aux opérateurs shell
- `&` → Exécuter une commande en arrière-plan.
- `&&` → Chaîner plusieurs commandes (exécution de la suivante seulement si la précédente réussit).
- `>` → Rediriger la sortie vers un fichier (écrasement).
- `>>` → Ajouter à la fin d'un fichier (sans écraser).

**Exemple :**
```bash
echo hey > welcome
echo hello >> welcome
```

---

## 📌 Récapitulatif
- Compréhension de l'importance de Linux dans différents domaines.
- Manipulation de commandes de base.
- Navigation efficace dans le système de fichiers.
- Utilisation d'outils puissants comme `find` et `grep`.
- Introduction aux opérateurs shell pour gérer les sorties.

---

✅ **Prochaine étape** : Passer à **Linux Fundamentals Part 2** pour approfondir la gestion des permissions, processus et scripts.
