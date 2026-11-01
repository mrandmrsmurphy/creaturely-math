---
title: The Road to Calculus
type: history
status: "canonical (draft; every date and attribution is from recollection and to be checked; two items are unverified anecdotes)"
provenance: "murphy (the frame: logarithms as the technology that made calculus conceivable, from Maor; the Principia in Euclid's style while taking Cartesian geometry seriously; an explosion of topics before the modern obsession with axiomatic proof; Berkeley's critique of infinitesimals as unfounded; the philosophical turn from reception to autonomy, with Kepler and Newton, and Daniel Robinson's anecdote of the sheep) + ai-synthesis (the timeline, the worked examples, the checks, the qualifications, the flagged problems)"
sources: "[[Mathematics 500 to 1500]], [[Discrete Calculus]], [[Calculus]], [[Infinitesimals]], [[Five Acts]], [[Greek Mathematics]], [[Historical Order]], [[Theology of Number]]"
updated: 2026-10-10
---

# The Road to Calculus

The fifth stage of [[Historical Order]], from the end of [[Mathematics 500 to 1500]] to about **1730**: Copernicus to the aftermath of Newton, with Berkeley's critique of 1734 as an epilogue. All dates are approximate recollections **to be checked**.

## What is claimed here

1. **Logarithms** were the technology that made calculus conceivable (Murphy, from Eli Maor's *e: The Story of a Number*).
2. Newton's *Principia* is written in **Euclid's style**, though Newton took Cartesian algebraic geometry seriously.
3. The period saw an **explosion of topics**, and it came **before the modern obsession with axiomatic proof**.
4. **Berkeley's critique** of infinitesimals turns out to be unfounded (Murphy; qualified below).
5. The **philosophical bent** of the age is inseparable from the mathematics: devout founders, then a turn toward autonomous human reason.

## A timeline (approximate)

| Date | Event |
|---|---|
| 1517; 1543 | Reformation begins; Copernicus, *De revolutionibus* |
| 1545; 1572 | Cardano, *Ars magna* (cubic and quartic); Bombelli's complex numbers |
| 1585 | Stevin, *De Thiende*: **decimal fractions** |
| 1591 | Viète: letters for known and unknown quantities |
| 1596; 1609; 1619 | Kepler: *Mysterium cosmographicum*; *Astronomia nova* (ellipses); *Harmonices mundi* |
| **1614** | **Napier's logarithms** (*Descriptio*); the construction explained in the *Constructio* (published 1619) |
| 1617–1624 | Briggs: base-10 logarithms; Bürgi independently (published 1620); Oughtred's slide rule (c. 1622) |
| 1623 | Galileo, *Il Saggiatore*: nature is written in the language of mathematics |
| 1627 | Kepler's *Rudolphine Tables*, computed with logarithms |
| 1635; 1637 | Cavalieri's indivisibles; **Descartes** (*Discourse* and *Geometry*) and **Fermat**: coordinates, tangents |
| 1647–1649 | Gregory of St Vincent and de Sarasa: the area under the hyperbola $y=1/x$ behaves as a logarithm |
| 1654; 1657 | Pascal and Fermat on the problem of points; Huygens on probability |
| 1656; 1668 | Wallis, *Arithmetica infinitorum*; Mercator's series for $\ln(1+x)$ |
| 1665–1671 | Newton's fluxions, worked out privately (*De analysi*, 1669, circulated) |
| 1670 | Barrow, *Lectiones geometricae*: tangents and areas as inverse problems, in geometric dress |
| 1675–1684 | Leibniz's notation ($dx$, $\int$) and first publication (1684) |
| **1687** | **Newton's *Principia*** |
| 1683; 1713; 1715 | Jacob Bernoulli's compound-interest limit; his *Ars conjectandi* (posthumous); Taylor's series |
| **1734** | **Berkeley, *The Analyst*** |
| 1748 | Euler, *Introductio in analysin infinitorum* |

## 1. Logarithms: the technology that made calculus conceivable

Murphy's reading of Maor is that logarithms are what made the calculus *conceivable*. [AI] I did not verify Maor's exact claim; a search confirmed that the book opens with Napier and ties his idea to geometric progressions, extended to a **continuous** range of exponents. Here is a way to see why the claim is plausible.

**A logarithm turns multiplication into addition.** A table pairs an arithmetic progression with a geometric one. That is the first widely used **function given by a rule and tabulated**, a new kind of object that is neither a geometric figure nor an algebraic formula. It is also the first widely used *transcendental* function, defined by a process and not by radicals.

**Napier's construction was discrete.** He started from $10^7$ and repeatedly multiplied by $1-10^{-7}$, obtaining $y_k=10^7(1-10^{-7})^k$, and recorded the step count $k$ as the "logarithm" of $y_k$ (recollection of the *Constructio*). This is **exactly the discrete exponential** of [[Discrete Calculus]]: the function $b^k$ with $b=1-10^{-7}$ satisfies $\Delta b^k=(b-1)\,b^k$, an eigenfunction of the difference operator. Checked numerically:

- $(1-10^{-7})^{10^{7}}=0.36787942\ldots$ against $\tfrac1e=0.36787944\ldots$ (relative difference $5\times10^{-8}$): after $10^7$ steps the value has shrunk by almost exactly $e$. So $e$ is hidden in Napier's table, long before it had a name.
- For $k=3{,}000{,}000$: $y_k=7{,}408{,}182.1$, and $10^7\ln(10^7/y_k)=3{,}000{,}000.15$, so Napier's integer $k$ equals $10^7$ times a *natural* logarithm to better than one part in $10^7$. (Napier's logarithms are to base $\tfrac1e$, as one source says.)

