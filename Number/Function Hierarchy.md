---
title: Function Hierarchy
type: hierarchy
status: canonical (draft)
provenance: "murphy (the idea that the number hierarchy carries over to functions; levels 1–4 are combinations of arithmetic, 5 adds square roots, 6 cube roots, and so on; rational-to-rational functions are the safe ones; a polynomial is an exact function and its Pixel nature appears only when one solves; a transcendental is a limit, a level 10 or 11 number, for every input; two axes, the certificate of the operations and the computational cost to a given pixel range; Pixel inputs are not worth considering in rating the function, since in practice every input is rounded first; inverses are harder than modern mathematics credits, as $2^?=6$ shows; an answer is a sum of parts of different standing and each part is to be labelled with its level, not given a name of its own) + ai-synthesis (the inverse-problem reading of levels 5–8, the definition of a function's level as the highest level its values reach, the worked checks, the sensitivity note, the hard problems)"
sources: "[[Number Hierarchy]], [[Certificates]], [[Exact Until Output]], [[Nested Radicals]], [[Numbers, Lengths and Pixels]]"
updated: 2026-10-20
---

# Function Hierarchy

The levels of [[Number Hierarchy]] carry over to functions with very little change. A function is rated **on exact inputs**, and has **two axes**.

## The rule

**Rate the function on rational inputs.** Nobody computes the infinite digits of $\pi$, the infinite digits of $e$, divides one infinite expansion by the other, and then sums infinitely many terms, each a power of those infinite digits. Everyone rounds the input to something, then runs the algorithm to a stated accuracy. So a Pixel input is not worth considering in rating the function itself (Murphy). The rounding is the user's act, with its own $\varepsilon$ ([[Exact Until Output]]).

**Example, $\sin(\pi/e)$.** Round the inputs, $\pi_7=3.1415926$ and $e_7=2.7182818$ (the $\pi_n$ convention of [[Exact Until Output]]). The quotient is a rational, $1.1557273\ldots$, and the sine algorithm then runs to a stated $\varepsilon$. The result is $0.9150885$ to seven places, and the same algorithm on the $\pi_7$, $e_7$ inputs and on the full values agree to about $3\times10^{-9}$ (computed). The function is rated by what it does to $1.1557273\ldots$, a rational.

## Axis 1: the certificate of the operations

| Level | Operations admitted | Value at a rational input | Example |
|---|---|---|---|
| 1–4 | $+,-,\times,\div$ (and the exact comparison), combined | a rational, **exact** | $f(x)=\dfrac{x^2+1}{x-1}$; $f(\tfrac32)=\tfrac{13}2$ |
| 5 | add $\sqrt{\ }$ | a Length in $\mathbb K$, exact | $\sqrt{x^2+1}$ at $x=\tfrac12$ is $\tfrac{\sqrt5}2$ |
| 6 | add $\sqrt[3]{\ }$ | a Length (origami) | $\sqrt[3]{x}$ at $x=2$ |
| 7 | add $\sqrt[n]{\ }$ | a Jiǔ Zhāng Pixel: digits right as they come | $\sqrt[5]{x}$ at $x=2$ |
| 8 | solve a polynomial in $y$ with coefficients in $x$ | a Pixel by iteration; Newton to the stated resolution is the certificate | $y^5-y-x=0$ at $x=1$ |
| 10–11 | a limit or a series, for every input | a Pixel at the far end of trust | $\exp$, $\ln$, $\sin$ at a rational |
| 14 | a function **extended beyond the domain of its definition** by analytic continuation | a value **assigned** by the extension; where the definition diverges, a Posit | $\zeta(-1)=-\tfrac1{12}$ |

A **polynomial is an exact function**, $\mathbb Q\to\mathbb Q$ (levels 1–4). Its Pixel nature does not show on evaluation; it shows when you **solve**, when does it equal zero. That is level 8.

**[AI] The levels grade the inverse problems admitted.** A square root is the inverse of squaring, a cube root of cubing, an $n$-th root of the $n$-th power, a polynomial root of the polynomial. Levels 5–8 are therefore the forward arithmetic of 1–4 plus a stated inverse. A function's level is the highest level its values reach over its rational inputs ($\sqrt x$ takes the rational value $2$ at $4$ and a Length at $2$, so it is level 5).

