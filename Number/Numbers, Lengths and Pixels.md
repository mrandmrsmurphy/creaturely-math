---
title: Numbers, Lengths and Pixels
aliases:
  - Ratios, Surds and Approximations
type: concept
status: "canonical (the names, the sort and the pixel-equality clauses are Murphy's, 2026-10-10)"
provenance: "murphy (the sort; the names Numbers, Lengths, Pixels; the pixel idea and its motivating question; the four clauses of pixel equality; Posits as a temptation; the rational as the first matrix; discrete versus continuous as the heart of the philosophy; the pixel-doctrine skeleton, the matrix facts, the object-names rationale, the Posit–fiat distinction and the continuum stance, adopted 2026-11-04) + ai-synthesis (the music figures, the mapping to the hierarchy)"
sources: "[[Number Hierarchy]], [[Equal Signs]], [[Babylonian Mathematics]], [[Constructible Numbers]], [[Exact Until Output]], [[Infinity and Cantor]]"
updated: 2026-11-04
---

# Numbers, Lengths and Pixels

Murphy's answer to the vault's first open problem ([[Future Directions]] item 1: split the word *number*). The word *number* today is like the word *star* two thousand years ago — planets, stars and galaxies under one name — and the [[Number Hierarchy]] does the sorting. The names are these (Murphy, 2026-10-10):

| Name | Levels | What it is | How it is known | Equality |
|---|---|---|---|---|
| **Number** | 1–4 (group A) | a count, a share, a ratio | **exhibited**: the count itself; the reduced pair $(a,b)$, $\gcd=1$ | exact: $\frac ab=\frac cd\iff ad=bc$ |
| **Length** | 5–6 (group B) | a magnitude: the diagonal, a folded cube root | **constructed** — admitted *as long as it stays tethered to geometry* | exact in $\mathbb K$, decidable ([[Exact Until Output]]) |
| **Pixel** | 7–11 (group C) | a value held at a stated resolution | **computed**: an algorithm with a stated error bound | agreement at a stated resolution |
| **Posit** | 12–14 (group D) | what can only be declared | **posited**: a named convention, or a pure existence argument | by the convention named |

The verbs run downhill — *exhibit, construct, compute, posit* — each a weaker hold than the last: the gradient of [[Creational Ultrafinitism]] given nouns. Wildberger draws the line after the first row (ratios only); Murphy's answer is that the word was always three words, and the first is "definitely good and right". The names line up with the three equal signs ([[Equal Signs]]): exact (Numbers and Lengths), algorithmic (Pixels), formal (Posits).

The line between "number" and the rest was drawn historically far more conservatively than modern mathematics suggests (the Greek *arithmos* was a multitude of units; magnitudes were another genus), and the real number system hides the sorting.

## Why object-names

Ratio, surd, approximation are *notation-words*: they name expressions. The names here name the **objects**, which is what creaturely realism wants. The old distinction stands and sharpens: for Numbers and Lengths, an approximation is a way of *writing* an object held exactly another way — the output stage ([[Exact Until Output]]). For the Pixels the algorithm **is** the object, and the pixel is its exhibited form: not a picture of the number but the number-as-held. Levels 12–14 are past holding altogether.

## The doctrine of the pixel

Murphy's motivating question: **why are we so confident looking at the graph of $y^3-x^2y+4x=0$?** His answer: because the picture is owed only to a stated resolution (an $\varepsilon$ of $10^{-6}$, say). It is **analytic geometry with smearing** — and like the engineer's $\pi=e=3$, it works practically. The doctrine:

