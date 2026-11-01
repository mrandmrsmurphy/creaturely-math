---
title: Babylonian Mathematics
type: history
status: "canonical (draft; the history is from recollection and to be checked)"
provenance: "murphy (the reading, the Babylonians as an engineering mathematics, one end of a spectrum; irregular reciprocals and the diagonal of the unit square treated alike; the rationals as the outermost entity to call numbers; the field matters; sevenths of a length versus of an angle) + ai-synthesis (the checks, the distinctions, the flagged problems)"
sources: "[[Sexagesimal]], [[Counting and Bases]], [[Historical Order]], [[Number Hierarchy]], [[Exact Until Output]], [[Theology of Number]]"
updated: 2026-10-10
---

# Babylonian Mathematics

The second stage of [[Historical Order]], after [[Tally Marks]]. The number system itself, base $60$ with its tables of multiples and reciprocals, is on [[Sexagesimal]]; this page is about **the stance** behind it. All historical statements are from recollection and to be checked against a source.

## The stance: engineering mathematics (Murphy)

Babylonian scribes (Old Babylonian period, c. 2000–1600 BC, and later) worked as a modern engineer does: a procedure that gives an answer good enough for the purpose is a good procedure. There are no theorems in the Greek sense; there are **worked problems with algorithms** and a stated precision. Murphy's shorthand is the engineer's joke "$3=\pi=e$": quantities are carried to the **significant digits** the job needs, and no further.

**The same distrust for $\sqrt2$ and $\tfrac17$ (Murphy).** An approximation of $\sqrt2$ was held in the same low regard as an approximation of $\tfrac17$, which does not terminate in base $60$ ([[Sexagesimal]]). They knew that our ability to subdivide and partition physical reality has limits, so for them the failure to exhibit "numbers" came sooner than it does for us: the line between what can be exhibited and what is only approached was drawn nearer to the rationals ([[Number Hierarchy]]).

Three features that make the stance concrete:

- **The system is floating.** Numerals carry no point: $1$, $60$ and $\tfrac1{60}$ look alike, and the size comes from context ([[Sexagesimal]]). A scribe carried the *significant digits* of a quantity and tracked its magnitude separately, exactly as scientific notation does.
- **Values are given to a chosen precision.** On the tablet YBC 7289 the diagonal of a square of side $30$ is written $42;25,35$, which is $30\times1;24,51,10$. The value $1;24,51,10=1+\tfrac{24}{60}+\tfrac{51}{3600}+\tfrac{10}{216000}\approx1.4142130$ differs from $\sqrt2=1.4142136\ldots$ by about $6\times10^{-7}$, and its square is $1.9999983$ (all computed). That is six-figure accuracy, from a purely numerical procedure.
- **Pi was taken as $3$ for most purposes**, and one tablet from Susa has $\tfrac{25}8=3;7,30=3.125$ (checked: $3+\tfrac7{60}+\tfrac{30}{3600}$). $e$ was not known; the "$=e$" in the joke is the modern engineer's. *(Susa tablet: recollection.)*

This is the same ethic as the budget forms of the vault: an answer **with a stated tolerance** is the honest kind ([[Intermediate Value Theorem]], [[Exact Until Output]]). The Babylonians did what the vault calls *round only at the output*, except that they had no exact form to round from.

## They did a lot

- **Plimpton 322**, a table of Pythagorean triples ($119^2+120^2=169^2$ is its first row, as I recall; the identity checked), c. 1800 BC.
- **Quadratic problems** solved by completing the square in words (the square-and-side problem of [[Historical Order]]).
- **Accumulation, before calculus.** Tablets from perhaps 350 to 50 BC compute Jupiter's displacement as the **area of a trapezoid in a time-velocity diagram** (Ossendrijver, *Science*, 2016; recollection, check the details). The area under a velocity graph is an integral; this is the *finite* form ([[Fundamental Theorem of Calculus]]) done exactly because the velocity is linear. The practice of accumulation is old and the derivative is the later idea, which supports the integral-first reading there.

## Regular and irregular (Murphy's observation)

The reciprocal tables list only the **regular** numbers ($2^a3^b5^c$), whose reciprocals terminate in base $60$ ([[Sexagesimal]]: $25$ of the first $60$ numbers). The others, $7,11,13,14,17,\dots$, are **irregular**: there are no entries, and the reciprocal is approximated when needed. In base $60$ (all computed):

| $n$ | $1/n$ | period |
|---|---|---|
| $7$ | $0;\overline{8,34,17}$ | $3$ |
| $11$ | $0;\overline{5,27,16,21,49}$ | $5$ |
| $13$ | $0;\overline{4,36,55,23}$ | $4$ |
| $17$ | $0;\overline{3,31,45,52,56,28,14,7}$ | $8$ |

Murphy's reading: scribes classed these with the **diagonal of the unit square**: things one does not have an exact sexagesimal value for, and approximates. [AI] A fair account of the evidence:

- **Supported:** both kinds of quantity were *approximated to a needed precision*, with no exact numeral; both are "irregular" in the sense of not terminating.
- **Not shown:** that the scribes held them to be *the same kind of thing*, or that a ratio like $\tfrac17$ was "not really real." The irregularity of $\tfrac17$ is a fact about the **base**: in base $7$ it is $0.1$, a one-digit number. The diagonal is irregular in **every** base. So the two irregularities differ in kind: one is notational and one is not. (This is the point of [[Counting and Bases]]: the rule that $\tfrac1n$ terminates iff every prime factor of $n$ divides the base.)

So the Babylonian evidence supports the **engineering stance** and the **notation-relative** nature of regularity; it supports "ratios are not numbers" only if one adds an interpretation.

