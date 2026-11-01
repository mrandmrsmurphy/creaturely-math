---
title: Diagonal Argument
type: theorem
status: "canonical (accepted as a statement about procedures; the ontological reading refused)"
provenance: "murphy (the position, accept the matching and the diagonal as processes, a negative result like the irrationality of the square root of 2) + ai-synthesis (the procedural statement, the finite diagonal, the checks, the flagged points)"
sources: "[[Infinity and Cantor]], [[Creational Ultrafinitism]], [[Certificates]], [[Number Hierarchy]]"
updated: 2026-10-09
---

# Diagonal Argument

Companion to [[Infinity and Cantor]], which states the position; this page works the argument out. Murphy's reading: both the matching of the whole numbers with the evens and the diagonal are **processes**, reasoned about as well as a creature can, and the diagonal is a **negative result** about lists, not an existence proof of the numbers beyond them, "any more than 'no $(a/b)^2=2$' proved existence."

## The matching $n\mapsto2n$

The whole numbers and the evens both go on as far as we can see. The rule $n\mapsto2n$ and its inverse $m\mapsto m/2$ are two procedures, each defined at every number reached, undoing each other. With matching taken as more fundamental than counting, they have "the same size."

Two comments [AI]:

- **Say what is claimed.** What is established is a *pair of mutually inverse procedures*, not a comparison of two completed sets. Galileo's old worry (the part matches the whole, against Euclid's "the whole is greater than the part") is then not a paradox: a part can be matched with the whole by a rule, while at every finite stage the part is smaller. Evens up to $2N$ are matched with $1,\dots,N$; the matching doubles the cost of reaching a given number.
- **The doubling matters at the threshold.** If $T$ is the largest number held ([[Creational Ultrafinitism]]), then $n\mapsto2n$ is defined only for $n\le T/2$. The rule is potentially unbounded, but each *application* has a cost, and the matching is total only as a rule.

## The diagonal as a procedure

> **Theorem (procedural).** Let $L$ be a listing procedure: given $n$ it produces a binary sequence $L(n)$, that is, a procedure giving digit $L(n)(k)$ on demand. Then the sequence $D(k)=1-L(k)(k)$ is a procedure, and it differs from $L(n)$ at digit $n$, for every $n$. So **no listing procedure lists all binary-sequence procedures.**

*Proof.* Digit $k$ of $D$ is found by running $L(k)$ for $k$ digits and flipping the last. Each step is finite. $D\ne L(n)$ because $D(n)\ne L(n)(n)$. $\square$

It has the shape the vault accepts: it **constructs**, it does not appeal to completed totalities, and the conclusion is a **negative** about lists. What it says is: *given a listing, here is a sequence-procedure the listing misses.* This is the constructive Cantor asked for in [[Future Directions]] item 4. *(Recollection to check: this is standard in constructive mathematics, valid for Bishop and for Brouwer.)*

### Worked example (checked)

Let row $k$ be the first eight binary digits of $1/(k+1)$, for $k=1,\dots,8$:

| $k$ | row |
|---|---|
| 1 | 10000000 |
| 2 | 01010101 |
| 3 | 01000000 |
| 4 | 00110011 |
| 5 | 00101010 |
| 6 | 00100100 |
| 7 | 00100000 |
| 8 | 00011100 |

The diagonal is $1,0,1,0,0,0,1,1$; flipping it gives $00100011$, which differs from row $k$ at digit $k$ for all eight rows.

### A finite version, exact

For $N$ strings each $N$ digits long, the flipped diagonal is a string of length $N$ not among them. This is an exact finite theorem, and a weak one: counting says $2^N-N$ strings are missing ($12$ for $N=4$, over a million for $N=20$). The diagonal finds one by reading $N$ digits.

## Where "up to a point" lies

What the argument yields is: **no procedure exhausts the sequences.** What the classical reading adds is: *therefore there is a completed set larger than the whole numbers.* The vault accepts the first, and for the second keeps only a difference of kind:

| | the whole numbers | the sequence-procedures |
|---|---|---|
| can be extended | yes, by $n\mapsto n+1$ | yes, by the diagonal |
| can be listed | yes, by $n\mapsto n$ | **no**, whatever the listing |

Both are *potentially* infinite. The whole numbers can be generated in order; the sequences cannot even be generated in an order. That is a real difference between the two, stated without a "bigger" or an $\aleph_1$. It matches the parallels Murphy draws: *no $a/b$ squares to $2$* (a negative about fractions), *no largest prime* (a negative about lists of primes, [[Proof Types]]), *no list of the sequences* (a negative about lists of sequences).

## Sequences are certificates, not numbers

The diagonal acts on **digit sequences**, which in the vault are the *certificates* of numbers at levels 7 to 11 ([[Number Hierarchy]]), not numbers. Two consequences [AI]:

- **A sequence is not yet a different number.** In binary $0.0111\ldots$ and $0.1000\ldots$ are the same number. To make the diagonal differ as a *number*, avoid tails of all $0$s or all $1$s (for instance, in base ten, use only the digits $4$ and $5$, flipping $4\leftrightarrow5$: against rows $1/3,1/7,1/9,1/11,1/13,1/17$ the diagonal digits are $4,5,4,4,4,4$, checked).
- **The diagonal gives no number.** The sequence $D$ is another certificate-procedure. That it is not on the list says nothing about a number "at the end," which is the point Murphy makes about irrationals.

## One sentence on [[Infinity and Cantor]] to reconsider [AI]

That page says that "definable numbers are countable; ℝ is not; so almost all reals are provably beyond any finite description." The second half treats the reals as a completed totality larger than the definable ones. In the vault's reading the sound statement is the procedural one: **no listing procedure of describable sequences is complete**, with no count of the reals. (Also, "definable" is not itself definable without paradox, the Berry/Richard worry.) Whether to rewrite that sentence is Murphy's call; I have left the page alone.

## Hard problems

1. **Which listings.** The theorem is about a listing that is a procedure. A list "someone proposes" without a rule is outside it; the vault should say that explicitly.
2. **Computable listings.** If $L$ is a total computable listing then $D$ is computable; so the total computable sequences have no total computable listing. This is a fact about procedures listing procedures (recollection of the standard result; the diagonal construction above is the proof).
3. **Cost.** To read digit $k$ of $D$ one runs $L(k)$ to digit $k$; the cost depends on $L$ and can be large well before $k$ is large.
4. **Cardinality language.** Whether the vault uses "size" at all beyond the matching of procedures, and whether $\aleph_0$ is worth keeping as a name for "listable" ([[Infinity and Cantor]]).
