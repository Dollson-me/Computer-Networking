# NET-05-LS2 — IPv4 and Initial Router Configuration

[← Wszystkie laboratoria](index.md)

> **Typ:** laboratorium z rozwiązaniem. Zachowano wszystkie kroki, pytania, odpowiedzi, komendy i wartości z materiału źródłowego; usunięto jedynie techniczne nagłówki stron OCR.

## Powiązana teoria

- [Routers and interfaces](../05-addressing-routing/routers-interfaces.md)
- [Routing process and routing table](../05-addressing-routing/routing-process.md)
- [IPv4 addressing](../05-addressing-routing/ipv4.md)

## Pełny przebieg laboratorium

> Zakres źródłowy: strony 131–147.

Computer Networking
Lab Assignment IP & Routing
& Solution Concepts
RO isis, NET-O5-LS2
olF IPv4 and Initial Router
i U Configuration
Copyright © 1996-2021 HackerU Ltd.
All Rights Reserved.

Note: Solutions for the instructor are shown in the green box.
G Lab Objective
Learn how to configure the initial setup of a router and how |Pv4 addressing is used to
communicate between networks.
* Lab Mission
Set IPv4 addresses in the initial router configuration, and the addresses of all devices on
each LAN. Practice using IPv4 to route traffic within a WAN and connecting to the wider
internet.
Note: All required commands were introduced in the presentation and can also be
found in the textbook.
ea .
©) Lab Duration
30-60 minutes
fe Requirements
e Knowledge of basic IOS commands and navigation
e Knowledge of IPv6
os

| Resources
e Environment & Tools

o All platforms

© Cisco Packet Tracer 7.2.2
e Files

© NET-05-L2.pka

Instructions for PKA Lab Files
Lab material includes the lab document and a PKA lab file.
Open the PKA file through the Cisco Packet Tracer menu by clicking File and Open...
WF Cisco Packet Tacer ; - ao x
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

Note: Double-clicking the PKA file in File Explorer may not work (depending on the
Packet Tracer version).
Lab material includes the lab document and a PKA lab file. When you open a PKA file in
Cisco Packet Tracer, two windows appear:

1. Lab topology window

2. Activity window
PKA Features
Note the following essential information regarding the Activity window:

1. Completion Percentage: Student progress appears at the bottom right corner of
the window.

2. Check Result Button: When you click this button and then click the Assessment
Items tab, you will find a checklist with lab objectives and status, whereby
V=done, X=not done.

