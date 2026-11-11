# No-mistakes science explanations

A working setup for getting careful physics explanations from Claude. It has two parts:

- **Instructions** that make Claude build a written model of a physical situation before answering, and verify that model against sources.
- **Models**: one document per physical situation, each listing the objects, processes and regimes involved, with every number and statement marked as verified, calculated or unverified.

This repository is a snapshot of a Claude project of the same name, taken on 2026-11-11. The project is the working copy; this repository is updated when a new snapshot is pushed.

## Contents

| File | What it is |
|---|---|
| `INSTRUCTIONS.md` | The project instructions given to Claude |
| `models/README.md` | Index of models and the conventions for writing and verifying them |
| `models/zeeman-effect.md` | Atom emitting or absorbing light in a static magnetic field |
| `models/atom-excitation-in-gas-discharge-lamp.md` | How atoms in a discharge lamp gain and lose energy |
| `chats/zeeman-effect-and-electron-precession/` | The conversation the project grew from: transcript, 8 diagrams and 5 animations |

The chat transcript keeps answers as they were given, including statements that were corrected later. For corrected and source-checked content, use the models.

## How a model is organised

1. Objects: what is involved, with numbers and units.
2. Processes: what can happen to those objects, with conditions and sizes, including processes not needed for a given answer.
3. Regimes: the parameter values at which the dominant process changes.
4. Selection: which processes matter under a stated set of conditions, and why the others are neglected.
5. Known limits.
6. Verification of numbers.
7. Verification of statements.

## Status codes

| Code | Meaning |
|---|---|
| V | Found in a cited source during a web lookup |
| V (weak) | Found, but the source is weak, or supports the item only by analogy, or its attribution is uncertain |
| C | Calculated or derived from V items, with the formula or argument stated |
| U | Not verified |

## How to read the models

- "V" means a cited source agrees with the item. It does not mean the item is proven; a source can be wrong.
- Items marked U are mostly standard physics that was not looked up. Treat them as unconfirmed.
- Some sources were read as abstracts or excerpts, so the conditions under which their results hold are only partly recorded.
- The models were written by Claude (Anthropic's AI model) in conversation with the repository owner, and were not reviewed by a physicist.
