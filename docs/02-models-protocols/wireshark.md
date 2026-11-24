# Wireshark

[← Indeks wiki](../index.md)

> **Źródło główne:** Computer Networking Textbook.pdf, s. 46–55. Treść została uporządkowana tematycznie; pełny ekstrakt źródłowy znajduje się w `_source-archive/`.


## Materiał kanoniczny

Wireshark is a free application that enables the capture and viewing of data traveling
back and forth on the network. It is able to read the contents of each packet and apply
different filters.
Wireshark is commonly used to troubleshoot network problems, and develop and test
software.
[a
aa @|5 xe S = £BIEBIAaak
(Winco e dspley titer. <oxi7> ES =] coresson... +
Capture
using this fter: (W]]entera cepturefiter, SSS) | irae sh =
No Interfaces found
Learn
User's Guide Wiki Questions and Answers Mailing Lists
You are running Wireshark 3.0.1 (v3.0.1-0-gea35icd8). You receive automatic updates.
© Ready to load or capture No Packets Profile: Default

Capturing Data
When invoked, Wireshark presents an initial screen with a list of available network
interfaces. Selecting an interface will start the capture of all traffic that passes through
it.
Wireshark can also be used to open traffic captured by other tools, such as TCP dump.
a
4uc TDRE QeestseBaqan
Gs Gi Jenson +
1@.e@e¢88 16.1.26.1 157.249.1.. TLSv1.2 85 Application Data =|
2.078369 157.240.1.53 10.1.28.1 TCP 60443 + 8199 [ACK] Seq=1 Ack=32 Win=144 Len=0 =
3.131368 10.1.26.1 62.0.136... TCP 55 [TCP segment of a reassembled PDU) =
40.131571 62.0.136.237 16.1.20.1 TCP 66 8093 + 11632 [ACK] Seq=1 Ack=2 Win=254 Len=@ SLE=1 SRE=2 —
5@.155242 157.240.1.53 1@.1.28.1 TLSv1.2 92 Application Data FJ
6@.195718 10.1.20.1 157.240.1.. TCP 548199 + 443 [ACK] Seq=32 Ack=39 Win=1027 Len=@ =
| 91.228919 146.185.219.33 16.1.20.1 TCP 69.80 + 49803 [ACK] Seq=l Ack=1 Win=501 Len=0 =
if . eep-A e + 116 A q: Ack=: = =
Frame 1: 85 bytes on wire (680 bits), 85 bytes captured (680 bits) on interface 0 a
Ethernet II, Src: HewlettP_3e:5b:9e (f4:39:09:3e:5b:9e), Dst: Fortinet_4e:8b:12 (@4:d5:90:4e:8b:12)
Internet Protocol Version 4, Src: 1@.1.20.1, Dst: 157.240.1.53
Transmission Control Protocol, Src Port: 8199, Dst Port: 443, Seq: 1, Ack: 1, Len: 31 s
9000 04 d5 90 4e 8b 12 F4 39 09 3e 5b 9e O8 00 45 00 Ne +9 ->[---E is
@@ 47 da 81 40 00 8@ G6 63 88 Ga O1 14 G1 9d FO G @ c
61 35 26 67 61 bb Sa 42 67 7e aO Oc O9 b2 5A 18 5 2B gy Pp
@4 @3 86 Ge 00 00 17 03 03 20 1a ca 99 84 24 00 ¥
Main View
Packet List - Packet List is the main view of Wireshark. It lists captured packets in the
order of their capture, and offers various search and filter options.
Packet Details - Packet Details is the part in the middle that displays the details of a
specific packet.
The details are divided into fields corresponding to TCP/IP layers, such as the Frame
(Physical), Ethernet (Data Link), and IP (Network).
Packet Bytes - The bottom part of the view corresponds to the actual bytes of the
selected packet, in hexadecimal format and ASCII encoding.

ICMP Traffic
The Ping command uses ICMP and includes a request and a reply.
Each ICMP packet is numbered and can be identified to find a corresponding response.
ICMP has only four fields since it is a Layer 3 protocol.
Each ICMP echo (ping) packet includes all the basic symbols and numbers on the
keyboard.
a
aacoeir Rei CeessFsSQ2>aqaaant
No. Time ‘Source Destination Protocol Length Info cet
f 1 6.000000 172.42.0.157 172.42.0.140 ‘ICMP 98 Echo (ping) request id-0xdcda, seq=1/256, tt1-64
Oe 2 0.300934 172.42.0.146 172.42.0.157 ICMP 98 Echo (ping) reply id=@x@cda, seq=1/256, ttl=64
3 1.006925 172.42.0.157 172.42.0.140 ICMP 98 Echo (ping) request id=@x@cda, seq=2/512, tt1=64
4 1.298136 172.42.0.140 172.42.0.157 ICMP 98 Echo (ping) reply id=@x@cda, seq=2/512, ttl-64
Frame 1: 98 bytes on wire (784 bits), 98 bytes captured (784 bits) tos
Ethernet II, Src: Vmware_c6:21:44 (06:@c:29:c6:21:44), Dst: SamsungE_83:45:3b (@4:d6:aa:83:45:3b)
Internet Protocol Version 4, Src: 172.42.0.157, Dst: 172.42.0.140
» Internet Control Message Protocol
Type: 8 (Echo (ping) request)
code: 0
Checksum: @x7d9@ [correct]
[Checksum Status: Good]
Identifier (BE): 3290 (@x@cda)
Identifier (LE): 55820 (@xda@c)
Sequence number (BE): 1 (@x@001)
Sequence number (LE): 256 (@x@100) v
2 @4 d6 aa 83 45 3b 08 Qc 29 c6 21 44 G8 0G 45 00 &3 P eights ES
ee1 @8 54 8c 1a 40 06 4@ G1 55 11 ac 2a 68 9d ac 2a T.-@@ U--*---*
020 @@ 8c @8 86 7d 90 Oc da OO 61 e9 53 bb 5c G8 BE } *Se\e°
030 09 00 04 11 06 00 00 0 09.00101112131415 --
0240 16 17 18 19 1a 1b 1c 1d 1e 1f 26 21 22 23 24 25 Lage
0050 26 27 28 29 2a 2b 2c 2d 2e 2F 30 31 32 33 34.35 = &'()*4,- ./012345 ¥
@ * cw sample.cap Packets; 8 : Displayed: 8 (100.0%) Profile: Default

