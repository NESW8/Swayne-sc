---
# TryHackMe – Tcpdump: The Basics
📡 Comprendre et manipuler les captures réseau avec tcpdump

## 📄 Description
Cette room présente **tcpdump**, un outil en ligne de commande pour capturer et analyser le trafic réseau. On y apprend à sélectionner une interface, enregistrer et relire des captures, filtrer les paquets (par host, port, protocole), utiliser des expressions avancées (opérations binaires et filtrage sur octets d'entête) et afficher les paquets dans différents formats (ASCII, hexadécimal, lien-niveau).

## 🎯 Objectifs
- Capturer des paquets et les sauvegarder dans un fichier pcap.  
- Appliquer des filtres pour limiter les paquets capturés ou affichés.  
- Contrôler l'affichage des paquets (brève, verbose, hex, ASCII).

## 🛠️ Outils et concepts
- **tcpdump** — capture et affichage de paquets (linux / BSD / macOS).  
- **Interface** : `-i INTERFACE` (ex. `-i eth0`, `-i any`).  
- **Écrire / lire fichiers** : `-w FILE` pour écrire, `-r FILE` pour relire.  
- **Compter** : `-c COUNT` pour n paquets.  
- **Résolution noms** : `-n` ne pas résoudre IP; `-nn` ne pas résoudre IP ni ports.  
- **Verbosity / Quick** : `-v`, `-vv` ; `-q` quick output.  
- **Link-level** : `-e` affiche en-têtes lien (MAC).  
- **Affichage ASCII / Hex** : `-A`, `-xx`, `-X`.  
- **Filtres BPF** : `host`, `src`, `dst`, `port`, `src port`, `dst port`, `tcp`, `udp`, `icmp` + opérateurs `and`, `or`, `not`.  
- **Filtres avancés** : `greater`, `less` (longueur), accès aux bytes d'entêtes via `tcp[off]` / `ip[off]` et opérations binaires (AND, OR, NOT).

---

## 📚 Résumé du contenu

### 1. Spécifier l'interface de capture
- L'option clé est `-i INTERFACE`. `-i any` écoute sur toutes les interfaces.  
- Exemple pour lister les interfaces : `ip a` ou `ifconfig`.

**Exemples :**
```bash
# Écouter l'interface eth0
sudo tcpdump -i eth0

# Écouter toutes les interfaces
sudo tcpdump -i any
```

### 2. Sauvegarder et relire des captures
- `-w file.pcap` écrit la capture dans un fichier pcap (lisible par Wireshark).  
- `-r file.pcap` relit un fichier pcap et l'affiche selon les options fournies.

**Exemples :**
```bash
# Écrire 50 paquets sur eth0
sudo tcpdump -i eth0 -c 50 -w capture.pcap

# Relire un pcap et afficher en ASCII
tcpdump -r capture.pcap -A
```

### 3. Limiter le nombre de paquets et éviter les résolutions DNS/ports
- `-c COUNT` pour arrêter après un nombre de paquets.  
- `-n` / `-nn` pour éviter les résolutions (utile pour vitesse/fiabilité).

**Exemple :**
```bash
sudo tcpdump -i eth0 -c 5 -n
```

### 4. Vérbosité et formats d'affichage
- `-q` : output rapide / succinct (timestamp + addresses + ports).  
- `-e` : afficher les en-têtes lien (MAC).  
- `-A` : afficher le payload en ASCII (utile pour lire HTTP en clair).  
- `-xx` : afficher paquets en hexadécimal (octet par octet).  
- `-X` : hex + ASCII côte à côte.

**Exemples :**
```bash
# Quick output
tcpdump -r TwoPackets.pcap -q

# Afficher adresses MAC
tcpdump -r TwoPackets.pcap -e

# Afficher payload en ASCII
tcpdump -r TwoPackets.pcap -A

# Afficher hexadécimal
tcpdump -r TwoPackets.pcap -xx

# Hex + ASCII
tcpdump -r TwoPackets.pcap -X
```

### 5. Filtres simples (host/port/protocol)
- `host <IP_or_name>` : paquets ayant pour source ou destination cette IP/nom.  
- `src host <IP>` / `dst host <IP>` : filtrage source/destination.  
- `port <NUM>` / `src port <NUM>` / `dst port <NUM>` : filtrer par port.  
- `tcp` / `udp` / `icmp` : filtrer par protocole.

**Exemples :**
```bash
# Capture tous les paquets impliquant 192.168.124.148
sudo tcpdump -i eth0 host 192.168.124.148 -w traffic.pcap

# Capture paquets vers ou depuis le port 53 (DNS)
sudo tcpdump -i eth0 port 53
```

### 6. Opérateurs logiques
- `and`, `or`, `not` (ex: `tcpdump host 1.2.3.4 and port 80`).  
- On peut combiner conditions sur src/dst/port/proto.

**Exemple :**
```bash
# Paquets TCP vers 10.0.0.5 destinés au port 80
sudo tcpdump -i eth0 tcp and dst host 10.0.0.5 and dst port 80
```

### 7. Filtrage avancé (Header bytes et opérations binaires)
- On peut tester des octets précis dans les entêtes (utile pour flags TCP etc.). Syntaxe : `tcpdump 'tcp[13] & 0x02 != 0'` (ex. vérifier flag SYN).  
- `greater` / `less` pour la longueur des paquets.  
- Les opérations bitwise (`&`, `|`, `!`) permettent de tester flags comme `SYN`, `RST`, `ACK` en regardant un offset TCP donné.

**Exemples :**
```bash
# Paquets TCP où le byte 13 (flags) a le bit RST (0x04) défini
tcpdump 'tcp[13] & 0x04 != 0'

# Paquets plus grands que 15000 octets
tcpdump 'greater 15000'
```

### 8. Affichage et extraction d'informations utiles
- Utiliser `-n` pour obtenir rapidement IPs sans latence DNS.  
- Relire un pcap (`-r`) et combiner `-A`, `-xx`, `-e` pour analyser payload, en-têtes lien et hex.  
- Exemples pratiques vus dans la room : identification d'une requête ARP (MAC source), nombre de paquets ICMP, résolution DNS retournée dans la capture.

---

## 📌 Commandes récapitulatives (tableau)

| Commande | Explication |
|---|---|
| `tcpdump -i INTERFACE` | Capture sur une interface spécifiée |
| `tcpdump -w FILE` | Écrit la capture dans un fichier pcap |
| `tcpdump -r FILE` | Relit un fichier pcap |
| `tcpdump -c COUNT` | Capture un nombre limité de paquets |
| `tcpdump -n` / `-nn` | Ne pas résoudre IPs (et ports si -nn) |
| `tcpdump -q` | Quick, sortie concise |
| `tcpdump -e` | Affiche en-têtes link-level (MAC) |
| `tcpdump -A` | Affiche payload en ASCII |
| `tcpdump -xx` | Affiche hexadécimal |
| `tcpdump -X` | Affiche hex + ASCII |
| `tcpdump host IP` | Filtre par host (src ou dst) |
| `tcpdump src host IP` | Filtre par host source |
| `tcpdump dst host IP` | Filtre par host destination |
| `tcpdump port NUM` | Filtre par port |
| `tcpdump tcp` / `udp` / `icmp` | Filtre par protocole |
| `tcpdump 'tcp[13] & 0x02 != 0'` | Filtre avancé: tests de flags TCP (ex. SYN) |

---

## ✅ Ce que j’ai appris
- Sélectionner précisément l’interface et sauvegarder des captures pour analyse.  
- Écrire des filtres BPF simples pour capturer uniquement ce qui intéresse (host/port/proto).  
- Utiliser des opérateurs logiques pour combiner filtres.  
- Construire des filtres avancés sur octets d'entête (vérifier flags TCP).  
- Afficher des paquets en ASCII et en hexadécimal pour inspecter payloads et en-têtes.

## 🔑 Mots-clés
tcpdump, capture, pcap, BPF, interface, filters, hex, ASCII, tcpflags, header bytes, Wireshark.

## 📚 Ressources
- Page man tcpdump : `man tcpdump`  
- Tcpdump/libpcap documentation : https://www.tcpdump.org/  
- Wireshark pour analyse graphique des pcap : https://www.wireshark.org/

---

## 📝 Conclusion
Tcpdump est un outil léger et puissant pour capturer et analyser le trafic réseau en ligne de commande. Couplé à des filtres BPF et à une bonne compréhension des entêtes (IP/TCP/UDP), il devient indispensable pour diagnostiquer ou étudier le comportement réseau.

---
