# Metadata: Dataset4_ceesat_assessments.csv

Data file: [../Data/Dataset4_ceesat_assessments.csv](../Data/Dataset4_ceesat_assessments.csv)

**Unit and coverage:** 50 included syntheses; one appraisal row per synthesis.

**Dimensions:** 50 rows × 44 columns. CSV with comma delimiter, quoted text fields and UTF-8 encoding.

CEESAT appraisal source with 16 item ratings and their justifications. Scoring is Red = 0, Amber = 1, Green = 3 and Gold = 4. The Total Score column is blank. Items 7.2 and 7.3 have meta-analysis-specific criteria in the rubric; the supplied dataset nevertheless retains a numeric rating for every synthesis, and the reported analysis sums all 16 items with maximum 64. Blank justifications mean no justification text recorded, not an unscored item.

## Column definitions

Column names below match the supplied CSV exactly. Observed values describe this release, not necessarily every permitted category.

| Position | Column | Format / coding | Definition |
|---|---|---|---|
| 1 | `Assessment Date` | MM/DD/YYYY | Recorded assessment date. |
| 2 | `Reviewer Name` | Initials | Initials of the assessor; AL = Anna Lenz. |
| 3 | `study_id` | Text identifier | Identifier of the included synthesis, usually first author and year. Use the recorded identifier for joins; do not infer publication year from it. |
| 4 | `study_type_title_abstract` | Systematic review; Meta-analysis; Systematic map | Synthesis type stated in the title or abstract and recorded during appraisal. |
| 5 | `quantitative` | yes/no | Whether the synthesis uses a quantitative approach. |
| 6 | `claim_used_meta_analysis` | yes/no | Whether the synthesis claims to use meta-analysis; one no value includes trailing whitespace. |
| 7 | `pooled_effect_meta_an` | yes/no | Whether the synthesis presents a pooled effect through meta-analysis. |
| 8 | `supplementary` | Yes/No | Whether supplementary material is available for the synthesis. |
| 9 | `protocol` | A priori; Not a priori; No | Availability and timing of a protocol for the assessed synthesis. |
| 10 | `doi` | Text | DOI of the included synthesis, as recorded. A URL or placeholder can occur when a DOI is unavailable; trim whitespace when matching. |
| 11 | `cited_in_policy` | 0 or 1 | Policy-citation indicator: 1 = cited in at least one retained policy record; 0 = not cited. |
| 12 | `1.1: Are the elements of the review question clear?` | Red (0); Amber (1); Green (3); Gold (4) | Are the elements of the review question clear? See the rating criteria below. |
| 13 | `1.1 Justification` | Free text | Evidence, page references and rationale for the CEESAT 1.1 rating. |
| 14 | `2.1: Is there an a-priori method/protocol document?` | Red (0); Amber (1); Green (3); Gold (4) | Is there an a-priori method/protocol document? See the rating criteria below. |
| 15 | `2.1 Justification` | Free text | Evidence, page references and rationale for the CEESAT 2.1 rating. |
| 16 | `3.1: Is the approach to searching clearly defined, systematic and transparent?` | Red (0); Amber (1); Green (3); Gold (4) | Is the approach to searching clearly defined, systematic and transparent? See the rating criteria below. |
| 17 | `3.1 Justification` | Free text | Evidence, page references and rationale for the CEESAT 3.1 rating. |
| 18 | `3.2: Is the search comprehensive?` | Red (0); Amber (1); Green (3); Gold (4) | Is the search comprehensive? See the rating criteria below. |
| 19 | `3.2Justification` | Free text | Evidence, page references and rationale for the CEESAT 3.2 rating. |
| 20 | `4.1: Are eligibility criteria clearly defined?` | Red (0); Amber (1); Green (3); Gold (4) | Are eligibility criteria clearly defined? See the rating criteria below. |
| 21 | `4.1 Justification` | Free text | Evidence, page references and rationale for the CEESAT 4.1 rating. |
| 22 | `4.2: Are eligibility criteria consistently applied to all potentially relevant articles?` | Red (0); Amber (1); Green (3); Gold (4) | Are eligibility criteria consistently applied to all potentially relevant articles and studies found during the search? See the rating criteria below. |
| 23 | `4.2 Justification` | Free text | Evidence, page references and rationale for the CEESAT 4.2 rating. |
| 24 | `4.3: Are eligibility decisions transparently reported?` | Red (0); Amber (1); Green (3); Gold (4) | Are eligibility decisions transparently reported? See the rating criteria below. |
| 25 | `4.3 Justification` | Free text | Evidence, page references and rationale for the CEESAT 4.3 rating. |
| 26 | `5.1: Does the review critically appraise each study?` | Red (0); Amber (1); Green (3); Gold (4) | Does the review critically appraise each study? See the rating criteria below. |
| 27 | `5.1 Justification` | Free text | Evidence, page references and rationale for the CEESAT 5.1 rating. |
| 28 | `5.2: During critical appraisal was an effort made to minimise subjectivity?` | Red (0); Amber (1); Green (3); Gold (4) | During critical appraisal was an effort made to minimise subjectivity? See the rating criteria below. |
| 29 | `5.2 Justification` | Free text | Evidence, page references and rationale for the CEESAT 5.2 rating. |
| 30 | `6.1: Is the method of data extraction fully documented?` | Red (0); Amber (1); Green (3); Gold (4) | Is the method of data extraction fully documented? See the rating criteria below. |
| 31 | `6.1 Justification` | Free text | Evidence, page references and rationale for the CEESAT 6.1 rating. |
| 32 | `6.2: Are the extracted data reported for each study?` | Red (0); Amber (1); Green (3); Gold (4) | Are the extracted data reported for each study? See the rating criteria below. |
| 33 | `6.2 Justification` | Free text | Evidence, page references and rationale for the CEESAT 6.2 rating. |
| 34 | `6.3: Were extracted data cross checked by more than one reviewer?` | Red (0); Amber (1); Green (3); Gold (4) | Were extracted data cross checked by more than one reviewer? See the rating criteria below. |
| 35 | `6.3 Justification` | Free text | Evidence, page references and rationale for the CEESAT 6.3 rating. |
| 36 | `7.1: Is the choice of synthesis approach appropriate?` | Red (0); Amber (1); Green (3); Gold (4) | Is the choice of synthesis approach appropriate? See the rating criteria below. |
| 37 | `7.1 Justification` | Free text | Evidence, page references and rationale for the CEESAT 7.1 rating. |
| 38 | `7.2: Is a statistical estimate of pooled effect provided with measure of variance and heterogeneity?` | Red (0); Amber (1); Green (3); Gold (4) | Is a statistical estimate of pooled effect (or similar) provided together with measure of variance and heterogeneity among studies? See the rating criteria below. |
| 39 | `7.2 Justification` | Free text | Evidence, page references and rationale for the CEESAT 7.2 rating. |
| 40 | `7.3: Is variability in the study findings investigated and discussed?` | Red (0); Amber (1); Green (3); Gold (4) | Is variability in the study findings investigated and discussed? See the rating criteria below. |
| 41 | `7.3 Justification` | Free text | Evidence, page references and rationale for the CEESAT 7.3 rating. |
| 42 | `8.1: Have the authors considered limitations of the synthesis?` | Red (0); Amber (1); Green (3); Gold (4) | Have the authors considered limitations of the synthesis? See the rating criteria below. |
| 43 | `8.1 Justification` | Free text | Evidence, page references and rationale for the CEESAT 8.1 rating. |
| 44 | `Total Score` | Blank in all 50 records | Unused source total field. The workflow computes raw_score from the 16 item ratings and validates it against Dataset5. |

