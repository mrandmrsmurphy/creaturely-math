---
title: Cyclic Groups
type: concept
status: canonical (draft)
provenance: "murphy+ai (Murphy's brief: document the cyclic groups $C_1$ through $C_8$; every table, generator list, subgroup list and element order below was computed and checked by exhaustive check)"
sources: "[[Groups]]"
updated: 2026-11-14
---

# Cyclic Groups

A group is **cyclic** when one element, a **generator**, produces all the others by repeated combining ([[Groups]]). The cyclic group of order $n$ is written $C_n$. Up to renaming its elements there is exactly one, and it is $(\mathbb Z/n,+)$, the clock arithmetic of [[Modular Arithmetic]]: the elements are $0,1,\dots,n-1$ and $a\cdot b$ means $a+b \bmod n$. It is also the group of rotations of a regular $n$-gon that carry it onto itself, with $1$ the smallest rotation: $C_3$ is the rotation subgroup $\{e,r,r^2\}$ of [[Symmetries of the Equilateral Triangle]] and $C_4$ is the rotation subgroup of [[Symmetries of the Square]].

*Note:* Every table below was checked against all four axioms by trying every case ($n^3$ associativity checks each), and every list of generators and subgroups was found by trying every element and every subset.

## The tables

Row $a$, column $b$, entry $a+b \bmod n$. Each is a Latin square, symmetric about its diagonal (cyclic groups are abelian), and each row is the row above it shifted one place left.

### $C_1$

| | $\mathbf{0}$ |
|---|---|
| $\mathbf{0}$ | $0$ |

### $C_2$

| | $\mathbf{0}$ | $\mathbf{1}$ |
|---|---|---|
| $\mathbf{0}$ | $0$ | $1$ |
| $\mathbf{1}$ | $1$ | $0$ |

### $C_3$

| | $\mathbf{0}$ | $\mathbf{1}$ | $\mathbf{2}$ |
|---|---|---|---|
| $\mathbf{0}$ | $0$ | $1$ | $2$ |
| $\mathbf{1}$ | $1$ | $2$ | $0$ |
| $\mathbf{2}$ | $2$ | $0$ | $1$ |

### $C_4$

| | $\mathbf{0}$ | $\mathbf{1}$ | $\mathbf{2}$ | $\mathbf{3}$ |
|---|---|---|---|---|
| $\mathbf{0}$ | $0$ | $1$ | $2$ | $3$ |
| $\mathbf{1}$ | $1$ | $2$ | $3$ | $0$ |
| $\mathbf{2}$ | $2$ | $3$ | $0$ | $1$ |
| $\mathbf{3}$ | $3$ | $0$ | $1$ | $2$ |

### $C_5$

| | $\mathbf{0}$ | $\mathbf{1}$ | $\mathbf{2}$ | $\mathbf{3}$ | $\mathbf{4}$ |
|---|---|---|---|---|---|
| $\mathbf{0}$ | $0$ | $1$ | $2$ | $3$ | $4$ |
| $\mathbf{1}$ | $1$ | $2$ | $3$ | $4$ | $0$ |
| $\mathbf{2}$ | $2$ | $3$ | $4$ | $0$ | $1$ |
| $\mathbf{3}$ | $3$ | $4$ | $0$ | $1$ | $2$ |
| $\mathbf{4}$ | $4$ | $0$ | $1$ | $2$ | $3$ |

### $C_6$

| | $\mathbf{0}$ | $\mathbf{1}$ | $\mathbf{2}$ | $\mathbf{3}$ | $\mathbf{4}$ | $\mathbf{5}$ |
|---|---|---|---|---|---|---|
| $\mathbf{0}$ | $0$ | $1$ | $2$ | $3$ | $4$ | $5$ |
| $\mathbf{1}$ | $1$ | $2$ | $3$ | $4$ | $5$ | $0$ |
| $\mathbf{2}$ | $2$ | $3$ | $4$ | $5$ | $0$ | $1$ |
| $\mathbf{3}$ | $3$ | $4$ | $5$ | $0$ | $1$ | $2$ |
| $\mathbf{4}$ | $4$ | $5$ | $0$ | $1$ | $2$ | $3$ |
| $\mathbf{5}$ | $5$ | $0$ | $1$ | $2$ | $3$ | $4$ |

