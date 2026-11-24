# NET-04-LS1 — Configure and Verify Port Security

[← Wszystkie laboratoria](index.md)

> **Typ:** laboratorium z rozwiązaniem. Zachowano wszystkie kroki, pytania, odpowiedzi, komendy i wartości z materiału źródłowego; usunięto jedynie techniczne nagłówki stron OCR.

## Powiązana teoria

- [Port security](../04-switch-security/port-security.md)

## Pełny przebieg laboratorium

> Zakres źródłowy: strony 86–110.

Computer Networking
Lab Assignment Switch Security
& Solution
NET-04-LS1
Configure and Verify
o° (ee Port Securi
Oln ty
EI
Copyright © 1996-2020 HackerU Ltd.
All Rights Reserved.

Note: Solutions for the instructor are shown inside the green box.
»©) Lab Objective
Learn how to implement port security and the various violation rules, and how port
security uses physical addresses.
by Lab Mission
Use port security to protect assets from a rogue laptop and show the importance of
physical security on a switch.
es .
©) Lab Duration
30-60 minutes
fe Requirements
e Knowledge of basic IOS commands and navigation
os

| Resources
e Environment & Tools

o All platforms

o Cisco Packet Tracer 7.2.2 and higher
e Extra Files

© NET-04-L1.pka

