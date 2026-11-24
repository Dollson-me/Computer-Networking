# NET-09-LS1 — Configuring VLANs, Trunks, and More

[← Wszystkie laboratoria](index.md)

> **Typ:** laboratorium z rozwiązaniem. Zachowano wszystkie kroki, pytania, odpowiedzi, komendy i wartości z materiału źródłowego; usunięto jedynie techniczne nagłówki stron OCR.

## Powiązana teoria

- [VLANs](../06-vlans-switching/vlans.md)
- [802.1Q trunking and DTP](../06-vlans-switching/trunking.md)
- [Inter-VLAN routing and router-on-a-stick](../06-vlans-switching/inter-vlan-routing.md)

## Pełny przebieg laboratorium

> Zakres źródłowy: strony 211–231.

Computer Networking
Lab Assignment VLANs & Trunk
& Solution
NET-09-LS1
és Configuring VLANs,
o [ae Trunks, and More
olin
E-
Copyright © 1996-2021 HackerU Ltd.
All Rights Reserved.

Note: Solutions for the instructor are shown in the green box.
G Lab Objective
Explore the benefits of using VLANs on a network and the role trunking plays in setting
up VLANs.
) Lab Mission
The objective of this exercise is to learn how to configure VLANs and trunks for two
different LANs using a router on a stick.
ea .
©) Lab Duration
45-80 minutes
fe Requirements
e Basic knowledge of IOS commands and navigation
e Basic understanding of the VLAN and trunk concepts
LT
[ra] Resources
© Tools
o Cisco Packet Tracer 7.2.2 or higher
e Files
o NET-09-L1.pka

Instructions for PKA Lab Files
Lab material includes the lab document and a PKA lab file.
Open the PKA file through the Cisco Packet Tracer menu by clicking File > Open...
Be ar. AQQQacmESs 2
Tees a A |
Open Aci Seance ae es)
a see ons Se
Prot Clee
ert m je: (Sasa To Dig and Diop To Woe :
Navigate to the file's location and open it.
a
a A 4)
a or
BB Seronage Stross
a
a
a
a
a
a
i
i
‘ Fearne [eS oka [Poet Fe Gotan.)

Note: Double-clicking the PKA file in your file explorer may not work (depending on the
Packet Tracer version).
Lab material includes the lab document and a PKA lab file.
When you open a PKA file in Cisco Packet Tracer, two windows appear:
1. Lab topology window
2. Activity window
PKA Features
Note the following essential information regarding the Activity window:

1. Completion percentage: Learner progress appears at the bottom right corner of
the window.

2. Check Results button: When you click this button and then click the Assessment
Items tab, you will find a checklist with lab objectives and status; V=done, X=not
done.

Note: Both features help the instructor grade the exercise swiftly and efficiently.

A PT Activity: 001012 - ao x ‘Expandialapas Al| Show incase Rena)

