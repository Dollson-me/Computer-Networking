# IPv6 addressing

[← Indeks wiki](../index.md)

> **Źródło główne:** Computer Networking Textbook.pdf, s. 109–112. Treść została uporządkowana tematycznie; pełny ekstrakt źródłowy znajduje się w `_source-archive/`.


## Materiał kanoniczny

Over the years, the IPv4 address pool was slowly depleted due to technical progress
that led to more and more devices around the world being connected to the Internet.
IPv6 was designed to solve the IPv4 address limitation and provide additional
enhancements. IPv6 has a larger 128-bit address pool, with the number of available
addresses being 340*10*.
Example of an IPv6 address: 2001:0000:3238:0001:0063:0000:0000:FEFB
Compressing IPv6 Addresses
IPv6 addresses are long and difficult to read. Some rules exist to omit specific numbers
to simplify the addresses.
Full Address - A full address contains all 8 blocks, with 4 hexadecimal digits.
Example of a full IPv6 address: 2001:0000:3238:0001:0063:0000:0000:FEFB
Leading Zeros - The first rule allows us to discard leading zeros in a block, making the
address a bit shorter: 2001:0:3238:1:63:0000:0000:FEFB
Consecutive Zeros - If two or more blocks contain consecutive zeros, they can be
omitted and replaced with double colon signs (::) resulting in: 2001:0:3238:1:63::FEFB
Note that omitting is allowed only once in the address.
Zero Block - If there is a block that consists of 4 zeros, but without a consecutive zero-
filled block, it can be replaced with a single zero, and the final address will be:
2001:0:3238:1:63::FEFB

IPv6 Address Breakdown
2001:0ABC:00BB:: 0000 ::0000:0000:0000:0001 : /64
The suffix represents the prefix portion of the address. IPv6 does not use notation
subnet masks like IPv4. The prefix length indicates the network portion.
1. Because the prefix is /64, the first 64 bits in the address represent the network
portion.
2. The 16 bits from the 49th to the 64th are for defining subnets.
3. The remaining 64 bits represent the host portion in the IPv6 address.
4. The prefix range can be from 0 to 128, with the most common being /64.
Router(config-if)#ipv6é address
2001 : QABC : QOBB : 0000 : 8000 : 0080 : 8000: 0001/64
Configure and Verify IPv6é
To enable IPv6 routing, enter the configuration terminal mode, and run the command
ipv6 unicast-routing.
Configure IPv6 on a router interface using the command ipv6é address.
Verify the configuration using the command show ipvé interface brief.
Router(config)#ipv6 unicast-routing
Router(config)#interface gigabitEthernet0/e/e
Router(config-if)#ipv6 address 2001: @ABC: Q@BB : 0000: 0000 : 8000: 0000 : 0801/64
Router(config-if)#no shutdown
Router (config-if)#exit
Router#show ipv6é interface brief
GigabitEthernet@/0/e [up/down]
FE8@: :201:97FF:FE13:A801
2001:ABC:BB::1
GigabitEthernet®/0/1 [administratively down/down]
unassigned
Vlan1 [administratively down/down]
unassigned

