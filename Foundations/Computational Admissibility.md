---
title: Computational Admissibility
type: concept
status: "canonical (Murphy's framework; the cost theorems themselves are open)"
provenance: "murphy (the framework: the three foundations; expression ≠ constructed object ≠ certified result; admissibility against a budget; the Finite Certification Theorem; functions with feasible domains and the inverse asymmetry; resolution and interval certificates; absolute and relative feasibility; the eight theses; the central principle) + ai-synthesis (the checks) + third-party (Parikh, Sazonov, Nelson, Buss, as reported by Murphy's reading)"
sources: "[[Creational Ultrafinitism]], [[Certificates]], [[Function Hierarchy]], [[Number Hierarchy]], [[Exact Until Output]]"
updated: 2026-11-07
---

# Computational Admissibility

*The working apparatus of [[Creational Ultrafinitism]]: not which numbers exist, but which constructions can be carried out, certified, and paid for.*

## The three foundations (Murphy)

1. **Ontological limitation.** Actualized infinity belongs to God alone. Created mathematical activity does not acquire divine attributes merely because its formal language permits us to write an expression.
2. **Epistemic and computational limitation.** A mathematical object must be accessible through a finite procedure, at a level of precision and complexity appropriate to the task.
3. **Certificate-based knowledge.** Having a mathematical expression is distinguished from having a finite, executable means of establishing the result it purports to describe ([[Certificates]]).

These are the limitation forms of the position's three parts ([[What this project is]]): creaturely realism, creational ultrafinitism, certificate-explicit constructivism.

The computer-science connection is what keeps ultrafinitism from degenerating into merely replacing infinite sets with very large finite sets: **a number can be finite in the formal sense and nevertheless be beyond any meaningful mathematical operation available to us.** Formal existence is not mathematical *availability*.

## Expression ≠ constructed object ≠ certified result (Murphy)

Three distinct concepts:

- **A. Mathematical expression** — a finite symbolic expression specifying a quantity. Writing $2^{2^{1000}}$ is easy.
- **B. Constructed numeral** — an actual finite representation of the quantity, produced through a specified procedure. The binary numeral of $2^{1000}$ is a 1 followed by 1000 zeros — manageable; the binary numeral of $2^{2^{1000}}$ requires $2^{1000}+1$ bits — inaccessible.
- **C. Executable computation** — a specified procedure that takes the available inputs and actually produces the required output or certificate within an admissible resource budget.

A refinement to Parikh: exponentiation is not uniformly infeasible — its cost depends on how input and output are represented (computing $2^n$ in binary from a binary $n$ is straightforward; materializing the output takes $n+1$ bits). Parikh's concern is not a blanket prohibition on exponentiation. Sazonov's treatment of notation and abbreviation is the literature's form of the point: a short binary expression can represent a number whose unary representation is impossibly long; a short expression is not automatically a feasible number. The recurring principle:

$$\text{expression}\ \ne\ \text{constructed object}\ \ne\ \text{certified result}.$$

## Admissibility (Murphy)

Let $x$ be the input, $L(x)$ its representation length, $\varepsilon>0$ rational the desired resolution, $C$ a construction or certification procedure, $T_C(x,\varepsilon)$ its computational cost, and $B$ the available resource budget. Then:

$$C \text{ is admissible} \iff T_C(x,\varepsilon)\le B.$$

Track memory and output size, not only time. **Construction cost and certification cost are bounded separately**: producing a result can be difficult while checking it is easy — the distinction at the heart of computational complexity and proof complexity, and the vault's own ([[Certificates]]).

### The Finite Certification Theorem (the proposed form)

For a specified object $X$, input class $D$, and rational resolution $\varepsilon>0$: there exists an explicit procedure $C$ such that

$$\forall x\in D,\quad T_C(x,\varepsilon)\le f\bigl(L(x),\varepsilon\bigr),$$

and $C$ produces a finite certificate verifying the claimed result to resolution $\varepsilon$. Three requirements:

1. an explicit construction algorithm;
2. a provable upper bound on its resource consumption;
3. an explicit verification procedure for the resulting certificate.

This is more rigorous than saying a calculation is feasible, and it connects directly to complexity theory, where time and memory are measured against input size.

## Functions have domains of feasible operation (Murphy)

A computational function is not initially a correspondence between two sets of numbers but

$$f:(D,C_D)\longrightarrow(E,C_E),$$

where $D,E$ are specified classes of constructed inputs and outputs and $C_D,C_E$ specify the admissible construction procedures. A function may be mathematically expressible and not computationally admissible over its entire proposed domain.

| Operation | Potential difficulty |
|---|---|
| Addition | output length and carry propagation |
| Multiplication | growth in output length and multiplication cost |
| Exponentiation | output size can grow exponentially |
| Factorial | extremely rapid output growth |
| Square root | the required output precision |
| Logarithm | precision and convergence cost |
| Inverse functions | error amplification and computational cost |
| Matrix inversion | dimension, coefficient growth, conditioning |

