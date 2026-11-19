# Model: Zeeman effect (atom emitting light in a magnetic field)

Status: built 2026-11-11. Numbers verified 2026-11-11 (section 6). Statements verified 2026-11-11 (section 7). Status codes: V = found in a cited source; C = calculated or derived from V items, method given; U = not verified. Update this document when a chat adds or corrects something.

Scope: a free atom with one or a few outer electrons, in a static, uniform magnetic field B, emitting or absorbing visible light. Worked examples: sodium D lines and the cadmium red line.

## 1. Objects

**Electron**
- Charge −e, mass m. e/m = 1.7588 × 10¹¹ C/kg.
- Spin S = ½, spin g-factor g_s = 2.00232 (taken as 2 in the simple formulas).
- Orbital g-factor g_l = 1.

**Constants for magnetic effects**
- Bohr magneton μ_B = eħ/2m = 9.2740 × 10⁻²⁴ J/T = 5.7884 × 10⁻⁵ eV/T.
- μ_B/h = 13.996 GHz per tesla.
- Larmor angular frequency ω_L = eB/2m = 8.794 × 10¹⁰ rad/s per tesla.
- Nuclear magneton = μ_B/1836.15.

**Atomic level**, labelled ²ˢ⁺¹L_J
- L: orbital angular momentum, S: total spin, J: total angular momentum, m_J from −J to +J in integer steps (2J + 1 values).
- Landé factor (weak field, LS coupling, g_s = 2, g_l = 1): g = 1 + [J(J+1) + S(S+1) − L(L+1)] / [2J(J+1)]. This form omits multi-electron and QED corrections.

**Sodium (Na-23, nuclear spin I = 3/2)**

| Level | Configuration | L | S | J | g (Landé formula) | g (measured) | Sublevels |
|---|---|---|---|---|---|---|---|
| ²S1/2 (ground) | 3s | 0 | ½ | ½ | 2 | 2.0023 | 2 |
| ²P1/2 | 3p | 1 | ½ | ½ | 2/3 | 0.6658 | 2 |
| ²P3/2 | 3p | 1 | ½ | 3/2 | 4/3 | 1.3342 | 4 |

- D1: ²P1/2 → ²S1/2, 589.756 nm in vacuum (about 589.59 nm in air). Photon energy 2.1023 eV.
- D2: ²P3/2 → ²S1/2, 589.158 nm in vacuum (about 589.00 nm in air). Photon energy 2.1044 eV.
- Fine-structure gap of 3p: 17.196 cm⁻¹ = 2.132 meV = 515.5 GHz.
- 3p lifetime: 16.30 ns (²P1/2), 16.25 ns (²P3/2). Natural linewidth 9.8 MHz.
- Fine-structure gaps of the d levels are far smaller and inverted (J = 5/2 below J = 3/2): 3d 0.050 cm⁻¹ = 1.5 GHz; 4d 1028.3 MHz; 5d and 6d smaller still (not looked up; about 0.5 and 0.3 GHz if the gap scales as 1/n³).
- The s levels (4s, 5s, 6s …) have no fine structure; like 3s they are ²S1/2 with g = 2.
- Ground-state hyperfine splitting: 1.7716 GHz.
- Nuclear g-factor g_I = −0.00080, about 4 × 10⁻⁴ of the ground-state g_J.
- Ionization energy: 5.1391 eV.

**Cadmium red line**
- 643.8 nm (465.7 THz), ¹D2 → ¹P1. Both levels have S = 0, so g = 1 for both.
- Natural cadmium: six even isotopes with nuclear spin 0, and two odd isotopes, ¹¹¹Cd (12.8%) and ¹¹³Cd (12.2%), with I = ½, which add hyperfine structure.

**Light**
- Electric-dipole photon carries one unit ħ of angular momentum.

## 2. Processes

