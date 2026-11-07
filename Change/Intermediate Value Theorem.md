---
title: Intermediate Value Theorem
type: theorem
status: "canonical (the exact statement rejected; the approximate form with a modulus kept)"
provenance: "murphy (the position, reject as is, results found to a specified precision and not infinitely so; the three further reasons, adopted 2026-11-04) + ai-synthesis (the algorithm, the cost, the example, the flagged problems)"
sources: "[[Calculus]], [[Certificates]], [[Number Hierarchy]], [[Creational Ultrafinitism]]"
updated: 2026-10-09
---

# Intermediate Value Theorem

> **Standard statement.** If $f$ is continuous on $[a,b]$ and $f(a)<0<f(b)$, then there is a number $c$ in $[a,b]$ with $f(c)=0$.

## What is rejected

The exact statement is rejected, because the $c$ it promises is a **real number** in the completed sense, and the vault does not hold such objects ([[Certificates]], [[Number Hierarchy]]). The standard proof takes $c=\sup\{x: f(x)<0\}$, the least upper bound of an infinite set: a completeness argument that hands you no number. The only honest content is *how close you can get, for how much work*.

Three further reasons:

1. **There is no procedure behind it.** For a general continuous $f$ no method can output the exact zero. Here is a construction (mine) of the failure. Let $r$ be a number given by an unsolved search, with $r=0$ if the search never succeeds and $r=\pm2^{-m}$ if it first succeeds at step $m$ (sign by the parity of $m$). Let $g$ be $x-\tfrac13$ for $x\le\tfrac13$, $0$ on $[\tfrac13,\tfrac23]$, and $x-\tfrac23$ for $x\ge\tfrac23$, and put $f=g+r$, so $f(0)<0<f(1)$ whatever $r$ is. The zero lies at $\tfrac13-r$ (left of $\tfrac13$) if $r>0$, anywhere in $[\tfrac13,\tfrac23]$ if $r=0$, and at $\tfrac23+|r|$ (right of $\tfrac23$) if $r<0$ (checked on a grid for $r=\pm\tfrac1{10},0$). Computing the zero *exactly* would decide the sign of $r$, that is, solve the search. *(Unverified recollection to check: in the constructive literature the exact statement is known to be equivalent to a weak omniscience principle, LLPO, and so is not provable without excluded middle.)*
2. **The cost is hidden.** "There exists $c$" says nothing about how many steps get you within $10^{-6}$.
3. **"Continuous" is too weak to cost anything.** The pointwise $\varepsilon$–$\delta$ definition promises a $\delta$ for each point and gives no way to find it. On $[a,b]$ the classical remedy is uniform continuity by compactness (Heine–Borel), itself a completeness theorem. Here continuity is taken **with a modulus**, as a certificate (below).

## What stays: the approximate form

**Continuity with a modulus.** $f$ is continuous on $[a,b]$ *with modulus* $\delta(\varepsilon)$ if $|x-y|\le\delta(\varepsilon)\Rightarrow|f(x)-f(y)|\le\varepsilon$, with $\delta$ a given function. This is a certificate in the sense of [[Certificates]]. For a differentiable $f$ it comes from [[Calculus]]: if $|f'|\le L$ on $[a,b]$ then $\delta(\varepsilon)=\varepsilon/L$. For a polynomial $L$ is computed from the coefficients.

> **Approximate IVT (budget form).** Let $f$ be continuous on $[a,b]$ with modulus $\delta$, and $f(a)\le0\le f(b)$. For every $\varepsilon>0$ one finds a rational $x\in[a,b]$ with $|f(x)|\le2\varepsilon$ in
> $$k=\lceil\log_2\rceil\Bigl(\frac{b-a}{\delta(\varepsilon)}\Bigr)$$
> bisection steps, each needing $f$ at one point to precision $\varepsilon/2$.

**The step count $\lceil\log_2\rceil$.** For a rational $x>0$, $\lceil\log_2\rceil(x)$ is the **least integer $k\ge0$ with $2^k\ge x$**: the number of times to double $1$ before it reaches $x$, or the number of times to halve $x$ before it is at most $1$. The brackets enclose the word and are one symbol; it is a function from the positive rationals to the natural numbers, defined by a finite search, with no real numbers and no logarithm in it. (It agrees with the ceiling of the real $\log_2$, but is defined without it. For a whole number $n\ge1$ it is the number of binary digits of $n-1$.) Values: $\lceil\log_2\rceil(1)=0$, $(2)=1$, $(3)=2$, $(4)=2$, $(400)=9$, since $2^8=256<400\le512=2^9$. It is the **number of bisections**, which is what $k$ counts.

**The algorithm.** Keep an interval $[a,b]$ with $f(a)\le\varepsilon$ and $f(b)\ge-\varepsilon$. At the midpoint $m$, compute an approximation $v$ of $f(m)$ within $\varepsilon/2$. If $v\ge0$ then $f(m)\ge-\varepsilon/2$: replace $b$ by $m$. If $v<0$ then $f(m)<\varepsilon/2$: replace $a$ by $m$. Both tests are decidable on the approximation, and no step asks whether $f(m)$ is *exactly* zero. Stop when $b-a\le\delta(\varepsilon)$.

