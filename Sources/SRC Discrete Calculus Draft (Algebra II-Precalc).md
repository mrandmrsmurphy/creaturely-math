---
title: "Discrete Calculus: A Curriculum Supplement for Algebra II and Precalculus"
type: source
status: verbatim snapshot (do not edit; edit the canonical notes instead)
provenance: murphy+ai (authorship not recorded)
date-written: "2026"
snapshot: 2026-10-07
---

> [!info] Source snapshot
> Full draft text. Overlaps (and is partly superseded by) the DC draft, see [[Discrete Calculus]].

# Discrete Calculus
*A Curriculum Supplement for Algebra II and Precalculus*

# Part I: Algebra II Additions
*(Sequences, Series, and Summation Notation)*

## Alternating Sequences: $(-1)^n$

Students already know that squaring a negative number gives a positive result. The expression $(-1)^n$ formalizes something simple: it alternates between $1$ and $-1$ depending on whether $n$ is even or odd.

$$
(-1)^0 = 1, \quad (-1)^1 = -1, \quad (-1)^2 = 1, \quad (-1)^3 = -1, \quad \ldots
$$

This is the simplest **alternating sequence**. It will reappear throughout mathematics. An alternating series is one whose terms alternate in sign, such as:

$$
1 - \frac{1}{2} + \frac{1}{3} - \frac{1}{4} + \cdots = \sum_{n=1}^{\infty} \frac{(-1)^{n+1}}{n}.
$$

The factor $(-1)^n$ is doing all the work of flipping signs. Students should become fluent with it as a tool.

## The Floor Function $\lfloor x \rfloor$

The **floor function** $\lfloor x \rfloor$ returns the greatest integer less than or equal to $x$. Think of it as "super-duper round down" — it always rounds toward $-\infty$, never toward zero.

$$
\lfloor 3.7 \rfloor = 3, \qquad \lfloor 5 \rfloor = 5, \qquad \lfloor -2.3 \rfloor = -3.
$$

Note carefully: $\lfloor -2.3 \rfloor = -3$, not $-2$. It goes *down*, not toward zero.

The floor function is a bridge between continuous and discrete mathematics. It lets us extract integer behavior from any real input.

The **modulo operator** is defined in terms of floor:

$$
n \bmod m \;=\; n - m\left\lfloor \frac{n}{m} \right\rfloor.
$$

This is the remainder after dividing $n$ by $m$. Some useful identities:

$$
\begin{align*}
n \bmod 2 &= n - 2\left\lfloor \frac{n}{2} \right\rfloor \qquad \text{($0$ if $n$ even, $1$ if $n$ odd)} \\
(-1)^n &= 1 - 2(n \bmod 2).
\end{align*}
$$

**Exercise.** Design a function that produces a "sawtooth" pattern — a sequence that counts $0, 1, 2, \ldots, m-1$, then resets to $0$ and repeats.

**Answer.** $f(n) = n \bmod m$, equivalently $f(n) = n - m\lfloor n/m \rfloor$.

## Rotating Sequences: $\cos_4(n)$ and $\sin_4(n)$

In the quadratic equations chapter, students discovered that the powers of $i$ cycle with period $4$:

$$
i^0 = 1, \quad i^1 = i, \quad i^2 = -1, \quad i^3 = -i, \quad i^4 = 1, \quad \ldots
$$

The standard trick for simplifying $i^{87}$ is to compute $87 \bmod 4 = 3$, giving $i^{87} = i^3 = -i$. But there is a deeper geometric reason: **multiplying by $i$ rotates a complex number $90^\circ$ counterclockwise** in the complex plane. So $i^n$ tracks the position after $n$ quarter-turns around the unit circle. The remainder $n \bmod 4$ is the *geometric residue* of the rotation.

We define two **discrete trigonometric functions**:

$$
\cos_4(n) = \operatorname{Re}(i^n), \qquad \sin_4(n) = \operatorname{Im}(i^n).
$$

| $n \bmod 4$ | 0 | 1 | 2 | 3 |
|-------------|---|---|---|---|
| $\cos_4(n)$ | 1 | 0 | -1 | 0 |
| $\sin_4(n)$ | 0 | 1 | 0 | -1 |

These are **period-4 analogues of cosine and sine**. The simpler alternator $(-1)^n$ is a special case: $(-1)^n = \cos_4(2n)$.

**Useful identities** (verifiable by checking four cases):

$$
\begin{align*}
\cos_4(n) + \sin_4(n) &= (-1)^{\lfloor n/2 \rfloor} \\
\cos_4(n) - \sin_4(n) &= (-1)^{\lfloor (n+1)/2 \rfloor}
\end{align*}
$$

**Application — Walking in Spirals.** Suppose a person walks $1$ step east, turns $90^\circ$ left, walks $2$ steps, turns $90^\circ$ left, walks $3$ steps, and so on. Their position after $n$ steps is:

$$
S_n = \sum_{k=1}^{n} k \cdot i^{k-1}.
$$

This is a complex-valued arithmetico-geometric series. Students can evaluate it for specific $n$ by grouping terms in fours: each complete group of four consecutive steps contributes exactly $-2-2i$ to the total, a fact discoverable by direct computation.