Dia ero ne cmt crf the = [Sa ra Compe [reek

‘See the percentage of completion at the right-bottom corner to E-NTP Sener o ‘Other

determine your progress. 5 NTP Sener o Other

Note: The Optional and Bonus section are not scored, eo mnie : »

Good Luck Vie ° ier
PKA Solution
To view the solution or edit the lab file, you can simply click the wizard hat icon and
enter the following password: C!ScOM@ster
Right-click the Answer network tab and then click Show Answer network.
Note: Be careful not to change anything so the lab will remain intact.

Lab Task 1: Revision Questions
Answer the following questions as a review of VLANs.

1 What are the benefits of creating VLANs?

A VLAN is a switched network that is logically segmented on a network. VLANs can
improve security by isolating groups. Users can be grouped into VLANs, and no users
outside those VLANs will be able to communicate with them. VLANs also allow logical
network topologies to overlay the physical switched infrastructure. The technology
logically segments the network into separate Layer 2 broadcast domains, whereby
packets are switched between ports assigned to the same VLAN. By confining traffic
from one LAN to other LANs within the same VLAN, switched virtual networks avoid
wasting bandwidth.

2 What happens when a computer connected to a switch sends a broadcast, such

as an ARP request?
Switches broadcast ARP requests as entries in the ethernet header of FFFF.FFFF.FFFF
(broadcast MAC address) to all nodes, except the one that requests the ARP.

3 > Howcan we implement security on a network without using security protocols?
VLANs can be used to limit user access to certain network segments by granting only
authorized users access to networks with highly sensitive information.

4 Assuming a default switch configuration, what is the standard VLAN range that

can be modified and removed on a Cisco switch?
Only VLANs 2—1001 can be modified or removed.

5 Which configuration allows a port to carry traffic for multiple VLANs?

Trunk configuration allows traffic from multiple VLANs over a single link, and the
extension of VLANs across the network.

Lab Task 2: Configure and Verify VLANs
On a switched network, there may be different types of device groups, such as
printers, workstations, and access points. By default, all interfaces on a switch can
communicate with each other.
VLANs permit the creation of virtual groups on the switch and assign interfaces to
different groups. Only interfaces in the same group are able to communicate with
each other.
Configure a VLAN on all network devices and verify that the VLANs were properly
configured using various troubleshooting methods.
Part 1: View the Default VLAN Configuration
1 Using the CLI, connect S1 and run the command that displays all configured
VLANs. Make sure all interfaces are assigned to VLAN 1, by using the command:
show vlan brief
S1>enable
S1#show vlan brief
VLAN Name Status Ports
[ <= =#=#=#=8 see Fa0/1, Fa0/2, FaO/3, Fao/4
Fa0/5, Fa0/6, Fa0/7, Fa0/s
Fa0/9, Fa0/10, FaQ/1l, Fa0/12
Fa0/13, Fa0/14, Fa0/15, Fa0/1é
Fa0/17, Fa0/18, Fa0/19, Fa0/20
Fa0/21, Fa0/22, Fa0/23, Fa0/24
Gig0/1, Gigd/2
1002 fddi-default active
1003 token-ring-default active
1004 fddinet-default active
1005 trnet-default active
Sl? ww

2 Repeat step 1 on S2.
S2>enable
S2#show vlan brief
S2>enable
S2#show vlan brief
VLAN Name Status Ports
Fa0/5, Fa0/6, Fa0/7, Fao/s
Fa0/3, FaO/10, Fa0/11, Fa0/12
FaQ/13, Fa0/l4, Fa0/15, Fa0/16
Fa0/17, Fa0/18, Fa0/15, Fa0/20
Fa0/21, FaO/22, Fa0/23, Fa0/24
GigO/1, Gigd/2
1002 fddi-default active
1003 token-ring-default active
1004 fddinet-default active
1005 trmet-default active
524] v
Part 2: Create and Name VLANs
3. Create and name the following VLANs on S1:
a) VLAN 10: Workstation
b) VLAN 20: Servers
Sl#configure terminal
S1(config)#vlan 10
S1(config-vlan)#name Workstation
S1(config-vlan)#exit
S1(config)#vlan 20
S1(config-vlan)#name Servers
S1(config-vlan)#exit

4 Using the same commands as those in the previous step, create and name the
same VLANs on S82.
S2#configure terminal
S2(config)#vlan 10
S2(config-vlan)#name Workstation
S2(config-vlan)#exit
S2(config)#vlan 20
S2(config-vlan)#name Servers
S2(config-vlan)#exit
Part 3: Assign VLANs to Ports
5 OnS1, assign the VLANs to the following ports:
a) All ports that connect to workstations and servers must be set in access
mode.

b) VLAN 10: Fast Ethernet 0/1-2

c) VLAN 20: Fast Ethernet 0/3
S1(config)#interface range fastethernet @/1-2
S1(config-if-range)#switchport mode access
S1(config-if-range)#switchport access vlan 10
S1(config-if-range)#exit
S1(config)#interface fastethernet 0/3
S1(config-if)# switchport mode access
S1(config-if)#switchport access vlan 20
S1(config-if)#exit

6 0nS2, assign the VLANs to the following ports:
a) All ports that connect to workstations and servers must be set in access
mode.

b) VLAN 10: Fast Ethernet 0/1-4

