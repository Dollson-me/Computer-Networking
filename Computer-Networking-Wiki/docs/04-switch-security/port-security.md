# Port security

[← Indeks wiki](../index.md)

> **Źródło główne:** Computer Networking Textbook.pdf, s. 81–85. Treść została uporządkowana tematycznie; pełny ekstrakt źródłowy znajduje się w `_source-archive/`.


## Materiał kanoniczny

The Port Security feature is used to restrict input to an interface by limiting MAC
addresses of workstations that are allowed to access a specific port.
When secure MAC addresses are assigned to a port, the port will not forward packets
with source addresses outside the defined group.
By default, port security is not defined on switches and requires configuration.
Switched Environment Risks
MAC Spoofing
MAC spoofing is when attackers change their own physical PC address to conceal their
true identity and pose as someone else. For example, an attacker may spoof a MAC
address with a legitimate address to bypass an access control mechanism, such as port
security.
CAM Table Overflow
CAM Table Overflow is an attack that targets a switch’s MAC table. The idea is to flood
the table with a large number of fake addresses. When the list of addresses exceeds the
maximum size of the table, the switch will initiate its fallback mode and begin to act as
a hub, meaning every frame will be forwarded to every host on the network.
Violation Modes
The port security feature includes three protection modes to handle incidents in which
it receives an Ethernet frame with an unauthorized MAC address.
Shutdown - This is the default violation mode. When a violation occurs, the port will be
shut down, and the violation will be logged automatically. The port must then be reset
manually to become operational again.

Restrict - In case of a violation, Ethernet frames with unauthorized source MAC
addresses are dropped. The switch provides notification of security violations and keeps
count of the number of violations.
Protect - In case of a violation, Ethernet frames with unauthorized source MAC
addresses are dropped. In this violation mode, the switch does not provide notification
regarding the event.
Address Learning — Manual vs. Sticky
MAC address learning can be performed in one of two ways: Manual or Sticky.
Manual - The manual method requires a static configuration of each allowed MAC
address and its assignment to an interface. This is the most secure method, but it is very
time consuming and open to faulty configuration.
Sticky - In the sticky method, allowed MAC addresses are learned dynamically and are
limited to the maximum number configured for the interface. The switch learns the
source address of the first few devices associated with the interface, providing a fast
and scalable method of operation.
Max and Err-Disabled
Max Allowed MAC Addresses
Although the number of default MAC addresses allowed in Port Security is one, the
number can be changed within the range of 1 to 3072.
Err-Disabled
When a switch port is in Err-disabled mode, the port may have been disabled
automatically by the switch operating system, due to port security shutdown mode
violation.
To determine if Err-disabled was turned off for a port, run the command:
show interfaces [interface] status

Example:

Switch# show interfaces fastEthernet 0/1 status

Port Status

Fa@/1 err-disabled

rage oo

Common Reasons for err-disable

Err-disabled may be triggered due to reasons other than Port Security, such as:

e Duplex Mismatch - This state occurs when two parties, set for point-to-point
communication, are configured to use different duplex modes.

e Bad NIC - A faulty network interface card with software problems or hardware
problems may trigger the Err-disabled state.

e Broadcast Storm - When there is a broadcast volume too large for processing in the
broadcast domain, the switches may be overwhelmed and trigger err-disabled
mode on its ports.

Port Security Requirements

Access Mode
Access ports are responsible for traffic flow.
Access mode should only be defined on ports connected to endpoint devices, such as

PCs.

You can configure port security on interfaces that you configured as access ports with
access mode activated.

Enable Port Security

Enabling port security is done in the interface configuration mode, which is set using

interface [interface-id]. Then, Access mode needs to be set with switchport mode

access.

Note: For port security to operate correctly, the interface must be configured as an

Access port.
Finally, Port Security can be enabled on the interface using the command:
switchport port-security

