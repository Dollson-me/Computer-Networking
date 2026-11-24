# NET-08-LS1 — Configuring and Verifying RIPv2

[← Wszystkie laboratoria](index.md)

> **Typ:** laboratorium z rozwiązaniem. Zachowano wszystkie kroki, pytania, odpowiedzi, komendy i wartości z materiału źródłowego; usunięto jedynie techniczne nagłówki stron OCR.

## Powiązana teoria

- [Dynamic routing concepts](../05-addressing-routing/dynamic-routing-concepts.md)
- [RIPv2](../05-addressing-routing/ripv2.md)

## Pełny przebieg laboratorium

> Zakres źródłowy: strony 187–202.

Computer Networking
Lab Assignment Dynamic Routing
& Solution
NET-08-LS1
i Configuring and
oe ni Verifying RIPv2
EI
Copyright © 1996-2020 HackerU Ltd.
All Rights Reserved.

Note: Solutions for the instructor are shown inside the green box.
G Lab Objective
Implement dynamic routing using RIP. RIP is a straightforward protocol that helps
the user understand basic network routing. However, it is no longer a commonly
used protocol.
») Lab Mission
Configure RIPv2 to connect all networks, and use it to propagate the network with a
default route, allowing the WAN to connect to an external network.
CN) 7
©) Lab Duration
30 minutes—1 hour
{fe Requirements
e Knowledge of basic IOS commands and navigation.
e Familiarity with routing concepts.
e Basic understanding of subnetting.
on

| Resources
¢ Environment & Tools

All platforms

Cisco Packet Tracer 7.2.2 and higher
e Files

NET-08-L1.pka

Instructions for PKA Lab Files
Lab material includes the lab document and a PKA lab file.
Open the PKA file through the Cisco Packet Tracer menu by clicking "File" and then
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

Note: Double-clicking the PKA file in your file explorer may not work (depending on the
Packet Tracer version).
Lab material includes the lab document, and a PKA lab file.
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

A PT Activity: 001012 - ao x ‘Expandialapas Al| Show incase Rena)

Please fr othe exer document an cea allo the fener [Saas Pas Compaen) [Feeick

‘See the percentage of completion at the right-bottom corner to E-NTP Sener o ‘Other

determine your progress. 5 NTP Sener o Other

Note: The Optional and Bonus section are not scored, eo mnie : »

Good Luck Vie ° ier
PKA Solution
To view the solution or edit the lab file, you can simply click the "Wizard hat" icon and
enter the following password: C!S$cOM@ster
Right-click the "Answer network" tab and then click "Show Answer network".
Note: Be careful not to change anything so that the lab will remain intact.

Lab Task 1: Revision Questions
Refresh your knowledge of routing protocols and RIP.
1. What is the default Administrative Distance value of RIP?
AD=120
2 What route source letter represents an RIP route in the routing table?
3. Whatare the default Hello and Hold intervals of RIP?
Hello is 30 seconds, Hold is 180 seconds
4 From which version of RIP VLSM is authentication supported?

Lab Task 2: Configure RIPv2
Configure RIPv2 so that all networks are connected, and verify the connectivity.
Part 1: Enable and configure RIP on the routers
1 Enter R1 global configuration mode and implement the following settings:
a) Enable RIP.
b) Set version 2.
c) Configure all local networks connected to R1 to be used by RIPv2.
Hint: Use Show ip route connected to view the local networks and
prefixes.
d) Disable auto-summarization.
e) Configure a passive-interface on the appropriate interface.
2 Save the configuration.
R1> enable
Ri#configure terminal
R1(config)#router rip
R1(config-router)#version 2
R1(config-router)#do show ip route connected
R1(config-router)#network 172.16.0.0
R1(config-router)#network 172.16.0.8
R1(config-router)#network 192.168.10.0
R1(config-router)#no auto-summary
R1(config-router)#passive-interface gigabitethernet 0/@
R1(config-router)#exit
R1(config)#exit
Rl#copy running-config startup-config

