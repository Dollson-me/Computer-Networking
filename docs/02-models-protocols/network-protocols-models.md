# Network protocols and client-server model

[← Indeks wiki](../index.md)

> **Źródło główne:** Computer Networking Textbook.pdf, s. 29–31. Treść została uporządkowana tematycznie; pełny ekstrakt źródłowy znajduje się w `_source-archive/`.


## Materiał kanoniczny

Client-Server Model
A client represents the endpoint device (not necessarily a PC) that requested an
operation.
A server represents the endpoint device that receives a request and performs the
requested operation.
z Dear Server 18.77.22.44,
www | can you please send my
c—o Facebook home page.
Sure! 10.2.2.7, here you
go, enjoy! _
The Client-Server model is a distributed application structure that manages tasks and
workloads by sharing them among providers of resources and services (servers), and
delivers responses to service requesters (clients).
An alternative method is to use broadcast or multicast channels to distribute
information.
Common Network Protocols
HTTP - HTTP is an unsecure protocol used to transfer information over the web.
Due to the fact that HTTP traffic is not encrypted, it can be sniffed on the network.
For example, if credit card information is entered at an HTTP website, it can be
captured in simple text format.

HTTPS - HTTPS is the encrypted version of HTTP.
It is used for secure communication and is widely used on the Internet.
Communication is encrypted using TLS (Transport Layer Security) or SSL (Secure Socket
Layer).
DNS - Translates domain names to IP addresses according to predefined databases.
The DNS protocol is used for address resolution in a network.
For example, when a URL is entered in a browser, the DNS protocol translates the
domain that was entered to an IP address.
FTP - File Transfer protocol is used to transfer files over the network.
For example, the FTP service can be used to transfer files to another device over the
network.
DHCP - The DHCP service is responsible for assigning an IP address to each device on a
network configured to use DHCP, such as PCs, routers, firewalls, servers, and others.
For example, a PC configured with DHCP will automatically be assigned an IP address
upon startup.
SMTP - Simple Mail Transfer Protocol is the standard protocol for mail transfer over the
Internet.
For example, when an Email is sent over the network, the SMTP protocol manages the
operation.
SSH - Secure SHell is a secure command-line protocol that allows the user to run remote
commands on a remote machine.
Any data that passes through SSH is encrypted.
For example, when a remote connection is made to a device, the connection is made
using SSH on port 22.
ICMP - Internet Control Message Protocol is used by network devices to generate error
messages when IP packets are not able to reach their destination.

Network Models
The idea behind creating a networking model was to set a standard for the
development and usage of network components.
Standards allow devices to communicate without requiring continuous configuration in
different device platforms.
In addition, dividing the networking process into smaller sub-processes helps debug
issues and pinpoint solutions.
OSI vs TCP/IP
Today, OSI and TCP/IP are very similar due to the way they evolved over time.
OSI is often used as an educational model, while TCP/IP is used more as a practical
model.
OSI is a network model in which each functionality of the network is represented by a
layer.
There are seven layers, in which the functionality of each is dependent on the one
below it.
OSI was developed by the International Organization of Standardization.
The first TCP/IP specification was submitted several years after the OSI model.
The original TCP/IP model consisted of 4 layers but was later updated to the current 5
layers. However, the 4-layer version is still more commonly used.
TCP/IP is typically used for network analysis due to its lesser involvement with the top 3
layers.

## Powiązane laboratoria

- Brak bezpośrednio przypisanego laboratorium w zestawie.


## Uzupełnienia z notatek Riseup / zajęć

<details>
<summary>Pokaż notatki prowadzącego, dodatkowe komendy i linki powiązane z tym tematem</summary>

#Architektura sieci

- Client-server - serwer udostępnia jedną lub więcej usług lub zasobów, do jednego
lub wielu klientów. Przykładowe usługi: SMTP, FTP, WWW, Samba itd. Klient zawsze
rozpoczyna komunikację i wysyła żądania (request) o dostęp do zasobów. Serwer
odpowiada na żądanie udostępniająć żądany zasób.

---

#Porty:
https://en.wikipedia.org/wiki/List_of_TCP_and_UDP_port_numbers
#Wybrane protokoły sieciowe

- IP - Internet Protocol - protokół stanowiący podstawę do wymiany danych wewnątrz
sieci

- DNS - Domain Name System - rozwiązywanie adresów http na adres fizyczne IP

- DHCP - Dynamic Host Configuration Protocol - automatyczna konfiguracja nowych
hostów w sieci

- HTTP - Hypertext Transfer Protocol - wykorzystywany do transferu danych
tekstowych, obrazów i innych danych które mozna umieścić na stronie internetowej

- HTTPS - secure implementation of HTTP - tak jak HTTP ale zapewnia szyfrowanie
danych wymiany danych pomiędzy klientem a hostem

- ARP - Address Resolution Protocol - protokół sieciowy umożliwiający mapowanie

</details>

## Powiązane tematy

- [OSI model](osi-model.md)
- [TCP/IP model](tcp-ip-model.md)
- [TCP, UDP, logical ports and sessions](transport-ports.md)

## Źródła w zestawie

- `Computer Networking Textbook.pdf` — strony 29–31.
- `Computer Networking.pdf` — prezentacja kursowa; odpowiadający rozdział zachowany w `_source-archive/02-Course-Slides.md`.
- `Padriseup Computer Networking.pdf` — uzupełnienia i materiały dodatkowe, jeśli występowały dla tego tematu.
