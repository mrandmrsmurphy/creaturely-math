---
title: Groups of Small Order
type: concept
status: canonical (draft)
provenance: "murphy+ai (Murphy's brief: document the groups of order 1 through 23, following TheGrayCuber's four-video series 'Group Theory Step-by-Step', whose transcripts Murphy supplied; the arguments are the video's, re-derived and checked here; the table of invariants was computed by machine)"
sources: "[[Groups]], [[Cyclic Groups]]; TheGrayCuber, *Group Theory Step-by-Step: 1–7*, *8–15*, *16* and *17–23* (YouTube), as exposition (third-party)"
updated: 2026-11-14
---

# Groups of Small Order

There are $28$ groups of order $1$ through $15$, $14$ of order $16$ and $17$ of order $17$ through $23$: $59$ in all (counted up to isomorphism, below). This page lists them, says how to tell them apart, and gives the arguments that show the list is complete. The explanation follows TheGrayCuber's video series, which is a good human introduction to this material.

*Note:* Every group below was built concretely (as permutations or as pairs) and its order, centre and element orders were computed by machine; the list for each order has no two groups with the same invariants, so no group appears twice. **Completeness** is proved here for prime order, for order $2p$ ($p$ odd) and for order $15$ by hand, for orders $1$ to $8$ by exhaustive search ([[Cyclic Groups]]), and for orders $9$, $12$, $16$, $18$, $20$ and $21$ by machine enumeration of the semidirect or index-$2$ extension cases (each in its section).

**Naming.** On this page $D_n$ is the dihedral group of order $2n$ (the symmetries of a regular $n$-gon), as on [[Symmetries of the Equilateral Triangle]] and [[Symmetries of the Square]]. The video writes the order instead, so its $D_6$ is our $D_3$, its $D_8$ is our $D_4$, and so on.

## Isomorphism

Two groups are **isomorphic** when one can be turned into the other by renaming the elements: a one-to-one correspondence under which products correspond to products. The groups $(\{1,-1\},\times)$, (even and odd integers, $+$) and (rotation by nothing or by a half turn) have different elements but the same Cayley table once the elements are renamed, so they are the same group of order $2$.

To show two groups **are** isomorphic, give the renaming. To show they are **not**, find an **invariant** that differs:

- the **order**;
- whether the group is **abelian**;
- the size of the **centre** (elements commuting with everything);
- the **number of elements of each order**;
- the **number of distinct squares** $\{x^2\}$: if the groups were isomorphic, the renaming would carry squares to squares, so the numbers must agree.

Equal element-order counts do not by themselves prove two groups isomorphic. Among **abelian** groups of finite order they do: the counts determine the group. Among nonabelian groups they may not, so a coincidence of counts there settles nothing; the number of distinct squares is then a second test (order $16$ below has four pairs it separates).

## Products of groups

The **direct product** $G\times H$ is the set of ordered pairs $(g,h)$ with the operation done in each coordinate separately. Its order is $|G|\,|H|$.

- $C_2\times C_2$ is the **Klein four-group** $V$: the symmetries of a non-square rectangle (the half turn, the horizontal flip, the vertical flip, and doing nothing). Flip then flip is the half turn.
- $C_m\times C_n\cong C_{mn}$ **exactly when $\gcd(m,n)=1$**. Then $C_6\cong C_2\times C_3$, $C_{10}\cong C_2\times C_5$, $C_{15}\cong C_3\times C_5$. This is the [[Chinese Remainder Theorem]] as group theory. It fails otherwise: $C_4\not\cong C_2\times C_2$ (an element of order $4$ against none), and $C_9\not\cong C_3\times C_3$ ($6$ elements of order $9$ against none).

## Orders 2, 3 and 4 by Sudoku

A group table is a Latin square, so each element appears once in every row and column (cancellation, [[Groups]]). The identity $e$ fills its own row and column.

- **Order 2.** One cell is left, in row $a$. The row already has $a$, so it must be $e$. The group is forced: $C_2$.
- **Order 3** ($e,a,b$). Row $a$ needs $b$ and $e$ in its last two cells, but column $b$ already contains $b$, so $ab=e$ and $aa=b$. The rest is forced: $C_3$.
- **Order 4.** Pair each element with its inverse. The identity is its own inverse, and three non-identity elements cannot all be paired, so at least one is its own inverse. Either **all three are** (the diagonal is all $e$) or **exactly one is, and the other two are inverses of each other** (they cannot also pair elsewhere: an element has one inverse). Each choice forces the whole table. The first is the Klein group $V$; the second, renamed $0,1,2,3$ with $1,3$ the pair and $0$ and $2$ self-inverse, is $C_4$. Both tables are on [[Groups]]. (Pairing a different two elements only renames.)

