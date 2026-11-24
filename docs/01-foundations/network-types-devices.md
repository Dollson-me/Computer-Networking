# Network types and devices

[← Indeks wiki](../index.md)

> **Źródło główne:** Computer Networking Textbook.pdf, s. 5–10. Treść została uporządkowana tematycznie; pełny ekstrakt źródłowy znajduje się w `_source-archive/`.


## Materiał kanoniczny

Communication is an essential characteristic of any society.

In today’s world, people communicate with other people around the world almost as
simply as they talk to a person standing right beside them.

Over the past several decades, global communication has advanced significantly and
has greatly improved the human social experience.

A network is basically two or more computers that communicate with each other and
share information.

Communication over a network (networking) brings people together for either generic
or specific purposes.

___Network Types___

__LAN__ - A Local Area Network defines a small geographical area in which multiple
computers and other devices are connected. LANs can be set up in homes and small
businesses and can be managed individually or centrally.
LANs can be designed to use one of two communication methods: Wired or Wireless.

__WAN__ - A Wide Area Network is spread across an unlimited geographical area and
connects between multiple LANs. WANs are usually managed by several service
providers.

__MAN__ - A Metropolitan Area Network is larger than a LAN but smaller than a WAN. In
most cases, it is managed by a city municipality and enables connection to broader
networks.

__SAN__ - A Storage Area Network is a dedicated network that supports file servers and
provides efficient transfer of unusually large data sizes at extremely high rates.
SAN networks are usually found in large companies and data centers

___Network Structure___

The history of computer networks began in the 1960s with a network called ARPANET.

Communication among devices can be as simple as connecting a cable between two
computers. On the other hand, it can be as complex as a large assembly of multiple
networks spread around the world and regulated by an assortment of sophisticated
devices and protocols.

___Devices in a Network___

__Endpoint Devices__ - Devices that connect to a network for communication purposes,
such as computers, phones, and others. All endpoint devices have unique addresses
that identify them on the network.

__Media__ - ‘Media’, based on the word ‘medium’ (meaning ‘in between’) is a means of
transferring data, such as metallic wire, glass or plastic fiber, wireless radio frequencies,
and others.

__Intermediary Devices__ - Devices that transfer messages over the network and facilitate
communication between end devices.

___Endpoint Devices___

In today’s world, most people communicate with each other through networks.

Endpoint devices are the source or destination devices in a networked system.

Computers, laptops, and phones are endpoint devices that allow us to communicate
over a network.

Endpoint devices must have the ability to connect to a network via a NIC (Network
Interface Controller), to be able to send and receive information.

___Network Interface Controller (NIC)___

To allow an endpoint device to send and receive information over a network it must
have the appropriate hardware.

A Network Interface Controller (NIC) allows endpoint devices to interact with other
devices over a network.

Other names for NIC include:
* Network Adapter
* LAN Adapter
* Physical Network Interface

___Network Devices___

Network devices act as bridges, interconnecting endpoint devices.

Smart network devices know how to differentiate between devices, and can send data
to specific destinations.

Unlike smart devices, simple network devices send information indiscriminately across a
network.

___Switches___

For multiple endpoint devices to communicate with each other, a mechanism needs to
be set up to handle the transfers.

A switch is a network device with physical ports to which endpoint devices can be
connected via Ethernet cables to create a network.

Switches use MAC addresses to pass information from one device to another.

Switch Types
__Hub__ - Hubs were used to relay data to multiple devices in a LAN. They broadcast data to
all connected devices, as opposed to a switch which sends information to dedicated destinations.

__Layer 2 Switch__ - This is the most common and basic switch in use. It uses MAC
addresses to forward information to specific destinations within the network.

__Layer 3 Switch__ - A layer 3 switch performs the same operations as a layer 2 switch, but
can also function as a router if it is configured to do so.
Switch Vs. Hub

Broadcast & Collision Domains
A Broadcast domain is a type of communication whereby the sender sends a single
copy of the data to all devices on the same network segment. Broadcast
communication must be used since protocols such as ARP and DHCP rely on it.
A broadcast domain includes devices that receive broadcast packets originating from
senders within the same network segment.
Routers operate in the network layer and separate both collision domains and
broadcast domains.

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

## Powiązane laboratoria

- [NET-01-LS1](../labs/net-01-ls1.md)


## Uzupełnienia z notatek Riseup / zajęć

<details>
<summary>Pokaż notatki prowadzącego, dodatkowe komendy i linki powiązane z tym tematem</summary>

06.08.2023
Ch1 & Ch2 - Network Introduction & Fundamentals
ARPANET https://pl.wikipedia.org/wiki/ARPANET
#Warto wspomnieć o modelu ISO/OSI i porównać z modelem TCP/IP.
https://pl.wikipedia.org/wiki/Model_OSI

---

danych, serwerownie) oraz łączyć ze sobą komputery z różnych zakątków świata.

NIC - Network Interface Controller - komponent sprzętowy, który zezwala na
połączenie się komputera do fizycznej sieci komputerowej. Każdy NIC posiada adres MAC
(unikalny identyfikator urządzenia).
Przykładowy adres MAC: 91-8D-89-2D-D5-A6 lub 00:0d:83:b1:c0:8e
gdzie pierwsze trzy segmenty identyfikują producenta
natomiast trzy ostatnie segmenty są numerem identyfikującym urządzenia
#Podziały sieci:
 - LAN (Local Area Network) - sieć niezbyt rozległa, zazwyczaj obejmuje biuro lub
dom a w jej skład wchodzi niedużo urządzeń, zarządzana z punktu jednego centralnego
 - WAN (Wide Area Network) - rozległa na kilka niegraniczonych geograficznie
obszarów, łączy kilka sieci LAN. Sieci te zazwyczaj są zarządzane przez dostawców, którzy
się tym zajmują
 - MAN (Metropolitan Area Network) - pomiędzy LAN i WAN, zazwyczaj obejmuje sieć
o rozmiarze miasta
 - SAN (Storage Area Network) - dedykowana dla optymalizacji przesyłu danych
#Architektura sieci

- Client-server - serwer udostępnia jedną lub więcej usług lub zasobów, do jednego

---

- urządzenia pośrednie (switch, router, hub)

- switch - służy do przekierowywania pakietów, aby nim zarządzać trzeba
wykorzystać zdalny terminal, typy switchy:
 * HUB - rozsyła dane wejsciowe z któregoś z portu na pozostałe,
 * switch warstwy drugiej - używa adres MAC do przekierowania danych na

---

docelowy adres IP

- router - potrafią wymieniać pakiety danych pomiędzy różymi sieciami (np. sieć
domowa i sieć globalna internet)

- Acess Point (AP) - łączy sieć bezprzewodową z siecią LAN
#Kabel ethernet == skrętka ethernet

- różne kategorie o różnych prędkościach

</details>

## Powiązane tematy

- [Network media and cabling](network-media-cabling.md)
- [Network topologies and architecture](network-topologies-architecture.md)
- [Network protocols and Windows commands](network-protocols-commands.md)

## Źródła w zestawie

- `Computer Networking Textbook.pdf` — strony 5–10.
- `Computer Networking.pdf` — prezentacja kursowa; odpowiadający rozdział zachowany w `_source-archive/02-Course-Slides.md`.
- `Padriseup Computer Networking.pdf` — uzupełnienia i materiały dodatkowe, jeśli występowały dla tego tematu.
