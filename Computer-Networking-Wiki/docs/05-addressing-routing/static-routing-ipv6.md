# IPv6 static routing

[← Indeks wiki](../index.md)

> **Źródło główne:** Computer Networking Textbook.pdf, s. 134–135. Treść została uporządkowana tematycznie; pełny ekstrakt źródłowy znajduje się w `_source-archive/`.


## Materiał kanoniczny

Static routing is similar for IPv4 and IPv6, with the exception of how the destination
network addresses are formatted.
IPv6 supports the same static routing types, and most of the parameters are identical to
those in IPv4 commands.
IPv6 Static Routing Requirements
The following are required to enable |Pv6 static routing:
= |IPv6 packet forwarding must be enabled on the Cisco router.
The command is IPv6 unicast-routing
«The interface must be enabled and configured with an IPv6 address.
IPv6 Static Routing Syntax
i Router (config) # i ipv6é route H <network-address> / <prefix> H <direction>
H H i 1 i 2 H 3 i
1. Specifies the IPv6 remote network address.
2. Specifies the remote network prefix.
3. Sets the direction of the network, which can be:
Directly-connected - the local outgoing interface.
Next-hop - the IPv6 link-local or global-unicast address of the interconnected
router.
R1(config)#ipv6 route
2001:abcd:cafe::/64 serial 0/0/02

IPv6 Configuration Example
The code below includes examples of all types of IPv6 static routes:
* Standard (next-hop)
* Default (directly-connected)
* Summary
* Floating
R1(config)#ipv6 route 2001:abcd:cafe::/64 2002:abcd:aaaa::1
Ri(config)#ipv6é route serial 0/0/08
Ri(config)#ipv6 route 2001:abcd:cafe:: gigabitethernet0/o
R1(config)#ipv6 route 2001:abcd:cafe::/64 gigabitetherneto/e
Verifying IPv6 Configuration
show ipv6 route displays and verifies the IPv6 routing table.
Remember not to use show ip route (displays IPv4 routing table), but rather
show ipv6 route
Ri(config)#do show ipv6é route
Ss 2001:ABCD:CAFE::/64 [1/0]
via 2002:ABCD: AAAA: :1
S ::/@ [1/0]
via serial 0/0/@

## Powiązane laboratoria

- Brak bezpośrednio przypisanego laboratorium w zestawie.

## Powiązane tematy

- [IPv6 addressing](ipv6.md)
- [IPv4 static and default routing](static-routing-ipv4.md)

## Źródła w zestawie

- `Computer Networking Textbook.pdf` — strony 134–135.
- `Computer Networking.pdf` — prezentacja kursowa; odpowiadający rozdział zachowany w `_source-archive/02-Course-Slides.md`.
- `Padriseup Computer Networking.pdf` — uzupełnienia i materiały dodatkowe, jeśli występowały dla tego tematu.
