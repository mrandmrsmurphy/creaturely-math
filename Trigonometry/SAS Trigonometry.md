---
title: SAS Trigonometry
type: method
status: canonical
provenance: murphy (formulas and method); murphy+ai (derivations, half-wedge slope, examples)
sources: "[[SRC Constructible Trigonometry Textbook (md)]]"
updated: 2026-10-07
---

# SAS Trigonometry

**Given** two sides and the wedge between them ([[SAS Congruence]]). Without loss of generality (relabel the vertices) the sides are $a=BC$ and $b=CA$ and the given wedge is $C$, with slope $m_C$ and characteristic length $\ell_C=\pm\sqrt{1+m_C^2}$ ([[Characteristic Length]]). **Find** the third side, the other two wedges, the area, the inradius and the circumradius.

## The missing side

The [[Law of Lengths]]:

$$c=\sqrt{a^2+b^2-\frac{2ab}{\ell_C}}.$$

## The missing wedges

$$m_A=\frac{a\,m_C}{b\,\ell_C-a},\qquad m_B=\frac{b\,m_C}{a\,\ell_C-b}.$$

**Derivation** (no trigonometry beyond the primitives). Drop the altitude from $A$ to the line $BC$, with foot $D$. As in the derivation of the [[Law of Lengths]], the run $CD=b/\ell_C$ and the height is $h=b\,m_C/\ell_C$, so $DB=a-b/\ell_C$. The wedge $B$ has rise $h$ over run $DB$:

$$m_B=\frac{h}{DB}=\frac{b\,m_C/\ell_C}{a-b/\ell_C}=\frac{b\,m_C}{a\,\ell_C-b}.$$

Dropping the altitude from $B$ to $CA$ gives $m_A$ the same way. A zero denominator, $b\ell_C=a$, is a right angle at $A$ ($m_A=\infty$). The sign needs no case split: for an obtuse $C$, $\ell_C<0$ puts $D$ beyond $C$ and the same formula holds.

**Right angle at $C$.** Then $m_C=\ell_C=\infty$ and the formulas above do not apply ([[Extended Constructible Numbers]]). Read the slopes directly off the right triangle: $m_A=a/b$, $m_B=b/a$, $c=\sqrt{a^2+b^2}$.

## The missing area

The [[Law of SAS Area]]:

$$Q=\frac12\,ab\,\frac{m_C}{\ell_C}.$$

## The inradius

$$r=\tfrac12\,m_{C/2}\,(a+b-c),$$

where $m_{C/2}$ is the slope of the half-wedge at $C$ (the wedge cut by the bisector of $C$).

The half-wedge slope comes from $m_C$ and $\ell_C$ alone, $m_{C/2}=\dfrac{m_C}{\ell_C+1}$ ([[Characteristic Length#Half a wedge]]).

Why $r=\tfrac12m_{C/2}(a+b-c)$: the incircle touches $CA$ and $CB$ at distance $s-c=\tfrac12(a+b-c)$ from $C$, and in the right triangle formed with the center, $r=(s-c)\,m_{C/2}$.

## The circumradius

$$R=\frac{\ell_C\sqrt{a^2+b^2-2ab/\ell_C}}{2\,m_C}=\frac{\ell_C\,c}{2\,m_C}.$$

This is the [[Law of the Circumdiameter]], $c\,\ell_C/m_C=2R$, with $c$ from above.

## Exactness

The one square root is in $c$. Everything else is field operations on $a,b,m_C,\ell_C$. If those are in $\mathbb K$, all the results are.

## Example: $a=13$, $b=14$, $m_C=\tfrac{12}5$

Here $\ell_C=\tfrac{13}5$.

- $c=\sqrt{169+196-\dfrac{2\cdot13\cdot14}{13/5}}=\sqrt{365-140}=15$.
- $m_A=\dfrac{13\cdot12/5}{14\cdot13/5-13}=\dfrac43$, $\ m_B=\dfrac{14\cdot12/5}{13\cdot13/5-14}=\dfrac{56}{33}$.
- $Q=\tfrac12\cdot13\cdot14\cdot\dfrac{12/5}{13/5}=84$.
- $m_{C/2}=\dfrac{12/5}{18/5}=\dfrac23$, so $r=\tfrac12\cdot\tfrac23\cdot12=4$.
- $R=\dfrac{(13/5)\cdot15}{2\cdot12/5}=\dfrac{65}8$.

This is the $13,14,15$ triangle of [[SSS Trigonometry]], with the same results.

## Example: an obtuse wedge

$a=b=1$ and $C$ the interior wedge of a regular hexagon: $m_C=-\sqrt3$, $\ell_C=-2$.

- $c=\sqrt{1+1+1}=\sqrt3$.
- $m_A=m_B=\dfrac{-\sqrt3}{-2-1}=\dfrac1{\sqrt3}$.
- $Q=\tfrac12\cdot\dfrac{-\sqrt3}{-2}=\dfrac{\sqrt3}4$.
- $m_{C/2}=\dfrac{-\sqrt3}{-1}=\sqrt3$, so $r=\tfrac12\sqrt3\,(2-\sqrt3)=\dfrac{2\sqrt3-3}2$.
- $R=\dfrac{(-2)\sqrt3}{2(-\sqrt3)}=1$.
