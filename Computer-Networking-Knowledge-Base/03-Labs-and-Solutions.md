# 03 — Lab Assignments & Solutions — wszystkie ćwiczenia i odpowiedzi

Źródło: `Computer Networking Zadania - Odpowiedzi.pdf` (266 stron). Zachowano cele, wymagania, zasoby, wszystkie kroki, pytania i odpowiedzi oznaczone w materiałach.


# NET-01-LS1 — Local Network Configuration

> Zakres źródłowy: strony 1–14.


### Lab Assignments & Solutions — strona 1

Computer Networking
Lab Assignment Introduction
& Solution to Networks
eo Vat NET-01-LS1
“alk F U | Local Network
Configuration
Copyright © 1996-2020 HackerU Ltd.
All Rights Reserved.


### Lab Assignments & Solutions — strona 2

Note: Solutions for the instructor appear in a green colored box.
G Lab Objective
Learn about and practice using CLI networking commands in Windows.
* Lab Mission
Configure a local network using CMD-based commands.
ea .
© Lab Duration
15-30 minutes
fe Requirements
e Familiarity with the Windows command line.
e Familiarity with the nslookup tool.
Lt

[ra] Resources
¢ Environment & Tools

Windows 7, 8, or 10

Internet connection


### Lab Assignments & Solutions — strona 3

Lab Task 1: Windows 10 Virtual Machine Installation
If you do not have a Windows 10 VM installed, set up a new machine.
You can follow the instructions in the Windows 10 Installation Guide located in the
Installation Guide module in your Canvas course.


### Lab Assignments & Solutions — strona 4

Lab Task 2: Local Network Configuration
In this task, you will use commands to view and document the local network
configuration of a Windows machine.
1 Open CMD on the local machine.

Press Win Key + R and type CMD.
2 Run the ipconfig command to display local PC network settings.

Type ipconfig and press Enter.

Connection-specific DNS Suffix . :

Ethernet adapter Bluetooth Network Connection:

3 According to the ipconfig command output, how many network cards are there?
Why do some PCs display information regarding more than one network card?
The ipconfig command displays information regarding all interfaces on the local
machine. For example, laptops usually have wired, wireless, and Bluetooth interfaces
installed.
4 Document the information in Notepad or a personal notebook.
Copy the details marked in red in Step 2 above.


### Lab Assignments & Solutions — strona 5

5 The command in Step 2 above does not show the physical and DNS address. Issue
the same command with the appropriate option to display the network settings in
more detail.

6 Which Help option displays all ipconfig option combinations and their purposes?

7 Which CMD command displays the physical address?

8 Run the cls command to clear the screen.

Page5


### Lab Assignments & Solutions — strona 6

Lab Task 3: Test Connectivity

In this task, we will verify connectivity to an internet based IP, and document

connection metrics such as latency and path.

1. Using the Ping command, verify connectivity between the local PC and another PC
in the same network (for example, the PC of an adjacent student or another device
on your network).

Ask another student for his/her IP address and ping it, or ping your default gateway.

2 Document the following details located in the ping statistics:

e Packets sent, received, and lost.
e Average round trip time.
Document only the details marked in red below.
C:\Windows \system32>ping 1@.21.6.3
Pinging 10.21.0.3 with 32 bytes of data:
Reply from 16.21.@.3: bytes=32 time-16ms TTL=128
Reply from 10.21.6.3: bytes=32 time=4ms TTL=128
Reply from 10.21.6.3: bytes=32 time=5ms TTL=128
Reply from 16.21.@.3: bytes=32 time=31ms TITL=128
\Approximate round trip times in milli-seconds:
Minimum = 4ms, Maximum = 31ms, Average = 12ms
i
3 Runtracert for the same target as in Step 1 above.
Run the tracert command for the IP address from Step 1 above.
C:\Windows\system32>tracert 10.21.6.3
Tracing route to 10.21.@.3 over a maximum of 3@ hops
2 4ms 4ms 7 ms 10.21.0.3
Trace complete.


### Lab Assignments & Solutions — strona 7

4 What is a Hop?
A router on the way to a packet's destination, from one network to another.
5 Document the number of hops.
C:\Windows \system32>tracert 168.21.6.3
Tracing route to 16.21.6.3 over a maximum of 38 hops
6 Use the ping command again to test connectivity to an external source (such as a
website or Google DNS public server, 8.8.8.8).
Ping an external source, such as a URL or public address (www.facebook.com, 8.8.8.8).
C: \Windows\system32>ping 8.8.8.8
Pinging 8.8.8.8 with 32 bytes of data:
Reply from 8.8.8.8: bytes=32 time=57ms TTL=55
Reply from 8.8.8.8: bytes=32 time=59ms TTL=55
Reply from 8.8.8.8: bytes=32 time=60ms TTL=55
Reply from 8.8.8.8: bytes=32 time=59ms TTL=55
Packets: Sent = 4, Received = 4, Lost = @ (0% loss),
Approximate round trip times in milli-seconds:
Minimum = 57ms, Maximum = 60ms, Average = 5S8ms


### Lab Assignments & Solutions — strona 8

7 Document the following details in the ping statistics:
e Packets sent, received, and lost.
e Average round trip time (latency as ms).
Document only the details marked in red below.
Reply from 8.8.8.8: bytes=32 time=S9ms TTL=55
Ping statistics for 8.8.8.8:
iWpproximate round trip times in milli-seconds:
Minimum S7ms, Maximum 6@ms, Average 5Bms
8 Run tracert for the same target as in Step 7 above.
Run tracert for the IP address in Step 7.
9 Document the number of hops.
1 6 ms 5 ms 8 ms 10.21.8.100
2 S ms 4 ms 38 ms b2q-252-97 .red.bezeqint.net [212.179.252.97]
3 6G ms 6 ms 6 ms bzq-179-16-121.cust.bezegint.net [212.179.16.121]
6 60 ms 6@ m 59 ms 108.170.252.65
i 62 ms 62 ms 62 ms 216.239.56.149


### Lab Assignments & Solutions — strona 9

10 Compare the findings. Why are the round-trip times and hop count results in
Steps 1-4 less than those in Steps 7-10?
The adjacent student's PC is in the same network, so no router is needed. The external
source is in a different network, which means the packet must be forwarded through
several routers.


### Lab Assignments & Solutions — strona 10

Lab Task 4: Domain Names and IPs
In this task, you will demonstrate knowledge of the nslookup command, document
your machine’s DNS servers, and find IP addresses of URLs.
1 Using the nslookup command, discover which DNS server is configured on the local
machine.
Type nslookup to enter resolve mode.
C:\Windows \system32>ns lookup
2 Using nslookup, what is the public IP address of www.cisco.com?
Default Server: dns.google
Addresses: 2a02:26f0:c00:584: :b33
www. cisco. com.akadns .net
wewds .cisco.com.edgekey net


### Lab Assignments & Solutions — strona 11

3 ADNS record can also work in reverse order. Which service or organization uses IP
address 185.60.216.35?
> 185.66.216.35
Server: dns.google
Name: edge-star-mini-shv-@1-frx5,. facebook. com
Address: 185.60.216.35
4 Press Ctrl+c to exit nslookup mode, or type exit, and close CMD.


### Lab Assignments & Solutions — strona 12

Lab Task 5: Domain CLI Vs GUI
In this task, you will configure your network interface using only the CLI.
There are two universal ways to communicate with a PC: via graphic interface (GUI), or
via a Command Line Interface (CLI).
The netsh command is run via the CLI, and is used to configure all network settings.
1 Open CMD as administrator.
Search for cmd, and right-click “Run as Administrator”.
w
=F
o Ea ~
& PD emder —
® ed commands
P mdb
P emda vs
2 amd
2 and nyse 1
==
a
o Ee 2D Web
«a Eo = @ a =
2 Display the local PC network configuration using netsh interface ip show config .
Command: netsh interface ip show config
Note: Interface names may be different.


### Lab Assignments & Solutions — strona 13

3 Configure the following addresses statically on the wired or wireless interface:
e |Pv4 192.168.0.5
e Subnet Mask: 255.255.255.0
e Default Gateway: 192.168.0.1
Use the following command:
netsh interface ip set address "Ethernet" static 192.168.10.5 255.255.255.0
192.168.0.1
Run:
netsh interface ip set address "Ethernet" static 192.168.10.5 255.255.255.0
192.168.0.1
Make sure to substitute “Local Area Connection*1” with the name of your interface (for
example “Ethernet”).
4 Use the command in Step 2 above to verify the new configuration.
Run: netsh interface ip show config
5 Which network protocol is responsible for allocating IP addresses and network
configurations dynamically to devices on the network?
DHCP
6 Revert the changes by enabling DHCP on the interface with the command:
netsh interface ip set address "Ethernet" dhcp
Run: netsh interface ip set address "Ethernet" dhcp
7 Disable the interface, with the following command:
netsh interface set interface "Ethernet" admin=DISABLED
Run: netsh interface set interface "Ethernet" admin=DISABLED
8 Enable the interface, with the following command:
netsh interface set interface "Ethernet" admin=ENABLE
Run: netsh interface set interface "Ethernet" admin=ENABLE


### Lab Assignments & Solutions — strona 14

9 Ping 8.8.8.8 to verify connectivity.
Run: Ping 8.8.8.8
Verify that the command was successful.


# NET-02-LS1 — Network Examination with Wireshark

> Zakres źródłowy: strony 15–33.


### Lab Assignments & Solutions — strona 15

Computer Networking
Lab Assignment Network
& Solution Fundamentals
ROLL) NET-02-LS1
ol TU Network Examination

with Wireshark
Copyright © 1996-2020 HackerU Ltd.
All Rights Reserved.


### Lab Assignments & Solutions — strona 16

Note: Solutions for the instructor are shown inside the green box.
G Lab Objective
The objective of this lab is to learn how to use Wireshark and how computers
encapsulate and send data.
%) Lab Mission
The mission of this lab is to capture various types of network traffic, and analyze the
data.
x) .
© Lab Duration
30-60 minutes
fe Requirements
¢ Knowledge of the TCP/IP model and data encapsulation.
e Knowledge of basic Wireshark filters.
oo

| Resources
¢ Environment & Tools

o Windows 10 VM

o Web browser

o Internet connection
e Extra Lab Files

o Wireshark-win64-4.0.5.exe


### Lab Assignments & Solutions — strona 17

Lab Task 1: OSI & TCP/IP
This task will review OSI & TCP/IP information previously learned.
1. What is the primary role of the Transport Layer and which are the two most
common corresponding protocols?
The transport layer handles the coordination of data transfer between two network
hosts: TCP and UDP.
2 Inwhich layer of the OSI model do protocols like DNS, HTTP, and SSH operate?
Application Layer (7).
3 Inwhich layer of OSI and TCP/IP models are source and destination logical
addresses added to the packet?
OSI - Network Layer (3), TCP/IP - Internet Layer (3).
4 Inwhich layer of OSI and TCP/IP are source and destination physical addresses
added to the frame?
OSI - Data Link Layer (2), TCP/IP - Network Access (1).
5 What does UDP do with corrupted or out-of-order packets?
Nothing, the destination discards corrupted packets.


### Lab Assignments & Solutions — strona 18

Lab Task 2:Wireshark Installation
In this task, we will install Wireshark.
1 Before you start, make sure your Windows 10 virtual machine’s NIC is configured
to NAT.
| Be cena | notwork
Bl sien sists Adele 2 stot ade +
Eh opty leient scone -
Dae | ue
EP woe |
Dus
[GBD stared Foes
a eK | Cane
2 Use the provided Wireshark installation file to install the software. Double-click
the file to start the installation.
3 Ifa message regarding “User Account Control” appears, click “Yes”.
) Do you want to allow this app to make changes to
© your PC?
4 Program name: — Wireshark installer for 64-bit Windows
Verified publisher: Wireshark Foundation, Inc.
File origin: Hard drive on this computer
Oshow dts
crete ee


### Lab Assignments & Solutions — strona 19

