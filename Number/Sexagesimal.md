---
title: Sexagesimal
type: concept
status: canonical
provenance: ai-synthesis (standard history of Babylonian mathematics; tables computed and checked exactly) + murphy (the point about $\tfrac17$)
sources: "[[SRC Confession of Mathematics (2023-24)]]"
updated: 2026-10-07
---

# Sexagesimal

*The stance behind the system (engineering mathematics, regular and irregular, the field that matters): [[Babylonian Mathematics]].*

The Babylonian number system: a **positional system in base 60**. It descends from the Sumerians and was in full use in Mesopotamia by the Old Babylonian period (about 2000–1600 BC). It is among the earliest known place-value systems, and the one in which Babylonian arithmetic and astronomy were done. Its remnants are the 60 minutes of an hour and the 60 seconds of a minute.

*Note:* The historical statements below are standard but have not been checked against sources here. The tables were computed and verified exactly.

## Writing numbers

**Digits.** Each place holds a number from $0$ to $59$, written in cuneiform by two wedge signs used additively: a vertical wedge for $1$ (repeated up to nine times) and a corner wedge for $10$ (repeated up to five times). So $47$ is four corner wedges and seven vertical wedges.

**Place value.** The digits are written left to right, each place worth $60$ times the one to its right, just as in our decimal numerals:

$$1,24,51,10\;=\;1\cdot60^3+24\cdot60^2+51\cdot60+10.$$

**Modern notation.** Scholars write the digits separated by commas and mark the sexagesimal point with a semicolon: $1;24,51,10=1+\dfrac{24}{60}+\dfrac{51}{60^2}+\dfrac{10}{60^3}$. The Babylonians themselves wrote neither commas nor a point.

- **No point.** The scribes did not mark where the integer part ends. $1$, $60$ and $\tfrac1{60}$ are written the same; the size is read from context. The system is *floating*, like scientific notation with the exponent left unwritten.
- **Zero.** In the early texts an empty place is simply a gap. A separate sign for an empty place (two slanted wedges) appears only late. It is a placeholder inside a numeral, not a number you could add: [[Counting and Bases]] treats zero as a separate leap.

## Why sixty

$60=2^2\cdot3\cdot5$ has twelve divisors ($1,2,3,4,5,6,10,12,15,20,30,60$). So the fractions $\tfrac12,\tfrac13,\tfrac14,\tfrac15,\tfrac16,\tfrac1{10},\tfrac1{12},\dots$ all have **finite** expansions. The rule: $\tfrac1n$ terminates in base $b$ exactly when every prime factor of $n$ divides $b$. Decimal manages only $2$ and $5$; base 60 adds $3$.

## Multiplication

Babylonian scribes multiplied from memorized **tables of multiples**, one for each principal number. The product of two single-place numbers is read from the table, then the places are added with carries in base 60. All products up to $10\times10$:

| × | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 |
|---|---|---|---|---|---|---|---|---|---|---|
| **1** | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 |
| **2** | 2 | 4 | 6 | 8 | 10 | 12 | 14 | 16 | 18 | 20 |
| **3** | 3 | 6 | 9 | 12 | 15 | 18 | 21 | 24 | 27 | 30 |
| **4** | 4 | 8 | 12 | 16 | 20 | 24 | 28 | 32 | 36 | 40 |
| **5** | 5 | 10 | 15 | 20 | 25 | 30 | 35 | 40 | 45 | 50 |
| **6** | 6 | 12 | 18 | 24 | 30 | 36 | 42 | 48 | 54 | 1,0 |
| **7** | 7 | 14 | 21 | 28 | 35 | 42 | 49 | 56 | 1,3 | 1,10 |
| **8** | 8 | 16 | 24 | 32 | 40 | 48 | 56 | 1,4 | 1,12 | 1,20 |
| **9** | 9 | 18 | 27 | 36 | 45 | 54 | 1,3 | 1,12 | 1,21 | 1,30 |
| **10** | 10 | 20 | 30 | 40 | 50 | 1,0 | 1,10 | 1,20 | 1,30 | 1,40 |

Each entry is a sexagesimal numeral: $1,3$ means $1\cdot60+3=63$, and $1,40$ means $100$. Products of $60$ or more ($6\times10$, $7\times9$, $7\times10$, $8\times8$ and up) need two places.

