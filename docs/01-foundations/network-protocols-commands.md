# Network protocols and Windows commands

[← Indeks wiki](../index.md)

> **Źródło główne:** Computer Networking Textbook.pdf, s. 20–24. Treść została uporządkowana tematycznie; pełny ekstrakt źródłowy znajduje się w `_source-archive/`.


## Materiał kanoniczny

Protocols can be considered “languages” of data transfer. To communicate properly,
two or more devices must first agree to use the same “language”.
Protocols are predefined sets of rules describing how something should work or
behave. They help maintain order among different technologies.
Network Protocol Examples
IP - The Internet Protocol is used to establish communication over the network, without
delivery verification.
DNS - Dynamic Name Service is a protocol used to translate domain names to IP
addresses, and vice versa.
DHCP - The Dynamic Host Configuration Protocol is used to allocate IP addresses to new
computers that join the network.
HTTP - The Hypertext Transfer Protocol is used to transfer text-based data, such as web
pages, over the Internet.
HTTPS - HTTPS is a secure implementation of HTTP. It encrypts the transferred data to
prevent it from being intercepted.
Network Commands
Commands are used in network configuration, maintenance, troubleshooting, and
more.
An example of a powerful use of network commands is for error detection.
It is essential for any network to frequently run commands that check the state of the
network and monitor it.
Although some systems enable network configuration via a GUI, the configuration is still
often done via the CLI.

Windows Network Command Examples
Ping
Ping is the most common command in administrative networking activity.
It is used to check connectivity between computers over the network.
It also provides information, such as connection speed and reliability.
Command:
Ping x.x.x.x

Example:

C:\Windows\system32> ping 8.8.8.8

Pinging 8.8.8.8 with 32 bytes of data:

Reply from 8.8.8.8: bytes=32 time=224ms TTL=54

Reply from 8.8.8.8: bytes=32 time=681ms TTL=54

Reply from 8.8.8.8: bytes=32 time=319ms TTL=54

Reply from 8.8.8.8: bytes=32 time=103ms TTL=54

Ping statistics for 8.8.8.8:

Packets: Sent = 4, Received = 4, Lost = @ (@% loss),
Approximate round trip times in milli-seconds:
Minimum = 103ms, Maximum = 681ms, Average = 331ms
IPconfig
ipconfig - displays a computer’s IP configuration.
ipconfig /all — displays extended information.
It can also request a new IP address if a DHCP server is configured.
ipconfig /release — drops an IP address.
ipconfig /renew — requests a new IP address.
Command:
ipconfig

Example:

C:\Windows\system32> ipconfig

Windows IP Configuration

Ethernet adapter Ethernet:

Connection-specific DNS Suffix .:
Link-local IPv6 Address... . . : £b21::b23e:28e9:c76b:7b35%11
IPv4 Address... ....... . ? 192.168.5.11
Subnet Mask... ..... . . . ? 255.255.255.0
Default Gateway ........ . 2 192.168.5.1
Nslookup
Computers use IP addresses to communicate with each other, while humans use names
that are easier to remember than numbers.
Nslookup sends a query to get the name of a computer by its IP address.
It can also do the opposite - query an IP address by the domain name.
Command:
nslookup x.x.x.x

Example:

C:\Windows\system32> nslookup www.cyber.com

Server: pfSense.c122b.lan

Address: 192.168.0.1

Non-authoritative answer:

Name: cyber.com

Address: 199.244.49.102

Aliases: www.cyber.com

C:\Windows\system32> nslookup 199.244.49.102

Server: pfSense.c122b.lan

Address: 192.168.0.1