Instructions for PKA Lab Files
Lab material includes the lab document and a PKA lab file.
Open the PKA file through the Cisco Packet Tracer menu by clicking File then Open...
Dette” d &%72aQane ase 2
Serine ome aT)
enn reel nou
Prt ome
ert m je: (Sasa To Dig and Diop To Woe :
Navigate to the file's location and open it.
a
a t: ©
a
r
a
a
a
a
a
4
1

Note: Double-clicking the PKA file in File Explorer may not work (depending on the
Packet Tracer version).
When you open a PKA file in Cisco Packet Tracer, two windows appear:
1. Lab topology window
2. Activity window
PKA Features
Note the following essential information regarding the PT Activity window:

1. Completion percentage: Learner progress appears at the bottom right corner of
the window.

2. Check Results button: When you click this button and then click the Assessment
Items tab, you will find a checklist with lab objectives and status, where “=done,
X=not done.

Note: Both features help the instructor grade the exercise swiftly and efficiently.
IR br activity: 000012 — xf Assessment items Stas Ponts Components) |Feedback
= NetWork
Please refer to the exercise docurnent and carefully follow the I 4 Re
See the peroentage cof completion at the right-bottom corner to ore
determine your progress, = Po Srey ,
Note: The Optional and Bonus section are not scored. < ot Meomect: t chest
Good tus ox aie macs Cored i ter
= Souetuncs ° ote
[00005793 87C4 Inconect tthe
© FexcbemetTo c One
X Ponsiaus roma | Pose
& Fast heme ¢ ote
x Pot Sis veered Pree
rts = rane — oe
Pass emt I Pres
PKA Solution
To view the solution or edit the lab file, you can simply click the wizard hat icon and
enter the following password: C!ScOM@ster
Right-click the Answer Network tab and then click Show Answer Network.
Note: Be careful not to change anything so the lab will remain intact.

Lab Task 1: Configure and Verify Port Security
Enable port security and define the physical address and violation rule for each
interface. All the required commands were introduced in the presentation and can also
be found in the textbook.
Note: If opening the PKA file by double-clicking it results in an error, open it in the
following way instead: Click File > Open... and select the file.
Rogue Laptop | N\ .
Rachel Ross Joey Monica
Issue all commands on S1:
1 Click $1, and then click the CLI tab.
Physical Config Attributes
10S. Command Line Interface

Compiled Wed 12-Oct-05 22:05 by pt_team a

Press RETURN to get started!

$LINK-5-CHANGED: Interface FastEthernet0/1, changed state to up

SLINEPROTO-5-UPDOWN: Line protocol on Interface FastEthernet0/1,

changed state to up

2. Check which computer is connected to which port by populating the MAC
address table. From Rachel’s PC, enter the command prompt and ping every
other PC.

Rachel - o x
Physical Config Programming Attributes
7
Pp Dialup Terminal ‘Command
Configuration Prompt
B
Reply from 10.0.0.2: bytes=32 timesIms TTI=128
Reply from 10.0-0.2: bytes=32 timesims TIL=128
Reply from 10.0.0.2: bytes=32 time<lms TTL=128
Reply from 10.0-0.2: bytes=32 timesIms TID=128
Apetiimate! foGnd-crip-eimed aa m2 1i-eeeonde:
Minimum = Oms, Maximum = ims, Average = oms
Reply from 10.0.0.3: bytes=32 time<lms TTL=1238
Reply from 10.0.0.3: bytes=32 timecims TIL=12¢
Reply from 10.0-0.3: bytes=32 time<Ims TII=128
Ping statistics for 10.0.0.3:
Approximate round trip times in milli-seconds:
C:\> igs

3 To view the MAC addresses connected to the ports, open the S1 switch in CLI
and, in privileged mode, use the command show mac-address-table. Compare
the MAC addresses in the CLI to the ones on the computers.

S1#show mac-address-table

Mac Address Table
Vlan Mac Address Type Ports
1 0004. 9a8b.2832 DYNAMIC Fa0/3
1 Q009.7c96.0271 DYNAMIC FaQ@/2
T 000b.be34. alae DYNAMIC Fae/4
1 00d@.9793.87c4 DYNAMIC Fa@/1
4 Access configure mode and enable port security on the following ports:
a. fastethernet 0/1
b. fastethernet 0/2
c. fastethernet 0/3
d. fastethernet 0/4
To do so, enter global mode and run the following commands:
1. To select all interfaces: interface range fastethernet 0/1-4
2. To set mode access on the selected interfaces: switchport mode access
3. To set port security: switchport port-security
4. To exit the selection of the interfaces: exit
S1(config)#interface range fastethernet @/1-4
S1(config-if-range)#switchport mode access
S1(config-if-range)#switchport port-security
S1(config-if-range)#exit
5 Set the authorized MAC addresses for the Fast Ethernet 0/1 and 0/2 interfaces to
manual by setting a manual MAC address for each interface.
S1(config)#interface fastethernet Q/1
S1(config-if)#switchport port-security mac-address @@D@.9793.87C4
S1(config-if)# exit
S1(config)#interface fastethernet 0/2
S1(config-if)#switchport port-security mac-address 0009.7C96.0271
S1(config-if)#exit

6 Set the authorized MAC addresses for the Fast Ethernet 0/3 and 0/4 interfaces to
sticky.
S1(config)#interface fastethernet 0/3
S1(config-if)#switchport port-security mac-address sticky
S1(config-if)# exit
S1(config)#interface fastethernet 0/4
S1(config-if)#switchport port-security mac-address sticky
S1(config-if)#exit
7 Set the violation mode for each interface, as follows:
a. Fast Ethernet 0/1 — Shutdown. The command is switchport port-security
violation shutdown
S1(config)#interface fastethernet Q/1
S1(config-if)#switchport port-security violation shutdown
S1(config-if)#exit
b. Fast Ethernet 0/2 — Restrict. The command is switchport port-security
violation restrict
S1(config)#interface fastethernet 0/2
S1(config-if)#switchport port-security violation restrict
S1(config-if)#exit
c. Fast Ethernet 0/3 — Restrict. The command is switchport port-security
violation restrict
S1(config)#interface fastethernet 0/3
S1(config-if)#switchport port-security violation restrict
S1(config-if)#exit
d. Fast Ethernet 0/4 — Protect. The command is switchport port-security
violation protect
S1(config)#interface fastethernet 0/4
S1(config-if)#switchport port-security violation protect
S1(config-if)#exit
8 Set the maximum MAC address count to 2 on Fast Ethernet 0/3. Use the
command switchport port-security maximum 2
S1(config)#interface fastethernet 0/3
S1(config-if)#switchport port-security maximum 2
S1(config-if)#exit

9 Set the maximum MAC address count to 2 on Fast Ethernet 0/4. Use the
command switchport port-security maximum 2
S1(config)#interface fastethernet 0/4
S1(config-if)#switchport port-security maximum 2
S1(config-if)#exit
10 Disable all remaining unused ports. (Hint: Use the shutdown command.)
Tip: The range command is useful when you want to issue the same command
simultaneously on multiple ports.
S1(config)#interface range fastethernet @/5-24, gigabitethernet @/1-2
S1(config-if-range)#shutdown
S1(config-if-range)#exit
11 Save the configuration on the switch.
Sl#copy running-config startup-config
12 From Rachel's PC, ping all other PCs.
Tip: Use the ipconfig command on the computer’s command prompt.

Lab Task 2: Verify Port Security
Practice the use of various commands and troubleshooting to verify the integrity of port
security.
1 Run the show port-security command on the switch to verify all settings.
S1#show port-security
Sl>enable
Sl#show port-security
Secure Port MaxSecureAddr CurrentAddr SecurityViolation Security
Action
(Count) (Count) (Count)
Fa0/1 & 1 Oo
Shutdown
Fad/2 pS & o
Restrict
Fa0/3 & 1 0
Restrict
Fad/4 2 & o
Protect
sl# Vv
Ctri+F6 to exit CLI focus Copy Paste
D1 Top
Additional Show commands:
Sl#show running-config

Rs = o x
Physical Config CLI Attributes
10S Command Line Interface
inlerface FaslELherneLl0/2 had
suitchport mode access
awitebport. port-security
switehport port-sccurity mac-address 00U0.9793.27C4
interface FastEthernet0/2
switchpork made access
switehport port security
switchport port-security violation rastrict
SwlLeLporl eosl-secucily mac-addsess 9008. 7096.0272
intertace FaseBthernet/3
switehport mode access
switchport port-security
switchport yort-security maximum 2
aw tehport povt-security mac-aderess sticky
switehport port security violation restrict
switchport port-security mac-address sticky 0004. 9A8B.2822
interface FastRthernet.0/4
switchport mode access
switehport port-security
Swilehporl eorl-securily maximum 2
suitchport port-security mac-address sticky
switchport port-security violation restrict
switchport port-security mac-address sticky 0008.##34.A1A0
Ctri+F6 to exit CLI focus Copy, Paste
UO tep
Sil#show port-security address

id
Physical Config CLI Attibutes
10S Command Line Interface
Configured MAC Addresses + 0 A
Sticky MAC Adcresses a
Last Souzce Addcess:Vlan : 0004, 9A8B.2890:1
seaurity Violation Gount 2 @
Sl (config) #do show port-security address
Secure Mac Address Table
vian Mac Addzessitype vorts
Remaining Age
(mins)
FastRtnernat/1 a
1 anos. 786.0272 Securetontiguzed
Fastkthe=nat/2 i
1 0004. YAEB. 232 SecureSticky
Fas LRU ern 1.0/3 7
1 0005.3=34.A1A0 securesticky
rastetne=net/4 -
Max addresses limit in system (excluding one mac per port) : 1024
sl(config) § .
Ctrl+F6 to exit CL! focus: Copy Paste
U top
Sil#show port-security interface type number
Example:
Sil#show port-security interface fastethernet 0/1
Port Security : Enabled
Port Status : Secure-up
Violation Mode : Shutdown
Aging Time : @ mins
Aging Type : Absolute
SecureStatic Address Aging : Disabled
Maximum MAC Addresses gal
Total MAC Addresses g il
Configured MAC Addresses 5 al
Sticky MAC Addresses 70
Last Source Address:Vlan : 000@.0000.2000:0
Security Violation Count 2 0

2 Disconnect Rachel's PC from S1. Click the Delete button 4 and then click the
item you want to delete.
eB Cisco Packet Tracer - C:\Users\mauri\OneDrive\ Desktop\revised labs\NET-04-L1.pka
File Edit Options View Tools Extensions Help
BmebRROrae BAC ’AAQOHES |
sdeas dv mee wa
[A Logical] Physical): 390, y: 254
Rogue Laptop K
teks Was Te Notices
3 Connect the rogue laptop to S1 on Fast Ethernet 0/1 using a straight-through
cable and press the time forward button.
QE) (Physical) 200 y- 274 Reo CIC Cons
Rogue Laptop
j=) Se =
Rachel Ross doey Monica
s§ulsae(s “(Visas |
ae 4
#

4 Try to ping Ross’s PC from the rogue laptop.
B Rogue Laptop = a x
Physical Config Desktop Programming —_ Attributes
|
|
Rachel Ross Joey Monica

5 _ Display the information regarding the Fast Ethernet 0/1 port and note that it is in
err-disabled mode.
Sl#show interface fastethernet 0/1
[ee ey
/ = OF
Rachel Ross Joay eae
SSC CISSEING OF "SHOW SNTSEESCS™ COUNTSES TEVEE
Input queue: 0/75/0/0 (size/max/drops/flushes); Total output drops: 0
Queueing strategy: fifo
Output queue :0/40 (size/max)
5 minute input rate 0 bits/sec, 0 packets/sec
5 minute output rate 0 bits/sec, 0 packets/sec
956 packets input, 193351 bytes, 0 no buffer
Received 956 broadcasts, 0 runts, 0 giants, 0 throttles
0 input errors, 0 CRC, 0 frame, 0 overrun, 0 ignored, 0 abort
0 watchdog, 0 multicast, 0 pause input
Ctrl+F6 to exit CLI focus Copy Paste
O Top
6 Reconnect Rachel’s PC to Fast Ethernet 0/1.
7 On Fast Ethernet 0/1, run the shutdown command, and then no shutdown. The
port is now back to normal.
S1(config)#interface fastethernet @/1
S1(config-if)#shutdown
S1(config-if)#no shutdown

Rs i
Physical Config _CLI_ Attributes,
10S Command Line Interface
si¥ :
Sl#show interfaces fastEthernet 0/1
FastEthernet0/1 is ee toe cea
Hardware is Lance, address 15 U0U1l-cla0.as01 (ora 0U01.c7a0.a301)
BW 100000 Kbit, DLY 1000 usec,
reliability 255/255, txload 1/255, rxload 1/255
Encapsulation ARPA, loopback not set
Keepalive set (10 sec)
Full-duplex, 100Mb/s
input flow-control is off, output flow-control is off
ARP type: ARPA, ARP Timeout 04:00:00
Last input 00:00:08, output 00:00:05, output hang never
Last clearing of "show interface" counters never
Input queue: 0/75/0/0 (size/max/drops/flushes); Total output drops: 0
Queueing strategy: fifo
Output queue :0/40 (size/max)
5 minute input rate 0 bits/sec, 0 packets/sec
5 minute output rate 0 bits/sec, 0 packets/sec
956 packets input, 193351 bytes, 0 no buffer
Received 956 broadcasts, 0 runts, 0 giants, 0 throttles
Q input errors, 0 CRC, 0 frame, 0 overrun, 0 ignored, 0 abort
atchdoac 0 miitica nance inn 4
Ctrl+F6 to exit CLI focus Copy Paste
O Top

AR Cisco Packet Tracer - = a x
File Edit Options View ‘Tools Extensions Help
BmePOraeALVTAQAAODEAESS 2
RQexcevmae@ Me
[A Logical] Physical] x: 595, y: 239 Root a \( a i( ay \( a \(~ 06:16:09]
y IN
Rogue Laptop J \
Rachel Ross. bey! Monica
PE LICE iavaraaeses esa
| <
Hi

8 Disconnect Ross’s computer and connect the rogue laptop. Then try to ping
Rachel.
® rogue Laptop - a x

Physical Config Desktop Programming _— Attributes ;

C:\>ping 10.0.0.1

Pinging 10.0.0.1 with 32 bytes of data:

Request timed out.

Request timed out.

Request timed out.

Request timed out.

Ping statistics tor 10.0.0.1:

Pinging 10.0.0.1 with 32 bytes of data:

Request timed out.

Request timed ont.

Request timed out.

Request timed out.

Ping statistics for 10.0.0.1:

Packets: Sent = 4, Received = 0, Lost = 4 (100% loss),
(Top
Rogue Laptop S
Poon
Rachel Ross Joey Monica
Learners should note that the rogue laptop does not go red as with Rachel’s port. They should also
notice that they cannot ping Rachel’s port, either.

9 Display the port security of the Fast Ethernet 0/2 port and remember that the
port security is set to one MAC address.
S1#show port-security interface fastethernet 0/2
Rsi * a x
Physical Cong _ CLI Atnbutes
10S Command Line nteriane
956 packets input, 199951 bytes, 0 ne buffer A
Roceived 956 brocGcasts, 0 rents, 0 giante, 9 throttics
9 output srrors, © Gellisions, 0” intevzace roscts
$1 (config-if}t
$1 (config-ift}#
Aging Time : 0 mins
Aging Typs + nbsolte
sticky Mic addresses 12
(Ctrl#F6 to exit CLI focus. ‘Copy Paste
(Top
Learners should notice that this port is set to only one MAC address, which is why the ping is being dropped.
10 Reconnect Ross’s computer to Fast Ethernet port 0/2 and see that you can ping
all the other computers on the network.

11 Disconnect Joey’s computer and connect Fast Ethernet 0/3 to the rogue laptop.
Then ping Monica’s computer.
W Rogue Laptop = oO x
Physical Config Desktop Programming Attributes
ing statistics for 10.0.0.1: is
Packets: Sent = 4, Received = 0, Lost = 4 (100% loss),
Ping statistics for 10.0.0.3:
Packets: Sent = 4, Received 0, Lost = 4 (100% loss),
C:\>ping 10.0.0.4
Reply from 10.0.0.4: bytes=32 time=1ms TTL=128
Reply from 10.0.0.4: bytes=3Z time<lms TTL=12'
Reply from 10.0.0.4: bytes=32 time=1ms TTL=128
Reply from 10.0.0.4: bytes=32 time<lms TTL=128
ing statistics for 10.0.0.4:
Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),
Approximate round trip times in milli-seconds:
Minimem Oms, Maximum = ims, Average = Oms
O Top
L__| =
Rogue Laptop 1
Poon
Rachel Ross Joey Monica
Learners should note that the switchport security is different on the Fast Ethernet 0/3 port, which is
why the rogue laptop is able to ping. Additionally, this should initiate a conversation about the security
issues.

12 Display the port security of the Fast Ethernet 0/3 port and note that the port
security is set to two MAC addresses.
S1#show port-security interface fastethernet 0/3
Bsi - a *
Physical Config _CLI__ Attributes
10S Command Line Intertace
Sl>show port-security intertace tastethernet 0/3
% invalid input detected at '*' marker
sl>enable
Sl#do show port-security interface fastethernet 0/3
& tnvaTia dnpnt detected at te marier
Slshow port-sncnvity tntertacs tastathernat 0/3
Berl Secusily 2 Enabled
Berl Slalus 2 Secure-up
Vivlal_on Mode 2 ResLeicl
Aging Time : 0 mins
Aging Type : Absolute
Securestatic Addzess Aging : Disabled
Maximum MAC Addresses 22
Toval MAC Addresses 22
Configured MAC Addresses: 0
Sticky MAC Addresses ae
Last Source Address:Vlan + 090.0026. 3cE3:1
Security violation count 1 ¢
sta Y
Ctrl+F6 to exit CLI focus Copy Paste
C1 Top
Learners should notice that this port is set to two MAC addresses.

13 Now move Monica’s ethernet port to the rogue laptop (Fast Ethernet 0/4) and
Joey’s to Monica’s computer (Fast Ethernet 0/3).
Y_| _
Rogue Laptop 4
S9OoOoD
Rachel Ross Joey Monica
14 Goto Monica’s computer, open the CLI, and ping Rachel.
Learners should note that Fast Ethernet 0/3 restrict is now set, hitting the maximum of two MAC
addresses. Fast Ethernet 0/4 is in protected mode, which is dropping the ping.
® Monica - Oo x
Physical Config _Deskoy Programming Attributes
Request timed out.
C1 Top

W Rogue Laptop - o x
Physical Config Desktop Pregramming Attributes
Command Prompt x
Ping statistics for 10.0.0.3: e
packets: Sent = 1, Received = 0, Lost = 4 (100 loss)
c:\ping 10.0.0.4
Pinging 10.0.0.4 with 32 bytes of data:
Roply from 10.0.0.4: bytes-32 timo-ims TrE-128
Reply from 10.0.0.4: bytes-32 time<lms ITL-128
ing statistics for 10.0.0.4:
Approximate round trip times in milli-seconds:
minimum = ms, Maximum = ims, avoraga = oms
Pinging 10.0.0.1 wilh 32 Lyles of dala:
Request timed out.
Request Lied oul.
Request timed oul
Ping statistics tor 10.0.0.1:
Packets: Sent = 4, Received = 0, Lost = 4 (100% loss),
LD Top

15. Display the port security of the Fast Ethernet 0/4 port and note that the port
security is set to protect.
S1#show port-security interface fastethernet 0/4
Bs =a a x
Physical Contig _CLi_Atibutes
10S Command Line Interface
Port. Securily 7 Fratied n
port stezus 1: Secure-up
Violation Node 1 Restric
Porl Slzlus 1 Scure-up
violation Node } Drovect
aging vine 10 mins
Aging Type ? Absvlule
SecureStatic Address Aginc : Disabled
Maximun Hac addresses 2
Total MAC Addresses +
Centigurea wac adazesges 0
Ctrl+F6 to exit CLI focus Copy Paste
Oop

Learners should notice that this port is set to two MAC addresses, but that its violation mode is set to

protect.

16 To wrap up, connect the ports back to their original locations and attempt to
ping Joey and Monica again. You should notice that there are no issues with
pinging any of the other members on the LAN.

& Mission Accomplished
® You protected endpoints by using port security to limit the number of MAC
address per port and filtered MAC addresses.
@ You now have an understanding of the different types of violation modes.
@ By not applying the proper port security, you have left one port vulnerable.
