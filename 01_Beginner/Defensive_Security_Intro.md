# TryHackMe – Intro to Defensive Security

| | |
|---|---|
| **Path / Module** | Pre Security – Introduction to Cyber Security |
| **Difficulté** | Info |
| **Date de complétion** | [À COMPLÉTER] |
| **Lien room** | [https://tryhackme.com/room/defensivesecurity](https://tryhackme.com/room/defensivesecurity) |
| **Tags** | `blue-team` `soc` `siem` `threat-intel` `dfir` |

---

## 🎯 Contexte / Objectif de la room

- **Contexte :** pendant offensif de la room précédente. Elle présente les métiers et les fonctions de la défense : SOC, threat intelligence, DFIR, malware analysis — c'est la room qui cadre directement mon orientation SOC.
- **Objectifs pédagogiques :**
  - Distinguer sécurité défensive et sécurité offensive.
  - Comprendre le rôle d'un SOC : surveillance, détection, triage et réponse.
  - Découvrir le SIEM comme point de centralisation des logs et des alertes.
  - Situer la threat intelligence, la réponse à incident et l'analyse de malware dans la chaîne défensive.
  - Réaliser un premier triage d'alertes sur un tableau de bord simulé.
- **Pertinence métier (SOC / GRC / offensif) :** c'est le vocabulaire quotidien d'un analyste SOC L1 (alerte, triage, faux positif, escalade). Côté GRC, ces fonctions sont exactement celles qu'un référentiel comme le NIST CSF classe sous *Detect* et *Respond*.

---

## 🛠️ Méthodologie & commandes utilisées

*Room principalement conceptuelle : la mise en pratique se fait via une interface web simulée, sans ligne de commande.*

### 1. Cartographie des fonctions défensives

Prise de notes sur les quatre briques présentées : SOC, Threat Intelligence, DFIR (Digital Forensics & Incident Response), Malware Analysis.

**Résultat / observation :** [À COMPLÉTER — synthèse personnelle du périmètre de chaque fonction]

### 2. Triage d'alertes sur le SIEM simulé

Analyse des événements remontés, identification de l'alerte réellement malveillante parmi le bruit, puis blocage de l'adresse IP source.

**Résultat / observation :** [À COMPLÉTER — nature de l'alerte, IP identifiée, décision prise]

### 3. Analyse d'un fichier suspect

Soumission de l'empreinte du fichier à une base de threat intelligence pour statuer sur sa dangerosité.

**Résultat / observation :** [À COMPLÉTER — verdict obtenu]

### Récapitulatif des concepts clés

| Élément | Rôle |
|---------|------|
| SOC | Surveillance continue, détection et réponse aux incidents |
| SIEM | Collecte et corrélation des logs, génération d'alertes |
| Threat Intelligence | Connaissance de l'adversaire (TTP, IOC) pour anticiper |
| DFIR | Investigation post-incident et remédiation |
| Malware Analysis | Compréhension du comportement d'un code malveillant |

---

## 🧩 Difficultés rencontrées

| Difficulté | Cause identifiée | Résolution |
|------------|------------------|------------|
| [À COMPLÉTER] | [À COMPLÉTER] | [À COMPLÉTER] |

---

## 📚 Ce que j'ai appris

- **Concepts :** cycle de vie d'une alerte, distinction vrai/faux positif, notion d'IOC, complémentarité prévention / détection / réponse.
- **Outils / commandes maîtrisés :** lecture d'un tableau de bord SIEM, consultation d'une base de threat intelligence.
- **Réflexe professionnel à retenir :** une alerte n'est pas un incident — le triage consiste d'abord à qualifier avant d'escalader.
- **À approfondir :** [À COMPLÉTER — ex. MITRE ATT&CK, règles Sigma, playbooks de réponse]

---

## 🔗 Liens utiles

- Room TryHackMe : https://tryhackme.com/room/defensivesecurity
- MITRE ATT&CK : https://attack.mitre.org/
- NIST Cybersecurity Framework : https://www.nist.gov/cyberframework
- Écosystème : [Offensive Security Intro](Offensive_Security_Intro.md) · [Careers in Cyber](Cyber_Careers.md)