| # | Process | Condition | Size or rate |
|---|---|---|---|
| P1 | Torque on the atomic magnetic moment: precession of J about B | B ≠ 0, weak-field regime (R2) | rate g·ω_L |
| P2 | Linear Zeeman shift of each sublevel | same as P1 | ΔE = g·m_J·μ_B·B; 5.79 × 10⁻⁵ eV (14.0 GHz) per tesla for g·m_J = 1 |
| P3 | Spin–orbit coupling: L and S precess about J; fine structure | L ≠ 0 and S ≠ 0 | 2.13 meV for Na 3p (internal precession ≈ 5.2 × 10¹¹ Hz) |
| P4 | Decoupling of L and S (Paschen–Back) | μ_B·B comparable to or larger than the fine-structure gap | for Na 3p, μ_B·B = gap at 36.8 T; μ_B·B/gap = 0.027 at 1 T |
| P5 | Electric-dipole emission or absorption between sublevels | Δm_J = 0 (π) or ±1 (σ); J = 0 → J = 0 forbidden | sets which lines exist |
| P6 | Polarization and angular pattern of the emitted light | follows from P5 | π: linear along B, no emission along B. σ: circular seen along B, linear ⊥ B seen across B; elliptical at intermediate angles |
| P7 | Hyperfine coupling of J to nuclear spin I | I ≠ 0 | Na ground state 1.77 GHz; equals the ground-state Zeeman splitting (g = 2) at 0.063 T |
| P8 | Nuclear Zeeman shift | I ≠ 0 | for Na, about 4 × 10⁻⁴ of the electronic shift |
| P9 | Quadratic (diamagnetic) shift | grows as B² and as orbit size squared, so roughly as n⁴ for excited states | 6.2 × 10⁻¹¹ eV at 1 T for an orbit of one Bohr radius (10⁻⁶ of μ_B·B); exceeds the linear term at 1 T for principal quantum number above roughly 25 |
| P10 | Doppler broadening of the line | thermal motion of emitting atoms | Na D lines: 1.70 GHz FWHM at 500 K, 1.75 GHz at 533 K |
| P11 | Natural, pressure and self-absorption broadening | finite lifetime, collisions, dense vapour | natural 9.8 MHz; the others depend on lamp conditions |
| P12 | Stark shift from electric fields in the discharge | E ≠ 0 | not estimated here |
| P13 | Coherent precession observed in time (quantum beats, Hanle effect, magnetic resonance) | atom prepared in a superposition of sublevels | beat frequency = sublevel spacing / h; the superposition precesses about B at the Larmor frequency |

**Sub-model: classical Lorentz oscillator.** Electron on a spring, frequency ω₀, plus magnetic force. Gives three modes at ω₀ and ω₀ ± ω_L, equivalent to an orbit precessing at ω_L. It reproduces P2, P5 and P6 for lines where both levels have S = 0 (g = 1). It fails when S ≠ 0; sodium needs the quantum treatment.

How one precessing orbit contains three frequencies (C, derived from the three modes): take a circular orbit of radius R whose axis is tilted by θ from B. Its motion splits into (a) an oscillation along B of amplitude R·sin θ, untouched by a rotation about B, frequency ω₀; (b) a circle about B in the sense of the precession, radius R(1 + cos θ)/2, frequency ω₀ + ω_L; (c) a circle about B in the opposite sense, radius R(1 − cos θ)/2, frequency ω₀ − ω_L. The precession multiplies the in-plane motion by a slow rotation, so it appears as the sum and difference frequencies and not as a separate component at ω_L; the orbit is centred on the nucleus, so nothing in the charge's position varies at ω_L alone. Limits: θ = 0 gives only ω₀ + ω_L, θ = 180° only ω₀ − ω_L, θ = 90° all three with (b) and (c) equal. A lamp contains atoms with every tilt, so all three lines appear together.

**Vector model (semi-classical picture of P1 and P3).**
- μ = −(e/2m)(L + 2S) = −(e/2m)(J + S); not parallel to J.
- Fast precession about J averages μ to −g(e/2m)J.
- dJ/dt = g(e/2m) B × J.
- The picture of the electron as a literal spinning ball is a cartoon. If the ball has the classical electron radius (2.8 × 10⁻¹⁵ m), its equator would have to move at roughly ten times the speed of light. A ball whose charge and mass are distributed alike would also give g = 1, not 2 (this second point is U).

