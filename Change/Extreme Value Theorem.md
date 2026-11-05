---
title: Extreme Value Theorem
type: theorem
status: "canonical (the exact statement rejected; the approximate form kept; compactness read as a finite grid)"
provenance: "murphy (the position, an approximation save, give me an epsilon and a supremum can be found to within it, but that is not asserting that a number exists that is the supremum) + ai-synthesis (the algorithm, the cost, the constructed failure, the flagged problems)"
sources: "[[Intermediate Value Theorem]], [[Calculus]], [[Certificates]], [[Creational Ultrafinitism]]"
updated: 2026-10-09
---

# Extreme Value Theorem

> **Standard statement.** If $f$ is continuous on $[a,b]$, then $f$ attains a greatest value: there is a point $c\in[a,b]$ with $f(c)\ge f(x)$ for all $x\in[a,b]$. Likewise a least value.

## What is rejected

The exact statement is rejected, in two parts. It claims a **supremum** $M=\sup f$, a number that is the least upper bound of infinitely many values, and it claims a **point** $c$ where $f(c)=M$.

The standard proof builds both from completed limits: $M$ exists by completeness; pick $x_n$ with $f(x_n)\to M$; the **Bolzano–Weierstrass** theorem gives a convergent subsequence with limit $c$; continuity gives $f(c)=M$. Each step asserts that an infinite process has finished. Nothing in it hands you $M$ or $c$.

Murphy's point, in his words: *give me an $\varepsilon$ and I can find a supremum to within $\varepsilon$, but that is not the same as asserting that a number exists that is the supremum.* The page makes it precise, and finds that **two different claims were run together**:

- **The value of the maximum is findable** to any stated precision (below). It is also **stable**: if two functions differ by at most $\eta$ everywhere, their maxima differ by at most $\eta$.
- **The location of the maximum is not.** It can jump with a tiny change of $f$, so no procedure outputs it.

### The location is unstable: a constructed failure

Let $f_r$ be two tents on $[0,1]$: one centred at $\tfrac14$ with height $1+r$ and slope $4(1+r)$, one centred at $\tfrac34$ with height $1-r$ and slope $4(1-r)$, and $0$ elsewhere. The maximum **value** is $1+|r|$, near $1$ for small $r$. The maximum **point** is $\tfrac14$ if $r>0$, $\tfrac34$ if $r<0$, and either if $r=0$ (checked on a grid for $r=\pm\tfrac1{1000},0$). Let $r$ be a number given by an unsolved search ($r=0$ while the search fails, $\pm2^{-m}$ when it succeeds at step $m$). To output the point $c$ exactly would decide the sign of $r$, that is, solve the search. The same device as in [[Intermediate Value Theorem]]. *(Unverified recollection to check: in the constructive literature the exact statement is not provable without an omniscience principle, while the version asserting only the supremum, not a point where it is attained, is provable for functions with a modulus of continuity.)*

## What stays: the approximate form

**$\varepsilon$-maximizer.** A point $x$ is an **$\varepsilon$-maximizer** of $f$ on $[a,b]$ if $f(x)\ge f(y)-\varepsilon$ for every $y$ in $[a,b]$. A rational $s$ is an **$\varepsilon$-supremum** if $f(y)\le s+\varepsilon$ for all $y$ and $f(x)\ge s-\varepsilon$ for some $x$. Neither definition mentions a supremum number.

> **Approximate EVT (budget form).** Let $f$ be continuous on $[a,b]$ with modulus $\delta$ ([[Intermediate Value Theorem]]). For every $\varepsilon>0$, let $N=\lceil(b-a)/\delta(\varepsilon/2)\rceil$ and $g_j=a+j(b-a)/N$ for $j=0,\dots,N$. Compute each $f(g_j)$ to within $\varepsilon/4$, giving $v_j$, and let $j^*$ be an index with $v_{j^*}$ largest. Then $x=g_{j^*}$ is an $\varepsilon$-maximizer, and $s=v_{j^*}$ is a $2\varepsilon$-supremum. The cost is $N+1$ evaluations.

*Proof.* Any $y$ lies within $\delta(\varepsilon/2)$ of a grid point $g_j$, so $f(y)\le f(g_j)+\tfrac\varepsilon2$. Also $f(g_j)\le v_j+\tfrac\varepsilon4\le v_{j^*}+\tfrac\varepsilon4\le f(g_{j^*})+\tfrac\varepsilon2$. Together, $f(y)\le f(g_{j^*})+\varepsilon$. $\square$

