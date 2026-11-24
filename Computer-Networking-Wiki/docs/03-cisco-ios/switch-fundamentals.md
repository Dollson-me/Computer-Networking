# Switch fundamentals

[← Indeks wiki](../index.md)

> **Źródło główne:** Computer Networking Textbook.pdf, s. 62–65. Treść została uporządkowana tematycznie; pełny ekstrakt źródłowy znajduje się w `_source-archive/`.


## Materiał kanoniczny

Switches are smart Layer 2 devices with many ports designed to forward frames from
source to destination, according to specific MAC addresses in the frame (Data-Link
Layer). They include multiple technologies, providing various capabilities.
Switches were developed to forward frames in accordance with their destination
addresses and MAC tables (CAM tables), using a MAC learning process known as
forwarding decision.
MAC Tables
The following command is used to display the MAC address table is in Cisco devices:
show mac-address-table
MAC address tables include the following columns:
- VLAN
- MAC address
- Dynamic or Static
- Associated physical ports
DYNAMIC is when a frame with a source MAC arrives at a switch, and the table is
updated with the device MAC address for that port.
STATIC indicates a manually configured MAC address on a switch.
MAC Table Example:
Switch#show mac-address-table
Mac Address Table
Vlan Mac Address Type Ports
1 0001.97d7.45c3 DYNAMIC Fa@/5
1 0004.9a3d.bbc6 DYNAMIC FaQ/4
1 00@c.8500.13bb DYNAMIC Fa@/3
1 00@d@.978c.5698 DYNAMIC Fa@/2

Switching Methods
Another important thing about switches is that they have different methods of
receiving and transmitting frames on the LAN.
The following switching methods are used:

= Store-and-Forward

= Cut-through

= Fragment-free
Store-and-Forward
A switch using the Store-and-Forward method buffers the entire frame upon receipt.
This enables the switch to support various port speeds. For example, a frame received
ona 100 Mb/s ingress port can be transmitted via a 1 Gb/s egress port.
Another advantage of this method is error checking, which can be done once the entire
frame is buffered. The switch can easily detect frame errors using the FCS field.
Although Store-and-Forward is relatively slow, it does provide error checking and
support for different speeds across multiple ports.
The buffer is a memory space used for storing some data before performing an action
on it. Frame buffering is the process of storing a frame in memory temporarily before it
is moved to the next destination.
Cut-Through
Cut-through switching is a much faster method than Store-and-Forward. In this method,
only the first 6 bytes of the incoming frame are buffered, meaning the switch only
regards the destination MAC address of the frame.
The switch forwards the frame immediately, even before the entire frame is received,
and no error checking is done.
Note: Modern switches can buffer up to 14 bytes of the beginning of a frame, before
deciding what to do with it.
Although the advantage of Cut-through is its speed, a significant disadvantage is that
some frames that reach the destination host may be corrupted due to lack of error
checking.

Fragment-Free
Fragment-free is a more advanced method of switching.
This method buffers the first 64 bytes of the frame, including MAC address data and the
frame’s payload. The technique provides faster switching than Store-and-Forward while
also performing partial error checking to make sure there is no fragmentation on the
first 64 bytes of the frame.
Fragment-free is therefore a better choice for switching since it is faster than Store-and-
Forward and provides partial error checking, unlike Cut-through.
Communication
Half Duplex - A connection for which the communication is restricted to exchanging
data in one direction at a time. For example, a walkie-talkie is a half-duplex device
because only one person can talk at a time.
Full Duplex - Full duplex means that data can be transmitted in both directions, ona
signal carrier, at the same time.
For example, a telephone is a full-duplex device because both users can talk at once.
Half Duplex
SSS
s) s)
re Full Duplex re
EEE
—> Ss

Port Speed

Switch ports are typically able to transfer traffic at speeds of 1OMbps, 100Mbps, or

1000Mbps.

The default is for the switch port to auto-configure its speed based on signaling

between the port and the connected device.

There are switches that can transfer traffic at 10 Gbps, or even 40 Gbps.

Auto-Negotiation

Auto-negotiation tells connected devices to announce their capabilities, and then,

based on the settings of the interconnected device at the other end, chooses the

optimal speed and duplex mode.

If one of the devices is configured with a different mode, a duplex mismatch will occur.

## Powiązane laboratoria

- Brak bezpośrednio przypisanego laboratorium w zestawie.

## Powiązane tematy

- [Cisco IOS and CLI](cisco-ios.md)
- [Port security](../04-switch-security/port-security.md)
- [VLANs](../06-vlans-switching/vlans.md)

## Źródła w zestawie

- `Computer Networking Textbook.pdf` — strony 62–65.
- `Computer Networking.pdf` — prezentacja kursowa; odpowiadający rozdział zachowany w `_source-archive/02-Course-Slides.md`.
- `Padriseup Computer Networking.pdf` — uzupełnienia i materiały dodatkowe, jeśli występowały dla tego tematu.