a
Rl>enable
Rl#conf t
Enter configuration commands, one per line. End with CNIL/Z.
Rl (config) #router rip
Rl (config-router)#version 2
Rl (config-router)#do show ip route connected
C 172.16.0.0/30 is directly connected, Serial0/1/0
C 172.16.0.8/30 4s directly connected, Serial0/1/1
© 192,168.10.0/24 is directly connected, GigabitEthernet0/0
R1 (config-router)#network 172.16.0.0
Rl (config-router)#network 172.16.0.8
Rl (config-router) #network 1$2.168.10.0
Rl (config-router)#no auto-summary
Rl (config-router) #passive-interface gigabitethernet 0/9
Rl (config-router) #exit
Rl (config) fexit
Re
$S5YS-S-CONFIG_I: Configured from console by console
Rl#copy run start
Destination filename [startup-config]?
Building configuration...
- yw
ite)
3 Repeat steps 1 and 2 for R2 and R3.
R2> enable
R2#configure terminal
R2(config)#router rip
R2(config-router)#version 2
R2(config-router)#do show ip route connected
R2(config-router)#network 172.16.0.0
R2(config-router)#network 172.16.0.4
R2(config-router)#network 192.168.20.0
R2(config-router)#no auto-summary
R2(config-router)#passive-interface gigabitethernet 0/@
R2(config-router)#exit
R2(config)#exit
R2#copy running-config startup-config

R3> enable
R3#configure terminal
R3(config)#router rip
R3(config-router)#version 2
R3(config-router)#do show ip route connected
R3(config-router)#network 172.16.0.4
R3(config-router)#network 172.16.0.8
R3(config-router)#network 192.168.30.0
R3(config-router)#network 210.10.10.0
R3(config-router)#no auto-summary
R3(config-router)#passive-interface gigabitethernet 0/0
R3(config-router)#exit
R3(config)#exit
R3#copy running-config startup-config
R2:
Ro>enable im
R2#conf t
Enter configuration commands, one per line. End with CNIL/Z.
R2(config)#router rip
R2(config-router)#version 2
R2(config-router)#do show ip route connected
Cc 172.16.0.0/30 is directly connected, Serial0/3/0
c 172.16.0.4/30 is directly connected, Serial0/3/1
c 192.168.20.0/24 is directly connected, GigabitEtherneto/0
R2(config-router)#network 172.16.0.0
R2(config-router)#network 172.16.0.4
R2(config-router)#network 192.168.20.0
R2(config-router)#no auto-summary
R2(config-router) #passive-interface gigabitethernet 0/0
R2(config-router) #exit
R2 (config) #exit
R2¢#
$SYS-5-CONFIG I: Configured from console by console
R2#copy run start
Destination filename [startup-config]?
Building configuration...
[0K]
R24] Ad

R3:
R3>enable cS
R3¥conf t
Enter configuration commands, one per line. End with CNTL/Z.
R3 (config) #router rip
R3 (config-router) #version 2
R3(config-router)#do show ip route connected
C 172.16.0.4/30 is directly connected, Serial0/3/1
C 172.16.0.8/30 is directly connected, Serial0/3/0
C 192.168.30.0/24 is directly connected, GigabitEthernet0/0
C 210.10.10.0/30 is directly connected, Serial0/2/0
R3 (config-router) fnetwork 172.16.0.4
R3 (config-router) #network 172.16.0.8
R3 (contig-router) #network 192.168.30.0
R3 (contig-router) #network 210.19.10.0
R3(config-router)#no auto-summary
R3 (config-router) #passive-interface gigabitethernet 0/9
R3 (config-router) #exit
R3 (config) #exit
R3#
$5YS-5-CONFIG_I: Configured from console by console
R3#copy run start
Destination filename [startup-config]?
ilding config io a

Part 2: Verify RIP configuration on the routers
4 Display the R1 routing table and check if RIP updated it with the remote networks.
Tip: Use the rip keyword to view RIP routes.
Rl#show ip route rip
Rlf#show ip route rip
172.16.0,.0/16 is variably subnetted, 5 subnets, 2 masks
Serialo/1/1
192.16%.10.0/24 is variably subnetted, 2 subnets, 2 masks
IR | 192.168.20.0/24 [120/2] via 172.16.0.9, 90:00:09,
exialo/l/l
LR} 192.168.30.0/24 [120/1] via 172.16.0.9, 90:00:09,
Serialo/i/1
210.10.10.0/30 is subnetted, 1 subnets
R | 210.10.10.0 [120/1] via 172.16.0.5, 00:00:05, Seriald/1/1
Rie bs
5 Run show ip protocols to view and verify RIP settings.
Rl#show ip protocols
RIF A
Rl#
Rl#show ip protocols
Routing Protocol is "rip"
Sending updates every 30 seconds, next due in 2 seconds
Invalid after 180 seconds, hold down 180, flushed after 240
Outgoing update filter list for all interfaces is not set
Incoming update filter list for all interfaces is not set
Redistributing: rip
Default version control: send version 2, receive 2
Interface Send Recv Triggered RIP Key-chain
Serial0/1/0 4 2
Serial0/1/1 2 2
Automatic network summarization is not in effect
Maximum path: 4
Routing for Networks:
172.16.0.0
192.168.10.0
Passive Interface(s)}:
GigabitEthernet0/0
Routing Information Sources:
Gateway Distance Last Update
172.16.0.9 120 00:00:10
Distance: (default is 120)
Rig] bell

