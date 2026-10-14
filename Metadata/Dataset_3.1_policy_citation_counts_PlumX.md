# Metadata: Dataset_3.1_policy_citation_counts_PlumX.csv

Data file: [../Data/Dataset_3.1_policy_citation_counts_PlumX.csv](../Data/Dataset_3.1_policy_citation_counts_PlumX.csv)

**Unit and coverage:** 50 synthesis rows plus one final Total summary row (51 physical data rows).

**Dimensions:** 51 rows × 14 columns. CSV with comma delimiter, quoted text fields and UTF-8 encoding.

Exclude the Total row (blank study_id) from study-level calculations; its values are summary totals. This is the PlumX policy-citation summary, not the Scopus bibliography. Counts can change between the initial capture and the extraction date. unique_policy_citations sums to 537 across the 50 synthesis rows and refers to deduplication within syntheses. Blanks and --/--- are missing values or placeholders, not zeros.

## Column definitions

Column names below match the supplied CSV exactly. Observed values describe this release, not necessarily every permitted category.

| Position | Column | Format / coding | Definition |
|---|---|---|---|
| 1 | `study_id` | Text identifier | Identifier of the included synthesis, usually first author and year. Use the recorded identifier for joins; do not infer publication year from it. |
| 2 | `title` | Text | Title of the synthesis. |
| 3 | `authors` | Text | Abbreviated author citation. |
| 4 | `year` | Integer, YYYY | Publication year in this dataset. |
| 5 | `language` | English; Spanish | Publication language. |
| 6 | `doi` | Text | DOI of the included synthesis, as recorded. A URL or placeholder can occur when a DOI is unavailable; trim whitespace when matching. |
| 7 | `plumx_url` | URL / placeholder | PlumX page for the synthesis; -- or --- indicate an unavailable identifier/link. |
| 8 | `policy_cited` | Yes; No; Total | Whether PlumX recorded policy citations. Total identifies the final summary row, which is not a synthesis. |
| 9 | `open_access` | Text; semicolon-separated labels | Open-access categories retained from the bibliometric record; blank means no label recorded. |
| 10 | `policy_number_July_9_2025` | Nonnegative integer | Policy-citation count captured on 9 July 2025, before the later extraction and within-synthesis deduplication. |
| 11 | `policy_extraction_date` | DD-Mon-YY or blank | Date on which the policy records for that synthesis were extracted. |
| 12 | `policy_number_in_date_of_extraction` | Nonnegative integer | Policy-citation count on the recorded extraction date, before within-synthesis deduplication. |
| 13 | `unique_policy_citations` | Nonnegative integer | Retained policy-citation count after deduplication within each synthesis. This is not a count of globally distinct policy documents across syntheses. |
| 14 | `Notes` | Free text | Extraction and deduplication notes supporting the counts. |

## Observed categorical values

- `language`: `English`; `Spanish`.
- `policy_cited`: `No`; `Total`; `Yes`.
- `policy_extraction_date`: `09-Jul-25`; `11-Jul-25`; `14-Jul-25`; `15-Jul-25`; `16-Jul-25`; `18-Jul-25`.

## File identity

SHA-256: `1079485f68a1554ea0ca3dca292242b34d83b9bd7431009d05622d8d57580c64`

Metadata checked against this file on 14 October 2026.
