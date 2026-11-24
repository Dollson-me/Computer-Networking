# NET-05-LS1 — Converting Decimal, Binary, and Hex

[← Wszystkie laboratoria](index.md)

> **Typ:** laboratorium z rozwiązaniem. Zachowano wszystkie kroki, pytania, odpowiedzi, komendy i wartości z materiału źródłowego; usunięto jedynie techniczne nagłówki stron OCR.

## Powiązana teoria

- [Number systems](../05-addressing-routing/number-systems.md)

## Pełny przebieg laboratorium

> Zakres źródłowy: strony 124–130.

Computer Networking
Lab Assignment IP & Routing
& Solution Concepts
°. an NET-05-LS1
al U Converting Decimal,
Binary, and Hex
Copyright © 1996-2020 HackerU Ltd.
All Rights Reserved.

Note: Solutions for the instructor are shown inside the green box.
@ Lab Objective
Understand the difference between binary, decimal, and hexadecimal number systems
and how to convert values among them.
4 Lab Mission
Use practice questions to evaluate and convert values among the numbering systems.
esa 7
©) Lab Duration
30-45 minutes
fe Requirements
e@ Basic understanding of the decimal (base 10) numbering system.
e Basic understanding of the hexadecimal (base 16) numbering system.
e@ Basic understanding of the binary (base 2) numbering system.
oo
| Resources
e Environment & Tools
o Optional: Calculator

Lab Task 1: Decimal and Binary
Understand how decimal numbering relates to binary.
Part 1: Convert Decimal to Binary
1. Which mathematical base does the binary system use, and which digits represent
it?
Base 2, two digits: 0 and 1
2 Whatisa bit?
A bit (binary digit) is the smallest unit of data in a computer. A bit has a single binary
value, either 0 or 1.
3. Whatis an octet?
8-bit string (IPv4 consists of four octets).
4 Convert the following decimal digits to a binary octet.
Pe joys ts fe fe fe fe
aE
Example: 56 in binary octet:
a) 26
b) 65
c) 91
d) 151
e) 168
f) 192
g) 254
26 = 00011010

65 = 01000001
91 = 01011011
151 = 10010111
168 = 10101000
192 = 11000000
254 = 11111110
Part 2: Convert Binary to Decimal
5 Convert the following IPv4 binary octets to decimal digits:
Example: 00000010 in decimal is 2.
a) 00000111
b) 00010010
c) 00101110
d) 01011111
e) 10010010
f) 11011110
g) 11111111
a. 7
b. 18
c. 46
d. 95
e. 146
£222
g. 255
6 Bonus: Convert the following IPv4 addresses to their binary equivalents:
Example: 10.0.0.5 is actually a long 32-bit string.
[oe inary
10.0.0.5 | 00001010.00000000.00000000.00000101

a) 172.16.10.2
b) 192.168.1.1
c) 8.8.8.8
a. 172.16.10.2 = 10101100.00010000.00001010.00000010
b. 192.168.1.1 = 11000000.10101000.0000001.0000001
c. 8.8.8.8 = 00001000.00001000.00001000.00001000

Lab Task 2: Binary and Hexadecimal
Understand how binary relates to hexadecimal numbering.
Part 1: Convert Binary to Hex
1 Which mathematical base does the hexadecimal system use, and which digits
represent it?
Base 16, 10 digits and 6 characters: 0-9, A, B, C, D, E, F
2 Convert the following binary nibbles (half-bytes) to hex digits:
Example: 1010 is A
a) 0010
b) 1101
c) 0110
d) 1100
e) 1000
f) 1011
g) 0000
h) 1110
i) 1111
a. 2
b. D
c. 6
dc
e. 8
f. B
g. O
h. E
i. F

Part 2: Convert Hex to Binary
3 The following is a random physical address of 12 decimal digits (MAC).
Convert the hexadecimal digits to binary digits:
Example: 00-B1-17-C2-A2-EE is represented in binary as follows:
Px a
|B [af] [2/o/e fol
7 [ofoe tafe] fala
| [2[{o[ofo]e|ato
[#2 [2/0] [o//e/alo
eer
a) B3-00-13-A1-02-3E
[Hex| Binary
[83 [1] o[1{1folofa) 4)
[00 [oj ofofofolafojo|
|.13 [ol ofo[1]olo} 1) 4/
[az [1/0/21 [olololo|.|
[02 [o|ofofofololso|
L3e [ofofa|1]1]2[1]o]
b) 04-01-0A-DD-CC-FF
[Hex[ Binary |
[04 [ol ofofofol1fofo|
[01 [ol ofofofolofojs|
[oa [ol ofofolslofajo|
[po [1/10] 11/10] 4]
[cc [1] 1{ofo]1[1]o/o|