6 Repeat steps 4 and 5 for R2 and R3.
R2#show ip route rip
R2#show ip protocols
R3#show ip route rip
R3#show ip protocols
R2:
R2>
R2>show ip route rip
172.16.0,.0/16 is variably subnetted, 5 subnets, 2 masks
| 172.16.0.8/30 [120/1] via 172.16.0.6, 00:00:23,
(serialo/3/1
8 192.168.10.0/24 [120/2] via 172.16.0.6, 00:00:23,
exrialo/3/1
192.16%.20.0/24 is variably subnetted, 2 subnets, 2 masks
iR| 192.16%.30.0/24 [120/1] via 172.16.0.6, 00:00:23,
jerialo/3/1
210.10.10.0/30 is subnetted, 1 subnets
| 210.10.10.0 [120/1] via 172.16.0.6, 00:00:23, Serialo/3/1
R2>| ii
R2>show ip protocols
Routing Protocol is "rip"
Sending updates every 30 seconds, next due in 1 seconds
Invalid after 180 seconds, hold down 180, flushed after 240
Outgoing update filter list for all interfaces is not set
Incoming update filter list for all interfaces is not set
Redistributing: rip
Default version control: send version 2, receive 2
Interface Send Recv Triggered RIP Key-chain
Serialo/3/0 2 2
Serialo/3/1 2 2
Automatic network summarization is not in effect
Maximum path: 4
Routing for Networks:
172.16.0.0
192.168.20.0
Passive Interface(s):
GigabitEthernet0/0
Routing Information Sources:
Gateway Distance Last Update
172.16.0.6 120 00:00:21
Distance: (default is 120)
R2> id

R3:
R3>show ip route rip
172.16.0.0/16 is variably subnetted, 5 subnets, 2 masks
LR | 172.16.0.0/30 [120/1] via 172.16.0.19, 00:00:26,
erialo/3/0
[120/1] via 172.16.0.5, 90:00:18,
grialo/3/1
fk] 192.168.10.0/24 [120/1] via 172.16.0.10, 00:00:26,
erialo/3/0
Re 192.168.20.0/24 [120/1] via 172.16.0.5, 00:00:18,
erialo/3/1
R3> v
R3>show ip protocols o
Routing Protocol is "rip"
Sending updates every 30 seconds, next due in 22 seconds
Invalid after 160 seconds, hold down 180, flushed after 240
Outgoing update filter list for all interfaces is not set
Incoming update filter list for all interfaces is not set
Redistributing: rip
Default version control: send version 2, receive 2
Interface Send Recv Triggered RIP Key-chain
Serialo/3/0 2 2
Serialo/3/1 2 2
Serialo/2/0 2 2
Automatic network summarization is not in effect
Maximum path: 4
Routing for Networks:
172.16.0.0
192.168.30.0
210.10.10.0
Passive Interface (s):
GigabitEthernet0/0
Routing Information Sources:
Gateway Distance Last Update
172.16.0.10 220 ooroor14
--More-- | v

Part 3: Test connectivity
7 From PC1, ping all other PCs. All pings should be successful.
Request timed out.
Reply from 192.168.20.2: bytes=32 time=1?ms TYL=125
Minimum = 2ms, Maximum = 17ms, Average = 7ms
Reply from 192.168.30.3: bytes=32 time=Ims TTL=126
JApproximate round trip times in milli-seconds:
Minimum = Ims, Maximum = lms, Average = Ims

