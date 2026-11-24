# 02 — Computer Networking — slajdy kursowe — pełna treść

Źródło: `Computer Networking.pdf` (525 slajdów). Każdy slajd ma własny nagłówek z numerem strony.


# Chapter 1: Introduction to Networks


### Slides — strona 1

i Introduction: - |
to Networks
Computer Networking


### Slides — strona 2

Computer Networking
Introduction Network Switch & IOS Switch Securit IP and Routing
to Networks Fundamentals Fundamentals y Concepts
Diagnostics and VLANs Dynamic IPv4 & IPv6é Subnetting
Troubleshooting and Trunk Routing Static Routing Concepts
Access Infrastructure Fiival Proiect
Control List Services J
2


### Slides — strona 3

Introduction to Networks
Overview
Lesson Objective
Network Types and Devices
This lesson is the starting point for Network Media and Cables
networking.
It teaches basic concepts and Network Topologies and Architecture
technologies of network structures,
. . Network Protocols and Commands
topologies, and devices.
Wireless Technology
G
3


### Slides — strona 4

CO
Introduction to Networks
NETWORK TYPES AND DEVICES


### Slides — strona 5

Network Types and Devices
Why is Networking Necessary?
Communication
Communication is an essential characteristic of any society.
In today’s world, people communicate with other people around
the world almost as simply as they talk to a person standing right
beside them.
Over the past several decades, global communication has
advanced significantly and has greatly improved the human social
experience.
Communication over a network (networking) brings people
together for either generic or specific purposes.
B
A network is basically two or more devices that communicate with each other and share information.
5


### Slides — strona 6

Network Types and Devices
Computer
LAN =") hl I
= = A Local Area Network defines a small geographical area is { = : a
Lme in which multiple computers and other devices are | ee = == = &
pa m connected. LANs can be set up in homes and small | = = &
businesses, and can be managed individually or centrally. ~~) 2 | ‘
ies
A Wide Area Network is spread across an unlimited = <= ae a
geographical area and connects between multiple LANs. Was | e
WANs are usually managed by several service providers. . ,
7
LANs can be designed to use one of two communication methods: Wired or Wireless
6


### Slides — strona 7

Network Center
MAN
A Metropolitan Area Network is larger than a LAN but
smaller than a WAN. In most cases, it is managed by a i -
city municipality and enables connection to broader = =a ‘
networks. Sie
SAN a a
—o A Storage Area Network is a dedicated network that Ai =
—o supports file servers and provides efficient transfer of
——d unusually large data sizes at extremely high rates. “thie \
@ ; : nF a
SAN is often not regarded as a type of network because it is closer to being infrastructure.
de


### Slides — strona 8

Network Types and Devices
Network Structure
Network Requirements
Communication among devices can be as simple as connecting a
cable between two computers.
On the other hand it can be as complex as a large assembly of
multiple networks spread around the world and regulated by a
variety of sophisticated devices and protocols.
B
The history of computer networks began in the 1960s with a network called ARPANET.
8


### Slides — strona 9

: Network
End Devices ; See
Devices that connect to a network for communication : aoe rk
purposes, such as computers, phones, and others. All ; a j ¥
end devices have unique addresses that identifies them j a :
on the network. vy ——
Media e-. =
‘Media’, based on the word ‘medium’ (meaning ‘in
between’) is a means of transferring data, such as
metallic wire, glass or plastic fiber, wireless radio
frequencies, and others.
=n
——— A
Intermediary Devices
=== =F Devices that transfer messages over the network and
ees facilitate communication between end devices.
2]


### Slides — strona 10

End Devi
Devices
In today’s world, most people
communicate with each other
through networks.
End devices are source or
destination devices ina
networked system.
Computers, laptops, and
phones are end devices that
allow us to communicate over
a network. a
———— a Re
End devices must have the
ability to connect to a network
via an NIC, to be able to send
and receive information.
EA
10


### Slides — strona 11

Network Types and Devices
NIC
To allow an end device to send
and receive information over a
network it must have the 2 Rass,
appropriate hardware. Le »* Z casos EN
A Network Interface Card (NIC) , —_. i : Ly, # —
allows end devices to interact a ci SSraah ae “et Y
with other devices over a < ONG s eS
network. » ok
Other names for NIC include:
* Network Adapter ‘ »
¢ LAN Adapter
* Physical Network Interface
iL


### Slides — strona 12

Network Types and Devices
Intermediary Devices
Definition
Intermediary devices act as bridges, interconnecting end devices.
Smart intermediary devices know how to differentiate between
devices, and can send data to specific destinations.
B
Unlike smart devices, simple intermediary devices send information indiscriminately across a network.
12


### Slides — strona 13

Network Types and Devices
Switch
For multiple end devices to
communicate with each other, a
mechanism needs to be set up _ —_
to handle the transfers. ’ SS
, — | (
A Switch is a device with physical 7. See » (
ports to which end devices can be se x Se £ f
connected via Ethernet cables, to meee |
create a network. bas Gere . '
Switches use MAC addresses to
pass information from one end
device to another.
13


### Slides — strona 14

Network Types and Devices
Switch Vs. Hub
Hub
A hub is the legacy implementation of a switch. Message 7g
: A a — a
uz It broadcasts data to all connected devices, as opposed to ——
to sending information to dedicated destinations. —
GO Message L—
. {1 \
Layer 2 Switch to A,B, ———|
we 6 F s and C
This is the most common and basic switch in use. [20009]
It uses MAC addresses to forward information to Hib L—_J
specific destinations within the network. ——
Layer 3 Switch
A layer 3 switch performs the same operations as a
layer 2 switch, but can also function as a router if it
is configured to do so.
14


### Slides — strona 15

Communication
A collision domain is a group of nodes that can ‘hear’ each other.
ee, TP Ideally, when one node talks, all the others only listen. When two
ig = iad is i nodes talk at the same time, a collision occurs. To resolve this issue, a
j : : hub creates collision domains.
’ A switch, which operates in Layer 2 of the OSI model, can create
separate conversations between nodes, which, in turn, creates
=” “2 , separate collision domains.
hii, 2 Although collisions are expected to occur in a half-duplex Ethernet
; network, if a collision domain becomes too big, traffic problems will
arise, due to re-transmissions.
B
15


### Slides — strona 16

Broadcast & Collision Domains
Communication
Broadcast is a type of communication whereby the sender sends a
single copy of the data to all devices on the same network segment.
oo Broadcast communication must be used, since protocols such as
° ARP and DHCP rely on it.
F VER. A broadcast domain includes devices that receive broadcast packets
A originating from senders within the same network segment.
X SS f, Routers operate in the network layer and separate both collision
Seas domains and broadcast domains.
e
16


### Slides — strona 17

Network Types and Devices
Half Duplex
Only one party can send or receive data at a single a a
moment. For example, a walkie-talkie works in half duplex.
fh Li
Full Duplex '
Both parties can send and receive data at the same time. Se St SS
For example, a phone call is performed in full duplex.
When 2 devices are set to different
duplex modes, a duplex mismatch
occurs. This reduces the quality of
the communication.
LY,


### Slides — strona 18

Network Types and Devices
Router
While switches allow devices to
interact in the same network,
routers allow them to communicate
with different networks. E == —
A router connects networks
and allows communication
between end devices in ST
different networks. same Pe es eee ey eer /
Routers use IP addresses to
route information among
networks.
=
18


### Slides — strona 19

Network Types and Devices
| Firewat |
pela = |
=e = oo =
(i) => oe,
es
Access points allow end Firewalls are effective A Wireless LAN Controller The home router combines
devices to connect toa security tools against allows the configuration of the features of all the
network wirelessly and threats that originate from multiple APs to be managed intermediary devices
manage information outside a network. from a central device. covered in this lesson so far,
transmission. Firewalls implement filters This is useful in large ina single device.
Awireless device user can that allow or block the organizations where It acts as an AP, a switch,
connect to a wired network transfer of information ina multiple APs are deployed and a firewall with the most
via a properly configured given direction. in different sections of a basic configuration.
access point. building.
19


### Slides — strona 20

CO
Introduction to Networks
NETWORK MEDIA AND CABLES


### Slides — strona 21

Network Media and Cables
Media
What does Media do?
Information cannot be transmitted over a network without a
means of transportation.
The term ‘media’ refers to the physical cables or wireless
technologies used to pass the information from one device to
another.
Different types of media feature varying speeds and distances
of data transfer.
6
Connections between continents were made possible using “submarine cables” that were
stretched across thousands of kilometers through the oceans.
21.


### Slides — strona 22

Network Media and Cables
CAT5e Cable
The most common way to
connect to a network is via an
Ethernet cable with an RJ-45 S
connector. =f
Cables are made of copper and i > Ss _~
can transmit information in the ss 3 eS —
form of electrical signals. — il ne a
= BS cessssuy 4
Signals deteriorate as the Con —— _/
distance grows, and due to the
influence of RFI & EMI, which
limits the cable length.
22


### Slides — strona 23

Network Media and Cables
Ethernet Cable Types
Cable Categories
CABLE SPECIFICATIONS
CAT-5 Maximum length of 100m, maximum speed of 100 Mb/s
CAT-5e Maximum length of 100m, maximum speed of 1 Gb/s
CAT-6 Maximum length of 100m, maximum speed of 1 Gb/s (Note: Supports 10 Gb/s for 55m)
CAT-6a Maximum length of 100m, maximum speed of 10 Gb/s
CAT-7 Maximum length of 100m, maximum speed of 10 Gb/s (Note: Supports 100 Gb/s for 50m)
EEE
23


### Slides — strona 24

Network Media and Cables
Cables
UTP
Unshielded Twisted-Pair is the most common copper Fou, SHIELDED CABLE | Tyileted
air

cable in use. It consists of four twisted pairs of colored -
wires. The act of twisting the wires is done to prevent Shielas Sonqucion
signal disruption (cross-talk). eo Yor!

Shielded Twisted-Pair cables are similar to UTP, but have beet

ire
additional protection against EMI and RFI interferences.
Each twisted pair is wrapped in foil. Outer ae
Jacket
a
EMI & RFI are electromagnetic and radio frequency interferences that can affect signals.
24


### Slides — strona 25

- - Ina straight-through cable, the colors match
Ethernet Cable Configurations rf y
Straight-Through r -
Straight-Through
Wires are placed in a straight formation from side A to
side B. This form is used for cables that are meant to Tees next
connect network devices of different types, such as a 2
switch and ai endpoint. gs a SSS
5 ae +
. Each cable is connected straight to the matching ee
pin on the other side. ED 61K.
O_O
DS
Rollover is another type of cable used to connect intermediary devices.
25


### Slides — strona 26

O In a crossover cable, pins 1&2 and 3&6 are crossed
Ethernet Cable Configurations age
Crossover 5: 7g j SS E,
= Wires crisscross from side A to side B. This form is ———a =.
a used in cables that are meant to connect similar 2-23 jj iff
: = network devices. a_i j
. Pins 1 &2 and crossed
. Pins 3 & 6 are crossed Crossover
e T568A to T568B eS STRAIGHT-THRU He re CROSSOVER Pc ”
Ree 3 3 TH RX 3, i 3 ee
—————Ssss 4 4
O [a —— ee FY 5—a— 5
RL 6 EE 6 Tx- RY 6 6 RX
== 2 ——— eel 2
= —_—_——==— 8 8 Ss EB &
26


### Slides — strona 27

Ethernet cables have a length
limit of 100m. A different type
of cable is used for greater
distances.
px
Optical Fiber Cables transmit 9 a
information using light, at high - CLA
8 lig Bl > a _
speed, over long distances. ' # _ [=
These cables are not sensitive ab 7
to RFI & EMI, but aren’t as J <a
flexible as Ethernet cables, and i a »
are more expensive. , -
—


### Slides — strona 28

CO
Introduction to Networks
NETWORK TOPOLOGIES AND ARCHITECTURE


### Slides — strona 29

Network Topologies and Architecture
Network Topology
Definition
Cal Pa
= i _ A network topology describes the structure of a network.
vi ¢
= | It represents all the connections between all components ina
7) network.
ot
Ld Several types of topologies can be used to construct networks.
6
A topology represents the resources of a network, but not locations and distances.
29


### Slides — strona 30

Network Topologies and Architecture
@ @Q
Q oN
@ EN, res
© pw
@ &
A connection between two In a star topology all end In a mesh topology each A hybrid topology is a
computers, networks or devices are connected to a end device can have combination of other
other devices. central intermediate device. multiple connections to topologies.
If the connection fails, the This type of topology is easy other end devices. Although a hybrid
communication is disrupted. to set up and maintain. It is This configuration is highly configuration takes
also highly scalable. resilient, due to its advantage of the strong
allowance of multiple points of other topologies,
connections, but it is also it also has to deal with the
expensive and very difficult disadvantages of those
to maintain. topologies as well.
30


### Slides — strona 31

Network Topologies and Architecture
3-Tier Architecture
Definition
The concept of a 3-Tier Architecture can be applied to any type of
network.
A The model helps design, implement, and maintain a scalable, reliable,
y ON and cost-effective network.
Its simplistic structure makes it very easy to manage.
yp —ti‘«<CSN The combination of these attributes means that it is the best choice
for large enterprises, in which thousands of computers need to be
interconnected, sometimes over an area that includes several
buildings.
B
Each layer has its own features and functionalities, which reduces network complexity.
31


### Slides — strona 32

Network Topologies and Architecture
3-Tier Structure
| a: |
A 3-Tier architecture consists of three layers
that provide isolation between devices, z0000|_ Ss Core
greater flexibility, more security options, Layer
and resilience.
te ge" 1
1 eS !

The separated layers are: ' an ate '

Core — routing layer connecting to servers * a

and the Internet. Distribution

Distribution — separation between core and BO) ees [z0000 Layer

access layers, and boundary control. _

Access — communication between end fag Se, ~e Sy

devices. wey ae ae 2 4g Ss

: Pig 1 —— S,
ze" om <4 Sig a
The layers can be managed independently 7 v 3s ~
Access Layer
SE 32


### Slides — strona 33

Network Topologies and Architecture
Collapsed Layer Structure
Core +
This architecture is similar to 3-Tier, but has =0000} ------- [BGO00] | Distribution
a different number of layers and a different Ke Layer
scalability potential. Wa f i i; Te
‘ s o ‘ s
¢ ‘ on re ° af \ a
¢ es

In this architecture, the core and distribution 3 H ax TSK ‘ ve

layers are collapsed together to form a single g* , * es CO = MM

layer. of Lb? Tye Sq Ry
This means it has the advantages of the 3-Tier
architecture, but a smaller network scale.

Access Layer
ee a


### Slides — strona 34

Network Topologies and Architecture
Physical & Logical Addresses
Why do we need a computer address?
When the first networks were created for local computers to
5 communicate with each other and share data, design engineers
. 5 realized they needed to know how computers would talk to
°@: each other and who they could talk to.
The idea was for each computer to have a unique name or
aa» identification, and the concept of a MAC address was born.
A MAC address is the unique identity of a computer within a
network, while IP addresses are used to identify machines
operating in different networks.
é
Each network card in a device has both a MAC address and an IP address at any given moment.
34


### Slides — strona 35

Network Topologies and Architecture
Physical Address
Media Access Control
A MAC address is a unique hardware identifier attached to each
network card. The address is static and should not be changed.
a = It consists of six hexadecimal nodes ranging from 00 to FF.
= A MAC address includes two parts:
¢ The first three nodes represent the manufacturer’s identifier
¢ The last three nodes represent a serial identifier
o
A MAC address will usually be written like 00:0d:83:b1:c0:8e, or sometimes 000d.83b1.c08e
35


### Slides — strona 36

Network Topologies and Architecture
An IP is used to uniquely identify computers on the network and create network partitions.
IPv4

IPv4 addresses are the most commonly used today. They consist of four octets of numbers between

0-255, which can generate approximately four billion different addresses.

Some addresses, such as X.X.X.255, are special, while others, such as 192.168.X.X, are dedicated to

specific uses.

IPv6
Due to advances in technology, IPv4’s four billion addresses were threatened with depletion, and
IPv6 was developed with six hexadecimal octets that can generate approximately 340x10‘36
addresses.
IPv6 addresses have not yet been fully integrated in modern use cases.
36


### Slides — strona 37

Network Topologies and Architecture
Class by Mask
The network The hosts
<< ———_ rd
Subnet masks define which addresses'in an IP address: 192 . 168. @ .0
octet can be used in an IP address, while C
remaining on the same network. Subnet mask: 255 . 255 . 255].0
The network The hosts
Devices (computers or network) must be in
the same network and subnet to
communicate without routing B IP address: 172 A116 | .0.0
Subnet mask: 255 .255/.0.0
The first IP address of each subnet is the The network The hosts
network address and cannot be used for —_—— ———
hosts or devices
A IP address: 10 |. 0.0.0
The last IP address of each subnet is the Subnet mask: 255}. @.0. 2
broadcast address and cannot be used
a »


### Slides — strona 38

CO
Introduction to Networks
NETWORK PROTOCOLS AND COMMANDS


### Slides — strona 39

Network Protocols and Commands
Communication Protocols
Protocols
To properly communicate with each other, different devices
require protocols.
Protocols are predefined sets of rules describing how something
should work or behave.
Protocols help maintain order among different technologies.
B
Protocols can be considered as ‘languages’ of data transfer. To communicate properly, two
or more devices must first agree to use the same ‘language’.
39


### Slides — strona 40

Network Protocols and Commands

The Internet Protocol Domain Name Service || The Dynamic Host The Hypertext HTTPS is a secure

is used to establish is a protocol used to Configuration Transfer Protocol is implementation of
communication over translate domain Protocol is used to used to transfer text- HTTP. It encrypts the

the network, without names to IP allocate IP addresses based data, such as transferred data to

delivery verification. addresses, and vice to new computers web pages, over the prevent it from being

versa. that join the network. Internet. intercepted.
40


### Slides — strona 41

Network Protocols and Commands
Network Commands
The Importance of Commands
Commands are used in network configuration, maintenance,
=a troubleshooting, and more.
= It is essential for any network to frequently run commands that check
the state of the network and monitor it.
Although some systems enable network configuration via a GUI, the
configuration is still often done via the CLI.
&
An example of a powerful use of network commands is for error detection.
41


### Slides — strona 42

Ping X.X.X.X
C:\Windows\system32> ping 8.8.8.8
Ping is the most common
command " administrative Pinging 8.8.8.8 with 32 bytes of data:
networking activity. .
Reply from 8.8.8.8: bytes=32 time=224ms TTL=54
It is used to check connectivity Reply from 8.8.8.8: bytes=32 time=681ms TTL=54
between computers over the Reply from 8.8.8.8: bytes=32 time=319ms TTL=54
network. Reply from 8.8.8.8: bytes=32 time=103ms TTL=54
It also provides information Ping statistics for 8.8.8.8:
such as connection speed and Packets: Sent = 4, Received = 4, Lost = @ (@% loss),
reliability. Approximate round trip times in milli-seconds:
Minimum = 103ms, Maximum = 681ms, Average = 331ms


### Slides — strona 43

ipconfig
ipconfig displays a computer’s C:\Windows\system32> ipconfig
IP configuration.
Windows IP Configuration
It can also request a new IP Ethernet adapter Ethernet:
address, if DHCP is configured.
Connection-specific DNS Suffix .:
— displays Link-local IPv6é Address... . . : £b21::b23e:28e9:c76b:7b35%11
extended information. IPv4 Address. ......... . : 192.168.5.11
— drops an Subnet Mask. ......... . : 255.255.255.0
IP address. Default Gateway. ........ : 192.168.5.1
— requests a
new IP address.


### Slides — strona 44

nslookup x.x.X.X
Computers use IP addresses to C:\Windows\system32> nslookup www.cyber.com
communicate with each other, Server: pfSense.cl22b.lan
while humans use names that Address: 192.168.0.1
are easier to remember than
numbers. . .
Non-authoritative answer:
coenaueniaaet Name: cyber.com
the name ofa computer by it Address: 199.244.49.102
puter by its
IPaddress. Aliases: www.cyber.com
It can also do the opposite - C:\Windows\system32> nslookup 199.244.49.102
query an IP address by the Server: pfSense.cl22b.lan
domain name. Address: 192.168.0.1


### Slides — strona 45

tracert xX.X.X.X
C:\Windows\system32> tracert 8.8.8.8
Information in the network
passes through multiple Tracing route to dns.google [8.8.8.8]
stations on the way to its over laymexinum) of 22 (ops:
a <1 ms <1 ms <1 ms pfSense.cl122b.lan [192.168.0.1]
destination. 2 115 ms 7@ms 59 ms 192.168.1.1
3 - - = Request timed out.
— — 4 + * a Request timed out.
displays all the stations 5 241 ms 170 ms 218 ms 172.17.10.182
along the route taken by the 6 * * * Request timed out.
information to its destination. 7 * * * Request timed out.
8 cf . Request timed out.
9 - = 259 ms core-213-57-0-69.PT.hotnet.net.il [213.57.0.69]
2 2 10 281 ms 245 ms 225 ms core-213-57-3-150.HFA.hotnet.net.il [213.57.3.150]
It can work with a domain 11 201 ms 174 ms 228 ms 108.170.251.129
name or an IP address. 12. 188 ms 230 ms 326 ms 74.125.37.167
13. 131 ms 83 ms 109 ms dns.google [8.8.8.8]
Trace complete.


### Slides — strona 46

Netsh [ command \ option ]
ni . : C:\Windows\system32> netsh interface ip set address “Ethernet”
ee ee static 192.168.10.5 255.255.255.@ 192.168.10.1
information is to use the
command.
C:\Windows\system32> netsh interface ip show config
It allows the configuration of
the IP address, DNS, default Configuration for interface "Ethernet"
gateway, and various network DHCP enabled: No
functions. Default Gateway: 192.168.10.1
Gateway Metric: 1
The example on the right InterfaceMetric: 5
shows how to'set an/\P address Statically Configured DNS Servers: None
and verify settings using : Register with which suffix: Primary only
Statically Configured WINS Servers: None


### Slides — strona 47

Network Protocols and Commands
Lab NET-01-L1 Mission
— Learn and practice CLI network commands in Windows
Local Network Configuration using CMD.
30-60 Min. © -
ww @ Local Network Configuration
a : ® Test Connectivity
ee, ™~ s ~ ® Domain names & IP
; rd = XN & N e wa
a) ) » : ~~ Environment & Tools NEaAteq Fes
| » . ®@ Windows 7/8/10 @ Lab document
| ve . W ® CMD
‘ ‘ :
.) o |
‘ ia —


### Slides — strona 48

CO
Introduction to Networks
WIRELESS TECHNOLOGIES


### Slides — strona 49

Wireless Technologies
Wireless Network Structure

Wireless networks for computer

communication are possible. Coo

Wireless media features better flexibility e H

than wired media, due to the absence of \

cables connected to end devices. i I ,

x. 1 oa
*& i} Pt
_
Information is transmitted using radio Ye H get ,
frequencies, which, however, do pose Mg wf
some security challenges. @ ~%
a z


### Slides — strona 50

Wireless Technologies
—
The ideal environment for Many common devices, The absence of physical The technology operates in
this technology is open such as microwave ovens, media exposes the network half-duplex, which means
space. and various wireless to the public and allows only one device can send
Some building materials can communication devices, others to discover it and and receive information at a
limit the range that wireless also transmit radio gain access to it, without time.
systems cover. frequencies. authorization to do so. When more and more users
These signals may interfere connect to the network, the
with signals transmitted in available bandwidth for
the wireless network and each user will decrease
affect their quality. accordingly.
50


### Slides — strona 51

Wireless Technologies
NIC Conversion
AP
Access point is the component that allows end devices
| | to connect to a network wirelessly using radio waves.
roses | The access point itself will be connected to the network
via cable. .
_—— _—
G bilnl Bore)
Wireless NIC Adapter _ ef —— ——— 11110
=== Fora device to connect to a wireless network it must
b Gi have a wireless NIC adapter to send and receive the
[ information.
Wireless NIC adapters can be implemented by an external device, or integrated in the computer.
Si


### Slides — strona 52

Wireless Technologies
Wireless Technologies
Wi-Fi
Wi-Fi, or wireless fidelity, is a technology based on IEEE 802.11 standards that allows
wi connection to a network wirelessly using radio waves.
Wi-Fi is used for LAN networks in shared spaces.
Wi-MAX
io~,
hk Wiemaxis an implementation of wireless network connection over a wide area.
It is used for LAN and MAN implementations.
Bluetooth
Bluetooth is an implementation of WPAN (Wireless Personal Area Network).
It is mainly used to pair devices and allows communication at up to 100 meters.
52


### Slides — strona 53

Wireless Technologies
Wireless Standards
Over the years, network standards were developed and modified to improve speed and bandwidth.
Wireless Standard History
STANDARD MAX SPEED FREQUENCY BACKWARD COMPATIBLE
802.11a 54 Mb/s 5 GHz NO
802.11b 11 Mb/s 2.4 GHz NO
802.11g 54 Mb/s 2.4 GHz 802.11b
802.11n 600 Mb/s 2.4 GHz & 5 GHz 802.11a/b/g
802.11ac 1.3 Gb/s 5 GHZ 802.11a/n
802.11ax 14 Gb/s* 1 GHz - 7.125 GHz 802.11a/b/g/n/ac
53


### Slides — strona 54

Wireless Technologies
Copper Fiber Wi-Fi
10 Mb/s — 10 Gb/s 10 Mb/s — 100 Gb/s 54 Mb/s — 14 Gb/s
D id the ti itter’:
Up to 100 meters Up to 100 Km epends:onmne ransmi ere F
strength and receiver’s sensitivity
Inexpensive Expensive Relatively Inexpensive
Vulnerable to the effects of EMI & REI Expensive equipment and The signal can be affected by
implementation surrounding structures
2 [amor Gi
54


### Slides — strona 55

’ = j FO Saw ~
= a # 4 i
4 ~~ ie
v). a " % * a4 a A
i >» ; Ss
> \ >
Chie —— . =
Fed Axncoes ta os 2 Spe
& Mh if
A ; 4 ~S : ra
=m Z By: ie ~~ zs
= Payee SQ


### Slides — strona 56

a i ™" : = a aw NETWORK ee Bal Ci = L D


# Chapter 2: Network Fundamentals


### Slides — strona 57

= # ' 4 — — = + i j
an Cybersecurity Professional Program
: : mana NEEWORK ! re hee += ca C ,
Computer Networking
Copyright © 1996-2023 HackerU Ltd. All Rights Reserved.


### Slides — strona 58

Computer Networking
Introduction Network Switch & IOS Switch Securit IP and Routing
to Networks Fundamentals Fundamentals y Concepts
Diagnostics and VLANs Dynamic IPv4 & IPv6é Subnetting
Troubleshooting and Trunk Routing Static Routing Concepts
Access Infrastructure Fiival Proiect
Control List Services d
2


### Slides — strona 59

Network Fundamentals
Overview
Lesson Objective Network Protocols and Models
OSI Model
This module introduces the network
components that together enable TCP/IP Model
communication between different
devices and services. Transport Protocols and Logical Ports
It also covers network architecture
models and their layers. Introduction to Wireshark Addresses
ARP and Encapsulation
G
3


### Slides — strona 60

CO
Network Fundamentals
NETWORK PROTOCOLS AND MODELS


### Slides — strona 61

. Web Browsin
Client g
ww 3 « ’ Dear Server 18.77.22.44,
eee A client represents the endpoint device (not www caryou please send my
a necessarily a PC) that requested an operation. a = Facebook home page.
Server
Sure! 10.2.2.7, here you
go, enjoy!
A server represents the endpoint device that receives
a request and performs the requested operation.
5


### Slides — strona 62

Network Protocols and Models
Client-Server
Client-Server Relationship
(o) The Client-Server model is a distributed application structure that
CARY + manages tasks and workloads by sharing them among providers
— of resources and services (servers), and delivers responses to
: service requesters (clients).
B
An alternative method is to use broadcast or multicast channels to distribute information.
6


### Slides — strona 63

Network Protocols and Models

HTTPS as

& ey a,
HTTP is an unsecure protocol HTTPS is the encrypted version Translates domain names to IP File Transfer protocol is used to
used to transfer information of HTTP. addresses according to transfer files over the network.
over-the web. It is used for secure predefined databases: For example, the FTP service can
Due to the fact that HTTP traffic communication and is widely The DNS protocol is used for be used to transfer files to
is not encrypted, it can be used on the Internet. address resolution in a network. another device over the
sniffed on the network. Communication is encrypted For example, when a URL is network.
For example, if credit card using TLS (Transport Layer entered in a browser, the DNS
information is entered in an Security) or SSL (Secure Socket protocol translates the domain
HTTP website, it can be Layer). that was entered to an IP
captured in simple text format. address.
de


### Slides — strona 64

Network Protocols and Models

>= ~ La

Eats! @ ¢

-
The DHCP service is responsible Simple Mail Transfer Protocol is Secure SHell is a secure Internet Control Message
for assigning an IP address to the standard protocol for mail command line protocol that Protocol is used by network
each device on a network transfer over the Internet. allows the user to run remote devices to generate error
configured to use DHCP, such as Forexamplewhenan Envail ig commands ona remote messages when IP packets are
PCs, Routers, Firewalls, Servers, Pe: machine. not able to reach their
ate sent over the network, the destinations

: SMTP protocol manages the Any data that passes through .
For example, a PC configured operation. SSH is encrypted.
with DHCP will automatically be For example, when a remote
assigned an IP address upon connection is made to a device,
startup. the connection is made using
SSH on port 22.
8


### Slides — strona 65

Network Protocols and Models
Network Model Concept

The idea behind creating a networking model was to set a standard for
Ca CJ the development and usage of network components.

Standards allow devices to communicate without requiring continuous

= = configuration in different device platforms.

« " mmeulipe In addition, dividing the networking process into smaller sub-processes

helps debug issues and pinpoint solutions.

&
TCP/IP and OSI were developed around the same time, with the aim of solving the same problem.
2]


### Slides — strona 66

Network Protocols and Models
Today, OSI and TCP/IP are very similar due to the way they evolved over time.
OSI is often used as an educational model, while TCP/IP is used more as a practical model.
OsI

OSI is a network model in which each functionality of the network is represented by a layer.
There are 7 layers, in which the functionality of each is dependent on the one below it.

OSI was developed by the International Organization of Standardization.

TCP/IP

The first TCP/IP specification was submitted several years after the OSI model.

The original TCP/IP model consisted of 4 layers, but was later updated to the current 5 layers.

However, the 4-layer version is still more commonly used.

TCP/IP is used for network analysis, due to its lesser involvement with the top 3 layers.

10


### Slides — strona 67

CO
Network Fundamentals
OSI MODEL


### Slides — strona 68

OSI Model
OSI Model

* OSI defines a networking framework to implement protocols in layers.

* OSI conceptually divides computer network architecture into a logical
seven-layer progression.

¢ Lower layers deal with electrical signals, chunks of binary data, and
routing data across networks.

¢ Higher levels cover network requests and responses, data representation,
and network protocols, from a user's viewpoint.

&
OSI was developed by the International Organization for Standardization (ISO) in 1974.
42


