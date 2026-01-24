---
layout: page
title: Comprehensive landscape of tRNA-derived fragments in lung cancer
subtitle: Diagnostic and prognostic tRDF signatures in NSCLC
description: tDRF profiling, diagnostic signatures, plasma validation, and immunotherapy associations
category: work
importance: 3
img: /assets/img/tRDF/graphical_abstract.png
---

## Overview
**Highlight:** Six tRDF diagnostic signatures achieve AUC up to 0.90; selected signatures validated in plasma and linked to cell cycle and PD-L1 pathways.

tRNA-derived fragments (tRDFs) are a class of small non-coding RNAs observed across multiple cancers, but their landscape in non-small cell lung cancer (NSCLC) remains under-characterized. In this study, we analyzed 1,550 NSCLC patient samples and identified 52 tRDFs across four subtypes. Six tRDFs were selected as diagnostic signatures based on expression patterns, achieving AUC up to 0.90 in independent validations. Two signatures were successfully validated in plasma samples, and six signatures showed consistent differential expression in NSCLC cell lines. Ten tRDFs, together with stage-specific risk scores, predicted survival outcomes; 5a_tRF-Ile-AAT/GAT may serve as an early-stage prognostic biomarker. Association analyses suggested that correlated mRNAs and targeted miRNAs were enriched in cell cycle and oocyte meiosis pathways. Five tRDFs were associated with PD-L1 immune checkpoint signatures and genes involved in PD-L1 signaling. Overall, this work provides a comprehensive tRDF atlas in lung cancer and supports tRDFs as diagnostic, prognostic, and immunotherapy-relevant biomarkers.

{% include figure.liquid
  path="/assets/img/tRDF/tsRNA_common_Page_1.png"
  class="img-fluid rounded z-depth-1"
  alt="Overview figure summarizing common tRDFs across datasets"
%}

---

## Differentially expressed tRDFs in tumor vs normal samples
**Highlight:** 11 common DE tRDFs replicated across GEO datasets; external validations reach AUC 0.914 and 0.905.

(A and B) Heatmaps show DE tRDFs in two GEO datasets with paired tumor and normal samples. Up- and downregulated tRDFs separate by unsupervised clustering.  
(C and D) Boxplots show 11 tRDFs identified as common DE across GEO datasets (p < 0.05).  
(E) Correlogram shows Pearson correlations among the 11 DE tRDFs.  
(F and G) AUCs show independent validation results in GEO and TCGA-LUAD.  
(H) Expression of six DE tRDFs in TCGA-LUAD.  
(I) Diagnostic performance of six-tRDF signature across five independent validations.

{% include figure.liquid
  path="/assets/img/tRDF/figure2.png"
  class="img-fluid rounded z-depth-1"
  alt="Differential expression and validation of tRDF signatures across GEO and TCGA cohorts"
%}

---

## Plasma validation in NSCLC patients and healthy donors
**Highlight:** Plasma TPM expression supports diagnostic utility of selected tRDFs.

TPM expression of six tRDFs between tumor and healthy controls:  
3P_tRNA-Ser-GCT-6-1 (A), 3P_tRNA-Arg-TCG-1-1 (B), 3P_tRNA-SeC-TCA-1-1 (C), 3P_tRNA-Val-TAC-1-1 (D), 5P_tRNA-Asn-GTT-2-3 (E), and 5b_tRF-Tyr-GTA (F).  
*p ≤ 0.05, **p ≤ 0.01, ns = not significant.*

{% include figure.liquid
  path="/assets/img/tRDF/figure3.png"
  class="img-fluid rounded z-depth-1"
  alt="Plasma validation of tRDF expression between NSCLC patients and healthy donors"
%}

---
## workflow of the whole bioinformatics analysis
{% include figure.liquid
  path="/assets/img/tRDF/workflow.png"
  class="img-fluid rounded z-depth-1"
  alt="workflow"
%}


---
## Immune infiltration and tumor microenvironment correlated with tRDFs

(A) Bar plot shows the correlation between tRDFs and TIME cell infiltration evaluated by Pearson correlation. The length of column indicates the correlation; immune cells were selected from the mutual correlation with 5ʹ-tRDFs and 3ʹ-tRDFs. (B) Kaplan-Meier curves show overall survival of plasma cells that correlated with prognostic tRDFs. Red color indicates the high abundance of plasma cells, and blue color indicates the low abundance of plasma cells. (C) Network shows the tRDF-targeted immune-related signaling pathways in TCGA-LUAD cohort, including primary immunodeficiency, viral protein interaction with cytokine and cytokine receptor, cytokine-cytokine receptor interaction, hematopoietic cell lineage, T cell receptor signaling pathway, and the other signaling pathway. IgA, immunoglobulin A. (D) The correlation between tRDF with immune checkpoint CD274 (PD-L1), CTLA4, CD80, and CD86.

{% include figure.liquid
  path="/assets/img/tRDF/figure7.png"
  class="img-fluid rounded z-depth-1"
  alt="Plasma validation of tRDF expression between NSCLC patients and healthy donors"
%}
