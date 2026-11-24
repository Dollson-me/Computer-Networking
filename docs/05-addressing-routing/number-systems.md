# Number systems

[← Indeks wiki](../index.md)

> **Źródło główne:** Computer Networking Textbook.pdf, s. 93–97. Treść została uporządkowana tematycznie; pełny ekstrakt źródłowy znajduje się w `_source-archive/`.


## Materiał kanoniczny

Decimal - The most common numbering system consists of ten numbers, 0-9, and it is
called the decimal system. The system is based on the 10 fingers we use to count and is
known as the base-10 numeral system.
Binary - Binary is an alternative number system that consists of only two numbers: 0
and 1. This system is used by computers, which communicate by modulating electrical
currents. Because there are only two numbers, the system is known as the base-2
numeral system.
Hexadecimal - Hex, or Hexadecimal, is a number system that consists of 16 characters
and is known as the base-16 numeral system. Hex uses the numbers 0-9, followed by
the letters A-F. Hex is widely used as an alternative representation to binary, since it is a
more human-oriented system.
Positional Notation
When learning about number systems, a good way to approach them is to consider
numbers a result of their positions.
Each number’s value can be calculated as a result of a function.
The function is the same regardless of the base being used, making it easier to perform
base transitions.
The function is: [number] = [digit] * [base] “ [position].

The Digits: 1 (2) 1. 1
02 The Positions: 2 22 21 2°
Base2 The Result: 8 (2) 2 1
The Digits: 1 (2) 2 4
10 The Positions: 103 102 10 16!
Base10 The Result: 1000 @ 20 4
The Digits: B a. (2) 5
16 The Positions: 16 162, 161 16°
Basel6 The Result: 45056 256 2) 5
Positional Conversion
Binary to Decimal
After the Positional Notation method is used to map a number’s value, the positional
value of each digit can be found. The next step is conversion, summarizing each of the
individual values to get the result.
Conversion Formula:
Positional Value 128 64 32 16 8 4 2 1
Binary value 1 i 0 1 0 1 0 0
Calculation 1x128 1x64 0x32 1x16 Ox8. 1x4 Ox2 Ox1
Final Value 128 64 0 16 0 4 0 i)
Decimal value of 128+64+0+16+0+4+0+0-212
the binary value Eres]

Decimal to Binary
While the aim of conversion to decimal is to solve a formula, the aim of conversion
from decimal is to find the missing variable.
The operation can be summed up as find the X that will result in the closest number.
For example, when converting the number 1994 to binary, the first step is to find X,
where 2* is the closest to 1994.
Continuing this process, the number should be written down and the calculation should
be repeated for the remainder.
1994 : 120
1024 8
970 2
512 2
458 ) (4)
256
— 32 16 8 4 2 1
202 4 ——
“4128 0 0 1 0 4: 0
74 Z +
= 2048 1024 512 256 128 64
64
10 ) 1 1 1 oe 1
Decimal to Binary Positional Conversion
Calculation Tricks
For binary, there are some tricks that can make the calculation easier, instead of having
to guess.
One trick is to take the desired number and divide it, without the remainder, while
recording each operation.
If the result is even, write a O. If it is odd, write a 1. The binary representation will
appear when the operations are done.

For other bases, there are other tricks and mathematical methods.
——~ £€£~ -—~ 2 —
62. 124 249 498 $97 1994
— 2 <— —
al 3 . 15 31,
111110010180
Division Calculation
Binary to Hexadecimal
Because 16 is technically 2*, conversion from base-2 to base-16 is rather easy. Each
hexadecimal digit can be considered a representation of 4 binary digits. For example,
101110 is 0010 + 1110, making it 2E in hexadecimal.
Binary to Hexadecimal Conversion Formula:
Number 0 1 2 3 4 5 6 7
Binary 0000 0001 0010 0011 0100 0101 0110 0111
Hexadecimal 0 1 2 | 3 4 | 5 6 | 7
Number 8 9 10 11 12 13 14 15
Binary 1000 1001 1010 1011 1100 1101 1110 1111
Hexadecimal 8 | 9 A | B c | D | E F

Hexadecimal Conversion
Here is how binary is converted to hex, with an example.
Conversion steps:
e Divide the binary number into groups of 4 digits.
© Convert each group to its equivalent hex value using the Base Comparison table.
e Merge the results of each group.
Conversion example: Convert 0111111111010100 to Hex
e 0111 1111 1101 0100
e 0111=7,1111 =F, 1101 =D, 0100 =4
e Answer is 7FD4
Other Bases
There are other bases besides binary, decimal, and hexadecimal.
Throughout history, other counting systems, such as base-6, base-8, and base-12 were
developed.
Old British measurements, such as dozen (12), gross (144), and feet (12 inches) are
suspected to have been originated by a base-12 number system.
Most of those bases are no longer in use today.
Z Lab — Converting Decimal, Binary, and Hex
—=/ | Understand numbering systems and how to convert among them.
m=:
Perform the instructions in lab document Net-05-L1.

## Powiązane laboratoria

- [NET-05-LS1](../labs/net-05-ls1.md)

## Powiązane tematy

- [IPv4 addressing](ipv4.md)
- [IPv6 addressing](ipv6.md)
- [Subnetting](subnetting.md)

## Źródła w zestawie

- `Computer Networking Textbook.pdf` — strony 93–97.
- `Computer Networking.pdf` — prezentacja kursowa; odpowiadający rozdział zachowany w `_source-archive/02-Course-Slides.md`.
- `Padriseup Computer Networking.pdf` — uzupełnienia i materiały dodatkowe, jeśli występowały dla tego tematu.
