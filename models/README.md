# Models: index and conventions

Each physical situation discussed in this project has its own model document in `models/`. A model is the full list of objects, processes and regimes for that situation, written before answers are given, so that answers can be checked against it.

## Current models

| Document | Situation | Numbers verified | Statements verified |
|---|---|---|---|
| `models/zeeman-effect.md` | Atom emitting or absorbing light in a static magnetic field (normal and anomalous Zeeman effect, precession, Landé g-factor) | 2026-11-11 | 2026-11-11 |
| `models/atom-excitation-in-gas-discharge-lamp.md` | How atoms in a discharge lamp gain and lose energy (electron collisions, light, heat, the applied field) | 2026-11-11 | 2026-11-11 |

## Conventions

- One situation per document. If a question concerns a situation not listed above, create a new document and add it to the table.
- Each model has the sections: 1. Objects, 2. Processes, 3. Regimes, 4. Selection (for a stated set of conditions), 5. Known limits, 6. Verification of numbers, 7. Verification of statements.
- Processes and regimes carry short labels (P1, R2, E4, ...) so answers can refer to them.
- Before answering a question about a listed situation, read its model. If the answer needs an object, process or regime that is missing, add it to the model first.
- When a chat finds an error in a model, correct the document, record the change under "Corrections" in section 6 or 7, and say in the chat what changed.

## Status codes (sections 6 and 7)

- V: found in a cited source during a web lookup in the chat that wrote it.
- V (weak): found, but the source is weak (patent, leaflet, hobby site, encyclopedia mirror), or supports the item only by analogy, or its attribution is uncertain. Say which.
- C: calculated or derived from V items, with the formula or argument stated; arithmetic run in code, not done from memory.
- U: not verified (recalled, textbook knowledge not looked up, typical value, or a judgement).

## Section 6: verification of numbers

- A list of sources with URLs, then a table with one row per number: quantity, value, status, source or formula.
- Prefer primary references: CODATA/NIST for constants and atomic data, critically evaluated data compilations, peer-reviewed papers.
- When two sources disagree, record both values and the size of the disagreement.

## Section 7: verification of statements

- A list of sources with URLs, then a table with one row per qualitative claim in the model: the item label, the statement, status, source.
- Cover every process (that it occurs, under what condition, and any claim about its importance), every regime boundary, every "dominates" or "negligible" claim in the Selection, and the sub-models and pictures.
- Split a row when one part of a claim is supported and another is not (for example "occurs" is V but "is the most frequent" is U).
- While searching, look for processes the model lacks. Add any that are found and list them under "Corrections".
- A "negligible" claim needs either a number comparison (C) or a source (V); otherwise it is U.

## Using unverified items

- A number or statement marked U may be used in an answer only if the answer says it is unverified.
