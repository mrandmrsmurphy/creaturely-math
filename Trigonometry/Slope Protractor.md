---
title: Slope Protractor
type: method
status: canonical (draft)
provenance: "murphy (article appendix: the idea of a square device with 60 marks per side, the additive and subtractive halves); murphy+ai (the reading rules written out, the table of top-edge marks, the resolution calculation; reconstructed from the article's text because its figure is not in the vault)"
sources: "images/constructible.tex"
updated: 2026-10-08
---

# Slope Protractor

If the slope is the basic quantity of [[Constructible Trigonometry]], a physical object needs a way to have its **slope** measured, as a protractor measures an angle. Slopes are "square" rather than rotational, so the device is a **square**, which can double as a carpenter's square if made of metal.

*[AI]* This page reconstructs the device from the article's description. The article's figure of the marked square is not in the vault, so the details below follow from the text and have not been compared with it.

## The device

![[SlopeProtractor.svg|620]]

A square of side $1$ (in any unit), with one corner at the origin $O=(0,0)$. Each side carries **$60$ equal marks**, in the manner of the Babylonian base ([[Sexagesimal]]).

Lay the object's line along the ray from the corner $O$. The ray leaves the square through the **right edge** (if its slope is at most $1$) or through the **top edge** (if its slope exceeds $1$).

- **Right edge** (additive half). A mark at height $j/60$ means the slope is $m=j/60$. Each mark is $+\tfrac1{60}$, and every six marks is $0.1$. A slope of $1$ is the top-right corner.
- **Top edge** (subtractive half). The ray meets the top edge at a point $x=1/m$. The marks are subtractive: starting from the corner marked $60/60$ (slope $1$), each mark to the left subtracts one from the **denominator**, so the mark at $x=d/60$ means $m=60/d$. The marks are evenly spaced in $x$, but not in $m$, so the "nice" slopes come at uneven places and the reader must know fractions.

| quantity | right edge | top edge |
|---|---|---|
| position | height $y=m$ | distance $x=1/m$ |
| slope $m$ | $j/60$ | $60/d$ |
| range | $0\le m\le1$ | $1\le m\le60$ |

Slopes above $60$ land between the last mark ($d=1$) and the left corner of the top edge ($d=0$), which is the slope $\infty$ (the ray runs up the left edge).

## The top edge

The marks where $d$ divides $60$ give whole-number slopes, and a few more give simple fractions:

| tick on the top edge ($x=d/60$) | slope $m=60/d$ |
|---|---|
| $60/60$ | $1$ |
| $50/60$ | $6/5$ |
| $48/60$ | $5/4$ |
| $45/60$ | $4/3$ |
| $40/60$ | $3/2$ |
| $30/60$ | $2$ |
| $20/60$ | $3$ |
| $15/60$ | $4$ |
| $12/60$ | $5$ |
| $10/60$ | $6$ |
| $6/60$ | $10$ |
| $5/60$ | $12$ |
| $4/60$ | $15$ |
| $3/60$ | $20$ |
| $2/60$ | $30$ |
| $1/60$ | $60$ |

The marks where $60/d$ is an integer are the **regular numbers** of [[Sexagesimal]]: $d\in\{1,2,3,4,5,6,10,12,15,20,30,60\}$. The unevenness the article describes is the unevenness of the reciprocal $1/d$.

## Every reading is an exact slope

A reading is a **rational** with denominator $60$ (right edge) or numerator $60$ (top edge). It is not an angle: it can be written down, added to another slope by the exact addition law ([[Sum of Slopes]]), and carried through a whole triangle solution without rounding. In the vocabulary of [[Certificates]], the position of the tick is the certificate. Wedges that are not multiples of $3^\circ$ ($\tfrac1{120}$ of a turn) have no exact slope in $\mathbb K$ ([[Slope Approximations]]), and the protractor gives the nearest tick.

## Resolution

*[AI]* Computed from the geometry. In degrees, for comparison with an ordinary protractor:

- Near a slope of $0$ (the bottom of the right edge) one mark is a step of $\arctan\tfrac1{60}\approx0.955^\circ$.
- At the diagonal (slope $1$) one mark is a step of about $0.48^\circ$.
- Near the vertical (the left of the top edge) one mark is again about $0.95^\circ$.

So the device resolves a wedge to **between about $0.48^\circ$ and $0.95^\circ$**, finest at the diagonal. Doubling the number of marks (to $120$) would halve each step.

## Related

The Egyptian **seked**, the slope measure of pyramid building, is a run per rise ([[Glossary]], Seqt): the top edge is its modern cousin, a reading of $1/m$ in sixtieths.
