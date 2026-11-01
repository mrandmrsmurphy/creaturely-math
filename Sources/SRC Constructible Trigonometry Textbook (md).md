---
title: "Constructible Trigonometry Textbook (framework + 17-chapter outline)"
type: source
status: source
provenance: murphy (outline) + ai-assisted wording
date-written: "2026"
snapshot: 2026-10-07
---

> [!info] Source snapshot
> Core framework and full outline. Canonical summary: [[Constructible Trigonometry]].

## CORE FRAMEWORK (folded in from Constructible Trigonometry.md)

### Abstract

Traditional trigonometry often acts as a "black box" for students, requiring transcendental functions ($\sin, \cos, \tan$) and reliance on calculators to produce opaque decimal approximations. **Constructible Trigonometry** offers a purely algebraic framework designed for post-Algebra II learners. By defining geometric relationships through **Angle Slopes** and **Characteristic Lengths**, students can solve any triangle using only rational operations, radicals, and quadratics. This method returns trigonometry to the realm of exact values and geometric construction.

### Fundamental Definitions

In this system, we discard degree and radian measures in favor of two coordinate-based properties:

- **Angle Slope ($m$):** Defined as "rise over run," following the linear form $y = mx + b$. In any triangle $ABC$, the slope at vertex $A$ is denoted $m_A$.
- **Characteristic Length ($\ell$):** Defined as the scaling factor of the hypotenuse relative to a unit "run." It is calculated as:    $$\ell_x = \pm\sqrt{1 + m_x^2}$$    with $+$ for a rightward direction and $-$ for a leftward one (so $\ell<0$ for an obtuse angle).

**The Addition Law**

![[AngleAdditionDiagramSlope.svg|380]]
Using the construction provided, we can derive the slope of a composite angle $(\alpha + \beta)$ without transcendental tables. The relationship is established as:

$$m_{A+B} = \frac{m_A + m_B}{1 - m_A m_B}$$

### The Core Laws of Triangles

This framework replaces the classical Law of Sines and Law of Cosines with algebraic identities that rely solely on the relationship between side lengths ($a, b, c$) and vertex properties ($m, \ell$).

**The Law of Slopes**

For any triangle, the slopes of the three vertices are constrained by the following identities:

- $m_{A+B+C} = 0$
- $m_A + m_B + m_C = m_A m_B m_C$

In other words, any slope is the opposite of the slope of the sum of the other two: $m_C = -m_{A+B}$.

**The Law of Lengths**

The distance between vertices can be determined using the characteristic length of the opposite angle. This is the "Constructible" equivalent of the Law of Cosines:

$$c^2 = a^2 + b^2 - \frac{2ab}{\ell_C}$$

This formula can be rearranged to solve for any side or any characteristic length $\ell$.

**The Law of SAS Area ($Q$)**

The area of a triangle, $Q$, is defined by the ratio of the vertex slope to its characteristic length:

$$Q = \frac{1}{2} ab \frac{m_C}{\ell_C}$$

**The Circumdiameter Relation**

The relationship between a side and its opposite vertex properties is constant for all three sides of a triangle, equaling the circumdiameter ($2R$):

$$a \cdot \frac{\ell_A}{m_A} = b \cdot \frac{\ell_B}{m_B} = c \cdot \frac{\ell_C}{m_C}$$

### Comprehensive Triangle Solutions

The following table provides the exact algebraic formulas for solving triangles based on given parameters.

|**Case**|**Sides**|**Angles (Slopes/Lengths)**|**Area (Q)**|
|---|---|---|---|
|**SSS**|Given $a, b, c$|$\ell_C = \frac{2ab}{a^2 + b^2 - c^2}$|$Q = \sqrt{s(s-a)(s-b)(s-c)}$|
|**SAS**|$c = \sqrt{a^2 + b^2 - \frac{2ab}{\ell_C}}$|$m_A = \frac{a m_C}{b \ell_C - a}$|$Q = \frac{1}{2} ab \frac{m_C}{\ell_C}$|
|**AAS**|$c = a \frac{m_C \ell_A}{m_A \ell_C}$|$m_B = \frac{m_A + m_C}{m_A m_C - 1}$|$Q = \frac{a^2 m_C}{2 m_A \ell_C^2}(m_A + m_C)$|
|**ASA**|$c = b \frac{m_C \ell_A}{m_A + m_C}$|$m_B = \frac{m_A + m_C}{m_A m_C - 1}$|$Q = \frac{b^2}{2} \cdot \frac{m_A m_C}{m_A + m_C}$|

### Derived Centers

The framework extends to the internal geometry of the triangle, including the **Inradius ($r$)** and **Circumradius ($R$)**.

**Circumradius ($R$)**

The radius of the circumscribed circle is derived from the side lengths and the area:

- **General:** $R = \frac{abc}{4Q}$
- **AAS/ASA specific:** $R = \frac{b}{2} \cdot \frac{\ell_A \ell_C}{m_A + m_C}$

