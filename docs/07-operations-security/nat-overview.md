# NAT overview

[← Indeks wiki](../index.md)

> **Źródło główne:** Computer Networking Textbook.pdf, s. 208–210. Treść została uporządkowana tematycznie; pełny ekstrakt źródłowy znajduje się w `_source-archive/`.


## Materiał kanoniczny

Network Address Translation (NAT) is an essential protocol and service that converts a
private address to a public address, and vice versa.
NAT is usually enabled on a firewall or router device at the edge of the local network,
and the beginning of the outside network.
Most home-based, corporate, or local network uses private IP addressing which cannot
be used on the public internet. NAT takes the private IP address and translates it toa
public IP address to be used on the public internet. When the data returns, it is
translated back to a private IP address.
The NAT process is transparent to users, and any evidence of its operation is stored ina
special table in the NAT-enabled device. This helps hide the internal network from the
internet, and adds an extra layer of security.
Private IP Space
According to RFC 1918, three address spaces are reserved for devices in a private
network (LAN). Their usage is unlimited and they can be implemented freely.
Private IP Range

IP Subnet

10.0.0.0-10.255.255.255 255.0.0.0

172.16.0.0-172.31.255.255 255.255.0.0

192.168.0.0-192.168.255.255 255.255.255.0
NAT Advantages and Disadvantages

Pros Cons

Conserves space allotted for IPv4 Accessing internal resources requires
addresses, preventing address special configuration and makes
depletion via PAT. troubleshooting more challenging.
Network flexibility and connection Difficult to troubleshoot issues
reliability. remotely.
Using tunneling protocols, NAT
. interferes with integrity checks,
Extra layer of network security. ; i. 7
because it modifies values in the
headers.
NAT64
NAT64 (Network Address Translation IPv6 to IPv4) technology facilitates
communication between IPv6-only and IPv4-only hosts and networks.
This solution allows enterprises and ISPs to accelerate IPv6 adoption, while
simultaneously handling IPv4 address depletion.
NAT Methods
Static NAT — one-to-one NAT. A permanent mapping of a single private IP to a specific
single public address. This method is not meant to conserve IPv4 addresses, but to
allow access to internal resources from an outside network.
Dynamic NAT — many-to-many NAT. This method is also not meant to conserve
addresses. Multiple IP addresses are mapped dynamically by the router to a pool of
public addresses. The conversion is done on a first-come, first-serve basis.
PAT (or NAT Overload) — many-to-one NAT. This is the most common method, and is
used to conserve addresses. In this method, multiple private IP addresses are converted
to a single public address. To distinguish the traffic from different devices, the source
port number is also used for the inside global address.
Theoretically, the maximum number of private addresses that can be translated to one
public address is 65,536.

NAT Address Types
Inside Local - The original IP address of the host. For example: 10.0.05/24
Outside Local - The IP address of the destination device as viewed from the inside local
device (the destination LAN). For example: A remote web server.
Inside Global - The public IP address used by the inside local device for identification
and access to the internet. For example: the WAN IP address.
Outside Global - An IP address from outside the network. For example: the WAN
address of the interface connected to the web server.
NAT Operation Steps
Step 1 - A host on the local network sends a request to an external destination (outside
local), such as a web server.
Step 2 - The NAT-enable device receives the request and changes the local device
source address (inside local) to the public IP configured on the WAN interface (inside
global).
Step 3 - The NAT-enable device receives the request and changes the local device
source address (inside local) to the public IP configured on the WAN interface (inside
global).
Step 4 - The web server receives the request and replies with a public source IP.
Step 5 - The NAT-enabled device receives the reply from the web server and converts
the public destination address to the original private address (based on the NAT table).
The local host then receives the server’s reply.

## Powiązane laboratoria

- Brak bezpośrednio przypisanego laboratorium w zestawie.

## Powiązane tematy

- [NAT implementation](nat-implementation.md)
- [DHCP overview](dhcp-overview.md)

## Źródła w zestawie

- `Computer Networking Textbook.pdf` — strony 208–210.
- `Computer Networking.pdf` — prezentacja kursowa; odpowiadający rozdział zachowany w `_source-archive/02-Course-Slides.md`.
- `Padriseup Computer Networking.pdf` — uzupełnienia i materiały dodatkowe, jeśli występowały dla tego tematu.
