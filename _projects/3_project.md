---
layout: page
title: Comprehensive landscape of tRNA-derived fragments in lung cancer
description: tDRF and its potential in lung cancer
img: assets/img/tRDF/graphical_abstract.jpg
importance: 3
category: work
---

tRNA-derived fragment (tRDF) is novel small non-coding RNA that presences in different types of cancer. The comprehensive understanding of tRDFs in non-small cell lung cancer remains largely unknown. In this study, 1550 patient samples of NSCLC were included, and 52 tRDFs with four subtypes were identified. Six tRDFs were picked as diagnostic signatures based on the tRDFs expression patterns, and under the curve (AUC) in independent validations is up to 0.90. Two signatures were validated successfully in plasma samples, and six signatures were confirmed the consistency of distinguished expression in NSCLC cell lines. Ten tRDFs along with independent risk scores can be used to predict survival outcomes by stages, 5a_tRF-Ile-AAT/GAT can be prognosis biomarker for early stage. Association analysis of tRDFs signatures correlated mRNAs and miRNA were targeted to the cell cycle and oocyte meiosis signaling pathways. Five tRDFs were assessed to associate with PD-L1 immune checkpoint and correlated with the genes that targets in PD-L1 checkpoint signaling pathway. Our study is the first to provide a comprehensive analysis of tRDFs in lung cancer including four subtypes of tRDFs, investigating the diagnostic and prognostic values, and demonstrated their biological function and transcriptional role as well as potential immune therapeutic value. 

{% include figure.liquid
  path="assets/img/tRDF/tsRNA_common_Page_1.png"
  class="img-fluid rounded z-depth-1"
  alt="Significantly expressed tRDF identified in lung cancer and healthy samples"
%}

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/1.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/3.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
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