### $C_7$

| | $\mathbf{0}$ | $\mathbf{1}$ | $\mathbf{2}$ | $\mathbf{3}$ | $\mathbf{4}$ | $\mathbf{5}$ | $\mathbf{6}$ |
|---|---|---|---|---|---|---|---|
| $\mathbf{0}$ | $0$ | $1$ | $2$ | $3$ | $4$ | $5$ | $6$ |
| $\mathbf{1}$ | $1$ | $2$ | $3$ | $4$ | $5$ | $6$ | $0$ |
| $\mathbf{2}$ | $2$ | $3$ | $4$ | $5$ | $6$ | $0$ | $1$ |
| $\mathbf{3}$ | $3$ | $4$ | $5$ | $6$ | $0$ | $1$ | $2$ |
| $\mathbf{4}$ | $4$ | $5$ | $6$ | $0$ | $1$ | $2$ | $3$ |
| $\mathbf{5}$ | $5$ | $6$ | $0$ | $1$ | $2$ | $3$ | $4$ |
| $\mathbf{6}$ | $6$ | $0$ | $1$ | $2$ | $3$ | $4$ | $5$ |

### $C_8$

| | $\mathbf{0}$ | $\mathbf{1}$ | $\mathbf{2}$ | $\mathbf{3}$ | $\mathbf{4}$ | $\mathbf{5}$ | $\mathbf{6}$ | $\mathbf{7}$ |
|---|---|---|---|---|---|---|---|---|
| $\mathbf{0}$ | $0$ | $1$ | $2$ | $3$ | $4$ | $5$ | $6$ | $7$ |
| $\mathbf{1}$ | $1$ | $2$ | $3$ | $4$ | $5$ | $6$ | $7$ | $0$ |
| $\mathbf{2}$ | $2$ | $3$ | $4$ | $5$ | $6$ | $7$ | $0$ | $1$ |
| $\mathbf{3}$ | $3$ | $4$ | $5$ | $6$ | $7$ | $0$ | $1$ | $2$ |
| $\mathbf{4}$ | $4$ | $5$ | $6$ | $7$ | $0$ | $1$ | $2$ | $3$ |
| $\mathbf{5}$ | $5$ | $6$ | $7$ | $0$ | $1$ | $2$ | $3$ | $4$ |
| $\mathbf{6}$ | $6$ | $7$ | $0$ | $1$ | $2$ | $3$ | $4$ | $5$ |
| $\mathbf{7}$ | $7$ | $0$ | $1$ | $2$ | $3$ | $4$ | $5$ | $6$ |

## Generators, element orders, subgroups

The **order** of $a$ in $C_n$ is $n/\gcd(a,n)$. The generators are the $a$ with $\gcd(a,n)=1$, the **units mod $n$**, and there are $\varphi(n)$ of them. *Subgroups* are in bijection with divisors of $n$: for each $d\mid n$ there is exactly one subgroup of order $d$, namely the multiples of $n/d$. All checked by trying every subset.

| $n$ | element orders of $0,1,\dots,n-1$ | generators | $\varphi(n)$ | subgroups (as sets) |
|---|---|---|---|---|
| $1$ | $1$ | $0$ | $1$ | $\{0\}$ |
| $2$ | $1,2$ | $1$ | $1$ | $\{0\}$, $C_2$ |
| $3$ | $1,3,3$ | $1,2$ | $2$ | $\{0\}$, $C_3$ |
| $4$ | $1,4,2,4$ | $1,3$ | $2$ | $\{0\}$, $\{0,2\}$, $C_4$ |
| $5$ | $1,5,5,5,5$ | $1,2,3,4$ | $4$ | $\{0\}$, $C_5$ |
| $6$ | $1,6,3,2,3,6$ | $1,5$ | $2$ | $\{0\}$, $\{0,3\}$, $\{0,2,4\}$, $C_6$ |
| $7$ | $1,7,7,7,7,7,7$ | $1,\dots,6$ | $6$ | $\{0\}$, $C_7$ |
| $8$ | $1,8,4,8,2,8,4,8$ | $1,3,5,7$ | $4$ | $\{0\}$, $\{0,4\}$, $\{0,2,4,6\}$, $C_8$ |

