---
title: Bolzano–Weierstrass Theorem
type: theorem
status: "canonical (the exact statement rejected; a finite pigeonhole form and a metastable form kept)"
provenance: "murphy (the position, Bolzano–Weierstrass has to change or be rejected) + ai-synthesis (the missing modulus, the computability failure, the finite forms, the worked examples, the flagged problems)"
sources: "[[Extreme Value Theorem]], [[Certificates]], [[Creational Ultrafinitism]], [[Number Hierarchy]]"
updated: 2026-10-09
---

# Bolzano–Weierstrass Theorem

> **Standard statement.** Every bounded sequence of real numbers has a convergent subsequence.

It is the engine of the standard proofs of the [[Extreme Value Theorem]] and of Heine–Borel compactness, and so of everything downstream ([[Mean Value Theorem]] through Rolle).

## The standard proof, and where it asserts too much

Put the sequence in $[a,b]$. Bisect: one half contains **infinitely many terms**; keep that half and bisect again. This gives nested intervals shrinking to a point $L$ (by completeness). Choose indices $n_1<n_2<\dots$ with $x_{n_k}$ in the $k$th interval. Then $x_{n_k}\to L$.

Each step claims something:

1. **"One half contains infinitely many terms."** A finite procedure can inspect any stated number of terms, never an infinite tail, so it cannot decide which half. It is an *excluded-middle* step over an infinite totality.
2. **The indices $n_k$ are chosen from an infinite sequence.** Each choice is a finite act; the completed subsequence is not a finite object.
3. **The limit $L$** is a real number in the completed sense, which the vault does not hold ([[Certificates]], [[Number Hierarchy]]).
4. **The convergence has no rate.** "For every $\varepsilon$ there is a $K$" is asserted with no function $\varepsilon\mapsto K$. Without that function a convergent sequence is not a *number* in the vault's sense: a convergence certificate is a procedure with a **modulus** ([[Certificates]], levels 7–11).

The fourth is the decisive one, and the vault's own terms show it: a subsequence that "converges" without a modulus is not a certificate of anything.

## The failure is not only philosophical [AI]

Bolzano–Weierstrass **implies the monotone convergence theorem**: if $(x_n)$ is non-decreasing and bounded, a convergent subsequence has limit $L$, and monotonicity forces the whole sequence to converge to $L$. So any computable Bolzano–Weierstrass would give a computable limit (with a rate) to every computable bounded monotone sequence of rationals.