DNS Traffic
DNS traffic includes multiple requests and replies.
Most of a search tree will not appear in a packet; only the request and response.
DNS may try to automatically resolve both A and AAAA records corresponding to the
IPv4 and IPv6 addresses, respectively.
a
AecO1:HREC ese etFeS2aqaqar
Expression. +
No. Time Source Destination Protocol Length Info
E 1 2.090000 172.42.0.151 172.42.0.138 DNS 74 Standard query @xd282 AAAA api.segment.io
« 2 0.010187 172.42.0.138 172.42.0.151 DNS: 158 Standard query response @xd282 AAAA api.segment.io SOA
3 5.906976 172.42.0.157 172.42.0.138 DNS 71 Standard query @xb97@ A hackeru.com
45.994438 172.42.0.138 172.42.0.157 DNS 87 Standard query response @xb970 A hackeru.com A 107.180.
5 5.995163 172.42.0.157 172.42.0.138 DNS 71 Standard query @x@276 AAAA hackeru.com
6 6.121930 172.42.0.138 172.42.0.157 DNS 142 Standard query response @x@276 AAAA hackeru.com SOA nsd
Frame 1: 74 bytes on wire (592 bits), 74 bytes captured (592 bits) “
Ethernet II, Src: LcfcHefe_7a:4b:17 (e8:6a:64:7a:4b:17), Dst: D-LinkIn_d7:48:d@ (78:32:1b:d7:48:de)
Internet Protocol Version 4, Src: 172.42.0.151, Dst: 172.42.0.138
User Datagram Protocol, Src Port: 62297, Dst Port: 53
~ Domain Name System (query)
Transaction ID: @xd282
Flags: @x@1@0 Standard query
Questions: 1
Answer RRS:
Authority RRs: @
Additional RRs: @ v
) 78 32 1b d7 48 d@ e8 Ga 64 7a 4b 17 @8 06 45 06 = x2--H--j dzK---E
219 @@ 3c Gf bb 0 CO 8811 71 BB ac 2a 097 ac 2a -<o geet
0920 @@ Ba f3 59 @@ 35 @@ 28 b1 10 d2 82 @1 06 G2 1 Y-5-¢ oe
220 @@ 80 00 20 62 20 63 G1 70 69 O7 73 65 67 6d 6S a pi-segme
10 Ge 74 @2 69 6F 00 0 1c 00 01 nt-io
@ * onssample.cap Packets: 6 * Displayed: 6 (100.0%) Profile: Default

