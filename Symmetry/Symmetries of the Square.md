---
title: Symmetries of the Square
type: concept
status: canonical (draft)
provenance: "murphy+ai (Murphy's brief: the symmetries of the square as a finite object; every table, subgroup and class below was computed and checked by exhaustive check)"
sources: "[[Groups]]"
updated: 2026-10-08
---

# Symmetries of the Square

A **symmetry** of the square is a distance-preserving map of the plane onto itself (an *isometry*) that carries the square onto itself. There are exactly **eight**, so they form a group of order $8$ ([[Groups]]), the **dihedral group** $D_4$. Compare [[Symmetries of the Equilateral Triangle]].

## The eight symmetries

Number the vertices $0,1,2,3$ counterclockwise, as the elements of $\mathbb Z/4$.

- **$e$**: do nothing.
- **$r$**: a quarter turn counterclockwise: vertex $x$ goes to $x+1$ (mod $4$). **$r^2$** is a half turn and **$r^3$** a three-quarter turn; $r^4=e$.
- **$s_c$** for $c=0,1,2,3$: the reflection $x\mapsto c-x$ (mod $4$).
  - $s_0$ and $s_2$ are the reflections in the two **diagonals**: $s_0$ fixes vertices $0$ and $2$, and $s_2$ fixes $1$ and $3$.
  - $s_1$ and $s_3$ are the reflections in the two lines through the **midpoints of opposite sides**: $s_1$ swaps $0\leftrightarrow1$ and $2\leftrightarrow3$, and $s_3$ swaps $0\leftrightarrow3$ and $1\leftrightarrow2$. They fix no vertex.

The four **rotations** can be done by sliding the square around in the plane. The four **reflections** need the square to be flipped over, through the third dimension, exactly as for [[Symmetries of the Equilateral Triangle]]; rotations have determinant $+1$ and reflections $-1$.

**Only eight of the $24$ permutations of the vertices occur.** A symmetry preserves distances, so it must keep the diagonals $\{0,2\}$ and $\{1,3\}$ together: $D_4$ is exactly the set of permutations of the vertices that preserve the diagonal pairing. This is unlike the triangle, where every one of the $3!=6$ permutations occurred.

## The Cayley table

The product $ab$ means *do $b$ first, then $a$*.

| | $e$ | $r$ | $r^2$ | $r^3$ | $s_0$ | $s_1$ | $s_2$ | $s_3$ |
|---|---|---|---|---|---|---|---|---|
| **$e$** | $e$ | $r$ | $r^2$ | $r^3$ | $s_0$ | $s_1$ | $s_2$ | $s_3$ |
| **$r$** | $r$ | $r^2$ | $r^3$ | $e$ | $s_1$ | $s_2$ | $s_3$ | $s_0$ |
| **$r^2$** | $r^2$ | $r^3$ | $e$ | $r$ | $s_2$ | $s_3$ | $s_0$ | $s_1$ |
| **$r^3$** | $r^3$ | $e$ | $r$ | $r^2$ | $s_3$ | $s_0$ | $s_1$ | $s_2$ |
| **$s_0$** | $s_0$ | $s_3$ | $s_2$ | $s_1$ | $e$ | $r^3$ | $r^2$ | $r$ |
| **$s_1$** | $s_1$ | $s_0$ | $s_3$ | $s_2$ | $r$ | $e$ | $r^3$ | $r^2$ |
| **$s_2$** | $s_2$ | $s_1$ | $s_0$ | $s_3$ | $r^2$ | $r$ | $e$ | $r^3$ |
| **$s_3$** | $s_3$ | $s_2$ | $s_1$ | $s_0$ | $r^3$ | $r^2$ | $r$ | $e$ |

- **Not abelian:** $r\,s_0=s_1$ but $s_0\,r=s_3$.
- **The relation** $s\,r\,s=r^{-1}$, with $r^4=e$ and $s^2=e$, describes the whole group.
- Every row and column holds each element once.

## As a mod with a sign