4 Click Next in the first setup page to begin.
A Wisharkacs Ob Setup = X
Welcome to Wireshark 4.0.5 64-bit
3 §) Setup
Th ward wl ude you auch the tation oF
Weer
Before staring theinstalatn, mate sure Wireshark rot
ick Non conve,
Cones!
5 Inthe next page, click “Noted”, for the license agreement.
A Wireinaican seat seup = 3
License Agreement
Place rev the ers ters before isang Wireshark 40.56¢bi r§
\reshrkis debuted under the GWU Genel ub Lense
1 UCHR BUCHER i
Veson 2 re 1951
Cerro (2 185, 1961 Fe Softnare Feud: ne
Franken Sree, Fh oer, cote, HA 21:0-1302USA
Everyone permed te coy and aavbute vebaim copes
of ts heros doument bot chang nt eon
Preantle
ucla formoet eft ar dic to take may yur :
This is not an end user license agreement (EULA). Its provided here for informational
Beeeesty
<a Core!
Page5


### Lab Assignments & Solutions — strona 20

6 Inthe next page, make sure all the components are selected, and click “Next”.
A Wireshark 4.05 64-bit Setup = x
‘choose Components
Croose whch features of iresha 4.0.9844Ht you nantto sta A
Tie lowes evant a availa frre
Sed meer
(A Tshark
1-7] Plugins & Extensions
BM Tools
Documentation
Description
scerequret:2510M8 — Foston your
aE aa
7 Inthe next page, make sure all the options are selected, and click “Next”.
Ai Wireshark 4.0.5 64-bit Setup = x
Adational Tasks
Create shorteuts and asscat le extensons A
cane
iveeshar str Men tem
atest Det con
Eaivresark uk eunch eon
festa Fae Eero
lassociate trace file extensions with Wireshark
mplog, ntar, out, pap, pcapne, pkig, pkt, rf5, snoop, syc, the, tr1, trace,
Teneo we a
aE Cone


### Lab Assignments & Solutions — strona 21

8 Inthe next page, select the installation destination folder, and click “Next”.
(@ Wireshark 4.05 64-bit Setup = x
Choose Install Location
Chooze the flier n hich to natal Weeshark 40.5 6b 4
Goose a drecoryin which total Wweshark
Destnaton Folder
space reared 231.08
ce aval: 18.368
etack ]
9 Inthe next page, make sure “Install Npcap 1.71” is selected, and click “Next”.
(Wireshark 4.05 64-bit Setup = x
Packet Capture
esha requres cher Npcap or WnPcap to capture ne meter data A
urrentyinstaled Np or WinPcap version
sted
Est cep 1.71
(Use Ade Renove Programs rt unnstal any undetected ol Nose o WP
portant nice
(i eee ee ee
'etstop nap a Amntator bere wpgradng Npcop 20 att oss cash epan
cet vmecp
Lear nore bout pcan and Wrap
ese) ea


### Lab Assignments & Solutions — strona 22

10 Inthe next page, click “Install” without changing anything.
The installation will begin.
A Wirernarcd 05 6abtSctop = x
‘USB Capture
Sm rae cape SE rae. na Pe aes rs
Current installed USiPczp version
tel
(Ditnstall usePcap 1.5.40
(Use Adc/Remove Programs first to uninstall any undetected old USEPcap versions)
eer oe
feral
Ite ths comfieconfcbeapesue/S
corer cee
az Za
11. When the installation process ends, click “I Agree” for the Npcap setup license
agreement.
@ Necop 171 Seup = x
license Agreement
memeecis eee
ck Riad TARA RBEE ‘i
hecan ins nacan.on) i Wins pate sifina iver and
library ard is copyright (c) 2013-2022 by Nmap Sofbvare LLC (“The Nmap
[Project’). Allrights reserved.
ren touch oxen source code's pub avaiable for review itis
fotapenseucesftere arday fot e eastbutedr sed ether
ferinerewioat specs permason Fon tie Nap Projet. The
tncrd (res) vrcon sual ned te stlaten ov fhe <
(ieee i eres Srey y
mrosatinsal ep U7
Core!


### Lab Assignments & Solutions — strona 23

12 Inthe next page, leave all the options unselected and click “Install”.
(G@ Npcap 1.71 Setup - x
Installation Options
af eA Foose reve te loving cotonsbefeeintalina Neca 1.71
Ciecinearives ace e Aneeteercan
Tpsepertran sc2.11 ac and monitor mode) for weless aanters
[1 Jrstall Npcap in Win?cap API-compattible Mode
ack corel
13 When the installation ends, click “Next”, and in the next window, click “Finish”.
The Wireshark installation process will continue.
G@ Nocap 1.71 Setup, ee
Instalition Compete
= Setup nas completed succesful
Conpleted
EEE
Show deta
@ Npcap 1.71 Setup a
Finished
J Thank you frinstingHocap
Te ee erate ree ene
krish to dese is ier


### Lab Assignments & Solutions — strona 24

14 When the installation ends, click “Next”, and in the next window, click “Finish”
without selecting “Show News”.
A Wireshark 4.05 64-bit Setup =
Irstallesion Complete
Setup was convicted succor 4
‘Completed
aaa SESS
Extract wenloize pedis ona A
bat secon ey
exvact tay astong
Seek monavien
extract omeranal.ona
Extract omoutong
Output fodder: C:\Program Files|Wireshark\Wireshark User's Guide
cut fer: C: Progam Flesiesharc
ext fa.nd
competed e
=)
Al Wireshark 4.05 62-bit Setup =
Completing Wireshark 4.0.5 64-bit
eam
\ireshark 40,564bithasbeen nstaledon your comute,
chris dose Setup
Cstow News
Te a


### Lab Assignments & Solutions — strona 25

Lab Task 3: Use Wireshark to Examine Live Network Traffic
In this task, we will install Wireshark and become familiar with the interface.
Part 1 — Learn about the Wireshark Dashboard
1 Choose the network adapter in use, and who you want to view data on.
The graph shows which interface is active.
(The Wireshark Network Analyzer - og x
Ae SO URREQ oo eT IBBaaan
Bexesson.. + |
Capture
using this filter: Wlenter a capture fiter ~) Allinterfaces shown ¥
(ethane Wl
Bluetooth Network Connection
EthernetO rw
Note: The answers in this section were taken from a lab environment.
Since you are working in a different network environment, some of the answers may be
different.
2 Dashboard View:
a) The top screen or bar contains the program’s tools, such as preferences,
settings, and the search bar.
ag26 1 i Qe
W/Apply a display filter... <Ctr-/> |
b) The windows in the middle show the live network traffic on the network card
(adapter). Data is presented as frames.
c) The screen at the bottom displays information for a selected frame.


### Lab Assignments & Solutions — strona 26

Part 2 — Examine Live Network Traffic
3 Start capturing the network by clicking the Wireshark icon a
4 Opena web browser (recommended: Edge or Firefox).
5 Browse to http://juice-shop.herokuapp.com/#/ and immediately after the web
.
page is loaded, click the stop button .
6 Take acloser look at a client requesting a web page from a server.
Use the search bar to display only the HTTP packets.
sauce RO VeeBreT aaa
(=o RE
me ore = re 7
1. 4.801384 10.0.2.15 13.226,6.34 HTTP 383 GET //MEOWSDBGMEQuQjAJBUrDgMCGgUABBSLWZ6EWSgdYc9UaSEaal j jE.
1. 4.807717 13.226.6.34 _10.0.2.15 _OCSP_338 Response
be
Ju 305.849... 10.0.2.15 52.16.192.249 HTTP 403 GET /styles.css HTTP/1.1
7. 305.849.. 10.0.2.15 52.16.192.249 HTTP 430 GET /runtime-es2015.js HTTP/1.1
> Frame 749: 385 bytes on wire (3080 bits), 385 bytes captured (3080 bits) on interface \Device\NPF_{872B33F-4678 ~
» Ethernet II, Src: PcsCompu_ic:ba:@c (08:00:27:1c:ba:@c), Dst: RealtekU_12:35:00 (52:54:00:12:35:00)
» Internet Protocol Version 4, Src: 10.0.2.15, Dst: 52.16.192.249
» Transmission Control Protocol, Src Port: 49687, Dst Port: 80, Seq: 1, Ack: 1, Len: 331
e030 ff ff 02 7e G0 G0 47 45 54 20 2f 20 48 54 54 50 GE T / HTTP fal
0042 2# 31 2e 31 @d @a 41 63 63 65 70 74 3a 20 74.65 /1.1--Ac cept: te
0050 78 74 2 68 74 6d 6c 2c 20 61 70 70 6c 69 63 61 xt/html, applica
060 74 69 6F 6e 2F 78 68 74 Gd 6c 2b 78 6d 6c 2c 28 tion/xht ml+xml,
0070 69 6d 61 67 65 2f 6a 78 72 2c 26 2a 2F 2a Gd Ga = image/jx r, */*+-


### Lab Assignments & Solutions — strona 27

7 Click the GET HTTP packet sent from the local PC to the server.

(i Copturing rom Ethemet 2

File Edit View Go Capture Analyze Statistics Telephony Wireless Tools Help

AMA CO 1M ROCeeoeeezBaaar

Time source Destination Protcch Length info
154 0.375544 93.184.220.29 10.0.2.15 ocsP” 853 Response
166 0.447538 192.124.249.31 10.0.2.15 PKIX-.. 1068 Certificate Revocation Li:
235 0.608679, 10,0.2.15 (192.124. 249.23 HTTP 274 GET //MEKWRZBFMEMWwQTAIBgUI

| 266 0.718556 192.124.249.23_10.0.2.15 OcsP 956 Response
296 0.807185 52.16.211.175 (10.0.2.15 HTTP 45@ HTTP/1.1 304 Not Modified
303 0.810648 10.0.2.15 52.16.211.175 HTTP 529 GET /styles.css HTTP/1.1

| 3e4 0.810929 10.@.2.15 52.16.211.175 HTTP 554 GET /runtime-es2015.js
‘Accept: text/html, application/xhtml+xml, image/jxr, */*\r\n
Accept-Language: en-US\r\n
User-Agent: Mozilla/5.@ (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko)|
Accept-Encoding: gzip, deflate\r\n
Host: juice-shop.herokuapp.com\r\n
If-Modified-Since: Tue, 21 Jul 2@2@ 26:01:20 GMT\r\n
If-None-Match: W/"785-17372f75b4a"\r\n
Connection: Keep-Alive\r\n

> Cookie: cookieconsent status=dismiss\r\n
\r\n
Full request URI: http://juice-shop.herokuapp.com/
<


### Lab Assignments & Solutions — strona 28

8 Click each header to view the encapsulated date (logical ports, IP, and MAC
address).
(Gi Capturing from Ethernet 2
Fle Edt View Go Capture Anahze— Statics Telephony Wireless Tools Help
mao RB OiQenseeseBacel
(eo
i ES Destnaton Protech Length no
154 0.375544 93.184.220.29 —10.0.2.35 ocsp 853 Response
166 0.447538 192.124. 249.31, 10.0.2.15 PKIX-.. 106@ Certificate Revocation List
(235 0.608679 10.0.2.15 192.124,249.23, HTTP” 274 GET //MEkwRZBFMEMwQTAIBgUrDgMCGe
| 266 0.718556 192.124.249.23 10.0.2.15 ocsP 956 Response
pe 278 0.724957 «10.0.2.15 52.16.211.175 HTTP 509 GET / HTTP/1.1
(296 0.807185 $2.16.211.175 10.0.2.15 HTTP 45@ HTTP/1.1 3@4 Not Modified
+ 303 0.810648 10.0.2.15 52.16.211.175 HTTP. 529 GET /styles.css HTTP/1.1
| 304 0.810929 10.0.2.15 52.16.211.175 HTTP 554 GET /runtime-es2015.js HTTP/1.1
Frame 278: 5@9 bytes on wire (4972 bits), 509 bytes captured (4072 bits) on interface \Device\NPF_{87
Ethernet II, Src: |PcsCompu_ic:ba:@c (@8:00:27:1c:ba:@c), Dst: RealtekU_12:35:8@ (52:54:00:12:35:00)|
Internet Protocol Version 4, Sre: 10.0.2.15, Dst: 52.16.231,175
\ Transmission Control Protocol, Sre Port: 49930, Dst Port: 80, Seq: 1, Ack: 1, Len: 455
Destination Port: 80
[Stream index: 34]
[TCP Segment Len: 455]
Sequence number: 1 (relative sequence number)
Sequence number (raw): 3952001607
[Next sequence number: 456 (relative sequence number)]
Acknowledgment number: 1 (relative ack number)
Acknowledgment number (raw): 1212293
<
9 Document the following details:
a) What are the logical port source and destination?
b) What are the logical source and destination addresses?
c) What are the physical source and destination addresses?
{coloring fute none: x17] A
Coloring tule string: Rete || tep.port =» a9 [| http
nee Te Srer PRC Te De Be SA ROTTS BOTOC) DHE RICO AE GETS GH SU OOD STOR)
frcernet Protacol Version &, sect 10:0.2-18, Dstt $2-26-211.475
SS |
Source Pore aE
Destination Port: 88
{streen indore 54]
{reo seanene Len: #55]
Sequence rumver (raw) 3952003607
[het sequence number: 458, (relative sequence ninber)]
Acknowledge munber: 1. (relative ack unber) :
Protocol Layer 4: TCP
Source Port: 49930 (usually selected randomly from the dynamic port range).
Destination Port: 80 (used by HTTP for web page transfer).
Flag: We can understand by observing the flags that this is the first packet of the TCP
3-way handshake process.


### Lab Assignments & Solutions — strona 29

.
Se tare
® iat = Header Length: 20 bytes (5)
Divrerenciatee services Field: ere0 (O5CP: C$6, ECN: NOE-ECT)
Total Length: 495
Teentification: exscS0 (23652)
Foes: extese, Don's frageent
Frogeent offsets 8
Tine to Liver 128
protocet: Top (6)
Neder checksum: 0080 [validation disabled]
Destination $2.16.2.375 :
Layer 3 protocol: IPv4
Source address: 10.0.2.15 (local machine)
Destination address: 52.16.211.175 (Juice shop hosting server)
{coloring tute tone: HTTP] 5
[eatoring fue strings neep | tep.pore on 66 || netoa
Tihernct Ty Srer PevComputetbaTee (au @O-a7 acrbarec)s OE) Rest ATAETGO (GTiBe GOTT)
Devtination: Realeet 17:35:00 (52°56:60:12:35:20)
Scurces PesCompu te:ba:8c_(65;00;27:1c:ba:6c)
en area (cores)
neernet erotocel Verso S#4! 10:0.2:5, ose! 52.26.212.175
> Hataassen cover seetosau cieiescee cael bar pees! oe] Gags Vneuslarlion aay
Source Pores 19930
Destination Port: 86
{steeen incers 34)
{ter segnent ten: 455]
Sequence murber (ras): 3952661667 S
Layer 2 protocol: Ethernet
Source address: 08:00:27:1c:ba:0c (local machine)
Destination address: 52:54:00:12:35:00
chernet Ht, Srcr Reolteni 12 35100 (GUS4r00 12:35:00), Oskr PesCompu_Terber8e (WBr@8:27 Ter¥ar80) 5
internet protocol Version 8, sre: $2-16:211375, ost 10.0.2.5
Hransnission control Pratoeeh, sre Ports 89, ost Port: 49930, seq: ty Aki 456, Len: 396
Servers Comoy\r\n
Content-Length: @\r\n
Access Control-Allow Origin: "rn
xcontent-Type-options: nosniff\rvn
rteane options: SSHEORZeDV\P\n
Feature-Policy: paynent"se1®"\r\0
secept-Ronges? bytes\rin
Cecne-Conerot: pubtic, nax-agee8\rin
Castedified: Twe, 21 dul 2620 20:61:20 GHT\r\n
fogs w/"785-17572¢7504a"\r\n
Date: ed, 22 201 2020 69:17°32 GHT\r\n
Vier 1-1 vegurvrin
\rn
Sane aT 0,082228000 seconds)
eauest in fran 278 l
Response packet: Note that the source and destination addresses switched places.


### Lab Assignments & Solutions — strona 30

Lab Task 4: Capture Network Traffic to a File and Analyze it
In this task, we will capture packet data and save it to our disk. We will then open the
saved file and look for specific data using filters.
1 Click the Wireshark icon @ to start capturing.
2 Open the CMD and send a ping to 8.8.8.8
EM Administrator; C\Windows\system32\cmd.exe aa oOo »*
Microsoft Windows [Version 16.0.18362.720] A
(c) 2019 Microsoft Corporation. All rights reserved.
Pinging 8.8.8.8 with 32 bytes of data:
Reply from 8.8.8.8: bytes=32 time=30ms TTL=53
Reply from &.8.8.8: bytes=32 time=26ms TTL=53
Reply from 8.8.8.8: bytes=32 time=24ms TTL=53
Reply from 8.8.8.8: bytes=32 time=23ms TTL=53
Ping statistics for 8.8.8.8:
Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),
Approximate round trip times in milli-seconds:
Minimum = 23ms, Maximum = 3@ms, Average = 25ms
C:\Users\User>
w
3 Browse to http://hack-yourself-first.com/
4 Stop capturing using the stop button M@.


### Lab Assignments & Solutions — strona 31

5 Click File and then Save as. Name the file capture1 and save it in the Desktop
folder.
rere
ACO UBRE CeseFiaeeaaaa
—— EE SS
Md Wireshark . Save Capture File As x
Savein: | TE Desktoo -] @& & Br
ao . Date mecified pe 18.211.118.21
No iterns match your search. 192.168.6.36
Seatiad 192.168.6.36
Bw 18.211.118.21
Desktop 192.168.6.40
i 192.168.6.36
192.168.6.40
bs 192.168.6.31
& 192.168.6.36
This PC 192.168.6.31
52.200.65.196
@ 192.168.6.36
meee be > 52.200.65.196
Flenane sae pee
Seveestwme: | Yeshak.-peaona (nr a ma“Doapnt Cancel EG ae
52.20.0.32
te
Ci compress wth gz —x— SSS
> rrame 4: 13% vytes on wire (irs ures), 198 vyLes Captured (1104 bits) on int
Ethernet IL, Src: IntelCor_@c:8e:e2 (38:08:25:0c:8e:e2), Dst: Netgear_1b:b7:8
Internet Protocol Version 4, Src: 192.168.6.36, Dst: 204.79.197.200
Transmission Control Protocol, Src Port: 50143, Dst Port: 443, Seq: 1, Ack: 1
Transport Layer Security
6 Close Wireshark.
7 Double-click capture1.pcap to open the file.
8 Using the appropriate display filter, display only the DNS packets.
Note: if you fail to find the query, flush the DNS cache with the command
ipconfig /flushdns and repeat steps 3-8.
a AME vr)
i oy eee, Pewee a
2.234844 10.6.2.15 8.8.8.8 DNS 72 Standard query @x@dc9 A www.bing.com
3.6,311586 8.8.8.8 10,0.2.15 DNS 193 Standard query response @x@dc9 A www.bing.com CNAME a-@@01.a-afden...
59 1.202924 10.€.2.15 162.159.27.72 DNS 139 Dynamic update @xilbd SOA Cyber.com CNAME AAAA A A 10,0.2.15
60 1.259667 _162.159.27.72_10.0.2.15 DNS __69 Unknown operation (8) response @x1ibd Not implemented SOA Cyber.com
+3.. 29.178947 8.8.8.8 10.0.2.15 DNS 157 Standard query response @xSa3e No such name A hack-yourself-fiurst..
3.. 36.128947 10.6.2.15 8.8.8.8 DNS 83 Standard query @xd68c A hack-yourself-first.com
3.. 36.220372 8.8.8.8 10.0.2.15 DNS 99 Standard query response @xd68c A hack-yourself-first.com A 104.42...
3.. 36.769431 10.6.2.15 8.8.8.8 DNS 77 Standard query 9x99de A urs.microsoft.com


### Lab Assignments & Solutions — strona 32

COMMANDO 22/67/2026 13:45:26.38
IC: \Windows\system32+ipconfig /flushdns
Windows IP Configuration
successfully flushed the DNS Resolver Cache.
9 Document the following details:
a) Which Layer 4 protocol is used to encapsulate the Layer 4 header.
b) What are the source and destination logical ports?
c) What is the default DNS server configured on your machine, according to the
Layer 3 header?
Frame 729: 84 bytes on wire (672 bits), 84 bytes captured (672 bits) on interface \Device\NPF_{87C2
Ethernet II, Src: PcsCompu_1c:ba:@c (@8:0@:27:1c:ba:@c), Dst: RealtekU_12:35:0@ (52:54:00:12:35:00)
Internet Protocol Version 4, Src: 10.@.2.15, Dst: 8.8.8.8
~[ser-Datagran Protocol, Src Port: i464, Dst Port: 53]
Source Port: 61464
Destination Port: 53
Length: 50
Checksum: @x1c62 [unverified]
[Checksum Status: Unverified]
[Stream index: 13]
[Timestamps]
Layer 4 protocol: UDP
Source port: 61464
Destination port: 53
10 Which filter will display all packets sent to port 53?
sec OT DRG QewBF2SSQaae |
2 ©.234844 10.0.2.15 8.8.8.8 ONS 72 Standard query @x@dc9 A www.bing.com
59 1.202924 10.0.2.15 162.159.27.72 DNS 139 Dynamic update @x11bd SOA Cyber.com CNAME AAAA A
2.. 29,109166 10.0.2.15 8.8.8.8 DNS 84 Standard query @xSa3e A hack-yourself-fiurst.com
3.. 36.128947 10.0.2.15 8.8.8.8 DNS 83 Standard query oxd68c A hack-yourself-first.com
3... 36.769431 10.0.2.15 8.8.8.8 DNS 77 Standard query @x99de A urs.microsoft.com
[+ Tm 37.410783 10.@.2.15 8.8.8.8 DNS 84 Standard query @x5d2a A www.google-analytics.com |


### Lab Assignments & Solutions — strona 33

11 Using the appropriate display filter, display only the Ping packets.
i
No. Time ‘Source Destination Protocol Length Info
84 8.714769 10.0.2.15 8.8.8.8 ICMP 74 Echo (ping) request
85 8.783218 8.8.8.8 10.0.2.15 ICMP 74 Echo (ping) reply
87 9.734447 10.0.2.15 8.8.8.8 ICMP 74 Echo (ping) request
88 9.802806 8.8.8.8 10.0.2.15 ICMP 74 Echo (ping) reply
89 10.749410 10.0.2.15 8.8.8.8 ICMP 74 Echo (ping) request
12 Document the following details:
a) How many requests and replays are shown?
b) Why doesn’t ICMP have a logical port number listed in the packet capture?
Request Packets: 4
Replay Packets: 4
ICMP is a Layer 3 protocol, meaning it does not have a logical port. To verify this, you
can view the header of the packet, and note that there is no Layer 4 header.
13. Which filter will display all packets sent to the 8.8.8.8 host?
[| ipdst--8.8.8.8
No. Tine source Destination Protocol
12 @.1655@9 10.0.2.15 Suerers DNS
35 0.249834 10.0.2.15 8.8.8.8 DNS
82 8.313399 10.0.2.15 8.8.8.8 DNS
— 848.714769 10.0.2.15 8.8.8.8 CMP
87 9.734447 10.0.2.15 8.8.8.8 ICMP


# NET-03-LS1 — Packet Tracer Installation

> Zakres źródłowy: strony 34–46.


### Lab Assignments & Solutions — strona 34

Computer Networking
Lab Assignment Switch & IOS
& Solution Fundamentals
. ai NET-03-LS1
a U Packet Tracer Installation


### Lab Assignments & Solutions — strona 35

Computer Networking
Lab Assignment Switch & IOS
& Solution Fundamentals
. ai NET-03-LS1
a U Packet Tracer Installation


### Lab Assignments & Solutions — strona 36

Note: Solutions for the instructor are shown inside the green box.
*@) Lab Objective
Become familiar with Cisco Packet Tracer software.
4) Lab Mission
Create a Cisco account and download Packet Tracer to explore the features it
provides.
CN) *
@) Lab Duration
30-60 minutes
{@ Requirements
e@ Working knowledge of browsers
Lt}

