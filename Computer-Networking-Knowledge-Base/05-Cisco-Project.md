# 05 — Cisco projekt — pełne notatki

Źródło: `Cisco projekt.pdf` (9 stron).

## Lab Task 1 — podział 172.16.10.0/24 na 8 podsieci

Maska: `/27` = `255.255.255.224`, rozmiar bloku 32 adresy.

| # | Network address | Usable hosts | Broadcast |
|---:|---|---|---|
| 1 | 172.16.10.0/27 | 172.16.10.1–172.16.10.30 | 172.16.10.31 |
| 2 | 172.16.10.32/27 | 172.16.10.33–172.16.10.62 | 172.16.10.63 |
| 3 | 172.16.10.64/27 | 172.16.10.65–172.16.10.94 | 172.16.10.95 |
| 4 | 172.16.10.96/27 | 172.16.10.97–172.16.10.126 | 172.16.10.127 |
| 5 | 172.16.10.128/27 | 172.16.10.129–172.16.10.158 | 172.16.10.159 |
| 6 | 172.16.10.160/27 | 172.16.10.161–172.16.10.190 | 172.16.10.191 |
| 7 | 172.16.10.192/27 | 172.16.10.193–172.16.10.222 | 172.16.10.223 |
| 8 | 172.16.10.224/27 | 172.16.10.225–172.16.10.254 | 172.16.10.255 |

## Lab Task 2 — VLAN, access ports, trunk i native VLAN

Tworzone VLAN-y:

```text
vlan 10
 name Management
vlan 20
 name Marketing
vlan 30
 name Accounting
vlan 100
 name Native
```

Przypisania access:

```text
interface range FastEthernet 0/1-10
 switchport mode access
 switchport access vlan 10
interface range FastEthernet 0/11-20
 switchport mode access
 switchport access vlan 20
interface range FastEthernet 0/21-24
 switchport mode access
 switchport access vlan 30
```

Trunki i native VLAN:

```text
interface range GigabitEthernet 0/1-2
 switchport mode trunk
 switchport trunk native vlan 100
```

Weryfikacja: `show interfaces switchport`, `show interfaces trunk`. Dla portów access użyto także `switchport nonegotiate`. Konfiguracja jest zapisywana przez `copy running-config startup-config`.

## Lab Task 3 — adresacja interfejsów i hostów

- R3 `GigabitEthernet0/0`: `172.16.10.1 255.255.255.224`, `no shutdown`.
- R3 `GigabitEthernet0/1`: `172.16.10.33 255.255.255.224`, `no shutdown`.
- Weryfikacja: `do show ip route`.
- Adresy wykorzystywane na łączach szeregowych w projekcie: `172.16.10.65`, `.66`, `.97`, `.98`, `.129`, `.130` z maską `/27`.
- Konfiguracja hostów w Packet Tracerze obejmuje m.in. CEO1 `.189`, CEO2 `.190`, Copyrighter1 `.221`, Copyrighter2 `.222`, Dialer1 `.253`, Dialer2 `.254`, a także hosty Office 2/Office 3, Guest, Admin, Syslog/NTP Server i E-mail Server. Pełne wartości ze screenshotów są zachowane niżej w transkrypcji stron 4–5.

## Lab Task 4 — Router-on-a-Stick

Fizyczny `GigabitEthernet0/0` jest uruchamiany `no shutdown`. Powstają subinterfejsy:

```text
interface GigabitEthernet 0/0.10
 encapsulation dot1Q 10
 ip address 172.16.10.161 255.255.255.224
interface GigabitEthernet 0/0.20
 encapsulation dot1Q 20
 ip address 172.16.10.193 255.255.255.224
interface GigabitEthernet 0/0.30
 encapsulation dot1Q 30
 ip address 172.16.10.225 255.255.255.224
```

Weryfikacja: `show ip interface brief`. Po stronie switcha porty GigabitEthernet są ustawiane jako trunk, a native VLAN to 100; używane jest `show interfaces trunk`.

## Task 5 — Port Security

```text
show port-security address
interface FastEthernet 0/2
 switchport mode access
 switchport port-security
 switchport port-security violation restrict
 switchport port-security mac-address sticky
show interfaces status
```

Konfiguracja jest powtarzana na S1 i S2 m.in. dla `Fa0/1`, `Fa0/11`, `Fa0/21`. Nieużywane zakresy portów są wyłączane przez `shutdown` (w materiale pokazano m.in. `interface range FastEthernet 0/12-20`). Na końcu `copy running-config startup-config`.

