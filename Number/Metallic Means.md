---
title: Metallic Means
type: concept
status: canonical (draft)
provenance: "murphy (the table: the family, the names, the OEIS links, from his wiki page 'Metallic means (Metallic ratios)') + ai-synthesis (the exact arithmetic, the bracketing certificate, the rectangle, the slope identity; every identity and decimal checked) + third-party (Hurwitz's theorem; the name 'metallic mean')"
sources: "Murphy's wiki page on the metallic means (pasted 2026-11-13)"
updated: 2026-11-13
---

# Metallic Means

The **$n$-th metallic mean** (metallic ratio) is the positive root of $x^2=nx+1$:

$$\sigma_n=\frac{n+\sqrt{n^2+4}}{2}.$$

Equivalently, $x=n+\dfrac1x$. Unfolding this gives the continued fraction $\sigma_n=[n;n,n,n,\dots]$, with every partial quotient equal to $n$. The golden ratio is $\sigma_1$ and the silver ratio is $\sigma_2$. The defining relation, with $\sigma$ for $\sigma_n$:

$$\sigma-\frac1\sigma=n,\qquad \sigma\cdot\Bigl(-\frac1\sigma\Bigr)=-1.$$

The other root of $x^2=nx+1$ is $-1/\sigma$. So $\sigma_n$ is a **unit** of norm $-1$ in $\mathbb Z[\sigma_n]$, which is why everything below stays in whole numbers.

## The table

All decimals on this page are **pixels rounded to nine places**, at $\varepsilon=10^{-9}$ (the page-wide banner of [[Exact Until Output]]); the exact value is the ratio column. The OEIS numbers are Murphy's; each sequence's title was checked against the ratio.

