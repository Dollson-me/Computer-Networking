# Protocols, ports and layers

[← Indeks wiki](../index.md)

## Najczęściej używane protokoły z materiałów

| Protokół | Rola | Warstwa / model | Port(y) z materiałów |
|---|---|---|---|
| IP | adresowanie i dostarczanie pakietów między sieciami | OSI L3 / TCP-IP Internet | — |
| ICMP | komunikaty kontrolne i diagnostyka (`ping`) | OSI L3 | — |
| ARP | mapowanie IPv4 → MAC w LAN | między L2/L3 | — |
| TCP | transport połączeniowy i niezawodny | OSI L4 | zależne od aplikacji |
| UDP | transport bezpołączeniowy | OSI L4 | zależne od aplikacji |
| HTTP | WWW, tekst i inne zasoby | aplikacja | TCP/80 |
| HTTPS | HTTP z szyfrowaniem TLS/SSL | aplikacja | TCP/443 |
| DNS | nazwa ↔ adres IP | aplikacja | UDP/53 |
| DHCP | automatyczna konfiguracja hostów | aplikacja | UDP/67,68 |
| SMTP | wysyłanie poczty | aplikacja | TCP/25 |
| POP3 | odbiór poczty | aplikacja | TCP/110 |
| SSH | szyfrowany zdalny CLI | aplikacja | TCP/22 |
| Telnet | nieszyfrowany zdalny CLI | aplikacja | TCP/23 |
| FTP | transfer plików | aplikacja | TCP/20,21 |
| TFTP | prosty transfer plików | aplikacja | UDP/69 |
| RDP | zdalny pulpit | aplikacja | TCP/3389 |
| SMB | udostępnianie zasobów | aplikacja | TCP/445 |
| NTP | synchronizacja czasu | aplikacja | UDP/123 |
| RIP | routing distance-vector | warstwa sieci | — |
| OSPF | routing link-state | warstwa sieci | — |
| CDP | odkrywanie urządzeń Cisco | L2 | — |
| LLDP | vendor-neutral discovery | L2 | — |

## Zakresy portów logicznych

- **Well-known:** 0–1023.
- **Registered:** 1024–49151.
- **Dynamic / Private:** 49152–65535.

## TCP flags

- `SYN` — synchronizacja i inicjowanie połączenia.
- `ACK` — potwierdzenie odbioru.
- `RST` — reset połączenia.
- `FIN` — żądanie zakończenia.
- `PSH` — natychmiastowe przekazanie buforowanych danych.
- `URG` — dane oznaczone jako pilne.

Szczegóły: [TCP, UDP, ports and sessions](../02-models-protocols/transport-ports.md).
