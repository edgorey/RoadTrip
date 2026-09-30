# Content Schema

## Common fields

```yaml
id: QUIZ-GEO-001
game: quiz
status: reviewed
difficulty: easy
age_band: 8+
topics: [geography]
language: en
prompt: What is the capital of Portugal?
answer: Lisbon
accepted_answers: [Lisboa]
explanation: Lisbon is Portugal's capital and largest city.
source_note: Stable general knowledge; verify if edited.
last_reviewed: 2026-09-30
```

Required fields are `id`, `game`, `status`, `difficulty`, `prompt` or game-specific content, and the answer when the game is factual.

## Difficulty

- **easy:** broad recognition or one-step recall
- **medium:** more specific recall or simple reasoning
- **hard:** specialist recall, multi-step reasoning, or explanation

Difficulty is relative to the configured player. The label is a starting point, not a judgment about the person.

## Status values

- `draft`: not ready for play
- `reviewed`: checked by an editor
- `play-tested`: used successfully at least once
- `accepted`: repeatedly successful and reliable
- `revised`: changed and awaiting another test
- `disputed`: answer or wording challenged
- `retired`: excluded from selection

## Game-specific fields

- Quiz: `answer`, `accepted_answers`, `explanation`
- Who Am I / Animal: ordered `clues`, `answer`, aliases
- Would You Rather: `option_a`, `option_b`, optional follow-up
- 20 Questions: `target`, `category`, and stable classification facts
- Narrative: premise, truth/fiction boundary, scenes, clues, and state transitions

## IDs

Use stable IDs so history and corrections survive wording changes:

`GAME-TOPIC-NNN`, for example `QUIZ-SPACE-004` or `ANIMAL-OCEAN-002`.

Never reuse a retired ID for unrelated content.