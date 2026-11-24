# NET-11-LS1 — Implement Standard and Extended ACLs

[← Wszystkie laboratoria](index.md)

> **Typ:** laboratorium z rozwiązaniem. Zachowano wszystkie kroki, pytania, odpowiedzi, komendy i wartości z materiału źródłowego; usunięto jedynie techniczne nagłówki stron OCR.

## Powiązana teoria

- [ACL overview](../07-operations-security/acl-overview.md)
- [Standard ACL](../07-operations-security/standard-acl.md)
- [Extended ACL](../07-operations-security/extended-acl.md)

## Pełny przebieg laboratorium

> Zakres źródłowy: strony 246–266.

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
