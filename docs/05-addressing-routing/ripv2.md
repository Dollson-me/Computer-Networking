# RIPv2

[← Indeks wiki](../index.md)

> **Źródło główne:** Computer Networking Textbook.pdf, s. 141–148. Treść została uporządkowana tematycznie; pełny ekstrakt źródłowy znajduje się w `_source-archive/`.


## Materiał kanoniczny

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

## Powiązane laboratoria

- [NET-08-LS1](../labs/net-08-ls1.md)


## Uzupełnienia z notatek Riseup / zajęć

<details>
<summary>Pokaż notatki prowadzącego, dodatkowe komendy i linki powiązane z tym tematem</summary>

S1(config)#username Admin password p@nd@
S1(config)#enable password c!sc0
S1(config)#ip ssh version 2
S1(config)#do show ip ssh

02.09.2023

---

Enter configuration commands, one per line. End with CNTL/Z.
R1(config)#router rip
R1(config-router)#version 2
R1(config-router)#no auto-summary
R1(config-router)#network 172.16.0.0
R1(config-router)#network 172.16.0.8
R1(config-router)#network 192.168.10.0

---

R1>en
R1#conf t
R1(config)#router rip
R1(config-router)#version 2
R1(config-router)#no auto-summary
R1(config-router)#network 172.16.0.0
R1(config-router)#network 172.16.0.8
R1(config-router)#network 192.168.10.0

---

C 192.168.20.0/24 is directly connected, GigabitEthernet0/0
R2#conf t
R2(config)#router rip
R2(config-router)#version 2
R2(config-router)#no auto-summary
R2(config-router)#network 172.16.0.0
R2(config-router)#network 172.16.0.4
R2(config-router)#network 192.168.20.0

---

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

---

R3#
R3#conf t
R3(config)#router rip
R3(config-router)#default-information originate
R3(config-router)#exit
R3(config)#
https://www.ciscopress.com/articles/article.asp?p=2294214&seqNum=2

</details>

## Powiązane tematy

- [Dynamic routing concepts](dynamic-routing-concepts.md)
- [OSPFv2](ospfv2.md)
- [IPv4 static and default routing](static-routing-ipv4.md)

## Źródła w zestawie

- `Computer Networking Textbook.pdf` — strony 141–148.
- `Computer Networking.pdf` — prezentacja kursowa; odpowiadający rozdział zachowany w `_source-archive/02-Course-Slides.md`.
- `Padriseup Computer Networking.pdf` — uzupełnienia i materiały dodatkowe, jeśli występowały dla tego tematu.
