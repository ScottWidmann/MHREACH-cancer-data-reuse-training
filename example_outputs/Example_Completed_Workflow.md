# Example Completed Workflow (Illustrative)

> **What this is.** No student work is included in this repository — none was available for public release, and this training release does not contain any student names, photos, or submitted assignments (see the exclusions list in `README.md`). To show what a completed run of the curriculum looks like, this document assembles the worked examples, sample sentences, and practice gene list that already appear inside the lecture decks and protocols in this repository. It is a **teaching illustration**, not a real research finding — every numeric value below is a textbook/illustrative example reproduced from the cited slide or protocol, not a result generated for this document. Do not cite this page as a scientific result.
>
> Every line below names the exact source file and slide/section it was copied from, so it can be checked against the repository.

---

## 1. Research question

*(Template and example from `lectures/02_Week2_Research_Questions.pdf`, "Reporting")*

> "We compared Basal-like with Luminal A tumors. We observed that TP53 mutations were more common in Basal-like tumors. The figure that supports this is the Genomic Alterations comparison. One question this raised was whether TP53 mutations are also associated with different survival outcomes."

**Provisional research question** *(matches the Track 1 example in `lectures/02_Week2_Research_Questions.pdf`, "Project track examples")*:

> Which genomic alterations distinguish Basal-like from Luminal A breast cancer, and do TP53 alterations differ between the two subtypes?

## 2. cBioPortal step (`protocols/cBioPortal_Introduction.md`)

- **Study used:** Breast Invasive Carcinoma (TCGA, PanCancer Atlas)
- **Groups compared:** BRCA_Basal vs. BRCA_LumA
- **Observation** *(from `lectures/04_Week3_Poster_Design.pdf`, "How to present cBioPortal results")*:

  > "TP53 alterations were more frequent in BRCA_Basal than BRCA_LumA tumors, suggesting stronger disruption of tumor-suppressor pathways in the Basal-like group."

- **Figure produced:** Genomic Alterations comparison (students save this as `Screenshots/02_Genomic_alterations_comparison.png`, per the protocol — no screenshot is bundled with this repository).

## 3. Gene list handed to Enrichr and STRING

*(Practice List A, "Cell cycle and DNA repair," from `protocols/Protocol_Enrichr_STRING.md`, Section 3 — used here because it is thematically consistent with a TP53/Basal-like question)*

```
TP53, RB1, CDKN1A, CCND1, CDK4, CDK6, CCNB1, CDK1,
BRCA1, BRCA2, PALB2, RAD51, ATM, ATR, CHEK1, CHEK2, PARP1, BARD1
```

## 4. Enrichr results (worked example)

*(Reproduced from the worked example table in `lectures/03_Week3_Enrichr_STRING.pdf`, "What to record from Enrichr" — presented there as illustrative, not as a real Enrichr run)*

| Enriched term | Adjusted p-value | Overlap | Genes |
|---|---|---|---|
| p53 signaling pathway | 1.2e-5 | 5/84 | TP53, CDKN1A, BAX, ... |
| Cell-cycle checkpoint | 3.8e-4 | 4/63 | RB1, CHEK1, CCND1, ... |
| DNA damage response | 8.1e-4 | 4/97 | BRCA1, ATM, TP53, ... |
| PI3K-AKT signaling | 0.012 | 3/120 | PIK3CA, PTEN, AKT1, ... |

**Interpretation** *(from `protocols/Protocol_Enrichr_STRING.md`, Section 5, "Interpretation example")*:

> "Enrichr identified p53 signaling, cell-cycle checkpoints, and DNA-repair pathways. TP53, CHEK1, CHEK2, and CDKN1A contributed to several terms. This supports a hypothesis that the gene list reflects disrupted genome-surveillance and proliferation control; it does not prove that every gene is a driver or drug target."

## 5. STRING results (worked example)

*(From `lectures/03_Week3_Enrichr_STRING.pdf`, "Integrating cBioPortal, Enrichr, and STRING")*

> "TP53, RB1, BRCA1, ATM, and CHEK1 form a connected functional cluster."

## 6. Integrated project claim

*(From `lectures/03_Week3_Enrichr_STRING.pdf`, same slide — note the deliberately cautious language)*

> "Basal-like tumors show a genomic pattern consistent with disrupted DNA-damage and cell-cycle control."

*(Notice the language: "consistent with" and "supports." Not "proves" — see `lectures/03_Week3_Enrichr_STRING.pdf`, "Scientific caution.")*

## 7. Example poster title and results sentence

*(From `lectures/04_Week3_Poster_Design.pdf`, "Start with the question" and "Poster writing is compressed scientific writing")*

**Title:** "TP53 Alteration Patterns Distinguish Basal-like and Luminal A Breast Cancer"

**Results sentence:**

> "TP53 alterations were more common in BRCA_Basal tumors than BRCA_LumA tumors, supporting TP53 pathway disruption as a distinguishing feature of Basal-like breast cancer."

## 8. Required limitations statement

*(From `lectures/04_Week3_Poster_Design.pdf`, "Limitations make the poster stronger")*

- Observational data cannot prove causation.
- Subtype groups may have unequal sizes.
- Survival may be confounded by stage or treatment.
- A database signal is not drug validation.

---

*This illustrative walkthrough intentionally reuses only content already published elsewhere in this repository (see citations above), so that every line here can be checked against the corresponding source file.*
