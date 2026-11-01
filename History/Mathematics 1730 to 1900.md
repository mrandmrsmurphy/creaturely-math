---
title: Mathematics 1730 to 1900
type: history
status: "canonical (draft; every date, attribution and quotation is from recollection and to be checked)"
provenance: "murphy (the frame: the post-calculus period up through Cantor as the pinnacle of hubris, a modern Tower of Babel; the credit to God of earlier generations replaced; a program of rigorous proof without yet the apparatus to carry it out, including the hand-waving acceptance of infinite work in Dedekind cuts; the collapse in the foundations debates and the multiple geometries; the whole from Kline; concurrent with the Huxley project of rewriting history in the secular humanist vein) + ai-synthesis (the timeline, the strands, the worked examples, the qualifications, the flagged problems)"
sources: "[[The Road to Calculus]], [[Five Acts]], [[Greek Mathematics]], [[Infinity and Cantor]], [[Diagonal Argument]], [[Christians and the Reals]], [[Corrective Narrative]], [[Historical Order]]"
updated: 2026-10-10
---

# Mathematics 1730 to 1900

The sixth stage of [[Historical Order]]: from the aftermath of Newton to **Cantor** and the turn of the twentieth century. It is the **Promethean** posture of [[Five Acts]] at full height, the pinnacle of mathematical confidence, and the setting for the **unmasking** that follows. All dates, attributions and quotations are from recollection and **to be checked**. The account of the collapse is Kline's (*Mathematics: The Loss of Certainty*, 1980).

## The hinge: Pope, 1730

Pope's epitaph for Newton (1730):

> *Nature and Nature's laws lay hid in night: / God said, Let Newton be! and all was light.*

[[Five Acts]] reads the couplet as the whole of the Promethean posture in two lines. Two features: **God does the saying**, so credit is still given; yet the whole of the *light* goes to the man. A later wit completed it (J. C. Squire, 1926; recollection): *It did not last: the Devil howling "Ho! Let Einstein be!" restored the status quo.* The previous generations (Kepler, Boyle, Newton himself) credited God for the intelligibility of nature; the period that follows steadily stops saying so.

## Murphy's frame

1. **The pinnacle of hubris, a modern Tower of Babel** ([[Five Acts]], Gen 11): a single system of reason reaching to heaven, to be built from the human mind.
2. **A programme of rigorous proof without the apparatus to carry it out.** The age sets out to put analysis on an unshakeable footing, but it lacks the **logic** (a precise predicate logic, a theory of sets with a safe rule of construction) and **hand-waves** the infinite: the acceptance of a **completed infinity** inside the definition of the real numbers (Dedekind's cuts, Cantor's sequences), without noticing what is being assumed.
3. **It comes down** in the debates on the foundations and in the **multiple geometries**: the certainty of mathematics, its crown, is lost.
4. **It is concurrent with the Huxley project** of rewriting history in the secular humanist vein ([[Corrective Narrative]]).

## A qualification up front [AI]

The hubris is **a current of the age and of its programme, not a trait of each person in it.** Several of the founders of rigour were devout: **Cauchy**, a Catholic royalist who lost his posts after 1830 for refusing an oath; **Riemann**, the son of a Lutheran pastor; **Boole**, who thought of logic as the laws of thought and wrote on theology; **Hamilton**; and **Cantor** himself, a Lutheran who defended the transfinite as consistent with Christian doctrine and corresponded with theologians (recollection; [[Infinity and Cantor]]). **Kronecker** opposed Cantor on grounds close to the vault's. So the claim is about **the programme and its rhetoric**, which are documented below. That keeps the account fair to the people and sharp on the idea.

## Timeline (approximate)

