# Toolbox reference

The tools a learner meets, grouped by what they are for. All are for use against
systems you own or are authorised to test. A tool does not grant permission; you
bring that.

## Operating systems

| Tool | For |
| --- | --- |
| Kali Linux | Security distribution with tools preinstalled |
| Parrot OS | Alternative security distribution, similar purpose |

## Reconnaissance and OSINT

| Tool | For |
| --- | --- |
| Maltego | Graphing relationships between people, domains, infrastructure |
| SpiderFoot | Automated OSINT collection and correlation |
| Shodan | Search engine for internet-exposed devices and services |
| theHarvester | Gathering emails, subdomains and names from public sources |
| Recon-ng | Framework for organising reconnaissance |
| Google dorking | Search operators (a technique, not a tool) |

## Scanning and enumeration

| Tool | For |
| --- | --- |
| Nmap | Host discovery, port scanning, service and version detection |
| Masscan | Very fast, large-scale port sweeping |
| Netdiscover | Local network host discovery |
| Nikto | Web server issue scanning |
| Gobuster / dirb | Discovering hidden directories and files |
| enum4linux | Enumerating Windows/Samba services |

## Network and traffic

| Tool | For |
| --- | --- |
| Wireshark | Capturing and analysing network traffic |
| tcpdump | Command-line packet capture |
| Ettercap / Bettercap | Man-in-the-middle framework (lab use) |
| Responder | Capturing local-network authentication traffic (lab use) |

## Wireless

| Tool | For |
| --- | --- |
| Aircrack-ng suite | Wi-Fi monitoring, capture and passphrase testing |
| Kismet | Wireless detection and monitoring |
| Wifite | Automating common wireless assessments |

## Web application

| Tool | For |
| --- | --- |
| Burp Suite | Intercepting proxy; the core manual web-testing tool |
| OWASP ZAP | Open-source intercepting proxy and scanner |
| SQLmap | Testing for and demonstrating SQL injection |
| wfuzz / ffuf | Fuzzing web inputs and discovering content |

## Exploitation and post-exploitation

| Tool | For |
| --- | --- |
| Metasploit Framework | Developing, testing and running exploit modules in a lab |
| Hashcat / John the Ripper | Password-hash cracking (testing your own hashes) |
| Hydra | Testing authentication strength against your own services |

## Utility

| Tool | For |
| --- | --- |
| Steganography tools | Hiding and detecting data inside images (a concept to understand both ways) |
| netcat | The "swiss army knife" for reading and writing network connections |
| CyberChef | Encoding, decoding and data transformation |

## A note on tool literacy

Knowing a tool's name is not knowing the tool. For each one that matters to you,
learn: what question it answers, what a normal run looks like, how to read its
output, and how to explain its finding to someone who has to fix it. A tester who
understands ten tools deeply is worth more than one who has run forty once.
