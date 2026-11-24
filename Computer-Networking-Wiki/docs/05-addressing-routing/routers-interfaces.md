# Routers and interfaces

[← Indeks wiki](../index.md)

> **Źródło główne:** Computer Networking Textbook.pdf, s. 98–101. Treść została uporządkowana tematycznie; pełny ekstrakt źródłowy znajduje się w `_source-archive/`.


## Materiał kanoniczny

A router is a device designed to receive, forward, and analyze packets transmitted to
and from other devices on a network, and other networks.
Routers enable inter-network communication, and can provide services such ACL and
NAT, which are required in any networking scheme.
A router is a Layer 3 device that communicates using IP addresses.
Default Gateway
The default gateway is a network device that can route traffic to and from other
networks. A router typically fulfills this role.
The default gateway is similar to the door of a room. If the desired object is in another
room, the object can be reached only by exiting the current room and entering the
other room through the door.
If the destination is on the same network, there is no need to pass through the router.
Configuration
Default gateway configuration options are typically located together with other adapter
configuration options.
In Windows, the settings are located under Network & Internet Settings in Change
Adapter Options.
By default, the gateway should be received from the DHCP.
However, if manual IPs were configured, the gateway should also be configured
manually.

7 Internet Protocol Version 4 (TCP/IPv4) Properties. x
Networking Shang —
Oroanize* Comet To Disable this el Camect ung 1m @
= bluetooth Nework Connection 1D roe) Duo Berd Wiles A 6260 Bical, Ghee yeumedioas yar evoke
ky TacercinanteSona te Deven sors

©) 8B Fie and Pier Shaing for Microsc Networks =

MB vitustfox NOISE Bridged Networking Onver mags Ee ae 8

& Pinca Pocket Die PCA oefad gator [mao]

A Bla0s Packet Scheduler

Et -hlend Poca Veen 4 TPZ) . —

= = @Use the following ONS server addresses:

ae pees Preferred DNS server: @.8,.8.8]

acme One Racca ema naa Marte seve ed

Wecrreerevok pesca pve commie

play carotene Giddaeniieseared =

a a == ieee
NIC Configuration
Router Interfaces
Fast Ethernet - First made public in 1995. Operates at a speed of 100 Mbps and uses
the media standard 100BaseT.
Gigabit Ethernet - Introduced in 1999. Supports a faster speed of 1000 Mbps, and uses
the media standard 1000BaseT, but can also support 100 Mbps.
Serial Interfaces - Used for long distance transmissions. If two serial ports need to
communicate with each other, they must be synchronized with the same clock
frequency and allocate the necessary bandwidth.
Other Router Interfaces
Console - This is a physical management port, visually similar to Ethernet ports, that
provides out-of-band access to a Cisco device. Out-of-band refers to access via a
dedicated management channel used only for device maintenance.
AUX - (not the one used for audio) The auxiliary port mainly functions as a backup
console port, although it can also be used as a dial-up port for remote management,
and other purposes. The main difference between Console and AUX is that AUX pushes
output to the port after power-up, while a Console does so during the power-up
process itself.

Interface Configuration
Router interfaces need to be set up with IP addresses, similar to computer network
interfaces.
The interface [type] [id] command selects the desired interface. To use an interface, it
must be set up with ip address [ip] [subnet mask] and enabled using the no shutdown
command.
Use show ip interface brief to verify interface settings on the router.
1(config)#interface gigabitEthernet 0/0
R1(config-if)#ip address 192.168.0.1 255.255.255.0
R1(config-if)#no shutdown
%LINK-5-CHANGED: Interface GigabitEthernet@/0, changed state to up
R1(config-if)#exit
R1(config)#exit
Rl#show ip interface brief
Interface IP-Address OK? Method Status Protocol
GigabitEthernete/e 192.168.0.1 YES manual up up
Loopback Interface
Loopback is a logical interface that is not assigned to a physical port. The interface can
be used to test and manage Cisco IOS devices, because it ensures that at least one
interface will always be available.
A loopback interface should not be confused with a loopback address.
Configuration
A Loopback Interface is often configured during the initial router configuration, mainly
for testing purposes.
The interface is configured to automatically be ready for operation.
A router can have more than one loopback interface enabled simultaneously, but each
interface must have a unique IP.

A loopback interface is created using the command interface loopback <ID> via the
configuration terminal.

Router(config)#interface loopback @

%LINK-5-CHANGED: Interface Loopback®, changed state to up
%LINEPROTO-5-UPDOWN: Line protocol on Interface Loopback®@, changed state
to up

Router(config-if)#ip address 10.10.10.10 255.0.0.0

Router(config-if)#no shutdown

Router(config-if)# exit

## Powiązane laboratoria

- [NET-05-LS2](../labs/net-05-ls2.md)

## Powiązane tematy

- [Routing process and routing table](routing-process.md)
- [IPv4 static and default routing](static-routing-ipv4.md)
- [IPv4 addressing](ipv4.md)

## Źródła w zestawie

- `Computer Networking Textbook.pdf` — strony 98–101.
- `Computer Networking.pdf` — prezentacja kursowa; odpowiadający rozdział zachowany w `_source-archive/02-Course-Slides.md`.
- `Padriseup Computer Networking.pdf` — uzupełnienia i materiały dodatkowe, jeśli występowały dla tego tematu.