| $n$ | ratio | simplified | value | OEIS | name |
|---|---|---|---|---|---|
| $0$ | $\dfrac{0+\sqrt4}{2}$ | $1$ | $1$ | | (degenerate: $x^2=1$) |
| $\tfrac23$ | $\dfrac{1+\sqrt{10}}{3}$ | | $1.387425887$ | | |
| $1$ | $\dfrac{1+\sqrt5}{2}$ | | $1.618033989$ | [A001622](https://oeis.org/A001622) | golden, $\varphi$ |
| $2$ | $\dfrac{2+\sqrt8}{2}$ | $1+\sqrt2$ | $2.414213562$ | [A014176](https://oeis.org/A014176) | silver, $\delta_S$ |
| $3$ | $\dfrac{3+\sqrt{13}}{2}$ | | $3.302775638$ | [A098316](https://oeis.org/A098316) | bronze |
| $4$ | $\dfrac{4+\sqrt{20}}{2}$ | $2+\sqrt5$ | $4.236067977$ | [A098317](https://oeis.org/A098317) | copper |
| $5$ | $\dfrac{5+\sqrt{29}}{2}$ | | $5.192582404$ | [A098318](https://oeis.org/A098318) | nickel |
| $6$ | $\dfrac{6+\sqrt{40}}{2}$ | $3+\sqrt{10}$ | $6.162277660$ | [A176398](https://oeis.org/A176398) | aluminum |
| $7$ | $\dfrac{7+\sqrt{53}}{2}$ | | $7.140054945$ | [A176439](https://oeis.org/A176439) | iron |
| $8$ | $\dfrac{8+\sqrt{68}}{2}$ | $4+\sqrt{17}$ | $8.123105626$ | [A176458](https://oeis.org/A176458) | tin |
| $9$ | $\dfrac{9+\sqrt{85}}{2}$ | | $9.109772229$ | [A176522](https://oeis.org/A176522) | lead |
| $10$ | $\dfrac{10+\sqrt{104}}{2}$ | $5+\sqrt{26}$ | $10.099019514$ | [A176537](https://oeis.org/A176537) | zinc |
| $\vdots$ | | | | | |
| $n$ | $\dfrac{n+\sqrt{n^2+4}}{2}$ | | | | |

Notes on the table:

- For $n$ even, $\sigma_n=\tfrac n2+\sqrt{\tfrac{n^2}{4}+1}$, the "simplified" column.
- The index need not be a whole number. For $n=p/q$ the root of $qx^2=px+q$ is $\dfrac{p+\sqrt{p^2+4q^2}}{2q}$; $n=\tfrac23$ gives $\dfrac{1+\sqrt{10}}{3}$. Its expansion is not $[n;n,\dots]$, since that form needs $n$ whole.
- The names beyond bronze are informal and vary from source to source (the three at the head of the list are the ones in common use).
- Copper is $2+\sqrt5=\varphi^3$ (see below).

## What kind of number

$\sigma_n$ is a root of a quadratic, so it is a **constructible number**, level 5 of [[Number Hierarchy]] — a Length, in [[Numbers, Lengths and Pixels]]. It is exhibited by compass and straightedge as soon as $\sqrt{n^2+4}$ is: the hypotenuse of a right triangle with legs $n$ and $2$.

**Stored exactly, never as digits** ([[Exact Until Output]]). Hold $\sigma_n$ as the symbol $\sigma$ with $\sigma^2=n\sigma+1$, and a value as a pair $a+b\sigma$ of integers (or rationals). Then:

$$(a+b\sigma)(c+d\sigma)=(ac+bd)+(ad+bc+nbd)\,\sigma,$$

all in whole-number arithmetic, with no root ever evaluated. Equality is the equality of pairs, since $1,\sigma$ are independent over $\mathbb Q$ ($\sigma$ is irrational). The powers are

$$\sigma^k=F_k\,\sigma+F_{k-1},\qquad F_0=0,\ F_1=1,\ F_{k+1}=nF_k+F_{k-1},$$

the **$n$-Fibonacci numbers** (Fibonacci for $n=1$, Pell for $n=2$). Checked for $n=3$: $\sigma^2=3\sigma+1$, $\sigma^3=10\sigma+3$, $\sigma^4=33\sigma+10$.

**Odd powers of a metallic mean are metallic.** The conjugate of $\sigma^k$ is $(-1/\sigma)^k=-\sigma^{-k}$ for odd $k$. So $\sigma^k-\sigma^{-k}=V_k$ is a whole number, where $V_0=2$, $V_1=n$, $V_{k+1}=nV_k+V_{k-1}$, and therefore $\sigma_n^{\,k}=\sigma_{V_k}$. In particular $V_3=n^3+3n$, so

$$\sigma_n^{\,3}=\sigma_{n^3+3n}:\qquad \varphi^3=\sigma_4\ (\text{copper}),\quad (1+\sqrt2)^3=7+5\sqrt2=\sigma_{14},\quad \sigma_3^{\,3}=\sigma_{36}.$$

Even powers are not metallic means: $\varphi^2=\tfrac{3+\sqrt5}{2}$ has norm $+1$, not $-1$.

## The certificate: convergents

The continued fraction is a **procedure that is never finished** — the ellipsis in $[n;n,n,\dots]$ is a potential infinity, not a completed one. What is finished at every stage is the convergent:

$$\frac{p_0}{q_0}=\frac n1,\quad \frac{p_1}{q_1}=\frac{n^2+1}{n},\quad p_{k+1}=np_k+p_{k-1},\quad q_{k+1}=nq_k+q_{k-1}.$$

Three exact, whole-number facts, each checkable by hand:

1. $p_k^2-n\,p_kq_k-q_k^2=(-1)^{k+1}$ (checked for $n=1,2,3,5$ through seven convergents). So $p_k/q_k$ is *almost* a root of $x^2=nx+1$, and the failure is $\pm1$ exactly.
2. $p_{k+1}q_k-p_kq_{k+1}=\pm1$, and the convergents alternate below and above $\sigma$. Two consecutive ones therefore **bracket** $\sigma_n$, with width exactly $\dfrac1{q_kq_{k+1}}$.
3. $q_k$ grows like $\sigma^k$, so each step gains about $2\log_{10}\sigma_n$ digits: $0.42$ for the golden ratio, $0.77$ for silver.

Examples: $\dfrac85<\varphi<\dfrac{13}8$ (width $\tfrac1{40}$); $\dfrac{12}5<1+\sqrt2<\dfrac{29}{12}$ (width $\tfrac1{60}$).

This is the pixel doctrine at its cleanest: the stored value is exact (level 5), the digits are a bracket with a stated width, and the bracket is a pair of integers whose certificate is one multiplication. For silver, fact 1 reads $(p-q)^2-2q^2=\pm1$: it is **Pell's equation** in $x=p-q$ and $q$ (checked at $5/2$: $3^2-2\cdot2^2=1$). The silver convergents $\tfrac52,\tfrac{12}5,\tfrac{29}{12}$ are $1$ plus the convergents $\tfrac32,\tfrac75,\tfrac{17}{12}$ of $\sqrt2$, since $\sigma_2=1+\sqrt2$. In general fact 1 is $(2p-nq)^2-(n^2+4)q^2=\pm4$.

**The golden ratio is the hardest to approximate.** Its partial quotients are all $1$, the smallest possible, so its convergents converge slowest. Hurwitz's theorem (third-party) makes this exact: every irrational has infinitely many fractions with $|x-p/q|<1/(\sqrt5q^2)$, and $\sqrt5$ cannot be raised for the golden ratio. For $\sigma_n$ the corresponding constant is $\sqrt{n^2+4}$.

## Geometry

**The rectangle.** Take a rectangle with sides $\sigma_n$ and $1$. Cut off $n$ unit squares along the long side. What remains has sides $\sigma_n-n=1/\sigma_n$ and $1$: the same shape, turned. For $n=1$ this is the golden rectangle, and for every $n$ it is the picture of $x=n+\dfrac1x$ and of the continued fraction (each cut is one partial quotient).

**A slope.** Let $w$ be the wedge of slope $m=\tfrac n2$, with characteristic length $\ell=\sqrt{1+m^2}=\tfrac{\sqrt{n^2+4}}{2}$ ([[Characteristic Length]]). Then

$$\sigma_n=\frac n2+\frac{\sqrt{n^2+4}}2=m+\ell,\qquad \frac1{\sigma_n}=\ell-m,$$

since $\ell^2-m^2=1$. So the metallic mean is the sum of the slope and the characteristic length of one wedge. It is also itself a slope: **the slope of the wedge made of an eighth of a turn plus half of $w$.**

*Proof.* By the half-wedge rule, $w/2$ has slope $t=\sqrt{\dfrac{\ell-1}{\ell+1}}$ ([[Nested Radicals]]). An eighth of a turn has slope $1$, so by [[Sum of Slopes]] the combined wedge has slope $\dfrac{1+t}{1-t}=\dfrac{(1+t)^2}{1-t^2}$. Now $1-t^2=\dfrac2{\ell+1}$ and $(1+t)^2=\dfrac{2\ell}{\ell+1}+2t$, so the quotient is $\ell+t(\ell+1)=\ell+\sqrt{(\ell-1)(\ell+1)}=\ell+m$. $\square$

For $n=2$: $m=1$, so $w$ is an eighth of a turn, and the wedge is an eighth plus a sixteenth, three sixteenths of a turn, with slope $1+\sqrt2$. This agrees with [[Exact Slopes]] (a sixteenth has slope $\sqrt2-1=1/\sigma_2$, and the three sixteenths are the complement of one). For $n=1$ the golden ratio is the slope of the wedge built from an eighth of a turn and half of the slope-$\tfrac12$ wedge. Whether that wedge belongs to any regular polygon is not checked here; the golden ratio's polygon appearance is as $k$ of a tenth of a turn ([[Nested Radicals#The golden pair]]).

The sister family $x^2=nx-1$ (roots like $2+\sqrt3$ and $\varphi^2$, with norm $+1$) is a different family: it is the $k$ of [[Nested Radicals]], $x+\tfrac1x=n$. Its members are not metallic means.

## Hard problems and flags

1. **Attribution of the name.** "Metallic mean" is from Vera W. de Spinadel (late 1990s), from memory, **to check**; Murphy's wiki table does not say.
2. **Names beyond bronze.** Informal; no authority is cited. Murphy's own list is kept as given.
3. **The $\tfrac23$ row** is in Murphy's table without a stated reason; kept, and treated as the first rational index. Whether a use of it was intended is for him to say.
4. **A tie to the position that is still open [AI].** The convergent certificate is a clean test case for the Finite Certification Theorems ([[Future Directions]], item 2): its construction cost ($k$ steps of one multiply-by-$n$ and one addition on whole numbers) and its verification cost (a few multiplications to check $p^2-npq-q^2=\pm1$) are separate and both small. Worth stating as a worked case on [[Certificates]]; not done.
