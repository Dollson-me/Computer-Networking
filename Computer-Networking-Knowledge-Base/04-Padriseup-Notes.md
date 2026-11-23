# 04 — Padriseup / Riseup Computer Networking — pełne notatki

Źródło: `Padriseup Computer Networking.pdf` (30 stron). Plik ma natywną warstwę tekstową, więc poniżej zachowano jego treść bez OCR.


### Padriseup — strona 1

Grupa: BM080723UJ
Uczelnia: Jagiellonian University-Krakow
Rodzaj kursu: Blue Main Bi-Weekly
Czas trwania zajęć: 8 h
International Computer Networking for Blue Team
https://www.hackampus.com/book/480
Wykładowca: Jacek Wislak jacek.w@hackeru.com
TA: Mateusz Włodarczyk, Adam Milian
UWAGA, UWAGA!
Riseup nie zastępuje własnych notatek, ma jedynie na celu usprawnienie prowadzenia
zajęć.
Zalecamy prowadzenie notatek z zajęć we własnym zakresie - zdecydowanie usprawni to
przyswojenie materiału z zajęć.
UWAGA, UWAGA!
​
Zasady przyjaznego chatu:
1.​ Problemy opisujemy w wiadomości publicznej, dzięki temu inni też skorzystają.​

2.​ Precyzyjny opis i screenshoty przyśpieszają rozwiązywanie problemów.​

3.​ Powstrzymujemy się od pisania nie na temat.​

4.​ Jeśli ktoś czegoś nie wie to trzeba pytać (wstydliwi mogą na priv).​

5.​ Używanie imienia i nazwiska na Zoomie ułatwia weryfikowanie obecności.​

6.​ Spóźnienie zgłaszaj do TA.​

Drodzy Państwo, kurs jest intensywny, wiedzę buduje się warstwami, więc zalecamy po
każdych zajęciach :
1.​ powtórzyć cały materiał z zajęć​

2.​ przejść jeszcze raz przez laby​

3.​ przeczytać materiały dodatkowe​


### Padriseup — strona 2

4.​ uzupełnić zaległości, brakującą wiedzę​

5.​ zapisać tematy zagadnienia niezrozumiałe i zapytać o nie na najbliższych zajęciach
na chacie głównym.​

Powyższe pomogą Państwu w sprawnym zdobywaniu wiedzy i kompetencji które są
wymagane w cyber.
W razie pytań etc, jesteśmy dla Państwa z pomocą 😉
Logistyka:
1.​ Używaj na Zoomie imienia i nazwiska (niezbędne do obecności).​

2.​ Spóźnienia zgłaszaj do TA (na priv)​

3.​ Wszelkie kwestie po zajęciach zgłaszaj na adres supportu:
supportblueteam@uj.edu.pl​

4.​ W książce logistycznej w Hackcampusie jest opisana cała logistyka kursu (Blue
Team Course book for [ID grupy]) - egzaminy, Final Projecty, Cywar itp.​

Bardzo dziękujemy za trzymanie się zasad :-)
Przerwy:
10:30 - 10:45
12:00 - 12:45
15:00 - 15:15
kontakt do prowadzącego: jacek.w@hackeru.com
kontakt do supportu: supportblueteam@uj.edu.pl
Opiekun grupy: Nikola Milczanowska email: nikola.m@hackeru.com, kom. 723 300 569

06.08.2023
Ch1 & Ch2 - Network Introduction & Fundamentals
ARPANET https://pl.wikipedia.org/wiki/ARPANET
#Warto wspomnieć o modelu ISO/OSI i porównać z modelem TCP/IP.
https://pl.wikipedia.org/wiki/Model_OSI


### Padriseup — strona 3

https://pl.wikipedia.org/wiki/Model_TCP/IP
typy skrętek:
https://www.dipol.com.pl/skretkakomputerowa-_oznaczenia_standardy_pomiary_bib526.htm
#Wstęp do sieci komputerowych
​
Sieć - grupa komputerów lub innych urządzeń, które są w stanie komunikować się ze
sobą. Sieć może być tworzona z pomocą fizycznych kabli (skrętka ethernet, światłowód,
kabel koncentrytczny etc.) lub za pomocą technologii bezprzewodowych. Sieci komputerowe
mogą różnić się rozmiarami (np. LAN, WAN) lub dostarczać określonych usług (np. centra
danych, serwerownie) oraz łączyć ze sobą komputery z różnych zakątków świata.
​
NIC - Network Interface Controller - komponent sprzętowy, który zezwala na
połączenie się komputera do fizycznej sieci komputerowej. Każdy NIC posiada adres MAC
(unikalny identyfikator urządzenia).
Przykładowy adres MAC: 91-8D-89-2D-D5-A6 lub 00:0d:83:b1:c0:8e
gdzie pierwsze trzy segmenty identyfikują producenta
natomiast trzy ostatnie segmenty są numerem identyfikującym urządzenia
#Podziały sieci:
​ - LAN (Local Area Network) - sieć niezbyt rozległa, zazwyczaj obejmuje biuro lub
dom a w jej skład wchodzi niedużo urządzeń, zarządzana z punktu jednego centralnego
​ - WAN (Wide Area Network) - rozległa na kilka niegraniczonych geograficznie
obszarów, łączy kilka sieci LAN. Sieci te zazwyczaj są zarządzane przez dostawców, którzy
się tym zajmują
​ - MAN (Metropolitan Area Network) - pomiędzy LAN i WAN, zazwyczaj obejmuje sieć
o rozmiarze miasta
​ - SAN (Storage Area Network) - dedykowana dla optymalizacji przesyłu danych
#Architektura sieci
​
- Client-server - serwer udostępnia jedną lub więcej usług lub zasobów, do jednego
lub wielu klientów. Przykładowe usługi: SMTP, FTP, WWW, Samba itd. Klient zawsze
rozpoczyna komunikację i wysyła żądania (request) o dostęp do zasobów. Serwer
odpowiada na żądanie udostępniająć żądany zasób.
#Podstawowe składniki sieci
​
- węzły - wszystko co jest podłączone do sieci np. komputer, telewizor, urządzenia
IoT


