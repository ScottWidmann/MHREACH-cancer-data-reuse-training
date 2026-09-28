# Getting to Know cBioPortal

**MHREACH • Breast Cancer Genomics**

*A step-by-step exploration for developing a breast cancer research question*

**Study View → Subtype Comparison → Genomic Alterations → Survival → Gene Query**

> This activity is for exploration and question development. You are not expected to complete a full research analysis today.

| Step | Focus |
|---|---|
| 1. FIND | The correct breast cancer study |
| 2. EXPLORE | The cohort and subtype charts |
| 3. COMPARE | Basal-like and Luminal A tumors |
| 4. QUESTION | Turn an observation into a project idea |

**What you will create:** A completed observation worksheet, four figures from cBioPortal, and one provisional research question.

> **Note on this document.** This is a text-only version of the original instructor handout. The original included illustrative screenshots of the live cBioPortal interface for each step; those screenshots have been removed from this public release because they reproduce a third-party website's interface and branding, and redistribution rights were not confirmed. Students still capture their own screenshots while completing the activity (see the `Screenshots/...` filenames referenced below) — only the instructor's example images were removed.

---

## Before You Begin

### Purpose of this activity

Your goal is to learn how cBioPortal is organized and to identify molecular differences that could become research questions. Do not try to explain every result. Focus on learning the interface, recording observations, and identifying one comparison that interests you.

### Set up your workspace

**A. Create a project folder**
- Create a folder named `LastName_cBioPortal_Exploration`.
- Inside it, create a subfolder named `Screenshots`.
- Open a blank document or use the spaces in this handout to record observations.

☐ **CHECKPOINT:** Your project folder and Screenshots subfolder are ready.

