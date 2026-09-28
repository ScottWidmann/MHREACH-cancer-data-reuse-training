# MHREACH Breast Cancer Data Reuse Training

A four-part, no-code training program that teaches high school students to reuse public cancer genomics databases such as cBioPortal, TCGA, and METABRIC, and pathway/network tools Enrichr and STRING to develop and investigate an original breast cancer research question, culminating in a scientific poster.

This repository is a curated, public-release version of the original MHREACH program materials (2026). Everything here runs in a standard web browser, with no coding, no downloads, and no specialized software license required.

**Rights holder:** Scott Widmann. See `LICENSE` for terms and `CITATION.cff` for how to cite this program.

## Audience

High-school students with no prior programming or bioinformatics experience. The program assumes only general high-school biology (cell biology, basic genetics) — the first lecture (`lectures/01_Breast_Cancer_Project_Intro.pdf`) builds the needed cancer-biology background from scratch ("Cancer Biology 101," oncogenes vs. tumor suppressors, breast cancer subtypes) before any database work begins.

## Learning objectives

By the end of the program, a student should be able to (per `lectures/01_Breast_Cancer_Project_Intro.pdf`, "What You Will Do in This Project" and "Success Criteria"):

1. **Ask** — frame a focused research question comparing breast cancer subtypes (e.g., ER+, HER2+, triple-negative).
2. **Extract** — pull mutation and expression data for chosen genes from cBioPortal.
3. **Analyze** — summarize alteration patterns and build an original chart in Excel/Google Sheets.
4. **Interpret** — use Enrichr and STRING to identify affected pathways and protein networks.
5. **Present** — deliver a scientific poster that states a research question, evidence, interpretation, and honest limitations.

Throughout, the curriculum explicitly trains students to distinguish an observed database pattern from a proven mechanism (see the "Scientific Claims" and "Stay honest about limits" material in `lectures/01_Breast_Cancer_Project_Intro.pdf` and `lectures/04_Week3_Poster_Design.pdf`).

## Prerequisites

- A web browser (Chrome, Edge, Firefox, or Safari) and internet access — no software installation.
- Access to a spreadsheet application (Google Sheets or Excel).
- No coding, statistics course, or prior research experience is required; all tools used are described in the curriculum as free and browser-based (see `resources.md`).

## Curriculum sequence

| Order | File | Content |
|---|---|---|
| 1 | `lectures/01_Breast_Cancer_Project_Intro.pdf` | Cancer biology fundamentals, breast cancer subtypes, public cancer databases (TCGA, METABRIC, cBioPortal), the five-step project workflow, approved research tracks, approved gene panels, and the one-month project timeline. |
| 2 | `protocols/cBioPortal_Introduction.md` | Hands-on, checkpointed walkthrough of cBioPortal: finding the TCGA breast cancer study, reading the Subtype chart, comparing two molecular subtypes, reading a survival curve, running a gene query and OncoPrint, and drafting a provisional research question. |
| 3 | `lectures/02_Week2_Research_Questions.pdf` | Turning a cBioPortal observation into a specific, answerable research question; question templates; the four project tracks (subtype comparison, candidate-target prioritization, mutation-pattern analysis, clinical-outcome association). |
| 4 | `lectures/03_Week3_Enrichr_STRING.pdf` and `protocols/Protocol_Enrichr_STRING.md` | Moving from a gene list to biological interpretation: running Enrichr (GO Biological Process, KEGG, Reactome) and STRING (protein association networks), recording results, and writing a cautious, evidence-based integrated conclusion. |
| 5 | `lectures/04_Week3_Poster_Design.pdf` | Turning the completed analysis into a scientific poster: required sections, figure selection, writing style, honest limitations, and a poster-pitch structure. |

`example_outputs/Example_Completed_Workflow.md` shows what a finished run of this sequence looks like, assembled entirely from the worked examples already published inside the files above (see that file for full sourcing — it is explicitly labeled as an illustrative teaching example, not a real research result).

## Repository structure

```
README.md                  — this file
resources.md                — databases/tools used, with full citations
LICENSE                     — CC BY 4.0 (docs/lectures/protocols) + MIT (any code)
CITATION.cff                — machine-readable citation metadata
lectures/                   — the four lecture decks, in curriculum order
protocols/                  — the two hands-on protocols, converted to Markdown
example_outputs/            — one illustrative worked example (see above)
```

There is no `scripts/` directory: the original program materials contain no code, only lecture decks and fillable protocol worksheets, so none is included.

## Data and privacy

This program does not use or redistribute any student data, and no student names, photos, or student-submitted work exist in this repository. It also does not download, store, or redistribute any dataset from a third-party database — students query TCGA and METABRIC live, through cBioPortal, in their own browser session, and record their own observations. See `resources.md` for the full list of external databases and tools referenced, with citations.

## License and citation

- Lectures, protocols, and this documentation are licensed under **CC BY 4.0**.
- Any code added to this repository in the future is licensed under **MIT**.
- See `LICENSE` for full terms and `CITATION.cff` for citation metadata.
