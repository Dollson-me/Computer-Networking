# NET-07-LS1 — Configuring IPv4 Static and Default Routes

[← Wszystkie laboratoria](index.md)

> **Typ:** laboratorium z rozwiązaniem. Zachowano wszystkie kroki, pytania, odpowiedzi, komendy i wartości z materiału źródłowego; usunięto jedynie techniczne nagłówki stron OCR.

## Powiązana teoria

- [Router operation and static routing concepts](../05-addressing-routing/router-operation.md)
- [IPv4 static and default routing](../05-addressing-routing/static-routing-ipv4.md)

## Pełny przebieg laboratorium

> Zakres źródłowy: strony 169–186.

Computer Networking
Lab Assignment IPv4 & IPv6 Static
& Solution Routing
RO isis, NET-O7-LS1
olf Configuring IPv4 Static
re U and Default Routes
Copyright © 1996-2020 HackerU Ltd.
All Rights Reserved.

Note: Solutions for the instructor are shown inside the green box.
G Lab Objective
Understand how static and default routes can be used to connect multiple networks,
and the routing methods used to configure routers.
5) Lab Mission
Interconnect three LANs, and connect them to an external network using IPv4
addressing.
ea .
©) Lab Duration
30-60 minutes
fe Requirements
e Knowledge of basic IOS commands and navigation.
e Familiarity with routing concepts.
e Basic understanding of subnetting.
Lt

[ea] Resources
¢ Environment & Tools

All platforms

Cisco Packet Tracer 7.2.2 or higher
e Files

NET-07-L1.pka

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
PKA features
Note the following essential information regarding the Activity window:
1. Completion Percentage — Student progress appears at the bottom right corner of
the window.
2. Check Result Button — When you click this button and then click the "Assessment
Items" tab, you will find a checklist with lab objectives and status, whereby V=done,
X=not done.
Note: Both features help the instructor grade the exercise swiftly and efficiently.

A PT Activity: 001012 - ao x ‘Expandialapas Al| Show incase Rena)