### Padriseup — strona 4

​
- medium transmisyjne - uczestniczy w przekazywaniu informacji np. skrętka lub sieć
bezprzewodowa
#Urządzenia sieciowe
​
- urządzenia końcowe - np. smartfony, PC, IoT
​
- media sieciowe - kable, fale radiowe, światłowody
​
- urządzenia pośrednie (switch, router, hub)
​
- switch - służy do przekierowywania pakietów, aby nim zarządzać trzeba
wykorzystać zdalny terminal, typy switchy:
​ * HUB - rozsyła dane wejsciowe z któregoś z portu na pozostałe,
​ * switch warstwy drugiej - używa adres MAC do przekierowania danych na
odpowiedni port, do którego urządzenie docelowe jest podpięte
​ * switch warstwy trzeciej - potrafi funkcjnować jako router, jest w stanie odczytać
docelowy adres IP
​
- router - potrafią wymieniać pakiety danych pomiędzy różymi sieciami (np. sieć
domowa i sieć globalna internet)
​
- Acess Point (AP) - łączy sieć bezprzewodową z siecią LAN
#Kabel ethernet == skrętka ethernet
​
- różne kategorie o różnych prędkościach
​ * CAT-5 - do 100Mb/s, do 100m
​ * CAT-5e - do 1Gb/s, do 100m
​ * CAT-6 - do 1Gb/s, do 100m lub 10Gb/s do 55m
​ * CAT-6a - do 10Gb/s do 100m
​ * CAT-7 - do 10Gb/s do 100m lub 100Gb/s do 50m
​
- kable:
​ * nieekranowany (UTP) - najczęściej stosowany typ kabla, 4 pary skręconych
przewodów zabieg ten niweluje zakłócenia
​ * ekranowany (STP) - kabel z ekranem wokół przewodów, eliminuje zewnętrzne
zakłócenia elektro-magnetyczne
#Mapa kabli podwodnych:


### Padriseup — strona 5

https://www.submarinecablemap.com
#Kable ethernet:
https://blog.programster.org/ethernet-cheatsheet
https://www.electronics-notes.com/articles/connectivity/ethernet-ieee-802-3/cables-types-pin
out-cat-5-5e-6.php
https://www.boston.co.uk/blog/2019/05/01/network-cables-reference-guide.aspx
#Informacja na temat budowy kabli sieciowych:
https://www.universalnetworks.co.uk/faq/what-does-utp-s-utp-ftp-stp-and-sftp-mean/
ciekawostka nt satellite tracking https://www.n2yo.com/
#IPv4 vs IPv6
https://www.netia.pl/pl/blog/ipv4-vs-ipv6-%E2%80%93-co-to-za-protokoly-i-jakie-sa-miedz
http://kti.eti.pg.gda.pl/ktilab/ipv6-adr/ipv6-adresy.pdf
https://www.soisk-me.pl/klasa-iv-sieci/klasy-adresow-ip
https://i.ytimg.com/vi/D1avGPpSJHs/maxresdefault.jpg
#Klasy adresów IP:
http://www.lomilowka.pl/upload/file/PiMLSK/klasyadres%C3%B3wIP.pdf
https://www.itbridge.pl/baza-wiedzy/adresacja-ip-publiczne-i-prywatne-adresy-ipv4
Wielkość strefy zależy od odległości między antenami i częstotliwości:
https://pl.wikipedia.org/wiki/Strefa_Fresnela
Kalkulator:
https://www.bestpartner.pl/index.php?d=kfresnel
I ciekawostka - chyba nic nie tłumi lepiej sygnału elektromagnetycznego niż drzewo liściaste
:)
Ping - używa protokołu ICMP - Internet Control Message Protocol, dosł. internetowy protokół
komunikatów kontrolnych - warstwy 3 (sieciowej).
https://pl.wikipedia.org/wiki/Internet_Control_Message_Protocol
ipconfig - komenda wyświetlająca informacje o konfiguracji interfejsów sieciowych w
windowsie. W linuxie jest ifconfig (interface config)


