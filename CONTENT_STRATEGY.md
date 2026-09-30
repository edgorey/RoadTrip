# Content Strategy

The host supports three content sources. It should use them in this order unless the players request something new.

1. **Curated bank:** reviewed questions, targets, clue sets, and prompts stored in `content/`.
2. **Curated pattern:** a tested format populated with a new subject that follows the same schema and validation rules.
3. **Live generation:** new material created during play for personalization, variety, or narrative continuity.

This is a hybrid system. The repository should hold enough authored material to start reliably, but it should not try to pre-write every possible session.

## Why keep curated content?

Curated items provide:

- dependable answers and accepted variants;
- predictable difficulty;
- protection against repeated or ambiguous questions;
- a stable baseline for comparing host behavior across tests;
- offline-readable material and easier review;
- explicit provenance and correction history.

## Why generate at runtime?

Live generation provides:

- topics tailored to the actual players;
- difficulty adjustment within a shared theme;
- fresh sessions after the bank has been exhausted;
- journey- and destination-aware fiction;
- follow-up questions based on what players say;
- effectively unlimited variety.

## Selection policy

Before presenting an item, the host should:

1. filter by game, language, age/difficulty, topic, and content boundary;
2. exclude IDs already used in the current session and recent history;
3. prefer curated items whose answer and wording are verified;
4. rotate topics rather than overfitting to one interest;
5. generate only when no suitable item remains or adaptation adds real value;
6. validate a generated scored item before asking it;
7. log disputed or weak generated items for review rather than silently adding them to the bank.

## Bank lifecycle

`draft → reviewed → play-tested → accepted`

An item may also become `revised`, `retired`, or `disputed`. Only reviewed, play-tested, or accepted items belong in default scored rotation. Starter items in this repository are marked **reviewed** but still need household-specific play-testing.

## Language strategy

Store a canonical meaning, answer, and aliases separately from spoken wording. A translated question is a variant, not a new fact. When translating live, preserve the accepted answer set and the configured regional language.

## Scope of v0.2

The starter library covers Quiz, Who Am I?, Guess the Animal, Would You Rather, and target ideas for 20 Questions. It intentionally does not attempt an exhaustive database. Narrative formats use authored premises and state structures rather than fixed scripts.