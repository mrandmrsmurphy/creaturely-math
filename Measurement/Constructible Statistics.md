---
title: Constructible Statistics
aliases:
  - Rational Statistics
type: theory
status: "framework (the objects, seven checked results, the costs, the gaps; not a finished theory)"
provenance: "murphy (the question, can statistics be built on finite datasets, exact moments and counts, quadrances, slopes and explicit finite bounds, with the Gaussian and transcendental functions optional; and the retooling from rational to constructible) + ai-synthesis (the framework, results and examples, all computed in exact arithmetic) + third-party (Wildberger's quadrance and spread, restated)"
sources: "[[Statistics]], [[Exact Until Output]], [[Constructible Trigonometry]], [[Constructible Numbers]], [[Certificates]], [[Creational Ultrafinitism]], [[Fundamental Theorem of Algebra]]"
updated: 2026-10-09
---

# Constructible Statistics

**Question (Murphy):** can statistics be built with, as primary objects, finite datasets, exact moments, quadrances, slopes, exact combinatorial probabilities and explicit finite bounds, while continuous distributions and transcendental functions are optional extensions and not foundations?

**Answer [AI]: yes for the working core, and most of its pieces already exist.** What does not yet exist is the assembly, the quadrance-first teaching, and a clear account of what is given up. "Constructive" means *certificate-explicit* ([[Certificates]]): every statement is a finite computation or a stated bound with an exact certificate.

## Why "constructible" and not "rational"

The first framing kept everything rational, as Wildberger does. The vault's own position ([[Exact Until Output]]) is wider: **radicals are exact numbers** and are kept, and a value is rounded only at the output. So the working field is the constructible field $\mathbb K$ ([[Constructible Numbers]]), and the primitive of angle is the **slope** (the tangent), not Wildberger's spread. The rational core is untouched; what is added is that the following may be held exactly:

- the standard deviation $\sqrt V$ and the $z$-scores $(x-\mu)/\sqrt V$;
- the correlation $r$, and the slope and characteristic length of the data wedge;
- interval endpoints that solve a quadratic.

What remains kept apart is the transcendental ($\pi$, $e$, the Gaussian density), carried as a named symbol or left out.

## The tiers of exactness in a statistic

| Tier | Quantities | Held as |
|---|---|---|
| **Counts** | sample sizes, binomial coefficients, p-values of exact tests | integers and ratios of integers |
| **Rational** | mean, quadrance, variance, covariance, regression coefficients, $r^2$, spread | reduced fractions |
| **Constructible** | $\sqrt V$, $z$-scores, $r$, the slope $m$ and length $\ell$ of the data wedge, quadratic-solution endpoints | an element of $\mathbb K$, rounded only at output |
| **Algebraic, higher degree** | endpoints of exact binomial intervals (roots of high-degree polynomials) | named by a polynomial and an isolating interval, refined on demand ([[Fundamental Theorem of Algebra]]) |
| **Transcendental** | normal density, $\pi$, exponential bounds | named symbols, optional |

## The primary objects

| Object | Definition |
|---|---|
| **Dataset** | a finite list of rationals (a measurement is a rational to a stated precision) |
| **Moments** | mean $\mu=\sum x/n$; central moments $\sum(x-\mu)^k/n$: rational |
| **Quadrance** | squared distance; the **variance is the mean quadrance** from the mean |
| **Standard deviation** | $\sqrt V\in\mathbb K$, held as a root |
| **Spread and slope** | for centred data vectors $u,v$: spread $s=1-\dfrac{(u\cdot v)^2}{Q(u)Q(v)}$ (Wildberger), $r^2=1-s$, and the **slope** $m=\pm\sqrt{\dfrac{1-r^2}{r^2}}\in\mathbb K$ with $r=1/\ell$, $\ell=\pm\sqrt{1+m^2}$ ([[Slope]], [[Characteristic Length]]) |
| **Finite probability space** | a finite set $\Omega$ with $P(A)=|A|/|\Omega|$; sampling models are sets of tuples, subsets or permutations |
| **Finite distribution** | a table (binomial, hypergeometric): integers over a power or a binomial coefficient |
| **Bound** | an inequality whose quantities are exact (rational or constructible), with a certificate for any approximation made |

## Seven results (all computed in exact arithmetic)

### 1. Description is quadrance geometry

For $x=1,2,3,4,5$ and $y=2,1,4,3,5$: means $3,3$; variances $2,2$; covariance $\tfrac85$; slope $\tfrac45$, intercept $\tfrac35$. The correlation is the cosine between the centred vectors, so $r^2=\tfrac{16}{25}$ and the spread is $\tfrac9{25}$ (sum $1$). Total quadrance splits **Pythagorean-style**: $10=\tfrac{32}5+\tfrac{18}5$ (explained plus residual), and $\mathrm{SSR}/\mathrm{SST}=r^2$.