### Padriseup — strona 6

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
​
- IP - Internet Protocol - protokół stanowiący podstawę do wymiany danych wewnątrz
sieci
​
- DNS - Domain Name System - rozwiązywanie adresów http na adres fizyczne IP
​
- DHCP - Dynamic Host Configuration Protocol - automatyczna konfiguracja nowych
hostów w sieci
​
- HTTP - Hypertext Transfer Protocol - wykorzystywany do transferu danych
tekstowych, obrazów i innych danych które mozna umieścić na stronie internetowej
​
- HTTPS - secure implementation of HTTP - tak jak HTTP ale zapewnia szyfrowanie
danych wymiany danych pomiędzy klientem a hostem
​
- ARP - Address Resolution Protocol - protokół sieciowy umożliwiający mapowanie
logicznych adresów warstwy sieciowej (warstwa 3) na fizyczne adresy warstwy łącza danych
(2).
#Sieci bezprzewodowe
Oparte o technologie bezprzewodowe (fale radiowe). Ich rozpowrzechnienie wprowadziło
nowe zagrożenia, z powodu braku fizycznego nośnika danych (skrętka ethernetowa).
Podstawowym zabezpieczeniem było filtrowanie urządzeń na podstawie adresów MAC
(przyłączyć do sieci mogło się urządzenie z listy dozwolonych urządzeń) jednak ten sposób
zabezpieczenia jest łatwy do obejścia. Aktualnie, w dużej części, problemy z
bezpieczeństwem sieci WiFi spowodowane są poprzez błędną konfigurację.
#Typy sieci bezprzewodowych
​
- WiFi (wireless fidelity) - bazuje na standardach IEEE 802.11, używane do tworzenia
sieci LAN


### Padriseup — strona 7

​
- Wi-MAX - implementacja WiFi, aby wspierać duże obszary
​
- BLuetooth - implementacja WPAN (Wireless Personal Area Network) -
wykorzystana do parowania i komunikacji urządzeń na odległości do 100m.
#Standardy sieci WiFi
https://snipboard.io/rvm902.jpg
#Model warstwowy TCP/IP
-Warstwa aplikacji (HTTP, FTP, DNS, RDP)
-Warstwa transportowa (TCP, UDP)
-Warstwa internetu (IP)
-Warstwa dostępu do sieci (MAC)
warstwa aplikacji -> warstwa dostępu do sieci -enkapsulacja
warstwa dostępu do sieci-> warstwa aplikacji - dekapsulacja
EBCDIC
https://pl.wikipedia.org/wiki/EBCDIC
Frame Relay
https://pl.wikipedia.org/wiki/Frame_Relay
Address Types
https://www.guru99.com/types-of-ip-addresses.html
https://pmr.ii.pw.edu.pl/~pmr/ws/
Wireshark
https://www.wireshark.org/
edit>>preferences>>packet diagram
#3-way handshake
SYN -> SYN/ACK -> ACK
FIN -> FIN/ACK -> ACK
Połączenie to nosi nazwę uzgadniania trój-etapowego (ang. three-way handshake). Host
źródłowy, czyli np. klient, wysyła segment zawierający flagę SYN (SYN to flaga
synchronizacji numerów sekwencyjnych) W segmencie też zawarty jest losowy numer


### Padriseup — strona 8

sekwencyjny klienta (zwany także numerem ISN, SEQ=100) służący do późniejszego
scalania fragmentów danych.
Odbierając ten segment host docelowy, czyli np. serwer jest informowany, że klient chce
nawiązać z nim połączenie. Serwer w odpowiedzi wysyła segment z ustawioną flagą SYN i
ACK (flaga ACK informuje klienta o tym, ze serwer odebrał poprzedni segment), numerem
sekwencyjnym odebranym od klienta zwiększonym o 1 (ACK=101) oraz swoim – losowym
numerem sekwencyjnym (SEQ=300).
Na koniec klient odsyła do serwera segment z ustawioną flagą ACK potwierdzającą odbiór
poprzedniego komunikatu z numerem sekwencyjnym serwera zwiększonym o 1 (SEQ=101,
ACK=301).
●​ SYN – klient nawiązuje połączenie z segmentem, numer sekwencyjny segmenty
(segment sequence number) = n
​
* SYN-ACK – serwer odpowiada z numerem potwierdzenia (acknowledgement
number) n + 1 i numerem sekwencji m
​
* ACK – klient odpowiada z numerem sekwencji równym m + 1
SYN (synchronize)
SYN-ACK (synchronize-acknowledge)
ACK (acknowledge)
​
* FIN – jedna ze stron wysyła komunikat zakończenia
​
* ACK – druga strona potwierdza zakończenie
​
* FIN – druga strona wysyła także komunikat o zakończeniu (można
​
* połączyć z ACK)
​
* ACK – pierwsza strona potwierdza zakończenie
https://www.adminsub.net/mac-address-finder/eui
https://access.redhat.com/sites/default/files/attachments/rh_ip_command_cheatsheet_1214_
jcs_print.pdf
https://www.asus.com/pl/networking-iot-servers/whole-home-mesh-wifi-system/zenwifi-wifi-s
ystems/asus-zenwifi-ax-hybrid-xp4/

