---
title: Triangle Identities
type: reference
status: canonical (draft)
provenance: "murphy (a note on the sum of reciprocals, the product, and the half-wedge versions); murphy+ai (the identities restated with right-hand sides that hold, derived from the sides, every identity checked numerically on eight triangles including obtuse ones and exactly on the 13-14-15 triangle)"
sources: "[[Law of Slopes]]"
updated: 2026-10-08
---

# Triangle Identities

Symmetric identities for the three wedges $A,B,C$ of a triangle, in slope and length, with the inradius $r$, circumradius $R$, semi-perimeter $s$ and area $Q$. They extend the [[Law of Slopes]]. Throughout, $a,b,c$ are the sides opposite $A,B,C$, and $Q=rs=\dfrac{abc}{4R}$.

## The three wedges

**The Law of Slopes.**
$$m_A+m_B+m_C=m_Am_Bm_C.$$

**Sum of reciprocals.**
$$\frac1{\ell_A}+\frac1{\ell_B}+\frac1{\ell_C}=1+\frac rR=1+\frac{4rQ}{abc}.$$

*Derivation.* By the [[Law of Lengths]], $\dfrac1{\ell_C}=\dfrac{a^2+b^2-c^2}{2ab}$, so the sum is $\dfrac{\sum_{\text{cyc}}c\,(a^2+b^2-c^2)}{2abc}$. The numerator equals $(a+b-c)(b+c-a)(c+a-b)+2abc=8(s-a)(s-b)(s-c)+2abc$, and $(s-a)(s-b)(s-c)=r^2s=rQ$ ([[Heron's Formula]]), so the sum is $1+\dfrac{4rQ}{abc}$, and $\dfrac{4Q}{abc}=\dfrac1R$.

**Product of reciprocals.**
$$\frac1{\ell_A\ell_B\ell_C}=\frac{(a^2+b^2-c^2)(b^2+c^2-a^2)(c^2+a^2-b^2)}{8a^2b^2c^2}=\frac{s^2-(2R+r)^2}{4R^2}.$$

The first form is the Law of Lengths three times. There is **no constant value** of $\ell_A\ell_B\ell_C$: it is $8$ for the equilateral triangle, infinite for a right triangle, and negative for an obtuse one.

## The three half-wedges

Write $m_{A/2}$ and so on for the half-slopes ([[Characteristic Length#Half a wedge]]). The incircle meets the sides at $A$ at the tangent length $s-a$, so
$$m_{A/2}=\frac r{s-a},\qquad m_{B/2}=\frac r{s-b},\qquad m_{C/2}=\frac r{s-c}.$$

**Pairs, product and sum of the half-slopes.**
$$m_{A/2}m_{B/2}+m_{B/2}m_{C/2}+m_{C/2}m_{A/2}=1,\qquad m_{A/2}m_{B/2}m_{C/2}=\frac rs,\qquad m_{A/2}+m_{B/2}+m_{C/2}=\frac{4R+r}s.$$

*Derivation.* The first says the three half-wedges make a right angle, the relation used on [[IAA Trigonometry]]. The second: $\dfrac{r^3}{(s-a)(s-b)(s-c)}=\dfrac{r^3}{r^2s}=\dfrac rs$. The third uses the standard identity $\sum(s-a)(s-b)=r^2+4Rr$: $r\cdot\dfrac{r^2+4Rr}{r^2s}=\dfrac{r+4R}s$.

**Half-lengths.** Since $\ell_{A/2}^2=1+m_{A/2}^2$ and $(s-a)^2+r^2=\dfrac{bc\,(s-a)}s$ (the square of the distance from $A$ to the incenter),
$$\ell_{A/2}^2=\frac{bc}{s\,(s-a)},\qquad \ell_{A/2}\,\ell_{B/2}\,\ell_{C/2}=\frac{4R}s,\qquad \frac1{\ell_{A/2}^2}+\frac1{\ell_{B/2}^2}+\frac1{\ell_{C/2}^2}=2+\frac r{2R}.$$

*Derivation.* The product of the squares is $\dfrac{(abc)^2}{s^3\cdot r^2s}=\dfrac{16R^2}{s^2}$, using $abc=4Rrs$. For the sum, $\dfrac1{\ell_{x/2}^2}=\dfrac{1+1/\ell_x}2$ (from $\ell_{x/2}^2=\dfrac{2\ell_x}{\ell_x+1}$), so the sum is $\dfrac{3+(1+r/R)}2$.

## Check: the 13-14-15 triangle

$s=21$, $Q=84$, $r=4$, $R=\tfrac{65}8$, with $\ell_A=\tfrac53$, $\ell_B=\tfrac{65}{33}$, $\ell_C=\tfrac{13}5$ and half-slopes $m_{A/2}=\tfrac12$, $m_{B/2}=\tfrac47$, $m_{C/2}=\tfrac23$. All evaluated exactly:

| identity | left | right |
|---|---|---|
| $\sum1/\ell$ | $\tfrac35+\tfrac{33}{65}+\tfrac5{13}=\tfrac{97}{65}$ | $1+\tfrac rR=1+\tfrac{32}{65}=\tfrac{97}{65}$ |
| $\prod1/\ell$ | $\tfrac35\cdot\tfrac{33}{65}\cdot\tfrac5{13}=\tfrac{99}{845}$ | $\dfrac{s^2-(2R+r)^2}{4R^2}=\tfrac{99}{845}$ |
| pairs of half-slopes | $\tfrac27+\tfrac8{21}+\tfrac13=1$ | $1$ |
| product of half-slopes | $\tfrac12\cdot\tfrac47\cdot\tfrac23=\tfrac4{21}$ | $\tfrac rs=\tfrac4{21}$ |
| sum of half-slopes | $\tfrac12+\tfrac47+\tfrac23=\tfrac{73}{42}$ | $\tfrac{4R+r}s=\tfrac{73}{42}$ |
| $\ell_{A/2}^2,\ \ell_{B/2}^2,\ \ell_{C/2}^2$ | $\tfrac54,\ \tfrac{65}{49},\ \tfrac{13}9$ | $\tfrac{bc}{s(s-a)},\dots$ |
| $\prod\ell_{x/2}^2$ | $\tfrac{4225}{1764}$ | $\tfrac{16R^2}{s^2}=\tfrac{4225}{1764}$ |
| $\sum1/\ell_{x/2}^2$ | $\tfrac{146}{65}$ | $2+\tfrac r{2R}=\tfrac{146}{65}$ |