Please fr othe exer document an cea allo the fener [Saas Pas Compaen) [Feeick

‘See the percentage of completion at the right-bottom corner to E-NTP Sener o ‘Other

determine your progress. 5 NIP Sener o Other

Note: The Optional and Bonus section are not scored, eo mnie : »

Good Luck Vie ° ier
PKA Solution
To view the solution or edit the lab file, you can simply click the "Wizard hat" icon and
enter the following password: C!S$cOM@ster
Right-click the "Answer network" tab and then click "Show Answer network".
Note: Be careful not to change anything so that the lab will remain intact.

Lab Task 1: Revision Questions
Answer the review questions below regarding routing.
1 What is the difference between standard and default static routes?
Standard static route - Manually configured route that forwards traffic to a specific
network.
Default static route — Handles all packets that don't have a destination route in the
routing table.
2 Which command displays a routing table?
3 In the routing table which letters represent a static route and default static route?
S-Static / S*-Default Static
4 What is the default administrative distance of a static route?
Administrative Distance = 1
5 Bonus: Name two advantages of static routing (as opposed to dynamic routing)?
Static Route advantages:
e Static routing consumes minimal resources. No algorithms mean no overhead on the
router CPU, and no dynamic updates means no extra bandwidth is being used.
e The path a packet takes between two destinations is predictable, which allows more
control over the data flow.

Lab Task 2: Configure IPv4 Standard Routes
Learn how to use |Pv4 to set up routes between the three LANs and the external
network using different routing methods.
192.168 0.64/26 210.10.10.0/30
a ¢ ( <sym, G Se Ss
192 168.0.192/30 192.168.0.196/30
192.168.0.0/26 ag Ny 192.168.0.128/26
hi WE ne (gael ae f F
ee ae So “a...
—_. 2960-26TT 4944 4941 2960-24TT =
Part 1: Configure Directly-Connected Static Routes on R1
1 Open PC1 and try to ping PC2. The ping will not be successful, which can be seen
by showing the R1 routing table and noting that the 192.168.0.64/26 network is
missing.
R1>enable
Rl#show ip route
IC:\>ping 192.168.0.66
Pinging 192.168.0.66 with 32 bytes of data:
Reply from 192.168.0.1: Destination host unreachable.
Reply from 192.168.0.1: Destination host unreachable.
Reply from 192.168.0.1: Destination host unreachable.
Reply from 192.168.0.1: Destination host unreachable.
Ping statistics for 192.168.0.66:
Packets: Sent = 4, Received = 0, Lost = 4 (100% loss),

Bi> Ts
Ri>enable
Rl#show ip route
Codes: L - local, C - connected, 5 - static, R - RIP, M — mobile,
B - BGP
D - EIGRP, EX - EIGRP external, © - OSPF, IA - OSPF inter
area
Nl - OSPF NSSA external type 1, N2 - OSPF NSSA external
type 2
El - OSPF external type 1, £2 - OSPF external type 2, © -
EGP
i - IS-IS, Ll - IS-I5 level-1, Lz - 15-15 level-2, ia -
IS-IS inter area
* — candidate default, U - per-user static route, o — ODR
P - periodic downloaded static route
Gateway of last resort is not set
152.168.0.0/24 is variably subnetted, 4 subnets, 3 masks
c 192.168.0.0/26 is directly connected, GigabitEthernetd/o
L 192.168.0.1/32 is directly connected, GigabitEthernet0/0
is 192.168.0.192/30 is directly connected, Serial0/0/0
L 192.168.0.193/32 is directly connected, Serial0/o/0
R1F| we
2 How many networks are directly connected to each router? (Excluding the
210.10.10.0 network.) Hint: Use show ip route, to check.
R1# show ip route
Directly connected networks:
R1-2
R2-3 (4, including the external network)
R3-2

3 OnR1, configure a directly-connected standard static route to every network not
directly connected to R1 (excluding the 210.10.10.0 network).
Note: When configuring directly-connected static routes, the router will issue a
warning, which you can ignore, because this is a point-to-point connection.
Tip: To simplify the process, go to “Options” in the Packet Tracer menu, select
“Preferences...”, and select “Always Show Port Labels in Logical Workspace” to
display the port names.
Ri#config terminal
R1(config)#ip route 192.168.0.64 255.255.255.192 serial 0/0/0
R1(config)#ip route 192.168.0.128 255.255.255.192 serial 0/0/0
R1(config)#ip route 192.168.0.196 255.255.255.252 serial 0/0/®
R1(config)#exit
WP Cinco Packet Tracer - ao x
File Edit Options | View Tools Extensions Help
. Preferences .. CHR = =
Beats om § + QR ES 2
= Algorithm Settings CrlvShiteM
TQ Disease cosy (a4 ia re
Cater) — Physical)x esa y: 125 Root) LC 035400)
192168.0 6426 210.10.10.030
Cap
pcer arial ~~ Intemet
182.168.0.1920 192 168.0.196/30
=. 2960-2477 2960-241 5
<< Es > if
Time: 00:035a( > )(_) (Q Reaitime] Simulation]
SIE Ss MP OGEGoeoseoaaancoce
=| 4331 4321 1941 2901 2911 B1910X BISHGW _ 829 1240 PrROUE PrEmpty _ 1841 at a
== & >|
Boe a fe ee

