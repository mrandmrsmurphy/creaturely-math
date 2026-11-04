---
title: Fundamental Theorem of Algebra
type: theorem
status: canonical (the standard statement rejected as stated; the exact parts kept; a budget form stated)
provenance: "murphy (the position, reject as stated, solutions displayed to a rounding given a budget of time and space; what is exact, the budget form's checkable statement, the space point, the hyper-Catalan level and the stopping-test pair, adopted 2026-11-04) + ai-synthesis (the worked example, the flagged problems) + third-party (Wildberger and Rubine, 2025, restated)"
sources: "[[Certificates]], [[Number Hierarchy]], [[Creational Ultrafinitism]]"
updated: 2026-10-09
---

# Fundamental Theorem of Algebra

> **Standard statement.** Every non-constant polynomial with complex coefficients has a root in $\mathbb C$; a polynomial of degree $n$ has exactly $n$ roots, counted with multiplicity.

## What is rejected, and why

As stated it is rejected, for three reasons.

1. **The roots are not displayed.** The statement asserts that a root *exists* in $\mathbb C$, a field built on the completed real line. The standard proofs (Argand's minimum of $|p|$; Liouville; the winding number) lean on completeness and compactness, and none hands you the root. For a certificate-explicit position this is an existence claim with no exhibited object ([[Certificates]]).
2. **There is no closed form.** The roots of the general polynomial of degree 5 or more cannot be written with radicals (Abel–Ruffini; [[Glossary]], "Galois boundary"). "The roots" are then names, not numbers one holds.
3. **Scale.** See "Space" below: even when each root is held, *all the roots at once* can be past the threshold.

## What is exact and stays

Several parts of the theorem survive intact. Each is finite, rational and certified.

**At most $n$ roots.** If $p(a)=0$ then $p(x)=(x-a)q(x)$, since $x^k-a^k$ is divisible by $x-a$ for each $k$. So a polynomial of degree $n$ over *any* field has at most $n$ roots: divide out a root and repeat, at most $n$ times. This is the half of the theorem that is just algebra.

**A root can always be adjoined, exactly.** If $p$ is irreducible over $\mathbb Q$ of degree $n$, then $\mathbb Q[x]/(p)$ is a field in which $p$ has a root (the class of $x$), with arithmetic done on lists of $n$ rational numbers. This is Kronecker's construction. The root is held *as a name with exact arithmetic*, a finite object ([[Modular Arithmetic]] does the same for $\mathbb Z/p$).

**Over a finite field the theorem is exact and finite.** $x^2+1$ over $\mathrm{GF}(5)$ is $(x-2)(x-3)$ because $2^2=4\equiv-1$: the roots are $2$ and $3$, displayed with no rounding. Over $\mathrm{GF}(3)$ and $\mathrm{GF}(7)$ it has no roots, since $-1$ is not a square; it splits in the extension of degree 2 ($\mathrm{GF}(9)$, $\mathrm{GF}(49)$). See [[GF(3)]], [[GF(5)]], [[GF(7)]].

**Counting is exact.** Equal roots are separated by rational arithmetic ($\gcd(p,p')$ gives the repeated part). Sturm's theorem counts the real roots in an interval, and the Routh–Hurwitz criterion counts those in a half-plane, using only the coefficients. *(Unverified recollection to check: both are standard, and are the certificates meant here.)*

## The budget form

The honest replacement, in Murphy's words, is that polynomials can have their solutions *displayed up to a given rounding, within a budget of time and space*. Stated so it can be checked:

> **Budget form.** Given a polynomial $p$ of degree $n$ with rational coefficients and a precision $10^{-k}$, one can produce $n$ disjoint discs (rational centre, radius at most $10^{-k}$) and a certificate that each contains exactly one root, counted with multiplicity. The cost is a stated number of rational operations on numbers of a stated size, growing with $n$ and $k$.

The certificate has two layers:

- **Exact:** the pair ($p$, a disc) *names* one root. It is a finite object (compare the reduced pair $(a,b)$ of [[Number Hierarchy]] level 4, which names a rational), and *equality of two such roots is decidable* (same minimal polynomial, overlapping discs). The digits are not exhibited by it.
- **Rounded:** digits on demand, at a cost, by shrinking the disc.

**Worked example: Wallis's cubic** $p(x)=x^3-2x-5$ (Newton's own illustration).

*Certificate of a root.* $p(2)=-1<0$ and $p(2.1)=0.061>0$, and $p'(x)=3x^2-2>0$ on the interval, so $p$ is strictly increasing there. The interval therefore holds at most one root, and the pair ($p$, interval) names it ([[Intermediate Value Theorem]]); and halving it by sign tests gives a nested sequence of rational intervals closing on it. That nested sequence, with its sign tests, is the certificate; no appeal to completeness is made.

*Bisection* (one binary digit per step, exact rationals):

| step | 1 | 2 | 3 | 4 | 5 | 6 |
|---|---|---|---|---|---|---|
| interval | $[2.05,\,2.1]$ | $[2.075,\,2.1]$ | $[2.0875,\,2.1]$ | $[2.09375,\,2.1]$ | $[2.09375,\,2.096875]$ | $[2.09375,\,2.0953125]$ |

*Newton* from $2$ (digits roughly double each step; errors against the true root $2.0945514815423265915\ldots$):

| step | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| value | $2.1$ | $2.094568121\ldots$ | $2.094551481698\ldots$ | $2.0945514815423265\ldots$ |
| error | $5\times10^{-3}$ | $1.7\times10^{-5}$ | $1.6\times10^{-10}$ | $3.9\times10^{-21}$ |

Newton alone carries no digit guarantee; **Newton inside a bisecting interval does** (accept a Newton step only if it stays in the certified interval). The sign-change certificate is what upgrades the digits from "agree with a computer" to *guaranteed*.

**A degree-5 case with no radical solution.** $x^5-x-1$ has $p(1.16)\approx-0.0597$ and $p(1.17)\approx0.0224$, so a root lies in $[1.16,1.17]$ (and $p'=5x^4-1>0$ there, so exactly one); its Galois group is the full symmetric group $S_5$, so no radicals. The budget form works with the same certificate. *(Unverified recollection: that this group is $S_5$ is the standard example.)*

## Wildberger and Rubine's series [third-party, restated]

Wildberger and Rubine (*American Mathematical Monthly* 132:5, 2025, pp. 383–402, "A Hyper-Catalan Series Solution to Polynomial Equations, and the Geode") show that the equation $0=1-\alpha+t_2\alpha^2+t_3\alpha^3+\cdots$ has a **formal power series** solution whose coefficients are the hyper-Catalan numbers (counts of subdivisions of a polygon into triangles, quadrilaterals, pentagons, …), and that this solves the general polynomial equation after a change of variables. It gives a uniform formula for all degrees, without radicals. It fits this vault: it is an algebraic, combinatorial, anti-transcendental solution (the Guidelines of [[Future Directions]], item 1).

The paper's own example is Wallis's cubic, and it shows both the use and the caution:

- The series cut off at degree 3 applied directly to $x^3-2x-5$ gives $-999.08$: **useless**, because the series is outside its convergence.
- Shift the variable by the guess $x=2$ (a certified isolating start) and apply it to $g(x)=-1+10x+6x^2+x^3$: the first terms give $0.0945345708$, so the root $\approx2.0945345708$ (error $1.7\times10^{-5}$).
- Feed that back in ("bootstrapping") with the truncated guess $2.0945$: $2.0945514815423265098\ldots$, agreeing with the true root to 16 places.

(I recomputed the first two values with exact rationals: $-999.08203125$ and $0.0945345708$.)

**In the vault's terms**: the series is a *formal* solution; to *hold a root* it needs a **convergence certificate** for the values plugged in, and the paper itself lists "the conditions for convergence" as an open question. A root given by such a series sits at Level 10, *Series: the summation process is the certificate* ([[Number Hierarchy]]), until a radius of convergence is proved for the case at hand. The sign-change certificate above is the independent check on the answer.

## Conditioning: the budget includes the coefficients

The budget form asks for $p$ *exactly*. If the coefficients are themselves known only to a precision, the roots may not be fixed to anything like that precision. A checkable instance: $(x-1)^{10}=10^{-10}$ has the ten roots $1+0.1\,\zeta$, with $\zeta^{10}=1$. A change of $10^{-10}$ in one coefficient moves a root by $0.1$: **nine of ten digits are lost.** *(Unverified recollection to check: Wilkinson's polynomial $\prod_{j=1}^{20}(x-j)$ is the classical, far more dramatic example, where a tiny change of one coefficient turns real roots complex.)* So "to precision $10^{-k}$" must say whether it refers to exact coefficients or to measured ones.

## Space

Each root is held in a field of degree $n$ over $\mathbb Q$. All roots *together* live in the **splitting field**, whose degree is $n!$ when the Galois group is the full $S_n$ (the generic case). Then:

$$120!\approx6.7\times10^{198}<10^{200}<121!\approx8.1\times10^{200}.$$

So for a generic polynomial of degree $121$ the splitting field is already of dimension past the threshold ([[Creational Ultrafinitism]]): "all the roots, as one exact algebraic object" is notation, not something held, while each root, one at a time, is. This is a concrete form of the space budget.

## Level 8 as a Pixel

[[Number Hierarchy]] level 8 (Algebraic, $\mathbb A$) is a Pixel: Newton's method on $p$, run until the desired resolution is reached. **That run is the certificate** (Murphy).

A run certifies a digit only if it ends with a stopping test that proves the error bound, so the certificate is the pair ($p$, isolating interval or disc), refined by bisection (one guaranteed binary digit per step) with Newton as the speed-up used inside the interval; bare Newton with no such test reports a pixel without proof.

What is exact is the **name**, a finite piece of data. The number's digits are never exhibited; they are given on demand, at a cost. Two consequences:

- Digits are guaranteed for any algebraic number, so "no guarantee" describes the *method*, not the level.
- Equality of algebraic numbers is decidable. That holds for *every* algebraic number, including levels 5 to 7, so it does not separate level 8 from them.

The lines between levels 5, 6, 7 and 8 are about *how the number is obtained* (construction, folding, a digit algorithm, an iteration on a polynomial).

## The theorem in the literature [AI, unverified]

Constructive proofs of the fundamental theorem of algebra exist (recollections: Weyl 1924, with a subdivide-and-exclude algorithm; Brouwer, Kneser and others in the constructive literature; and near-optimal root-finders, Pan 2002). If right, the objection to the standard statement is **not** that no constructive form exists; it is that (a) the standard proofs are not those, (b) "exists in $\mathbb C$" says nothing about a budget, and (c) the cost is a function of $n$ and $k$ that the theorem hides. Check before citing.

## Hard problems

1. **The cost function.** State the budget form with a proved cost in $n$ and $k$ (and coefficient size), not just "polynomial". Sign-change bisection costs about $3.3k$ evaluations of $p$, each $n$ multiplications; the size of the rationals grows. A real statement needs a theorem.
2. **Complex roots.** The worked example is real. Complex roots need discs in the plane and a certificate that each disc holds exactly one root (an exclusion/inclusion test, or counting by the argument principle without angles). The vault avoids angle measure; how to count roots in a disc without it is open.
3. **Multiplicity and near-multiplicity.** With exact rational coefficients, $\gcd(p,p')$ separates repeated roots exactly. With the budget form, a cluster of roots closer than $10^{-k}$ is one disc: say what the certificate then claims.
4. **The series.** A radius of convergence for the hyper-Catalan series, in terms of the coefficients, and a cost for "bootstrapping" ([[Future Directions]] item 1).
5. **Level 8.** What the stopping test is for each of the root-finding methods, complex roots included.