**The slope form [AI].** In the vault's primitive the same quantity is a slope: $m^2=\dfrac{\mathrm{SSE}}{\mathrm{SSR}}=\dfrac{1-r^2}{r^2}$. Here $m^2=\tfrac{18/5}{32/5}=\tfrac9{16}$, so $m=\tfrac34$ and $\ell=\tfrac54=1/r$ (the 3-4-5 triangle; the spread is $\tfrac{m^2}{1+m^2}=\tfrac9{25}$, checked). For $r^2=\tfrac13$ one gets $m^2=2$ and $m=\sqrt2$, held exactly. This $m$ is the slope of the wedge between the two data vectors in $n$-space, *not* the slope of the fitted line (here $\tfrac45$). The sign of $r$ is the sign of $\ell$ and of $m$.

### 2. $z$-scores and comparisons without roots

For $1,2,3,4,5$ the variance is $2$, so the standard deviation is $\sqrt2$ and the $z$-scores are $-\sqrt2,\ -\tfrac{\sqrt2}2,\ 0,\ \tfrac{\sqrt2}2,\ \sqrt2$ **exactly**. And any comparison "is $x$ within $k$ standard deviations of the mean?" is decided by squares: $|x-\mu|\le k\sqrt V\iff(x-\mu)^2\le k^2V$, a comparison of rationals. For the ten-number population ($V=\tfrac{7329}{100}$), exactly $9$ of the $10$ values lie within $1.5$ standard deviations (all but $29$), decided with $\tfrac94V$ and no root.

### 3. Exact sampling theory

Population $2,3,5,7,11,13,17,19,23,29$ ($N=10$, mean $\tfrac{129}{10}$), all $120$ samples of size $3$:

- the average of the sample variances with divisor $n-1$ is exactly $\tfrac{2443}{30}$, which equals the population variance with divisor $N-1$;
- with divisor $n$ it is $\tfrac{2443}{45}$, too small by the factor $\tfrac{n-1}{n}$;
- the variance of the sample mean is exactly $\tfrac{17101}{900}=(1-\tfrac nN)\,S^2/n$.

So the "$n-1$" is a **counting fact about all samples**, not an incantation.

### 4. Tail bounds: Chebyshev in quadrance form, and the moment ladder

Chebyshev needs no root: $P\bigl((X-\mu)^2\ge q\bigr)\le V/q$. Markov's inequality on higher even central moments gives a **ladder** of exact bounds. For $n=1000$ fair flips, $t=50$ (exact tail $0.00173$):

| $2k$ | 2 | 4 | 6 | 8 | 10 | 12 | 14 |
|---|---|---|---|---|---|---|---|
| bound | $0.100$ | $0.0300$ | $0.0150$ | $0.0105$ | $0.00939$ | $0.0103$ | $0.0133$ |

The best rung (here $2k=10$) beats Hoeffding's exponential bound $0.0135$ with polynomial arithmetic only. The $2k=4$ rung used the binomial fourth moment, $187375$ (checked against the direct sum).

### 5. A constructible interval, with guaranteed coverage

Poll: $n=400$, $220$ yes, $\hat p=\tfrac{11}{20}$. Chebyshev, inverted: the set of $p$ with $(\hat p-p)^2\le k^2\,p(1-p)/n$ covers the true $p$ with probability at least $1-1/k^2$ **whatever $p$ is**. For $95\%$, $k^2=20$, and the boundary is the quadratic $420p^2-460p+121=0$, whose discriminant is $8320=64\cdot130$. The endpoints are

$$p=\frac{115\pm2\sqrt{130}}{210}\approx(0.4390,\ 0.6562),$$

**exact constructible numbers**, an interval of half-width $0.1086$ (checked: both endpoints satisfy the equation exactly in $\mathbb Q(\sqrt{130})$, and the miss probability at several true $p$ was far below $0.05$). It is conservative, as Chebyshev always is, and it is the first interval with a closed form in $\mathbb K$ and a proved guarantee, with no normal table.

### 6. A tighter exact interval, when computed

The **exact binomial (Clopper–Pearson) 95% interval** for the same poll has lower end defined by $P(X\ge220\mid p)=\tfrac1{40}$ and upper end by $P(X\le220\mid p)=\tfrac1{40}$. Solving by bisection with exact rational arithmetic: $(0.49978,\ 0.59948)$, i.e. $0.55\pm0.0498$, against the normal approximation $\pm0.049$. Any interval enclosing it, such as $[0.4997,\ 0.5995]$, keeps the guarantee. The endpoints are roots of polynomials of degree $400$, so they are **algebraic and not constructible**: named by an isolating interval and refined on demand, the budget form of [[Fundamental Theorem of Algebra]]. And exactness is cheap: the full binomial tail for $n=10{,}000$, $P(|S-5000|\ge100)=0.04659$, is computed in under a tenth of a second with exact integers. The Gaussian began as a device for hand computation (de Moivre, 1733, to check), and the need has gone.

