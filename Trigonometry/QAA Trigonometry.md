---
title: QAA Trigonometry
type: method
status: canonical
provenance: murphy (formulas and method); murphy+ai (derivations, signs for an obtuse wedge, examples)
sources: "[[SRC Constructible Trigonometry Textbook (md)]]"
updated: 2026-10-08
---

# QAA Trigonometry

**Given** the area $Q$ and two wedges. Without loss of generality the wedges are $A$ and $B$, so $Q$, $m_A,\ell_A$ and $m_B,\ell_B$ are known ([[Slope]], [[Characteristic Length]]). The side $c=AB$ lies between them. **Find** the three sides, the third wedge, the inradius and the circumradius.

Unlike [[QSS Trigonometry]] and [[SSA Trigonometry]], this case is **not ambiguous**: the two wedges fix the shape, as in [[ASA Trigonometry]], and the area fixes the scale.

In a right triangle with a wedge of slope $m$ and characteristic length $\ell$, the hypotenuse, the leg next to the wedge, and the leg opposite it are in the ratio $\ell:1:m$.

## The missing wedge

By the [[Law of Slopes]]:

$$m_C=\frac{m_A+m_B}{m_Am_B-1}.$$

## The missing sides

Drop the altitude $h$ from $C$ to $AB$. As in [[ASA Trigonometry]], with $c$ the side between the wedges:

$$h=c\,\frac{m_Am_B}{m_A+m_B},\qquad a=h\,\frac{\ell_B}{m_B}=c\,\frac{m_A\ell_B}{m_A+m_B},\qquad b=h\,\frac{\ell_A}{m_A}=c\,\frac{m_B\ell_A}{m_A+m_B}.$$

The area is $Q=\tfrac12ch=\dfrac{c^2}{2}\cdot\dfrac{m_Am_B}{m_A+m_B}$. Solving for $c$:

$$c=\sqrt{2Q\,\frac{m_A+m_B}{m_Am_B}}.$$

Substituting $c$ into $a$ and $b$:

$$a=\left|\ell_B\sqrt{\frac{m_A}{m_B}\cdot\frac{2Q}{m_A+m_B}}\right|,\qquad b=\left|\ell_A\sqrt{\frac{m_B}{m_A}\cdot\frac{2Q}{m_A+m_B}}\right|.$$

**Absolute values.** A side, inradius or circumradius is a length. If $A$ is obtuse then $\ell_A<0$ and the expression inside the bars is negative for $b$, $r$ and $R$ (likewise $a$, $r$, $R$ if $B$ is obtuse), so the bars give the length. At most one wedge of a triangle is obtuse.

## The inradius

With the half-wedge slopes ([[Characteristic Length#Half a wedge]]), $r=c\,\dfrac{m_{A/2}\,m_{B/2}}{m_{A/2}+m_{B/2}}$ ([[ASA Trigonometry]]). Substituting $m_{X/2}=\dfrac{m_X}{\ell_X+1}$ and $c$:

$$r=\left|\frac{\sqrt{2Q\,m_Am_B\,(m_A+m_B)}}{m_A(\ell_B+1)+m_B(\ell_A+1)}\right|.$$

## The circumradius

$R=\dfrac c2\cdot\dfrac{\ell_A\ell_B}{m_A+m_B}$ ([[ASA Trigonometry]]), so

$$R=\left|\ell_A\ell_B\sqrt{\frac{Q}{2\,m_Am_B\,(m_A+m_B)}}\right|.$$

## Right angles

If $A$ or $B$ is a right angle its slope is $\infty$ and the formulas do not apply ([[Extended Constructible Numbers]]): read the triangle off directly. A right angle at $C$ is fine: $m_Am_B=1$ gives $m_C=\dfrac{m_A+m_B}{0}=\infty$.

## Exactness

Each of $a,b,c,r,R$ is one square root of a quantity built from $Q,m_A,m_B,\ell_A,\ell_B$ by field operations, so if those are in $\mathbb K$ the results are, with no approximation.

## Example: $Q=84$, $m_A=\tfrac43$, $m_B=\tfrac{56}{33}$

$\ell_A=\tfrac53$, $\ell_B=\tfrac{65}{33}$, $m_A+m_B=\tfrac{100}{33}$, $m_Am_B=\tfrac{224}{99}$.

- $m_C=\dfrac{100/33}{224/99-1}=\dfrac{12}5$.
- $c=\sqrt{168\cdot\dfrac{100/33}{224/99}}=\sqrt{225}=15$.
- $a=\dfrac{65}{33}\sqrt{\dfrac{11}{14}\cdot\dfrac{1386}{25}}=\dfrac{65}{33}\cdot\dfrac{33}5=13$, $\ b=\dfrac53\sqrt{\dfrac{14}{11}\cdot\dfrac{1386}{25}}=\dfrac53\cdot\dfrac{42}5=14$.
- $r=\dfrac{1120/33}{280/33}=4$, since $m_A(\ell_B+1)+m_B(\ell_A+1)=\dfrac{280}{33}$ and $2Q\,m_Am_B(m_A+m_B)=\dfrac{1254400}{1089}$.
- $R=\dfrac{325}{99}\sqrt{\dfrac{9801}{1600}}=\dfrac{65}8$.

This is the $13,14,15$ triangle ([[SSS Trigonometry]]).

## Example: an obtuse wedge

$Q=\dfrac{\sqrt3}4$, $m_A=-\sqrt3$, $\ell_A=-2$ (the interior wedge of a regular hexagon), $m_B=\dfrac1{\sqrt3}$, $\ell_B=\dfrac2{\sqrt3}$. Then $m_A+m_B=-\dfrac2{\sqrt3}$ and $m_Am_B=-1$.

- $m_C=\dfrac{-2/\sqrt3}{-2}=\dfrac1{\sqrt3}$.
- $c=\sqrt{\dfrac{\sqrt3}2\cdot\dfrac{-2/\sqrt3}{-1}}=1$.
- $a=\dfrac2{\sqrt3}\sqrt{(-3)\cdot\left(-\dfrac34\right)}=\dfrac2{\sqrt3}\cdot\dfrac32=\sqrt3$.
- $b=\left|-2\sqrt{\left(-\dfrac13\right)\left(-\dfrac34\right)}\right|=|-1|=1$.
- $r=\left|\dfrac{1}{-(2\sqrt3+4)/\sqrt3}\right|=\dfrac{\sqrt3}{4+2\sqrt3}=\dfrac{2\sqrt3-3}2$.
- $R=\left|(-2)\cdot\dfrac2{\sqrt3}\cdot\dfrac{\sqrt3}4\right|=|-1|=1$.

This is the $1,1,\sqrt3$ triangle.
