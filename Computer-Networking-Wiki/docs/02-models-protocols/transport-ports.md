# TCP, UDP, logical ports and sessions

[← Indeks wiki](../index.md)

> **Źródło główne:** Computer Networking Textbook.pdf, s. 38–45. Treść została uporządkowana tematycznie; pełny ekstrakt źródłowy znajduje się w `_source-archive/`.


## Materiał kanoniczny

TCP and UDP
TCP and UDP are protocols that operate in Layer 4 (Transport Layer), and are used to
transmit data over the network.
Note: There are other Transport Layer protocols, such as RTP and SCTP, but they are
beyond the scope of this section.
TCP is trusted and more commonly used than UDP, and is fully described in RFC 793.
It verifies the availability of all parties before initiating a connection by performing a
three-way handshake. It then marks packets and makes sure they are received in the
correct order.
UDP is less strict about data integrity and is more speed-oriented. It simply sends
packets, without checking the data, even if no device is ready to receive them.
This type of communication works better when streaming content, such as audio,
where some packets may be skipped without affecting the entire stream.
UDP is fully described in RFC 768.

TCP vs UDP
TCP UDP
Connection-oriented protocol. Connectionless protocol.
Suited for applications that need fast,
Suited for applications that require high . PP
Pe pSaI sears efficient transmission. Also useful for
reliability, where transmission time is less
critical servers that answer small queries from
. large numbers of clients.
Rearranges data packets in the order Packets may arrive out of order, UDP does
specified. not rearrange them.
Guarantees that transferred data remains .
‘ = ae There is no guarantee that messages or
intact. If a packet is corrupt upon arrival, it 3 a" segs
. packets will reach their destinations.
is resent.
Performs error-checking but discards
Errors are detected via checksum. erroneous packets. Error recovery is not
attempted.
Relatively slow. Relatively fast.
Detection of error via checksum*. No error detection.
* Checksum is a piece of data that is calculated and represented as a number, and is
used for data integrity and error detection.

TCP Flags
TCP uses flags to provide additional useful information or control the connection.
Flag Role
Synchronization - this is the first flag between two hosts, and
SYN . .
is used to establish a 3-way handshake.
AGE Acknowledged - acknowledges a successful receipt by the
host.
Ret Reset - Terminates a connection if a TCP failure occurs or a
conversation is not permitted.
FIN Finish - Requests connection termination.
PSH Push - Immediately sends all buffered data.
URG Urgent - Data with a URG segment is immediately forwarded
to the Application Layer.
3-Way Handshake
A 3-way handshake is responsible for communication between network devices that
use TCP.
The handshake is known as “3-way” because it includes 3 steps:
1. The client sends “SYN”.
2. The server responds with “SYN-ACK”.
3. The client finalizes with “ACK”.
If the process ends successfully, a connection is established between the client and the
server, and data can immediately be transferred between them.

Client Server
HTML =
a cee)
ae
:
i]
i ee
3-Way Handshake Process
Session Termination
Session Termination is the last stage of a TCP connection. This is when communication
ends and the session is closed.
Step 1 - One of the sides (client) requests to close the connection, by sending a FIN flag
to the other side (server).
Step 2 - The receiver of the FIN flag (server) returns an ACK flag, to approve the request.
Step 3 -The server then sends a FIN flag to the client.
Step 4 - The client approves the FIN request by the server, and responds with an ACK
flag. The connection is then terminated.

Client Server
= ©
ee
ee
ae
~
CE ie
Session Termination Process
Logical Ports
In computer science, a logical port is a number assigned to a “logical” connection, which
is used to represent a service or protocol on the end device.
There are 65,536 in TCP and 65,536 UDP ports, ranging from O to 65535.
An IP address can send packets to the destination host, but not to the destination
service on that end device.
As an example, a street address can lead to the correct building, but it does not specify
the apartment number within that building.

Logical Port Groups
There are 65,536 ports in TCP and 65,536 in UDP, divided into three main groups, as
follows:
Well-Known Ports (0-1023) - Port numbers in the “well-known” range are assigned to
commonly used and essential protocols. The port numbers are permanent, and every
network administrator must know them.
The range includes protocols such as HTTPS, DNS, DHCP, Email protocols, and others.
Registered Ports (1024-49151) - IANA assigned these ports for IT companies that want
to register them for proprietary applications. For example, Microsoft RDP 3389 and
Dropbox 7600.
Dynamic and Private Ports (49152-65535) - This group covers the remaining logical
ports that are available for any application. The port range is known as “client ports”
and is usually used for logical client connection.
For example, a host connecting to a web server sends requests to port 80. This lets the
web server know which service the client is requesting. However, the return traffic
must be sent to a source port, which is chosen randomly. When the connection closes,
the port can be reused for another connection, enabling the client to establish multiple
connections and manage responses from multiple sources.

