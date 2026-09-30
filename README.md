# Voice-Native Family Host

A portable knowledge base for turning conversational AI into a voice-first family game host, especially on car journeys where screens are undesirable.

The experiment began with a practical question: **can ChatGPT through CarPlay entertain a child and accompanying adults on a six-hour drive?** It evolved from generating trivia into designing an adaptive host that manages players, turns, difficulty, pacing, scoring, game changes, and stories through conversation.

The central idea is **generative UX**: the model does not merely generate content; it generates and reshapes the interaction. “Short Mode,” “harder,” “different game,” and “this isn’t working” act like interface controls.

## Quick start

1. Copy this repository into a ChatGPT project or otherwise provide its Markdown files.
2. Copy [examples/FAMILY_CONFIG_TEMPLATE.md](examples/FAMILY_CONFIG_TEMPLATE.md) and create your own private configuration. Do not commit personal family details to a public repository.
3. Give ChatGPT [prompts/BOOTSTRAP_PROMPT.md](prompts/BOOTSTRAP_PROMPT.md) with the repository. The host will prefer reviewed material in [content/](content/) and generate new items when needed.
4. Say **“Start Short Mode”** or **“Start Road Trip Mode.”**
5. After play, record evidence with [playtesting/SESSION_TEMPLATE.md](playtesting/SESSION_TEMPLATE.md) and update [LEARNING_LOG.md](LEARNING_LOG.md).

## Repository map

- `FRAMEWORK.md` — reusable architecture and principles
- `VOICE_UX.md` — voice-specific interaction rules
- `STATE_AND_SCORING.md` — turns, validation, and scoring
- `FAILURE_MODES.md` — observed failures and mitigations
- `modes/` — Short and Road Trip behavior
- `games/` — formats and narrative play
- `content/` — curated question, clue, target, and discussion banks
- `CONTENT_STRATEGY.md` — curated versus generated content policy
- `prompts/` — portable bootstrap and customization instructions
- `examples/` — privacy-safe blank configuration
- `playtesting/` — repeatable session record
- `LEARNING_LOG.md` and `CHANGELOG.md` — evidence and evolution

## Evidence labels

- **Observed:** happened in real car play or was explicitly reported.
- **Working rule:** a behavioral fix adopted from observation.
- **Proposed:** designed but not established as successful.
- **Open:** unresolved and worth testing.

Do not silently promote proposed behavior to observed success. Record the supporting session.

## Safety

The driver must not configure or troubleshoot while driving. A passenger should manage changes, or setup should happen before departure. The host must never demand visual attention or physical interaction. This is an experiment, not a safety-certified in-car product.

## Thesis

The product is not the chatbot or question catalogue. It is the **behavior designed around the model**: rules, memory, state, context, recovery, pacing, and conversational adaptability.