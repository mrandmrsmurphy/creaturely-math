---
title: Mathematics 500 to 1500
type: history
status: "canonical (draft; a grab-bag by design; every date and attribution is from recollection and to be checked)"
provenance: "murphy (the frame: Boethius through 1500; Chinese, Indian, Persian, Arabic, Roman and early European perpetuation and advancement; the one seismic shift, algebra slowly replacing geometry; the Romans building an enormous civilization without advancing mathematics; proof-based mathematics as an intellectual curiosity and applied mathematics as the greater; today's pure-mathematics bias) + ai-synthesis (the timeline, the shift in stages, the worked examples, the counterpoints, the flagged problems)"
sources: "[[Greek Mathematics]], [[Babylonian Mathematics]], [[Historical Order]], [[Sexagesimal]], [[Nested Radicals]], [[Chinese Remainder Theorem]], [[Quadriga for Mathematics]], [[Corrective Narrative]]"
updated: 2026-10-10
---

# Mathematics 500 to 1500

The fourth stage of [[Historical Order]], after [[Greek Mathematics]] (about 600 BCE to 500 CE). Murphy's frame is deliberately a **grab-bag**: from **Boethius** (c. 480–524) to **1500**, with Chinese, Indian, Persian, Arabic, Roman and early European mathematicians perpetuating and advancing the earlier ideas. There is no single centre; the work moved between civilizations and across languages. All dates and attributions are approximate recollections **to be checked**.

## The one seismic shift: algebra slowly replaces geometry (Murphy)

The central change of the period is not a theorem but a **change of language**: algebra, a way of working with unknown quantities by rules, slowly takes over the work that geometry had done. It takes about eight centuries, in stages [AI]:

| Stage | When | What changes | Geometry's role |
|---|---|---|---|
| **Diophantus** | c. 250 | abbreviations for the unknown and its powers; rational solutions | none (pure arithmetic) |
| **al-Khwarizmi** | c. 820 | *al-jabr*: solving equations by named operations; six standard forms | **justifies** each step by cutting squares and rectangles |
| **al-Karaji** | c. 1000 | an algebra of polynomials with its own rules (powers, products, quotients, the binomial pattern) | no longer needed for the *rules* |
| **Omar Khayyam** | c. 1070 | classifies and solves cubics | **solves** them geometrically, by intersecting conics |
| **Fibonacci, the abbacists** | 1202 and after | algebra in the service of trade | little |
| **Cardano and Bombelli** | 1545, 1572 | formulas for the cubic and quartic | still **justified** by cutting cubes |
| **Viète** | 1591 | letters for known and unknown quantities | the symbols themselves are the proof's medium |
| **Descartes** | 1637 | geometry *translated into* algebra (coordinates) | **now written in** algebra |

The last two rows are past 1500, and they close the story: geometry, the older queen, becomes a subject in the new language. This is the stretch that [[Historical Order]] counts as the step "letters arrive late."

**A worked example of the middle of it** (checked). Al-Khwarizmi's standard problem: *a square and ten roots equal thirty-nine*, $x^2+10x=39$. The geometric recipe: take a square on $x$ and two rectangles of sides $x$ and $5$; add a corner square $5\times5=25$ to complete a larger square. Then $39+25=64$, the large square has side $8$, and $x=8-5=3$. Check: $9+30=39$. Three equal things happen at once: a **rule** ("halve the roots, square, add, root, subtract"), a **picture** (the completed square), and a **notation** (here written with letters only after the fact). It is the Babylonian problem of [[Historical Order]] given a name and a proof.

**And the cubic** (checked). Cardano's formula for $x^3+px=q$ gives, for $x^3+6x=20$,
$$x=\sqrt[3]{10+\sqrt{108}}-\sqrt[3]{\sqrt{108}-10}\approx2.7321-0.7321=2.$$
The nested radicals **denest exactly**: $10+\sqrt{108}=10+6\sqrt3=(1+\sqrt3)^3$ and $\sqrt{108}-10=(\sqrt3-1)^3$ (both verified in $\mathbb Q(\sqrt3)$), so $x=(1+\sqrt3)-(\sqrt3-1)=2$ exactly. This is the kind of simplification of [[Nested Radicals]].

**What it means for the vault** [AI]. The shift is real and it is the origin of the standard order of teaching. The vault's own programme *partly reverses* it: [[Constructible Trigonometry]] returns geometry to the centre with exact surds, and [[Discrete Calculus]] works from the picture of a growing rectangle. Neither refuses algebra; both keep the figure.

## Place value, the zero, and the road west (Murphy: it belongs here)

The most consequential change of the period for ordinary people is **written place-value notation with a zero**, not any theorem.

