# DHCP implementation

[← Indeks wiki](../index.md)

> **Źródło główne:** Computer Networking Textbook.pdf, s. 205–207. Treść została uporządkowana tematycznie; pełny ekstrakt źródłowy znajduje się w `_source-archive/`.


## Materiał kanoniczny

Configuring a DHCPv4 Client
Configuration Steps:
Step 1: Exclude addresses from the DHCP pool.
Run ip dhcp excluded-address to reserve an IP address for the default gateway or
statically configured servers.
Step 2: Set up a DHCP pool of addresses using ip dhcp pool
Step 3: Configure specific tasks, such as the default gateway, DNS server, domain name,
etc.
Note: The lease 0 4 30 (days, hours, minutes) will not work in Packet Tracker. It does
operate on an authentic Cisco device.
R1(config)#ip dhcp excluded-address 192.168.0.1
R1(config)#ip dhcp excluded-address 192.168.0.100 192.168.0.150
R1(config)#ip dhcp pool LAN1
R1(dhcp-config)#network 192.168.0.0 255.255.255.0
R1(dhcp-config)#default-router 192.168.0.1
R1(dhcp-config)#dns-server 192.168.0.105
R1(dhcp-config)#domain-name Cyber.com
R1(dhcp-config)#lease ® 4 30
R1(dhcp-config)#exit
Verify DHCP Settings
Several commands can be used to verify and troubleshoot DHCP settings:
Show ip dhcp pool - Displays pool settings.
Show ip dhcp binding - Displays the client list, with IP, MAC address, and lease
expiration.
Show ip dhcp conflict - Displays IP conflicts detected during DHCP negotiation.

R1#show ip dhcp pool

Utilization mark (high/low) : 100 / @

Subnet size (first/next) : 0/20

Pending event : none

1 subnet is currently in the pool

Current index IP address range Leased/Excluded/Total

192.168.0.1 3 /2 / 254
Configuring DHCPv4 Server
Addresses can be excluded from the DHCP pool during service configuration, using the
ip dhcp excluded-address command.
This can be done, for example, to reserve an IP address for the default gateway.
Set up a DHCP pool of addresses using the command: ip dhcp pool pool-name
Configure specific tasks like default-router and DNS-server. Tasks such as default-router
must be configured, while other tasks, such as DNS, do not have to be configured.
Example:

//Example: Suppose your router connects to 4 PCs using a switch, and you

want to configure them using DHCPv4, the network address is

192.168.0.0/24 with excluded IP address 192.168.0.1. Configure the

appropriate DHCP pool:

Router#configure terminal

Router(config)#ip dhcp excluded-address 192.168.0.1

Router(config)#ip dhcp pool poolone

Router(dhcp-config)#network 192.168.0.0 255.255.255.0

Router (dhcp-config)#default-router 192.168.0.1

Router (dhcp-config)#dns-server 192.168.0.1

Router(dhcp-config)#domain local.host

Router (dhcp-config)#end

Configuring DHCPv4 Relay
DHCP relay is used by devices to obtain addresses from a remote network using
broadcast messages.
Broadcast messages are not transmitted to other networks. When a client sends
DHCPDiscover, the router acts as a relay and forwards the message directly to the
server in Unicast.
The command to set the DHCPv4 relay is ip helper-address.
Example:

//Example: Suppose your DHCPv4 server is located on another subnet

than that of your PC. The router needs to be enabled with Cisco

helper to process the request:

Router#configure terminal

Router(config)#interface ge/e

Router(config-if)# ip helper-address 192.168.11.6

Router (config-if)#

b Lab Assignment — Configure DCHPv4 on a Cisco Router
—=/ | Setup a DHCP service on a Cisco router, and make sure all devices on the
mm | network receive addresses dynamically. The lab also helps understand the
DHCP Relay concept
Perform the instructions in lab document NET-12-L1.

## Powiązane laboratoria

- Brak bezpośrednio przypisanego laboratorium w zestawie.

## Powiązane tematy

- [DHCP overview](dhcp-overview.md)
- [NAT implementation](nat-implementation.md)

## Źródła w zestawie

- `Computer Networking Textbook.pdf` — strony 205–207.
- `Computer Networking.pdf` — prezentacja kursowa; odpowiadający rozdział zachowany w `_source-archive/02-Course-Slides.md`.
- `Padriseup Computer Networking.pdf` — uzupełnienia i materiały dodatkowe, jeśli występowały dla tego tematu.
