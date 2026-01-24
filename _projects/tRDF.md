---
layout: page
title: Comprehensive landscape of tRNA-derived fragments in lung cancer
subtitle: Diagnostic and prognostic tRDF signatures in NSCLC
img: assets/img/tRDF/graphical abstract.png
description: tDRF profiling, diagnostic signatures, plasma validation, and immunotherapy associations
category: work
importance: 3
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
## workflow of the whole bioinformatics analysis
{% include figure.liquid
  path="/assets/img/tRDF/workflow.png"
  class="img-fluid rounded z-depth-1"
  alt="workflow"
%}

---

## Differentially expressed tRDFs in tumor vs normal samples
**Highlight:** 11 common DE tRDFs replicated across GEO datasets; external validations reach AUC 0.914 and 0.905.

Based on clustering results, we investigated the differentially expressed (DE) tRDFs in cluster B to gain a comprehensive understanding of the expression pattern of the tRDFs between tumor and normal samples. Due to the different data platforms, GEO and TCGA were separately calculated. We used Deseq2 and t-test in two GEO datasets (GSE83527 and GSE62812) and TCGA-LUAD cohort based on both raw read counts and normalized expression profile TPM, respectively. Both tumor and normal samples were included and the DE tRDFs were chosen with the selection standard Padj/FDR<0.05 and |log2fold change| > 0.58.
In the GSE83527, 32 DE tRDFs were identified including 18 5’-tRDFs and 14 3’-tRDFs (Table S7-1). In the GSE628182, 16 DE tRDFs in total were found as significant differentially expressed tRDFs including eight 5’-tRDFs (5P_tRNA-Gly-TCC-1-1, 5P_tRNA-Asn-GTT-2-3, 5b_tRF-Tyr-GTA , 5c_tRF-Arg-CCG-2-1, 5P_tRNA-Gly-TCC-3-1, 5P_tRNA-Gln-TCC-1-1,  5a_tRF-Asp-GTC,5a_tRF-Ile-AAT/GAT) and eight 3’-tRDFs (3P_tRNA-Val-TAC-1-1, 3P_tRNA-SeC-TCA-1-1, 3P_tRNA-Thr-CGT-4-1, 3P_tRNA-Arg-TCT-4-1,  3P_tRNA-Ser-GCT-6-1, 3a_tRF-Leu-TAG/AAG, 3P_tRNA-Arg-TCG-1-1, and 3b_tRF-Leu-CAA/CGA). (A, B). 
Finally, 11 mutual tRDFs in two GEO datasets were identified, including five upregulated tRDFs: 3P_tRNA-Ser-GCT-6-1, 3P_tRNA-Arg-TCG-1-1, 5a_tRF-Asp-GTC, 3P_tRNA-Arg-TCT-4-1, 5a_tRF-Ile-AAT/GAT and six downregulated tRDFs: 5b_tRF-Tyr-GTA , 5P_tRNA-Gly-TCC-1-1, 5P_tRNA-Gly-TCC-3-1, 5P_tRNA-Asn-GTT-2-3, 3P_tRNA-Val-TAC-1-1, 3P_tRNA-SeC-TCA-1-1 (C, D). The log2 fold changes of two datasets can be found in Figure S1E. We also included the genome tracks of 11 tRDFs in Fig S2, S3. Besides DE tRDFs, three unchanged tRDFs, 3P_tRNA-Arg-CCT-3-1, 3P_tRNA-Arg-TCG-2-1, and 5P_tRNA-SeC-TCA-1-1 were found overlapped in GEO and TCGA datasets. 
To explore the relationship within these candidate tRDFs, we calculated pairwise correlations among the expression of 11 tRDFs in GSE83527 and GSE62182 (E). Notably, the expression of two downregulated tRDFs (5P_tRNA-Gly-TCC-1-1 and 5P_tRNA-Asn-GTT-2-3) were remarkably correlated with the rest of tRDFs (absolute value of correlation coefficients are between 0.18-0.47). We also noticed that the expression of 5’-tRDFs was not only correlated in the same category, but also significantly correlated with 3’-tRDFs. 5P_tRNA-Gly-TCC-1-1 with 3P_tRNA-Val-TAC-1-1 and 5P_tRNA-Asn-GTT-2-3 were positively correlated, and the highest correlation coefficient between upregulated tRDFs 5a_tRF-Ile-AAT/GAT and 5a_tRF-Asp-GTC is 0.42. A negative correlation was found between upregulated and downregulated tRDFs such as 5P_tRNA-Gly-TCC-1-1 and 3P_tRNA-Arg-TCG-1-1 with a coefficient of -0.44. 
In terms of the GMM-tsne cluster result, we decided to take advantage of the machine learning technique, random forest, to investigate the diagnostic value of the 11 tRDFs on distinguishing the tumor and normal samples. Two GEO datasets (GSE83527 and GSE62182) that contain pairwise data (N: 128; T: 128) were merged and used as training datasets; we also included two independent validation groups from the TCGA-LUAD cohort (N: 46, T: 460) and GSE110907 (N: 48, T: 48). 11 DE tRDFs were used as variables to build this classification model, with an out of bag (OOB) estimate of error rate at 8.09%. Independent validations on TCGA-LUAD and GSE110907 achieved excellent AUC (GSE110907: 0.914, TCGA-LUAD: 0.905) (F, G), and all sensitivity, specificity, and accuracy were above 0.80. The results suggest the performance of 11 DE tRDFs in the random forest model was significantly associated with adenocarcinoma and can be used for tumor and normal diagnostic determination. 
In addition, the calculation results of TCGA-LUAD identified 21 DE tRDFs including 12 5’-tRDRs and 9 3’-tRDFs. When comparing the candidates with GEO, six tRDFs (5P_tRNA-Gly-TCC-1-1, 5a_tRF-Ile-AAT/GAT, 3P_tRNA-Arg-TCG-1-1, and 3P_tRNA-Arg-TCT-4-1, 5P_tRNA-Asn-GTT-2-3, 5a_tRF-Asp-GTC) in TCGA-LUAD were found overlapping with 11 DE tRDFs candidates from the independent validation by random forest models, which was referred to as a signature to be diagnostic biomarkers (H). 
We also tested the diagnostic ability of six tRDFs signatures with the same training and validation datasets in five combinations in descending order from six signatures to two signatures (5a_tRF-Ile-AAT/GAT and 5P_tRNA-Gly-TCC-1-1), the results exhibited excellent diagnostic value of tRDFs that combined in groups as AUCs are more than 0.87, sensitivity and specificity are all above 0.77. The best performance of grouped tRDF is the combination of 3P_tRNA-Arg-TCG-1-1, 3P_tRNA-Arg-TCT-4-1, 5a_tRF-Ile-AAT/GAT and 5P_tRNA-Gly-TCC-1-1, presenting AUC as 0.91 (I). We then tested the diagnostic value of individual signatures, however, the identification ability showed lower accuracy compared with grouped tRDFs. 5a_tRF-Ile-AAT/GAT exhibited best performance that AUC is 0.786, while 5a_tRF-Asp-GTC has the worst accuracy among all signature with 0.587 AUC.



