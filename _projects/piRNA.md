---
layout: page
title: Novel non-small cell lung cancer(NSCLC) diagnosis panel from small RNA (piRNA)
description: piTPI risk score for early-stage NSCLC
img: assets/img/piTPI/graphical_abstract.jpg
importance: 2
category: work
giscus_comments: true
---

Non-small cell lung cancer (NSCLC) is a lethal cancer and lacks robust biomarkers for non-invasive clinical diagnosis. Detecting NSCLC at the early stage can decrease the mortality rate and minimize harm caused by various treatments. We curated 2,050 samples from public tissue and plasma datasets including both invasive and non-invasive types, then supplemented with in-house pooled plasma and exosome samples. Eleven independent transcriptome datasets were utilized to develop a new machine learning model by integrating PIWI-interacting RNA (piRNA) to predict NSCLC. Five piRNA signatures derived from ribosomal subunits identified to be tumor-specific exhibited robust diagnostic ability and were combined into a piRNA-Based Tumor Probability Index (pi-TPI) risk evaluation model. pi-TPI effectively distinguished NSCLC patients from healthy individuals and showed efficacy in identifying early-stage cancers with Area under the ROC Curve (AUC) values over 0.80. Plasma cohorts exhibited the diagnosis efficacy of pi-TPI with an AUC value of 0.85. Experimental exosomal data enhances the accuracy of diagnosing non-cancerous, benign, and cancer cases. The pi-TPI marker in the non-cancer/cancer subgroup exhibited superior predictive performance with an AUC value of 0.96. These findings underscore the significant clinical potential of the five piRNA signatures as a powerful diagnostic tool for NSCLC, particularly of non-invasive cancer diagnostics.

{% include figure.liquid
  path="assets/img/piTPI/figure1.jpg"
  class="img-fluid rounded z-depth-1"
  alt="Graphical abstract of the pi-TPI model for NSCLC diagnosis"
%}

Diagnostic panel consisting of five piRNAs regarded as piRNA Base Tumor Probability Index (pi-TPI) exhibited high distinguish ability between cancer and non-cancer groups. 

{% include figure.liquid
  path="assets/img/piTPI/figure2.png"
  class="img-fluid rounded z-depth-1"
  alt="Graphical abstract of the pi-TPI model for NSCLC diagnosis"
%}
 
