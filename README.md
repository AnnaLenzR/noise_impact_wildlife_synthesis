# A systematic map of syntheses on anthropogenic noise impacts on wildlife: evidence gaps, policy attention, and quality appraisal

This repository contains the full datasets, coding metadata to interpret the datasets, and analysis and figure code supporting Lenz et al. (2026).

The pre-registered protocol is available on OSF ([Lenz et al. 2025](https://osf.io/dmjc4/)). It describes our aims to systematically map reviews of the behavioural, physiological and ecological impacts of anthropogenic noise on wildlife across taxa and noise sources, examine research trends and collaboration networks, evaluate methodological quality using CEESAT, and assess policy relevance. We originally deposited the protocol as an OSF project on 30 May 2025 and created a [formal registration of the same protocol](https://osf.io/7bx6g/) on 9 October 2026 for preservation.

## GitHub contents

The table below lists the folder names and their contents.

| Folder | Contents |
|---|---|
| [Data](Data/) | Seven final dataset files: six CSV files and one BibTeX (.bib) file. |
| [Metadata](Metadata/) | Seven CSV codebooks describing the variables and definitions used to code and interpret each dataset. |
| [R](R/) | The R Markdown file that reproduces the main and supplementary figures and analyses of the published article. |
| [Figures](Figures/) | Two subfolders: [Final_figures](Figures/Final_figures/) contains the exported main figures, including the final Figure 2; [Supplementary](Figures/Supplementary/) contains the exported supplementary figures. |

## Dataset names, content and metadata

These datasets are located in Data. The table gives each file’s full name, its content and the name of its corresponding metadata file. Descriptions follow the dataset list in Online Resource 1.

| Dataset file name | Content | Metadata file name |
|---|---|---|
| [Dataset1_map_data_extraction.csv](Data/Dataset1_map_data_extraction.csv) | Map data extraction. | [Dataset1_map_data_extraction_codebook.csv](Metadata/Dataset1_map_data_extraction_codebook.csv) |
| [Dataset2_bibliometric_data.csv](Data/Dataset2_bibliometric_data.csv) | Bibliometric data extracted from Scopus. | [Dataset2_bibliometric_data_codebook.csv](Metadata/Dataset2_bibliometric_data_codebook.csv) |
| [bibliometric.bib](Data/bibliometric.bib) | The same bibliometric dataset as Dataset 2, in BibTeX format. Used by the bibliometrix route for the chord diagram; the default route uses Dataset 2 affiliation data. | [bibliometric_codebook.csv](Metadata/bibliometric_codebook.csv) |
| [Dataset_3_policy_data_extraction.csv](Data/Dataset_3_policy_data_extraction.csv) | Policy-document data extraction. | [Dataset_3_policy_data_extraction_codebook.csv](Metadata/Dataset_3_policy_data_extraction_codebook.csv) |
| [Dataset_3.1_policy_citation_counts_PlumX.csv](Data/Dataset_3.1_policy_citation_counts_PlumX.csv) | Policy tracker and policy-citation counts. | [Dataset_3.1_policy_citation_counts_PlumX_codebook.csv](Metadata/Dataset_3.1_policy_citation_counts_PlumX_codebook.csv) |
| [Dataset4_ceesat_assessments.csv](Data/Dataset4_ceesat_assessments.csv) | CEESAT assessments for the included syntheses. | [Dataset4_ceesat_assessments_codebook.csv](Metadata/Dataset4_ceesat_assessments_codebook.csv) |
| [Dataset5_ceesat_processed.csv](Data/Dataset5_ceesat_processed.csv) | Processed CEESAT data: final scores for analysis. | [Dataset5_ceesat_processed_codebook.csv](Metadata/Dataset5_ceesat_processed_codebook.csv) |

## How to reproduce the analysis

The R folder contains [Wildlife_syntheses_figures_.Rmd](R/Wildlife_syntheses_figures_.Rmd). Its annotated code, together with the datasets, recreates the R-generated main and supplementary figures and the statistical analysis comparing the quality of syntheses cited and not cited in policy documents.

To run the code:

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

This exports main Figures 1, 3, 4 and 5 as 600-dpi PNG/TIFF and PDF, a code-generated base for Figure 2, and supplementary Figures S3–S11 as PNG/PDF. We manually edited the submitted Figure 2 in Affinity Designer 2, adding Anna Lenz’s original animal silhouettes and adjusting the Helvetica font size and appearance. The final composite figure is included; the separate original artwork files are available on request. We prepared Figures S1 and S2 manually in Affinity Designer 2. S4 uses an embedded publication word-cloud raster with an input-frequency check; if the keyword data change, the workflow stops until the embedded cloud and its frequency table are updated. Fonts and rendering engines can affect exact pixel appearance on another computer.

The workflow was tested with R 4.5.1. The tutorial’s **R packages** table lists the versions used to render it. RStudio is optional; rendering requires Pandoc, which RStudio includes.

## Interactive tutorial to replicate the figures and analysis

Our [HTML tutorial](https://annalenzr.github.io/noise_impact_wildlife_synthesis/Analysis.html) presents the rendered R Markdown workflow. Viewing it requires no software installation or accompanying files. The sidebar leads through an overview, direct links to the datasets and codebooks, the main figures with annotated code, the statistical analysis comparing CEESAT scores between syntheses cited and not cited in policy documents, and the supplementary figures generated with R (S3–S11).

You can also download [Analysis.html](Analysis.html) using GitHub’s **Download raw file** button and open it offline in a browser. Running the code requires R and the datasets, as described above.

## Protocol and paper citations

**Protocol.** Lenz A, Lundgren E, Mizuno A, Morrison K, Ortega S, Lagisz M, Nakagawa S. 2025. A systematic map of systematic reviews on anthropogenic noise impact on wildlife—protocol. OSF. https://doi.org/10.17605/OSF.IO/DMJC4.

**Original OSF project.** Nakagawa S, Lundgren E, Lagisz M, Ortega S, Morrison K, Mizuno A, Lenz A. 2025. A systematic map of systematic reviews on anthropogenic noise impact on wildlife—protocol [project]. OSF. https://doi.org/10.17605/OSF.IO/DMJC4. The protocol document and project share this DOI; their author orders follow the document and the OSF project’s citation metadata, respectively.

**OSF registration.** Lenz A, Nakagawa S, Lagisz M, Morrison K, Mizuno A, Ortega S, Lundgren E. 2025. A systematic map of systematic reviews on anthropogenic noise impact on wildlife—protocol [registration]. OSF. https://doi.org/10.17605/OSF.IO/7BX6G. The DOI metadata assigns 2025 to the protocol; the formal registration was created on 9 October 2026.

**Article.** Lenz A, Mizuno A, Lundgren E, Morrison K, Ortega S, Lagisz M, Nakagawa S. 2026. A systematic map of syntheses on anthropogenic noise impacts on wildlife: evidence gaps, policy attention, and quality appraisal. Environ Sci Pollut Res. https://doi.org/10.1007/s11356-026-38268-9.

**Zenodo repository.** [Authors]. [Year]. A systematic map of syntheses on anthropogenic noise impacts on wildlife: evidence gaps, policy attention, and quality appraisal: datasets and analysis code [dataset and software]. Version [version]. Zenodo. DOI: [to be added after archiving].

Please cite the Zenodo repository when using materials from this repository. We will add the final citation and DOI after archiving this release on Zenodo.

## License

Repository software is available under the [MIT License](LICENSE). Copyright (c) 2025 AnnaLenzR. You may use, copy, modify and distribute the software provided that you retain the copyright and permission notices. The software is provided “as is”, without warranty. Bibliographic source content retains its original rights; the separate animal artwork files are available on request.

## Corresponding author

Anna Lenz — [lenzrive@ualberta.ca](mailto:lenzrive@ualberta.ca) — [ORCID: 0009-0002-5706-7815](https://orcid.org/0009-0002-5706-7815).