## 3. Regimes

| # | Regime | Boundary | What dominates |
|---|---|---|---|
| R0 | B = 0 | — | fine structure and hyperfine structure; sublevels degenerate |
| R1 | Hyperfine regime | Zeeman splitting ≲ hyperfine splitting; for Na ground state B ≲ 0.06 T | F is a good quantum number, shifts g_F·m_F·μ_B·B; P7 with P2. At intermediate fields the ground state follows the Breit–Rabi formula |
| R2 | Weak field (anomalous Zeeman) | hyperfine ≪ μ_B·B ≪ fine structure; for Na roughly 0.1 T to a few T | P1, P2, P3, P5, P6. For the nucleus this is already the "hyperfine Paschen–Back" regime: states labelled m_J, m_I |
| R3 | Intermediate | μ_B·B approaching fine structure; Na 3p: roughly 5 T to 100 T (boundaries are a judgement, not sharp) | P2 and P4 mixed; g-factor formula inaccurate; in general needs numerical diagonalization |
| R4 | Strong field (Paschen–Back) | μ_B·B ≫ fine structure (≫ 37 T for Na 3p) | L and S precess about B separately; J is no longer a good quantum number; shifts (m_L + 2m_S)·μ_B·B; transitions keep the spin orientation (Δm_S = 0, Δm_L = 0, ±1), so the spin part of the shift is the same in both levels and cancels in the line positions; pattern is a triplet whose lines are narrow doublets (one member from spin-up atoms, one from spin-down, separated by the leftover spin–orbit energy) |
| R5 | Very strong field or highly excited states | P9 comparable to P2 (at 1 T: n above roughly 25) | diamagnetic term matters |

Regimes apply level by level, not atom by atom. The boundary for each level is set by its own fine-structure gap, so one spectral line can join an upper level in R4 to a lower level in R2. For sodium: μ_B·B equals the gap at 0.107 T for 3d and 0.073 T for 4d, against 36.8 T for 3p. At 1 T the d levels are therefore in the Paschen–Back regime while 3p is still in the weak-field regime. Patterns of such lines do not follow from two Landé factors; they are obtained by diagonalizing A·L·S + μ_B·B·(L_z + 2S_z) for each level.

Resolution condition: components are separable when their spacing exceeds the line width. For the Na D lines, component shifts range from 4.7 to 23.3 GHz per tesla and the smallest spacing between neighbouring components is 9.3 GHz per tesla. With a Doppler width of about 1.7 GHz, spacing equals width at about 0.18 T. A high-resolution instrument (Fabry–Pérot) is needed.

Special case S = 0: P3 and P4 are absent, g = 1 for both levels, and the pattern is the normal triplet in R2 through R4.

## 4. Selection for the standard teaching experiment

Conditions: discharge lamp, B ≈ 0.2 to 1 T, viewing across or along B, Fabry–Pérot etalon.

**Kept:** P1, P2, P3, P5, P6, and P10 as the resolution limit.

**Neglected, with reason:**
- P4: μ_B·B / fine-structure gap = 0.027 at 1 T for Na.
- P7: hyperfine 1.77 GHz is small next to the 9.3 GHz component spacing at 1 T, and is comparable to the Doppler width, so it is not resolved. This reasoning fails below about 0.2 T.
- P8: about 4 × 10⁻⁴ of P2.
- P9: about 10⁻⁶ of P2 at 1 T.
- P11 (pressure, self-absorption), P12: not estimated; assumed smaller than P10 in a low-pressure lamp (U).