| Date | Event |
|---|---|
| 1730; 1748; 1755 | Pope's epitaph; Euler, *Introductio in analysin infinitorum*; Euler's *Institutiones calculi differentialis* |
| 1788 | Lagrange, *Mécanique analytique*: no figures |
| 1796; 1801 | Gauss constructs the regular 17-gon; *Disquisitiones Arithmeticae* (congruence notation $\equiv$) |
| 1817; 1821 | Bolzano's proof of the intermediate value theorem; **Cauchy**, *Cours d'analyse* (limits, continuity) |
| 1822; 1824 | **Fourier**, *Théorie analytique de la chaleur*; Abel on the unsolvability of the quintic |
| 1826 | Abel finds a counterexample to Cauchy's sum theorem |
| 1829–1832 | **Lobachevsky** and **Bolyai**: non-Euclidean geometry; Galois (d. 1832) |
| 1837; 1843 | Wantzel: no trisection of an angle, no doubling of the cube; **Hamilton**'s quaternions |
| 1844 | Liouville's first transcendental numbers |
| 1854 | **Riemann**: geometry of curved spaces; the Riemann integral; Boole, *The Laws of Thought* |
| 1859 | Darwin, *Origin of Species* |
| 1860s | Weierstrass's lectures ($\varepsilon$–$\delta$); the X Club (1864); Beltrami's model of non-Euclidean geometry (1868) |
| 1872 | **Dedekind**, *Continuity and Irrational Numbers*; Cantor's construction by sequences; Weierstrass's continuous nowhere-differentiable function |
| 1873; 1882 | Hermite: $e$ is transcendental; **Lindemann**: $\pi$ is transcendental (the circle cannot be squared) |
| 1874; 1878 | Cantor: the reals are uncountable; the continuum hypothesis; Draper's *History of the Conflict between Religion and Science* (1874) |
| 1879; 1889 | Frege, *Begriffsschrift*; Peano's axioms |
| 1883; 1891 | Cantor, *Grundlagen*; the **diagonal argument** |
| 1886 | Kronecker's "God made the integers" (as reported) |
| 1895–1897 | Cantor's transfinite numbers; the Burali-Forti paradox |
| 1896 | A. D. White, *A History of the Warfare of Science with Theology* |
| 1899; 1900 | **Hilbert**, *Foundations of Geometry*; the Paris problems, with "no *ignorabimus*" |

(The **collapse** proper, Russell's paradox of 1901 and Gödel's theorems of 1931, belongs to the next stage.)

## Five strands

### 1. Calculus becomes analysis: the rigour movement

The 18th century (Euler, Lagrange, Laplace) computed with infinitesimals and series with astonishing success and little justification ([[The Road to Calculus]]). **Fourier's** heat theory (1822) forced the question *what is a function?* and which functions have series. **Cauchy** (1821) defined limit and continuity; **Bolzano** earlier; **Weierstrass** made the $\varepsilon$–$\delta$ form standard. The aim was to replace the "ghosts" of Berkeley with certificates.

**Cauchy was wrong at once, and it was found.** His theorem that a convergent series of continuous functions has a continuous sum fails: the continuous functions $f_n(x)=x^n$ on $[0,1]$ converge, for each $x$, to $0$ for $x<1$ and to $1$ at $x=1$, a **discontinuous** limit. The convergence is not *uniform*: at $x=1-\tfrac1n$ the value is $(1-\tfrac1n)^n$, which tends to $\tfrac1e\approx0.3679$ (computed: $0.3487$, $0.3660$, $0.36770$, $0.367879$ for $n=10,10^2,10^3,10^6$), so the largest value of $x^n$ below $1$ stays at about $1$ however large $n$ is. Abel noted the counterexample in 1826; the concept of uniform convergence followed.

**Intuition fails: continuous but nowhere differentiable** (Weierstrass, 1872). $W(x)=\sum a^n\cos(b^n\pi x)$ with $0<a<1$, $b$ an odd integer and $ab>1+\tfrac{3\pi}2$. With $a=\tfrac12$, $b=13$ ($ab=6.5>5.71$), the difference quotient of a 14-term sum at $x=0.3$, for steps $h=13^{-k}$, is
$$-9.6,\ 73,\ 195,\ -2780,\ -16956,\ 130405,\ 342556,\ -5039116\qquad(k=1,\dots,8),$$
growing in size and changing sign: no tangent (all computed; a finite partial sum, and the pattern is the point). Fourier's physics and Weierstrass's monsters are the pressure that made rigour necessary.

