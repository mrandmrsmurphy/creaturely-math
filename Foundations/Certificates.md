---
title: Certificates
aliases:
  - Certificate Constructivism
  - Certificate-Explicit Constructivism
type: concept
status: canonical
provenance: "murphy (framework; the definition — a certificate is a procedure — and the four clauses of pixel equality, 2026-10-10) + ai-synthesis (classroom formulations; the table; the Borwein figure to verify)"
sources: "Murphy's raw mathematics draft (2026-05); his Constructible Trigonometry textbook"
updated: 2026-10-11
---

# Certificates (certificate-explicit constructivism)

*This page is the concept. The position built on it, **certificate constructivism** (certificate-explicit constructivism), is one of the three legs with [[Creaturely Realism]] and [[Creational Ultrafinitism]]. Unlike the standard constructivist schools it asks for a stated warrant at every "=", at every level of the [[Number Hierarchy]], and does not by itself limit scale (that is the third leg).*

**How we know and build mathematics.** Every equality is a *claim*; every claim needs a stated kind of *warrant* — a **certificate**.

> **The rule:** *Before any equals sign — "What is your certificate?"*

## Definition (Murphy)

**A certificate is a procedure.** What "=" means at each level of the [[Number Hierarchy]] *is* the procedure that level affords:

| Kind | "=" is decided by | Example |
|---|---|---|
| **Number** (levels 1–4) | a finite check | $a/b=c/d\iff ad=bc$ |
| **Length** (5–6) | exact arithmetic in $\mathbb K$ | $\sqrt8=2\sqrt2$, by squaring: $8=4\cdot2$ |
| **Pixel** (7–11) | one inequality, at a stated resolution | agreement to $n$ digits; apartness at the first disagreeing digit |
| **Posit** (12–14) | the named convention | the Cesàro $\tfrac12$ versus the zeta $-\tfrac1{12}$ |

The kinds are Murphy's names ([[Numbers, Lengths and Pixels]]). The kinds of procedure, from the raw notes:

- you can *exhibit* it (a count; a reduced pair $(a,b)$ with $\gcd=1$);
- you can *construct* it (compass and straightedge; closure under $+,-,\times,\div,\sqrt{}$);
- you can *converge* to it with an algorithm and a stated error bound;
- you can *assign* it by a stated convention (Cesàro, analytic continuation);
- or you can only know *that it exists* (diagonalization; Chaitin's Ω).

See [[Number Hierarchy]] for the 14 levels and [[Equal Signs]] for how this lines up with the three-equal-sign catechism. The definition gives each kind its own "=" the way Bishop defines a set — by how a member is constructed and by what equality of two members means (*Foundations of Constructive Analysis*, ch. 1; recollection, to check; on the [[Reading List]]).

## Pixel equality: the four clauses (Murphy)

No one has ever generated infinite digits to compare. A comparison is of finite numeral lengths; the cost accumulates, but it is never impossible. So, for Pixels:

1. **Apartness by computation** — a discovered difference, at whatever digit it shows up.
2. **Agreement at a stated resolution** — this is all "=" ever means between Pixels, and it carries its cost history with it.
3. **Exact equality, when claimed, is proved about the generating rules** — never established by comparing outputs.
4. The classical theorem that equality of algorithmic numbers is undecidable is accepted as a **procedural negative** (like the diagonal, [[Diagonal Argument]]): no certificate stated in advance covers all pairs.

**The Borwein lesson.** The Borwein integrals — products of sinc factors — agree with $\pi/2$ digit after digit, up through $\operatorname{sinc}(x/13)$; adding the $\operatorname{sinc}(x/15)$ factor betrays a difference only around the eleventh digit (a gap of about $2.3\times10^{-11}$; standard reported figure, to verify). Two certificates can agree at every resolution anyone has paid for, until someone pays for more. That is why clause 2 is all there is.

**The 9-tail belongs to the twilight.** At any point where you quit writing 9's in $0.4999\ldots$, you are not equal to $\tfrac12$. The equality $0.4999\ldots=0.5$ is a claim about completed expansions (level 11), not about Pixels; no tail convention is needed below the twilight.

## The bargain

> Every step up is a **bargain**: we weaken what "equals" means; we gain expressive power. The cost is that we **must name the certificate type**, or we are equivocating.

Standard analysis collapses levels 7–12 into one object, **ℝ**, with one "=", and "charges nothing for the move." That is the **bamboozlement**: borrowing the certainty of level 2 to spend at level 11. Without a certificate discipline, proponents of admitting divergent sums and zeta assignments "rightly complain that it makes no sense to exclude them" — the discipline is what lets you admit them *honestly*, as conventions.

## Consequences

- **Debate Math.** Mathematics as argument about what you are entitled to claim and on what grounds. Students learn that $2+2=4$ and $\sum 1/n^2=\pi^2/6$ are not the same *kind* of claim.
- **Proof by construction** is the gold standard at every level. **Proof by contradiction** is permitted to prove a **negative**. A negative result is not a positive proof of the existence of something else: that no $a/b$ with $a,b$ natural squares to $2$ is accepted, but it does not prove that irrational numbers exist as another class of numbers. $\sqrt2$ is exhibited by the diagonal of the unit square ([[Number Hierarchy]], level 5). The diagonal argument is likewise accepted as a negative result ([[Infinity and Cantor]]).
- **Against the four schools**: *logicism* (certificates aren't syntax-derived); *formalism* (a certificate isn't a mechanical rule but a claim about what kind of thing you hold); *intuitionism* (right criterion, wrong ground: objects are real before we construct them, construction is our *access* not their *cause*); *ZFC* (name the cost of every upward move). Details in [[Schools Compared]].

## In the classroom

- "Why does 0.999… = 1?" → *What's your certificate?* $0.999\ldots$ is not a well-formed number: it is a level-11 object (a limit) and would require infinite work. Only if you grant the infinite limit concept is it coherent, and then it equals $1$. See [[Equal Signs]].
- Doxological payoff: the student who knows what certificate she needs is reading a book, not pushing symbols. Q.E.D. is "a little eschatology: *I have demonstrated what was already true, and I did not make it so.*"

## Open

The definition is settled (above). Remaining: the **cost accounting** — budget functions for time and space, and the feasible-number literature (Parikh, Sazonov, Nelson) to check. Item 3 in [[Future Directions]].
