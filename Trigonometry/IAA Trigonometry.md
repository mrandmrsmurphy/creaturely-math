---
title: IAA Trigonometry
type: method
status: canonical
provenance: murphy (formulas for the sides and the area; method); murphy+ai (tangent-length derivation, third wedge, circumradius, examples)
sources: "[[SRC Constructible Trigonometry Textbook (md)]]"
updated: 2026-10-08
---

# IAA Trigonometry

**IAA** is *inradius, angle, angle*. **Given** the inradius $r$ and two wedges, WLOG $A$ and $B$ (written $rAB$), so $r$, $m_A,\ell_A$ and $m_B,\ell_B$ are known ([[Slope]], [[Characteristic Length]]). The side $c=AB$ lies between them. **Find** the three sides, the third wedge, the area and the circumradius.

This case is **not ambiguous**: the wedges fix the shape, and $r$ fixes the scale. It is the same relation as [[QAA Trigonometry]], with the area replaced by the inradius.

Write $t=m_{A/2}$ and $u=m_{B/2}$, the half-wedge slopes ([[Characteristic Length#Half a wedge]]): $t=\dfrac{m_A}{\ell_A+1}$, $u=\dfrac{m_B}{\ell_B+1}$.

## The tangent lengths

The incircle touches each side. From a vertex, the two tangent lengths are equal, and each is the rise $r$ of the incircle's center over the run of the half-wedge: from $A$ it is $r/t$, from $B$ it is $r/u$, and from $C$ it is $r/m_{C/2}$.

The three half-wedges $A/2$, $B/2$, $C/2$ together make a right angle, so $C/2$ is the complement of $A/2+B/2$:

$$m_{C/2}=\frac{1-tu}{t+u}.$$

## The missing sides

Each side is the sum of two tangent lengths:

$$c=\frac rt+\frac ru=r\,\frac{m_{A/2}+m_{B/2}}{m_{A/2}\,m_{B/2}},$$

$$a=\frac ru+\frac r{m_{C/2}}=\frac{r\,(1+u^2)}{u\,(1-tu)},\qquad b=\frac rt+\frac r{m_{C/2}}=\frac{r\,(1+t^2)}{t\,(1-tu)}.$$

In terms of the whole wedges:

$$a=2r\,\frac{m_A\,\ell_B}{m_Am_B-(\ell_A-1)(\ell_B-1)},\qquad b=2r\,\frac{\ell_A\,m_B}{m_Am_B-(\ell_A-1)(\ell_B-1)}.$$

These agree with each other and with the [[ASA Trigonometry]] sides $a=c\,\dfrac{m_A\ell_B}{m_A+m_B}$, $b=c\,\dfrac{m_B\ell_A}{m_A+m_B}$. The whole-wedge forms have one denominator, and it does not vanish when $m_A+m_B=0$.

## The third wedge

By the [[Law of Slopes]]:

$$m_C=\frac{m_A+m_B}{m_Am_B-1}.$$

## The area

$Q=r\,s$ with $s=\dfrac r t+\dfrac ru+\dfrac r{m_{C/2}}$, which gives

$$Q=\frac{r^2}{m_{A/2}\,m_{B/2}}\cdot\frac{m_{A/2}+m_{B/2}}{1-m_{A/2}\,m_{B/2}}.$$

## The circumradius

$$R=r\,\frac{\ell_A\,\ell_B}{m_Am_B-(\ell_A-1)(\ell_B-1)}.$$

It is the [[Law of the Circumdiameter]], $2R=a\,\ell_A/m_A$, with $a$ above. It has the same denominator as $a$ and $b$, and it is equivalent to the ASA form $R=\dfrac{c\,\ell_A\ell_B}{2(m_A+m_B)}$.

## Right angles

If $A$ or $B$ is a right angle its slope is $\infty$ and the formulas do not apply ([[Extended Constructible Numbers]]): read the triangle off directly. The wedges must together be narrower than a straight wedge, so $1-tu>0$.

## Exactness

Every result is a field operation on $r,m_A,\ell_A,m_B,\ell_B$ and the half-wedge slopes, which are themselves field operations on those. If the data are in $\mathbb K$, so is every result. No new square root appears: unlike [[ISS Trigonometry]], IAA stays in $\mathbb K$.

## Example: $r=4$, $m_A=\tfrac43$, $m_B=\tfrac{56}{33}$

$\ell_A=\tfrac53$, $\ell_B=\tfrac{65}{33}$, so $t=\tfrac12$ and $u=\tfrac47$, with $m_Am_B-(\ell_A-1)(\ell_B-1)=\dfrac{224}{99}-\dfrac{64}{99}=\dfrac{160}{99}$.

- $c=4\cdot\dfrac{15/14}{2/7}=15$.
- $a=\dfrac{8\cdot\frac43\cdot\frac{65}{33}}{160/99}=13$, $\ b=\dfrac{8\cdot\frac53\cdot\frac{56}{33}}{160/99}=14$.
- $m_C=\dfrac{100/33}{224/99-1}=\dfrac{12}5$.
- $Q=16\cdot\dfrac{1}{2/7}\cdot\dfrac{15/14}{5/7}=84$.
- $R=\dfrac{4\cdot\frac{325}{99}}{160/99}=\dfrac{65}8$.

The $13,14,15$ triangle ([[SSS Trigonometry]]).

## Example: an obtuse wedge

$r=\dfrac{2\sqrt3-3}2$, $m_A=-\sqrt3$, $\ell_A=-2$ (the interior wedge of a regular hexagon), $m_B=\dfrac1{\sqrt3}$, $\ell_B=\dfrac2{\sqrt3}$. Then $t=\sqrt3$, $u=2-\sqrt3$, $tu=2r$.

- $c=r\cdot\dfrac{t+u}{tu}=r\cdot\dfrac{2}{2r}=1$.
- The denominator is $m_Am_B-(\ell_A-1)(\ell_B-1)=-1+3\left(\dfrac2{\sqrt3}-1\right)=2\sqrt3-4$, so $a=\dfrac{2r(-\sqrt3)(2/\sqrt3)}{2\sqrt3-4}=\sqrt3$ and $b=\dfrac{2r(-2)(1/\sqrt3)}{2\sqrt3-4}=1$.
- $m_C=\dfrac{-2/\sqrt3}{-2}=\dfrac1{\sqrt3}$.
- $Q=r^2\cdot\dfrac{2}{2r(1-2r)}=\dfrac r{1-2r}=\dfrac{\sqrt3}4$.

This is the $1,1,\sqrt3$ triangle.
