# Metadata: Dataset2_bibliometric_data.csv

Data file: [../Data/Dataset2_bibliometric_data.csv](../Data/Dataset2_bibliometric_data.csv)

**Unit and coverage:** 47 Scopus-indexed syntheses; one row per bibliographic record.

**Dimensions:** 47 rows × 25 columns. CSV with comma delimiter, quoted text fields and UTF-8 encoding.

Scopus bibliographic data used for authorship, geography, keywords and academic-citation figures. Citation counts are the study snapshot, not live counts. Match records to other datasets by DOI; there is no study_id column. The accompanying bibliometric.bib covers the same 47 syntheses but has a different field structure. A bibliometric year can differ from the year used in a publisher-formatted citation; do not regenerate study IDs from this field.

## Column definitions

Column names below match the supplied CSV exactly. Observed values describe this release, not necessarily every permitted category.

| Position | Column | Format / coding | Definition |
|---|---|---|---|
| 1 | `authors` | Free text | Abbreviated author initials and surnames separated by semicolons (e.g., “R., Williams, Rob; K.D., Cox, Kieran D.”). |
| 2 | `author_full_names` | Free text | Full names of all authors with unique Scopus Author IDs in parentheses, separated by semicolons. |
| 3 | `author_id` | Text / Numeric identifiers | List of Scopus Author IDs corresponding to each author, separated by semicolons. |
| 4 | `title` | Text | Full title of the publication. |
| 5 | `year` | Integer (YYYY) | Year the publication was released. |
| 6 | `cited_by` | Integer | Number of citations the article has received (from Scopus). |
| 7 | `doi` | Text | Digital Object Identifier (DOI) for the article. |
| 8 | `link` | URL | Direct Scopus URL to the publication record. |
| 9 | `affiliations` | Free text | Institutional affiliations and countries of all authors, separated by semicolons. |
| 10 | `authors_with_affiliations` | Free text / structured | Combined field listing each author followed by their institutional affiliation and country. |
| 11 | `abstract` | Free text | Abstract text of the article summarizing the main findings. |
| 12 | `author_keywords` | Semicolon-separated terms | Keywords in the supplied author-keyword field. The analysis combines this field with index_keywords and applies the documented synonym dictionary; occurrences can repeat across fields. |
| 13 | `index_keywords` | Free text | Indexed keywords from Scopus (e.g., MeSH or subject tags). |
| 14 | `funding_text` | Free text | Narrative funding acknowledgment text included in the article. |
| 15 | `funding` | yes/no | Whether a funding acknowledgement is recorded. |
| 16 | `references` | Free text | List of references cited by the article (semicolon-separated). |
| 17 | `editors` | Empty / NA | Editor names; this column is empty for all records. |
| 18 | `publisher` | Text | Name of the publishing organization (e.g., Elsevier Ltd). |
| 19 | `PubMed ID` | Text identifier / blank | PubMed identifier where available; preserve as an identifier, not a measurement. |
| 20 | `language` | Text (single category) | Language of publication (all entries are “English”). |
| 21 | `document_type` | Categorical | Type of publication (e.g., Article, Review, Editorial) |
| 22 | `publication_stage` | Categorical | Stage of publication (e.g., Final, Pre-print) |
| 23 | `open_access` | Semicolon-separated category labels | Scopus open-access classifications; this is not a yes/no field. |
| 24 | `source` | Scopus | Name of the database |
| 25 | `eid` | Text | Electronic identifier assigned by Scopus |

## Observed categorical values

- `funding`: `no`; `yes`.
- `language`: `English`.
- `document_type`: `Article`; `Conference paper`; `Review`.
- `publication_stage`: `Final`.
- `source`: `Scopus`.

## File identity

SHA-256: `f564af87e8596f97e9779a08efb086c1adab6a914c3bc9d8df2c5111b66a43b4`

Metadata checked against this file on 14 October 2026.