## Prime order is cyclic

Let $|G|=p$ prime and $a\ne e$. The elements $e,a,a^2,\dots$ form a subgroup, and by **Lagrange's theorem** its order divides $p$. It contains $e$ and $a$, so its order is not $1$; it is $p$. So $\langle a\rangle=G$ and $G\cong C_p$. The same reasoning gives $C_5,C_7,C_{11},C_{13}$, and the answers $1$ for orders $2,3,5,7,11,13$.

## Order $2p$ for an odd prime $p$: cyclic or dihedral

This covers orders $6,10,14$. It uses two facts from the **Sylow theorems**, stated here and not proved: a group of order divisible by a prime power has a subgroup of that order (in particular an element $a$ of order $2$ and an element $b$ of order $p$), and the **number of subgroups of order $p$ is $\equiv1\pmod p$**.

1. The number of $p$-subgroups is $1$ or at least $p+1$. Two different subgroups of prime order share only $e$, so $p+1$ of them hold at least $1+(p+1)(p-1)=p^2>2p$ elements (for $p\ge3$), more than the group has. So there is exactly **one** subgroup of order $p$: $\langle b\rangle$.
2. The order of $ab$ divides $2p$. It is not $1$ or $p$ (either would put $a$ inside $\langle b\rangle$). So it is $2$ or $2p$.
3. If $ab$ has order $2p$, the group is $C_{2p}$.
4. If $ab$ has order $2$, then $abab=e$; multiplying on the left by $a$ and on the right by $b^{-1}$ gives $ba=ab^{-1}$. With $a^2=b^p=e$ these are the relations of the dihedral group $D_p$.

So order $6$: $C_6$, $D_3$. Order $10$: $C_{10}$, $D_5$. Order $14$: $C_{14}$, $D_7$. (For $p=2$, order $4$, step 1 fails: that is why $V$ appears.)

## Order 15: only $C_{15}$

The number of subgroups of order $5$ is $1$ or $6$ ($\equiv1\bmod5$); six would hold $1+6\cdot4=25>15$ elements. So there is one, $H$. The other $10$ elements cannot have order $1$ or $5$ (that would put them in $H$), so they have order $3$ or $15$. If all had order $3$ they would sit two at a time in $5$ subgroups of order $3$, but the count must be $\equiv1\pmod3$ and $5\not\equiv1$. So some element has order $15$: $G\cong C_{15}$.

## Abelian groups: the fundamental theorem

**Fundamental theorem of finite abelian groups** (stated, not proved): every finite abelian group is a direct product of cyclic groups of prime-power order, uniquely up to order of the factors. (The uniqueness is the point: the prime-power cycles are the building blocks, and cycles whose orders share a prime never combine into a larger cycle, while coprime ones do. So there is no need to count element orders to find duplicates among abelian groups.) So the abelian groups of order $n$ are found by factoring $n$ into prime powers and splitting each prime power into a sum of exponents.

| order | abelian groups | how many |
|---|---|---|
| $8=2^3$ | $C_8$, $C_4\times C_2$, $C_2^3$ | $3$ (exponent $3=3=2+1=1+1+1$) |
| $9=3^2$ | $C_9$, $C_3^2$ | $2$ |
| $12=2^2\cdot3$ | $C_4\times C_3\;(=C_{12})$, $C_2^2\times C_3\;(=C_6\times C_2)$ | $2$ |
| $4=2^2$ | $C_4$, $C_2^2$ | $2$ |
| $16=2^4$ | $C_{16}$, $C_8\times C_2$, $C_4\times C_4$, $C_4\times C_2^2$, $C_2^4$ | $5$ (exponent $4$ split five ways) |
| $18=2\cdot3^2$ | $C_9\times C_2\;(=C_{18})$, $C_3^2\times C_2\;(=C_6\times C_3)$ | $2$ |
| $20=2^2\cdot5$ | $C_4\times C_5\;(=C_{20})$, $C_2^2\times C_5\;(=C_{10}\times C_2)$ | $2$ |
| $n$ squarefree ($1,2,3,5,6,7,10,11,13,14,15,17,19,21,22,23$) | $C_n$ only | $1$ |

