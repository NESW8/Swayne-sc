# TryHackMe – Active Directory Basics  
📡 Introduction aux concepts et composants essentiels d’Active Directory  

## 📄 Description  
Cette room introduit **Active Directory (AD)**, le service centralisé de gestion des identités et ressources dans les environnements Windows. On y découvre les domaines, utilisateurs, groupes, ordinateurs et politiques, ainsi que leur rôle dans une infrastructure d’entreprise.  

## 🎯 Objectifs  
- Comprendre ce qu’est **Active Directory** et ses usages.  
- Identifier les composants clés : **domaines, OUs, contrôleurs de domaine (DC)**.  
- Gérer utilisateurs, groupes, ordinateurs et politiques.  
- Explorer les mécanismes d’authentification (Kerberos & NTLM).  
- Comprendre la notion de **forêts et relations de confiance**.  

## 🛠️ Outils et concepts  
- **Active Directory Domain Services (AD DS)** : service central de gestion.  
- **Domain Controller (DC)** : serveur gérant l’AD.  
- **Organizational Units (OU)** : conteneurs hiérarchiques pour organiser utilisateurs, groupes et machines.  
- **Group Policy Objects (GPO)** : application de politiques de sécurité et de configuration.  
- **Kerberos** : protocole d’authentification par tickets.  
- **NTLM** : protocole d’authentification par challenge/réponse (hérité).  

## 📚 Résumé du contenu  

### 🔑 Concepts fondamentaux  
- **AD** = annuaire centralisé regroupant utilisateurs, groupes, ordinateurs et ressources.  
- **Domaines** = regroupement logique sous l’autorité d’un contrôleur de domaine.  
- **OUs** = permettent de structurer et déléguer l’administration.  
- **Groupes** = attribuent droits et permissions aux utilisateurs.  

### 👥 Gestion des identités  
- Création et organisation des comptes utilisateurs.  
- Attribution de rôles via des **groupes de sécurité** (Domain Admins, Server Operators, etc.).  
- Organisation en OUs (ex : IT, Marketing, Management).  

### 🖥️ Gestion des machines  
- Classement des machines dans l’AD (Workstations, Servers, Domain Controllers).  
- Application de règles spécifiques par type de machine.  

### 🛡️ Politiques & Sécurité  
- Les **GPOs** définissent des configurations (sécurité, restrictions, mots de passe…).  
- Application ciblée aux OUs ou à tout le domaine.  

### 🔐 Authentification  
- **Kerberos** : basé sur des tickets (TGT, TGS), sécurisé et rapide.  
- **NTLM** : ancien protocole, encore présent pour compatibilité.  

### 🌳 Forêts & Relations de confiance  
- **Arbre (Tree)** : plusieurs domaines partageant le même namespace.  
- **Forêt (Forest)** : plusieurs arbres avec namespaces différents.  
- **Trust relationships** : autorisent l’accès entre domaines distincts.  

## 📌 Points essentiels  
- AD simplifie la gestion **centralisée** des utilisateurs et machines.  
- Les **Domain Controllers** sont critiques (sécurité & disponibilité).  
- Les **OUs + GPOs** permettent une administration fine et hiérarchisée.  
- **Kerberos** est le protocole par défaut, mais NTLM reste présent.  
- Les **forêts** permettent de fédérer plusieurs environnements AD.  

## ✅ Ce que j’ai appris  
- Compréhension du rôle d’AD dans les entreprises.  
- Différence entre domaines, OUs, arbres et forêts.  
- Gestion et délégation via **Group Policy**.  
- Différences entre Kerberos et NTLM (avantages/inconvénients).  
- Importance des **trust relationships** dans des environnements multi-domaines.  

## 🔑 Mots-clés  
Active Directory, Domain Controller, Organizational Unit, GPO, Kerberos, NTLM, Domain Trust, Forest  

## 📚 Ressources  
- [Microsoft Docs – Active Directory](https://learn.microsoft.com/en-us/windows-server/identity/active-directory-domain-services)  
- [Kerberos Explained](https://web.mit.edu/kerberos/)  
- [NTLM Authentication](https://learn.microsoft.com/en-us/windows-server/security/kerberos/ntlm-overview)  