| Resources
e Environment and tools

o Web browser
e External links

o Cisco registration:

id.cisco.com/signin/register
o Networking Academy registration/Packet Tracer download:
netacad.com/courses/packet-tracer/introduction-packet-tracer


### Lab Assignments & Solutions — strona 37

Lab Task 1: Cisco Account Registration
In this task, you will create a Cisco account to download the Packet Tracer
application.
1 Using a browser, navigate to the Cisco registration link provided in the
resources section above.
& > CB hitps://id.cisco.com/signin/register
2 _ Fill in the fields with your personal information (do not use fake data). This
information will be used to download and work with Packet Tracer.
Create Account
Email
First Name
Last Name
Country or Region .
Company
Password
Confirm Password


### Lab Assignments & Solutions — strona 38

Lab Task 2: Downloading & Installing Packet Tracer
In this task, you will download and install the Packet Tracer application.

1 Navigate to the second link provided in the lab resources to register for
Cisco’s Network Academy. Then on the top right, log into the account you
made in Lab Task 1.

3 en e
Introduction to Packet Tracer B i F Se’: .
r fi a X
Hands-On Practice @ 02 0s :


### Lab Assignments & Solutions — strona 39

SS a a aaa aa
2 Go to the Resources drop-down and select Download Packet Tracer.
inluealai prsicli My NetAcad Resources Courses Careers More
Home / I'm Learning Certification Exams & Discounts
I'm Learning Find an Academy
Courses I've Enrolled In AU Resources
Alumni Courses
> 4 o Ended
acm
Introduction to Packet Tracer English 1020
Cisco Virtual Academy
3 Scroll down to Download and choose the 64-bit download version.
Note: You should be signed into the Cisco account you previously created.
+ For oNAY.02, Packet Taeer8.0 64 the minimum version ene acs an new PTSAt® work oper
Linux Desktop Version 8.0 English
smacos Version 80 nls
ite


### Lab Assignments & Solutions — strona 40

SS a a aaa aa
4 Click the downloaded .exe to start the installation process.
Windows Desktop Version 7.3.0 English
64 Bit Download 32 Bit Download
Open ion 7.3.0 English
Show in folder |
An Enalich
WD PacketTracer-7.3.0-...0%
LM 0 Type here to search oO [oa g
5 Allow the program to make changes to the device. Allowing the application
to make changes is a Windows feature that helps prevent unauthorized
changes. The changes can be approved only by an administrator.
ee Cisco Packet Tracer
Verified publisher: CISCO SYSTEMS, INC.
File origin: Hard drive on this computer
Show more details
a *


### Lab Assignments & Solutions — strona 41

ee
6 Accept the agreement to continue the installation process.
License Agreement
Please read the following License Agreement. You must accept the terms of this
agreornent before continuing with the metalation.
DOWNLOADING, INSTALLING, OR USING THE CISCO PACKET TRACER SOFTWARE
(CONSTITUTES ACCEPTANCE GF THE CISCO END USER LICENSE AGREEMENT
("EULA" https://vww.cisco.com/c/en/us/about/legal/ cloud-and-
Softuare/and user icense- agreement trl) AND THE SUPPLEMENTAL END USER
|LICENSE AGREEMENT FOR CISCO PACKET TRACER (""SEULA"
Itosi/wrecsco com/c/dam/en us/ebout/doing busiess/leal'seula/cisco-packet:
[racersoftware.pd) IF YOU DO NOT AGREE TO ALL OF THE TERMS OF THE EULA
JAND SEULA, THEN CISCO SYSTEMS, INC. ("CISCO") IS UNWILLING TO LICENSE
|THE SOFTWARE TO YOU AND YOU’ARE NOT AUTHORIZED TO DOWNLOAD,
INSTALL OR USE THE SOFTWARE.
OT do not accept the agreement
eH
7 Select a path for the program's files.
Select Destination Location >
Where should Cisco Packet Tracer 8.0 64Bit be installed? a
| Setup will install Cisco Packet Tracer 8.0 64Bit into the following folder.
To continu, cick Next. If you woul ke to selec a cfferent folder, cick Browse
Atleast 46,6 MB of ree diskspace i required
co =


### Lab Assignments & Solutions — strona 42

SS a a aaa aa
8 Select a name for the start menu folder.
Note: It is recommended to leave the name as-is.
Fy =
Select Start Menu Folder ~
Where should Setup place the program's shortcuts? @
-L. setup wil create the program's shortcuts inthe folowing Start Menu folder.
To continue, click Next. If you would like to select a different folder, click Browse.
Browse.
Tas canal
9 Create a shortcut for ease of access.
PA a
Select Additional Tasks Se
Which additional tasks should be performed? as
Select the additional tasks you would like Setup to perform while installing Cisco
Packet Tracer 8.0 64Bit, then click Next.
Adeitional shortcuts:
(icreate a Quick Launch shortcut
co cme


### Lab Assignments & Solutions — strona 43

———————— = EEE Eas
10 Click Install to begin the process.
Ready to Install
‘Setup is now ready to beain installing Cisco Packet Tracer 8.0 64Bit on your A
computer ‘Sz
ck Instal to continue withthe installation, or cick Back f you want to review or
change any settings.
Destination location:
C:\Program Files\Cisco Packet Tracer 8,0
Start Menu folder:
Cisco Packet Tracer
Additional tasks:
‘Addtonal shortcuts:
Create a desktop shortcut
11 When the installation ends, select Launch Cisco Packet Tracer and click
Finish.
~~ Completing the Cisco Packet
FeV Tracer 8.0 64Bit Setup Wizard
= ‘Setup has finished installing Cisco Packet Tracer 8.0 64Bit on
your computer. The application may be launched by selecting
the installed shortcuts.
Click Finish to exit Setup.


### Lab Assignments & Solutions — strona 44

———————— = EEE Eas
12 Once Packet Tracer launches, select No in the message that asks about
running multi-user.
Networking Hy
Academy. Cisco Packet Tracer
.¢
2) Would you like to run multi-user when application starts?
"
© Copyright CisgB 2021
13 Inthe Windows Security Alert that appears, select Private networks and
click Allow access.
[ i Windows Security Alt x
6 Windows Defender Firewall has blocked some features of this
app
indo Defender Preval hs bled sane eae of Pade Tac Exetel pe
popes
ome: ‘Packet Tree Exeable
Pate Crogan essen pct Wace 7.3.06
(oielvareoe
et i ace ib cnemuse tse ta
[lhenetws, su as ese prs and cffee sha (pt ecamended
caine hese heersoherovelte oho sear)
e=T


### Lab Assignments & Solutions — strona 45

SS a a aaa aa
14 Sign in using the email you provided in Lab Task 1.
@s
EN
stftatfie
cisco
Sign in
Username or Email
-
15 Provide the password for the account.
<Back @s
AT
cisco
Welcome
Username or Email
Dummy@example.com
Password
Forgot Password?


### Lab Assignments & Solutions — strona 46

16 You should now be able to work with Packet Tracer.
fF
Sqetdveese ge
om 4 re PS RRR Ro wee ee mene ee


# NET-03-LS2 — Initial Cisco Device Configuration

> Zakres źródłowy: strony 47–70.


### Lab Assignments & Solutions — strona 47

Computer Networking
Lab Assignment Switch & IOS
& Solution Fundamentals
4 NET-03-LS2
Ta Initial Cisco Device
at U Configuration
Copyright © 1996-2020 HackerU Ltd.
All Rights Reserved.


### Lab Assignments & Solutions — strona 48

Note: Solutions for the instructor are shown inside the green box.
*@) Lab Objective
Learn how to set basic configurations on a switch using Cisco IOS commands.
bs Lab Mission
e Connect to and access the device IOS using the out-of-band management
method.
e Explore and navigate the different Cisco IOS modes.
e Understand and practice Cisco IOS commands used to configure a network
device for the first time, focusing on switch settings.
ea .
©) Lab Duration
30-60 minutes
fe Requirements
e Basic understanding of IOS commands and navigation.
oo
| Resources
e Environment & Tools
Cisco Packet Tracer 7.2.2 or later
e Extra Lab Files
NET-03-L2.pka


### Lab Assignments & Solutions — strona 49

Instructions for PKA Lab Files
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
Ee ee fT a cmt
Please refer to the exercise document and carefully follow the — —
See the percentage of completion a the right-battom comer to = Na ° a
determine your progres, Fi nae ¢ ote
‘Note: The Optional and Bonus section are not scored. XK Senice Inconect 1 ie
Good bia + nooo ° other
qo Sc ee = on) PEL sae ema Ot °
PKA Solution
To view the solution or edit the lab file, you can simply click the "Wizard hat" icon and
enter the following password: C!ScOM@ster
Right-click the "Answer network" tab and then click "Show Answer network".
Note: Be careful not to change anything so that the lab will remain intact.


### Lab Assignments & Solutions — strona 50

Lab Task 1: Access the Device
Connect to a switch with a console cable and gain access to the console.
Note: If the lab opens with missing parts, configurations, or errors, refer to the last task
(Task 4) in the lab for guidance.
1 Click the connections box # at the bottom left corner and select the console
cable “.
Bs —
ay CS a) ales ESE Pale
cr | and
a ee
2 Connect one end of the cable to the RS-232 port on the admin PC, and the other
end to the Console port on the switch.
Flotgr1
Admin PC
Userl -
User2


### Lab Assignments & Solutions — strona 51

3 Now that you established a physical connection, start the terminal session, as
follows:
=
Click the admin PC, navigate to the Desktop tab, and click the Terminal icon Ba
Then click OK (accept the default settings).
Note: The messages that appear on the screen are part of the boot process.
® admin ec ist 2nd - op x
Physical Confo [Dosen] Programming Janrbutes
= <> lA =| Pva [rvs J
=e v
Cte
B Admin PC = a x
Physical Config Deaton Progamming Atributes
Per Corfaration
Dts Per Second 00 5
Date Bits 5 z
Pay ie z
Stop Bits 1 3
Flow Coil None z
te
Page5


### Lab Assignments & Solutions — strona 52

4 When the boot ends, press Enter to begin.
B Laptopo os o x
Physical Config Desktop Programming —_ Attributes
[Terminal
[Top


### Lab Assignments & Solutions — strona 53

5 Answer the following questions:
a. List the four IOS modes of Cisco devices.
b. Which cable type and what kind of software are required for out-of-band
management (initial device configuration)?

c. Which device components store operating system files?
d. Do Cisco devices run diagnostic tests upon startup?

A. 10S Modes:
(1) User EXEC Mode - Limited monitoring commands.
(2) Privileged EXEC Mode - View and manage configuration files (using copy and
show commands).
(3) Global Configuration Mode - Configure general device settings (such as device
name, user names, passwords, etc.).
(4) Interface or Line Configuration Mode — Configure interface settings (such as IP
addresses).

B. Console Cable and Terminal Software, such as PuTTY.

C. Flash memory

D. Yes, POST (Power-On Self-Test).


### Lab Assignments & Solutions — strona 54

Run all commands on S1-Floor1.
Tip: Pay attention to the prompt!
Step 1— Explore the User EXE Mode
Note: The commands are also valid on a router IOS system.
1 Welcome to User EXEC mode. Type ? and view the list of commands available in
this mode.
Press RETURN to get started!
Switch>?
Exec commands:
connect Open a terminal connection
disable Turn off privileged commands
disconnect Disconnect an existing network connection
enable Turn on privileged commands
exit Exit from the EXEC
logout Exit from the EXEC
ping Send echo messages
resume Resume an active network connection
show Show running system information
telnet Open a telnet connection
terminal Set terminal line parameters
traceroute Trace route to destination


### Lab Assignments & Solutions — strona 55

2 The show command in the list displays system settings. Enter show and ? (with a
space between them).
Choose the correct command combination from the list to display the clock. The
clock appears not to be set because in this mode we do not have permission to
configure it.
Switch>show ?
arp Arp table
cdp CDP. information
clock Display the system clock
crypto Encryption module
dtp DTP information
etherchannel EtherChannel information
flash: display information about flash: file system
history Display the session command history
interfaces Interface status and configuration
<output omitted>
Switch>show clock
*@:9:32.744 UTC Mon Mar 1 1993


### Lab Assignments & Solutions — strona 56

Step 2 — Explore the Privileged EXE mode
3 Type ? again and locate the Enable command. Enter the command to move to
the next mode.
This mode (#) is called Privileged EXEC, and is meant only for troubleshooting and
file system management.
Switch>?
Exec commands:
connect Open a terminal connection
disable Turn off privileged commands
disconnect Disconnect an existing network connection
exit Exit from the EXEC
<output omitted>
Switch>enable
Switch#


### Lab Assignments & Solutions — strona 57

4 Set the clock to the correct date and time. Type clock set with ? and add the
missing information. Check each time if anything else is missing by adding ? at
the end of the command. Then, verify the clock settings using the show clock
command.

Switch#clock set ?
hh:mm:ss Current Time
Switch#clock set 19:41:00 ?
<1-31> Day of the month
MONTH Month of the year
Switch#clock set 19:41:00 14 september ?
<1993-2035> Year
Switch#clock set 19:41:00 14 september 2019 ?
<cr>
Switch#clock set 19:41:00 14 september 2019
Switch#show clock
19:41:4.345 UTC Sat Sep 14 2019

5 Enter conf and press the TAB key to auto-compete the command. Press the
spacebar with ?. The only option is Terminal. Type t and press the TAB key. Press
Enter to move to Global Configuration mode. Continue with Task 3.

Switch#conf
Switch#configure ?

terminal Configure from the terminal

<cr>
Switch#configure t
Switch#configure terminal
Enter configuration commands, one per line. End with CNTL/Z.
Switch(config)#


### Lab Assignments & Solutions — strona 58

Lab Task 3: Initial and Security Settings
Secure access to the switch using a password and a banner.
Step 1— Configure the device name and create accounts
Tip: All of the required commands for this exercise can be found in the presentation or
textbook in the Initial Device Configuration section.
1 Set the device name to $1-Floor1.
Switch(config)#hostname S1-Floor1
2. Create a user account with the following details:
Username: Admin
Password: p@nd@
S$1-Floor1(config)#username Admin password p@nd@
Step 2 — Configure security settings
3 Set the enable password to c!scO
S1-Floor1(config)#enable password c!sc@
4 Set an appropriate security message (banner):

Access to this device is for authorized personnel only!
S$1-Floor1(config)#banner motd #Access to this device is for authorized
personnel only!#


### Lab Assignments & Solutions — strona 59

Step 3 — Secure the console port and verify settings
5 Secure access to the console port by setting username and password
authentication on the port. To enter the port configuration use the command line
console 0 to set the username and password use the command login local.
S1-Floor1(config)#line console @
S$1-Floor1(config-line)#login local
S$1-Floor1(config-line)#exit
6 Return to Privileged mode.
$1-Floor1(config)#exit
S1-Floor1#
%SYS-5-CONFIG_I: Configured from console by console
7 Using show running-config, display device settings, and verify that the system is
set up correctly.
The output should be similar to the following (notice the highlighted text):
$1-Floorl#show running-config
Building configuration...
Current configuration : 1234 bytes
!
version 12.2
no service timestamps log datetime msec
no service timestamps debug datetime msecno service password-encryption
enable password c!sc@
!


### Lab Assignments & Solutions — strona 60

!
!
spanning-tree mode pvst
spanning-tree extend system-id
!
interface FastEthernet0/1
!
<output omitted>
!
interface GigabitEthernet0/1
!
interface GigabitEthernet0/2
!
interface Vlan1
no ip address
shutdown
!
banner motd “CAccess to this device is for authorized personnel only!*C
!
!
!
line con @
login local
!
line vty 0 4
login
line vty 5 15


### Lab Assignments & Solutions — strona 61

login
!
End
8 Answer the following questions:
a. What is the difference between the login and login local commands?
b. Where on the device is the running-config file stored?
c. How many FastEthernet and Gigabit Ethernet interfaces does the switch have
according to the show running-config command output?
d. Are the passwords displayed in plain text? Why?
e. Where on the device is startup-config stored, and why is it important to copy
all settings to it?

A. Configured on line console 0, the login command enables only password checking.
The login local command enables both username and password checking.

B. RAM (Random Access Memory)

C. 24 FastEthernet / 2 Gigabit Ethernet

D. Yes, the service password encryption is not enabled.

E. NVRAM Memory. This is non-volatile memory, meaning the data is available after
power loss, unlike RAM. (Note that the system loads the device settings by default
from the NVRAM, upon startup.)


### Lab Assignments & Solutions — strona 62

Step 4 — Enable the password-encryption service and back up the
configuration
9 Return to Global Config mode and encrypt all passwords on the device with the
command service password-encryption.
Switch#configure terminal
10 Enter End and press Enter. Display the running-config file again, and make sure all
passwords are encrypted with the command show running-config.
S$1-Floor1(config)#end
S1-Floor1#
%SYS-5-CONFIG_I: Configured from console by console
$1-Floorl#show running-config
Building configuration...
Current configuration : 1247 bytes
!
version 12.2
no service timestamps log datetime msec
no service timestamps debug datetime msec
service password-encryption
!
hostname S1-Floor1
!
enable password 7 @822@D5D0A49
!
username Admin privilege 1 password 7 @8316C49@D39


### Lab Assignments & Solutions — strona 63

11 Save all device settings locally with the command copy running-config startup-
config.
$1-Floorl#copy running-config startup-config
Destination filename [startup-config]?
Building configuration...
[OK]
12 Display startup-config to make sure all settings were copied. To do so, make sure
that the running-config is identical to the startup-config.
$1-Floorl#show startup-config
<output omitted>
#Make sure the setting in this file is identical to the running-config
file.#
Step 5 — Configure IP addresses on the user PCs
13 Click the User1 computer, move to the desktop tab, and click the IP configuration
icon: Ee
14 Configure the following static addresses and close the window:
e@ IP: 10.0.0.1
@ Subnet mask: 255.0.0.0


### Lab Assignments & Solutions — strona 64

15 For the User2 PC, configure the IP: 10.0.0.2 with the same subnet mask address
as User1.

a E

O pice © sac

IPAddess raco2

Subnet Mask 56000

Deft Gateway e000

DNS Sener e000
16 Which command in CMD is used to display the host network settings?
17 Enter the User1 Desktop tab and click the Command Prompt icon.

|
ey el Sy Se
a
Dep


### Lab Assignments & Solutions — strona 65

18 Ping the User2 address to check connectivity.
Packet Tracer PC Command Line 1.0
ci\>ping 10.0.0.2
Pinging 10.0.0.2 with 32 bytes of data:
Reply from 10.0.0.2: bytes=32 time=Ims TTL=128
Reply from 10.0.0.2: bytes=32 time<1ms TTL=128
Reply from 10.0.0.2: bytes=32 time<Ims TTL=128
Reply from 10.0.0.2: bytes=32 time<Ims TTL=128
Ping statistics for 10.0.0.2:
Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),
Approximate round trip times in milli-seconds:
Minimum = Oms, Maximum = lms, Average = Oms
Note: A connectivity test in Packet Tracer can also be done using the Envelope tool:
a. Click the Envelope icon 4 .
b. Click the source device.
c. Click the destination device.
d. Check the status, Failed/Successful, in the status bar (marked by “<” at the
bottom right corner).
BeestOraaarr+.raacobges 2
sQec bv meee
GEER Physical ee ean ae
| 1 seléct envelope tool ‘ c
2 masewne et] (| 3.elk pe you want to
to test from wes test
=a situiaion
poe sees e Sere sssessesse 4, check success/fallure
ae by clicking here
[Be gage; ea :


### Lab Assignments & Solutions — strona 66

Step 6 — View the MAC table and interface settings of the switch
19 To view interface settings, such as duplex mode, bandwidth, and the interface
speed, use the show interface [interface name] command in privileged exec
mode. Return to the terminal in the “Admin PC” and use the command to check
the status of interface fastEthernet 0/1. The output should be similar to the
following:
S1-Floorl#show interfaces fastEthernet 9/1
FastEthernet@/1 is up, line protocol is up (connected)
Hardware is Lance, address is 00e0.8f38.b601 (bia @0e0.8f38.b601)
BW 100000 Kbit, DLY 1000 usec,
reliability 255/255, txload 1/255, rxload 1/255
Encapsulation ARPA, loopback not set
Keepalive set (10 sec)
Full-duplex, 10@Mb/s
input flow-control is off, output flow-control is off
ARP type: ARPA, ARP Timeout 04:00:00
Last input 00:00:08, output 90:00:05, output hang never
Last clearing of “show interface" counters never
Input queue: @/75/0/® (size/max/drops/flushes); Total output drops: @
Queueing strategy: fifo
Output queue :0@/40@ (size/max)
5 minute input rate @ bits/sec, @ packets/sec
5 minute output rate @ bits/sec, @ packets/sec
956 packets input, 193351 bytes, @ no buffer
Received 956 broadcasts, @ runts, @ giants, © throttles
@ input errors, @ CRC, @ frame, @ overrun, @ ignored, @ abort
@ watchdog, @ multicast, @ pause input


### Lab Assignments & Solutions — strona 67

@ input packets with dribble condition detected
2357 packets output, 263570 bytes, @ underruns
® output errors, @ collisions, 10 interface resets
®@ babbles, @ late collision, ® deferred
@ lost carrier, @ no carrier
® output buffer failures, @ output buffers swapped out
20 Display the switch’s MAC table, with the command: show mac-address-table .
S1-Floorl#show mac-address-table
Mac Address Table
Vlan Mac Address Type Ports
1 @001.c9bb.9e7b DYNAMIC Fa@/2
1 0003.e41a.b68d DYNAMIC Fa@/1
21 How do we measure the network speed of an interface or cable (the bandwidth)?
(Refer to the show interface output.)
Megabits per second, or Mbps


### Lab Assignments & Solutions — strona 68

22 Which PC physical address is associated with the fastEthernet 2 interface?
S1-Floorl#show mac-address-table
Mac Address Table
Vlan Mac Address Type Ports
il Q001.c9bb.9e7b DYNAMIC Fa@/2
1 0003.e41a.b68d DYNAMIC Fa@/1


### Lab Assignments & Solutions — strona 69

Lab Task 4: Alternative Lab Opening
In this task, you will open the PKA file in an alternative way to avoid potential errors.
1 Open Packet Tracer.
2 Inthe menu, click “File” and then click “Open...”.
IR Cisco Packet Tracer - a x)
Fie| E6t Optons View Tos Extensions Hep
tam 1° 7CQQne ise E
El Open Samples Ctrl+ShitsT
ioe meen 6 Be ee
Open Activity Sequence Root] re iC I (~~ 00:43:30}
la Save Chri+s: ———— ae
Save As Ctrl+Shit+S
Save As PAZ Ctsatez
Save As Common Ganridge
AR Print cuiep
Exit and Logout
Exit
Time: 000127( JC) CED Sinuiaton
29S OOECSESSESGGEG05 G56
Od casei) Cassis) Caso) Casts) ieee eames Cate) Cocea) eran ey Cane) aed
S628 0 9 OS wane nantes)


