# COMPLETE NOTES — Computer Networking

> Monolityczna wersja całego repozytorium. Poszczególne pliki są wygodniejsze do przeglądania na GitHubie.


---

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


---

# 01 — Computer Networking Textbook — pełna treść

Źródło: `Computer Networking Textbook.pdf` (214 stron). Treść zachowana strona po stronie; podział rozdziałów zgodny ze spisem treści.

## Materiały wstępne — strony 1–4

### Textbook — strona 1

Cybersecurity Professional Program
Computer Networking
Textbook
Ka
Copyright © 1996-2020 HackerU Ltd.
All Rights Reserved.


### Textbook — strona 2

Table of Contents

SECTION 1: NETWORK TYPES AND DEVICES....sesssessssesssssesssecssseessssessvsessssessesessessssesssseessseesssesssesessestsssetssesssesesses D
SECTION 2: NETWORK MEDIA AND CABLES «..sesssessssessssecssseesssecssesessesessseessesessesssseessseessseenssesssestssestesstsseessvaees LD
SECTION 3: NETWORK TOPOLOGIES AND ARCHITECTURE ..-+sssesssecsssesssssessseesssssssesssseesssectsseesseeessentssestssveesseesssenes LA
SECTION 4: NETWORK PROTOCOLS AND COMMANDS ...sssessssesssesssssesssesssseesssecssesessssessecssseessseessestssestssvsesseessseses 20
SECTION 5: WIRELESS: TECHNOLOGIES sists sistsscvsesstvesniesnitvninscivsicnnereenisiniivncrsiiersnnisiienirenctaaniiniintie 2D
SECTION 1: NETWORK PROTOCOLS AND MODELS wssissssvsssssvvssvscivsscssesessssssscsctsusetsivssvustivenseonstacartaveneincieinatsiees 2D
SECTION22.OS| MODEl :ssissisessceessssisetsisnittssessenncennestienciinenninwintenieseiscsninaieenenmeereie BD
SECTION SE TCP/IP MODE bascssssveoscrresrervcocevssucersarrssaeun rene NESW I SEIN WE NS RO
SECTION 4: TRANSPORT PROTOCOLS AND LOGICAL PORTS....ssesssessssssssseessseessessssessssessssecssseesseesssestssestsssesseessseess 3B
SECTION 5: INTRODUCTION TO WIRESHARK ...sesssessssesessscessecsssecsssesssssessssensvecssessssessasestsseesssesssentssestesssesseessveess 46
SECTION 6: ARP AND ENCAPSULATION. .ssecsssesssesessessssscesssesssecssseesssstssseessessssesssseessseetsseessvessseatssestssssesseessesss 9
CHAPTER 3: SWITCH AND IOS FUNDAMENTAL ...........:cssssssesssesseestsesnsseeseeeseseseeeseessO2
SECTION 1: SWITCH FUNDAMENTALS ...esssecsssecssesessesessscsssscsssecsseseesssessvecssvscssecssseessssetssensvecssesessestsssstsseesssenss O2
SECTION 2: THE CISCO IOS ...ssessssesssseesssecsssecssesessesssssctsseesssecssuetssesessssessesessesssseesasectsseesseeesseatssestssssessesessesss OO
SECTION 3: INITIAL DEVICE CONFIGURATION COMMANDS ...ssesssscssssssssssssveessseessesessessssscssseessveessesessestssesesseeessenes 72,
SECTION 4: ADDITIONAL IOS PROTOCOLS AND COMMANDS ....sssessssssssesssssessseessesessessssecssseessvecssesessestssvsessesssseses 70
SECTION 5: VERIFYING CONFIGURED REGISTER VALUE ....sessssessseesssessssesssseessscessesessessssectsssessesesseatssestssveesseeesseees BO
SECTION 1: PORT SECURITY sisiissetasscseenrs srr ninieescivirni niin nininnunnmaiamnanen OL
SECTION 2: REMOTE ACCESS swsssseasnesnnannannniennciarantmnena OO
SECTION 3! VV Viceesosecsescesmsecerecscccneoer seen coce re ese tectres cue one rere vccurae ee rectnee tn eore rer vcore rece eernace ee BB
SECTION 4: SVI (SWITCHED VIRTUAL INTERFACE) ..-ssessssecsssecsssecsssesssssessssensesessessssesesseetsseenseesssenessestssssessessssesss OB
SECTION 5: SSH CONFIGURATION ..sssssssssecsssecssesessesessecssssesssecssuseesustesveessvscssesssscessetsseessvesssestssestssesesseesssesss OO
SECTION 1: NUMBER SYSTEMS....ssesssssssssecsssesssesessesessscssssesssecssusssssstesseessessssessssecssseessseessusessenesseatssssessesssseses OD
SECTION 2::THEI ROUTER civscsssscsvaessiseutssostessssssiensusnntestntsnunasestsestaesitvucstvenvbisentesstiseitesnitesienaundetnreenteernsien OB:
SECTION 3::ROUTING PROCESS ssvssssncseisissisescvsesctvesnievnivvcinsiisiccvereensssiacvictsisecsavsivestieenicenesaanaentwvcient LOD
SECTION 42 IPV4 sesssvsceesceesveversseceventncarenraceesevenuenueniarinrcraeenn een LOS
SECTION 52 1PWG esses ccomsaepeesapessceuseseueree urn eommeaeseen meee ea cere aen eee eer urn eee eeeeeyecey LOO


### Textbook — strona 3

SECTION LE SUBNETTING wcessstsccsccscisesasnitsaccesteninnctiscicciinatnitiacecteninniisioniiintatectenenciecctiae LAS
SECTION 22 CIDR sssecsererssenernesee en neveree veneers meen evar earners eens une nneereen! 1ES

BS {ey To) SE 5.1 Bs) | Brerenrerereerernr rereererererrer ec rerrer rere errr oer crnrrerverrcrerrcreTerrereererirerrn rererermererrrerrererrerrrrrrral C40)
SECTION 4: NETWORK ADDRESS SCHEME DESIGN.....cssessessessessessesssssesessesessesseessessssesssesssnsssssssssessessssssssessees LOZ
CHAPTER 7: IPV4 & IPV6 STATIC ROUTING. ...........ccssscssssssssesssssssssseessseesesesseseeseseseee L2G
SECTION 1: ROUTER OPERATION ....sssessesseseseessesseseesessesseessssesseessssssssssssssesseessesnssesseesssesssssussessessecsssstesessees LOA
SECTION 2: IPV4 STATIC ROUTING ....sssessesssseessssseseesessesseessssesssesssnssssssssssessresessssseassesssnssssssssessessrssssssssessees LOZ
SECTION 3: IPV6 STATIC ROUTING ....sssessesssseessesseseeseeseessessssesstesssssssssssssesseessesnesesseenssessessatsessessessresessessees LSA
SECTION 1: DYNAMIC ROUTING CONCEPTS.....csscessesesseeseessesessesseeessssesiesessesseessesnssesseensessitsisessessssessesees LO
SECTION:2 | RIPV2 3 swccnsnasrvecavsussausarsectesnumscesnactyncevraswitinenventarannerasvaitiearsbacestntveareeenemsararennnuserearnenerell 4D
SECTIONS! OSPEV2 swscsconennanrsvevionisoriinnnmnersrnarr mnemonic nee een IAD
SECTION 1: VIRTUAL LANS wisscvscvsciewsivscie nics nneenicinicnrcsniincivsain tina LOB
SECTION 22 TRONKING iecsccesvssisccsccscaeisacnitsaccesteninnctisciccniiacnitia ce cteninnctisiccniatitia tetanic LOS
SECTION 32 INTER-VLAN ROUTING iescissstsinsosnenatinrninncnnianitin nanny 168
CHAPTER 10: DIAGNOSTICS AND TROUBLESHOOTING .............sssssseeeesssereeensssseeereee LOL
SECTION 1: TROUBLESHOOTING METHODS.....scscsssssssssssesssssessessssssssesessssssssssssssstssesstsssssessssssessssessssisseseees LOL
SECTION'2° CDP: & UDP: cnessscenrenarnecnen mannan Een 174:
SECTION 3: SYSLOG — LOG EVENTS ...ssssessesesseessessesessesseeseessssesssesssnssssssssessesseessessssesssesssnsssssssessessesssessssessees LZO
SECTION 4: NETWORK TIME PROTOCOL (NTP) .....-ssssceseececeseeeessseeeeaeseeecseeetaeeesssetetseetsstetetetetateetttetetteeeeeee LBD
SECTION 1: ACL OVERVIEW .ossessessessessessessssessesseseesesssessessssesstesssssssssssssesseessesnesesseenssessessessessessssesessessees LBS.
SECTION 2: STANDARD ACL IMPLEMENTATION js. .cssscestecvessessevsisessiessiscstensustuctostsstevaitestiessisssteceustecronrsecevssesess LOD
SECTION 3: EXTENDED ACL IMPLEMENTATION sccsssstosctscvsscsnsivsciesitsrnsesntattvanecionntivssieniternieenciteanieeneacivsei nie LOS
CHAPTER 12: INFRASTRUCTURE SERVICEG............ssssssesssssseeseeeseseeeeeeesssseeeeeessssseeesees 200
SECTION 1: DHCP OVERVIEW wecvsciswsivsciesicsisncenisinicnecvsnieneinnieiesnneenicineann niece tients DOK
SECTION2 DHEP IMPLEMENTATION sieisevsssssscesctennisciscsciniiasnitsacectennneisccnmianntiate tennessee 205
SECTION 3° NAT OVERVIEW ssitscsstesncsssntsnenienatinrnnncnreniania aan 208
SECTION 4: NAT IMPLEMENTATION .....ssssesssseessesseseeseesesseessssesseesssssssesesssesssessessssesstesssessssessessessesseeseeseseees QLD


### Textbook — strona 4

| About this Textbook
This textbook is designed to help students study and review the material covered
throughout the Computer Networking course. It contains information relevant to the
lessons covered in class, as well as references to lab activities that should be practiced
to boost your knowledge level.
Material covered in this textbook includes the basics of network structures, topologies,
and network devices.
The focus of the material is on networking concepts, methods, and tools.
Legend
Colored text blocks may appear throughout the textbook, to redirect the reader to a
specific source or enrich them with additional information.
The text blocks include:
Lab Assignment
— This is a good time to review the relevant lab files (according to the lab
mm =| code) and practice what was taught so far.
® | Good to Know
Additional information or insight regarding a topic. This is for enrichment
purposes only and is not part of the exam materials.
ve Tip
° © * | Useful information that may help students study the material or work with
= specific tools.
@ More Information
) 1g Links or references to external material that can be used to expand one’s
knowledge on a subject.


# Chapter 1: Introduction to Networks


### Textbook — strona 5

| Chapter 1: Introduction to Networks
Section 1: Network Types and Devices
Communication is an essential characteristic of any society.
In today’s world, people communicate with other people around the world almost as
simply as they talk to a person standing right beside them.
Over the past several decades, global communication has advanced significantly and
has greatly improved the human social experience.
A network is basically two or more computers that communicate with each other and
share information.
Communication over a network (networking) brings people together for either generic
or specific purposes.
Network Types
LAN - A Local Area Network defines a small geographical area in which multiple
computers and other devices are connected. LANs can be set up in homes and small
businesses and can be managed individually or centrally.
LANs can be designed to use one of two communication methods: Wired or Wireless.
WAN - A Wide Area Network is spread across an unlimited geographical area and
connects between multiple LANs. WANs are usually managed by several service
providers.
MAN - A Metropolitan Area Network is larger than a LAN but smaller than a WAN. In
most cases, it is managed by a city municipality and enables connection to broader
networks.
SAN - A Storage Area Network is a dedicated network that supports file servers and
provides efficient transfer of unusually large data sizes at extremely high rates.
SAN networks are usually found in large companies and data centers


### Textbook — strona 6

Network Structure
The history of computer networks began in the 1960s with a network called ARPANET.
Communication among devices can be as simple as connecting a cable between two
computers. On the other hand, it can be as complex as a large assembly of multiple
networks spread around the world and regulated by an assortment of sophisticated
devices and protocols.
Devices in a Network
Endpoint Devices - Devices that connect to a network for communication purposes,
such as computers, phones, and others. All endpoint devices have unique addresses
that identify them on the network.
Media - ‘Media’, based on the word ‘medium’ (meaning ‘in between’) is a means of
transferring data, such as metallic wire, glass or plastic fiber, wireless radio frequencies,
and others.
Intermediary Devices - Devices that transfer messages over the network and facilitate
communication between end devices.
Endpoint Devices
In today’s world, most people communicate with each other through networks.
Endpoint devices are the source or destination devices in a networked system.
Computers, laptops, and phones are endpoint devices that allow us to communicate
over a network.
Endpoint devices must have the ability to connect to a network via a NIC (Network
Interface Controller), to be able to send and receive information.


### Textbook — strona 7

Network Interface Controller (NIC)
To allow an endpoint device to send and receive information over a network it must
have the appropriate hardware.
A Network Interface Controller (NIC) allows endpoint devices to interact with other
devices over a network.
Other names for NIC include:

* Network Adapter

* LAN Adapter

* Physical Network Interface
Network Devices
Network devices act as bridges, interconnecting endpoint devices.
Smart network devices know how to differentiate between devices, and can send data
to specific destinations.
Unlike smart devices, simple network devices send information indiscriminately across a
network.
Switches
For multiple endpoint devices to communicate with each other, a mechanism needs to
be set up to handle the transfers.
A switch is a network device with physical ports to which endpoint devices can be
connected via Ethernet cables to create a network.
Switches use MAC addresses to pass information from one device to another.


### Textbook — strona 8

Switch Types
Hub - Hubs were used to relay data to multiple devices in a LAN. They broadcast data to
all connected devices, as opposed to a switch which sends information to dedicated
destinations.
Layer 2 Switch - This is the most common and basic switch in use. It uses MAC
addresses to forward information to specific destinations within the network.
Layer 3 Switch - A layer 3 switch performs the same operations as a layer 2 switch, but
can also function as a router if it is configured to do so.
Switch Vs. Hub
=
Message
tok es. —_\
—+
Switch
LJ)
—a_\
Message
toA
—+ [z0000] —
Lo
Hub —S_\
Broadcast & Collision Domains
A Broadcast domain is a type of communication whereby the sender sends a single
copy of the data to all devices on the same network segment. Broadcast
communication must be used since protocols such as ARP and DHCP rely on it.
A broadcast domain includes devices that receive broadcast packets originating from
senders within the same network segment.
Routers operate in the network layer and separate both collision domains and
broadcast domains.


### Textbook — strona 9

A Collision domain is a group of nodes that can ‘hear’ each other. Ideally, when one
node talks, all the others only listen. When two nodes talk at the same time, a collision
occurs. To resolve this issue, a switch creates collision domains.
A switch, which operates in Layer 2 of the OSI model, can create separate conversations
between nodes, which, in turn, creates separate collision domains.
Although collisions are expected to occur in a half-duplex Ethernet network, if a
collision domain becomes too big, traffic problems will arise, due to re-transmissions.
Duplex Modes
Duplex is a form of point-to-point communication between two or more parties. This
type of communication allows both ends to communicate in both directions. There are
two types of duplex modes: HDX (Half Duplex) and FDX (Full Duplex).
Half Duplex allows unidirectional traffic flow for peer-to-peer communicating parties.
Only one party can send or receive data at any moment. For example, a walkie-talkie is
performed in half duplex.
Full Duplex allows bidirectional traffic flow for peer-to-peer communicating parties.
Both parties can send and receive data at the same time. For example, a phone call is
performed in full duplex.
Note that when two peer-to-peer devices are set to different duplex modes, a duplex
mismatch occurs. This situation will reduce the quality of the communication.

f f}

fm fio

=)! ———————“—{(Y- SI

Sy Si

lf) ()

3888 SF ESS


### Textbook — strona 10

Routers
While switches allow devices to interact in the same network, routers allow them to
communicate with different networks.
A router connects networks and allows communication between endpoint devices in
different networks.
Routers use IP addresses to route information among networks.
Additional Devices
Access Point (AP) - Access points allow endpoint devices to connect to a network
wirelessly and manage information transmission.
A wireless device user can access a wired network via a properly configured access
point.
Firewall - Firewalls are security tools that are effective against threats that originate
from outside a network. They work with filters that allow the blockage or transfer of
information in a given direction.
WLC - A Wireless LAN Controller allows the configuration of multiple APs to be
managed from a central device. This is useful in large organizations where multiple APs
are deployed in different sections of a building.
Home Router - The router that many people have at home includes all the features
covered in this lesson so far. It acts as an AP, a switch, a router, and a firewall with the
most basic configuration.


### Textbook — strona 11

Section 2: Network Media and Cables
Information cannot be transmitted over a network without a means of transportation.
The term ‘media’ refers to the physical cables or wireless technologies used to pass the
information from one device to another.
Different types of media feature varying speeds and distances of data transfer.
Connections between continents were made possible using submarine cables that were
stretched across thousands of kilometers through the oceans.
Ethernet Cable
The most common way to connect to a network is via an Ethernet cable with an RJ-45
connector.
Cables are made of copper and can transmit information in the form of electrical
signals.
Signals deteriorate as the distance grows, and due to the influence of RFI and EMI,
which limits the cable length.


### Textbook — strona 12

Ethernet Cable Types
Over the years, network speed has increased and cable standards were modified
accordingly.

CABLE SPECIFICATIONS

CAT-5 Maximum length of 100m, maximum speed of 100 Mb/s

CAT-5e Maximum length of 100m, maximum speed of 1 Gb/s

care Maximum length of 100m, maximum speed of 1 Gb/s

(Note: Supports 10 Gb/s for 55m)
CAT-6a Maximum length of 100m, maximum speed of 10 Gb/s
CAT Maximum length of 100m, maximum speed of 10 Gb/s
(Note: Supports 100 Gb/s for 50m)
hm
CATS5e Cable with an RJ45 Connector at the end
Ethernet STP and UTP
UTP - Unshielded Twisted-Pair is the most common copper cable in use. It consists of
four twisted pairs of colored wires. The act of twisting the wires is done to prevent
signal disruption (cross-talk).
STP - Shielded Twisted-Pair cables are similar to UTP, but have additional protection
against EMI and RFI interferences. Each twisted pair is wrapped in foil.
EMI and RFI are electromagnetic and radio frequency interferences that can affect
signals.


### Textbook — strona 13

Ethernet Cable Configurations
Straight Through - Wires are placed in a straight formation from side A to side B. This
form is used for cables that are meant to connect network devices of different types,
such as a switch and an endpoint.
Crossover - Wires crisscross from side A to side B. This form is used in cables that are
meant to connect similar network devices.
Rollover - Flat cable in which the pinouts on one end are reversed at the other end.

Straight Vs. Crossover

|

————————

{See ee ee ete

§

ee

hs

[oewiwers eee eT

3 $$,

pe oan a

2 So OSS em ee 2

a Same 5

4 4

Siren oe ae 5

6 ee 6

Leaner nea 7

8 |
Fiber Media
Ethernet cables have a length limit of 100m. A different type of cable is used for greater
distances.
Fiber optic cables transmit information using light, at high speed, over long distances.
These cables are not sensitive to RFI and EMI, but aren’t as physically flexible as
Ethernet cables, and are more expensive.

Fiber Optic Cable


### Textbook — strona 14

Section 3: Network Topologies and Architecture
A network topology describes the structure of a network.
It represents all the connections between all components in a network.
Several types of topologies can be used to construct networks.
Note: A topology represents the resources of a network, but not locations and
distances.
Topology Types
Point-to-Point
A connection between two computers that share a client-server relationship.
If the connection fails, the communication is disrupted.
Star
In a star topology, all endpoint devices are connected to a central intermediate device.
This type of topology is easy to set up and maintain. It is also highly scalable.
vos


### Textbook — strona 15

Mesh
In a mesh topology, each end device can have multiple connections to other end
devices.
This configuration is highly resilient, due to its allowance of multiple connections, but it
is also expensive and very difficult to maintain.
Hybrid
A hybrid topology is a combination of other topologies.
Although a hybrid configuration takes advantage of the strong points of other
topologies, it also has to deal with the disadvantages of those topologies as well.
Architecture Types
3-Tier Architecture
The concept of a 3-Tier Architecture can be applied to any type of network.
Each layer has its own features and functionalities, which reduces network complexity.
The model helps design, implement, and maintain a scalable, reliable, and cost-effective
network.
Its simplistic structure makes it very easy to manage.
The combination of these attributes means that it is the best choice for large
enterprises, in which thousands of computers need to be interconnected, sometimes
over an area that includes several buildings.


### Textbook — strona 16

A 3-Tier architecture consists of three layers that provide isolation between devices,
greater flexibility, more security options, and resilience.
The separate layers include:
Core — routing layer connecting to servers and the Internet.
Distribution — separation between core and access layers, and boundary control.
Access — communication between endpoint devices.
The layers can be managed independently without affecting other layers.
Core
E0000)
[s0009] ae Se ae [fs0005] Layer

a aac

1 ee aa 1

' yon. H

1 as - ee i 1

> “Sap

Distribution
E00Co] i. =000G] Layer
De e__pa
2 y . aeet se , oS
wee gee
Pol ri ze ¥ ca <= are
a e* Se’ ek Se
Access Layer
3-Tier Network Architecture
Collapsed Architecture
This architecture is similar to 3-Tier, but has a different number of layers and a different
scalability potential.
In this architecture, the core and distribution layers are collapsed together to form a
single layer.


### Textbook — strona 17

This means it has the advantages of the 3-Tier architecture, but for a smaller network
scale.
Core +
=0U00g] a le Lhe [e0009| Distribution
Layer
i thine )
DP eee ae,
ee, h % x Pi , 4 Re
ae ! a y \ a
* f Ps ~y¥ \ ats
' as ¢ ‘ =
i = = feed s
Access Layer
Collapsed Network Architecture
Physical and Logical Addresses
Back when the first networks were created for local computers to communicate with
each other and share data, design engineers realized they needed to know how
computers would talk to each other and who they could talk to.
The idea was for each computer to have a unique name or identification, and the
concept of a MAC address was born.
A MAC address is the unique identity of a computer within a network, while IP
addresses are used to identify machines operating in different networks.
Each network card has a set MAC address and only one IP address at any given
moment.
MAC Address
A MAC address is a unique hardware identifier attached to each network card. The
address is static and should not be changed.
It consists of six hexadecimal nodes with two hexadecimal numbers ranging from 00 to
FF.


### Textbook — strona 18

A MAC address includes two parts:
e The first three nodes represent the manufacturer’s identifier.
e The last three nodes represent a serial identifier.
. . . . .
00:0d:83:b1:c0:8e
Manufacturer Serial Identifier
Identifier
IP Address
An IP (Internet Protocol) address is used to uniquely identify computers on the network
and create network partitions.
IPv4 - IPv4 addresses are commonly used today. They consist of four octets of numbers
between 0-255, separated by dots. This structure can generate approximately four
billion different addresses.
Some addresses, such as 192.168.X.X, are dedicated to specific uses.
IPv6 - Due to advances in technology, four billion addresses were soon no longer
enough, and IPv6 was developed with eight groups of four hexadecimal numbers which
are known as hextets (two octets). This structure can generate approximately 3.4x10*°
addresses.
IPv6 addresses have not yet been fully integrated in modern use cases.
Network Classes
Over time, as more and more people began using the internet, the amount of available
IPv4 addresses started to become depleted. To resolve that issue, subnet masks were
implemented to increase the available IPv4 address pool.
Subnet masks define which octets represent the network ID, with the remainder used
for hosts on the same network.
In a subnet mask, 255 means the octet must be the same in all IP addresses to be on
the same network.


### Textbook — strona 19

Subnet mask 0 means any address with matching octets (255) can use this octet to
create a unique address.
The following illustration shows private IP address subnet classes.
Class by Mask
The network The hosts
C IP address: 192 . 168 . 001. | 000
Subnet mask: 255 - 255:. 255 ; | 000
The network The hosts
B IP address: 172.016 . | 000 . 000
Subnet mask: 255 . 255. | 000 . 000
The network The hosts
A IP address: 010 . | 000 . 000 . 000
Subnet mask: 255 . | 000. 000 . 000


### Textbook — strona 20

Section 4: Network Protocols and Commands
Protocols can be considered “languages” of data transfer. To communicate properly,
two or more devices must first agree to use the same “language”.
Protocols are predefined sets of rules describing how something should work or
behave. They help maintain order among different technologies.
Network Protocol Examples
IP - The Internet Protocol is used to establish communication over the network, without
delivery verification.
DNS - Dynamic Name Service is a protocol used to translate domain names to IP
addresses, and vice versa.
DHCP - The Dynamic Host Configuration Protocol is used to allocate IP addresses to new
computers that join the network.
HTTP - The Hypertext Transfer Protocol is used to transfer text-based data, such as web
pages, over the Internet.
HTTPS - HTTPS is a secure implementation of HTTP. It encrypts the transferred data to
prevent it from being intercepted.
Network Commands
Commands are used in network configuration, maintenance, troubleshooting, and
more.
An example of a powerful use of network commands is for error detection.
It is essential for any network to frequently run commands that check the state of the
network and monitor it.
Although some systems enable network configuration via a GUI, the configuration is still
often done via the CLI.


### Textbook — strona 21

Windows Network Command Examples
Ping
Ping is the most common command in administrative networking activity.
It is used to check connectivity between computers over the network.
It also provides information, such as connection speed and reliability.
Command:
Ping x.x.x.x

Example:

C:\Windows\system32> ping 8.8.8.8

Pinging 8.8.8.8 with 32 bytes of data:

Reply from 8.8.8.8: bytes=32 time=224ms TTL=54

Reply from 8.8.8.8: bytes=32 time=681ms TTL=54

Reply from 8.8.8.8: bytes=32 time=319ms TTL=54

Reply from 8.8.8.8: bytes=32 time=103ms TTL=54

Ping statistics for 8.8.8.8:

Packets: Sent = 4, Received = 4, Lost = @ (@% loss),
Approximate round trip times in milli-seconds:
Minimum = 103ms, Maximum = 681ms, Average = 331ms
IPconfig
ipconfig - displays a computer’s IP configuration.
ipconfig /all — displays extended information.
It can also request a new IP address if a DHCP server is configured.
ipconfig /release — drops an IP address.
ipconfig /renew — requests a new IP address.
Command:
ipconfig


### Textbook — strona 22

Example:

C:\Windows\system32> ipconfig

Windows IP Configuration

Ethernet adapter Ethernet:

Connection-specific DNS Suffix .:
Link-local IPv6 Address... . . : £b21::b23e:28e9:c76b:7b35%11
IPv4 Address... ....... . ? 192.168.5.11
Subnet Mask... ..... . . . ? 255.255.255.0
Default Gateway ........ . 2 192.168.5.1
Nslookup
Computers use IP addresses to communicate with each other, while humans use names
that are easier to remember than numbers.
Nslookup sends a query to get the name of a computer by its IP address.
It can also do the opposite - query an IP address by the domain name.
Command:
nslookup x.x.x.x

Example:

C:\Windows\system32> nslookup www.cyber.com

Server: pfSense.c122b.lan

Address: 192.168.0.1

Non-authoritative answer:

Name: cyber.com

Address: 199.244.49.102

Aliases: www.cyber.com

C:\Windows\system32> nslookup 199.244.49.102

Server: pfSense.c122b.lan

Address: 192.168.0.1


### Textbook — strona 23

Tracert
Information in the network passes through multiple stations on the way to its
destination.
Tracert displays all the stations (hops) along the route taken by the information to its
destination.
It can work with a domain name or an IP address.
Command:
tracert X.x.x.x
Example:
C:\Windows\system32> tracert 8.8.8.8
Tracing route to dns.google [8.8.8.8]
over a maximum of 3@ hops:
1 <1 ms <1 ms <1 ms pfSense.cl22b.lan [192.168.0.1]
2 115 ms 78 ms 59 ms 192.168.1.1
3 * * * Request timed out.
4 * * * Request timed out.
5 241 ms 178 ms 218 ms 172.17.10.182
6 * * = Request timed out.
7 bs is * Request timed out.
8 * # m= Request timed out.
9 * * 259 ms core-213-57-0-69.PT.hotnet.net.il [213.57.0.69]
10 «281 ms) «245 ms) 225 ms_ core-213-57-3-150.HFA.hotnet.net.il [213.57.3.150]
11 201 ms 174 ms 228 ms 108.170.251.129
12 188 ms 23 ms 326 ms 74.125.37.167
13 +131 ms 83 ms 109 ms dns.google [8.8.8.8]
Trace complete.


### Textbook — strona 24

Netsh
A fast way to configure network information is to use the netsh command.
It allows the configuration of the IP address, DNS, default gateway, and various network
functions.
The example below shows how to set an IP address and verify settings using netsh.
Command:
Netsh [command \ option ]
Example:
C:\Windows\system32> netsh interface ip set address “Ethernet" static
192.168.10.5 255.255.255.0 192.168.10.1
C:\Windows\system32> netsh interface ip show config
Configuration for interface "Ethernet"
DHCP enabled: No)
Default Gateway: 192.168.10.1
Gateway Metric: 1
InterfaceMetric: 5
Statically Configured DNS Servers: None
Register with which suffix: Primary only
Statically Configured WINS Servers: None
é Lab — Local Network Configuration
— J | Learn about and practice CLI network commands on Windows, using CMD.
m=:
Perform the instructions in lab document Net-01-L1.


### Textbook — strona 25

Section 5: Wireless Technologies
Wireless networks for computer communication are possible.
Wireless media features better flexibility than wired media, due to the absence of
cables connected to end devices.
Information is transmitted using radio frequencies, which, however, does pose some
security challenges.
8
om \
0 \ -ao
i) o
H
Re i) ‘
* i) 2»
. \ -
ey 1 ”
x i) Fal
By, 1 rai
~*~
| 7 |
Besse 5
Wireless Network
Security Issues
Coverage Area - The ideal environment for this technology is open space.
Some building materials can limit the range that wireless systems cover.
Transmission Interference - Many common devices, such as microwave ovens and
wireless communication devices, also transmit radio frequencies.
Signals from such equipment may interfere with signals transmitted in a wireless
network, and affect their quality.
Security - The absence of physical media exposes the network to the public and allows
others to discover it and try to gain access to it, without authorization to do so.


### Textbook — strona 26

Shared Medium - The technology operates in half-duplex, which means only one device
can send and receive information at a time.
When more and more users connect to the network, the available bandwidth for each
user will decrease accordingly.
Wireless LAN Components
AP - Access Point is the component that allows end devices to connect to a network
wirelessly using radio waves. The access point itself will be connected to the network
via cable.
Wireless NIC Adapter - For a device to connect to a wireless network, it must have a
wireless NIC adapter to send and receive the information.
Wireless NIC adapters can either be an external device or integrated in the computer.
Wireless Technologies
Wi-Fi - Wi-Fi (Wlreless Fidelity) is a technology based on IEEE 802.11 standards that
allows wireless connection to a network via radio waves.
Wi-Fi is used for LAN networks in shared spaces.
Wi-MAX - Wi-MAX is an implementation of a wireless network connection over a wide
area. It is used for LAN and MAN implementations.
Bluetooth - Bluetooth is an implementation of WPAN (Wireless Personal Area
Network). It is mainly used to pair devices and allows communication at up to 100
meters.


### Textbook — strona 27

Wireless Standards
Over the years, network standards were developed and modified to improve speed and
bandwidth.
Wireless Standard History:
BACKWARD
STANDARD MAX SPEED FREQUENCY
COMPATIBLE
802.11a 54 Mb/s 5 GHz No
802.11b 11 Mb/s 2.4 GHz No
802.11g 54 Mb/s 2.4 GHz 802.11a
802.11n 600 Mb/s 2.4 GHz & 5 GHz 802.11a/b/g
802.11ac 1.3 Gb/s 5 GHZ 802.11a/n
802.11ax 14 Gb/s* 1 GHz - 7.125 GHz 802.11a/b/g/n/ac


### Textbook — strona 28

Media Comparison
Copper Fiber Wi-Fi
10 Mb/s - 10 Gb/s 10 Mb/s - 100 Gb/s 54 Mb/s - 14 Gb/s
D d th
Up to 100 meters Up to 100 Km epen on e
transmitter’s strength
Cheap Expensive Relatively cheap
Vulnerable to the effects Expensive equipment The signal can be affected
of EMI and RFI and less flexibility by local structures


# Chapter 2: Network Fundamentals


### Textbook — strona 29

| Chapter 2: Network Fundamentals
Section 1: Network Protocols and Models
Client-Server Model
A client represents the endpoint device (not necessarily a PC) that requested an
operation.
A server represents the endpoint device that receives a request and performs the
requested operation.
z Dear Server 18.77.22.44,
www | can you please send my
c—o Facebook home page.
Sure! 10.2.2.7, here you
go, enjoy! _
The Client-Server model is a distributed application structure that manages tasks and
workloads by sharing them among providers of resources and services (servers), and
delivers responses to service requesters (clients).
An alternative method is to use broadcast or multicast channels to distribute
information.
Common Network Protocols
HTTP - HTTP is an unsecure protocol used to transfer information over the web.
Due to the fact that HTTP traffic is not encrypted, it can be sniffed on the network.
For example, if credit card information is entered at an HTTP website, it can be
captured in simple text format.


### Textbook — strona 30

HTTPS - HTTPS is the encrypted version of HTTP.
It is used for secure communication and is widely used on the Internet.
Communication is encrypted using TLS (Transport Layer Security) or SSL (Secure Socket
Layer).
DNS - Translates domain names to IP addresses according to predefined databases.
The DNS protocol is used for address resolution in a network.
For example, when a URL is entered in a browser, the DNS protocol translates the
domain that was entered to an IP address.
FTP - File Transfer protocol is used to transfer files over the network.
For example, the FTP service can be used to transfer files to another device over the
network.
DHCP - The DHCP service is responsible for assigning an IP address to each device on a
network configured to use DHCP, such as PCs, routers, firewalls, servers, and others.
For example, a PC configured with DHCP will automatically be assigned an IP address
upon startup.
SMTP - Simple Mail Transfer Protocol is the standard protocol for mail transfer over the
Internet.
For example, when an Email is sent over the network, the SMTP protocol manages the
operation.
SSH - Secure SHell is a secure command-line protocol that allows the user to run remote
commands on a remote machine.
Any data that passes through SSH is encrypted.
For example, when a remote connection is made to a device, the connection is made
using SSH on port 22.
ICMP - Internet Control Message Protocol is used by network devices to generate error
messages when IP packets are not able to reach their destination.


### Textbook — strona 31

Network Models
The idea behind creating a networking model was to set a standard for the
development and usage of network components.
Standards allow devices to communicate without requiring continuous configuration in
different device platforms.
In addition, dividing the networking process into smaller sub-processes helps debug
issues and pinpoint solutions.
OSI vs TCP/IP
Today, OSI and TCP/IP are very similar due to the way they evolved over time.
OSI is often used as an educational model, while TCP/IP is used more as a practical
model.
OSI is a network model in which each functionality of the network is represented by a
layer.
There are seven layers, in which the functionality of each is dependent on the one
below it.
OSI was developed by the International Organization of Standardization.
The first TCP/IP specification was submitted several years after the OSI model.
The original TCP/IP model consisted of 4 layers but was later updated to the current 5
layers. However, the 4-layer version is still more commonly used.
TCP/IP is typically used for network analysis due to its lesser involvement with the top 3
layers.


### Textbook — strona 32

Section 2: OSI Model
OSI (Open Systems Interconnection) was developed by the International Organization
for Standardization (ISO) in 1974.
OSI defines a networking framework to implement protocols in layers. It conceptually
divides computer network architecture into a logical seven-layer progression.
Lower layers deal with electrical signals, chunks of binary data, and routing data across
networks.
Higher levels cover network requests and responses, data representation, and network
protocols, from a user's perspective.
The OSI model is divided into seven layers: Application, Presentation, Session,
Transport, Network, Datalink, and Physical.
When network traffic is generated, it is assembled (encapsulated) from the top layer to
the bottom layer.
When received, traffic goes through the model in the reverse direction: from bottom to
top (decapsulation).

Transmit Data Receive Data

APPLICATION APPLICATION
PRESENTATION PRESENTATION
SESSION SESSION
TRANSPORT TRANSPORT

NETWORK NETWORK

DATA LINK DATA LINK

PHYSICAL Physical Layer PHYSICAL

OSI Model Structure


### Textbook — strona 33

OSI Layers
Layer 7 Application - Users interact directly with applications that operate at Layer 7.
Examples of Layer 7 applications include web browsers such as Google Chrome, Firefox,
and Safari, and other applications, such as SSH and FTP.
Layer 6 Presentation - The Presentation Layer prepares or translates data from
application format to network format, and vice versa.
An example of the Presentation Layer operation is the encryption and decryption
process.
Layer 5 Session - The session layer is responsible for creating a session between two
devices. It is also responsible for session checkpoints and recovery.
Layer 4 Transport - The Transport Layer handles the coordination of data transfer
between end systems and hosts, including how much data to send, at what rate,
destination, and more. Data in this layer is organized in segments.
The transport layer determines if the connection should be instantiated, how to verify
data integrity, how to recover from a connection error, and if retransmission is
necessary. The protocols in this layer provide flow control, multiplexing, and reliability.
Layer 3 Network - The Network Layer organizes data into packets, known as IP
datagrams. The datagrams contain logical source and destination addresses.
Routers operate in this layer.
The Network Layer’s job is to allow hosts to send packets across multiple paths to any
other network, and deliver them to their destinations, via routers that operate in
Layer 3.
Diagnostic tools, such as ping and tracert, operate in this layer.
Layer 2 Data Link - The Data Link Layer provides node-to-node data transfer (between
two directly connected nodes) and can provide the means to detect errors that may
occur in the Physical Layer. Data in this layer is organized into frames.
The Data Link Layer includes two sub-layers: MAC (Media Access Control) and LLC
(Logical Link Control).
Switches operate in this layer.


### Textbook — strona 34

Layer1 Physical - The Physical Layer defines the details of how data is physically sent
through the network.
This layer determines how bits are electrically or optically transferred by hardware
devices that interface directly with a network medium, such as coaxial cable, optical
fiber, or twisted-pair copper wire.
Hubs operate in this layer.
Protocols used in OSI Layers
Each network protocol is assigned to a particular OSI layer.
Common protocols in each layer include:

LAYER PROTOCOLS

Application DNS, DHCP, SSH, HTTPS, FTP, SNMP, SMTP, POP3

. Encryption, Encoding, SSL/TLS, ASCII, EBCDIC, TIFF, GIF, PICT,
Presentation
JPEG, MPEG, MIDI

Session NFS, NetBios names, RPC, SQL

Transport TCP, UDP, RTP, SCTP

Network IPv4, IPv6, ICMPv4, ICMPv6, IPX

Data Link Ethernet, PPP, FDDI, ATM, IEEE 802.5/ 802.2, HDLC, Frame Relay

. Ethernet (IEEE802.3), Wi-Fi (IEEE 802.11), FDDI, B8ZS, V.35, V.24,
Physical
RJ45


### Textbook — strona 35

Memory Tips for OSI Layers
Layer 1 to Layer 7 - Please Do Not Throw Sausage Pizza Away
Layer 1 to Layer 7 - Please Do Not Touch Steve’s Pet Alligator
Layer 7 to Layer 1 - All People Seem To Need Data Processing


### Textbook — strona 36

Section 3: TCP/IP Model
TCP/IP (Transmission Control Protocol/Internet Protocol) was developed by DARPA in
the US Department of Defense, in 1982.
This model is a suite of communication protocols used to interconnect network devices
on the Internet.
The model describes how data is exchanged over the Internet, including how data
should be divided into packets, addressed, transmitted, routed, and received by the
destination.
TCP/IP was designed to make networks reliable and enable them to automatically
recover from a failure of any device on the network.
TCP/IP Layers
Layers in the TCP/IP model are similar to those in the OSI, except for the top three
layers.
TCP/IP uses the client-server model of communication in which a user or machine is
given access to a service by another computer on the network.
Collectively, the TCP/IP suite of protocols is classified as “Stateless”, which means each
client request is considered new, and is unrelated to previous requests.
Transmit Data Receive Data
APPLICATION APPLICATION
TRANSPORT TRANSPORT
NETWORK NETWORK
Network Access Physical Layer Network Access
TCP/IP Model Structure


### Textbook — strona 37

Layer 4 Application - The Application Layer defines TCP/IP application protocols and
how host programs interface with Transport Layer services to use the network.
The Application Layer includes all higher-level protocols, such as DNS, HTTP, Telnet,
SSH, FTP, TFTP, SNMP, SMTP, DHCP, X Windows, RDP, and others.
The TCP/IP top layer is equivalent to the combined three top layers of OSI.
Layer 3 Transport — The Transport Layer in TCP/IP corresponds to the Transport Layer in
OSI. It handles the coordination of data transfer between end systems and hosts,
including how much data to send, at what rate, destinations, etc.
The transport layer determines if the connection should be instantiated, how to verify
data integrity, how to recover from a connection error, and if retransmission is
necessary. Data in this layer is organized in segments.
The protocols in this layer provide flow control, multiplexing, and reliability.
Layer 2 Internet - The Internet Layer organizes data into packets known as IP
datagrams. The datagrams contain logical source and destination addresses.
The Internet Layer’s job is to allow hosts to send packets across multiple paths to any
other network, and deliver them to their destinations, via routers operating on this
layer.
Routers operate in this layer.
The Internet layer in TCP/IP corresponds to the Network Layer in OSI.
Layer 1 Network Access - The Network Access Layer is the lowest layer of the TCP/IP
protocol model. It corresponds to the Data Link and Physical layers of OSI.
Packets from the Internet layer are sent to the Network Access layer for delivery within
the physical network. Data in this layer is organized in frames.
Protocols in this layer provide the means for the system to deliver data to other devices
in a directly connected network, using physical addresses (MACs).
The protocols and standards defined for this layer dictate how data is transmitted on
the media (Ethernet cable, wireless connection, others).
The Access Layer of the TCP/IP model corresponds to the Data Link and Physical layers
of OSI.


### Textbook — strona 38

Section 4: Transport Protocols and Logical Ports
TCP and UDP
TCP and UDP are protocols that operate in Layer 4 (Transport Layer), and are used to
transmit data over the network.
Note: There are other Transport Layer protocols, such as RTP and SCTP, but they are
beyond the scope of this section.
TCP is trusted and more commonly used than UDP, and is fully described in RFC 793.
It verifies the availability of all parties before initiating a connection by performing a
three-way handshake. It then marks packets and makes sure they are received in the
correct order.
UDP is less strict about data integrity and is more speed-oriented. It simply sends
packets, without checking the data, even if no device is ready to receive them.
This type of communication works better when streaming content, such as audio,
where some packets may be skipped without affecting the entire stream.
UDP is fully described in RFC 768.


### Textbook — strona 39

TCP vs UDP
TCP UDP
Connection-oriented protocol. Connectionless protocol.
Suited for applications that need fast,
Suited for applications that require high . PP
Pe pSaI sears efficient transmission. Also useful for
reliability, where transmission time is less
critical servers that answer small queries from
. large numbers of clients.
Rearranges data packets in the order Packets may arrive out of order, UDP does
specified. not rearrange them.
Guarantees that transferred data remains .
‘ = ae There is no guarantee that messages or
intact. If a packet is corrupt upon arrival, it 3 a" segs
. packets will reach their destinations.
is resent.
Performs error-checking but discards
Errors are detected via checksum. erroneous packets. Error recovery is not
attempted.
Relatively slow. Relatively fast.
Detection of error via checksum*. No error detection.
* Checksum is a piece of data that is calculated and represented as a number, and is
used for data integrity and error detection.


### Textbook — strona 40

TCP Flags
TCP uses flags to provide additional useful information or control the connection.
Flag Role
Synchronization - this is the first flag between two hosts, and
SYN . .
is used to establish a 3-way handshake.
AGE Acknowledged - acknowledges a successful receipt by the
host.
Ret Reset - Terminates a connection if a TCP failure occurs or a
conversation is not permitted.
FIN Finish - Requests connection termination.
PSH Push - Immediately sends all buffered data.
URG Urgent - Data with a URG segment is immediately forwarded
to the Application Layer.
3-Way Handshake
A 3-way handshake is responsible for communication between network devices that
use TCP.
The handshake is known as “3-way” because it includes 3 steps:
1. The client sends “SYN”.
2. The server responds with “SYN-ACK”.
3. The client finalizes with “ACK”.
If the process ends successfully, a connection is established between the client and the
server, and data can immediately be transferred between them.


### Textbook — strona 41

Client Server
HTML =
a cee)
ae
:
i]
i ee
3-Way Handshake Process
Session Termination
Session Termination is the last stage of a TCP connection. This is when communication
ends and the session is closed.
Step 1 - One of the sides (client) requests to close the connection, by sending a FIN flag
to the other side (server).
Step 2 - The receiver of the FIN flag (server) returns an ACK flag, to approve the request.
Step 3 -The server then sends a FIN flag to the client.
Step 4 - The client approves the FIN request by the server, and responds with an ACK
flag. The connection is then terminated.


### Textbook — strona 42

Client Server
= ©
ee
ee
ae
~
CE ie
Session Termination Process
Logical Ports
In computer science, a logical port is a number assigned to a “logical” connection, which
is used to represent a service or protocol on the end device.
There are 65,536 in TCP and 65,536 UDP ports, ranging from O to 65535.
An IP address can send packets to the destination host, but not to the destination
service on that end device.
As an example, a street address can lead to the correct building, but it does not specify
the apartment number within that building.


### Textbook — strona 43

Logical Port Groups
There are 65,536 ports in TCP and 65,536 in UDP, divided into three main groups, as
follows:
Well-Known Ports (0-1023) - Port numbers in the “well-known” range are assigned to
commonly used and essential protocols. The port numbers are permanent, and every
network administrator must know them.
The range includes protocols such as HTTPS, DNS, DHCP, Email protocols, and others.
Registered Ports (1024-49151) - IANA assigned these ports for IT companies that want
to register them for proprietary applications. For example, Microsoft RDP 3389 and
Dropbox 7600.
Dynamic and Private Ports (49152-65535) - This group covers the remaining logical
ports that are available for any application. The port range is known as “client ports”
and is usually used for logical client connection.
For example, a host connecting to a web server sends requests to port 80. This lets the
web server know which service the client is requesting. However, the return traffic
must be sent to a source port, which is chosen randomly. When the connection closes,
the port can be reused for another connection, enabling the client to establish multiple
connections and manage responses from multiple sources.


### Textbook — strona 44

Common Protocol Ports
The following table lists common network protocols and their TCP and UDP ports.
Protocol TCP/UDP Logical Ports Protocol TCP/UDP _ Logical Ports
HTTP TCP 80 SSH TCP 22
HTTPS TCP 443 RDP TCP 3389
DNS UDP 53 SMB TCP 445
DHCP UDP 67, 68 FTP TCP 20, 21
SMTP TCP 25 TFTP UDP 69
POP3 TCP 110 NTP UDP 123
Viewing Open Ports
Ports are used to receive and send data.
A web server will open Port 80 in listening mode if it intends to receive HTTP traffic.
A client will open a random port for each server it accesses when browsing the web.
To inspect open ports, use the command netstat —ab, where: a represents ‘all’, and b
represents the names.


### Textbook — strona 45

Netstat Example:
C:\WINDOWS\system32>netstat -ab
Active Connections
Proto Local Address Foreign Address State
TCP @.0.0.0:135 Leningrad:® LISTENING
[svchost.exe]
TCP @.0.0.0:443 Leningrad:® LISTENING
[vmware-hostd.exe]
TCP @.0.0.0:445 Leningrad:@ LISTENING
Can not obtain ownership information
TCP @.0.0.0:902 Leningrad:® LISTENING
[vmware -authd. exe]
TCP @.0.0.0:912 Leningrad:® LISTENING
[vmware -authd.exe]
TCP @.0.0.0:1536 Leningrad:@ LISTENING
[svchost.exe]
TCP @.0.0.0:1538 Leningrad:@ LISTENING
[svchost.exe]
TCP @.0.0.0:1539 Leningrad:® LISTENING
Short Practice
— According to the material learned in the previous part, answer the following
mm =| questions as best as you can. You can use external materials, such as
Internet searches.
1. Briefly describe the operation or function of each protocol layer.
(For example, Layer 6 encodes, encrypts, and compresses the
information.)
2. List at least two main protocols that operate in each layer. (For
example IP, ICMP-Network Layer.)
3. List two protocols that use TCP, and two that use UDP.
4. Describe the TCP 3-Way Handshake.
5. List the logical ports of the following protocols: HTTP, HTTPS, DNS,
FTP, SMTP.
6. How many layers do the TCP/IP and OSI models have, and what are
their names? (Try to answer from memory.)


### Textbook — strona 46

Section 5: Introduction to Wireshark
Wireshark is a free application that enables the capture and viewing of data traveling
back and forth on the network. It is able to read the contents of each packet and apply
different filters.
Wireshark is commonly used to troubleshoot network problems, and develop and test
software.
[a
aa @|5 xe S = £BIEBIAaak
(Winco e dspley titer. <oxi7> ES =] coresson... +
Capture
using this fter: (W]]entera cepturefiter, SSS) | irae sh =
No Interfaces found
Learn
User's Guide Wiki Questions and Answers Mailing Lists
You are running Wireshark 3.0.1 (v3.0.1-0-gea35icd8). You receive automatic updates.
© Ready to load or capture No Packets Profile: Default


### Textbook — strona 47

Capturing Data
When invoked, Wireshark presents an initial screen with a list of available network
interfaces. Selecting an interface will start the capture of all traffic that passes through
it.
Wireshark can also be used to open traffic captured by other tools, such as TCP dump.
a
4uc TDRE QeestseBaqan
Gs Gi Jenson +
1@.e@e¢88 16.1.26.1 157.249.1.. TLSv1.2 85 Application Data =|
2.078369 157.240.1.53 10.1.28.1 TCP 60443 + 8199 [ACK] Seq=1 Ack=32 Win=144 Len=0 =
3.131368 10.1.26.1 62.0.136... TCP 55 [TCP segment of a reassembled PDU) =
40.131571 62.0.136.237 16.1.20.1 TCP 66 8093 + 11632 [ACK] Seq=1 Ack=2 Win=254 Len=@ SLE=1 SRE=2 —
5@.155242 157.240.1.53 1@.1.28.1 TLSv1.2 92 Application Data FJ
6@.195718 10.1.20.1 157.240.1.. TCP 548199 + 443 [ACK] Seq=32 Ack=39 Win=1027 Len=@ =
| 91.228919 146.185.219.33 16.1.20.1 TCP 69.80 + 49803 [ACK] Seq=l Ack=1 Win=501 Len=0 =
if . eep-A e + 116 A q: Ack=: = =
Frame 1: 85 bytes on wire (680 bits), 85 bytes captured (680 bits) on interface 0 a
Ethernet II, Src: HewlettP_3e:5b:9e (f4:39:09:3e:5b:9e), Dst: Fortinet_4e:8b:12 (@4:d5:90:4e:8b:12)
Internet Protocol Version 4, Src: 1@.1.20.1, Dst: 157.240.1.53
Transmission Control Protocol, Src Port: 8199, Dst Port: 443, Seq: 1, Ack: 1, Len: 31 s
9000 04 d5 90 4e 8b 12 F4 39 09 3e 5b 9e O8 00 45 00 Ne +9 ->[---E is
@@ 47 da 81 40 00 8@ G6 63 88 Ga O1 14 G1 9d FO G @ c
61 35 26 67 61 bb Sa 42 67 7e aO Oc O9 b2 5A 18 5 2B gy Pp
@4 @3 86 Ge 00 00 17 03 03 20 1a ca 99 84 24 00 ¥
Main View
Packet List - Packet List is the main view of Wireshark. It lists captured packets in the
order of their capture, and offers various search and filter options.
Packet Details - Packet Details is the part in the middle that displays the details of a
specific packet.
The details are divided into fields corresponding to TCP/IP layers, such as the Frame
(Physical), Ethernet (Data Link), and IP (Network).
Packet Bytes - The bottom part of the view corresponds to the actual bytes of the
selected packet, in hexadecimal format and ASCII encoding.


### Textbook — strona 48

ICMP Traffic
The Ping command uses ICMP and includes a request and a reply.
Each ICMP packet is numbered and can be identified to find a corresponding response.
ICMP has only four fields since it is a Layer 3 protocol.
Each ICMP echo (ping) packet includes all the basic symbols and numbers on the
keyboard.
a
aacoeir Rei CeessFsSQ2>aqaaant
No. Time ‘Source Destination Protocol Length Info cet
f 1 6.000000 172.42.0.157 172.42.0.140 ‘ICMP 98 Echo (ping) request id-0xdcda, seq=1/256, tt1-64
Oe 2 0.300934 172.42.0.146 172.42.0.157 ICMP 98 Echo (ping) reply id=@x@cda, seq=1/256, ttl=64
3 1.006925 172.42.0.157 172.42.0.140 ICMP 98 Echo (ping) request id=@x@cda, seq=2/512, tt1=64
4 1.298136 172.42.0.140 172.42.0.157 ICMP 98 Echo (ping) reply id=@x@cda, seq=2/512, ttl-64
Frame 1: 98 bytes on wire (784 bits), 98 bytes captured (784 bits) tos
Ethernet II, Src: Vmware_c6:21:44 (06:@c:29:c6:21:44), Dst: SamsungE_83:45:3b (@4:d6:aa:83:45:3b)
Internet Protocol Version 4, Src: 172.42.0.157, Dst: 172.42.0.140
» Internet Control Message Protocol
Type: 8 (Echo (ping) request)
code: 0
Checksum: @x7d9@ [correct]
[Checksum Status: Good]
Identifier (BE): 3290 (@x@cda)
Identifier (LE): 55820 (@xda@c)
Sequence number (BE): 1 (@x@001)
Sequence number (LE): 256 (@x@100) v
2 @4 d6 aa 83 45 3b 08 Qc 29 c6 21 44 G8 0G 45 00 &3 P eights ES
ee1 @8 54 8c 1a 40 06 4@ G1 55 11 ac 2a 68 9d ac 2a T.-@@ U--*---*
020 @@ 8c @8 86 7d 90 Oc da OO 61 e9 53 bb 5c G8 BE } *Se\e°
030 09 00 04 11 06 00 00 0 09.00101112131415 --
0240 16 17 18 19 1a 1b 1c 1d 1e 1f 26 21 22 23 24 25 Lage
0050 26 27 28 29 2a 2b 2c 2d 2e 2F 30 31 32 33 34.35 = &'()*4,- ./012345 ¥
@ * cw sample.cap Packets; 8 : Displayed: 8 (100.0%) Profile: Default


### Textbook — strona 49

DNS Traffic
DNS traffic includes multiple requests and replies.
Most of a search tree will not appear in a packet; only the request and response.
DNS may try to automatically resolve both A and AAAA records corresponding to the
IPv4 and IPv6 addresses, respectively.
a
AecO1:HREC ese etFeS2aqaqar
Expression. +
No. Time Source Destination Protocol Length Info
E 1 2.090000 172.42.0.151 172.42.0.138 DNS 74 Standard query @xd282 AAAA api.segment.io
« 2 0.010187 172.42.0.138 172.42.0.151 DNS: 158 Standard query response @xd282 AAAA api.segment.io SOA
3 5.906976 172.42.0.157 172.42.0.138 DNS 71 Standard query @xb97@ A hackeru.com
45.994438 172.42.0.138 172.42.0.157 DNS 87 Standard query response @xb970 A hackeru.com A 107.180.
5 5.995163 172.42.0.157 172.42.0.138 DNS 71 Standard query @x@276 AAAA hackeru.com
6 6.121930 172.42.0.138 172.42.0.157 DNS 142 Standard query response @x@276 AAAA hackeru.com SOA nsd
Frame 1: 74 bytes on wire (592 bits), 74 bytes captured (592 bits) “
Ethernet II, Src: LcfcHefe_7a:4b:17 (e8:6a:64:7a:4b:17), Dst: D-LinkIn_d7:48:d@ (78:32:1b:d7:48:de)
Internet Protocol Version 4, Src: 172.42.0.151, Dst: 172.42.0.138
User Datagram Protocol, Src Port: 62297, Dst Port: 53
~ Domain Name System (query)
Transaction ID: @xd282
Flags: @x@1@0 Standard query
Questions: 1
Answer RRS:
Authority RRs: @
Additional RRs: @ v
) 78 32 1b d7 48 d@ e8 Ga 64 7a 4b 17 @8 06 45 06 = x2--H--j dzK---E
219 @@ 3c Gf bb 0 CO 8811 71 BB ac 2a 097 ac 2a -<o geet
0920 @@ Ba f3 59 @@ 35 @@ 28 b1 10 d2 82 @1 06 G2 1 Y-5-¢ oe
220 @@ 80 00 20 62 20 63 G1 70 69 O7 73 65 67 6d 6S a pi-segme
10 Ge 74 @2 69 6F 00 0 1c 00 01 nt-io
@ * onssample.cap Packets: 6 * Displayed: 6 (100.0%) Profile: Default


### Textbook — strona 50

HTTP Traffic
HTTP is an unsecure protocol used to transfer information over the web.
Since HTTP traffic is not encrypted, it can be sniffed on the network.
(iP Sompiocon =e x
File Edit View Go Capture Analyze Statistics Telephony Wireless Tools Help
4G C4O\LDRBEVCeeZtseSaaanh
ity EGS =) Expression. +
No, Time source Destination Protocol Length Info
16 14.384881 172.42.0.157 192.195.77.80 HTTP 779 POST /login-form/ HTTP/1.1_(application/x-waw-form-ur
e 22 14.571270 192.195.77.80 172.42.0.157 HTTP 357 HTTP/1.1 200 OK (text/html)
Frame 16: 779 bytes on wire (6232 bits), 779 bytes captured (6232 bits)
Ethernet II, Src: Vmware_c6:21:44 (08:0c:29:c6:21:44), Dst: D-LinkIn_d7:48:d@ (78:32:1b:d7:48:d@)
Internet Protocol Version 4, Src: 172.42.0.157, Dst: 192.195.77.80
Transmission Control Protocol, Src Port: 60834, Dst Port: 8@, Seq: 1, Ack: 1, Len: 713
» HTML Form URL Encoded: application/x-www-form-urlencoded
Form item: “username” = "lionk"
Form item: "password" = "Aa123456"
Form item: “submit” = "Login®
960 78 32 1b d7 48 do 00 Oc 29 cé 21 44 SMEG 45.00 x2 -H- )- IOBBE ~
0010 @2 fd bf 2f 40 82 40 e6 bd FO ac 2a G8 9d cB C3 10-0 *
4d 5@ ed a2 @@ 5@ dd 31 94 33 cb c3 de c6 8918 MP. -P-1 3
9 @0 eS bd ca 628 00 61 G1 @8 Ga c7 af be 43 d9 21 cel
10 5f ed 50 4f 53 54 20 2F 6c GF 67 69 Ge 2d 66 GF _-POST / login-fo
0050 72 6d 2f 26 48 54 54 5@ 2 31 2e 31 @d @a 48 GF =—rm/ HTTP /1.1--Ho
9 73 74 3a 2077 7777 2e 64 65 6d Gf 2e 61 Gd 69 = st: www. demo.ami
e 74 6a 61 6b 68 75 2e 63 GF 6d Od Oa 55 73 65 72 tjakhu.c om--User
59 2d 41 67 65 Ge 74 3a 20 4d GF 7a 69 6c 6c 61 2F Agent: Nozilla/
990 35 2e 30 2@ 28 58 31 31 3b 20 4c 69 Ge 75 78 26 «5. (X11 ; Linux
2 78 38 36 Sf 36 34 3b 20 72 76 3a 36 30 2e 30 29 «= x86_64; rv:60.0) wl
QF HTTP sample.cap Packets: 31 Displayed: 2 (6.5%) Profile: Default,
Captured data can be saved as a .pcap or .pcapng files for later use or sharing. This
option is available by clicking “File” and selecting “Save As...”.
The .pcapng files store additional information regarding captured data, such as
interfaces, statistics, name resolution, and more.


### Textbook — strona 51

(Mf *Cthemet 3 - ia x
File Edit View Go Capture Analyze Statistics Telephony Wireless Tools Help
Open Ctrl+0 zFTaabeaaanr
Open Recent pO pression. +
Merge. Destination Protocol Length Info ”
Import from Hex Bump L 127.0.0.1 TcP 94 220i
Close Ctrlew L 127.0.0.1 TCP 96 220:
L 127.0.0.1 TcP 94 220:
=e oe L 127.0.0.1 TCP 96 220:
| Seven ate SfteS 127.0.0.1 1c 94 220;
File Set i 127.0.0.1 TcP 96 220:
L 127.0.0.1 TCP 94 220%
Export Specified Packets. l 127.0.0.1 TCP 96 220:
Export Packet Dissections vo 127.0.0.1 TCP 94 2207
Export Packet Bytes... Cirle ShifteX 1 127.0.0.1 TCP 96 220:
Export PDUs to Files. L 127.0.0.1 TCP 94 220;
Export TLS Session Keys. 5
Export Objects »
its), 55 bytes captured (44@ bits) on interface @ “
Print Cirle? 100 (00:00:00:00:00:00), Dst: 00:00:00 00:00:00 (90:00:00:0¢
1 127.0.0.1, Dst: 127.0.0.1
ae Sree be I A. OP. “i
€ >
e082 80 00 e0 22 20 00 FEMME co 00 ea es co 4500 CRE
e018 @8 29 c@ 71 49 a2 80 a6 G0 CO 7F OO GO C1 7F OO = -)-g@--- -----
0020 @@ 01 08 9b OB 9a ac G7 Je 14 1469 16 885018 «ga -P-
003@ FF #F Se 27 8 00 4d AM
QO F wireshsrk_Ethernet 3_20200722154827_301240.peapng || Packets: 16 + Displayed: 16 (100.0%) || Profile: Default


### Textbook — strona 52

Filtering Traffic
A .pcap file can contain thousands of packets, even after a few seconds of logging.
To view the packets efficiently, filters can be applied. Filters can also be applied during
capture to prevent the capture of unwanted packets.
Filters are logical conditions that are applied using &&, | |, == and !=.
Brackets can also be used.
MLITTP Semple cop eR
File Edit View Go Capture Analyze Statistics Telephony Wireless Tools Help
Aec@1rOoRelir_ee2ts#etaaak
(Wacpiy e display iter. <cariy> CES ~) exwession. | +
No. Time Source Destination Protocol Length Info =>
| 1 8.000000 172.42.0.157 81.218.31.137 Top 66 38908 + 86 [ACK] Seq=1 Ack=1 Win=329 Len=0 ene |
+3 3.426254 172.42.0,151 | ncaa, ee: 60 16852 + 8@ [ACK] Seq=1 Ack=1 Win=1023 Len=1
4 3.488723 85.114.134.23 1 Mark/Unmark Packet 66 80 + 16852 [ACK] Seq=1 Ack=2 Win=260 Len=0 SLE=1
Ignore/Unignore Packet
Set/Unset Time Reference
Time Shift.
Packet Comment.
9 14.146553 172.42.0.157 1 74 60446 + 86 [SYN] Seq=@ Win=29260 Len=@ MSS=146@ S
16 14. 266035 172.42.0.157 1 Edit Resolved Name 74 60834 + 86 [SYN] Seq=@ Win=2926@ Len=@ MSS=146@ S
11 14.206138 172.42.0.157 1 Seq=@ Win=29200 Len=@ MSS=1460 S
12.14.218727—172.217.22.18 7 eee ssiiter sees | ace Seqe0 Ack=1 Win=6010? Len=ofllll
a OE + Prepare a Filter > Not Selected pee eee eee
= Conversation Filter , and Selected z:
Frame 3: 60 bytes on wire (48@ bits), 6@ by Celadon Canveretion > of Selected
Ethernet II, Src: LefcHefe_7a:4b:17 (e8:6a SCIP > nor seleered 248:de)
Internet Protocol Version 4, Src: 172.42.0. 5 vant
Transmission Control Protocol, Src Port: 1¢ Fallow _ espe net selected
|
) 78 32 1b d7 48 d@ e8 Ga 64 7a 4b 17 68 Copy »
©9 29 ae 6c 40 00 80 05 4 17 ac 2a 00
86 17 41 d4 @@ 50.96 16 c9 1f 18 Sb fF —_—Protocol Preferences y
9 @3 fF Ga Se 68 22 02 20 00 08 20 26 Decode As...
‘Show Packet in New Window
O FY arp samplecap Packets: 31 « Displayed: 31 (100.0%) Profile: Default


### Textbook — strona 53

Wireshark Filters
Wireshark includes many display filters.
&& - means that both conditions are searched to match packets.
| | - means that one of the conditions is searched to match packets.
== - searches for everything that matches the specified parameter.
!= - searches for everything that doesn’t match the specified parameter.
The following table lists some useful filters.
Filter Data
Find a match for packets using a specific protocol (i.e.
Protocol Name
ICMP, ARP, HTTP, DNS).
“ Find a match for this address in the source and
ip.addr == 10.0.0.3 oo.
destination.
ip.dst != 10.0.0.2 Find all matches that do not have this destination.
ip.sre != 10.0.0.3 Find all matches that are not from this source.
tcp.port == 25 &&
P-P Find packets that match both port numbers in TCP.
tcp.port == 80
udp.port == 53 || Find packets that match one of the port numbers in
udp.port == 69 UDP.
Find packets that match a specific port number of the
tcp.dstport == 25 an
destination in TCP.


### Textbook — strona 54

Following Traffic
After capturing traffic and filtering, stream inspection can be done.
Streams are collections of packets from the same conversation.
Left-click a packet to choose the option to follow a stream, which can be TCP, UDP, or
HTTP.
Unless traffic is encrypted, it should be readable.
een :
\aneaoe: OID; ne sn.) Gak/200010 efoe0.0
ia etcetera tamed rds
fecolmeerneny
[peaakirvar they dane Or
Scawe pec eeesumicceonratees
eoeeameee
aoe ae cas een ares ser See seb oS SSS sO SSS rec mint
epee
seare-Ketcamnend at taba 20
erry
ras Se kd
[ee
acon
eee
(Ser nodfed sat 15 an 205203787 mt
Sacre Soran
pee
sop
‘Sa rom
jlo
See wr otek ata >
Selsey ct ayaa pee
Sere tec Henao
Scam pees
Presuerieerceery
ear ation
Re aera |.


### Textbook — strona 55

Encrypted traffic will not be readable, and will appear as non-meaningful characters.
[SSt42.0-OpensSHt_7.9p1 Debiar-9 =]
Sidecars

revrrare

nic dua anezss sacs rach hz i236 ho ch a 051 ean Ln tans sha. edman uns 2 Ae isn rusia Ae ena gun hte
Leer epee teatro entice poe ir argent Sepp ren bees enter epnepeoerti
Mersusceacntsn con oopsesnconnces fot noses cosesat mgm sein sec acon or atais ree loom see eek me onals an aesceeen omen oscoaste oececr oat
engrenthcomnn SSpngusrtatcm: ace tbturwcs ont testa cot cect gomoepaoh omentae vorgepnas ara. emeecbapapemtramyaansineoabgeac oars
Sepsis smorc at ss ep aneynt se vacmensconi arene meres amen oon ocr Gat racers eau ot Gereelcaries ceaeren aT
Setecpec cet at cut eens onto et eneeest cine: ofnemes cone mpcn ohmic: <oretca tiie al “eeceieen meee me
inundation ite tse ba gtr apa at wae ie pep eeinge sli negepieasttetsinen ga) teh goa
Sctieaiehaina oat aal_ieaaet su er aes Beate eae soreciseonaass, Uasuibpent sesoatamed weabt oncise meet spatenmancmeatsemeaerchon eon
eee Se ee ree ree eae me ee eee re eee ome
Exieeeeh om nas pudonah om nce spec cee es aaiec erat mac sel--uner maniac cones ie aneeoctartnacaer Er anerfoah confess: iz omen rar
Stectecname et erat ctmce inerera miner ant Suipecsalitlineidat—mememeation mommenemtones ce ee aim amie eae eae
ee eae

ra lewen ie aed mage ach tae Oo BM DG

Car

[erence ees

oa

een

patie es eee

Ser ee

ramet ae are

cers a as a ae

Peas er ra ee si SBS RCS

fi

caer eree

Lee ci aaa ae WP eae

zorwramkecnsial

ee ee ee ee ae ee ee

Preeti en a

NRT ee TC

Fare eri a es}

Pe-anigahion rics ferry ee ae eee eS

ini. ashe bance SEP

Bares

#0. Zo 26. PB Ah nl DOADE HS? Jot 4D ne $B. {EAD} % cM Bo bt DB. Ro BNSTBLQ, 1B) 6. FRO AL...) 2S Ms xl 1.27. IN. BBE on IY TT [Poo slo T hue 2 IO.

a acc eA wae ae ear sic eh ee Te RL ah eee eee ae
Fetlbnerdrecad frresyariesre- Qala arrsrte Arar amare ir

Beek Taree cn aa ane rer a

Cat moon
1a)

Z Lab — Network Examination with Wireshark
— Learn how to use Wireshark and how computers encapsulate and send data.
a
Perform the instructions in lab document Net-02-L1.


### Textbook — strona 56

Section 6: ARP and Encapsulation
If a device wants to communicate with another device on the same LAN, it must
encapsulate the MAC address of the destination device.
To get the MAC address, it uses a protocol called ARP (Address Resolution Protocol),
that resolves a logical address (IP) to a physical address (MAC), and saves the results in
the host ARP cache.
ARP operates in Layers 2 and 3 of the OSI model.
Every Layer 3 device uses ARP.
Note: Switches make forwarding decisions based on the physical address of the frame.
ARP Process
Scenario: Host A wants to communicate with host B. Host A knows host B’s IP address
but not its MAC address.
Step 1 - Host A sends an ARP Request to all hosts on the network (Broadcast), with
Host B’s IP as the destination MAC, requesting its MAC address.
Step 2 - The switch forwards the ARP request to all ports.
Step 3 - Host B recognizes the IP address in the request, so it performs an ARP reply, in
which it lists its own MAC address.
Step 4 - Host A receives the ARP reply and saves host B’s MAC address in the ARP cache,
together with Host B’s corresponding IP address.


### Textbook — strona 57

ll Es
v,
&. 5 wy neg
& > z - 5 %
GY
qt Ml
fo \ fo \ TT mn
ARP Table:
Host IP MAC
[8 | 10002 | ewe |
ARP Process

ARP Table (Cache)
Command: arp -a
The ARP table or cache is stored in the RAM of the device.
The ARP contains three parameters:
* Destination host IP
* Corresponding MAC of that host
* Entry source MAC learned automatically or manually
arp —a and arp —g display the host ARP table.
Show arp displays a Cisco device ARP table.
Example:

C:\Windows\system32>arp -a 7

Interface: 10.71.0.110 --- x17

Internet Address Physical Address Type
Q ®.100 90-7c-ac-a9-a2-c9 dvnami


### Textbook — strona 58

Additional ARP Commands
arp —d deletes the host ARP table.
arp —s adds a static entry to the ARP table that resolves to a specific IP address.
Note: Static ARP helps reduce the risk of ARP spoofing attacks.
arp inet_addr defines a specific IP address.
arp eth_addr defines a specific MAC address.
Examples:

C:\Windows\system32>arp -d

C:\Windows\system32>arp -s 10.0.0.2 @0-aa-bb-11-22-33
Data Encapsulation
When a message is sent from source to destination, it must have a specific format or
structure. Message formats depend on the type of message and the channel used to
deliver it.
The opposite process of encapsulation is called decapsulation. This is when the host is
on the receiving side.
The same process occurs in OSI and TCP/IP using the same protocols.
For example, to send mail, we place a message in an envelope — encapsulation. The
envelope is written in a format the mail service accepts and is sent to the destination.
The receiving side opens the envelope and takes out the message — decapsulation.
Note: The envelope is similar to a network frame.
Terminology
Headers and Trailers - Headers and trailers represent control data added by protocols
to the beginning and end of each data unit, in each layer.
For example, IP packages the logical source and destination address in an IPv4 header,
and adds it to the data unit in the Network Layer.


### Textbook — strona 59

Encapsulation - Adding Headers and Trailers to data is called encapsulation. Processing
them and removing them is called decapsulation.
Depending on the communication type, protocols in each layer add the correct header
to the data unit.
PDU - Protocol Data Unit is a piece of information added to or removed from the first 4
layers of the OSI model and the first 3 layers of the TCP/IP model.
PDU consists of protocol-specific control information and user data.
Examples are segments, packets, and frames.
Encapsulation Process
As an example, we can focus on the process of sending data. The first step in the
process is ... YOU!
When you click on a link:
The Application layer creates an HTTP header requesting the web page from the server.
The Presentation layer encodes, encrypts, or compresses the data traveling down from
the Application layer, if necessary. For example, it may convert text to a binary string.
The Session layer determines the direction of the data, one-way or two-way, and
whether the connection is secure or not.
In addition, a session ID is assigned to the connection.
The Transport layer adds a header containing the source and destination logical ports,
and other control information.
This layer also divides data from upper layers into smaller pieces called Segments. Each
segment is a maximum (MSS) of 1460 bytes.


### Textbook — strona 60

Data
HTTP GET
Data
0101101010101010
Data
0101101010101010 Thisis‘alled’a
TCP Header Payload
0101101010101010
Encapsulation in Layers 4 to 7
The Network Layer adds a header to the segment with the IP source and destination
addresses, and other control information (such as TTL). During this step, the segment is
encapsulated in a packet.
Packets are limited to a maximum size (MTU — Maximum Transmission Unit) of 1500
bytes without fragmentation. This excludes the 18 bytes of overhead that are used for
the frame’s header and FCC.
The Data Layer adds a Header and Trailer to the Packet. The header contains the
physical source and destination addresses. The trailer, also called FCS, is for frame error
checking only.
The Physical layer accurately transmits the Frames along with the physical medium.
For example, it sends electric pulses over an Ethernet cable, or wireless radio waves.


### Textbook — strona 61

Packet
IP Header TCP Header Payload
Ethernet Header IP Header TCP Header ~ FCS
> IU
Encapsulation in Layers 1 to 3


# Chapter 3: Switch and IOS Fundamentals


### Textbook — strona 62

| Chapter 3: Switch and IOS Fundamentals
Section 1: Switch Fundamentals
Switches are smart Layer 2 devices with many ports designed to forward frames from
source to destination, according to specific MAC addresses in the frame (Data-Link
Layer). They include multiple technologies, providing various capabilities.
Switches were developed to forward frames in accordance with their destination
addresses and MAC tables (CAM tables), using a MAC learning process known as
forwarding decision.
MAC Tables
The following command is used to display the MAC address table is in Cisco devices:
show mac-address-table
MAC address tables include the following columns:
- VLAN
- MAC address
- Dynamic or Static
- Associated physical ports
DYNAMIC is when a frame with a source MAC arrives at a switch, and the table is
updated with the device MAC address for that port.
STATIC indicates a manually configured MAC address on a switch.
MAC Table Example:
Switch#show mac-address-table
Mac Address Table
Vlan Mac Address Type Ports
1 0001.97d7.45c3 DYNAMIC Fa@/5
1 0004.9a3d.bbc6 DYNAMIC FaQ/4
1 00@c.8500.13bb DYNAMIC Fa@/3
1 00@d@.978c.5698 DYNAMIC Fa@/2


### Textbook — strona 63

Switching Methods
Another important thing about switches is that they have different methods of
receiving and transmitting frames on the LAN.
The following switching methods are used:

= Store-and-Forward

= Cut-through

= Fragment-free
Store-and-Forward
A switch using the Store-and-Forward method buffers the entire frame upon receipt.
This enables the switch to support various port speeds. For example, a frame received
ona 100 Mb/s ingress port can be transmitted via a 1 Gb/s egress port.
Another advantage of this method is error checking, which can be done once the entire
frame is buffered. The switch can easily detect frame errors using the FCS field.
Although Store-and-Forward is relatively slow, it does provide error checking and
support for different speeds across multiple ports.
The buffer is a memory space used for storing some data before performing an action
on it. Frame buffering is the process of storing a frame in memory temporarily before it
is moved to the next destination.
Cut-Through
Cut-through switching is a much faster method than Store-and-Forward. In this method,
only the first 6 bytes of the incoming frame are buffered, meaning the switch only
regards the destination MAC address of the frame.
The switch forwards the frame immediately, even before the entire frame is received,
and no error checking is done.
Note: Modern switches can buffer up to 14 bytes of the beginning of a frame, before
deciding what to do with it.
Although the advantage of Cut-through is its speed, a significant disadvantage is that
some frames that reach the destination host may be corrupted due to lack of error
checking.


### Textbook — strona 64

Fragment-Free
Fragment-free is a more advanced method of switching.
This method buffers the first 64 bytes of the frame, including MAC address data and the
frame’s payload. The technique provides faster switching than Store-and-Forward while
also performing partial error checking to make sure there is no fragmentation on the
first 64 bytes of the frame.
Fragment-free is therefore a better choice for switching since it is faster than Store-and-
Forward and provides partial error checking, unlike Cut-through.
Communication
Half Duplex - A connection for which the communication is restricted to exchanging
data in one direction at a time. For example, a walkie-talkie is a half-duplex device
because only one person can talk at a time.
Full Duplex - Full duplex means that data can be transmitted in both directions, ona
signal carrier, at the same time.
For example, a telephone is a full-duplex device because both users can talk at once.
Half Duplex
SSS
s) s)
re Full Duplex re
EEE
—> Ss


### Textbook — strona 65

Port Speed

Switch ports are typically able to transfer traffic at speeds of 1OMbps, 100Mbps, or

1000Mbps.

The default is for the switch port to auto-configure its speed based on signaling

between the port and the connected device.

There are switches that can transfer traffic at 10 Gbps, or even 40 Gbps.

Auto-Negotiation

Auto-negotiation tells connected devices to announce their capabilities, and then,

based on the settings of the interconnected device at the other end, chooses the

optimal speed and duplex mode.

If one of the devices is configured with a different mode, a duplex mismatch will occur.


### Textbook — strona 66

Section 2: The Cisco IOS
Every network device, such as a switch or a router, has an operating system that tells it
how to forward packets and execute network operations.
An operating system for a device is known as a Network Operating System (NOS).
NOS does not operate the same way as PC and server operating systems.
Internetworking Operation System (IOS) is a CLI-based system, and users interface with
it using Cisco text-based commands.
Most Cisco devices, regardless of their size or type, run the IOS, which is an advantage
due its singularity and familiarity.
While all devices come with a default IOS and feature set, it is possible to upgrade the
IOS version or feature set to obtain additional capabilities.
The versions of the IOS may be different, depending on the device hardware.
This course focuses on versions 12 and 15.
10S Interface Features
CLI - IOS uses a command line interface (CLI) to enable administrators and technicians
to interact with the system via special Cisco commands.
CLI is a means of interacting with programs by entering commands in a command line.
Using a CLI-based system has many advantages, such as minimum resource usage,
faster ability to operate in the system, and others.
Terminal Emulation - Many network devices are configured and managed using
Terminal Emulation software, such as PuTTY. TE programs enable the configuration of
local devices using a serial cable or a remote management protocol, such as SSH.


### Textbook — strona 67

Terminal Software
PuTTY — PuTTY is a very versatile tool for remote access to another computer. It is often
used by people who want secure remote shell access to UNIX or Linux systems, though
that is only one of its many uses.
Category:
Leeeeeaee Specify the destination you want to connectio
| Keyboard Host Name (orlP address) Port
eee p2
es Raia, Connection type:
+ ‘Apaeatenee’ CRaw ©Telnet CRiogn @SSH COSerial
Behaviour Load, save or delete a stored session
rf apo ‘Saved Sessions
i §-Colours
Ei Gommecton [Detauesetngs da
Fs
Tenet Ean
Rlegin Delete
SSH
Serial
Close window on exit:
CAways (Never = @Only onclean exit
= Hep cam
Tera Term — Tera Term is an open-source, free, software-based terminal emulator
(communication) program. It emulates different types of computer terminals, from DEC
VT100 to DEC VT382, and supports telnet, SSH 1 and 2, and serial port connections.
SecureCRT — SecureCRT is a commercial SSH and Telnet client and terminal emulator by
VanDyke Software. Originally a Windows product, VanDyke recently added Mac OS X
and Linux versions.
Access Methods
Out-of-Band - This method uses a dedicated management console cable that must be
physically connected to the device. Initial configuration is usually done using this
method.
In-Band - This method uses management protocols, such as SSH or Telnet, which access
the device remotely over the network.


### Textbook — strona 68

Qut-of-Band Management
Out-of-Band management requires two main items:
© PC with terminal software
¢ Console cable
Terminal - A network device is like a PC, but without a mouse, keyboard, or screen. PC
with a terminal provides a way to input commands and view output from the device.
Console Cable - A console cable or management cable is like a bridge between the PC
and the device. Almost every device has a designated console cable for this purpose.
Older cables use an RS232 connector, while modern ones use USB.
10S Modes
IOS can operate in one of three work modes, each with different capabilities and
permissions. For example, one mode may have a lower level of privileges compared
with another mode.
The division of modes is meant to separate the management levels and increase the
efficiency of network device security and configuration.
Cisco OS modes have a hierarchical structure and are similar among switches and
routers.
User EXEC Mode
This mode has low-level capabilities but is useful for basic operations. It has a limited
amount of monitoring commands, but does not allow any device configuration changes.
Privilege EXEC Mode
This mode has a large number of monitoring commands and device configuration
viewing commands (Show commands). It also enables file management operations,
such as device configuration backup, and IOS upgrade.


### Textbook — strona 69

Global Configuration Mode
Global configuration is the only mode that allows administrators to change device
configuration. This mode is only accessible from the Privilege EXEC mode.
Mode Navigation
Navigating the system and understanding the differences among the modes is
important when working in the system.
The default display name of a device appears before the prompt. In the example on
below, the name is Switch.
The enable command moves the user from User mode to Privilege mode.
The configure terminal command moves the user from User mode to Global
configuration mode.
The exit command takes the user one mode back.
Example:

Switch>enable

Switch#configure terminal

Enter configuration commands, one per line. End with CNTL/Z.

Switch(config)#exit

Switch#exit

Switch>
10S Error Messages
Incomplete Command - The command is correct, but not complete.
Ambiguous Command - Not enough characters were entered for the command to be
recognized. Or, more than one command exists with the same name.
Invalid Input - The command was entered incorrectly (i.e. typo) or inserted in the
wrong mode.


### Textbook — strona 70

Example:

Switch>di

% Ambiguous command: "di"

Switch#show

%Incomplete Command.

Switch(config)#hostnme S1

A

% Invalid input detected at '*' marker.
Hotkeys and Shortcuts
TAB - Completes a partial entry.
CTRL + D - Erases the character at the cursor.
CTRL + K - Erases all characters from the cursor to the end of the command line.
ESC + D - Erases all characters from the cursor to the end of the word.
CTRL + Shift + 6 - Break sequence used to abort DNS lookups, traceroutes, pings, etc.
CTRL + W - Erases the word to the left of the cursor.
CTRL + P - Recalls a command from the history buffer.
CTRL + Z - Ends Configuration mode and returns to Privileged EXEC mode.
Cisco Device Components
RAM - Volatile memory that stores the system configuration (running-config) and
tables (such as the MAC table).
ROM — Non-volatile memory responsible for the POST (Power-On Self-Test) process and
bootstrap, which is the initial program that is responsible for booting the IOS.
Flash — Non-volatile memory that stores the operating system itself (IOS).
NVRAM — Non-volatile memory that stores the startup config file.


### Textbook — strona 71

Device Boot Process
1 - POST (Power-On Self-Test) and bootstrap program load — This part of the sequence
checks the CPU, RAM, and NVRAM. When done, the device copies the bootstrap
program from the ROM to the RAM.
2 - Load IOS — After copying the bootstrap program from the ROM to the RAM, the IOS
(which is still stored in flash memory) is copied to the RAM for execution.
3 - Load Configuration — The bootstrap program now copies the startup configuration
file from the NVRAM to the RAM.


### Textbook — strona 72

Section 3: Initial Device Configuration Commands
Device Name
This command sets the local network device name. For example, S-Floor1.
Command:
hostname <device name>
Example:
Switch(config)#hostname S1-Floor1
S1-Floor1(config)#
Create User Account
Creates a Local User Account on the device.
Command:
username <user-name> password <password>
Example:
Switch(config)#username Admin password p@nd@
Switch(config)#username Peter password Spiderm@n


### Textbook — strona 73

Secure Privileged Mode
Enables password authentication when accessing the Privileged EXEC mode.
Command:
enable password <password>
Example:
Switch(config)#enable password c!sc@
Security Message
Displays a security message each time a user logs in to the system.
Command:
banner motd #security-massage#
Example:
Switch(config)#banner motd #Access to this device is for
authorized personnel only!#
Encrypt Passwords
Configured passwords appear in plain text in the configuration file.
The command encrypts all plain text passwords, using the Cisco Type 7 method.
Command:
service password-encryption
Example:
Switch(config)#service password-encryption


### Textbook — strona 74

Save Device Configuration
Copies the device configuration from the RAM to the NVRAM (non-volatile memory).
If the configuration isn’t saved to the NVRAM, all of the configurations that were
performed will be lost.
Command:
copy running-config startup-config
Example:
Secure Console Access
Two steps are performed to enable local credential (username & password)
authentication on the console port.
1. Enter the Console port config mode (Line mode).
2. Enter the local login and exit.
Note: Besides the local login command, there is a login command that enables only
password checking.
Command:
line console 0 & login local
Example:
Switch(config-line)#login local
Switch(config-line)#exit


### Textbook — strona 75

Verify Configuration
All configuration changes are immediately saved in the running-config file.
To display them, run the show running-config or show run command.
Note: The example below is a brief glimpse of the actual file.
Example:
$1-Floorl#show running-config
Building configuration...
Current configuration : 1234 bytes
!
version 12.2
service password-encryption
!
hostname S1-Floor1
!
enable password 7 9822@D5D@A49
!
username Admin privilege 1 password 7 @8316C4@@D39
!
banner motd “CAccess to this device is for authorized personnel only!
!
line con @
login local
b Lab — Initial Cisco Device Configuration
—J | Learn to connect to and access the device IOS using the out-of-band
=== =| management method.
Understand how to work in the different Cisco IOS modes.
Understand and practice Cisco IOS commands used to configure a network
device for the first time, focusing on switch settings.
Perform the instructions in lab document Net-03-L1.


### Textbook — strona 76

Section 4: Additional IOS Protocols and Commands
TFTP
TFTP (Trivial File Transfer Protocol) is a simple lock-step file transfer protocol that
allows clients to retrieve files from or transfer files to a remote host.
TFTP can also be used to remotely start a computer, back up network or router
configuration files, and upgrade a device’s IOS.
TFTP relies on UDP to transport data, and uses port 69.
Back Up Device Configuration
This process copies the running-configuration file to a remote TFTP server. This is very
useful for when a disaster occurs, and a quick restoration of settings is required.
Command:

copy running-config tftp
Example:
Backup using TFTP
Note: First save the configuration locally, using:

copy running-config startup-config
Step 1 — Copy the file to the server.
Step 2 — Enter the TFTP server IP address.
Step 3 — Select the name of the file saved on the server.
Backing up the IOS file is almost the same. You only need to replace the source location
of the file, meaning flash: instead of running-config.


### Textbook — strona 77

Example:
Sl#copy running-config tftp:
Address or name of remote host []? 192.168.1.3
Destination filename [R1-confg]? R1-config-backup20.9
Writing running-config....!!
[OK - 1362 bytes]
10S Upgrade
Step 1—The command copy tftp: flash: is used to copy the new IOS file from a TFTP
server to the flash memory.
Step 2 - Upgrading the device can be performed after copying the new IOS to the
device, using the boot system command. This command tells the device which IOS file
to load upon the next startup.
Step 3 — The command copy running-config startup-config is used to save current
configuration to the startup configuration, and reload the device to enable the new IOS
to load.
Example:
Sl1#copy tftp: flash:
Address or name of remote host []? 192.168.1.3
Source filename []? c1901-imoversa;19.mz.SPA.152-4.M3.bin
Destination filename [c1901-imoversa;19.mz.SPA.152-4.M3.bin]?
Accessing tftp://192.168.1.3/ c1901-imoversa;19.mz.SPA.152-4.M3.bin...
Loading c1901-imoversa;19.mz.SPA.152-4.M3.bin from 192.168.1.3:
PEEPEPPPPP rb err repre rrr errr errr rrr errr err rere errr rrr errr errr rrr
[OK - 4670455 bytes]
S1# Configuration terminal
S1(config)#boot system flash®://c1901-imoversa;19.mz.SPA.152-4.M3.bin
S1(config)# exit
S1#copy running-config startup-config
Sl#reload


### Textbook — strona 78

ROMmon
The purpose of the ROMmon (Read Only Memory MONitor) configuration register is to
change the router’s behavior in several ways:

© Determine how the router will boot.

e Apply options while booting (such as ignore configuration).

e Set the console speed and band rate for terminal emulation sessions.
Configure Register Value
In the Configuration terminal mode, we can change the register value, which will affect
the next boot process.
In the example below, the register value is changed to the default 0x2102, and the
configuration is saved in startup config, which will revert the settings to the factory
default.
Example:

Router(config)# config-register @x2102

Router(config)# end

Router# copy running-config startup-config

Destination filename [startup-config]?

Building configuration

[OK]

Router# Reload


### Textbook — strona 79

ROMmon Register Value
The default configuration register is Ox2102, which can be verified using the show
version command.
Use the configreg command to change the register value and the router’s behavior.
Common Settings
Register Value Device Behavior
- Ignores break key
0x102 - 9600 console baud rate (maximum transfer rate of the
console port in bits per second, in this case 9600 bits per
second)
0x1202 - 1200 baud rate
- Boots into bootstrap
- Ignores break key
0x2101
- Boots into ROM if initial boot fails
- 9600 console baud rate
- Default register value
- Boots into ROM if initial boot fails
0x2102
- 9600 console baud rate default value for most
platforms


### Textbook — strona 80

Section 5: Verifying Configured Register Value
By entering the show version command, we can verify the configured register value.
We can also display additional information, such as the software type and version.
Example:

Router#show version

<output omitted>

Cisco I0S Software, 1841 Software (C1841-IPBASEK9-M), Version 12.4(12),

RELEASE SOFTWARE (fc1)

Technical Support: http://www.cisco.com/techsupport

Copyright (c) 1986-2006 by Cisco Systems, Inc.

Compiled Mon 15-May-@6 14:54 by pt_team

ROM: System Bootstrap, Version 12.3(8r)T8, RELEASE SOFTWARE (fc1)

System returned to ROM by power-on

System image file is "flash:c1841-ipbasek9-mz.124-12.bin"

Cisco 1841 (revision 5.0) with 114688K/16384K bytes of memory.

Processor board ID FTX@947Z18E

M86® processor: part number @, mask 49

2 FastEthernet/IEEE 802.3 interface(s)

191K bytes of NVRAM.

63488K bytes of ATA CompactFlash (Read/Write)

Configuration register is @x2102

: Lab — Backing Up Config Files and Managing the IOS
= | Practice configuration file backup and device operating system upgrade via
— a remote TFTP server.
Perform the instructions in lab document Net-03-L2.


# Chapter 4: Switch Security


### Textbook — strona 81

| Chapter 4: Switch Security
Section 1: Port Security
The Port Security feature is used to restrict input to an interface by limiting MAC
addresses of workstations that are allowed to access a specific port.
When secure MAC addresses are assigned to a port, the port will not forward packets
with source addresses outside the defined group.
By default, port security is not defined on switches and requires configuration.
Switched Environment Risks
MAC Spoofing
MAC spoofing is when attackers change their own physical PC address to conceal their
true identity and pose as someone else. For example, an attacker may spoof a MAC
address with a legitimate address to bypass an access control mechanism, such as port
security.
CAM Table Overflow
CAM Table Overflow is an attack that targets a switch’s MAC table. The idea is to flood
the table with a large number of fake addresses. When the list of addresses exceeds the
maximum size of the table, the switch will initiate its fallback mode and begin to act as
a hub, meaning every frame will be forwarded to every host on the network.
Violation Modes
The port security feature includes three protection modes to handle incidents in which
it receives an Ethernet frame with an unauthorized MAC address.
Shutdown - This is the default violation mode. When a violation occurs, the port will be
shut down, and the violation will be logged automatically. The port must then be reset
manually to become operational again.


### Textbook — strona 82

Restrict - In case of a violation, Ethernet frames with unauthorized source MAC
addresses are dropped. The switch provides notification of security violations and keeps
count of the number of violations.
Protect - In case of a violation, Ethernet frames with unauthorized source MAC
addresses are dropped. In this violation mode, the switch does not provide notification
regarding the event.
Address Learning — Manual vs. Sticky
MAC address learning can be performed in one of two ways: Manual or Sticky.
Manual - The manual method requires a static configuration of each allowed MAC
address and its assignment to an interface. This is the most secure method, but it is very
time consuming and open to faulty configuration.
Sticky - In the sticky method, allowed MAC addresses are learned dynamically and are
limited to the maximum number configured for the interface. The switch learns the
source address of the first few devices associated with the interface, providing a fast
and scalable method of operation.
Max and Err-Disabled
Max Allowed MAC Addresses
Although the number of default MAC addresses allowed in Port Security is one, the
number can be changed within the range of 1 to 3072.
Err-Disabled
When a switch port is in Err-disabled mode, the port may have been disabled
automatically by the switch operating system, due to port security shutdown mode
violation.
To determine if Err-disabled was turned off for a port, run the command:
show interfaces [interface] status

Example:

Switch# show interfaces fastEthernet 0/1 status

Port Status

Fa@/1 err-disabled

rage oo


### Textbook — strona 83

Common Reasons for err-disable

Err-disabled may be triggered due to reasons other than Port Security, such as:

e Duplex Mismatch - This state occurs when two parties, set for point-to-point
communication, are configured to use different duplex modes.

e Bad NIC - A faulty network interface card with software problems or hardware
problems may trigger the Err-disabled state.

e Broadcast Storm - When there is a broadcast volume too large for processing in the
broadcast domain, the switches may be overwhelmed and trigger err-disabled
mode on its ports.

Port Security Requirements

Access Mode
Access ports are responsible for traffic flow.
Access mode should only be defined on ports connected to endpoint devices, such as

PCs.

You can configure port security on interfaces that you configured as access ports with
access mode activated.

Enable Port Security

Enabling port security is done in the interface configuration mode, which is set using

interface [interface-id]. Then, Access mode needs to be set with switchport mode

access.

Note: For port security to operate correctly, the interface must be configured as an

Access port.
Finally, Port Security can be enabled on the interface using the command:
switchport port-security


### Textbook — strona 84

Commands:
switchport mode access
switchport port-security
Example:
Switch(config)# interface fastEthernet @/1
Switch(config-if)# switchport mode access
Switch(config-if)# switchport port-security
Switch(config-if)#
Port Security Configuration
Port Security is configured by setting up each component individually using the same
structure.
Violation defines the type of violation rule to be applied to the port.
The commands mac-address and maximum define sticky learning, up to a maximum of
five addresses.
Command:
switchport port-security [configuration] [value]
Example:
Switch(config)# interface fastEthernet 0/1
Switch(config-if)# switchport mode access
Switch(config-if)# switchport port-security
2 A A A KK KK Ke 2 ee 2 2 2 2 2 2K 2K 2K 2K 2K 2 2K 2K 2 2K 2 2K 2 2K 2K 2K OK OK OK OK OK OK OK OK OK OK OK KKK KK KK
Switch(config-if)# switchport port-security violation restrict
Switch(config-if)# switchport port-security mac-address sticky
Switch(config-if)# switchport port-security maximum 5


### Textbook — strona 85

Port Security Show Commands
Presenting the authorized MAC addresses associated with a port and the type (sticky or
manually) is done with the command show port-security address.
If only an overview is needed, show port-security can be run for a quick overview of the
configuration.
To view a specific interface, the command show port-security interface [interface]
should be used, since it provides more information.
Example:
Switch# show port-security
Secure Port MaxSecureAddr CurrentAddr SecurityViolation Security Action
(Count) (Count) (Count)
Fae@/1 5 a (7) Restrict
Fae/2 1 (2) (2) Shutdown
Switch# show port-security address
Secure Mac Address Table
Vlan Mac Address Type Ports Remaining Age
(mins)
a @002.1798.DAC6 SecureSticky FastEthernet0/1 -
1 Q090.2172.8736 DynamicConfigured FastEthernet0/2 -
Total Addresses in System (excluding one mac per port) : @
Max Addresses limit in System (excluding one mac per port) : 1024
é Lab — Configure and Verify Port Security
=, Implement Port Security on a switch, practice using Port Security options,
= | and learn how to verify settings.
Perform the instructions in lab document Net-04-L1.


### Textbook — strona 86

Section 2: Remote Access
Today, other than for initial configuration, most access to deployed switches is done
remotely.
Remote access allows administrators to manage and monitor their network devices
from anywhere in the network.
This is important since some switches may be located in physically inaccessible areas.
Telnet vs. SSH
Telnet and SSH are the two most widely used CLI-based remote access protocols.
Telnet - Telnet was developed many years ago to allow users to manage devices from
anywhere, via a simple and minimal configuration. However, using Telnet involves a
potential security risk because usernames and passwords are sent in plain text on TCP
port 23.
SSH - SSH is similar to Telnet, but with a significant difference: SSH encrypts all data
transferred between the user and end device. SSH uses RSA encryption, a robust and
reliable encryption type. It operates on TCP port 22.
SSH Encryption
Modern encryption relies heavily on the RSA algorithm since most methods use public
and private encryption keys.
The public and private encryption key method, also known as asymmetric cryptography,
uses two different, but mathematically linked keys.
The public key is shared with everyone, while the private key is only given to specific
persons.
RSA ensures implementation of the CIA triangle, and avoids authentication rejection.
Protocols like SSH and SSL/TLS use RSA to encrypt communication and digital
signatures.
Although RSA works through the computational difficulty of factoring large integers,
computational complexity grows exponentially every day, and larger and larger
numbers are required to maintain secure communication.


### Textbook — strona 87

RSA is dependent on a powerful computational system. More complex keys require
more computation.
Recently, ECC (Elliptic Curve Cryptography) is becoming popular, since it can create
faster, smaller, and more efficient cryptographic keys.
Asymmetric Encryption
Asymmetric encryption is when two different keys are used to encrypt and decrypt
messages.
The keys are mathematically related in a way that messages encrypted with one key,
usually the public key, cannot be decrypted by it. The decryption can be done only using
the corresponding private key in the key pair.
This method is considered more complex and slower than symmetric encryption which
uses one key for both encryption and decryption.
Public key
a
of fo Decryption ap
ee SEE Sanaa!
[se] Encryption [ieee] Q cor
Private key
————— EEE
Data transfer
42222 noo ee een ---------
P Key publicly available —_
Encryption-Decryption Process


### Textbook — strona 88

Section 3: VTY
Virtual Teletype (VTY) is a command-line interface (CLI) in network devices used to
create remote access connections.
VTY is virtual and does not require any hardware.
Switches have 16 VTY lines (0-15), routers have 5 VTY lines (0-4).
Section 4: SVI (Switched Virtual Interface)
The primary purpose of creating a computer network is to share resources and enable
communication within the network.
Layer 2 switches create VLANs (Virtual LANs) that form a single broadcast domain. If a
broadcast message is sent within the same VLAN, all devices connected to that VLAN
will receive the message.
Hosts can communicate on the same VLAN without a Layer 3 device (router). Devices
on a different VLAN, on the other hand, cannot communicate with each other without
proper routing.
A router or Layer 3 switch can handle network segmentation and inter-VLAN
communication. A router can segment a network and create separate broadcast
domains, with each network segment using a different sub-interface of a physical
interface on the router.
Layer 3 switches require the creation of multiple VLANs on the switch, which form
multiple broadcast domains. Then, for each VLAN, a corresponding Layer 3 interface
needs to be created on the switch, to handle the routing. This Layer 3 interface is the
SVI. The difference is that the SVI Layer 3 interface is virtual.


### Textbook — strona 89

Section 5: SSH Configuration
Before establishing an SSH session, several items need to be configured, as follows:
© Change the default hostname.
© Create a user account.
e Set the enable password.
© Configure a domain name.
e Seta security message.
e Enable VTY lines and limit protocol access.
e Enable Layer 3 connectivity.
e Generate SSH keys.
SSH Prerequisites
Several initial settings must be configured before enabling SSH on the device.
1. Set the device name.
2. Create a local account.
3. Secure the privileged mode.
4. Set an appropriate security message (optional).
5. Set a domain name.
Example:
S1(config)#username Admin password p@nd@
S1(config)#enable password c!sc@
S1(config)#service password-encryption
S1(config)#banner motd #Access to this device is for
authorized personnel only!#
S1(config)#ip domain-name CyberPro.com


### Textbook — strona 90

SSH Configuration Commands
Allow Remote Access
Step 1 - Enter the VTY configuration mode. Select the number of maximum sessions.
Step 2 - Enable authentication using a username and password.
Step 3 - Telnet is enabled by default; the transport command prevents using Telnet and
only uses SSH for remote connections. The options are none, all, Telnet, or SSH.
Command:
line vty <id-range> & login local

Example:

S1(config)#line vty @ 15

S1(config-line)#login local

S1(config-line)#transport input ssh

S1(config-line)#exit
IP Switch Settings
The default SVI is VLAN 1. Setting an address and enabling the interface is crucial if we
want to communicate directly with the switch. If the switch needs to send data to other
networks, the default gateway is also required.
Command:

Interface vian 1 & ip address <ip-address> < subnet-mast>

Example:

S1(config)#interface vlan 1

S1(config-if)#ip address 10.0.0.150 255.255.255.080

S1(config-if)#no shutdown

S1(config-if)#exit

S1(config)#ip default-gateway 10.0.0.1


### Textbook — strona 91

Generate RSA Keys
The crypto key command generates the Private and Public RSA keys on the network
device. The switch or router needs those keys to secure the SSH session.
Set the key length. The default is 512, but it is recommended to set the number of bits
to higher than 1024. The maximum value is 2048.
Command:
crypto key generate rsa
Example:
S1(config)#crypto key generate rsa
The name for the keys will be: S1.CyberPro.com
Choose the size of the key modulus in the range of 360 to 2048 for your
General Purpose Keys. Choosing a key modulus greater than 512 may take
a few minutes.
How many bits in the modulus [512]: 1024
% Generating 1024 bit RSA keys, keys will be non-exportable...[0OK]
Verify SSH Configuration
Show ssh command presents the active SSH sessions on the network device.
Show ip ssh displays the version definition, authentication timeout, and retries.
Example:
S1#show ssh
Connection Version Mode Encryption Hmac State Username
2 1.99 IN aes128-cbc hmac-shal Session Started Admin
2 1.99, OUT aesi128-cbc hmac-shal Session Started Admin
%No SSHv1 server connections running.
S1#show ip ssh
SSH Enabled - version 2.0
Authentication timeout: 12@ secs; Authentication retries: 3


### Textbook — strona 92

SSH Connection
Accessing the device remotely using SSH can be done using a CLI, such as PuTTY or the
device’s terminal.
The universal command for creating an SSH session is:
ssh -I <username> <target-ip>
In the following example, the command is executed in Windows CMD.
GEE Administrator: Command Prompt - ssh -| root 192.168.137.129
Microsoft Windows [Version 10.0.18362.239]
(c) 2019 Microsoft Corporation. All rights reserved.
iC: \Windows\system32>ssh -1 root 192.168.137.129
Iroot@192.168.137.129's password
hk
Lab — Remote Access with SSH
— Set up the SSH service on network devices for remote management from
mm | anywhere on the network, and practice configuring IP connectivity to a
Layer 2 switch using the In-Band Management method.
Perform the instructions in lab document Net-04-L2.


# Chapter 5: IP and Routing Concepts


### Textbook — strona 93

| Chapter 5: IP and Routing Concepts
In a network, IP addresses are used to identify a device’s source and destination.
It is important to understand routers, how they work, their processes, and the logic
involved in IPv4 and IPv6 configuration.
Section 1: Number Systems
Decimal - The most common numbering system consists of ten numbers, 0-9, and it is
called the decimal system. The system is based on the 10 fingers we use to count and is
known as the base-10 numeral system.
Binary - Binary is an alternative number system that consists of only two numbers: 0
and 1. This system is used by computers, which communicate by modulating electrical
currents. Because there are only two numbers, the system is known as the base-2
numeral system.
Hexadecimal - Hex, or Hexadecimal, is a number system that consists of 16 characters
and is known as the base-16 numeral system. Hex uses the numbers 0-9, followed by
the letters A-F. Hex is widely used as an alternative representation to binary, since it is a
more human-oriented system.
Positional Notation
When learning about number systems, a good way to approach them is to consider
numbers a result of their positions.
Each number’s value can be calculated as a result of a function.
The function is the same regardless of the base being used, making it easier to perform
base transitions.
The function is: [number] = [digit] * [base] “ [position].


### Textbook — strona 94

The Digits: 1 (2) 1. 1
02 The Positions: 2 22 21 2°
Base2 The Result: 8 (2) 2 1
The Digits: 1 (2) 2 4
10 The Positions: 103 102 10 16!
Base10 The Result: 1000 @ 20 4
The Digits: B a. (2) 5
16 The Positions: 16 162, 161 16°
Basel6 The Result: 45056 256 2) 5
Positional Conversion
Binary to Decimal
After the Positional Notation method is used to map a number’s value, the positional
value of each digit can be found. The next step is conversion, summarizing each of the
individual values to get the result.
Conversion Formula:
Positional Value 128 64 32 16 8 4 2 1
Binary value 1 i 0 1 0 1 0 0
Calculation 1x128 1x64 0x32 1x16 Ox8. 1x4 Ox2 Ox1
Final Value 128 64 0 16 0 4 0 i)
Decimal value of 128+64+0+16+0+4+0+0-212
the binary value Eres]


### Textbook — strona 95

Decimal to Binary
While the aim of conversion to decimal is to solve a formula, the aim of conversion
from decimal is to find the missing variable.
The operation can be summed up as find the X that will result in the closest number.
For example, when converting the number 1994 to binary, the first step is to find X,
where 2* is the closest to 1994.
Continuing this process, the number should be written down and the calculation should
be repeated for the remainder.
1994 : 120
1024 8
970 2
512 2
458 ) (4)
256
— 32 16 8 4 2 1
202 4 ——
“4128 0 0 1 0 4: 0
74 Z +
= 2048 1024 512 256 128 64
64
10 ) 1 1 1 oe 1
Decimal to Binary Positional Conversion
Calculation Tricks
For binary, there are some tricks that can make the calculation easier, instead of having
to guess.
One trick is to take the desired number and divide it, without the remainder, while
recording each operation.
If the result is even, write a O. If it is odd, write a 1. The binary representation will
appear when the operations are done.


### Textbook — strona 96

For other bases, there are other tricks and mathematical methods.
——~ £€£~ -—~ 2 —
62. 124 249 498 $97 1994
— 2 <— —
al 3 . 15 31,
111110010180
Division Calculation
Binary to Hexadecimal
Because 16 is technically 2*, conversion from base-2 to base-16 is rather easy. Each
hexadecimal digit can be considered a representation of 4 binary digits. For example,
101110 is 0010 + 1110, making it 2E in hexadecimal.
Binary to Hexadecimal Conversion Formula:
Number 0 1 2 3 4 5 6 7
Binary 0000 0001 0010 0011 0100 0101 0110 0111
Hexadecimal 0 1 2 | 3 4 | 5 6 | 7
Number 8 9 10 11 12 13 14 15
Binary 1000 1001 1010 1011 1100 1101 1110 1111
Hexadecimal 8 | 9 A | B c | D | E F


### Textbook — strona 97

Hexadecimal Conversion
Here is how binary is converted to hex, with an example.
Conversion steps:
e Divide the binary number into groups of 4 digits.
© Convert each group to its equivalent hex value using the Base Comparison table.
e Merge the results of each group.
Conversion example: Convert 0111111111010100 to Hex
e 0111 1111 1101 0100
e 0111=7,1111 =F, 1101 =D, 0100 =4
e Answer is 7FD4
Other Bases
There are other bases besides binary, decimal, and hexadecimal.
Throughout history, other counting systems, such as base-6, base-8, and base-12 were
developed.
Old British measurements, such as dozen (12), gross (144), and feet (12 inches) are
suspected to have been originated by a base-12 number system.
Most of those bases are no longer in use today.
Z Lab — Converting Decimal, Binary, and Hex
—=/ | Understand numbering systems and how to convert among them.
m=:
Perform the instructions in lab document Net-05-L1.


### Textbook — strona 98

Section 2: The Router
A router is a device designed to receive, forward, and analyze packets transmitted to
and from other devices on a network, and other networks.
Routers enable inter-network communication, and can provide services such ACL and
NAT, which are required in any networking scheme.
A router is a Layer 3 device that communicates using IP addresses.
Default Gateway
The default gateway is a network device that can route traffic to and from other
networks. A router typically fulfills this role.
The default gateway is similar to the door of a room. If the desired object is in another
room, the object can be reached only by exiting the current room and entering the
other room through the door.
If the destination is on the same network, there is no need to pass through the router.
Configuration
Default gateway configuration options are typically located together with other adapter
configuration options.
In Windows, the settings are located under Network & Internet Settings in Change
Adapter Options.
By default, the gateway should be received from the DHCP.
However, if manual IPs were configured, the gateway should also be configured
manually.


### Textbook — strona 99

7 Internet Protocol Version 4 (TCP/IPv4) Properties. x
Networking Shang —
Oroanize* Comet To Disable this el Camect ung 1m @
= bluetooth Nework Connection 1D roe) Duo Berd Wiles A 6260 Bical, Ghee yeumedioas yar evoke
ky TacercinanteSona te Deven sors

©) 8B Fie and Pier Shaing for Microsc Networks =

MB vitustfox NOISE Bridged Networking Onver mags Ee ae 8

& Pinca Pocket Die PCA oefad gator [mao]

A Bla0s Packet Scheduler

Et -hlend Poca Veen 4 TPZ) . —

= = @Use the following ONS server addresses:

ae pees Preferred DNS server: @.8,.8.8]

acme One Racca ema naa Marte seve ed

Wecrreerevok pesca pve commie

play carotene Giddaeniieseared =

a a == ieee
NIC Configuration
Router Interfaces
Fast Ethernet - First made public in 1995. Operates at a speed of 100 Mbps and uses
the media standard 100BaseT.
Gigabit Ethernet - Introduced in 1999. Supports a faster speed of 1000 Mbps, and uses
the media standard 1000BaseT, but can also support 100 Mbps.
Serial Interfaces - Used for long distance transmissions. If two serial ports need to
communicate with each other, they must be synchronized with the same clock
frequency and allocate the necessary bandwidth.
Other Router Interfaces
Console - This is a physical management port, visually similar to Ethernet ports, that
provides out-of-band access to a Cisco device. Out-of-band refers to access via a
dedicated management channel used only for device maintenance.
AUX - (not the one used for audio) The auxiliary port mainly functions as a backup
console port, although it can also be used as a dial-up port for remote management,
and other purposes. The main difference between Console and AUX is that AUX pushes
output to the port after power-up, while a Console does so during the power-up
process itself.


### Textbook — strona 100

Interface Configuration
Router interfaces need to be set up with IP addresses, similar to computer network
interfaces.
The interface [type] [id] command selects the desired interface. To use an interface, it
must be set up with ip address [ip] [subnet mask] and enabled using the no shutdown
command.
Use show ip interface brief to verify interface settings on the router.
1(config)#interface gigabitEthernet 0/0
R1(config-if)#ip address 192.168.0.1 255.255.255.0
R1(config-if)#no shutdown
%LINK-5-CHANGED: Interface GigabitEthernet@/0, changed state to up
R1(config-if)#exit
R1(config)#exit
Rl#show ip interface brief
Interface IP-Address OK? Method Status Protocol
GigabitEthernete/e 192.168.0.1 YES manual up up
Loopback Interface
Loopback is a logical interface that is not assigned to a physical port. The interface can
be used to test and manage Cisco IOS devices, because it ensures that at least one
interface will always be available.
A loopback interface should not be confused with a loopback address.
Configuration
A Loopback Interface is often configured during the initial router configuration, mainly
for testing purposes.
The interface is configured to automatically be ready for operation.
A router can have more than one loopback interface enabled simultaneously, but each
interface must have a unique IP.


### Textbook — strona 101

A loopback interface is created using the command interface loopback <ID> via the
configuration terminal.

Router(config)#interface loopback @

%LINK-5-CHANGED: Interface Loopback®, changed state to up
%LINEPROTO-5-UPDOWN: Line protocol on Interface Loopback®@, changed state
to up

Router(config-if)#ip address 10.10.10.10 255.0.0.0

Router(config-if)#no shutdown

Router(config-if)# exit


### Textbook — strona 102

Section 3: Routing Process
The routing process involves selecting a path for the delivery of packets across different
networks, from source to destination, through Layer 3 devices.
It is important to note that routers can route packets to directly connected networks,
without requiring configuration. However, if the networks are not connected directly to
the router, the route needs to be learned.
Routing decisions are made based on a router’s routing table.
Process Stages
Examination - In the first step, the router decides whether to process a packet or ignore
it. Routers will ignore packets with errors, or packets they don't know how to process.
Decapsulation - The router examines the Layer 2 address to decide if the packet was
intended for itself (the default gateway), and verifies the integrity of the frame using
the FCS (Layer 2 trailer).
Decision-Making - The router decides where to forward the packet to, based on its
destination IP address and the routers routing table.
Encapsulation - The router re-encapsulates the packet with new Layer 2 headers for the
next hop, according to the decision made in step 3.
Forwarding - After a decision is made, the router forwards the packet to the interface
from which the packet must exit to reach its destination.


### Textbook — strona 103

Routing Choices
Same LAN - If the destination IP is on the same LAN as the source device, there is no
need for routing. The frame will get to the destination via the switch.
Known Route - If the destination IP is on a different LAN, but the network device has a
static or dynamic route to the destination IP, it will forward the packet to the next hop,
based on the route.
No Route - If there is no static or dynamic route in the network device’s routing table, it
will forward the packet to its default ‘Gateway of last resort’.
Note that a ‘Gateway of last resort’ is where the router will send packets to if there is
no other known route to which they should be sent.
No Gateway - If there is no ‘Gateway of last resort’ and the destination packet is not
listed, the router will discard the packet.
Routing Table
The Routing Table contains lists of routes to possible network destinations. The table
includes information about the network topology.
The codes on the left side of a route show how the network is learned by the router.
Router# show ip route
Codes: C - connected, S - static, I - IGRP, R - RIP, M - mobile, B - BGP

D - EIGRP, EX - EIGRP external, O - OSPF, IA - OSPF inter area

N1 - OSPF NSSA external type 1, N2 - OSPF NSSA external type 2

El - OSPF external type 1, E2 - OSPF external type 2, E - EGP

i - IS-IS, L1 - IS-IS level-1, L2 - IS-IS level-2, ia - IS-IS inter area

* - candidate default, U - per-user static route, o - ODR

P - periodic downloaded static route
Gateway of last resort is not set

172.16.0.0/16 is variably subnetted, 5 subnets, 2 masks
D 172.16.0.0/16 [90/5376] via 192.168.4.2, 00:02:24, GigabitEthernet4/0e
G 172.16.0.0/24 is directly connected, GigabitEthernet0/0
Ss 172.16.1.0/24 [1/0] via 192.168.1.2
R 172.16.2.0/24 [1260/1] via 192.168.2.2, 00:00:15, GigabitEthernet2/0
10) 172.16.3.0/24 [110/2] via 192.168.3.2, 00:01:26, GigabitEthernet3/@
Cc 192.168.1.0/24 is directly connected, GigabitEthernet1/0
Cc 192.168.2.0/24 is directly connected, GigabitEthernet2/0
Cc 192.168.3.0/24 is directly connected, GigabitEthernet3/0
Cc 192.168.4.0/24 is directly connected, GigabitEthernet4/0


### Textbook — strona 104

Routing Table Codes
Directly-Connected / Local Route - When inspecting the routing table, records
identified by the codes C or L indicate directly connected networks. The codes mean
that the devices are connected to the physical layer. The C and L records are
automatically created.
Static Route - Static routes are configured and recorded manually, and are identified in
the routing table by the letter S.
Dynamic Route - Dynamic routes are identified with unique letters that indicate the
dynamic protocol that was used to create them.
Dynamic protocols include the following:

D - EIGRP routing protocol

O - OSPF routing protocol

R - RIP routing protocol


### Textbook — strona 105

Section 4: IPv4
An Internet Protocol (IP) is a numerical label assigned to devices connected to a
network. It is used for host identification and communication.
The public IP address space is managed by IANA (Internet Assigned Numbers Authority)
and divided into five regional Internet registries (RIRs), each responsible for their
designated territories.
Each RIR is responsible for address assignment to users and service providers.
Addresses
IPv4 addresses consist of 32 bits and are divided into four octets, each containing 8 bits.
This addressing method provides 4,294,967,296 (2%32) IPv4 addresses in total.
An IP address represented in binary will appear as follows:

192.168.1.1 = 11000000.10101000.00000001.00000001
Structure
An |Pv4 address consists of two parts: network and host, defined by the subnet mask.
Network - Represents the network segment part of the IP address.
Host - Represents a specific device on the network segment.
Subnet Mask
A subnet mask is a 32-bit address, the same as an IP address.
Like an IPv4 address, a subnet mask consists of 4 octets, separated by dots (.).
Two similar IP addresses can belong to completely different networks, depending on
the subnet mask.
Subnet masks will be further explained in the next module.


### Textbook — strona 106

Suffix Calculation
Just like the IPv4 address, the subnet mask is constructed of 4 octets (8 bits each).
The suffix is a simple representation of the subnet mask, using less characters, and is
placed after the IPv4 address.
The suffix will be written in correspondence to the number of bits set to 1 in the subnet
mask.
8 bits = 255.0.0.0/8 255.0.0.0/8
16 bits = 255.255.0.0/16 |
24 bits = 255.255.255.0/24
11111111.00000000.00000000.00000000

32 bits = 255.255.255.255/32
Classful Addressing
This type of addressing architecture was used from 1981 to 1993, when the CIDR
originated. It categorizes the IPv4 address space into 5 different classes. The categories
are based on the address’s first octet.

NETMASK RANGES PREFIX CLASS

255.0.0.0 1.0.0.0 - 127.255.255.255 /8 A

255.255.0.0 128.0.0.0 - 191.255.255.255 /16 B

255.255.255.0 192.0.0.0 - 223.255.255.255 /24 oe

* Reserved for multicasting 224.0.0.0 - 239.255.255.255 D

* Experimental 240.0.0.0 - 239.255.255.255 E


### Textbook — strona 107

Communication Types
Unicast - The most basic form of IP communication is one-to-one, where a packet is
sent directly from one device on the network to another device on the network.
A single source communicates with a single destination.
Multicast - Multicast is when a single source communicates with multiple destinations.
A packet is sent from one device on the network to a group comprised of one or more
devices, using Class D addresses.
Broadcast - Broadcast is when a packet is sent from one device on the network to all
other devices on the network, using a generic broadcast address (255.255.255.255 for
IPv4, or FF:FF:FF:FF:FF:FF for IPv6).
Link-Local
Link-Local addresses, also known as APIPA addresses, are valid only for communication
within the network broadcast domain. The entire 169.254.0.0/16 address range is
reserved for Link-Local.
If the DHCP is not available or an IP is not statically configured, the OS will randomly
generate a Link-Local address.
Link-Local addresses are not guaranteed to be unique outside their network segments,
which is the reason why routers do not forward their packets.
Loopback
Loopback addresses represent the same interface in a computer. In IPv4, an entire
network (127.0.0.0/8) is reserved for loopback addresses.
Almost all leading operating systems use the name "localhost" to represent IPv4
loopback address 127.0.0.1.
The IPv6 address reserved for loopback is:

0000:0000:0000:0000:0000:0000:0000:0001/128


### Textbook — strona 108

Public vs Private
Private IPs are non-unique global addresses that can belong to one of three IP address
ranges. They are used to create networks that do not communicate over the Internet.
The same private IPs can be found in multiple separate networks and can be used
freely.
Public addresses are used for communication over the Internet. These IP addresses
must be unique, require a fee, and are purchased from service providers. A router will
typically have both a private IP on one NIC, and a public IP on another NIC. For example,
the address 8.8.8.8 is a public address used by Google.
Private IP Ranges
Private addresses are used in networks designed for homes and organizations. The
ranges differ according to the amount of separate networks and computers in each
network, and there are no enforced rules.

RANGE TARGET CLASS

10.0.0.0 — 10.255.255.255 A few large networks with many computers. A

172.16.0.0— 172.31.255.255 A considerable amount of medium-size networks B

192.168.0.0 - 192.168.255.255 Ahigh amount of small networks with only a few computers. &

é Lab — IPv4 & Initial Router Configuration
—=/ | Learn how to configure initial settings on a Cisco Router.
m=:
Perform the instructions in lab document Net-05-L2.


### Textbook — strona 109

Section 5: IPv6é
Over the years, the IPv4 address pool was slowly depleted due to technical progress
that led to more and more devices around the world being connected to the Internet.
IPv6 was designed to solve the IPv4 address limitation and provide additional
enhancements. IPv6 has a larger 128-bit address pool, with the number of available
addresses being 340*10*.
Example of an IPv6 address: 2001:0000:3238:0001:0063:0000:0000:FEFB
Compressing IPv6 Addresses
IPv6 addresses are long and difficult to read. Some rules exist to omit specific numbers
to simplify the addresses.
Full Address - A full address contains all 8 blocks, with 4 hexadecimal digits.
Example of a full IPv6 address: 2001:0000:3238:0001:0063:0000:0000:FEFB
Leading Zeros - The first rule allows us to discard leading zeros in a block, making the
address a bit shorter: 2001:0:3238:1:63:0000:0000:FEFB
Consecutive Zeros - If two or more blocks contain consecutive zeros, they can be
omitted and replaced with double colon signs (::) resulting in: 2001:0:3238:1:63::FEFB
Note that omitting is allowed only once in the address.
Zero Block - If there is a block that consists of 4 zeros, but without a consecutive zero-
filled block, it can be replaced with a single zero, and the final address will be:
2001:0:3238:1:63::FEFB


### Textbook — strona 110

IPv6 Address Breakdown
2001:0ABC:00BB:: 0000 ::0000:0000:0000:0001 : /64
The suffix represents the prefix portion of the address. IPv6 does not use notation
subnet masks like IPv4. The prefix length indicates the network portion.
1. Because the prefix is /64, the first 64 bits in the address represent the network
portion.
2. The 16 bits from the 49th to the 64th are for defining subnets.
3. The remaining 64 bits represent the host portion in the IPv6 address.
4. The prefix range can be from 0 to 128, with the most common being /64.
Router(config-if)#ipv6é address
2001 : QABC : QOBB : 0000 : 8000 : 0080 : 8000: 0001/64
Configure and Verify IPv6é
To enable IPv6 routing, enter the configuration terminal mode, and run the command
ipv6 unicast-routing.
Configure IPv6 on a router interface using the command ipv6é address.
Verify the configuration using the command show ipvé interface brief.
Router(config)#ipv6 unicast-routing
Router(config)#interface gigabitEthernet0/e/e
Router(config-if)#ipv6 address 2001: @ABC: Q@BB : 0000: 0000 : 8000: 0000 : 0801/64
Router(config-if)#no shutdown
Router (config-if)#exit
Router#show ipv6é interface brief
GigabitEthernet@/0/e [up/down]
FE8@: :201:97FF:FE13:A801
2001:ABC:BB::1
GigabitEthernet®/0/1 [administratively down/down]
unassigned
Vlan1 [administratively down/down]
unassigned


### Textbook — strona 111

Device Communication Types
Unicast - Unicast addresses represent specific network interfaces that support IPv6.
Unicast addresses have 3 sub-types (described in the following section).
Multicast - Addresses used to send |Pv6 packets from a single host to multiple
destinations.
Anycast - IPv6 unicast addresses that can be assigned to multiple devices. Packets sent
to an Anycast address are routed to the nearest device that has that address (which is
why Anycast is also known as "one to the nearest“). This method operates similar to
IPv4 broadcast.
Unicast Types
Global Unicast - |Pv6 global unicast addresses are similar to IPv4 public addresses. They
are unique and can be routed via the Internet. IANA currently assigns only 2000::/3
addresses.
Link-Local - Addresses that enable communication between devices in the same local
link (LAN).
Link Local addresses must be unique only within the link. They are not guaranteed to be
unique beyond their network segment, and begin with FE80::/10.
Unique-Local - Similar to IPv4 private addresses, with minor differences.
Unique addresses should not be routable in the global IPv6, and should not be
translated to global IPv6 addresses. They begin with FCOO::/8.


### Textbook — strona 112

IPv6 Address Example
The following table lists examples of commonly used IPv6 addresses of various types.
Type Address Example Notes

Global Unicast 2001:0ABC:1111:0000:1111:0000:0000:0200 The address range is from 2000 to 3FFF.
Global Unicast 2001:0ABC:0000:00BB:DCBA:0000:0000:0200 The address range is from 2000 to 3FFF.
Link-Local FE80:0000:0000:0000:3211:5412:ECDC:FE11 Link-local address prefix is FE80::/10.
Link-Local FE80:0000:0000:0000:3211:5412:CAD1:FE12 Link-local address prefix is FE80::/10.
Multicast FF02:0000:0000:0000:0000:000F:FFO0:120F Multicast addresses use the prefix ff00::/8.
Anycast ¥0004.100410040040000:0000:0000:0000 Similar to broadcast addresses in IPv4.
IPv4 and IPv6 Coexistence

IPv4 and IPv6 can coexist using protocols and tools created by IEFT, which are known as:
Dual Stack, Tunneling, and Translation.

Dual Stack - Dual Stack means that a device runs both IPv4 and IPv6 protocols
simultaneously. Using two stacks allows both IP versions to coexist.
Tunneling - Tunneling is used when IPv6 addresses are to be sent over IPv4 networks,
or vice versa. In this method, the IPv6 packet is encapsulated within an IPv4 packet.
Translation - Translation allows IPv6 to communicate with IPv4-enabled devices using
techniques similar to those used by NAT.

é Lab — Configure IPv6 Addressing
—J | Practice configuring IPv6 addresses on a router and clients, and verification
m= =| of IPv6 addressing implementation.
Perform the instructions in lab document Net-05-L3.


# Chapter 6: Subnetting Concepts


### Textbook — strona 113

| Chapter 6: Subnetting Concepts
Section 1: Subnetting
Subnetting means subdividing a network to manage, design, and implement an
effective IP addressing plan. When organizations add hundreds and even thousands of
hosts to their network, subdividing the network facilitates faster packet delivery and
adds filtration by minimizing local traffic.
Subnetting reduces overall network traffic and improves performance.
Broadcast Domains
Large networks containing many hosts poses a problem for broadcast domains, because
hosts can generate broadcast messages and affect network performance.
A large amount of traffic generated by broadcast messages causes network operation
to slow down.
Each device must accept and process broadcast requests, even if the request is not
intended for a particular device.
The solution is to reduce the network size, and create smaller broadcast domains by
subnetting the network.
Why Subnetting?
Subnetting improves network performance by reducing the overall volume of network
traffic.
In addition, it enables an administrator to implement security policies and control
network growth.
Subnetting creates more manageable network congestion, and simplifies network
administration.


### Textbook — strona 114

Octet Boundary
An Octet Boundary is a subnet created by borrowing one or more of the host bits to be
used as network bits.
By extending the subnet mask with bits from the host portion, additional subnets can
be created.
The easiest method of network subnetting is to use the octets /8, /16, and /24.
Additional 1 bits mean more Networks.
Additional 0 bits mean more Hosts.
The following table lists attributes of the most common boundaries: /8, /16, and /24:
Prefix Subnet Mask Binary Number of Hosts
11111111.00000000.00000000.00000000
/8 255.0.0.0 nnnnnnon.hhhhhhhh.hhhhhhhh.hhhhhhhh 16,777,214
255 0 0 0
11111111.11111111.00000000.00000000
nonnnannn.nnnnnnnn.hhhhhhhh.hhhhhhhh 65,534
/16 255.255.0.0 355 355 0 6
11111111,11111111.11111111.00000000
nnnnnnnn.nnnnnnnn.nnnannnnn.hhhhhhhh 254
/24 255.255.255.0 _ O55: 955 7
n= Network portion, h = Host portion


### Textbook — strona 115

Section 2: CIDR
Since not all networks in an organization are compatible with IPv4 address classes (due
to the number of hosts), using these classes, in some cases, may result in a waste of
addresses (which are important commodities in any organization).
For example, an organization with a network of 400 hosts must use class B, which
means they will waste more than 60,000 addresses.
Classless Inter-Domain Routing
To resolve that issue, Classless Inter-Domain Routing (CIDR) was defined in RFC 4632.
CIDR allows an IP address to use any subnet mask, regardless of predefined classes.
For example, IP address 10.1.1.1, which according to the class-based system should be
in class A, can belong to class B or C, in accordance with the user’s preference.
The following table displays addresses subnetted with different boundaries.
Subnet Address Useable Address Range Broadcast Address
10.0.0.0/16 10.0.0.1— 10.0.255.254 10.0.255.255
10.1.0.0/16 10.1.0.1— 10.1.255.254 10.1.255.255
10.2.0.0/16 10.2.0.1— 10.2.255.254 10.2:255.255
10.100.0.0/24 10.100.0.1— 10.100.0.254 10.100.0.255
10.101.0.0/24 10.101.0.1—10.101.0.254 10.101.0.255
10.255.255.0/24 10.255.255.1- 10.255.255.254 10.255.255.255
CIDR Subnetting Example
As an example, we will use the subnet 10.1.1.0/24. The subnet must appear in binary on
the left side.
Creating two smaller sub-networks can be done by “borrowing” a bit from the host
portion to the network portion.
After subnetting, the new address will be 10.1.1.0/25. Each network address will be
assigned 126 host addresses.


### Textbook — strona 116

Network Portion Host Portion
SSS k
i 1
11111111.11111111.111111111. 00000000
Network Portion Host Portion
f - 7‘; a
11111111.11111111.11111111.1 0000000
* For one borrowed bit: 25u>-network bits = 21 = 2
sub-networks
¢ For two borrowed bits: 25u>-network bits = 22 = 4
sub-networks
* Andsoon...
Subnetting Classless Network
Subnets can borrow bits from any host bit to create additional masks. For each
borrowed bit in the fourth octet, the number of sub-networks is doubled, while the
number of hosts per subnet is reduced.
Prefix Subnet Mask Mask in Binary Networks Hosts
Anannnnn.nnnnnnnn.nnnnnnnn.nhhhhhhh 2 126
ie ape.2sn.2n ee 11111111.11111111.11111111.10000000
nnnnnnna.nnnnnnnn.annnanan.anhhhhhh 4 62
126 LEE NT 11111111.11111111.11111111.11000000
nnnnnnnn.nnnnnnnn.nnnnnnan.annhhhhh 8 30
pi 295.259.255.224 11111111.11111111.11111111.11100000
nnnnnnnn.nnnnnnnn.nnnnnnan.annnhhhh 16 4
ps THE ASS 255280 11111111.11111111.11111111.11110000
n = Network Portion, h = Host Portion


### Textbook — strona 117

Case Study 1: Configuration Per Sub-Network
A network manager requests to extend the current network to an additional four sub-
networks. The given IP address and subnet mask is 172.16.0.0/24.
* How would we add four more networks?
* What are the new network addresses?
| Network Address i Usable IP Addresses Broadcast Address i
Solution:
* Adding four networks: 24x = 4 ?, the answer is 2. That means we need to borrow
two bits from the subnet to create an additional four sub-networks.
* RED =new network portion, BLUE = new host portion:
11111111.11111111.11111111.11000000
* The new network addresses are: 172.16.0.0, 172.16.0.64, 172.16.0.128,
172.16.0.192
|[_2asco | Grsonvexsos [vaso
The total number of
jump in the last octet:


### Textbook — strona 118

Case Study 2: Configuration Per Sub-Network

A network manager requests to extend the current network by an additional five sub-

networks. The given IP address and subnet mask is 192.168.0.0/24.
* How would we add five more networks?
* What are the new network addresses?

Solution:

* Adding five networks is not possible, with the closest possible network division being
8.

* 24x =8 ?, the answer is 3. That means we need to borrow three bits from the subnet
to create an additional eight sub-networks.

* RED =new network portion, BLUE = new host portion:
11111111.11111111.11111111.11100000

* The new network addresses are: 192.168.0.0, 192.168.0.32, 192.168.0.64,
192.168.0.96, and so on.

Note: The table below displays only the first four of eight subnets.

jump in the last octet:


### Textbook — strona 119

Case Study 3: Network Configuration Per User

A network manager requests a 300-workstation expansion of the network. The

workstations are to be installed in a single broadcast domain. The correct given address

is 10.0.0.0. The aim of the expansion is to use as few resources as possible.
* How would we use the least amount of resources possible?
* What is the new network address, network range, and broadcast address?

Solution:

* To use the least amount of resources possible, the matching subnet will be /23,
because it allows the use of 510 host addresses: 2*9 = 512, 512 — 2 (Minus Network
address, Broadcast Address) = 510 hosts.

* RED =new network portion, BLUE = new host portion:
11111111.11111111.11111110.00000000

* The new network address will be 10.0.0.0/23

* The network range is 10.0.0.1/23 — 10.0.1.254/23

* The broadcast address is 10.0.1.255/23


### Textbook — strona 120

Section 3: VLSM
VLSM (Variable Length Subnet Mask) is a method by which a network is subnetted, and
the subnets are then subnetted further (when using only CIDR, they are not subnetted
further).
The process can be repeated several times to divide the subnets into various sizes, to
ensure that IP addresses are not wasted.
Formulas are applied to calculate the number of hosts and subnets.
Note: Knowing your address requirements will help determine the range of host
addresses.
VLSM Subnetting Example
As an example, we will start with the network address 10.0.0.0/8. This address is
subnetted into 2 additional networks.
The subnetting process (CIDR) created the networks 10.0.0.0/9 and 10.128.0.0/9.
After creating the networks, each was subnetted (VLSM) to create additional networks,
similar to using CIDR.
VLSM is useful when using CIDR provides too many unused addresses for one network.
Sa Ps
see Pe
a ae
- we
10.0.0.0 /9 10.128.0.0 /9
10.0.0.0/10 10.64.0.0/10 10.128.0.0/10 10.192.0.0 /10
10.0.0.0 /9 used to create 2 —_
11111111.11000000.000000.000000
10.0.0.0 /10 and 10.64.0.0 /10 subnets are created >


### Textbook — strona 121

‘ Lab — Subnetting Practice
—=J/ | Answer questions based on material covered in the module, including the
= =| topics of how to subnet networks and assign IP addresses.
Perform the instructions in document Net-06-L1.


### Textbook — strona 122

Section 4: Network Address Scheme Design

Network Planning

A network needs to be well-designed. Addresses must not be assigned randomly!

Planning a network requires examination of how the organization is structured, and

how the subnets will be structured.

Planning addresses involves deciding how many hosts per subnet there will be, how

large each subnet will be, and how host addresses will be assigned.

Note: Knowing your address requirements will help determine the range of host

addresses.

Planning Considerations

Prevent Duplication In an inter-network structure, each host must have a unique
address. Planning and documentation prevent the creation of
duplicate addresses.

Access Control If addresses are randomly assigned, servers that provide
resources to internal and external hosts will not be able to
control access efficiently and effectively.

Monitor Network traffic is examined for source IP addresses generated or
received from packets. With proper planning, finding problematic
devices should be a simple process.

Assignable Address Devices

Clients Most networks use DHCP to dynamically assign addresses,
eliminating the need for network staff to do so, and preventing
entry errors. When the address scheme changes, the DHCP server
must be reconfigured.

Servers In most networks, servers must be made available to remote
users. The servers are assigned private internal addresses, and
the forwarding device will perform additional translations to
public addresses (NAT). Servers are typically configured with
static addresses.


### Textbook — strona 123

Routers/Switches Routers and switches are assigned IP addresses. Switches can be
managed remotely via the cloud. Routers are assigned IP
addresses because they operate in Layer 3. Routers are typically
configured with static addresses.

Gateway A gateway is a packet-forwarding device, and is typically a firewall
or router. Each interface that serves as a gateway for hosts in the
network must be assigned an IP address.


# Chapter 7: IPv4 & IPv6 Static Routing


### Textbook — strona 124

| Chapter 7: IPv4 & IPv6 Static Routing

Section 1: Router Operation

Router Operation Review

One of the router’s main jobs is to select the best path for a packet. The decision is

based on its destination address.

After determining the best path on which to forward the packet, the router

encapsulates the packet in a new frame in accordance with the relevant outgoing

interface.

Packet Forwarding Process

Examination In the first step, the router decides whether to process a packet
or ignore it. Routers will ignore packets with errors, or packets
they don't know how to process.

Decapsulation The router examines the Layer 2 address to decide if the packet
was intended for itself (the default gateway), and verifies the
integrity of the frame using the FCS (Layer 2 trailer).

Decision-making The router decides where to forward the packet to, based on its
destination IP address and the routing table.

Encapsulation The router re-encapsulates the packet with new Layer 2 headers
for the next hop (MAC address of the next hop), according to the
decision made in step 3.

Forwarding After a decision is made, the router forwards the packet to the
interface from which the packet must exit.


### Textbook — strona 125

Remote Networks
A router's best routing decision is based on its routing table. But where does the routing
table get its information from?
Networks connected directly are added to the table immediately, but a remote network
must be configured by the user.
A remote network is any network not connected locally to the router.
Note: The ICMP message "Destination unreachable" is displayed whenever the router
cannot find a match for the path in its routing table.
Remote Network Learning
A remote network can be learned by a router in one of two ways: statically or
dynamically.
In the static routing method, the user enters every network manually in the routing
table.
In the dynamic routing method, the router automatically learns the remote network
from the routing tables of adjacent routers, by using various protocols.


### Textbook — strona 126

Static Method Pros and Cons
Advantages Disadvantages
A simple solution for small Error-prone in large network
networks. environments.
Not advertised over the network, Does not support verification
meaning better security. methods.
No CPU and memory usage for Configuration and maintenance
routing purposes. are time-consuming.
Every path a packet takes is known, .
a . Requires complete knowledge of
which improves network traffic ;
the entire network.
management.
When to use Static Routing
Network administrators decide if and when to use Static Routing, based on network
requirements.
Stub Networks
Static routing is a better choice when routing to and from stub networks.
Stub networks consist of a single router that sends and receives non-local traffic via a
single path.
Small Networks
Although Static Routing is simple and secure, and saves resources, it does not provide a
sufficient level of scalability in larger networks.


### Textbook — strona 127

Section 2: IPV4 Static Routing

Static Route Types

The following are the most common types of Static Route implementation.

Standard Static Route = Manually configured route that forwards traffic to a specific
network.

Default Static Route Typically used as a Gateway of Last Resort, which is used for
any packet that does not have a destination route in the
routing table. The destination in such cases is often set to the
Internet.

Network Topology Example

A host on network A wants to communicate with a host on network B.

If no static or dynamic routing is used, R1 does not know the destination network and

its direction.

For R1 to know network B, add the network and direction to the routing table. Now, R1

will forward network A host packets to the correct destination.

The same is required for R2 and R3 to recognize network A.

|
> _ a
172.17.0.2 Ss =
———sIy
: R3 Net C 10.2.0.0/24
— Gig2/0 an creat
——— —"
— ———4
Ey EY
Net A 10.0.0.0/24 oe i Net B 10.1.0.0/24


### Textbook — strona 128

Syntax
H Router (config)# ip route | <network-address> i <subnet-mask> i <direction> H
i i | i i 2 i 3 1
1. Specifies the remote network address.
2. Specifies the remote network subnet mask.
3. Sets the direction of the network, which can be:
Directly-connected - the local outgoing interface.
Next-hop - the IP address of the interconnected router.
Ri(config)#ip route 10.1.0.0
255.255.255.0 172.16.0.2
Standard Configuration Example
The example below is a static route configuration example, based on the topology
above.
The ip route command is used to add a new network route to the routing table.
Verify the addition of static routes by displaying the routing table using the show ip
route command.
Note: The next-hop and directly-connected options are also known as recursive and
directly-attached routes.
R1(config)#ip route 10.1.0.@ 255.255.255.@ 172.16.0.2
R1(config)#ip route 10.2.0.0 255.255.255.0 gigabitEthernet 1/0
%Default route without gateway, if not a point-to-point interface,
may impact performance
R1(config)#do show ip route
10.0.0.0/24 is subnetted, 2 subnets
C 172.16.0.0/16 is directly connected, GigabitEtherneto/oe
Cc 172.17.0.0/16 is directly connected, GigabitEthernet1/0
Cc 172.18.0.0/16 is directly connected, GigabitEthernet2/e


### Textbook — strona 129

Default Configuration Example
The default and standard routes use the same syntax, except for one difference: The
default route uses 0.0.0.0 to represent any network address with any subnet mask.
A default route can be set with a next-hop or outgoing interface.
The standard route is denoted by S, while the default is denoted by S*.
R1(config)#ip route 0.0.0.0 0.0.0.8 gigabitEthernet 2/0
R1(config)#do show ip route
10.0.0.0/24 is subnetted, 2 subnets
Ss 10.1.0.0 [1/0] via 172.16.0.2
Ss 10.2.0.0 is directly connected, GigabitEthernet1/0
Cc 172.16.0.0/16 is directly connected, GigabitEthernet0/oe
Cc 172.17.0.0/16 is directly connected, GigabitEthernet1/0
ie 172.18.0.0/16 is directly connected, GigabitEthernet2/0
Administrative Distance
Administrative Distance (AD) is a predefined value for each routing method.
The router selects the path of the lowest AD value in the routing table.
For example, if there are two routes to the same destination network, one via OSPF (a
dynamic routing protocol) and the other a static route, the router will select the static
route (1 vs. 110).
The following table lists default AD values for different routing methods:
Method/Protocol AD Value
Directly-connected 0
Static Route 1
Internal EIGRP 90
OSPF 110
RIP 120


### Textbook — strona 130

Additional Types of Static Routing
Floating Static Route Provides backup paths to primary static routes for situations
in which a link failure occurs. This route type is only used
when the primary route is not available. The AD for floating
static routes is higher than the AD for primary routes.
Summary Static Route = To reduce the number of routing table entries, multiple static
routes can be summarized to a single address.
Host Static Route Similar to standard route, but instead of configuring a
network, it is used to forward traffic to a specific host. It uses
a default mask of 255.255.255.255
Floating Configuration Example
Command:
ip route <network-address> <subnet-mask> <direction> <AD>
The code below is an example of a primary and backup route configuration.
The primary route is set with a default AD (1).
The backup route points to the same network but from a different direction, and is set
with a higher AD (5).
Note: The backup route will be shown only if the primary route fails.
Ri(config)#ip route 192.168.1.@ 255.255.255.@ 172.16.0.2
Ri(config)#ip route 192.168.1.@ 255.255.255.0@ 10.0.0.2
Ri(config)#do show ip route
iG 10.@.@.6/30 is directly connected, GigabitEthernet0/1
e 172.16.0.0/3@ is directly connected, GigabitEthernet0/o
S 192.168.1.0/24 [| /0] via 172.16.0.2
S 192.168.1.0/24 [°/0] via 10.0.0.2


### Textbook — strona 131

Host Configuration Example
Command:
ip route <ip-address> 255.255.255.255 <direction>

Although this type of static route is not very common, it can be useful as a redundant
path to a specific resource, such as a server.
This method may be useful for special routing requirements.

R1(config)#ip route 192.168.1.5 255.255.255.255 172.16.0.2

R1(config)#do show ip route

(é 10.0.0.0/3@ is directly connected, GigabitEthernete/1
Summarizing Addresses
Contiguous: To summarize the network to a single address, the destination networks
need to be contiguous.
Same Routing Path: All networks must use the same outgoing interface or next-hop
address.
In the example below, instead of four standard static routes, a single summarized static
route is used.

—S
— 10.0.0.0/30 =) 172.10.0.0/16 ee 172.11.0.0/16
Ri R2 7 R3
172.13.0.016
172.12.0.0/16
R4


### Textbook — strona 132

Summarizing Process
1—Convert to Binary

172.10.0.0 — 10101100.00001010.00000000.00000000

172.11.0.0 — 10101100.00001011.00000000.00000000

172.12.0.0 — 10101100.00001100.00000000.00000000

172.13.0.0 — 10101100.00001101.00000000.00000000
2 — Compare Identical Bits

172.10.0.0 — 10101100.00001010.00000000.00000000

172.11.0.0 — 10101100.00001011.00000000.00000000

172.12.0.0 — 10101100.00001100.00000000.00000000

172.13.0.0 — 10101100.00001101.00000000.00000000
3 —Create a Summarized Address

Network Address:

172.8.0.0 - 10101100.00001000.00000000.00000000

Subnet Mask:

255.248.0.0 - 11111111.11111000.00000000.00000000
Summarizing Configuration Example
Command:

ip route <summarize-address> <summarize-mask> <direction>
The example below shows the code for summarizing and verifying the new route.
Note the prefix 13.

R1i(config)#ip route 172.8.0.@ 255.248.0.0 10.0.0.1
C 10.0.0.0/24 is directly connected, GigabitEtherneto/o


### Textbook — strona 133

‘ Lab — Configuring IPv4 Static and Default Routes
= | Implement IPv4 standard and default static routes in a full network
=== | topology.
Perform the instructions in document Net-07-L1.


### Textbook — strona 134

Section 3: IPV6 Static Routing
Static routing is similar for IPv4 and IPv6, with the exception of how the destination
network addresses are formatted.
IPv6 supports the same static routing types, and most of the parameters are identical to
those in IPv4 commands.
IPv6 Static Routing Requirements
The following are required to enable |Pv6 static routing:
= |IPv6 packet forwarding must be enabled on the Cisco router.
The command is IPv6 unicast-routing
«The interface must be enabled and configured with an IPv6 address.
IPv6 Static Routing Syntax
i Router (config) # i ipv6é route H <network-address> / <prefix> H <direction>
H H i 1 i 2 H 3 i
1. Specifies the IPv6 remote network address.
2. Specifies the remote network prefix.
3. Sets the direction of the network, which can be:
Directly-connected - the local outgoing interface.
Next-hop - the IPv6 link-local or global-unicast address of the interconnected
router.
R1(config)#ipv6 route
2001:abcd:cafe::/64 serial 0/0/02


### Textbook — strona 135

IPv6 Configuration Example
The code below includes examples of all types of IPv6 static routes:
* Standard (next-hop)
* Default (directly-connected)
* Summary
* Floating
R1(config)#ipv6 route 2001:abcd:cafe::/64 2002:abcd:aaaa::1
Ri(config)#ipv6é route serial 0/0/08
Ri(config)#ipv6 route 2001:abcd:cafe:: gigabitethernet0/o
R1(config)#ipv6 route 2001:abcd:cafe::/64 gigabitetherneto/e
Verifying IPv6 Configuration
show ipv6 route displays and verifies the IPv6 routing table.
Remember not to use show ip route (displays IPv4 routing table), but rather
show ipv6 route
Ri(config)#do show ipv6é route
Ss 2001:ABCD:CAFE::/64 [1/0]
via 2002:ABCD: AAAA: :1
S ::/@ [1/0]
via serial 0/0/@


# Chapter 8: Dynamic Routing


### Textbook — strona 136

| Chapter 8: Dynamic Routing

Section 1: Dynamic Routing Concepts

Dynamic routing protocols have been in use since the late 1980s.

Many of the early routing protocols are no longer in use today because of the

complexity of today’s networks compared with those in earlier years.

Dynamic routing protocols have two main goals:

@ To help routers update each other regarding routing information on the network.

@ To determine the best path to destination networks, based on several parameters
(each dynamic protocol chooses the best path based on different parameters). After
determining the best path, it is added to the routing table.

Dynamic routing protocols are used by routers to inform other routers of networks it

can reach. This ensures that all routers on the network work together to exchange data

among them.

The act of broadcasting or multicasting such information is called “advertising”.

Some routing protocols use “hello” packets to verify that other routers are “alive.” If a

router does not reply, it will eventually be considered “dead” by the sending router.

Some routing protocols send “hello” packets regularly, even if no changes occur in the

network.

Classful/Classless

Dynamic routing protocols can either be classful or classless, which refer to the

protocol’s addressing method.

Classful routing protocols do not include subnet mask routing information. Instead, they

determine the subnet mask based on the first octet of the IP address.

Classless routing protocols are more modern and include subnet masks in their routing

updates.


### Textbook — strona 137

AD Tables
AD (Administrative Distance) is a predefined value that represents a route preference.
The value is assigned to dynamic routes, static routes, and directly-connected routes.
The following table lists default AD values for various routing protocols.

(0) Directly Connected Interface

1 Static Route

90 Internal EIGRP

110 OSPF

115 IS—IS

120 RIP.
Metrics
A metric is a measurable value assigned by the routing protocol to different routes
based on the usefulness of the route.
When there are multiple paths to a remote network in the same protocol, routing
metrics are used to determine the overall “cost” of a path from source to destination.
Routing protocols determine the best path based on the route with the lowest cost.


### Textbook — strona 138

Metrics used in Routing Protocols
Routing Information Protocol (RIP) — The RIP hop count metric will choose the path
with the least amount of hops.
Open Shortest Path First (OSPF) — This is Cisco’s route cost protocol, which is based on
cumulative bandwidth from source to destination. OSPF will choose the path with the
highest bandwidth.
Enhanced Interior Gateway Routing Protocol (EIGRP) — This protocol uses a metric
based on minimum bandwidth, delay, load, and reliability.
Distance Vector
Distance Vector is a routing algorithm that calculates the best path for a packet based
on the characteristics of Distance and Vector.
Distance — The distance between the router and the destination network, based on a
metric, such as link cost, number of hops, bandwidth, others.
Vector — The outgoing interface and the direction to the path that leads to the next-hop
router.
Link State
Link State routing protocols include complete network topology maps.
The map is created based on information gathered from all routers on the network.
Link State routing protocols do not broadcast information regularly.
Updates are only sent when a change occurs on the network.
Routing Table
Routing tables contain data stored in the router, and lists of routes to particular
network destinations.
The tables also include network topology information.
The example code below shows how a router “learns” remote network routes.


### Textbook — strona 139

Router#show ip route

Codes: C - connected, S - static, I - IGRP, R - RIP, M - mobile, B - BGP

D - EIGRP, EX - EIGRP external, O - OSPF, IA - OSPF inter area

N1 - OSPF NSSA external type 1, N2 - OSPF NSSA external type 2

El - OSPF external type 1, E2 - OSPF external type 2, E - EGP

i - IS-IS, L1 - IS-IS level-1, L2 - IS-IS level-2, ia - IS-IS inter area

* - candidate default, U - per-user static route, o - ODR

P - periodic downloaded static route

Gateway of last resort is not set

C 192.168.4.0/24 is directly connected, Serial2/@

C 192.168.5.0/24 is directly connected, FastEthernet@/@

O 192.168.1.0/24 [110/129] via 192.168.4.1, 00:00:52, Serial2/0

0 192.168.2.0/24 [110/128] via 192.168.4.1, 0:00:52, Serial2/o

O 192.168.3.0/24 [110/65] via 192.168.4.1, 00:00:52, Serial2/0
Routing Table Keys
S — Indicates that the route was manually created by an administrator to reach a
specific network. This is known as a static route.
D - Indicates that the route was learned dynamically from another router using the
EIGRP routing protocol.
O - Indicates that the route was learned dynamically from another router using the
OSPF routing protocol.
R — Indicates that the route was learned dynamically from another router using the RIP
routing protocol.
Once the protocols are activated, the routers begin “talking” to each other and map the
network topologies themselves.
Dynamic Routing is based on software that can gather a lot of information in a short
time and input it to an algorithm that computes the information to find the fastest
route to each network.
Each Dynamic Routing protocol uses Timers that detect any change in the topology,
such as a connection failure. When a change is detected, and the change involves a
network failure, the protocols will search for an alternate path.


### Textbook — strona 140

OSPF Route
Displayed Route : : 7 7
jo | 192.168.20.0/24 | [110/65] via | 172.16.0.2 | 00:04:06 +} — Serialo/o/o
11 z ' 3 ‘ 4 t 5 ' 6 <p>
1. O-Route source sign that represents the learned path.
2. 192.168.20.0/24 — Remote network address.
3. 110- Administrative Distance value that assists in determining the path.
65 — A metric value of the path assigned by the routing protocol.
4. 172.16.0.2 — Next hop. Neighbor’s router IP address through which the local router
will transmit information.
5. 00:04:06 — Route timestamp. A signature indicating how much time the route
remains active.
6. Serial0/0/0 — Outgoing interface. The local interface through which information will
be sent to the remote router.
Example:
Gateway of last resort is not set
C 192.168.4.0/24 is directly connected, Serial2/0e
C 192.168.5.0/24 is directly connected, FastEthernete/e
O 192.168.1.0/24 [110/129] via 192.168.4.1, 00:00:52, Serial2/e
O 192.168.2.0/24 [110/128] via 192.168.4.1, 00:00:52, Serial2/e
O 192.168.3.0/24 [110/65] via 192.168.4.1, 00:00:52, Serial2/@e


### Textbook — strona 141

Passive Interface

Passive interface is a feature used in all routing protocols. Its purpose is to disable

routing updates on specific interfaces, which decreases resource usage and increases

security. It is typically placed on interfaces facing the LAN, and the command syntax is
the same in all routing protocols.

Passive interface should not be configured between routers.

Passive interfaces are used for the following reasons:

1. Bandwidth - dynamic routing updates consume bandwidth because messages are
sent in broadcast or multicast, causing switches to broadcast to all ports.

2. Resources - devices in the same LAN must process updates up to Layer 4 (transport
layer), and only then discard the update.

3. Security - packet sniffing software can be used to intercept packets that include
routing updates, and redirect traffic by corrupting the routing table with false
metrics.

Classful & Classless Routing Protocols

Classful routing protocols provide routing updates according to classful network

addresses (A, B, C). For example, the route for 10.15.30.2/11 and 10.80.0.15/11 will be

advertised as 10.0.0.0 even if subnetted.

Classful routing protocols include RIPv1 and IGRP.

Classless routing protocols provide routing updates according to VLSM addresses,

rather than according to classful addresses. For example, the route for 10.80.30.2/11

will be advertised as 10.64.0.0/11.

Classless routing protocols include RIPv2, EIGRP, and OSPF.


### Textbook — strona 142

Section 2: RIPv2
RIPv1, released in 1988, operates using the auto-summary method, which combines
two or more subnets into one larger subnet.
For example, if a router using the RIPv1 routing protocol has two links, one leading to
10.0.1.0/24 and another leading to 10.0.0.0/24, auto-summary will merge them to
10.0.0.0/8.
RIPv2 (Routing Information Protocol, version 2) is a classless, Distance Vector routing
protocol that was first introduced in 1993 (RFC 1723).
It is an enhancement of RIPv1, created mainly to support CIDR and include subnet
masks in its routing updates.
RIPv1 vs RIPv2 vs RIPng
RIPv1 - 1988 RIPv2 - 1993 RIPng
Released in 1988 Released in 1993 Released in 1997
Classful routing protocol Classless routing protocol
Doesn't support VLSM and CIDR Supports VLSM and CIDR Support IPv6
Hop-count metric Hop-count metric Hop-count metric
Doesn't include subnet mask in Includes subnet mask in routing Includes subnet mask in routing
routing updates updates updates
Routing updates are sent in broadcast Routing updates are sent in multicast Routing updates are sent in multicast
(255.255.255.255) (224.0.0.9) (ff00::/3)
Doesn't support authentication Supports authentication Support Pus inherent [see
Sends full routing updates Sends full routing updates Sends full routing updates
RIP Attributes
Administrative Distance - By default, RIP’s administrative distance is 120.
Metric - RIP will determine the path with the least amount of hops. Hop count 0
denotes a directly connected network. 16 denotes a network that is unreachable
because of an RIP hop limitation.


### Textbook — strona 143

RIP Timers
Update - By default, the update value is 30 seconds, and messages will be
broadcast/multicast to an RIP enabled interface.
Example: Two routers with valid RIP routes to each other will send an update every 30
seconds, even if there is no change in the topology.
Invalid - Invalid is also known as an expiration timer, and by default its value is 180
seconds, after which the routing entry will be set to 16 to indicate that the destination
is unreachable.
Example: If a router will not receive an update from its neighbor within 180 seconds, it
will set the route’s hop count to 16 (destination is unreachable).
Flush - When a route is unreachable (invalidated), for another 60 seconds the router
will continuously inform its neighbors of its status.
By default, its status will be announced for 240 seconds in total (180+60 seconds).
If a route is invalid after 180 seconds, it will remain in the routing table for an additional
60 seconds before it is removed.
Hold-down - When the hop count changes from a lower to a higher value, the hold-
down timer begins per-route entry, allowing the route to be stabilized. During this time,
the routing entry cannot be updated.
The default value is 180 seconds.
Auto Summary
Auto Summary is a feature that allows the automatic summarization of routes to their
Classful networks.
By default, RIP summarizes subnets to a major classful network, without exceeding the
classful boundaries.
RIP performs auto-summarization whenever the boundary between two different major
networks is crossed.


### Textbook — strona 144

Network Topology Example
Networks A, B, and C cannot reach each other because their routers do not ‘know’ each
other yet. Once RIP is enabled on all routers, they will start to share routing
information. Next, each router will add remote networks to its table. R1 will add Nets B
and C, for example. This process is called convergence. Every router can reach any
network.
ST 11
Sere igo ( |
$0/0/0 eS S0I0/1 = =
Re Net B 192.168.20.0/2
172.16.0.0/30 172.16.0.4/30
= r s0/0/0 Sr) ——
L B)) Cig010_ qe S001 S010 eee cigov0 {_ ail
-————( eax 172,16.0.8/30 Sa —
INet A 192.168.10.0/24 BE baie Net C 192.168.30.0/2
RIPv2 Configuration Example
The following example demonstrates how the topology above can be configured to use
RIPv2 for Dynamic Routing. The commands used for the configuration are listed and
explained after the example.
R1(config)#router rip
R1(config-router)#version 2
R2(config-router)#no auto-summary
R1(config-router)#network 192.168.10.0
R1(config-router)#network 172.16.0.0
R1(config-router)#network 172.16.0.8
R1(config-router)#passive-interface gigabitEthernet 0/@
R2(config)#router rip
R2(config-router)#version 2
R2(config-router)#no auto-summary
R2(config-router)#network 192.168.20.0
R2(config-router)#network 172.16.0.0
R2(config-router)#network 172.16.0.4
R2(config-router)#passive-interface gigabitEthernet 0/@


### Textbook — strona 145

router rip enables RIP and enters RIP configuration mode.
version sets the RIP version.
network advertises the network and enables RIP updates on the network interface.
no-summary disables the auto-summary feature.
passive-interface disables RIP updates on the interface.
Verify RIPv2 on R1
The example below shows R1’s routing table after RIP finished updating it.
R represents the route learned by the RIP protocol.
An important feature is that if the router finds two equal paths to the network, both
routes are added the table, and load balancing is applied. For example, 172.16.0.4/30

Rl#show ip route

172.16.0.0/16 is variably subnetted, 5 subnets, 2 masks

€ 172.16.0.0/30 is directly connected, Serial@/0/o

L 172.16.0.1/32 is directly connected, Serial@/0/e

Cc 172.16.0.8/30 is directly connected, Serial@/0/1

L 172.16.0.9/32 is directly connected, Serial@/0/1

192.168.10.0/24 is variably subnetted, 2 subnets, 2 masks
Cc 192.168.10.0/24 is directly connected, GigabitEthernete/e
L 192.168.10.254/32 is directly connected, GigabitEthernete/e


### Textbook — strona 146

Verify RIPv2 on R2 & R3
The rip flag shows only RIP entries in the router table.
Another method is to check the running-config file to view the current configuration.
172.16.0.0/16 is variably subnetted, 5 subnets, 2 masks
R 172.16.0.8/30 [120/1] via 172.16.0.1, 00:00:24,
Seriale/e/e
[120/1] via 172.16.0.6, 00:00:08,
Serial@/e/1
R 192.168.10.0/24 [120/1] via 172.16.0.1, 00:00:24,
Seriale/e/e
192.168.20.0/24 is variably subnetted, 2 subnets, 2 masks
R 192.168.30.0/24 [120/1] via 172.16.0.6, 00:00:08,
Serial@/e/1
172.16.0.0/16 is variably subnetted, 5 subnets, 2 masks
R 172.16.0.0/30 [120/1] via 172.16.0.5, 00:00:09,
Seriale/e/e
[120/1] via 172.16.0.9, 00:00:28,
Serial@/e/1
R 192.168.10.0/24 [120/1] via 172.16.0.9, 00:00:28,
Serial@/e/1
R 192.168.20.0/24 [120/1] via 172.16.0.5, 00:00:09,
Seriale/e/e
Show IP Protocols
show ip protocols displays the current protocol settings. This is valid for every dynamic
routing configuration, such as OSPF.
The output includes:
© Timer information
e Advertised networks
e Passive interfaces
e More


### Textbook — strona 147

Rl#show ip protocols
Routing Protocol is "rip"
Redistributing: rip
Interface Send Recv Triggered RIP Key-chain
Seriale/e/e 2 2
Serial@/0/1 2 2
Maximum path: 4
Routing Information Sources:
Gateway Distance Last Update
Distance: (default is 120)
Routing Table Entry
The information presented in routing table entry is segmented into multiple parts, each
part presenting a different type of information.
| R | 192.168.20.0/24/[120/1]} via 172.16.0.5, |@0:00:09, | Serialo/o/e |
1. Route source.
2. The destination network address and prefix.
3. The AD and metric of the route.
4. Next-hop address through which the packet passes to the target network.
5. The route age (timestamp).
6. The local outgoing interface that points to the target network.


### Textbook — strona 148

Gateway of Last Resort
Static Default Route - The static default route redirects packets with unknown
destinations to the Gateway of Last Resort, which is a router that communicates in a
specific direction, typically to the ISP (internet).
Propagating Default Routers - Each routing protocol shares its default routes with all
routers on the network, through protocol updates.

R1(config)#ip route 0.0.0.0

Q.0.0.0 Gig 0/1

R1(config)#router rip

R1(config-router)#

R2(config)#do show ip route

@.0.0.0/@ [120/1] via 192.168.12.1, 00:00:26, Gig
Q/1
GigabitEthernet0/o
E Lab Assignment — Configuring and Verifying RIPv2
=f | Implement and verify dynamic routing using RIP.
m=:
Perform the instructions in document NET-08-L1.


### Textbook — strona 149

Section3: OSPFv2
OSPF (Open Shortest Path First) is a Link State routing protocol introduced in 1989, that
was meant as an alternative to RIP.
OSPFv2 was released in 1991, and is still in use today.
OSPFv3 was developed for IPv6 in 1997.
Best Path
Unlike RIP, OSPF bases its metric calculation not only on hop count, but also on the
bandwidth of the links along the path to the destination.
Cost
OSPFv2 cost calculation (sum of all considerations) determines the best path available.
The default OSPFv2 cost for a Fast Ethernet interface operating at 100 Mbps is the same
as that for a Gigabit Ethernet interface operating at 1 Gbps.
The default OSPFv2 cost formula can be adjusted by running the auto-cost command in
the OSPF routing process.
Note that when using auto-cost, you need to remember to change the OSPF reference
bandwidth in all OSPF routes.
OSPFv2 Concepts
Topology - OSPFv2 keeps track of changes in the topology, such as when a new network
is added or a link fails.
Hello Intervals — “Hello” packets are sent every 10 seconds to all OSPF-enabled routers.
Dead Intervals — When a router does not receive a “hello” packet from its neighbor
within 40 seconds, it will consider that neighbor “dead.”


### Textbook — strona 150

SPF Tree

OSPFv2 uses the Dijkstra SPF algorithm to calculate all routes to each network in the

topology. It then creates a map of the network called an SPF Tree.

The SPF Tree is stored in a database on the router called a Link State Database (LSDB).

Packet Exchange

LSA - Routers use Link State Advertisement to advertise the routing topology to all

other local routers in the same OSPFv2 area.

LSAs are sent in multicast.

LSDB - Link State Database stores received LSA packets, after the routers enable OSPFv2

to use the SPF algorithm to calculate the routes.

DBD - When an adjacency is initialized, OSPFv2 exchanges Database Description Packets

to describe the content of the topological database.

LSR - If a router notices that parts of its topological database are outdated, it will send a

Link State Request to a neighbor for more updated versions of those components.

LSRs are sent in multicast.

LSU - Link State Update messages are responses to LSR messages.

LSUs are sent in unicast.

SPF Algorithm and Tree

By calculating all routes to each network in the topology using the Dijkstra Algorithm,

OSPFv2 creates a map of the network called an SPF Tree.

The SPF Tree is stored in a database on the router called a Link State Database (LSDB).


### Textbook — strona 151

Wildcard Masks
Wildcard masks are used in some routing protocols, such as OSPF, as inverted subnet
masks.
For example, the subnet 255.255.255.0 (binary equivalent =
11111111.11111111.11111111.00000000) inverts to a wildcard mask of 0.0.0.255
(binary equivalent = 00000000.00000000.00000000.11111111).
Router ID
When OSPFv2 is enabled on an interface, the router must determine if there is another
OSPFv2 neighbor on the link.
The OSPFv2 router ID is used to uniquely identify each OSPF-enabled router.
If no OSPFv2 router ID is configured, the highest IP address of any router Loopback
Interface is selected as the OSPFv2 router ID.
If no Loopback Interface is configured, the highest IP address among its active interfaces
is selected as the OSPFv2 router ID.
Areas
In OSPFv2, a single AS (Autonomous System) is considered an IP network.
AS is a group of routers managed by the same organization and administrators.
Dividing the topology into areas reduces router resource consumption and protocol
response time.
Area 0 - Small to medium size networks that use a single area will use the default
OSPFv2 area, which is Area 0.
Other Areas - In larger networks that require more areas, Area 0 will be the backbone
area, and all routers outside that area will be assigned other unique numbers (1, 2, 3,
etc.).
Multiple Areas - As mentioned, OSPFv2 can be divided into multiple areas. The router is
located near the border area, known as ABR (Area Border Router). It is used to establish
connection between OSPF areas and the backbone.


### Textbook — strona 152

Area 2
Areal 10.1.2.0/24
10.1.1.0/24 _ = zy
eS Area 0
>, x 10.1.0.0/24 \ ee
N\A YS
x_n] aie
\
A>
— —
ee wee
Area 3
10.1.3.0/24
OSPFv2 Areas
Areas- Advantages and Disadvantages
Advantages
e Smaller database (LSDB) for each area, saves resources.
e Smaller routing table for each area, saves resources.
e Less traffic on the network due to less exchange of routing information between
routers.
e Reduced resource consumption, since the algorithm calculates the best path for
packets.
e Insmaller areas, updates regarding changes in the topology are distributed faster.
Disadvantages
e CPU utilization is high due to the amount of SPF calculations.
e OSPFv2 requires all areas to be connected to the backbone.


### Textbook — strona 153

Network Topology Example
Networks A, B, and C cannot reach each other, because the routers do not ‘know’ each
other yet. Once OSPF is enabled on all routers, they will start to share routing
information. Next, each outer adds remote networks to its table. For example, R1 will
add Nets B and C. This process is called convergence. Any router can reach any network.
—=
el 0
$010/0 S0i04 L—_——
Net B 192.168.20.0/2
172.16.0.0/30 172.16.0.4/30
a $0/0/0 0/010 —
(}) me) soio/t soi0/t ee) cigoo (i |
es a
Net A 192.168.10.0/24 iad RS Net C 192.168.30.012]
OSPFv2 Configuration
The following example demonstrates how the topology above can be configured to use
OSPFv2 for Dynamic Routing. The commands used for the configuration are listed and
explained after the example.
R1(config)#router ospf 1
R1(config-router)#router-id 1.1.1.1
R1(config-router)#network 192.168.10.0 @.0.0.255 area @
R1(config-router)#network 172.16.0.0 0.0.0.3 area @
R1(config-router)#network 172.16.0.8 0.0.0.3 area @
R1(config-router)#passive-interface gigabitethernet 0/0
R1(config-router)#
00:29:39: %OSPF-5-ADJCHG: Process 1, Nbr 2.2.2.2 on Serial@/0/e
from LOADING to FULL, Loading Done
00:29:59: %OSPF-5-ADJCHG: Process 1, Nbr 3.3.3.3 on Serial@/0/1
from LOADING to FULL, Loading Done


### Textbook — strona 154

router ospf enables OSPF and enters OSPF configuration mode.
router-id sets the router OSPF identifier.
network advertises the network and enables OSPF updates on the network interface.
area sets the interface area ID.
passive-interface disables OSPF updates on the interface.
A log message indicates a link to another OSPF-enabled router.
Verify OSPF on R1
The example below shows R1’s routing table after OSPF finished updating it.
O represents the route learned by the OSPF protocol.
An important feature of OSPF routing, is that if the router finds two equal paths to the
network, both routes will be added to the table, and load balancing will be applied. For
example, 172.16.0.4/30
Rl#show ip route
172.16.0.0/16 is variably subnetted, 5 subnets, 2 masks
€ 172.16.0.0/38 is directly connected, Serial@/0/e
L 172.16.0.1/32 is directly connected, Serial@/0/o
€ 172.16.0.8/30 is directly connected, Serial@/0/1
L 172.16.0.9/32 is directly connected, Serial@/0/1
192.168.10.0/24 is variably subnetted, 2 subnets, 2 masks
€ 192.168.10.0/24 is directly connected, GigabitEthernete/e
L 192.168.10.254/32 is directlv connected.
Show IP Protocols
show ip protocols displays the current protocol settings.
The output includes:
e Router ID
e Area and process ID
e Advertised networks


### Textbook — strona 155

e Passive interfaces
e More
show ip ospf interface displays timer information.
show ip ospf neighbor displays adjacent OSPF-enabled routers.
Rl#show ip protocols
Routing Protocol is "ospf 1"
Outgoing update filter list for all interfaces is not set
Incoming update filter list for all interfaces is not set
Router ID 1.1.1.1
Number of areas in this router is 1. 1 normal @ stub @ nssa
Maximum path: 4
Routing for Networks:
192.168.10.0 @.0.8.255 area 0
172.16.9.0 8.0.6.3 area @
172.16.0.8 @.0.0.3 area @
Passive Interface(s):
GigabitEthernet0/0
Routing Information Sources:
Gateway Distance Last Update
pe oe 110 00:21:40
2.2.2.2 110 00:21:43
3033.3 110 00:21:40
Distance: (default is 110)
Passive Interfaces
Passive Interfaces advertise their addresses, but do not run the OSPFv2 protocol. This
means adjacencies are not formed and “hello” packets are not generated.
Passive interfaces are used to prevent the transmission of routing updates through a
router interface.
Why use Passive Interfaces?
Bandwidth - Dynamic routing updates consume a large amount of bandwidth because
messages are sent in broadcast or multicast, causing switches to broadcast to all ports.
Resources - Devices in the same LAN must process updates up to Layer 4 (transport
layer), and only then discard the update.


### Textbook — strona 156




### Textbook — strona 157

Security - Packet sniffing software can be used to intercept packets that include routing
updates, and redirect traffic by corrupting the routing table with false metrics.
E Lab Assignment — NET-08-LS2 Configuring & Verifying OSPF
4 | Learn how to configure VLANs and trunks.
Perform the instructions in lab document NET-08-L2.


# Chapter 9: VLANs and Trunk


### Textbook — strona 158

| Chapter 9: VLANs and Trunk
Section 1: Virtual LANs
VLAN is a Layer 2 feature that represents a broadcast domain, enabling network
administrators to create several virtual LANs on a single switch.
The LANs are logical divisions (not physical divisions) between local networks.
Multiple ports are configured on the switch and associated with a VLAN, creating a
logical barrier between end components connected to the switch.
Benefits
Security - Separating systems that store sensitive data from the rest of the network
decreases chances that people will gain access to information they are not authorized
to view.
Improvement - Reducing the size of broadcast domains increases the performance and
minimizes unnecessary traffic on the network. VLANs also reduce network cost.
Simplicity - VLANs simplify network management operations and maintenance.
VLAN ID
When traffic passes through a network, it has to be identified to keep it separate from
other traffic. A unique ID identifies a VLAN in the network.
There is a complete separation between virtual networks, whereby users on VLAN 10
cannot access data on VLAN 20.
The valid ID range for VLANs is 1 to 1005. There is also an additional extended range of
valid VLAN IDs from 1006 to 4094.
VLAN Types
Default VLAN - VLANs 1 and 1002-1005 are reserved and added automatically during
device installation. These IDs cannot be removed.
Data VLAN - VLANs 2-1001 are commonly used by users for data exchanges. Their main
function is to tag data traffic with an identifier.


### Textbook — strona 159

Voice VLAN - This VLAN is designed for VoIP (Voice over IP) networks.
Management VLAN - Interface VLAN 1 is a management VLAN that uses a Layer 3
interface called SVI. The management VLAN is also used for remote connection via
protocols such as Telnet and SSH.
Native VLAN - Native VLANs forward untagged traffic, such as DTP and CDP.
Default VLAN Settings
The command show vlan brief shows that the switch is already pre-configured with
VLAN 1, and all ports are associated with it by default. Additional VLANs are available in
the switch configuration. They are reserved and known as Default VLANs.
S1#show vlan brief
VLAN Name Status Ports
1 default active FaQ/1, Fa@/2, FaQ/3, Fad/4
FaQ/5, Fa@/6, FaQ/7, Fad/8
Fa@/9, FaQ/10, Fa@/11, FaQ/12
FaQ/13, Fa@/14, FaQ/15, FaQ/16
Fa@/17, Fa@/18, FaQ/19, Fae/20
Fa@/21, Fa@/22, FaQ/23, Fa/24
Gig®/1, Gigd/2
1002 fddi-default active
1003 token-ring-default active
1004 fddinet-default active
1005 trnet-default active
VLAN Configuration
VLANs should be assigned appropriate names upon creation. The valid ID range for
sending data is 1-1005.
Command:
vian vlan-id | name name
Example:
Switch(config)#vlan 10
Switch(config-vlan)#name HR
Switch(config-vlan)#exit


### Textbook — strona 160

Switchport Modes
The switch interface operates in one of two modes, Access or Trunk, via the switchport
command.
Access - The Access port is used when connecting end devices. For example, when
connecting a PC to a switch, the interface must be configured as an Access port.
Unlike Trunk ports, Access ports only transport traffic to and from the VLAN they are
assigned to.
Trunk - Trunk ports carry traffic for different VLANs and devices. The port sets unique
identifier tags on the frame, using either the 802.1Q or ISL encapsulation protocols. This
ensures that each frame is directed to its intended VLAN.
Switchport Access Mode
Access ports only carry traffic on the VLAN to which they belong, and Access mode
should only be defined on ports connected to end devices, such as PCs.
As a security-related best practice, it is highly recommended to enable Access mode for
a port, before assigning it to a VLAN.
The switchport command is used to configure a port to operate in Access mode.
The assignment of users (end devices, such as PCs) to different VLANs is done by
matching the interconnected interface to the appropriate VLAN.
. ‘ ¢
a © ~ | Assigning multiple ports to a VLAN simultaneously can be done using the
range command.
=
Command:
Switch mode access | switchport access vlan vlan-id


### Textbook — strona 161

Example:
Switch(config)#interface fastEthernet 0/1
Switch(config-if)#switchport mode access
Switch(config-if)#switchport access vlan 10
Switch(config-if)#exit
Switch(config)#interface range fastEthernet @/1-5
Switch(config-if)#switchport mode access
Switch(config-if)#switchport access vlan 10
Verifying VLAN Configuration
By running the show vlan brief command, it is easy to spot the two new VLANs and the
interfaces assigned to them. To display the interface mode, use show interfaces
switchport.
Sl#show vlan brief
VLAN Name Status Ports
all default active Fa@/5, Fa@/6, Fa@/7, Fa0/8
Fa@/9, Fa@/10, FaQ/11, FaQ/12
FaQ@/13, FaQ/14, Fa@/15, Fad/16
FaQ@/17, FaQ/18, Fa@/19, Fae/20
FaQ@/21, FaQ/22, Fa@/23, Fa0/24
Gig®/1, Gigd/2
100 class_A active Fa@/1, Fa0/2
200 class_B active Fa@/3, Fa0/4
1002 fddi-default active
1003 token-ring-default active
1004 fddinet-default active
1085 trnet-default active
Voice VLAN Configuration
The following commands are used to configure an interface to use a VLAN as a Voice
VLAN.
Commands:
Switch mode access | switchport voice vlan vlan-id


### Textbook — strona 162

Example:
Switch(config)#interface fastEthernet @/1
Switch(config-if)#switchport mode access
Switch(config-if)#switchport access vlan 10
Switch(config-if)#switchport voice vlan 101 //assume its pre-
configured VLAN
Switch(config-if)#exit


### Textbook — strona 163

Section 2: Trunking
The Trunk interface is designed to transmit multiple VLAN traffic sessions over the same
connection, and to a remote device, such as a switch or router.
This is done by tagging frames with the source VLAN, ensuring that the Trunk link
forwards the VLAN frames to the same VLAN on another switch.
Common Trunking Protocols
The two most common trunking protocols are ISL and 802.1q.
ISL - ISL (Inter-Switch Link) was developed by Cisco and requires a license to create
Trunking groups of ISLs between adjacent switches.
802.1q - 802.1q was developed by IEEE. It is the default protocol in most switches
today. The same trunk protocol must be used on both ends of the trunk link
(encapsulation).
DTP
DTP is a protocol developed by Cisco to create Trunk links automatically. It operates by
default on all Cisco switches, but can be turned off for security purposes.
DTP automatically “negotiates” for packets between interconnected switches. When
two switches reach an “agreement”, the trunk is established.
DTP can run in one of two dynamic port modes: dynamic auto or dynamic desirable.
Dynamic Auto - This mode, which is the default for each port, is passive and does not
negotiate. Instead, it waits until an explicit request is received from the other side.
Dynamic Desirable - This mode allows DTP negotiation packets to be sent to the switch
on the other side of the connection.
When configuring the interface on a device, each DTP mode enabled on the device will
result in different operational behavior.


### Textbook — strona 164

DTP Mode Configuration

The example below shows the configuration of DTP modes on the interconnected

interfaces of the switches. The command used to set the configuration is switchport

mode dynamic <mode>.

Remember: Dynamic Auto is the default mode.

To display the interface mode, use show interfaces switchport.
S1(config)#interface gigabitEthernet @/1
S1(config-if)#switchport mode dynamic auto
S1(config-if)#exit
S1(config)#interface gigabitEthernet @/1
S1(config-if)#switchport mode dynamic desirable
S1(config-if)#exit

Disabling DTP

Since using DTP can make the switch vulnerable to a VLAN attack, it is recommended to

disable DTP on a port connected to an end device. This is done using the command

switchport nonegotiate.

Configuring the port in access mode is not enough, and nonegotiate is required. To

display the interface mode, use show interfaces switchport.
S1(config)#interface fastEthernet @/1
S1(config-if)#switchport mode access
S1(config-if)#switchport nonegotiate
S1(config-if)#exit
S1#show interfaces switchport
Name: FaQ/1
Switchport: Enabled
Administrative Mode: static access
Operational Mode: down
Administrative Trunking Encapsulation: dotigq
Operational Trunking Encapsulation: native
Negotiation of Trunking: Off


### Textbook — strona 165

Dynamic Trunking Protocol Mode Behavior
The following table lists the results of each mode combination on opposite ends of the
connection.
Dynamic Auto Access Trunk Trunk Access
Dynamic Desirable — Trunk Trunk Trunk Trunk
Trunk Trunk Trunk Trunk (Etta _
Connectivity
Access Access Access pimited we Access
Connectivity
Configuring Trunk Links
The switchport mode trunk command creates IEEE 802.1q trunk links.
Use this command to create a static trunk connection, without using the DTP protocol.
Command:
switchport mode trunk
Example:
Switch(config)#interface gigabitEthernet 0/1
Switch(config-if)#switchport mode trunk
Switch(config-if)#exit
After the switchport creates a trunk link, by default all VLANs are allowed to pass
throught the link, but a set of allowed VLANs can be specified.
Command:
switchport access trunk allowed vlan vlan-id


### Textbook — strona 166

Example:
Switch(config)#interface gigabitEthernet 0/1
Switch(config-if)#switchport mode trunk
Switch(config-if)#switchport mode trunk allow vlan 10
Switch(config-if)#exit
Native VLANs
Native VLANs process untagged frames when they reach switch trunk ports.
The default Native VLAN is VLAN 1.
A best practice regarding Native VLANs is to assign roles to unused VLANs, such as VLAN
100, for security purposes.
The same Native VLAN must be used on both ends of the trunk link.
Important Native VLAN Points
Best Practice - A best practice regarding Native VLANs is to re-assign them to non-
default VLANs, such as VLAN 200, for security purposes. Doing so can, for example,
mitigate Double Tagging attacks.
Identical Native VLAN - The same Native VLAN must be used on both ends of the trunk
link. If not, untagged frames will not be delivered correctly, and the switch’s OS will
send continuous warning messages to the user, in the form of: “%CDP-4-
NATIVE_VLAN_MISMATCH: Native VLAN mismatch discovered on GigabitEthernet0/1
(200), with $2 GigabitEthernetO/1 (1).”
Why are Native VLANs Important?
Without Native VLANs, sending and receiving updates for protocols such as CDP, VTP,
DTP, and STP between interconnected switches would not be possible, since trunk ports
drop untagged frames.


### Textbook — strona 167

Changing Native VLANs
The Native VLAN should be changed because using the default Native VLAN leaves the
switch open to an attack called Double Tagging.
Command:
Switchport trunk native vlan vlan-id
Example:
Switch(config)#interface gigabitEthernet 0/1
Switch(config-if)#switchport trunk native vlan 100
Switch(config-if)#exit


### Textbook — strona 168

Section 3: Inter-VLAN Routing
Although VLANs are logical segments, they still operate within the framework of a
network, which means they are also broadcast domains. Switches (which generally
Operate at Layer 2) cannot move traffic across different VLANs or broadcast domains.
Routing data among different VLANs requires a Layer 3 device (such as a router), which
encapsulates and decapsulates the frames.
Router-On-A-Stick
The most common technique for Inter-VLAN Routing is called Router-On-A-Stick. This
method is effective because it requires only a single physical connection between the
switch and the router, avoiding the need for additional components and costs.
Sub-Interface
Multiple IP addresses - Multiple IP addresses are possible because a router’s single
physical interface is segmented into multiple logical interfaces, called sub-interfaces.
Logical Interface - Each sub-interface is configured with a unique IP address and subnet
mask. Every sub-interface represents a default gateway for a specific VLAN.
Simple rule: The number of VLANs dictates the number of sub-interfaces.

Ri(config)#interface gigabitEthernet 0/0.1

R1(config)#interface gigabitEthernet 0/0.2

R1(config)#interface gigabitEthernet 0/0.3


### Textbook — strona 169

The Switch Side
On the switch side, set the logical interface connected to the router to trunk mode
using the command switchport mode trunk. This enables VLAN tagging towards the
switch.
S1(config)#interface gigabitEthernet 0/1
S1(config-if)#switchport mode trunk
S1(config-if)#exit
Inter-VLAN Routing Configuration
On the router side:
1. Enter the physical interface and enable it.
2. Create a sub-interface.
3. Configure interface encapsulation on 802.1q, and assign the appropriate VLAN ID.
4. Configure the VLAN’s corresponding IP address and mask (default gateway).
5. Repeat this process for every VLAN.
R1(config)#interface gigabitEthernet 0/0
R1(config-if)#
R1(config-if)#exit
R1(config)#interface gigabitEthernet 0/0.1
R1(config-subif)#encapsulation dot1Q 100
R1(config-subif)#ip address
R1(config-subif)#exit
R1(config)#interface gigabitEthernet 0/0.2
R1(config-subif)#encapsulation dot1Q 200
R1(config-subif)#ip address
R1(config-subif)#exit


### Textbook — strona 170

Verify Configuration
Use show ip interface brief to display the interface settings and mode. The show
running-config command shows additional details, such as the interface and its VLAN
ID.
Rl#show ip interface brief
Interface IP-Address OK? Method Status Protocol
GigabitEthernet@/1 unassigned YES unset administratively down down
Vlan1 unassigned YES unset administratively down down
é Lab Assignment — Configuring VLANs and Trunks
—=J | Learn how to configure VLANs and trunks.
m=:
Perform the instructions in lab document NET-09-L1.


# Chapter 10: Diagnostics and Troubleshooting


### Textbook — strona 171

| Chapter 10: Diagnostics and Troubleshooting
Section 1: Troubleshooting Methods
Issues can and will arise, even in networks that were designed using the most advanced
technologies.
This lesson covers the ways network issues can be resolved and the tools that can help
resolve them quickly and efficiently.
An important aspect of network troubleshooting, also described in this lesson, is the
usage of discovery protocols.
Documentation
Quick and efficient troubleshooting is based, in part, on continuous and detailed
network-related documentation.
Network documentation includes physical and logical topological diagrams, network
and end-device backup configuration files, IP and MAC addressing schemes, and
network performance baselines.
Troubleshooting Steps
Gather Information - The first and most important step is gathering information and
symptoms from network devices, end systems, and users.
Isolate the Problem - Based on the symptoms, eliminate variables until a single
problem or a set of related problems is identified as the cause.
Implement a Solution - Consider the severity of the problem and the impact of the
solution. Then begin planning, testing, and documenting possible solutions.
Problem Solved? - If the problem was not solved, repeat steps two and three again, and
deepen the research.
Documentation - Document every step you took in the process.


### Textbook — strona 172

Gathering Information

© Question end users

e Protocol Analyzers (Wireshark, others)

e Physical troubleshooting tools (cable tester, others)

e Network management software

e CMD network commands

e Show and Debug commands

e IP SLA - Monitors network performance in real-time

e Neighbor Discovery Protocols

OSI Troubleshooting Methods

Troubleshooting methods based on the OSI module include the following techniques:
Bottom-Up - In this method, the starting point is at the bottom of the OSI model, the
physical layer. The examination starts from the network's infrastructure, such as cables
and NICs.

Top-Down - In this method, the starting point is at the top of the OSI model, the
application layer. The examination starts with the application itself.
Divide-&-Conquer - In this method, the starting point isn't predefined as in previous
methods. A particular layer is selected and examined, then the layer above it is
examined, and so on. If a layer is faulty, the next one to examine should be the one
below it.

Software Tools

Network Management Software (NMS) provides excellent tools for troubleshooting.
NMS continuously monitors network activity and establishes a clear baseline for
reference purposes. This enables network administrators to promptly identify issues,
and, in some cases, predict the occurrence of such issues.


### Textbook — strona 173

Top IOS Show Commands
Show interfaces - This command outputs a large volume of information, including
interface errors, bandwidth utilization, and interface speed.
Show ip route - This command verifies network reachability, and indicates if routing
protocols are operating as they should.
Show ip interface brief - This command presents only information about interfaces
associated with the IP protocol. The command outputs a detailed summary of interface
status and IP addresses.
Show running-config - This command displays the complete router configuration in use
at that time.
Show start-up config - By default, the initial configuration controlling the system is the
start-up config. When the router boots, it will load start-up config automatically.
Extended Ping and Traceroute
Extended Ping is used to perform advanced checks of network connectivity. It is also
able to change the source IP on the packet leaving the router.
Example:

<Output Omitted>

R2#ping

Protocol [ip]:

Target IP address: 172.16.1.2

Repeat count [5]:

Datagram size [100]:

Timeout in seconds [2]:

Sending 5, 10@-byte ICMP Echos to 172.16.1.2, timeout is 2 seconds:

titi

Success rate is 100 percent (5/5), round-trip min/avg/max = 0/@/3 ms
The Traceroute command discovers the path packets take to a remote destination, and
where routing failures occurred.


### Textbook — strona 174

Section 2: CDP & LLDP
Cisco Discovery Protocol (CDP) is a Layer 2 Cisco proprietary protocol enabled by
default on all Cisco devices. Its purpose is similar to that of NDP.
CDP can be disabled on specific devices or interfaces, for security purposes.
CDP Attributes
Eavesdropping - Since CDP does not encrypt transmitted data, it is vulnerable to
reconnaissance type attacks (such as sniffing) that, for example, allow an attacker to
map the victim's network.
Information Gathering - CDP gathers information on the local device and periodically
sends it to all directly connected devices.
Advertisements - CDP advertisements are special packets that reveal device details to
neighbors also running CDP.
When advertisements are received, they are stored in the neighbor's table.
Advertised Packets
CDP includes the following data in advertised packets:

* Type of device (router, switch)

* Device name

* Interconnected interfaces

* 10S version

* Next-hop IP

* Connection's duplex mode (full, half)
Mismatch Error Detection
CDP includes a unique feature that can detect a protocol-connection mismatch. When
such a mismatch is detected, CDP notifies the network administrator by recording the
incident in a log.
Examples of mismatch types include:
* Native VLAN mismatch
* Duplex mismatch


### Textbook — strona 175

Intervals
Advertisement messages also include the following intervals, which can be modified.
Advertisement packets are sent every 60 seconds to all directly-connected devices.
When a device does not receive Hello packets from its neighbor for 180 seconds, it will
consider the neighbor "dead," and remove it from its CDP neighbor table.
CDP Commands
Because CDP is not secure or encrypted, it is easy to eavesdrop. If necessary, the
protocol can be turned off entirely on the device or on selected interfaces.
It is recommended to enable CDP only for port interconnection with other network
devices.
cdp run
Enable/disable CDP on the device.
Command:
cdp run | no cdp run

Examples:

Switch(config)#cdp run

Switch(config)#no cdp run


### Textbook — strona 176

cdp enable

Enable/disable CDP ona specific interface.
Command:

cdp enable | no cdp enable

Examples:

Switch(config)#interface fastethernet 0/1

Switch(config-if)#cdp enable

Switch(config)#interface fastethernet 0/1

Switch(config-if)#no cdp enable
Show cdp neighbors
The show cdp neighbors command displays all connected devices that CDP can
communicate with via its advertisement messages. It also displays additional
information, such as IP address and IOS version.
Topology example:

——s0-2
_ Q ——

= Switch? ~ —_—
2960-247 ai ao 2960-24TT
Senda ee a Switch3

a _
2960-24TT
Switch4

Example:
Switchl#show cdp neighbors
Capability Codes: R - Router, T - Trans Bridge, B - Source Route Bridge
S - Switch, H - Host, I - IGMP, r - Repeater, P - Phone
Device ID Local Intrfce Holdtme Capability Platform Port ID
Switch Fas 0/2 101 S 2960 Fas @/1
Switch Fas 0/1 104 S 2960 Fas @/1
Switch2 Fas @/2 161 S 2960 Fas 9/1
Switch4 Fas @/1 164 S 2960 Fas 9/1


### Textbook — strona 177

LLDP
LLDP (Link Layer Discovery Protocol) is a Neighbor Discovery Protocol similar to CDP
that was developed by the IEEE.
LLDP is an industry-standard protocol, meaning it is not proprietary and can operate on
any network device.
Although LLDP is not enabled by default on Cisco devices, it is fully supported.
Default LLDP messages also include intervals that can be modified as necessary.
LLDP advertisement packets are sent to LLDP neighbors at periodic intervals, which is 60
seconds by default. You can increase or decrease the interval as necessary. The default
interval recommended by IEEE is 30 seconds, but any value between 5 and 300 seconds
can be specified.
When a device does not receive Hello packets from its neighbor for 120 seconds, it will
consider the neighbor "dead", and remove it from its LLDP neighbor table.
LLDP Commands
IIdp run
Enable/disable LLDP on the device.
Command:
IIdp run | no Ildp run
Examples:
Switch(config)#lldp run
Switch(config)#no lldp run


### Textbook — strona 178

Show Ildp neighbors
The show Ildp neighbors command displays all connected LLDP devices that LLDP was
able to communicate with via its advertisement messages.
Topology Example:
_ ee
—_—_— 2960-24TT _—— .

— a Switch2 = 7 OU
2960-24TT 2a, ao 2960-24TT
Switch1 ~~ =- ce

~ _—
“te an
—__
2960-24TT
Switch
Code Example:
Switchl#show lldp neighbors
Capability codes:
(R) Router, (B) Bridge, (T) Telephone, (C) DOCSIS Cable Device
(W) WLAN Access Point, (P) Repeater, (S) Station, (0) Other
Device ID Local Intf Hold-time Capability Port ID
Switch2 Fa0/2 120 B Fa@/1
Switch4 Fa@/1 120 B Fa@/1


### Textbook — strona 179

Section 3: Syslog — Log Events
Syslog is a standard for logging messages. Each device records actions and events that
occur, similar to a private diary. Among other tasks, network administrators need to
monitor the network to ensure smooth, errorless functionality. Monitoring the network
improves troubleshooting capability and helps identify issues such as device health and
network load.
Why are logs useful?
System notification logging increases a network administrator's awareness of hardware
or software malfunctions, service status, and security accountability. In some cases, logs
can be used to predict component failures. Log analysis can help administrators
troubleshoot the system, and can be useful to information security experts when
investigating security breaches.
Syslog messages can be stored locally on the device, or on a Syslog server in the
network.
Device Logs
The following points should be considered when working wth device logs:
e Log storage takes up space, and can, in some cases, degrade system performance.
e Log message count is limited due to buffer size.
e Collecting logs from separate devices can take a long time.
e RAM is erased upon device power off.
Syslog Server
A Syslog Server is a computer that runs Syslog software. The Syslog software
concentrates logs from all devices (PC, router, etc.) on the network into one centralized
location, which makes management and backup easier. It also offers a convenient user
interface. This way of working is more efficient than storing logs in RAM.
Many free and enterprise versions of Syslog exist, such as the Kiwi Syslog Viewer.


### Textbook — strona 180

Storage Methods
Logging Buffer - A Logging Buffer is a predetermined storage space allocated on RAM
for Syslog messages.
Console Line - Console Line is a method of viewing messages locally via the console
window.
Terminal Line - Terminal Line is a method of viewing messages via a CLI program (such
as Putty).
Syslog Server - If a Syslog Server is configured on the device, the device will send all
Syslog messages to the server over the UDP 514 port.
Messages
Status - Network devices generate Syslog status messages in response to events in the
network (such as when the status of a device changes, login attempts, etc.).
Fields - Fields in Syslog messages include:

Severity — The urgency of the message.

Facility — Specifies in which component of the device the message originated.
Severity & Facility
Syslog messages include several pieces of information, of which the most important
are:
Message Severity - The urgency of the log message is represented by its severity level,
which is a number from 0 to 7. Level 0 indicates emergencies, and 7 indicates system
debugging. The values also represent critical malfunctions and system warnings.
Message Facility - The facility parameter indicates the source that generated the
message, which, for example, can be a network card or routing protocol. The facility can
be a hardware component, protocol, or system service.


### Textbook — strona 181

Message Severity
The severity of a Syslog message is represented by a number called the Syslog Security
Level. The lower the number, the higher the severity.
Message Type Severity Explanation
Emergency Level 0 System unusable
Alert Level 1 Immediate action needed
Critical Level 2 Critical condition
Error Level 3 Error condition
Warning Level 4 Warning condition
Notification Level 5 Normal, but significant
Information Level 6 Informative message
Messages related to the
Debug Level 7 es
debugging process
Log Message Format
7 Log Event 7 7 " i t
Dec 28 19:01! %LINK} -5- | CHANGED: | Interface GigabitEthernet@/1, changed state to up!
' 1 fo2 tsi oa H 5 H
</>
1. Timestamp: Records the time and date of the log (this service is disabled by default,
and should be enabled once to update the system’s time).
2. Facility: The category of the source that created the log message. In the example
above, the link represents the state of the router's hardware ports.
3. Severity: The severity level, which in the example above, indicates that it is a
notification message.
4. Mnemonic: A device-specific code that identifies the log message.
5. Text Description: The log/event description and other details.
Messages in the console consist of the following:
*Dec 28 19:01 %LINK-5-CHANGED: Interface GigabitEthernet@/1, changed state to up


### Textbook — strona 182

Syslog Configuration Commands
Command Meaning
Logging host [IP address] Sets the log server.
| Determines what log severity levels to
Logging trap
send to the server.
Service timestamps lo
; Ps (08 Sends alerts with time included.
datetime msec
| Shows system messages on the screen
Terminal monitor ;
of a remote connection (Telnet, SSH).
Shows system messages on the screen
Logging console of the console connection (enabled by
default).
Saves system messages to RAM
Login buffered ” B
(enabled by default).


### Textbook — strona 183

Syslog Config Example
The logging host command sets the destination IP of the Syslog server, to which all logs
are sent. The logging trap command sends all severity log levels to the server (levels 7
and above). The remaining commands in the example below are used to add time
records.
R1(config)#logging host 172.16.0.250
R1(config)#logging trap debugging
R1(config)#logging userinfo
R1(config)#service timestamps log datetime msec
R1(config)#do show logging
<Output Omitted>
ESM: @ messages dropped
» 9 message lines logged
(udp port 514, audit disabled,
authentication disabled, encryption disabled, link up),
2 message lines logged,
@ message lines rate-limited,
@ message lines dropped-by-MD,
xml disabled, sequence number disabled
£iltaning dinahtad


### Textbook — strona 184

Server Configuration
To simulate Syslog in your packet tracer environment, first create the server.
Open the server configuration window, search for Syslog, and make sure that it is
turned on.
The IP address will be used in the host configuration statement.
Physical Config _Senmices_ Desktop Programming Attributes.
SERVICES svsea
Sune Syslog
DHCP ne
ST Senice @on Oo
Pqer TTF Time Hoanane —
1 “ONS
fs canst %SYS-5-CONFIG_E Configur.
AAA
: ae s eee or S6LINK-5-CHANGED: Interfac
= ae 3° 1229821 SULINEPROTO 5. UPOOWE L
at tl IoT 4)- 192.168.2.1 ‘%LINK-5-CHANGED: Interfac.
VM Management
Saas Pie 1eeB2 1 ‘%LINEPROTO-5-UPDOWN: L.
IsAk321
-
Server-PT
Syslog
Clear Log
C1 tep
Syslog Server Service Activation


### Textbook — strona 185

Section 4: Network Time Protocol (NTP)
NTP (Network Time Protocol) is responsible for the synchronization of all clocks in
devices on the network.
NTP is a client-server protocol. All clients must be configured with the NTP server's IP
address, so that they will all have the same date and time.
Cisco routers and switches can have the date and time set in one of following ways:
Manual configuration — This method requires manual setting of the time and date on
each device on the network.
It is not recommended to work this way for various reasons, among which is the lack of
scalability for large networks. (Setting the clock in every device will waste valuable
time.)
Collective NTP configuration — This method requires an available and configured NTP
server. Only the server's IP address needs to be set on network devices.
This ensures that all devices on the network will be set to the most accurate time and
date automatically.
Cisco routers can be configured to act as NTP servers. End devices on the network are
assigned the NTP server's IP address, and sync their clocks according to the NTP.
Since the entire network depends on the NTP server, it is very important to ensure that
the NTP clock is as accurate as possible.
How NTP Operates
Cisco routers and switches (and many other devices around the world) use NTP to
determine the date and time.
Accurate timestamps are extremely important for troubleshooting, managing, and
securing networks.
NTP operates with UDP, on port 123, and is defined in RFC 1305.


### Textbook — strona 186

Stratum Model - Stratum levels define the distance from high-precision reference clocks
which begin with stratum 0, to devices connected hierarchically. Servers linked to the
reference clock are Stratum 1, devices that receive the time from the servers are
Stratum 2, and so on. To avoid delays, a maximum of 15 levels are allowed.
Services - Accurate time settings are crucial for many protocols and device functions.
For example, DHCP leases and Syslog events are time-sensitive services. Timestamps
are extremely important for troubleshooting, management, and network security.
Local Clock Configuration
Configuring a clock on the router locally, without using an NTP server.
Command:
Router#clock set hh:mm:ss Day<1-31> Month<January-December> Year<1993-2035>
Example:
Router>enable
Router#clock set 09:21:14 16 January 2019
Setting the clock manually has two drawbacks: a device can become out of sync if it is
shut down, and setting each and every device clock can waste valuable time.
Server Configuration
Configuring a Cisco device to sync its clock with an external NTP server.
Command:
Router(config)#ntp server <ip_address>
Example:
Router>enable
Router#configure terminal
Router(config)#ntp server 172.30.226.100


### Textbook — strona 187

When configuring a device as an NTP server, the number after "master" in the
command (optional) represents how many hops the NTP server is from an accurate
time source. Value (stratum) n servers are n hops away from an accurate time source
(such as a radio or atomic clock). The default is 8.
Command:
Router(config)#ntp master <1-15>

Example:

Router>enable

Router#configure terminal

Router(config)#ntp master
Logging Alerts with Time
Logging alerts with time included.
Command:

Router(config)#service timestamps log datatime msec

Example:

Router>enable

Router#configure terminal

Router(config)#service timestamps log datetime msec

é Lab Assignment — Configure NTP and Syslog
—/f | Answer questions based on material covered in the lesson, and understand
= | how to configure NTP and Syslog servers.
Perform the instructions in lab document NET-10-L1.


# Chapter 11: Access Control List


### Textbook — strona 188

| Chapter 11: Access Control List
Section 1: ACL Overview
ACL (Access Control List) is a rule-based feature that allows network administrators and
engineers to configure basic traffic filtering.
ACL is a series of commands that determine, based on information in the packet
header, whether to drop the packet or forward it.
ACL vs Firewall
Similar to ACL, firewalls are used to protect networks from unauthorized use.
A difference between them is that firewalls are placed at the entry and exit points of
the network architecture, to analyze all traffic coming into the network, while ACLs are
placed wherever they are needed in the network.
Advantages of Configuring an ACL on a Device
Network Performance - Network performance can be improved by allowing only
relevant services to communicate with devices across the network.
For example, restricting the network to block video traffic can improve network
performance.
Securing the Network - In a network environment, users may be restricted from
accessing sensitive services.
ACL provides a basic level of network security by allowing some hosts to access parts of
the network, while preventing others from accessing the same parts.
Restriction Capability - ACLs can also restrict the following:
e Routing protocol advertisement messages
e Packets from security protocols
e Packets from other protocols, such as ICMP


### Textbook — strona 189

Standard and Extended ACLs
There are Standard ACLs and Extended ACLs, with the difference in the parameters
examined in the process.
Standard ACLs examine only the source IP address when implementing restrictions.
Cisco recommends to place this type of ACL as close to the destination device as
possible.
Extended ACLs filter packets according to protocol type, source or destination IP
address, and source or destination port. Cisco recommends to place this type of ACL as
close to the source as possible.
Traffic Direction
Traffic direction must be specified on an interface when configuring ACL. The direction
can be ether inbound or outbound. This is done so that the router will implement the
proper restrictions when examining the source network and destination.
Inbound ACL - Configures the ACL for inbound traffic. The router will examine incoming
traffic to the interface.
Outbound ACL - Configures the ACL for outbound traffic. The router will examine
outgoing traffic from the interface.
Wildcards
Wildcards are inverted subnet masks that can be used in statements of both Extended
and Standard ACLs.
For example, 255.255.255.0
(binary equivalent = 11111111.11111111.11111111.00000000)
This inverts to a wildcard mask of 0.0.0.255
(binary equivalent = 00000000.00000000.00000000.11111111)


### Textbook — strona 190

ACL Order
Among other important guidelines, the ACL order is crucial.
Check Order - ACEs (Access Control Entries), which represent the order of statements in
the ACL, are essential and must be planned carefully. The router checks each packet’s
parameters against the ACEs to find a matching condition. When a condition is met, the
ACL will be applied, and additional ACEs will be ignored.
Implicit Deny - At the end of every ACL, there is an invisible statement called implicit
deny. When no match is found for a packet, the implicit deny statement is applied.
Note: Each ACL must have at least one Permit statement!


### Textbook — strona 191

Section 2: Standard ACL Implementation
Standard ACLs are placed as close to the destination as possible. Cisco set this rule
because placing standard ACLs at the source of traffic will prevent communication with
any network hosting interfaces to which the ACL applies.
Standard ACLs filter traffic only according to the source IP address.
Named or Numbered ACLs
ACLs can be assigned unique names or numbers.
Standard Named Access Control Lists allow unique names and numbers to be assigned
to ACLs.
The Standard Numbered ACL range is 1-99 and 1300-1999.
Standard Numbered ACL Command
Command F F f 1 :
Router(config)# i access-list <access-list-number> | <deny | permit |remark>i <source-address>! <source-wildcard>
0 : 1 ! 2 ! 3 ! 4 i 5
</>
0- To run the command, you must be in terminal configuration mode.
1 - Initial syntax to configure a Standard ACL.
2 - Decimal number from 1 to 99, or 1300 to 1999 (only for Standard ACLs).
3 - Deny - denies access if the conditions match, Permit - permits access if the
conditions match, Remark - adds a remark about entries.
4 - IP of the network or host from which the packets were sent. You can specify any
instead of using a 32-bit address.
5 - 32-bit wildcard mask that will be applied on the source.
Example:
R1(config)# access-list 10 permit 192.168.10.0 @.0.0.255


### Textbook — strona 192

Standard ACL Scenario
Scenario #1:
A network administrator decided that new users on network 10.0.0.0/24 will not have
access to the server network, but will be able to communicate with neighboring
network 192.168.0.0/24
Scenario #2:
After malicious software was discovered on Host A, an administrator decided to
temporarily block access from the host to 10.0.0.0/24, until the threat is removed.
ml
—M™e:s nh =
= vets
Host A GigO/1 Gigd/2 10,0.0.10/24
192.168.0.10/24 bom] pra
+—————-*,
ans ‘
? Host C
10.0.0.20/24
=] al
— <=
DNS Server FIP Server
172.16,1.1/24 172.16,1.2/24
Standard Numbered ACL Configuration Example
The following ACL configuration example is based on scenario #1 above.
Step 1 - Create a numbered ACL using the access-list command.
Step 2 - Choose the interface for which the ACL will apply, using the interface command.
Step 3 — The ip access-group 1 out command links ACL 1 to the Gigabitethernet 0/3
interface in the outbound direction.


### Textbook — strona 193

R1(config)#access-list 1 deny 10.0.0.0 @.0.0.255
R1(config)#access-list 1 permit any
R1(config)# interface Gigabitethernet 0/3
R1(config-if)#ip access-group 1 out
R1(config-if)#exit
Standard Named ACL Configuration Example
The following ACL configuration example is based on scenario #2 above.
Step 1 - Use the ip access-list standard command to create a named ACL.
Step 2 - In ACL configuration mode, create Deny and Permit ACE statements.
Step 3 - Apply the ACL on an interface using the ip access-group command, and specify
the traffic direction (in or out).
R1(config)# ip access-list standard
R1(config-std-nacl)#deny host 192.168.0.10
R1(config-std-nacl)#permit any
R1(config-std-nacl)#exit
R1(config)#interface Gigabitethernet 0/2
R1(config-if)#ip access-group out
R1(config-if)#exit
Verify ACL Settings
ACL rules can be verified in different ways, one of which is by searching the running-
config file using an include filter.
Run show running-config to display on which interface each ACL is applied.
The show access-list command can also be used.


### Textbook — strona 194

R2#
Standard IP access list Block_Host_A
10 deny host 192.168.0.10
28 permit any
Standard IP access list 1
10 deny 10.0.0.0 0.0.0.255
28 permit any
R1#
interface GigabitEthernet0/2
ip address 10.0.0.15@ 255.255.255.0
ip access-group Block__Host_A out
!
interface GigabitEthernet0/3
ip address 172.16.0.15@ 255.255.255.080
ip access-group 1 out
E Lab Assignment — Implement Standard and Extended ACLs (Tasks 1-3)
— Jf | Configure and verify standard and extended ACLs.
—
Perform the instructions in lab document NET-11-L1.


### Textbook — strona 195

Section 3: Extended ACL Implementation
Extended ACLs filter packets based on the following attributes:
© Source and destination IP addresses.
e Source and destination Layer4 protocols (UDP and TCP).
e Protocol type or number. For example: IP, HTTPS, 80, etc.
Extended ACLs use the following range of numbers: 100 to 199 and 2000 to 2699.
Configure Extended ACLs as close as possible to the source of the traffic being filtered.
Doing so ensures that traffic will be denied, and prevented from traversing the network
infrastructure.
It’s important to understand that even if the ACL is not placed as close as possible to
the source, the ACL will still operate as it should.
Standard Numbered Extended ACL Configuration
The numbers Extended ACLs use are 100-199 and 2000-2699.
In the protocol field, insert the name of the internet protocol, such as UDP, TCP, or
ICMP.
Source — The origin of the packet.
Destination — Where the packet is being sent to.
Operator — Compares source or destination ports, and can be It (less than), gt (greater
than), eq (equal), neq (not equal), or range (inclusive range).
Port is the number or name of an active TCP or UDP port.


### Textbook — strona 196

Example:
Router(config)#access-list <access-list-number> <deny|permit|remark>
<Protocol> <source-address> <source-wildcard> <operator> <Port
Number\Name> <destination-address> <destination wildcard> <operator>
<Port Number\Name>
Ex1.
R1(config)#access-list 180 deny tcp 192.168.10.1 0.0.0.255 192.168.10.2
@.0.0.255 eq ftp
Ex2.
R1(config)#access-list 181 permit tcp 192.168.10.0 @.0.0.255 any eq www
//Appling on an interface
R1(config)#interface f0/0
R1(config-if)#ip access-group 18@ out
R1(config-if)#ip access-group 181 in
Standard Named ACL Configuration
Step1: Define a Named Access List using the command ip access-list extended.
Step2: Specify the conditions (Permit/Deny).
Step3: In configuration mode, choose an interface on which to apply the ACL, and apply
the ACL using ip access-group (in the correct direction).
Verify that the ACL is configured correctly using the show access-list command, and
save the configuration in the startup-config file.
Example:
R1(config)#ip access-list extended <name>
R1(config-ext-nac1)# <deny|permit|remark> <Protocol> <source-address>
<source-wildcard> <destination-address> <destination-wildcard> <operator>
<port number\name>
Ex.
R1(config)# ip access-list extended WEB
R1(config)# permit tcp 192.168.10.0 @.0.0.255 any eq 443
R1(config)# permit tcp 192.168.10.@ @.0.0.255 192.168.11.1 @.0.0.255 eq
telnet
R1(config)#interface f0/e
R1(config)# ip access-group WEB


### Textbook — strona 197

Configuration Display Methods
ACL rule verification can be implement in several ways, one of which is to search the
running-config file using an include filter.
The output of the command show running-config | include access-list shows
configured Numbered and Named ACLs.
The command show access-list can also be used.
Example:
Rl#show access-lists
Extended IP access list 180
10 deny tcp 192.168.10.0 0.0.0.255 192.168.10.0 @.0.0.255 eq ftp
Extended IP access list 181
10 permit tcp 192.168.10.0 @.0.@.255 any eq www
Extended IP access list WEB
10 permit tcp 192.168.10.0 @.0.0.255 any eq 443
280 permit tcp 192.168.10.0 0.0.0.255 192.168.11.0 @.0.0.255 eq telnet
Extended ACL Examples
Scenario #1:
Due to new procedures and changes in the organizational structure, Hosts A and C are
not allowed to communicate.
Scenario #2:
The network administrator decided that the enterprise department on network
10.0.0.0/24 cannot access the FTP service on the FTP server, due to the risk of exposing
sensitive information. It can however receive services from the same server, such as
DHCP.


### Textbook — strona 198

—,
CI a
—— ———/ =i ae)
—M™*s:s nh =
——
Host A Gigo/i Seay Gigo/2 er
192.168.0,10/24 Sew pascal:
Gig0/3 ws
| =
-—— >
—/ ae
10.0.0.20/24
= =|
= Le)
DNS Server FTP Server
172.16.1.1/24 172.16.1.2/24
Extended Numbered ACL Configuration Example
The following extended ACL configuration example is based on scenario #1 above.
Step 1 - Create a numbered ACL using the access-list command.
Step 2 - Choose the interface for which the ACL will apply, using the interface
command.
Step 3 — The ip access-group 1 in command links ACL 1 to the GigabitEthernet 0/1
interface in the inbound direction.
R1(config)#access-list 100 deny ip host 192.168.0.1@ host 10.0.0.20
R1(config)#access-list 100 permit ip any any
R1(config)#interface gigabitEthernet 0/1
R1(config-if)#ip access-group 100 in
R1(config-if)#exit


### Textbook — strona 199

Extended Named ACL Configuration Example
The following extended ACL configuration example is based on scenario #2 above.
Step 1 - Use the ip access-list standard command to create a named ACL.
Step 2 - In ACL configuration mode, create Deny and Permit ACE statements.
Step 3 - Apply the ACL on an interface using the ip access-group command and specify
the traffic direction (in or out).
R1(config)#ip access-list extended
R1(config-ext-nacl)#deny tcp 10.0.0.0 @.0.0.255 host 172.16.1.2 eq 21
R1(config-ext-nacl)#deny tcp 10.0.0.0 0.0.0.255 host 172.16.1.2 eq 20
R1(config-ext-nacl)#permit ip any any
R1(config-ext-nacl)#exit
R1(config)#interface gigabitEthernet 0/2
R1(config-if)#ip access-group in
R1(config-if)#exit
Verify ACL Settings
ACL rules can be verified in various ways, one of which is by searching the running-
config file using an include filter.
Run the show running-config command to display on which interface each ACL is
applied. The show access-list command can also be used.
R2#
Extended IP access list 100
10 deny ip host 192.168.0.1@ host 10.0.0.20
20 permit ip any any
Extended IP access list Block_FTP
10 deny tcp 10.0.0.0 0.0.0.255 host 172.16.1.2 eq 21
20 deny tcp 10.0.0.0 0.0.0.255 host 172.16.1.2 eq 20
3@ permit ip any any
R1i#
interface GigabitEthernet0/1
ip address 192.168.0.15@ 255.255.255.0
ip access-group 100 in
!
interface GigabitEthernet0/2
ip address 10.0.0.15@ 255.255.255.0
ip access-group Block_FTP in


# Chapter 12: Infrastructure Services


### Textbook — strona 200

é Lab Assignment — Implement Standard and Extended ACLs (Tasks 4-6)
—=/ | Configure and verify standard and extended ACLs.
m=:
Perform the instructions in lab document NET-11-L1.


### Textbook — strona 201

| Chapter 12: Infrastructure Services
Section 1: DHCP Overview
To communicate with each other, all devices on a network must have a unique IP
address.
Network administrators will often be responsible for assigning static IP addresses to
network components, such as routers, servers, firewalls, etc.
Assigning a static IP address for every endpoint in an organization can be time-
consuming. Many endpoints do not require a static IP address at all.
The solution is to use DHCP (Dynamic Host Configuration Protocol).
DHCP is designed to simplify the process of IP address allocation for devices on the
network. A DHCP server is configured with a range of IP addresses, which it allocates to
devices on the network.
DHCPv4 dynamically allocates IPv4 addresses to devices in the network, including DNS
server address and default gateway addresses.
Routers and DHCP servers also have the ability to allocate IP addresses using the DHCP
protocol.
DHCP Characteristics
OSI Model Layer - DHCP operates in the Application Layer of the OSI model.
Logical Ports - DHCP works with the UDP protocol and uses ports 67 and 68.
Versions - DHCP supports both IPv4 (DHCPv4) and IPv6 (DHCPv6).
DHCP Allocation Methods
Dynamic Allocation - The DHCP server assigns an available IP address to the client from
its address pool, for a limited amount of time. The client “leases” the address from the
server, for a period set by the administrator. At the end of the lease, the client requests
an extension or a new address.


### Textbook — strona 202

Automatic Allocation - As in the Dynamic Allocation method, the client receives a
random available IP address. But in this case, there is no time limit for the address. The
client does not have to renew the lease for the address it was assigned.
Reservation Address - The network administrator configures the DHCP server to
allocate a specific IP address to a selected client device. The address is reserved for a
specific device in advance, based on its MAC address. This method is useful for devices
such as network printers.
Lease Process
DHCP Discover - A client device that requires an IP address sends a discover message in
broadcast, to search for a DHCP server on the network. They communicate using Layer
2 and Layer 3 broadcast addresses.
DHCP Offer - After the server receives the discover message, it reserves an available IP
address and offers it to the client, along with the lease details. DHCPv4 sends a message
to the requesting client to reserve an available I|Pv4 address.
The server also creates an ARP entry with the requesting client MAC address.
DHCP Request - The client responds to the offer by sending a response with accept or
decline.
DHCP Acknowledgment - After receiving an accept message, the server sends
DHCPACK, with all the necessary configuration information.
Lease Renewal Process
DHCP Request - Before a lease expires, the client sends a DHCPREQUEST message
directly to the DHCPv4 server that originally offered the IPv4 address.
DHCP Acknowledgement - Upon receiving the DHCPREQUEST message, the server
verifies the lease information by returning a DHCPACK.
Messages can be sent as Unicast or Broadcast.


### Textbook — strona 203

DHCPv6
Unlike IPv4, IPv6 uses multiple types of addresses from different hosts. DHCPv6 was
developed due to the usage in networks of various address formats and prefixes,
instead of subnet masks.
DHCPVv6 also supports more allocation methods than DHCPv4. For example, an IPv6
host can automatically generate an IP address internally, using stateless address auto-
configuration (SLAAC), or the EUI-64 process for link-local addresses.
More information about DHCPvé6 is provided in RFC 2460.
DHCPv6 Allocation Methods
SLAAC - In this method, the device can obtain an IPv6 global address without the
services of a DHCP server. The device uses ICMPv6 for advertisement messages, to
provide addressing and other configuration information that would normally be
provided by a DHCP server.
Stateless DHCPV6 - The stateless DHCPv6 method informs the client to use the
information in the RA (Router Advertisement) message for addressing, while additional
configuration parameters are available from a DHCPv6 server. The client will then
communicate with a stateless DHCPv6 server to obtain information not provided in the
RA message, such as a DNS server address.
Stateful DHCPv6 - Similar to DHCPv4, but both addressing information and
configuration need to be obtained from a DHCPV6 server.


### Textbook — strona 204

DHCP Router vs Server
Router Server
Used in smaller networks and .
q . Used in larger networks and
SMBs (small and medium-sized .
. enterprises.
businesses).
Easy to manage. Easy to manage.
Requires knowledge of Cisco IOS Requires general knowledge of servers,
and the relevant configuration. especially DHCP servers.
Relatively low cost, since no device _— Relatively expensive, especially if the
is required other than the existing organization needs to buy a dedicated
router. server to act as the DHCP server.


### Textbook — strona 205

Section 2: DHCP Implementation
Configuring a DHCPv4 Client
Configuration Steps:
Step 1: Exclude addresses from the DHCP pool.
Run ip dhcp excluded-address to reserve an IP address for the default gateway or
statically configured servers.
Step 2: Set up a DHCP pool of addresses using ip dhcp pool
Step 3: Configure specific tasks, such as the default gateway, DNS server, domain name,
etc.
Note: The lease 0 4 30 (days, hours, minutes) will not work in Packet Tracker. It does
operate on an authentic Cisco device.
R1(config)#ip dhcp excluded-address 192.168.0.1
R1(config)#ip dhcp excluded-address 192.168.0.100 192.168.0.150
R1(config)#ip dhcp pool LAN1
R1(dhcp-config)#network 192.168.0.0 255.255.255.0
R1(dhcp-config)#default-router 192.168.0.1
R1(dhcp-config)#dns-server 192.168.0.105
R1(dhcp-config)#domain-name Cyber.com
R1(dhcp-config)#lease ® 4 30
R1(dhcp-config)#exit
Verify DHCP Settings
Several commands can be used to verify and troubleshoot DHCP settings:
Show ip dhcp pool - Displays pool settings.
Show ip dhcp binding - Displays the client list, with IP, MAC address, and lease
expiration.
Show ip dhcp conflict - Displays IP conflicts detected during DHCP negotiation.


### Textbook — strona 206

R1#show ip dhcp pool

Utilization mark (high/low) : 100 / @

Subnet size (first/next) : 0/20

Pending event : none

1 subnet is currently in the pool

Current index IP address range Leased/Excluded/Total

192.168.0.1 3 /2 / 254
Configuring DHCPv4 Server
Addresses can be excluded from the DHCP pool during service configuration, using the
ip dhcp excluded-address command.
This can be done, for example, to reserve an IP address for the default gateway.
Set up a DHCP pool of addresses using the command: ip dhcp pool pool-name
Configure specific tasks like default-router and DNS-server. Tasks such as default-router
must be configured, while other tasks, such as DNS, do not have to be configured.
Example:

//Example: Suppose your router connects to 4 PCs using a switch, and you

want to configure them using DHCPv4, the network address is

192.168.0.0/24 with excluded IP address 192.168.0.1. Configure the

appropriate DHCP pool:

Router#configure terminal

Router(config)#ip dhcp excluded-address 192.168.0.1

Router(config)#ip dhcp pool poolone

Router(dhcp-config)#network 192.168.0.0 255.255.255.0

Router (dhcp-config)#default-router 192.168.0.1

Router (dhcp-config)#dns-server 192.168.0.1

Router(dhcp-config)#domain local.host

Router (dhcp-config)#end


### Textbook — strona 207

Configuring DHCPv4 Relay
DHCP relay is used by devices to obtain addresses from a remote network using
broadcast messages.
Broadcast messages are not transmitted to other networks. When a client sends
DHCPDiscover, the router acts as a relay and forwards the message directly to the
server in Unicast.
The command to set the DHCPv4 relay is ip helper-address.
Example:

//Example: Suppose your DHCPv4 server is located on another subnet

than that of your PC. The router needs to be enabled with Cisco

helper to process the request:

Router#configure terminal

Router(config)#interface ge/e

Router(config-if)# ip helper-address 192.168.11.6

Router (config-if)#

b Lab Assignment — Configure DCHPv4 on a Cisco Router
—=/ | Setup a DHCP service on a Cisco router, and make sure all devices on the
mm | network receive addresses dynamically. The lab also helps understand the
DHCP Relay concept
Perform the instructions in lab document NET-12-L1.


### Textbook — strona 208

Section 3: NAT Overview
Network Address Translation (NAT) is an essential protocol and service that converts a
private address to a public address, and vice versa.
NAT is usually enabled on a firewall or router device at the edge of the local network,
and the beginning of the outside network.
Most home-based, corporate, or local network uses private IP addressing which cannot
be used on the public internet. NAT takes the private IP address and translates it toa
public IP address to be used on the public internet. When the data returns, it is
translated back to a private IP address.
The NAT process is transparent to users, and any evidence of its operation is stored ina
special table in the NAT-enabled device. This helps hide the internal network from the
internet, and adds an extra layer of security.
Private IP Space
According to RFC 1918, three address spaces are reserved for devices in a private
network (LAN). Their usage is unlimited and they can be implemented freely.
Private IP Range

IP Subnet

10.0.0.0-10.255.255.255 255.0.0.0

172.16.0.0-172.31.255.255 255.255.0.0

192.168.0.0-192.168.255.255 255.255.255.0
NAT Advantages and Disadvantages

Pros Cons


### Textbook — strona 209

Conserves space allotted for IPv4 Accessing internal resources requires
addresses, preventing address special configuration and makes
depletion via PAT. troubleshooting more challenging.
Network flexibility and connection Difficult to troubleshoot issues
reliability. remotely.
Using tunneling protocols, NAT
. interferes with integrity checks,
Extra layer of network security. ; i. 7
because it modifies values in the
headers.
NAT64
NAT64 (Network Address Translation IPv6 to IPv4) technology facilitates
communication between IPv6-only and IPv4-only hosts and networks.
This solution allows enterprises and ISPs to accelerate IPv6 adoption, while
simultaneously handling IPv4 address depletion.
NAT Methods
Static NAT — one-to-one NAT. A permanent mapping of a single private IP to a specific
single public address. This method is not meant to conserve IPv4 addresses, but to
allow access to internal resources from an outside network.
Dynamic NAT — many-to-many NAT. This method is also not meant to conserve
addresses. Multiple IP addresses are mapped dynamically by the router to a pool of
public addresses. The conversion is done on a first-come, first-serve basis.
PAT (or NAT Overload) — many-to-one NAT. This is the most common method, and is
used to conserve addresses. In this method, multiple private IP addresses are converted
to a single public address. To distinguish the traffic from different devices, the source
port number is also used for the inside global address.
Theoretically, the maximum number of private addresses that can be translated to one
public address is 65,536.


### Textbook — strona 210

NAT Address Types
Inside Local - The original IP address of the host. For example: 10.0.05/24
Outside Local - The IP address of the destination device as viewed from the inside local
device (the destination LAN). For example: A remote web server.
Inside Global - The public IP address used by the inside local device for identification
and access to the internet. For example: the WAN IP address.
Outside Global - An IP address from outside the network. For example: the WAN
address of the interface connected to the web server.
NAT Operation Steps
Step 1 - A host on the local network sends a request to an external destination (outside
local), such as a web server.
Step 2 - The NAT-enable device receives the request and changes the local device
source address (inside local) to the public IP configured on the WAN interface (inside
global).
Step 3 - The NAT-enable device receives the request and changes the local device
source address (inside local) to the public IP configured on the WAN interface (inside
global).
Step 4 - The web server receives the request and replies with a public source IP.
Step 5 - The NAT-enabled device receives the reply from the web server and converts
the public destination address to the original private address (based on the NAT table).
The local host then receives the server’s reply.


### Textbook — strona 211

Section 4: NAT Implementation
The example below illustrates the simple topology of a router connecting a small
corporate network to the internet.
sacl
oN
R1
— Internet
LJ
——*,
i
——7
00020
NAT Interface Configuration
The first step in configuring NAT is to enable router interfaces for translation.
The ip nat inside\outside command informs the router which interfaces will participate
in the NAT process, and their direction, based on the network topology.
Each interface connected to the private network, is defined as inside, and each
interface connected to the internet is defined as outside.
#The interface facing the LAN.
Edge-R1(config)#interface gigabitEthernet 0/@
Edge-R1(config-if)#ip add 10.0.0.1 255.255.255.0
Edge-R1(config-if)#ip nat inside
Edge-R1(config-if)#no shutdown
Edge-R1(config-if)#exit
#The interface facing the WAN.
Edge-R1(config)#interface serial 0/0/08
Edge-R1(config-if)#ip add 209.15.10.1 255.255.255.0
Edge-R1(config-if)#ip nat outside
Edge-R1(config-if)#no shutdown
Edge-R1(config-if)#exit


### Textbook — strona 212

Static NAT Configuration
Command
ip nat inside source static <local-ip> <global-ip>
<)>
In this example, a user wants to connect to the internal server from somewhere on the
internet.
Because the user cannot access the LAN directly, it sends the request to public router
interface 209.15.10.1, and the router uses the NAT static map to forward the request to
the 10.0.0.10 server.
The second section in the example is for Port Forwarding. It forwards only SSH traffic
from outside to the server.
#Map all traffic between 10.0.0.10 and 209.15.10.1
Edge-R1(config)#ip nat inside source static 10.0.0.10 209.15.10.1
#Map only SSH connection between 10.0.0.10 and 209.15.10@.1 on tcp port
8080 of the outside
Edge-R1(config)# ip nat inside source static tcp 10.0.0.10 22 209.15.10.1
8080
Dynamic NAT Configuration
Assume the ISP defined 10 public addresses on the WAN interface:
Step 1: Create a public address pool using ip nat pool.
Step 2: Configure standard ACL to identify local addresses that need to be translated,
using access-list.
Step 3: Bind the ACL and the pool using ip nat inside source list.
Note: Using this method, the pool should contain enough available addresses, one for
each device.
#Dynamic NAT allows local hosts access to the outside network, using a
randomly selected public address from the pool.
Edge-R1(config)#ip nat pool ToFreedom 209.15.10.1 209.15.10.1@ netmask
255.299.2590
Edge-R1(config)#access-list 1 permit 10.0.0.0 0.0.0.255
Edge-R1(config)#ip nat inside source list 1 pool ToFreedom


### Textbook — strona 213

NAT Overload Configuration
NAT Overload or Port Address Translation allows a router to use a single public address
for multiple inside local addresses.
Methods to configure PAT:
1. Using an address pool.
2. Using a single address defined on the interface.
An important part of the command is the overload option.
#Method 1
Edge-R1(config)#ip nat pool ToFreedom 209.15.10.1 209.15.10.10 netmask
255.255.255.0
Edge-R1(config)#access-list 1 permit 10.0.0.0 0.0.0.255
Edge-R1(config)#ip nat inside source list 1 pool ToFreedom
#Method 2
Edge-R1(config)#access-list 1 permit 10.0.0.0 0.0.0.255
Edge-R1(config)#ip nat inside source list 1
NAT Overload Configuration Verification
Two commands can be used to fully verify a NAT operation.
The show ip nat statistics command displays NAT parameter and pool configuration,
pool status, and interface configuration.
The show ip nat translations command shows the active NAT translation (inside local
and inside global address paring, when they occur).
Note: Static NAT translation is always shown in the table.


### Textbook — strona 214

Edge-Rl1#show ip nat statistics
Total translations: 5 (1 static, 4 dynamic, 4 extended)
Outside Interfaces: Serial@/e/e
Inside Interfaces: GigabitEthernet0/o
Hits: 5 Misses: 13
Expired translations: 1
Dynamic mappings:
-- Inside Source
access-list 1 pool ToFreedom refCount @
pool ToFreedom: netmask 255.255.255.0
start 209.15.10.1 end 209.15.10.1
type generic, total addresses 1 , allocated @ (0%), misses 8
Edge-Ri1#show ip nat translations
Pro Inside global Inside local Outside local Outside
global
--- 209.15.10.1 10.0.0.10 --- ---
tcp 209.15.10.1:50016 10.0.0.10:50016 8.8.8.8:53 8.8.8.8:53
tcp 209.15.10.1:50017 10.0.0.10:50017 200.10.0.254:88
200.10.0.254:80
tcp 209.15.10.1:50018 10.0.0.20:50018 157.160.27.8:80
157.160.27.8:80
tcp 209.15.10.1:50019 10.0.0.20:50019 82.11.0.2:443
82.11.0.2:443


---

# 02 — Computer Networking — slajdy kursowe — pełna treść

Źródło: `Computer Networking.pdf` (525 slajdów). Każdy slajd ma własny nagłówek z numerem strony.


# Chapter 1: Introduction to Networks


### Slides — strona 1

i Introduction: - |
to Networks
Computer Networking


### Slides — strona 2

Computer Networking
Introduction Network Switch & IOS Switch Securit IP and Routing
to Networks Fundamentals Fundamentals y Concepts
Diagnostics and VLANs Dynamic IPv4 & IPv6é Subnetting
Troubleshooting and Trunk Routing Static Routing Concepts
Access Infrastructure Fiival Proiect
Control List Services J
2


### Slides — strona 3

Introduction to Networks
Overview
Lesson Objective
Network Types and Devices
This lesson is the starting point for Network Media and Cables
networking.
It teaches basic concepts and Network Topologies and Architecture
technologies of network structures,
. . Network Protocols and Commands
topologies, and devices.
Wireless Technology
G
3


### Slides — strona 4

CO
Introduction to Networks
NETWORK TYPES AND DEVICES


### Slides — strona 5

Network Types and Devices
Why is Networking Necessary?
Communication
Communication is an essential characteristic of any society.
In today’s world, people communicate with other people around
the world almost as simply as they talk to a person standing right
beside them.
Over the past several decades, global communication has
advanced significantly and has greatly improved the human social
experience.
Communication over a network (networking) brings people
together for either generic or specific purposes.
B
A network is basically two or more devices that communicate with each other and share information.
5


### Slides — strona 6

Network Types and Devices
Computer
LAN =") hl I
= = A Local Area Network defines a small geographical area is { = : a
Lme in which multiple computers and other devices are | ee = == = &
pa m connected. LANs can be set up in homes and small | = = &
businesses, and can be managed individually or centrally. ~~) 2 | ‘
ies
A Wide Area Network is spread across an unlimited = <= ae a
geographical area and connects between multiple LANs. Was | e
WANs are usually managed by several service providers. . ,
7
LANs can be designed to use one of two communication methods: Wired or Wireless
6


### Slides — strona 7

Network Center
MAN
A Metropolitan Area Network is larger than a LAN but
smaller than a WAN. In most cases, it is managed by a i -
city municipality and enables connection to broader = =a ‘
networks. Sie
SAN a a
—o A Storage Area Network is a dedicated network that Ai =
—o supports file servers and provides efficient transfer of
——d unusually large data sizes at extremely high rates. “thie \
@ ; : nF a
SAN is often not regarded as a type of network because it is closer to being infrastructure.
de


### Slides — strona 8

Network Types and Devices
Network Structure
Network Requirements
Communication among devices can be as simple as connecting a
cable between two computers.
On the other hand it can be as complex as a large assembly of
multiple networks spread around the world and regulated by a
variety of sophisticated devices and protocols.
B
The history of computer networks began in the 1960s with a network called ARPANET.
8


### Slides — strona 9

: Network
End Devices ; See
Devices that connect to a network for communication : aoe rk
purposes, such as computers, phones, and others. All ; a j ¥
end devices have unique addresses that identifies them j a :
on the network. vy ——
Media e-. =
‘Media’, based on the word ‘medium’ (meaning ‘in
between’) is a means of transferring data, such as
metallic wire, glass or plastic fiber, wireless radio
frequencies, and others.
=n
——— A
Intermediary Devices
=== =F Devices that transfer messages over the network and
ees facilitate communication between end devices.
2]


### Slides — strona 10

End Devi
Devices
In today’s world, most people
communicate with each other
through networks.
End devices are source or
destination devices ina
networked system.
Computers, laptops, and
phones are end devices that
allow us to communicate over
a network. a
———— a Re
End devices must have the
ability to connect to a network
via an NIC, to be able to send
and receive information.
EA
10


### Slides — strona 11

Network Types and Devices
NIC
To allow an end device to send
and receive information over a
network it must have the 2 Rass,
appropriate hardware. Le »* Z casos EN
A Network Interface Card (NIC) , —_. i : Ly, # —
allows end devices to interact a ci SSraah ae “et Y
with other devices over a < ONG s eS
network. » ok
Other names for NIC include:
* Network Adapter ‘ »
¢ LAN Adapter
* Physical Network Interface
iL


### Slides — strona 12

Network Types and Devices
Intermediary Devices
Definition
Intermediary devices act as bridges, interconnecting end devices.
Smart intermediary devices know how to differentiate between
devices, and can send data to specific destinations.
B
Unlike smart devices, simple intermediary devices send information indiscriminately across a network.
12


### Slides — strona 13

Network Types and Devices
Switch
For multiple end devices to
communicate with each other, a
mechanism needs to be set up _ —_
to handle the transfers. ’ SS
, — | (
A Switch is a device with physical 7. See » (
ports to which end devices can be se x Se £ f
connected via Ethernet cables, to meee |
create a network. bas Gere . '
Switches use MAC addresses to
pass information from one end
device to another.
13


### Slides — strona 14

Network Types and Devices
Switch Vs. Hub
Hub
A hub is the legacy implementation of a switch. Message 7g
: A a — a
uz It broadcasts data to all connected devices, as opposed to ——
to sending information to dedicated destinations. —
GO Message L—
. {1 \
Layer 2 Switch to A,B, ———|
we 6 F s and C
This is the most common and basic switch in use. [20009]
It uses MAC addresses to forward information to Hib L—_J
specific destinations within the network. ——
Layer 3 Switch
A layer 3 switch performs the same operations as a
layer 2 switch, but can also function as a router if it
is configured to do so.
14


### Slides — strona 15

Communication
A collision domain is a group of nodes that can ‘hear’ each other.
ee, TP Ideally, when one node talks, all the others only listen. When two
ig = iad is i nodes talk at the same time, a collision occurs. To resolve this issue, a
j : : hub creates collision domains.
’ A switch, which operates in Layer 2 of the OSI model, can create
separate conversations between nodes, which, in turn, creates
=” “2 , separate collision domains.
hii, 2 Although collisions are expected to occur in a half-duplex Ethernet
; network, if a collision domain becomes too big, traffic problems will
arise, due to re-transmissions.
B
15


### Slides — strona 16

Broadcast & Collision Domains
Communication
Broadcast is a type of communication whereby the sender sends a
single copy of the data to all devices on the same network segment.
oo Broadcast communication must be used, since protocols such as
° ARP and DHCP rely on it.
F VER. A broadcast domain includes devices that receive broadcast packets
A originating from senders within the same network segment.
X SS f, Routers operate in the network layer and separate both collision
Seas domains and broadcast domains.
e
16


### Slides — strona 17

Network Types and Devices
Half Duplex
Only one party can send or receive data at a single a a
moment. For example, a walkie-talkie works in half duplex.
fh Li
Full Duplex '
Both parties can send and receive data at the same time. Se St SS
For example, a phone call is performed in full duplex.
When 2 devices are set to different
duplex modes, a duplex mismatch
occurs. This reduces the quality of
the communication.
LY,


### Slides — strona 18

Network Types and Devices
Router
While switches allow devices to
interact in the same network,
routers allow them to communicate
with different networks. E == —
A router connects networks
and allows communication
between end devices in ST
different networks. same Pe es eee ey eer /
Routers use IP addresses to
route information among
networks.
=
18


### Slides — strona 19

Network Types and Devices
| Firewat |
pela = |
=e = oo =
(i) => oe,
es
Access points allow end Firewalls are effective A Wireless LAN Controller The home router combines
devices to connect toa security tools against allows the configuration of the features of all the
network wirelessly and threats that originate from multiple APs to be managed intermediary devices
manage information outside a network. from a central device. covered in this lesson so far,
transmission. Firewalls implement filters This is useful in large ina single device.
Awireless device user can that allow or block the organizations where It acts as an AP, a switch,
connect to a wired network transfer of information ina multiple APs are deployed and a firewall with the most
via a properly configured given direction. in different sections of a basic configuration.
access point. building.
19


### Slides — strona 20

CO
Introduction to Networks
NETWORK MEDIA AND CABLES


### Slides — strona 21

Network Media and Cables
Media
What does Media do?
Information cannot be transmitted over a network without a
means of transportation.
The term ‘media’ refers to the physical cables or wireless
technologies used to pass the information from one device to
another.
Different types of media feature varying speeds and distances
of data transfer.
6
Connections between continents were made possible using “submarine cables” that were
stretched across thousands of kilometers through the oceans.
21.


### Slides — strona 22

Network Media and Cables
CAT5e Cable
The most common way to
connect to a network is via an
Ethernet cable with an RJ-45 S
connector. =f
Cables are made of copper and i > Ss _~
can transmit information in the ss 3 eS —
form of electrical signals. — il ne a
= BS cessssuy 4
Signals deteriorate as the Con —— _/
distance grows, and due to the
influence of RFI & EMI, which
limits the cable length.
22


### Slides — strona 23

Network Media and Cables
Ethernet Cable Types
Cable Categories
CABLE SPECIFICATIONS
CAT-5 Maximum length of 100m, maximum speed of 100 Mb/s
CAT-5e Maximum length of 100m, maximum speed of 1 Gb/s
CAT-6 Maximum length of 100m, maximum speed of 1 Gb/s (Note: Supports 10 Gb/s for 55m)
CAT-6a Maximum length of 100m, maximum speed of 10 Gb/s
CAT-7 Maximum length of 100m, maximum speed of 10 Gb/s (Note: Supports 100 Gb/s for 50m)
EEE
23


### Slides — strona 24

Network Media and Cables
Cables
UTP
Unshielded Twisted-Pair is the most common copper Fou, SHIELDED CABLE | Tyileted
air

cable in use. It consists of four twisted pairs of colored -
wires. The act of twisting the wires is done to prevent Shielas Sonqucion
signal disruption (cross-talk). eo Yor!

Shielded Twisted-Pair cables are similar to UTP, but have beet

ire
additional protection against EMI and RFI interferences.
Each twisted pair is wrapped in foil. Outer ae
Jacket
a
EMI & RFI are electromagnetic and radio frequency interferences that can affect signals.
24


### Slides — strona 25

- - Ina straight-through cable, the colors match
Ethernet Cable Configurations rf y
Straight-Through r -
Straight-Through
Wires are placed in a straight formation from side A to
side B. This form is used for cables that are meant to Tees next
connect network devices of different types, such as a 2
switch and ai endpoint. gs a SSS
5 ae +
. Each cable is connected straight to the matching ee
pin on the other side. ED 61K.
O_O
DS
Rollover is another type of cable used to connect intermediary devices.
25


### Slides — strona 26

O In a crossover cable, pins 1&2 and 3&6 are crossed
Ethernet Cable Configurations age
Crossover 5: 7g j SS E,
= Wires crisscross from side A to side B. This form is ———a =.
a used in cables that are meant to connect similar 2-23 jj iff
: = network devices. a_i j
. Pins 1 &2 and crossed
. Pins 3 & 6 are crossed Crossover
e T568A to T568B eS STRAIGHT-THRU He re CROSSOVER Pc ”
Ree 3 3 TH RX 3, i 3 ee
—————Ssss 4 4
O [a —— ee FY 5—a— 5
RL 6 EE 6 Tx- RY 6 6 RX
== 2 ——— eel 2
= —_—_——==— 8 8 Ss EB &
26


### Slides — strona 27

Ethernet cables have a length
limit of 100m. A different type
of cable is used for greater
distances.
px
Optical Fiber Cables transmit 9 a
information using light, at high - CLA
8 lig Bl > a _
speed, over long distances. ' # _ [=
These cables are not sensitive ab 7
to RFI & EMI, but aren’t as J <a
flexible as Ethernet cables, and i a »
are more expensive. , -
—


### Slides — strona 28

CO
Introduction to Networks
NETWORK TOPOLOGIES AND ARCHITECTURE


### Slides — strona 29

Network Topologies and Architecture
Network Topology
Definition
Cal Pa
= i _ A network topology describes the structure of a network.
vi ¢
= | It represents all the connections between all components ina
7) network.
ot
Ld Several types of topologies can be used to construct networks.
6
A topology represents the resources of a network, but not locations and distances.
29


### Slides — strona 30

Network Topologies and Architecture
@ @Q
Q oN
@ EN, res
© pw
@ &
A connection between two In a star topology all end In a mesh topology each A hybrid topology is a
computers, networks or devices are connected to a end device can have combination of other
other devices. central intermediate device. multiple connections to topologies.
If the connection fails, the This type of topology is easy other end devices. Although a hybrid
communication is disrupted. to set up and maintain. It is This configuration is highly configuration takes
also highly scalable. resilient, due to its advantage of the strong
allowance of multiple points of other topologies,
connections, but it is also it also has to deal with the
expensive and very difficult disadvantages of those
to maintain. topologies as well.
30


### Slides — strona 31

Network Topologies and Architecture
3-Tier Architecture
Definition
The concept of a 3-Tier Architecture can be applied to any type of
network.
A The model helps design, implement, and maintain a scalable, reliable,
y ON and cost-effective network.
Its simplistic structure makes it very easy to manage.
yp —ti‘«<CSN The combination of these attributes means that it is the best choice
for large enterprises, in which thousands of computers need to be
interconnected, sometimes over an area that includes several
buildings.
B
Each layer has its own features and functionalities, which reduces network complexity.
31


### Slides — strona 32

Network Topologies and Architecture
3-Tier Structure
| a: |
A 3-Tier architecture consists of three layers
that provide isolation between devices, z0000|_ Ss Core
greater flexibility, more security options, Layer
and resilience.
te ge" 1
1 eS !

The separated layers are: ' an ate '

Core — routing layer connecting to servers * a

and the Internet. Distribution

Distribution — separation between core and BO) ees [z0000 Layer

access layers, and boundary control. _

Access — communication between end fag Se, ~e Sy

devices. wey ae ae 2 4g Ss

: Pig 1 —— S,
ze" om <4 Sig a
The layers can be managed independently 7 v 3s ~
Access Layer
SE 32


### Slides — strona 33

Network Topologies and Architecture
Collapsed Layer Structure
Core +
This architecture is similar to 3-Tier, but has =0000} ------- [BGO00] | Distribution
a different number of layers and a different Ke Layer
scalability potential. Wa f i i; Te
‘ s o ‘ s
¢ ‘ on re ° af \ a
¢ es

In this architecture, the core and distribution 3 H ax TSK ‘ ve

layers are collapsed together to form a single g* , * es CO = MM

layer. of Lb? Tye Sq Ry
This means it has the advantages of the 3-Tier
architecture, but a smaller network scale.

Access Layer
ee a


### Slides — strona 34

Network Topologies and Architecture
Physical & Logical Addresses
Why do we need a computer address?
When the first networks were created for local computers to
5 communicate with each other and share data, design engineers
. 5 realized they needed to know how computers would talk to
°@: each other and who they could talk to.
The idea was for each computer to have a unique name or
aa» identification, and the concept of a MAC address was born.
A MAC address is the unique identity of a computer within a
network, while IP addresses are used to identify machines
operating in different networks.
é
Each network card in a device has both a MAC address and an IP address at any given moment.
34


### Slides — strona 35

Network Topologies and Architecture
Physical Address
Media Access Control
A MAC address is a unique hardware identifier attached to each
network card. The address is static and should not be changed.
a = It consists of six hexadecimal nodes ranging from 00 to FF.
= A MAC address includes two parts:
¢ The first three nodes represent the manufacturer’s identifier
¢ The last three nodes represent a serial identifier
o
A MAC address will usually be written like 00:0d:83:b1:c0:8e, or sometimes 000d.83b1.c08e
35


### Slides — strona 36

Network Topologies and Architecture
An IP is used to uniquely identify computers on the network and create network partitions.
IPv4

IPv4 addresses are the most commonly used today. They consist of four octets of numbers between

0-255, which can generate approximately four billion different addresses.

Some addresses, such as X.X.X.255, are special, while others, such as 192.168.X.X, are dedicated to

specific uses.

IPv6
Due to advances in technology, IPv4’s four billion addresses were threatened with depletion, and
IPv6 was developed with six hexadecimal octets that can generate approximately 340x10‘36
addresses.
IPv6 addresses have not yet been fully integrated in modern use cases.
36


### Slides — strona 37

Network Topologies and Architecture
Class by Mask
The network The hosts
<< ———_ rd
Subnet masks define which addresses'in an IP address: 192 . 168. @ .0
octet can be used in an IP address, while C
remaining on the same network. Subnet mask: 255 . 255 . 255].0
The network The hosts
Devices (computers or network) must be in
the same network and subnet to
communicate without routing B IP address: 172 A116 | .0.0
Subnet mask: 255 .255/.0.0
The first IP address of each subnet is the The network The hosts
network address and cannot be used for —_—— ———
hosts or devices
A IP address: 10 |. 0.0.0
The last IP address of each subnet is the Subnet mask: 255}. @.0. 2
broadcast address and cannot be used
a »


### Slides — strona 38

CO
Introduction to Networks
NETWORK PROTOCOLS AND COMMANDS


### Slides — strona 39

Network Protocols and Commands
Communication Protocols
Protocols
To properly communicate with each other, different devices
require protocols.
Protocols are predefined sets of rules describing how something
should work or behave.
Protocols help maintain order among different technologies.
B
Protocols can be considered as ‘languages’ of data transfer. To communicate properly, two
or more devices must first agree to use the same ‘language’.
39


### Slides — strona 40

Network Protocols and Commands

The Internet Protocol Domain Name Service || The Dynamic Host The Hypertext HTTPS is a secure

is used to establish is a protocol used to Configuration Transfer Protocol is implementation of
communication over translate domain Protocol is used to used to transfer text- HTTP. It encrypts the

the network, without names to IP allocate IP addresses based data, such as transferred data to

delivery verification. addresses, and vice to new computers web pages, over the prevent it from being

versa. that join the network. Internet. intercepted.
40


### Slides — strona 41

Network Protocols and Commands
Network Commands
The Importance of Commands
Commands are used in network configuration, maintenance,
=a troubleshooting, and more.
= It is essential for any network to frequently run commands that check
the state of the network and monitor it.
Although some systems enable network configuration via a GUI, the
configuration is still often done via the CLI.
&
An example of a powerful use of network commands is for error detection.
41


### Slides — strona 42

Ping X.X.X.X
C:\Windows\system32> ping 8.8.8.8
Ping is the most common
command " administrative Pinging 8.8.8.8 with 32 bytes of data:
networking activity. .
Reply from 8.8.8.8: bytes=32 time=224ms TTL=54
It is used to check connectivity Reply from 8.8.8.8: bytes=32 time=681ms TTL=54
between computers over the Reply from 8.8.8.8: bytes=32 time=319ms TTL=54
network. Reply from 8.8.8.8: bytes=32 time=103ms TTL=54
It also provides information Ping statistics for 8.8.8.8:
such as connection speed and Packets: Sent = 4, Received = 4, Lost = @ (@% loss),
reliability. Approximate round trip times in milli-seconds:
Minimum = 103ms, Maximum = 681ms, Average = 331ms


### Slides — strona 43

ipconfig
ipconfig displays a computer’s C:\Windows\system32> ipconfig
IP configuration.
Windows IP Configuration
It can also request a new IP Ethernet adapter Ethernet:
address, if DHCP is configured.
Connection-specific DNS Suffix .:
— displays Link-local IPv6é Address... . . : £b21::b23e:28e9:c76b:7b35%11
extended information. IPv4 Address. ......... . : 192.168.5.11
— drops an Subnet Mask. ......... . : 255.255.255.0
IP address. Default Gateway. ........ : 192.168.5.1
— requests a
new IP address.


### Slides — strona 44

nslookup x.x.X.X
Computers use IP addresses to C:\Windows\system32> nslookup www.cyber.com
communicate with each other, Server: pfSense.cl22b.lan
while humans use names that Address: 192.168.0.1
are easier to remember than
numbers. . .
Non-authoritative answer:
coenaueniaaet Name: cyber.com
the name ofa computer by it Address: 199.244.49.102
puter by its
IPaddress. Aliases: www.cyber.com
It can also do the opposite - C:\Windows\system32> nslookup 199.244.49.102
query an IP address by the Server: pfSense.cl22b.lan
domain name. Address: 192.168.0.1


### Slides — strona 45

tracert xX.X.X.X
C:\Windows\system32> tracert 8.8.8.8
Information in the network
passes through multiple Tracing route to dns.google [8.8.8.8]
stations on the way to its over laymexinum) of 22 (ops:
a <1 ms <1 ms <1 ms pfSense.cl122b.lan [192.168.0.1]
destination. 2 115 ms 7@ms 59 ms 192.168.1.1
3 - - = Request timed out.
— — 4 + * a Request timed out.
displays all the stations 5 241 ms 170 ms 218 ms 172.17.10.182
along the route taken by the 6 * * * Request timed out.
information to its destination. 7 * * * Request timed out.
8 cf . Request timed out.
9 - = 259 ms core-213-57-0-69.PT.hotnet.net.il [213.57.0.69]
2 2 10 281 ms 245 ms 225 ms core-213-57-3-150.HFA.hotnet.net.il [213.57.3.150]
It can work with a domain 11 201 ms 174 ms 228 ms 108.170.251.129
name or an IP address. 12. 188 ms 230 ms 326 ms 74.125.37.167
13. 131 ms 83 ms 109 ms dns.google [8.8.8.8]
Trace complete.


### Slides — strona 46

Netsh [ command \ option ]
ni . : C:\Windows\system32> netsh interface ip set address “Ethernet”
ee ee static 192.168.10.5 255.255.255.@ 192.168.10.1
information is to use the
command.
C:\Windows\system32> netsh interface ip show config
It allows the configuration of
the IP address, DNS, default Configuration for interface "Ethernet"
gateway, and various network DHCP enabled: No
functions. Default Gateway: 192.168.10.1
Gateway Metric: 1
The example on the right InterfaceMetric: 5
shows how to'set an/\P address Statically Configured DNS Servers: None
and verify settings using : Register with which suffix: Primary only
Statically Configured WINS Servers: None


### Slides — strona 47

Network Protocols and Commands
Lab NET-01-L1 Mission
— Learn and practice CLI network commands in Windows
Local Network Configuration using CMD.
30-60 Min. © -
ww @ Local Network Configuration
a : ® Test Connectivity
ee, ™~ s ~ ® Domain names & IP
; rd = XN & N e wa
a) ) » : ~~ Environment & Tools NEaAteq Fes
| » . ®@ Windows 7/8/10 @ Lab document
| ve . W ® CMD
‘ ‘ :
.) o |
‘ ia —


### Slides — strona 48

CO
Introduction to Networks
WIRELESS TECHNOLOGIES


### Slides — strona 49

Wireless Technologies
Wireless Network Structure

Wireless networks for computer

communication are possible. Coo

Wireless media features better flexibility e H

than wired media, due to the absence of \

cables connected to end devices. i I ,

x. 1 oa
*& i} Pt
_
Information is transmitted using radio Ye H get ,
frequencies, which, however, do pose Mg wf
some security challenges. @ ~%
a z


### Slides — strona 50

Wireless Technologies
—
The ideal environment for Many common devices, The absence of physical The technology operates in
this technology is open such as microwave ovens, media exposes the network half-duplex, which means
space. and various wireless to the public and allows only one device can send
Some building materials can communication devices, others to discover it and and receive information at a
limit the range that wireless also transmit radio gain access to it, without time.
systems cover. frequencies. authorization to do so. When more and more users
These signals may interfere connect to the network, the
with signals transmitted in available bandwidth for
the wireless network and each user will decrease
affect their quality. accordingly.
50


### Slides — strona 51

Wireless Technologies
NIC Conversion
AP
Access point is the component that allows end devices
| | to connect to a network wirelessly using radio waves.
roses | The access point itself will be connected to the network
via cable. .
_—— _—
G bilnl Bore)
Wireless NIC Adapter _ ef —— ——— 11110
=== Fora device to connect to a wireless network it must
b Gi have a wireless NIC adapter to send and receive the
[ information.
Wireless NIC adapters can be implemented by an external device, or integrated in the computer.
Si


### Slides — strona 52

Wireless Technologies
Wireless Technologies
Wi-Fi
Wi-Fi, or wireless fidelity, is a technology based on IEEE 802.11 standards that allows
wi connection to a network wirelessly using radio waves.
Wi-Fi is used for LAN networks in shared spaces.
Wi-MAX
io~,
hk Wiemaxis an implementation of wireless network connection over a wide area.
It is used for LAN and MAN implementations.
Bluetooth
Bluetooth is an implementation of WPAN (Wireless Personal Area Network).
It is mainly used to pair devices and allows communication at up to 100 meters.
52


### Slides — strona 53

Wireless Technologies
Wireless Standards
Over the years, network standards were developed and modified to improve speed and bandwidth.
Wireless Standard History
STANDARD MAX SPEED FREQUENCY BACKWARD COMPATIBLE
802.11a 54 Mb/s 5 GHz NO
802.11b 11 Mb/s 2.4 GHz NO
802.11g 54 Mb/s 2.4 GHz 802.11b
802.11n 600 Mb/s 2.4 GHz & 5 GHz 802.11a/b/g
802.11ac 1.3 Gb/s 5 GHZ 802.11a/n
802.11ax 14 Gb/s* 1 GHz - 7.125 GHz 802.11a/b/g/n/ac
53


### Slides — strona 54

Wireless Technologies
Copper Fiber Wi-Fi
10 Mb/s — 10 Gb/s 10 Mb/s — 100 Gb/s 54 Mb/s — 14 Gb/s
D id the ti itter’:
Up to 100 meters Up to 100 Km epends:onmne ransmi ere F
strength and receiver’s sensitivity
Inexpensive Expensive Relatively Inexpensive
Vulnerable to the effects of EMI & REI Expensive equipment and The signal can be affected by
implementation surrounding structures
2 [amor Gi
54


### Slides — strona 55

’ = j FO Saw ~
= a # 4 i
4 ~~ ie
v). a " % * a4 a A
i >» ; Ss
> \ >
Chie —— . =
Fed Axncoes ta os 2 Spe
& Mh if
A ; 4 ~S : ra
=m Z By: ie ~~ zs
= Payee SQ


### Slides — strona 56

a i ™" : = a aw NETWORK ee Bal Ci = L D


# Chapter 2: Network Fundamentals


### Slides — strona 57

= # ' 4 — — = + i j
an Cybersecurity Professional Program
: : mana NEEWORK ! re hee += ca C ,
Computer Networking
Copyright © 1996-2023 HackerU Ltd. All Rights Reserved.


### Slides — strona 58

Computer Networking
Introduction Network Switch & IOS Switch Securit IP and Routing
to Networks Fundamentals Fundamentals y Concepts
Diagnostics and VLANs Dynamic IPv4 & IPv6é Subnetting
Troubleshooting and Trunk Routing Static Routing Concepts
Access Infrastructure Fiival Proiect
Control List Services d
2


### Slides — strona 59

Network Fundamentals
Overview
Lesson Objective Network Protocols and Models
OSI Model
This module introduces the network
components that together enable TCP/IP Model
communication between different
devices and services. Transport Protocols and Logical Ports
It also covers network architecture
models and their layers. Introduction to Wireshark Addresses
ARP and Encapsulation
G
3


### Slides — strona 60

CO
Network Fundamentals
NETWORK PROTOCOLS AND MODELS


### Slides — strona 61

. Web Browsin
Client g
ww 3 « ’ Dear Server 18.77.22.44,
eee A client represents the endpoint device (not www caryou please send my
a necessarily a PC) that requested an operation. a = Facebook home page.
Server
Sure! 10.2.2.7, here you
go, enjoy!
A server represents the endpoint device that receives
a request and performs the requested operation.
5


### Slides — strona 62

Network Protocols and Models
Client-Server
Client-Server Relationship
(o) The Client-Server model is a distributed application structure that
CARY + manages tasks and workloads by sharing them among providers
— of resources and services (servers), and delivers responses to
: service requesters (clients).
B
An alternative method is to use broadcast or multicast channels to distribute information.
6


### Slides — strona 63

Network Protocols and Models

HTTPS as

& ey a,
HTTP is an unsecure protocol HTTPS is the encrypted version Translates domain names to IP File Transfer protocol is used to
used to transfer information of HTTP. addresses according to transfer files over the network.
over-the web. It is used for secure predefined databases: For example, the FTP service can
Due to the fact that HTTP traffic communication and is widely The DNS protocol is used for be used to transfer files to
is not encrypted, it can be used on the Internet. address resolution in a network. another device over the
sniffed on the network. Communication is encrypted For example, when a URL is network.
For example, if credit card using TLS (Transport Layer entered in a browser, the DNS
information is entered in an Security) or SSL (Secure Socket protocol translates the domain
HTTP website, it can be Layer). that was entered to an IP
captured in simple text format. address.
de


### Slides — strona 64

Network Protocols and Models

>= ~ La

Eats! @ ¢

-
The DHCP service is responsible Simple Mail Transfer Protocol is Secure SHell is a secure Internet Control Message
for assigning an IP address to the standard protocol for mail command line protocol that Protocol is used by network
each device on a network transfer over the Internet. allows the user to run remote devices to generate error
configured to use DHCP, such as Forexamplewhenan Envail ig commands ona remote messages when IP packets are
PCs, Routers, Firewalls, Servers, Pe: machine. not able to reach their
ate sent over the network, the destinations

: SMTP protocol manages the Any data that passes through .
For example, a PC configured operation. SSH is encrypted.
with DHCP will automatically be For example, when a remote
assigned an IP address upon connection is made to a device,
startup. the connection is made using
SSH on port 22.
8


### Slides — strona 65

Network Protocols and Models
Network Model Concept

The idea behind creating a networking model was to set a standard for
Ca CJ the development and usage of network components.

Standards allow devices to communicate without requiring continuous

= = configuration in different device platforms.

« " mmeulipe In addition, dividing the networking process into smaller sub-processes

helps debug issues and pinpoint solutions.

&
TCP/IP and OSI were developed around the same time, with the aim of solving the same problem.
2]


### Slides — strona 66

Network Protocols and Models
Today, OSI and TCP/IP are very similar due to the way they evolved over time.
OSI is often used as an educational model, while TCP/IP is used more as a practical model.
OsI

OSI is a network model in which each functionality of the network is represented by a layer.
There are 7 layers, in which the functionality of each is dependent on the one below it.

OSI was developed by the International Organization of Standardization.

TCP/IP

The first TCP/IP specification was submitted several years after the OSI model.

The original TCP/IP model consisted of 4 layers, but was later updated to the current 5 layers.

However, the 4-layer version is still more commonly used.

TCP/IP is used for network analysis, due to its lesser involvement with the top 3 layers.

10


### Slides — strona 67

CO
Network Fundamentals
OSI MODEL


### Slides — strona 68

OSI Model
OSI Model

* OSI defines a networking framework to implement protocols in layers.

* OSI conceptually divides computer network architecture into a logical
seven-layer progression.

¢ Lower layers deal with electrical signals, chunks of binary data, and
routing data across networks.

¢ Higher levels cover network requests and responses, data representation,
and network protocols, from a user's viewpoint.

&
OSI was developed by the International Organization for Standardization (ISO) in 1974.
42


### Slides — strona 69

OSI Model
OSI Model
—_ OosI
Transmit Data Receive Data
The OSI model is divided into 7 layers: APPLICATION APPLICATION
Application, Presentation, Session,
Transport, Network, Datalink, Physical. PRESENTATION PRESENTATION
When network traffic is generated, it
top layer to the bottom layer.
TRANSPORT TRANSPORT
When received, traffic goes through
the model in the reverse direction: NETWORK NETWORK
from bottom to top (decapsulated).
; DATA LINK DATA LINK
PHYSICAL Physical Layer PHYSICAL
13


### Slides — strona 70

OSI Model
Layer 7 - Application Upper Layers
Users interact directly with applications that operate at
Layer 7. Examples of Layer 7 applications include web
=== browsers such as Google Chrome, Firefox, and Safari, APPLICATION
and other applications, such as SSH and FTP.
G PRESENTATION
Layer 6 - Presentation
The Presentation Layer prepares or translates data from SESSION
application format to network format, and vice versa.
An example of the Presentation Layer operation is the
encryption and decryption process. a =
Layer 5 - Session
The session layer is responsible for creating a session
Y between two devices.
It is also responsible for session checkpoints and recovery.
14


### Slides — strona 71

OSI Model
Layer 4 - Transport
The Transport Layer handles coordination of data transfer between end
systems and hosts, including how much data to send, at what rate,
destination, etc. Data in this layer is organized into segments.
The transport layer determines if the connection should be instantiated, how
a to verify data integrity, how to recover from a connection error, and if
retransmission is necessary.
The protocols in this layer provide flow control, multiplexing, and reliability.
&
TCP and UDP are discussed in more detail in later slides.
15


### Slides — strona 72

OSI Model
Layer 3 - Network
The Network Layer organizes data into packets called IP datagrams that
contain logical source and destination addresses.
Routers operate in this layer.
The Network Layer’s job is to allow hosts to send packets across multiple
paths to any other network, and deliver them to their destinations, via
routers operating on this layer.
&
Diagnostic tools, such as ping and tracert operate in this layer.
16


### Slides — strona 73

OSI Model
Layer 2 — Data Link
queen. The Data Link Layer provides node-to-node data transfer (between two directly connected
ii ft | . nodes) and can provide the means to detect errors that may occur in the Physical Layer.
— Switches operate in this layer. Data in this layer is organized into frames.
Layer 1 -Physical
The Physical Layer defines the details of how data is physically sent through the network.
This layer determines how bits are electrically or optically transferred by hardware devices that
“2 interface directly with a network medium, such as coaxial cable, optical fiber, or twisted-pair
- - copper wire.
Hubs operate in this layer. a
The Data Link Layer includes two sub-layers: MAC (Media Access Control) and LLC (Logical Link Control).
LY,


### Slides — strona 74

OSI Model
Each network protocol is assigned to a particular OSI layer.
Common Protocols in Each Layer
LAYER PROTOCOLS
Application DNS, DHCP, SSH, HTTP\S, FTP, SNMP, SMTP, POP3
Presentation Encryption, Encoding, SSL, ASCII, EBCDIC, TIFF, GIF, PICT, JPEG, MPEG, MIDI
Session NFS, NetBios names, RPC, SQL
Transport TCP, UDP, RTP, SCTP
Network IPv4, IPv6, ICMPv4, ICMPv6, IPX
Data Link Ethernet, PPP, FDDI, ATM, IEEE 802.5/ 802.2, HDLC, Frame Relay
Physical Ethernet (IEEE802.3), Wi-Fi (IEEE 802.11), FDDI, B8ZS, V.35, V.24, RJ45
18


### Slides — strona 75

OSI Model
Memorize the Layers
Memory Tips
e All People Seem To Need Data Processing
e Please Do Not Throw Sausage Pizza Away
e Please Do Not Touch Steve’s Pet Alligator
2)
19


### Slides — strona 76

Encapsulation
Data Encapsulation
What is Encapsulation?
When a message is sent from source to destination, it must have a
specific format or structure. Message formats depend on the type of
Ea message and the channel used to deliver it.
The opposite process of encapsulation is called decapsulation. This is
when the host is on the receiving side.
The same process occurs in OSI and TCP/IP using the same protocols.
20


### Slides — strona 77

Encapsulation
Data Encapsulation
Encapsulation
MP,. For example, to send mail, we place a message in an envelope —
encapsulation. The envelope is written in a format the mail service
accepts and is sent to the destination. The receiving side opens the
envelope and takes out the message — decapsulation.
The envelope is similar to a network Frame.
21


### Slides — strona 78

ARP and Encapsulation
Encapsulation in Layers 4-7
As an example, we can focus on the process of sending data.
The first step in the process is ... YOU!
Data
When you click on a link:
HTTP GET
The Application layer creates an HTTP header requesting the APPLICATION
web page from the server.
. Data
The Presentation layer encodes, encrypts, or compresses the
data traveling down from the Application layer, if , 0101101010101010
6 PP on lave necessary. PRESENTATION 1101010101001101
For example, it may convert text to a binary string.
The Session layer determines the direction of the data: one- Data
way or two-way, and whether the connection is secure or not. 0101101010101010 This is called a
In addition, a session ID is assigned to the connection. SESSION 1101010101001101 Segment
TCP Header Payload
The Transport layer adds a header containing the source and . . 0101101010101010
oe . : : TRANSPORT Sre: 51001 Dst:80 | 4194910101001101
destination logical ports, and other control information.
This layer also divides data from upper layers into smaller pieces
called Segments. Each segment is a maximum (MSS) of 1460
bytes.
22


### Slides — strona 79

— Encapsulation in Layers 1-3

The Network Layer adds a header to the segment with This is called a
the IP source and destination addresses, and other Packet
control information (such as TTL) . During this step, the
segment is encapsulated in a packet. IP Header TCP Header Payload
Packets are limited to a maximum size (MTU — Maximum NETWORK Src: 10.0.0.1 | Src: 51001 § 010110101 This is called a
Transmission Unit) of 1500 bytes. Dst:80.7.1.2 Dst:80 001010100 Frame

Ethernet Header IP Header TCP Header FCS
The Data Layer adds'a: Header and Trailer to the packet: DATA LINK sre: 00:aa:bf:22:11:11] Src: 10.0.0.1 }src: 51001| 01011 | crc
The header contains the physical source and destination Dst: 00:cc:ff:69:11:11| Dst:80.7.1.2 | Dst:30 | 01010 | 0xA78
addresses. The trailer, also known as FCS, is for frame
error checking only.

00101001010101010

PHYSICAL >

10101001101010001
The Physical layer accurately transmits the Frames along
the physical medium. For example, it sends electric
pulses over an Ethernet cable, or wireless radio waves.

23


### Slides — strona 80

CO
Network Fundamentals
TCP/IP MODEL


### Slides — strona 81

TCP/IP Model
Transmission Control Protocol/Internet Protocol
TCP/IP Model
This model is a suite of communication protocols used to interconnect
network devices on the Internet.
The model describes how data is exchanged over the Internet, including
how data should be divided into packets, addressed, transmitted, routed,
es and received by the destination.
ae TCP/IP was designed to make networks reliable and enable them to
automatically recover from the failure of any device on the network.
25


### Slides — strona 82

TCP/IP Model
— TCP/IP
Transmit Data Receive Data
Layers in the TCP/IP model are similar to
those in the OSI, except for the top three
layers.
APPLICATION APPLICATION
TCP/IP uses the client-server model of
communication in which a user or machine
is given access to a service by another
computer on the network.
TRANSPORT TRANSPORT
Collectively, the TCP/IP suite of protocols is
classified as ’Stateless”, which means each
client request is considered new, and is INTERNET INTERNET
unrelated to previous requests.
Network Access Physical Layer Network Access
ey
26


### Slides — strona 83

TCP/IP Model
Layer 4
The Application Layer defines TCP/IP application protocols and how host
programs interface with Transport Layer services to use the network.
>= The Application Layer includes all higher-level protocols, such as DNS, HTTP,
Telnet, SSH, FTP, TETP, SNMP, SMTP, DHCP, X Windows, RDP, and others.
&
The TCP/IP top layer is equivalent to the combined three top layers of OSI.
2/


### Slides — strona 84

TCP/IP Model
Layer 3

The Transport Layer handles coordination of data transfer between end systems
and hosts, including how much data to send, at what rate, destinations, etc.
The transport layer determines if the connection should be instantiated, how to

Ti verify data integrity, how to recover from a connection error, and if retransmission
is necessary. Data in this layer is organized into segments.
The protocols in this layer provide flow control, multiplexing, and reliability.

&
The Transport layer in TCP/IP corresponds to the Transport Layer in OSI.
28


### Slides — strona 85

TCP/IP Model
Layer 2

The Internet Layer organizes data into packets called IP datagrams that
contain logical source and destination addresses.
Routers operate in this layer.
The Internet Layer’s job is to allow hosts to send packets across multiple

: paths to any other network, and deliver them to their destinations, via
routers operating on this layer.

&
The Internet layer in TCP/IP corresponds to the Network Layer in OSI.
29


### Slides — strona 86

TCP/IP Model
Layer 1

The Network Access Layer is the lowest layer of the TCP/IP protocol model.
Packets from the Internet layer are sent to the Network Access layer for delivery
within the physical network. Data in this layer is organized into frames.

e" Protocols in this layer provide the means for the system to deliver data to other

ay pe devices in a directly connected network, using physical addresses (MACs).
The protocols and standards defined for this layer dictate how data is transmitted
on the media (Ethernet cable, wireless connection, others).

The Access Layer of the TCP/IP model corresponds with the Data Link and Physical layers of OSI.

30


### Slides — strona 87

CO
Network Fundamentals
TRANSPORT PROTOCOLS AND LOGICAL PORTS


### Slides — strona 88

Transport Protocols and Logical Ports
Transport Protocols
TCP & UDP
TCP and UDP are protocols that are used to transmit
data over the network.
TCP and UDP operate in Layer 4 (Transport Layer).
6
32


### Slides — strona 89

Transport Protocols and Logical Ports
Transmission Control Protocol
TCP is more trusted and commonly used than UDP.
It verifies the availability of all parties before initiating a connection,
by performing a three-way handshake. It then marks packets and
makes sure they are received in the correct order.
TCP is described in detail in RFC 793.
33


### Slides — strona 90

Transport Protocols and Logical Ports
User Datagram Protocol

UDP is less strict about data integrity and is more speed-oriented.
UDP simply sends packets, without checking the data, even if nobody is
ready to receive them.

YY) This type of communication works better when streaming content, such

6 as audio, where some packets may be skipped without affecting the
entire stream.

UDP is described in detail in RFC 768.
34


### Slides — strona 91

Transport Protocols and Logical Ports
TCP UDP
Connection-oriented protocol. A connectionless protocol.
. 4. . . ae Suitable for applications that need fast, efficient
Suitable for applications that require high reliability, . PP
‘of aa wae transmission. Also useful for servers that answer small
where transmission time is less critical. . :
queries from large numbers of clients.
. _ Packets may arrive out of order, UDP does not
Rearranges data packets in the order specified. y
rearrange them.
I | \/ S(O
Guarantees that transferred data remains intact. If a There is no guarantee that messages or packets that
packet is corrupt upon arrival, it is resent. are sent will reach their destinations.
. UDP does error-checking but simply discards
Errors are detected via checksum. 8 Ply
erroneous packets. Error recovery is not attempted.
TCP is relatively slow. UDP is relatively fast.
35


### Slides — strona 92

Transport Protocols and Logical Ports
TCP uses flags to provide additional useful information or control the connection.
TCP Flags
Flag Role
SYN Synchronization - this is the first flag between two hosts, and is used to establish a 3-way handshake.
ACK Acknowledged - acknowledges successful receipt by the host.
RST Reset - Terminates a connection if a TCP failure occurs or a conversation is not permitted.
FIN Finish - Requests connection termination.
PSH Push - Immediately sends all buffered data.
URG Urgent - Data with a URG segment is forwarded to the Applications Layer immediately.
36


### Slides — strona 93

Transport Protocols and Logical Ports
—_— 3-Way Process
Client Server
A 3-way handshake is responsible for
communication between network
devices that use TCP. HTML
The handshake is known as “3-way”
because it includes 3 steps:
1. The client sends “SYN”. @
2. The server responds with “SYN-ACK”.
3. The client finalizes with “ACK”. _
When the process ends successfully, a 2)
connection is established between the client
and the server, and data can immediately be
transferred between them. rs)
os
37


### Slides — strona 94

Transport Protocols and Logical Ports
—_— Termination Process
Client Server
Session Termination is the last stage of a
TCP connection. This is when
communication ends and the session is HTML
closed.
Step 1 - One of the sides (client) requests to P
close the connection by sending a FIN flag to @)
the other side (server). all EE rercee
Step 2 - The receiver of the FIN flag (server)
returns an ACK flag, to approve the request. 2)
Step 3 -The server then sends a FIN flag to the gentile
cen, oO
Step 4 - The client approves the FIN request :
by the server, and responds with an ACK flag. ; —ooeSESFSFes#sS
The connection is then terminated. aoa
Y
———_———___,
38


### Slides — strona 95

Transport Protocols and Logical Ports
What are Logical Ports?
In computer science, a logical port is a number assigned to a “logical”
connection, which is used to represent a service or protocol on the end
device.
An IP address can send packets to the destination host, but not to the
destination service on that end device.
As an example, a street address can lead to the correct building, but it does
not specify the apartment number within that building.
&
39


### Slides — strona 96

Transport Protocols and Logical Ports
Logical Port Groups
There are 65,536 in TCP and 65,536 UDP ports, divided into three main groups, as follows:
Well-Known Ports
Port numbers in the “well-known” port range are assigned to commonly used and essential
0-023 protocols. The port numbers are permanent, and every network administrator must know them.
We use these numbers all the time, without realizing it.
The range includes protocols such as HTTPS, DNS, DHCP, Email protocols, and others.
Registered Ports
O24 “IANA assigned these ports for IT companies that want to register them for proprietary
ALS) 5541, applications. For example, Microsoft RDP 3389 and Dropbox 7600.
40


### Slides — strona 97

Dynamic & Private Ports
This group covers the remaining logical ports that are available for any application.
The port range is known as “client ports” and is usually used for logical client
AGi1S2 connection.
For example, a host connecting to a web server sends requests to port 80. This lets
65535 the web server know which service the client is requesting. However, the return
traffic must be sent to a source port, which is chosen randomly. When the connection
closes, the port can be reused for another connection, enabling the client to establish
multiple connections and manage responses from multiple sources.
&
41


### Slides — strona 98

Transport Protocols and Logical Ports
The following table lists common network protocols and their TCP and UDP ports.
Logical Port Numbers
Protocol TCP\UDP Logical Ports Protocol TCP\UDP Logical Ports

HTTP TCP 80 SSH TCP 22
HTTPS TCP 443 RDP TCP 3389

DNS UDP 53 SMB TCP 445
DHCP UDP 67, 68 FTP TCP 20, 21
SMTP TCP 25, 587 TFTP UDP 69

POP3 TCP 110 NTP UDP 123

42


### Slides — strona 99

C:\WINDOWS\system32>netstat -ab
Ports are used to receive and Active Connections
send data.
Proto Local Address Foreign Address State
TCP Q.0.0.0:135 Server_01:0 LISTENING
A web server will open Port 80 [svchost.exe]
in listening mode if it intends to TCP =: @.0.@.@:443 Server_01:0 LISTENING
receive HTTP traffic. [vmware-hostd.exe]
TCP Q@.0.0.0:445 Server_01:0 LISTENING
Adlient will openca random Can not obtain ownership information
port for each server it accesses han Sn wes Server_01:0 LISTENING
. vmware-authd.exe
when browsing the web. TCP @.@.0.0:912 Server_01:0 LISTENING
[vmware -authd.exe]
rai TCP Q.0.0.0:1536 Server_01:0 LISTENING
eee ports, use [svchost.exe]
stands forall. ee Loa Server_01:0 LISTENING
svchost.exe
stands:for the:names. TCP 0.0.0.0:1539 Server_01:0 LISTENING


### Slides — strona 100

Transport Protocols and Logical Ports
According to the materials learned in the previous part, answer the following questions as best as you can.
You may use external materials, such as Internet searches.
Communication Roles
Number Question
1 Briefly describe the operation or function of each layer. (For example, Layer 6 encodes, encrypts, and compresses the
information)
2 List two to three main protocols that operate in each layer. (For example IP, ICMP-Network Layer)
3 List two protocols that use TCP, and two that use UDP.
4 Describe the TCP 3-Way Handshake.
5 List the logical ports of the following protocols: HTTP, HTTPS, DNS, FTP, SMTP.
6 How many layers do the TCP/IP and OSI models have, and what are their names? (Try to answer from memory) FEE
44


### Slides — strona 101

CO
Network Fundamentals
INTRODUCTION TO WIRESHARK


### Slides — strona 102

Introduction to Wireshark
Wireshark
— Wireshark
File Edit View Go Capture Analyze Statistics Telephony Wireless Tools Help
4Ud@O 1D ROC eset sbeaaan
Wireshark is a free application Expression... +
that enables the capture and
viewing of data traveling back
and forth on the network. Capture
using this filter: [J [Enter a capture filter ~] All interfaces shown *
It is able to read the contents Normerfeces found
of each packet and apply
different filters.
Wireshark is commonly used to
troubleshoot network
problems, and develop and test
software.
Learn
User's Guide - Wiki - Questions and Answers - Mailing Lists
You are running Wireshark 3.0.1 (v3.0.1-0-gea35icd8). You receive automatic updates.
% — Ready to load or capture || No Packets || Profile: Default
jm
46


### Slides — strona 103

Capturing Data
— Wireshark
\a ax
A A AecOUBRE Cereerabeaacawkt
When invoked, Wireshark ey ES
initi i he Toe = ator Pol Leg fo im”)
presents aniinitial:screen with 10.000000 10.1.20.1 157.240.1., TLSv1.2 85 Application Data =
a list of available network i 2.078309 157.240.1.53 10.1.20.1 TCP 66443 5 8199 [ACK] Seq=1 Ack=32 Win=144 Len=@ =
interfaces. | 3.131308 10.1.20.1 62.0.136... TCP 55 [TCP segment of a reassembled PDU] =
| 4.131571 62.0.136.237 10.1.20.1 TCP 66 8093 > 11632 [ACK] Seq=1 Ack=2 Win=254 Len=@ SLE=1 SRE=2
5.155242 157.240.1.53 10.1.20.1 TLSv1.2 92Application Data =
Selecting an interface will start 6 0.195710 10.1.20.1 157.240.1.. TCP 548199 » 443 [ACK] Seq=32 Ack=39 Win=1027 Len=0 =
the capture of all traffic that | _81.132066 62.0.136.237 _10.1.20.1_TCP 6 [TCP Keep-Al CK] 8093 > 11632 [ACK] Seq=1 Ack= =25
passes through it | 91,228919 146.185.219.33 10.1.20.1 TCP 60.80 > 49803 [ACK] Seq=1 Ack=1 Win=501 Len=0 —
Wireshark can also be used to a : wastes : : aa via aerate —
open traffic captured by other Frame 1: 85 bytes on wire (680 bits), 85 bytes captured (680 bits) on interface ® By
Ethernet II, Src: HewlettP_3e:5b:9e (4:39:09:3e:5b:9e), Dst: Fortinet_4e:8b:12 (04:d5:90:4e:8b:12)
tools, such as TCP dump. Internet Protocol Version 4, Src: 10.1.20.1, Dst: 157.240.1.53
Transmission Control Protocol, Src Port: 8199, Dst Port: 443, Seq: 1, Ack: 1, Len: 31
Captured data can be exported 0000 04 d5 90 de 8b 12 #4 39 09 3e Sb Je 08 GO 45 00 Ne--9 s>[+--E |
j fil 0010 00 47 da 81 40 00 80 06 63 @8 Ga O1 14 G1 9d FO Gs c |
into .pcap or .pcapng Tiles. 0020 @1 35 20 @7 O1 bb 5a 42 67 7e a@ Oc C9 b250 18 -5 ---ZB ge... -P
2030 04 @3 86 Ge 00 00 17 @3 03 0 la ca 99 84 ed 00 al
OF - sreshark_Ethemet_20200721130008_a 14160, ca009 Fackets: 522 * Displayed: 496 (95.0%) Profile: Default
eal
—_—
=


### Slides — strona 104

Introduction to Wireshark
Packet List
Packet List is the main view of Wireshark. It lists captured packets in the order of their capture,
=| and offers various search and filter options.
Packet Details

= Packet Details is the part in the middle that displays the details of a specific packet.

"4 The details are divided into fields corresponding to TCP/IP layers, such as the Frame (Physical),
4 Ethernet (Data Link), and IP (Network).

Packet Bytes
FTieiaa The bottom part of the view corresponds to the actual bytes of the selected packet, in
hexadecimal format and ASCII encoding.
=
48


### Slides — strona 105

Introduction to Wireshark
ICMP Traffi
— Wireshark
MicuP Sample a
File Edit View Go Capture Analyze Statistics Telephony Wireless Tools Help
The Ping command includes a auc@it LeeSP seb aaak
Expression... +
request and a reply.
No. Time Source Destination Protocol Length Info “2
1 0.000000 172.42.0.157 172.42.0.140 ICMP 98 Echo (ping) request id=@x@cda, seq=1/256, tt1=64
Each ICMP packet is numbered 2 0.300934 172.42.0.140 172.42.0.157 ICMP 98 Echo (ping) reply id=0x@cda, seq=1/256, ttl=64
‘ ape " 3 1.000925 172.42.0.157 172.42.0.140 ICMP 98 Echo (ping) request id=@x@cda, seq=2/512, ttl=64
and can be identified to find a 4 1.298136 172.42.0.140 172.42.0.157 ICMP. 98 Echo (ping) reply id=@x@cda, seq=2/512, ttl=64 ¥
corresponding response. s >
Frame 1: 98 bytes on wire (784 bits), 98 bytes captured (784 bits) a
Ethernet II, Src: Vmware_c6:21:44 (@0:@c:29:c6:21:44), Dst: SamsungE_83:45:3b (@4:d6:aa:83:45:3b)
ICMP has only four fields since Internet Protocol Version 4, Src: 172.42.0.157, Dst: 172.42.0.140
. + Internet Control Message Protocol
it is a Layer 3 protocol. Type: 8 (Echo (ping) request)
Code: @
~ Checksum: @x7d9@ [correct]
In Windows each ICMP echo [Checksum Status: Good]
(ping) packet includes all the Identifier (BE): 3290 (@x@cda)
4 Identifier (LE): 5582@ (@xdaec)
basic symbols and numbers on Sequence number (BE): 1 (@x@001)
the keyboard. Sequence number (LE): 256 (@x0100) tp
9000 4 dé aa 83 45 3b @@ Gc 29 c6 21 44 O8 G8 45 00 Oe ): 1D -E “
0010 @@ 54 8c 1a 40 @@ 40 @1 55 11 ac 2a @@ 9d ac 2a T+ -@:@ Us -*. +e #
0828 @@ 8c @8 @@ 7d 98 Gc da CO O1 e9 53 bb Sc BO BO ves} +Se\ee
0030 00 00 04 11 06 00 00 00 000010111213 1415 ------- :
0040 1617 18 19 1a 1b 4c 1d Je 1f 20 21 22 23.24.25 0 -------- ++ MRSS
| 0050 26 27 28 29 2a 2b 2c 2d 2e 2F 30 31 32 33.34.35 &'()*+,- ./012345 ¥
Q@ * icmp sample.cap || Packets: 8 - Displayed: 8 (100.0%) || Profile: Default
EA
—_
=a


### Slides — strona 106

Introduction to Wireshark
DNS Traffic
— Wireshark
a
Aac@i PRO errseFsstlbaaagr
Expression... +
DNS traffic includes multiple ns hae rn naa Pretest Lage Does
requests and replies. es 1 0.000000 172.42.0.151 172.42.0.138 DNS 74 Standard query @xd282 AAAA api.segment.io
ols 2 0.010187 172.42.0.138 172.42.0.151 ONS 158 Standard query response @xd282 AAAA api.segment.io SOA
3 5.906976 172.42.0.157 172.42.0.138 ONS 71 Standard query @xb970 A
4 5.994438 172.42.0.138 172.42.0.157 ONS 87 Standard query response @xb97@ A -com A 107.180.
Most of a search tree will not 5 5.995163 172.42.0.157 172.42.0.138 ONS 71 Standard query @x6276 AAAA
. 6 6.121930 172.42.0.138 172.42.0,157 ONS 142 Standard query response 0x0276 AAAA -com SOA nst
appear in a packet. Only the : >
request and response. Frame 1: 74 bytes on wire (592 bits), 74 bytes captured (592 bits) “
Ethernet II, Src: LcfcHefe_7a:4b:17 (€8:6a:64:7a:4b:17), Dst: D-LinkIn_d7:48:d0 (78:32: 1b:47:48:40)
Internet Protocol Version 4, Src: 172.42.0.151, Ost: 172.42.0.138
DNS may try to automatically User Datagram Protocol, Src Port: 62297, Ost Port: 53
~ Domain Name System (query)
resolve both A and AAAA Transaction 10: @n#202
records corresponding to the Flags: @x@1@@ Standard query
Questions: 1
IPv4 and IPv6 addresses pneuan Waa
respectively. Authority RRs: @
Additional RRs: @ .
0000 78 32 1b d7 48 do e8 Ga 64 7a 4b 17 08 00 45 00 = x2--H.-j dzK.--E
O@10 8 3c 6F bb G8 06 82 11 71 88 ac 2a 00 97 ac 2a <o | haba
2020 00 Ba £3 59 G2 35 G8 28 bi 10 d2 82 @1 00 02 O1 Ve5e( oesoee
0020 08 00 00 8 G2 G2 O3 61 70 69 07 73 65 67 6d 6S a pi-segne
0080 Ge 74 02 69 GF 00 G2 1c 00 1 nt-io
@ 7 oNssample.cap | Packets: 6 ° Displayed: 6 (100.0%) | Profile: Default
=


### Slides — strona 107

Introduction to Wireshark
— Wireshark
AMLHTTP Sample.cap - x
File Edit View Go Capture Analyze Statistics Telephony Wireless Tools Help
4udc@i <eeSsF¥esaaawn
expression... ++
. No. Time ‘Source Destination Protocol Length Info
HTTP is an unsecure protocol i 16 14.384881 172.42.0.157 192.195.77.80 HTTP. 779 POST /login-form/ HTTP/1.1 (application/x-www-form-url
used to transfer information ‘ 22 14.571270 192.195.77.80 172.42.0.157 HTTP 357 HTTP/1.1 200 OK (text/html) i
over the web. Frame 16: 779 bytes on wire (6232 bits), 779 bytes captured (6232 bits)
Ethernet II, Src: Vmware_c6:21:44 (@0:0c:29:c6:21:44), Dst: D-LinkIn_d7:48:d0 (78:32:1b:d7:48:d@)
: . Internet Protocol Version 4, Src: 172.42.0.157, Dst: 192.195.77.80
Since HTTP traffic is not Transmission Control Protocol, Src Port: 60834, Dst Port: 80, Seq: 1, Ack: 1, Len: 713
encrypted, it can be sniffed Hypertext Transfer Protocol
» HTML Form URL Encoded: application/x-www-form-urlencoded
on the network. Form item: “username” = “lionk”
Form item: "password" = "Aal23456"
Form item: "submit" = "Login"
0000 78 32 1b d7 48 de @@ ec 29 c6 21 44 EERE 45 0 = x2--H--- )- !DBBE ay
2010 02 fd bf 2F 40 @2 40 e6 bd FO ac 2a 2B Sd cOC3_—--/@-@ ---*--
0020 4d 50 ed a2 08 50 dd 31 94 33 cb c3 de c6 8018 MP---P-1 -3.----
9030 @@ e5 bd ca 60 68 O1 G1 8 Ga c7 af bO 43 dO 21 a Oo
9040 Sf ed 5@ 4f 53 54 20 2F 6c 6F 67 69 be 2d 66 GF _-POST / login-fo
9050 72 6d 2f 20 48 54 54 5@ 2f 31 2e 31 Od Oa 48 6F rm/ HTTP /1.1--Ho
0060 73 74 3a 207777 77 2e 64 65 6d GF 2e 61 6d 69 st: www. demo.ami
0070 74 6a 61 6b 68 75 2e 63 6F 6d Gd Ga 55 73 65 72 tjakhu.c om: -User
0080 2d 41 67 65 be 74 3a 20 4d OF 7a 69 6c 6c 61 2F -Agent: Mozilla/
2090 35 2e 30 20 28 58 31 31 3b 20 4c 69 Ge 75 78 20 5.0 (X11 ; Linux
0020 78 38 36 Sf 36 34 3b 20 72 76 3a 36 30 2e 30 29 x86_64; rv:60.@) Ri
O ¥ HTTP sample.cap || Packets: 31 - Displayed: 2 (6.5%) || Profile: Default
im
—
ES


### Slides — strona 108

Filtering Traffi
— Wireshark
(MUTI Sample.cap = x“
File Edit View Go Capture Analyze Statistics Telephony Wireless Tools Help
A .pcap file can contain ZUd@ i FROCeef#F G52 aAQqQ8
thousands of packets, even Expression... +
(
after a few seconds of logging. No. Time Source Destination Protocol Length Info i
1 0.000000 172.42.0.157 81.218.31.137 TCP 66 38908 > 80 [ACK] Seq=1 Ack=1 Win=329 Len=0 a
; ae 3 3.426254 172.42.0.151 Ba 114 130 93 Trp 60 16852 + 8@ [ACK] Seq=1 Ack=1 Win=1023 Len=1
[to view the packets efficiently, | 4 3.488723 85.114.134.23 1 Mark/Unmark Packet 66 8@ + 16852 [ACK] Seq=1 Ack=2 Win=26@ Len=@ SLE=1
filters can be applied. Ignore/Unignore Packet
Set/Unset Time Reference
Time Shift...
i i Packet Comment...
Filters can also be applied 9 14.146553 172.42.0.157 1 74 60446 > 80 [SYN] Seq=@ Win=29200 Len=0 MSS=1460 S
during capture to prevent 10 14. 206035 172.42.0.157 1 Edit Resolved Name 74 60834 + 80 [SYN] Seq=@ Win=29200 Len=0 MSS=1460 S
the capture of unwanted 11 14.206138 172.42.0.157 1 Seq=0 Win=29200 Len=@ MSS=1460 S
12 14.218727 172.217.22.10 1 " . ACK] Seq=@ Ack=1 Win=60192 Len-o]il
packets. ‘ BNP PA SEEIES - Prepare a Filter » Not Selected ee y
- = Conversation Filter » ..and Selected
frame 3: 68 bytes on wire (4G bits )s GO Be. soa Conversation > or Selected
Ethernet II, Src: LefcHefe_7a:4b:17 (e8:6a =, , ‘and not Selected f 48:48)
Filters are logical conditions Internet Protocol Version 4, Sre: 172.42.0, ; fae ee
senne . collow ..0F not Selecter
that are applied using &&, | |, Transmission Control Protocol, Src Port: 1¢
stay dls 9000 78 32 1b d7 48 d@ e8 6a 64 7a 4b 17 08 Copy a
==, and '= 9010 00 29 ae Gc 40 00 80 06 C417 ac 2a "
0020 86 17 41 d4 e850 96 16 c9 If 18 5b fF rotocol Preferences
Brackets can also be used. 0030 @3 FF 6a 9e G8 28 28 20 20 20 20 20 Decode As...
| Show Packet in New Window
OQ F HTTP sample.cap || Packets: 31 - Displayed: 31 (100.0%) | Profile: Default
_
=,


### Slides — strona 109

Introduction to Wireshark
Wireshark includes many display filters. The following table lists some useful ones.
Logical Port Groups
Filter Data
Protocol Name Find a match for packets using a specific protocol (i.e. icmp, arp, http, dns).
ip.addr == 10.0.0.3 Find a match for this address on the source and destination.
ip.dst != 10.0.0.2 Find all matches that are not this destination.
ip.src != 10.0.0.3 Find all matches that are not this source.
tcp.port == 25 && tcp.port == 80 Find packets that match both specified port numbers in TCP.
udp.port == 53 || udp.port == 69 Find packets that match one of the specified port numbers in UDP.
udp.dstport == 25 Find packets that match a specific port number on the destination in UDP.
53


### Slides — strona 110

Introduction to Wireshark
— Wireshark
(A esas Foton HTTP Seam Gcptreame9 3): HTT Samplecap - 6 x
POST feo WTF zi
ee cr eae
Usa Agea: Mona's ct, Ux 866; 60.0) Geke/0400101 Feefo60.0
Reap ter appctenttamlapecanvenar0.7ge08
feepeianquage erena-03
After capturing traffic and few hin nroaiicononnod
— . : Fae eee yarn
filtering, stream inspection Sie rt nensnencnseerem serene ore ERENT
een ae
can be done. [eens teen
sma onkpasord-Aa2458RsubtLognkTP/Lt 200 0K
Emr type: te
"nd rg: ured
: ee
Streams are collections of op Ave: tnesutets
Dae an 20 fpr 2019 18:05:05 GT
Ess
packets from the same tose a, 18 Aug 205 201757 GT
os ro sites
conversation. ———
“100CTYPE unl PUBLIC"/WC/DTD YT 1.0 Tanston/E" "pf rR /OTD-rnstiona >
ah
. ‘ocinromn
Left-click a packet to choose Pcie,
the option to follow a stream, rr
. 1S Berne
which can be TCP, UDP, or HTTP. aoa
eesrnesneets-+
Sink efcevsyecas reo "eeshee peels >
<escurts->
Soke eee: 'src="httpi//ajax.qoogleapis.com/ajaxilibs/jquery/1.2.6/;query.min.js"> </script>
Unless traffic is encrypted, it “crip type—"terncrpt>
linear crest oe
should be readable. Fn er coe a AB ul
(ce gl Som nae te lS
ee [12]
[Reroute sum) [rae | [sown || mock || Gwe || hey
=


### Slides — strona 111




### Slides — strona 112

The Cisco IOS
ee ae. The objective of this lab is to learn how to use Wireshark
Network Examination with Wireshark and how computers encapsulate and send data.
30-60 Min.
i ; ® Become familiar with Wireshark.
— = @ Examine live Network.
$s S, 4 ¥ ® Capture and analyze.
i b NN ® e di
| ‘ » @ r ® Windows 7/8/10 @ Lab document
=~ 8 « ® Wireshark Installation file
e . | ® Web Browser
{ ; 4 . . is


### Slides — strona 113

Network Fundamentals
ARP


### Slides — strona 114

ARP and Encapsulation
Address Resolution Protocol
If a device wants to communicate with another device on the same
LAN, it must encapsulate the MAC address of the destination device.
To get the MAC address, it uses a protocol called ARP, that resolves a
logical address (IP) to a physical address (MAC), and saves the results
in the host ARP cache.
ARP operates in Layers 2 and 3 of the OSI model.
Every Layer 3 device uses ARP.
B
Switches make forwarding decisions based on the physical address of the frame.
58


### Slides — strona 115

—_ ARP Process
Scenario: Host A wants to communicate with minke
host B. Host A knows host B’s IP address but
not its MAC address.
lh, Ed
Step 1 - Host A sends an ARP Request to all hosts on £ 2 %,
the network (Broadcast), with Host B’s IP as the Sy = Ne XN,
destination MAC, requesting its MAC address. & XY 2 MX a NP %,
vy 5
tm
Step 2 - The switch forwards the ARP request
— LA | LB |
Step 3 - Host B recognizes the IP address in the LJ La L=
request, so it performs an ARP reply, in which it lists ESE Eee aon ee
its own MAC address. ARP Table:
Host IP MAC
Step 4 - Host A receives the ARP reply and saves |e | 1000.2 | aes |
host B’s MAC address in the ARP cache, together
with Host B’s corresponding IP address.
So


### Slides — strona 116

arp -a
The ARP table or cache is stored in C:\Windows\system32>arp -a
the RAM of the device.
The ARP contains three parameters: Interface: 10.71.0.110 --- @x17
* Destination host IP Internet Address Physical Address Type
* Corresponding MAC of that host 10.71.0.100 90@-7c-ac-a9-a2-c9 dynamic
. etialbrer wane 10.71.0.104 64-cc-24-96-8b-e0 dynamic
10.71.0.255 F¥-fFF-FF-FF-FF-FF static
224.0.0.22 Q@1-00-5e-00-00-16 static
arp —a and arp -g display the 224.0.0.251 Q@1-00-5e-00-00-fb static
host ARP table. 224.0.0.252 @1-@0-5e-00-20-fc static
SHOW amp dsplayea Chea deus 239.255.255.250 01-00-5e-7f-ff-fa static
ARP table. 255.255.255.255 F¥-FF-FF-FF-FF-FF static


### Slides — strona 117

C:\Windows\system32>arp -d
arp —d deletes the host ARP
table. 4
ame C:\Windows\system32>arp -s 10.@.0.2 Q@-aa-bb-11-22-33
arp —s adds a static entry to
the ARP table that resolves to
a specific IP address.
Note: Static ARP helps reduce
the risk of ARP spoofing
attacks.
arp inet_addr — defines a
specific IP address.
arp eth_addr - defines a
specific MAC address.


### Slides — strona 118

ARP and Encapsulation
Headers and Trailers are Adding Headers and Trailers Protocol Data Unit is a piece
control data added by to data is called of information added to or
protocols to the beginning encapsulation. Processing removed from a layer of the
and end of each data unit, in them and removing them is OSI model.
each layer. called decapsulation. PDU consists of protocol-
For example, IP packages Depending on the specific control information
the logical source and communication type, and user data.
destination address in an protocols in each layer add Examples are segments,
IPv4 header, and adds it to the correct header to the packets, and frames.
the data unit in the Network data unit. ,
Layer.

62


### Slides — strona 119

/ 4% ; a Vy Zs oe ?
7 4 : = / “oo : hie i
~ 4 Paty iy
a % , af . f
La =, > Pt @ 4
Y Ss oN N a SS
q ewan we & \ 3 a,
(Qed Bs by
NOABORE ie
' oe She ~ ey he ae
Se A = =
=== ar ag See _ + ae
| isl he a f
/; >
WW | :
uN . ron y ae a


### Slides — strona 120

a i ™" : = a aw NETWORK ee Bal Ci = L D


# Chapter 3: Switch & IOS Fundamentals


### Slides — strona 121

‘Cybersecurity Professional Program
. : e ;' 2 7 om C
Switch & IOS
Fundamentals
Computer Networking


### Slides — strona 122

Computer Networking
Introduction Network Switch & IOS Switch Securit IP and Routing
to Networks Fundamentals Fundamentals y Concepts
Diagnostics and VLANs Dynamic IPv4 & IPv6é Subnetting
Troubleshooting and Trunk Routing Static Routing Concepts
Access Infrastructure Fiival Proiect
Control List Services d


### Slides — strona 123

Switch & IOS Fundamentals
Overview
Lesson Objective
Switch Fundamentals
The objective of this lesson is to learn more
about the network switch and how it The Cisco 10S
operates.
It also covers Cisco's operating system and = ; ; ;
: ‘ : 3 Initial Device Configuration
configuration settings for Cisco and other
platform devices.
Managing IOS & System Files
G


### Slides — strona 124

OO
Switch & IOS Fundamentals
SWITCH FUNDAMENTALS


### Slides — strona 125

Switch Fundamentals
The Switch
Overview
Switches are smart Layer 2 devices with many ports designed to
forward frames from source to destination, according to specific MAC
a a addresses in the frame (Data-Link Layer).
Ee They include multiple technologies providing various capabilities.
Switches were developed to forward frames in accordance with their
destination addresses and MAC tables using a MAC learning process
known as forwarding decision.
B


### Slides — strona 126

The command used to display Switch#show mac address-table
the MAC address table is Mac Address Table
show mac address-table ee ee
MAC address tables include the Vlan Mac Address Type Ports
following columns: Sees Seesoeto eee ee ere ae SS eoe
¢ VLAN
, MAC adress 1 @0@1.97d7.45c3 DYNAMIC FaQ/5
ynamic or sane 1 @00@4.9a3d.bbc6 DYNAMIC Fae/4
¢ Associated physical ports
dl 000c.8500.13bb DYNAMIC Fa@/3
al 00de.978c.5698 DYNAMIC Fa@/2
DYNAMIC refers to a frame with a
source MAC that arrives at a switch
and updates the table with the MAC
address for that port.
STATIC indicates a manually configured
MAC address on a switch.


### Slides — strona 127

Switch Fundamentals
Switching Methods
Switching Methods
Switches have different methods of receiving and
transmitting frames on the LAN.
The following switching methods are used:
° Store-and-forward
& * Cut-through
. Fragment-free
é


### Slides — strona 128

Store-and-Forward Switching
Store-and-Forward Switching

. A switch using the store-and-forward method buffers the
entire frame upon receipt. This enables the switch to support
various port speeds. For example, a frame received on a 100

« Mbps ingress port can be transmitted via a 1 Gbps egress
port.

° Another advantage of this method is error checking, which

— can be done once the entire frame is buffered. The switch
— can easily detect frame errors using the FCS field.

° Although store-and-forward is relatively slow, it does provide
error checking and support for different speeds across
multiple ports. _

&


### Slides — strona 129

Cut-through Switching
Cut-through Switching
° Cut-through switching is a much faster method than store-
and-forward. In this method, only the first 6 bytes of the
mae incoming frame are buffered, meaning the switch only regards
A ‘ Dr the destination MAC address of the frame.
f \ ¢« — The switch forwards the frame immediately, even before the
{ | entire frame is received, and no error checking is done.
X A * Note: Modern switches can buffer up to 14 bytes of the
ll beginning of a frame, before deciding what to do with it.
° Although the advantage of cut-through switching is its speed,
a significant disadvantage is that most frames that reach the
destination host are corrupted due to lack of error checking.
6


### Slides — strona 130

Fragment-Free Switching

Fragment-Free Switching

° Fragment-free switching is a more advanced method.

¢ — This method buffers the first 64 bytes of the frame, including MAC address data and
the frame’s payload. The technique provides faster switching than the store-and-
forward method while also performing partial error checking to make sure there is no
fragmentation on the first 64 bytes of the frame.

. Fragment-free switching is therefore a better choice, as it is faster than store-and-
forward switching and provides partial error checking, unlike the cut-through method.

B


### Slides — strona 131

Switch Fundamentals
Half-Duplex Communication
| A connection for which the communication is restricted
to exchanging data in one direction at a time. For f| : fl ‘
= example, a walkie-talkie is a half-duplex device because =I ———————> =
only one person at a time can talk.
@ 3338 SS $388
Full-Duplex = =
Full-duplex means that data can be transmitted in both z > ra
directions, on a signal carrier, at the same time.
For example, a telephone is a full-duplex device - ~
because both users can talk at once. aon
@ ©)


### Slides — strona 132

Port Speed
Switch Ports
=> , Switch ports can transfer traffic at speeds of 10 Mbps, 100
2 ida Mbps, or 1000 Mbps.
: x aN The default is for the switch port to auto-configure its speed
X based on signaling between the port and the connected device.


### Slides — strona 133

Switch Fundamentals
Auto-Negotiation
Auto-Negotiation
via _ ;
Auto-negotiation tells connected devices to announce their
capabilities, and then, based on the settings of the interconnected
device at the other end, chooses the optimal speed and duplex
mode.
If one of the devices is configured with a different mode, a duplex mismatch will occur.


### Slides — strona 134

OO
Switch & IOS Fundamentals
THE CISCO IOS


### Slides — strona 135

Overview
Every network device, such as a switch or router, has an operating system
that tells it how to forward packets and execute network operations.
An operating system for a device is known as a Network Operating System
) (NOS).
An NOS does not operate in the same way as PC and server operating
systems.
An Internetwork Operating System (IOS) is a CLI-based system, and users
interface with it using text-based Cisco commands.
&


### Slides — strona 136

The Cisco IOS
The Cisco IOS
Overview
Most Cisco devices, regardless of their size or type, run the IOS,
ors which is an advantage due its singularity and familiarity.
—————— While all devices come with a default IOS and feature set, it is
_—-— possible to upgrade the IOS version or feature set to obtain
a additional capabilities.
This course focuses on versions 12 and 15.
6
The versions of the IOS may be different, depending on the device hardware.


### Slides — strona 137

The Cisco 10S
The Cisco IOS
10S or iOS
IOS VS. iOS
otfnotfte ¢
Cisco.
Internetwork Operating System


### Slides — strona 138

The Cisco IOS
IOS Interface Features
Command Line
IOS uses a command line interface (CLI) to enable administrators and technicians to
interact with the system via special Cisco commands.
CLI
K)>) \ CLI is a means of interacting with programs by entering commands on a command
= line. Using a CLI-based system has many advantages, such as minimum resource
usage, faster ability to operate on the system, and others.
Terminal Emulation
f[s——) Many network devices are configured and managed using Terminal Emulation (TE)
software, such as PuTTY. TE programs enable configuration of local devices using a
=== serial cable or a remote management protocol, such as SSH.


### Slides — strona 139

The Cisco IOS
Terminal Software
PuTTY PuTTY
Pul TY is a versatile tool for remote access to another —
mn computer. It is often used by people who want secure [ie eal
remote shell access to a UNIX or Linux system, though that | tae ee e—]
is only one of its many uses. vy ‘a San Sena aso @sst Osou!
he Te Term is an open-source, free, software-based = i Sere
terminal emulator (communication) program. It ee
[7] emulates different types of computer terminals, from oo ee
£———)_:~SsCDEEC VT100 to DEC VT382, and supports Telnet, SSH 1 — =
and 2, and serial port connections. a |
SecureCRT tO
SecureCRT is a commercial SSH and Telnet client and
5 terminal emulator by VanDyke Software. Originally a
Windows product, VanDyke recently added Mac OS X
and Linux versions. vy


### Slides — strona 140

Cisco Packet Tracer
Overview
Cisco Packet Tracer allows the user to map a network.
Packet Tracer enables the testing of network configurations,
trains users to work with network configuration, helps them
understand how a network operates, and provides them with
network deployment experience.
2)


### Slides — strona 141

The Cisco IOS
ce eee ft Create a Cisco account and download Packet Tracer to
Packet Tracer Installation explore the features it provides.
30-60 Min.
r @ Register the account.
- 7 ® Download Packet Tracer.
. ia 4 —_ @ Install Packet Tracer.
; ® Web Browser ® Lab document
®
,.
a .
~ iY ol


### Slides — strona 142

The Cisco IOS
Gut-of Band Console Cable

This method uses a dedicated management console

cable that must be physically connected to the device.

Initial configuration is usually done using this method. <3

In-Band ee y
This method uses management protocols, such as SSH Ne)
or Telnet, which access the device remotely over the . E |
network. —
@ </>


### Slides — strona 143

The Cisco IOS
How Local Configuration Works
© Out-of-Band management requires two main items:
ie e PC with terminal software
* Console cable
Terminal
A network device is like a PC, but without a mouse,
— keyboard, and screen. A PC with a terminal provides a
= way to input commands and view output from the
device. eo
Console Cable
A console cable or management cable is like a bridge
between the PC and the device. Almost every device has
a designated console cable for this purpose. Older cables
use an RS-232 connector; modern ones use USB. y,


### Slides — strona 144

The Cisco IOS
IOS Modes
Permissions
__ IOS can operate in one of three work modes, each with different capabilities and
— permissions. For example, one mode may have a lower level of privileges compared
= with another mode.
Modes
The division of modes is meant to separate the management levels and increase the
efficiency of network device security and configuration.
Structure
Cisco IOS modes have a hierarchical structure and are similar among switches
and routers.


### Slides — strona 145

The Cisco IOS
IOS Modes
User EXEC Mode
> This mode has low-level capabilities but is useful for basic operations. It has a limited
number of monitoring commands and does not allow device configuration changes.
Privileged EXEC Mod
This mode has a large number of monitoring commands and device configuration
# viewing commands (show commands). It also enables file management operations,

such as device configuration backups and IOS upgrades.


### Slides — strona 146

The Cisco IOS
IOS Modes
Global Configuration Mode
‘ Global configuration is the only mode that allows administrators to change device
(config) # configuration. This mode is only accessible from the privileged EXEC mode.
Interface Configuration Mode
The interface mode allows you to change specific parameters within a switch or
router.


### Slides — strona 147

Q
Navigating the system and Switch>enable
understanding the difference Switch#configure terminal
between the modes is very Enter configuration commands, one per line. End with CNTL/Z.
important when working in the
system. . . .
Switch(config)#exit
The default display name of a device Switch#exit
appears before the prompt. In the Switch>
example at right, the name is Switch.
The enable command moves the user
from user mode to privileged mode.
The configure terminal command moves
the user from user mode to global
configuration mode.
The exit command takes the user
one mode back.


### Slides — strona 148

Example
Incomplete Command i
Switch>di
% Ambiguous command: "di"
The command is correct but not complete.
(38) Switch#show
WV %Incomplete Command.
Ambiguous Command Switch(config)#hostname S1
Not enough characters were entered for the command ; . ‘ vat
x to be recognized. Or, more than one command exists % Invalid input detected at
. marker.
with the same name.
A
Invalid Input
The command was entered incorrectly (i.e., typo) or
inserted in the wrong mode.


### Slides — strona 149

The Cisco IOS
Hotkeys and Shortcuts
. | | Break sequence used to abort DNS
TAB Completes partial entry. lookups, traceroutes, pings, etc. alleles
CTRL+D__ Erases the character at the cursor. | | Erases the word to the left of the CTRL+W
cursor.
CTRLEK Erases all characters from the cursor Recalls a command from the history eee 8
to the end of the command line. buffer. id
Erases all characters from the cursor Ends configuration mode and returns
FSC +P to the end of the word. to privileged EXEC mode. lal


### Slides — strona 150

The Cisco IOS
Cisco Device Components
eS
oh tl
Volatile memory that Non-volatile memory Non-volatile memory Non-volatile memory
stores the system responsible for the that stores the operating that stores the startup
configuration (running- Power-On Self-Test system itself (IOS). config file.
config) and tables (such (POST) process and
as the MAC table). bootstrap, which is the
initial program
responsible for booting
the IOS.


### Slides — strona 151

The Cisco IOS
POST
POST and bootstrap program load: This part of the
sequence checks the CPU, RAM, and NVRAM. When iin,"
; ? Load IIOS
done, the device copies the bootstrap program from ;
the ROM to the RAM. Load IOS: After copying the bootstrap program
from the ROM to the RAM, the IOS (which is still
stored in flash memory) is copied to the RAM for
execution.
Load Configuration
Load configuration: The bootstrap program now
copies the startup configuration file from the
NVRAM to the RAM.


### Slides — strona 152

OO
Switch & IOS Fundamentals
INITIAL DEVICE CONFIGURATION


### Slides — strona 153

hostname <device name>
Switch(config)#hostname S1-Floor1
S1-Floor1(config)#


### Slides — strona 154

username <user-name> password <password>
Switch(config)#username Admin password p@nd@
Switch(config)#username Peter password Spiderm@n


### Slides — strona 155

enable password <password>
Switch(config)#enable password c!sc@


### Slides — strona 156

banner motd #security-message#

Switch(config)#banner motd #Access to this device is for authorized personnel only!#
Press RETURN to get started!

Access to this device is for authorized personnel only

User Access Verification

Password:


### Slides — strona 157

service password-encryption
Switch(config)#service password-encryption


### Slides — strona 158

copy running-config startup-config
Switch#copy running-config startup-config


### Slides — strona 159

line console 0 & login local
Two steps are performed to enable Switch(config)#line console @
local credential (username and Switch(config-line)#login local
password) authentication on the Switch(config-line)#exit
console port.
1. Enter the console port config
mode (line mode).
2. Enter the local login and exit.
Note: Besides the local login
command, there is a login
command that enables only
password checking.


### Slides — strona 160

S$1-Floorl#show running-config
Building configuration...
All configuration changes are Current configuration : 1234 bytes
immediately saved in the !
running-config file. version 12.2
service password-encryption
!
To display them, run the show hostname! Si-Flooril
running-config or show run !
command. enable password 7 @822@D5D0A49
!
Note: The example on the right username Admin privilege 1 password 7 08316C400D39
is a brief glimpse of the actual !
file. banner motd #Access to this device is for authorized personnel only!#
!
line con @
line aux @
Line vty @ 4
login


### Slides — strona 161

Initial Device Configuration
eee Learn how to set basic configurations on a switch using
Initial Cisco Cisco lIOS commands.
Device Configuratio ‘
30-60 Min. ( . aap |
} ®@ Access the device.
2 ' ® Navigate the IOS.
ee, ~ " ~ ® Configure initial and security settings.
(Ci ee if 0, @ Alternate PKA opening
| a» " ® Cisco Packet Tracer 7.2.2 @ Lab document
: a 4 ® or later @ NET-03-L2.pka
4 ‘ :
| r ’ |
| a x —
‘ ia —


### Slides — strona 162

OO
Switch & IOS Fundamentals
MANAGE IOS & SYSTEM FILES


### Slides — strona 163

TFTP
Trivial File Transfer Protocol (TFTP) is a simple file transfer
protocol that allows clients to retrieve files from a remote host or
—_ transfer files to a remote host.
TFTP can also be used to remotely start a computer, back up network
or router configuration files, and upgrade a device’s IOS.
o)
TFTP relies on UDP to transport data and uses port number 69.


### Slides — strona 164

copy running-config tftp
Switch#copy running-config tftp:


### Slides — strona 165

NGreTEl a a : Ril#copy running-config tftp:
| ote: First save t S Senneuration Address or name of remote host []? 192.168.1.3
ocally using: copy running-config . . . .
startup-config Destination filename [R1-confg]? R1-config-backup2e.9
; Writing running-config....!!
Step 1: Copy the file to the server. [OK - 1362 bytes]
Step 2: Enter the TFTP server IP
address.
Step 3: Select the name of the file
saved on the server.
Backing up the IOS file is almost
the same. You only need to
replace the source location of the
file, meaning flash: instead of
running-config


### Slides — strona 166

Step 1: The command copy tftp: Ri#copy tftp: flash:
flashzis.used to copy the new IOS Address or name of remote host []? 192.168.1.3
file from a TETP server to the flash Source filename []? c1901-imoversa;19.mz.SPA.152-4.M3.bin
memory. Destination filename [c1901-imoversa;19.mz.SPA.152-4.M3.bin]?
Step 2: Upgrading the device can Accessing tftp://192.168.1.3/ c1901-imoversa;19.mz.SPA.152-4.M3.bin...
be performed after copying the Loading c1901-imoversa;19.mz.SPA.152-4.M3.bin from 192.168.1.3:
new IOS to the device using the PEEPPEP EP PPP ere r rrr errr epee errr errr pepe rrr reer rrr ere rrr erry
boot system command. This [OK - 4670455 bytes]
command tells the device which
10S file to load on the next R1# Configuration terminal
startup. R1(config)#boot system flash@://c1901-imoversa;19.mz.SPA.152-4.M3.bin
R1(config)# exit
Step 3: The command copy Ri#copy running-config startup-config
running-config startup-config is R1i#reload
used to save the current
configuration to the startup
configuration and reload the
device for the new IOS to load.


### Slides — strona 167

ROMmon
What Does ROMmon Do?
_ The purpose of the Read-Only Memory MONitor (ROMmon)

| configuration register is to change the router’s behavior in several ways:
(le :[B]:] = Determine how the router will boot.
a —" ¢ Apply options while booting (such as ignore configuration).
a ——"

e Set the console speed and band rate for terminal emulation sessions.

&


### Slides — strona 168

Router(config)# config-register 0x2102
Router(config)# end
In the configuration terminal Router# copy running-config startup-config
mode, we can change the register Destination filename [startup-config]?
value, which will affect the next Building configuration
boot process. [OK]
Router# Reload
In the example on the right,
we change the register
value to the default 0x2102,
and save the configuration
in startup config, which will
set default factory settings.


### Slides — strona 169

Manage IOS & System Files
The default configuration register is Ox2102. We can verify this using the command.
Using the command , we can change the register value and the router’s behavior.
Common Settings
Register Value Device Behavior

0x102 * Ignores break key
* 9600 console baud rate (maximum transfer rate of the console port in bits per second; in this case, 9600)

0x1202 * 1200 baud rate
* Boots into bootstrap
* Ignores break key

Ox2101 * Boots into ROM if initial boot fails
* 9600 console baud rate
* Default register value

0x2102 * Boots into ROM if initial boot fails
* 9600 console baud rate default value for most platforms


### Slides — strona 170

Router#show version
<output omitted>
Cisco IOS Software, 1841 Software (C1841-IPBASEK9-M), Version 12.4(12), RELEASE SOFTWARE
(Giteil))
By entering the command show Technical Support: http://www. cisco.com/techsupport
. . Copyright (c) 1986-2006 by Cisco Systems, Inc.
version we can verify the Compiled Mon 15-May-@6 14:54 by pt_team
configured register value.
ROM: System Bootstrap, Version 12.3(8r)T8, RELEASE SOFTWARE (fc1)
System returned to ROM by power-on
We can also display additional System image file is "flash:c1841-ipbasek9-mz.124-12.bin"
information, such as the
software type and version. Cisco 1841 (revision 5.0) with 114688K/16384K bytes of memory.
Processor board ID FTX@947Z18E
M86@ processor: part number @, mask 49
2 FastEthernet/IEEE 802.3 interface(s)
191K bytes of NVRAM.
63488K bytes of ATA CompactFlash (Read/Write)
Configuration register is @x2102


### Slides — strona 171

ManageJOS & System Files
—— Use a TFTP server to back up and roll out switch
Backing up Config Files configurations.
and Managing the IOS ‘
30-60 Min. ( . ee uration f
; @ Back up configuration files.
' @ Back up and upgrade the device ISO.
re 4 é yl.” ~~
; rd ae ~ N e yr
| M Md ® . ® Cisco Packet Tracer 7.2.2 ® Lab document
: aw 4 & or higher @ NET-03-L3.pka
‘ ; :
| r ’ |
‘ ia —


### Slides — strona 172

/ 4% ; a Vy Zs oe ?
7 4 : = / “oo : hie i
~ 4 Paty iy
a % , af . f
La =, > Pt @ 4
Y Ss oN N a SS
q ewan we & \ 3 a,
(Qed Bs by
NOABORE ie
' oe She ~ ey he ae
Se A = =
=== ar ag See _ + ae
| isl he a f
/; >
WW | :
uN . ron y ae a


### Slides — strona 173

a i ™" : = a aw NETWORK ee Bal Ci = L D


# Chapter 4: Switch Security


### Slides — strona 174

osal l
; 2 _ —I iy
aa ; 7 — Le 3 ieee
_ i — a ont. NETWORK ei Bee _ ¢ ; a)
af K 4
a: SWITCH SECURITY
Computer Networking


### Slides — strona 175

Computer Networking

Introduction Network Switch & IOS Griavdnaanrit IP and Routing

to Networks Fundamentals Fundamentals y Concepts
Diagnostics and VLANs Dynamic IPv4 & IPv6é Subnetting
Troubleshooting and Trunk Routing Static Routing Concepts

Access Infrastructure Fiival Proiect
Control List Services d
2


### Slides — strona 176

Switch Security
Overview
Lesson Objective
The objective of this lesson is to learn new
ways to secure a switch from unwanted access. Port Security
The lesson explains how the Port Security
feature helps prevent access by unauthorized
MAC addresses, and how to establish secure Remote Access
connections over the network.
G
3


### Slides — strona 177

CO
Switch Security
PORT SECURITY


### Slides — strona 178

Port Security
Risks in a Switched Environment
MAC Spoofing
MAC spoofing is when attackers change their own physical PC address to conceal their
_ true identity and pose as someone else. For example, an attacker may spoof a MAC
address with a legitimate MAC address, to bypass an access control mechanism, such as
port security.
CAM Table Overflow
® | CAM Table Overflow is an attack that targets a switch’s MAC table. The idea is to flood
= — the table with a large number of fake addresses. When the list of addresses exceeds the
maximum size of the table, the switch will initiate its fallback mode and begin to act as a
hub, meaning every frame will be forwarded to every host on the network.
5


### Slides — strona 179

Port Security
Overview
The Port Security feature is used to restrict input to an interface by
limiting MAC addresses of workstations that are allowed to access a
specific port.
When secure MAC addresses are assigned to a port, the port will not
forward packets with source addresses outside the defined group.
6
By default, port security is not defined on switches and requires configuration.
6


### Slides — strona 180

Port Security
Violation Modes
Shutdown
This is the default violation mode. When a violation
occurs, the port will be shut down and logged
automatically. The port must then be reset manually to
become operational again.
@ The port security feature includes
Restrict three protection modes to handle
1 | | | In case of a violation, Ethernet frames with incidents in which it receives an
! unauthorized source MAC addresses are dropped. The Ethernet frame with a restricted
a switch provides notification of security violations and MAC address.
keeps count of the number of violations. yi
Protect
In case of a violation, Ethernet frames with
unauthorized source MAC addresses are dropped. In
this violation mode, the switch does not provide
notification regarding the event. yi
re


### Slides — strona 181

Port Security
MAC address learning can be performed in one of two ways: Manual or Sticky.
Manual
© The manual method requires static configuration of each allowed MAC address and its
assignment to an interface. This is the most secure method, but it is very time consuming
7) and open to faulty configuration.
Sticky
In the sticky method, allowed MAC addresses are learned dynamically and are limited to
the maximum number configured for the interface. The switch learns the source address
of the first few devices associated with the interface, providing a fast and scalable
l= method of operation.
8


### Slides — strona 182

Max Allowed MAC Addresses Raitt statis
Switch# show interfaces
Although the number of default MAC addresses allowed fastEthernet @/1 status
in Port Security is one, the number can be changed
within the range of 1 to 3072. Port Status
a FaQ@/1 err-disabled
Err-disabled

When a switch port is in Err-disabled mode, the

port may have been disabled automatically by the

switch operating system, due to port security

shutdown mode violation.

@ [el
To determine if Err-disabled was turned off for a port, run the show interfaces [interface] status command.
5


### Slides — strona 183

Port Security
Duplex Mismatch
sd 9 Q This state occurs when two parties, set for point-to-point CEchonnetO/A in Sumy [ eae pee Ce ae EERE]
ele . . . . 100000 Kbit, DEY 1000 usec,
communication, are configured to use different duplex gq TREAT Ay as6 (298) ekipedia 7s, cmetosat/25s
modes. wibauple, 100%b/e"
Sb type: ARPA, ARP Pimeout OA0000
Bad NIC Se ee
A faulty network interface card with software or hardware fh Toast oticinen situ ce likie cancicton
issues may trigger the Err-disabled state.
Err-disabled may be triggered due to
Broadcast Storms reasons other than Port Security.
» When there is a broadcast volume too large for processing
in the broadcast domain, the switches may be
overwhelmed and trigger the err-disabled mode on their
os ports.
10


### Slides — strona 184

Port Security
Port Security Requirements
Access Mode
Access ports are responsible for traffic flow.
Access mode should only be defined on ports connected to endpoint
devices, such as PCs.
You can configure port security on interfaces that you configured as
access ports with access mode.
e
Kul


### Slides — strona 185

Switchport mode access
switchport port-security
Enabling port security is done
in the interface configuration Switch(config)# interface fastEthernet @/1
mode, which is set using Switch(config-if)# switchport mode access
: Switch(config-if)# switchport port-security
Switch(config-if)#
Then, Access mode needs to be set
with fs
For port security to operate correctly,
the interface must be configured as
an Access port.
Finally, Port Security can be
enabled on the interface using
the command


### Slides — strona 186

switchport port-security [configuration] [value]
Port Security is configured by setting Switch(config)# interface fastEthernet 0/1
up each component individually Switch(config-if)# switchport mode access
using the same structure. Switch(config-if)# switchport port-security
z ORR RR KE BOR OR BR RK RK EK OK KE KK KK KK KKK KK KKK KK KKK KK KKK KKK KK KK KKK KK KKK KKKEKKEK
defines the type of
violation rule to be applied to
the port. Switch(config-if)# switchport port-security violation restrict
Switch(config-if)# switchport port-security mac-address sticky
The commands Switch(config-if)# switchport port-security maximum 5
and define sticky
learning, up to a maximum of
five addresses.


### Slides — strona 187

Switch# show port-security
Presenting the authorized MAC Secure Port MaxSecureAddr CurrentAddr SecurityViolation Security Action
addresses associated with a port (Count) (Count) (Count)
and the type (sticky or manually) ooo eee eee eee eee eee eee eee eee eee eee
is done with the command FaQ/1 5 1 @ Restrict
Fa@/2 al () 2) Shutdown
If only an overview is needed,
can be run Switch# show port-security address
for a quick overview of the Secure Mac Address Table
configuration. PRED I2S eee
Vlan Mac Address Type Ports Remaining Age
To view a specific interface, the (mins)
command _ a a a oO ee
should be 1 Q002.1798.DAC6 SecureSticky FastEthernet®/1 =
used, since it provides more 1 Q090.2172.8736 DynamicConfigured FastEthernet@/2 =
information. nnn IIS
Total Addresses in System (excluding one mac per port) : O
Max Addresses limit in System (excluding one mac per port) : 1024


### Slides — strona 188

Port Security
2 eee The objective of this exercise is to implement Port Security
Configure and Verify Port Security ona switch, pigetes using Port Security options, and learn
= | how to verify settings.
30-60 Min. _
i . ®@ Configure & Verify Port Security
a ’ =; "
ia >»
i b NN s e yr
| ‘ ‘Ss i) _ i 3 ® All platforms @ Lab document
= 88 W ®@ Cisco Packet tracer 7.2.2 @ NET-04-L1.pka
; ‘i } and higher
: :


### Slides — strona 189

CO
Switch Security
REMOTE ACCESS


### Slides — strona 190

Remote Access
Overview
Today, other than for initial configuration, most access to deployed
Y switches is done remotely.
Remote access allows administrators to manage and monitor their
_ network devices from anywhere in the network.

ba This is important, since some switches may be located in physically

inaccessible areas.
Two common remote access protocols are used in switches today: SSH and Telnet.
Le


### Slides — strona 191

Remote Access
Telnet Vs. SSH
Telnet and SSH are the two most widely used CLI-based remote access protocols.
Telnet
Telnet was developed many years ago to allow users to manage devices from anywhere,
)) via a simple and minimal configuration. However, using Telnet involves a potential
security risk because usernames and passwords are sent in plain text on TCP port 23.
SSH
lolonolon oo, . Lag .
pul md SSH is similar to Telnet, but with a significant difference: SSH encrypts all data transferred
mi ttt between the user and end device. SSH uses RSA encryption, a robust and reliable
He TOOlIN encryption type. It operates on TCP port 22.
18


### Slides — strona 192

Remote Access
SSH Encryption
RSA Encryption
Modern encryption relies heavily on the RSA algorithm since most
methods use public and private encryption keys.
Z The public and private encryption key method, also known as
€ ) asymmetric cryptography, uses two different, but mathematically
linked, keys.
9 ..- 7 The public key is shared with everyone, while the private key is only
given to specific persons.
RSA ensures implementation of the CIA triangle, and avoids
authentication rejection.
B
19


### Slides — strona 193

Remote Access
SSH Encryption
RSA Encryption
Protocols like SSH and SSL/TLS use RSA to encrypt communication
and digital signatures.
Although RSA works through the computational difficulty of factoring
a large integers, computational complexity grows exponentially every
€ ) day, and larger and larger numbers are required to maintain secure
communication.
? ../.- 7 RSA is dependent on a powerful computational system. The more
complicated the keys are, the more power is required.
Recently, ECC (Elliptic Curve Cryptography) is becoming more
popular, since it can create faster, smaller, and more efficient
cryptographic keys.
B
20


### Slides — strona 194

—_— Encryption/Decryption Process
Asymmetric encryption is when two Public key
different keys are used to encrypt and £
decrypt messages.
The keys are mathematically related in a
way that messages encrypted with one
My 2 e ° yp af & A Decryption af
key, typically the public key, cannot be
CLEAR toro! CLEAR
decrypted by it. | er Encryption [izes a | atl
The decryption can be done only using the
corresponding private key in the key pair.
This method is considered to be more Private key
complex and slower than symmetric
encryption, which uses one key for both
encryption and decryption. fal
_
Data transfer
ee
Key publicly available Pr
Pail


### Slides — strona 195

Remote Access
Virtual Teletype
eee . . . . .
Virtual Teletype (VTY) is a command-line interface (CLI) in network
devices used to create remote access connections.
VTY is virtual and does not require any hardware.
Switches have 16 VTY lines (0-15), routers have 5 VTY lines (0-4).
22


### Slides — strona 196

Switched Virtual Interface

The primary purpose of creating a computer network is to share
resources and enable communication within the network.

oO Layer 2 switches create VLANs (Virtual LANs) that form a single

} ) broadcast domain. If a broadcast message is sent within the same
t- — VLAN, all devices connected to that VLAN will receive the message.
—O—————__ Hosts can communicate on the same VLAN without a Layer 3 device
(router). Devices on a different VLAN, on the other hand, cannot
communicate with each other, without proper routing.
&
23


### Slides — strona 197

Switched Virtual Interface

A router or Layer 3 switch can handle network segmentation and
inter-VLAN communication.
A router can segment a network and create separate broadcast

re) domains, with each network segment using a different sub-interface

) of a physical interface on the router.
t- — _ Layer 3 switches require the creation of multiple VLANs on the
5° o- switch, which form multiple broadcast domains. Then, for each
VLAN, a corresponding Layer 3 interface needs to be created on the
switch, to handle the routing.
This Layer 3 interface is the SVI.
The difference is that the SV! Layer 3 interface is virtual.
&
24


### Slides — strona 198

Remote Access
SSH Configuration
Ol Change the default hostname. | | Set a security message. 05
Q2 Create a user account. | | Enable VTY lines and limit protocol access. 06
03 Set the enable password. | | Enable Layer 3 connectivity. OT
QA. Configure a domain name. | | Generate SSH keys. 08
25


### Slides — strona 199

Switch(config)#hostname S1
S1(config)#username Admin password p@nd@

Several initial settings must be S1(config)#enable password c!sc@

configured before enabling SSH : : F

on the device. S1(config)#service password-encryption
S1(config)#banner motd #Access to this device is for authorized
personnel only!#

1. Setithe:device name. S1(config)#ip domain-name CyberPro.com

2. Create a local account.

3. Secure the privileged mode.

4. Set an appropriate security

message (optional).

5. Set a domain name.


### Slides — strona 200

line vty <id-range> & login local
Step 1 - Enter the VTY configuration S1(config)#line vty @ 15
triode. Selerkeheaiimilier Sf S1(config-line)#login local
maximum sessions. r : :
S1(config-line)#transport input ssh
Step 2 - Enable authentication S1(config-line)#exit
using username and password.
Step 3 - Telnet is enabled by default;
the transport command prevents
using Telnet and only uses SSH for
remote connections. The options are
none, all, Telnet, or SSH.


### Slides — strona 201

interface vlan 1

ip address <ip-address> <subnet-mask>
S1(config)#interface vlan 1

S1(config-if)#ip address 10.0.0.150@ 255.255.255.0
S1(config-if)#no shutdown

S1(config-if)#exit

S1(config)#ip default-gateway 10.0.0.1


### Slides — strona 202

crypto key generate rsa
The crypto key command generates S1(config)#crypto key generate rsa
the Private and Public RSA keys on The name for the keys will be: S1.CyberPro.com
the networkideyice. The switchior Choose the size of the key modulus in the range of 360 to 2048 for
router needs those keys to secure
the SSH session. your
General Purpose Keys. Choosing a key modulus greater than 512 may
take
Set the key length. The default is a few minutes.
512, but it is recommended to set
the number of bits to higher than How many bits in the modulus [512]: 1024
1024. The maximum value is 2048. % Generating 1024 bit RSA keys, keys will be non-exportable...[OK]


### Slides — strona 203

S1#show ssh
Connection Version Mode Encryption Hmac State
Username
The show ssh command 2 1.99 IN aes128-cbc hmac-shal Session
presents the active SSH sessions Started Admin
on the network device. 2 1.99 OUT aesi128-cbc hmac-shal Session
Started Admin
%No SSHv1 server connections running.
Show ip ssh displays the version oe
definition, authentication
timeout, and retries.
S1#show ip ssh
SSH Enabled - version 2.0
Authentication timeout: 128 secs; Authentication retries: 3


### Slides — strona 204

GE Administrator: Command Prompt - ssh -I root 192.168.137.129
Microsoft Windows [Version 10.0.18362.239]
(c) 2019 Microsoft Corporation. All rights reserved.
Accessing the device remotely IC: \Windows\system32>ssh -1 root 192.168.137.129
using SSH can be done using a root@192.168.137.129's password:
CLI, such as PuTTY or a device
terminal.
The universal command for creating
an SSH session is: h
ssh -1 <username> <target-ip>
In the example on the right,
the command is executed in
Windows CMD.


### Slides — strona 205

Remote Access
The objective of this exercise is to set up the SSH service on network
pen VWaVayay : devices for remote management from anywhere on the network. In
Remote Access with SSH | addition, this exercise practices configuring IP connectivity to a Layer 2
30-60 Min. A : switch using the In-Band Management method.
=e ® Configure SSH.
. 4 ‘ @ Verify SSH configuration.
—— ® $ di
| i) a J ® All platforms ® Lab document
; W | ® Cisco Packet Tracer 7.2.2 @ NET-04-L2.pka
or higher
4
| |
l iY |
{ \ ) Fy ™ “= roy


### Slides — strona 206

’ = j FO Saw ~
= a # 4 i
4 ~~ ie
v). a " % * a4 a A
i >» ; Ss
> \ >
Chie —— . =
Fed Axncoes ta os 2 Spe
& Mh if
A ; 4 ~S : ra
=m Z By: ie ~~ zs
= Payee SQ


### Slides — strona 207

a i ™" : = a aw NETWORK ee Bal Ci = L D


### Slides — strona 208

<a = —— :
il LAYS) ea IDESIGN - ‘ ¥ = =
= IP. & ROUTING =
Computer Networking
Copyright © 1996-2023 HackerU Ltd. All Rights Reserved.


# Chapter 5: IP & Routing Concepts


### Slides — strona 209

Computer Networking
Introduction Network 10s Switch Securit IP & Routing
to Networks Fundamentals Fundamentals y Concepts
Diagnostics & Dynamic F :
Troubleshooting VLANs & Trunk Reuiting Static Routing Subnetting
Access Infrastructure
Control List Services


### Slides — strona 210

Computer Networking
Overview
Lesson Objective ’ ’
Decimal, Binary, and Hex
In a network, IP addresses are used to The Router
identify a device’s source and destination.
The object of this lesson is to understand Routing Process
routers, how they work, their processes, and
the logic involved in IPv4/6 configuration.
G


### Slides — strona 211

OO
IP & Routing Concepts
DECIMAL, BINARY, AND HEX


### Slides — strona 212

Decimal
fExaail The most common numbering system consists of ten numbers, 0-9, and it is called the decimal
‘|= em. system. The system is based on the 10 fingers we use to count and is known as the base-10
S| | numeral system.
Binary
Binary is an alternative number system that consists of only two numbers: 0 and 1. This system
is used by computers, which communicate by transmitting negative and positive electrical
currents. Because there are only two numbers, the system is known as the base-2 numeral
system. a
Hexadecimal
Hex, or Hexadecimal, is a number system that consists of 16 characters, and is known as the
base-16 numeral system. Hex uses the numbers 0-9, followed by the letters A-F. Hex is widely
used as an alternative representation to binary, since it is a more human-oriented system.


### Slides — strona 213

Decimal, Binary, and Hex
Positional Notation
Positional Conversion
When learning about number systems, a The Digits: Bt (2) al i
good way to approach them is to consider 02 The Positions: 23 22 21 20
numbers a result of their positions. $5 es
Base2 The Result: 8 i) zz i
Each number’s value can be calculated as
a result of a function. The Digits: 1 e 5 4
10 The Positions: 107 102 10: 10°
The function is the same regardless of the TT
base being used, making it easier to perform Base10 The Result: 10ee @ 220 4
base transitions.
The function is: The Digits: B a ) 5
[number] = [digit] * [base] “ [position]. 1 6 The Positions: 163 162 161 162
Baseié The Result: 45056 256 2) 5


### Slides — strona 214

Decimal, Binary, and Hex |
Binary to Decima
found. The next step is conversion, summarizing each of the individual values to get the result.
Conversion Formula
Positional Value 128 64 32 16 8 4 2 1
Result 128+64+0+16+0+4+0+0=212
EEE


### Slides — strona 215

Decimal, Binary, and Hex
Positional Conversion
While the aim of ion to decimal is t oe 20= 1024 ” 28
ile the aim of conversion to decimal is to - -
solve a formula, the aim of conversion from 1024 8
decimal is to find the missing variable. 970 29=512 2 21=2
“512 “2
The operation can be summed up as find
the X that will result in the closest number. 458 28=256 (3)
; 256
For example, when converting the number 32 16 8 4 2 1
1994 to binary, the first step is to find X, 202 27=128
where 2% is the closest to 1994. _ a 0 ri a 4“ 6
128
Continuing this process, the number should 74 26=64
be written down and the calculation should = 2048 1024 512 256 128 64
be repeated for the remainder. 64
10 27=8 0 41 1 1 i 1


### Slides — strona 216

Decimal, Binary, and Hex
Division Calculation
For binary, there are some tricks that can
make the calculation easier, instead of me oe p ‘ ‘
having 16 Buess 62. 124 249 498 997 1994
One trick is to take the desired number i) 1 i) 1 i)
and divide it, without the remainder,
while recording each operation.
If the result is even, write a O. If it is odd, 1 3 S 15 31
write a 1. The binary representation will
appear when the operations are done.
1 i A 1 iL
For other bases, there are other tricks and
mathematical methods.
11111001010


### Slides — strona 217

Decimal, Binary, and Hex i |
Binary to Hexadecima
considered a representation of 4 binary digits. For example, 101110 is 0010 + 1110, making it 2E in hexadecimal.
Conversion Formula
Number 0 1 2 3 4 5 6 7
Hexadecimal 0 1 2 3 4 5 6 7
Number 8 9 10 11 12 13 14 15
Hexadecimal 8 9 A B € D E F
Eze


### Slides — strona 218

Decimal, Binary, and Hex
Hexadecimal Conversion
Binary to Hex
¢ Divide the binary number into groups of 4 digits.
b04%00%:| © Convert each group to its equivalent hex value using the Base Comparison table.
¢ Merge the results of each group.
Example
Convert 0111111111010100 to hex.
A OR] e 0111 1111 1101 0100
* 0111 =7, 1111 =F, 1101 =D, 0100 =4
° Answer is 7FD4 eo


### Slides — strona 219

Decimal, Binary, and Hex
Other Bases
Base-X
There are other bases besides binary, decimal, and hexadecimal.
Throughout history, other counting systems, such as base-6, base-8,
and base-12 were developed.
Old British measurements, such as dozen (12), gross (144), and feet
(12 inches) are suspected to have been originated by a base-12
number system.
&


### Slides — strona 220

ox ae . et el 7 The objectives of this exercise are to understand
Converting Decimal, Binary, and Hex numbering systems and how to convert between them.
30-60 Min.
= a r yA ' 7 Convert Decimal to Binary
, ’ « ; ® Convert Binary to Decimal
mi ee q 4 = ® Convert Binary to Hex
iw | LA ® Convert Hex to Binary
| - iY @ ; ® Calculator ®@ NET-05-L1 Converting
: Decimal ,Binary, and Hex
4 |
*
. ~_———
i 4 —7


### Slides — strona 221

OO
IP & Routing Concepts
THE ROUTER


### Slides — strona 222

The Router
Overview
Router
A router is a device designed to receive, forward, and analyze
packets transmitted to and from other devices on a network, and
other networks.
Routers enable inter-network communication, and can provide
services such ACL and NAT, which are required in any networking
scheme.
6
A router is a Layer 3 device that communicates using IP addresses.


### Slides — strona 223

The Router
Default Gateway
Default Gateway
The default gateway is a network device that can route traffic to
and from other networks. A router typically fulfills this role.
The default gateway is similar to the door of a room. If a desired
object is in another room, the object can be reached only by
exiting through the door.
B


### Slides — strona 224

Default Gat Confi ti
NIC Configuration
Default gateway configuration =
options are typically located “ Internet Protocol Version 4 (TCP/IP v4) Properties x
together with other adapter i General
' Ovganize * Connect To Disable this ne! Connect using: a oe
configuration options. . ‘You can get IP setings assigned automaticaly if 1vork
e P A Bluetooth Network Cemnection G® keel) Dual Bard Wireteas-AC 8260 Pecos Odherwton, youeed Weck your network ede ator
Mat connected the aoprocriate IP settings.
In Windows, the settings are = Wii This connection uses the folowing tema (Co0btan an IP address automaticaly
located under Network & a student 2 Epi chert or Microsc Networks 7 se te toning Paces
F . Intel(R) Dual Band Wireless-AC 62. 4 Vidware Bridge Protocol BP address: 192.168. 0 . 10
Internet Settings in Change "SP Fie and Porter Shar for Microsoft Networks
Ad Oti SB tualBox NOISE Badged Netwatking river Sabet mask: 255.255.2558. 0
japter Options. a peellerearragial Default gateway: oe eT
% Boos Packer Scheduler .
4 9. itemet Protocal Version 4 (TCP/IP) . a ae
By default, the gateway should s z Gi0ki te haa cre aarti
be received from the DHCP. hia iret Propels Preferred DNS server: 3.8.8.8]
Desorption
Te Cat Plt Praca The dod Alternate ONS server: Ls -.8-.4.4/]
# area network, prot ‘prov | COMMUNES ION
However, if manual IPs were acront diverts interconnected networks Aivaldate settngs upon est z
configured, the gateway should
also be configured manually. ok Cancel =
jm
—
=


### Slides — strona 225

Logical Ports
Fast Ethernet Interface 2 ee ey
— @ Fast Ethernet was first made public in 1995. Ethernet % >. - . ,
= operates at a speed of 100 Mbps and uses the media ' oo -
standard 100BaseT. a . >
Gigabit Ethernet Interface PND
Gigabit Ethernet was introduced in 1999, and it
supports a faster speed of 1000 Mbps. It uses the media
standard 1000BaseT, but can also support 100 Mbps.
cA
Serial Interface
Serial interfaces are used for long distance transmissions.
If two serial ports need to communicate with each other,
they must be synchronized with the same clock frequency
and allocate the necessary bandwidth. a


### Slides — strona 226

The Router
Other Router Interfaces
Console
</> This is a physical management port, visually similar to Ethernet ports, that provides
out-of-band access to a Cisco device. Out-of-band refers to access via a dedicated
_. management channel used only for device maintenance.
AUX
i The auxiliary port mainly functions as a backup console port, although it can also be used
l as a dial-up port for remote management, and other purposes. The main difference
LU between Console and AUX is that AUX pushes output to the port after power-up, while a
Console does so during the power-up process itself.


### Slides — strona 227

Router interfacesneedito be R1(config)#interface gigabitEthernet @/@
set up with IP addresses, R1(config-if)#ip address 192.168.0.1 255.255.255.0
similar to computer network . .
interfaces: R1(config-if)#no shutdown
%LINK-5-CHANGED: Interface GigabitEthernet®/@, changed state to up
The R1(config-if)#exit
command selects the desired R1(config)#exit
iiterface. Ri#show ip interface brief
To use an interface, it must be Interface IP-Address OK? Method Status Protocol
set up with GigabitEthernete/e 192.168.0.1 YES manual up up
and enabled using the
command.
Use to
verify interface settings on the
router.


### Slides — strona 228

The Router
Loopback Interface
What it is used for ...
7~ Loopback is a logical interface that is not assigned to a physical port.
The interface can be used to test and manage Cisco IOS devices, because
SJ it ensures that at least one interface will always be available.
It can also be used in the OSPF identification process.
e


### Slides — strona 229

seit ratitianeds 5 ord Router(config)#interface loopback @
configured Suring tne.inttis %LINK-5-CHANGED: Interface Loopback®, changed state to up
router configuration, mainly 6 .
for testing/purposes. %#LINEPROTO-5-UPDOWN: Line protocol on Interface Loopback@, changed
state to up
The interface is configured . .
to automatically be ready Router(config-if)#ip address 10.10.10.10 255.0.0.0
for operation. Router(config-if)#no shutdown
Router(config-if)# exit
A router can have more than
one loopback interface enabled
simultaneously, but each
interface must have a unique IP.
A loopback interface is created
using the command
via the configuration terminal.


### Slides — strona 230

OO
IP & Routing Concepts
ROUTING PROCESS


### Slides — strona 231

Routing Process
Overview
The Routing Process

The routing process involves selecting a path for the delivery of
packets across different networks, from source to destination,
through Layer 3 devices.
It is important to note that routers can route packets to directly
connected networks, without requiring configuration. However, if
the networks are not connected, the route needs to be learned.
Routing decisions are made based on a routing table.


### Slides — strona 232

Routing Process
Examination
In the first step, the router decides whether to
process a packet or ignore it. Routers will ignore ie Decapsulation
packets with errors, or packets they don't know The router examines the Layer 2 address to
how to process. decide if the packet was intended for itself (the
default gateway), and verifies the integrity of the
Decision-Making frame using the FCS (Layer 2 trailer).
The router decides where to forward the packet
to, based on its destination IP address and the a e Encapsulation
ting table.
rouring rane The router re-encapsulates the packet with new
Layer 2 headers for the next hop, according to
. the decision made in step 3.
Forwarding 7
After a decision is made, the router forwards the
packet to the interface from which the packet
must exit.


### Slides — strona 233

Routing Process
Routing Choices
oe es
=eeee Pre
ess oe ee
pS
If the destination IP is on If the destination IP is ona If there is no static or If there is no ‘gateway of
the same LAN as the source different LAN, but the dynamic route in the last resort’ and the
device, there is no need for network device has a static network device’s routing destination packet is not
routing. The frame will get or dynamic route to the table, it will forward the listed, the router will
to the destination via the destination IP, it will forward packet to its default discard the packet.
switch. the packet to the next hop, ‘gateway of last resort’.
based on the route.


### Slides — strona 234

Router# show ip route
The Routing Table contains Codes: C - connected, S - static, I - IGRP, R - RIP, M - mobile, B - BGP
data stored in the router, with D - EIGRP, EX - EIGRP external, O - OSPF, IA - OSPF inter area
lists of routes to possible N1 - OSPF NSSA external type 1, N2 - OSPF NSSA external type 2
network destinations. E1 - OSPF external type 1, E2 - OSPF external type 2, E - EGP
i - IS-IS, L1 - IS-IS level-1, L2 - IS-IS level-2, ia - IS-IS inter area
* - candidate default, U - per-user static route, o - ODR
The table includes information P - periodic downloaded static route
about the network topology.
Gateway of last resort is not set
The codes on the left side of a 172.16.0.0/16 is variably subnetted, 5 subnets, 2 masks
route show how the network is ) 172.16.0.0/16 [90/5376] via 192.168.4.2, 00:02:24, GigabitEthernet4/o
learned by the router. G 172.16.0.0/24 is directly connected, GigabitEthernet@/o
Ss 172.16.1.0/24 [1/0] via 192.168.1.2
. R 172.16.2.0/24 [120/1] via 192.168.2.2, 00:00:15, GigabitEthernet2/0
The command show ip route 0 172.16.3.0/24 [110/2] via 192.168.3.2, 00:01:26, GigabitEthernet3/0
displays the routing table and C 192.168.1.0/24 is directly connected, GigabitEthernet1/0
is run in the Enable mode. C 192.168.2.0/24 is directly connected, GigabitEthernet2/0
C 192.168.3.0/24 is directly connected, GigabitEthernet3/0
C 192.168.4.0/24 is directly connected, GigabitEthernet4/o


### Slides — strona 235

Routing Process
Directly Connected / Local Route
When inspecting the routing table, records identified by the codes C or L indicate directly
connected networks. The codes mean that the devices are connected to the physical layer.
The C and L records are automatically created.
Static Route
x Static routes are configured and recorded manually, and are identified in the routing
table by the letter S.
Dynamic Route
Dynamic routes are identified with unique letters that indicate the dynamic
S, protocol, as follows:
D - EIGRP routing protocol
O - OSPF routing protocol
R - RIP routing protocol a


### Slides — strona 236

IP & Routing Concepts
IPV4


### Slides — strona 237

IPv4
Overview
IP
An Internet Protocol (IP) is a numerical label assigned to devices
@ connected to a network. It is used for host identification and
communication.
The IP address space is managed by IANA (Internet Assigned
Numbers Authority) and divided into five regional Internet registries
(RIRs), each responsible for their designated territories.
e
Each RIR is responsible for address assignment to users and service providers.


### Slides — strona 238

IPv4
IPv4 Addresses
IPv4 addresses consist of 32 bits and are divided into four octets, each containing 8 bits.
This addressing method provides 4,294,967,296 (232) IPv4 addresses in total.
An IP address represented in binary will appear as follows:
192.168.1.1 = 11000000.10101000.00000001.00000001
IPv4 Structure
4 7 An |Pv4 address consists of two parts: network and host, defined by the subnet mask.
. Lie Network - Represents the network part of the IP address.
SS Host - Represents the specific device on the network segment.


### Slides — strona 239

IPv4
Subnet Mask
Subnet Mask
A subnet mask is a 32-bit address, same as an IP address.
Like an IPv4 address, a subnet mask consists of 4 octets, separated
by dots (.).
Subnet masks will be further explained in the next module.
o)
Two similar IP addresses can belong to completely different networks, depending on the subnet mask.


### Slides — strona 240

IPv4 f
Classful Addressing
Inter-Domain Routing in 1993. It divides IPv4 address space into 5 classes, based on the 4 leading address bits.
Classful Table
NETMASK RANGES PREFIX CLASS
255.0.0.0 1.0.0.0 - 127.255.255.255 /8 A
255.255.0.0 128.0.0.0 - 191.255.255.255 /16 B
255.255.255.0 192.0.0.0 - 223.255.255.255 /24 C
* Reserved for multicasting 224.0.0.0 - 239.255.255.255 D
* Experimental 240.0.0.0 - 255.255.255.255 E
NOTE: 255.255.255.255 is reserved as the IPv4 Broadcast address. ey


### Slides — strona 241

IPv4.
Communication Types
Unicast
The most basic form of IP communication is one-on-one, where a packet is sent
directly from one device on the network to another device on the network.
A single source communicates with a single destination.
Multicast
— Multicast is when a single source communicates with multiple destinations. A packet
— is sent from one device on the network to a group comprised of one or more devices,
GE using Class D addresses.
Broadcast
Broadcast is when a packet is sent from one device on the network to all other
f 5 devices on the network, using a generic broadcast address (255.255.255.255 or
FF:FF:FF:FF:FF:FF).


### Slides — strona 242

IPv4 Link Local
Link-Local
Link-Local addresses, also known as APIPA addresses, are valid only
for communication within the network broadcast domain. The entire
169.254.0.0/16 address range is reserved for Link-Local.
If the DHCP is not available or an IP is not statically configured, the
(BR (\. OS will randomly generate a Link-Local address.
)
4h an Link-Local addresses are not guaranteed to be unique outside their
network segment, which is the reason why routers do not forward
their packets.
&


### Slides — strona 243

IPv4
Loopback Address
Loopback Address
Loopback addresses represent the same interface in a
computer. In IPv4, an entire network (127.0.0.0/8) is reserved
for loopback addresses.
J Almost all leading operating systems use the name "localhost"
to represent IPv4 loopback address 127.0.0.1.
&


### Slides — strona 244

IPv4
Public vs Private
IP addresses are typically divided into two groups: private and public.
Private
IN Private IPs are non-unique addresses that can belong to one of three IP address ranges.
a _ They are used to create networks that do not communicate over the Internet.
E The same private IPs can be found in multiple separate networks and are free to use.
Public
Public addresses are used for communication over the Internet. These IP addresses must
be unique, require a fee, and are purchased from service providers. A router will typically
have both a private and public IP. For example, the address 8.8.8.8 is a public address
used by Google.


### Slides — strona 245

IPv4
Private addresses are used in networks designed for homes and organizations. The ranges differ according
to the amount of separate networks and computers in each network, and there are no enforced rules.
Ranges

RANGE TARGET CLASS

10.0.0.0 — 10.255.255.255 A few large networks with many computers. A

172.16.0.0 — 172.31.255.255 A considerable amount of medium-size networks. B

192.168.0.0 - 192.168.255.255 Many small networks with only a few computers. Cc


### Slides — strona 246

IPv4
a , 5 ] ; . The objective of this exercise is to learn how to configure
IPv4 & initial Router Configuration initial settings on a Cisco Router.
30-60 Min. \\
= 7“ Ff yA ‘ . Initial Router Configuration
. ’ « ; ® Configure IPv4
.——.. =. wy ~.
| van a! ® os @ NET-05-L2 IPv4 and Initial
, * All platforms Router Configuration
. y) @ Tools ®@ NET-05-L2.pka
. ® ; | © Cisco Packet Tracer 7.2.2
i % ) =~


### Slides — strona 247

IP & Routing Concepts
IPV6


### Slides — strona 248

IPv6
Overview
The Need for IPv6é
Over the years, the IPv4 address space was depleted, since technical
progress meant that many more devices around the world were
connected to the Internet.
IPv6 was designed to solve the IPv4 address space limitation and
provide some additional enhancements. IPv6 has a larger 128-bit
address space, with the number of available addresses being 340* 102°,
é
Example of an IPv6 address: 2001:0000:3238:0001:0063:0000:0000:FEFB


### Slides — strona 249

IPv6
Compressing IPv6 Addresses
IPv6 addresses are long and difficult to read.
Some rules exist to omit specific numbers to Full Address
simplify the addresses. A full address contains all 8 blocks, with 4
hexadecimal digits.
Example of a full IPv6 address:
Leading Zeros a 2001:0000:3238:0001:0063:0000:0000:FEFB
The first rule allows us to discard leading zeros
in a block, making the address a bit shorter: i Consecutive Zeros
2001:0:3238-1:63:0000-0000:FEEB If two or more blocks contain consecutive zeros,
they can be omitted and replaced with double colon
signs (::) resulting in: 2001:0:3238:1:63::FEFB
Zero Block 7 Note that omitting is allowed only once in the
If there is a block that consists of 4 zeros, but
i . : 3 address.
without a consecutive zero-filled block, it can be
replaced with a single zero, and the final address
will be: 2001:0:3238:1:63::FEFB


### Slides — strona 250

IPv6 Address Breakdown
IPv6 Address t
| 2001:0ABC:00BB:'! 0000 }:0000:0000:0000:0001 | /64
1 ! 2 ! 3 1; a
</>
Configuration Example
Router(config-if)#ipv6 address
The prefix represents the prefix portion of the address. IPv6 does not use 2001: GABC : OBB : 8800 : 0000 : 0000:
notation subnet masks like IPv4. The prefix length indicates the network 0000: 0001/64
portion.
1. Because the prefix is /64, the first 64 bits in the address represent the
network portion.
2. The 16 bits from the 49th to the 64th are for defining subnets.
3. The remaining 64 bits represent the host portion in the IPv6 address.
4. The range can be from 0 to 128, with the most common being /64.


### Slides — strona 251

Router(config)#ipv6 unicast-routing
To enable IPv6 routing, Router(config)#interface gigabitEthernet/0/e
enter the configuration Router(config-if)#ipv6 address 2001: @ABC:@@BB: 0000: 0000: 0000: 0000: 0001/64
terminal mode, and run Router(config-if)#no shutdown
the command Router (config-if)#exit
Router#show ipv6é interface brief
GigabitEthernet0/0/0 [up/down]
Configure IPv6 on the FE8@: :201:97FF:FE13:A801
router interface using the 2001: ABC: BB: :1
command GigabitEthernet@/0/1 [administratively down/down]
unassigned
Vlan1 [administratively down/down]
Verify the configuration using unassigned
the command


### Slides — strona 252

IPv6
Device Communication Types
Unicast
({) Unicast addresses represent specific network interfaces that support IPv6.
O-- Unicast addresses have 3 sub-types (described in the following slide).
Multicast
Q Addresses used to send IPv6 packets from a single host to multiple destinations.
Anycast
ae IPv6 unicast addresses that can be assigned to multiple devices. Packets sent to an Anycast
5S address are routed to the nearest device that has that address (which is why Anycast is
I o =I also known as "one to the nearest“). This method operates similar to IPv4 broadcast.


### Slides — strona 253

IPv6 Unicast Types
Global Unicast
4 xy IPv6 global unicast addresses are similar to IPv4 public addresses. They are unique
and can be routed via the Internet. IANA currently assigns only 2000::/3 addresses.
Link-Local
r) [7 Addresses that enable communication between devices in the same local link (LAN).
5 Link Local addresses must be unique only within the link. They are not guaranteed to
tit be unique beyond their network segment, and begin with FE80::/10.
Unique-Local
Similar to IPv4 private addresses, with minor differences.
(mann) Unique addresses should not be routable in the global IPv6, and should
= not be translated to global IPv6 addresses. They begin with FCOO::/8.


### Slides — strona 254

IPv6
IPv6 Address Example
Common IPv6 Addresses
Type Address Example Notes
Global Unicast 2001:0ABC:1111:0000:1111:0000:0000:0200 The address range is from 2000 to 3FFF.
Global Unicast 2001:0ABC:0000:00BB:DCBA:0000:0000:0200 The address range is from 2000 to 3FFF. .
Link-Local FE80:0000:0000:0000:3211:5412:ECDC:FE11 Link-local address prefix is FE80::/10.
Link-Local FE80:0000:0000:0000:3211:5412:CAD1:FE12 Link-local address prefix is FE80::/10.
Multicast FFO2:0000:0000:0000:0000:000F:FFOO:120F Multicast addresses use the prefix ff00::/8.
Anycast XXXX.XXXXXXXX!XXXX!0000:0000:0000:0000 Similar to broadcast addresses in IPv4.
Ee


### Slides — strona 255

IPv6
Dual Stack
Dual Stack means that a device runs both IPv4 and IPv6
protocols simultaneously. Using two stacks allows both
IP versions to coexist.
: F Tunneling
IPv4 and IPv6 can coexist using
protocols and tools created by Tunneling is used when IPv6 addresses are to be sent
IEFT, which are known as: Dual S» over IPv4 networks, or vice versa. In this method, the
Stack, Tunneling, and Translation. IPv6 packet is encapsulated within an IPv4 packet.
Translation
Translation allows IPv6 to communicate with IPv4-
enabled devices using techniques similar to those
used by NAT.


### Slides — strona 256

IPv6
LAB NET-05-L3 freee
= The objective of this exercise is to practice configuring IPv6é
Poe! q jog . addresses on a router and clients.
Cont igure IPv6 Add ressing | The lab also covers practicing verification of IPv6 addressing
30-60 Min. J implementation.
a Pa “ ® Configure IPv6 Unicast Global address on R1
4 \ « interfaces
etn S, ” ‘Ex, ; ® Configure IPv6 on Users PC’s and verify connectivity
("Pe Ly ‘ ® Configure IPv6 Link -local address on R11 interfaces
p Ce yo i @) and PC’s (Optional)
Sat. eet ne
a a 6! >
1 ~ >
A) ® r Sos > NET-05-L3 Configure IPv6
* All platforms ; Addressing
" yy @ Tools > NET-05-L3.pka
SA y
‘ . : | © Cisco Packet Tracer 7.2.2
8 ~~
J |


### Slides — strona 257

; ¢ 4 im Z f
se “ =) > Be 4

vl om ES \ . 7! >
So ~ Ww =
CDOS \ —

CTE > <=

SRS 2 SS

oe CSS i. > fo

SS \ ke sug ie

Bo PLO i Sy

* ‘ 4 Crs = f


### Slides — strona 258

aul egal 5 i 2B
—— — Sy " : ™ ty .
ie. = 4 a wet, NETWORK ga Cm D


# Chapter 6: Subnetting Concepts


### Slides — strona 259

atl
’ ? Cybersecurity Professional Program
a * a nD ‘Bee eee
-__- Subnetting Concepts
Computer Networking
Copyright © 1996-2023 HackerU Ltd. All Rights Reserved.


### Slides — strona 260

Computer Networking
Introduction Network Switch & IOS Switch Securit IP and Routing
to Networks Fundamentals Fundamentals y Concepts
Diagnostics and VLANs Dynamic IPv4 & IPv6é Subnetting
Troubleshooting and Trunk Routing Static Routing Concepts
Access Infrastructure Fiival Proiect
Control List Services d


### Slides — strona 261

Subnetting Concepts
Overview
Lesson Objective
Subnetting
The object of this lesson is to understand
how IP addresses and subnet masks operate, CIDR
and how they work together.
The lesson also covers how to configure VLSM
networks with the correct usage of resources
and why it’s important to employ CIDR.
Network Address Scheme Design
G


### Slides — strona 262

CO
Subnetting Concepts
SUBNETTING


### Slides — strona 263

Subnetting
Overview
Definition
Subnetting means subdividing a network to manage, design, and
implement an effective IP addressing plan. When organizations add
[SUB hundreds and even thousands of hosts to their network, subdividing the
network facilitates faster packet delivery and adds filtration by minimizing
local traffic.
Subnetting reduces overall network traffic and improves performance.


### Slides — strona 264

Subnetting
Broadcast Domain Issue
Large Broadcast Domains
Large networks containing many hosts poses a problem for
broadcast domains, because hosts can generate broadcast
messages and affect network performance.
A large amount of traffic generated by broadcast messages
causes network operation to slow down.
Each device must accept and process broadcast requests, even
if the request is not intended for a particular device.
2
The solution is to reduce the network size, and create smaller broadcast domains by subnetting the network.


### Slides — strona 265

Subnetting
Subnetting
Why Subnetting?
Subnetting improves network performance by reducing the
overall volume of network traffic.
In addition, it enables an administrator to implement security
policies and control network growth.
Subnetting creates more manageable network congestion, and
simplifies network administration.
&


### Slides — strona 266

Subnetting
Octet Boundary
What is an Octet Boundary?
An Octet Boundary is a subnet created by borrowing one or more
of the host bits to be used as network bits.
By extending the subnet mask with bits from the host portion,
] additional subnets can be created.
: The easiest method of network subnetting is to use the octets /8,
/16, and /24.
Additional 1 bits mean more Networks.
Additional 0 bits mean more Hosts. e
=f


### Slides — strona 267

Subnetting
The following table lists attributes of the most common boundaries: /8, /16, and /24.
Subnets
Prefix Subnet Mask Binary Number of Hosts
11111111.00000000.00000000.00000000
/8 255.0.0.0 nnnnnnnn.hhhhhhhh.hhhhhhhh.hhhhhhhh 16,777,214
255 0 0 0
11111111.11111111.00000000.00000000
nnnnnnnn.nnnnnnnn.hhhhhhhh.hhhhhhhh 65,534
/16 255.255.0.0 255 255 0 0
11111111.11111111.11111111.00000000
nnnnnnnn.nnnnannnn.nnnnnnnn.hhhhhhhh 254
/24 255.255.255.0 255 255 255 0
n=Network portion h = Host portion


### Slides — strona 268

Subnetting Concepts
CIDR


### Slides — strona 269

CIDR
CIDR Overview
. Since not all networks in an organization are compatible with IPv4
© ' address classes (due to the number of hosts), using these classes, in
ooss \ some cases, may result in a waste of addresses (which are important
' ' commodities in any organization).
A
== % For example, an organization with a network of 400 hosts must use
1
- class B, which means they will waste more than 60,000 addresses.
&


### Slides — strona 270

CIDR
Classless Inter-Domain Routing
Explanation
@-¢. To resolve this issue, Classless Inter-Domain Routing (CIDR) was
G defined in RFC 4632. CIDR allows an IP address to use any subnet
mask, regardless of predefined classes.
For example, IP address 10.1.1.1, which according to the class-based
system should be in class A, can belong to class B or C, in accordance
with the user’s preference.
&


### Slides — strona 271

CIDR
CIDR Addresses
Address Table

Subnet Address Useable Address Range Broadcast Address
10.0.0.0/16 10.0.0.1 — 10.0.255.254 10.0.255.255
10.1.0.0/16 10.1.0.1 — 10.1.255.254 10.1.255.255
10.2.0.0/16 10.2.0.1 — 10.2.255.254 10.2.255.255
10.100.0.0/24 10.100.0.1 — 10.100.0.254 10.100.0.255
10.101.0.0/24 10.101.0.1 — 10.101.0.254 10.101.0.255
10.255.255.0/24 10.255.255.1— 10.255.255.254 10.255.255.255 a


### Slides — strona 272

CIDR
CIDR Subnetting Example
Example
Network Portion Host Portion
IAT, —_ As an example, we will use the
11111111.11111111.111111111. 00000000 subnet 10.1.1.0/24. The subnet
must appear in binary on the
left side.
Network Portion Host Portion
SS SSS Creating two smaller sub-networks
11111111,11111111.11111111,1 0000000 can be done by “borrowing” a bit
from the host portion to the
* For one borrowed bit: 2sub-network bits = 21 = 2 ———
sub-networks
, After subnetting, the new address will
* For two borrowed bits: 2sub-network bits = 22 = 4 be 10.1.1.0/25. Each network address
sub-networks will be assigned 126 host addresses.
¢ Andso on...


### Slides — strona 273

CIDR

Subnets can borrow bits from any host bit to create additional masks. For each borrowed bit in the fourth octet, the number

of sub-networks is doubled, while the number of hosts per subnet is reduced. n = Network Portion, h = Host Portion

Subnets

Prefix Subnet Mask Mask in Binary Networks Hosts

nannnnnnn.nnnnnnnn.nnnnnnnn.nhhhhhhh 2 126

2s 288-255.255-128 11111111.11111111.11111111.10000000
nannnnnnn.nnnnnnnn.nnnnnnnn.nnhhhhhh 4 62

i ABaoaPoate2 11111111.11111111.11111111.11000000
nannnnnnn.nnnnnnnn.nannnnnnn.nnnhhhhh 8 30

[27 295.255.255.224 11111111.11111111.11111111.11100000
nnnnnnnn.nannnnnnn.nannnnnnn.nnnnhhhh 16 14

j28 295.255.255.240 11111111,71111111,11111111.11110000


### Slides — strona 274

CIDR
Case Study 1
Configuration Per Sub-Network
A network manager requests to extend the current network to an additional four sub-networks.
The given IP address and subnet mask is 172.16.0.0/24.
¢ How would we add four more networks?
¢ What are the new network addresses?
Network Address Usable IP Addresses Broadcast Address


### Slides — strona 275

CIDR
Case Study 1
Configuration Per Sub-Network
A network manager requests to extend the current network to an additional four sub-networks.
The given IP address and subnet mask is 172.16.0.0/24.
¢ Adding four networks: 24x = 4 ?, the answer is 2. That means we need to borrow two bits from
the subnet to create an additional four sub-networks.
¢« RED = new network portion, BLUE = new host portion: 11111111.11111111.11111111.11000000
¢ The new network addresses are: 172.16.0.0, 172.16.0.64, 172.16.0.128, 172.16.0.192
(| 2ase0 | 172.16.0.1-172.16.0.62 | - 172.16.0.62 | 172.16.0.63
The total number of
jump in the last octet:
246 = 64 addresses (


### Slides — strona 276

CIDR
Case Study 2
Configuration Per Sub-Network
A network manager requests to extend the current network by an additional five sub-
networks. The given IP address and subnet mask is 192.168.0.0/24.
* How would we add five more networks?
¢« What are the new network addresses?
Network Address Usable IP Addresses Broadcast Address


### Slides — strona 277

CIDR
Configuration Per Sub-Network
A network manager requests to extend the current network by an additional five sub-networks.
The given IP address and subnet mask is 192.168.0.0/24.
¢ Adding five networks is not possible, with the closest possible network division being 8.
¢ 24x = 8 ?, the answer is 3. That means we need to borrow three bits from the subnet to create an
additional eight sub-networks.
¢ RED = new network portion, BLUE = new host portion: 11111111.11111111.11111111.11100000
¢ The new network addresses are: 192.168.0.0, 192.168.0.32, 192.168.0.64, 192.168.0.96, and so on.
Note: The table below displays only the first four of eight subnets.
[/__ezston | aeesssosmssassenae | sszsconar
The total number of
jump in the last octet:


### Slides — strona 278

CIDR

Case Study 3

Network Configuration Per User
A network manager requests a 300-workstation expansion of the network. The workstations are to be
installed in a single broadcast domain. The correct given address is 10.0.0.0. The aim of the expansion is
to use as few resources as possible.
¢ How would we use the least amount of resources possible?
¢ What is the new network address, network range, and broadcast address?


### Slides — strona 279

CIDR
Case Study 3
Network Configuration Per User
A network manager requests a 300-workstation expansion of the network. The workstations are to be
installed in a single broadcast domain. The correct given address is 10.0.0.0. The aim of the expansion is to
use as few resources as possible.
* To use the least amount of resources possible, the matching subnet will be /23, because it allows the use
of 510 host addresses: 249 = 512, 512 — 2 (Minus Network address, Broadcast Address) = 510 hosts.
¢ RED =new network portion, BLUE = new host portion: 11111111.11111111.11111110.00000000
* The new network address will be 10.0.0.0/23
¢ The network range is 10.0.0.1/23 — 10.0.1.254/23
¢ The broadcast address is 10.0.1.255/23


### Slides — strona 280

Subnetting Concepts
VLSM


### Slides — strona 281

VLSM
VLSM Overview
VLSM
VLSM (Variable Length Subnet Mask) is a method by which a network is
subnetted, and the subnets are then subnetted further (when using only
ly lI CIDR, they are not subnetted further).
aaa: The process can be repeated several times to divide the subnets into
various sizes, to ensure that IP addresses are not wasted.
Formulas are applied to calculate the number of hosts and subnets.
&


### Slides — strona 282

VLSM
VLSM Subnetting Example
Example
10 O O O /8 As an example, we will start with
cu eee the network address 10.0.0.0/8.
This address is subnetted into 2
additional networks.
The subnetting process (CIDR)
10.0.0.0 /9 10. 128.0.0 /9 created the networks 10.0.0.0/9
/~ and 10.128.0.0/9.
aN After creating the networks, each
10.0.0.0/10 10.64.0.0/10 10.128.0.0/10 10.192.0.0/10 was subnetted (VLSM) to create
additional networks, similar to
a using CIDR.
10.0.0.0 /9 used to create 2 networks
) VLSM is useful when using CIDR
11111111.11000000.00000000.00000000 provides too many unused
» addresses for one network.
10.0.0.0 /10 and 10.64.0.0 /10 subnets are created is


### Slides — strona 283

VLSM
Lab NET-06-L1: Subnetting Practice
A Lab Mission Q— Steps
The aim of this lab is to provide review questions Subnetting questions
for all the material covered in the module, 7 F
Practice subnetting
including the topics of how to subnet networks
and assign IP addresses.
(ag Env. & Tools (5 Related Files
OS: All platforms Lab document
Tools: Calculator (optional)


### Slides — strona 284

VLSM
2 eee The aim of this lab is to provide review questions for all the
Su bn etti ng Pra ctice material covered in the module, including the topics of how
. | to subnet networks and assign IP addresses.
30-60 Min. |
oo . @ Subnetting questions
— 4 : ®@ Practice subnetting
a: =
" b NN ® e yr
| ‘ ‘Ss i) _ i 3 ® OS: All platforms @ Lab document
= 88 W ® Tools: Calculator
; ‘i } (optional)
| { ; 4 . s
if ’ . |


### Slides — strona 285

CO
Subnetting Concepts
NETWORK ADDRESS SCHEME DESIGN


### Slides — strona 286

Network Address Scheme Design
Network Planning
How to Plan a Network
A network needs to be well-designed. Addresses must not be assigned
= randomly!
Planning a network requires examination of how the organization is
structured, and how the subnets will be structured.
7 i i Planning addresses involves deciding how many hosts per subnet there will
be, how large each subnet will be, and how host addresses will be assigned.
E,
Knowing your address requirements will help determine the range of host addresses.


### Slides — strona 287

Network Address Scheme Design
Planning Considerations
Prevent Duplication
%. In. an inter-network structure, each host must have a unique address.
n Planning and documentation prevent the creation of duplicate addresses.
Access Control
_ If addresses are randomly assigned, servers that provide resources to internal and
external hosts will not be able to control access efficiently and effectively.
Monitor
7 o- —] Network traffic is examined for source IP addresses generated or received from
packets. With proper planning, finding problematic devices should be a simple
= process.


### Slides — strona 288

Network Address Scheme Design
ey Fi or?
ras ofo
Most networks use DHCP to In most networks, servers Routers and switches are A gateway is a packet-
dynamically assign must be made available to assigned IP addresses. forwarding device, and is
addresses, eliminating the remote users. The servers . tvpicallya fi lI t
need for network staff to do are assigned private Switches can be managed VPI Y it URES OF TOURED
so, and preventing entry internal addresses, and the remotely via the cloud. Each interface that serves as
errors. forwarding device will Routers are assigned IP a gateway for hosts in the
When the address scheme perform additional addresses because they network must be assigned
changes, the DHCP server ite ations:to public operate in Layer 3. an IP address.
must be reconfigured. addresses (NAT). call
Servers are typically Routers are typically
configured with static configured with static
addresses. addresses.


### Slides — strona 289

A :
,/, e ‘ sss 4
.. / = » 4, f
= wv 4 , , N \ ~~,
SSO : ’ a .
QUESTIONS? A ‘faa
7
% ’ *.
ag Pg rey y ik os - a a

: @a, Pe, y 4 nal


### Slides — strona 290

a i ™" : = a aw NETWORK ee Bal Ci = L D


# Chapter 7: IPv4 & IPv6 Static Routing


### Slides — strona 291

<a = —— :
: Cybersecurity Professional Program
IPv4 & IPv6
Static Routing
Computer Networking
Copyright © 1996-2020 HackerU Ltd. All Rights Reserved.


### Slides — strona 292

cae IData
Introduction Network Switch & IOS Switch Securit IP and Routing
to Networks Fundamentals Fundamentals y Concepts
Diagnostics and VLANs Dynamic IPv4 & IPv6 Subnetting
Troubleshooting and Trunk Routing Static Routing Concepts
Access Infrastructure Fiival Proiect
Control List Services d


### Slides — strona 293

IPv4 & IPv6 Static Routing
Overview
Lesson Objective
Router Operation
The objective of this lesson is to learn
about the static routing method and IPv4 Static Routing
how to configure it in IPv4 and IPv6.
IPv6 Static Routing
G


### Slides — strona 294

OO
IPv4 & IPv6 Static Routing
ROUTER OPERATION


### Slides — strona 295

Router Operation
Routing Review
How a Router Operates
=> One of the router’s main jobs is to select the best path for a packet.
<i _> The decision is based on its destination address.
After determining the best path on which to forward the packet, the
, router encapsulates the packet in a new frame in accordance with the
relevant outgoing interface.
6


### Slides — strona 296

Router Operation
Examination
In the first step, the router decides whether to
process a packet or ignore it. Routers will ignore ie Decapsulation
packets with errors, or packets they don't know The router examines the Layer 2 address to
how to process. decide if the packet was intended for itself (the
default gateway), and verifies the integrity of the
Decision-Making frame using the FCS (Layer 2 trailer).
The router decides where to forward the packet
to, based on its destination IP address and the San Encapsulation
routing table. The router re-encapsulates the packet with new
Layer 2 headers for the next hop (MAC address
of the next hop), according to the decision made
Forwarding 7 in step 3. a]
After a decision is made, the router forwards the
packet to the interface from which the packet
must exit.


### Slides — strona 297

Router Operation
Remote Networks
What is a Remote Network?
A router's best routing decision is based on its routing table. But where
does the routing table get its information from?
Networks connected directly are added to the table immediately, but a
remote network must be configured by the user.
A remote network is any network not connected locally to the router.
6
The ICMP message "Destination unreachable" is displayed whenever the router cannot find
a match for the path in its routing table.


### Slides — strona 298

Router Operation
Remote Network Learning
A remote network can be learned by a router in one of two ways: statically or dynamically.
Static Method
Using the static routing method, the user enters every network manually
ae in the routing table.
Dynamic Method
AUTO In the dynamic routing method, the router automatically learns the remote network
from the routing tables of adjacent routers, by using various protocols.


### Slides — strona 299

Router Operation
Advantages Disadvantages
A simple solution for small networks. Error-prone in large network environments.
Not advertised over the network, meaning better security. Does not support verification methods.
No CPU and memory usage for routing purposes. Configuration and maintenance are time-consuming.
Every path a packet takes is known, which improves network Regiiires complete knowledge of the'entire network.
traffic management.


### Slides — strona 300

Router Operation
When to Use Static Routing
Network administrators decide if and when to use Static Routing, based on network requirements.
Stub Networks
Static routing is a better choice when routing to and from stub networks.
ONE WAY Stub networks consist of a single router that sends and receives non-local traffic
via a single path.
Small Networks
a® Although Static Routing is simple and secure, and saves resources, it does not
ae) provide a sufficient level of scalability in larger networks.


### Slides — strona 301

OO
IPv4 & IPv6 Static Routing
IPV4 STATIC ROUTING


### Slides — strona 302

IPv4 Static Routing
Static Route Types
The following are the most common types of Static Route implementation.
Standard Static Route
g Manually configured route that forwards traffic to a specific network.
Default Static Route

Typically used as a Gateway of Last Resort, which is used for any packet that does not
have a destination route in the routing table. The destination in such cases is often set to
the Internet.


### Slides — strona 303

IPv4 Static Routing
Network Topology Illustration
A host on network A wants to
communicate with a host on
network B.
If no static or dynamic routing
is used, R1 does not know the
er
destination network and its |
direction. ea)
as
172.17.0.2 4]
— aay
For R1 to know network B, add R3 Net C 10.2.0.0/24
: ‘ Gig2/0_ 7 7
the network and direction to the —, Gigt/0 a,
routing table. Now, R1 will hi) eng Gigolo 172.16.0.2 ei |
forward network A host packets ——5 7
to the correct destination. L_—— ——
Net A 10.0.0.0/24 i & Net B 10.1.0.0/24
The same is required for R2 and
R3 to recognize network A.


### Slides — strona 304

Syntax Usage
_- Command , ji F 1 1
Router (config)# ip route <network-address> <subnet-mask> <direction>
| i 1 2 3
</>
Code Example
R1(config)#ip route 10.1.0.0
1. Specifies the remote network address. 255.255.255.0 172.16.0.2
2. Specifies the remote network subnet mask.
3. Sets the direction of the network, which can be:
Directly-connected - the local outgoing interface.
Next-hop - the IP address of the interconnected router.


### Slides — strona 305

The'example‘on the rightis'a R1(config)#ip route 10.1.0.@ 255.255.255.@ 172.16.0.2
static route configuration
example, based on the R1(config)#ip route 10.2.0.@ 255.255.255.@ gigabitEthernet 1/0
topology in the previous slide. *#Default route without gateway, if not a point-to-point interface,
may impact performance
The command is used to
add a new network route to the R1(config)#do show ip route
routing table. 10.0.0.0/24 is subnetted, 2 subnets
Verify the addition of static routes
by displaying the routing table C 172.16.0.0/16 is directly connected, GigabitEthernet@/a
using the command. Cc 172.17.0.0/16 is directly connected, GigabitEthernet1/@
C 172.18.0.0/16 is directly connected, GigabitEthernet2/0
Note: The next-hop and directly-
connected options are also known
as recursive and directly-attached
routes.


### Slides — strona 306

R1(config)#ip route 0.0.0.0 0.0.0.0 gigabitEthernet 2/0

The default and standard

pects diss taeenenn R1(config)#do show ip route

routes use the same syntax,

except for one difference: 10.0.0.0/24 is subnetted, 2 subnets

The défault:routeuses S 10.1.0.0 [1/0] via 172.16.0.2

to represent any network S 10.2.0.0 is directly connected, GigabitEthernet1/0

address with any subnet mask. C 172.16.0.0/16 is directly connected, GigabitEthernet@/oe
C 172.17.0.0/16 is directly connected, GigabitEthernet1/0

- C 172.18.0.0/16 is directly connected, GigabitEthernet2/0

A default route can be set with a

next-hop or outgoing interface.

The standard route is denoted by S,

while the default is denoted by S*.


### Slides — strona 307

Administrative Distance
Administrative Distance

an Oy) Administrative Distance (AD) is a predefined value for each routing method.

The router selects the path of the lowest AD value in the routing table.

a) For example, if there are two routes to the same destination network, one
==, via OSPF (a dynamic routing protocol) and the other a static route, the
<3) router will select the static route (1 vs. 110).

e


### Slides — strona 308

IPv4 Static Routing
Default AD Values

Method/Protocol AD Value
Directly-connected (6)
Static Route 1
Internal EIGRP 90
OSPF 110
RIP 120


### Slides — strona 309

IPv4 Static Routing
Floating Static Route Summary Static Route
Gr
Provides backup paths to To reduce the number of Similar to standard route,
primary static routes for routing table entries, but instead of configuring a
situations in which a link multiple static routes can be network, it is used to
failure occurs. This route summarized to a single forward traffic to a specific
type is only used when the address. host.
Primary route Is not It uses a default mask of
available. 255.255.255.255
The AD for floating static
routes is higher than the
AD for primary routes.


### Slides — strona 310

ip route <network-address> <subnet-mask> <direction> <AD>
The code on the right is an
example of a primary and Ri(config)#ip route 192.168.1.0 255.255.255.0 172.16.0.2
backup route configuration. R1(config)#ip route 192.168.1.@ 255.255.255.@ 10.0.0.2
The primary route is set with a R1(config)#do show ip route
default AD (1). Cc 10.0.0.0/3@ is directly connected, GigabitEthernet@/1
- Cc 172.16.0.0/30 is directly connected, GigabitEthernete/oe
ihe backtip dear ae S 192.168.1.0/24 [1/0] via 172.16.0.2
the same networ utTtroma .
Hifferentdirectionvand isset 5 192.168.1.0/24 [°/@] via 10.0.0.2
with a higher AD (5).
Note: The backup route will
be shown only if the primary
route fails.


### Slides — strona 311

ip route <ip-address> 255.255.255.255 <direction>
Although this type of static R1(config)#ip route 192.168.1.5 255.255.255.255 172.16.0.2
route is not very common, it
B és s Cc 10.0.0.0/30 is directly connected, GigabitEthernete/1
such as a server. :

Ss 192.168.1.5/32 [1/0] via 172.16.0.2

This method may be useful for
special routing requirements.


### Slides — strona 312

IPv4 Static Routing
Network Topology Illustration

Contiguous:
To summarize the network to a
single address, the destination ==»
networks need to be
contiguous. eg 10.0.0.0/30 as) 172.10.0.0/16 ee 472.11.0.0/16

Same Routing Path: =

All networks use the same i Re RS

outgoing interface or next-hop

address.

172.13.0.0/16
172.12.0.0/16
In this example, instead of four Bese
standard static routes, a single
summarized static route is R4
used, as shown in the next
slide.
EA


### Slides — strona 313

IPv4 Static Routing
Summarizing Steps
Convert IP to Binary
172.10.0.0 — 10101100.00001010.00000000.00000000
172.11.0.0 — 10101100.00001011.00000000.00000000
172.12.0.0 — 10101100.00001100.00000000.00000000
172.13.0.0 — 10101100.00001101.00000000.00000000 Compare the Identical Bits
~ H 172.10.0.0 — 10101100.00001010.00000000.00000000
172.11.0.0 — 10101100.00001011.00000000.00000000
172.12.0.0 — 10101100.00001100.00000000.00000000
Create a Summarized Address 172.13.0.0 — 10101100.00001101.00000000.00000000
Network Address :
172.8.0.0 - 10101100.00001000.00000000.00000000
Subnet Mask:
255.248.0.0 - 11111111.11111000.00000000.00000000


### Slides — strona 314

ip route <summarize-address> <summarize-mask> <direction>

R1(config)#ip route 172.8.0.@ 255.248.0.0 10.0.0.1
R1(config)#do show ip route

The exaniple:sn the C 10.0.0.0/24 is directly connected, GigabitEthernet0/e

right shows the code for

summarizing and

verifying the new route.

Note the prefix 13.


### Slides — strona 315

IPv4: Static Routing
EFS Se The objective of this exercise is to implement IPv4 standard
Configuring IPv4 Static and Default Routes and default static routes in a full network topology.
30-60 Min.
~ wr r yA , . Configure IPv4 Standard Route
. ’ ‘ « ; ® Configure IPv4 Default Routes
>. q 4 = ® Configure IPv4 Summary Route
| —an ® 8 OS: All platforms © Lab document
: ® Tools: Cisco Packet Tracer ® NET-07-L1.pka
. y) 7.2.2 or higher
*
. _——
i ‘ a


### Slides — strona 316

OO
IPv4 & IPv6 Static Routing
IPV6 STATIC ROUTING


### Slides — strona 317

IPv6 Static Routes
IPv6 Static Route Types
(IP) Static routing is similar for IPv4 and IPv6, with the exception of how the
destination network addresses are formatted.
se \: IPv6 supports the same static routing types, and most of the parameters
4h an are identical to those in IPv4 commands.
B


### Slides — strona 318

IPv6 Prerequisites
What’s Required for IPv6 Static Routing?
N = IPv6 packet forwarding must be enabled on the Cisco router.
= Command: IPv6 unicast-routing
fi) = The interface must be enabled and configured with an IPv6
address.
é


### Slides — strona 319

Syntax Usage
— Command , , ' ' H
i Router(config)# | ipv6é route i <network-address> i / <prefix> | <direction> !
| ! 2 3
</>
Code Example
1. Specifies the IPv6 remote network address. Ba (cant te) #Tpvo scouts .
2001: abcd: cafe::/64 serial
2. Specifies the remote network prefix. e/e/e
3. Sets the direction of the network, which can be:
Directly-connected - the local outgoing interface.
Next-hop - the |Pv6 link-local or global-unicast address of the
interconnected router.


### Slides — strona 320

R1(config)#ipv6 route 2001:abcd:cafe::/64 2002:abcd:aaaa::1
R1(config)#ipv6é route serial 0/0/0
The code on the right includes R1(config)#ipv6 route 2001:abcd:cafe:: gigabitethernet0/e
examples of all types of IPv6
static routes: Ri(config)#ipv6 route 2001:abcd:cafe::/64 gigabitetherneto/o
* Standard (next-hop)
* Default (directly-connected)
* Summary
¢ Floating


### Slides — strona 321

R1(config)#do show ipv6 route
Ss 2001:ABCD:CAFE::/64 [1/0]
via 2002:ABCD:AAAA: :1
; S ::/@ [1/0]
displays and via serial 0/e/@

verifies the IPv6 routing table.

Remember not to use

(displays IPv4 routing table),

but rather


### Slides — strona 322

; ¢ 4 im Z f
se “ =) > Be 4

vl om ES \ . 7! >
So ~ Ww =
CDOS \ —

CTE > <=

SRS 2 SS

oe CSS i. > fo

SS \ ke sug ie

Bo PLO i Sy

* ‘ 4 Crs = f


### Slides — strona 323

aul egal 5 i 2B
—— — Sy " : ™ ty .
ie. = 4 a wet, NETWORK ga Cm D


# Chapter 8: Dynamic Routing


### Slides — strona 324

—" ‘Cybersecurity Professional Program
— — rg Stoeeanemo™ mae p oe :
E Dynamic Routing
Computer Networking


### Slides — strona 325

Computer Networking

Introduction Network Switch & IOS Switch Securit IP and Routing

to Networks Fundamentals Fundamentals y Concepts
Diagnostics and VLANs Dynamic IPv4 & IPv6é Subnetting
Troubleshooting and Trunk Routing Static Routing Concepts

Access Infrastructure Fiival Proiect
Control List Services d
2


### Slides — strona 326

Dynamic Routing
Overview
Lesson Objective
; ; ; Dynamic Routing Concepts

This lesson covers dynamic routing concepts

and protocols, including RIPv2 and OSPFv2.

It also explains processes, algorithms, and RIPv2

messages used to exchange routing

information.

OSPFv2
G
3


### Slides — strona 327

OO
Dynamic Routing
DYNAMIC ROUTING CONCEPTS


### Slides — strona 328

Overview

What is Dynamic Routing?

Dynamic routing protocols have been in use since the late 1980s.

4 he purpose of these protocols is to map networks and update routing
tables with the shortest routes, in a fully automatic and independent

Wy manner.

i The method is made possible by special algorithms and protocol
packets.

e


### Slides — strona 329




### Slides — strona 330

Dynamic Routing Concepts
Routing Source Codes
S — Indicates that the D — Indicates that the O - Indicates that the R — Indicates that the
route was manually route was learned route was learned route was learned
created by an dynamically from dynamically from dynamically from
administrator to reach a another router using the another router using the another router using the
specific network. EIGRP routing protocol OSPF routing protocol. RIP routing protocol.
(which will not be
covered during this
course).


### Slides — strona 331

Key Elements
Fits Any Topology
Once the protocols are activated, the routers begin “talking” to each other,
and map the network topologies themselves.
Fast and Independent
Dynamic Routing is based on software that can gather a lot of information in a short
on time and input it to an algorithm that computes the information to find the fastest
route to each network.
Awareness
Each Dynamic Routing protocol uses Timers that detect any change in the topology,
( such as a connection failure. When a change is detected and involves a network
() failure, the protocols will search for an alternate path.


### Slides — strona 332

Dynamic Routing Concepts
Administrative Distance (AD) Values
Default AD Values

Method/Protocol AD

Directly Connected (6)

Static Route 1

Internal EIGRP 90

OSPF 110

RIP 120

EEE


### Slides — strona 333

Metrics
What is a Metric?

A metric is a measurable value assigned by the routing protocol to
different routes based on the usefulness of the route.

® | | l When there are multiple paths to a remote network in the same

= = protocol, routing metrics are used to determine the overall

[== “length” of a path from source to destination.
Routing protocols determine the best path based on the route
with the lowest metric value.

e


### Slides — strona 334

Dynamic Routing Concepts
Routing Protocol Metrics
Routing Information Protocol Hep Count Matas Exanpls
The RIP hop count metric will choose the path
with the least amount of hops, where hops refer Route A is shorter
ye to routers. than Route B
@ Src Network Route A Dst Network
Open Shortest Path First = > =)
" The OSPF metric is based on cumulative R1 = ==
aS bandwidth from source to destination. OSPF will \es_ es
Ag” choose the path with the highest bandwidth. Route B
G


### Slides — strona 335

Dynamic Routing Concepts
IGP Vs EGP Protocol Classification Map
Interior Gateway Protocols are routing protocols used within an
Autonomous System (AS), such as company routers. ice | EP
Exterior Gateway Protocols are used to map routes between AS’s,
and are mainly used by ISPs. a
Distance Vector Vs Link-State [Distance Vector | | _ Link State
The fundamental difference between distance vector and link-state
routing protocols, is how the protocols discover the topology and RIP } { EIGRP [iss | | OSPF | BGP
the way they share routing information with the routers.
G
BGP is classified as a Path Vector protocol and is used to map the Internet.


### Slides — strona 336

Dynamic Routing Concepts
Distance Vector
Distance Vector
RS Distance Vector is a routing algorithm that calculates the best path for a packet
7
SX based on the factors of Distance and Vector.
WMA
Distance
0) Distance — The distance between the router and the destination network, based
©) 77 onthe metric of number of hops (routers).
Vector
Vector — The outgoing interface and the direction to the path that leads to the
destination network.


### Slides — strona 337

Dynamic Routing Concepts
Link State
Link State
Gu Link State routing protocols include complete network topology maps.
Network Map
8 The map is created based on information gathered from all routers on the network.
e=y,
Network Changes
vN Link State routing protocols do not broadcast information regularly.
WA Updates are only sent when a change occurs on the network.


### Slides — strona 338

Dynamic Routing Concepts
Passive Interface
Passive Interface Feature
Passive interface is a feature used in all routing protocols. Its purpose
is to disable routing updates on specific interfaces, which decreases
resource usage and increases security.
The command syntax is the same in all routing protocols.
It is typically placed on interfaces facing the LAN.
Passive interfaces should not be configured between routers.


### Slides — strona 339

Dynamic Routing Concepts

(Q

IO Ek®
Dynamic routing updates Devices in the same LAN Packet sniffing software can
consume bandwidth must process updates up to be used to intercept packets
because messages are sent Layer 4 (transport layer), that include routing
in broadcast or multicast, and only then discard the updates, and redirect traffic
causing switches to update. by corrupting the routing
broadcast to all ports. table with false metrics.


### Slides — strona 340

Dynamic Routing Concepts
Classful :
Classful routing protocols provide routing updates os .
according to classful network addresses (A, B, C). For
example, the route for 10.15.30.2/11 and 10.80.0.15/11
will be advertised as 10.0.0.0 even if it is subnetted. .
Classless 3 :
Classless routing protocols provide routing updates —_
according to VLSM addresses and does not follow only
classful addresses. For example, the route for
10.80.30.2/11 will be advertised as 10.64.0.0/11 classtillirantingpravaaals
RIPv1, IGRP
Classless routing protocols:
RIPv2, EIGRP, OSPF, IS-IS
by


### Slides — strona 341

Dynamic Routing
RIPV2


### Slides — strona 342

RIPv2
RIP Overview
Routing Information Protocol
RIPv1 was released in 1988 and is one of the oldest routing protocols.
It is a distance-vector protocol, and its metric method is hop count.
The protocol has limitations, such as the maximum allowed hops for a
route, which is 15. Due to its limitations, it is often implemented only in
small networks that do not require a high level of scalability.
Unlike other protocols, RIP operates in Layer 7 (OSI) and uses port 520
(UDP).
B
There are three versions of the protocol. RIPv2 is the most widely used, but is not the most
popular, due to its inherent limitations.


### Slides — strona 343

RIPv2
RIPv1 RIPv2 RIPng
Released in 1988 Released in 1993 Released in 1997
Classful routing protocol Classless routing protocol ---
Doesn’t support VLSM and CIDR Supports VLSM and CIDR Supports IPv6
Hop-count metric Hop-count metric Hop-count metric
Doesn't include subnet mask in Includes subnet mask in routing Includes subnet mask in routing
routing updates updates updates
Routing updates are sent in broadcast Routing updates are sent in multicast Routing updates are sent in multicast
(255.255.255.255) (224.0.0.9) (ff02::9)
5 ow. co. Supports IPv6 inherent IPsec
Doesn’t support authentication Supports authentication
authentication

Sends full routing updates Sends full routing updates Sends full routing updates

Bi SB Bi


### Slides — strona 344

RIPv2
RIP Parameters
Administrative Distance
| AD | RIP’s default AD value is 120.
i] The value can be modified, but it is not recommended to do so.
Metric
fix) RIP determines the shortest route to a network by the number of hops (routers) to the
La target network. The route with the least amount of hops is added to the routing table.
=H RIP supports routes of up to 15 hops.


### Slides — strona 345

RIPv2
eee eee ee
(2 e®.
Kc) “eae
@,e
By default, the update value Invalid is also known as an If a route is invalid after 180 The default value is 180
is 30 seconds, and messages expiration timer, and by seconds, it will remain in the seconds.
will be broadcast/multicast default its value is 180 routing table for an additional . oo
ona RIP-enabled interface. seconds, after which the 60 seconds before it is During this time, the router
Example: Two routing entry will indicate removed, and inform its on vi accept new updates
interconnected neighbor destination is unreachable. neighbors of its status. or the route.
routers send each other Example: If a router does
updates every 30 seconds, not receive an update from Total: 180+60=240
even if there is no change in its neighbor within 180
the topology. seconds, it will set the
route’s hop count to 16
(destination is unreachable).


### Slides — strona 346

RIPv2
Auto-Summary
Auto-Summarization Feature
| Auto Summary is a feature that allows automatic summarization of
routes to their classful networks. This allows multiple networks to be
= § @==== represented with a single summary address.
as = = By default, RIP and EIGRP summarize subnets exceeding the classful
4 hs boundaries to a major classful network address in the routing
updates.
6
This feature is often disabled because most address schemes in networks today do not allow
address summaries without compromising communication.


### Slides — strona 347

RIPv2
Network Illustration
Networks A, B, and C cannot reach
each other because their routers do —=,
not ‘know’ each other yet. ee) Gigo/0 |
SS
Once RIP is enabled on all 0/010 So/0/1 =
routers, they will start to share R2 Net B 192.168.20.0/2
routing information. 172.16.0.0/30 172.16.0.4/30
Next, each router will add
remote networks to its table.
R1 will add Nets B and C, for =e, S0/0/0 SOO =,
example. = Gigo/o aoe 00/1 $0i0/1 Gigol0 wl
— 172.16.0.8/30 a7
This process is called — ——
convergence. Net A 192.168.10.0/24 Re BS Net C 192.168.30.0/2
Every router can reach
any network.


### Slides — strona 348

R1(config)#router rip
enables RIP and R1(config-router)#version 2
enters RIP configuration mode. R2(config-router)#no auto-summary
R1(config-router)#network 192.168.10.@
R1(config-router)#network 172.16.0.0
sets the RIP version. R1(config-router)#network 172.16.0.8
R1(config-router)#passive-interface gigabitEthernet 0/0
advertises the network
and enables RIP updates on the R2(config)#router rip
hetworkintertace. R2(config-router)#version 2
R2(config-router)#no auto-summary
disables the auto- R2(config-router)#network 192.168.20.0
summary feature. R2(config-router)#network 172.16.0.0
disables RIP R2(config-router)#network 172.16.0.4
updates on the interface. R2(config-router)#passive-interface gigabitEthernet 0/0


### Slides — strona 349

Ri#show ip route
Theeinple ontherietit 172.16.0.0/16 is variably subnetted, 5 subnets, 2 masks
shows R1’s routing table after C 172.16.0.0/30 is directly connected, Serial@/e/e
RIP finished updating it. L 172.16.0.1/32 is directly connected, Seriale@/e/e
represents the route learned
by the RIP protocol.
C 172.16.0.8/30 is directly connected, Serial@/0/1
. . : L 172.16.0.9/32 is directly connected, Serial@/@/1
An important feature is that if . .
the router finds two equal paths 192.168.10.0/24 is variably subnetted, 2 subnets, 2 masks
to the network, both routes are Cc 192.168.10.0/24 is directly connected, GigabitEthernet0/0e
added to the table, and load L 192.168.10.254/32 is directly connected, GigabitEthernet@/e
balancing is applied.
For example,


### Slides — strona 350




### Slides — strona 351

Ri#show ip protocols
. Routing Protocol is "rip"
displays the
current protocol settings.
This Is'valid forevery dynamic Redistributing: rip
routing configuration, such as
OSPF. Interface Send Recv Triggered RIP Key-chain
Serial0/0/0 2 2
Serial0/0/1 2 2
The output includes:
* Timer information Maximum path: 4
* Advertised networks
* Passive interfaces
* More
Routing Information Sources:
Gateway Distance Last Update
Distance: (default is 120)


### Slides — strona 352

Routing Table Entry
: Command
R 192.168.20.0/24'[120/1]i via 172.16.0.5, '00:00:09,!Serial@/e/e ' |
toad 2 3 4 5 6
; : : : : </>
Show IP Route Output
1. Rout Ril#show ip route
# ROULS'SOULCe: R 192.168.20.0/24 [120/1] via

2. The destination network address and prefix. 172.16.0.5, 00:00:09, Seriale/0/a

3. The AD and metric of the route.

4. Next-hop address through which the packet passes to the target

network.
5. The route age (timestamp).
6. The local outgoing interface that points to the target network.


### Slides — strona 353

Static Default Route Code Example
The static default route redirects packets with unknown R1(config)#ip route 0.0.0.0
destinations to the Gateway of Last Resort, which is a Bolelt@) (nye (Oa
eee ee ea uriicee je a specific direction Ri (config #eouter Cip
{typically to the (Internet). V4 R1(config-router)#
Propagating Default Routes
R2(config)#do show ip route
E) Each routing protocol shares its default routes with all @.0.0.0/@ [120/1] via
& wy routers on the network, through protocol updates. 192.168.12.1, 00:00:26, Gig 0/1
Bea
G eal


### Slides — strona 354

RIPv2
The objective of this lab is to implement and verify dynamic routing
an tei, Ae an PP. using RIP. The RIP protocol is straightforward, and can help
Configu ring and Verifying RIPv2 | understand basic network routing. RIP is no longer commonly in use
30-60 Min. today.
oe ¢ : ® Configure RIPv2.
— 4 : @ Propagate a default route.
Ja =
i b NY s e yr
ce ee | ; wa
| nN ‘Ss ® - * ®@ OS: All platforms ®@ Lab document
ss 8 W ® Tools: Cisco Packet Tracer @ NET-08-L1.pka
; } 7.2.2
{ ‘ ‘,
* |


### Slides — strona 355

OO
Dynamic Routing
OSPFV2


### Slides — strona 356

OSPFv2
OSPF Overview
Open Shortest Path First
@ OSPF is a Link State routing protocol introduced in 1989, with more
advanced features, making it a strong and scalable solution for any
° size network. OSPF was designed as an alternative to RIP.
bad OSPFv2 was released in 1991 and is still in use today.
@
OSPFv3 was developed for IPv6 in 1997.
e


### Slides — strona 357

OSPFv2
Topology Changes and Timers
Monitor the Network
0 OSPFv2 keeps track of changes in the topology, such as when a new network is
B4 added, ora link fails.
Hello
Hello Intervals — “Hello” packets are sent every 10 seconds to all OSPF-enabled
routers.
Dead
ed Dead Intervals — When a router does not receive a “hello” packet from its neighbor
: within 40 seconds, it will consider that neighbor “dead”, and will start looking for
alternative routes.


### Slides — strona 358

OSPFv2
Routers use Link Link State Database When an adjacency is If a router notices Link State Update
State Advertisement stores received LSA initialized, OSPFv2 that parts of its messages are
to advertise the packets, after the exchanges Database topological database responses to LSR
routing topology to routers enable Description packets are outdated, it will messages.
all other local routers OSPFv2 to use the to describe the send a Link State (SUs aresentin
in the same OSPFv2 SPF algorithm to content of the Request to a unicast.
area. calculate the routes. topological database. neighbor for more
LSAs are sent in updated versions of
multicast. those components.
LSRs are sent in
multicast.


### Slides — strona 359

OSPFv2
SPF Algorithm and Tree
Dijkstra
By calculating all routes to each network in the topology using the
Dijkstra Algorithm, OSPFv2 creates a map of the network called an SPF
Tree.
The SPF Tree is stored in a database on the router called a Link State
Database (LSDB).
e


### Slides — strona 360

OSPFv2
OSPF Metric
Best Route Determination mest Calkulation
x OSPF bases its metric calculation on the bandwidth Reference Speed (Mbps):
of the links along the path to the destination. 1000
@ _ Link Cost:
Cost 10
Wi All bandwidth information recorded for the route is Interface Speed (Mbps):
==] calculated using the OSPF formula (all considerations 100
=©5] are summed), resulting in the cost value.
G
The default reference speed is 100 Mbps, and can be adjusted using the auto-cost command.


### Slides — strona 361

Wildcard Masks
Mask Inversion
| Wildcard masks are used in some routing protocols, such as OSPF, as
a inverted subnet masks.
01 ae
0110 re } For example, the subnet 255.255.255.0 inverts to a wildcard mask of
0001
ood 0.0.0.255.
e


### Slides — strona 362

Router ID Configuration
Router ID -
When OSPFv2 is enabled on an interface, the router R1(config)#router ospf 1
must determine if there is another OSPFv2 neighbor on R1(config-router )#router-id
the link. Router IDs are set manually and used to ;
uniquely identify each router. R2(config)#router ospf 1
a R2(config-router)#router-id
First Fallback R3(config)#router ospf 1
‘x If no router ID is configured, the highest IP address of R3(config-router)#router-id
any router Loopback Interface is selected as the router
ID.
Go </>
Second Fallback [|
y If no Loopback Interface is configured, the highest IP
(x) address among its active interfaces is selected as the
(v) OSPFv2 router ID.


### Slides — strona 363

OSPFv2 Areas
What is an Area?
| fy OSPF uses a concept called Areas. A single AS or full topology can be
| im | divided into smaller areas.
| iat Dividing the topology into areas reduces router resource consumption
HMM sand protocol response time.
e


### Slides — strona 364

OSPFv2
Single-Area OSPF Area Illustration
For small to medium size networks that use a single
area, the default OSPFv2 is Area 0. The maximum
recommended area is 50 routers.
Ca — an)
ABR
Multi-Area OSPF > 2c =
=a —Ce aw aa
In larger networks that require more areas, Area 0 will Area 1 Area 0 Area 51
be the backbone area, and all routers outside that area
| | | | will be assigned other unique numbers (1, 2, 3, etc.).
GO
Routing between areas is done by an ABR (Area Border Router).


### Slides — strona 365

OSPFv2
Advantages Disadvantages
Smaller database (LSDB) for each area, saves memory. CPU utilization is high due to the amount of SPF calculations.
Smaller routing table for each area, saves resources. OSPFv2 requires all areas to be connected to the backbone.
Less traffic on the network due to less exchange of routing
information among routers.
Reduced algorithm calculation, only within areas.
In smaller areas, updates regarding changes in the topology
are distributed faster.


### Slides — strona 366

OSPFv2
Network Illustration
Networks A, B, and C cannot
reach each other, because the
routers do not ‘know’ each a
other yet. ee Gigd/0 |
—_«"
Once OSPF is enabled on all S0/0/0 RO SOO —
routers, they will start to share Net B 192.168.20.0/2
routing information. 172.16.0.0/30 172.16.0.4/30
Next, each router adds remote
networks to its table. For So/o/o So/o/0
example, R1 will add Nets B . .
endt’@. = Gigo/0 roe eon s0/0/1 soot eo Gigolo (__}
ef Sf
i———(4 172.16.0.8/30 Ew =
This process is called ar, ae R1 R3 = =i
convergence. Net A 192.168.10.0/24 Net C 192.168.30.0/2
Any router can reach any
network.


### Slides — strona 367

enables OSPF and R1(config)#router ospf 1
enters OSPF contiguration mode: R1(config-router)#router-id 1.1.1.1
router ig sets the TOMTEPOSEF R1(config-router)#network 192.168.10.@ @.0.0.255 area @
R1(config-router)#network 172.16.0.0 0.0.0.3 area @
R1(config-router)#network 172.16.0.8 0.0.0.3 area @
advertises the network R1(config-router)#auto-cost reference-bandwidth 10@0
ant Stables OS8e Updates elythe R1(config-router)#passive-interface gigabitethernet 0/0
network interface.
sets the interface area ID. R1(config-router )#
cetsthe veferenee @0:29:39: %OSPF-5-ADJCHG: Process 1, Nbr 2.2.2.2 on Serial@/0/e from
bandwidth calculation LOADING to FULL, Loading Done
disables OSPF @@:29:59: %OSPF-5-ADJCHG: Process 1, Nbr 3.3.3.3 on Serial@/@/1 from
updates on the interface. LOADING to FULL, Loading Done
Al indi : Please ensure reference bandwidth is consistent across all routers
og message indicates a link to
another OSPF-enabled router.


### Slides — strona 368

Ri#show ip route

The example on the right shows

faieieme 172.16.0.0/16 is variably subnetted, 5 subnets, 2 masks

inisnec upcanng tt. C 172.16.0.@/3@ is directly connected, Seriale/e/e

represents the route learned . . .
by the OSPF protocol. L 172.16.0.1/32 is directly connected, Seriale@/0e/e
An Pe ml eos a C 172.16.@.8/3@ is directly connected, Serial@/0/1
routing Is that i the router finds L 172.16.0.9/32 is directly connected, Serial@/@/1
two equal paths to the network, ; i
bath reuteswill be added tthe 192.168.10.0/24 is variably subnetted, 2 subnets, 2 masks
ing wi . .10. is direc connecte igabi erne

table, and load balancing will be Cc 192.168.10.0/24 is di tly ted, GigabitEth te/e@
applied. 0 .10. is direc connecte igabi erne
pp L 192.168.10.254/32 is directly ted, GigabitEthernete/o
For example,


### Slides — strona 369

Ri#show ip protocols
displays the Outgoing update filter list for all interfaces is not set
current protocol settings. Incoming update filter list for all interfaces is not set
The output includes: Number of areas in this router is 1. 1 normal @ stub @ nssa
* Router ID Maximum path: 4
* Area and process ID
* Advertised networks
* Passive interfaces
* More
displays Routing Information Sources:
timer information.
displays
adjacent OSPF-enabled routers.
Distance: (default is 110)


### Slides — strona 370

OSPFv2
Se Configuring routers to use OSPF with best practices in mind.
Configuring and Verifying OSPFv2
30-60 Min. at \\
gt —lrh f ® Configure OSPF.
; ‘ 2 «€ ; ® Propagate a default route.
_ j cc 5 i =
Se eS
} j
| iY ® 4 ® Os: All platforms ® Lab document
“ig |) ® Tools: Cisco Packet Tracer & NET-08-L2.pka
" y} 7.2.2 or later
|
‘ |
} i % SS — |


### Slides — strona 371

- / : . ee 7 ; 2 = :
‘ 7
= eat ¥ oat / “s
al = g \ . =
i VSso, ~ =
Fees \ 2 —
COTTE & ~
POPE » * a
{ > CAINS ~ 0 ee
J PORE " Fe
COV OSS > &
H 2 ~~ a ———.
i CU i ™
Me, "a », y 4, Fees
Sh SOS jj .
“ : ay Wage, y eS /
( ep y t /
~~" 2 CS — be a!


### Slides — strona 372

ok
aul egal 5 i 2B
— _ = : ste a) :
ie. = 4 a wet NETWORK Sr cay Cm D


### Slides — strona 373

Sir Cy bersacu ity Professional Program
Computer Networking


# Chapter 9: VLANs & Trunk


### Slides — strona 374

Computer Networking
Introduction Network Switch & IOS Switch Securit IP and Routing
to Networks Fundamentals Fundamentals y Concepts
Diagnostics and VLANs Dynamic IPv4 & IPv6é Subnetting
Troubleshooting and Trunk Routing Static Routing Concepts
Access Infrastructure Fiival Proiect
Control List Services d
2


### Slides — strona 375

VLANs & Trunk
Overview
Lesson Objective
Virtual LANs

The objective of this lesson is to learn how

to manage Virtual LANs (VLANs) and about

the impact they have on modern networks. Trunk Protocols

It also covers trunk protocols and the VLAN

Paging PIOCEss. Inter-VLAN Routing

G
3


### Slides — strona 376

CO
VLANs & Trunk
VIRTUAL LANS


### Slides — strona 377

Virtual LANs
VLANs
Virtual Local Area Networks
VLAN is acommon concept and practice among network administrators.
@-B Most networks today implement VLANs in one way or another.
VLAN is a Layer 2 feature that allows virtual network segmentation,
1 meaning dividing a physical network into separate logical networks.
GJ GJ Each logical network is a VLAN and represents a separate broadcast
domain.
B
The same rules that govern LANs also apply to VLANs.
5


### Slides — strona 378

Virtual LANs
VLANs
How do VLANs work?
Multiple ports are configured on the switch and associated with a
VLAN, creating a logical barrier between end devices connected to
the switch.
This enables network administrators to create several Virtual LANs
ona single switch.
VLANs are logical, not physical, divisions.
Transferring data between VLANs requires a router or other Layer 3 device.
6


### Slides — strona 379

Virtual LANs
Benefits of using VLANs
Improved Security
VLANs help separate and isolate sensitive user data, and reduce the chance
of spreading malicious data and unauthorized user access via network traffic.
Enhanced Performance
we VLANs reduce the size of broadcast domains, enhance performance, and
GF minimize unnecessary traffic on the network.
Simplified Management
e2 ra} VLANs allow administrators to group end devices and users by departments (such as
, 2 by job roles) rather than by physical location. This improves network policy flexibility
and reduces network costs.
7


### Slides — strona 380

Virtual LANs
i ?

What is a VLAN ID? When traffic passes through a VLAN, it must be identified to keep it
separate from traffic in other VLANs. A unique ID identifies a VLAN in
the network.

There is complete separation between virtual networks, whereby
users on VLAN 10 cannot access user data on VLAN 20.
=o On Cisco devices, the valid ID range for VLANs is 1 to 1005. There is
also an additional extended range of valid VLAN IDs from 1006 to
4094. a
B
The extended range of VLAN IDs from 1006 to 4094 is primarily
used in large networks, such as an ISP network.
8


### Slides — strona 381

Virtual LANs
Default VLAN Data VLAN Voice VLAN Management VLAN Native VLAN
comes aia ) Qe g
ae

Z L@ |
VLANs 1 and 1002- VLANs 2-1001 are This type of VLAN is Interface VLAN 1 is a Native VLANs are
1005 are reserved commonly used for designed for VoIP management VLAN designed to forward
and added data exchanges. (Voice over IP) used for SVI. untagged traffic, such
automatically during Their main function is network traffic. Management VLANs as DTP and CDP,
device installation. to tag data traffic enablevremote among switches. By
These VLANs cannot with an identifier. connection and default, MELON 1 ista
be removed or conduct basic native and
renamed. network functions. management VLAN.

9


### Slides — strona 382

show vlan brief
S1#show vlan brief
The command shows that the
switch is already pre-configured VMAS Neti SASGTEUE POIneS
with VLAN 1, and all ports are nn
associated with it by default.
Additional VLANs are available
in the switch configuration.
They are reserved and known
as default VLANs. . .
1002 fddi-default active
1003 token-ring-default active
1004 fddinet-default active
1005 trnet-default active


### Slides — strona 383

Virtual LANs
Switchport Modes
Access
Access ports carry traffic only on the VLAN to which they belong. Access mode
> should only be defined on ports connected to end devices, such as PCs.
As a security-related best practice, it is highly recommended to enable Access
mode for a port, before assigning it to a VLAN.
Trunk
‘~. Trunk ports carry traffic for different VLANs and devices. The port sets unique
Bays identifier tags on the frame, using either the 802.1Q or ISL encapsulation protocols.
This ensures that each frame is directed to its intended VLAN.
11


### Slides — strona 384

vlan <id>
name <word>
The example on the right shows S1(config)#vlan 100
VLAN 100 and 200 creation, whereby S1(config-vlan)#name class A
a valid ID is any number between S1(config-vlan)#exit
2 and 1001 (1, 1002-1005 are
ossunledh: S1(config)#vlan 200
S1(config-vlan)#name class B
It is recommended to assign an $1(config-vlan)#exit
appropriate to the VLAN
upon creation.


### Slides — strona 385

switchport mode access
switchport access vlan <id>
S1(config)#interface range fastEthernet 0/1-2
Thevassignment of hosts (end S1(config-if)#switchport mode access
devices, such as PCs) to different S1(config-if)#switchport access vlan 100
VLANs is done by matching the an .
interconnected interface to the S1(config-if)#exit
appropriate VLAN.
S1(config)#interface range fastEthernet 0/3-4
a ae P S1(config-if)#switchport mode access
Tip: Assigning multiple ports to a an .
VLAN simultaneously can be done S1(config-if)#switchport access vlan 200
using the command. $1(config-if)#exit


### Slides — strona 386

Si#show vlan brief
VLAN Name Status Ports
By running the oo Le ee 8
command, it'is.easy to spot:the 1 default active Fa@/5, FaQ/6, FaQ/7, Fae/8
two new VLANs and the Fa@/9, Fa@/10, Fa@/11, Fae/12
interfaces assigned to them. FaQ@/13, FaQ@/14, Fa@/15, Fa0/16
Fa@/17, FaQ@/18, FaQ/19, Fae/20
Fa@/21, FaQ/22, FaQ/23, Fae/24
To display the interface mode, Gig@/1, Gige/2
use ‘
1002 fddi-default active
10@3 token-ring-default active
1004 fddinet-default active
1005 trnet-default active


### Slides — strona 387

switchport voice vlan <id>
: : S1(config)#interface fastEthernet 0/1
eee area S1(config-if)#switchport mode access
. S1(config-if)#switchport access vlan 100
the network.
S1(config-if)#exit

The example on the right shows
how a Voice VLAN is set up on
an interface.
Note: VoIP settings on the
network are necessary, but are
not within the scope of this
course.


### Slides — strona 388

CO
VLANs & Trunk
TRUNK PROTOCOLS


### Slides — strona 389

Trunk Protocols
Trunk Mode
What is Trunking?
Trunk mode is designed to transmit multiple VLAN traffic sessions,
over the same physical connection, to a remote device, such as a
switch or router.
This is done by tagging frames with the source VLAN, ensuring that
the Trunk link forwards the VLAN frames to the same VLAN on
another switch. This helps maintain the isolation of other devices.
6
Trunk mode makes sure that relevant information stays among devices within the
same VLAN (such as switches). However, routing among VLANs still requires a router.
17


### Slides — strona 390

Trunk Protocols
Trunking Protocols
Inter-Switch Link
, | it | ln ISL is a proprietary protocol developed by Cisco that only operates on Cisco
cisco equipment.
The protocol adds VLAN information to Ethernet frames.
IEEE 802.1Q
802.1q or dotigq is an industry standard developed by IEEE that allows trunk
IEEE link creation between various vendor switches.
J Cisco uses this standard as its default trunk protocol.
Unlike ISL, 802.1q encapsulates the VLAN info in the frame.
18


### Slides — strona 391

Si(config)#interface gigabitEthernet 0/1
S1(config-if)#
The S1(config-if)#exit
command sets the interface to
trunk mode and creates trunk . . . .
links. S2(config)#interface gigabitEthernet 0/1
S2(config-if)#
S2(config-if)#exit
To display the trunk’s configuration,
run the S1#show interfaces trunk
command: Port Mode Encapsulation Status Native vlan
al
Note: The switchport mode
trunk command creates a static S2#show interfaces trunk
trunk link, without using the Port Mode Encapsulation Status Native vlan
DTP protocol. 1


### Slides — strona 392

Trunk Protocols

Dynamic Trunking Protocol

DTP is a protocol developed by Cisco to automate the creation of
~, trunk links, mainly to save time and prevent misconfiguration.
>_> Ne DTP operates on Cisco switches by default, and uses a special packet
» >> to "negotiate" the interconnected interfaces.
DTP is also responsible for selecting the trunk protocol on both sides.
&
DTP can be disabled on specific ports for security purposes (such as to prevent switch spoofing attacks).
20


### Slides — strona 393

Trunk Protocols
DTP Modes
The protocol includes two port modes for interface negotiation.
Dynamic Auto
This mode, which is the default for every port, is passive and does not negotiate.
Instead, it waits until an explicit request is received from the other side, and then
establishes the trunk link.
Dynamic Desirable
This mode actively attempts to change the mode of the interconnected interface
via DTP packets, to establish a trunk link.
Once a directly interconnected port is set to trunk, dynamic auto, or dynamic
desirable, a link will be established.
21


### Slides — strona 394

switchport mode dynamic <mode>
S1(config)#interface gigabitEthernet 0/1
The example on the right shows the S1(config-if)#
configuration of DTP modes on the S1(config-if)#exit
interconnected interfaces of the
switches. 4 : 4 4
Remember: Dynamite Aurerie the S1(config)#interface gigabitEthernet 0/1
default mode. S1(config-if )#
S1(config-if)#exit
To display the interface mode,
use f


### Slides — strona 395

switchport nonegotiate
Since using DTP can make the switch S1(config)#interface fastEthernet 0/1
vulnerable to a VLAN attack, it is best S1(config-if)#switchport mode access
to disable DTP on a port connected S1(config-if)#
to an end device. S1(config-if)#exit
Configuring the port in access mode S1#show interfaces switchport
is not enough, and is Name: FaQ@/1
required. Switchport: Enabled
Administrative Mode: static access
To display the interface mode, use Operational Mode: down
; Administrative Trunking Encapsulation: dotiq
Operational Trunking Encapsulation: native


### Slides — strona 396

Trunk Protocols
Port Configuration Options
Mode Negotiation Results
Dynamic Dynamic
Auto Desirable Trunk Agnes
Dynamic Access Trunk Trunk Access
Auto
Dynamic Trunk Trunk Trunk Access
Desirable
Trunk Trunk Trunk Trunk ---
Access Access Access --- Access
24


### Slides — strona 397

Trunk Protocols
Native VLAN
What is a Native VLAN?
of Native VLANs process untagged frames when they reach trunk ports.
Rod Untagged frames are frames that do not have a source or destination VLAN.
= VLAN 1 is the default native VLAN.
Why is Native VLAN Required?
>a Without Native VLANs, sending and receiving updates for protocols such as CDP, VTP,
DTP, and STP among interconnected switches would not be possible, since trunk ports
drop untagged frames.
25


### Slides — strona 398

Trunk Protocols
Important Native VLAN Points
Best Practice
A best practice regarding Native VLANs is to re-assign them to non-default VLANs, such
as VLAN 200, for security purposes. Doing so, can, for example, mitigate Double Tagging
attacks.
Identical Native VLAN
The same Native VLAN must be used on both ends of the trunk link. If not,
) c) untagged frames will not be delivered correctly, and the switch’s OS will
bs PS continuously send warning messages to the user, in the form of:
1 ff) “%CDP-4-NATIVE_VLAN_MISMATCH: Native VLAN mismatch discovered on
GigabitEthernet0/1 (200), with $2 GigabitEthernetO/1 (1).”
26


### Slides — strona 399

switchport trunk native vlan <id>
S1(config)#interface gigabitEthernet 0/1
The example on the right shows how S1(config-if)#
to change the default native VLAN S1(config-if)#exit
on two interconnected switches.
S2(config)#interface gigabitEthernet 0/1
S2(config-if)#
To display the Native VLAN settings S2(config-if)#exit
use
S1#show interfaces trunk
Port Mode Encapsulation Status Native vlan
GigQ/1 on 802.1q trunking
S2#show interfaces trunk
Port Mode Encapsulation Status Native vlan
GigQ@/1 on 802.1q trunking


### Slides — strona 400

CO
VLANs & Trunk
INTER-VLAN ROUTING


### Slides — strona 401

Inter-VLAN Routing
Inter-VLAN Routing Overview
Inter-VLAN Routing
Although VLANs are logical segments, they still operate within the
framework of a network, which means they are also broadcast
domains.
Switches (which generally operate at Layer 2) cannot move traffic
across different VLANs or broadcast domains.
Routing data among different VLANs requires a Layer 3 device (such
as a router), which encapsulates and decapsulates the frames.
B
A Layer 3 switch (also known as a multilayer switch) can be used for routing among VLANs,
which can also reduce the amount of network components needed to handle the traffic.
29


### Slides — strona 402

Inter-VLAN Routing
Router-On-A-stick
How Does Inter-VLAN Routing Work?
The most common technique for Inter-VLAN Routing is called
Router-On-A-Stick.
This method is effective because it requires only a single physical
connection between the switch and the router, avoiding the need
SS for additional components and costs.
&
30


### Slides — strona 403

Sub-Interface
Multiple IP Addresses Sub-Interface Command
Multiple IP addresses are possible because a R1(config)#interface
1 ni oy . . gigabitEthernet @/0.1
router’s single physical interface is segmented into
multiple logical interfaces, called sub-interfaces. R1(config)#interface
@ gigabitEthernet 0/0.2
Logical Interface R1(config)#interface
aa Each sub-interface is configured with a unique IP gigabitEthernet @/0@.3
sve | address and subnet mask. Every sub-interface
5 represents a default gateway for a specific VLAN.
Simple rule: The number of VLANs dictates the number of sub-interfaces.
31


### Slides — strona 404

Switchport mode trunk
S1(config)#interface gigabitEthernet 0/1
S1(config-if)#switchport mode trunk
S1(config-if)#exit


### Slides — strona 405

- R1(config)#interface gigabitEthernet 0/20
pees eee _ R1(config-if)#
. Enter e€ physical interface : . .
and enable tt: R1(config-if)#exit
R1(config)#interface gigabitEthernet
2. Create a sub-interface. R1(config-subif)#encapsulation dot1Q
3. Configure interface R1(config-subif)#ip address
encapsulation on 802.1q and R1(config-subif)#exit
assign the appropriate VLAN ID.
R1(config)#interface gigabitEthernet
R1(config-subif)#encapsulation dot1Q
4. Configure the VLAN’s R1(config-subif)#ip address
corresponding IP address R1(config-subif)#exit
and mask (default gateway).
5. Repeat this process for
every VLAN.


### Slides — strona 406

Ri#show ip interface brief
Interface IP-Address OK? Method Status
Protocol
Use
to display the interface settings
and mode.
GigabitEthernet@/1 unassigned YES unset administratively down down
= Vlan1 unassigned YES unset administratively down down
e
command shows additional
details, such as the interface
and its VLAN ID.


### Slides — strona 407

Inter-VLAN Routing
Lab NET-09-L1 Jai
a = Eo" Sway . The objective of this exercise is to learn how to configure
Configuring VLANs, Trunks, and More | VLANs and trunks.
oe r SS ‘ ” Configure & verify VLANs.
- a «€ ; ‘ 8 Configure trunks and native VLANs.
7 —. 4 = ® Configure R.O.A.S
a /, i,
P ton » >
j l
| ® ; @ r 8 OS: All platforms ® Lab document
=m 8 Tools: Cisco Packet Tracer ®& NET-O9-L1.pka
. y} 722
| .
‘ |


### Slides — strona 408

- / : . ee 7 ; 2 = :
‘ 7
= eat ¥ oat / “s
al = g \ . =
i VSso, ~ =
Fees \ 2 —
COTTE & ~
POPE » * a
{ > CAINS ~ 0 ee
J PORE " Fe
COV OSS > &
H 2 ~~ a ———.
i CU i ™
Me, "a », y 4, Fees
Sh SOS jj .
“ : ay Wage, y eS /
( ep y t /
~~" 2 CS — be a!


### Slides — strona 409

ok
aul egal 5 i 2B
— _ = : ste a) :
ie. = 4 a wet NETWORK Sr cay Cm D


# Chapter 10: Diagnostics & Troubleshooting


### Slides — strona 410

= A ay canoe ee ee |
Diagnostics & Troubleshooting
Computer Networking


### Slides — strona 411

Computer Networking
Introduction Network Switch & IOS Switch IP & Routing
to Networks Fundamentals Fundamentals Security Concepts
Diagnostics & Dynamic IPv4 & IPv6é Subnetting
Troubleshooting NLANs & Trdnis Routing Static Routing Concepts
Access Infrastructure Final Project
Control List Services
2


### Slides — strona 412

Diagnostics & Troubleshooting
Overview
Lesson Objective
The object of this lesson is to understand Troubleshooting Methods
how to diagnose network issues and
troubleshoot them. Neighbor Discovery Protocols
The lesson also introduces useful tools for
troubleshooting and explains how CDP Log Events & Syslog Server
works, what log events are, syslog server
operation, and the Network Time Protocol. Network Time Protocol
G
3


### Slides — strona 413

i
Diagnostics & Troubleshooting
Troubleshooting Methods


### Slides — strona 414

Troubleshooting Methods
Troubleshooting Overview
What We Will Learn
Issues can and will arise, even in networks that were designed using
the most advanced technologies.
=
This lesson covers the ways network issues can be resolved and the
tools that can help resolve them quickly and efficiently.
An important aspect of network troubleshooting, also described in
this lesson, is the usage of discovery protocols.
e
5


### Slides — strona 415

Troubleshooting Methods
Troubleshooting
Documentation
y
— Quick and efficient troubleshooting is based, in part, on continuous and detailed
= network-related documentation.
What Does Documentation Include?
ii =. Network documentation includes the following: physical and logical topological
C= diagrams, network and end-device backup configuration files, IP and MAC addressing
—— schemes, and network performance baselines.
6


### Slides — strona 416

Troubleshooting Methods
Gather Information
The first and most important step is gathering a a
information and symptoms from network Isolate the Problem
devices, ehdl systems Jana OSErs, Based on the symptoms, eliminate variables until
a single problem or a set of related problems is
> identified as the cause.
Implement a Solution
Consider the severity of the problem and the
impact of the solution. Then, begin planning, Se Problem Solved?
testing, and documenting possible solutions.
If the problem was not solved, repeat steps two
and three again and deepen the research.
Documentation 7
Document every step you took in the process for
future reference.
7


### Slides — strona 417

Troubleshooting Methods
Gathering Information

01 Question end users | CMD network commands 05

02 Protocol analyzers

(Wireshark, etc.) show and debug commands 06
03 Physical troubleshooting tools IP SLA: monitors network 07
(cable tester, others) performance in real-time
Network . .
04 management software | Neighbor Discovery Protocols 08
8


### Slides — strona 418

Troubleshooting Methods
Open Systems Interconnection (OSI) Troubleshooting Methods
In this method, the starting In this method, the starting In this method, the starting
point is at the bottom of the point is at the top of the OSI point is not predefined as in
OSI model: the physical layer. model: the application the other methods.
The examination starts from layer. A particular layer is selected
the network’s infrastructure, The examination starts from and examined; if the layer
such as cables and NICs. the application itself. functions, then the next
layer to examine is the one
above it. If the layer is
faulty, then the next one
should be the one below it.
9


### Slides — strona 419

Troubleshooting Methods
Software Tools
Software Troubleshooting Tools
Network Management Software (NMS) provides excellent tools for
(@) © troubleshooting.
NMS continuously monitors network activity and establishes a clear
baseline for reference purposes. This enables network administrators
= to promptly identify issues, and, in some cases, even predict the
occurrence of such issues.
e
10


### Slides — strona 420

Troubleshooting Methods
show ip interface brief show running-config show startup-config

show interfaces show ip route verifies show ip interface show running-config show startup-config
outputs a large network reachability. brief presents only displays the complete displays the complete
volume of It will indicate if information about device configuration device configuration
information, including routing protocols are interfaces associated that is being used at that ree: used
interface errors, — operating as they with the IP protocol. that time. when it loads.
bandit utilization, should. The command
and interface speed. outputs a detailed

summary of interface

status and IP

addresses.

11


### Slides — strona 421

e
Extended ping & traceroute Commands
, Extended Ping Example
Extended Ping ae
ping
Extended ping is used to perform advanced checks of Protocol [ip]:
network connectivity. It is also able to change the source Target IP address:
IP on the packet leaving the router. Repeat count [5]:
Wd Datagram size [100]: C
Timeout in seconds [2]:
Traceroute Sending 6, ) ICMP Echos to
The traceroute command discovers the path packets nait » timeout is :
take to a remote destination and where routing failures vere ele)
Success rate is 100 percent (6/6),
occur.
round-trip min/avg/max = @/0/3 ms
12


### Slides — strona 422

OO
Diagnostics & Troubleshooting
Neighbor Discovery Protocols


### Slides — strona 423

CDP Overview

Cisco Discovery Protocol
CDP (Cisco Discovery Protocol) is a Layer 2 Cisco proprietary

8 | | | Py | | | a protocol enabled by default on all Cisco devices. Its purpose is
similar to the purpose of NDP.

C | Ss C Oo 7 CDP can be disabled on specific devices or interfaces for
security reasons.
é
14


### Slides — strona 424

Neighbor Discovery Protocols
Eavesdropping Information Gathering
‘4

[i ‘
Since CDP does not encrypt CDP gathers information on CDP advertisements are
transmitted data, it is the local device and special packets that reveal
vulnerable to reconnaissance- periodically sends it to all device details to neighbors
type attacks (such as Sniffing). directly connected devices. also running CDP.
Such attacks will allow the When advertisements are
attacker to map the victim’s received, they are stored in
network and more. the neighbor table.

15


### Slides — strona 425

CDP Advertisement
CDP Packets
CDP includes the following data in advertised packets:
* Type of device (router, switch)
l *« Device name
° ¢ Interconnected interfaces

tL. DP * IOS version
* Next-hop IP
* Connection’s duplex mode (full, half)

ES
16


### Slides — strona 426

Neighbor Discovery Protocols
Mismatch Detection
Mismatch Error Detection
CDP includes a unique feature that can detect a protocol-connection
mismatch.
When such a mismatch is detected, CDP notifies the network
administrator by recording the incident in a log.
® Examples of mismatch types include:
¢ Native VLAN mismatch
* Duplex mismatch
e
17


### Slides — strona 427

CDP Intervals
CDP Show Command Output
CDP Packet Timer
S1#show cdp
fe HID CDP sends advertisement packets every 60 Global CDP information:
j seconds by default to all directly connected Sending CDP packets every
devices Sending a holdtime value of
, a Sending CDPv2 advertisements is enabled
CDP Hold Timer
If a device does not receive CDP packets from a
Me, I Pal < neighbor for 180 seconds, it will consider that
a LN neighbor "dead“ and remove it from its
neighbor table.
@ </>
The timers can be modified.
18


### Slides — strona 428

cdp run \ enable
#Enable\Disable on Device:
Because CDP is not secure or S1(config)i#cdp run
encrypted, it is easy to eavesdrop. S1(config)#no cdp run
If necessary, the protocol can be
turned off entirely on the device or #Enable\Disable on Port:
on selected interfaces. S1(config)#interface range fastEthernet @/1-24
S1(config-if-range)#cdp enable
Recommended: Enable CDP S1(config-if-range)#no cdp enable
only for port interconnection
with other network devices.


### Slides — strona 429

The command
displays all connected devices that
CDP can communicate with. | a) LFA
The command s4 R4 $2
displays more information on each device,
such as IP address and IOS version.
S1#
Capability Codes: R - Router, T - Trans Bridge, B - Source Route Bridge
S - Switch, H - Host, I - IGMP, r - Repeater, P - Phone


### Slides — strona 430

Neighbor Discovery Protocols
Link Layer Discovery Protocol
LLDP is a Neighbor Discovery Protocol similar to CDP that was
developed by the IEEE.
IEEE LLDP is an industry standard protocol, meaning it is not proprietary
° and can operate on any network device, and even on PCs and servers.
Although LLDP is not enabled by default on Cisco devices, it is fully
supported.
e
21


### Slides — strona 431

LLDP Intervals
LLDP Sh Cc d Output
LLDP Packet Timer aii
Si#show lldp
AD LLDP sends advertisement packets every 30 Global LLDP Information:
seconds by default to all directly connected Status: ACTIVE LLDP advertisements are
/ devices sent every
. a LLDP hold time advertised is
LLDP Hold Timer
If a device does not receive LLDP packets from a
~ t a neighbor for 120 seconds, it will consider that
= . neighbor "dead“ and remove it from its neighbor
table.
O </>
22


### Slides — strona 432

Lldp run \ receive \ transmit
LLDP is also not secure or encrypted, #Enable\Disable on Device:
like CDP. If necessary, it can be turned S1(config)#11ldp run
off entirely on the device or fora S1(config)#no lldp run
specific direction on selected
interfaces.
S1(config)#interface range fastEthernet @/1-24
Recommended: Enable LLDP S1(config-if-range)#lldp transmit
only on ports interconnected S1(config-if-range)#no lldp transmit
with other network devices. S1(config-if-range)#lldp receive
S1(config-if-range)#no lldp receive


### Slides — strona 433

LLDP show commands are similar to CDP
show commands but can display additional SF, — ,
information. — f ——€ ——_ (4
S41 R1 $2
The commands include
and :
S1#
Capability codes:
(R) Router, (B) Bridge, (T) Telephone, (C) DOCSIS Cable Device
(W) WLAN Access Point, (P) Repeater, (S) Station, (0) Other
Total entries displayed: 1


### Slides — strona 434

ee eee
Diagnostics & Troubleshooting
Log Events & Syslog Server


### Slides — strona 435

Log Events & Syslog Server
Overview
What Is Syslog?
Syslog is a standard for logging messages.
Each device records actions and events that occur like a
— — private diary.
| LOG Among other tasks, network administrators need to monitor
the network to ensure smooth, errorless functionality.
__J} Monitoring the network improves troubleshooting capability
and helps identify issues such as device health and network
load.
&
The syslog protocol is documented in RFC 5424.
26


### Slides — strona 436

Log Events & Syslog Server
System Log Events
Why Are Logs Useful?
System notification logging increases a network administrator's
awareness of hardware or software malfunctions, service status,
and security accountability.
In some cases, logs can be used to predict component failures.
Log analysis can help administrators troubleshoot the system and
can be useful to information security experts when investigating
security breaches.
Syslog messages can be stored locally on the device or on a syslog server in the network.
27


### Slides — strona 437

Log Events & Syslog Server
Device Logs
Log Storage
Log storage takes up space, and can, in some cases, degrade
system performance.
= Log message count is limited due to buffer size.
= Collecting logs from separate devices can take a long time.
= RAM is erased upon device power off.
&
28


### Slides — strona 438

Log Events & Syslog Server
— {__
|
A logging buffer is a Console line is a method of Terminal line is a method of If a syslog server is
predetermined storage viewing messages locally via viewing messages via a CLI configured on the device,
space allocated on RAM the console window. program (such as Putty). the device will send all
for syslog messages. syslog messages to the
server over the UDP 514
port.
29


### Slides — strona 439

Log Events & Syslog Server
Syslog Server
What Is a Syslog Server?
A syslog server is a computer that runs syslog software.
The syslog software concentrates logs from all devices (PC, router,
etc.) on the network into one centralized location, which makes
management and log backup easier.
It also offers a convenient user interface.
This way of working is more efficient than storing logs in RAM.
Many free and enterprise versions of syslog exist, such as the Kiwi Syslog Viewer.
30


### Slides — strona 440

Log Events & Syslog Server
Severity & Facility
Syslog messages include several pieces of information, of which the most important are:
Message Severity
The urgency of the log message is represented by its severity level, which is a number
value from 0 to 7. Level 0 indicates emergencies, and 7 indicates system debugging.
The values also represent critical malfunctions and system warnings.
Message Facility
The facility parameter indicates the source that generated the message, which,
for example, can be a network card or routing protocol.
The facility can be a hardware component, protocol, or system service.
31


### Slides — strona 441

Log Events & Syslog Server
Syslog Message Severity Levels
The following table lists syslog severity levels with their number values.
The lower the number, the higher the severity.
Severity Levels
Message Type Severity Level Explanation
Emergency Level 0 System unusable
Alert Level 1 Immediate action is required
Critical Level 2 Critical condition
Error Level 3 Error condition
Warning Level 4 Warning condition
Notification Level 5 Normal, but important
Information Level 6 Informative message
Debugging Level 7 Debugging message
32


### Slides — strona 442

, Log Event ; ; ; , F
i*Dec 28 19:01 i LINK} =5= i CHANGED: 1 Interface GigabitEthernet@/1, changed state to up}
: 1 1 2 t 34 4 ' 5 b>
Enable GigO/1 Log
1. Timestamp: records the time and date of the log (this service is R1(config)#interface gigabitEthernet @/1
disabled by default and should be enabled once so the system has the R1(config-if)#no shutdown
correct time info)
2. Facility: The category of the source that created the log message. In
the example above, link represents the state of the router's hardware
ports.
3. Severity: The severity level, which, in the example above, indicates
that it is a notification message.
4. Mnemonic: a device-specific code that identifies the log message
5. Text Description: the log/event description and other details
33


### Slides — strona 443

Log Events & Syslog Server
Typical configuration commands used to set up syslog on a Cisco device:
Cisco Syslog Commands
Command Description
logging host Sets the destination syslog server
logging trap Determines what log severity levels to send to the server
won sienna play Attaches time information to the alerts
datatime msec
logging console Shows system messages on the screen of the console connection (enabled by default)
terminal monitor Shows system messages on the screen of a remote connection (Telnet, SSH)
login buffered Saves system messages to the RAM (enabled by default) FEE
34


### Slides — strona 444

R1(config)#logging host 172.16.0.250
R1(config)#logging trap debugging
The dad command sets R1(config)#logging userinfo
theldestination |P'of-the syslog R1(config)#service timestamps log datetime msec
server, to which all logs are sent.
R1(config)#do show logging
The command <Output Omitted>
sends all severity log levels to ESM: @ messages dropped
the server (levels 7 and above). ,» 9 message lines logged
(udp port 514, audit disabled,
authentication disabled, encryption disabled, link up),
The remaining commands in 2 message lines logged
. d
the example on the right are @ message lines rate-limited,
used to add time records. .
@ message lines dropped-by-MD,
xml disabled, sequence number disabled
filtering disabled


### Slides — strona 445

aa 2... =...
Diagnostics & Troubleshooting
Network Time Protocol


### Slides — strona 446

Network Time Protocol
NTP Overview
What is NTP?
NTP (Network Time Protocol) is responsible for the synchronization of
4 the time and date across all devices on the network.
NTP is a simple client-server protocol and is implemented in networks
everywhere.
, It is very easy to set up and even has an authentication mechanism
for security.
NTP operates on UDP port 123 and is defined in RFC 1305.
37


### Slides — strona 447

Network Time Protocol
Time Configuration
Date and time for network devices can be set in one of two ways:
Vaal Cogeco eee =o”
This method requires manual setting of the time and date on each device on the
network.
It is not recommended to work this way for various reasons, among which is the lack of
scalability for large networks. (Setting the clock in every device will waste valuable time.)
Automatic Configuration
This method requires an available and configured NTP server.
Only the server’s IP address needs to be set on network devices.
This ensures that all devices on the network will be set to the most accurate
A) eS) 2 time and date automatically.
Cisco routers can be configured to act as NTP servers. a
38


### Slides — strona 448

NTP Usage
=o000 Cisco routers and switches (and many other devices around the world) use NTP to
= determine the date and time, although routers and switches can also act as NTP servers.
Stratum Model
Stratum levels define the distance from high-precision reference clocks, which begin with
stratum 0, to devices connected hierarchically. Servers linked to the reference clock are
stratum 1, devices that receive the time from the servers are stratum 2, and so on.
To avoid delays, a maximum of 15 levels are allowed. a
Services
rx Accurate time settings are crucial for many protocols and device functions. For example,
DHCP leases and syslog events are time-sensitive services. Timestamps are extremely
Caw important for troubleshooting, management, and network security.
39


### Slides — strona 449

clock set <hh:mm:ss> <day> <month-name> <year>


### Slides — strona 450

R1(config)#
To make R11 set the clock with R1(config)#do show clock
an external NTP server, use the 18:58:46.855 UTC Sat Dec 28 2019
command together
with the server’s IP. R1(config)#
R1(config)#interface gigabitEthernet 0/1
Verify the device time information R1(config-if)#no shutdown
using the command or %LINK-5-CHANGED: Interface GigabitEthernet@/1,
changed state to up
Once the device clock is
tuned correctly, run
, which logs device
messages and events with a
time and date.


### Slides — strona 451

ntp master <1-15>
R1(config)#ntp master
R1(config)#do show run ntp


### Slides — strona 452

Network Time Protocol
; 2 = eee The objects of this lab are to answer questions based on
Pac. et material covered in the lesson and understand how to
Configure NTP and Syslog | configure NTP and syslog servers.
a ie r @ yA : 1 Answer the questions.
. " ‘ « ; ® Configure Syslog.
,—-=1 Ts” = ® Configure NTP.
| —an ® 8 OS: All platforms © Lab document
: ® Tools: Cisco Packet Tracer ® NET-10-L1.pka
. y) 7.2.2 or higher
\ |
i e { ~ 43


### Slides — strona 453

d f 9 rd ; - * 5 y A ~ - ‘
g 1 ’ (fp ee .

# . ~<e "SEG fas f
i < ‘ hs, < : *, pd y
OS ~ a . > > SS
SS errs. \ <i -—~ ~ u
' SISOS \ ~~

Conk ; > ~~

' Cea SD 2 .——

ys \. y 7 . =

Tim By a . i

>. ye Cy fan. a ae


### Slides — strona 454

—— — “a : ™ Ty .
ie. = 4 a wet, NETWORK ga Cm D


# Chapter 11: Access Control List


### Slides — strona 455

— a a toca NTU api =, 0 i D
_ Access Control List
Computer Networking


### Slides — strona 456

Computer Networking
Introduction Network Switch & IOS Switch IP & Routing
to Networks Fundamentals Fundamentals Security Concepts
Diagnostics & Dynamic IPv4 & IPv6é Subnetting
Troubleshooting NLANs & Trdnis Routing Static Routing Concepts
Access Infrastructure Final Projact
Control List Services J
2


### Slides — strona 457

Access Control List
Overview
Lesson Objective
The object of this lesson is to understand the ACL Overview
basic concepts of an Access Control List, and
how named and numbered standard ACLs :
. Standard ACL Implementation
are configured.
The lesson also explains Extended Access
Lists. Extended ACL Implementation
G
3


### Slides — strona 458

CO
Access Control list
ACL OVERVIEW


### Slides — strona 459

ACL Overview
Concept: Access Control List
Where it is used
ACUs are used in
° Computer Networks (Firewalls, Switches and Routers)
tl ° Computer File Systems (Servers and Workstation)
° Web Portals (Canvas, Amazon.com)
° Cloud Configurations (Amazon Web Service VPC, Microsoft Azure VNET)
é
5


### Slides — strona 460

ACL Overview
ACL Definition — Computer Networks
What is ACL?
ACL (Access Control List) is a rule-based feature that allows network
administrators and engineers to configure basic traffic filtering.
MED “YD ACLis aseries of commands that, based on information in the packet
header, determine whether to drop a packet or forward it.
é
6


### Slides — strona 461

Stateless vs Stateful
Stateless vs Stateful

One device that you place on ACU’ are firewalls.
° Stateless firewalls will remember the state of the session and close

i it once it is completed.
° Stateful firewalls will understand the details of a connection and

allow the return traffic.
Most decent firewalls today are stateful.
é
4


### Slides — strona 462

ACL Overview
ACL Advantages
Advantages of configuring an Access List on a device:
Network Performance
Network performance can be improved by allowing only relevant services to
communicate with devices across the network.
i For example, restricting the network to block video traffic can improve network
TL performance.
Securing the Network
+
In a network environment, users may be restricted from accessing sensitive services.
&) ACL provides a basic level of network security by allowing some hosts to access parts of
+ + the network, while preventing others from accessing the same parts.
8


### Slides — strona 463

Additional ACL Capabilities
Protocol Restriction
ACLs can also restrict the following:
¢ Routing protocol advertisement messages
¢ Packets from security protocols
¢ Packets from other protocols, such as ICMP
9


### Slides — strona 464

ACL Overview
Standard Vs Extended
There are Standard ACLs and Extended ACLs, with the difference in the parameters examined in the process.
Standard ACLs
Standard ACLs examine only the source IP address when implementing restrictions.
Cisco recommends to place this type of ACL as close to the destination device as
possible.
Extended ACLs
Extended ACLs filter packets according to the following parameters: protocol type,
source or destination IP address, and source or destination port.
Cisco recommends to place this type of ACL as close to the source as possible.
10


### Slides — strona 465

ACL Overview
Traffic Direction

When configuring ACL, traffic direction, inbound or outbound, must be specified on an interface. This is done

so that the router will implement the proper restrictions when examining the source network and destination.

Inbound ACL
> Configures the ACL for inbound traffic.
The router will examine incoming traffic to the interface.
Outbound ACL
é Configures the ACL for outbound traffic.
The router will examine outgoing traffic from the interface.
11


### Slides — strona 466

Wildcards
What are Wildcards?
Wildcards are inverted subnet masks that can be used in statements
— in both Extended and Standard ACLs.
© Ti | For example, 255.255.255.0
1 Paes (binary equivalent = 11111111.11111111.11111111.00000000)
0001 OB inverts to a wildcard mask of 0.0.0.255
1
(binary equivalent = 00000000.00000000.00000000.11111111)
12


### Slides — strona 467

ACL Overview
ACL Order
Check Order
= ACEs (Access Control Entries), which represent the order of statements in the ACL, are
— | crucial and must be carefully planned. The router checks each packet’s parameters
‘i against the ACEs to find a matching condition. When a condition is met, the ACL will be
applied, and additional ACEs will be ignored.
Implicit Deny
At the end of every ACL, there is an invisible statement called implicit deny.
When no match is found for a packet, the implicit deny is applied to the packet.
Note: Each ACL must have at least one Permit statement!
13


### Slides — strona 468

CO
Access Control List
STANDARD ACL IMPLEMENTATION


### Slides — strona 469

Standard ACL Implementation
Standard ACL Placement
Where are Standard ACLs Placed?
Standard ACLs are placed as close to the destination as possible.
Cisco set this rule because placing standard ACLs at the source of
traffic will prevent communication with any network hosting
interfaces to which the ACL applies.
15


### Slides — strona 470

Standard ACL Implementation
Named Vs Numbered
Standard Named ACL
e
(2) — Standard Named Access Control Lists allow unique names to be assigned to ACLs.
Standard Numbered ACL
dee = (Standard Numbered Access Control Lists allow unique numbers to be assigned
2— to ACLs.
3m The Standard Numbered ACL range includes 1-99 and 1300-1999.
16


### Slides — strona 471

Command — ; :
1 H i H H
access-list i<access-list-number>} <deny | permit |remark> | <source-address> | <source-wildcard>|
1 t
1 ! 2 i 3 H 4 H 5 ! |
: </>
Command Example
1. Beginning syntax to configure a numbered ACL. R1(config)# access-list 10
. permit 192.168.10.0 0.0.0.255
2. Decimal number from 1 to 99, or 1300 to 1999 (only for Standard
ACLs).
3. Deny - denies access if the conditions match, Permit - permits access if
the conditions match, Remark - adds a remark about entries.
4. IP of the network or host from which the packets were sent. You can
specify any instead of using a 32-bit address.
5. 32-bit wildcard mask that will be applied on the source.
17


### Slides — strona 472

Standard ACL Implementation
Network Example
Scenario #1: ———s af
A network administrator decided that new Be | y——/ aE A SS
users on network 10.0.0.0/24 will not have —_, rt si Za) =
access to the server network, but will be | —_—= i —_
able to communicate with neighboring Host A Gigo/1 aay Gigo/2 Host B
network 192.168.0.0/24 192.168.0.10/24 eee 10.0.0,10/24
00/3 |
s 4
Scenario #2: 2
After malicious software was discovered
on Host A, an administrator decided to Papgten
temporarily block access from the Host to =, ==,
10.0.0.0/24, until the threat was removed. = | =
=a ——
The following slides include ACL DNS Server FIPS:
configuration examples based on 172.16.1.1/24 172.16.1.2/24
these scenarios.
18


### Slides — strona 473

R1(config)#access-list 1 deny 10.0.0.0 0.0.0.255
ACL configuration example based R1(config)#access-list a PIER any
Sn Scenatio #1. R1(config)# interface Gigabitethernet 0/3
R1(config-if)#ip access-group 1 out
Step 1 - Create a numbered ACL R1(config-if)#exit
using the command.
Step 2 - Choose the interface for
which the ACL will apply, using
the command.
Step 3 -
command links ACL 1 to the
Gigabitethernet 0/3 interface
in the outbound direction.


### Slides — strona 474

R1(config)# ip access-list standard
ACL configuration example based R1(config-std-nac1)#deny host 192.168.0.10
on scenario #2. R1(config-std-nac1)#permit any
R1(config-std-nac1)#exit
Step 1 - Use the R1(config)#interface Gigabitethernet 0/2
command to create R1(config-if)#ip access-group out
a named ACL. R1(config-if)#exit
Step 2 - In ACL configuration
mode, create Deny and
Permit ACE statements.
Step 3 - Apply the ACL on an
interface using the
command, and specify
the traffic direction (in or out).


### Slides — strona 475

R2#
Standard IP access list Block_Host_A
1@ deny host 192.168.0.10
ACL rules can be verified in 2 permit any
different ways, one of which is by Standardhpleccesclieted
searching the running-config file
using an include filter. 1@ deny 10.0.0.@ @.0.0.255
2@ permit any
Run to R1#
ee interfassegch interface GigabitEthernet0/2
ip address 10.0.0.15@ 255.255.255.080
ip access-group Block__Host_A out
The command !
can also be used. interface GigabitEthernet0/3
ip address 172.16.0.150 255.255.255.080
ip access-group 1 out


### Slides — strona 476

Extended ACL Implementation
; _ ET The objective of this lab is to plan, configure, and verify
Implement Standard and Extended ACLs ceandard and extended RCIE
(Tasks 4-6) .
—— f Ss ; : ® Configure a Numbered Extended ACL.
“= 8 » 4 .
‘ " : « ; ® Configure a Named Extended ACL
ws. 4 = (optional).
| = Rr - LA ® Modify an Extended ACL (optional).
- iY @ : 8 OS: All platforms ® Lab document
’ 8 Tools: Cisco Packet Tracer © NET-11-L1.pka
" y) 7.2.2, or higher
*
i % =~ 22


### Slides — strona 477

CO
Access Control List
EXTENDED ACL IMPLEMENTATION


### Slides — strona 478

Extended ACLs
What are Extended ACLs?
Extended ACLs filter packets based on the following attributes:
* Source and destination IP addresses.
= ¢ Source and destination Layer4 protocols (UDP and TCP).
a ¢ Protocol type or number. For example: IP, HTTPS, 80, etc.
— e Extended ACLs use the following range of numbers: 100 to 199
and 2000 to 2699.
&
24


### Slides — strona 479

Extended ACL Implementation
Extended ACL Placement
Where are Extended ACLs Placed?
Configure Extended ACLs as close as possible to the source of the
traffic being filtered.
Doing so ensures that traffic will be denied and prevented from
traversing the network infrastructure.
It’s important to understand that even if the ACL is not placed as close as possible to
the source, the ACL will still operate as it should.
25


### Slides — strona 480

Command ~ : : : ,
H I H I H
access-list i<number> 1<action>:<protocol>! <source-address><destination-address>} <operator>
| 1 H 2 H 3 H 4 ! 5 H 6 |
</>
Command Examples
1. Syntax used to configure a numbered ACL. R1(config)#access-list 101
2. Decimal numbers. Extended ACLs use 100-199 and 2000-2699. deny ip host 10.0.@.1 host
Ev Deny - denies access if the conditions match, Permit - permits access if the 172.16.0.2
conditions match, Remark - adds a remark about entries.
4. The name of the protocol being used: IP, TCP, UDP, ICMP, etc. R1(config)#access-list 101
5. The source and destination of the network traffic, which can be Host, or a deny tcp host 10.0.0.2 host
network 32-bit address. The any option can be used, and different 172.16.0.3 eq 22
combinations can also be used.
6. For logical port configuration, the following operators can be used for more
control: It (less than}, gt (greater than), eq (equal to), neq (not equal to),
and range (inclusive reel
26


### Slides — strona 481

Extended ACL Implementation
Network Example
Scenario #1: ——
Due to new procedures and changes in the | & |
organizational structure, Hosts A and C are it) 7 ———/ 7 ———/ (J
——- a R i =
not allowed to communicate. = a wi —=s=
5 Host B
HostA GigO/1 << Gigd/2 10.0.0.10/24
192,168.0.10/24 premade:
Scenario #2:
0/3 |
The network administrator decided that Goo =
the enterprise department on network =
10.0.0.0/24 cannot access the FTP service
on the FTP server, due to the risk of Host C
exposing sensitive information. It can =, 7, 10.0.0.20/24
however receive services from the same
server, such as DHCP. = =
— —
The following slides include ACL configuration DNS Server FIP Server
examples based on these scenarios. 172.16.1.1/24 172.16.1.2/24
27


### Slides — strona 482

R1(config)#access-list 100 deny ip host 192.168.0.10 host 10.0.0.20
; : R1(config)#access-list 100 permit ip any any
ACL configuration:examples R1(config)#interface gigabitEthernet @/1
based on scenario #1. ; . x
R1(config-if)#ip access-group 10@ in
R1(config-if)#exit
Step 1 - Create a numbered ACL
using the command.
Step 2 - Choose the interface for
which the ACL will apply, using
the command.
Step 3 -
command links ACL 1 to the
GigabitEthernet 0/1 interface
in the inbound direction.


### Slides — strona 483

R1(config)#ip access-list extended
ACL configuration examples R1(config-ext-nacl)#deny tcp 10.0.0.0 0.0.0.255 host 172.16.1.2 eq 21
based on scenario #2. R1(config-ext-nacl)#deny tcp 10.0.0.0 0.0.0.255 host 172.16.1.2 eq 20
R1(config-ext-nacl)#permit ip any any
Step 1 - Use the R1(config-ext-nacl)#exit
command to create a R1(config)#interface gigabitEthernet 0/2
named ACL. R1(config-if)#ip access-group in
R1(config-if)#exit
Step 2 - In ACL configuration
mode, create Deny and Permit
ACE statements.
Step 3 - Apply the ACL on an
interface using the
command and specify
the traffic direction (in or out).


### Slides — strona 484

R2#
Extended IP access list 100
ACL rules can be verified in various 10 deny ip host 192.168.0.1@ host 10.0.0.20
ways, ane of which Is by searching 2@ permit ip any any
ee using’2n Extended IP access list Block_FTP
. 18 deny tcp 10.0.0.0 @.0.0.255 host 172.16.1.2 eq 21
2@ deny tcp 10.0.0.0 @.0.0.255 host 172.16.1.2 eq 20
Run the 3@ permit ip any any
command can to display on which
interface each ACL is applied. Rit
interface GigabitEthernet@/1
The command ip address 192.168.0.150 255.255.255.0
can also be used. ip access-group 100 in
|
interface GigabitEthernet0/2
ip address 10.0.0.15@ 255.255.255.080
ip access-group Block_FTP in


### Slides — strona 485

d f 9 rd ; - * 5 y A ~ - ‘
g 1 ’ (fp ee .

# . ~<e "SEG fas f
i < ‘ hs, < : *, pd y
OS ~ a . > > SS
SS errs. \ <i -—~ ~ u
' SISOS \ ~~

Conk ; > ~~

' Cea SD 2 .——

ys \. y 7 . =

Tim By a . i

>. ye Cy fan. a ae


### Slides — strona 486

—— — “a : ™ Ty .
ie. = 4 a wet, NETWORK ga Cm D


# Chapter 12: Infrastructure Services


### Slides — strona 487

teens! ie ei nile
-___ Infrastructure Services
Computer Networking


### Slides — strona 488

Computer Networking
Introduction Network Switch & IOS Switch IP & Routing
to Networks Fundamentals Fundamentals Security Concepts
Diagnostics & Dynamic IPv4 & IPv6é Subnetting
Troubleshooting NLANs & Trdnis Routing Static Routing Concepts
Access Infrastructure Final Project
Control List Services inal rrojec
2


### Slides — strona 489

Infrastructure Services
Overview
Lesson Objective
DHCP Overview
The objective of this lesson is to become
familiar with infrastructure services, such DHCP Implementation
as NAT, and how they are configured.
In addition, this lesson covers how to RIN ROU Eee
configure and implement DHCP.
NAT Implementation
G
3


### Slides — strona 490

OO
Infrastructure Services
DHCP OVERVIEW


### Slides — strona 491

DHCP Purpose
Why Use DHCP?
To communicate with each other, all devices on a network must
have a unique IP address.
eo$0o
CI e Network administrators will often be responsible for assigning
e static IP addresses to network components, such as routers,

@ servers, firewalls, etc.

: ae C Assigning a static IP address for every endpoint in an organization
can be time consuming. Many endpoints do not require a static IP
address.

&
5


### Slides — strona 492

DHCP
The solution is to use Dynamic Host Configuration Protocol (DHCP).
DHCP was designed to manage IP address allocation automatically on
any network or device. It operates as a server with a range of IP
addresses that it allocates dynamically to devices on the network.
It also includes additional network information, such as the DNS
server address, default gateway address, and more.
Routers can also operate as DHCP servers.
2)
DHCP is defined in RFC 2131.
6


### Slides — strona 493

DHCP Overview
DHCP Characteristics
OSI Model Layer Logical Ports
DHCP operates in the DHCP operates on UDP DHCP supports both
application layer of the ports 67 (server) and 68 IPv4 (DHCPv4) and
OSI and TCP/IP models. (client). IPv6 (DHCPv6).
%


### Slides — strona 494

DHCP Overview

Dynamic Allocation Automatic Allocation Reservation Address
The DHCP server assigns As in the dynamic The network administrator
an available IP address to allocation method, the configures the DHCP
fhe client trom ifsaddress client receives a random server to allocate a

ool for a limited amount available IP address. But in specific IP address to a
poo! this case, there is no time selected client device.
of time. limit for the address. ;

. . The address is reserved for
This means that the client The client does not have a specific device in
“leases” the address from to renew the lease for the advance based on its MAC
the server for a period set address it was assigned. address.
by Ene eediritnistrater This method is useful for
At the end of the lease, devices such as network
the client requests an printers and others.
extension or a new
address.

8


### Slides — strona 495

DHCP Operation
How DHCP Works
The DHCP process includes four basic steps:
Discover, Offer, Request, and Acknowledgment (DORA).
{0}-*} The client device typically starts the process by contacting the server.
The information passing between the client and server is encapsulated in
| D> dedicated DHCP packets.
The DHCP server allocates the IP address and other information according
to the chosen allocation method (dynamic, automatic, etc.).
9


### Slides — strona 496

DHCP Overview
DHCP Process
DHCP Discover
A client device that requires an IP address
sends a discover message in broadcast to ii DHCP Offer
search for a DHCP server on the network. After the server receives the discover
message, it reserves an available IP address
and offers it to the client along with the
DHCP Request a lease details. H
The client responds to the offer with a
request to accept the offer or decline it. iin DHCP Acknowledgment
After receiving the request message, the
server sends the DHCPACK containing all
necessary configuration information.
10


### Slides — strona 497

DHCP Overview
DHCP Lease Renewal Process
DHCP Request
HELP| Before a lease expires, the client sends a DHCPREQUEST message directly to the
pd DHCPV4 server that originally offered the IPv4 address.
DHCP Acknowledgment
w Upon receiving the DHCPREQUEST message, the server verifies it and, if possible,
extends the lease information by returning a DHCPACK.
11


### Slides — strona 498

DHCP Overview
Router vs. Server
Router Server
Used in small and medium-sized businesses Used in larger networks and enterprises
Easy to manage Easy to manage
Requires knowledge of Cisco IOS and the Requires general knowledge of servers,
relevant configuration especially DHCP servers
Relatively low cost, as no device is required Relatively expensive, especially if the
other than the existing router organization needs to buy a dedicated server
to act as the DHCP server
one <
12


### Slides — strona 499

DHCP Overview
DHCPv6
DHCP for IPv6
Unlike IPv4, IPv6 uses multiple types of addresses from different
hosts. DHCPv6 was developed due to the usage in networks of
various address formats and prefixes instead of subnet masks.
DHCPv6 also supports more allocation methods than DHCPv4.
For example, an IPv6 host can automatically generate an IP address
internally using stateless address auto-configuration (SLAAC) or the
EUI-64 process for link-local addresses.
&
13


### Slides — strona 500

SLAAC
Tres In this method, the device can obtain an IPv6 global address without the services of a DHCP
server. The device uses ICMPv6 for advertisement messages to provide addressing and other
Y configuration information that would normally be provided by a DHCP server.
Stateless DHCPv6
The stateless DHCPv6 method informs the client to use the information in the router
== [=] advertisement (RA) message for addressing, while additional configuration parameters are
ca =] available from a DHCPVv6 server. The client will then communicate with a stateless DHCPv6
»— Le} server to obtain additional information not provided in the RA message, such as a DNS server
address. ao
Stateful DHCPv6
Like DHCPv4, addressing information and configuration need to be obtained from
EEE a DHCPvé6 server.
14


### Slides — strona 501

OO
Infrastructure Services
DHCP IMPLEMENTATION


### Slides — strona 502

Configiration btaps R1(config)#ip dhcp excluded-address 192.168.0.1

Stepdluexcludesaddresses fromthe R1(config)#ip dhcp excluded-address 192.168.0.100 192.168.0.150

DHCP pool. ' és

fe ' R1(config)#ip dhcp pool LAN1

i dean par canal eka R1(dhcp-config)#network 192.168.0.@ 255.255.255.0

gateway or statically configured R1(dhcp-config)#default-router 192.168.0.1

servers’ R1(dhcp-config)#dns-server 192.168.0.105
R1(dhcp-config)#domain-name Cyber.com

Step 2: Set up a DHCP pool of R1(dhcp-config)#lease @ 4 30

addresses using R1(dhcp-config)#exit

Step 3: Configure specific tasks, such

as the default gateway, DNS server,

domain name, etc.

Note: The /ease 0 4 30 (days, hours,

minutes) will not work in Packet

Tracer, but it does work on real Cisco

devices.


### Slides — strona 503

Ri#show ip dhcp pool
Several commands can be used to :
verify and troubleshoot DHCP Utilization mark (high/low) : 100 / @
settings: Subnet size (first/next) :@/20
: Displays pool

settings Pending event : none

: Displays the
client ist win le MaACiaddress, end 1 subnet is currently in the pool

C “Di Current index IP address range Leased/Excluded/Total

: Displays IP
conflicts detected during DHCP 192.168.0.1
negotiation


### Slides — strona 504

R1(config)#interface gigabitethernet 0/0
DHCP relay is a technique that #The IP of the DHCP Server.
allows devices to obtain addresses R1(config-if)#ip helper-address 10.0.0.250
from a DHCP server on a remote R1(config-if)#exit
network.
Note: Broadcast messages are not
transmitted to other networks.
When a client sends
DHCPDiscover, the router acts as a
relay and forwards the message
directly to the server in unicast.
Enable the
command and DHCP server
address on the interface that
receives the requests.


### Slides — strona 505

R1(config)#interface gigabitethernet 0/0

R1(config)#ip address dhcp
A router can also act as a DHCP client. R1(config)#exit
Its interface can be set manually or , r 7]
dynamically. : c+ ' ‘ = fee ;
Use the command on R1(config)#do show ip interface brief
the interface to enable dynamic Interface IP-Address OK? Method Status
allocation. Protocol

GigabitEthernete/e 209.168.201.12 YES DHCP up up
For example, an interface facing the GigabitEthernet@/1 unassigned YES unset administratively
ISP typically gets an IP from the ISP
DHCP server.


### Slides — strona 506

DHCP. Implementation
Lab NET-12-L1 Mission
2 eee The objective of this lab is to set up a DHCP service on a Cisco
eel eae | Ld GDU 4 router and make sure all devices on the network receive addresses
Configure DHCPv4 on a Cisco Router | dynamically. The lab also promotes understanding of the DHCP
30-60 Min. r relay concept.
— ¥ | re
“=e a - @ Answer the questions.
eh” p
. ’ ‘ ; ® Configure DHCPVv4 on R1.
=. Y “ ® Verify DHCP configuration.
(Wy ( LA @) @ Configure DHCP rel
| ' ’ , ® Configure relay.
amv 3 3
j
‘ s , 5 a , Envir TEEEICEIC ¢€ PVUVUIS IACSIGtCCU FT TGs
man ® ; 8 OS: All platforms » Lab document
: ® Tools: Cisco Packet Tracer ® NET-12-L1.pka
" \ Z 7.2.2 or higher
\ —
4 = 20


### Slides — strona 507

OO
Infrastructure Services
NAT OVERVIEW


### Slides — strona 508

NAT Overview
What Is NAT?
NAT Protocol
Network address translation (NAT) is an essential protocol and service
Eda that converts a private address to a public address and vice versa.
NAT is usually enabled on a firewall or router device at the edge of
RR. the local network and the beginning of the outside network.
Access to the internet from any home-based, corporate, or local
network is only possible through NAT.
&
22


### Slides — strona 509

NAT Overview
Why Use NAT?
NAT’s Usefulness
Although IPv4 is required for a device to communicate properly, the
number of available addresses is being depleted rapidly, and, at this
rate, a worldwide address shortage is imminent.
To save addresses and slow the depletion, private addresses were
| separated from public addresses.
Private addresses uniquely identify devices within a network, such as
a computer connected to an internal server.
Public addresses identify groups of computers outside of a local
network.
B
Private IP addresses are defined in RFC 1918.
23


### Slides — strona 510

NAT Overview
Private IP Space
According to RFC 1918, three address spaces are reserved for
devices in a private network (LAN). Their usage is unlimited,
and they can be freely implemented.
Private IP Range
IP Subnet
10.0.0.0—10.255.255.255/8 255.0.0.0
172.16.0.0-172.31.255.255/12 255.240.0.0
192.168.0.0-192.168.255.255/16 255.255.0.0
24


### Slides — strona 511

NAT Overview
NAT Operation
How NAT Works
The NAT process is transparent to users, and any evidence of its
operation is stored in a special table in the NAT-enabled device.
= ») This helps hide the internal network from the internet and adds
an extra layer of security.
— NAT operates in one of three methods: static, dynamic, or port
\N address translation (PAT).
Each method uses a specific address terminology to describe its
operation. =
Theoretically, the maximum number of private addresses
that can be translated into one public address is 65,536.
25


### Slides — strona 512

NAT Overview
NAT Advantages and Disadvantages
Advantages Disadvantages
Accessing internal resources requires special
Prevents IPv4 address depletion (PAT) configuration and makes troubleshooting more
challenging.
Reduces network performance and resource
Flexible network design and address scheme : availability. Difficult to troubleshoot issues
remotely.
Provides an additional layer of security Nal interferes with integrity checks because It
Pac modifies values in the headers. Pac
26


### Slides — strona 513

NAT Overview
Inside Local Outside Local Inside Global Outside Global
(00) at) Oo
The source IP address of the The IP address of the The public IP address used The IP address of the
local device in the private destination device as by the inside local device for destination device as
network viewed from the inside identification and access to viewed from the outside
For example: 10.0.0.5/24 local device (the the internet network (the NAT-
destination LAN) For example: The IP address enabled router)
For example: A remote on an interface facing a For example: A remote
web server WAN web server
27


### Slides — strona 514

NAT Overview

Step 1
A host on the local network sends a request to an gS
external destination (outside local), such as a web Step 2
server. The NAT-enable device receives the request and

changes the local device source address (inside
local) to the public IP configured on the WAN
Step 3 ——— interface (inside global).
[2]
The mapped address pair is saved in the device’s
NAT table and forwarded to the external destination ae Step 4
IP (outside global) on the internet.
The web server receives the request and replies
3
with a public source IP.

Step 5 ee
The NAT-enabled device receives the reply from the
web server and converts the public destination
address to the original private address (based on the
NAT table). The local host then receives the server’s
reply.

28


### Slides — strona 515

NAT Methods
Static NAT
One-to-One NAT
This is a permanent mapping of a single private IP to a specific single public address.
This method is not meant to conserve IPv4 addresses but to allow access to
internal resources from an outside network. yi
Dynamic NAT
+ Many-to-Many NAT
This method is also not meant to conserve addresses. Multiple IP addresses are
mapped dynamically by the router to a pool of public addresses. The conversion
is done on a first-come, first-served basis. a
NAT Overload Many-to-One NAT
=> NAT overload or port address translation (PAT) is the most common method and
is used to conserve addresses. In this method, multiple private IP addresses are
converted into a single public address. To distinguish the traffic from different
devices, the source port number is also used for the inside global address. @
29


### Slides — strona 516

What Is NAT64?
Network address translation IPv6 to IPv4 (NAT64) technology
C1 LE) facilitates communication between IPv6-only and IPv4-only hosts and
2S ee networks.
The solution allows enterprises and ISPs to accelerate IPv6 adoption
while simultaneously handling IPv4 address depletion.
&
30


### Slides — strona 517

OO
Infrastructure Services
NAT IMPLEMENTATION


### Slides — strona 518

NAT Implementation
NAT Topology
Network Example

The example on the right = |

illustrates the simple topology of a

a router connecting a small —

corporate network to the 10.0010 _ =

: p 10.0.0.1 |) — ren wih aque” s
R1

The next slide shows how each fie] Internet

NAT method is configured and —s

verified on R1. _—

4non20
32


### Slides — strona 519

#The interface facing the LAN.
The first step in configuring NAT is to Edge-R1(config)#interface gigabitEthernet 0/0
set the router's interfaces for the Edge-R1(config-if)#ip add 10.0.0.1 255.255.255.0
translation process. Edge-R1(config-if)#
Edge-R1(config-if)#no shutdown
The comma Edge-R1(config-if)#exit
tells the router which interfaces will
participate in the NAT process and #The interface facing the WAN.
their direction based on the network Edge-R1(config)#interface serial 0/0/0
topology. Edge-R1(config-if)#ip add 209.15.10.1 255.255.255.0
Edge-R1(config-if)#
Edge-R1(config-if)#no shutdown
Each interface connected to the Edge-R1(config-if)#exit
private network is defined as ,
and each interface connected to the
internet is defined as E


### Slides — strona 520

ip nat inside source static <local-ip> <global-ip>
In this example, a user wants to
connect to the internal server from +l Ff i) = :
somewhere on the internet. Edge-R1(config)#ip nat inside source static 10.0.0.10 209.15.10.1
The user cannot access the LAN 7 A
directly, so it sends the request to :
public router interface 209.15.10.1, ; wae " . .
and the router uses the NAT static map Edge-R1(config)# ip nat inside source static tcp 10.0.0.10 22
to forward the request to the 209.15.10.1 8080
10.0.0.10 server.
The second section in the example on
the right is for port forwarding. It
forwards only SSH traffic from outside
to the server.


### Slides — strona 521

Assume the ISP defined 10 public 1 ] E L ’ i

addresses on the WAN interface: Edge-Ri(config)#ip nat pool ToFreedom 209.15.10.1 209.15.10.10
netmask 255.255.255.0

Step 1: Create a public address pool Edge-R1(config)#access-list 1 permit 10.0.0.0 0.0.0.255

using Edge-R1(config)#ip nat inside source list 1 pool ToFreedom

Step 2: Configure standard ACL to

identify local addresses that need to

be translated using :

Step 3: Bind the ACL and the pool

using 5

Note: Using this method, the pool

should contain enough available

addresses: one for each device.


### Slides — strona 522

Edge-R1(config)#ip nat pool ToFreedom 209.15.10.1 209.15.10.10
netmask 255.255.255.0@
NAT overload or port address Edge-R1(config)#access-list 1 permit 10.0.0.0 0.0.0.255
translation (PAT) allows a router to . . oo .
use a single public address for Edge-R1(config)#ip nat inside source list 1 pool ToFreedom
multiple inside local addresses.
Methods 1 eadfigure PAT: Edge-R1(config)#access-list 1 permit 10.0.0.8 @.0.0.255
1. Use an address pool. Edge-R1(config)#ip nat inside source list 1
2. Use a single address
defined on the interface.
An important part of the command
is the option.


### Slides — strona 523

Edge-R1#show ip nat statistics
Two commands can be used to fully Total translations: 5 (1 static, 4 dynamic, 4 extended)
verify a NAT operation.
Hits: 5 Misses: 13
The command Expired translations: 1
displays NAT parameter and pool Dynamic mappings:
configuration, pool status, and -- Inside Source
interface configuration. access-list 1 pool ToFreedom refCount @
phe t ic, total add 1, allocated @ (0%), mi 8
command shows the active NAT ype generic, total addresses 1 , allocate (0%), misses
abated (inside local a i Edge-Ri#show ip nat translations
plobaladdress palting, when they Pro Inside global Inside local Outside local Outside global
occur). --- 209.15.10.1 10.0.0.10 --- ---
tcp 209.15.10.1:50016 10.0.0.10:50016 8.8.8.8:53 8.8.8.8:53
Note: Static NAT translation is always tcp 209.15.10.1:50017 10.0.0.10:50017 200.10.0.254:80 200.10.0.254:80
shown in the table. tcp 209.15.10.1:50018 10.0.0.20:50018 157.160.27.8:80 157.160.27.8:80
tcp 209.15.10.1:50019 10.0.0.20:50019 82.11.0.2:443 82.11.0.2:443


### Slides — strona 524

d f 9 rd ; - * 5 y A ~ - ‘
g 1 ’ (fp ee .

# . ~<e "SEG fas f
i < ‘ hs, < : *, pd y
OS ~ a . > > SS
SS errs. \ <i -—~ ~ u
' SISOS \ ~~

Conk ; > ~~

' Cea SD 2 .——

ys \. y 7 . =

Tim By a . i

>. ye Cy fan. a ae


### Slides — strona 525

aul egal 5 i 2B
—— — Sy " : ™ ty .
ie. = 4 a wet, NETWORK ga Cm D


---

# 03 — Lab Assignments & Solutions — wszystkie ćwiczenia i odpowiedzi

Źródło: `Computer Networking Zadania - Odpowiedzi.pdf` (266 stron). Zachowano cele, wymagania, zasoby, wszystkie kroki, pytania i odpowiedzi oznaczone w materiałach.


# NET-01-LS1 — Local Network Configuration

> Zakres źródłowy: strony 1–14.


### Lab Assignments & Solutions — strona 1

Computer Networking
Lab Assignment Introduction
& Solution to Networks
eo Vat NET-01-LS1
“alk F U | Local Network
Configuration
Copyright © 1996-2020 HackerU Ltd.
All Rights Reserved.


### Lab Assignments & Solutions — strona 2

Note: Solutions for the instructor appear in a green colored box.
G Lab Objective
Learn about and practice using CLI networking commands in Windows.
* Lab Mission
Configure a local network using CMD-based commands.
ea .
© Lab Duration
15-30 minutes
fe Requirements
e Familiarity with the Windows command line.
e Familiarity with the nslookup tool.
Lt

[ra] Resources
¢ Environment & Tools

Windows 7, 8, or 10

Internet connection


### Lab Assignments & Solutions — strona 3

Lab Task 1: Windows 10 Virtual Machine Installation
If you do not have a Windows 10 VM installed, set up a new machine.
You can follow the instructions in the Windows 10 Installation Guide located in the
Installation Guide module in your Canvas course.


### Lab Assignments & Solutions — strona 4

Lab Task 2: Local Network Configuration
In this task, you will use commands to view and document the local network
configuration of a Windows machine.
1 Open CMD on the local machine.

Press Win Key + R and type CMD.
2 Run the ipconfig command to display local PC network settings.

Type ipconfig and press Enter.

Connection-specific DNS Suffix . :

Ethernet adapter Bluetooth Network Connection:

3 According to the ipconfig command output, how many network cards are there?
Why do some PCs display information regarding more than one network card?
The ipconfig command displays information regarding all interfaces on the local
machine. For example, laptops usually have wired, wireless, and Bluetooth interfaces
installed.
4 Document the information in Notepad or a personal notebook.
Copy the details marked in red in Step 2 above.


### Lab Assignments & Solutions — strona 5

5 The command in Step 2 above does not show the physical and DNS address. Issue
the same command with the appropriate option to display the network settings in
more detail.

6 Which Help option displays all ipconfig option combinations and their purposes?

7 Which CMD command displays the physical address?

8 Run the cls command to clear the screen.

Page5


### Lab Assignments & Solutions — strona 6

Lab Task 3: Test Connectivity

In this task, we will verify connectivity to an internet based IP, and document

connection metrics such as latency and path.

1. Using the Ping command, verify connectivity between the local PC and another PC
in the same network (for example, the PC of an adjacent student or another device
on your network).

Ask another student for his/her IP address and ping it, or ping your default gateway.

2 Document the following details located in the ping statistics:

e Packets sent, received, and lost.
e Average round trip time.
Document only the details marked in red below.
C:\Windows \system32>ping 1@.21.6.3
Pinging 10.21.0.3 with 32 bytes of data:
Reply from 16.21.@.3: bytes=32 time-16ms TTL=128
Reply from 10.21.6.3: bytes=32 time=4ms TTL=128
Reply from 10.21.6.3: bytes=32 time=5ms TTL=128
Reply from 16.21.@.3: bytes=32 time=31ms TITL=128
\Approximate round trip times in milli-seconds:
Minimum = 4ms, Maximum = 31ms, Average = 12ms
i
3 Runtracert for the same target as in Step 1 above.
Run the tracert command for the IP address from Step 1 above.
C:\Windows\system32>tracert 10.21.6.3
Tracing route to 10.21.@.3 over a maximum of 3@ hops
2 4ms 4ms 7 ms 10.21.0.3
Trace complete.


### Lab Assignments & Solutions — strona 7

4 What is a Hop?
A router on the way to a packet's destination, from one network to another.
5 Document the number of hops.
C:\Windows \system32>tracert 168.21.6.3
Tracing route to 16.21.6.3 over a maximum of 38 hops
6 Use the ping command again to test connectivity to an external source (such as a
website or Google DNS public server, 8.8.8.8).
Ping an external source, such as a URL or public address (www.facebook.com, 8.8.8.8).
C: \Windows\system32>ping 8.8.8.8
Pinging 8.8.8.8 with 32 bytes of data:
Reply from 8.8.8.8: bytes=32 time=57ms TTL=55
Reply from 8.8.8.8: bytes=32 time=59ms TTL=55
Reply from 8.8.8.8: bytes=32 time=60ms TTL=55
Reply from 8.8.8.8: bytes=32 time=59ms TTL=55
Packets: Sent = 4, Received = 4, Lost = @ (0% loss),
Approximate round trip times in milli-seconds:
Minimum = 57ms, Maximum = 60ms, Average = 5S8ms


### Lab Assignments & Solutions — strona 8

7 Document the following details in the ping statistics:
e Packets sent, received, and lost.
e Average round trip time (latency as ms).
Document only the details marked in red below.
Reply from 8.8.8.8: bytes=32 time=S9ms TTL=55
Ping statistics for 8.8.8.8:
iWpproximate round trip times in milli-seconds:
Minimum S7ms, Maximum 6@ms, Average 5Bms
8 Run tracert for the same target as in Step 7 above.
Run tracert for the IP address in Step 7.
9 Document the number of hops.
1 6 ms 5 ms 8 ms 10.21.8.100
2 S ms 4 ms 38 ms b2q-252-97 .red.bezeqint.net [212.179.252.97]
3 6G ms 6 ms 6 ms bzq-179-16-121.cust.bezegint.net [212.179.16.121]
6 60 ms 6@ m 59 ms 108.170.252.65
i 62 ms 62 ms 62 ms 216.239.56.149


### Lab Assignments & Solutions — strona 9

10 Compare the findings. Why are the round-trip times and hop count results in
Steps 1-4 less than those in Steps 7-10?
The adjacent student's PC is in the same network, so no router is needed. The external
source is in a different network, which means the packet must be forwarded through
several routers.


### Lab Assignments & Solutions — strona 10

Lab Task 4: Domain Names and IPs
In this task, you will demonstrate knowledge of the nslookup command, document
your machine’s DNS servers, and find IP addresses of URLs.
1 Using the nslookup command, discover which DNS server is configured on the local
machine.
Type nslookup to enter resolve mode.
C:\Windows \system32>ns lookup
2 Using nslookup, what is the public IP address of www.cisco.com?
Default Server: dns.google
Addresses: 2a02:26f0:c00:584: :b33
www. cisco. com.akadns .net
wewds .cisco.com.edgekey net


### Lab Assignments & Solutions — strona 11

3 ADNS record can also work in reverse order. Which service or organization uses IP
address 185.60.216.35?
> 185.66.216.35
Server: dns.google
Name: edge-star-mini-shv-@1-frx5,. facebook. com
Address: 185.60.216.35
4 Press Ctrl+c to exit nslookup mode, or type exit, and close CMD.


### Lab Assignments & Solutions — strona 12

Lab Task 5: Domain CLI Vs GUI
In this task, you will configure your network interface using only the CLI.
There are two universal ways to communicate with a PC: via graphic interface (GUI), or
via a Command Line Interface (CLI).
The netsh command is run via the CLI, and is used to configure all network settings.
1 Open CMD as administrator.
Search for cmd, and right-click “Run as Administrator”.
w
=F
o Ea ~
& PD emder —
® ed commands
P mdb
P emda vs
2 amd
2 and nyse 1
==
a
o Ee 2D Web
«a Eo = @ a =
2 Display the local PC network configuration using netsh interface ip show config .
Command: netsh interface ip show config
Note: Interface names may be different.


### Lab Assignments & Solutions — strona 13

3 Configure the following addresses statically on the wired or wireless interface:
e |Pv4 192.168.0.5
e Subnet Mask: 255.255.255.0
e Default Gateway: 192.168.0.1
Use the following command:
netsh interface ip set address "Ethernet" static 192.168.10.5 255.255.255.0
192.168.0.1
Run:
netsh interface ip set address "Ethernet" static 192.168.10.5 255.255.255.0
192.168.0.1
Make sure to substitute “Local Area Connection*1” with the name of your interface (for
example “Ethernet”).
4 Use the command in Step 2 above to verify the new configuration.
Run: netsh interface ip show config
5 Which network protocol is responsible for allocating IP addresses and network
configurations dynamically to devices on the network?
DHCP
6 Revert the changes by enabling DHCP on the interface with the command:
netsh interface ip set address "Ethernet" dhcp
Run: netsh interface ip set address "Ethernet" dhcp
7 Disable the interface, with the following command:
netsh interface set interface "Ethernet" admin=DISABLED
Run: netsh interface set interface "Ethernet" admin=DISABLED
8 Enable the interface, with the following command:
netsh interface set interface "Ethernet" admin=ENABLE
Run: netsh interface set interface "Ethernet" admin=ENABLE


### Lab Assignments & Solutions — strona 14

9 Ping 8.8.8.8 to verify connectivity.
Run: Ping 8.8.8.8
Verify that the command was successful.


# NET-02-LS1 — Network Examination with Wireshark

> Zakres źródłowy: strony 15–33.


### Lab Assignments & Solutions — strona 15

Computer Networking
Lab Assignment Network
& Solution Fundamentals
ROLL) NET-02-LS1
ol TU Network Examination

with Wireshark
Copyright © 1996-2020 HackerU Ltd.
All Rights Reserved.


### Lab Assignments & Solutions — strona 16

Note: Solutions for the instructor are shown inside the green box.
G Lab Objective
The objective of this lab is to learn how to use Wireshark and how computers
encapsulate and send data.
%) Lab Mission
The mission of this lab is to capture various types of network traffic, and analyze the
data.
x) .
© Lab Duration
30-60 minutes
fe Requirements
¢ Knowledge of the TCP/IP model and data encapsulation.
e Knowledge of basic Wireshark filters.
oo

| Resources
¢ Environment & Tools

o Windows 10 VM

o Web browser

o Internet connection
e Extra Lab Files

o Wireshark-win64-4.0.5.exe


### Lab Assignments & Solutions — strona 17

Lab Task 1: OSI & TCP/IP
This task will review OSI & TCP/IP information previously learned.
1. What is the primary role of the Transport Layer and which are the two most
common corresponding protocols?
The transport layer handles the coordination of data transfer between two network
hosts: TCP and UDP.
2 Inwhich layer of the OSI model do protocols like DNS, HTTP, and SSH operate?
Application Layer (7).
3 Inwhich layer of OSI and TCP/IP models are source and destination logical
addresses added to the packet?
OSI - Network Layer (3), TCP/IP - Internet Layer (3).
4 Inwhich layer of OSI and TCP/IP are source and destination physical addresses
added to the frame?
OSI - Data Link Layer (2), TCP/IP - Network Access (1).
5 What does UDP do with corrupted or out-of-order packets?
Nothing, the destination discards corrupted packets.


### Lab Assignments & Solutions — strona 18

Lab Task 2:Wireshark Installation
In this task, we will install Wireshark.
1 Before you start, make sure your Windows 10 virtual machine’s NIC is configured
to NAT.
| Be cena | notwork
Bl sien sists Adele 2 stot ade +
Eh opty leient scone -
Dae | ue
EP woe |
Dus
[GBD stared Foes
a eK | Cane
2 Use the provided Wireshark installation file to install the software. Double-click
the file to start the installation.
3 Ifa message regarding “User Account Control” appears, click “Yes”.
) Do you want to allow this app to make changes to
© your PC?
4 Program name: — Wireshark installer for 64-bit Windows
Verified publisher: Wireshark Foundation, Inc.
File origin: Hard drive on this computer
Oshow dts
crete ee


### Lab Assignments & Solutions — strona 19

4 Click Next in the first setup page to begin.
A Wisharkacs Ob Setup = X
Welcome to Wireshark 4.0.5 64-bit
3 §) Setup
Th ward wl ude you auch the tation oF
Weer
Before staring theinstalatn, mate sure Wireshark rot
ick Non conve,
Cones!
5 Inthe next page, click “Noted”, for the license agreement.
A Wireinaican seat seup = 3
License Agreement
Place rev the ers ters before isang Wireshark 40.56¢bi r§
\reshrkis debuted under the GWU Genel ub Lense
1 UCHR BUCHER i
Veson 2 re 1951
Cerro (2 185, 1961 Fe Softnare Feud: ne
Franken Sree, Fh oer, cote, HA 21:0-1302USA
Everyone permed te coy and aavbute vebaim copes
of ts heros doument bot chang nt eon
Preantle
ucla formoet eft ar dic to take may yur :
This is not an end user license agreement (EULA). Its provided here for informational
Beeeesty
<a Core!
Page5


### Lab Assignments & Solutions — strona 20

6 Inthe next page, make sure all the components are selected, and click “Next”.
A Wireshark 4.05 64-bit Setup = x
‘choose Components
Croose whch features of iresha 4.0.9844Ht you nantto sta A
Tie lowes evant a availa frre
Sed meer
(A Tshark
1-7] Plugins & Extensions
BM Tools
Documentation
Description
scerequret:2510M8 — Foston your
aE aa
7 Inthe next page, make sure all the options are selected, and click “Next”.
Ai Wireshark 4.0.5 64-bit Setup = x
Adational Tasks
Create shorteuts and asscat le extensons A
cane
iveeshar str Men tem
atest Det con
Eaivresark uk eunch eon
festa Fae Eero
lassociate trace file extensions with Wireshark
mplog, ntar, out, pap, pcapne, pkig, pkt, rf5, snoop, syc, the, tr1, trace,
Teneo we a
aE Cone


### Lab Assignments & Solutions — strona 21

8 Inthe next page, select the installation destination folder, and click “Next”.
(@ Wireshark 4.05 64-bit Setup = x
Choose Install Location
Chooze the flier n hich to natal Weeshark 40.5 6b 4
Goose a drecoryin which total Wweshark
Destnaton Folder
space reared 231.08
ce aval: 18.368
etack ]
9 Inthe next page, make sure “Install Npcap 1.71” is selected, and click “Next”.
(Wireshark 4.05 64-bit Setup = x
Packet Capture
esha requres cher Npcap or WnPcap to capture ne meter data A
urrentyinstaled Np or WinPcap version
sted
Est cep 1.71
(Use Ade Renove Programs rt unnstal any undetected ol Nose o WP
portant nice
(i eee ee ee
'etstop nap a Amntator bere wpgradng Npcop 20 att oss cash epan
cet vmecp
Lear nore bout pcan and Wrap
ese) ea


### Lab Assignments & Solutions — strona 22

10 Inthe next page, click “Install” without changing anything.
The installation will begin.
A Wirernarcd 05 6abtSctop = x
‘USB Capture
Sm rae cape SE rae. na Pe aes rs
Current installed USiPczp version
tel
(Ditnstall usePcap 1.5.40
(Use Adc/Remove Programs first to uninstall any undetected old USEPcap versions)
eer oe
feral
Ite ths comfieconfcbeapesue/S
corer cee
az Za
11. When the installation process ends, click “I Agree” for the Npcap setup license
agreement.
@ Necop 171 Seup = x
license Agreement
memeecis eee
ck Riad TARA RBEE ‘i
hecan ins nacan.on) i Wins pate sifina iver and
library ard is copyright (c) 2013-2022 by Nmap Sofbvare LLC (“The Nmap
[Project’). Allrights reserved.
ren touch oxen source code's pub avaiable for review itis
fotapenseucesftere arday fot e eastbutedr sed ether
ferinerewioat specs permason Fon tie Nap Projet. The
tncrd (res) vrcon sual ned te stlaten ov fhe <
(ieee i eres Srey y
mrosatinsal ep U7
Core!


### Lab Assignments & Solutions — strona 23

12 Inthe next page, leave all the options unselected and click “Install”.
(G@ Npcap 1.71 Setup - x
Installation Options
af eA Foose reve te loving cotonsbefeeintalina Neca 1.71
Ciecinearives ace e Aneeteercan
Tpsepertran sc2.11 ac and monitor mode) for weless aanters
[1 Jrstall Npcap in Win?cap API-compattible Mode
ack corel
13 When the installation ends, click “Next”, and in the next window, click “Finish”.
The Wireshark installation process will continue.
G@ Nocap 1.71 Setup, ee
Instalition Compete
= Setup nas completed succesful
Conpleted
EEE
Show deta
@ Npcap 1.71 Setup a
Finished
J Thank you frinstingHocap
Te ee erate ree ene
krish to dese is ier


### Lab Assignments & Solutions — strona 24

14 When the installation ends, click “Next”, and in the next window, click “Finish”
without selecting “Show News”.
A Wireshark 4.05 64-bit Setup =
Irstallesion Complete
Setup was convicted succor 4
‘Completed
aaa SESS
Extract wenloize pedis ona A
bat secon ey
exvact tay astong
Seek monavien
extract omeranal.ona
Extract omoutong
Output fodder: C:\Program Files|Wireshark\Wireshark User's Guide
cut fer: C: Progam Flesiesharc
ext fa.nd
competed e
=)
Al Wireshark 4.05 62-bit Setup =
Completing Wireshark 4.0.5 64-bit
eam
\ireshark 40,564bithasbeen nstaledon your comute,
chris dose Setup
Cstow News
Te a


### Lab Assignments & Solutions — strona 25

Lab Task 3: Use Wireshark to Examine Live Network Traffic
In this task, we will install Wireshark and become familiar with the interface.
Part 1 — Learn about the Wireshark Dashboard
1 Choose the network adapter in use, and who you want to view data on.
The graph shows which interface is active.
(The Wireshark Network Analyzer - og x
Ae SO URREQ oo eT IBBaaan
Bexesson.. + |
Capture
using this filter: Wlenter a capture fiter ~) Allinterfaces shown ¥
(ethane Wl
Bluetooth Network Connection
EthernetO rw
Note: The answers in this section were taken from a lab environment.
Since you are working in a different network environment, some of the answers may be
different.
2 Dashboard View:
a) The top screen or bar contains the program’s tools, such as preferences,
settings, and the search bar.
ag26 1 i Qe
W/Apply a display filter... <Ctr-/> |
b) The windows in the middle show the live network traffic on the network card
(adapter). Data is presented as frames.
c) The screen at the bottom displays information for a selected frame.


### Lab Assignments & Solutions — strona 26

Part 2 — Examine Live Network Traffic
3 Start capturing the network by clicking the Wireshark icon a
4 Opena web browser (recommended: Edge or Firefox).
5 Browse to http://juice-shop.herokuapp.com/#/ and immediately after the web
.
page is loaded, click the stop button .
6 Take acloser look at a client requesting a web page from a server.
Use the search bar to display only the HTTP packets.
sauce RO VeeBreT aaa
(=o RE
me ore = re 7
1. 4.801384 10.0.2.15 13.226,6.34 HTTP 383 GET //MEOWSDBGMEQuQjAJBUrDgMCGgUABBSLWZ6EWSgdYc9UaSEaal j jE.
1. 4.807717 13.226.6.34 _10.0.2.15 _OCSP_338 Response
be
Ju 305.849... 10.0.2.15 52.16.192.249 HTTP 403 GET /styles.css HTTP/1.1
7. 305.849.. 10.0.2.15 52.16.192.249 HTTP 430 GET /runtime-es2015.js HTTP/1.1
> Frame 749: 385 bytes on wire (3080 bits), 385 bytes captured (3080 bits) on interface \Device\NPF_{872B33F-4678 ~
» Ethernet II, Src: PcsCompu_ic:ba:@c (08:00:27:1c:ba:@c), Dst: RealtekU_12:35:00 (52:54:00:12:35:00)
» Internet Protocol Version 4, Src: 10.0.2.15, Dst: 52.16.192.249
» Transmission Control Protocol, Src Port: 49687, Dst Port: 80, Seq: 1, Ack: 1, Len: 331
e030 ff ff 02 7e G0 G0 47 45 54 20 2f 20 48 54 54 50 GE T / HTTP fal
0042 2# 31 2e 31 @d @a 41 63 63 65 70 74 3a 20 74.65 /1.1--Ac cept: te
0050 78 74 2 68 74 6d 6c 2c 20 61 70 70 6c 69 63 61 xt/html, applica
060 74 69 6F 6e 2F 78 68 74 Gd 6c 2b 78 6d 6c 2c 28 tion/xht ml+xml,
0070 69 6d 61 67 65 2f 6a 78 72 2c 26 2a 2F 2a Gd Ga = image/jx r, */*+-


### Lab Assignments & Solutions — strona 27

7 Click the GET HTTP packet sent from the local PC to the server.

(i Copturing rom Ethemet 2

File Edit View Go Capture Analyze Statistics Telephony Wireless Tools Help

AMA CO 1M ROCeeoeeezBaaar

Time source Destination Protcch Length info
154 0.375544 93.184.220.29 10.0.2.15 ocsP” 853 Response
166 0.447538 192.124.249.31 10.0.2.15 PKIX-.. 1068 Certificate Revocation Li:
235 0.608679, 10,0.2.15 (192.124. 249.23 HTTP 274 GET //MEKWRZBFMEMWwQTAIBgUI

| 266 0.718556 192.124.249.23_10.0.2.15 OcsP 956 Response
296 0.807185 52.16.211.175 (10.0.2.15 HTTP 45@ HTTP/1.1 304 Not Modified
303 0.810648 10.0.2.15 52.16.211.175 HTTP 529 GET /styles.css HTTP/1.1

| 3e4 0.810929 10.@.2.15 52.16.211.175 HTTP 554 GET /runtime-es2015.js
‘Accept: text/html, application/xhtml+xml, image/jxr, */*\r\n
Accept-Language: en-US\r\n
User-Agent: Mozilla/5.@ (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko)|
Accept-Encoding: gzip, deflate\r\n
Host: juice-shop.herokuapp.com\r\n
If-Modified-Since: Tue, 21 Jul 2@2@ 26:01:20 GMT\r\n
If-None-Match: W/"785-17372f75b4a"\r\n
Connection: Keep-Alive\r\n

> Cookie: cookieconsent status=dismiss\r\n
\r\n
Full request URI: http://juice-shop.herokuapp.com/
<


### Lab Assignments & Solutions — strona 28

8 Click each header to view the encapsulated date (logical ports, IP, and MAC
address).
(Gi Capturing from Ethernet 2
Fle Edt View Go Capture Anahze— Statics Telephony Wireless Tools Help
mao RB OiQenseeseBacel
(eo
i ES Destnaton Protech Length no
154 0.375544 93.184.220.29 —10.0.2.35 ocsp 853 Response
166 0.447538 192.124. 249.31, 10.0.2.15 PKIX-.. 106@ Certificate Revocation List
(235 0.608679 10.0.2.15 192.124,249.23, HTTP” 274 GET //MEkwRZBFMEMwQTAIBgUrDgMCGe
| 266 0.718556 192.124.249.23 10.0.2.15 ocsP 956 Response
pe 278 0.724957 «10.0.2.15 52.16.211.175 HTTP 509 GET / HTTP/1.1
(296 0.807185 $2.16.211.175 10.0.2.15 HTTP 45@ HTTP/1.1 3@4 Not Modified
+ 303 0.810648 10.0.2.15 52.16.211.175 HTTP. 529 GET /styles.css HTTP/1.1
| 304 0.810929 10.0.2.15 52.16.211.175 HTTP 554 GET /runtime-es2015.js HTTP/1.1
Frame 278: 5@9 bytes on wire (4972 bits), 509 bytes captured (4072 bits) on interface \Device\NPF_{87
Ethernet II, Src: |PcsCompu_ic:ba:@c (@8:00:27:1c:ba:@c), Dst: RealtekU_12:35:8@ (52:54:00:12:35:00)|
Internet Protocol Version 4, Sre: 10.0.2.15, Dst: 52.16.231,175
\ Transmission Control Protocol, Sre Port: 49930, Dst Port: 80, Seq: 1, Ack: 1, Len: 455
Destination Port: 80
[Stream index: 34]
[TCP Segment Len: 455]
Sequence number: 1 (relative sequence number)
Sequence number (raw): 3952001607
[Next sequence number: 456 (relative sequence number)]
Acknowledgment number: 1 (relative ack number)
Acknowledgment number (raw): 1212293
<
9 Document the following details:
a) What are the logical port source and destination?
b) What are the logical source and destination addresses?
c) What are the physical source and destination addresses?
{coloring fute none: x17] A
Coloring tule string: Rete || tep.port =» a9 [| http
nee Te Srer PRC Te De Be SA ROTTS BOTOC) DHE RICO AE GETS GH SU OOD STOR)
frcernet Protacol Version &, sect 10:0.2-18, Dstt $2-26-211.475
SS |
Source Pore aE
Destination Port: 88
{streen indore 54]
{reo seanene Len: #55]
Sequence rumver (raw) 3952003607
[het sequence number: 458, (relative sequence ninber)]
Acknowledge munber: 1. (relative ack unber) :
Protocol Layer 4: TCP
Source Port: 49930 (usually selected randomly from the dynamic port range).
Destination Port: 80 (used by HTTP for web page transfer).
Flag: We can understand by observing the flags that this is the first packet of the TCP
3-way handshake process.


### Lab Assignments & Solutions — strona 29

.
Se tare
® iat = Header Length: 20 bytes (5)
Divrerenciatee services Field: ere0 (O5CP: C$6, ECN: NOE-ECT)
Total Length: 495
Teentification: exscS0 (23652)
Foes: extese, Don's frageent
Frogeent offsets 8
Tine to Liver 128
protocet: Top (6)
Neder checksum: 0080 [validation disabled]
Destination $2.16.2.375 :
Layer 3 protocol: IPv4
Source address: 10.0.2.15 (local machine)
Destination address: 52.16.211.175 (Juice shop hosting server)
{coloring tute tone: HTTP] 5
[eatoring fue strings neep | tep.pore on 66 || netoa
Tihernct Ty Srer PevComputetbaTee (au @O-a7 acrbarec)s OE) Rest ATAETGO (GTiBe GOTT)
Devtination: Realeet 17:35:00 (52°56:60:12:35:20)
Scurces PesCompu te:ba:8c_(65;00;27:1c:ba:6c)
en area (cores)
neernet erotocel Verso S#4! 10:0.2:5, ose! 52.26.212.175
> Hataassen cover seetosau cieiescee cael bar pees! oe] Gags Vneuslarlion aay
Source Pores 19930
Destination Port: 86
{steeen incers 34)
{ter segnent ten: 455]
Sequence murber (ras): 3952661667 S
Layer 2 protocol: Ethernet
Source address: 08:00:27:1c:ba:0c (local machine)
Destination address: 52:54:00:12:35:00
chernet Ht, Srcr Reolteni 12 35100 (GUS4r00 12:35:00), Oskr PesCompu_Terber8e (WBr@8:27 Ter¥ar80) 5
internet protocol Version 8, sre: $2-16:211375, ost 10.0.2.5
Hransnission control Pratoeeh, sre Ports 89, ost Port: 49930, seq: ty Aki 456, Len: 396
Servers Comoy\r\n
Content-Length: @\r\n
Access Control-Allow Origin: "rn
xcontent-Type-options: nosniff\rvn
rteane options: SSHEORZeDV\P\n
Feature-Policy: paynent"se1®"\r\0
secept-Ronges? bytes\rin
Cecne-Conerot: pubtic, nax-agee8\rin
Castedified: Twe, 21 dul 2620 20:61:20 GHT\r\n
fogs w/"785-17572¢7504a"\r\n
Date: ed, 22 201 2020 69:17°32 GHT\r\n
Vier 1-1 vegurvrin
\rn
Sane aT 0,082228000 seconds)
eauest in fran 278 l
Response packet: Note that the source and destination addresses switched places.


### Lab Assignments & Solutions — strona 30

Lab Task 4: Capture Network Traffic to a File and Analyze it
In this task, we will capture packet data and save it to our disk. We will then open the
saved file and look for specific data using filters.
1 Click the Wireshark icon @ to start capturing.
2 Open the CMD and send a ping to 8.8.8.8
EM Administrator; C\Windows\system32\cmd.exe aa oOo »*
Microsoft Windows [Version 16.0.18362.720] A
(c) 2019 Microsoft Corporation. All rights reserved.
Pinging 8.8.8.8 with 32 bytes of data:
Reply from 8.8.8.8: bytes=32 time=30ms TTL=53
Reply from &.8.8.8: bytes=32 time=26ms TTL=53
Reply from 8.8.8.8: bytes=32 time=24ms TTL=53
Reply from 8.8.8.8: bytes=32 time=23ms TTL=53
Ping statistics for 8.8.8.8:
Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),
Approximate round trip times in milli-seconds:
Minimum = 23ms, Maximum = 3@ms, Average = 25ms
C:\Users\User>
w
3 Browse to http://hack-yourself-first.com/
4 Stop capturing using the stop button M@.


### Lab Assignments & Solutions — strona 31

5 Click File and then Save as. Name the file capture1 and save it in the Desktop
folder.
rere
ACO UBRE CeseFiaeeaaaa
—— EE SS
Md Wireshark . Save Capture File As x
Savein: | TE Desktoo -] @& & Br
ao . Date mecified pe 18.211.118.21
No iterns match your search. 192.168.6.36
Seatiad 192.168.6.36
Bw 18.211.118.21
Desktop 192.168.6.40
i 192.168.6.36
192.168.6.40
bs 192.168.6.31
& 192.168.6.36
This PC 192.168.6.31
52.200.65.196
@ 192.168.6.36
meee be > 52.200.65.196
Flenane sae pee
Seveestwme: | Yeshak.-peaona (nr a ma“Doapnt Cancel EG ae
52.20.0.32
te
Ci compress wth gz —x— SSS
> rrame 4: 13% vytes on wire (irs ures), 198 vyLes Captured (1104 bits) on int
Ethernet IL, Src: IntelCor_@c:8e:e2 (38:08:25:0c:8e:e2), Dst: Netgear_1b:b7:8
Internet Protocol Version 4, Src: 192.168.6.36, Dst: 204.79.197.200
Transmission Control Protocol, Src Port: 50143, Dst Port: 443, Seq: 1, Ack: 1
Transport Layer Security
6 Close Wireshark.
7 Double-click capture1.pcap to open the file.
8 Using the appropriate display filter, display only the DNS packets.
Note: if you fail to find the query, flush the DNS cache with the command
ipconfig /flushdns and repeat steps 3-8.
a AME vr)
i oy eee, Pewee a
2.234844 10.6.2.15 8.8.8.8 DNS 72 Standard query @x@dc9 A www.bing.com
3.6,311586 8.8.8.8 10,0.2.15 DNS 193 Standard query response @x@dc9 A www.bing.com CNAME a-@@01.a-afden...
59 1.202924 10.€.2.15 162.159.27.72 DNS 139 Dynamic update @xilbd SOA Cyber.com CNAME AAAA A A 10,0.2.15
60 1.259667 _162.159.27.72_10.0.2.15 DNS __69 Unknown operation (8) response @x1ibd Not implemented SOA Cyber.com
+3.. 29.178947 8.8.8.8 10.0.2.15 DNS 157 Standard query response @xSa3e No such name A hack-yourself-fiurst..
3.. 36.128947 10.6.2.15 8.8.8.8 DNS 83 Standard query @xd68c A hack-yourself-first.com
3.. 36.220372 8.8.8.8 10.0.2.15 DNS 99 Standard query response @xd68c A hack-yourself-first.com A 104.42...
3.. 36.769431 10.6.2.15 8.8.8.8 DNS 77 Standard query 9x99de A urs.microsoft.com


### Lab Assignments & Solutions — strona 32

COMMANDO 22/67/2026 13:45:26.38
IC: \Windows\system32+ipconfig /flushdns
Windows IP Configuration
successfully flushed the DNS Resolver Cache.
9 Document the following details:
a) Which Layer 4 protocol is used to encapsulate the Layer 4 header.
b) What are the source and destination logical ports?
c) What is the default DNS server configured on your machine, according to the
Layer 3 header?
Frame 729: 84 bytes on wire (672 bits), 84 bytes captured (672 bits) on interface \Device\NPF_{87C2
Ethernet II, Src: PcsCompu_1c:ba:@c (@8:0@:27:1c:ba:@c), Dst: RealtekU_12:35:0@ (52:54:00:12:35:00)
Internet Protocol Version 4, Src: 10.@.2.15, Dst: 8.8.8.8
~[ser-Datagran Protocol, Src Port: i464, Dst Port: 53]
Source Port: 61464
Destination Port: 53
Length: 50
Checksum: @x1c62 [unverified]
[Checksum Status: Unverified]
[Stream index: 13]
[Timestamps]
Layer 4 protocol: UDP
Source port: 61464
Destination port: 53
10 Which filter will display all packets sent to port 53?
sec OT DRG QewBF2SSQaae |
2 ©.234844 10.0.2.15 8.8.8.8 ONS 72 Standard query @x@dc9 A www.bing.com
59 1.202924 10.0.2.15 162.159.27.72 DNS 139 Dynamic update @x11bd SOA Cyber.com CNAME AAAA A
2.. 29,109166 10.0.2.15 8.8.8.8 DNS 84 Standard query @xSa3e A hack-yourself-fiurst.com
3.. 36.128947 10.0.2.15 8.8.8.8 DNS 83 Standard query oxd68c A hack-yourself-first.com
3... 36.769431 10.0.2.15 8.8.8.8 DNS 77 Standard query @x99de A urs.microsoft.com
[+ Tm 37.410783 10.@.2.15 8.8.8.8 DNS 84 Standard query @x5d2a A www.google-analytics.com |


### Lab Assignments & Solutions — strona 33

11 Using the appropriate display filter, display only the Ping packets.
i
No. Time ‘Source Destination Protocol Length Info
84 8.714769 10.0.2.15 8.8.8.8 ICMP 74 Echo (ping) request
85 8.783218 8.8.8.8 10.0.2.15 ICMP 74 Echo (ping) reply
87 9.734447 10.0.2.15 8.8.8.8 ICMP 74 Echo (ping) request
88 9.802806 8.8.8.8 10.0.2.15 ICMP 74 Echo (ping) reply
89 10.749410 10.0.2.15 8.8.8.8 ICMP 74 Echo (ping) request
12 Document the following details:
a) How many requests and replays are shown?
b) Why doesn’t ICMP have a logical port number listed in the packet capture?
Request Packets: 4
Replay Packets: 4
ICMP is a Layer 3 protocol, meaning it does not have a logical port. To verify this, you
can view the header of the packet, and note that there is no Layer 4 header.
13. Which filter will display all packets sent to the 8.8.8.8 host?
[| ipdst--8.8.8.8
No. Tine source Destination Protocol
12 @.1655@9 10.0.2.15 Suerers DNS
35 0.249834 10.0.2.15 8.8.8.8 DNS
82 8.313399 10.0.2.15 8.8.8.8 DNS
— 848.714769 10.0.2.15 8.8.8.8 CMP
87 9.734447 10.0.2.15 8.8.8.8 ICMP


# NET-03-LS1 — Packet Tracer Installation

> Zakres źródłowy: strony 34–46.


### Lab Assignments & Solutions — strona 34

Computer Networking
Lab Assignment Switch & IOS
& Solution Fundamentals
. ai NET-03-LS1
a U Packet Tracer Installation


### Lab Assignments & Solutions — strona 35

Computer Networking
Lab Assignment Switch & IOS
& Solution Fundamentals
. ai NET-03-LS1
a U Packet Tracer Installation


### Lab Assignments & Solutions — strona 36

Note: Solutions for the instructor are shown inside the green box.
*@) Lab Objective
Become familiar with Cisco Packet Tracer software.
4) Lab Mission
Create a Cisco account and download Packet Tracer to explore the features it
provides.
CN) *
@) Lab Duration
30-60 minutes
{@ Requirements
e@ Working knowledge of browsers
Lt}

| Resources
e Environment and tools

o Web browser
e External links

o Cisco registration:

id.cisco.com/signin/register
o Networking Academy registration/Packet Tracer download:
netacad.com/courses/packet-tracer/introduction-packet-tracer


### Lab Assignments & Solutions — strona 37

Lab Task 1: Cisco Account Registration
In this task, you will create a Cisco account to download the Packet Tracer
application.
1 Using a browser, navigate to the Cisco registration link provided in the
resources section above.
& > CB hitps://id.cisco.com/signin/register
2 _ Fill in the fields with your personal information (do not use fake data). This
information will be used to download and work with Packet Tracer.
Create Account
Email
First Name
Last Name
Country or Region .
Company
Password
Confirm Password


### Lab Assignments & Solutions — strona 38

Lab Task 2: Downloading & Installing Packet Tracer
In this task, you will download and install the Packet Tracer application.

1 Navigate to the second link provided in the lab resources to register for
Cisco’s Network Academy. Then on the top right, log into the account you
made in Lab Task 1.

3 en e
Introduction to Packet Tracer B i F Se’: .
r fi a X
Hands-On Practice @ 02 0s :


### Lab Assignments & Solutions — strona 39

SS a a aaa aa
2 Go to the Resources drop-down and select Download Packet Tracer.
inluealai prsicli My NetAcad Resources Courses Careers More
Home / I'm Learning Certification Exams & Discounts
I'm Learning Find an Academy
Courses I've Enrolled In AU Resources
Alumni Courses
> 4 o Ended
acm
Introduction to Packet Tracer English 1020
Cisco Virtual Academy
3 Scroll down to Download and choose the 64-bit download version.
Note: You should be signed into the Cisco account you previously created.
+ For oNAY.02, Packet Taeer8.0 64 the minimum version ene acs an new PTSAt® work oper
Linux Desktop Version 8.0 English
smacos Version 80 nls
ite


### Lab Assignments & Solutions — strona 40

SS a a aaa aa
4 Click the downloaded .exe to start the installation process.
Windows Desktop Version 7.3.0 English
64 Bit Download 32 Bit Download
Open ion 7.3.0 English
Show in folder |
An Enalich
WD PacketTracer-7.3.0-...0%
LM 0 Type here to search oO [oa g
5 Allow the program to make changes to the device. Allowing the application
to make changes is a Windows feature that helps prevent unauthorized
changes. The changes can be approved only by an administrator.
ee Cisco Packet Tracer
Verified publisher: CISCO SYSTEMS, INC.
File origin: Hard drive on this computer
Show more details
a *


### Lab Assignments & Solutions — strona 41

ee
6 Accept the agreement to continue the installation process.
License Agreement
Please read the following License Agreement. You must accept the terms of this
agreornent before continuing with the metalation.
DOWNLOADING, INSTALLING, OR USING THE CISCO PACKET TRACER SOFTWARE
(CONSTITUTES ACCEPTANCE GF THE CISCO END USER LICENSE AGREEMENT
("EULA" https://vww.cisco.com/c/en/us/about/legal/ cloud-and-
Softuare/and user icense- agreement trl) AND THE SUPPLEMENTAL END USER
|LICENSE AGREEMENT FOR CISCO PACKET TRACER (""SEULA"
Itosi/wrecsco com/c/dam/en us/ebout/doing busiess/leal'seula/cisco-packet:
[racersoftware.pd) IF YOU DO NOT AGREE TO ALL OF THE TERMS OF THE EULA
JAND SEULA, THEN CISCO SYSTEMS, INC. ("CISCO") IS UNWILLING TO LICENSE
|THE SOFTWARE TO YOU AND YOU’ARE NOT AUTHORIZED TO DOWNLOAD,
INSTALL OR USE THE SOFTWARE.
OT do not accept the agreement
eH
7 Select a path for the program's files.
Select Destination Location >
Where should Cisco Packet Tracer 8.0 64Bit be installed? a
| Setup will install Cisco Packet Tracer 8.0 64Bit into the following folder.
To continu, cick Next. If you woul ke to selec a cfferent folder, cick Browse
Atleast 46,6 MB of ree diskspace i required
co =


### Lab Assignments & Solutions — strona 42

SS a a aaa aa
8 Select a name for the start menu folder.
Note: It is recommended to leave the name as-is.
Fy =
Select Start Menu Folder ~
Where should Setup place the program's shortcuts? @
-L. setup wil create the program's shortcuts inthe folowing Start Menu folder.
To continue, click Next. If you would like to select a different folder, click Browse.
Browse.
Tas canal
9 Create a shortcut for ease of access.
PA a
Select Additional Tasks Se
Which additional tasks should be performed? as
Select the additional tasks you would like Setup to perform while installing Cisco
Packet Tracer 8.0 64Bit, then click Next.
Adeitional shortcuts:
(icreate a Quick Launch shortcut
co cme


### Lab Assignments & Solutions — strona 43

———————— = EEE Eas
10 Click Install to begin the process.
Ready to Install
‘Setup is now ready to beain installing Cisco Packet Tracer 8.0 64Bit on your A
computer ‘Sz
ck Instal to continue withthe installation, or cick Back f you want to review or
change any settings.
Destination location:
C:\Program Files\Cisco Packet Tracer 8,0
Start Menu folder:
Cisco Packet Tracer
Additional tasks:
‘Addtonal shortcuts:
Create a desktop shortcut
11 When the installation ends, select Launch Cisco Packet Tracer and click
Finish.
~~ Completing the Cisco Packet
FeV Tracer 8.0 64Bit Setup Wizard
= ‘Setup has finished installing Cisco Packet Tracer 8.0 64Bit on
your computer. The application may be launched by selecting
the installed shortcuts.
Click Finish to exit Setup.


### Lab Assignments & Solutions — strona 44

———————— = EEE Eas
12 Once Packet Tracer launches, select No in the message that asks about
running multi-user.
Networking Hy
Academy. Cisco Packet Tracer
.¢
2) Would you like to run multi-user when application starts?
"
© Copyright CisgB 2021
13 Inthe Windows Security Alert that appears, select Private networks and
click Allow access.
[ i Windows Security Alt x
6 Windows Defender Firewall has blocked some features of this
app
indo Defender Preval hs bled sane eae of Pade Tac Exetel pe
popes
ome: ‘Packet Tree Exeable
Pate Crogan essen pct Wace 7.3.06
(oielvareoe
et i ace ib cnemuse tse ta
[lhenetws, su as ese prs and cffee sha (pt ecamended
caine hese heersoherovelte oho sear)
e=T


### Lab Assignments & Solutions — strona 45

SS a a aaa aa
14 Sign in using the email you provided in Lab Task 1.
@s
EN
stftatfie
cisco
Sign in
Username or Email
-
15 Provide the password for the account.
<Back @s
AT
cisco
Welcome
Username or Email
Dummy@example.com
Password
Forgot Password?


### Lab Assignments & Solutions — strona 46

16 You should now be able to work with Packet Tracer.
fF
Sqetdveese ge
om 4 re PS RRR Ro wee ee mene ee


# NET-03-LS2 — Initial Cisco Device Configuration

> Zakres źródłowy: strony 47–70.


### Lab Assignments & Solutions — strona 47

Computer Networking
Lab Assignment Switch & IOS
& Solution Fundamentals
4 NET-03-LS2
Ta Initial Cisco Device
at U Configuration
Copyright © 1996-2020 HackerU Ltd.
All Rights Reserved.


### Lab Assignments & Solutions — strona 48

Note: Solutions for the instructor are shown inside the green box.
*@) Lab Objective
Learn how to set basic configurations on a switch using Cisco IOS commands.
bs Lab Mission
e Connect to and access the device IOS using the out-of-band management
method.
e Explore and navigate the different Cisco IOS modes.
e Understand and practice Cisco IOS commands used to configure a network
device for the first time, focusing on switch settings.
ea .
©) Lab Duration
30-60 minutes
fe Requirements
e Basic understanding of IOS commands and navigation.
oo
| Resources
e Environment & Tools
Cisco Packet Tracer 7.2.2 or later
e Extra Lab Files
NET-03-L2.pka


### Lab Assignments & Solutions — strona 49

Instructions for PKA Lab Files
Lab material includes the lab document and a PKA lab file.
When you open a PKA file in Cisco Packet Tracer, two windows appear:
1. Lab topology window
2. Activity window
PKA Features
Note the following essential information regarding the Activity window:
1. Completion Percentage — Student progress appears at the bottom right corner of
the window.
2. Check Result Button — When you click this button and then click the "Assessment
Items" tab, you will find a checklist with lab objectives and status, whereby V=done,
X=not done.
Note: Both features help the instructor grade the exercise swiftly and efficiently.
Ee ee fT a cmt
Please refer to the exercise document and carefully follow the — —
See the percentage of completion a the right-battom comer to = Na ° a
determine your progres, Fi nae ¢ ote
‘Note: The Optional and Bonus section are not scored. XK Senice Inconect 1 ie
Good bia + nooo ° other
qo Sc ee = on) PEL sae ema Ot °
PKA Solution
To view the solution or edit the lab file, you can simply click the "Wizard hat" icon and
enter the following password: C!ScOM@ster
Right-click the "Answer network" tab and then click "Show Answer network".
Note: Be careful not to change anything so that the lab will remain intact.


### Lab Assignments & Solutions — strona 50

Lab Task 1: Access the Device
Connect to a switch with a console cable and gain access to the console.
Note: If the lab opens with missing parts, configurations, or errors, refer to the last task
(Task 4) in the lab for guidance.
1 Click the connections box # at the bottom left corner and select the console
cable “.
Bs —
ay CS a) ales ESE Pale
cr | and
a ee
2 Connect one end of the cable to the RS-232 port on the admin PC, and the other
end to the Console port on the switch.
Flotgr1
Admin PC
Userl -
User2


### Lab Assignments & Solutions — strona 51

3 Now that you established a physical connection, start the terminal session, as
follows:
=
Click the admin PC, navigate to the Desktop tab, and click the Terminal icon Ba
Then click OK (accept the default settings).
Note: The messages that appear on the screen are part of the boot process.
® admin ec ist 2nd - op x
Physical Confo [Dosen] Programming Janrbutes
= <> lA =| Pva [rvs J
=e v
Cte
B Admin PC = a x
Physical Config Deaton Progamming Atributes
Per Corfaration
Dts Per Second 00 5
Date Bits 5 z
Pay ie z
Stop Bits 1 3
Flow Coil None z
te
Page5


### Lab Assignments & Solutions — strona 52

4 When the boot ends, press Enter to begin.
B Laptopo os o x
Physical Config Desktop Programming —_ Attributes
[Terminal
[Top


### Lab Assignments & Solutions — strona 53

5 Answer the following questions:
a. List the four IOS modes of Cisco devices.
b. Which cable type and what kind of software are required for out-of-band
management (initial device configuration)?

c. Which device components store operating system files?
d. Do Cisco devices run diagnostic tests upon startup?

A. 10S Modes:
(1) User EXEC Mode - Limited monitoring commands.
(2) Privileged EXEC Mode - View and manage configuration files (using copy and
show commands).
(3) Global Configuration Mode - Configure general device settings (such as device
name, user names, passwords, etc.).
(4) Interface or Line Configuration Mode — Configure interface settings (such as IP
addresses).

B. Console Cable and Terminal Software, such as PuTTY.

C. Flash memory

D. Yes, POST (Power-On Self-Test).


### Lab Assignments & Solutions — strona 54

Run all commands on S1-Floor1.
Tip: Pay attention to the prompt!
Step 1— Explore the User EXE Mode
Note: The commands are also valid on a router IOS system.
1 Welcome to User EXEC mode. Type ? and view the list of commands available in
this mode.
Press RETURN to get started!
Switch>?
Exec commands:
connect Open a terminal connection
disable Turn off privileged commands
disconnect Disconnect an existing network connection
enable Turn on privileged commands
exit Exit from the EXEC
logout Exit from the EXEC
ping Send echo messages
resume Resume an active network connection
show Show running system information
telnet Open a telnet connection
terminal Set terminal line parameters
traceroute Trace route to destination


### Lab Assignments & Solutions — strona 55

2 The show command in the list displays system settings. Enter show and ? (with a
space between them).
Choose the correct command combination from the list to display the clock. The
clock appears not to be set because in this mode we do not have permission to
configure it.
Switch>show ?
arp Arp table
cdp CDP. information
clock Display the system clock
crypto Encryption module
dtp DTP information
etherchannel EtherChannel information
flash: display information about flash: file system
history Display the session command history
interfaces Interface status and configuration
<output omitted>
Switch>show clock
*@:9:32.744 UTC Mon Mar 1 1993


### Lab Assignments & Solutions — strona 56

Step 2 — Explore the Privileged EXE mode
3 Type ? again and locate the Enable command. Enter the command to move to
the next mode.
This mode (#) is called Privileged EXEC, and is meant only for troubleshooting and
file system management.
Switch>?
Exec commands:
connect Open a terminal connection
disable Turn off privileged commands
disconnect Disconnect an existing network connection
exit Exit from the EXEC
<output omitted>
Switch>enable
Switch#


### Lab Assignments & Solutions — strona 57

4 Set the clock to the correct date and time. Type clock set with ? and add the
missing information. Check each time if anything else is missing by adding ? at
the end of the command. Then, verify the clock settings using the show clock
command.

Switch#clock set ?
hh:mm:ss Current Time
Switch#clock set 19:41:00 ?
<1-31> Day of the month
MONTH Month of the year
Switch#clock set 19:41:00 14 september ?
<1993-2035> Year
Switch#clock set 19:41:00 14 september 2019 ?
<cr>
Switch#clock set 19:41:00 14 september 2019
Switch#show clock
19:41:4.345 UTC Sat Sep 14 2019

5 Enter conf and press the TAB key to auto-compete the command. Press the
spacebar with ?. The only option is Terminal. Type t and press the TAB key. Press
Enter to move to Global Configuration mode. Continue with Task 3.

Switch#conf
Switch#configure ?

terminal Configure from the terminal

<cr>
Switch#configure t
Switch#configure terminal
Enter configuration commands, one per line. End with CNTL/Z.
Switch(config)#


### Lab Assignments & Solutions — strona 58

Lab Task 3: Initial and Security Settings
Secure access to the switch using a password and a banner.
Step 1— Configure the device name and create accounts
Tip: All of the required commands for this exercise can be found in the presentation or
textbook in the Initial Device Configuration section.
1 Set the device name to $1-Floor1.
Switch(config)#hostname S1-Floor1
2. Create a user account with the following details:
Username: Admin
Password: p@nd@
S$1-Floor1(config)#username Admin password p@nd@
Step 2 — Configure security settings
3 Set the enable password to c!scO
S1-Floor1(config)#enable password c!sc@
4 Set an appropriate security message (banner):

Access to this device is for authorized personnel only!
S$1-Floor1(config)#banner motd #Access to this device is for authorized
personnel only!#


### Lab Assignments & Solutions — strona 59

Step 3 — Secure the console port and verify settings
5 Secure access to the console port by setting username and password
authentication on the port. To enter the port configuration use the command line
console 0 to set the username and password use the command login local.
S1-Floor1(config)#line console @
S$1-Floor1(config-line)#login local
S$1-Floor1(config-line)#exit
6 Return to Privileged mode.
$1-Floor1(config)#exit
S1-Floor1#
%SYS-5-CONFIG_I: Configured from console by console
7 Using show running-config, display device settings, and verify that the system is
set up correctly.
The output should be similar to the following (notice the highlighted text):
$1-Floorl#show running-config
Building configuration...
Current configuration : 1234 bytes
!
version 12.2
no service timestamps log datetime msec
no service timestamps debug datetime msecno service password-encryption
enable password c!sc@
!


### Lab Assignments & Solutions — strona 60

!
!
spanning-tree mode pvst
spanning-tree extend system-id
!
interface FastEthernet0/1
!
<output omitted>
!
interface GigabitEthernet0/1
!
interface GigabitEthernet0/2
!
interface Vlan1
no ip address
shutdown
!
banner motd “CAccess to this device is for authorized personnel only!*C
!
!
!
line con @
login local
!
line vty 0 4
login
line vty 5 15


### Lab Assignments & Solutions — strona 61

login
!
End
8 Answer the following questions:
a. What is the difference between the login and login local commands?
b. Where on the device is the running-config file stored?
c. How many FastEthernet and Gigabit Ethernet interfaces does the switch have
according to the show running-config command output?
d. Are the passwords displayed in plain text? Why?
e. Where on the device is startup-config stored, and why is it important to copy
all settings to it?

A. Configured on line console 0, the login command enables only password checking.
The login local command enables both username and password checking.

B. RAM (Random Access Memory)

C. 24 FastEthernet / 2 Gigabit Ethernet

D. Yes, the service password encryption is not enabled.

E. NVRAM Memory. This is non-volatile memory, meaning the data is available after
power loss, unlike RAM. (Note that the system loads the device settings by default
from the NVRAM, upon startup.)


### Lab Assignments & Solutions — strona 62

Step 4 — Enable the password-encryption service and back up the
configuration
9 Return to Global Config mode and encrypt all passwords on the device with the
command service password-encryption.
Switch#configure terminal
10 Enter End and press Enter. Display the running-config file again, and make sure all
passwords are encrypted with the command show running-config.
S$1-Floor1(config)#end
S1-Floor1#
%SYS-5-CONFIG_I: Configured from console by console
$1-Floorl#show running-config
Building configuration...
Current configuration : 1247 bytes
!
version 12.2
no service timestamps log datetime msec
no service timestamps debug datetime msec
service password-encryption
!
hostname S1-Floor1
!
enable password 7 @822@D5D0A49
!
username Admin privilege 1 password 7 @8316C49@D39


### Lab Assignments & Solutions — strona 63

11 Save all device settings locally with the command copy running-config startup-
config.
$1-Floorl#copy running-config startup-config
Destination filename [startup-config]?
Building configuration...
[OK]
12 Display startup-config to make sure all settings were copied. To do so, make sure
that the running-config is identical to the startup-config.
$1-Floorl#show startup-config
<output omitted>
#Make sure the setting in this file is identical to the running-config
file.#
Step 5 — Configure IP addresses on the user PCs
13 Click the User1 computer, move to the desktop tab, and click the IP configuration
icon: Ee
14 Configure the following static addresses and close the window:
e@ IP: 10.0.0.1
@ Subnet mask: 255.0.0.0


### Lab Assignments & Solutions — strona 64

15 For the User2 PC, configure the IP: 10.0.0.2 with the same subnet mask address
as User1.

a E

O pice © sac

IPAddess raco2

Subnet Mask 56000

Deft Gateway e000

DNS Sener e000
16 Which command in CMD is used to display the host network settings?
17 Enter the User1 Desktop tab and click the Command Prompt icon.

|
ey el Sy Se
a
Dep


### Lab Assignments & Solutions — strona 65

18 Ping the User2 address to check connectivity.
Packet Tracer PC Command Line 1.0
ci\>ping 10.0.0.2
Pinging 10.0.0.2 with 32 bytes of data:
Reply from 10.0.0.2: bytes=32 time=Ims TTL=128
Reply from 10.0.0.2: bytes=32 time<1ms TTL=128
Reply from 10.0.0.2: bytes=32 time<Ims TTL=128
Reply from 10.0.0.2: bytes=32 time<Ims TTL=128
Ping statistics for 10.0.0.2:
Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),
Approximate round trip times in milli-seconds:
Minimum = Oms, Maximum = lms, Average = Oms
Note: A connectivity test in Packet Tracer can also be done using the Envelope tool:
a. Click the Envelope icon 4 .
b. Click the source device.
c. Click the destination device.
d. Check the status, Failed/Successful, in the status bar (marked by “<” at the
bottom right corner).
BeestOraaarr+.raacobges 2
sQec bv meee
GEER Physical ee ean ae
| 1 seléct envelope tool ‘ c
2 masewne et] (| 3.elk pe you want to
to test from wes test
=a situiaion
poe sees e Sere sssessesse 4, check success/fallure
ae by clicking here
[Be gage; ea :


### Lab Assignments & Solutions — strona 66

Step 6 — View the MAC table and interface settings of the switch
19 To view interface settings, such as duplex mode, bandwidth, and the interface
speed, use the show interface [interface name] command in privileged exec
mode. Return to the terminal in the “Admin PC” and use the command to check
the status of interface fastEthernet 0/1. The output should be similar to the
following:
S1-Floorl#show interfaces fastEthernet 9/1
FastEthernet@/1 is up, line protocol is up (connected)
Hardware is Lance, address is 00e0.8f38.b601 (bia @0e0.8f38.b601)
BW 100000 Kbit, DLY 1000 usec,
reliability 255/255, txload 1/255, rxload 1/255
Encapsulation ARPA, loopback not set
Keepalive set (10 sec)
Full-duplex, 10@Mb/s
input flow-control is off, output flow-control is off
ARP type: ARPA, ARP Timeout 04:00:00
Last input 00:00:08, output 90:00:05, output hang never
Last clearing of “show interface" counters never
Input queue: @/75/0/® (size/max/drops/flushes); Total output drops: @
Queueing strategy: fifo
Output queue :0@/40@ (size/max)
5 minute input rate @ bits/sec, @ packets/sec
5 minute output rate @ bits/sec, @ packets/sec
956 packets input, 193351 bytes, @ no buffer
Received 956 broadcasts, @ runts, @ giants, © throttles
@ input errors, @ CRC, @ frame, @ overrun, @ ignored, @ abort
@ watchdog, @ multicast, @ pause input


### Lab Assignments & Solutions — strona 67

@ input packets with dribble condition detected
2357 packets output, 263570 bytes, @ underruns
® output errors, @ collisions, 10 interface resets
®@ babbles, @ late collision, ® deferred
@ lost carrier, @ no carrier
® output buffer failures, @ output buffers swapped out
20 Display the switch’s MAC table, with the command: show mac-address-table .
S1-Floorl#show mac-address-table
Mac Address Table
Vlan Mac Address Type Ports
1 @001.c9bb.9e7b DYNAMIC Fa@/2
1 0003.e41a.b68d DYNAMIC Fa@/1
21 How do we measure the network speed of an interface or cable (the bandwidth)?
(Refer to the show interface output.)
Megabits per second, or Mbps


### Lab Assignments & Solutions — strona 68

22 Which PC physical address is associated with the fastEthernet 2 interface?
S1-Floorl#show mac-address-table
Mac Address Table
Vlan Mac Address Type Ports
il Q001.c9bb.9e7b DYNAMIC Fa@/2
1 0003.e41a.b68d DYNAMIC Fa@/1


### Lab Assignments & Solutions — strona 69

Lab Task 4: Alternative Lab Opening
In this task, you will open the PKA file in an alternative way to avoid potential errors.
1 Open Packet Tracer.
2 Inthe menu, click “File” and then click “Open...”.
IR Cisco Packet Tracer - a x)
Fie| E6t Optons View Tos Extensions Hep
tam 1° 7CQQne ise E
El Open Samples Ctrl+ShitsT
ioe meen 6 Be ee
Open Activity Sequence Root] re iC I (~~ 00:43:30}
la Save Chri+s: ———— ae
Save As Ctrl+Shit+S
Save As PAZ Ctsatez
Save As Common Ganridge
AR Print cuiep
Exit and Logout
Exit
Time: 000127( JC) CED Sinuiaton
29S OOECSESSESGGEG05 G56
Od casei) Cassis) Caso) Casts) ieee eames Cate) Cocea) eran ey Cane) aed
S628 0 9 OS wane nantes)


### Lab Assignments & Solutions — strona 70

3 Navigate to the file’s location and open it.

€© > © IRL « Matera Development > US > Modules > NETMichigan > NETO

Organize + New folder S~ m@ @
a
|
1 cA) sf
j A =
' ® von Ooo
i
i
i
i
i
|

Filename: [NET-B-L2pta | [Packet TacerFle pla". ©]


# NET-03-LS3 — Backing Up Config Files and Managing the IOS

> Zakres źródłowy: strony 71–85.


### Lab Assignments & Solutions — strona 71

Computer Networking
Lab Assignment Switch & IOS
& Solution Fundamentals
NET-03-LS3
° aT Backing Up Config Files
ia U and Managing the IOS
Copyright © 1996-2021 HackerU Ltd.
All Rights Reserved.


### Lab Assignments & Solutions — strona 72

Note: Solutions for the instructor are shown inside the green box.
©) . .
©) Lab Objective
Understand how to configure and back up Cisco devices.
bs) Lab Mission
Use a Trivial File Transfer Protocol (TFTP) server to back up and roll out switch
configurations.
C2 .
©) Lab Duration
30-60 minutes
fe Requirements
e Knowledge of basic IOS commands and navigation
e Knowledge of Cisco device components and system files
oo

| Resources
e Environment & Tools

o Cisco Packet Tracer 7.2.2 or later
e Extra Lab Files

o NET-03-L3.pka


### Lab Assignments & Solutions — strona 73

Instructions for PKA Lab Files
Lab material includes the lab document and a PKA lab file.
When you open a PKA file in Cisco Packet Tracer, two windows appear:
1. Lab topology window
2. Activity window
PKA Features
Note the following essential information regarding the Activity window:
1. Completion Percentage: Learner progress appears at the bottom right corner of the
window.
2. Check Result Button: When you click this button and then click the Assessment
Items tab, you will find a checklist with lab objectives and status, where V means done
and X means not done.
Note: Both features help the instructor grade the exercise swiftly and efficiently.
ee ne) Omak aascesis Gmatiat
Please refer to the exercise document and carefully follow the a ae -
ledisa a = ae Capa ea
See the percentage of completion atthe right-bottom corner to = Ta fi sas
determine your progress. 5) NIP Sener oO Other:
Note: The Optional and Bonus section are not sored Ses wef ,
Good tude A ‘ cite
PKA Solution
To view the solution or edit the lab file, click the wizard hat icon and enter the following
password: C!ScOM@ster.
Right-click the Answer Network tab and then click Show Answer Network.
Note: Be careful not to change anything so that the lab will remain intact.


### Lab Assignments & Solutions — strona 74

Important Note: In this lab, to avoid potential errors, do not open the associated
PKA file by double-clicking it. Instead, open the file by using the following method:
1 Open Cisco Packet Tracer.
2 Inthe window that appears, click File and then click Open...
IR Cisco Packet Tacer - a x
Fie]] Eo Optons View Tools Extensions Hep
1. ee IF 782QQ0H ESE 2
lm Open Samples Cirl+Shit+T
= » ée Sa ia ee
Open Activity Sequence Root] I iC IC ( ~ 00:43:30)
ka Save cries ———
Save As cuts shites
Sare As PKZ cisaitez
Save As Common Cartridge
prot cise
Berets
Ext
Tine: o00427( JC) (Q Reatime) Simulation]
SIRS DOGSESesSssooonses.e
\4331_) 4321) _1941 | | 2901 ) | 2911 | (61910%) ‘G19HGW \_829_/ _1240 ) (PERouss) (Prempy |_1641_ (2620
(OT
S28 0 9 Om nae tases


### Lab Assignments & Solutions — strona 75

3 Navigate to the file's location and open it.
€ > © 1 | « Materal Development > US > Modules > NETMichigan > NETO
Organize + New folder S~ @ @
a
a
a A A
. A
a
a
a
a
a
a
1
a
i


### Lab Assignments & Solutions — strona 76

Lab Task 1: Back Up Configuration Files
Note: If the lab opens with missing parts, configurations, or errors, close and repeat the
above steps to reopen the lab.
192.168.1.0/24
R1
192.168.1.1
$1
TFTP Server
192.168.1.3 192.168.1.2
Note: Run all commands on S1.
1 The preconfigured devices have logical addresses. From the TFTP server, test
connectivity to $1 and R1.
2 Click the switch $1 and navigate to the CLI tab.
beasoraeariaaaomase 2
SQexhvmeé@ mm
(A coos SNES [een ce


### Lab Assignments & Solutions — strona 77

id
Physical Config Attributes
10S Command Line Interface
TANBASE-
12.2 (25) FK, RELEASE SOFTWARE (201)
Compiled Wed 12-Oct-05 22:05 by pt_team
Press RETURU to get started!
SLINK-S-CHANGED: Interface FastEthernet0/1, chenged state to wp
SLINEPROTO-S-UPDOWN: Line protocol on Interface FastEthemet0/1,
SLINEPROTO-S-UPDOWN: Line protocol on Interface Vianl, changed
SLINEPROTO-5-UPDOWM: Line protocol on Interface
Cuil to exit CL focus Copy | | Paste
OTop
3. Onthe switch, create two user accounts:
i) Username: Admin, password: p@nd@
ii) Username: Technician, password: ku@I@
To do so, use the following commands:
S1>enable
Si#configure terminal
S1(config)#username Admin password p@nd@
S1(config)#username Technician password ku@1l@
4 Secure the console line by enabling local password checking.
To do so, use the following commands:
S1(config)#line console @
S1(config-line)#login local
S1(config-line)#exit


### Lab Assignments & Solutions — strona 78

5 Set the enable password to clscO.
To do so, use the following command:
S1(config)#enable password c!sc@
6 Encrypt all passwords on the device.
To do so, use the following command:
S1(config)#service password-encryption
7 Set an appropriate security message (banner):
Access to this device is for authorized personnel only!
To do so, use the following command:
S1(config)#banner motd #Access to this device is for authorized personnel
only!#
8 Disable DNS lookup on the device using the following command:
S1(config)#no ip domain-lookup
9 What does the command copy running-config startup-config do?
The command saves the configuration from RAM to NVRAM.
10 Save the running configuration to the startup file of the switch.
To do so, use the following commands:
Si#copy running-config startup-config
Destination filename [startup-config]?
Note: you can also use the shortcut for this command, which is $1#copy run
start.


### Lab Assignments & Solutions — strona 79

Sl#copy run
Sl#copy Sonningecorieig startup-config
Destination filename [startup-config] ?|
Building configuration...
[OK]
Sslé# v
Ctrl+F6 to exit CLI focus Copy Paste
C1 Top
11. Verify that the TFTP service is up and running on the server (TFTP server) by
clicking the server, going to the Services tab, clicking TFTP, and selecting On.
® TFTP Server - im x
Physical Config Services Desktop Programming —_ Attributes
SERVICES P
HTTP 7
DHCP Senice O of
File A
= asa842-k8.bin
SYSLOG asa923-k8.bin
AAA CARA A advinconirock@.m7 194.16 T1 hin
12 On the switch, copy the running-config file to the TFTP server and name it $1-
config-backup20.9. Use the command S1#copy running-config tftp. When
prompted, enter the IP of the TFTP server, which is 192.168.1.3. Name the file
when prompted to do so.
S1#copy running-config tftp
Address or name of remote host []? 192.168.1.3
Destination filename [S1-confg]? S1-config-backup20.9


### Lab Assignments & Solutions — strona 80

sl¢
Sl#copy running-config tftp
Address or name of remote host []? 192.168.1.3
Destination filename [Sl-confg]? Sl-config-backup20.9
Writing running-config...!!
{OK - 1364 bytes]
1364 bytes copied in 0 secs
Siz] Ms
Ctrl+F6 to exit CLI focus Copy Paste
(1 Top
13 Verify that the configuration was backed up to the TFTP server by clicking the
server, going to the Services tab, clicking TFTP, and reviewing the files.
® TFTP Server = o x
Physical Config Services Desktop Programming —_ Attributes
SERVICES THI
HTTP
DHCP Service @ on O of
DHCPv6
File “
SYSLOG asa842-k8 bin
DAA asa923-k8.bin
NTP 184 1.advineorirack9.m7 194.16 T4 hin


### Lab Assignments & Solutions — strona 81

Lab Task 2: Back Up and Upgrade the Device ISO
Note: Run all commands on S1.
Part 1: Back up the device operating system
Note: Every file can potentially become corrupted. If the operating system itself is
corrupt, the device may not even be able to boot correctly. It is therefore always a
good idea to keep current copies of OS files.
1 Show the version of the IOS on the switch using the show version command in
Privileged EXEC mode.
2 Display the contents of the flash memory and document the IOS file name with
S1#show flash.
[ Jee
CifsF6 to ext CL focus em Pasie
C1 Top
3 Use the copy command to back up the image file to the TFTP server and name it
$1-OSimage-backup.
Si#copy flash tftp
Source filename []? C2960-lanbase-mz.122-25.FX.bin
Address or name of remote host []? 192.168.1.3
Destination filename [C2960-lanbase-mz.122-25.FX.bin]? S1-OSimage-backup


### Lab Assignments & Solutions — strona 82

Slt
Sl#copy flash tftp
Source filename []? c2960-lanbase-mz.122-25.FX.bin
Address or name of remote host []? 192.168.1.3
Destination filename [c2960-lanbase-mz.122-25.FX.bin]? Sl-
OSimage-backup
Writing c2960-lanbase-mz.
122-25. FX.bin.. SPF EUEF PEPE PEP EP ESE PEP EP ESP Pee ee ee ee ee eee gees
{OK - 4414921 bytes]
4414921 bytes copied in 0.054 secs (2221364 bytes/sec)
siz] ¥
Ctrl+F6 to exit CLI focus Copy Paste
(Top
4 Access the TFTP server and verify the IOS image copy on the server.
® TFTP Server = o x
Physical Config Services Desktop Programming Attributes
SERVICES TeTP
HTTP
eS Senice @on O of
DHCPv6 -————. eww.0mmm >>]
File a
me $1-OSimage-backup
SYSLOG ‘St-config-backup20.9
Part 2: Upgrade the device IOS to a newer version
5 Locate the following image filename on the TFTP server:
c2960-lanbasek9-mz.150-2.SE4.bin.
6 Access $1 and verify that there is enough free space in flash memory for the new
10S file using the $1#show flash command.


### Lab Assignments & Solutions — strona 83

Slt
slit
Sl#show flash
Directory of flash:/
1 -rw- 4414921 <no date> c2960-lanbase-mz.
122-25.FX.bin
14° -rw- 4670455 <no date> c2960-lanbasek9-mz.
150-2.SE4.bin
130 -rw- 1364 <no date> config.text
[| c2016384 bytes total (54925644 bytes free) |
v
Ctri+F6 to exit CLI focus Copy Paste
(1 Top
7 Copy the new image file version from the TFTP server (c2960-lanbasek9-mz.150-
2.SE4.bin) using the command copy tftp flash. |n the first dialog option, insert the
IP address of the TFTP server. In the second option, insert the name of the image
file. The filename must be typed as shown to prevent transmission errors. In the
third option, press Enter.
Si#copy tftp flash
Address or name of remote host []? 192.168.1.3
Source filename []? c2960-lanbasek9-mz.15@-2.SE4.bin
Destination filename [C2960-lanbasek9-mz.150-2.SE4.bin]?
Sl#copy tftp flash
Address or name of remote host []? 192.168.1.3
Source filename []? c2960-lanbasek9-mz.150-2.SE4.bin
Destination filename [c2960-lanbasek9-mz.150-2.S5E4.bin]?
Accessing tftp://192.168.1.3/c2960-lanbasek9-mz.150-2.SE4.bin...
Loading c2960-lanbasek9-mz.150-2.SE4.bin from 192.168.1.3:
[OK - 4670455 bytes]
4670455 bytes copied in 0.062 secs (6056253 bytes/sec)
siz Mw
Ctrl+F6 to exit CLI focus Copy Paste
L Top
8 Verify that the new IOS image was copied to flash memory. To do so, use the
command $1# show flash.


### Lab Assignments & Solutions — strona 84

Sifshow flash
Directory of flash:/
Lonrw 4414922 <no dave> c2960-Lanbase-mz.
150-2.5E4.bin
= TSE oo oer
c4016384 bytes total (54929644 bytes free)
Slt ¥
Ctrl#F6 to exit CLI focus Copy Paste
(Top
9 Use the boot system in Global mode to load the new image.
Enter the command:
IS1(config)#boot system flash: /c2960-lanbasek9-mz.150-2.SE4.bin
S1 (config) #
S1 (config) #
Sl(config)#boot system flash: /c2960-lanbasek9-mz.150-2.SE4.bin
S1 (config) #| v
Ctrl+F6 to exit CLI focus Copy Paste
CO Top
10 Reload the switch. Type yes when asked to save and click OK to proceed with the
reload.
Slé#
Sl#reload
System configuration has been modified. Save? [yes/no]:yes
Building configuration...
[0K]
Proceed with reload? [confirm] M
Ctri+F6 to exit CLI focus Copy Paste
C1 Top
11 Verify that the new version was installed after reboot using the command
S1#show version.


### Lab Assignments & Solutions — strona 85

| Bs — a x Bs — o x
| Physical Cong ctl Abies Physical Cong _CLI_artibutas
| 19S Command Line Interface 10S Command Line Interface

ery n _ - x

fu 69% bytes of Tlash-simated non-volatile confaguration memory.

a Base ethernet WAC Addreos + 00417:59:A7151:20

a Motnezbserd assembly number + 73-10380-03

: Power supply part nunber + 341-0087-02
| TOTeeTeEe, C2960 Sofcware (C2960-LANERSEKS-H), Version Reet pay seael aaa

18.0(2)SE4, RELEASE SOFTWARE (£c1) evi alan: nine :

‘Technical Support: Aetp!//www.ciaco.com/techsupport Bone oor evisionmmmper = 15

" Mode number + W5-c2960-247T-L

Copyzight (c) 1986-2019 by Cisco Systema, Inc. Bee Pe vcsnenae Lea

Compiied Wes 26-dun-13 02249 by naguyen See ee erence 2 oro

ROK: Bootstrap program is C2960 boot loader eeeaeeesbLclaistensiints: cA
Uf | sorame: cate sive seer senneacemcor-ay veisia. sasaineeyre ET canae —

ETWARE Raravare Board Revision Munber + 0x02

Switch uptine is 99 minucee

Syeten returned to ROK by power-on AKU ee ih —— oe

Staten Guapo Gilg Voce oe etokpe lanbend¥S an iii 30S, SEN Switch Ports Model SITET Sw Image

+ 126 ws-cosep-zerrn | 15.0(2)988 c2960-

this product contains cryptographic feacuzes and is subject to Paes

unitea

States and local country lave governing import, export, transfer | accep Bceaste Peseccl Mer 55

CUi+F6 to exit CLI focus Copy Paste (Cul#=6 to exit CLI focus Copy Paste
Ctop Oto


# NET-04-LS1 — Configure and Verify Port Security

> Zakres źródłowy: strony 86–110.


### Lab Assignments & Solutions — strona 86

Computer Networking
Lab Assignment Switch Security
& Solution
NET-04-LS1
Configure and Verify
o° (ee Port Securi
Oln ty
EI
Copyright © 1996-2020 HackerU Ltd.
All Rights Reserved.


### Lab Assignments & Solutions — strona 87

Note: Solutions for the instructor are shown inside the green box.
»©) Lab Objective
Learn how to implement port security and the various violation rules, and how port
security uses physical addresses.
by Lab Mission
Use port security to protect assets from a rogue laptop and show the importance of
physical security on a switch.
es .
©) Lab Duration
30-60 minutes
fe Requirements
e Knowledge of basic IOS commands and navigation
os

| Resources
e Environment & Tools

o All platforms

o Cisco Packet Tracer 7.2.2 and higher
e Extra Files

© NET-04-L1.pka


### Lab Assignments & Solutions — strona 88

Instructions for PKA Lab Files
Lab material includes the lab document and a PKA lab file.
Open the PKA file through the Cisco Packet Tracer menu by clicking File then Open...
Dette” d &%72aQane ase 2
Serine ome aT)
enn reel nou
Prt ome
ert m je: (Sasa To Dig and Diop To Woe :
Navigate to the file's location and open it.
a
a t: ©
a
r
a
a
a
a
a
4
1


### Lab Assignments & Solutions — strona 89

Note: Double-clicking the PKA file in File Explorer may not work (depending on the
Packet Tracer version).
When you open a PKA file in Cisco Packet Tracer, two windows appear:
1. Lab topology window
2. Activity window
PKA Features
Note the following essential information regarding the PT Activity window:

1. Completion percentage: Learner progress appears at the bottom right corner of
the window.

2. Check Results button: When you click this button and then click the Assessment
Items tab, you will find a checklist with lab objectives and status, where “=done,
X=not done.

Note: Both features help the instructor grade the exercise swiftly and efficiently.
IR br activity: 000012 — xf Assessment items Stas Ponts Components) |Feedback
= NetWork
Please refer to the exercise docurnent and carefully follow the I 4 Re
See the peroentage cof completion at the right-bottom corner to ore
determine your progress, = Po Srey ,
Note: The Optional and Bonus section are not scored. < ot Meomect: t chest
Good tus ox aie macs Cored i ter
= Souetuncs ° ote
[00005793 87C4 Inconect tthe
© FexcbemetTo c One
X Ponsiaus roma | Pose
& Fast heme ¢ ote
x Pot Sis veered Pree
rts = rane — oe
Pass emt I Pres
PKA Solution
To view the solution or edit the lab file, you can simply click the wizard hat icon and
enter the following password: C!ScOM@ster
Right-click the Answer Network tab and then click Show Answer Network.
Note: Be careful not to change anything so the lab will remain intact.


### Lab Assignments & Solutions — strona 90

Lab Task 1: Configure and Verify Port Security
Enable port security and define the physical address and violation rule for each
interface. All the required commands were introduced in the presentation and can also
be found in the textbook.
Note: If opening the PKA file by double-clicking it results in an error, open it in the
following way instead: Click File > Open... and select the file.
Rogue Laptop | N\ .
Rachel Ross Joey Monica
Issue all commands on S1:
1 Click $1, and then click the CLI tab.
Physical Config Attributes
10S. Command Line Interface

Compiled Wed 12-Oct-05 22:05 by pt_team a

Press RETURN to get started!

$LINK-5-CHANGED: Interface FastEthernet0/1, changed state to up

SLINEPROTO-5-UPDOWN: Line protocol on Interface FastEthernet0/1,

changed state to up


### Lab Assignments & Solutions — strona 91

2. Check which computer is connected to which port by populating the MAC
address table. From Rachel’s PC, enter the command prompt and ping every
other PC.

Rachel - o x
Physical Config Programming Attributes
7
Pp Dialup Terminal ‘Command
Configuration Prompt
B
Reply from 10.0.0.2: bytes=32 timesIms TTI=128
Reply from 10.0-0.2: bytes=32 timesims TIL=128
Reply from 10.0.0.2: bytes=32 time<lms TTL=128
Reply from 10.0-0.2: bytes=32 timesIms TID=128
Apetiimate! foGnd-crip-eimed aa m2 1i-eeeonde:
Minimum = Oms, Maximum = ims, Average = oms
Reply from 10.0.0.3: bytes=32 time<lms TTL=1238
Reply from 10.0.0.3: bytes=32 timecims TIL=12¢
Reply from 10.0-0.3: bytes=32 time<Ims TII=128
Ping statistics for 10.0.0.3:
Approximate round trip times in milli-seconds:
C:\> igs

3 To view the MAC addresses connected to the ports, open the S1 switch in CLI
and, in privileged mode, use the command show mac-address-table. Compare
the MAC addresses in the CLI to the ones on the computers.

S1#show mac-address-table


### Lab Assignments & Solutions — strona 92

Mac Address Table
Vlan Mac Address Type Ports
1 0004. 9a8b.2832 DYNAMIC Fa0/3
1 Q009.7c96.0271 DYNAMIC FaQ@/2
T 000b.be34. alae DYNAMIC Fae/4
1 00d@.9793.87c4 DYNAMIC Fa@/1
4 Access configure mode and enable port security on the following ports:
a. fastethernet 0/1
b. fastethernet 0/2
c. fastethernet 0/3
d. fastethernet 0/4
To do so, enter global mode and run the following commands:
1. To select all interfaces: interface range fastethernet 0/1-4
2. To set mode access on the selected interfaces: switchport mode access
3. To set port security: switchport port-security
4. To exit the selection of the interfaces: exit
S1(config)#interface range fastethernet @/1-4
S1(config-if-range)#switchport mode access
S1(config-if-range)#switchport port-security
S1(config-if-range)#exit
5 Set the authorized MAC addresses for the Fast Ethernet 0/1 and 0/2 interfaces to
manual by setting a manual MAC address for each interface.
S1(config)#interface fastethernet Q/1
S1(config-if)#switchport port-security mac-address @@D@.9793.87C4
S1(config-if)# exit
S1(config)#interface fastethernet 0/2
S1(config-if)#switchport port-security mac-address 0009.7C96.0271
S1(config-if)#exit


### Lab Assignments & Solutions — strona 93

6 Set the authorized MAC addresses for the Fast Ethernet 0/3 and 0/4 interfaces to
sticky.
S1(config)#interface fastethernet 0/3
S1(config-if)#switchport port-security mac-address sticky
S1(config-if)# exit
S1(config)#interface fastethernet 0/4
S1(config-if)#switchport port-security mac-address sticky
S1(config-if)#exit
7 Set the violation mode for each interface, as follows:
a. Fast Ethernet 0/1 — Shutdown. The command is switchport port-security
violation shutdown
S1(config)#interface fastethernet Q/1
S1(config-if)#switchport port-security violation shutdown
S1(config-if)#exit
b. Fast Ethernet 0/2 — Restrict. The command is switchport port-security
violation restrict
S1(config)#interface fastethernet 0/2
S1(config-if)#switchport port-security violation restrict
S1(config-if)#exit
c. Fast Ethernet 0/3 — Restrict. The command is switchport port-security
violation restrict
S1(config)#interface fastethernet 0/3
S1(config-if)#switchport port-security violation restrict
S1(config-if)#exit
d. Fast Ethernet 0/4 — Protect. The command is switchport port-security
violation protect
S1(config)#interface fastethernet 0/4
S1(config-if)#switchport port-security violation protect
S1(config-if)#exit
8 Set the maximum MAC address count to 2 on Fast Ethernet 0/3. Use the
command switchport port-security maximum 2
S1(config)#interface fastethernet 0/3
S1(config-if)#switchport port-security maximum 2
S1(config-if)#exit


### Lab Assignments & Solutions — strona 94

9 Set the maximum MAC address count to 2 on Fast Ethernet 0/4. Use the
command switchport port-security maximum 2
S1(config)#interface fastethernet 0/4
S1(config-if)#switchport port-security maximum 2
S1(config-if)#exit
10 Disable all remaining unused ports. (Hint: Use the shutdown command.)
Tip: The range command is useful when you want to issue the same command
simultaneously on multiple ports.
S1(config)#interface range fastethernet @/5-24, gigabitethernet @/1-2
S1(config-if-range)#shutdown
S1(config-if-range)#exit
11 Save the configuration on the switch.
Sl#copy running-config startup-config
12 From Rachel's PC, ping all other PCs.
Tip: Use the ipconfig command on the computer’s command prompt.


### Lab Assignments & Solutions — strona 95

Lab Task 2: Verify Port Security
Practice the use of various commands and troubleshooting to verify the integrity of port
security.
1 Run the show port-security command on the switch to verify all settings.
S1#show port-security
Sl>enable
Sl#show port-security
Secure Port MaxSecureAddr CurrentAddr SecurityViolation Security
Action
(Count) (Count) (Count)
Fa0/1 & 1 Oo
Shutdown
Fad/2 pS & o
Restrict
Fa0/3 & 1 0
Restrict
Fad/4 2 & o
Protect
sl# Vv
Ctri+F6 to exit CLI focus Copy Paste
D1 Top
Additional Show commands:
Sl#show running-config


### Lab Assignments & Solutions — strona 96

Rs = o x
Physical Config CLI Attributes
10S Command Line Interface
inlerface FaslELherneLl0/2 had
suitchport mode access
awitebport. port-security
switehport port-sccurity mac-address 00U0.9793.27C4
interface FastEthernet0/2
switchpork made access
switehport port security
switchport port-security violation rastrict
SwlLeLporl eosl-secucily mac-addsess 9008. 7096.0272
intertace FaseBthernet/3
switehport mode access
switchport port-security
switchport yort-security maximum 2
aw tehport povt-security mac-aderess sticky
switehport port security violation restrict
switchport port-security mac-address sticky 0004. 9A8B.2822
interface FastRthernet.0/4
switchport mode access
switehport port-security
Swilehporl eorl-securily maximum 2
suitchport port-security mac-address sticky
switchport port-security violation restrict
switchport port-security mac-address sticky 0008.##34.A1A0
Ctri+F6 to exit CLI focus Copy, Paste
UO tep
Sil#show port-security address


### Lab Assignments & Solutions — strona 97

id
Physical Config CLI Attibutes
10S Command Line Interface
Configured MAC Addresses + 0 A
Sticky MAC Adcresses a
Last Souzce Addcess:Vlan : 0004, 9A8B.2890:1
seaurity Violation Gount 2 @
Sl (config) #do show port-security address
Secure Mac Address Table
vian Mac Addzessitype vorts
Remaining Age
(mins)
FastRtnernat/1 a
1 anos. 786.0272 Securetontiguzed
Fastkthe=nat/2 i
1 0004. YAEB. 232 SecureSticky
Fas LRU ern 1.0/3 7
1 0005.3=34.A1A0 securesticky
rastetne=net/4 -
Max addresses limit in system (excluding one mac per port) : 1024
sl(config) § .
Ctrl+F6 to exit CL! focus: Copy Paste
U top
Sil#show port-security interface type number
Example:
Sil#show port-security interface fastethernet 0/1
Port Security : Enabled
Port Status : Secure-up
Violation Mode : Shutdown
Aging Time : @ mins
Aging Type : Absolute
SecureStatic Address Aging : Disabled
Maximum MAC Addresses gal
Total MAC Addresses g il
Configured MAC Addresses 5 al
Sticky MAC Addresses 70
Last Source Address:Vlan : 000@.0000.2000:0
Security Violation Count 2 0


### Lab Assignments & Solutions — strona 98

2 Disconnect Rachel's PC from S1. Click the Delete button 4 and then click the
item you want to delete.
eB Cisco Packet Tracer - C:\Users\mauri\OneDrive\ Desktop\revised labs\NET-04-L1.pka
File Edit Options View Tools Extensions Help
BmebRROrae BAC ’AAQOHES |
sdeas dv mee wa
[A Logical] Physical): 390, y: 254
Rogue Laptop K
teks Was Te Notices
3 Connect the rogue laptop to S1 on Fast Ethernet 0/1 using a straight-through
cable and press the time forward button.
QE) (Physical) 200 y- 274 Reo CIC Cons
Rogue Laptop
j=) Se =
Rachel Ross doey Monica
s§ulsae(s “(Visas |
ae 4
#


### Lab Assignments & Solutions — strona 99

4 Try to ping Ross’s PC from the rogue laptop.
B Rogue Laptop = a x
Physical Config Desktop Programming —_ Attributes
|
|
Rachel Ross Joey Monica


### Lab Assignments & Solutions — strona 100

5 _ Display the information regarding the Fast Ethernet 0/1 port and note that it is in
err-disabled mode.
Sl#show interface fastethernet 0/1
[ee ey
/ = OF
Rachel Ross Joay eae
SSC CISSEING OF "SHOW SNTSEESCS™ COUNTSES TEVEE
Input queue: 0/75/0/0 (size/max/drops/flushes); Total output drops: 0
Queueing strategy: fifo
Output queue :0/40 (size/max)
5 minute input rate 0 bits/sec, 0 packets/sec
5 minute output rate 0 bits/sec, 0 packets/sec
956 packets input, 193351 bytes, 0 no buffer
Received 956 broadcasts, 0 runts, 0 giants, 0 throttles
0 input errors, 0 CRC, 0 frame, 0 overrun, 0 ignored, 0 abort
0 watchdog, 0 multicast, 0 pause input
Ctrl+F6 to exit CLI focus Copy Paste
O Top
6 Reconnect Rachel’s PC to Fast Ethernet 0/1.
7 On Fast Ethernet 0/1, run the shutdown command, and then no shutdown. The
port is now back to normal.
S1(config)#interface fastethernet @/1
S1(config-if)#shutdown
S1(config-if)#no shutdown


### Lab Assignments & Solutions — strona 101

Rs i
Physical Config _CLI_ Attributes,
10S Command Line Interface
si¥ :
Sl#show interfaces fastEthernet 0/1
FastEthernet0/1 is ee toe cea
Hardware is Lance, address 15 U0U1l-cla0.as01 (ora 0U01.c7a0.a301)
BW 100000 Kbit, DLY 1000 usec,
reliability 255/255, txload 1/255, rxload 1/255
Encapsulation ARPA, loopback not set
Keepalive set (10 sec)
Full-duplex, 100Mb/s
input flow-control is off, output flow-control is off
ARP type: ARPA, ARP Timeout 04:00:00
Last input 00:00:08, output 00:00:05, output hang never
Last clearing of "show interface" counters never
Input queue: 0/75/0/0 (size/max/drops/flushes); Total output drops: 0
Queueing strategy: fifo
Output queue :0/40 (size/max)
5 minute input rate 0 bits/sec, 0 packets/sec
5 minute output rate 0 bits/sec, 0 packets/sec
956 packets input, 193351 bytes, 0 no buffer
Received 956 broadcasts, 0 runts, 0 giants, 0 throttles
Q input errors, 0 CRC, 0 frame, 0 overrun, 0 ignored, 0 abort
atchdoac 0 miitica nance inn 4
Ctrl+F6 to exit CLI focus Copy Paste
O Top


### Lab Assignments & Solutions — strona 102

AR Cisco Packet Tracer - = a x
File Edit Options View ‘Tools Extensions Help
BmePOraeALVTAQAAODEAESS 2
RQexcevmae@ Me
[A Logical] Physical] x: 595, y: 239 Root a \( a i( ay \( a \(~ 06:16:09]
y IN
Rogue Laptop J \
Rachel Ross. bey! Monica
PE LICE iavaraaeses esa
| <
Hi


### Lab Assignments & Solutions — strona 103

8 Disconnect Ross’s computer and connect the rogue laptop. Then try to ping
Rachel.
® rogue Laptop - a x

Physical Config Desktop Programming _— Attributes ;

C:\>ping 10.0.0.1

Pinging 10.0.0.1 with 32 bytes of data:

Request timed out.

Request timed out.

Request timed out.

Request timed out.

Ping statistics tor 10.0.0.1:

Pinging 10.0.0.1 with 32 bytes of data:

Request timed out.

Request timed ont.

Request timed out.

Request timed out.

Ping statistics for 10.0.0.1:

Packets: Sent = 4, Received = 0, Lost = 4 (100% loss),
(Top
Rogue Laptop S
Poon
Rachel Ross Joey Monica
Learners should note that the rogue laptop does not go red as with Rachel’s port. They should also
notice that they cannot ping Rachel’s port, either.


### Lab Assignments & Solutions — strona 104

9 Display the port security of the Fast Ethernet 0/2 port and remember that the
port security is set to one MAC address.
S1#show port-security interface fastethernet 0/2
Rsi * a x
Physical Cong _ CLI Atnbutes
10S Command Line nteriane
956 packets input, 199951 bytes, 0 ne buffer A
Roceived 956 brocGcasts, 0 rents, 0 giante, 9 throttics
9 output srrors, © Gellisions, 0” intevzace roscts
$1 (config-if}t
$1 (config-ift}#
Aging Time : 0 mins
Aging Typs + nbsolte
sticky Mic addresses 12
(Ctrl#F6 to exit CLI focus. ‘Copy Paste
(Top
Learners should notice that this port is set to only one MAC address, which is why the ping is being dropped.
10 Reconnect Ross’s computer to Fast Ethernet port 0/2 and see that you can ping
all the other computers on the network.


### Lab Assignments & Solutions — strona 105

11 Disconnect Joey’s computer and connect Fast Ethernet 0/3 to the rogue laptop.
Then ping Monica’s computer.
W Rogue Laptop = oO x
Physical Config Desktop Programming Attributes
ing statistics for 10.0.0.1: is
Packets: Sent = 4, Received = 0, Lost = 4 (100% loss),
Ping statistics for 10.0.0.3:
Packets: Sent = 4, Received 0, Lost = 4 (100% loss),
C:\>ping 10.0.0.4
Reply from 10.0.0.4: bytes=32 time=1ms TTL=128
Reply from 10.0.0.4: bytes=3Z time<lms TTL=12'
Reply from 10.0.0.4: bytes=32 time=1ms TTL=128
Reply from 10.0.0.4: bytes=32 time<lms TTL=128
ing statistics for 10.0.0.4:
Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),
Approximate round trip times in milli-seconds:
Minimem Oms, Maximum = ims, Average = Oms
O Top
L__| =
Rogue Laptop 1
Poon
Rachel Ross Joey Monica
Learners should note that the switchport security is different on the Fast Ethernet 0/3 port, which is
why the rogue laptop is able to ping. Additionally, this should initiate a conversation about the security
issues.


### Lab Assignments & Solutions — strona 106

12 Display the port security of the Fast Ethernet 0/3 port and note that the port
security is set to two MAC addresses.
S1#show port-security interface fastethernet 0/3
Bsi - a *
Physical Config _CLI__ Attributes
10S Command Line Intertace
Sl>show port-security intertace tastethernet 0/3
% invalid input detected at '*' marker
sl>enable
Sl#do show port-security interface fastethernet 0/3
& tnvaTia dnpnt detected at te marier
Slshow port-sncnvity tntertacs tastathernat 0/3
Berl Secusily 2 Enabled
Berl Slalus 2 Secure-up
Vivlal_on Mode 2 ResLeicl
Aging Time : 0 mins
Aging Type : Absolute
Securestatic Addzess Aging : Disabled
Maximum MAC Addresses 22
Toval MAC Addresses 22
Configured MAC Addresses: 0
Sticky MAC Addresses ae
Last Source Address:Vlan + 090.0026. 3cE3:1
Security violation count 1 ¢
sta Y
Ctrl+F6 to exit CLI focus Copy Paste
C1 Top
Learners should notice that this port is set to two MAC addresses.


### Lab Assignments & Solutions — strona 107

13 Now move Monica’s ethernet port to the rogue laptop (Fast Ethernet 0/4) and
Joey’s to Monica’s computer (Fast Ethernet 0/3).
Y_| _
Rogue Laptop 4
S9OoOoD
Rachel Ross Joey Monica
14 Goto Monica’s computer, open the CLI, and ping Rachel.
Learners should note that Fast Ethernet 0/3 restrict is now set, hitting the maximum of two MAC
addresses. Fast Ethernet 0/4 is in protected mode, which is dropping the ping.
® Monica - Oo x
Physical Config _Deskoy Programming Attributes
Request timed out.
C1 Top


### Lab Assignments & Solutions — strona 108

W Rogue Laptop - o x
Physical Config Desktop Pregramming Attributes
Command Prompt x
Ping statistics for 10.0.0.3: e
packets: Sent = 1, Received = 0, Lost = 4 (100 loss)
c:\ping 10.0.0.4
Pinging 10.0.0.4 with 32 bytes of data:
Roply from 10.0.0.4: bytes-32 timo-ims TrE-128
Reply from 10.0.0.4: bytes-32 time<lms ITL-128
ing statistics for 10.0.0.4:
Approximate round trip times in milli-seconds:
minimum = ms, Maximum = ims, avoraga = oms
Pinging 10.0.0.1 wilh 32 Lyles of dala:
Request timed out.
Request Lied oul.
Request timed oul
Ping statistics tor 10.0.0.1:
Packets: Sent = 4, Received = 0, Lost = 4 (100% loss),
LD Top


### Lab Assignments & Solutions — strona 109

15. Display the port security of the Fast Ethernet 0/4 port and note that the port
security is set to protect.
S1#show port-security interface fastethernet 0/4
Bs =a a x
Physical Contig _CLi_Atibutes
10S Command Line Interface
Port. Securily 7 Fratied n
port stezus 1: Secure-up
Violation Node 1 Restric
Porl Slzlus 1 Scure-up
violation Node } Drovect
aging vine 10 mins
Aging Type ? Absvlule
SecureStatic Address Aginc : Disabled
Maximun Hac addresses 2
Total MAC Addresses +
Centigurea wac adazesges 0
Ctrl+F6 to exit CLI focus Copy Paste
Oop

Learners should notice that this port is set to two MAC addresses, but that its violation mode is set to

protect.

16 To wrap up, connect the ports back to their original locations and attempt to
ping Joey and Monica again. You should notice that there are no issues with
pinging any of the other members on the LAN.


### Lab Assignments & Solutions — strona 110

& Mission Accomplished
® You protected endpoints by using port security to limit the number of MAC
address per port and filtered MAC addresses.
@ You now have an understanding of the different types of violation modes.
@ By not applying the proper port security, you have left one port vulnerable.


# NET-04-LS2 — Remote Access with SSH

> Zakres źródłowy: strony 111–123.


### Lab Assignments & Solutions — strona 111

Computer Networking
Lab Assignment Switch Security
& Solution
NET-04-LS2
Remote Access with SSH
Ped ibaa
fo} in
Ee
Copyright © 1996-2020 HackerU Ltd.
All Rights Reserved.


### Lab Assignments & Solutions — strona 112

Note: Solutions for the instructor are shown inside the green box.
<i _ ‘i
©) Lab Objective
Learn about the SSH protocol and how it can be used to securely and remotely access
network devices.
2 Lab Mission
Set up a switch with basic security and layer 3 connectivity, after enabling SSH
connections using RSA encryption, and test SSH by opening a session from a local PC.
esa .
©@) Lab Duration
30-60 minutes
fe Requirements
e Knowledge of basic IOS commands and navigation.
on

| Resources
e¢ Environment & Tools

o All platforms

o Cisco Packet Tracer 7.2.2 or later
e Extra Files

o Net-04-L2.pka


### Lab Assignments & Solutions — strona 113

' Fi
s ¢ | Tip
o © * | Refer back to NET-03-L2 for basic Cisco device configurations.
=
Instructions for PKA Lab Files
Lab material includes the lab document and a PKA lab file.
Open the pka file through the Cisco Packet Tracer menu by clicking "File", and then click
"Open...".
Cisco Packet acer _ pp
jaca 69 Q2QQ0R ese 2
rca oar aT)
OpenAcity Seavnce ee ns)
see ons SS a
Prot — Cle
Exton Lopet
29 E 480838 9SSS3SSC83S8¢
a ere ———*
Navigate to the file's location and open it.


### Lab Assignments & Solutions — strona 114

.

a A A

72, @

Bree rou

‘si

a

a

a

a

a

4

i

Filename [NETO2 pa | [Packet ace Fie ake pie™ |
Note: Double-clicking the pka file in file explorer may not work (depending on the
Packet Tracer version).
When you open a PKA file in Cisco Packet Tracer, two windows appear:
1. Lab topology window
2. Activity window
PKA Features
Note the following essential information regarding the Activity window:
1. Completion Percentage — Student progress appears at the right-bottom corner of
the window.
2. Check Result Button — When you click this button, and then click the "Assessment
Items" tab, you will find a checklist with lab objectives and status, whereby V-done, X-
not done.
Note: Both features help the instructor grade the exercise swiftly and efficiently.


### Lab Assignments & Solutions — strona 115

1B Pr pct oncon2 ee
Pease refer to the exercise document and carefully follow the =a a ia ee
‘See the percentage of completion at the right-bottom corner to a wi Server o Other
determine your progress. MP Sere Rowe ¢ oe
Note: The Optional and Bonus section ae not scored bet
Good Luck Lege ¢ cee
o A oe
See ran ¢ ote
Settee nema oe
a syaodeace A oe
Sir altesss ¢ ote
PKA Solution
To view the solution or edit the lab file, you can click the "Wizard hat" icon and enter
the following password: C!ScOM@ster
Right-click the "Answer network" tab, and then click "Show Answer network".
Note: Be careful not to change anything so that the lab will remain intact.


### Lab Assignments & Solutions — strona 116

Lab Task 1: Configure SSH
Set basic switch configurations, assign the switch an IPv4 address, and enable SSH to
connect to the switch with RSA encryption.
All the required commands were introduced in the presentation, and are also found in
the textbook.
10.0.0.0/24
R1
rr
Admin PC a
Part 1: Initial access and settings:
1 Using aconsole cable, connect to $1 and the terminal software.
&S
Ri
tooo
3rd
s9mgmel Ve Sas
a 2nd
rs] Ast «
E | tt __§_—__


### Lab Assignments & Solutions — strona 117

2 Set $1 as the switch's device name.
Switch>enable
Switch#configure terminal
Enter configuration commands, one per line. End with CNTL/Z.
Switch(config)#hostname S1
S1(config)#
3 Create a user account:
Username: Admin
Password: p@nd@
S1(config)#username Admin password p@nd@
4 Set the enable password to c!scO
S1(config)#enable password c!sc@
Encrypt all passwords on the device.
S1(config)#service password-encryption
5 Setan appropriate security message (Banner):
Access to this device is for authorized personnel only!
S1(config)#banner motd #Access to this device is for authorized personnel only!#
6 Set CyberPro.com as the device domain.
S1(config)#ip domain-name CyberPro.com
Part 2: Enable layer 3 connectivity on the switch
1 Enable interface VLAN1, configure it with the address 10.0.0.150 255.255.255.0
and turn on the interface using no shutdown.
S1(config)#interface vlan 1
S1(config-if)#ip address 10.0.0.15@ 255.255.255.0
S1(config-if)#no shutdown
2 Set the switch’s default gateway address to 10.0.0.1
S1(config)#ip default-gateway 10.0.0.1


### Lab Assignments & Solutions — strona 118

3 Exit the terminal window on the Admin PC, go to the command prompt, and test
connectivity to the switch using the Ping command.
C:\>ping 10.0.0.150
Pinging 10.0.0.150 with 32 bytes of data:
Reply from 10.0.0.150: bytes=32 time<lms TTL=255
Reply from 10.0.0.150: bytes=32 time<lms TTL=255
Reply from 10.0.0.150: bytes=32 time<lms TTL=255
Reply from 10.0.0.150: bytes=32 time<lms TTL=255
Ping statistics for 10.0.0.150:
Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),
Approximate round trip times in milli-seconds:
Minimum = Oms, Maximum = Oms, Average = Oms
Part 3: Permit remote access to the device
1. Go back to the terminal on the Admin PC and enter the line vty mode (channels
Oto 15).
S1(config)#line vty @ 15
S1(config-line)#
2 Configure line vty for local password checking, using the command login local.
S1(config-line)# login local
3 Set the line to display the banner when accessing the switch remotely, using the
command motd-banner.
S1(config-line)# motd-banner
4 Allow only SSH connection requests to the switch.
Sl{config-line)¢transport input ssh
S1(config-line) fexit
Sl (config) #| Lg
C1 top


### Lab Assignments & Solutions — strona 119

S1(config-line)# transport input ssh
S1(config-line)# exit
5 RSA uses two types of keys, name them and their functions.
Public Key — Encrypts data, Private key - Decrypts secure data
Part 4: Configure SSH
1 Generate the RSA keys for the SSH process, with a key length of 1024 bits, via
the switch privileged exec mode.
S1(config)#crypto key generate rsa
$1 (config) #
Sl(config)#crypto key generate rsa
The name for the keys will be: 51.Cyberpro.com
Choose the size of the key modulus in the range of 360 to 2048
for your
General Purpose Keys. Choosing a key modulus greater than 512
may take
a few minutes.
How many bits in the modulus [512]: 1024
% Generating 1024 bit RSA keys, keys will be non-exportable...
Sl (contig) # be
1 Top
2 Set the SSH version to 2, using the command ip ssh version 2.
S1(config)#ip ssh version 2
S1(config)#exit
3. What is the maximum key length in RSA?
2048


### Lab Assignments & Solutions — strona 120

Lab Task 2: Verify SSH Configuration
Practice troubleshooting commands and techniques for SSH.
Part 5: Verify settings in S1
1 Make sure all settings are correct, using the following Show commands:
a. Show ip ssh (via the privileged exec mode)
bell


### Lab Assignments & Solutions — strona 121

b. Show running-config
Sl#show running-config
Building configuration...
Current configuration : 1370 bytes
q
version 12.2
no service timestamps log datetime msec
no service timestamps debug datetime msec
service password-encryption
,
hostname 51
!
enable password 7 08220D5D0A49
1
:
ip domain-name Cyberpro.com
|.
username Admin privilege 1 password 7 08316C400D39
!
1
1
spanning-tree mode pvst
spanning-tree extend system-id
x
--More-—
interface Vlanl
ap address 10.0.0.150 255.255.255.090
!
ip default-gateway 10.0.0.1
banner motd “CAccess to this device is for authorized personnel
only!*C
!
:
!
line con 0
1
line vty 0 4
login local
transport input ssh
ine vty 5 15
login local
transport input ssh


### Lab Assignments & Solutions — strona 122

2 > Which IOS show command displays active SSH connections on the device?
Part 6: Establish an SSH session
1 Close the terminal window, disconnect the console cable, and open the
command prompt window.
<R Admin PC - ao x
Physical Conig Desktop Progamming Attibutes
e = a
O tp
roonas =


### Lab Assignments & Solutions — strona 123

2 Connect to the switch using SSH, as follows:
ssh -] <username><target-ip>

C:\>ssh -1 Admin 10.0.0.150
Password:
Access to this device is for authorized personnel only!
S1>enable
Password:
S1#

3 InS1, start a second SSH session to R1.

Note: R1 is preconfigured with all the necessary settings. Login credentials are
the same as for S1.

C:\>ssh -1 Admin 10.0.0.1
Password:
Access to this device is for authorized personnel only!
R1>enable
Password:
R1l#

4 Which TCP port protocols do SSH and Telnet use?

Telnet: 23, SSH: 22
5 Which encryption method and type does SSH use?
RSA, Asymmetric Encryption


# NET-05-LS1 — Converting Decimal, Binary, and Hex

> Zakres źródłowy: strony 124–130.


### Lab Assignments & Solutions — strona 124

Computer Networking
Lab Assignment IP & Routing
& Solution Concepts
°. an NET-05-LS1
al U Converting Decimal,
Binary, and Hex
Copyright © 1996-2020 HackerU Ltd.
All Rights Reserved.


### Lab Assignments & Solutions — strona 125

Note: Solutions for the instructor are shown inside the green box.
@ Lab Objective
Understand the difference between binary, decimal, and hexadecimal number systems
and how to convert values among them.
4 Lab Mission
Use practice questions to evaluate and convert values among the numbering systems.
esa 7
©) Lab Duration
30-45 minutes
fe Requirements
e@ Basic understanding of the decimal (base 10) numbering system.
e Basic understanding of the hexadecimal (base 16) numbering system.
e@ Basic understanding of the binary (base 2) numbering system.
oo
| Resources
e Environment & Tools
o Optional: Calculator


### Lab Assignments & Solutions — strona 126

Lab Task 1: Decimal and Binary
Understand how decimal numbering relates to binary.
Part 1: Convert Decimal to Binary
1. Which mathematical base does the binary system use, and which digits represent
it?
Base 2, two digits: 0 and 1
2 Whatisa bit?
A bit (binary digit) is the smallest unit of data in a computer. A bit has a single binary
value, either 0 or 1.
3. Whatis an octet?
8-bit string (IPv4 consists of four octets).
4 Convert the following decimal digits to a binary octet.
Pe joys ts fe fe fe fe
aE
Example: 56 in binary octet:
a) 26
b) 65
c) 91
d) 151
e) 168
f) 192
g) 254
26 = 00011010


### Lab Assignments & Solutions — strona 127

65 = 01000001
91 = 01011011
151 = 10010111
168 = 10101000
192 = 11000000
254 = 11111110
Part 2: Convert Binary to Decimal
5 Convert the following IPv4 binary octets to decimal digits:
Example: 00000010 in decimal is 2.
a) 00000111
b) 00010010
c) 00101110
d) 01011111
e) 10010010
f) 11011110
g) 11111111
a. 7
b. 18
c. 46
d. 95
e. 146
£222
g. 255
6 Bonus: Convert the following IPv4 addresses to their binary equivalents:
Example: 10.0.0.5 is actually a long 32-bit string.
[oe inary
10.0.0.5 | 00001010.00000000.00000000.00000101


### Lab Assignments & Solutions — strona 128

a) 172.16.10.2
b) 192.168.1.1
c) 8.8.8.8
a. 172.16.10.2 = 10101100.00010000.00001010.00000010
b. 192.168.1.1 = 11000000.10101000.0000001.0000001
c. 8.8.8.8 = 00001000.00001000.00001000.00001000


### Lab Assignments & Solutions — strona 129

Lab Task 2: Binary and Hexadecimal
Understand how binary relates to hexadecimal numbering.
Part 1: Convert Binary to Hex
1 Which mathematical base does the hexadecimal system use, and which digits
represent it?
Base 16, 10 digits and 6 characters: 0-9, A, B, C, D, E, F
2 Convert the following binary nibbles (half-bytes) to hex digits:
Example: 1010 is A
a) 0010
b) 1101
c) 0110
d) 1100
e) 1000
f) 1011
g) 0000
h) 1110
i) 1111
a. 2
b. D
c. 6
dc
e. 8
f. B
g. O
h. E
i. F


### Lab Assignments & Solutions — strona 130

Part 2: Convert Hex to Binary
3 The following is a random physical address of 12 decimal digits (MAC).
Convert the hexadecimal digits to binary digits:
Example: 00-B1-17-C2-A2-EE is represented in binary as follows:
Px a
|B [af] [2/o/e fol
7 [ofoe tafe] fala
| [2[{o[ofo]e|ato
[#2 [2/0] [o//e/alo
eer
a) B3-00-13-A1-02-3E
[Hex| Binary
[83 [1] o[1{1folofa) 4)
[00 [oj ofofofolafojo|
|.13 [ol ofo[1]olo} 1) 4/
[az [1/0/21 [olololo|.|
[02 [o|ofofofololso|
L3e [ofofa|1]1]2[1]o]
b) 04-01-0A-DD-CC-FF
[Hex[ Binary |
[04 [ol ofofofol1fofo|
[01 [ol ofofofolofojs|
[oa [ol ofofolslofajo|
[po [1/10] 11/10] 4]
[cc [1] 1{ofo]1[1]o/o|


# NET-05-LS2 — IPv4 and Initial Router Configuration

> Zakres źródłowy: strony 131–147.


### Lab Assignments & Solutions — strona 131

Computer Networking
Lab Assignment IP & Routing
& Solution Concepts
RO isis, NET-O5-LS2
olF IPv4 and Initial Router
i U Configuration
Copyright © 1996-2021 HackerU Ltd.
All Rights Reserved.


### Lab Assignments & Solutions — strona 132

Note: Solutions for the instructor are shown in the green box.
G Lab Objective
Learn how to configure the initial setup of a router and how |Pv4 addressing is used to
communicate between networks.
* Lab Mission
Set IPv4 addresses in the initial router configuration, and the addresses of all devices on
each LAN. Practice using IPv4 to route traffic within a WAN and connecting to the wider
internet.
Note: All required commands were introduced in the presentation and can also be
found in the textbook.
ea .
©) Lab Duration
30-60 minutes
fe Requirements
e Knowledge of basic IOS commands and navigation
e Knowledge of IPv6
os

| Resources
e Environment & Tools

o All platforms

© Cisco Packet Tracer 7.2.2
e Files

© NET-05-L2.pka


### Lab Assignments & Solutions — strona 133

Instructions for PKA Lab Files
Lab material includes the lab document and a PKA lab file.
Open the PKA file through the Cisco Packet Tracer menu by clicking File and Open...
WF Cisco Packet Tacer ; - ao x
Be ar. AQQQacmESs 2
Tees a A |
Open Aci Seance ae es)
a see ons Se
Prot Clee
ert m je: (Sasa To Dig and Diop To Woe :
Navigate to the file's location and open it.
a
a A 4)
a or
BB Seronage Stross
a
a
a
a
a
a
i
i
‘ Fearne [eS oka [Poet Fe Gotan.)


### Lab Assignments & Solutions — strona 134

Note: Double-clicking the PKA file in File Explorer may not work (depending on the
Packet Tracer version).
Lab material includes the lab document and a PKA lab file. When you open a PKA file in
Cisco Packet Tracer, two windows appear:

1. Lab topology window

2. Activity window
PKA Features
Note the following essential information regarding the Activity window:

1. Completion Percentage: Student progress appears at the bottom right corner of
the window.

2. Check Result Button: When you click this button and then click the Assessment
Items tab, you will find a checklist with lab objectives and status, whereby
V=done, X=not done.

Note: Both features help the instructor grade the exercise swiftly and efficiently.
Please refer to the exercise document and carefully follow the [Assessment Reme ‘Status Points Component(s) | Feedback
feoinons teat
‘See the percentage of completion at the right-bottom corner to NTP Server o ‘Other
determine your progress, FES 3 ote
Note: The Optional and Bonus section are not scored, Lao rears ‘ ss
Good Luck is ° Or

PKA Solution

To view the solution or edit the lab file, you can simply click the wizard hat icon and

enter the following password: C!ScOM@ster

Right-click the Answer network tab and then click Show Answer network.

Note: Be careful not to change anything so the lab will remain intact.


### Lab Assignments & Solutions — strona 135

Lab Task 1: Initial Router Configuration
Connect the router to local switches and secure it with login credentials.
Issue all commands on R1.
Note: Router IOS is similar to Switch IOS.
Part 1: Connect R1 to Switches
1 Using a straight-through cable, connect R1 gigabitEthernet 0/0 to gigabitEthernet
0/1, on S1.
(DD FastEthemetoi20
B FastEthernet0/21 =
[DD FastEthemetoi23 ath
FastEthernet0/24
eet oe LESS!
IgabitmemnetOr /\ 10.0.0.0/24
«
PE] el F[Oh 4 Fs aisiAdv
es | 2nd
] Ast e


### Lab Assignments & Solutions — strona 136

2 Using a straight-through cable, connect R1 gigabitEthernet 0/1 to
gigabitEthernet 0/1, on 82.
BD Festtiveneion9
Rt [Dy Fastethemetoe2
[Di Fastethemetor2a
4th mn
oOo 22 } =)
Usert User User3 Userd
le —.
2duile° Fj aS) AARBREHAA
2nd
| a Ast 3
a
Part 2: Initial Settings on R1
3 Click R1, click the CLI tab, and enter global configuration mode.
Router>enable
Router#configure terminal
4 Set the device name to R1.
Router (config)#hostname R1
R1(config)#
5 Create a user account: Username: Admin, Password: p@nd@
R1(config)#username Admin password p@nd@
6 Set enable password to c!scO
R1(config)#enable password c!sc®


### Lab Assignments & Solutions — strona 137

7 Set an appropriate security message (banner):
Access to this device is for authorized personnel only!
R1(config)#banner motd #Access to this device is for authorized personnel
only!#
8 Encrypt all passwords on the device.
R1(config)#service password-encryption
9 Secure access to the console port by enabling username and password
authentication on the port.
R1(config)#line console @
R1(config-line)#login local
R1(config-line)#exit
R1(config)#exit
10 Verify and save settings. Press Enter and do not write anything after the
question mark.
Rl#show running-config
Rl#copy running-config startup-config
Destination Filename [startup-config]?


### Lab Assignments & Solutions — strona 138

Lab Task 2: Configure IPv4
Assign IPv4 addresses to the router and establish connections with the LANs.
Part 1: Review Questions
1 How many bits are in an IP or subnet mask address?
2 What is the purpose of IPv4 Class D?
Class D IP range is reserved for multicast communications.

3. What is the difference between a public IP address and a private IP address?
Private addresses are only allowed on the LAN and are used to represent internal
hosts. Public addresses are unique, only allowed on the internet, and are used to
represent large networks (AS).

4 What is the difference between an IPv4 unicast message and an IPv4 broadcast

message?
A unicast message only has a single destination, while a broadcast message is sent to
the entire broadcast domain (all devices on the same network).

5 What are the three IP address ranges used in private networks?
In accordance with RFC1918, the following ranges are assigned to private networks:
10.0.0.0—10.255.255.255
172.16.0.0-172.31.255.255
192.168.0.0-192.168.255.255

6 Whatis a suffix?
A suffix is a decimal method of displaying a subnet mask based on bits.
For example: /8 > 255.0.0.0


### Lab Assignments & Solutions — strona 139

7 What is a default gateway address?

From the host perspective, the default getaway is the address of the router that routes
traffic to other networks.

8 Based on which two items of information does a router make routing decisions?

Based on the destination packet IP and the routing table.
Part 2: Configure IPv4 on R1 Interfaces:
Issue all commands on R1.
9 InR1, enter global configuration.
R1>enable
Password:
Rl#configure terminal
R1(config)#

10 Enter interface gigabitEthernet 0/0, configure the IP address 192.168.0.1, and
configure the appropriate subnet mask: 255.255.255.0. Then enable the
interface.

R1(config)#interface gigabitethernet 0/0
R1(config-if)#ip address 192.168.0.1 255.255.255.080
R1(config-if)#no shutdown

R1(config-if)#exit

11 Repeat the previous step for gigabitEthernet 0/1 with the IP address 10.0.0.1/24

and enable the interface.
R1l(config)#interface gigabitethernet 0/1
R1(config-if)#ip address 10.0.0.1 255.255.255.0
R1(config-if)#no shutdown
R1(config-if)#exit


### Lab Assignments & Solutions — strona 140

Part 3: Verify Interface Settings
12 Stay in global configuration mode. Note: The do command enables the privileged
mode command in global configuration mode. It does not support the
autocomplete feature.
13 Verify the status and IP configuration, using do show ip interface brief
Note: Disregard Giga 0/0/0, which is preconfigured.
R1(config)#do show ip interface brief
R1 (config) #
R1(config)#do show ip interface brief
Intexface IP-address OK? Method status
Protocol
GigabitEthernet0/0 192.168.0.1 YES manual up
up
GigabitEthernet0/1 10.0.0.1 YES manual up
ue
GigabitEthernet0/0/O 7.7.7.1 YES manual up
up
Viani unassigned YES unset
administratively down down
R1 (config) #| v
14 Display the routing table using do show ip route
Gateway of last resort ig 7.7.7.2 to network 9.0.0.0
7.0.0.0/8 ig variably submetted, 2 subnets, 2 masks
c 7.7.7.0/30 ig directly conmected, GigabitEthernet0/0/0
L 7.7.7.1/32 is directly connected, GigabitEthernet0/0/0
TTT TE GITecery CeMnected, CIdan ee TneEneey
L 192.168.0.1/32 is directly connected, GigabitEthernet0/0
a 0.0.0.0/0 [1/0] via 7.7.7.2
R1 (config) # v
15. What do the letters C and L represent in the routing table?
C= Directly connected network
L = Local interface IP address


### Lab Assignments & Solutions — strona 141

16 Save the configuration. Press Enter and do not write anything after the question
mark.
R1(config)#exit
Rl#copy running-config startup-config
Destination Filename [startup-config]?
Part 4: Configure IPs on the User PCs
17 Click User1 and then the Desktop tab.
18 Click the /P Configuration icon.
e _
Physical Config Desktop. Programming Altibuies
S—a G IPv4 IPv6
Oop
19 InUser1, configure the IP address 192.168.0.2/24.
20 In User1, configure the default gateway address, which is the IP address of the
router's interface connected to the same network.


### Lab Assignments & Solutions — strona 142

® Usert - a x]
Physical Confg Desig Progamming _Anntee
Waeteco —_(Fesithona :
F Contgutan
© oxcp @ Static
IP Aahess 20902
Stn! Mask |
Dat Steuay |
ONS Sener |
21 In User2, configure the IP address 192.168.0.3/24.
22 In User2, configure the default gateway address.
R User2 - og x
Psi Corba _ Dasiop Prostanning tious
ect Ct‘CS
Wierace (Fathom 5
congutn
© bHcP © Static
PAdtess ezien03
Subnet Mask 562580
Dal Gateway ve2c001
ONS Sever 0000


### Lab Assignments & Solutions — strona 143

23° Enter the command prompt and use ipconfig to verify settings for both User1
and User2.
phys Cov] Geskion Phowainning Albiitee _
el al
DN fsen er
ae — a [reve | [Ive |
tee
Packet Tracer PC Command Line 1.0
c:\>ipconfig
FastEthernet0 Connection: (default port)
Link-local IPv6 Address.........! FE80::230:A3FF: FE75:ED22
SUBNCE: MASK or ce nvceececwenenenwet 2-2 oe tnoO
Default Gateway.........e2.ee2+2-! 192.168.0.1


### Lab Assignments & Solutions — strona 144

24 Repeat steps 17 through 23 for User3 and User4. In User3, set the IP address
10.0.0.2/24. |n User4, set the IP address 10.0.0.3/24. In both computers, set the
default gateway address, which is the IP address of the router's interface
connected to the same network.

| Users - oo x
|
(Pcomigeatn
| Omer © ome
IP Addvoss [to0.02
Suboet Mas (zssane 2580
| ort comay fiooot
DNS Sever {nooo
R Users - Oo x
waetace (Fastenal E
contain
© ouep @ Static
PAdose ja003 |
‘Subnet Mask 255. 256.256.0 |
Default Gateway 40004 1
DNS Sener |
Part 5: Verify Connectivity
25 On the User1 desktop, click the Command Prompt icon.
26 Use ipconfig to verify network settings.
Packet Tracer PC Command Line 1.0
C:\>ipconfig
FastEthernet0 Connection: (default port)
Link-local IPv6 Address.........: FE80::230:A3FF: FE75:ED22
Subnet Masks: 2600s cose eiecia wat 2956255.255.0
Default Gateway. .......eeeeeeee-! 192.168.0.1


### Lab Assignments & Solutions — strona 145

27 Ping its default gateway to make sure there is connectivity with the router.
Packet Tracer PC Command Line 1.0
Ic:\>ping 192.168.0.1
Pinging 192.168.0.1 with 32 bytes of data:
Reply from 192.168.0.1: bytes=32 time=2ms TTI=255
Reply from 192.168.0.1: bytes=32 time=5ms TTL=255
Reply from 192.168.0.1: bytes=32 time=12ms TTL=255
Reply from 192.168.0.1: bytes=32 time=llms TTL=255
Ping statistics for 192.168.0.1:
Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),
‘Approximate round trip times in milli-seconds:
Minimum = 2ms, Maximum = 12ms, Average = 7ms
28 Ping User2, User3, and User4 to verify connectivity with all hosts on the internal
and adjacent networks.
c:\ ping 16.0.0.2
Pinging 10.0.0.2 with 32 bytes of data:
Reply from 10.0.0.2: bytes=32 time=lms TTL=127
Reply from 10.0.0.2: bytes=32 time<lms TTL=127
Reply from 10.0.0.2: bytes=32 time<lms TTL=127
Reply from 10.0.0.2: bytes=32 time<lms TTL=127
Ping statistics for 10.0.0.2:
Packets: Sent = 4, Received = 4, Lost = 6 (0% loss),
Approximate round trip times in milli-seconds:
Minimum = Oms, Maximum = lms, Average = Oms

chp}

Ping 192.168.0.3

Ping 10.0.0.3

Ping 10.0.0.2


### Lab Assignments & Solutions — strona 146

29 Ping 8.8.8.8 to verify internet connectivity.
C:\>ping 8.8.8.8
Pinging 8.8.8.8 with 32 bytes of data:
Reply from 8.8.8.8: bytes=32 time<lms TIL=254
Reply from $.8.5.8: bytes=32 time<lms TIL=254
Reply from &.8.8.8: bytes=32 time<lms TIL=254
Reply from §.8.5.8: bytes=32 time<lms TIL=254
Ping statistics for §.8.8.8:
Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),
Approximate round trip times in milli-seconds:
Minimum = Oms, Maximum = Oms, Average = Oms
Csi>
Part 6 (Bonus): Set IPs and the Default Gateway on the Switches
30 Click $1 and then click the CLI tab.
31 Enter interface vlan 1 configuration mode.
S$1>enable
S1#configure terminal
S1(config)#interface vlan 1
S1(config-if)#
32 InS1, for vlan 1, configure the IP address 192.168.0.4/24. Remember to enable
the interface.
S1(config-if)#ip address 192.168.0.4 255.255.255.080
S1(config-if)#no shutdown
S1(config-if)#exit


### Lab Assignments & Solutions — strona 147

33 InS1, set the default gateway to 192.168.0.1.
$1 (config) #
Sl(config)#ip default-gateway 192.168.0.1
51 (config) #exit
Sif
$SY¥S-S-CONFIG I: Configured from console by console
Slt ¥
S1(config)#ip default-gateway 192.168.0.1
S1(config)#exit
34 Enter the privileged mode and ping R1 to check connectivity.
S1#ping 192.168.0.1
Type escape sequence to abort.
Sending 5, 100-byte ICMP Echos to 192.168.0.1, timeout is 2
seconds:
round-trip min/avg/max = 0/0/0
Slt he
Sl#ping 192.168.0.1
35 Repeat steps 30-35 for S2 with IP address 10.0.0.4/24 and default gateway
10.0.0.1.
S$2(config)#interface vlan1
S2(config-if)#ip address 10.0.0.4 255.255.255.080
S2(config-if)#no shutdown
S$2(config-if)#exit
S2(config)#ip default-gateway 10.0.0.1


# NET-05-LS3 — Configure IPv6 Addressing

> Zakres źródłowy: strony 148–160.


### Lab Assignments & Solutions — strona 148

Computer Networking
Lab Assignment IP & Routing
& Solution Concepts
RO isis, NET-05-LS3
ol Configure IPv6 Addressing
Es}
Copyright © 1996-2020 HackerU Ltd.
All Rights Reserved.


### Lab Assignments & Solutions — strona 149

Note: Solutions for the instructor are shown inside the green box.
G Lab Objective
Become familiar with IPv6 addressing and how to configure a network to use IPv6.
%) Lab Mission
Configure a router to connect two LANs using IPv6 addresses, then use troubleshooting
techniques to verify connectivity.
Note: All the required commands were introduced in the presentation, and can also be
found in the textbook.
C2 7
@) Lab Duration
30-60 minutes
fe Requirements
e Knowledge of basic IOS commands and navigation.
e Knowledge of IPv6.
Lt

[ea] Resources
¢ Environment & Tools

All platforms

Cisco Packet Tracer 7.2.2 or higher
e Files

NET-05-L3.pka


### Lab Assignments & Solutions — strona 150

Instructions for PKA Lab Files
Lab material includes the lab document and a PKA lab file.
Open the pka file through the Cisco Packet Tracer menu by clicking "File", and then
"Open...".
bw ae 2 QQQ0R Ese 2
Bran ome ore)
Open Acti Seance ae 04039)
Print CuleP
ed
Navigate to the file's location and open it.
a
a A t)
a
a
a
-
a
i
i
1
lena [NE-03 La Se


### Lab Assignments & Solutions — strona 151

Note: Double-clicking the pka file in your file explorer may not work (depending on the
Packet Tracer version).
Lab material includes the lab document and a PKA lab file.
When you open a PKA file in Cisco Packet Tracer, two windows appear:
1. Lab topology window
2. Activity window
PKA Features
Note the following essential information regarding the Activity window:
1. Completion Percentage — Student progress appears at the bottom right corner of
the window.
2. Check Result Button — When you click this button and then click the "Assessment
Items" tab, you will find a checklist with lab objectives and status, whereby V=done,
X=not done.
Note: Both features help the instructor grade the exercise swiftly and efficiently.

reas refer to the exercise document and carefully folow the aes = fae ca ee

‘See the percentage of completion at the right-bottom corner to = NTP Sener 0 Other

determine your rome, 2 NP See H ote

Note: The Optional and Bonus section are not scored. cet Smee Incamet 1 »
PKA Solution
To view the solution or edit the lab file, you can simply click the "Wizard hat" icon and
enter the following password: C!ScOM@ster
Right-click the "Answer network" tab, and then click "Show Answer network".
Note: Be careful not to change anything so that the lab will remain intact.


### Lab Assignments & Solutions — strona 152

Lab Task 1: IPv6 Revision Questions
Refresh you IPv6 skills with practice questions.

1 = Howlong is an IPv6 address in bits?
128 bits.

2 What is the corresponding IPv6 term for an IPv4 octet?

3 Name two IPv6 Unicast address types.
IPv6 Unicast types:
Global Unicast (the equivalent of an IPv4 public address).
Link-local FE80::/10 (the equivalent of an IPv4 APIPA address).
Loopback ::1/128 (the equivalent of an IPv4 loopback address).
Unique-local FCO0::/7 (the equivalent of an IPv4 private address).

4 What is the default suffix of an IPv6 address?

5 What are the three parts of an IPv6 with a suffix of /64?
The three parts are:
First 45 bits (3 Hextets) - Global routing prefix, global identifier.
First 16 bits (1 Hextet) - Subnet ID, network identifier.
Last 64 bits (4 Hextets) - Interface ID, host identifier.

Page5


### Lab Assignments & Solutions — strona 153

Lab Task 2: Configure IPv6
Establish a functional network using only IPv6 addressing.
Issue all commands on R1:
Part 1: Configure IPv6 Unicast Global address on R11 interfaces:
1 InR1, enter Global Configuration mode.
R1>enable
Rl#config terminal
R1(config)#
2 |Pv6is installed on every router, but not enabled by default. The ipv6 unicast-
routing command must be run to enable IPv6 packet forwarding on R1.
Note: In IPv6, all addresses are valid for configuration, including the first and last
addresses, unlike in IPv4.
R1(config)#ipv6 unicast-routing
3 Enter interface gigabitEthernet 0/0 and configure the first IP address in the range
(2001:CAFE:ABCD:1::) with a suffix of 64, according to the IP documentation in
the topology.
R1(config)#interface gigabitethernet 0/0
R1(config-if)#ipv6é address 2001:cafe:abcd:1::/64
R1(config-if)#exit
R1(config)#


### Lab Assignments & Solutions — strona 154

4 Repeat the previous step for gigabitEthernet 0/1 with the corresponding
network (2001:CAFE:ABCD:2::), also using suffix 64.
R1l(config)#interface gigabitethernet 0/1
R1(config-if)#ipv6 address 2001:cafe:abcd:2::/64
R1(config-if)#exit
R1(config)#
5 Enable both interfaces.
R1(config)#interface range gigabitethernet 0/0-1
R1(config-if-range)#no shutdown
R1(config-if-range)#exit
R1(config)#exit
6 Verify the R1 interface using show ipv6 interface brief.
Note: All Cisco commands that contain “IP” relate to IPv4. There are different
commands for IPv6.
Rl#show ipv6 interface brief
Ri¢show ipvé interface brief
GigabitEthernet6/0 {up/up]
FE&0: :203:E4FF: FESB:3456
2001:CAFE:ABCD:1::
GigabitEthernet6/1 {up/up]
FES80: :201:C9FF:FESS:1B97
2001:CAFE:ABCD:2::
Vlanl [administratively down/down]
unassigned
R1#| nd


### Lab Assignments & Solutions — strona 155

Part 2: Configure IPv6 on User PCs and Verify Connectivity
7 Click User1, and then click the Desktop tab.
8 Click the IP configuration icon.
9 Configure the IPv6 address 2001:CAFE:ABCD:1::1 with a suffix of 64.
Note: Leave the link local address as is.
10 Configure the default gateway address of the network.
Physical —Conig_Desitop_ Progamming _Atitutes
TP Contguraion
© pHer @ Static
Padres
Sabre Mask i
Dea Gaeny foo CCS
IP Corfgaton
© pxcp O Auto Config @ Sialic
Ps Adress fmoredeaet? SSS
AE DNS Sener
11 Configure the IPv6 address 2001:CAFE:ABCD:1::2 with a suffix of 64. In addition,
configure the appropriate default gateway address.
Note: Leave the link local address as is.
User2
IPV6 Configuration
© pxcp © Auto Contig @ Static
Pw Address [povtceeateet2 S™~CS~SSCSCS*«dS
Ling Local Adcress [Feezovcerrreszee 2 OOSO~<—~sSsSY
Py Gateway
PW DNS Sener (


### Lab Assignments & Solutions — strona 156

12 Repeat steps 8 to 10 for User3 and User4.
For User3, configure the IPv6 address 2001:CAFE:ABCD:2::1
For User4, configure the IPv6 address 2001:CAFE:ABCD:2::2
For both User3 and User4, set the appropriate default gateway and leave the
link local address as is.
User3
Fr Corton
) DHCP © Auto Config @ Static
Preaddoss 2
Link Local Adress [Few-aotwrresoaas
1PA6 Gateway [2o0ricafe.abed 2
V6 ONS Sonor CO]
User4
1x6 Contuaton
IP Akiess EC
16 Gateway Boies etese
(PW ONS Sener Cr
13 Ping the default gateway to make sure there is connectivity with the router.
User1 to default gateway (giga 0/0)
Pinging 2001:cafe:abed:1:: with 32 bytes of data:
Reply from 2001:CAFE:ABCD:1::: bytes=32 time<lms TTL=255
Ping statistics for 2001:CAFE:ABCD:1:::
Minimum — Oms, Maximum — Ims, Average - oms
14 Ping User2 to verify connectivity on the internal network.
User1 to User2
c:\>ping 2001:cafe:abed:1::2
Reply from 2001:CAFE:ABCD:1::2: bytes=32 time<lms TTL=128
Reply from 2001:CAFE:ABCD:1::2: bytes-32 time-Ims TTL=128
Ping statistics for 2001:CAFE:ABCD:1::2:
Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),


### Lab Assignments & Solutions — strona 157

15 Repeat steps 13 and 14 for User3, so it will ping its default gateway and User4.
User3 to default gateway (giga 0/1)
c:\>ping 2001:cafe:abcd:23:
Pinging 2001:caferabed:2:: with 32 bytes of data:
ping statistics for 2001:CAFE:ABCD:2:::
Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),
Approximate round trip times in milli-seconds:
User3 to User4
Reply from 2001:CAFE:ABCD:2::2: bytes=32 time=Ims TTL=128
Reply from 2001:CAFE:ABCD:2::2: bytes=32 time<lms TTL=128
Reply from 2001:CAFE:ABCD:2::2: bytes=32 time<lms TTL=128
Reply from 2001:CAFE:ABCD:2::2: bytes=32 time<lms TTL=128
Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),
16 Ping User3 from User1 to verify connectivity between the networks.
Note: Don’t use the envelope tool, since it does not work properly with IPv6.
User1 to User3
approximate round trip times in milli~seconds:


### Lab Assignments & Solutions — strona 158

Part 3 (Optional): Configure IPv6 Link-local Address on R1 Interfaces and PCs
Except for the IPv6 global address, devices using IPv6 need IPv6 link-local addresses.
Devices use this kind of address to communicate with other hosts on the local network
segment only, and must be unique only for that particular network segment. The link-
local address is assigned automatically using a random or EUI-64 process, meaning they
are long and not easy to remember. A technician can assign a simpler address
manually.
17 Configure the FE80::1 link-local address on both interfaces of R1. The command
to use is ipv6 address fe80::1 link local
Verify the configuration with the command show ipv6 interface brief
R1(config)#interface gigabitethernet 0/0
R1(config-if)#ipv6 address fe8@::1 link-local
R1(config-if)#exit
R1l(config)#interface gigabitethernet 0/1
R1(config-if)#ipv6 address fe8@::1 link-local
R1(config-if)#exit
R1(config)#exit
Rl#show ipv6 interface brief
Rl#show ipv6é interface brief
GigabitEthernet0/0 (up/up]
a TCA tABCD:1::
Giggp berneto/1 (up/up]
2001:CAFE:ABCD:2::
Vlanl [administratively down/down]
unassigned
18 Configure the FE80::2 link-local address on User1.


### Lab Assignments & Solutions — strona 159

19 Configure the FE80::3 link-local address on User2.
|Pv6 Configuration
© pHcP O Auto Config ® Static
Pas Address foorcarenscot2 =i —id
Link Local Address
a6 Gateway [oorcareaccot; SS~S~S~S~™d:
Pv DNS Server |
20 Repeat steps 18 and 19 on User3 and User4.
For User3, set the IPv6 address FE80::2
For User4, set the IPv6 address FE80::3
IPv6 Configuration
© bHeP © Auto Config @ Static
IPv6 Address [2001:CAFE-ABCD:2::1 | 1 [64 ]
Link Local Address [FE80::2 ]
IPv6 Gateway '2001:CAFE:ABCD:2: |
IPv6 DNS Server
IPv6 Configuration
© DHeP © Auto Config @ Static
IPA6 Adress foorcareanco22 —=«di (eid
Link Local Address FE80:-3
IPv6 Gateway |2001:CAFE:ABCD:2:
IPv6 DNS Server
21 From User1, ping the default gateway and User2 link-local addresses to verify
connectivity.
Userl to default gateway
Pinging feg0::1 with 32 bytes of data:
Reply from FE80::1: bytes=32 time=Ims TTI=255
Reply from FE80::1: bytes=32 time<lms TTI=255
Reply from FE80::1: bytes=32 time<Ims TTL=255
Reply from FE80::1: bytes=32 time<lms TTI=255
Ping statistics for FE80::1:
Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),
Approximate round trip times in milli-seconds:
Minimum = Oms, Maximum = lms, Average = Oms
Userl to User2


### Lab Assignments & Solutions — strona 160

Ic:\>ping fe80::3
Reply from FE80::3: bytes=32 time=lms TIL=128
Reply from FE80::3: bytes=32 time<lms TTL=128
Reply from FE80::3: bytes=32 time<lms TTL=128
Reply from FE80::3: bytes=32 time<lms TTL=128
Ping statistics for FE80::3:
Packets: Sent = 4, Received = 4, Lost = 0 (0%
loss),
lapproximate round trip times in milliseconds:
Minimum = Oms, Maximum = lms, Average = Oms
22 Repeat the previous step for User3.
Pinging fe80::1 with 32 bytes of data:
Reply from FE80::1: bytes=32 time<lms TTL=255
Reply from FF80::1: bytes=32 time<lms TTL=255
Reply from FE80::1: bytes=32 time<lms TTL=255
Reply from FE80::1: bytes=32 time=lms TTL=255
Ping statistics for FE80::1:
Packets: Sent - 4, Received - 4, Lost = 0 (0% loss),
Approximate round trip times in milli-seconds:
Minimum = Oms, Maximum = lms, Average = Oms
C:\sping feg0::3
Pinging £80::3 with 32 bytes of data:
Reply from FE80::3: bytes-32 time<lms TTL=128
Reply from FE80::3: bytes=32 time<lms TTL=128
Reply from FE80::3: bytes-32 time<lms TTL=123
Reply from FE80::3: bytes=32 time<ims TTL=128
Ping statistics for FE8Q::3:
Packets: Sent = 4, Received = 4, Lost = 9 (0% loss),
Approximate round trip times in milli-seconds:


# NET-06-LS1 — Subnetting Practice

> Zakres źródłowy: strony 161–168.


### Lab Assignments & Solutions — strona 161

Computer Networking
Lab Assignment Subnetting
& Solution Concepts
ocnae NET-06-LS1
ol Subnetting Practice

EI
Copyright © 1996-2021 HackerU Ltd.
All Rights Reserved.


### Lab Assignments & Solutions — strona 162

Note: Solutions for the instructor are shown in the green box.
G Lab Objective
Apply what you learned about subnetting by answering the review questions below
relating to the material covered in the module. The topics include how to subnet
networks and how to assign IP addresses.

fy Lab Mission
Answer all review questions.
ea .
©) Lab Duration
30-60 minutes
fe Requirements
e Knowledge of subnetting concepts
e Knowledge of the binary and decimal number systems

LT
[ra] Resources
¢ Calculator (optional)


### Lab Assignments & Solutions — strona 163

Lab Task 1: CIDR & VLSM
Answer practice questions covering variable length subnet masks and classless inter-
domain routing.
1. What is the subnet mask of prefix /28?
11111111.11111111.11111111.11110000, 128+64+32+16 = 240
2 Whatare the three prefixes of classful addresses represented as an
IP address suffix?
3 How many usable IP addresses are there if the subnet mask is
255.255.255.128?
4 What is the main purpose of subnetting?


### Lab Assignments & Solutions — strona 164

Lab Task 2: Practice Questions for Subnetting
Answer practice questions covering subnetting.
1 You were asked to subnet the network address 192.168.1.0/24 so that each sub-
network includes 45 hosts. How should this be done?
a) 255.255.255.128
b) 255.255.224.0
c) 255.255.255.192
d) 255.255.255.224
2 How many assignable host addresses are there in a network with the address
172.16.0.0 and subnet mask 255.255.252.0?
a) 510
b) 1022
c) 254
d) 1024

3 True or false: There are eight sub-network addresses if the given network is
192.168.10.0 with subnet mask 255.255.255.224.

4 Network administrators require you to create an addressing scheme for a new
division in the company. The requirements include a minimum of three network
addresses and at least 35 users per network. The given IP address is 10.0.0.0 and
the subnet mask is 255.255.255.0.

a) What prefix should be used?
b) What subnet mask should be used?
c) Fill in the following table with the new addressing scheme:


### Lab Assignments & Solutions — strona 165

Network Address Usable Address
Network Address Usable Address
10.0.0.0 10.0.0.1—10.0.0.62 10.0.0.63

10.0.0.64 10.0.0.65—10.0.0.126 10.0.0.127
10.0.0.128 10.0.0.129—10.0.0.190 10.0.0.191
10.0.0.192 10.0.0.193—10.0.0.254 10.0.0.255

a) Prefix: /26

b) Subnet mask: 255.255.255.192

5 What is the correct prefix for the address 10.0.0.0 and subnet mask

255.255.255.240?

a) 10.0.0.0/25
b) 10.0.0.0/30
c) 10.0.0.0/27
d) 10.0.0.0/28

6 What is the network address for a host with IP address 192.168.23.61/28?
a) 192.168.23.0
b) 192.168.23.48
c) 192.168.23.32
d) 192.168.23.60


### Lab Assignments & Solutions — strona 166

7 Which IP addresses are valid for hosts belonging to the 10.1.16.0/20 subnet?
(Choose three answers.)
a) 10.1.15.255
b) 10.1.16.7
c) 10.1.80.150
d) 10.1.16.250
e) 10.1.32.50
f) 10.1.30.10
8 Anadmin is working with network 192.168.4.0, which has been subnetted with a
/26 prefix. Which addresses can be assigned for a host on the same subnet?
(Choose two answers.)
a) 192.168.4.67
b) 192.168.4.128
c) 192.168.4.15
d) 192.138.4.132
e) 192.168.4.61
f) 192.168.4.125
9 Anadministrator needs to configure a point-to-point connection. To do so, he
needs to divide the address 172.16.0.0/24 into 64 subnets, each having four
addresses.
a) What prefix should be used?
b) What subnet mask should be used?
c) Fill in the following table with the new addressing scheme (fill in only
the first three rows):
a
|
a


### Lab Assignments & Solutions — strona 167

a) /30
b) 255.255.255.252
Network Address Usable Address
172.16.0.0 172.16.0.1-172.16.0.2 172.16.0.3
172.16.0.4 172.16.0.5-172.16.0.6 172.16.0.7
172.16.0.8 172.16.0.9-172.16.0.10 172.16.0.11
10 A network administrator was asked to divide the address 192.168.10.0/24 into
eight subnets.
a) What prefix should be used?
b) What subnet mask should be used?
c) Fill in the following table with the new addressing scheme (fill in only
the first four rows):
Network Address Usable Address
a) /27
b) 255.255.255.224
Network Address Usable Address
192.168.10.0 192.168.10.1—192.168.10.30 192.168.10.31
192.168.10.32 192.168.10.33-192.168.10.62 192.168.10.63
192.168.10.64 192.168.10.65—-192.168.10.94 192.168.10.95
192.168.10.96 192.168.10.97—192.168.10.126 192.168.10.127


### Lab Assignments & Solutions — strona 168

11. Network administrators require you to create an addressing scheme for a new
division in the company. The requirements include a maximum number of
networks, with each network having at least 500 users. The given IP address is
80.0.0.0/16.

a) What prefix should be used?
b) What subnet mask should be used?
c) Fill in the following table with the new addressing scheme (fill in only
the first four rows):
Network Address Usable Address
a) /23
b) 255.255.254.0
Network Address Usable Address
80.0.0.0 80.0.0.1-80.0.1.254 80.0.1.255
80.0.2.0 80.0.2.1-80.0.3.254 80.0.3.255
80.0.4.0 80.0.4.1—80.0.5.254 80.0.5.255
80.0.6.0 80.0.6.1-80.0.7.254 80.0.7.255


# NET-07-LS1 — Configuring IPv4 Static and Default Routes

> Zakres źródłowy: strony 169–186.


### Lab Assignments & Solutions — strona 169

Computer Networking
Lab Assignment IPv4 & IPv6 Static
& Solution Routing
RO isis, NET-O7-LS1
olf Configuring IPv4 Static
re U and Default Routes
Copyright © 1996-2020 HackerU Ltd.
All Rights Reserved.


### Lab Assignments & Solutions — strona 170

Note: Solutions for the instructor are shown inside the green box.
G Lab Objective
Understand how static and default routes can be used to connect multiple networks,
and the routing methods used to configure routers.
5) Lab Mission
Interconnect three LANs, and connect them to an external network using IPv4
addressing.
ea .
©) Lab Duration
30-60 minutes
fe Requirements
e Knowledge of basic IOS commands and navigation.
e Familiarity with routing concepts.
e Basic understanding of subnetting.
Lt

[ea] Resources
¢ Environment & Tools

All platforms

Cisco Packet Tracer 7.2.2 or higher
e Files

NET-07-L1.pka


### Lab Assignments & Solutions — strona 171

Instructions for PKA Lab Files
Lab material includes the lab document and a PKA lab file.
Open the pka file through the Cisco Packet Tracer menu by clicking "File", and then
"Open...".
bw ae 2 QQQ0R Ese 2
Bran ome ore)
Open Acti Seance ae 04039)
Print CuleP
ed
Navigate to the file's location and open it.
a
a A t)
a
a
a
-
a
i
i
1
lena [NE-03 La Se


### Lab Assignments & Solutions — strona 172

Note: Double-clicking the pka file in your file explorer may not work (depending on the
Packet Tracer version).
Lab material includes the lab document and a PKA lab file.
When you open a PKA file in Cisco Packet Tracer, two windows appear:
1. Lab topology window
2. Activity window
PKA features
Note the following essential information regarding the Activity window:
1. Completion Percentage — Student progress appears at the bottom right corner of
the window.
2. Check Result Button — When you click this button and then click the "Assessment
Items" tab, you will find a checklist with lab objectives and status, whereby V=done,
X=not done.
Note: Both features help the instructor grade the exercise swiftly and efficiently.

A PT Activity: 001012 - ao x ‘Expandialapas Al| Show incase Rena)

Please fr othe exer document an cea allo the fener [Saas Pas Compaen) [Feeick

‘See the percentage of completion at the right-bottom corner to E-NTP Sener o ‘Other

determine your progress. 5 NIP Sener o Other

Note: The Optional and Bonus section are not scored, eo mnie : »

Good Luck Vie ° ier
PKA Solution
To view the solution or edit the lab file, you can simply click the "Wizard hat" icon and
enter the following password: C!S$cOM@ster
Right-click the "Answer network" tab and then click "Show Answer network".
Note: Be careful not to change anything so that the lab will remain intact.


### Lab Assignments & Solutions — strona 173

Lab Task 1: Revision Questions
Answer the review questions below regarding routing.
1 What is the difference between standard and default static routes?
Standard static route - Manually configured route that forwards traffic to a specific
network.
Default static route — Handles all packets that don't have a destination route in the
routing table.
2 Which command displays a routing table?
3 In the routing table which letters represent a static route and default static route?
S-Static / S*-Default Static
4 What is the default administrative distance of a static route?
Administrative Distance = 1
5 Bonus: Name two advantages of static routing (as opposed to dynamic routing)?
Static Route advantages:
e Static routing consumes minimal resources. No algorithms mean no overhead on the
router CPU, and no dynamic updates means no extra bandwidth is being used.
e The path a packet takes between two destinations is predictable, which allows more
control over the data flow.


### Lab Assignments & Solutions — strona 174

Lab Task 2: Configure IPv4 Standard Routes
Learn how to use |Pv4 to set up routes between the three LANs and the external
network using different routing methods.
192.168 0.64/26 210.10.10.0/30
a ¢ ( <sym, G Se Ss
192 168.0.192/30 192.168.0.196/30
192.168.0.0/26 ag Ny 192.168.0.128/26
hi WE ne (gael ae f F
ee ae So “a...
—_. 2960-26TT 4944 4941 2960-24TT =
Part 1: Configure Directly-Connected Static Routes on R1
1 Open PC1 and try to ping PC2. The ping will not be successful, which can be seen
by showing the R1 routing table and noting that the 192.168.0.64/26 network is
missing.
R1>enable
Rl#show ip route
IC:\>ping 192.168.0.66
Pinging 192.168.0.66 with 32 bytes of data:
Reply from 192.168.0.1: Destination host unreachable.
Reply from 192.168.0.1: Destination host unreachable.
Reply from 192.168.0.1: Destination host unreachable.
Reply from 192.168.0.1: Destination host unreachable.
Ping statistics for 192.168.0.66:
Packets: Sent = 4, Received = 0, Lost = 4 (100% loss),


### Lab Assignments & Solutions — strona 175

Bi> Ts
Ri>enable
Rl#show ip route
Codes: L - local, C - connected, 5 - static, R - RIP, M — mobile,
B - BGP
D - EIGRP, EX - EIGRP external, © - OSPF, IA - OSPF inter
area
Nl - OSPF NSSA external type 1, N2 - OSPF NSSA external
type 2
El - OSPF external type 1, £2 - OSPF external type 2, © -
EGP
i - IS-IS, Ll - IS-I5 level-1, Lz - 15-15 level-2, ia -
IS-IS inter area
* — candidate default, U - per-user static route, o — ODR
P - periodic downloaded static route
Gateway of last resort is not set
152.168.0.0/24 is variably subnetted, 4 subnets, 3 masks
c 192.168.0.0/26 is directly connected, GigabitEthernetd/o
L 192.168.0.1/32 is directly connected, GigabitEthernet0/0
is 192.168.0.192/30 is directly connected, Serial0/0/0
L 192.168.0.193/32 is directly connected, Serial0/o/0
R1F| we
2 How many networks are directly connected to each router? (Excluding the
210.10.10.0 network.) Hint: Use show ip route, to check.
R1# show ip route
Directly connected networks:
R1-2
R2-3 (4, including the external network)
R3-2


### Lab Assignments & Solutions — strona 176

3 OnR1, configure a directly-connected standard static route to every network not
directly connected to R1 (excluding the 210.10.10.0 network).
Note: When configuring directly-connected static routes, the router will issue a
warning, which you can ignore, because this is a point-to-point connection.
Tip: To simplify the process, go to “Options” in the Packet Tracer menu, select
“Preferences...”, and select “Always Show Port Labels in Logical Workspace” to
display the port names.
Ri#config terminal
R1(config)#ip route 192.168.0.64 255.255.255.192 serial 0/0/0
R1(config)#ip route 192.168.0.128 255.255.255.192 serial 0/0/0
R1(config)#ip route 192.168.0.196 255.255.255.252 serial 0/0/®
R1(config)#exit
WP Cinco Packet Tracer - ao x
File Edit Options | View Tools Extensions Help
. Preferences .. CHR = =
Beats om § + QR ES 2
= Algorithm Settings CrlvShiteM
TQ Disease cosy (a4 ia re
Cater) — Physical)x esa y: 125 Root) LC 035400)
192168.0 6426 210.10.10.030
Cap
pcer arial ~~ Intemet
182.168.0.1920 192 168.0.196/30
=. 2960-2477 2960-241 5
<< Es > if
Time: 00:035a( > )(_) (Q Reaitime] Simulation]
SIE Ss MP OGEGoeoseoaaancoce
=| 4331 4321 1941 2901 2911 B1910X BISHGW _ 829 1240 PrROUE PrEmpty _ 1841 at a
== & >|
Boe a fe ee


### Lab Assignments & Solutions — strona 177

®
intraca’ |sbaresttee [ine [Font | Miscekareos | Anewver Tues [|(Coston inevieene | Pubtoher! [Gnas Caste
customize User Experience
© Show Animation © Show Link Lights
Olay Sound © Play Telephony Sound
‘Show Device Medel Labels ‘Show QoS Stamps on Packets
[2 Show Device Name Labels Show Port Labels When Mouse Over in Logical Workspace
[Enable Cable Length Ect
ODisable Auto Cable C1 Use CLI as Device Default Tab
Use Matric System (Uncheck to use Imperial) EZ Show Cable info Popup in Physical Workspace
TD Align logical workspace objects DAlion physical workspace objects
4 Display the R1 routing table to verify all static route configurations.
Hint: Use the keyword static at the end of the show ip route command to display
only the static routes.
Rl#show ip route static
Rl#show ip route static
192.168.0.0/24 is variably subnetted, 7 subnets, 3 masks
Ss 192.168.0.64/26 is directly connected, Serial0/0/0
8s 192.168.0.128/26 is directly connected, Serial0/0/0
5 192.168.0.196/30 is directly connected, Serial0/0/0
Rl# heat
Part 2: Configure Next-Hop Static Routes on R2
General hint: Use show ip interface brief to view IP addresses on the routers.
5 On Rz2, configure a next-hop standard static route for every network not directly
connected to R2 (excluding the 210.10.10.0 network).
R2>enable
R2>conf t
R2(config)#ip route 192.168.0.@ 255.255.255.192 192.168.0.193
R2(config)#ip route 192.168.0.128 255.255.255.192 192.168.0.198
R2(config)#exit


### Lab Assignments & Solutions — strona 178

6 Display the R2 routing table to verify all static route configurations.
R2#show ip route static
R2#show ip route static
192.168.0.0/24 is variably subnetted, & subnets, 3 masks
5 192.168.0.0/26 [1/0] via 192.168.0.193
s 192.168.0.128/26 [1/0] via 192.168.0.198
R2# ng
Part 3: Configure Directly-Connected Static Routes on R3
7 OnR3, configure a directly-connected standard static route for every network not
directly connected to R3 (excluding the 210.10.10.0 network).
R3>enable
R3#conf t
R3(config)#ip route 192.168.0.@ 255.255.255.192 serial @/0/1
R3(config)#ip route 192.168.0.64 255.255.255.192 serial @/0/1
R3(config)#ip route 192.168.0.192 255.255.255.252 serial 0/@/1
R3(config)#exit
R3(config)#ip route 192.168.0.64 255.255.255.192 serial 0/0/1
Default route without gateway, if not a point-to-point
interface, may impact performance
R3(config)#ip route 192.168.0.0 255.255.255.192 serial 0/0/1
&Default route without gateway, if not a point-to-point
interface, may impact performance
R3(config)#ip route 192.168.0.192 255.255.255.252 serial 0/0/1
Default route without gateway, if not a point-to-point
interface, may impact performance
R3 (contig) #| Re
8 Display the R3 routing table to verify all static route configurations.
R3#show ip route static
R3#show ip route static
192.168.0.0/24 is variably subnetted, 7 subnets, 3 masks
5 192.168.0.0/26 is directly connected, Serial0/0/1
& 192.168.0.64/26 is directly connected, Serial0/0/1
5 192.168.0.192/30 is directly connected, Serial0/0/1
R3#| w


### Lab Assignments & Solutions — strona 179

Step 4: Verify Connectivity
9 From PC1, ping PC2 and PC3. All pings should be successful.
C:\>ping 152.168.0.66
Pinging 192.168.0.66 with 32 bytes of data:
Request timed out.
Reply from 192.168.0.66: bytes=32 time=lms TITL=126
Reply from 192.168.0.66: bytes=32 time=2ms TIL=126
Reply from 152.168.0.€6: bytes=32 time=lms TIL=126
Bing statistics for 192.168.0.66:
Packets: Sent = 4, Received = 3, Lost = 1 (25% loss),
Approximate round trip times in milli-seconds:
Minimum = lms, Maximum = ims, Average = lms
10 Use the tracert command on PC1 to view the path of the packets to PC2.
C:\>tracert 192.168.0.66
Tracing route to 192.168.0.66 over a maximum of 30 hops:
1 0 ms O ms O ms 192.168.0.1
2 0 ms 1 ms 1 ms 192.168.0.194
3 2 2 ms 0 ms 192.168.0.66
Trace complete.


### Lab Assignments & Solutions — strona 180

Lab Task 3: Configure IPv4 Default Routes
Connect to the external network using default routes.

1 From PC1, try to ping an external resource 8.8.8.8 server. The ping will not be
successful because the routers do not know where to forward unknown external
network traffic.

Display the R1 routing table and verify that the “Gateway of last resort” option is
not set.
R1>enable
Rl#show ip route
C:\>ping 8.8.8.8
Pinging §.8.8.8 with 32 bytes of data:
Reply from 192.168.0.1: Destination host unreachable.
Reply from 192.168.0.1: Destination host unreachable.
Reply from 192.168.0.1: Destination host unreachable.
Reply from 192.168.0.1: Destination host unreachable.
Ping statistics for 8.8.8.8:
Packets: Sent = 4, Received = 0, Lost = 4 (100% loss),

Rl#show ip route tal
Codes: L - local, C - connected, 5 - static, R - RIP, M - mobile,
B - BGP

D - EIGRP, EX - EIGRP external, © - OSPF, IA - OSPF inter
area

Nl - OSPF NSSA external type 1, N2 - OSPF NSSA external
type 2

El - OSPF extermal type 1, E2 - OSPF external type 2, E -—
EGP

i - IS-IS, Ll - IS-IS level-1, L2 - IS-IS level-2, ia -
Is-IS inter area

* — candidate default, U - per-user static route, o - ODR

P - periodic downloaded static route

192.168.0.0/24 is variably subnetted, 7 subnets, 3 masks
c 192.168.0.0/26 is directly connected, GigabitEthernet0/0
L 192.168.0.1/32 is directly connected, GigabitEthernet0/0
s 192.168.0.64/26 is directly connected, Serialo/o/o
s 192.168.0.128/26 is directly connected, Serialo/o/o
c 192.168.0.192/30 is directly conmected, Serialo/o/o
L 192.168.0.193/32 is directly connected, Serialo/o/o
s 192.168.0.196/30 is directly connected, Serialo/o/o @


### Lab Assignments & Solutions — strona 181

2 OnR1, configure a (directly-connected) default route towards the Internet. Use
the outgoing interface that is in the direction of the Internet.
R1#conf t
R1(config)#ip route 0.0.0.0 0.0.0.® serial 0/0/20
R1(config)#exit
Rl (config)#ip route 0.0.0.0 0.0.0.0 serial 0/o/0
Default route without gateway, if not a point-to-point
interface, may impact performance
R1 (config) #| Mm
3 Display the routing table on R1, and verify that the “Gateway of last resort” is set
and the new default route is listed below.
Rl#show ip route
Rl#show ip route a
Codes: L - local, C - connected, 5 - static, R - RIP, M - mobile,
B - BGP
D - EIGRP, EX - EIGRP external, © - OSPF, IA - OSPF inter
area
Nl - OSPF NSSA external type 1, N2 - OSPF NSSA external
type 2
El - OSPF external type 1, E2 - OSPF external type 2, E -—
EGP
i - IS-IS, Ll - I5-IS level-1, L2 - I5-IS level-2, ia -
Is-IS inter area
* — candidate default, U - per-user static route, o - ODR
P -— periodic downloaded static route
192.168.0.0/24 is variably subnetted, 7 subnets, 3 masks
c 192.168.0.0/26 is directly connected, GigabitEthernet0/0
L 152.168.0.1/32 is directly connected, GigabitEthernet0/0
S 192.168.0.64/26 is directly connected, Serial0/0/0
ed 152.168.0.128/26 is directly connected, Serial0/0/0
c 192.168.0.192/30 is directly connected, Serial0/0/0
L 152.168.0.193/32 is directly connected, Serial0/0/0
s eo é nat oppected Serial /o/o


### Lab Assignments & Solutions — strona 182

4 Repeat steps 2 and 3 on R2 and R3.
R2#conf t
R2(config)#ip route 0.0.0.0 0.0.0.0 serial 0/1/0
R2(config)#do show ip route static
R3#conf t
R3(config)#ip route 0.0.0.0 0.0.0.0 serial 0/0/1
R3(config)#do show ip route static
sDefault route without gateway, 1f not a point-to-point
interface, mg DDS, perform =
R2 (config)
192.168.0.0/24 is variably subnetted, & subnets, 3 masks
EI 192.168.0.0/26 [1/0] via 192.168.0.193
a 192.168.0.128/26 [1/0] via 192.168.0.198
a* 0.0.0.0/0 is directly connected, Serial0/1/0
R2 (config) # be
SDefault route withoue Gateuay, 2 NOt a Pein’ bo point
interface, may impact performance
192. 188-0 Oot ae variably sebnetted, 7 subnets, 3 masks
= 192.168.0.0/26 is directly connected, Serial0/0/1
5 192.168.0.64/26 is directly connected, Serial0/0/1
s 192.168.0.192/30 is directly connected, Serial0/0/1
Ei 0.0.0.0/0 is directly connected, Serial0/0/1
R3 (config) 4 MM


### Lab Assignments & Solutions — strona 183

5 From PC1, PC2, and PC3, try to ping the 8.8.8.8 server again and observe the
results.
Pinging 8.8.8.8 with 32 bytes of data:
Reply from 8.8.8.8: bytes=32 time=2ms TTL=253
Reply from 8.8.8.8: bytes=32 time=3ms TTL=253
Reply from 8.8.8.8: bytes=32 time=2ms TTL=253
Reply from 8.8.8.8: bytes=32 time=2ms TTL=253
Ping statistics for 8.8.8.8:
Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),
Approximate round trip times in milli-seconds:
Minimum = 2ms, Maximum = 3ms, Average = 2ms
6 Use the tracert command on PC1 to view the path of the packets to the 8.8.8.8

server.
C:\>tracert 8.8.8.8
Tracing route to 8.8.8.8 over a maximum of 30 hops:

il 1 ms 1 ms 0 ms 192.168.0.1

2 1 tis O ms 1 ms 192.168.0.194

3 1 ms 0 ms 0 ms 8.8.8.8
Trace complete.


### Lab Assignments & Solutions — strona 184

Lab Task 4 (Optional): Configure IPv4 Summary Route
Check to see if a routing table has routes that can be summarized, and replace those
routes with a summarized route.

1 __ Display the R1 routing table and note the remote network address and outgoing
interface configured for all. The network partition and interface are identical. This
means this is a proper situation for a summary setup.

R1(config)#do show ip route static
R1 (config) #do show ip route static
192.168.0.0/24 is variably subnetted, 7 subnets, 3 masks
a 192.168.0.64/26 is directly connected, Serial0/0/0
ES 192.168.0.128/26 is directly connected, Serial0/0/0
Ss 192.168.0.196/30 is directly connected, Serial0/0/0
5 0.0.0.0/0 is directly connected, Serial0/0/0
Rl (config) # ae
2 Erase the standard static route configuration.
R1(config)#no ip route 192.168.0.64 255.255.255.192 serial 0/0/®
R1(config)#no ip route 192.168.0.128 255.255.255.192 serial 0/0/20
R1(config)#no ip route 192.168.0.196 255.255.255.252 serial 0/0/0
aE COREETTY
Ri(config)#nqj ap routef192.168.0.64 §55.255.255.1929 serial 0/0/0
Ri (config) #ngj ip route9}192.168.0.128§255.255.255.19% serial 0/0/0
Ri(config)#noj ip routef[192.168.0.196§255.255.255.25§ serial 0/0/0
Rl (contig) # =
3 Summarize networks into a single address and mask, as follows:
Step 1 - List the 192.168.0.X networks in binary format.
Summary steps:
192.168.0.64 -11000000.10101000.90000000.01000000
192.168.0.128-11000000.10101000. 20000000 .10000000
192.168.0.196-11000000.10101000 . 920000000.11000100
Step 2 - Count the number of far-left matching bits to determine the mask for the
summary route. The 24 far-left matching bits constitute the prefix, or subnet
mask, for the summarized route.


### Lab Assignments & Solutions — strona 185

Step 3 - Copy the matching bits and add zero bits to determine the summarized
network address. The matching bits with zeros at the end result in the
summarized network address.
New address:
192.168.0.0 - 11000000.10101000. 200000000 .2e0000000
New mask:
255.255.255.@ 11111111. 11111111. 11111111.eeee0e00ee
4 Configure the new summary network and subnet mask using next-hop or directly-
connected.
R1(config)#ip route 192.168.0.@ 255.255.255.@ serial 0/0/0
Ri (config) #ip route 192.168.0.0 255.255.255.0 serial 0/0/0
5 _ Display the R1 routing table and verify the new summary route.
R1(config)#exit
Rl#show ip route static
192.168.0.0/24 is variably subnetted, @ subnets, 4 masks
s 192.162.0,0/24 as dizectly connected, Serial0/0/0
s 192 .168.0.€4/2€ is directly connected, Serial0/0/0
8 192.168.0.128/2€ is directly connected, Serial0/0/a
s 192.162.9,15¢/30 is directly connected, serialo/o/0
S* 0.0.0.0/0 is directly connected, Serial0/0/0


### Lab Assignments & Solutions — strona 186

6 From PC1, ping PC2 and the 8.8.8.8 server to verify connectivity.

C:\>ping 192.168.0.66
Pinging 192.168.0.66 with 32 bytes of data:
Request timed out.
Reply from 192.168.0.66: bytes=32 time=l2ms TTL=126
Reply from 192.168.0.66: bytes=32 time=lms TTL=126
Reply from 192.168.0.66: bytes=32 time=1ms TTL=126
Ping statistics for 192.168.0.66:

Packets: Sent = 4, Received = 3, Lost = 1 (25% loss),
Approximate round trip times in milli-seconds:

Minimum = lms, Maximum = 12ms, Average = 4ms
Ci\>ping 8.8.8.8
Pinging 8.8.8.8 with 32 bytes of data:
Reply from 8.8.8.8: bytes=32 time=2ms TTL=253
Reply from 8.8.8.8: bytes=32 time=2ms TTL=253
Reply from 8.8.8.8: bytes=32 time=2ms TTL=253
Reply from 8.8.8.8: bytes=32 time=2ms TTL=253
Ping statistics for 8.8.8.8:

Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),
Approximate round trip times in milli-seconds:

Minimum = 2ms, Maximum = 2ms, Average = 2ms


# NET-08-LS1 — Configuring and Verifying RIPv2

> Zakres źródłowy: strony 187–202.


### Lab Assignments & Solutions — strona 187

Computer Networking
Lab Assignment Dynamic Routing
& Solution
NET-08-LS1
i Configuring and
oe ni Verifying RIPv2
EI
Copyright © 1996-2020 HackerU Ltd.
All Rights Reserved.


### Lab Assignments & Solutions — strona 188

Note: Solutions for the instructor are shown inside the green box.
G Lab Objective
Implement dynamic routing using RIP. RIP is a straightforward protocol that helps
the user understand basic network routing. However, it is no longer a commonly
used protocol.
») Lab Mission
Configure RIPv2 to connect all networks, and use it to propagate the network with a
default route, allowing the WAN to connect to an external network.
CN) 7
©) Lab Duration
30 minutes—1 hour
{fe Requirements
e Knowledge of basic IOS commands and navigation.
e Familiarity with routing concepts.
e Basic understanding of subnetting.
on

| Resources
¢ Environment & Tools

All platforms

Cisco Packet Tracer 7.2.2 and higher
e Files

NET-08-L1.pka


### Lab Assignments & Solutions — strona 189

Instructions for PKA Lab Files
Lab material includes the lab document and a PKA lab file.
Open the PKA file through the Cisco Packet Tracer menu by clicking "File" and then
"Open...".
bw ae 2 QQQ0R Ese 2
Bran ome ore)
Open Acti Seance ae 04039)
Print CuleP
ed
Navigate to the file's location and open it.
a
a A t)
a
a
a
-
a
i
i
1
lena [NE-03 La Se


### Lab Assignments & Solutions — strona 190

Note: Double-clicking the PKA file in your file explorer may not work (depending on the
Packet Tracer version).
Lab material includes the lab document, and a PKA lab file.
When you open a PKA file in Cisco Packet Tracer, two windows appear:
1. Lab topology window
2. Activity window
PKA Features
Note the following essential information regarding the Activity window:
1. Completion Percentage — Student progress appears at the bottom right corner of
the window.
2. Check Result Button — When you click this button and then click the "Assessment
Items" tab, you will find a checklist with lab objectives and status, whereby V=done,
X=not done.
Note: Both features help the instructor grade the exercise swiftly and efficiently.

A PT Activity: 001012 - ao x ‘Expandialapas Al| Show incase Rena)

Please fr othe exer document an cea allo the fener [Saas Pas Compaen) [Feeick

‘See the percentage of completion at the right-bottom corner to E-NTP Sener o ‘Other

determine your progress. 5 NTP Sener o Other

Note: The Optional and Bonus section are not scored, eo mnie : »

Good Luck Vie ° ier
PKA Solution
To view the solution or edit the lab file, you can simply click the "Wizard hat" icon and
enter the following password: C!S$cOM@ster
Right-click the "Answer network" tab and then click "Show Answer network".
Note: Be careful not to change anything so that the lab will remain intact.


### Lab Assignments & Solutions — strona 191

Lab Task 1: Revision Questions
Refresh your knowledge of routing protocols and RIP.
1. What is the default Administrative Distance value of RIP?
AD=120
2 What route source letter represents an RIP route in the routing table?
3. Whatare the default Hello and Hold intervals of RIP?
Hello is 30 seconds, Hold is 180 seconds
4 From which version of RIP VLSM is authentication supported?


### Lab Assignments & Solutions — strona 192

Lab Task 2: Configure RIPv2
Configure RIPv2 so that all networks are connected, and verify the connectivity.
Part 1: Enable and configure RIP on the routers
1 Enter R1 global configuration mode and implement the following settings:
a) Enable RIP.
b) Set version 2.
c) Configure all local networks connected to R1 to be used by RIPv2.
Hint: Use Show ip route connected to view the local networks and
prefixes.
d) Disable auto-summarization.
e) Configure a passive-interface on the appropriate interface.
2 Save the configuration.
R1> enable
Ri#configure terminal
R1(config)#router rip
R1(config-router)#version 2
R1(config-router)#do show ip route connected
R1(config-router)#network 172.16.0.0
R1(config-router)#network 172.16.0.8
R1(config-router)#network 192.168.10.0
R1(config-router)#no auto-summary
R1(config-router)#passive-interface gigabitethernet 0/@
R1(config-router)#exit
R1(config)#exit
Rl#copy running-config startup-config


### Lab Assignments & Solutions — strona 193

a
Rl>enable
Rl#conf t
Enter configuration commands, one per line. End with CNIL/Z.
Rl (config) #router rip
Rl (config-router)#version 2
Rl (config-router)#do show ip route connected
C 172.16.0.0/30 is directly connected, Serial0/1/0
C 172.16.0.8/30 4s directly connected, Serial0/1/1
© 192,168.10.0/24 is directly connected, GigabitEthernet0/0
R1 (config-router)#network 172.16.0.0
Rl (config-router)#network 172.16.0.8
Rl (config-router) #network 1$2.168.10.0
Rl (config-router)#no auto-summary
Rl (config-router) #passive-interface gigabitethernet 0/9
Rl (config-router) #exit
Rl (config) fexit
Re
$S5YS-S-CONFIG_I: Configured from console by console
Rl#copy run start
Destination filename [startup-config]?
Building configuration...
- yw
ite)
3 Repeat steps 1 and 2 for R2 and R3.
R2> enable
R2#configure terminal
R2(config)#router rip
R2(config-router)#version 2
R2(config-router)#do show ip route connected
R2(config-router)#network 172.16.0.0
R2(config-router)#network 172.16.0.4
R2(config-router)#network 192.168.20.0
R2(config-router)#no auto-summary
R2(config-router)#passive-interface gigabitethernet 0/@
R2(config-router)#exit
R2(config)#exit
R2#copy running-config startup-config


### Lab Assignments & Solutions — strona 194

R3> enable
R3#configure terminal
R3(config)#router rip
R3(config-router)#version 2
R3(config-router)#do show ip route connected
R3(config-router)#network 172.16.0.4
R3(config-router)#network 172.16.0.8
R3(config-router)#network 192.168.30.0
R3(config-router)#network 210.10.10.0
R3(config-router)#no auto-summary
R3(config-router)#passive-interface gigabitethernet 0/0
R3(config-router)#exit
R3(config)#exit
R3#copy running-config startup-config
R2:
Ro>enable im
R2#conf t
Enter configuration commands, one per line. End with CNIL/Z.
R2(config)#router rip
R2(config-router)#version 2
R2(config-router)#do show ip route connected
Cc 172.16.0.0/30 is directly connected, Serial0/3/0
c 172.16.0.4/30 is directly connected, Serial0/3/1
c 192.168.20.0/24 is directly connected, GigabitEtherneto/0
R2(config-router)#network 172.16.0.0
R2(config-router)#network 172.16.0.4
R2(config-router)#network 192.168.20.0
R2(config-router)#no auto-summary
R2(config-router) #passive-interface gigabitethernet 0/0
R2(config-router) #exit
R2 (config) #exit
R2¢#
$SYS-5-CONFIG I: Configured from console by console
R2#copy run start
Destination filename [startup-config]?
Building configuration...
[0K]
R24] Ad


### Lab Assignments & Solutions — strona 195

R3:
R3>enable cS
R3¥conf t
Enter configuration commands, one per line. End with CNTL/Z.
R3 (config) #router rip
R3 (config-router) #version 2
R3(config-router)#do show ip route connected
C 172.16.0.4/30 is directly connected, Serial0/3/1
C 172.16.0.8/30 is directly connected, Serial0/3/0
C 192.168.30.0/24 is directly connected, GigabitEthernet0/0
C 210.10.10.0/30 is directly connected, Serial0/2/0
R3 (config-router) fnetwork 172.16.0.4
R3 (config-router) #network 172.16.0.8
R3 (contig-router) #network 192.168.30.0
R3 (contig-router) #network 210.19.10.0
R3(config-router)#no auto-summary
R3 (config-router) #passive-interface gigabitethernet 0/9
R3 (config-router) #exit
R3 (config) #exit
R3#
$5YS-5-CONFIG_I: Configured from console by console
R3#copy run start
Destination filename [startup-config]?
ilding config io a


### Lab Assignments & Solutions — strona 196

Part 2: Verify RIP configuration on the routers
4 Display the R1 routing table and check if RIP updated it with the remote networks.
Tip: Use the rip keyword to view RIP routes.
Rl#show ip route rip
Rlf#show ip route rip
172.16.0,.0/16 is variably subnetted, 5 subnets, 2 masks
Serialo/1/1
192.16%.10.0/24 is variably subnetted, 2 subnets, 2 masks
IR | 192.168.20.0/24 [120/2] via 172.16.0.9, 90:00:09,
exialo/l/l
LR} 192.168.30.0/24 [120/1] via 172.16.0.9, 90:00:09,
Serialo/i/1
210.10.10.0/30 is subnetted, 1 subnets
R | 210.10.10.0 [120/1] via 172.16.0.5, 00:00:05, Seriald/1/1
Rie bs
5 Run show ip protocols to view and verify RIP settings.
Rl#show ip protocols
RIF A
Rl#
Rl#show ip protocols
Routing Protocol is "rip"
Sending updates every 30 seconds, next due in 2 seconds
Invalid after 180 seconds, hold down 180, flushed after 240
Outgoing update filter list for all interfaces is not set
Incoming update filter list for all interfaces is not set
Redistributing: rip
Default version control: send version 2, receive 2
Interface Send Recv Triggered RIP Key-chain
Serial0/1/0 4 2
Serial0/1/1 2 2
Automatic network summarization is not in effect
Maximum path: 4
Routing for Networks:
172.16.0.0
192.168.10.0
Passive Interface(s)}:
GigabitEthernet0/0
Routing Information Sources:
Gateway Distance Last Update
172.16.0.9 120 00:00:10
Distance: (default is 120)
Rig] bell


### Lab Assignments & Solutions — strona 197

6 Repeat steps 4 and 5 for R2 and R3.
R2#show ip route rip
R2#show ip protocols
R3#show ip route rip
R3#show ip protocols
R2:
R2>
R2>show ip route rip
172.16.0,.0/16 is variably subnetted, 5 subnets, 2 masks
| 172.16.0.8/30 [120/1] via 172.16.0.6, 00:00:23,
(serialo/3/1
8 192.168.10.0/24 [120/2] via 172.16.0.6, 00:00:23,
exrialo/3/1
192.16%.20.0/24 is variably subnetted, 2 subnets, 2 masks
iR| 192.16%.30.0/24 [120/1] via 172.16.0.6, 00:00:23,
jerialo/3/1
210.10.10.0/30 is subnetted, 1 subnets
| 210.10.10.0 [120/1] via 172.16.0.6, 00:00:23, Serialo/3/1
R2>| ii
R2>show ip protocols
Routing Protocol is "rip"
Sending updates every 30 seconds, next due in 1 seconds
Invalid after 180 seconds, hold down 180, flushed after 240
Outgoing update filter list for all interfaces is not set
Incoming update filter list for all interfaces is not set
Redistributing: rip
Default version control: send version 2, receive 2
Interface Send Recv Triggered RIP Key-chain
Serialo/3/0 2 2
Serialo/3/1 2 2
Automatic network summarization is not in effect
Maximum path: 4
Routing for Networks:
172.16.0.0
192.168.20.0
Passive Interface(s):
GigabitEthernet0/0
Routing Information Sources:
Gateway Distance Last Update
172.16.0.6 120 00:00:21
Distance: (default is 120)
R2> id


### Lab Assignments & Solutions — strona 198

R3:
R3>show ip route rip
172.16.0.0/16 is variably subnetted, 5 subnets, 2 masks
LR | 172.16.0.0/30 [120/1] via 172.16.0.19, 00:00:26,
erialo/3/0
[120/1] via 172.16.0.5, 90:00:18,
grialo/3/1
fk] 192.168.10.0/24 [120/1] via 172.16.0.10, 00:00:26,
erialo/3/0
Re 192.168.20.0/24 [120/1] via 172.16.0.5, 00:00:18,
erialo/3/1
R3> v
R3>show ip protocols o
Routing Protocol is "rip"
Sending updates every 30 seconds, next due in 22 seconds
Invalid after 160 seconds, hold down 180, flushed after 240
Outgoing update filter list for all interfaces is not set
Incoming update filter list for all interfaces is not set
Redistributing: rip
Default version control: send version 2, receive 2
Interface Send Recv Triggered RIP Key-chain
Serialo/3/0 2 2
Serialo/3/1 2 2
Serialo/2/0 2 2
Automatic network summarization is not in effect
Maximum path: 4
Routing for Networks:
172.16.0.0
192.168.30.0
210.10.10.0
Passive Interface (s):
GigabitEthernet0/0
Routing Information Sources:
Gateway Distance Last Update
172.16.0.10 220 ooroor14
--More-- | v


### Lab Assignments & Solutions — strona 199

Part 3: Test connectivity
7 From PC1, ping all other PCs. All pings should be successful.
Request timed out.
Reply from 192.168.20.2: bytes=32 time=1?ms TYL=125
Minimum = 2ms, Maximum = 17ms, Average = 7ms
Reply from 192.168.30.3: bytes=32 time=Ims TTL=126
JApproximate round trip times in milli-seconds:
Minimum = Ims, Maximum = lms, Average = Ims


### Lab Assignments & Solutions — strona 200

Lab Task 3: Propagating a Default Route
Use RIPv2 to distribute the default route (gateway) for all routers from a single router
on the network.
Part 1: Configure a default route
1 From PC1, try to ping an external resource 8.8.8.8 server. The ping will not be
successful because the routers don't know where to forward unknown external
network traffic.
Display the R3 routing table and verify that the “Gateway of last resort” option is
not set.
R3#show ip route
Pinging 8.8.8.8 with 32 bytes of data:
Reply from 192.168.10.1: Destination host unreachable.
Reply from 192.168.10.1: Destination host unreachable.
Reply from 192.168.10.1: Destination host unreachable.
Reply from 192.168.10.1: Destination host unreachable.
Ping statistics for 8.8.8.8:
Packets: Sent = 4, Received = 0, Lost = 4 (100% loss),
R3>show ip route
Codes: L - local, C - connected, S - static, R - RIP, M - mobile,
B - BGP
D - EIGRP, EX - EIGRP external, 0 - OSPF, IA - OSPF inter
area
Nl - OSPF NSSA external type 1, N2 - OSPF NSSA external
type 2
El - OSPF external type 1, E2 - OSPF external type 2, E -
EGP
i - IS-IS, Ll - IS-IS level-l, L2 - IS-IS level-2, ia -
Is-IS inter area
® — candidate default, U - per-user static route, o - ODR
P - periodic downloaded static route
172.16.0.0/16 is variably subnetted, 5 subnets, 2 masks
R 172.16.0.0/30 [120/1] via 172.16.0.10, 00:00:25,
Serial0/3/0
[120/1] via 172.16.0.5, 00:00:01,
Serial0/3/1
(c 172.16.0.4/30 is directly connected, Serial0/3/1
ds 172.16.0.6/32 is directly connected, Serial0/3/1
(c 172.16.0.8/30 is directly connected, Serial0/3/0 v


### Lab Assignments & Solutions — strona 201

2 OnR3, configure a (directly-connected) default route towards the Internet,
meaning the outgoing interface that is in the direction of the Internet.
R3>enable
R3#configure terminal
R3(config)#ip route 0.0.0.0 0.0.0.0 serial 0/2/20
3 Display the R2 routing table before distributing the default route for comparison.
R2#show ip route
BagShoW Ep Eoute
Codes: L - lecal, C - connected, S - static, R - RIP, M - mobile, B -
BGP
D - EIGRP, EX - EIGRP external, O - OSPF, IA - OSPF inter area
Nl - OSPF NSSA external type 1, NZ - OSPF NSSA external type 2
El - OSPF external type 1, E2 - OSPF external type 2, E - EGP
i - Is-Is, Ll - IS-IS level-1, L2 - IS-IS level-2, ia - IS-IS
inter area
* - candidate default, U - per-user static route, o - ODR
P - periodic downloaded static route
Gateway of last resort is not set
172.1€.0.0/1€ is variably subnetted, § subnets, 2 masks
c 172.16.0.0/30 is directly connected, Serial0/3/0
L 172.1€.0.1/22 is directly connected, Serial0/3/0
c 172.1€.0.4/30 is directly connected, Serial0/3/1
172.1€.0.5/32 is directly connected, SerialO/3/1
R 172.1€6.0.8/30 [120/1] via 172.1€.0.€, 00:00:23, SerialO/3/1
Rg 192.168.10.0/24 [120/2] via 172.16.0.6, 00:00:23, Serial0/3/1
192.168.20.0/24 is variably subnetted, 2 subnets, 2 masks re


### Lab Assignments & Solutions — strona 202

Part 2: Update the default route on all routers
4 OnR3, enter RIP configuration mode and distribute the default route to all
routers, using the default-information originate command.
R3>enable
R3#configure terminal
R3(config)#router rip
R3(config-router )#default-information originate
R3(config-router )#exit
5 Display the R1, R2, and R3 routing tables and check for the default route.
R2#show ip route rip
R2#show ip route rip
172.16.0.0/16 is variably subnetted, 5 subnets, 2 masks
R 172.16.0.8/30 [120/1] via 172.16.0.6, 00:00:20,
Serial0/3/1
R 192.168.10.0/24 [120/2] via 172.16.0.6, 00:00:20,
Serial0/3/1
192.168.20.0/24 is variably subnetted, 2 subnets, 2 masks
R 192.168.30.0/24 [120/1] via 172.16.0.6, 00:00:20,
Serial0/3/1
210.10.10.0/30 is subnetted, 1 subnets
R 210.10.10.0 [120/1] via 172.16.0.6, 00:00:20, Serial0/3/1
R2¢ he
Part 3: Test connectivity
6 From PC1 and the rest of the hosts, try to ping the 8.8.8.8 server again and
observe the result.
C:\>ping 8.8.8.8
Pinging 8.8.8.8 with 32 bytes of data:
Reply from 8.8.8.8: bytes=32 time=2ms TTL=253
Reply from 8.8.8.8: bytes=32 time=llms TTL=253
Reply from 8.8.8.8: bytes=32 time-2ms TTL=253
Reply from 8.8.8.8: bytes=32 time=2ms TTL=253
Ping statistics for 8.8.8.8:
Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),
Approximate round trip times in milli-seconds:
Minimum = 2ms, Maximum = 1lms, Average = 4ms


# NET-08-LS2 — Configuring & Verifying OSPFv2

> Zakres źródłowy: strony 203–210.


### Lab Assignments & Solutions — strona 203

Computer Networking
Lab Assignment Dynamic Routing
& Solution
NET-08-LS2
i Configuring &
oe ni Verifying OSPFv2
EI
Copyright © 1996-2020 HackerU Ltd.
All Rights Reserved.


### Lab Assignments & Solutions — strona 204

Note: Solutions for the instructor are shown inside the green box.
@ Lab Objective
Understand the principles of OSPF and use best practices when working with OSPF in a
production environment.
4) Lab Mission
Configuring routers to use OSPF with best practices in mind.
rN) .
©) Lab Duration
25 — 35 Minutes
(© Requirements
e Knowledge of Cisco IOS.
e Anunderstanding of the Dynamic Routing flow.
e Knowledge of OSPF configuration.
on

| Resources
e Environment & ToolsTools

All Platforms

Cisco Packet Tracer 7.2.2 and higher
e Files

NET-08-L2.pka


### Lab Assignments & Solutions — strona 205

Instructions for PKA Lab Files
Lab material includes the lab document and a PKA lab file.
Open the PKA file through the Cisco Packet Tracer menu by clicking "File" and then
"Open...".
bw ae 2 QQQ0R Ese 2
Bran ome ore)
Open Acti Seance ae 04039)
Print CuleP
ed
Navigate to the file's location and open it.
a
a A t)
a
a
a
-
a
i
i
1
lena [NE-03 La Se


### Lab Assignments & Solutions — strona 206

Note: Double-clicking on the PKA file in your file explorer may not work (depending on
the Packet Tracer version).
Lab material includes the lab document and a PKA lab file.
When you open a PKA file in Cisco Packet Tracer, two windows appear:
1. Lab topology window
2. Activity window
PKA features
Note the following essential information regarding the Activity window:
1. Completion Percentage — Student progress appears at the bottom right corner of
the window.
2. Check Result Button — When you click this button and then click the "Assessment
Items" tab, you will find a checklist with lab objectives and status, whereby V=done,
X=not done.
Note: Both features help the instructor grade the exercise swiftly and efficiently.

A PT Activity: 001012 - ao x ‘Expandialapas Al| Show incase Rena)

Please fr othe exer document an cea allo the fener [Saas Pas Compaen) [Feeick

‘See the percentage of completion at the right-bottom corner to E-NTP Sener o ‘Other

determine your progress. 5 NTP Sener o Other

Note: The Optional and Bonus section are not scored, eo mnie : »

Good Luck Vie ° ier
PKA Solution
To view the solution or edit the lab file, you can simply click the "Wizard hat" icon and
enter the following password: C!S$cOM@ster
Right-click the "Answer network" tab and then click "Show Answer network".
Note: Be careful not to change anything so that the lab will remain intact.


### Lab Assignments & Solutions — strona 207

In this task you will configure the OSPF routing protocol on routers RO, R1, and R2, and
specify the networks for broadcasting.

1 Start the OSPF process with the ID of 1 on RO.
R@>enable
RQ#configure terminal
R@(config)#router ospf 1

2 Set the RO router ID to 1.1.1.0
RO(config-router)#router-id 1.1.1.0

3 Add RO connected networks to OSPF broadcasting.
RO(config-router)#network 192.168.0.0 @.0.0.255 area 0
RO(config-router)#network 172.16.0.0 0.0.0.3 area @
RO(config-router)#network 172.16.0.8 0.0.0.3 area @
RO(config-router)#auto-cost reference-bandwidth 1000

4 Set the gigabitEthernet 0/1 interface to passive.
RO(config-router)#passive-interface gigabitEthernet 0/1
RO(config-router)#exit
RO(config)#exit

5 Repeat steps 1 through 5 on R1 and R2 while setting R1’s ID to 1.1.1.1 and R2’s ID

to 1.1.1.2.
R1>enable
Rl#configure terminal
R1(config)#router ospf 1
R1(config-router)#router-id 1.1.1.1
R1(config-router)#network 192.168.1.@ @.0.0.255 area 0
R1(config-router)#network 172.16.0.4 0.0.0.3 area @
R1(config-router)#network 172.16.0.8 0.0.0.3 area @
R1(config-router)#auto-cost reference-bandwidth 1000
R1(config-router)#passive-interface gigabitEthernet 9/1


### Lab Assignments & Solutions — strona 208

R1(config-router)#exit
R1(config)#exit
R2>enable
R2#configure terminal
R2(config)#router ospf 1
R2(config-router)#router-id 1.1.1.2
R2(config-router)#network 192.168.2.@ @.0.0.255 area 0
R2(config-router)#network 172.16.0.4 0.0.0.3 area 0
R2(config-router)#network 172.16.0.0 0.0.0.3 area @
R2(config-router)#auto-cost reference-bandwidth 1000
R2(config-router)#passive-interface gigabitEthernet 0/1
R2(config-router)#exit


### Lab Assignments & Solutions — strona 209

Lab Task 2: Default Route with OSPF
In this task, you will configure the default route on router R2.

1 OnR2set the default route towards the internet (directly connected).
R2(config)#ip route 0.0.0.0 0.0.0.0 gigabitEthernet 0/0

2 Enable OSPF default route broadcasting.
R2(config)#router ospf 1
R2(config-router)#default-information originate
R2(config-router)#exit
R2(config)#exit

3 Verify that the routering information was propagated to all three routers using

the show ip route command on all the routers.

R@#show ip route ospf
Ri#show ip route ospf
R2#show ip route ospf

ROPER 2p TERS RERE

172.16.0.0/1€ is variably subnetted, 5 subnets, 2 masks
oO 1972.16.0.4 [110/2] wia 172.1€.0.2, 00:04:13, GigabitEthernet0/0/0
[110/2] wia 172.16.0.5, 00:04:13, GigabitEthernet0/1/0

°o 192.168.1.0 [110/2] via 172.1€.0.9, 00:05:43, GigabitEthernet0/1/0

oO 192.168.2.0 [110/2] via 172.1€.0.2, 00:04:13, GigabitEtherneto/0/0

O*EZ 0.0.0.0/0 [110/1] wia 172.16.0-2, 00:03:07, GigabitEthernet0/0/0

Rog v

Rlgshow ip route ospf

172.16.0.0/1€ is variably subnetted, 5 subnets, 2 masks
° 172.16.0.0 [110/2] wia 172.16.0.5, 00:04:47, GigabitEtherneto/o/o
[110/2] via 172.1€.0.10, 00:04:47, GigabitEtherneto/1/0

° 192.162.0.0 [110/2] via 172.16€.0.10, 00:06:15, GigabitEthernet0/1/0

° 192.16€8.2.0 [110/2] via 172.1€.0.5, 00:04:47, GigabitEthernet0/0/0

OWE2Z 0.0.0.0/0 [110/1] via 172.1€.0.5, 00:03:41, GigabitEthernetO/0/0

Rig v


### Lab Assignments & Solutions — strona 210

R2¢show ip route ospf
172.16.0_0/16 is wariably subnetted, 5 subnets, 2 masks
o 172.16.0.8 [110/2] wia 172.1€.0.€, 00:01:23, GigabitEthernet0/1/0
(1106/2) wia 172.16.0.1, 00:01:23, GigabitEthernet0/0/0
°o 192.168.0.0 [110/2] wia 172.16.0.1, 00:01:23, GigabitEthernet0/0/0
°° 192.1€6.1.0 [110/2] wia 172.16.0.€, 00:01:33, GigabitEthernet0/1/0
R2¢| w


# NET-09-LS1 — Configuring VLANs, Trunks, and More

> Zakres źródłowy: strony 211–231.


### Lab Assignments & Solutions — strona 211

Computer Networking
Lab Assignment VLANs & Trunk
& Solution
NET-09-LS1
és Configuring VLANs,
o [ae Trunks, and More
olin
E-
Copyright © 1996-2021 HackerU Ltd.
All Rights Reserved.


### Lab Assignments & Solutions — strona 212

Note: Solutions for the instructor are shown in the green box.
G Lab Objective
Explore the benefits of using VLANs on a network and the role trunking plays in setting
up VLANs.
) Lab Mission
The objective of this exercise is to learn how to configure VLANs and trunks for two
different LANs using a router on a stick.
ea .
©) Lab Duration
45-80 minutes
fe Requirements
e Basic knowledge of IOS commands and navigation
e Basic understanding of the VLAN and trunk concepts
LT
[ra] Resources
© Tools
o Cisco Packet Tracer 7.2.2 or higher
e Files
o NET-09-L1.pka


### Lab Assignments & Solutions — strona 213

Instructions for PKA Lab Files
Lab material includes the lab document and a PKA lab file.
Open the PKA file through the Cisco Packet Tracer menu by clicking File > Open...
Be ar. AQQQacmESs 2
Tees a A |
Open Aci Seance ae es)
a see ons Se
Prot Clee
ert m je: (Sasa To Dig and Diop To Woe :
Navigate to the file's location and open it.
a
a A 4)
a or
BB Seronage Stross
a
a
a
a
a
a
i
i
‘ Fearne [eS oka [Poet Fe Gotan.)


### Lab Assignments & Solutions — strona 214

Note: Double-clicking the PKA file in your file explorer may not work (depending on the
Packet Tracer version).
Lab material includes the lab document and a PKA lab file.
When you open a PKA file in Cisco Packet Tracer, two windows appear:
1. Lab topology window
2. Activity window
PKA Features
Note the following essential information regarding the Activity window:

1. Completion percentage: Learner progress appears at the bottom right corner of
the window.

2. Check Results button: When you click this button and then click the Assessment
Items tab, you will find a checklist with lab objectives and status; V=done, X=not
done.

Note: Both features help the instructor grade the exercise swiftly and efficiently.

A PT Activity: 001012 - ao x ‘Expandialapas Al| Show incase Rena)

Dia ero ne cmt crf the = [Sa ra Compe [reek

‘See the percentage of completion at the right-bottom corner to E-NTP Sener o ‘Other

determine your progress. 5 NTP Sener o Other

Note: The Optional and Bonus section are not scored, eo mnie : »

Good Luck Vie ° ier
PKA Solution
To view the solution or edit the lab file, you can simply click the wizard hat icon and
enter the following password: C!ScOM@ster
Right-click the Answer network tab and then click Show Answer network.
Note: Be careful not to change anything so the lab will remain intact.


### Lab Assignments & Solutions — strona 215

Lab Task 1: Revision Questions
Answer the following questions as a review of VLANs.

1 What are the benefits of creating VLANs?

A VLAN is a switched network that is logically segmented on a network. VLANs can
improve security by isolating groups. Users can be grouped into VLANs, and no users
outside those VLANs will be able to communicate with them. VLANs also allow logical
network topologies to overlay the physical switched infrastructure. The technology
logically segments the network into separate Layer 2 broadcast domains, whereby
packets are switched between ports assigned to the same VLAN. By confining traffic
from one LAN to other LANs within the same VLAN, switched virtual networks avoid
wasting bandwidth.

2 What happens when a computer connected to a switch sends a broadcast, such

as an ARP request?
Switches broadcast ARP requests as entries in the ethernet header of FFFF.FFFF.FFFF
(broadcast MAC address) to all nodes, except the one that requests the ARP.

3 > Howcan we implement security on a network without using security protocols?
VLANs can be used to limit user access to certain network segments by granting only
authorized users access to networks with highly sensitive information.

4 Assuming a default switch configuration, what is the standard VLAN range that

can be modified and removed on a Cisco switch?
Only VLANs 2—1001 can be modified or removed.

5 Which configuration allows a port to carry traffic for multiple VLANs?

Trunk configuration allows traffic from multiple VLANs over a single link, and the
extension of VLANs across the network.


### Lab Assignments & Solutions — strona 216

Lab Task 2: Configure and Verify VLANs
On a switched network, there may be different types of device groups, such as
printers, workstations, and access points. By default, all interfaces on a switch can
communicate with each other.
VLANs permit the creation of virtual groups on the switch and assign interfaces to
different groups. Only interfaces in the same group are able to communicate with
each other.
Configure a VLAN on all network devices and verify that the VLANs were properly
configured using various troubleshooting methods.
Part 1: View the Default VLAN Configuration
1 Using the CLI, connect S1 and run the command that displays all configured
VLANs. Make sure all interfaces are assigned to VLAN 1, by using the command:
show vlan brief
S1>enable
S1#show vlan brief
VLAN Name Status Ports
[ <= =#=#=#=8 see Fa0/1, Fa0/2, FaO/3, Fao/4
Fa0/5, Fa0/6, Fa0/7, Fa0/s
Fa0/9, Fa0/10, FaQ/1l, Fa0/12
Fa0/13, Fa0/14, Fa0/15, Fa0/1é
Fa0/17, Fa0/18, Fa0/19, Fa0/20
Fa0/21, Fa0/22, Fa0/23, Fa0/24
Gig0/1, Gigd/2
1002 fddi-default active
1003 token-ring-default active
1004 fddinet-default active
1005 trnet-default active
Sl? ww


### Lab Assignments & Solutions — strona 217

2 Repeat step 1 on S2.
S2>enable
S2#show vlan brief
S2>enable
S2#show vlan brief
VLAN Name Status Ports
Fa0/5, Fa0/6, Fa0/7, Fao/s
Fa0/3, FaO/10, Fa0/11, Fa0/12
FaQ/13, Fa0/l4, Fa0/15, Fa0/16
Fa0/17, Fa0/18, Fa0/15, Fa0/20
Fa0/21, FaO/22, Fa0/23, Fa0/24
GigO/1, Gigd/2
1002 fddi-default active
1003 token-ring-default active
1004 fddinet-default active
1005 trmet-default active
524] v
Part 2: Create and Name VLANs
3. Create and name the following VLANs on S1:
a) VLAN 10: Workstation
b) VLAN 20: Servers
Sl#configure terminal
S1(config)#vlan 10
S1(config-vlan)#name Workstation
S1(config-vlan)#exit
S1(config)#vlan 20
S1(config-vlan)#name Servers
S1(config-vlan)#exit


### Lab Assignments & Solutions — strona 218

4 Using the same commands as those in the previous step, create and name the
same VLANs on S82.
S2#configure terminal
S2(config)#vlan 10
S2(config-vlan)#name Workstation
S2(config-vlan)#exit
S2(config)#vlan 20
S2(config-vlan)#name Servers
S2(config-vlan)#exit
Part 3: Assign VLANs to Ports
5 OnS1, assign the VLANs to the following ports:
a) All ports that connect to workstations and servers must be set in access
mode.

b) VLAN 10: Fast Ethernet 0/1-2

c) VLAN 20: Fast Ethernet 0/3
S1(config)#interface range fastethernet @/1-2
S1(config-if-range)#switchport mode access
S1(config-if-range)#switchport access vlan 10
S1(config-if-range)#exit
S1(config)#interface fastethernet 0/3
S1(config-if)# switchport mode access
S1(config-if)#switchport access vlan 20
S1(config-if)#exit


### Lab Assignments & Solutions — strona 219

6 0nS2, assign the VLANs to the following ports:
a) All ports that connect to workstations and servers must be set in access
mode.

b) VLAN 10: Fast Ethernet 0/1-4

c) VLAN 20: Fast Ethernet 0/5-6
S2(config)#interface range fastethernet @/1-4
S2(config-if-range)#switchport mode access
S2(config-if-range)#switchport access vlan 10
S2(config-if-range)#exit
S2(config)#interface range fastethernet @/5-6
S2(config-if-range)#switchport mode access
S2(config-if-range)#switchport access vlan 20
S2(config-if-range)#exit


### Lab Assignments & Solutions — strona 220

7 Verify S1 and S2 VLAN configuration using the do show vian brief command and
save the configuration.
S1(config)#do show vlan brief
S2(config)#do show vlan brief
Sis
S1(config)#do show vlan brief
VLAN Name Status Ports
1 default active Fag/4, Fa0/5, Fa0/é, Fad/7
Fa0/8, Fa0/9, Fa0/10, FaQ/1l
Fa0/12, Fa0/13, Fa0/14, Fa0/15
Fa0/16, Fa0/17, Fa0/18, Fao/19
Fa0/20, Fa0/21, Fa0/22, Fa0/23
Fa0/24, GigO/1, Gig0/2
10 Workstation active Fa0/l, Fa0/2
20 Servers active Fad/3
1002 fddi-default active
1003 token-ring-default active
1004 fddinet-default active
1005 trnet-default active
Si (contig) 4 Me
$2:
S2(config)#do show vlan brief
VLAN Name Status Ports
1 default active Fa0/7, Fa0/8, Fa0/9, Fa0/10
Fa0/ll, Fa0/12, Fa0/13, Fa0/14
Fa0/15, Fa0/lé, Fa0/17, Fad/18
Fa0/13, Fa0/20, Fa0/21, Fa0/22
Fa0/23, Fa0/24, GigQ/l, Gigd/2
190 Workstation active FaQ/l, Fa0/2, Fa0/3, Fao/4
20 Servers active Fao/5, Fao/é
1002 fddi-default active
1003 token-ring-default active
1004 fddinet—default active
1005 trnet-default active
S2 (config) # ¥


### Lab Assignments & Solutions — strona 221

Part 4: Configure and Verify Basic Connectivity
8 Assign IP addresses for all workstation hosts using the address range and subnet
mask: 10.0.0.0 255.255.255.0. Use the last available IP address as the default
gateway.
Rect - asx
Physical Config Desktop Programming Attributes
Inertace —_FastEthernef0 =
IP Configuration
O Duce @ Static
IPAddress
Subnet Mask
Default Gateway
ONS Serer
PC1: IP:10.0.0.1 SM:255.255.255.@ DG:10.0.0.254
PC2: IP:10.0.0.2 SM:255.255.255.@ DG:10.0.0.254
PC3: IP:10.0.0.3 SM:255.255.255.0 DG:10.0.0.254
PC4: IP:10.0.0.4 SM:255.255.255.@ DG:10.0.0.254
PC5: IP:10.0.0.5 SM:255.255.255.@ DG:10.0.0.254
PC6: IP:10.0.0.6 SM:255.255.255.@ DG:10.0.0.254
9 Assign IP addresses for all server hosts using the address range and subnet mask:
192.168.0.0 255.255.255.0. Use the last available IP address as the default
gateway.
B servert - a x
Physical ‘Config ‘Senices Desktop Programming Attributes
IP Configuration
© DHCP @ Static
IPAddress. 192 168.01 |]
‘Subnet Mask 255.255.255.0
Default Gateway 192 168.0 254
DNS Server 0.0.00 |
Server1: IP:192.168.0.1 SM:255.255.255.@ DG:192.168.0.254
Server2: IP:192.168.0.2 SM:255.255.255.@ DG:192.168.0.254
Server3: IP:192.168.0.3 SM:255.255.255.@ DG:192.168.0.254


### Lab Assignments & Solutions — strona 222

10 Perform a connectivity test between all workstations connected to switch S1.
ETH: aN ,
Rc 2nd 3rd — a 54
Ald
pcpTy PCPT .
PC1 Pc2
1st iP Dial-up Terminal ommand Web Br
Configuration Prompt |
C:\>ping 10.0.0.2
Pinging 10.0.0.2 with 32 bytes of data:
Reply from 10.0.0.2: bytes=32 time=1ms TTL=128
Reply from 10.0.0.2: bytes=32 time<Ims TTL=128
Reply from 10.0.0.2: bytes=32 time<lms TTL=128
Reply from 10.0.0.2: bytes=32 time<Ims TTL=128
Ping statistics for 10.0.0.2:
Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),
Approximate round trip times in milli-seconds:
Minimum = Oms, Maximum = lms, Average = Oms
11 Repeat the process from the previous step and test connectivity among
workstations connected to switch S2.
From PC3: Ping 10.0.0.6
5
Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),
Reply from 10.0.0.5: bytes=92 time<ims TTL=128
Reply from 10.0.0.5: bytes=32 time=Ims TTL=128


### Lab Assignments & Solutions — strona 223

12 Test connectivity between PC1 and PC6. The ping should fail.
RB eci - a x
Physical Config Desktop Programming Attributes


### Lab Assignments & Solutions — strona 224

Lab Task 3: Configure Trunks and Native VLAN
To enable VLAN communication between switches, we need to configure trunks.
Part 1: Configure Trunking Ports

1 Configure GigabitEthernet 0/1 on S11 as trunk.
S1(config)#interface gigabitethernet 0/1
S1(config-if)#switchport mode trunk
S1(config-if)#exit
S1(config)#exit

2 Configure GigabitEthernet 0/2 on S11 as trunk. Note: This is connected to the

router,

Sl#configure terminal
S1(config)#interface gigabitethernet 0/2
S1(config-if)#switchport mode trunk
S1(config-if)#exit

3 Configure GigabitEthernet 0/1 on S2 as trunk.
S2(config)#interface gigabitethernet 0/1
S2(config-if)#switchport mode trunk
S2(config-if)#exit
S2(config)#exit


### Lab Assignments & Solutions — strona 225

Part 2: Configure Native VLAN

4 Create VLAN 30 on both switches and name it Native.
S1(config)#vlan 30
S1(config-vlan)#name Native
S1(config-vlan)#exit
S2(config)#vlan 30
S2(config-vlan)#name Native
S2(config-vlan)#exit

5 Configure VLAN 30 as the native VLAN for GigabitEthernet0/1 interface on S1.
S1(config)#interface gigabitethernet 0/1
S1(config-if)#switchport trunk native vlan 30
S1(config-if)#exit

6 Configure VLAN 30 as the native VLAN for GigabitEthernet0/1 interface on S2.
S2(config)#interface gigabitethernet 0/1
S2(config-if)#switchport trunk native vlan 30
S2(config-if)#exit


### Lab Assignments & Solutions — strona 226

Part 3: Verify Trunk and Native Settings

7 Stay in global configuration mode. Note: The do command enables the privileged
mode command in global configuration mode.

8 Verify trunk and native VLAN configurations on both switches using the do show
interfaces trunk command. Note: You should see both VLANs assigned to the
appropriate ports, and for both switches, the native VLAN should be VLAN 30.

S1(config)#do show interface trunk
S2(config)#do show interface trunk
si:
$1 (config) #do show interface trunk
Port Mode Encapsulation Status Native vlan
GigO/1 on 802.1q trunking 30
Port Vians allowed on trunk
GigO/1 1-1005
Port Vians allowed and active in management domain
Gigd/1 1,10,20,30
Port Vlans in spanning tree forwarding state and not
pruned
GigO/1 1,10,20,30
$1 (config) 4 ~.
S2:
S2(config)#do show interface trunk
Port Mode Encapsulation Status Native vlan
Gigo/l on 802.1q trunking 30
Port Vians allowed on trunk
Gigd/1 1-1005
Port Vians allowed and active in management domain
GigO/1 1,10,20,30
Port Vians in spanning tree forwarding state and not pruned
Gigo/1 1,10,20,30
52 (config) # ba


### Lab Assignments & Solutions — strona 227

9 Save the configuration on both switches. Press Enter and do not write anything
after the question mark.
S1(config)#exit
Sl#copy running-config startup-config
Destination Filename [startup-config]?
S2(config)#exit
S2#copy running-config startup-config
Destination Filename [startup-config]?
Part 4: Verify Connectivity
10 Try to test connectivity between PC1 and PC3. The ping should succeed.
Pinging 10.0.0.3 with 32 bytes of data:
Reply from 10.0.0.3: bytes=32 time<lms TTL=128
Reply from 10.0.0.3: bytes=32 time<lms TTL=128
Reply from 10.0.0.3: bytes=32 time=lms TTL=128
Reply from 10.0.0.3: bytes=32 time=lms TTL=123
Ping statistics for 10.0.0.3:
Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),
Approximate round trip times in milli-seconds:
Minimum = Oms, Maximum = lms, Average = Oms


### Lab Assignments & Solutions — strona 228

11 Try to test connectivity between workstations and servers. The ping should fail.
C:\>ping 192.168.0.2
Pinging 192.168.0.2 with 32 bytes of data:
Request timed out.
Request timed out.
Request timed out.
Request timed out.
Ping statistics for 192.168.0.2:
Packets: Sent = 4, Received = 0, Lost = 4 (100% loss),
Ci\3 ie


### Lab Assignments & Solutions — strona 229

For different VLANs to communicate with each other, inter-VLAN routing must be
configured.
Part 1: Configure Router on a Stick on R1
1 Configure GigabitEthernet0/2 on S11 for trunking.
Sl#configure terminal
S1(config)#interface gigabitethernet 0/2
S1(config-if)#switchport mode trunk
S1(config-if)#exit
2 OnR1, enter global configuration mode.
R1>enable
Ril#configure terminal
3 Enter the GigabitEthernet0/0 interface and activate it using the no shutdown
command. Then return to global configuration.
R1(config)#interface gigabitethernet 0/0
R1(config-if)#no shutdown
R1(config-if)#exit
4 OnR1, create sub-interface GigabitEthernet 0/0.10
R1(config)#interface gigabitethernet 0/0.10
R1(config-subif)#
5 Set the encapsulation type to 802.1Q and assign VLAN 10 to the sub-interface.
R1(config-subif)#encapsulation dotiq 10
6 Referring to the addresses used in Lab Task 2, part 4, step 8, assign the correct IP
address and subnet mask to the sub-interface (workstations). Then return to
global configuration.
R1(config-subif)#ip address 10.0.0.254 255.255.255.0
R1(config-subif)#exit


### Lab Assignments & Solutions — strona 230

7 OnR1, create sub-interface GigabitEthernet 0/0.20
R1(config)#interface gigabitethernet 0/0.20
R1(config-subif)#
8 Set the encapsulation type to 802.1Q and assign VLAN 20 to the sub-interface.
R1(config-subif)#encapsulation dotiq 20
9 Referring to the addresses used in Lab Task 2, part 4, step 9, assign the correct IP
address and subnet mask to the sub-interface (servers).
R1(config-subif)#ip address 192.168.0.254 255.255.255.0
R1(config-subif)#exit
Part 2: Verify Settings and Inter-VLAN Connectivity
10 On the router, verify the configuration using the show ip interface brief and
show running-config commands.
R1(config)#do show ip interface brief
R1(config)#do show running-config
Rl(config)#do show ip interface brief
Interface IP-Address OK? Method Status
Protocol
GigabitEthernet0/0 unassigned YES NVRAM up up
GigabitEthernet0/0.10 10.0.0.254 YES manual up up
GigabitEthernet60/0.20 192.1668.0.254 YES manual up up
GigabitEthernet0/1 unassigned YES NVRAM administratively down down
Vlanl unassigned YES unset administratively down down
Rl (config) # vv
R1# show running-config


### Lab Assignments & Solutions — strona 231

no ip address
duplex auto
speed auto
interface GigabicEthernet0/0.10
encapsulation dot1Q 10
ip address 10.0.0.254 255.255.255.0
interface GigebitEtherncto/0.20
ip address 192.168.0.254 255.255.255.0
anterface GigabirEtnernet0/1
no ip address
duplex auto
speed auto
shuedown
no ip address
=-More-- “
11 Save the configuration.
R1(config)#exit
Rl#copy running-config startup-config
12 From PC1, ping all other PCs and servers. All pings should be successful.
C:\>ping 192.168.0.1
Pinging 192.168.0.1 with 32 bytes of data:
Request timed out.
Reply from 192.168.0.1: bytes=32 time<lms TTL=127
Reply from 192.168.0.1: bytes=32 time<lms TTL=127
Reply from 192.168.0.1: bytes=32 time<lms TTL=127
Ping statistics for 192.168.0.1:
Packets: Sent = 4, Received = 3, Lost = 1 (25% loss),
Approximate round trip times in milli-seconds:
Minimum = Oms, Maximum = Oms, Average = Oms


# NET-10-LS1 — Configure NTP and Syslog

> Zakres źródłowy: strony 232–245.


### Lab Assignments & Solutions — strona 232

Computer Networking
Lab Assignment Diagnostics &
& Solution Troubleshooting
sohRe NET-10-LS1
ol Configure NTP and Syslog
El


### Lab Assignments & Solutions — strona 233

Note: Solutions for the instructor are shown inside the green box.
@ Lab Objective
Understand what syslog services are used for and how syslog works in tandem with NTP
services.
* Lab Mission
Configure a syslog server and an NTP server to log events across the network.
Then, configure a router to send system logs to the syslog server.
rx) .
@ Lab Duration
30-50 minutes
fe Requirements
e Knowledge of basic Cisco IOS commands and navigation
Lt
[ra] Resources
e Tools
o Cisco Packet Tracer 7.2.2 or higher
e Extra Files
o NET-10-L1.pka


### Lab Assignments & Solutions — strona 234

Instructions for PKA Lab Files
Lab material includes the lab document and a PKA lab file.
Open the PKA file through the Cisco Packet Tracer menu by clicking File and then
Open....
Bet 2 2QQOR Eee 2
Orcs aay aT)
a see on ee
WB Poot Cte
29 4 OORBSSSSCSSSeSeeg
S28 0 fe Ep mama menmEs
Navigate to the file's location and open it.
a
a t) %
5
8
a
a
a
a
4
4
1


### Lab Assignments & Solutions — strona 235

Note: Double-clicking on the PKA file in your file explorer may not work (depending on

the Packet Tracer version).

Lab material includes the lab document and a PKA lab file.

When you open a PKA file in Cisco Packet Tracer, two windows appear:

1. Lab topology window

2. Activity window

PKA Features

Note the following essential information regarding the Activity window:

¢ Completion Percentage: Learner progress appears at the bottom right corner of the
window.

e Check Result Button: When you click this button and then click the Assessment
Items tab, you will find a checklist with lab objectives and status, where V = done
and X = not done.

Note: Both features help the instructor grade the exercise swiftly and efficiently.

instructions. a

See the percentage of completion a the rght- bottom commer to ST et 2 ter
determine your progres aS 3 oe
Note:The Optional and Bonus section are not scored oe Se —_ : :
Good Luck a ; “a

PKA Solution

To view the solution or edit the lab file, you can simply click the Wizard hat icon and

enter the following password: C!ScOM@ster

Right-click the Answer network tab and then click Show Answer network.

Note: Be careful not to change anything so that the lab will remain intact.


### Lab Assignments & Solutions — strona 236

Lab Task 1: Revision Questions
Answer the following questions to review event logging and NTP.
1 Explain what a syslog server is.
Syslog is a message logging server that collects and stores all the syslog messages that
are sent to it.
2 What is the default location of device log files?
The device RAM
3 How many severity levels are there?
There are eight severity levels:
Trap Level: Severity:
0 Emergency
1 Alert
2, Critical
3 Error
4 Warning
5 Notification
6 Informational
7 Debugging
4 Explain what an NTP server is.
NTP stands for Network Time Protocol and is used for clock synchronization among
network devices and computers. The server provides the time for other devices.


### Lab Assignments & Solutions — strona 237

Lab Task 2: Configure Syslog
Configure a server with the syslog service to obtain network event logs.
Part 1: Enable logging to the server on R1
1 Save the current running configuration into NRAM.
Command: copy running-config startup-config
Learners need to do this to have the startup configuration match the base
running configuration file. Do not skip this step!
2 Goto the syslog server Services tab and make sure the SYSLOG service is
enabled.
{ Ld S 1st
Physical Config Cee] omrey Programming Attributes
SERVICES
Syslog
HTTP d
Te Syslog FI]
DHCP V6 Service O of
TFTP Time HostName Message
DNS
i, Se |
1 DAA
3. What is a logging buffer?
It is a predetermined storage size allocated on RAM for syslog messages.


### Lab Assignments & Solutions — strona 238

4 From R1, ping the syslog server to verify connectivity.
R1> ping 192.168.0.10
ra veiling 192.168.0.10
Type escape sequence to abort.
Sending 5, 100-byte ICMP Echos to 192.168.0.10, timeout is 2
seconds:
Success rate is 100 percent (5/5), round-trip min/avg/max = 0/0/1
pas v
5 Configure R1 to send events and logs to the syslog server.
R1> enable
R1#configure terminal
R1(config)#logging host 192.168.0.10
6 Permit the logging of security severity level 7 (debugging) and exit global mode.
R1(config)#logging trap debugging
R1(config)#exit
Rl(config) #logging trap debugging
Rl (config) #exit
Rl¢#
%5YS-5-CONFIG_I: Configured from console by console
%SYS-6-LOGGINGHOST_STARTSTOP: Logging to host 192.168.0.10 port
514 started - CLI initiated
R1# fot


### Lab Assignments & Solutions — strona 239

7 Enable debugging for the ICMP protocol and ping PC1.
R1#debug ip icmp
R1#ping 172.16.0.2
a a
TCMP packet debugging is on
Rl¢
Type escape sequence to abort.
Sending 5, 100-byte ICMP Echos to 172.16.0.2, timeout is 2
seconds:
ICMP: echo reply rcvd, src 172.16.0.2, dst 172.16.0.1
ICMP: echo reply rcvd, src 172.16.0.2, dst 172.16.0.1
ICMP: echo reply revd, src 172.16.0.2, dst 172.16.0.1
ICMP: echo reply revd, src 172.16.0.2, dst 172.16.0.1
Success rate is 100 percent (5/5), round-trip min/avg/max = 0/0/0
ms
Rlt
ICMP: echo reply revd, src 172.16.0.2, dst 172.16.0.1
v


### Lab Assignments & Solutions — strona 240

Part 2: Verify Syslog settings
8 Use the show running-config command on R1 to verify the settings.
R1#show running-config
: a
interface GigabitEthernet0/1
ip address 172.16.0.1 255.255.0.0
duplex auto
speed auto
interface Vlanl
no ip address
shutdown
ip classless
ip flow-export version $
logging trap debugging
logging 192.168.0.10
line con 0
v
9 Goto the syslog server again, and, in the Services tab, click SYSLOG and verify
log operation.
Note: The logs currently do not include a timestamp because NTP is still not set
up.
® syslog server - ia x
Physical Config Services Desktop Programming —_ Attributes
SERVICES
Syslog
Linke Syslo.
DHCP aaa
DHCPv6é Senice @ On O of
TFTP Time HostNiame Message a|
DNS
[__systoc | 1 pont ICMP: echo reply
BAA
ae al bicabimt ICMP: echo reply
EMAIL 3 |= 192.168.0.1 ICMP: echo reply
FIP
IoT ill ddr ICMP- echo repl


### Lab Assignments & Solutions — strona 241

Lab Task 3: Configure NTP
Configure the NTP server to work with the syslog server and provide unified
timestamps across the network.
Part 1: Enable NTP on R1
1 Goto the NTP server Services tab and make sure that the NTP service is enabled.
® NTP Server ist - Oo x
Physical Config Desktop Programming Attributes,
SERVICES NTP
HTTP 3rd
DHCPv6 Authentication
TFTP © Enable @ Disable
DNS
aie aha Key Password
2 > What can operate as an NTP server?
Any device that offers the feature can operate as an NTP server: switches, routers,
servers, and others.


### Lab Assignments & Solutions — strona 242

3. Make sure the correct date and time are set on the server. Adjust them if
necessary.
® NTP Server = Oo x
Physical Config _ Services Desktop Programming Attributes
SERVICES NTP
HTTP
ae Service @© On O of
nae Authentication
TFTP O Enable @ Disable
oe Key Password
SYSLOG
Be € April, 2020 P| 11-32:52am 5]
EMAIL Sun Mon Tue Wed Thu Fri
FTP a
2 | 3 | 31 | 1 | 2] 3
ToT
VM Management 5 6 7 8 9 10
Radius EAP
wz | 13 | 4 | 15 | 16 | 47
19 20 210 22 | 8h
2% 7 2 8 8 t
3|/4]s5s]6]7]8
D Top


### Lab Assignments & Solutions — strona 243

4 From R1, ping the NTP server to verify connectivity.
R1#configure terminal
R1(config)#do ping 192.168.0.20
Rléconf t
Enter configuration commands, one per line. End with CNTL/Z.
Rl (config)#do ping 192.168.0.20
Type escape sequence to abort.
Sending 5, 100-byte ICMP Echos to 192.168.0.20, timeout is 2
seconds:
ome: echo reply revd, src 192.168.0.20, dst 192.168.0.1
ICMP: echo reply revd, src 192.168.0.20, dst 192.168.0.1
ICMP: echo reply rcvd, src 192.168.0.20, dst 192.168.0.1
Success rate is 80 percent (4/5), round-trip min/avg/max = 0/0/1
ms
Rl (config) #
ICMP: echo reply revd, src 192.168.0.20, dst 192.168.0.1
v
5 Configure R1 to get the time and date from the server dynamically.
R1(config)#ntp server 192.168.0.20
R1(config)#exit


### Lab Assignments & Solutions — strona 244

Part 2: Verify NTP settings
6 Display the R1 clock to verify time settings.
Important: If the clock was not changed, click Fast forward at the bottom left
corner several times and check again.
R1#show clock
- :
BmeBOrcaRArVAQRQOA ESS 2?
MQek Bree mn
[A Logical] Physical)x 891,359 Root] aD) i( a i im \( a (00:15:09)
me 192.166 0.0724
Geo Gigolo
an
_ ag Fa02 Fa0
| ven —
S1
NTP Server
4 a,
Fao
Fa
Pet Sysloa sever
192.168.0.10
Timo: 00:01:14 ©) i( > ) (Q Reaitime) Simulation
BIS DT OGESSsesaaacausce
i net Case ant [ant ite sir Cas) Cs) bro omy Las =)
Rl#show clock
16:15:43.724 UTC Mon Mar 30 2020
Riz »


### Lab Assignments & Solutions — strona 245

7 Enable the log timestamp services with milliseconds.
R1#configure terminal
R1(config)#service timestamps log datetime msec
R1(config)#exit
8 From R1, ping the NTP server to generate new log messages.
Ri#ping 192.168.0.20
Note: The time and date should be next to the log massage:
Rl#ping 192.168.0.20
Type escape sequence to abort.
Sending 5, 100-byte ICMP Echos to 192.168.0.20, timeout is 2 seconds:
*Mar 30, 16:25:18.2525: ICMP: echo reply rcvd, src 192.168.0.20, dst 192.168.0.1!
*Mar 30, 16:25:18.2525: ICMP: echo reply rcevd, src 192.168.0.20, dst 192.168.0.1!
*Mar 30, 16:25:18.2525: ICMP: echo reply rcvd, src 192.168.0.20, dst 192.168.0.1!
*Mar 30, 16:25:18.2525: ICMP: echo reply rcvd, src 192.168.0.20, dst 192.168.0.1!
Success rate is 100 percent (5/5), round-trip min/avg/max = 0/0/0 ms
Rl#
*Mar 30, 16:25:18.2525: ICMP: echo reply rcvd, src 192.168.0.20, dst 192.168.0.1
Rid ¥
9 Goto the syslog server, review the logs, and make sure the logs have the correct
time and date.
B® sysiog server - a cd
Physical Confg _Senices_ Desktop Progiomming Atribtes
SERVICES
sysieg
HTTP :
syslog
DHCP
Eee Senice @on Oot
Balad Time HosiName Message an
DNs
aa 1 09.30.2020 04.26 46.788 Pu fis2 1600.1 a
ae 2 ca3e 2020 04-2646 606 Puce e804 a
ema 3. 230.2020 0426.46 573 Pw f192 168.04 lspcccrsrnmranen
ww 4 03:30.2020 04:2646.404 Paige 19.0.1 baeesermmsre
ve vecooeert 5 03.30.2020 0426 6.364 palpi 168.01 leesenaranaere
6 03.30.2020 0425-16910 euifi 168.01 leeemeopmeaee
7 0330.2020 0425.16.02 Pw ft 168.01 eaasecweesaesatse
6 03.30.2020 0425-1700 paifigo 168.01 ena.
Gearlog


# NET-11-LS1 — Implement Standard and Extended ACLs

> Zakres źródłowy: strony 246–266.


### Lab Assignments & Solutions — strona 246

Computer Networking
Lab Assignment Access Control Lists
& Solution
NET-11-LS1
rr Implement Standard
o [ire and Extended ACLs
Oln
EI
Copyright © 1996-2020 HackerU Ltd.
All Rights Reserved.


### Lab Assignments & Solutions — strona 247

Note: Solutions for the instructor are shown inside the green box.
G Lab Objective
Practice setting up ACLs, and compare Named and Numbered ACLs, and Standard and
Extended ACLs.
bs Lab Mission
Learn the different ways to configure ACLs to secure parts of a network from
unauthorized users or machines, and which ACLs are best suited for specific use
cases.
ea 7
©) Lab Duration
60-100 minutes
fe Requirements
e Basic knowledge of IOS commands and navigation.
e Basic knowledge of wildcard address calculation.
e Basic knowledge of the standard and extended ACL concepts, and how they operate.
oo
| Resources
© Tools
Cisco Packet Tracer 7.2.2, or higher
e Extra Files
NET-11-L1.pka


### Lab Assignments & Solutions — strona 248

Instructions for PKA Lab Files
Lab material includes the lab document and a PKA lab file.
Open the PKA file through the Cisco Packet Tracer menu by clicking "File" and then
"Open...".
bw ae 2 QQQ0R Ese 2
Bran ome ore)
Open Acti Seance ae 04039)
Print CuleP
ed
Navigate to the file's location and open it.
a
a A t)
a
a
a
-
a
i
i
1
lena [NE-03 La Se


### Lab Assignments & Solutions — strona 249

Note: Double-clicking the PKA file in your file explorer may not work (depending on the
Packet Tracer version).
Lab material includes the lab document, and a PKA lab file.
When you open a PKA file in Cisco Packet Tracer, two windows appear:
1. Lab topology window
2. Activity window
PKA Features
Note the following essential information regarding the Activity window:
1. Completion Percentage — Student progress appears at the bottom right corner of
the window.
2. Check Result Button — When you click this button and then click the "Assessment
Items" tab, you will get a checklist with lab objectives and status, whereby V=done,
X=not done.
Note: Both features help the instructor grade the exercise swiftly and efficiently.
Cera Feedback _ Assessor: tons Comecthy Tet
Eapaaapse al [Shon nce Re
BR PT Activity 000012 - oOo x ‘Assessment tems Stas Points Components) | Feedback
Please fer to the exerise document and carefully low the SNe he
determine your progress, eR
Note The Optonal and Bonus scion are not sored a 0 other
Good Luck! ‘KK Semce timestamp log Incorrect 1 Other
= 3 Omer
Fre Sane oman } ote
eee comet ‘ one
> syetod viet H one
Altess———ncoect ' one,
Time a » SYSLOG Sener 0 ee
PKA Solution
To view the solution or edit the lab file, you can click the "Wizard hat" icon, and enter
the following password: C!ScOM@ster
Right-click the "Answer network" tab and then click "Show Answer network".
Note: Be careful not to change anything, so that the lab will remain intact.


### Lab Assignments & Solutions — strona 250

Lab Task 1: Revision Questions
IP ACL (Access Control List) is a rule-based feature in Cisco routers that enables network
administrators to identify packet types. An ACL can identify a packet by source or
destination IP address, or source or destination port. When a router identifies a packet
that matches an ACL, one of several actions can be taken by the router.
Complete the following questions to review ACLs.

1. What is the difference between named and numbered ACLs?
Numbered ACLs use numbers for identification, while named ACLs use names for
identification.

2 True or False: Standard ACLs filter traffic only by the destination IP address.
False - A standard ACL filters traffic by source IP address.

3 What is the default ACE located at the end of any IPv4 ACL?
Implicit Deny.

4 Does a router verify every packet it forwards against an ACL in chronological

order?
Yes - Every inbound or outbound packet parameter is checked according to the received
information in every ACE. For example, if you send a stateful packet out via HTTP it is
only checked against the outbound rules. The return packet is not checked. On the flip
side, if you send out a stateless packet like SNMP, the return packet is a new packet and
checked against inbound rules.
Page5


### Lab Assignments & Solutions — strona 251

Lab Task 2: Configure a Numbered Standard ACL
Use a numbered ACL to block traffic from the marketing network to the server farm.
192,168, 1.0/24 RAD 172.16.1.0/24 Server Farm
AA ara
™ 10.0.0,0/30 .: 80.10. 10.0/30 —_
2901
SP
a oa a ]
192.168.2.0/24 Management 172.16.2.0/24 Marketiog
Part 1: Create the ACL
In R2, configure the network policies in accordance with the following steps:
1 Create a standard ACL numbered 1.
R2>enable
R2#configure terminal
R2(config)#ip access-list standard 1
R2(config-std-nacl)#exit


### Lab Assignments & Solutions — strona 252

2 OnR2, add the appropriate ACEs to meet the following requirements:
a) Traffic from the marketing (172.16.2.0/24) network to the server farm is not
permitted.
b) All other network traffic is permitted.
R2(config)#access-list 1 deny 172.16.2.0 0.0.0.255
R2(config)#access-list 1 permit any
3° What is the wildcard mask for /24?
(0100) 225;5)
Part 2: Apply the ACL on the Correct Interface
4 Apply the ACL you created on the correct interface for inbound traffic.
Tip: Apply standard ACLs as close as possible to the destination, and for outbound
traffic.
R2(config)#interface gigabitethernet 0/0
R2(config-if)#ip access-group 1 out
R2(config-if)#exit
Note: Gigabitethernet 0/0 is closest to the server farm (the destination of the traffic we
want to check).


### Lab Assignments & Solutions — strona 253

Part 3: Verify the ACL Configuration
5 Use show access-lists to view the ACL configuration, and show running-config to
verify the application of the ACL on GigabitEthernet 0/0.
R2(config)#do show access-lists
R2 (config) ¢#
R2 (config) #do show access-lists
Standard IP access list 1
10 deny 172.16.2.0 0.0.0.255
20 permit any
R2 (config) # “
R2(config)#do show running-config
q “a
interface GigabitEtherneto/o
4p address 172.16.1.100 255.255.255.0]
ip access-group 1 out
duplex auto
speed auto
interface GigabitEthernet0/1
ip address 172.16.2.100 255.255.255.0
duplex auto
speed auto
interface GigabitEthernet6/0/0
ip address 10.0.0.2 255.255.255.252
qacevewee GigabitEthernet0/1/0
ip address 90.10.10.1 255.255.255.252
aeeReMce GigabitEthernet0/2/0
no ip address
shutdown
\
--More-- bs


### Lab Assignments & Solutions — strona 254

6 Use ping to verify that the configuration is correct.
From a PC in the marketing network (such as 172.16.2.1), try to ping a server (such
as 172.16.1.1). The ping should fail.
Other hosts on different networks should have access. Ping the same server again,
but from a PC in the management network (such as 192.16.2.1), and compare the
results with the previous test.
Ping 172.16.1.1 from 172.16.2.1
C:\>ping 172.16.1.1
Pinging 172.16.1.1 with 32 bytes of data:
Reply from 172.16.2.100: Destination host unreachable.
Reply from 172.16.2.100: Destination host unreachable.
Reply from 172.16.2.100: Destination host unreachable.
Reply from 172.16.2.100: Destination host unreachable.
Ping statistics for 172.16.1.1:
Packets: Sent = 4, Received = 0, Lost = 4 (100%
loss),
Ping 172.16.1.1 from 192.168.2.1
C:\>ping 172.16.1.1
Pinging 172.16.1.1 with 32 bytes of data:
Reply from 172.16.1.1: bytes=32 time<lms TTL=126
Reply from 172.16.1.1: bytes=32 time=12ms TTL=126
Reply from 172.16.1.1: bytes=32 time=14ms TTL=126
Reply from 172.16.1.1: bytes=32 time=14ms TTL=126
Ping statistics for 172.16.1.1:
Packets: Sent = 4, Received = 4, Lost = 0 (0%
loss),
Approximate round trip times in milli-seconds:
Minimum = Oms, Maximum = 14ms, Average = 10ms


### Lab Assignments & Solutions — strona 255

Lab Task 3: Configure a Named Standard ACL
Use a named standard ACL to block traffic from a specific host PC to the R&D network.
Part 1: Create the ACL
In R1, configure the network policies in accordance with the following steps:
1 Create a standard ACL named BLOCK_HOST (case-sensitive).
R1>enable
Rl#configure terminal
R1(config)#ip access-list standard BLOCK_HOST
R1(config-std-nacl)#
2 Add the appropriate ACEs to meet the following requirements:
a) Traffic from the 192.168.2.1 host to the 192.168.1.0/24 network is not
permitted.
b) All other network traffic is permitted.
R1(config-std-nacl)#deny host 192.168.2.1
R1(config-std-nacl)#permit any
R1(config-std-nacl)#exit
3 What is the default standard ACL number range?


### Lab Assignments & Solutions — strona 256

Part 2: Apply the ACL on the correct interface
4 Apply the ACL you created on the correct interface for outbound traffic.
R1(config)#interface gigabitethernet 0/0
R1(config-if)#ip access-group BLOCK_HOST out
R1(config-if)#exit
Part 3: Verify the ACL Configuration
5 Use show access-lists to view the ACL configuration, and show running-config to
verify the application of the ACL on GigabitEthernet 0/0.
R1(config)#do show access-lists
Rl (config) #do Show access—lists
Standard IP access list BLOCK_HOST
10 deny host 192.168.2.1
20 permit any
Rl (config) #| S
R1(config)#do show running-config
a ra
interface GigabitEthernet0/0
ip address 152.168.1.100 255.255.255.0
ip access-group BLOCK_HOST out
duplex auto
speed auto
ineeeracs GigabitEthernet0/1
ip address 192.168.2.100 255.255.255.0
duplex auto
speed auto
dnb race GigabitEtherneto/0/0
ip address 10.0.0.1 255.255.255.252
ft
interface GigabitEthernet0/1/0
no ip address
shutdown
ft
interface GigabitEthernet0/2/0
no ip address
shutdown
dopertace Vianl
--More-- iad


### Lab Assignments & Solutions — strona 257

6 Ping both computers on the 192.168.1.0/24 network from the host 192.168.2.1.
The test should fail.
To verify that only this host is blocked, try pinging the same computers from the
second host 192.168.2.2. The ping should be successful.
Ping 192.168.1.1 from 192.168.2.1
C:\>ping 192.168.1.1
Pinging 192.168.1.1 with 32 bytes of data:
Reply from 192.168.2.100: Destination host unreachable.
Reply from 192.168.2.100: Destination host unreachable.
Reply from 192.168.2.100: Destination host unreachable.
Reply from 192.168.2.100: Destination host unreachable.
Ping statiarics for 192.168 1.04
Packets: Sent = 4, Received = 0, Lost = 4 (100% loss),
Ping 192.168.1.2 from 192.168.2.2
c:\>ping 192.168.1.2
Pinging 192.168.1.2 with 32 bytes of data:
Reply from 192.168.1.2: bytes=32 time<lms TTL=127
Reply from 192.168.1.2: bytes=32 time=Ims TTL=127
Reply from 192.168.1.2: bytes=32 time=6éms TTL=127
Reply from 192.168.1.2: bytes=32 time=12ms TTL=127
Ping Statistics for 192.166.1.2*
Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),
Approximate round trip times in milli-seconds:
Minimum = Oms, Maximum = 12ms, Average = 4ms
'
Sa’ | Important!
o © * | Continue to task 4 only after learning about extended ACL, and when you
= are instructed to do so! Don’t close Packet Tracer after completing Task 3.


### Lab Assignments & Solutions — strona 258

Lab Task 4: Configure a Numbered Extended ACL
Use an extended numbered ACL to block traffic from an endpoint on the marketing
network to an endpoint on the R&D network.
Part 1: Create the ACL
In R2, configure the network policies in accordance with the following steps:
1 Create an Extended ACL numbered 100.
R2(config)#ip access-list extended 100
R2(config-ext-nacl)#exit
2 Add the appropriate ACEs to meet the following requirements:
a) Traffic from host 172.16.2.1 to host 192.168.1.2 is not permitted.
b) All other network traffic is permitted.
R2(config)#access-list 100 deny ip host 172.16.2.1 host
192.168.1.2
R2(config)#access-list 100 permit ip any any
3 What is the default extended ACL number range?
100-199, 2000-2699
4 What will happen if we type “deny any” in the first statement?
All traffic will be denied.


### Lab Assignments & Solutions — strona 259

Part 2: Apply the ACL on the correct interface
5 Apply the ACL you created on the correct interface for inbound traffic.
Tip: Apply extended ACLs as close as possible to the source, and for inbound
traffic.
R2(config)#interface gigabitethernet 0/1
R2(config-if)#ip access-group 100 in
R2(config-if)#exit
Part 3: Verify the ACL configuration
6 Use show access-lists to view the ACL configuration, and show running-config to
verify the application of the ACL on GigabitEthernet 0/1.
R2(config)#do show access-lists
R2 (contig) #do show access-lists
Standard IP access list 1
10 deny 172.16.2.0 0.0.0.255
Extended 7 access list 100
10 deny ip host 172.16.2.1 host 192.168.1.2
20 permit ip any any
R2 (config) # he
R2(config)#do show running-config


### Lab Assignments & Solutions — strona 260

! “a
interface GigabitEthernet0/0
ip address 172.16.1.100 255.255.255.0
ip access-group 1 out
duplex auto
speed auto
interface GigabitEthernet0/1
ip address 172.16.2.100 255.255.255.0
ip access-group 100 in
duplex auto
speed auto
J
interface GigabitEtherneto/0/0
ip address 10.0.0.2 255.255.255.252
J
interface GigabitEthernet0/1/0
ip address 80.10.10.1 255.255.255.252
J
interface GigabitEthernet0/2/0
no ip address
shutdown
4
interface Vlanl
--More-- mA
7 Use ping to make sure both hosts cannot communicate with each other.
However, use ping to verify that other hosts will be able to access the 192.168.1.2
host.
Ping from 172.16.2.1 to 192.168.1.2
c:\>ping 192.168.1.2
Pinging 192.168.1.2 with 32 bytes of data:
Reply from 172.16.2.100: Destination host unreachable.
Reply from 172.16.2.100: Destination host unreachable.
Reply from 172.16.2.100: Destination host unreachable.
Reply from 172.16.2.100: Destination host unreachable.
Ping statistics for 19?.168.1..2*
Packets: Sent = 4, Received = 0, Lost = 4 (100% loss),


### Lab Assignments & Solutions — strona 261

Ping from 172.16.2.2 to 192.168.1.2

C:\>ping 192.168.1.2
Pinging 192.168.1.2 with 32 bytes of data:
Reply from 192.168.1.2: bytes=32 time=13ms TTL=126
Reply from 192.168.1.2: bytes=32 time<lms TTL=126
Reply from 192.168.1.2: bytes=32 time<ims TTL=126
Reply from 192.168.1.2: bytes=32 time<lms TTL=126
Ping statistics for 192.168.1.2:

Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),
Approximate round trip times in milli-seconds:

Minimum = Oms, Maximum = 13ms, Average = 3ms


### Lab Assignments & Solutions — strona 262

Lab Task 5: Configure a Named Extended ACL (Bonus)
Use an Extended Named ACL to block HTTP traffic from a host on the R&D network to
the web server on the Server Farm network.
Part 1: Create the ACL
In R1, configure the network policies in accordance with the following steps:

1 Create an extended ACL named BLOCK_HTTP (case-sensitive).
R1(config)#ip access-list extended BLOCK_HTTP
R1(config-ext-nacl)#

2 Add the appropriate ACEs to meet the following requirements:

a) Web traffic (HTTP) from the 192.168.1.2 host to the web server is not
permitted.
b) All other network traffic is permitted.

R1(config-ext-nacl)#deny tcp host 192.168.1.2 host 172.16.1.2 eq
80
R1(config-ext-nacl)#permit ip any any
R1(config-ext-nacl)#exit
Part 2: Apply the ACL on the correct interface

3 Apply the ACL you created on the correct interface for inbound traffic.
R1(config)#interface gigabitethernet 0/0
R1(config-if)#ip access-group BLOCK_HTTP in
R1(config-if)#exit


### Lab Assignments & Solutions — strona 263

Part 3: Verify the ACL configuration
4 Use show access-lists to view the ACL configuration, and show running-config to
verify the application of the ACL on GigabitEthernet 0/0.
R1(config)#do show access-lists
Rl(config)#do show access—lists
Standard IP access list BLOCK_HOST
10 deny host 192.168.2.1
20 permit any (4 matchi(es
extended IP access list BLOCK HITP
10 deny tcp host 152.168.1.2 host 172.16.1.2 eq waw
20 permit ip any any
Rl (config) # ~
R1(config)#do show running-config
! a
4
4
interface GigabitEtherneto/0
ip address 192.168.1.100 255.255.255.0
ip access-group BLOCK HOST out
duplex auto
speed auto
interface GigabitEthernet0/1
ip address 192.168.2.100 255.255.255.0
duplex auto
speed auto
a
interface GigabitEtherneto/0/0
ip address 10.0.0.1 255.255.255.252
4
interface GigabitEtherneto/1/0
no ip address
shutdown
a
interface GigabitEthernet0/2/0
--More-- nd
R1(config)#exit


### Lab Assignments & Solutions — strona 264

5 Open 192.168.1.2, click the Desktop tab, click the web browser icon, and try to
access the www.cyberpro.com website. Can you view the website? Why?
Try to access the website from the 192.168.1.1 web browser. Can you view the
website? Why?
From PC 192.168.1.2, browse to www.cyberpro.com (unsuccessful).
Answer: No, traffic to port 80 is blocked.
ad
Physical Config Desktop Programming Attributes
<> URL http:/Awww.cyberpro.com
Request Timeout
From PC 192.168.1.1, browse to www.cyberpro.com (successful).
Answer: Yes, the ACL only applies to the 192.168.1.2 host.
eae
Fe re
Cyber Pro
Well done! You made it!
“If you can dream it, you can do it.” —Walt Disney
Are you up for another challenge?
Block all incoming PING requests to the Server Fram. All other network traffic is permitted.
Good Luck!


### Lab Assignments & Solutions — strona 265

Lab Task 6: Modify an Extended ACL (Bonus)
Modify an existing Extended ACL to include an ACE that will block HTTPS traffic.
Part 1: Modify the ACL
Since a new policy was issued, we need to edit the extended ACL from Lab Task 5
above. Secure web traffic (HTTPS) is now also not permitted between the 192.168.1.2
host and the web server. Make the appropriate changes to the ACL.
1 In R1, run show access lists. You should see two ACEs under the extended ACL
from Lab Task 5. The ACEs are listed in numerical order, whereby the first ACE is
10, the second is 20, and so on. This means numbers 11 to 19 are free and can be
used to add new ACEs in the correct positions in the ACL.
Rl#show access-lists
R1l¢
Rl#show access-lists
Standard IP access list BLOCK HOST
10 deny host 192.168.2.1 |
20 permit any (4 match (es))
Extended IP access list BLOCK HTTP ss
First
R1#| Mw
2 The newACE needs to come after the first ACE, but before the last (permit any)
ACE (hint: 11-19).
Rl#configure terminal
R1(config)#ip access-list extended BLOCK_HTTP
R1(config-ext-nacl)#15 deny tcp host 192.168.1.2 host 172.16.1.2
eq 443
R1(config-ext-nacl)#exit


### Lab Assignments & Solutions — strona 266

3 Use show access-lists to verify that the new ACE was added correctly.
R1(config)#do show access-lists

Ri(config)#do show access—lists

Standard IP access list BLOCK_HOST
10 deny host 192.168.2.1
20 permit any

Extended IP access list BLOCK_HTTP
10 deny tcp host 192.168.1.2 host 172.16.1.2 eq www
HS deny tcp host 192.168.1.2 host 172.16.1.2 eq 443
20 permit ip any any


---

# 04 — Padriseup / Riseup Computer Networking — pełne notatki

Źródło: `Padriseup Computer Networking.pdf` (30 stron). Plik ma natywną warstwę tekstową, więc poniżej zachowano jego treść bez OCR.


### Padriseup — strona 1

Grupa: BM080723UJ
Uczelnia: Jagiellonian University-Krakow
Rodzaj kursu: Blue Main Bi-Weekly
Czas trwania zajęć: 8 h
International Computer Networking for Blue Team
https://www.hackampus.com/book/480
Wykładowca: Jacek Wislak jacek.w@hackeru.com
TA: Mateusz Włodarczyk, Adam Milian
UWAGA, UWAGA!
Riseup nie zastępuje własnych notatek, ma jedynie na celu usprawnienie prowadzenia
zajęć.
Zalecamy prowadzenie notatek z zajęć we własnym zakresie - zdecydowanie usprawni to
przyswojenie materiału z zajęć.
UWAGA, UWAGA!
​
Zasady przyjaznego chatu:
1.​ Problemy opisujemy w wiadomości publicznej, dzięki temu inni też skorzystają.​

2.​ Precyzyjny opis i screenshoty przyśpieszają rozwiązywanie problemów.​

3.​ Powstrzymujemy się od pisania nie na temat.​

4.​ Jeśli ktoś czegoś nie wie to trzeba pytać (wstydliwi mogą na priv).​

5.​ Używanie imienia i nazwiska na Zoomie ułatwia weryfikowanie obecności.​

6.​ Spóźnienie zgłaszaj do TA.​

Drodzy Państwo, kurs jest intensywny, wiedzę buduje się warstwami, więc zalecamy po
każdych zajęciach :
1.​ powtórzyć cały materiał z zajęć​

2.​ przejść jeszcze raz przez laby​

3.​ przeczytać materiały dodatkowe​


### Padriseup — strona 2

4.​ uzupełnić zaległości, brakującą wiedzę​

5.​ zapisać tematy zagadnienia niezrozumiałe i zapytać o nie na najbliższych zajęciach
na chacie głównym.​

Powyższe pomogą Państwu w sprawnym zdobywaniu wiedzy i kompetencji które są
wymagane w cyber.
W razie pytań etc, jesteśmy dla Państwa z pomocą 😉
Logistyka:
1.​ Używaj na Zoomie imienia i nazwiska (niezbędne do obecności).​

2.​ Spóźnienia zgłaszaj do TA (na priv)​

3.​ Wszelkie kwestie po zajęciach zgłaszaj na adres supportu:
supportblueteam@uj.edu.pl​

4.​ W książce logistycznej w Hackcampusie jest opisana cała logistyka kursu (Blue
Team Course book for [ID grupy]) - egzaminy, Final Projecty, Cywar itp.​

Bardzo dziękujemy za trzymanie się zasad :-)
Przerwy:
10:30 - 10:45
12:00 - 12:45
15:00 - 15:15
kontakt do prowadzącego: jacek.w@hackeru.com
kontakt do supportu: supportblueteam@uj.edu.pl
Opiekun grupy: Nikola Milczanowska email: nikola.m@hackeru.com, kom. 723 300 569

06.08.2023
Ch1 & Ch2 - Network Introduction & Fundamentals
ARPANET https://pl.wikipedia.org/wiki/ARPANET
#Warto wspomnieć o modelu ISO/OSI i porównać z modelem TCP/IP.
https://pl.wikipedia.org/wiki/Model_OSI


### Padriseup — strona 3

https://pl.wikipedia.org/wiki/Model_TCP/IP
typy skrętek:
https://www.dipol.com.pl/skretkakomputerowa-_oznaczenia_standardy_pomiary_bib526.htm
#Wstęp do sieci komputerowych
​
Sieć - grupa komputerów lub innych urządzeń, które są w stanie komunikować się ze
sobą. Sieć może być tworzona z pomocą fizycznych kabli (skrętka ethernet, światłowód,
kabel koncentrytczny etc.) lub za pomocą technologii bezprzewodowych. Sieci komputerowe
mogą różnić się rozmiarami (np. LAN, WAN) lub dostarczać określonych usług (np. centra
danych, serwerownie) oraz łączyć ze sobą komputery z różnych zakątków świata.
​
NIC - Network Interface Controller - komponent sprzętowy, który zezwala na
połączenie się komputera do fizycznej sieci komputerowej. Każdy NIC posiada adres MAC
(unikalny identyfikator urządzenia).
Przykładowy adres MAC: 91-8D-89-2D-D5-A6 lub 00:0d:83:b1:c0:8e
gdzie pierwsze trzy segmenty identyfikują producenta
natomiast trzy ostatnie segmenty są numerem identyfikującym urządzenia
#Podziały sieci:
​ - LAN (Local Area Network) - sieć niezbyt rozległa, zazwyczaj obejmuje biuro lub
dom a w jej skład wchodzi niedużo urządzeń, zarządzana z punktu jednego centralnego
​ - WAN (Wide Area Network) - rozległa na kilka niegraniczonych geograficznie
obszarów, łączy kilka sieci LAN. Sieci te zazwyczaj są zarządzane przez dostawców, którzy
się tym zajmują
​ - MAN (Metropolitan Area Network) - pomiędzy LAN i WAN, zazwyczaj obejmuje sieć
o rozmiarze miasta
​ - SAN (Storage Area Network) - dedykowana dla optymalizacji przesyłu danych
#Architektura sieci
​
- Client-server - serwer udostępnia jedną lub więcej usług lub zasobów, do jednego
lub wielu klientów. Przykładowe usługi: SMTP, FTP, WWW, Samba itd. Klient zawsze
rozpoczyna komunikację i wysyła żądania (request) o dostęp do zasobów. Serwer
odpowiada na żądanie udostępniająć żądany zasób.
#Podstawowe składniki sieci
​
- węzły - wszystko co jest podłączone do sieci np. komputer, telewizor, urządzenia
IoT


### Padriseup — strona 4

​
- medium transmisyjne - uczestniczy w przekazywaniu informacji np. skrętka lub sieć
bezprzewodowa
#Urządzenia sieciowe
​
- urządzenia końcowe - np. smartfony, PC, IoT
​
- media sieciowe - kable, fale radiowe, światłowody
​
- urządzenia pośrednie (switch, router, hub)
​
- switch - służy do przekierowywania pakietów, aby nim zarządzać trzeba
wykorzystać zdalny terminal, typy switchy:
​ * HUB - rozsyła dane wejsciowe z któregoś z portu na pozostałe,
​ * switch warstwy drugiej - używa adres MAC do przekierowania danych na
odpowiedni port, do którego urządzenie docelowe jest podpięte
​ * switch warstwy trzeciej - potrafi funkcjnować jako router, jest w stanie odczytać
docelowy adres IP
​
- router - potrafią wymieniać pakiety danych pomiędzy różymi sieciami (np. sieć
domowa i sieć globalna internet)
​
- Acess Point (AP) - łączy sieć bezprzewodową z siecią LAN
#Kabel ethernet == skrętka ethernet
​
- różne kategorie o różnych prędkościach
​ * CAT-5 - do 100Mb/s, do 100m
​ * CAT-5e - do 1Gb/s, do 100m
​ * CAT-6 - do 1Gb/s, do 100m lub 10Gb/s do 55m
​ * CAT-6a - do 10Gb/s do 100m
​ * CAT-7 - do 10Gb/s do 100m lub 100Gb/s do 50m
​
- kable:
​ * nieekranowany (UTP) - najczęściej stosowany typ kabla, 4 pary skręconych
przewodów zabieg ten niweluje zakłócenia
​ * ekranowany (STP) - kabel z ekranem wokół przewodów, eliminuje zewnętrzne
zakłócenia elektro-magnetyczne
#Mapa kabli podwodnych:


### Padriseup — strona 5

https://www.submarinecablemap.com
#Kable ethernet:
https://blog.programster.org/ethernet-cheatsheet
https://www.electronics-notes.com/articles/connectivity/ethernet-ieee-802-3/cables-types-pin
out-cat-5-5e-6.php
https://www.boston.co.uk/blog/2019/05/01/network-cables-reference-guide.aspx
#Informacja na temat budowy kabli sieciowych:
https://www.universalnetworks.co.uk/faq/what-does-utp-s-utp-ftp-stp-and-sftp-mean/
ciekawostka nt satellite tracking https://www.n2yo.com/
#IPv4 vs IPv6
https://www.netia.pl/pl/blog/ipv4-vs-ipv6-%E2%80%93-co-to-za-protokoly-i-jakie-sa-miedz
http://kti.eti.pg.gda.pl/ktilab/ipv6-adr/ipv6-adresy.pdf
https://www.soisk-me.pl/klasa-iv-sieci/klasy-adresow-ip
https://i.ytimg.com/vi/D1avGPpSJHs/maxresdefault.jpg
#Klasy adresów IP:
http://www.lomilowka.pl/upload/file/PiMLSK/klasyadres%C3%B3wIP.pdf
https://www.itbridge.pl/baza-wiedzy/adresacja-ip-publiczne-i-prywatne-adresy-ipv4
Wielkość strefy zależy od odległości między antenami i częstotliwości:
https://pl.wikipedia.org/wiki/Strefa_Fresnela
Kalkulator:
https://www.bestpartner.pl/index.php?d=kfresnel
I ciekawostka - chyba nic nie tłumi lepiej sygnału elektromagnetycznego niż drzewo liściaste
:)
Ping - używa protokołu ICMP - Internet Control Message Protocol, dosł. internetowy protokół
komunikatów kontrolnych - warstwy 3 (sieciowej).
https://pl.wikipedia.org/wiki/Internet_Control_Message_Protocol
ipconfig - komenda wyświetlająca informacje o konfiguracji interfejsów sieciowych w
windowsie. W linuxie jest ifconfig (interface config)


### Padriseup — strona 6

Nslookup - odpytuje serwer DNS (zawsze) o rekord. Dlatego Nslookup nie pokaże nam
rekordów lokalnych ustawionych w pliku hosts.
nslookup może odpytać o konkretny rodzaj rekordu, np:
nslookup -q=TXT hackampus.com
Tracert - działa podobnie jak ping z użyciem ICMP. Wysyła natomiast pakiety z TTL
zwiększanym o 1, tak by kolejne routery odpowiadały z informacją o wygaśnięciu pakietu.
Jeśli router jest ustawiony tak by nie zmniejszać TTL - nie pojawi się na liście tracerta.
Netsh - Netshell - narzędzie tekstowe do konfiguracji sieci w Windowsie.
#Porty:
https://en.wikipedia.org/wiki/List_of_TCP_and_UDP_port_numbers
#Wybrane protokoły sieciowe
​
- IP - Internet Protocol - protokół stanowiący podstawę do wymiany danych wewnątrz
sieci
​
- DNS - Domain Name System - rozwiązywanie adresów http na adres fizyczne IP
​
- DHCP - Dynamic Host Configuration Protocol - automatyczna konfiguracja nowych
hostów w sieci
​
- HTTP - Hypertext Transfer Protocol - wykorzystywany do transferu danych
tekstowych, obrazów i innych danych które mozna umieścić na stronie internetowej
​
- HTTPS - secure implementation of HTTP - tak jak HTTP ale zapewnia szyfrowanie
danych wymiany danych pomiędzy klientem a hostem
​
- ARP - Address Resolution Protocol - protokół sieciowy umożliwiający mapowanie
logicznych adresów warstwy sieciowej (warstwa 3) na fizyczne adresy warstwy łącza danych
(2).
#Sieci bezprzewodowe
Oparte o technologie bezprzewodowe (fale radiowe). Ich rozpowrzechnienie wprowadziło
nowe zagrożenia, z powodu braku fizycznego nośnika danych (skrętka ethernetowa).
Podstawowym zabezpieczeniem było filtrowanie urządzeń na podstawie adresów MAC
(przyłączyć do sieci mogło się urządzenie z listy dozwolonych urządzeń) jednak ten sposób
zabezpieczenia jest łatwy do obejścia. Aktualnie, w dużej części, problemy z
bezpieczeństwem sieci WiFi spowodowane są poprzez błędną konfigurację.
#Typy sieci bezprzewodowych
​
- WiFi (wireless fidelity) - bazuje na standardach IEEE 802.11, używane do tworzenia
sieci LAN


### Padriseup — strona 7

​
- Wi-MAX - implementacja WiFi, aby wspierać duże obszary
​
- BLuetooth - implementacja WPAN (Wireless Personal Area Network) -
wykorzystana do parowania i komunikacji urządzeń na odległości do 100m.
#Standardy sieci WiFi
https://snipboard.io/rvm902.jpg
#Model warstwowy TCP/IP
-Warstwa aplikacji (HTTP, FTP, DNS, RDP)
-Warstwa transportowa (TCP, UDP)
-Warstwa internetu (IP)
-Warstwa dostępu do sieci (MAC)
warstwa aplikacji -> warstwa dostępu do sieci -enkapsulacja
warstwa dostępu do sieci-> warstwa aplikacji - dekapsulacja
EBCDIC
https://pl.wikipedia.org/wiki/EBCDIC
Frame Relay
https://pl.wikipedia.org/wiki/Frame_Relay
Address Types
https://www.guru99.com/types-of-ip-addresses.html
https://pmr.ii.pw.edu.pl/~pmr/ws/
Wireshark
https://www.wireshark.org/
edit>>preferences>>packet diagram
#3-way handshake
SYN -> SYN/ACK -> ACK
FIN -> FIN/ACK -> ACK
Połączenie to nosi nazwę uzgadniania trój-etapowego (ang. three-way handshake). Host
źródłowy, czyli np. klient, wysyła segment zawierający flagę SYN (SYN to flaga
synchronizacji numerów sekwencyjnych) W segmencie też zawarty jest losowy numer


### Padriseup — strona 8

sekwencyjny klienta (zwany także numerem ISN, SEQ=100) służący do późniejszego
scalania fragmentów danych.
Odbierając ten segment host docelowy, czyli np. serwer jest informowany, że klient chce
nawiązać z nim połączenie. Serwer w odpowiedzi wysyła segment z ustawioną flagą SYN i
ACK (flaga ACK informuje klienta o tym, ze serwer odebrał poprzedni segment), numerem
sekwencyjnym odebranym od klienta zwiększonym o 1 (ACK=101) oraz swoim – losowym
numerem sekwencyjnym (SEQ=300).
Na koniec klient odsyła do serwera segment z ustawioną flagą ACK potwierdzającą odbiór
poprzedniego komunikatu z numerem sekwencyjnym serwera zwiększonym o 1 (SEQ=101,
ACK=301).
●​ SYN – klient nawiązuje połączenie z segmentem, numer sekwencyjny segmenty
(segment sequence number) = n
​
* SYN-ACK – serwer odpowiada z numerem potwierdzenia (acknowledgement
number) n + 1 i numerem sekwencji m
​
* ACK – klient odpowiada z numerem sekwencji równym m + 1
SYN (synchronize)
SYN-ACK (synchronize-acknowledge)
ACK (acknowledge)
​
* FIN – jedna ze stron wysyła komunikat zakończenia
​
* ACK – druga strona potwierdza zakończenie
​
* FIN – druga strona wysyła także komunikat o zakończeniu (można
​
* połączyć z ACK)
​
* ACK – pierwsza strona potwierdza zakończenie
https://www.adminsub.net/mac-address-finder/eui
https://access.redhat.com/sites/default/files/attachments/rh_ip_command_cheatsheet_1214_
jcs_print.pdf
https://www.asus.com/pl/networking-iot-servers/whole-home-mesh-wifi-system/zenwifi-wifi-s
ystems/asus-zenwifi-ax-hybrid-xp4/

19.08.2023
Ch3 & Ch4 - Switches Fundamentals & Security


### Padriseup — strona 9

#Kompendium wiedzy na temat sieci komputerowych - dobre do uzupełnienia braków
wiedzy w danych zagadnieniach
https://sieci.infopl.info/
#Jak skutecznie uczyć się złożonych zagadnień?
https://miroslawzelent.pl/nauka/the-slight-edge-jeff-olson/
#Czym przełącznik sieciowy różni się od routera?
https://www.komputronik.pl/informacje/co-to-jest-switch-czym-przelacznik-sieciowy-rozni-sie-
od-routera/
#Typy routerów
https://community.fs.com/blog/different-types-of-routers-in-networking.html
#Typy przełączników
https://www.spiceworks.com/tech/networking/articles/what-is-network-switch/
#Most i przełącznik
https://sieci.infopl.info/index.php/urzadzenia/switch
#Typy transmisji danych
https://soisk.info/index.php/Typy_transmisji_danych:_unicast,_multicast,_broadcast
#Collision Domain
https://www.guru99.com/collision-broadcast-domain.html
#Typy kabli ethernetowych
https://www.electronics-notes.com/articles/connectivity/ethernet-ieee-802-3/cables-types-pin
out-cat-5-5e-6.php
https://www.vssmonitoring.com/types-of-ethernet-cables/
https://www.unitek-products.com/blogs/products
https://www.komputronik.pl/informacje/jaki-kabel-sieciowy-kabel-do-internetu/
#RJ45 typy T568A oraz T568B
https://cablesupply.com/rj45-ethernet-wiring-color-guides/
#Kategorie kabli sieciowych
https://blog.laptopcontrol.pl/informatyka/kategorie-kabel-sieciowy-lan-skretka/


### Padriseup — strona 10

#Topologie sieci
https://pasja-informatyki.pl/sieci-komputerowe/topologie-sieci/
#RIR
https://pl.wikipedia.org/wiki/Regional_Internet_Registry
#IPV4 vs IPV6
https://www.netia.pl/pl/blog/ipv4-vs-ipv6-%E2%80%93-co-to-za-protokoly-i-jakie-sa-miedz
#Klasy adresów IP
https://www.soisk-me.pl/klasa-iv-sieci/klasy-adresow-ip
http://www.lomilowka.pl/upload/file/PiMLSK/klasyadres%C3%B3wIP.pdf
#Maska podsieci
https://pl.wikipedia.org/wiki/Maska_podsieci
Standardy sieci WiFi
https://snipboard.io/rvm902.jpg
#Model ISO OSI
https://pasja-informatyki.pl/sieci-komputerowe/model-tcp-ip-iso-osi/
https://www.soisk-me.pl/klasa-iv-sieci/model-iso-osi-i-tcp-ip
#enkapsulacja
http://oprogramowaniu.pl/czym-jest-enkapsulacja/
warstwa aplikacji -> warstwa dostępu do sieci -enkapsulacja
warstwa dostępu do sieci-> warstwa aplikacji - dekapsulacja
https://pmr.ii.pw.edu.pl/~pmr/ws/
[Windows]
arp -a - wyświetlenie tablicy ARP
arp -d - usuwanie tablicy ARP [jako Administrator]
#Wireshark - przykładowe filtry


### Padriseup — strona 11

https://wiki.wireshark.org/CaptureFilters
https://www.wireshark.org/docs/wsug_html_chunked/
https://bugs.wireshark.org/bugzilla/attachment.cgi?id=11612
https://wiki.wireshark.org/SampleCaptures
https://wiki.wireshark.org/uploads/moin_import/attachments/SampleCaptures/dhcp.pcap
#Podstawowe komendy CISCO (IOS)
https://rioco.pl/komendy/komendy-ciscoios/
odświeżenie interfejsu
Ctrl-R - refresh
automatyczne odświeżanie interfejsu
logging synchronous
https://wiki.wireshark.org/uploads/moin_import/attachments/SampleCaptures/dns-icmp.pca
png.gz
https://ia601604.us.archive.org/20/items/cisco-packet-tracer-821-ubuntu-64bit/CiscoPacketT
racer_821_Windows_64bit.exe
configure terminal
hostname S1-Floor1
username Admin password p@nd@
show running-config
conf t
service password-encryption
exit
show running-config
copy running-config startup-config
show interfaces FastEthernet 0/1
show mac-address-table
zadanie domowe:


### Padriseup — strona 12

https://www.hackampus.com/practices/book/480/chapter/2945
chapter 3 task 3 - sprobowac w domu przerobic, jeżeli będą problemmy, zapisać pytania i
screeny na nastepne zajecia.

20.08.2023
LAB NET03-L3
Instruckja całego rozwiązania jest na HackCampus w Chapter 3->Practice tasks->Task 3
Remote Access

Telnet-TCP/23
SSH-TCP/22
Przechwycenie protokołu SSH
https://www.cloudshark.org/captures/849d3c7f09d3
LAB SSH1
hostname S1
username Admin password p@nd@
enable password c!sc0
service password-encryption
banner motd #Authorized Access only. Hacking is illegal, log out#
ip domain-name CyberPro.com
exit
wr
line vty 0 15
login local
transport input ssh
exit
interface vlan 1


### Padriseup — strona 13

ip add
ip address 10.0.0.150 255.255.255.0
no shutdown
exit
Generowanie klucza:
crypto key generate rsa
1024
S1#show ip ssh - pokaże, że ssh uruchomiono
https://beyond.hackampus.com/canvas/general/general-LLcAf-2021.12.12.10.09.23-Extra%2
0Files.rar
conf t
interface range fastEthernet 0/1-4
switchport mode access
switchport port-security
exit
S1(config)#interface fastEthernet 0/1
S1(config-if)#switchport port-security mac-address 00D0.9793.87C4
S1(config-if)#exit
S1(config)#interface fastEthernet 0/2
S1(config-if)#switchport port-security mac-address 0009.7C96.0271
S1(config-if)#exit
S1(config)#interface fastEthernet 0/3
S1(config-if)#switchport port-security mac-address sticky
S1(config-if)#exit
S1(config)#interface fastEthernet 0/4
S1(config-if)#switchport port-security mac-address sticky
S1(config-if)#exit


### Padriseup — strona 14

S1(config)#interface fastEthernet 0/1
S1(config-if)#switchport port-security violation shutdown
S1(config-if)#exit
S1(config)#interface range fastEthernet 0/2-3
S1(config-if-range)#switchport port-security violation restrict
S1(config-if-range)#exit
S1(config)#interface range fastEthernet 0/4
S1(config-if-range)#switchport port-security violation protect
S1(config-if-range)#exit
S1(config)#interface range fastEthernet 0/5-24, gigabitEthernet 0/1-2
S1(config-if-range)#shutdown
S1(config-if-range)#exit
S1>enable
S1#show port-security
S1#show port-security address
S1#show port-security interface fastEthernet 0/4
S1#show running-config
interface FastEthernet0/3
switchport mode access
switchport port-security
switchport port-security maximum 2
switchport port-security mac-address sticky
switchport port-security violation restrict
switchport port-security mac-address sticky 0004.9A8B.2832
switchport port-security mac-address sticky 0090.0C26.3CEE
S1#show port-security interface fastEthernet 0/4


### Padriseup — strona 15

Switch>enable
Switch#conf t
Switch(config)#hostname S1
S1(config)#username Admin password p@nd@
S1(config)#enable password c!sc0
S1(config)#ip ssh version 2
S1(config)#do show ip ssh

02.09.2023
https://www.cisco.com/c/en/us/support/docs/routers/7200-series-routers/12219-17.html
pliki do net-05-l2
https://beyond.hackampus.com/canvas/general/general-qji5R-2021.12.12.10.18.12-Extra%2
0FIles.rar
enable
conf t - przechodzimy w tryb konfiguracji
Router>enable
Router#conf t
Router(config)#hostname R1
R1(config)#username Admin password p@nd@
R1(config)#enable password c!sc0
R1(config)#service password-encryption
R1(config)#banner motd #Access to this device is for authorized personnel only!#
R1(config)#line console 0
R1(config-line)#login local
R1(config-line)#exit
R1(config)#exit
R1#show running-config


### Padriseup — strona 16

R1#copy running-config startup-config
Destination filename [startup-config]? --> [ENTER klawisz]
R1#conf t
R1(config)#interface gigabitEthernet 0/0
R1(config-if)#ip address 192.168.0.1 255.255.255.0
R1(config-if)#no shutdown
R1(config-if)#exit
R1(config)#interface gigabitEthernet 0/1
R1(config-if)#ip address 10.0.0.1 255.255.255.0
R1(config-if)#no shutdown
R1(config-if)#exit
R1(config)#do show ip interface brief
R1(config)#do show ip route
banner motd # Access to this device is for authorized personnel only!#
// troubleshooting nie pingujących routerów ,sprawdzamy:
R1(config)#do show ip interface brief
Interface ​
IP-Address ​ OK? Method Status ​ Protocol
GigabitEthernet0/0 ​
192.168.0.1 ​ YES manual up ​
up
GigabitEthernet0/1 ​
10.0.0.1 ​
YES manual up ​
up
GigabitEthernet0/0/0 7.7.7.1 ​
YES manual up
// troubleshooting jeżeli usunięto połączenie z routerem:
R1# show ip interface brief
Interface ​
IP-Address ​ OK? Method Status ​ Protocol
GigabitEthernet0/0 ​
192.168.0.1 ​ YES manual up ​
up
GigabitEthernet0/1 ​
10.0.0.1 ​
YES manual up ​
up
GigabitEthernet0/0/0 7.7.7.1 ​
YES manual up ​
up


### Padriseup — strona 17

Vlan1 ​unassigned ​ YES unset administratively down down
jeżeli nie ma konfiguracji/została usunięta, to tworzymy ją na nowo.
S1>enable
S1#conf t
S1(config)#interface vlan 1
S1(config-if)#ip address 192.168.0.4 255.255.255.0
S1(config-if)#no shutdown
S1(config-if)#exit
S1(config)#
S2>enable
S2#conf t
S2(config)#interface vlan 1
S2(config-if)#ip address 10.0.0.4 255.255.255.0
S2(config-if)#no shutdown
S2(config-if)#exit
S2(config)#
S2(config)#ip default-gateway 10.0.0.1
R1>enable
R1#conf t
R1(config)#ipv6 unicast-routing
R1(config)#interface gigabitEthernet 0/0
R1(config-if)#ipv6 address 2001:cafe:abcd:1::/64
R1(config-if)#exit
R1(config)#
https://www.browserling.com/tools/ip-to-bin
https://www.browserling.com/tools/bin-to-ip


### Padriseup — strona 18

https://42.pl/ipcalc/
do pobrania na następne zajęcia:
https://beyond.hackampus.com/canvas/general/general-YbaTH-2021.12.12.10.36.21-NET-0
7-L1.rar

03.09.2023
w cmd win:
route print
route add 0.0.0.0 mask 0.0.0.0 192.168.100.1 metric 1
route delete 0.0.0.0
https://beyond.hackampus.com/canvas/general/general-YbaTH-2021.12.12.10.36.21-NET-0
7-L1.rar
R1>enable
R1#show ip route
R1(config)#ip route 192.168.0.64 255.255.255.192 serial 0/0/0
R1(config)#ip route 192.168.0.128 255.255.255.192 serial 0/0/0
R1(config)#ip route 192.168.0.196 255.255.255.252 serial 0/0/0
R1(config)#do show ip route
R2(config)#ip route 192.168.0.0 255.255.255.192 192.168.0.193
R2(config)#ip route 192.168.0.128 255.255.255.192 192.168.0.198
R2(config)#exit
no ip route 192.168.0.0 255.255.255.192 192.168.0.193
no ip route 192.168.0.128 255.255.255.192 192.168.0.198
R3#conf terminal
R3(config)#ip route 192.168.0.0 255.255.255.192 ser
R3(config)#ip route 192.168.0.0 255.255.255.192 serial 0/0/1
R3(config)#ip route 192.168.0.64 255.255.255.192 serial 0/0/1


### Padriseup — strona 19

R3(config)#ip route 192.168.0.192 255.255.255.252 serial 0/0/1
R3(config)#exit
R3#show ip route
PC2=192.168.0.66
PC3=192.168.0.130
ping 192.168.0.194
sprawdzić czy widzi router
R1(config)#ip route 192.168.0.64 255.255.255.192 serial 0/0/0
R1(config)#ip route 192.168.0.128 255.255.255.192 serial 0/0/0
R1(config)#ip route 192.168.0.196 255.255.255.252 serial 0/0/0
R1(config)#do show ip route
R1>enable
R1#conf t
R1(config)#ip route 0.0.0.0 0.0.0.0 serial 0/0/0
R2#conf t
R2(config)#ip route 0.0.0.0 0.0.0.0 serial 0/1/0
R2(config)#do show ip route static
R3>enable
R3#conf t
Enter configuration commands, one per line. End with CNTL/Z.
R3(config)#ip route 0.0.0.0 0.0.0.0 serial 0/0/1
R3(config)#do show ip route static
https://beyond.hackampus.com/canvas/general/general-LJUoB-2021.12.12.10.39.31-Extra%
20Files.rar
https://ipwithease.com/ospf-timers/
R1#enable
R1#conf t


### Padriseup — strona 20

Enter configuration commands, one per line. End with CNTL/Z.
R1(config)#router rip
R1(config-router)#version 2
R1(config-router)#no auto-summary
R1(config-router)#network 172.16.0.0
R1(config-router)#network 172.16.0.8
R1(config-router)#network 192.168.10.0
R1(config-router)#passive-interface gigabitEthernet 0/0
R1(config-router)#exit
R1(config)#
R1>en
R1#conf t
R1(config)#router rip
R1(config-router)#version 2
R1(config-router)#no auto-summary
R1(config-router)#network 172.16.0.0
R1(config-router)#network 172.16.0.8
R1(config-router)#network 192.168.10.0
R1(config-router)#passive-interface gigabitEthernet 0/0
R1(config-router)#exit
R1(config)#exit
R1#copy running-config startup-config
Destination filename [startup-config]? ​
<KLAWISZ ENTER
Building configuration...
[OK]
R1#


### Padriseup — strona 21

R2>en
R2#show ip route connected
C 172.16.0.0/30 is directly connected, Serial0/3/0
C 172.16.0.4/30 is directly connected, Serial0/3/1
C 192.168.20.0/24 is directly connected, GigabitEthernet0/0
R2#conf t
R2(config)#router rip
R2(config-router)#version 2
R2(config-router)#no auto-summary
R2(config-router)#network 172.16.0.0
R2(config-router)#network 172.16.0.4
R2(config-router)#network 192.168.20.0
R2(config-router)#passive-interface gigabitEthernet 0/0
R2(config-router)#exit
R2(config)#exit
R2#copy running-config startup-config
Destination filename [startup-config]? ​
<KLAWISZ ENTER
Building configuration...
[OK]
R2#
R3>en
R3#show ip route connected
C 172.16.0.4/30 is directly connected, Serial0/3/1
C 172.16.0.8/30 is directly connected, Serial0/3/0
C 192.168.30.0/24 is directly connected, GigabitEthernet0/0
C 210.10.10.0/30 is directly connected, Serial0/2/0


### Padriseup — strona 22

R3#conf t
Enter configuration commands, one per line. End with CNTL/Z.
R3(config)#router rip
R3(config-router)#version 2
R3(config-router)#no auto-summary
R3(config-router)#network 172.16.0.4
R3(config-router)#network 172.16.0.8
R3(config-router)#network 192.168.30.0
R3(config-router)#network 210.10.10.0
R3(config-router)#no auto-summary
R3(config-router)#passive-interface gigabitEthernet 0/0
R3(config-router)#exit
R3(config)#exit
R3#copy running-config startup-config
Destination filename [startup-config]? ​
<KLAWISZ ENTER
Building configuration...
[OK]
R3#show ip route rip
R3>enable
R3#conf t
R3(config)#ip route 0.0.0.0 0.0.0.0 serial 0/2/0
R3(config)#exit
R3#show ip route
Codes: L - local, C - connected, S - static, R - RIP, M - mobile, B - BGP
​
D - EIGRP, EX - EIGRP external, O - OSPF, IA - OSPF inter area
​
N1 - OSPF NSSA external type 1, N2 - OSPF NSSA external type 2


### Padriseup — strona 23

​
E1 - OSPF external type 1, E2 - OSPF external type 2, E - EGP
​
i - IS-IS, L1 - IS-IS level-1, L2 - IS-IS level-2, ia - IS-IS inter area
​
* - candidate default, U - per-user static route, o - ODR
​
P - periodic downloaded static route
Gateway of last resort is 0.0.0.0 to network 0.0.0.0 ​ << SPRAWDZIC
R3>enable
R3#conf t
R3(config)#ip route 0.0.0.0 0.0.0.0 serial 0/2/0
R3(config)#exit
R3#show ip route
Codes: L - local, C - connected, S - static, R - RIP, M - mobile, B - BGP
​
D - EIGRP, EX - EIGRP external, O - OSPF, IA - OSPF inter area
​
N1 - OSPF NSSA external type 1, N2 - OSPF NSSA external type 2
​
E1 - OSPF external type 1, E2 - OSPF external type 2, E - EGP
​
i - IS-IS, L1 - IS-IS level-1, L2 - IS-IS level-2, ia - IS-IS inter area
​
* - candidate default, U - per-user static route, o - ODR
​
P - periodic downloaded static route
Gateway of last resort is 0.0.0.0 to network 0.0.0.0 ​ << SPRAWDZIC
R3#
R3#conf t
R3(config)#router rip
R3(config-router)#default-information originate
R3(config-router)#exit
R3(config)#
https://www.ciscopress.com/articles/article.asp?p=2294214&seqNum=2
R0#conf t


### Padriseup — strona 24

R0(config)#router ospf 1
R0(config-router)#router-id 1.1.1.0
R0(config-router)#network 192.168.0.0 0.0.0.255 area 0
R0(config-router)#network 172.16.0.0 0.0.0.3 area 0
R0(config-router)#network 172.16.0.8 0.0.0.3 area 0
R0(config-router)#auto-cost reference-bandwidth 1000
R0(config-router)#passive-interface gigabitEthernet 0/1
R0(config-router)#exit
R0(config)#exit
R0#
R1>en
R1#conf t
R1(config)#router ospf 1
R1(config-router)#router-id 1.1.1.1
R1(config-router)#network 192.168.1.0 0.0.0.255 area 0
R1(config-router)#network 172.16.0.4 0.0.0.3 area 0
R1(config-router)#network 172.16.0.8 0.0.0.3 area 0
R1(config-router)#auto-cost reference-bandwidth 1000
R1(config-router)#passive-interface gigabitEthernet 0/1
R1(config-router)#exit
R1(config)#exit
R1#
R2>en
R2#conf t
R2(config)#router ospf 1
R2(config-router)#router-id 1.1.1.2


### Padriseup — strona 25

R2(config-router)#network 192.168.2.0 0.0.0.255 area 0
R2(config-router)#network 172.16.0.4 0.0.0.3 area 0
R2(config-router)#network 172.16.0.0 0.0.0.3 area 0
R2(config-router)#auto-cost reference-bandwidth 1000
R2(config-router)#passive-interface gigabitEthernet 0/1
R2(config-router)#exit
R2(config)#
R2(config)#exit
R2#show ip route ospf
​
172.16.0.0/16 is variably subnetted, 5 subnets, 2 masks
O ​
172.16.0.8 [110/2] via 172.16.0.6, 00:02:08, GigabitEthernet0/1/0
​
[110/2] via 172.16.0.1, 00:02:08, GigabitEthernet0/0/0
O​
192.168.0.0 [110/2] via 172.16.0.1, 00:02:08, GigabitEthernet0/0/0
O​
192.168.1.0 [110/2] via 172.16.0.6, 00:02:08, GigabitEthernet0/1/0

https://pasja-informatyki.pl/sieci-komputerowe/
https://42.pl/ipcalc/
https://beyond.hackampus.com/canvas/general/general-1izuf-2021.12.12.10.42.45-NET-09-
L1.rar
S2#conf t
S2(config)#vlan 10
S2(config-vlan)#name Workstation
S2(config-vlan)#exit
S2(config)#vlan 20
S2(config-vlan)#name Servers
S2(config-vlan)#exit
S2(config)#do show vlan brief


### Padriseup — strona 26

F0/1-4 VLAN10
F0/5-6 VLAN20
S2(config)#interface range fastEthernet 0/1-4
S2(config-if-range)#switchport mode access
S2(config-if-range)#switchport access vlan 10
S2(config-if-range)#exit
S2(config)#interface range fastEthernet 0/5-6
S2(config-if-range)#switchport mode access
S2(config-if-range)#switchport access vlan 20
S2(config-if-range)#exit
S2(config)#do show vlan brief
Polaczenia fizyczne dla switcha S1
F0/1-2 VLAN10 (stacje robocze)
F0/3 VLAN20 (serwer)
S1>enable
S1#conf t
S1(config)#vlan 10
S1(config-vlan)#name Workstation
S1(config-vlan)#exit
S1(config)#vlan 20
S1(config-vlan)#name Servers
S1(config-vlan)#exit
S1(config)#interface range fastEthernet 0/1-2
S1(config-if-range)#switchport mode access
S1(config-if-range)#switchport access vlan 10
S1(config-if-range)#exit


### Padriseup — strona 27

S1(config)#interface fastEthernet 0/3
S1(config-if)#switchport mode access
S1(config-if)#switchport access vlan 20
S1(config-if)#exit
S1(config)#do show vlan brief
10.0.0.0 255.255.255.0
10.0.0.254
192.168.0.0 255.255.255.0 - Serwery
10.0.0.0 255.255.255.0 ​
- Komputery
ostatni adres w sieci to brama domyslna
10.0.0.1
255.255.255.0
10.0.0.254
192.168.0.1
255.255.255.0
192.168.0.254
192.168.0.0 255.255.255.0 zakres sieci i ostatni adres to brama
S1>enable
S1#conf t
S1(config)#interface range gigabitEthernet 0/1-2
S1(config-if-range)#switchport mode trunk
S1(config-if-range)#
%LINEPROTO-5-UPDOWN: Line protocol on Interface GigabitEthernet0/1, changed state to
down
%LINEPROTO-5-UPDOWN: Line protocol on Interface GigabitEthernet0/1, changed state to
up
S1(config-if-range)#exit


### Padriseup — strona 28

do show interfaces switchport
S2>en
S2#conf t
S2(config)#interface gigabitEthernet 0/1
S2(config-if)#switchport mode trunk
S2(config-if)#exit
S2(config)#vlan 30
S2(config-vlan)#name Native
S2(config-vlan)#exit
S2(config)#interface gigabitEthernet 0/1
S2(config-if)#switchport trunk native vlan 30
S2(config-if)#exit
S1#copy running-config startup-config
S2#copy running-config startup-config
do copy running-config startup-config
R1>enable
R1#conf t
R1(config)#interface gigabitEthernet 0/0
R1(config-if)#no shutdown
R1(config-if)#exit
https://beyond.hackampus.com/canvas/general/general-NVfKC-2021.12.12.11.25.45-NET-11
-L1.rar
R2>enable
R2#conf terminal
R2(config)#ip access-list standard 1
R2(config-std-nacl)#exit
R2(config)#access-list 1 deny 172.16.2.0 0.0.0.255


### Padriseup — strona 29

R2(config)#access-list 1 permit any
R2(config)#interface gigabitEthernet 0/0
R2(config-if)#ip access-group 1 out
R2(config-if)#exit
R1>enable
R1#configure terminal
R1(config)#ip access-list standard BLOCK_HOST
R1(config-std-nacl)#deny host 192.168.2.1
R1(config-std-nacl)#permit any
R1(config-std-nacl)#exit
R1(config)#interface gigabitEthernet 0/0
R1(config-if)#ip access-group BLOCK_HOST out
R1(config-if)#exit
R1(config)#do show access-list
R2>enable
R2#conf t
R2(config)#ip access-list extended 100
R2(config-ext-nacl)#exit
R2(config)#access-list 100 deny ip host 172.16.2.1 host 192.168.1.2
R2(config)#access-list 100 permit ip any any
R2(config)#interface gigabitEthernet 0/1
R2(config-if)#ip access-group 100 in
R2(config-if)#exit
R2(config)#do show access-list
R1(config)#ip access-list extended BLOCK_HTTP
R1(config-ext-nacl)#deny tcp host 192.168.1.2 host 172.16.1.2 eq 80


### Padriseup — strona 30

R1(config-ext-nacl)#permit ip any any
R1(config-ext-nacl)#exit
R1(config)#interface gigabitEthernet 0/0
R1(config-if)#ip access-group BLOCK_HTTP in
R1(config-if)#exit
R1(config)#do show access-list


---

# 05 — Cisco projekt — pełne notatki

Źródło: `Cisco projekt.pdf` (9 stron).

## Lab Task 1 — podział 172.16.10.0/24 na 8 podsieci

Maska: `/27` = `255.255.255.224`, rozmiar bloku 32 adresy.

| # | Network address | Usable hosts | Broadcast |
|---:|---|---|---|
| 1 | 172.16.10.0/27 | 172.16.10.1–172.16.10.30 | 172.16.10.31 |
| 2 | 172.16.10.32/27 | 172.16.10.33–172.16.10.62 | 172.16.10.63 |
| 3 | 172.16.10.64/27 | 172.16.10.65–172.16.10.94 | 172.16.10.95 |
| 4 | 172.16.10.96/27 | 172.16.10.97–172.16.10.126 | 172.16.10.127 |
| 5 | 172.16.10.128/27 | 172.16.10.129–172.16.10.158 | 172.16.10.159 |
| 6 | 172.16.10.160/27 | 172.16.10.161–172.16.10.190 | 172.16.10.191 |
| 7 | 172.16.10.192/27 | 172.16.10.193–172.16.10.222 | 172.16.10.223 |
| 8 | 172.16.10.224/27 | 172.16.10.225–172.16.10.254 | 172.16.10.255 |

## Lab Task 2 — VLAN, access ports, trunk i native VLAN

Tworzone VLAN-y:

```text
vlan 10
 name Management
vlan 20
 name Marketing
vlan 30
 name Accounting
vlan 100
 name Native
```

Przypisania access:

```text
interface range FastEthernet 0/1-10
 switchport mode access
 switchport access vlan 10
interface range FastEthernet 0/11-20
 switchport mode access
 switchport access vlan 20
interface range FastEthernet 0/21-24
 switchport mode access
 switchport access vlan 30
```

Trunki i native VLAN:

```text
interface range GigabitEthernet 0/1-2
 switchport mode trunk
 switchport trunk native vlan 100
```

Weryfikacja: `show interfaces switchport`, `show interfaces trunk`. Dla portów access użyto także `switchport nonegotiate`. Konfiguracja jest zapisywana przez `copy running-config startup-config`.

## Lab Task 3 — adresacja interfejsów i hostów

- R3 `GigabitEthernet0/0`: `172.16.10.1 255.255.255.224`, `no shutdown`.
- R3 `GigabitEthernet0/1`: `172.16.10.33 255.255.255.224`, `no shutdown`.
- Weryfikacja: `do show ip route`.
- Adresy wykorzystywane na łączach szeregowych w projekcie: `172.16.10.65`, `.66`, `.97`, `.98`, `.129`, `.130` z maską `/27`.
- Konfiguracja hostów w Packet Tracerze obejmuje m.in. CEO1 `.189`, CEO2 `.190`, Copyrighter1 `.221`, Copyrighter2 `.222`, Dialer1 `.253`, Dialer2 `.254`, a także hosty Office 2/Office 3, Guest, Admin, Syslog/NTP Server i E-mail Server. Pełne wartości ze screenshotów są zachowane niżej w transkrypcji stron 4–5.

## Lab Task 4 — Router-on-a-Stick

Fizyczny `GigabitEthernet0/0` jest uruchamiany `no shutdown`. Powstają subinterfejsy:

```text
interface GigabitEthernet 0/0.10
 encapsulation dot1Q 10
 ip address 172.16.10.161 255.255.255.224
interface GigabitEthernet 0/0.20
 encapsulation dot1Q 20
 ip address 172.16.10.193 255.255.255.224
interface GigabitEthernet 0/0.30
 encapsulation dot1Q 30
 ip address 172.16.10.225 255.255.255.224
```

Weryfikacja: `show ip interface brief`. Po stronie switcha porty GigabitEthernet są ustawiane jako trunk, a native VLAN to 100; używane jest `show interfaces trunk`.

## Task 5 — Port Security

```text
show port-security address
interface FastEthernet 0/2
 switchport mode access
 switchport port-security
 switchport port-security violation restrict
 switchport port-security mac-address sticky
show interfaces status
```

Konfiguracja jest powtarzana na S1 i S2 m.in. dla `Fa0/1`, `Fa0/11`, `Fa0/21`. Nieużywane zakresy portów są wyłączane przez `shutdown` (w materiale pokazano m.in. `interface range FastEthernet 0/12-20`). Na końcu `copy running-config startup-config`.

## Task 6 — OSPF

- `show ip route connected`;
- uruchomienie wymaganych interfejsów (`no shutdown`);
- `router ospf 1`;
- ustawienie `router-id`;
- polecenia `network ... wildcard ... area 0`;
- `passive-interface`;
- weryfikacja: `show ip protocols`, `show ip ospf interface`, `show ip ospf neighbor`;
- zapis konfiguracji.

## Task 7 — ACL

Materiał pokazuje rozszerzoną regułę blokującą komunikację pomiędzy konkretnymi hostami:

```text
access-list 137 deny ip host 172.16.10.60 host 172.16.10.29
show access-lists
```

## Task 8 — lokalne konto i zabezpieczenie konfiguracji

```text
username Admin password ACDC1973
enable password beatles1960
service password-encryption
banner motd #Only authorized personnel are allowed accessing this device#
wr
```

## Task 9 — SSH

```text
ip domain-name Cyber.local
hostname R1
crypto key generate rsa
# modulus: 1024
ip ssh version 2
line vty 0 4
 login local
 transport input ssh
show ip ssh
show ssh
```

W logu widoczny jest komunikat aktywacji SSH 1.99/2.0, timeout uwierzytelnienia 120 s, 3 próby oraz sesja z szyfrowaniem AES128-CBC i HMAC-SHA1.

# Transkrypcja źródła strona po stronie


### Cisco projekt — strona 1

Lab Task 1:
Divide 172.16.10.0/24 network into 8 subnets
Subnet number Network address Usable Host Broadcast Address
Address Range
1 172.16.10.0/27 172.16.10.1 to 172.16.10.31
172.16.10.30
2 172.16.10.32/27 172.16.10.33 to 172.16.10.63
172.16.10.62
3 172.16.10.64/27 172.16.10.65 to 172.16.10.95
172.16.10.94
4 172.16.10.96/27 172.16.10.97 to 172.16.10.127
172.16.10.126
5 172.16.10.128/27 172.16.10.129 to 172.16.10.159
172.16.10.158
6 172.16.10.160/27 172.16.10.161 to 172.16.10.191
172.16.10.190
7 172.16.10.192/27 172.16.10.193 to 172.16.10.223
172.16.10.222
8 172.16.10.224/27 172.16.10.225 to 172.16.10.255
172.16.10.254
255.255.255.224
Lab Task 2:
1.
Switch>
Switch>en
Switch#conf t
Enter configuration commands, one per line. End with CNTL/Z.
Switch (config) #vlan 10
Switch (config-vlan) #name Management
Switch (config-vlan) #exit
Switch (config) #vlan 20
Switch (config-vlan) #name Marketing
Switch (config-vlan) #exit
Switch(config)#vlan 30
Switch (config-vlan) #name Accounting
Switch (config-vlan) #exit
Switch(config)#vlan 100
Switch (config-vlan) fname Native
Switch (config-vlan) #exit
Switch (config) #
2.
Switch (config) ¥
Switch (config) #int
Switch (config) #interface range F
Switch (config) #interface range FastEthernet 0/1-10
Switch (config-if-range) #switchport mode access
Switch (config-if-range) #switchport access vlan 10
Switch (config-if-range) #exit
Switch (config) #interface range FastEthernet 0/11-20
Switch (config-if-range) #switchport mode access
Switch (config-if-range) #switchport access vlan 20
Switch (config-if-range) #exit
Switch (config) #interface range FastEthernet 0/21-24
Switch (config-if-range)#switchport mode access
Switch (config-if-range) #switchport access vlan 30
Switch (config-if-range) #exit
Switch (config) #


### Cisco projekt — strona 2

Interface range gigabitethernet 0/1-2

Switchport mode trunk

Switchport trunk native vlan 100

do show interfaces switchport
Name: Gig0/1 Name: Gig0/1
Switchport: Enabled Switchport: Enabled
eee eas frunk Administrative Mode: trunk
Administrative Trunking Encapsulation: dot1q Operational Mode: trunk
Operational Trunking Encapsulation: dot1q Administrative Trunking Encapsulation: dot1q
Negotiation of Trunking: On Operational Trunking Encapsulation: dot1q
Access Mode VLAN: 1 (default) Negotiation of Trunking: On
Trunking Native Mode VLAN: 100 (Native) Access Mode VLAN: 1 (default)
Voice VLAN: none Trunking Native Mode VLAN: 100 (Native)
Administrative private-vlan host-association: none Voice VLAN: none
Administrative private-vlan mapping: none Administrative private-vlan host-association: none
Administrative private-vlan trunk native VLAN: none Administrative private-vlan mapping: none
Administrative private-vlan trunk encapsulation: dot1q Administrative private-vlan trunk native VLAN: none
Administrative private-vlan trunk normal VLANs: none Administrative private-vlan trunk encapsulation: dot1q
Administrative private-vlan trunk private VLANs: none Administrative private-vlan trunk normal VLANs: none
Operational private-vlan: none Administrative private-vlan trunk private VLANs: none
Trunking VLANs Enabled: All Operational private-vlan: none
Pruning WEAN Enabled: 2-1001 Trunking VLANs Enabled: All
Capture Mode Disable: Pruning VLANs Enabled: 2-1001
Capture VLANs Allowed: ALL
Protected: false Capture Mode Disabled
Unknown unicast blocked: disabled Capture VLANs Allowed: ALL
Unknown multicast blocked: disabled Protected: false
Appliance trust: none Unknown unicast blocked: disabled

Unknown multicast blocked: disabled
Name: Gig0/2
Switchport: Enabled
Administrative Mode: trunk
Operational Mode: trunk
Administrative Trunking Encapsulation: dot1q
Operational Trunking Encapsulation: dotiq
Negotiation of Trunking: On
Access Mode VLAN: 1 (default)
Trunking Native Mode VLAN: 100 (Native)
Voice VLAN: none
Do show interfaces trunk

Gigo/2 on 02.14 fronting 100 Gigo/ on 02.14 trunking 100
Gigo/2 11005 Gigost 3-108
Gigove—1,10020,s0y190 Gigd/d 1,410, 20,20,100
Port: Vlans in spanning tree forwarding state and not pruned Port: Vlans in spanning tree forwarding state and not pruned
Gigd/2 1,10, 20, 30,100 Gigd/1 1,10,20, 30,100

Interface range fastethernet 0/1-24

Switchport mode access

Switchport nonegotiate

Exit

Show interfaces switchport

Switch#show interfaces switchport

Name: Fa0/1

Switchport: Enabled

Administrative Mode: static access

Operational Mode: static access

Administrative Trunking Encapsulation: dotiq

Operational Trunking Encapsulation: native

Negotiatio: Trunking: Off

— ode VLAN? 10 ee.)

Trunking Native Mode VLAN: 1 (default)

Voice VLAN: none

Administrative private-vlan host-association: none

copy running-config startup-config


### Cisco projekt — strona 3

Lab Task 3:
255.255.255.224
1.2.
R3 (config) #interface gigabitEthernet 0/0
R3(config-if)#ip add
R3(config-if)#ip address 172.16.10.1 255.255.255.224
R3(config-if)#no s
R3(config-if)#no sh
R3(config-if)#no shutdown
R3(config-if)#
SLINK-5-CHANGED: Interface GigabitEthernet0/0, changed state to up
SLINEPROTO-5-UPDOWN: Line protocol on Interface GigabitEthernet0/0, changed state to up
interface gigabitEthernet 0/1
R3(config-if)#ip address 172.16.10.33 255.255.255.224
R3(config-if)#no shutdown
R3(config-if)#
SLINK-5-CHANGED: Interface GigabitEthernet0/1, changed state to up
SLINEPROTO-5-UPDOWN: Line protocol on Interface GigabitEthernet0/1, changed state to up
R3(config-if) texit
R3 (config) #do show ip route
Codes: L - local, C - connected, S - static, R - RIP, M - mobile, B - BGP
D ~ EIGRP, EX - EIGRP external, 0 - OSPF, IA ~ OSPF inter area
Nl - OSPF NSSA external type 1, N2 - OSPF NSSA external type 2
El - OSPF external type 1, £2 ~ OSPF external type 2, E - EGP
i - IS-IS, Ll - IS-IS level-1, L2 - IS-IS level-2, ia - IS-IS inter area
+ - candidate default, U - per-user static route, 0 ~ ODR
P - periodic downloaded static route
Gateway of last resort is not set
172.16.0.0/16 is variably subnetted, 4 subnets, 2 masks
c 172.16.10.0/27 is directly connected, GigabitEthernet0/0
L 172.16.10.1/32 is directly connected, GigabitEthernet0/0
c 172.16.10.32/27 is directly connected, GigabitEthernet0/1
L 172.16.10.33/32 is directly connected, GigabitEthernet0/1
3. 4. 5.
172.16.10.65
172.16.10.66
172.16.10.97
172.16.10.98
172.16.10.129
172.16.10.130
255.255.255.224
Rl (config-if)#ip address 172.16.10.97 255.255.255.224 R2 (config) #interface Serial0/0/0
Rl (config-if)#no sh aoe :
R1(config-if) #no shutdown R2(config-if)#ip address 172.16.10.66 255.255.0.0
R2(config-if)#ip address 172.16.10.66 255.255.255.224
%LINK-5-CHANGED: Interface Serial0/0/0, changed state to down 2 fi -if #
R1 (config-if) # R2 (config-if)
Rl (config-if) # R2 (config-if) #exit
Rl (config-if)#no shutdown * A .
Rl (config-if)#interface Serial0/0/1 R2 (config) #interface Serial0/0/1
R1 (config-if) #exit R2(config-if)#ip address 172.16.10.129 255.255.255.224
Rl (config) #interface Serial0/0/1 iag-i ‘
Rl (config-if)#ip address 172.16.10.65 255.255.255.224 R2 (config if) #ip address 172.16.10.129 255.255.255.224
R3 (config) #interface Serial0/0/1
R3(config-if)#ip address 172.16.10.130 255.255.255.224
R3(config-if)#ip address 172.16.10.130 255.255.255.224
R3 (config-if) #
R3 (config-if) #exit
R3 (config) #interface Serial0/0/0
R3(config-if)#ip address 172.16.10.98 255.255.255.224
R3 (config-if) #


### Cisco projekt — strona 4

6.
eco CEO1 eco CEO2
Physical Config Desktop. Programming Attributes Physical Contig Desktop. Programming Attributes
Interface FastEthernet0 Interface FastEthernetO
IP Configuration IP Configuration
DHCP O Siatic DHCP. O Static
IPv4 Address 172.16.10.189 IPv4 Address 172.16.10.190
‘Subnet Mask (255.255.255.224 ‘Subnet Mask 255.255.255.224
Default Gateway 172.16.10.160 Default Gateway 172.16.10.160
DNS Server 0.0.0.0 DNS Server 0.0.0.0
7.
ece Copyrighter1 eee Copyrighter2
Physical Config Desktop = Programming Attributes Physical Config Desktop | Programming Attributes
Interface FastEthernet0 Interface FastEthernet0
IP Configuration IP Configuration
DHCP O Static DHCP O Static
IPv4 Address 172.16.10.221 IPv4 Address 172.16.10.222
Default Gateway 172.16.10.192 Default Gateway 172.16.10.192
DNS Server 0.0.0.0 DNS Server 0.0.0.0
8.
eco Dialert eee Dialer2
Physical Config Desktop Programming Attributes Physical Config Desktop, Programming Attributes
reece Fastethemet0 Interface Fastethometa
IP Configuration IP Configuration
oHoP O state Dyce O static
IPv4 Address 172.16.10.253 IPv4 Address 172.16.10.254
Default Gateway 172.16.10.224 Default Gateway 172.16.10.224
9.
Office 2 Office 3
eco Employee 1 eee E-mail Server
Physical Config Deso0P= Programming Attributes Physical — Config Services Desktop. Programming Attributes.
ior SeeiereD IP Configuration
DHOP O Static
DHCP O Suatic
DNS Server 0.0.0.9 DNS Server 0.0.0.0


### Cisco projekt — strona 5

eco Employee 2 eco Syslog\NTP Server
Physical Config Deskiop | Programming Attributes Physical Config Services| Desktop | Programming Attributes
Inertace Fasteheet0 8 IP Configuration
1P Configuration bHoP O static
ea OS IPv4 Address 172.16.10.29
baarenteas ee ‘Subnet Mask (255.255.255.224
Renibentt ei Default Gateway 172.16.10.0
Detaut Gateway 172.18:1032
DNS Server 00.00
DNS Sever 0000
eco Guest eco Admin
Physical Config Desktop = Programming Atuibutes Physical Con _Dasitgp | Programming _Attbutes
Interace FastEthernet0 Itertace FastEthornot0
1P Configuration 1P Configuration
DHCP O Satie DHCP O siatic
IPs Adéross 172.16:10.60 IPs Address 172.16.1028
‘Subnet Mask 255,255,255.224 ‘Subnet Mask 255,255,255 224
Default Gatoway 172.16.10% Dotault Gatoway 172.16.100
DNS Sener 00.00 DNS Server 0009
Lab Task 4:
1. interface GigabitEthernet 0/0
no shutdown
SLINK-5-CHANGED: Interface GigabitEthernet0/0, changed state to up
SLINEPROTO-5-UPDOWN: Line protocol on Interface GigabitEthernet0/0, changed state to up
2. 3. 4.
R1 (config) #int
R1 (config) #interface gig
Rl (config) #interface gigabitEthernet 0/0.10
R1 (config-subif) #
SLINK-5-CHANGED: Interface GigabitEthernet0/0.10, changed state to up
SLINEPROTO-5-UPDOWN: Line protocol on Interface GigabitEthernet0/0.10, changed state to
up
enc
R1 (config-subif) #encapsulation d
Rl (config-subif) #encapsulation dot1Q 10
R1 (config-subif)#ip address 172.16.10.161 255.255.255.224
R1 (config-subif) #exit
Rl (config) #interface gigabitEthernet 0/0.20
R1 (config-subif) #
SLINK-5-CHANGED: Interface GigabitEthernet0/0.20, changed state to up
SLINEPROTO-5-UPDOWN: Line protocol on Interface GigabitEthernet0/0.20, changed state to
up
encapsulation dot1Q 20
Rl (config-subif)#ip address 172.16.10.193 255.255.255.224
R1 (config-subif) fexit
R1 (config) #interface gigabitEthernet 0/0.30
Rl (config-subif) #
SLINK-5-CHANGED: Interface GigabitEthernet0/0.30, changed state to up
SLINEPROTO-5-UPDOWN: Line protocol on Interface GigabitEthernet0/0.30, changed state to
up
encapsulation dot1Q 30
Rl (config-subif)#ip address 172.16.10.225 255.255.255.224
R1 (config-subif) #exit


### Cisco projekt — strona 6

5.
R1#
®SYS-5-CONFIG_I: Configured from console by console
show ip interface brief
Interface IP-Address OK? Method Status Protocol
GigabitEthernet0/0 unassigned YES NVRAM up up
GigabitEthernet0/0.10 172.16.10.161 YES manual up up
GigabitEthernet0/0.20 172.16.10.193 YES manual up up
GigabitEthernet0/0.30 172.16.10.225 YES manual up up
GigabitEthernet0/1 unassigned YES NVRAM administratively down down
Serial0/0/0 172.16.10.97 YES manual up up
Serial0/0/1 172.16.10.65 YES manual up up
6.
Switch>en
Switch (config) finterface gigabitEthernet 0/1 Switch#conf t
Switch (config-if) #swi Enter configuration commands, one per line. End with CNTL/Z.
Switch (config-if) #switchport mode trunk Switch (config) #sw
te Switch (config) #int
Switch (config-if) fexit Switch (config) #interface gig
Switch (config) #interface gigabitEthernet 0/2 Switch (config) #interface gigabitEthernet 0/1
Switch (config-if)#switchport mode trunk Switch (config-if) #swit
Switch (config-if) fexit Switch (config-if)#switchport mo
Switch (config-if)#switchport mode trunk
Switch (config-if) #exit
Switchport trunk native vlan 100 Switen(configy af
Show
7
Port | Mode Encapsulation Status Native vlan switchtshow interfaces tr
Gigo/t on 802.14 trunking 200 Switch#show interfaces trunk
Gigd/2 on 802.14 trunking 100 Port Mode Encapsulation Status Native v
Port vlans allowed on trunk Gigo/2 on 802.1q trunking 100
Gig0/1 11-1005
Gigo/2 11008 Port Vlans allowed on trunk
Gigd/1 1-1005
Port Vlans allowed and active in management domain
Gig0/1 1, 10,20, 30,100 Port Vlans allowed and active in management domain
Gigd/2 1,10,20, 30,100 Gigd/1 1,10,20,30,100
Port Vlans in spanning tree forwarding state and not pruned Port Vlans in spanning tree forwarding state and not pr
Gigd/1 1,10,20, 30,100 Gigd/1 1,10,20,30,100
Gigd/2 1,10,20, 30,100
Task 5.
Show port-security address.
Interface fastEthernet 0/2
switchport mode access
switchport port-security
switchport port-security violation restrict
switchport port-security mac-address sticky
Show interfaces status
Interface fast...
Shut down
ExitCopy running-config startup-config


### Cisco projekt — strona 7

Powtarzamy w S71 i S2 dla: Fa 0/1, Fa 0/11, Fa 0/21.
Switch (config) #interface fastEthernet 0/1
Switeh (config-if) #aw
Switch (config-if) fawitchport m
Switch (config-if)fawitchport mode a
Switeh (config-if) baw
Switch (config-if) #awitchport por
Switch (config-if) fawitchport port-security
Switch (config-if) #switchport port-security vioa
Switch (config-if) #awitchport port-security vi
Switch (config-if) fexit
Switch (config) #exit
Switch’
SSYS-S-CONFIG _T: Configured from console by conscle
Port. Name Status vian Duplex Speed Type
Fa0/1 connected 10 auto. auto 10/100Baserx
Fa0/2 notconnect 10 auto auto 10/100BaseTX
Fa0/3 notconnect 10 auto auto 10/100BaseTX
Fa0/6 disabled 10 auto auto 10/100BaseTx Switch(config)#interface range fastEthernet
rors isabied 10 tke les levdeonssent 0/12-20
Pao/it connected. 20 auto "sue, 0/0 SWitch(config-if-range)#shutdown
Pa0/12 disabled 20 auto auto’ 10/100BaaerX
Fao/i4 disabled 20 Gute tute 10/100Baserx
Pa0/15 disabled 20 Gute tute 10/100Baserx
Pa0/16 disabled 20 Gute auto 10/100Baserx
mesa diesbied 20 tito ute 10/100nasenx Copy running-config startup-config
Task 6
Show ip route connected
Passive Interface(s): show ip protocols Routing Information Sources:
Serial interface
No shutdown
R3: gigabitethernet no shutdown
Router ospf 1
router-id 1.1.1.1
Network 111.111.111.111 0.0.0.255 area 0
Passive-interface


### Cisco projekt — strona 8

Show ip protocols
Show ip ospf interface
Show ip ospf neighbor
Copy running-config startup-config
Task 7
Show access-list
Router (config) #access-list 137 deny ip host 172.16.10.60 host 172.16.10.29
Router (config) #exit
Router#show access-lists
Extended IP access list 137
10 deny ip host 172.16.10.60 host 172.16.10.29
Access-list 2137 deny ip host 172.16.10.60 host 172.16.10.29
Task 8
Username Admin password ACDC1973
Enable password beatles1960
Service password-encryption
Banner motd #Only authorized personnel are allowed accessing this device#
Wr
Exit
Task 9
Ip domain-name Cyber.local
Crypto key generate rsa 1024
Ip ssh version 2
Line vty 0 4
Login local
Transport input SSH


### Cisco projekt — strona 9

Show ip ssh
Show ssh

Router>en

Password:

Password

Router#conf t

Enter configuration commands, one per line. End with CNTL/Z.

Router (config) #ip do

Router (config) #ip dom

Router (config) #ip domain-name Cyber. local

Router (config) #cry

Router (config) #crypto key generate rsa

% Please define a hostname other than Router

Router (config) thostn

Router (config) #hostname R1

Rl (config) #crypto key generate rsa

& You already have RSA keys defined named R1.Cyber.com .

% Do you really want to replace them? [yes/no]: yes

The name for the keys will be: R1.Cyber.local

Choose the size of the key modulus in the range of 360 to 4096 for your
General Purpose Keys. Choosing a key modulus greater than 512 may take
a few minutes

How many bits in the modulus [512]: 1024

% Generating 1024 bit RSA keys, keys will be non-exportable... [OK]

Rl (config) #ip ssh version 2

*Mar 2 11:36:58.388: $SSH-5-ENABLED: SSH 1.99 has been enabled

Rl (config) #line vty 0 4

Rl (config-line)#login local

Rl (config-line)#transport input ssh

Rl (config-line) #exit

Rl#show ip ssh

SSH Enabled - version 2.0

Authentication timeout: 120 secs; Authentication retries: 3

R1¢

C:\>ssh “1 Adin 172.16.10.1

Password

i Login invalid

Password:

only authorized personnel are allowed accessing this device!

banner motd

231

R3# show ip ssh

SSH Enabled - version 2.0

Authentication timeout: 120 secs; Authentication retries: 3

R3#show ssh

Connection Version Mode Encryption Hmac State

Username

0 1.99 IN aes128-cbe hmac-shal Session Started

Admin

0 1.99 OUT aes128-cbce hmac-shal Session Started

Admin

%No SSHvl server connections running.

R3#


---

# 06 — Wszystkie linki i zasoby

Linki z `Padriseup` zostały odczytane z natywnych adnotacji PDF. Linki z PDF-ów obrazowych pochodzą z treści widocznej na stronach i są oznaczone jako OCR.

| Źródło | Strona | URL | Sposób odczytu |
|---|---:|---|---|
| Padriseup | 1 | <https://www.hackampus.com/book/480> | exact PDF hyperlink |
| Padriseup | 2 | <https://pl.wikipedia.org/wiki/ARPANET> | exact PDF hyperlink |
| Padriseup | 2 | <https://pl.wikipedia.org/wiki/Model_OSI> | exact PDF hyperlink |
| Padriseup | 3 | <https://pl.wikipedia.org/wiki/Model_TCP/IP> | exact PDF hyperlink |
| Padriseup | 3 | <https://www.dipol.com.pl/skretka_komputerowa_-_oznaczenia_standardy_pomiary_bib526.htm> | exact PDF hyperlink |
| Padriseup | 5 | <https://www.submarinecablemap.com/> | exact PDF hyperlink |
| Padriseup | 5 | <https://blog.programster.org/ethernet-cheatsheet> | exact PDF hyperlink |
| Padriseup | 5 | <https://www.electronics-notes.com/articles/connectivity/ethernet-ieee-802-3/cables-types-pinout-cat-5-5e-6.php> | exact PDF hyperlink |
| Padriseup | 5 | <https://www.boston.co.uk/blog/2019/05/01/network-cables-reference-guide.aspx> | exact PDF hyperlink |
| Padriseup | 5 | <https://www.universalnetworks.co.uk/faq/what-does-utp-s-utp-ftp-stp-and-sftp-mean/> | exact PDF hyperlink |
| Padriseup | 5 | <https://www.n2yo.com/> | exact PDF hyperlink |
| Padriseup | 5 | <https://www.netia.pl/pl/blog/ipv4-vs-ipv6-%E2%80%93-co-to-za-protokoly-i-jakie-sa-miedz> | exact PDF hyperlink |
| Padriseup | 5 | <http://kti.eti.pg.gda.pl/ktilab/ipv6-adr/ipv6-adresy.pdf> | exact PDF hyperlink |
| Padriseup | 5 | <https://www.soisk-me.pl/klasa-iv-sieci/klasy-adresow-ip> | exact PDF hyperlink |
| Padriseup | 5 | <https://i.ytimg.com/vi/D1avGPpSJHs/maxresdefault.jpg> | exact PDF hyperlink |
| Padriseup | 5 | <http://www.lomilowka.pl/upload/file/PiMLSK/klasyadres%C3%B3wIP.pdf> | exact PDF hyperlink |
| Padriseup | 5 | <https://www.itbridge.pl/baza-wiedzy/adresacja-ip-publiczne-i-prywatne-adresy-ipv4> | exact PDF hyperlink |
| Padriseup | 5 | <https://pl.wikipedia.org/wiki/Strefa_Fresnela> | exact PDF hyperlink |
| Padriseup | 5 | <https://www.bestpartner.pl/index.php?d=kfresnel> | exact PDF hyperlink |
| Padriseup | 5 | <https://pl.wikipedia.org/wiki/Internet_Control_Message_Protocol> | exact PDF hyperlink |
| Padriseup | 6 | <https://en.wikipedia.org/wiki/List_of_TCP_and_UDP_port_numbers> | exact PDF hyperlink |
| Padriseup | 7 | <https://snipboard.io/rvm902.jpg> | exact PDF hyperlink |
| Padriseup | 7 | <https://pl.wikipedia.org/wiki/EBCDIC> | exact PDF hyperlink |
| Padriseup | 7 | <https://pl.wikipedia.org/wiki/Frame_Relay> | exact PDF hyperlink |
| Padriseup | 7 | <https://www.guru99.com/types-of-ip-addresses.html> | exact PDF hyperlink |
| Padriseup | 7 | <https://pmr.ii.pw.edu.pl/~pmr/ws/> | exact PDF hyperlink |
| Padriseup | 7 | <https://www.wireshark.org/> | exact PDF hyperlink |
| Padriseup | 8 | <https://www.adminsub.net/mac-address-finder/eui> | exact PDF hyperlink |
| Padriseup | 8 | <https://access.redhat.com/sites/default/files/attachments/rh_ip_command_cheatsheet_1214_jcs_print.pdf> | exact PDF hyperlink |
| Padriseup | 8 | <https://www.asus.com/pl/networking-iot-servers/whole-home-mesh-wifi-system/zenwifi-wifi-systems/asus-zenwifi-ax-hybrid-xp4/> | exact PDF hyperlink |
| Padriseup | 9 | <https://sieci.infopl.info/> | exact PDF hyperlink |
| Padriseup | 9 | <https://miroslawzelent.pl/nauka/the-slight-edge-jeff-olson/> | exact PDF hyperlink |
| Padriseup | 9 | <https://www.komputronik.pl/informacje/co-to-jest-switch-czym-przelacznik-sieciowy-rozni-sie-od-routera/> | exact PDF hyperlink |
| Padriseup | 9 | <https://community.fs.com/blog/different-types-of-routers-in-networking.html> | exact PDF hyperlink |
| Padriseup | 9 | <https://www.spiceworks.com/tech/networking/articles/what-is-network-switch/> | exact PDF hyperlink |
| Padriseup | 9 | <https://sieci.infopl.info/index.php/urzadzenia/switch> | exact PDF hyperlink |
| Padriseup | 9 | <https://soisk.info/index.php/Typy_transmisji_danych:_unicast,_multicast,_broadcast> | exact PDF hyperlink |
| Padriseup | 9 | <https://www.guru99.com/collision-broadcast-domain.html> | exact PDF hyperlink |
| Padriseup | 9 | <https://www.electronics-notes.com/articles/connectivity/ethernet-ieee-802-3/cables-types-pinout-cat-5-5e-6.php> | exact PDF hyperlink |
| Padriseup | 9 | <https://www.vssmonitoring.com/types-of-ethernet-cables/> | exact PDF hyperlink |
| Padriseup | 9 | <https://www.unitek-products.com/blogs/products> | exact PDF hyperlink |
| Padriseup | 9 | <https://www.komputronik.pl/informacje/jaki-kabel-sieciowy-kabel-do-internetu/> | exact PDF hyperlink |
| Padriseup | 9 | <https://cablesupply.com/rj45-ethernet-wiring-color-guides/> | exact PDF hyperlink |
| Padriseup | 9 | <https://blog.laptopcontrol.pl/informatyka/kategorie-kabel-sieciowy-lan-skretka/> | exact PDF hyperlink |
| Padriseup | 10 | <https://pasja-informatyki.pl/sieci-komputerowe/topologie-sieci/> | exact PDF hyperlink |
| Padriseup | 10 | <https://pl.wikipedia.org/wiki/Regional_Internet_Registry> | exact PDF hyperlink |
| Padriseup | 10 | <https://www.netia.pl/pl/blog/ipv4-vs-ipv6-%E2%80%93-co-to-za-protokoly-i-jakie-sa-miedz> | exact PDF hyperlink |
| Padriseup | 10 | <https://www.soisk-me.pl/klasa-iv-sieci/klasy-adresow-ip> | exact PDF hyperlink |
| Padriseup | 10 | <http://www.lomilowka.pl/upload/file/PiMLSK/klasyadres%C3%B3wIP.pdf> | exact PDF hyperlink |
| Padriseup | 10 | <https://pl.wikipedia.org/wiki/Maska_podsieci> | exact PDF hyperlink |
| Padriseup | 10 | <https://snipboard.io/rvm902.jpg> | exact PDF hyperlink |
| Padriseup | 10 | <https://pasja-informatyki.pl/sieci-komputerowe/model-tcp-ip-iso-osi/> | exact PDF hyperlink |
| Padriseup | 10 | <https://www.soisk-me.pl/klasa-iv-sieci/model-iso-osi-i-tcp-ip> | exact PDF hyperlink |
| Padriseup | 10 | <http://oprogramowaniu.pl/czym-jest-enkapsulacja/> | exact PDF hyperlink |
| Padriseup | 10 | <https://pmr.ii.pw.edu.pl/~pmr/ws/> | exact PDF hyperlink |
| Padriseup | 11 | <https://wiki.wireshark.org/CaptureFilters> | exact PDF hyperlink |
| Padriseup | 11 | <https://www.wireshark.org/docs/wsug_html_chunked/> | exact PDF hyperlink |
| Padriseup | 11 | <https://bugs.wireshark.org/bugzilla/attachment.cgi?id=11612> | exact PDF hyperlink |
| Padriseup | 11 | <https://wiki.wireshark.org/SampleCaptures> | exact PDF hyperlink |
| Padriseup | 11 | <https://wiki.wireshark.org/uploads/__moin_import__/attachments/SampleCaptures/dhcp.pcap> | exact PDF hyperlink |
| Padriseup | 11 | <https://rioco.pl/komendy/komendy-ciscoios/> | exact PDF hyperlink |
| Padriseup | 11 | <https://wiki.wireshark.org/uploads/__moin_import__/attachments/SampleCaptures/dns-icmp.pcapng.gz> | exact PDF hyperlink |
| Padriseup | 11 | <https://ia601604.us.archive.org/20/items/cisco-packet-tracer-821-ubuntu-64bit/CiscoPacketTracer_821_Windows_64bit.exe> | exact PDF hyperlink |
| Padriseup | 12 | <https://www.hackampus.com/practices/book/480/chapter/2945> | exact PDF hyperlink |
| Padriseup | 12 | <https://www.cloudshark.org/captures/849d3c7f09d3> | exact PDF hyperlink |
| Padriseup | 13 | <https://beyond.hackampus.com/canvas/general/general-LLcAf-2021.12.12.10.09.23-Extra%20Files.rar> | exact PDF hyperlink |
| Padriseup | 15 | <https://www.cisco.com/c/en/us/support/docs/routers/7200-series-routers/12219-17.html> | exact PDF hyperlink |
| Padriseup | 15 | <https://beyond.hackampus.com/canvas/general/general-qji5R-2021.12.12.10.18.12-Extra%20FIles.rar> | exact PDF hyperlink |
| Padriseup | 17 | <https://www.browserling.com/tools/ip-to-bin> | exact PDF hyperlink |
| Padriseup | 17 | <https://www.browserling.com/tools/bin-to-ip> | exact PDF hyperlink |
| Padriseup | 18 | <https://42.pl/ipcalc/> | exact PDF hyperlink |
| Padriseup | 18 | <https://beyond.hackampus.com/canvas/general/general-YbaTH-2021.12.12.10.36.21-NET-07-L1.rar> | exact PDF hyperlink |
| Padriseup | 19 | <https://beyond.hackampus.com/canvas/general/general-LJUoB-2021.12.12.10.39.31-Extra%20Files.rar> | exact PDF hyperlink |
| Padriseup | 19 | <https://ipwithease.com/ospf-timers/> | exact PDF hyperlink |
| Padriseup | 23 | <https://www.ciscopress.com/articles/article.asp?p=2294214&seqNum=2> | exact PDF hyperlink |
| Padriseup | 25 | <https://pasja-informatyki.pl/sieci-komputerowe/> | exact PDF hyperlink |
| Padriseup | 25 | <https://42.pl/ipcalc/> | exact PDF hyperlink |
| Padriseup | 25 | <https://beyond.hackampus.com/canvas/general/general-1izuf-2021.12.12.10.42.45-NET-09-L1.rar> | exact PDF hyperlink |
| Padriseup | 28 | <https://beyond.hackampus.com/canvas/general/general-NVfKC-2021.12.12.11.25.45-NET-11-L1.rar> | exact PDF hyperlink |
| Textbook | 22 | <www.cyber.com> | OCR-visible URL |
| Textbook | 80 | <http://www.cisco.com/techsupport> | OCR-visible URL |
| Labs | 7 | <www.facebook.com> | OCR-visible URL |
| Labs | 10 | <www.cisco.com?> | OCR-visible URL |
| Labs | 26 | <http://juice-shop.herokuapp.com/#/> | OCR-visible URL |
| Labs | 27 | <http://juice-shop.herokuapp.com/> | OCR-visible URL |
| Labs | 30 | <http://hack-yourself-first.com/> | OCR-visible URL |
| Labs | 31 | <www.bing.com> | OCR-visible URL |
| Labs | 32 | <www.bing.com> | OCR-visible URL |
| Labs | 32 | <www.google-analytics.com> | OCR-visible URL |
| Labs | 41 | <https://vww.cisco.com/c/en/us/about/legal/> | OCR-visible URL |
| Labs | 85 | <www.ciaco.com/techsupport> | OCR-visible URL |
| Labs | 264 | <www.cyberpro.com> | OCR-visible URL |
| Slides | 44 | <www.cyber.com> | OCR-visible URL |
| Slides | 170 | <http://www> | OCR-visible URL |

---

# 07 — Command Reference — wszystkie wykryte polecenia

Indeks jest automatycznie wyciągnięty z pięciu materiałów. Zachowuje numer strony i oryginalny zapis linii; pełny kontekst znajduje się w plikach źródłowych.


## Textbook

- s. 5: `Network Types`
- s. 6: `Network Structure`
- s. 6: `Interface Controller), to be able to send and receive information.`
- s. 7: `Network Interface Controller (NIC)`
- s. 7: `Network Devices`
- s. 7: `Network devices act as bridges, interconnecting endpoint devices.`
- s. 7: `network.`
- s. 8: `copy of the data to all devices on the same network segment. Broadcast`
- s. 18: `IP Address`
- s. 18: `IPv6 - Due to advances in technology, four billion addresses were soon no longer`
- s. 18: `IPv6 addresses have not yet been fully integrated in modern use cases.`
- s. 18: `Network Classes`
- s. 20: `Network Protocol Examples`
- s. 20: `IP - The Internet Protocol is used to establish communication over the network, without`
- s. 20: `Network Commands`
- s. 20: `network and monitor it.`
- s. 21: `Ping`
- s. 21: `Ping is the most common command in administrative networking activity.`
- s. 21: `Ping x.x.x.x`
- s. 21: `C:\Windows\system32> ping 8.8.8.8`
- s. 21: `Ping statistics for 8.8.8.8:`
- s. 21: `IPconfig`
- s. 21: `ipconfig - displays a computer’s IP configuration.`
- s. 21: `ipconfig /all — displays extended information.`
- s. 21: `ipconfig /release — drops an IP address.`
- s. 21: `ipconfig /renew — requests a new IP address.`
- s. 21: `ipconfig`
- s. 22: `C:\Windows\system32> ipconfig`
- s. 22: `Nslookup`
- s. 22: `Nslookup sends a query to get the name of a computer by its IP address.`
- s. 22: `nslookup x.x.x.x`
- s. 22: `C:\Windows\system32> nslookup www.cyber.com`
- s. 22: `Name: cyber.com`
- s. 22: `C:\Windows\system32> nslookup 199.244.49.102`
- s. 23: `Tracert`
- s. 23: `Tracert displays all the stations (hops) along the route taken by the information to its`
- s. 23: `tracert X.x.x.x`
- s. 23: `C:\Windows\system32> tracert 8.8.8.8`
- s. 24: `Netsh`
- s. 24: `Netsh [command \ option ]`
- s. 24: `C:\Windows\system32> netsh interface ip set address “Ethernet" static`
- s. 24: `C:\Windows\system32> netsh interface ip show config`
- s. 25: `network, and affect their quality.`
- s. 26: `Network). It is mainly used to pair devices and allows communication at up to 100`
- s. 30: `network configured to use DHCP, such as PCs, routers, firewalls, servers, and others.`
- s. 30: `SSH - Secure SHell is a secure command-line protocol that allows the user to run remote`
- s. 31: `Network Models`
- s. 32: `Transport, Network, Datalink, and Physical.`
- s. 32: `TRANSPORT TRANSPORT`
- s. 32: `NETWORK NETWORK`
- s. 34: `Transport TCP, UDP, RTP, SCTP`
- s. 34: `Network IPv4, IPv6, ICMPv4, ICMPv6, IPX`
- s. 36: `Network Access Physical Layer Network Access`
- s. 37: `SSH, FTP, TFTP, SNMP, SMTP, DHCP, X Windows, RDP, and others.`
- s. 42: `service on that end device.`
- s. 43: `network administrator must know them.`
- s. 45: `Netstat Example:`
- s. 45: `C:\WINDOWS\system32>netstat -ab`
- s. 46: `No Interfaces found`
- s. 56: `ARP operates in Layers 2 and 3 of the OSI model.`
- s. 56: `ARP Process`
- s. 57: `ARP Table:`
- s. 57: `ARP Table (Cache)`
- s. 57: `arp —a and arp —g display the host ARP table.`
- s. 57: `Show arp displays a Cisco device ARP table.`
- s. 57: `C:\Windows\system32>arp -a 7`
- s. 57: `Interface: 10.71.0.110 --- x17`
- s. 58: `arp —d deletes the host ARP table.`
- s. 58: `arp —s adds a static entry to the ARP table that resolves to a specific IP address.`
- s. 58: `arp inet_addr defines a specific IP address.`
- s. 58: `arp eth_addr defines a specific MAC address.`
- s. 58: `C:\Windows\system32>arp -d`
- s. 58: `C:\Windows\system32>arp -s 10.0.0.2 @0-aa-bb-11-22-33`
- s. 59: `Encapsulation - Adding Headers and Trailers to data is called encapsulation. Processing`
- s. 59: `Encapsulation Process`
- s. 60: `Encapsulation in Layers 4 to 7`
- s. 61: `IP Header TCP Header Payload`
- s. 61: `Encapsulation in Layers 1 to 3`
- s. 62: `show mac-address-table`
- s. 62: `Switch#show mac-address-table`
- s. 62: `Vlan Mac Address Type Ports`
- s. 67: `SSH`
- s. 69: `Switch>enable`
- s. 69: `Switch#configure terminal`
- s. 69: `Switch(config)#exit`
- s. 69: `Switch#exit`
- s. 69: `Switch>`
- s. 70: `Switch>di`
- s. 70: `Switch#show`
- s. 70: `Switch(config)#hostnme S1`
- s. 72: `hostname <device name>`
- s. 72: `Switch(config)#hostname S1-Floor1`
- s. 72: `S1-Floor1(config)#`
- s. 72: `username <user-name> password <password>`
- s. 72: `Switch(config)#username Admin password p@nd@`
- s. 72: `Switch(config)#username Peter password Spiderm@n`
- s. 73: `enable password <password>`
- s. 73: `Switch(config)#enable password c!sc@`
- s. 73: `banner motd #security-massage#`
- s. 73: `Switch(config)#banner motd #Access to this device is for`
- s. 73: `Configured passwords appear in plain text in the configuration file.`
- s. 73: `service password-encryption`
- s. 73: `Switch(config)#service password-encryption`
- s. 74: `copy running-config startup-config`
- s. 74: `line console 0 & login local`
- s. 74: `Switch(config-line)#login local`
- s. 74: `Switch(config-line)#exit`
- s. 75: `hostname S1-Floor1`
- s. 75: `enable password 7 9822@D5D@A49`
- s. 75: `username Admin privilege 1 password 7 @8316C4@@D39`
- s. 75: `banner motd “CAccess to this device is for authorized personnel only!`
- s. 75: `line con @`
- s. 75: `login local`
- s. 76: `copy running-config tftp`
- s. 77: `Sl#copy running-config tftp:`
- s. 77: `Sl1#copy tftp: flash:`
- s. 77: `S1# Configuration terminal`
- s. 77: `S1(config)#boot system flash®://c1901-imoversa;19.mz.SPA.152-4.M3.bin`
- s. 77: `S1(config)# exit`
- s. 77: `S1#copy running-config startup-config`
- s. 77: `Sl#reload`
- s. 78: `Configure Register Value`
- s. 78: `Router(config)# config-register @x2102`
- s. 78: `Router(config)# end`
- s. 78: `Router# copy running-config startup-config`
- s. 78: `Router# Reload`
- s. 80: `Router#show version`
- s. 81: `Shutdown - This is the default violation mode. When a violation occurs, the port will be`
- s. 82: `show interfaces [interface] status`
- s. 82: `Switch# show interfaces fastEthernet 0/1 status`
- s. 83: `Enable Port Security`
- s. 83: `interface [interface-id]. Then, Access mode needs to be set with switchport mode`
- s. 83: `switchport port-security`
- s. 84: `switchport mode access`
- s. 84: `Switch(config)# interface fastEthernet @/1`
- s. 84: `Switch(config-if)# switchport mode access`
- s. 84: `Switch(config-if)# switchport port-security`
- s. 84: `Switch(config-if)#`
- s. 84: `switchport port-security [configuration] [value]`
- s. 84: `Switch(config)# interface fastEthernet 0/1`
- s. 84: `Switch(config-if)# switchport port-security violation restrict`
- s. 84: `Switch(config-if)# switchport port-security mac-address sticky`
- s. 84: `Switch(config-if)# switchport port-security maximum 5`
- s. 85: `Switch# show port-security`
- s. 85: `Switch# show port-security address`
- s. 85: `Vlan Mac Address Type Ports Remaining Age`
- s. 86: `SSH - SSH is similar to Telnet, but with a significant difference: SSH encrypts all data`
- s. 86: `SSH Encryption`
- s. 88: `interface on the router.`
- s. 89: `SSH Prerequisites`
- s. 89: `S1(config)#username Admin password p@nd@`
- s. 89: `S1(config)#enable password c!sc@`
- s. 89: `S1(config)#service password-encryption`
- s. 89: `S1(config)#banner motd #Access to this device is for`
- s. 89: `S1(config)#ip domain-name CyberPro.com`
- s. 90: `SSH Configuration Commands`
- s. 90: `line vty <id-range> & login local`
- s. 90: `S1(config)#line vty @ 15`
- s. 90: `S1(config-line)#login local`
- s. 90: `S1(config-line)#transport input ssh`
- s. 90: `S1(config-line)#exit`
- s. 90: `IP Switch Settings`
- s. 90: `Interface vian 1 & ip address <ip-address> < subnet-mast>`
- s. 90: `S1(config)#interface vlan 1`
- s. 90: `S1(config-if)#ip address 10.0.0.150 255.255.255.080`
- s. 90: `S1(config-if)#no shutdown`
- s. 90: `S1(config-if)#exit`
- s. 90: `S1(config)#ip default-gateway 10.0.0.1`
- s. 91: `crypto key generate rsa`
- s. 91: `S1(config)#crypto key generate rsa`
- s. 91: `Show ssh command presents the active SSH sessions on the network device.`
- s. 91: `Show ip ssh displays the version definition, authentication timeout, and retries.`
- s. 91: `S1#show ssh`
- s. 91: `S1#show ip ssh`
- s. 91: `SSH Enabled - version 2.0`
- s. 92: `SSH Connection`
- s. 92: `ssh -I <username> <target-ip>`
- s. 99: `Router Interfaces`
- s. 100: `Interface Configuration`
- s. 100: `Router interfaces need to be set up with IP addresses, similar to computer network`
- s. 100: `1(config)#interface gigabitEthernet 0/0`
- s. 100: `R1(config-if)#ip address 192.168.0.1 255.255.255.0`
- s. 100: `R1(config-if)#no shutdown`
- s. 100: `R1(config-if)#exit`
- s. 100: `R1(config)#exit`
- s. 100: `Rl#show ip interface brief`
- s. 100: `Interface IP-Address OK? Method Status Protocol`
- s. 100: `interface will always be available.`
- s. 100: `interface must have a unique IP.`
- s. 101: `Router(config)#interface loopback @`
- s. 101: `Router(config-if)#ip address 10.10.10.10 255.0.0.0`
- s. 101: `Router(config-if)#no shutdown`
- s. 101: `Router(config-if)# exit`
- s. 102: `Encapsulation - The router re-encapsulates the packet with new Layer 2 headers for the`
- s. 103: `No Route - If there is no static or dynamic route in the network device’s routing table, it`
- s. 103: `no other known route to which they should be sent.`
- s. 103: `No Gateway - If there is no ‘Gateway of last resort’ and the destination packet is not`
- s. 103: `Router# show ip route`
- s. 105: `network. It is used for host identification and communication.`
- s. 105: `Network - Represents the network segment part of the IP address.`
- s. 107: `network (127.0.0.0/8) is reserved for loopback addresses.`
- s. 108: `network, and there are no enforced rules.`
- s. 109: `IPv6 was designed to solve the IPv4 address limitation and provide additional`
- s. 109: `IPv6 addresses are long and difficult to read. Some rules exist to omit specific numbers`
- s. 110: `IPv6 Address Breakdown`
- s. 110: `Router(config-if)#ipv6é address`
- s. 110: `Configure and Verify IPv6é`
- s. 110: `ipv6 unicast-routing.`
- s. 110: `Configure IPv6 on a router interface using the command ipv6é address.`
- s. 110: `Router(config)#ipv6 unicast-routing`
- s. 110: `Router(config)#interface gigabitEthernet0/e/e`
- s. 110: `Router(config-if)#ipv6 address 2001: @ABC: Q@BB : 0000: 0000 : 8000: 0000 : 0801/64`
- s. 110: `Router (config-if)#exit`
- s. 110: `Router#show ipv6é interface brief`
- s. 112: `IPv6 Address Example`
- s. 113: `network growth.`
- s. 116: `Network Portion Host Portion`
- s. 122: `Network Planning`
- s. 123: `configured with static addresses.`
- s. 123: `network must be assigned an IP address.`
- s. 124: `Router Operation Review`
- s. 124: `interface.`
- s. 124: `Encapsulation The router re-encapsulates the packet with new Layer 2 headers`
- s. 124: `interface from which the packet must exit.`
- s. 126: `No CPU and memory usage for Configuration and maintenance`
- s. 126: `Network administrators decide if and when to use Static Routing, based on network`
- s. 127: `Network Topology Example`
- s. 128: `Ri(config)#ip route 10.1.0.0`
- s. 128: `route command.`
- s. 128: `R1(config)#ip route 10.1.0.@ 255.255.255.@ 172.16.0.2`
- s. 128: `R1(config)#ip route 10.2.0.0 255.255.255.0 gigabitEthernet 1/0`
- s. 128: `R1(config)#do show ip route`
- s. 129: `R1(config)#ip route 0.0.0.0 0.0.0.8 gigabitEthernet 2/0`
- s. 129: `route (1 vs. 110).`
- s. 130: `network, it is used to forward traffic to a specific host. It uses`
- s. 130: `ip route <network-address> <subnet-mask> <direction> <AD>`
- s. 130: `Ri(config)#ip route 192.168.1.@ 255.255.255.@ 172.16.0.2`
- s. 130: `Ri(config)#ip route 192.168.1.@ 255.255.255.0@ 10.0.0.2`
- s. 130: `Ri(config)#do show ip route`
- s. 131: `ip route <ip-address> 255.255.255.255 <direction>`
- s. 131: `R1(config)#ip route 192.168.1.5 255.255.255.255 172.16.0.2`
- s. 131: `route is used.`
- s. 132: `Network Address:`
- s. 132: `ip route <summarize-address> <summarize-mask> <direction>`
- s. 132: `R1i(config)#ip route 172.8.0.@ 255.248.0.0 10.0.0.1`
- s. 134: `network addresses are formatted.`
- s. 134: `IPv6 supports the same static routing types, and most of the parameters are identical to`
- s. 134: `IPv6 Static Routing Requirements`
- s. 134: `IPv6 Static Routing Syntax`
- s. 134: `router.`
- s. 134: `R1(config)#ipv6 route`
- s. 135: `IPv6 Configuration Example`
- s. 135: `R1(config)#ipv6 route 2001:abcd:cafe::/64 2002:abcd:aaaa::1`
- s. 135: `Ri(config)#ipv6é route serial 0/0/08`
- s. 135: `Ri(config)#ipv6 route 2001:abcd:cafe:: gigabitethernet0/o`
- s. 135: `R1(config)#ipv6 route 2001:abcd:cafe::/64 gigabitetherneto/e`
- s. 135: `show ipv6 route displays and verifies the IPv6 routing table.`
- s. 135: `show ipv6 route`
- s. 135: `Ri(config)#do show ipv6é route`
- s. 136: `router does not reply, it will eventually be considered “dead” by the sending router.`
- s. 138: `network destinations.`
- s. 139: `Router#show ip route`
- s. 139: `network topologies themselves.`
- s. 139: `route to each network.`
- s. 139: `network failure, the protocols will search for an alternate path.`
- s. 144: `R1(config)#router rip`
- s. 144: `R1(config-router)#version 2`
- s. 144: `R2(config-router)#no auto-summary`
- s. 144: `R1(config-router)#network 192.168.10.0`
- s. 144: `R1(config-router)#network 172.16.0.0`
- s. 144: `R1(config-router)#network 172.16.0.8`
- s. 144: `R1(config-router)#passive-interface gigabitEthernet 0/@`
- s. 144: `R2(config)#router rip`
- s. 144: `R2(config-router)#version 2`
- s. 144: `R2(config-router)#network 192.168.20.0`
- s. 144: `R2(config-router)#network 172.16.0.0`
- s. 144: `R2(config-router)#network 172.16.0.4`
- s. 144: `R2(config-router)#passive-interface gigabitEthernet 0/@`
- s. 145: `router rip enables RIP and enters RIP configuration mode.`
- s. 145: `network advertises the network and enables RIP updates on the network interface.`
- s. 145: `passive-interface disables RIP updates on the interface.`
- s. 145: `Rl#show ip route`
- s. 146: `Show IP Protocols`
- s. 146: `show ip protocols displays the current protocol settings. This is valid for every dynamic`
- s. 147: `Rl#show ip protocols`
- s. 147: `Interface Send Recv Triggered RIP Key-chain`
- s. 148: `R1(config)#ip route 0.0.0.0`
- s. 148: `R1(config-router)#`
- s. 148: `R2(config)#do show ip route`
- s. 151: `Router ID`
- s. 151: `Interface is selected as the OSPFv2 router ID.`
- s. 152: `A>`
- s. 153: `R1(config)#router ospf 1`
- s. 153: `R1(config-router)#router-id 1.1.1.1`
- s. 153: `R1(config-router)#network 192.168.10.0 @.0.0.255 area @`
- s. 153: `R1(config-router)#network 172.16.0.0 0.0.0.3 area @`
- s. 153: `R1(config-router)#network 172.16.0.8 0.0.0.3 area @`
- s. 153: `R1(config-router)#passive-interface gigabitethernet 0/0`
- s. 154: `router ospf enables OSPF and enters OSPF configuration mode.`
- s. 154: `router-id sets the router OSPF identifier.`
- s. 154: `network advertises the network and enables OSPF updates on the network interface.`
- s. 154: `passive-interface disables OSPF updates on the interface.`
- s. 154: `network, both routes will be added to the table, and load balancing will be applied. For`
- s. 154: `show ip protocols displays the current protocol settings.`
- s. 155: `show ip ospf interface displays timer information.`
- s. 155: `show ip ospf neighbor displays adjacent OSPF-enabled routers.`
- s. 155: `Router ID 1.1.1.1`
- s. 155: `router interface.`
- s. 158: `VLAN is a Layer 2 feature that represents a broadcast domain, enabling network`
- s. 158: `VLAN ID`
- s. 158: `VLAN Types`
- s. 159: `interface called SVI. The management VLAN is also used for remote connection via`
- s. 159: `VLAN 1, and all ports are associated with it by default. Additional VLANs are available in`
- s. 159: `S1#show vlan brief`
- s. 159: `VLAN Name Status Ports`
- s. 159: `VLAN Configuration`
- s. 159: `Switch(config)#vlan 10`
- s. 159: `Switch(config-vlan)#name HR`
- s. 159: `Switch(config-vlan)#exit`
- s. 160: `Switchport Modes`
- s. 160: `Switchport Access Mode`
- s. 161: `Switch(config)#interface fastEthernet 0/1`
- s. 161: `Switch(config-if)#switchport mode access`
- s. 161: `Switch(config-if)#switchport access vlan 10`
- s. 161: `Switch(config-if)#exit`
- s. 161: `Switch(config)#interface range fastEthernet @/1-5`
- s. 161: `switchport.`
- s. 161: `Sl#show vlan brief`
- s. 161: `VLAN.`
- s. 162: `Switch(config)#interface fastEthernet @/1`
- s. 162: `Switch(config-if)#switchport voice vlan 101 //assume its pre-`
- s. 162: `configured VLAN`
- s. 164: `S1(config)#interface gigabitEthernet @/1`
- s. 164: `S1(config-if)#switchport mode dynamic auto`
- s. 164: `S1(config-if)#switchport mode dynamic desirable`
- s. 164: `switchport nonegotiate.`
- s. 164: `S1(config)#interface fastEthernet @/1`
- s. 164: `S1(config-if)#switchport mode access`
- s. 164: `S1(config-if)#switchport nonegotiate`
- s. 164: `S1#show interfaces switchport`
- s. 164: `Name: FaQ/1`
- s. 164: `Switchport: Enabled`
- s. 165: `switchport mode trunk`
- s. 165: `Switch(config)#interface gigabitEthernet 0/1`
- s. 165: `Switch(config-if)#switchport mode trunk`
- s. 165: `switchport access trunk allowed vlan vlan-id`
- s. 166: `Switch(config-if)#switchport mode trunk allow vlan 10`
- s. 167: `Switchport trunk native vlan vlan-id`
- s. 167: `Switch(config-if)#switchport trunk native vlan 100`
- s. 168: `network, which means they are also broadcast domains. Switches (which generally`
- s. 168: `Router-On-A-Stick`
- s. 168: `Ri(config)#interface gigabitEthernet 0/0.1`
- s. 168: `R1(config)#interface gigabitEthernet 0/0.2`
- s. 168: `R1(config)#interface gigabitEthernet 0/0.3`
- s. 169: `S1(config)#interface gigabitEthernet 0/1`
- s. 169: `S1(config-if)#switchport mode trunk`
- s. 169: `R1(config)#interface gigabitEthernet 0/0`
- s. 169: `R1(config-if)#`
- s. 169: `R1(config)#interface gigabitEthernet 0/0.1`
- s. 169: `R1(config-subif)#encapsulation dot1Q 100`
- s. 169: `R1(config-subif)#ip address`
- s. 169: `R1(config-subif)#exit`
- s. 169: `R1(config-subif)#encapsulation dot1Q 200`
- s. 171: `network-related documentation.`
- s. 171: `Network documentation includes physical and logical topological diagrams, network`
- s. 171: `network performance baselines.`
- s. 172: `Network Management Software (NMS) provides excellent tools for troubleshooting.`
- s. 173: `Show interfaces - This command outputs a large volume of information, including`
- s. 173: `interface errors, bandwidth utilization, and interface speed.`
- s. 173: `Show ip route - This command verifies network reachability, and indicates if routing`
- s. 173: `Show ip interface brief - This command presents only information about interfaces`
- s. 173: `Show running-config - This command displays the complete router configuration in use`
- s. 173: `Show start-up config - By default, the initial configuration controlling the system is the`
- s. 173: `R2#ping`
- s. 175: `Enable/disable CDP on the device.`
- s. 175: `Switch(config)#cdp run`
- s. 175: `Switch(config)#no cdp run`
- s. 176: `Enable/disable CDP ona specific interface.`
- s. 176: `Switch(config)#interface fastethernet 0/1`
- s. 176: `Switch(config-if)#cdp enable`
- s. 176: `Switch(config-if)#no cdp enable`
- s. 176: `Show cdp neighbors`
- s. 176: `Switchl#show cdp neighbors`
- s. 177: `Enable/disable LLDP on the device.`
- s. 177: `Switch(config)#lldp run`
- s. 177: `Switch(config)#no lldp run`
- s. 178: `Show Ildp neighbors`
- s. 178: `Switchl#show lldp neighbors`
- s. 179: `network load.`
- s. 179: `interface. This way of working is more efficient than storing logs in RAM.`
- s. 180: `Logging Buffer - A Logging Buffer is a predetermined storage space allocated on RAM`
- s. 180: `network (such as when the status of a device changes, login attempts, etc.).`
- s. 182: `Logging host [IP address] Sets the log server.`
- s. 182: `Logging trap`
- s. 182: `Service timestamps lo`
- s. 182: `Logging console of the console connection (enabled by`
- s. 182: `Login buffered ” B`
- s. 183: `R1(config)#logging host 172.16.0.250`
- s. 183: `R1(config)#logging trap debugging`
- s. 183: `R1(config)#logging userinfo`
- s. 183: `R1(config)#service timestamps log datetime msec`
- s. 183: `R1(config)#do show logging`
- s. 184: `Clear Log`
- s. 185: `NTP (Network Time Protocol) is responsible for the synchronization of all clocks in`
- s. 185: `NTP is a client-server protocol. All clients must be configured with the NTP server's IP`
- s. 185: `NTP operates with UDP, on port 123, and is defined in RFC 1305.`
- s. 186: `Router#clock set hh:mm:ss Day<1-31> Month<January-December> Year<1993-2035>`
- s. 186: `Router>enable`
- s. 186: `Router#clock set 09:21:14 16 January 2019`
- s. 186: `Router(config)#ntp server <ip_address>`
- s. 186: `Router#configure terminal`
- s. 186: `Router(config)#ntp server 172.30.226.100`
- s. 187: `Router(config)#ntp master <1-15>`
- s. 187: `Router(config)#ntp master`
- s. 187: `Logging Alerts with Time`
- s. 187: `Logging alerts with time included.`
- s. 187: `Router(config)#service timestamps log datatime msec`
- s. 187: `Router(config)#service timestamps log datetime msec`
- s. 188: `Network Performance - Network performance can be improved by allowing only`
- s. 191: `Router(config)# i access-list <access-list-number> | <deny | permit |remark>i <source-address>! <source-wildcard>`
- s. 191: `R1(config)# access-list 10 permit 192.168.10.0 @.0.0.255`
- s. 192: `network 192.168.0.0/24`
- s. 192: `interface in the outbound direction.`
- s. 193: `R1(config)#access-list 1 deny 10.0.0.0 @.0.0.255`
- s. 193: `R1(config)#access-list 1 permit any`
- s. 193: `R1(config)# interface Gigabitethernet 0/3`
- s. 193: `R1(config-if)#ip access-group 1 out`
- s. 193: `R1(config)# ip access-list standard`
- s. 193: `R1(config-std-nacl)#deny host 192.168.0.10`
- s. 193: `R1(config-std-nacl)#permit any`
- s. 193: `R1(config-std-nacl)#exit`
- s. 193: `R1(config)#interface Gigabitethernet 0/2`
- s. 193: `R1(config-if)#ip access-group out`
- s. 194: `R2#`
- s. 194: `R1#`
- s. 194: `interface GigabitEthernet0/2`
- s. 194: `ip address 10.0.0.15@ 255.255.255.0`
- s. 194: `ip access-group Block__Host_A out`
- s. 194: `interface GigabitEthernet0/3`
- s. 194: `ip address 172.16.0.15@ 255.255.255.080`
- s. 194: `ip access-group 1 out`
- s. 195: `Configure Extended ACLs as close as possible to the source of the traffic being filtered.`
- s. 196: `Router(config)#access-list <access-list-number> <deny|permit|remark>`
- s. 196: `R1(config)#access-list 180 deny tcp 192.168.10.1 0.0.0.255 192.168.10.2`
- s. 196: `R1(config)#access-list 181 permit tcp 192.168.10.0 @.0.0.255 any eq www`
- s. 196: `R1(config)#interface f0/0`
- s. 196: `R1(config-if)#ip access-group 18@ out`
- s. 196: `R1(config-if)#ip access-group 181 in`
- s. 196: `R1(config)#ip access-list extended <name>`
- s. 196: `R1(config-ext-nac1)# <deny|permit|remark> <Protocol> <source-address>`
- s. 196: `R1(config)# ip access-list extended WEB`
- s. 196: `R1(config)# permit tcp 192.168.10.0 @.0.0.255 any eq 443`
- s. 196: `R1(config)# permit tcp 192.168.10.@ @.0.0.255 192.168.11.1 @.0.0.255 eq`
- s. 196: `R1(config)#interface f0/e`
- s. 196: `R1(config)# ip access-group WEB`
- s. 197: `configured Numbered and Named ACLs.`
- s. 197: `Rl#show access-lists`
- s. 198: `interface in the inbound direction.`
- s. 198: `R1(config)#access-list 100 deny ip host 192.168.0.1@ host 10.0.0.20`
- s. 198: `R1(config)#access-list 100 permit ip any any`
- s. 198: `R1(config)#interface gigabitEthernet 0/1`
- s. 198: `R1(config-if)#ip access-group 100 in`
- s. 199: `R1(config)#ip access-list extended`
- s. 199: `R1(config-ext-nacl)#deny tcp 10.0.0.0 @.0.0.255 host 172.16.1.2 eq 21`
- s. 199: `R1(config-ext-nacl)#deny tcp 10.0.0.0 0.0.0.255 host 172.16.1.2 eq 20`
- s. 199: `R1(config-ext-nacl)#permit ip any any`
- s. 199: `R1(config-ext-nacl)#exit`
- s. 199: `R1(config)#interface gigabitEthernet 0/2`
- s. 199: `R1(config-if)#ip access-group in`
- s. 199: `R1i#`
- s. 199: `interface GigabitEthernet0/1`
- s. 199: `ip address 192.168.0.15@ 255.255.255.0`
- s. 199: `ip access-group 100 in`
- s. 199: `ip access-group Block_FTP in`
- s. 201: `Network administrators will often be responsible for assigning static IP addresses to`
- s. 201: `network components, such as routers, servers, firewalls, etc.`
- s. 201: `network. A DHCP server is configured with a range of IP addresses, which it allocates to`
- s. 204: `Router Server`
- s. 204: `router. server to act as the DHCP server.`
- s. 205: `R1(config)#ip dhcp excluded-address 192.168.0.1`
- s. 205: `R1(config)#ip dhcp excluded-address 192.168.0.100 192.168.0.150`
- s. 205: `R1(config)#ip dhcp pool LAN1`
- s. 205: `R1(dhcp-config)#network 192.168.0.0 255.255.255.0`
- s. 205: `R1(dhcp-config)#default-router 192.168.0.1`
- s. 205: `R1(dhcp-config)#dns-server 192.168.0.105`
- s. 205: `R1(dhcp-config)#domain-name Cyber.com`
- s. 205: `R1(dhcp-config)#lease ® 4 30`
- s. 205: `R1(dhcp-config)#exit`
- s. 205: `Show ip dhcp pool - Displays pool settings.`
- s. 205: `Show ip dhcp binding - Displays the client list, with IP, MAC address, and lease`
- s. 205: `Show ip dhcp conflict - Displays IP conflicts detected during DHCP negotiation.`
- s. 206: `R1#show ip dhcp pool`
- s. 206: `ip dhcp excluded-address command.`
- s. 206: `Configure specific tasks like default-router and DNS-server. Tasks such as default-router`
- s. 206: `Router(config)#ip dhcp excluded-address 192.168.0.1`
- s. 206: `Router(config)#ip dhcp pool poolone`
- s. 206: `Router(dhcp-config)#network 192.168.0.0 255.255.255.0`
- s. 206: `Router (dhcp-config)#default-router 192.168.0.1`
- s. 206: `Router (dhcp-config)#dns-server 192.168.0.1`
- s. 206: `Router(dhcp-config)#domain local.host`
- s. 206: `Router (dhcp-config)#end`
- s. 207: `Router(config)#interface ge/e`
- s. 207: `Router(config-if)# ip helper-address 192.168.11.6`
- s. 207: `Router (config-if)#`
- s. 208: `Network Address Translation (NAT) is an essential protocol and service that converts a`
- s. 208: `network (LAN). Their usage is unlimited and they can be implemented freely.`
- s. 208: `IP Subnet`
- s. 209: `Network flexibility and connection Difficult to troubleshoot issues`
- s. 211: `interface connected to the internet is defined as outside.`
- s. 211: `Edge-R1(config)#interface gigabitEthernet 0/@`
- s. 211: `Edge-R1(config-if)#ip add 10.0.0.1 255.255.255.0`
- s. 211: `Edge-R1(config-if)#ip nat inside`
- s. 211: `Edge-R1(config-if)#no shutdown`
- s. 211: `Edge-R1(config-if)#exit`
- s. 211: `Edge-R1(config)#interface serial 0/0/08`
- s. 211: `Edge-R1(config-if)#ip add 209.15.10.1 255.255.255.0`
- s. 211: `Edge-R1(config-if)#ip nat outside`
- s. 212: `ip nat inside source static <local-ip> <global-ip>`
- s. 212: `interface 209.15.10.1, and the router uses the NAT static map to forward the request to`
- s. 212: `Edge-R1(config)#ip nat inside source static 10.0.0.10 209.15.10.1`
- s. 212: `Edge-R1(config)# ip nat inside source static tcp 10.0.0.10 22 209.15.10.1`
- s. 212: `Edge-R1(config)#ip nat pool ToFreedom 209.15.10.1 209.15.10.1@ netmask`
- s. 212: `Edge-R1(config)#access-list 1 permit 10.0.0.0 0.0.0.255`
- s. 212: `Edge-R1(config)#ip nat inside source list 1 pool ToFreedom`
- s. 213: `Edge-R1(config)#ip nat pool ToFreedom 209.15.10.1 209.15.10.10 netmask`
- s. 213: `Edge-R1(config)#ip nat inside source list 1`
- s. 214: `Edge-Rl1#show ip nat statistics`
- s. 214: `access-list 1 pool ToFreedom refCount @`
- s. 214: `Edge-Ri1#show ip nat translations`

## Slides

- s. 3: `Network Types and Devices`
- s. 4: `NETWORK TYPES AND DEVICES`
- s. 7: `Network Center`
- s. 8: `Network Structure`
- s. 8: `Network Requirements`
- s. 11: `network it must have the 2 Rass,`
- s. 11: `network. » ok`
- s. 18: `Router`
- s. 18: `route information among`
- s. 19: `network wirelessly and threats that originate from multiple APs to be managed intermediary devices`
- s. 20: `NETWORK MEDIA AND CABLES`
- s. 21: `Network Media and Cables`
- s. 28: `NETWORK TOPOLOGIES AND ARCHITECTURE`
- s. 29: `Network Topologies and Architecture`
- s. 29: `Network Topology`
- s. 31: `network.`
- s. 34: `network, while IP addresses are used to identify machines`
- s. 35: `network card. The address is static and should not be changed.`
- s. 36: `IPv6 was developed with six hexadecimal octets that can generate approximately 340x10‘36`
- s. 36: `IPv6 addresses have not yet been fully integrated in modern use cases.`
- s. 37: `network address and cannot be used for —_—— ———`
- s. 38: `NETWORK PROTOCOLS AND COMMANDS`
- s. 39: `Network Protocols and Commands`
- s. 41: `Network Commands`
- s. 42: `Ping X.X.X.X`
- s. 42: `C:\Windows\system32> ping 8.8.8.8`
- s. 42: `Ping is the most common`
- s. 42: `network. Reply from 8.8.8.8: bytes=32 time=103ms TTL=54`
- s. 43: `ipconfig`
- s. 43: `ipconfig displays a computer’s C:\Windows\system32> ipconfig`
- s. 43: `IP configuration.`
- s. 43: `IP address. Default Gateway. ........ : 192.168.5.1`
- s. 44: `nslookup x.x.X.X`
- s. 45: `tracert xX.X.X.X`
- s. 45: `C:\Windows\system32> tracert 8.8.8.8`
- s. 45: `name or an IP address. 12. 188 ms 230 ms 326 ms 74.125.37.167`
- s. 46: `Netsh [ command \ option ]`
- s. 46: `C:\Windows\system32> netsh interface ip show config`
- s. 59: `Network Fundamentals`
- s. 59: `ARP and Encapsulation`
- s. 60: `NETWORK PROTOCOLS AND MODELS`
- s. 62: `Network Protocols and Models`
- s. 64: `configured to use DHCP, such as Forexamplewhenan Envail ig commands ona remote messages when IP packets are`
- s. 64: `SSH on port 22.`
- s. 65: `Network Model Concept`
- s. 69: `Transport, Network, Datalink, Physical. PRESENTATION PRESENTATION`
- s. 69: `TRANSPORT TRANSPORT`
- s. 74: `Transport TCP, UDP, RTP, SCTP`
- s. 74: `Network IPv4, IPv6, ICMPv4, ICMPv6, IPX`
- s. 76: `Encapsulation`
- s. 77: `encapsulation. The envelope is written in a format the mail service`
- s. 78: `Encapsulation in Layers 4-7`
- s. 81: `network devices on the Internet.`
- s. 82: `Network Access Physical Layer Network Access`
- s. 87: `TRANSPORT PROTOCOLS AND LOGICAL PORTS`
- s. 88: `Transport Protocols and Logical Ports`
- s. 88: `Transport Protocols`
- s. 99: `C:\WINDOWS\system32>netstat -ab`
- s. 112: `Network Examination with Wireshark and how computers encapsulate and send data.`
- s. 113: `ARP`
- s. 114: `ARP operates in Layers 2 and 3 of the OSI model.`
- s. 116: `arp -a`
- s. 116: `arp —a and arp -g display the 224.0.0.251 Q@1-00-5e-00-00-fb static`
- s. 116: `SHOW amp dsplayea Chea deus 239.255.255.250 01-00-5e-7f-ff-fa static`
- s. 116: `ARP table. 255.255.255.255 F¥-FF-FF-FF-FF-FF static`
- s. 117: `C:\Windows\system32>arp -d`
- s. 117: `arp —d deletes the host ARP`
- s. 117: `arp —s adds a static entry to`
- s. 117: `arp inet_addr — defines a`
- s. 117: `arp eth_addr - defines a`
- s. 126: `show mac address-table ee ee`
- s. 135: `interface with it using text-based Cisco commands.`
- s. 140: `network deployment experience.`
- s. 142: `network. —`
- s. 145: `# viewing commands (show commands). It also enables file management operations,`
- s. 146: `Interface Configuration Mode`
- s. 146: `router.`
- s. 147: `Switch(config)#exit`
- s. 148: `Switch>di`
- s. 153: `hostname <device name>`
- s. 153: `Switch(config)#hostname S1-Floor1`
- s. 153: `S1-Floor1(config)#`
- s. 154: `username <user-name> password <password>`
- s. 154: `Switch(config)#username Admin password p@nd@`
- s. 154: `Switch(config)#username Peter password Spiderm@n`
- s. 155: `enable password <password>`
- s. 155: `Switch(config)#enable password c!sc@`
- s. 156: `banner motd #security-message#`
- s. 156: `Switch(config)#banner motd #Access to this device is for authorized personnel only!#`
- s. 157: `service password-encryption`
- s. 157: `Switch(config)#service password-encryption`
- s. 158: `copy running-config startup-config`
- s. 158: `Switch#copy running-config startup-config`
- s. 159: `line console 0 & login local`
- s. 160: `line con @`
- s. 160: `line aux @`
- s. 160: `Line vty @ 4`
- s. 160: `login`
- s. 164: `copy running-config tftp`
- s. 164: `Switch#copy running-config tftp:`
- s. 166: `R1(config)# exit`
- s. 168: `Router(config)# config-register 0x2102`
- s. 168: `Router(config)# end`
- s. 168: `Router# Reload`
- s. 170: `Router#show version`
- s. 170: `configured register value.`
- s. 180: `Shutdown`
- s. 182: `Switch# show interfaces`
- s. 182: `shutdown mode violation.`
- s. 185: `Switchport mode access`
- s. 185: `switchport port-security`
- s. 185: `Switch(config-if)#`
- s. 186: `switchport port-security [configuration] [value]`
- s. 186: `Switch(config-if)# switchport port-security mac-address sticky`
- s. 187: `Switch# show port-security`
- s. 187: `Vlan Mac Address Type Ports Remaining Age`
- s. 188: `Configure and Verify Port Security ona switch, pigetes using Port Security options, and learn`
- s. 191: `SSH`
- s. 192: `SSH Encryption`
- s. 194: `CLEAR toro! CLEAR`
- s. 197: `VLAN, a corresponding Layer 3 interface needs to be created on the`
- s. 198: `SSH Configuration`
- s. 199: `Switch(config)#hostname S1`
- s. 199: `S1(config)#username Admin password p@nd@`
- s. 199: `configured before enabling SSH : : F`
- s. 199: `S1(config)#banner motd #Access to this device is for authorized`
- s. 200: `line vty <id-range> & login local`
- s. 200: `S1(config-line)#transport input ssh`
- s. 201: `interface vlan 1`
- s. 201: `ip address <ip-address> <subnet-mask>`
- s. 201: `S1(config)#interface vlan 1`
- s. 201: `S1(config-if)#ip address 10.0.0.150@ 255.255.255.0`
- s. 201: `S1(config-if)#no shutdown`
- s. 201: `S1(config-if)#exit`
- s. 201: `S1(config)#ip default-gateway 10.0.0.1`
- s. 202: `crypto key generate rsa`
- s. 202: `router needs those keys to secure`
- s. 203: `S1#show ssh`
- s. 203: `Username`
- s. 203: `Show ip ssh displays the version oe`
- s. 203: `S1#show ip ssh`
- s. 203: `SSH Enabled - version 2.0`
- s. 204: `ssh -1 <username> <target-ip>`
- s. 211: `IP & Routing Concepts`
- s. 224: `# area network, prot ‘prov | COMMUNES ION`
- s. 224: `configured, the gateway should`
- s. 227: `Router interfacesneedito be R1(config)#interface gigabitEthernet @/@`
- s. 229: `configured Suring tne.inttis %LINK-5-CHANGED: Interface Loopback®, changed state to up`
- s. 229: `router configuration, mainly 6 .`
- s. 229: `Router(config-if)# exit`
- s. 229: `interface must have a unique IP.`
- s. 234: `Router# show ip route`
- s. 234: `network destinations. E1 - OSPF external type 1, E2 - OSPF external type 2, E - EGP`
- s. 234: `route show how the network is ) 172.16.0.0/16 [90/5376] via 192.168.4.2, 00:02:24, GigabitEthernet4/o`
- s. 242: `network segment, which is the reason why routers do not forward`
- s. 244: `IP addresses are typically divided into two groups: private and public.`
- s. 248: `IPv6 was designed to solve the IPv4 address space limitation and`
- s. 249: `IPv6 addresses are long and difficult to read.`
- s. 250: `IPv6 Address Breakdown`
- s. 250: `IPv6 Address t`
- s. 250: `Router(config-if)#ipv6 address`
- s. 250: `network portion.`
- s. 251: `Router(config)#ipv6 unicast-routing`
- s. 251: `Router#show ipv6é interface brief`
- s. 251: `Configure IPv6 on the FE8@: :201:97FF:FE13:A801`
- s. 251: `router interface using the 2001: ABC: BB: :1`
- s. 253: `IPv6 Unicast Types`
- s. 254: `IPv6 Address Example`
- s. 255: `IP versions to coexist.`
- s. 261: `Network Address Scheme Design`
- s. 263: `network facilitates faster packet delivery and adds filtration by minimizing`
- s. 272: `Network Portion Host Portion`
- s. 274: `Network Address Usable IP Addresses Broadcast Address`
- s. 278: `Network Configuration Per User`
- s. 285: `NETWORK ADDRESS SCHEME DESIGN`
- s. 286: `Network Planning`
- s. 288: `configured with static configured with static`
- s. 293: `Router Operation`
- s. 293: `IPv6 Static Routing`
- s. 294: `ROUTER OPERATION`
- s. 299: `No CPU and memory usage for routing purposes. Configuration and maintenance are time-consuming.`
- s. 300: `Network administrators decide if and when to use Static Routing, based on network requirements.`
- s. 303: `Network Topology Illustration`
- s. 303: `network B.`
- s. 304: `Router (config)# ip route <network-address> <subnet-mask> <direction>`
- s. 304: `R1(config)#ip route 10.1.0.0`
- s. 306: `R1(config)#ip route 0.0.0.0 0.0.0.0 gigabitEthernet 2/0`
- s. 310: `ip route <network-address> <subnet-mask> <direction> <AD>`
- s. 310: `route fails.`
- s. 311: `ip route <ip-address> 255.255.255.255 <direction>`
- s. 311: `route is not very common, it`
- s. 313: `Network Address :`
- s. 314: `ip route <summarize-address> <summarize-mask> <direction>`
- s. 314: `R1(config)#ip route 172.8.0.@ 255.248.0.0 10.0.0.1`
- s. 314: `R1(config)#do show ip route`
- s. 316: `IPV6 STATIC ROUTING`
- s. 317: `IPv6 Static Routes`
- s. 317: `IPv6 Static Route Types`
- s. 318: `IPv6 Prerequisites`
- s. 320: `R1(config)#ipv6 route 2001:abcd:cafe::/64 2002:abcd:aaaa::1`
- s. 320: `R1(config)#ipv6é route serial 0/0/0`
- s. 321: `R1(config)#do show ipv6 route`
- s. 330: `route was manually route was learned route was learned route was learned`
- s. 331: `route to each network.`
- s. 337: `Network Map`
- s. 337: `Network Changes`
- s. 342: `route, which is 15. Due to its limitations, it is often implemented only in`
- s. 345: `route’s hop count to 16`
- s. 347: `Network Illustration`
- s. 348: `R1(config)#router rip`
- s. 348: `R1(config-router)#network 192.168.10.@`
- s. 348: `R1(config-router)#network 172.16.0.0`
- s. 348: `R1(config-router)#passive-interface gigabitEthernet 0/0`
- s. 348: `R2(config-router)#no auto-summary`
- s. 349: `Ri#show ip route`
- s. 351: `Ri#show ip protocols`
- s. 352: `Show IP Route Output`
- s. 352: `# ROULS'SOULCe: R 192.168.20.0/24 [120/1] via`
- s. 353: `R2(config)#do show ip route`
- s. 362: `Router ID Configuration`
- s. 362: `Router ID -`
- s. 367: `router ig sets the TOMTEPOSEF R1(config-router)#network 192.168.10.@ @.0.0.255 area @`
- s. 367: `R1(config-router)#network 172.16.0.0 0.0.0.3 area @`
- s. 367: `R1(config-router)#network 172.16.0.8 0.0.0.3 area @`
- s. 367: `network interface.`
- s. 377: `VLAN is acommon concept and practice among network administrators.`
- s. 377: `VLAN is a Layer 2 feature that allows virtual network segmentation,`
- s. 378: `VLAN, creating a logical barrier between end devices connected to`
- s. 382: `show vlan brief`
- s. 382: `S1#show vlan brief`
- s. 383: `Switchport Modes`
- s. 384: `vlan <id>`
- s. 384: `name <word>`
- s. 384: `VLAN 100 and 200 creation, whereby S1(config-vlan)#name class A`
- s. 384: `S1(config-vlan)#name class B`
- s. 385: `switchport mode access`
- s. 385: `switchport access vlan <id>`
- s. 385: `S1(config)#interface range fastEthernet 0/1-2`
- s. 385: `S1(config)#interface range fastEthernet 0/3-4`
- s. 385: `VLAN simultaneously can be done S1(config-if)#switchport access vlan 200`
- s. 386: `Si#show vlan brief`
- s. 386: `VLAN Name Status Ports`
- s. 387: `switchport voice vlan <id>`
- s. 387: `network are necessary, but are`
- s. 391: `Si(config)#interface gigabitEthernet 0/1`
- s. 391: `S1(config-if)#`
- s. 391: `S2(config-if)#`
- s. 391: `S2(config-if)#exit`
- s. 394: `switchport mode dynamic <mode>`
- s. 394: `S1(config)#interface gigabitEthernet 0/1`
- s. 395: `switchport nonegotiate`
- s. 399: `switchport trunk native vlan <id>`
- s. 399: `S2(config)#interface gigabitEthernet 0/1`
- s. 399: `S1#show interfaces trunk`
- s. 399: `S2#show interfaces trunk`
- s. 402: `Router-On-A-stick`
- s. 402: `Router-On-A-Stick.`
- s. 403: `router’s single physical interface is segmented into`
- s. 404: `Switchport mode trunk`
- s. 404: `S1(config-if)#switchport mode trunk`
- s. 405: `R1(config)#interface gigabitEthernet`
- s. 405: `encapsulation on 802.1q and R1(config-subif)#exit`
- s. 405: `R1(config-subif)#encapsulation dot1Q`
- s. 406: `Ri#show ip interface brief`
- s. 406: `Interface IP-Address OK? Method Status`
- s. 417: `Network . .`
- s. 419: `Network Management Software (NMS) provides excellent tools for`
- s. 420: `show ip interface brief show running-config show startup-config`
- s. 420: `show interfaces show ip route verifies show ip interface show running-config show startup-config`
- s. 420: `interface errors, — operating as they with the IP protocol. that time. when it loads.`
- s. 421: `ping`
- s. 421: `network connectivity. It is also able to change the source Target IP address:`
- s. 421: `IP on the packet leaving the router. Repeat count [5]:`
- s. 421: `Traceroute Sending 6, ) ICMP Echos to`
- s. 424: `network and more. the neighbor table.`
- s. 427: `S1#show cdp`
- s. 428: `S1(config-if-range)#cdp enable`
- s. 429: `S1#`
- s. 431: `Si#show lldp`
- s. 432: `S1(config)#interface range fastEthernet @/1-24`
- s. 432: `S1(config-if-range)#no lldp receive`
- s. 433: `show commands but can display additional SF, — ,`
- s. 442: `Enable GigO/1 Log`
- s. 443: `logging host Sets the destination syslog server`
- s. 443: `logging trap Determines what log severity levels to send to the server`
- s. 443: `logging console Shows system messages on the screen of the console connection (enabled by default)`
- s. 443: `login buffered Saves system messages to the RAM (enabled by default) FEE`
- s. 444: `R1(config)#logging host 172.16.0.250`
- s. 444: `R1(config)#logging trap debugging`
- s. 444: `R1(config)#do show logging`
- s. 445: `Network Time Protocol`
- s. 446: `NTP Overview`
- s. 446: `NTP (Network Time Protocol) is responsible for the synchronization of`
- s. 446: `NTP is a simple client-server protocol and is implemented in networks`
- s. 446: `NTP operates on UDP port 123 and is defined in RFC 1305.`
- s. 448: `NTP Usage`
- s. 449: `clock set <hh:mm:ss> <day> <month-name> <year>`
- s. 450: `R1(config)#`
- s. 450: `R1(config)#interface gigabitEthernet 0/1`
- s. 451: `ntp master <1-15>`
- s. 451: `R1(config)#ntp master`
- s. 451: `R1(config)#do show run ntp`
- s. 452: `Configure NTP and Syslog | configure NTP and syslog servers.`
- s. 453: `# . ~<e "SEG fas f`
- s. 462: `Network Performance`
- s. 462: `Network performance can be improved by allowing only relevant services to`
- s. 471: `access-list i<access-list-number>} <deny | permit |remark> | <source-address> | <source-wildcard>|`
- s. 472: `Network Example`
- s. 472: `network 192.168.0.0/24 192.168.0.10/24 eee 10.0.0,10/24`
- s. 473: `R1(config)#access-list 1 deny 10.0.0.0 0.0.0.255`
- s. 473: `R1(config-if)#ip access-group 1 out`
- s. 474: `R1(config)# ip access-list standard`
- s. 474: `R1(config-std-nac1)#exit`
- s. 474: `interface using the`
- s. 475: `R2#`
- s. 475: `ip address 10.0.0.15@ 255.255.255.080`
- s. 475: `ip access-group Block__Host_A out`
- s. 475: `ip address 172.16.0.150 255.255.255.080`
- s. 475: `ip access-group 1 out`
- s. 479: `Configure Extended ACLs as close as possible to the source of the`
- s. 480: `access-list i<number> 1<action>:<protocol>! <source-address><destination-address>} <operator>`
- s. 480: `network 32-bit address. The any option can be used, and different 172.16.0.3 eq 22`
- s. 482: `R1(config)#access-list 100 deny ip host 192.168.0.10 host 10.0.0.20`
- s. 482: `R1(config-if)#ip access-group 10@ in`
- s. 482: `R1(config-if)#exit`
- s. 483: `R1(config)#ip access-list extended`
- s. 483: `R1(config-ext-nacl)#permit ip any any`
- s. 484: `interface each ACL is applied. Rit`
- s. 484: `interface GigabitEthernet@/1`
- s. 484: `interface GigabitEthernet0/2`
- s. 484: `ip access-group Block_FTP in`
- s. 489: `configure and implement DHCP.`
- s. 498: `Router vs. Server`
- s. 498: `Router Server`
- s. 502: `R1(dhcp-config)#domain-name Cyber.com`
- s. 503: `Ri#show ip dhcp pool`
- s. 504: `R1(config)#interface gigabitethernet 0/0`
- s. 504: `Enable the`
- s. 505: `R1(config)#ip address dhcp`
- s. 506: `Configure DHCPv4 on a Cisco Router | dynamically. The lab also promotes understanding of the DHCP`
- s. 508: `Network address translation (NAT) is an essential protocol and service`
- s. 508: `network is only possible through NAT.`
- s. 510: `IP Subnet`
- s. 513: `network viewed from the inside identification and access to viewed from the outside`
- s. 514: `IP (outside global) on the internet.`
- s. 516: `Network address translation IPv6 to IPv4 (NAT64) technology`
- s. 519: `Edge-R1(config-if)#no shutdown`
- s. 519: `Edge-R1(config-if)#`
- s. 520: `ip nat inside source static <local-ip> <global-ip>`
- s. 522: `Edge-R1(config)#ip nat pool ToFreedom 209.15.10.1 209.15.10.10`
- s. 523: `Edge-R1#show ip nat statistics`
- s. 523: `interface configuration. access-list 1 pool ToFreedom refCount @`

## Labs

- s. 2: `Configure a local network using CMD-based commands.`
- s. 4: `Copy the details marked in red in Step 2 above.`
- s. 6: `C:\Windows \system32>ping 1@.21.6.3`
- s. 6: `C:\Windows\system32>tracert 10.21.6.3`
- s. 7: `C:\Windows \system32>tracert 168.21.6.3`
- s. 7: `Ping an external source, such as a URL or public address (www.facebook.com, 8.8.8.8).`
- s. 8: `Ping statistics for 8.8.8.8:`
- s. 10: `C:\Windows \system32>ns lookup`
- s. 11: `Name: edge-star-mini-shv-@1-frx5,. facebook. com`
- s. 13: `netsh interface ip set address "Ethernet" static 192.168.10.5 255.255.255.0`
- s. 13: `netsh interface ip set address "Ethernet" dhcp`
- s. 13: `netsh interface set interface "Ethernet" admin=DISABLED`
- s. 13: `netsh interface set interface "Ethernet" admin=ENABLE`
- s. 23: `Show deta`
- s. 30: `C:\Users\User>`
- s. 31: `No iterns match your search. 192.168.6.36`
- s. 31: `Transport Layer Security`
- s. 31: `ipconfig /flushdns and repeat steps 3-8.`
- s. 40: `Show in folder |`
- s. 40: `Show more details`
- s. 43: `C:\Program Files\Cisco Packet Tracer 8,0`
- s. 45: `Username or Email`
- s. 53: `show commands).`
- s. 53: `name, user names, passwords, etc.).`
- s. 54: `Switch>?`
- s. 54: `enable Turn on privileged commands`
- s. 54: `exit Exit from the EXEC`
- s. 54: `ping Send echo messages`
- s. 54: `show Show running system information`
- s. 54: `traceroute Trace route to destination`
- s. 55: `clock appears not to be set because in this mode we do not have permission to`
- s. 55: `configure it.`
- s. 55: `Switch>show ?`
- s. 55: `arp Arp table`
- s. 55: `clock Display the system clock`
- s. 55: `crypto Encryption module`
- s. 55: `Switch>show clock`
- s. 56: `Switch>enable`
- s. 56: `Switch#`
- s. 57: `Switch#clock set ?`
- s. 57: `Switch#clock set 19:41:00 ?`
- s. 57: `Switch#clock set 19:41:00 14 september ?`
- s. 57: `Switch#clock set 19:41:00 14 september 2019 ?`
- s. 57: `Switch#clock set 19:41:00 14 september 2019`
- s. 57: `Switch#show clock`
- s. 57: `Switch#conf`
- s. 57: `Switch#configure ?`
- s. 57: `Switch#configure t`
- s. 57: `Switch#configure terminal`
- s. 57: `Switch(config)#`
- s. 58: `Switch(config)#hostname S1-Floor1`
- s. 58: `Username: Admin`
- s. 58: `S1-Floor1(config)#enable password c!sc@`
- s. 59: `S1-Floor1(config)#line console @`
- s. 59: `S1-Floor1#`
- s. 59: `no service timestamps log datetime msec`
- s. 59: `no service timestamps debug datetime msecno service password-encryption`
- s. 59: `enable password c!sc@`
- s. 60: `interface FastEthernet0/1`
- s. 60: `interface GigabitEthernet0/1`
- s. 60: `interface GigabitEthernet0/2`
- s. 60: `interface Vlan1`
- s. 60: `no ip address`
- s. 60: `shutdown`
- s. 60: `banner motd “CAccess to this device is for authorized personnel only!*C`
- s. 60: `line con @`
- s. 60: `login local`
- s. 60: `line vty 0 4`
- s. 60: `login`
- s. 60: `line vty 5 15`
- s. 62: `no service timestamps debug datetime msec`
- s. 62: `service password-encryption`
- s. 62: `hostname S1-Floor1`
- s. 62: `enable password 7 @822@D5D0A49`
- s. 62: `username Admin privilege 1 password 7 @8316C49@D39`
- s. 65: `Ping statistics for 10.0.0.2:`
- s. 66: `S1-Floorl#show interfaces fastEthernet 9/1`
- s. 66: `Encapsulation ARPA, loopback not set`
- s. 66: `ARP type: ARPA, ARP Timeout 04:00:00`
- s. 67: `S1-Floorl#show mac-address-table`
- s. 67: `Vlan Mac Address Type Ports`
- s. 69: `Exit and Logout`
- s. 69: `Exit`
- s. 77: `S1>enable`
- s. 77: `Si#configure terminal`
- s. 77: `S1(config)#username Admin password p@nd@`
- s. 77: `S1(config)#username Technician password ku@1l@`
- s. 77: `S1(config)#line console @`
- s. 77: `S1(config-line)#login local`
- s. 77: `S1(config-line)#exit`
- s. 78: `S1(config)#enable password c!sc@`
- s. 78: `S1(config)#service password-encryption`
- s. 78: `S1(config)#banner motd #Access to this device is for authorized personnel`
- s. 78: `S1(config)#no ip domain-lookup`
- s. 78: `Si#copy running-config startup-config`
- s. 79: `Sl#copy run`
- s. 79: `Sl#copy Sonningecorieig startup-config`
- s. 79: `S1#copy running-config tftp`
- s. 80: `Sl#copy running-config tftp`
- s. 80: `NTP 184 1.advineorirack9.m7 194.16 T4 hin`
- s. 81: `S1#show flash.`
- s. 81: `Si#copy flash tftp`
- s. 82: `Sl#copy flash tftp`
- s. 83: `Sl#show flash`
- s. 83: `IP address of the TFTP server. In the second option, insert the name of the image`
- s. 83: `Si#copy tftp flash`
- s. 83: `Sl#copy tftp flash`
- s. 84: `Ctrl#F6 to exit CLI focus Copy Paste`
- s. 84: `IS1(config)#boot system flash: /c2960-lanbasek9-mz.150-2.SE4.bin`
- s. 84: `Sl(config)#boot system flash: /c2960-lanbasek9-mz.150-2.SE4.bin`
- s. 84: `Sl#reload`
- s. 84: `S1#show version.`
- s. 86: `Configure and Verify`
- s. 90: `Enable port security and define the physical address and violation rule for each`
- s. 90: `interface. All the required commands were introduced in the presentation and can also`
- s. 91: `Ping statistics for 10.0.0.3:`
- s. 91: `C:\> igs`
- s. 91: `S1#show mac-address-table`
- s. 92: `S1(config)#interface range fastethernet @/1-4`
- s. 92: `S1(config-if-range)#switchport mode access`
- s. 92: `S1(config-if-range)#switchport port-security`
- s. 92: `S1(config-if-range)#exit`
- s. 92: `S1(config)#interface fastethernet Q/1`
- s. 92: `S1(config-if)#switchport port-security mac-address @@D@.9793.87C4`
- s. 92: `S1(config-if)# exit`
- s. 92: `S1(config)#interface fastethernet 0/2`
- s. 92: `S1(config-if)#switchport port-security mac-address 0009.7C96.0271`
- s. 92: `S1(config-if)#exit`
- s. 93: `S1(config)#interface fastethernet 0/3`
- s. 93: `S1(config-if)#switchport port-security mac-address sticky`
- s. 93: `S1(config)#interface fastethernet 0/4`
- s. 93: `S1(config-if)#switchport port-security violation shutdown`
- s. 93: `S1(config-if)#switchport port-security violation restrict`
- s. 93: `S1(config-if)#switchport port-security violation protect`
- s. 93: `S1(config-if)#switchport port-security maximum 2`
- s. 94: `S1(config)#interface range fastethernet @/5-24, gigabitethernet @/1-2`
- s. 94: `S1(config-if-range)#shutdown`
- s. 94: `Sl#copy running-config startup-config`
- s. 95: `S1#show port-security`
- s. 95: `Sl>enable`
- s. 95: `Sl#show port-security`
- s. 95: `Shutdown`
- s. 95: `sl# Vv`
- s. 95: `Sl#show running-config`
- s. 96: `interface FastEthernet0/2`
- s. 96: `switchport port-security violation rastrict`
- s. 96: `switchport port-security`
- s. 96: `switchport yort-security maximum 2`
- s. 96: `switchport port-security mac-address sticky 0004. 9A8B.2822`
- s. 96: `interface FastRthernet.0/4`
- s. 96: `switchport mode access`
- s. 96: `switchport port-security violation restrict`
- s. 96: `switchport port-security mac-address sticky 0008.##34.A1A0`
- s. 96: `Sil#show port-security address`
- s. 97: `Configured MAC Addresses + 0 A`
- s. 97: `Sil#show port-security interface type number`
- s. 97: `Sil#show port-security interface fastethernet 0/1`
- s. 97: `Configured MAC Addresses 5 al`
- s. 100: `Sl#show interface fastethernet 0/1`
- s. 100: `S1(config)#interface fastethernet @/1`
- s. 100: `S1(config-if)#shutdown`
- s. 100: `S1(config-if)#no shutdown`
- s. 101: `Sl#show interfaces fastEthernet 0/1`
- s. 103: `C:\>ping 10.0.0.1`
- s. 103: `Ping statistics tor 10.0.0.1:`
- s. 103: `Ping statistics for 10.0.0.1:`
- s. 104: `S1#show port-security interface fastethernet 0/2`
- s. 105: `C:\>ping 10.0.0.4`
- s. 106: `S1#show port-security interface fastethernet 0/3`
- s. 106: `Sl>show port-security intertace tastethernet 0/3`
- s. 106: `sl>enable`
- s. 106: `Sl#do show port-security interface fastethernet 0/3`
- s. 106: `Configured MAC Addresses: 0`
- s. 108: `Ping statistics for 10.0.0.3: e`
- s. 108: `c:\ping 10.0.0.4`
- s. 109: `S1#show port-security interface fastethernet 0/4`
- s. 109: `ping Joey and Monica again. You should notice that there are no issues with`
- s. 112: `network devices.`
- s. 117: `Switch(config)#hostname S1`
- s. 117: `S1(config)#`
- s. 117: `S1(config)#banner motd #Access to this device is for authorized personnel only!#`
- s. 117: `S1(config)#ip domain-name CyberPro.com`
- s. 117: `S1(config)#interface vlan 1`
- s. 117: `S1(config-if)#ip address 10.0.0.15@ 255.255.255.0`
- s. 117: `S1(config)#ip default-gateway 10.0.0.1`
- s. 118: `C:\>ping 10.0.0.150`
- s. 118: `Ping statistics for 10.0.0.150:`
- s. 118: `S1(config)#line vty @ 15`
- s. 118: `S1(config-line)#`
- s. 118: `S1(config-line)# login local`
- s. 118: `S1(config-line)# motd-banner`
- s. 119: `S1(config-line)# transport input ssh`
- s. 119: `S1(config-line)# exit`
- s. 119: `S1(config)#crypto key generate rsa`
- s. 119: `Sl(config)#crypto key generate rsa`
- s. 119: `S1(config)#ip ssh version 2`
- s. 119: `S1(config)#exit`
- s. 121: `hostname 51`
- s. 121: `enable password 7 08220D5D0A49`
- s. 121: `ip domain-name Cyberpro.com`
- s. 121: `username Admin privilege 1 password 7 08316C400D39`
- s. 121: `interface Vlanl`
- s. 121: `ip default-gateway 10.0.0.1`
- s. 121: `banner motd “CAccess to this device is for authorized personnel`
- s. 121: `line con 0`
- s. 121: `transport input ssh`
- s. 123: `ssh -] <username><target-ip>`
- s. 123: `C:\>ssh -1 Admin 10.0.0.150`
- s. 123: `S1#`
- s. 123: `C:\>ssh -1 Admin 10.0.0.1`
- s. 123: `R1>enable`
- s. 123: `R1l#`
- s. 136: `Router>enable`
- s. 136: `Router#configure terminal`
- s. 136: `Router (config)#hostname R1`
- s. 136: `R1(config)#`
- s. 136: `R1(config)#username Admin password p@nd@`
- s. 136: `R1(config)#enable password c!sc®`
- s. 137: `R1(config)#banner motd #Access to this device is for authorized personnel`
- s. 137: `R1(config)#service password-encryption`
- s. 137: `R1(config)#line console @`
- s. 137: `R1(config-line)#login local`
- s. 137: `R1(config-line)#exit`
- s. 137: `R1(config)#exit`
- s. 137: `Rl#show running-config`
- s. 137: `Rl#copy running-config startup-config`
- s. 139: `Rl#configure terminal`
- s. 139: `configure the appropriate subnet mask: 255.255.255.0. Then enable the`
- s. 139: `interface.`
- s. 139: `R1(config)#interface gigabitethernet 0/0`
- s. 139: `R1(config-if)#ip address 192.168.0.1 255.255.255.080`
- s. 139: `R1(config-if)#no shutdown`
- s. 139: `R1(config-if)#exit`
- s. 139: `R1l(config)#interface gigabitethernet 0/1`
- s. 139: `R1(config-if)#ip address 10.0.0.1 255.255.255.0`
- s. 140: `R1(config)#do show ip interface brief`
- s. 141: `router's interface connected to the same network.`
- s. 142: `IP Aahess 20902`
- s. 143: `c:\>ipconfig`
- s. 144: `IP Addvoss [to0.02`
- s. 144: `C:\>ipconfig`
- s. 145: `Ping statistics for 192.168.0.1:`
- s. 145: `c:\ ping 16.0.0.2`
- s. 145: `Ping 192.168.0.3`
- s. 145: `Ping 10.0.0.3`
- s. 145: `Ping 10.0.0.2`
- s. 146: `C:\>ping 8.8.8.8`
- s. 146: `Ping statistics for §.8.8.8:`
- s. 146: `Csi>`
- s. 146: `S1#configure terminal`
- s. 146: `S1(config-if)#`
- s. 146: `S1(config-if)#ip address 192.168.0.4 255.255.255.080`
- s. 147: `Sl(config)#ip default-gateway 192.168.0.1`
- s. 147: `S1(config)#ip default-gateway 192.168.0.1`
- s. 147: `S1#ping 192.168.0.1`
- s. 147: `Sl#ping 192.168.0.1`
- s. 147: `S2(config-if)#ip address 10.0.0.4 255.255.255.080`
- s. 147: `S2(config-if)#no shutdown`
- s. 147: `S2(config)#ip default-gateway 10.0.0.1`
- s. 149: `Configure a router to connect two LANs using IPv6 addresses, then use troubleshooting`
- s. 152: `IPv6 Unicast types:`
- s. 153: `Rl#config terminal`
- s. 153: `R1(config)#ipv6 unicast-routing`
- s. 153: `R1(config-if)#ipv6é address 2001:cafe:abcd:1::/64`
- s. 154: `network (2001:CAFE:ABCD:2::), also using suffix 64.`
- s. 154: `R1(config-if)#ipv6 address 2001:cafe:abcd:2::/64`
- s. 154: `R1(config)#interface range gigabitethernet 0/0-1`
- s. 154: `R1(config-if-range)#no shutdown`
- s. 154: `R1(config-if-range)#exit`
- s. 154: `Rl#show ipv6 interface brief`
- s. 154: `R1#| nd`
- s. 155: `IP Corfgaton`
- s. 155: `configure the appropriate default gateway address.`
- s. 155: `IPV6 Configuration`
- s. 156: `IP Akiess EC`
- s. 156: `Ping statistics for 2001:CAFE:ABCD:1:::`
- s. 156: `c:\>ping 2001:cafe:abed:1::2`
- s. 156: `Ping statistics for 2001:CAFE:ABCD:1::2:`
- s. 157: `c:\>ping 2001:cafe:abcd:23:`
- s. 157: `ping statistics for 2001:CAFE:ABCD:2:::`
- s. 158: `R1(config-if)#ipv6 address fe8@::1 link-local`
- s. 158: `Rl#show ipv6é interface brief`
- s. 159: `IPv6 Configuration`
- s. 159: `IPv6 Address [2001:CAFE-ABCD:2::1 | 1 [64 ]`
- s. 159: `IPv6 Gateway '2001:CAFE:ABCD:2: |`
- s. 159: `IPv6 DNS Server`
- s. 159: `IPv6 Gateway |2001:CAFE:ABCD:2:`
- s. 159: `Ping statistics for FE80::1:`
- s. 160: `Ping statistics for FE80::3:`
- s. 160: `C:\sping feg0::3`
- s. 160: `Ping statistics for FE8Q::3:`
- s. 163: `IP address suffix?`
- s. 164: `network includes 45 hosts. How should this be done?`
- s. 165: `Network Address Usable Address`
- s. 173: `network.`
- s. 173: `router CPU, and no dynamic updates means no extra bandwidth is being used.`
- s. 174: `network using different routing methods.`
- s. 174: `Rl#show ip route`
- s. 174: `Ping statistics for 192.168.0.66:`
- s. 175: `Bi> Ts`
- s. 175: `Ri>enable`
- s. 175: `R1# show ip route`
- s. 176: `Ri#config terminal`
- s. 176: `R1(config)#ip route 192.168.0.64 255.255.255.192 serial 0/0/0`
- s. 176: `R1(config)#ip route 192.168.0.128 255.255.255.192 serial 0/0/0`
- s. 176: `R1(config)#ip route 192.168.0.196 255.255.255.252 serial 0/0/®`
- s. 177: `Rl#show ip route static`
- s. 177: `Rl# heat`
- s. 177: `R2>enable`
- s. 177: `R2>conf t`
- s. 177: `R2(config)#ip route 192.168.0.@ 255.255.255.192 192.168.0.193`
- s. 177: `R2(config)#ip route 192.168.0.128 255.255.255.192 192.168.0.198`
- s. 177: `R2(config)#exit`
- s. 178: `R2#show ip route static`
- s. 178: `R2# ng`
- s. 178: `R3>enable`
- s. 178: `R3#conf t`
- s. 178: `R3(config)#ip route 192.168.0.@ 255.255.255.192 serial @/0/1`
- s. 178: `R3(config)#ip route 192.168.0.64 255.255.255.192 serial @/0/1`
- s. 178: `R3(config)#ip route 192.168.0.192 255.255.255.252 serial 0/@/1`
- s. 178: `R3(config)#exit`
- s. 178: `R3(config)#ip route 192.168.0.64 255.255.255.192 serial 0/0/1`
- s. 178: `interface, may impact performance`
- s. 178: `R3(config)#ip route 192.168.0.0 255.255.255.192 serial 0/0/1`
- s. 178: `R3(config)#ip route 192.168.0.192 255.255.255.252 serial 0/0/1`
- s. 178: `R3#show ip route static`
- s. 178: `R3#| w`
- s. 179: `C:\>ping 152.168.0.66`
- s. 179: `C:\>tracert 192.168.0.66`
- s. 180: `network traffic.`
- s. 180: `Rl#show ip route tal`
- s. 181: `R1#conf t`
- s. 181: `R1(config)#ip route 0.0.0.0 0.0.0.® serial 0/0/20`
- s. 181: `Rl#show ip route a`
- s. 182: `R2#conf t`
- s. 182: `R2(config)#ip route 0.0.0.0 0.0.0.0 serial 0/1/0`
- s. 182: `R2(config)#do show ip route static`
- s. 182: `R3(config)#ip route 0.0.0.0 0.0.0.0 serial 0/0/1`
- s. 182: `R3(config)#do show ip route static`
- s. 182: `interface, mg DDS, perform =`
- s. 183: `C:\>tracert 8.8.8.8`
- s. 184: `interface configured for all. The network partition and interface are identical. This`
- s. 184: `R1(config)#do show ip route static`
- s. 184: `R1(config)#no ip route 192.168.0.64 255.255.255.192 serial 0/0/®`
- s. 184: `R1(config)#no ip route 192.168.0.128 255.255.255.192 serial 0/0/20`
- s. 184: `R1(config)#no ip route 192.168.0.196 255.255.255.252 serial 0/0/0`
- s. 184: `Ri(config)#nqj ap routef192.168.0.64 §55.255.255.1929 serial 0/0/0`
- s. 184: `Ri(config)#noj ip routef[192.168.0.196§255.255.255.25§ serial 0/0/0`
- s. 185: `network address. The matching bits with zeros at the end result in the`
- s. 185: `R1(config)#ip route 192.168.0.@ 255.255.255.@ serial 0/0/0`
- s. 186: `C:\>ping 192.168.0.66`
- s. 188: `Configure RIPv2 to connect all networks, and use it to propagate the network with a`
- s. 192: `Configure RIPv2 so that all networks are connected, and verify the connectivity.`
- s. 192: `R1> enable`
- s. 192: `Ri#configure terminal`
- s. 192: `R1(config)#router rip`
- s. 192: `R1(config-router)#version 2`
- s. 192: `R1(config-router)#do show ip route connected`
- s. 192: `R1(config-router)#network 172.16.0.0`
- s. 192: `R1(config-router)#network 172.16.0.8`
- s. 192: `R1(config-router)#network 192.168.10.0`
- s. 192: `R1(config-router)#no auto-summary`
- s. 192: `R1(config-router)#passive-interface gigabitethernet 0/@`
- s. 192: `R1(config-router)#exit`
- s. 193: `Rl>enable`
- s. 193: `Rl#conf t`
- s. 193: `Rl#copy run start`
- s. 193: `R2> enable`
- s. 193: `R2#configure terminal`
- s. 193: `R2(config)#router rip`
- s. 193: `R2(config-router)#version 2`
- s. 193: `R2(config-router)#do show ip route connected`
- s. 193: `R2(config-router)#network 172.16.0.0`
- s. 193: `R2(config-router)#network 172.16.0.4`
- s. 193: `R2(config-router)#network 192.168.20.0`
- s. 193: `R2(config-router)#no auto-summary`
- s. 193: `R2(config-router)#passive-interface gigabitethernet 0/@`
- s. 193: `R2(config-router)#exit`
- s. 193: `R2#copy running-config startup-config`
- s. 194: `R3> enable`
- s. 194: `R3#configure terminal`
- s. 194: `R3(config)#router rip`
- s. 194: `R3(config-router)#version 2`
- s. 194: `R3(config-router)#do show ip route connected`
- s. 194: `R3(config-router)#network 172.16.0.4`
- s. 194: `R3(config-router)#network 172.16.0.8`
- s. 194: `R3(config-router)#network 192.168.30.0`
- s. 194: `R3(config-router)#network 210.10.10.0`
- s. 194: `R3(config-router)#no auto-summary`
- s. 194: `R3(config-router)#passive-interface gigabitethernet 0/0`
- s. 194: `R3(config-router)#exit`
- s. 194: `R3#copy running-config startup-config`
- s. 194: `Ro>enable im`
- s. 194: `R2#copy run start`
- s. 195: `R3>enable cS`
- s. 195: `R3#`
- s. 195: `R3#copy run start`
- s. 196: `Rl#show ip route rip`
- s. 196: `Rlf#show ip route rip`
- s. 196: `Rl#show ip protocols`
- s. 196: `Rl#`
- s. 196: `Interface Send Recv Triggered RIP Key-chain`
- s. 197: `R2#show ip route rip`
- s. 197: `R2#show ip protocols`
- s. 197: `R3#show ip route rip`
- s. 197: `R3#show ip protocols`
- s. 197: `R2>`
- s. 197: `R2>show ip route rip`
- s. 197: `R2>| ii`
- s. 197: `R2>show ip protocols`
- s. 197: `R2> id`
- s. 198: `R3>show ip route rip`
- s. 198: `R3> v`
- s. 198: `R3>show ip protocols o`
- s. 200: `R3#show ip route`
- s. 200: `R3>show ip route`
- s. 201: `R3(config)#ip route 0.0.0.0 0.0.0.0 serial 0/2/20`
- s. 201: `R2#show ip route`
- s. 202: `R3(config-router )#default-information originate`
- s. 202: `R3(config-router )#exit`
- s. 207: `RQ#configure terminal`
- s. 207: `RO(config-router)#router-id 1.1.1.0`
- s. 207: `RO(config-router)#network 192.168.0.0 @.0.0.255 area 0`
- s. 207: `RO(config-router)#network 172.16.0.0 0.0.0.3 area @`
- s. 207: `RO(config-router)#network 172.16.0.8 0.0.0.3 area @`
- s. 207: `RO(config-router)#auto-cost reference-bandwidth 1000`
- s. 207: `RO(config-router)#passive-interface gigabitEthernet 0/1`
- s. 207: `RO(config-router)#exit`
- s. 207: `RO(config)#exit`
- s. 207: `R1(config)#router ospf 1`
- s. 207: `R1(config-router)#router-id 1.1.1.1`
- s. 207: `R1(config-router)#network 192.168.1.@ @.0.0.255 area 0`
- s. 207: `R1(config-router)#network 172.16.0.4 0.0.0.3 area @`
- s. 207: `R1(config-router)#network 172.16.0.8 0.0.0.3 area @`
- s. 207: `R1(config-router)#auto-cost reference-bandwidth 1000`
- s. 207: `R1(config-router)#passive-interface gigabitEthernet 9/1`
- s. 208: `R2(config)#router ospf 1`
- s. 208: `R2(config-router)#router-id 1.1.1.2`
- s. 208: `R2(config-router)#network 192.168.2.@ @.0.0.255 area 0`
- s. 208: `R2(config-router)#network 172.16.0.4 0.0.0.3 area 0`
- s. 208: `R2(config-router)#network 172.16.0.0 0.0.0.3 area @`
- s. 208: `R2(config-router)#auto-cost reference-bandwidth 1000`
- s. 208: `R2(config-router)#passive-interface gigabitEthernet 0/1`
- s. 209: `R2(config)#ip route 0.0.0.0 0.0.0.0 gigabitEthernet 0/0`
- s. 209: `R2(config-router)#default-information originate`
- s. 209: `Ri#show ip route ospf`
- s. 209: `R2#show ip route ospf`
- s. 215: `network topologies to overlay the physical switched infrastructure. The technology`
- s. 216: `Configure a VLAN on all network devices and verify that the VLANs were properly`
- s. 216: `configured using various troubleshooting methods.`
- s. 216: `show vlan brief`
- s. 216: `S1#show vlan brief`
- s. 216: `VLAN Name Status Ports`
- s. 217: `S2>enable`
- s. 217: `S2#show vlan brief`
- s. 217: `Sl#configure terminal`
- s. 217: `S1(config)#vlan 10`
- s. 217: `S1(config-vlan)#name Workstation`
- s. 217: `S1(config-vlan)#exit`
- s. 217: `S1(config)#vlan 20`
- s. 217: `S1(config-vlan)#name Servers`
- s. 218: `S2#configure terminal`
- s. 218: `S2(config)#vlan 10`
- s. 218: `S2(config-vlan)#name Workstation`
- s. 218: `S2(config-vlan)#exit`
- s. 218: `S2(config)#vlan 20`
- s. 218: `S2(config-vlan)#name Servers`
- s. 218: `S1(config)#interface range fastethernet @/1-2`
- s. 218: `S1(config-if-range)#switchport access vlan 10`
- s. 218: `S1(config-if)# switchport mode access`
- s. 218: `S1(config-if)#switchport access vlan 20`
- s. 219: `S2(config)#interface range fastethernet @/1-4`
- s. 219: `S2(config-if-range)#switchport mode access`
- s. 219: `S2(config-if-range)#switchport access vlan 10`
- s. 219: `S2(config-if-range)#exit`
- s. 219: `S2(config)#interface range fastethernet @/5-6`
- s. 219: `S2(config-if-range)#switchport access vlan 20`
- s. 220: `S1(config)#do show vlan brief`
- s. 220: `S2(config)#do show vlan brief`
- s. 221: `IP Configuration`
- s. 222: `C:\>ping 10.0.0.2`
- s. 224: `S1(config)#interface gigabitethernet 0/1`
- s. 224: `S1(config-if)#switchport mode trunk`
- s. 224: `router,`
- s. 224: `S1(config)#interface gigabitethernet 0/2`
- s. 224: `S2(config)#interface gigabitethernet 0/1`
- s. 224: `S2(config-if)#switchport mode trunk`
- s. 224: `S2(config-if)#exit`
- s. 224: `S2(config)#exit`
- s. 225: `S1(config)#vlan 30`
- s. 225: `S1(config-vlan)#name Native`
- s. 225: `S2(config)#vlan 30`
- s. 225: `S2(config-vlan)#name Native`
- s. 225: `S1(config-if)#switchport trunk native vlan 30`
- s. 225: `S2(config-if)#switchport trunk native vlan 30`
- s. 226: `S1(config)#do show interface trunk`
- s. 226: `S2(config)#do show interface trunk`
- s. 227: `S2#copy running-config startup-config`
- s. 228: `C:\>ping 192.168.0.2`
- s. 228: `Ping statistics for 192.168.0.2:`
- s. 229: `configured.`
- s. 229: `Ril#configure terminal`
- s. 229: `R1(config)#interface gigabitethernet 0/0.10`
- s. 229: `R1(config-subif)#`
- s. 229: `R1(config-subif)#encapsulation dotiq 10`
- s. 229: `R1(config-subif)#ip address 10.0.0.254 255.255.255.0`
- s. 229: `R1(config-subif)#exit`
- s. 230: `R1(config)#interface gigabitethernet 0/0.20`
- s. 230: `R1(config-subif)#encapsulation dotiq 20`
- s. 230: `R1(config-subif)#ip address 192.168.0.254 255.255.255.0`
- s. 230: `show running-config commands.`
- s. 230: `R1(config)#do show running-config`
- s. 230: `Rl(config)#do show ip interface brief`
- s. 230: `Interface IP-Address OK? Method Status`
- s. 230: `R1# show running-config`
- s. 231: `interface GigabicEthernet0/0.10`
- s. 231: `encapsulation dot1Q 10`
- s. 231: `ip address 10.0.0.254 255.255.255.0`
- s. 231: `interface GigebitEtherncto/0.20`
- s. 231: `ip address 192.168.0.254 255.255.255.0`
- s. 231: `C:\>ping 192.168.0.1`
- s. 233: `Configure a syslog server and an NTP server to log events across the network.`
- s. 236: `NTP stands for Network Time Protocol and is used for clock synchronization among`
- s. 236: `network devices and computers. The server provides the time for other devices.`
- s. 237: `Configure a server with the syslog service to obtain network event logs.`
- s. 238: `R1> ping 192.168.0.10`
- s. 238: `R1#configure terminal`
- s. 238: `R1(config)#logging host 192.168.0.10`
- s. 238: `R1(config)#logging trap debugging`
- s. 238: `R1# fot`
- s. 239: `R1#debug ip icmp`
- s. 239: `R1#ping 172.16.0.2`
- s. 240: `R1#show running-config`
- s. 240: `ip address 172.16.0.1 255.255.0.0`
- s. 240: `ip classless`
- s. 240: `ip flow-export version $`
- s. 240: `logging trap debugging`
- s. 240: `logging 192.168.0.10`
- s. 241: `Configure the NTP server to work with the syslog server and provide unified`
- s. 243: `R1(config)#do ping 192.168.0.20`
- s. 243: `R1(config)#ntp server 192.168.0.20`
- s. 244: `R1#show clock`
- s. 244: `NTP Server`
- s. 244: `Rl#show clock`
- s. 245: `R1(config)#service timestamps log datetime msec`
- s. 245: `Ri#ping 192.168.0.20`
- s. 245: `Rl#ping 192.168.0.20`
- s. 250: `IP ACL (Access Control List) is a rule-based feature in Cisco routers that enables network`
- s. 251: `R2(config)#ip access-list standard 1`
- s. 251: `R2(config-std-nacl)#exit`
- s. 252: `R2(config)#access-list 1 deny 172.16.2.0 0.0.0.255`
- s. 252: `R2(config)#access-list 1 permit any`
- s. 252: `R2(config)#interface gigabitethernet 0/0`
- s. 252: `R2(config-if)#ip access-group 1 out`
- s. 252: `R2(config-if)#exit`
- s. 253: `R2(config)#do show access-lists`
- s. 253: `R2(config)#do show running-config`
- s. 253: `interface GigabitEtherneto/o`
- s. 253: `ip access-group 1 out`
- s. 253: `ip address 172.16.2.100 255.255.255.0`
- s. 253: `interface GigabitEthernet6/0/0`
- s. 253: `ip address 10.0.0.2 255.255.255.252`
- s. 253: `ip address 90.10.10.1 255.255.255.252`
- s. 254: `Ping 172.16.1.1 from 172.16.2.1`
- s. 254: `C:\>ping 172.16.1.1`
- s. 254: `Ping statistics for 172.16.1.1:`
- s. 254: `Ping 172.16.1.1 from 192.168.2.1`
- s. 255: `R1(config)#ip access-list standard BLOCK_HOST`
- s. 255: `R1(config-std-nacl)#`
- s. 255: `R1(config-std-nacl)#deny host 192.168.2.1`
- s. 255: `R1(config-std-nacl)#permit any`
- s. 255: `R1(config-std-nacl)#exit`
- s. 256: `R1(config-if)#ip access-group BLOCK_HOST out`
- s. 256: `R1(config)#do show access-lists`
- s. 256: `interface GigabitEthernet0/0`
- s. 256: `ip address 152.168.1.100 255.255.255.0`
- s. 256: `ip access-group BLOCK_HOST out`
- s. 256: `ip address 192.168.2.100 255.255.255.0`
- s. 256: `ip address 10.0.0.1 255.255.255.252`
- s. 256: `interface GigabitEthernet0/1/0`
- s. 256: `interface GigabitEthernet0/2/0`
- s. 257: `Ping 192.168.1.1 from 192.168.2.1`
- s. 257: `C:\>ping 192.168.1.1`
- s. 257: `Ping statiarics for 192.168 1.04`
- s. 257: `Ping 192.168.1.2 from 192.168.2.2`
- s. 257: `c:\>ping 192.168.1.2`
- s. 257: `Ping Statistics for 192.166.1.2*`
- s. 258: `network to an endpoint on the R&D network.`
- s. 258: `R2(config)#ip access-list extended 100`
- s. 258: `R2(config-ext-nacl)#exit`
- s. 258: `R2(config)#access-list 100 deny ip host 172.16.2.1 host`
- s. 258: `R2(config)#access-list 100 permit ip any any`
- s. 259: `R2(config)#interface gigabitethernet 0/1`
- s. 259: `R2(config-if)#ip access-group 100 in`
- s. 260: `ip address 172.16.1.100 255.255.255.0`
- s. 260: `ip access-group 100 in`
- s. 260: `interface GigabitEtherneto/0/0`
- s. 260: `ip address 80.10.10.1 255.255.255.252`
- s. 260: `Ping from 172.16.2.1 to 192.168.1.2`
- s. 260: `Ping statistics for 19?.168.1..2*`
- s. 261: `Ping from 172.16.2.2 to 192.168.1.2`
- s. 261: `C:\>ping 192.168.1.2`
- s. 261: `Ping statistics for 192.168.1.2:`
- s. 262: `R1(config)#ip access-list extended BLOCK_HTTP`
- s. 262: `R1(config-ext-nacl)#`
- s. 262: `R1(config-ext-nacl)#deny tcp host 192.168.1.2 host 172.16.1.2 eq`
- s. 262: `R1(config-ext-nacl)#permit ip any any`
- s. 262: `R1(config-ext-nacl)#exit`
- s. 262: `R1(config-if)#ip access-group BLOCK_HTTP in`
- s. 263: `Rl(config)#do show access—lists`
- s. 263: `interface GigabitEtherneto/0`
- s. 263: `ip address 192.168.1.100 255.255.255.0`
- s. 263: `ip access-group BLOCK HOST out`
- s. 263: `interface GigabitEtherneto/1/0`
- s. 265: `Rl#show access-lists`
- s. 265: `R1#| Mw`
- s. 265: `R1(config-ext-nacl)#15 deny tcp host 192.168.1.2 host 172.16.1.2`
- s. 266: `Ri(config)#do show access—lists`

## Padriseup

- s. 5: `Ping - używa protokołu ICMP - Internet Control Message Protocol, dosł. internetowy protokół`
- s. 5: `ipconfig - komenda wyświetlająca informacje o konfiguracji interfejsów sieciowych w`
- s. 6: `Nslookup - odpytuje serwer DNS (zawsze) o rekord. Dlatego Nslookup nie pokaże nam`
- s. 6: `nslookup może odpytać o konkretny rodzaj rekordu, np:`
- s. 6: `nslookup -q=TXT hackampus.com`
- s. 6: `Tracert - działa podobnie jak ping z użyciem ICMP. Wysyła natomiast pakiety z TTL`
- s. 6: `Netsh - Netshell - narzędzie tekstowe do konfiguracji sieci w Windowsie.`
- s. 7: `edit>>preferences>>packet diagram`
- s. 10: `arp -a - wyświetlenie tablicy ARP`
- s. 10: `arp -d - usuwanie tablicy ARP [jako Administrator]`
- s. 11: `logging synchronous`
- s. 11: `configure terminal`
- s. 11: `hostname S1-Floor1`
- s. 11: `username Admin password p@nd@`
- s. 11: `show running-config`
- s. 11: `conf t`
- s. 11: `service password-encryption`
- s. 11: `exit`
- s. 11: `copy running-config startup-config`
- s. 11: `show interfaces FastEthernet 0/1`
- s. 11: `show mac-address-table`
- s. 12: `SSH-TCP/22`
- s. 12: `hostname S1`
- s. 12: `enable password c!sc0`
- s. 12: `banner motd #Authorized Access only. Hacking is illegal, log out#`
- s. 12: `ip domain-name CyberPro.com`
- s. 12: `wr`
- s. 12: `line vty 0 15`
- s. 12: `login local`
- s. 12: `transport input ssh`
- s. 12: `interface vlan 1`
- s. 13: `ip add`
- s. 13: `ip address 10.0.0.150 255.255.255.0`
- s. 13: `no shutdown`
- s. 13: `crypto key generate rsa`
- s. 13: `S1#show ip ssh - pokaże, że ssh uruchomiono`
- s. 13: `interface range fastEthernet 0/1-4`
- s. 13: `switchport mode access`
- s. 13: `switchport port-security`
- s. 13: `S1(config)#interface fastEthernet 0/1`
- s. 13: `S1(config-if)#switchport port-security mac-address 00D0.9793.87C4`
- s. 13: `S1(config-if)#exit`
- s. 13: `S1(config)#interface fastEthernet 0/2`
- s. 13: `S1(config-if)#switchport port-security mac-address 0009.7C96.0271`
- s. 13: `S1(config)#interface fastEthernet 0/3`
- s. 13: `S1(config-if)#switchport port-security mac-address sticky`
- s. 13: `S1(config)#interface fastEthernet 0/4`
- s. 14: `S1(config-if)#switchport port-security violation shutdown`
- s. 14: `S1(config)#interface range fastEthernet 0/2-3`
- s. 14: `S1(config-if-range)#switchport port-security violation restrict`
- s. 14: `S1(config-if-range)#exit`
- s. 14: `S1(config)#interface range fastEthernet 0/4`
- s. 14: `S1(config-if-range)#switchport port-security violation protect`
- s. 14: `S1(config)#interface range fastEthernet 0/5-24, gigabitEthernet 0/1-2`
- s. 14: `S1(config-if-range)#shutdown`
- s. 14: `S1>enable`
- s. 14: `S1#show port-security`
- s. 14: `S1#show port-security address`
- s. 14: `S1#show port-security interface fastEthernet 0/4`
- s. 14: `S1#show running-config`
- s. 14: `interface FastEthernet0/3`
- s. 14: `switchport port-security maximum 2`
- s. 14: `switchport port-security mac-address sticky`
- s. 14: `switchport port-security violation restrict`
- s. 14: `switchport port-security mac-address sticky 0004.9A8B.2832`
- s. 14: `switchport port-security mac-address sticky 0090.0C26.3CEE`
- s. 15: `Switch>enable`
- s. 15: `Switch#conf t`
- s. 15: `Switch(config)#hostname S1`
- s. 15: `S1(config)#username Admin password p@nd@`
- s. 15: `S1(config)#enable password c!sc0`
- s. 15: `S1(config)#ip ssh version 2`
- s. 15: `S1(config)#do show ip ssh`
- s. 15: `enable`
- s. 15: `conf t - przechodzimy w tryb konfiguracji`
- s. 15: `Router>enable`
- s. 15: `Router#conf t`
- s. 15: `Router(config)#hostname R1`
- s. 15: `R1(config)#username Admin password p@nd@`
- s. 15: `R1(config)#enable password c!sc0`
- s. 15: `R1(config)#service password-encryption`
- s. 15: `R1(config)#banner motd #Access to this device is for authorized personnel only!#`
- s. 15: `R1(config)#line console 0`
- s. 15: `R1(config-line)#login local`
- s. 15: `R1(config-line)#exit`
- s. 15: `R1(config)#exit`
- s. 15: `R1#show running-config`
- s. 16: `R1#copy running-config startup-config`
- s. 16: `R1#conf t`
- s. 16: `R1(config)#interface gigabitEthernet 0/0`
- s. 16: `R1(config-if)#ip address 192.168.0.1 255.255.255.0`
- s. 16: `R1(config-if)#no shutdown`
- s. 16: `R1(config-if)#exit`
- s. 16: `R1(config)#interface gigabitEthernet 0/1`
- s. 16: `R1(config-if)#ip address 10.0.0.1 255.255.255.0`
- s. 16: `R1(config)#do show ip interface brief`
- s. 16: `R1(config)#do show ip route`
- s. 16: `banner motd # Access to this device is for authorized personnel only!#`
- s. 16: `Interface ​`
- s. 16: `R1# show ip interface brief`
- s. 17: `S1#conf t`
- s. 17: `S1(config)#interface vlan 1`
- s. 17: `S1(config-if)#ip address 192.168.0.4 255.255.255.0`
- s. 17: `S1(config-if)#no shutdown`
- s. 17: `S1(config)#`
- s. 17: `S2>enable`
- s. 17: `S2#conf t`
- s. 17: `S2(config)#interface vlan 1`
- s. 17: `S2(config-if)#ip address 10.0.0.4 255.255.255.0`
- s. 17: `S2(config-if)#no shutdown`
- s. 17: `S2(config-if)#exit`
- s. 17: `S2(config)#`
- s. 17: `S2(config)#ip default-gateway 10.0.0.1`
- s. 17: `R1>enable`
- s. 17: `R1(config)#ipv6 unicast-routing`
- s. 17: `R1(config-if)#ipv6 address 2001:cafe:abcd:1::/64`
- s. 17: `R1(config)#`
- s. 18: `route print`
- s. 18: `route add 0.0.0.0 mask 0.0.0.0 192.168.100.1 metric 1`
- s. 18: `route delete 0.0.0.0`
- s. 18: `R1#show ip route`
- s. 18: `R1(config)#ip route 192.168.0.64 255.255.255.192 serial 0/0/0`
- s. 18: `R1(config)#ip route 192.168.0.128 255.255.255.192 serial 0/0/0`
- s. 18: `R1(config)#ip route 192.168.0.196 255.255.255.252 serial 0/0/0`
- s. 18: `R2(config)#ip route 192.168.0.0 255.255.255.192 192.168.0.193`
- s. 18: `R2(config)#ip route 192.168.0.128 255.255.255.192 192.168.0.198`
- s. 18: `R2(config)#exit`
- s. 18: `no ip route 192.168.0.0 255.255.255.192 192.168.0.193`
- s. 18: `no ip route 192.168.0.128 255.255.255.192 192.168.0.198`
- s. 18: `R3#conf terminal`
- s. 18: `R3(config)#ip route 192.168.0.0 255.255.255.192 ser`
- s. 18: `R3(config)#ip route 192.168.0.0 255.255.255.192 serial 0/0/1`
- s. 18: `R3(config)#ip route 192.168.0.64 255.255.255.192 serial 0/0/1`
- s. 19: `R3(config)#ip route 192.168.0.192 255.255.255.252 serial 0/0/1`
- s. 19: `R3(config)#exit`
- s. 19: `R3#show ip route`
- s. 19: `ping 192.168.0.194`
- s. 19: `R1(config)#ip route 0.0.0.0 0.0.0.0 serial 0/0/0`
- s. 19: `R2#conf t`
- s. 19: `R2(config)#ip route 0.0.0.0 0.0.0.0 serial 0/1/0`
- s. 19: `R2(config)#do show ip route static`
- s. 19: `R3>enable`
- s. 19: `R3#conf t`
- s. 19: `R3(config)#ip route 0.0.0.0 0.0.0.0 serial 0/0/1`
- s. 19: `R3(config)#do show ip route static`
- s. 19: `R1#enable`
- s. 20: `R1(config)#router rip`
- s. 20: `R1(config-router)#version 2`
- s. 20: `R1(config-router)#no auto-summary`
- s. 20: `R1(config-router)#network 172.16.0.0`
- s. 20: `R1(config-router)#network 172.16.0.8`
- s. 20: `R1(config-router)#network 192.168.10.0`
- s. 20: `R1(config-router)#passive-interface gigabitEthernet 0/0`
- s. 20: `R1(config-router)#exit`
- s. 20: `R1>en`
- s. 20: `R1#`
- s. 21: `R2>en`
- s. 21: `R2#show ip route connected`
- s. 21: `R2(config)#router rip`
- s. 21: `R2(config-router)#version 2`
- s. 21: `R2(config-router)#no auto-summary`
- s. 21: `R2(config-router)#network 172.16.0.0`
- s. 21: `R2(config-router)#network 172.16.0.4`
- s. 21: `R2(config-router)#network 192.168.20.0`
- s. 21: `R2(config-router)#passive-interface gigabitEthernet 0/0`
- s. 21: `R2(config-router)#exit`
- s. 21: `R2#copy running-config startup-config`
- s. 21: `R2#`
- s. 21: `R3>en`
- s. 21: `R3#show ip route connected`
- s. 22: `R3(config)#router rip`
- s. 22: `R3(config-router)#version 2`
- s. 22: `R3(config-router)#no auto-summary`
- s. 22: `R3(config-router)#network 172.16.0.4`
- s. 22: `R3(config-router)#network 172.16.0.8`
- s. 22: `R3(config-router)#network 192.168.30.0`
- s. 22: `R3(config-router)#network 210.10.10.0`
- s. 22: `R3(config-router)#passive-interface gigabitEthernet 0/0`
- s. 22: `R3(config-router)#exit`
- s. 22: `R3#copy running-config startup-config`
- s. 22: `R3#show ip route rip`
- s. 22: `R3(config)#ip route 0.0.0.0 0.0.0.0 serial 0/2/0`
- s. 23: `R3#`
- s. 23: `R3(config-router)#default-information originate`
- s. 23: `R3(config)#`
- s. 23: `R0#conf t`
- s. 24: `R0(config)#router ospf 1`
- s. 24: `R0(config-router)#router-id 1.1.1.0`
- s. 24: `R0(config-router)#network 192.168.0.0 0.0.0.255 area 0`
- s. 24: `R0(config-router)#network 172.16.0.0 0.0.0.3 area 0`
- s. 24: `R0(config-router)#network 172.16.0.8 0.0.0.3 area 0`
- s. 24: `R0(config-router)#auto-cost reference-bandwidth 1000`
- s. 24: `R0(config-router)#passive-interface gigabitEthernet 0/1`
- s. 24: `R0(config-router)#exit`
- s. 24: `R0(config)#exit`
- s. 24: `R0#`
- s. 24: `R1(config)#router ospf 1`
- s. 24: `R1(config-router)#router-id 1.1.1.1`
- s. 24: `R1(config-router)#network 192.168.1.0 0.0.0.255 area 0`
- s. 24: `R1(config-router)#network 172.16.0.4 0.0.0.3 area 0`
- s. 24: `R1(config-router)#network 172.16.0.8 0.0.0.3 area 0`
- s. 24: `R1(config-router)#auto-cost reference-bandwidth 1000`
- s. 24: `R1(config-router)#passive-interface gigabitEthernet 0/1`
- s. 24: `R2(config)#router ospf 1`
- s. 24: `R2(config-router)#router-id 1.1.1.2`
- s. 25: `R2(config-router)#network 192.168.2.0 0.0.0.255 area 0`
- s. 25: `R2(config-router)#network 172.16.0.4 0.0.0.3 area 0`
- s. 25: `R2(config-router)#network 172.16.0.0 0.0.0.3 area 0`
- s. 25: `R2(config-router)#auto-cost reference-bandwidth 1000`
- s. 25: `R2(config-router)#passive-interface gigabitEthernet 0/1`
- s. 25: `R2(config)#`
- s. 25: `R2#show ip route ospf`
- s. 25: `S2(config)#vlan 10`
- s. 25: `S2(config-vlan)#name Workstation`
- s. 25: `S2(config-vlan)#exit`
- s. 25: `S2(config)#vlan 20`
- s. 25: `S2(config-vlan)#name Servers`
- s. 25: `S2(config)#do show vlan brief`
- s. 26: `S2(config)#interface range fastEthernet 0/1-4`
- s. 26: `S2(config-if-range)#switchport mode access`
- s. 26: `S2(config-if-range)#switchport access vlan 10`
- s. 26: `S2(config-if-range)#exit`
- s. 26: `S2(config)#interface range fastEthernet 0/5-6`
- s. 26: `S2(config-if-range)#switchport access vlan 20`
- s. 26: `S1(config)#vlan 10`
- s. 26: `S1(config-vlan)#name Workstation`
- s. 26: `S1(config-vlan)#exit`
- s. 26: `S1(config)#vlan 20`
- s. 26: `S1(config-vlan)#name Servers`
- s. 26: `S1(config)#interface range fastEthernet 0/1-2`
- s. 26: `S1(config-if-range)#switchport mode access`
- s. 26: `S1(config-if-range)#switchport access vlan 10`
- s. 27: `S1(config-if)#switchport mode access`
- s. 27: `S1(config-if)#switchport access vlan 20`
- s. 27: `S1(config)#do show vlan brief`
- s. 27: `S1(config)#interface range gigabitEthernet 0/1-2`
- s. 27: `S1(config-if-range)#switchport mode trunk`
- s. 27: `S1(config-if-range)#`
- s. 28: `do show interfaces switchport`
- s. 28: `S2>en`
- s. 28: `S2(config)#interface gigabitEthernet 0/1`
- s. 28: `S2(config-if)#switchport mode trunk`
- s. 28: `S2(config)#vlan 30`
- s. 28: `S2(config-vlan)#name Native`
- s. 28: `S2(config-if)#switchport trunk native vlan 30`
- s. 28: `S1#copy running-config startup-config`
- s. 28: `S2#copy running-config startup-config`
- s. 28: `R2>enable`
- s. 28: `R2#conf terminal`
- s. 28: `R2(config)#ip access-list standard 1`
- s. 28: `R2(config-std-nacl)#exit`
- s. 28: `R2(config)#access-list 1 deny 172.16.2.0 0.0.0.255`
- s. 29: `R2(config)#access-list 1 permit any`
- s. 29: `R2(config)#interface gigabitEthernet 0/0`
- s. 29: `R2(config-if)#ip access-group 1 out`
- s. 29: `R2(config-if)#exit`
- s. 29: `R1#configure terminal`
- s. 29: `R1(config)#ip access-list standard BLOCK_HOST`
- s. 29: `R1(config-std-nacl)#deny host 192.168.2.1`
- s. 29: `R1(config-std-nacl)#permit any`
- s. 29: `R1(config-std-nacl)#exit`
- s. 29: `R1(config-if)#ip access-group BLOCK_HOST out`
- s. 29: `R1(config)#do show access-list`
- s. 29: `R2(config)#ip access-list extended 100`
- s. 29: `R2(config-ext-nacl)#exit`
- s. 29: `R2(config)#access-list 100 deny ip host 172.16.2.1 host 192.168.1.2`
- s. 29: `R2(config)#access-list 100 permit ip any any`
- s. 29: `R2(config)#interface gigabitEthernet 0/1`
- s. 29: `R2(config-if)#ip access-group 100 in`
- s. 29: `R2(config)#do show access-list`
- s. 29: `R1(config)#ip access-list extended BLOCK_HTTP`
- s. 29: `R1(config-ext-nacl)#deny tcp host 192.168.1.2 host 172.16.1.2 eq 80`
- s. 30: `R1(config-ext-nacl)#permit ip any any`
- s. 30: `R1(config-ext-nacl)#exit`
- s. 30: `R1(config-if)#ip access-group BLOCK_HTTP in`

## Cisco project

- s. 1: `Switch>`
- s. 1: `Switch>en`
- s. 1: `Switch#conf t`
- s. 1: `Switch(config)#vlan 30`
- s. 1: `Switch(config)#vlan 100`
- s. 2: `Interface range gigabitethernet 0/1-2`
- s. 2: `Switchport mode trunk`
- s. 2: `Switchport trunk native vlan 100`
- s. 2: `do show interfaces switchport`
- s. 2: `Name: Gig0/1 Name: Gig0/1`
- s. 2: `Switchport: Enabled Switchport: Enabled`
- s. 2: `Name: Gig0/2`
- s. 2: `Switchport: Enabled`
- s. 2: `Do show interfaces trunk`
- s. 2: `Interface range fastethernet 0/1-24`
- s. 2: `Switchport mode access`
- s. 2: `Switchport nonegotiate`
- s. 2: `Exit`
- s. 2: `Show interfaces switchport`
- s. 2: `Switch#show interfaces switchport`
- s. 2: `Name: Fa0/1`
- s. 2: `copy running-config startup-config`
- s. 3: `R3(config-if)#ip add`
- s. 3: `R3(config-if)#ip address 172.16.10.1 255.255.255.224`
- s. 3: `R3(config-if)#no s`
- s. 3: `R3(config-if)#no sh`
- s. 3: `R3(config-if)#no shutdown`
- s. 3: `R3(config-if)#`
- s. 3: `interface gigabitEthernet 0/1`
- s. 3: `R3(config-if)#ip address 172.16.10.33 255.255.255.224`
- s. 3: `R2(config-if)#ip address 172.16.10.66 255.255.255.224`
- s. 3: `R3(config-if)#ip address 172.16.10.130 255.255.255.224`
- s. 3: `R3(config-if)#ip address 172.16.10.98 255.255.255.224`
- s. 4: `Interface FastEthernet0 Interface FastEthernetO`
- s. 4: `IP Configuration IP Configuration`
- s. 4: `Interface FastEthernet0 Interface FastEthernet0`
- s. 5: `no shutdown`
- s. 5: `encapsulation dot1Q 20`
- s. 5: `encapsulation dot1Q 30`
- s. 6: `R1#`
- s. 6: `show ip interface brief`
- s. 6: `Interface IP-Address OK? Method Status Protocol`
- s. 6: `Switchport trunk native vlan 100 Switen(configy af`
- s. 6: `Show`
- s. 6: `Show port-security address.`
- s. 6: `Interface fastEthernet 0/2`
- s. 6: `switchport mode access`
- s. 6: `switchport port-security`
- s. 6: `switchport port-security violation restrict`
- s. 6: `switchport port-security mac-address sticky`
- s. 6: `Show interfaces status`
- s. 6: `Interface fast...`
- s. 7: `Show ip route connected`
- s. 7: `No shutdown`
- s. 7: `Router ospf 1`
- s. 7: `router-id 1.1.1.1`
- s. 7: `Network 111.111.111.111 0.0.0.255 area 0`
- s. 7: `Passive-interface`
- s. 8: `Show ip protocols`
- s. 8: `Show ip ospf interface`
- s. 8: `Show ip ospf neighbor`
- s. 8: `Copy running-config startup-config`
- s. 8: `Show access-list`
- s. 8: `Router (config) #access-list 137 deny ip host 172.16.10.60 host 172.16.10.29`
- s. 8: `Router (config) #exit`
- s. 8: `Router#show access-lists`
- s. 8: `Access-list 2137 deny ip host 172.16.10.60 host 172.16.10.29`
- s. 8: `Username Admin password ACDC1973`
- s. 8: `Enable password beatles1960`
- s. 8: `Service password-encryption`
- s. 8: `Banner motd #Only authorized personnel are allowed accessing this device#`
- s. 8: `Wr`
- s. 8: `Ip domain-name Cyber.local`
- s. 8: `Crypto key generate rsa 1024`
- s. 8: `Ip ssh version 2`
- s. 8: `Line vty 0 4`
- s. 8: `Login local`
- s. 8: `Transport input SSH`
- s. 9: `Show ip ssh`
- s. 9: `Show ssh`
- s. 9: `Router>en`
- s. 9: `Router#conf t`
- s. 9: `Router (config) #ip do`
- s. 9: `Router (config) #ip dom`
- s. 9: `Router (config) #ip domain-name Cyber. local`
- s. 9: `Router (config) #cry`
- s. 9: `Router (config) #crypto key generate rsa`
- s. 9: `Router (config) thostn`
- s. 9: `Router (config) #hostname R1`
- s. 9: `Rl#show ip ssh`
- s. 9: `SSH Enabled - version 2.0`
- s. 9: `C:\>ssh “1 Adin 172.16.10.1`
- s. 9: `banner motd`
- s. 9: `R3# show ip ssh`
- s. 9: `R3#show ssh`
- s. 9: `Username`
- s. 9: `R3#`

---

# 08 — Indeks technologii, protokołów, narzędzi i zagadnień

Numery stron wskazują, gdzie termin pojawia się w danym źródle. Indeks nie zastępuje pełnej treści — jest nawigacją.

- **ARPANET** — Textbook: 6 | Slides: 8 | Padriseup: 2
- **LAN** — Textbook: 3, 5, 7, 8, 10, 20, 22, 23, 26, 56, 62, 63, 85, 88, 90, 103, 110, 111, 113, 122, 141, 145, 154, 155, 157, 158, 159, 160, 161, 162, 163, 164, 165, 166, 167, 168, 169, 170, 171, 174, 178, 181, 190, 205, 208, 210, 211, 212 | Slides: 2, 6, 7, 11, 19, 39, 44, 45, 52, 58, 114, 122, 126, 127, 175, 187, 196, 197, 201, 209, 233, 251, 253, 260, 263, 270, 286, 287, 292, 325, 338, 339, 349, 368, 374, 375, 376, 377, 378, 379, 380, 381, 382, 383, 384, 385, 386, 387, 388, 389, 390, 391, 395, 397, 398, 399, 400, 401, 402, 403… | Labs: 27, 60, 66, 67, 68, 81, 82, 83, 84, 85, 92, 97, 101, 106, 109, 117, 121, 132, 138, 146, 147, 149, 154, 158, 170, 174, 211, 212, 215, 216, 217, 218, 219, 220, 224, 225, 226, 229, 230, 240, 260 | Padriseup: 3, 4, 6, 8, 9, 12, 17, 25, 26, 27, 28 | Cisco project: 1, 2, 6
- **WAN** — Textbook: 5, 15, 43, 52, 56, 67, 90, 127, 206, 210, 211, 212 | Slides: 6, 7, 30, 96, 108, 114, 115, 116, 119, 139, 172, 176, 303, 513, 514, 519, 520, 521 | Labs: 18, 25, 43, 65, 69, 94, 98, 132, 188, 252 | Padriseup: 1, 2, 3, 4, 6, 7, 8, 10, 13 | Cisco project: 9
- **MAN** — Textbook: 2, 3, 5, 10, 15, 16, 18, 20, 21, 22, 23, 24, 25, 26, 29, 30, 43, 44, 45, 48, 53, 55, 57, 58, 62, 66, 67, 68, 69, 70, 72, 73, 74, 75, 76, 77, 79, 80, 81, 82, 83, 84, 85, 86, 88, 90, 91, 92, 93, 98, 99, 100, 101, 104, 105, 108, 110, 113, 117, 118… | Slides: 3, 5, 6, 7, 19, 31, 32, 35, 38, 39, 40, 41, 42, 44, 46, 47, 50, 52, 57, 62, 64, 96, 97, 100, 105, 109, 123, 125, 126, 135, 138, 139, 142, 143, 144, 145, 147, 148, 149, 159, 160, 161, 162, 166, 169, 170, 171, 180, 181, 182, 185, 186, 187, 190, 191, 195, 200, 202, 203, 204… | Labs: 2, 4, 5, 6, 7, 10, 12, 13, 14, 31, 32, 33, 48, 53, 54, 55, 56, 57, 58, 59, 61, 62, 63, 64, 65, 66, 67, 71, 72, 76, 77, 78, 79, 81, 82, 83, 84, 85, 87, 90, 91, 92, 93, 94, 95, 96, 97, 100, 101, 104, 106, 108, 109, 112, 116, 117, 118, 119, 120, 122… | Padriseup: 2, 3, 8, 16, 19, 20, 22 | Cisco project: 1, 6, 9
- **SAN** — Textbook: 5, 11, 15, 52, 87, 113, 174 | Slides: 7, 21, 31, 108, 126, 139, 263, 296, 363, 424 | Labs: 19, 29, 44, 144, 249 | Padriseup: 1, 2, 3
- **NIC** — Textbook: 2, 3, 5, 6, 7, 8, 9, 10, 14, 16, 17, 20, 22, 25, 26, 30, 31, 36, 38, 40, 41, 55, 56, 59, 64, 66, 67, 80, 83, 86, 88, 90, 93, 96, 98, 99, 105, 107, 108, 109, 110, 111, 112, 127, 134, 148, 150, 172, 176, 178, 181, 184, 188, 191, 192, 197, 201, 202, 203, 207… | Slides: 5, 6, 7, 8, 9, 10, 11, 13, 15, 16, 17, 18, 30, 32, 34, 37, 39, 40, 44, 49, 50, 51, 52, 59, 63, 65, 81, 82, 90, 93, 94, 100, 114, 115, 118, 131, 138, 139, 170, 183, 193, 196, 197, 212, 222, 224, 225, 237, 241, 242, 244, 248, 251, 252, 253, 254, 255, 256, 303, 318… | Labs: 12, 18, 21, 49, 77, 79, 82, 85, 90, 98, 99, 102, 103, 105, 107, 109, 132, 138, 152, 153, 158, 215, 216, 221, 224, 229, 240, 245, 260 | Padriseup: 3, 4, 5, 9, 17 | Cisco project: 2
- **MAC address** — Textbook: 7, 17, 18, 56, 58, 62, 63, 64, 81, 82, 85, 124, 171, 202, 205 | Slides: 13, 14, 34, 35, 114, 115, 117, 126, 129, 130, 176, 178, 179, 180, 181, 182, 187, 296, 415 | Labs: 67, 68, 91, 92, 93, 94, 97, 104, 106, 109, 110, 215
- **Hub** — Textbook: 8, 34, 81 | Slides: 14, 15, 73, 178 | Padriseup: 4
- **Switch** — Textbook: 2, 7, 8, 9, 10, 13, 33, 56, 62, 63, 64, 65, 66, 68, 69, 70, 72, 73, 74, 75, 81, 82, 83, 84, 85, 86, 88, 90, 91, 92, 103, 123, 141, 155, 158, 159, 160, 161, 162, 163, 164, 165, 166, 167, 168, 169, 174, 175, 176, 177, 178, 185, 206 | Slides: 2, 13, 14, 15, 18, 19, 25, 58, 73, 114, 115, 121, 122, 123, 124, 125, 126, 127, 128, 129, 130, 131, 132, 133, 134, 135, 144, 146, 147, 148, 152, 153, 154, 155, 156, 157, 158, 159, 161, 162, 164, 171, 174, 175, 176, 177, 178, 179, 180, 181, 182, 183, 185, 186, 187, 188, 189, 190, 195, 196… | Labs: 29, 34, 35, 47, 48, 50, 54, 55, 56, 57, 58, 61, 62, 66, 67, 71, 72, 76, 77, 78, 79, 81, 84, 85, 86, 87, 91, 92, 93, 94, 95, 96, 105, 111, 112, 116, 117, 118, 119, 123, 135, 146, 215, 216, 218, 219, 222, 224, 225, 226, 227, 229, 241 | Padriseup: 4, 8, 9, 13, 14, 15, 26, 27, 28 | Cisco project: 1, 2, 6, 7
- **Layer 2** — Textbook: 8, 9, 33, 37, 62, 88, 92, 102, 124, 158, 168, 174 | Slides: 14, 15, 73, 85, 125, 196, 205, 232, 296, 377, 401, 423 | Labs: 29, 215
- **Layer 3** — Textbook: 8, 33, 37, 48, 56, 88, 89, 98, 102, 123, 159, 168, 202 | Slides: 14, 72, 84, 105, 114, 196, 197, 198, 222, 231, 288, 378, 401 | Labs: 29, 32, 33, 112, 117
- **Router** — Textbook: 2, 3, 8, 10, 30, 33, 37, 66, 68, 76, 78, 79, 80, 88, 91, 93, 98, 99, 100, 101, 102, 103, 107, 108, 110, 112, 123, 124, 125, 126, 128, 129, 134, 136, 138, 139, 140, 141, 142, 143, 144, 145, 146, 148, 149, 150, 151, 152, 153, 154, 155, 163, 168, 169, 173, 174, 176, 178, 179, 181… | Slides: 14, 16, 18, 19, 64, 72, 85, 135, 144, 146, 163, 167, 168, 169, 170, 195, 196, 197, 202, 210, 221, 222, 223, 226, 227, 228, 229, 231, 232, 233, 234, 242, 244, 246, 250, 251, 256, 288, 293, 294, 295, 296, 297, 298, 299, 300, 304, 307, 318, 319, 330, 331, 334, 335, 336, 337, 338, 344, 345, 347… | Labs: 7, 9, 54, 131, 132, 135, 136, 138, 139, 141, 144, 145, 149, 153, 156, 170, 173, 175, 176, 177, 180, 192, 193, 194, 195, 196, 200, 202, 204, 207, 208, 209, 212, 224, 229, 230, 233, 241, 250 | Padriseup: 4, 6, 9, 15, 16, 19, 20, 21, 22, 23, 24, 25 | Cisco project: 7, 8, 9
- **Access Point** — Textbook: 10, 26, 178 | Slides: 19, 51, 433 | Labs: 216
- **Firewall** — Textbook: 10, 30, 123, 188, 201, 208 | Slides: 19, 64, 459, 461, 491, 508 | Labs: 44
- **WLC** — Textbook: 10
- **Broadcast domain** — Textbook: 8, 83, 88, 107, 113, 119, 158, 168 | Slides: 16, 183, 196, 197, 242, 264, 278, 279, 379, 401 | Labs: 138, 215
- **Collision domain** — Textbook: 8, 9 | Slides: 15, 16 | Padriseup: 9
- **Half Duplex** — Textbook: 9, 64 | Slides: 17
- **Full Duplex** — Textbook: 9, 64 | Slides: 17
- **Ethernet** — Textbook: 7, 9, 11, 12, 13, 22, 24, 34, 37, 47, 48, 49, 50, 51, 52, 60, 61, 80, 81, 82, 84, 85, 99, 100, 103, 110, 128, 129, 130, 131, 132, 135, 139, 140, 144, 145, 148, 149, 153, 154, 155, 161, 162, 164, 165, 166, 167, 168, 169, 170, 176, 181, 192, 193, 194, 198, 199, 211, 214 | Slides: 13, 15, 22, 23, 25, 26, 27, 43, 46, 74, 79, 86, 103, 104, 105, 106, 107, 108, 170, 180, 182, 185, 186, 187, 225, 226, 227, 234, 251, 305, 306, 310, 311, 314, 320, 348, 349, 367, 368, 385, 387, 390, 391, 394, 395, 398, 399, 403, 404, 405, 406, 428, 432, 442, 450, 473, 474, 475, 482, 483… | Labs: 4, 13, 25, 26, 28, 29, 31, 32, 60, 61, 66, 68, 77, 85, 90, 92, 93, 94, 96, 97, 98, 100, 101, 104, 105, 106, 107, 109, 135, 136, 139, 140, 143, 144, 153, 154, 158, 175, 180, 181, 192, 193, 194, 195, 196, 197, 198, 207, 208, 209, 210, 215, 218, 219, 224, 225, 229, 230, 231, 240… | Padriseup: 3, 4, 5, 6, 9, 11, 13, 14, 16, 17, 20, 21, 22, 24, 25, 26, 27, 28, 29, 30 | Cisco project: 1, 2, 3, 4, 5, 6, 7
- **RJ45** — Textbook: 12, 34 | Slides: 74 | Padriseup: 9
- **CAT-5** — Textbook: 12 | Slides: 23 | Padriseup: 4, 5, 9
- **CAT-5e** — Textbook: 12 | Slides: 23 | Padriseup: 4
- **CAT-6** — Textbook: 12 | Slides: 23 | Padriseup: 4
- **CAT-6a** — Textbook: 12 | Slides: 23 | Padriseup: 4
- **CAT-7** — Slides: 23 | Padriseup: 4
- **UTP** — Textbook: 12, 68, 80, 99, 146, 154, 173, 183, 197 | Slides: 24, 143, 170, 226, 351, 352, 369, 420, 427, 431, 444 | Labs: 4, 24, 55, 56, 59, 60, 61, 63, 66, 67, 100, 101, 104 | Padriseup: 4, 5
- **STP** — Textbook: 12, 53, 166 | Slides: 109, 397 | Padriseup: 4, 5
- **RFI** — Textbook: 11, 12, 13, 28 | Slides: 22, 24, 27
- **EMI** — Textbook: 11, 12, 13, 28 | Slides: 22, 24, 27, 54
- **Fiber** — Textbook: 6, 13, 28, 34 | Slides: 9, 27, 54, 73
- **Straight Through** — Textbook: 13
- **Crossover** — Textbook: 13 | Slides: 26
- **Rollover** — Textbook: 13 | Slides: 25
- **Point-to-Point** — Textbook: 9, 14, 83, 128 | Slides: 183, 305 | Labs: 166, 176, 178, 181, 182
- **Star** — Textbook: 14, 18, 30, 47, 70, 71, 74, 76, 77, 78, 91, 120, 144, 153, 172, 173, 196, 214 | Slides: 3, 30, 64, 103, 150, 151, 156, 158, 163, 165, 166, 168, 203, 282, 347, 357, 366, 418, 420, 495 | Labs: 11, 18, 19, 26, 30, 40, 42, 43, 44, 51, 53, 54, 61, 63, 77, 78, 79, 90, 94, 123, 137, 141, 192, 193, 194, 195, 207, 227, 231, 237, 238 | Padriseup: 3, 11, 16, 20, 21, 22, 28 | Cisco project: 2, 6, 7, 8, 9
- **Mesh** — Textbook: 15 | Slides: 30 | Padriseup: 8
- **Hybrid** — Textbook: 15 | Slides: 30 | Padriseup: 8
- **3-Tier** — Textbook: 15, 16, 17 | Slides: 31, 32, 33
- **Collapsed Architecture** — Textbook: 16
- **IPv4** — Textbook: 2, 3, 18, 22, 34, 49, 58, 93, 99, 105, 106, 107, 108, 109, 110, 111, 112, 115, 124, 127, 133, 134, 135, 201, 202, 203, 209 | Slides: 2, 36, 43, 58, 74, 106, 118, 122, 175, 210, 236, 237, 238, 239, 240, 241, 242, 243, 244, 245, 246, 248, 250, 252, 253, 254, 255, 260, 269, 291, 292, 293, 294, 301, 302, 303, 308, 309, 312, 313, 315, 316, 317, 321, 325, 374, 411, 456, 488, 493, 497, 499, 509, 512, 515, 516 | Labs: 29, 116, 126, 127, 131, 132, 138, 139, 141, 152, 153, 154, 169, 170, 174, 180, 184, 250 | Padriseup: 5, 10 | Cisco project: 4, 5
- **IPv6** — Textbook: 3, 18, 22, 34, 49, 93, 107, 109, 110, 111, 112, 124, 134, 135, 142, 149, 201, 203, 209 | Slides: 2, 36, 43, 58, 74, 106, 122, 175, 247, 248, 249, 250, 251, 252, 253, 254, 255, 256, 260, 291, 292, 293, 294, 301, 316, 317, 318, 319, 320, 321, 325, 343, 356, 374, 411, 456, 488, 493, 499, 500, 516 | Labs: 132, 141, 143, 144, 148, 149, 152, 153, 154, 155, 156, 157, 158, 159, 169 | Padriseup: 5, 10, 17
- **Subnet Mask** — Textbook: 18, 19, 22, 100, 105, 106, 110, 114, 115, 116, 117, 118, 120, 128, 129, 132, 136, 142, 189, 203 | Slides: 37, 43, 238, 239, 250, 261, 266, 267, 273, 274, 275, 276, 277, 281, 304, 306, 313, 343, 361, 403, 466, 499 | Labs: 13, 63, 64, 138, 139, 142, 144, 163, 164, 165, 166, 167, 168, 185, 221, 229, 230 | Cisco project: 4, 5
- **Classful** — Textbook: 106, 136, 141, 142, 143 | Slides: 240, 340, 343, 346 | Labs: 163
- **Classless** — Textbook: 115, 116, 136, 141, 142 | Slides: 270, 340, 343 | Labs: 163, 240
- **CIDR** — Textbook: 3, 106, 115, 120, 142 | Slides: 261, 268, 269, 270, 271, 272, 273, 274, 275, 276, 277, 278, 279, 281, 282, 343 | Labs: 163
- **VLSM** — Textbook: 120, 141, 142 | Slides: 261, 280, 281, 282, 283, 284, 340, 343 | Labs: 163, 191
- **Wildcard** — Textbook: 151, 189, 191, 196 | Slides: 361, 466, 471 | Labs: 247, 252
- **Default Gateway** — Textbook: 22, 24, 90, 98, 102, 124, 168, 169, 201, 205, 206 | Slides: 43, 46, 223, 224, 232, 296, 403, 405, 492, 502 | Labs: 6, 13, 117, 139, 141, 142, 143, 144, 145, 146, 147, 155, 156, 157, 159, 221 | Cisco project: 4, 5
- **Loopback** — Textbook: 100, 101, 107, 151 | Slides: 228, 229, 243, 362 | Labs: 66, 101, 152
- **Link-local** — Textbook: 22, 107, 111, 112, 134, 203 | Slides: 43, 242, 253, 254, 319, 499 | Labs: 143, 144, 152, 158, 159
- **IP** — Textbook: 2, 3, 4, 5, 6, 7, 8, 10, 14, 15, 17, 18, 19, 20, 21, 22, 23, 24, 25, 28, 30, 31, 33, 34, 35, 36, 37, 38, 40, 42, 43, 45, 47, 49, 50, 52, 53, 55, 56, 57, 58, 59, 60, 61, 62, 63, 76, 80, 87, 88, 89, 90, 91, 92, 93, 98, 99, 100, 101, 102… | Slides: 2, 6, 7, 8, 13, 18, 19, 30, 34, 36, 37, 40, 42, 43, 44, 45, 46, 47, 54, 58, 59, 62, 63, 64, 65, 66, 71, 72, 74, 75, 76, 79, 80, 81, 82, 83, 84, 85, 86, 90, 92, 95, 97, 99, 100, 104, 106, 109, 110, 114, 115, 116, 117, 118, 122, 125, 128, 165, 170, 175… | Labs: 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 16, 17, 20, 22, 27, 28, 29, 30, 31, 32, 33, 53, 54, 58, 60, 63, 64, 65, 73, 78, 79, 83, 91, 94, 105, 108, 113, 116, 117, 118, 119, 120, 121, 123, 124, 126, 127, 131, 132, 138, 139, 140, 141, 142, 143, 144, 145, 146, 147, 148… | Padriseup: 2, 3, 4, 5, 6, 7, 8, 10, 12, 13, 15, 16, 17, 18, 19, 20, 21, 22, 23, 25, 28, 29, 30 | Cisco project: 3, 4, 5, 6, 7, 8, 9
- **DNS** — Textbook: 20, 22, 23, 24, 30, 34, 37, 43, 44, 45, 49, 53, 70, 99, 192, 198, 201, 203, 205, 206 | Slides: 43, 45, 46, 63, 74, 83, 96, 98, 100, 106, 109, 149, 224, 472, 481, 492, 500, 502 | Labs: 4, 5, 7, 10, 11, 17, 31, 32, 33, 64, 78, 144, 155, 159, 221, 237, 240, 241, 245 | Padriseup: 6, 7, 11 | Cisco project: 4, 5
- **DHCP** — Textbook: 3, 8, 20, 21, 24, 30, 34, 37, 43, 44, 98, 107, 122, 184, 186, 197, 201, 202, 203, 204, 205, 206, 207 | Slides: 16, 43, 46, 64, 74, 83, 96, 98, 224, 242, 288, 448, 481, 489, 490, 491, 492, 493, 494, 495, 496, 497, 498, 499, 500, 501, 502, 503, 504, 505, 506 | Labs: 13, 79, 80, 82, 156, 221, 237, 240, 241, 245 | Padriseup: 6, 11 | Cisco project: 4, 5
- **HTTP** — Textbook: 20, 29, 30, 34, 37, 43, 44, 45, 50, 53, 54, 59, 60, 80, 195 | Slides: 40, 63, 74, 78, 83, 96, 98, 99, 100, 107, 108, 109, 110, 170, 478 | Labs: 17, 26, 27, 28, 29, 30, 41, 79, 80, 82, 237, 241, 242, 245, 250, 262, 264, 265, 266 | Padriseup: 1, 2, 3, 5, 6, 7, 8, 9, 10, 11, 12, 13, 15, 17, 18, 19, 23, 25, 28, 29, 30
- **HTTPS** — Textbook: 20, 30, 34, 43, 44, 45, 195 | Slides: 40, 63, 96, 98, 100, 478 | Labs: 41, 265 | Padriseup: 1, 2, 3, 5, 6, 7, 8, 9, 10, 11, 12, 13, 15, 17, 18, 19, 23, 25, 28
- **FTP** — Textbook: 30, 33, 34, 37, 44, 45, 76, 77, 80, 196, 197, 198, 199 | Slides: 63, 70, 74, 83, 98, 100, 163, 164, 165, 166, 171, 481, 484 | Labs: 72, 76, 79, 80, 81, 82, 83, 237, 240, 241, 242 | Padriseup: 3, 5, 7
- **SMTP** — Textbook: 30, 34, 37, 44, 45 | Slides: 64, 74, 83, 98, 100 | Padriseup: 3
- **SSH** — Textbook: 2, 30, 33, 34, 37, 44, 55, 66, 67, 86, 89, 90, 91, 92, 159, 182, 212 | Slides: 64, 70, 74, 83, 98, 138, 139, 142, 190, 191, 192, 193, 198, 199, 200, 202, 203, 204, 205, 443, 520 | Labs: 17, 29, 111, 112, 116, 118, 119, 120, 121, 122, 123 | Padriseup: 12, 13, 15 | Cisco project: 8, 9
- **ICMP** — Textbook: 30, 34, 45, 48, 53, 125, 173, 188, 195, 203 | Slides: 74, 100, 105, 109, 297, 421, 463, 480, 500 | Labs: 33, 147, 238, 239, 240, 243, 245 | Padriseup: 5, 6, 11
- **ARP** — Textbook: 2, 6, 8, 36, 52, 53, 56, 57, 58, 202 | Slides: 8, 16, 59, 78, 109, 113, 114, 115, 116, 117, 118, 183 | Labs: 55, 66, 101, 215 | Padriseup: 2, 6, 10
- **TCP** — Textbook: 2, 31, 34, 36, 37, 38, 39, 40, 41, 42, 43, 44, 45, 47, 51, 53, 54, 58, 59, 60, 61, 86, 99, 195, 196, 197, 199, 212, 214 | Slides: 59, 65, 66, 71, 74, 76, 78, 79, 80, 81, 82, 83, 84, 85, 86, 88, 89, 91, 92, 93, 94, 96, 98, 99, 100, 103, 104, 108, 109, 110, 191, 224, 478, 480, 483, 484, 493, 520, 523 | Labs: 16, 17, 28, 123, 262, 263, 265, 266 | Padriseup: 2, 3, 6, 7, 10, 12, 29
- **UDP** — Textbook: 3, 34, 38, 39, 42, 43, 44, 45, 53, 54, 76, 180, 183, 185, 195, 201 | Slides: 71, 74, 88, 89, 90, 91, 96, 98, 100, 109, 110, 163, 342, 438, 444, 446, 478, 480, 493 | Labs: 17, 32 | Padriseup: 6, 7
- **RTP** — Textbook: 34, 38 | Slides: 74
- **SCTP** — Textbook: 34, 38 | Slides: 74
- **SNMP** — Textbook: 34, 37 | Slides: 74, 83 | Labs: 250
- **POP3** — Textbook: 34, 44 | Slides: 74, 98
- **SMB** — Textbook: 44, 204 | Slides: 98
- **TFTP** — Textbook: 37, 44, 76, 77, 80 | Slides: 98, 163, 164, 165, 166, 171 | Labs: 72, 76, 79, 80, 81, 82, 83, 237, 240, 241, 242
- **NTP** — Textbook: 3, 44, 185, 186, 187 | Slides: 98, 446, 447, 448, 450, 451, 452 | Labs: 80, 134, 151, 172, 190, 206, 214, 232, 233, 236, 240, 241, 242, 243, 244, 245 | Cisco project: 5
- **OSI** — Textbook: 9, 22, 31, 32, 33, 34, 35, 36, 37, 45, 56, 58, 59, 91, 93, 94, 95, 165, 172, 197, 201 | Slides: 15, 44, 59, 65, 66, 67, 68, 69, 70, 71, 72, 73, 74, 75, 76, 82, 83, 84, 85, 86, 100, 114, 118, 202, 212, 213, 214, 215, 342, 418, 481, 493 | Labs: 17, 41, 81, 82, 119, 245, 265 | Padriseup: 2, 3, 7, 10 | Cisco project: 9
- **TCP/IP** — Textbook: 2, 31, 36, 37, 45, 47, 58, 59, 99 | Slides: 59, 65, 66, 76, 80, 81, 82, 83, 84, 85, 86, 100, 104, 224, 493 | Labs: 16, 17 | Padriseup: 2, 3, 7
- **Encapsulation** — Textbook: 2, 56, 58, 59, 60, 61, 102, 124, 160, 163, 164, 169 | Slides: 59, 76, 77, 78, 79, 114, 118, 232, 296, 383, 391, 395, 399, 405 | Labs: 16, 66, 101, 226, 229, 230, 231 | Cisco project: 2, 5, 6
- **Decapsulation** — Textbook: 32, 58, 59, 102, 124 | Slides: 76, 77, 118, 232, 296
- **PDU** — Textbook: 47, 51, 59 | Slides: 103, 118
- **MTU** — Textbook: 60 | Slides: 79
- **FCS** — Textbook: 60, 61, 63, 102, 124 | Slides: 79, 128, 232, 296
- **SYN** — Textbook: 40, 52, 99, 128, 129, 134, 141, 185, 186, 191 | Slides: 92, 93, 108, 225, 304, 306, 319, 338, 446, 471, 480 | Labs: 236 | Padriseup: 7, 8, 11
- **ACK** — Textbook: 1, 8, 17, 21, 27, 30, 33, 36, 37, 38, 39, 40, 41, 42, 46, 47, 48, 49, 50, 51, 52, 53, 54, 58, 59, 60, 61, 63, 66, 68, 69, 76, 77, 80, 81, 98, 99, 100, 101, 102, 103, 107, 111, 112, 113, 122, 123, 124, 126, 127, 130, 134, 136, 138, 141, 147, 148, 149, 150, 151… | Slides: 16, 24, 42, 53, 57, 64, 72, 79, 81, 85, 86, 89, 90, 91, 92, 93, 94, 95, 102, 103, 104, 105, 106, 107, 108, 109, 110, 117, 118, 129, 135, 140, 141, 145, 147, 161, 163, 165, 171, 178, 179, 188, 205, 208, 222, 224, 226, 228, 229, 231, 232, 233, 241, 242, 243, 246, 252, 255, 256, 259… | Labs: 1, 6, 7, 8, 9, 15, 17, 21, 23, 26, 27, 28, 29, 30, 31, 32, 33, 34, 35, 36, 37, 38, 39, 40, 41, 42, 43, 44, 45, 46, 47, 48, 49, 62, 65, 66, 67, 69, 70, 71, 72, 73, 74, 76, 79, 80, 81, 82, 86, 87, 88, 89, 98, 100, 101, 102, 103, 104, 105, 108… | Padriseup: 1, 2, 5, 6, 7, 8, 11, 12, 13, 15, 18, 19, 25, 28
- **RST** — Textbook: 17, 18, 20, 31, 40, 59, 63, 64, 69, 75, 76, 82, 93, 95, 97, 99, 102, 106, 109, 110, 118, 124, 136, 138, 142, 149, 171, 184, 187, 195, 206, 207, 209, 211 | Slides: 34, 35, 37, 39, 66, 78, 92, 129, 130, 140, 147, 165, 181, 210, 215, 220, 225, 232, 249, 250, 261, 277, 296, 334, 354, 356, 362, 412, 416, 452, 457, 461, 479, 503, 506, 515, 519 | Labs: 19, 22, 23, 24, 28, 30, 31, 32, 37, 48, 72, 83, 110, 125, 126, 129, 152, 153, 166, 167, 168, 170, 188, 204, 212, 233, 258, 265 | Padriseup: 1, 4, 5, 6, 7, 10
- **FIN** — Textbook: 5, 18, 20, 30, 32, 34, 37, 40, 41, 48, 53, 58, 81, 83, 84, 91, 93, 94, 95, 105, 109, 110, 115, 122, 125, 129, 137, 139, 141, 145, 154, 157, 160, 172, 174, 185, 186, 190, 196, 211, 212, 213 | Slides: 6, 12, 29, 31, 37, 39, 63, 68, 73, 83, 86, 92, 93, 94, 105, 109, 117, 178, 179, 184, 185, 186, 203, 212, 215, 238, 249, 250, 263, 270, 287, 297, 307, 331, 339, 349, 368, 383, 392, 411, 418, 424, 446, 448, 456, 460, 467, 488, 492, 509, 519, 521, 522 | Labs: 9, 10, 22, 23, 24, 31, 39, 43, 49, 73, 89, 90, 114, 134, 151, 172, 190, 206, 214, 215, 235 | Padriseup: 2, 7, 8 | Cisco project: 6, 9
- **PSH** — Textbook: 40 | Slides: 92
- **URG** — Textbook: 40, 180 | Slides: 92, 440
- **3-Way Handshake** — Textbook: 40, 41, 45 | Slides: 92, 93, 100 | Labs: 28 | Padriseup: 7
- **Logical Ports** — Textbook: 2, 38, 42, 44, 45, 59, 201 | Slides: 59, 78, 87, 88, 89, 90, 91, 92, 93, 94, 95, 96, 97, 98, 100, 225, 493 | Labs: 28, 32
- **Wireshark** — Textbook: 2, 46, 47, 53, 55, 172 | Slides: 59, 101, 102, 103, 104, 105, 106, 107, 108, 109, 110, 112, 417 | Labs: 15, 16, 18, 19, 20, 21, 23, 24, 25, 26, 30, 31 | Padriseup: 7, 10, 11
- **pcap** — Textbook: 50, 52 | Slides: 103, 108 | Labs: 20, 21, 22, 23, 31 | Padriseup: 11
- **pcapng** — Textbook: 50 | Slides: 103
- **Packet List** — Textbook: 47 | Slides: 104
- **Packet Details** — Textbook: 47 | Slides: 104
- **Packet Bytes** — Textbook: 47, 51 | Slides: 104
- **Cisco IOS** — Textbook: 2, 75, 100, 204 | Slides: 134, 136, 170, 228, 498 | Labs: 48
- **Packet Tracer** — Textbook: 184 | Slides: 140, 141, 161, 171, 188, 205, 246, 256, 315, 354, 370, 407, 452, 476, 506 | Labs: 34, 35, 36, 37, 38, 39, 40, 41, 42, 43, 44, 46, 48, 49, 65, 69, 72, 73, 74, 87, 88, 89, 98, 102, 112, 113, 114, 132, 133, 134, 143, 144, 145, 149, 150, 151, 170, 171, 172, 176, 188, 189, 190, 204, 205, 206, 212, 213, 214, 233, 234, 235, 247, 248, 249, 257
- **User EXEC** — Textbook: 68 | Slides: 145 | Labs: 53, 54
- **Privileged EXEC** — Textbook: 70, 73 | Slides: 145, 146, 149 | Labs: 53, 56, 66, 81, 119, 120
- **Global Configuration** — Textbook: 69 | Slides: 146 | Labs: 53, 57, 136, 139, 140, 153, 192, 226, 229
- **POST** — Textbook: 50, 70, 71 | Slides: 107, 110, 150, 151 | Labs: 53
- **ROMmon** — Textbook: 78, 79 | Slides: 167
- **configuration register** — Textbook: 78, 79, 80 | Slides: 167, 169, 170
- **TFTP** — Textbook: 37, 44, 76, 77, 80 | Slides: 98, 163, 164, 165, 166, 171 | Labs: 72, 76, 79, 80, 81, 82, 83, 237, 240, 241, 242
- **Port Security** — Textbook: 2, 81, 82, 83, 84, 85 | Slides: 176, 177, 178, 179, 180, 181, 182, 183, 184, 185, 186, 188 | Labs: 87, 90, 92, 95, 96, 97, 104, 105, 106, 109, 110
- **sticky** — Textbook: 82, 84, 85 | Slides: 181, 186, 187 | Labs: 93, 96, 97, 104, 106 | Padriseup: 13, 14 | Cisco project: 6
- **shutdown** — Textbook: 81, 82, 85, 90, 100, 101, 110, 211 | Slides: 180, 182, 187, 201, 227, 229, 251, 442, 450, 519 | Labs: 60, 93, 94, 95, 97, 100, 117, 139, 146, 147, 154, 229, 240, 253, 256, 260, 263 | Padriseup: 13, 14, 16, 17, 28 | Cisco project: 3, 5, 7
- **restrict** — Textbook: 64, 81, 82, 84, 85, 188, 189 | Slides: 131, 179, 180, 186, 187, 462, 463, 464, 465 | Labs: 93, 95, 96, 107 | Padriseup: 14 | Cisco project: 6
- **protect** — Textbook: 12, 81, 82, 188 | Slides: 24, 180 | Labs: 87, 93, 95, 107, 109, 110 | Padriseup: 14 | Cisco project: 2
- **Telnet** — Textbook: 37, 67, 86, 90, 159, 182, 196, 197 | Slides: 83, 139, 142, 190, 191, 200, 443 | Labs: 54, 123 | Padriseup: 12
- **VTY** — Textbook: 88, 89, 90 | Slides: 160, 195, 198, 200 | Labs: 60, 118, 121 | Padriseup: 12 | Cisco project: 8, 9
- **SVI** — Textbook: 2, 88, 90, 159 | Slides: 197, 381
- **RSA** — Textbook: 2, 9, 20, 33, 40, 52, 54, 67, 77, 86, 87, 91, 92, 112, 208 | Slides: 15, 40, 70, 92, 108, 110, 139, 166, 191, 192, 193, 202, 204, 255, 373, 508 | Labs: 12, 105, 112, 116, 119, 123 | Padriseup: 5, 13 | Cisco project: 8, 9
- **SSH version 2** — Labs: 119 | Padriseup: 15 | Cisco project: 8, 9
- **Decimal** — Textbook: 17, 18, 47, 93, 94, 95, 96, 97, 109, 191 | Slides: 35, 36, 104, 210, 211, 212, 213, 214, 215, 216, 217, 218, 219, 220, 249, 471, 480 | Labs: 124, 125, 126, 127, 129, 130, 138, 162
- **Binary** — Textbook: 32, 59, 93, 94, 95, 96, 97, 105, 114, 115, 116, 132, 151, 189 | Slides: 68, 78, 210, 211, 212, 213, 214, 215, 216, 217, 218, 219, 220, 238, 267, 272, 273, 313, 466 | Labs: 124, 125, 126, 127, 129, 130, 162, 184
- **Hexadecimal** — Textbook: 17, 18, 47, 93, 96, 97, 109 | Slides: 35, 36, 104, 212, 217, 218, 219, 249 | Labs: 125, 129, 130
- **Routing table** — Textbook: 102, 103, 104, 124, 125, 127, 128, 129, 130, 135, 136, 138, 139, 141, 143, 145, 147, 152, 154, 157 | Slides: 231, 234, 235, 296, 297, 298, 302, 303, 305, 307, 309, 321, 344, 345, 349, 352, 365 | Labs: 139, 140, 173, 174, 177, 178, 180, 181, 184, 185, 191, 196, 200, 201, 202
- **Static Route** — Textbook: 103, 104, 127, 128, 129, 130, 131, 133, 135, 137, 139 | Slides: 234, 235, 302, 305, 307, 308, 309, 312, 315, 317, 320, 332 | Labs: 173, 174, 175, 176, 177, 178, 180, 181, 184, 200, 201 | Padriseup: 23 | Cisco project: 3
- **Default Route** — Textbook: 128, 129, 133, 148 | Slides: 305, 306, 315, 353, 354, 370 | Labs: 169, 170, 178, 180, 181, 182, 188, 200, 201, 202, 209
- **Floating Static Route** — Textbook: 130 | Slides: 309
- **Summary Route** — Slides: 315 | Labs: 184, 185
- **Administrative Distance** — Textbook: 129, 137, 140, 142 | Slides: 307, 332, 344 | Labs: 173, 191
- **RIP** — Textbook: 3, 21, 103, 104, 129, 137, 138, 139, 141, 142, 143, 144, 145, 146, 147, 148, 149, 150, 173, 181 | Slides: 42, 110, 234, 235, 308, 326, 330, 332, 334, 335, 340, 341, 342, 343, 344, 345, 346, 347, 348, 349, 351, 354, 356, 358, 421, 442, 443 | Labs: 6, 7, 8, 9, 20, 30, 65, 91, 105, 108, 118, 145, 146, 147, 157, 159, 160, 175, 179, 180, 181, 183, 186, 187, 188, 191, 192, 193, 194, 195, 196, 197, 198, 199, 200, 201, 202, 222, 227, 231, 238, 239, 243, 245, 254, 257, 261 | Padriseup: 20, 21, 22, 23 | Cisco project: 3
- **RIPv2** — Textbook: 3, 141, 142, 144, 145, 146, 148 | Slides: 326, 340, 341, 342, 343, 344, 345, 346, 347, 354 | Labs: 187, 188, 192, 200
- **RIPng** — Textbook: 142 | Slides: 343
- **OSPF** — Textbook: 103, 104, 129, 137, 138, 139, 140, 141, 146, 149, 150, 151, 152, 153, 154, 155, 157 | Slides: 228, 234, 235, 307, 308, 326, 330, 332, 334, 335, 340, 351, 355, 356, 357, 358, 359, 360, 361, 362, 363, 364, 365, 366, 367, 368, 369, 370 | Labs: 175, 180, 181, 200, 201, 203, 204, 207, 208, 209, 210 | Padriseup: 19, 22, 23, 24, 25 | Cisco project: 3, 7, 8
- **OSPFv2** — Textbook: 149, 150, 151, 152, 153, 155 | Slides: 326, 355, 356, 357, 358, 359, 360, 362, 363, 364, 365, 366, 370 | Labs: 203
- **SPF** — Textbook: 103, 104, 129, 137, 138, 139, 140, 141, 146, 149, 150, 151, 152, 153, 154, 155, 157 | Slides: 228, 234, 235, 307, 308, 326, 330, 332, 334, 335, 340, 351, 355, 356, 357, 358, 359, 360, 361, 362, 363, 364, 365, 366, 367, 368, 369, 370 | Labs: 82, 175, 180, 181, 200, 201, 203, 204, 207, 208, 209, 210 | Padriseup: 19, 22, 23, 24, 25 | Cisco project: 3, 7, 8
- **Link State** — Textbook: 138, 149, 150 | Slides: 335, 337, 356, 358, 359
- **Distance Vector** — Textbook: 138, 142 | Slides: 335, 336
- **IGP** — Slides: 335
- **EGP** — Textbook: 103, 139 | Slides: 234, 335 | Labs: 175, 180, 181, 200, 201 | Padriseup: 23 | Cisco project: 3
- **Passive Interface** — Textbook: 141, 146, 155 | Slides: 338, 351, 369 | Labs: 196, 197, 198 | Cisco project: 7
- **Router ID** — Textbook: 151, 154, 155 | Slides: 362, 369 | Labs: 207, 250
- **Area 0** — Textbook: 151, 152, 155 | Slides: 364 | Labs: 207, 208 | Padriseup: 24, 25 | Cisco project: 7
- **VLAN** — Textbook: 3, 62, 85, 88, 90, 110, 157, 158, 159, 160, 161, 162, 163, 164, 165, 166, 167, 168, 169, 170, 174 | Slides: 2, 58, 122, 126, 175, 187, 196, 197, 201, 209, 251, 260, 292, 325, 374, 375, 376, 377, 378, 379, 380, 381, 382, 383, 384, 385, 386, 387, 388, 389, 390, 391, 395, 397, 398, 399, 400, 401, 402, 403, 405, 406, 407, 426 | Labs: 60, 67, 68, 92, 97, 106, 117, 121, 146, 147, 154, 158, 211, 212, 215, 216, 217, 218, 219, 220, 224, 225, 226, 229, 230, 240, 260 | Padriseup: 12, 17, 25, 26, 27, 28 | Cisco project: 1, 2, 6
- **Trunk** — Textbook: 157, 158, 160, 163, 164, 165, 166, 167, 169, 170 | Slides: 2, 58, 122, 175, 209, 260, 292, 325, 374, 375, 376, 383, 388, 389, 390, 391, 392, 393, 395, 396, 397, 398, 399, 400, 404, 407 | Labs: 211, 212, 215, 224, 225, 226, 229 | Padriseup: 27, 28 | Cisco project: 2, 6
- **802.1Q** — Textbook: 160, 163, 165, 169 | Slides: 383, 390, 399, 405 | Labs: 226, 229, 230 | Cisco project: 6
- **DTP** — Textbook: 159, 163, 164, 165, 166 | Slides: 381, 391, 392, 393, 394, 395, 397 | Labs: 55
- **Native VLAN** — Textbook: 159, 166, 167, 174 | Slides: 381, 391, 397, 398, 399, 407, 426 | Labs: 224, 225, 226 | Padriseup: 28 | Cisco project: 2, 6
- **Voice VLAN** — Textbook: 159, 161, 162 | Slides: 381, 387 | Cisco project: 2
- **Management VLAN** — Textbook: 159 | Slides: 381
- **Inter-VLAN** — Textbook: 3, 88, 168, 169 | Slides: 197, 375, 400, 401, 402, 407 | Labs: 229, 230
- **Router-on-a-stick** — Textbook: 168 | Slides: 402
- **Sub-interface** — Textbook: 88, 168, 169 | Slides: 197, 403, 405 | Labs: 229, 230
- **Troubleshooting** — Textbook: 3, 20, 171, 172, 179, 185, 186, 209 | Slides: 2, 41, 58, 122, 175, 209, 260, 292, 325, 374, 410, 411, 412, 413, 414, 415, 416, 417, 418, 419, 420, 422, 434, 435, 445, 448, 456, 488, 512 | Labs: 56, 95, 120, 149, 216, 232 | Padriseup: 16
- **CDP** — Textbook: 3, 159, 166, 174, 175, 176, 177 | Slides: 381, 397, 398, 412, 423, 424, 425, 426, 427, 428, 429, 430, 432, 433 | Labs: 55
- **LLDP** — Textbook: 174, 177, 178 | Slides: 430, 431, 432, 433
- **Syslog** — Textbook: 3, 179, 180, 181, 182, 183, 184, 186, 187 | Slides: 412, 434, 435, 436, 437, 438, 439, 440, 441, 443, 444, 448, 452 | Labs: 79, 80, 82, 232, 233, 236, 237, 238, 240, 241, 242, 245, 249 | Cisco project: 5
- **NTP** — Textbook: 3, 44, 185, 186, 187 | Slides: 98, 446, 447, 448, 450, 451, 452 | Labs: 80, 134, 151, 172, 190, 206, 214, 232, 233, 236, 240, 241, 242, 243, 244, 245 | Cisco project: 5
- **ACL** — Textbook: 3, 98, 188, 189, 190, 191, 192, 193, 194, 195, 196, 197, 198, 199, 200, 211, 212 | Slides: 222, 457, 458, 459, 460, 462, 463, 464, 465, 466, 467, 468, 469, 470, 471, 472, 473, 474, 475, 476, 477, 478, 479, 480, 481, 482, 483, 484, 521 | Labs: 26, 246, 247, 250, 251, 252, 253, 255, 256, 257, 258, 259, 262, 263, 264, 265 | Padriseup: 28, 29, 30
- **Standard ACL** — Textbook: 3, 189, 191, 192, 212 | Slides: 457, 464, 466, 468, 469, 470, 472, 521 | Labs: 250, 251, 252, 255
- **Extended ACL** — Textbook: 3, 189, 194, 195, 197, 198, 199, 200 | Slides: 457, 464, 476, 477, 478, 479, 480, 481 | Labs: 246, 247, 257, 258, 259, 262, 265
- **Stateful** — Textbook: 203 | Slides: 461, 500 | Labs: 250
- **Stateless** — Textbook: 36, 203 | Slides: 82, 461, 499, 500 | Labs: 250
- **NAT** — Textbook: 2, 3, 6, 7, 8, 10, 15, 23, 29, 30, 31, 32, 33, 36, 37, 39, 40, 41, 42, 48, 49, 50, 51, 52, 53, 55, 56, 57, 58, 59, 60, 62, 63, 67, 68, 77, 78, 86, 93, 97, 98, 102, 103, 105, 106, 107, 111, 112, 122, 124, 125, 127, 129, 131, 134, 136, 137, 138, 139, 140… | Slides: 10, 12, 14, 16, 19, 30, 31, 45, 62, 64, 66, 68, 71, 72, 76, 77, 78, 79, 81, 84, 85, 91, 92, 94, 95, 105, 107, 108, 109, 112, 114, 115, 116, 118, 125, 129, 143, 161, 165, 166, 168, 193, 210, 212, 219, 222, 224, 231, 232, 233, 234, 237, 241, 252, 255, 270, 286, 288, 295, 296… | Labs: 5, 7, 15, 17, 18, 21, 27, 28, 29, 32, 33, 41, 43, 54, 55, 63, 65, 69, 78, 79, 80, 81, 82, 83, 97, 106, 137, 138, 139, 141, 173, 174, 180, 181, 193, 194, 195, 200, 202, 209, 224, 225, 226, 227, 250, 252, 254, 257, 260 | Padriseup: 1, 3, 6, 16, 20, 21, 22, 23, 28 | Cisco project: 1, 2, 6
- **PAT** — Textbook: 27, 33, 37, 55, 102, 115, 124, 125, 126, 129, 130, 131, 136, 137, 138, 139, 140, 142, 145, 147, 149, 152, 154, 155, 173, 209, 211, 213 | Slides: 53, 72, 85, 119, 172, 231, 269, 295, 297, 299, 300, 307, 309, 312, 331, 333, 334, 335, 336, 349, 351, 356, 360, 368, 369, 421, 511, 512, 515, 519, 522 | Labs: 6, 22, 23, 41, 44, 173, 179, 183, 196, 197, 198
- **NAT64** — Textbook: 209 | Slides: 516
- **SLAAC** — Textbook: 203 | Slides: 499, 500
- **DHCPv6** — Textbook: 201, 203 | Slides: 493, 499, 500 | Labs: 80, 82, 240, 241
- **DHCP relay** — Textbook: 207 | Slides: 504
- **ip helper-address** — Textbook: 207 | Slides: 504
- **ping** — Textbook: 21, 33, 48, 70, 173, 174, 209, 214 | Slides: 42, 72, 105, 149, 421, 424, 515, 523 | Labs: 6, 7, 8, 14, 30, 33, 54, 65, 91, 94, 99, 103, 104, 105, 107, 108, 109, 118, 145, 146, 147, 156, 157, 159, 160, 174, 179, 180, 183, 186, 199, 200, 202, 222, 223, 227, 228, 231, 238, 239, 243, 245, 254, 257, 260, 261, 264 | Padriseup: 5, 6, 16, 19 | Cisco project: 2
- **ipconfig** — Textbook: 21, 22 | Slides: 43 | Labs: 4, 5, 31, 32, 94, 143, 144 | Padriseup: 5
- **ifconfig** — Padriseup: 5
- **nslookup** — Textbook: 22 | Slides: 44 | Labs: 2, 10, 11 | Padriseup: 6
- **tracert** — Textbook: 23, 33 | Slides: 45, 72 | Labs: 6, 7, 8, 179, 183 | Padriseup: 6
- **netsh** — Textbook: 24 | Slides: 46 | Labs: 12, 13 | Padriseup: 6
- **netstat** — Textbook: 44, 45 | Slides: 99
- **arp -a** — Textbook: 57 | Slides: 116 | Padriseup: 10
- **route print** — Padriseup: 18
- **CloudShark** — Padriseup: 12
- **PuTTY** — Textbook: 66, 67, 92, 180 | Slides: 138, 139, 204, 438 | Labs: 53