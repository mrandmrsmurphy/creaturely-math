---
title: IAS Trigonometry
type: method
status: canonical
provenance: murphy (formulas for the area, $c$ and the half-wedges); murphy+ai (tangent-length derivation, $a$ and $R$ in half-wedge form, examples)
sources: "[[SRC Constructible Trigonometry Textbook (md)]]"
updated: 2026-10-08
---

# IAS Trigonometry

**IAS** is *inradius, angle, side*. **Given** the inradius $r$, a wedge $A$, and a side $b=AC$ next to it (written $rAb$). So $r$, $b$, $m_A,\ell_A$ are known ([[Slope]], [[Characteristic Length]]). **Find** the other two sides, the other two wedges, the area and the circumradius.

This case is **not ambiguous**: one triangle, or none.

The canonical quantities are the **half-wedges** ([[Characteristic Length#Half a wedge]]). Write

$$t=m_{A/2}=\frac{m_A}{\ell_A+1},\qquad L=\ell_{A/2}^2=1+t^2.$$

## The tangent lengths

The incircle touches each side, and the two tangents from a vertex are equal. From $A$ the tangent length is $x=r/m_{A/2}$, from $C$ it is $z=r/m_{C/2}$, from $B$ it is $y=r/m_{B/2}$. The side $b=AC=x+z$ is given, so

$$x=\frac rt,\qquad z=b-\frac rt=\frac{b\,t-r}{t}.$$

## The half-wedges

$$m_{C/2}=\frac{r\,m_{A/2}}{b\,m_{A/2}-r},\qquad m_{B/2}=\frac{b\,m_{A/2}-r\,\ell_{A/2}^2}{b\,m_{A/2}^2}.$$

The first is $r/z$. The second follows because the three half-wedges make a right angle: $m_{B/2}=\dfrac{1-t\,m_{C/2}}{t+m_{C/2}}$. Whole wedges, if wanted, are $m_X=\dfrac{2m_{X/2}}{1-m_{X/2}^2}$.

## Existence

The triangle exists when both half-wedges are positive:

$$b\,m_{A/2}>r\,\ell_{A/2}^2\quad(\text{which includes }b\,m_{A/2}>r).$$

For acute $A$ this is the same as $b\,m_A>2r\,\ell_A$, since $b\,m_A-2r\ell_A=\dfrac{2\bigl(bt-rL\bigr)}{1-t^2}$.

## The missing sides

The third tangent length is $y=\dfrac{r}{m_{B/2}}=\dfrac{r\,b\,t^2}{b\,t-r\,L}$. Then

$$a=y+z=\frac{(b\,t-r)^2+(r\,t)^2}{t\,(b\,t-r\,L)},\qquad c=x+y=\frac{r\,L\,(b\,t-r)}{t\,(b\,t-r\,L)}.$$

In terms of the whole wedge, $c$ is

$$c=\frac{2r\,\ell_A\,\bigl(b-b\,\ell_A+r\,m_A\bigr)}{(\ell_A-1)\,(2r\,\ell_A-b\,m_A)}.$$

## The area

$Q=r\,s$ with $s=b+y$:

$$Q=\frac{b\,r\,(b\,t-r)}{b\,t-r\,L}=b\,r\cdot\frac{b\,m_A-r(\ell_A+1)}{b\,m_A-2r\,\ell_A}.$$

The second form is in the whole wedge. Note that $b\,m_A-r(\ell_A+1)=m_A\,z$.

## The circumradius

The [[Law of the Circumdiameter]], $2R=a\ell_A/m_A$, with $\ell_A/m_A=\dfrac{1+t^2}{2t}$:

$$R=\frac{a\,L}{4\,t}=\frac{L\,\bigl[(b\,t-r)^2+(r\,t)^2\bigr]}{4\,t^2\,(b\,t-r\,L)}.$$

## Right angles

If $A$ is a right angle its slope is $\infty$ and the formulas in $m_A$ do not apply; the half-wedge forms with $t=1$ and $L=2$ do ([[Extended Constructible Numbers]]).

## Exactness

Every result is a field operation on $r$, $b$, $t$, and $t$ is a field operation on $m_A,\ell_A$. If the data are in $\mathbb K$, so is every result: no cubic and no new square root, like [[IAA Trigonometry]] and unlike [[ISS Trigonometry]].

## Example: $r=4$, $b=14$, $m_A=\tfrac43$

$\ell_A=\tfrac53$, $t=\tfrac12$, $L=\tfrac54$, $\ b\,t-r\,L=7-5=2$.

- $m_{C/2}=\dfrac{4\cdot\frac12}{7-4}=\dfrac23$, $\ m_{B/2}=\dfrac{2}{14/4}=\dfrac47$.
- $x=8$, $z=\dfrac{3}{1/2}=6$, $y=\dfrac{4\cdot14\cdot\frac14}{2}=7$.
- $a=y+z=13$ and $c=x+y=15$.
- $Q=\dfrac{14\cdot4\cdot3}{2}=84$.
- $R=\dfrac{a\,L}{4t}=\dfrac{13\cdot\frac54}{4\cdot\frac12}=\dfrac{65}{8}$.

The $13,14,15$ triangle ([[SSS Trigonometry]]).

## Example: an obtuse wedge

$r=\dfrac{2\sqrt3-3}2$, $b=1$, $m_A=-\sqrt3$, $\ell_A=-2$ (the interior wedge of a regular hexagon). Then $t=\sqrt3$, $L=4$, $b\,t-r\,L=6-3\sqrt3$.

- $m_{C/2}=\dfrac{r\sqrt3}{\sqrt3-r}=2-\sqrt3$ and $m_{B/2}=\dfrac{6-3\sqrt3}{3}=2-\sqrt3$.
- $x=\dfrac r{\sqrt3}=1-\dfrac{\sqrt3}2$, $\ z=\dfrac{\sqrt3}2$, $\ y=\dfrac{3r}{6-3\sqrt3}=\dfrac{\sqrt3}2$.
- $a=\sqrt3$, $\ c=1$.
- $Q=\dfrac{r\cdot\frac32}{6-3\sqrt3}=\dfrac{\sqrt3}4$ and $R=\dfrac{\sqrt3\cdot4}{4\sqrt3}=1$.

This is the $1,1,\sqrt3$ triangle.
