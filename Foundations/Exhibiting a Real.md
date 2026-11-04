---
title: Exhibiting a Real
type: argument
status: "canonical (the challenge and what can be shown in answer; theorems cited from recollection and to be checked)"
provenance: "murphy (the challenge: even the square root of 2 is not checkable through a Dedekind cut, which only defines an algorithm for more digits, never completed or exhibited; if every number is an algorithm then algorithm, acceptable operations and comparison need rigorous definition; the replacement of exhibitable certificates by faith; only trivial cases are ever used; do it for one of the irrationals; the carry problem — pi+e is a procedure-pair, 2026-10-11; the interval form of the carry problem, the aim of the charge in section 3, and the cautions, adopted 2026-11-04) + ai-synthesis (the three meanings of exhibiting, the computability facts, the worked examples, the ladder, the guard sentence)"
sources: "[[Mathematics 1730 to 1900]], [[Number Hierarchy]], [[Certificates]], [[Equal Signs]], [[Christians and the Reals]], [[Diagonal Argument]], [[Bolzano-Weierstrass Theorem]], [[Fundamental Theorem of Algebra]]"
updated: 2026-10-11
---

# Exhibiting a Real

**Murphy's challenge.** A Dedekind cut for $\sqrt2$ does not exhibit $\sqrt2$. It defines a procedure for producing more and more digits, which by its nature can never be completed or shown. If the claim is that *every number is an algorithm*, then "algorithm", the acceptable operations and an air-tight way of comparing algorithms all need rigorous definitions, or the matter is "passing the buck". The buck was in fact passed to the axiom of choice and similar principles. The replacement of exhibitable certificates by faith varies from object to object, and **only the trivial cases are ever used**. Given the "greater infinity" of irrational reals: *do it for one of them.*

This page answers each part, and corrects an overstatement in [[Mathematics 1730 to 1900]].

A guard on the challenge, from [[Creaturely Realism]]: *show me* does not mean *put the object in my hands* — no one has seen twoness either. It means *show me your certificate of access*. The distinction that does the work is **complete versus partial exhibition**: two fingers exhibit twoness completely; every exhibit of $\pi$ is a $\pi_n$, partial by construction. Under that reading the challenge cannot be turned aside by pointing at the symbol $\pi$ — a pointer is not an exhibit.

## 1. What "exhibiting $\sqrt2$" can mean

Three different things go by the name, and only one of them is a *digit procedure*:

| Meaning | What is held | Finite? | Verdict |
|---|---|---|---|
| **A length** | the diagonal of a unit square, constructed | yes | exact; the Greek and vault sense ([[Constructible Numbers]]) |
| **An equation with an isolating interval** | $x^2-2=0$ and $[1.41421356,\ 1.41421357]$ (checked: the squares are $1.99999999\ldots$ and $2.00000002\ldots$, either side of $2$) | **yes**, a finite exact object | exact: arithmetic in $\mathbb Q(\sqrt2)$ is finite and decidable ([[Fundamental Theorem of Algebra]], [[Exact Until Output]]) |
| **Digits** (a cut, a Cauchy sequence, a decimal) | a rule that yields digits on demand | **never completed** | a *convergence certificate*, Group C of [[Number Hierarchy]] |

**So the objection holds against the cut and not against $\sqrt2$.** The cut is the third meaning, and it cannot exhibit anything. $\sqrt2$ is exhibited by the first two, which are finite. The earlier page said the vault "accepts a cut given by a rule" as a convergence certificate; that is correct *as a label* and wrong if it suggests the cut exhibits the number. For an algebraic number the **right** certificate is the finite one; the cut is a way of printing digits ([[Equal Signs]]: $(\sqrt2,\text{length})$ is exact; $(\sqrt2,\text{decimal})$ is not).

## 2. If a number is an algorithm: the definitions exist, and the comparison cannot be made air-tight

The definitions are not missing; they are a whole field. [AI; from recollection, to check]