19.08.2023
Ch3 & Ch4 - Switches Fundamentals & Security


### Padriseup — strona 9

#Kompendium wiedzy na temat sieci komputerowych - dobre do uzupełnienia braków
wiedzy w danych zagadnieniach
https://sieci.infopl.info/
#Jak skutecznie uczyć się złożonych zagadnień?
https://miroslawzelent.pl/nauka/the-slight-edge-jeff-olson/
#Czym przełącznik sieciowy różni się od routera?
https://www.komputronik.pl/informacje/co-to-jest-switch-czym-przelacznik-sieciowy-rozni-sie-
od-routera/
#Typy routerów
https://community.fs.com/blog/different-types-of-routers-in-networking.html
#Typy przełączników
https://www.spiceworks.com/tech/networking/articles/what-is-network-switch/
#Most i przełącznik
https://sieci.infopl.info/index.php/urzadzenia/switch
#Typy transmisji danych
https://soisk.info/index.php/Typy_transmisji_danych:_unicast,_multicast,_broadcast
#Collision Domain
https://www.guru99.com/collision-broadcast-domain.html
#Typy kabli ethernetowych
https://www.electronics-notes.com/articles/connectivity/ethernet-ieee-802-3/cables-types-pin
out-cat-5-5e-6.php
https://www.vssmonitoring.com/types-of-ethernet-cables/
https://www.unitek-products.com/blogs/products
https://www.komputronik.pl/informacje/jaki-kabel-sieciowy-kabel-do-internetu/
#RJ45 typy T568A oraz T568B
https://cablesupply.com/rj45-ethernet-wiring-color-guides/
#Kategorie kabli sieciowych
https://blog.laptopcontrol.pl/informatyka/kategorie-kabel-sieciowy-lan-skretka/


### Padriseup — strona 10

#Topologie sieci
https://pasja-informatyki.pl/sieci-komputerowe/topologie-sieci/
#RIR
https://pl.wikipedia.org/wiki/Regional_Internet_Registry
#IPV4 vs IPV6
https://www.netia.pl/pl/blog/ipv4-vs-ipv6-%E2%80%93-co-to-za-protokoly-i-jakie-sa-miedz
#Klasy adresów IP
https://www.soisk-me.pl/klasa-iv-sieci/klasy-adresow-ip
http://www.lomilowka.pl/upload/file/PiMLSK/klasyadres%C3%B3wIP.pdf
#Maska podsieci
https://pl.wikipedia.org/wiki/Maska_podsieci
Standardy sieci WiFi
https://snipboard.io/rvm902.jpg
#Model ISO OSI
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


### Padriseup — strona 11

https://wiki.wireshark.org/CaptureFilters
https://www.wireshark.org/docs/wsug_html_chunked/
https://bugs.wireshark.org/bugzilla/attachment.cgi?id=11612
https://wiki.wireshark.org/SampleCaptures
https://wiki.wireshark.org/uploads/moin_import/attachments/SampleCaptures/dhcp.pcap
#Podstawowe komendy CISCO (IOS)
https://rioco.pl/komendy/komendy-ciscoios/
odświeżenie interfejsu
Ctrl-R - refresh
automatyczne odświeżanie interfejsu
logging synchronous
https://wiki.wireshark.org/uploads/moin_import/attachments/SampleCaptures/dns-icmp.pca
png.gz
https://ia601604.us.archive.org/20/items/cisco-packet-tracer-821-ubuntu-64bit/CiscoPacketT
racer_821_Windows_64bit.exe
configure terminal
hostname S1-Floor1
username Admin password p@nd@
show running-config
conf t
service password-encryption
exit
show running-config
copy running-config startup-config
show interfaces FastEthernet 0/1
show mac-address-table
zadanie domowe:


### Padriseup — strona 12

https://www.hackampus.com/practices/book/480/chapter/2945
chapter 3 task 3 - sprobowac w domu przerobic, jeżeli będą problemmy, zapisać pytania i
screeny na nastepne zajecia.

20.08.2023
LAB NET03-L3
Instruckja całego rozwiązania jest na HackCampus w Chapter 3->Practice tasks->Task 3
Remote Access

Telnet-TCP/23
SSH-TCP/22
Przechwycenie protokołu SSH
https://www.cloudshark.org/captures/849d3c7f09d3
LAB SSH1
hostname S1
username Admin password p@nd@
enable password c!sc0
service password-encryption
banner motd #Authorized Access only. Hacking is illegal, log out#
ip domain-name CyberPro.com
exit
wr
line vty 0 15
login local
transport input ssh
exit
interface vlan 1


### Padriseup — strona 13

