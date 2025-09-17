# TryHackMe — Networking Essentials — Report

**Author:** Your Name  
**Room:** Networking Essentials  
**Date:** YYYY-MM-DD

---

## 1. Overview
This report documents my work through the *Networking Essentials* room on TryHackMe. It summarizes the theory covered (DHCP, ARP, ICMP, routing, NAT, TCP/UDP), the hands-on exercises performed, useful commands used, and key findings/answers from the room.

---

## 2. Learning Objectives
- Understand DHCP's DORA sequence (Discover, Offer, Request, Acknowledge).  
- Inspect ARP requests and replies; identify MAC addresses.  
- Use ICMP utilities (`ping`, `traceroute`) to troubleshoot network reachability.  
- Understand basic routing concepts and common routing protocols (OSPF, EIGRP, BGP, RIP).  
- Understand NAT and how private IPs map to a public IP and port ranges.  
- Practice basic TCP interaction using `telnet` for educational purposes.

---

## 3. Environment
- Platform: TryHackMe lab environment (AttackBox / provided VMs)  
- Tools used: `tshark`, `tcpdump`, `arp`, `ping`, `traceroute`, `telnet`, `wireshark` (capture screenshots were taken in the room).

---

## 4. Summary of Tasks & Key Notes

### 4.1 DHCP — DORA
**What I learned:** DHCP automates IP configuration. The DHCP client/server exchange follows DORA:
- **D**iscover (client broadcasts a DHCPDISCOVER)  
- **O**ffer (server responds with DHCPOFFER)  
- **R**equest (client sends DHCPREQUEST to accept offer)  
- **A**cknowledge (server replies DHCPACK to confirm lease)

**Observed packet fields:**  
- Client initially uses `0.0.0.0` as source IP, destination `255.255.255.255` (broadcast).  
- Link-layer uses broadcast MAC `ff:ff:ff:ff:ff:ff` for discovery.

**Example capture notes:** client got IP `192.168.66.133` in the sample capture.

**Commands / captures used:**
```sh
# Capture DHCP packets
tshark -r DHCP-G5000.pcap -n
# Or live capture
sudo tcpdump -i eth0 port 67 or port 68 -w dhcp.pcap
```

---

### 4.2 ARP (Address Resolution Protocol)
**What I learned:** ARP maps IPv4 addresses (layer 3) to MAC addresses (layer 2). ARP Requests are broadcast; ARP Replies are unicast with the MAC of the requested IP.

**Observed examples:**  
- ARP Request destination MAC: `ff:ff:ff:ff:ff:ff`  
- Example MAC observed in the room: `44:df:65:d8:fe:6c` for `192.168.66.1` (example).

**Commands used:**
```sh
# Show ARP traffic using tcpdump
sudo tcpdump -n -vv -e arp
# Or filter a capture
tcpdump -r capture.pcap arp
```

---

### 4.3 ICMP (Ping, Traceroute)
**What I learned:**  
- `ping` uses ICMP Echo Request/Reply to test connectivity; typical payload in examples: `40` bytes.  
- `traceroute` (or `tracert` on Windows) discovers the routers between source and destination using TTL and ICMP/UDP probes.

**Commands used:**
```sh
# ping a host 4 times
ping -c 4 192.168.11.1
# run traceroute
traceroute example.com
# or on Windows
tracert example.com
```

**Observed:** The `traceroute` output showed intermediate hops and RTTs; `ping` displays RTT statistics (min/avg/max/mdev).

---

### 4.4 Routing (conceptual)
**What I learned:** Routers forward packets based on routing tables. Common routing protocols mentioned:
- **OSPF** — Open Shortest Path First (link-state)  
- **EIGRP** — Cisco proprietary (distance vector / advanced metrics)  
- **BGP** — Border Gateway Protocol (interdomain routing on the Internet)  
- **RIP** — Routing Information Protocol (distance vector, hop count metric)

Use-case: routers build tables to select the best path to reach a destination network.

---

### 4.5 NAT (Network Address Translation)
**What I learned:** NAT allows many private IPs to share a single public IP by translating internal IP:port pairs to external IP:port pairs. The router maintains a translation table mapping internal connections to external tuples.

**Example from room:** Internal machine `192.168.0.129:15401` could be translated to `212.3.4.5:19273` on the Internet-facing side.

---

### 4.6 Telnet (educational only)
**What I learned:** `telnet` is a simple TCP client that can connect to a TCP port and interact manually. It was used in the lab to connect to echo, daytime, and HTTP services on particular ports (7, 13, 80) for demonstration. **Note:** Telnet transmits data unencrypted—avoid using it for sensitive connections.

**Example usage:**
```sh
telnet 10.10.245.50 7     # echo server
telnet 10.10.245.50 13    # daytime
telnet 10.10.245.50 80    # HTTP -> then send `GET / HTTP/1.1` and `Host:` header
```

**Flag found in room (example):** `THM{TELNET_MASTER}` (as shown in the lab exercises).

---

## 5. Useful Commands Quick Reference
```sh
# DHCP / network discovery
sudo tcpdump -i any port 67 or port 68
sudo tshark -Y "bootp" -T fields -e bootp.option.type -e bootp.option.value

# ARP
arp -a
sudo tcpdump -n -e arp

# ICMP
ping -c 4 <target>
traceroute <target>

# Telnet (manual TCP interaction)
telnet <host> <port>

# General packet capture
sudo tcpdump -i eth0 -w capture.pcap
sudo tshark -r capture.pcap -V
```

---

## 6. Findings & Answers (from lab screenshots & exercises)
- **How many steps does DHCP use to provide network configuration?** 4 (DORA).  
- **Destination IP used when client sends DHCP Discover?** `255.255.255.255` (broadcast).  
- **In ARP request the destination MAC is:** `ff:ff:ff:ff:ff:ff`.  
- **Example MAC for 192.168.66.1 (from capture):** `44:df:65:d8:fe:6c`.  
- **Ping example bytes sent:** 40 (ICMP payload shown).  
- **Protocol that requires three-way handshake:** TCP.  
- **Telnet room HTTP server and flag example:** `lighttpd/1.4.63` and `THM{TELNET_MASTER}` (as observed in the lab).

> Replace or redact any flags if you plan to publish this repository publicly—flags are intended for use inside the lab only.

---

## 7. Recommendations & Next Steps
- Practice more packet analysis with `tshark`/Wireshark: follow the packet life from application payload → TCP/UDP → IP → Ethernet.  
- Repeat capturing a DHCP DORA exchange in a small lab network to inspect headers at each layer.  
- Explore `tcpdump` and `tshark` display filters to quickly locate relevant packets (e.g., `bootp`, `arp`, `icmp`, `tcp.port == 80`).  
- Learn basic router config commands for OSPF/BGP on vendor simulators (GNS3, EVE-NG) to solidify routing concepts.  
- When publishing notes on GitHub, remove lab flags and sensitive data before pushing public repos.

---

## 8. Appendix — Example Capture Commands
```sh
# Capture ARP requests and replies and write to file
sudo tcpdump -i eth0 -w arp_capture.pcap arp

# Filter DHCP messages from a capture using tshark
tshark -r capture.pcap -Y "bootp" -V

# Show ARP table on Linux
ip neighbour show
# or older
arp -n
```

---

**End of report**

*Generated from notes & screenshots taken during the TryHackMe "Networking Essentials" room.*
