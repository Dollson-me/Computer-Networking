# NET-05-LS3 — Configure IPv6 Addressing

[← Wszystkie laboratoria](index.md)

> **Typ:** laboratorium z rozwiązaniem. Zachowano wszystkie kroki, pytania, odpowiedzi, komendy i wartości z materiału źródłowego; usunięto jedynie techniczne nagłówki stron OCR.

## Powiązana teoria

- [IPv6 addressing](../05-addressing-routing/ipv6.md)

## Pełny przebieg laboratorium

> Zakres źródłowy: strony 148–160.

Computer Networking
Lab Assignment IP & Routing
& Solution Concepts
RO isis, NET-05-LS3
ol Configure IPv6 Addressing
Es}
Copyright © 1996-2020 HackerU Ltd.
All Rights Reserved.

Note: Solutions for the instructor are shown inside the green box.
G Lab Objective
Become familiar with IPv6 addressing and how to configure a network to use IPv6.
%) Lab Mission
Configure a router to connect two LANs using IPv6 addresses, then use troubleshooting
techniques to verify connectivity.
Note: All the required commands were introduced in the presentation, and can also be
found in the textbook.
C2 7
@) Lab Duration
30-60 minutes
fe Requirements
e Knowledge of basic IOS commands and navigation.
e Knowledge of IPv6.
Lt

[ea] Resources
¢ Environment & Tools

All platforms

Cisco Packet Tracer 7.2.2 or higher
e Files

NET-05-L3.pka

