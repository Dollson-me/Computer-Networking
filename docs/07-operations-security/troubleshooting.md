# Troubleshooting methodology

[← Indeks wiki](../index.md)

> **Źródło główne:** Computer Networking Textbook.pdf, s. 171–173. Treść została uporządkowana tematycznie; pełny ekstrakt źródłowy znajduje się w `_source-archive/`.


## Materiał kanoniczny

Issues can and will arise, even in networks that were designed using the most advanced
technologies.
This lesson covers the ways network issues can be resolved and the tools that can help
resolve them quickly and efficiently.
An important aspect of network troubleshooting, also described in this lesson, is the
usage of discovery protocols.
Documentation
Quick and efficient troubleshooting is based, in part, on continuous and detailed
network-related documentation.
Network documentation includes physical and logical topological diagrams, network
and end-device backup configuration files, IP and MAC addressing schemes, and
network performance baselines.
Troubleshooting Steps
Gather Information - The first and most important step is gathering information and
symptoms from network devices, end systems, and users.
Isolate the Problem - Based on the symptoms, eliminate variables until a single
problem or a set of related problems is identified as the cause.
Implement a Solution - Consider the severity of the problem and the impact of the
solution. Then begin planning, testing, and documenting possible solutions.
Problem Solved? - If the problem was not solved, repeat steps two and three again, and
deepen the research.
Documentation - Document every step you took in the process.

Gathering Information

© Question end users

e Protocol Analyzers (Wireshark, others)

e Physical troubleshooting tools (cable tester, others)

e Network management software

e CMD network commands

e Show and Debug commands

e IP SLA - Monitors network performance in real-time

e Neighbor Discovery Protocols

OSI Troubleshooting Methods

Troubleshooting methods based on the OSI module include the following techniques:
Bottom-Up - In this method, the starting point is at the bottom of the OSI model, the
physical layer. The examination starts from the network's infrastructure, such as cables
and NICs.

Top-Down - In this method, the starting point is at the top of the OSI model, the
application layer. The examination starts with the application itself.
Divide-&-Conquer - In this method, the starting point isn't predefined as in previous
methods. A particular layer is selected and examined, then the layer above it is
examined, and so on. If a layer is faulty, the next one to examine should be the one
below it.

Software Tools

Network Management Software (NMS) provides excellent tools for troubleshooting.
NMS continuously monitors network activity and establishes a clear baseline for
reference purposes. This enables network administrators to promptly identify issues,
and, in some cases, predict the occurrence of such issues.

Top IOS Show Commands
Show interfaces - This command outputs a large volume of information, including
interface errors, bandwidth utilization, and interface speed.
Show ip route - This command verifies network reachability, and indicates if routing
protocols are operating as they should.
Show ip interface brief - This command presents only information about interfaces
associated with the IP protocol. The command outputs a detailed summary of interface
status and IP addresses.
Show running-config - This command displays the complete router configuration in use
at that time.
Show start-up config - By default, the initial configuration controlling the system is the
start-up config. When the router boots, it will load start-up config automatically.
Extended Ping and Traceroute
Extended Ping is used to perform advanced checks of network connectivity. It is also
able to change the source IP on the packet leaving the router.
Example:

<Output Omitted>

R2#ping

Protocol [ip]:

Target IP address: 172.16.1.2

Repeat count [5]:

Datagram size [100]:

Timeout in seconds [2]:

Sending 5, 10@-byte ICMP Echos to 172.16.1.2, timeout is 2 seconds:

titi

Success rate is 100 percent (5/5), round-trip min/avg/max = 0/@/3 ms
The Traceroute command discovers the path packets take to a remote destination, and
where routing failures occurred.

## Powiązane laboratoria

- Brak bezpośrednio przypisanego laboratorium w zestawie.

## Powiązane tematy

- [CDP and LLDP](cdp-lldp.md)
- [Syslog](syslog.md)
- [NTP](ntp.md)

## Źródła w zestawie

- `Computer Networking Textbook.pdf` — strony 171–173.
- `Computer Networking.pdf` — prezentacja kursowa; odpowiadający rozdział zachowany w `_source-archive/02-Course-Slides.md`.
- `Padriseup Computer Networking.pdf` — uzupełnienia i materiały dodatkowe, jeśli występowały dla tego tematu.
