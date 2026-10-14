# Metadata: Dataset1_map_data_extraction.csv

Data file: [../Data/Dataset1_map_data_extraction.csv](../Data/Dataset1_map_data_extraction.csv)

**Unit and coverage:** 50 included syntheses; one row per synthesis.

**Dimensions:** 50 rows × 28 columns. CSV with comma delimiter, quoted text fields and UTF-8 encoding.

Comma-separated fields allow multiple categories. Blank fields mean not recorded or unavailable, not zero. Preserve source spelling and free-text notes. The last column has no header; it is documented below rather than silently renamed. Counts in multicategory plots can exceed 50.

## Column definitions

Column names below match the supplied CSV exactly. Observed values describe this release, not necessarily every permitted category.

| Position | Column | Format / coding | Definition |
|---|---|---|---|
| 1 | `extractor_initials` | AA, BB, etc. | Initials of the data extractor, first name and last name initials. |
| 2 | `study_id` | Text identifier | Identifier of the included synthesis, usually first author and year. Use the recorded identifier for joins; do not infer publication year from it. |
| 3 | `doi` | Text | DOI of the included synthesis, as recorded. A URL or placeholder can occur when a DOI is unavailable; trim whitespace when matching. |
| 4 | `year` | Integer, YYYY | Publication year in this dataset. |
| 5 | `review_type` | Categorical; comma-separated when multiple apply | Systematic review: Structured evidence synthesis using a search strategy (keywords + databases), predefined criteria to identify and analyze studies, which often answer a question or make a recommendation about what they are reviewing.; Systematic map: Provides a structured overview of existing evidence to identify research clusters, gaps, and trends without quantitative synthesis; Meta-analysis: Statistical combination of effect sizes from multiple studies using statistical techniques to estimate overall trends and variation |
| 6 | `quantitative` | yes/no | Whether the synthesis includes a quantitative approach; this does not necessarily mean it reports a pooled meta-analytic effect. |
| 7 | `ceesat` | yes/no | Original extraction flag for CEESAT assessment. This is not the analysis inclusion filter: Datasets 4 and 5 contain all 50 appraisals. |
| 8 | `cited_policy` | yes/no | Whether the synthesis received policy citations. |
| 9 | `study_designs` | Categorical; comma-separated when multiple apply | Experimental: Includes manipulations with controlled conditions; Observational: Observes variables in natural settings without manipulation; Mixed: Includes both experimental and observational studies; Other: Includes theory or modelling, not empirical studies; Unclear: No information reported on study design |
| 10 | `n_studies` | Text / count | Number of primary studies concerning noise reported by the synthesis; preserve qualified or nonnumeric entries. |
| 11 | `ecosystem_type` | Categorical; comma-separated when multiple apply | Terrestrial: Land-based ecosystems, excluding urban areas, but can include rural and natural area.s; Freshwater: Lakes, rivers, wetlands, estuaries; Marine: Saltwater environments like the ocean; Urban: Human-dominated environments, cities, or industrial zones; Other: Ecosystems that don’t fit above (e.g., caves, polar); Unclear: Ecosystem type is not explicitly mentioned |
| 12 | `noise_frequencies` | Categorical; comma-separated when multiple apply | Infrasonic: Below 20 Hz; Audible: Between 20 Hz and 20 kHz; Ultrasonic: Above 20 kHz; Mixed: Covers more than one range; Other: Unclassified or ambiguous range; Unclear: Not specified in the review |
| 13 | `specific_noises` | yes/no/unclear | “Yes” for explicitly specified focus (e.g., sonar, aircraft, boat, road traffic) |
| 14 | `noise_source` | Categorical; comma-separated when multiple apply | Transportation: Traffic, car, aircraft, roadway, marine vessels (includes cruise ships, drillships, freight/passenger vessels), recreational boats; Energy: Air gun, Water gun, seismic survey, drilling, turbines, wind turbines, wind farm, gas compressor, hydroelectric turbines, energy infrastructure; Construction: Pile driving, dredging, construction, pier noise, road construction; Industrial: Mining, industry, industrial, compressor, generator; Urban: Whole urban soundscape/background noise; Recreational: Music, tourism, Fireworks, Human voices; UAV/UAS: Drones, Unmanned Aerial Vehicles (UAVs) or Unmanned Aircraft Systems (UASs); Synthetic: White noise, brown noise, synthetic tones, linear sweeps, sine waves, and playback tones; Military: Missile launch, military sonar, sonic boom, military activity; Unclear: Not specified |
| 15 | `scope_single_species` | yes/no/unclear | “Yes” for explicitly specified focus on a single species (e.g., polar bear) |
| 16 | `scope_singlehigher_taxa` | yes/no/unclear | “Yes” for explicitly specified focus on a higher taxonomic group (e.g., birds, insects, marine mammals). Use “No” If review is on animals in general. |
| 17 | `scope_taxon` | Latin names (e.g., Chordata, Arthropoda, Aves) | Use the high-level taxa of the included species, if specified, or derive from the list of species, if available. |
| 18 | `taxa_notes` | text | Any observations about the taxonomic scope |
| 19 | `n_species` | Text / count | Number of species reported by the synthesis, where available; preserve qualified or nonnumeric entries. |
| 20 | `sp_source` | yes/no/unclear | “Yes,”  if explicitly mentioned that focus is on wild or free-living animals only. If not, code as  “No” |
| 21 | `sp_source_category` | Categorical; comma-separated when multiple apply | Wild: Free-living animals in natural/semi-natural environments; Domestic: Pets, livestock, and working animals; Laboratory: Animals bred for use in lab-controlled settings (e.g. rodent models for health research); Mixed: Combination of multiple categories above; Other: Captive but not domestic or laboratory (e.g., zoo animals); Unclear: Not clearly reported |
| 22 | `outcome_category` | Categorical; comma-separated when multiple apply | Behavioural: Observable behaviours (e.g., vigilance, foraging); Physiological: Biological responses (e.g., hormones, immune system); Ecological: Population- or community-level impacts (e.g. spatial distribution, abundance, occupancy); Reproductive: Fertility, mating, or offspring effects; Communication: Vocal/acoustic signalling changes (e.g. higher frequencies or temporal changes in calls); Other: Does not fit any above; Unclear: Not enough information |
| 23 | `outcome_notes` | Free text | Details supporting the recorded outcome categories. |
| 24 | `effects` | Text; mostly blank | Extracted direction-of-effect notes; not a complete effect-size dataset and not used to estimate pooled effects. |
| 25 | `contextual_modifiers` | yes/no/unclear | Does the review assess how noise interacts with other factors? “Yes,” if explicitly stated that interactions are considered in the review (e.g., a meta-analysis has moderators for other variable types such as time of day, light, predators, animal sex, location or climate type). If not, code as “No.” |
| 26 | `contextual_modifiers_name` | Exact words/terms of the author in the review used to describe considered interactions or moderators | Name the additional potentially interacting factor considered in the review |
| 27 | `general_notes` | free text | Any observations about the syntheses |
| 28 | *(empty header)* | Free text | Unnamed final column (column 28) containing additional extraction notes. R readr assigns it ...28. It is retained unchanged and is not used in figures. |