**Inradius ($r$)**

The radius of the inscribed circle utilizes "half-slope" constructions ($m_{x/2}$):

- **SAS:** $r = \frac{1}{2} m_{C/2} (a + b - \sqrt{a^2 + b^2 - \frac{2ab}{\ell_C}})$
- **ASA:** $r = b \cdot \frac{m_{A/2} \, m_{C/2}}{m_{A/2} + m_{C/2}}$

### Conclusion (of the core framework)

Constructible Trigonometry empowers students to engage with geometry through the lens of coordinate algebra. By removing the need for calculators, it emphasizes the derivation of exact values and deepens the understanding of the relationship between linear slopes and spatial dimensions. This approach ensures that trigonometry is not a series of button-presses, but a logical extension of Algebra II principles.

---

## OUTLINE

### PART I: THE EXACT APPARATUS (Review and Foundations)

**Chapter 1: Rehearsing Exact Algebra**
- 1.1 The Constructible Field K
- 1.2 What "Unsolvable" Means
- 1.3 Number Systems: ℕ, ℤ, ℚ, K, and the formal extensions
- 1.4 Babylonian Base-60: why 1/2, 1/3, 1/4, 1/5, 1/6 "exist" but 1/7 doesn't
- 1.5 Repeating Decimals: four examples, conversion to fraction
- 1.6 Compass and Straightedge: what operations are possible; example of constructible number
- 1.7 The Equal Sign: three kinds (running discussion introduced)

**Chapter 2: Lines, Matrices, and the Projective Slope**
- 2.1 Coordinate Geometry: origin, axes, quadrants
- 2.2 Slope-Intercept and Standard Form
- 2.3 Systems of Linear Equations: substitution, elimination, graphical
- 2.4 Matrix Operations: row echelon form
- 2.5 The Projective Line ℙ¹(K): adjoining ∞ as slope
- 2.6 Determinants

**Chapter 3: Radicals and the Boundary of K**
- 3.1 Simplifying Radicals
- 3.2 Rationalizing Denominators: simple and conjugate
- 3.3 The Babylonian Method for Square Roots
- 3.4 Mental Exactitude: 8^(2/3) = 4 and 8^(3/2) = 16√2, both in K

**Chapter 4: Quadratics and the Exact Solution**
- 4.1 Factoring
- 4.2 Vertex Form by Completing the Square
- 4.3 The Quadratic Formula: discriminant analysis
- 4.4 The Complex Plane: i as lateral number, 90° rotation
- 4.5 Grant's Trick: complex numbers generating Pythagorean triples

**Chapter 5: The Central Objects: Slope and Length**
- 5.1 The Defining Right Triangle: base 1, height m, hypotenuse ℓ, ℓ² = 1 + m²
- 5.2 The Group Law ⊕: derivation from similar triangles or matrices
- 5.3 The Pythagorean Identity in ℓ, m language
- 5.4 Composition: R(m₁)R(m₂) = R(m₁ ⊕ m₂)
- 5.5 The Discrete Group: exact but not divisible; preview of trisection wall

---

### PART II: THE BABYLONIAN THREADS (c. 1800–500 BC)

**Chapter 6: The Spherical Thread: Time, Arc, and Approximation**
- 6.1 The 360° Convention: not a theorem, a convention
- 6.2 DMS and Sexagesimal Tables: approximate, interpolated, empirical
- 6.3 The Two-Sphere Model: exact geometry vs. approximate data
- 6.4 Physical Measurement: significant digits, parallax, arc-seconds at equator
- 6.5 Why the Sky is Still Approximate

**Chapter 7: The Planar Thread: Seqts, Slopes, and Exact Triples**
- 7.1 The Seqt in Pyramid Construction
- 7.2 Plimpton 322: exact generation of (m, ℓ) pairs
- 7.3 The Pythagorean Relation in Babylonian clothing
- 7.4 YBC 7289 and √2 approximation
- 7.5 Constructible Polygons: n = 3,4,5,6,8,10,12,15,16,17...
- 7.6 The List of Constructible n (OEIS A003401)

**→ First exact trigonometry interlude:**
- 7.7 The Defining Right Triangle applied: computing seqts as slopes
- 7.8 Area of triangles from exact slopes: the half-base-height formula in m, ℓ language
- 7.9 The Pythagorean Identity: ℓ² = 1 + m² on Plimpton 322 data

---

### PART III: THE GREEK DEMONSTRATION (c. 400–150 BC)

**Chapter 8: Geometry Without Numbered Angles**
- 8.1 Euclid's Elements: magnitude and ratio, angles as geometric figures
- 8.2 Geometric Algebra: Book II theorems in m, ℓ language
- 8.3 The Chord as Segment: length in a circle, not function of angle number
- 8.4 Constructions: angle bisectors, perpendicular bisectors, altitudes, seven equal segments
- 8.5 Why Trisection is Impossible: the cubic wall

