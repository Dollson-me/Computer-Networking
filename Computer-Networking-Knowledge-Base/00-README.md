# Computer Networking — kompletna baza wiedzy z dostarczonych PDF-ów

> **Zakres:** 5 PDF-ów, łącznie 1044 strony: podręcznik (214), prezentacja kursowa (525), laboratoria z rozwiązaniami (266), notatki Padriseup/Riseup (30) oraz projekt Cisco (9).
>
> **Założenie:** niczego nie skracamy. Ten plik `00-README.md` jest tylko mapą nawigacyjną. Pełna treść — strona po stronie, wszystkie ćwiczenia, odpowiedzi, polecenia, linki, uwagi i ciekawostki — znajduje się w pozostałych plikach oraz w `COMPLETE-NOTES.md`.
>
> **Uwaga techniczna:** trzy duże PDF-y są obrazami stron bez warstwy tekstowej. Zostały odczytane strona po stronie; przy nietypowych fontach i zrzutach terminala mogą pozostać pojedyncze artefakty OCR. Każdy fragment ma numer strony źródłowej, więc komendy i adresy można łatwo zweryfikować z oryginałem.

## Pliki w repozytorium

- `00-README.md` — mapa materiału, indeks tematów i laboratoriów.
- `01-Theory-Textbook.md` — pełny podręcznik, 214 stron, uporządkowany według 12 rozdziałów.
- `02-Course-Slides.md` — pełna prezentacja, 525 slajdów, zachowana strona po stronie.
- `03-Labs-and-Solutions.md` — wszystkie laboratoria i rozwiązania, 266 stron, pogrupowane według kodów NET-xx-LSx.
- `04-Padriseup-Notes.md` — komplet 30 stron notatek prowadzącego/Riseup, łącznie z logistyką, komentarzami, komendami, pracą domową i odnośnikami.
- `05-Cisco-Project.md` — projekt Cisco: subnetting, VLAN-y, trunking, routing, router-on-a-stick, port-security, OSPF, ACL, konta/hasła i SSH.
- `06-Links-and-Resources.md` — biblioteka wszystkich wykrytych linków z numerami stron źródłowych.
- `07-Command-Reference.md` — indeks poleceń Windows/Linux/Cisco IOS/Wireshark i konfiguracji z materiałów.
- `08-Technology-Protocol-Index.md` — indeks technologii, protokołów, narzędzi i zagadnień z odsyłaczami do stron.
- `COMPLETE-NOTES.md` — jeden monolityczny plik zawierający całość powyższych materiałów.

## Pełna mapa programu

### 1. Introduction to Networks
- potrzeba komunikacji i sieci komputerowych;
- typy sieci: LAN, WAN, MAN, SAN oraz kontekst sieci domowych, firmowych, centrów danych i Internetu;
- ARPANET i rozwój sieci;
- urządzenia końcowe, media, urządzenia pośrednie;
- NIC / Network Adapter / LAN Adapter / Physical Network Interface;
- hub, switch warstwy 2, switch warstwy 3, router, access point, firewall, WLC, home router;
- broadcast domain i collision domain;
- half-duplex i full-duplex, duplex mismatch;
- Ethernet, RJ-45, skrętka, światłowód, fale radiowe;
- CAT-5, CAT-5e, CAT-6, CAT-6a, CAT-7;
- UTP i STP, RFI i EMI;
- straight-through, crossover, rollover;
- topologie point-to-point, star, mesh, hybrid;
- architektura 3-tier: core, distribution, access;
- collapsed architecture;
- adres MAC, OUI/identyfikator producenta, część urządzenia;
- IPv4, IPv6, maski podsieci, klasy adresowe;
- podstawowe protokoły: IP, DNS, DHCP, HTTP, HTTPS;
- polecenia Windows: `ping`, `ipconfig`, `nslookup`, `tracert`, `netsh`;
- sieci bezprzewodowe: AP, wireless NIC, Wi‑Fi/IEEE 802.11, WiMAX, Bluetooth/WPAN;
- problemy radiowe: zasięg, zakłócenia, bezpieczeństwo, współdzielone medium;
- standardy 802.11a/b/g/n/ac/ax oraz porównanie copper/fiber/Wi‑Fi.