c) VLAN 20: Fast Ethernet 0/5-6
S2(config)#interface range fastethernet @/1-4
S2(config-if-range)#switchport mode access
S2(config-if-range)#switchport access vlan 10
S2(config-if-range)#exit
S2(config)#interface range fastethernet @/5-6
S2(config-if-range)#switchport mode access
S2(config-if-range)#switchport access vlan 20
S2(config-if-range)#exit

7 Verify S1 and S2 VLAN configuration using the do show vian brief command and
save the configuration.
S1(config)#do show vlan brief
S2(config)#do show vlan brief
Sis
S1(config)#do show vlan brief
VLAN Name Status Ports
1 default active Fag/4, Fa0/5, Fa0/é, Fad/7
Fa0/8, Fa0/9, Fa0/10, FaQ/1l
Fa0/12, Fa0/13, Fa0/14, Fa0/15
Fa0/16, Fa0/17, Fa0/18, Fao/19
Fa0/20, Fa0/21, Fa0/22, Fa0/23
Fa0/24, GigO/1, Gig0/2
10 Workstation active Fa0/l, Fa0/2
20 Servers active Fad/3
1002 fddi-default active
1003 token-ring-default active
1004 fddinet-default active
1005 trnet-default active
Si (contig) 4 Me
$2:
S2(config)#do show vlan brief
VLAN Name Status Ports
1 default active Fa0/7, Fa0/8, Fa0/9, Fa0/10
Fa0/ll, Fa0/12, Fa0/13, Fa0/14
Fa0/15, Fa0/lé, Fa0/17, Fad/18
Fa0/13, Fa0/20, Fa0/21, Fa0/22
Fa0/23, Fa0/24, GigQ/l, Gigd/2
190 Workstation active FaQ/l, Fa0/2, Fa0/3, Fao/4
20 Servers active Fao/5, Fao/é
1002 fddi-default active
1003 token-ring-default active
1004 fddinet—default active
1005 trnet-default active
S2 (config) # ¥

Part 4: Configure and Verify Basic Connectivity
8 Assign IP addresses for all workstation hosts using the address range and subnet
mask: 10.0.0.0 255.255.255.0. Use the last available IP address as the default
gateway.
Rect - asx
Physical Config Desktop Programming Attributes
Inertace —_FastEthernef0 =
IP Configuration
O Duce @ Static
IPAddress
Subnet Mask
Default Gateway
ONS Serer
PC1: IP:10.0.0.1 SM:255.255.255.@ DG:10.0.0.254
PC2: IP:10.0.0.2 SM:255.255.255.@ DG:10.0.0.254
PC3: IP:10.0.0.3 SM:255.255.255.0 DG:10.0.0.254
PC4: IP:10.0.0.4 SM:255.255.255.@ DG:10.0.0.254
PC5: IP:10.0.0.5 SM:255.255.255.@ DG:10.0.0.254
PC6: IP:10.0.0.6 SM:255.255.255.@ DG:10.0.0.254
9 Assign IP addresses for all server hosts using the address range and subnet mask:
192.168.0.0 255.255.255.0. Use the last available IP address as the default
gateway.
B servert - a x
Physical ‘Config ‘Senices Desktop Programming Attributes
IP Configuration
© DHCP @ Static
IPAddress. 192 168.01 |]
‘Subnet Mask 255.255.255.0
Default Gateway 192 168.0 254
DNS Server 0.0.00 |
Server1: IP:192.168.0.1 SM:255.255.255.@ DG:192.168.0.254
Server2: IP:192.168.0.2 SM:255.255.255.@ DG:192.168.0.254
Server3: IP:192.168.0.3 SM:255.255.255.@ DG:192.168.0.254

