# A systematic map of syntheses on anthropogenic noise impacts on wildlife: evidence gaps, policy attention, and quality appraisal

[![Interactive tutorial](https://img.shields.io/badge/Tutorial-open%20in%20browser-537f72)](https://annalenzr.github.io/noise_impact_wildlife_synthesis/)
[![Protocol](https://img.shields.io/badge/Protocol-OSF-8b5776)](https://doi.org/10.17605/OSF.IO/7BX6G)
[![R](https://img.shields.io/badge/R-4.5.1-273d43)](#software-environment)
[![License: MIT](https://img.shields.io/badge/License-MIT-607074)](LICENSE)

We created this repository to support open science and help others reproduce our synthesis of syntheses on noise impacts on wildlife, their quality and their use in policy. Here, we share the full datasets, metadata to help you interpret them, and the R code for the analyses and figures in Lenz et al. (2026).

In this synthesis, we mapped reviews of the behavioural, physiological and ecological impacts of noise on wildlife across taxa and noise sources. We also examined research trends and collaboration networks, assessed synthesis quality using CEESAT, and explored policy relevance.

> [!TIP]
> **No installation needed to explore the results.** Our [interactive tutorial](https://annalenzr.github.io/noise_impact_wildlife_synthesis/) shows every figure, the statistical analysis and the annotated R code in your browser. To read it offline, right-click [this download link](https://github.com/AnnaLenzR/noise_impact_wildlife_synthesis/raw/main/Analysis.html) and choose *Save link as…*, then open the saved file in any browser.

## Contents

- [Protocol](#protocol)
- [Repository contents](#repository-contents)
- [Datasets and metadata](#datasets-and-metadata)
- [Software environment](#software-environment)
- [How to reproduce the analysis](#how-to-reproduce-the-analysis)
- [How to cite](#how-to-cite)
- [Contact](#contact)
- [Acknowledgements](#acknowledgements)
- [License](#license)

## Protocol

We deposited our protocol as an OSF project on 30 May 2025 ([Lenz et al. 2025](https://doi.org/10.17605/OSF.IO/DMJC4)). Following OSF's announcement of changes to its platform, we created a [formal registration of the same protocol](https://doi.org/10.17605/OSF.IO/7BX6G) on 9 October 2026 for preservation. You can read the protocol at either link.

Besides this repository, the journal's website hosts our supplementary material, with further details on our methods, search strategy and screening decisions.

## Repository contents

| Folder | Contents |
|---|---|
| [Data](Data/) | Seven final dataset files: six CSV files and one BibTeX (.bib) file. |
| [Metadata](Metadata/) | Seven CSV codebooks with variable definitions to help you code and interpret each dataset. |
| [R](R/) | The R Markdown file that reproduces the main and supplementary figures and analyses of the published article. |
| [Figures](Figures/) | [Final_figures](Figures/Final_figures/) holds the main figures as PNG files, with 600-dpi TIFF versions in its `tiff` subfolder; [Supplementary](Figures/Supplementary/) holds the supplementary figures as PNG and PDF files. |

The repository root also contains the rendered tutorial (`Analysis.html`, published at [annalenzr.github.io/noise_impact_wildlife_synthesis](https://annalenzr.github.io/noise_impact_wildlife_synthesis/)), the RStudio project file and [CITATION.cff](CITATION.cff).

## Datasets and metadata

The table lists each file in the Data folder, its content and its matching codebook in the Metadata folder.

<table>
  <thead>
    <tr>
      <th width="25%" align="left">Dataset file name</th>
      <th width="50%" align="left">Content</th>
      <th width="25%" align="left">Metadata file name</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td valign="top"><a href="Data/Dataset1_map_data_extraction.csv">Dataset1_map_data_<br>extraction.csv</a></td>
    <td valign="top">Map data extraction.</td>
    <td valign="top"><a href="Metadata/Dataset1_map_data_extraction_codebook.csv">Dataset1_map_data_<br>extraction_<br>codebook.csv</a></td>
  </tr>
  <tr>
    <td valign="top"><a href="Data/Dataset2_bibliometric_data.csv">Dataset2_<br>bibliometric_<br>data.csv</a></td>
    <td valign="top">Bibliometric data extracted from Scopus.</td>
    <td valign="top"><a href="Metadata/Dataset2_bibliometric_data_codebook.csv">Dataset2_<br>bibliometric_data_<br>codebook.csv</a></td>
  </tr>
  <tr>
    <td valign="top"><a href="Data/bibliometric.bib">bibliometric.bib</a></td>
    <td valign="top">The same bibliometric dataset as Dataset 2, in BibTeX format. The code can use this file with bibliometrix to draw the chord diagram.</td>
    <td valign="top"><a href="Metadata/bibliometric_codebook.csv">bibliometric_<br>codebook.csv</a></td>
  </tr>
  <tr>
    <td valign="top"><a href="Data/Dataset_3_policy_data_extraction.csv">Dataset_3_policy_<br>data_extraction.csv</a></td>
    <td valign="top">Policy-document data extraction.</td>
    <td valign="top"><a href="Metadata/Dataset_3_policy_data_extraction_codebook.csv">Dataset_3_policy_<br>data_extraction_<br>codebook.csv</a></td>
  </tr>
  <tr>
    <td valign="top"><a href="Data/Dataset_3.1_policy_citation_counts_PlumX.csv">Dataset_3.1_policy_<br>citation_counts_<br>PlumX.csv</a></td>
    <td valign="top">Policy tracker and policy-citation counts.</td>
    <td valign="top"><a href="Metadata/Dataset_3.1_policy_citation_counts_PlumX_codebook.csv">Dataset_3.1_policy_<br>citation_counts_<br>PlumX_codebook.csv</a></td>
  </tr>
  <tr>
    <td valign="top"><a href="Data/Dataset4_ceesat_assessments.csv">Dataset4_ceesat_<br>assessments.csv</a></td>
    <td valign="top">CEESAT assessments for the included syntheses.</td>
    <td valign="top"><a href="Metadata/Dataset4_ceesat_assessments_codebook.csv">Dataset4_ceesat_<br>assessments_<br>codebook.csv</a></td>
  </tr>
  <tr>
    <td valign="top"><a href="Data/Dataset5_ceesat_processed.csv">Dataset5_ceesat_<br>processed.csv</a></td>
    <td valign="top">Processed CEESAT data with final scores for analysis. We removed assessment comments and verbatim notes.</td>
    <td valign="top"><a href="Metadata/Dataset5_ceesat_processed_codebook.csv">Dataset5_ceesat_<br>processed_<br>codebook.csv</a></td>
  </tr>
  </tbody>
</table>

## Software environment

We rendered the tutorial and figures with the versions below. The tutorial's **R packages** table reports the same versions.

> [!IMPORTANT]
> **R 4.5.1.** Newer R releases should work, but package updates can change figure layout, fonts or colours.

> [!NOTE]
> **Data handling**
>
> | Package | Version |
> |---|---|
> | tidyverse | 2.0.0 |
> | here | 1.0.2 |
> | scales | 1.4.0 |
> | countrycode | 1.9.0 |

> [!NOTE]
> **Figures and layout**
>
> | Package | Version |
> |---|---|
> | paletteer | 1.7.0 |
> | treemapify | 2.6.1 |
> | ComplexUpset | 1.3.3 |
> | patchwork | 1.3.2 |
> | ggalluvial | 0.12.6 |
> | circlize | 0.4.18 |
> | ggthemes | 7.0.0 |
> | wordcloud2 | 0.2.1 |

> [!NOTE]
> **Bibliometrics and mapping**
>
> | Package | Version |
> |---|---|
> | bibliometrix | 5.5.0 |
> | sf | 1.1.3 |
> | rnaturalearth | 1.2.0 |
> | rnaturalearthdata | 1.0.0 |

> [!NOTE]
> **Rendering and export**
>
> | Package | Version |
> |---|---|
> | rmarkdown | 2.31 |
> | knitr | 1.51 |
> | ragg | 1.5.2 |
> | png | 0.1.9 |
> | base64enc | 0.1.6 |

> [!TIP]
> To install all packages at once:
>
> ```r
> install.packages(c(
>   "tidyverse", "here", "paletteer", "scales", "treemapify",
>   "bibliometrix", "ComplexUpset", "patchwork", "wordcloud2",
>   "sf", "rnaturalearthdata", "rnaturalearth", "ggalluvial",
>   "circlize", "countrycode", "png", "ragg", "ggthemes", "knitr",
>   "base64enc", "rmarkdown"
> ))
> ```

## How to reproduce the analysis

The R folder contains [Wildlife_syntheses_figures_.Rmd](R/Wildlife_syntheses_figures_.Rmd). Use this code with the datasets to recreate the figures we made in R and to compare the quality of syntheses cited and not cited in policy documents.

1. Clone or download this repository and open `Umbrella_review_noise.Rproj`, or set the working directory to the repository root.
2. Install the packages listed under [Software environment](#software-environment). The code checks that they are installed and stops with a list of any that are missing; it does not install them for you.
3. Render from the repository root:

```r
rmarkdown::render(
  "R/Wildlife_syntheses_figures_.Rmd",
  output_file = "Analysis.html",
  output_dir = getwd()
)
```

The code reconstructs Dataset 5 from Dataset 4 using Red = 0, Amber = 1, Green = 3 and Gold = 4. It checks all 1,050 cells against the final Dataset 5, then uses that final file for analysis. This check runs in memory and does not save another dataset or overwrite the source files.

By default, rendering updates only the HTML tutorial and leaves the final figure files intact. To export the figures as well:

```r
rmarkdown::render(
  "R/Wildlife_syntheses_figures_.Rmd",
  output_file = "Analysis.html",
  output_dir = getwd(),
  params = list(export_figures = TRUE)
)
```

This exports main Figures 1, 3, 4 and 5 as 600-dpi PNG/TIFF and PDF, a code-generated base for Figure 2, and supplementary Figures S3–S11 as PNG/PDF.

> [!NOTE]
> **Figures prepared outside R.** We edited the submitted Figure 2 in Affinity Designer 2, adding Anna Lenz's original animal silhouettes and adjusting the Helvetica font size and appearance. The final Figure 2 is in this repository; you can request the separate original artwork files from Anna. We also prepared Figures S1 and S2 in Affinity Designer 2.

> [!WARNING]
> **Figure S4 word cloud.** Figure S4 includes a saved word-cloud image. The code checks its keyword frequencies against the data and stops if they differ, so if you change the keyword data, update both the image and its frequency table. Fonts and graphics software can also change how figures look on another computer.

## How to cite

If you use materials from this repository, please cite our article.

**Article**

Lenz A, Mizuno A, Lundgren E, Morrison K, Ortega S, Lagisz M, Nakagawa S. 2026. A systematic map of syntheses on anthropogenic noise impacts on wildlife: evidence gaps, policy attention, and quality appraisal. Environmental Science and Pollution Research. https://doi.org/10.1007/s11356-026-38268-9

**Protocol**

Lenz A, Nakagawa S, Lagisz M, Morrison K, Mizuno A, Ortega S, Lundgren E. 2025. A systematic map of systematic reviews on anthropogenic noise impact on wildlife – protocol. OSF. https://doi.org/10.17605/OSF.IO/DMJC4

Lenz A, Nakagawa S, Lagisz M, Morrison K, Mizuno A, Ortega S, Lundgren E. 2026. A systematic map of systematic reviews on anthropogenic noise impact on wildlife – protocol [registration]. OSF Registries. https://doi.org/10.17605/OSF.IO/7BX6G

## Contact

For questions or requests, please contact Anna Lenz — [lenzrive@ualberta.ca](mailto:lenzrive@ualberta.ca) — [ORCID 0009-0002-5706-7815](https://orcid.org/0009-0002-5706-7815).

## Acknowledgements

We used Claude (Anthropic), an AI assistant, to help manage this repository: editing the README, checking links and citations, and tidying documentation. The authors reviewed all changes. The data, analyses and scientific content are the authors' own.

## License

We share the repository's software under the [MIT License](LICENSE). Copyright (c) 2025 AnnaLenzR. You may use, copy, modify and distribute the software provided that you retain the copyright and permission notices. The software is provided "as is", without warranty. The original rights still apply to bibliographic source content. Contact Anna to request the separate animal artwork files.