Device Communication Types
Unicast - Unicast addresses represent specific network interfaces that support IPv6.
Unicast addresses have 3 sub-types (described in the following section).
Multicast - Addresses used to send |Pv6 packets from a single host to multiple
destinations.
Anycast - IPv6 unicast addresses that can be assigned to multiple devices. Packets sent
to an Anycast address are routed to the nearest device that has that address (which is
why Anycast is also known as "one to the nearest“). This method operates similar to
IPv4 broadcast.
Unicast Types
Global Unicast - |Pv6 global unicast addresses are similar to IPv4 public addresses. They
are unique and can be routed via the Internet. IANA currently assigns only 2000::/3
addresses.
Link-Local - Addresses that enable communication between devices in the same local
link (LAN).
Link Local addresses must be unique only within the link. They are not guaranteed to be
unique beyond their network segment, and begin with FE80::/10.
Unique-Local - Similar to IPv4 private addresses, with minor differences.
Unique addresses should not be routable in the global IPv6, and should not be
translated to global IPv6 addresses. They begin with FCOO::/8.

IPv6 Address Example
The following table lists examples of commonly used IPv6 addresses of various types.
Type Address Example Notes

Global Unicast 2001:0ABC:1111:0000:1111:0000:0000:0200 The address range is from 2000 to 3FFF.
Global Unicast 2001:0ABC:0000:00BB:DCBA:0000:0000:0200 The address range is from 2000 to 3FFF.
Link-Local FE80:0000:0000:0000:3211:5412:ECDC:FE11 Link-local address prefix is FE80::/10.
Link-Local FE80:0000:0000:0000:3211:5412:CAD1:FE12 Link-local address prefix is FE80::/10.
Multicast FF02:0000:0000:0000:0000:000F:FFO0:120F Multicast addresses use the prefix ff00::/8.
Anycast ¥0004.100410040040000:0000:0000:0000 Similar to broadcast addresses in IPv4.
IPv4 and IPv6 Coexistence

IPv4 and IPv6 can coexist using protocols and tools created by IEFT, which are known as:
Dual Stack, Tunneling, and Translation.

Dual Stack - Dual Stack means that a device runs both IPv4 and IPv6 protocols
simultaneously. Using two stacks allows both IP versions to coexist.
Tunneling - Tunneling is used when IPv6 addresses are to be sent over IPv4 networks,
or vice versa. In this method, the IPv6 packet is encapsulated within an IPv4 packet.
Translation - Translation allows IPv6 to communicate with IPv4-enabled devices using
techniques similar to those used by NAT.

é Lab — Configure IPv6 Addressing
—J | Practice configuring IPv6 addresses on a router and clients, and verification
m= =| of IPv6 addressing implementation.
Perform the instructions in lab document Net-05-L3.

## Powiązane laboratoria

- [NET-05-LS3](../labs/net-05-ls3.md)


## Uzupełnienia z notatek Riseup / zajęć

<details>
<summary>Pokaż notatki prowadzącego, dodatkowe komendy i linki powiązane z tym tematem</summary>

https://www.universalnetworks.co.uk/faq/what-does-utp-s-utp-ftp-stp-and-sftp-mean/
ciekawostka nt satellite tracking https://www.n2yo.com/
#IPv4 vs IPv6
https://www.netia.pl/pl/blog/ipv4-vs-ipv6-%E2%80%93-co-to-za-protokoly-i-jakie-sa-miedz
http://kti.eti.pg.gda.pl/ktilab/ipv6-adr/ipv6-adresy.pdf
https://www.soisk-me.pl/klasa-iv-sieci/klasy-adresow-ip

---

#RIR
https://pl.wikipedia.org/wiki/Regional_Internet_Registry
#IPV4 vs IPV6
https://www.netia.pl/pl/blog/ipv4-vs-ipv6-%E2%80%93-co-to-za-protokoly-i-jakie-sa-miedz
#Klasy adresów IP
https://www.soisk-me.pl/klasa-iv-sieci/klasy-adresow-ip

---

R1>enable
R1#conf t
R1(config)#ipv6 unicast-routing
R1(config)#interface gigabitEthernet 0/0
R1(config-if)#ipv6 address 2001:cafe:abcd:1::/64
R1(config-if)#exit
R1(config)#
https://www.browserling.com/tools/ip-to-bin

</details>

## Powiązane tematy

- [IPv4 addressing](ipv4.md)
- [IPv6 static routing](static-routing-ipv6.md)

## Źródła w zestawie

- `Computer Networking Textbook.pdf` — strony 109–112.
- `Computer Networking.pdf` — prezentacja kursowa; odpowiadający rozdział zachowany w `_source-archive/02-Course-Slides.md`.
- `Padriseup Computer Networking.pdf` — uzupełnienia i materiały dodatkowe, jeśli występowały dla tego tematu.
