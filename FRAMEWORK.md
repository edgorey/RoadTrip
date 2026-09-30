# Reusable Framework

## Goals

- Voice-native: all essential actions work without a screen.
- Low-friction: begin quickly and avoid repeated menus.
- Adaptive: vary difficulty, subject, pace, and format by player.
- Resilient: uncertainty triggers clarification, not confident scoring.
- Interruptible: changing direction or stopping is always safe.
- Host-like: keep momentum without seeking permission after every turn.
- Transparent: explain rulings and corrections briefly.
- Playful rather than bureaucratic.

## Conceptual architecture

1. **Context:** available time, journey phase, language, noise, themes, constraints.
2. **Player model:** names, ages, interests, accessibility, difficulty, teams, boundaries.
3. **Game Director:** selects activities and controls pacing.
4. **Game module:** defines rules, content, end conditions, and recovery.
5. **State manager:** tracks turn, score, attempts, history, and narrative state.
6. **Voice policy:** handles transcription doubt, overlap, interruption, and confirmation.
7. **Host response:** concise spoken output ending with a clear expected action.

These are logical roles, not necessarily separate software. The original model performed them conversationally.

## Host loop

1. Read mode, game, active player, and pending item.
2. Interpret speech as answer, pass, command, correction, side speech, or unclear input.
3. Resolve ambiguity before changing state.
4. Apply the game transition.
5. Announce only what players need.
6. Continue unless stopped, paused, or naturally finished.

## Conversational controls

Treat “Short Mode,” “Road Trip Mode,” “different game,” “harder,” “easier,” “repeat,” “that’s not what I said,” “score?”, “pause,” “stop,” and “this isn’t working” as high-priority controls. Briefly acknowledge, change state, and resume.

## Content principles

Use the selection order in `CONTENT_STRATEGY.md`: curated bank, curated pattern, then live generation. Load the relevant `content/` bank, track stable item IDs, and never promote generated material without review.

Personalize without narrowing everything to known interests. Adapt difficulty per player. Avoid recent repetition. Prefer defensible answers when scoring. Separate fiction from fact. Keep explanations short unless asked. Let boredom and rejection change the experience immediately.

## Lifecycle

**Configure → choose mode → establish players/teams → play → adapt → close → capture learning.**