- **Algorithm:** Turing's machines (1936; his paper was about *computable numbers*), recursive functions, the Church–Turing thesis.
- **Computable real:** a real whose digits (or a rational approximation to any stated precision) a machine produces. Bishop's *constructive reals* are regular Cauchy sequences **with an explicit modulus**. Weihrauch's computable analysis fixes the model for functions on the reals.
- **Acceptable operations:** the field operations, roots, and the elementary functions are computable; limits are computable only **with a modulus**.

**And the comparison problem has a negative answer, which is a theorem.**

- Computable reals are **countable** (programs are listed), so they are **not** all the reals.
- **Equality of two computable reals is undecidable** (the zero-test problem; Richardson and others). One can only certify *difference* (strict inequality is semi-decidable: it shows itself when it holds).
- A computable sequence with no computable limit exists: **Specker's sequence** ([[Bolzano-Weierstrass Theorem]]).

So Murphy's demand for an "air-tight method for comparing them" cannot be met in general, and that fact is **why the vault insists on a certificate relative to a representation** ([[Certificates]], [[Equal Signs]]). Two worked illustrations (computed):

1. **Digits cannot decide equality.** The number $e^{\pi\sqrt{163}}=262537412640768743.99999999999925\ldots$ is **$7.5\times10^{-13}$ short of an integer**: twelve nines and then a difference. A machine comparing it to $262537412640768744$ by digits must run past the twelfth place before it can say they differ; had the nines continued, no finite run would show equality. (That it is *not* an integer rests on a theorem about transcendence, not on digits.) Similarly $e^\pi-\pi=19.99909997\ldots$ looks like $20$.
2. **An equality that encodes an open problem.** Let $G=\sum_k2^{-k}[\text{the $k$th even number is a counterexample to Goldbach}]$. Every term is computable and checked to $20{,}000$ shows no counterexample, but "$G=0$" **is Goldbach's conjecture**. No algorithm that *compares* $G$ to $0$ exists unless the conjecture is settled.
3. **The carry problem: $\pi+e$ is a procedure-pair, not an answer (Murphy).** Feed two digit-machines into a summer and even the first decimal digit of the sum can depend on digits not yet examined: $0.4999\ldots+0.0000\ldots$ lands just below or just above $0.5$ according to a tail no one has computed, so no finite prefix of the inputs settles whether the sum begins $0.4$ or $0.5$. Hence Murphy's charge that the system **fails at step 1, addition**: ask for $\pi+e$ and the answer comes back "$\pi+e$". The precise form: addition of algorithm-given reals *is* exhibitable as an **interval algorithm** (add the procedures; nested rational intervals come out — a pixel machine, and at every stated resolution the sum is decided); what fails is **canonical form and equality** — a *decimal* for the sum cannot always be printed digit-certain, and whether two sums are equal is undecidable (above). So the exhibitable arithmetic of the reals is certified procedures on rationals, constructibles and intervals, whose "=" is the four pixel clauses of [[Certificates]]; "$\pi+e$" names a procedure-pair, and only under a named convention is it an answer.

## 3. What classical ℝ actually claims, and where the buck went

The classical real line does **not** say every real is an algorithm. It says every real is an **arbitrary** cut or Cauchy sequence, an object carrying infinite information with **no rule required**. Almost all such objects are not computable (the computable ones are countable), and almost all are not even definable. So:

- The charge of "sloppy computer science" is **fair in effect and slightly mis-aimed**: classical analysis does not *claim* algorithms; the *practice* of "keep taking more digits" imports an algorithmic picture, while the *definition* is a completed infinite set. The equivocation between the two is the **bamboozlement** ([[Certificates]]).
- The buck is passed to **set theory and the axiom of choice**, which supply **existence without an instance**: a well-ordering of the reals; a basis of the reals as a vector space over the rationals (a Hamel basis); non-measurable sets of reals (Vitali); the Banach–Tarski decomposition. **No explicit example of any of these exists**; and it is consistent with the axioms (without full choice) that all sets of reals are Lebesgue measurable (Solovay, 1970; recollection), so no explicit non-measurable set can be proved to exist from the weaker axioms.