*Why it works.* At the end $f(a)\le\varepsilon$ and $f(a)\ge f(b)-\varepsilon\ge-2\varepsilon$ (modulus), so $|f(a)|\le2\varepsilon$. $\square$

**Worked example.** $f(x)=x^2-2$ on $[1,2]$, $\varepsilon=\tfrac1{100}$. Here $|f'|=2x\le4$, so $\delta=\tfrac1{400}$ and $k=\lceil\log_2\rceil(400)=9$:

| step | $a$ | $b$ | $f(a)$ | $f(b)$ |
|---|---|---|---|---|
| 1 | $1$ | $1.5$ | $-1$ | $0.25$ |
| 2 | $1.25$ | $1.5$ | $-0.4375$ | $0.25$ |
| 3 | $1.375$ | $1.5$ | $-0.1094$ | $0.25$ |
| 4 | $1.375$ | $1.4375$ | $-0.1094$ | $0.0664$ |
| 5 | $1.40625$ | $1.4375$ | $-0.0225$ | $0.0664$ |
| 6 | $1.40625$ | $1.421875$ | $-0.0225$ | $0.0217$ |
| 7 | $1.4140625$ | $1.421875$ | $-0.00043$ | $0.0217$ |
| 8 | $1.4140625$ | $1.41796875$ | $-0.00043$ | $0.0106$ |
| 9 | $1.4140625$ | $1.416015625$ | $-0.00043$ | $0.0051$ |

Output $x=\tfrac{181}{128}$ with $|f(x)|=0.00043\le2\varepsilon$ (exact rationals, checked). The width is $\tfrac1{512}\le\tfrac1{400}$.

**What precision costs.** Each decimal digit costs between $3$ and $\tfrac{10}3$ steps, since $2^3<10$ and $2^{10}>10^3$ (the bounds are whole-number facts; no logarithm is needed): with $L=4$, $b-a=1$, six digits take $22$ steps, $20$ digits $69$, $50$ digits $169$, $100$ digits $335$. The cost is **linear in the number of digits**, and no number of steps is "all the digits". A *level of precision* is a finite request with a finite answer; the infinite precision the classical theorem promises is not on offer, and the budget ([[Creational Ultrafinitism]]) caps the requests that can be made.

## Where the exact form is recovered

- **Polynomials with rational coefficients.** The sign of $p$ at a rational point is exact, so there is no approximation step, and the sign-change interval of the budget form is *exact data*. A root is then **named** by ($p$, isolating interval), a finite object, and the zero is the algebraic number so named ([[Fundamental Theorem of Algebra]], including the caution about level 8 of [[Number Hierarchy]]). Here the IVT's role is to say that the name is well formed, with strict monotonicity on the interval ($p'$ of one sign) to say that it names only one.
- **Strictly monotone $f$ with a modulus.** If $|f(x)-f(y)|\ge m|x-y|$ (a lower bound on the slope), a root is *computable to any stated precision* by the same bisection, and one can say "the" root without the exact-zero decision. *(Unverified recollection to check: this is the form of the theorem the constructive literature proves.)*
- **Bounded decidable domains.** On a finite lattice $x_0<x_1<\dots<x_n$ the discrete version is exact: if $f(x_0)<0<f(x_n)$ there is a first index $i$ with $f(x_i)<0\le f(x_{i+1})$, found by a finite search ([[Discrete Calculus]]). The sign change lies between two neighbouring lattice points one step apart.

## What it was used for, and the budget version

- **$n$th roots, $\sqrt2$:** by construction ([[Constructible Numbers]]) or by a digit algorithm (level 7 of [[Number Hierarchy]]); bisection is the guaranteed-digit way.
- **Inverse functions** (the logarithm as inverse of the exponential): the same bisection, with the modulus of the exponential.
- **Existence of fixed points of maps of an interval** (the one-dimensional case of Brouwer): bisection on $f(x)-x$.
- **Roots of polynomials:** the budget form of [[Fundamental Theorem of Algebra]].

## Hard problems

1. **The modulus is an input.** The theorem is only as good as the certificate $\delta(\varepsilon)$. Where does it come from for a function *given by a process* (a limit, a series, a solution of an equation)? Another face of the certificate problem ([[Future Directions]] item 3).
2. **Evaluating $f$ to precision $\varepsilon/2$** has its own cost, which grows with the precision and with the function. The step count above counts *evaluations*, not the total work.
3. **No excluded middle.** The algorithm avoids the question "$f(m)=0$?" in favour of two overlapping tests. In SIA ([[Infinitesimals]]) case analysis is also unavailable, and how much of the IVT survives there is not settled here; see [[Calculus]], hard problem 1.
4. **The extreme value theorem, Heine–Borel, Bolzano–Weierstrass** are the same sort of completeness claims; see [[Extreme Value Theorem]]. Finding a maximum costs exponentially more in the digits than finding a zero.
