# Model: excitation of atoms in a gas-discharge lamp (electrons and light acting on a sodium atom)

Status: built 2026-11-11. Numbers verified 2026-11-11 (section 6). Statements verified 2026-11-11 (section 7). Status codes: V = found in a cited source; C = calculated or derived from V items, method given; U = not verified. Lamp operating values come from commercial low-pressure sodium lighting lamps and research discharges; small laboratory spectral lamps may differ. Update this document when a chat adds or corrects something.

Scope: a low-pressure metal-vapour discharge lamp of the kind used as a spectral source, and the ways an atom in it can gain or lose energy. Worked example: sodium.

## 1. Objects

**Sodium atom**
- 11 electrons; 10 in closed shells, one outer electron.
- Ground state 3s (²S1/2).
- First excited state 3p: 2.102 eV (²P1/2) and 2.104 eV (²P3/2) above ground; emits 589.6 and 589.0 nm (air); lifetime 16.2 to 16.3 ns.
- Higher levels, for example 4p at 3.753 eV (absorption from ground at 330.2/330.3 nm), 5p at 4.34 eV (285.3 nm), forming a series that converges to the ionization limit.
- Ionization energy from ground: 5.1391 eV (photon wavelength 241.3 nm).
- Ionization energy from 3p: 3.035 to 3.037 eV (408.3 to 408.6 nm).

**Free electrons in the discharge**
- Heated by the axial electric field; much hotter than the gas and the ions.
- Electron temperature of order 1 eV. A review of discharge lamps quotes measured values of 0.8 to 1.7 eV for a low-pressure discharge; from the excerpt read, it is not certain these refer to sodium-lamp conditions.
- The energy distribution has a tail to higher energies and can deviate from Maxwellian.

**Starter (buffer) gas**
- Commercial low-pressure sodium lamps: about 99% neon with about 1% argon, total pressure about 5 to 12 torr (roughly 7 to 16 mbar).
- Neon: lowest excited (metastable) states 16.62 and 16.72 eV; ionization 21.56 eV.
- Argon: lowest excited states about 11.5 to 11.8 eV; ionization 15.76 eV.

**Sodium vapour**
- Pressure about 0.4 Pa at the operating tube temperature of about 260 °C (533 K). The vapour-pressure curve gives 0.09 Pa at 500 K and 0.86 Pa at 550 K.
- The pressure is set by the coldest spot of the tube.

**Photons**
- Visible range ≈ 1.6 to 3.3 eV. A photon is absorbed whole or not at all in ordinary absorption.

**Circuit**
- Supply of hundreds to thousands of volts; ballast limits the current (U).
- Field in the tube is steady or oscillates at 50 Hz to radio frequency, far below the atomic resonance at 5.09 × 10¹⁴ Hz.

**Energy balance**
- In a commercial low-pressure sodium lamp about 30% of the input power leaves as visible light; the rest goes mainly to heat.

**Thermal energy**
- kT = 0.046 eV at 533 K; 0.172 eV at 2000 K (flame).

## 2. Processes

**Electron on atom**

| # | Process | Condition | Note |
|---|---|---|---|
| E1 | Elastic scattering | all electron energies | limits conductivity; heats the gas slightly. "Most frequent collision" is U |
| E2 | Excitation 3s → 3p | electron energy ≥ 2.10 eV (database threshold 2.099 eV) | electron keeps the remainder; no exact match needed |
| E3 | Excitation to higher levels | energy ≥ that level's threshold (3.75 eV for 4p) | "weaker than E2" is U |
| E4 | Ionization from ground | energy ≥ 5.14 eV | supplies new free electrons |
| E5 | Stepwise (multistep) ionization from excited atoms | energy ≥ 3.04 eV from 3p; less from higher levels | in Na–Ne positive columns, multistep ionization through many excited states is reported to be a dominant ionization route, already at low pressures and current densities |
| E6 | Superelastic collision (excited atom gives energy to the electron) | atom already excited | removes excitation without light; produces energetic electrons |
| E7 | Excitation or ionization of the buffer gas | ≥ 16.62 eV (Ne), ≥ about 11.5 eV (Ar) | carries the discharge at start-up, before the metal evaporates |
| E8 | Loss of electrons and ions | low pressure: ambipolar diffusion to the wall, recombination there; volume recombination matters at higher pressure | balances ionization in steady state |

**Photon on atom**