**Transcendentals.** A transcendental function is a limit for every input, so every value is a level 10 or 11 number (Murphy). The only exceptions are the special inputs where it collapses ($\exp 0=1$, $\ln1=0$). A value at a rational is held as a Pixel, with the trust of [[Number Hierarchy#Trust across the levels]]. The exact, discrete replacement for sine and cosine, a rational orbit at levels 1–4, is [[Rational Rotation]].

**Beyond the limits: the continuation (level 14).** The zeta function is defined for $\operatorname{Re}s>1$ by $\zeta(s)=\sum n^{-s}$. At $s=-1$ that series is $1+2+3+\cdots$, which diverges. The value $\zeta(-1)=-\tfrac1{12}$ is the value of the **one and only extension** of $\zeta$ that stays differentiable (in the complex sense) on the connected plane, apart from the pole at $s=1$ (Murphy). It is not a limit of the partial sums, and no partial sum is near it. This is level 14 of [[Number Hierarchy]]: same notation, a different certificate.

**[AI]** Two further points, both for Murphy to judge.
- *The values are tame; the bridge is not.* The values of the continuation at negative integers are rationals: $\zeta(-n)=-B_{n+1}/(n+1)$ with $B_k$ the Bernoulli numbers, so $\zeta(-1)=-\tfrac{B_2}2=-\tfrac1{12}$ and $\zeta(-3)=-\tfrac{B_4}4=\tfrac1{120}$ (checked from $B_2=\tfrac16$, $B_4=-\tfrac1{30}$). Each is an exact level 1–4 number. What is a Posit is the **warrant**: the uniqueness of the extension is a theorem inside a system that has accepted a completed plane, all the earlier levels and their limits (compare level 12, "existence only for someone who has accepted the previous levels").
- *What it is not.* It is not the Cesàro value of level 13. Cesàro assigns $\tfrac12$ to $1-1+1-\cdots$ by averaging partial sums; no such averaging assigns $-\tfrac1{12}$ to $1+2+3+\cdots$ (the Cesàro means grow without bound). A second method (a smoothed sum with the divergent part removed) also returns $-\tfrac1{12}$, but that is a literature point to check before citing.

**[AI] Level 9 and levels 12–13.** Level 9 (geometric: the right edge of an area) is a way of *defining* a number, so for functions it sits with the limits. Level 12 (uncomputable) is not a function one evaluates; level 13 (divergent) is a summation method attached to a series, and the continuation of level 14 is the form it takes for a function.

## Inverses are harder than they look

Murphy's repeated theme: modern mathematics gives inverses less weight than they cost. $2^2=4$ and $2^3=8$, but $2^?=6$.

A forward operation is **total on its level**: any two whole numbers have a power. Its inverse is **defined only on the image**, and off the image the answer lives at a higher level.

**The example, $2^x=6$.**
- No whole number: $2^2<6<2^3$.
- No fraction $p/q$: $2^{p/q}=6$ means $2^p=6^q$, impossible since $3$ divides $6^q$ and not $2^p$ ([[Fundamental Theorem of Arithmetic]]).
- Not algebraic either **[AI]**: $x=\log_26=2.5849625007\ldots$ (computed), and if $x$ were algebraic and irrational, $2^x=6$ would be transcendental (Gelfond–Schneider, third-party), which it is not. So the inverse of a level 1–4 operation, on level 1–4 data, lands at levels 10–11.

**The ladder** (Murphy, [[Counting and Bases]]): the inverse of $+$ forces zero and negatives; the inverse of $\times$ forces $\mathbb Q$; the inverse of squaring and cubing forces Lengths (levels 5–6); of a polynomial, level 8; of exponentiation, levels 9–11. The forward operations never leave the exact levels; **each inverse costs a new kind of number and a step out along the trust gradient** ([[Number Hierarchy#Trust across the levels]]).

**The ladder in history** (Murphy: addition and multiplication are closed over the whole numbers; the coming of their inverses made the integers and the rationals; the line between Numbers and Lengths begins with the attempt to invert squaring, then cubing, then higher powers). **[AI]** The attached episodes are recollections to check, and the order is not strictly the order of levels:

| Inverse attempted | What it forced | Episode |
|---|---|---|
| subtraction | zero, negatives (levels 1–4) | rules for debts in Brahmagupta (c. 628); slow acceptance in Europe |
| division | fractions (levels 1–4) | Egyptian and Babylonian fractions |
| squaring | Lengths, level 5 | incommensurable diagonal (Greek); $\sqrt2$ in sexagesimal on YBC 7289 |
| cubing | Lengths, level 6 | doubling the cube: impossible with straightedge and compass (Wantzel, 1837), possible by origami |
| $n$-th powers | Pixels, level 7 | root extraction in the *Jiǔ Zhāng* |
| a polynomial of degree 5 | Pixels, level 8 | no solution in radicals (Abel, 1824; Ruffini earlier, incomplete): Newton's iteration instead |
| exponentiation | levels 9–11 | Napier's logarithms (1614), tables computed by method |

The cubic gave a second, different consequence: Cardano's formula (1545) can pass through $\sqrt{-1}$ even when all three roots are real (the casus irreducibilis), so one inverse forced a new kind of number in a second direction as well.

**[AI] Three prices, not one.**
1. *Existence.* The inverse is partial: it answers on the image and says nothing, or something larger, elsewhere.
2. *Kind.* The answer is of a higher level than the question, and its certificate is weaker.
3. *Cost.* The forward direction is cheap and the inverse dear: multiplying $7\times13$ against factoring $91$; differentiating a rational function (always a rational function) against antidifferentiating $1/x$ (never one); solving $y'=f(x,y)$ against differentiating a solution.

**[AI] The inverse that stays cheap.** On exact data an inverse can be easy. On the tick orbit of [[Rational Rotation]] with $N$ even, the step count $k$ of a point is the number of factors $N^2+1$ in its common denominator: for $N=10$ the denominator is $101^k$, so $k$ is read off. Checked for $k<60$. A point *off* the orbit has no such $k$: the inverse is again partial, and the nearest tick is a Pixel claim.

## Reading an answer by parts

An answer is usually a sum of parts of different standing, and the convention is to **say which part is which**. A transcendental function does not need a name of its own to be understood; it needs its level and its certificate stated (Murphy).

**Example.** $\displaystyle\int\Bigl(1+\frac1{x^2+1}\Bigr)dx=x+\arctan x+C$.

| Part | Level | At a rational $x$ |
|---|---|---|
| $x$ | 1–4 | exact |
| $\arctan x$ | 10–11 | a Pixel, to a stated $\varepsilon$, by $x-\tfrac{x^3}3+\tfrac{x^5}5-\tfrac{x^7}7+\cdots$ |

Nobody computes all the terms of the second part; the name stands for "the part that is only approximatable". The same reading applies to $\operatorname{Si}$, $\operatorname{Li}$ and any later function defined as an antiderivative: the label is the level of the part and the certificate that comes with it, not a new name.

**[AI] The certificate has a range.** The series for $\arctan x$ converges only for $|x|\le1$. There the tail of the alternating series is at most the first omitted term; at $x=\tfrac12$, five terms give $0.46368427$ against $0.46364761$, an error of $3.7\times10^{-5}$ under the next term $4.4\times10^{-5}$ (computed by hand). Beyond $|x|=1$ the argument is first replaced by the slope of its half-wedge, $\dfrac{x}{1+\sqrt{1+x^2}}$ ([[Characteristic Length#Half a wedge]]), which moves a level-5 root into the exact part; so the division into parts depends on the certificate used.

## Axis 2: the cost to a pixel range

The certificate says what kind of answer you get. The cost says what it takes to get the answer to a stated resolution, as a function of the digits $n$ asked for and the size of the input.

- **Exact levels still cost.** Take $f(x)=x^2+1$ and iterate it from $\tfrac12$ (computed): $\tfrac12,\ \tfrac54,\ \tfrac{41}{16},\ \tfrac{1937}{256},\ \tfrac{3817505}{65536}$. The denominators are $2,4,16,256,65536=2^{2^k}$, so the digits **double** at every composition. A level 1–4 function is the safest in trust and not in cost: the rational that answers exactly may not fit the budget ([[Creational Ultrafinitism]]).
- **Nesting.** A nested radical stays at levels 5–7 by certificate, but the degree of the field it lives in grows with each nesting ([[Nested Radicals]]). The level does not rise and the cost does.
- **Iteration.** Newton's method roughly doubles the correct digits per step ([[Fundamental Theorem of Algebra]]), so the cost of $n$ digits at level 8 is about $\log n$ steps, each costing an evaluation of the polynomial. The stopping test that proves the digits is extra.
- **Sensitivity** **[AI]**. Since the input was rounded, the function itself determines how many input digits are owed for a stated output $\varepsilon$ (its sensitivity, the derivative of [[Calculus]]). This is a property of the function on rational inputs, and it is why rounding the input is safe.

## Differential equations

Most differential equations have no closed form and are simply graphed at a given pixel level (Murphy). The hierarchy covers this.

**[AI] Where the solution sits.** Solving $y'=f(x,y)$ is the inverse of differentiation, so it is an inverse problem like levels 5–8. The solution is defined as a limit of a process (Picard iteration, or Euler with step $h	o0$), and the process is not just addition, so every value is a level 11 number. The ones that happen to have a closed form (constant-coefficient linear, separable) are written with $\exp$, $\sin$, $\ln$, which are already levels 10–11. A solved equation is more famous than an unsolved one, not more certain.

**[AI] The graph is exact data.** Euler's method with rational $f$ and rational step $h$ is arithmetic at every step, so the output at step $k$ is a rational: levels 1–4, $\mathbb Q\to\mathbb Q$. The polyline is exact. The Pixel claim is that it lies within $\varepsilon$ of the true solution. Take $y'=y$, $y(0)=1$, up to $x=1$ (computed): $h=\tfrac12$ gives $\tfrac94=2.25$; $h=\tfrac1{10}$ gives $(1.1)^{10}=2.5937424601$; $h=\tfrac1{100}$ gives $2.7048138\ldots$. Against $e=2.7182818\ldots$ the errors are $0.468$, $0.125$, $0.0135$: about tenfold smaller for a tenfold smaller $h$, as a first-order method should.

Two certificates, as everywhere:
- **Axis 1, the method's error theorem.** For a method of order $p$ with a Lipschitz bound on $f$ the global error is $O(h^p)$. That theorem, not any one run, is what certifies the graph. Level 7's digits needed no such theorem; here the trust is in the method, which is a step outward on [[Number Hierarchy#Trust across the levels]].
- **Axis 2, the cost.** Steps scale as $1/h$, and the exact rationals grow: the $h=\tfrac1{100}$ value above has denominator $100^{100}=10^{200}$. Past the budget one rounds at each step, and the rounding enters the error bound.

**[AI] The horizon.** Where nearby solutions separate like $e^{\lambda t}$ (chaotic systems), the certificate holds only up to a time. Past it the graph cannot be trusted for that trajectory, so the certificate must state its horizon.

**The tie to [[Discrete Calculus]].** The difference equation $y(x+h)=y(x)+h\,f(x,y)$ is the exact object, and the differential equation is its step-size dial taken to the limit.

## Hard problems

1. **The cost theorems.** Axis 2 needs stated bounds (big-O in $n$ and in the height of the input), not examples. None are proved here; the doubling above is a single worked case.
2. **Several variables.** The hierarchy is written for one input. Functions of several variables share the levels; the cost grows with the number of coordinates.
3. **Level 14.** Whether other continuations (the gamma function, which continues the factorial beyond the whole numbers, is the nearest example; unverified) are the same level or need their own, and what the certificate of a continuation is beyond "it exists and is unique."
4. **Level 9.** Whether a geometrically defined function (area under a curve as a function of its right edge) is a level of its own or a limit is open.
5. **Differential equations.** Error theorems and horizons are stated here only in words; no bound is proved for a named method on a named equation. Existence and uniqueness (Picard) as a constructive procedure is not worked.
6. **Piecewise functions and decisions.** On rational inputs, comparisons are exact. At a Pixel input a comparison can be undecidable, which is why the rule rates the function on exact inputs.
