---
title: Fourier Analysis
type: concept
status: "canonical (draft; Wildberger's results are third-party, restated and checked; the worked example was recomputed)"
provenance: "murphy (the claim: Fourier analysis should be rational; spread polynomials are important; the rational-avatar remark and the slope-language restatement, adopted 2026-11-04) + ai-synthesis (the page, the two-ends argument, the checks) + third-party (Limanta–Wildberger 2021; Goh–Wildberger 2009; restated carefully and checked, not claimed)"
sources: "[[Christians and the Reals]], [[Numbers, Lengths and Pixels]], [[Constructible Trigonometry]]"
updated: 2026-10-11
---

# Fourier Analysis

A periodic phenomenon — a musical note, a tide, an alternating voltage — can be decomposed into pure **harmonics**: a fundamental tone and its integer multiples. *Fourier analysis* is that decomposition and the machinery that recovers the strengths of the harmonics (the Fourier coefficients) by averaging the signal against each harmonic over a period.

The classical theory leans on the completed ℝ in exactly two places: the **harmonics** themselves ($\sin$, $\cos$, $\pi$ as level-11 objects of the [[Number Hierarchy]]) and the **integral over the circle** (a completed continuum average). This page records Murphy's claim — Fourier analysis *should be rational* — and the two facts that carry it.

## Why it should be rational (Murphy)

The objection "we need the reals to do Fourier analysis" ([[Christians and the Reals]], objection 2) fails at both ends:

- **Practice was always finite.** A measured signal is a finite list of samples — Pixels, each a value at a stated resolution ([[Numbers, Lengths and Pixels]]). The transform the world actually computes, the discrete Fourier transform (DFT/FFT), is a finite computation in roots of unity — algebraic numbers, level 8, exactly computable. No completed ℝ ever touches a signal processor.
- **Theory has a finite, rational avatar** (below): integration over the circle can be *characterized* and *computed* as a finite sum over a finite-field circle, and the answers are the same rational numbers the classical integrals give.
- What remains of the classical apparatus — $\sin$ and $\cos$ as level-11 functions, pointwise convergence theorems for arbitrary functions — belongs to the twilight: useful conventions to be held as Posits, not as the ground of the subject. The claim "Fourier analysis needs ℝ" has no certificate at the level where the work is done.

## Spread polynomials (third-party: Wildberger)

The rational avatar of the Fourier *basis*. Chebyshev's observation: $\cos n\theta$ is a polynomial in $\cos\theta$. Wildberger's parallel: $\sin^2 n\theta$ is a polynomial in the **spread** $s=\sin^2\theta$, with integer coefficients — the *spread polynomials* $S_n$:

$$S_0=0,\qquad S_1=s,\qquad S_{n+1}=2(1-2s)S_n-S_{n-1}+2s.$$

The first few: $S_2=4s(1-s)$, $S_3=s(3-4s)^2$ (both checked two ways: from the recurrence, and directly from $\sin^2 2\theta=4s(1-s)$ and $\sin^2 3\theta=s(3-4s)^2$). Every identity here is rational arithmetic in $s$ — no angle named, no $\pi$. A series in spread polynomials is the rational avatar of a Fourier series.

In the vault's slope language: the spread of a wedge of slope $m$ is $s=m^2/\ell^2=m^2/(1+m^2)$, so $S_n$ is a polynomial in $m^2/(1+m^2)$ — the comparison of Wildberger's quadrance/spread with the vault's slope/length is [[Future Directions]] item 9. References: Wildberger, *Divine Proportions* (2005); Goh & Wildberger, "Spread polynomials, rotations and the butterfly effect," [arXiv:0911.1025](https://arxiv.org/abs/0911.1025) (2009); the WildTrig lectures on the *Insights into Mathematics* channel.

## Fourier summation over finite fields (third-party: Limanta & Wildberger)

