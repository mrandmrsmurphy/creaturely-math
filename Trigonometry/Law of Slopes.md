---
title: Law of Slopes
type: law
status: canonical
provenance: murphy (derivation); remarks on right angles and $\ell$ drafted by AI
sources: "[[SRC Constructible Trigonometry Textbook (md)]]"
updated: 2026-10-07
---

# Law of Slopes

From geometry, we know that the interior angles of any triangle add up to half a rotation. In terms of slope, this means that the slopes of the wedges of a triangle add, by the [[Sum of Slopes]], to a straight wedge, whose slope is zero:

$$m_{A+B+C}=0.$$

## Derivation

Recall the [[Sum of Slopes]] formula, $m_{A+B}=\dfrac{m_A+m_B}{1-m_Am_B}$. Adding $m_C$ gives a complex fraction:

$$m_{(A+B)+C}=\cfrac{\dfrac{m_A+m_B}{1-m_Am_B}+m_C}{1-\dfrac{m_A+m_B}{1-m_Am_B}\cdot m_C}.$$

Multiply top and bottom by $1-m_Am_B$:

$$m_{A+B+C}=\frac{m_A+m_B+m_C-m_Am_Bm_C}{1-m_Am_B-m_Am_C-m_Bm_C}.$$

Set this equal to $0$ and discard the denominator. This resolves to

$$\boxed{m_A+m_B+m_C=m_Am_Bm_C}$$

Solving for $m_C$:

$$m_C=\frac{m_A+m_B}{m_Am_B-1}\;(=-m_{A+B}).$$

## Remarks

- The sum of the three slopes is **not** zero; the slope *of the sum* of the three wedges is. Equilateral: $3\sqrt3=(\sqrt3)^3$.
- A right angle has slope $\infty$ (see [[Slope#Slopes live on 𝕂 ∪ {∞}]]). If a wedge is a right angle, the other two are complementary, $m_Am_B=1$, and the formula for $m_C$ correctly gives $\frac{m_A+m_B}{0}=\infty$. The boxed identity itself is for finite slopes.
- **[AI]** The straight wedge is $m=0$ with $\ell=-1$ (leftward): with the denominator above written $D$, $\ell_{A+B+C}=\dfrac{\ell_A\ell_B\ell_C}{D}=-1$, so $D=-\ell_A\ell_B\ell_C$. Checked: equilateral, $D=-8=-2^3$; the triangle with slopes $-\sqrt3,\tfrac1{\sqrt3},\tfrac1{\sqrt3}$ (a regular-hexagon wedge and two equal wedges), $D=\tfrac83=-(-2)\cdot\tfrac2{\sqrt3}\cdot\tfrac2{\sqrt3}$.