HTTP Traffic
HTTP is an unsecure protocol used to transfer information over the web.
Since HTTP traffic is not encrypted, it can be sniffed on the network.
(iP Sompiocon =e x
File Edit View Go Capture Analyze Statistics Telephony Wireless Tools Help
4G C4O\LDRBEVCeeZtseSaaanh
ity EGS =) Expression. +
No, Time source Destination Protocol Length Info
16 14.384881 172.42.0.157 192.195.77.80 HTTP 779 POST /login-form/ HTTP/1.1_(application/x-waw-form-ur
e 22 14.571270 192.195.77.80 172.42.0.157 HTTP 357 HTTP/1.1 200 OK (text/html)
Frame 16: 779 bytes on wire (6232 bits), 779 bytes captured (6232 bits)
Ethernet II, Src: Vmware_c6:21:44 (08:0c:29:c6:21:44), Dst: D-LinkIn_d7:48:d@ (78:32:1b:d7:48:d@)
Internet Protocol Version 4, Src: 172.42.0.157, Dst: 192.195.77.80
Transmission Control Protocol, Src Port: 60834, Dst Port: 8@, Seq: 1, Ack: 1, Len: 713
» HTML Form URL Encoded: application/x-www-form-urlencoded
Form item: “username” = "lionk"
Form item: "password" = "Aa123456"
Form item: “submit” = "Login®
960 78 32 1b d7 48 do 00 Oc 29 cé 21 44 SMEG 45.00 x2 -H- )- IOBBE ~
0010 @2 fd bf 2f 40 82 40 e6 bd FO ac 2a G8 9d cB C3 10-0 *
4d 5@ ed a2 @@ 5@ dd 31 94 33 cb c3 de c6 8918 MP. -P-1 3
9 @0 eS bd ca 628 00 61 G1 @8 Ga c7 af be 43 d9 21 cel
10 5f ed 50 4f 53 54 20 2F 6c GF 67 69 Ge 2d 66 GF _-POST / login-fo
0050 72 6d 2f 26 48 54 54 5@ 2 31 2e 31 @d @a 48 GF =—rm/ HTTP /1.1--Ho
9 73 74 3a 2077 7777 2e 64 65 6d Gf 2e 61 Gd 69 = st: www. demo.ami
e 74 6a 61 6b 68 75 2e 63 GF 6d Od Oa 55 73 65 72 tjakhu.c om--User
59 2d 41 67 65 Ge 74 3a 20 4d GF 7a 69 6c 6c 61 2F Agent: Nozilla/
990 35 2e 30 2@ 28 58 31 31 3b 20 4c 69 Ge 75 78 26 «5. (X11 ; Linux
2 78 38 36 Sf 36 34 3b 20 72 76 3a 36 30 2e 30 29 «= x86_64; rv:60.0) wl
QF HTTP sample.cap Packets: 31 Displayed: 2 (6.5%) Profile: Default,
Captured data can be saved as a .pcap or .pcapng files for later use or sharing. This
option is available by clicking “File” and selecting “Save As...”.
The .pcapng files store additional information regarding captured data, such as
interfaces, statistics, name resolution, and more.

