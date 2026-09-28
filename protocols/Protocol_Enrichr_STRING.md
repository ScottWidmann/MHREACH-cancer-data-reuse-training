# Week 3 Protocol: Pathway Enrichment with Enrichr and Protein Association Networks with STRING

*A self-guided, step-by-step workflow using breast cancer gene lists*

| | | | | |
|---|---|---|---|---|
| 1. Prepare | 2. Enrichr | 3. STRING | 4. Compare | 5. Interpret |

Name: ______________________________________&nbsp;&nbsp;&nbsp;&nbsp;Group: ____________

Project question: ____________________________________________________________

**Purpose:** Use a gene list derived from your cBioPortal analysis to identify over-represented biological pathways in Enrichr and visualize functional protein associations in STRING. These tools generate hypotheses; they do not prove that a pathway causes cancer or that a gene is a validated drug target.

> Web interfaces change over time. Follow the named buttons and page sections in this protocol; small changes in color or placement are normal.

---

## 1. Before You Begin

**Learning objectives**
- Prepare a clean list of official human gene symbols.
- Use Enrichr to identify biological processes and pathways that overlap with the gene list.
- Use STRING to build and interpret a protein association network.
- Compare Enrichr and STRING results and write a cautious, evidence-based conclusion.

**Websites**
- Enrichr: [maayanlab.cloud/Enrichr](https://maayanlab.cloud/Enrichr/)
- STRING: [string-db.org](https://string-db.org)

**Files and screenshots to create**

| Required item | Suggested filename |
|---|---|
| Clean gene list | `Group##_gene_list.txt` |
| Enrichr results screenshot | `Group##_Enrichr_top_pathways.png` |
| Enrichr results table | `Group##_Enrichr_results.xlsx` or `.csv` |
| STRING network image | `Group##_STRING_network.svg` or `.png` |
| STRING enrichment table | `Group##_STRING_enrichment.tsv` or screenshot |
| Completed result tables in this protocol | `Group##_Week3_results.docx` or printed copy |

> **Important terminology.** Enrichr performs gene-set enrichment: it asks whether your list contains more genes from a known pathway than expected. STRING displays protein associations, including direct physical interactions and indirect functional relationships. A STRING edge does not automatically mean that two proteins physically bind.

**Minimum gene-list size**
- For practice: use one of the example lists in Section 3.
- For your project: aim for 15–50 unique genes. Lists shorter than about 10 genes often provide weak or unstable enrichment results.
- Do not submit one candidate gene alone. Enrichment and network analyses require a gene set.

---

## 2. Prepare a Project Gene List

**Preferred source: cBioPortal Group Comparison**

1. Open your Basal-like versus Luminal A comparison, or the comparison used for your project.
2. Open the Genomic Alterations tab.
3. Identify genes that differ between the groups. Record the group in which each gene is more frequently altered.
4. Create separate lists when direction matters: one list for genes enriched in Group A and another for genes enriched in Group B.
5. Select 15–50 genes using a consistent rule, such as the most significant genes with q < 0.05, or the top 20 genes after excluding obvious low-information entries.

> **Do not mix opposite directions without a reason.** If TP53 is more altered in Basal-like tumors and PIK3CA is more altered in Luminal A tumors, combining both into one list can obscure subtype-specific biology. Run separate Enrichr and STRING analyses for the two subtype-enriched lists when possible.

**Clean the list**

| Check | What to do |
|---|---|
| One symbol per line | Use official human gene symbols such as TP53, PIK3CA, ERBB2, and ESR1. |
| Uppercase symbols | Use standard HGNC-style capitalization for human genes. |
| Remove duplicates | Each gene should appear once. |
| Remove blanks and punctuation | Do not include commas, percentages, q-values, descriptions, or mutation names in the gene column. |
| Keep a record of the selection rule | Write how the genes were chosen and which cBioPortal groups were compared. |

**Project gene-list record**

| Field | Your entry |
|---|---|
| cBioPortal study | |
| Comparison groups | |
| Direction represented by this list | |
| Selection rule | |
| Number of unique genes | |
| Filename | |

> **Scientific limitation.** Standard Enrichr and STRING analyses compare your list with broad reference collections, not specifically with the TCGA breast-cancer genes that were measurable in your study. Treat the results as exploratory pathway and network evidence.

---

## 3. Example Gene Lists

Use these lists to learn the interfaces. For the final project, replace the practice list with genes derived from your cBioPortal analysis.

**Practice List A — Cell cycle and DNA repair**

`TP53, RB1, CDKN1A, CCND1, CDK4, CDK6, CCNB1, CDK1, BRCA1, BRCA2, PALB2, RAD51, ATM, ATR, CHEK1, CHEK2, PARP1, BARD1`

*Expected broad themes for practice: cell-cycle control, p53 signaling, DNA repair, homologous recombination.*

**Practice List B — ER/HER2 and PI3K-MAPK signaling**

`ESR1, PGR, ERBB2, ERBB3, EGFR, PIK3CA, AKT1, MTOR, PTEN, GATA3, FOXA1, GRB2, SHC1, SRC, MAPK1, MAPK3, CCND1, MYC`

*Expected broad themes for practice: estrogen signaling, receptor tyrosine kinase signaling, PI3K-AKT, MAPK, proliferation.*

### 3B. Project-Oriented Example Lists

Practice alternatives for different breast-cancer questions:

| Example focus | Gene list | Likely broad themes |
|---|---|---|
| Basal-like/TNBC candidates | TP53, BRCA1, BRCA2, PTEN, RB1, EGFR, MYC, PARP1, CHEK1, CHEK2, ATR, AURKA, CDK1, CCNB1, BCL2L1, MCL1, STAT1, JAK2, AKT1, PIK3CA | DNA damage, cell cycle, apoptosis, growth signaling |
| Luminal/ER-positive biology | ESR1, PGR, GATA3, FOXA1, PIK3CA, AKT1, PTEN, CCND1, CDK4, CDK6, RB1, MAP3K1, MAP2K4, CDH1, KMT2C, TBX3, NCOR1, GREB1, TFF1, BCL2 | estrogen response, luminal differentiation, PI3K signaling, cell cycle |
| HER2-centered signaling | ERBB2, ERBB3, GRB7, STARD3, MIEN1, PGAP3, EGFR, PIK3CA, AKT1, PTEN, SHC1, GRB2, SRC, MAPK1, MAPK3, MTOR, CCND1, MYC | HER2/ERBB signaling, PI3K-AKT, MAPK, proliferation |

> **Avoid circular interpretation.** These practice lists were selected because they contain known pathway members, so clear enrichment is expected. Your project list should be derived using a documented cBioPortal rule. Do not claim that an expected practice result is a new discovery.

---

## 4. Run Enrichr

**A. Submit the gene list**
1. Open the site. Go to the Enrichr homepage using the link in Section 1.
2. Paste the genes. Click inside the large gene-list text box and paste one gene symbol per line.
3. Add a description. In the optional description field, enter a short name such as `Group03_Basal_enriched_genes`.
4. Submit. Click Submit. Wait for the results page to load.
5. Check the recognized list. Open the input-gene-list view if available and confirm that the expected genes were recognized. Correct misspelled or outdated symbols before continuing.

**B. Open the three required libraries**
- GO Biological Process: choose the most recent human GO Biological Process library visible in the Ontologies section.
- KEGG Human: choose the most recent KEGG Human library visible in the Pathways section.
- Reactome: choose the most recent Reactome pathway library visible in the Pathways section.
- Record the exact library names and years displayed. Library versions change over time.

> **Which statistic should you use?** Use the adjusted p-value as the primary significance measure because many pathway terms are tested. For this student project, prioritize terms with adjusted p < 0.05 and at least 3 overlapping genes. The Combined Score can help rank terms, but it should not replace the adjusted p-value.

**C. Examine and save results**
1. For each required library, display the results table or bar chart.
2. Sort or visually prioritize terms by adjusted p-value. Do not select a result only because it has the largest Combined Score.
3. Record the top 3–5 biologically interpretable terms. Avoid very broad terms when a more specific supported term is available.
4. Record the overlapping input genes for each term. These genes explain why the pathway was returned.
5. Use the download control for the library results when available. Save the table as CSV, TSV, or Excel-compatible text.
6. Save a screenshot of one clear results chart or table that supports your project question.

---

## 5. Enrichr Results Worksheet

**Run information**

| Field | Student entry |
|---|---|
| Gene-list description | |
| Number of submitted genes | |
| Number recognized | |
| GO library name/year | |
| KEGG library name/year | |
| Reactome library name/year | |

**Top Enrichr terms**

| Library | Term | Adjusted p-value | Overlap | Input genes in term | Interpretation |
|---|---|---|---|---|---|
| GO BP | | | | | |
| GO BP | | | | | |
| KEGG | | | | | |
| KEGG | | | | | |
| Reactome | | | | | |
| Reactome | | | | | |

**Questions to answer**
- ☐ Which biological theme appears in more than one library?
  Response: __________________________________________________________________________
- ☐ Which input genes contribute to several enriched terms?
  Response: __________________________________________________________________________
- ☐ Does the result support your cBioPortal observation, contradict it, or add a new hypothesis?
  Response: __________________________________________________________________________
- ☐ Could the result be driven mainly by two or three famous genes?
  Response: __________________________________________________________________________
- ☐ What is one limitation of the gene list or enrichment analysis?
  Response: __________________________________________________________________________

> **Interpretation example.** Enrichr identified p53 signaling, cell-cycle checkpoints, and DNA-repair pathways. TP53, CHEK1, CHEK2, and CDKN1A contributed to several terms. This supports a hypothesis that the gene list reflects disrupted genome-surveillance and proliferation control; it does not prove that every gene is a driver or drug target.

---

## 6. Run STRING

**A. Submit the same gene list**
1. Open the site. Go to the STRING homepage using the link in Section 1.
2. Choose Multiple proteins. Click Multiple proteins in the Search area.
3. Paste the genes. Paste the same gene list used in Enrichr. STRING accepts one identifier per line or comma-separated entries.
4. Set the organism. In Organisms, select Homo sapiens. Do not leave the organism ambiguous.
5. Open Advanced Settings. Use Full STRING network and High confidence (0.700) for a clear student-level network. Use the default 5% FDR stringency unless your instructor specifies otherwise.
6. Search. Click Search.

**B. Resolve identifiers**
1. If STRING displays a protein-mapping page, confirm that each input maps to the correct human protein.
2. For ambiguous entries, select the standard protein corresponding to the official human gene symbol.
3. Record unmatched genes. Correct obvious spelling errors, but do not silently replace a gene with a different family member.
4. Continue to the network.

**C. Keep the network restricted to your input**
- Do not add extra first-shell or second-shell proteins for the initial analysis.
- If additional interactors appear, open Settings and set the number of added interactors to 0.
- Keeping only the input proteins makes the network easier to compare with the original cBioPortal list.

> **Network meaning.** STRING edges represent evidence-supported functional associations. Evidence may come from experiments, curated databases, co-expression, genomic context, or text mining. Some edges represent direct binding; others do not.

---

## 7. Interpret and Export the STRING Network

**A. Read the network summary**

| Metric | What it means | What to record |
|---|---|---|
| Number of nodes | Proteins included in the displayed network | Record the count and compare it with the number of recognized genes. |
| Number of edges | Displayed associations between proteins | More edges can indicate a connected functional module, but also reflect well-studied proteins. |
| Expected edges | Edges expected for a random protein set of similar size | Compare observed and expected edges. |
| Average node degree | Average number of associations per node | Use descriptively; high degree alone does not validate a target. |
| PPI enrichment p-value | Whether the proteins are more connected than expected | Record the value. A small p-value supports non-random functional connectivity. |

**B. Identify patterns**
1. Locate highly connected nodes. Record 2–3 possible hubs, but do not label them drug targets based only on network degree.
2. Look for clusters: groups of proteins connected more strongly to each other than to the rest of the network.
3. Click a node to read the protein name and functional annotation.
4. Open the evidence or edge display controls if you want to see whether an association is supported by experiments, databases, co-expression, or text mining.
5. Open the Analysis tab. Record the top biological processes and pathways that overlap with your Enrichr results.

**C. Export**
1. Open Download or Export on the STRING results page.
2. Save the network as SVG for the sharpest poster figure. PNG is acceptable when SVG is not available or cannot be inserted.
3. Download the interaction table and functional-enrichment table when available.
4. Record the STRING version, organism, network type, confidence threshold, and whether extra interactors were added.

> **Do not overinterpret a hub.** A highly connected node may be central to the submitted network, but degree can be inflated because some proteins are studied more extensively. Target prioritization also requires disease specificity, biological necessity, druggability, safety, and experimental validation.

---

## 8. STRING Results Worksheet

**Run settings and network statistics**

| Field | Student entry |
|---|---|
| STRING version | |
| Organism | Homo sapiens |
| Network type | Full STRING network |
| Required score | High confidence (0.700) |
| Added interactors | 0 |
| Recognized proteins | |
| Nodes | |
| Edges | |
| Expected edges | |
| Average node degree | |
| PPI enrichment p-value | |

**Network observations**

| Observation | Student entry |
|---|---|
| Two or three highly connected proteins | |
| One possible protein cluster | |
| Top STRING biological process | |
| Top STRING pathway | |
| Result shared with Enrichr | |
| Result unique to STRING | |

**Network interpretation prompts**
- ☐ Are most input proteins connected, or are several isolated?
- ☐ Which edges are supported by experimental or database evidence?
- ☐ Does one cluster correspond to a pathway identified by Enrichr?
- ☐ Which candidate gene is connected to proteins with relevant cancer functions?
- ☐ What evidence is still missing before calling the candidate a therapeutic target?

---

## 9. Integrate Enrichr and STRING

**Evidence table**

| Evidence source | Main result | What it supports | What it cannot establish |
|---|---|---|---|
| cBioPortal | A gene or gene set differs between breast-cancer groups. | Subtype association and recurrence across tumors. | Causation, pathway activity, or therapeutic response. |
| Enrichr | Input genes overlap known pathways or processes. | A pathway-level biological hypothesis. | That the pathway is active in every tumor or caused the phenotype. |
| STRING | Input proteins form a connected functional network. | Functional relationships, clusters, and candidate network context. | Direct physical binding for every edge or target validity. |
| Survival analysis, if used | Groups differ or do not differ in observed survival. | Clinical association worth investigating. | Causation; confounding by stage, treatment, and cohort composition remains. |

**Write the integrated conclusion**

> **Four-sentence template:** 1. We analyzed [number] genes selected because [selection rule]. 2. Enrichr identified [pathways/processes], supported by [key genes]. 3. STRING showed [connectivity, cluster, or hub pattern] and a PPI enrichment p-value of [value]. 4. Together, these results support the hypothesis that [cautious interpretation], but experimental studies are required to establish mechanism and therapeutic value.

**Target-prioritization checklist**
- ☐ Altered at a meaningful frequency in the disease group.
- ☐ More specific to the subtype or comparison group of interest.
- ☐ Located in an enriched cancer-relevant pathway.
- ☐ Connected to relevant proteins in STRING.
- ☐ Associated with outcome, when survival analysis is appropriate.
- ☐ Biologically plausible and potentially druggable.
- ☐ Not already dismissed by obvious safety or essential-function concerns.
- ☐ Requires laboratory validation before being called a validated target.

**Integrated student conclusion**

____________________________________________________________________________________
____________________________________________________________________________________
____________________________________________________________________________________
____________________________________________________________________________________
____________________________________________________________________________________

---

## 10. Troubleshooting

| Problem | Likely cause | Action |
|---|---|---|
| Enrichr recognizes very few genes | Misspelled, outdated, non-human, or non-gene identifiers | Return to the input list; use official human symbols; remove mutation notation such as TP53 R175H. |
| No significant Enrichr terms | List is too short, heterogeneous, or lacks a coherent pathway signal | Check list size and selection rule. Do not add genes merely to force significance. Report the negative result if the list is valid. |
| Enrichr returns hundreds of broad terms | Overlapping libraries and highly connected genes produce redundant results | Prioritize adjusted p-value, overlap size, specificity, and repeated themes across libraries. |
| STRING asks for organism | Organism was left on auto-detect | Select Homo sapiens before searching. |
| STRING cannot map a gene | Ambiguous or unsupported identifier | Confirm the official symbol. Record unresolved entries rather than choosing a different protein without justification. |
| STRING network is overcrowded | Extra interactors were added or confidence threshold is low | Set added interactors to 0 and required score to high confidence (0.700). |
| STRING network has isolated nodes | No strong association at the chosen confidence level | Keep the result. Isolation is informative; do not lower confidence solely to make the network look connected. |
| Enrichr and STRING disagree | The tools use different databases, statistics, and evidence types | Report both results and explain the difference rather than selecting only the preferred result. |
| Downloaded image is blurry | Raster image was copied from the screen | Export SVG or a high-resolution PNG from the tool rather than using a low-resolution screenshot. |

> **Issues to look out for:** If fewer than 10 genes map, when you cannot determine which group a gene list represents, when a gene symbol maps to multiple proteins, or when a statistical result appears inconsistent with the plotted data.

---

## 11. Submission Checklist

- ☐ Clean project gene list with one official human gene symbol per line.
- ☐ Written cBioPortal comparison and gene-selection rule.
- ☐ Enrichr run using GO Biological Process, KEGG Human, and Reactome.
- ☐ Enrichr table with adjusted p-values, overlap, and contributing genes.
- ☐ One Enrichr figure or clearly legible results screenshot.
- ☐ STRING network using Homo sapiens, full network, high confidence (0.700), and 0 added interactors.
- ☐ STRING network statistics, including PPI enrichment p-value.
- ☐ One exported STRING network image.
- ☐ Integrated conclusion using evidence from both tools.
- ☐ At least two limitations and one proposed follow-up experiment.

**Suggested follow-up experiment**

What laboratory or computational experiment would test your hypothesis?

____________________________________________________________________________________
____________________________________________________________________________________
____________________________________________________________________________________
____________________________________________________________________________________

Official web resources are linked in Section 1. Record the displayed database and library versions because online resources are updated.