- **Before:** place value existed in **Babylon** (base 60, with a gap and later a placeholder; [[Sexagesimal]]) and in the **Chinese counting rods**, a decimal positional system with an empty place for zero, used on the counting board. *But* the **written** Chinese numerals (for example 三百二十一, "three hundred two ten one") stayed *multiplicative-additive*, not positional; a written circle for zero appears only late (about the 13th century; possibly influenced by India; to check). Murphy's point: **the Chinese never adopted the Hindu-Arabic written place-value numerals** in their own tradition; that adoption came only in recent centuries. The refinement is that they *computed* positionally on the rods.
- **India:** a decimal place-value numeral with a **zero as a number** (Brahmagupta, 628: rules for adding, subtracting and multiplying with zero), with earlier uses of a dot or circle as placeholder (the Bakhshali manuscript, dated by recent work to roughly the 3rd to 4th century CE; the dating is disputed; to check).
- **The Arabic-language world:** al-Khwarizmi's book on the Hindu numerals (c. 825) carried the system west; its Latin translation gave us *algorithm* (his name). The Arabic *sifr* ("empty") became *cipher* and *zero*.
- **Europe:** Gerbert's abacus (c. 1000), then **Fibonacci's *Liber abaci*** (1202) taught the nine Indian figures and the sign $0$ to merchants. The **abacists** (calculating on a counting board with counters) and the **algorists** (writing figures) competed for generations; city rules restricted the new numerals in bankers' accounts (Florence, 1299; recollection, to check), partly from fear that $0$ could be altered into $6$ or $9$. The standard Roman numerals lingered in accounts and inscriptions.
- **Decimal fractions** came last: al-Kashi (c. 1424), then Stevin's *De Thiende* (1585), in the next stage ([[The Road to Calculus]]).

**What it did** [AI]: it made the algorithms of arithmetic mechanical, which turned calculation from an expert craft into a school subject; it carried the Babylonian idea, with a full zero, to the whole world; and it set up the logarithm tables and the calculus. The vault treats the numeral as a **compression** of the tally ([[Tally Marks]]) and as a notation, not a number ([[Creational Ultrafinitism]]).

## Regions

### Rome and the Latin West

- **Rome.** Roman mathematics was practical: surveying (the *agrimensores* and the *groma*), engineering and architecture (Vitruvius, Frontinus on aqueducts), the calendar (the Julian reform of 46 BCE, planned by the Alexandrian Sosigenes), law and accounting. Fractions were reckoned in **twelfths** (the *as* divided into twelve *unciae*, whence *ounce* and *inch*), a base with six divisors, as the Babylonians chose a base with twelve ([[Sexagesimal]]). Roman numerals are poor for calculation; the abacus did the work.
- **Cicero's remark** (*Tusculan Disputations* I; recollection, to check) is the classic statement of the Roman attitude: among the Greeks nothing was more honoured than geometry, whereas *we* have limited the art to the usefulness of measuring and calculating.
- **Boethius** (c. 480–524), *De institutione arithmetica* and *De musica*, passed Nicomachus's number tradition to the Latin world and gave the name **quadrivium** (arithmetic, geometry, music, astronomy). Cassiodorus and Isidore of Seville (c. 560, c. 600) transmitted the encyclopaedic tradition.
- **Bede** (c. 673–735), *De temporum ratione*: the reckoning of **Easter** (the *computus*), with a chapter on counting on the fingers. See below.
- **Alcuin** (c. 800), a collection of recreational problems; **Gerbert of Aurillac** (c. 940–1003, later Pope Sylvester II), the abacus and early use of Hindu-Arabic numerals.
- **The translation movement** (12th century: Toledo, Sicily; Adelard of Bath, Gerard of Cremona) brought Euclid, the *Almagest* and al-Khwarizmi from Arabic into Latin.
- **Fibonacci** (Leonardo of Pisa, c. 1170–1250), *Liber abaci* (1202): the Hindu-Arabic numerals taught for merchants, with commercial problems and a rabbit problem; *Liber quadratorum* (1225) on squares.
- **Universities and the calculators** (13th–14th centuries): the Oxford Merton school (Bradwardine, Heytesbury, Swineshead) on motion and **mean speed**; **Oresme** (c. 1320–1382) on graphing qualities (an early coordinate picture) and the divergence of the **harmonic series** (the grouping $\tfrac13+\tfrac14>\tfrac12$, $\tfrac15+\dots+\tfrac18>\tfrac12$, the very proof in the [[Discrete Calculus]] draft). Bradwardine became Archbishop of Canterbury and Oresme a bishop: **churchmen did mathematics**.
- **Nicholas of Cusa** (1401–1464), *De docta ignorantia* (*On Learned Ignorance*): a polygon inscribed in a circle never *becomes* the circle however many sides it has; the finite intellect cannot attain the infinite truth, so "learned ignorance" is the right posture. This is theology doing mathematics, and it is close to [[Creational Ultrafinitism]]'s point (below).
- **Regiomontanus** (1436–1476), *De triangulis omnibus*: trigonometry as a subject on its own, separate from astronomy; **Pacioli** (1445–1517), *Summa* (1494): arithmetic, algebra and **double-entry bookkeeping**; Chuquet (1484) and Widmann (1489) on exponents, negative numbers and the signs $+$ and $-$.

