---
title: QAS Trigonometry
type: method
status: canonical
provenance: murphy (formulas and method); murphy+ai (derivations, corrections to $a$ and $r$, signs, examples)
sources: "Murphy's Constructible Trigonometry textbook (2026)"
updated: 2026-10-08
---

# QAS Trigonometry

**Given** the area $Q$, a wedge $A$, and a side $b$ next to it, so $Q$, $m_A,\ell_A$ and $b=AC$ are known ([[Slope]], [[Characteristic Length]]). The side $c=AB$ is the other side of the wedge. **Find** the other two sides, the other two wedges, the inradius and the circumradius.

This case is **not ambiguous**: the area and the two sides of the wedge $A$ give $c$ outright.

## The missing sides

The [[Law of SAS Area]], $Q=\tfrac12\,b\,c\,\dfrac{m_A}{\ell_A}$, solved for $c$:

$$c=\frac{2Q\,\ell_A}{b\,m_A}.$$

The [[Law of Lengths]], $a^2=b^2+c^2-\dfrac{2bc}{\ell_A}$, with $\dfrac{2bc}{\ell_A}=\dfrac{4Q}{m_A}$:

$$a=\sqrt{\,b^2-\frac{4Q}{m_A}+c^2\,}=\sqrt{\,b^2-\frac{4Q}{m_A}+\left(\frac{2Q\,\ell_A}{b\,m_A}\right)^2}.$$

## The missing wedges

Drop the altitude from $B$ to the line $AC$: its height is $h=\dfrac{2Q}b$ and its foot is $\dfrac c{\ell_A}=\dfrac{2Q}{b\,m_A}$ from $A$. The wedge $C$ has rise $h$ over run $b-\dfrac{2Q}{b\,m_A}$, so

$$\frac1{m_C}=\frac{b^2}{2Q}-\frac1{m_A}.$$

This form has no zero denominator at a right angle: $\dfrac1{m_C}=0$ means $C$ is a right angle ([[Extended Constructible Numbers]]).

By the [[Law of Slopes]], $m_B=\dfrac{m_A+m_C}{m_Am_C-1}$, which simplifies to

$$m_B=\frac{b^2\,m_A^2}{2Q\,\ell_A^2-b^2\,m_A}.$$

## The inradius

$r=Q/s=\dfrac{2Q}{a+b+c}$. Multiplying top and bottom by $b\,m_A$ turns $c$ into $2Q\ell_A$ and $a$ into $\sqrt{b^4m_A^2-4Q\,b^2m_A+4Q^2\ell_A^2}$:

$$r=\frac{2Q\,b\,|m_A|}{\,\bigl|b^2m_A+2Q\,\ell_A\bigr|+\sqrt{b^4m_A^2-4Q\,b^2m_A+4Q^2\ell_A^2}\,}.$$

The bars are for an obtuse $A$, where $m_A$ and $\ell_A$ are negative: then the first two terms of the denominator are negative and the root has to enter with a positive sign. The bars make that automatic. The radicand is $(b\,m_A\,a)^2$ and is never negative.

## The circumradius

The [[Law of the Circumdiameter]], $2R=\dfrac{a\,\ell_A}{m_A}$ (positive, since $m_A$ and $\ell_A$ have the same sign):

$$R=\frac{a\,\ell_A}{2\,m_A}.$$

In terms of the data alone, with $a=\dfrac{\sqrt{b^4m_A^2-4Q\,b^2m_A+4Q^2\ell_A^2}}{b\,|m_A|}$ from the inradius:

$$R=\frac{|\ell_A|\,\sqrt{b^4m_A^2-4Q\,b^2m_A+4Q^2\ell_A^2}}{2\,b\,m_A^2}.$$

It has the same radicand as the inradius, $(b\,m_A\,a)^2$. The bars on $\ell_A$ make $R$ positive when $A$ is obtuse. For the example below, $\dfrac{(5/3)\cdot\frac{728}3}{2\cdot14\cdot\frac{16}9}=\dfrac{65}8$.

## Right angles

If $A$ is a right angle, $m_A=\infty$ and the formulas do not apply: read the triangle off directly, since $c=2Q/b$ and $a=\sqrt{b^2+c^2}$. A right angle at $C$ or $B$ is fine (see $1/m_C$ above).

## Exactness

$a$ and $r$ each take one square root of a quantity built from $Q,b,m_A,\ell_A$ by field operations, and everything else is field operations, so if the data are in $\mathbb K$ so are the results.

## Example: $Q=84$, $b=14$, $m_A=\tfrac43$

$\ell_A=\tfrac53$.

- $c=\dfrac{168\cdot\frac53}{14\cdot\frac43}=15$.
- $a=\sqrt{196-\dfrac{336}{4/3}+225}=\sqrt{196-252+225}=13$.
- $\dfrac1{m_C}=\dfrac{196}{168}-\dfrac34=\dfrac5{12}$, so $m_C=\dfrac{12}5$.
- $m_B=\dfrac{196\cdot\frac{16}9}{168\cdot\frac{25}9-196\cdot\frac43}=\dfrac{3136/9}{1848/9}=\dfrac{56}{33}$.
- $r$: the denominator is $\left|\tfrac{784}{3}+280\right|+\tfrac{728}{3}=\tfrac{1624}{3}+\tfrac{728}3=784$ and the numerator is $2\cdot84\cdot14\cdot\tfrac43=3136$, so $r=4$.
- $R=\dfrac{13\cdot\frac53}{2\cdot\frac43}=\dfrac{65}8$.

The $13,14,15$ triangle ([[SSS Trigonometry]]).

## Example: an obtuse wedge

$Q=\dfrac{\sqrt3}4$, $b=1$, $m_A=-\sqrt3$, $\ell_A=-2$ (the interior wedge of a regular hexagon).

- $c=\dfrac{2\cdot\frac{\sqrt3}4\cdot(-2)}{1\cdot(-\sqrt3)}=1$.
- $a=\sqrt{1-\dfrac{\sqrt3}{-\sqrt3}+1}=\sqrt3$.
- $\dfrac1{m_C}=\dfrac2{\sqrt3}+\dfrac1{\sqrt3}=\sqrt3$, so $m_C=\dfrac1{\sqrt3}$. And $m_B=\dfrac{3}{2\sqrt3+\sqrt3}=\dfrac1{\sqrt3}$.
- $r=\dfrac{2\cdot\frac{\sqrt3}4\cdot\sqrt3}{|-\sqrt3-\sqrt3|+3}=\dfrac{3/2}{2\sqrt3+3}=\dfrac{2\sqrt3-3}2$.
- $R=\dfrac{\sqrt3\cdot(-2)}{2\cdot(-\sqrt3)}=1$.

This is the $1,1,\sqrt3$ triangle.
