---
title: SQA Trigonometry
type: method
status: canonical
provenance: murphy (formulas and method); murphy+ai (derivations, existence condition, examples)
sources: "Murphy's Constructible Trigonometry textbook (2026)"
updated: 2026-10-08
---

# SQA Trigonometry

**Given** a side $a$, the area $Q$, and the wedge $A$ **opposite** $a$, so $a$, $Q$, $m_A,\ell_A$ are known ([[Slope]], [[Characteristic Length]]). **Find** the other two sides $b,c$ (the sides around $A$), the other two wedges, the inradius and the circumradius.

This is **one triangle**, up to mirror image: the formulas give $b$ and $c$ as an unordered pair. It is not an ambiguous case like [[SSA Trigonometry]], but it has a **maximum area**.

## The existence condition

For a given $a$ and $A$, the area is greatest for the isosceles triangle, $b=c$:

$$Q\le Q_{\max}=\frac{a^2(\ell_A+1)}{4\,m_A}=\frac{a^2}{4\,m_{A/2}}.$$

Beyond $Q_{\max}$ there is no triangle.

## The missing sides

The [[Law of SAS Area]] gives $bc=\dfrac{2Q\,\ell_A}{m_A}$. The [[Law of Lengths]], $a^2=b^2+c^2-\dfrac{2bc}{\ell_A}$, gives $b^2+c^2=a^2+\dfrac{4Q}{m_A}$. Then

$$(b\pm c)^2=a^2+\frac{4Q}{m_A}(1\pm\ell_A),$$

so, with
$$u=\sqrt{\frac{a^2}4+\frac{Q}{m_A}(1+\ell_A)},\qquad v=\sqrt{\frac{a^2}4+\frac{Q}{m_A}(1-\ell_A)},$$
we have $b+c=2u$, $b-c=2v$, and

$$b,\,c=u\pm v.$$

$v$ is real exactly when $Q\le Q_{\max}$, and $v=0$ is the isosceles triangle.

## The missing wedges

With $D=2Q\,m_A-a^2$. The wedges $B,C$ lie at the ends of $a$, and by the [[Law of Slopes]] and the area (as in [[ASA Trigonometry]]) their sum $s=m_B+m_C$ and product $p=m_Bm_C$ satisfy $s=m_A(p-1)$ and $2Q\,s=a^2p$. So $p=\dfrac{2Q\,m_A}{D}$, $s=\dfrac{a^2m_A}{D}$, and $m_B,m_C$ are the roots of $x^2-sx+p=0$:

$$m_{B,C}=\frac{a^2m_A\pm\sqrt{m_A\bigl(a^4m_A-8Q\,D\bigr)}}{2D}.$$

The radicand equals $16\,m_A^2\,(Q_{\max}-Q)(Q-Q_{\min})$ with $Q_{\min}<0$, so the wedges are real exactly when $Q\le Q_{\max}$.

**$D=0$.** When $2Q\,m_A=a^2$, one of $B,C$ is a right angle: read the triangle off directly, where the other wedge has slope $1/m_A$ ([[Extended Constructible Numbers]]).

## The inradius

Let $t=m_{A/2}=\dfrac{m_A}{\ell_A+1}$ ([[Characteristic Length#Half a wedge]]). The incircle meets the sides at $A$ at distance $s_*-a$ from $A$, where $s_*=\tfrac12(a+b+c)$, so $r=(s_*-a)\,t$. With $Q=r\,s_*$: $r=\bigl(\tfrac Qr-a\bigr)t$, i.e. $r^2+a\,t\,r-Q\,t=0$:

$$r=\frac a2\left(\sqrt{\frac{4Q\,m_{A/2}}{a^2}+m_{A/2}^2}-m_{A/2}\right).$$

The half-wedge $A/2$ is acute, so there are no sign cases, and $r$ needs only $a$, $Q$ and $A$.

## The circumradius

The [[Law of the Circumdiameter]]:

$$R=\frac{a\,\ell_A}{2\,m_A}.$$

## Right angles

If $A$ is a right angle, $m_A=\infty$ and the formulas do not apply: $a$ is the hypotenuse and $b,c$ are read off.

## Exactness

$u$, $v$, the wedge radical and $r$ are one square root each of quantities built from $a,Q,m_A,\ell_A$ by field operations, so if the data are in $\mathbb K$ so is everything.

## Example: $a=13$, $Q=84$, $m_A=\tfrac43$

$\ell_A=\tfrac53$, $Q_{\max}=\dfrac{169\cdot\frac83}{4\cdot\frac43}=\dfrac{169}2=84.5$.

- $u=\sqrt{\dfrac{169}4+84\cdot\dfrac{8/3}{4/3}}=\sqrt{\dfrac{169}4+168}=\dfrac{29}2$, $\ v=\sqrt{\dfrac{169}4-42}=\dfrac12$, so $b,c=15,14$.
- $D=224-169=55$ and the radical is $\sqrt{\tfrac43\bigl(\tfrac{114244}3-36960\bigr)}=\dfrac{116}3$, so $m_{B,C}=\dfrac{\frac{676}3\pm\frac{116}3}{110}=\dfrac{12}5,\ \dfrac{56}{33}$.
- $r=\dfrac{13}2\left(\dfrac{29}{26}-\dfrac12\right)=4$. $\ R=\dfrac{13\cdot\frac53}{2\cdot\frac43}=\dfrac{65}8$.

The $13,14,15$ triangle ([[SSS Trigonometry]]). Nearly isosceles at $A$, so $Q$ is close to $Q_{\max}=84.5$.

## Example: the isosceles limit

$a=\sqrt3$, $Q=\dfrac{\sqrt3}4$, $m_A=-\sqrt3$, $\ell_A=-2$ (the interior wedge of a regular hexagon). $Q_{\max}=\dfrac{3\cdot(-1)}{4\cdot(-\sqrt3)}=\dfrac{\sqrt3}4=Q$, so this is the isosceles case: $v=0$, $u=1$, $b=c=1$, both wedges $\dfrac1{\sqrt3}$. $r$: $t=\sqrt3$, $\ r=\dfrac{\sqrt3}2(2-\sqrt3)=\dfrac{2\sqrt3-3}2$. $\ R=\dfrac{\sqrt3\cdot(-2)}{2\cdot(-\sqrt3)}=1$.

## Example: no triangle

$a=13$, $m_A=\tfrac43$, $Q=100>Q_{\max}=84.5$. $v^2=\dfrac{169}4-\dfrac{100\cdot\frac23}{4/3}<0$: no triangle.
