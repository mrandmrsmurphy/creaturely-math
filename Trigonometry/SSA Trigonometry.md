---
title: SSA Trigonometry
type: method
status: canonical
provenance: murphy (formulas, discriminant, and method); murphy+ai (derivations, corrected inradius, case count, examples)
sources: "Murphy's Constructible Trigonometry textbook (2026)"
updated: 2026-10-07
---

# SSA Trigonometry

**Given** two sides and a wedge that is **not** between them: the sides $a,b$ and the wedge $A$, which is opposite $a$ and next to $b$ (SSA, the ambiguous case; compare [[SAS Congruence]]). So $a$, $b$, $m_A$, $\ell_A$ are known ([[Slope]], [[Characteristic Length]]). The data can fit **no** triangle, **one**, or **two**. Write $c_1,c_2$ for the two possible third sides, and $1,2$ for the two triangles.

The right-angle case ($A$ a right angle, $m_A=\infty$) is not covered; there $a$ is the hypotenuse and the triangle is determined.

## The discriminant

$$D=D_{abA}=\sqrt{a^2\ell_A^2-b^2m_A^2}\;=\;\sqrt{a^2+(a^2-b^2)\,m_A^2}.$$

Most of the formulas below contain $D$. It has its origin in the third side:

## The missing side

The [[Law of Lengths]] with the wedge $A$ between $b$ and $c$ says $a^2=b^2+c^2-\dfrac{2bc}{\ell_A}$. As an equation for $c$:

$$\ell_A\,c^2-2b\,c+\ell_A(b^2-a^2)=0\quad\Longrightarrow\quad c_{1,2}=\frac{b\pm\sqrt{b^2-\ell_A^2(b^2-a^2)}}{\ell_A}.$$

Since $\ell_A^2-1=m_A^2$, the radicand is $a^2\ell_A^2-b^2m_A^2=D^2$:

$$c_{1,2}=\frac{b\pm D}{\ell_A}.$$

Geometrically: the circle of radius $a$ about $C$ meets the ray from $A$ in $0$, $1$ or $2$ points.

## How many triangles

Let $h=b\,\dfrac{m_A}{\ell_A}$, the altitude from $C$ to the line $AB$. Then $D=\ell_A\sqrt{a^2-h^2}$.

- **$A$ acute.**
  - $a<h$: $D$ is not real, **no triangle**.
  - $a=h$: $D=0$, **one triangle**, with a right angle at $B$.
  - $h<a<b$: $0<D<b$, so both $c_1,c_2>0$: **two triangles**.
  - $a\ge b$: $D\ge b$, so $c_2\le0$: **one triangle**, $c_1$.
- **$A$ obtuse** ($\ell_A,m_A<0$). Need $a>b$ (the side opposite an obtuse wedge is the longest); then $D>b$ and only $c_2=(b-D)/\ell_A>0$: **one triangle**. If $a\le b$, none.

## The missing wedges

By the formulas of [[SAS Trigonometry]], with the wedge $A$ between $b$ and $c$:

$$m_{C_{1,2}}=m_A\,\frac{b\pm D}{b\,m_A^2\mp D},\qquad m_{B_{1,2}}=\pm\,\frac{m_A\,b}{D}.$$

Derivation: the SAS formulas give $m_C=\dfrac{c\,m_A}{b\ell_A-c}$ and $m_B=\dfrac{b\,m_A}{c\,\ell_A-b}$. Substituting $c=\dfrac{b\pm D}{\ell_A}$, and using $\ell_A^2-1=m_A^2$, gives the two. In particular $m_{B_2}=-m_{B_1}$: the wedges $B_1,B_2$ are supplements, since both triangles sit in the same circle.

## The missing area

The [[Law of SAS Area]] with the wedge $A$ between $b$ and $c$, $Q=\tfrac12\,b\,c\,\dfrac{m_A}{\ell_A}$:

$$Q_{1,2}=\frac{m_A\,b}{2\,\ell_A^2}\,(b\pm D).$$

## The inradius

$r=Q/s$ with $s=\tfrac12(a+b+c)$:

$$r_{1,2}=\frac{m_A\,b\,(b\pm D)}{\ell_A\bigl(\ell_A\,(a+b)+(b\pm D)\bigr)}.$$

## The circumradius

The same for both triangles:

$$R=\frac{a\,\ell_A}{2\,m_A}.$$

This is the [[Law of the Circumdiameter]]. Both triangles are inscribed in the same circle.

## Exactness

$D$ is one square root of a quantity built from $a,b,m_A,\ell_A$ by field operations, so if those are in $\mathbb K$, then $D$ is, and so is every result for both triangles.

## Example: $a=13$, $b=14$, $m_A=\tfrac43$ (two triangles)

$\ell_A=\tfrac53$, $h=14\cdot\dfrac{4/3}{5/3}=\dfrac{56}5=11.2<13<14$, and $D=\sqrt{\tfrac{169\cdot25}{9}-\tfrac{196\cdot16}9}=\sqrt{121}=11$.

| | triangle 1 ($+D$) | triangle 2 ($-D$) |
|---|---|---|
| $c$ | $\dfrac{25}{5/3}=15$ | $\dfrac{3}{5/3}=\dfrac95$ |
| $m_C$ | $\dfrac{(4/3)\cdot25}{14\cdot\frac{16}9-11}=\dfrac{12}5$ | $\dfrac{(4/3)\cdot3}{14\cdot\frac{16}9+11}=\dfrac{36}{323}$ |
| $m_B$ | $\dfrac{(4/3)\cdot14}{11}=\dfrac{56}{33}$ | $-\dfrac{56}{33}$ |
| $Q$ | $84$ | $\dfrac{252}{25}$ |
| $r$ | $4$ | $\dfrac7{10}$ |

$R=\dfrac{13\cdot5/3}{2\cdot4/3}=\dfrac{65}8$ for both. Triangle 1 is the $13,14,15$ triangle ([[SSS Trigonometry]]). Triangle 2 has sides $13,14,\tfrac95$, and Heron gives $Q=\tfrac{252}{25}$.

## Example: an obtuse wedge (one triangle)

$a=\sqrt3$, $b=1$, $A$ the interior wedge of a regular hexagon: $m_A=-\sqrt3$, $\ell_A=-2$. Then $D=\sqrt{12-3}=3$. The $+D$ root gives $c=\dfrac{1+3}{-2}=-2$, rejected; the $-D$ root gives $c=\dfrac{1-3}{-2}=1$. So $m_C=m_B=\dfrac{(-\sqrt3)(-2)}{3+3}=\dfrac1{\sqrt3}$, $Q=\dfrac{\sqrt3}4$, $r=\dfrac{2\sqrt3-3}2$, $R=1$: the $1,1,\sqrt3$ triangle.
