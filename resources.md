# Resources and Citations

This training program teaches students to work with public, browser-based cancer genomics resources. No dataset is redistributed inside this repository — students query these databases live, in their own browser, on each database's own site. This page lists every external database and tool referenced in the curriculum, together with the primary literature citation for each, and the additional references named directly in the Week 3 lecture (`lectures/03_Week3_Enrichr_STRING.pdf`, "Source notes and cautions").

Citation details below were retrieved from PubMed and are current as of the date this page was written.

## Databases and tools used

| Resource | What students use it for | Where it appears |
|---|---|---|
| **cBioPortal for Cancer Genomics** ([cbioportal.org](https://www.cbioportal.org/)) | Browser-based exploration of TCGA and METABRIC breast cancer cohorts: subtype charts, mutation/copy-number tables, group comparison, survival curves, OncoPrint, gene queries. | `lectures/01_Breast_Cancer_Project_Intro.pdf`, `lectures/02_Week2_Research_Questions.pdf`, `protocols/cBioPortal_Introduction.md` |
| **TCGA — The Cancer Genome Atlas** (Breast Invasive Carcinoma, PanCancer Atlas cohort, accessed via cBioPortal) | Primary breast cancer cohort used for the training program's comparisons (e.g., BRCA_Basal vs. BRCA_LumA). | `lectures/01_Breast_Cancer_Project_Intro.pdf`, `protocols/cBioPortal_Introduction.md` |
| **METABRIC — Molecular Taxonomy of Breast Cancer International Consortium** (accessed via cBioPortal) | Alternative/comparison breast cancer cohort referenced in the introductory lecture. | `lectures/01_Breast_Cancer_Project_Intro.pdf` |
| **Enrichr** ([maayanlab.cloud/Enrichr](https://maayanlab.cloud/Enrichr/)) | Gene-set enrichment analysis against GO Biological Process, KEGG, and Reactome libraries. | `lectures/03_Week3_Enrichr_STRING.pdf`, `protocols/Protocol_Enrichr_STRING.md` |
| **STRING** ([string-db.org](https://string-db.org)) | Protein-protein functional association networks and network-level enrichment. | `lectures/03_Week3_Enrichr_STRING.pdf`, `protocols/Protocol_Enrichr_STRING.md` |
| **Google Sheets / Microsoft Excel** | General-purpose spreadsheet tools for tabulating alteration frequencies and building charts. No account or license beyond a standard spreadsheet application is required. | `lectures/01_Breast_Cancer_Project_Intro.pdf` |

All of the above are free, browser-based, and require no coding, no local installation, and no special institutional license — consistent with this program's role as the no-code precursor tier described in `README.md`.

## Primary citations

**cBioPortal**
- Cerami E, Gao J, Dogrusoz U, et al. The cBio Cancer Genomics Portal: An Open Platform for Exploring Multidimensional Cancer Genomics Data. *Cancer Discovery*. 2012;2(5):401–404. [DOI: 10.1158/2159-8290.CD-12-0095](https://doi.org/10.1158/2159-8290.CD-12-0095)
- Gao J, Aksoy BA, Dogrusoz U, et al. Integrative analysis of complex cancer genomics and clinical profiles using the cBioPortal. *Science Signaling*. 2013;6(269):pl1. [DOI: 10.1126/scisignal.2004088](https://doi.org/10.1126/scisignal.2004088)

**TCGA breast cancer cohort**
- The Cancer Genome Atlas Network. Comprehensive molecular portraits of human breast tumours. *Nature*. 2012;490(7418):61–70. [DOI: 10.1038/nature11412](https://doi.org/10.1038/nature11412)

**METABRIC**
- Curtis C, Shah SP, Chin SF, et al. The genomic and transcriptomic architecture of 2,000 breast tumours reveals novel subgroups. *Nature*. 2012;486(7403):346–352. [DOI: 10.1038/nature10983](https://doi.org/10.1038/nature10983)

**Enrichr** *(the first two references below are named directly in `lectures/03_Week3_Enrichr_STRING.pdf`)*
- Chen EY, Tan CM, Kou Y, et al. Enrichr: interactive and collaborative HTML5 gene list enrichment analysis tool. *BMC Bioinformatics*. 2013;14:128. [DOI: 10.1186/1471-2105-14-128](https://doi.org/10.1186/1471-2105-14-128)
- Xie Z, Bailey A, Kuleshov MV, et al. Gene Set Knowledge Discovery with Enrichr. *Current Protocols*. 2021;1(3):e90. [DOI: 10.1002/cpz1.90](https://doi.org/10.1002/cpz1.90)
- Kuleshov MV, Jones MR, Rouillard AD, et al. Enrichr: a comprehensive gene set enrichment analysis web server 2016 update. *Nucleic Acids Research*. 2016;44(W1):W90–W97. [DOI: 10.1093/nar/gkw377](https://doi.org/10.1093/nar/gkw377)

**STRING** *(the reference below is named directly in `lectures/03_Week3_Enrichr_STRING.pdf`)*
- Szklarczyk D, Nastou K, Koutrouli M, et al. The STRING database in 2025: protein networks with directionality of regulation. *Nucleic Acids Research*. 2025;53(D1):D730–D737. [DOI: 10.1093/nar/gkae1113](https://doi.org/10.1093/nar/gkae1113)
- Szklarczyk D, Kirsch R, Koutrouli M, et al. The STRING database in 2023: protein-protein association networks and functional enrichment analyses for any sequenced genome of interest. *Nucleic Acids Research*. 2023;51(D1):D638–D646. [DOI: 10.1093/nar/gkac1000](https://doi.org/10.1093/nar/gkac1000)

*Citation metadata retrieved from PubMed.*

## Data-reuse note

This training program never downloads, stores, or redistributes patient-level or cohort-level data from TCGA, METABRIC, or any other database. Students query these public portals live, in their own browser session, and record their own observations (numbers, screenshots, charts) as coursework. No third-party dataset, and no screenshot of a third-party website's interface, is bundled in this repository — see the exclusions section of `README.md` for what was left out and why.