### Lab Assignments & Solutions — strona 70

3 Navigate to the file’s location and open it.

€© > © IRL « Matera Development > US > Modules > NETMichigan > NETO

Organize + New folder S~ m@ @
a
|
1 cA) sf
j A =
' ® von Ooo
i
i
i
i
i
|

Filename: [NET-B-L2pta | [Packet TacerFle pla". ©]


# NET-03-LS3 — Backing Up Config Files and Managing the IOS

> Zakres źródłowy: strony 71–85.


### Lab Assignments & Solutions — strona 71

Computer Networking
Lab Assignment Switch & IOS
& Solution Fundamentals
NET-03-LS3
° aT Backing Up Config Files
ia U and Managing the IOS
Copyright © 1996-2021 HackerU Ltd.
All Rights Reserved.


### Lab Assignments & Solutions — strona 72

Note: Solutions for the instructor are shown inside the green box.
©) . .
©) Lab Objective
Understand how to configure and back up Cisco devices.
bs) Lab Mission
Use a Trivial File Transfer Protocol (TFTP) server to back up and roll out switch
configurations.
C2 .
©) Lab Duration
30-60 minutes
fe Requirements
e Knowledge of basic IOS commands and navigation
e Knowledge of Cisco device components and system files
oo

| Resources
e Environment & Tools

o Cisco Packet Tracer 7.2.2 or later
e Extra Lab Files

o NET-03-L3.pka


### Lab Assignments & Solutions — strona 73

Instructions for PKA Lab Files
Lab material includes the lab document and a PKA lab file.
When you open a PKA file in Cisco Packet Tracer, two windows appear:
1. Lab topology window
2. Activity window
PKA Features
Note the following essential information regarding the Activity window:
1. Completion Percentage: Learner progress appears at the bottom right corner of the
window.
2. Check Result Button: When you click this button and then click the Assessment
Items tab, you will find a checklist with lab objectives and status, where V means done
and X means not done.
Note: Both features help the instructor grade the exercise swiftly and efficiently.
ee ne) Omak aascesis Gmatiat
Please refer to the exercise document and carefully follow the a ae -
ledisa a = ae Capa ea
See the percentage of completion atthe right-bottom corner to = Ta fi sas
determine your progress. 5) NIP Sener oO Other:
Note: The Optional and Bonus section are not sored Ses wef ,
Good tude A ‘ cite
PKA Solution
To view the solution or edit the lab file, click the wizard hat icon and enter the following
password: C!ScOM@ster.
Right-click the Answer Network tab and then click Show Answer Network.
Note: Be careful not to change anything so that the lab will remain intact.


### Lab Assignments & Solutions — strona 74