### 2. Network Fundamentals
- model client-server;
- HTTP/HTTPS, DNS, FTP, DHCP, SMTP, SSH, ICMP;
- modele OSI i TCP/IP, zależności i mapowanie warstw;
- 7 warstw OSI i 4-warstwowy TCP/IP;
- enkapsulacja/dekapsulacja, headers, trailers, PDU, segment, packet, frame, MTU, FCS;
- TCP i UDP, niezawodność, kolejność, checksum;
- flagi TCP: SYN, ACK, RST, FIN, PSH, URG;
- 3-way handshake i zamykanie sesji TCP;
- porty logiczne, well-known / registered / dynamic-private;
- porty m.in. HTTP, HTTPS, DNS, DHCP, SMTP, POP3, SSH, RDP, SMB, FTP, TFTP, NTP;
- `netstat -ab`;
- Wireshark: interfejs, Packet List, Packet Details, Packet Bytes, przechwytywanie, zapis `.pcap/.pcapng`, filtry, Follow Stream;
- analiza ICMP, DNS i HTTP;
- ARP: request/reply, broadcast, cache, `arp -a`, `arp -d`, wpis statyczny;
- proces enkapsulacji w każdej warstwie.

### 3. Switch & IOS Fundamentals
- działanie switcha i tablica MAC;
- switching methods: store-and-forward, cut-through, fragment-free;
- prędkość portów, duplex, auto-negotiation;
- Cisco IOS i terminal/CLI;
- Cisco Packet Tracer;
- out-of-band access i kabel console;
- tryby IOS: User EXEC, Privileged EXEC, Global Configuration, Interface/Line Configuration;
- pomoc `?`, autouzupełnianie, skróty klawiaturowe;
- POST, pamięć flash, startup-config/running-config;
- `hostname`, `username`, `enable password`, `banner motd`, `service password-encryption`;
- `show running-config`, `copy running-config startup-config`;
- console login local;
- TFTP i kopie konfiguracji/IOS;
- ROMmon i configuration register.

### 4. Switch Security
- zagrożenia w środowisku przełączanym;
- port-security: manual/sticky MAC learning, maximum, violation modes shutdown/restrict/protect;
- wymagania port-security i weryfikacja;
- remote access: Telnet vs SSH;
- szyfrowanie, klucze asymetryczne;
- VTY;
- SVI / Switched Virtual Interface;
- SSH: hostname, local user, domain-name, RSA, SSH v2, `login local`, `transport input ssh`, `show ip ssh`, `show ssh`.

### 5. IP & Routing Concepts
- system dziesiętny, binarny i szesnastkowy;
- notacja pozycyjna i konwersje;
- router, default gateway, interfejsy Ethernet/Serial/Loopback;
- routing table i proces wyboru trasy;
- directly connected/local routes;
- IPv4: adres, maska, classful addressing, unicast/broadcast/multicast, link-local, loopback, public/private;
- IPv6: budowa, skracanie, global unicast/link-local/multicast, dual stack, `ipv6 unicast-routing`.

### 6. Subnetting Concepts
- problem domen rozgłoszeniowych;
- subnetting i granice oktetów;
- CIDR i prefix length;
- classless inter-domain routing;
- obliczanie network/host/broadcast;
- case studies subnetting;
- VLSM;
- projektowanie schematu adresacji i planowanie sieci.

### 7. IPv4 & IPv6 Static Routing
- praca routera z sieciami zdalnymi;
- zastosowania, zalety i wady routingu statycznego;
- standard static route, default route, floating static route, summary route;
- administrative distance;
- `ip route` i `ipv6 route`;
- sumaryzacja adresów;
- weryfikacja tablic routingu IPv4/IPv6.

### 8. Dynamic Routing
- routing dynamiczny, routing source codes, metryki, administrative distance;
- IGP vs EGP;
- distance-vector vs link-state;
- passive-interface;
- classful/classless routing;
- RIP/RIPv2/RIPng, parametry, auto-summary, `router rip`, `version 2`, `no auto-summary`, `network`, `show ip protocols`;
- default-information originate;
- OSPFv2: link-state database, adjacency, LSU, SPF, cost/metric, wildcard masks, router-id, areas, single-area OSPF;
- `router ospf`, `network ... area`, `auto-cost reference-bandwidth`, `show ip route ospf`, `show ip ospf interface`, `show ip ospf neighbor`.

### 9. VLANs & Trunk
- VLAN i korzyści segmentacji;
- default/data/voice/management/native VLAN;
- `show vlan brief`;
- access port i przypisanie VLAN;
- trunking i IEEE 802.1Q;
- Dynamic Trunking Protocol, DTP modes, `switchport nonegotiate`;
- native VLAN i zasady konfiguracji;
- inter-VLAN routing;
- router-on-a-stick;
- subinterfaces i `encapsulation dot1Q`.