## Task 6 — OSPF

- `show ip route connected`;
- uruchomienie wymaganych interfejsów (`no shutdown`);
- `router ospf 1`;
- ustawienie `router-id`;
- polecenia `network ... wildcard ... area 0`;
- `passive-interface`;
- weryfikacja: `show ip protocols`, `show ip ospf interface`, `show ip ospf neighbor`;
- zapis konfiguracji.

## Task 7 — ACL

Materiał pokazuje rozszerzoną regułę blokującą komunikację pomiędzy konkretnymi hostami:

```text
access-list 137 deny ip host 172.16.10.60 host 172.16.10.29
show access-lists
```

## Task 8 — lokalne konto i zabezpieczenie konfiguracji

```text
username Admin password ACDC1973
enable password beatles1960
service password-encryption
banner motd #Only authorized personnel are allowed accessing this device#
wr
```

## Task 9 — SSH

```text
ip domain-name Cyber.local
hostname R1
crypto key generate rsa
# modulus: 1024
ip ssh version 2
line vty 0 4
 login local
 transport input ssh
show ip ssh
show ssh
```

W logu widoczny jest komunikat aktywacji SSH 1.99/2.0, timeout uwierzytelnienia 120 s, 3 próby oraz sesja z szyfrowaniem AES128-CBC i HMAC-SHA1.

# Transkrypcja źródła strona po stronie


### Cisco projekt — strona 1

Lab Task 1:
Divide 172.16.10.0/24 network into 8 subnets
Subnet number Network address Usable Host Broadcast Address
Address Range
1 172.16.10.0/27 172.16.10.1 to 172.16.10.31
172.16.10.30
2 172.16.10.32/27 172.16.10.33 to 172.16.10.63
172.16.10.62
3 172.16.10.64/27 172.16.10.65 to 172.16.10.95
172.16.10.94
4 172.16.10.96/27 172.16.10.97 to 172.16.10.127
172.16.10.126
5 172.16.10.128/27 172.16.10.129 to 172.16.10.159
172.16.10.158
6 172.16.10.160/27 172.16.10.161 to 172.16.10.191
172.16.10.190
7 172.16.10.192/27 172.16.10.193 to 172.16.10.223
172.16.10.222
8 172.16.10.224/27 172.16.10.225 to 172.16.10.255
172.16.10.254
255.255.255.224
Lab Task 2:
1.
Switch>
Switch>en
Switch#conf t
Enter configuration commands, one per line. End with CNTL/Z.
Switch (config) #vlan 10
Switch (config-vlan) #name Management
Switch (config-vlan) #exit
Switch (config) #vlan 20
Switch (config-vlan) #name Marketing
Switch (config-vlan) #exit
Switch(config)#vlan 30
Switch (config-vlan) #name Accounting
Switch (config-vlan) #exit
Switch(config)#vlan 100
Switch (config-vlan) fname Native
Switch (config-vlan) #exit
Switch (config) #
2.
Switch (config) ¥
Switch (config) #int
Switch (config) #interface range F
Switch (config) #interface range FastEthernet 0/1-10
Switch (config-if-range) #switchport mode access
Switch (config-if-range) #switchport access vlan 10
Switch (config-if-range) #exit
Switch (config) #interface range FastEthernet 0/11-20
Switch (config-if-range) #switchport mode access
Switch (config-if-range) #switchport access vlan 20
Switch (config-if-range) #exit
Switch (config) #interface range FastEthernet 0/21-24
Switch (config-if-range)#switchport mode access
Switch (config-if-range) #switchport access vlan 30
Switch (config-if-range) #exit
Switch (config) #


### Cisco projekt — strona 2

Interface range gigabitethernet 0/1-2

Switchport mode trunk

Switchport trunk native vlan 100

