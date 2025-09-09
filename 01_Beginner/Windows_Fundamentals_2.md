# TryHackMe – Windows Fundamentals 2  
📡 Exploration des outils administratifs et de diagnostic système intégrés à Windows

## 📄 Description
Ce module approfondit la découverte des outils intégrés à Windows pour diagnostiquer, configurer et surveiller le système.  
Il inclut MSConfig, UAC, Computer Management, System Information, Resource Monitor, Command Prompt et Registry Editor.

## 🎯 Objectifs
- Utiliser MSConfig pour diagnostiquer et configurer le démarrage.
- Configurer les paramètres de l’UAC.
- Gérer le système via Computer Management.
- Obtenir des informations détaillées sur le système avec System Information.
- Surveiller les performances avec Resource Monitor.
- Utiliser le Command Prompt pour l'administration.
- Modifier le registre avec Registry Editor (avec précaution).

## 🛠️ Outils et concepts
- **MSConfig** : configuration système et gestion du démarrage.
- **UAC** : contrôle des comptes utilisateurs.
- **Computer Management** : gestion centralisée des outils d'administration.
- **System Information** : vue globale du matériel et des logiciels.
- **Resource Monitor** : surveillance en temps réel des ressources.
- **Command Prompt** : exécution de commandes et scripts.
- **Registry Editor** : modification de la base de registre.

## 📚 Résumé du contenu
### MSConfig
- Commande : `msconfig`.
- Onglets : General, Boot, Services, Startup (redirige vers Task Manager), Tools.

### UAC
- Commande : `UserAccountControlSettings.exe`.
- Ne pas désactiver pour éviter les risques.

### Computer Management
- Commande : `compmgmt.msc`.
- Inclut :
  - **Task Scheduler**, **Event Viewer**, **Shared Folders**.
  - **Performance Monitor**, **Device Manager**.
  - **Disk Management** pour partitions.
  - **Services** et **WMI Control**.

### System Information
- Commande : `msinfo32.exe`.
- Trois sections : Hardware Resources, Components, Software Environment.
- Variables système comme `%windir%`, `%temp%`.

### Resource Monitor
- Commande : `resmon.exe`.
- Surveillance CPU, Memory, Disk, Network.

### Command Prompt
- Commande : `cmd`.
- Exemples :
  - `hostname`, `whoami`, `ipconfig /all`.
  - `netstat -ano`, `net user`, `net share`.
  - Aide : `commande /?`.

### Registry Editor
- Commandes : `regedt32.exe` ou `regedit`.
- Base hiérarchique de configuration système.

## 📌 Ports et services
N/A – Room centrée sur outils locaux.

## ✅ Ce que j’ai appris
- Utiliser MSConfig pour gérer le démarrage et accéder aux outils.
- Configurer et comprendre l’UAC.
- Utiliser Computer Management pour la gestion système complète.
- Obtenir un inventaire matériel/logiciel via System Information.
- Surveiller et diagnostiquer avec Resource Monitor.
- Employer cmd pour diverses tâches d'administration.
- Comprendre l'importance et les risques de Registry Editor.

## 🔑 Mots-clés
Windows, MSConfig, UAC, Computer Management, System Information, Resource Monitor, Command Prompt, Registry Editor

## 📚 Ressources
- [Microsoft – System Configuration](https://learn.microsoft.com/en-us/windows/client-management/system-configuration)
- [Microsoft – Registry Editor](https://learn.microsoft.com/en-us/troubleshoot/windows-server/performance/windows-registry-advanced-users)
