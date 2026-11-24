# OSPFv2

[← Indeks wiki](../index.md)

> **Źródło główne:** Computer Networking Textbook.pdf, s. 149–157. Treść została uporządkowana tematycznie; pełny ekstrakt źródłowy znajduje się w `_source-archive/`.


## Materiał kanoniczny

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



Security - Packet sniffing software can be used to intercept packets that include routing
updates, and redirect traffic by corrupting the routing table with false metrics.
E Lab Assignment — NET-08-LS2 Configuring & Verifying OSPF
4 | Learn how to configure VLANs and trunks.
Perform the instructions in lab document NET-08-L2.

## Powiązane laboratoria

- [NET-08-LS2](../labs/net-08-ls2.md)


## Uzupełnienia z notatek Riseup / zajęć

<details>
<summary>Pokaż notatki prowadzącego, dodatkowe komendy i linki powiązane z tym tematem</summary>

R0#conf t

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

R2(config-router)#network 192.168.2.0 0.0.0.255 area 0
R2(config-router)#network 172.16.0.4 0.0.0.3 area 0
R2(config-router)#network 172.16.0.0 0.0.0.3 area 0
R2(config-router)#auto-cost reference-bandwidth 1000
R2(config-router)#passive-interface gigabitEthernet 0/1
R2(config-router)#exit
R2(config)#
R2(config)#exit
R2#show ip route ospf

172.16.0.0/16 is variably subnetted, 5 subnets, 2 masks
O

</details>

## Powiązane tematy

- [Dynamic routing concepts](dynamic-routing-concepts.md)
- [RIPv2](ripv2.md)

## Źródła w zestawie

- `Computer Networking Textbook.pdf` — strony 149–157.
- `Computer Networking.pdf` — prezentacja kursowa; odpowiadający rozdział zachowany w `_source-archive/02-Course-Slides.md`.
- `Padriseup Computer Networking.pdf` — uzupełnienia i materiały dodatkowe, jeśli występowały dla tego tematu.
