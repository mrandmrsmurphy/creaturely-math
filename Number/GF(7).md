---
title: GF(7)
type: concept
status: canonical (draft)
provenance: "murphy+ai (Murphy's brief: the same treatment as GF(5) and GF(3), with balanced digits; worked material computed and checked exactly)"
sources: "[[SRC Confession of Mathematics (2023-24)]]"
updated: 2026-10-08
---

# GF(7)

The field with seven elements: the integers mod $7$ ([[Modular Arithmetic]]) with all four operations. Same treatment as [[GF(3)]] and [[GF(5)]].

**Balanced residues.** The seven elements are written $\bar3,\ \bar2,\ \bar1,\ 0,\ 1,\ 2,\ 3$, where $\bar3=-3\equiv4$, $\bar2=-2\equiv5$ and $\bar1=-1\equiv6$. Negation swaps the bar and the unbarred digit.

*[AI]* Every table and every count on this page was computed and verified exactly.

## Addition

| | $\bar3$ | $\bar2$ | $\bar1$ | $0$ | $1$ | $2$ | $3$ |
|---|---|---|---|---|---|---|---|
| **$\bar3$** | $1$ | $2$ | $3$ | $\bar3$ | $\bar2$ | $\bar1$ | $0$ |
| **$\bar2$** | $2$ | $3$ | $\bar3$ | $\bar2$ | $\bar1$ | $0$ | $1$ |
| **$\bar1$** | $3$ | $\bar3$ | $\bar2$ | $\bar1$ | $0$ | $1$ | $2$ |
| **$0$** | $\bar3$ | $\bar2$ | $\bar1$ | $0$ | $1$ | $2$ | $3$ |
| **$1$** | $\bar2$ | $\bar1$ | $0$ | $1$ | $2$ | $3$ | $\bar3$ |
| **$2$** | $\bar1$ | $0$ | $1$ | $2$ | $3$ | $\bar3$ | $\bar2$ |
| **$3$** | $0$ | $1$ | $2$ | $3$ | $\bar3$ | $\bar2$ | $\bar1$ |

- The cyclic group of order $7$. Every row is a rotation of the first.

## Multiplication

| | $\bar3$ | $\bar2$ | $\bar1$ | $0$ | $1$ | $2$ | $3$ |
|---|---|---|---|---|---|---|---|
| **$\bar3$** | $2$ | $\bar1$ | $3$ | $0$ | $\bar3$ | $1$ | $\bar2$ |
| **$\bar2$** | $\bar1$ | $\bar3$ | $2$ | $0$ | $\bar2$ | $3$ | $1$ |
| **$\bar1$** | $3$ | $2$ | $1$ | $0$ | $\bar1$ | $\bar2$ | $\bar3$ |
| **$0$** | $0$ | $0$ | $0$ | $0$ | $0$ | $0$ | $0$ |
| **$1$** | $\bar3$ | $\bar2$ | $\bar1$ | $0$ | $1$ | $2$ | $3$ |
| **$2$** | $1$ | $3$ | $\bar2$ | $0$ | $2$ | $\bar3$ | $\bar1$ |
| **$3$** | $\bar2$ | $1$ | $\bar3$ | $0$ | $3$ | $\bar1$ | $2$ |

- The nonzero elements form a **cyclic** group of order $6$.
- Inverses: $1\leftrightarrow1$, $\bar1\leftrightarrow\bar1$, $2\leftrightarrow\bar3$ ($2\cdot\bar3=\bar6=1$), $3\leftrightarrow\bar2$ ($3\cdot\bar2=\bar6=1$). Every nonzero row is a rearrangement of the nonzero elements.

## Exponents

| $x$ | $x^0$ | $x^1$ | $x^2$ | $x^3$ | $x^4$ | $x^5$ | $x^6$ | order |
|---|---|---|---|---|---|---|---|---|
| $\bar3$ | $1$ | $\bar3$ | $2$ | $1$ | $\bar3$ | $2$ | $1$ | 3 |
| $\bar2$ | $1$ | $\bar2$ | $\bar3$ | $\bar1$ | $2$ | $3$ | $1$ | 6 |
| $\bar1$ | $1$ | $\bar1$ | $1$ | $\bar1$ | $1$ | $\bar1$ | $1$ | 2 |
| $0$ | 1 | $0$ | $0$ | $0$ | $0$ | $0$ | $0$ | — |
| $1$ | $1$ | $1$ | $1$ | $1$ | $1$ | $1$ | $1$ | 1 |
| $2$ | $1$ | $2$ | $\bar3$ | $1$ | $2$ | $\bar3$ | $1$ | 3 |
| $3$ | $1$ | $3$ | $2$ | $\bar1$ | $\bar3$ | $\bar2$ | $1$ | 6 |

