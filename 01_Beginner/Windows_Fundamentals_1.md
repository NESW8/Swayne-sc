# TryHackMe – Windows Fundamentals 1  
📡 Introduction aux bases de Windows : interface, système de fichiers, comptes et paramètres

## 📄 Description
Ce module initie à l'environnement Windows, en présentant ses différentes éditions, l'interface graphique (GUI), le système de fichiers NTFS, les dossiers système critiques, la gestion des comptes utilisateurs, l'UAC et les paramètres via le Control Panel.

## 🎯 Objectifs
- Comprendre les différences entre les éditions Windows (Home, Pro, Server).
- Savoir naviguer dans l'interface graphique (Desktop, Start Menu, Taskbar).
- Comprendre la structure du système de fichiers NTFS.
- Identifier et utiliser les dossiers système critiques.
- Gérer les comptes utilisateurs et comprendre les permissions.
- Configurer et utiliser l'UAC (User Account Control).
- Utiliser le Control Panel et le Task Manager.

## 🛠️ Outils et concepts
- **GUI** : Interface graphique utilisateur.
- **NTFS** : New Technology File System, système de fichiers Windows avec gestion avancée des permissions.
- **UAC** : User Account Control, sécurité contre les élévations de privilèges non autorisées.
- **Control Panel** : Paramètres système centralisés.
- **Task Manager** : Gestion des processus et surveillance système.

## 📚 Résumé du contenu
### Éditions Windows
- **Windows Home** : grand public, pas de BitLocker.
- **Windows Pro** : fonctionnalités avancées (BitLocker, GPO, Hyper-V).
- **Windows Server** : usage professionnel, version vue : Server 2019.

### Interface graphique
- Desktop, Start Menu, Search Box, Task View, Taskbar, Notification Area.
- Cacher la Search Box : clic droit → Search → Hidden.
- Désactiver Task View : clic droit → décocher "Show Task View button".

### Système de fichiers
- NTFS : fichiers >4GB, journalisation, compression, permissions.
- Permissions : Read, Write, Execute, Modify, Full Control.
- **ADS** (Alternate Data Streams) : flux cachés utilisés parfois par des malwares.

### Dossiers système
- `C:\Windows` : fichiers système.
- `C:\Windows\System32` : fichiers critiques.
- Variable système : `%windir%`.

### Comptes utilisateurs
- Types : Administrator, Standard User.
- Profils : `C:\Users`.
- Gestion via `lusrmgr.msc`.

### UAC
- Bouclier sur les actions nécessitant élévation de privilèges.
- Protection contre modifications non autorisées.

### Control Panel & Task Manager
- Vue "Small icons" → dernier élément : Windows Defender Firewall.
- Task Manager : `Ctrl + Shift + Esc`.

## 📌 Ports et services
N/A – Room centrée sur l’OS local.

## ✅ Ce que j’ai appris
- Différences Home / Pro (BitLocker exclusif à Pro).
- Utilisation et personnalisation de la Taskbar.
- Gestion et compréhension du système de fichiers NTFS.
- Identification et gestion des dossiers critiques.
- Utilisation de l’UAC pour renforcer la sécurité.
- Navigation et réglages via Control Panel.
- Usage efficace du Task Manager.

## 🔑 Mots-clés
Windows, NTFS, UAC, Control Panel, Task Manager, BitLocker, ADS, System32

## 📚 Ressources
- [Microsoft – NTFS Overview](https://learn.microsoft.com/en-us/windows/win32/fileio/ntfs-technical-reference)
- [Microsoft – User Account Control](https://learn.microsoft.com/en-us/windows/security/identity-protection/user-account-control/how-user-account-control-works)
