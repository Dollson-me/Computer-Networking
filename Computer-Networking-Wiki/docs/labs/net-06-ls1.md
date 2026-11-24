# NET-06-LS1 — Subnetting Practice

[← Wszystkie laboratoria](index.md)

> **Typ:** laboratorium z rozwiązaniem. Zachowano wszystkie kroki, pytania, odpowiedzi, komendy i wartości z materiału źródłowego; usunięto jedynie techniczne nagłówki stron OCR.

## Powiązana teoria

- [Subnetting](../05-addressing-routing/subnetting.md)
- [CIDR and prefix notation](../05-addressing-routing/cidr.md)
- [VLSM](../05-addressing-routing/vlsm.md)
- [Network address scheme design](../05-addressing-routing/address-scheme-design.md)

## Pełny przebieg laboratorium

> Zakres źródłowy: strony 161–168.

Computer Networking
Lab Assignment Subnetting
& Solution Concepts
ocnae NET-06-LS1
ol Subnetting Practice

EI
Copyright © 1996-2021 HackerU Ltd.
All Rights Reserved.

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