{% include figure.liquid
  path="/assets/img/tRDF/figure2.png"
  class="img-fluid rounded z-depth-1"
  alt="Differential expression and validation of tRDF signatures across GEO and TCGA cohorts"
%}

(A and B) Heatmaps show DE tRDFs in two GEO datasets with paired tumor and normal samples. Up- and downregulated tRDFs separate by unsupervised clustering.  
(C and D) Boxplots show 11 tRDFs identified as common DE across GEO datasets (p < 0.05).  
(E) Correlogram shows Pearson correlations among the 11 DE tRDFs.  
(F and G) AUCs show independent validation results in GEO and TCGA-LUAD.  
(H) Expression of six DE tRDFs in TCGA-LUAD.  
(I) Diagnostic performance of six-tRDF signature across five independent validations.

---

## Plasma validation in NSCLC patients and healthy donors
**Highlight:** Plasma TPM expression supports diagnostic utility of selected tRDFs.

To validate the diagnostic value of 11 tRDFs candidates on LUAD patients, we collected blood samples from 50 patients and 60 healthy controls and performed small RNA sequencing. After the same upstream and downstream analysis, six tRDFs can be identified. We compared the tRDFs expression level between tumor and healthy samples. The results showed that two tRDFs, 3P_tRNA-Arg-TCG-1-1 and 5P_tRNA-Asn-GTT-2-3 had significant differences between two groups (B, E). 
No statistical differences can be identified among the rest of the four tRDFs. However, the expression pattern of tRDF can still be evaluated, as the trend of expression in two types of samples have the same performance in GEO and TCGA-LUAD. In the group of upregulated tRDFs, the 3P_tRNA-Ser-GCT-6-1 in tumor samples showed higher expression than the normal sample. On the other hand, three downregulated tRDFs (3P_tRNA-SeC-TCA-1-1, 3P_tRNA-Val-TAC-1-1 and 5b_tRF-Tyr-GTA) are all highly expressed in normal samples. 


{% include figure.liquid
  path="/assets/img/tRDF/figure3.png"
  class="img-fluid rounded z-depth-1"
  alt="Plasma validation of tRDF expression between NSCLC patients and healthy donors"
%}


3P_tRNA-Ser-GCT-6-1 (A), 3P_tRNA-Arg-TCG-1-1 (B), 3P_tRNA-SeC-TCA-1-1 (C), 3P_tRNA-Val-TAC-1-1 (D), 5P_tRNA-Asn-GTT-2-3 (E), and 5b_tRF-Tyr-GTA (F).  
*p ≤ 0.05, **p ≤ 0.01, ns = not significant.*



---
## Immune infiltration and tumor microenvironment correlated with tRDFs

