# ACL overview

[← Indeks wiki](../index.md)

> **Źródło główne:** Computer Networking Textbook.pdf, s. 188–190. Treść została uporządkowana tematycznie; pełny ekstrakt źródłowy znajduje się w `_source-archive/`.


## Materiał kanoniczny

ACL (Access Control List) is a rule-based feature that allows network administrators and
engineers to configure basic traffic filtering.
ACL is a series of commands that determine, based on information in the packet
header, whether to drop the packet or forward it.
ACL vs Firewall
Similar to ACL, firewalls are used to protect networks from unauthorized use.
A difference between them is that firewalls are placed at the entry and exit points of
the network architecture, to analyze all traffic coming into the network, while ACLs are
placed wherever they are needed in the network.
Advantages of Configuring an ACL on a Device
Network Performance - Network performance can be improved by allowing only
relevant services to communicate with devices across the network.
For example, restricting the network to block video traffic can improve network
performance.
Securing the Network - In a network environment, users may be restricted from
accessing sensitive services.
ACL provides a basic level of network security by allowing some hosts to access parts of
the network, while preventing others from accessing the same parts.
Restriction Capability - ACLs can also restrict the following:
e Routing protocol advertisement messages
e Packets from security protocols
e Packets from other protocols, such as ICMP

Standard and Extended ACLs
There are Standard ACLs and Extended ACLs, with the difference in the parameters
examined in the process.
Standard ACLs examine only the source IP address when implementing restrictions.
Cisco recommends to place this type of ACL as close to the destination device as
possible.
Extended ACLs filter packets according to protocol type, source or destination IP
address, and source or destination port. Cisco recommends to place this type of ACL as
close to the source as possible.
Traffic Direction
Traffic direction must be specified on an interface when configuring ACL. The direction
can be ether inbound or outbound. This is done so that the router will implement the
proper restrictions when examining the source network and destination.
Inbound ACL - Configures the ACL for inbound traffic. The router will examine incoming
traffic to the interface.
Outbound ACL - Configures the ACL for outbound traffic. The router will examine
outgoing traffic from the interface.
Wildcards
Wildcards are inverted subnet masks that can be used in statements of both Extended
and Standard ACLs.
For example, 255.255.255.0
(binary equivalent = 11111111.11111111.11111111.00000000)
This inverts to a wildcard mask of 0.0.0.255
(binary equivalent = 00000000.00000000.00000000.11111111)

ACL Order
Among other important guidelines, the ACL order is crucial.
Check Order - ACEs (Access Control Entries), which represent the order of statements in
the ACL, are essential and must be planned carefully. The router checks each packet’s
parameters against the ACEs to find a matching condition. When a condition is met, the
ACL will be applied, and additional ACEs will be ignored.
Implicit Deny - At the end of every ACL, there is an invisible statement called implicit
deny. When no match is found for a packet, the implicit deny statement is applied.
Note: Each ACL must have at least one Permit statement!

## Powiązane laboratoria

- [NET-11-LS1](../labs/net-11-ls1.md)

## Powiązane tematy

- [Standard ACL](standard-acl.md)
- [Extended ACL](extended-acl.md)

## Źródła w zestawie

- `Computer Networking Textbook.pdf` — strony 188–190.
- `Computer Networking.pdf` — prezentacja kursowa; odpowiadający rozdział zachowany w `_source-archive/02-Course-Slides.md`.
- `Padriseup Computer Networking.pdf` — uzupełnienia i materiały dodatkowe, jeśli występowały dla tego tematu.
