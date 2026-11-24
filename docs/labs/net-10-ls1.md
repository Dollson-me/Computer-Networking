# NET-10-LS1 — Configure NTP and Syslog

[← Wszystkie laboratoria](index.md)

> **Typ:** laboratorium z rozwiązaniem. Zachowano wszystkie kroki, pytania, odpowiedzi, komendy i wartości z materiału źródłowego; usunięto jedynie techniczne nagłówki stron OCR.

## Powiązana teoria

- [Syslog](../07-operations-security/syslog.md)
- [NTP](../07-operations-security/ntp.md)

## Pełny przebieg laboratorium

> Zakres źródłowy: strony 232–245.

Computer Networking
Lab Assignment Diagnostics &
& Solution Troubleshooting
sohRe NET-10-LS1
ol Configure NTP and Syslog
El

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
