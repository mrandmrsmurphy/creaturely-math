---
title: Infinitesimals
type: concept
status: canonical
provenance: murphy (position; 2020 essay, 2023 Confession, 2026 ladders and discussion) + ai-synthesis (SIA, dual numbers, Robinson notes)
sources: "[[SRC Christian Mathematics (c2020)]], [[SRC Confession of Mathematics (2023-24)]], [[SRC Mathematics (raw, 2026-05)]]"
updated: 2026-10-07
---

# Infinitesimals

**An infinitesimal is the reciprocal of a number too big to manage.** Infinitesimals belong to ultrafinitism, not against it.

## The position

- Some numbers are too big to manage: past a threshold, a notation is not a number ([[Creational Ultrafinitism]]). Their reciprocals are too small to manage. An infinitesimal is $1/N$ for an $N$ past the threshold, a quantity we cannot possess.
- The parallel is physics. There may be objects narrower than the Planck length, but we can never measure them ([[Number in Natural Philosophy]], [[Scale and Bands]]).
- So the old question, whether the continuum is discrete or continuous, is resolved in a bizarre way: **below a certain threshold it is unknowable.**
- The Confession says it in its own words: Newton and Leibniz "required there to be a successor to zero"; "we shall call it ε… it has the property that **ε² = 0**. Zero is an infinitesimal, but we posit that there are others. **We are incapable of distinguishing among infinitesimals**, except to say one is zero and that there are others."

## Logic: no excluded middle below the threshold

For infinitesimals $\varepsilon,\delta$ we **cannot make inequalities**: we can assert neither $\varepsilon=0$ nor $\varepsilon\ne0$, and we cannot decide $\varepsilon<\delta$ or $\delta<\varepsilon$. The law of the excluded middle is unavailable for statements about them. This is the same boundary as in [[Future Directions]] item 7: LEM holds where exhaustion is possible, and below the threshold it is not.

## Smooth infinitesimal analysis

John Bell's smooth infinitesimal analysis (SIA) has this shape. It has nilsquare infinitesimals, $\varepsilon^2=0$, and works in intuitionistic logic, with no excluded middle. Two facts about SIA match the Confession sentence above:

- For every $\varepsilon$ with $\varepsilon^2=0$ it is *not not* the case that $\varepsilon=0$, so one can never exhibit an $\varepsilon\ne0$.
- "Every nilsquare $\varepsilon$ is $0$" is **refutable** (it would force every derivative to vanish). So one can say neither that all infinitesimals are zero nor produce one that is not.

That is exactly "we cannot distinguish among them, except to say one is zero and that there are others."

## The dual numbers: the exhibitable form

The dual numbers $\mathbb Q[\varepsilon]/(\varepsilon^2)$ (or over $\mathbb K$) are the concrete, finite form. In terms of matrices,

$$a+b\varepsilon\;\longleftrightarrow\;\begin{pmatrix}a&b\\0&a\end{pmatrix},\qquad \varepsilon=\begin{pmatrix}0&1\\0&0\end{pmatrix},\qquad \varepsilon^2=\begin{pmatrix}0&0\\0&0\end{pmatrix}=0.$$

The matrix $\varepsilon$ is **nilpotent**: its square is zero. (An idempotent matrix is a different thing, $e^2=e$.)

- **Exact first-order calculus:** $f(x+\varepsilon)=f(x)+f'(x)\,\varepsilon$. For example $(x+\varepsilon)^3=x^3+3x^2\varepsilon$, which is the matrix cube $\begin{pmatrix}x&1\\0&x\end{pmatrix}^3=\begin{pmatrix}x^3&3x^2\\0&x^3\end{pmatrix}$.
- **No inequalities:** the ring is not a field ($\varepsilon$ has no inverse) and carries no order that compares $\varepsilon$ with anything. This is the algebraic form of "we cannot make inequalities with infinitesimals."
- **Link to SIA:** in SIA the functions on the nilsquare infinitesimals $\{\varepsilon:\varepsilon^2=0\}$ are exactly the $a+b\varepsilon$.
- **First order only.** $\varepsilon^2=0$ is a first-order truncation. Higher derivatives need $\mathbb Q[\varepsilon]/(\varepsilon^{n+1})$.

## Robinson

Abraham Robinson's work is "an excellent example of rediscovering the intuitive origins of calculus" (the 2020 essay, citing Keisler). That is an alliance of *intuition*: $\delta$ and $\varepsilon$ are infinitesimal quantities. The *formal* system differs: the hyperreal field ${}^*\mathbb R$ is built in classical logic, usually from a non-principal ultrafilter, and is an **ordered** field in which every inequality between infinitesimals is decided ($0<\varepsilon<1/n$ for all standard $n$). So hyperreals are not the system with no inequalities on infinitesimals. SIA and the dual numbers are. See [[Certificates]]: the hyperreals are an existence proof with no exhibited object.

## Calculus

The calculus built on $f(x+\varepsilon)=f(x)+f'(x)\varepsilon$, $\varepsilon^2=0$, is on its own page: [[Calculus]].

## Discrete calculus

A step size $h$ at or below the threshold is an infinitesimal in this sense. [[Discrete Calculus]] (exact differences, no limits) with its step at the threshold is a calculus with infinitesimals: "ε² = 0" is "$h^2$ is below the resolution of the certificate," and first-order discrete calculus carries an explicit error bound.

## Hard problems

1. **The threshold.** What exactly is "past the threshold": a number, a band, a resource-relative notion? ([[Future Directions]] item 2.)
2. **Robinson's ordering versus no inequalities.** Which of Robinson's theorems survive when the order on infinitesimals is not available?
3. **How much of SIA's logic.** SIA gives up excluded middle everywhere, in an intuitionistic setting. The vault's home logic is three-valued ([[Three-Valued Logic]]; [[Future Directions]] item 7): "$\varepsilon=0$" is unknown. What remains open is how SIA's theorems (every function is microaffine, the cancellation of $\varepsilon$) read in K3.
4. **Higher order.** Second derivatives and Taylor remainders need $\varepsilon^3=0$, $\varepsilon^4=0$, and so on: how many orders does the threshold allow?

## Literature

Full list: [[Reading List]].

Wildberger's *Algebraic Calculus*; Keisler's *Elementary Calculus: An Infinitesimal Approach*; Crowell's *Brief Calculus*; Bell's *A Primer of Infinitesimal Analysis*; Archimedes' *The Method*; Euler's *Introduction to the Analysis of the Infinite*.