(Mf *Cthemet 3 - ia x
File Edit View Go Capture Analyze Statistics Telephony Wireless Tools Help
Open Ctrl+0 zFTaabeaaanr
Open Recent pO pression. +
Merge. Destination Protocol Length Info ”
Import from Hex Bump L 127.0.0.1 TcP 94 220i
Close Ctrlew L 127.0.0.1 TCP 96 220:
L 127.0.0.1 TcP 94 220:
=e oe L 127.0.0.1 TCP 96 220:
| Seven ate SfteS 127.0.0.1 1c 94 220;
File Set i 127.0.0.1 TcP 96 220:
L 127.0.0.1 TCP 94 220%
Export Specified Packets. l 127.0.0.1 TCP 96 220:
Export Packet Dissections vo 127.0.0.1 TCP 94 2207
Export Packet Bytes... Cirle ShifteX 1 127.0.0.1 TCP 96 220:
Export PDUs to Files. L 127.0.0.1 TCP 94 220;
Export TLS Session Keys. 5
Export Objects »
its), 55 bytes captured (44@ bits) on interface @ “
Print Cirle? 100 (00:00:00:00:00:00), Dst: 00:00:00 00:00:00 (90:00:00:0¢
1 127.0.0.1, Dst: 127.0.0.1
ae Sree be I A. OP. “i
€ >
e082 80 00 e0 22 20 00 FEMME co 00 ea es co 4500 CRE
e018 @8 29 c@ 71 49 a2 80 a6 G0 CO 7F OO GO C1 7F OO = -)-g@--- -----
0020 @@ 01 08 9b OB 9a ac G7 Je 14 1469 16 885018 «ga -P-
003@ FF #F Se 27 8 00 4d AM
QO F wireshsrk_Ethernet 3_20200722154827_301240.peapng || Packets: 16 + Displayed: 16 (100.0%) || Profile: Default

Filtering Traffic
A .pcap file can contain thousands of packets, even after a few seconds of logging.
To view the packets efficiently, filters can be applied. Filters can also be applied during
capture to prevent the capture of unwanted packets.
Filters are logical conditions that are applied using &&, | |, == and !=.
Brackets can also be used.
MLITTP Semple cop eR
File Edit View Go Capture Analyze Statistics Telephony Wireless Tools Help
Aec@1rOoRelir_ee2ts#etaaak
(Wacpiy e display iter. <cariy> CES ~) exwession. | +
No. Time Source Destination Protocol Length Info =>
| 1 8.000000 172.42.0.157 81.218.31.137 Top 66 38908 + 86 [ACK] Seq=1 Ack=1 Win=329 Len=0 ene |
+3 3.426254 172.42.0,151 | ncaa, ee: 60 16852 + 8@ [ACK] Seq=1 Ack=1 Win=1023 Len=1
4 3.488723 85.114.134.23 1 Mark/Unmark Packet 66 80 + 16852 [ACK] Seq=1 Ack=2 Win=260 Len=0 SLE=1
Ignore/Unignore Packet
Set/Unset Time Reference
Time Shift.
Packet Comment.
9 14.146553 172.42.0.157 1 74 60446 + 86 [SYN] Seq=@ Win=29260 Len=@ MSS=146@ S
16 14. 266035 172.42.0.157 1 Edit Resolved Name 74 60834 + 86 [SYN] Seq=@ Win=2926@ Len=@ MSS=146@ S
11 14.206138 172.42.0.157 1 Seq=@ Win=29200 Len=@ MSS=1460 S
12.14.218727—172.217.22.18 7 eee ssiiter sees | ace Seqe0 Ack=1 Win=6010? Len=ofllll
a OE + Prepare a Filter > Not Selected pee eee eee
= Conversation Filter , and Selected z:
Frame 3: 60 bytes on wire (48@ bits), 6@ by Celadon Canveretion > of Selected
Ethernet II, Src: LefcHefe_7a:4b:17 (e8:6a SCIP > nor seleered 248:de)
Internet Protocol Version 4, Src: 172.42.0. 5 vant
Transmission Control Protocol, Src Port: 1¢ Fallow _ espe net selected
|
) 78 32 1b d7 48 d@ e8 Ga 64 7a 4b 17 68 Copy »
©9 29 ae 6c 40 00 80 05 4 17 ac 2a 00
86 17 41 d4 @@ 50.96 16 c9 1f 18 Sb fF —_—Protocol Preferences y
9 @3 fF Ga Se 68 22 02 20 00 08 20 26 Decode As...
‘Show Packet in New Window
O FY arp samplecap Packets: 31 « Displayed: 31 (100.0%) Profile: Default