The least value is the same with the signs reversed. For a Lipschitz $f$ ($|f'|\le L$, so $\delta(\eta)=\eta/L$), $N=\lceil2L(b-a)/\varepsilon\rceil$.

**Worked example.** $f(x)=x(2-3x)$ on $[0,1]$, $\varepsilon=\tfrac1{10}$. Here $|f'|=|2-6x|\le4$, so $\delta(\varepsilon/2)=\tfrac1{80}$ and $N=80$: $81$ evaluations. The best grid point is $x=\tfrac{27}{80}$, with $f(x)=0.33328125$. The true maximum (named below) is $\tfrac13$, so the gap is $5.2\times10^{-5}$, far inside $\varepsilon$ (the guarantee is only that it is at most $\tfrac1{10}$; it is usually much better).

## The cost: exponential in the digits

Compare with the IVT. Bisection needs a number of steps **linear** in the digits of precision ([[Intermediate Value Theorem]]). The grid needs $N\approx2L(b-a)/\varepsilon$ evaluations, which is **proportional to $1/\varepsilon$, exponential in the digits**: $d$ digits cost about $8\cdot10^d$ evaluations when $L=4$ and $b-a=1$.

This is not a weakness of the grid. If all that is known about $f$ is its modulus, **no method can do much better**: after $m$ evaluations, a gap between sample points of width greater than $2\varepsilon/L$ can hold a tent of slope $L$ and height just above $\varepsilon$ that every evaluation missed, so the maximum has not been located to within $\varepsilon$. Hence one needs about $L(b-a)/(2\varepsilon)$ evaluations (a spike of base just over $0.05$ and height just over $0.1$ with $L=4$ fits into any gap wider than $0.05$, so at least $19$ evaluations for the example; the grid used $81$, the same order).

So for a general continuous function, **finding the maximum is much harder than finding a zero**, and it is capped by the budget: with a physical bound of order $10^{140}$ events ([[Creational Ultrafinitism]]) a Lipschitz-only maximization cannot reach more than roughly $140$ digits, whatever the algorithm.

## Where the exact form returns

More known structure makes the maximum cheap and often exact.

- **Polynomials with rational coefficients.** The extremes occur at the endpoints or where $p'=0$ (Fermat). The critical points are the roots of $p'$, **named** by isolating intervals ([[Fundamental Theorem of Algebra]]), and the values of $p$ there are algebraic numbers, which can be compared exactly. Example: $f(x)=x(2-3x)$ has $f'=2-6x=0$ at $x=\tfrac13$, $f(\tfrac13)=\tfrac13$, and the endpoints give $0$ and $-1$: three evaluations, the exact maximum $\tfrac13$. For $p(x)=x^3-x$ on $[0,1]$: $p'=3x^2-1$, critical point $\tfrac{\sqrt3}3\approx0.577$, minimum value $-\tfrac{2\sqrt3}9\approx-0.3849$, and the maximum $0$ is attained at *both* endpoints (a tie, decided exactly). Here the supremum **is** a number, named: a constructible number ([[Constructible Numbers]]).
- **Convex or unimodal functions.** Ternary search needs steps linear in the digits.
- **A finite list.** Any finite list of numbers has a largest, found by comparing, and for a lattice of rational points the discrete EVT is exact and finite ([[Discrete Calculus]]): at an interior lattice maximum the difference $\Delta f$ changes from non-negative to non-positive, which is an IVT statement about $\Delta f$ (Fermat's theorem in discrete form).

## Compactness, Bolzano–Weierstrass, Heine–Borel

These are the engines of the standard proof. Their **finite forms** survive:

- **Finite cover (Heine–Borel).** The interval $[a,b]$ is covered by the $N+1$ intervals of width $2\delta$ centred at the grid points. This is the grid above, and it is *exact*: a finite list of intervals.
- **Pigeonhole (Bolzano–Weierstrass, treated on [[Bolzano-Weierstrass Theorem]]).** Among any $N+1$ points of $[a,b]$ two are within $(b-a)/N$ of each other. Finite, exact, elementary. It replaces "every bounded sequence has a convergent subsequence" by "every long enough finite list has two close members".

What is rejected is the infinite version: a cover by *arbitrary infinitely many* open sets, or a subsequence chosen out of an infinite sequence, with a limit point that is asserted to exist. Where the standard theorems say "compact", the vault says "**totally bounded with a stated modulus**", which is the grid. [[Intermediate Value Theorem]] already takes continuity with a modulus; it is the same certificate.

The extreme value theorem is the engine of Rolle's theorem and so of the mean value theorem ([[Mean Value Theorem]]), whose inequality form is proved without it.

## Hard problems

1. **The cost of the location.** The value is findable and the point is not. Is there a statement about *near-maximizers* that is as useful as the classical "attained", for example: the set of $\varepsilon$-maximizers, which is non-empty and which one can sample from?
2. **The lower bound with more information.** The bound $\sim L(b-a)/(2\varepsilon)$ assumes only the modulus. What does one more derivative bound, or analyticity, buy, as a function of the certificates the vault accepts?
3. **Several variables.** The grid costs $(1/\varepsilon)^n$ in $n$ dimensions: the curse of dimension, in budget terms. Not written.
4. **Fermat in the $\varepsilon$-calculus.** "At an interior maximum $f'=0$" is proved above by finite steps. In SIA ([[Infinitesimals]]) one cannot compare infinitesimal steps by inequality, so the usual argument ($f'\varepsilon\le0$ and $-f'\varepsilon\le0$) is not available. How the vault states it there is open ([[Calculus]], hard problem 2).
5. **The cost of evaluating $f$** to precision $\varepsilon/4$, which the count of $N+1$ evaluations ignores.