**Resulting patterns (shifts in units of μ_B·B; 1 unit = 14.0 GHz per tesla):**
- Na D1: ±2/3 (π), ±4/3 (σ). Four lines. Total span 8/3 units = 37 GHz = 0.043 nm at 1 T.
- Na D2: ±1/3 (π), ±1 and ±5/3 (σ). Six lines.
- Cd 643.8 nm: 0 (π), ±1 (σ). Three lines. σ shift 14 GHz = 0.019 nm at 1 T.
- Viewed along B, the π lines are absent.
- These use the Landé-formula g values; the measured g values differ by about 0.1%.

**Other visible sodium lines at 1 T (calculated by diagonalization; shifts in GHz from the zero-field line):**
- Sharp series, ns → 3p (616.07/615.42 nm, 515.34/514.88 nm): the levels are ²S1/2 and ²P, the same pair of g-factors as the D lines. The line ending on ²P3/2 (longer wavelength) gives the six-line pattern, the one ending on ²P1/2 the four-line pattern.
- Diffuse series, nd → 3p (568.82/568.26, 498.28/497.85, 466.86/466.48 nm): upper level in R4, lower in R2. The line group ending on ²P3/2 has about 15 components and the group ending on ²P1/2 has 12, lying on a grid of about 4.7 GHz (μ_B·B/3) between −24 and +24 GHz, several of them coinciding within 0.5 GHz.
- At 1 T the 3p level already departs slightly from the weak-field formula: the D2 components come out at −23.2, −14.0, −4.6, +4.8, +14.0, +23.4 GHz instead of symmetric values.

## 5. Known limits of this model

- Assumes LS coupling. Heavy atoms need intermediate or jj coupling, and their g-factors differ from the Landé formula.
- Assumes a static, uniform field. Field gradients (Stern–Gerlach) and oscillating fields (magnetic resonance) need extra processes.
- Line intensities within a pattern are not included.
- Electric-quadrupole and magnetic-dipole transitions are left out.
- The classical and vector pictures are aids; the quantitative content is in the sublevel energies and selection rules.

## 6. Verification of numbers

Sources:
- [S1] CODATA 2022 recommended values, NIST: https://www.physics.nist.gov/cuu/pdf/wall_2022.pdf
- [S2] D. A. Steck, "Sodium D Line Data", rev. 2.3.4 (2025): https://steck.us/alkalidata/sodiumnumbers.pdf
- [S3] NIST Handbook of Basic Atomic Spectroscopic Data, Na I energy levels and lines: https://physics.nist.gov/PhysRefData/Handbook/Tables/sodiumtable5.htm and .../sodiumtable3.htm
- [S4] Leybold physics leaflet, normal Zeeman effect in cadmium (copy): https://ifsc.usp.br/lavfis/wp-content/uploads/2024/09/Leybold-Normal-Zeeman-effect-1.pdf
- [S5] WebElements, cadmium isotopes: https://webelements.co.uk/cadmium/isotopes.html ; Roederer et al., arXiv:1204.3901