A group of order $p^2$ is always abelian.

## All the groups of order 1 to 15

Element orders are written *order: number of elements*. "Centre" is the number of elements commuting with everything. All computed by machine.

| order | group | abelian | centre | element orders |
|---|---|---|---|---|
| $1$ | $C_1$ | yes | $1$ | $1{:}1$ |
| $2$ | $C_2$ | yes | $2$ | $1{:}1,\ 2{:}1$ |
| $3$ | $C_3$ | yes | $3$ | $1{:}1,\ 3{:}2$ |
| $4$ | $C_4$ | yes | $4$ | $1{:}1,\ 2{:}1,\ 4{:}2$ |
| $4$ | $V=C_2^2$ | yes | $4$ | $1{:}1,\ 2{:}3$ |
| $5$ | $C_5$ | yes | $5$ | $1{:}1,\ 5{:}4$ |
| $6$ | $C_6$ | yes | $6$ | $1{:}1,\ 2{:}1,\ 3{:}2,\ 6{:}2$ |
| $6$ | $D_3$ | no | $1$ | $1{:}1,\ 2{:}3,\ 3{:}2$ |
| $7$ | $C_7$ | yes | $7$ | $1{:}1,\ 7{:}6$ |
| $8$ | $C_8$ | yes | $8$ | $1{:}1,\ 2{:}1,\ 4{:}2,\ 8{:}4$ |
| $8$ | $C_4\times C_2$ | yes | $8$ | $1{:}1,\ 2{:}3,\ 4{:}4$ |
| $8$ | $C_2^3$ | yes | $8$ | $1{:}1,\ 2{:}7$ |
| $8$ | $D_4$ | no | $2$ | $1{:}1,\ 2{:}5,\ 4{:}2$ |
| $8$ | $Q_8$ | no | $2$ | $1{:}1,\ 2{:}1,\ 4{:}6$ |
| $9$ | $C_9$ | yes | $9$ | $1{:}1,\ 3{:}2,\ 9{:}6$ |
| $9$ | $C_3^2$ | yes | $9$ | $1{:}1,\ 3{:}8$ |
| $10$ | $C_{10}$ | yes | $10$ | $1{:}1,\ 2{:}1,\ 5{:}4,\ 10{:}4$ |
| $10$ | $D_5$ | no | $1$ | $1{:}1,\ 2{:}5,\ 5{:}4$ |
| $11$ | $C_{11}$ | yes | $11$ | $1{:}1,\ 11{:}10$ |
| $12$ | $C_{12}$ | yes | $12$ | $1{:}1,\ 2{:}1,\ 3{:}2,\ 4{:}2,\ 6{:}2,\ 12{:}4$ |
| $12$ | $C_6\times C_2$ | yes | $12$ | $1{:}1,\ 2{:}3,\ 3{:}2,\ 6{:}6$ |
| $12$ | $D_6$ | no | $2$ | $1{:}1,\ 2{:}7,\ 3{:}2,\ 6{:}2$ |
| $12$ | $Q_{12}$ | no | $2$ | $1{:}1,\ 2{:}1,\ 3{:}2,\ 4{:}6,\ 6{:}2$ |
| $12$ | $A_4$ | no | $1$ | $1{:}1,\ 2{:}3,\ 3{:}8$ |
| $13$ | $C_{13}$ | yes | $13$ | $1{:}1,\ 13{:}12$ |
| $14$ | $C_{14}$ | yes | $14$ | $1{:}1,\ 2{:}1,\ 7{:}6,\ 14{:}6$ |
| $14$ | $D_7$ | no | $1$ | $1{:}1,\ 2{:}7,\ 7{:}6$ |
| $15$ | $C_{15}$ | yes | $15$ | $1{:}1,\ 3{:}2,\ 5{:}4,\ 15{:}8$ |

The counts by order are $1,1,1,2,1,2,1,5,2,2,1,5,1,2,1$. Within each order the rows differ in an invariant, so they are different groups (for the abelian rows, this is also enough to show they are isomorphic to nothing else in the list).

## Semidirect products

