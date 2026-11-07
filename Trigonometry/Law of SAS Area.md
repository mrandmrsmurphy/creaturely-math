---
title: Law of SAS Area
type: law
status: canonical
provenance: murphy+ai (statement and method Murphy's; proof text drafted by AI)
sources: "Murphy's Constructible Trigonometry textbook (2026)"
updated: 2026-10-07
---

# Law of SAS Area

In triangle $ABC$ with sides $a,b$ and the wedge $C$ between them (side–wedge–side), the area $Q$ is

$$Q=\frac12\,ab\,\frac{m_C}{\ell_C}.$$

## Derivation

**Step 1 — drop an altitude.** Take $b=CA$ as the base and drop the altitude $h$ from $B$ to the line $CA$.

In the right triangle at $C$, the hypotenuse is $a$ and the wedge is $C$. By [[Slope]] and [[Characteristic Length]], hypotenuse : run : rise $=\ell_C:1:m_C$, so

$$h=a\,\frac{m_C}{\ell_C}.$$

**Step 2 — substitute into $\tfrac12bh$.**

$$Q=\frac12\,b\,h=\frac12\,b\cdot a\,\frac{m_C}{\ell_C}=\frac12\,ab\,\frac{m_C}{\ell_C}.$$

**Step 3 — the altitude is unnecessary.** The answer contains only the two sides and the wedge between them; $h$ and the foot of the altitude have disappeared. So the law needs no construction: given $a$, $b$ and $m_C$, $\ell_C$, the area follows.

By symmetry, $Q=\tfrac12\,bc\,\dfrac{m_A}{\ell_A}=\tfrac12\,ca\,\dfrac{m_B}{\ell_B}$.

## Remarks

- **Obtuse wedges.** If $C$ is wider than a right angle then $m_C<0$ and $\ell_C<0$, so $m_C/\ell_C>0$ and the area is positive. The altitude's foot lies on the extension of $CA$, and the height $h=a\,m_C/\ell_C$ is still correct. This is why $\ell$ must be signed.
- **Right angle.** $m_C/\ell_C=\infty\div\infty=1$ in $\mathbb K^+$ ([[Extended Constructible Numbers]]), so $Q=\tfrac12ab$, the familiar half of a rectangle.
- **Exactness.** If $a,b,m_C,\ell_C$ are in $\mathbb K$, so is $Q$: there is no approximation.
- **Checks.** Sides $13,14,15$ with $C$ opposite $15$: $m_C/\ell_C=\dfrac{12/5}{13/5}=\dfrac{12}{13}$, so $Q=\tfrac12\cdot13\cdot14\cdot\tfrac{12}{13}=84$ ✔. Sides $1,1$ with $C$ the interior wedge of a regular hexagon: $m_C/\ell_C=\dfrac{-\sqrt3}{-2}$, so $Q=\dfrac{\sqrt3}4$ ✔. Sides $3,4$ with a right angle: $Q=6$ ✔.
- With the [[Law of the Circumdiameter]], $c\,\ell_C/m_C=2R$ gives $m_C/\ell_C=c/(2R)$, so $Q=\dfrac{abc}{4R}$.