Example: $25\times36$. Since $25\times36=900=15\cdot60$, the answer is $15,0$.

## Division is multiplication by a reciprocal

There was no separate division algorithm. To divide by $n$, multiply by $1/n$, which is read from a **table of reciprocals**. The standard tables list only the **regular** numbers: those whose reciprocal terminates, i.e. $2^a3^b5^c$. Those up to $59$ are

$$1, 2, 3, 4, 5, 6, 8, 9, 10, 12, 15, 16, 18, 20, 24, 25, 27, 30, 32, 36, 40, 45, 48, 50, 54.$$

That is 25 of the first 59 numbers (counting $1$). The others, $7,11,13,14,\dots$ are **irregular**; their reciprocals do not terminate and the standard tables omit them. In base 60, $\tfrac17$ is $0;\overline{8,34,17}$: the digits $8,34,17$ repeat forever. The Babylonians could see this and wrote the first few places ("who is even chopping stuff up into 216,000 pieces?") and stopped. They knew which divisions their system could perform exactly and which it could only approach. See [[Counting and Bases]], [[Equal Signs]].

## Reciprocals of $1$ through $59$

The sexagesimal expansion of $1/n$. A bar marks the digits that repeat forever; "leading digits" are those before the repetition starts. The period of $1/n$ is how long the repeating block is. All were verified by summing the digits back to $1/n$.

