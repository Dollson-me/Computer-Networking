# OSI model

[← Indeks wiki](../index.md)

> **Źródło główne:** Computer Networking Textbook.pdf, s. 32–35. Treść została uporządkowana tematycznie; pełny ekstrakt źródłowy znajduje się w `_source-archive/`.


## Materiał kanoniczny

OSI (Open Systems Interconnection) was developed by the International Organization
for Standardization (ISO) in 1974.
OSI defines a networking framework to implement protocols in layers. It conceptually
divides computer network architecture into a logical seven-layer progression.
Lower layers deal with electrical signals, chunks of binary data, and routing data across
networks.
Higher levels cover network requests and responses, data representation, and network
protocols, from a user's perspective.
The OSI model is divided into seven layers: Application, Presentation, Session,
Transport, Network, Datalink, and Physical.
When network traffic is generated, it is assembled (encapsulated) from the top layer to
the bottom layer.
When received, traffic goes through the model in the reverse direction: from bottom to
top (decapsulation).

Transmit Data Receive Data

APPLICATION APPLICATION
PRESENTATION PRESENTATION
SESSION SESSION
TRANSPORT TRANSPORT

NETWORK NETWORK

DATA LINK DATA LINK

PHYSICAL Physical Layer PHYSICAL

OSI Model Structure

OSI Layers
Layer 7 Application - Users interact directly with applications that operate at Layer 7.
Examples of Layer 7 applications include web browsers such as Google Chrome, Firefox,
and Safari, and other applications, such as SSH and FTP.
Layer 6 Presentation - The Presentation Layer prepares or translates data from
application format to network format, and vice versa.
An example of the Presentation Layer operation is the encryption and decryption
process.
Layer 5 Session - The session layer is responsible for creating a session between two
devices. It is also responsible for session checkpoints and recovery.
Layer 4 Transport - The Transport Layer handles the coordination of data transfer
between end systems and hosts, including how much data to send, at what rate,
destination, and more. Data in this layer is organized in segments.
The transport layer determines if the connection should be instantiated, how to verify
data integrity, how to recover from a connection error, and if retransmission is
necessary. The protocols in this layer provide flow control, multiplexing, and reliability.
Layer 3 Network - The Network Layer organizes data into packets, known as IP
datagrams. The datagrams contain logical source and destination addresses.
Routers operate in this layer.
The Network Layer’s job is to allow hosts to send packets across multiple paths to any
other network, and deliver them to their destinations, via routers that operate in
Layer 3.
Diagnostic tools, such as ping and tracert, operate in this layer.
Layer 2 Data Link - The Data Link Layer provides node-to-node data transfer (between
two directly connected nodes) and can provide the means to detect errors that may
occur in the Physical Layer. Data in this layer is organized into frames.
The Data Link Layer includes two sub-layers: MAC (Media Access Control) and LLC
(Logical Link Control).
Switches operate in this layer.

Layer1 Physical - The Physical Layer defines the details of how data is physically sent
through the network.
This layer determines how bits are electrically or optically transferred by hardware
devices that interface directly with a network medium, such as coaxial cable, optical
fiber, or twisted-pair copper wire.
Hubs operate in this layer.
Protocols used in OSI Layers
Each network protocol is assigned to a particular OSI layer.
Common protocols in each layer include:

LAYER PROTOCOLS

Application DNS, DHCP, SSH, HTTPS, FTP, SNMP, SMTP, POP3

. Encryption, Encoding, SSL/TLS, ASCII, EBCDIC, TIFF, GIF, PICT,
Presentation
JPEG, MPEG, MIDI

Session NFS, NetBios names, RPC, SQL

Transport TCP, UDP, RTP, SCTP

Network IPv4, IPv6, ICMPv4, ICMPv6, IPX

Data Link Ethernet, PPP, FDDI, ATM, IEEE 802.5/ 802.2, HDLC, Frame Relay

. Ethernet (IEEE802.3), Wi-Fi (IEEE 802.11), FDDI, B8ZS, V.35, V.24,
Physical
RJ45

Memory Tips for OSI Layers
Layer 1 to Layer 7 - Please Do Not Throw Sausage Pizza Away
Layer 1 to Layer 7 - Please Do Not Touch Steve’s Pet Alligator
Layer 7 to Layer 1 - All People Seem To Need Data Processing

## Powiązane laboratoria

- [NET-02-LS1](../labs/net-02-ls1.md)


## Uzupełnienia z notatek Riseup / zajęć

<details>
<summary>Pokaż notatki prowadzącego, dodatkowe komendy i linki powiązane z tym tematem</summary>

Ch1 & Ch2 - Network Introduction & Fundamentals
ARPANET https://pl.wikipedia.org/wiki/ARPANET
#Warto wspomnieć o modelu ISO/OSI i porównać z modelem TCP/IP.
https://pl.wikipedia.org/wiki/Model_OSI

https://pl.wikipedia.org/wiki/Model_TCP/IP

---

:)
Ping - używa protokołu ICMP - Internet Control Message Protocol, dosł. internetowy protokół
komunikatów kontrolnych - warstwy 3 (sieciowej).
https://pl.wikipedia.org/wiki/Internet_Control_Message_Protocol
ipconfig - komenda wyświetlająca informacje o konfiguracji interfejsów sieciowych w
windowsie. W linuxie jest ifconfig (interface config)

</details>

## Powiązane tematy

- [TCP/IP model](tcp-ip-model.md)
- [ARP and encapsulation](arp-encapsulation.md)
- [TCP, UDP, logical ports and sessions](transport-ports.md)

## Źródła w zestawie

- `Computer Networking Textbook.pdf` — strony 32–35.
- `Computer Networking.pdf` — prezentacja kursowa; odpowiadający rozdział zachowany w `_source-archive/02-Course-Slides.md`.
- `Padriseup Computer Networking.pdf` — uzupełnienia i materiały dodatkowe, jeśli występowały dla tego tematu.
