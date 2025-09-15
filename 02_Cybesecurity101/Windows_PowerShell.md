# TryHackMe – Windows PowerShell  
⚡ Introduction à l’automatisation et à l’administration avec PowerShell

## 📄 Description
Cette room initie à **Windows PowerShell**, un shell et langage de script moderne développé par Microsoft.  
Contrairement à l’invite de commande traditionnelle (cmd), PowerShell est **orienté objet** et permet de manipuler des données complexes, d’automatiser des tâches et de gérer efficacement des systèmes Windows et multi-plateformes.

## 🎯 Objectifs
- Comprendre ce qu’est **PowerShell** et son approche objet.  
- Lancer PowerShell et utiliser sa syntaxe de base (`Verbe-Nom`).  
- Explorer les **cmdlets** disponibles et savoir les documenter avec `Get-Help`.  
- Naviguer dans le **système de fichiers** et manipuler des fichiers/dossiers.  
- Appliquer le **piping, filtrage et tri des données**.  
- Obtenir des **informations système et réseau** avec des cmdlets dédiés.  
- Effectuer une **analyse en temps réel** (processus, services, connexions).  
- Découvrir le **scripting PowerShell** et son rôle en cybersécurité.

## 🛠️ Outils et concepts
- **Cmdlets** : petites commandes orientées objet (ex. `Get-Command`, `Get-Help`).  
- **Syntaxe Verbe-Nom** : facilite la lecture et l’exécution des commandes (`Get-Process`, `Set-Location`).  
- **Piping (|)** : chaîner les commandes pour transformer et filtrer les données.  
- **Objets** : chaque résultat conserve ses propriétés et méthodes (≠ simple texte).  
- **Aliases** : raccourcis pour certaines cmdlets (`dir` → `Get-ChildItem`).  
- **Modules** : extensions téléchargeables pour enrichir PowerShell (`Find-Module`, `Install-Module`).  
- **Scripting** : automatisation via fichiers `.ps1`.

## 📚 Résumé du contenu
### 🔹 Introduction
- PowerShell est né pour dépasser les limites du **cmd.exe** et des batch scripts.  
- Basé sur le **.NET Framework**, il est extensible, multi-plateforme et orienté objet.

### 🔹 Bases et syntaxe
- Lancer PowerShell : via le menu Démarrer, la commande `powershell`, ou depuis un terminal.  
- Syntaxe principale : **Verbe-Nom** (ex. `Get-Content`, `Set-Location`).  
- Cmdlets essentielles :  
  - `Get-Command` → liste toutes les commandes.  
  - `Get-Help` → fournit documentation et exemples.  
  - `Get-Alias` → liste les raccourcis.  

### 🔹 Navigation et gestion de fichiers
- `Get-ChildItem` : liste les fichiers/dossiers (équivalent de `dir`).  
- `Set-Location` : change de dossier (équivalent de `cd`).  
- `New-Item`, `Remove-Item`, `Copy-Item`, `Move-Item` : gestion de fichiers/dossiers.  
- `Get-Content` : affiche le contenu d’un fichier (équivalent de `type` ou `cat`).

### 🔹 Piping et filtrage
- `|` permet de chaîner les cmdlets.  
- `Sort-Object` : trier par taille, date, etc.  
- `Where-Object` : filtrer selon des propriétés (`Extension -eq ".txt"`).  
- `Select-Object` : afficher uniquement certaines propriétés.  
- `Select-String` : rechercher dans les fichiers (équivalent de `grep`).

### 🔹 Informations système et réseau
- `Get-ComputerInfo` : infos système complètes.  
- `Get-LocalUser` : liste les comptes utilisateurs.  
- `Get-NetIPConfiguration`, `Get-NetIPAddress` : configuration réseau et IPs.  

### 🔹 Analyse en temps réel
- `Get-Process` : liste les processus actifs avec leur consommation.  
- `Get-Service` : état des services (running, stopped).  
- `Get-NetTCPConnection` : connexions réseau actives (utile en détection de backdoors).  
- `Get-FileHash` : calcul d’empreinte SHA256 (intégrité de fichiers).

### 🔹 Scripting
- Scripts `.ps1` → automatisation de tâches récurrentes.  
- `Invoke-Command` : exécution locale ou distante (fondamental pour l’admin & le pentest).  

## 📌 Cmdlets vues
- `Get-Command`, `Get-Help`, `Get-Alias`, `Find-Module`, `Install-Module`  
- `Get-ChildItem`, `Set-Location`, `New-Item`, `Remove-Item`, `Copy-Item`, `Move-Item`, `Get-Content`  
- `Sort-Object`, `Where-Object`, `Select-Object`, `Select-String`  
- `Get-ComputerInfo`, `Get-LocalUser`, `Get-NetIPConfiguration`, `Get-NetIPAddress`  
- `Get-Process`, `Get-Service`, `Get-NetTCPConnection`, `Get-FileHash`  
- `Invoke-Command`  

## ✅ Ce que j’ai appris
- Différence entre **cmd.exe** (texte) et **PowerShell** (objet).  
- Manipuler fichiers et répertoires avec des **cmdlets unifiées**.  
- Utiliser le **piping** pour trier, filtrer et rechercher des données.  
- Récupérer **informations système, réseau et sécurité** en ligne de commande.  
- Importance de **PowerShell en cybersécurité** : réponse à incident, analyse, automatisation.  

## 🔑 Mots-clés
PowerShell, Cmdlets, Piping, Object-oriented, Windows, Cybersecurity, Get-Process, Get-Service, Invoke-Command

## 📚 Ressources
- [Documentation officielle Microsoft PowerShell](https://learn.microsoft.com/en-us/powershell/)  
- [TryHackMe – Windows PowerShell](https://tryhackme.com/)  
- [PowerShell Gallery](https://www.powershellgallery.com/)  