| $n$ | $1/n$ | kind |
|---|---|---|
| 1 | $1$ | — |
| 2 | $0;30$ | regular (terminates) |
| 3 | $0;20$ | regular (terminates) |
| 4 | $0;15$ | regular (terminates) |
| 5 | $0;12$ | regular (terminates) |
| 6 | $0;10$ | regular (terminates) |
| 7 | $0;\overline{8,34,17}$ | period 3 |
| 8 | $0;7,30$ | regular (terminates) |
| 9 | $0;6,40$ | regular (terminates) |
| 10 | $0;6$ | regular (terminates) |
| 11 | $0;\overline{5,27,16,21,49}$ | period 5 |
| 12 | $0;5$ | regular (terminates) |
| 13 | $0;\overline{4,36,55,23}$ | period 4 |
| 14 | $0;4,\overline{17,8,34}$ | period 3, then 1 leading digit |
| 15 | $0;4$ | regular (terminates) |
| 16 | $0;3,45$ | regular (terminates) |
| 17 | $0;\overline{3,31,45,52,56,28,14,7}$ | period 8 |
| 18 | $0;3,20$ | regular (terminates) |
| 19 | $0;\overline{3,9,28,25,15,47,22,6,18,56,50,31,34,44,12,37,53,41}$ | period 18 |
| 20 | $0;3$ | regular (terminates) |
| 21 | $0;2,\overline{51,25,42}$ | period 3, then 1 leading digit |
| 22 | $0;2,\overline{43,38,10,54,32}$ | period 5, then 1 leading digit |
| 23 | $0;\overline{2,36,31,18,15,39,7,49,33,54,46,57,23,28,41,44,20,52,10,26,5,13}$ | period 22 |
| 24 | $0;2,30$ | regular (terminates) |
| 25 | $0;2,24$ | regular (terminates) |
| 26 | $0;2,\overline{18,27,41,32}$ | period 4, then 1 leading digit |
| 27 | $0;2,13,20$ | regular (terminates) |
| 28 | $0;2,\overline{8,34,17}$ | period 3, then 1 leading digit |
| 29 | $0;\overline{2,4,8,16,33,6,12,24,49,39,18,37,14,28,57,55,51,43,26,53,47,35,10,20,41,22,45,31}$ | period 28 |
| 30 | $0;2$ | regular (terminates) |
| 31 | $0;\overline{1,56,7,44,30,58,3,52,15,29}$ | period 10 |
| 32 | $0;1,52,30$ | regular (terminates) |
| 33 | $0;1,\overline{49,5,27,16,21}$ | period 5, then 1 leading digit |
| 34 | $0;1,\overline{45,52,56,28,14,7,3,31}$ | period 8, then 1 leading digit |
| 35 | $0;1,\overline{42,51,25}$ | period 3, then 1 leading digit |
| 36 | $0;1,40$ | regular (terminates) |
| 37 | $0;\overline{1,37,17,50,16,12,58,22,42,9,43,47}$ | period 12 |
| 38 | $0;1,\overline{34,44,12,37,53,41,3,9,28,25,15,47,22,6,18,56,50,31}$ | period 18, then 1 leading digit |
| 39 | $0;1,\overline{32,18,27,41}$ | period 4, then 1 leading digit |
| 40 | $0;1,30$ | regular (terminates) |
| 41 | $0;\overline{1,27,48,17,33,39,30,43,54,8,46,49,45,21,57,4,23,24,52,40,58,32,11,42,26,20,29,16,5,51,13,10,14,38,2,55,36,35,7,19}$ | period 40 |
| 42 | $0;1,\overline{25,42,51}$ | period 3, then 1 leading digit |
| 43 | $0;\overline{1,23,43,15,20,55,48,50,13,57,12,33,29,18,8,22,19,32,5,34,53}$ | period 21 |
| 44 | $0;1,\overline{21,49,5,27,16}$ | period 5, then 1 leading digit |
| 45 | $0;1,20$ | regular (terminates) |
| 46 | $0;1,\overline{18,15,39,7,49,33,54,46,57,23,28,41,44,20,52,10,26,5,13,2,36,31}$ | period 22, then 1 leading digit |
| 47 | $0;\overline{1,16,35,44,40,51,3,49,47,14,2,33,11,29,21,42,7,39,34,28,5,6,22,58,43,24,15,19,8,56,10,12,45,57,26,48,30,38,17,52,20,25,31,54,53,37}$ | period 46 |
| 48 | $0;1,15$ | regular (terminates) |
| 49 | $0;\overline{1,13,28,9,47,45,18,22,2,26,56,19,35,30,36,44,4,53,52,39,11}$ | period 21 |
| 50 | $0;1,12$ | regular (terminates) |
| 51 | $0;1,\overline{10,35,17,38,49,24,42,21}$ | period 8, then 1 leading digit |
| 52 | $0;1,\overline{9,13,50,46}$ | period 4, then 1 leading digit |
| 53 | $0;\overline{1,7,55,28,18,6,47,32,49,48,40,45,16,58,52,4,31,41,53,12,27,10,11,19,14,43}$ | period 26 |
| 54 | $0;1,6,40$ | regular (terminates) |
| 55 | $0;1,\overline{5,27,16,21,49}$ | period 5, then 1 leading digit |
| 56 | $0;1,4,\overline{17,8,34}$ | period 3, then 2 leading digits |
| 57 | $0;1,\overline{3,9,28,25,15,47,22,6,18,56,50,31,34,44,12,37,53,41}$ | period 18, then 1 leading digit |
| 58 | $0;1,\overline{2,4,8,16,33,6,12,24,49,39,18,37,14,28,57,55,51,43,26,53,47,35,10,20,41,22,45,31}$ | period 28, then 1 leading digit |
| 59 | $0;\overline{1}$ | period 1 |

- **Regular numbers terminate.** The longest expansions are $1/27=0;2,13,20$, $1/32=0;1,52,30$ and $1/54=0;1,6,40$, with three places.
- **Irregular numbers repeat.** The period is a divisor of $n-1$ when $n$ is prime and not $2,3,5$: e.g. $1/7$ has period $3$, $1/13$ period $4$, $1/59$ period $1$ ($60\equiv1\pmod{59}$), and $1/47$ has period $46$.
- **Shared blocks.** $1/7$, $1/14$, $1/28$ and $1/56$ all repeat the same three digits $8,34,17$, in rotation.

## Square roots and $\sqrt2$

A clay tablet in the Yale Babylonian Collection (YBC 7289) shows a square with its diagonal and the numbers $1;24,51,10$ and $42;25,35$. With the side $30$, the diagonal is $30\sqrt2$:

$$\sqrt2\approx1;24,51,10=1.41421296\ldots\qquad 30\times1;24,51,10=42;25,35.$$

The value is within $7\times10^{-7}$ of $\sqrt2$. It is an *approximation* in a stated precision, a number the scribe stopped writing: see [[Constructible Numbers]] for what $\sqrt2$ is as a length.