### Slides — strona 69

OSI Model
OSI Model
—_ OosI
Transmit Data Receive Data
The OSI model is divided into 7 layers: APPLICATION APPLICATION
Application, Presentation, Session,
Transport, Network, Datalink, Physical. PRESENTATION PRESENTATION
When network traffic is generated, it
top layer to the bottom layer.
TRANSPORT TRANSPORT
When received, traffic goes through
the model in the reverse direction: NETWORK NETWORK
from bottom to top (decapsulated).
; DATA LINK DATA LINK
PHYSICAL Physical Layer PHYSICAL
13


### Slides — strona 70

OSI Model
Layer 7 - Application Upper Layers
Users interact directly with applications that operate at
Layer 7. Examples of Layer 7 applications include web
=== browsers such as Google Chrome, Firefox, and Safari, APPLICATION
and other applications, such as SSH and FTP.
G PRESENTATION
Layer 6 - Presentation
The Presentation Layer prepares or translates data from SESSION
application format to network format, and vice versa.
An example of the Presentation Layer operation is the
encryption and decryption process. a =
Layer 5 - Session
The session layer is responsible for creating a session
Y between two devices.
It is also responsible for session checkpoints and recovery.
14


### Slides — strona 71

OSI Model
Layer 4 - Transport
The Transport Layer handles coordination of data transfer between end
systems and hosts, including how much data to send, at what rate,
destination, etc. Data in this layer is organized into segments.
The transport layer determines if the connection should be instantiated, how
a to verify data integrity, how to recover from a connection error, and if
retransmission is necessary.
The protocols in this layer provide flow control, multiplexing, and reliability.
&
TCP and UDP are discussed in more detail in later slides.
15


### Slides — strona 72

OSI Model
Layer 3 - Network
The Network Layer organizes data into packets called IP datagrams that
contain logical source and destination addresses.
Routers operate in this layer.
The Network Layer’s job is to allow hosts to send packets across multiple
paths to any other network, and deliver them to their destinations, via
routers operating on this layer.
&
Diagnostic tools, such as ping and tracert operate in this layer.
16


### Slides — strona 73

OSI Model
Layer 2 — Data Link
queen. The Data Link Layer provides node-to-node data transfer (between two directly connected
ii ft | . nodes) and can provide the means to detect errors that may occur in the Physical Layer.
— Switches operate in this layer. Data in this layer is organized into frames.
Layer 1 -Physical
The Physical Layer defines the details of how data is physically sent through the network.
This layer determines how bits are electrically or optically transferred by hardware devices that
“2 interface directly with a network medium, such as coaxial cable, optical fiber, or twisted-pair
- - copper wire.
Hubs operate in this layer. a
The Data Link Layer includes two sub-layers: MAC (Media Access Control) and LLC (Logical Link Control).
LY,


### Slides — strona 74

OSI Model
Each network protocol is assigned to a particular OSI layer.
Common Protocols in Each Layer
LAYER PROTOCOLS
Application DNS, DHCP, SSH, HTTP\S, FTP, SNMP, SMTP, POP3
Presentation Encryption, Encoding, SSL, ASCII, EBCDIC, TIFF, GIF, PICT, JPEG, MPEG, MIDI
Session NFS, NetBios names, RPC, SQL
Transport TCP, UDP, RTP, SCTP
Network IPv4, IPv6, ICMPv4, ICMPv6, IPX
Data Link Ethernet, PPP, FDDI, ATM, IEEE 802.5/ 802.2, HDLC, Frame Relay
Physical Ethernet (IEEE802.3), Wi-Fi (IEEE 802.11), FDDI, B8ZS, V.35, V.24, RJ45
18


### Slides — strona 75

OSI Model
Memorize the Layers
Memory Tips
e All People Seem To Need Data Processing
e Please Do Not Throw Sausage Pizza Away
e Please Do Not Touch Steve’s Pet Alligator
2)
19


### Slides — strona 76

Encapsulation
Data Encapsulation
What is Encapsulation?
When a message is sent from source to destination, it must have a
specific format or structure. Message formats depend on the type of
Ea message and the channel used to deliver it.
The opposite process of encapsulation is called decapsulation. This is
when the host is on the receiving side.
The same process occurs in OSI and TCP/IP using the same protocols.
20


### Slides — strona 77

Encapsulation
Data Encapsulation
Encapsulation
MP,. For example, to send mail, we place a message in an envelope —
encapsulation. The envelope is written in a format the mail service
accepts and is sent to the destination. The receiving side opens the
envelope and takes out the message — decapsulation.
The envelope is similar to a network Frame.
21


### Slides — strona 78

ARP and Encapsulation
Encapsulation in Layers 4-7
As an example, we can focus on the process of sending data.
The first step in the process is ... YOU!
Data
When you click on a link:
HTTP GET
The Application layer creates an HTTP header requesting the APPLICATION
web page from the server.
. Data
The Presentation layer encodes, encrypts, or compresses the
data traveling down from the Application layer, if , 0101101010101010
6 PP on lave necessary. PRESENTATION 1101010101001101
For example, it may convert text to a binary string.
The Session layer determines the direction of the data: one- Data
way or two-way, and whether the connection is secure or not. 0101101010101010 This is called a
In addition, a session ID is assigned to the connection. SESSION 1101010101001101 Segment
TCP Header Payload
The Transport layer adds a header containing the source and . . 0101101010101010
oe . : : TRANSPORT Sre: 51001 Dst:80 | 4194910101001101
destination logical ports, and other control information.
This layer also divides data from upper layers into smaller pieces
called Segments. Each segment is a maximum (MSS) of 1460
bytes.
22


### Slides — strona 79

— Encapsulation in Layers 1-3

The Network Layer adds a header to the segment with This is called a
the IP source and destination addresses, and other Packet
control information (such as TTL) . During this step, the
segment is encapsulated in a packet. IP Header TCP Header Payload
Packets are limited to a maximum size (MTU — Maximum NETWORK Src: 10.0.0.1 | Src: 51001 § 010110101 This is called a
Transmission Unit) of 1500 bytes. Dst:80.7.1.2 Dst:80 001010100 Frame

Ethernet Header IP Header TCP Header FCS
The Data Layer adds'a: Header and Trailer to the packet: DATA LINK sre: 00:aa:bf:22:11:11] Src: 10.0.0.1 }src: 51001| 01011 | crc
The header contains the physical source and destination Dst: 00:cc:ff:69:11:11| Dst:80.7.1.2 | Dst:30 | 01010 | 0xA78
addresses. The trailer, also known as FCS, is for frame
error checking only.

00101001010101010

PHYSICAL >

10101001101010001
The Physical layer accurately transmits the Frames along
the physical medium. For example, it sends electric
pulses over an Ethernet cable, or wireless radio waves.

23


### Slides — strona 80

CO
Network Fundamentals
TCP/IP MODEL


### Slides — strona 81

TCP/IP Model
Transmission Control Protocol/Internet Protocol
TCP/IP Model
This model is a suite of communication protocols used to interconnect
network devices on the Internet.
The model describes how data is exchanged over the Internet, including
how data should be divided into packets, addressed, transmitted, routed,
es and received by the destination.
ae TCP/IP was designed to make networks reliable and enable them to
automatically recover from the failure of any device on the network.
25


### Slides — strona 82

TCP/IP Model
— TCP/IP
Transmit Data Receive Data
Layers in the TCP/IP model are similar to
those in the OSI, except for the top three
layers.
APPLICATION APPLICATION
TCP/IP uses the client-server model of
communication in which a user or machine
is given access to a service by another
computer on the network.
TRANSPORT TRANSPORT
Collectively, the TCP/IP suite of protocols is
classified as ’Stateless”, which means each
client request is considered new, and is INTERNET INTERNET
unrelated to previous requests.
Network Access Physical Layer Network Access
ey
26


### Slides — strona 83

TCP/IP Model
Layer 4
The Application Layer defines TCP/IP application protocols and how host
programs interface with Transport Layer services to use the network.
>= The Application Layer includes all higher-level protocols, such as DNS, HTTP,
Telnet, SSH, FTP, TETP, SNMP, SMTP, DHCP, X Windows, RDP, and others.
&
The TCP/IP top layer is equivalent to the combined three top layers of OSI.
2/


### Slides — strona 84

TCP/IP Model
Layer 3

The Transport Layer handles coordination of data transfer between end systems
and hosts, including how much data to send, at what rate, destinations, etc.
The transport layer determines if the connection should be instantiated, how to

Ti verify data integrity, how to recover from a connection error, and if retransmission
is necessary. Data in this layer is organized into segments.
The protocols in this layer provide flow control, multiplexing, and reliability.

&
The Transport layer in TCP/IP corresponds to the Transport Layer in OSI.
28


### Slides — strona 85

TCP/IP Model
Layer 2

The Internet Layer organizes data into packets called IP datagrams that
contain logical source and destination addresses.
Routers operate in this layer.
The Internet Layer’s job is to allow hosts to send packets across multiple

: paths to any other network, and deliver them to their destinations, via
routers operating on this layer.

&
The Internet layer in TCP/IP corresponds to the Network Layer in OSI.
29


### Slides — strona 86

TCP/IP Model
Layer 1

The Network Access Layer is the lowest layer of the TCP/IP protocol model.
Packets from the Internet layer are sent to the Network Access layer for delivery
within the physical network. Data in this layer is organized into frames.

e" Protocols in this layer provide the means for the system to deliver data to other

ay pe devices in a directly connected network, using physical addresses (MACs).
The protocols and standards defined for this layer dictate how data is transmitted
on the media (Ethernet cable, wireless connection, others).

The Access Layer of the TCP/IP model corresponds with the Data Link and Physical layers of OSI.

30


### Slides — strona 87

CO
Network Fundamentals
TRANSPORT PROTOCOLS AND LOGICAL PORTS


### Slides — strona 88

Transport Protocols and Logical Ports
Transport Protocols
TCP & UDP
TCP and UDP are protocols that are used to transmit
data over the network.
TCP and UDP operate in Layer 4 (Transport Layer).
6
32


### Slides — strona 89

Transport Protocols and Logical Ports
Transmission Control Protocol
TCP is more trusted and commonly used than UDP.
It verifies the availability of all parties before initiating a connection,
by performing a three-way handshake. It then marks packets and
makes sure they are received in the correct order.
TCP is described in detail in RFC 793.
33


### Slides — strona 90

Transport Protocols and Logical Ports
User Datagram Protocol

UDP is less strict about data integrity and is more speed-oriented.
UDP simply sends packets, without checking the data, even if nobody is
ready to receive them.

YY) This type of communication works better when streaming content, such

6 as audio, where some packets may be skipped without affecting the
entire stream.

UDP is described in detail in RFC 768.
34


### Slides — strona 91

Transport Protocols and Logical Ports
TCP UDP
Connection-oriented protocol. A connectionless protocol.
. 4. . . ae Suitable for applications that need fast, efficient
Suitable for applications that require high reliability, . PP
‘of aa wae transmission. Also useful for servers that answer small
where transmission time is less critical. . :
queries from large numbers of clients.
. _ Packets may arrive out of order, UDP does not
Rearranges data packets in the order specified. y
rearrange them.
I | \/ S(O
Guarantees that transferred data remains intact. If a There is no guarantee that messages or packets that
packet is corrupt upon arrival, it is resent. are sent will reach their destinations.
. UDP does error-checking but simply discards
Errors are detected via checksum. 8 Ply
erroneous packets. Error recovery is not attempted.
TCP is relatively slow. UDP is relatively fast.
35


### Slides — strona 92

Transport Protocols and Logical Ports
TCP uses flags to provide additional useful information or control the connection.
TCP Flags
Flag Role
SYN Synchronization - this is the first flag between two hosts, and is used to establish a 3-way handshake.
ACK Acknowledged - acknowledges successful receipt by the host.
RST Reset - Terminates a connection if a TCP failure occurs or a conversation is not permitted.
FIN Finish - Requests connection termination.
PSH Push - Immediately sends all buffered data.
URG Urgent - Data with a URG segment is forwarded to the Applications Layer immediately.
36


### Slides — strona 93

Transport Protocols and Logical Ports
—_— 3-Way Process
Client Server
A 3-way handshake is responsible for
communication between network
devices that use TCP. HTML
The handshake is known as “3-way”
because it includes 3 steps:
1. The client sends “SYN”. @
2. The server responds with “SYN-ACK”.
3. The client finalizes with “ACK”. _
When the process ends successfully, a 2)
connection is established between the client
and the server, and data can immediately be
transferred between them. rs)
os
37


### Slides — strona 94

Transport Protocols and Logical Ports
—_— Termination Process
Client Server
Session Termination is the last stage of a
TCP connection. This is when
communication ends and the session is HTML
closed.
Step 1 - One of the sides (client) requests to P
close the connection by sending a FIN flag to @)
the other side (server). all EE rercee
Step 2 - The receiver of the FIN flag (server)
returns an ACK flag, to approve the request. 2)
Step 3 -The server then sends a FIN flag to the gentile
cen, oO
Step 4 - The client approves the FIN request :
by the server, and responds with an ACK flag. ; —ooeSESFSFes#sS
The connection is then terminated. aoa
Y
———_———___,
38


### Slides — strona 95

Transport Protocols and Logical Ports
What are Logical Ports?
In computer science, a logical port is a number assigned to a “logical”
connection, which is used to represent a service or protocol on the end
device.
An IP address can send packets to the destination host, but not to the
destination service on that end device.
As an example, a street address can lead to the correct building, but it does
not specify the apartment number within that building.
&
39


### Slides — strona 96

Transport Protocols and Logical Ports
Logical Port Groups
There are 65,536 in TCP and 65,536 UDP ports, divided into three main groups, as follows:
Well-Known Ports
Port numbers in the “well-known” port range are assigned to commonly used and essential
0-023 protocols. The port numbers are permanent, and every network administrator must know them.
We use these numbers all the time, without realizing it.
The range includes protocols such as HTTPS, DNS, DHCP, Email protocols, and others.
Registered Ports
O24 “IANA assigned these ports for IT companies that want to register them for proprietary
ALS) 5541, applications. For example, Microsoft RDP 3389 and Dropbox 7600.
40


### Slides — strona 97

Dynamic & Private Ports
This group covers the remaining logical ports that are available for any application.
The port range is known as “client ports” and is usually used for logical client
AGi1S2 connection.
For example, a host connecting to a web server sends requests to port 80. This lets
65535 the web server know which service the client is requesting. However, the return
traffic must be sent to a source port, which is chosen randomly. When the connection
closes, the port can be reused for another connection, enabling the client to establish
multiple connections and manage responses from multiple sources.
&
41


### Slides — strona 98

Transport Protocols and Logical Ports
The following table lists common network protocols and their TCP and UDP ports.
Logical Port Numbers
Protocol TCP\UDP Logical Ports Protocol TCP\UDP Logical Ports

HTTP TCP 80 SSH TCP 22
HTTPS TCP 443 RDP TCP 3389

DNS UDP 53 SMB TCP 445
DHCP UDP 67, 68 FTP TCP 20, 21
SMTP TCP 25, 587 TFTP UDP 69

POP3 TCP 110 NTP UDP 123

42


### Slides — strona 99

C:\WINDOWS\system32>netstat -ab
Ports are used to receive and Active Connections
send data.
Proto Local Address Foreign Address State
TCP Q.0.0.0:135 Server_01:0 LISTENING
A web server will open Port 80 [svchost.exe]
in listening mode if it intends to TCP =: @.0.@.@:443 Server_01:0 LISTENING
receive HTTP traffic. [vmware-hostd.exe]
TCP Q@.0.0.0:445 Server_01:0 LISTENING
Adlient will openca random Can not obtain ownership information
port for each server it accesses han Sn wes Server_01:0 LISTENING
. vmware-authd.exe
when browsing the web. TCP @.@.0.0:912 Server_01:0 LISTENING
[vmware -authd.exe]
rai TCP Q.0.0.0:1536 Server_01:0 LISTENING
eee ports, use [svchost.exe]
stands forall. ee Loa Server_01:0 LISTENING
svchost.exe
stands:for the:names. TCP 0.0.0.0:1539 Server_01:0 LISTENING


### Slides — strona 100

Transport Protocols and Logical Ports
According to the materials learned in the previous part, answer the following questions as best as you can.
You may use external materials, such as Internet searches.
Communication Roles
Number Question
1 Briefly describe the operation or function of each layer. (For example, Layer 6 encodes, encrypts, and compresses the
information)
2 List two to three main protocols that operate in each layer. (For example IP, ICMP-Network Layer)
3 List two protocols that use TCP, and two that use UDP.
4 Describe the TCP 3-Way Handshake.
5 List the logical ports of the following protocols: HTTP, HTTPS, DNS, FTP, SMTP.
6 How many layers do the TCP/IP and OSI models have, and what are their names? (Try to answer from memory) FEE
44


### Slides — strona 101

CO
Network Fundamentals
INTRODUCTION TO WIRESHARK


### Slides — strona 102

Introduction to Wireshark
Wireshark
— Wireshark
File Edit View Go Capture Analyze Statistics Telephony Wireless Tools Help
4Ud@O 1D ROC eset sbeaaan
Wireshark is a free application Expression... +
that enables the capture and
viewing of data traveling back
and forth on the network. Capture
using this filter: [J [Enter a capture filter ~] All interfaces shown *
It is able to read the contents Normerfeces found
of each packet and apply
different filters.
Wireshark is commonly used to
troubleshoot network
problems, and develop and test
software.
Learn
User's Guide - Wiki - Questions and Answers - Mailing Lists
You are running Wireshark 3.0.1 (v3.0.1-0-gea35icd8). You receive automatic updates.
% — Ready to load or capture || No Packets || Profile: Default
jm
46


### Slides — strona 103

Capturing Data
— Wireshark
\a ax
A A AecOUBRE Cereerabeaacawkt
When invoked, Wireshark ey ES
initi i he Toe = ator Pol Leg fo im”)
presents aniinitial:screen with 10.000000 10.1.20.1 157.240.1., TLSv1.2 85 Application Data =
a list of available network i 2.078309 157.240.1.53 10.1.20.1 TCP 66443 5 8199 [ACK] Seq=1 Ack=32 Win=144 Len=@ =
interfaces. | 3.131308 10.1.20.1 62.0.136... TCP 55 [TCP segment of a reassembled PDU] =
| 4.131571 62.0.136.237 10.1.20.1 TCP 66 8093 > 11632 [ACK] Seq=1 Ack=2 Win=254 Len=@ SLE=1 SRE=2
5.155242 157.240.1.53 10.1.20.1 TLSv1.2 92Application Data =
Selecting an interface will start 6 0.195710 10.1.20.1 157.240.1.. TCP 548199 » 443 [ACK] Seq=32 Ack=39 Win=1027 Len=0 =
the capture of all traffic that | _81.132066 62.0.136.237 _10.1.20.1_TCP 6 [TCP Keep-Al CK] 8093 > 11632 [ACK] Seq=1 Ack= =25
passes through it | 91,228919 146.185.219.33 10.1.20.1 TCP 60.80 > 49803 [ACK] Seq=1 Ack=1 Win=501 Len=0 —
Wireshark can also be used to a : wastes : : aa via aerate —
open traffic captured by other Frame 1: 85 bytes on wire (680 bits), 85 bytes captured (680 bits) on interface ® By
Ethernet II, Src: HewlettP_3e:5b:9e (4:39:09:3e:5b:9e), Dst: Fortinet_4e:8b:12 (04:d5:90:4e:8b:12)
tools, such as TCP dump. Internet Protocol Version 4, Src: 10.1.20.1, Dst: 157.240.1.53
Transmission Control Protocol, Src Port: 8199, Dst Port: 443, Seq: 1, Ack: 1, Len: 31
Captured data can be exported 0000 04 d5 90 de 8b 12 #4 39 09 3e Sb Je 08 GO 45 00 Ne--9 s>[+--E |
j fil 0010 00 47 da 81 40 00 80 06 63 @8 Ga O1 14 G1 9d FO Gs c |
into .pcap or .pcapng Tiles. 0020 @1 35 20 @7 O1 bb 5a 42 67 7e a@ Oc C9 b250 18 -5 ---ZB ge... -P
2030 04 @3 86 Ge 00 00 17 @3 03 0 la ca 99 84 ed 00 al
OF - sreshark_Ethemet_20200721130008_a 14160, ca009 Fackets: 522 * Displayed: 496 (95.0%) Profile: Default
eal
—_—
=


### Slides — strona 104

Introduction to Wireshark
Packet List
Packet List is the main view of Wireshark. It lists captured packets in the order of their capture,
=| and offers various search and filter options.
Packet Details

= Packet Details is the part in the middle that displays the details of a specific packet.

"4 The details are divided into fields corresponding to TCP/IP layers, such as the Frame (Physical),
4 Ethernet (Data Link), and IP (Network).

Packet Bytes
FTieiaa The bottom part of the view corresponds to the actual bytes of the selected packet, in
hexadecimal format and ASCII encoding.
=
48


### Slides — strona 105

Introduction to Wireshark
ICMP Traffi
— Wireshark
MicuP Sample a
File Edit View Go Capture Analyze Statistics Telephony Wireless Tools Help
The Ping command includes a auc@it LeeSP seb aaak
Expression... +
request and a reply.
No. Time Source Destination Protocol Length Info “2
1 0.000000 172.42.0.157 172.42.0.140 ICMP 98 Echo (ping) request id=@x@cda, seq=1/256, tt1=64
Each ICMP packet is numbered 2 0.300934 172.42.0.140 172.42.0.157 ICMP 98 Echo (ping) reply id=0x@cda, seq=1/256, ttl=64
‘ ape " 3 1.000925 172.42.0.157 172.42.0.140 ICMP 98 Echo (ping) request id=@x@cda, seq=2/512, ttl=64
and can be identified to find a 4 1.298136 172.42.0.140 172.42.0.157 ICMP. 98 Echo (ping) reply id=@x@cda, seq=2/512, ttl=64 ¥
corresponding response. s >
Frame 1: 98 bytes on wire (784 bits), 98 bytes captured (784 bits) a
Ethernet II, Src: Vmware_c6:21:44 (@0:@c:29:c6:21:44), Dst: SamsungE_83:45:3b (@4:d6:aa:83:45:3b)
ICMP has only four fields since Internet Protocol Version 4, Src: 172.42.0.157, Dst: 172.42.0.140
. + Internet Control Message Protocol
it is a Layer 3 protocol. Type: 8 (Echo (ping) request)
Code: @
~ Checksum: @x7d9@ [correct]
In Windows each ICMP echo [Checksum Status: Good]
(ping) packet includes all the Identifier (BE): 3290 (@x@cda)
4 Identifier (LE): 5582@ (@xdaec)
basic symbols and numbers on Sequence number (BE): 1 (@x@001)
the keyboard. Sequence number (LE): 256 (@x0100) tp
9000 4 dé aa 83 45 3b @@ Gc 29 c6 21 44 O8 G8 45 00 Oe ): 1D -E “
0010 @@ 54 8c 1a 40 @@ 40 @1 55 11 ac 2a @@ 9d ac 2a T+ -@:@ Us -*. +e #
0828 @@ 8c @8 @@ 7d 98 Gc da CO O1 e9 53 bb Sc BO BO ves} +Se\ee
0030 00 00 04 11 06 00 00 00 000010111213 1415 ------- :
0040 1617 18 19 1a 1b 4c 1d Je 1f 20 21 22 23.24.25 0 -------- ++ MRSS
| 0050 26 27 28 29 2a 2b 2c 2d 2e 2F 30 31 32 33.34.35 &'()*+,- ./012345 ¥
Q@ * icmp sample.cap || Packets: 8 - Displayed: 8 (100.0%) || Profile: Default
EA
—_
=a


### Slides — strona 106