ip add
ip address 10.0.0.150 255.255.255.0
no shutdown
exit
Generowanie klucza:
crypto key generate rsa
1024
S1#show ip ssh - pokaże, że ssh uruchomiono
https://beyond.hackampus.com/canvas/general/general-LLcAf-2021.12.12.10.09.23-Extra%2
0Files.rar
conf t
interface range fastEthernet 0/1-4
switchport mode access
switchport port-security
exit
S1(config)#interface fastEthernet 0/1
S1(config-if)#switchport port-security mac-address 00D0.9793.87C4
S1(config-if)#exit
S1(config)#interface fastEthernet 0/2
S1(config-if)#switchport port-security mac-address 0009.7C96.0271
S1(config-if)#exit
S1(config)#interface fastEthernet 0/3
S1(config-if)#switchport port-security mac-address sticky
S1(config-if)#exit
S1(config)#interface fastEthernet 0/4
S1(config-if)#switchport port-security mac-address sticky
S1(config-if)#exit


### Padriseup — strona 14

S1(config)#interface fastEthernet 0/1
S1(config-if)#switchport port-security violation shutdown
S1(config-if)#exit
S1(config)#interface range fastEthernet 0/2-3
S1(config-if-range)#switchport port-security violation restrict
S1(config-if-range)#exit
S1(config)#interface range fastEthernet 0/4
S1(config-if-range)#switchport port-security violation protect
S1(config-if-range)#exit
S1(config)#interface range fastEthernet 0/5-24, gigabitEthernet 0/1-2
S1(config-if-range)#shutdown
S1(config-if-range)#exit
S1>enable
S1#show port-security
S1#show port-security address
S1#show port-security interface fastEthernet 0/4
S1#show running-config
interface FastEthernet0/3
switchport mode access
switchport port-security
switchport port-security maximum 2
switchport port-security mac-address sticky
switchport port-security violation restrict
switchport port-security mac-address sticky 0004.9A8B.2832
switchport port-security mac-address sticky 0090.0C26.3CEE
S1#show port-security interface fastEthernet 0/4


### Padriseup — strona 15

Switch>enable
Switch#conf t
Switch(config)#hostname S1
S1(config)#username Admin password p@nd@
S1(config)#enable password c!sc0
S1(config)#ip ssh version 2
S1(config)#do show ip ssh

02.09.2023
https://www.cisco.com/c/en/us/support/docs/routers/7200-series-routers/12219-17.html
pliki do net-05-l2
https://beyond.hackampus.com/canvas/general/general-qji5R-2021.12.12.10.18.12-Extra%2
0FIles.rar
enable
conf t - przechodzimy w tryb konfiguracji
Router>enable
Router#conf t
Router(config)#hostname R1
R1(config)#username Admin password p@nd@
R1(config)#enable password c!sc0
R1(config)#service password-encryption
R1(config)#banner motd #Access to this device is for authorized personnel only!#
R1(config)#line console 0
R1(config-line)#login local
R1(config-line)#exit
R1(config)#exit
R1#show running-config


### Padriseup — strona 16

R1#copy running-config startup-config
Destination filename [startup-config]? --> [ENTER klawisz]
R1#conf t
R1(config)#interface gigabitEthernet 0/0
R1(config-if)#ip address 192.168.0.1 255.255.255.0
R1(config-if)#no shutdown
R1(config-if)#exit
R1(config)#interface gigabitEthernet 0/1
R1(config-if)#ip address 10.0.0.1 255.255.255.0
R1(config-if)#no shutdown
R1(config-if)#exit
R1(config)#do show ip interface brief
R1(config)#do show ip route
banner motd # Access to this device is for authorized personnel only!#
// troubleshooting nie pingujących routerów ,sprawdzamy:
R1(config)#do show ip interface brief
Interface ​
IP-Address ​ OK? Method Status ​ Protocol
GigabitEthernet0/0 ​
192.168.0.1 ​ YES manual up ​
up
GigabitEthernet0/1 ​
10.0.0.1 ​
YES manual up ​
up
GigabitEthernet0/0/0 7.7.7.1 ​
YES manual up
// troubleshooting jeżeli usunięto połączenie z routerem:
R1# show ip interface brief
Interface ​
IP-Address ​ OK? Method Status ​ Protocol
GigabitEthernet0/0 ​
192.168.0.1 ​ YES manual up ​
up
GigabitEthernet0/1 ​
10.0.0.1 ​
YES manual up ​
up
GigabitEthernet0/0/0 7.7.7.1 ​
YES manual up ​
up


### Padriseup — strona 17

Vlan1 ​unassigned ​ YES unset administratively down down
jeżeli nie ma konfiguracji/została usunięta, to tworzymy ją na nowo.
S1>enable
S1#conf t
S1(config)#interface vlan 1
S1(config-if)#ip address 192.168.0.4 255.255.255.0
S1(config-if)#no shutdown
S1(config-if)#exit
S1(config)#
S2>enable
S2#conf t
S2(config)#interface vlan 1
S2(config-if)#ip address 10.0.0.4 255.255.255.0
S2(config-if)#no shutdown
S2(config-if)#exit
S2(config)#
S2(config)#ip default-gateway 10.0.0.1
R1>enable
R1#conf t
R1(config)#ipv6 unicast-routing
R1(config)#interface gigabitEthernet 0/0
R1(config-if)#ipv6 address 2001:cafe:abcd:1::/64
R1(config-if)#exit
R1(config)#
https://www.browserling.com/tools/ip-to-bin
https://www.browserling.com/tools/bin-to-ip