do show interfaces switchport
Name: Gig0/1 Name: Gig0/1
Switchport: Enabled Switchport: Enabled
eee eas frunk Administrative Mode: trunk
Administrative Trunking Encapsulation: dot1q Operational Mode: trunk
Operational Trunking Encapsulation: dot1q Administrative Trunking Encapsulation: dot1q
Negotiation of Trunking: On Operational Trunking Encapsulation: dot1q
Access Mode VLAN: 1 (default) Negotiation of Trunking: On
Trunking Native Mode VLAN: 100 (Native) Access Mode VLAN: 1 (default)
Voice VLAN: none Trunking Native Mode VLAN: 100 (Native)
Administrative private-vlan host-association: none Voice VLAN: none
Administrative private-vlan mapping: none Administrative private-vlan host-association: none
Administrative private-vlan trunk native VLAN: none Administrative private-vlan mapping: none
Administrative private-vlan trunk encapsulation: dot1q Administrative private-vlan trunk native VLAN: none
Administrative private-vlan trunk normal VLANs: none Administrative private-vlan trunk encapsulation: dot1q
Administrative private-vlan trunk private VLANs: none Administrative private-vlan trunk normal VLANs: none
Operational private-vlan: none Administrative private-vlan trunk private VLANs: none
Trunking VLANs Enabled: All Operational private-vlan: none
Pruning WEAN Enabled: 2-1001 Trunking VLANs Enabled: All
Capture Mode Disable: Pruning VLANs Enabled: 2-1001
Capture VLANs Allowed: ALL
Protected: false Capture Mode Disabled
Unknown unicast blocked: disabled Capture VLANs Allowed: ALL
Unknown multicast blocked: disabled Protected: false
Appliance trust: none Unknown unicast blocked: disabled

Unknown multicast blocked: disabled
Name: Gig0/2
Switchport: Enabled
Administrative Mode: trunk
Operational Mode: trunk
Administrative Trunking Encapsulation: dot1q
Operational Trunking Encapsulation: dotiq
Negotiation of Trunking: On
Access Mode VLAN: 1 (default)
Trunking Native Mode VLAN: 100 (Native)
Voice VLAN: none
Do show interfaces trunk

Gigo/2 on 02.14 fronting 100 Gigo/ on 02.14 trunking 100
Gigo/2 11005 Gigost 3-108
Gigove—1,10020,s0y190 Gigd/d 1,410, 20,20,100
Port: Vlans in spanning tree forwarding state and not pruned Port: Vlans in spanning tree forwarding state and not pruned
Gigd/2 1,10, 20, 30,100 Gigd/1 1,10,20, 30,100

Interface range fastethernet 0/1-24

Switchport mode access

Switchport nonegotiate

Exit

Show interfaces switchport

Switch#show interfaces switchport

Name: Fa0/1

Switchport: Enabled

Administrative Mode: static access

Operational Mode: static access

Administrative Trunking Encapsulation: dotiq

Operational Trunking Encapsulation: native

Negotiatio: Trunking: Off

— ode VLAN? 10 ee.)

Trunking Native Mode VLAN: 1 (default)

Voice VLAN: none

Administrative private-vlan host-association: none

copy running-config startup-config


### Cisco projekt — strona 3

Lab Task 3:
255.255.255.224
1.2.
R3 (config) #interface gigabitEthernet 0/0
R3(config-if)#ip add
R3(config-if)#ip address 172.16.10.1 255.255.255.224
R3(config-if)#no s
R3(config-if)#no sh
R3(config-if)#no shutdown
R3(config-if)#
SLINK-5-CHANGED: Interface GigabitEthernet0/0, changed state to up
SLINEPROTO-5-UPDOWN: Line protocol on Interface GigabitEthernet0/0, changed state to up
interface gigabitEthernet 0/1
R3(config-if)#ip address 172.16.10.33 255.255.255.224
R3(config-if)#no shutdown
R3(config-if)#
SLINK-5-CHANGED: Interface GigabitEthernet0/1, changed state to up
SLINEPROTO-5-UPDOWN: Line protocol on Interface GigabitEthernet0/1, changed state to up
R3(config-if) texit
R3 (config) #do show ip route
Codes: L - local, C - connected, S - static, R - RIP, M - mobile, B - BGP
D ~ EIGRP, EX - EIGRP external, 0 - OSPF, IA ~ OSPF inter area
Nl - OSPF NSSA external type 1, N2 - OSPF NSSA external type 2
El - OSPF external type 1, £2 ~ OSPF external type 2, E - EGP
i - IS-IS, Ll - IS-IS level-1, L2 - IS-IS level-2, ia - IS-IS inter area
+ - candidate default, U - per-user static route, 0 ~ ODR
P - periodic downloaded static route
Gateway of last resort is not set
172.16.0.0/16 is variably subnetted, 4 subnets, 2 masks
c 172.16.10.0/27 is directly connected, GigabitEthernet0/0
L 172.16.10.1/32 is directly connected, GigabitEthernet0/0
c 172.16.10.32/27 is directly connected, GigabitEthernet0/1
L 172.16.10.33/32 is directly connected, GigabitEthernet0/1
3. 4. 5.
172.16.10.65
172.16.10.66
172.16.10.97
172.16.10.98
172.16.10.129
172.16.10.130
255.255.255.224
Rl (config-if)#ip address 172.16.10.97 255.255.255.224 R2 (config) #interface Serial0/0/0
Rl (config-if)#no sh aoe :
R1(config-if) #no shutdown R2(config-if)#ip address 172.16.10.66 255.255.0.0
R2(config-if)#ip address 172.16.10.66 255.255.255.224
%LINK-5-CHANGED: Interface Serial0/0/0, changed state to down 2 fi -if #
R1 (config-if) # R2 (config-if)
Rl (config-if) # R2 (config-if) #exit
Rl (config-if)#no shutdown * A .
Rl (config-if)#interface Serial0/0/1 R2 (config) #interface Serial0/0/1
R1 (config-if) #exit R2(config-if)#ip address 172.16.10.129 255.255.255.224
Rl (config) #interface Serial0/0/1 iag-i ‘
Rl (config-if)#ip address 172.16.10.65 255.255.255.224 R2 (config if) #ip address 172.16.10.129 255.255.255.224
R3 (config) #interface Serial0/0/1
R3(config-if)#ip address 172.16.10.130 255.255.255.224
R3(config-if)#ip address 172.16.10.130 255.255.255.224
R3 (config-if) #
R3 (config-if) #exit
R3 (config) #interface Serial0/0/0
R3(config-if)#ip address 172.16.10.98 255.255.255.224
R3 (config-if) #