The **continuous** logarithm then arrived by two routes: the *area under the hyperbola* $1/x$ (1647–1649), and the *series* $\ln(1+x)=x-\tfrac{x^2}2+\tfrac{x^3}3-\cdots$ (Mercator, 1668). Compound interest gave $e$ as $\lim(1+\tfrac1n)^n$ (Bernoulli, 1683); for $n=10^7$ it is $2.7182817$ against $e=2.7182818$ (computed).

**Why the discrete-first reading fits the vault** [AI]: the road to calculus *began with a table*. Differences and sums of tables (Napier, Briggs, and Newton's own interpolation formula, below) came before the derivative, which is the order [[Discrete Calculus]] teaches. The motive was applied: Napier wrote that he wished to lighten the labour of calculation (recollection of his preface), and Kepler used the tables to compute planetary positions. **A practical technology prepared the way for a pure idea**, which is the pattern of [[Mathematics 500 to 1500]].

## 2. The *Principia* in Euclid's style

Newton's *Principia* (1687) proves its results by **synthetic geometry**: lemmas, propositions and "first and last ratios" of vanishing quantities, in the manner of Euclid, though Newton had worked out his fluxions two decades earlier and knew Descartes's algebraic geometry well (his *Enumeration of Cubic Curves*, appended to the *Opticks* in 1704, classifies cubics by algebra). Why the geometric dress is **debated**: whether Newton found results with the calculus and then recast them in geometry for acceptability, or worked geometrically much of the time; scholars differ (recollection; to check). Two observations that need no resolution:

- **Geometry still carried the weight of proof.** Algebra and the new symbolic methods were *tools of discovery*; the *Elements* was still the standard of demonstration. This is the transition [[Mathematics 500 to 1500]] traces: the shift of the language of proof from geometry to algebra is not complete in 1687. It is complete by about **1788**, when Lagrange's *Mécanique analytique* boasts in its preface that it contains no figures (recollection).
- **Newton's book contains finite differences.** His **interpolation formula** (Book III, Lemma V; later *Methodus differentialis*, 1711) is the forward-difference formula of [[Discrete Calculus]]: $f(n)=\sum_j\binom nj\Delta^jf(0)$. For $f(n)=n^3-2n+5$ the differences at $0$ are $5,-1,6,6$ and the formula reproduces every value (checked in that page). So the discrete calculus is in the *Principia* itself.

## 3. An explosion of topics, before the obsession with axioms

In about two centuries the list of subjects is extraordinary: decimals; logarithms; analytic geometry; probability; complex numbers; infinite series; the calculus; mechanics; the mathematics of tides, optics and planetary motion. Observations:

- **It came from problems, not foundations**: astronomy, navigation, ballistics, gambling, annuities, optics, wine-barrel volumes (Kepler's *Nova stereometria doliorum*, 1615, measured barrels with infinitesimal slices; recollection). Applied drove it.
- **Proof existed, but foundations-first did not.** Mathematicians proved things in the Euclidean style but did not first axiomatize their subject. The demand for *foundations before results* arrives with the rigorous analysis of Cauchy and Weierstrass (from the 1820s), and fully with **Hilbert** (1899) and **Bourbaki** (from the 1930s). The explosion of results thus preceded the "modern obsession with axiomatic proof", and was not hurt by lacking it.
- **Heuristics ran ahead of justification.** Euler summed series with no convergence theory ($1-1+1-\cdots=\tfrac12$ by regularization), the "level 13 and 14" numbers of [[Number Hierarchy]], with named methods.

The lesson the vault draws [AI] is the **order**, which agrees with [[Historical Order]]: practice, then tools, then results, and only later foundations. A teaching sequence that begins with axioms inverts it.

## 4. Berkeley's critique

**The text.** Bishop George Berkeley's *The Analyst* (1734) is subtitled, as I recall, *A Discourse Addressed to an Infidel Mathematician* (traditionally Edmond Halley), and asks whether the objects, principles and inferences of the modern analysis are more distinctly conceived than religious mysteries. It attacks Newton's **evanescent increments**: they are neither finite quantities nor infinitely small nor nothing, and one may call them "the ghosts of departed quantities." It adds that the calculus reaches correct results only by **compensating errors**.

**Berkeley's example, in four treatments.** For $y=x^2$: the increment is $(x+o)^2-x^2=2xo+o^2$.

| Treatment | Steps | Berkeley's worry |
|---|---|---|
| **Newton and Leibniz** | divide by $o$ to get $2x+o$, then let $o$ vanish: $2x$ | $o$ is nonzero (you divided by it) and then zero |
| **Limits** (Cauchy, Weierstrass) | $\dfrac{(x+h)^2-x^2}h=2x+h\to2x$ as $h\to0$ | none, but no infinitesimals |
| **$\varepsilon^2=0$** ([[Calculus]]) | $(x+\varepsilon)^2=x^2+2x\,\varepsilon$; read off the coefficient of $\varepsilon$ | no division by $\varepsilon$, no vanishing: **cancel only for all $\varepsilon$** |
| **Discrete** ([[Discrete Calculus]]) | $\Delta x^2=2x\,h+h^2$ exactly; the error is stated | none: the error $h^2$ is kept |

**The verdict, in two halves** [AI]:

- **Against the formulation of 1734, Berkeley was largely right.** Dividing by $o$ and then setting it to zero *is* inconsistent. The historian Ewald, as I recall, concludes his objections were mostly well taken at the time; and it took about a century for limits to replace the ghosts.
- **As a verdict on infinitesimals, the critique is unfounded.** Abraham Robinson's non-standard analysis (1960–1966) gave infinitesimals a rigorous footing; Bell's smooth infinitesimal analysis and the dual numbers of [[Infinitesimals]] do so without excluded middle. Berkeley's two ghosts are exorcised by never dividing by an infinitesimal on its own (**microcancellation**) and by stating the first-order error. So **both statements hold**: Newton's *argument* was unsound, and Newton's *idea* is sound. Murphy's reading is right about the second.

**The theological side** [AI]: Berkeley's argument is a **theological** one, from a bishop. The mathematicians of the age mocked religion's mysteries while resting their own on obscurity, so they should be humble. That is close to the vault's posture of epistemic humility, and it is a rare case of a Christian apologist doing *good mathematical criticism*; the foundations were indeed wanting.

## 5. The philosophical bent: reception, then autonomy

The mathematics of this period cannot be separated from what the age believed about knowledge.

**Devout founders.** **Kepler** (a Lutheran) held that God had given humanity reason and the capacity to observe, so that studying the heavens was a kind of worship; the words "I am thinking your thoughts after you" are attributed to him (to check). He also gave up his beloved nested-Platonic-solids theory (*Mysterium*, 1596), when Tycho Brahe's data left a discrepancy of **8 minutes of arc** ($\tfrac{8}{60}$ of a degree) for Mars, and arrived at ellipses (*Astronomia nova*, 1609): **honesty before the data over the beauty of the system**. That is the Babylonian discipline within a Pythagorean-Platonic temperament ([[Babylonian Mathematics]], [[Greek Mathematics]]). Galileo (1623) said the book of nature is written in mathematics. **Boyle**, **Ray** and **Pascal** were openly devout; Boyle endowed lectures to defend Christianity (to check). **Newton** wrote more on theology than on physics, in heterodox directions, and the General Scholium of the *Principia* (1713 edition) attributes the order of the system to "an intelligent and powerful Being" (recollection).

**The turn.** **Descartes** (1637, 1641) sought certainty by doubting everything and starting from the self: a method whose foundation is the individual reasoner. **Spinoza**'s *Ethics* (1677) is "demonstrated in geometrical order", **the Euclidean form used to prove a monism** that dissolves a personal God into Nature: the Greek *One triumphant*, and exactly the **ahistorical, universal, eternal** hubris of [[Greek Mathematics]], now in a Christian land. Leibniz dreamed of a universal calculus of reason. By Kant's "dare to know" (1784) and Laplace's reported "I had no need of that hypothesis" (c. 1800) the transfer of ultimacy is visible. The story is that of the sapiential posture giving way to the **Promethean** one in [[Five Acts]]: *the promethean turn, right around the corner.*

**Authority moves.** Murphy reports an anecdote from **Daniel Robinson**, in his lecture on Newton in *The Great Ideas of Philosophy* (The Great Courses; the Newton lecture is, as the course listing gives it, "Newton, the Saint of Science"; exact lecture number to check): a **mutation in a sheep**, in England shortly *before* Newton's lifetime, was brought to the **priest** as the arbiter of what it meant; a similar case *after* Newton was brought to the **Royal Society**, to the scientists.

[AI] **What a search found.** A transcript of the lecture was not located, so Robinson's wording is unchecked. But the *after-Newton* half has a **documented candidate**: James Parsons, "Some Account of a Sheep, Shewed Alive to the Royal Society, in November 1754, Having a Monstrous Horn Growing from His Throat", *Philosophical Transactions* (1755); the stuffed skin with the horn was kept in the Society's museum ([Royal Society](https://royalsocietypublishing.org/doi/10.1098/rstl.1755.0030); [Public Domain Review](https://publicdomainreview.org/collection/some-account-of-a-sheep-having-a-monstrous-horn-growing-from-his-throat-1755/)). Newton died in 1727, so this is a case of the type described, a monstrous sheep brought to the scientists, in the generation after him. Whether it is the case Robinson means is **not confirmed**; the *before-Newton* half (the sheep brought to a priest) has **no source yet**. Record both as Murphy's report; cite the 1755 paper for the after-Newton fact, and do not cite the before-Newton half until the passage is found (the Great Courses guidebook or transcript is the place to look). The reading of *monstrous births* as portents, taken to the clergy, is a plausible background (to check).

The *point* of the anecdote is well supported by the history: **Newton's age is where ultimate arbitration passes from the church to science**, the very category shift that Harrison argues about the "territories" of science and religion ([[Greek Mathematics]]).

**The vault's reading** [AI]: not that science supplanted the church *because* it was better at truth, but that **authority was relocated**, and with it the claim to be the final court. Each sphere is legitimate where it is competent; the error is **ultimacy**.

## Teaching [AI]

1. **Make a logarithm table by hand**: multiply repeatedly by a ratio such as $1.1$, record the exponents, and use the table to multiply two numbers by adding exponents (Praxis; the Napier idea; the same repeated multiplication as $\Delta b^k=(b-1)b^k$).
2. **Slide rules and tables** as the technology the calculus grew from.
3. **Newton's interpolation**: a difference table of a cubic and its Newton form.
4. **Berkeley's $x^2$ in four treatments** (the table above) as a lesson on what a proof needs.
5. **Kepler's 8 minutes**: a case study in honesty before data.
6. **Read a passage of the *Principia*** to see the geometric style, and a passage of Lagrange's preface.

## Hard problems

1. **Maor's exact thesis.** Murphy's reading ("logs made calculus conceivable") should be checked against the book; the search confirmed only the opening on Napier.
2. **The sheep anecdote**: source named by Murphy (Robinson's Newton lecture); the after-Newton half has a documented candidate (Parsons, 1755), the before-Newton half none; Robinson's own words unchecked.
3. **Newton's method in the *Principia***: how much was calculus, how much geometry; scholars disagree.
4. **The balance of the qualification on Berkeley**: whether the vault says "unfounded" (about infinitesimals) or "well founded then, answered since" (about the arguments); the page says the second and notes the first.
5. **Where the road ends.** Euler (1748), the 18th-century rigour crisis, and Cauchy and Weierstrass belong to the next stage.