### Padriseup — strona 18

https://42.pl/ipcalc/
do pobrania na następne zajęcia:
https://beyond.hackampus.com/canvas/general/general-YbaTH-2021.12.12.10.36.21-NET-0
7-L1.rar

03.09.2023
w cmd win:
route print
route add 0.0.0.0 mask 0.0.0.0 192.168.100.1 metric 1
route delete 0.0.0.0
https://beyond.hackampus.com/canvas/general/general-YbaTH-2021.12.12.10.36.21-NET-0
7-L1.rar
R1>enable
R1#show ip route
R1(config)#ip route 192.168.0.64 255.255.255.192 serial 0/0/0
R1(config)#ip route 192.168.0.128 255.255.255.192 serial 0/0/0
R1(config)#ip route 192.168.0.196 255.255.255.252 serial 0/0/0
R1(config)#do show ip route
R2(config)#ip route 192.168.0.0 255.255.255.192 192.168.0.193
R2(config)#ip route 192.168.0.128 255.255.255.192 192.168.0.198
R2(config)#exit
no ip route 192.168.0.0 255.255.255.192 192.168.0.193
no ip route 192.168.0.128 255.255.255.192 192.168.0.198
R3#conf terminal
R3(config)#ip route 192.168.0.0 255.255.255.192 ser
R3(config)#ip route 192.168.0.0 255.255.255.192 serial 0/0/1
R3(config)#ip route 192.168.0.64 255.255.255.192 serial 0/0/1


### Padriseup — strona 19

R3(config)#ip route 192.168.0.192 255.255.255.252 serial 0/0/1
R3(config)#exit
R3#show ip route
PC2=192.168.0.66
PC3=192.168.0.130
ping 192.168.0.194
sprawdzić czy widzi router
R1(config)#ip route 192.168.0.64 255.255.255.192 serial 0/0/0
R1(config)#ip route 192.168.0.128 255.255.255.192 serial 0/0/0
R1(config)#ip route 192.168.0.196 255.255.255.252 serial 0/0/0
R1(config)#do show ip route
R1>enable
R1#conf t
R1(config)#ip route 0.0.0.0 0.0.0.0 serial 0/0/0
R2#conf t
R2(config)#ip route 0.0.0.0 0.0.0.0 serial 0/1/0
R2(config)#do show ip route static
R3>enable
R3#conf t
Enter configuration commands, one per line. End with CNTL/Z.
R3(config)#ip route 0.0.0.0 0.0.0.0 serial 0/0/1
R3(config)#do show ip route static
https://beyond.hackampus.com/canvas/general/general-LJUoB-2021.12.12.10.39.31-Extra%
20Files.rar
https://ipwithease.com/ospf-timers/
R1#enable
R1#conf t


### Padriseup — strona 20

Enter configuration commands, one per line. End with CNTL/Z.
R1(config)#router rip
R1(config-router)#version 2
R1(config-router)#no auto-summary
R1(config-router)#network 172.16.0.0
R1(config-router)#network 172.16.0.8
R1(config-router)#network 192.168.10.0
R1(config-router)#passive-interface gigabitEthernet 0/0
R1(config-router)#exit
R1(config)#
R1>en
R1#conf t
R1(config)#router rip
R1(config-router)#version 2
R1(config-router)#no auto-summary
R1(config-router)#network 172.16.0.0
R1(config-router)#network 172.16.0.8
R1(config-router)#network 192.168.10.0
R1(config-router)#passive-interface gigabitEthernet 0/0
R1(config-router)#exit
R1(config)#exit
R1#copy running-config startup-config
Destination filename [startup-config]? ​
<KLAWISZ ENTER
Building configuration...
[OK]
R1#


### Padriseup — strona 21

R2>en
R2#show ip route connected
C 172.16.0.0/30 is directly connected, Serial0/3/0
C 172.16.0.4/30 is directly connected, Serial0/3/1
C 192.168.20.0/24 is directly connected, GigabitEthernet0/0
R2#conf t
R2(config)#router rip
R2(config-router)#version 2
R2(config-router)#no auto-summary
R2(config-router)#network 172.16.0.0
R2(config-router)#network 172.16.0.4
R2(config-router)#network 192.168.20.0
R2(config-router)#passive-interface gigabitEthernet 0/0
R2(config-router)#exit
R2(config)#exit
R2#copy running-config startup-config
Destination filename [startup-config]? ​
<KLAWISZ ENTER
Building configuration...
[OK]
R2#
R3>en
R3#show ip route connected
C 172.16.0.4/30 is directly connected, Serial0/3/1
C 172.16.0.8/30 is directly connected, Serial0/3/0
C 192.168.30.0/24 is directly connected, GigabitEthernet0/0
C 210.10.10.0/30 is directly connected, Serial0/2/0


