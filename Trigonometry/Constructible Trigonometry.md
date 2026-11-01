---
title: Constructible Trigonometry
type: theory
status: canonical (summary of an active book/article project)
provenance: murphy (original mathematics); formulas spot-checked by AI
sources: "[[SRC Constructible Trigonometry Textbook (md)]]"
updated: 2026-10-07
---

# Constructible Trigonometry

**The original mathematics in this corpus.** Trigonometry rebuilt on *slope* instead of *angle measure*, entirely inside the constructible field 𝕂⁺ = 𝕂 ∪ {∞} ([[Extended Constructible Numbers]], [[Slope]]) — "exact solutions where traditional methods require approximation," no transcendental functions and no calculator until students choose to cross the bridge.

## Primitives

- **[[Slope]]** $m$ — rise over run, $\frac{y_2-y_1}{x_2-x_1}$; the first primitive. The slope of the wedge at vertex $A$ is $m_A$ (other frameworks: $\tan\theta$). "Angle" means only that concrete wedge; there is no angle measure.
- **[[Characteristic Length]]** $\ell=\pm\sqrt{1+m^2}$, positive for rightward directions and negative for leftward (in other frameworks $=\sec\theta$): the hypotenuse of the *defining right triangle* with base 1, height $m$. Together $m$ and $\ell$ cover all four quadrants.
- So $\sin=m/\ell$, $\cos=1/\ell$ — but never needed as names until "the Great Reveal" (Euler, ch. 14 of the outline).

**Addition law** ([[Sum of Slopes]], the group law ⊕): $m_{A+B}=\dfrac{m_A+m_B}{1-m_Am_B}$. The rational parametrization of the circle, the same group law reappears in [[Discrete Calculus]] ("From the Line to the Circle").

## Notation for triangles

In triangle $ABC$ the sides $a,b,c$ lie opposite the wedges $A,B,C$. Then:

