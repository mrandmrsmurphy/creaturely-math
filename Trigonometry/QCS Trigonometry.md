---
title: QCS Trigonometry
type: method
status: canonical
provenance: murphy (the case and the form of the sides); murphy+ai (corrected radicand, reduction to SQA, count, examples)
sources: "Murphy's Constructible Trigonometry textbook (2026)"
updated: 2026-10-08
---

# QCS Trigonometry

**QCS** is *area, circumradius, side*. **Given** the area $Q$, the circumradius $R$, and a side $a$. **Find** the other two sides, the wedges and the inradius.

This is an **ambiguous case**: up to two triangles. The two scale quantities $Q$ and $R$ and one side $a$ fix the shape, with one choice left over.

## The wedge $A$

By the [[Law of the Circumdiameter]], $\dfrac{m_A}{\ell_A}=\dfrac a{2R}$, so the wedge opposite $a$ is known up to acute versus obtuse. With $\alpha=\pm\sqrt{4R^2-a^2}$ ($\alpha>0$ for $A$ acute, $\alpha<0$ for $A$ obtuse):

$$m_A=\frac a\alpha,\qquad \ell_A=\frac{2R}\alpha.$$

Existence needs $a\le2R$.

## Each sign is an SQA triangle

With $a$, $Q$ and $A$ known, the data are those of [[SQA Trigonometry]], which gives one triangle when $Q\le a^2/(4\,m_{A/2})$ and none above. Since $m_{A/2}=\dfrac{a}{2R+\alpha}$, that bound is

$$Q\le Q_{\max}=\frac{a\,(2R+\alpha)}4.$$

The acute bound is larger than the obtuse one. So:

- $Q\le\dfrac{a(2R-\sqrt{4R^2-a^2})}4$: **two triangles**, $A$ acute and $A$ obtuse.
- between that and $\dfrac{a(2R+\sqrt{4R^2-a^2})}4$: **one triangle**, $A$ acute.
- above: **none**.

At the obtuse bound the obtuse triangle is isosceles.

## The other two sides

$Q=\dfrac{abc}{4R}$ gives $bc=\dfrac{4RQ}a$, and the [[Law of Lengths]] gives $b^2+c^2=a^2+\dfrac{4Q}{m_A}=a^2+\dfrac{4Q\alpha}a$. So $b^2$ and $c^2$ are the two roots of a quadratic, and the discriminant simplifies (using $\alpha^2-4R^2=-a^2$) to $a^4+8aQ\alpha-16Q^2$:

$$b^2,\ c^2=\frac{a^3+4Q\alpha\pm a\sqrt{a^4+8aQ\alpha-16Q^2}}{2a},$$

and $b$, $c$ are the square roots. Equivalently, from [[SQA Trigonometry]],

$$b,c=u\pm v,\qquad u^2=\frac{a^2}4+\frac{Q\,(2R+\alpha)}a,\qquad v^2=\frac{a^2}4-\frac{Q\,(2R-\alpha)}a.$$

## The wedges

The wedge $A$ is above. The other two are the roots of a quadratic: by the [[Law of Slopes]] and the area, $m_B+m_C=\dfrac{a^2}{2Q-a\alpha}$ and $m_Bm_C=\dfrac{2Q}{2Q-a\alpha}$. So, directly from $Q$, $R$, $a$,

$$m_B,\ m_C=\frac{a^2\pm\sqrt{a^4+8aQ\alpha-16Q^2}}{2\,(2Q-a\alpha)},\qquad \alpha=\pm\sqrt{4R^2-a^2}.$$

The radicand is the same one that gives $b$ and $c$. The larger sign belongs to the wedge opposite the larger of $b,c$. If $2Q=a\alpha$ one of them is a right angle (slope $\infty$, [[Extended Constructible Numbers]]) and the other has slope $1/m_A$. Each is positive for an acute wedge and negative for an obtuse one.

Equivalently, from the sides found above and [[SSS Trigonometry]]: $m_B=\dfrac{4Q}{a^2+c^2-b^2}$, $m_C=\dfrac{4Q}{a^2+b^2-c^2}$.

## The inradius

$r=\dfrac{2Q}{a+b+c}$. The sum $b+c$ is known without finding $b,c$ separately: $(b+c)^2=b^2+c^2+2bc=a^2+\dfrac{4Q\alpha}a+\dfrac{8RQ}a$, so

$$r=\frac{2Q}{a+\sqrt{a^2+\dfrac{4Q\,(2R+\alpha)}a}}.$$

Equivalently, with $u$ as above (so $b+c=2u$), $r=\dfrac{a\,(2u-a)}{2\,(2R+\alpha)}$, which is the SQA inradius $\dfrac a2\bigl(\sqrt{4Q\,t/a^2+t^2}-t\bigr)$ with $t=m_{A/2}=\dfrac a{2R+\alpha}$. Also $r=\dfrac{abc}{2R(a+b+c)}$.

## Exactness

Two square roots, $\sqrt{4R^2-a^2}$ and the discriminant, then a third for $b,c$. If the data are in $\mathbb K$, so is everything. No cubic.

## Example: $R=\tfrac{65}8$, $a=13$, $Q=84$ (one triangle)

$\alpha=\pm\dfrac{39}4$. The bounds: acute $Q_{\max}=\dfrac{13(\frac{65}4+\frac{39}4)}4=\dfrac{169}2=84.5$, obtuse $Q_{\max}=\dfrac{13(\frac{65}4-\frac{39}4)}4=\dfrac{169}8=21.1$.

- **$A$ acute:** $b^2,c^2=\dfrac{2197+3276\pm13\cdot29}{26}=225,\ 196$, so $b,c=15,14$. The $13,14,15$ triangle ([[SSS Trigonometry]]), $r=\dfrac{168}{13+\sqrt{169+672}}=\dfrac{168}{42}=4$. Its wedges: $2Q-a\alpha=168-\dfrac{507}4=\dfrac{165}4$, so $m_B,m_C=\dfrac{169\pm29}{165/2}=\dfrac{12}5,\ \dfrac{56}{33}$.
- **$A$ obtuse:** $84>21.1$, so none.

## Example: $R=\tfrac{65}8$, $a=13$, $Q=\tfrac{252}{25}$ (two triangles)

Both bounds exceed $Q=10.08$:

- **$A$ acute:** $b^2,c^2=\dfrac{2590.12\pm13\sqrt{37156.42}}{26}=196,\ 3.24$, so $b,c=14,\ \dfrac95$.
- **$A$ obtuse:** $b^2,c^2\approx134.0,\ 4.74$, so $b,c\approx11.577,\ 2.177$.

Two different triangles with the same $a$, $Q$ and $R$.

## Example: $R=1$, $a=\sqrt3$, $Q=\dfrac{\sqrt3}4$

$\sqrt{4R^2-a^2}=1$.

- **$A$ acute** ($m_A=\sqrt3$): $\sqrt{a^4+8aQ-16Q^2}=2\sqrt3$, so $b^2,c^2=2\pm\sqrt3$ and $b,c=\dfrac{\sqrt6\pm\sqrt2}2\approx1.932,\ 0.518$.
- **$A$ obtuse** ($m_A=-\sqrt3$, the interior wedge of a regular hexagon): the radicand is $0$, so $b^2=c^2=1$: the isosceles $1,1,\sqrt3$ triangle, at its maximum area.