Introduction to Wireshark
DNS Traffic
— Wireshark
a
Aac@i PRO errseFsstlbaaagr
Expression... +
DNS traffic includes multiple ns hae rn naa Pretest Lage Does
requests and replies. es 1 0.000000 172.42.0.151 172.42.0.138 DNS 74 Standard query @xd282 AAAA api.segment.io
ols 2 0.010187 172.42.0.138 172.42.0.151 ONS 158 Standard query response @xd282 AAAA api.segment.io SOA
3 5.906976 172.42.0.157 172.42.0.138 ONS 71 Standard query @xb970 A
4 5.994438 172.42.0.138 172.42.0.157 ONS 87 Standard query response @xb97@ A -com A 107.180.
Most of a search tree will not 5 5.995163 172.42.0.157 172.42.0.138 ONS 71 Standard query @x6276 AAAA
. 6 6.121930 172.42.0.138 172.42.0,157 ONS 142 Standard query response 0x0276 AAAA -com SOA nst
appear in a packet. Only the : >
request and response. Frame 1: 74 bytes on wire (592 bits), 74 bytes captured (592 bits) “
Ethernet II, Src: LcfcHefe_7a:4b:17 (€8:6a:64:7a:4b:17), Dst: D-LinkIn_d7:48:d0 (78:32: 1b:47:48:40)
Internet Protocol Version 4, Src: 172.42.0.151, Ost: 172.42.0.138
DNS may try to automatically User Datagram Protocol, Src Port: 62297, Ost Port: 53
~ Domain Name System (query)
resolve both A and AAAA Transaction 10: @n#202
records corresponding to the Flags: @x@1@@ Standard query
Questions: 1
IPv4 and IPv6 addresses pneuan Waa
respectively. Authority RRs: @
Additional RRs: @ .
0000 78 32 1b d7 48 do e8 Ga 64 7a 4b 17 08 00 45 00 = x2--H.-j dzK.--E
O@10 8 3c 6F bb G8 06 82 11 71 88 ac 2a 00 97 ac 2a <o | haba
2020 00 Ba £3 59 G2 35 G8 28 bi 10 d2 82 @1 00 02 O1 Ve5e( oesoee
0020 08 00 00 8 G2 G2 O3 61 70 69 07 73 65 67 6d 6S a pi-segne
0080 Ge 74 02 69 GF 00 G2 1c 00 1 nt-io
@ 7 oNssample.cap | Packets: 6 ° Displayed: 6 (100.0%) | Profile: Default
=


### Slides — strona 107

Introduction to Wireshark
— Wireshark
AMLHTTP Sample.cap - x
File Edit View Go Capture Analyze Statistics Telephony Wireless Tools Help
4udc@i <eeSsF¥esaaawn
expression... ++
. No. Time ‘Source Destination Protocol Length Info
HTTP is an unsecure protocol i 16 14.384881 172.42.0.157 192.195.77.80 HTTP. 779 POST /login-form/ HTTP/1.1 (application/x-www-form-url
used to transfer information ‘ 22 14.571270 192.195.77.80 172.42.0.157 HTTP 357 HTTP/1.1 200 OK (text/html) i
over the web. Frame 16: 779 bytes on wire (6232 bits), 779 bytes captured (6232 bits)
Ethernet II, Src: Vmware_c6:21:44 (@0:0c:29:c6:21:44), Dst: D-LinkIn_d7:48:d0 (78:32:1b:d7:48:d@)
: . Internet Protocol Version 4, Src: 172.42.0.157, Dst: 192.195.77.80
Since HTTP traffic is not Transmission Control Protocol, Src Port: 60834, Dst Port: 80, Seq: 1, Ack: 1, Len: 713
encrypted, it can be sniffed Hypertext Transfer Protocol
» HTML Form URL Encoded: application/x-www-form-urlencoded
on the network. Form item: “username” = “lionk”
Form item: "password" = "Aal23456"
Form item: "submit" = "Login"
0000 78 32 1b d7 48 de @@ ec 29 c6 21 44 EERE 45 0 = x2--H--- )- !DBBE ay
2010 02 fd bf 2F 40 @2 40 e6 bd FO ac 2a 2B Sd cOC3_—--/@-@ ---*--
0020 4d 50 ed a2 08 50 dd 31 94 33 cb c3 de c6 8018 MP---P-1 -3.----
9030 @@ e5 bd ca 60 68 O1 G1 8 Ga c7 af bO 43 dO 21 a Oo
9040 Sf ed 5@ 4f 53 54 20 2F 6c 6F 67 69 be 2d 66 GF _-POST / login-fo
9050 72 6d 2f 20 48 54 54 5@ 2f 31 2e 31 Od Oa 48 6F rm/ HTTP /1.1--Ho
0060 73 74 3a 207777 77 2e 64 65 6d GF 2e 61 6d 69 st: www. demo.ami
0070 74 6a 61 6b 68 75 2e 63 6F 6d Gd Ga 55 73 65 72 tjakhu.c om: -User
0080 2d 41 67 65 be 74 3a 20 4d OF 7a 69 6c 6c 61 2F -Agent: Mozilla/
2090 35 2e 30 20 28 58 31 31 3b 20 4c 69 Ge 75 78 20 5.0 (X11 ; Linux
0020 78 38 36 Sf 36 34 3b 20 72 76 3a 36 30 2e 30 29 x86_64; rv:60.@) Ri
O ¥ HTTP sample.cap || Packets: 31 - Displayed: 2 (6.5%) || Profile: Default
im
—
ES


### Slides — strona 108

Filtering Traffi
— Wireshark
(MUTI Sample.cap = x“
File Edit View Go Capture Analyze Statistics Telephony Wireless Tools Help
A .pcap file can contain ZUd@ i FROCeef#F G52 aAQqQ8
thousands of packets, even Expression... +
(
after a few seconds of logging. No. Time Source Destination Protocol Length Info i
1 0.000000 172.42.0.157 81.218.31.137 TCP 66 38908 > 80 [ACK] Seq=1 Ack=1 Win=329 Len=0 a
; ae 3 3.426254 172.42.0.151 Ba 114 130 93 Trp 60 16852 + 8@ [ACK] Seq=1 Ack=1 Win=1023 Len=1
[to view the packets efficiently, | 4 3.488723 85.114.134.23 1 Mark/Unmark Packet 66 8@ + 16852 [ACK] Seq=1 Ack=2 Win=26@ Len=@ SLE=1
filters can be applied. Ignore/Unignore Packet
Set/Unset Time Reference
Time Shift...
i i Packet Comment...
Filters can also be applied 9 14.146553 172.42.0.157 1 74 60446 > 80 [SYN] Seq=@ Win=29200 Len=0 MSS=1460 S
during capture to prevent 10 14. 206035 172.42.0.157 1 Edit Resolved Name 74 60834 + 80 [SYN] Seq=@ Win=29200 Len=0 MSS=1460 S
the capture of unwanted 11 14.206138 172.42.0.157 1 Seq=0 Win=29200 Len=@ MSS=1460 S
12 14.218727 172.217.22.10 1 " . ACK] Seq=@ Ack=1 Win=60192 Len-o]il
packets. ‘ BNP PA SEEIES - Prepare a Filter » Not Selected ee y
- = Conversation Filter » ..and Selected
frame 3: 68 bytes on wire (4G bits )s GO Be. soa Conversation > or Selected
Ethernet II, Src: LefcHefe_7a:4b:17 (e8:6a =, , ‘and not Selected f 48:48)
Filters are logical conditions Internet Protocol Version 4, Sre: 172.42.0, ; fae ee
senne . collow ..0F not Selecter
that are applied using &&, | |, Transmission Control Protocol, Src Port: 1¢
stay dls 9000 78 32 1b d7 48 d@ e8 6a 64 7a 4b 17 08 Copy a
==, and '= 9010 00 29 ae Gc 40 00 80 06 C417 ac 2a "
0020 86 17 41 d4 e850 96 16 c9 If 18 5b fF rotocol Preferences
Brackets can also be used. 0030 @3 FF 6a 9e G8 28 28 20 20 20 20 20 Decode As...
| Show Packet in New Window
OQ F HTTP sample.cap || Packets: 31 - Displayed: 31 (100.0%) | Profile: Default
_
=,


### Slides — strona 109

Introduction to Wireshark
Wireshark includes many display filters. The following table lists some useful ones.
Logical Port Groups
Filter Data
Protocol Name Find a match for packets using a specific protocol (i.e. icmp, arp, http, dns).
ip.addr == 10.0.0.3 Find a match for this address on the source and destination.
ip.dst != 10.0.0.2 Find all matches that are not this destination.
ip.src != 10.0.0.3 Find all matches that are not this source.
tcp.port == 25 && tcp.port == 80 Find packets that match both specified port numbers in TCP.
udp.port == 53 || udp.port == 69 Find packets that match one of the specified port numbers in UDP.
udp.dstport == 25 Find packets that match a specific port number on the destination in UDP.
53


### Slides — strona 110

Introduction to Wireshark
— Wireshark
(A esas Foton HTTP Seam Gcptreame9 3): HTT Samplecap - 6 x
POST feo WTF zi
ee cr eae
Usa Agea: Mona's ct, Ux 866; 60.0) Geke/0400101 Feefo60.0
Reap ter appctenttamlapecanvenar0.7ge08
feepeianquage erena-03
After capturing traffic and few hin nroaiicononnod
— . : Fae eee yarn
filtering, stream inspection Sie rt nensnencnseerem serene ore ERENT
een ae
can be done. [eens teen
sma onkpasord-Aa2458RsubtLognkTP/Lt 200 0K
Emr type: te
"nd rg: ured
: ee
Streams are collections of op Ave: tnesutets
Dae an 20 fpr 2019 18:05:05 GT
Ess
packets from the same tose a, 18 Aug 205 201757 GT
os ro sites
conversation. ———
“100CTYPE unl PUBLIC"/WC/DTD YT 1.0 Tanston/E" "pf rR /OTD-rnstiona >
ah
. ‘ocinromn
Left-click a packet to choose Pcie,
the option to follow a stream, rr
. 1S Berne
which can be TCP, UDP, or HTTP. aoa
eesrnesneets-+
Sink efcevsyecas reo "eeshee peels >
<escurts->
Soke eee: 'src="httpi//ajax.qoogleapis.com/ajaxilibs/jquery/1.2.6/;query.min.js"> </script>
Unless traffic is encrypted, it “crip type—"terncrpt>
linear crest oe
should be readable. Fn er coe a AB ul
(ce gl Som nae te lS
ee [12]
[Reroute sum) [rae | [sown || mock || Gwe || hey
=


### Slides — strona 111




### Slides — strona 112

The Cisco IOS
ee ae. The objective of this lab is to learn how to use Wireshark
Network Examination with Wireshark and how computers encapsulate and send data.
30-60 Min.
i ; ® Become familiar with Wireshark.
— = @ Examine live Network.
$s S, 4 ¥ ® Capture and analyze.
i b NN ® e di
| ‘ » @ r ® Windows 7/8/10 @ Lab document
=~ 8 « ® Wireshark Installation file
e . | ® Web Browser
{ ; 4 . . is


### Slides — strona 113

Network Fundamentals
ARP


### Slides — strona 114

ARP and Encapsulation
Address Resolution Protocol
If a device wants to communicate with another device on the same
LAN, it must encapsulate the MAC address of the destination device.
To get the MAC address, it uses a protocol called ARP, that resolves a
logical address (IP) to a physical address (MAC), and saves the results
in the host ARP cache.
ARP operates in Layers 2 and 3 of the OSI model.
Every Layer 3 device uses ARP.
B
Switches make forwarding decisions based on the physical address of the frame.
58


### Slides — strona 115

—_ ARP Process
Scenario: Host A wants to communicate with minke
host B. Host A knows host B’s IP address but
not its MAC address.
lh, Ed
Step 1 - Host A sends an ARP Request to all hosts on £ 2 %,
the network (Broadcast), with Host B’s IP as the Sy = Ne XN,
destination MAC, requesting its MAC address. & XY 2 MX a NP %,
vy 5
tm
Step 2 - The switch forwards the ARP request
— LA | LB |
Step 3 - Host B recognizes the IP address in the LJ La L=
request, so it performs an ARP reply, in which it lists ESE Eee aon ee
its own MAC address. ARP Table:
Host IP MAC
Step 4 - Host A receives the ARP reply and saves |e | 1000.2 | aes |
host B’s MAC address in the ARP cache, together
with Host B’s corresponding IP address.
So


### Slides — strona 116

arp -a
The ARP table or cache is stored in C:\Windows\system32>arp -a
the RAM of the device.
The ARP contains three parameters: Interface: 10.71.0.110 --- @x17
* Destination host IP Internet Address Physical Address Type
* Corresponding MAC of that host 10.71.0.100 90@-7c-ac-a9-a2-c9 dynamic
. etialbrer wane 10.71.0.104 64-cc-24-96-8b-e0 dynamic
10.71.0.255 F¥-fFF-FF-FF-FF-FF static
224.0.0.22 Q@1-00-5e-00-00-16 static
arp —a and arp -g display the 224.0.0.251 Q@1-00-5e-00-00-fb static
host ARP table. 224.0.0.252 @1-@0-5e-00-20-fc static
SHOW amp dsplayea Chea deus 239.255.255.250 01-00-5e-7f-ff-fa static
ARP table. 255.255.255.255 F¥-FF-FF-FF-FF-FF static


### Slides — strona 117

C:\Windows\system32>arp -d
arp —d deletes the host ARP
table. 4
ame C:\Windows\system32>arp -s 10.@.0.2 Q@-aa-bb-11-22-33
arp —s adds a static entry to
the ARP table that resolves to
a specific IP address.
Note: Static ARP helps reduce
the risk of ARP spoofing
attacks.
arp inet_addr — defines a
specific IP address.
arp eth_addr - defines a
specific MAC address.


### Slides — strona 118

ARP and Encapsulation
Headers and Trailers are Adding Headers and Trailers Protocol Data Unit is a piece
control data added by to data is called of information added to or
protocols to the beginning encapsulation. Processing removed from a layer of the
and end of each data unit, in them and removing them is OSI model.
each layer. called decapsulation. PDU consists of protocol-
For example, IP packages Depending on the specific control information
the logical source and communication type, and user data.
destination address in an protocols in each layer add Examples are segments,
IPv4 header, and adds it to the correct header to the packets, and frames.
the data unit in the Network data unit. ,
Layer.

62


### Slides — strona 119

/ 4% ; a Vy Zs oe ?
7 4 : = / “oo : hie i
~ 4 Paty iy
a % , af . f
La =, > Pt @ 4
Y Ss oN N a SS
q ewan we & \ 3 a,
(Qed Bs by
NOABORE ie
' oe She ~ ey he ae
Se A = =
=== ar ag See _ + ae
| isl he a f
/; >
WW | :
uN . ron y ae a


### Slides — strona 120

a i ™" : = a aw NETWORK ee Bal Ci = L D


# Chapter 3: Switch & IOS Fundamentals


### Slides — strona 121

‘Cybersecurity Professional Program
. : e ;' 2 7 om C
Switch & IOS
Fundamentals
Computer Networking


### Slides — strona 122

Computer Networking
Introduction Network Switch & IOS Switch Securit IP and Routing
to Networks Fundamentals Fundamentals y Concepts
Diagnostics and VLANs Dynamic IPv4 & IPv6é Subnetting
Troubleshooting and Trunk Routing Static Routing Concepts
Access Infrastructure Fiival Proiect
Control List Services d


### Slides — strona 123

Switch & IOS Fundamentals
Overview
Lesson Objective
Switch Fundamentals
The objective of this lesson is to learn more
about the network switch and how it The Cisco 10S
operates.
It also covers Cisco's operating system and = ; ; ;
: ‘ : 3 Initial Device Configuration
configuration settings for Cisco and other
platform devices.
Managing IOS & System Files
G


### Slides — strona 124

OO
Switch & IOS Fundamentals
SWITCH FUNDAMENTALS


### Slides — strona 125

Switch Fundamentals
The Switch
Overview
Switches are smart Layer 2 devices with many ports designed to
forward frames from source to destination, according to specific MAC
a a addresses in the frame (Data-Link Layer).
Ee They include multiple technologies providing various capabilities.
Switches were developed to forward frames in accordance with their
destination addresses and MAC tables using a MAC learning process
known as forwarding decision.
B


### Slides — strona 126

The command used to display Switch#show mac address-table
the MAC address table is Mac Address Table
show mac address-table ee ee
MAC address tables include the Vlan Mac Address Type Ports
following columns: Sees Seesoeto eee ee ere ae SS eoe
¢ VLAN
, MAC adress 1 @0@1.97d7.45c3 DYNAMIC FaQ/5
ynamic or sane 1 @00@4.9a3d.bbc6 DYNAMIC Fae/4
¢ Associated physical ports
dl 000c.8500.13bb DYNAMIC Fa@/3
al 00de.978c.5698 DYNAMIC Fa@/2
DYNAMIC refers to a frame with a
source MAC that arrives at a switch
and updates the table with the MAC
address for that port.
STATIC indicates a manually configured
MAC address on a switch.


### Slides — strona 127

Switch Fundamentals
Switching Methods
Switching Methods
Switches have different methods of receiving and
transmitting frames on the LAN.
The following switching methods are used:
° Store-and-forward
& * Cut-through
. Fragment-free
é


### Slides — strona 128

Store-and-Forward Switching
Store-and-Forward Switching

. A switch using the store-and-forward method buffers the
entire frame upon receipt. This enables the switch to support
various port speeds. For example, a frame received on a 100

« Mbps ingress port can be transmitted via a 1 Gbps egress
port.

° Another advantage of this method is error checking, which

— can be done once the entire frame is buffered. The switch
— can easily detect frame errors using the FCS field.

° Although store-and-forward is relatively slow, it does provide
error checking and support for different speeds across
multiple ports. _

&


### Slides — strona 129

Cut-through Switching
Cut-through Switching
° Cut-through switching is a much faster method than store-
and-forward. In this method, only the first 6 bytes of the
mae incoming frame are buffered, meaning the switch only regards
A ‘ Dr the destination MAC address of the frame.
f \ ¢« — The switch forwards the frame immediately, even before the
{ | entire frame is received, and no error checking is done.
X A * Note: Modern switches can buffer up to 14 bytes of the
ll beginning of a frame, before deciding what to do with it.
° Although the advantage of cut-through switching is its speed,
a significant disadvantage is that most frames that reach the
destination host are corrupted due to lack of error checking.
6


### Slides — strona 130

Fragment-Free Switching

Fragment-Free Switching

° Fragment-free switching is a more advanced method.

¢ — This method buffers the first 64 bytes of the frame, including MAC address data and
the frame’s payload. The technique provides faster switching than the store-and-
forward method while also performing partial error checking to make sure there is no
fragmentation on the first 64 bytes of the frame.

. Fragment-free switching is therefore a better choice, as it is faster than store-and-
forward switching and provides partial error checking, unlike the cut-through method.

B


### Slides — strona 131

Switch Fundamentals
Half-Duplex Communication
| A connection for which the communication is restricted
to exchanging data in one direction at a time. For f| : fl ‘
= example, a walkie-talkie is a half-duplex device because =I ———————> =
only one person at a time can talk.
@ 3338 SS $388
Full-Duplex = =
Full-duplex means that data can be transmitted in both z > ra
directions, on a signal carrier, at the same time.
For example, a telephone is a full-duplex device - ~
because both users can talk at once. aon
@ ©)


### Slides — strona 132

Port Speed
Switch Ports
=> , Switch ports can transfer traffic at speeds of 10 Mbps, 100
2 ida Mbps, or 1000 Mbps.
: x aN The default is for the switch port to auto-configure its speed
X based on signaling between the port and the connected device.


### Slides — strona 133

Switch Fundamentals
Auto-Negotiation
Auto-Negotiation
via _ ;
Auto-negotiation tells connected devices to announce their
capabilities, and then, based on the settings of the interconnected
device at the other end, chooses the optimal speed and duplex
mode.
If one of the devices is configured with a different mode, a duplex mismatch will occur.


### Slides — strona 134

OO
Switch & IOS Fundamentals
THE CISCO IOS


### Slides — strona 135

Overview
Every network device, such as a switch or router, has an operating system
that tells it how to forward packets and execute network operations.
An operating system for a device is known as a Network Operating System
) (NOS).
An NOS does not operate in the same way as PC and server operating
systems.
An Internetwork Operating System (IOS) is a CLI-based system, and users
interface with it using text-based Cisco commands.
&


### Slides — strona 136

The Cisco IOS
The Cisco IOS
Overview
Most Cisco devices, regardless of their size or type, run the IOS,
ors which is an advantage due its singularity and familiarity.
—————— While all devices come with a default IOS and feature set, it is
_—-— possible to upgrade the IOS version or feature set to obtain
a additional capabilities.
This course focuses on versions 12 and 15.
6
The versions of the IOS may be different, depending on the device hardware.


### Slides — strona 137

The Cisco 10S
The Cisco IOS
10S or iOS
IOS VS. iOS
otfnotfte ¢
Cisco.
Internetwork Operating System


### Slides — strona 138

The Cisco IOS
IOS Interface Features
Command Line
IOS uses a command line interface (CLI) to enable administrators and technicians to
interact with the system via special Cisco commands.
CLI
K)>) \ CLI is a means of interacting with programs by entering commands on a command
= line. Using a CLI-based system has many advantages, such as minimum resource
usage, faster ability to operate on the system, and others.
Terminal Emulation
f[s——) Many network devices are configured and managed using Terminal Emulation (TE)
software, such as PuTTY. TE programs enable configuration of local devices using a
=== serial cable or a remote management protocol, such as SSH.


### Slides — strona 139

The Cisco IOS
Terminal Software
PuTTY PuTTY
Pul TY is a versatile tool for remote access to another —
mn computer. It is often used by people who want secure [ie eal
remote shell access to a UNIX or Linux system, though that | tae ee e—]
is only one of its many uses. vy ‘a San Sena aso @sst Osou!
he Te Term is an open-source, free, software-based = i Sere
terminal emulator (communication) program. It ee
[7] emulates different types of computer terminals, from oo ee
£———)_:~SsCDEEC VT100 to DEC VT382, and supports Telnet, SSH 1 — =
and 2, and serial port connections. a |
SecureCRT tO
SecureCRT is a commercial SSH and Telnet client and
5 terminal emulator by VanDyke Software. Originally a
Windows product, VanDyke recently added Mac OS X
and Linux versions. vy


### Slides — strona 140

Cisco Packet Tracer
Overview
Cisco Packet Tracer allows the user to map a network.
Packet Tracer enables the testing of network configurations,
trains users to work with network configuration, helps them
understand how a network operates, and provides them with
network deployment experience.
2)


### Slides — strona 141

The Cisco IOS
ce eee ft Create a Cisco account and download Packet Tracer to
Packet Tracer Installation explore the features it provides.
30-60 Min.
r @ Register the account.
- 7 ® Download Packet Tracer.
. ia 4 —_ @ Install Packet Tracer.
; ® Web Browser ® Lab document
®
,.
a .
~ iY ol


### Slides — strona 142

The Cisco IOS
Gut-of Band Console Cable

This method uses a dedicated management console

cable that must be physically connected to the device.

Initial configuration is usually done using this method. <3

In-Band ee y
This method uses management protocols, such as SSH Ne)
or Telnet, which access the device remotely over the . E |
network. —
@ </>


### Slides — strona 143

The Cisco IOS
How Local Configuration Works
© Out-of-Band management requires two main items:
ie e PC with terminal software
* Console cable
Terminal
A network device is like a PC, but without a mouse,
— keyboard, and screen. A PC with a terminal provides a
= way to input commands and view output from the
device. eo
Console Cable
A console cable or management cable is like a bridge
between the PC and the device. Almost every device has
a designated console cable for this purpose. Older cables
use an RS-232 connector; modern ones use USB. y,


### Slides — strona 144

The Cisco IOS
IOS Modes
Permissions
__ IOS can operate in one of three work modes, each with different capabilities and
— permissions. For example, one mode may have a lower level of privileges compared
= with another mode.
Modes
The division of modes is meant to separate the management levels and increase the
efficiency of network device security and configuration.
Structure
Cisco IOS modes have a hierarchical structure and are similar among switches
and routers.


### Slides — strona 145

The Cisco IOS
IOS Modes
User EXEC Mode
> This mode has low-level capabilities but is useful for basic operations. It has a limited
number of monitoring commands and does not allow device configuration changes.
Privileged EXEC Mod
This mode has a large number of monitoring commands and device configuration
# viewing commands (show commands). It also enables file management operations,

such as device configuration backups and IOS upgrades.


### Slides — strona 146

The Cisco IOS
IOS Modes
Global Configuration Mode
‘ Global configuration is the only mode that allows administrators to change device
(config) # configuration. This mode is only accessible from the privileged EXEC mode.
Interface Configuration Mode
The interface mode allows you to change specific parameters within a switch or
router.


### Slides — strona 147

Q
Navigating the system and Switch>enable
understanding the difference Switch#configure terminal
between the modes is very Enter configuration commands, one per line. End with CNTL/Z.
important when working in the
system. . . .
Switch(config)#exit
The default display name of a device Switch#exit
appears before the prompt. In the Switch>
example at right, the name is Switch.
The enable command moves the user
from user mode to privileged mode.
The configure terminal command moves
the user from user mode to global
configuration mode.
The exit command takes the user
one mode back.


### Slides — strona 148

Example
Incomplete Command i
Switch>di
% Ambiguous command: "di"
The command is correct but not complete.
(38) Switch#show
WV %Incomplete Command.
Ambiguous Command Switch(config)#hostname S1
Not enough characters were entered for the command ; . ‘ vat
x to be recognized. Or, more than one command exists % Invalid input detected at
. marker.
with the same name.
A
Invalid Input
The command was entered incorrectly (i.e., typo) or
inserted in the wrong mode.


### Slides — strona 149

The Cisco IOS
Hotkeys and Shortcuts
. | | Break sequence used to abort DNS
TAB Completes partial entry. lookups, traceroutes, pings, etc. alleles
CTRL+D__ Erases the character at the cursor. | | Erases the word to the left of the CTRL+W
cursor.
CTRLEK Erases all characters from the cursor Recalls a command from the history eee 8
to the end of the command line. buffer. id
Erases all characters from the cursor Ends configuration mode and returns
FSC +P to the end of the word. to privileged EXEC mode. lal


### Slides — strona 150

The Cisco IOS
Cisco Device Components
eS
oh tl
Volatile memory that Non-volatile memory Non-volatile memory Non-volatile memory
stores the system responsible for the that stores the operating that stores the startup
configuration (running- Power-On Self-Test system itself (IOS). config file.
config) and tables (such (POST) process and
as the MAC table). bootstrap, which is the
initial program
responsible for booting
the IOS.


### Slides — strona 151

The Cisco IOS
POST
POST and bootstrap program load: This part of the
sequence checks the CPU, RAM, and NVRAM. When iin,"
; ? Load IIOS
done, the device copies the bootstrap program from ;
the ROM to the RAM. Load IOS: After copying the bootstrap program
from the ROM to the RAM, the IOS (which is still
stored in flash memory) is copied to the RAM for
execution.
Load Configuration
Load configuration: The bootstrap program now
copies the startup configuration file from the
NVRAM to the RAM.


### Slides — strona 152

OO
Switch & IOS Fundamentals
INITIAL DEVICE CONFIGURATION


### Slides — strona 153

hostname <device name>
Switch(config)#hostname S1-Floor1
S1-Floor1(config)#


### Slides — strona 154

username <user-name> password <password>
Switch(config)#username Admin password p@nd@
Switch(config)#username Peter password Spiderm@n


### Slides — strona 155

enable password <password>
Switch(config)#enable password c!sc@


### Slides — strona 156

banner motd #security-message#

Switch(config)#banner motd #Access to this device is for authorized personnel only!#
Press RETURN to get started!

Access to this device is for authorized personnel only

User Access Verification

Password:


### Slides — strona 157

service password-encryption
Switch(config)#service password-encryption


### Slides — strona 158

copy running-config startup-config
Switch#copy running-config startup-config


### Slides — strona 159

line console 0 & login local
Two steps are performed to enable Switch(config)#line console @
local credential (username and Switch(config-line)#login local
password) authentication on the Switch(config-line)#exit
console port.
1. Enter the console port config
mode (line mode).
2. Enter the local login and exit.
Note: Besides the local login
command, there is a login
command that enables only
password checking.


### Slides — strona 160

S$1-Floorl#show running-config
Building configuration...
All configuration changes are Current configuration : 1234 bytes
immediately saved in the !
running-config file. version 12.2
service password-encryption
!
To display them, run the show hostname! Si-Flooril
running-config or show run !
command. enable password 7 @822@D5D0A49
!
Note: The example on the right username Admin privilege 1 password 7 08316C400D39
is a brief glimpse of the actual !
file. banner motd #Access to this device is for authorized personnel only!#
!
line con @
line aux @
Line vty @ 4
login


### Slides — strona 161

Initial Device Configuration
eee Learn how to set basic configurations on a switch using
Initial Cisco Cisco lIOS commands.
Device Configuratio ‘
30-60 Min. ( . aap |
} ®@ Access the device.
2 ' ® Navigate the IOS.
ee, ~ " ~ ® Configure initial and security settings.
(Ci ee if 0, @ Alternate PKA opening
| a» " ® Cisco Packet Tracer 7.2.2 @ Lab document
: a 4 ® or later @ NET-03-L2.pka
4 ‘ :
| r ’ |
| a x —
‘ ia —


### Slides — strona 162

OO
Switch & IOS Fundamentals
MANAGE IOS & SYSTEM FILES


### Slides — strona 163

TFTP
Trivial File Transfer Protocol (TFTP) is a simple file transfer
protocol that allows clients to retrieve files from a remote host or
—_ transfer files to a remote host.
TFTP can also be used to remotely start a computer, back up network
or router configuration files, and upgrade a device’s IOS.
o)
TFTP relies on UDP to transport data and uses port number 69.


### Slides — strona 164

copy running-config tftp
Switch#copy running-config tftp:


### Slides — strona 165

NGreTEl a a : Ril#copy running-config tftp:
| ote: First save t S Senneuration Address or name of remote host []? 192.168.1.3
ocally using: copy running-config . . . .
startup-config Destination filename [R1-confg]? R1-config-backup2e.9
; Writing running-config....!!
Step 1: Copy the file to the server. [OK - 1362 bytes]
Step 2: Enter the TFTP server IP
address.
Step 3: Select the name of the file
saved on the server.
Backing up the IOS file is almost
the same. You only need to
replace the source location of the
file, meaning flash: instead of
running-config


### Slides — strona 166

Step 1: The command copy tftp: Ri#copy tftp: flash:
flashzis.used to copy the new IOS Address or name of remote host []? 192.168.1.3
file from a TETP server to the flash Source filename []? c1901-imoversa;19.mz.SPA.152-4.M3.bin
memory. Destination filename [c1901-imoversa;19.mz.SPA.152-4.M3.bin]?
Step 2: Upgrading the device can Accessing tftp://192.168.1.3/ c1901-imoversa;19.mz.SPA.152-4.M3.bin...
be performed after copying the Loading c1901-imoversa;19.mz.SPA.152-4.M3.bin from 192.168.1.3:
new IOS to the device using the PEEPPEP EP PPP ere r rrr errr epee errr errr pepe rrr reer rrr ere rrr erry
boot system command. This [OK - 4670455 bytes]
command tells the device which
10S file to load on the next R1# Configuration terminal
startup. R1(config)#boot system flash@://c1901-imoversa;19.mz.SPA.152-4.M3.bin
R1(config)# exit
Step 3: The command copy Ri#copy running-config startup-config
running-config startup-config is R1i#reload
used to save the current
configuration to the startup
configuration and reload the
device for the new IOS to load.


### Slides — strona 167

ROMmon
What Does ROMmon Do?
_ The purpose of the Read-Only Memory MONitor (ROMmon)

| configuration register is to change the router’s behavior in several ways:
(le :[B]:] = Determine how the router will boot.
a —" ¢ Apply options while booting (such as ignore configuration).
a ——"

e Set the console speed and band rate for terminal emulation sessions.

&


### Slides — strona 168

Router(config)# config-register 0x2102
Router(config)# end
In the configuration terminal Router# copy running-config startup-config
mode, we can change the register Destination filename [startup-config]?
value, which will affect the next Building configuration
boot process. [OK]
Router# Reload
In the example on the right,
we change the register
value to the default 0x2102,
and save the configuration
in startup config, which will
set default factory settings.


### Slides — strona 169

Manage IOS & System Files
The default configuration register is Ox2102. We can verify this using the command.
Using the command , we can change the register value and the router’s behavior.
Common Settings
Register Value Device Behavior

0x102 * Ignores break key
* 9600 console baud rate (maximum transfer rate of the console port in bits per second; in this case, 9600)

0x1202 * 1200 baud rate
* Boots into bootstrap
* Ignores break key

Ox2101 * Boots into ROM if initial boot fails
* 9600 console baud rate
* Default register value

0x2102 * Boots into ROM if initial boot fails
* 9600 console baud rate default value for most platforms


### Slides — strona 170

Router#show version
<output omitted>
Cisco IOS Software, 1841 Software (C1841-IPBASEK9-M), Version 12.4(12), RELEASE SOFTWARE
(Giteil))
By entering the command show Technical Support: http://www. cisco.com/techsupport
. . Copyright (c) 1986-2006 by Cisco Systems, Inc.
version we can verify the Compiled Mon 15-May-@6 14:54 by pt_team
configured register value.
ROM: System Bootstrap, Version 12.3(8r)T8, RELEASE SOFTWARE (fc1)
System returned to ROM by power-on
We can also display additional System image file is "flash:c1841-ipbasek9-mz.124-12.bin"
information, such as the
software type and version. Cisco 1841 (revision 5.0) with 114688K/16384K bytes of memory.
Processor board ID FTX@947Z18E
M86@ processor: part number @, mask 49
2 FastEthernet/IEEE 802.3 interface(s)
191K bytes of NVRAM.
63488K bytes of ATA CompactFlash (Read/Write)
Configuration register is @x2102


### Slides — strona 171

ManageJOS & System Files
—— Use a TFTP server to back up and roll out switch
Backing up Config Files configurations.
and Managing the IOS ‘
30-60 Min. ( . ee uration f
; @ Back up configuration files.
' @ Back up and upgrade the device ISO.
re 4 é yl.” ~~
; rd ae ~ N e yr
| M Md ® . ® Cisco Packet Tracer 7.2.2 ® Lab document
: aw 4 & or higher @ NET-03-L3.pka
‘ ; :
| r ’ |
‘ ia —


### Slides — strona 172

/ 4% ; a Vy Zs oe ?
7 4 : = / “oo : hie i
~ 4 Paty iy
a % , af . f
La =, > Pt @ 4
Y Ss oN N a SS
q ewan we & \ 3 a,
(Qed Bs by
NOABORE ie
' oe She ~ ey he ae
Se A = =
=== ar ag See _ + ae
| isl he a f
/; >
WW | :
uN . ron y ae a


### Slides — strona 173

a i ™" : = a aw NETWORK ee Bal Ci = L D


# Chapter 4: Switch Security


### Slides — strona 174

osal l
; 2 _ —I iy
aa ; 7 — Le 3 ieee
_ i — a ont. NETWORK ei Bee _ ¢ ; a)
af K 4
a: SWITCH SECURITY
Computer Networking


### Slides — strona 175

Computer Networking

Introduction Network Switch & IOS Griavdnaanrit IP and Routing

to Networks Fundamentals Fundamentals y Concepts
Diagnostics and VLANs Dynamic IPv4 & IPv6é Subnetting
Troubleshooting and Trunk Routing Static Routing Concepts

Access Infrastructure Fiival Proiect
Control List Services d
2


### Slides — strona 176

Switch Security
Overview
Lesson Objective
The objective of this lesson is to learn new
ways to secure a switch from unwanted access. Port Security
The lesson explains how the Port Security
feature helps prevent access by unauthorized
MAC addresses, and how to establish secure Remote Access
connections over the network.
G
3


### Slides — strona 177

CO
Switch Security
PORT SECURITY


### Slides — strona 178

Port Security
Risks in a Switched Environment
MAC Spoofing
MAC spoofing is when attackers change their own physical PC address to conceal their
_ true identity and pose as someone else. For example, an attacker may spoof a MAC
address with a legitimate MAC address, to bypass an access control mechanism, such as
port security.
CAM Table Overflow
® | CAM Table Overflow is an attack that targets a switch’s MAC table. The idea is to flood
= — the table with a large number of fake addresses. When the list of addresses exceeds the
maximum size of the table, the switch will initiate its fallback mode and begin to act as a
hub, meaning every frame will be forwarded to every host on the network.
5


### Slides — strona 179

Port Security
Overview
The Port Security feature is used to restrict input to an interface by
limiting MAC addresses of workstations that are allowed to access a
specific port.
When secure MAC addresses are assigned to a port, the port will not
forward packets with source addresses outside the defined group.
6
By default, port security is not defined on switches and requires configuration.
6


### Slides — strona 180

Port Security
Violation Modes
Shutdown
This is the default violation mode. When a violation
occurs, the port will be shut down and logged
automatically. The port must then be reset manually to
become operational again.
@ The port security feature includes
Restrict three protection modes to handle
1 | | | In case of a violation, Ethernet frames with incidents in which it receives an
! unauthorized source MAC addresses are dropped. The Ethernet frame with a restricted
a switch provides notification of security violations and MAC address.
keeps count of the number of violations. yi
Protect
In case of a violation, Ethernet frames with
unauthorized source MAC addresses are dropped. In
this violation mode, the switch does not provide
notification regarding the event. yi
re


### Slides — strona 181

Port Security
MAC address learning can be performed in one of two ways: Manual or Sticky.
Manual
© The manual method requires static configuration of each allowed MAC address and its
assignment to an interface. This is the most secure method, but it is very time consuming
7) and open to faulty configuration.
Sticky
In the sticky method, allowed MAC addresses are learned dynamically and are limited to
the maximum number configured for the interface. The switch learns the source address
of the first few devices associated with the interface, providing a fast and scalable
l= method of operation.
8


### Slides — strona 182

Max Allowed MAC Addresses Raitt statis
Switch# show interfaces
Although the number of default MAC addresses allowed fastEthernet @/1 status
in Port Security is one, the number can be changed
within the range of 1 to 3072. Port Status
a FaQ@/1 err-disabled
Err-disabled

When a switch port is in Err-disabled mode, the

port may have been disabled automatically by the

switch operating system, due to port security

shutdown mode violation.

@ [el
To determine if Err-disabled was turned off for a port, run the show interfaces [interface] status command.
5


### Slides — strona 183

Port Security
Duplex Mismatch
sd 9 Q This state occurs when two parties, set for point-to-point CEchonnetO/A in Sumy [ eae pee Ce ae EERE]
ele . . . . 100000 Kbit, DEY 1000 usec,
communication, are configured to use different duplex gq TREAT Ay as6 (298) ekipedia 7s, cmetosat/25s
modes. wibauple, 100%b/e"
Sb type: ARPA, ARP Pimeout OA0000
Bad NIC Se ee
A faulty network interface card with software or hardware fh Toast oticinen situ ce likie cancicton
issues may trigger the Err-disabled state.
Err-disabled may be triggered due to
Broadcast Storms reasons other than Port Security.
» When there is a broadcast volume too large for processing
in the broadcast domain, the switches may be
overwhelmed and trigger the err-disabled mode on their
os ports.
10


### Slides — strona 184

Port Security
Port Security Requirements
Access Mode
Access ports are responsible for traffic flow.
Access mode should only be defined on ports connected to endpoint
devices, such as PCs.
You can configure port security on interfaces that you configured as
access ports with access mode.
e
Kul


### Slides — strona 185

Switchport mode access
switchport port-security
Enabling port security is done
in the interface configuration Switch(config)# interface fastEthernet @/1
mode, which is set using Switch(config-if)# switchport mode access
: Switch(config-if)# switchport port-security
Switch(config-if)#
Then, Access mode needs to be set
with fs
For port security to operate correctly,
the interface must be configured as
an Access port.
Finally, Port Security can be
enabled on the interface using
the command


### Slides — strona 186

switchport port-security [configuration] [value]
Port Security is configured by setting Switch(config)# interface fastEthernet 0/1
up each component individually Switch(config-if)# switchport mode access
using the same structure. Switch(config-if)# switchport port-security
z ORR RR KE BOR OR BR RK RK EK OK KE KK KK KK KKK KK KKK KK KKK KK KKK KKK KK KK KKK KK KKK KKKEKKEK
defines the type of
violation rule to be applied to
the port. Switch(config-if)# switchport port-security violation restrict
Switch(config-if)# switchport port-security mac-address sticky
The commands Switch(config-if)# switchport port-security maximum 5
and define sticky
learning, up to a maximum of
five addresses.


### Slides — strona 187

Switch# show port-security
Presenting the authorized MAC Secure Port MaxSecureAddr CurrentAddr SecurityViolation Security Action
addresses associated with a port (Count) (Count) (Count)
and the type (sticky or manually) ooo eee eee eee eee eee eee eee eee eee eee
is done with the command FaQ/1 5 1 @ Restrict
Fa@/2 al () 2) Shutdown
If only an overview is needed,
can be run Switch# show port-security address
for a quick overview of the Secure Mac Address Table
configuration. PRED I2S eee
Vlan Mac Address Type Ports Remaining Age
To view a specific interface, the (mins)
command _ a a a oO ee
should be 1 Q002.1798.DAC6 SecureSticky FastEthernet®/1 =
used, since it provides more 1 Q090.2172.8736 DynamicConfigured FastEthernet@/2 =
information. nnn IIS
Total Addresses in System (excluding one mac per port) : O
Max Addresses limit in System (excluding one mac per port) : 1024


### Slides — strona 188

Port Security
2 eee The objective of this exercise is to implement Port Security
Configure and Verify Port Security ona switch, pigetes using Port Security options, and learn
= | how to verify settings.
30-60 Min. _
i . ®@ Configure & Verify Port Security
a ’ =; "
ia >»
i b NN s e yr
| ‘ ‘Ss i) _ i 3 ® All platforms @ Lab document
= 88 W ®@ Cisco Packet tracer 7.2.2 @ NET-04-L1.pka
; ‘i } and higher
: :


### Slides — strona 189

CO
Switch Security
REMOTE ACCESS


### Slides — strona 190

Remote Access
Overview
Today, other than for initial configuration, most access to deployed
Y switches is done remotely.
Remote access allows administrators to manage and monitor their
_ network devices from anywhere in the network.

ba This is important, since some switches may be located in physically

inaccessible areas.
Two common remote access protocols are used in switches today: SSH and Telnet.
Le


### Slides — strona 191

Remote Access
Telnet Vs. SSH
Telnet and SSH are the two most widely used CLI-based remote access protocols.
Telnet
Telnet was developed many years ago to allow users to manage devices from anywhere,
)) via a simple and minimal configuration. However, using Telnet involves a potential
security risk because usernames and passwords are sent in plain text on TCP port 23.
SSH
lolonolon oo, . Lag .
pul md SSH is similar to Telnet, but with a significant difference: SSH encrypts all data transferred
mi ttt between the user and end device. SSH uses RSA encryption, a robust and reliable
He TOOlIN encryption type. It operates on TCP port 22.
18