### India

- **Aryabhata** (born 476), *Aryabhatiya* (499); **Brahmagupta** (598–c. 670), *Brahmasphutasiddhanta* (628): the rules for **zero** and **negative numbers** (debts and fortunes); the "Brahmagupta–Fibonacci" identity below; methods for equations such as $x^2-Dy^2=1$.
- **Bhaskara II** (1114–c. 1185), *Lilavati* and *Bijaganita*: arithmetic and algebra for practical problems; the cyclic method for $x^2-Dy^2=1$.
- **Madhava of Sangamagrama** (c. 1340–1425) and the **Kerala school**: infinite series for the sine, cosine and arctangent, with **correction terms** that speed convergence (recollection). A series *with an error term* is the vault's Level 10 done honestly ([[Number Hierarchy]]).
- The **place-value decimal numeral with a zero** (see above), which travelled to the Arab world and Europe.

### China

- **The Nine Chapters on the Mathematical Art** (*Jiuzhang suanshu*, compiled c. 100 BCE–100 CE): a manual for officials (fields, grain, taxes, canals, wages) with an algorithm for **digit-by-digit root extraction**, which gives the vault's Level 7 ([[Number Hierarchy]], the "Jiǔ Zhāng" numbers). Counting **rods** gave a decimal place-value system on the counting board early (the written numerals stayed non-positional; see above).
- **Liu Hui** (3rd century), a commentary; π from a polygon doubled to 192 sides (about 3.1416); **Zu Chongzhi** (429–500), $\tfrac{355}{113}$, correct to $2.7\times10^{-7}$ (checked: $3.1415929$).
- **Sunzi Suanjing** (c. 3rd–5th century): the remainder problem of [[Chinese Remainder Theorem]]; **Qin Jiushao** (1247), a general method for simultaneous congruences and a Horner-type method for polynomial roots; **Yang Hui** (1261) and **Zhu Shijie** (1303, the *Precious Mirror of the Four Elements*) on the arithmetic triangle and equations in several unknowns.

### Persia and the Arabic-language world

- **Al-Khwarizmi** (c. 780–850), the book on Hindu numerals (*algoritmi*, whence *algorithm*) and the *Compendious Book on Calculation by Completion and Balancing* (*al-jabr*, whence *algebra*). Its examples include **inheritance** and **trade**.
- **Thabit ibn Qurra** (836–901), amicable numbers; **al-Karaji** (c. 953–1029), the algebra of polynomials and the binomial pattern; **Ibn al-Haytham** (c. 965–1040), sums of powers and optics; **al-Biruni** (973–1048), trigonometry and astronomy.
- **Omar Khayyam** (1048–1131), cubics by conics, a critique of Euclid's parallel postulate; **Nasir al-Din al-Tusi** (1201–1274), the Maragha observatory and trigonometry as a field; **al-Kashi** (c. 1380–1429), decimal fractions and a value of $\pi$ to sixteen places.
- **Practical drivers:** the law of **inheritance**, the **prayer times and direction of Mecca** (spherical astronomy), the calendar, trade, and the astronomical tables.

## Easter: the Church's modular arithmetic [AI, checked]

The computus is a problem in **clock math** ([[Modular Arithmetic]]). Easter depends on the **19-year** cycle of the moon and the **7-day** week and, in the Julian calendar, the **28-year** cycle of the solar calendar; since $19$ and $28$ are coprime, the whole pattern repeats every $19\times28=532$ years (the Dionysian Easter cycle; checked by the Chinese remainder theorem). Today's arithmetic: using the standard Gregorian algorithm (Gauss and later authors), Easter falls on **March 31, 2024**, **April 20, 2025**, **April 5, 2026** and **March 28, 2027** (all computed). A middle-school class can compute the date with remainders, which is why the topic belongs in the sequence ([[Historical Order]]).

## The Brahmagupta–Fibonacci identity and the circle [AI, checked]

$$(a^2+b^2)(c^2+d^2)=(ac-bd)^2+(ad+bc)^2.$$
For $(a,b)=(3,4)$ and $(c,d)=(5,12)$ both sides are $4225=65^2$ ($25\cdot169$). It says that the product of two sums of two squares is again one, which is **complex multiplication**, and so the law of the circle of [[Discrete Calculus]] and [[Sum of Slopes]] ($\oplus$) at the level of whole numbers: multiplying Pythagorean triples. It was in Brahmagupta (628) and Fibonacci (1225) long before it had a name.