## Observed categorical values

- `study_type_title_abstract`: `Meta-analysis`; `Systematic map`; `Systematic review`.
- `quantitative`: `no`; `yes`.
- `claim_used_meta_analysis`: `no`; `yes`.
- `pooled_effect_meta_an`: `no`; `yes`.
- `supplementary`: `No`; `Yes`.
- `protocol`: `A priori`; `No`; `Not a priori`.
- `cited_in_policy`: `0`; `1`.
- `1.1: Are the elements of the review question clear?`: `Amber (1)`; `Gold (4)`; `Green (3)`; `Red (0)`.
- `2.1: Is there an a-priori method/protocol document?`: `Gold (4)`; `Green (3)`; `Red (0)`.
- `3.1: Is the approach to searching clearly defined, systematic and transparent?`: `Amber (1)`; `Gold (4)`; `Green (3)`; `Red (0)`.
- `3.2: Is the search comprehensive?`: `Amber (1)`; `Gold (4)`; `Green (3)`; `Red (0)`.
- `4.1: Are eligibility criteria clearly defined?`: `Amber (1)`; `Gold (4)`; `Green (3)`; `Red (0)`.
- `4.2: Are eligibility criteria consistently applied to all potentially relevant articles?`: `Amber (1)`; `Gold (4)`; `Green (3)`; `Red (0)`.
- `4.3: Are eligibility decisions transparently reported?`: `Amber (1)`; `Gold (4)`; `Red (0)`.
- `5.1: Does the review critically appraise each study?`: `Amber (1)`; `Gold (4)`; `Red (0)`.
- `5.2: During critical appraisal was an effort made to minimise subjectivity?`: `Amber (1)`; `Red (0)`.
- `6.1: Is the method of data extraction fully documented?`: `Amber (1)`; `Gold (4)`; `Green (3)`; `Red (0)`.
- `6.2: Are the extracted data reported for each study?`: `Amber (1)`; `Gold (4)`; `Green (3)`; `Red (0)`.
- `6.3: Were extracted data cross checked by more than one reviewer?`: `Gold (4)`; `Green (3)`; `Red (0)`.
- `7.1: Is the choice of synthesis approach appropriate?`: `Amber (1)`; `Gold (4)`; `Green (3)`; `Red (0)`.
- `7.2: Is a statistical estimate of pooled effect provided with measure of variance and heterogeneity?`: `Amber (1)`; `Gold (4)`; `Green (3)`; `Red (0)`.
- `7.3: Is variability in the study findings investigated and discussed?`: `Amber (1)`; `Gold (4)`; `Green (3)`; `Red (0)`.
- `8.1: Have the authors considered limitations of the synthesis?`: `Amber (1)`; `Gold (4)`; `Green (3)`; `Red (0)`.

