# TryHackMe – Intro to Offensive Security

| | |
|---|---|
| **Path / Module** | Pre Security – Introduction to Cyber Security |
| **Difficulté** | Info |
| **Date de complétion** | [À COMPLÉTER] |
| **Lien room** | [https://tryhackme.com/room/introtooffensivesecurity](https://tryhackme.com/room/introtooffensivesecurity) |
| **Tags** | `red-team` `pentest` `web` `méthodologie` |

---

## 🎯 Contexte / Objectif de la room

- **Contexte :** première mise en situation offensive du path Pre Security. La room fait « casser » une application web volontairement vulnérable pour montrer, concrètement, ce que recouvre le métier d'attaquant éthique.
- **Objectifs pédagogiques :**
  - Comprendre ce qu'est la sécurité offensive et le cadre légal qui l'encadre (autorisation, périmètre, engagement).
  - Découvrir la notion de contenu caché / non référencé sur un serveur web.
  - Utiliser un outil de brute-force de répertoires pour énumérer une application.
  - Identifier les principaux métiers offensifs : pentester, red teamer, chercheur en vulnérabilités.
- **Pertinence métier (SOC / GRC / offensif) :** connaître la démarche d'un attaquant est la base d'une détection pertinente côté SOC — une énumération de répertoires laisse une signature très visible dans les logs HTTP (rafales de 404). Côté GRC, c'est ce qui justifie l'exigence de tests d'intrusion réguliers dans un plan de contrôle.

---

## 🛠️ Méthodologie & commandes utilisées

### 1. Reconnaissance de l'application cible

Exploration manuelle du site pour comprendre les pages exposées et repérer ce qui n'est pas lié depuis la navigation.

**Résultat / observation :** [À COMPLÉTER — pages visibles, technologies repérées]

### 2. Énumération du contenu caché (GoBuster)

```bash
gobuster -u http://fakebank.com -w wordlist.txt dir
```

- `-u` : URL cible
- `-w` : dictionnaire de noms de répertoires à tester
- `dir` : mode énumération de répertoires

**Résultat / observation :** découverte d'un répertoire non référencé (page de transfert bancaire interne) accessible sans authentification. [À COMPLÉTER — sortie exacte obtenue]

### 3. Exploitation du défaut de contrôle d'accès

Utilisation du formulaire caché pour effectuer un virement non autorisé entre deux comptes, démontrant l'absence de contrôle d'autorisation côté serveur.

**Résultat / observation :** [À COMPLÉTER — montant transféré, message de confirmation]

### Récapitulatif des commandes clés

| Commande | Rôle |
|----------|------|
| `gobuster dir -u <url> -w <wordlist>` | Énumérer les répertoires et fichiers non référencés |

---

## 🧩 Difficultés rencontrées

| Difficulté | Cause identifiée | Résolution |
|------------|------------------|------------|
| [À COMPLÉTER] | [À COMPLÉTER] | [À COMPLÉTER] |

---

## 📚 Ce que j'ai appris

- **Concepts :** sécurité offensive vs défensive, notion de périmètre autorisé, contenu web caché, défaut de contrôle d'accès (broken access control, OWASP A01).
- **Outils / commandes maîtrisés :** GoBuster en mode `dir`, lecture d'une réponse HTTP pour distinguer 200 / 301 / 404.
- **Réflexe professionnel à retenir :** « non lié » ne veut jamais dire « protégé » — l'obscurité n'est pas un contrôle de sécurité.
- **À approfondir :** [À COMPLÉTER — ex. wordlists SecLists, ffuf, filtrage par code/longueur de réponse]

---

## 🔗 Liens utiles

- Room TryHackMe : https://tryhackme.com/room/introtooffensivesecurity
- GoBuster : https://github.com/OJ/gobuster
- OWASP Top 10 – A01 Broken Access Control : https://owasp.org/Top10/A01_2021-Broken_Access_Control/
- Écosystème : [Defensive Security Intro](Defensive_Security_Intro.md) · [Careers in Cyber](Cyber_Careers.md)
