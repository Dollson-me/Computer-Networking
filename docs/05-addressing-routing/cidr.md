# CIDR and prefix notation

[← Indeks wiki](../index.md)

> **Źródło główne:** Computer Networking Textbook.pdf, s. 115–119. Treść została uporządkowana tematycznie; pełny ekstrakt źródłowy znajduje się w `_source-archive/`.


## Materiał kanoniczny

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

## Powiązane laboratoria

- [NET-06-LS1](../labs/net-06-ls1.md)


## Uzupełnienia z notatek Riseup / zajęć

<details>
<summary>Pokaż notatki prowadzącego, dodatkowe komendy i linki powiązane z tym tematem</summary>

https://www.soisk-me.pl/klasa-iv-sieci/klasy-adresow-ip
http://www.lomilowka.pl/upload/file/PiMLSK/klasyadres%C3%B3wIP.pdf
#Maska podsieci
https://pl.wikipedia.org/wiki/Maska_podsieci
Standardy sieci WiFi
https://snipboard.io/rvm902.jpg

---

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
- [VLSM](vlsm.md)
- [Network address scheme design](address-scheme-design.md)

## Źródła w zestawie

- `Computer Networking Textbook.pdf` — strony 115–119.
- `Computer Networking.pdf` — prezentacja kursowa; odpowiadający rozdział zachowany w `_source-archive/02-Course-Slides.md`.
- `Padriseup Computer Networking.pdf` — uzupełnienia i materiały dodatkowe, jeśli występowały dla tego tematu.