Currently, no studies have conducted association between tRDFs and TME-infiltrating immune cells, therefore, we used CIBSORT methods to further understand the functional role of tRDFs in TME-infiltrating immune cells. 35 tRDFs were associated with tumor immune microenvironment (TIME) cell infiltration with correlation coefficient over 0.1 or less than -0.1. For example, 5P_tRNA-Thr-CGT-4-1 correlated with Dendritic cells activated (R=0.29), 3b_tRF-Leu-CCA/CGA correlated with T cells follicular helper (R=0.24), and 5b_tRF-Tyr-GTA(R=0.200) linked with T cells CD4 memory activated. T cells CD4 memory activated had the most link with tRDFs. 
Differences in TIME cell infiltration between two types of tRDFs were also analyzed; 14 immune cells were found in common between two types of tRDFs. We noticed 5’-tRDFs were strongly positively correlated with T cells CD8, and T cells CD4 memory activated. Both 5’-tRDFs and 3’-tRDFs had positive link with dendritic cells resting (A). Three 5’-tRDFs had negative association with neutrophils while 3P_tRNA-Arg-CCG-1-3 had positive correlation. Four 3’-tRDFs were positively correlated with Macrophages M0. In order to explore any prognostic value of tRDFs that combined with immune infiltration, we conducted survival analysis based on prognostic related tRDFs we analyzed by all stages, early stages and advanced stages from TCGA-LUAD cohorts (3P_tRNA-Arg-CCT-3-1, 3P_tRNA-SeC-TCA-1-1, 5P_tRNA-Ala-TGC-3-1, 3b_tRF-Leu-CCA/CGA, 3P_tRNA-Ser-TGA-1-1, 5P_tRNA-Phe-GAA-1-5, 5c_tRF-Pro-AGG/TGG and 5P_tRNA-Arg-CCG-2-1). 13 types of immune cells were found to be correlated with all tRDFs except 5c_tRF-Pro-AGG/TGG. Survival analysis was based on all stage patients among 13 immune cells, and only plasma cell that correlated with 3P_tRNA-Arg-CCT-3-1 (R= -0.1) was identified to be significant related to overall survival (B). 
	We also characterized the functional role of tRDFs that highly correlated with immune infiltration-related genes. We identified 100 immune-related genes from LM22 that were correlated with 30 tRDFs. The enrichment analysis results presented that these genes were enriched in biological processes, particularly those related to B cell proliferation, activating cell surface receptor signaling pathway, and activating signal transduction. Immune receptor activity, cytokine activity, signaling receptor activator activity are specific immune-related gene that enriched in molecular function. 
According to the results of KEGG pathway enrichment, there are 20 tRDFs correlated genes were identified to be enriched in signaling pathways such as cytokine-cytokine receptor interaction, chemokine signaling pathway, and T cell receptor signaling pathway (C). Only one tRDFs signature was detected among 20 tRDFs, 3P_tRNA-Arg-TCT-4-1 is identified as targeting in Cytokine-cytokine receptor interaction, viral protein interaction with cytokine-cytokine receptor and chemokine signaling pathway. Besides the signature, we also noticed three tRDFs, tRNA-Ala-TGC-3-1, tRNA-Arg-CCG-2-1, and 3b_tRF-Leu-CCA/CGA that demonstrated association with prognosis were enriched in some immune-related signaling pathways. For example, tRNA-Ala-TGC-3-1, identified as correlated with all stage and early-stage patient survival outcome in LUAD cohorts were correlated in T cell receptor signaling pathway, which may indicate some links of tRDFs prognosis with possible immune therapy.
	We finally conducted correlation analysis based on four immune checkpoints: CD274 (PD-L1), CD80, CD86 and CTLA4. The correlation with 10 tRDFs were identified (D). 5P_tRNA-Gln-TTG-1-1 had the most negative correlation with three checkpoints including CTLA4, CD80 and CD86. 5a_tRF-Cys-GCA, 3P_tRNA-Ser-GCT-6-1, 3P_tRNA-Thr-CGT-4-1, 3P_tRNA-Arg-TCT-4-1 and 5P_tRNA-Trp-CCA-3-3 were five tRDFs that correlated with CD274. 


{% include figure.liquid
  path="/assets/img/tRDF/figure7.png"
  class="img-fluid rounded z-depth-1"
  alt="Plasma validation of tRDF expression between NSCLC patients and healthy donors"
%}

(A) Bar plot shows the correlation between tRDFs and TIME cell infiltration evaluated by Pearson correlation. The length of column indicates the correlation; immune cells were selected from the mutual correlation with 5ʹ-tRDFs and 3ʹ-tRDFs. (B) Kaplan-Meier curves show overall survival of plasma cells that correlated with prognostic tRDFs. Red color indicates the high abundance of plasma cells, and blue color indicates the low abundance of plasma cells. (C) Network shows the tRDF-targeted immune-related signaling pathways in TCGA-LUAD cohort, including primary immunodeficiency, viral protein interaction with cytokine and cytokine receptor, cytokine-cytokine receptor interaction, hematopoietic cell lineage, T cell receptor signaling pathway, and the other signaling pathway. IgA, immunoglobulin A. (D) The correlation between tRDF with immune checkpoint CD274 (PD-L1), CTLA4, CD80, and CD86.
