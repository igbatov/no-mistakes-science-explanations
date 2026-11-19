# Model: emission spectrum of sodium (why it has many lines, and which)

Status: built 2026-11-11. Numbers and statements verified 2026-11-11 (sections 6 and 7). Status codes: V = found in a cited source; V (weak) = weak source, analogy, or uncertain attribution; C = calculated or derived from V items, method given; U = not verified.

Scope: light emitted by neutral sodium atoms (Na I) with one electron excited, from the ultraviolet to the near infrared, with no external field. Related models: `zeeman-effect.md` (splitting of these lines in a magnetic field) and `atom-excitation-in-gas-discharge-lamp.md` (how the atoms get excited).

## 1. Objects

**Sodium atom**
- Core: nucleus (charge +11) and 10 inner electrons in closed shells (1s² 2s² 2p⁶). Net core charge +1.
- One outer (valence) electron. Its state is labelled n l: principal quantum number n ≥ 3, orbital angular momentum l (s, p, d, f for l = 0, 1, 2, 3).
- Ionization energy 5.1391 eV (limit at 41449.451 cm⁻¹).

**Energy levels of the outer electron** (binding energy = energy needed to remove the electron from that level)

| Level | Energy above ground (cm⁻¹) | Binding energy (eV) | Effective n* | Quantum defect n − n* |
|---|---|---|---|---|
| 3s | 0 | 5.139 | 1.627 | 1.373 |
| 3p (J = ½, 3/2) | 16956.172, 16973.368 | 3.037, 3.035 | 2.117 | 0.883 |
| 4s | 25739.991 | 1.948 | 2.643 | 1.357 |
| 3d (J = 5/2, 3/2) | 29172.839, 29172.889 | 1.522 | 2.990 | 0.010 |
| 4p (J = ½, 3/2) | 30266.99, 30272.58 | 1.386 | 3.133 | 0.867 |
| 5s | about 33200 | 1.023 | — | — |
| 4f | 34586.92 | 0.851 | 3.999 | 0.001 |
| 5p (J = ½, 3/2) | 35040.38, 35042.85 | 0.794 | 4.138 | 0.862 |

- For comparison, hydrogen: 1.512 eV for n = 3 and 0.850 eV for n = 4, the same for every l.
- Levels continue upward without end, crowding together towards the ionization limit.

**Lines** (air wavelengths)

| Transition | Wavelengths (nm) | Series | Region | Transition rate A (10⁸ s⁻¹) |
|---|---|---|---|---|
| 3p → 3s | 588.995, 589.592 | principal | yellow | 0.616, 0.614 |
| 4p → 3s | 330.237, 330.298 | principal | ultraviolet | 0.0281 |
| 5p → 3s | 285.281, 285.301 | principal | ultraviolet | 0.00554 |
| 4s → 3p | 1138.145, 1140.378 | sharp | infrared | 0.090, 0.176 |
| 5s → 3p | about 615.4, 616.1 | sharp | orange-red | not looked up |
| 6s → 3p | 514.88, 515.34 | sharp | green | not looked up |
| 3d → 3p | 818.326, 819.479, 819.482 | diffuse | near infrared | 0.453, 0.090, 0.54 |
| 4d → 3p | 568.263, 568.819, 568.821 | diffuse | yellow-green | not looked up |
| 5d → 3p | 497.854, 498.281 | diffuse | blue-green | not looked up |
| 6d → 3p | 466.481, 466.856 | diffuse | blue | not looked up |
| 4f → 3d | 1846.5 | fundamental | infrared | 0.140 |

**Photon**
- Energy = difference between the two level energies. Carries one unit of angular momentum (electric-dipole radiation).

## 2. Processes

