---
title: Exact Slopes
type: reference
status: canonical (draft)
provenance: "murphy (article: the list of exact tangent values and their forms); murphy+ai (indexing by the doubled wedge, every entry checked numerically)"
sources: "images/constructible.tex"
updated: 2026-10-08
---

# Exact Slopes

The exact slope of every wedge that is a multiple of a $\tfrac1{120}$ of a turn, and of its repeated halves, up to an eighth of a turn. Every value is in $\mathbb K$ ([[Constructible Numbers]]), and each is a nest built by [[Nested Radicals]]. No value on this page is approximated; the decimals are only a check.

## The rule

For a wedge $w$, let $K=k_{2w}=2/\ell_{2w}$, the doubled reciprocal length of **twice** the wedge. Then

$$m_w=\sqrt{\frac{2-K}{2+K}}.$$

Equivalently, $w$ is the half of the wedge $2w$, and [[Nested Radicals]] gives its slope from $K$. The seeds are $\sqrt2,\ \sqrt3,\ \varphi,\ \Phi$ and the quartet $\Xi,\xi,\Upsilon,\upsilon$.

## The table

The wedge is given as a fraction of a turn. The degree column is only for readers coming from other frameworks.

| wedge (turn) | degrees (comparison) | $K=k_{2w}$ | exact slope $m_w$ | decimal |
|---|---|---|---|---|
| $1/120$ | $3^\circ$ | $\sqrt{2+\Xi}$ | nest only | 0.0524077793 |
| $1/60$ | $6^\circ$ | $\Xi$ | $\sqrt{7-2\sqrt5-2\sqrt{15-6\sqrt5}}$ | 0.1051042353 |
| $1/48$ | $7.5^\circ$ | $\sqrt{2+\sqrt3}$ | $\sqrt6-\sqrt3+\sqrt2-2=(\sqrt2-1)(\sqrt3-\sqrt2)$ | 0.1316524976 |
| $1/40$ | $9^\circ$ | $\sqrt{2+\varphi}$ | $1+\sqrt5-\sqrt{5+2\sqrt5}$ | 0.1583844403 |
| $1/32$ | $11.25^\circ$ | $\sqrt{2+\sqrt2}$ | $-1-\sqrt2+\sqrt{4+2\sqrt2}$ | 0.1989123674 |
| $1/30$ | $12^\circ$ | $\xi$ | $\sqrt{23-10\sqrt5-2\sqrt{3(85-38\sqrt5)}}$ | 0.2125565617 |
| $1/24$ | $15^\circ$ | $\sqrt3$ | $2-\sqrt3$ | 0.2679491924 |
| $1/20$ | $18^\circ$ | $\varphi$ | $\sqrt{1-\tfrac2{\sqrt5}}=\tfrac{\sqrt{25-10\sqrt5}}5$ | 0.3249196962 |
| $7/120$ | $21^\circ$ | $\sqrt{2+\upsilon}$ | nest only | 0.3838640350 |
| $1/16$ | $22.5^\circ$ | $\sqrt2$ | $\sqrt2-1$ | 0.4142135624 |
| $1/15$ | $24^\circ$ | $\Upsilon$ | $\sqrt{23+10\sqrt5-2\sqrt{3(85+38\sqrt5)}}$ | 0.4452286853 |
| $3/40$ | $27^\circ$ | $\sqrt{2-\Phi}$ | $-1+\sqrt5-\sqrt{5-2\sqrt5}$ | 0.5095254495 |
| $1/12$ | $30^\circ$ | $1$ | $\tfrac1{\sqrt3}=\tfrac{\sqrt3}3$ | 0.5773502692 |
| $11/120$ | $33^\circ$ | $\sqrt{2-\Upsilon}$ | nest only | 0.6494075932 |
| $3/32$ | $33.75^\circ$ | $\sqrt{2-\sqrt2}$ | nest only | 0.6681786379 |
| $1/10$ | $36^\circ$ | $\Phi$ | $\sqrt{5-2\sqrt5}$ | 0.7265425280 |
| $5/48$ | $37.5^\circ$ | $\sqrt{2-\sqrt3}$ | $\sqrt6+\sqrt3-\sqrt2-2=(\sqrt2+1)(\sqrt3-\sqrt2)$ | 0.7673269880 |
| $13/120$ | $39^\circ$ | $\sqrt{2-\xi}$ | $\dfrac{\sqrt{4-\Phi^2}-1}{\sqrt3-\Phi}$ | 0.8097840332 |
| $7/60$ | $42^\circ$ | $\upsilon$ | $\sqrt{7+2\sqrt5-2\sqrt{3(5+2\sqrt5)}}$ | 0.9004040443 |
| $1/8$ | $45^\circ$ | $0$ | $1$ | 1.0000000000 |

Every wedge between an eighth and a quarter of a turn has a slope that is the **reciprocal** of the slope of its complement in a right angle. A wedge past a quarter turn has a negative slope. Any wedge in the table can be halved again by [[Nested Radicals]].

## Notes

- The twenty wedges are the fifteen multiples of $\tfrac1{120}$ of a turn up to an eighth (the $3^\circ$ steps), plus five halved wedges: $\tfrac1{48},\ \tfrac1{32},\ \tfrac1{16},\ \tfrac3{32},\ \tfrac5{48}$.
- Forms for $3^\circ$, $21^\circ$, $33^\circ$ and $33.75^\circ$ are given only as nests. Each also has a closed form with radicals, but it is long.
- The slope $\sqrt2-1$ of a sixteenth of a turn is the reciprocal of the silver ratio $1+\sqrt2$ ([[Metallic Means]]), and $2-\sqrt3$ for a twenty-fourth is the reciprocal of $2+\sqrt3$.
