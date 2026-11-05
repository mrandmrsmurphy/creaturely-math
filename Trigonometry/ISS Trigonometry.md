---
title: ISS Trigonometry
type: method
status: canonical
provenance: murphy (cubics for the side, the wedge and the area; method); murphy+ai (derivations, the exradius root, the count and $r_{\max}$, circumradius, examples)
sources: "[[SRC Constructible Trigonometry Textbook (md)]]"
updated: 2026-10-08
---

# ISS Trigonometry

**ISS** is *inradius, side, side*. **Given** the inradius $r$ and two sides $a,b$. Without loss of generality the wedge $C$ lies between $a$ and $b$, and $c$ is the third side. **Find** $c$, the wedges, the area and the circumradius.

This is an **ambiguous case** like [[SSA Trigonometry]], but unlike every other case in this folder **the unknown is the root of a cubic**. It is the truly new situation: the answer is generally not in $\mathbb K$.

Throughout, $\sigma=a+b$ and $\delta=a-b$.

## The missing side

Heron's formula ([[Heron's Formula]]) with $Q=r\,s$ and $s=\tfrac12(a+b+c)$ gives $r^2s=(s-a)(s-b)(s-c)$. In $c$:

$$4r^2(\sigma+c)=\bigl(c^2-\delta^2\bigr)(\sigma-c).$$

Expanded, $c$ is a root of

$$c^3-\sigma\,c^2+\bigl(4r^2-\delta^2\bigr)c+\sigma\bigl(\delta^2+4r^2\bigr)=0.$$

The constant term is the same as $a^3+b^3+(a+b)(4r^2-ab)$.

## The three roots

The cubic has three roots, and each has a meaning:

1. A root with $|a-b|<c<a+b$ is a **triangle** with inradius $r$.
2. A second such root is a **second triangle** with the same $a$, $b$, $r$.
3. The remaining root is **negative**. Read $|c|$ as a side: the triangle with sides $a,b,|c|$ has **exradius** $r_c=r$, where $r_c=Q/(s-|c|)$ is the radius of the circle tangent to side $c$ and the extensions of the other two sides. It is not a triangle with inradius $r$.

## How many triangles

Write the equation as $4r^2=g(c)$ with $g(c)=\dfrac{(c^2-\delta^2)(\sigma-c)}{\sigma+c}$. On $|\delta|\le c\le\sigma$, $g$ is $0$ at both ends, positive between, and has one maximum. So:

- $r<r_{\max}$: **two triangles**;
- $r=r_{\max}$: **one triangle**;
- $r>r_{\max}$: **none**.

The maximum is where $g'(c)=0$, which is a second cubic:

$$c^3+\sigma c^2-\sigma^2c-\sigma\delta^2=0,\qquad 4r_{\max}^2=g(c).$$

For $a=b$ it factors, $c(c^2+2ac-4a^2)=0$, so $c=a(\sqrt5-1)$ and $r_{\max}$ is **exact in $\mathbb K$**; for $a\ne b$ it is a root of this cubic and not in $\mathbb K$ in general. For $a=b=1$: $r_{\max}^2=\dfrac{5\sqrt5-11}2$.

## The wedge $C$

Let $x=m_C$. From $r(\sigma+c)=ab\,x/\ell_C$ and $c^2=a^2+b^2-2ab/\ell_C$, eliminating $c$ and then $\ell_C$ (with $1/\ell_C^2=1/(1+x^2)$) leaves a quartic with zero constant term. Dividing by $x$ and by $4r^2$:

$$2r\sigma+\bigl(r^2+ab-\sigma^2\bigr)x+2r\sigma\,x^2+\Bigl(r^2+ab-\sigma^2+\bigl(\tfrac{ab}{2r}\bigr)^2\Bigr)x^3=0.$$

Its three real roots are $m_C$ for the two triangles and for the exradius triangle, matching the roots $c$ above. With $c$ and $m_C$, the other two wedges follow from [[SAS Trigonometry]]:

$$m_A=\frac{a\,m_C}{b\,\ell_C-a},\qquad m_B=\frac{b\,m_C}{a\,\ell_C-b},\qquad \ell_C=\frac{2ab}{a^2+b^2-c^2}.$$

## The area

With $Q=r\,s$ and $c=2Q/r-\sigma$, Heron's formula becomes

$$Q^3-2r\sigma\,Q^2+r^2\bigl(r^2+ab+\sigma^2\bigr)Q-ab\,r^3\sigma=0.$$

Its three roots are the areas of the two triangles and (as $r\,s$ with $c<0$) of the exradius triangle. By Vieta their sum is $2r\sigma$ and their product is $ab\,r^3\sigma$.

## The circumradius

For a triangle found above, $R=\dfrac{abc}{4Q}$ (from the [[Law of the Circumdiameter]] and the [[Law of SAS Area]]).

$R$ is also the root of a cubic in $r,a,b$ alone:

$$(4r)^3R^3+16r^2\bigl(r^2+\delta^2-ab\bigr)R^2-8ab\,r\bigl(2r^2+\delta^2\bigr)R+a^2b^2\bigl(4r^2+\delta^2\bigr)=0.$$

Its three roots are the circumradii of the two triangles and, with a **minus sign**, of the exradius triangle ($c<0$ makes $abc/4Q$ negative). By Vieta the three sum to $-\dfrac{r^2+\delta^2-ab}{4r}$.

