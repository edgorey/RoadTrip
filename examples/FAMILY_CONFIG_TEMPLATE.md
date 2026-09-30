# Family Configuration Template

Copy and edit. Leave unknown fields blank rather than inventing them.

```yaml
family:
  language: en
  content_boundaries: []
  accessibility_needs: []
  players:
    - name: Player 1
      age_or_band: child | teen | adult
      role: player
      interests: []
      preferred_difficulty: easy | medium | hard | adaptive
      dislikes: []
journey:
  expected_duration_minutes: 15
  destination_or_theme: null
  planned_breaks: []
interface:
  channel: voice
  speaker_labels_available: false
session_defaults:
  mode: short
  scoring: true
  turn_model: rotation
  avoid_games: []
```

Only include what improves play. Avoid precise location, medical details, or other sensitive data without clear need and consent.