So the trade is visible: the constructible interval (result 5) is closed-form and wide; the exact binomial interval (result 6) is tight and needs computation.

### 7. Exact tests; the probability comes from the design

*Permutation test.* Group A $=3,5,8$, group B $=1,2,4$: difference of means $3$. Of the $\binom63=20$ ways to split the six values into two groups of three, $4$ give a difference at least as large, so the exact two-sided $p=\tfrac15$. *Fisher's exact test* for rows $3,1$ and $1,3$: one-sided $p=\tfrac{17}{70}$, from the hypergeometric table. Tea-tasting, $4$ right of $4$ among $8$ cups: $\tfrac1{70}$. The p-value is a **ratio of counts**. The probability comes from the *randomization* the experimenter performed, not from an assumed shape of the data.

*A constructible Bayes, optionally.* With a flat prior on a success probability, $\int_0^1p^k(1-p)^{n-k}dp=\dfrac{k!(n-k)!}{(n+1)!}$ is rational (checked for $k=1,n-k=2$: $\tfrac1{12}$), and the predictive probability of success after $k$ of $n$ is $\dfrac{k+1}{n+2}$ (Laplace). The integral over the continuum can be replaced by a sum over a finite grid of $p$ values, which keeps everything exact.

## What the Gaussian becomes

A **named approximation to a binomial table, with an error**, kept as an optional extension. Its three classical jobs have constructible replacements:

1. *Approximating sums of many small effects:* exact convolution (the binomial table) where it can be computed; the moment ladder where not.
2. *Justifying least squares* (Gauss's route used the normal law): the Pythagorean geometry of result 1, and the Gauss–Markov theorem, a statement about variances and covariances only (to check).
3. *Tables for the hand:* obsolete.

## What is given up, or hard [AI]

1. **Robustness.** Squares overweight outliers: for $10,11,9,10,12,10,11,500$ the mean is $71.625$, the median is $10.5$, and the variance is about $26{,}216$. Median and absolute-deviation methods are also finite and exact, though they lack the Pythagorean decomposition.
2. **Cost of exactness.** Enumerating all permutations is exponential in general. Polynomial dynamic programmes exist for some rank tests (to check), and otherwise one samples permutations, with a rational error bound of its own.
3. **Looseness of bounds.** The best rung of the ladder was about five times the exact tail, and the Chebyshev interval is about twice as wide as the exact one. Exact computation is better where it is feasible; closed forms are better for a classroom.
4. **Continuous measurement and densities.** Data are rationals of finite precision, so the discrete model is the honest one; densities become optional approximations. A treatment of "the data is $5.3\pm0.05$" as an interval is not written.
5. **Asymptotic theory.** Results such as the asymptotic normality of estimators have no immediate finite form; each needs a bound with a rate.
6. **Where randomness comes from.** The design-based approach requires a randomizing act (a shuffle, lots), a physical process with its own certificate; the deeper question of what makes a sequence random is deferred.
7. **Population.** Classical inference imagines an infinite hypothetical population. Here it is a finite list (survey sampling) or the randomization itself.
8. **Nested radicals grow.** For many-variable statistics the $\mathbb K$ expressions can become large; a size budget is not stated ([[Exact Until Output]], hard problem 1).

Two features favour the position [AI]: a finite dataset **always has a finite variance** (the infinite-variance pathologies of the Cauchy law arise only in infinite models), and every statement is decidable, so classical logic is safe throughout ([[Future Directions]] item 7).

## Related work (all from recollection, to check; no claim of novelty)

Fisher's randomization and exact tests and Pitman's permutation tests (1930s); Neyman and Cochran on design-based survey sampling; **algebraic statistics** (Diaconis and Sturmfels, 1998); Nelson, *Radically Elementary Probability Theory* (1987); Shafer and Vovk, *Probability and Finance: It's Only a Game!* (2001); de Finetti on finite additivity; Wildberger on quadrance and spread; the Wilson score interval, which has the same quadratic shape as result 5 with a normal quantile in place of $k$. The item to search is a text that teaches introductory statistics in quadrance and exact counts from the start.

## Next steps

1. A short list of the minimal theorems with proofs (results 1–7 are candidates).
2. A derivation of the Gaussian as a named approximation of the binomial, with an explicit error.
3. A closed form for the best rung of the ladder.
4. The quadrance-first course: squared $z$-scores, Chebyshev in quadrance form ([[Statistics]]).
5. Intervals for measured data.
