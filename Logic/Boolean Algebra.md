---
title: Boolean Algebra
type: concept
status: canonical (draft)
provenance: "murphy+ai (Murphy's brief: $1+1=1$ is very special; list some identities, not all. Worked material checked by exhaustive truth table)"
sources: "[[SRC Confession of Mathematics (2023-24)]]"
updated: 2026-10-08
---

# Boolean Algebra

Algebra on two values, $0$ and $1$, with an addition, a multiplication and a complement:

$$\boxed{1+1=1}$$

Here $+$ means **or**, $\times$ means **and**, and $\bar x$ (or $x'$) means **not**. This is the arithmetic of [[Binary]] with a different addition. In ordinary arithmetic $1+1=2$; in [[Modular Arithmetic]] mod 2, $1+1=0$; in Boolean algebra $1+1=1$.

*[AI]* Historical remarks are from memory. Every identity listed was verified by checking all cases.

## The tables

| + | 0 | 1 |   | × | 0 | 1 |   | $x$ | $x'$ |
|---|---|---|---|---|---|---|---|---|---|
| **0** | 0 | 1 | | **0** | 0 | 0 | | 0 | 1 |
| **1** | 1 | 1 | | **1** | 0 | 1 | | 1 | 0 |

Multiplication is the same as in ordinary numbers and as mod 2. Only the single entry $1+1$ differs, and with it the whole algebra.

## Why $1+1=1$ is special

- **Idempotence.** $x+x=x$ and $x\cdot x=x$ for every element. In ordinary arithmetic only $0$ and $1$ satisfy $x^2=x$; here every element does, and the addition does it too.
- **No subtraction.** Nothing added to $1$ gives $0$, since $1+x=1$ always. So $1$ has no negative and the structure is **not a group under $+$**. Compare the additive group $\mathbb Z/n$ of [[Modular Arithmetic]], where every element has a negative. The step that created negatives from debt in [[Counting and Bases]] is unavailable here. Adding never undoes. Information accumulates and is not cancelled.
- **Adding is "at least one".** $x+y$ says that $x$ holds, or $y$ holds, or both. Counting how many does not matter; this is the point of the table, and it is the opposite of tally marks.
- **Order from addition.** Define $x\le y$ to mean $x+y=y$. This is the same as $xy=x$. It gives $0\le x\le1$ for all $x$, with $x+y$ the least element above both and $xy$ the greatest element below both.

## Some identities

Ordinary algebra holds for commutativity and associativity: $x+y=y+x$, $xy=yx$, $(x+y)+z=x+(y+z)$, and the same for products. Also $x+0=x$, $x\cdot1=x$, $x\cdot0=0$, $x+1=1$. The following are the distinctive ones.

| name | identity |
|---|---|
| idempotent | $x+x=x$, $\quad xx=x$ |
| complement | $x+x'=1$, $\quad xx'=0$ |
| double negation | $(x')'=x$ |
| absorption | $x+xy=x$, $\quad x(x+y)=x$ |
| distributive (both ways) | $x(y+z)=xy+xz$ and $\;x+yz=(x+y)(x+z)$ |
| De Morgan | $(x+y)'=x'y'$, $\quad(xy)'=x'+y'$ |

**The second distributive law is false in ordinary arithmetic.** With $x=y=z=2$: $2+2\cdot2=6$ but $(2+2)(2+2)=16$. In Boolean algebra the roles of $+$ and $\times$ are interchangeable: swap $+\leftrightarrow\times$ and $0\leftrightarrow1$ in any true identity and the result is also true (**duality**). De Morgan's laws are the dual pair.

**Example: absorption.** If $x=1$: $1+1\cdot y=1+y=1=x$ ✓. If $x=0$: $0+0\cdot y=0=x$ ✓. Two cases settle it.

## Three models

One structure, three costumes:

| | $0$ | $1$ | $+$ | $\times$ | $'$ |
|---|---|---|---|---|---|
| **Logic** | false | true | or | and | not |
| **Sets** (inside a universe $U$) | $\varnothing$ | $U$ | union | intersection | complement |
| **Switches** | open (off) | closed (on) | two switches in parallel | two in series | the opposite switch |

*Switches:* current flows through a parallel pair if either is closed, which is $x+y$; through a series pair only if both are closed, which is $xy$. This is why Boolean algebra describes circuits. Shannon showed in the late 1930s that switching circuits obey it, and Boole's original work was in the 1840s–50s *[AI]* from memory.

## Aristotle in Boole

Boole read a letter as a **class** and wrote the four categorical forms as equations:

| form | statement | equation |
|---|---|---|
| A | All $S$ are $P$ | $S(1-P)=0$ |
| E | No $S$ are $P$ | $SP=0$ |
| I | Some $S$ are $P$ | $SP\neq0$ |
| O | Some $S$ are not $P$ | $S(1-P)\neq0$ |

The product $SP$ is the class of things in both; $1-P$ is everything not in $P$. So "All $S$ are $P$" says that nothing in $S$ lies outside $P$, which is $S\subseteq P$, and in the order of this page $S\le P$.

**Barbara** (All $M$ are $P$; all $S$ are $M$; so all $S$ are $P$) becomes a calculation. From $S(1-M)=0$ we get $S=SM$, hence $S(1-P)=SM(1-P)=S\cdot[M(1-P)]=S\cdot0=0$ ✓.

**Existential import.** Traditional logic took "All $S$ are $P$" to presuppose that there *are* $S$'s, so "All unicorns are white" was false when no unicorns exist. The equation $S(1-P)=0$ says no such thing: if $S$ is empty ($S=0$) it holds for every $P$, and "All unicorns are white" is **vacuously true**. Modern logic ($\forall x[S(x)\to P(x)]$) adopts this reading, and the cost is that parts of the traditional square of opposition lapse for empty classes. With $S$ empty, A and E are both true, so they are no longer contraries; and A no longer implies I (the equation for I needs $SP\neq0$). The move is from a logic of what *is* to a logic of form.

## Where mod 2 comes back

The **exclusive or** $x\oplus y$ ("one or the other but not both") is addition mod 2. In Boolean terms $x\oplus y=xy'+x'y$, and arithmetically $x\oplus y=x+y-2xy$ when $x,y\in\{0,1\}$. With $\oplus$ as addition and $\times$ as multiplication, every Boolean algebra is also a **ring** in which $x^2=x$ and $x+x=0$. So the two additions on $\{0,1\}$ are related:

| | $1+1$ | negatives? | |
|---|---|---|---|
| $\mathbb N$ | $2$ | no | counting |
| mod 2 ($\oplus$) | $0$ | yes: $-x=x$ | parity |
| Boolean ($\vee$) | $1$ | no | at least one |

## Size

A finite Boolean algebra always has $2^k$ elements: it is the subsets of a $k$-element set. The number of distinct Boolean functions of $n$ variables is $2^{2^n}$: $16$ for $n=2$ and $256$ for $n=3$. Every Boolean function is a sum of minterms, one for each row of its truth table where it equals 1. Doubly exponential growth is a practical limit for any creature's handling of Boolean formulas.

## Certificates

*[AI]* Every identity above is decided by a finite truth table, which is the model case of a [[Certificates]]-style proof: the check is mechanical and short for few variables. The law of the excluded middle, $x+x'=1$, is the identity that the intuitionist school doubts when the statement $x$ ranges over an infinite domain ([[Schools Compared]]). For a statement decided by a finite check, the identity holds because the check can be carried out.

## Beyond two values

Adding a third value, *unknown*, with Boolean-style tables that decide whenever the known inputs decide, gives [[Three-Valued Logic]]. Boolean algebra is the part of it where nothing is unknown.

## Open points

- The Boolean algebra chapter is planned for *Precalculus for Everyone* ([[Counting and Bases]]); this page records the material and does not fix its place in a curriculum.
