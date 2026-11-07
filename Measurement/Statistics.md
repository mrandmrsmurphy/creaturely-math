---
title: Statistics
type: concept
status: "stub (the stance and a few checked examples; the course is unwritten)"
provenance: "murphy (the direction, statistics is what most students get at the end of mandatory schooling; the $p$-value teaching decision; the foundation/framework distinction — design-based foundational, finite Bayesian primary) + ai-synthesis (the stance, the examples, the flagged problems)"
sources: "[[Historical Order]], [[Curriculum Plan]], [[Future Directions]], [[Certificates]], [[Theological Grounds]]"
updated: 2026-11-07
---

# Statistics

For most students, the last mathematics of mandatory schooling: how to say what a body of numbers shows, and **how sure one is.** *Statistics for Everyone* and *Infinity and Uncertainty* are unwritten ([[Curriculum Plan]]); this page records the stance so the course has something to stand on ([[Future Directions]] item 13).

## Why it suits the position

Statistics is the place where the vault's two rules are tested daily:

- **Every claim needs a warrant** ([[Certificates]]). A statistic reported without its error is a false balance (Lev 19:35–36; Prov 11:1; [[Theological Grounds]]).
- **Do not claim to know what one cannot** ([[Christians and the Reals]], the ethical form). To state an uncertainty honestly is the practical form of epistemic humility.

The counting and rules this rests on are on [[Probability]].

## Two halves

| | What it is | Certificate |
|---|---|---|
| **Describing** | counts, tables, means, medians, spread | **exact**: arithmetic on the data |
| **Inferring** | what a sample says about a larger whole | **a stated bound**, with its assumptions named |

Keeping the halves apart is half the course. The mean of a list is a computed number; what it says about a population is a claim with an error.

**The mean as a balance point** (exact): for $1,2,2,9$ the mean is $3.5$ and the deviations from it sum to $0$. The median is $2$; the difference is the lesson in skew.

## Finite populations, exact sampling

A population is a finite list, and samples of it are finite, so the **sampling distribution can be written out** in small cases. Take the population $2,3,5,7,11,13,17,19,23,29$ (mean $12.9$). There are $\binom{10}{3}=120$ samples of size $3$. Their means range from $\tfrac{10}3$ to $\tfrac{71}3$; the mean of all the sample means is exactly $12.9$; and $59$ of the $120$ samples (about $49\%$) have a mean within $3$ of the population mean (all computed). So a sample of three tells little, and the table says how little, with no approximation. Larger cases use the same logic with more arithmetic.

## Tools, in order of what they assume

1. **Counting and the binomial distribution:** exact. ($\tfrac{63}{256}$ for exactly 5 heads in 10; [[Historical Order]].)
2. **Chebyshev's inequality:** valid for any distribution with a given spread. For $n$ fair flips the fraction of heads is off by $\varepsilon$ or more with probability at most $\dfrac1{4n\varepsilon^2}$.
3. **Hoeffding's inequality** (statement from recollection, to check): $2e^{-2n\varepsilon^2}$, which uses only that each outcome lies in $[0,1]$.
4. **The normal approximation:** an approximation with an error. Its error (the Berry–Esseen theorem, to check) is the reason to say "approximately".

**Worked example: a poll.** A sample of $n=400$ gives $220$ yes, so $\hat p=0.55$. Half-widths of an interval built to cover the true proportion at least $95\%$ of the time:

| method | half-width |
|---|---|
| Chebyshev | $0.112$ |
| Hoeffding | $0.068$ |
| normal approximation | $0.049$ |

(computed). The guaranteed methods are wider, the approximate one narrower; the price of not assuming a shape is width. A student sees what each assumption buys. The same sample therefore supports "about $55\%$, give or take $11$ points for certain, give or take $5$ if the approximation holds."

For $n=1000$, $\varepsilon=0.05$ the three bounds on the chance of a miss are $\le0.1$ (Chebyshev), $\le0.0135$ (Hoeffding), and the exact tail is $0.0017$ (all computed): true, loose, and tightening with assumptions.

A development that takes finite data, rational moments, quadrance and exact counting as primary, with the Gaussian as an optional approximation, is on [[Constructible Statistics]].

**$p$-values, as taught (Murphy).** Significance tests enter the course only in their exact, combinatorial form — the permutation test and Fisher's exact test, where $p$ is a ratio of counts and the probability comes from the randomization the experimenter performed ([[Constructible Statistics]]). The main instruments are the intervals and bounds above. The $0.05$ ritual is named as a custom to be read with suspicion, not practised: students will meet $p$-value claims in journalism and medicine, and they should be able to audit one — to ask for its certificate. A $p$-value sold as "the probability the null is true" is a false balance.

**Foundation and framework (Murphy).** Design-based probability is the foundation: its probabilities are grounded in an actual finite randomization that can be enumerated and counted. Bayesian inference is the primary inferential framework, in its finite form — enumerated hypotheses, rational priors and likelihoods, exact arithmetic, every prior carrying a justification ([[Constructible Statistics]], "Design-based and Bayesian"). The two answer different questions over the same finite space, and students must not slide between their two meanings of probability.

## Hard problems

1. **Continuous distributions.** The normal density and the integral under it are idealisations. Under the position they are approximations to finite sums with named error ([[Calculus]], [[Fundamental Theorem of Calculus]]).
2. **Infinite populations and limits.** Statements "as $n\to\infty$" need to be replaced by the finite bound above.
3. **Randomness.** What a sequence must be to count as random is deferred.
