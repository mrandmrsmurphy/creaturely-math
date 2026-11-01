---
title: Exact Until Output
type: principle
status: "canonical (the rule and its machinery; independence questions flagged)"
provenance: "murphy (the principle, keep constructible values exact and approximate only at an output stage, never as the stored value; keep transcendentals separate, answering circle questions in terms of pi; slope, not spread; the pi_n convention, 2026-10-11) + ai-synthesis (the representation, the demonstrations, the decidability facts, the flagged problems) + third-party (Wildberger's rational trigonometry, restated)"
sources: "[[Constructible Numbers]], [[Number Hierarchy]], [[Constructible Trigonometry]], [[Certificates]], [[Equal Signs]]"
updated: 2026-10-11
---

# Exact Until Output

> **The rule (Murphy):** a computed value is stored exactly. A decimal approximation appears only at an **output stage**, as a rounding for a reader, and is never itself the stored value. Radicals are welcome: they are exact numbers. What is kept apart is the **transcendental**, carried as a named symbol.

This is a middle position on a spectrum. Wildberger's rational trigonometry refuses radicals and works with quadrance and spread (the squares, so everything stays rational). [[Constructible Trigonometry]] keeps the constructible numbers $\mathbb K$, closed under $+,-,\times,\div,\sqrt{\ }$ ([[Constructible Numbers]]), and takes the **slope** (the tangent) as the primitive instead of the spread. Both are exact; the difference is whether $\sqrt{\ }$ is allowed to be a number. The relation is simple: spread $=\dfrac{m^2}{1+m^2}$, slope $m=\sqrt{\dfrac{s}{1-s}}$.

## Three tiers of stored value

| Tier | What | Examples | Equality |
|---|---|---|---|
| **1. Rational** | reduced fractions | $\tfrac{3}{4}$ | decidable by cross-multiplication |
| **2. Constructible** | $\mathbb K$: radicals, nested radicals ([[Nested Radicals]]) | $\sqrt2$, $\tfrac{1+\sqrt5}2$, $\sqrt{2+\sqrt2}$ | decidable (below) |
| **3. Named transcendental symbols** | $\pi$, and any other kept as a symbol | $25\pi$, $\tfrac{5\pi}3$ | decidable for $\pi$ alone (below) |

A value of tier 3 is a polynomial in the symbols with coefficients in $\mathbb K$: $\ 25\pi,\ \tfrac{\sqrt3}{4}\pi r^2$, and so on. Nothing is rounded until the output.

## Why exact storage is better than a stored decimal

Floating point throws information away irreversibly:

- $\sqrt2\cdot\sqrt2$ in double precision is $2.0000000000000004$, and `==` with $2$ fails; $\sin(\pi)$ prints $1.22\times10^{-16}$, not $0$; $0.1+0.2\ne0.3$.
- In $\mathbb Q(\sqrt5)$, held as pairs $a+b\sqrt5$ of rationals, the golden ratio $\varphi=\tfrac12+\tfrac12\sqrt5$ satisfies $\varphi^2=\tfrac32+\tfrac12\sqrt5=\varphi+1$ **exactly**, and $(\sqrt5)^2=5$ exactly (checked).
- Murphy's point about circles: an answer $25\pi$ **can be turned into any number of digits, and can be recognised and factored**. The decimal $78.5398\ldots$ cannot be turned back: nothing says whether it was $25\pi$, or $\tfrac{25}{2}\cdot2\pi$, or a rounding of something else. Tools that guess the closed form from digits exist (integer-relation algorithms, to check) but are heuristic. *The symbolic answer keeps the structure.*

This is the certificate rule ([[Certificates]]) applied to storage: carry the strongest certificate you have, and weaken it only on output.

## Equality and order, exactly

- **In $\mathbb K$**: equality and sign are decidable. A number is a finite expression in radicals; two are equal iff their difference is $0$, which can be decided by refining an enclosing rational interval until it excludes $0$ or by comparing minimal polynomials (the standard decision procedure in computer algebra; separation bounds guarantee termination, to check).
- **In $\mathbb K[\pi]$**: $\pi$ is transcendental over $\mathbb Q$ (Lindemann, 1882, to check), hence over every algebraic number, and $\mathbb K$ is algebraic. So $\pi$ behaves as an **indeterminate** over $\mathbb K$: two expressions are equal iff their coefficients are equal in $\mathbb K$. The comparison is exact and mechanical.
- **Order** in $\mathbb K[\pi]$ needs bounds on $\pi$, supplied by a **rational enclosure with a certificate**. Archimedes' polygons give it from $\mathbb K$ itself: the inscribed side doubles by $s'=\sqrt{2-\sqrt{4-s^2}}$, a nested radical. Starting from the hexagon ($s=1$) and doubling four times gives the 96-gon, with half-perimeters $3.14103$ (inscribed) and $3.14272$ (circumscribed), which sit between $\tfrac{223}{71}=3.14085$ and $\tfrac{22}7=3.14286$ (all computed). So **$\pi$ is bracketed by constructible numbers**, a convergence certificate at Level 9 of [[Number Hierarchy]]: defined geometrically, computed second.

