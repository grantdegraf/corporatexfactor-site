# Judgment Discovery

Outputs from the `unmonetized_judgment_detection` automated discovery module.

## Record Format

File naming: `discovery_<timestamp>.json`

## Detection Signals

- Large judgment amounts
- Fraud findings
- Offshore defendants
- Bankruptcy or insolvency
- Corporate dissolution
- Cross-border asset barriers

## Collectability Score (0–100)

| Score Range | Action |
|-------------|--------|
| 0–59 | Monitor only |
| 60–79 | Recovery analysis triggered |
| 80–100 | High priority — immediate gatekeeper assessment |

## Scoring Factors

- Defendant insolvency (+25)
- Offshore jurisdiction (+25)
- Fraud findings (+20)
- Lack of visible assets (+15)
- Corporate dissolution (+10)
- Cross-border barriers (+5)
