---
title: Fundamental Theorem of Arithmetic
type: theorem
status: canonical (kept; the qualification is about what "number" means)
provenance: "murphy (the position, keep the theorem, every number, the 10^200+23 challenge) + ai-synthesis (proofs, costs, the factored example, flagged problems)"
sources: "[[Creational Ultrafinitism]], [[Certificates]], [[Number Hierarchy]]"
updated: 2026-10-09
---

# Fundamental Theorem of Arithmetic

> **Every number greater than 1 is a product of primes, in exactly one way** (up to the order of the factors).

A **prime** is a number greater than 1 whose only divisors are $1$ and itself. $1$ is not a prime (else $6=2\cdot3=1\cdot2\cdot3$ would be two factorizations); it is the empty product. Examples: $360=2^3\cdot3^2\cdot5=2\cdot2\cdot2\cdot3\cdot3\cdot5$, in no other way.

The theorem is **kept**. Nothing in the vault contradicts it: it is proved by finite, constructive steps ([[Certificates]]). What it needs is the word *number* taken seriously: "every **number**" means every number you can hold ([[Creational Ultrafinitism]]), and a numeral you can write is not thereby a number.

## Existence

*Claim.* Each $n\ge2$ is a product of primes.

*Proof.* If $n$ is prime, done. If not, $n=ab$ with $1<a,b<n$; factor $a$ and $b$ (strong induction, bounded by $n$) and multiply.

*Procedure.* Divide by $2,3,4,\dots$ and by each divisor found, until what is left is $1$. For $360$: $360=2\cdot180=2\cdot2\cdot90=2\cdot2\cdot2\cdot45=\dots$ gives $2,2,2,3,3,5$. The procedure stops after at most $\sqrt n$ trial divisions plus the factors found, so its cost grows like $\sqrt n$, which is **exponential in the number of digits**.

## Uniqueness

*Euclid's lemma.* If a prime $p$ divides $ab$, then $p\mid a$ or $p\mid b$.

*Proof.* Suppose $p\nmid a$. Then $\gcd(a,p)=1$, so the Euclidean algorithm produces $x,y$ with $ax+py=1$. Multiply by $b$: $b=(ab)x+p(by)$. Both terms are divisible by $p$, so $p\mid b$. $\square$

Worked example: $p=7$, $a=6$, $b=14$, $ab=84$. Here $6\cdot(-1)+7\cdot1=1$, and $14=84\cdot(-1)+7\cdot14=-84+98$, visibly divisible by $7$.

*Uniqueness.* If $p_1\cdots p_r=q_1\cdots q_s$ with all factors prime, then $p_1$ divides the right side, so by the lemma divides some $q_j$, so equals it (both prime). Cancel and repeat. After $r$ steps the factorizations match. $\square$

The Euclidean algorithm takes about as many steps as the number has digits, so **uniqueness is feasible at any size**: it never *finds* a factor, it only compares two factorizations you already hold.

## Four claims that are often run together [AI]

| Claim | What it asks for | Cost | In this vault |
|---|---|---|---|
| **Existence**: $n$ has a prime factorization | a procedure | trial division, $\sim\sqrt n$ steps | constructive and true for every $n$; it *produces* the factorization only while that is affordable |
| **Uniqueness** | two factorizations in hand | gcd, $\sim$ digits | affordable at any size |
| **Verification**: this list is the factorization | multiply, and certify each factor prime | multiplication is cheap; primality certificates are cheap (below) | the certificate for "$n=p_1\cdots p_r$" |
| **Finding** the factors | a search | no known cheap method | the horizon |

So the theorem is not endangered by large $n$; what large $n$ breaks is only the *finding* of the factorization, and with it the right to say "the factorization is $\dots$" of a number whose factorization you do not hold. That is the discipline the vault asks: before the equals sign, name the certificate.

## The challenge: $10^{200}+23$

Murphy's question to a critic: *factor $10^{200}+23$.* All figures here are exact:

$$10^{200}+23=3\cdot47\cdot C,\qquad C=\frac{10^{200}+23}{141},$$

with $C$ a **198-digit** number. The first two factors fall out of a divisibility test ($3$ divides it because the digit sum is $6$; $47$ by one division). Then:

- $C$ has **no prime factor below $2\times10^6$** (trial division).
- $C$ is **composite**, certified by a *Fermat witness*: $2^{C-1}\not\equiv1\pmod C$ (one modular exponentiation; the residue is a 198-digit number beginning $4095145\ldots$). If $C$ were prime that power would be $1$.
- Nothing in that certificate gives a factor of $C$.

