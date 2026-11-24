# CDP and LLDP

[← Indeks wiki](../index.md)

> **Źródło główne:** Computer Networking Textbook.pdf, s. 174–178. Treść została uporządkowana tematycznie; pełny ekstrakt źródłowy znajduje się w `_source-archive/`.


## Materiał kanoniczny

Cisco Discovery Protocol (CDP) is a Layer 2 Cisco proprietary protocol enabled by
default on all Cisco devices. Its purpose is similar to that of NDP.
CDP can be disabled on specific devices or interfaces, for security purposes.
CDP Attributes
Eavesdropping - Since CDP does not encrypt transmitted data, it is vulnerable to
reconnaissance type attacks (such as sniffing) that, for example, allow an attacker to
map the victim's network.
Information Gathering - CDP gathers information on the local device and periodically
sends it to all directly connected devices.
Advertisements - CDP advertisements are special packets that reveal device details to
neighbors also running CDP.
When advertisements are received, they are stored in the neighbor's table.
Advertised Packets
CDP includes the following data in advertised packets:

* Type of device (router, switch)

* Device name

* Interconnected interfaces

* 10S version

* Next-hop IP

* Connection's duplex mode (full, half)
Mismatch Error Detection
CDP includes a unique feature that can detect a protocol-connection mismatch. When
such a mismatch is detected, CDP notifies the network administrator by recording the
incident in a log.
Examples of mismatch types include:
* Native VLAN mismatch
* Duplex mismatch

Intervals
Advertisement messages also include the following intervals, which can be modified.
Advertisement packets are sent every 60 seconds to all directly-connected devices.
When a device does not receive Hello packets from its neighbor for 180 seconds, it will
consider the neighbor "dead," and remove it from its CDP neighbor table.
CDP Commands
Because CDP is not secure or encrypted, it is easy to eavesdrop. If necessary, the
protocol can be turned off entirely on the device or on selected interfaces.
It is recommended to enable CDP only for port interconnection with other network
devices.
cdp run
Enable/disable CDP on the device.
Command:
cdp run | no cdp run

Examples:

Switch(config)#cdp run

Switch(config)#no cdp run

cdp enable

Enable/disable CDP ona specific interface.
Command:

cdp enable | no cdp enable

Examples:

Switch(config)#interface fastethernet 0/1

Switch(config-if)#cdp enable

Switch(config)#interface fastethernet 0/1

Switch(config-if)#no cdp enable
Show cdp neighbors
The show cdp neighbors command displays all connected devices that CDP can
communicate with via its advertisement messages. It also displays additional
information, such as IP address and IOS version.
Topology example:

——s0-2
_ Q ——

= Switch? ~ —_—
2960-247 ai ao 2960-24TT
Senda ee a Switch3

a _
2960-24TT
Switch4

Example:
Switchl#show cdp neighbors
Capability Codes: R - Router, T - Trans Bridge, B - Source Route Bridge
S - Switch, H - Host, I - IGMP, r - Repeater, P - Phone
Device ID Local Intrfce Holdtme Capability Platform Port ID
Switch Fas 0/2 101 S 2960 Fas @/1
Switch Fas 0/1 104 S 2960 Fas @/1
Switch2 Fas @/2 161 S 2960 Fas 9/1
Switch4 Fas @/1 164 S 2960 Fas 9/1

LLDP
LLDP (Link Layer Discovery Protocol) is a Neighbor Discovery Protocol similar to CDP
that was developed by the IEEE.
LLDP is an industry-standard protocol, meaning it is not proprietary and can operate on
any network device.
Although LLDP is not enabled by default on Cisco devices, it is fully supported.
Default LLDP messages also include intervals that can be modified as necessary.
LLDP advertisement packets are sent to LLDP neighbors at periodic intervals, which is 60
seconds by default. You can increase or decrease the interval as necessary. The default
interval recommended by IEEE is 30 seconds, but any value between 5 and 300 seconds
can be specified.
When a device does not receive Hello packets from its neighbor for 120 seconds, it will
consider the neighbor "dead", and remove it from its LLDP neighbor table.
LLDP Commands
IIdp run
Enable/disable LLDP on the device.
Command:
IIdp run | no Ildp run
Examples:
Switch(config)#lldp run
Switch(config)#no lldp run

Show Ildp neighbors
The show Ildp neighbors command displays all connected LLDP devices that LLDP was
able to communicate with via its advertisement messages.
Topology Example:
_ ee
—_—_— 2960-24TT _—— .

— a Switch2 = 7 OU
2960-24TT 2a, ao 2960-24TT
Switch1 ~~ =- ce

~ _—
“te an
—__
2960-24TT
Switch
Code Example:
Switchl#show lldp neighbors
Capability codes:
(R) Router, (B) Bridge, (T) Telephone, (C) DOCSIS Cable Device
(W) WLAN Access Point, (P) Repeater, (S) Station, (0) Other
Device ID Local Intf Hold-time Capability Port ID
Switch2 Fa0/2 120 B Fa@/1
Switch4 Fa@/1 120 B Fa@/1

## Powiązane laboratoria

- Brak bezpośrednio przypisanego laboratorium w zestawie.

## Powiązane tematy

- [Troubleshooting methodology](troubleshooting.md)
- [Syslog](syslog.md)

## Źródła w zestawie

- `Computer Networking Textbook.pdf` — strony 174–178.
- `Computer Networking.pdf` — prezentacja kursowa; odpowiadający rozdział zachowany w `_source-archive/02-Course-Slides.md`.
- `Padriseup Computer Networking.pdf` — uzupełnienia i materiały dodatkowe, jeśli występowały dla tego tematu.
