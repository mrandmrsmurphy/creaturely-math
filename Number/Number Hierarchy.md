---
title: Number Hierarchy
type: hierarchy
status: canonical
provenance: "murphy (the hierarchy; the level-9 cost analysis for e, adopted 2026-11-04; the Posits recorded dialectically, adopted 2026-11-06) + ai-synthesis (the level-9 worked brackets; the negative-half details of level 12)"
sources: "Murphy's raw mathematics draft (2026-05)"
updated: 2026-10-11
---

# Number Hierarchy — 14 levels of "equals"

**Why a hierarchy.** The word *number* today is like the word *star* two thousand years ago. Some of those "stars" are gas planets, some are rocky planets, some are stars, some are galaxies. We are not careful enough with the word *number* to gain the right insights, and the hierarchy is the sorting: it separates the kinds of things that now share one name.

Organized by **what "=" means** and **what certificate is required**. A certificate is a **procedure**, and each kind's "=" is the procedure its level affords ([[Certificates]]). The central insight: [[Certificates#The bargain|every step up is a bargain]]. This is the *exhibitability* direction; the orthogonal direction, adjoining numbers by fiat ($\varepsilon$, $i$, $j$, and the quaternions and beyond), is [[Fiat Numbers]].

| # | Name | Symbol | Certificate | Key examples / notes |
|---|---|---|---|---|
| **A. Numbers** (the exhibitable) — *exact equality certificates* | | | | |
| 1 | Natural | ℕ | the count itself | |
| 2 | Whole | 𝕎 | add zero — "the philosophical leap is larger than it looks" (zero is not a count of anything) | |
| 3 | Integers | ℤ | add direction/sign | |
| 4 | Rational | ℚ | reduced pair $(a,b)$, $\gcd=1$; $\frac ab=\frac cd\iff ad=bc$ | |
| **B. Lengths** (the geometric) — *inequality certificates; equality is asymptotic* | | | | |
| 5 | Constructible | 𝕂 | compass & straightedge; closed under $+,-,\times,\div,\sqrt{}$; Galois group a 2-group | [[Constructible Numbers]] |
| 6 | Origami | 𝔽 (article: 𝒪) | folding adds cube roots / some cubics; degree-3 now allowed | $\sqrt[3]{2}$ lives here |
| **C. Pixels** (the algorithmic) — *convergence certificates; "=" becomes agreement-to-n-places* | | | | |
| 7 | Jiǔ Zhāng | 𝕁 | $n$-th roots with a **determinate digit algorithm**; digits guaranteed in order; exact to stated precision | $\sqrt[5]{2}$; algorithm from 九章算術, ch. 4 (*Shaoguang*) |
| 8 | Algebraic | 𝔸 | polynomial roots by Newton's method, iterated until the stated resolution is reached (that run is the certificate); digits may be revised along the way: may overshoot, correct, overshoot; first needed for general quintic roots | Same object as 7 where it exists there |
| 9 | Transcendental **Geometric** | 𝕋 | *defined* geometrically first, *computed* analytically second | π (circumference/diameter); $e$ (the $x$ with unit area under $y=1/x$ from 1 to $x$); elliptic integrals $E(k)$ (arc length of an ellipse); lemniscate constant ϖ (from $r^2=2\cos2\theta$); areas of paraboloid/spheroid sections; $\zeta(2)=\pi^2/6$ (geometric because it reduces to π). "Very rich, not fully enumerated." |
| 10 | Series | 𝕊 | the *summation process* is the certificate; no known geometric primary definition | Apéry's $\zeta(3)$ — irrational (1978), transcendence unknown |
| 11 | Limit | 𝕃 | a limiting process that is neither geometric (9) nor a convergent series (10) | Feigenbaum δ≈4.669, α≈2.502 (period doubling); Euler–Mascheroni γ = lim$(H_n-\ln n)$ (irrationality unknown); functions sin/exp/log as objects live here too |
| **D. Posits** (the twilight) — *existence without exhibition* | | | | |
| 12 | Uncomputable | 𝕌 | existence provable (Cantor/diagonal accepted *as negative results*), but only for someone who has accepted all or most of the previous levels; no algorithm even in principle | Chaitin's Ω |
| 13 | Divergent | 𝔻 | **the summation method itself** — must be stated or the expression is meaningless | $1-1+1-\cdots=\frac12$ (Cesàro): a *different kind of object* from ℚ's ½ |
| 14 | Zeta | ζ | analytic-continuation assignment | $1+2+3+\cdots=-\frac1{12}$: not the $-\frac1{12}$ of ℤ — "same notation, utterly different certificate" |

## Levels 5–8: the toolkits and the Galois boundary

Each of these levels is defined by the **tool** that makes its numbers:

| level | tool | digits |
|---|---|---|
| 5 Constructible 𝕂 | compass and straightedge: $+,-,\times,\div,\sqrt{\ }$ | never finished, but a length exhibits the number (the diagonal of a unit square) |
| 6 Origami 𝔽 | the same, plus cube roots | likewise: $\sqrt[3]2$ is a length you can fold |
| 7 Jiǔ Zhāng 𝕁 | the decimal expansion of an arbitrary radical, digit by digit | a digit, once written, is right and never revised: nothing beyond the digit is needed to trust it |
| 8 Algebraic 𝔸 | Newton's method on a polynomial | an iteration can rewrite earlier digits, so the last digit is trusted only after running further than the digit itself requires |