10 Perform a connectivity test between all workstations connected to switch S1.
ETH: aN ,
Rc 2nd 3rd — a 54
Ald
pcpTy PCPT .
PC1 Pc2
1st iP Dial-up Terminal ommand Web Br
Configuration Prompt |
C:\>ping 10.0.0.2
Pinging 10.0.0.2 with 32 bytes of data:
Reply from 10.0.0.2: bytes=32 time=1ms TTL=128
Reply from 10.0.0.2: bytes=32 time<Ims TTL=128
Reply from 10.0.0.2: bytes=32 time<lms TTL=128
Reply from 10.0.0.2: bytes=32 time<Ims TTL=128
Ping statistics for 10.0.0.2:
Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),
Approximate round trip times in milli-seconds:
Minimum = Oms, Maximum = lms, Average = Oms
11 Repeat the process from the previous step and test connectivity among
workstations connected to switch S2.
From PC3: Ping 10.0.0.6
5
Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),
Reply from 10.0.0.5: bytes=92 time<ims TTL=128
Reply from 10.0.0.5: bytes=32 time=Ims TTL=128

12 Test connectivity between PC1 and PC6. The ping should fail.
RB eci - a x
Physical Config Desktop Programming Attributes

Lab Task 3: Configure Trunks and Native VLAN
To enable VLAN communication between switches, we need to configure trunks.
Part 1: Configure Trunking Ports

1 Configure GigabitEthernet 0/1 on S11 as trunk.
S1(config)#interface gigabitethernet 0/1
S1(config-if)#switchport mode trunk
S1(config-if)#exit
S1(config)#exit

2 Configure GigabitEthernet 0/2 on S11 as trunk. Note: This is connected to the

router,

Sl#configure terminal
S1(config)#interface gigabitethernet 0/2
S1(config-if)#switchport mode trunk
S1(config-if)#exit

3 Configure GigabitEthernet 0/1 on S2 as trunk.
S2(config)#interface gigabitethernet 0/1
S2(config-if)#switchport mode trunk
S2(config-if)#exit
S2(config)#exit

Part 2: Configure Native VLAN

4 Create VLAN 30 on both switches and name it Native.
S1(config)#vlan 30
S1(config-vlan)#name Native
S1(config-vlan)#exit
S2(config)#vlan 30
S2(config-vlan)#name Native
S2(config-vlan)#exit

5 Configure VLAN 30 as the native VLAN for GigabitEthernet0/1 interface on S1.
S1(config)#interface gigabitethernet 0/1
S1(config-if)#switchport trunk native vlan 30
S1(config-if)#exit

6 Configure VLAN 30 as the native VLAN for GigabitEthernet0/1 interface on S2.
S2(config)#interface gigabitethernet 0/1
S2(config-if)#switchport trunk native vlan 30
S2(config-if)#exit

Part 3: Verify Trunk and Native Settings

7 Stay in global configuration mode. Note: The do command enables the privileged
mode command in global configuration mode.

8 Verify trunk and native VLAN configurations on both switches using the do show
interfaces trunk command. Note: You should see both VLANs assigned to the
appropriate ports, and for both switches, the native VLAN should be VLAN 30.

S1(config)#do show interface trunk
S2(config)#do show interface trunk
si:
$1 (config) #do show interface trunk
Port Mode Encapsulation Status Native vlan
GigO/1 on 802.1q trunking 30
Port Vians allowed on trunk
GigO/1 1-1005
Port Vians allowed and active in management domain
Gigd/1 1,10,20,30
Port Vlans in spanning tree forwarding state and not
pruned
GigO/1 1,10,20,30
$1 (config) 4 ~.
S2:
S2(config)#do show interface trunk
Port Mode Encapsulation Status Native vlan
Gigo/l on 802.1q trunking 30
Port Vians allowed on trunk
Gigd/1 1-1005
Port Vians allowed and active in management domain
GigO/1 1,10,20,30
Port Vians in spanning tree forwarding state and not pruned
Gigo/1 1,10,20,30
52 (config) # ba

9 Save the configuration on both switches. Press Enter and do not write anything
after the question mark.
S1(config)#exit
Sl#copy running-config startup-config
Destination Filename [startup-config]?
S2(config)#exit
S2#copy running-config startup-config
Destination Filename [startup-config]?
Part 4: Verify Connectivity
10 Try to test connectivity between PC1 and PC3. The ping should succeed.
Pinging 10.0.0.3 with 32 bytes of data:
Reply from 10.0.0.3: bytes=32 time<lms TTL=128
Reply from 10.0.0.3: bytes=32 time<lms TTL=128
Reply from 10.0.0.3: bytes=32 time=lms TTL=128
Reply from 10.0.0.3: bytes=32 time=lms TTL=123
Ping statistics for 10.0.0.3:
Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),
Approximate round trip times in milli-seconds:
Minimum = Oms, Maximum = lms, Average = Oms