The direct product lets the two factors ignore each other. In a **semidirect product** $N\rtimes_\alpha K$ the second factor acts on the first. Take a group $K$ and a **homomorphism** $\psi$ from $K$ to the automorphisms of $N$. The elements are the pairs $(n,k)$ and $(n_1,k_1)(n_2,k_2)=(n_1\,\psi(k_1)(n_2),\ k_1k_2)$. For $K=C_m$ the homomorphism is the choice of one automorphism $\alpha=\psi(1)$ with $\alpha^m=\mathrm{id}$, and the formula reads $(n_1,k_1)(n_2,k_2)=(n_1\,\alpha^{k_1}(n_2),\ k_1+k_2)$. Associativity, which is what makes it a group, was checked for every product on this page.

Two things are needed of $\alpha$, and the video shows the first: it must be **one-to-one and preserve products** (an isomorphism), or the relation $f\,x\,f^{-1}=\alpha(x)$ does not define a group. In $C_8$, "$r\mapsto r^2$" sends $r$ and $r^5$ to the same element, and "add $1$ to the power" does not preserve products. The automorphisms of $C_8$ are $r\mapsto r,\ r^3,\ r^5,\ r^7=r^{-1}$ (the units mod $8$), four in all. And $\alpha^m=\mathrm{id}$, since $f^m=e$.

The **direct product is the semidirect product with $\alpha=\mathrm{id}$**. The dihedral group is $C_n\rtimes C_2$ with $\alpha(r)=r^{-1}$ ([[Symmetries of the Equilateral Triangle]]). A group may be a semidirect product in several ways, so the action is part of the name.

**Direction matters:** $N\rtimes K$ (the second group acts on the first) can differ from $K\rtimes N$. Every useful shortcut below says when the action is forced to be trivial, and then the product is direct:

- **$K$ acts on $N=C_2$ (or any $N$ with trivial automorphism group):** the only automorphism is the identity, so the product is direct. So a $C_2$ on the **left** of a semidirect product is never interesting.
- **The order of $\psi(k)$ divides the order of $k$.** If $\gcd(|K|,|\mathrm{Aut}(N)|)=1$ the action is trivial. Example: $C_3$ acting on $C_3$ ($\mathrm{Aut}(C_3)=C_2$), $C_5$ acting on $C_4$ ($\mathrm{Aut}(C_4)=C_2$) or on $C_2^2$ ($\mathrm{Aut}=S_3$, order $6$, no element of order $5$).
- **Inner actions give direct products:** if the action of each $k$ is conjugation by $\theta(k)$ for some homomorphism $\theta:K\to N$, the product is $N\times K$ (rename $(n,k)$ as $(n\,\theta(k),k)$). So $C_3$ acting on $D_3$ by conjugation by a rotation gives nothing new.

## Automorphisms

An **automorphism** of $G$ is an isomorphism from $G$ to itself (a renaming of $G$ that preserves products). The automorphisms of $G$ form a group $\mathrm{Aut}(G)$ under composition: composing two is one; the identity is one; every automorphism can be run backwards; associativity is that of functions.

For a cyclic group, an automorphism is determined by where $1$ goes, and it must go to a generator, so **$\mathrm{Aut}(C_n)$ is the group of units mod $n$** ([[Cyclic Groups]]). Machine-checked small cases:

| $N$ | $\mathrm{Aut}(N)$ |
|---|---|
| $C_2$ | trivial |
| $C_3$ | $C_2$ (identity, inverse) |
| $C_4$ | $C_2$ |
| $C_5$ | $C_4$ (identity, square, inverse, square-then-inverse) |
| $C_7$ | $C_6$ |
| $C_8$ | $C_2^2$ (the units mod $8$) |
| $C_9$ | $C_6$ |
| $C_2^2$ | $S_3$ ($=D_3$, order $6$) |
## The nonabelian ones

