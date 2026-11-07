---
title: AAS Trigonometry
type: method
status: canonical
provenance: murphy (formulas and method); murphy+ai (derivations, inradius in terms of $a$, examples)
sources: "Murphy's Constructible Trigonometry textbook (2026)"
updated: 2026-10-07
---

# AAS Trigonometry

**Given** two wedges and a side that is not between them ([[AAS Congruence]]). Without loss of generality the wedges are $A$ and $C$ and the side is $a=BC$ (adjacent to $C$, opposite $A$). So $m_A,\ell_A,m_C,\ell_C$ and $a$ are known. **Find** the third wedge, the other two sides $b$ and $c$, the area, the inradius and the circumradius.

In a right triangle with a wedge of slope $m$ and characteristic length $\ell$ ([[Slope]], [[Characteristic Length]]), the hypotenuse, the leg next to the wedge, and the leg opposite it are in the ratio $\ell:1:m$.

## The missing wedge

By the [[Law of Slopes]]:

$$m_B=\frac{m_A+m_C}{m_Am_C-1}.$$

## The missing sides

The circumdiameter, from the [[Law of the Circumdiameter]]:

$$2R=\frac{a\,\ell_A}{m_A}.$$

The same law gives $c$ at once:

$$c=2R\,\frac{m_C}{\ell_C}=a\,\frac{m_C\,\ell_A}{m_A\,\ell_C}.$$

For $b$, drop the altitude from $B$ to $AC$, with foot $E$.

- In the right triangle $BEC$ the hypotenuse is $a$ and the wedge is $C$, so $CE=\dfrac{a}{\ell_C}$ and $BE=\dfrac{a\,m_C}{\ell_C}$.
- In the right triangle $BEA$ the wedge is $A$ and the leg opposite it is $BE$, so $AE=\dfrac{BE}{m_A}=\dfrac{a\,m_C}{m_A\,\ell_C}$.
- $b=AC=CE+AE$:

$$b=\frac{a}{\ell_C}+\frac{a\,m_C}{m_A\,\ell_C}=a\,\frac{m_A+m_C}{m_A\,\ell_C}.$$

(For an obtuse $C$ or $A$ the foot $E$ falls outside $AC$, $\ell$ is negative, and the same sum holds with signs.)

## The missing area

Area is half the base $AC$ times the altitude $BE$. Both were found above in terms of $a$, and substituting them:

$$Q=\frac12\cdot a\,\frac{m_A+m_C}{m_A\,\ell_C}\cdot\frac{a\,m_C}{\ell_C}=\frac{a^2\,m_C\,(m_A+m_C)}{2\,m_A\,\ell_C^2}.$$

## The inradius

$$r=a\,\frac{m_{C/2}\,\ell_{A/2}}{\ell_{C/2}\,\ell_{(A+C)/2}}.$$

Derivation. Write $t=m_{A/2}$, $u=m_{C/2}$, $v=m_{B/2}$ for the slopes of the half-wedges, with $m_{X/2}=\dfrac{m_X}{\ell_X+1}$ ([[Characteristic Length#Half a wedge]]).

- The incircle touches $BC$ at $T$. Its center lies on the bisectors, so in the right triangles formed with the center, $CT=r/u$ and $BT=r/v$. Since $CT+BT=a$, $r=a\,\dfrac{uv}{u+v}$.
- The three half-wedges together make a right angle, so $B/2$ and $W=(A+C)/2$ make a right angle: $v=1/m_W$, where $m_W=\dfrac{t+u}{1-tu}$ by the [[Sum of Slopes]], and $\ell_W=\dfrac{\ell_{A/2}\,\ell_{C/2}}{1-tu}$.
- Then $\dfrac{v}{u+v}=\dfrac1{1+u\,m_W}$, and $1+u\,m_W=\dfrac{1+u^2}{1-tu}=\dfrac{\ell_{C/2}^{\,2}}{1-tu}=\dfrac{\ell_{C/2}\,\ell_W}{\ell_{A/2}}$. So $r=a\,u\,\dfrac{\ell_{A/2}}{\ell_{C/2}\,\ell_W}$.

Equivalently, with no square roots beyond those already in $\mathbb K$,

$$r=a\,\frac{u\,(1-tu)}{1+u^2}.$$

## The circumradius

$$R=\frac{a\,\ell_A}{2\,m_A}.$$

## Right angles

If $A$ or $C$ is a right angle the slope is $\infty$ and the formulas above do not apply ([[Extended Constructible Numbers]]). Read the sides directly off the right triangle.

## Exactness

All results are field operations on $a$ and the slopes and lengths of the two given wedges. If those are in $\mathbb K$, so is every result.

## Example: $a=13$, $m_A=\tfrac43$, $m_C=\tfrac{12}5$

Here $\ell_A=\tfrac53$, $\ell_C=\tfrac{13}5$.

- $m_B=\dfrac{4/3+12/5}{(4/3)(12/5)-1}=\dfrac{56/15}{11/5}=\dfrac{56}{33}$.
- $b=13\cdot\dfrac{56/15}{(4/3)(13/5)}=14$, $\ c=13\cdot\dfrac{(12/5)(5/3)}{(4/3)(13/5)}=15$.
- $Q=\dfrac{169\cdot\frac{12}5\cdot\frac{56}{15}}{2\cdot\frac43\cdot\frac{169}{25}}=84$.
- $m_{C/2}=\dfrac{12/5}{18/5}=\dfrac23$, $\ell_{A/2}=\dfrac{\sqrt5}2$, $\ell_{C/2}=\dfrac{\sqrt{13}}3$, and $m_{(A+C)/2}=\dfrac74$ so $\ell_{(A+C)/2}=\dfrac{\sqrt{65}}4$. Then $r=13\cdot\dfrac{\frac23\cdot\frac{\sqrt5}2}{\frac{\sqrt{13}}3\cdot\frac{\sqrt{65}}4}=4$.
- $R=\dfrac{13\cdot5/3}{2\cdot4/3}=\dfrac{65}8$.

This is the $13,14,15$ triangle again ([[SSS Trigonometry]]).

## Example: an obtuse third wedge

$a=1$, $m_A=m_C=\dfrac1{\sqrt3}$ (so $\ell_A=\ell_C=\dfrac2{\sqrt3}$).

- $m_B=\dfrac{2/\sqrt3}{1/3-1}=-\sqrt3$: $B$ is the interior wedge of a regular hexagon.
- $b=\sqrt3$, $\ c=1$.
- $Q=\dfrac{\sqrt3}4$, $\ R=1$.
- $A=C$, so $\ell_{A/2}=\ell_{C/2}$ and $(A+C)/2=A$: $r=a\,\dfrac{m_{C/2}}{\ell_A}=\dfrac{2-\sqrt3}{2/\sqrt3}=\dfrac{2\sqrt3-3}2$.