| # | Process | Condition | Note |
|---|---|---|---|
| L1 | Resonant absorption | photon energy matches an allowed transition within the line width | from ground: 589.0/589.6 nm, 330.2/330.3 nm, 285.3 nm and the rest of the series down to 241.3 nm; the D lines are the ground-state absorptions that fall in the visible |
| L2 | Photoionization | photon energy ≥ 5.139 eV from ground (≤ 241.3 nm); ≥ 3.04 eV from 3p (≤ 408 nm) | electron leaves with the excess as kinetic energy. Ground state: measured cross-section at threshold about 0.11 Mb, falling to a deep (Cooper) minimum just above threshold. From 3p: measured threshold values between about 2 and 8.5 Mb (experiments disagree) |
| L3 | Elastic (Rayleigh) scattering | off resonance | weak; photon keeps its energy (U) |
| L4 | Raman scattering | off resonance | weaker still; photon energy changes by a level difference (U) |
| L5 | Multiphoton excitation or ionization | very high intensity (lasers) | absent for ordinary lamps (U) |
| L6 | Stimulated emission | resonant photon meets an excited atom | small in a lamp because the excited fraction is small (U) |
| L7 | Compton scattering | photon energies of keV and above | outside the optical range (U) |

**Atom alone or atom on atom**

