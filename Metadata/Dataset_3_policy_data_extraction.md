# Metadata: Dataset_3_policy_data_extraction.csv

Data file: [../Data/Dataset_3_policy_data_extraction.csv](../Data/Dataset_3_policy_data_extraction.csv)

**Unit and coverage:** 537 retained policy-citation records linked to 23 syntheses.

**Dimensions:** 537 rows × 18 columns. CSV with comma delimiter, quoted text fields and UTF-8 encoding.

Each row represents one retained citation record, not necessarily a globally unique policy document. The same source may cite more than one synthesis. Retained repeated records may represent chapters or compilations. All 537 rows contribute weight 1 to the policy analyses; no additional row deduplication is applied. The main alluvial plot shows the ten most frequent combinations (327 records); the supplementary plot shows all combinations. S10 uses 447 country-attributed records and reports 59 International, 28 EU and 3 Mixed records separately. Blank fields mean not recorded or unavailable. The embedded space in policy _level_category and the hyphen in full-text_url are part of the CSV headers.

## Column definitions

Column names below match the supplied CSV exactly. Observed values describe this release, not necessarily every permitted category.

| Position | Column | Format / coding | Definition |
|---|---|---|---|
| 1 | `study_id` | Text identifier | Identifier of the included synthesis, usually first author and year. Use the recorded identifier for joins; do not infer publication year from it. |
| 2 | `doi` | Text | DOI of the included synthesis, as recorded. A URL or placeholder can occur when a DOI is unavailable; trim whitespace when matching. |
| 3 | `study_title` | Text | Title of the cited synthesis. |
| 4 | `policy_title` | Text | Title of the citing policy document or source, as extracted. |
| 5 | `repeated_within_same_study_id` | Integer or blank | Number of repeated appearances recorded within the same synthesis in PlumX. Blank means no repeat count was entered, not a numerical zero. Do not use as a row weight. |
| 6 | `policy_year` | Integer, YYYY | Publication year of the policy source; the most recent year was recorded for revisions or multiple versions. |
| 7 | `policy_identifier_or_doi` | Text or blank | Identifier or DOI of the citing policy source. |
| 8 | `policy_author` | Text | Institution, organisation or author responsible for the policy source. |
| 9 | `policy_document_type` | Categorical | Government policy: Published by national or subnational governments (e.g, branches, departments, secretariats, etc.); Intergovernmental policy: Published by multinational organizations (e.g., UNEP, EU, WHO); NGO report: Published by non-profit, NGO organizations; Academic advisory: Published by academic expert panels. Can be a synthesis or technical advice; Regulatory Submission: Formal applications or impact statements submitted to authorities by proponents—independent from the government—seeking permits or approvals; Think Tank: Published by declared Think Tank organizations; Other document: Doesn’t match any above; Unclear: Not identifiable |
| 10 | `policy_country` | Text | Country or geographical scope of the source; the dataset also contains regions, international scope and Nairobi. For S10 only, the plotting code maps Nairobi to Kenya and UK constituent countries to the United Kingdom, and reports EU, International and Mixed separately. |
| 11 | `policy _level_category` | Categorical | International: Applies to multiple countries or globally; Regional: Applies to a multi-country region (e.g., European Union); National: Country-wide application; Subnational: Applies to a province, state, and/or municipal level; Mixed: More than one level; Other: Special categories (e.g., sector-specific); Unclear: Not clearly stated |
| 12 | `ecological_context` | Categorical | Terrestrial: Policy about land-based environments; Marine: Marine systems (e.g.  Pacific Ocean, bahias); Freshwater: Freshwater systems (e.g.,   rivers, lakes, ponds); Coastal: Coastal systems (e.g.  Estuaries, Urban coast); Urban: Built or human-modified environments (e.g. cities); Mixed: Covers more than one context; Other: Not clearly ecological or atypical settings (e.g. rural areas); Unclear: Not clearly specified (e.g. when the policy talked about computer tools used for any environment) |
| 13 | `policy_topic` | Categorical | Conservation: Biodiversity protection, habitat or species policies; Urban planning: Infrastructure or land use in urban areas; Sustainability: Meeting economic and social goals without compromising the environment, wildlife and natural resources; Health: Public health and well-being impacts of noise; Energy: Industry involved in producing and supplying fuel and power, including extraction, generation, transmission, and distribution (e.g. fossil fuels, nuclear, renewables, infrastructure like energy grids, pipelines); Mixed topic: Multiple focus areas (e.g. Energy + Conservation); Other topic: Topics like defence or education (e.g. mineral mining, animal welfare) |
| 14 | `policy_topic_notes` | Free text | Details supporting the assigned policy-topic category. |
| 15 | `policy_source` | URL / text | Source link used to locate the policy record, usually Overton. |
| 16 | `full_text_available` | Yes/No | Whether full text was available during extraction. |
| 17 | `full-text_url` | URL / text / blank | Link or availability note for the full policy text. |
| 18 | `attention_notes` | Free text | Extraction notes about the policy source and its citation or relevance. |

## Observed categorical values

- `repeated_within_same_study_id`: `2`; `3`; `4`; `5`.
- `policy_document_type`: `Academic advisory`; `Government policy`; `Intergovernmental policy`; `NGO report`; `Other document`; `Regulatory Submission`; `Think Tank`.
- `policy _level_category`: `International`; `National`; `Regional`; `Subnational`.
- `ecological_context`: `Coastal`; `Freshwater`; `Marine`; `Mixed`; `Other`; `Terrestrial`; `Unclear`; `Urban`.
- `policy_topic`: `Conservation`; `Energy`; `Health`; `Mixed topic`; `Other topic`; `Sustainability`; `Urban planning`.
- `full_text_available`: `No`; `Yes`.

## File identity

SHA-256: `184f8fe8de7ea95cf881cfc60a81e70e2489e2d68043e5c3f3a0dcef8a1b95e5`

Metadata checked against this file on 14 October 2026.
