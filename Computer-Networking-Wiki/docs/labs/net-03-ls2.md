# NET-03-LS2 — Initial Cisco Device Configuration

[← Wszystkie laboratoria](index.md)

> **Typ:** laboratorium z rozwiązaniem. Zachowano wszystkie kroki, pytania, odpowiedzi, komendy i wartości z materiału źródłowego; usunięto jedynie techniczne nagłówki stron OCR.

## Powiązana teoria

- [Cisco IOS and CLI](../03-cisco-ios/cisco-ios.md)
- [Initial Cisco device configuration](../03-cisco-ios/initial-device-configuration.md)

## Pełny przebieg laboratorium

> Zakres źródłowy: strony 47–70.

Computer Networking
Lab Assignment Switch & IOS
& Solution Fundamentals
4 NET-03-LS2
Ta Initial Cisco Device
at U Configuration
Copyright © 1996-2020 HackerU Ltd.
All Rights Reserved.

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

4 When the boot ends, press Enter to begin.
B Laptopo os o x
Physical Config Desktop Programming —_ Attributes
[Terminal
[Top

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

22 Which PC physical address is associated with the fastEthernet 2 interface?
S1-Floorl#show mac-address-table
Mac Address Table
Vlan Mac Address Type Ports
il Q001.c9bb.9e7b DYNAMIC Fa@/2
1 0003.e41a.b68d DYNAMIC Fa@/1

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
