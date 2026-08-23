# 🛡️ Cyber Security Learning Journey – TryHackMe

Ce dépôt documente ma reconversion vers la cybersécurité sous forme de rapports techniques structurés, rédigés room par room sur TryHackMe.
L'objectif professionnel visé est un poste **SOC / GRC** (analyse d'alertes, réponse à incident, conformité et gouvernance du risque), appuyé sur une **base offensive solide** (reconnaissance, Metasploit, méthodologie de test d'intrusion) — parce qu'on ne détecte bien que ce qu'on sait reproduire.
Chaque write-up suit un format constant : contexte, méthodologie et commandes, difficultés rencontrées, acquis.

🏅 **Certification obtenue :** [Pre Security Path – TryHackMe (SEC0)](certifications/THM-7Z2MQXNRFS.pdf)

---

## 🧭 Skills matrix

| Compétence | Niveau actuel | Preuve |
|------------|---------------|--------|
| **Réseaux — modèles & fondamentaux** (OSI, TCP/IP, LAN, sous-réseaux) | Intermédiaire | [OSI Model](01_Beginner/OSI_Model.md) · [Packets & Frames](01_Beginner/Packets_&_Frames.md) · [Networking Concepts](02_Cybersecurity101/Networking_Concepts.md) · [Networking Essentials](02_Cybersecurity101/Networking_Essentials.md) |
| **Réseaux — protocoles applicatifs** (DNS, HTTP, DHCP, SMTP) | Intermédiaire | [DNS in Detail](01_Beginner/DNS_in_Detail.md) · [HTTP in Detail](01_Beginner/HTTP_in_Detail.md) · [Networking Core Protocols](02_Cybersecurity101/Networking_Core_Protocols.md) |
| **Réseaux — protocoles sécurisés** (TLS, SSH, VPN) | Intermédiaire | [Networking Secure Protocols](02_Cybersecurity101/Networking_Secure_Protocols.md) |
| **Analyse de trafic réseau** (Wireshark, tcpdump, filtres BPF) | Intermédiaire | [Wireshark: The Basics](02_Cybersecurity101/Wireshark_Basics.md) · [Tcpdump: The Basics](02_Cybersecurity101/Tcpdump_Basics.md) |
| **Linux** (arborescence, permissions, processus, cron, logs, shells) | Intermédiaire | [Linux Fundamentals 1](01_Beginner/Linux_Fundamentals_Part_1.md) · [2](01_Beginner/Linux_Fundamentals_Part_2.md) · [3](01_Beginner/Linux_Fundamentals_Part_3.md) · [Linux Shells](02_Cybersecurity101/Linux_Shells.md) |
| **Windows** (système de fichiers, comptes, services, durcissement) | Intermédiaire | [Windows Fundamentals 1](01_Beginner/Windows_Fundamentals_1.md) · [2](01_Beginner/Windows_Fundamentals_2.md) · [3](01_Beginner/Windows_Fundamentals_3.md) |
| **Windows CLI & PowerShell** | Intermédiaire | [Windows Command Line](02_Cybersecurity101/Windows_Command_Line.md) · [Windows PowerShell](02_Cybersecurity101/Windows_PowerShell.md) |
| **Active Directory** (objets, OU, GPO, authentification) | Débutant | [Active Directory Basics](02_Cybersecurity101/Active_Directory_Basics.md) |
| **Reconnaissance & scan de ports** (Nmap) | Intermédiaire | [Nmap: The Basics](02_Cybersecurity101/Nmap_Basics.md) |
| **Metasploit** (msfconsole, modules, exploitation, Meterpreter) | Débutant *(en cours – module 7)* | 🔄 [Write-ups à venir](02_Cybersecurity101/README.md) |
| **Méthodologie de pentest** (recon → énumération → exploitation → rapport) | Débutant | [Offensive Security Intro](01_Beginner/Offensive_Security_Intro.md) · [Nmap: The Basics](02_Cybersecurity101/Nmap_Basics.md) |
| **Sécurité défensive / SOC** (triage d'alertes, SIEM, IOC) | Débutant | [Defensive Security Intro](01_Beginner/Defensive_Security_Intro.md) |
| **OSINT & recherche d'information** (dorks, CVE, bases de vulnérabilités) | Intermédiaire | [Search Skills](02_Cybersecurity101/Search_Skills.md) |
| **Fonctionnement du web** (front/back, injection HTML, exposition de données) | Débutant | [How Websites Work](01_Beginner/How_Websites_Work.md) · [Putting it All Together](01_Beginner/Putting_it_All_Together.md) |
| **Documentation & restitution technique** | Intermédiaire | L'ensemble des write-ups de ce dépôt + [template standardisé](templates/room-writeup-template.md) |

> **Échelle** — *Débutant* : notions comprises, mise en pratique guidée. *Intermédiaire* : mise en œuvre autonome sur un cas simple. *Avancé* : maîtrise en environnement complexe, capacité à former.

---

## 🗺️ Roadmap de progression

| # | Parcours | Statut | Focus |
|---|----------|--------|-------|
| 1 | **Pre Security** | ✅ **Terminé** — [certificat SEC0](certifications/THM-7Z2MQXNRFS.pdf) | Réseaux, Linux, Windows, web |
| 2 | **Cyber Security 101** | 🔄 **En cours — 48 %** (module 7 : Exploitation Basics) | Outils réseau, crypto, exploitation, web hacking, défense |
| 3 | **SOC Level 1** | ⬜ **À venir** | SIEM, threat intelligence, DFIR, analyse de logs |
| 4 | **Gouvernance & conformité (GRC)** | ⬜ **Objectif moyen terme** | ISO 27001, NIST CSF, analyse de risque |

### Détail du parcours en cours — Cyber Security 101

| Module | Statut |
|--------|--------|
| 1. Start Your Cyber Security Journey | ✅ [write-up](02_Cybersecurity101/Search_Skills.md) |
| 2. Linux Fundamentals | ✅ [write-ups](01_Beginner/Linux_Fundamentals_Part_1.md) |
| 3. Windows and AD Fundamentals | ✅ [write-up](02_Cybersecurity101/Active_Directory_Basics.md) |
| 4. Command Line | ✅ [write-ups](02_Cybersecurity101/README.md) |
| 5. Networking | ✅ [write-ups](02_Cybersecurity101/README.md) |
| 6. Cryptography | 🔄 rooms suivies — *write-ups à rédiger* |
| 7. Exploitation Basics *(Metasploit, Blue)* | 🔄 **en cours** |
| 8. Web Hacking · 9. Offensive Tooling · 10. Defensive Security · 11. Security Solutions · 12. Defensive Tooling · 13. Build Your Career | ⬜ à venir |

---

## 📚 Write-ups par room

### 1️⃣ Pre Security — [`01_Beginner/`](01_Beginner/README.md)

**Introduction à la cybersécurité**
- [Intro to Offensive Security](01_Beginner/Offensive_Security_Intro.md)
- [Intro to Defensive Security](01_Beginner/Defensive_Security_Intro.md)
- [Careers in Cyber](01_Beginner/Cyber_Careers.md)

**Réseaux & Internet**
- [What is Networking?](01_Beginner/Networking.md)
- [Intro to LAN](01_Beginner/Intro_to_LAN.md)
- [OSI Model](01_Beginner/OSI_Model.md)
- [Packets & Frames](01_Beginner/Packets_&_Frames.md)
- [Network Expansion](01_Beginner/Network_Expansion.md)
- [DNS in Detail](01_Beginner/DNS_in_Detail.md)
- [HTTP in Detail](01_Beginner/HTTP_in_Detail.md)
- [How Websites Work](01_Beginner/How_Websites_Work.md)
- [Putting it All Together](01_Beginner/Putting_it_All_Together.md)

**Systèmes**
- [Linux Fundamentals Part 1](01_Beginner/Linux_Fundamentals_Part_1.md) · [Part 2](01_Beginner/Linux_Fundamentals_Part_2.md) · [Part 3](01_Beginner/Linux_Fundamentals_Part_3.md)
- [Windows Fundamentals 1](01_Beginner/Windows_Fundamentals_1.md) · [2](01_Beginner/Windows_Fundamentals_2.md) · [3](01_Beginner/Windows_Fundamentals_3.md)

### 2️⃣ Cyber Security 101 — [`02_Cybersecurity101/`](02_Cybersecurity101/README.md)

- [Search Skills](02_Cybersecurity101/Search_Skills.md)
- [Active Directory Basics](02_Cybersecurity101/Active_Directory_Basics.md)
- [Windows Command Line](02_Cybersecurity101/Windows_Command_Line.md)
- [Windows PowerShell](02_Cybersecurity101/Windows_PowerShell.md)
- [Linux Shells](02_Cybersecurity101/Linux_Shells.md)
- [Networking Concepts](02_Cybersecurity101/Networking_Concepts.md)
- [Networking Essentials](02_Cybersecurity101/Networking_Essentials.md)
- [Networking Core Protocols](02_Cybersecurity101/Networking_Core_Protocols.md)
- [Networking Secure Protocols](02_Cybersecurity101/Networking_Secure_Protocols.md)
- [Wireshark: The Basics](02_Cybersecurity101/Wireshark_Basics.md)
- [Tcpdump: The Basics](02_Cybersecurity101/Tcpdump_Basics.md)
- [Nmap: The Basics](02_Cybersecurity101/Nmap_Basics.md)

---

## 📂 Structure du dépôt

| Dossier | Contenu |
|---------|---------|
| [`01_Beginner/`](01_Beginner/README.md) | Write-ups du path Pre Security — réseaux, systèmes, web |
| [`02_Cybersecurity101/`](02_Cybersecurity101/README.md) | Write-ups du path Cyber Security 101 — outils, méthodologies, scénarios pratiques |
| [`certifications/`](certifications/) | Certificats obtenus (PDF) |
| [`templates/`](templates/room-writeup-template.md) | Template de write-up réutilisable pour chaque nouvelle room |

---

## ✍️ Méthode de travail

Chaque room terminée donne lieu à un rapport rédigé à partir du [template commun](templates/room-writeup-template.md) :
**Contexte / Objectif** → **Méthodologie & commandes** → **Difficultés rencontrées** → **Ce que j'ai appris** → **Liens utiles**.
Les difficultés et les erreurs sont documentées volontairement : elles montrent la démarche d'analyse, pas seulement le résultat.