Commands:
switchport mode access
switchport port-security
Example:
Switch(config)# interface fastEthernet @/1
Switch(config-if)# switchport mode access
Switch(config-if)# switchport port-security
Switch(config-if)#
Port Security Configuration
Port Security is configured by setting up each component individually using the same
structure.
Violation defines the type of violation rule to be applied to the port.
The commands mac-address and maximum define sticky learning, up to a maximum of
five addresses.
Command:
switchport port-security [configuration] [value]
Example:
Switch(config)# interface fastEthernet 0/1
Switch(config-if)# switchport mode access
Switch(config-if)# switchport port-security
2 A A A KK KK Ke 2 ee 2 2 2 2 2 2K 2K 2K 2K 2K 2 2K 2K 2 2K 2 2K 2 2K 2K 2K OK OK OK OK OK OK OK OK OK OK OK KKK KK KK
Switch(config-if)# switchport port-security violation restrict
Switch(config-if)# switchport port-security mac-address sticky
Switch(config-if)# switchport port-security maximum 5

Port Security Show Commands
Presenting the authorized MAC addresses associated with a port and the type (sticky or
manually) is done with the command show port-security address.
If only an overview is needed, show port-security can be run for a quick overview of the
configuration.
To view a specific interface, the command show port-security interface [interface]
should be used, since it provides more information.
Example:
Switch# show port-security
Secure Port MaxSecureAddr CurrentAddr SecurityViolation Security Action
(Count) (Count) (Count)
Fae@/1 5 a (7) Restrict
Fae/2 1 (2) (2) Shutdown
Switch# show port-security address
Secure Mac Address Table
Vlan Mac Address Type Ports Remaining Age
(mins)
a @002.1798.DAC6 SecureSticky FastEthernet0/1 -
1 Q090.2172.8736 DynamicConfigured FastEthernet0/2 -
Total Addresses in System (excluding one mac per port) : @
Max Addresses limit in System (excluding one mac per port) : 1024
é Lab — Configure and Verify Port Security
=, Implement Port Security on a switch, practice using Port Security options,
= | and learn how to verify settings.
Perform the instructions in lab document Net-04-L1.

## Powiązane laboratoria

- [NET-04-LS1](../labs/net-04-ls1.md)


## Uzupełnienia z notatek Riseup / zajęć

<details>
<summary>Pokaż notatki prowadzącego, dodatkowe komendy i linki powiązane z tym tematem</summary>

interface range fastEthernet 0/1-4
switchport mode access
switchport port-security
exit
S1(config)#interface fastEthernet 0/1
S1(config-if)#switchport port-security mac-address 00D0.9793.87C4
S1(config-if)#exit
S1(config)#interface fastEthernet 0/2
S1(config-if)#switchport port-security mac-address 0009.7C96.0271
S1(config-if)#exit
S1(config)#interface fastEthernet 0/3
S1(config-if)#switchport port-security mac-address sticky
S1(config-if)#exit
S1(config)#interface fastEthernet 0/4
S1(config-if)#switchport port-security mac-address sticky
S1(config-if)#exit

S1(config)#interface fastEthernet 0/1
S1(config-if)#switchport port-security violation shutdown
S1(config-if)#exit
S1(config)#interface range fastEthernet 0/2-3
S1(config-if-range)#switchport port-security violation restrict
S1(config-if-range)#exit
S1(config)#interface range fastEthernet 0/4
S1(config-if-range)#switchport port-security violation protect
S1(config-if-range)#exit
S1(config)#interface range fastEthernet 0/5-24, gigabitEthernet 0/1-2
S1(config-if-range)#shutdown
S1(config-if-range)#exit
S1>enable
S1#show port-security
S1#show port-security address
S1#show port-security interface fastEthernet 0/4
S1#show running-config
interface FastEthernet0/3
switchport mode access
switchport port-security
switchport port-security maximum 2
switchport port-security mac-address sticky
switchport port-security violation restrict
switchport port-security mac-address sticky 0004.9A8B.2832
switchport port-security mac-address sticky 0090.0C26.3CEE
S1#show port-security interface fastEthernet 0/4

Switch>enable
Switch#conf t

</details>

## Powiązane tematy

- [Switch fundamentals](../03-cisco-ios/switch-fundamentals.md)
- [Remote access, VTY, SVI and SSH](ssh-svi-vty.md)

## Źródła w zestawie

- `Computer Networking Textbook.pdf` — strony 81–85.
- `Computer Networking.pdf` — prezentacja kursowa; odpowiadający rozdział zachowany w `_source-archive/02-Course-Slides.md`.
- `Padriseup Computer Networking.pdf` — uzupełnienia i materiały dodatkowe, jeśli występowały dla tego tematu.
