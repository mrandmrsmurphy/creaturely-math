---
title: CAA Trigonometry
type: method
status: canonical
provenance: murphy (formulas for the sides, the area and the inradius); murphy+ai (derivations, comparison with IAA and QAA, examples)
sources: "Murphy's Constructible Trigonometry textbook (2026)"
updated: 2026-10-08
---

# CAA Trigonometry

**CAA** is *circumradius, angle, angle*. **Given** the circumradius $R$ and two wedges, WLOG $A$ and $B$ (written $RAB$), so $R$, $m_A,\ell_A$ and $m_B,\ell_B$ are known ([[Slope]], [[Characteristic Length]]). **Find** the three sides, the third wedge, the area and the inradius.

This case is **not ambiguous**: the wedges fix the shape, and $R$ fixes the scale. It is the same relationship as [[QAA Trigonometry]] and [[IAA Trigonometry]], with the scale given by the circumradius instead of the area or the inradius.

## The missing sides

The [[Law of the Circumdiameter]], $2R=a\,\dfrac{\ell_A}{m_A}=b\,\dfrac{\ell_B}{m_B}$, gives

$$a=2R\,\frac{m_A}{\ell_A},\qquad b=2R\,\frac{m_B}{\ell_B}.$$

For $c$, $c=2R\,\sin C=2R\,\sin(A+B)=2R\,(\sin A\cos B+\cos A\sin B)$, and with $\sin=m/\ell$, $\cos=1/\ell$:

$$c=2R\,\frac{m_A+m_B}{\ell_A\,\ell_B}.$$

(Here $\sin,\cos$ only name the ratios $m/\ell$ and $1/\ell$ for readers of other frameworks.)

**No absolute values.** For an obtuse $A$, $m_A$ and $\ell_A$ are both negative, so $a$ stays positive. Likewise $m_A+m_B$ and $\ell_A\ell_B$ change sign together, so $c$ stays positive.

## The missing wedge

By the [[Law of Slopes]]:

$$m_C=\frac{m_A+m_B}{m_Am_B-1}.$$

## The area

$Q=\dfrac{abc}{4R}$ ([[Law of SAS Area]] with the [[Law of the Circumdiameter]]):

$$Q=2R^2\,\frac{m_A\,m_B\,(m_A+m_B)}{\ell_A^2\,\ell_B^2}.$$

## The inradius

$r=R\,(\cos A+\cos B+\cos C-1)$, with $\cos C=\dfrac{m_Am_B-1}{\ell_A\ell_B}$:

$$r=R\,\frac{m_Am_B-(\ell_A-1)(\ell_B-1)}{\ell_A\,\ell_B}.$$

This is the formula of [[IAA Trigonometry]], $R=r\,\dfrac{\ell_A\ell_B}{m_Am_B-(\ell_A-1)(\ell_B-1)}$, solved for $r$. In a triangle with wedges $A,B$ the ratio $R/r$ depends only on the shape.

## Right angles

If $A$ or $B$ is a right angle its slope is $\infty$ and the formulas do not apply ([[Extended Constructible Numbers]]): read the triangle off directly. A right angle at $C$ is fine: $m_Am_B=1$ gives $m_C=\infty$.

## Exactness

Every result is a field operation on $R,m_A,\ell_A,m_B,\ell_B$, so if the data are in $\mathbb K$ so is everything: no new square root and no cubic.

## Example: $R=\tfrac{65}8$, $m_A=\tfrac43$, $m_B=\tfrac{56}{33}$

$\ell_A=\tfrac53$, $\ell_B=\tfrac{65}{33}$, $m_A+m_B=\tfrac{100}{33}$, $m_Am_B=\tfrac{224}{99}$.

- $a=\dfrac{65}4\cdot\dfrac{4/3}{5/3}=13$, $\ b=\dfrac{65}4\cdot\dfrac{56/33}{65/33}=14$.
- $c=\dfrac{65}4\cdot\dfrac{100/33}{325/99}=15$.
- $m_C=\dfrac{100/33}{224/99-1}=\dfrac{12}5$.
- $Q=2\cdot\dfrac{4225}{64}\cdot\dfrac{\frac{224}{99}\cdot\frac{100}{33}}{\frac{25}9\cdot\frac{4225}{1089}}=84$.
- $r=\dfrac{65}8\cdot\dfrac{160/99}{325/99}=4$.

The $13,14,15$ triangle ([[SSS Trigonometry]]).

## Example: an obtuse wedge

$R=1$, $m_A=-\sqrt3$, $\ell_A=-2$ (the interior wedge of a regular hexagon), $m_B=\dfrac1{\sqrt3}$, $\ell_B=\dfrac2{\sqrt3}$.

- $a=2\cdot\dfrac{-\sqrt3}{-2}=\sqrt3$, $\ b=2\cdot\dfrac{1/\sqrt3}{2/\sqrt3}=1$.
- $c=2\cdot\dfrac{-2/\sqrt3}{-4/\sqrt3}=1$.
- $m_C=\dfrac{-2/\sqrt3}{-2}=\dfrac1{\sqrt3}$.
- $Q=2\cdot\dfrac{(-\sqrt3)(\frac1{\sqrt3})(-\frac2{\sqrt3})}{4\cdot\frac43}=\dfrac{\sqrt3}4$.
- $r=\dfrac{-1+3\left(\frac2{\sqrt3}-1\right)}{(-2)\cdot\frac2{\sqrt3}}=\dfrac{2\sqrt3-3}2$.

This is the $1,1,\sqrt3$ triangle.
