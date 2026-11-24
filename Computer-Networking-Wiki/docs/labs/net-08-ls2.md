# NET-08-LS2 — Configuring & Verifying OSPFv2

[← Wszystkie laboratoria](index.md)

> **Typ:** laboratorium z rozwiązaniem. Zachowano wszystkie kroki, pytania, odpowiedzi, komendy i wartości z materiału źródłowego; usunięto jedynie techniczne nagłówki stron OCR.

## Powiązana teoria

- [Dynamic routing concepts](../05-addressing-routing/dynamic-routing-concepts.md)
- [OSPFv2](../05-addressing-routing/ospfv2.md)

## Pełny przebieg laboratorium

> Zakres źródłowy: strony 203–210.

Computer Networking
Lab Assignment Dynamic Routing
& Solution
NET-08-LS2
i Configuring &
oe ni Verifying OSPFv2
EI
Copyright © 1996-2020 HackerU Ltd.
All Rights Reserved.

Note: Solutions for the instructor are shown inside the green box.
@ Lab Objective
Understand the principles of OSPF and use best practices when working with OSPF in a
production environment.
4) Lab Mission
Configuring routers to use OSPF with best practices in mind.
rN) .
©) Lab Duration
25 — 35 Minutes
(© Requirements
e Knowledge of Cisco IOS.
e Anunderstanding of the Dynamic Routing flow.
e Knowledge of OSPF configuration.
on

| Resources
e Environment & ToolsTools

All Platforms

Cisco Packet Tracer 7.2.2 and higher
e Files

NET-08-L2.pka

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

Note: Double-clicking on the PKA file in your file explorer may not work (depending on
the Packet Tracer version).
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

determine your progress. 5 NTP Sener o Other

Note: The Optional and Bonus section are not scored, eo mnie : »

Good Luck Vie ° ier
PKA Solution
To view the solution or edit the lab file, you can simply click the "Wizard hat" icon and
enter the following password: C!S$cOM@ster
Right-click the "Answer network" tab and then click "Show Answer network".
Note: Be careful not to change anything so that the lab will remain intact.

In this task you will configure the OSPF routing protocol on routers RO, R1, and R2, and
specify the networks for broadcasting.

1 Start the OSPF process with the ID of 1 on RO.
R@>enable
RQ#configure terminal
R@(config)#router ospf 1

2 Set the RO router ID to 1.1.1.0
RO(config-router)#router-id 1.1.1.0

3 Add RO connected networks to OSPF broadcasting.
RO(config-router)#network 192.168.0.0 @.0.0.255 area 0
RO(config-router)#network 172.16.0.0 0.0.0.3 area @
RO(config-router)#network 172.16.0.8 0.0.0.3 area @
RO(config-router)#auto-cost reference-bandwidth 1000

4 Set the gigabitEthernet 0/1 interface to passive.
RO(config-router)#passive-interface gigabitEthernet 0/1
RO(config-router)#exit
RO(config)#exit

5 Repeat steps 1 through 5 on R1 and R2 while setting R1’s ID to 1.1.1.1 and R2’s ID

to 1.1.1.2.
R1>enable
Rl#configure terminal
R1(config)#router ospf 1
R1(config-router)#router-id 1.1.1.1
R1(config-router)#network 192.168.1.@ @.0.0.255 area 0
R1(config-router)#network 172.16.0.4 0.0.0.3 area @
R1(config-router)#network 172.16.0.8 0.0.0.3 area @
R1(config-router)#auto-cost reference-bandwidth 1000
R1(config-router)#passive-interface gigabitEthernet 9/1

R1(config-router)#exit
R1(config)#exit
R2>enable
R2#configure terminal
R2(config)#router ospf 1
R2(config-router)#router-id 1.1.1.2
R2(config-router)#network 192.168.2.@ @.0.0.255 area 0
R2(config-router)#network 172.16.0.4 0.0.0.3 area 0
R2(config-router)#network 172.16.0.0 0.0.0.3 area @
R2(config-router)#auto-cost reference-bandwidth 1000
R2(config-router)#passive-interface gigabitEthernet 0/1
R2(config-router)#exit

Lab Task 2: Default Route with OSPF
In this task, you will configure the default route on router R2.

1 OnR2set the default route towards the internet (directly connected).
R2(config)#ip route 0.0.0.0 0.0.0.0 gigabitEthernet 0/0

2 Enable OSPF default route broadcasting.
R2(config)#router ospf 1
R2(config-router)#default-information originate
R2(config-router)#exit
R2(config)#exit

3 Verify that the routering information was propagated to all three routers using

the show ip route command on all the routers.

R@#show ip route ospf
Ri#show ip route ospf
R2#show ip route ospf

ROPER 2p TERS RERE

172.16.0.0/1€ is variably subnetted, 5 subnets, 2 masks
oO 1972.16.0.4 [110/2] wia 172.1€.0.2, 00:04:13, GigabitEthernet0/0/0
[110/2] wia 172.16.0.5, 00:04:13, GigabitEthernet0/1/0

°o 192.168.1.0 [110/2] via 172.1€.0.9, 00:05:43, GigabitEthernet0/1/0

oO 192.168.2.0 [110/2] via 172.1€.0.2, 00:04:13, GigabitEtherneto/0/0

O*EZ 0.0.0.0/0 [110/1] wia 172.16.0-2, 00:03:07, GigabitEthernet0/0/0

Rog v

Rlgshow ip route ospf

172.16.0.0/1€ is variably subnetted, 5 subnets, 2 masks
° 172.16.0.0 [110/2] wia 172.16.0.5, 00:04:47, GigabitEtherneto/o/o
[110/2] via 172.1€.0.10, 00:04:47, GigabitEtherneto/1/0

° 192.162.0.0 [110/2] via 172.16€.0.10, 00:06:15, GigabitEthernet0/1/0

° 192.16€8.2.0 [110/2] via 172.1€.0.5, 00:04:47, GigabitEthernet0/0/0

OWE2Z 0.0.0.0/0 [110/1] via 172.1€.0.5, 00:03:41, GigabitEthernetO/0/0

Rig v

R2¢show ip route ospf
172.16.0_0/16 is wariably subnetted, 5 subnets, 2 masks
o 172.16.0.8 [110/2] wia 172.1€.0.€, 00:01:23, GigabitEthernet0/1/0
(1106/2) wia 172.16.0.1, 00:01:23, GigabitEthernet0/0/0
°o 192.168.0.0 [110/2] wia 172.16.0.1, 00:01:23, GigabitEthernet0/0/0
°° 192.1€6.1.0 [110/2] wia 172.16.0.€, 00:01:33, GigabitEthernet0/1/0
R2¢| w
