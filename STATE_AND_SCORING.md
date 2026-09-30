# State, Turns, and Scoring

## Minimum state

```yaml
session: {mode: short, language: en, scoring: true, game: quiz, phase: active}
players:
  - {name: Player 1, difficulty: adaptive, score: 0}
turn: {active_player: Player 1, attempt: 1, max_attempts: 2}
pending: {prompt: "...", accepted_answers: ["..."], ruling_locked: false}
history: {used_items: [], rejected_games: []}
```

The host should be able to state current player, game, and score when asked.

## Scored-question protocol

1. Name the active player and ask one question.
2. Wait for a complete answer.
3. Confirm unclear transcription or identity without scoring.
4. Validate intended answer and reasonable equivalents.
5. If correct, confirm and award exactly one point, then advance.
6. If wrong, say so explicitly and pass to the next eligible player.
7. “I don’t know” passes immediately without shame.
8. After the second miss/pass, reveal the answer briefly.
9. Lock the ruling, then move on.

## Invariants

- Never award before understanding speaker and answer.
- Never say “correct” without validation.
- One answer yields at most one point unless designed otherwise.
- Correct host mistakes without player penalty.
- Void unresolved ambiguity; do not guess.
- Apply state changes once.

## Turn models

- **Rotation:** fixed order; best noisy-environment default.
- **Pass-and-steal:** active player, then one named player.
- **Teams:** one named spokesperson.
- **Open buzz-in:** only with reliable attribution or name-first answers.
- **Cooperative:** group seeks a shared result.

Prefer rotation or cooperation in the car.

## Disputes

Pause transition, restate what was heard, accept clarification, and re-evaluate. If a fact dispute cannot be checked, void or flag the item. Momentum matters more than winning an argument.