1. **A pixel is a value with a stated error bound, never a bare value.** The resolution is part of the object.
2. **Among pixels there is no bare equality.** The four clauses are Murphy's, on [[Certificates]]: apartness by computation; agreement at a stated resolution is all "=" means between pixels; exact equality is proved about the generating rules; the classical undecidability of equality is accepted as a procedural negative. No one has ever generated infinite digits to compare; the cost accumulates, but it is never impossible. (The Borwein lesson: agreement through the tenth digit, betrayal at the eleventh.)
3. **A pixel is only as honest as the modulus behind it.** Graphing calculators lie — the aliasing of $\sin(100x)$, the false join across the pole of $1/(x-1)$, the smear of $\sin(1/x)$ near $0$ — and every lie is a dropped certificate: features smaller than the pixel, with no named modulus $\delta(\varepsilon)$. The approximate [[Intermediate Value Theorem]] is exactly the licence for trusting a sign-change pixel.
4. **Display is the output stage** ([[Exact Until Output]]): store the algorithm; print the pixel. For $\pi$, the $\pi_n$ convention is how a pixel is printed: $\pi_7=3.1415926$, exact, with $\pi_7\le\pi<\pi_7+10^{-7}$.
5. **Literature to check:** interval arithmetic (Moore) is the arithmetic of pixels; provably reliable graphing exists — Tupper's thesis and the GrafEq program colour a pixel only when an interval evaluation *proves* the curve passes through it (unverified recollections).

## Posits

Murphy names levels 12–14 **Posits**. The fit: a Cesàro value or a zeta assignment is *laid down* by convention (Latin *positum*, a thing placed), and an uncomputable such as Chaitin's Ω is existence asserted with no exhibition. The name itself carries the verdict: *you posited this*. They are kept on the ladder dialectically (Murphy): not numbers in the normal sense, and their systems not warranted, but recorded so that the believer in the completed reals must wrestle with what his acceptance asserts without exhibition ([[Number Hierarchy]]). The distinction from [[Fiat Numbers]]: a fiat ($i$, $\varepsilon$, $j$) is declared *and* exhibitable — you compute with it exactly; a Posit is declared and *not* exhibitable on the main axis.

## The rational as the first matrix (Murphy)

A rational number **is a pair of whole numbers**, which Pythagoreans could accept. That pair is a column vector $\binom ab$, and several facts make it the first matrix object (all checked):

- **Equality is a determinant.** $\tfrac ab=\tfrac cd$ exactly when $\det\begin{pmatrix}a&c\\b&d\end{pmatrix}=ad-bc=0$: two pairs name the same ratio when they are *parallel*. A ratio is a **direction** (a point of the projective line), which is why the slope of [[Slope]] is a ratio and $\infty$ ($b=0$) is a legitimate point ([[Extended Constructible Numbers]]).
- **Matrices act on ratios.** The matrix $\begin{pmatrix}a&b\\c&d\end{pmatrix}$ sends $x$ to $\dfrac{ax+b}{cx+d}$.
- **The slope-addition law is a matrix product.** With $M(t)=\begin{pmatrix}1&-t\\t&1\end{pmatrix}$, the product $M(t)M(u)$ has the same ratio of entries as $M(t\oplus u)$: for $t=\tfrac12$, $u=\tfrac13$ the product is $\begin{pmatrix}5/6&-5/6\\5/6&5/6\end{pmatrix}$, entry ratio $1=t\oplus u$ ([[Sum of Slopes]]; checked).
- **Every positive ratio is a product of two matrices.** The Stern–Brocot tree: read a word in $L=\begin{pmatrix}1&0\\1&1\end{pmatrix}$ and $R=\begin{pmatrix}1&1\\0&1\end{pmatrix}$, form the product, add the columns of the result, and you reach each positive ratio exactly once. Checked: all words of length up to $5$ reach $63$ ratios, among them all $19$ reduced ratios $\tfrac ab$ with $a,b\le5$.

So the Numbers have an *algebra of their own* (matrices and their products) that the Lengths, being roots, do not.

## Why the numbers are first: the ear

The ear is a ratio-detector: the octave $2:1$, the fifth $3:2$, the fourth $4:3$, the major third $5:4$ sound consonant, and combine by multiplication ($\tfrac32\cdot\tfrac43=2$, an octave; $\tfrac54\cdot\tfrac65=\tfrac32$; checked). This is the Pythagorean discovery, and a clean case of *number heard*.

Music shows three of the kinds at work:

| | Fifth | Kind |
|---|---|---|
| **Just intonation** | exactly $\tfrac32=701.96$ cents | Number |
| **Equal temperament** | $2^{7/12}=1.498307\ldots=700$ cents | Length (a twelfth root of $2$, geometric in origin) |
| **What the ear tolerates** | within about $2$ cents | Pixel |

