---
title: ASA Congruence
type: theorem
status: canonical
provenance: ai-synthesis (standard Euclid, Elements I.26 (first part); case selection Murphy's)
sources: "[[Geometry Hierarchy]]"
updated: 2026-10-07
---
# ASA Congruence

Purely geometric: no numbers, no slopes, no trigonometry. "Equal" means *congruent*, the level-4 relation of the [[Geometry Hierarchy]]. A **wedge** is the concrete angle at a vertex; two wedges are congruent when one fits exactly on the other.

**Statement.** If two wedges and the side **between** them in one triangle are congruent to two wedges and the side between them in another, the triangles are congruent.

In triangles $ABC$ and $DEF$: wedge $B\cong$ wedge $E$, $BC\cong EF$, wedge $C\cong$ wedge $F$ $\Rightarrow$ $\triangle ABC\cong\triangle DEF$.

## Proof

Suppose $AB$ and $DE$ were not congruent; say $AB$ is the longer. Mark $G$ on $BA$ with $BG\cong ED$.

- Triangles $GBC$ and $DEF$ have $BG\cong ED$, wedge $B\cong$ wedge $E$, and $BC\cong EF$. By [[SAS Congruence]] they are congruent, so wedge $BCG\cong$ wedge $EFD$.
- But wedge $EFD\cong$ wedge $BCA$ by hypothesis, so wedge $BCG\cong$ wedge $BCA$.
- $G$ lies inside the side $BA$, so the wedge $BCG$ is only part of the wedge $BCA$. A part is not congruent to the whole. Contradiction.

So $AB\cong DE$, and the triangles are congruent by [[SAS Congruence]]. $\blacksquare$

## Construction

Given a segment and two wedges: copy one wedge at each end of the segment, on the same side. Where the free arms meet is the third vertex. The arms meet exactly when the two wedges together are narrower than a straight wedge.

## The four cases

[[SSS Congruence]] · [[SAS Congruence]] · [[ASA Congruence]] · [[AAS Congruence]]. Together they say which three facts about a triangle fix it completely. Two sides and a *non-included* wedge (SSA) do not in general: the ambiguous case, which can give two triangles.
