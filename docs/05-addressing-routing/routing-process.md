# Routing process and routing table

[← Indeks wiki](../index.md)

> **Źródło główne:** Computer Networking Textbook.pdf, s. 102–104. Treść została uporządkowana tematycznie; pełny ekstrakt źródłowy znajduje się w `_source-archive/`.


## Materiał kanoniczny

The routing process involves selecting a path for the delivery of packets across different
networks, from source to destination, through Layer 3 devices.
It is important to note that routers can route packets to directly connected networks,
without requiring configuration. However, if the networks are not connected directly to
the router, the route needs to be learned.
Routing decisions are made based on a router’s routing table.
Process Stages
Examination - In the first step, the router decides whether to process a packet or ignore
it. Routers will ignore packets with errors, or packets they don't know how to process.
Decapsulation - The router examines the Layer 2 address to decide if the packet was
intended for itself (the default gateway), and verifies the integrity of the frame using
the FCS (Layer 2 trailer).
Decision-Making - The router decides where to forward the packet to, based on its
destination IP address and the routers routing table.
Encapsulation - The router re-encapsulates the packet with new Layer 2 headers for the
next hop, according to the decision made in step 3.
Forwarding - After a decision is made, the router forwards the packet to the interface
from which the packet must exit to reach its destination.

Routing Choices
Same LAN - If the destination IP is on the same LAN as the source device, there is no
need for routing. The frame will get to the destination via the switch.
Known Route - If the destination IP is on a different LAN, but the network device has a
static or dynamic route to the destination IP, it will forward the packet to the next hop,
based on the route.
No Route - If there is no static or dynamic route in the network device’s routing table, it
will forward the packet to its default ‘Gateway of last resort’.
Note that a ‘Gateway of last resort’ is where the router will send packets to if there is
no other known route to which they should be sent.
No Gateway - If there is no ‘Gateway of last resort’ and the destination packet is not
listed, the router will discard the packet.
Routing Table
The Routing Table contains lists of routes to possible network destinations. The table
includes information about the network topology.
The codes on the left side of a route show how the network is learned by the router.
Router# show ip route
Codes: C - connected, S - static, I - IGRP, R - RIP, M - mobile, B - BGP

D - EIGRP, EX - EIGRP external, O - OSPF, IA - OSPF inter area

N1 - OSPF NSSA external type 1, N2 - OSPF NSSA external type 2

El - OSPF external type 1, E2 - OSPF external type 2, E - EGP

i - IS-IS, L1 - IS-IS level-1, L2 - IS-IS level-2, ia - IS-IS inter area

* - candidate default, U - per-user static route, o - ODR

P - periodic downloaded static route
Gateway of last resort is not set

172.16.0.0/16 is variably subnetted, 5 subnets, 2 masks
D 172.16.0.0/16 [90/5376] via 192.168.4.2, 00:02:24, GigabitEthernet4/0e
G 172.16.0.0/24 is directly connected, GigabitEthernet0/0
Ss 172.16.1.0/24 [1/0] via 192.168.1.2
R 172.16.2.0/24 [1260/1] via 192.168.2.2, 00:00:15, GigabitEthernet2/0
10) 172.16.3.0/24 [110/2] via 192.168.3.2, 00:01:26, GigabitEthernet3/@
Cc 192.168.1.0/24 is directly connected, GigabitEthernet1/0
Cc 192.168.2.0/24 is directly connected, GigabitEthernet2/0
Cc 192.168.3.0/24 is directly connected, GigabitEthernet3/0
Cc 192.168.4.0/24 is directly connected, GigabitEthernet4/0

Routing Table Codes
Directly-Connected / Local Route - When inspecting the routing table, records
identified by the codes C or L indicate directly connected networks. The codes mean
that the devices are connected to the physical layer. The C and L records are
automatically created.
Static Route - Static routes are configured and recorded manually, and are identified in
the routing table by the letter S.
Dynamic Route - Dynamic routes are identified with unique letters that indicate the
dynamic protocol that was used to create them.
Dynamic protocols include the following:

D - EIGRP routing protocol

O - OSPF routing protocol

R - RIP routing protocol

## Powiązane laboratoria

- [NET-05-LS2](../labs/net-05-ls2.md)

## Powiązane tematy

- [Routers and interfaces](routers-interfaces.md)
- [IPv4 static and default routing](static-routing-ipv4.md)
- [Dynamic routing concepts](dynamic-routing-concepts.md)

## Źródła w zestawie

- `Computer Networking Textbook.pdf` — strony 102–104.
- `Computer Networking.pdf` — prezentacja kursowa; odpowiadający rozdział zachowany w `_source-archive/02-Course-Slides.md`.
- `Padriseup Computer Networking.pdf` — uzupełnienia i materiały dodatkowe, jeśli występowały dla tego tematu.