**B. Open cBioPortal**
- Open a desktop or laptop web browser. Chrome, Edge, Firefox, or Safari are acceptable.
- Go to the cBioPortal homepage only. You will practice locating the study yourself.
- [https://www.cbioportal.org/](https://www.cbioportal.org/)

☐ **CHECKPOINT:** The cBioPortal homepage is open.

> **Use the correct study.** For this activity, use *Breast Invasive Carcinoma (TCGA, PanCancer Atlas)*.
>
> **Important chart name.** Use the chart titled *Subtype*.

---

## Part 1 — Find and Open the Study

**1. Search for the breast cancer study**
- On the cBioPortal homepage, click the study-search box.
- Type: `Breast Invasive Carcinoma`
- Find the entry named *Breast Invasive Carcinoma (TCGA, PanCancer Atlas)*.
- Select the checkbox beside that study.
- Click **Explore Selected Studies**.

☐ **CHECKPOINT:** The Study View page opens and the study title includes "TCGA, PanCancer Atlas."

*Note: If you open the wrong study, return to the homepage and repeat this step.*

**2. Orient yourself in Study View**
- Read the study title at the top of the page.
- Locate the number of selected patients and samples near the top.
- Scan the page. You should see clinical charts, mutation summaries, copy-number summaries, and other study-level information.
- Do not click anything yet. Spend one minute identifying the major sections of the page.

☐ **CHECKPOINT:** You can point to the study title, sample count, Subtype chart, Mutated Genes table, and CNA Genes table.

### Record the study information

| Item | Your observation |
|---|---|
| Study name | |
| Patients / samples shown | |
| One data type available | |
| One chart or table you noticed | |

---

## Part 2 — Explore the Study View

**3. Find the molecular-subtype chart**
- Locate the multicolored pie chart titled *Subtype*. It is displayed by default in this study.
- Hover over each colored slice. Confirm that the labels include BRCA_Basal, BRCA_Her2, BRCA_LumA, BRCA_LumB, and BRCA_Normal.
- Record the sample count shown for each subtype.
- Take a screenshot of the Subtype chart and save it as `Screenshots/01_Subtype_chart.png`.

☐ **CHECKPOINT:** You have recorded the subtype counts and saved the screenshot.

*Note: If the chart is missing, click Charts → Clinical, search "Subtype," and select the chart named exactly "Subtype."*

### Subtype observations

| Subtype | Sample count | One observation |
|---|---|---|
| BRCA_Basal | | |
| BRCA_Her2 | | |
| BRCA_LumA | | |
| BRCA_LumB | | |
| BRCA_Normal | | |

**4. Inspect the most frequently mutated genes**
- Find the table titled *Mutated Genes*.
- Read the Gene, # Mut, and Freq columns.
- Record the first three genes shown and their mutation frequencies.
- Click one gene name to see whether the page filters or opens more information. Then clear the filter or use the browser Back button if needed.

☐ **CHECKPOINT:** You can explain that this table summarizes how often each gene is mutated across the study.

### Frequently mutated genes

| Gene | Mutation frequency | What might make this gene interesting? |
|---|---|---|
| | | |
| | | |
| | | |

**5. Inspect copy-number alterations**
- Find the table titled *CNA Genes*.
- Notice that the table distinguishes AMP (amplification) and HOMDEL (deep deletion).
- Record three genes with frequent amplifications or deep deletions.
- Compare this table with Mutated Genes. A gene may be important because it is mutated, amplified, deleted, or altered in more than one way.

☐ **CHECKPOINT:** You can distinguish a mutation from an amplification and a deep deletion.

### Copy-number observations

| Gene | Alteration type | Frequency | Why it might matter |
|---|---|---|---|
| | | | |
| | | | |
| | | | |

> **Pause and think.** Which result was more interesting to you: a frequently mutated gene, a subtype-specific pattern, or a copy-number alteration? Circle or highlight one observation before continuing.

---

## Part 3 — Compare Two Molecular Subtypes

**6. Open Group Comparison from the Subtype chart**
- Return to the Subtype pie chart if you have scrolled away from it.
- Open the menu in the upper-right corner of the Subtype chart. The icon appears as three horizontal lines.
- Click **Compare groups**.

☐ **CHECKPOINT:** The Group Comparison page opens and subtype groups appear across the top.

**7. Keep only BRCA_Basal and BRCA_LumA**
- Keep BRCA_Basal active.
- Keep BRCA_LumA active.
- Remove BRCA_Her2, BRCA_LumB, BRCA_Normal, and NA.
- Confirm that exactly two groups remain.

☐ **CHECKPOINT:** Only BRCA_Basal and BRCA_LumA are active in the comparison.

**8. Create a Genomic Alterations comparison figure**
- Click the **Genomic Alterations** tab.
- Wait for the gene-level comparison table and plot to load.
- Locate the q-Value column. Click its heading if needed so the smallest q-values are near the top.
- Record three genes with q-value < 0.05 and note which subtype shows the higher alteration frequency.
- Take a screenshot that includes the comparison plot or table, the two group names, and the q-values. Save it as `Screenshots/02_Genomic_alterations_comparison.png`.
- Do not interpret the q-value as the size of the difference. It indicates statistical evidence that the groups differ.

☐ **CHECKPOINT:** You recorded three genes and saved the Genomic Alterations comparison figure.

### Subtype-associated genomic differences

| Gene | BRCA_Basal % | BRCA_LumA % | q-value | Higher in |
|---|---|---|---|---|
| | | | | |
| | | | | |
| | | | | |

**9. Create a survival curve**
- Click the **Survival** tab near the top of the Group Comparison page.
- Confirm that the legend includes only BRCA_Basal and BRCA_LumA.
- Select **Overall Survival** if a survival-outcome menu is shown and another outcome is selected.
- Identify the Kaplan–Meier curve for each subtype. Observe whether the curves separate, overlap, or cross.
- Record the log-rank p-value shown with the plot and which group has the higher curve over most of the follow-up period.
- Take a screenshot that includes the curve, legend, axis labels, and p-value. Save it as `Screenshots/03_Survival_curve.png`.

☐ **CHECKPOINT:** You saved the survival curve and recorded a cautious interpretation.

*Note: A survival association provides clinical context. It does not prove that a particular gene causes the outcome or is a validated drug target.*

### Survival-curve observations

| Observation | Your response |
|---|---|
| Outcome displayed | |
| Log-rank p-value | |
| Which curve is generally higher? | |
| One limitation of this comparison | |

**10. Explore mutation locations with Mutations Beta**
- Click the **Mutations Beta** tab.
- Do not look for q-value sorting on this tab. Mutations Beta shows one gene at a time as paired lollipop plots.
- Click **TP53** under Highest Frequency. The upper plot represents BRCA_Basal and the lower plot represents BRCA_LumA.
- Look at the mutation-class counts at the right, including missense, truncating, inframe, and splice mutations.
- Repeat with **PIK3CA**.
- Optional: save a mutation lollipop screenshot if it will help explain your provisional research question.

☐ **CHECKPOINT:** You can describe one visible difference between the two subtypes for TP53 or PIK3CA.

### Mutation-pattern observations

| Gene | What differs between the two subtypes? | One question this result raises |
|---|---|---|
| TP53 | | |
| PIK3CA | | |

> **What the comparison views do.** Genomic Alterations identifies statistically significant differences in genes across groups. Survival compares patient outcomes between groups. Mutations Beta shows where mutations occur in a protein and which mutation classes are present. These views answer different questions.
>
> **How these figures support target research.** The Genomic Alterations comparison can nominate subtype-associated genes for further study. The survival curve can show whether the compared patient groups have different outcomes. Together, they provide hypothesis-generating evidence, but they do not validate a drug target on their own; laboratory and clinical studies are still required.

---

## Part 4 — Run a Simple Gene Query

**11. Return to the study and query a small gene panel**
- Click the study name near the top of the Group Comparison page to return to Study View. If that does not work, use the browser Back button until Study View reappears.
- Find the gene-entry box near the upper-right of Study View. It may say "Click gene symbols below or enter here."
- Paste this gene panel: `ESR1 ERBB2 TP53 PIK3CA`
- Click **Query**.
- Keep the default molecular profiles.

☐ **CHECKPOINT:** The Results View opens and the OncoPrint tab is visible.

**12. Create and read an OncoPrint**
- In the OncoPrint, each row is a gene and each column is a tumor sample.
- Use the legend to identify mutations, amplifications, deep deletions, and no alteration.
- Record the alteration percentage shown beside each gene.
- Choose one gene and hover over several colored cells to see sample-specific information.
- Take a screenshot that includes the queried genes, alteration percentages, and legend. Save it as `Screenshots/04_OncoPrint.png`.

☐ **CHECKPOINT:** You can explain the OncoPrint and saved the figure.

### Gene-query observations

| Gene | Alteration % | Main alteration type you noticed |
|---|---|---|
| ESR1 | | |
| ERBB2 | | |
| TP53 | | |
| PIK3CA | | |

---

## Part 5 — Develop Your Research Question

### Choose the observation you want to pursue

- ☐ A gene differed strongly between BRCA_Basal and BRCA_LumA.
- ☐ A mutation pattern differed between the two subtypes.
- ☐ A gene was frequently amplified or deeply deleted.
- ☐ A gene in the OncoPrint had an unexpected alteration pattern.
- ☐ The BRCA_Basal and BRCA_LumA survival curves differed or overlapped in an interesting way.
- ☐ Another cBioPortal result raised a question I want to investigate.

### Build a focused question

Use this template:

> In the TCGA PanCancer Atlas breast cancer cohort, does [gene or alteration] differ between [subtype A] and [subtype B]?

**Examples of appropriately focused questions**
- Is TP53 mutation frequency higher in BRCA_Basal than BRCA_LumA tumors?
- Is PIK3CA mutation frequency higher in BRCA_LumA than BRCA_Basal tumors?
- Is ERBB2 amplification concentrated in a specific molecular subtype?
- Do BRCA_Basal and BRCA_LumA tumors differ in the mutation classes observed in TP53?
- Do BRCA_Basal and BRCA_LumA tumors differ in overall survival?

### Draft your research question

> My provisional research question:
>
> _______________________________________________________________

### Question-quality checklist

- ☐ The question names a specific gene, alteration, or molecular feature.
- ☐ The question names the two groups being compared.
- ☐ The question can be investigated with data available in cBioPortal.
- ☐ The question asks about a difference or relationship rather than trying to prove a treatment works.
- ☐ The question is narrow enough to investigate during the training program.

---

## Final Checklist and Troubleshooting

### Files and responses to submit

- ☐ Completed study information table.
- ☐ Completed subtype, mutation, CNA, genomic-alteration, survival, and gene-query observation tables.
- ☐ `Screenshots/01_Subtype_chart.png`
- ☐ `Screenshots/02_Genomic_alterations_comparison.png`
- ☐ `Screenshots/03_Survival_curve.png`
- ☐ `Screenshots/04_OncoPrint.png`
- ☐ One provisional research question.
- ☐ One sentence explaining why the question interests you.

### One-sentence rationale

> Why this question interests me:
>
> _______________________________________________________________

### Common problems

| Problem | What to do |
|---|---|
| The page is blank or loads continuously | Refresh once. Close extra browser tabs. Return to the cBioPortal homepage and repeat the study-search steps. |
| I opened TCGA GDC 2025 | Return to the homepage and select Breast Invasive Carcinoma (TCGA, PanCancer Atlas). |
| The subtype chart shows only BRCA at 100% | You selected TCGA PanCanAtlas Cancer Type. Find the chart titled exactly "Subtype." |
| Compare groups is missing from the chart menu | Use the Groups button near the upper-right of Study View and compare groups based on the clinical attribute Subtype. |
| I cannot find q-values | Use the Genomic Alterations tab. Mutations Beta does not contain q-value sorting. |
| The Survival tab is missing or empty | Confirm that you are in Group Comparison, only BRCA_Basal and BRCA_LumA are selected, and the TCGA PanCancer Atlas study is open. If the plot still does not load, document the issue and continue. |
| The survival curves overlap or the p-value is not significant | Report that result honestly. Lack of a significant difference is still a valid observation. |
| My percentages differ from a group member's | Confirm that both of you used the same study and exactly BRCA_Basal and BRCA_LumA. |
| The interface label is slightly different | cBioPortal is updated periodically. Use the equivalent menu or button described in the step, and document what you clicked. |
