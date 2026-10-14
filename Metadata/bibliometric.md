# Metadata: bibliometric.bib

Data file: [../Data/bibliometric.bib](../Data/bibliometric.bib)

**Coverage:** 47 bibliographic records; Scopus export dated 31 July 2025. This is the BibTeX counterpart of Dataset2, not an additional set of syntheses. The retained working bibliography includes verified bibliographic corrections and is not an untouched database export.

The initial `Scopus` and `EXPORT DATE` lines identify the source. Each `@ARTICLE{key, ...}` entry is one record. Citation keys are export identifiers, not the study_id keys in the extraction datasets. Fields vary by record; absent or empty fields indicate unavailable metadata. DOI is the cross-dataset matching key. The analysis defaults to Dataset2 for country parsing; an optional bibliometrix route reads this file.

| Field | Definition |
|---|---|
| `abstract` | Publication abstract. |
| `affiliations` | Institutional affiliations and countries, separated by semicolons. |
| `author` | Authors, separated by BibTeX and. |
| `author_keywords` | Keywords in the exported author-keyword field. |
| `coden` | Journal CODEN identifier. |
| `doi` | Digital Object Identifier. |
| `isbn` | ISBN identifier(s), when available. |
| `issn` | ISSN identifier(s). |
| `journal` | Journal or proceedings title. |
| `keywords` | Indexed keyword terms. |
| `language` | Publication language. |
| `note` | Scopus snapshot citation count (Cited by: n). |
| `number` | Issue number. |
| `pages` | Page range; can be empty for article-number publications. |
| `pmid` | PubMed identifier. |
| `publication_stage` | Scopus publication-stage label. |
| `publisher` | Publisher. |
| `source` | Bibliographic source, Scopus. |
| `title` | Publication title. |
| `type` | Scopus document type. |
| `url` | Scopus record URL. |
| `volume` | Journal/proceedings volume. |
| `year` | Publication year in this bibliography. |

## File identity

SHA-256: `b2e9cd6c8bba74e0295aa7194dbd173b5b28920fcf6e40511cb56cc299b17cc7`

Metadata checked against this file on 14 October 2026.
