---
# TryHackMe – Nmap  
📡 Découverte et analyse réseau avec l’outil de scan incontournable

## 📄 Description
Cette room présente **Nmap**, un scanner réseau puissant et flexible. Elle explique comment découvrir les hôtes vivants, identifier les ports et services en écoute, détecter les versions et le système d’exploitation, contrôler le timing pour être discret ou rapide, et sauvegarder les résultats dans différents formats.

## 🎯 Objectifs
- Découvrir les hôtes actifs sur un réseau.  
- Identifier les ports et services ouverts sur ces hôtes.  
- Détecter les versions de services et l’OS des cibles.  
- Contrôler la vitesse et la discrétion d’un scan (timing).  
- Sauvegarder et formater les résultats pour analyse ultérieure.

## 🛠️ Outils et concepts
- **Nmap** — scanner réseau (installation habituelle : `apt install nmap` / `brew install nmap`).  
- **Host discovery** : `-sn` (ping scan), ARP vs ICMP/TCP discovery selon réseau local ou distant.  
- **TCP connect scan** : `-sT` (complète le 3-way handshake, bruyant).  
- **SYN scan** : `-sS` (scan "furtif", n’effectue pas la connexion complète).  
- **UDP scan** : `-sU` (plus lent, utile pour DNS, SNMP, NTP, etc.).  
- **Service & version detection** : `-sV`.  
- **OS detection** : `-O`.  
- **Scan complet/forcé** : `-A` (OS + version + traceroute), `-Pn` (traiter tous les hôtes comme en ligne).  
- **Timing** : `-T0` (paranoid) → `-T5` (insane).  
- **Parallelisme / rate** : `--min-parallelism`, `--max-parallelism`, `--min-rate`, `--max-rate`.  
- **Verbosity / Debug** : `-v`, `-vv`, `-d`, `-d2` ...  
- **Sortie / rapport** : `-oN` (normal), `-oX` (XML), `-oG` (grepable), `-oA` (all formats).

---

## 📚 Résumé du contenu

### 1. Introduction & contexte
Nmap est l’outil de référence pour l’énumération réseau. Il propose des méthodes adaptées aux réseaux locaux (ARP discovery) et aux réseaux distants (ICMP/TCP/UDP). L’approche manuelle (ping, arp-scan, telnet) est lente et limitée ; Nmap automatise et centralise ces tâches.

### 2. Host Discovery (Qui est en ligne)
- **Local network (ARP)** : `nmap -sn 192.168.66.0/24` détecte rapidement les hôtes avec ARP.  
- **Remote networks** : Nmap utilise ICMP, TCP, UDP. Exemple : `nmap -sn 192.168.11.0/24`.  
- Options utiles : `-PS`/`-PA`/`-PU` pour forcer l’usage de probes (TCP SYN, TCP ACK, UDP).  
- **List-only** : `-sL` liste les cibles sans les scanner.

**Exemples :**
```bash
# Découverte ARP sur réseau local
nmap -sn 192.168.66.0/24

# Traiter tous les hôtes comme online (utile si host discovery échoue)
nmap -Pn 192.168.11.0/24
```

### 3. Port Scanning (Qui écoute)
- **TCP connect scan** : `-sT` (par défaut si pas de privilèges root).  
- **SYN scan** : `-sS` (nécessite privilèges root, plus discret).  
- **UDP scan** : `-sU` (utiliser si on cible services UDP).  
- **Fast / limited ports** : `-F` (100 ports courants), `-p-` (tous les ports), `-p 1-1000` (plage).  

**Exemples :**
```bash
# SYN stealth scan (privilèges root)
sudo nmap -sS 192.168.124.211

# Scan UDP (lent)
sudo nmap -sU 192.168.124.211

# Scan complet de tous les ports
sudo nmap -p- 192.168.124.211
```

**Comportements TCP vus :**
- `-sT` : complète la 3-way handshake (SYN, SYN-ACK, ACK) → plus facilement détectable.  
- `-sS` : envoie SYN et lit la réponse (SYN-ACK → port ouvert ; RST → port fermé), n’achève pas la connexion.  

