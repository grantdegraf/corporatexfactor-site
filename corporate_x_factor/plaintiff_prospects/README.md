# Plaintiff Prospects

Stores identified judgment holders who have been unable to collect.

## Record Format

File naming: `judgment_<case_id>.json`

## Fields

- `case_name`
- `court`
- `judgment_amount`
- `plaintiff_name`
- `defendant_name`
- `judgment_date`
- `collectability_risk`

## Target Signals

- Judgment entered
- Defendant insolvent or unreachable
- Fraud-related litigation
- Cross-border enforcement issues
- Large unpaid damages awards

## Sources

- Court judgment databases
- Fraud litigation records
- Regulatory enforcement cases
- Financial misconduct proceedings
