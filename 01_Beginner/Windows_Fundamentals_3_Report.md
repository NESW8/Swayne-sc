---
# TryHackMe – Windows Fundamentals 3  
📡 Exploration des outils et paramètres de sécurité intégrés à Windows

## 📄 Description
Cette room explore les fonctionnalités de sécurité intégrées à Windows, telles que Windows Update, Windows Security, le pare-feu, BitLocker et le service Volume Shadow Copy.  
L'objectif est de comprendre comment ces outils protègent le système et comment les configurer efficacement.

## 🎯 Objectifs
- Comprendre le rôle et l'importance de **Windows Update**.
- Utiliser et configurer **Windows Security** et ses modules.
- Paramétrer la **protection antivirus** et les profils réseau.
- Découvrir **BitLocker** et le rôle du **TPM**.
- Comprendre le fonctionnement du **Volume Shadow Copy Service (VSS)**.

## 🛠️ Outils et concepts
- **Windows Update** : mise à jour et correctifs de sécurité.
- **Windows Security** : interface centrale regroupant les protections système.
- **Microsoft Defender Antivirus** : protection en temps réel contre les menaces.
- **Pare-feu Windows** : gestion des connexions entrantes/sortantes.
- **SmartScreen** : protection contre les applications/sites non reconnus.
- **BitLocker** : chiffrement de disque intégral.
- **TPM (Trusted Platform Module)** : sécurité matérielle cryptographique.
- **Volume Shadow Copy Service** : sauvegardes instantanées et restaurations.

## 📚 Résumé du contenu

### 🔄 Windows Update
- Service qui fournit mises à jour de sécurité et améliorations.
- **Patch Tuesday** : publication le 2ᵉ mardi du mois (sauf urgence).
- Accès via `Paramètres → Mise à jour et sécurité` ou commande :
  ```powershell
  control /name Microsoft.WindowsUpdate
  ```
- Statuts : aucune mise à jour, mise à jour dispo, redémarrage requis.

### 🛡️ Windows Security
- Zones principales :
  - Virus & threat protection
  - Firewall & network protection
  - App & browser control
  - Device security
- Codes couleur :
  - 🟢 Vert = protégé
  - 🟡 Jaune = attention
  - 🔴 Rouge = action urgente

### 🦠 Virus & Threat Protection
- **Current threats** : menaces détectées en temps réel.
- **Settings** : protection en temps réel, cloud, exclusions, notifications.
- Modes de scan : Quick, Full, Custom.
- Protection cloud et soumission auto recommandées.

### 🌐 Firewall & Network Protection
- Profils : Domain, Private, Public.
- Paramétrage avancé via `wf.msc`.
- Possibilité de bloquer toutes connexions entrantes.

### 🌍 App & Browser Control
- **SmartScreen** : blocage/avertissement/désactivation.
- **Exploit protection** : DEP, ASLR, CFG.

### 💻 Device Security
- **Core isolation** (Memory Integrity) : bloque code malveillant en mémoire.
- **TPM** : puce pour opérations cryptographiques et intégrité système.

### 🔐 BitLocker
- Chiffrement disque total.
- Fonctionne idéalement avec TPM v1.2+.
- Sans TPM : clé USB de démarrage nécessaire.

### 📀 Volume Shadow Copy Service (VSS)
- Crée instantanés système.
- Utilisé pour restauration système et sauvegardes.
- Cible fréquente des ransomwares.

## 📌 Ports et services
- Windows Update Service
- Microsoft Defender Antivirus
- Windows Firewall Service
- Volume Shadow Copy Service

## ✅ Ce que j’ai appris
- Configurer et vérifier Windows Update pour maintenir un système sécurisé.
- Utiliser Windows Security comme tableau de bord de protection.
- Paramétrer efficacement le pare-feu selon le profil réseau.
- Comprendre et activer le chiffrement avec BitLocker.
- Exploiter VSS pour restaurer un système.

## 🔑 Mots-clés
Windows Update, Windows Security, Defender, Pare-feu, BitLocker, TPM, VSS, Antivirus, Patch Tuesday

## 📚 Ressources
- [Microsoft – Windows Update](https://support.microsoft.com/windows-update)
- [Microsoft – Windows Security](https://support.microsoft.com/windows-security)
- [BitLocker Overview](https://docs.microsoft.com/windows/security/information-protection/bitlocker/bitlocker-overview)
- [Volume Shadow Copy Service](https://docs.microsoft.com/windows-server/storage/file-server/volume-shadow-copy-service)

---