## CEESAT rating criteria

Criteria retained from the accompanying appraisal metadata. The numeric coding above governs score conversion.

### 1.1 — Are the elements of the review question clear?

Systematic map; review; meta-analysis.

| Rating | Criterion |
|---|---|
| Gold (4) | The review question or hypothesis is clearly stated and clearly defines key elements (e.g., PICO, PECO, PO, PIT, etc.) correctly, such as the subject or population of interest, the intervention or exposure type, the comparator, and valid measures of outcome. |
| Green (3) | The review question or hypothesis is clearly stated, and key elements are mentioned although not formally defined in terms of PICO, PECO, PO, PIT, etc. |
| Amber (1) | The question or hypothesis is stated in broad terms but key elements are unclear or poorly defined. |
| Red (0) | A question, hypothesis, or problem is not stated OR There is no stated objective to provide an answer to a question or test of a hypothesis OR The article does not contain an evidence synthesis (e.g., primary research or descriptive overview). |

### 2.1 — Is there an a-priori method/protocol document?

Systematic map; review; meta-analysis.

| Rating | Criterion |
|---|---|
| Gold (4) | The review cites a separate a-priori protocol or documented pre-defined method containing details of proposed conduct of all review and synthesis stages (e.g., question, search, eligibility screening, critical appraisal, data extraction, and synthesis) AND it is linked from the synthesis AND it was publicly accessible prior to the conduct of the review AND it was submitted to an independent body for peer review and publication. |
| Green (3) | The review cites a separate a-priori protocol or documented pre-defined method containing details of conduct of all review and synthesis stages AND it is linked from the synthesis AND it was publicly accessible prior to the conduct of the review. |
| Amber (1) | The review cites a separate a-priori protocol or documented pre-defined method, but this does not contain all details of conduct of all review and synthesis stages or was not publicly accessible prior to the conduct of the review OR the review includes a defined methods section (not a-priori) listing the synthesis stages conducted and providing sufficient detail to enable the method to be replicated (this standard is met only if all of 3.1, 4.1, 6.1 & 7.1 are rated green or above). |
| Red (0) | There is no protocol and the review methods are not clearly defined in the methods section of the review or there are no methods reported. |