### Slides — strona 192

Remote Access
SSH Encryption
RSA Encryption
Modern encryption relies heavily on the RSA algorithm since most
methods use public and private encryption keys.
Z The public and private encryption key method, also known as
€ ) asymmetric cryptography, uses two different, but mathematically
linked, keys.
9 ..- 7 The public key is shared with everyone, while the private key is only
given to specific persons.
RSA ensures implementation of the CIA triangle, and avoids
authentication rejection.
B
19


### Slides — strona 193

Remote Access
SSH Encryption
RSA Encryption
Protocols like SSH and SSL/TLS use RSA to encrypt communication
and digital signatures.
Although RSA works through the computational difficulty of factoring
a large integers, computational complexity grows exponentially every
€ ) day, and larger and larger numbers are required to maintain secure
communication.
? ../.- 7 RSA is dependent on a powerful computational system. The more
complicated the keys are, the more power is required.
Recently, ECC (Elliptic Curve Cryptography) is becoming more
popular, since it can create faster, smaller, and more efficient
cryptographic keys.
B
20


### Slides — strona 194

—_— Encryption/Decryption Process
Asymmetric encryption is when two Public key
different keys are used to encrypt and £
decrypt messages.
The keys are mathematically related in a
way that messages encrypted with one
My 2 e ° yp af & A Decryption af
key, typically the public key, cannot be
CLEAR toro! CLEAR
decrypted by it. | er Encryption [izes a | atl
The decryption can be done only using the
corresponding private key in the key pair.
This method is considered to be more Private key
complex and slower than symmetric
encryption, which uses one key for both
encryption and decryption. fal
_
Data transfer
ee
Key publicly available Pr
Pail


### Slides — strona 195

Remote Access
Virtual Teletype
eee . . . . .
Virtual Teletype (VTY) is a command-line interface (CLI) in network
devices used to create remote access connections.
VTY is virtual and does not require any hardware.
Switches have 16 VTY lines (0-15), routers have 5 VTY lines (0-4).
22


### Slides — strona 196

Switched Virtual Interface

The primary purpose of creating a computer network is to share
resources and enable communication within the network.

oO Layer 2 switches create VLANs (Virtual LANs) that form a single

} ) broadcast domain. If a broadcast message is sent within the same
t- — VLAN, all devices connected to that VLAN will receive the message.
—O—————__ Hosts can communicate on the same VLAN without a Layer 3 device
(router). Devices on a different VLAN, on the other hand, cannot
communicate with each other, without proper routing.
&
23


### Slides — strona 197

Switched Virtual Interface

A router or Layer 3 switch can handle network segmentation and
inter-VLAN communication.
A router can segment a network and create separate broadcast

re) domains, with each network segment using a different sub-interface

) of a physical interface on the router.
t- — _ Layer 3 switches require the creation of multiple VLANs on the
5° o- switch, which form multiple broadcast domains. Then, for each
VLAN, a corresponding Layer 3 interface needs to be created on the
switch, to handle the routing.
This Layer 3 interface is the SVI.
The difference is that the SV! Layer 3 interface is virtual.
&
24


### Slides — strona 198

Remote Access
SSH Configuration
Ol Change the default hostname. | | Set a security message. 05
Q2 Create a user account. | | Enable VTY lines and limit protocol access. 06
03 Set the enable password. | | Enable Layer 3 connectivity. OT
QA. Configure a domain name. | | Generate SSH keys. 08
25


### Slides — strona 199

Switch(config)#hostname S1
S1(config)#username Admin password p@nd@

Several initial settings must be S1(config)#enable password c!sc@

configured before enabling SSH : : F

on the device. S1(config)#service password-encryption
S1(config)#banner motd #Access to this device is for authorized
personnel only!#

1. Setithe:device name. S1(config)#ip domain-name CyberPro.com

2. Create a local account.

3. Secure the privileged mode.

4. Set an appropriate security

message (optional).

5. Set a domain name.


### Slides — strona 200

line vty <id-range> & login local
Step 1 - Enter the VTY configuration S1(config)#line vty @ 15
triode. Selerkeheaiimilier Sf S1(config-line)#login local
maximum sessions. r : :
S1(config-line)#transport input ssh
Step 2 - Enable authentication S1(config-line)#exit
using username and password.
Step 3 - Telnet is enabled by default;
the transport command prevents
using Telnet and only uses SSH for
remote connections. The options are
none, all, Telnet, or SSH.


### Slides — strona 201

interface vlan 1

ip address <ip-address> <subnet-mask>
S1(config)#interface vlan 1

S1(config-if)#ip address 10.0.0.150@ 255.255.255.0
S1(config-if)#no shutdown

S1(config-if)#exit

S1(config)#ip default-gateway 10.0.0.1


### Slides — strona 202

crypto key generate rsa
The crypto key command generates S1(config)#crypto key generate rsa
the Private and Public RSA keys on The name for the keys will be: S1.CyberPro.com
the networkideyice. The switchior Choose the size of the key modulus in the range of 360 to 2048 for
router needs those keys to secure
the SSH session. your
General Purpose Keys. Choosing a key modulus greater than 512 may
take
Set the key length. The default is a few minutes.
512, but it is recommended to set
the number of bits to higher than How many bits in the modulus [512]: 1024
1024. The maximum value is 2048. % Generating 1024 bit RSA keys, keys will be non-exportable...[OK]


### Slides — strona 203

S1#show ssh
Connection Version Mode Encryption Hmac State
Username
The show ssh command 2 1.99 IN aes128-cbc hmac-shal Session
presents the active SSH sessions Started Admin
on the network device. 2 1.99 OUT aesi128-cbc hmac-shal Session
Started Admin
%No SSHv1 server connections running.
Show ip ssh displays the version oe
definition, authentication
timeout, and retries.
S1#show ip ssh
SSH Enabled - version 2.0
Authentication timeout: 128 secs; Authentication retries: 3


### Slides — strona 204

GE Administrator: Command Prompt - ssh -I root 192.168.137.129
Microsoft Windows [Version 10.0.18362.239]
(c) 2019 Microsoft Corporation. All rights reserved.
Accessing the device remotely IC: \Windows\system32>ssh -1 root 192.168.137.129
using SSH can be done using a root@192.168.137.129's password:
CLI, such as PuTTY or a device
terminal.
The universal command for creating
an SSH session is: h
ssh -1 <username> <target-ip>
In the example on the right,
the command is executed in
Windows CMD.


### Slides — strona 205

Remote Access
The objective of this exercise is to set up the SSH service on network
pen VWaVayay : devices for remote management from anywhere on the network. In
Remote Access with SSH | addition, this exercise practices configuring IP connectivity to a Layer 2
30-60 Min. A : switch using the In-Band Management method.
=e ® Configure SSH.
. 4 ‘ @ Verify SSH configuration.
—— ® $ di
| i) a J ® All platforms ® Lab document
; W | ® Cisco Packet Tracer 7.2.2 @ NET-04-L2.pka
or higher
4
| |
l iY |
{ \ ) Fy ™ “= roy


### Slides — strona 206

’ = j FO Saw ~
= a # 4 i
4 ~~ ie
v). a " % * a4 a A
i >» ; Ss
> \ >
Chie —— . =
Fed Axncoes ta os 2 Spe
& Mh if
A ; 4 ~S : ra
=m Z By: ie ~~ zs
= Payee SQ


### Slides — strona 207

a i ™" : = a aw NETWORK ee Bal Ci = L D


### Slides — strona 208

<a = —— :
il LAYS) ea IDESIGN - ‘ ¥ = =
= IP. & ROUTING =
Computer Networking
Copyright © 1996-2023 HackerU Ltd. All Rights Reserved.


# Chapter 5: IP & Routing Concepts


### Slides — strona 209

Computer Networking
Introduction Network 10s Switch Securit IP & Routing
to Networks Fundamentals Fundamentals y Concepts
Diagnostics & Dynamic F :
Troubleshooting VLANs & Trunk Reuiting Static Routing Subnetting
Access Infrastructure
Control List Services


### Slides — strona 210

Computer Networking
Overview
Lesson Objective ’ ’
Decimal, Binary, and Hex
In a network, IP addresses are used to The Router
identify a device’s source and destination.
The object of this lesson is to understand Routing Process
routers, how they work, their processes, and
the logic involved in IPv4/6 configuration.
G


### Slides — strona 211

OO
IP & Routing Concepts
DECIMAL, BINARY, AND HEX


### Slides — strona 212

Decimal
fExaail The most common numbering system consists of ten numbers, 0-9, and it is called the decimal
‘|= em. system. The system is based on the 10 fingers we use to count and is known as the base-10
S| | numeral system.
Binary
Binary is an alternative number system that consists of only two numbers: 0 and 1. This system
is used by computers, which communicate by transmitting negative and positive electrical
currents. Because there are only two numbers, the system is known as the base-2 numeral
system. a
Hexadecimal
Hex, or Hexadecimal, is a number system that consists of 16 characters, and is known as the
base-16 numeral system. Hex uses the numbers 0-9, followed by the letters A-F. Hex is widely
used as an alternative representation to binary, since it is a more human-oriented system.


### Slides — strona 213

Decimal, Binary, and Hex
Positional Notation
Positional Conversion
When learning about number systems, a The Digits: Bt (2) al i
good way to approach them is to consider 02 The Positions: 23 22 21 20
numbers a result of their positions. $5 es
Base2 The Result: 8 i) zz i
Each number’s value can be calculated as
a result of a function. The Digits: 1 e 5 4
10 The Positions: 107 102 10: 10°
The function is the same regardless of the TT
base being used, making it easier to perform Base10 The Result: 10ee @ 220 4
base transitions.
The function is: The Digits: B a ) 5
[number] = [digit] * [base] “ [position]. 1 6 The Positions: 163 162 161 162
Baseié The Result: 45056 256 2) 5


### Slides — strona 214

Decimal, Binary, and Hex |
Binary to Decima
found. The next step is conversion, summarizing each of the individual values to get the result.
Conversion Formula
Positional Value 128 64 32 16 8 4 2 1
Result 128+64+0+16+0+4+0+0=212
EEE


### Slides — strona 215

Decimal, Binary, and Hex
Positional Conversion
While the aim of ion to decimal is t oe 20= 1024 ” 28
ile the aim of conversion to decimal is to - -
solve a formula, the aim of conversion from 1024 8
decimal is to find the missing variable. 970 29=512 2 21=2
“512 “2
The operation can be summed up as find
the X that will result in the closest number. 458 28=256 (3)
; 256
For example, when converting the number 32 16 8 4 2 1
1994 to binary, the first step is to find X, 202 27=128
where 2% is the closest to 1994. _ a 0 ri a 4“ 6
128
Continuing this process, the number should 74 26=64
be written down and the calculation should = 2048 1024 512 256 128 64
be repeated for the remainder. 64
10 27=8 0 41 1 1 i 1


### Slides — strona 216

Decimal, Binary, and Hex
Division Calculation
For binary, there are some tricks that can
make the calculation easier, instead of me oe p ‘ ‘
having 16 Buess 62. 124 249 498 997 1994
One trick is to take the desired number i) 1 i) 1 i)
and divide it, without the remainder,
while recording each operation.
If the result is even, write a O. If it is odd, 1 3 S 15 31
write a 1. The binary representation will
appear when the operations are done.
1 i A 1 iL
For other bases, there are other tricks and
mathematical methods.
11111001010


### Slides — strona 217

Decimal, Binary, and Hex i |
Binary to Hexadecima
considered a representation of 4 binary digits. For example, 101110 is 0010 + 1110, making it 2E in hexadecimal.
Conversion Formula
Number 0 1 2 3 4 5 6 7
Hexadecimal 0 1 2 3 4 5 6 7
Number 8 9 10 11 12 13 14 15
Hexadecimal 8 9 A B € D E F
Eze


### Slides — strona 218

Decimal, Binary, and Hex
Hexadecimal Conversion
Binary to Hex
¢ Divide the binary number into groups of 4 digits.
b04%00%:| © Convert each group to its equivalent hex value using the Base Comparison table.
¢ Merge the results of each group.
Example
Convert 0111111111010100 to hex.
A OR] e 0111 1111 1101 0100
* 0111 =7, 1111 =F, 1101 =D, 0100 =4
° Answer is 7FD4 eo


### Slides — strona 219

Decimal, Binary, and Hex
Other Bases
Base-X
There are other bases besides binary, decimal, and hexadecimal.
Throughout history, other counting systems, such as base-6, base-8,
and base-12 were developed.
Old British measurements, such as dozen (12), gross (144), and feet
(12 inches) are suspected to have been originated by a base-12
number system.
&


### Slides — strona 220

ox ae . et el 7 The objectives of this exercise are to understand
Converting Decimal, Binary, and Hex numbering systems and how to convert between them.
30-60 Min.
= a r yA ' 7 Convert Decimal to Binary
, ’ « ; ® Convert Binary to Decimal
mi ee q 4 = ® Convert Binary to Hex
iw | LA ® Convert Hex to Binary
| - iY @ ; ® Calculator ®@ NET-05-L1 Converting
: Decimal ,Binary, and Hex
4 |
*
. ~_———
i 4 —7


### Slides — strona 221

OO
IP & Routing Concepts
THE ROUTER


### Slides — strona 222

The Router
Overview
Router
A router is a device designed to receive, forward, and analyze
packets transmitted to and from other devices on a network, and
other networks.
Routers enable inter-network communication, and can provide
services such ACL and NAT, which are required in any networking
scheme.
6
A router is a Layer 3 device that communicates using IP addresses.


### Slides — strona 223

The Router
Default Gateway
Default Gateway
The default gateway is a network device that can route traffic to
and from other networks. A router typically fulfills this role.
The default gateway is similar to the door of a room. If a desired
object is in another room, the object can be reached only by
exiting through the door.
B


### Slides — strona 224

Default Gat Confi ti
NIC Configuration
Default gateway configuration =
options are typically located “ Internet Protocol Version 4 (TCP/IP v4) Properties x
together with other adapter i General
' Ovganize * Connect To Disable this ne! Connect using: a oe
configuration options. . ‘You can get IP setings assigned automaticaly if 1vork
e P A Bluetooth Network Cemnection G® keel) Dual Bard Wireteas-AC 8260 Pecos Odherwton, youeed Weck your network ede ator
Mat connected the aoprocriate IP settings.
In Windows, the settings are = Wii This connection uses the folowing tema (Co0btan an IP address automaticaly
located under Network & a student 2 Epi chert or Microsc Networks 7 se te toning Paces
F . Intel(R) Dual Band Wireless-AC 62. 4 Vidware Bridge Protocol BP address: 192.168. 0 . 10
Internet Settings in Change "SP Fie and Porter Shar for Microsoft Networks
Ad Oti SB tualBox NOISE Badged Netwatking river Sabet mask: 255.255.2558. 0
japter Options. a peellerearragial Default gateway: oe eT
% Boos Packer Scheduler .
4 9. itemet Protocal Version 4 (TCP/IP) . a ae
By default, the gateway should s z Gi0ki te haa cre aarti
be received from the DHCP. hia iret Propels Preferred DNS server: 3.8.8.8]
Desorption
Te Cat Plt Praca The dod Alternate ONS server: Ls -.8-.4.4/]
# area network, prot ‘prov | COMMUNES ION
However, if manual IPs were acront diverts interconnected networks Aivaldate settngs upon est z
configured, the gateway should
also be configured manually. ok Cancel =
jm
—
=


### Slides — strona 225

Logical Ports
Fast Ethernet Interface 2 ee ey
— @ Fast Ethernet was first made public in 1995. Ethernet % >. - . ,
= operates at a speed of 100 Mbps and uses the media ' oo -
standard 100BaseT. a . >
Gigabit Ethernet Interface PND
Gigabit Ethernet was introduced in 1999, and it
supports a faster speed of 1000 Mbps. It uses the media
standard 1000BaseT, but can also support 100 Mbps.
cA
Serial Interface
Serial interfaces are used for long distance transmissions.
If two serial ports need to communicate with each other,
they must be synchronized with the same clock frequency
and allocate the necessary bandwidth. a


### Slides — strona 226

The Router
Other Router Interfaces
Console
</> This is a physical management port, visually similar to Ethernet ports, that provides
out-of-band access to a Cisco device. Out-of-band refers to access via a dedicated
_. management channel used only for device maintenance.
AUX
i The auxiliary port mainly functions as a backup console port, although it can also be used
l as a dial-up port for remote management, and other purposes. The main difference
LU between Console and AUX is that AUX pushes output to the port after power-up, while a
Console does so during the power-up process itself.


### Slides — strona 227

Router interfacesneedito be R1(config)#interface gigabitEthernet @/@
set up with IP addresses, R1(config-if)#ip address 192.168.0.1 255.255.255.0
similar to computer network . .
interfaces: R1(config-if)#no shutdown
%LINK-5-CHANGED: Interface GigabitEthernet®/@, changed state to up
The R1(config-if)#exit
command selects the desired R1(config)#exit
iiterface. Ri#show ip interface brief
To use an interface, it must be Interface IP-Address OK? Method Status Protocol
set up with GigabitEthernete/e 192.168.0.1 YES manual up up
and enabled using the
command.
Use to
verify interface settings on the
router.


### Slides — strona 228

The Router
Loopback Interface
What it is used for ...
7~ Loopback is a logical interface that is not assigned to a physical port.
The interface can be used to test and manage Cisco IOS devices, because
SJ it ensures that at least one interface will always be available.
It can also be used in the OSPF identification process.
e


### Slides — strona 229

seit ratitianeds 5 ord Router(config)#interface loopback @
configured Suring tne.inttis %LINK-5-CHANGED: Interface Loopback®, changed state to up
router configuration, mainly 6 .
for testing/purposes. %#LINEPROTO-5-UPDOWN: Line protocol on Interface Loopback@, changed
state to up
The interface is configured . .
to automatically be ready Router(config-if)#ip address 10.10.10.10 255.0.0.0
for operation. Router(config-if)#no shutdown
Router(config-if)# exit
A router can have more than
one loopback interface enabled
simultaneously, but each
interface must have a unique IP.
A loopback interface is created
using the command
via the configuration terminal.


### Slides — strona 230

OO
IP & Routing Concepts
ROUTING PROCESS


### Slides — strona 231

Routing Process
Overview
The Routing Process

The routing process involves selecting a path for the delivery of
packets across different networks, from source to destination,
through Layer 3 devices.
It is important to note that routers can route packets to directly
connected networks, without requiring configuration. However, if
the networks are not connected, the route needs to be learned.
Routing decisions are made based on a routing table.


### Slides — strona 232

Routing Process
Examination
In the first step, the router decides whether to
process a packet or ignore it. Routers will ignore ie Decapsulation
packets with errors, or packets they don't know The router examines the Layer 2 address to
how to process. decide if the packet was intended for itself (the
default gateway), and verifies the integrity of the
Decision-Making frame using the FCS (Layer 2 trailer).
The router decides where to forward the packet
to, based on its destination IP address and the a e Encapsulation
ting table.
rouring rane The router re-encapsulates the packet with new
Layer 2 headers for the next hop, according to
. the decision made in step 3.
Forwarding 7
After a decision is made, the router forwards the
packet to the interface from which the packet
must exit.


### Slides — strona 233

Routing Process
Routing Choices
oe es
=eeee Pre
ess oe ee
pS
If the destination IP is on If the destination IP is ona If there is no static or If there is no ‘gateway of
the same LAN as the source different LAN, but the dynamic route in the last resort’ and the
device, there is no need for network device has a static network device’s routing destination packet is not
routing. The frame will get or dynamic route to the table, it will forward the listed, the router will
to the destination via the destination IP, it will forward packet to its default discard the packet.
switch. the packet to the next hop, ‘gateway of last resort’.
based on the route.


### Slides — strona 234

Router# show ip route
The Routing Table contains Codes: C - connected, S - static, I - IGRP, R - RIP, M - mobile, B - BGP
data stored in the router, with D - EIGRP, EX - EIGRP external, O - OSPF, IA - OSPF inter area
lists of routes to possible N1 - OSPF NSSA external type 1, N2 - OSPF NSSA external type 2
network destinations. E1 - OSPF external type 1, E2 - OSPF external type 2, E - EGP
i - IS-IS, L1 - IS-IS level-1, L2 - IS-IS level-2, ia - IS-IS inter area
* - candidate default, U - per-user static route, o - ODR
The table includes information P - periodic downloaded static route
about the network topology.
Gateway of last resort is not set
The codes on the left side of a 172.16.0.0/16 is variably subnetted, 5 subnets, 2 masks
route show how the network is ) 172.16.0.0/16 [90/5376] via 192.168.4.2, 00:02:24, GigabitEthernet4/o
learned by the router. G 172.16.0.0/24 is directly connected, GigabitEthernet@/o
Ss 172.16.1.0/24 [1/0] via 192.168.1.2
. R 172.16.2.0/24 [120/1] via 192.168.2.2, 00:00:15, GigabitEthernet2/0
The command show ip route 0 172.16.3.0/24 [110/2] via 192.168.3.2, 00:01:26, GigabitEthernet3/0
displays the routing table and C 192.168.1.0/24 is directly connected, GigabitEthernet1/0
is run in the Enable mode. C 192.168.2.0/24 is directly connected, GigabitEthernet2/0
C 192.168.3.0/24 is directly connected, GigabitEthernet3/0
C 192.168.4.0/24 is directly connected, GigabitEthernet4/o


### Slides — strona 235

Routing Process
Directly Connected / Local Route
When inspecting the routing table, records identified by the codes C or L indicate directly
connected networks. The codes mean that the devices are connected to the physical layer.
The C and L records are automatically created.
Static Route
x Static routes are configured and recorded manually, and are identified in the routing
table by the letter S.
Dynamic Route
Dynamic routes are identified with unique letters that indicate the dynamic
S, protocol, as follows:
D - EIGRP routing protocol
O - OSPF routing protocol
R - RIP routing protocol a


### Slides — strona 236

IP & Routing Concepts
IPV4


### Slides — strona 237

IPv4
Overview
IP
An Internet Protocol (IP) is a numerical label assigned to devices
@ connected to a network. It is used for host identification and
communication.
The IP address space is managed by IANA (Internet Assigned
Numbers Authority) and divided into five regional Internet registries
(RIRs), each responsible for their designated territories.
e
Each RIR is responsible for address assignment to users and service providers.


### Slides — strona 238

IPv4
IPv4 Addresses
IPv4 addresses consist of 32 bits and are divided into four octets, each containing 8 bits.
This addressing method provides 4,294,967,296 (232) IPv4 addresses in total.
An IP address represented in binary will appear as follows:
192.168.1.1 = 11000000.10101000.00000001.00000001
IPv4 Structure
4 7 An |Pv4 address consists of two parts: network and host, defined by the subnet mask.
. Lie Network - Represents the network part of the IP address.
SS Host - Represents the specific device on the network segment.


### Slides — strona 239

IPv4
Subnet Mask
Subnet Mask
A subnet mask is a 32-bit address, same as an IP address.
Like an IPv4 address, a subnet mask consists of 4 octets, separated
by dots (.).
Subnet masks will be further explained in the next module.
o)
Two similar IP addresses can belong to completely different networks, depending on the subnet mask.


### Slides — strona 240

IPv4 f
Classful Addressing
Inter-Domain Routing in 1993. It divides IPv4 address space into 5 classes, based on the 4 leading address bits.
Classful Table
NETMASK RANGES PREFIX CLASS
255.0.0.0 1.0.0.0 - 127.255.255.255 /8 A
255.255.0.0 128.0.0.0 - 191.255.255.255 /16 B
255.255.255.0 192.0.0.0 - 223.255.255.255 /24 C
* Reserved for multicasting 224.0.0.0 - 239.255.255.255 D
* Experimental 240.0.0.0 - 255.255.255.255 E
NOTE: 255.255.255.255 is reserved as the IPv4 Broadcast address. ey


### Slides — strona 241

IPv4.
Communication Types
Unicast
The most basic form of IP communication is one-on-one, where a packet is sent
directly from one device on the network to another device on the network.
A single source communicates with a single destination.
Multicast
— Multicast is when a single source communicates with multiple destinations. A packet
— is sent from one device on the network to a group comprised of one or more devices,
GE using Class D addresses.
Broadcast
Broadcast is when a packet is sent from one device on the network to all other
f 5 devices on the network, using a generic broadcast address (255.255.255.255 or
FF:FF:FF:FF:FF:FF).


### Slides — strona 242

IPv4 Link Local
Link-Local
Link-Local addresses, also known as APIPA addresses, are valid only
for communication within the network broadcast domain. The entire
169.254.0.0/16 address range is reserved for Link-Local.
If the DHCP is not available or an IP is not statically configured, the
(BR (\. OS will randomly generate a Link-Local address.
)
4h an Link-Local addresses are not guaranteed to be unique outside their
network segment, which is the reason why routers do not forward
their packets.
&


### Slides — strona 243

IPv4
Loopback Address
Loopback Address
Loopback addresses represent the same interface in a
computer. In IPv4, an entire network (127.0.0.0/8) is reserved
for loopback addresses.
J Almost all leading operating systems use the name "localhost"
to represent IPv4 loopback address 127.0.0.1.
&


### Slides — strona 244

IPv4
Public vs Private
IP addresses are typically divided into two groups: private and public.
Private
IN Private IPs are non-unique addresses that can belong to one of three IP address ranges.
a _ They are used to create networks that do not communicate over the Internet.
E The same private IPs can be found in multiple separate networks and are free to use.
Public
Public addresses are used for communication over the Internet. These IP addresses must
be unique, require a fee, and are purchased from service providers. A router will typically
have both a private and public IP. For example, the address 8.8.8.8 is a public address
used by Google.


### Slides — strona 245

IPv4
Private addresses are used in networks designed for homes and organizations. The ranges differ according
to the amount of separate networks and computers in each network, and there are no enforced rules.
Ranges

RANGE TARGET CLASS

10.0.0.0 — 10.255.255.255 A few large networks with many computers. A

172.16.0.0 — 172.31.255.255 A considerable amount of medium-size networks. B

192.168.0.0 - 192.168.255.255 Many small networks with only a few computers. Cc


### Slides — strona 246

IPv4
a , 5 ] ; . The objective of this exercise is to learn how to configure
IPv4 & initial Router Configuration initial settings on a Cisco Router.
30-60 Min. \\
= 7“ Ff yA ‘ . Initial Router Configuration
. ’ « ; ® Configure IPv4
.——.. =. wy ~.
| van a! ® os @ NET-05-L2 IPv4 and Initial
, * All platforms Router Configuration
. y) @ Tools ®@ NET-05-L2.pka
. ® ; | © Cisco Packet Tracer 7.2.2
i % ) =~


