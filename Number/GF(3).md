---
title: GF(3)
type: concept
status: canonical (draft)
provenance: "murphy+ai (Murphy's brief: the same treatment as GF(5), with balanced digits; worked material computed and checked exactly)"
sources: "Murphy's 2023–24 Confession of Mathematics"
updated: 2026-10-08
---

# GF(3)

The field with three elements: the integers mod $3$ ([[Modular Arithmetic]]) with all four operations. It is the smallest field after $\mathrm{GF}(2)$, and the easiest case of the treatment given to [[GF(5)]].

**Balanced residues.** The three elements are written $\bar1,\ 0,\ 1$, with $\bar1=-1\equiv2$. These are exactly the digits of [[Balanced Ternary]]. So the digit-by-digit arithmetic of that page, with the carries dropped, *is* arithmetic in $\mathrm{GF}(3)$.

*Note:* Every table and every count on this page was computed and verified exactly.

## Addition

| | $\bar1$ | $0$ | $1$ |
|---|---|---|---|
| **$\bar1$** | $1$ | $\bar1$ | $0$ |
| **$0$** | $\bar1$ | $0$ | $1$ |
| **$1$** | $0$ | $1$ | $\bar1$ |

- It is the cyclic group of order $3$. Negation swaps $1$ and $\bar1$, and every row is a rotation of the first.
- $1+1=\bar1$ and $\bar1+\bar1=1$: the digit sums of [[Balanced Ternary]] ($1+1=2=1\bar1$) with the carry removed.

## Multiplication

| | $\bar1$ | $0$ | $1$ |
|---|---|---|---|
| **$\bar1$** | $1$ | $0$ | $\bar1$ |
| **$0$** | $0$ | $0$ | $0$ |
| **$1$** | $\bar1$ | $0$ | $1$ |

- The nonzero elements $\bar1,1$ form a cyclic group of order $2$: the **sign group**. Multiplication is the rule of signs, with $0$ absorbing.
- Every nonzero element is its own inverse.

## Exponents

| $x$ | $x^0$ | $x^1$ | $x^2$ | order |
|---|---|---|---|---|
| $\bar1$ | $1$ | $\bar1$ | $1$ | 2 |
| $0$ | 1 | $0$ | $0$ | — |
| $1$ | $1$ | $1$ | $1$ | 1 |

- **Fermat:** $x^2=1$ for every $x\ne0$, and $x^3=x$ for every $x$.
- $\bar1$ is the only element of order $2$, so it is the **only primitive root**. Every nonzero element is a power of $\bar1$: $1=\bar1^0=\bar1^2$ and $\bar1=\bar1^1$.
- **Discrete logarithm base $\bar1$:** $\log_{\bar1}1=0$ and $\log_{\bar1}\bar1=1$, in $\mathbb Z/2$. (The base $2$ is the same element, since $2\equiv\bar1$. A base $3$ would be $0$.)

## Squares

The squares are $0$ and $1$. So **$\bar1$ is not a square**: $x^2=\bar1$ has no solution in $\mathrm{GF}(3)$.

- This is the opposite of $\mathrm{GF}(5)$, where $2^2=\bar1$. Here the fiat number $i$ of [[Fiat Numbers]] is genuinely needed: adjoining $i$ with $i^2=\bar1$ gives a new field, $\mathrm{GF}(9)$.
- In the Gaussian integers, $3$ is prime, and $\mathbb Z[i]/(3)\cong\mathrm{GF}(9)$ (a standard fact; $5=(2+i)(2-i)$ splits, which is why $\mathbb Z[i]/(2+i)\cong\mathrm{GF}(5)$).

## Polynomials over GF(3)

**Identities.** Every element is a root of $x^3-x$: $x^3-x=x(x-1)(x+1)$. Also $x^2-1=(x-1)(x+1)$ and $x^2+1$ is irreducible, so $x^4-1=(x-1)(x+1)(x^2+1)$. And
$$x^4+1=(x^2+x+\bar1)(x^2+\bar1x+\bar1),$$
a product of the two **primitive** quadratics, since $(x^2-1)^2-x^2=x^4-3x^2+1=x^4+1$. This is the cyclotomic polynomial $\Phi_8$, the counterpart of $\Phi_{24}$ over $\mathrm{GF}(5)$.

**Up to isomorphism.** As in $\mathrm{GF}(5)$: two monic polynomials are the same class when one becomes the other under $x\mapsto\lambda x+\mu$ ($\lambda\ne0$). There are $2\cdot3=6$ such substitutions. **There is no depressed form for cubics here:** the substitution $x\mapsto x+\mu$ changes the $x^2$ coefficient of a cubic by $3\mu=0$, so it can never be removed. So the classes of cubics are listed with all their members.

**Degree 1.** One class: $x$.

**Degree 2.** Three classes, $9$ polynomials in all.

| class | size | the polynomials |
|---|---|---|
| double root | 3 | $x^2$, $x^2+x+1$, $x^2+\bar1x+1$ |
| irreducible | 3 | $x^2+1$, $x^2+x+\bar1$, $x^2+\bar1x+\bar1$ |
| two distinct roots | 3 | $x^2+\bar1$, $x^2+x$, $x^2+\bar1x$ |

