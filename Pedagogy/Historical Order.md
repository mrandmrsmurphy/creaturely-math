---
title: Historical Order
type: concept
status: "canonical (draft; dates and literature to check)"
provenance: "murphy (the rule of thumb, historical order unless compelling reason; clock math as fundamental; symbolic algebra is recent yet the immediate goal of middle school) + ai-synthesis (the history table, the transparency test, the worked examples, the flagged problems)"
sources: "[[Counting and Bases]], [[Modular Arithmetic]], [[Curriculum Plan]], [[Corrective Narrative]]"
updated: 2026-10-09
---

# Historical Order

> **Rule of thumb (Murphy):** teach things in the order they were discovered, unless there is a compelling reason not to. The Confession puts it: the historical development of mathematics is mirrored in the learning of the individual ([[Counting and Bases]]; Kline echoes it in the article).

Everyone agrees numeracy and arithmetic fluency come first. Murphy adds that **clock math** (modular arithmetic) belongs beside $+,-,\times,\div$ ([[Modular Arithmetic]]). The trouble starts after that.

**Scope of arithmetic (Murphy):** kindergarten through grade 5, with the goal of **total fluency in addition, subtraction, multiplication and division of whole numbers, integers and rational numbers.** Remainders and clock math are taught in a **limited way** within it and become **much heavier** in the next stage, so that there is **never an abrupt change of topic**. Call this the *continuity principle*: each stage should open with the previous stage's last idea, enlarged.

## The observation

In the usual course, arithmetic is followed in middle school by **symbolic algebra**, as the immediate goal. Yet algebraic symbolism is recent. All dates below are recollections, **to check**:

| Stage | When (approx.) | What |
|---|---|---|
| **Tally marks** (addition is concatenation, subtraction removal, multiplication area or repeated addition) | from prehistory (notched bones, c. 20,000 to 43,000 years ago; to check) | [[Tally Marks]] |
| Bundling, bases, place value; **Babylonian engineering mathematics** | from prehistory; Babylonian sexagesimal place value c. 2000–1600 BC | [[Counting and Bases]], [[Sexagesimal]], [[Babylonian Mathematics]] |
| Rhetorical problem-solving (no symbols) | Babylonian tablets c. 1800 BC; Egyptian (Rhind papyrus) c. 1650 BC | equations solved by recipes in words |
| Geometry, proportion, number theory | Euclid, c. 300 BC | Book II (algebraic identities as areas), V (proportion), VII–IX (number theory, the Euclidean algorithm, no last prime), X (incommensurables) |
| Syncopated algebra | Diophantus (c. 3rd century AD, dating uncertain) | abbreviations for the unknown and its powers |
| Zero and negatives | Brahmagupta, 628 | |
| Rhetorical algebra with geometric proof | al-Khwarizmi, c. 820 | *al-jabr*; completing the square by squares and rectangles |
| Hindu-Arabic numerals to Europe | Fibonacci, 1202 | |
| Symbols for operations | $+,-$ in print 1489 (Widmann); $=$ 1557 (Recorde); $\times$ 1631 (Oughtred) | |
| **Letters for unknowns and known quantities** | **Viète, 1591**; Descartes (x, y, z; exponents; coordinates), 1637 | the symbolic algebra of the middle-school goal |
| Function notation $f(x)$ | Euler, 18th century (*Introductio*, 1748) | |
| Congruence notation, $a\equiv b\pmod n$ | Gauss, 1801 | the *notation*; the practice is far older |
| Calculus | Archimedes' exhaustion; Newton and Leibniz, 17th century; **finite differences** (Newton, 1687 and 1711; Taylor 1715) | |
| Limits ($\varepsilon$–$\delta$) | Cauchy 1821; Weierstrass, mid 19th century | |

**The history, stage by stage:** [[Tally Marks]] (prehistory); [[Babylonian Mathematics]] (c. 2000 BCE and after); [[Greek Mathematics]] (c. 600 BCE to c. 500 CE); [[Mathematics 500 to 1500]] (Latin, Indian, Chinese, Persian and Arabic, and early European, with algebra slowly replacing geometry); [[The Road to Calculus]] (c. 1500 to c. 1730); [[Mathematics 1730 to 1900]] (rigour, the reals, Cantor, the multiple geometries); [[Mathematics 1900 to Today]] (the foundations debate, Gödel, the New Math, proof assistants and AI).

So the sequence from the arithmetic years is: **geometry, proportion and number theory, then rhetorical algebra, then syncopated, then symbolic (about 1600), then calculus (infinitesimals and differences), then limits (19th century).** The standard course is closer to: arithmetic, symbolic algebra, geometry, trigonometry, then calculus *opening with limits*, the newest layer first.

Two clear departures [AI]:

