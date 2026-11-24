# NET-04-LS2 — Remote Access with SSH

[← Wszystkie laboratoria](index.md)

> **Typ:** laboratorium z rozwiązaniem. Zachowano wszystkie kroki, pytania, odpowiedzi, komendy i wartości z materiału źródłowego; usunięto jedynie techniczne nagłówki stron OCR.

## Powiązana teoria

- [Remote access, VTY, SVI and SSH](../04-switch-security/ssh-svi-vty.md)

## Pełny przebieg laboratorium

> Zakres źródłowy: strony 111–123.

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

Lab Task 2: Verify SSH Configuration
Practice troubleshooting commands and techniques for SSH.
Part 5: Verify settings in S1
1 Make sure all settings are correct, using the following Show commands:
a. Show ip ssh (via the privileged exec mode)
bell

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

2 > Which IOS show command displays active SSH connections on the device?
Part 6: Establish an SSH session
1 Close the terminal window, disconnect the console cable, and open the
command prompt window.
<R Admin PC - ao x
Physical Conig Desktop Progamming Attibutes
e = a
O tp
roonas =

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