11 Try to test connectivity between workstations and servers. The ping should fail.
C:\>ping 192.168.0.2
Pinging 192.168.0.2 with 32 bytes of data:
Request timed out.
Request timed out.
Request timed out.
Request timed out.
Ping statistics for 192.168.0.2:
Packets: Sent = 4, Received = 0, Lost = 4 (100% loss),
Ci\3 ie

For different VLANs to communicate with each other, inter-VLAN routing must be
configured.
Part 1: Configure Router on a Stick on R1
1 Configure GigabitEthernet0/2 on S11 for trunking.
Sl#configure terminal
S1(config)#interface gigabitethernet 0/2
S1(config-if)#switchport mode trunk
S1(config-if)#exit
2 OnR1, enter global configuration mode.
R1>enable
Ril#configure terminal
3 Enter the GigabitEthernet0/0 interface and activate it using the no shutdown
command. Then return to global configuration.
R1(config)#interface gigabitethernet 0/0
R1(config-if)#no shutdown
R1(config-if)#exit
4 OnR1, create sub-interface GigabitEthernet 0/0.10
R1(config)#interface gigabitethernet 0/0.10
R1(config-subif)#
5 Set the encapsulation type to 802.1Q and assign VLAN 10 to the sub-interface.
R1(config-subif)#encapsulation dotiq 10
6 Referring to the addresses used in Lab Task 2, part 4, step 8, assign the correct IP
address and subnet mask to the sub-interface (workstations). Then return to
global configuration.
R1(config-subif)#ip address 10.0.0.254 255.255.255.0
R1(config-subif)#exit

7 OnR1, create sub-interface GigabitEthernet 0/0.20
R1(config)#interface gigabitethernet 0/0.20
R1(config-subif)#
8 Set the encapsulation type to 802.1Q and assign VLAN 20 to the sub-interface.
R1(config-subif)#encapsulation dotiq 20
9 Referring to the addresses used in Lab Task 2, part 4, step 9, assign the correct IP
address and subnet mask to the sub-interface (servers).
R1(config-subif)#ip address 192.168.0.254 255.255.255.0
R1(config-subif)#exit
Part 2: Verify Settings and Inter-VLAN Connectivity
10 On the router, verify the configuration using the show ip interface brief and
show running-config commands.
R1(config)#do show ip interface brief
R1(config)#do show running-config
Rl(config)#do show ip interface brief
Interface IP-Address OK? Method Status
Protocol
GigabitEthernet0/0 unassigned YES NVRAM up up
GigabitEthernet0/0.10 10.0.0.254 YES manual up up
GigabitEthernet60/0.20 192.1668.0.254 YES manual up up
GigabitEthernet0/1 unassigned YES NVRAM administratively down down
Vlanl unassigned YES unset administratively down down
Rl (config) # vv
R1# show running-config

no ip address
duplex auto
speed auto
interface GigabicEthernet0/0.10
encapsulation dot1Q 10
ip address 10.0.0.254 255.255.255.0
interface GigebitEtherncto/0.20
ip address 192.168.0.254 255.255.255.0
anterface GigabirEtnernet0/1
no ip address
duplex auto
speed auto
shuedown
no ip address
=-More-- “
11 Save the configuration.
R1(config)#exit
Rl#copy running-config startup-config
12 From PC1, ping all other PCs and servers. All pings should be successful.
C:\>ping 192.168.0.1
Pinging 192.168.0.1 with 32 bytes of data:
Request timed out.
Reply from 192.168.0.1: bytes=32 time<lms TTL=127
Reply from 192.168.0.1: bytes=32 time<lms TTL=127
Reply from 192.168.0.1: bytes=32 time<lms TTL=127
Ping statistics for 192.168.0.1:
Packets: Sent = 4, Received = 3, Lost = 1 (25% loss),
Approximate round trip times in milli-seconds:
Minimum = Oms, Maximum = Oms, Average = Oms