Important Note: In this lab, to avoid potential errors, do not open the associated
PKA file by double-clicking it. Instead, open the file by using the following method:
1 Open Cisco Packet Tracer.
2 Inthe window that appears, click File and then click Open...
IR Cisco Packet Tacer - a x
Fie]] Eo Optons View Tools Extensions Hep
1. ee IF 782QQ0H ESE 2
lm Open Samples Cirl+Shit+T
= » ée Sa ia ee
Open Activity Sequence Root] I iC IC ( ~ 00:43:30)
ka Save cries ———
Save As cuts shites
Sare As PKZ cisaitez
Save As Common Cartridge
prot cise
Berets
Ext
Tine: o00427( JC) (Q Reatime) Simulation]
SIRS DOGSESesSssooonses.e
\4331_) 4321) _1941 | | 2901 ) | 2911 | (61910%) ‘G19HGW \_829_/ _1240 ) (PERouss) (Prempy |_1641_ (2620
(OT
S28 0 9 Om nae tases


### Lab Assignments & Solutions — strona 75

3 Navigate to the file's location and open it.
€ > © 1 | « Materal Development > US > Modules > NETMichigan > NETO
Organize + New folder S~ @ @
a
a
a A A
. A
a
a
a
a
a
a
1
a
i


### Lab Assignments & Solutions — strona 76

Lab Task 1: Back Up Configuration Files
Note: If the lab opens with missing parts, configurations, or errors, close and repeat the
above steps to reopen the lab.
192.168.1.0/24
R1
192.168.1.1
$1
TFTP Server
192.168.1.3 192.168.1.2
Note: Run all commands on S1.
1 The preconfigured devices have logical addresses. From the TFTP server, test
connectivity to $1 and R1.
2 Click the switch $1 and navigate to the CLI tab.
beasoraeariaaaomase 2
SQexhvmeé@ mm
(A coos SNES [een ce


### Lab Assignments & Solutions — strona 77

id
Physical Config Attributes
10S Command Line Interface
TANBASE-
12.2 (25) FK, RELEASE SOFTWARE (201)
Compiled Wed 12-Oct-05 22:05 by pt_team
Press RETURU to get started!
SLINK-S-CHANGED: Interface FastEthernet0/1, chenged state to wp
SLINEPROTO-S-UPDOWN: Line protocol on Interface FastEthemet0/1,
SLINEPROTO-S-UPDOWN: Line protocol on Interface Vianl, changed
SLINEPROTO-5-UPDOWM: Line protocol on Interface
Cuil to exit CL focus Copy | | Paste
OTop
3. Onthe switch, create two user accounts:
i) Username: Admin, password: p@nd@
ii) Username: Technician, password: ku@I@
To do so, use the following commands:
S1>enable
Si#configure terminal
S1(config)#username Admin password p@nd@
S1(config)#username Technician password ku@1l@
4 Secure the console line by enabling local password checking.
To do so, use the following commands:
S1(config)#line console @
S1(config-line)#login local
S1(config-line)#exit


### Lab Assignments & Solutions — strona 78

5 Set the enable password to clscO.
To do so, use the following command:
S1(config)#enable password c!sc@
6 Encrypt all passwords on the device.
To do so, use the following command:
S1(config)#service password-encryption
7 Set an appropriate security message (banner):
Access to this device is for authorized personnel only!
To do so, use the following command:
S1(config)#banner motd #Access to this device is for authorized personnel
only!#
8 Disable DNS lookup on the device using the following command:
S1(config)#no ip domain-lookup
9 What does the command copy running-config startup-config do?
The command saves the configuration from RAM to NVRAM.
10 Save the running configuration to the startup file of the switch.
To do so, use the following commands:
Si#copy running-config startup-config
Destination filename [startup-config]?
Note: you can also use the shortcut for this command, which is $1#copy run
start.


### Lab Assignments & Solutions — strona 79

Sl#copy run
Sl#copy Sonningecorieig startup-config
Destination filename [startup-config] ?|
Building configuration...
[OK]
Sslé# v
Ctrl+F6 to exit CLI focus Copy Paste
C1 Top
11. Verify that the TFTP service is up and running on the server (TFTP server) by
clicking the server, going to the Services tab, clicking TFTP, and selecting On.
® TFTP Server - im x
Physical Config Services Desktop Programming —_ Attributes
SERVICES P
HTTP 7
DHCP Senice O of
File A
= asa842-k8.bin
SYSLOG asa923-k8.bin
AAA CARA A advinconirock@.m7 194.16 T1 hin
12 On the switch, copy the running-config file to the TFTP server and name it $1-
config-backup20.9. Use the command S1#copy running-config tftp. When
prompted, enter the IP of the TFTP server, which is 192.168.1.3. Name the file
when prompted to do so.
S1#copy running-config tftp
Address or name of remote host []? 192.168.1.3
Destination filename [S1-confg]? S1-config-backup20.9


### Lab Assignments & Solutions — strona 80

sl¢
Sl#copy running-config tftp
Address or name of remote host []? 192.168.1.3
Destination filename [Sl-confg]? Sl-config-backup20.9
Writing running-config...!!
{OK - 1364 bytes]
1364 bytes copied in 0 secs
Siz] Ms
Ctrl+F6 to exit CLI focus Copy Paste
(1 Top
13 Verify that the configuration was backed up to the TFTP server by clicking the
server, going to the Services tab, clicking TFTP, and reviewing the files.
® TFTP Server = o x
Physical Config Services Desktop Programming —_ Attributes
SERVICES THI
HTTP
DHCP Service @ on O of
DHCPv6
File “
SYSLOG asa842-k8 bin
DAA asa923-k8.bin
NTP 184 1.advineorirack9.m7 194.16 T4 hin


### Lab Assignments & Solutions — strona 81

Lab Task 2: Back Up and Upgrade the Device ISO
Note: Run all commands on S1.
Part 1: Back up the device operating system
Note: Every file can potentially become corrupted. If the operating system itself is
corrupt, the device may not even be able to boot correctly. It is therefore always a
good idea to keep current copies of OS files.
1 Show the version of the IOS on the switch using the show version command in
Privileged EXEC mode.
2 Display the contents of the flash memory and document the IOS file name with
S1#show flash.
[ Jee
CifsF6 to ext CL focus em Pasie
C1 Top
3 Use the copy command to back up the image file to the TFTP server and name it
$1-OSimage-backup.
Si#copy flash tftp
Source filename []? C2960-lanbase-mz.122-25.FX.bin
Address or name of remote host []? 192.168.1.3
Destination filename [C2960-lanbase-mz.122-25.FX.bin]? S1-OSimage-backup


### Lab Assignments & Solutions — strona 82

Slt
Sl#copy flash tftp
Source filename []? c2960-lanbase-mz.122-25.FX.bin
Address or name of remote host []? 192.168.1.3
Destination filename [c2960-lanbase-mz.122-25.FX.bin]? Sl-
OSimage-backup
Writing c2960-lanbase-mz.
122-25. FX.bin.. SPF EUEF PEPE PEP EP ESE PEP EP ESP Pee ee ee ee ee eee gees
{OK - 4414921 bytes]
4414921 bytes copied in 0.054 secs (2221364 bytes/sec)
siz] ¥
Ctrl+F6 to exit CLI focus Copy Paste
(Top
4 Access the TFTP server and verify the IOS image copy on the server.
® TFTP Server = o x
Physical Config Services Desktop Programming Attributes
SERVICES TeTP
HTTP
eS Senice @on O of
DHCPv6 -————. eww.0mmm >>]
File a
me $1-OSimage-backup
SYSLOG ‘St-config-backup20.9
Part 2: Upgrade the device IOS to a newer version
5 Locate the following image filename on the TFTP server:
c2960-lanbasek9-mz.150-2.SE4.bin.
6 Access $1 and verify that there is enough free space in flash memory for the new
10S file using the $1#show flash command.


### Lab Assignments & Solutions — strona 83

Slt
slit
Sl#show flash
Directory of flash:/
1 -rw- 4414921 <no date> c2960-lanbase-mz.
122-25.FX.bin
14° -rw- 4670455 <no date> c2960-lanbasek9-mz.
150-2.SE4.bin
130 -rw- 1364 <no date> config.text
[| c2016384 bytes total (54925644 bytes free) |
v
Ctri+F6 to exit CLI focus Copy Paste
(1 Top
7 Copy the new image file version from the TFTP server (c2960-lanbasek9-mz.150-
2.SE4.bin) using the command copy tftp flash. |n the first dialog option, insert the
IP address of the TFTP server. In the second option, insert the name of the image
file. The filename must be typed as shown to prevent transmission errors. In the
third option, press Enter.
Si#copy tftp flash
Address or name of remote host []? 192.168.1.3
Source filename []? c2960-lanbasek9-mz.15@-2.SE4.bin
Destination filename [C2960-lanbasek9-mz.150-2.SE4.bin]?
Sl#copy tftp flash
Address or name of remote host []? 192.168.1.3
Source filename []? c2960-lanbasek9-mz.150-2.SE4.bin
Destination filename [c2960-lanbasek9-mz.150-2.S5E4.bin]?
Accessing tftp://192.168.1.3/c2960-lanbasek9-mz.150-2.SE4.bin...
Loading c2960-lanbasek9-mz.150-2.SE4.bin from 192.168.1.3:
[OK - 4670455 bytes]
4670455 bytes copied in 0.062 secs (6056253 bytes/sec)
siz Mw
Ctrl+F6 to exit CLI focus Copy Paste
L Top
8 Verify that the new IOS image was copied to flash memory. To do so, use the
command $1# show flash.


### Lab Assignments & Solutions — strona 84

Sifshow flash
Directory of flash:/
Lonrw 4414922 <no dave> c2960-Lanbase-mz.
150-2.5E4.bin
= TSE oo oer
c4016384 bytes total (54929644 bytes free)
Slt ¥
Ctrl#F6 to exit CLI focus Copy Paste
(Top
9 Use the boot system in Global mode to load the new image.
Enter the command:
IS1(config)#boot system flash: /c2960-lanbasek9-mz.150-2.SE4.bin
S1 (config) #
S1 (config) #
Sl(config)#boot system flash: /c2960-lanbasek9-mz.150-2.SE4.bin
S1 (config) #| v
Ctrl+F6 to exit CLI focus Copy Paste
CO Top
10 Reload the switch. Type yes when asked to save and click OK to proceed with the
reload.
Slé#
Sl#reload
System configuration has been modified. Save? [yes/no]:yes
Building configuration...
[0K]
Proceed with reload? [confirm] M
Ctri+F6 to exit CLI focus Copy Paste
C1 Top
11 Verify that the new version was installed after reboot using the command
S1#show version.


### Lab Assignments & Solutions — strona 85

| Bs — a x Bs — o x
| Physical Cong ctl Abies Physical Cong _CLI_artibutas
| 19S Command Line Interface 10S Command Line Interface

ery n _ - x

fu 69% bytes of Tlash-simated non-volatile confaguration memory.

a Base ethernet WAC Addreos + 00417:59:A7151:20

a Motnezbserd assembly number + 73-10380-03

: Power supply part nunber + 341-0087-02
| TOTeeTeEe, C2960 Sofcware (C2960-LANERSEKS-H), Version Reet pay seael aaa

18.0(2)SE4, RELEASE SOFTWARE (£c1) evi alan: nine :

‘Technical Support: Aetp!//www.ciaco.com/techsupport Bone oor evisionmmmper = 15

" Mode number + W5-c2960-247T-L

Copyzight (c) 1986-2019 by Cisco Systema, Inc. Bee Pe vcsnenae Lea

Compiied Wes 26-dun-13 02249 by naguyen See ee erence 2 oro

ROK: Bootstrap program is C2960 boot loader eeeaeeesbLclaistensiints: cA
Uf | sorame: cate sive seer senneacemcor-ay veisia. sasaineeyre ET canae —

ETWARE Raravare Board Revision Munber + 0x02

Switch uptine is 99 minucee

Syeten returned to ROK by power-on AKU ee ih —— oe

Staten Guapo Gilg Voce oe etokpe lanbend¥S an iii 30S, SEN Switch Ports Model SITET Sw Image

+ 126 ws-cosep-zerrn | 15.0(2)988 c2960-

this product contains cryptographic feacuzes and is subject to Paes

unitea

States and local country lave governing import, export, transfer | accep Bceaste Peseccl Mer 55

CUi+F6 to exit CLI focus Copy Paste (Cul#=6 to exit CLI focus Copy Paste
Ctop Oto


# NET-04-LS1 — Configure and Verify Port Security

> Zakres źródłowy: strony 86–110.


### Lab Assignments & Solutions — strona 86

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


### Lab Assignments & Solutions — strona 87

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


### Lab Assignments & Solutions — strona 88

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


### Lab Assignments & Solutions — strona 89

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


### Lab Assignments & Solutions — strona 90

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


### Lab Assignments & Solutions — strona 91

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


### Lab Assignments & Solutions — strona 92

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


### Lab Assignments & Solutions — strona 93

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


### Lab Assignments & Solutions — strona 94

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


### Lab Assignments & Solutions — strona 95

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


### Lab Assignments & Solutions — strona 96

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


### Lab Assignments & Solutions — strona 97

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


### Lab Assignments & Solutions — strona 98

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


### Lab Assignments & Solutions — strona 99

4 Try to ping Ross’s PC from the rogue laptop.
B Rogue Laptop = a x
Physical Config Desktop Programming —_ Attributes
|
|
Rachel Ross Joey Monica


### Lab Assignments & Solutions — strona 100

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


### Lab Assignments & Solutions — strona 101

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


### Lab Assignments & Solutions — strona 102

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


### Lab Assignments & Solutions — strona 103

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


### Lab Assignments & Solutions — strona 104

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


### Lab Assignments & Solutions — strona 105

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


### Lab Assignments & Solutions — strona 106

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


### Lab Assignments & Solutions — strona 107

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


### Lab Assignments & Solutions — strona 108

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


### Lab Assignments & Solutions — strona 109

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


### Lab Assignments & Solutions — strona 110

& Mission Accomplished
® You protected endpoints by using port security to limit the number of MAC
address per port and filtered MAC addresses.
@ You now have an understanding of the different types of violation modes.
@ By not applying the proper port security, you have left one port vulnerable.


# NET-04-LS2 — Remote Access with SSH

> Zakres źródłowy: strony 111–123.


### Lab Assignments & Solutions — strona 111

Computer Networking
Lab Assignment Switch Security
& Solution
NET-04-LS2
Remote Access with SSH
Ped ibaa
fo} in
Ee
Copyright © 1996-2020 HackerU Ltd.
All Rights Reserved.


### Lab Assignments & Solutions — strona 112

Note: Solutions for the instructor are shown inside the green box.
<i _ ‘i
©) Lab Objective
Learn about the SSH protocol and how it can be used to securely and remotely access
network devices.
2 Lab Mission
Set up a switch with basic security and layer 3 connectivity, after enabling SSH
connections using RSA encryption, and test SSH by opening a session from a local PC.
esa .
©@) Lab Duration
30-60 minutes
fe Requirements
e Knowledge of basic IOS commands and navigation.
on

| Resources
e¢ Environment & Tools

o All platforms

o Cisco Packet Tracer 7.2.2 or later
e Extra Files

o Net-04-L2.pka


### Lab Assignments & Solutions — strona 113

' Fi
s ¢ | Tip
o © * | Refer back to NET-03-L2 for basic Cisco device configurations.
=
Instructions for PKA Lab Files
Lab material includes the lab document and a PKA lab file.
Open the pka file through the Cisco Packet Tracer menu by clicking "File", and then click
"Open...".
Cisco Packet acer _ pp
jaca 69 Q2QQ0R ese 2
rca oar aT)
OpenAcity Seavnce ee ns)
see ons SS a
Prot — Cle
Exton Lopet
29 E 480838 9SSS3SSC83S8¢
a ere ———*
Navigate to the file's location and open it.


### Lab Assignments & Solutions — strona 114

.

a A A

72, @

Bree rou

‘si

a

a

a

a

a

4

i

Filename [NETO2 pa | [Packet ace Fie ake pie™ |
Note: Double-clicking the pka file in file explorer may not work (depending on the
Packet Tracer version).
When you open a PKA file in Cisco Packet Tracer, two windows appear:
1. Lab topology window
2. Activity window
PKA Features
Note the following essential information regarding the Activity window:
1. Completion Percentage — Student progress appears at the right-bottom corner of
the window.
2. Check Result Button — When you click this button, and then click the "Assessment
Items" tab, you will find a checklist with lab objectives and status, whereby V-done, X-
not done.
Note: Both features help the instructor grade the exercise swiftly and efficiently.


### Lab Assignments & Solutions — strona 115

1B Pr pct oncon2 ee
Pease refer to the exercise document and carefully follow the =a a ia ee
‘See the percentage of completion at the right-bottom corner to a wi Server o Other
determine your progress. MP Sere Rowe ¢ oe
Note: The Optional and Bonus section ae not scored bet
Good Luck Lege ¢ cee
o A oe
See ran ¢ ote
Settee nema oe
a syaodeace A oe
Sir altesss ¢ ote
PKA Solution
To view the solution or edit the lab file, you can click the "Wizard hat" icon and enter
the following password: C!ScOM@ster
Right-click the "Answer network" tab, and then click "Show Answer network".
Note: Be careful not to change anything so that the lab will remain intact.


### Lab Assignments & Solutions — strona 116

Lab Task 1: Configure SSH
Set basic switch configurations, assign the switch an IPv4 address, and enable SSH to
connect to the switch with RSA encryption.
All the required commands were introduced in the presentation, and are also found in
the textbook.
10.0.0.0/24
R1
rr
Admin PC a
Part 1: Initial access and settings:
1 Using aconsole cable, connect to $1 and the terminal software.
&S
Ri
tooo
3rd
s9mgmel Ve Sas
a 2nd
rs] Ast «
E | tt __§_—__


### Lab Assignments & Solutions — strona 117

2 Set $1 as the switch's device name.
Switch>enable
Switch#configure terminal
Enter configuration commands, one per line. End with CNTL/Z.
Switch(config)#hostname S1
S1(config)#
3 Create a user account:
Username: Admin
Password: p@nd@
S1(config)#username Admin password p@nd@
4 Set the enable password to c!scO
S1(config)#enable password c!sc@
Encrypt all passwords on the device.
S1(config)#service password-encryption
5 Setan appropriate security message (Banner):
Access to this device is for authorized personnel only!
S1(config)#banner motd #Access to this device is for authorized personnel only!#
6 Set CyberPro.com as the device domain.
S1(config)#ip domain-name CyberPro.com
Part 2: Enable layer 3 connectivity on the switch
1 Enable interface VLAN1, configure it with the address 10.0.0.150 255.255.255.0
and turn on the interface using no shutdown.
S1(config)#interface vlan 1
S1(config-if)#ip address 10.0.0.15@ 255.255.255.0
S1(config-if)#no shutdown
2 Set the switch’s default gateway address to 10.0.0.1
S1(config)#ip default-gateway 10.0.0.1


### Lab Assignments & Solutions — strona 118

3 Exit the terminal window on the Admin PC, go to the command prompt, and test
connectivity to the switch using the Ping command.
C:\>ping 10.0.0.150
Pinging 10.0.0.150 with 32 bytes of data:
Reply from 10.0.0.150: bytes=32 time<lms TTL=255
Reply from 10.0.0.150: bytes=32 time<lms TTL=255
Reply from 10.0.0.150: bytes=32 time<lms TTL=255
Reply from 10.0.0.150: bytes=32 time<lms TTL=255
Ping statistics for 10.0.0.150:
Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),
Approximate round trip times in milli-seconds:
Minimum = Oms, Maximum = Oms, Average = Oms
Part 3: Permit remote access to the device
1. Go back to the terminal on the Admin PC and enter the line vty mode (channels
Oto 15).
S1(config)#line vty @ 15
S1(config-line)#
2 Configure line vty for local password checking, using the command login local.
S1(config-line)# login local
3 Set the line to display the banner when accessing the switch remotely, using the
command motd-banner.
S1(config-line)# motd-banner
4 Allow only SSH connection requests to the switch.
Sl{config-line)¢transport input ssh
S1(config-line) fexit
Sl (config) #| Lg
C1 top


### Lab Assignments & Solutions — strona 119

S1(config-line)# transport input ssh
S1(config-line)# exit
5 RSA uses two types of keys, name them and their functions.
Public Key — Encrypts data, Private key - Decrypts secure data
Part 4: Configure SSH
1 Generate the RSA keys for the SSH process, with a key length of 1024 bits, via
the switch privileged exec mode.
S1(config)#crypto key generate rsa
$1 (config) #
Sl(config)#crypto key generate rsa
The name for the keys will be: 51.Cyberpro.com
Choose the size of the key modulus in the range of 360 to 2048
for your
General Purpose Keys. Choosing a key modulus greater than 512
may take
a few minutes.
How many bits in the modulus [512]: 1024
% Generating 1024 bit RSA keys, keys will be non-exportable...
Sl (contig) # be
1 Top
2 Set the SSH version to 2, using the command ip ssh version 2.
S1(config)#ip ssh version 2
S1(config)#exit
3. What is the maximum key length in RSA?
2048


### Lab Assignments & Solutions — strona 120

Lab Task 2: Verify SSH Configuration
Practice troubleshooting commands and techniques for SSH.
Part 5: Verify settings in S1
1 Make sure all settings are correct, using the following Show commands:
a. Show ip ssh (via the privileged exec mode)
bell


### Lab Assignments & Solutions — strona 121

b. Show running-config
Sl#show running-config
Building configuration...
Current configuration : 1370 bytes
q
version 12.2
no service timestamps log datetime msec
no service timestamps debug datetime msec
service password-encryption
,
hostname 51
!
enable password 7 08220D5D0A49
1
:
ip domain-name Cyberpro.com
|.
username Admin privilege 1 password 7 08316C400D39
!
1
1
spanning-tree mode pvst
spanning-tree extend system-id
x
--More-—
interface Vlanl
ap address 10.0.0.150 255.255.255.090
!
ip default-gateway 10.0.0.1
banner motd “CAccess to this device is for authorized personnel
only!*C
!
:
!
line con 0
1
line vty 0 4
login local
transport input ssh
ine vty 5 15
login local
transport input ssh


### Lab Assignments & Solutions — strona 122

2 > Which IOS show command displays active SSH connections on the device?
Part 6: Establish an SSH session
1 Close the terminal window, disconnect the console cable, and open the
command prompt window.
<R Admin PC - ao x
Physical Conig Desktop Progamming Attibutes
e = a
O tp
roonas =


### Lab Assignments & Solutions — strona 123

2 Connect to the switch using SSH, as follows:
ssh -] <username><target-ip>

C:\>ssh -1 Admin 10.0.0.150
Password:
Access to this device is for authorized personnel only!
S1>enable
Password:
S1#

3 InS1, start a second SSH session to R1.

Note: R1 is preconfigured with all the necessary settings. Login credentials are
the same as for S1.

C:\>ssh -1 Admin 10.0.0.1
Password:
Access to this device is for authorized personnel only!
R1>enable
Password:
R1l#

4 Which TCP port protocols do SSH and Telnet use?

Telnet: 23, SSH: 22
5 Which encryption method and type does SSH use?
RSA, Asymmetric Encryption


# NET-05-LS1 — Converting Decimal, Binary, and Hex

> Zakres źródłowy: strony 124–130.


### Lab Assignments & Solutions — strona 124

Computer Networking
Lab Assignment IP & Routing
& Solution Concepts
°. an NET-05-LS1
al U Converting Decimal,
Binary, and Hex
Copyright © 1996-2020 HackerU Ltd.
All Rights Reserved.


### Lab Assignments & Solutions — strona 125

Note: Solutions for the instructor are shown inside the green box.
@ Lab Objective
Understand the difference between binary, decimal, and hexadecimal number systems
and how to convert values among them.
4 Lab Mission
Use practice questions to evaluate and convert values among the numbering systems.
esa 7
©) Lab Duration
30-45 minutes
fe Requirements
e@ Basic understanding of the decimal (base 10) numbering system.
e Basic understanding of the hexadecimal (base 16) numbering system.
e@ Basic understanding of the binary (base 2) numbering system.
oo
| Resources
e Environment & Tools
o Optional: Calculator


