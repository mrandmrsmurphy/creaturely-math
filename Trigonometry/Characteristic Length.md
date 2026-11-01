---
title: Characteristic Length
type: concept
status: canonical
provenance: murphy+ai (definition Murphy's; page drafted by AI)
sources: "[[SRC Constructible Trigonometry Textbook (md)]]"
updated: 2026-10-07
---

# Characteristic Length

The second primitive of [[Constructible Trigonometry]], after [[Slope]]. It is *not* ordinary length (distance is never negative), though it is often abbreviated to "length" when context is clear.

## Definition

$$\ell=\pm\sqrt{1+m^2},$$

where $m$ is a [[Slope]] and the sign records orientation:

- $\ell>0$ — the direction points **rightward**;
- $\ell<0$ — the direction points **leftward**.

Geometrically: a direction of slope $m$ from the origin, followed rightward, meets the vertical line $x=1$ at $(1,m)$, at distance $+\sqrt{1+m^2}$ — the hypotenuse of the *defining right triangle* (base $1$, height $m$). Followed leftward it meets $x=-1$ at $(-1,-m)$, at signed distance $-\sqrt{1+m^2}$.

The relation $\ell^2=1+m^2$ is exact ([[Equal Signs]]). Conversely, $\ell$ determines $m$ up to sign:

$$m=\pm\sqrt{\ell^2-1}.$$

For the interior wedge of a triangle (narrower than a straight wedge), $m$ and $\ell$ have the same sign: both positive when the wedge is acute, both negative when it is obtuse.

## $(m,\ell)$ covers every direction

| direction | $\ell$ | $m$ | endpoint | quadrant |
|---|---|---|---|---|
| rightward, rising | $+$ | $+$ | $(1,m)$ | I |
| leftward, rising | $-$ | $-$ | $(-1,-m)$ | II |
| leftward, falling | $-$ | $+$ | $(-1,-m)$ | III |
| rightward, falling | $+$ | $-$ | $(1,m)$ | IV |

The pair $(m,\ell)$ determines the unit direction $\left(\dfrac1\ell,\dfrac m\ell\right)$, so its horizontal part is $1/\ell$ and its vertical part is $m/\ell$, with the correct signs in all four quadrants and no case analysis (other frameworks: $\cos$ and $\sin$). In the $(m,\ell)$ plane, $\ell^2-m^2=1$ is a hyperbola whose right branch ($\ell>0$) holds the rightward directions and left branch ($\ell<0$) the leftward ones.

The horizontal directions are $m=0$, $\ell=\pm1$. The two vertical directions have $m=\infty$ and are not captured by a finite pair; they need the point $\infty$ of $\mathbb P^1(\mathbb K)$ and a separate up/down label.

## Addition law

Slopes add by $m_{A+B}=\dfrac{m_A+m_B}{1-m_Am_B}$; characteristic lengths by

$$\ell_{A+B}=\frac{\ell_A\,\ell_B}{1-m_Am_B}.$$

With signed $\ell$ this holds in every quadrant, with no sign fixes. It is the product $(1+im_A)(1+im_B)=(1-m_Am_B)+i(m_A+m_B)$ read off in components. Example: $m_A=m_B=2$, $\ell_A=\ell_B=\sqrt5$ gives $m_{A+B}=-\tfrac43$ and $\ell_{A+B}=-\tfrac53$ — leftward and rising, quadrant II, with unit direction $\left(-\tfrac35,\tfrac45\right)$.

## Half a wedge

The half of a wedge $x$, cut by its bisector, has slope and characteristic length

$$m_{x/2}=\frac{\ell_x-1}{m_x}=\frac{m_x}{\ell_x+1},\qquad \ell_{x/2}=\sqrt{\frac{2\,\ell_x}{\ell_x+1}}.$$

Derivation. Let $t=m_{x/2}$. By the [[Sum of Slopes]], $m_x=\dfrac{2t}{1-t^2}$, and $\ell_x=\dfrac{\ell_{x/2}^2}{1-t^2}=\dfrac{1+t^2}{1-t^2}$. Then $\ell_x+1=\dfrac2{1-t^2}$ and $\ell_x-1=\dfrac{2t^2}{1-t^2}$, so $\dfrac{m_x}{\ell_x+1}=t=\dfrac{\ell_x-1}{m_x}$. Finally $\ell_{x/2}^2=1+t^2=\dfrac{(\ell_x+1)^2+\ell_x^2-1}{(\ell_x+1)^2}=\dfrac{2\ell_x}{\ell_x+1}$.

- The two forms for $m_{x/2}$ are equal because $m_x^2=(\ell_x-1)(\ell_x+1)$. Use whichever has a nonzero denominator: $m_x/(\ell_x+1)$ fails only at $\ell_x=-1$, and $(\ell_x-1)/m_x$ fails only at $\ell_x=1$.
- The half-wedge of a wedge narrower than a straight wedge is acute, so $m_{x/2}>0$ and $\ell_{x/2}>0$, and the positive root is the right one. The radicand is always positive since $|\ell_x|\ge1$.
- A straight wedge ($m_x=0$, $\ell_x=-1$) has half a right angle: $m_{x/2}=(\ell_x-1)/m_x=-2/0=\infty$ and $\ell_{x/2}=2\ell_x/0=\infty$ ([[Extended Constructible Numbers]]).
- A right angle ($m_x=\infty$) is not covered, since arithmetic on $\infty$ is undefined. Its half has $m=1$ and $\ell=\sqrt2$.
- Examples: $m_x=\tfrac{12}5,\ \ell_x=\tfrac{13}5$ gives $m_{x/2}=\tfrac23$, $\ell_{x/2}=\tfrac{\sqrt{13}}3$. The regular-hexagon wedge, $m_x=-\sqrt3,\ \ell_x=-2$, gives $m_{x/2}=\sqrt3$, $\ell_{x/2}=2$.

Repeated halving gives nested radicals: see [[Nested Radicals]].

## Obtuse wedges

The wedge at a vertex wider than a right angle has $m<0$ and $\ell<0$ (its second arm points leftward). The sign is what makes the laws of triangles hold unchanged:

- **Law of Lengths**, $c^2=a^2+b^2-\dfrac{2ab}{\ell_C}$: for $a=b=1$, $C$ the interior wedge of a regular hexagon ($m_C=-\sqrt3$, $\ell_C=-2$), $c^2=1+1+1=3$ ✔.
- **[[Law of SAS Area]]**, $Q=\tfrac12ab\,\dfrac{m_C}{\ell_C}$: $\tfrac12\cdot\dfrac{-\sqrt3}{-2}=\dfrac{\sqrt3}{4}>0$ ✔.

With the unsigned $\ell=+2$ the first gives $c^2=1$ and the second a negative area.