- **Fermat:** $x^6=1$ for every $x\ne0$, and $x^7=x$ for every $x$.
- **Orders:** $1$ has order $1$, $\bar1$ has order $2$, $2$ and $\bar3$ have order $3$, and $3$ and $\bar2$ have order $6$. So the **primitive roots** are $3$ and $\bar2$ (and $\bar2=3^{-1}$).
- **Discrete logarithm base $3$:** $1,3,2,\bar1,\bar3,\bar2$ are $3^0,3^1,3^2,3^3,3^4,3^5$, so $\log_3$ of $1,2,3,\bar1,\bar3,\bar2$ is $0,2,1,3,4,5$ (mod $6$). Base $2$ is not primitive: it has order $3$, so $\log_2$ is defined only on $\{1,2,\bar3\}$.

## Squares and cubes

- **Squares:** $0,\ 1,\ 2,\ \bar3$ ($1^2=1$, $2^2=\bar3$, $3^2=2$). The nonzero squares are the elements $x$ with $x^3=1$, and the nonsquares $\bar1,\bar2,3$ have $x^3=\bar1$.
- **$\bar1$ is not a square.** As in $\mathrm{GF}(3)$, the fiat number $i$ is genuinely adjoined: $\mathrm{GF}(7)[i]=\mathrm{GF}(49)$ (the Gaussian integers mod $7$).
- **$\bar3$ is a square:** $2^2=\bar3$. So $\sqrt{-3}$ exists, $=\pm2$.
- **Cube roots of unity:** $x^3=1$ has the roots $1,2,\bar3$. So $x^2+x+1=(x-2)(x+3)$ splits: $\mathrm{GF}(7)$ contains the cube roots of unity, which the Eisenstein integers ($\omega^2+\omega+1=0$) need.

## Polynomials over GF(7)

**Identities.** $x^7-x=\prod_a(x-a)$. $x^6-1=(x-1)(x+1)(x-2)(x+2)(x-3)(x+3)$. $x^3-1=(x-1)(x-2)(x+3)$ and $x^3+1=(x+1)(x+2)(x-3)$. $x^2+x+1=(x-2)(x+3)$ and $x^2-x+1=(x+2)(x-3)$. And $x^2+1$ is irreducible.

**Up to isomorphism.** As before: monic polynomials are the same class when one becomes the other under $x\mapsto\lambda x+\mu$ ($\lambda\ne0$); there are $6\cdot7=42$ substitutions. Since $7\nmid d$ for $d=2,3,4$, each class has a **depressed form** (no $x^{d-1}$ term).

**Degree 1.** One class: $x$.

**Degree 2.** Three classes, $49$ polynomials in all.

| class | size | depressed forms |
|---|---|---|
| double root | 7 | $x^2$ |
| irreducible | 21 | $x^2+1$, $x^2+2$, $x^2+\bar3$ |
| two distinct roots | 21 | $x^2+3$, $x^2+\bar2$, $x^2+\bar1$ |

**Degree 3.** 12 classes, $343$ polynomials in all. Depressed cubics are $x^3+px+q$; the six scalings $\lambda$ act on $(p,q)$ by $(p,q)\mapsto(p/\lambda^2,q/\lambda^3)$.

