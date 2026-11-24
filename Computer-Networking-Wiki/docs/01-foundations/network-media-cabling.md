# Network media and cabling

[← Indeks wiki](../index.md)

> **Źródło główne:** Computer Networking Textbook.pdf, s. 11–13. Treść została uporządkowana tematycznie; pełny ekstrakt źródłowy znajduje się w `_source-archive/`.


## Materiał kanoniczny

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

## Powiązane laboratoria

- Brak bezpośrednio przypisanego laboratorium w zestawie.


## Uzupełnienia z notatek Riseup / zajęć

<details>
<summary>Pokaż notatki prowadzącego, dodatkowe komendy i linki powiązane z tym tematem</summary>

Sieć - grupa komputerów lub innych urządzeń, które są w stanie komunikować się ze
sobą. Sieć może być tworzona z pomocą fizycznych kabli (skrętka ethernet, światłowód,
kabel koncentrytczny etc.) lub za pomocą technologii bezprzewodowych. Sieci komputerowe
mogą różnić się rozmiarami (np. LAN, WAN) lub dostarczać określonych usług (np. centra
danych, serwerownie) oraz łączyć ze sobą komputery z różnych zakątków świata.

---

IoT

- medium transmisyjne - uczestniczy w przekazywaniu informacji np. skrętka lub sieć
bezprzewodowa
#Urządzenia sieciowe

---

- Acess Point (AP) - łączy sieć bezprzewodową z siecią LAN
#Kabel ethernet == skrętka ethernet

- różne kategorie o różnych prędkościach
 * CAT-5 - do 100Mb/s, do 100m
 * CAT-5e - do 1Gb/s, do 100m
 * CAT-6 - do 1Gb/s, do 100m lub 10Gb/s do 55m
 * CAT-6a - do 10Gb/s do 100m
 * CAT-7 - do 10Gb/s do 100m lub 100Gb/s do 50m

- kable:
 * nieekranowany (UTP) - najczęściej stosowany typ kabla, 4 pary skręconych
przewodów zabieg ten niweluje zakłócenia
 * ekranowany (STP) - kabel z ekranem wokół przewodów, eliminuje zewnętrzne
zakłócenia elektro-magnetyczne
#Mapa kabli podwodnych:

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

---

https://pl.wikipedia.org/wiki/Strefa_Fresnela
Kalkulator:
https://www.bestpartner.pl/index.php?d=kfresnel
I ciekawostka - chyba nic nie tłumi lepiej sygnału elektromagnetycznego niż drzewo liściaste
:)
Ping - używa protokołu ICMP - Internet Control Message Protocol, dosł. internetowy protokół

---

#Sieci bezprzewodowe
Oparte o technologie bezprzewodowe (fale radiowe). Ich rozpowrzechnienie wprowadziło
nowe zagrożenia, z powodu braku fizycznego nośnika danych (skrętka ethernetowa).
Podstawowym zabezpieczeniem było filtrowanie urządzeń na podstawie adresów MAC
(przyłączyć do sieci mogło się urządzenie z listy dozwolonych urządzeń) jednak ten sposób
zabezpieczenia jest łatwy do obejścia. Aktualnie, w dużej części, problemy z

---

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

</details>

## Powiązane tematy

- [Network types and devices](network-types-devices.md)
- [Network topologies and architecture](network-topologies-architecture.md)

## Źródła w zestawie

- `Computer Networking Textbook.pdf` — strony 11–13.
- `Computer Networking.pdf` — prezentacja kursowa; odpowiadający rozdział zachowany w `_source-archive/02-Course-Slides.md`.
- `Padriseup Computer Networking.pdf` — uzupełnienia i materiały dodatkowe, jeśli występowały dla tego tematu.
