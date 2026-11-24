# Dynamic routing concepts

[← Indeks wiki](../index.md)

> **Źródło główne:** Computer Networking Textbook.pdf, s. 136–140. Treść została uporządkowana tematycznie; pełny ekstrakt źródłowy znajduje się w `_source-archive/`.


## Materiał kanoniczny

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

## Powiązane laboratoria

- [NET-08-LS1](../labs/net-08-ls1.md)
- [NET-08-LS2](../labs/net-08-ls2.md)

## Powiązane tematy

- [RIPv2](ripv2.md)
- [OSPFv2](ospfv2.md)
- [Routing process and routing table](routing-process.md)

## Źródła w zestawie

- `Computer Networking Textbook.pdf` — strony 136–140.
- `Computer Networking.pdf` — prezentacja kursowa; odpowiadający rozdział zachowany w `_source-archive/02-Course-Slides.md`.
- `Padriseup Computer Networking.pdf` — uzupełnienia i materiały dodatkowe, jeśli występowały dla tego tematu.