**Degree 3.** Seven classes, $27$ polynomials in all.

| class | size | the polynomials |
|---|---|---|
| a double root and a simple root | 6 | $x^3+x^2$, $x^3+x^2+x$, $x^3+x^2+\bar1x+\bar1$, $x^3+\bar1x^2$, $x^3+\bar1x^2+x$, $x^3+\bar1x^2+\bar1x+1$ |
| irreducible | 6 | $x^3+x^2+\bar1$, $x^3+x^2+x+\bar1$, $x^3+x^2+\bar1x+1$, $x^3+\bar1x^2+1$, $x^3+\bar1x^2+x+1$, $x^3+\bar1x^2+\bar1x+\bar1$ |
| irreducible | 2 | $x^3+\bar1x+1$, $x^3+\bar1x+\bar1$ |
| one root and an irreducible quadratic | 6 | $x^3+x^2+1$, $x^3+x^2+x+1$, $x^3+x^2+\bar1x$, $x^3+\bar1x^2+\bar1$, $x^3+\bar1x^2+x+\bar1$, $x^3+\bar1x^2+\bar1x$ |
| one root and an irreducible quadratic | 3 | $x^3+x$, $x^3+x+1$, $x^3+x+\bar1$ |
| three distinct roots | 1 | $x^3+\bar1x$ |
| triple root | 3 | $x^3$, $x^3+1$, $x^3+\bar1$ |

- The class of size $1$, $x^3-x$, is the polynomial of which every element is a root; it is fixed by every substitution.
- The two irreducible cubics of the size-$2$ class, $x^3-x\pm1$, are the **Artin-Schreier** polynomials: $f(x+1)=f(x)$ for $f=x^3-x\pm1$. Their roots generate $\mathrm{GF}(27)$.
- Eight cubics are irreducible, $(27-3)/3=8$, in the two irreducible classes.

**Degree 4.** There are 18 classes among the $81$ monic quartics. They are not listed here.

## GF(9)

$\mathrm{GF}(3)[x]/(f)$ for any irreducible monic quadratic $f$ is a field with $9$ elements, and all are **isomorphic**. The three monic irreducible quadratics, with the order of $x$ in $\mathrm{GF}(3)[x]/(f)$:

| polynomial | order of $x$ | primitive |
|---|---|---|
| $x^2+1$ | 4 | |
| $x^2+x+\bar1$ | 8 | **yes** |
| $x^2+\bar1x+\bar1$ | 8 | **yes** |

- $\mathrm{GF}(9)^\times$ is cyclic of order $8$. A **primitive** polynomial has $x$ of order $8$; there are $2$.
- With $f=x^2+1$: the element $i=x$ has $i^2=\bar1$ and order $4$, and the nine elements are $a+bi$ with $a,b\in\{\bar1,0,1\}$. So $\mathrm{GF}(9)$ is the **Gaussian integers mod $3$**, with balanced digits.
- In $\mathrm{GF}(9)$, $\bar1=i^2$ is a square, and so is $i$ itself: an element of order $4$ in a cyclic group of order $8$ is the square of an element of order $8$.

## Functions on GF(3) are polynomials

Every function from $\mathrm{GF}(3)$ to itself is a unique polynomial of degree at most $2$ ($3^3=27$ of each), because $x^3=x$.

**Exponentials need a lift.** $a^x$ has $x\in\mathbb Z/3$ but the exponent lives in $\mathbb Z/2$, so a choice of lift is needed. With the balanced lift $x\in\{\bar1,0,1\}$ (the vault's convention, as in [[GF(5)]]):

| $a$ | values at $\bar1,0,1$ | polynomial | factorization |
|---|---|---|---|
| $1$ | $1,1,1$ | $1$ | |
| $\bar1$ ($=2$) | $\bar1,1,\bar1$ | $x^2+1$ | irreducible |

So **$(-1)^x$ is the irreducible polynomial $x^2+1$**, and $i$ is its root in $\mathrm{GF}(9)$. With the lift $x\in\{0,1,2\}$ instead, the values are $1,\bar1,1$ and the polynomial is $\bar1x^2+\bar1x+1=-(x^2+x+\bar1)$: a **primitive** polynomial.

**Logarithm.** The only base is $\bar1$. Taking $\log$ with values $0,1$ and $\log0:=0$:

| | values at $\bar1,0,1$ | polynomial | factorization |
|---|---|---|---|
| $\log_{\bar1}$ | $1,0,0$ | $\bar1x^2+x$ | $-x\,(x-1)$ |

It vanishes at $0$ and $1$, as it should.

## The affine group and the triangle

The substitutions $x\mapsto\lambda x+\mu$ ($\lambda=\pm1$) form a group of order $6$, nonabelian: the symmetry group of the equilateral triangle, with the three field elements as vertices ([[Symmetries of the Equilateral Triangle]]).

## Fiat numbers

$\mathrm{GF}(3)$ is the smallest field where the fiat number $i$ is genuinely adjoined, and $\mathrm{GF}(9)$ is what results. In $\mathrm{GF}(5)$, $i$ was already there ($2^2=\bar1$). A finite field has no order, so unlike the complex numbers it has nothing to lose at the first step.