Twelve perfect fifths overshoot seven octaves by the **Pythagorean comma** $\dfrac{3^{12}}{2^{19}}=\dfrac{531441}{524288}=1.01364$ (about $23.5$ cents; checked): *no stack of ratios $3:2$ closes on the octave*, a small incommensurability inside the arithmetic of Numbers. Equal temperament repairs it with a Length, and the repair is inaudible to within a tolerance. (The equal-tempered major third is $13.7$ cents sharp of $\tfrac54$, a larger compromise.) Pythagoras's world of ratios needed an irrational to tune.

## Lengths are inherently geometrical

A Length is **constructed**. $\sqrt n$ is the altitude of a right triangle whose hypotenuse is cut into segments $1$ and $n$ (the geometric mean: for $2$ and $8$ it is $4$, for $1$ and $2$ it is $\sqrt2$; checked), or the diagonal of a rectangle. It has no natural home in counting, which is why the Pythagorean discovery of the incommensurable diagonal shook arithmetic and not geometry. The tether to geometry is Murphy's condition on levels 5–6, and its home in the vault is [[Constructible Trigonometry]]; the Lengths are kept exactly, in the constructible field $\mathbb K$ ([[Constructible Numbers]]).

## Discrete and continuous: the heart of the philosophy [Murphy]

*The discrete-versus-continuous question is the center of the philosophy of mathematics and is no more resolved today than it was in the Greek world.* The names line up with it:

- **Numbers** are the **discrete** side: pairs of counted units.
- **Lengths** are the **continuous** side: magnitudes that cannot be counted out.
- **Pixels** are the **bridge**, the practical device that lets a discrete numeral stand in for a continuous length — at a stated resolution.

The standard **real number system sweeps the question under the carpet**: it names one object, ℝ, for ratio, surd, transcendental and unconstructible alike, and declares the continuum to be a set of discrete points (a Dedekind cut is a *set of rationals*). It resolves the question by fiat, and that is why the sorting above is invisible to a student ([[Certificates]], the "bamboozlement").

**Where the vault sits**: the continuum is *potentially* divisible and never a completed set of points (Aristotle, *Physics*; [[Future Directions]] item 8); an infinitesimal is the reciprocal of a number past the threshold ([[Infinitesimals]]); and the discrete and continuous are bridged by the difference calculus ([[Discrete Calculus]]), where one rule governs both.

### In education: what students meet

Strong elementary students meet **radicals** with no account of what a radical is: a calculator key that produces an unending decimal. Under this sort a radical is introduced as a **Length**: the diagonal of a square, constructed, exact, and *then* approximated on output, so the student sees a Length as geometry and the decimal as a reading — a Pixel. The word "irrational" can wait. See [[Historical Order]] and [[Babylonian Mathematics]].

## The Greeks and the one and the many

The Greek stance let the **One** triumph over the many (the Pythagoreans' "all is number" broke on the diagonal). The Christian answer is that the One and the many are equally ultimate. Worked out on [[Greek Mathematics]] and [[Theology of Number]].

## Hard problems

1. **The wall inside the Pixels.** Level 7's digits (Jiǔ Zhāng) appear right and are never revised, which is what makes level 7 more explicit than level 8; level 8's may be rewritten, and to be sure of the last digit one must do more work than the digit itself needs (Newton's method can correct earlier digits; it is run until the stated resolution is reached, and that run is the certificate); levels 9–11 are named by their process, not a toolkit. One name covers five levels the hierarchy distinguishes: either the doctrine absorbs this (a pixel is the output of any of them), or *Pixel* is a genus with species. The species are ordered by trust and remoteness from verification (Murphy: [[Number Hierarchy#Trust across the levels]]).
2. **Where $\sqrt[n]{x}$ with $n\ge3$ sits.** $\sqrt[3]2$ is origami — a Length. $\sqrt[5]2$ is level 7: the *expression* is a surd, but the object is held as a Pixel, by a determinate digit algorithm.
3. **The ear.** The cent figures above are computed, but the psychoacoustics (that the ear hears ratios) is the Pythagorean and later view, not examined.
