---
title: CAS Trigonometry
type: method
status: canonical
provenance: murphy (formulas for $a$ and $m_B$); murphy+ai (reduction to SSA, $c$, count, area, inradius, examples)
sources: "[[SRC Constructible Trigonometry Textbook (md)]]"
updated: 2026-10-08
---

# CAS Trigonometry

**CAS** is *circumradius, angle, side*. **Given** the circumradius $R$, a wedge $A$, and a side $b=AC$ next to it (written $RAb$). So $R$, $b$, $m_A,\ell_A$ are known ([[Slope]], [[Characteristic Length]]). **Find** the other two sides, the other two wedges, the area and the inradius.

This is an **ambiguous case**: up to two triangles. It is [[SSA Trigonometry]] in disguise. The side opposite $A$ is already determined by $R$ and $A$, so the data are $(a,b,A)$ and $R$ carries no further condition.

## The side opposite $A$

The [[Law of the Circumdiameter]], $2R=a\ell_A/m_A$:

$$a=2R\,\frac{m_A}{\ell_A}.$$

## The wedge $B$

From $\dfrac{m_B}{\ell_B}=\dfrac b{2R}$, with $\beta=\pm\sqrt{4R^2-b^2}$ ($\beta>0$ when $B$ is acute, $\beta<0$ when $B$ is obtuse):

$$m_B=\frac{b}{\beta}=\pm\frac b{\sqrt{4R^2-b^2}},\qquad \ell_B=\frac{2R}{\beta}.$$

Existence needs $b\le2R$ (a chord is at most a diameter). If $b=2R$, $B$ is a right angle: $m_B=\infty$ ([[Extended Constructible Numbers]]).

## The missing side $c$

The CAA relation $c=2R\,\dfrac{m_A+m_B}{\ell_A\ell_B}$ ([[CAA Trigonometry]]) simplifies, with $m_B=b/\beta$ and $\ell_B=2R/\beta$, to

$$c=\frac{b+m_A\,\beta}{\ell_A}=\frac{b\pm D}{\ell_A},\qquad D=|m_A|\sqrt{4R^2-b^2}.$$

This is the SSA formula: $D^2=a^2\ell_A^2-b^2m_A^2$ since $a^2\ell_A^2=4R^2m_A^2$.

## How many triangles

The lower sign needs $c>0$, which is $b>D$, equivalent to $b>a$. So:

- **$A$ obtuse:** $B$ must be acute: **one triangle** ($\beta>0$). The other sign gives $c<0$.
- **$A$ acute and $b>a$:** **two triangles** ($B$ acute or $B$ obtuse).
- **$A$ acute and $b\le a$:** **one triangle**.
- **$b>2R$:** none.

## The third wedge

By the [[Law of Slopes]]:

$$m_C=\frac{m_A+m_B}{m_Am_B-1}.$$

## The area

$Q=\dfrac{abc}{4R}$ (the [[Law of the Circumdiameter]] with the [[Law of SAS Area]]), which in the data is

$$Q=\frac{b\,m_A\,(b+m_A\beta)}{2\,\ell_A^2}=\frac{b\,m_A\,(b\pm D)}{2\,\ell_A^2},$$

the same as the SSA area.

## The inradius

$r=Q/s$:

$$r=\frac{abc}{2R\,(a+b+c)}.$$

Equivalently, from the CAA form, $r=R\,\dfrac{m_Am_B-(\ell_A-1)(\ell_B-1)}{\ell_A\ell_B}$.

## Exactness

Every result is a field operation on $R,b,m_A,\ell_A$ and the one root $\sqrt{4R^2-b^2}$: if the data are in $\mathbb K$, so is everything. No cubic.

## Example: $R=\tfrac{65}8$, $m_A=\tfrac43$, $b=14$ (two triangles)

$\ell_A=\tfrac53$, $a=\dfrac{65}4\cdot\dfrac{4/3}{5/3}=13$, $\ \sqrt{4R^2-b^2}=\dfrac{33}4$, $\ D=\dfrac43\cdot\dfrac{33}4=11$. Here $b=14>a=13$.

| | triangle 1 ($\beta=+\tfrac{33}4$) | triangle 2 ($\beta=-\tfrac{33}4$) |
|---|---|---|
| $c$ | $\dfrac{14+11}{5/3}=15$ | $\dfrac{14-11}{5/3}=\dfrac95$ |
| $m_B$ | $\dfrac{56}{33}$ | $-\dfrac{56}{33}$ |
| $m_C$ | $\dfrac{12}5$ | $\dfrac{36}{323}$ |
| $Q$ | $\dfrac{14\cdot\frac43\cdot25}{2\cdot\frac{25}9}=84$ | $\dfrac{14\cdot\frac43\cdot3}{2\cdot\frac{25}9}=\dfrac{252}{25}$ |
| $r$ | $4$ | $\dfrac7{10}$ |

These are the same two triangles as in [[CSS Trigonometry]] and [[SSA Trigonometry]].

## Example: one triangle

$R=1$, $b=1$, so $\sqrt{4R^2-b^2}=\sqrt3$.

- **$A$ acute, $m_A=\sqrt3$** ($\ell_A=2$): $a=\sqrt3>b$. Only $\beta=+\sqrt3$ works: $c=\dfrac{1+3}{2}=2$ and $m_B=\dfrac1{\sqrt3}$, $m_C=\infty$. The right triangle with legs $1,\sqrt3$ and hypotenuse $2=2R$. The sign $\beta=-\sqrt3$ gives $c=\dfrac{1-3}2<0$.
- **$A$ obtuse, $m_A=-\sqrt3$** ($\ell_A=-2$, the interior wedge of a regular hexagon): $a=\sqrt3$, $\beta=+\sqrt3$, $c=\dfrac{1-3}{-2}=1$, $m_B=m_C=\dfrac1{\sqrt3}$, $Q=\dfrac{\sqrt3}4$, $r=\dfrac{2\sqrt3-3}2$. The $1,1,\sqrt3$ triangle.