### 3.1 — Is the approach to searching clearly defined, systematic and transparent?

Systematic map; review; meta-analysis.

| Rating | Criterion |
|---|---|
| Gold (4) | All search terms and search strings, with Boolean operators and wildcards, are clearly stated for each source so that the exact search is replicable by a third party AND there is information about the sources searched, together with dates of search and any limitations justified (e.g., languages, publication date, no grey literature searches). |
| Green (3) | All search terms and search strings, with Boolean operators and wildcards, are clearly stated for each major source so that the exact search is replicable by a third party, but search terms for minor sources, if used, may be missing AND there is information about the sources searched and search options selected, together with dates of search, but some limitations not justified. |
| Amber (1) | The search is described but not adequately to be fully replicable by a third party (e.g., specific terms or Boolean operators/wildcards not stated) OR there is information about the databases searched, but dates of search not given and no limitations justified. |
| Red (0) | No information regarding the search strategy (search terms and strings) used. |

### 3.2 — Is the search comprehensive?

Systematic map; review; meta-analysis.

| Rating | Criterion |
|---|---|
| Gold (4) | Sources of articles searched capture both conventionally published scientific literature and grey literature using a combination of databases, search engines, and specialist websites (may also be informed by stakeholders) or limitations are fully justified AND comprehensiveness of search is tested using independent samples of articles (test lists provided) to demonstrate adequate sensitivity. |
| Green (3) | Sources of articles searched are stated and capture both conventionally published scientific literature and grey literature using a combination of databases, search engines, and specialist websites (may also be informed by stakeholders) or limitations are fully justified. |
| Amber (1) | Resources used are stated but limited, without justification, to conventionally published scientific literature or just one or two sources. |
| Red (0) | Resources used not stated or search is not systematic (i.e., studies appear to have been selected). |

### 4.1 — Are eligibility criteria clearly defined?

Systematic map; review; meta-analysis.

| Rating | Criterion |
|---|---|
| Gold (4) | Eligibility criteria are precisely defined and expressly related to each key element of the question AND criteria are consistent between a-priori protocol and review or differences are fully explained. |
| Green (3) | Eligibility criteria are precisely defined and are expressly related to each key element of the question. |
| Amber (1) | The questions/scope/objectives of the review are stated such that the type of primary research to be included are broadly apparent, but the review does not explicitly identify criteria expressly related to each key element of the question OR some eligibility criteria are defined but either incomplete or not clearly related to a review question. |
| Red (0) | Eligibility criteria are not stated. |

### 4.2 — Are eligibility criteria consistently applied to all potentially relevant articles and studies found during the search?

Systematic map; review; meta-analysis.

| Rating | Criterion |
|---|---|
| Gold (4) | Eligibility criteria are independently applied by more than one reviewer to all of the screened articles/studies (with justified subsampling at title stage if needed) AND replicability of eligibility decisions was measured and reported AND all disagreements discussed to inform subsequent assessments. |
| Green (3) | Eligibility criteria are independently applied by more than one reviewer to a justified sample at title, abstract, and full text AND replicability of eligibility decisions was measured and reported AND all disagreements discussed to inform subsequent assessments. |
| Amber (1) | Eligibility criteria are applied by more than one reviewer to a sample at abstract and full text but reviewer independence is uncertain or absent AND replicability of decisions was examined (measure may not be reported) and disagreements discussed to inform subsequent assessments. |
| Red (0) | Number of reviewers not reported OR only one reviewer applied criteria at abstract or full text stage OR where two reviewers, consistency of decisions not tested/reported OR no eligibility criteria (see 4.1). |

### 4.3 — Are eligibility decisions transparently reported?

Systematic map; review; meta-analysis.