| Quantity | Value | Status | Source or formula |
|---|---|---|---|
| e/m | 1.7588 × 10¹¹ C/kg | V | S1 |
| g_s | 2.00232 | V | S1 |
| μ_B | 9.2740 × 10⁻²⁴ J/T; 5.7884 × 10⁻⁵ eV/T | V | S1 |
| μ_B/h | 13.996 GHz/T | C | μ_B / h |
| ω_L per tesla | 8.794 × 10¹⁰ rad/s | C | (e/m)/2 |
| proton/electron mass ratio | 1836.15 | V | S1 |
| Na nuclear spin | 3/2 | V | S2 |
| Na measured g_J | 2.0023, 0.6658, 1.3342 | V | S2 |
| Na nuclear g_I | −0.00080; 4 × 10⁻⁴ of g_J | V, C | S2 |
| D1, D2 vacuum wavelengths | 589.756, 589.158 nm | V | S2 |
| D1, D2 air wavelengths | ≈ 589.59, 589.00 nm | V | S3 gives 589.592 and 588.995; S2 gives values about 0.005 nm higher, so the third decimal is uncertain here |
| 3p levels | 16956.172, 16973.368 cm⁻¹ | V | S3 |
| Fine-structure gap | 17.196 cm⁻¹; 2.132 meV; 515.5 GHz | C | difference of S3 levels |
| D photon energies | 2.1023, 2.1044 eV | C | S3 levels / 8065.544 cm⁻¹ per eV |
| 3p lifetimes | 16.30, 16.25 ns | V | S2 |
| Natural linewidth | 9.8 MHz | V | S2 |
| Ground hyperfine splitting | 1.7716 GHz | V | S2 |
| Na ionization energy | 5.1391 eV | V | S2, S3 |
| Cd line | 643.8 nm, 465.7 THz, ¹D2 → ¹P1, S = 0 | V | S4 |
| Cd σ shift at 1 T | 14 GHz, 0.02 nm | V | S4; C gives 0.019 nm |
| Cd isotopes | six even with I = 0; ¹¹¹Cd 12.80%, ¹¹³Cd 12.22%, both I = ½ | V | S5 |
| Paschen–Back field, Na 3p | 36.8 T; ratio 0.027 at 1 T | C | gap / μ_B |
| Hyperfine crossover | 0.063 T | C | 1.7716 GHz / (2 × 13.996 GHz/T) |
| Diamagnetic shift | 6.2 × 10⁻¹¹ eV at 1 T | C | e²B²a₀²/8m; order-of-magnitude estimate for r = a₀ |
| Diamagnetic > linear at 1 T for n > ~25 | — | V (weak source) | T8 (patent text); consistent with n⁴ scaling in T7 |
| Doppler FWHM | 1.70 GHz (500 K), 1.75 GHz (533 K) | C | ν·√(8kT·ln2 / Mc²), M = 22.99 u |
| D-line component shifts | 4.7 to 23.3 GHz/T; min spacing 9.3 GHz/T | C | (1/3 … 5/3) × 13.996 |
| D1 span at 1 T | 37 GHz; 0.043 nm | C | (8/3) × 13.996 GHz; Δλ = λ²Δν/c |
| Classical electron radius; equator speed ≈ 10 c | 2.8 × 10⁻¹⁵ m | V | T11 |
| R3 boundaries (5 T, 100 T) | — | U | judgement |
| 3d fine-structure gap | 0.050 cm⁻¹ = 1.50 GHz, inverted | V, C | S3 (levels 29172.839 and 29172.889 cm⁻¹) |
| 4d fine-structure gap | 1028.3(6) MHz | V | S6 |
| 5d, 6d gaps | about 0.5, 0.3 GHz | U | 1/n³ scaling from 4d; not looked up |
| Field where μ_B·B = gap | 0.107 T (3d), 0.073 T (4d) | C | gap / 13.996 GHz per tesla |
| Patterns of the sharp and diffuse lines at 1 T | as listed in section 4 | C | numerical diagonalization of A·L·S + μ_B·B·(L_z + 2S_z) in the m_l, m_s basis, dipole strengths from Clebsch–Gordan coefficients; the same code reproduces ±2/3, ±4/3 for D1 |

- [S6] Fredriksson & Svanberg, Phys. Lett. A 53, 61 (1975), fine structure of Na 4d: https://www.lunduniversity.lu.se/lup/publication/8da77823-be7e-4b13-aad3-d4d72074bac8

Corrections to numbers (2026-11-11):
- Fine-structure gap 516 GHz → 515.5 GHz.
- "P2 ≈ 9 to 28 GHz per tesla for the D lines" was wrong: 28 GHz/T is the ground-level sublevel spacing (g = 2), not a line shift. Replaced by component shifts 4.7 to 23.3 GHz/T and minimum spacing 9.3 GHz/T.
- Added measured g_J values, vacuum wavelengths, and the D1 span (0.043 nm at 1 T; an earlier chat answer said "about 0.03 nm").
- P8 "about 10⁻³ or less" → 4 × 10⁻⁴ for sodium, from the measured g_I.

## 7. Verification of statements

