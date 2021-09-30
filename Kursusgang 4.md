[[_Softwaresikkerhed]]

# Web Application Hacking Intro

**Todays reading**: AoST chapters 6,7,8,9 - ca 72 pages.

[Getting Started with Portswigger](https://portswigger.net/burp/documentation/desktop/getting-started)

## Lecture notes

**Hacker tools**
- Nikto
- Whatweb
- Burp lokal webproxy
- Zed Attack Proxy (gratis Burp-lignende værktøj)

**Informationsindsamling (recon)**
*passiv indsamling* kunne være at lytte med på trafik eller søge i databaser på Internet: google, whois, archive.org m.fl. (hvor man *ikke* kontakter målet)

*aktiv indsamling* er eksempelvis at sende ICMP pakker og registrere hvad man får af svar, portscan m.v. (hvor man *aktivt* kontakter målet)

**Godt råd: brug HSTS**

**Nmap** (brug zenmap til at lære nmap)
- Brug Nmap scripting
- Brug evt. også nping

**Generic Network Fault Injection** (fra bogen)
- loooong input - *buffer overflows*
- *SQL injection* - database commands
- *Cross-site scripting* (*bør læses op*)
- Random bytes - recommend using real *fuzzers that understand target protocol
- Metacharacters like null bytes


#KEA/Softwaresikkerhed 