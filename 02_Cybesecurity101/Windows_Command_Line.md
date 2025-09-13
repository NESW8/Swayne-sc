# TryHackMe – Windows Command Line  
💻 Découverte et utilisation de l’invite de commandes Windows (cmd.exe)

## 📄 Description
Cette room introduit l’utilisation de l’interface en ligne de commande **cmd.exe** sous Windows. Elle couvre les commandes essentielles pour explorer un système, gérer les fichiers, surveiller les processus et résoudre des problèmes réseau.

## 🎯 Objectifs
- Apprendre les bases de **cmd.exe**.  
- Récupérer des informations système et réseau.  
- Gérer les fichiers et dossiers.  
- Lister et gérer les processus en cours.  
- Explorer les commandes pratiques pour l’administration et le troubleshooting.

## 🛠️ Outils et concepts
- **cmd.exe** : interpréteur de commandes par défaut sous Windows.  
- **systeminfo, ver** : récupérer les infos système.  
- **ipconfig, ping, tracert, nslookup, netstat** : diagnostic réseau.  
- **dir, cd, type, copy, del** : gestion des fichiers et répertoires.  
- **tasklist, taskkill** : gestion des processus.  
- **shutdown** : redémarrage et arrêt système.  

## 📚 Résumé du contenu
### 🔹 Introduction
- Comparaison GUI vs CLI.  
- Avantages du CLI : efficacité, automatisation, gestion distante (via SSH).  

### 🔹 Basic System Information
- **ver** → version de Windows.  
- **systeminfo** → infos système détaillées (OS, architecture, processeurs, mémoire).  
- **set** → variables d’environnement.  

### 🔹 Network Troubleshooting
- **ipconfig /all** → config réseau détaillée.  
- **ping** → test de connectivité.  
- **tracert** → suivi du chemin réseau.  
- **nslookup** → résolution DNS.  
- **netstat -ano** → connexions actives et ports ouverts.  

### 🔹 File and Disk Management
- **dir** → lister les fichiers/dossiers.  
- **cd** → naviguer entre répertoires.  
- **mkdir / rmdir** → créer/supprimer un répertoire.  
- **type** → lire un fichier texte.  
- **copy / move / del** → gestion des fichiers.  

### 🔹 Task and Process Management
- **tasklist** → lister les processus.  
- **tasklist /FI "imagename eq X"** → filtrer par nom.  
- **taskkill /PID X** → tuer un processus par PID.  

### 🔹 Conclusion
- Autres commandes utiles :  
  - **chkdsk** : vérifier le disque.  
  - **driverquery** : lister les pilotes.  
  - **sfc /scannow** : vérifier et réparer les fichiers système.  
- **shutdown /r** : redémarrage.  
- **shutdown /a** : annuler un arrêt planifié.  

## 📌 Points clés
- `cmd.exe` est l’outil de base pour administrer Windows en CLI.  
- Savoir récupérer des infos système et réseau rapidement est crucial.  
- La gestion des processus avec `tasklist` et `taskkill` est utile en troubleshooting.  
- Beaucoup de commandes acceptent l’option **/?** pour afficher l’aide.  

## ✅ Ce que j’ai appris
- Compréhension des principales commandes de **cmd.exe**.  
- Diagnostic réseau de base (IP, ping, DNS, routes, ports).  
- Navigation et manipulation de fichiers via CLI.  
- Gestion des processus Windows par la ligne de commande.  
- Préparation à utiliser PowerShell pour des tâches plus avancées.  

## 🔑 Mots-clés
cmd.exe, systeminfo, ipconfig, nslookup, netstat, ping, tracert, tasklist, taskkill, shutdown, Windows CLI  

## 📚 Ressources
- [Documentation Microsoft – Command-line reference](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/windows-commands)  
- [Cheat Sheet Windows CMD](https://ss64.com/nt/)  
