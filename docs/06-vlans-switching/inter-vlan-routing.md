# Inter-VLAN routing and router-on-a-stick

[← Indeks wiki](../index.md)

> **Źródło główne:** Computer Networking Textbook.pdf, s. 168–170. Treść została uporządkowana tematycznie; pełny ekstrakt źródłowy znajduje się w `_source-archive/`.


## Materiał kanoniczny

Although VLANs are logical segments, they still operate within the framework of a
network, which means they are also broadcast domains. Switches (which generally
Operate at Layer 2) cannot move traffic across different VLANs or broadcast domains.
Routing data among different VLANs requires a Layer 3 device (such as a router), which
encapsulates and decapsulates the frames.
Router-On-A-Stick
The most common technique for Inter-VLAN Routing is called Router-On-A-Stick. This
method is effective because it requires only a single physical connection between the
switch and the router, avoiding the need for additional components and costs.
Sub-Interface
Multiple IP addresses - Multiple IP addresses are possible because a router’s single
physical interface is segmented into multiple logical interfaces, called sub-interfaces.
Logical Interface - Each sub-interface is configured with a unique IP address and subnet
mask. Every sub-interface represents a default gateway for a specific VLAN.
Simple rule: The number of VLANs dictates the number of sub-interfaces.

Ri(config)#interface gigabitEthernet 0/0.1

R1(config)#interface gigabitEthernet 0/0.2

R1(config)#interface gigabitEthernet 0/0.3

The Switch Side
On the switch side, set the logical interface connected to the router to trunk mode
using the command switchport mode trunk. This enables VLAN tagging towards the
switch.
S1(config)#interface gigabitEthernet 0/1
S1(config-if)#switchport mode trunk
S1(config-if)#exit
Inter-VLAN Routing Configuration
On the router side:
1. Enter the physical interface and enable it.
2. Create a sub-interface.
3. Configure interface encapsulation on 802.1q, and assign the appropriate VLAN ID.
4. Configure the VLAN’s corresponding IP address and mask (default gateway).
5. Repeat this process for every VLAN.
R1(config)#interface gigabitEthernet 0/0
R1(config-if)#
R1(config-if)#exit
R1(config)#interface gigabitEthernet 0/0.1
R1(config-subif)#encapsulation dot1Q 100
R1(config-subif)#ip address
R1(config-subif)#exit
R1(config)#interface gigabitEthernet 0/0.2
R1(config-subif)#encapsulation dot1Q 200
R1(config-subif)#ip address
R1(config-subif)#exit

Verify Configuration
Use show ip interface brief to display the interface settings and mode. The show
running-config command shows additional details, such as the interface and its VLAN
ID.
Rl#show ip interface brief
Interface IP-Address OK? Method Status Protocol
GigabitEthernet@/1 unassigned YES unset administratively down down
Vlan1 unassigned YES unset administratively down down
é Lab Assignment — Configuring VLANs and Trunks
—=J | Learn how to configure VLANs and trunks.
m=:
Perform the instructions in lab document NET-09-L1.

## Powiązane laboratoria

- [NET-09-LS1](../labs/net-09-ls1.md)

## Powiązane tematy

- [VLANs](vlans.md)
- [802.1Q trunking and DTP](trunking.md)
- [Routers and interfaces](../05-addressing-routing/routers-interfaces.md)

## Źródła w zestawie

- `Computer Networking Textbook.pdf` — strony 168–170.
- `Computer Networking.pdf` — prezentacja kursowa; odpowiadający rozdział zachowany w `_source-archive/02-Course-Slides.md`.
- `Padriseup Computer Networking.pdf` — uzupełnienia i materiały dodatkowe, jeśli występowały dla tego tematu.
