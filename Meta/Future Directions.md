---
title: Future Directions
type: meta
status: living — the vault's to-do list and its guidelines
updated: 2026-10-22
---

# Future Directions

**This page is the vault's to-do list.** Asked "what needs doing?", read **the Agenda** below and answer from it; do not rebuild the list from the pages. Items marked **[AI]** are my suggestions, not Murphy's; literature pointers are *unverified recollections to check*.

**Keeping it true** (the rule that makes the Agenda trustworthy):
1. The Agenda is updated in the same session as any change to the work. A finished item moves to **Settled** with a pointer to the page, and the change goes in [[log]].
2. Every open line names a page: either a page *to write* or the page whose hard-problems section holds the detail. Detail stays on its page and is linked, never copied here.
3. The numbered problems in Part II keep their numbers (other pages cite "item 7", "item 2c").
4. Before answering from the Agenda, spot-check it against the pages it points to; if a page has moved ahead, fix the Agenda first.

---

## The Agenda

### Settled (Murphy's decisions and what the vault now says)

| What | Where |
|---|---|
| Split the word "number": Numbers 1–4, Lengths 5–6, Pixels 7–11, Posits 12–14; level 8 is a Pixel | [[Numbers, Lengths and Pixels]], [[Number Hierarchy]] (item 1) |
| A certificate is a procedure; the four clauses of pixel equality | [[Certificates]] (item 3) |
| The trust gradient across the levels | [[Number Hierarchy#Trust across the levels]] |
| The number hierarchy applied to functions, with the two axes | [[Function Hierarchy]] |
| What the diagonal argument proves: a procedural negative about lists | [[Diagonal Argument]] (item 4) |
| Induction: a rule that permits one further step does not justify an arbitrarily long iteration of it | item 6 below |
| Home logic: three-valued (Kleene K3); "$\varepsilon=0$" is unknown | [[Three-Valued Logic]] (item 7) |
| Calculus on $\varepsilon^2=0$: definition, product, power, reciprocal, quotient and chain rules, the integral's local half | [[Calculus]], [[Infinitesimals]] |
| The five theorems of the Change ladder worked in budget form | [[Fundamental Theorem of Calculus]], [[Intermediate Value Theorem]], [[Extreme Value Theorem]], [[Mean Value Theorem]], [[Bolzano-Weierstrass Theorem]] |
| Fourier analysis without transcendentals | [[Fourier Analysis]] |
| Statistics begun: seven exact results | [[Constructible Statistics]] |
| Constructible trigonometry: 15 triangle cases plus ISS, QCS, area, inradius, circumradius | [[Constructible Trigonometry]] |
| An answer is read by parts, each labelled with its level and certificate (no new name needed for Si, Li, arctan) | [[Function Hierarchy#Reading an answer by parts]] |
| Sine and cosine are levels 10–11; the vault's replacement is a discrete rational orbit (exact, levels 1–4, no angle) | [[Rational Rotation]] |
| Quadriga documented | [[Quadriga for Mathematics]] |

### A. Murphy decides (nothing below can be settled without him)

1. **Zeta:** he said "same derivative" for the extension; the page uses complex-differentiable on a connected domain. Confirm. ([[Function Hierarchy]])
2. **Babylon under Rebellion?** ([[Theology of Number]] table; left unchanged.)
3. **The sentence in [[Infinity and Cantor]]** ("almost all reals are provably beyond any finite description"): rewrite to the procedural form? ([[Diagonal Argument]], last section.)
4. **Level 12:** its existence is conditional on the levels before it; how far to inhabit that system. ([[Number Hierarchy]], Open (a).)
5. **Catechism/Confession** (item 11).
6. **Quadriga:** review the ecumenical draft (the Protestant text is canonical here). ([[Quadriga for Mathematics]], Open 3.)
7. **Names for the tick functions** ($\operatorname{dsin}_N,\operatorname{dcos}_N$ are the pasted conversation's). ([[Rational Rotation]], hard problem 6.)
8. **Pedagogy choices:** untimed fluency checks ([[Praxis]]); whether to teach $p$-values ([[Statistics]]); Bayesian or frequentist first.

### B. Open work, by strand

Tags: **core** (unlocks the most) · **next** (ready to do) · **medium** · **small** · **background** (verification, history). Page names in *italics* are pages that do not yet exist.

**Foundations and logic**
- **core** Threshold as a function (item 2): prove cost bounds and check the feasible-number literature. The same work appears as [[Function Hierarchy]] hard problem 1, [[Fundamental Theorem of Arithmetic]] 1, [[Exact Until Output]] 1, [[Fundamental Theorem of Algebra]] 1, [[Certificates]] Open.
- **next** Induction as a schema with its cost (item 6): rewrite [[Proof Types]] #8 and the infinite-primes remark; work a bounded induction with its cost. Reads into [[Apodeixis]] hard problem 1.
- **next** *Proof in K3* (item 7): validity as truth-preservation (K3 has no tautologies); how proof by contradiction, bounded quantification and induction read in it. Then: which of SIA's theorems read in K3 ([[Infinitesimals]] hard problem 3).
- **medium** *The Reals* (a page defining "the Reals": axioms, constructions, the four meanings), so the thesis has a target. Also premise 2 argued out and the divine-idea / created-quantity tension ([[Christians and the Reals]], gaps 1, 2, 5).
- **medium** [[Exhibiting a Real]]: a feasible notion of algorithm (Ko–Friedman), the scope of Feferman's result (verify), which authors hold "every number is an algorithm".
- **medium** [[Four Kinds of Truth]]: where theorems sit; name the kind of each premise of the position.
- **small** [[Diagonal Argument]]: its four hard problems.
- **background** Literature check (item 10) with the seven search questions on [[Reading List]]; Parikh, Sazonov, Nelson.

**Number**
- **next** *Primes* (one page): why $\mathbb Z/p$ is special; a positive certificate (Pratt) beside Fermat's witness; Wilson as characterisation. Four pages wait on it: [[Modular Arithmetic]], [[Wilson's Theorem]], [[Fermat's Little Theorem]], [[Fundamental Theorem of Arithmetic]].
- **medium** [[Function Hierarchy]]: cost theorems; several variables; level 9 for functions; other continuations (gamma); ODE bounds and Picard.
- **small** [[Function Hierarchy#Inverses are harder than they look]]: check the history table's dates and the Gelfond–Schneider step against sources; where the cubic's second consequence (Cardano's route through $\sqrt{-1}$) sits on the ladder; a cost statement for inverses beyond examples.
- **medium** [[Numbers, Lengths and Pixels]] hard problem 1: Pixel genus versus species (the trust order supplies the ordering).
- **medium** [[Fundamental Theorem of Algebra]]: complex roots without angle measure; multiplicity and near-multiplicity; the hyper-Catalan series' radius; stopping tests for level 8.
- **medium** [[Exact Until Output]]: canonical form for sums of radicals; what counts as "output".
- **small** [[Chinese Remainder Theorem]] cost bound; [[Euler's Theorem]], [[Fiat Numbers]], [[Tally Marks]] hard problems.

**Change (calculus)** — item 5; all of these are stated as open on the pages named
- **core** *Derivatives of $\exp,\log,\sin,\cos$ with certificates*, taken from their discrete ancestors ($E_h$, $H_n$, the circle) with explicit error: [[Calculus]] "Exact versus honest" and hard problem 1; [[Mean Value Theorem]] 1; [[Discrete Calculus]] 1. This unlocks the rest. The circle's discrete ancestor now has a page ([[Rational Rotation]]) and the reading of answers by level is set ([[Function Hierarchy#Reading an answer by parts]]); the error bounds against the classical graphs are not written.
- **next** *The bridge theorem*: for a general $f$, an explicit bound licensing "drop the terms $h$ multiplies" in terms of $f''$ (exact for polynomials). [[Calculus]] 3; [[Fundamental Theorem of Calculus]] 1; [[Discrete Calculus]] 1.
- **next** Second derivative and Taylor remainder with a stated error; how many powers of $\varepsilon$ the threshold allows. [[Infinitesimals]] 4; [[Calculus]] 4; [[Mean Value Theorem]] 3.
- **medium** Infinite intervals and series as bounded sums with a tail bound ([[Fundamental Theorem of Calculus]] 3); antiderivatives beyond the algebraic functions (4); constancy: adopt the SIA axiom or require a modulus (2).
- **medium** Several variables ([[Extreme Value Theorem]] 3, [[Bolzano-Weierstrass Theorem]] 4, [[Mean Value Theorem]] 4); near-maximizers ([[Extreme Value Theorem]] 1); metastability for general bounded sequences ([[Bolzano-Weierstrass Theorem]] 1); Fermat's interior-maximum argument in the $\varepsilon$-calculus ([[Extreme Value Theorem]] 4).
- **medium** [[Discrete Calculus]] Part II is thin: second circular difference, $\sum S(t_n)$, the hyperbolic case; $\gamma$ as a gap between levels.
- **medium** Differential equations: a systematic budget-form account ([[Function Hierarchy]], ODE section; [[Christians and the Reals]] gap 4).

**Trigonometry and geometry**
- **next** CPA and IQA triangle cases (item 15): formulas and checks are worked out below; CPA needs the letter **P** in the hub's convention table. Then examine QIS, QIC, ICS.
- **medium** Constructible against rational trigonometry (item 9): no page compares them. [[Rational Rotation]] is the first page on the rational side.
- **medium** [[Rational Rotation]], open: almost-periods of the tick set, a cost theorem to a target wedge, which wedges a rational step reaches, a Fourier basis on the ticks (hard problems 1–5).
- **medium** The article's open items ([[Constructible Trigonometry]]): exact $r_{\max}$, the 17-gon, sin/cos transition, vectors, spherical and hyperbolic.
- **medium** A geometry without continuity axioms (item 8): engage Hilbert's continuity axioms ([[Geometry Hierarchy]], Open).

**Measurement**
- **next** [[Constructible Statistics]] next steps: the minimal theorems with proofs; the Gaussian as a named approximation of the binomial with explicit error; intervals for measured data.
- **medium** [[Probability]]: conditional probability and independence on huge spaces; a density as an approximation to a finite table, with error. [[Statistics]]: continuous distributions; "as $n\to\infty$" replaced by finite bounds.
- **background** Randomness (deferred on both pages).

**Pedagogy** — all future pedagogical work, none taught as a year yet
- Proof types by grade; a classroom set per Exercise; rubrics; a curriculum placement chart; a unit template; teacher-equipping sequence: the list is on [[Quadriga for Mathematics]] ("Future pedagogical work"). Open questions on [[Historical Order]], [[Quaestio]], [[Praxis]], [[Noesis]].

**History and verification** (**background**)
- Quotations, attributions and dates are recollections on [[Mathematics 1730 to 1900]], [[Greek Mathematics]], [[Babylonian Mathematics]], [[The Road to Calculus]], [[Mathematics 500 to 1500]], [[Mathematics 1900 to Today]]; each page's hard problems list what to check. [[Five Acts]]: the typology is interpretive.

### C. Suggested next jobs **[AI]**
1. *Primes* page: small, and four pages wait on it.
2. CPA and IQA: ready, formulas checked.
3. *Derivatives of exp, log, sin, cos with certificates*: the largest unlock in Change.
4. Induction (item 6) and proof in K3 (item 7): Murphy has just decided both principles; the pages are what is left.
5. Threshold cost theorems (item 2): the core problem, and the hardest.

### D. Deferred on purpose
The book plans of Part I.

---

## Guidelines for this vault

The vault does several things at once, all under one roof: **creaturely-realist, ultrafinite, Christian, well-taught mathematics.**

### 1. Document the new maths

Document all of the "new" maths in one place, each idea on its own canonical page.

- **Wildberger's Fourier analysis without transcendentals** — documented: [[Fourier Analysis]] (2026-10-11).
- **Wildberger's hyper-Catalan numbers**, which "solve" polynomials of degree above 5 by being realistic and anti-transcendental.
- **Constructible Trigonometry**, which avoids transcendentals (already documented in `Trigonometry/`).
- **Quadriga**, Murphy's answer to how to teach STEM: a riff on Polya ([[Quadriga for Mathematics]]; one page per art: [[Quaestio]], [[Noesis]], [[Praxis]], [[Apodeixis]]; and [[Twelve Exercises]], [[Four Kinds of Truth]], [[Quadriga and the Position]]). Documented; the proof types by grade, rubrics and a mathematics unit template are future pedagogical work.

Others' work gets the provenance tag `third-party`, is attributed by name, and is restated carefully and checked, not claimed.

### 2. Teach people without much math skill

The vault is meant to be usable by people without much math skill, building them up. This is putting the money where the mouth is, and a quiet rebellion against the way math has been taught and done for the last hundred years.

- Plain language first, then precision; define a term where it is first needed, and link to what it builds on.
- Every method gets a worked example with exact numbers.
- A page should be climbable by someone who has only read the pages it links to.

### 3. Write it all down first; books come later

All of this serves several books some day. **None of that is the goal now.** Murphy has already launched too soon at writing *Constructible Trigonometry*, *What is Math* and *Discrete Calculus* without laying everything out first. Math is broken enough that it has to be written down first.

- Pages are documentation, not draft chapters: no chapter order, page counts, or book prose.
- When tempted to draft a book, document the idea instead.
- The book plans below are **deferred**.

---

## I. Book plans (deferred — not the goal now)

| | Task | Where it's said | Status |
|---|---|---|---|
| a | **Write WIM Part II** — *Fallen and Finite · Creaturely Realism · Certificate Constructivism · Biblical Ultra-finitism* | WIM outline | headings only. **This vault is the raw material.** |
| b | **Write WIM Part III** — Quaestio · Noesis · Praxis · Apodeixis ("this is Polya's method") | WIM outline | headings only. The vault now has the material: [[Quadriga for Mathematics]] |
| c | **WIM Part I stubs** — zero/negatives/imaginaries; scientific revolution; calculus; multiple geometries; Cantor–Dedekind–Cauchy–Hilbert | WIM outline | one-line notes |
| d | **Infinity and Uncertainty** (Calculus with Stats) | Textbooks to write | file is empty |
| e | ***Exact Algebra*** | Textbooks to write | not started (spec exists) |
| f | *Statistics for Everyone*; *Calculus for Everyone* (text) | Textbooks to write | not started |
| g | ***A Discrete Bridge*** ch. 9–17 | [[SRC Constructible Trigonometry Textbook (md)]] outline | outline only |
| h | Confession §§ after ε: *Logs and exponents, e; Infinity—the continuum; Geometry; Algebra; Trigonometry; Calculus; Abstract Algebra; Probability, Statistics* | Confession last 8 lines | outline only |
| i | Precalc for Everyone: *Not Rational*; *Project: Are You For Reals?*; *Boolean Algebra*; *Abstract Algebra* | *Precalculus for Everyone* outline | empty |
| j | ISS: exact $r_{\max}$; 17-gon angles; sin/cos transition; vectors; spherical/hyperbolic constructibility | article's own "further avenues" | open |

## II. Problem notes (numbering is cited from other pages; status of each is on the Agenda)

### 1. Split the word "number" — **the point of the vault** — *answered (Murphy, 2026-10-10)*
The word *number* today is like the word *star* two thousand years ago: gas planets, rocky planets, stars and galaxies all went by one name ([[Number Hierarchy]]). **Murphy's answer: Numbers (levels 1–4), Lengths (5–6, admitted while tethered to geometry — the home of [[Constructible Trigonometry]]), Pixels (7–11), Posits (12–14) — see [[Numbers, Lengths and Pixels]].** The pixel: analytic geometry with smearing — we trust the graph of $y^3-x^2y+4x=0$ because the answer is owed only to a stated $\varepsilon$. The pixel doctrine is on that page (five points, marked [AI]); what remains is its hard problem 1 (genus versus species).

### 2. Make the threshold precise ("tempered") — a threshold *function*, not a number  — **core**
The biggest number is $10^{200}$, and the skepticism is a gradient, not a line ([[Creational Ultrafinitism]]). Ways to make that precise: (a) a fixed bound ($10^{200}$, with $10^{140}$ events as the physical argument); (b) a **band** with graduated skepticism; (c) a **resource-relative** notion — "feasible" relative to a stated budget (time, memory, energy, the age of the universe). **[AI]** (c) is how the *feasible-number* literature works — Parikh's "Existence and feasibility in arithmetic" (1971) gives a formal treatment in which "feasible" is a vague predicate closed under successor in a weak sense yet bounded — and it would let you *prove* things while keeping the sorites-style objection ("why not one more?") from being fatal. Also Sazonov's *feasible numbers*; Edward Nelson's *predicative arithmetic* and his essay on possible collapse of mathematics. **Check these before citing.** [[Creational Ultrafinitism]].

### 3. Define "certificate" — **answered (Murphy, 2026-10-10): a certificate is a procedure**
Each kind's "=" is the procedure its level affords; see [[Certificates]] for the definition, the four clauses of pixel equality and the Borwein lesson. The remaining work is the cost accounting and the literature check. The representation-relative refinement below survives, now as a description of the procedure's inputs and outputs. **[AI] Proposal:** a certificate is a triple *(representation, procedure, error bound/cost)*; "=" is claimed *relative to a representation* ((√2, length) exact; (√2, ℚ) asymptotic; (√2, decimal) algorithmic). This (i) resolves [[Equal Signs]], (ii) explains why the "same number" can sit at different levels, (iii) gives levels 13–14 a definite shape (the certificate is the *summation method*), and (iv) connects to **computational complexity**: a "certificate" in NP is something checkable cheaply even if hard to find — "creaturely mathematics = what can be *verified* within a bounded budget." That's an unusually natural bridge to the theory of computation; and Zeilberger-style experimental mathematics sits nearby.

### 4. A constructive Cantor  — **answered in [[Diagonal Argument]]**
The page states the procedural theorem with proof, a worked table, the finite version and the "sequences are certificates, not numbers" reading. Remaining: its four hard problems (which listings; computable listings; cost; whether to keep any cardinality language), and Murphy's call on one sentence of [[Infinity and Cantor]] ("almost all reals are provably beyond any finite description"). [[Infinity and Cantor]].

### 5. Calculus with infinitesimals as unmanageable reciprocals — **the big constructive project**
An infinitesimal is the reciprocal of a number past the threshold ([[Infinitesimals]]). Calculus is then first-order: dual numbers or discrete calculus with an explicit error term, and no excluded middle among the infinitesimals. **Written:** the first-order calculus ([[Calculus]]) and the five theorems of the Change ladder. **Not written:** see the Agenda, strand *Change*. **[AI]** Test case still open: $\int_1^e dx/x=1$ (the Level-9 definition of $e$; a bracket for $e$ exists on [[Number Hierarchy]]). This is the content *Infinity and Uncertainty* needs. See also [[Discrete Calculus]] (γ as "the cost of discretization").

### 6. What happens to induction?  — **principle answered (Murphy, 2026-10-22); the page work is open**
**A rule that permits one further step does not automatically justify an arbitrarily long iteration of that rule.** Induction certifies $P(k)$ by $k$ applications of the step, and each application has a cost; it does not certify "for all $n$" as a completed claim. The same point answers the sorites ("why not one more?": each step is fine, the iteration is what is not owed; [[Creational Ultrafinitism]], Esenin-Volpin). To write: [[Proof Types]] #8 and the infinite-primes remark restated as schemas; bounded induction worked with its cost; the budget form of a proof by induction.

### 7. Name your home logic — **answered (Murphy, 2026-10-22): three-valued logic**
The home logic is [[Three-Valued Logic]] (Kleene's K3): true, false, unknown, where unknown is "no certificate yet". The classical case is the subsystem with no unknowns. Infinitesimals fit directly: "$\varepsilon=0$" is unknown, not true and not false ([[Infinitesimals]]). To write: what a proof is in K3 (K3 has no tautologies, so validity is preservation of truth, not "always true"), and how proof by contradiction, bounded quantification and induction (item 6) read in it.

### 8. A geometry without continuity axioms — **medium**
What replaces Dedekind/Archimedean *completeness*? **[AI]** Aristotle's *potentially infinitely divisible* continuum (already in the Physics Textbook) — i.e., geometry as a *theory of constructions that can be refined as far as you like*. Read Hilbert's *Foundations of Geometry* (in your library) with that question; compare Wildberger. [[Geometry Hierarchy]].

### 9. Constructible trigonometry ⇄ Rational trigonometry — **medium, likely publishable**
Wildberger's *quadrance/spread* and your *slope/length* are two exact reformulations. Questions: are they equivalent? is one preferable pedagogically? Does the ISS cubic have a rational-trig formulation? Is there a *finite-geometry* extension? [[Constructible Trigonometry]].

### 10. Literature check on the novelty claim — **cheap, important before publishing**
me.md's AI analysis said it found no prior "creaturely realism" that grounds constructivism *theologically*. That claim was not backed by a search. **[AI]** Things to check: Poythress (*Redeeming Mathematics*, on your shelf), Kronecker ("God made the integers"), Weyl's *Das Kontinuum* (predicativism), Bishop's own remarks, Brouwer's idealism, the Christian philosophy-of-mathematics literature (Nickel's *Mathematics: Is God Silent?* is cited in your 2020 essay), and finitist Christian writers. If the niche is empty, *say so with citations*.

### 11. Unify the Catechism and the Confession — **small**
Catechism = Q&A for students; Confession = numbered statements for teachers. Finish both; decide whether the Confession's later sections (calculus onward) are replaced by this vault's content.

### 13. Probability and statistics, finitely — **begun**
Measure theory is rung 6 of the Change ladder and rejected-adjacent. **Begun:** [[Constructible Statistics]] (seven exact results), [[Statistics]], [[Probability]]. **[AI]** Finite probability + sampling distributions with explicit error bounds is exactly "certificate-explicit statistics"; the remaining work is on the Agenda, strand *Measurement*.

### 14. Levels 13–14: what's a convention-certificate? — **small/medium**
Cesàro, Abel, zeta-regularization are *named summation methods*. Make the "certificate" literally the method's name + its regularity theorem. [[Number Hierarchy]]; level 14 is begun on [[Function Hierarchy]] (analytic continuation).

### 15. More triangle cases for [[Constructible Trigonometry]] — **small, planned**

Two cases with no formulas worked out yet. Each was checked to be well-posed: **one triangle or none, not ambiguous**.

- **CPA** (circumradius $R$, perimeter $P$, wedge $A$). $R$ and $A$ fix the opposite side, $a=2R\,m_A/\ell_A$ (as in [[CAS Trigonometry]]). Then $b+c=P-a$ is known and the [[Law of Lengths]] gives $bc=\dfrac{\ell_A\bigl((P-a)^2-a^2\bigr)}{2(\ell_A+1)}$, so $b,c$ are the roots of $x^2-(P-a)x+bc=0$. Existence: $P>2a$ and a nonnegative discriminant, $(1-\ell_A)(P-a)^2+2\ell_A a^2\ge0$. It is the article's SPA case with $a$ computed first. Check: $R=\tfrac{65}8$, $P=42$, $m_A=\tfrac43$ gives $a=13$, $b+c=29$, $bc=210$, so $b,c=15,14$. Needs a new letter **P** in the hub's convention table.
- **IQA** (inradius $r$, area $Q$, wedge $A$). $s=Q/r$ and the tangent length from $A$ is $s-a=r/m_{A/2}$, so $a=Q/r-r/m_{A/2}$. Then $(a,Q,A)$ is [[SQA Trigonometry]]. It is not overdetermined: $s$ is the one positive root of $s^2-as-Q/m_{A/2}=0$, so the SQA triangle automatically has inradius $r$. Existence: $Q\le a^2/(4\,m_{A/2})$. Check: $r=4$, $Q=84$, $m_A=\tfrac43$ gives $a=13$, then $b,c=15,14$.

Neither is the QCS type of ambiguity: there a wedge is fixed only through $m/\ell$, so it and its supplement both fit; here $A$ is given outright. Other mixes of two scale quantities (QIS, QIC, ICS) have not been examined.

## III. Housekeeping

1. **Reading list:** the full list is [[Reading List]]. Poythress; Hilbert *Foundations of Geometry*; Bishop *Constructive Analysis*; Knuth *Surreal Numbers* (a rival "constructive-ish" number system worth positioning against).