Sources for statements:
- [T1] HyperPhysics, Paschen–Back effect and vector model: https://hyperphysics.gsu.edu/hbase/quantum/paschen.html ; https://hyperphysics.gsu.edu/hbase/quantum/vecmod.html
- [T2] J. Baez et al., "Spin" notes, magnetic moments: https://math.ucr.edu/home/baez/spin/node11.html
- [T3] University of Leicester lecture notes PA322, lecture 9: https://www.star.le.ac.uk/~nrt3/322/lect9.pdf
- [T4] Socas-Navarro, Trujillo Bueno, Landi Degl'Innocenti, arXiv:astro-ph/0409005
- [T5] arXiv:1110.2282 (polarization of Zeeman components); arXiv:astro-ph/0601625; arXiv:2011.01781
- [T6] Tipler & Llewellyn excerpt on the Zeeman effect: https://physicsx.erau.edu/Courses/CoursesS2021/PS315/Zeeman/Zeeman%20Effect%20(Freeman).pdf
- [T7] Rydberg helium in magnetic fields, arXiv:1701.01638; arXiv:1802.08587 (supplement)
- [T8] US patent 11774482 (Rydberg-atom field sensing): https://image-ppubs.uspto.gov/dirsearch-public/print/downloadPdf/11774482
- [T9] Hanle effect, Wikipedia: https://en.wikipedia.org/wiki/Hanle_effect ; Stony Brook quantum-beats page: https://www.stonybrook.edu/metcalf/qbeats.html ; Cohen-Tannoudji, Physica Scripta T70, 79 (1997): https://www.phys.ens.psl.eu/~cct/articles/physica-scripta/phys-scrip-T70-p79-1997.pdf
- [T10] LibreTexts, normal Zeeman effect: https://chem.libretexts.org/Bookshelves/Physical_and_Theoretical_Chemistry_Textbook_Maps/Supplemental_Modules_%28Physical_and_Theoretical_Chemistry%29/Quantum_Mechanics/Zeeman_Effect/1%3A_Normal_Zeeman_Effect
- [T11] Kiessling/Appel, arXiv:math-ph/0009003; Scientific American on spin: https://www.scientificamerican.com/article/quantum-particles-arent-spinning-so-where-does-their-spin-come-from/ ; arXiv:1502.01925
- [T12] Zeeman, Astrophys. J. 5, 332 (1897): https://articles.adsabs.harvard.edu/pdf/1897ApJ.....5..332Z ; Kox, history of the discovery: https://sites.astro.caltech.edu/~srk/Ay121/SRKNotes/ZeemanEffect_History.pdf
- [S2], [S4] as in section 6.