### 2. Arithmetization and the real numbers

The programme (Weierstrass, Dedekind, Cantor, Méray): found analysis on **arithmetic**, with no appeal to geometric intuition, by *constructing* the reals from the rationals.

**Dedekind's cut** (1872): a cut is a split of the rationals into a lower set $A$ and an upper set $B$. For $\sqrt2$ take $A=\{q: q\le0\text{ or }q^2<2\}$ and $B=\{q>0:q^2>2\}$. **A worked proof that there is no largest element of $A$** uses the map $q\mapsto q'=\dfrac{2q+2}{q+2}$, for which
$$q'^2-2=\frac{2(q^2-2)}{(q+2)^2},\qquad q'-q=\frac{2-q^2}{q+2}.$$
So if $q\in A$ then $q'\in A$ and $q'>q$; and if $q\in B$ then $q'\in B$ and $q'<q$ (checked in exact fractions: $1\mapsto\tfrac43\mapsto\cdots$; $\tfrac75\mapsto\tfrac{24}{17}$; from above $\tfrac32\mapsto\tfrac{10}7$). That is a **procedure** producing rationals ever closer to $\sqrt2$ from each side.

**What the vault accepts and what it refuses** [AI]:

- **Accepted, as a label only:** a cut *given by a rule*, with the improving procedure above, is a **convergence certificate**: a way of printing more digits, **never completed and never an exhibit**. $\sqrt2$ itself is exhibited otherwise, by a finite equation with an isolating interval or a constructed length, and the cut adds nothing to that ([[Exhibiting a Real]]; [[Numbers, Lengths and Pixels]]).
- **Refused:** the **set of all cuts** as the completed ℝ. The definition quantifies over *every* set of rationals and treats the infinite set $A$ as a finished object; and (as Dedekind's text says, in recollection) when a cut is not produced by a rational, "we **create** a new irrational number". That is **existence by fiat**, the thread of [[Greek Mathematics]] (section 2); Cantor's version is that "the essence of mathematics lies precisely in its **freedom**" (*Grundlagen*, 1883; recollection), limited only by consistency. Hilbert's 1899 letter to Frege put it as consistency *is* existence.

This is the **hand-waving** Murphy points to: the arithmetization was meant to remove all intuition, and it installed a completed infinity without saying so. In his words: **the replacement of exhibitable certificates by faith in something that varies from object to object, with only the trivial cases ever used**, so that no one can exhibit one of the irrationals the definition promises, beyond the countably many with names ([[Exhibiting a Real]]).

### 3. Cantor and the transfinite

**Cantor** (1874) proved the reals uncountable, and (1891) gave the **diagonal argument** ([[Diagonal Argument]]); then built a hierarchy of infinite numbers ($\aleph_0,\aleph_1,\dots$) and conjectured the continuum hypothesis (1878). Reception was split. **Kronecker**, the opposition: "God made the integers; all else is the work of man" (reported, 1886), and he called Cantor a "corrupter of youth" (recollection); Poincaré and others called the transfinite a disease; **Hilbert** answered that no one would expel mathematicians from the paradise Cantor had made (1925, later). Cantor, a Christian, believed the transfinite numbers had a reality in the mind of God and defended them to theologians. **The vault's reading** is in [[Infinity and Cantor]] and [[Christians and the Reals]]; the point here is the history: **a Christian mathematician extends mathematics into the actual infinite, claiming divine warrant, while a Christian mathematician (Kronecker) opposes him** on the ground that creatures make constructions. Both appeal to God.

### 4. Multiple geometries, and multiple algebras: the loss of certainty

For two thousand years Euclid's geometry was *the* true description of space, and for Kant (1781) its truth was **necessary**. Then:

- **Non-Euclidean geometry** (Lobachevsky 1829, Bolyai 1832, Gauss privately, Riemann 1854): changing the parallel postulate gives a **consistent** geometry; Beltrami (1868) and Klein (1871) built models *inside* Euclidean geometry, so each geometry is as consistent as the other. Which describes *space* became an empirical question (Einstein, 1915, uses Riemannian geometry).
- **A triangle with three right angles** exists on a sphere (the octant: the pole and two points of the equator a quarter-turn apart), so the angle sum there exceeds two right angles by exactly one, and its area is the excess times the square of the radius: $\tfrac{4\pi R^2}{8}=\tfrac\pi2R^2$ against $3\cdot\tfrac\pi2-\pi=\tfrac\pi2$ (checked). Euclid's theorem of the angle sum is not a law of geometry but a **consequence of one postulate**.
- **Quaternions** (Hamilton, 1843): an algebra where $ij=k$ and $ji=-k$ (checked), so **order matters**; the first noncommutative multiplication in the arithmetic of numbers. Boole's algebra of logic (1854) had $1+1=1$ ([[Boolean Algebra]]).
- **Hilbert's** *Foundations of Geometry* (1899) finally listed the **hidden assumptions** of Euclid (betweenness and continuity, Pasch) and proved their independence ([[Greek Mathematics]], section 1).

Kline's argument: when geometry, the paradigm of certain knowledge, turned out to be one among several, **the claim that mathematics reveals necessary truths about the world collapsed**, and the foundations were rebuilt on arithmetic, which then also failed (next stage). For [[Historical Order]], this is the period in which "proof from first principles" ceased to be a safe ground.

### 5. The century of impossibility, and of structure

A different and lasting gift: the period learned **what cannot be done**, by proof.

- **Abel and Ruffini** (1820s): no general solution of the quintic by radicals; **Galois** (d. 1832): the reason, in the **group** of a polynomial ([[Fundamental Theorem of Algebra]], the "Galois boundary").
- **Wantzel** (1837): the cube cannot be doubled nor the angle trisected by ruler and compass, because constructible numbers have degree a power of two ([[Constructible Numbers]]); and **Gauss** (1796) had constructed the regular 17-gon, whose $\cos\tfrac{2\pi}{17}$ is a nested radical (checked numerically: the standard formula gives $0.932472\ldots$ matching the cosine).
- **Liouville** (1844) constructed the first transcendental numbers; his constant $\sum10^{-k!}=0.110001000000000000000001\ldots$ has $1$s at places $1,2,6,24,\dots$ (checked). **Hermite** (1873) proved $e$ transcendental; **Lindemann** (1882) proved the same of $\pi$, which settles that **the circle cannot be squared**, and which is also what lets the vault treat $\pi$ as an **indeterminate** over every algebraic number ([[Exact Until Output]]).

The vault values this strand: an impossibility proof is a **certificate of a negative**, the kind it accepts ([[Certificates]]).

## The evidence of hubris [AI; all from recollection, to check]

| Statement | Who, when | Reading |
|---|---|---|
| "The sole end of science is the honour of the human spirit" | Jacobi to Legendre, 1830, answering a remark that mathematics should serve public utility (via Fourier) | purpose is human glory, not neighbour or God; compare the applied-versus-pure remarks of [[Mathematics 500 to 1500]] |
| "We **create** a new irrational number" | Dedekind, 1872 | existence by fiat |
| "The essence of mathematics lies in its **freedom**" | Cantor, 1883 | unconstrained creation, limited by consistency |
| "In mathematics there is **no *ignorabimus***": every problem can be solved | Hilbert, Paris, 1900 | the claim to a God's-eye completeness; [[Greek Mathematics]], section 1 |
| Comte's three stages: theological, metaphysical, **positive** (1830–1842) | the philosophy of the age | a secular history of knowledge in which religion is a stage to be left |

**Contrast** the posture of the previous stage: Kepler thinking God's thoughts after him ([[The Road to Calculus]]) against Hilbert's "we must know, we will know" (1930, a little later). That is the Promethean posture against the sapiential one.

## The Huxley project, concurrent [AI]

The same decades produce the **conflict thesis** and the retelling of history in which religion is the obstacle:

- Washington Irving's *Life of Columbus* (1828) popularised the claim that the medieval Church taught a flat earth (the myth, as Russell and others document; recollection).
- Darwin (1859); the **X Club** (1864) of Huxley, Hooker, Tyndall and others, who worked to put science into secular hands and institutions; the Huxley–Wilberforce exchange (1860) retold as a victory.
- **Draper** (1874) and **White** (1896) supply the narrative: *the Dark Ages*, *Galileo*, *the warfare of science and theology*.
- **Peter Harrison** shows the narrative fails and that "science" and "religion" are modern categories ([[Greek Mathematics]], section 3; [[Reading List]]).

The **parallel** with mathematics is Murphy's point: the foundations story ("we have put certainty on rigorous arithmetic") and the history story ("science freed itself from religion") are **twin products of one confidence**, and both are the Promethean posture. The history of mathematics in particular was rewritten as a march of rigour from the Greek miracle to Hilbert, in which Babylon, India, China and the medieval world are omitted ([[Corrective Narrative]]).

## What the vault keeps and refuses

| Keeps | Refuses |
|---|---|
| The **demand for rigour**, read as the demand for certificates | Rigour as the claim to *final* foundations |
| **$\varepsilon$–$\delta$** read as a *modulus*: the vault's "continuity with a modulus" is Weierstrass's $\delta(\varepsilon)$ with the function named and costed ([[Intermediate Value Theorem]]) | The completed ℝ as the set of all cuts |
| **Rules that yield digits**, labelled as convergence certificates (not exhibits); finite exact certificates for algebraic numbers | Existence by *free creation*, "we create" |
| **Impossibility proofs** (Abel, Galois, Wantzel, Lindemann) | "No *ignorabimus*" |
| **Group theory and fields** | The claim that this makes mathematics autonomous |
| **Cantor's diagonal** as a procedural negative ([[Diagonal Argument]]) | The ontology of a hierarchy of completed infinities |
| **Non-Euclidean models** as relative consistency, and the lesson that geometry is not a priori | The conclusion that mathematics has no truth |

[AI] Note that the vault is **closer to Weierstrass than to Dedekind**: it keeps the $\varepsilon$–$\delta$ certificate and drops the completed totality that the same century added.

## Teaching [AI]

1. **This is where the standard curriculum starts**: limits and $\varepsilon$–$\delta$ come first in the usual calculus ([[Historical Order]], departure 2). Teaching it as a *later repair*, with its history, shows why it exists.
2. **Cauchy's mistake and the counterexample $x^n$** as a lesson in what a proof needs.
3. **Weierstrass's function** by a finite sum and its difference quotients.
4. **A triangle on a ball** (a three-right-angle triangle drawn on an orange).
5. **Quaternions**: multiply $i$, $j$, $k$ and see that order matters, to link with the symmetries of the square ([[Groups]]).
6. **A cut by rule** for $\sqrt2$ and the map $q\mapsto\tfrac{2q+2}{q+2}$.
7. **Read the quotations above in context**, as primary sources on the posture of the age.

## Hard problems

1. **How fairly to describe the people.** The devout founders (Cauchy, Riemann, Boole, Cantor) complicate "the pinnacle of hubris"; the page locates the hubris in the programme and its rhetoric.
2. **The quotations** (Jacobi, Dedekind, Cantor, Hilbert, Kronecker) are recollections and the wording matters; each must be checked against the source and the translation.
3. **Kline's account** is one narrative; later historians (Grabiner, Gray, Ferreirós) refine it. The vault uses Kline as Murphy does and should check the details.
4. **Whether the collapse is a collapse.** Mathematicians mostly continued as before; Kline's "loss of certainty" is a loss of a *philosophical claim*, not of results.
5. **The Huxley parallel** is an interpretation joining two stories that historians treat separately.
