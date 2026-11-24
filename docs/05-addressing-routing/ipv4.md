# IPv4 addressing

[← Indeks wiki](../index.md)

> **Źródło główne:** Computer Networking Textbook.pdf, s. 105–108. Treść została uporządkowana tematycznie; pełny ekstrakt źródłowy znajduje się w `_source-archive/`.


## Materiał kanoniczny

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

## Powiązane laboratoria

- [NET-05-LS2](../labs/net-05-ls2.md)


## Uzupełnienia z notatek Riseup / zajęć

<details>
<summary>Pokaż notatki prowadzącego, dodatkowe komendy i linki powiązane z tym tematem</summary>

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

---

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

---

R1(config-if)#exit
R1(config)#
https://www.browserling.com/tools/ip-to-bin
https://www.browserling.com/tools/bin-to-ip

https://42.pl/ipcalc/
do pobrania na następne zajęcia:
https://beyond.hackampus.com/canvas/general/general-YbaTH-2021.12.12.10.36.21-NET-0
7-L1.rar

---

https://pasja-informatyki.pl/sieci-komputerowe/
https://42.pl/ipcalc/
https://beyond.hackampus.com/canvas/general/general-1izuf-2021.12.12.10.42.45-NET-09-
L1.rar
S2#conf t

</details>

## Powiązane tematy

- [Subnetting](subnetting.md)
- [CIDR and prefix notation](cidr.md)
- [IPv6 addressing](ipv6.md)

## Źródła w zestawie

- `Computer Networking Textbook.pdf` — strony 105–108.
- `Computer Networking.pdf` — prezentacja kursowa; odpowiadający rozdział zachowany w `_source-archive/02-Course-Slides.md`.
- `Padriseup Computer Networking.pdf` — uzupełnienia i materiały dodatkowe, jeśli występowały dla tego tematu.
