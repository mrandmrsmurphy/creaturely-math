---
title: Binary
type: concept
status: canonical (draft)
provenance: "murphy+ai (Murphy's brief: binary matters because of computers, has real applications such as the Tower of Hanoi, and is tied to octal, hexadecimal and base 64; the worked material was computed and checked exactly)"
sources: "[[SRC Confession of Mathematics (2023-24)]]"
updated: 2026-10-08
---

# Binary

**Base 2.** Two digits, $0$ and $1$, called **bits**. Each place is worth twice the one to its right. [[Counting and Bases]] lists two as the first base to learn after ten, and it is the base of nearly every computer.

*[AI]* Historical remarks are standard recollections and have not been checked against sources here. Numbers and tables were computed and verified exactly.

## Writing numbers

$$10110111_2=1\cdot2^7+0\cdot2^6+1\cdot2^5+1\cdot2^4+0\cdot2^3+1\cdot2^2+1\cdot2+1=183.$$

The places are $1,2,4,8,16,32,64,128,\dots$. To write a number in binary, repeatedly take the largest power of 2 that fits, or repeatedly halve and record the remainders (read bottom to top):

| 183 ÷ 2 | quotient | remainder |
|---|---|---|
| 183 | 91 | 1 |
| 91 | 45 | 1 |
| 45 | 22 | 1 |
| 22 | 11 | 0 |
| 11 | 5 | 1 |
| 5 | 2 | 1 |
| 2 | 1 | 0 |
| 1 | 0 | 1 |

Reading upward: $10110111_2$.

Counting to ten: $1,\ 10,\ 11,\ 100,\ 101,\ 110,\ 111,\ 1000,\ 1001,\ 1010$. Add and multiply with the same carrying rules as decimal, but the table is tiny: $1+1=10$, and $0\times0=0$, $0\times1=0$, $1\times1=1$. Multiplying by $2$ appends a $0$, the way multiplying by ten does in decimal.

## Why it is natural

- **A bit is a yes/no.** Each digit records one decided question: is this power of 2 present or absent? A switch is on or off; a voltage is high or low; a hole is punched or not. Two states are the easiest to tell apart reliably, which is why machines use base 2.
- **Twenty questions.** Ten yes/no questions distinguish $2^{10}=1024$ possibilities; twenty distinguish $2^{20}=1{,}048{,}576$. Each question halves the field, which is binary search.
- **Doubling and halving.** Any whole number is a sum of distinct powers of 2, so it can be built from a doubling chain (**Egyptian** or "Russian peasant" multiplication: double one factor, halve the other, add the rows where the halved factor is odd). A balance scale with weights $1,2,4,8,\dots$ can weigh every whole number up to $2^n-1$.
- **Fractions.** The termination rule of [[Counting and Bases]] says $\tfrac1n$ terminates in base 2 only if $n$ is a power of 2. So $\tfrac12=0.1_2$ and $\tfrac38=0.011_2$ are finite, but $\tfrac1{10}=0.0\overline{0011}_2$ repeats forever. A computer that stores binary fractions must stop somewhere, so it holds only an approximation of $\tfrac1{10}$. This is the Babylonians' $\tfrac17$ again: a place where the base cannot say the number exactly, and where one stops and says so.

## Octal, hexadecimal and base 64

Bases $8=2^3$, $16=2^4$ and $64=2^6$ are **powers of 2**, so they are binary in shorthand. Group the bits in threes (octal), fours (hexadecimal) or sixes (base 64), starting from the right; each group is one digit. No arithmetic is needed. Converting to base 10, by contrast, is real computation.

| base | bits per digit | digits |
|---|---|---|
| 2 | 1 | 0 1 |
| 8 | 3 | 0–7 |
| 16 | 4 | 0–9, A–F ($A=10,\dots,F=15$) |
| 64 | 6 | A–Z, a–z, 0–9, +, / (value 0 to 63, in that order) |

**Example: $183$.**

$$10\,110\,111_2=267_8\qquad 1011\,0111_2=\mathrm{B7}_{16}.$$

Check: $2\cdot64+6\cdot8+7=183$ and $11\cdot16+7=183$.

**Example: $1000$.** $1111101000_2$ regroups as $1\,111\,101\,000_2=1750_8$ and as $11\,1110\,1000_2=\mathrm{3E8}_{16}$.