### 10. Diagnostics & Troubleshooting
- metodyka troubleshooting;
- zbieranie informacji i podejście według warstw OSI;
- narzędzia software/CLI;
- `show ip interface brief`, `show running-config`, `show startup-config`;
- extended ping/traceroute;
- Cisco Discovery Protocol (CDP), reklamy i neighbor information;
- LLDP;
- bezpieczeństwo protokołów odkrywania;
- logi urządzeń i Syslog;
- severity/facility;
- `logging host`, `logging trap`;
- Network Time Protocol, zegar lokalny, NTP master/client, `clock set`, `show clock`.

### 11. Access Control Lists
- ACL jako filtrowanie ruchu;
- stateless vs stateful;
- standard vs extended ACL;
- kierunek `in` / `out`;
- wildcard masks;
- kolejność reguł i implicit deny;
- placement standard/extended ACL;
- numbered vs named ACL;
- `access-list`, `ip access-list standard`, `ip access-list extended`, `ip access-group`;
- filtrowanie hostów, sieci, protokołów i portów (np. HTTP/80).

### 12. Infrastructure Services
- DHCP: po co, charakterystyka, dynamic/automatic/reservation allocation;
- proces DHCP i odnowienie lease;
- serwer DHCP vs router;
- DHCPv6 i SLAAC;
- DHCP pools, excluded addresses, relay (`ip helper-address`) i klient DHCP;
- NAT: cel, private IP space, translacja inside/outside local/global;
- static NAT, dynamic NAT, PAT/overload oraz NAT64;
- konfiguracja `ip nat inside`, `ip nat outside`, static mappings i pools.

## Laboratoria — pełna lista
- **NET-01-LS1 — Local Network Configuration** (strony 1–14 pliku z zadaniami i rozwiązaniami)
- **NET-02-LS1 — Network Examination with Wireshark** (strony 15–33 pliku z zadaniami i rozwiązaniami)
- **NET-03-LS1 — Packet Tracer Installation** (strony 34–46 pliku z zadaniami i rozwiązaniami)
- **NET-03-LS2 — Initial Cisco Device Configuration** (strony 47–70 pliku z zadaniami i rozwiązaniami)
- **NET-03-LS3 — Backing Up Config Files and Managing the IOS** (strony 71–85 pliku z zadaniami i rozwiązaniami)
- **NET-04-LS1 — Configure and Verify Port Security** (strony 86–110 pliku z zadaniami i rozwiązaniami)
- **NET-04-LS2 — Remote Access with SSH** (strony 111–123 pliku z zadaniami i rozwiązaniami)
- **NET-05-LS1 — Converting Decimal, Binary, and Hex** (strony 124–130 pliku z zadaniami i rozwiązaniami)
- **NET-05-LS2 — IPv4 and Initial Router Configuration** (strony 131–147 pliku z zadaniami i rozwiązaniami)
- **NET-05-LS3 — Configure IPv6 Addressing** (strony 148–160 pliku z zadaniami i rozwiązaniami)
- **NET-06-LS1 — Subnetting Practice** (strony 161–168 pliku z zadaniami i rozwiązaniami)
- **NET-07-LS1 — Configuring IPv4 Static and Default Routes** (strony 169–186 pliku z zadaniami i rozwiązaniami)
- **NET-08-LS1 — Configuring and Verifying RIPv2** (strony 187–202 pliku z zadaniami i rozwiązaniami)
- **NET-08-LS2 — Configuring & Verifying OSPFv2** (strony 203–210 pliku z zadaniami i rozwiązaniami)
- **NET-09-LS1 — Configuring VLANs, Trunks, and More** (strony 211–231 pliku z zadaniami i rozwiązaniami)
- **NET-10-LS1 — Configure NTP and Syslog** (strony 232–245 pliku z zadaniami i rozwiązaniami)
- **NET-11-LS1 — Implement Standard and Extended ACLs** (strony 246–266 pliku z zadaniami i rozwiązaniami)


## Projekt Cisco — zakres
- podział `172.16.10.0/24` na 8 podsieci `/27`;
- VLAN 10 Management, VLAN 20 Marketing, VLAN 30 Accounting, VLAN 100 Native;
- porty access i trunk, native VLAN i wyłączenie negocjacji DTP;
- adresacja routerów i hostów;
- router-on-a-stick;
- port-security i sticky MAC;
- wyłączanie nieużywanych portów;
- OSPF;
- ACL blokujący konkretny host-to-host;
- użytkownik lokalny, hasło enable, szyfrowanie haseł i MOTD;
- SSH v2, RSA 1024, VTY 0–4, `login local`, `transport input ssh`.
