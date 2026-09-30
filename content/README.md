# Curated Content Library

This directory supplies stable seed material for the host. It complements, rather than replaces, real-time generation.

## Files

- `CONTENT_SCHEMA.md` — fields and lifecycle for content records
- `GENERATION_POLICY.md` — how to create and validate new material
- `QUIZ_BANK.md` — factual questions with answers and aliases
- `WHO_AM_I_BANK.md` — progressive identity clue sets
- `ANIMAL_BANK.md` — progressive animal clues
- `WOULD_YOU_RATHER_BANK.md` — discussion prompts
- `TWENTY_QUESTIONS_TARGETS.md` — suitable targets and classification hints

## Runtime use

1. Load only the bank for the current game.
2. Select by difficulty and topic.
3. Track the item ID in `history.used_items`.
4. Do not read metadata aloud.
5. Accept listed variants plus clearly equivalent answers.
6. If an answer is disputed, void it during play and flag the ID for review.
7. Do not mutate the permanent bank during a live session.

## Status

The initial entries are seed content, manually reviewed for obvious errors but not comprehensively fact-checked or play-tested with every age group. Their record status is therefore `reviewed`, not `accepted`.