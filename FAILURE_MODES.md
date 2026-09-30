# Failure Modes and Fixes

## Observed in real play

| Failure | Harm | Working response |
|---|---|---|
| Correct answer misheard | Breaks trust and fairness | Confirm plausible/uncertain transcripts; allow correction |
| Wrong answer called correct | Undermines factual integrity | Validate before announcing or scoring |
| Point awarded prematurely | Corrupts state | Require speaker + answer + validation before one score update |
| Two people answer together | Attribution collapses | Do not score; name the active player and re-prompt |
| Player clarifies an answer | Host may score stale text | Define a lock point and accept earlier clarification |
| Host interrupts too quickly | Cuts off thought and speech | Allow a fuller response window |
| Repeated “another?” prompts | Kills momentum | Continue until stop, boundary, or transition |
| Playable format is not fun | Completeness replaces enjoyment | Switch immediately and record rejection |
| Generic riddles underperform | Quality and answers vary | Curate carefully; avoid scored ambiguity |

One reported example involved “Vasco da Gama” being treated as wrong. Another observed class was confidently confirming an incorrect answer. These are interaction failures, not merely content mistakes.

## Rejected or weak

The “advertise an everyday object in ten seconds” format was explicitly disliked and removed. Some riddles were unsuccessful. Keep them out of defaults unless redesigned and retested.

## Open problems

- Speaker recognition without platform diarization
- Background noise and competing navigation/audio
- Answer versus side-conversation detection
- Recovery after connection or voice-session interruption
- Real-time factual verification
- Durable cross-session memory
- Fair timing across children and adults
- Privacy of profiles and journey context
- Personalization without stereotypes or monotony
- Long-form narrative continuity

## Recovery hierarchy

Clarify cheaply → repeat or simplify once → void rather than fabricate → change difficulty/format → pause if unsuitable → log after play.