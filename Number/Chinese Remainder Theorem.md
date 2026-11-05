---
title: Chinese Remainder Theorem
type: theorem
status: "canonical (adopted whole; one scale remark)"
provenance: "murphy (the position, adopt it wholesale; the scale remark, adopted 2026-11-04) + ai-synthesis (proof, worked examples)"
sources: "[[Modular Arithmetic]], [[Fundamental Theorem of Arithmetic]], [[Certificates]]"
updated: 2026-10-09
---

# Chinese Remainder Theorem

> **Statement.** If $m_1,\dots,m_k$ are pairwise coprime and $M=m_1\cdots m_k$, then for any residues $r_1,\dots,r_k$ the system $x\equiv r_i \pmod{m_i}$ has exactly one solution $x$ with $0\le x<M$.

**Adopted whole.** Nothing in it is objectionable: it is finite, exact, constructive, and its proof is an algorithm ([[Certificates]]: the solution is *exhibited*).

## Proof (a procedure)

Put $M_i=M/m_i$. Since $\gcd(M_i,m_i)=1$, the Euclidean algorithm gives $u_i$ with $M_iu_i\equiv1\pmod{m_i}$. Then
$$x=\sum_i r_iM_iu_i \bmod M$$
works: modulo $m_j$ every term but the $j$th contains the factor $m_j$ and vanishes, and the $j$th is $r_j\cdot1$.

*Uniqueness.* Two solutions differ by a number divisible by every $m_i$, hence by $M$ (coprime moduli), so they agree in $[0,M)$.

## Worked examples (checked)

- Sunzi's problem: $x\equiv2\ (3)$, $3\ (5)$, $2\ (7)$. $M=105$, and $x=23$.
- $x\equiv3\ (5)$, $x\equiv4\ (7)$: $x=18$ in $[0,35)$, the only one (checked by listing).
- **Ring form.** $\mathbb Z/15\to\mathbb Z/3\times\mathbb Z/5$, $x\mapsto(x\bmod3,\,x\bmod5)$, is a bijection that respects $+$ and $\times$. Multiplying $23\cdot17$ residue by residue mod $3,5,7,11$ gives $(1,1,6,6)$, which reconstructs to $391=23\cdot17$ in $[0,1155)$.

## Without coprime moduli

The system is solvable iff the congruences agree modulo each $\gcd(m_i,m_j)$, and then the solution is unique mod the lcm. $x\equiv1\ (4)$, $x\equiv3\ (6)$ gives $9\bmod12$; $x\equiv1\ (4)$, $x\equiv2\ (6)$ has no solution (both checked).

## The one remark: scale

Coprimality is checked by gcd, which is cheap; **no factoring is needed**. The theorem does not endanger the vault's position on "number" ([[Fundamental Theorem of Arithmetic]]), but it does hold a lesson. The reconstruction lives in $[0,M)$, and $M$ can pass the threshold even when every $m_i$ is small: the first $93$ primes (largest $487$) have a product past $10^{200}$ ([[Creational Ultrafinitism]]). Then:

- The residue tuple $(r_1,\dots,r_k)$ is a perfectly good finite object, and arithmetic on it is exact, one small modulus at a time.
- The integer $x<M$ it names is *notation, not a number* if $M>10^{200}$.

So CRT is kept in full, and its tuple form is the honest way to hold large quantities: **the residues are the number you hold; the big integer is what you may not claim to possess.** *(This is a reading for Murphy to accept or reject.)*

## Uses

- **Structure:** $\mathbb Z/mn\cong\mathbb Z/m\times\mathbb Z/n$ for coprime $m,n$; hence the unit group of $\mathbb Z/n$ splits into the unit groups of its prime-power parts, and cyclicity questions ([[Modular Arithmetic]]) reduce to prime powers.
- **Fields:** a product of fields $\mathrm{GF}(p)$ ([[GF(3)]], [[GF(5)]], [[GF(7)]]) is $\mathbb Z/M$ in disguise.
- **Computation:** residue-number arithmetic, and the calendar problem (periods of coprime lengths realign every $M$ steps).
- **History** *(unverified recollection)*: the problem is in Sunzi's *Suanjing*; Qin Jiushao gave the general method in 1247.

## Hard problems

1. Whether the vault states CRT in the tuple form as primary (above).
2. Cost: the Euclidean algorithm is linear in digits, so reconstruction is cheap; a bound with the sizes of $M_i$ is not written out.