- $m_A,\ell_A$ — slope and characteristic length of the wedge at $A$; $m_{A/2},\ell_{A/2}$ for its half ([[Characteristic Length#Half a wedge]]); $m_{A+B}$ for two wedges together ([[Sum of Slopes]]).
- $s=\dfrac{a+b+c}{2}$ — the semi-perimeter.
- $Q$ — the area; $r$ — the inradius; $R$ — the circumradius.
- A right angle has slope $\infty$ ([[Extended Constructible Numbers]]).

## Laws

- [[Law of Slopes]] — the slopes of a triangle's three wedges satisfy one relation, because the wedges make a straight wedge.
- [[Law of Lengths]] — the third side from two sides and the wedge between them; solved for $\ell$, a wedge from the three sides.
- [[Law of SAS Area]] — the area from two sides and the wedge between them.
- [[Law of the Circumdiameter]] — each side times $\ell/m$ of its opposite wedge is the circumdiameter.
- [[Triangle Identities]] — sum and product identities for the wedges and the half-wedges, with $r$ and $R$.
- [[Heron's Formula]] — the area from the three sides.

## Solving triangles

### The naming convention

A case is named by **what is given**, in three letters:

| letter | given |
|---|---|
| **S** | a side |
| **A** | a wedge (an angle) |
| **Q** | the area |
| **I** | the inradius |
| **C** | the circumradius |

- **Without loss of generality** (WLOG) the vertices are relabeled so that the given data are as in the right-hand column below. A lowercase letter is a side and the capital of the same letter is the wedge opposite it ($a$ is opposite $A$).
- **The first letter is the scale** in the area, inradius and circumradius cases: **Q**, **I** or **C** comes first, it fixes the size, and the other two letters fix the shape. The one exception is **SQA**, written with the side first so that the wedge $A$ reads as opposite $a$.
- **Order tells position.** In SSA and SQA a wedge written *after* a side is the wedge **opposite** that side. A wedge written *before* a side (QAS, IAS, CAS) has that side **next to** it. In SAS the wedge is **between** the two sides, and in ASA the side is between the two wedges.

### The cases

| case | given (WLOG) | triangles |
|---|---|---|
| [[SSS Trigonometry]] ([[SSS Congruence]]) | $a,b,c$ | one (or none) |
| [[SAS Trigonometry]] ([[SAS Congruence]]) | $a,C,b$ | one |
| [[AAS Trigonometry]] ([[AAS Congruence]]) | $A,C,a$ | one |
| [[ASA Trigonometry]] ([[ASA Congruence]]) | $A,b,C$ | one |
| [[SSA Trigonometry]] | $a,b,A$ | **ambiguous**: 0, 1 or 2 |
| [[QSS Trigonometry]] | $Q,a,b$ | **ambiguous**: 0, 1 or 2 |
| [[QAA Trigonometry]] | $Q,A,B$ | one |
| [[QAS Trigonometry]] | $Q,A,b$ | one |
| [[SQA Trigonometry]] | $a,Q,A$ | one (or none; maximum area) |
| [[ISS Trigonometry]] | $r,a,b$ | **ambiguous**: 0, 1 or 2; the unknown is a root of a **cubic** |
| [[IAA Trigonometry]] | $r,A,B$ | one |
| [[IAS Trigonometry]] | $r,A,b$ | one (or none) |
| [[QCS Trigonometry]] | $Q,R,a$ | **ambiguous**: 0, 1 or 2 |
| [[CSS Trigonometry]] | $R,a,b$ | **ambiguous**: up to 2 |
| [[CAA Trigonometry]] | $R,A,B$ | one |
| [[CAS Trigonometry]] | $R,A,b$ | **ambiguous**: up to 2 ([[SSA Trigonometry]] in disguise) |

The six **ambiguous** cases are SSA, QSS, ISS, CSS, CAS and QCS. In SSA, QSS, CSS, CAS and QCS the data fix a wedge only through the ratio $m/\ell$ (its sine), so the wedge and its supplement both fit. In ISS the unknown is a root of a cubic with two admissible roots. Every other case fixes the shape.

Each case gives the missing wedges, sides, area, inradius and circumradius (the ambiguous ones give them for each possible triangle).

## Exact values and tools

- [[Nested Radicals]] — repeated halving of a wedge, the golden pair, and the quartet $\Xi,\xi,\Upsilon,\upsilon$.
- [[Exact Slopes]] — the exact slope of every wedge that is a multiple of $\tfrac1{120}$ of a turn.
- [[Slope Approximations]] — a short rational slope for every wedge from $1^\circ$ to $45^\circ$, with its error.
- [[Slope Protractor]] — a square device that reads a slope directly, in sixtieths.

## Novel results (the journal article)

- **ISS (Inradius–Side–Side) is a new ambiguous case** that reduces to **cubic** equations — "the truly surprising result." Given $a,b,r$: 0, 1, or 2 triangles; $r_{\max}$ is itself a cubic (exact for $a=b$, approximated otherwise). The 13-14-15 triangle ($r=4$) gives the worked example. Also: QSS, CAS, SPA, CPA — all determined.
- **Why it matters:** cubics are the natural, *historically* motivated bridge from 𝕂 to 𝔸 (Tartaglia–Cardano–Bombelli); casus irreducibilis motivates complex numbers; Marden's Theorem shows up (Prodanov).
- **Pedagogy claim:** an intermediate course between Algebra II and standard trig; "delayed introduction of transcendental numbers"; aligns with slope, SSS, bisectors students already know; AI/CAS adapt well since "no floating point arithmetic is needed."
- **Admitted open items:** $r_{\max}$ inexact; the wedges of the 17-gon and other constructible polygons beyond the 15-gon untouched ([[Nested Radicals]]); sin/cos transition unexplored; vectors/linear algebra; spherical and hyperbolic ("seem amenable to constructibility, but perhaps not").

## The book: *A Discrete Bridge: From Constructible to Transcendental Trigonometry*

Six parts, 17 chapters + 6 appendices, structured as a **historical walk**: Exact Apparatus (𝕂, ℙ¹(𝕂), radicals, quadratics, the slope-length objects) → Babylonian threads (spherical: 360°, DMS; planar: seqt, Plimpton 322, YBC 7289) → Greek demonstration (Euclid without numbered angles; Menelaus, Ptolemy; "geometry proves, astronomy computes") → Indian algorithms (jyā; Bhāskara; **Madhava**: the series; π ∉ 𝕂; "the bridge, presented historically, not endorsed ontologically") → European analytic turn (Descartes, Viète, **Euler's Great Reveal**: "m was tangent all along, ℓ was secant all along") → Modern divergence (three geometries, Cauchy–Weierstrass, floating point vs. constructible). Full outline: [[SRC Constructible Trigonometry Textbook (md)]].
