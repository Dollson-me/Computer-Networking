# NAT implementation

[← Indeks wiki](../index.md)

> **Źródło główne:** Computer Networking Textbook.pdf, s. 211–214. Treść została uporządkowana tematycznie; pełny ekstrakt źródłowy znajduje się w `_source-archive/`.


## Materiał kanoniczny

The example below illustrates the simple topology of a router connecting a small
corporate network to the internet.
sacl
oN
R1
— Internet
LJ
——*,
i
——7
00020
NAT Interface Configuration
The first step in configuring NAT is to enable router interfaces for translation.
The ip nat inside\outside command informs the router which interfaces will participate
in the NAT process, and their direction, based on the network topology.
Each interface connected to the private network, is defined as inside, and each
interface connected to the internet is defined as outside.
#The interface facing the LAN.
Edge-R1(config)#interface gigabitEthernet 0/@
Edge-R1(config-if)#ip add 10.0.0.1 255.255.255.0
Edge-R1(config-if)#ip nat inside
Edge-R1(config-if)#no shutdown
Edge-R1(config-if)#exit
#The interface facing the WAN.
Edge-R1(config)#interface serial 0/0/08
Edge-R1(config-if)#ip add 209.15.10.1 255.255.255.0
Edge-R1(config-if)#ip nat outside
Edge-R1(config-if)#no shutdown
Edge-R1(config-if)#exit

Static NAT Configuration
Command
ip nat inside source static <local-ip> <global-ip>
<)>
In this example, a user wants to connect to the internal server from somewhere on the
internet.
Because the user cannot access the LAN directly, it sends the request to public router
interface 209.15.10.1, and the router uses the NAT static map to forward the request to
the 10.0.0.10 server.
The second section in the example is for Port Forwarding. It forwards only SSH traffic
from outside to the server.
#Map all traffic between 10.0.0.10 and 209.15.10.1
Edge-R1(config)#ip nat inside source static 10.0.0.10 209.15.10.1
#Map only SSH connection between 10.0.0.10 and 209.15.10@.1 on tcp port
8080 of the outside
Edge-R1(config)# ip nat inside source static tcp 10.0.0.10 22 209.15.10.1
8080
Dynamic NAT Configuration
Assume the ISP defined 10 public addresses on the WAN interface:
Step 1: Create a public address pool using ip nat pool.
Step 2: Configure standard ACL to identify local addresses that need to be translated,
using access-list.
Step 3: Bind the ACL and the pool using ip nat inside source list.
Note: Using this method, the pool should contain enough available addresses, one for
each device.
#Dynamic NAT allows local hosts access to the outside network, using a
randomly selected public address from the pool.
Edge-R1(config)#ip nat pool ToFreedom 209.15.10.1 209.15.10.1@ netmask
255.299.2590
Edge-R1(config)#access-list 1 permit 10.0.0.0 0.0.0.255
Edge-R1(config)#ip nat inside source list 1 pool ToFreedom

NAT Overload Configuration
NAT Overload or Port Address Translation allows a router to use a single public address
for multiple inside local addresses.
Methods to configure PAT:
1. Using an address pool.
2. Using a single address defined on the interface.
An important part of the command is the overload option.
#Method 1
Edge-R1(config)#ip nat pool ToFreedom 209.15.10.1 209.15.10.10 netmask
255.255.255.0
Edge-R1(config)#access-list 1 permit 10.0.0.0 0.0.0.255
Edge-R1(config)#ip nat inside source list 1 pool ToFreedom
#Method 2
Edge-R1(config)#access-list 1 permit 10.0.0.0 0.0.0.255
Edge-R1(config)#ip nat inside source list 1
NAT Overload Configuration Verification
Two commands can be used to fully verify a NAT operation.
The show ip nat statistics command displays NAT parameter and pool configuration,
pool status, and interface configuration.
The show ip nat translations command shows the active NAT translation (inside local
and inside global address paring, when they occur).
Note: Static NAT translation is always shown in the table.

Edge-Rl1#show ip nat statistics
Total translations: 5 (1 static, 4 dynamic, 4 extended)
Outside Interfaces: Serial@/e/e
Inside Interfaces: GigabitEthernet0/o
Hits: 5 Misses: 13
Expired translations: 1
Dynamic mappings:
-- Inside Source
access-list 1 pool ToFreedom refCount @
pool ToFreedom: netmask 255.255.255.0
start 209.15.10.1 end 209.15.10.1
type generic, total addresses 1 , allocated @ (0%), misses 8
Edge-Ri1#show ip nat translations
Pro Inside global Inside local Outside local Outside
global
--- 209.15.10.1 10.0.0.10 --- ---
tcp 209.15.10.1:50016 10.0.0.10:50016 8.8.8.8:53 8.8.8.8:53
tcp 209.15.10.1:50017 10.0.0.10:50017 200.10.0.254:88
200.10.0.254:80
tcp 209.15.10.1:50018 10.0.0.20:50018 157.160.27.8:80
157.160.27.8:80
tcp 209.15.10.1:50019 10.0.0.20:50019 82.11.0.2:443
82.11.0.2:443

## Powiązane laboratoria

- Brak bezpośrednio przypisanego laboratorium w zestawie.

## Powiązane tematy

- [NAT overview](nat-overview.md)
- [DHCP implementation](dhcp-implementation.md)

## Źródła w zestawie

- `Computer Networking Textbook.pdf` — strony 211–214.
- `Computer Networking.pdf` — prezentacja kursowa; odpowiadający rozdział zachowany w `_source-archive/02-Course-Slides.md`.
- `Padriseup Computer Networking.pdf` — uzupełnienia i materiały dodatkowe, jeśli występowały dla tego tematu.
