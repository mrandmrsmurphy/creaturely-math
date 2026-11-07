---
title: Mathematics 1900 to Today
type: history
status: "canonical (draft; dated 2026-10-10; the 2026 events are from web sources read or searched that day, the rest from recollection, all to be checked)"
provenance: "murphy (the thesis: mathematics is singularly broken; the frontier is far from what a doctorate reaches; silos; errata; AI and Lean unmasking weak work; the schools of foundations debated and ignored; the New Math replacing counting with set theory; the human-endeavor response, a secular version of Francis Su; Godel and Cohen on the continuum hypothesis against the positivists) + ai-synthesis (the structure, the sourcing and its limits, the qualifications, the flagged points)"
sources: "[[Mathematics 1730 to 1900]], [[Five Acts]], [[Infinity and Cantor]], [[Christians and the Reals]], [[Certificates]], [[Historical Order]], [[Quadriga for Mathematics]], [[Number Hierarchy]]"
updated: 2026-10-10
---

# Mathematics 1900 to Today

The seventh and last stage of [[Historical Order]]. In the vocabulary of [[Five Acts]] (postures, not periods) this stage shows **unmasking** (the exposure of the foundations) and **repression** (carry on and ask nothing), and, with the news of 2026, the possible beginning of **chastened doxology**. Murphy's frame: *mathematics is singularly broken today*, and the cause is a foundation whose cracks were seen at the start of the century and then ignored.