1. **Symbols before the thing symbolised.** Algebra's letters came last of the algebraic developments; the standard course makes them the first.
2. **Limits before differences and infinitesimals.** The 19th-century foundation is taught before the 17th-century calculus it was invented to repair. [[Discrete Calculus]] and [[Calculus]] reverse this deliberately: differences, then infinitesimals, and limits (if at all) last.

## Clock math as fundamental (Murphy's claim, with reasons) [AI]

On a clock of $n$ hours, addition, subtraction and multiplication always close; no new kind of number is needed:

- **Subtraction never fails.** $3-5\equiv10\pmod{12}$: going back two hours past noon is an ordinary position. The ladder of [[Counting and Bases]] (subtraction fails in ℕ, so zero, so negatives) is not needed to make sense of "back."
- **Division works where it works, and tells you why.** Mod $5$: $1/2=3$, since $2\cdot3=6\equiv1$. Mod $12$: $2$, $3$ and $4$ have no inverse, and the clock shows why ($2$, $3$ divide $12$). A prime clock has all four operations exactly: a **field** ([[GF(5)]], [[GF(7)]]). The question "when is division possible?" arises with a finite table to read.
- **Exact and finite.** Every statement can be checked by listing: this is the certificate ethic ([[Certificates]]) in its simplest classroom form.
- **Old in practice.** Parity (odd and even), the calendar and week, hours, divisibility tests, music (a stack of $7$ fifths visits all $12$ pitch classes mod $12$, checked), and the Chinese remainder problem ([[Chinese Remainder Theorem]]). The *notation* is Gauss's, 1801: late, but the thing came early, as the historical rule predicts.
- **Computers.** Machine integers are arithmetic mod a power of two ([[Binary]]).

## Why the standard order may have a reason, and what the reason would have to be [AI]

The rule has an exception clause ("unless a compelling reason"). The best candidate reason for early symbols is that a late invention may be a **compression** of earlier understanding, and compression is useful. Positional notation, which is late historically, is taught first and rightly: it is *transparent*, since a child can unfold $347$ into bundles of ten and a hundred.

> **Transparency test (proposal).** A late invention may be taught early only if the student can **unfold it** into the earlier, concrete cases it summarises.

Symbolic algebra fails the test for a student who has not first written the pattern many times in words and in numbers. History shows the route that passes it: rhetorical (write it out), then syncopated (abbreviate what you keep writing), then symbolic. A student who is given letters first manipulates syntax with no cases to unfold. *Literature to check:* the rhetorical, syncopated, symbolic stages as a teaching sequence (Harper, "Ghosts of Diophantus", 1987, as I recall); the genetic method (Toeplitz); Piaget and Garcia on parallels between history and development (1989); and the standing criticism that recapitulation is a loose analogy. Research on the equals sign as "the answer comes next" rather than a balance bears on [[Equal Signs]].

## After arithmetic: number theory, then geometry (Murphy's candidate) [AI]

Murphy's proposal: after arithmetic (about ages 5 to 10 or 11), a light **number theory**, then **geometry** with Euclid and others, done with few numbers. Number theory would reach basic groups (symmetries of the square) and division in a prime modulus, and would be mostly divisibility tests and remainders ("what is $7^{10}$ mod $5$?").

This fits the existing plan: [[Curriculum Plan]] already has Euclid for the freshman year and *Exact Algebra* (symbols) for the sophomore year, so the proposal fills the years before. It also agrees with the history table above.

**Why number theory first.** Division with remainder is the last thing arithmetic teaches; modular arithmetic is that remainder taken seriously, so number theory is the *next page* of arithmetic and not a new subject. It builds the habit of exact, checkable answers ([[Certificates]]) and gives the first proofs in the simplest setting.

**Why not obviously.** Euclid himself puts plane geometry (Books I–VI) before number theory (VII–IX), and his number theory is written in the language of line segments. Either order is historically defensible. The practical case for number theory first is continuity with arithmetic; the case for geometry first is that Euclid's deductive style is learned on pictures. A sensible reading is to teach the *practice* of number theory first and the *proof habit* through geometry, with the easy number-theory proofs (parity) done Euclid-style.

**Letters arrive here, and pass the transparency test.** The first use of a variable in this stretch is to prove something the student has already checked on many numbers: an even number is $2k$ and an odd number is $2k+1$, so odd times odd is $(2a+1)(2b+1)=2(2ab+a+b)+1$, odd ($3\cdot5=15=2\cdot7+1$, checked). The letter abbreviates a pattern the student can unfold, which is the syncopated stage.