---

# Part II: Precalculus Additions
*(Before Trigonometry)*

## The Forward Difference Operator $\Delta$

The **forward difference** of a sequence $a(n)$ is:

$$
\Delta a(n) = a(n+1) - a(n) = \frac{a(n+1)-a(n)}{1}.
$$

This is the discrete difference quotient with step size $1$, and the discrete analogue of the derivative. No limits are required. Everything is exact.

## Basic Forward Difference Rules

### Constant Rule
$$
\Delta[c] = 0.
$$

### Constant Multiple Rule
$$
\Delta[c \cdot a(n)] = c \cdot \Delta a(n).
$$

### Sum Rule
$$
\Delta[a(n) + b(n)] = \Delta a(n) + \Delta b(n).
$$

These two rules together say that $\Delta$ is a **linear operator**.

### Factorial Rule
$$
\Delta[n!] = n \cdot n!
$$

*Proof.* $(n+1)! - n! = n!\,(n+1-1) = n \cdot n!$.

## Falling Powers (Permutations)

The **falling power** $n^{\underline{k}}$ is defined as:

$$
n^{\underline{k}} = n(n-1)(n-2)\cdots(n-k+1) \qquad (k\text{ factors}).
$$

Students have already computed these: $n^{\underline{k}} = P(n,k)$, the number of permutations of $k$ objects from $n$.

### Discrete Power Rule
$$
\boxed{\Delta\left[n^{\underline{k}}\right] = k \cdot n^{\underline{k-1}}}
$$

*Proof.*
$$
\begin{align*}
\Delta\left[n^{\underline{k}}\right]
&= (n+1)^{\underline{k}} - n^{\underline{k}} \\
&= (n+1)n(n-1)\cdots(n-k+2) \;-\; n(n-1)\cdots(n-k+1) \\
&= n(n-1)\cdots(n-k+2)\bigl[(n+1)-(n-k+1)\bigr] \\
&= k \cdot n^{\underline{k-1}}.
\end{align*}
$$

This rule is **exact** — no limits, no approximation. Compare with the continuous power rule $\frac{d}{dx}x^k = kx^{k-1}$, which requires a limit argument.

### Harmonic Numbers and the Discrete Logarithm

The **harmonic numbers** are defined by:

$$
H_n = \sum_{k=1}^{n} \frac{1}{k} = 1 + \frac{1}{2} + \frac{1}{3} + \cdots + \frac{1}{n}.
$$

Their forward difference is:

$$
\Delta[H_n] = H_{n+1} - H_n = \frac{1}{n+1},
$$

so $H_n$ is the antidifference of $\frac{1}{n+1}$, or equivalently $H_{n-1}$ is the antidifference of $\frac{1}{n}$. This is the discrete analogue of $\frac{d}{dx}\ln x = \frac{1}{x}$, and the parallel runs deep: just as $\ln x$ cannot be obtained by the ordinary power rule (it is the "missing" antiderivative of $x^{-1}$), $H_n$ cannot be obtained from the falling power antidifference rule — it requires its own definition.

The connection between the two is made precise by the **Euler–Mascheroni constant**:

$$
\gamma = \lim_{n\to\infty}\left(H_n - \ln n\right) \approx 0.5772.
$$

That is, $H_n$ and $\ln n$ grow at exactly the same rate, differing by the constant $\gamma$ in the limit. The discrete logarithm and the continuous logarithm are the same function, up to that fixed offset — $\gamma$ is precisely the "cost" of discretization.

## Forward Difference of Regular Powers

For ordinary powers $n^k$, the Binomial Theorem gives:

$$
\Delta[n^k] = (n+1)^k - n^k = \sum_{m=0}^{k-1}\binom{k}{m}n^m.
$$

This is the $k$-th row of Pascal's triangle with the leading term removed. The result has $k$ terms rather than one, which is exactly why falling powers are the preferred basis for discrete calculus.

## The Exponential Rule

For any base $b$:

$$
\boxed{\Delta[b^n] = (b-1)\cdot b^n}
$$

*Proof.* $b^{n+1} - b^n = b^n(b-1)$.

The exponential is an **eigenfunction** of $\Delta$, just as $e^{bx}$ is an eigenfunction of $\frac{d}{dx}$:

| **Continuous** | **Discrete** |
|----------------|---------------|
| $\dfrac{d}{dx}e^{bx} = b\cdot e^{bx}$ | $\Delta[b^n] = (b-1)\cdot b^n$ |
| eigenfunctions of $\frac{d}{dx}$ are $e^{bx}$ | eigenfunctions of $\Delta$ are $b^n$ |

The eigenvalue is $(b-1)$ rather than $b$. For $b = e^h$ with small $h$, $b - 1 = e^h - 1 \approx h$, recovering the continuous eigenvalue in the limit.

### Application to $\cos_4$ and $\sin_4$

Since $i^n$ is exponential with base $b = i$, we have $\Delta[i^n] = (i-1)\cdot i^n$. Taking real and imaginary parts:

$$
\begin{align*}
\Delta\cos_4(n) &= -\cos_4(n) - \sin_4(n), \\
\Delta\sin_4(n) &= \cos_4(n) - \sin_4(n).
\end{align*}
$$

These are the discrete analogues of $\frac{d}{dx}\cos x = -\sin x$ and $\frac{d}{dx}\sin x = \cos x$.

## Product Rule and Quotient Rule

### Product Rule
$$
\Delta[f(n)\cdot g(n)] = g(n)\cdot\Delta f(n) + f(n+1)\cdot\Delta g(n).
$$

Note the asymmetry: one factor is evaluated at $n$, the other at $n+1$. This is unavoidable in the discrete setting. The continuous product rule is recovered when $\Delta f$ and $\Delta g$ are small enough that $f(n+1)\approx f(n)$.

*Proof.* Add and subtract $f(n+1)g(n)$:
$$
f(n+1)g(n+1) - f(n)g(n) = f(n+1)g(n+1) - f(n+1)g(n) + f(n+1)g(n) - f(n)g(n) = f(n+1)\,\Delta g(n) + g(n)\,\Delta f(n).
$$

### Quotient Rule
$$
\Delta\left[\frac{f(n)}{g(n)}\right] = \frac{g(n)\,\Delta f(n) - f(n)\,\Delta g(n)}{g(n)\,g(n+1)}.
$$

The denominator is $g(n)\cdot g(n+1)$, not $g(n)^2$ as in continuous calculus.

## Antidifferences and the Discrete FTC

The **antidifference** of $f(n)$ is any $F(n)$ satisfying $\Delta F(n) = f(n)$.

**Discrete Fundamental Theorem of Calculus:**
$$
\sum_{n=a}^{b-1} f(n) = F(b) - F(a), \qquad \text{where } \Delta F = f.
$$

*Proof.* The sum telescopes: $\displaystyle\sum_{n=a}^{b-1}\Delta F(n) = \sum_{n=a}^{b-1}[F(n+1)-F(n)] = F(b)-F(a)$.

## Antidifference Table

| $f(n)$ | $\Delta f(n)$ | $\displaystyle\sum f(n)$ (antidifference) |
|--------|---------------|--------------------------------------------|
| $c$ | $0$ | $cn$ |
| $n^{\underline{k}}$ | $k\cdot n^{\underline{k-1}}$ | $\dfrac{n^{\underline{k+1}}}{k+1}$ |
| $b^n$ | $(b-1)b^n$ | $\dfrac{b^n}{b-1}$ |
| $n\cdot n!$ | $\Delta[n!]$ | $n!$ |
| $H_n = \sum_{j=1}^{n}\frac{1}{j}$ | $\dfrac{1}{n+1}$ | $\text{---}$ |
| $\cos_4(n)$ | $-\cos_4(n)-\sin_4(n)$ | (via $b=i$ exponential rule) |
| $\sin_4(n)$ | $\cos_4(n)-\sin_4(n)$ | (via $b=i$ exponential rule) |

**The special reciprocal case.** Since $\Delta[1/n] = 1/(n+1) - 1/n = -1/\bigl(n(n+1)\bigr) = -1/(n+1)^{\underline{2}}$, the function $1/\bigl(n(n+1)\bigr)$ antidifferences to $-1/n$. However, $1/n$ itself does not antidifference to a closed form: its antidifference is the **harmonic numbers**

$$
H_n = \sum_{k=1}^{n}\frac{1}{k}, \qquad \Delta H_n = \frac{1}{n+1}.
$$

This is the exact discrete analogue of $\int \frac{1}{x}\,dx = \ln x$. The harmonic numbers play the role of the logarithm in discrete calculus.

## Summation by Parts

Antidifferencing the product rule gives:

$$
\sum f(n)\,\Delta g(n) = f(n)g(n) - \sum g(n+1)\,\Delta f(n).
$$

In definite form:

$$
\sum_{n=a}^{b-1} f(n)\,\Delta g(n) = \Bigl[f(n)g(n)\Bigr]_{a}^{b} - \sum_{n=a}^{b-1} g(n+1)\,\Delta f(n).
$$

This is the discrete analogue of integration by parts $\int u\,dv = uv - \int v\,du$, with the shift on $g(n+1)$ as the honest discrete correction.

## Looking Ahead: From Discrete to Continuous

The sequences $\cos_4(n)$ and $\sin_4(n)$ rotate through four positions with period $4$. The natural question is: *what if we allow rotation by any angle, not just multiples of $90^\circ$?*

That question is precisely what trigonometry answers. The functions $\cos\theta$ and $\sin\theta$ are what $\cos_4$ and $\sin_4$ become when the discrete index $n$ becomes a continuous angle $\theta$ and the step of $90^\circ$ becomes an infinitesimally small increment. Euler's formula

$$
e^{i\theta} = \cos\theta + i\sin\theta
$$

is the continuous version of $i^n = \cos_4(n) + i\sin_4(n)$.

Every rule in this document has a continuous analogue in calculus. The discrete versions are in some ways cleaner — they require no limits and are provable by direct computation. Understanding discrete calculus first gives students a concrete foundation on which the abstraction of limits can be built.