### Slides — strona 247

IP & Routing Concepts
IPV6


### Slides — strona 248

IPv6
Overview
The Need for IPv6é
Over the years, the IPv4 address space was depleted, since technical
progress meant that many more devices around the world were
connected to the Internet.
IPv6 was designed to solve the IPv4 address space limitation and
provide some additional enhancements. IPv6 has a larger 128-bit
address space, with the number of available addresses being 340* 102°,
é
Example of an IPv6 address: 2001:0000:3238:0001:0063:0000:0000:FEFB


### Slides — strona 249

IPv6
Compressing IPv6 Addresses
IPv6 addresses are long and difficult to read.
Some rules exist to omit specific numbers to Full Address
simplify the addresses. A full address contains all 8 blocks, with 4
hexadecimal digits.
Example of a full IPv6 address:
Leading Zeros a 2001:0000:3238:0001:0063:0000:0000:FEFB
The first rule allows us to discard leading zeros
in a block, making the address a bit shorter: i Consecutive Zeros
2001:0:3238-1:63:0000-0000:FEEB If two or more blocks contain consecutive zeros,
they can be omitted and replaced with double colon
signs (::) resulting in: 2001:0:3238:1:63::FEFB
Zero Block 7 Note that omitting is allowed only once in the
If there is a block that consists of 4 zeros, but
i . : 3 address.
without a consecutive zero-filled block, it can be
replaced with a single zero, and the final address
will be: 2001:0:3238:1:63::FEFB


### Slides — strona 250

IPv6 Address Breakdown
IPv6 Address t
| 2001:0ABC:00BB:'! 0000 }:0000:0000:0000:0001 | /64
1 ! 2 ! 3 1; a
</>
Configuration Example
Router(config-if)#ipv6 address
The prefix represents the prefix portion of the address. IPv6 does not use 2001: GABC : OBB : 8800 : 0000 : 0000:
notation subnet masks like IPv4. The prefix length indicates the network 0000: 0001/64
portion.
1. Because the prefix is /64, the first 64 bits in the address represent the
network portion.
2. The 16 bits from the 49th to the 64th are for defining subnets.
3. The remaining 64 bits represent the host portion in the IPv6 address.
4. The range can be from 0 to 128, with the most common being /64.


### Slides — strona 251

Router(config)#ipv6 unicast-routing
To enable IPv6 routing, Router(config)#interface gigabitEthernet/0/e
enter the configuration Router(config-if)#ipv6 address 2001: @ABC:@@BB: 0000: 0000: 0000: 0000: 0001/64
terminal mode, and run Router(config-if)#no shutdown
the command Router (config-if)#exit
Router#show ipv6é interface brief
GigabitEthernet0/0/0 [up/down]
Configure IPv6 on the FE8@: :201:97FF:FE13:A801
router interface using the 2001: ABC: BB: :1
command GigabitEthernet@/0/1 [administratively down/down]
unassigned
Vlan1 [administratively down/down]
Verify the configuration using unassigned
the command


### Slides — strona 252

IPv6
Device Communication Types
Unicast
({) Unicast addresses represent specific network interfaces that support IPv6.
O-- Unicast addresses have 3 sub-types (described in the following slide).
Multicast
Q Addresses used to send IPv6 packets from a single host to multiple destinations.
Anycast
ae IPv6 unicast addresses that can be assigned to multiple devices. Packets sent to an Anycast
5S address are routed to the nearest device that has that address (which is why Anycast is
I o =I also known as "one to the nearest“). This method operates similar to IPv4 broadcast.


### Slides — strona 253

IPv6 Unicast Types
Global Unicast
4 xy IPv6 global unicast addresses are similar to IPv4 public addresses. They are unique
and can be routed via the Internet. IANA currently assigns only 2000::/3 addresses.
Link-Local
r) [7 Addresses that enable communication between devices in the same local link (LAN).
5 Link Local addresses must be unique only within the link. They are not guaranteed to
tit be unique beyond their network segment, and begin with FE80::/10.
Unique-Local
Similar to IPv4 private addresses, with minor differences.
(mann) Unique addresses should not be routable in the global IPv6, and should
= not be translated to global IPv6 addresses. They begin with FCOO::/8.


### Slides — strona 254

IPv6
IPv6 Address Example
Common IPv6 Addresses
Type Address Example Notes
Global Unicast 2001:0ABC:1111:0000:1111:0000:0000:0200 The address range is from 2000 to 3FFF.
Global Unicast 2001:0ABC:0000:00BB:DCBA:0000:0000:0200 The address range is from 2000 to 3FFF. .
Link-Local FE80:0000:0000:0000:3211:5412:ECDC:FE11 Link-local address prefix is FE80::/10.
Link-Local FE80:0000:0000:0000:3211:5412:CAD1:FE12 Link-local address prefix is FE80::/10.
Multicast FFO2:0000:0000:0000:0000:000F:FFOO:120F Multicast addresses use the prefix ff00::/8.
Anycast XXXX.XXXXXXXX!XXXX!0000:0000:0000:0000 Similar to broadcast addresses in IPv4.
Ee


### Slides — strona 255

IPv6
Dual Stack
Dual Stack means that a device runs both IPv4 and IPv6
protocols simultaneously. Using two stacks allows both
IP versions to coexist.
: F Tunneling
IPv4 and IPv6 can coexist using
protocols and tools created by Tunneling is used when IPv6 addresses are to be sent
IEFT, which are known as: Dual S» over IPv4 networks, or vice versa. In this method, the
Stack, Tunneling, and Translation. IPv6 packet is encapsulated within an IPv4 packet.
Translation
Translation allows IPv6 to communicate with IPv4-
enabled devices using techniques similar to those
used by NAT.


### Slides — strona 256

IPv6
LAB NET-05-L3 freee
= The objective of this exercise is to practice configuring IPv6é
Poe! q jog . addresses on a router and clients.
Cont igure IPv6 Add ressing | The lab also covers practicing verification of IPv6 addressing
30-60 Min. J implementation.
a Pa “ ® Configure IPv6 Unicast Global address on R1
4 \ « interfaces
etn S, ” ‘Ex, ; ® Configure IPv6 on Users PC’s and verify connectivity
("Pe Ly ‘ ® Configure IPv6 Link -local address on R11 interfaces
p Ce yo i @) and PC’s (Optional)
Sat. eet ne
a a 6! >
1 ~ >
A) ® r Sos > NET-05-L3 Configure IPv6
* All platforms ; Addressing
" yy @ Tools > NET-05-L3.pka
SA y
‘ . : | © Cisco Packet Tracer 7.2.2
8 ~~
J |


### Slides — strona 257

; ¢ 4 im Z f
se “ =) > Be 4

vl om ES \ . 7! >
So ~ Ww =
CDOS \ —

CTE > <=

SRS 2 SS

oe CSS i. > fo

SS \ ke sug ie

Bo PLO i Sy

* ‘ 4 Crs = f


### Slides — strona 258

aul egal 5 i 2B
—— — Sy " : ™ ty .
ie. = 4 a wet, NETWORK ga Cm D


# Chapter 6: Subnetting Concepts


### Slides — strona 259

atl
’ ? Cybersecurity Professional Program
a * a nD ‘Bee eee
-__- Subnetting Concepts
Computer Networking
Copyright © 1996-2023 HackerU Ltd. All Rights Reserved.


### Slides — strona 260

Computer Networking
Introduction Network Switch & IOS Switch Securit IP and Routing
to Networks Fundamentals Fundamentals y Concepts
Diagnostics and VLANs Dynamic IPv4 & IPv6é Subnetting
Troubleshooting and Trunk Routing Static Routing Concepts
Access Infrastructure Fiival Proiect
Control List Services d


### Slides — strona 261

Subnetting Concepts
Overview
Lesson Objective
Subnetting
The object of this lesson is to understand
how IP addresses and subnet masks operate, CIDR
and how they work together.
The lesson also covers how to configure VLSM
networks with the correct usage of resources
and why it’s important to employ CIDR.
Network Address Scheme Design
G


### Slides — strona 262

CO
Subnetting Concepts
SUBNETTING


### Slides — strona 263

Subnetting
Overview
Definition
Subnetting means subdividing a network to manage, design, and
implement an effective IP addressing plan. When organizations add
[SUB hundreds and even thousands of hosts to their network, subdividing the
network facilitates faster packet delivery and adds filtration by minimizing
local traffic.
Subnetting reduces overall network traffic and improves performance.


### Slides — strona 264

Subnetting
Broadcast Domain Issue
Large Broadcast Domains
Large networks containing many hosts poses a problem for
broadcast domains, because hosts can generate broadcast
messages and affect network performance.
A large amount of traffic generated by broadcast messages
causes network operation to slow down.
Each device must accept and process broadcast requests, even
if the request is not intended for a particular device.
2
The solution is to reduce the network size, and create smaller broadcast domains by subnetting the network.


### Slides — strona 265

Subnetting
Subnetting
Why Subnetting?
Subnetting improves network performance by reducing the
overall volume of network traffic.
In addition, it enables an administrator to implement security
policies and control network growth.
Subnetting creates more manageable network congestion, and
simplifies network administration.
&


### Slides — strona 266

Subnetting
Octet Boundary
What is an Octet Boundary?
An Octet Boundary is a subnet created by borrowing one or more
of the host bits to be used as network bits.
By extending the subnet mask with bits from the host portion,
] additional subnets can be created.
: The easiest method of network subnetting is to use the octets /8,
/16, and /24.
Additional 1 bits mean more Networks.
Additional 0 bits mean more Hosts. e
=f


### Slides — strona 267

Subnetting
The following table lists attributes of the most common boundaries: /8, /16, and /24.
Subnets
Prefix Subnet Mask Binary Number of Hosts
11111111.00000000.00000000.00000000
/8 255.0.0.0 nnnnnnnn.hhhhhhhh.hhhhhhhh.hhhhhhhh 16,777,214
255 0 0 0
11111111.11111111.00000000.00000000
nnnnnnnn.nnnnnnnn.hhhhhhhh.hhhhhhhh 65,534
/16 255.255.0.0 255 255 0 0
11111111.11111111.11111111.00000000
nnnnnnnn.nnnnannnn.nnnnnnnn.hhhhhhhh 254
/24 255.255.255.0 255 255 255 0
n=Network portion h = Host portion


### Slides — strona 268

Subnetting Concepts
CIDR


### Slides — strona 269

CIDR
CIDR Overview
. Since not all networks in an organization are compatible with IPv4
© ' address classes (due to the number of hosts), using these classes, in
ooss \ some cases, may result in a waste of addresses (which are important
' ' commodities in any organization).
A
== % For example, an organization with a network of 400 hosts must use
1
- class B, which means they will waste more than 60,000 addresses.
&


### Slides — strona 270

CIDR
Classless Inter-Domain Routing
Explanation
@-¢. To resolve this issue, Classless Inter-Domain Routing (CIDR) was
G defined in RFC 4632. CIDR allows an IP address to use any subnet
mask, regardless of predefined classes.
For example, IP address 10.1.1.1, which according to the class-based
system should be in class A, can belong to class B or C, in accordance
with the user’s preference.
&


### Slides — strona 271

CIDR
CIDR Addresses
Address Table

Subnet Address Useable Address Range Broadcast Address
10.0.0.0/16 10.0.0.1 — 10.0.255.254 10.0.255.255
10.1.0.0/16 10.1.0.1 — 10.1.255.254 10.1.255.255
10.2.0.0/16 10.2.0.1 — 10.2.255.254 10.2.255.255
10.100.0.0/24 10.100.0.1 — 10.100.0.254 10.100.0.255
10.101.0.0/24 10.101.0.1 — 10.101.0.254 10.101.0.255
10.255.255.0/24 10.255.255.1— 10.255.255.254 10.255.255.255 a


### Slides — strona 272

CIDR
CIDR Subnetting Example
Example
Network Portion Host Portion
IAT, —_ As an example, we will use the
11111111.11111111.111111111. 00000000 subnet 10.1.1.0/24. The subnet
must appear in binary on the
left side.
Network Portion Host Portion
SS SSS Creating two smaller sub-networks
11111111,11111111.11111111,1 0000000 can be done by “borrowing” a bit
from the host portion to the
* For one borrowed bit: 2sub-network bits = 21 = 2 ———
sub-networks
, After subnetting, the new address will
* For two borrowed bits: 2sub-network bits = 22 = 4 be 10.1.1.0/25. Each network address
sub-networks will be assigned 126 host addresses.
¢ Andso on...


### Slides — strona 273

CIDR

Subnets can borrow bits from any host bit to create additional masks. For each borrowed bit in the fourth octet, the number

of sub-networks is doubled, while the number of hosts per subnet is reduced. n = Network Portion, h = Host Portion

Subnets

Prefix Subnet Mask Mask in Binary Networks Hosts

nannnnnnn.nnnnnnnn.nnnnnnnn.nhhhhhhh 2 126

2s 288-255.255-128 11111111.11111111.11111111.10000000
nannnnnnn.nnnnnnnn.nnnnnnnn.nnhhhhhh 4 62

i ABaoaPoate2 11111111.11111111.11111111.11000000
nannnnnnn.nnnnnnnn.nannnnnnn.nnnhhhhh 8 30

[27 295.255.255.224 11111111.11111111.11111111.11100000
nnnnnnnn.nannnnnnn.nannnnnnn.nnnnhhhh 16 14

j28 295.255.255.240 11111111,71111111,11111111.11110000


### Slides — strona 274

CIDR
Case Study 1
Configuration Per Sub-Network
A network manager requests to extend the current network to an additional four sub-networks.
The given IP address and subnet mask is 172.16.0.0/24.
¢ How would we add four more networks?
¢ What are the new network addresses?
Network Address Usable IP Addresses Broadcast Address


### Slides — strona 275

CIDR
Case Study 1
Configuration Per Sub-Network
A network manager requests to extend the current network to an additional four sub-networks.
The given IP address and subnet mask is 172.16.0.0/24.
¢ Adding four networks: 24x = 4 ?, the answer is 2. That means we need to borrow two bits from
the subnet to create an additional four sub-networks.
¢« RED = new network portion, BLUE = new host portion: 11111111.11111111.11111111.11000000
¢ The new network addresses are: 172.16.0.0, 172.16.0.64, 172.16.0.128, 172.16.0.192
(| 2ase0 | 172.16.0.1-172.16.0.62 | - 172.16.0.62 | 172.16.0.63
The total number of
jump in the last octet:
246 = 64 addresses (


### Slides — strona 276

CIDR
Case Study 2
Configuration Per Sub-Network
A network manager requests to extend the current network by an additional five sub-
networks. The given IP address and subnet mask is 192.168.0.0/24.
* How would we add five more networks?
¢« What are the new network addresses?
Network Address Usable IP Addresses Broadcast Address


### Slides — strona 277

CIDR
Configuration Per Sub-Network
A network manager requests to extend the current network by an additional five sub-networks.
The given IP address and subnet mask is 192.168.0.0/24.
¢ Adding five networks is not possible, with the closest possible network division being 8.
¢ 24x = 8 ?, the answer is 3. That means we need to borrow three bits from the subnet to create an
additional eight sub-networks.
¢ RED = new network portion, BLUE = new host portion: 11111111.11111111.11111111.11100000
¢ The new network addresses are: 192.168.0.0, 192.168.0.32, 192.168.0.64, 192.168.0.96, and so on.
Note: The table below displays only the first four of eight subnets.
[/__ezston | aeesssosmssassenae | sszsconar
The total number of
jump in the last octet:


### Slides — strona 278

CIDR

Case Study 3

Network Configuration Per User
A network manager requests a 300-workstation expansion of the network. The workstations are to be
installed in a single broadcast domain. The correct given address is 10.0.0.0. The aim of the expansion is
to use as few resources as possible.
¢ How would we use the least amount of resources possible?
¢ What is the new network address, network range, and broadcast address?


### Slides — strona 279

CIDR
Case Study 3
Network Configuration Per User
A network manager requests a 300-workstation expansion of the network. The workstations are to be
installed in a single broadcast domain. The correct given address is 10.0.0.0. The aim of the expansion is to
use as few resources as possible.
* To use the least amount of resources possible, the matching subnet will be /23, because it allows the use
of 510 host addresses: 249 = 512, 512 — 2 (Minus Network address, Broadcast Address) = 510 hosts.
¢ RED =new network portion, BLUE = new host portion: 11111111.11111111.11111110.00000000
* The new network address will be 10.0.0.0/23
¢ The network range is 10.0.0.1/23 — 10.0.1.254/23
¢ The broadcast address is 10.0.1.255/23


### Slides — strona 280

Subnetting Concepts
VLSM


### Slides — strona 281

VLSM
VLSM Overview
VLSM
VLSM (Variable Length Subnet Mask) is a method by which a network is
subnetted, and the subnets are then subnetted further (when using only
ly lI CIDR, they are not subnetted further).
aaa: The process can be repeated several times to divide the subnets into
various sizes, to ensure that IP addresses are not wasted.
Formulas are applied to calculate the number of hosts and subnets.
&


### Slides — strona 282

VLSM
VLSM Subnetting Example
Example
10 O O O /8 As an example, we will start with
cu eee the network address 10.0.0.0/8.
This address is subnetted into 2
additional networks.
The subnetting process (CIDR)
10.0.0.0 /9 10. 128.0.0 /9 created the networks 10.0.0.0/9
/~ and 10.128.0.0/9.
aN After creating the networks, each
10.0.0.0/10 10.64.0.0/10 10.128.0.0/10 10.192.0.0/10 was subnetted (VLSM) to create
additional networks, similar to
a using CIDR.
10.0.0.0 /9 used to create 2 networks
) VLSM is useful when using CIDR
11111111.11000000.00000000.00000000 provides too many unused
» addresses for one network.
10.0.0.0 /10 and 10.64.0.0 /10 subnets are created is


### Slides — strona 283

VLSM
Lab NET-06-L1: Subnetting Practice
A Lab Mission Q— Steps
The aim of this lab is to provide review questions Subnetting questions
for all the material covered in the module, 7 F
Practice subnetting
including the topics of how to subnet networks
and assign IP addresses.
(ag Env. & Tools (5 Related Files
OS: All platforms Lab document
Tools: Calculator (optional)


### Slides — strona 284

VLSM
2 eee The aim of this lab is to provide review questions for all the
Su bn etti ng Pra ctice material covered in the module, including the topics of how
. | to subnet networks and assign IP addresses.
30-60 Min. |
oo . @ Subnetting questions
— 4 : ®@ Practice subnetting
a: =
" b NN ® e yr
| ‘ ‘Ss i) _ i 3 ® OS: All platforms @ Lab document
= 88 W ® Tools: Calculator
; ‘i } (optional)
| { ; 4 . s
if ’ . |


### Slides — strona 285

CO
Subnetting Concepts
NETWORK ADDRESS SCHEME DESIGN


### Slides — strona 286

Network Address Scheme Design
Network Planning
How to Plan a Network
A network needs to be well-designed. Addresses must not be assigned
= randomly!
Planning a network requires examination of how the organization is
structured, and how the subnets will be structured.
7 i i Planning addresses involves deciding how many hosts per subnet there will
be, how large each subnet will be, and how host addresses will be assigned.
E,
Knowing your address requirements will help determine the range of host addresses.


### Slides — strona 287

Network Address Scheme Design
Planning Considerations
Prevent Duplication
%. In. an inter-network structure, each host must have a unique address.
n Planning and documentation prevent the creation of duplicate addresses.
Access Control
_ If addresses are randomly assigned, servers that provide resources to internal and
external hosts will not be able to control access efficiently and effectively.
Monitor
7 o- —] Network traffic is examined for source IP addresses generated or received from
packets. With proper planning, finding problematic devices should be a simple
= process.


### Slides — strona 288

Network Address Scheme Design
ey Fi or?
ras ofo
Most networks use DHCP to In most networks, servers Routers and switches are A gateway is a packet-
dynamically assign must be made available to assigned IP addresses. forwarding device, and is
addresses, eliminating the remote users. The servers . tvpicallya fi lI t
need for network staff to do are assigned private Switches can be managed VPI Y it URES OF TOURED
so, and preventing entry internal addresses, and the remotely via the cloud. Each interface that serves as
errors. forwarding device will Routers are assigned IP a gateway for hosts in the
When the address scheme perform additional addresses because they network must be assigned
changes, the DHCP server ite ations:to public operate in Layer 3. an IP address.
must be reconfigured. addresses (NAT). call
Servers are typically Routers are typically
configured with static configured with static
addresses. addresses.


### Slides — strona 289

A :
,/, e ‘ sss 4
.. / = » 4, f
= wv 4 , , N \ ~~,
SSO : ’ a .
QUESTIONS? A ‘faa
7
% ’ *.
ag Pg rey y ik os - a a

: @a, Pe, y 4 nal


### Slides — strona 290

a i ™" : = a aw NETWORK ee Bal Ci = L D


# Chapter 7: IPv4 & IPv6 Static Routing


### Slides — strona 291

<a = —— :
: Cybersecurity Professional Program
IPv4 & IPv6
Static Routing
Computer Networking
Copyright © 1996-2020 HackerU Ltd. All Rights Reserved.


### Slides — strona 292

cae IData
Introduction Network Switch & IOS Switch Securit IP and Routing
to Networks Fundamentals Fundamentals y Concepts
Diagnostics and VLANs Dynamic IPv4 & IPv6 Subnetting
Troubleshooting and Trunk Routing Static Routing Concepts
Access Infrastructure Fiival Proiect
Control List Services d


### Slides — strona 293

IPv4 & IPv6 Static Routing
Overview
Lesson Objective
Router Operation
The objective of this lesson is to learn
about the static routing method and IPv4 Static Routing
how to configure it in IPv4 and IPv6.
IPv6 Static Routing
G


### Slides — strona 294

OO
IPv4 & IPv6 Static Routing
ROUTER OPERATION


### Slides — strona 295

Router Operation
Routing Review
How a Router Operates
=> One of the router’s main jobs is to select the best path for a packet.
<i _> The decision is based on its destination address.
After determining the best path on which to forward the packet, the
, router encapsulates the packet in a new frame in accordance with the
relevant outgoing interface.
6


### Slides — strona 296

Router Operation
Examination
In the first step, the router decides whether to
process a packet or ignore it. Routers will ignore ie Decapsulation
packets with errors, or packets they don't know The router examines the Layer 2 address to
how to process. decide if the packet was intended for itself (the
default gateway), and verifies the integrity of the
Decision-Making frame using the FCS (Layer 2 trailer).
The router decides where to forward the packet
to, based on its destination IP address and the San Encapsulation
routing table. The router re-encapsulates the packet with new
Layer 2 headers for the next hop (MAC address
of the next hop), according to the decision made
Forwarding 7 in step 3. a]
After a decision is made, the router forwards the
packet to the interface from which the packet
must exit.


### Slides — strona 297

Router Operation
Remote Networks
What is a Remote Network?
A router's best routing decision is based on its routing table. But where
does the routing table get its information from?
Networks connected directly are added to the table immediately, but a
remote network must be configured by the user.
A remote network is any network not connected locally to the router.
6
The ICMP message "Destination unreachable" is displayed whenever the router cannot find
a match for the path in its routing table.


### Slides — strona 298

Router Operation
Remote Network Learning
A remote network can be learned by a router in one of two ways: statically or dynamically.
Static Method
Using the static routing method, the user enters every network manually
ae in the routing table.
Dynamic Method
AUTO In the dynamic routing method, the router automatically learns the remote network
from the routing tables of adjacent routers, by using various protocols.


### Slides — strona 299

Router Operation
Advantages Disadvantages
A simple solution for small networks. Error-prone in large network environments.
Not advertised over the network, meaning better security. Does not support verification methods.
No CPU and memory usage for routing purposes. Configuration and maintenance are time-consuming.
Every path a packet takes is known, which improves network Regiiires complete knowledge of the'entire network.
traffic management.


### Slides — strona 300

Router Operation
When to Use Static Routing
Network administrators decide if and when to use Static Routing, based on network requirements.
Stub Networks
Static routing is a better choice when routing to and from stub networks.
ONE WAY Stub networks consist of a single router that sends and receives non-local traffic
via a single path.
Small Networks
a® Although Static Routing is simple and secure, and saves resources, it does not
ae) provide a sufficient level of scalability in larger networks.


### Slides — strona 301

OO
IPv4 & IPv6 Static Routing
IPV4 STATIC ROUTING


### Slides — strona 302

IPv4 Static Routing
Static Route Types
The following are the most common types of Static Route implementation.
Standard Static Route
g Manually configured route that forwards traffic to a specific network.
Default Static Route

Typically used as a Gateway of Last Resort, which is used for any packet that does not
have a destination route in the routing table. The destination in such cases is often set to
the Internet.


### Slides — strona 303

IPv4 Static Routing
Network Topology Illustration
A host on network A wants to
communicate with a host on
network B.
If no static or dynamic routing
is used, R1 does not know the
er
destination network and its |
direction. ea)
as
172.17.0.2 4]
— aay
For R1 to know network B, add R3 Net C 10.2.0.0/24
: ‘ Gig2/0_ 7 7
the network and direction to the —, Gigt/0 a,
routing table. Now, R1 will hi) eng Gigolo 172.16.0.2 ei |
forward network A host packets ——5 7
to the correct destination. L_—— ——
Net A 10.0.0.0/24 i & Net B 10.1.0.0/24
The same is required for R2 and
R3 to recognize network A.


### Slides — strona 304

Syntax Usage
_- Command , ji F 1 1
Router (config)# ip route <network-address> <subnet-mask> <direction>
| i 1 2 3
</>
Code Example
R1(config)#ip route 10.1.0.0
1. Specifies the remote network address. 255.255.255.0 172.16.0.2
2. Specifies the remote network subnet mask.
3. Sets the direction of the network, which can be:
Directly-connected - the local outgoing interface.
Next-hop - the IP address of the interconnected router.


### Slides — strona 305

The'example‘on the rightis'a R1(config)#ip route 10.1.0.@ 255.255.255.@ 172.16.0.2
static route configuration
example, based on the R1(config)#ip route 10.2.0.@ 255.255.255.@ gigabitEthernet 1/0
topology in the previous slide. *#Default route without gateway, if not a point-to-point interface,
may impact performance
The command is used to
add a new network route to the R1(config)#do show ip route
routing table. 10.0.0.0/24 is subnetted, 2 subnets
Verify the addition of static routes
by displaying the routing table C 172.16.0.0/16 is directly connected, GigabitEthernet@/a
using the command. Cc 172.17.0.0/16 is directly connected, GigabitEthernet1/@
C 172.18.0.0/16 is directly connected, GigabitEthernet2/0
Note: The next-hop and directly-
connected options are also known
as recursive and directly-attached
routes.


### Slides — strona 306

R1(config)#ip route 0.0.0.0 0.0.0.0 gigabitEthernet 2/0

The default and standard

pects diss taeenenn R1(config)#do show ip route

routes use the same syntax,

except for one difference: 10.0.0.0/24 is subnetted, 2 subnets

The défault:routeuses S 10.1.0.0 [1/0] via 172.16.0.2

to represent any network S 10.2.0.0 is directly connected, GigabitEthernet1/0

address with any subnet mask. C 172.16.0.0/16 is directly connected, GigabitEthernet@/oe
C 172.17.0.0/16 is directly connected, GigabitEthernet1/0

- C 172.18.0.0/16 is directly connected, GigabitEthernet2/0

A default route can be set with a

next-hop or outgoing interface.

The standard route is denoted by S,

while the default is denoted by S*.


### Slides — strona 307

Administrative Distance
Administrative Distance

an Oy) Administrative Distance (AD) is a predefined value for each routing method.

The router selects the path of the lowest AD value in the routing table.

a) For example, if there are two routes to the same destination network, one
==, via OSPF (a dynamic routing protocol) and the other a static route, the
<3) router will select the static route (1 vs. 110).

e


### Slides — strona 308

IPv4 Static Routing
Default AD Values

Method/Protocol AD Value
Directly-connected (6)
Static Route 1
Internal EIGRP 90
OSPF 110
RIP 120


### Slides — strona 309

IPv4 Static Routing
Floating Static Route Summary Static Route
Gr
Provides backup paths to To reduce the number of Similar to standard route,
primary static routes for routing table entries, but instead of configuring a
situations in which a link multiple static routes can be network, it is used to
failure occurs. This route summarized to a single forward traffic to a specific
type is only used when the address. host.
Primary route Is not It uses a default mask of
available. 255.255.255.255
The AD for floating static
routes is higher than the
AD for primary routes.


### Slides — strona 310

ip route <network-address> <subnet-mask> <direction> <AD>
The code on the right is an
example of a primary and Ri(config)#ip route 192.168.1.0 255.255.255.0 172.16.0.2
backup route configuration. R1(config)#ip route 192.168.1.@ 255.255.255.@ 10.0.0.2
The primary route is set with a R1(config)#do show ip route
default AD (1). Cc 10.0.0.0/3@ is directly connected, GigabitEthernet@/1
- Cc 172.16.0.0/30 is directly connected, GigabitEthernete/oe
ihe backtip dear ae S 192.168.1.0/24 [1/0] via 172.16.0.2
the same networ utTtroma .
Hifferentdirectionvand isset 5 192.168.1.0/24 [°/@] via 10.0.0.2
with a higher AD (5).
Note: The backup route will
be shown only if the primary
route fails.


### Slides — strona 311

ip route <ip-address> 255.255.255.255 <direction>
Although this type of static R1(config)#ip route 192.168.1.5 255.255.255.255 172.16.0.2
route is not very common, it
B és s Cc 10.0.0.0/30 is directly connected, GigabitEthernete/1
such as a server. :

Ss 192.168.1.5/32 [1/0] via 172.16.0.2

This method may be useful for
special routing requirements.


### Slides — strona 312

IPv4 Static Routing
Network Topology Illustration

Contiguous:
To summarize the network to a
single address, the destination ==»
networks need to be
contiguous. eg 10.0.0.0/30 as) 172.10.0.0/16 ee 472.11.0.0/16

Same Routing Path: =

All networks use the same i Re RS

outgoing interface or next-hop

address.

172.13.0.0/16
172.12.0.0/16
In this example, instead of four Bese
standard static routes, a single
summarized static route is R4
used, as shown in the next
slide.
EA


### Slides — strona 313

IPv4 Static Routing
Summarizing Steps
Convert IP to Binary
172.10.0.0 — 10101100.00001010.00000000.00000000
172.11.0.0 — 10101100.00001011.00000000.00000000
172.12.0.0 — 10101100.00001100.00000000.00000000
172.13.0.0 — 10101100.00001101.00000000.00000000 Compare the Identical Bits
~ H 172.10.0.0 — 10101100.00001010.00000000.00000000
172.11.0.0 — 10101100.00001011.00000000.00000000
172.12.0.0 — 10101100.00001100.00000000.00000000
Create a Summarized Address 172.13.0.0 — 10101100.00001101.00000000.00000000
Network Address :
172.8.0.0 - 10101100.00001000.00000000.00000000
Subnet Mask:
255.248.0.0 - 11111111.11111000.00000000.00000000


