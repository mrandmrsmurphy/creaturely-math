---
title: Symmetries of the Equilateral Triangle
type: concept
status: canonical (draft)
provenance: "murphy+ai (Murphy's brief: the symmetries of the equilateral triangle as a finite object; every table, subgroup and class below was computed and checked by exhaustive check)"
sources: "[[Groups]]"
updated: 2026-10-08
---

# Symmetries of the Equilateral Triangle

A **symmetry** of the equilateral triangle is a distance-preserving map of the plane onto itself (an *isometry*) that carries the triangle onto itself. There are exactly **six**, so they form a group of order $6$ ([[Groups]]). It is the smallest nonabelian group.

## The six symmetries

Label the three vertices by the balanced digits of $\mathrm{GF}(3)$ ([[GF(3)]]): $\bar1,\ 0,\ 1$, placed in order a third of a turn apart, counterclockwise. A symmetry is determined by where it sends the vertices, and each pair of vertices is joined by a side of the same length, so **every permutation of the three vertices is realized**: $3!=6$, and there are no others.

- **$e$**: do nothing.
- **$r$**: a third of a turn counterclockwise. It sends vertex $x$ to $x+1$ (mod $3$): $0\to1\to\bar1\to0$.
- **$r^2$**: two thirds of a turn. $r^3=e$.
- **$s_a$** for $a=\bar1,0,1$: the **reflection** in the line through vertex $a$ and the midpoint of the opposite side. It fixes vertex $a$ and swaps the other two. As a map on the vertices, $s_a(x)=-x-a$ (mod $3$).

(The three reflection lines are the medians, which for an equilateral triangle are also the altitudes, the angle bisectors and the perpendicular bisectors.)

## Rotations and reflections

The three **rotations** $e,r,r^2$ can be done by *sliding* the triangle around inside the plane. The three **reflections cannot**: to turn the triangle into its mirror image it has to be **flipped over**, which needs the third dimension. A creature confined to the plane could never do it. A being with a third dimension does it by a half turn about the reflection line in space.

One dimension up, the same holds: no motion in space turns a left hand into a right hand, but a being with a fourth dimension could. A reflection in $n$ dimensions is a rotation in $n+1$.

That is the quotient of order $2$ below. The rotations have determinant $+1$ (they preserve orientation) and the reflections have determinant $-1$. *Isometry* is the right definition because it asks only for distances to be kept, not for a continuous motion inside the plane.

## The Cayley table

The product $ab$ means *do $b$ first, then $a$*.

| | $e$ | $r$ | $r^2$ | $s_{\bar1}$ | $s_0$ | $s_1$ |
|---|---|---|---|---|---|---|
| **$e$** | $e$ | $r$ | $r^2$ | $s_{\bar1}$ | $s_0$ | $s_1$ |
| **$r$** | $r$ | $r^2$ | $e$ | $s_1$ | $s_{\bar1}$ | $s_0$ |
| **$r^2$** | $r^2$ | $e$ | $r$ | $s_0$ | $s_1$ | $s_{\bar1}$ |
| **$s_{\bar1}$** | $s_{\bar1}$ | $s_0$ | $s_1$ | $e$ | $r$ | $r^2$ |
| **$s_0$** | $s_0$ | $s_1$ | $s_{\bar1}$ | $r^2$ | $e$ | $r$ |
| **$s_1$** | $s_1$ | $s_{\bar1}$ | $s_0$ | $r$ | $r^2$ | $e$ |

- **Not abelian:** $r\,s_0=s_{\bar1}$ but $s_0\,r=s_1$. Doing the rotation then the reflection is not the same as the reflection then the rotation.
- **The relation** $s\,r\,s=r^{-1}$: conjugating a rotation by a reflection reverses it ($s_0\,r\,s_0=r^2$). With $r^3=e$ and $s^2=e$ this describes the whole group.
- Every row and column holds each element once (the Latin square property).

## Element orders

| order | elements | how many |
|---|---|---|
| $1$ | $e$ | 1 |
| $2$ | $s_{\bar1},s_0,s_1$ | 3 |
| $3$ | $r,r^2$ | 2 |

No element has order $6$, so the group is not cyclic.

## Subgroups

There are **six** subgroups (checked by trying every subset): $\{e\}$; the three reflection subgroups $\{e,s_a\}$ of order $2$; the rotation subgroup $\{e,r,r^2\}$ of order $3$; and the whole group. Their orders $1,2,2,2,3,6$ all divide $6$, as Lagrange's theorem says.

- The **rotations** $\{e,r,r^2\}$ form a copy of $\mathbb Z/3$, the additive group of $\mathrm{GF}(3)$.
- There is no subgroup of order $4$ or $5$.

## Conjugacy classes and normal subgroups

