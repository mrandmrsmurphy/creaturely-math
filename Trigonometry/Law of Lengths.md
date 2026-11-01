---
title: Law of Lengths
type: law
status: canonical
provenance: murphy+ai (statement and use Murphy's; proof text drafted by AI)
sources: "[[SRC Constructible Trigonometry Textbook (md)]]"
updated: 2026-10-07
---

# Law of Lengths

In triangle $ABC$ with sides $a,b,c$ opposite the wedges $A,B,C$,

$$c^2=a^2+b^2-\frac{2ab}{\ell_C}.$$

(In other frameworks this is the Law of Cosines, with $1/\ell_C=\cos C$.)

## Solving for $\ell$

The law is used most often to find a characteristic length from three sides:

$$\boxed{\ell_C=\frac{2ab}{a^2+b^2-c^2}}$$

and likewise $\ell_A=\dfrac{2bc}{b^2+c^2-a^2}$ and $\ell_B=\dfrac{2ac}{a^2+c^2-b^2}$.

- $\ell$ is a **rational** function of the sides: no square root, no approximation. Then $m_C=\pm\sqrt{\ell_C^2-1}$, with the sign of $\ell_C$ ([[Characteristic Length]]).
- **The sign comes free.** $\ell_C>0$ when $a^2+b^2>c^2$ (acute), $\ell_C<0$ when $a^2+b^2<c^2$ (obtuse). If $a^2+b^2=c^2$ the denominator is $0$ and $\ell_C=2ab/0=\infty$, a right angle ([[Extended Constructible Numbers]]).
- The extremes: $c=a+b$ gives $\ell_C=-1$ (a straight wedge), and $c=|a-b|$ gives $\ell_C=1$ (no wedge).

Examples:

- Sides $13,14,15$, $c=15$: $\ell_C=\dfrac{2\cdot13\cdot14}{169+196-225}=\dfrac{364}{140}=\dfrac{13}{5}$, so $m_C=\sqrt{\tfrac{169}{25}-1}=\dfrac{12}{5}$.
- Sides $1,1,\sqrt3$: $\ell_C=\dfrac{2}{1+1-3}=-2$ and $m_C=-\sqrt3$ — the interior wedge of a regular hexagon.
- Sides $3,4,5$: $\ell_C=\dfrac{24}{9+16-25}=\dfrac{24}{0}=\infty$ — a right angle.

## Derivation

Drop the altitude from $A$ to the line $BC$, with foot $D$.

- In the right triangle $ADC$, wedge $C$ and hypotenuse $b$ give (hypotenuse : run : rise $=\ell_C:1:m_C$) the run $CD=\dfrac{b}{\ell_C}$ and the height $h=\dfrac{b\,m_C}{\ell_C}$. For an obtuse wedge $\ell_C<0$, so $CD<0$: the foot lies on the extension of $BC$ beyond $C$, and no separate case is needed.
- Then $DB=a-\dfrac{b}{\ell_C}$.
- Pythagoras on the right triangle $ADB$:
$$c^2=h^2+DB^2=\frac{b^2m_C^2}{\ell_C^2}+a^2-\frac{2ab}{\ell_C}+\frac{b^2}{\ell_C^2}=a^2-\frac{2ab}{\ell_C}+\frac{b^2\,(1+m_C^2)}{\ell_C^2}.$$
- Since $\ell_C^2=1+m_C^2$, the last term is $b^2$:
$$c^2=a^2+b^2-\frac{2ab}{\ell_C}.\qquad\blacksquare$$

Solving for $\ell_C$ gives the boxed form.

**Right angle.** The derivation divides by $\ell_C$, so it assumes $C$ is not a right angle. For a right angle the law is the Pythagorean theorem, $c^2=a^2+b^2$, stated directly. Writing it as $c^2=a^2+b^2-2ab/\ell_C$ with $\ell_C=\infty$ would need $x/\infty=0$, which is the open item on [[Extended Constructible Numbers]].

## Remarks
* In other frameworks, this is called the Law of Cosines