®
intraca’ |sbaresttee [ine [Font | Miscekareos | Anewver Tues [|(Coston inevieene | Pubtoher! [Gnas Caste
customize User Experience
© Show Animation © Show Link Lights
Olay Sound © Play Telephony Sound
‘Show Device Medel Labels ‘Show QoS Stamps on Packets
[2 Show Device Name Labels Show Port Labels When Mouse Over in Logical Workspace
[Enable Cable Length Ect
ODisable Auto Cable C1 Use CLI as Device Default Tab
Use Matric System (Uncheck to use Imperial) EZ Show Cable info Popup in Physical Workspace
TD Align logical workspace objects DAlion physical workspace objects
4 Display the R1 routing table to verify all static route configurations.
Hint: Use the keyword static at the end of the show ip route command to display
only the static routes.
Rl#show ip route static
Rl#show ip route static
192.168.0.0/24 is variably subnetted, 7 subnets, 3 masks
Ss 192.168.0.64/26 is directly connected, Serial0/0/0
8s 192.168.0.128/26 is directly connected, Serial0/0/0
5 192.168.0.196/30 is directly connected, Serial0/0/0
Rl# heat
Part 2: Configure Next-Hop Static Routes on R2
General hint: Use show ip interface brief to view IP addresses on the routers.
5 On Rz2, configure a next-hop standard static route for every network not directly
connected to R2 (excluding the 210.10.10.0 network).
R2>enable
R2>conf t
R2(config)#ip route 192.168.0.@ 255.255.255.192 192.168.0.193
R2(config)#ip route 192.168.0.128 255.255.255.192 192.168.0.198
R2(config)#exit

6 Display the R2 routing table to verify all static route configurations.
R2#show ip route static
R2#show ip route static
192.168.0.0/24 is variably subnetted, & subnets, 3 masks
5 192.168.0.0/26 [1/0] via 192.168.0.193
s 192.168.0.128/26 [1/0] via 192.168.0.198
R2# ng
Part 3: Configure Directly-Connected Static Routes on R3
7 OnR3, configure a directly-connected standard static route for every network not
directly connected to R3 (excluding the 210.10.10.0 network).
R3>enable
R3#conf t
R3(config)#ip route 192.168.0.@ 255.255.255.192 serial @/0/1
R3(config)#ip route 192.168.0.64 255.255.255.192 serial @/0/1
R3(config)#ip route 192.168.0.192 255.255.255.252 serial 0/@/1
R3(config)#exit
R3(config)#ip route 192.168.0.64 255.255.255.192 serial 0/0/1
Default route without gateway, if not a point-to-point
interface, may impact performance
R3(config)#ip route 192.168.0.0 255.255.255.192 serial 0/0/1
&Default route without gateway, if not a point-to-point
interface, may impact performance
R3(config)#ip route 192.168.0.192 255.255.255.252 serial 0/0/1
Default route without gateway, if not a point-to-point
interface, may impact performance
R3 (contig) #| Re
8 Display the R3 routing table to verify all static route configurations.
R3#show ip route static
R3#show ip route static
192.168.0.0/24 is variably subnetted, 7 subnets, 3 masks
5 192.168.0.0/26 is directly connected, Serial0/0/1
& 192.168.0.64/26 is directly connected, Serial0/0/1
5 192.168.0.192/30 is directly connected, Serial0/0/1
R3#| w

Step 4: Verify Connectivity
9 From PC1, ping PC2 and PC3. All pings should be successful.
C:\>ping 152.168.0.66
Pinging 192.168.0.66 with 32 bytes of data:
Request timed out.
Reply from 192.168.0.66: bytes=32 time=lms TITL=126
Reply from 192.168.0.66: bytes=32 time=2ms TIL=126
Reply from 152.168.0.€6: bytes=32 time=lms TIL=126
Bing statistics for 192.168.0.66:
Packets: Sent = 4, Received = 3, Lost = 1 (25% loss),
Approximate round trip times in milli-seconds:
Minimum = lms, Maximum = ims, Average = lms
10 Use the tracert command on PC1 to view the path of the packets to PC2.
C:\>tracert 192.168.0.66
Tracing route to 192.168.0.66 over a maximum of 30 hops:
1 0 ms O ms O ms 192.168.0.1
2 0 ms 1 ms 1 ms 192.168.0.194
3 2 2 ms 0 ms 192.168.0.66
Trace complete.

Lab Task 3: Configure IPv4 Default Routes
Connect to the external network using default routes.

1 From PC1, try to ping an external resource 8.8.8.8 server. The ping will not be
successful because the routers do not know where to forward unknown external
network traffic.

Display the R1 routing table and verify that the “Gateway of last resort” option is
not set.
R1>enable
Rl#show ip route
C:\>ping 8.8.8.8
Pinging §.8.8.8 with 32 bytes of data:
Reply from 192.168.0.1: Destination host unreachable.
Reply from 192.168.0.1: Destination host unreachable.
Reply from 192.168.0.1: Destination host unreachable.
Reply from 192.168.0.1: Destination host unreachable.
Ping statistics for 8.8.8.8:
Packets: Sent = 4, Received = 0, Lost = 4 (100% loss),

Rl#show ip route tal
Codes: L - local, C - connected, 5 - static, R - RIP, M - mobile,
B - BGP

D - EIGRP, EX - EIGRP external, © - OSPF, IA - OSPF inter
area

Nl - OSPF NSSA external type 1, N2 - OSPF NSSA external
type 2

El - OSPF extermal type 1, E2 - OSPF external type 2, E -—
EGP

i - IS-IS, Ll - IS-IS level-1, L2 - IS-IS level-2, ia -
Is-IS inter area

* — candidate default, U - per-user static route, o - ODR

P - periodic downloaded static route

192.168.0.0/24 is variably subnetted, 7 subnets, 3 masks
c 192.168.0.0/26 is directly connected, GigabitEthernet0/0
L 192.168.0.1/32 is directly connected, GigabitEthernet0/0
s 192.168.0.64/26 is directly connected, Serialo/o/o
s 192.168.0.128/26 is directly connected, Serialo/o/o
c 192.168.0.192/30 is directly conmected, Serialo/o/o
L 192.168.0.193/32 is directly connected, Serialo/o/o
s 192.168.0.196/30 is directly connected, Serialo/o/o @

2 OnR1, configure a (directly-connected) default route towards the Internet. Use
the outgoing interface that is in the direction of the Internet.
R1#conf t
R1(config)#ip route 0.0.0.0 0.0.0.® serial 0/0/20
R1(config)#exit
Rl (config)#ip route 0.0.0.0 0.0.0.0 serial 0/o/0
Default route without gateway, if not a point-to-point
interface, may impact performance
R1 (config) #| Mm
3 Display the routing table on R1, and verify that the “Gateway of last resort” is set
and the new default route is listed below.
Rl#show ip route
Rl#show ip route a
Codes: L - local, C - connected, 5 - static, R - RIP, M - mobile,
B - BGP
D - EIGRP, EX - EIGRP external, © - OSPF, IA - OSPF inter
area
Nl - OSPF NSSA external type 1, N2 - OSPF NSSA external
type 2
El - OSPF external type 1, E2 - OSPF external type 2, E -—
EGP
i - IS-IS, Ll - I5-IS level-1, L2 - I5-IS level-2, ia -
Is-IS inter area
* — candidate default, U - per-user static route, o - ODR
P -— periodic downloaded static route
192.168.0.0/24 is variably subnetted, 7 subnets, 3 masks
c 192.168.0.0/26 is directly connected, GigabitEthernet0/0
L 152.168.0.1/32 is directly connected, GigabitEthernet0/0
S 192.168.0.64/26 is directly connected, Serial0/0/0
ed 152.168.0.128/26 is directly connected, Serial0/0/0
c 192.168.0.192/30 is directly connected, Serial0/0/0
L 152.168.0.193/32 is directly connected, Serial0/0/0
s eo é nat oppected Serial /o/o

4 Repeat steps 2 and 3 on R2 and R3.
R2#conf t
R2(config)#ip route 0.0.0.0 0.0.0.0 serial 0/1/0
R2(config)#do show ip route static
R3#conf t
R3(config)#ip route 0.0.0.0 0.0.0.0 serial 0/0/1
R3(config)#do show ip route static
sDefault route without gateway, 1f not a point-to-point
interface, mg DDS, perform =
R2 (config)
192.168.0.0/24 is variably subnetted, & subnets, 3 masks
EI 192.168.0.0/26 [1/0] via 192.168.0.193
a 192.168.0.128/26 [1/0] via 192.168.0.198
a* 0.0.0.0/0 is directly connected, Serial0/1/0
R2 (config) # be
SDefault route withoue Gateuay, 2 NOt a Pein’ bo point
interface, may impact performance
192. 188-0 Oot ae variably sebnetted, 7 subnets, 3 masks
= 192.168.0.0/26 is directly connected, Serial0/0/1
5 192.168.0.64/26 is directly connected, Serial0/0/1
s 192.168.0.192/30 is directly connected, Serial0/0/1
Ei 0.0.0.0/0 is directly connected, Serial0/0/1
R3 (config) 4 MM

5 From PC1, PC2, and PC3, try to ping the 8.8.8.8 server again and observe the
results.
Pinging 8.8.8.8 with 32 bytes of data:
Reply from 8.8.8.8: bytes=32 time=2ms TTL=253
Reply from 8.8.8.8: bytes=32 time=3ms TTL=253
Reply from 8.8.8.8: bytes=32 time=2ms TTL=253
Reply from 8.8.8.8: bytes=32 time=2ms TTL=253
Ping statistics for 8.8.8.8:
Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),
Approximate round trip times in milli-seconds:
Minimum = 2ms, Maximum = 3ms, Average = 2ms
6 Use the tracert command on PC1 to view the path of the packets to the 8.8.8.8

server.
C:\>tracert 8.8.8.8
Tracing route to 8.8.8.8 over a maximum of 30 hops:

il 1 ms 1 ms 0 ms 192.168.0.1

2 1 tis O ms 1 ms 192.168.0.194

3 1 ms 0 ms 0 ms 8.8.8.8
Trace complete.

Lab Task 4 (Optional): Configure IPv4 Summary Route
Check to see if a routing table has routes that can be summarized, and replace those
routes with a summarized route.

1 __ Display the R1 routing table and note the remote network address and outgoing
interface configured for all. The network partition and interface are identical. This
means this is a proper situation for a summary setup.

R1(config)#do show ip route static
R1 (config) #do show ip route static
192.168.0.0/24 is variably subnetted, 7 subnets, 3 masks
a 192.168.0.64/26 is directly connected, Serial0/0/0
ES 192.168.0.128/26 is directly connected, Serial0/0/0
Ss 192.168.0.196/30 is directly connected, Serial0/0/0
5 0.0.0.0/0 is directly connected, Serial0/0/0
Rl (config) # ae
2 Erase the standard static route configuration.
R1(config)#no ip route 192.168.0.64 255.255.255.192 serial 0/0/®
R1(config)#no ip route 192.168.0.128 255.255.255.192 serial 0/0/20
R1(config)#no ip route 192.168.0.196 255.255.255.252 serial 0/0/0
aE COREETTY
Ri(config)#nqj ap routef192.168.0.64 §55.255.255.1929 serial 0/0/0
Ri (config) #ngj ip route9}192.168.0.128§255.255.255.19% serial 0/0/0
Ri(config)#noj ip routef[192.168.0.196§255.255.255.25§ serial 0/0/0
Rl (contig) # =
3 Summarize networks into a single address and mask, as follows:
Step 1 - List the 192.168.0.X networks in binary format.
Summary steps:
192.168.0.64 -11000000.10101000.90000000.01000000
192.168.0.128-11000000.10101000. 20000000 .10000000
192.168.0.196-11000000.10101000 . 920000000.11000100
Step 2 - Count the number of far-left matching bits to determine the mask for the
summary route. The 24 far-left matching bits constitute the prefix, or subnet
mask, for the summarized route.

Step 3 - Copy the matching bits and add zero bits to determine the summarized
network address. The matching bits with zeros at the end result in the
summarized network address.
New address:
192.168.0.0 - 11000000.10101000. 200000000 .2e0000000
New mask:
255.255.255.@ 11111111. 11111111. 11111111.eeee0e00ee
4 Configure the new summary network and subnet mask using next-hop or directly-
connected.
R1(config)#ip route 192.168.0.@ 255.255.255.@ serial 0/0/0
Ri (config) #ip route 192.168.0.0 255.255.255.0 serial 0/0/0
5 _ Display the R1 routing table and verify the new summary route.
R1(config)#exit
Rl#show ip route static
192.168.0.0/24 is variably subnetted, @ subnets, 4 masks
s 192.162.0,0/24 as dizectly connected, Serial0/0/0
s 192 .168.0.€4/2€ is directly connected, Serial0/0/0
8 192.168.0.128/2€ is directly connected, Serial0/0/a
s 192.162.9,15¢/30 is directly connected, serialo/o/0
S* 0.0.0.0/0 is directly connected, Serial0/0/0

6 From PC1, ping PC2 and the 8.8.8.8 server to verify connectivity.

C:\>ping 192.168.0.66
Pinging 192.168.0.66 with 32 bytes of data:
Request timed out.
Reply from 192.168.0.66: bytes=32 time=l2ms TTL=126
Reply from 192.168.0.66: bytes=32 time=lms TTL=126
Reply from 192.168.0.66: bytes=32 time=1ms TTL=126
Ping statistics for 192.168.0.66:

Packets: Sent = 4, Received = 3, Lost = 1 (25% loss),
Approximate round trip times in milli-seconds:

Minimum = lms, Maximum = 12ms, Average = 4ms
Ci\>ping 8.8.8.8
Pinging 8.8.8.8 with 32 bytes of data:
Reply from 8.8.8.8: bytes=32 time=2ms TTL=253
Reply from 8.8.8.8: bytes=32 time=2ms TTL=253
Reply from 8.8.8.8: bytes=32 time=2ms TTL=253
Reply from 8.8.8.8: bytes=32 time=2ms TTL=253
Ping statistics for 8.8.8.8:

Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),
Approximate round trip times in milli-seconds:

Minimum = 2ms, Maximum = 2ms, Average = 2ms