### Padriseup — strona 22

R3#conf t
Enter configuration commands, one per line. End with CNTL/Z.
R3(config)#router rip
R3(config-router)#version 2
R3(config-router)#no auto-summary
R3(config-router)#network 172.16.0.4
R3(config-router)#network 172.16.0.8
R3(config-router)#network 192.168.30.0
R3(config-router)#network 210.10.10.0
R3(config-router)#no auto-summary
R3(config-router)#passive-interface gigabitEthernet 0/0
R3(config-router)#exit
R3(config)#exit
R3#copy running-config startup-config
Destination filename [startup-config]? ​
<KLAWISZ ENTER
Building configuration...
[OK]
R3#show ip route rip
R3>enable
R3#conf t
R3(config)#ip route 0.0.0.0 0.0.0.0 serial 0/2/0
R3(config)#exit
R3#show ip route
Codes: L - local, C - connected, S - static, R - RIP, M - mobile, B - BGP
​
D - EIGRP, EX - EIGRP external, O - OSPF, IA - OSPF inter area
​
N1 - OSPF NSSA external type 1, N2 - OSPF NSSA external type 2


### Padriseup — strona 23

​
E1 - OSPF external type 1, E2 - OSPF external type 2, E - EGP
​
i - IS-IS, L1 - IS-IS level-1, L2 - IS-IS level-2, ia - IS-IS inter area
​
* - candidate default, U - per-user static route, o - ODR
​
P - periodic downloaded static route
Gateway of last resort is 0.0.0.0 to network 0.0.0.0 ​ << SPRAWDZIC
R3>enable
R3#conf t
R3(config)#ip route 0.0.0.0 0.0.0.0 serial 0/2/0
R3(config)#exit
R3#show ip route
Codes: L - local, C - connected, S - static, R - RIP, M - mobile, B - BGP
​
D - EIGRP, EX - EIGRP external, O - OSPF, IA - OSPF inter area
​
N1 - OSPF NSSA external type 1, N2 - OSPF NSSA external type 2
​
E1 - OSPF external type 1, E2 - OSPF external type 2, E - EGP
​
i - IS-IS, L1 - IS-IS level-1, L2 - IS-IS level-2, ia - IS-IS inter area
​
* - candidate default, U - per-user static route, o - ODR
​
P - periodic downloaded static route
Gateway of last resort is 0.0.0.0 to network 0.0.0.0 ​ << SPRAWDZIC
R3#
R3#conf t
R3(config)#router rip
R3(config-router)#default-information originate
R3(config-router)#exit
R3(config)#
https://www.ciscopress.com/articles/article.asp?p=2294214&seqNum=2
R0#conf t


### Padriseup — strona 24

R0(config)#router ospf 1
R0(config-router)#router-id 1.1.1.0
R0(config-router)#network 192.168.0.0 0.0.0.255 area 0
R0(config-router)#network 172.16.0.0 0.0.0.3 area 0
R0(config-router)#network 172.16.0.8 0.0.0.3 area 0
R0(config-router)#auto-cost reference-bandwidth 1000
R0(config-router)#passive-interface gigabitEthernet 0/1
R0(config-router)#exit
R0(config)#exit
R0#
R1>en
R1#conf t
R1(config)#router ospf 1
R1(config-router)#router-id 1.1.1.1
R1(config-router)#network 192.168.1.0 0.0.0.255 area 0
R1(config-router)#network 172.16.0.4 0.0.0.3 area 0
R1(config-router)#network 172.16.0.8 0.0.0.3 area 0
R1(config-router)#auto-cost reference-bandwidth 1000
R1(config-router)#passive-interface gigabitEthernet 0/1
R1(config-router)#exit
R1(config)#exit
R1#
R2>en
R2#conf t
R2(config)#router ospf 1
R2(config-router)#router-id 1.1.1.2


### Padriseup — strona 25

R2(config-router)#network 192.168.2.0 0.0.0.255 area 0
R2(config-router)#network 172.16.0.4 0.0.0.3 area 0
R2(config-router)#network 172.16.0.0 0.0.0.3 area 0
R2(config-router)#auto-cost reference-bandwidth 1000
R2(config-router)#passive-interface gigabitEthernet 0/1
R2(config-router)#exit
R2(config)#
R2(config)#exit
R2#show ip route ospf
​
172.16.0.0/16 is variably subnetted, 5 subnets, 2 masks
O ​
172.16.0.8 [110/2] via 172.16.0.6, 00:02:08, GigabitEthernet0/1/0
​
[110/2] via 172.16.0.1, 00:02:08, GigabitEthernet0/0/0
O​
192.168.0.0 [110/2] via 172.16.0.1, 00:02:08, GigabitEthernet0/0/0
O​
192.168.1.0 [110/2] via 172.16.0.6, 00:02:08, GigabitEthernet0/1/0

