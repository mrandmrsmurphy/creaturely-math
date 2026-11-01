---
title: QSS Trigonometry
type: method
status: canonical
provenance: murphy (formulas and method); murphy+ai (discriminant convention, derivations, two-triangle analysis, examples)
sources: "[[SRC Constructible Trigonometry Textbook (md)]]"
updated: 2026-10-08
---

# QSS Trigonometry

**Given** the area $Q$ and two sides $a,b$. The wedge $C$ between $a$ and $b$ is not given. **Find** the third side, the three wedges, the inradius and the circumradius. This is another ambiguous case, like [[SSA Trigonometry]]: the data can fit two triangles, and the formulas carry $\mp D$.

## The discriminant

$$D=D_{Qab}=2\sqrt{a^2b^2-4Q^2}.$$

The factor $2$ is part of $D$, so the formulas below have only $\mp D$. In every pair the **upper sign is triangle 1**, with $C$ acute, and the **lower sign is triangle 2**, with $C$ obtuse.

## How many triangles

The [[Law of SAS Area]], $Q=\tfrac12ab\,\dfrac{m_C}{\ell_C}$, fixes $\dfrac{m_C}{\ell_C}=\dfrac{2Q}{ab}$, and that leaves the sign of $\ell_C$ free.

- $2Q<ab$: $D>0$, **two triangles** ($C$ acute and $C$ obtuse).
- $2Q=ab$: $D=0$, **one triangle**, with a right angle at $C$.
- $2Q>ab$: $D$ is not real, **no triangle**. Two sides cannot enclose more than $\tfrac12ab$.

## The missing side

$\dfrac1{\ell_C^2}=1-\dfrac{4Q^2}{a^2b^2}=\dfrac{D^2}{4a^2b^2}$ by $\ell_C^2=1+m_C^2$ ([[Characteristic Length]]), so $\dfrac1{\ell_C}=\pm\dfrac{D}{2ab}$. The [[Law of Lengths]] gives

$$c_{1,2}=\sqrt{a^2+b^2\mp D}.$$

The inner root is real: $a^2+b^2-D\ge(a-b)^2\ge0$.

## The missing wedges

$$m_{C_{1,2}}=\pm\frac{4Q}{D},\qquad m_{B_{1,2}}=\frac{4Q}{2a^2\mp D},\qquad m_{A_{1,2}}=\frac{4Q}{2b^2\mp D}.$$

Derivation: $m_C=\ell_C\cdot\dfrac{2Q}{ab}=\pm\dfrac{2ab}{D}\cdot\dfrac{2Q}{ab}=\pm\dfrac{4Q}{D}$. Then $m_B$ and $m_A$ follow from the formulas of [[SAS Trigonometry]], $m_B=\dfrac{b\,m_C}{a\ell_C-b}$ and $m_A=\dfrac{a\,m_C}{b\ell_C-a}$. Each is positive when its wedge is acute and negative when it is obtuse.

## The inradius

$r=Q/s$ with $s=\tfrac12(a+b+c)$:

$$r_{1,2}=\frac{2Q}{a+b+\sqrt{a^2+b^2\mp D}}.$$

## The circumradius

$R=\dfrac{abc}{4Q}$, from the [[Law of the Circumdiameter]] and the [[Law of SAS Area]]:

$$R_{1,2}=\frac{ab\sqrt{a^2+b^2\mp D}}{4Q}.$$

## Right angle at $C$

When $2Q=ab$, $D=0$ and $m_C=4Q/0=\infty$ ([[Extended Constructible Numbers]]). Then $c=\sqrt{a^2+b^2}$, $m_B=b/a$, $m_A=a/b$.

## Exactness

$D$ is one square root and $c$ a second. Everything else is field operations, so if $a,b,Q\in\mathbb K$ then everything for both triangles is in $\mathbb K$.

## Example: $a=13$, $b=14$, $Q=84$ (two triangles)

$D=2\sqrt{182^2-4\cdot84^2}=2\sqrt{4900}=140$.

| | triangle 1 ($-D$) | triangle 2 ($+D$) |
|---|---|---|
| $c$ | $\sqrt{365-140}=15$ | $\sqrt{365+140}=\sqrt{505}$ |
| $m_C$ | $\dfrac{336}{140}=\dfrac{12}5$ | $-\dfrac{12}5$ |
| $m_B$ | $\dfrac{336}{338-140}=\dfrac{56}{33}$ | $\dfrac{336}{338+140}=\dfrac{168}{239}$ |
| $m_A$ | $\dfrac{336}{392-140}=\dfrac43$ | $\dfrac{336}{392+140}=\dfrac{12}{19}$ |
| $r$ | $\dfrac{168}{27+15}=4$ | $\dfrac{168}{27+\sqrt{505}}$ |
| $R$ | $\dfrac{182\cdot15}{336}=\dfrac{65}8$ | $\dfrac{13\sqrt{505}}{24}$ |

Triangle 1 is the $13,14,15$ triangle ([[SSS Trigonometry]]).

## Example: the equilateral triangle and the regular hexagon wedge

$a=b=1$, $Q=\dfrac{\sqrt3}4$: $D=2\sqrt{1-\tfrac34}=1$.

- Triangle 1: $c=\sqrt{2-1}=1$, $m_C=\sqrt3$, $m_B=m_A=\dfrac{\sqrt3}{2-1}=\sqrt3$: the **equilateral triangle**.
- Triangle 2: $c=\sqrt3$, $m_C=-\sqrt3$, $m_B=m_A=\dfrac{\sqrt3}{2+1}=\dfrac1{\sqrt3}$: the $1,1,\sqrt3$ triangle with the interior wedge of a regular hexagon at $C$.

Both have the same two sides and the same area.
