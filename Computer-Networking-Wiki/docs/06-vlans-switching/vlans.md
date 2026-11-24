# VLANs

[← Indeks wiki](../index.md)

> **Źródło główne:** Computer Networking Textbook.pdf, s. 158–162. Treść została uporządkowana tematycznie; pełny ekstrakt źródłowy znajduje się w `_source-archive/`.


## Materiał kanoniczny

VLAN is a Layer 2 feature that represents a broadcast domain, enabling network
administrators to create several virtual LANs on a single switch.
The LANs are logical divisions (not physical divisions) between local networks.
Multiple ports are configured on the switch and associated with a VLAN, creating a
logical barrier between end components connected to the switch.
Benefits
Security - Separating systems that store sensitive data from the rest of the network
decreases chances that people will gain access to information they are not authorized
to view.
Improvement - Reducing the size of broadcast domains increases the performance and
minimizes unnecessary traffic on the network. VLANs also reduce network cost.
Simplicity - VLANs simplify network management operations and maintenance.
VLAN ID
When traffic passes through a network, it has to be identified to keep it separate from
other traffic. A unique ID identifies a VLAN in the network.
There is a complete separation between virtual networks, whereby users on VLAN 10
cannot access data on VLAN 20.
The valid ID range for VLANs is 1 to 1005. There is also an additional extended range of
valid VLAN IDs from 1006 to 4094.
VLAN Types
Default VLAN - VLANs 1 and 1002-1005 are reserved and added automatically during
device installation. These IDs cannot be removed.
Data VLAN - VLANs 2-1001 are commonly used by users for data exchanges. Their main
function is to tag data traffic with an identifier.

Voice VLAN - This VLAN is designed for VoIP (Voice over IP) networks.
Management VLAN - Interface VLAN 1 is a management VLAN that uses a Layer 3
interface called SVI. The management VLAN is also used for remote connection via
protocols such as Telnet and SSH.
Native VLAN - Native VLANs forward untagged traffic, such as DTP and CDP.
Default VLAN Settings
The command show vlan brief shows that the switch is already pre-configured with
VLAN 1, and all ports are associated with it by default. Additional VLANs are available in
the switch configuration. They are reserved and known as Default VLANs.
S1#show vlan brief
VLAN Name Status Ports
1 default active FaQ/1, Fa@/2, FaQ/3, Fad/4
FaQ/5, Fa@/6, FaQ/7, Fad/8
Fa@/9, FaQ/10, Fa@/11, FaQ/12
FaQ/13, Fa@/14, FaQ/15, FaQ/16
Fa@/17, Fa@/18, FaQ/19, Fae/20
Fa@/21, Fa@/22, FaQ/23, Fa/24
Gig®/1, Gigd/2
1002 fddi-default active
1003 token-ring-default active
1004 fddinet-default active
1005 trnet-default active
VLAN Configuration
VLANs should be assigned appropriate names upon creation. The valid ID range for
sending data is 1-1005.
Command:
vian vlan-id | name name
Example:
Switch(config)#vlan 10
Switch(config-vlan)#name HR
Switch(config-vlan)#exit

Switchport Modes
The switch interface operates in one of two modes, Access or Trunk, via the switchport
command.
Access - The Access port is used when connecting end devices. For example, when
connecting a PC to a switch, the interface must be configured as an Access port.
Unlike Trunk ports, Access ports only transport traffic to and from the VLAN they are
assigned to.
Trunk - Trunk ports carry traffic for different VLANs and devices. The port sets unique
identifier tags on the frame, using either the 802.1Q or ISL encapsulation protocols. This
ensures that each frame is directed to its intended VLAN.
Switchport Access Mode
Access ports only carry traffic on the VLAN to which they belong, and Access mode
should only be defined on ports connected to end devices, such as PCs.
As a security-related best practice, it is highly recommended to enable Access mode for
a port, before assigning it to a VLAN.
The switchport command is used to configure a port to operate in Access mode.
The assignment of users (end devices, such as PCs) to different VLANs is done by
matching the interconnected interface to the appropriate VLAN.
. ‘ ¢
a © ~ | Assigning multiple ports to a VLAN simultaneously can be done using the
range command.
=
Command:
Switch mode access | switchport access vlan vlan-id

