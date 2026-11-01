---
title: Law of the Circumdiameter
type: law
status: canonical
provenance: murphy+ai (statement and method Murphy's; proof text drafted by AI)
sources: "[[SRC Constructible Trigonometry Textbook (md)]]"
updated: 2026-10-07
---

# Law of the Circumdiameter

In triangle $ABC$ with sides $a,b,c$ opposite the wedges $A,B,C$,

$$a\,\frac{\ell_A}{m_A}=b\,\frac{\ell_B}{m_B}=c\,\frac{\ell_C}{m_C}=2R,$$

where $R$ is the circumradius, so $2R$ is the **circumdiameter**. The three terms are equal, and each is equal to the circumdiameter. (In other frameworks this is the Law of Sines.)

## Derivation

**Step 1 — drop an altitude.** Drop the altitude $h$ from $C$ to the line $AB$. It splits the triangle into two right triangles.

- At $A$, the right triangle has hypotenuse $b$ and wedge $A$. By [[Slope]] and [[Characteristic Length]], hypotenuse : run : rise $=\ell_A : 1 : m_A$, so $h=b\,\dfrac{m_A}{\ell_A}$.
- At $B$, likewise, hypotenuse $a$ and wedge $B$ give $h=a\,\dfrac{m_B}{\ell_B}$.

Equate the two values of $h$: $b\,\dfrac{m_A}{\ell_A}=a\,\dfrac{m_B}{\ell_B}$. Cross-multiplying and dividing by $m_Am_B$,

$$a\,\frac{\ell_A}{m_A}=b\,\frac{\ell_B}{m_B}.$$

Dropping the altitude from $A$ or $B$ instead gives the other equalities.

**Step 2 — the altitude is unnecessary.** The $h$ cancelled: the common value does not depend on it, nor on any choice of base. So it must be a property of the triangle itself. It is the circumdiameter.

**Step 3 — each term is $2R$.** Draw the circumcircle. Take the diameter $BB'$ through $B$. The wedge at $B'$ over the chord $BC$ is congruent to the wedge $A$ (wedges on the same chord are equal, Euclid III.21), and the triangle $BCB'$ has a right angle at $C$ (Thales). In that right triangle the hypotenuse is $2R$, the side opposite wedge $A$ is $a$, and the ratio of the opposite side to the hypotenuse is $m_A/\ell_A$. So

$$a=2R\,\frac{m_A}{\ell_A},\qquad\text{i.e.}\qquad a\,\frac{\ell_A}{m_A}=2R.$$

The same argument at $B$ and $C$ finishes the law.

## Remarks

- **Obtuse wedges.** The supplement of a wedge has slope $-m$ and characteristic length $-\ell$, so $m/\ell$ is the same for both. That is why Step 3 holds when $A$ is obtuse and $B'$ lies on the other arc, provided $\ell$ is signed.
- **Right angle.** If $A$ is a right angle then $m_A=\infty$, and $\ell_A\div m_A=\infty\div\infty=1$ in $\mathbb K^+$ ([[Extended Constructible Numbers]]), so $a=2R$: the hypotenuse is a diameter.
- **Checks.** The $3$-$4$-$5$ triangle, $a=3$ opposite $m_A=\tfrac34,\ \ell_A=\tfrac54$: $3\cdot\tfrac54\div\tfrac34=5=2R$ ✔. The triangle with sides $1,1,\sqrt3$ and $C$ the interior wedge of a regular hexagon ($m_C=-\sqrt3,\ \ell_C=-2$): $\sqrt3\cdot(-2)\div(-\sqrt3)=2=2R$ ✔.
- **Exactness.** When the data are constructible, $2R=a\,\ell_A/m_A$ is built from field operations in $\mathbb K$, so the circumdiameter (and $R$) lie in $\mathbb K$: no approximation is involved.
- This is called the Law of Sines in other frameworks