## Circle questions, exactly

- Circle of radius $5$: area $25\pi$, circumference $10\pi$.
- **A fraction of the circle**, named without angle measure: a wedge that is the interior wedge of a regular hexagon is one sixth of a full turn ([[Constructible Trigonometry]] names wedges concretely, never by degrees). Then the arc of radius $5$ over that wedge is $\tfrac{5\pi}3$ and the sector area is $\tfrac{25\pi}{6}$ (numerically $5.236$ and $13.090$, output only).
- **Arcs of general wedges.** The arc over a wedge of slope $m$ is a transcendental function of $m$ (the arctangent), not a rational multiple of $\pi$ in general. In the vault's style it is **named and kept**, not computed: it is a new symbol with its own certificate, as $\pi$ is.

## The π_n convention (Murphy)

When digits are shown at all, say how many: **$\pi_n$ is $\pi$ truncated to $n$ decimal places** — $\pi_2=3.14$, $\pi_7=3.1415926$ — and **$\pi_\infty$ is not accessible to us**. The convention kills an equivocation at birth. When someone writes $\pi$ and claims to have *shown* the number, what is shown is a symbol, which points; when they write digits, what is shown is $\pi_n$ for some $n$, which stops. Three consequences:

1. **$\pi_n$ is a Number** — a rational, $\pi_7=\tfrac{31415926}{10^7}$ — so $\pi_7=3.1415926$ is an *exact* equality of tier 1, no algorithmic "≈" needed. The subscript moves the decimal out of the twilight and into the exhibited.
2. **The truncation carries its own certificate:** $\pi_n\le\pi<\pi_n+10^{-n}$ (checked at $n=7$: the digits run $3.14159265\ldots$, so $3.1415926\le\pi<3.1415927$). The relation between $\pi$ and each of its exhibits is a finitely checkable *inequality* — the pixel equality of [[Certificates]], with the cost stated.
3. **The family $\{\pi_n\}$ is the classical construction in honest dress** [AI]. A Cauchy sequence of rationals is, potentially, exactly this list: each term exhibited, the list never completed. Nothing is lost but the pretense of arrival.

For a page full of digits, declare the resolution once — *all decimals herein are pixels at $\varepsilon=10^{-6}$* — and write $\pi=3.141593$ under that banner [AI]. The banner, not the bare "=", is what makes the page honest; it is the page-wide form of the pixel doctrine ([[Numbers, Lengths and Pixels]]). Bare $\pi$ remains welcome as a tier-3 *named symbol*; the convention governs digits, not symbols.

## Two cautions [AI]

1. **More than one transcendental.** Treating each of $\pi,\ e,\ \ln2,\dots$ as an independent indeterminate is a *convention that gives sufficient equality*, not a theorem. It is known that $\pi$ and $e$ are each transcendental; whether $\pi$ and $e$ are **algebraically independent over $\mathbb Q$ is an open problem**, as are the relations among many other constants (a conjecture of Schanuel would settle many; to check). So an expression mixing several symbols is equal when it is *formally* equal; if two expressions are formally different it is not decided, by this method alone, that they differ. For $\pi$ alone the method is exact.
2. **Extraction at the output stage.** Rounding for a reader should state the precision and the rounding direction. A value of tier 2 or 3 is bracketed by rationals with a stated width; the output is a member of that bracket.

## Consequences for the rest of the vault

- **Statistics:** the standard deviation is $\sqrt V$, held as a radical and rounded only for display; the correlation $r$ is exact in $\mathbb K$ ([[Constructible Statistics]]).
- **Calculus:** transcendental functions ($\exp$, $\ln$, trigonometric) enter as named symbols with their discrete ancestors and error certificates ([[Calculus]], [[Discrete Calculus]]).
- **[[Equal Signs]]:** the three signs are the three tiers' equalities; a printed decimal is a fourth, weakest kind, and the page's rule is to name it.

## Hard problems

1. **The cost of exact computation.** Radicals nest and expressions grow. A canonical form and a size budget for tier 2 (denesting is not always possible) are not stated here.
2. **A canonical form for sums of radicals**, and the best known procedure for the sign of such a sum, which is a hard problem in general (to check).
3. **Several transcendentals.** The independence question above.
4. **What counts as "output".** The line between a stored value and a displayed one must be stated for software and for a classroom.
