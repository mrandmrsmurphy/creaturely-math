---
title: Euler's Theorem
type: theorem
status: "canonical (adopted whole; one cost remark about computing the totient)"
provenance: "murphy (the position, adopt what is finite and exact; the totient remark, adopted 2026-11-04) + ai-synthesis (proof, examples)"
sources: "[[Fermat's Little Theorem]], [[Chinese Remainder Theorem]], [[Modular Arithmetic]], [[Fundamental Theorem of Arithmetic]]"
updated: 2026-10-09
---

# Euler's Theorem

> **Statement.** If $\gcd(a,n)=1$ then $a^{\varphi(n)}\equiv1\pmod n$, where $\varphi(n)$ is the number of integers in $1,\dots,n$ coprime to $n$.

**Adopted whole.** It is [[Fermat's Little Theorem]] with the prime replaced by any modulus, with the same proof, and it is finite and exact.

## Proof

The units mod $n$ are the $\varphi(n)$ residues coprime to $n$. Multiplication by a unit $a$ permutes them, so the product of all units is unchanged: $a^{\varphi(n)}U\equiv U$ with $U$ the product, itself a unit. Cancel $U$.

Mod $12$: the units are $1,5,7,11$ ($\varphi=4$), and multiplying by $5$ gives $5,1,11,7$, a rearrangement (checked).

## The totient

- $\varphi(p)=p-1$, $\varphi(p^k)=p^{k-1}(p-1)$.
- **Multiplicative** for coprime arguments, by the [[Chinese Remainder Theorem]] ($\mathbb Z/mn\cong\mathbb Z/m\times\mathbb Z/n$ matches units to pairs of units).
- Checked: $\varphi(12)=4$, $\varphi(15)=8$, $\varphi(36)=12$, $\varphi(49)=42$; $\varphi(12)=\varphi(4)\varphi(3)$; $\sum_{d\mid12}\varphi(d)=12$.

## Examples (checked)

- $7^{222}\bmod15$: $\varphi(15)=8$, $222\equiv6\pmod8$, so $7^{222}\equiv7^6\equiv4$.
- Last digit of $3^{100}$: $\varphi(10)=4$ and $4\mid100$, so $3^{100}\equiv1\pmod{10}$.

## It is not sharp

The least exponent that works for every unit, the **exponent of the group**, can be smaller than $\varphi(n)$. Mod $15$ every unit has fourth power $1$ though $\varphi=8$; mod $12$ every unit squares to $1$ though $\varphi=4$ (checked from the orders). Euler's theorem is true with $\varphi(n)$, and often with less.

## The one cost remark

The theorem is unobjectionable; **using it with $\varphi(n)$** requires knowing $\varphi(n)$, and for a general $n$ that is equivalent in difficulty to knowing its factorization ([[Fundamental Theorem of Arithmetic]]; the equivalence is a recollection to check). So for a large $n$ whose factors you do not hold, "$a^{\varphi(n)}\equiv1$" is true and unusable.

This is the other half of public-key arithmetic: the maker holds $p,q$, knows $\varphi(pq)=(p-1)(q-1)$ and so can invert exponentiation; others cannot. Toy case: $n=11\cdot13=143$, $\varphi=120$, $e=7$ has inverse $d=103$ mod $120$; $42^7\equiv81$ and $81^{103}\equiv42\pmod{143}$ (checked). This is the factoring horizon of [[Fundamental Theorem of Arithmetic]] in action.

## Hard problems

1. Whether the vault states the sharper exponent (the group exponent) as primary.
2. The equivalence of computing $\varphi(n)$ and factoring $n$ is cited, not proved here.