| # | Process | Condition | Note |
|---|---|---|---|
| A1 | Spontaneous emission | atom excited | 3p → 3s in about 16 ns; the source of the spectral lines |
| A2 | Radiation trapping | vapour optically thick at the resonance line | sodium vapour is opaque to its own 589 nm light; a photon is re-absorbed (L1) and re-emitted many times before escaping; causes self-absorption |
| A3 | Thermal excitation by atom–atom collisions | kT not far below the gap | Boltzmann fraction for 3p: 1.5 × 10⁻⁵ at 2000 K (flame); about 4 × 10⁻²⁰ at 533 K. A salted flame does emit the D lines (Zeeman's 1896 source) |
| A4 | Collisional quenching and pressure broadening | higher pressure | small in a low-pressure lamp (U) |
| A5 | Penning ionization by metastable neon | Ne metastable (16.62 eV) exceeds the ionization energy of Ar (15.76 eV) and of Na (5.14 eV) | Ne–Ar is a "Penning mixture": the small argon admixture lowers the striking voltage. Ionization of Na by the same route is energetically allowed; its importance in the running lamp is U |
| A6 | Depletion of ground-state sodium on the tube axis | higher discharge currents | sodium is ionized and driven outward faster than neutral atoms diffuse back; reported to have a decisive effect on discharge properties at higher currents and to be a major limit on lamp efficacy |

**Field on atom directly**

| # | Process | Condition | Note |
|---|---|---|---|
| F1 | Direct excitation by the supply field | would need frequency near 5 × 10¹⁴ Hz | absent: supply frequency is many orders of magnitude too low |
| F2 | Field ionization | classical threshold 1/(16 n*⁴) atomic units, about 5 × 10⁹ V/m for ground-state Na; the atomic unit of field is 5.1 × 10¹¹ V/m | absent: lamp fields are many orders of magnitude lower (U for the lamp field itself) |
| F3 | Acceleration (heating) of free electrons and ions | applied field ≠ 0 | the route by which electrical power enters the gas |

## 3. Regimes

**By electron energy (Na)**
- Below 2.10 eV: E1; also E5 and E6 if excited atoms are present.
- 2.10 to 5.14 eV: E2 and E3 added.
- Above 5.14 eV: E4 added.
- Above about 11.5 eV (Ar) and 16.62 eV (Ne): E7 added.

**By photon energy, atom in ground state**
- Matches a transition: L1.
- No match and below 5.139 eV: L3, L4 (weak); the atom is not excited.
- At or above 5.139 eV: L2 (weak near threshold because of the Cooper minimum).
- keV and above: L7 becomes relevant; inner-shell ionization also appears (not modelled here).

**By light intensity**
- Ordinary sources: one-photon processes.
- Intense lasers: L5 and L6 become important.

**By temperature**
- Around 500 K: A3 negligible (fraction of order 10⁻²⁰); excitation is by electrons.
- Around 2000 K and above (flames): A3 gives visible emission without a discharge (fraction of order 10⁻⁵).

**By lamp phase**
- Cold start: discharge runs in the neon–argon gas (E7, A5); reddish-pink colour.
- Warm (tube near 260 °C): sodium evaporates and its yellow lines take over. Explanation offered here: sodium's thresholds (2.10 and 5.14 eV) are far below the buffer's, so electrons lose energy to sodium first (supported only by analogy with noble-gas mixtures, where the species with the lower excitation energy is the one mostly excited).

**By discharge current**
- Low: sodium density roughly uniform across the tube.
- High: A6 depletes sodium on the axis; discharge properties and efficacy change.

**By gas pressure**
- Low: E8 is wall loss by ambipolar diffusion.
- Higher: volume recombination takes over; the column constricts (outside this model).

**By vapour density**
- Low: lines narrow.
- High: A2 and A4 broaden and self-reverse the resonance lines.

## 4. Selection for a warm low-pressure sodium lamp used as a spectral source

**Kept:** F3 → E2 → A1 as the main chain producing the D lines; E5 and E4 as the ionization that sustains the discharge, balanced by E8 at the wall; A2 as the main distortion of the line shape; A6 if the lamp is run at high current.

**Neglected, with reason:**
- F1, F2: frequency and field strength are many orders of magnitude from what is needed.
- A3: Boltzmann fraction at 533 K for a 2.10 eV gap is about 4 × 10⁻²⁰.
- L2: the lamp emits little light below 241 nm (U), and the cross-section is about 0.1 Mb or less.
- L3, L4, L5, L7: weak or outside the conditions of an ordinary lamp (U).
- E7 once warm: few electrons reach 16.6 eV while sodium is present to absorb their energy at 2.10 eV (U; qualitative argument).
- A5 for sodium: importance unknown (U).

## 5. Known limits of this model

- Qualitative for the discharge itself: no cross-section values, electron energy distribution, or rate equations.
- Describes the positive column. The cathode region, where fields and electron energies are higher, is not modelled.
- Sodium is the example. Other elements have different thresholds and level schemes; mercury and cadmium lamps involve metastable levels not covered here.
- High-pressure lamps, where A4 and continuum emission dominate, are outside the scope.
- Molecules (Na₂), negative ions and wall chemistry are left out.

## 6. Verification of numbers

Sources:
- [S1] CODATA 2022 recommended values, NIST: https://www.physics.nist.gov/cuu/pdf/wall_2022.pdf
- [S2] D. A. Steck, "Sodium D Line Data", rev. 2.3.4 (2025): https://steck.us/alkalidata/sodiumnumbers.pdf
- [S3] NIST Handbook of Basic Atomic Spectroscopic Data, Na I levels and lines: https://physics.nist.gov/PhysRefData/Handbook/Tables/sodiumtable5.htm and .../sodiumtable3.htm
- [S4] NIST ionization energies, as reproduced in the PDG table: https://ccwww.kek.jp/pdg/2024/reviews/rpp2024-rev-elements-electronic-struct.pdf
- [S5] Metastable energies table in Falcinelli et al., Atmosphere 6, 299 (2015): https://www.mdpi.com/2073-4433/6/3/299
- [S6] Lamptech, low-pressure sodium lamp pages: https://lamptech.co.uk/Documents/SO%20Vapour.htm ; .../SO%20Gas.htm ; .../SO%20Density.htm ; .../SO%20Introduction.htm
- [S7] US patent 4459510 (low-pressure sodium lamp example): https://image-ppubs.uspto.gov/dirsearch-public/print/downloadPdf/4459510
- [S8] Hudson, abstract (1963), Na absorption 1040–3500 Å: https://kb.osu.edu/items/6679450a-e731-5850-bf14-41a81abfcc46
- [S9] Gorczyca et al., Phys. Rev. A 109, 053102 (2024): https://strathprints.strath.ac.uk/89305/1/Gorczyca-et-al-Photoionization-of-atomic-sodium-near-threshold.pdf
- [S10] Amin et al., Eur. Phys. J. D 37, 23 (2006): https://link.springer.com/article/10.1140/epjd/e2005-00261-y ; and DOE report on Na(3p) photoionization: https://core.ac.uk/download/216530209.pdf
- [S11] US patent 10262852 (excited argon energies): https://image-ppubs.uspto.gov/dirsearch-public/print/downloadPdf/10262852
- [S12] IAEA collision database, e + Na 3s → 3p: https://amdis.iaea.org/db/collisiondb/datasets/107534
- [S13] Lister, Lawler, Lapatovich, Godyak, "The physics of discharge lamps" (excerpt): https://www.researchgate.net/publication/243478934_The_physics_of_discharge_lamps

| Quantity | Value | Status | Source or formula |
|---|---|---|---|
| 3p levels | 16956.172, 16973.368 cm⁻¹ → 2.1023, 2.1044 eV | V, C | S3; ÷ 8065.544 cm⁻¹/eV |
| D wavelengths (air) | 589.59, 589.00 nm | V | S3 |
| 3p lifetime | 16.30, 16.25 ns | V | S2 |
| 4p levels | 30266.99, 30272.58 cm⁻¹ → 3.753 eV; lines 330.24, 330.30 nm | V, C | S3 |
| 5p level | 35040–35043 cm⁻¹ → 4.34 eV; 285.3 nm | V, C | S3 |
| Na ionization | 41449.451 cm⁻¹ = 5.1391 eV; 241.26 nm | V, C | S2, S3, S4; λ = 1/wavenumber |
| Ionization from 3p | 3.035–3.037 eV; 408.3–408.6 nm | C | limit minus 3p levels |
| E2 threshold | 2.099 eV | V | S12 |
| Ne metastables | 16.619, 16.715 eV | V | S5 |
| Ne ionization | 21.5645 eV | V | S4 |
| Ar ionization | 15.7596 eV | V | S4 |
| Ar lowest excited states | 11.5–11.8 eV | V (weak source) | S11 |
| Fill gas | 99% Ne, 1% Ar; 5.5 torr (730 Pa) in one lamp; 8–12 torr in low-wattage lamps | V | S7, S6 |
| Tube temperature | about 260 °C | V | S6, S7 |
| Na vapour pressure | 0.4 Pa at 260 °C | V | S6, S7; S2 formula gives 0.42 Pa |
| Vapour pressure at 500 K, 550 K | 0.09, 0.86 Pa | C | S2 formula: log₁₀P(torr) = 7.585 − 5377/T |
| Electron temperature | 0.8–1.7 eV | V (weak: attribution to sodium conditions uncertain) | S13 |
| Visible output | about 30% of input power | V | S6 |
| Resonance frequency | 5.09 × 10¹⁴ Hz | C | c / 589 nm |
| kT | 0.0459 eV (533 K), 0.172 eV (2000 K) | C | k from S1 |
| Boltzmann fraction 3p/3s | 1.5 × 10⁻⁵ (2000 K); 4 × 10⁻²⁰ (533 K) | C | 3·exp(−2.104 eV/kT) |
| Ground-state photoionization at threshold | 0.112 ± 0.010 Mb | V | S8; S9 argues older measured magnitudes away from the minimum are too high |
| Cooper minimum just above threshold | minimum ≈ 1.4 × 10⁻⁵ Mb (calculated) | V | S9 |
| 3p photoionization at threshold | 2.2–3.7 Mb; 8.5 Mb | V | S10 (experiments disagree) |
| Field for over-the-barrier ionization | ≈ 5 × 10⁹ V/m | C | 1/(16 n*⁴) a.u. (formula V, T11) with n* = 1.63 from the binding energy |
| Atomic unit of field | 5.14 × 10¹¹ V/m | V | T11 excerpt (5.14 × 10⁹ V/cm) |
| Supply voltage, lamp field strength | — | U | not looked up |
| Lamp emission below 241 nm is small | — | U | not looked up |

Corrections to numbers (2026-11-11):
- Buffer gas pressure "of order 1 to 10 mbar" → about 7 to 16 mbar (5 to 12 torr), 99% Ne with 1% Ar.
- Operating temperature "500 to 550 K" → about 533 K (260 °C); vapour pressure pinned to 0.4 Pa.
- Field-ionization scale "order 10¹⁰ V/m" → about 5 × 10⁹ V/m, with the formula stated.
- Boltzmann fraction at lamp temperature now includes the statistical weight: 4 × 10⁻²⁰ at 533 K.
- Mean electron energy "one to a few eV" → electron temperature of order 1 eV, with the reported range and its caveat.

## 7. Verification of statements

Sources for statements:
- [T1] Han, Schwinn, Gallagher, Phys. Rev. A 42, 1245 (1990): https://link.aps.org/doi/10.1103/PhysRevA.42.1245
- [T2] Electron-impact ionization of Na, Phys. Rev. A 51 (1995), record: https://www.osti.gov/biblio/6584750
- [T3] Multistep ionization in Na–Ne and Ne positive columns, J. Appl. Phys. 49, 3814 (1978), abstract: https://scilit.com/publications/1ed1678e9d3c826f682f308330131b42
- [T4] van Tongeren & Heuvelmans, positive column of Na–Ar and Na–Ne–Ar discharges, abstract: https://scilit.com/publications/4274c4c1c510cbe3104387f0b9c5a95b
- [T5] Positive-column descriptions: US patent 5420481 (background section): https://image-ppubs.uspto.gov/dirsearch-public/print/downloadPdf/5420481 ; arXiv:2306.02370 ; Phys. Rev. E 97, 013201 (accepted manuscript): https://link.aps.org/accepted/10.1103/PhysRevE.97.013201
- [T6] Kinetic positive-column simulations including superelastic collisions: https://w3.pppl.gov/~ikaganov/PPPL2005/SpecialIssue/TPS1018.pdf ; superelastic scattering from sodium is the subject of papers cited in T1's reference list
- [T7] Start-up sequence: https://www.electrical4u.com/low-pressure-sodium-vapour-lamp/ ; https://physicsshop.blogs.bucknell.edu/tag/sodium/
- [T8] arXiv:physics/0504021 (noble-gas mixtures: lower excitation energy species is mostly excited)
- [T9] Zeeman, Astrophys. J. 5, 332 (1897): https://articles.adsabs.harvard.edu/pdf/1897ApJ.....5..332Z
- [T10] IET review "Low-pressure sodium discharge lamps" (abstract): https://digital-library.theiet.org/doi/10.1049/ip-a-1.1981.0065
- [T11] Field ionization threshold: https://discovery-pp.ucl.ac.uk/id/eprint/10067244/1/PhysRevA.99.013421.pdf ; atomic field unit: https://repository.royalholloway.ac.uk/items/dd3f0569-7400-8a4e-9728-2e4c8cd473a7/8/PhysRevA.58.3884.pdf
- [S2], [S3], [S6], [S8], [S9], [S12], [S13] as in section 6.

| Item | Statement | Status | Source |
|---|---|---|---|
| Electrons | electron temperature far above gas and ion temperature; heated by the axial field | V | T5 |
| Electrons | distribution can be non-Maxwellian | V | T4 |
| E1 | elastic collisions limit conductivity | V | NIST fluorescent-lamp paper found in the same search (Hg–Ar); by analogy |
| E1 | most frequent collision type | U | no cross-sections compared |
| E2 | electron-impact 3s → 3p occurs from threshold near 2.1 eV | V | S12, T1 |
| E2 | electron keeps the remaining energy | U | textbook (inelastic collision), not looked up |
| E3 | excitation to higher levels exists | V | S12 (database covers levels up to 5s) |
| E3 | weaker than E2 | U | values not compared |
| E4 | electron-impact ionization of Na | V | T2 |
| E5 | multistep ionization via excited states is a dominant route in Na–Ne columns | V | T3 |
| E6 | superelastic collisions occur and are included in column models | V | T6 |
| E7 | discharge starts in the neon–argon gas, reddish at first | V | T7 |
| E8 | low pressure: loss by ambipolar diffusion to walls with recombination there; volume recombination at higher pressure | V | T5 |
| L1 | series of absorption lines from the ground state up to the limit at 241 nm | V | S3, S8 |
| L2 | photoionization above the limit; Cooper minimum | V | S8, S9 |
| L3–L7 | existence and relative weakness of these processes | U | textbook, not looked up |
| Photons | absorbed whole or not at all | U | textbook, not looked up |
| A1 | emission lifetime | V | S2 |
| A2 | sodium vapour opaque to its own resonance light | V | S6 |
| A3 | Boltzmann estimate | C | section 6 |
| A3 | salted flame emits D lines | V | T9 |
| A4 | small at low pressure | U | not looked up |
| A5 | Ne–Ar Penning mixture lowers striking voltage | V | S6 |
| A5 | Penning ionization of Na in the running lamp | U | energetically allowed; importance not found |
| A6 | sodium depletion decisive at higher currents; limits efficacy | V | T4, S13, S6 (ionic pumping) |
| F1 | supply frequency far from resonance | C | 50 Hz–MHz against 5 × 10¹⁴ Hz |
| F2 | classical threshold formula 1/(16 n*⁴) | V | T11 |
| F2 | lamp fields far below threshold | U | lamp field not looked up |
| F3 | field heats electrons | V | T5, T6 |
| Lamp phase | sodium takes over when the tube reaches about 260 °C | V | T7, S6 |
| Lamp phase | reason: lower thresholds of sodium | V (weak: analogy) | T8 |
| Output | emission is essentially the 589.0/589.6 nm lines | V | T10 |
| Pressure setting | vapour pressure fixed by the coldest spot | V | S6 |

Corrections to statements (2026-11-11):
- E5 upgraded: from "needs a meaningful excited population" to a dominant ionization route in Na–Ne columns; section 4 now keeps E5 with E4.
- A6 (sodium depletion on the axis) added; it was missing.
- E8 rewritten as wall loss by ambipolar diffusion at low pressure, with the higher-pressure alternative named.
- A5 rewritten: the verified role of Penning ionization is Ne* + Ar at start-up; the Na route is marked U.
- Regime list by electron energy corrected (E5, E6 below 2.10 eV); regimes by current and by pressure added.
- Limit added: the model describes the positive column, not the cathode region.
- Added: Cooper minimum, measured photoionization cross-sections, 5p line, argon excited states, energy balance.
