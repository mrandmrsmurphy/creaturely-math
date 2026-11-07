---
title: Geometry Hierarchy
type: hierarchy
status: canonical
provenance: "murphy (the branching revision — the table, the principles, the Hilbert treatment, the topology line, the reading order, the freshman recommendation; from his 2026-11-07 outline) + ai-synthesis (the organization)"
sources: "Murphy's raw mathematics draft (2026-05); his 2026-11-07 geometry outline"
updated: 2026-11-07
---

# Geometry Hierarchy — structures, constructions, and measurement

Geometry is organized by the structures it assumes — with one correction to the older picture: **this is a branching structure, not a single ladder.** Two orderings were being conflated: ordering geometries by the amount of *structure* they assume, and ordering them by the degree of *numerical machinery* they require. They are related but not the same, and the second is not the goal of the first: analytic geometry is a representational method, not the culmination of geometry.

| # | Level | Primitive relation | Gloss |
|---|---|---|---|
| 1 | **Incidence** | *lies on* | points, lines, intersection; no measurement |
| 2 | **Ordered** | *is between* | betweenness, segments, rays, orientation |
| 3 | **Congruent** | *is congruent to* | equality of segments and angles without numerical measurement |
| 4 | **Affine / Projective** | *is parallel to* / *projects to* | direction, parallelism, ratios; projective incidence |
| 5 | **Metric** | *has quadrance* | numerical measurement through admissible quantities |
| 6 | **Geometric classification** | parallel behavior / curvature | Euclidean, hyperbolic, spherical, and related geometries |
| 7 | **Analytic representation** | *has coordinates* | algebraic representation of geometric configurations |

**Qualification.** The levels are organizational, not strictly sequential. Incidence is foundational; order, congruence and parallelism are *distinct* additional structures — affine geometry can be developed without an ordering relation, ordered geometry does not require parallelism, and congruence geometry needs no numerical lengths. Hilbert's axiom groups (incidence, order, congruence, parallelism, continuity) are the model: he explicitly investigates their *independence*. The dependency shape:

> **Incidence** (points, lines, intersection) — then three branches: **order** (betweenness), **affine** (parallelism), **congruence** (equal segments and angles) — then compatible combinations (the synthetic geometries: neutral, Euclidean, hyperbolic, spherical, projective, affine), then **measurement structures** (segment arithmetic, quadrance, spread, area), then **coordinate realization** (rational, algebraic, and other admissible coordinate systems).

This is a dependency diagram, not a claim that every geometry must be constructed in this order.

## Perpendicularity does not select the geometry

Perpendicularity is a metrical or congruential relation; it does not distinguish the geometries. The distinguishing mark is the **behavior of parallels**:

- **Euclidean:** through an external point, exactly one parallel to a given line.
- **Hyperbolic:** more than one — in the usual hyperbolic plane, infinitely many.
- **Spherical:** great circles intersect; there are no parallel great circles. (Technical qualification: two great circles meet in two antipodal points, so the sphere is not simply a Hilbert plane with a different parallel axiom; identifying antipodal points gives *elliptic* geometry, where the projective lines meet uniquely.)

The parallel postulate distinguishes Euclidean from hyperbolic within neutral geometry; spherical geometry requires a different underlying model.

## Congruence is powerful without numbers (Murphy)

Levels 1–3 (with the affine branch) need no numbers at all — but the point is stronger than that: **congruence is a substantial mathematical structure that never mentions measurement.** Two segments congruent; two angles congruent; two triangles congruent; a segment copied onto a ray; a perpendicular constructed; a circle drawn from a center and an exhibited radius segment — none of this assigns a numerical length or angle measure. There is a distinction between saying two segments have *equal lengths* and saying each *has length 5*: the former is geometric, the latter numerical. The vault preserves that distinction carefully.

One qualification: no numbers does not mean no certificates. A construction is still finitely many operations and a theorem is still a finite proof, and an unrestricted axiom quantifying over all points may still presume an unlimited domain. The vault distinguishes a finite geometric construction from the claim that a completed infinite geometric plane exists.

## Hilbert's continuity axioms, taken separately

Hilbert's *Grundlagen der Geometrie* (1899) groups the axioms: incidence, order, congruence, parallelism, continuity. The continuity group originally contained the Archimedean axiom; a completeness axiom was added in later editions in varying formulations. The two get different answers.