https://pasja-informatyki.pl/sieci-komputerowe/
https://42.pl/ipcalc/
https://beyond.hackampus.com/canvas/general/general-1izuf-2021.12.12.10.42.45-NET-09-
L1.rar
S2#conf t
S2(config)#vlan 10
S2(config-vlan)#name Workstation
S2(config-vlan)#exit
S2(config)#vlan 20
S2(config-vlan)#name Servers
S2(config-vlan)#exit
S2(config)#do show vlan brief


### Padriseup — strona 26

F0/1-4 VLAN10
F0/5-6 VLAN20
S2(config)#interface range fastEthernet 0/1-4
S2(config-if-range)#switchport mode access
S2(config-if-range)#switchport access vlan 10
S2(config-if-range)#exit
S2(config)#interface range fastEthernet 0/5-6
S2(config-if-range)#switchport mode access
S2(config-if-range)#switchport access vlan 20
S2(config-if-range)#exit
S2(config)#do show vlan brief
Polaczenia fizyczne dla switcha S1
F0/1-2 VLAN10 (stacje robocze)
F0/3 VLAN20 (serwer)
S1>enable
S1#conf t
S1(config)#vlan 10
S1(config-vlan)#name Workstation
S1(config-vlan)#exit
S1(config)#vlan 20
S1(config-vlan)#name Servers
S1(config-vlan)#exit
S1(config)#interface range fastEthernet 0/1-2
S1(config-if-range)#switchport mode access
S1(config-if-range)#switchport access vlan 10
S1(config-if-range)#exit


### Padriseup — strona 27

S1(config)#interface fastEthernet 0/3
S1(config-if)#switchport mode access
S1(config-if)#switchport access vlan 20
S1(config-if)#exit
S1(config)#do show vlan brief
10.0.0.0 255.255.255.0
10.0.0.254
192.168.0.0 255.255.255.0 - Serwery
10.0.0.0 255.255.255.0 ​
- Komputery
ostatni adres w sieci to brama domyslna
10.0.0.1
255.255.255.0
10.0.0.254
192.168.0.1
255.255.255.0
192.168.0.254
192.168.0.0 255.255.255.0 zakres sieci i ostatni adres to brama
S1>enable
S1#conf t
S1(config)#interface range gigabitEthernet 0/1-2
S1(config-if-range)#switchport mode trunk
S1(config-if-range)#
%LINEPROTO-5-UPDOWN: Line protocol on Interface GigabitEthernet0/1, changed state to
down
%LINEPROTO-5-UPDOWN: Line protocol on Interface GigabitEthernet0/1, changed state to
up
S1(config-if-range)#exit


### Padriseup — strona 28

do show interfaces switchport
S2>en
S2#conf t
S2(config)#interface gigabitEthernet 0/1
S2(config-if)#switchport mode trunk
S2(config-if)#exit
S2(config)#vlan 30
S2(config-vlan)#name Native
S2(config-vlan)#exit
S2(config)#interface gigabitEthernet 0/1
S2(config-if)#switchport trunk native vlan 30
S2(config-if)#exit
S1#copy running-config startup-config
S2#copy running-config startup-config
do copy running-config startup-config
R1>enable
R1#conf t
R1(config)#interface gigabitEthernet 0/0
R1(config-if)#no shutdown
R1(config-if)#exit
https://beyond.hackampus.com/canvas/general/general-NVfKC-2021.12.12.11.25.45-NET-11
-L1.rar
R2>enable
R2#conf terminal
R2(config)#ip access-list standard 1
R2(config-std-nacl)#exit
R2(config)#access-list 1 deny 172.16.2.0 0.0.0.255


### Padriseup — strona 29

R2(config)#access-list 1 permit any
R2(config)#interface gigabitEthernet 0/0
R2(config-if)#ip access-group 1 out
R2(config-if)#exit
R1>enable
R1#configure terminal
R1(config)#ip access-list standard BLOCK_HOST
R1(config-std-nacl)#deny host 192.168.2.1
R1(config-std-nacl)#permit any
R1(config-std-nacl)#exit
R1(config)#interface gigabitEthernet 0/0
R1(config-if)#ip access-group BLOCK_HOST out
R1(config-if)#exit
R1(config)#do show access-list
R2>enable
R2#conf t
R2(config)#ip access-list extended 100
R2(config-ext-nacl)#exit
R2(config)#access-list 100 deny ip host 172.16.2.1 host 192.168.1.2
R2(config)#access-list 100 permit ip any any
R2(config)#interface gigabitEthernet 0/1
R2(config-if)#ip access-group 100 in
R2(config-if)#exit
R2(config)#do show access-list
R1(config)#ip access-list extended BLOCK_HTTP
R1(config-ext-nacl)#deny tcp host 192.168.1.2 host 172.16.1.2 eq 80


### Padriseup — strona 30

R1(config-ext-nacl)#permit ip any any
R1(config-ext-nacl)#exit
R1(config)#interface gigabitEthernet 0/0
R1(config-if)#ip access-group BLOCK_HTTP in
R1(config-if)#exit
R1(config)#do show access-list