### Slides — strona 314

ip route <summarize-address> <summarize-mask> <direction>

R1(config)#ip route 172.8.0.@ 255.248.0.0 10.0.0.1
R1(config)#do show ip route

The exaniple:sn the C 10.0.0.0/24 is directly connected, GigabitEthernet0/e

right shows the code for

summarizing and

verifying the new route.

Note the prefix 13.


### Slides — strona 315

IPv4: Static Routing
EFS Se The objective of this exercise is to implement IPv4 standard
Configuring IPv4 Static and Default Routes and default static routes in a full network topology.
30-60 Min.
~ wr r yA , . Configure IPv4 Standard Route
. ’ ‘ « ; ® Configure IPv4 Default Routes
>. q 4 = ® Configure IPv4 Summary Route
| —an ® 8 OS: All platforms © Lab document
: ® Tools: Cisco Packet Tracer ® NET-07-L1.pka
. y) 7.2.2 or higher
*
. _——
i ‘ a


### Slides — strona 316

OO
IPv4 & IPv6 Static Routing
IPV6 STATIC ROUTING


### Slides — strona 317

IPv6 Static Routes
IPv6 Static Route Types
(IP) Static routing is similar for IPv4 and IPv6, with the exception of how the
destination network addresses are formatted.
se \: IPv6 supports the same static routing types, and most of the parameters
4h an are identical to those in IPv4 commands.
B


### Slides — strona 318

IPv6 Prerequisites
What’s Required for IPv6 Static Routing?
N = IPv6 packet forwarding must be enabled on the Cisco router.
= Command: IPv6 unicast-routing
fi) = The interface must be enabled and configured with an IPv6
address.
é


### Slides — strona 319

Syntax Usage
— Command , , ' ' H
i Router(config)# | ipv6é route i <network-address> i / <prefix> | <direction> !
| ! 2 3
</>
Code Example
1. Specifies the IPv6 remote network address. Ba (cant te) #Tpvo scouts .
2001: abcd: cafe::/64 serial
2. Specifies the remote network prefix. e/e/e
3. Sets the direction of the network, which can be:
Directly-connected - the local outgoing interface.
Next-hop - the |Pv6 link-local or global-unicast address of the
interconnected router.


### Slides — strona 320

R1(config)#ipv6 route 2001:abcd:cafe::/64 2002:abcd:aaaa::1
R1(config)#ipv6é route serial 0/0/0
The code on the right includes R1(config)#ipv6 route 2001:abcd:cafe:: gigabitethernet0/e
examples of all types of IPv6
static routes: Ri(config)#ipv6 route 2001:abcd:cafe::/64 gigabitetherneto/o
* Standard (next-hop)
* Default (directly-connected)
* Summary
¢ Floating


### Slides — strona 321

R1(config)#do show ipv6 route
Ss 2001:ABCD:CAFE::/64 [1/0]
via 2002:ABCD:AAAA: :1
; S ::/@ [1/0]
displays and via serial 0/e/@

verifies the IPv6 routing table.

Remember not to use

(displays IPv4 routing table),

but rather


### Slides — strona 322

; ¢ 4 im Z f
se “ =) > Be 4

vl om ES \ . 7! >
So ~ Ww =
CDOS \ —

CTE > <=

SRS 2 SS

oe CSS i. > fo

SS \ ke sug ie

Bo PLO i Sy

* ‘ 4 Crs = f


### Slides — strona 323

aul egal 5 i 2B
—— — Sy " : ™ ty .
ie. = 4 a wet, NETWORK ga Cm D


# Chapter 8: Dynamic Routing


### Slides — strona 324

—" ‘Cybersecurity Professional Program
— — rg Stoeeanemo™ mae p oe :
E Dynamic Routing
Computer Networking


### Slides — strona 325

Computer Networking

Introduction Network Switch & IOS Switch Securit IP and Routing

to Networks Fundamentals Fundamentals y Concepts
Diagnostics and VLANs Dynamic IPv4 & IPv6é Subnetting
Troubleshooting and Trunk Routing Static Routing Concepts

Access Infrastructure Fiival Proiect
Control List Services d
2


### Slides — strona 326

Dynamic Routing
Overview
Lesson Objective
; ; ; Dynamic Routing Concepts

This lesson covers dynamic routing concepts

and protocols, including RIPv2 and OSPFv2.

It also explains processes, algorithms, and RIPv2

messages used to exchange routing

information.

OSPFv2
G
3


### Slides — strona 327

OO
Dynamic Routing
DYNAMIC ROUTING CONCEPTS


### Slides — strona 328

Overview

What is Dynamic Routing?

Dynamic routing protocols have been in use since the late 1980s.

4 he purpose of these protocols is to map networks and update routing
tables with the shortest routes, in a fully automatic and independent

Wy manner.

i The method is made possible by special algorithms and protocol
packets.

e


### Slides — strona 329




### Slides — strona 330

Dynamic Routing Concepts
Routing Source Codes
S — Indicates that the D — Indicates that the O - Indicates that the R — Indicates that the
route was manually route was learned route was learned route was learned
created by an dynamically from dynamically from dynamically from
administrator to reach a another router using the another router using the another router using the
specific network. EIGRP routing protocol OSPF routing protocol. RIP routing protocol.
(which will not be
covered during this
course).


### Slides — strona 331

Key Elements
Fits Any Topology
Once the protocols are activated, the routers begin “talking” to each other,
and map the network topologies themselves.
Fast and Independent
Dynamic Routing is based on software that can gather a lot of information in a short
on time and input it to an algorithm that computes the information to find the fastest
route to each network.
Awareness
Each Dynamic Routing protocol uses Timers that detect any change in the topology,
( such as a connection failure. When a change is detected and involves a network
() failure, the protocols will search for an alternate path.


### Slides — strona 332

Dynamic Routing Concepts
Administrative Distance (AD) Values
Default AD Values

Method/Protocol AD

Directly Connected (6)

Static Route 1

Internal EIGRP 90

OSPF 110

RIP 120

EEE


### Slides — strona 333

Metrics
What is a Metric?

A metric is a measurable value assigned by the routing protocol to
different routes based on the usefulness of the route.

® | | l When there are multiple paths to a remote network in the same

= = protocol, routing metrics are used to determine the overall

[== “length” of a path from source to destination.
Routing protocols determine the best path based on the route
with the lowest metric value.

e


### Slides — strona 334

Dynamic Routing Concepts
Routing Protocol Metrics
Routing Information Protocol Hep Count Matas Exanpls
The RIP hop count metric will choose the path
with the least amount of hops, where hops refer Route A is shorter
ye to routers. than Route B
@ Src Network Route A Dst Network
Open Shortest Path First = > =)
" The OSPF metric is based on cumulative R1 = ==
aS bandwidth from source to destination. OSPF will \es_ es
Ag” choose the path with the highest bandwidth. Route B
G


### Slides — strona 335

Dynamic Routing Concepts
IGP Vs EGP Protocol Classification Map
Interior Gateway Protocols are routing protocols used within an
Autonomous System (AS), such as company routers. ice | EP
Exterior Gateway Protocols are used to map routes between AS’s,
and are mainly used by ISPs. a
Distance Vector Vs Link-State [Distance Vector | | _ Link State
The fundamental difference between distance vector and link-state
routing protocols, is how the protocols discover the topology and RIP } { EIGRP [iss | | OSPF | BGP
the way they share routing information with the routers.
G
BGP is classified as a Path Vector protocol and is used to map the Internet.


### Slides — strona 336

Dynamic Routing Concepts
Distance Vector
Distance Vector
RS Distance Vector is a routing algorithm that calculates the best path for a packet
7
SX based on the factors of Distance and Vector.
WMA
Distance
0) Distance — The distance between the router and the destination network, based
©) 77 onthe metric of number of hops (routers).
Vector
Vector — The outgoing interface and the direction to the path that leads to the
destination network.


### Slides — strona 337

Dynamic Routing Concepts
Link State
Link State
Gu Link State routing protocols include complete network topology maps.
Network Map
8 The map is created based on information gathered from all routers on the network.
e=y,
Network Changes
vN Link State routing protocols do not broadcast information regularly.
WA Updates are only sent when a change occurs on the network.


### Slides — strona 338

Dynamic Routing Concepts
Passive Interface
Passive Interface Feature
Passive interface is a feature used in all routing protocols. Its purpose
is to disable routing updates on specific interfaces, which decreases
resource usage and increases security.
The command syntax is the same in all routing protocols.
It is typically placed on interfaces facing the LAN.
Passive interfaces should not be configured between routers.


### Slides — strona 339

Dynamic Routing Concepts

(Q

IO Ek®
Dynamic routing updates Devices in the same LAN Packet sniffing software can
consume bandwidth must process updates up to be used to intercept packets
because messages are sent Layer 4 (transport layer), that include routing
in broadcast or multicast, and only then discard the updates, and redirect traffic
causing switches to update. by corrupting the routing
broadcast to all ports. table with false metrics.


### Slides — strona 340

Dynamic Routing Concepts
Classful :
Classful routing protocols provide routing updates os .
according to classful network addresses (A, B, C). For
example, the route for 10.15.30.2/11 and 10.80.0.15/11
will be advertised as 10.0.0.0 even if it is subnetted. .
Classless 3 :
Classless routing protocols provide routing updates —_
according to VLSM addresses and does not follow only
classful addresses. For example, the route for
10.80.30.2/11 will be advertised as 10.64.0.0/11 classtillirantingpravaaals
RIPv1, IGRP
Classless routing protocols:
RIPv2, EIGRP, OSPF, IS-IS
by


### Slides — strona 341

Dynamic Routing
RIPV2


### Slides — strona 342

RIPv2
RIP Overview
Routing Information Protocol
RIPv1 was released in 1988 and is one of the oldest routing protocols.
It is a distance-vector protocol, and its metric method is hop count.
The protocol has limitations, such as the maximum allowed hops for a
route, which is 15. Due to its limitations, it is often implemented only in
small networks that do not require a high level of scalability.
Unlike other protocols, RIP operates in Layer 7 (OSI) and uses port 520
(UDP).
B
There are three versions of the protocol. RIPv2 is the most widely used, but is not the most
popular, due to its inherent limitations.


### Slides — strona 343

RIPv2
RIPv1 RIPv2 RIPng
Released in 1988 Released in 1993 Released in 1997
Classful routing protocol Classless routing protocol ---
Doesn’t support VLSM and CIDR Supports VLSM and CIDR Supports IPv6
Hop-count metric Hop-count metric Hop-count metric
Doesn't include subnet mask in Includes subnet mask in routing Includes subnet mask in routing
routing updates updates updates
Routing updates are sent in broadcast Routing updates are sent in multicast Routing updates are sent in multicast
(255.255.255.255) (224.0.0.9) (ff02::9)
5 ow. co. Supports IPv6 inherent IPsec
Doesn’t support authentication Supports authentication
authentication

Sends full routing updates Sends full routing updates Sends full routing updates

Bi SB Bi


### Slides — strona 344

RIPv2
RIP Parameters
Administrative Distance
| AD | RIP’s default AD value is 120.
i] The value can be modified, but it is not recommended to do so.
Metric
fix) RIP determines the shortest route to a network by the number of hops (routers) to the
La target network. The route with the least amount of hops is added to the routing table.
=H RIP supports routes of up to 15 hops.


### Slides — strona 345

RIPv2
eee eee ee
(2 e®.
Kc) “eae
@,e
By default, the update value Invalid is also known as an If a route is invalid after 180 The default value is 180
is 30 seconds, and messages expiration timer, and by seconds, it will remain in the seconds.
will be broadcast/multicast default its value is 180 routing table for an additional . oo
ona RIP-enabled interface. seconds, after which the 60 seconds before it is During this time, the router
Example: Two routing entry will indicate removed, and inform its on vi accept new updates
interconnected neighbor destination is unreachable. neighbors of its status. or the route.
routers send each other Example: If a router does
updates every 30 seconds, not receive an update from Total: 180+60=240
even if there is no change in its neighbor within 180
the topology. seconds, it will set the
route’s hop count to 16
(destination is unreachable).


### Slides — strona 346

RIPv2
Auto-Summary
Auto-Summarization Feature
| Auto Summary is a feature that allows automatic summarization of
routes to their classful networks. This allows multiple networks to be
= § @==== represented with a single summary address.
as = = By default, RIP and EIGRP summarize subnets exceeding the classful
4 hs boundaries to a major classful network address in the routing
updates.
6
This feature is often disabled because most address schemes in networks today do not allow
address summaries without compromising communication.


### Slides — strona 347

RIPv2
Network Illustration
Networks A, B, and C cannot reach
each other because their routers do —=,
not ‘know’ each other yet. ee) Gigo/0 |
SS
Once RIP is enabled on all 0/010 So/0/1 =
routers, they will start to share R2 Net B 192.168.20.0/2
routing information. 172.16.0.0/30 172.16.0.4/30
Next, each router will add
remote networks to its table.
R1 will add Nets B and C, for =e, S0/0/0 SOO =,
example. = Gigo/o aoe 00/1 $0i0/1 Gigol0 wl
— 172.16.0.8/30 a7
This process is called — ——
convergence. Net A 192.168.10.0/24 Re BS Net C 192.168.30.0/2
Every router can reach
any network.


### Slides — strona 348

R1(config)#router rip
enables RIP and R1(config-router)#version 2
enters RIP configuration mode. R2(config-router)#no auto-summary
R1(config-router)#network 192.168.10.@
R1(config-router)#network 172.16.0.0
sets the RIP version. R1(config-router)#network 172.16.0.8
R1(config-router)#passive-interface gigabitEthernet 0/0
advertises the network
and enables RIP updates on the R2(config)#router rip
hetworkintertace. R2(config-router)#version 2
R2(config-router)#no auto-summary
disables the auto- R2(config-router)#network 192.168.20.0
summary feature. R2(config-router)#network 172.16.0.0
disables RIP R2(config-router)#network 172.16.0.4
updates on the interface. R2(config-router)#passive-interface gigabitEthernet 0/0


### Slides — strona 349

Ri#show ip route
Theeinple ontherietit 172.16.0.0/16 is variably subnetted, 5 subnets, 2 masks
shows R1’s routing table after C 172.16.0.0/30 is directly connected, Serial@/e/e
RIP finished updating it. L 172.16.0.1/32 is directly connected, Seriale@/e/e
represents the route learned
by the RIP protocol.
C 172.16.0.8/30 is directly connected, Serial@/0/1
. . : L 172.16.0.9/32 is directly connected, Serial@/@/1
An important feature is that if . .
the router finds two equal paths 192.168.10.0/24 is variably subnetted, 2 subnets, 2 masks
to the network, both routes are Cc 192.168.10.0/24 is directly connected, GigabitEthernet0/0e
added to the table, and load L 192.168.10.254/32 is directly connected, GigabitEthernet@/e
balancing is applied.
For example,


### Slides — strona 350




### Slides — strona 351

Ri#show ip protocols
. Routing Protocol is "rip"
displays the
current protocol settings.
This Is'valid forevery dynamic Redistributing: rip
routing configuration, such as
OSPF. Interface Send Recv Triggered RIP Key-chain
Serial0/0/0 2 2
Serial0/0/1 2 2
The output includes:
* Timer information Maximum path: 4
* Advertised networks
* Passive interfaces
* More
Routing Information Sources:
Gateway Distance Last Update
Distance: (default is 120)


### Slides — strona 352

Routing Table Entry
: Command
R 192.168.20.0/24'[120/1]i via 172.16.0.5, '00:00:09,!Serial@/e/e ' |
toad 2 3 4 5 6
; : : : : </>
Show IP Route Output
1. Rout Ril#show ip route
# ROULS'SOULCe: R 192.168.20.0/24 [120/1] via

2. The destination network address and prefix. 172.16.0.5, 00:00:09, Seriale/0/a

3. The AD and metric of the route.

4. Next-hop address through which the packet passes to the target

network.
5. The route age (timestamp).
6. The local outgoing interface that points to the target network.


### Slides — strona 353

Static Default Route Code Example
The static default route redirects packets with unknown R1(config)#ip route 0.0.0.0
destinations to the Gateway of Last Resort, which is a Bolelt@) (nye (Oa
eee ee ea uriicee je a specific direction Ri (config #eouter Cip
{typically to the (Internet). V4 R1(config-router)#
Propagating Default Routes
R2(config)#do show ip route
E) Each routing protocol shares its default routes with all @.0.0.0/@ [120/1] via
& wy routers on the network, through protocol updates. 192.168.12.1, 00:00:26, Gig 0/1
Bea
G eal


### Slides — strona 354

RIPv2
The objective of this lab is to implement and verify dynamic routing
an tei, Ae an PP. using RIP. The RIP protocol is straightforward, and can help
Configu ring and Verifying RIPv2 | understand basic network routing. RIP is no longer commonly in use
30-60 Min. today.
oe ¢ : ® Configure RIPv2.
— 4 : @ Propagate a default route.
Ja =
i b NY s e yr
ce ee | ; wa
| nN ‘Ss ® - * ®@ OS: All platforms ®@ Lab document
ss 8 W ® Tools: Cisco Packet Tracer @ NET-08-L1.pka
; } 7.2.2
{ ‘ ‘,
* |


### Slides — strona 355

OO
Dynamic Routing
OSPFV2


### Slides — strona 356

OSPFv2
OSPF Overview
Open Shortest Path First
@ OSPF is a Link State routing protocol introduced in 1989, with more
advanced features, making it a strong and scalable solution for any
° size network. OSPF was designed as an alternative to RIP.
bad OSPFv2 was released in 1991 and is still in use today.
@
OSPFv3 was developed for IPv6 in 1997.
e


### Slides — strona 357

OSPFv2
Topology Changes and Timers
Monitor the Network
0 OSPFv2 keeps track of changes in the topology, such as when a new network is
B4 added, ora link fails.
Hello
Hello Intervals — “Hello” packets are sent every 10 seconds to all OSPF-enabled
routers.
Dead
ed Dead Intervals — When a router does not receive a “hello” packet from its neighbor
: within 40 seconds, it will consider that neighbor “dead”, and will start looking for
alternative routes.


### Slides — strona 358

OSPFv2
Routers use Link Link State Database When an adjacency is If a router notices Link State Update
State Advertisement stores received LSA initialized, OSPFv2 that parts of its messages are
to advertise the packets, after the exchanges Database topological database responses to LSR
routing topology to routers enable Description packets are outdated, it will messages.
all other local routers OSPFv2 to use the to describe the send a Link State (SUs aresentin
in the same OSPFv2 SPF algorithm to content of the Request to a unicast.
area. calculate the routes. topological database. neighbor for more
LSAs are sent in updated versions of
multicast. those components.
LSRs are sent in
multicast.


### Slides — strona 359

OSPFv2
SPF Algorithm and Tree
Dijkstra
By calculating all routes to each network in the topology using the
Dijkstra Algorithm, OSPFv2 creates a map of the network called an SPF
Tree.
The SPF Tree is stored in a database on the router called a Link State
Database (LSDB).
e


### Slides — strona 360

OSPFv2
OSPF Metric
Best Route Determination mest Calkulation
x OSPF bases its metric calculation on the bandwidth Reference Speed (Mbps):
of the links along the path to the destination. 1000
@ _ Link Cost:
Cost 10
Wi All bandwidth information recorded for the route is Interface Speed (Mbps):
==] calculated using the OSPF formula (all considerations 100
=©5] are summed), resulting in the cost value.
G
The default reference speed is 100 Mbps, and can be adjusted using the auto-cost command.


### Slides — strona 361

Wildcard Masks
Mask Inversion
| Wildcard masks are used in some routing protocols, such as OSPF, as
a inverted subnet masks.
01 ae
0110 re } For example, the subnet 255.255.255.0 inverts to a wildcard mask of
0001
ood 0.0.0.255.
e


### Slides — strona 362

Router ID Configuration
Router ID -
When OSPFv2 is enabled on an interface, the router R1(config)#router ospf 1
must determine if there is another OSPFv2 neighbor on R1(config-router )#router-id
the link. Router IDs are set manually and used to ;
uniquely identify each router. R2(config)#router ospf 1
a R2(config-router)#router-id
First Fallback R3(config)#router ospf 1
‘x If no router ID is configured, the highest IP address of R3(config-router)#router-id
any router Loopback Interface is selected as the router
ID.
Go </>
Second Fallback [|
y If no Loopback Interface is configured, the highest IP
(x) address among its active interfaces is selected as the
(v) OSPFv2 router ID.


### Slides — strona 363

OSPFv2 Areas
What is an Area?
| fy OSPF uses a concept called Areas. A single AS or full topology can be
| im | divided into smaller areas.
| iat Dividing the topology into areas reduces router resource consumption
HMM sand protocol response time.
e


### Slides — strona 364

OSPFv2
Single-Area OSPF Area Illustration
For small to medium size networks that use a single
area, the default OSPFv2 is Area 0. The maximum
recommended area is 50 routers.
Ca — an)
ABR
Multi-Area OSPF > 2c =
=a —Ce aw aa
In larger networks that require more areas, Area 0 will Area 1 Area 0 Area 51
be the backbone area, and all routers outside that area
| | | | will be assigned other unique numbers (1, 2, 3, etc.).
GO
Routing between areas is done by an ABR (Area Border Router).


### Slides — strona 365

OSPFv2
Advantages Disadvantages
Smaller database (LSDB) for each area, saves memory. CPU utilization is high due to the amount of SPF calculations.
Smaller routing table for each area, saves resources. OSPFv2 requires all areas to be connected to the backbone.
Less traffic on the network due to less exchange of routing
information among routers.
Reduced algorithm calculation, only within areas.
In smaller areas, updates regarding changes in the topology
are distributed faster.


### Slides — strona 366

OSPFv2
Network Illustration
Networks A, B, and C cannot
reach each other, because the
routers do not ‘know’ each a
other yet. ee Gigd/0 |
—_«"
Once OSPF is enabled on all S0/0/0 RO SOO —
routers, they will start to share Net B 192.168.20.0/2
routing information. 172.16.0.0/30 172.16.0.4/30
Next, each router adds remote
networks to its table. For So/o/o So/o/0
example, R1 will add Nets B . .
endt’@. = Gigo/0 roe eon s0/0/1 soot eo Gigolo (__}
ef Sf
i———(4 172.16.0.8/30 Ew =
This process is called ar, ae R1 R3 = =i
convergence. Net A 192.168.10.0/24 Net C 192.168.30.0/2
Any router can reach any
network.


### Slides — strona 367

enables OSPF and R1(config)#router ospf 1
enters OSPF contiguration mode: R1(config-router)#router-id 1.1.1.1
router ig sets the TOMTEPOSEF R1(config-router)#network 192.168.10.@ @.0.0.255 area @
R1(config-router)#network 172.16.0.0 0.0.0.3 area @
R1(config-router)#network 172.16.0.8 0.0.0.3 area @
advertises the network R1(config-router)#auto-cost reference-bandwidth 10@0
ant Stables OS8e Updates elythe R1(config-router)#passive-interface gigabitethernet 0/0
network interface.
sets the interface area ID. R1(config-router )#
cetsthe veferenee @0:29:39: %OSPF-5-ADJCHG: Process 1, Nbr 2.2.2.2 on Serial@/0/e from
bandwidth calculation LOADING to FULL, Loading Done
disables OSPF @@:29:59: %OSPF-5-ADJCHG: Process 1, Nbr 3.3.3.3 on Serial@/@/1 from
updates on the interface. LOADING to FULL, Loading Done
Al indi : Please ensure reference bandwidth is consistent across all routers
og message indicates a link to
another OSPF-enabled router.


### Slides — strona 368

Ri#show ip route

The example on the right shows

faieieme 172.16.0.0/16 is variably subnetted, 5 subnets, 2 masks

inisnec upcanng tt. C 172.16.0.@/3@ is directly connected, Seriale/e/e

represents the route learned . . .
by the OSPF protocol. L 172.16.0.1/32 is directly connected, Seriale@/0e/e
An Pe ml eos a C 172.16.@.8/3@ is directly connected, Serial@/0/1
routing Is that i the router finds L 172.16.0.9/32 is directly connected, Serial@/@/1
two equal paths to the network, ; i
bath reuteswill be added tthe 192.168.10.0/24 is variably subnetted, 2 subnets, 2 masks
ing wi . .10. is direc connecte igabi erne

table, and load balancing will be Cc 192.168.10.0/24 is di tly ted, GigabitEth te/e@
applied. 0 .10. is direc connecte igabi erne
pp L 192.168.10.254/32 is directly ted, GigabitEthernete/o
For example,


### Slides — strona 369

Ri#show ip protocols
displays the Outgoing update filter list for all interfaces is not set
current protocol settings. Incoming update filter list for all interfaces is not set
The output includes: Number of areas in this router is 1. 1 normal @ stub @ nssa
* Router ID Maximum path: 4
* Area and process ID
* Advertised networks
* Passive interfaces
* More
displays Routing Information Sources:
timer information.
displays
adjacent OSPF-enabled routers.
Distance: (default is 110)


### Slides — strona 370

OSPFv2
Se Configuring routers to use OSPF with best practices in mind.
Configuring and Verifying OSPFv2
30-60 Min. at \\
gt —lrh f ® Configure OSPF.
; ‘ 2 «€ ; ® Propagate a default route.
_ j cc 5 i =
Se eS
} j
| iY ® 4 ® Os: All platforms ® Lab document
“ig |) ® Tools: Cisco Packet Tracer & NET-08-L2.pka
" y} 7.2.2 or later
|
‘ |
} i % SS — |


### Slides — strona 371

- / : . ee 7 ; 2 = :
‘ 7
= eat ¥ oat / “s
al = g \ . =
i VSso, ~ =
Fees \ 2 —
COTTE & ~
POPE » * a
{ > CAINS ~ 0 ee
J PORE " Fe
COV OSS > &
H 2 ~~ a ———.
i CU i ™
Me, "a », y 4, Fees
Sh SOS jj .
“ : ay Wage, y eS /
( ep y t /
~~" 2 CS — be a!


### Slides — strona 372

ok
aul egal 5 i 2B
— _ = : ste a) :
ie. = 4 a wet NETWORK Sr cay Cm D


### Slides — strona 373

Sir Cy bersacu ity Professional Program
Computer Networking


# Chapter 9: VLANs & Trunk


### Slides — strona 374

Computer Networking
Introduction Network Switch & IOS Switch Securit IP and Routing
to Networks Fundamentals Fundamentals y Concepts
Diagnostics and VLANs Dynamic IPv4 & IPv6é Subnetting
Troubleshooting and Trunk Routing Static Routing Concepts
Access Infrastructure Fiival Proiect
Control List Services d
2


### Slides — strona 375

VLANs & Trunk
Overview
Lesson Objective
Virtual LANs

The objective of this lesson is to learn how

to manage Virtual LANs (VLANs) and about

the impact they have on modern networks. Trunk Protocols

It also covers trunk protocols and the VLAN

Paging PIOCEss. Inter-VLAN Routing

G
3


### Slides — strona 376

CO
VLANs & Trunk
VIRTUAL LANS


### Slides — strona 377

Virtual LANs
VLANs
Virtual Local Area Networks
VLAN is acommon concept and practice among network administrators.
@-B Most networks today implement VLANs in one way or another.
VLAN is a Layer 2 feature that allows virtual network segmentation,
1 meaning dividing a physical network into separate logical networks.
GJ GJ Each logical network is a VLAN and represents a separate broadcast
domain.
B
The same rules that govern LANs also apply to VLANs.
5


### Slides — strona 378

Virtual LANs
VLANs
How do VLANs work?
Multiple ports are configured on the switch and associated with a
VLAN, creating a logical barrier between end devices connected to
the switch.
This enables network administrators to create several Virtual LANs
ona single switch.
VLANs are logical, not physical, divisions.
Transferring data between VLANs requires a router or other Layer 3 device.
6


### Slides — strona 379

Virtual LANs
Benefits of using VLANs
Improved Security
VLANs help separate and isolate sensitive user data, and reduce the chance
of spreading malicious data and unauthorized user access via network traffic.
Enhanced Performance
we VLANs reduce the size of broadcast domains, enhance performance, and
GF minimize unnecessary traffic on the network.
Simplified Management
e2 ra} VLANs allow administrators to group end devices and users by departments (such as
, 2 by job roles) rather than by physical location. This improves network policy flexibility
and reduces network costs.
7


### Slides — strona 380

Virtual LANs
i ?

What is a VLAN ID? When traffic passes through a VLAN, it must be identified to keep it
separate from traffic in other VLANs. A unique ID identifies a VLAN in
the network.

There is complete separation between virtual networks, whereby
users on VLAN 10 cannot access user data on VLAN 20.
=o On Cisco devices, the valid ID range for VLANs is 1 to 1005. There is
also an additional extended range of valid VLAN IDs from 1006 to
4094. a
B
The extended range of VLAN IDs from 1006 to 4094 is primarily
used in large networks, such as an ISP network.
8


### Slides — strona 381

Virtual LANs
Default VLAN Data VLAN Voice VLAN Management VLAN Native VLAN
comes aia ) Qe g
ae

Z L@ |
VLANs 1 and 1002- VLANs 2-1001 are This type of VLAN is Interface VLAN 1 is a Native VLANs are
1005 are reserved commonly used for designed for VoIP management VLAN designed to forward
and added data exchanges. (Voice over IP) used for SVI. untagged traffic, such
automatically during Their main function is network traffic. Management VLANs as DTP and CDP,
device installation. to tag data traffic enablevremote among switches. By
These VLANs cannot with an identifier. connection and default, MELON 1 ista
be removed or conduct basic native and
renamed. network functions. management VLAN.

9


### Slides — strona 382

show vlan brief
S1#show vlan brief
The command shows that the
switch is already pre-configured VMAS Neti SASGTEUE POIneS
with VLAN 1, and all ports are nn
associated with it by default.
Additional VLANs are available
in the switch configuration.
They are reserved and known
as default VLANs. . .
1002 fddi-default active
1003 token-ring-default active
1004 fddinet-default active
1005 trnet-default active


### Slides — strona 383

Virtual LANs
Switchport Modes
Access
Access ports carry traffic only on the VLAN to which they belong. Access mode
> should only be defined on ports connected to end devices, such as PCs.
As a security-related best practice, it is highly recommended to enable Access
mode for a port, before assigning it to a VLAN.
Trunk
‘~. Trunk ports carry traffic for different VLANs and devices. The port sets unique
Bays identifier tags on the frame, using either the 802.1Q or ISL encapsulation protocols.
This ensures that each frame is directed to its intended VLAN.
11


### Slides — strona 384

