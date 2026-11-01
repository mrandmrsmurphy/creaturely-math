---
title: Fiat Numbers
type: concept
status: canonical
provenance: murphy (the two-direction picture, "fiat numbers", "inbred"); ai-synthesis (standard algebra; examples computed and checked exactly)
sources: "[[SRC Mathematics (raw, 2026-05)]]"
updated: 2026-10-07
---

# Fiat Numbers

The [[Number Hierarchy]] has two directions, and they ask different questions.

- **Down: exhibitability.** The 14 levels, from the counting numbers to the zeta values. Going down, you lose the ability to exhibit all the digits, but there is still a length that does the same trick: the diagonal of a unit square is $\sqrt2$, exhibited even though its digits never end ([[Constructible Numbers]]).
- **Across, orthogonal: fiat numbers.** At any level you can adjoin a number **by declaration**: a field extension such as $\varepsilon$, $i$ or $j$. These are not lost to exhibition. On the complex plane $i$ is plainly a right-angle rotation. What is declared is that the rotation is a *number*, something you may add and multiply like one. The declaration is justified by use, and they even appear to represent something in physical reality: the wavefunction of quantum mechanics is complex-valued.

Using a fiat number *inside itself* gives the "inbred" numbers: the complex numbers, then quaternions, octonions, and so on. Each step loses algebraic properties.

## Fiat numbers: adjoining a root of $x^2=a$

Over a base such as $\mathbb Q$, $\mathbb K$ or $\mathbb R$, there are three ways to adjoin a square root ($a=0,-1,+1$):

| fiat number | relation | exhibited as | numbers | keeps | loses |
|---|---|---|---|---|---|
| $i$ | $i^2=-1$ | a right-angle rotation of the plane | complex $a+bi$ | a field; commutative; associative | the order (no $i>0$ or $i<0$) |
| $j$ | $j^2=+1$, $j\ne\pm1$ | the reflection swapping the two axes, $\begin{pmatrix}0&1\\1&0\end{pmatrix}$ | split-complex $a+bj$ | commutative; associative | field: $(1+j)(1-j)=0$ (zero divisors) |
| $\varepsilon$ | $\varepsilon^2=0$ | the matrix $\begin{pmatrix}0&1\\0&0\end{pmatrix}$ | dual $a+b\varepsilon$ | commutative; associative | field: $\varepsilon$ has no inverse (nilpotent) |

- $\varepsilon$ is the infinitesimal of [[Infinitesimals]], with the matrix form $\begin{pmatrix}0&1\\0&0\end{pmatrix}$.
- $i$ is the fiat number behind the complex plane. The slope formulas of [[Sum of Slopes]] and [[Characteristic Length]] are the product $(1+im_A)(1+im_B)$ read in components.
- The base can be any level of the hierarchy: $\mathbb Q[\varepsilon]$, $\mathbb K(i)$ (the constructible numbers with $i$), and so on.

## Using a fiat number inside itself: "inbred" numbers

Doubling takes an algebra $A$ with a conjugation $\bar{\ }$ and forms pairs $(a,b)$, adding a new unit $\ell$ with $\ell^2=-1$. This is the Cayley–Dickson construction:

$$(a,b)(c,d)=(ac-\bar d\,b,\ da+b\,\bar c).$$

Starting from $\mathbb R$ and doubling repeatedly:

| algebra | dimension | what it loses relative to the one before |
|---|---|---|
| $\mathbb R$ | 1 | — (ordered field) |
| $\mathbb C$ | 2 | **order** |
| $\mathbb H$ quaternions | 4 | **commutativity** |
| $\mathbb O$ octonions | 8 | **associativity** (still alternative, still a division algebra) |
| $\mathbb S$ sedenions | 16 | **alternativity and division**: nonzero numbers can multiply to $0$; the norm is no longer multiplicative |

Hurwitz's theorem: normed division algebras exist only in dimensions $1,2,4,8$, so $\mathbb O$ is the last stop before division fails.

Checked exactly with this construction (basis $e_0=1$, and $e_{2^n+k}=(0,e_k)$):

- **Quaternions:** $e_1e_2=e_3$ but $e_2e_1=-e_3$: not commutative.
- **Octonions:** $(e_1e_2)e_4=e_7$ but $e_1(e_2e_4)=-e_7$: not associative.
- **Sedenions:** $(e_3+e_{10})(e_6-e_{15})=0$ with both factors nonzero: zero divisors.

Doubling with $\ell^2=+1$ instead gives the split versions (split-quaternions, split-octonions), which have zero divisors earlier.

## Two gradients of losing the word "number"

The entire number hierarchy is a gradient of losing the meaning of the word *number*, and so is the fiat axis, but in a different way.

- **Down the hierarchy** the number is still exhibited, but less and less of its digits and its exactness: an exact count, a ratio, a length, a number known only by a process, a number that is only the name of a summation method.
- **Across** the number is exhibited at once (a rotation, a reflection, a matrix), but the *algebra* thins: the order goes first, then commutativity, then associativity, then division.
- They are orthogonal because they are different losses. Fiat numbers are useful, and they appear to represent something in physical reality.
- The fiat axis ends usefully at $\mathbb O$ (Hurwitz).

## Hard problem

What is the certificate for a declared number? The relation ($i^2=-1$) says what it does, and the representation (a rotation, a matrix) exhibits it. In the vocabulary of [[Future Directions]] item 3, **[AI]** the certificate of a fiat number is its *representation*. Whether usefulness, including physical usefulness, is part of the certificate is open.
