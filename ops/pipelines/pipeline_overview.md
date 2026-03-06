# Corporate X-Factor — Pipeline Overview

## Full Pipeline Flow

```
judgment_discovery
  → collectability_analysis
  → gatekeeper_exposure_assessment
  → attorney_network_matching
  → plaintiff_outreach
  → recovery_strategy
```

## Pipeline 1: Attorney Network Development

**Purpose:** Identify attorneys capable of executing recovery strategies for gatekeeper liability and insurance exposure.

**Target expertise:**
- Fraud recovery
- Insurance coverage disputes
- Professional liability
- Asset recovery
- Complex commercial enforcement

**Data location:** `corporate_x_factor/attorney_network/attorney_<id>.json`

## Pipeline 2: Plaintiff / Judgment Holder Identification

**Purpose:** Identify plaintiffs who obtained judgments but cannot collect.

**Target signals:**
- Judgment entered
- Defendant insolvent or unreachable
- Fraud-related litigation
- Cross-border enforcement issues
- Large unpaid damages awards

**Data location:** `corporate_x_factor/plaintiff_prospects/judgment_<case_id>.json`

## System Rules

1. Corporate X-Factor must remain **separate** from CourtReady
2. Both pipelines must remain active
3. Discovery prioritizes high-value and high-risk judgments
4. Recovery strategies emphasize **settlement leverage** over immediate litigation