### Lab Assignments & Solutions — strona 126

Lab Task 1: Decimal and Binary
Understand how decimal numbering relates to binary.
Part 1: Convert Decimal to Binary
1. Which mathematical base does the binary system use, and which digits represent
it?
Base 2, two digits: 0 and 1
2 Whatisa bit?
A bit (binary digit) is the smallest unit of data in a computer. A bit has a single binary
value, either 0 or 1.
3. Whatis an octet?
8-bit string (IPv4 consists of four octets).
4 Convert the following decimal digits to a binary octet.
Pe joys ts fe fe fe fe
aE
Example: 56 in binary octet:
a) 26
b) 65
c) 91
d) 151
e) 168
f) 192
g) 254
26 = 00011010


### Lab Assignments & Solutions — strona 127

65 = 01000001
91 = 01011011
151 = 10010111
168 = 10101000
192 = 11000000
254 = 11111110
Part 2: Convert Binary to Decimal
5 Convert the following IPv4 binary octets to decimal digits:
Example: 00000010 in decimal is 2.
a) 00000111
b) 00010010
c) 00101110
d) 01011111
e) 10010010
f) 11011110
g) 11111111
a. 7
b. 18
c. 46
d. 95
e. 146
£222
g. 255
6 Bonus: Convert the following IPv4 addresses to their binary equivalents:
Example: 10.0.0.5 is actually a long 32-bit string.
[oe inary
10.0.0.5 | 00001010.00000000.00000000.00000101


### Lab Assignments & Solutions — strona 128

a) 172.16.10.2
b) 192.168.1.1
c) 8.8.8.8
a. 172.16.10.2 = 10101100.00010000.00001010.00000010
b. 192.168.1.1 = 11000000.10101000.0000001.0000001
c. 8.8.8.8 = 00001000.00001000.00001000.00001000


### Lab Assignments & Solutions — strona 129

Lab Task 2: Binary and Hexadecimal
Understand how binary relates to hexadecimal numbering.
Part 1: Convert Binary to Hex
1 Which mathematical base does the hexadecimal system use, and which digits
represent it?
Base 16, 10 digits and 6 characters: 0-9, A, B, C, D, E, F
2 Convert the following binary nibbles (half-bytes) to hex digits:
Example: 1010 is A
a) 0010
b) 1101
c) 0110
d) 1100
e) 1000
f) 1011
g) 0000
h) 1110
i) 1111
a. 2
b. D
c. 6
dc
e. 8
f. B
g. O
h. E
i. F


### Lab Assignments & Solutions — strona 130

Part 2: Convert Hex to Binary
3 The following is a random physical address of 12 decimal digits (MAC).
Convert the hexadecimal digits to binary digits:
Example: 00-B1-17-C2-A2-EE is represented in binary as follows:
Px a
|B [af] [2/o/e fol
7 [ofoe tafe] fala
| [2[{o[ofo]e|ato
[#2 [2/0] [o//e/alo
eer
a) B3-00-13-A1-02-3E
[Hex| Binary
[83 [1] o[1{1folofa) 4)
[00 [oj ofofofolafojo|
|.13 [ol ofo[1]olo} 1) 4/
[az [1/0/21 [olololo|.|
[02 [o|ofofofololso|
L3e [ofofa|1]1]2[1]o]
b) 04-01-0A-DD-CC-FF
[Hex[ Binary |
[04 [ol ofofofol1fofo|
[01 [ol ofofofolofojs|
[oa [ol ofofolslofajo|
[po [1/10] 11/10] 4]
[cc [1] 1{ofo]1[1]o/o|


# NET-05-LS2 — IPv4 and Initial Router Configuration

> Zakres źródłowy: strony 131–147.


### Lab Assignments & Solutions — strona 131

Computer Networking
Lab Assignment IP & Routing
& Solution Concepts
RO isis, NET-O5-LS2
olF IPv4 and Initial Router
i U Configuration
Copyright © 1996-2021 HackerU Ltd.
All Rights Reserved.


### Lab Assignments & Solutions — strona 132

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


### Lab Assignments & Solutions — strona 133

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


### Lab Assignments & Solutions — strona 134

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


### Lab Assignments & Solutions — strona 135

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


### Lab Assignments & Solutions — strona 136

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


### Lab Assignments & Solutions — strona 137

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


### Lab Assignments & Solutions — strona 138

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


### Lab Assignments & Solutions — strona 139

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


### Lab Assignments & Solutions — strona 140

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


### Lab Assignments & Solutions — strona 141

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


### Lab Assignments & Solutions — strona 142

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


### Lab Assignments & Solutions — strona 143

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


### Lab Assignments & Solutions — strona 144

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


### Lab Assignments & Solutions — strona 145

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


### Lab Assignments & Solutions — strona 146

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


### Lab Assignments & Solutions — strona 147

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


# NET-05-LS3 — Configure IPv6 Addressing

> Zakres źródłowy: strony 148–160.


### Lab Assignments & Solutions — strona 148

Computer Networking
Lab Assignment IP & Routing
& Solution Concepts
RO isis, NET-05-LS3
ol Configure IPv6 Addressing
Es}
Copyright © 1996-2020 HackerU Ltd.
All Rights Reserved.


### Lab Assignments & Solutions — strona 149

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


### Lab Assignments & Solutions — strona 150

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


### Lab Assignments & Solutions — strona 151

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


### Lab Assignments & Solutions — strona 152

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


### Lab Assignments & Solutions — strona 153

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


### Lab Assignments & Solutions — strona 154

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


### Lab Assignments & Solutions — strona 155

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


### Lab Assignments & Solutions — strona 156

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


### Lab Assignments & Solutions — strona 157

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


### Lab Assignments & Solutions — strona 158

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


### Lab Assignments & Solutions — strona 159

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


### Lab Assignments & Solutions — strona 160

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


# NET-06-LS1 — Subnetting Practice

> Zakres źródłowy: strony 161–168.


### Lab Assignments & Solutions — strona 161

Computer Networking
Lab Assignment Subnetting
& Solution Concepts
ocnae NET-06-LS1
ol Subnetting Practice

EI
Copyright © 1996-2021 HackerU Ltd.
All Rights Reserved.


### Lab Assignments & Solutions — strona 162

Note: Solutions for the instructor are shown in the green box.
G Lab Objective
Apply what you learned about subnetting by answering the review questions below
relating to the material covered in the module. The topics include how to subnet
networks and how to assign IP addresses.

fy Lab Mission
Answer all review questions.
ea .
©) Lab Duration
30-60 minutes
fe Requirements
e Knowledge of subnetting concepts
e Knowledge of the binary and decimal number systems

LT
[ra] Resources
¢ Calculator (optional)


### Lab Assignments & Solutions — strona 163

Lab Task 1: CIDR & VLSM
Answer practice questions covering variable length subnet masks and classless inter-
domain routing.
1. What is the subnet mask of prefix /28?
11111111.11111111.11111111.11110000, 128+64+32+16 = 240
2 Whatare the three prefixes of classful addresses represented as an
IP address suffix?
3 How many usable IP addresses are there if the subnet mask is
255.255.255.128?
4 What is the main purpose of subnetting?


### Lab Assignments & Solutions — strona 164

Lab Task 2: Practice Questions for Subnetting
Answer practice questions covering subnetting.
1 You were asked to subnet the network address 192.168.1.0/24 so that each sub-
network includes 45 hosts. How should this be done?
a) 255.255.255.128
b) 255.255.224.0
c) 255.255.255.192
d) 255.255.255.224
2 How many assignable host addresses are there in a network with the address
172.16.0.0 and subnet mask 255.255.252.0?
a) 510
b) 1022
c) 254
d) 1024

3 True or false: There are eight sub-network addresses if the given network is
192.168.10.0 with subnet mask 255.255.255.224.

4 Network administrators require you to create an addressing scheme for a new
division in the company. The requirements include a minimum of three network
addresses and at least 35 users per network. The given IP address is 10.0.0.0 and
the subnet mask is 255.255.255.0.

a) What prefix should be used?
b) What subnet mask should be used?
c) Fill in the following table with the new addressing scheme:


### Lab Assignments & Solutions — strona 165

Network Address Usable Address
Network Address Usable Address
10.0.0.0 10.0.0.1—10.0.0.62 10.0.0.63

10.0.0.64 10.0.0.65—10.0.0.126 10.0.0.127
10.0.0.128 10.0.0.129—10.0.0.190 10.0.0.191
10.0.0.192 10.0.0.193—10.0.0.254 10.0.0.255

a) Prefix: /26

b) Subnet mask: 255.255.255.192

5 What is the correct prefix for the address 10.0.0.0 and subnet mask

255.255.255.240?

a) 10.0.0.0/25
b) 10.0.0.0/30
c) 10.0.0.0/27
d) 10.0.0.0/28

6 What is the network address for a host with IP address 192.168.23.61/28?
a) 192.168.23.0
b) 192.168.23.48
c) 192.168.23.32
d) 192.168.23.60


### Lab Assignments & Solutions — strona 166

7 Which IP addresses are valid for hosts belonging to the 10.1.16.0/20 subnet?
(Choose three answers.)
a) 10.1.15.255
b) 10.1.16.7
c) 10.1.80.150
d) 10.1.16.250
e) 10.1.32.50
f) 10.1.30.10
8 Anadmin is working with network 192.168.4.0, which has been subnetted with a
/26 prefix. Which addresses can be assigned for a host on the same subnet?
(Choose two answers.)
a) 192.168.4.67
b) 192.168.4.128
c) 192.168.4.15
d) 192.138.4.132
e) 192.168.4.61
f) 192.168.4.125
9 Anadministrator needs to configure a point-to-point connection. To do so, he
needs to divide the address 172.16.0.0/24 into 64 subnets, each having four
addresses.
a) What prefix should be used?
b) What subnet mask should be used?
c) Fill in the following table with the new addressing scheme (fill in only
the first three rows):
a
|
a


### Lab Assignments & Solutions — strona 167

a) /30
b) 255.255.255.252
Network Address Usable Address
172.16.0.0 172.16.0.1-172.16.0.2 172.16.0.3
172.16.0.4 172.16.0.5-172.16.0.6 172.16.0.7
172.16.0.8 172.16.0.9-172.16.0.10 172.16.0.11
10 A network administrator was asked to divide the address 192.168.10.0/24 into
eight subnets.
a) What prefix should be used?
b) What subnet mask should be used?
c) Fill in the following table with the new addressing scheme (fill in only
the first four rows):
Network Address Usable Address
a) /27
b) 255.255.255.224
Network Address Usable Address
192.168.10.0 192.168.10.1—192.168.10.30 192.168.10.31
192.168.10.32 192.168.10.33-192.168.10.62 192.168.10.63
192.168.10.64 192.168.10.65—-192.168.10.94 192.168.10.95
192.168.10.96 192.168.10.97—192.168.10.126 192.168.10.127


### Lab Assignments & Solutions — strona 168

11. Network administrators require you to create an addressing scheme for a new
division in the company. The requirements include a maximum number of
networks, with each network having at least 500 users. The given IP address is
80.0.0.0/16.

a) What prefix should be used?
b) What subnet mask should be used?
c) Fill in the following table with the new addressing scheme (fill in only
the first four rows):
Network Address Usable Address
a) /23
b) 255.255.254.0
Network Address Usable Address
80.0.0.0 80.0.0.1-80.0.1.254 80.0.1.255
80.0.2.0 80.0.2.1-80.0.3.254 80.0.3.255
80.0.4.0 80.0.4.1—80.0.5.254 80.0.5.255
80.0.6.0 80.0.6.1-80.0.7.254 80.0.7.255


# NET-07-LS1 — Configuring IPv4 Static and Default Routes

> Zakres źródłowy: strony 169–186.


### Lab Assignments & Solutions — strona 169

Computer Networking
Lab Assignment IPv4 & IPv6 Static
& Solution Routing
RO isis, NET-O7-LS1
olf Configuring IPv4 Static
re U and Default Routes
Copyright © 1996-2020 HackerU Ltd.
All Rights Reserved.


### Lab Assignments & Solutions — strona 170

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


### Lab Assignments & Solutions — strona 171

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


### Lab Assignments & Solutions — strona 172

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


### Lab Assignments & Solutions — strona 173

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


### Lab Assignments & Solutions — strona 174

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


### Lab Assignments & Solutions — strona 175

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


### Lab Assignments & Solutions — strona 176

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


### Lab Assignments & Solutions — strona 177

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


### Lab Assignments & Solutions — strona 178

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


### Lab Assignments & Solutions — strona 179

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


### Lab Assignments & Solutions — strona 180

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


### Lab Assignments & Solutions — strona 181

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


### Lab Assignments & Solutions — strona 182

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


### Lab Assignments & Solutions — strona 183

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


### Lab Assignments & Solutions — strona 184

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


### Lab Assignments & Solutions — strona 185

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


### Lab Assignments & Solutions — strona 186

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


# NET-08-LS1 — Configuring and Verifying RIPv2

> Zakres źródłowy: strony 187–202.


### Lab Assignments & Solutions — strona 187

Computer Networking
Lab Assignment Dynamic Routing
& Solution
NET-08-LS1
i Configuring and
oe ni Verifying RIPv2
EI
Copyright © 1996-2020 HackerU Ltd.
All Rights Reserved.


### Lab Assignments & Solutions — strona 188

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


### Lab Assignments & Solutions — strona 189

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


### Lab Assignments & Solutions — strona 190

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


### Lab Assignments & Solutions — strona 191

Lab Task 1: Revision Questions
Refresh your knowledge of routing protocols and RIP.
1. What is the default Administrative Distance value of RIP?
AD=120
2 What route source letter represents an RIP route in the routing table?
3. Whatare the default Hello and Hold intervals of RIP?
Hello is 30 seconds, Hold is 180 seconds
4 From which version of RIP VLSM is authentication supported?


### Lab Assignments & Solutions — strona 192

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


### Lab Assignments & Solutions — strona 193

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


### Lab Assignments & Solutions — strona 194

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


### Lab Assignments & Solutions — strona 195

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


### Lab Assignments & Solutions — strona 196

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


### Lab Assignments & Solutions — strona 197

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


### Lab Assignments & Solutions — strona 198

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


### Lab Assignments & Solutions — strona 199

Part 3: Test connectivity
7 From PC1, ping all other PCs. All pings should be successful.
Request timed out.
Reply from 192.168.20.2: bytes=32 time=1?ms TYL=125
Minimum = 2ms, Maximum = 17ms, Average = 7ms
Reply from 192.168.30.3: bytes=32 time=Ims TTL=126
JApproximate round trip times in milli-seconds:
Minimum = Ims, Maximum = lms, Average = Ims


### Lab Assignments & Solutions — strona 200

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


### Lab Assignments & Solutions — strona 201

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


### Lab Assignments & Solutions — strona 202

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


# NET-08-LS2 — Configuring & Verifying OSPFv2

> Zakres źródłowy: strony 203–210.


### Lab Assignments & Solutions — strona 203

