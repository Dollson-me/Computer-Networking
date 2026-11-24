# Network topologies and architecture

[← Indeks wiki](../index.md)

> **Źródło główne:** Computer Networking Textbook.pdf, s. 14–19. Treść została uporządkowana tematycznie; pełny ekstrakt źródłowy znajduje się w `_source-archive/`.


## Materiał kanoniczny

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

## Powiązane laboratoria

- Brak bezpośrednio przypisanego laboratorium w zestawie.


## Uzupełnienia z notatek Riseup / zajęć

<details>
<summary>Pokaż notatki prowadzącego, dodatkowe komendy i linki powiązane z tym tematem</summary>

o rozmiarze miasta
 - SAN (Storage Area Network) - dedykowana dla optymalizacji przesyłu danych
#Architektura sieci

- Client-server - serwer udostępnia jedną lub więcej usług lub zasobów, do jednego
lub wielu klientów. Przykładowe usługi: SMTP, FTP, WWW, Samba itd. Klient zawsze
rozpoczyna komunikację i wysyła żądania (request) o dostęp do zasobów. Serwer
odpowiada na żądanie udostępniająć żądany zasób.

---

https://blog.laptopcontrol.pl/informatyka/kategorie-kabel-sieciowy-lan-skretka/

#Topologie sieci
https://pasja-informatyki.pl/sieci-komputerowe/topologie-sieci/
#RIR
https://pl.wikipedia.org/wiki/Regional_Internet_Registry

</details>

## Powiązane tematy

- [Network types and devices](network-types-devices.md)
- [IPv4 addressing](../05-addressing-routing/ipv4.md)
- [Subnetting](../05-addressing-routing/subnetting.md)

## Źródła w zestawie

- `Computer Networking Textbook.pdf` — strony 14–19.
- `Computer Networking.pdf` — prezentacja kursowa; odpowiadający rozdział zachowany w `_source-archive/02-Course-Slides.md`.
- `Padriseup Computer Networking.pdf` — uzupełnienia i materiały dodatkowe, jeśli występowały dla tego tematu.
