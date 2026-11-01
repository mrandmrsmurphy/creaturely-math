---
title: SAS Congruence
type: theorem
status: canonical
provenance: ai-synthesis (standard Euclid, Elements I.4; case selection Murphy's)
sources: "[[Geometry Hierarchy]]"
updated: 2026-10-07
---
# SAS Congruence

Purely geometric: no numbers, no slopes, no trigonometry. "Equal" means *congruent*, the level-4 relation of the [[Geometry Hierarchy]]. A **wedge** is the concrete angle at a vertex; two wedges are congruent when one fits exactly on the other.

**Statement.** If two sides and the wedge **between** them in one triangle are congruent to two sides and the wedge between them in another, the triangles are congruent: the third sides are congruent, and the other two wedges match.

In triangles $ABC$ and $DEF$: $AB\cong DE$, $AC\cong DF$, and wedge $A\cong$ wedge $D$ $\Rightarrow$ $\triangle ABC\cong\triangle DEF$.

## Proof (by superposition)

Move $\triangle ABC$ so that $A$ sits on $D$ and the side $AB$ lies along $DE$. Since $AB\cong DE$, the point $B$ lands on $E$. The wedges at $A$ and $D$ are congruent, so $AC$ falls along $DF$, and since $AC\cong DF$ the point $C$ lands on $F$. Now $BC$ and $EF$ have the same endpoints, and there is only one straight line between two points, so $BC$ coincides with $EF$. The whole triangles coincide. $\blacksquare$

## Construction

Given two segments and a wedge: lay off the first segment on one arm of a copy of the wedge and the second on the other arm, and join the ends. The result is the triangle.

## Remarks

- This is Euclid's own proof, which uses motion of figures. Hilbert's axioms avoid the motion by taking SAS as an axiom of congruence.
- The wedge must be the *included* one. With the wedge opposite one of the sides, the data can fit two triangles.

## The four cases

[[SSS Congruence]] · [[SAS Congruence]] · [[ASA Congruence]] · [[AAS Congruence]]. Together they say which three facts about a triangle fix it completely. Two sides and a *non-included* wedge (SSA) do not in general: the ambiguous case, which can give two triangles.
