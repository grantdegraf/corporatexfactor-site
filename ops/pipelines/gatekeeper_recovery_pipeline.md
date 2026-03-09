# Gatekeeper Recovery Pipeline — Corporate X-Factor

## Recovery Model

**Case Structure:**
- Plaintiff holds default judgment against foreign corporation (e.g., Chinese-registered entity)
- Defendant has no reachable assets — direct enforcement not viable
- Recovery opportunity: gatekeeper liability

**Gatekeeper Types:**
| Gatekeeper | Liability Theory |
|------------|------------------|
| Auditors | Failed to detect/report fraud in financial statements |
| Insurance carriers | Coverage obligation; bad faith denial |
| Professional advisors | Negligence, breach of fiduciary duty |
| Banks / financial institutions | Facilitated fraud; failed KYC/AML |
| Underwriters | Due diligence failure |
| Escrow agents / fiduciaries | Breach of fiduciary duty |

**Recovery Strategy:** Settlement leverage — identify gatekeeper exposure, negotiate settlement. Litigation is last resort.

---

## Pipeline Modules

### attorney_specialist_scraper
Sources: law firm websites, legal directories, litigation rankings, case law references
Target: attorneys with auditor liability, professional negligence, securities fraud, insurance recovery, third-party recovery experience
Output: `corporate_x_factor/attorney_network/attorney_<id>.json`

### practice_area_classifier
Classifies each discovered attorney by gatekeeper type:
- auditors, insurers, professional advisors, financial institutions, fiduciaries, offshore structures

### reputation_scoring_engine
Scores each attorney 0–100 based on:
- Practice area match to gatekeeper recovery model
- Notable cases involving gatekeeper/third-party liability
- Firm tier (AmLaw ranking, Chambers, Benchmark Litigation)
- Recent recovery results
- Government background (DOJ/SEC)

### gatekeeper_liability_filter
Filters to attorneys with fit_score ≥ 75 and at least one gatekeeper focus area matching the case model

### attorney_shortlist_generator
Ranks filtered attorneys by fit_score descending
Outputs shortlist to `ops/pipelines/attorney_shortlist_<date>.json`
Target: 20–40 qualified attorneys per run

---

## Outreach Queue

Location: `corporate_x_factor/outreach_queue/gatekeeper_recovery_attorneys/`  
Template: `outreach_templates/attorney_intro_letters/gatekeeper_recovery/template_v1.md`  
Status: Drafts prepared for operator approval — **do not send automatically**

---

## Current Run (2026-03-09)

- Attorneys identified: **20**
- Avg fit score: **86.1**
- Top fit score: **93** (John Rizio-Hamilton, Bernstein Litowitz)
- Outreach drafts prepared: **6** (top-fit attorneys)
- Pipeline stage reached: `attorney_network_matching` → `plaintiff_outreach` (pending operator approval)
