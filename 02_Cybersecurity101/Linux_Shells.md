# TryHackMe -- Linux Shells

🐧 Découverte des shells Linux et introduction au scripting

## 📄 Description

Cette room introduit les **Linux Shells**, qui permettent d'interagir
avec le système d'exploitation via la ligne de commande.\
On y apprend à utiliser les shells, explorer leurs types, manipuler des
fichiers, et écrire des scripts basiques pour automatiser des tâches.

------------------------------------------------------------------------

## 🎯 Objectifs

-   Comprendre le rôle du shell comme interface entre l'utilisateur et
    l'OS.\
-   Savoir naviguer et exécuter des commandes dans un shell Linux.\
-   Explorer différents types de shells (Bash, Fish, Zsh).\
-   Écrire et exécuter des scripts shell simples avec variables, boucles
    et conditions.\
-   Pratiquer avec un exercice pratique d'automatisation.

------------------------------------------------------------------------

## 🛠️ Outils et concepts

-   **CLI (Command Line Interface)** : interface textuelle pour
    interagir avec l'OS.\
-   **Shells Linux** : Bash, Fish, Zsh et leurs différences.\
-   **Commandes essentielles** :
    -   `pwd` (afficher le répertoire courant)\
    -   `cd` (changer de répertoire)\
    -   `ls` (lister le contenu d'un répertoire)\
    -   `cat` (afficher le contenu d'un fichier)\
    -   `grep` (rechercher un mot/regex dans un fichier)\
-   **Shell scripting** :
    -   Variables (`name="value"`)\
    -   Boucles (`for`, `while`)\
    -   Conditions (`if`, `elif`, `else`)\
    -   Commentaires (`#`)\
-   **Permissions** : `chmod +x script.sh` pour rendre un script
    exécutable.\
-   **Exercice pratique** : écriture d'un script de recherche dans des
    logs et d'authentification basique.

------------------------------------------------------------------------

## 📚 Résumé du contenu

### 🖥️ Introduction au shell

-   Le shell est **l'intermédiaire entre l'utilisateur et l'OS**.\
-   Comparaison GUI vs CLI : la CLI offre plus de puissance et de
    contrôle.

### 🔑 Commandes de base

-   `pwd`, `cd`, `ls` pour naviguer dans le système.\
-   `cat` pour afficher des fichiers.\
-   `grep` pour rechercher des mots-clés.

### 🐚 Types de shells

-   **Bash** (par défaut sur la plupart des distributions) : scripting
    puissant, historique de commandes.\
-   **Fish** : très user-friendly, syntax highlighting intégré.\
-   **Zsh** : hautement personnalisable, riche en fonctionnalités avec
    plugins.

### 📜 Scripting

-   Création de scripts avec **shebang** (`#!/bin/bash`).\
-   Définition de **variables**, utilisation de **boucles** et
    **conditions**.\
-   Ajout de **commentaires** pour clarifier le code.\
-   Exemple : script de locker nécessitant un username, une company et
    un PIN corrects.

### 🔒 Exercice pratique

-   Passage en root avec `sudo su`.\
-   Script utilisé pour rechercher un mot-clé dans les fichiers `.log`
    d'un répertoire.\
-   Identification des logs contenant la flag et extraction de la bonne
    réponse.

------------------------------------------------------------------------

## 📌 Points clés

-   Le **shell** est l'outil principal pour interagir avec Linux de
    façon avancée.\
-   Savoir écrire des **scripts** permet d'automatiser efficacement des
    tâches.\
-   La **puissance de Linux** réside dans la combinaison de commandes
    simples (`ls`, `cat`, `grep`, etc.) avec la logique des scripts.

------------------------------------------------------------------------

## ✅ Ce que j'ai appris

-   Utiliser efficacement **Bash** et comparer avec Fish et Zsh.\
-   Créer et exécuter des scripts pour automatiser des actions.\
-   Gérer les **permissions d'exécution** (`chmod +x`).\
-   Lire et analyser des fichiers logs avec `grep`.

------------------------------------------------------------------------

## 🔑 Mots-clés

Linux, Shell, Bash, Zsh, Fish, CLI, pwd, ls, cat, grep, scripting,
variables, boucles, conditions, logs, chmod

------------------------------------------------------------------------

## 📚 Ressources

-   [GNU Bash
    Manual](https://www.gnu.org/software/bash/manual/bash.html)\
-   [Zsh Documentation](https://zsh.sourceforge.io/Doc/)\
-   [Fish Shell Documentation](https://fishshell.com/docs/current/)\
-   [Linux Command Cheat
    Sheet](https://linuxcommand.org/lc3_cheat_sheet.php)