Elements $h$ and $ghg^{-1}$ are **conjugate**. The classes are

$$\{e\},\qquad \{r,r^2\},\qquad \{s_{\bar1},s_0,s_1\}$$

and $6=1+2+3$. The three reflections are conjugate to one another: they are "the same kind of symmetry seen from three vertices". The **center** (elements commuting with everything) is $\{e\}$.

A subgroup is **normal** when it is a union of conjugacy classes. The normal subgroups are $\{e\}$, the rotations $\{e,r,r^2\}$, and the whole group. The reflection subgroups $\{e,s_a\}$ are **not** normal: conjugating moves $s_a$ to another reflection. Dividing out by the rotations leaves a group of order $2$: *rotation* versus *reflection*, which is the **orientation** of the triangle.

## Connection to GF(3)

The **affine maps** $x\mapsto\lambda x+\mu$ of $\mathrm{GF}(3)$, with $\lambda=\pm1$ and $\mu\in\{\bar1,0,1\}$, are exactly the six symmetries above:

- $x\mapsto x+\mu$ are the rotations ($\mu=1$ is $r$);
- $x\mapsto-x-a$ are the reflections.

So the group of substitutions $x\mapsto\lambda x+\mu$ that the [[GF(3)]] page used to sort polynomials into classes **is the symmetry group of the triangle**, acting on the three field elements as vertices. Its order is $2\cdot3=6$, and the table above is its Cayley table.

**Written with bar numbers only.** Each symmetry is a pair $[\lambda,\mu]$ of balanced digits, $\lambda\in\{\bar1,1\}$ and $\mu\in\{\bar1,0,1\}$, meaning $x\mapsto\lambda x+\mu$ in $\mathrm{GF}(3)$. So $e=[1,0]$, $r=[1,1]$, $r^2=[1,\bar1]$, $s_0=[\bar1,0]$, $s_1=[\bar1,\bar1]$, $s_{\bar1}=[\bar1,1]$. The product is $[\lambda,\mu]\,[\lambda',\mu']=[\lambda\lambda',\ \lambda\mu'+\mu]$ (the right factor first), with the arithmetic of $\mathrm{GF}(3)$. For example $r\,s_0=[1,1][\bar1,0]=[\bar1,1]=s_{\bar1}$ and $s_0\,r=[\bar1,0][1,1]=[\bar1,\bar1]=s_1$. The letters $e,r,s$ are a convenience: the triangle's group **is** the affine group of the field $\mathrm{GF}(3)$, the mod-3 numbers with a sign.

## In coordinates

Put the center at the origin and the vertices at $(1,0)$, $\left(-\tfrac12,\tfrac{\sqrt3}2\right)$, $\left(-\tfrac12,-\tfrac{\sqrt3}2\right)$ for $x=0,1,\bar1$. All coordinates lie in $\mathbb K$ ([[Constructible Numbers]]). The symmetries are the $2\times2$ matrices

$$r=\begin{pmatrix}-\tfrac12&-\tfrac{\sqrt3}2\\\tfrac{\sqrt3}2&-\tfrac12\end{pmatrix},\ \ r^2=\begin{pmatrix}-\tfrac12&\tfrac{\sqrt3}2\\-\tfrac{\sqrt3}2&-\tfrac12\end{pmatrix},\ \ s_0=\begin{pmatrix}1&0\\0&-1\end{pmatrix},$$
$$s_1=\begin{pmatrix}-\tfrac12&-\tfrac{\sqrt3}2\\-\tfrac{\sqrt3}2&\tfrac12\end{pmatrix},\ \ s_{\bar1}=\begin{pmatrix}-\tfrac12&\tfrac{\sqrt3}2\\\tfrac{\sqrt3}2&\tfrac12\end{pmatrix}.$$

I checked that matrix multiplication reproduces the Cayley table and that each matrix moves the three vertices as described.

**Slopes.** A rotation has the form $\dfrac1\ell\begin{pmatrix}1&-m\\m&1\end{pmatrix}$ for a wedge of slope $m$ and characteristic length $\ell$ ([[Slope]], [[Characteristic Length]]). A third of a turn is the wedge with $(m,\ell)=(-\sqrt3,-2)$ (the interior wedge of a regular hexagon), which gives exactly the matrix $r$. In the slope group of [[Sum of Slopes]], $-\sqrt3\oplus-\sqrt3=\sqrt3$ and $\sqrt3\oplus\sqrt3=-\sqrt3$, and $-\sqrt3\oplus\sqrt3=0$: the slopes $\{0,\sqrt3,-\sqrt3\}$ form a cyclic group of order $3$ under $\oplus$, the rotation subgroup. The rotation group is therefore inside $\mathbb K\cup\{\infty\}$ with $\oplus$.
