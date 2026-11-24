# TCP/IP model

[← Indeks wiki](../index.md)

> **Źródło główne:** Computer Networking Textbook.pdf, s. 36–37. Treść została uporządkowana tematycznie; pełny ekstrakt źródłowy znajduje się w `_source-archive/`.


## Materiał kanoniczny

TCP/IP (Transmission Control Protocol/Internet Protocol) was developed by DARPA in
the US Department of Defense, in 1982.
This model is a suite of communication protocols used to interconnect network devices
on the Internet.
The model describes how data is exchanged over the Internet, including how data
should be divided into packets, addressed, transmitted, routed, and received by the
destination.
TCP/IP was designed to make networks reliable and enable them to automatically
recover from a failure of any device on the network.
TCP/IP Layers
Layers in the TCP/IP model are similar to those in the OSI, except for the top three
layers.
TCP/IP uses the client-server model of communication in which a user or machine is
given access to a service by another computer on the network.
Collectively, the TCP/IP suite of protocols is classified as “Stateless”, which means each
client request is considered new, and is unrelated to previous requests.
Transmit Data Receive Data
APPLICATION APPLICATION
TRANSPORT TRANSPORT
NETWORK NETWORK
Network Access Physical Layer Network Access
TCP/IP Model Structure

Layer 4 Application - The Application Layer defines TCP/IP application protocols and
how host programs interface with Transport Layer services to use the network.
The Application Layer includes all higher-level protocols, such as DNS, HTTP, Telnet,
SSH, FTP, TFTP, SNMP, SMTP, DHCP, X Windows, RDP, and others.
The TCP/IP top layer is equivalent to the combined three top layers of OSI.
Layer 3 Transport — The Transport Layer in TCP/IP corresponds to the Transport Layer in
OSI. It handles the coordination of data transfer between end systems and hosts,
including how much data to send, at what rate, destinations, etc.
The transport layer determines if the connection should be instantiated, how to verify
data integrity, how to recover from a connection error, and if retransmission is
necessary. Data in this layer is organized in segments.
The protocols in this layer provide flow control, multiplexing, and reliability.
Layer 2 Internet - The Internet Layer organizes data into packets known as IP
datagrams. The datagrams contain logical source and destination addresses.
The Internet Layer’s job is to allow hosts to send packets across multiple paths to any
other network, and deliver them to their destinations, via routers operating on this
layer.
Routers operate in this layer.
The Internet layer in TCP/IP corresponds to the Network Layer in OSI.
Layer 1 Network Access - The Network Access Layer is the lowest layer of the TCP/IP
protocol model. It corresponds to the Data Link and Physical layers of OSI.
Packets from the Internet layer are sent to the Network Access layer for delivery within
the physical network. Data in this layer is organized in frames.
Protocols in this layer provide the means for the system to deliver data to other devices
in a directly connected network, using physical addresses (MACs).
The protocols and standards defined for this layer dictate how data is transmitted on
the media (Ethernet cable, wireless connection, others).
The Access Layer of the TCP/IP model corresponds to the Data Link and Physical layers
of OSI.

## Powiązane laboratoria

- [NET-02-LS1](../labs/net-02-ls1.md)


## Uzupełnienia z notatek Riseup / zajęć

<details>
<summary>Pokaż notatki prowadzącego, dodatkowe komendy i linki powiązane z tym tematem</summary>

-Warstwa internetu (IP)
-Warstwa dostępu do sieci (MAC)
warstwa aplikacji -> warstwa dostępu do sieci -enkapsulacja
warstwa dostępu do sieci-> warstwa aplikacji - dekapsulacja
EBCDIC
https://pl.wikipedia.org/wiki/EBCDIC
Frame Relay

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

</details>

## Powiązane tematy

- [OSI model](osi-model.md)
- [TCP, UDP, logical ports and sessions](transport-ports.md)
- [ARP and encapsulation](arp-encapsulation.md)

## Źródła w zestawie

- `Computer Networking Textbook.pdf` — strony 36–37.
- `Computer Networking.pdf` — prezentacja kursowa; odpowiadający rozdział zachowany w `_source-archive/02-Course-Slides.md`.
- `Padriseup Computer Networking.pdf` — uzupełnienia i materiały dodatkowe, jeśli występowały dla tego tematu.
