---
title: Fermat's Little Theorem
type: theorem
status: "canonical (adopted whole; the converse fails, and that is the useful part)"
provenance: "murphy (the position, adopt what is finite and exact) + ai-synthesis (proofs, examples, the cost, the Fermat witness)"
sources: "[[Modular Arithmetic]], [[Chinese Remainder Theorem]], [[Fundamental Theorem of Arithmetic]], [[Certificates]]"
updated: 2026-10-09
---

# Fermat's Little Theorem

> **Statement.** If $p$ is prime and $p\nmid a$, then $a^{p-1}\equiv1\pmod p$. Equivalently, for every $a$: $a^p\equiv a\pmod p$.

**Adopted whole.** It is finite, exact, and proved by direct computation; nothing in it asks for a completed infinity.

## Three proofs

1. **Permutation.** For $p\nmid a$, multiplication by $a$ permutes the units $1,\dots,p-1$ mod $p$ (it is invertible, [[Modular Arithmetic]]). So $a\cdot2a\cdots(p-1)a\equiv(p-1)!$, i.e. $a^{p-1}(p-1)!\equiv(p-1)!$. Cancel $(p-1)!$, a unit because $p$ is prime. Mod $7$, $a=3$: $3,6,2,5,1,4$ is a rearrangement of $1,\dots,6$ (checked).
2. **Binomial.** $(x+y)^p\equiv x^p+y^p\pmod p$, since $p\mid\binom pk$ for $0<k<p$. Induct on $a$: $(a+1)^p\equiv a^p+1\equiv a+1$.
3. **Necklaces.** There are $a^p-a$ colourings of $p$ beads with $a$ colours that are not constant; rotation groups them into orbits of size exactly $p$. So $p\mid a^p-a$. For $a=2,p=5$: $30=5\cdot6$; for $a=3$: $240=5\cdot48$ (checked).

## Examples (checked)

- $a^6\bmod7=1$ for $a=1,\dots,6$; $a^7\equiv a$ for $a=0,\dots,6$.
- **Inverses for free:** $a^{-1}\equiv a^{p-2}$. Mod $7$: $3^5\equiv5$ and $3\cdot5=15\equiv1$. Mod $17$: $10^{15}\equiv12$ and $10\cdot12=120\equiv1$.

## The converse fails, and that is useful

If $a^{n-1}\not\equiv1\pmod n$ for some $a$ coprime to $n$, then $n$ is **certainly composite**. This is the **Fermat witness** used on $C=(10^{200}+23)/141$ in [[Fundamental Theorem of Arithmetic]]: a cheap certificate of a *negative*, which the vault accepts, and which yields no factor.

The reverse does not hold:
- $2^{340}\equiv1\pmod{341}$ though $341=11\cdot31$; base $3$ exposes it ($3^{340}\equiv56$).
- $561$, $1105$, $1729$ are the **Carmichael numbers** below $2000$ (composites with $a^{n-1}\equiv1$ for every $a$ coprime to $n$; found by exhaustive search). For $561$ the base $3$ gives $375$ only because $\gcd(3,561)=3$, which already factors it.

So "$a^{n-1}\equiv1$" certifies nothing positive. A positive primality certificate is a different object ([[Fundamental Theorem of Arithmetic]], flagged there as unverified).

## Cost

Computing $a^{e}\bmod n$ by repeated squaring takes about $\lceil\log_2\rceil(e)$ squarings and multiplications mod $n$ (the symbol of [[Intermediate Value Theorem]]): $665$ for an exponent near $10^{200}$. Linear in the digits, so the check is cheap at any size.

## Generalisations

- **Euler** ([[Euler's Theorem]]): $a^{\varphi(n)}\equiv1\pmod n$ for $\gcd(a,n)=1$, with $\varphi(n)$ the count of units. For $n=15$, $\varphi=8$ and every unit's 8th power is $1$ (checked).
- **Via CRT:** reduce to prime-power moduli ([[Chinese Remainder Theorem]]).
- **In a finite field:** $x^{q}=x$ for every element of $\mathrm{GF}(q)$ ([[GF(3)]], [[GF(5)]], [[GF(7)]], [[GF(11)]]): the whole field is the roots of $x^q-x$.

## Hard problems

1. Whether the vault's page on primes should state a positive certificate (Pratt-style) beside the Fermat witness.
2. The exact count of $a$ that are witnesses for a given composite $n$ is not stated.
