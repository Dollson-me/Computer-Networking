# IPv4 static and default routing

[← Indeks wiki](../index.md)

> **Źródło główne:** Computer Networking Textbook.pdf, s. 127–133. Treść została uporządkowana tematycznie; pełny ekstrakt źródłowy znajduje się w `_source-archive/`.


## Materiał kanoniczny

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

‘ Lab — Configuring IPv4 Static and Default Routes
= | Implement IPv4 standard and default static routes in a full network
=== | topology.
Perform the instructions in document Net-07-L1.

## Powiązane laboratoria

- [NET-07-LS1](../labs/net-07-ls1.md)


## Uzupełnienia z notatek Riseup / zajęć

<details>
<summary>Pokaż notatki prowadzącego, dodatkowe komendy i linki powiązane z tym tematem</summary>

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

---

R2>en
R2#show ip route connected
C 172.16.0.0/30 is directly connected, Serial0/3/0
C 172.16.0.4/30 is directly connected, Serial0/3/1
C 192.168.20.0/24 is directly connected, GigabitEthernet0/0

---

R2#
R3>en
R3#show ip route connected
C 172.16.0.4/30 is directly connected, Serial0/3/1
C 172.16.0.8/30 is directly connected, Serial0/3/0
C 192.168.30.0/24 is directly connected, GigabitEthernet0/0

---

Building configuration...
[OK]
R3#show ip route rip
R3>enable
R3#conf t
R3(config)#ip route 0.0.0.0 0.0.0.0 serial 0/2/0
R3(config)#exit
R3#show ip route
Codes: L - local, C - connected, S - static, R - RIP, M - mobile, B - BGP

---

R3>enable
R3#conf t
R3(config)#ip route 0.0.0.0 0.0.0.0 serial 0/2/0
R3(config)#exit
R3#show ip route
Codes: L - local, C - connected, S - static, R - RIP, M - mobile, B - BGP

---

R2(config)#
R2(config)#exit
R2#show ip route ospf

172.16.0.0/16 is variably subnetted, 5 subnets, 2 masks
O

</details>

## Powiązane tematy

- [Router operation and static routing concepts](router-operation.md)
- [IPv6 static routing](static-routing-ipv6.md)
- [Dynamic routing concepts](dynamic-routing-concepts.md)

## Źródła w zestawie

- `Computer Networking Textbook.pdf` — strony 127–133.
- `Computer Networking.pdf` — prezentacja kursowa; odpowiadający rozdział zachowany w `_source-archive/02-Course-Slides.md`.
- `Padriseup Computer Networking.pdf` — uzupełnienia i materiały dodatkowe, jeśli występowały dla tego tematu.
