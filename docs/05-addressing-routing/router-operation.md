# Router operation and static routing concepts

[← Indeks wiki](../index.md)

> **Źródło główne:** Computer Networking Textbook.pdf, s. 124–126. Treść została uporządkowana tematycznie; pełny ekstrakt źródłowy znajduje się w `_source-archive/`.


## Materiał kanoniczny

Router Operation Review

One of the router’s main jobs is to select the best path for a packet. The decision is

based on its destination address.

After determining the best path on which to forward the packet, the router

encapsulates the packet in a new frame in accordance with the relevant outgoing

interface.

Packet Forwarding Process

Examination In the first step, the router decides whether to process a packet
or ignore it. Routers will ignore packets with errors, or packets
they don't know how to process.

Decapsulation The router examines the Layer 2 address to decide if the packet
was intended for itself (the default gateway), and verifies the
integrity of the frame using the FCS (Layer 2 trailer).

Decision-making The router decides where to forward the packet to, based on its
destination IP address and the routing table.

Encapsulation The router re-encapsulates the packet with new Layer 2 headers
for the next hop (MAC address of the next hop), according to the
decision made in step 3.

Forwarding After a decision is made, the router forwards the packet to the
interface from which the packet must exit.

Remote Networks
A router's best routing decision is based on its routing table. But where does the routing
table get its information from?
Networks connected directly are added to the table immediately, but a remote network
must be configured by the user.
A remote network is any network not connected locally to the router.
Note: The ICMP message "Destination unreachable" is displayed whenever the router
cannot find a match for the path in its routing table.
Remote Network Learning
A remote network can be learned by a router in one of two ways: statically or
dynamically.
In the static routing method, the user enters every network manually in the routing
table.
In the dynamic routing method, the router automatically learns the remote network
from the routing tables of adjacent routers, by using various protocols.

Static Method Pros and Cons
Advantages Disadvantages
A simple solution for small Error-prone in large network
networks. environments.
Not advertised over the network, Does not support verification
meaning better security. methods.
No CPU and memory usage for Configuration and maintenance
routing purposes. are time-consuming.
Every path a packet takes is known, .
a . Requires complete knowledge of
which improves network traffic ;
the entire network.
management.
When to use Static Routing
Network administrators decide if and when to use Static Routing, based on network
requirements.
Stub Networks
Static routing is a better choice when routing to and from stub networks.
Stub networks consist of a single router that sends and receives non-local traffic via a
single path.
Small Networks
Although Static Routing is simple and secure, and saves resources, it does not provide a
sufficient level of scalability in larger networks.

## Powiązane laboratoria

- [NET-07-LS1](../labs/net-07-ls1.md)

## Powiązane tematy

- [IPv4 static and default routing](static-routing-ipv4.md)
- [Routing process and routing table](routing-process.md)

## Źródła w zestawie

- `Computer Networking Textbook.pdf` — strony 124–126.
- `Computer Networking.pdf` — prezentacja kursowa; odpowiadający rozdział zachowany w `_source-archive/02-Course-Slides.md`.
- `Padriseup Computer Networking.pdf` — uzupełnienia i materiały dodatkowe, jeśli występowały dla tego tematu.
