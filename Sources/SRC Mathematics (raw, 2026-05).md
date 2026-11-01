---
title: "Mathematics (Murphy, raw)"
type: source
status: verbatim snapshot (do not edit; edit the canonical notes instead)
provenance: murphy
date-written: "2026-05-07 (ingested; file touched 2026-06-25)"
snapshot: 2026-10-07
---

> [!info] Source snapshot
> Murphy-authored. The 14-level number hierarchy and the four views (Number, Geometry, Structure, Change, Tools). Primary source for [[Number Hierarchy]], [[Three Tiers]], [[Structure Hierarchies]].

# Mathematics
*Mathematics is the human study of number, shape, structure, and change, together with the systematic study of the tools used in mathematics.*  It asks not just "what is the answer?" but "what kind of thing is this, why does it behave as it does, and what can we know about it?"


We contrast this with **arithmetic** which is the computation of calculable values by exact algorithms, within a given system.  A very related field is Computer Science (CS).  In that domain, execution of a program is like arithmetic, whereas studying how to make and understand programs is CS proper.

> **Arithmetic** is the computation of calculable values by exact algorithms within a stated system. Its criterion of success is correctness — it either works or it does not.

> **Mathematics** is the human study of number, shape, structure, and change, together with the tools developed in that study. Its criterion of success is understanding — not just _that_ something is true but _why_ it is true and _what kind of thing_ it is.

> **Metamathematics** is the study of mathematics itself — its foundations, its limits, its tools, and its nature. It is mathematics becoming self-aware. Its criterion of success is grounded-ness — not just _why_ something is true within a system but _what the system is_ and _what we are entitled to assume_.


## Number-view
One avenue into mathematics is Number Theory, Discrete mathematics, and Combinatorics.  We should begin by exploring what "=" means, and how more and more has been subsumed under the rubric "number".

#### The Exhibitable Numbers (Exact Equality Certificates)

**1. Natural Numbers $\mathbb{N}$** — Counting. The certificate is the count itself.
**2. Whole Numbers $\mathbb{W}$** — Add zero. The philosophical leap is larger than it looks.
**3. Integers $\mathbb{Z}$** — Add direction/sign.
**4. Rational Numbers $\mathbb{Q}$** — Add exact division where possible. Certificate is the pair (a,b) with gcd⁡(a,b)=1. $\frac{a}{b}=\frac{c}{d}$ iff $ad=bc$.

---
#### The Geometric Numbers (Inequality Certificates; Equality is Asymptotic)

**5. Constructible Numbers $\mathbb{K}$ ** — Compass and straightedge. Closed under +,−,×,÷,√. The Galois group here is a 2-group — every constructible number sits in a tower of degree-2 extensions over $\mathbb{Q}$.
**6. Origami Numbers $\mathbb{F}$** — Folding adds cube roots and some cubics. Galois groups now include degree 3. This is where $\sqrt[3]{2}$​ lives — inaccessible to compass but reachable by fold.

---
#### The Galois Boundary

*This is the wall Abel and Galois identified. Levels 5 and 6 correspond precisely to polynomials **solvable by radicals** of degree $\leq 4$. The quintic is the first polynomial whose general solution cannot be expressed in radicals — its Galois group $S_5$​ is not solvable. This is a **hard structural boundary**, not a matter of computational convenience.*

**7. Jiǔ Zhāng Numbers $\mathbb{J}$**  — n-th roots with a *determinate digit algorithm*. Digits produced in guaranteed order. Certificate at each step is exact to stated precision. Includes $\sqrt[5]{2}$​ (a specific radical) but *not* the general quintic solution.  Follows an algorithm first described in the 九章算術/Jiǔ Zhāng Suànshù (Chapter 4, _Shaoguang_).

---

#### The Algorithmic Numbers (Convergence Certificates; Equality Replaced by Agreement-to-n-Places)