Kevin Limanta & N. J. Wildberger, "Super Catalan Numbers and Fourier Summation over Finite Fields," [arXiv:2108.10191](https://arxiv.org/abs/2108.10191) (2021; v3 2022; journal publication unchecked). Restated and checked.

**The finite circle.** Replace the continuum circle by the unit circle over a finite field $\mathbb F_q$ ($q$ a power of an odd prime): $S_{b,q}=\{[x,y]:x^2+y^2=1\}$, a finite set of $q-\bigl(\frac{-1}{q}\bigr)$ points.

**The functional.** On *polynumbers* (Wildberger's formal polynomials, from his Math Foundations lectures), average over the circle: $\psi_{b,q}(\pi)=\dfrac{1}{|S_{b,q}|}\displaystyle\sum_{[x,y]\in S_{b,q}}\pi(x,y)$.

**Theorem 1 (uniqueness).** $\psi_{b,q}$ is the *unique* linear functional satisfying **Normalization** ($\psi(\mathbf 1)=1$), **Locality** (a polynumber vanishing on the circle averages to $0$) and **Invariance** (rotational invariance). "Integration over the circle" is characterized with no continuum anywhere.

**Theorem 2 (Euclidean case).** The average of $x^{2m}y^{2n}$ over the finite circle is $\Omega(m,n)\bmod p$ (odd powers average to $0$), where

$$\Omega(m,n)=\frac{S(m,n)}{4^{m+n}}=\frac{(2m)!\,(2n)!}{4^{m+n}\,m!\,n!\,(m+n)!}$$

is rational — a *circular super Catalan number* — and the one rational $\Omega(m,n)$ determines the average for every prime power $q>2(m+n)+1$.

**The bridge.** The classical integral is the *same* rational: $\frac1{2\pi}\int_0^{2\pi}\cos^{2m}\theta\,\sin^{2n}\theta\,d\theta=\Omega(m,n)$. Checked at $(m,n)=(1,0)$: both sides $\tfrac12$; at $(1,1)$: both $\tfrac18$. The continuum integral was carrying rational content all along.

**Worked example (recomputed).** Over $\mathbb F_{13}$, since $-1$ is a square, the circle has $13-1=12$ points: $[1,0],[12,0],[0,1],[0,12],[2,6],[2,7],[11,6],[11,7],[6,2],[7,2],[6,11],[7,11]$ (check: $2^2+6^2=40\equiv1$). Average $x^2y^6$: each nonzero $y$ has $y^6\equiv-1$ (e.g. $2^6=64\equiv-1$), so $x^2y^6\equiv-x^2$; the values $x\in\{2,6,7,11\}$ each occur twice and $x^2\equiv4,10,10,4$, so $\sum x^2y^6\equiv-2(4+10+10+4)=-56\equiv9$. Multiplying by $1/12\equiv-1$ gives $\psi_{b,13}(x^2y^6)\equiv4$. And indeed $\Omega(1,3)=\dfrac{S(1,3)}{4^4}=\dfrac{10}{256}=\dfrac5{128}$; since $128\equiv11$ and $11^{-1}\equiv6$, we get $5\cdot6=30\equiv4$. Both sides agree, as Theorem 2 promises.

**Three geometries.** The same story runs in the two relativistic geometries (unit "circles" $x^2-y^2=1$ and $xy=1$), with a sign variant $(-1)^n\Omega(m,n)$ in the red geometry — the threefold symmetry of chromogeometry, and the Euclidean formula is in fact derived from the other two.

## What is not covered (the honest boundary)

- The paper treats polynomial — hence trigonometric-polynomial — data over circles. Arbitrary signals, and the convergence theory of Fourier series, are untouched; the classical pointwise-convergence theorems are Posit-level claims whose computations are rational.
- Differential equations and probability under the budget form remain open ([[Christians and the Reals]], gap 4).
- Journal publication unchecked; all formulas above were restated from the arXiv text, and the arithmetic was recomputed.