Tracert
Information in the network passes through multiple stations on the way to its
destination.
Tracert displays all the stations (hops) along the route taken by the information to its
destination.
It can work with a domain name or an IP address.
Command:
tracert X.x.x.x
Example:
C:\Windows\system32> tracert 8.8.8.8
Tracing route to dns.google [8.8.8.8]
over a maximum of 3@ hops:
1 <1 ms <1 ms <1 ms pfSense.cl22b.lan [192.168.0.1]
2 115 ms 78 ms 59 ms 192.168.1.1
3 * * * Request timed out.
4 * * * Request timed out.
5 241 ms 178 ms 218 ms 172.17.10.182
6 * * = Request timed out.
7 bs is * Request timed out.
8 * # m= Request timed out.
9 * * 259 ms core-213-57-0-69.PT.hotnet.net.il [213.57.0.69]
10 «281 ms) «245 ms) 225 ms_ core-213-57-3-150.HFA.hotnet.net.il [213.57.3.150]
11 201 ms 174 ms 228 ms 108.170.251.129
12 188 ms 23 ms 326 ms 74.125.37.167
13 +131 ms 83 ms 109 ms dns.google [8.8.8.8]
Trace complete.

Netsh
A fast way to configure network information is to use the netsh command.
It allows the configuration of the IP address, DNS, default gateway, and various network
functions.
The example below shows how to set an IP address and verify settings using netsh.
Command:
Netsh [command \ option ]
Example:
C:\Windows\system32> netsh interface ip set address “Ethernet" static
192.168.10.5 255.255.255.0 192.168.10.1
C:\Windows\system32> netsh interface ip show config
Configuration for interface "Ethernet"
DHCP enabled: No)
Default Gateway: 192.168.10.1
Gateway Metric: 1
InterfaceMetric: 5
Statically Configured DNS Servers: None
Register with which suffix: Primary only
Statically Configured WINS Servers: None
é Lab — Local Network Configuration
— J | Learn about and practice CLI network commands on Windows, using CMD.
m=:
Perform the instructions in lab document Net-01-L1.

## Powiązane laboratoria

- [NET-01-LS1](../labs/net-01-ls1.md)


## Uzupełnienia z notatek Riseup / zajęć

<details>
<summary>Pokaż notatki prowadzącego, dodatkowe komendy i linki powiązane z tym tematem</summary>

I ciekawostka - chyba nic nie tłumi lepiej sygnału elektromagnetycznego niż drzewo liściaste
:)
Ping - używa protokołu ICMP - Internet Control Message Protocol, dosł. internetowy protokół
komunikatów kontrolnych - warstwy 3 (sieciowej).
https://pl.wikipedia.org/wiki/Internet_Control_Message_Protocol
ipconfig - komenda wyświetlająca informacje o konfiguracji interfejsów sieciowych w
windowsie. W linuxie jest ifconfig (interface config)

Nslookup - odpytuje serwer DNS (zawsze) o rekord. Dlatego Nslookup nie pokaże nam
rekordów lokalnych ustawionych w pliku hosts.
nslookup może odpytać o konkretny rodzaj rekordu, np:
nslookup -q=TXT hackampus.com
Tracert - działa podobnie jak ping z użyciem ICMP. Wysyła natomiast pakiety z TTL
zwiększanym o 1, tak by kolejne routery odpowiadały z informacją o wygaśnięciu pakietu.
Jeśli router jest ustawiony tak by nie zmniejszać TTL - nie pojawi się na liście tracerta.
Netsh - Netshell - narzędzie tekstowe do konfiguracji sieci w Windowsie.
#Porty:
https://en.wikipedia.org/wiki/List_of_TCP_and_UDP_port_numbers
#Wybrane protokoły sieciowe

---

automatyczne odświeżanie interfejsu
logging synchronous
https://wiki.wireshark.org/uploads/moin_import/attachments/SampleCaptures/dns-icmp.pca
png.gz
https://ia601604.us.archive.org/20/items/cisco-packet-tracer-821-ubuntu-64bit/CiscoPacketT
racer_821_Windows_64bit.exe

</details>

## Powiązane tematy

- [TCP, UDP, logical ports and sessions](../02-models-protocols/transport-ports.md)
- [ARP and encapsulation](../02-models-protocols/arp-encapsulation.md)
- [Wireshark](../02-models-protocols/wireshark.md)

## Źródła w zestawie

- `Computer Networking Textbook.pdf` — strony 20–24.
- `Computer Networking.pdf` — prezentacja kursowa; odpowiadający rozdział zachowany w `_source-archive/02-Course-Slides.md`.
- `Padriseup Computer Networking.pdf` — uzupełnienia i materiały dodatkowe, jeśli występowały dla tego tematu.