The levels are nested like **concentric circles, but not strictly**: a number sits at the first level whose tool makes it. $\sqrt2$ is at level 5 even though the algorithm of level 7 also computes it.

The Galois-theoretic picture matches the toolkits:

- **Levels 5 and 6** are built by iterating steps of degree $\le4$: a square root for $\mathbb K$ (a tower of degree-2 extensions, Galois group a 2-group), and also a cube root for origami (towers of degree 2 and 3). Iteration reaches numbers of higher degree: $6,9,12,\dots$ occur.
- **Level 7** is everything solvable by radicals, which brings in numbers that no tower of degree-2 and 3 steps reaches, such as $\sqrt[5]{2}$ (degree 5).
- **The wall** between levels 7 and 8 is the one Abel and Galois identified. The roots of $x^5-x-1$ are not expressible by radicals, because the Galois group of that polynomial is $S_5$, which is not solvable. This is a hard structural boundary, not computational convenience: past it, Newton's method is the only digit procedure, with its rewriting.

## The names, in short

Group A is the **Numbers**, group B the **Lengths**, group C the **Pixels**, group D the **Posits**: Murphy's names for the sort, on [[Numbers, Lengths and Pixels]].

## Why the Posits are on the ladder (Murphy)

The Posits are not numbers in the normal sense, and the systems of belief behind them are not warranted. Level 12, the least involved of them, is recorded here to force people who believe in the reals to wrestle with the implications of that acceptance: **uncomputable numbers are asserted without any exhibition.** The vault owns the negative half as theorems and declines the positive existence. [AI] The negatives: no algorithm prints the digits of Chaitin's $\Omega$ (from the first $n$ bits one could decide the halting of every program of length $\le n$); the defining sum is bounded (the machines are prefix-free, so Kraft's inequality gives $\sum2^{-|p|}\le1$); and its stage-by-stage approximants are computable rationals with no modulus of convergence — the Specker phenomenon of [[Bolzano-Weierstrass Theorem]].

## Trust across the levels

Every level is a step into more trust of the methods; the levels grow more and more remote from verification.

- **Level 7:** you trust every digit as it comes.
- **Level 8:** you depend on the error bounds of riding tangent lines (Newton's method).
- **Level 9:** you trust that the shape bounds your number, as when one hunts for the right bound that makes the area under $1/x$ from $1$ equal $1$. ($e$ has a geometric and an analytic definition.)
- **Level 10:** a convergent series aims at a quantity with no name and no easy shape, but seems to get narrowly closer to something.
- **Level 11:** the same, but broader: the process is not just addition.

This is the pattern of **every** level of the hierarchy, and it is why the levels exist: the trust gets more and more threadbare as one goes out. The Babylonians drew the line early: they distrusted an approximation of $\sqrt2$ exactly as they distrusted one of $\tfrac17$ ([[Babylonian Mathematics]]).

### A certificate for level 9: the right edge of the area under $1/x$

$e$ is the $b$ with $\int_1^b dx/x=1$. For a decreasing curve the area lies between the right-endpoint and left-endpoint rectangle sums, so a rational pair of bounds is a certificate that trusts only the shape. Divide $[1,b]$ into $n=1000$ equal strips (all computed, exact rational sums):

| $b$ | area is at least | area is at most | verdict |
|---|---|---|---|
| $\tfrac{27}{10}$ | $0.99271\ldots$ | $0.99378\ldots$ | below $1$ (the upper bound is under $1$) |
| $\tfrac{28}{10}$ | $1.02904\ldots$ | $1.03019\ldots$ | above $1$ (the lower bound is over $1$) |

So the area reaches $1$ somewhere in $(2.7,\,2.8)$, an isolating interval for $e$ (the area grows with $b$), and bisection on $b$ halves it at each step. The width of each bracket is the strip width times $1-\tfrac1b$, so to certify $k$ digits one needs about $10^k$ strips: the geometric definition certifies by trusting the shape, and it is slow. The analytic definition is fast: ten terms of $\sum 1/k!$ give $2.7182818011\ldots$ with the tail under $\tfrac1{10!\cdot10}<2.8\times10^{-8}$ (computed; the tail bound is the standard one, to check against a source). That the two definitions name the same number is a theorem, and trust in that theorem is the extra thing level 9 asks for.

## Why it matters pedagogically

- "What *is* $\sqrt2$?" → a level-5 geometric object: exhibited as a *length*; equal to any rational only by approximation. "What *is* $e$?" → right edge of unit area under $xy=1$ — a level-9 object, *not primarily* a series. "It's a real number" is the bamboozlement in action.
- Proof becomes concrete: *the provision of a certificate appropriate to the level.*
- Mathematics' history = the history of bargains, "sometimes made honestly and sometimes not" — see [[Corrective Narrative]] (Cardano's "sophistic numbers" as the first uncertified admission).

## Open

(a) Is the ordering total or a lattice? (b) Complex numbers do not sit on this axis: they are adjoined by fiat, in the orthogonal direction ([[Fiat Numbers]]). (c) Levels 13–14 are admitted "if the convention is named" — what exactly is the convention-certificate? See [[Future Directions]] items 3, 5.