- **Dihedral $D_n$** (order $2n$): rotation $r$ with $r^n=e$ and a flip $s$ with $s^2=e$, tied by $srs=r^{-1}$. *Rotate then flip equals flip then the inverse rotation.* $D_3$ is the triangle group; $D_4$, $D_5$, $D_6$, $D_7$ are the square, regular pentagon, hexagon and heptagon.
- **Quaternion $Q_8$:** $i^2=j^2=k^2=-1$, $ij=k$, and $ij=-ji$ (so the elements do not commute). One element of order $2$ ($-1$) and six of order $4$, against five and two in $D_4$: the same order, but not the same group ([[Symmetries of the Square]], [[Fiat Numbers]]). A tempting slip: squaring $ij=k$ and rearranging the left side gives $i^2j^2=+1$, but $k^2=-1$. The rearrangement is the error, because $i$ and $j$ cannot be swapped.
- **$Q_{12}$** (the dicyclic group of order $12$): an element $\zeta$ of order $6$ with $\zeta^3=-1$, and $j$ with $j^2=-1$ and $j\zeta j^{-1}=\zeta^{-1}$. In general $Q_{4n}$ has $\zeta^n=-1$ together with the $j$ relation, and $Q_8$ is the case $n=2$. The Cayley picture matches the dihedral one, except that $j$ has order $4$ where the flip has order $2$.
- **$A_4$**, the **rotations of a regular tetrahedron**. Label the four faces $1,2,3,4$. Put face $1$ in any of $4$ places and face $2$ in any of the $3$ remaining ones, and the rest is fixed: $4\cdot3=12$ rotations, as permutations of the faces. Cycle notation (143) means $1\to4\to3\to1$ with $2$ fixed; products are read right to left. Example, checked: (2 4 3) after (1 4 3) is the double swap (1 3)(2 4). It has eight elements of order $3$ and three of order $2$, and **none of order $6$ or more**, unlike every other group of order $12$. **$A_4$ is only the rotations.** Including reflections the full symmetry group of the tetrahedron is $S_4$, of order $24$, which this page does not treat.

## $D_3\times C_2$ is $D_6$

The product of the triangle group and $C_2$ is isomorphic to the hexagon group $D_6$ (checked by trying every assignment of generators). The reason is general:

**When $m$ is odd, $D_{2m}\cong D_m\times C_2$.** The half turn $r^m$ commutes with everything (it is its own inverse and is sent to itself by a flip), and the subgroup $\langle r^2,s\rangle\cong D_m$ does not contain it. So $D_{2m}$ splits as $D_m\times\langle r^m\rangle$. This gives $D_6\cong D_3\times C_2$ and $D_{10}\cong D_5\times C_2$.

**When $m$ is even, it does not split in this way.** The centre of $D_n$ is $\{e,r^{n/2}\}$ for even $n$ (two elements); $D_4\times C_2$ has a centre of four. So $D_8\not\cong D_4\times C_2$. Whether $D_8$ or $D_{12}$ is a direct product of *any* two groups is argued by hand on the centre, not machine-checked.

Every dihedral group is the **semidirect product** $C_n\rtimes C_2$: the rotation subgroup and the pair of "flip or not", glued by $srs=r^{-1}$. The video calls this a "product with an extra bar". With these two factors it is a direct product only when the glue does nothing, that is when $r=r^{-1}$, so $n\le2$. A group can still be a direct product of *different* factors: $D_6\cong D_3\times C_2$ above.

## The Sylow counts for order 12

For each prime $p$, the number of subgroups of order $p^k$ (the largest power of $p$ dividing the order) is $\equiv1\pmod p$. For order $12$ (subgroups of order $4$ and of order $3$), computed:

| group | subgroups of order $4$ | subgroups of order $3$ |
|---|---|---|
| $C_{12}$, $C_6\times C_2$ | $1$ | $1$ |
| $D_6$ | $3$ | $1$ |
| $Q_{12}$ | $3$ | $1$ |
| $A_4$ | $1$ | $4$ |

All counts are $\equiv1\pmod2$ for order $4$ and $\equiv1\pmod3$ for order $3$ ($4\equiv1$).

## Order 16: fourteen groups