### 4. Version & OS Detection (Extraire plus d’informations)
- `-sV` : renseigne la version des services détectés (ex. `OpenSSH 8.9p1`, `lighttpd 1.4.74`).  
- `-O` : déduction du système d’exploitation (ex. Linux kernel 4.x).  
- `-A` : option "agressive" combinant `-O -sV --traceroute` et quelques scripts NSE par défaut.

**Exemple :**
```bash
sudo nmap -sS -sV -O 192.168.124.211
# ou pour tout activer
sudo nmap -A 192.168.124.211
```

### 5. Timing : How fast is fast
- Templates : `-T0` (paranoid), `-T1` (sneaky), `-T2` (polite), `-T3` (normal, défaut), `-T4` (aggressive), `-T5` (insane).  
- Impact : temps total du scan, délai entre probes, risque d’IDS/IPS.  
- Contrôle fin : `--min-parallelism`, `--max-parallelism`, `--min-rate`, `--max-rate`, `--host-timeout`.  

**Exemple :**
```bash
# SYN scan sur les 100 ports les plus courants en timing agressif
sudo nmap -sS -F -T4 192.168.124.148
```

### 6. Output / Verbosity / Debugging
- **Verbosity** : `-v`, `-vv` pour plus de messages.  
- **Debug** : `-d`, `-d2`... pour logs très détaillés (utile pour apprentissage du flux).  
- **Export** :  
  - `-oN filename` → sortie lisible (normal).  
  - `-oX filename` → XML.  
  - `-oG filename` → grepable (pratique pour scripts).  
  - `-oA basename` → génère `basename.nmap`, `basename.xml`, `basename.gnmap`.

**Exemple :**
```bash
# Verbose + sauvegarde en tous formats
sudo nmap -sS -sV -O -v -oA scan_gateway 192.168.139.1
```

### 7. Conclusion & bonnes pratiques
- Lancer Nmap avec **sudo** (pour utiliser les scans furtifs et toutes les fonctionnalités). Si exécuté sans privilèges, Nmap utilisera `-sT` par défaut pour les scans TCP.  
- Utiliser `-Pn` si le host discovery ne retourne rien mais que l’on sait que les hôtes sont en ligne.  
- Adapter le `-T` et les options de parallelisme selon le réseau (éviter d’être trop agressif sur des réseaux sensibles).  
- Sauvegarder les résultats (`-oA`) pour l’analyse et exploitation ultérieures.

---

## 📌 Ports et services (exemples mentionnés)
- `22/tcp` — SSH (`OpenSSH 8.9p1` dans l’exemple).  
- `80/tcp` — HTTP (ex. `lighttpd 1.4.74`).  
- `53/udp` — DNS.  
- `123/udp` — NTP.  
- `161/udp` — SNMP.  

---

## ✅ Ce que j’ai appris
- Quand utiliser ARP vs ICMP/TCP pour la découverte d’hôtes.  
- Différences opérationnelles entre `-sT` et `-sS`.  
- Limitations et lenteurs des scans UDP (`-sU`) et techniques pour les optimiser.  
- Comment forcer un scan (tous les hôtes en ligne) avec `-Pn`.  
- Exporter des scans de manière scriptable et lisible (`-oG`, `-oX`, `-oA`).  
- Ajuster la discrétion/rapidité via `-T` et `--max-rate`, `--min-parallelism`, etc.

---

## 🔑 Mots-clés
Nmap, reconnaissance, host discovery, SYN scan, connect scan, UDP scan, OS detection, service detection, timing, verbosity, reporting, pentest.

---

## 📚 Ressources
- Documentation officielle Nmap : https://nmap.org/book/man.html  
- Guides & cheat sheets (SANS, etc.) — utile pour révision rapide des options.  
- TryHackMe — Nmap room (pour pratiquer les commandes et interpréter les captures).

---