### Cisco projekt — strona 4

6.
eco CEO1 eco CEO2
Physical Config Desktop. Programming Attributes Physical Contig Desktop. Programming Attributes
Interface FastEthernet0 Interface FastEthernetO
IP Configuration IP Configuration
DHCP O Siatic DHCP. O Static
IPv4 Address 172.16.10.189 IPv4 Address 172.16.10.190
‘Subnet Mask (255.255.255.224 ‘Subnet Mask 255.255.255.224
Default Gateway 172.16.10.160 Default Gateway 172.16.10.160
DNS Server 0.0.0.0 DNS Server 0.0.0.0
7.
ece Copyrighter1 eee Copyrighter2
Physical Config Desktop = Programming Attributes Physical Config Desktop | Programming Attributes
Interface FastEthernet0 Interface FastEthernet0
IP Configuration IP Configuration
DHCP O Static DHCP O Static
IPv4 Address 172.16.10.221 IPv4 Address 172.16.10.222
Default Gateway 172.16.10.192 Default Gateway 172.16.10.192
DNS Server 0.0.0.0 DNS Server 0.0.0.0
8.
eco Dialert eee Dialer2
Physical Config Desktop Programming Attributes Physical Config Desktop, Programming Attributes
reece Fastethemet0 Interface Fastethometa
IP Configuration IP Configuration
oHoP O state Dyce O static
IPv4 Address 172.16.10.253 IPv4 Address 172.16.10.254
Default Gateway 172.16.10.224 Default Gateway 172.16.10.224
9.
Office 2 Office 3
eco Employee 1 eee E-mail Server
Physical Config Deso0P= Programming Attributes Physical — Config Services Desktop. Programming Attributes.
ior SeeiereD IP Configuration
DHOP O Static
DHCP O Suatic
DNS Server 0.0.0.9 DNS Server 0.0.0.0


### Cisco projekt — strona 5

eco Employee 2 eco Syslog\NTP Server
Physical Config Deskiop | Programming Attributes Physical Config Services| Desktop | Programming Attributes
Inertace Fasteheet0 8 IP Configuration
1P Configuration bHoP O static
ea OS IPv4 Address 172.16.10.29
baarenteas ee ‘Subnet Mask (255.255.255.224
Renibentt ei Default Gateway 172.16.10.0
Detaut Gateway 172.18:1032
DNS Server 00.00
DNS Sever 0000
eco Guest eco Admin
Physical Config Desktop = Programming Atuibutes Physical Con _Dasitgp | Programming _Attbutes
Interace FastEthernet0 Itertace FastEthornot0
1P Configuration 1P Configuration
DHCP O Satie DHCP O siatic
IPs Adéross 172.16:10.60 IPs Address 172.16.1028
‘Subnet Mask 255,255,255.224 ‘Subnet Mask 255,255,255 224
Default Gatoway 172.16.10% Dotault Gatoway 172.16.100
DNS Sener 00.00 DNS Server 0009
Lab Task 4:
1. interface GigabitEthernet 0/0
no shutdown
SLINK-5-CHANGED: Interface GigabitEthernet0/0, changed state to up
SLINEPROTO-5-UPDOWN: Line protocol on Interface GigabitEthernet0/0, changed state to up
2. 3. 4.
R1 (config) #int
R1 (config) #interface gig
Rl (config) #interface gigabitEthernet 0/0.10
R1 (config-subif) #
SLINK-5-CHANGED: Interface GigabitEthernet0/0.10, changed state to up
SLINEPROTO-5-UPDOWN: Line protocol on Interface GigabitEthernet0/0.10, changed state to
up
enc
R1 (config-subif) #encapsulation d
Rl (config-subif) #encapsulation dot1Q 10
R1 (config-subif)#ip address 172.16.10.161 255.255.255.224
R1 (config-subif) #exit
Rl (config) #interface gigabitEthernet 0/0.20
R1 (config-subif) #
SLINK-5-CHANGED: Interface GigabitEthernet0/0.20, changed state to up
SLINEPROTO-5-UPDOWN: Line protocol on Interface GigabitEthernet0/0.20, changed state to
up
encapsulation dot1Q 20
Rl (config-subif)#ip address 172.16.10.193 255.255.255.224
R1 (config-subif) fexit
R1 (config) #interface gigabitEthernet 0/0.30
Rl (config-subif) #
SLINK-5-CHANGED: Interface GigabitEthernet0/0.30, changed state to up
SLINEPROTO-5-UPDOWN: Line protocol on Interface GigabitEthernet0/0.30, changed state to
up
encapsulation dot1Q 30
Rl (config-subif)#ip address 172.16.10.225 255.255.255.224
R1 (config-subif) #exit


### Cisco projekt — strona 6

5.
R1#
®SYS-5-CONFIG_I: Configured from console by console
show ip interface brief
Interface IP-Address OK? Method Status Protocol
GigabitEthernet0/0 unassigned YES NVRAM up up
GigabitEthernet0/0.10 172.16.10.161 YES manual up up
GigabitEthernet0/0.20 172.16.10.193 YES manual up up
GigabitEthernet0/0.30 172.16.10.225 YES manual up up
GigabitEthernet0/1 unassigned YES NVRAM administratively down down
Serial0/0/0 172.16.10.97 YES manual up up
Serial0/0/1 172.16.10.65 YES manual up up
6.
Switch>en
Switch (config) finterface gigabitEthernet 0/1 Switch#conf t
Switch (config-if) #swi Enter configuration commands, one per line. End with CNTL/Z.
Switch (config-if) #switchport mode trunk Switch (config) #sw
te Switch (config) #int
Switch (config-if) fexit Switch (config) #interface gig
Switch (config) #interface gigabitEthernet 0/2 Switch (config) #interface gigabitEthernet 0/1
Switch (config-if)#switchport mode trunk Switch (config-if) #swit
Switch (config-if) fexit Switch (config-if)#switchport mo
Switch (config-if)#switchport mode trunk
Switch (config-if) #exit
Switchport trunk native vlan 100 Switen(configy af
Show
7
Port | Mode Encapsulation Status Native vlan switchtshow interfaces tr
Gigo/t on 802.14 trunking 200 Switch#show interfaces trunk
Gigd/2 on 802.14 trunking 100 Port Mode Encapsulation Status Native v
Port vlans allowed on trunk Gigo/2 on 802.1q trunking 100
Gig0/1 11-1005
Gigo/2 11008 Port Vlans allowed on trunk
Gigd/1 1-1005
Port Vlans allowed and active in management domain
Gig0/1 1, 10,20, 30,100 Port Vlans allowed and active in management domain
Gigd/2 1,10,20, 30,100 Gigd/1 1,10,20,30,100
Port Vlans in spanning tree forwarding state and not pruned Port Vlans in spanning tree forwarding state and not pr
Gigd/1 1,10,20, 30,100 Gigd/1 1,10,20,30,100
Gigd/2 1,10,20, 30,100
Task 5.
Show port-security address.
Interface fastEthernet 0/2
switchport mode access
switchport port-security
switchport port-security violation restrict
switchport port-security mac-address sticky
Show interfaces status
Interface fast...
Shut down
ExitCopy running-config startup-config


### Cisco projekt — strona 7

Powtarzamy w S71 i S2 dla: Fa 0/1, Fa 0/11, Fa 0/21.
Switch (config) #interface fastEthernet 0/1
Switeh (config-if) #aw
Switch (config-if) fawitchport m
Switch (config-if)fawitchport mode a
Switeh (config-if) baw
Switch (config-if) #awitchport por
Switch (config-if) fawitchport port-security
Switch (config-if) #switchport port-security vioa
Switch (config-if) #awitchport port-security vi
Switch (config-if) fexit
Switch (config) #exit
Switch’
SSYS-S-CONFIG _T: Configured from console by conscle
Port. Name Status vian Duplex Speed Type
Fa0/1 connected 10 auto. auto 10/100Baserx
Fa0/2 notconnect 10 auto auto 10/100BaseTX
Fa0/3 notconnect 10 auto auto 10/100BaseTX
Fa0/6 disabled 10 auto auto 10/100BaseTx Switch(config)#interface range fastEthernet
rors isabied 10 tke les levdeonssent 0/12-20
Pao/it connected. 20 auto "sue, 0/0 SWitch(config-if-range)#shutdown
Pa0/12 disabled 20 auto auto’ 10/100BaaerX
Fao/i4 disabled 20 Gute tute 10/100Baserx
Pa0/15 disabled 20 Gute tute 10/100Baserx
Pa0/16 disabled 20 Gute auto 10/100Baserx
mesa diesbied 20 tito ute 10/100nasenx Copy running-config startup-config
Task 6
Show ip route connected
Passive Interface(s): show ip protocols Routing Information Sources:
Serial interface
No shutdown
R3: gigabitethernet no shutdown
Router ospf 1
router-id 1.1.1.1
Network 111.111.111.111 0.0.0.255 area 0
Passive-interface


### Cisco projekt — strona 8

Show ip protocols
Show ip ospf interface
Show ip ospf neighbor
Copy running-config startup-config
Task 7
Show access-list
Router (config) #access-list 137 deny ip host 172.16.10.60 host 172.16.10.29
Router (config) #exit
Router#show access-lists
Extended IP access list 137
10 deny ip host 172.16.10.60 host 172.16.10.29
Access-list 2137 deny ip host 172.16.10.60 host 172.16.10.29
Task 8
Username Admin password ACDC1973
Enable password beatles1960
Service password-encryption
Banner motd #Only authorized personnel are allowed accessing this device#
Wr
Exit
Task 9
Ip domain-name Cyber.local
Crypto key generate rsa 1024
Ip ssh version 2
Line vty 0 4
Login local
Transport input SSH


### Cisco projekt — strona 9

Show ip ssh
Show ssh

Router>en

Password:

Password

Router#conf t

Enter configuration commands, one per line. End with CNTL/Z.

Router (config) #ip do

Router (config) #ip dom

Router (config) #ip domain-name Cyber. local

Router (config) #cry

Router (config) #crypto key generate rsa

% Please define a hostname other than Router

Router (config) thostn

Router (config) #hostname R1

Rl (config) #crypto key generate rsa

& You already have RSA keys defined named R1.Cyber.com .

% Do you really want to replace them? [yes/no]: yes

The name for the keys will be: R1.Cyber.local

Choose the size of the key modulus in the range of 360 to 4096 for your
General Purpose Keys. Choosing a key modulus greater than 512 may take
a few minutes

How many bits in the modulus [512]: 1024

% Generating 1024 bit RSA keys, keys will be non-exportable... [OK]

Rl (config) #ip ssh version 2

*Mar 2 11:36:58.388: $SSH-5-ENABLED: SSH 1.99 has been enabled

Rl (config) #line vty 0 4

Rl (config-line)#login local

Rl (config-line)#transport input ssh

Rl (config-line) #exit

Rl#show ip ssh

SSH Enabled - version 2.0

Authentication timeout: 120 secs; Authentication retries: 3

R1¢

C:\>ssh “1 Adin 172.16.10.1

Password

i Login invalid

Password:

only authorized personnel are allowed accessing this device!

banner motd

231

R3# show ip ssh

SSH Enabled - version 2.0

Authentication timeout: 120 secs; Authentication retries: 3

R3#show ssh

Connection Version Mode Encryption Hmac State

Username

0 1.99 IN aes128-cbe hmac-shal Session Started

Admin

0 1.99 OUT aes128-cbce hmac-shal Session Started

Admin

%No SSHvl server connections running.

R3#