## Observed categorical values

- `review_type`: `Meta-analysis`; `Systematic map`; `Systematic review`.
- `quantitative`: `no`; `yes`.
- `ceesat`: `no`; `yes`.
- `cited_policy`: `no`; `yes`.
- `study_designs`: `Experimental`; `Mixed`; `Observational`; `Unclear`.
- `ecosystem_type`: `Freshwater`; `Freshwater, Marine`; `Marine`; `Terrestrial`; `Terrestrial, Marine`; `Terrestrial, Marine, Freshwater`; `Terrestrial, Marine, Freshwater, Urban`; `Urban`.
- `noise_frequencies`: `Audible (20 HzÐ20 kHz),`; `Mixed`; `Unclear`.
- `specific_noises`: `No`; `Unclear`; `Yes`.
- `scope_single_species`: `No`; `Yes`.
- `scope_singlehigher_taxa`: `No`; `Yes`.
- `sp_source`: `No`; `Unclear`; `Yes`.
- `sp_source_category`: `Mixed`; `Unclear`; `Wild`.
- `effects`: `Positive, Negative`.
- `contextual_modifiers`: `No`; `Yes`.

## File identity

SHA-256: `39c7d928022d8c8b952819ba18ee68bf39c76a8a565e1450d21ed2b9425e9dfa`

Metadata checked against this file on 14 October 2026.
