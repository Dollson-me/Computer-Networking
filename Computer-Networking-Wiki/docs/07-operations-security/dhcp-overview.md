# DHCP overview

[← Indeks wiki](../index.md)

> **Źródło główne:** Computer Networking Textbook.pdf, s. 200–204. Treść została uporządkowana tematycznie; pełny ekstrakt źródłowy znajduje się w `_source-archive/`.


## Materiał kanoniczny

To communicate with each other, all devices on a network must have a unique IP
address.
Network administrators will often be responsible for assigning static IP addresses to
network components, such as routers, servers, firewalls, etc.
Assigning a static IP address for every endpoint in an organization can be time-
consuming. Many endpoints do not require a static IP address at all.
The solution is to use DHCP (Dynamic Host Configuration Protocol).
DHCP is designed to simplify the process of IP address allocation for devices on the
network. A DHCP server is configured with a range of IP addresses, which it allocates to
devices on the network.
DHCPv4 dynamically allocates IPv4 addresses to devices in the network, including DNS
server address and default gateway addresses.
Routers and DHCP servers also have the ability to allocate IP addresses using the DHCP
protocol.
DHCP Characteristics
OSI Model Layer - DHCP operates in the Application Layer of the OSI model.
Logical Ports - DHCP works with the UDP protocol and uses ports 67 and 68.
Versions - DHCP supports both IPv4 (DHCPv4) and IPv6 (DHCPv6).
DHCP Allocation Methods
Dynamic Allocation - The DHCP server assigns an available IP address to the client from
its address pool, for a limited amount of time. The client “leases” the address from the
server, for a period set by the administrator. At the end of the lease, the client requests
an extension or a new address.

Automatic Allocation - As in the Dynamic Allocation method, the client receives a
random available IP address. But in this case, there is no time limit for the address. The
client does not have to renew the lease for the address it was assigned.
Reservation Address - The network administrator configures the DHCP server to
allocate a specific IP address to a selected client device. The address is reserved for a
specific device in advance, based on its MAC address. This method is useful for devices
such as network printers.
Lease Process
DHCP Discover - A client device that requires an IP address sends a discover message in
broadcast, to search for a DHCP server on the network. They communicate using Layer
2 and Layer 3 broadcast addresses.
DHCP Offer - After the server receives the discover message, it reserves an available IP
address and offers it to the client, along with the lease details. DHCPv4 sends a message
to the requesting client to reserve an available I|Pv4 address.
The server also creates an ARP entry with the requesting client MAC address.
DHCP Request - The client responds to the offer by sending a response with accept or
decline.
DHCP Acknowledgment - After receiving an accept message, the server sends
DHCPACK, with all the necessary configuration information.
Lease Renewal Process
DHCP Request - Before a lease expires, the client sends a DHCPREQUEST message
directly to the DHCPv4 server that originally offered the IPv4 address.
DHCP Acknowledgement - Upon receiving the DHCPREQUEST message, the server
verifies the lease information by returning a DHCPACK.
Messages can be sent as Unicast or Broadcast.

DHCPv6
Unlike IPv4, IPv6 uses multiple types of addresses from different hosts. DHCPv6 was
developed due to the usage in networks of various address formats and prefixes,
instead of subnet masks.
DHCPVv6 also supports more allocation methods than DHCPv4. For example, an IPv6
host can automatically generate an IP address internally, using stateless address auto-
configuration (SLAAC), or the EUI-64 process for link-local addresses.
More information about DHCPvé6 is provided in RFC 2460.
DHCPv6 Allocation Methods
SLAAC - In this method, the device can obtain an IPv6 global address without the
services of a DHCP server. The device uses ICMPv6 for advertisement messages, to
provide addressing and other configuration information that would normally be
provided by a DHCP server.
Stateless DHCPV6 - The stateless DHCPv6 method informs the client to use the
information in the RA (Router Advertisement) message for addressing, while additional
configuration parameters are available from a DHCPv6 server. The client will then
communicate with a stateless DHCPv6 server to obtain information not provided in the
RA message, such as a DNS server address.
Stateful DHCPv6 - Similar to DHCPv4, but both addressing information and
configuration need to be obtained from a DHCPV6 server.

DHCP Router vs Server
Router Server
Used in smaller networks and .
q . Used in larger networks and
SMBs (small and medium-sized .
. enterprises.
businesses).
Easy to manage. Easy to manage.
Requires knowledge of Cisco IOS Requires general knowledge of servers,
and the relevant configuration. especially DHCP servers.
Relatively low cost, since no device _— Relatively expensive, especially if the
is required other than the existing organization needs to buy a dedicated
router. server to act as the DHCP server.

## Powiązane laboratoria

- Brak bezpośrednio przypisanego laboratorium w zestawie.

## Powiązane tematy

- [DHCP implementation](dhcp-implementation.md)
- [NAT overview](nat-overview.md)

## Źródła w zestawie

- `Computer Networking Textbook.pdf` — strony 200–204.
- `Computer Networking.pdf` — prezentacja kursowa; odpowiadający rozdział zachowany w `_source-archive/02-Course-Slides.md`.
- `Padriseup Computer Networking.pdf` — uzupełnienia i materiały dodatkowe, jeśli występowały dla tego tematu.