**A note on sources.** The 2026 material below (AI, Lean, Tao's statements) comes from web pages found or read on **10 October 2026**, which postdate my own knowledge; I mark what I read myself, what I only saw in search summaries, and what is Murphy's report. Everything earlier is from recollection and **to be checked**.

## 1. The state of the field (Murphy)

Murphy's observation, "not original to me":

- **Distance from the frontier.** In most sciences the doctorate ends at the frontier; in mathematics a student would be lucky to reach "the 1960s mark" in what was *taught*. [AI] A qualification: a doctoral thesis in mathematics usually *does* contain a new result, so the claim is about the **breadth** of what a student has been taught, not about the thesis. It is also unverified here as a measured fact.
- **Silos.** Each subfield makes its own definitions: "some new definition of a number over here or some new notation over there", so no one can know the whole field. (The last mathematicians who covered it are usually said to be Poincaré, d. 1912, Hilbert and Weyl; recollection. The classification scheme of the *Mathematical Reviews* has some sixty top-level classes, to check.) This is the problem of [[Number Hierarchy]] at the scale of a profession: **one word, "number", for many different things**, and no sorting.
- **Errata.** A recent doctor reported to Murphy that one inherits "an enormous pile of errata" on entering a field. [AI] A documented case: **Voevodsky** described errors in his own published work, including a 1989 claim shown wrong by Simpson in 1998, as a motive for formal verification (his 2014 IAS talk; recollection and search, to check).

## 2. Proof assistants, Lean, and AI (2026)

**What Lean does.** Lean is a *proof assistant*: a proof is written as a finite object that a small program, the **kernel**, checks. [AI] That is **the certificate rule of [[Certificates]] in its purest form**: a proof is an *exhibited finite object* checked by a procedure, not a claim made on trust. It descends from the type-theoretic tradition (the Curry–Howard idea that proofs are programs), which came from the constructive schools of the 1960s and 1970s (Bishop's *Constructive Analysis*, 1967; Martin-Löf's type theory), the very schools the programme of 1900 to 1930 had set aside. (Lean's main library, *mathlib*, nevertheless assumes classical logic and the axiom of choice, and many definitions of real-number operations are marked *noncomputable*; recollection.)

**What formalization has found.**

- Major results were **confirmed**: Gonthier's Four Colour Theorem (2005) and Feit–Thompson (2012) in Coq; Hales's Kepler conjecture (Flyspeck, 2014); the **Liquid Tensor Experiment**, Scholze's challenge of December 2020, completed in Lean in 2022, which also simplified the mathematics (its dependence on certain homotopy groups of spheres was removed, per a search summary; the project's early announcement, June 2021, covered a key theorem and not yet the whole).
- **Small errors and misstatements** are found often. Tao has found small mistakes in published proofs while formalizing his own papers; a 2025 Lean formalization is reported to have flagged an error in a 2006 physics paper (the two-Higgs-doublet potential); and formalizing the Erdős problems exposed many **misformalizations**, statements that did not say what was meant (all from a search summary; to check).

**Murphy's clarification of the claim:** not that Lean has overturned anything major, but that **it is hard to get everything into Lean, because the field is poorly documented and understood in places**: results rest on folklore, unwritten steps and arguments few people have read in full. That is a claim about the *state of the literature*, and the best inside witness is below. (Separately, formalization finds **widespread small gaps and misstatements**; I did not find a case where Lean overturned a *major* accepted theorem.)

### The state of the literature, from inside (Kevin Buzzard)

I read **Buzzard's slides "The future of mathematics?"** (Microsoft Research, 5 September 2019). He is a number theorist at Imperial College London who leads the project to formalize a proof of Fermat's Last Theorem (his March 2026 talk for the London Institute for Mathematical Sciences, "AI and the formalisation of mathematics", is announced; I did not see it). In his own words:

- "**Nervousness about the state of the mathematical literature** was one reason I started to experiment with computer theorem provers."
- "And now I never want to go back to pen and paper mathematics – **I am beginning to mistrust it.**"
- "I believe that **no human, alive or dead, knows all the details of the proof of Fermat's Last Theorem**. But the community accept the proof nonetheless, because the proof is modular."
- "Our community even accepts proofs if the author says '**There are now 100 missing pages, which we will get to later on.**'" And: "The elders have decreed that the proof is OK."
- Of the odd order theorem: it was accepted in 1970, which is why Thompson received a Fields Medal; "We don't care that it got formalised – it was already 'checked'."
- On the future: "I now clearly understand that software such as Lean is part of the inevitable future of mathematics"; "tools such as Lean will begin to do research semi-autonomously, perhaps uncover problems in the literature. **Maybe these tools will replace research mathematicians**"; and a Google engineer (Szegedy) "believes that computers will be beating humans at math within ten years" (said to him in April 2019).

[AI] **This is the clearest support for Murphy's claim from inside the field.** Acceptance in mathematics is **social** ("the elders have decreed"), and a proof is accepted though *no one* knows all of it. That is exactly the situation the vault's certificate rule addresses: a claim whose warrant is the **trust of a community** and not an exhibited finite object ([[Certificates]]). A qualification: Buzzard is describing the sociology of acceptance, not saying the results are false; he also says elsewhere that his frustration with Lean itself was *documentation of Lean*, a different matter.

**The limits of Lean (read in full: Thomas Hales, a guest post on Tao's blog, 9 October 2026).** Hales's points, as I read them:

- A Lean proof should be believed **only once the kernel has checked it**, and **a human must audit that the formal statement means what was intended**: "a proof in Lean should not be accepted until a human audit is performed to ensure statement fidelity."
- **Soundness bugs** (a proof of *False* gets through) surfaced in summer 2026; one "led to an illicit disproof of the Collatz conjecture". Hales says they were found by **AI tools** used by security researchers and have been fixed. Different kernels can share defects.
- As of October 2026 there is **no complete public consistency proof for Lean's type theory**; Gödel's second theorem limits what a kernel can prove about itself, so "the most we might hope for is a relative consistency proof". He warns that "we absolutely cannot put blind trust in systems such as Lean", and that foundational work delegated to AI is "dangerous unless carefully audited by humans."

[AI] **Reading for the vault.** A checkable certificate is a real gain, and the **checker cannot certify itself**: that is Gödel's sword of [[Five Acts]] (the *unmasking* posture) applied to the machine. The verifier is a finite object we have to *trust or audit*, and the statement it checks has to be *read* by a person. Certificates are not abolished by this; they **need a community of checkers**, which is the "I am not trustworthy alone" of [[Quadriga for Mathematics]].

**AI and the field.** From web sources (not all opened): a Scientific American piece titled "AI has finally come for math—mathematicians might never recover"; Tao's July 2026 lecture to the International Congress of Mathematicians, "Mathematics in the Age of AI" (an essay version is on arXiv, 2608.16753), which treats AI capability as given and asks what the **goals and values** of mathematical research are; and a series of posts on his blog in September and October 2026. A search summary says Tao reported AI systems improving flagship bounds (bounded gaps between primes) by September 2026; I did not confirm that.

**The OpenAI release (6 October 2026)** is the event behind Murphy's "decimating the field in the last few weeks." From the sources found: OpenAI released a public **repository of 700-plus manuscripts** (722 manuscripts in 372 related result families, per OpenAI's developer post as reported; counts vary by source) presenting proofs, solutions and progress on open problems, some touching famous ones; **not all were certified in Lean**, OpenAI says it is sharing formalizations of many, and **some manuscripts have already been retracted** after outside readers found mistakes (Scientific American, as reported); the **model has not been released**, so outsiders cannot replicate it. I could not read the Nature or Scientific American articles in full. I read the response of the **Association for Human Mathematics**, posted on Tao's blog on 7 October (Tao is not the author): it objects that the work was not requested, shows "total disregard for the norms of scientific research", that releasing so many files at once is "a demonstration of power" and not scholarship, and asks mathematicians to "discontinue their work with OpenAI". Reactions are **mixed**: some call the results jaw-dropping, a number theorist quoted says he will not read them, and others say they need independent replication.

**Murphy's point**: *if mathematics is just about writing proofs, machines are now poised to outstrip humans in every measurable way.* [AI] The vault already says mathematics is **not** just proof: the Quadriga names four arts, **Quaestio** (is this a mathematical question at all?), **Noesis** (insight), **Praxis** (the doing) and **Apodeixis** (proof), and its line "math ≠ computation" ([[Quadriga for Mathematics]]) is the same move as "math ≠ proof-production". If a machine can supply Apodeixis, the claim to be made is that the human work lies elsewhere and that the **reason to do mathematics was never the output**. That is exactly where the secular "human endeavor" line needs the ground below. Note also the **audit problem** the release exposes: a manuscript no human has read, with a Lean file whose *statement* a human must still check (Hales).

**"Mathematics is a human endeavor."** Here a correction of attribution. I read Tao's 3 October 2026 post: it is a **guest post by Jennifer Taback** (Bowdoin College), and the words are hers: "Mathematics is a human endeavor." She argues that machine output needs substantial human work before it adds to knowledge, that exposition matters as much as discovery, that the field must decide "what counts as proof, and what we value for publication and tenure," and that she does "not want to surrender my questions." Tao's own stance, from the search summaries, is that the question to ask is of **values and purposes** and not just of capability. So the "human endeavor" line is shared by several mathematicians, with Tao leading the discussion.

**A secular version of Francis Su** (Murphy). Su's *Mathematics for Human Flourishing* (Yale, 2020; recollection) argues that mathematics serves human **flourishing** (play, beauty, truth, justice, love), not only results. [AI] The vault can say what the secular version lacks: a **ground**. If mathematics is merely something humans invent, a machine that produces the same theorems has displaced the reason to do it. If it is **a created order that creatures are given to receive and investigate**, with the doing itself a work of love of neighbour and of worship ([[Creaturely Realism]]; [[Quadriga for Mathematics]]: *Praxis* is a glory), then the human act of understanding has its own worth whatever machine output exists, as walking a mountain has its own worth beside a helicopter. That gives "human endeavor" a reason beyond preference. (A proposal, not a settled argument.)

## 3. The foundations: the answer that was ignored

The debate over what mathematics is rested on three schools: **logicism** (Frege, Russell and Whitehead's *Principia Mathematica*, 1910–1913), **formalism** (Hilbert), and **intuitionism** (Brouwer, 1912 and after; Weyl joined briefly in 1921). It ran through the 1920s, with Hilbert removing Brouwer from the board of *Mathematische Annalen* in 1928 (recollection). **Gödel** (1931) answered it: the programme of *Principia Mathematica* and of Hilbert, a complete and provably consistent formal system for arithmetic, **cannot be carried out**. The title of the paper names *Principia Mathematica*.

[AI] What followed, in Murphy's reading, was the posture of **repression** ([[Five Acts]]). Mathematicians mostly agreed to proceed as if the question were settled, with **ZFC** as the working foundation (assumed, and not examined), and **Bourbaki** (from 1935) wrote the structural, set-based style. A remark attributed to several mathematicians is that they are Platonists on weekdays and formalists on Sundays (recollection). The constructive and type-theoretic traditions *continued* beside this (Bishop 1967; Martin-Löf; the proof assistants), and it is their descendants that now check proofs.

### The continuum hypothesis

**Gödel** (1938–1940) showed that the continuum hypothesis (CH) **cannot be disproved** from the standard axioms (ZFC, if consistent); **Cohen** (1963, by forcing) showed it **cannot be proved**. CH is **independent**. [AI] Precisely: it was not "defeated" (shown false) but **shown undecidable by the axioms**, which means that the axioms of set theory do **not** determine the answer to a natural question about the very objects they are about: *how many real numbers there are*. Consequences:

- It undercuts the **positivist** and logicist hope (the Vienna Circle; Russell and Whitehead) that mathematics is **analytic**, a matter of conventions and logical consequence that settles every question: the question here is meaningful and not settled by the conventions.
- **Gödel** himself drew the opposite lesson from the positivists: that mathematical reality exceeds the axioms, and he hoped new axioms would decide CH (he thought it false); recent set theory has two camps (a single true universe, with new axioms to find, and a **multiverse** of set-theoretic worlds; recollection: Woodin and Hamkins).
- For the vault ([[Infinity and Cantor]], [[Christians and the Reals]]): **the continuum is not a determinate completed object** that the axioms pin down. That is what a potential, creaturely continuum would predict.

On the **atheists who still parrot the positivists**: I read "ANW" as Whitehead (with Russell, the authors of *Principia*). The logicist project they led is the one Gödel's 1931 paper targets; that its central hope failed is a matter of record. Whether a given popular writer still repeats it I cannot check, and I do not rank the claim.

## 4. The New Math, and education

**The history** (recollection, to check): after Sputnik (1957), the School Mathematics Study Group (SMSG, 1958, under Begle) and similar projects rewrote school mathematics around **sets, structure and the properties of operations**. At the Royaumont seminar (1959) Dieudonné is remembered for "*Euclid must go!*"; in 1962 sixty-five mathematicians, Kline among them, signed a letter criticising the reform; Tom Lehrer's "New Math" song dates from 1965. **Kline's** *Why Johnny Can't Add* (1973) is the standard critique: rigour and abstraction before understanding, and set theory as the foundation in place of number.

**Murphy's claims**, and what the evidence gives. Murphy cites **Johan Prytz and Martin Karlberg, "Nordic school mathematics revisited: on the introduction and functionality of New Math"** (*Nordic Studies in Mathematics Education* 21, no. 1, 2016, pp. 71–93). **I read the paper.** Its content, which is the opposite of a demonstration that the New Math lowered results:

- **What it tests:** "the claim that New Math material had negative effects on students' learning". Its own words: "**Our conclusion is that the claim is, in most parts, incorrect.**"
- **Data:** an intervention study run in Sweden while the reform was prepared (grades 1–9, reported in *Nordisk skolmatematik*, 1967), with national-test items in experimental and control classes. Their reading: there were teachers who "could use the experimental texts and achieve acceptable results"; experimental students did "really badly in about 25 percent of the items", which "is far from the New Math material being a failure." (A later paper, as reported in a search summary, adds that high achievers in grade 9 did better with the traditional curriculum; I did not find that in the parts I read.)
- **Other studies they cite:** Kristiansson (1979) found students on the old curriculum did significantly better in grades 3 and 6 in 1973, soon after launch, but Westin (1999) found **clear improvement** on the same items from 1973 to 1977, so they read "trails of success as well as failure."
- **What *did* fail, in their account:** **set theory as a common foundation**: "formulations about set theory disappeared from the national curriculum of 1980", replaced by problem solving. They add that new topics (algebra and geometry in earlier years, statistics and probability) stayed. They cite Kline's *Why Johnny Can't Add* as the source of the "negative effects per se" claim and take it as the claim to test. They also describe the New Math's **intent**: "a common foundation for school mathematics using elements from modern mathematics, for instance set theory", with the **Bourbaki group** as the role model.

| Claim | Evidence | Verdict |
|---|---|---|
| The New Math put set theory in place of the natural numbers as the foundation | Prytz and Karlberg: the aim was a common foundation from set theory, after Bourbaki; but the programme also brought other topics | **supported** as an account of the intent |
| The New Math **lowered student performance** | Prytz and Karlberg's data and conclusion: the negative-effects claim is "in most parts incorrect", results mixed; Kristiansson 1979 versus Westin 1999; US data: SAT math fell about 502 to 465 (1963 to 1980) but a College Board panel attributed most of the 1960s fall to who took the test; NAEP long-term math starts only in 1973; 13-year-olds rose about 21 points 1978 to 2012 | **not supported by the best source offered**; the effect remains unestablished |
| Set theory as the school foundation was **abandoned** | Prytz and Karlberg: it disappeared from the Swedish curriculum of 1980 | **supported** |
| "Pre-algebra" and "pre-calculus" were invented in the 1970s to remedy poor preparation | not checked | **to check**; also consistent with more students reaching college-preparatory mathematics |

[AI] So the page records the **foundational critique** (set theory is the wrong foundation for school mathematics) as Murphy's, with Kline, and as a **policy that was abandoned**; it records the claim that the New Math *damaged achievement* as **not established**, and the best study found points the other way (for Sweden, in the trials). The vault's own alternative stands without it: **counting first** ([[Tally Marks]]), **history before abstraction** ([[Historical Order]]), structure *instantiated* before it is named (the cardboard square).

**Kline's three offices (Murphy, from the 2020 essay).** In *Why the Professor Can't Teach* Kline names three offices a healthy university needs: the **researcher**, who pushes the frontier; the **disseminator** or networker, who understands and connects; and the **educator**, who hands the ideas on. After the war the researcher was made the *summum bonum*: PhD programs produce only researchers, disseminators are all but eradicated, educators quit for want of power — and the misalignment reaches the schools, where mathematics sits stuck at the grammar stage on "a death march to calculus". The companion charge in *The Loss of Certainty*: research divorced from its source in real-world problems, mathematics cleft into pure and applied, the pure side writing what no one else reads. The vault's answer at the school level is [[Curriculum Plan]].

## 5. Timeline, 1900 to today (approximate)

| Date | Event |
|---|---|
| 1900 | Hilbert's Paris problems ("no *ignorabimus*") |
| 1901–1902 | Russell's paradox |
| 1904; 1908 | Zermelo's well-ordering theorem (the axiom of choice) and axiomatization of set theory |
| 1910–1913 | Whitehead and Russell, *Principia Mathematica* |
| 1912; 1918; 1921 | Brouwer's intuitionism; Weyl, *Das Kontinuum*; Weyl's turn to Brouwer |
| 1925–1930 | Hilbert's "paradise" remark (1925); the Annalen dispute (1928); "we must know, we will know" (1930) |
| **1931** | **Gödel's incompleteness theorems** |
| 1935; 1936 | Bourbaki begins; Church and Turing; Gentzen's consistency proof for arithmetic |
| 1938–1940 | Gödel: CH is consistent with ZFC |
| 1957–1959 | Sputnik; SMSG; Royaumont |
| **1963** | **Cohen: CH is independent** |
| 1960–1966 | Robinson's non-standard analysis |
| 1967; 1970s | Bishop's *Constructive Analysis*; Martin-Löf's type theory |
| 1973 | Kline, *Why Johnny Can't Add*; NAEP long-term trend mathematics begins |
| 1976 | Appel and Haken's Four Colour Theorem, the first major computer-assisted proof, and a dispute over whether it counts |
| 1995 | Wiles's proof of Fermat's Last Theorem (a proof few can check end to end) |
| 2005; 2012; 2014 | Four Colour in Coq; Feit–Thompson in Coq; Flyspeck |
| 2013 | The Univalent Foundations (HoTT) book; Voevodsky's formal-verification turn |
| 2020–2022 | Liquid Tensor Experiment |
| 2025 | AI systems reach gold-medal level on the International Mathematical Olympiad (recollection) |
| **2026** | Tao's ICM lecture on mathematics in the age of AI (July); Lean soundness bugs (summer); Hales's and Taback's guest posts (October) |

## 6. Where the vault stands

| Symptom | Murphy's root | The vault's response |
|---|---|---|
| Silos, new "numbers" everywhere | no shared foundation after 1931; "number" unsorted | the sorting of [[Number Hierarchy]]; counting and exhibits as the common base |
| Errata, unreadable proofs | proofs no one can check | **certificates** with **checkers**, plus the community of checkers and the audit of statements |
| Education | set theory for number, abstraction first | counting first, history, instantiation ([[Historical Order]]) |
| Machine proofs | what remains for humans | the human act of *reception*, *Praxis*, and its theological ground |
| Foundations | answered and ignored | take the answer seriously: creaturely access, potential infinity, certificates ([[Creational Ultrafinitism]]) |

**The shape of chastened doxology** [AI]: not a return to the naive first posture, but *the garden become a city*: the machine certificates, the formalization, the exhibits, held **without the claim to autonomy**. If 2026 is a hinge, it is because the tools of the constructive tradition have become the working tools, while the **ground** of why anyone does mathematics is being asked, openly, by the leaders of the field.

## Teaching [AI]

1. **Why a proof assistant is a certificate checker**: write a short proof in Lean or a similar tool, and see the kernel accept or reject it.
2. **Statement fidelity**: have students read a formal statement and say what it means, as Hales requires of humans.
3. **The independence of CH** told as a story of what axioms can and cannot decide.
4. **History of the New Math**, with the data actually available, as an exercise in separating a story from evidence.
5. **A reading of Taback's and Tao's posts** on mathematics as a human endeavor.

## Hard problems

1. **The claim that mathematics is "singularly broken"** is Murphy's evaluation; the page records the symptoms and the sources and does not measure the field's health against others.
2. **AI.** The 2026 sources are web posts, partly from search summaries; the situation is changing weekly and every statement here dates from 10 October 2026.
3. **New Math causation** is unproven by the data found; the literature (SMSG-era evaluations; later studies) is not examined.
4. **Lean's relation to the vault**: its kernel is a certificate checker, but mathlib is classical and uses choice; whether the vault endorses it, wants a constructive fragment, or a checker for its own budget forms is open.
5. **Whether this is chastened doxology.** An interpretation, not a prediction.
