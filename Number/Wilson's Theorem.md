---
title: Wilson's Theorem
type: theorem
status: "canonical (adopted whole; it is exact, and useless as a test at scale)"
provenance: "murphy (the position, adopt what is finite and exact; the cost remark, adopted 2026-11-04) + ai-synthesis (proof, examples)"
sources: "[[Fermat's Little Theorem]], [[Modular Arithmetic]], [[Fundamental Theorem of Arithmetic]], [[Certificates]]"
updated: 2026-10-09
---

# Wilson's Theorem

> **Statement.** An integer $n>1$ is prime if and only if $(n-1)!\equiv-1\pmod n$.

**Adopted whole.** Finite, exact, and an *if and only if*, which [[Fermat's Little Theorem]] is not.

## Proof

*Prime $\Rightarrow$.* Mod a prime $p$ every unit $a\in\{1,\dots,p-1\}$ has a unique inverse ([[Modular Arithmetic]]). A unit is its own inverse only if $a^2\equiv1$, i.e. $p\mid(a-1)(a+1)$, so $a\equiv\pm1$ because $p$ is prime. The other $p-3$ units pair off $a\leftrightarrow a^{-1}$ with product $1$, leaving $(p-1)!\equiv1\cdot(-1)=-1$. For $p=11$ the pairs are $2\!\cdot\!6,\ 3\!\cdot\!4,\ 5\!\cdot\!9,\ 7\!\cdot\!8$ (each product $\equiv1$) and the only self-inverses are $1,10$ (checked).

*Composite $\Rightarrow$ not.* If $n=ab$ with $1<a\le b<n$ and $a<b$, both $a,b$ appear in $(n-1)!$, so $n\mid(n-1)!$ and $(n-1)!\equiv0$. If $n=a^2$ with $a>2$, then $a$ and $2a<n$ both appear, so again $n\mid(n-1)!$. Only $n=4$ is left: $3!=6\equiv2\ne-1$.

## Examples (checked)

- $p=2,3,5,7,11,13$: $(p-1)!\bmod p=1,2,4,6,10,12$, i.e. $-1$ each time.
- Composites $4,\dots,25$: $(n-1)!\bmod n$ is $0$ except $n=4$ where it is $2$.
- $12!=479001600\equiv12\pmod{13}$.

## Generalisation (Gauss)

The product of all units mod $n$ is $-1$ when $n=4,\ p^k,\ 2p^k$ ($p$ an odd prime) and $+1$ otherwise. Checked: it is $-1$ for $n=9,10$ and $+1$ for $n=8,12,15$.

## Cost: exact and useless as a test

Wilson's theorem is a perfect *characterisation* of primes and a poor *procedure*. Computing $(n-1)!\bmod n$ takes about $n$ multiplications, which is **exponential in the digits** of $n$. By contrast the Fermat witness takes $\sim\lceil\log_2\rceil(n)$ steps ([[Fermat's Little Theorem]]) and trial division about $\sqrt n$. For $n\approx10^{200}$ the Wilson product is past any budget.

The factorial itself is past the threshold long before $n$ is: $100!$ has $158$ digits and $200!$ has $375$, so $(n-1)!$ for $n>150$ or so is notation, not a number you hold, even though its residue mod $n$ is perfectly defined. Wilson's theorem is a good example of the point in [[Creational Ultrafinitism]]: a true statement in which the written object, $(n-1)!$, is not the thing one can possess, yet the finite residue procedure is meaningful for small $n$.

A teaching use is real: it gives the cleanest proof that $\mathbb Z/p$ is a field in which only $\pm1$ square to $1$ ([[GF(5)]], [[GF(7)]]).

## Hard problems

1. Whether the vault uses Wilson as the definition-level characterisation of "prime" in the primes page still to be written.
2. The count of steps is stated for the naive product; faster factorial-mod-$p$ methods exist (recollection, not checked here).