## Fibonacci numbers and the golden ratio [AI, checked]

The rabbit problem gives $1,1,2,3,5,8,13,21,34,55,89,144,233,377$. The exact formula needs $\sqrt5$: in $\mathbb Q(\sqrt5)$, $\varphi=\tfrac{1+\sqrt5}2$ and $\psi=\tfrac{1-\sqrt5}2$ give $\varphi^{12}-\psi^{12}=144\sqrt5$, hence $F_{12}=144$. A whole number is the difference of two surds, held *exactly*, which is the method of [[Exact Until Output]].

## Weight: applied against pure (Murphy) [AI]

Murphy's observation: the Romans built an enormous civilization without advancing mathematics much, and proof-based mathematics is an **intellectual curiosity**; *if their view is given any weight, then applied mathematics is the greater*; today's **pure-mathematics bias stands out**.

**The pattern is general and supports him.** Across the civilizations of this chapter the driving problems are practical:

| Civilization | Chief practical drivers |
|---|---|
| Rome | surveying, engineering, the calendar, law, commerce |
| India | astronomy and the calendar, trade |
| China | administration: fields, grain, taxes, canals; the calendar |
| Islamic world | inheritance law, prayer times and the direction of Mecca, trade, astronomy |
| Latin Christendom | the Church's calendar (computus), merchants and bookkeeping, the quadrivium in the schools |

The Greek proof-first tradition ([[Greek Mathematics]]) is the **exception**, and in the vault's reading it already shared its world with Babylonian computation and Hellenistic engineering.

**Four counterpoints, stated fairly:**

1. **The Romans borrowed.** Vitruvius cites Archimedes; Roman engineers used Greek applied mathematics. They did not *extend* mathematics, but they *used* an inheritance, much of it built by the pure tradition.
2. **Curiosities pay off.** The Greek study of conic sections (Apollonius) became the mathematics of planetary orbits (Kepler, Newton) after some 1,800 years. Theory and practice feed each other, and no one can say in advance which curiosity will matter.
3. **The pure/applied split is modern.** Archimedes, Ptolemy, Brahmagupta, al-Khwarizmi, Newton, Euler and Gauss worked on both. The sharp division is of the 19th and 20th centuries (Hardy's *A Mathematician's Apology*, 1940, celebrates *uselessness*; recollection). So "today's bias" is a recent professional feature, and not the Greek one.
4. **Weight is a judgement of value, not of history.** Showing that most civilizations *did* applied mathematics does not by itself show that it *ought to* count for more. The vault's reason is theological and pedagogical: **Praxis is a glory** and the *tekton* is honoured ([[Quadriga for Mathematics]]), mathematics serves the neighbour, and proof (*Apodeixis*) is a rest at the end of work, not the whole of it.

**A position that fits** [AI]: the vault does not reject proof (it is a certificate, [[Certificates]]); it **refuses to rank proof above practice**, and counts the engineering mathematics of Babylon, Rome, India, China and the Islamic world as mathematics in full.

## Cusa and the vault [AI]

Nicholas of Cusa's circle and polygon is a clean medieval statement of *potential* against *actual* infinity: the perimeter of the inscribed $n$-gon, $n\sin\tfrac\pi n$, **approaches** $\pi$ but never equals it ($6\to3.0000$, $12\to3.1058$, $96\to3.14103$, $1000\to3.14159$; computed) while the circle is the *limit that is not reached*. His conclusion is epistemic humility before the infinite God, which is the posture of [[Christians and the Reals]] and [[Creational Ultrafinitism]]. He is worth reading as a **theologian-mathematician of the right temper**.

## For teaching [AI]

1. **Place value** and the zero, with the story of their travel and the resistance to them (the abacists against the algorists; recollection); the Chinese rods beside the written numerals.
2. **Al-Khwarizmi's completing the square** done with cut paper (Praxis), then written with letters.
3. **Easter** as a modular arithmetic project.
4. **Fibonacci's merchant problems** and the rabbit problem.
5. **Chinese remainder problems** from Sunzi, and rod numerals.
6. **Roman fractions in twelfths**, to see why $12$ and $60$ are good bases.
7. **Liu Hui's polygon** for π, with the check by $n\sin\tfrac\pi n$.

## Hard problems

1. **The weight of the claim.** That applied mathematics is "greater" is a value judgement; the page records the history and the vault's reasons and lets the claim stand as Murphy's.
2. **Attribution and dating.** Most dates are approximate, and the transmission paths (India to the Arab world to Europe; China's independent line) are debated.
3. **Whether the shift from geometry to algebra is a gain without a loss.** The vault's programme argues that something was lost (the picture) and partly restores it.
4. **A grab-bag has no thesis.** This page is a map; the argument is the shift and the weighting.