| Rating | Criterion |
|---|---|
| Gold (4) | The number of unique articles found during the searches (after removal of duplicates) is presented AND the number excluded at each stage is fully presented (e.g., flow diagram/table) AND reasons for exclusion of each full-text article/study are presented (e.g., appendix) AND a list of eligible (included) articles/studies is presented as a separate list or in tables. |
| Green (3) | The number of articles excluded at each stage is reported but some aspects missing (e.g., number of unique articles or unobtainable articles) AND reasons for exclusion of each full-text article/study are presented AND a list of eligible (included) articles/studies is presented as a separate list or in tables. |
| Amber (1) | The number of articles excluded during screening is reported (or inferable) but some aspects missing (e.g., number of unique articles, unobtainable articles, or reasons for exclusion at full text) AND a list of eligible (included) articles/studies is presented as a separate list or in tables. |
| Red (0) | Does not meet the amber standard (e.g., missing counts and/or missing reasons and/or no list of included studies). |

### 5.1 — Does the review critically appraise each study?

Systematic map; review; meta-analysis.

| Rating | Criterion |
|---|---|
| Gold (4) | An effort is made to identify all sources of bias relevant to individual included studies (threats to internal and external validity) AND each type of bias is assessed and explained individually for all included studies AND results are reported using an a-priori defined (in protocol) critical appraisal sheet. |
| Green (3) | An effort is made to identify all sources of bias relevant to individual included studies AND each type of bias or threat to validity is assessed individually for all included studies and reported on a critical appraisal sheet. |
| Amber (1) | Some characteristics of all included studies are explicitly identified as indicators of threats to validity but not reported for individual studies. |
| Red (0) | No critical appraisal conducted OR all critical appraisal criteria not applied to all individual included studies. |

### 5.2 — During critical appraisal was an effort made to minimise subjectivity?

Systematic map; review; meta-analysis.

| Rating | Criterion |
|---|---|
| Gold (4) | A critical appraisal process is predefined in a protocol AND at least two people independently critically appraised each study with disagreements and process of resolution reported. |
| Green (3) | A critical appraisal process is predefined in a protocol AND at least two people critically appraised each study but not independently (e.g., second person aware of first person‚Äôs decision). |
| Amber (1) | At least two people critically appraised each study but not independently OR a subset was appraised independently; disagreements/resolution might not be reported. |
| Red (0) | Only one person critically appraised each study or number not reported OR no critical appraisal conducted. |

### 6.1 — Is the method of data extraction fully documented?

Systematic map; review; meta-analysis.

| Rating | Criterion |
|---|---|
| Gold (4) | Authors state in an a-priori protocol the type of data to be extracted AND the methods by which data from each study will be extracted so that the process can be replicated, and confirm these methods were used or justify deviations. |
| Green (3) | Authors state in the methods (but not a-priori) the type of data to be extracted AND the methods by which data were extracted so that the process can be replicated. |
| Amber (1) | Authors state in the methods the type of data to be extracted AND, although a fully replicable methodology is not provided, the broad method can be inferred from reported results (e.g., an extraction table). |
| Red (0) | It is not clear what data were selected for extraction and/or no consistent approach to data extraction is reported. |

### 6.2 — Are the extracted data reported for each study?

Systematic map; review; meta-analysis.

| Rating | Criterion |
|---|---|
| Gold (4) | All data selected for extraction are provided in a table/spreadsheet as set out in the a-priori protocol, including data used in the synthesis from each study and meta-data AND any calculations/transformations (e.g., effect sizes, coding) are reported in full and replicable. |
| Green (3) | All data selected for extraction are provided in a post-hoc table/spreadsheet, including data used in the synthesis from each study and meta-data AND any calculations/transformations are reported in full and replicable. |
| Amber (1) | A table/spreadsheet is provided that includes some extracted metrics for some or all studies, but other data are missing and/or not all studies are represented. |
| Red (0) | Data extracted are not presented. |

### 6.3 — Were extracted data cross checked by more than one reviewer?

Systematic map; review; meta-analysis.