**8. Algebraic Numbers $\mathbb{A}$** — Polynomial roots via Newton's method. Certificate is approximate and potentially chaotic — convergence is not guaranteed without analysis of the specific case. The *same object* as level 7 when it exists there; first appears here for general algebraic numbers like quintic roots.
	The key distinction from level 7: the algorithm does not guarantee correct digits in order. It may overshoot, correct, overshoot again.
**9. Transcendental Geometric Numbers $\mathbb{T}$** — Geometrically *defined* first, analytically *computed* second. The primary certificate is a geometric construction or measurement; numerical value requires algorithmic computation. This level is very rich and not fully enumerated — the following are representative kinds:
- **π** — ratio of circumference to diameter of any circle
- **$e$** — the value of $x$ such that the area bounded by $y=1/x$, $y=0$, $x=1$, and $x=?$ equals 1 (the unit-area point on the unit rectangular hyperbola $xy=1$)
- **Elliptic integrals** $E(k)$ — arc lengths of ellipses with eccentricity $k$; each distinct eccentricity yields a transcendental believed independent
- **Arc lengths of polar curves** — e.g., the lemniscate constant $\varpi$ from the lemniscate of Bernoulli $r^2 = 2\cos(2\theta)$; the elliptic analogue of π
- **Surface areas of geometric solids** — e.g., sections of paraboloids, oblate/prolate spheroids
- Note: $\zeta(2) = \pi^2/6$ belongs here despite its series form, because its primary certificate is geometric (it reduces to π).

**10. Series Numbers $\mathbb{S}$** — Defined *primarily* as the result of summation processes, with no known geometric primary definition. *e* has moved to Level 9 (see above). The canonical example here is **Apéry's constant** $\zeta(3) = \sum_{n=1}^{\infty} \frac{1}{n^3} \approx 1.20206\ldots$ — proven irrational (Apéry, 1978), not proven to be transcendental, and with no geometric primary definition known. The series is the certificate.
**11. Limit Numbers $\mathbb{L}$** — Numbers whose primary certificate is a limiting process that is neither a geometric construction nor a convergent series. The canonical examples:
- **Feigenbaum constants** ($\delta \approx 4.669...$, $\alpha \approx 2.502...$) — limits of ratios in the period-doubling bifurcation sequence of iterated maps; no known series representation; the process is dynamical, not geometric or summation-based. Not known to be transcendental.
- **Euler-Mascheroni constant** $\gamma \approx 0.5772...$ — $\lim_{n\to\infty}(H_n - \ln n)$, the gap between the harmonic series and its continuous analogue; primary certificate is a limit involving $\ln$ (Level 9), not purely a series. Not known to be irrational. Has series representations but the limit is the natural home.
- *Note*: transcendental functions ($\sin, \exp, \log$) also live at this level as objects — defined by limiting processes and producing Level 9 or Level 10 values when evaluated at specific inputs. But this list is about numbers, not functions.

---

#### The Twilight Numbers (Existence Without Exhibition)

**12. Uncomputable Numbers $\mathbb{U}$** — Logical existence provable (e.g. by Cantor/diagonalization arguments, which you accept as *negative* results even if not as existence proofs), but no algorithmic certificate possible even in principle. Chaitin's Ω lives here.
**13. Divergent Numbers $\mathbb{D}$** — Reassigned by explicit summation conventions. $1-1+1-1+\cdots = \frac{1}{2}$​ under Cesàro summation. The certificate is the *summation method itself*, which must be stated or the expression is meaningless. The $\frac{1}{2}$​ here is a *different kind of object* than the $\frac{1}{2}$​ in $\mathbb{Q}$.
**14. Zeta Numbers $\zeta$** — Analytic continuation assignments. $1+2+3+\cdots = -\frac{1}{12}$ under analytic continuation-regularization. The $-\frac{1}{12}$​ here is not the $−\frac{1}{12}$​ in $\mathbb{Z}$. Same notation, utterly different certificate.

---

### The Central Insight

