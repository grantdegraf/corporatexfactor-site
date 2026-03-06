# Unmonetized Judgment Detection Module

## Overview

Automated discovery module that monitors newly entered judgments and evaluates collectability risk.

## Algorithm

1. **Monitor** — Watch court databases for newly entered judgments
2. **Evaluate** — Score each judgment against risk indicators
3. **Route** — Judgments scoring ≥ 60 proceed to recovery analysis

## Scoring Formula

| Signal | Weight |
|--------|--------|
| Defendant insolvency | +25 |
| Offshore jurisdiction | +25 |
| Fraud findings | +20 |
| Lack of visible assets | +15 |
| Corporate dissolution | +10 |
| Cross-border asset barrier | +5 |

**Score range: 0–100. Threshold for recovery analysis: ≥ 60.**

## Output

Stored in `corporate_x_factor/judgment_discovery/discovery_<timestamp>.json`

## Example Record

```json
{
  "case_name": "Plaintiff Corp v. Offshore Holdings Ltd",
  "judgment_amount": 25000000,
  "collectability_score": 82,
  "risk_signals": [
    "defendant offshore",
    "fraud finding",
    "assets not located"
  ],
  "detected_at": "2026-03-06T09:00:00Z",
  "routed_to_recovery": true
}
```

## System Rules

- Prioritize high-value judgments (> $1M) and high-risk signals
- Recovery strategy must emphasize settlement leverage
- Do NOT reuse CourtReady discovery logic