$D_4$ is not itself a mod, since it is not abelian, but it is built from one. Write each symmetry as a pair $[\lambda,\mu]$ meaning the map $x\mapsto\lambda x+\mu$ on the vertices $\mathbb Z/4$, with $\lambda=\pm1$ (written $1$ or $\bar1$) and $\mu\in\mathbb Z/4$:

- rotations: $r^k=[1,k]$;
- reflections: $s_c=[\bar1,c]$.

The product is $[\lambda,\mu]\,[\lambda',\mu']=[\lambda\lambda',\ \lambda\mu'+\mu]$ (the right factor first, mod $4$). So the group notation with $e,r,s$ is a convenience: every symmetry is a **mod-4 clock reading, run forwards or backwards, shifted by $\mu$**. For example $r\,s_0=[1,1][\bar1,0]=[\bar1,1]=s_1$ and $s_0\,r=[\bar1,0][1,1]=[\bar1,\bar1]=[\bar1,3]=s_3$. The rotations are the pairs with $\lambda=1$: a copy of $\mathbb Z/4$ with the sign dropped. The elements of $\mathbb Z/4$ can be written in balanced digits $\bar1,0,1,2$.

This is the **affine group of the ring** $\mathbb Z/4$: the units of $\mathbb Z/4$ are $\{1,\bar1\}$ (the sign), and $x\mapsto\lambda x+\mu$ is every invertible affine map. In general the symmetries of the regular $n$-gon are $\{x\mapsto\pm x+\mu\}$ on $\mathbb Z/n$.

## On a card: eight letters for eight symmetries

*Reconstruction of Murphy's classroom activity; the naming is mine and may differ from his.* Take a cardboard square. Label the front corners $A,B,C,D$ counterclockwise, and the back corners $E,F,G,H$ with $E$ behind $A$, $F$ behind $B$, and so on. Every one of the eight symmetries can be **named by the corner that ends up in the place where $A$ began**, with the face that is then showing:

| name | $A$ | $B$ | $C$ | $D$ | $E$ | $F$ | $G$ | $H$ |
|---|---|---|---|---|---|---|---|---|
| symmetry | $e$ | $r^3$ | $r^2$ | $r$ | $s_0$ | $s_1$ | $s_2$ | $s_3$ |

