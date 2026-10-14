# Noise impacts on wildlife: synthesis data and analysis

Data, coding metadata, analysis code and figures supporting:

**Lenz, A., Mizuno, A., Lundgren, E., Morrison, K., Ortega, S., Lagisz, M., & Nakagawa, S. (2026). A systematic map of syntheses on anthropogenic noise impacts on wildlife: evidence gaps, policy attention, and quality appraisal.** *Environmental Science and Pollution Research*. [Article DOI: 10.1007/s11356-026-38268-9](https://doi.org/10.1007/s11356-026-38268-9).

We mapped 50 syntheses, appraised all 50 using CEESAT, analysed bibliometric records for 47, and classified 537 retained policy-citation records linked to 23 syntheses. Policy-record counts are not counts of globally distinct policy documents.

## Contents

| Location | Contents |
|---|---|
| [Data](Data/) | Six final CSV datasets and the accompanying Scopus BibTeX file |
| [Metadata](Metadata/) | One metadata document per data file, including column definitions, coding and file checksums |
| [R/Wildlife_syntheses_figures_.Rmd](R/Wildlife_syntheses_figures_.Rmd) | Complete analysis and figure workflow, with processing and plotting helpers included |
| [Analysis.html](Analysis.html) | Self-contained report with code, analyses and figures; download and open in a browser |
| [Figures/Final_figures](Figures/Final_figures/) | Final main-figure PNG/TIFF exports; Figure 2's original artwork is not distributed |
| [Figures/Supplementary](Figures/Supplementary/) | Final supplementary Figures S1–S11 |
| [Metadata/software](Metadata/software/) | R/package versions and package citations |

Working notes, draft manuscripts, archives, intermediate outputs and local artwork sources are not part of this release. The protocol is available on OSF rather than duplicated here.

## Datasets and metadata

| Dataset | Coverage | Metadata |
|---|---|---|
| [Dataset 1](Data/Dataset1_map_data_extraction.csv) | Systematic-map extraction: 50 syntheses | [Definitions](Metadata/Dataset1_map_data_extraction.md) |
| [Dataset 2](Data/Dataset2_bibliometric_data.csv) | Bibliometric data: 47 Scopus-indexed syntheses | [Definitions](Metadata/Dataset2_bibliometric_data.md) |
| [Dataset 3](Data/Dataset_3_policy_data_extraction.csv) | 537 retained policy-citation records | [Definitions](Metadata/Dataset_3_policy_data_extraction.md) |
| [Dataset 3.1](Data/Dataset_3.1_policy_citation_counts_PlumX.csv) | PlumX counts for 50 syntheses plus one summary row | [Definitions](Metadata/Dataset_3.1_policy_citation_counts_PlumX.md) |
| [Dataset 4](Data/Dataset4_ceesat_assessments.csv) | CEESAT ratings and supporting justifications for 50 syntheses | [Definitions and rating criteria](Metadata/Dataset4_ceesat_assessments.md) |
| [Dataset 5](Data/Dataset5_ceesat_processed.csv) | Numeric CEESAT scores for the same 50 syntheses | [Definitions](Metadata/Dataset5_ceesat_processed.md) |
| [Bibliography](Data/bibliometric.bib) | BibTeX records for the 47 bibliometric syntheses | [Definitions](Metadata/bibliometric.md) |

The metadata lists the actual CSV headers, including retained spaces and the unnamed notes column in Dataset 1. Blank cells are not automatically zero. Dataset 3.1's final `Total` row is not a synthesis and must be excluded from study-level calculations. Dataset 3 retains repeated records that can represent chapter or compilation citations; the analysis does not remove additional rows.

## View the report offline

Download [Analysis.html](Analysis.html) using GitHub's **Download raw file** button, then open the downloaded file in a browser. Its figures, styles and scripts are embedded; no R installation, accompanying files or internet connection is needed to view it. External reference links require internet access. GitHub displays HTML source rather than running the report on the file page.

## Reproduce the analysis

The report was tested with **R 4.5.1**. Package versions appear at the end of the HTML report and in [Metadata/software/Rpackages_versions.csv](Metadata/software/Rpackages_versions.csv). RStudio is optional; R Markdown rendering requires Pandoc (included with RStudio).

1. Clone or download this repository and open `Umbrella_review_noise.Rproj`, or set the working directory to the repository root.
2. Install the packages listed in the R Markdown setup chunk if needed. The workflow checks dependencies but never installs them automatically.
3. Render from the repository root:

```r
rmarkdown::render(
  "R/Wildlife_syntheses_figures_.Rmd",
  output_file = "Analysis.html",
  output_dir = getwd()
)
```

Rendering validates Dataset 5 against a reconstruction from Dataset 4, then reads the final Dataset 5. The reconstruction uses Red = 0, Amber = 1, Green = 3 and Gold = 4, and checks all 1,050 cells. It stays in memory: no duplicate dataset is saved, and the source datasets are not overwritten.

By default, rendering updates only the HTML report and leaves the final figure files intact. To regenerate figure exports explicitly:

```r
rmarkdown::render(
  "R/Wildlife_syntheses_figures_.Rmd",
  output_file = "Analysis.html",
  output_dir = getwd(),
  params = list(export_figures = TRUE)
)
```

This exports main Figures 1, 3, 4 and 5 as 600-dpi PNG/TIFF and PDF, a code-generated base for Figure 2, and supplementary Figures S3–S11 as PNG/PDF. The submitted Figure 2 was composed manually using the author's original animal artwork, which is not included. Figures S1 and S2 are manually prepared diagrams. S4 uses an embedded publication word-cloud raster with an input-frequency check; if the keyword data change, the workflow stops until the embedded cloud and its frequency table are updated. Fonts and rendering engines can affect exact pixel appearance on another computer.

## Protocol and citation

- [Original OSF protocol project, deposited 30 May 2025](https://osf.io/dmjc4/) — DOI [10.17605/OSF.IO/DMJC4](https://doi.org/10.17605/OSF.IO/DMJC4).
- [Formal OSF registration of the same protocol, created later for preservation](https://osf.io/7bx6g/) — DOI [10.17605/OSF.IO/7BX6G](https://doi.org/10.17605/OSF.IO/7BX6G).

Please cite the article above when using these materials. [CITATION.cff](CITATION.cff) provides the citation in a machine-readable format. The [MIT licence](LICENSE) applies to repository software; bibliographic source content retains its original rights.

Contact: Anna Lenz — [lenzrive@ualberta.ca](mailto:lenzrive@ualberta.ca).