## The rationals as the outermost numbers [AI]

Murphy: ratios are the outermost entity to call *numbers*; he is stating that the line on the [[Number Hierarchy]] was drawn **historically far more conservatively** than modern mathematics suggests, and he has **sorted ratios and surds differently**, both different again from approximations (the Babylonian "irregular" number). The sort is worked out on [[Numbers, Lengths and Pixels]], where Murphy has named the kinds — Numbers, Lengths, Pixels — and so drawn the line ([[Future Directions]] item 1).

A note on the Greeks, who were stricter still: for Euclid (Book VII) a *number* is a multitude of units, a whole number; ratios of numbers and **magnitudes** (lengths, areas) are compared in Book V without being numbers (recollection, to check). **[AI] note:** the vault's names are Numbers for levels 1–4 and Lengths for 5–6 ([[Numbers, Lengths and Pixels]]); the Greeks' *magnitude* is the ancestor of the Length. And one respect in which the Babylonians do *not* fit the stance: they computed with an irrational magnitude (the diagonal) as freely as with a fraction.

## The field matters (Murphy)

*"You can divide any length in sevenths perfectly, but you can't any angle."* Both halves are true, and they show how much depends on the field one works in:

- **Dividing a length into $7$ equal parts** is a ruler-and-compass construction (parallel lines), so $\tfrac17$ of a length is a rational, in $\mathbb Q$.
- **Dividing a given angle into $7$ equal parts** is not constructible in general (as the trisection of an angle is not). The seventh of the full turn needs $\cos\tfrac{2\pi}7\approx0.6235$, a root of the cubic $8x^3+4x^2-4x-1=0$ (checked: residual about $10^{-15}$), so it lies in a **degree-3 extension** of $\mathbb Q$: outside the constructible numbers $\mathbb K$ ([[Constructible Numbers]]; the regular heptagon is not constructible), though reachable with folding (origami, level 6 of [[Number Hierarchy]]; recollection).
- **In sexagesimal degrees**, one seventh of the full turn is $\tfrac{360}7=51;25,42,51,25,\dots$ (repeating $25,42,51$), irregular in the notational sense as well, so the *same* "sevenths" is irregular twice over.

One word ("sevenths"), three different fields: lengths in $\mathbb Q$; the angle in a cubic extension; the sexagesimal notation for it, a non-terminating expansion. **The field over which one works is rarely stated and decides what can be done.** The vault's hierarchy states it ([[Number Hierarchy]], [[Constructible Trigonometry]], which avoids angle measure for exactly this reason).

### What may be divided: the domain of the problem [AI]

*"Cutting a person in sevenths gets you jail or worse; cutting a bull in sevenths and you are a legal butcher."* The difference is **discrete versus continuous quantity**, which Aristotle drew (*Categories*, recollection): persons are counted units that must stay whole; a bull is a quantity of weight that may be shared. The Greek *arithmos* was of the first kind and *megethos* of the second. A word problem therefore **names its domain**, and the right arithmetic depends on it:

| What is shared | Domain | Seven ways |
|---|---|---|
| Seven people among ... | whole numbers | share only by $\tfrac17$ of a *group* (a remainder, [[Modular Arithmetic]]) |
| A length of rope | rationals / lengths | exactly $\tfrac17$ by construction |
| A bull's meat, by weight | physical quantity | $\tfrac17$ **to the butcher's precision**, never perfectly (cut by weight, to a stated tolerance) |
| A dollar among three | cents (discrete) | cannot be equal ([[Counting and Bases]]) |

The butcher's case is the Babylonian stance in a shop: "perfectly" in the *length* case means in the geometric idealization; in the *meat* case it means to the precision of the scale.

## A spectrum of stances [AI]

| Stance | Question | Mode | Example |
|---|---|---|---|
| **Babylonian** | How do I get the answer? | procedure, with a precision | $1;24,51,10$ for the diagonal |
| **Greek** | Why is it true? | proof from first principles | Euclid; the irrationality of $\sqrt2$ |
| **Modern** | What is it? | definition within a system | the completed reals |
| **The vault** | What is my warrant, and for what precision? | certificate | [[Certificates]] |

The vault wants the Babylonian honesty about precision and the Greek demand for proof, with no claim to a completed totality: closest to a **proof-bearing engineering**. A note on [[Theology of Number]]: its table lists "Many-ness wins in B.C. empiricism (Babylon, Egypt)" under *Rebellion*; this page treats the Babylonian stance as **one end of a legitimate spectrum**, not as a fall. Whether the table should be changed is Murphy's decision.

## For teaching [AI]

1. **Sexagesimal is worth teaching** because it survives in hours, minutes and seconds, and in the measure of the circle ([[Sexagesimal]]). It is also *clock math* with base $60$ ([[Modular Arithmetic]]).
2. **Floating arithmetic by hand**: carry the significant digits and track the size separately.
3. **Which fractions terminate** in base $10$, base $60$, base $7$ (the rule of [[Counting and Bases]]); why $60$ was a good choice ($12$ divisors).
4. **Ask "what is the domain?"** for every word problem (the table above).
5. **Give the diagonal a value** to a stated precision, with a check by squaring, as the scribe did.

## Hard problems

1. **The evidence for how the scribes classed irregular quantities** is thin; this page flags the interpretation as Murphy's and as not established.
2. **Whether "number" should mean levels 1 to 4** is the large question behind [[Future Directions]] item 1.
3. **Dates and attributions** (YBC 7289, Susa, Plimpton 322, Ossendrijver) are recollections.