($B$ is a quarter turn clockwise, so that $B$ comes to $A$'s place; $E$ is the flip about the diagonal through $A$ and $C$.) With the product convention above ($ab$ means do $b$ first), the table in letters is:

| | A | B | C | D | E | F | G | H |
|---|---|---|---|---|---|---|---|---|
| **A** | A | B | C | D | E | F | G | H |
| **B** | B | C | D | A | H | E | F | G |
| **C** | C | D | A | B | G | H | E | F |
| **D** | D | A | B | C | F | G | H | E |
| **E** | E | F | G | H | A | B | C | D |
| **F** | F | G | H | E | D | A | B | C |
| **G** | G | H | E | F | C | D | A | B |
| **H** | H | E | F | G | B | C | D | A |

It agrees with the table above under the dictionary: $D\cdot E=r\,s_0=s_1=F$ but $E\cdot D=s_0\,r=s_3=H$, so the group is not abelian. Associativity was checked on all $512$ triples.

**Nested products.** $A(B(C(D(E(F(G(H)))))))$ is evaluated from the inside out: $G\cdot H=E$, then $F\cdot E=D$, and so on; with this naming the answer is $A$, and the left-to-right grouping $((((((A\,B)C)D)E)F)G)H$ gives the same $A$. That the grouping does not matter is **associativity**, met as a fact about a piece of cardboard before it is named.

## Element orders

| order | elements | how many |
|---|---|---|
| $1$ | $e$ | 1 |
| $2$ | $r^2,\ s_0,s_1,s_2,s_3$ | 5 |
| $4$ | $r,\ r^3$ | 2 |

No element has order $8$, so the group is not cyclic. **Five** elements of order $2$: this tells it apart from the quaternion group (below).

## Subgroups

There are **ten** subgroups (checked by trying every subset): $\{e\}$; five of order $2$ ($\{e,r^2\}$ and the four $\{e,s_c\}$); three of order $4$; and the whole group. Their orders divide $8$, as Lagrange's theorem says.

The three subgroups of order $4$ are the two groups of order $4$ from [[Groups]]:

- **The rotations** $\{e,r,r^2,r^3\}$: cyclic, $\cong\mathbb Z/4$.
- **The diagonal Klein group** $\{e,r^2,s_0,s_2\}$ and **the side Klein group** $\{e,r^2,s_1,s_3\}$: both $\cong$ the Klein four-group, since every element has order $2$.

So $D_4$ contains **both** groups of order $4$, and the Klein group twice.

## Conjugacy classes, center and normal subgroups

The conjugacy classes are

$$\{e\},\qquad\{r^2\},\qquad\{r,r^3\},\qquad\{s_0,s_2\},\qquad\{s_1,s_3\},$$

and $8=1+1+2+2+2$. The two diagonal reflections are conjugate to each other, and so are the two side reflections, but a diagonal reflection is never conjugate to a side reflection. The **center** is $\{e,r^2\}$: the half turn commutes with everything.

**Six** subgroups are normal, because each is a union of conjugacy classes: $\{e\}$, the center $\{e,r^2\}$, the rotations, the two Klein groups, and the whole group. The four subgroups $\{e,s_c\}$ of order $2$ are not normal.

**Quotient.** Dividing out the center $\{e,r^2\}$ leaves four cosets, $\{e,r^2\},\{r,r^3\},\{s_0,s_2\},\{s_1,s_3\}$, and each squares to the identity coset: the quotient is the **Klein four-group**.

## The other nonabelian group of order 8

The only other nonabelian group of order $8$ is the **quaternion group** $Q_8=\{\pm1,\pm i,\pm j,\pm k\}$ of the fiat numbers of [[Fiat Numbers]]. It has **one** element of order $2$ ($-1$) and **six** of order $4$ (checked), where $D_4$ has five and two. So they are different groups, even though both have order $8$ and both are nonabelian.

## In coordinates

Place the vertices at $(1,0),(0,1),(-1,0),(0,-1)$ for $x=0,1,2,3$. The eight symmetries are exactly the $2\times2$ matrices with entries $0,\pm1$ and one nonzero entry in each row and column (the *signed permutation matrices*; $2^2\cdot2!=8$):

$$r=\begin{pmatrix}0&-1\\1&0\end{pmatrix},\quad r^2=\begin{pmatrix}-1&0\\0&-1\end{pmatrix},\quad r^3=\begin{pmatrix}0&1\\-1&0\end{pmatrix},$$
$$s_0=\begin{pmatrix}1&0\\0&-1\end{pmatrix},\quad s_2=\begin{pmatrix}-1&0\\0&1\end{pmatrix},\quad s_1=\begin{pmatrix}0&1\\1&0\end{pmatrix},\quad s_3=\begin{pmatrix}0&-1\\-1&0\end{pmatrix}.$$

All entries are integers, so unlike the triangle (which needs $\sqrt3$) the square's symmetries live in $\mathbb Z$. I checked that matrix multiplication reproduces the Cayley table and that each matrix moves the four vertices as described.

**Slopes.** The four reflection lines have slopes $0,\ \infty,\ 1,\ -1$ (the axes and the two diagonals, $s_0$: $0$; $s_2$: $\infty$; $s_1$: $1$; $s_3$: $-1$). Under the $\oplus$ of [[Sum of Slopes]] these four slopes form a **cyclic group of order $4$**: $1\oplus1=\infty$, $1\oplus\infty=-1$, $1\oplus-1=0$, with $1$ as generator ([[Extended Constructible Numbers]]). Adding the slope $1$ turns a reflection line by an eighth of a turn.

A quarter turn has slope $\infty$ ($m=\ell=\infty$ with $m/\ell=1$, $1/\ell=0$, so $\tfrac1\ell\begin{pmatrix}1&-m\\m&1\end{pmatrix}$ becomes the matrix $r$). But a slope forgets the half turn, so under $\oplus$ the four rotations collapse onto $\{0,\infty\}$: the square's rotation group is **not** a subgroup of the slope group, though its reflection lines are.