| Item | Statement | Status | Source |
|---|---|---|---|
| Landé formula | g_J expression and that it comes from projecting μ on J | V | S2 (Eq. 21), T3, T2 |
| Vector model | μ ∝ L + 2S, not parallel to J; L and S precess about J; in a weak field J precesses about B | V | T2, T1, T3 |
| P1 | precession rate g·ω_L | C | from dJ/dt = g(e/2m)B × J; the equation itself follows from the V vector model |
| P2 | sublevel shift g·m·μ_B·B | V | S2 (Eq. 24, for F levels), T3 |
| P3 | fine structure from L–S coupling | V | S2 |
| P4, R4 | strong field decouples L and S; they precess separately about B; J not a good quantum number; shifts (m_L + 2m_S)μ_B·B; triplet of narrow doublets | V | T1, T3, T4, T6 |
| R4 | strong-field selection rules Δm_S = 0, Δm_L = 0, ±1; lines resemble the normal triplet | V | T3 |
| R4 | the two members of each narrow doublet come from the two spin orientations | C | follows from Δm_S = 0 and a residual spin–orbit term proportional to m_L·m_S |
| R3 | intermediate fields need numerical treatment in general | V | T4, S2 |
| P5 | Δm = 0, ±1 | V | T5, S4 |
| P5 | J = 0 → J = 0 forbidden | U | textbook rule, not looked up |
| P6 | π absent along B; σ circular and opposite along B; across B all linear, π ∥ B, σ ⊥ B; elliptical in between | V | T5, S4 |
| P7, R1 | weak field: F good quantum number; strong field: hyperfine Paschen–Back, states m_J, m_I; Breit–Rabi for the ground state | V | S2 |
| P8 | nuclear term much smaller than electronic | V | S2 |
| P9, R5 | diamagnetic term scales as n⁴; usually neglected for low states | V | T7 |
| P10 | Doppler width formula | U | standard formula, not sourced |
| P11, P12 | assumed smaller than Doppler width in a low-pressure lamp | U | not looked up |
| P13 | superposition of Zeeman sublevels precesses at the Larmor frequency; beats at the Zeeman splitting; Hanle effect is the zero-field case | V | T9 |
| Lorentz sub-model | linear oscillation = one component along the field plus two counter-rotating ones; outer lines at ν₀ ± ν_L | V | T10, S4 |
| Lorentz sub-model | applies to S = 0 lines; sodium needs quantum treatment | V | S4, T12 (encyclopedia mirror of the Zeeman-effect article) |
| Spinning ball | equator faster than light for a classical-radius sphere (Lorentz's objection) | V | T11 |
| Spinning ball | classical ball gives g = 1 | U | standard argument, value not confirmed in a source |
| Cd, S = 0 | normal effect occurs for S = 0 transitions | V | S4 |
| Limits | LS coupling assumed; jj coupling changes g | U | textbook, not looked up |
| Regimes per level | the weak/strong boundary depends on each level's own fine-structure gap | C | follows from P4's condition applied to each level; T1 notes that lithium, with a 0.3 cm⁻¹ gap, meets Paschen–Back conditions at modest fields |
| Na d levels | fine structure is inverted | V | S3, S6 and Fredriksson & Svanberg 1976 (core.ac.uk/download/83786432.pdf) |
| Diffuse-line patterns | upper level in R4, lower in R2 at 1 T; pattern from diagonalization | C | section 6; not compared with a measured or published pattern |
| Light | dipole photon carries ħ | U | textbook, not looked up |

Historical note (V, T12): Zeeman's first observation in 1896, with a sodium-salted flame between magnet poles, was a widening of the D lines, not a resolved pattern. Resolved splitting was obtained later with cadmium. Earlier chat answers that described the full line pattern as "what Zeeman found" compressed this.

Historical note on Stern–Gerlach and spin (V, T13): the 1922 experiment was designed to test space quantization of orbital angular momentum in the Bohr–Sommerfeld model, with silver assumed to carry one unit of it; the two-beam result was read as confirming that. Silver's ground state in fact has zero orbital angular momentum and spin ½. Uhlenbeck and Goudsmit did not mention the result when they proposed spin in 1925. Fraser showed in 1927 that ground-state silver, hydrogen and sodium have no orbital moment, after which the splitting was attributed to spin; Phipps and Taylor repeated the experiment with hydrogen in 1927. Landé had argued in 1923, from the two beams, that silver must be in a doublet state with projections ±½.
- [T13] Friedrich et al., arXiv:2203.07833; Stanford Encyclopedia of Philosophy, "Experiment in Physics", appendix 5: https://plato.stanford.edu/archives/win2016/entries/physics-experiment/app5.html ; Friedrich, Isr. J. Chem. 2023, e202300047.

Corrections to statements (2026-11-11):
- Spinning-ball objection now states its assumption (classical electron radius).
- R4 now gives the strong-field energy formula and describes the pattern as a triplet of narrow doublets.
- R1 and R2 now state which quantum numbers are good, and that R2 is already the hyperfine Paschen–Back regime.
- P6 now mentions elliptical polarization at intermediate viewing angles.
- R5 now has a boundary (n above roughly 25 at 1 T).
- Added: regimes apply level by level; sodium's d levels are in the Paschen–Back regime above about 0.1 T. Before this, the model implied that the visible sodium lines are in the weak-field regime up to a few tesla, which holds for lines between s and p levels only.
