# Metadata: Dataset5_ceesat_processed.csv

Data file: [../Data/Dataset5_ceesat_processed.csv](../Data/Dataset5_ceesat_processed.csv)

**Unit and coverage:** 50 included syntheses; one processed appraisal row per synthesis.

**Dimensions:** 50 rows × 21 columns. CSV with comma delimiter, quoted text fields and UTF-8 encoding.

Processed numeric counterpart of Dataset4. The R Markdown preserves the four metadata fields, converts the 16 labelled ratings to numeric scores, sums raw_score, and checks all 1,050 cells against this file before analysis. It performs this reconstruction in memory and does not store a duplicate derived dataset. All 16 items enter raw_score; the proportional score is raw_score/64. The cited-versus-not-cited comparison uses a Welch two-sample t-test on log(proportional_score).

## Column definitions

Column names below match the supplied CSV exactly. Observed values describe this release, not necessarily every permitted category.

| Position | Column | Format / coding | Definition |
|---|---|---|---|
| 1 | `study_id` | Text identifier | Identifier of the included synthesis, usually first author and year. Use the recorded identifier for joins; do not infer publication year from it. |
| 2 | `study_type_title_abstract` | Systematic review; Meta-analysis; Systematic map | Synthesis type stated in the title or abstract and recorded during appraisal. |
| 3 | `doi` | Text | DOI of the included synthesis, as recorded. A URL or placeholder can occur when a DOI is unavailable; trim whitespace when matching. |
| 4 | `cited_in_policy` | 0 or 1 | Policy-citation indicator: 1 = cited in at least one retained policy record; 0 = not cited. |
| 5 | `CEESAT1.1` | Integer: 0, 1, 3, 4 | Are the elements of the review question clear? Red = 0; Amber = 1; Green = 3; Gold = 4. See Dataset4 metadata for the full rubric. |
| 6 | `CEESAT2.1` | Integer: 0, 1, 3, 4 | Is there an a-priori method/protocol document? Red = 0; Amber = 1; Green = 3; Gold = 4. See Dataset4 metadata for the full rubric. |
| 7 | `CEESAT3.1` | Integer: 0, 1, 3, 4 | Is the approach to searching clearly defined, systematic and transparent? Red = 0; Amber = 1; Green = 3; Gold = 4. See Dataset4 metadata for the full rubric. |
| 8 | `CEESAT3.2` | Integer: 0, 1, 3, 4 | Is the search comprehensive? Red = 0; Amber = 1; Green = 3; Gold = 4. See Dataset4 metadata for the full rubric. |
| 9 | `CEESAT4.1` | Integer: 0, 1, 3, 4 | Are eligibility criteria clearly defined? Red = 0; Amber = 1; Green = 3; Gold = 4. See Dataset4 metadata for the full rubric. |
| 10 | `CEESAT4.2` | Integer: 0, 1, 3, 4 | Are eligibility criteria consistently applied to all potentially relevant articles and studies found during the search? Red = 0; Amber = 1; Green = 3; Gold = 4. See Dataset4 metadata for the full rubric. |
| 11 | `CEESAT4.3` | Integer: 0, 1, 3, 4 | Are eligibility decisions transparently reported? Red = 0; Amber = 1; Green = 3; Gold = 4. See Dataset4 metadata for the full rubric. |
| 12 | `CEESAT5.1` | Integer: 0, 1, 3, 4 | Does the review critically appraise each study? Red = 0; Amber = 1; Green = 3; Gold = 4. See Dataset4 metadata for the full rubric. |
| 13 | `CEESAT5.2` | Integer: 0, 1, 3, 4 | During critical appraisal was an effort made to minimise subjectivity? Red = 0; Amber = 1; Green = 3; Gold = 4. See Dataset4 metadata for the full rubric. |
| 14 | `CEESAT6.1` | Integer: 0, 1, 3, 4 | Is the method of data extraction fully documented? Red = 0; Amber = 1; Green = 3; Gold = 4. See Dataset4 metadata for the full rubric. |
| 15 | `CEESAT6.2` | Integer: 0, 1, 3, 4 | Are the extracted data reported for each study? Red = 0; Amber = 1; Green = 3; Gold = 4. See Dataset4 metadata for the full rubric. |
| 16 | `CEESAT6.3` | Integer: 0, 1, 3, 4 | Were extracted data cross checked by more than one reviewer? Red = 0; Amber = 1; Green = 3; Gold = 4. See Dataset4 metadata for the full rubric. |
| 17 | `CEESAT7.1` | Integer: 0, 1, 3, 4 | Is the choice of synthesis approach appropriate? Red = 0; Amber = 1; Green = 3; Gold = 4. See Dataset4 metadata for the full rubric. |
| 18 | `CEESAT7.2` | Integer: 0, 1, 3, 4 | Is a statistical estimate of pooled effect (or similar) provided together with measure of variance and heterogeneity among studies? Red = 0; Amber = 1; Green = 3; Gold = 4. See Dataset4 metadata for the full rubric. |
| 19 | `CEESAT7.3` | Integer: 0, 1, 3, 4 | Is variability in the study findings investigated and discussed? Red = 0; Amber = 1; Green = 3; Gold = 4. See Dataset4 metadata for the full rubric. |
| 20 | `CEESAT8.1` | Integer: 0, 1, 3, 4 | Have the authors considered limitations of the synthesis? Red = 0; Amber = 1; Green = 3; Gold = 4. See Dataset4 metadata for the full rubric. |
| 21 | `raw_score` | Integer, theoretical range 0–64 | Sum of all 16 numeric item scores. The analysis divides this by 64 for every synthesis; it does not apply a synthesis-specific denominator. |

## Observed categorical values

- `study_type_title_abstract`: `Meta-analysis`; `Systematic map`; `Systematic review`.
- `cited_in_policy`: `0`; `1`.
- `CEESAT1.1`: `0`; `1`; `3`; `4`.
- `CEESAT2.1`: `0`; `3`; `4`.
- `CEESAT3.1`: `0`; `1`; `3`; `4`.
- `CEESAT3.2`: `0`; `1`; `3`; `4`.
- `CEESAT4.1`: `0`; `1`; `3`; `4`.
- `CEESAT4.2`: `0`; `1`; `3`; `4`.
- `CEESAT4.3`: `0`; `1`; `4`.
- `CEESAT5.1`: `0`; `1`; `4`.
- `CEESAT5.2`: `0`; `1`.
- `CEESAT6.1`: `0`; `1`; `3`; `4`.
- `CEESAT6.2`: `0`; `1`; `3`; `4`.
- `CEESAT6.3`: `0`; `3`; `4`.
- `CEESAT7.1`: `0`; `1`; `3`; `4`.
- `CEESAT7.2`: `0`; `1`; `3`; `4`.
- `CEESAT7.3`: `0`; `1`; `3`; `4`.
- `CEESAT8.1`: `0`; `1`; `3`; `4`.

## File identity

SHA-256: `5a91bd720145442a69f120408de31181009313aa49b022ec06d0c30831b0b327`

Metadata checked against this file on 14 October 2026.