Common Protocol Ports
The following table lists common network protocols and their TCP and UDP ports.
Protocol TCP/UDP Logical Ports Protocol TCP/UDP _ Logical Ports
HTTP TCP 80 SSH TCP 22
HTTPS TCP 443 RDP TCP 3389
DNS UDP 53 SMB TCP 445
DHCP UDP 67, 68 FTP TCP 20, 21
SMTP TCP 25 TFTP UDP 69
POP3 TCP 110 NTP UDP 123
Viewing Open Ports
Ports are used to receive and send data.
A web server will open Port 80 in listening mode if it intends to receive HTTP traffic.
A client will open a random port for each server it accesses when browsing the web.
To inspect open ports, use the command netstat —ab, where: a represents ‘all’, and b
represents the names.

Netstat Example:
C:\WINDOWS\system32>netstat -ab
Active Connections
Proto Local Address Foreign Address State
TCP @.0.0.0:135 Leningrad:® LISTENING
[svchost.exe]
TCP @.0.0.0:443 Leningrad:® LISTENING
[vmware-hostd.exe]
TCP @.0.0.0:445 Leningrad:@ LISTENING
Can not obtain ownership information
TCP @.0.0.0:902 Leningrad:® LISTENING
[vmware -authd. exe]
TCP @.0.0.0:912 Leningrad:® LISTENING
[vmware -authd.exe]
TCP @.0.0.0:1536 Leningrad:@ LISTENING
[svchost.exe]
TCP @.0.0.0:1538 Leningrad:@ LISTENING
[svchost.exe]
TCP @.0.0.0:1539 Leningrad:® LISTENING
Short Practice
— According to the material learned in the previous part, answer the following
mm =| questions as best as you can. You can use external materials, such as
Internet searches.
1. Briefly describe the operation or function of each protocol layer.
(For example, Layer 6 encodes, encrypts, and compresses the
information.)
2. List at least two main protocols that operate in each layer. (For
example IP, ICMP-Network Layer.)
3. List two protocols that use TCP, and two that use UDP.
4. Describe the TCP 3-Way Handshake.
5. List the logical ports of the following protocols: HTTP, HTTPS, DNS,
FTP, SMTP.
6. How many layers do the TCP/IP and OSI models have, and what are
their names? (Try to answer from memory.)

## Powiązane laboratoria

- [NET-02-LS1](../labs/net-02-ls1.md)


## Uzupełnienia z notatek Riseup / zajęć

<details>
<summary>Pokaż notatki prowadzącego, dodatkowe komendy i linki powiązane z tym tematem</summary>

Jeśli router jest ustawiony tak by nie zmniejszać TTL - nie pojawi się na liście tracerta.
Netsh - Netshell - narzędzie tekstowe do konfiguracji sieci w Windowsie.
#Porty:
https://en.wikipedia.org/wiki/List_of_TCP_and_UDP_port_numbers
#Wybrane protokoły sieciowe

---

https://www.wireshark.org/
edit>>preferences>>packet diagram
#3-way handshake
SYN -> SYN/ACK -> ACK
FIN -> FIN/ACK -> ACK
Połączenie to nosi nazwę uzgadniania trój-etapowego (ang. three-way handshake). Host
źródłowy, czyli np. klient, wysyła segment zawierający flagę SYN (SYN to flaga
synchronizacji numerów sekwencyjnych) W segmencie też zawarty jest losowy numer

---

(segment sequence number) = n

* SYN-ACK – serwer odpowiada z numerem potwierdzenia (acknowledgement
number) n + 1 i numerem sekwencji m

* ACK – klient odpowiada z numerem sekwencji równym m + 1
SYN (synchronize)
SYN-ACK (synchronize-acknowledge)
ACK (acknowledge)

* FIN – jedna ze stron wysyła komunikat zakończenia

</details>

## Powiązane tematy

- [Network protocols and client-server model](network-protocols-models.md)
- [Wireshark](wireshark.md)
- [ARP and encapsulation](arp-encapsulation.md)

## Źródła w zestawie

- `Computer Networking Textbook.pdf` — strony 38–45.
- `Computer Networking.pdf` — prezentacja kursowa; odpowiadający rozdział zachowany w `_source-archive/02-Course-Slides.md`.
- `Padriseup Computer Networking.pdf` — uzupełnienia i materiały dodatkowe, jeśli występowały dla tego tematu.
