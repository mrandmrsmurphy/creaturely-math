---
title: SSS Congruence
type: theorem
status: canonical
provenance: ai-synthesis (standard Euclid, Elements I.7–I.8; case selection Murphy's)
sources: "[[Geometry Hierarchy]]"
updated: 2026-10-07
---
# SSS Congruence

Purely geometric: no numbers, no slopes, no trigonometry. "Equal" means *congruent*, the level-4 relation of the [[Geometry Hierarchy]]. A **wedge** is the concrete angle at a vertex; two wedges are congruent when one fits exactly on the other.

**Statement.** If the three sides of one triangle are congruent to the three sides of another, the triangles are congruent, and so their wedges match.

In triangles $ABC$ and $DEF$: $AB\cong DE$, $BC\cong EF$, $CA\cong FD$ $\Rightarrow$ $\triangle ABC\cong\triangle DEF$.

## Existence

Three segments make a triangle exactly when each is shorter than the other two together (the triangle inequality, Elements I.20, I.22). With equality the "triangle" collapses onto a line.

## Proof

Place $\triangle ABC$ with $B$ on $E$ and $C$ on $F$, with the vertex $A$ on the opposite side of $EF$ from $D$. (Flip the triangle if necessary.) Join $AD$.

- $EA\cong AB\cong DE$ (the moved vertex $A$ is at the same distances from $E$ and $F$ as before), so triangle $EAD$ has two congruent sides $EA,ED$, and its base wedges at $A$ and at $D$ are congruent (the isosceles theorem, Elements I.5).
- Likewise $FA\cong CA\cong FD$, so the wedges of triangle $FAD$ at $A$ and $D$ are congruent.
- Adding these (or subtracting, when $AD$ falls outside $EF$), the whole wedge at $A$ is congruent to the whole wedge at $D$.

So $AE\cong DE$, $AF\cong DF$, and the included wedges at $A$ and $D$ are congruent. By [[SAS Congruence]], $\triangle EAF\cong\triangle EDF$. $\blacksquare$

## Construction

Given three segments: draw the first as the base, then draw a circle about each end with radius the other two segments. A meeting point of the circles is the third vertex ([[Constructible Numbers]]: one compass-and-straightedge step). The two meeting points are mirror images, so the triangle is unique up to reflection.

## The four cases

[[SSS Congruence]] · [[SAS Congruence]] · [[ASA Congruence]] · [[AAS Congruence]]. Together they say which three facts about a triangle fix it completely. Two sides and a *non-included* wedge (SSA) do not in general: the ambiguous case, which can give two triangles.