Every transition in this hierarchy is a **bargain**:

> _We weaken what "equals" means. In exchange, we gain expressive power. The cost is that we must state the certificate type explicitly, or we are equivocating._

The $\mathbb{R}$ of standard mathematics tries to collapse levels 7 through 12 into one object with one equality relation, and then *charges nothing* for the move. That is the bamboozlement.
Mathematics progresses by admitting new objects only when accompanied by a clearly stated weakening of equality, together with explicit certificates appropriate to that weakening.  Without this certificate process, proponents of admitting 13 and 14 rightly complain that it makes no sense to exclude them.

## Geometric View
### Geometry
1. Incidence (lies on)
2. Affine (parallel)
3. Ordered (is between)
4. Congruent (congruence)
5. Metric (distance)
6. Euclidean/Hyperbolic/Spherical (perpendicular)
7. Analytic (has coordinates)
Rational Trigonometry
Topology, but not what is has become.  Combinatorial typology is valid.

## Structure
### Algebra (in the full, non-high school sense)
1. Magma
2. Semi-group
3. Monoid
4. Group 
	1. Abelian
5. Ring
	1. Commutative
6. Integral Domain
	1. UFD
	2. PID
7. Field
Category theory is this plus Tools.

## Change
Calculus and Non-Standard Analysis
1. Discrete
2. Non-Standard Analysis (ε)
3. Non-Standard Complex Analysis (removing poles)
4. Combinatorial Analysis
5. ε-δ Analysis
6. Measure Theory
7. Dirac delta
8. Naked Infinities

## Tools
### Logic
1. Finite T vs F
2. Three-Value
3. Syllogisms
4. Predicate Logic
5. First-Order
6. Para-consistent Logic
7. Second-Order
8. Modal Logic
9. Type theory
10. ZFC
11. Large Cardinals

## Contrast with Math Today

|                                  | **Classical **                                                 | **Modern **                                   |
| -------------------------------- | -------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| **What a number is**             | A thing with a nature, defined by how it can be exhibited or certified                       | A node in a structure, defined by its relations to other nodes               |
| **What $\frac{1}{2}$ means**     | A ratio of two discrete magnitudes; certificate is the pair $(1,2)$                          | An equivalence class of pairs $(a,b)$ under $(a,b)\sim(c,d)$ iff $ad=bc$     |
| **What $\sqrt[5]{2}$ means**     | A quantity approximatable by the Jiǔ Zhāng algorithm; certificate is stepwise              | The unique real root of $x^5-2=0$; certificate is "satisfies the polynomial" |
| **What equality means**          | Same certificate type, same value. Different certificates = different kinds of objects       | Same place in the structure. Different paths to the same node are irrelevant |
| **The teacher's job**            | Lead the student to apprehend the *nature* of the object                                     | Train the student to manipulate the formal system correctly                  |
| **Criterion of success**         | Understanding — *what kind of thing is this?*                                                | Provability — *what follows from the axioms?*                                |
| **The role of construction**     | Primary. To exist is to be constructible with a stated certificate                           | Secondary. 'Existence' means "consistent with ZFC"                             |
| **$1-1+1-\cdots = \frac{1}{2}$** | A different kind of object, assigned by convention; not the $\frac{1}{2}$ of $\mathbb{Q}$    | A true statement under Cesàro summation; context handles the overload        |
| **The Continuum Hypothesis**     | A real question about the nature of infinity; "independent" means our tools are insufficient | A pseudo-question; pick your axiom and move on                               |
| **Gödel's incompleteness**       | Confirmation that formal systems are incomplete guides to truth                              | Boundary condition; we work inside the system anyway                         |
| **Metaphysical stance**          | Realist. Mathematical objects exist and have natures we discover                             | Formalist / Structuralist. Objects are defined by their role in a system     |
| **The PhD's question**           | *What is the nature of the thing I am teaching?*                                             | *What can I prove within the framework?*                            |