Example:
Switch(config)#interface fastEthernet 0/1
Switch(config-if)#switchport mode access
Switch(config-if)#switchport access vlan 10
Switch(config-if)#exit
Switch(config)#interface range fastEthernet @/1-5
Switch(config-if)#switchport mode access
Switch(config-if)#switchport access vlan 10
Verifying VLAN Configuration
By running the show vlan brief command, it is easy to spot the two new VLANs and the
interfaces assigned to them. To display the interface mode, use show interfaces
switchport.
Sl#show vlan brief
VLAN Name Status Ports
all default active Fa@/5, Fa@/6, Fa@/7, Fa0/8
Fa@/9, Fa@/10, FaQ/11, FaQ/12
FaQ@/13, FaQ/14, Fa@/15, Fad/16
FaQ@/17, FaQ/18, Fa@/19, Fae/20
FaQ@/21, FaQ/22, Fa@/23, Fa0/24
Gig®/1, Gigd/2
100 class_A active Fa@/1, Fa0/2
200 class_B active Fa@/3, Fa0/4
1002 fddi-default active
1003 token-ring-default active
1004 fddinet-default active
1085 trnet-default active
Voice VLAN Configuration
The following commands are used to configure an interface to use a VLAN as a Voice
VLAN.
Commands:
Switch mode access | switchport voice vlan vlan-id

Example:
Switch(config)#interface fastEthernet @/1
Switch(config-if)#switchport mode access
Switch(config-if)#switchport access vlan 10
Switch(config-if)#switchport voice vlan 101 //assume its pre-
configured VLAN
Switch(config-if)#exit

## Powiązane laboratoria

- [NET-09-LS1](../labs/net-09-ls1.md)


## Uzupełnienia z notatek Riseup / zajęć

<details>
<summary>Pokaż notatki prowadzącego, dodatkowe komendy i linki powiązane z tym tematem</summary>

https://access.redhat.com/sites/default/files/attachments/rh_ip_command_cheatsheet_1214_
jcs_print.pdf
https://www.asus.com/pl/networking-iot-servers/whole-home-mesh-wifi-system/zenwifi-wifi-s
ystems/asus-zenwifi-ax-hybrid-xp4/

19.08.2023

---

L1.rar
S2#conf t
S2(config)#vlan 10
S2(config-vlan)#name Workstation
S2(config-vlan)#exit
S2(config)#vlan 20
S2(config-vlan)#name Servers
S2(config-vlan)#exit
S2(config)#do show vlan brief

F0/1-4 VLAN10
F0/5-6 VLAN20
S2(config)#interface range fastEthernet 0/1-4
S2(config-if-range)#switchport mode access
S2(config-if-range)#switchport access vlan 10
S2(config-if-range)#exit
S2(config)#interface range fastEthernet 0/5-6
S2(config-if-range)#switchport mode access
S2(config-if-range)#switchport access vlan 20
S2(config-if-range)#exit
S2(config)#do show vlan brief
Polaczenia fizyczne dla switcha S1
F0/1-2 VLAN10 (stacje robocze)
F0/3 VLAN20 (serwer)
S1>enable
S1#conf t
S1(config)#vlan 10
S1(config-vlan)#name Workstation
S1(config-vlan)#exit
S1(config)#vlan 20
S1(config-vlan)#name Servers
S1(config-vlan)#exit
S1(config)#interface range fastEthernet 0/1-2
S1(config-if-range)#switchport mode access
S1(config-if-range)#switchport access vlan 10
S1(config-if-range)#exit

S1(config)#interface fastEthernet 0/3
S1(config-if)#switchport mode access
S1(config-if)#switchport access vlan 20
S1(config-if)#exit
S1(config)#do show vlan brief
10.0.0.0 255.255.255.0
10.0.0.254
192.168.0.0 255.255.255.0 - Serwery

</details>

## Powiązane tematy

- [802.1Q trunking and DTP](trunking.md)
- [Inter-VLAN routing and router-on-a-stick](inter-vlan-routing.md)
- [Switch fundamentals](../03-cisco-ios/switch-fundamentals.md)

## Źródła w zestawie

- `Computer Networking Textbook.pdf` — strony 158–162.
- `Computer Networking.pdf` — prezentacja kursowa; odpowiadający rozdział zachowany w `_source-archive/02-Course-Slides.md`.
- `Padriseup Computer Networking.pdf` — uzupełnienia i materiały dodatkowe, jeśli występowały dla tego tematu.