Instructions for PKA Lab Files
Lab material includes the lab document and a PKA lab file.
Open the pka file through the Cisco Packet Tracer menu by clicking "File", and then
"Open...".
bw ae 2 QQQ0R Ese 2
Bran ome ore)
Open Acti Seance ae 04039)
Print CuleP
ed
Navigate to the file's location and open it.
a
a A t)
a
a
a
-
a
i
i
1
lena [NE-03 La Se

Note: Double-clicking the pka file in your file explorer may not work (depending on the
Packet Tracer version).
Lab material includes the lab document and a PKA lab file.
When you open a PKA file in Cisco Packet Tracer, two windows appear:
1. Lab topology window
2. Activity window
PKA Features
Note the following essential information regarding the Activity window:
1. Completion Percentage — Student progress appears at the bottom right corner of
the window.
2. Check Result Button — When you click this button and then click the "Assessment
Items" tab, you will find a checklist with lab objectives and status, whereby V=done,
X=not done.
Note: Both features help the instructor grade the exercise swiftly and efficiently.

reas refer to the exercise document and carefully folow the aes = fae ca ee

‘See the percentage of completion at the right-bottom corner to = NTP Sener 0 Other

determine your rome, 2 NP See H ote

Note: The Optional and Bonus section are not scored. cet Smee Incamet 1 »
PKA Solution
To view the solution or edit the lab file, you can simply click the "Wizard hat" icon and
enter the following password: C!ScOM@ster
Right-click the "Answer network" tab, and then click "Show Answer network".
Note: Be careful not to change anything so that the lab will remain intact.

Lab Task 1: IPv6 Revision Questions
Refresh you IPv6 skills with practice questions.

1 = Howlong is an IPv6 address in bits?
128 bits.

2 What is the corresponding IPv6 term for an IPv4 octet?

3 Name two IPv6 Unicast address types.
IPv6 Unicast types:
Global Unicast (the equivalent of an IPv4 public address).
Link-local FE80::/10 (the equivalent of an IPv4 APIPA address).
Loopback ::1/128 (the equivalent of an IPv4 loopback address).
Unique-local FCO0::/7 (the equivalent of an IPv4 private address).

4 What is the default suffix of an IPv6 address?

5 What are the three parts of an IPv6 with a suffix of /64?
The three parts are:
First 45 bits (3 Hextets) - Global routing prefix, global identifier.
First 16 bits (1 Hextet) - Subnet ID, network identifier.
Last 64 bits (4 Hextets) - Interface ID, host identifier.

Page5

Lab Task 2: Configure IPv6
Establish a functional network using only IPv6 addressing.
Issue all commands on R1:
Part 1: Configure IPv6 Unicast Global address on R11 interfaces:
1 InR1, enter Global Configuration mode.
R1>enable
Rl#config terminal
R1(config)#
2 |Pv6is installed on every router, but not enabled by default. The ipv6 unicast-
routing command must be run to enable IPv6 packet forwarding on R1.
Note: In IPv6, all addresses are valid for configuration, including the first and last
addresses, unlike in IPv4.
R1(config)#ipv6 unicast-routing
3 Enter interface gigabitEthernet 0/0 and configure the first IP address in the range
(2001:CAFE:ABCD:1::) with a suffix of 64, according to the IP documentation in
the topology.
R1(config)#interface gigabitethernet 0/0
R1(config-if)#ipv6é address 2001:cafe:abcd:1::/64
R1(config-if)#exit
R1(config)#

4 Repeat the previous step for gigabitEthernet 0/1 with the corresponding
network (2001:CAFE:ABCD:2::), also using suffix 64.
R1l(config)#interface gigabitethernet 0/1
R1(config-if)#ipv6 address 2001:cafe:abcd:2::/64
R1(config-if)#exit
R1(config)#
5 Enable both interfaces.
R1(config)#interface range gigabitethernet 0/0-1
R1(config-if-range)#no shutdown
R1(config-if-range)#exit
R1(config)#exit
6 Verify the R1 interface using show ipv6 interface brief.
Note: All Cisco commands that contain “IP” relate to IPv4. There are different
commands for IPv6.
Rl#show ipv6 interface brief
Ri¢show ipvé interface brief
GigabitEthernet6/0 {up/up]
FE&0: :203:E4FF: FESB:3456
2001:CAFE:ABCD:1::
GigabitEthernet6/1 {up/up]
FES80: :201:C9FF:FESS:1B97
2001:CAFE:ABCD:2::
Vlanl [administratively down/down]
unassigned
R1#| nd

Part 2: Configure IPv6 on User PCs and Verify Connectivity
7 Click User1, and then click the Desktop tab.
8 Click the IP configuration icon.
9 Configure the IPv6 address 2001:CAFE:ABCD:1::1 with a suffix of 64.
Note: Leave the link local address as is.
10 Configure the default gateway address of the network.
Physical —Conig_Desitop_ Progamming _Atitutes
TP Contguraion
© pHer @ Static
Padres
Sabre Mask i
Dea Gaeny foo CCS
IP Corfgaton
© pxcp O Auto Config @ Sialic
Ps Adress fmoredeaet? SSS
AE DNS Sener
11 Configure the IPv6 address 2001:CAFE:ABCD:1::2 with a suffix of 64. In addition,
configure the appropriate default gateway address.
Note: Leave the link local address as is.
User2
IPV6 Configuration
© pxcp © Auto Contig @ Static
Pw Address [povtceeateet2 S™~CS~SSCSCS*«dS
Ling Local Adcress [Feezovcerrreszee 2 OOSO~<—~sSsSY
Py Gateway
PW DNS Sener (

12 Repeat steps 8 to 10 for User3 and User4.
For User3, configure the IPv6 address 2001:CAFE:ABCD:2::1
For User4, configure the IPv6 address 2001:CAFE:ABCD:2::2
For both User3 and User4, set the appropriate default gateway and leave the
link local address as is.
User3
Fr Corton
) DHCP © Auto Config @ Static
Preaddoss 2
Link Local Adress [Few-aotwrresoaas
1PA6 Gateway [2o0ricafe.abed 2
V6 ONS Sonor CO]
User4
1x6 Contuaton
IP Akiess EC
16 Gateway Boies etese
(PW ONS Sener Cr
13 Ping the default gateway to make sure there is connectivity with the router.
User1 to default gateway (giga 0/0)
Pinging 2001:cafe:abed:1:: with 32 bytes of data:
Reply from 2001:CAFE:ABCD:1::: bytes=32 time<lms TTL=255
Ping statistics for 2001:CAFE:ABCD:1:::
Minimum — Oms, Maximum — Ims, Average - oms
14 Ping User2 to verify connectivity on the internal network.
User1 to User2
c:\>ping 2001:cafe:abed:1::2
Reply from 2001:CAFE:ABCD:1::2: bytes=32 time<lms TTL=128
Reply from 2001:CAFE:ABCD:1::2: bytes-32 time-Ims TTL=128
Ping statistics for 2001:CAFE:ABCD:1::2:
Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),

15 Repeat steps 13 and 14 for User3, so it will ping its default gateway and User4.
User3 to default gateway (giga 0/1)
c:\>ping 2001:cafe:abcd:23:
Pinging 2001:caferabed:2:: with 32 bytes of data:
ping statistics for 2001:CAFE:ABCD:2:::
Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),
Approximate round trip times in milli-seconds:
User3 to User4
Reply from 2001:CAFE:ABCD:2::2: bytes=32 time=Ims TTL=128
Reply from 2001:CAFE:ABCD:2::2: bytes=32 time<lms TTL=128
Reply from 2001:CAFE:ABCD:2::2: bytes=32 time<lms TTL=128
Reply from 2001:CAFE:ABCD:2::2: bytes=32 time<lms TTL=128
Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),
16 Ping User3 from User1 to verify connectivity between the networks.
Note: Don’t use the envelope tool, since it does not work properly with IPv6.
User1 to User3
approximate round trip times in milli~seconds:

Part 3 (Optional): Configure IPv6 Link-local Address on R1 Interfaces and PCs
Except for the IPv6 global address, devices using IPv6 need IPv6 link-local addresses.
Devices use this kind of address to communicate with other hosts on the local network
segment only, and must be unique only for that particular network segment. The link-
local address is assigned automatically using a random or EUI-64 process, meaning they
are long and not easy to remember. A technician can assign a simpler address
manually.
17 Configure the FE80::1 link-local address on both interfaces of R1. The command
to use is ipv6 address fe80::1 link local
Verify the configuration with the command show ipv6 interface brief
R1(config)#interface gigabitethernet 0/0
R1(config-if)#ipv6 address fe8@::1 link-local
R1(config-if)#exit
R1l(config)#interface gigabitethernet 0/1
R1(config-if)#ipv6 address fe8@::1 link-local
R1(config-if)#exit
R1(config)#exit
Rl#show ipv6 interface brief
Rl#show ipv6é interface brief
GigabitEthernet0/0 (up/up]
a TCA tABCD:1::
Giggp berneto/1 (up/up]
2001:CAFE:ABCD:2::
Vlanl [administratively down/down]
unassigned
18 Configure the FE80::2 link-local address on User1.

19 Configure the FE80::3 link-local address on User2.
|Pv6 Configuration
© pHcP O Auto Config ® Static
Pas Address foorcarenscot2 =i —id
Link Local Address
a6 Gateway [oorcareaccot; SS~S~S~S~™d:
Pv DNS Server |
20 Repeat steps 18 and 19 on User3 and User4.
For User3, set the IPv6 address FE80::2
For User4, set the IPv6 address FE80::3
IPv6 Configuration
© bHeP © Auto Config @ Static
IPv6 Address [2001:CAFE-ABCD:2::1 | 1 [64 ]
Link Local Address [FE80::2 ]
IPv6 Gateway '2001:CAFE:ABCD:2: |
IPv6 DNS Server
IPv6 Configuration
© DHeP © Auto Config @ Static
IPA6 Adress foorcareanco22 —=«di (eid
Link Local Address FE80:-3
IPv6 Gateway |2001:CAFE:ABCD:2:
IPv6 DNS Server
21 From User1, ping the default gateway and User2 link-local addresses to verify
connectivity.
Userl to default gateway
Pinging feg0::1 with 32 bytes of data:
Reply from FE80::1: bytes=32 time=Ims TTI=255
Reply from FE80::1: bytes=32 time<lms TTI=255
Reply from FE80::1: bytes=32 time<Ims TTL=255
Reply from FE80::1: bytes=32 time<lms TTI=255
Ping statistics for FE80::1:
Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),
Approximate round trip times in milli-seconds:
Minimum = Oms, Maximum = lms, Average = Oms
Userl to User2

Ic:\>ping fe80::3
Reply from FE80::3: bytes=32 time=lms TIL=128
Reply from FE80::3: bytes=32 time<lms TTL=128
Reply from FE80::3: bytes=32 time<lms TTL=128
Reply from FE80::3: bytes=32 time<lms TTL=128
Ping statistics for FE80::3:
Packets: Sent = 4, Received = 4, Lost = 0 (0%
loss),
lapproximate round trip times in milliseconds:
Minimum = Oms, Maximum = lms, Average = Oms
22 Repeat the previous step for User3.
Pinging fe80::1 with 32 bytes of data:
Reply from FE80::1: bytes=32 time<lms TTL=255
Reply from FF80::1: bytes=32 time<lms TTL=255
Reply from FE80::1: bytes=32 time<lms TTL=255
Reply from FE80::1: bytes=32 time=lms TTL=255
Ping statistics for FE80::1:
Packets: Sent - 4, Received - 4, Lost = 0 (0% loss),
Approximate round trip times in milli-seconds:
Minimum = Oms, Maximum = lms, Average = Oms
C:\sping feg0::3
Pinging £80::3 with 32 bytes of data:
Reply from FE80::3: bytes-32 time<lms TTL=128
Reply from FE80::3: bytes=32 time<lms TTL=128
Reply from FE80::3: bytes-32 time<lms TTL=123
Reply from FE80::3: bytes=32 time<ims TTL=128
Ping statistics for FE8Q::3:
Packets: Sent = 4, Received = 4, Lost = 9 (0% loss),
Approximate round trip times in milli-seconds:
