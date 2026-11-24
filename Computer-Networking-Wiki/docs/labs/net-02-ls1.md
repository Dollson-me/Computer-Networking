# NET-02-LS1 — Network Examination with Wireshark

[← Wszystkie laboratoria](index.md)

> **Typ:** laboratorium z rozwiązaniem. Zachowano wszystkie kroki, pytania, odpowiedzi, komendy i wartości z materiału źródłowego; usunięto jedynie techniczne nagłówki stron OCR.

## Powiązana teoria

- [OSI model](../02-models-protocols/osi-model.md)
- [TCP/IP model](../02-models-protocols/tcp-ip-model.md)
- [TCP, UDP, logical ports and sessions](../02-models-protocols/transport-ports.md)
- [Wireshark](../02-models-protocols/wireshark.md)
- [ARP and encapsulation](../02-models-protocols/arp-encapsulation.md)

## Pełny przebieg laboratorium

> Zakres źródłowy: strony 15–33.

Computer Networking
Lab Assignment Network
& Solution Fundamentals
ROLL) NET-02-LS1
ol TU Network Examination

with Wireshark
Copyright © 1996-2020 HackerU Ltd.
All Rights Reserved.

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
