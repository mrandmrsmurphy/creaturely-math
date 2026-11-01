---
title: Slope
type: concept
status: canonical
provenance: murphy+ai (definition and framing Murphy's; page drafted by AI)
sources: "[[SRC Constructible Trigonometry Textbook (md)]]"
updated: 2026-10-07
---

# Slope

**The first primitive of [[Constructible Trigonometry]].** Everything else — characteristic length, the addition law, the laws of triangles — is built from slope. There is no angle *measure* (degrees, radians, arc length); the only "angle" is the concrete wedge at a vertex, and slope is how it is described.

## Definition

For two points $(x_1,y_1)\ne(x_2,y_2)$ with $x_1\ne x_2$,

$$m=\frac{y_2-y_1}{x_2-x_1}=\frac{\text{rise}}{\text{run}}.$$

- It does not depend on which two points of the line are used: any two such pairs give similar right triangles, with proportional rise and run. On the line $y=mx+b$ the slope is $m$.
- Horizontal lines have $m=0$. Vertical lines have run $0$: their slope is **$\infty$**. A right angle has slope $\infty$. See [[#Slopes live on 𝕂 ∪ {∞}]].
- If the points have coordinates in the constructible field $\mathbb K$, then $m\in\mathbb K$, since $\mathbb K$ is closed under subtraction and division. Slope needs only exact rational operations, never a transcendental function or an approximation.
- Sign: $m>0$ rises to the right, $m<0$ falls. Parallel lines have equal slope; perpendicular lines have slopes $m$ and $-1/m$.

## The slope of a wedge

An **angle** here is a concrete object: the wedge at a vertex of a triangle. Lay one arm along the positive $x$-axis with the vertex at the origin. The **slope of the wedge** is the slope of the other arm, i.e. the rise over run of the second arm relative to the first.

- A wedge narrower than a right angle has $m>0$; a right angle has $m=\infty$ (the straight wedge, half a rotation, has $m=0$); a wider wedge has $m<0$.
- Congruent wedges have equal slope. $m_A$ denotes the slope of the wedge at vertex $A$.
- To combine wedges, lay them side by side and take the slope of the whole. This is the **addition law** ([[Sum of Slopes]])
$$m_{A+B}=\frac{m_A+m_B}{1-m_Am_B},$$
with identity $0$, inverse $-m$, and $1\oplus1=\infty$ (two half-right wedges make a right wedge). When a slope is $\infty$ the formula is not used; see [[Extended Constructible Numbers]].

## Slopes live on 𝕂 ∪ {∞}

Slopes are numbers of $\mathbb K^+=\mathbb K\cup\{\infty\}$ ([[Extended Constructible Numbers]]), almost as in projective geometry. $\infty$ is the slope of a vertical line and of a right angle. It is not a limit, and arithmetic with it is mostly undefined, so the addition of wedges is taught by cases there.

- Perpendicular: $m\mapsto-1/m$ for $m\ne0$, and $0$ and $\infty$ are perpendicular.
- A slope fixes a direction only up to a half-turn: the wedge and its half-turn rotation have the same $m$. The sign of $\ell$ ([[Characteristic Length]]) says which.

## Characteristic length

The companion of slope is the signed distance $\ell=\pm\sqrt{1+m^2}$ to the point $(1,m)$ (rightward) or $(-1,-m)$ (leftward). Together $m$ and $\ell$ give every direction, and each determines the other up to sign: $\ell=\pm\sqrt{1+m^2}$, $m=\pm\sqrt{\ell^2-1}$. The slope of half a wedge is $m_{x/2}=\dfrac{m_x}{\ell_x+1}$. See [[Characteristic Length]].

## Slope elsewhere

- Slope is what other frameworks call $\tan\theta$, and $\ell$ is their $\sec\theta$. Here those are not defined through an angle measure; slope comes first.
- The difference quotient $\dfrac{f(x+h)-f(x)}{h}$ is the slope of a secant line. This is the same definition, which is why slope is also the primitive of [[Discrete Calculus]].
