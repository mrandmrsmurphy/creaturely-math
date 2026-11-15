---
title: Simple Groups
type: concept
status: canonical (draft)
provenance: "murphy+ai (Murphy's brief: continue the group theory documentation toward the Monster group; the worked examples were computed by machine; the classification theorem and the Jordan–Hölder theorem are third-party and are stated, not proved)"
sources: "[[Groups]], [[Groups of Small Order]], [[Symmetries of the Equilateral Triangle]]"
updated: 2026-11-14
---

# Simple Groups

*Simple groups are the atoms of finite group theory, as the primes are the atoms of the whole numbers ([[Fundamental Theorem of Arithmetic]]). This page says what that means, works two small cases with exact numbers, and states the classification that leads to [[Monster Group]].*

## Normal subgroups and quotients

A subgroup $N$ of $G$ is **normal** when conjugating by any element of $G$ leaves it where it is: $gNg^{-1}=N$ for every $g$. Equivalently, $N$ is a subgroup that is a **union of conjugacy classes**. (The conjugacy class of $a$ is every element $gag^{-1}$.)

If $N$ is normal, the cosets $gN$ are themselves the elements of a group, the **quotient** $G/N$: *ignore $N$*. Two cases already on the vault:

- In the triangle group $D_3$ the rotations $\{e,r,r^2\}$ are normal. The quotient has order $2$: rotation or reflection ([[Symmetries of the Equilateral Triangle]]).
- In the square group $D_4$ the centre $\{e,r^2\}$ is normal and the quotient is the Klein four-group ([[Symmetries of the Square]]).

In an abelian group every subgroup is normal (the conjugate of $a$ is $a$).

A group is **simple** when its only normal subgroups are $\{e\}$ and the whole group. A simple group cannot be taken apart by ignoring a piece: every quotient is either the group itself or trivial.

## Abelian simple groups

An abelian group is simple exactly when it has no subgroups other than $\{e\}$ and itself. The subgroups of $C_n$ are one for each divisor of $n$ ([[Cyclic Groups]], checked for $n\le8$), so **$C_n$ is simple exactly when $n$ is prime**. Every abelian simple group is $C_p$.

## Worked example: $A_4$ is not simple, $A_5$ is

The **alternating group** $A_n$ is the group of even permutations of $n$ points (order $n!/2$). $A_4$ is the group of rotations of the tetrahedron ([[Groups of Small Order]]).

**$A_4$** (order $12$). Its conjugacy classes have sizes $1,3,4,4$. The classes of sizes $1$ and $3$ together make $1+3=4$ elements, which divide $12$: they are $\{e\}$ and the three double swaps, and with the product they make the Klein four-group $V$. So $V$ is a normal subgroup of order $4$, and $A_4$ is **not** simple. The quotient $A_4/V$ is $C_3$.

**$A_5$** (order $60$). Its conjugacy classes have sizes $1,12,12,15,20$: the identity, two classes of five-cycles ($12$ each), the $15$ double swaps $(a\,b)(c\,d)$, and the $20$ three-cycles. A normal subgroup is a union of classes containing the identity class, and its order must divide $60$. Every way of adding the other sizes to $1$ was tried:

| classes taken | order |
|---|---|
| identity only | $1$ |
| identity and $15$ | $16$ (does not divide $60$) |
| identity and $20$ | $21$ |
| identity and a $12$ | $13$ |
| identity and both $12$s | $25$ |
| identity, $15$, $20$ | $36$ |
| and so on: only $1$ and $60$ divide $60$ | |

So **$A_5$ is simple**. It is the smallest nonabelian simple group (cited, not re-derived here; every group of order $2$ to $23$ on [[Groups of Small Order]] is either of prime order or has a normal subgroup other than $\{e\}$ and itself, which agrees with it).

The class sizes, and the list of unions that divide $60$, were computed by machine. $A_5$ is the rotation group of the regular icosahedron (and of the dodecahedron), the first of the groups with a large and rigid structure.

## Composition series: factoring a group

Choose a normal subgroup $G_1$ of $G$, then a normal subgroup $G_2$ of $G_1$, and so on down to $\{e\}$, each time taking a **largest** proper normal subgroup so that the quotients are simple:

$$G=G_0\supset G_1\supset G_2\supset\cdots\supset\{e\}.$$

The simple quotients $G_{i}/G_{i+1}$ are the **composition factors**. The **Jordan–Hölder theorem** (cited): the composition factors are the same for every such chain, up to order and isomorphism, just as the prime factors of a whole number are.

Examples, with the orders of the factors:

| group | a composition series | factor orders |
|---|---|---|
| $C_6$ | $C_6\supset C_3\supset e$ | $2,3$ |
| $D_3$ | $D_3\supset C_3\supset e$ | $2,3$ |
| $A_4$ | $A_4\supset V\supset C_2\supset e$ | $3,2,2$ |
| $S_4$ | $S_4\supset A_4\supset V\supset C_2\supset e$ | $2,3,2,2$ |
| $A_5$ | $A_5\supset e$ | $60$ (simple) |

Two warnings. The factors multiply to the order of the group ($2\cdot3=6$, $3\cdot2\cdot2=12$), as primes do. But **the factors do not determine the group**: $C_6$ and $D_3$ have the same factors $C_2,C_3$ and are different groups (one abelian, one not). How the factors are glued together is the extension problem, and it is what the semidirect products of [[Groups of Small Order]] describe.

Every finite group is therefore built from simple groups, and the simple groups are the finite groups that cannot be factored further.

## The classification

**Classification of finite simple groups** (cited, not proved). Every finite simple group is one of:

1. a cyclic group $C_p$ of prime order;
2. an alternating group $A_n$ with $n\ge5$;
3. a group **of Lie type**, which comes in several infinite families built from matrices over finite fields (for example the group of $2\times2$ matrices of determinant $1$ over $\mathrm{GF}(p)$, modulo $\pm1$; the finite fields are [[GF(5)]], [[GF(7)]] and the like);
4. one of **26 sporadic groups**, which belong to no family.

The sporadic groups range from $M_{11}$, of order $7920$, to the Monster ([[Monster Group]]), of order about $8\times10^{53}$.

The twenty-six sporadic groups, with their names and orders, the Happy Family and the pariahs, are on [[Sporadic Groups]].

## How the position reads this

**[AI]** The classification is a finite statement about an infinite list, whose proof is spread over a very large body of papers and is not something a reader can follow end to end, only trust through a community of checkers. In the vocabulary of [[Certificates]] it is a result held by testimony and by a procedure of mutual checking, more than by one certificate that anyone can run. This is a flag, not a verdict, and it is Murphy's to judge. The same question in sharper form, for one object, is on [[Monster Group]].
