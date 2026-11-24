# Wireless technologies

[← Indeks wiki](../index.md)

> **Źródło główne:** Computer Networking Textbook.pdf, s. 25–28. Treść została uporządkowana tematycznie; pełny ekstrakt źródłowy znajduje się w `_source-archive/`.


## Materiał kanoniczny

Wireless networks for computer communication are possible.
Wireless media features better flexibility than wired media, due to the absence of
cables connected to end devices.
Information is transmitted using radio frequencies, which, however, does pose some
security challenges.
8
om \
0 \ -ao
i) o
H
Re i) ‘
* i) 2»
. \ -
ey 1 ”
x i) Fal
By, 1 rai
~*~
| 7 |
Besse 5
Wireless Network
Security Issues
Coverage Area - The ideal environment for this technology is open space.
Some building materials can limit the range that wireless systems cover.
Transmission Interference - Many common devices, such as microwave ovens and
wireless communication devices, also transmit radio frequencies.
Signals from such equipment may interfere with signals transmitted in a wireless
network, and affect their quality.
Security - The absence of physical media exposes the network to the public and allows
others to discover it and try to gain access to it, without authorization to do so.

Shared Medium - The technology operates in half-duplex, which means only one device
can send and receive information at a time.
When more and more users connect to the network, the available bandwidth for each
user will decrease accordingly.
Wireless LAN Components
AP - Access Point is the component that allows end devices to connect to a network
wirelessly using radio waves. The access point itself will be connected to the network
via cable.
Wireless NIC Adapter - For a device to connect to a wireless network, it must have a
wireless NIC adapter to send and receive the information.
Wireless NIC adapters can either be an external device or integrated in the computer.
Wireless Technologies
Wi-Fi - Wi-Fi (Wlreless Fidelity) is a technology based on IEEE 802.11 standards that
allows wireless connection to a network via radio waves.
Wi-Fi is used for LAN networks in shared spaces.
Wi-MAX - Wi-MAX is an implementation of a wireless network connection over a wide
area. It is used for LAN and MAN implementations.
Bluetooth - Bluetooth is an implementation of WPAN (Wireless Personal Area
Network). It is mainly used to pair devices and allows communication at up to 100
meters.

Wireless Standards
Over the years, network standards were developed and modified to improve speed and
bandwidth.
Wireless Standard History:
BACKWARD
STANDARD MAX SPEED FREQUENCY
COMPATIBLE
802.11a 54 Mb/s 5 GHz No
802.11b 11 Mb/s 2.4 GHz No
802.11g 54 Mb/s 2.4 GHz 802.11a
802.11n 600 Mb/s 2.4 GHz & 5 GHz 802.11a/b/g
802.11ac 1.3 Gb/s 5 GHZ 802.11a/n
802.11ax 14 Gb/s* 1 GHz - 7.125 GHz 802.11a/b/g/n/ac

Media Comparison
Copper Fiber Wi-Fi
10 Mb/s - 10 Gb/s 10 Mb/s - 100 Gb/s 54 Mb/s - 14 Gb/s
D d th
Up to 100 meters Up to 100 Km epen on e
transmitter’s strength
Cheap Expensive Relatively cheap
Vulnerable to the effects Expensive equipment The signal can be affected
of EMI and RFI and less flexibility by local structures

## Powiązane laboratoria

- Brak bezpośrednio przypisanego laboratorium w zestawie.


## Uzupełnienia z notatek Riseup / zajęć

<details>
<summary>Pokaż notatki prowadzącego, dodatkowe komendy i linki powiązane z tym tematem</summary>

https://www.itbridge.pl/baza-wiedzy/adresacja-ip-publiczne-i-prywatne-adresy-ipv4
Wielkość strefy zależy od odległości między antenami i częstotliwości:
https://pl.wikipedia.org/wiki/Strefa_Fresnela
Kalkulator:
https://www.bestpartner.pl/index.php?d=kfresnel
I ciekawostka - chyba nic nie tłumi lepiej sygnału elektromagnetycznego niż drzewo liściaste

---

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

- WiFi (wireless fidelity) - bazuje na standardach IEEE 802.11, używane do tworzenia
sieci LAN

- Wi-MAX - implementacja WiFi, aby wspierać duże obszary

- BLuetooth - implementacja WPAN (Wireless Personal Area Network) -
wykorzystana do parowania i komunikacji urządzeń na odległości do 100m.
#Standardy sieci WiFi
https://snipboard.io/rvm902.jpg
#Model warstwowy TCP/IP
-Warstwa aplikacji (HTTP, FTP, DNS, RDP)

---

https://access.redhat.com/sites/default/files/attachments/rh_ip_command_cheatsheet_1214_
jcs_print.pdf
https://www.asus.com/pl/networking-iot-servers/whole-home-mesh-wifi-system/zenwifi-wifi-s
ystems/asus-zenwifi-ax-hybrid-xp4/

19.08.2023
Ch3 & Ch4 - Switches Fundamentals & Security

---

#Maska podsieci
https://pl.wikipedia.org/wiki/Maska_podsieci
Standardy sieci WiFi
https://snipboard.io/rvm902.jpg
#Model ISO OSI
https://pasja-informatyki.pl/sieci-komputerowe/model-tcp-ip-iso-osi/

</details>

## Powiązane tematy

- [Network media and cabling](network-media-cabling.md)
- [Network types and devices](network-types-devices.md)

## Źródła w zestawie

- `Computer Networking Textbook.pdf` — strony 25–28.
- `Computer Networking.pdf` — prezentacja kursowa; odpowiadający rozdział zachowany w `_source-archive/02-Course-Slides.md`.
- `Padriseup Computer Networking.pdf` — uzupełnienia i materiały dodatkowe, jeśli występowały dla tego tematu.