**A. The Archimedean axiom — retained in local, constructive form.** Geometrically: given segments $a$ and $b$, some finite multiple of $a$ exceeds $b$. For represented positive lengths this is a finite arithmetic assertion with an explicit witness: $a=\tfrac37$, $b=\tfrac{100}{11}$ needs $n>\tfrac{700}{33}$, so $n=22$ suffices (computed). Distinguish the *local* principle — given two exhibited lengths, produce the witness — from the *global* axiom quantifying over every pair of segments in the whole domain. The first is a working principle; the second's status depends on the admissible geometric domain, and is left open.

**B. The completeness axiom — rejected as a foundational requirement.** Hilbert's completeness says the system cannot be extended by further points while preserving the other axioms: a maximality condition, meant to eliminate gaps in the geometric continuum. But why should a creaturely geometry contain every point that could be described abstractly? The rational coordinate plane $\mathbb Q^2$ contains $(0,0)$, $(1,0)$, $(0,1)$ but not $\bigl(\tfrac12,\tfrac{\sqrt3}2\bigr)$ — and we can still reason about the equilateral triangle, exhibiting its height as a quadratic algebraic quantity with a finite certificate. We do not need to fill the plane.

**C. What replaces completeness (Murphy).** No replacement global axiom; instead, **finite geometric extendibility**, a methodological principle: a geometric system may be extended by any point or construction that can be explicitly exhibited and whose defining relations can be certified, without requiring the system to contain every describable point. Its working forms:

1. **Constructive extension.** Given a finite configuration, an additional point is admitted when a specified construction produces it.
2. **Locatedness.** When a question requires the position of a point relative to a line, there must be a procedure establishing the relation, or a bounded uncertainty where exact determination is unavailable.
3. **Resolution-bounded approximation.** Where exact construction exceeds the available numerical domain, rational bounds with an explicit resolution certificate: $a\le x\le b$, $b-a\le\varepsilon$ ([[Computational Admissibility]]).

The absence of a global completeness principle does not prevent rigorous construction, comparison, or approximation.

## Coordinates are a representation, not a culmination

Analytic geometry is not a higher form of geometry; it is a representation of geometry by algebra. The Cartesian plane is usually presented over $\mathbb R$, but nothing requires that — and note where $\mathbb R$ enters the classroom: "Descartes laid a grid over the world," after which the Greeks' separation of arithmetic and geometry was forgotten (Murphy's *What is Mathematics*, ch. *Incommensurate*). The admissible alternatives:

- a **rational** coordinate plane;
- an **algebraic** coordinate plane;
- a **finite-field** affine plane (Murphy's favorite);
- a **projective** plane over a suitable field (the wheel with infinity and bottom);
- coordinate systems over other admissible structures ([[Computational Admissibility]]).

On the rational plane, with $A=(a_1,a_2)$, $B=(b_1,b_2)$ rational: the **quadrance** $Q(A,B)=(b_1-a_1)^2+(b_2-a_2)^2$ is rational, and orthogonality is the dot-product condition $u\cdot v=0$ — perpendicularity without computing an angle. Wildberger's rational trigonometry (`third-party`: quadrance and spread in place of distance and angle) is useful here, though the vault does not adopt all its commitments; the vault's own [[Constructible Trigonometry]] is the allied route through slopes and constructible lengths. The two projects are to be cross-linked ([[Future Directions]] item 9).

The distinction to keep: **rational geometry** (primary quantities rational), **constructible geometry** (quantities from permitted finite constructions, [[Constructible Numbers]]), **algebraic geometry** (broader algebraic quantities, subject to admissibility), **conventional analytic geometry** (coordinates over the completed reals).

## Two structural developments that are not rungs

**Projective geometry** is not a corner of analytic geometry; it is a distinct development, studying incidence and what is invariant under projection. Parallel lines are treated as meeting at a point at infinity — which in this vault is a **projective direction**, not evidence of a completed infinite extension. A direction is a ratio $[m:n]$ rather than a slope $m/n$, so vertical directions need no special treatment, and homogeneous coordinates do not presume a completed real plane (compare $\mathbb P^1(\mathbb K)$ in the CT framework).

**Transformation geometry.** Klein's Erlangen program organizes geometry by the transformations under which its properties are invariant — a second organizational axis, by invariance rather than by primitive relations:

| Geometry | Transformations |
|---|---|
| Projective | projective transformations |
| Affine | affine transformations |
| Euclidean | isometries |
| Similarity | similarity transformations |

## Topology

Finite combinatorial topology is foundational: finite graphs, simplicial complexes, finite cell complexes, finite combinatorial surfaces, finite topological spaces; explicitly generated complexes subject to resource bounds. Euler's $V-E+F=2$ for a convex polyhedron is an entirely finite combinatorial result, and surfaces, triangulations, connectivity and homology can be investigated through finite constructions. Rejected as foundations: arbitrary power sets of infinite domains, unrestricted infinite open covers, general compactness via arbitrary covers. General point-set topology is admissible only insofar as its objects and arguments can be given constructive, finite presentations.

## Euclid's postulates, in the vault's reading

Postulate 2 is traditionally "to extend a finite straight line continuously in a straight line" — it does not require constructing an actually infinite segment. A given segment can be extended; a further finite extension can be made; the process can be repeated whenever required. The vault makes the *procedure* primary, not the primitive infinite line:

| Euclid's postulate | Ultrafinitist interpretation |
|---|---|
| 1. Draw a line between two points | construct a finite straight segment |
| 2. Extend a line | potentially extend a finite segment |
| 3. Draw a circle | construct a circle from an exhibited center and radius segment |
| 4. All right angles are equal | congruence of right angles |
| 5. The parallel postulate | a geometric axiom selecting a particular geometry |

The fifth postulate remains an independent geometric choice, not a consequence of the first four.

## Hilbert's segment calculus — the bridge to arithmetic

Hilbert showed that a **calculus of segments** — addition and multiplication of segments — can be developed from incidence, order, congruence and the parallel axiom, *without* the Archimedean axiom, leading to a form of analytic geometry (discussed in Bernays's account of Hilbert's foundations). For this project that is fascinating: the transition from geometry to arithmetic need not pass through the real continuum. Arithmetic can be developed geometrically, through constructions and operations on segments — a natural bridge between the freshman Euclidean year and the later *Exact Algebra* ([[Curriculum Plan]]), and a named research project below.

## The geometric principles (Murphy)

1. Incidence and congruence do not require numerical measurement.
2. Geometric constructions must be specified through finite procedures.
3. Lines are approached through potentially extensible finite segments, not assumed to be completed infinite collections.
4. Congruence precedes numerical measurement: equality of segments does not require assigning them numbers.
5. Metric geometry privileges quadrance over ordinary distance wherever possible.
6. Perpendicularity is a relation of geometric orthogonality, not the defining distinction between Euclidean and non-Euclidean geometries.
7. Coordinate systems need not employ the completed real-number system; rational and constructible coordinate systems are legitimate alternatives.
8. Projective and transformation geometry are studied as distinct structural developments.

## Open research

1. Formalize incidence, order, congruence and affine geometry over finite construction domains.
2. Investigate Hilbert's segment calculus without the Archimedean axiom — can the useful arithmetic of segments be derived without importing a completed continuum? (The bridge project.)
3. Establish a rational and constructible metric geometry based on quadrance (and possibly spread).
4. Develop finite projective geometry and the projective slope.
5. Develop the constructive replacements for global completeness above into formal principles.
6. Computational bounds for geometric constructions and inverse constructions ([[Computational Admissibility]]).
7. Finite combinatorial topology and its relationship to geometry.

## Reading order (Murphy)

| Priority | Work | What to investigate |
|---|---|---|
| 1 | Euclid's *Elements* | Books I–IV: construction before measurement |
| 2 | Hilbert, *Foundations of Geometry* | the five axiom groups; independence; the segment calculus |
| 3 | Wildberger, *Divine Proportions* | quadrance, spread, rational metrical geometry |
| 4 | Geometry of numbers; rational coordinate geometry | arithmetic arising from geometric constructions |
| 5 | Klein, the Erlangen program | geometry organized by invariance |

Two useful Wildberger papers: "The Ancient Greeks Present: Rational Trigonometry" ([arXiv:0806.3481](https://arxiv.org/abs/0806.3481)) and "Trisecting the Equilateral Triangle with Rational Trigonometry" ([his UNSW page](https://web.maths.unsw.edu.au/~norman/papers/Equilateral.pdf)).

## The freshman recommendation (Murphy)

Make **congruence geometry** the center of freshman Euclidean geometry — not a stepping stone toward measurement. There is substantial genuine mathematics before numerical measurement enters. When quadrance does enter, it should feel like a natural extension of something students already understand geometrically, not the beginning of geometry proper.