Wireshark Filters
Wireshark includes many display filters.
&& - means that both conditions are searched to match packets.
| | - means that one of the conditions is searched to match packets.
== - searches for everything that matches the specified parameter.
!= - searches for everything that doesn’t match the specified parameter.
The following table lists some useful filters.
Filter Data
Find a match for packets using a specific protocol (i.e.
Protocol Name
ICMP, ARP, HTTP, DNS).
“ Find a match for this address in the source and
ip.addr == 10.0.0.3 oo.
destination.
ip.dst != 10.0.0.2 Find all matches that do not have this destination.
ip.sre != 10.0.0.3 Find all matches that are not from this source.
tcp.port == 25 &&
P-P Find packets that match both port numbers in TCP.
tcp.port == 80
udp.port == 53 || Find packets that match one of the port numbers in
udp.port == 69 UDP.
Find packets that match a specific port number of the
tcp.dstport == 25 an
destination in TCP.

Following Traffic
After capturing traffic and filtering, stream inspection can be done.
Streams are collections of packets from the same conversation.
Left-click a packet to choose the option to follow a stream, which can be TCP, UDP, or
HTTP.
Unless traffic is encrypted, it should be readable.
een :
\aneaoe: OID; ne sn.) Gak/200010 efoe0.0
ia etcetera tamed rds
fecolmeerneny
[peaakirvar they dane Or
Scawe pec eeesumicceonratees
eoeeameee
aoe ae cas een ares ser See seb oS SSS sO SSS rec mint
epee
seare-Ketcamnend at taba 20
erry
ras Se kd
[ee
acon
eee
(Ser nodfed sat 15 an 205203787 mt
Sacre Soran
pee
sop
‘Sa rom
jlo
See wr otek ata >
Selsey ct ayaa pee
Sere tec Henao
Scam pees
Presuerieerceery
ear ation
Re aera |.

Encrypted traffic will not be readable, and will appear as non-meaningful characters.
[SSt42.0-OpensSHt_7.9p1 Debiar-9 =]
Sidecars

revrrare

nic dua anezss sacs rach hz i236 ho ch a 051 ean Ln tans sha. edman uns 2 Ae isn rusia Ae ena gun hte
Leer epee teatro entice poe ir argent Sepp ren bees enter epnepeoerti
Mersusceacntsn con oopsesnconnces fot noses cosesat mgm sein sec acon or atais ree loom see eek me onals an aesceeen omen oscoaste oececr oat
engrenthcomnn SSpngusrtatcm: ace tbturwcs ont testa cot cect gomoepaoh omentae vorgepnas ara. emeecbapapemtramyaansineoabgeac oars
Sepsis smorc at ss ep aneynt se vacmensconi arene meres amen oon ocr Gat racers eau ot Gereelcaries ceaeren aT
Setecpec cet at cut eens onto et eneeest cine: ofnemes cone mpcn ohmic: <oretca tiie al “eeceieen meee me
inundation ite tse ba gtr apa at wae ie pep eeinge sli negepieasttetsinen ga) teh goa
Sctieaiehaina oat aal_ieaaet su er aes Beate eae soreciseonaass, Uasuibpent sesoatamed weabt oncise meet spatenmancmeatsemeaerchon eon
eee Se ee ree ree eae me ee eee re eee ome
Exieeeeh om nas pudonah om nce spec cee es aaiec erat mac sel--uner maniac cones ie aneeoctartnacaer Er anerfoah confess: iz omen rar
Stectecname et erat ctmce inerera miner ant Suipecsalitlineidat—mememeation mommenemtones ce ee aim amie eae eae
ee eae

ra lewen ie aed mage ach tae Oo BM DG

Car

[erence ees

oa

een

patie es eee

Ser ee

ramet ae are

cers a as a ae

Peas er ra ee si SBS RCS

fi

caer eree

Lee ci aaa ae WP eae

zorwramkecnsial

ee ee ee ee ae ee ee

Preeti en a

NRT ee TC

Fare eri a es}

Pe-anigahion rics ferry ee ae eee eS

ini. ashe bance SEP

Bares

#0. Zo 26. PB Ah nl DOADE HS? Jot 4D ne $B. {EAD} % cM Bo bt DB. Ro BNSTBLQ, 1B) 6. FRO AL...) 2S Ms xl 1.27. IN. BBE on IY TT [Poo slo T hue 2 IO.

a acc eA wae ae ear sic eh ee Te RL ah eee eee ae
Fetlbnerdrecad frresyariesre- Qala arrsrte Arar amare ir

Beek Taree cn aa ane rer a

Cat moon
1a)

Z Lab — Network Examination with Wireshark
— Learn how to use Wireshark and how computers encapsulate and send data.
a
Perform the instructions in lab document Net-02-L1.

## Powiązane laboratoria

- [NET-02-LS1](../labs/net-02-ls1.md)


## Uzupełnienia z notatek Riseup / zajęć

<details>
<summary>Pokaż notatki prowadzącego, dodatkowe komendy i linki powiązane z tym tematem</summary>

https://www.guru99.com/types-of-ip-addresses.html
https://pmr.ii.pw.edu.pl/~pmr/ws/
Wireshark
https://www.wireshark.org/
edit>>preferences>>packet diagram
#3-way handshake
SYN -> SYN/ACK -> ACK

---

arp -a - wyświetlenie tablicy ARP
arp -d - usuwanie tablicy ARP [jako Administrator]
#Wireshark - przykładowe filtry

https://wiki.wireshark.org/CaptureFilters
https://www.wireshark.org/docs/wsug_html_chunked/
https://bugs.wireshark.org/bugzilla/attachment.cgi?id=11612
https://wiki.wireshark.org/SampleCaptures
https://wiki.wireshark.org/uploads/moin_import/attachments/SampleCaptures/dhcp.pcap
#Podstawowe komendy CISCO (IOS)
https://rioco.pl/komendy/komendy-ciscoios/
odświeżenie interfejsu
Ctrl-R - refresh
automatyczne odświeżanie interfejsu
logging synchronous
https://wiki.wireshark.org/uploads/moin_import/attachments/SampleCaptures/dns-icmp.pca
png.gz
https://ia601604.us.archive.org/20/items/cisco-packet-tracer-821-ubuntu-64bit/CiscoPacketT
racer_821_Windows_64bit.exe

---

SSH-TCP/22
Przechwycenie protokołu SSH
https://www.cloudshark.org/captures/849d3c7f09d3
LAB SSH1
hostname S1
username Admin password p@nd@

</details>

## Powiązane tematy

- [TCP, UDP, logical ports and sessions](transport-ports.md)
- [ARP and encapsulation](arp-encapsulation.md)
- [Network protocols and Windows commands](../01-foundations/network-protocols-commands.md)

## Źródła w zestawie

- `Computer Networking Textbook.pdf` — strony 46–55.
- `Computer Networking.pdf` — prezentacja kursowa; odpowiadający rozdział zachowany w `_source-archive/02-Course-Slides.md`.
- `Padriseup Computer Networking.pdf` — uzupełnienia i materiały dodatkowe, jeśli występowały dla tego tematu.