## 4. "Do it for one of them": what can be named

The ladder of the most the profession can actually *show*, from the best to nothing:

| Real | What shows it | Status |
|---|---|---|
| $\sqrt2$ and every algebraic number | a finite equation plus an isolating interval, or a constructed length | **exhibited** (finite, exact) |
| $\pi$, $e$ | a **geometric** definition (circumference over diameter; the area under $1/x$) and bracketing by rationals with proof ([[Exact Until Output]]: Archimedes' 96-gon gives $3.14103<\pi<3.14272$) | exhibited **geometrically**, digits by procedure |
| **Liouville's constant** $\sum10^{-k!}=0.110001000000000000000001\ldots$ (transcendental) | a rule for each digit | computable, by a rule |
| **Champernowne's constant** $0.123456789101112\ldots$ (shown normal in base ten, as I recall) | a rule for each digit | computable, by a rule |
| **Chaitin's $\Omega$**, or $\sum2^{-k}[\text{program $k$ halts}]$ | a *definition* | **definable but not computable**: its digits cannot be produced; it is shown only as a description (hierarchy Level 12) |
| **A typical real** | **nothing** | cannot be named |

**The last row is not an accident.** There are only countably many finite descriptions, so to *name* a real is to put it among a countable collection. Hence **it is impossible to exhibit an example of a typical real**: to give it is to define it, and the definable reals are not typical. So the "greater infinity of irrational reals" is, in the precise sense of your challenge, **a claim about objects no one can show**. The ladder above, ending in $\Omega$, is exactly levels 5 to 12 of [[Number Hierarchy]]; the hierarchy is the honest answer to "do it for one", and below Level 12 there is nothing to point to ([[Diagonal Argument]]: the argument is a procedural negative, not a way of reaching those reals).

**A caution on "undefinable"**: "definable" depends on the language, and "almost all reals are undefinable" is a statement made *inside* set theory. By Skolem-type results there are countable models of set theory in which every real is definable (recollection), so the claim is not absolute. The vault does not need it; the claim above (that one cannot exhibit a typical real) stands as the procedural statement.

## 5. Only the trivial cases are used

True of applied mathematics and almost true of analysis: every real that appears in a calculation, a theorem's example or a physical measurement is **computable**, nearly always an algebraic number, $\pi$, $e$, or a value of an elementary function. The **non-computable** reals appear only in existence arguments (and in the logic of computability itself). There is a body of work suggesting that scientifically applicable analysis needs only a small, predicative fragment: **Weyl** (*Das Kontinuum*, 1918) and **Feferman** ("Why a little bit goes a long way", 1993, as I recall) argue that the mathematics used in science is conservative over weak arithmetic. If so, the completed ℝ is **not needed by the sciences**, and Murphy's "trivial cases" observation is the empirical side of that result. *(To check against the texts.)*

## What this does to the vault's wording

- A cut or Cauchy sequence **by rule** is a **convergence certificate** (Group C): it never exhibits and never completes.
- Where an **algebraic** or **geometric** exhibit exists (length; equation and interval), **that** is the certificate, and it is finite.
- **Equality** between numbers represented by procedures is **not decidable**; the vault's certificate for equality is representation-relative and exact only inside $\mathbb K$ and $\mathbb K[\pi]$.
- Everything past Level 12 has **no exhibit**, and the vault says so.

## Hard problems

1. **A feasible notion of "algorithm".** "Computable" allows astronomically long computations; the vault's budget forms ask for a **cost**. A rigorous account of reals computable in polynomial time exists (Ko and Friedman, 1982; recollection), and the vault needs the corresponding notion of comparison with a stated budget.
2. **Whether "every number is an algorithm" is a thesis anyone holds.** The constructive schools hold a version (reals as procedures with a modulus). The vault should say which authors, and what they accept as operations.
3. **The scope of Feferman's result** (above) is cited from recollection and is the single most useful result to verify.
4. **A short demonstration for students.** The almost-integer and the Goldbach real are suitable.