Lab Task 3: Propagating a Default Route
Use RIPv2 to distribute the default route (gateway) for all routers from a single router
on the network.
Part 1: Configure a default route
1 From PC1, try to ping an external resource 8.8.8.8 server. The ping will not be
successful because the routers don't know where to forward unknown external
network traffic.
Display the R3 routing table and verify that the “Gateway of last resort” option is
not set.
R3#show ip route
Pinging 8.8.8.8 with 32 bytes of data:
Reply from 192.168.10.1: Destination host unreachable.
Reply from 192.168.10.1: Destination host unreachable.
Reply from 192.168.10.1: Destination host unreachable.
Reply from 192.168.10.1: Destination host unreachable.
Ping statistics for 8.8.8.8:
Packets: Sent = 4, Received = 0, Lost = 4 (100% loss),
R3>show ip route
Codes: L - local, C - connected, S - static, R - RIP, M - mobile,
B - BGP
D - EIGRP, EX - EIGRP external, 0 - OSPF, IA - OSPF inter
area
Nl - OSPF NSSA external type 1, N2 - OSPF NSSA external
type 2
El - OSPF external type 1, E2 - OSPF external type 2, E -
EGP
i - IS-IS, Ll - IS-IS level-l, L2 - IS-IS level-2, ia -
Is-IS inter area
® — candidate default, U - per-user static route, o - ODR
P - periodic downloaded static route
172.16.0.0/16 is variably subnetted, 5 subnets, 2 masks
R 172.16.0.0/30 [120/1] via 172.16.0.10, 00:00:25,
Serial0/3/0
[120/1] via 172.16.0.5, 00:00:01,
Serial0/3/1
(c 172.16.0.4/30 is directly connected, Serial0/3/1
ds 172.16.0.6/32 is directly connected, Serial0/3/1
(c 172.16.0.8/30 is directly connected, Serial0/3/0 v

2 OnR3, configure a (directly-connected) default route towards the Internet,
meaning the outgoing interface that is in the direction of the Internet.
R3>enable
R3#configure terminal
R3(config)#ip route 0.0.0.0 0.0.0.0 serial 0/2/20
3 Display the R2 routing table before distributing the default route for comparison.
R2#show ip route
BagShoW Ep Eoute
Codes: L - lecal, C - connected, S - static, R - RIP, M - mobile, B -
BGP
D - EIGRP, EX - EIGRP external, O - OSPF, IA - OSPF inter area
Nl - OSPF NSSA external type 1, NZ - OSPF NSSA external type 2
El - OSPF external type 1, E2 - OSPF external type 2, E - EGP
i - Is-Is, Ll - IS-IS level-1, L2 - IS-IS level-2, ia - IS-IS
inter area
* - candidate default, U - per-user static route, o - ODR
P - periodic downloaded static route
Gateway of last resort is not set
172.1€.0.0/1€ is variably subnetted, § subnets, 2 masks
c 172.16.0.0/30 is directly connected, Serial0/3/0
L 172.1€.0.1/22 is directly connected, Serial0/3/0
c 172.1€.0.4/30 is directly connected, Serial0/3/1
172.1€.0.5/32 is directly connected, SerialO/3/1
R 172.1€6.0.8/30 [120/1] via 172.1€.0.€, 00:00:23, SerialO/3/1
Rg 192.168.10.0/24 [120/2] via 172.16.0.6, 00:00:23, Serial0/3/1
192.168.20.0/24 is variably subnetted, 2 subnets, 2 masks re

Part 2: Update the default route on all routers
4 OnR3, enter RIP configuration mode and distribute the default route to all
routers, using the default-information originate command.
R3>enable
R3#configure terminal
R3(config)#router rip
R3(config-router )#default-information originate
R3(config-router )#exit
5 Display the R1, R2, and R3 routing tables and check for the default route.
R2#show ip route rip
R2#show ip route rip
172.16.0.0/16 is variably subnetted, 5 subnets, 2 masks
R 172.16.0.8/30 [120/1] via 172.16.0.6, 00:00:20,
Serial0/3/1
R 192.168.10.0/24 [120/2] via 172.16.0.6, 00:00:20,
Serial0/3/1
192.168.20.0/24 is variably subnetted, 2 subnets, 2 masks
R 192.168.30.0/24 [120/1] via 172.16.0.6, 00:00:20,
Serial0/3/1
210.10.10.0/30 is subnetted, 1 subnets
R 210.10.10.0 [120/1] via 172.16.0.6, 00:00:20, Serial0/3/1
R2¢ he
Part 3: Test connectivity
6 From PC1 and the rest of the hosts, try to ping the 8.8.8.8 server again and
observe the result.
C:\>ping 8.8.8.8
Pinging 8.8.8.8 with 32 bytes of data:
Reply from 8.8.8.8: bytes=32 time=2ms TTL=253
Reply from 8.8.8.8: bytes=32 time=llms TTL=253
Reply from 8.8.8.8: bytes=32 time-2ms TTL=253
Reply from 8.8.8.8: bytes=32 time=2ms TTL=253
Ping statistics for 8.8.8.8:
Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),
Approximate round trip times in milli-seconds:
Minimum = 2ms, Maximum = 1lms, Average = 4ms