On this page $D_8$ is the octagon group of order $16$ (the video's $D_{16}$), $Q_{16}$ is the quaternion-type group with $\zeta^4=-1$, and $D_4\times C_2$, $Q_8\times C_2$ are products. Element orders are *order: number*; "squares" is the number of distinct values of $x^2$. All computed by machine.

| group | abelian | centre | element orders | squares |
|---|---|---|---|---|
| $C_{16}$ | yes | $16$ | $1{:}1,\ 2{:}1,\ 4{:}2,\ 8{:}4,\ 16{:}8$ | $8$ |
| $C_8\times C_2$ | yes | $16$ | $1{:}1,\ 2{:}3,\ 4{:}4,\ 8{:}8$ | $4$ |
| $C_4\times C_4$ | yes | $16$ | $1{:}1,\ 2{:}3,\ 4{:}12$ | $4$ |
| $C_4\times C_2^2$ | yes | $16$ | $1{:}1,\ 2{:}7,\ 4{:}8$ | $2$ |
| $C_2^4$ | yes | $16$ | $1{:}1,\ 2{:}15$ | $1$ |
| $D_8$ | no | $2$ | $1{:}1,\ 2{:}9,\ 4{:}2,\ 8{:}4$ | $4$ |
| $Q_{16}$ | no | $2$ | $1{:}1,\ 2{:}1,\ 4{:}10,\ 8{:}4$ | $4$ |
| $SD_{16}=C_8\rtimes_3C_2$ | no | $2$ | $1{:}1,\ 2{:}5,\ 4{:}6,\ 8{:}4$ | $4$ |
| $M_{16}=C_8\rtimes_5C_2$ | no | $4$ | $1{:}1,\ 2{:}3,\ 4{:}4,\ 8{:}8$ | $4$ |
| $D_4\times C_2$ | no | $4$ | $1{:}1,\ 2{:}11,\ 4{:}4$ | $2$ |
| $Q_8\times C_2$ | no | $4$ | $1{:}1,\ 2{:}3,\ 4{:}12$ | $2$ |
| $C_4\rtimes C_4$ | no | $4$ | $1{:}1,\ 2{:}3,\ 4{:}12$ | $3$ |
| $C_2^2\rtimes C_4$ | no | $4$ | $1{:}1,\ 2{:}7,\ 4{:}8$ | $3$ |
| $Q_8\rtimes C_2$ ($=C_4\circ D_4$) | no | $4$ | $1{:}1,\ 2{:}7,\ 4{:}8$ | $2$ |

**Where each comes from.**
- **Abelian (five):** the fundamental theorem. The exponent $4$ of $2^4$ splits in five ways ($4$, $3+1$, $2+2$, $2+1+1$, $1+1+1+1$). A prime power gives no coincidences: $C_{p^a}\times C_{p^b}$ never merges into one cycle, because the orders share the factor $p$, so every split is a different group. This is also why $C_{16}$ is the only group with an element of order $16$ (such an element generates the whole group).
- **Products** $D_4\times C_2$ and $Q_8\times C_2$: an order-$8$ group times $C_2$. An order-$4$ times an order-$4$ group is abelian, since both groups of order $4$ are.
- **$D_8$, $Q_{16}$**: the octagon, and the dicyclic group with $\zeta^4=-1$ ($\zeta$ of order $8$, $j^2=-1$, $j\zeta j^{-1}=\zeta^{-1}$).
- **$C_8\rtimes C_2$**, one for each automorphism of $C_8$ ($r\mapsto r^{-1}$, $r^3$, $r^5$, identity): the first is $D_8$, the second is the **semidihedral** group $SD_{16}$, the third is the **modular** group $M_{16}$, the last is the abelian $C_8\times C_2$. In $SD_{16}$ the element $r^kf$ squares to $r^{4k}$, so the four with $k$ even have order $2$ and the four with $k$ odd have order $4$, which gives the counts $5,6,4$.
- **$C_4\rtimes C_4$** ($a^4=b^4=e$, $bab^{-1}=a^{-1}$; $C_4$ has only two automorphisms, identity and inverse), **$C_2^2\rtimes C_4$** (the generator of $C_4$ swaps the two coordinates) and **$Q_8\rtimes C_2$** (the $C_2$ inverts $i$ and fixes $j$). The last is the central product $C_4\circ D_4=C_4\circ Q_8$, which I checked is the same group.

**Pairs with equal element-order counts, and what separates them:**

| shared counts | groups | what separates them |
|---|---|---|
| $1{:}1,\ 2{:}3,\ 4{:}4,\ 8{:}8$ | $C_8\times C_2$, $M_{16}$ | the first is abelian |
| $1{:}1,\ 2{:}3,\ 4{:}12$ | $C_4\times C_4$, $Q_8\times C_2$, $C_4\rtimes C_4$ | squares $4,\,2,\,3$ |
| $1{:}1,\ 2{:}7,\ 4{:}8$ | $C_4\times C_2^2$, $C_2^2\rtimes C_4$, $Q_8\rtimes C_2$ | squares $2,\,3,\,2$; the first is abelian and the third is not |

All fourteen rows have different (counts, squares, abelian, centre) together, so they are fourteen different groups.

**Why there are no others** (certificate by machine). A group of order $16$ is a $2$-group and has a subgroup $H$ of index $2$ (recalled), which is normal and has order $8$, so it is one of the five groups of order $8$. Pick $g\notin H$. Then $g^2=h\in H$, conjugation by $g$ is an automorphism $\varphi$ of $H$ with $\varphi(h)=h$, and $\varphi^2$ is conjugation by $h$; the group is $H\cup Hg$ with $(xg^a)(yg^b)=x\varphi^a(y)g^{a+b}$. I listed **every** triple $(H,\varphi,h)$ satisfying these conditions, built the group of order $16$ for each, checked associativity, and tested it for isomorphism with the table's rows. Each fell into one of the fourteen, and each of the fourteen occurred. So the count is exactly fourteen.

## Orders 9 and 12, completed

Two tools: **Schur–Zassenhaus** (stated, not proved): a normal subgroup whose order is coprime to its index has a complement, so $G=N\rtimes K$; and the Sylow count $n_p\equiv1\pmod p$.

- **Order 9.** An element of order $9$ gives $C_9$. Otherwise every non-identity element has order $3$; a subgroup $\langle a\rangle$ of order $3$ has index $3$ and so is normal (an index-$p$ subgroup of a $p$-group), and taking $b\notin\langle a\rangle$ gives $C_3\rtimes C_3$. The only automorphism of $C_3$ of order dividing $3$ is the identity, so the product is direct: $C_3^2$. Two groups.
- **Order 12.** $n_3\in\{1,4\}$. If $n_3=1$ then $C_3$ is normal with a complement $K$ of order $4$ ($C_4$ or $C_2^2$), acting through $\mathrm{Aut}(C_3)=C_2$: $C_4$ trivially is $C_{12}$, nontrivially is $Q_{12}$; $C_2^2$ trivially is $C_6\times C_2$, nontrivially is $D_6$. If $n_3=4$ there are eight elements of order $3$, and the other four form the unique (normal) subgroup $N$ of order $4$, with $G=N\rtimes C_3$. $C_4$ has no automorphism of order $3$, and $C_2^2$ has ($\mathrm{Aut}=S_3$): this is $A_4$. Five groups.

Both counts were also found by machine: every homomorphism from the complement into the automorphism group of the normal subgroup, built, checked for associativity and sorted by isomorphism, gives exactly these.

## Orders 17 to 23

Prime orders $17,19,23$: only $C_p$. Order $22=2\cdot11$: $C_{22}$ and $D_{11}$, by the order-$2p$ argument above.

**Order 18.** By the Sylow count $n_3\mid2$ and $n_3\equiv1\pmod3$, so $n_3=1$: the subgroup $N$ of order $9$ is normal, $N$ is $C_9$ or $C_3^2$, and $G=N\rtimes C_2$, with $C_2$ acting by an automorphism of order dividing $2$.
- $N=C_9$: $\mathrm{Aut}(C_9)=C_6$ has one element of order $2$ (inverse). Identity gives $C_{18}$; inverse gives $D_9$.
- $N=C_3^2$: an automorphism of order dividing $2$ is diagonalizable with entries $\pm1$, so up to renaming it is the identity ($C_6\times C_3$), inverse on one factor ($D_3\times C_3$), or inverse on both ($(C_3\times C_3)\rtimes C_2$, the "two triangles flipped together" group: both flip or neither flips, so every element has order $2$ or $3$).
Five groups. $D_9$ has no element of order $6$ and $D_3\times C_3$ has none of order $9$, which tells them apart at a glance.

**Order 20.** $n_5\mid4$ and $n_5\equiv1\pmod5$ give $n_5=1$: $C_5$ is normal with a complement $K$ of order $4$, acting through $\mathrm{Aut}(C_5)=C_4$.
- $K=C_2^2$: the action has image of order dividing $2$: trivial gives $C_{10}\times C_2$; otherwise one factor of $K$ inverts $C_5$ and the other commutes: $D_5\times C_2\cong D_{10}$.
- $K=C_4$: the generator acts by an automorphism of order dividing $4$: identity gives $C_{20}$; inverse gives $Q_{20}$ (dicyclic); the square map $r\mapsto r^2$ (order $4$) gives the **Frobenius group** $F_{20}=C_5\rtimes C_4$. The remaining one, $r\mapsto r^3$, is the square map's inverse, and gives an isomorphic group (replace the generator of $K$ by its inverse).
Five groups. $F_{20}$ has only elements of order $2,4,5$; $D_{10}$ and $Q_{20}$ have elements of order $10$.

**Order 21.** $n_7\mid3$ and $\equiv1\pmod7$ give $n_7=1$: $C_7$ is normal with complement $C_3$, acting by an automorphism of $C_7$ ($\mathrm{Aut}=C_6$) of order dividing $3$: the identity ($C_{21}$), or $r\mapsto r^2$ or $r\mapsto r^4$, which give isomorphic groups. That is the **Frobenius group** $F_{21}=C_7\rtimes C_3$, the only nonabelian group of order $21$ (so there are two groups). Odd order, so no dihedral or quaternion group.

All the semidirect cases above were enumerated by machine as well (every homomorphism from $K$ to $\mathrm{Aut}(N)$, associativity checked, sorted by isomorphism): $5$, $5$ and $2$ groups. Element orders, computed:

| order | group | abelian | centre | element orders |
|---|---|---|---|---|
| $17$ | $C_{17}$ | yes | $17$ | $1{:}1,\ 17{:}16$ |
| $18$ | $C_{18}$ | yes | $18$ | $1{:}1,\ 2{:}1,\ 3{:}2,\ 6{:}2,\ 9{:}6,\ 18{:}6$ |
| $18$ | $C_6\times C_3$ | yes | $18$ | $1{:}1,\ 2{:}1,\ 3{:}8,\ 6{:}8$ |
| $18$ | $D_9$ | no | $1$ | $1{:}1,\ 2{:}9,\ 3{:}2,\ 9{:}6$ |
| $18$ | $D_3\times C_3$ | no | $3$ | $1{:}1,\ 2{:}3,\ 3{:}8,\ 6{:}6$ |
| $18$ | $(C_3\times C_3)\rtimes C_2$ | no | $1$ | $1{:}1,\ 2{:}9,\ 3{:}8$ |
| $19$ | $C_{19}$ | yes | $19$ | $1{:}1,\ 19{:}18$ |
| $20$ | $C_{20}$ | yes | $20$ | $1{:}1,\ 2{:}1,\ 4{:}2,\ 5{:}4,\ 10{:}4,\ 20{:}8$ |
| $20$ | $C_{10}\times C_2$ | yes | $20$ | $1{:}1,\ 2{:}3,\ 5{:}4,\ 10{:}12$ |
| $20$ | $D_{10}$ | no | $2$ | $1{:}1,\ 2{:}11,\ 5{:}4,\ 10{:}4$ |
| $20$ | $Q_{20}$ | no | $2$ | $1{:}1,\ 2{:}1,\ 4{:}10,\ 5{:}4,\ 10{:}4$ |
| $20$ | $F_{20}$ | no | $1$ | $1{:}1,\ 2{:}5,\ 4{:}10,\ 5{:}4$ |
| $21$ | $C_{21}$ | yes | $21$ | $1{:}1,\ 3{:}2,\ 7{:}6,\ 21{:}12$ |
| $21$ | $F_{21}$ | no | $1$ | $1{:}1,\ 3{:}14,\ 7{:}6$ |
| $22$ | $C_{22}$ | yes | $22$ | $1{:}1,\ 2{:}1,\ 11{:}10,\ 22{:}10$ |
| $22$ | $D_{11}$ | no | $1$ | $1{:}1,\ 2{:}11,\ 11{:}10$ |
| $23$ | $C_{23}$ | yes | $23$ | $1{:}1,\ 23{:}22$ |

The counts by order are $1,5,1,5,2,2,1$ for $17$ to $23$. Semidirect products tend to concentrate elements in small orders: $F_{20}$ has none of order $10$ or $20$, and $F_{21}$ none of order $21$.

## Open

- Order $24$ (fifteen groups, from memory) is next; the series stops at order $23$ so far.
- Normal subgroups and quotients in general (the video's "extra bar") are on [[Symmetries of the Equilateral Triangle]] and [[Symmetries of the Square]] for two cases, not as a general theory.
- Schur–Zassenhaus and the Sylow theorems are used here as stated, not proved.