| class | size | depressed forms |
|---|---|---|
| a double root and a simple root | 42 | $x^3+x+2$, $x^3+2x+2$, $x^3+\bar3x+2$, $x^3+x+\bar2$, $x^3+2x+\bar2$, $x^3+\bar3x+\bar2$ |
| irreducible | 42 | $x^3+x+1$, $x^3+2x+1$, $x^3+\bar3x+1$, $x^3+x+\bar1$, $x^3+2x+\bar1$, $x^3+\bar3x+\bar1$ |
| irreducible | 42 | $x^3+3x+2$, $x^3+\bar2x+2$, $x^3+\bar1x+2$, $x^3+3x+\bar2$, $x^3+\bar2x+\bar2$, $x^3+\bar1x+\bar2$ |
| irreducible | 14 | $x^3+2$, $x^3+\bar2$ |
| irreducible | 14 | $x^3+3$, $x^3+\bar3$ |
| one root and an irreducible quadratic | 42 | $x^3+3x+1$, $x^3+\bar2x+1$, $x^3+\bar1x+1$, $x^3+3x+\bar1$, $x^3+\bar2x+\bar1$, $x^3+\bar1x+\bar1$ |
| one root and an irreducible quadratic | 42 | $x^3+x+3$, $x^3+2x+3$, $x^3+\bar3x+3$, $x^3+x+\bar3$, $x^3+2x+\bar3$, $x^3+\bar3x+\bar3$ |
| one root and an irreducible quadratic | 42 | $x^3+3x+3$, $x^3+\bar2x+3$, $x^3+\bar1x+3$, $x^3+3x+\bar3$, $x^3+\bar2x+\bar3$, $x^3+\bar1x+\bar3$ |
| one root and an irreducible quadratic | 21 | $x^3+x$, $x^3+2x$, $x^3+\bar3x$ |
| three distinct roots | 21 | $x^3+3x$, $x^3+\bar2x$, $x^3+\bar1x$ |
| three distinct roots | 14 | $x^3+1$, $x^3+\bar1$ |
| triple root | 7 | $x^3$ |

**Degree 4.** There are 68 classes among the $2401$ monic quartics. They are not listed here.

## GF(49)

$\mathrm{GF}(7)[x]/(f)$ for any irreducible monic quadratic $f$ is a field with $49$ elements, and all are **isomorphic**. There are $(49-7)/2=21$ monic irreducible quadratics, with the order of $x$ in $\mathrm{GF}(7)[x]/(f)$:

| polynomial | order of $x$ | primitive |
|---|---|---|
| $x^2+1$ | 4 |  |
| $x^2+3x+1$ | 8 |  |
| $x^2+\bar3x+1$ | 8 |  |
| $x^2+2$ | 12 |  |
| $x^2+\bar3$ | 12 |  |
| $x^2+3x+\bar1$ | 16 |  |
| $x^2+\bar1x+\bar1$ | 16 |  |
| $x^2+\bar3x+\bar1$ | 16 |  |
| $x^2+x+\bar1$ | 16 |  |
| $x^2+2x+2$ | 24 |  |
| $x^2+\bar1x+\bar3$ | 24 |  |
| $x^2+\bar2x+2$ | 24 |  |
| $x^2+x+\bar3$ | 24 |  |
| $x^2+2x+3$ | 48 | **yes** |
| $x^2+2x+\bar2$ | 48 | **yes** |
| $x^2+3x+\bar2$ | 48 | **yes** |
| $x^2+\bar1x+3$ | 48 | **yes** |
| $x^2+\bar2x+3$ | 48 | **yes** |
| $x^2+\bar2x+\bar2$ | 48 | **yes** |
| $x^2+\bar3x+\bar2$ | 48 | **yes** |
| $x^2+x+3$ | 48 | **yes** |

- $\mathrm{GF}(49)^\times$ is cyclic of order $48$. A **primitive** polynomial has $x$ of order $48$: there are $8$, which is $\varphi(48)/2$.
- With $f=x^2+1$: $i=x$ has order $4$, and the elements are $a+bi$ with $a,b$ balanced digits $\bar3,\dots,3$.

## Functions on GF(7) are polynomials

Every function from $\mathrm{GF}(7)$ to itself is a unique polynomial of degree at most $6$ ($7^7$ of each), because $x^7=x$.

