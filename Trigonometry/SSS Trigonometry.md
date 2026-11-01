---
title: SSS Trigonometry
type: method
status: canonical
provenance: murphy (formulas and method); murphy+ai (derivations, exact slopes, example)
sources: "[[SRC Constructible Trigonometry Textbook (md)]]"
updated: 2026-10-07
---

# SSS Trigonometry

**Given** the three sides $a,b,c$ of a triangle ([[SSS Congruence]]). The triangle exists exactly when each side is shorter than the other two together. **Find** the three wedges, the area, the inradius and the circumradius. Let $s=\tfrac12(a+b+c)$.

## The missing wedges

The [[Law of Lengths]], solved for $\ell$, gives each wedge's characteristic length:

$$\ell_C=\frac{2ab}{a^2+b^2-c^2},\qquad \ell_A=\frac{2bc}{b^2+c^2-a^2},\qquad \ell_B=\frac{2ac}{a^2+c^2-b^2}.$$

Each is a rational function of the sides, and its sign says whether the wedge is acute or obtuse ([[Characteristic Length]]). A zero denominator is a right angle, $\ell=\infty$.

The slopes follow once the area is known (below):

$$m_C=\frac{4Q}{a^2+b^2-c^2},\qquad m_A=\frac{4Q}{b^2+c^2-a^2},\qquad m_B=\frac{4Q}{a^2+c^2-b^2}.$$

**[AI]** Derivation: the [[Law of SAS Area]], $Q=\tfrac12ab\,m_C/\ell_C$, gives $m_C=\ell_C\cdot\dfrac{2Q}{ab}$, and substituting $\ell_C$ gives the form above. It has the right sign for free, and a right angle gives $4Q/0=\infty$. (The other route, $m_C=\pm\sqrt{\ell_C^2-1}$ with the sign of $\ell_C$, needs a second root.)

## The missing area

[[Heron's Formula]]:

$$Q=\sqrt{s(s-a)(s-b)(s-c)}.$$

## The inradius

$$r=\sqrt{\frac{(s-a)(s-b)(s-c)}{s}}.$$

Derivation: join the incenter to the three vertices. The triangle splits into three, with bases $a,b,c$ and common height $r$, so $Q=\tfrac12r(a+b+c)=rs$, and $r=Q/s$. Substitute Heron.

## The circumradius

$$R=\frac{abc}{4\sqrt{s(s-a)(s-b)(s-c)}}=\frac{abc}{4Q}.$$

Derivation: the [[Law of the Circumdiameter]] gives $c\,\ell_C/m_C=2R$, and $m_C/\ell_C=2Q/(ab)$ from the [[Law of SAS Area]], so $2R=\dfrac{abc}{2Q}$.

## Exactness

$\ell_A,\ell_B,\ell_C$ are rational in the sides. The one square root is in $Q$; after it, $m_A,m_B,m_C,r,R$ are all field operations. If the sides are in $\mathbb K$ everything is in $\mathbb K$, with no approximation.

## Example: sides $13,14,15$

$s=21$, $Q=84$.

| | wedge $A$ ($a=13$) | wedge $B$ ($b=14$) | wedge $C$ ($c=15$) |
|---|---|---|---|
| $\ell$ | $\dfrac{2\cdot14\cdot15}{196+225-169}=\dfrac53$ | $\dfrac{2\cdot13\cdot15}{169+225-196}=\dfrac{65}{33}$ | $\dfrac{2\cdot13\cdot14}{169+196-225}=\dfrac{13}5$ |
| $m$ | $\dfrac{336}{252}=\dfrac43$ | $\dfrac{336}{198}=\dfrac{56}{33}$ | $\dfrac{336}{140}=\dfrac{12}5$ |

- $r=\sqrt{\dfrac{8\cdot7\cdot6}{21}}=\sqrt{16}=4$.
- $R=\dfrac{13\cdot14\cdot15}{4\cdot84}=\dfrac{2730}{336}=\dfrac{65}8$.
- **Check by the [[Law of Slopes]]:** $m_A+m_B+m_C=\dfrac43+\dfrac{56}{33}+\dfrac{12}5=\dfrac{896}{165}=m_Am_Bm_C$ ✔.