Computer Networking
Lab Assignment Dynamic Routing
& Solution
NET-08-LS2
i Configuring &
oe ni Verifying OSPFv2
EI
Copyright © 1996-2020 HackerU Ltd.
All Rights Reserved.


### Lab Assignments & Solutions — strona 204

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


### Lab Assignments & Solutions — strona 205

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


### Lab Assignments & Solutions — strona 206

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


### Lab Assignments & Solutions — strona 207

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


### Lab Assignments & Solutions — strona 208

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


### Lab Assignments & Solutions — strona 209

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


### Lab Assignments & Solutions — strona 210

R2¢show ip route ospf
172.16.0_0/16 is wariably subnetted, 5 subnets, 2 masks
o 172.16.0.8 [110/2] wia 172.1€.0.€, 00:01:23, GigabitEthernet0/1/0
(1106/2) wia 172.16.0.1, 00:01:23, GigabitEthernet0/0/0
°o 192.168.0.0 [110/2] wia 172.16.0.1, 00:01:23, GigabitEthernet0/0/0
°° 192.1€6.1.0 [110/2] wia 172.16.0.€, 00:01:33, GigabitEthernet0/1/0
R2¢| w


# NET-09-LS1 — Configuring VLANs, Trunks, and More

> Zakres źródłowy: strony 211–231.


### Lab Assignments & Solutions — strona 211

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


### Lab Assignments & Solutions — strona 212

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


### Lab Assignments & Solutions — strona 213

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


### Lab Assignments & Solutions — strona 214

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


### Lab Assignments & Solutions — strona 215

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


### Lab Assignments & Solutions — strona 216

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


### Lab Assignments & Solutions — strona 217

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


### Lab Assignments & Solutions — strona 218

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


### Lab Assignments & Solutions — strona 219

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


### Lab Assignments & Solutions — strona 220

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


### Lab Assignments & Solutions — strona 221

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


### Lab Assignments & Solutions — strona 222

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


### Lab Assignments & Solutions — strona 223

12 Test connectivity between PC1 and PC6. The ping should fail.
RB eci - a x
Physical Config Desktop Programming Attributes


### Lab Assignments & Solutions — strona 224

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


### Lab Assignments & Solutions — strona 225

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


### Lab Assignments & Solutions — strona 226

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


### Lab Assignments & Solutions — strona 227

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


### Lab Assignments & Solutions — strona 228

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


### Lab Assignments & Solutions — strona 229

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


### Lab Assignments & Solutions — strona 230

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


### Lab Assignments & Solutions — strona 231

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


# NET-10-LS1 — Configure NTP and Syslog

> Zakres źródłowy: strony 232–245.


### Lab Assignments & Solutions — strona 232

Computer Networking
Lab Assignment Diagnostics &
& Solution Troubleshooting
sohRe NET-10-LS1
ol Configure NTP and Syslog
El


### Lab Assignments & Solutions — strona 233

Note: Solutions for the instructor are shown inside the green box.
@ Lab Objective
Understand what syslog services are used for and how syslog works in tandem with NTP
services.
* Lab Mission
Configure a syslog server and an NTP server to log events across the network.
Then, configure a router to send system logs to the syslog server.
rx) .
@ Lab Duration
30-50 minutes
fe Requirements
e Knowledge of basic Cisco IOS commands and navigation
Lt
[ra] Resources
e Tools
o Cisco Packet Tracer 7.2.2 or higher
e Extra Files
o NET-10-L1.pka


### Lab Assignments & Solutions — strona 234

Instructions for PKA Lab Files
Lab material includes the lab document and a PKA lab file.
Open the PKA file through the Cisco Packet Tracer menu by clicking File and then
Open....
Bet 2 2QQOR Eee 2
Orcs aay aT)
a see on ee
WB Poot Cte
29 4 OORBSSSSCSSSeSeeg
S28 0 fe Ep mama menmEs
Navigate to the file's location and open it.
a
a t) %
5
8
a
a
a
a
4
4
1


### Lab Assignments & Solutions — strona 235

Note: Double-clicking on the PKA file in your file explorer may not work (depending on

the Packet Tracer version).

Lab material includes the lab document and a PKA lab file.

When you open a PKA file in Cisco Packet Tracer, two windows appear:

1. Lab topology window

2. Activity window

PKA Features

Note the following essential information regarding the Activity window:

¢ Completion Percentage: Learner progress appears at the bottom right corner of the
window.

e Check Result Button: When you click this button and then click the Assessment
Items tab, you will find a checklist with lab objectives and status, where V = done
and X = not done.

Note: Both features help the instructor grade the exercise swiftly and efficiently.

instructions. a

See the percentage of completion a the rght- bottom commer to ST et 2 ter
determine your progres aS 3 oe
Note:The Optional and Bonus section are not scored oe Se —_ : :
Good Luck a ; “a

PKA Solution

To view the solution or edit the lab file, you can simply click the Wizard hat icon and

enter the following password: C!ScOM@ster

Right-click the Answer network tab and then click Show Answer network.

Note: Be careful not to change anything so that the lab will remain intact.


### Lab Assignments & Solutions — strona 236

Lab Task 1: Revision Questions
Answer the following questions to review event logging and NTP.
1 Explain what a syslog server is.
Syslog is a message logging server that collects and stores all the syslog messages that
are sent to it.
2 What is the default location of device log files?
The device RAM
3 How many severity levels are there?
There are eight severity levels:
Trap Level: Severity:
0 Emergency
1 Alert
2, Critical
3 Error
4 Warning
5 Notification
6 Informational
7 Debugging
4 Explain what an NTP server is.
NTP stands for Network Time Protocol and is used for clock synchronization among
network devices and computers. The server provides the time for other devices.


### Lab Assignments & Solutions — strona 237

Lab Task 2: Configure Syslog
Configure a server with the syslog service to obtain network event logs.
Part 1: Enable logging to the server on R1
1 Save the current running configuration into NRAM.
Command: copy running-config startup-config
Learners need to do this to have the startup configuration match the base
running configuration file. Do not skip this step!
2 Goto the syslog server Services tab and make sure the SYSLOG service is
enabled.
{ Ld S 1st
Physical Config Cee] omrey Programming Attributes
SERVICES
Syslog
HTTP d
Te Syslog FI]
DHCP V6 Service O of
TFTP Time HostName Message
DNS
i, Se |
1 DAA
3. What is a logging buffer?
It is a predetermined storage size allocated on RAM for syslog messages.


### Lab Assignments & Solutions — strona 238

4 From R1, ping the syslog server to verify connectivity.
R1> ping 192.168.0.10
ra veiling 192.168.0.10
Type escape sequence to abort.
Sending 5, 100-byte ICMP Echos to 192.168.0.10, timeout is 2
seconds:
Success rate is 100 percent (5/5), round-trip min/avg/max = 0/0/1
pas v
5 Configure R1 to send events and logs to the syslog server.
R1> enable
R1#configure terminal
R1(config)#logging host 192.168.0.10
6 Permit the logging of security severity level 7 (debugging) and exit global mode.
R1(config)#logging trap debugging
R1(config)#exit
Rl(config) #logging trap debugging
Rl (config) #exit
Rl¢#
%5YS-5-CONFIG_I: Configured from console by console
%SYS-6-LOGGINGHOST_STARTSTOP: Logging to host 192.168.0.10 port
514 started - CLI initiated
R1# fot


### Lab Assignments & Solutions — strona 239

7 Enable debugging for the ICMP protocol and ping PC1.
R1#debug ip icmp
R1#ping 172.16.0.2
a a
TCMP packet debugging is on
Rl¢
Type escape sequence to abort.
Sending 5, 100-byte ICMP Echos to 172.16.0.2, timeout is 2
seconds:
ICMP: echo reply rcvd, src 172.16.0.2, dst 172.16.0.1
ICMP: echo reply rcvd, src 172.16.0.2, dst 172.16.0.1
ICMP: echo reply revd, src 172.16.0.2, dst 172.16.0.1
ICMP: echo reply revd, src 172.16.0.2, dst 172.16.0.1
Success rate is 100 percent (5/5), round-trip min/avg/max = 0/0/0
ms
Rlt
ICMP: echo reply revd, src 172.16.0.2, dst 172.16.0.1
v


### Lab Assignments & Solutions — strona 240

Part 2: Verify Syslog settings
8 Use the show running-config command on R1 to verify the settings.
R1#show running-config
: a
interface GigabitEthernet0/1
ip address 172.16.0.1 255.255.0.0
duplex auto
speed auto
interface Vlanl
no ip address
shutdown
ip classless
ip flow-export version $
logging trap debugging
logging 192.168.0.10
line con 0
v
9 Goto the syslog server again, and, in the Services tab, click SYSLOG and verify
log operation.
Note: The logs currently do not include a timestamp because NTP is still not set
up.
® syslog server - ia x
Physical Config Services Desktop Programming —_ Attributes
SERVICES
Syslog
Linke Syslo.
DHCP aaa
DHCPv6é Senice @ On O of
TFTP Time HostNiame Message a|
DNS
[__systoc | 1 pont ICMP: echo reply
BAA
ae al bicabimt ICMP: echo reply
EMAIL 3 |= 192.168.0.1 ICMP: echo reply
FIP
IoT ill ddr ICMP- echo repl


### Lab Assignments & Solutions — strona 241

Lab Task 3: Configure NTP
Configure the NTP server to work with the syslog server and provide unified
timestamps across the network.
Part 1: Enable NTP on R1
1 Goto the NTP server Services tab and make sure that the NTP service is enabled.
® NTP Server ist - Oo x
Physical Config Desktop Programming Attributes,
SERVICES NTP
HTTP 3rd
DHCPv6 Authentication
TFTP © Enable @ Disable
DNS
aie aha Key Password
2 > What can operate as an NTP server?
Any device that offers the feature can operate as an NTP server: switches, routers,
servers, and others.


### Lab Assignments & Solutions — strona 242

3. Make sure the correct date and time are set on the server. Adjust them if
necessary.
® NTP Server = Oo x
Physical Config _ Services Desktop Programming Attributes
SERVICES NTP
HTTP
ae Service @© On O of
nae Authentication
TFTP O Enable @ Disable
oe Key Password
SYSLOG
Be € April, 2020 P| 11-32:52am 5]
EMAIL Sun Mon Tue Wed Thu Fri
FTP a
2 | 3 | 31 | 1 | 2] 3
ToT
VM Management 5 6 7 8 9 10
Radius EAP
wz | 13 | 4 | 15 | 16 | 47
19 20 210 22 | 8h
2% 7 2 8 8 t
3|/4]s5s]6]7]8
D Top


### Lab Assignments & Solutions — strona 243

4 From R1, ping the NTP server to verify connectivity.
R1#configure terminal
R1(config)#do ping 192.168.0.20
Rléconf t
Enter configuration commands, one per line. End with CNTL/Z.
Rl (config)#do ping 192.168.0.20
Type escape sequence to abort.
Sending 5, 100-byte ICMP Echos to 192.168.0.20, timeout is 2
seconds:
ome: echo reply revd, src 192.168.0.20, dst 192.168.0.1
ICMP: echo reply revd, src 192.168.0.20, dst 192.168.0.1
ICMP: echo reply rcvd, src 192.168.0.20, dst 192.168.0.1
Success rate is 80 percent (4/5), round-trip min/avg/max = 0/0/1
ms
Rl (config) #
ICMP: echo reply revd, src 192.168.0.20, dst 192.168.0.1
v
5 Configure R1 to get the time and date from the server dynamically.
R1(config)#ntp server 192.168.0.20
R1(config)#exit


### Lab Assignments & Solutions — strona 244

Part 2: Verify NTP settings
6 Display the R1 clock to verify time settings.
Important: If the clock was not changed, click Fast forward at the bottom left
corner several times and check again.
R1#show clock
- :
BmeBOrcaRArVAQRQOA ESS 2?
MQek Bree mn
[A Logical] Physical)x 891,359 Root] aD) i( a i im \( a (00:15:09)
me 192.166 0.0724
Geo Gigolo
an
_ ag Fa02 Fa0
| ven —
S1
NTP Server
4 a,
Fao
Fa
Pet Sysloa sever
192.168.0.10
Timo: 00:01:14 ©) i( > ) (Q Reaitime) Simulation
BIS DT OGESSsesaaacausce
i net Case ant [ant ite sir Cas) Cs) bro omy Las =)
Rl#show clock
16:15:43.724 UTC Mon Mar 30 2020
Riz »


### Lab Assignments & Solutions — strona 245

7 Enable the log timestamp services with milliseconds.
R1#configure terminal
R1(config)#service timestamps log datetime msec
R1(config)#exit
8 From R1, ping the NTP server to generate new log messages.
Ri#ping 192.168.0.20
Note: The time and date should be next to the log massage:
Rl#ping 192.168.0.20
Type escape sequence to abort.
Sending 5, 100-byte ICMP Echos to 192.168.0.20, timeout is 2 seconds:
*Mar 30, 16:25:18.2525: ICMP: echo reply rcvd, src 192.168.0.20, dst 192.168.0.1!
*Mar 30, 16:25:18.2525: ICMP: echo reply rcevd, src 192.168.0.20, dst 192.168.0.1!
*Mar 30, 16:25:18.2525: ICMP: echo reply rcvd, src 192.168.0.20, dst 192.168.0.1!
*Mar 30, 16:25:18.2525: ICMP: echo reply rcvd, src 192.168.0.20, dst 192.168.0.1!
Success rate is 100 percent (5/5), round-trip min/avg/max = 0/0/0 ms
Rl#
*Mar 30, 16:25:18.2525: ICMP: echo reply rcvd, src 192.168.0.20, dst 192.168.0.1
Rid ¥
9 Goto the syslog server, review the logs, and make sure the logs have the correct
time and date.
B® sysiog server - a cd
Physical Confg _Senices_ Desktop Progiomming Atribtes
SERVICES
sysieg
HTTP :
syslog
DHCP
Eee Senice @on Oot
Balad Time HosiName Message an
DNs
aa 1 09.30.2020 04.26 46.788 Pu fis2 1600.1 a
ae 2 ca3e 2020 04-2646 606 Puce e804 a
ema 3. 230.2020 0426.46 573 Pw f192 168.04 lspcccrsrnmranen
ww 4 03:30.2020 04:2646.404 Paige 19.0.1 baeesermmsre
ve vecooeert 5 03.30.2020 0426 6.364 palpi 168.01 leesenaranaere
6 03.30.2020 0425-16910 euifi 168.01 leeemeopmeaee
7 0330.2020 0425.16.02 Pw ft 168.01 eaasecweesaesatse
6 03.30.2020 0425-1700 paifigo 168.01 ena.
Gearlog


# NET-11-LS1 — Implement Standard and Extended ACLs

> Zakres źródłowy: strony 246–266.


### Lab Assignments & Solutions — strona 246

Computer Networking
Lab Assignment Access Control Lists
& Solution
NET-11-LS1
rr Implement Standard
o [ire and Extended ACLs
Oln
EI
Copyright © 1996-2020 HackerU Ltd.
All Rights Reserved.


### Lab Assignments & Solutions — strona 247

Note: Solutions for the instructor are shown inside the green box.
G Lab Objective
Practice setting up ACLs, and compare Named and Numbered ACLs, and Standard and
Extended ACLs.
bs Lab Mission
Learn the different ways to configure ACLs to secure parts of a network from
unauthorized users or machines, and which ACLs are best suited for specific use
cases.
ea 7
©) Lab Duration
60-100 minutes
fe Requirements
e Basic knowledge of IOS commands and navigation.
e Basic knowledge of wildcard address calculation.
e Basic knowledge of the standard and extended ACL concepts, and how they operate.
oo
| Resources
© Tools
Cisco Packet Tracer 7.2.2, or higher
e Extra Files
NET-11-L1.pka


### Lab Assignments & Solutions — strona 248

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


### Lab Assignments & Solutions — strona 249

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
Items" tab, you will get a checklist with lab objectives and status, whereby V=done,
X=not done.
Note: Both features help the instructor grade the exercise swiftly and efficiently.
Cera Feedback _ Assessor: tons Comecthy Tet
Eapaaapse al [Shon nce Re
BR PT Activity 000012 - oOo x ‘Assessment tems Stas Points Components) | Feedback
Please fer to the exerise document and carefully low the SNe he
determine your progress, eR
Note The Optonal and Bonus scion are not sored a 0 other
Good Luck! ‘KK Semce timestamp log Incorrect 1 Other
= 3 Omer
Fre Sane oman } ote
eee comet ‘ one
> syetod viet H one
Altess———ncoect ' one,
Time a » SYSLOG Sener 0 ee
PKA Solution
To view the solution or edit the lab file, you can click the "Wizard hat" icon, and enter
the following password: C!ScOM@ster
Right-click the "Answer network" tab and then click "Show Answer network".
Note: Be careful not to change anything, so that the lab will remain intact.


### Lab Assignments & Solutions — strona 250

