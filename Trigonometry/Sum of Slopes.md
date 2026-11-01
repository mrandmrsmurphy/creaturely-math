---
title: Sum of Slopes
type: law
status: canonical
provenance: murphy+ai (figure and formula Murphy's; proof text drafted by AI)
sources: "[[SRC Constructible Trigonometry Textbook (md)]]"
updated: 2026-10-07
---

# Sum of Slopes

The slope of two wedges laid side by side is

$$m_{A+B}=\frac{m_A+m_B}{1-m_Am_B}.$$

It is the addition law of [[Slope]]: identity $0$, inverse $-m$, and $1\oplus1=\infty$. The characteristic lengths add by $\ell_{A+B}=\dfrac{\ell_A\ell_B}{1-m_Am_B}$ ([[Characteristic Length]]). It is the basis of the [[Law of Slopes]].

## Doubling

Adding a wedge to itself gives

$$m_{2x}=\frac{2m_x}{1-m_x^2},\qquad \ell_{2x}=\frac{\ell_x^2}{1-m_x^2}=\frac{\ell_x^2}{2-\ell_x^2}.$$

Inverting this gives the half-wedge formulas of [[Characteristic Length#Half a wedge]], and repeating the inversion gives the nests of [[Nested Radicals]].

## Proof

![[AngleAdditionDiagramSlope.svg|380]]

Let $\alpha,\beta$ be wedges with slopes $m_\alpha,m_\beta$ ($m_\alpha m_\beta<1$, as drawn). The whole figure is a rectangle of width $1$.

1. **Blue triangle.** Base $1$, height $m_\alpha$, hypotenuse $\ell_\alpha$, wedge $\alpha$ at the lower left.
2. **Pink triangle.** Stand a right triangle on the hypotenuse $\ell_\alpha$, with wedge $\beta$ at the lower left. Its other leg has slope $m_\beta$ against $\ell_\alpha$, so it is $m_\beta\ell_\alpha$ long. The two wedges together make the wedge $\alpha+\beta$ at the origin.
3. **Where the leg lands.** The leg $m_\beta\ell_\alpha$ is perpendicular to $\ell_\alpha$, so it makes the wedge $\alpha$ with the vertical, at the point $(1,m_\alpha)$. Its vertical part is $m_\beta\ell_\alpha\cdot\frac1{\ell_\alpha}=m_\beta$ and its horizontal part is $m_\beta\ell_\alpha\cdot\frac{m_\alpha}{\ell_\alpha}=m_\alpha m_\beta$.
4. **Read off the rectangle.** The right side is $m_\alpha+m_\beta$ tall, and the top edge splits into $m_\alpha m_\beta$ and $1-m_\alpha m_\beta$. The pink hypotenuse runs from the origin to the top-left piece's end, at $\bigl(1-m_\alpha m_\beta,\;m_\alpha+m_\beta\bigr)$.
5. **Its slope is rise over run:**
$$m_{\alpha+\beta}=\frac{m_\alpha+m_\beta}{1-m_\alpha m_\beta}.$$

The drawing is the case $0<m_\alpha m_\beta<1$. For other signs and for $m_\alpha m_\beta\ge1$ the formula is the same algebraic identity, with signed $\ell$ ([[Characteristic Length]]) carrying the orientation.
