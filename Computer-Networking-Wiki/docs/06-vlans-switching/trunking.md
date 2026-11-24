# 802.1Q trunking and DTP

[← Indeks wiki](../index.md)

> **Źródło główne:** Computer Networking Textbook.pdf, s. 163–167. Treść została uporządkowana tematycznie; pełny ekstrakt źródłowy znajduje się w `_source-archive/`.


## Materiał kanoniczny

The Trunk interface is designed to transmit multiple VLAN traffic sessions over the same
connection, and to a remote device, such as a switch or router.
This is done by tagging frames with the source VLAN, ensuring that the Trunk link
forwards the VLAN frames to the same VLAN on another switch.
Common Trunking Protocols
The two most common trunking protocols are ISL and 802.1q.
ISL - ISL (Inter-Switch Link) was developed by Cisco and requires a license to create
Trunking groups of ISLs between adjacent switches.
802.1q - 802.1q was developed by IEEE. It is the default protocol in most switches
today. The same trunk protocol must be used on both ends of the trunk link
(encapsulation).
DTP
DTP is a protocol developed by Cisco to create Trunk links automatically. It operates by
default on all Cisco switches, but can be turned off for security purposes.
DTP automatically “negotiates” for packets between interconnected switches. When
two switches reach an “agreement”, the trunk is established.
DTP can run in one of two dynamic port modes: dynamic auto or dynamic desirable.
Dynamic Auto - This mode, which is the default for each port, is passive and does not
negotiate. Instead, it waits until an explicit request is received from the other side.
Dynamic Desirable - This mode allows DTP negotiation packets to be sent to the switch
on the other side of the connection.
When configuring the interface on a device, each DTP mode enabled on the device will
result in different operational behavior.

DTP Mode Configuration

The example below shows the configuration of DTP modes on the interconnected

interfaces of the switches. The command used to set the configuration is switchport

mode dynamic <mode>.

Remember: Dynamic Auto is the default mode.

To display the interface mode, use show interfaces switchport.
S1(config)#interface gigabitEthernet @/1
S1(config-if)#switchport mode dynamic auto
S1(config-if)#exit
S1(config)#interface gigabitEthernet @/1
S1(config-if)#switchport mode dynamic desirable
S1(config-if)#exit

Disabling DTP

Since using DTP can make the switch vulnerable to a VLAN attack, it is recommended to

disable DTP on a port connected to an end device. This is done using the command

switchport nonegotiate.

Configuring the port in access mode is not enough, and nonegotiate is required. To

display the interface mode, use show interfaces switchport.
S1(config)#interface fastEthernet @/1
S1(config-if)#switchport mode access
S1(config-if)#switchport nonegotiate
S1(config-if)#exit
S1#show interfaces switchport
Name: FaQ/1
Switchport: Enabled
Administrative Mode: static access
Operational Mode: down
Administrative Trunking Encapsulation: dotigq
Operational Trunking Encapsulation: native
Negotiation of Trunking: Off

Dynamic Trunking Protocol Mode Behavior
The following table lists the results of each mode combination on opposite ends of the
connection.
Dynamic Auto Access Trunk Trunk Access
Dynamic Desirable — Trunk Trunk Trunk Trunk
Trunk Trunk Trunk Trunk (Etta _
Connectivity
Access Access Access pimited we Access
Connectivity
Configuring Trunk Links
The switchport mode trunk command creates IEEE 802.1q trunk links.
Use this command to create a static trunk connection, without using the DTP protocol.
Command:
switchport mode trunk
Example:
Switch(config)#interface gigabitEthernet 0/1
Switch(config-if)#switchport mode trunk
Switch(config-if)#exit
After the switchport creates a trunk link, by default all VLANs are allowed to pass
throught the link, but a set of allowed VLANs can be specified.
Command:
switchport access trunk allowed vlan vlan-id

Example:
Switch(config)#interface gigabitEthernet 0/1
Switch(config-if)#switchport mode trunk
Switch(config-if)#switchport mode trunk allow vlan 10
Switch(config-if)#exit
Native VLANs
Native VLANs process untagged frames when they reach switch trunk ports.
The default Native VLAN is VLAN 1.
A best practice regarding Native VLANs is to assign roles to unused VLANs, such as VLAN
100, for security purposes.
The same Native VLAN must be used on both ends of the trunk link.
Important Native VLAN Points
Best Practice - A best practice regarding Native VLANs is to re-assign them to non-
default VLANs, such as VLAN 200, for security purposes. Doing so can, for example,
mitigate Double Tagging attacks.
Identical Native VLAN - The same Native VLAN must be used on both ends of the trunk
link. If not, untagged frames will not be delivered correctly, and the switch’s OS will
send continuous warning messages to the user, in the form of: “%CDP-4-
NATIVE_VLAN_MISMATCH: Native VLAN mismatch discovered on GigabitEthernet0/1
(200), with $2 GigabitEthernetO/1 (1).”
Why are Native VLANs Important?
Without Native VLANs, sending and receiving updates for protocols such as CDP, VTP,
DTP, and STP between interconnected switches would not be possible, since trunk ports
drop untagged frames.

Changing Native VLANs
The Native VLAN should be changed because using the default Native VLAN leaves the
switch open to an attack called Double Tagging.
Command:
Switchport trunk native vlan vlan-id
Example:
Switch(config)#interface gigabitEthernet 0/1
Switch(config-if)#switchport trunk native vlan 100
Switch(config-if)#exit

## Powiązane laboratoria

- [NET-09-LS1](../labs/net-09-ls1.md)


## Uzupełnienia z notatek Riseup / zajęć

<details>
<summary>Pokaż notatki prowadzącego, dodatkowe komendy i linki powiązane z tym tematem</summary>

S1#conf t
S1(config)#interface range gigabitEthernet 0/1-2
S1(config-if-range)#switchport mode trunk
S1(config-if-range)#
%LINEPROTO-5-UPDOWN: Line protocol on Interface GigabitEthernet0/1, changed state to
down

---

S1(config-if-range)#exit

do show interfaces switchport
S2>en
S2#conf t
S2(config)#interface gigabitEthernet 0/1
S2(config-if)#switchport mode trunk
S2(config-if)#exit
S2(config)#vlan 30
S2(config-vlan)#name Native
S2(config-vlan)#exit
S2(config)#interface gigabitEthernet 0/1
S2(config-if)#switchport trunk native vlan 30
S2(config-if)#exit
S1#copy running-config startup-config
S2#copy running-config startup-config

</details>

## Powiązane tematy

- [VLANs](vlans.md)
- [Inter-VLAN routing and router-on-a-stick](inter-vlan-routing.md)

## Źródła w zestawie

- `Computer Networking Textbook.pdf` — strony 163–167.
- `Computer Networking.pdf` — prezentacja kursowa; odpowiadający rozdział zachowany w `_source-archive/02-Course-Slides.md`.
- `Padriseup Computer Networking.pdf` — uzupełnienia i materiały dodatkowe, jeśli występowały dla tego tematu.