vlan <id>
name <word>
The example on the right shows S1(config)#vlan 100
VLAN 100 and 200 creation, whereby S1(config-vlan)#name class A
a valid ID is any number between S1(config-vlan)#exit
2 and 1001 (1, 1002-1005 are
ossunledh: S1(config)#vlan 200
S1(config-vlan)#name class B
It is recommended to assign an $1(config-vlan)#exit
appropriate to the VLAN
upon creation.


### Slides — strona 385

switchport mode access
switchport access vlan <id>
S1(config)#interface range fastEthernet 0/1-2
Thevassignment of hosts (end S1(config-if)#switchport mode access
devices, such as PCs) to different S1(config-if)#switchport access vlan 100
VLANs is done by matching the an .
interconnected interface to the S1(config-if)#exit
appropriate VLAN.
S1(config)#interface range fastEthernet 0/3-4
a ae P S1(config-if)#switchport mode access
Tip: Assigning multiple ports to a an .
VLAN simultaneously can be done S1(config-if)#switchport access vlan 200
using the command. $1(config-if)#exit


### Slides — strona 386

Si#show vlan brief
VLAN Name Status Ports
By running the oo Le ee 8
command, it'is.easy to spot:the 1 default active Fa@/5, FaQ/6, FaQ/7, Fae/8
two new VLANs and the Fa@/9, Fa@/10, Fa@/11, Fae/12
interfaces assigned to them. FaQ@/13, FaQ@/14, Fa@/15, Fa0/16
Fa@/17, FaQ@/18, FaQ/19, Fae/20
Fa@/21, FaQ/22, FaQ/23, Fae/24
To display the interface mode, Gig@/1, Gige/2
use ‘
1002 fddi-default active
10@3 token-ring-default active
1004 fddinet-default active
1005 trnet-default active


### Slides — strona 387

switchport voice vlan <id>
: : S1(config)#interface fastEthernet 0/1
eee area S1(config-if)#switchport mode access
. S1(config-if)#switchport access vlan 100
the network.
S1(config-if)#exit

The example on the right shows
how a Voice VLAN is set up on
an interface.
Note: VoIP settings on the
network are necessary, but are
not within the scope of this
course.


### Slides — strona 388

CO
VLANs & Trunk
TRUNK PROTOCOLS


### Slides — strona 389

Trunk Protocols
Trunk Mode
What is Trunking?
Trunk mode is designed to transmit multiple VLAN traffic sessions,
over the same physical connection, to a remote device, such as a
switch or router.
This is done by tagging frames with the source VLAN, ensuring that
the Trunk link forwards the VLAN frames to the same VLAN on
another switch. This helps maintain the isolation of other devices.
6
Trunk mode makes sure that relevant information stays among devices within the
same VLAN (such as switches). However, routing among VLANs still requires a router.
17


### Slides — strona 390

Trunk Protocols
Trunking Protocols
Inter-Switch Link
, | it | ln ISL is a proprietary protocol developed by Cisco that only operates on Cisco
cisco equipment.
The protocol adds VLAN information to Ethernet frames.
IEEE 802.1Q
802.1q or dotigq is an industry standard developed by IEEE that allows trunk
IEEE link creation between various vendor switches.
J Cisco uses this standard as its default trunk protocol.
Unlike ISL, 802.1q encapsulates the VLAN info in the frame.
18


### Slides — strona 391

Si(config)#interface gigabitEthernet 0/1
S1(config-if)#
The S1(config-if)#exit
command sets the interface to
trunk mode and creates trunk . . . .
links. S2(config)#interface gigabitEthernet 0/1
S2(config-if)#
S2(config-if)#exit
To display the trunk’s configuration,
run the S1#show interfaces trunk
command: Port Mode Encapsulation Status Native vlan
al
Note: The switchport mode
trunk command creates a static S2#show interfaces trunk
trunk link, without using the Port Mode Encapsulation Status Native vlan
DTP protocol. 1


### Slides — strona 392

Trunk Protocols

Dynamic Trunking Protocol

DTP is a protocol developed by Cisco to automate the creation of
~, trunk links, mainly to save time and prevent misconfiguration.
>_> Ne DTP operates on Cisco switches by default, and uses a special packet
» >> to "negotiate" the interconnected interfaces.
DTP is also responsible for selecting the trunk protocol on both sides.
&
DTP can be disabled on specific ports for security purposes (such as to prevent switch spoofing attacks).
20


### Slides — strona 393

Trunk Protocols
DTP Modes
The protocol includes two port modes for interface negotiation.
Dynamic Auto
This mode, which is the default for every port, is passive and does not negotiate.
Instead, it waits until an explicit request is received from the other side, and then
establishes the trunk link.
Dynamic Desirable
This mode actively attempts to change the mode of the interconnected interface
via DTP packets, to establish a trunk link.
Once a directly interconnected port is set to trunk, dynamic auto, or dynamic
desirable, a link will be established.
21


### Slides — strona 394

switchport mode dynamic <mode>
S1(config)#interface gigabitEthernet 0/1
The example on the right shows the S1(config-if)#
configuration of DTP modes on the S1(config-if)#exit
interconnected interfaces of the
switches. 4 : 4 4
Remember: Dynamite Aurerie the S1(config)#interface gigabitEthernet 0/1
default mode. S1(config-if )#
S1(config-if)#exit
To display the interface mode,
use f


### Slides — strona 395

switchport nonegotiate
Since using DTP can make the switch S1(config)#interface fastEthernet 0/1
vulnerable to a VLAN attack, it is best S1(config-if)#switchport mode access
to disable DTP on a port connected S1(config-if)#
to an end device. S1(config-if)#exit
Configuring the port in access mode S1#show interfaces switchport
is not enough, and is Name: FaQ@/1
required. Switchport: Enabled
Administrative Mode: static access
To display the interface mode, use Operational Mode: down
; Administrative Trunking Encapsulation: dotiq
Operational Trunking Encapsulation: native


### Slides — strona 396

Trunk Protocols
Port Configuration Options
Mode Negotiation Results
Dynamic Dynamic
Auto Desirable Trunk Agnes
Dynamic Access Trunk Trunk Access
Auto
Dynamic Trunk Trunk Trunk Access
Desirable
Trunk Trunk Trunk Trunk ---
Access Access Access --- Access
24


### Slides — strona 397

Trunk Protocols
Native VLAN
What is a Native VLAN?
of Native VLANs process untagged frames when they reach trunk ports.
Rod Untagged frames are frames that do not have a source or destination VLAN.
= VLAN 1 is the default native VLAN.
Why is Native VLAN Required?
>a Without Native VLANs, sending and receiving updates for protocols such as CDP, VTP,
DTP, and STP among interconnected switches would not be possible, since trunk ports
drop untagged frames.
25


### Slides — strona 398

Trunk Protocols
Important Native VLAN Points
Best Practice
A best practice regarding Native VLANs is to re-assign them to non-default VLANs, such
as VLAN 200, for security purposes. Doing so, can, for example, mitigate Double Tagging
attacks.
Identical Native VLAN
The same Native VLAN must be used on both ends of the trunk link. If not,
) c) untagged frames will not be delivered correctly, and the switch’s OS will
bs PS continuously send warning messages to the user, in the form of:
1 ff) “%CDP-4-NATIVE_VLAN_MISMATCH: Native VLAN mismatch discovered on
GigabitEthernet0/1 (200), with $2 GigabitEthernetO/1 (1).”
26


### Slides — strona 399

switchport trunk native vlan <id>
S1(config)#interface gigabitEthernet 0/1
The example on the right shows how S1(config-if)#
to change the default native VLAN S1(config-if)#exit
on two interconnected switches.
S2(config)#interface gigabitEthernet 0/1
S2(config-if)#
To display the Native VLAN settings S2(config-if)#exit
use
S1#show interfaces trunk
Port Mode Encapsulation Status Native vlan
GigQ/1 on 802.1q trunking
S2#show interfaces trunk
Port Mode Encapsulation Status Native vlan
GigQ@/1 on 802.1q trunking


### Slides — strona 400

CO
VLANs & Trunk
INTER-VLAN ROUTING


### Slides — strona 401

Inter-VLAN Routing
Inter-VLAN Routing Overview
Inter-VLAN Routing
Although VLANs are logical segments, they still operate within the
framework of a network, which means they are also broadcast
domains.
Switches (which generally operate at Layer 2) cannot move traffic
across different VLANs or broadcast domains.
Routing data among different VLANs requires a Layer 3 device (such
as a router), which encapsulates and decapsulates the frames.
B
A Layer 3 switch (also known as a multilayer switch) can be used for routing among VLANs,
which can also reduce the amount of network components needed to handle the traffic.
29


### Slides — strona 402

Inter-VLAN Routing
Router-On-A-stick
How Does Inter-VLAN Routing Work?
The most common technique for Inter-VLAN Routing is called
Router-On-A-Stick.
This method is effective because it requires only a single physical
connection between the switch and the router, avoiding the need
SS for additional components and costs.
&
30


### Slides — strona 403

Sub-Interface
Multiple IP Addresses Sub-Interface Command
Multiple IP addresses are possible because a R1(config)#interface
1 ni oy . . gigabitEthernet @/0.1
router’s single physical interface is segmented into
multiple logical interfaces, called sub-interfaces. R1(config)#interface
@ gigabitEthernet 0/0.2
Logical Interface R1(config)#interface
aa Each sub-interface is configured with a unique IP gigabitEthernet @/0@.3
sve | address and subnet mask. Every sub-interface
5 represents a default gateway for a specific VLAN.
Simple rule: The number of VLANs dictates the number of sub-interfaces.
31


### Slides — strona 404

Switchport mode trunk
S1(config)#interface gigabitEthernet 0/1
S1(config-if)#switchport mode trunk
S1(config-if)#exit


### Slides — strona 405

- R1(config)#interface gigabitEthernet 0/20
pees eee _ R1(config-if)#
. Enter e€ physical interface : . .
and enable tt: R1(config-if)#exit
R1(config)#interface gigabitEthernet
2. Create a sub-interface. R1(config-subif)#encapsulation dot1Q
3. Configure interface R1(config-subif)#ip address
encapsulation on 802.1q and R1(config-subif)#exit
assign the appropriate VLAN ID.
R1(config)#interface gigabitEthernet
R1(config-subif)#encapsulation dot1Q
4. Configure the VLAN’s R1(config-subif)#ip address
corresponding IP address R1(config-subif)#exit
and mask (default gateway).
5. Repeat this process for
every VLAN.


### Slides — strona 406

Ri#show ip interface brief
Interface IP-Address OK? Method Status
Protocol
Use
to display the interface settings
and mode.
GigabitEthernet@/1 unassigned YES unset administratively down down
= Vlan1 unassigned YES unset administratively down down
e
command shows additional
details, such as the interface
and its VLAN ID.


### Slides — strona 407

Inter-VLAN Routing
Lab NET-09-L1 Jai
a = Eo" Sway . The objective of this exercise is to learn how to configure
Configuring VLANs, Trunks, and More | VLANs and trunks.
oe r SS ‘ ” Configure & verify VLANs.
- a «€ ; ‘ 8 Configure trunks and native VLANs.
7 —. 4 = ® Configure R.O.A.S
a /, i,
P ton » >
j l
| ® ; @ r 8 OS: All platforms ® Lab document
=m 8 Tools: Cisco Packet Tracer ®& NET-O9-L1.pka
. y} 722
| .
‘ |


### Slides — strona 408

- / : . ee 7 ; 2 = :
‘ 7
= eat ¥ oat / “s
al = g \ . =
i VSso, ~ =
Fees \ 2 —
COTTE & ~
POPE » * a
{ > CAINS ~ 0 ee
J PORE " Fe
COV OSS > &
H 2 ~~ a ———.
i CU i ™
Me, "a », y 4, Fees
Sh SOS jj .
“ : ay Wage, y eS /
( ep y t /
~~" 2 CS — be a!


### Slides — strona 409

ok
aul egal 5 i 2B
— _ = : ste a) :
ie. = 4 a wet NETWORK Sr cay Cm D


# Chapter 10: Diagnostics & Troubleshooting


### Slides — strona 410

= A ay canoe ee ee |
Diagnostics & Troubleshooting
Computer Networking


### Slides — strona 411

Computer Networking
Introduction Network Switch & IOS Switch IP & Routing
to Networks Fundamentals Fundamentals Security Concepts
Diagnostics & Dynamic IPv4 & IPv6é Subnetting
Troubleshooting NLANs & Trdnis Routing Static Routing Concepts
Access Infrastructure Final Project
Control List Services
2


### Slides — strona 412

Diagnostics & Troubleshooting
Overview
Lesson Objective
The object of this lesson is to understand Troubleshooting Methods
how to diagnose network issues and
troubleshoot them. Neighbor Discovery Protocols
The lesson also introduces useful tools for
troubleshooting and explains how CDP Log Events & Syslog Server
works, what log events are, syslog server
operation, and the Network Time Protocol. Network Time Protocol
G
3


### Slides — strona 413

i
Diagnostics & Troubleshooting
Troubleshooting Methods


### Slides — strona 414

Troubleshooting Methods
Troubleshooting Overview
What We Will Learn
Issues can and will arise, even in networks that were designed using
the most advanced technologies.
=
This lesson covers the ways network issues can be resolved and the
tools that can help resolve them quickly and efficiently.
An important aspect of network troubleshooting, also described in
this lesson, is the usage of discovery protocols.
e
5


### Slides — strona 415

Troubleshooting Methods
Troubleshooting
Documentation
y
— Quick and efficient troubleshooting is based, in part, on continuous and detailed
= network-related documentation.
What Does Documentation Include?
ii =. Network documentation includes the following: physical and logical topological
C= diagrams, network and end-device backup configuration files, IP and MAC addressing
—— schemes, and network performance baselines.
6


### Slides — strona 416

Troubleshooting Methods
Gather Information
The first and most important step is gathering a a
information and symptoms from network Isolate the Problem
devices, ehdl systems Jana OSErs, Based on the symptoms, eliminate variables until
a single problem or a set of related problems is
> identified as the cause.
Implement a Solution
Consider the severity of the problem and the
impact of the solution. Then, begin planning, Se Problem Solved?
testing, and documenting possible solutions.
If the problem was not solved, repeat steps two
and three again and deepen the research.
Documentation 7
Document every step you took in the process for
future reference.
7


### Slides — strona 417

Troubleshooting Methods
Gathering Information

01 Question end users | CMD network commands 05

02 Protocol analyzers

(Wireshark, etc.) show and debug commands 06
03 Physical troubleshooting tools IP SLA: monitors network 07
(cable tester, others) performance in real-time
Network . .
04 management software | Neighbor Discovery Protocols 08
8


### Slides — strona 418

Troubleshooting Methods
Open Systems Interconnection (OSI) Troubleshooting Methods
In this method, the starting In this method, the starting In this method, the starting
point is at the bottom of the point is at the top of the OSI point is not predefined as in
OSI model: the physical layer. model: the application the other methods.
The examination starts from layer. A particular layer is selected
the network’s infrastructure, The examination starts from and examined; if the layer
such as cables and NICs. the application itself. functions, then the next
layer to examine is the one
above it. If the layer is
faulty, then the next one
should be the one below it.
9


### Slides — strona 419

Troubleshooting Methods
Software Tools
Software Troubleshooting Tools
Network Management Software (NMS) provides excellent tools for
(@) © troubleshooting.
NMS continuously monitors network activity and establishes a clear
baseline for reference purposes. This enables network administrators
= to promptly identify issues, and, in some cases, even predict the
occurrence of such issues.
e
10


### Slides — strona 420

Troubleshooting Methods
show ip interface brief show running-config show startup-config

show interfaces show ip route verifies show ip interface show running-config show startup-config
outputs a large network reachability. brief presents only displays the complete displays the complete
volume of It will indicate if information about device configuration device configuration
information, including routing protocols are interfaces associated that is being used at that ree: used
interface errors, — operating as they with the IP protocol. that time. when it loads.
bandit utilization, should. The command
and interface speed. outputs a detailed

summary of interface

status and IP

addresses.

11


### Slides — strona 421

e
Extended ping & traceroute Commands
, Extended Ping Example
Extended Ping ae
ping
Extended ping is used to perform advanced checks of Protocol [ip]:
network connectivity. It is also able to change the source Target IP address:
IP on the packet leaving the router. Repeat count [5]:
Wd Datagram size [100]: C
Timeout in seconds [2]:
Traceroute Sending 6, ) ICMP Echos to
The traceroute command discovers the path packets nait » timeout is :
take to a remote destination and where routing failures vere ele)
Success rate is 100 percent (6/6),
occur.
round-trip min/avg/max = @/0/3 ms
12


### Slides — strona 422

OO
Diagnostics & Troubleshooting
Neighbor Discovery Protocols


### Slides — strona 423

CDP Overview

Cisco Discovery Protocol
CDP (Cisco Discovery Protocol) is a Layer 2 Cisco proprietary

8 | | | Py | | | a protocol enabled by default on all Cisco devices. Its purpose is
similar to the purpose of NDP.

C | Ss C Oo 7 CDP can be disabled on specific devices or interfaces for
security reasons.
é
14


### Slides — strona 424

Neighbor Discovery Protocols
Eavesdropping Information Gathering
‘4

[i ‘
Since CDP does not encrypt CDP gathers information on CDP advertisements are
transmitted data, it is the local device and special packets that reveal
vulnerable to reconnaissance- periodically sends it to all device details to neighbors
type attacks (such as Sniffing). directly connected devices. also running CDP.
Such attacks will allow the When advertisements are
attacker to map the victim’s received, they are stored in
network and more. the neighbor table.

15


### Slides — strona 425

CDP Advertisement
CDP Packets
CDP includes the following data in advertised packets:
* Type of device (router, switch)
l *« Device name
° ¢ Interconnected interfaces

tL. DP * IOS version
* Next-hop IP
* Connection’s duplex mode (full, half)

ES
16


### Slides — strona 426

Neighbor Discovery Protocols
Mismatch Detection
Mismatch Error Detection
CDP includes a unique feature that can detect a protocol-connection
mismatch.
When such a mismatch is detected, CDP notifies the network
administrator by recording the incident in a log.
® Examples of mismatch types include:
¢ Native VLAN mismatch
* Duplex mismatch
e
17


### Slides — strona 427

CDP Intervals
CDP Show Command Output
CDP Packet Timer
S1#show cdp
fe HID CDP sends advertisement packets every 60 Global CDP information:
j seconds by default to all directly connected Sending CDP packets every
devices Sending a holdtime value of
, a Sending CDPv2 advertisements is enabled
CDP Hold Timer
If a device does not receive CDP packets from a
Me, I Pal < neighbor for 180 seconds, it will consider that
a LN neighbor "dead“ and remove it from its
neighbor table.
@ </>
The timers can be modified.
18


### Slides — strona 428

cdp run \ enable
#Enable\Disable on Device:
Because CDP is not secure or S1(config)i#cdp run
encrypted, it is easy to eavesdrop. S1(config)#no cdp run
If necessary, the protocol can be
turned off entirely on the device or #Enable\Disable on Port:
on selected interfaces. S1(config)#interface range fastEthernet @/1-24
S1(config-if-range)#cdp enable
Recommended: Enable CDP S1(config-if-range)#no cdp enable
only for port interconnection
with other network devices.


### Slides — strona 429

The command
displays all connected devices that
CDP can communicate with. | a) LFA
The command s4 R4 $2
displays more information on each device,
such as IP address and IOS version.
S1#
Capability Codes: R - Router, T - Trans Bridge, B - Source Route Bridge
S - Switch, H - Host, I - IGMP, r - Repeater, P - Phone


### Slides — strona 430

Neighbor Discovery Protocols
Link Layer Discovery Protocol
LLDP is a Neighbor Discovery Protocol similar to CDP that was
developed by the IEEE.
IEEE LLDP is an industry standard protocol, meaning it is not proprietary
° and can operate on any network device, and even on PCs and servers.
Although LLDP is not enabled by default on Cisco devices, it is fully
supported.
e
21


### Slides — strona 431

LLDP Intervals
LLDP Sh Cc d Output
LLDP Packet Timer aii
Si#show lldp
AD LLDP sends advertisement packets every 30 Global LLDP Information:
seconds by default to all directly connected Status: ACTIVE LLDP advertisements are
/ devices sent every
. a LLDP hold time advertised is
LLDP Hold Timer
If a device does not receive LLDP packets from a
~ t a neighbor for 120 seconds, it will consider that
= . neighbor "dead“ and remove it from its neighbor
table.
O </>
22


### Slides — strona 432

Lldp run \ receive \ transmit
LLDP is also not secure or encrypted, #Enable\Disable on Device:
like CDP. If necessary, it can be turned S1(config)#11ldp run
off entirely on the device or fora S1(config)#no lldp run
specific direction on selected
interfaces.
S1(config)#interface range fastEthernet @/1-24
Recommended: Enable LLDP S1(config-if-range)#lldp transmit
only on ports interconnected S1(config-if-range)#no lldp transmit
with other network devices. S1(config-if-range)#lldp receive
S1(config-if-range)#no lldp receive


### Slides — strona 433

LLDP show commands are similar to CDP
show commands but can display additional SF, — ,
information. — f ——€ ——_ (4
S41 R1 $2
The commands include
and :
S1#
Capability codes:
(R) Router, (B) Bridge, (T) Telephone, (C) DOCSIS Cable Device
(W) WLAN Access Point, (P) Repeater, (S) Station, (0) Other
Total entries displayed: 1


### Slides — strona 434

ee eee
Diagnostics & Troubleshooting
Log Events & Syslog Server


### Slides — strona 435

Log Events & Syslog Server
Overview
What Is Syslog?
Syslog is a standard for logging messages.
Each device records actions and events that occur like a
— — private diary.
| LOG Among other tasks, network administrators need to monitor
the network to ensure smooth, errorless functionality.
__J} Monitoring the network improves troubleshooting capability
and helps identify issues such as device health and network
load.
&
The syslog protocol is documented in RFC 5424.
26


### Slides — strona 436

Log Events & Syslog Server
System Log Events
Why Are Logs Useful?
System notification logging increases a network administrator's
awareness of hardware or software malfunctions, service status,
and security accountability.
In some cases, logs can be used to predict component failures.
Log analysis can help administrators troubleshoot the system and
can be useful to information security experts when investigating
security breaches.
Syslog messages can be stored locally on the device or on a syslog server in the network.
27


### Slides — strona 437

Log Events & Syslog Server
Device Logs
Log Storage
Log storage takes up space, and can, in some cases, degrade
system performance.
= Log message count is limited due to buffer size.
= Collecting logs from separate devices can take a long time.
= RAM is erased upon device power off.
&
28


### Slides — strona 438

Log Events & Syslog Server
— {__
|
A logging buffer is a Console line is a method of Terminal line is a method of If a syslog server is
predetermined storage viewing messages locally via viewing messages via a CLI configured on the device,
space allocated on RAM the console window. program (such as Putty). the device will send all
for syslog messages. syslog messages to the
server over the UDP 514
port.
29


### Slides — strona 439

Log Events & Syslog Server
Syslog Server
What Is a Syslog Server?
A syslog server is a computer that runs syslog software.
The syslog software concentrates logs from all devices (PC, router,
etc.) on the network into one centralized location, which makes
management and log backup easier.
It also offers a convenient user interface.
This way of working is more efficient than storing logs in RAM.
Many free and enterprise versions of syslog exist, such as the Kiwi Syslog Viewer.
30


### Slides — strona 440

Log Events & Syslog Server
Severity & Facility
Syslog messages include several pieces of information, of which the most important are:
Message Severity
The urgency of the log message is represented by its severity level, which is a number
value from 0 to 7. Level 0 indicates emergencies, and 7 indicates system debugging.
The values also represent critical malfunctions and system warnings.
Message Facility
The facility parameter indicates the source that generated the message, which,
for example, can be a network card or routing protocol.
The facility can be a hardware component, protocol, or system service.
31


### Slides — strona 441

Log Events & Syslog Server
Syslog Message Severity Levels
The following table lists syslog severity levels with their number values.
The lower the number, the higher the severity.
Severity Levels
Message Type Severity Level Explanation
Emergency Level 0 System unusable
Alert Level 1 Immediate action is required
Critical Level 2 Critical condition
Error Level 3 Error condition
Warning Level 4 Warning condition
Notification Level 5 Normal, but important
Information Level 6 Informative message
Debugging Level 7 Debugging message
32


### Slides — strona 442

, Log Event ; ; ; , F
i*Dec 28 19:01 i LINK} =5= i CHANGED: 1 Interface GigabitEthernet@/1, changed state to up}
: 1 1 2 t 34 4 ' 5 b>
Enable GigO/1 Log
1. Timestamp: records the time and date of the log (this service is R1(config)#interface gigabitEthernet @/1
disabled by default and should be enabled once so the system has the R1(config-if)#no shutdown
correct time info)
2. Facility: The category of the source that created the log message. In
the example above, link represents the state of the router's hardware
ports.
3. Severity: The severity level, which, in the example above, indicates
that it is a notification message.
4. Mnemonic: a device-specific code that identifies the log message
5. Text Description: the log/event description and other details
33


### Slides — strona 443

Log Events & Syslog Server
Typical configuration commands used to set up syslog on a Cisco device:
Cisco Syslog Commands
Command Description
logging host Sets the destination syslog server
logging trap Determines what log severity levels to send to the server
won sienna play Attaches time information to the alerts
datatime msec
logging console Shows system messages on the screen of the console connection (enabled by default)
terminal monitor Shows system messages on the screen of a remote connection (Telnet, SSH)
login buffered Saves system messages to the RAM (enabled by default) FEE
34


### Slides — strona 444

R1(config)#logging host 172.16.0.250
R1(config)#logging trap debugging
The dad command sets R1(config)#logging userinfo
theldestination |P'of-the syslog R1(config)#service timestamps log datetime msec
server, to which all logs are sent.
R1(config)#do show logging
The command <Output Omitted>
sends all severity log levels to ESM: @ messages dropped
the server (levels 7 and above). ,» 9 message lines logged
(udp port 514, audit disabled,
authentication disabled, encryption disabled, link up),
The remaining commands in 2 message lines logged
. d
the example on the right are @ message lines rate-limited,
used to add time records. .
@ message lines dropped-by-MD,
xml disabled, sequence number disabled
filtering disabled


### Slides — strona 445

aa 2... =...
Diagnostics & Troubleshooting
Network Time Protocol


### Slides — strona 446

Network Time Protocol
NTP Overview
What is NTP?
NTP (Network Time Protocol) is responsible for the synchronization of
4 the time and date across all devices on the network.
NTP is a simple client-server protocol and is implemented in networks
everywhere.
, It is very easy to set up and even has an authentication mechanism
for security.
NTP operates on UDP port 123 and is defined in RFC 1305.
37


### Slides — strona 447

Network Time Protocol
Time Configuration
Date and time for network devices can be set in one of two ways:
Vaal Cogeco eee =o”
This method requires manual setting of the time and date on each device on the
network.
It is not recommended to work this way for various reasons, among which is the lack of
scalability for large networks. (Setting the clock in every device will waste valuable time.)
Automatic Configuration
This method requires an available and configured NTP server.
Only the server’s IP address needs to be set on network devices.
This ensures that all devices on the network will be set to the most accurate
A) eS) 2 time and date automatically.
Cisco routers can be configured to act as NTP servers. a
38


### Slides — strona 448

NTP Usage
=o000 Cisco routers and switches (and many other devices around the world) use NTP to
= determine the date and time, although routers and switches can also act as NTP servers.
Stratum Model
Stratum levels define the distance from high-precision reference clocks, which begin with
stratum 0, to devices connected hierarchically. Servers linked to the reference clock are
stratum 1, devices that receive the time from the servers are stratum 2, and so on.
To avoid delays, a maximum of 15 levels are allowed. a
Services
rx Accurate time settings are crucial for many protocols and device functions. For example,
DHCP leases and syslog events are time-sensitive services. Timestamps are extremely
Caw important for troubleshooting, management, and network security.
39


### Slides — strona 449

clock set <hh:mm:ss> <day> <month-name> <year>


### Slides — strona 450

R1(config)#
To make R11 set the clock with R1(config)#do show clock
an external NTP server, use the 18:58:46.855 UTC Sat Dec 28 2019
command together
with the server’s IP. R1(config)#
R1(config)#interface gigabitEthernet 0/1
Verify the device time information R1(config-if)#no shutdown
using the command or %LINK-5-CHANGED: Interface GigabitEthernet@/1,
changed state to up
Once the device clock is
tuned correctly, run
, which logs device
messages and events with a
time and date.


### Slides — strona 451

ntp master <1-15>
R1(config)#ntp master
R1(config)#do show run ntp


### Slides — strona 452