**Worked example from Murphy.** $7^{10}\bmod5$: $7\equiv2$, and the powers of $2$ mod $5$ cycle $2,4,3,1$ with period $4$; $10\equiv2\pmod4$, so $7^{10}\equiv4$ (checked, as is the cycle of $7^k$ itself). The student *discovers the cycle* by listing, then meets [[Fermat's Little Theorem]] as the explanation of why the period divides $4$.

**Content already in the vault** that this stretch can draw on: [[Modular Arithmetic]] (divisibility tests including $7\cdot11\cdot13=1001$, casting out nines, parity), [[Fundamental Theorem of Arithmetic]], the Euclidean algorithm (for instance $\gcd(252,198)=18$), [[Chinese Remainder Theorem]], [[GF(5)]] and [[GF(7)]] (division in a prime modulus), [[Groups]], [[Symmetries of the Equilateral Triangle]] and [[Symmetries of the Square]].

**Cautions.**

1. **Ratio and proportion.** With rationals inside arithmetic (grade 5) the fractions question is settled; what remains is whether ratio and proportion are taught as part of arithmetic, since they must be in place before similarity and Euclid V–VI.
2. **"Few numbers" in geometry is a Greek feature, not a free choice.** Euclid compares magnitudes without measuring them; areas and the Pythagorean theorem are comparisons of squares. Measurement by number returns with Descartes (coordinates, slope), which the vault's [[Constructible Trigonometry]] keeps free of angle measure.
3. **Readiness for deductive geometry.** The van Hiele levels (visual, descriptive, informal deduction, formal) suggest many students need preparation before Euclid-style proof; the existing plan puts Euclid in ninth grade. *Literature to check.*
4. **Groups early.** Murphy reports that middle schoolers can do simple groups: they were given a cardboard square, labelled the front vertices ABCD and the back EFGH, built the Cayley table (it took a while, with no difficulty), and then evaluated nested products such as A(B(C(D(E(F(G(H))))))). Reconstructed with letters in [[Symmetries of the Square]]. This is one teacher's classroom report, not a study.

## Then a growing set of symbols: analytic geometry and probability (Murphy's candidate) [AI]

The student now knows geometry, clock math and some real algebra, and has met associativity and commutativity as facts about cardboard. Murphy's next step: a growing stock of symbols, leading to **analytic geometry** and **probability**. History agrees: both came within a generation of symbolic algebra (Viète 1591; Descartes 1637; Pascal and Fermat on the problem of points, 1654; Huygens 1657; Bernoulli, *Ars Conjectandi*, 1713; all dates to check). The existing plan puts this stretch at *Exact Algebra* (quadratics, conics, function notation, matrices) and then either *Discrete Bridges* or *Statistics for Everyone* ([[Curriculum Plan]]).

**Symbols in the order they are needed.** The transparency test again: each symbol enters when the student has a stock of cases to unfold. The sequence suggested by the history: a letter for a pattern already seen (parity, done); a letter for an unknown in an equation (the rhetorical recipe, abbreviated: the Babylonian square above); a letter for a *known but general* quantity, Viète's step, so that a recipe becomes a formula (the quadratic formula as the recipe with $a,b,c$ in place of numbers); function notation; coordinates; matrices as tables with a product.

### Analytic geometry: where the strands meet

It joins the geometry strand and the number strand, and it is natural for these students.

- **Lines by slope**, from [[Slope]]: no angle measure; a line is $y=mx+b$, and the rise-over-run is the middle-school ratio.
- **Circles and rational points.** The circle $x^2+y^2=1$ has the rational points $\left(\frac{1-t^2}{1+t^2},\frac{2t}{1+t^2}\right)$; for $t=\tfrac23$ this is $\left(\tfrac5{13},\tfrac{12}{13}\right)$, the 5-12-13 triple (checked). So Pythagorean triples, from the number-theory stage, *are* the rational points of the circle, and the slope-addition law $\oplus$ gives the group structure ([[Discrete Calculus]] Part II; [[Constructible Trigonometry]]).
- **The circle over a clock.** Students who know a prime clock can count the points of $x^2+y^2=1$ mod $p$. Checked: $4,4,8,12,12,16$ points for $p=3,5,7,11,13,17$, that is $p+1$ when $p\equiv3\pmod4$ and $p-1$ when $p\equiv1\pmod4$. It is a finite geometry that ties the stages together: number theory (when is $-1$ a square?), geometry (the circle), and groups (the points form a cyclic group under $\oplus$, to check). [[GF(5)]], [[GF(7)]].
- **Conics and transformations** (from the *Exact Algebra* list): the algebra of a shape, and function notation as a rule for moving a graph.

### Probability: counting, with explicit error

Classical probability is a **ratio of counts**, which is exact and finite and rests on the combinatorics the students can already do (arrangements $P(n,k)$, the falling powers of [[Discrete Calculus]], the binomial coefficients of Pascal's triangle). It fits the position ([[Future Directions]] item 13): finite probability with stated bounds, no measure theory.

- **Exact answers by counting.** Exactly 5 heads in 10 flips: $\binom{10}{5}/2^{10}=\tfrac{252}{1024}=\tfrac{63}{256}$. At least 8 heads: $(45+10+1)/1024=\tfrac{7}{128}$.
- **The problem of points** (Pascal and Fermat): a game to 3 points, the first player needs 1 more, the second needs 2 more; fair split of the stake is $3:1$, since the first wins unless the second wins both of the next two: $1-\left(\tfrac12\right)^2=\tfrac34$.
- **A stated error bound in place of "as $n\to\infty$".** The law of large numbers in finite form: for $n$ fair flips, the chance that the fraction of heads is off by $\varepsilon$ or more is at most $\dfrac1{4n\varepsilon^2}$ (Chebyshev). For $n=1000$, $\varepsilon=0.05$ this is at most $0.1$; the exact count of the tail gives about $0.0017$, so the bound is true and loose (both computed). That is the vault's stance in a small case: the statement comes with its error.
- **Providence.** Probability is a natural place for the Christian theme that outcomes of chance are under God's rule (for example Prov 16:33, to check); it is a pastoral link, not a mathematical premise.

### Cautions

1. **Probability and analytic geometry are two threads.** They are contemporaries but need not be taught together; counting (arrangements, binomial) can come as early as the number-theory stretch.
2. **"Genuine algebra" is a stage, not a count of topics.** What the students have done is not specified here.
3. **The sophomore texts are unwritten** ([[Curriculum Plan]]); this section is documentation of the order, not a syllabus.

## The final pieces, and the end of mandatory schooling (Murphy) [AI]

The sequence ends in two tracks. **Advanced students** get [[Constructible Trigonometry]] and the discrete-to-infinitesimal calculus ([[Discrete Calculus]], then [[Calculus]]); **the majority** get [[Statistics]]. This matches the choices already in [[Curriculum Plan]]: *Discrete Bridges* or *Statistics for Everyone* in the junior year, and *Infinity and Uncertainty* or *Calculus for Everyone* in the senior year.

**What is out of historical order, and why it is allowed.** The rule has an exception clause ("a compelling reason"), and here it is the end of mandatory schooling: the last stretch must give the student what is most useful.

| Piece | Historically | In this sequence |
|---|---|---|
| Trigonometry | **early** (chords of Hipparchus and Ptolemy, c. 150 BC onward; astronomy) | **late**, because the slope-based form needs algebra and coordinates first, and the vault uses no angle measure |
| Calculus | differences and infinitesimals (17th century), then limits (19th) | **in order**: differences, then infinitesimals, limits last or never |
| Statistics | **very late** (Gauss and Laplace, then Galton, Pearson and Fisher; 19th and 20th centuries, to check) | **last, for the majority**, by the compelling reason: a citizen needs to read an uncertain claim and see its error |

The calculus track is the one place the whole sequence is in historical order. The two out-of-order pieces are late for opposite reasons: trigonometry because its modern form needs the algebra that came after it, statistics because the civic need outranks the chronology.

## What goes in the middle-school slot (documentation, not a syllabus) [AI]

The vault already holds material from the historical stretch between arithmetic and symbolic algebra:

- **Number theory and clock math:** [[Modular Arithmetic]], divisibility, primes and unique factorization ([[Fundamental Theorem of Arithmetic]]), the Euclidean algorithm, the Chinese remainder theorem, [[Fermat's Little Theorem]]. Symbol-light, exact, checkable.
- **Geometry as the first algebra:** Euclid II. $(a+b)^2=a^2+2ab+b^2$ is a square cut into two squares and two rectangles. It is the same picture as the product-rule rectangle of [[Discrete Calculus]].
- **Ratio and proportion to slope:** [[Slope]], [[Constructible Trigonometry]] (no angle measure, so no degrees).
- **Rhetorical algebra.** A Babylonian problem: *I added the area and the side of my square: three quarters. What is the side?* Recipe: take half of $1$, which is $\tfrac12$; square it, $\tfrac14$; add to $\tfrac34$, giving $1$; its root is $1$; subtract the $\tfrac12$: the side is $\tfrac12$. Check: $\tfrac14+\tfrac12=\tfrac34$. This is completing the square with no letter in it.
- **Calculus by differences** before limits: [[Discrete Calculus]].

## Hard problems

1. **How early are letters teachable?** The transparency test gives a criterion but not an age; it needs classroom evidence.
2. **Is recapitulation true enough to steer by?** The rule is Murphy's guide and has the Confession and Kline behind it, but the research record is mixed (to check).
3. **Cost of leaving the standard path.** Students who move between schools enter the standard sequence (Dimensions, AoPS, Exeter), and this order is an alternative to it.
4. **Is history one line?** Different cultures ordered these developments differently; the table is a Mediterranean-and-European thread with Indian and Arabic contributions.
