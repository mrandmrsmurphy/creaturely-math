---
title: ASA Trigonometry
type: method
status: canonical
provenance: murphy (formulas and method); murphy+ai (derivations, examples)
sources: "Murphy's Constructible Trigonometry textbook (2026)"
updated: 2026-10-07
---

# ASA Trigonometry

**Given** two wedges and the side between them ([[ASA Congruence]]). Without loss of generality the side is $b=AC$ and the wedges are $A$ and $C$ at its ends. So $b$, $m_A,\ell_A$ and $m_C,\ell_C$ are known ([[Slope]], [[Characteristic Length]]). The wedges must together be narrower than a straight wedge. **Find** the third wedge, the other two sides, the area, the inradius and the circumradius.

In a right triangle with a wedge of slope $m$ and characteristic length $\ell$, the hypotenuse, the leg next to the wedge, and the leg opposite it are in the ratio $\ell:1:m$.

## The missing wedge

By the [[Law of Slopes]]:

$$m_B=\frac{m_A+m_C}{m_Am_C-1}.$$

## The missing sides

Drop the altitude $h$ from $B$ to $AC$, with foot $E$.

- In the right triangle $BEA$ the leg next to wedge $A$ is $AE$ and the leg opposite is $h$, so $AE=\dfrac{h}{m_A}$. Likewise $CE=\dfrac{h}{m_C}$.
- $b=AE+CE=h\left(\dfrac1{m_A}+\dfrac1{m_C}\right)$, so
$$h=b\,\frac{m_Am_C}{m_A+m_C}.$$
- The hypotenuses are $a=h\,\dfrac{\ell_C}{m_C}$ and $c=h\,\dfrac{\ell_A}{m_A}$:

$$c=b\,\frac{m_C\,\ell_A}{m_A+m_C},\qquad a=b\,\frac{m_A\,\ell_C}{m_A+m_C}.$$

(For an obtuse $A$ or $C$ the foot $E$ falls outside $AC$ and the signs of $m$ and $\ell$ account for it.)

## The missing area

Half the base times the altitude:

$$Q=\frac12\,b\,h=\frac{b^2}{2}\cdot\frac{m_Am_C}{m_A+m_C}.$$

## The inradius

$$r=b\,\frac{m_{A/2}\,m_{C/2}}{m_{A/2}+m_{C/2}},\qquad m_{X/2}=\frac{m_X}{\ell_X+1}.$$

The center of the incircle lies on the bisectors of $A$ and $C$, and the incircle touches $AC$ at a point $P$. In the right triangles formed with the center, $AP=r/m_{A/2}$ and $CP=r/m_{C/2}$, and $AP+CP=b$. This is the altitude computation above, applied to the half-wedges ([[Characteristic Length#Half a wedge]]). The same expression with the full slopes, $b\,m_Am_C/(m_A+m_C)$, is the altitude $h$, not the inradius.

## The circumradius

$$R=\frac b2\cdot\frac{\ell_A\,\ell_C}{m_A+m_C}.$$

This is the [[Law of the Circumdiameter]], $2R=a\,\ell_A/m_A$, with $a$ from above.

## Right angles

If $A$ or $C$ is a right angle the slope is $\infty$ and the formulas above do not apply ([[Extended Constructible Numbers]]). Read the sides directly off the right triangle.

## Exactness

All results are field operations on $b$ and the slopes and lengths of the two given wedges. If those are in $\mathbb K$, so is every result.

## Example: $b=14$, $m_A=\tfrac43$, $m_C=\tfrac{12}5$

Here $\ell_A=\tfrac53$, $\ell_C=\tfrac{13}5$.

- $m_B=\dfrac{56/15}{16/5-1}=\dfrac{56}{33}$.
- $h=14\cdot\dfrac{16/5}{56/15}=12$, $\ c=12\cdot\dfrac{5/3}{4/3}=15$, $\ a=12\cdot\dfrac{13/5}{12/5}=13$.
- $Q=\dfrac{196}2\cdot\dfrac{16/5}{56/15}=84$.
- $m_{A/2}=\dfrac12$, $m_{C/2}=\dfrac23$, so $r=14\cdot\dfrac{1/3}{7/6}=4$.
- $R=7\cdot\dfrac{(5/3)(13/5)}{56/15}=\dfrac{65}8$.

The $13,14,15$ triangle again ([[SSS Trigonometry]]).

## Example: an obtuse third wedge

$b=\sqrt3$, $m_A=m_C=\dfrac1{\sqrt3}$ (so $\ell_A=\ell_C=\dfrac2{\sqrt3}$).

- $m_B=-\sqrt3$: $B$ is the interior wedge of a regular hexagon.
- $h=\dfrac12$, $\ a=c=1$.
- $Q=\dfrac{\sqrt3}4$, $\ R=1$, $\ r=\dfrac{2\sqrt3-3}2$.