| # | Process | Condition | Size or note |
|---|---|---|---|
| S1 | Spontaneous emission between two levels | upper level populated; transition allowed (S3) | one line per allowed pair of levels; rates in the table above |
| S2 | Core penetration and screening | outer electron in a low-l orbit passes inside the inner shells and feels more than charge +1 | lowers s levels most, then p, d hardly, f almost not at all: quantum defects 1.37, 0.88, 0.01, 0.001. Makes the level energy depend on l, unlike hydrogen |
| S3 | Selection rule for electric-dipole radiation | l must change by ±1; n may change by any amount | sorts the lines into series: p → s (principal, ends on 3s), s → p (sharp), d → p (diffuse), f → d (fundamental) |
| S4 | Spin–orbit splitting (fine structure) | l ≥ 1 | 3p: 17.196 cm⁻¹ (0.6 nm at 589 nm); 4p: 5.59 cm⁻¹; 5p: 2.47 cm⁻¹; 3d: 0.05 cm⁻¹, inverted. Turns each line into a close doublet (or a three-component group for d → p) |
| S5 | Cascade | atom excited to a high level | it can return in several steps, emitting one line per step, for example 4d → 3p → 3s |
| S6 | Population of upper levels | depends on the source: electron collisions in a discharge, thermal collisions in a flame | sets the relative brightness of the lines. In a low-pressure sodium lamp the output is essentially the 589.0/589.6 nm pair |
| S7 | Weakening along a series | higher members have smaller transition rates | principal series: rate falls by a factor of 22 from 3p to 4p and 111 from 3p to 5p |
| S8 | Self-absorption of resonance lines | vapour dense enough to re-absorb lines ending on the ground state | distorts or reverses the D lines; lines ending on 3p are much less affected because few atoms are in 3p |
| S9 | Hyperfine splitting | nuclear spin 3/2 | ground state 1.77 GHz; far below the resolution of an ordinary spectroscope |
| S10 | Lines of the sodium ion (Na II) | energetic sources such as sparks; needs ionization and further excitation | many lines, mostly in the ultraviolet; a different spectrum from that of the neutral atom |
| S11 | Lines of other elements in the source | buffer gas in a lamp (neon, argon), impurities | appear alongside the sodium lines; not part of the sodium spectrum |
| S12 | Forbidden transitions (l unchanged or changing by 2) | very weak magnetic-dipole or electric-quadrupole radiation | not looked up |
| S13 | Splitting or shifting in external fields (Zeeman, Stark) | field present | see `zeeman-effect.md`; outside this model's scope |

## 3. Regimes

**By resolution of the instrument**
- Low (cannot separate 0.6 nm): each transition looks like one line; about ten sodium lines between the ultraviolet and the near infrared.
- Medium (separates 0.6 nm, about 17 cm⁻¹): the D lines and other lines ending on 3p appear as doublets (S4).
- High (GHz): hyperfine structure (S9) shows.

**By excitation energy available**
- About 2.1 eV per atom (cool flame, low-pressure lamp): 3p is populated; the yellow pair dominates.
- 3 to 5 eV: higher s, p and d levels are populated; the sharp, diffuse and higher principal lines appear.
- Above 5.14 eV, with further energy: ionization, then Na II lines (S10).

**By vapour density**
- Low: all lines sharp.
- High: resonance lines self-absorbed (S8).

**By viewing mode**
- Emission from an excited source: all four series can appear.
- Absorption by cool vapour: atoms start in 3s, so mainly the principal series appears.

## 4. Selection: "why are there several different lines in the spectrum of sodium?"

**Kept:** S1 with the level scheme (many levels, so many differences), S2 (levels depend on l, which multiplies the number of distinct differences), S3 (limits which pairs occur and groups them into series), S4 (doublets), S5 and S6 (which lines are bright in a given source).

**Neglected, with reason:**
- S9: 1.77 GHz is about 0.002 nm at 589 nm, three hundred times smaller than the 0.6 nm doublet spacing (C).
- S12: assumed far weaker than allowed lines (U).
- S13: no external field in the question.
- S10, S11: real in some sources, but they are not lines of the neutral sodium atom; mentioned as a caution.

## 5. Known limits of this model

- One-electron picture: the ten core electrons are treated as a fixed screen. States with a core electron excited are left out.
- Quantum defects are treated as constant along a series; they drift slightly with n (1.373 for 3s, 1.357 for 4s).
- Line brightness is described qualitatively; no level populations are calculated.
- Transition rates were looked up for the persistent lines only.

## 6. Verification of numbers

Sources:
- [S1] NIST Handbook of Basic Atomic Spectroscopic Data, Na I energy levels: https://physics.nist.gov/PhysRefData/Handbook/Tables/sodiumtable5.htm
- [S2] Same handbook, Na I persistent lines (wavelengths, rates, classifications): https://physics.nist.gov/PhysRefData/Handbook/Tables/sodiumtable3.htm
- [S3] Same handbook, strong lines of sodium: https://physics.nist.gov/PhysRefData/Handbook/Tables/sodiumtable2_a.htm
- [S4] CODATA 2022 (Rydberg constant, electron mass): https://www.physics.nist.gov/cuu/pdf/wall_2022.pdf
- [S5] Dublin City University lecture notes, alkali spectra (table of quantum defects): https://www.physics.dcu.ie/~be/Ps415/Original/Atomic2.pdf
- [S6] A&A 2019, Table 1 (Na level energies incl. 5s): https://www.aanda.org/articles/aa/full_html/2019/08/aa35593-19/T1.html
- [S7] D. A. Steck, Sodium D Line Data: https://steck.us/alkalidata/sodiumnumbers.pdf

