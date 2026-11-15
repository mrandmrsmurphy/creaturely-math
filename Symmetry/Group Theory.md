---
title: Group Theory
type: hub
status: canonical (draft)
provenance: "ai-synthesis (the hub and its reading order, built from the group pages; the banner is the vault's three-part position applied to groups, and is the AI's wording, not Murphy's); the pages it links carry their own provenance"
sources: "[[Groups]], [[Cyclic Groups]], [[Groups of Small Order]], [[Simple Groups]], [[Sporadic Groups]], [[Monster Group]]"
updated: 2026-11-14
---

# Group Theory

> **Creaturely realism:** a group is a real finite structure, like the six symmetries of a triangle, and not a formal fiction. **Certificate-explicit constructivism:** a Cayley table, a presentation, or a set of generators is a certificate; every claim about a small group is checked by looking entries up. **Creational ultrafinitism:** the table stops being writable long before the group stops being finite, and the Monster is the extreme case ([[What this project is]]).

*Group theory is the mathematics of symmetry: a set of transformations that can be done in sequence, undone, and done again. This page is the map; each idea is on one page.*

## Reading order

1. **[[Groups]]** — the four axioms, the Cayley table as certificate, the two groups of order $4$, orders and subgroups, Lagrange's theorem.
2. **[[Symmetries of the Equilateral Triangle]]** and **[[Symmetries of the Square]]** — the first nonabelian groups, as the symmetries of shapes you can hold: the Cayley tables, element orders, subgroups, conjugacy, normal subgroups, quotients.
3. **[[Cyclic Groups]]** — $C_1$ through $C_8$: tables, generators (the units mod $n$), subgroups (one per divisor), $C_6\cong C_2\times C_3$.
4. **[[Groups of Small Order]]** — all $59$ groups of order $1$ to $23$: isomorphism and the invariants that tell groups apart, direct and semidirect products, automorphisms, the arguments that show each list is complete.
5. **[[Simple Groups]]** — normal subgroups and quotients in general; simple groups as the atoms; composition series; $A_4$ against $A_5$; the classification.
6. **[[Sporadic Groups]]** — the twenty-six groups that belong to no family: names, orders (checked), the Happy Family and the pariahs, and where tables stop being possible.
7. **[[Monster Group]]** — the largest sporadic simple group, its order, moonshine, and what a finite object that cannot be listed means for the position.

## Conventions on these pages

- $D_n$ is the dihedral group of **order $2n$** (the symmetries of a regular $n$-gon). The video series the small-order pages follow writes the order instead; a note on [[Groups of Small Order]] gives the translation.
- A product $ab$ means *do $b$ first, then $a$* (right to left, like composing functions).
- "Checked" means an exhaustive machine check or a worked check by hand on the page. "Cited" means a theorem from the literature, stated and not proved here (Sylow, Schur–Zassenhaus, Jordan–Hölder, the fundamental theorem of finite abelian groups, the classification of finite simple groups). "Recalled" means a fact from memory that was not checked.
- Exact arithmetic throughout; no angle measure. Wedges are named concretely (a third of a turn, a half turn).

## What the vault has settled and what it cites

| | Status |
|---|---|
| All groups of order $1$ to $23$ | **Checked**: counts $1,1,1,2,1,2,1,5,2,2,1,5,1,2,1,14,1,5,1,5,2,2,1$ (orders $1$ to $23$), by exhaustive search or by enumeration of extensions |
| Orders $24$ and above | Not documented (order $24$ has fifteen groups, recalled) |
| Sylow theorems, Schur–Zassenhaus, Jordan–Hölder, the abelian structure theorem | **Cited** |
| The classification of finite simple groups | **Cited**; flagged as a result held by testimony ([[Simple Groups]]) |
| The Monster | **Third-party**; its arithmetic is checked, its properties recalled ([[Monster Group]]) |

## Where groups already appear elsewhere in the vault

- **Clock arithmetic and the finite fields:** $(\mathbb Z/n,+)$ is $C_n$ ([[Modular Arithmetic]]); the nonzero elements of a prime field form a cyclic group, and Fermat's little theorem is Lagrange's ([[GF(5)]], [[GF(7)]], [[Fermat's Little Theorem]], [[Euler's Theorem]], [[Wilson's Theorem]]).
- **The Chinese remainder theorem** is the statement $C_m\times C_n\cong C_{mn}$ when $\gcd(m,n)=1$ ([[Chinese Remainder Theorem]]).
- **The quaternion group $Q_8$** is the unit quaternions of [[Fiat Numbers]].
- **The group law on slopes** ([[Sum of Slopes]]) and the **units of a number system** ([[Number Hierarchy]]).

## Open

The open items for this strand are on the Agenda in [[Future Directions]] (Symmetry): order $24$; full Cayley tables for $C_2\times C_4$, $C_2^3$ and $Q_8$; the dihedral family in general; the finite fields' additive groups; a worked example of moonshine at feasible scale; and the Monster's status under the position, flagged to Murphy on [[Monster Group]].
