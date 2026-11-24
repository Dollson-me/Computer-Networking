# NET-03-LS3 — Backing Up Config Files and Managing the IOS

[← Wszystkie laboratoria](index.md)

> **Typ:** laboratorium z rozwiązaniem. Zachowano wszystkie kroki, pytania, odpowiedzi, komendy i wartości z materiału źródłowego; usunięto jedynie techniczne nagłówki stron OCR.

## Powiązana teoria

- [IOS backup, TFTP and configuration register](../03-cisco-ios/ios-backup-and-register.md)

## Pełny przebieg laboratorium

> Zakres źródłowy: strony 71–85.

Computer Networking
Lab Assignment Switch & IOS
& Solution Fundamentals
NET-03-LS3
° aT Backing Up Config Files
ia U and Managing the IOS
Copyright © 1996-2021 HackerU Ltd.
All Rights Reserved.

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