**Uses.**

- **Octal:** Unix file permissions are three bits (read, write, execute) for each of owner, group and others, so $755=111\,101\,101_2$ means owner may read, write and execute, and everyone else may read and execute.
- **Hexadecimal:** a byte is 8 bits, exactly two hex digits ($0$ to $\mathrm{FF}=255$). Web colors give one byte each of red, green and blue: $\mathrm{FF8000}$ is full red, half green, no blue (orange). Memory addresses and character codes are written in hex.
- **Base 64:** sends binary data through channels that accept only text (e-mail attachments, web pages). Three bytes (24 bits) become four base-64 digits (also 24 bits). The bytes of "Man" are $01001101\ 01100001\ 01101110$, which regroup as $010011\ 010110\ 000101\ 101110=19,22,5,46$, written $\mathrm{TWFu}$. If the input is not a multiple of three bytes, the end is padded with "=": "M" becomes $\mathrm{TQ{=}{=}}$.

Base 64 is the natural counterpart of [[Sexagesimal]]: a large base, with a real table of digit symbols, chosen for convenience in the working tool.

## The Tower of Hanoi

Three pegs. $n$ disks of different sizes are stacked on the first peg, largest at the bottom. Move the whole stack to another peg, one disk at a time, never placing a larger disk on a smaller one. (Invented by Édouard Lucas in 1883, with a legend of a temple tower of 64 disks. *[AI]* from memory.)

**Minimum number of moves: $2^n-1$.** To move $n$ disks, move the top $n-1$ aside, move the largest, then move the $n-1$ back on top. So $M_n=2M_{n-1}+1$ with $M_1=1$, giving $1,3,7,15,31,\dots$, one less than a power of 2 — the number whose binary form is all ones.

**The binary counter.** Write the move number $m=1,2,\dots,2^n-1$ in binary. The disk to move is the disk whose number is **one more than the count of trailing zeros of $m$**. Disk 1 (smallest) moves on odd moves, disk 2 on moves $2,6,10,\dots$, disk 3 on moves $4,12,20,\dots$, and disk $k$ moves every $2^k$ moves, starting at move $2^{k-1}$. For $n=3$:

| move $m$ | binary | disk moved | from → to | result (bottom → top) |
|---|---|---|---|---|
| 1 | 001 | 1 | A → C | A: 3 2 · B: – · C: 1 |
| 2 | 010 | 2 | A → B | A: 3 · B: 2 · C: 1 |
| 3 | 011 | 1 | C → B | A: 3 · B: 2 1 · C: – |
| 4 | 100 | 3 | A → C | A: – · B: 2 1 · C: 3 |
| 5 | 101 | 1 | B → A | A: 1 · B: 2 · C: 3 |
| 6 | 110 | 2 | B → C | A: 1 · B: – · C: 3 2 |
| 7 | 111 | 1 | A → C | A: – · B: – · C: 3 2 1 |

The smallest disk moves every other turn, always in the same cyclic direction around the pegs (A → C → B → A when $n$ is odd; the opposite way when $n$ is even). On the other turns exactly one other move is legal. This gives a complete procedure with no planning ahead. Each bit that flips from one count to the next corresponds to one disk moving, which is why the puzzle is also the ordering of the **Gray code**, where successive numbers differ in one bit.

**Scale.** With 64 disks the minimum is $2^{64}-1=18{,}446{,}744{,}073{,}709{,}551{,}615$ moves. At one move per second this is about $5.8\times10^{11}$ years, many times the age of the universe. The rule is perfectly clear and every move is trivial, yet no creature will ever carry it out. This is the ultrafinitist's point about [[Creational Ultrafinitism]]: the procedure is exhibited, the output is not.

## Other places binary appears

- **Computers:** all stored data is bits; characters (ASCII, Unicode), images, sound.
- **Boolean algebra:** $1$ and $0$ as true and false, with AND, OR, NOT, where $1+1=1$: [[Boolean Algebra]].
- **Error detection:** a parity bit makes the count of 1s even, so a single flipped bit is noticed.
- **Leibniz** wrote on binary arithmetic around 1703 and read in it the creation of everything from one and nothing. *[AI]* from memory; check before relying on it. It sits near [[Theology of Number]].