Note: Both features help the instructor grade the exercise swiftly and efficiently.
Please refer to the exercise document and carefully follow the [Assessment Reme ‘Status Points Component(s) | Feedback
feoinons teat
‘See the percentage of completion at the right-bottom corner to NTP Server o ‘Other
determine your progress, FES 3 ote
Note: The Optional and Bonus section are not scored, Lao rears ‘ ss
Good Luck is ° Or

PKA Solution

To view the solution or edit the lab file, you can simply click the wizard hat icon and

enter the following password: C!ScOM@ster

Right-click the Answer network tab and then click Show Answer network.

Note: Be careful not to change anything so the lab will remain intact.

Lab Task 1: Initial Router Configuration
Connect the router to local switches and secure it with login credentials.
Issue all commands on R1.
Note: Router IOS is similar to Switch IOS.
Part 1: Connect R1 to Switches
1 Using a straight-through cable, connect R1 gigabitEthernet 0/0 to gigabitEthernet
0/1, on S1.
(DD FastEthemetoi20
B FastEthernet0/21 =
[DD FastEthemetoi23 ath
FastEthernet0/24
eet oe LESS!
IgabitmemnetOr /\ 10.0.0.0/24
«
PE] el F[Oh 4 Fs aisiAdv
es | 2nd
] Ast e

2 Using a straight-through cable, connect R1 gigabitEthernet 0/1 to
gigabitEthernet 0/1, on 82.
BD Festtiveneion9
Rt [Dy Fastethemetoe2
[Di Fastethemetor2a
4th mn
oOo 22 } =)
Usert User User3 Userd
le —.
2duile° Fj aS) AARBREHAA
2nd
| a Ast 3
a
Part 2: Initial Settings on R1
3 Click R1, click the CLI tab, and enter global configuration mode.
Router>enable
Router#configure terminal
4 Set the device name to R1.
Router (config)#hostname R1
R1(config)#
5 Create a user account: Username: Admin, Password: p@nd@
R1(config)#username Admin password p@nd@
6 Set enable password to c!scO
R1(config)#enable password c!sc®

7 Set an appropriate security message (banner):
Access to this device is for authorized personnel only!
R1(config)#banner motd #Access to this device is for authorized personnel
only!#
8 Encrypt all passwords on the device.
R1(config)#service password-encryption
9 Secure access to the console port by enabling username and password
authentication on the port.
R1(config)#line console @
R1(config-line)#login local
R1(config-line)#exit
R1(config)#exit
10 Verify and save settings. Press Enter and do not write anything after the
question mark.
Rl#show running-config
Rl#copy running-config startup-config
Destination Filename [startup-config]?

Lab Task 2: Configure IPv4
Assign IPv4 addresses to the router and establish connections with the LANs.
Part 1: Review Questions
1 How many bits are in an IP or subnet mask address?
2 What is the purpose of IPv4 Class D?
Class D IP range is reserved for multicast communications.

3. What is the difference between a public IP address and a private IP address?
Private addresses are only allowed on the LAN and are used to represent internal
hosts. Public addresses are unique, only allowed on the internet, and are used to
represent large networks (AS).

4 What is the difference between an IPv4 unicast message and an IPv4 broadcast

message?
A unicast message only has a single destination, while a broadcast message is sent to
the entire broadcast domain (all devices on the same network).

5 What are the three IP address ranges used in private networks?
In accordance with RFC1918, the following ranges are assigned to private networks:
10.0.0.0—10.255.255.255
172.16.0.0-172.31.255.255
192.168.0.0-192.168.255.255

6 Whatis a suffix?
A suffix is a decimal method of displaying a subnet mask based on bits.
For example: /8 > 255.0.0.0

7 What is a default gateway address?

From the host perspective, the default getaway is the address of the router that routes
traffic to other networks.

8 Based on which two items of information does a router make routing decisions?

Based on the destination packet IP and the routing table.
Part 2: Configure IPv4 on R1 Interfaces:
Issue all commands on R1.
9 InR1, enter global configuration.
R1>enable
Password:
Rl#configure terminal
R1(config)#

10 Enter interface gigabitEthernet 0/0, configure the IP address 192.168.0.1, and
configure the appropriate subnet mask: 255.255.255.0. Then enable the
interface.

R1(config)#interface gigabitethernet 0/0
R1(config-if)#ip address 192.168.0.1 255.255.255.080
R1(config-if)#no shutdown

R1(config-if)#exit

11 Repeat the previous step for gigabitEthernet 0/1 with the IP address 10.0.0.1/24

and enable the interface.
R1l(config)#interface gigabitethernet 0/1
R1(config-if)#ip address 10.0.0.1 255.255.255.0
R1(config-if)#no shutdown
R1(config-if)#exit

Part 3: Verify Interface Settings
12 Stay in global configuration mode. Note: The do command enables the privileged
mode command in global configuration mode. It does not support the
autocomplete feature.
13 Verify the status and IP configuration, using do show ip interface brief
Note: Disregard Giga 0/0/0, which is preconfigured.
R1(config)#do show ip interface brief
R1 (config) #
R1(config)#do show ip interface brief
Intexface IP-address OK? Method status
Protocol
GigabitEthernet0/0 192.168.0.1 YES manual up
up
GigabitEthernet0/1 10.0.0.1 YES manual up
ue
GigabitEthernet0/0/O 7.7.7.1 YES manual up
up
Viani unassigned YES unset
administratively down down
R1 (config) #| v
14 Display the routing table using do show ip route
Gateway of last resort ig 7.7.7.2 to network 9.0.0.0
7.0.0.0/8 ig variably submetted, 2 subnets, 2 masks
c 7.7.7.0/30 ig directly conmected, GigabitEthernet0/0/0
L 7.7.7.1/32 is directly connected, GigabitEthernet0/0/0
TTT TE GITecery CeMnected, CIdan ee TneEneey
L 192.168.0.1/32 is directly connected, GigabitEthernet0/0
a 0.0.0.0/0 [1/0] via 7.7.7.2
R1 (config) # v
15. What do the letters C and L represent in the routing table?
C= Directly connected network
L = Local interface IP address

16 Save the configuration. Press Enter and do not write anything after the question
mark.
R1(config)#exit
Rl#copy running-config startup-config
Destination Filename [startup-config]?
Part 4: Configure IPs on the User PCs
17 Click User1 and then the Desktop tab.
18 Click the /P Configuration icon.
e _
Physical Config Desktop. Programming Altibuies
S—a G IPv4 IPv6
Oop
19 InUser1, configure the IP address 192.168.0.2/24.
20 In User1, configure the default gateway address, which is the IP address of the
router's interface connected to the same network.

® Usert - a x]
Physical Confg Desig Progamming _Anntee
Waeteco —_(Fesithona :
F Contgutan
© oxcp @ Static
IP Aahess 20902
Stn! Mask |
Dat Steuay |
ONS Sener |
21 In User2, configure the IP address 192.168.0.3/24.
22 In User2, configure the default gateway address.
R User2 - og x
Psi Corba _ Dasiop Prostanning tious
ect Ct‘CS
Wierace (Fathom 5
congutn
© bHcP © Static
PAdtess ezien03
Subnet Mask 562580
Dal Gateway ve2c001
ONS Sever 0000

23° Enter the command prompt and use ipconfig to verify settings for both User1
and User2.
phys Cov] Geskion Phowainning Albiitee _
el al
DN fsen er
ae — a [reve | [Ive |
tee
Packet Tracer PC Command Line 1.0
c:\>ipconfig
FastEthernet0 Connection: (default port)
Link-local IPv6 Address.........! FE80::230:A3FF: FE75:ED22
SUBNCE: MASK or ce nvceececwenenenwet 2-2 oe tnoO
Default Gateway.........e2.ee2+2-! 192.168.0.1

24 Repeat steps 17 through 23 for User3 and User4. In User3, set the IP address
10.0.0.2/24. |n User4, set the IP address 10.0.0.3/24. In both computers, set the
default gateway address, which is the IP address of the router's interface
connected to the same network.

| Users - oo x
|
(Pcomigeatn
| Omer © ome
IP Addvoss [to0.02
Suboet Mas (zssane 2580
| ort comay fiooot
DNS Sever {nooo
R Users - Oo x
waetace (Fastenal E
contain
© ouep @ Static
PAdose ja003 |
‘Subnet Mask 255. 256.256.0 |
Default Gateway 40004 1
DNS Sener |
Part 5: Verify Connectivity
25 On the User1 desktop, click the Command Prompt icon.
26 Use ipconfig to verify network settings.
Packet Tracer PC Command Line 1.0
C:\>ipconfig
FastEthernet0 Connection: (default port)
Link-local IPv6 Address.........: FE80::230:A3FF: FE75:ED22
Subnet Masks: 2600s cose eiecia wat 2956255.255.0
Default Gateway. .......eeeeeeee-! 192.168.0.1

27 Ping its default gateway to make sure there is connectivity with the router.
Packet Tracer PC Command Line 1.0
Ic:\>ping 192.168.0.1
Pinging 192.168.0.1 with 32 bytes of data:
Reply from 192.168.0.1: bytes=32 time=2ms TTI=255
Reply from 192.168.0.1: bytes=32 time=5ms TTL=255
Reply from 192.168.0.1: bytes=32 time=12ms TTL=255
Reply from 192.168.0.1: bytes=32 time=llms TTL=255
Ping statistics for 192.168.0.1:
Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),
‘Approximate round trip times in milli-seconds:
Minimum = 2ms, Maximum = 12ms, Average = 7ms
28 Ping User2, User3, and User4 to verify connectivity with all hosts on the internal
and adjacent networks.
c:\ ping 16.0.0.2
Pinging 10.0.0.2 with 32 bytes of data:
Reply from 10.0.0.2: bytes=32 time=lms TTL=127
Reply from 10.0.0.2: bytes=32 time<lms TTL=127
Reply from 10.0.0.2: bytes=32 time<lms TTL=127
Reply from 10.0.0.2: bytes=32 time<lms TTL=127
Ping statistics for 10.0.0.2:
Packets: Sent = 4, Received = 4, Lost = 6 (0% loss),
Approximate round trip times in milli-seconds:
Minimum = Oms, Maximum = lms, Average = Oms

chp}

Ping 192.168.0.3

Ping 10.0.0.3

Ping 10.0.0.2

29 Ping 8.8.8.8 to verify internet connectivity.
C:\>ping 8.8.8.8
Pinging 8.8.8.8 with 32 bytes of data:
Reply from 8.8.8.8: bytes=32 time<lms TIL=254
Reply from $.8.5.8: bytes=32 time<lms TIL=254
Reply from &.8.8.8: bytes=32 time<lms TIL=254
Reply from §.8.5.8: bytes=32 time<lms TIL=254
Ping statistics for §.8.8.8:
Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),
Approximate round trip times in milli-seconds:
Minimum = Oms, Maximum = Oms, Average = Oms
Csi>
Part 6 (Bonus): Set IPs and the Default Gateway on the Switches
30 Click $1 and then click the CLI tab.
31 Enter interface vlan 1 configuration mode.
S$1>enable
S1#configure terminal
S1(config)#interface vlan 1
S1(config-if)#
32 InS1, for vlan 1, configure the IP address 192.168.0.4/24. Remember to enable
the interface.
S1(config-if)#ip address 192.168.0.4 255.255.255.080
S1(config-if)#no shutdown
S1(config-if)#exit

33 InS1, set the default gateway to 192.168.0.1.
$1 (config) #
Sl(config)#ip default-gateway 192.168.0.1
51 (config) #exit
Sif
$SY¥S-S-CONFIG I: Configured from console by console
Slt ¥
S1(config)#ip default-gateway 192.168.0.1
S1(config)#exit
34 Enter the privileged mode and ping R1 to check connectivity.
S1#ping 192.168.0.1
Type escape sequence to abort.
Sending 5, 100-byte ICMP Echos to 192.168.0.1, timeout is 2
seconds:
round-trip min/avg/max = 0/0/0
Slt he
Sl#ping 192.168.0.1
35 Repeat steps 30-35 for S2 with IP address 10.0.0.4/24 and default gateway
10.0.0.1.
S$2(config)#interface vlan1
S2(config-if)#ip address 10.0.0.4 255.255.255.080
S2(config-if)#no shutdown
S$2(config-if)#exit
S2(config)#ip default-gateway 10.0.0.1