**Exponentials need a lift.** $a^x$ has $x\in\mathbb Z/7$ but the exponent lives in $\mathbb Z/6$. With the balanced lift $x\in\{-3,\dots,3\}$ (the vault's convention):

| $a$ | values at $\bar3,\bar2,\bar1,0,1,2,3$ | polynomial | factorization |
|---|---|---|---|
| $1$ | $1,1,1,1,1,1,1$ | $1$ | |
| $2$ | $1,2,\bar3,1,2,\bar3,1$ | $\bar1x^6+\bar2x^5+x^4+2x^2+x+1$ | $-(x^6+2x^5+\bar1x^4+\bar2x^2+\bar1x+\bar1)$, the sextic irreducible |
| $3$ | $\bar1,\bar3,\bar2,1,3,2,\bar1$ | $x^6+\bar1x^5+\bar3x^3+2x^2+3x+1$ | irreducible sextic |
| $\bar3$ ($=4$) | $1,\bar3,2,1,\bar3,2,1$ | $\bar1x^6+2x^5+x^4+2x^2+\bar1x+1$ | $-(x^6+\bar2x^5+\bar1x^4+\bar2x^2+x+\bar1)$, the sextic irreducible |
| $\bar2$ ($=5$) | $\bar1,2,3,1,\bar2,\bar3,\bar1$ | $x^6+x^5+3x^3+2x^2+\bar3x+1$ | irreducible sextic |
| $\bar1$ ($=6$) | $\bar1,1,\bar1,1,\bar1,1,\bar1$ | $x^6+\bar2x^4+\bar1x^2+1$ | $(x^2+\bar3)^3$ |

- **Reflection:** $a^{-1}$ gives the polynomial of $a$ at $-x$: $p_{\bar3}(x)=p_2(-x)$ (since $\bar3=2^{-1}$) and $p_{\bar2}(x)=p_3(-x)$ (since $\bar2=3^{-1}$). The polynomial for $\bar1=\bar1^{-1}$ is even.
- **Unlike $\mathrm{GF}(5)$,** where the exponentials factored into primitive quadratics, here the four non-trivial ones are **irreducible sextics**: their roots live in $\mathrm{GF}(7^6)$. They are interpolation artefacts of the lift.
- **$(-1)^x$ is $(x^2-3)^3$**, with $x^2-3=x^2+\bar3$ irreducible (as $3$ is a nonsquare).

**Logarithms.** Take the values $0,1,\dots,5$ (written in $\mathrm{GF}(7)$ as $0,1,2,3,\bar3,\bar2$) and $\log0:=0$. The two **primitive** bases $3$ and $5=\bar2$ give logarithms on all of $\mathrm{GF}(7)^\times$:

| | values at $\bar3,\bar2,\bar1,0,1,2,3$ | polynomial | factorization |
|---|---|---|---|
| $\log_3$ | $\bar3,\bar2,3,0,0,2,1$ | $\bar1x^6+\bar3x^5+x^4+3x^3+\bar2x^2+2x$ | $-x\,(x-1)\,(x^4+\bar3x^3+3x^2+2)$ |
| $\log_5$ ($5=\bar2$) | $2,1,3,0,0,\bar3,\bar2$ | $\bar1x^6+2x^5+\bar2x^4+3x^3+x^2+\bar3x$ | $-x\,(x-1)\,(x^4+\bar1x^3+x^2+\bar2x+\bar3)$ |

Both vanish at $0$ and $1$, and the quartic factor is irreducible, so there are no other zeros. $\log_5=-\log_3$ as integers mod $6$, but the lifts to $\mathrm{GF}(7)$ are not a ring map, so the polynomials are not negatives.

**The other bases are partial.** $2$ and $4=\bar3$ have order $3$, so $\log_2$ and $\log_4$ exist only on the subgroup $\{1,2,\bar3\}$, with values in $\mathbb Z/3$ ($\log_21=0$, $\log_22=1$, $\log_2\bar3=2$; and $\log_4\bar3=1$, $\log_42=2$). Everything outside the subgroup is undefined; setting it to $0$, as with $\log0$, gives polynomials. **That is a convention, and the answer depends on it.**

| | values at $\bar3,\bar2,\bar1,0,1,2,3$ | factorization |
|---|---|---|
| $\log_2$ | $2,0,0,0,0,1,0$ | $-3\,x\,(x+1)\,(x+2)^2\,(x-3)\,(x-1)$ |
| $\log_4$ ($4=\bar3$) | $1,0,0,0,0,2,0$ | $-3\,x\,(x+1)\,(x+2)\,(x-3)\,(x-1)^2$ |

Both are degree $6$ and split completely: they are $\bar3$ times a product of linear factors, with roots at the four points outside the subgroup and at $1$ ($\log1=0$), and a **double root** at one of $\bar2,1$ for the two bases.

The natural polynomial maps of $\mathrm{GF}(7)$ are $x\mapsto x^k$ with $k$ mod $6$; $a^x$ and $\log_a$ become polynomials only after fixing a lift.