| Rating | Criterion |
|---|---|
| Gold (4) | Data were extracted from each study by at least two independent reviewers. |
| Green (3) | An explanation is provided of how a sample of extracted data was cross checked between two or more reviewers. |
| Amber (1) | A statement that cross-checking between two reviewers was carried out is provided but the explanation is unclear or incomplete. |
| Red (0) | No report of cross checking is provided. |

### 7.1 — Is the choice of synthesis approach appropriate?

Systematic map; review; meta-analysis.

| Rating | Criterion |
|---|---|
| Gold (4) | The choice of synthesis method (quantitative or narrative) is pre-specified, described in sufficient detail to be replicable, and justified (e.g., in the protocol) OR justified post hoc as a deviation from protocol, and, where meta-analysis is not employed when it may have been appropriate, a justification is given. |
| Green (3) | The choice of synthesis method is described in sufficient detail to be replicable and is (or appears) justified on the basis of included study characteristics AND, where meta-analysis is not employed when it may have been appropriate, a justification is given. |
| Amber (1) | No to either or both of the green criteria (e.g., no justification for not undertaking meta-analysis when it may have been appropriate) but none of the red criteria apply. |
| Red (0) | Fails green criteria AND either meta-analysis undertaken when inappropriate OR vote-counting relied on as indicator of impact/effectiveness OR narrative synthesis excludes studies or is unclear whether it includes all studies. |

### 7.2 — Is a statistical estimate of pooled effect (or similar) provided together with measure of variance and heterogeneity among studies?

Meta-analysis only.

| Rating | Criterion |
|---|---|
| Gold (4) | Statistical estimates of findings are presented using pre-defined meta-analysis methods that justify synthesis approach including study weighting and subgroup analysis AND consideration is given to study independence (e.g., sensitivity analysis) and bias (e.g., tests for publication bias). |
| Green (3) | Statistical estimates of findings are presented using meta-analysis methods that justify approach (e.g., study weighting and subgroup analysis) AND consideration is given to study independence and bias. |
| Amber (1) | Statistical estimates of findings are presented using a defined meta-analysis method but lack justification of approach and/or consideration of study independence and/or bias. |
| Red (0) | No statistical estimate provided because meta-analysis not conducted or not possible OR statistical estimate provided but the meta-analysis method is unclear. |

### 7.3 — Is variability in the study findings investigated and discussed?

Meta-analysis only.

| Rating | Criterion |
|---|---|
| Gold (4) | A strategy for investigating effect modifiers is provided in an a-priori protocol and followed (or variations explained) AND effect modifiers are investigated statistically through meta-analysis (or heterogeneity tested and reported as non-significant) AND results of critical appraisal (not just statistical weighting) are used in synthesis. |
| Green (3) | Effect modifiers are investigated statistically through meta-analysis (or heterogeneity tested and reported as non-significant) AND results of critical appraisal are used in synthesis. |
| Amber (1) | Effect modifiers investigated statistically through meta-analysis (or heterogeneity tested and reported as non-significant) but critical appraisal results are not used in synthesis OR effect modifiers are investigated descriptively through narrative synthesis. |
| Red (0) | Reasons for variability in study findings not investigated; effect modifiers not considered (including studies that use quantitative synthesis but fail to test for heterogeneity statistically). |

### 8.1 — Have the authors considered limitations of the synthesis?

Systematic map; review; meta-analysis.

| Rating | Criterion |
|---|---|
| Gold (4) | An explicit section is devoted to limitations, including limitations of the primary data (available evidence), possible sources of bias in the review process, conduct of the review process, and recommendations for future syntheses and primary research. |
| Green (3) | An explicit section or identifiable passage considers limitations of primary research/data and of conduct of the review process but does not consider all of: possible sources of bias in the review process, conduct of the review process, and recommendations for future syntheses and primary research. |
| Amber (1) | Some consideration of limitations is evident but not explicitly stated or not the focus of a specific section OR limitations of primary research included but not limitations of review conduct. |
| Red (0) | No evident consideration of limitations of primary data or review conduct. |

## File identity

SHA-256: `1e9e2e180733b38a1dd7833c7c663c263ea29eebf02d1e57e7a8922d319cf88a`

Metadata checked against this file on 14 October 2026.