Network Time Protocol
; 2 = eee The objects of this lab are to answer questions based on
Pac. et material covered in the lesson and understand how to
Configure NTP and Syslog | configure NTP and syslog servers.
a ie r @ yA : 1 Answer the questions.
. " ‘ « ; ® Configure Syslog.
,—-=1 Ts” = ® Configure NTP.
| —an ® 8 OS: All platforms © Lab document
: ® Tools: Cisco Packet Tracer ® NET-10-L1.pka
. y) 7.2.2 or higher
\ |
i e { ~ 43


### Slides — strona 453

d f 9 rd ; - * 5 y A ~ - ‘
g 1 ’ (fp ee .

# . ~<e "SEG fas f
i < ‘ hs, < : *, pd y
OS ~ a . > > SS
SS errs. \ <i -—~ ~ u
' SISOS \ ~~

Conk ; > ~~

' Cea SD 2 .——

ys \. y 7 . =

Tim By a . i

>. ye Cy fan. a ae


### Slides — strona 454

—— — “a : ™ Ty .
ie. = 4 a wet, NETWORK ga Cm D


# Chapter 11: Access Control List


### Slides — strona 455

— a a toca NTU api =, 0 i D
_ Access Control List
Computer Networking


### Slides — strona 456

Computer Networking
Introduction Network Switch & IOS Switch IP & Routing
to Networks Fundamentals Fundamentals Security Concepts
Diagnostics & Dynamic IPv4 & IPv6é Subnetting
Troubleshooting NLANs & Trdnis Routing Static Routing Concepts
Access Infrastructure Final Projact
Control List Services J
2


### Slides — strona 457

Access Control List
Overview
Lesson Objective
The object of this lesson is to understand the ACL Overview
basic concepts of an Access Control List, and
how named and numbered standard ACLs :
. Standard ACL Implementation
are configured.
The lesson also explains Extended Access
Lists. Extended ACL Implementation
G
3


### Slides — strona 458

CO
Access Control list
ACL OVERVIEW


### Slides — strona 459

ACL Overview
Concept: Access Control List
Where it is used
ACUs are used in
° Computer Networks (Firewalls, Switches and Routers)
tl ° Computer File Systems (Servers and Workstation)
° Web Portals (Canvas, Amazon.com)
° Cloud Configurations (Amazon Web Service VPC, Microsoft Azure VNET)
é
5


### Slides — strona 460

ACL Overview
ACL Definition — Computer Networks
What is ACL?
ACL (Access Control List) is a rule-based feature that allows network
administrators and engineers to configure basic traffic filtering.
MED “YD ACLis aseries of commands that, based on information in the packet
header, determine whether to drop a packet or forward it.
é
6


### Slides — strona 461

Stateless vs Stateful
Stateless vs Stateful

One device that you place on ACU’ are firewalls.
° Stateless firewalls will remember the state of the session and close

i it once it is completed.
° Stateful firewalls will understand the details of a connection and

allow the return traffic.
Most decent firewalls today are stateful.
é
4


### Slides — strona 462

ACL Overview
ACL Advantages
Advantages of configuring an Access List on a device:
Network Performance
Network performance can be improved by allowing only relevant services to
communicate with devices across the network.
i For example, restricting the network to block video traffic can improve network
TL performance.
Securing the Network
+
In a network environment, users may be restricted from accessing sensitive services.
&) ACL provides a basic level of network security by allowing some hosts to access parts of
+ + the network, while preventing others from accessing the same parts.
8


### Slides — strona 463

Additional ACL Capabilities
Protocol Restriction
ACLs can also restrict the following:
¢ Routing protocol advertisement messages
¢ Packets from security protocols
¢ Packets from other protocols, such as ICMP
9


### Slides — strona 464

ACL Overview
Standard Vs Extended
There are Standard ACLs and Extended ACLs, with the difference in the parameters examined in the process.
Standard ACLs
Standard ACLs examine only the source IP address when implementing restrictions.
Cisco recommends to place this type of ACL as close to the destination device as
possible.
Extended ACLs
Extended ACLs filter packets according to the following parameters: protocol type,
source or destination IP address, and source or destination port.
Cisco recommends to place this type of ACL as close to the source as possible.
10


### Slides — strona 465

ACL Overview
Traffic Direction

When configuring ACL, traffic direction, inbound or outbound, must be specified on an interface. This is done

so that the router will implement the proper restrictions when examining the source network and destination.

Inbound ACL
> Configures the ACL for inbound traffic.
The router will examine incoming traffic to the interface.
Outbound ACL
é Configures the ACL for outbound traffic.
The router will examine outgoing traffic from the interface.
11


### Slides — strona 466

Wildcards
What are Wildcards?
Wildcards are inverted subnet masks that can be used in statements
— in both Extended and Standard ACLs.
© Ti | For example, 255.255.255.0
1 Paes (binary equivalent = 11111111.11111111.11111111.00000000)
0001 OB inverts to a wildcard mask of 0.0.0.255
1
(binary equivalent = 00000000.00000000.00000000.11111111)
12


### Slides — strona 467

ACL Overview
ACL Order
Check Order
= ACEs (Access Control Entries), which represent the order of statements in the ACL, are
— | crucial and must be carefully planned. The router checks each packet’s parameters
‘i against the ACEs to find a matching condition. When a condition is met, the ACL will be
applied, and additional ACEs will be ignored.
Implicit Deny
At the end of every ACL, there is an invisible statement called implicit deny.
When no match is found for a packet, the implicit deny is applied to the packet.
Note: Each ACL must have at least one Permit statement!
13


### Slides — strona 468

CO
Access Control List
STANDARD ACL IMPLEMENTATION


### Slides — strona 469

Standard ACL Implementation
Standard ACL Placement
Where are Standard ACLs Placed?
Standard ACLs are placed as close to the destination as possible.
Cisco set this rule because placing standard ACLs at the source of
traffic will prevent communication with any network hosting
interfaces to which the ACL applies.
15


### Slides — strona 470

Standard ACL Implementation
Named Vs Numbered
Standard Named ACL
e
(2) — Standard Named Access Control Lists allow unique names to be assigned to ACLs.
Standard Numbered ACL
dee = (Standard Numbered Access Control Lists allow unique numbers to be assigned
2— to ACLs.
3m The Standard Numbered ACL range includes 1-99 and 1300-1999.
16


### Slides — strona 471

Command — ; :
1 H i H H
access-list i<access-list-number>} <deny | permit |remark> | <source-address> | <source-wildcard>|
1 t
1 ! 2 i 3 H 4 H 5 ! |
: </>
Command Example
1. Beginning syntax to configure a numbered ACL. R1(config)# access-list 10
. permit 192.168.10.0 0.0.0.255
2. Decimal number from 1 to 99, or 1300 to 1999 (only for Standard
ACLs).
3. Deny - denies access if the conditions match, Permit - permits access if
the conditions match, Remark - adds a remark about entries.
4. IP of the network or host from which the packets were sent. You can
specify any instead of using a 32-bit address.
5. 32-bit wildcard mask that will be applied on the source.
17


### Slides — strona 472

Standard ACL Implementation
Network Example
Scenario #1: ———s af
A network administrator decided that new Be | y——/ aE A SS
users on network 10.0.0.0/24 will not have —_, rt si Za) =
access to the server network, but will be | —_—= i —_
able to communicate with neighboring Host A Gigo/1 aay Gigo/2 Host B
network 192.168.0.0/24 192.168.0.10/24 eee 10.0.0,10/24
00/3 |
s 4
Scenario #2: 2
After malicious software was discovered
on Host A, an administrator decided to Papgten
temporarily block access from the Host to =, ==,
10.0.0.0/24, until the threat was removed. = | =
=a ——
The following slides include ACL DNS Server FIPS:
configuration examples based on 172.16.1.1/24 172.16.1.2/24
these scenarios.
18


### Slides — strona 473

R1(config)#access-list 1 deny 10.0.0.0 0.0.0.255
ACL configuration example based R1(config)#access-list a PIER any
Sn Scenatio #1. R1(config)# interface Gigabitethernet 0/3
R1(config-if)#ip access-group 1 out
Step 1 - Create a numbered ACL R1(config-if)#exit
using the command.
Step 2 - Choose the interface for
which the ACL will apply, using
the command.
Step 3 -
command links ACL 1 to the
Gigabitethernet 0/3 interface
in the outbound direction.


### Slides — strona 474

R1(config)# ip access-list standard
ACL configuration example based R1(config-std-nac1)#deny host 192.168.0.10
on scenario #2. R1(config-std-nac1)#permit any
R1(config-std-nac1)#exit
Step 1 - Use the R1(config)#interface Gigabitethernet 0/2
command to create R1(config-if)#ip access-group out
a named ACL. R1(config-if)#exit
Step 2 - In ACL configuration
mode, create Deny and
Permit ACE statements.
Step 3 - Apply the ACL on an
interface using the
command, and specify
the traffic direction (in or out).


### Slides — strona 475

R2#
Standard IP access list Block_Host_A
1@ deny host 192.168.0.10
ACL rules can be verified in 2 permit any
different ways, one of which is by Standardhpleccesclieted
searching the running-config file
using an include filter. 1@ deny 10.0.0.@ @.0.0.255
2@ permit any
Run to R1#
ee interfassegch interface GigabitEthernet0/2
ip address 10.0.0.15@ 255.255.255.080
ip access-group Block__Host_A out
The command !
can also be used. interface GigabitEthernet0/3
ip address 172.16.0.150 255.255.255.080
ip access-group 1 out


### Slides — strona 476

Extended ACL Implementation
; _ ET The objective of this lab is to plan, configure, and verify
Implement Standard and Extended ACLs ceandard and extended RCIE
(Tasks 4-6) .
—— f Ss ; : ® Configure a Numbered Extended ACL.
“= 8 » 4 .
‘ " : « ; ® Configure a Named Extended ACL
ws. 4 = (optional).
| = Rr - LA ® Modify an Extended ACL (optional).
- iY @ : 8 OS: All platforms ® Lab document
’ 8 Tools: Cisco Packet Tracer © NET-11-L1.pka
" y) 7.2.2, or higher
*
i % =~ 22


### Slides — strona 477

CO
Access Control List
EXTENDED ACL IMPLEMENTATION


### Slides — strona 478

Extended ACLs
What are Extended ACLs?
Extended ACLs filter packets based on the following attributes:
* Source and destination IP addresses.
= ¢ Source and destination Layer4 protocols (UDP and TCP).
a ¢ Protocol type or number. For example: IP, HTTPS, 80, etc.
— e Extended ACLs use the following range of numbers: 100 to 199
and 2000 to 2699.
&
24


### Slides — strona 479

Extended ACL Implementation
Extended ACL Placement
Where are Extended ACLs Placed?
Configure Extended ACLs as close as possible to the source of the
traffic being filtered.
Doing so ensures that traffic will be denied and prevented from
traversing the network infrastructure.
It’s important to understand that even if the ACL is not placed as close as possible to
the source, the ACL will still operate as it should.
25


### Slides — strona 480

Command ~ : : : ,
H I H I H
access-list i<number> 1<action>:<protocol>! <source-address><destination-address>} <operator>
| 1 H 2 H 3 H 4 ! 5 H 6 |
</>
Command Examples
1. Syntax used to configure a numbered ACL. R1(config)#access-list 101
2. Decimal numbers. Extended ACLs use 100-199 and 2000-2699. deny ip host 10.0.@.1 host
Ev Deny - denies access if the conditions match, Permit - permits access if the 172.16.0.2
conditions match, Remark - adds a remark about entries.
4. The name of the protocol being used: IP, TCP, UDP, ICMP, etc. R1(config)#access-list 101
5. The source and destination of the network traffic, which can be Host, or a deny tcp host 10.0.0.2 host
network 32-bit address. The any option can be used, and different 172.16.0.3 eq 22
combinations can also be used.
6. For logical port configuration, the following operators can be used for more
control: It (less than}, gt (greater than), eq (equal to), neq (not equal to),
and range (inclusive reel
26


### Slides — strona 481

Extended ACL Implementation
Network Example
Scenario #1: ——
Due to new procedures and changes in the | & |
organizational structure, Hosts A and C are it) 7 ———/ 7 ———/ (J
——- a R i =
not allowed to communicate. = a wi —=s=
5 Host B
HostA GigO/1 << Gigd/2 10.0.0.10/24
192,168.0.10/24 premade:
Scenario #2:
0/3 |
The network administrator decided that Goo =
the enterprise department on network =
10.0.0.0/24 cannot access the FTP service
on the FTP server, due to the risk of Host C
exposing sensitive information. It can =, 7, 10.0.0.20/24
however receive services from the same
server, such as DHCP. = =
— —
The following slides include ACL configuration DNS Server FIP Server
examples based on these scenarios. 172.16.1.1/24 172.16.1.2/24
27


### Slides — strona 482

R1(config)#access-list 100 deny ip host 192.168.0.10 host 10.0.0.20
; : R1(config)#access-list 100 permit ip any any
ACL configuration:examples R1(config)#interface gigabitEthernet @/1
based on scenario #1. ; . x
R1(config-if)#ip access-group 10@ in
R1(config-if)#exit
Step 1 - Create a numbered ACL
using the command.
Step 2 - Choose the interface for
which the ACL will apply, using
the command.
Step 3 -
command links ACL 1 to the
GigabitEthernet 0/1 interface
in the inbound direction.


### Slides — strona 483

R1(config)#ip access-list extended
ACL configuration examples R1(config-ext-nacl)#deny tcp 10.0.0.0 0.0.0.255 host 172.16.1.2 eq 21
based on scenario #2. R1(config-ext-nacl)#deny tcp 10.0.0.0 0.0.0.255 host 172.16.1.2 eq 20
R1(config-ext-nacl)#permit ip any any
Step 1 - Use the R1(config-ext-nacl)#exit
command to create a R1(config)#interface gigabitEthernet 0/2
named ACL. R1(config-if)#ip access-group in
R1(config-if)#exit
Step 2 - In ACL configuration
mode, create Deny and Permit
ACE statements.
Step 3 - Apply the ACL on an
interface using the
command and specify
the traffic direction (in or out).


### Slides — strona 484

R2#
Extended IP access list 100
ACL rules can be verified in various 10 deny ip host 192.168.0.1@ host 10.0.0.20
ways, ane of which Is by searching 2@ permit ip any any
ee using’2n Extended IP access list Block_FTP
. 18 deny tcp 10.0.0.0 @.0.0.255 host 172.16.1.2 eq 21
2@ deny tcp 10.0.0.0 @.0.0.255 host 172.16.1.2 eq 20
Run the 3@ permit ip any any
command can to display on which
interface each ACL is applied. Rit
interface GigabitEthernet@/1
The command ip address 192.168.0.150 255.255.255.0
can also be used. ip access-group 100 in
|
interface GigabitEthernet0/2
ip address 10.0.0.15@ 255.255.255.080
ip access-group Block_FTP in


### Slides — strona 485

d f 9 rd ; - * 5 y A ~ - ‘
g 1 ’ (fp ee .

# . ~<e "SEG fas f
i < ‘ hs, < : *, pd y
OS ~ a . > > SS
SS errs. \ <i -—~ ~ u
' SISOS \ ~~

Conk ; > ~~

' Cea SD 2 .——

ys \. y 7 . =

Tim By a . i

>. ye Cy fan. a ae


### Slides — strona 486

—— — “a : ™ Ty .
ie. = 4 a wet, NETWORK ga Cm D


# Chapter 12: Infrastructure Services


### Slides — strona 487

teens! ie ei nile
-___ Infrastructure Services
Computer Networking


### Slides — strona 488

Computer Networking
Introduction Network Switch & IOS Switch IP & Routing
to Networks Fundamentals Fundamentals Security Concepts
Diagnostics & Dynamic IPv4 & IPv6é Subnetting
Troubleshooting NLANs & Trdnis Routing Static Routing Concepts
Access Infrastructure Final Project
Control List Services inal rrojec
2


### Slides — strona 489

Infrastructure Services
Overview
Lesson Objective
DHCP Overview
The objective of this lesson is to become
familiar with infrastructure services, such DHCP Implementation
as NAT, and how they are configured.
In addition, this lesson covers how to RIN ROU Eee
configure and implement DHCP.
NAT Implementation
G
3


### Slides — strona 490

OO
Infrastructure Services
DHCP OVERVIEW


### Slides — strona 491

DHCP Purpose
Why Use DHCP?
To communicate with each other, all devices on a network must
have a unique IP address.
eo$0o
CI e Network administrators will often be responsible for assigning
e static IP addresses to network components, such as routers,

@ servers, firewalls, etc.

: ae C Assigning a static IP address for every endpoint in an organization
can be time consuming. Many endpoints do not require a static IP
address.

&
5


### Slides — strona 492

DHCP
The solution is to use Dynamic Host Configuration Protocol (DHCP).
DHCP was designed to manage IP address allocation automatically on
any network or device. It operates as a server with a range of IP
addresses that it allocates dynamically to devices on the network.
It also includes additional network information, such as the DNS
server address, default gateway address, and more.
Routers can also operate as DHCP servers.
2)
DHCP is defined in RFC 2131.
6


### Slides — strona 493

DHCP Overview
DHCP Characteristics
OSI Model Layer Logical Ports
DHCP operates in the DHCP operates on UDP DHCP supports both
application layer of the ports 67 (server) and 68 IPv4 (DHCPv4) and
OSI and TCP/IP models. (client). IPv6 (DHCPv6).
%


### Slides — strona 494

DHCP Overview

Dynamic Allocation Automatic Allocation Reservation Address
The DHCP server assigns As in the dynamic The network administrator
an available IP address to allocation method, the configures the DHCP
fhe client trom ifsaddress client receives a random server to allocate a

ool for a limited amount available IP address. But in specific IP address to a
poo! this case, there is no time selected client device.
of time. limit for the address. ;

. . The address is reserved for
This means that the client The client does not have a specific device in
“leases” the address from to renew the lease for the advance based on its MAC
the server for a period set address it was assigned. address.
by Ene eediritnistrater This method is useful for
At the end of the lease, devices such as network
the client requests an printers and others.
extension or a new
address.

8


### Slides — strona 495

DHCP Operation
How DHCP Works
The DHCP process includes four basic steps:
Discover, Offer, Request, and Acknowledgment (DORA).
{0}-*} The client device typically starts the process by contacting the server.
The information passing between the client and server is encapsulated in
| D> dedicated DHCP packets.
The DHCP server allocates the IP address and other information according
to the chosen allocation method (dynamic, automatic, etc.).
9


### Slides — strona 496

DHCP Overview
DHCP Process
DHCP Discover
A client device that requires an IP address
sends a discover message in broadcast to ii DHCP Offer
search for a DHCP server on the network. After the server receives the discover
message, it reserves an available IP address
and offers it to the client along with the
DHCP Request a lease details. H
The client responds to the offer with a
request to accept the offer or decline it. iin DHCP Acknowledgment
After receiving the request message, the
server sends the DHCPACK containing all
necessary configuration information.
10


### Slides — strona 497

DHCP Overview
DHCP Lease Renewal Process
DHCP Request
HELP| Before a lease expires, the client sends a DHCPREQUEST message directly to the
pd DHCPV4 server that originally offered the IPv4 address.
DHCP Acknowledgment
w Upon receiving the DHCPREQUEST message, the server verifies it and, if possible,
extends the lease information by returning a DHCPACK.
11


### Slides — strona 498

DHCP Overview
Router vs. Server
Router Server
Used in small and medium-sized businesses Used in larger networks and enterprises
Easy to manage Easy to manage
Requires knowledge of Cisco IOS and the Requires general knowledge of servers,
relevant configuration especially DHCP servers
Relatively low cost, as no device is required Relatively expensive, especially if the
other than the existing router organization needs to buy a dedicated server
to act as the DHCP server
one <
12


### Slides — strona 499

DHCP Overview
DHCPv6
DHCP for IPv6
Unlike IPv4, IPv6 uses multiple types of addresses from different
hosts. DHCPv6 was developed due to the usage in networks of
various address formats and prefixes instead of subnet masks.
DHCPv6 also supports more allocation methods than DHCPv4.
For example, an IPv6 host can automatically generate an IP address
internally using stateless address auto-configuration (SLAAC) or the
EUI-64 process for link-local addresses.
&
13


### Slides — strona 500

SLAAC
Tres In this method, the device can obtain an IPv6 global address without the services of a DHCP
server. The device uses ICMPv6 for advertisement messages to provide addressing and other
Y configuration information that would normally be provided by a DHCP server.
Stateless DHCPv6
The stateless DHCPv6 method informs the client to use the information in the router
== [=] advertisement (RA) message for addressing, while additional configuration parameters are
ca =] available from a DHCPVv6 server. The client will then communicate with a stateless DHCPv6
»— Le} server to obtain additional information not provided in the RA message, such as a DNS server
address. ao
Stateful DHCPv6
Like DHCPv4, addressing information and configuration need to be obtained from
EEE a DHCPvé6 server.
14


### Slides — strona 501

OO
Infrastructure Services
DHCP IMPLEMENTATION


### Slides — strona 502

Configiration btaps R1(config)#ip dhcp excluded-address 192.168.0.1

Stepdluexcludesaddresses fromthe R1(config)#ip dhcp excluded-address 192.168.0.100 192.168.0.150

DHCP pool. ' és

fe ' R1(config)#ip dhcp pool LAN1

i dean par canal eka R1(dhcp-config)#network 192.168.0.@ 255.255.255.0

gateway or statically configured R1(dhcp-config)#default-router 192.168.0.1

servers’ R1(dhcp-config)#dns-server 192.168.0.105
R1(dhcp-config)#domain-name Cyber.com

Step 2: Set up a DHCP pool of R1(dhcp-config)#lease @ 4 30

addresses using R1(dhcp-config)#exit

Step 3: Configure specific tasks, such

as the default gateway, DNS server,

domain name, etc.

Note: The /ease 0 4 30 (days, hours,

minutes) will not work in Packet

Tracer, but it does work on real Cisco

devices.


### Slides — strona 503

Ri#show ip dhcp pool
Several commands can be used to :
verify and troubleshoot DHCP Utilization mark (high/low) : 100 / @
settings: Subnet size (first/next) :@/20
: Displays pool

settings Pending event : none

: Displays the
client ist win le MaACiaddress, end 1 subnet is currently in the pool

C “Di Current index IP address range Leased/Excluded/Total

: Displays IP
conflicts detected during DHCP 192.168.0.1
negotiation


### Slides — strona 504

R1(config)#interface gigabitethernet 0/0
DHCP relay is a technique that #The IP of the DHCP Server.
allows devices to obtain addresses R1(config-if)#ip helper-address 10.0.0.250
from a DHCP server on a remote R1(config-if)#exit
network.
Note: Broadcast messages are not
transmitted to other networks.
When a client sends
DHCPDiscover, the router acts as a
relay and forwards the message
directly to the server in unicast.
Enable the
command and DHCP server
address on the interface that
receives the requests.


### Slides — strona 505

R1(config)#interface gigabitethernet 0/0

R1(config)#ip address dhcp
A router can also act as a DHCP client. R1(config)#exit
Its interface can be set manually or , r 7]
dynamically. : c+ ' ‘ = fee ;
Use the command on R1(config)#do show ip interface brief
the interface to enable dynamic Interface IP-Address OK? Method Status
allocation. Protocol

GigabitEthernete/e 209.168.201.12 YES DHCP up up
For example, an interface facing the GigabitEthernet@/1 unassigned YES unset administratively
ISP typically gets an IP from the ISP
DHCP server.


### Slides — strona 506

DHCP. Implementation
Lab NET-12-L1 Mission
2 eee The objective of this lab is to set up a DHCP service on a Cisco
eel eae | Ld GDU 4 router and make sure all devices on the network receive addresses
Configure DHCPv4 on a Cisco Router | dynamically. The lab also promotes understanding of the DHCP
30-60 Min. r relay concept.
— ¥ | re
“=e a - @ Answer the questions.
eh” p
. ’ ‘ ; ® Configure DHCPVv4 on R1.
=. Y “ ® Verify DHCP configuration.
(Wy ( LA @) @ Configure DHCP rel
| ' ’ , ® Configure relay.
amv 3 3
j
‘ s , 5 a , Envir TEEEICEIC ¢€ PVUVUIS IACSIGtCCU FT TGs
man ® ; 8 OS: All platforms » Lab document
: ® Tools: Cisco Packet Tracer ® NET-12-L1.pka
" \ Z 7.2.2 or higher
\ —
4 = 20


### Slides — strona 507

OO
Infrastructure Services
NAT OVERVIEW


### Slides — strona 508

NAT Overview
What Is NAT?
NAT Protocol
Network address translation (NAT) is an essential protocol and service
Eda that converts a private address to a public address and vice versa.
NAT is usually enabled on a firewall or router device at the edge of
RR. the local network and the beginning of the outside network.
Access to the internet from any home-based, corporate, or local
network is only possible through NAT.
&
22


### Slides — strona 509

NAT Overview
Why Use NAT?
NAT’s Usefulness
Although IPv4 is required for a device to communicate properly, the
number of available addresses is being depleted rapidly, and, at this
rate, a worldwide address shortage is imminent.
To save addresses and slow the depletion, private addresses were
| separated from public addresses.
Private addresses uniquely identify devices within a network, such as
a computer connected to an internal server.
Public addresses identify groups of computers outside of a local
network.
B
Private IP addresses are defined in RFC 1918.
23


### Slides — strona 510

NAT Overview
Private IP Space
According to RFC 1918, three address spaces are reserved for
devices in a private network (LAN). Their usage is unlimited,
and they can be freely implemented.
Private IP Range
IP Subnet
10.0.0.0—10.255.255.255/8 255.0.0.0
172.16.0.0-172.31.255.255/12 255.240.0.0
192.168.0.0-192.168.255.255/16 255.255.0.0
24


### Slides — strona 511

NAT Overview
NAT Operation
How NAT Works
The NAT process is transparent to users, and any evidence of its
operation is stored in a special table in the NAT-enabled device.
= ») This helps hide the internal network from the internet and adds
an extra layer of security.
— NAT operates in one of three methods: static, dynamic, or port
\N address translation (PAT).
Each method uses a specific address terminology to describe its
operation. =
Theoretically, the maximum number of private addresses
that can be translated into one public address is 65,536.
25


### Slides — strona 512

NAT Overview
NAT Advantages and Disadvantages
Advantages Disadvantages
Accessing internal resources requires special
Prevents IPv4 address depletion (PAT) configuration and makes troubleshooting more
challenging.
Reduces network performance and resource
Flexible network design and address scheme : availability. Difficult to troubleshoot issues
remotely.
Provides an additional layer of security Nal interferes with integrity checks because It
Pac modifies values in the headers. Pac
26


### Slides — strona 513

NAT Overview
Inside Local Outside Local Inside Global Outside Global
(00) at) Oo
The source IP address of the The IP address of the The public IP address used The IP address of the
local device in the private destination device as by the inside local device for destination device as
network viewed from the inside identification and access to viewed from the outside
For example: 10.0.0.5/24 local device (the the internet network (the NAT-
destination LAN) For example: The IP address enabled router)
For example: A remote on an interface facing a For example: A remote
web server WAN web server
27


### Slides — strona 514

NAT Overview

Step 1
A host on the local network sends a request to an gS
external destination (outside local), such as a web Step 2
server. The NAT-enable device receives the request and

changes the local device source address (inside
local) to the public IP configured on the WAN
Step 3 ——— interface (inside global).
[2]
The mapped address pair is saved in the device’s
NAT table and forwarded to the external destination ae Step 4
IP (outside global) on the internet.
The web server receives the request and replies
3
with a public source IP.

Step 5 ee
The NAT-enabled device receives the reply from the
web server and converts the public destination
address to the original private address (based on the
NAT table). The local host then receives the server’s
reply.

28


### Slides — strona 515

NAT Methods
Static NAT
One-to-One NAT
This is a permanent mapping of a single private IP to a specific single public address.
This method is not meant to conserve IPv4 addresses but to allow access to
internal resources from an outside network. yi
Dynamic NAT
+ Many-to-Many NAT
This method is also not meant to conserve addresses. Multiple IP addresses are
mapped dynamically by the router to a pool of public addresses. The conversion
is done on a first-come, first-served basis. a
NAT Overload Many-to-One NAT
=> NAT overload or port address translation (PAT) is the most common method and
is used to conserve addresses. In this method, multiple private IP addresses are
converted into a single public address. To distinguish the traffic from different
devices, the source port number is also used for the inside global address. @
29


### Slides — strona 516

What Is NAT64?
Network address translation IPv6 to IPv4 (NAT64) technology
C1 LE) facilitates communication between IPv6-only and IPv4-only hosts and
2S ee networks.
The solution allows enterprises and ISPs to accelerate IPv6 adoption
while simultaneously handling IPv4 address depletion.
&
30


### Slides — strona 517

OO
Infrastructure Services
NAT IMPLEMENTATION


### Slides — strona 518

NAT Implementation
NAT Topology
Network Example

The example on the right = |

illustrates the simple topology of a

a router connecting a small —

corporate network to the 10.0010 _ =

: p 10.0.0.1 |) — ren wih aque” s
R1

The next slide shows how each fie] Internet

NAT method is configured and —s

verified on R1. _—

4non20
32


### Slides — strona 519

#The interface facing the LAN.
The first step in configuring NAT is to Edge-R1(config)#interface gigabitEthernet 0/0
set the router's interfaces for the Edge-R1(config-if)#ip add 10.0.0.1 255.255.255.0
translation process. Edge-R1(config-if)#
Edge-R1(config-if)#no shutdown
The comma Edge-R1(config-if)#exit
tells the router which interfaces will
participate in the NAT process and #The interface facing the WAN.
their direction based on the network Edge-R1(config)#interface serial 0/0/0
topology. Edge-R1(config-if)#ip add 209.15.10.1 255.255.255.0
Edge-R1(config-if)#
Edge-R1(config-if)#no shutdown
Each interface connected to the Edge-R1(config-if)#exit
private network is defined as ,
and each interface connected to the
internet is defined as E


### Slides — strona 520

ip nat inside source static <local-ip> <global-ip>
In this example, a user wants to
connect to the internal server from +l Ff i) = :
somewhere on the internet. Edge-R1(config)#ip nat inside source static 10.0.0.10 209.15.10.1
The user cannot access the LAN 7 A
directly, so it sends the request to :
public router interface 209.15.10.1, ; wae " . .
and the router uses the NAT static map Edge-R1(config)# ip nat inside source static tcp 10.0.0.10 22
to forward the request to the 209.15.10.1 8080
10.0.0.10 server.
The second section in the example on
the right is for port forwarding. It
forwards only SSH traffic from outside
to the server.


### Slides — strona 521

Assume the ISP defined 10 public 1 ] E L ’ i

addresses on the WAN interface: Edge-Ri(config)#ip nat pool ToFreedom 209.15.10.1 209.15.10.10
netmask 255.255.255.0

Step 1: Create a public address pool Edge-R1(config)#access-list 1 permit 10.0.0.0 0.0.0.255

using Edge-R1(config)#ip nat inside source list 1 pool ToFreedom

Step 2: Configure standard ACL to

identify local addresses that need to

be translated using :

Step 3: Bind the ACL and the pool

using 5

Note: Using this method, the pool

should contain enough available

addresses: one for each device.


### Slides — strona 522

Edge-R1(config)#ip nat pool ToFreedom 209.15.10.1 209.15.10.10
netmask 255.255.255.0@
NAT overload or port address Edge-R1(config)#access-list 1 permit 10.0.0.0 0.0.0.255
translation (PAT) allows a router to . . oo .
use a single public address for Edge-R1(config)#ip nat inside source list 1 pool ToFreedom
multiple inside local addresses.
Methods 1 eadfigure PAT: Edge-R1(config)#access-list 1 permit 10.0.0.8 @.0.0.255
1. Use an address pool. Edge-R1(config)#ip nat inside source list 1
2. Use a single address
defined on the interface.
An important part of the command
is the option.


### Slides — strona 523

Edge-R1#show ip nat statistics
Two commands can be used to fully Total translations: 5 (1 static, 4 dynamic, 4 extended)
verify a NAT operation.
Hits: 5 Misses: 13
The command Expired translations: 1
displays NAT parameter and pool Dynamic mappings:
configuration, pool status, and -- Inside Source
interface configuration. access-list 1 pool ToFreedom refCount @
phe t ic, total add 1, allocated @ (0%), mi 8
command shows the active NAT ype generic, total addresses 1 , allocate (0%), misses
abated (inside local a i Edge-Ri#show ip nat translations
plobaladdress palting, when they Pro Inside global Inside local Outside local Outside global
occur). --- 209.15.10.1 10.0.0.10 --- ---
tcp 209.15.10.1:50016 10.0.0.10:50016 8.8.8.8:53 8.8.8.8:53
Note: Static NAT translation is always tcp 209.15.10.1:50017 10.0.0.10:50017 200.10.0.254:80 200.10.0.254:80
shown in the table. tcp 209.15.10.1:50018 10.0.0.20:50018 157.160.27.8:80 157.160.27.8:80
tcp 209.15.10.1:50019 10.0.0.20:50019 82.11.0.2:443 82.11.0.2:443


### Slides — strona 524

d f 9 rd ; - * 5 y A ~ - ‘
g 1 ’ (fp ee .

# . ~<e "SEG fas f
i < ‘ hs, < : *, pd y
OS ~ a . > > SS
SS errs. \ <i -—~ ~ u
' SISOS \ ~~

Conk ; > ~~

' Cea SD 2 .——

ys \. y 7 . =

Tim By a . i

>. ye Cy fan. a ae


### Slides — strona 525

aul egal 5 i 2B
—— — Sy " : ™ ty .
ie. = 4 a wet, NETWORK ga Cm D