Lab Task 1: Revision Questions
IP ACL (Access Control List) is a rule-based feature in Cisco routers that enables network
administrators to identify packet types. An ACL can identify a packet by source or
destination IP address, or source or destination port. When a router identifies a packet
that matches an ACL, one of several actions can be taken by the router.
Complete the following questions to review ACLs.

1. What is the difference between named and numbered ACLs?
Numbered ACLs use numbers for identification, while named ACLs use names for
identification.

2 True or False: Standard ACLs filter traffic only by the destination IP address.
False - A standard ACL filters traffic by source IP address.

3 What is the default ACE located at the end of any IPv4 ACL?
Implicit Deny.

4 Does a router verify every packet it forwards against an ACL in chronological

order?
Yes - Every inbound or outbound packet parameter is checked according to the received
information in every ACE. For example, if you send a stateful packet out via HTTP it is
only checked against the outbound rules. The return packet is not checked. On the flip
side, if you send out a stateless packet like SNMP, the return packet is a new packet and
checked against inbound rules.
Page5


### Lab Assignments & Solutions — strona 251

Lab Task 2: Configure a Numbered Standard ACL
Use a numbered ACL to block traffic from the marketing network to the server farm.
192,168, 1.0/24 RAD 172.16.1.0/24 Server Farm
AA ara
™ 10.0.0,0/30 .: 80.10. 10.0/30 —_
2901
SP
a oa a ]
192.168.2.0/24 Management 172.16.2.0/24 Marketiog
Part 1: Create the ACL
In R2, configure the network policies in accordance with the following steps:
1 Create a standard ACL numbered 1.
R2>enable
R2#configure terminal
R2(config)#ip access-list standard 1
R2(config-std-nacl)#exit


### Lab Assignments & Solutions — strona 252

2 OnR2, add the appropriate ACEs to meet the following requirements:
a) Traffic from the marketing (172.16.2.0/24) network to the server farm is not
permitted.
b) All other network traffic is permitted.
R2(config)#access-list 1 deny 172.16.2.0 0.0.0.255
R2(config)#access-list 1 permit any
3° What is the wildcard mask for /24?
(0100) 225;5)
Part 2: Apply the ACL on the Correct Interface
4 Apply the ACL you created on the correct interface for inbound traffic.
Tip: Apply standard ACLs as close as possible to the destination, and for outbound
traffic.
R2(config)#interface gigabitethernet 0/0
R2(config-if)#ip access-group 1 out
R2(config-if)#exit
Note: Gigabitethernet 0/0 is closest to the server farm (the destination of the traffic we
want to check).


### Lab Assignments & Solutions — strona 253

Part 3: Verify the ACL Configuration
5 Use show access-lists to view the ACL configuration, and show running-config to
verify the application of the ACL on GigabitEthernet 0/0.
R2(config)#do show access-lists
R2 (config) ¢#
R2 (config) #do show access-lists
Standard IP access list 1
10 deny 172.16.2.0 0.0.0.255
20 permit any
R2 (config) # “
R2(config)#do show running-config
q “a
interface GigabitEtherneto/o
4p address 172.16.1.100 255.255.255.0]
ip access-group 1 out
duplex auto
speed auto
interface GigabitEthernet0/1
ip address 172.16.2.100 255.255.255.0
duplex auto
speed auto
interface GigabitEthernet6/0/0
ip address 10.0.0.2 255.255.255.252
qacevewee GigabitEthernet0/1/0
ip address 90.10.10.1 255.255.255.252
aeeReMce GigabitEthernet0/2/0
no ip address
shutdown
\
--More-- bs


### Lab Assignments & Solutions — strona 254

6 Use ping to verify that the configuration is correct.
From a PC in the marketing network (such as 172.16.2.1), try to ping a server (such
as 172.16.1.1). The ping should fail.
Other hosts on different networks should have access. Ping the same server again,
but from a PC in the management network (such as 192.16.2.1), and compare the
results with the previous test.
Ping 172.16.1.1 from 172.16.2.1
C:\>ping 172.16.1.1
Pinging 172.16.1.1 with 32 bytes of data:
Reply from 172.16.2.100: Destination host unreachable.
Reply from 172.16.2.100: Destination host unreachable.
Reply from 172.16.2.100: Destination host unreachable.
Reply from 172.16.2.100: Destination host unreachable.
Ping statistics for 172.16.1.1:
Packets: Sent = 4, Received = 0, Lost = 4 (100%
loss),
Ping 172.16.1.1 from 192.168.2.1
C:\>ping 172.16.1.1
Pinging 172.16.1.1 with 32 bytes of data:
Reply from 172.16.1.1: bytes=32 time<lms TTL=126
Reply from 172.16.1.1: bytes=32 time=12ms TTL=126
Reply from 172.16.1.1: bytes=32 time=14ms TTL=126
Reply from 172.16.1.1: bytes=32 time=14ms TTL=126
Ping statistics for 172.16.1.1:
Packets: Sent = 4, Received = 4, Lost = 0 (0%
loss),
Approximate round trip times in milli-seconds:
Minimum = Oms, Maximum = 14ms, Average = 10ms


### Lab Assignments & Solutions — strona 255

Lab Task 3: Configure a Named Standard ACL
Use a named standard ACL to block traffic from a specific host PC to the R&D network.
Part 1: Create the ACL
In R1, configure the network policies in accordance with the following steps:
1 Create a standard ACL named BLOCK_HOST (case-sensitive).
R1>enable
Rl#configure terminal
R1(config)#ip access-list standard BLOCK_HOST
R1(config-std-nacl)#
2 Add the appropriate ACEs to meet the following requirements:
a) Traffic from the 192.168.2.1 host to the 192.168.1.0/24 network is not
permitted.
b) All other network traffic is permitted.
R1(config-std-nacl)#deny host 192.168.2.1
R1(config-std-nacl)#permit any
R1(config-std-nacl)#exit
3 What is the default standard ACL number range?


### Lab Assignments & Solutions — strona 256

Part 2: Apply the ACL on the correct interface
4 Apply the ACL you created on the correct interface for outbound traffic.
R1(config)#interface gigabitethernet 0/0
R1(config-if)#ip access-group BLOCK_HOST out
R1(config-if)#exit
Part 3: Verify the ACL Configuration
5 Use show access-lists to view the ACL configuration, and show running-config to
verify the application of the ACL on GigabitEthernet 0/0.
R1(config)#do show access-lists
Rl (config) #do Show access—lists
Standard IP access list BLOCK_HOST
10 deny host 192.168.2.1
20 permit any
Rl (config) #| S
R1(config)#do show running-config
a ra
interface GigabitEthernet0/0
ip address 152.168.1.100 255.255.255.0
ip access-group BLOCK_HOST out
duplex auto
speed auto
ineeeracs GigabitEthernet0/1
ip address 192.168.2.100 255.255.255.0
duplex auto
speed auto
dnb race GigabitEtherneto/0/0
ip address 10.0.0.1 255.255.255.252
ft
interface GigabitEthernet0/1/0
no ip address
shutdown
ft
interface GigabitEthernet0/2/0
no ip address
shutdown
dopertace Vianl
--More-- iad


### Lab Assignments & Solutions — strona 257

6 Ping both computers on the 192.168.1.0/24 network from the host 192.168.2.1.
The test should fail.
To verify that only this host is blocked, try pinging the same computers from the
second host 192.168.2.2. The ping should be successful.
Ping 192.168.1.1 from 192.168.2.1
C:\>ping 192.168.1.1
Pinging 192.168.1.1 with 32 bytes of data:
Reply from 192.168.2.100: Destination host unreachable.
Reply from 192.168.2.100: Destination host unreachable.
Reply from 192.168.2.100: Destination host unreachable.
Reply from 192.168.2.100: Destination host unreachable.
Ping statiarics for 192.168 1.04
Packets: Sent = 4, Received = 0, Lost = 4 (100% loss),
Ping 192.168.1.2 from 192.168.2.2
c:\>ping 192.168.1.2
Pinging 192.168.1.2 with 32 bytes of data:
Reply from 192.168.1.2: bytes=32 time<lms TTL=127
Reply from 192.168.1.2: bytes=32 time=Ims TTL=127
Reply from 192.168.1.2: bytes=32 time=6éms TTL=127
Reply from 192.168.1.2: bytes=32 time=12ms TTL=127
Ping Statistics for 192.166.1.2*
Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),
Approximate round trip times in milli-seconds:
Minimum = Oms, Maximum = 12ms, Average = 4ms
'
Sa’ | Important!
o © * | Continue to task 4 only after learning about extended ACL, and when you
= are instructed to do so! Don’t close Packet Tracer after completing Task 3.


### Lab Assignments & Solutions — strona 258

Lab Task 4: Configure a Numbered Extended ACL
Use an extended numbered ACL to block traffic from an endpoint on the marketing
network to an endpoint on the R&D network.
Part 1: Create the ACL
In R2, configure the network policies in accordance with the following steps:
1 Create an Extended ACL numbered 100.
R2(config)#ip access-list extended 100
R2(config-ext-nacl)#exit
2 Add the appropriate ACEs to meet the following requirements:
a) Traffic from host 172.16.2.1 to host 192.168.1.2 is not permitted.
b) All other network traffic is permitted.
R2(config)#access-list 100 deny ip host 172.16.2.1 host
192.168.1.2
R2(config)#access-list 100 permit ip any any
3 What is the default extended ACL number range?
100-199, 2000-2699
4 What will happen if we type “deny any” in the first statement?
All traffic will be denied.


### Lab Assignments & Solutions — strona 259

Part 2: Apply the ACL on the correct interface
5 Apply the ACL you created on the correct interface for inbound traffic.
Tip: Apply extended ACLs as close as possible to the source, and for inbound
traffic.
R2(config)#interface gigabitethernet 0/1
R2(config-if)#ip access-group 100 in
R2(config-if)#exit
Part 3: Verify the ACL configuration
6 Use show access-lists to view the ACL configuration, and show running-config to
verify the application of the ACL on GigabitEthernet 0/1.
R2(config)#do show access-lists
R2 (contig) #do show access-lists
Standard IP access list 1
10 deny 172.16.2.0 0.0.0.255
Extended 7 access list 100
10 deny ip host 172.16.2.1 host 192.168.1.2
20 permit ip any any
R2 (config) # he
R2(config)#do show running-config


### Lab Assignments & Solutions — strona 260

! “a
interface GigabitEthernet0/0
ip address 172.16.1.100 255.255.255.0
ip access-group 1 out
duplex auto
speed auto
interface GigabitEthernet0/1
ip address 172.16.2.100 255.255.255.0
ip access-group 100 in
duplex auto
speed auto
J
interface GigabitEtherneto/0/0
ip address 10.0.0.2 255.255.255.252
J
interface GigabitEthernet0/1/0
ip address 80.10.10.1 255.255.255.252
J
interface GigabitEthernet0/2/0
no ip address
shutdown
4
interface Vlanl
--More-- mA
7 Use ping to make sure both hosts cannot communicate with each other.
However, use ping to verify that other hosts will be able to access the 192.168.1.2
host.
Ping from 172.16.2.1 to 192.168.1.2
c:\>ping 192.168.1.2
Pinging 192.168.1.2 with 32 bytes of data:
Reply from 172.16.2.100: Destination host unreachable.
Reply from 172.16.2.100: Destination host unreachable.
Reply from 172.16.2.100: Destination host unreachable.
Reply from 172.16.2.100: Destination host unreachable.
Ping statistics for 19?.168.1..2*
Packets: Sent = 4, Received = 0, Lost = 4 (100% loss),


### Lab Assignments & Solutions — strona 261

Ping from 172.16.2.2 to 192.168.1.2

C:\>ping 192.168.1.2
Pinging 192.168.1.2 with 32 bytes of data:
Reply from 192.168.1.2: bytes=32 time=13ms TTL=126
Reply from 192.168.1.2: bytes=32 time<lms TTL=126
Reply from 192.168.1.2: bytes=32 time<ims TTL=126
Reply from 192.168.1.2: bytes=32 time<lms TTL=126
Ping statistics for 192.168.1.2:

Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),
Approximate round trip times in milli-seconds:

Minimum = Oms, Maximum = 13ms, Average = 3ms


### Lab Assignments & Solutions — strona 262

Lab Task 5: Configure a Named Extended ACL (Bonus)
Use an Extended Named ACL to block HTTP traffic from a host on the R&D network to
the web server on the Server Farm network.
Part 1: Create the ACL
In R1, configure the network policies in accordance with the following steps:

1 Create an extended ACL named BLOCK_HTTP (case-sensitive).
R1(config)#ip access-list extended BLOCK_HTTP
R1(config-ext-nacl)#

2 Add the appropriate ACEs to meet the following requirements:

a) Web traffic (HTTP) from the 192.168.1.2 host to the web server is not
permitted.
b) All other network traffic is permitted.

R1(config-ext-nacl)#deny tcp host 192.168.1.2 host 172.16.1.2 eq
80
R1(config-ext-nacl)#permit ip any any
R1(config-ext-nacl)#exit
Part 2: Apply the ACL on the correct interface

3 Apply the ACL you created on the correct interface for inbound traffic.
R1(config)#interface gigabitethernet 0/0
R1(config-if)#ip access-group BLOCK_HTTP in
R1(config-if)#exit


### Lab Assignments & Solutions — strona 263

Part 3: Verify the ACL configuration
4 Use show access-lists to view the ACL configuration, and show running-config to
verify the application of the ACL on GigabitEthernet 0/0.
R1(config)#do show access-lists
Rl(config)#do show access—lists
Standard IP access list BLOCK_HOST
10 deny host 192.168.2.1
20 permit any (4 matchi(es
extended IP access list BLOCK HITP
10 deny tcp host 152.168.1.2 host 172.16.1.2 eq waw
20 permit ip any any
Rl (config) # ~
R1(config)#do show running-config
! a
4
4
interface GigabitEtherneto/0
ip address 192.168.1.100 255.255.255.0
ip access-group BLOCK HOST out
duplex auto
speed auto
interface GigabitEthernet0/1
ip address 192.168.2.100 255.255.255.0
duplex auto
speed auto
a
interface GigabitEtherneto/0/0
ip address 10.0.0.1 255.255.255.252
4
interface GigabitEtherneto/1/0
no ip address
shutdown
a
interface GigabitEthernet0/2/0
--More-- nd
R1(config)#exit


### Lab Assignments & Solutions — strona 264

5 Open 192.168.1.2, click the Desktop tab, click the web browser icon, and try to
access the www.cyberpro.com website. Can you view the website? Why?
Try to access the website from the 192.168.1.1 web browser. Can you view the
website? Why?
From PC 192.168.1.2, browse to www.cyberpro.com (unsuccessful).
Answer: No, traffic to port 80 is blocked.
ad
Physical Config Desktop Programming Attributes
<> URL http:/Awww.cyberpro.com
Request Timeout
From PC 192.168.1.1, browse to www.cyberpro.com (successful).
Answer: Yes, the ACL only applies to the 192.168.1.2 host.
eae
Fe re
Cyber Pro
Well done! You made it!
“If you can dream it, you can do it.” —Walt Disney
Are you up for another challenge?
Block all incoming PING requests to the Server Fram. All other network traffic is permitted.
Good Luck!


### Lab Assignments & Solutions — strona 265

Lab Task 6: Modify an Extended ACL (Bonus)
Modify an existing Extended ACL to include an ACE that will block HTTPS traffic.
Part 1: Modify the ACL
Since a new policy was issued, we need to edit the extended ACL from Lab Task 5
above. Secure web traffic (HTTPS) is now also not permitted between the 192.168.1.2
host and the web server. Make the appropriate changes to the ACL.
1 In R1, run show access lists. You should see two ACEs under the extended ACL
from Lab Task 5. The ACEs are listed in numerical order, whereby the first ACE is
10, the second is 20, and so on. This means numbers 11 to 19 are free and can be
used to add new ACEs in the correct positions in the ACL.
Rl#show access-lists
R1l¢
Rl#show access-lists
Standard IP access list BLOCK HOST
10 deny host 192.168.2.1 |
20 permit any (4 match (es))
Extended IP access list BLOCK HTTP ss
First
R1#| Mw
2 The newACE needs to come after the first ACE, but before the last (permit any)
ACE (hint: 11-19).
Rl#configure terminal
R1(config)#ip access-list extended BLOCK_HTTP
R1(config-ext-nacl)#15 deny tcp host 192.168.1.2 host 172.16.1.2
eq 443
R1(config-ext-nacl)#exit


### Lab Assignments & Solutions — strona 266

3 Use show access-lists to verify that the new ACE was added correctly.
R1(config)#do show access-lists

Ri(config)#do show access—lists

Standard IP access list BLOCK_HOST
10 deny host 192.168.2.1
20 permit any

Extended IP access list BLOCK_HTTP
10 deny tcp host 192.168.1.2 host 172.16.1.2 eq www
HS deny tcp host 192.168.1.2 host 172.16.1.2 eq 443
20 permit ip any any