## Estimating the maximum inradius

For $a=b$ the maximum is exact: $r_{\max}=a\sqrt{\dfrac{5\sqrt5-11}2}\approx0.3002831\,a$ (the isosceles case, $c=a(\sqrt5-1)$). For $a\ne b$ it is the root of the cubic above, and not in $\mathbb K$. The article offers an approximation:

$$r_{\max}\approx\sqrt{\frac{ab-0.155\,(a^2+b^2)}{7.799}}.$$

Compared with the exact maximum from the cubic:

| $a,b$ | exact $r_{\max}$ | approximation | error |
|---|---|---|---|
| $1,1$ | $0.30028$ | $0.29744$ | $-0.95\%$ |
| $2,3$ | $0.71216$ | $0.71482$ | $+0.37\%$ |
| $13,14$ | $4.04655$ | $4.01026$ | $-0.90\%$ |
| $5,12$ | $2.02561$ | $2.08195$ | $+2.78\%$ |
| $1,2$ | $0.38813$ | $0.39632$ | $+2.11\%$ |
| $1,5$ | $0.45229$ | $0.35267$ | $-22.0\%$ |
| $1,20$ | $0.48765$ | undefined (negative radicand) | |

It is good to a percent or two when $a$ and $b$ are within a factor of about $2.5$, and fails for lopsided triangles: the exact maximum tends to $a/2$ as $b/a$ grows ($0.4876$ at $b=20a$, $0.4975$ at $100a$, $0.4998$ at $1000a$), and the approximation does not.

## Why a cubic: three real roots and an equilateral triangle

The cubic for $c$ has three real roots whenever there are two triangles. A cubic with three real roots is the *casus irreducibilis*, the historical reason complex numbers were invented. There is a geometric picture (the **Siebeck-Marden theorem**, in the form of Northshield): for a depressed cubic $x^3+Px+Q$ with three real roots, an equilateral triangle exists whose incircle has radius $\sqrt{-P/3}$, with the incircle's diameter standing over the cubic's two critical points. The circumradius is then $2\sqrt{-P/3}=\sqrt{-4P/3}$ (twice the inradius), and the vertices are a third of a turn apart. Where the first vertex lies needs a wedge $3\theta$ with $\cos3\theta=\dfrac{3Q}{2P}\sqrt{-\dfrac3P}$, and in general that wedge is not constructible; the roots are then $2\sqrt{-P/3}\cos(\theta-\tfrac{2\pi k}3)$ for $k=0,1,2$ (in radians, for readers coming from other frameworks).

Check: the cubic with roots $-3,1,2$ is $x^3-7x+6$, so $P=-7$, $Q=6$, critical points $\pm\sqrt{7/3}=\pm1.5275$, inradius $1.5275$, circumradius $3.0551$, and $\cos3\theta=-0.842$, which reproduces the three roots.

## When the cubic is reducible

The cubic for $c$ is irreducible over $\mathbb Q$ unless it has a rational root. For $a=13$, $b=14$, $r=4$ it is $(c-15)(c^2-12c-117)$, with the rational root $15$ (a triangle whose third side is in $\mathbb Q$). Among $a,b\le8$ and $r\le5$, $8$ of $180$ cubics have an integer root. When there is a rational root the other two are in $\mathbb K$, from a quadratic.

## Exactness

The three unknowns $c$, $m_C$, $Q$ are roots of three cubics with coefficients in $\mathbb Q(r,a,b)$, so if $r,a,b$ are in $\mathbb K$ these are **generally not in $\mathbb K$**. This is where the hierarchy leaves $\mathbb K$: they are **algebraic** numbers (level 8 of the [[Number Hierarchy]], found by Newton's method), and a cubic with three real roots and no rational root is the *casus irreducibilis*: the roots cannot be written with real radicals. The cases that do stay in $\mathbb K$ are those where the cubic has a rational root.

## Example: $r=4$, $a=13$, $b=14$ (two triangles)

The cubic is $c^3-27c^2+63c+1755=(c-15)(c^2-12c-117)$, so $c=15$ and $c=6\pm3\sqrt{17}$. Here the cubic has a rational root, so everything stays in $\mathbb K$.

| | triangle 1 | triangle 2 | exradius triangle |
|---|---|---|---|
| $c$ | $15$ | $6+3\sqrt{17}\approx18.369$ | $|c|=3\sqrt{17}-6\approx6.369$ |
| $Q$ | $84$ | $66+6\sqrt{17}\approx90.739$ | $66-6\sqrt{17}\approx41.261$ |
| $m_C$ | $\tfrac{12}5$ | $\approx13.166$ | $\approx0.509$ |
| $m_A$, $m_B$ | $\tfrac43$, $\tfrac{56}{33}$ | $\approx0.996$, $\approx1.169$ | |
| $R$ | $\tfrac{65}8$ | $\approx9.211$ | $\approx-7.024$ (circumradius $7.024$) |

Triangle 1 is the $13,14,15$ triangle ([[SSS Trigonometry]]). Here $r_{\max}\approx4.0465$, so $r=4$ lies just below the maximum.

## Example: no triangle

$a=13$, $b=14$, $r=5>r_{\max}\approx4.0465$: no triangle has two such sides and so large an inradius.
