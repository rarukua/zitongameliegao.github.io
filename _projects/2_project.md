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
 
<div class="row">
    <div class="col-md-4">
        {% include figure.liquid loading="eager" path="assets/img/piTPI/figure2.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    
</div>
<div class="caption">
    Caption photos easily. On the left, a road goes through a tunnel. Middle, leaves artistically fall in a hipster photoshoot. Right, in another hipster photoshoot, a lumberjack grasps a handful of pine needles.
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    This image can also have a caption. It's like magic.
</div>

You can also put regular text between your rows of images.
Say you wanted to write a little bit about your project before you posted the rest of the images.
You describe how you toiled, sweated, _bled_ for your project, and then... you reveal its glory in the next row of images.

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    You can also have artistically styled 2/3 + 1/3 images, like these.
</div>

The code is simple.
Just wrap your images with `<div class="col-sm">` and place them inside `<div class="row">` (read more about the <a href="https://getbootstrap.com/docs/4.4/layout/grid/">Bootstrap Grid</a> system).
To make images responsive, add `img-fluid` class to each; for rounded corners and shadows use `rounded` and `z-depth-1` classes.
Here's the code for the last row of images above:

{% raw %}

```html
<div class="row justify-content-sm-center">
  <div class="col-sm-8 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="col-sm-4 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
```

{% endraw %}