**Chapter 9: Spherical Theorems and the Table Tradition**
- 9.1 Menelaus' Theorem: exact theorem for spherical triangle
- 9.2 Aristarchus: exact inequalities from exact premises
- 9.3 Hipparchus and the Chord Table: approximate instrument for astronomy
- 9.4 Ptolemy's Theorem: exact cyclic quadrilateral law
- 9.5 The Almagest: sexagesimal tables in 1/2° increments, explicit interpolation
- 9.6 The Great Divide: geometry proves, astronomy computes

**→ Second exact trigonometry interlude:**
- 9.7 The Law of Cosines: c² = a² + b² − 2ab/ℓ_C, derived from Euclid II.12–13
- 9.8 The Law of Sines: aℓ_A/m_A = bℓ_B/m_B = cℓ_C/m_C = 2R, from exact chords
- 9.9 The Circumdiameter in slope language: why 2R appears naturally
- 9.10 Area formulas: Heron's formula, SAS, ASA, AAS in m, ℓ notation

---

### PART IV: THE INDIAN ALGORITHMS (c. 500–1500 AD)

**Chapter 10: The Jyā: Slope as Half-Chord**
- 10.1 Āryabhaṭa and the Sine as Geometric Length
- 10.2 Exact Rules, Approximate Tables
- 10.3 The Spherical Law of Sines: exact theorem

**Chapter 11: The Algebraic Turn**
- 11.1 Bhāskara II: algebraic identities in m, ℓ language
- 11.2 The Radius and the Unit Circle: scaling from R to ℓ
- 11.3 Half-Angle and Sum-Difference Formulas in m, ℓ language
- 11.4 Slope Addition: the group law ⊕ in practice (problems from 2024 Ch. 20)

**Chapter 12: Madhava and the Bridge to the Transcendental**
- 12.1 The Exact Infinite Series: arctan m = m − m³/3 + m⁵/5 − ...
- 12.2 π ∉ K: the Leibniz formula proves π is not constructible
- 12.3 The Introduction of Radians: angle measure as real number
- 12.4 The Embedding (ℙ¹(K), ⊕) ↪ (ℝ/πℤ, +): the bridge, presented historically, not endorsed ontologically
- 12.5 What We Gain and What We Lose

**→ Third exact trigonometry interlude:**
- 12.6 The Matrix R(m): rotation as geometric construction
- 12.7 Composition of Rotations: R(m₁)R(m₂) = R(m₁ ⊕ m₂)
- 12.8 The Discrete Group: exact but not divisible; trisection revisited
- 12.9 Solving Triangles: putting the Laws together with Indian algebra

---

### PART V: THE EUROPEAN ANALYTIC TURN (c. 1600–1800)

**Chapter 13: The Cartesian Plane**
- 13.1 Coordinate Proofs: LoC and LoS re-derived analytically
- 13.2 Viète's Infinite Product
- 13.3 The Impossibility of Trisection: triple-angle formula in m, cubic wall
- 13.4 Why Transcendence Was Not a Choice but a Necessity: formal, not ontological

**Chapter 14: Euler and the Great Reveal**
- 14.1 The Rational Parametrization: R(m) as rational image of SO(2, ℝ)
- 14.2 Euler's Formula: e^(iθ) = cos θ + i sin θ
- 14.3 The Reveal of Names: "m was tangent all along, ℓ was secant all along"
- 14.4 Standard Notation Introduced Only Now: sin, cos, tan, sec as transcendental names
- 14.5 The Analytic Fork: exactitude traded for power

---

### PART VI: MODERN DIVERGENCE (c. 1800–Present)

**Chapter 15: The Three Geometries**
- 15.1 Spherical: Positive Curvature—exact theorems, historically approximate tables
- 15.2 Euclidean: Zero Curvature—our m, ℓ formalism
- 15.3 Hyperbolic: Negative Curvature—Lobachevsky's exact formulas
- 15.4 Curvature as Unifying Parameter: the three laws of cosines as one template

**Chapter 16: The Analytic Definition**
- 16.1 Cauchy–Weierstrass: sin x and cos x by exact power series
- 16.2 Complex Arguments: analytic continuation
- 16.3 Fourier Analysis: exact trigonometric series, approximate partial sums
- 16.4 The Eternal Return: the exact/approximate divide never disappears

**Chapter 17: The World Beyond This Class**
- 17.1 Standard Notation and Calculator Culture: the loss of exactitude
- 17.2 Floating Point vs. Constructible: what calculators actually do
- 17.3 What We Gain and What We Lose: power vs. exhibition
- 17.4 Review: From Discrete to Transcendental
- 17.5 The Exact Remnant: what remains constructible, compass and straightedge, human finitude

---

### APPENDICES

**Appendix A: The Constructible Field K**
**Appendix B: Hyperbolic Trigonometry**
**Appendix C: Spherical Astronomy for the Modern Student**
**Appendix D: The Golden Ratio and Its Kin**
**Appendix E: Historical Maps and Thread Diagrams**
**Appendix F: Tables**