This is a more nuanced position than accepting or rejecting operations wholesale.

### The special problem of inverses

Even when $f(x)$ is inexpensive, $f^{-1}(y)$ to a specified precision may be expensive or unstable. Example (checked): for $y=x^2$ with nonnegative $x$, if $y$ is known within $\delta$ then

$$|\sqrt y-\sqrt{\tilde y}\,|\le\sqrt{|y-\tilde y|},$$

so guaranteeing error at most $\varepsilon$ can require $\delta\le\varepsilon^2$ — a cost-of-certification issue in miniature. (The inequality holds because, for $y\ge\tilde y\ge0$, $(\sqrt y-\sqrt{\tilde y})^2=y+\tilde y-2\sqrt{y\tilde y}\le y-\tilde y$.) Every major function is to be investigated together with its inverse: domain restrictions, output growth, precision requirements, error propagation, construction cost, certification cost ([[Function Hierarchy]], "Inverses are harder than they look"). This asymmetry between the cost of a function and the cost of its inverse is already the heart of modern cryptography ([[Fundamental Theorem of Arithmetic]]: factorization).

## Resolution (Murphy)

Exact rational results are distinguished from approximate results with certified precision. To establish a quantity $x$ to resolution $\varepsilon$: produce rational endpoints $a\le x\le b$ with $b-a\le\varepsilon$. The certificate consists of the rational endpoints, the construction procedure, the verification of the inequalities, and the resource bound. No infinitely precise real number is asserted — a finite interval with a provable property is. This is a natural seed for a constructive numerical analysis within the framework.

Resolution is not accuracy: a certificate establishes an approximation within a specified interval; it cannot make the underlying measurement more accurate than the evidence permits ([[Scale and Bands]], [[Number in Natural Philosophy]]).

## Absolute and relative feasibility (Murphy)

- **Absolute feasibility.** There is a meaningful boundary beyond which a number or operation is not mathematically available to created minds, irrespective of the particular computer, technology, or application. This establishes the philosophical horizon: human beings are finite creatures and cannot presume unlimited mathematical access; the physical bounds of [[Creational Ultrafinitism]] are the working estimate of that horizon's upper edge. (Sazonov explores something like this approach, with proposed boundaries, while acknowledging the difficulty of a universally accepted one.)
- **Relative feasibility.** An object or operation is feasible relative to a specified resource budget, computational procedure, and resolution — close to conventional computational complexity.

The vault needs both, with a carefully defined relationship: the absolute establishes the horizon; the relative provides the working mathematical apparatus. The distinction prevents every mathematical result from depending on the specifications of a particular computer, while also preventing the pretense that every finite expression represents an available mathematical object.

## The eight theses (Murphy)

1. Actualized infinity is an attribute of God, not of creation.
2. Created mathematical knowledge operates through finite acts of construction and demonstration.
3. A finite symbolic expression does not automatically establish the availability of its denoted object.
4. Mathematical operations have resource costs.
5. Those costs must be established through explicit procedures and arithmetic bounds.
6. Numerical claims should carry certificates appropriate to their required resolution.
7. Functions and their inverses must be evaluated for computational feasibility, not merely formal definability.
8. Mathematical induction and other general principles require scrutiny regarding the constructions they authorize. (Careful: bounded induction, predicative arithmetic, and the theological rejection of actualized infinity are three different things — Parikh and Nelson offer different technical restrictions, and they are not to be conflated. See [[Future Directions]] item 6.)

## The central principle (Murphy)

> A mathematical assertion about a created quantity is warranted only insofar as its object, construction, and certification are accessible through a finite procedure whose resource requirements can themselves be established.

That is a distinctive mathematical program, not merely a philosophical objection to conventional mathematics.

## Literature (from Murphy's reading; full details on [[Reading List]], section 4)

Parikh (1971), *Existence and Feasibility in Arithmetic* — the starting point; Sazonov (1995), *On Feasible Numbers* — notation, and restrictions on deduction itself; Nelson (1986), *Predicative Arithmetic* — arithmetic without the usual induction principle; Buss (1999), *Bounded Arithmetic, Proof Complexity and Two Papers of Parikh* — the survey of the technical landscape. Three strands: feasible and bounded arithmetic (Parikh, Sazonov, Buss); predicative and constructive foundations (Nelson, Bishop, Martin-Löf); computational complexity and certification (Cobham, Cook, Bellantoni and Cook, Buss). **These authors supply mathematical and philosophical tools; they do not collectively establish the theological position.**

## Open

1. The cost theorems themselves: a Finite Certification Theorem for each kind of certificate — the shared hard problem 1 of [[Function Hierarchy]], [[Fundamental Theorem of Arithmetic]], [[Exact Until Output]] and [[Fundamental Theorem of Algebra]].
2. The precise relationship between the absolute horizon and particular relative budgets.
