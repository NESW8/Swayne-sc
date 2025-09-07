# Windows Fundamentals 1 - Rapport d'apprentissage

## 🎯 Objectif
Apprendre les bases de l'utilisation du système d'exploitation Windows, y compris :
- Les éditions de Windows
- L'interface graphique (GUI)
- Le système de fichiers NTFS
- Les dossiers système critiques
- La gestion des comptes utilisateurs et des permissions
- Le fonctionnement de l'UAC (User Account Control)
- Les paramètres via le Control Panel
- L'utilisation du Task Manager

---

## 📚 Résumé des Tâches

### **Task 1 - Introduction to Windows**
- Présentation générale du système Windows et de ses composants.
- Accès à la machine virtuelle via RDP avec des identifiants fournis.
- Objectif : se familiariser avec l'environnement de travail.

### **Task 2 - Windows Editions**
- Explication des différentes versions : Home, Pro, Server.
- **BitLocker** : disponible sur Pro mais pas sur Home.
- Windows 11 est la version actuelle pour les utilisateurs finaux.
- Présentation de Windows Server 2019 dans la VM.

### **Task 3 - The Desktop (GUI)**
- Éléments principaux : Desktop, Start Menu, Search Box, Task View, Taskbar, Toolbars, Notification Area.
- **Search Box** peut être masqué via les paramètres de la Taskbar.
- La Task View peut être activée/désactivée via clic droit sur la Taskbar.
- Dans la Notification Area, on retrouve Clock, Network et Volume.

### **Task 4 - The File System**
- **NTFS** : New Technology File System.
- Avantages : fichiers > 4GB, permissions avancées, journalisation, compression.
- Permissions : Read, Write, Read & Execute, List Folder Contents, Modify, Full Control.
- Présentation des **Alternate Data Streams (ADS)**.

### **Task 5 - The Windows\System32 Folders**
- Contient les fichiers critiques du système.
- Variable système pour le dossier Windows : `%windir%`.
- Manipulation risquée → ne pas supprimer/modifier sans raison.

### **Task 6 - User Accounts, Profiles, and Permissions**
- Deux types de comptes : **Administrator** et **Standard User**.
- Profils utilisateurs stockés dans `C:\Users`.
- Gestion via **lusrmgr.msc** (Local User and Group Management).
- Exemple : utilisateur `tryhackmebilly` membre des groupes `Remote Desktop Users` et `Users`.

### **Task 7 - User Account Control (UAC)**
- L’UAC limite les droits administratifs pour réduire les risques.
- Icône avec bouclier = nécessite une élévation de privilèges.
- En Standard User, installation d’un programme demande un mot de passe admin.

### **Task 8 - Settings and the Control Panel**
- **Control Panel** : possibilité d’afficher en Small icons.
- Dernier élément affiché : **Windows Defender Firewall**.
- Utilisation des paramètres pour personnaliser l'affichage et gérer le système.

### **Task 9 - Task Manager**
- Raccourci clavier : **CTRL + SHIFT + ESC**.
- Permet de gérer les processus, voir les performances, et arrêter des programmes.

### **Task 10 - Conclusion**
- Révision des notions clés vues dans la partie 1.
- Mise en pratique sur VM pour comprendre et manipuler les composants Windows.

---

## 💻 Commandes / Actions clés à retenir
- `lusrmgr.msc` → Gestion des utilisateurs et groupes locaux
- `%windir%` → Variable système pour dossier Windows
- `CTRL + SHIFT + ESC` → Ouvrir Task Manager
- Paramètres Taskbar → Cacher/afficher Search Box et Task View
- **BitLocker** disponible uniquement sur Pro

---

## 📌 Points importants à retenir
- Différences entre Windows Home et Pro (BitLocker, gestion avancée).
- NTFS est le système de fichiers par défaut, avec gestion avancée des permissions.
- Le dossier System32 est critique pour le fonctionnement du système.
- Importance de l’UAC pour protéger contre les modifications non autorisées.
- Control Panel permet de gérer de nombreux aspects du système, même si les Settings prennent plus de place dans Windows 10/11.
- Task Manager est essentiel pour le diagnostic et la gestion des processus.

---

_Room complétée le 
