---
title: Heron's Formula
type: law
status: canonical
provenance: murphy+ai (statement Murphy's; derivation drafted by AI from the Law of Lengths and the Law of SAS Area)
sources: "[[Law of Lengths]], [[Law of SAS Area]]"
updated: 2026-10-07
---

# Heron's Formula

For a triangle with sides $a,b,c$ and semi-perimeter $s=\tfrac12(a+b+c)$, the area is

$$Q=\sqrt{s(s-a)(s-b)(s-c)}.$$

## Derivation

Start from the [[Law of SAS Area]], $Q=\tfrac12ab\,\dfrac{m_C}{\ell_C}$. Since $\ell_C^2=1+m_C^2$ and $m_C/\ell_C>0$ ([[Characteristic Length]]),
$$\frac{m_C}{\ell_C}=\sqrt{1-\frac1{\ell_C^2}}.$$
By the [[Law of Lengths]], $\dfrac1{\ell_C}=\dfrac{a^2+b^2-c^2}{2ab}$. So
$$Q=\frac12ab\sqrt{1-\left(\frac{a^2+b^2-c^2}{2ab}\right)^2}=\frac14\sqrt{4a^2b^2-(a^2+b^2-c^2)^2}.$$
The radicand is a difference of squares:
$$\bigl(2ab-a^2-b^2+c^2\bigr)\bigl(2ab+a^2+b^2-c^2\bigr)=\bigl(c^2-(a-b)^2\bigr)\bigl((a+b)^2-c^2\bigr)$$
$$=(c-a+b)(c+a-b)(a+b-c)(a+b+c).$$
With $a+b+c=2s$, $a+b-c=2(s-c)$, $a-b+c=2(s-b)$, $-a+b+c=2(s-a)$, this is $16\,s(s-a)(s-b)(s-c)$. Therefore
$$Q=\frac14\sqrt{16\,s(s-a)(s-b)(s-c)}=\sqrt{s(s-a)(s-b)(s-c)}.\qquad\blacksquare$$

## Remarks

- **Existence.** The radicand is positive exactly when each of $s-a,s-b,s-c$ is positive, i.e. when the sides satisfy the triangle inequality ([[SSS Congruence]]).
- **Exactness.** $Q$ takes one square root of a quantity built from the sides by field operations, so it lies in $\mathbb K$ when the sides do.
- **Example.** Sides $13,14,15$: $s=21$, $Q=\sqrt{21\cdot8\cdot7\cdot6}=\sqrt{7056}=84$.