Three things to read off:

- **Prime order: no proper subgroups, every non-identity element a generator.** $C_2,C_3,C_5,C_7$. This is Lagrange's theorem at its smallest ([[Groups]]), and it is why every group of prime order is cyclic: any non-identity element generates a subgroup of size dividing $p$ that is not $1$.
- **Prime-power order: the subgroups form a single chain.** $C_4$: $1\mid2\mid4$; $C_8$: $1\mid2\mid4\mid8$. Each is contained in the next.
- **Composite order with two prime factors: the subgroups branch.** $C_6$ has the two proper subgroups $\{0,3\}$ and $\{0,2,4\}$, of orders $2$ and $3$, and neither contains the other. The number of subgroups of $C_n$ is the number of divisors of $n$: $1,2,2,3,2,4,2,4$ for $n=1,\dots,8$.

## $C_6$ is $C_2\times C_3$, but $C_4$ is not $C_2\times C_2$

Pair each element of $\mathbb Z/6$ with its residues mod $2$ and mod $3$: $a\mapsto(a \bmod 2,\ a \bmod 3)$. This is a bijection ($0\mapsto(0,0)$, $1\mapsto(1,1)$, $2\mapsto(0,2)$, $3\mapsto(1,0)$, $4\mapsto(0,1)$, $5\mapsto(1,2)$) and it carries addition to componentwise addition. So $C_6\cong C_2\times C_3$. This is the [[Chinese Remainder Theorem]] read as group theory, and it works whenever the two orders have no common factor.

When they do, it fails. $C_2\times C_2$ is the Klein four-group, in which every element has order $\le2$, while $C_4$ has two elements of order $4$ ([[Groups]]). Likewise $C_8$, $C_2\times C_4$ and $C_2\times C_2\times C_2$ all have order $8$ and are pairwise different, told apart by their element orders (checked by listing every element):

| group | elements of order $1,2,4,8$ |
|---|---|
| $C_8$ | $1,1,2,4$ |
| $C_2\times C_4$ | $1,3,4,0$ |
| $C_2\times C_2\times C_2$ | $1,7,0,0$ |

These three, with $D_4$ and $Q_8$ ([[Symmetries of the Square]]), are all five groups of order $8$; three are abelian and two are not.

## $C_n$ inside the dihedral group

$C_n$ is the subgroup of rotations of the dihedral group $D_n$ (order $2n$), which adds $n$ reflections. $C_3\subset D_3$ and $C_4\subset D_4$ are on the two symmetry pages, and in each the rotation subgroup is **normal** with quotient $C_2$: rotation versus reflection, the orientation of the figure. $D_3$ and $D_4$ are the first two nonabelian groups in the vault. No cyclic group is nonabelian, so the cyclic groups are the abelian end of the list.

The other groups of order up to $15$, and the arguments that no others exist, are on [[Groups of Small Order]].

## Where the cyclic groups already appear

- **$\mathrm{GF}(p)^\times\cong C_{p-1}$**, generated by a primitive root: $C_2$ for [[GF(3)]], $C_4$ for [[GF(5)]], $C_6$ for [[GF(7)]], $C_{10}$ for [[GF(11)]].
- **The additive group of every prime field** $\mathrm{GF}(p)$ is $C_p$. The addition tables of [[GF(3)]], [[GF(5)]] and [[GF(7)]] are the tables above for $n=3,5,7$.
- **Units mod $n$** need not be cyclic: the units mod $8$ are the Klein four-group, not $C_4$ ([[Groups]]).
