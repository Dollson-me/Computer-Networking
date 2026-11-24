# ARP and encapsulation

[← Indeks wiki](../index.md)

> **Źródło główne:** Computer Networking Textbook.pdf, s. 56–61. Treść została uporządkowana tematycznie; pełny ekstrakt źródłowy znajduje się w `_source-archive/`.


## Materiał kanoniczny

If a device wants to communicate with another device on the same LAN, it must
encapsulate the MAC address of the destination device.
To get the MAC address, it uses a protocol called ARP (Address Resolution Protocol),
that resolves a logical address (IP) to a physical address (MAC), and saves the results in
the host ARP cache.
ARP operates in Layers 2 and 3 of the OSI model.
Every Layer 3 device uses ARP.
Note: Switches make forwarding decisions based on the physical address of the frame.
ARP Process
Scenario: Host A wants to communicate with host B. Host A knows host B’s IP address
but not its MAC address.
Step 1 - Host A sends an ARP Request to all hosts on the network (Broadcast), with
Host B’s IP as the destination MAC, requesting its MAC address.
Step 2 - The switch forwards the ARP request to all ports.
Step 3 - Host B recognizes the IP address in the request, so it performs an ARP reply, in
which it lists its own MAC address.
Step 4 - Host A receives the ARP reply and saves host B’s MAC address in the ARP cache,
together with Host B’s corresponding IP address.

ll Es
v,
&. 5 wy neg
& > z - 5 %
GY
qt Ml
fo \ fo \ TT mn
ARP Table:
Host IP MAC
[8 | 10002 | ewe |
ARP Process

ARP Table (Cache)
Command: arp -a
The ARP table or cache is stored in the RAM of the device.
The ARP contains three parameters:
* Destination host IP
* Corresponding MAC of that host
* Entry source MAC learned automatically or manually
arp —a and arp —g display the host ARP table.
Show arp displays a Cisco device ARP table.
Example:

C:\Windows\system32>arp -a 7

Interface: 10.71.0.110 --- x17

Internet Address Physical Address Type
Q ®.100 90-7c-ac-a9-a2-c9 dvnami

Additional ARP Commands
arp —d deletes the host ARP table.
arp —s adds a static entry to the ARP table that resolves to a specific IP address.
Note: Static ARP helps reduce the risk of ARP spoofing attacks.
arp inet_addr defines a specific IP address.
arp eth_addr defines a specific MAC address.
Examples:

C:\Windows\system32>arp -d

C:\Windows\system32>arp -s 10.0.0.2 @0-aa-bb-11-22-33
Data Encapsulation
When a message is sent from source to destination, it must have a specific format or
structure. Message formats depend on the type of message and the channel used to
deliver it.
The opposite process of encapsulation is called decapsulation. This is when the host is
on the receiving side.
The same process occurs in OSI and TCP/IP using the same protocols.
For example, to send mail, we place a message in an envelope — encapsulation. The
envelope is written in a format the mail service accepts and is sent to the destination.
The receiving side opens the envelope and takes out the message — decapsulation.
Note: The envelope is similar to a network frame.
Terminology
Headers and Trailers - Headers and trailers represent control data added by protocols
to the beginning and end of each data unit, in each layer.
For example, IP packages the logical source and destination address in an IPv4 header,
and adds it to the data unit in the Network Layer.

Encapsulation - Adding Headers and Trailers to data is called encapsulation. Processing
them and removing them is called decapsulation.
Depending on the communication type, protocols in each layer add the correct header
to the data unit.
PDU - Protocol Data Unit is a piece of information added to or removed from the first 4
layers of the OSI model and the first 3 layers of the TCP/IP model.
PDU consists of protocol-specific control information and user data.
Examples are segments, packets, and frames.
Encapsulation Process
As an example, we can focus on the process of sending data. The first step in the
process is ... YOU!
When you click on a link:
The Application layer creates an HTTP header requesting the web page from the server.
The Presentation layer encodes, encrypts, or compresses the data traveling down from
the Application layer, if necessary. For example, it may convert text to a binary string.
The Session layer determines the direction of the data, one-way or two-way, and
whether the connection is secure or not.
In addition, a session ID is assigned to the connection.
The Transport layer adds a header containing the source and destination logical ports,
and other control information.
This layer also divides data from upper layers into smaller pieces called Segments. Each
segment is a maximum (MSS) of 1460 bytes.

Data
HTTP GET
Data
0101101010101010
Data
0101101010101010 Thisis‘alled’a
TCP Header Payload
0101101010101010
Encapsulation in Layers 4 to 7
The Network Layer adds a header to the segment with the IP source and destination
addresses, and other control information (such as TTL). During this step, the segment is
encapsulated in a packet.
Packets are limited to a maximum size (MTU — Maximum Transmission Unit) of 1500
bytes without fragmentation. This excludes the 18 bytes of overhead that are used for
the frame’s header and FCC.
The Data Layer adds a Header and Trailer to the Packet. The header contains the
physical source and destination addresses. The trailer, also called FCS, is for frame error
checking only.
The Physical layer accurately transmits the Frames along with the physical medium.
For example, it sends electric pulses over an Ethernet cable, or wireless radio waves.

Packet
IP Header TCP Header Payload
Ethernet Header IP Header TCP Header ~ FCS
> IU
Encapsulation in Layers 1 to 3

## Powiązane laboratoria

- [NET-02-LS1](../labs/net-02-ls1.md)


## Uzupełnienia z notatek Riseup / zajęć

<details>
<summary>Pokaż notatki prowadzącego, dodatkowe komendy i linki powiązane z tym tematem</summary>

danych wymiany danych pomiędzy klientem a hostem

- ARP - Address Resolution Protocol - protokół sieciowy umożliwiający mapowanie
logicznych adresów warstwy sieciowej (warstwa 3) na fizyczne adresy warstwy łącza danych
(2).
#Sieci bezprzewodowe

---

https://pasja-informatyki.pl/sieci-komputerowe/model-tcp-ip-iso-osi/
https://www.soisk-me.pl/klasa-iv-sieci/model-iso-osi-i-tcp-ip
#enkapsulacja
http://oprogramowaniu.pl/czym-jest-enkapsulacja/
warstwa aplikacji -> warstwa dostępu do sieci -enkapsulacja
warstwa dostępu do sieci-> warstwa aplikacji - dekapsulacja
https://pmr.ii.pw.edu.pl/~pmr/ws/
[Windows]
arp -a - wyświetlenie tablicy ARP
arp -d - usuwanie tablicy ARP [jako Administrator]
#Wireshark - przykładowe filtry

https://wiki.wireshark.org/CaptureFilters

</details>

## Powiązane tematy

- [OSI model](osi-model.md)
- [TCP/IP model](tcp-ip-model.md)
- [Wireshark](wireshark.md)

## Źródła w zestawie

- `Computer Networking Textbook.pdf` — strony 56–61.
- `Computer Networking.pdf` — prezentacja kursowa; odpowiadający rozdział zachowany w `_source-archive/02-Course-Slides.md`.
- `Padriseup Computer Networking.pdf` — uzupełnienia i materiały dodatkowe, jeśli występowały dla tego tematu.