So the question has a **partial answer in hand** ($3$, $47$, and a *certificate that $C$ is not prime*) and **no further answer**. This is the clean case of a [[Certificates]] point: the vault accepts proof by contradiction for a **negative** ("$C$ is not prime") and refuses to treat it as the **existence** claim ("here are $a,b>1$ with $ab=C$"). "$C$ has a prime factorization" is true, and "the prime factorization of $C$" is a name for something not possessed.

**A fairer challenge** [AI]: the example is partly factorable, so as stated it is a weaker rebuttal than it looks. It works best with a number that survives a first pass, such as $C$ itself, or a product of two primes of a hundred digits each (which one can build and *know* the factorization of, while the critic cannot find it). The point is not that factoring is impossible but that **possessing the factorization is a matter of resources**: the *factoring horizon* depends on the budget (a person with a computer, a worldwide effort, a physical bound) and lies **far below the naming horizon**, since $10^{200}$ is a number one can *count* to in principle but one cannot *factor* in practice. *Unverified recollection to check:* general 200-digit numbers (RSA-200, 2005) and 250-digit numbers (RSA-250, 2020) have been factored with enormous computation, so $C$ itself is at the edge of what an organized world effort has done; the right statement is resource-relative ([[Future Directions]] item 2c), not a single cutoff.

## Primes and certificates

Certifying a *factorization* is cheap. [AI] *Unverified recollections to check:* Pratt (1975) showed every prime has a short certificate (primes are in NP: a witness that $p-1$ factors as claimed and a generator, recursively), and Agrawal–Kayal–Saxena (2002) gave a deterministic polynomial-time primality test. If right, "$p$ is prime" is checkable far more cheaply than "find the factors of $n$", which is why the first claim of a factorization can be certified even when the second cannot be found.

## What the theorem is for

- **Every positive rational is a list of integer exponents** over the primes (positive for numerator, negative for denominator): $\tfrac{12}{35}=2^2\cdot3\cdot5^{-1}\cdot7^{-1}$. Multiplication is adding the lists. This is how the integers and rationals are *built* from atoms.
- **gcd and lcm** by exponents ($\gcd$ takes the minimum, lcm the maximum), though the Euclidean algorithm computes gcd without factoring.
- **$\sqrt2$ is not rational:** in $a^2=2b^2$ the prime $2$ appears with an even exponent on the left and an odd one on the right, against uniqueness. A negative result, accepted ([[Certificates]]).
- **Primes are the *why* of the fields** $\mathbb Z/p$ ([[Modular Arithmetic]], [[GF(3)]], [[GF(5)]], [[GF(7)]], [[GF(11)]]).
- **Infinitely many primes:** from any list $p_1,\dots,p_k$, take $p_1\cdots p_k+1$; by *existence* it has a prime factor, and it is on no list. A potential-infinity statement: you produce the next prime, you do not hold all of them ([[Proof Types]]). The next prime may be past the threshold.

## The theorem depends on the structure

"Every number" must be *which* numbers. In $\mathbb Z[\sqrt{-5}]=\{a+b\sqrt{-5}\}$:

$$6=2\cdot3=(1+\sqrt{-5})(1-\sqrt{-5}).$$

Both are products of irreducibles: no element has "norm" $a^2+5b^2=2$ or $3$, so none of the four factors splits further. Unique factorization fails. In the Gaussian integers $\mathbb Z[i]$ it holds. So the theorem is a fact about **the integers** (and some rings of the same kind), proved from the Euclidean algorithm ([[Structure Hierarchies]], rung 6: PID, UFD), and not a property of "numbers" in general: the word *number* ([[Number Hierarchy]]) hides a choice of structure.

## Hard problems

1. **The horizon as a function.** Where do the claims "$n$ has a factorization" and "this is the factorization of $n$" part company, as a function of the budget? It is the resource-relative threshold of [[Future Directions]] item 2c, now for a concrete problem.
2. **Existence for what is not held.** For $n$ past the threshold ("notation, not a number"), the sentence "$n$ has a prime factorization" is carried by the procedure alone and is not a claim about a held number. Whether the vault states the theorem as a *schema over the numbers you can reach* (as for induction, [[Future Directions]] item 6) is open.
3. **Pratt and AKS.** The remarks on primality certificates are recollections; both need checking before they are relied on.
4. **The challenge.** Choose the example Murphy wants: $10^{200}+23$ as it stands is partly factored; $C$ is the 198-digit remainder.
