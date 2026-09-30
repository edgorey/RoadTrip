# Customization Guide

## Adaptation order

1. Copy the configuration template and enter only useful player data.
2. Set language and regional variant.
3. Choose mode, duration, scoring, and turn model.
4. Add concise content boundaries.
5. Select two or three likely games.
6. Test on a low-stakes journey with passenger-managed setup.
7. Record what actually happened.

Customize age/difficulty, topic variety, competition/cooperation, vocabulary, timers, journey themes, boundaries, disliked formats, and score persistence.

## Adding a game

Use the module checklist in `GAME_CATALOG.md`. Mark it proposed, tested, successful, weak, or rejected. Define turn ownership and ambiguity behavior before competitive use.

## Changing a rule

Record the observation, old behavior, new rule, expected benefit, and regression risk in `LEARNING_LOG.md`. Update the relevant specification and `CHANGELOG.md`. A local fix should not silently change every game.

Keep the bootstrap prompt focused on invariants and details in repository files. Rewrite repeatedly missed rules as short observable trigger/outcome behaviors.