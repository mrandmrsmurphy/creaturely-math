---
title: AAS Congruence
type: theorem
status: canonical
provenance: ai-synthesis (standard Euclid, Elements I.26 (second part); case selection Murphy's)
sources: "[[Geometry Hierarchy]]"
updated: 2026-10-07
---
# AAS Congruence

Purely geometric: no numbers, no slopes, no trigonometry. "Equal" means *congruent*, the level-4 relation of the [[Geometry Hierarchy]]. A **wedge** is the concrete angle at a vertex; two wedges are congruent when one fits exactly on the other.

**Statement.** If two wedges and a side **not between** them in one triangle are congruent to the corresponding two wedges and side in another, the triangles are congruent.

In triangles $ABC$ and $DEF$: wedge $A\cong$ wedge $D$, wedge $B\cong$ wedge $E$, and $BC\cong EF$ (the side adjacent to $B$ and opposite $A$) $\Rightarrow$ $\triangle ABC\cong\triangle DEF$.

## Proof

*Via the third wedge.* In a plane triangle the three wedges together make a straight wedge (Elements I.32, which uses the parallel postulate). So wedge $C\cong$ wedge $F$, and the side $BC$ lies between the wedges $B$ and $C$: this is [[ASA Congruence]].

*Without the parallel postulate (Euclid's own route).* Suppose $AB$ and $DE$ were not congruent; say $AB$ is longer, and mark $G$ on $BA$ with $BG\cong ED$.

- By [[SAS Congruence]], $\triangle GBC\cong\triangle DEF$, so wedge $BGC\cong$ wedge $EDF\cong$ wedge $BAC$.
- In $\triangle AGC$, the wedge $BGC$ is an *exterior* wedge at $G$, and the exterior wedge is wider than the interior wedge at $A$ (Elements I.16). Contradiction.

So $AB\cong DE$, and [[SAS Congruence]] finishes. $\blacksquare$

## Construction

Given a segment $BC$, a wedge $B$ at one end and a wedge $A$ that is to be opposite $BC$: the third wedge $C$ is determined (it makes a straight wedge with $A$ and $B$), so the problem becomes [[ASA Congruence]].

## The four cases

[[SSS Congruence]] · [[SAS Congruence]] · [[ASA Congruence]] · [[AAS Congruence]]. Together they say which three facts about a triangle fix it completely. Two sides and a *non-included* wedge (SSA) do not in general: the ambiguous case, which can give two triangles.