| Quantity | Value | Status | Source or formula |
|---|---|---|---|
| Levels 3s, 3p, 4s, 3d, 4p, 4f, 5p; limit | as in the table | V | S1 |
| 5s level | about 33200 cm⁻¹ | V | S6 (rounded value) |
| Binding energies | as in the table | C | (limit − level) / 8065.544 cm⁻¹ per eV |
| Effective n* and quantum defects | 1.373, 0.883, 1.357, 0.010, 0.867, 0.001, 0.862 | C | n* = √(R_Na / (limit − level)), R_Na = 109734.7 cm⁻¹ |
| Quantum defects, literature | s 1.35, p 0.85, d 0.01, f 0.00 | V | S5; agrees with the C values |
| Hydrogen binding, n = 3, 4 | 1.512, 0.850 eV | C | 13.6057 eV / n² |
| Wavelengths 285.28, 285.30, 330.24, 330.30, 589.00, 589.59, 818.33, 819.48, 1138.1, 1140.4, 1846.5 nm | — | V | S2 |
| Classifications of those lines | — | V | S2 |
| Wavelengths 466.48, 466.86, 497.85, 498.28, 514.88, 515.34, 568.26, 568.82 nm | — | V | S3 |
| Assignment of 568, 498, 467 nm to 4d, 5d, 6d → 3p | — | C | quantum-defect formula with δ_d = 0.010 predicts 568.6, 498.2, 466.8 nm |
| Assignment of 515 nm to 6s → 3p | — | C | formula with δ_s = 1.373 predicts 516.6 nm (within about 1 nm; δ_s drifts with n) |
| 5s → 3p at about 615.4, 616.1 nm | — | C | from the S6 level (rounded) minus the 3p levels |
| Transition rates | as in the table | V | S2 |
| Rate ratios 22 and 111 | — | C | 0.616/0.0281; 0.616/0.00554 |
| Fine-structure intervals 17.196, 5.59, 2.47, 0.05 cm⁻¹ | — | C | differences of S1 levels |
| 3d doublet inverted (J = 5/2 below 3/2) | — | V | S1 |
| Ground hyperfine 1.77 GHz; 0.002 nm | — | V, C | S7; Δλ = λ²Δν/c |

## 7. Verification of statements

Sources for statements:
- [T1] NIST, "Atomic Spectroscopy: term series, quantum defects": https://www.nist.gov/pml/atomic-spectroscopy-term-series-quantum-defects
- [T2] e-PG Pathshala, "Spectra of Alkali Metals": https://ebooks.inflibnet.ac.in/phyp10/chapter/spectra-of-alkali-metals
- [T3] College of William & Mary lab manual, "Spectrum of Sodium": https://qo.physics.wm.edu/cgit/manual_for_Experimental_Atomic_Physics.git/plain/unused_chapters/naspec.tex
- [T4] Caltech course notes, alkali orbits: https://sites.astro.caltech.edu/~srk/Ay121/SRKNotes/AlkaliOrbits.pdf
- [T5] IET review "Low-pressure sodium discharge lamps" (abstract): https://digital-library.theiet.org/doi/10.1049/ip-a-1.1981.0065
- [T6] Lamptech, discharge current density (self-absorption): https://lamptech.co.uk/Documents/SO%20Density.htm
- [S1]–[S5] as in section 6.

| Item | Statement | Status | Source |
|---|---|---|---|
| Objects | outer electron moves in the field of a core of net charge +1 | V | T2, T1 |
| S1 | each line is a transition between two levels, photon energy = level difference | U | textbook, not looked up separately |
| S2 | deviations from hydrogen come from core penetration (low l) and core polarization (high l) | V | T1, T2, T4 |
| S2 | s levels lie deepest, then p, d, f; defect depends strongly on l and little on n | V | T2, T4, S5 |
| S2 | d and f levels are close to hydrogen's | V | T3; C from section 6 |
| S3 | selection rule Δl = ±1, n unrestricted | V | T2, T3 |
| S3 | the four series and which levels they connect | V | S5, T2 |
| S4 | series lines are doublets; d → p lines have three components | V | T2, S5; S2 lists three 3d → 3p components |
| S5 | cascades occur | C | follows from S1 and S3: an upper level reached by S6 can decay only to levels allowed by S3, which may themselves be excited levels |
| S6 | low-pressure sodium lamp emits essentially the D lines | V | T5 |
| S6 | brightness set by populations of upper levels | U | textbook, not looked up |
| S7 | higher principal-series members have smaller rates | V | S2 |
| S8 | sodium vapour absorbs its own resonance light | V | T6 |
| S8 | lines ending on 3p are less affected | U | reasoning from the small 3p population, not sourced |
| S9 | hyperfine structure exists and is small | V | S7 |
| S10 | Na II lines exist, many in the ultraviolet | V | S3 |
| S11 | lamp buffer-gas lines can appear | V (weak) | lamp model: start-up glow is from neon–argon; presence in the warm-lamp spectrum not looked up |
| S12 | forbidden lines are far weaker | U | not looked up |
| Regimes | absorption from cool vapour shows mainly the principal series | V | T2 |
| Regimes | boundaries by excitation energy | C | level energies in section 1 |
