---
title: CSS Trigonometry
type: method
status: canonical
provenance: murphy (formulas for $c$, the area and the inradius); murphy+ai (signs and the second triangle, wedges, examples)
sources: "[[SRC Constructible Trigonometry Textbook (md)]]"
updated: 2026-10-08
---

# CSS Trigonometry

**CSS** is *circumradius, side, side*. **Given** the circumradius $R$ and two sides $a,b$. WLOG the wedge $C$ lies between them. **Find** $c$, the wedges, the area and the inradius.

This is an **ambiguous case** like [[SSA Trigonometry]] and [[QSS Trigonometry]]: up to **two triangles**.

## The key relation

By the [[Law of the Circumdiameter]], $2R=\dfrac{a\,\ell_A}{m_A}=\dfrac{b\,\ell_B}{m_B}$, so each wedge is known up to acute versus obtuse:

$$\frac{m_A}{\ell_A}=\frac a{2R},\qquad \frac{m_B}{\ell_B}=\frac b{2R}.$$

Write $\alpha=\pm\sqrt{4R^2-a^2}$ and $\beta=\pm\sqrt{4R^2-b^2}$, with $\alpha>0$ when $A$ is acute and $\alpha<0$ when $A$ is obtuse (likewise $\beta$). Then

$$m_A=\frac a\alpha,\quad \ell_A=\frac{2R}\alpha,\qquad m_B=\frac b\beta,\quad \ell_B=\frac{2R}\beta.$$

## Existence and the two triangles

$R\ge\tfrac12\max(a,b)$, otherwise no triangle has a chord that long.

Of the four sign combinations, two are triangles:

- $(\alpha,\beta)$ both positive: $A$ and $B$ both acute. **Triangle 1.**
- The wedge **opposite the longer side** obtuse, the other acute: $\alpha<0$ if $a>b$, $\beta<0$ if $b>a$. **Triangle 2.**
- Both obtuse is impossible, and the shorter side's wedge obtuse is excluded (a larger wedge lies opposite a larger side).

If $a=b$ there is only triangle 1. If $R=\tfrac12\max(a,b)$, that side is a diameter, its opposite wedge is a right angle, and triangle 2 disappears.

## The missing side

$c=2R\sin C=2R\sin(A+B)=a\cos B+b\cos A$:

$$c_1=a\sqrt{1-\frac{b^2}{4R^2}}+b\sqrt{1-\frac{a^2}{4R^2}},\qquad c_2=\left|a\sqrt{1-\frac{b^2}{4R^2}}-b\sqrt{1-\frac{a^2}{4R^2}}\right|.$$

In terms of $\alpha,\beta$: $c=\dfrac{a\beta+b\alpha}{2R}$ for either triangle. $c_2>0$ exactly when $a\ne b$, because $a^2-\dfrac{a^2b^2}{4R^2}>b^2-\dfrac{a^2b^2}{4R^2}\iff a>b$.

## The wedges

$$m_A=\pm\frac a{\sqrt{4R^2-a^2}},\qquad m_B=\pm\frac b{\sqrt{4R^2-b^2}},\qquad m_C=\frac{m_A+m_B}{m_Am_B-1},$$

with the signs of the triangle above. The third wedge is by the [[Law of Slopes]]. A right angle at $C$ appears when $m_Am_B=1$ and then $m_C=\infty$ ([[Extended Constructible Numbers]]).

## The area

$Q=\dfrac{abc}{4R}$ (the [[Law of the Circumdiameter]] with the [[Law of SAS Area]]):

$$Q=\frac{ab}{8R^2}\left(a\sqrt{4R^2-b^2}\pm b\sqrt{4R^2-a^2}\right),$$

with $+$ for triangle 1 and $-$ (absolute value) for triangle 2.

## The inradius

$r=Q/s$:

$$r=\frac{abc}{2R\,(a+b+c)}.$$

Without $c$: $r=\dfrac{\alpha+\beta}2-R+\dfrac{ab-\alpha\beta}{4R}$.

## Exactness

$c$, the wedges, $Q$, $r$ each take at most two square roots of quantities built from $R,a,b$ by field operations. If the data are in $\mathbb K$, everything is in $\mathbb K$: no cubic.

## Example: $R=\tfrac{65}8$, $a=13$, $b=14$

$4R^2=\dfrac{4225}{16}$, $\ \sqrt{4R^2-b^2}=\dfrac{33}4$, $\ \sqrt{4R^2-a^2}=\dfrac{39}4$.

| | triangle 1 (both acute) | triangle 2 ($B$ obtuse, since $b>a$) |
|---|---|---|
| $c$ | $\dfrac{13\cdot\frac{33}4+14\cdot\frac{39}4}{65/4}=15$ | $\dfrac{14\cdot\frac{39}4-13\cdot\frac{33}4}{65/4}=\dfrac95$ |
| $m_A$ | $\dfrac43$ | $\dfrac43$ |
| $m_B$ | $\dfrac{56}{33}$ | $-\dfrac{56}{33}$ |
| $m_C$ | $\dfrac{12}5$ | $\dfrac{36}{323}$ |
| $Q$ | $84$ | $\dfrac{252}{25}$ |
| $r$ | $\dfrac{2730}{2\cdot\frac{65}8\cdot42}=4$ | $\dfrac7{10}$ |

Triangle 1 is the $13,14,15$ triangle ([[SSS Trigonometry]]).

## Example: a right triangle and the isosceles triangle

$R=1$, $a=\sqrt3$, $b=1$. Here $a>b$, so triangle 2 has $A$ obtuse. $\sqrt{4R^2-a^2}=1$, $\sqrt{4R^2-b^2}=\sqrt3$.

| | triangle 1 | triangle 2 |
|---|---|---|
| $c$ | $\dfrac{\sqrt3\cdot\sqrt3+1\cdot1}{2}=2$ | $\dfrac{3-1}2=1$ |
| $m_A$, $m_B$ | $\sqrt3$, $\tfrac1{\sqrt3}$ | $-\sqrt3$, $\tfrac1{\sqrt3}$ |
| $m_C$ | $\infty$ (right angle) | $\tfrac1{\sqrt3}$ |
| $Q$ | $\dfrac{\sqrt3}2$ | $\dfrac{\sqrt3}4$ |
| $r$ | $\dfrac{\sqrt3-1}2$ | $\dfrac{2\sqrt3-3}2$ |

Triangle 1 is the right triangle with legs $1$, $\sqrt3$ and hypotenuse $2=2R$; triangle 2 is the $1,1,\sqrt3$ triangle with the interior wedge of a regular hexagon at $A$.
