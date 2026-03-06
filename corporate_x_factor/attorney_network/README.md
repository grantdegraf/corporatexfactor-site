# Attorney Network

Stores attorney records for Corporate X-Factor recovery pipeline.

## Record Format

File naming: `attorney_<id>.json`

## Fields

- `attorney_name`
- `firm_name`
- `practice_area` (fraud recovery, insurance coverage disputes, professional liability, asset recovery, complex commercial enforcement)
- `relevant_cases`
- `location`
- `contact_information`

## Sources

- Law firm websites
- Court filings
- Legal directories
- Published cases involving fraud recovery or insurance litigation

## Pipeline Role

Attorneys in this network are matched to high-collectability-risk judgments via `attorney_network_matching` stage.
Recovery strategies emphasize **settlement leverage** over immediate litigation.