There are computable bounded monotone sequences of rationals whose limit is **not** computable: $x_n=\sum 2^{-k}$ over those $k\le n$ whose $k$th program has halted within $n$ steps (Specker's sequence). Every $x_n$ is an exact rational, found by running programs for $n$ steps; the limit is a sum over the halting set, so naming it to precision $2^{-j}$ would decide halting for the first $j$ programs. So **no procedure produces the subsequence with its limit and rate**, even for a sequence of rationals that is exactly known term by term. *(Unverified recollection to check: this is Specker 1949; in reverse mathematics Bolzano–Weierstrass is equivalent to arithmetical comprehension, and in constructive mathematics it is not provable without an omniscience principle, since monotone convergence already implies one. The derivation above is the part I checked.)*

## What stays

### Finite pigeonhole form

> **Theorem.** Let $x_1,\dots,x_N$ lie in an interval of length $\ell$, and let $\varepsilon>0$. Put $M=\lceil\ell/\varepsilon\rceil$. Then some $\lceil N/M\rceil$ of the terms lie within $\varepsilon$ of one another. Equivalently: among any $M(k-1)+1$ terms, some $k$ lie within $\varepsilon$.

*Proof.* Cut the interval into $M$ boxes of width at most $\varepsilon$. If every box held fewer than $\lceil N/M\rceil$ terms, the total would be fewer than $N$. $\square$

It is **exact**, finite, and elementary, and it states a *cluster in a finite sample at a stated precision*, with no limit and no subsequence.

**Worked example.** $x_n=(n^2\bmod101)/101$ for $n=1,\dots,50$, in $[0,1)$ with $M=10$ boxes of width $\tfrac1{10}$. The box counts are $5,6,6,4,4,4,4,6,6,5$; the guarantee is $\lceil50/10\rceil=5$, and the fullest box holds $6$.

**The bound is tight.** For $x_n=(n\bmod10)/10$ (the values $0,\tfrac1{10},\dots,\tfrac9{10}$ repeating) and $\varepsilon<\tfrac1{10}$, a cluster of $k$ terms needs $k$ equal values, and the first $N$ with $k$ equal terms is $N=10(k-1)+1$: $11,21,41$ for $k=2,3,5$, exactly $M(k-1)+1$.

**Cost.** A cluster of $k$ terms at precision $\varepsilon$ needs about $k\ell/\varepsilon$ terms of the sequence, **proportional to $1/\varepsilon$, exponential in the digits**, the same price as the grid of the EVT, and for the same reason: nothing is known about where the terms fall. Nesting does not help: after $j$ rounds with $M$ boxes each, $N\ge M^j$ terms are needed to keep one, which is again $\ell/\text{(final width)}$.

### Metastable form (monotone sequences) [AI]

For a monotone bounded sequence the question "does it converge" has no uniform answer (Specker), but a **finite** statement is true and has an explicit bound:

> **Theorem.** Let $0\le x_1\le x_2\le\dots\le1$, let $\varepsilon>0$, and let $F:\mathbb N\to\mathbb N$ be any function with $F(N)>N$. Then there is $N\le F^{(\lceil1/\varepsilon\rceil)}(1)$ with $x_{F(N)}-x_N<\varepsilon$.

*Proof.* Let $K=\lceil1/\varepsilon\rceil$, $N_0=1$ and $N_{i+1}=F(N_i)$. Suppose, for contradiction, that $x_{N_{i+1}}-x_{N_i}\ge\varepsilon$ for every $i=0,1,\dots,K$. Adding these $K+1$ gaps gives $x_{N_{K+1}}-x_{N_0}\ge(K+1)\varepsilon>1$, which is impossible for a sequence in $[0,1]$. So some $i\le K$ has $x_{N_{i+1}}-x_{N_i}<\varepsilon$; take $N=N_i\le N_K=F^{(K)}(1)$. $\square$

The point is that the sequence **does not move by more than $\varepsilon$ across the window $[N,F(N)]$**, for some $N$ found within an explicit bound that depends on $\varepsilon$ and $F$ only, not on the sequence.

**Worked example.** $F(N)=2N$, $\varepsilon=\tfrac1{10}$: the bound is $N\le2^{10}=1024$. It is **attained**: for $x_n=\tfrac1{10}\lfloor\log_2n\rfloor$ (capped at $1$) the first $N$ with $x_{2N}-x_N<\tfrac1{10}$ is exactly $N=1024$ (checked). For a slowly growing sequence, $x_n=1-\tfrac1{1+\lfloor\log_2n\rfloor}$, it is $N=4$ (checked). With $F(N)=N^2$ the bound is a tower: $F^{(3)}(2)=256$, and for $\varepsilon=\tfrac1{10}$ ten iterations of squaring.

This is the *finitary content* of convergence: not "there is a limit", but "on some window of stated size the sequence is stable to within $\varepsilon$". *(Unverified recollection to check: this is the "metastability" or "finite convergence principle" of Tao (2007), going back to Kreisel and Kohlenbach's proof mining; for general bounded sequences a metastable Bolzano–Weierstrass is known.)*

## What "converges" means in the vault

A **convergent sequence** is a sequence of rationals *with a modulus*: a function $K(\varepsilon)$ with $|x_m-x_n|\le\varepsilon$ for $m,n\ge K(\varepsilon)$. That pair is the certificate of a number at levels 7 to 11 ([[Number Hierarchy]]), and "complete" then means *by definition*: such a pair names a number. Completeness is not a theorem that Bolzano–Weierstrass would help prove; it is how numbers are *named*. What the vault drops is the claim that every bounded sequence can be *made* to carry one.

## What depended on it

- **[[Extreme Value Theorem]]:** replaced by the grid (ε-maximizer), proved without any subsequence.
- **Heine–Borel:** replaced by the finite cover of the grid ([[Extreme Value Theorem]], "Compactness").
- **Cauchy completeness:** by definition, above.
- **Weierstrass's other theorems** (uniform continuity on a closed interval, Arzelà–Ascoli, and so on): each needs its own treatment with a stated modulus; none is simply kept.

## Hard problems

1. **Metastability for general bounded sequences.** The monotone statement is proved above; the version for arbitrary bounded sequences (with a cluster at each stage) needs a statement and a proof in the vault's terms.
2. **The cost, again.** The pigeonhole bound is $\propto1/\varepsilon$. Is there a *structured* class of sequences (for instance, those generated by a rational map with a known Lipschitz constant) where a cluster is found in time linear in the digits?
3. **What replaces compactness** for sequences in the vault's sense: "totally bounded with a modulus" is the proposal; it should be set against the rival notions in [[Extreme Value Theorem]], hard problem 2.
4. **Several variables and sequences of functions.** Arzelà–Ascoli and the like.
