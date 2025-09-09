# Windows Fundamentals 2 - Rapport

## Introduction
Ce module est la deuxième partie de la série **Windows Fundamentals** sur TryHackMe.  
Il couvre des outils et utilitaires intégrés à Windows, accessibles via **MSConfig**, ainsi que d'autres méthodes pour gérer et diagnostiquer le système.

---

## 1. System Configuration (MSConfig)
- **But** : Utilitaire de dépannage avancé pour gérer le démarrage, diagnostiquer et configurer certains services.
- **Commandes** :
  - Lancer : `msconfig`
- **Onglets principaux** :
  1. **General** : Choix du mode de démarrage (**Normal**, **Diagnostic**, **Sélectif**).
  2. **Boot** : Options liées au démarrage (safe mode, etc.).
  3. **Services** : Liste des services, possibilité de les activer/désactiver.
  4. **Startup** : Redirige vers le **Task Manager** pour gérer les programmes au démarrage.
  5. **Tools** : Accès rapide à divers outils système.

---

## 2. Changer les paramètres UAC
- **UAC (User Account Control)** : Permet de limiter les actions des applications nécessitant des privilèges élevés.
- **Commande** : `UserAccountControlSettings.exe`
- Recommandation : Ne pas désactiver complètement l'UAC.

---

## 3. Computer Management
- **Commande** : `compmgmt.msc`
- Regroupe trois sections principales :
  1. **System Tools**
     - **Task Scheduler** : Programmer des tâches automatiques.
     - **Event Viewer** : Journaux système (types : Error, Warning, Information, Success Audit, Failure Audit).
     - **Shared Folders** : Voir les dossiers partagés.
     - **Performance Monitor** : Surveillance en temps réel des performances.
     - **Device Manager** : Gestion du matériel.
  2. **Storage**
     - **Disk Management** : Gérer les partitions, volumes et disques.
  3. **Services and Applications**
     - **Services** : Activer/désactiver ou configurer des services Windows.

---

## 4. System Information
- **Commande** : `msinfo32.exe`
- Permet de voir :
  - **Hardware Resources**
  - **Components**
  - **Software Environment** (y compris variables d'environnement).
- Accès rapide aux détails matériels et logiciels installés.

---

## 5. Resource Monitor
- **Commande** : `resmon.exe`
- Surveillance détaillée :
  - **CPU**
  - **Memory**
  - **Disk**
  - **Network**
- Donne aussi les fichiers et processus utilisant des ressources.

---

## 6. Command Prompt (cmd)
- **Commandes utiles** :
  - `hostname` → Nom de la machine.
  - `whoami` → Utilisateur connecté.
  - `ipconfig` / `ipconfig /all` → Infos réseau.
  - `netstat` → Connexions réseau actives.
  - `net help` / `net help user` → Aide pour les commandes `net`.

---

## 7. Registry Editor
- **Commande** : `regedt32.exe` ou `regedit`
- Base de données hiérarchique contenant les paramètres système et logiciels.
- Prudence : modification risquée pour la stabilité du système.

---

## Conclusion
Windows Fundamentals 2 approfondit la maîtrise des outils intégrés de Windows, utiles pour :
- Diagnostiquer les problèmes système.
- Surveiller les performances.
- Gérer les services, le matériel et les connexions réseau.
- Accéder aux paramètres avancés via **MSConfig** et d'autres utilitaires.

---
