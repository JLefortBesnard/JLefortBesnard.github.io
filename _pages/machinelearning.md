---
layout: archive
permalink: /machine-learning/
title: "Machine Learning Posts"
author_profile: true
header:
  image: "/images/ml.jpeg"
---

# First Ph.D. project

The overwhelming majority of mental disorders show disturbance in the default mode network (DMN). Yet, mental disorders with diverging clinical phenotypes are unlikely to be caused by an identical pathophysiological mechanism. Our study resolves previous inconsistencies on network disruption in schizophrenic patients by delineating aberration of top-level DMN control on subordinate multi-modal networks using meta-analytic atlases and pattern-learning algorithms in a large multi-site dataset (n=325).

![DMN subregions](/images/dmn.png)


We find that DMN activity does not obey the neuroanatomical boundaries of Brodmann's 100-year-old cytoarchitectonic atlas. We therefore deploy detailed topographical definitions using a recently completed DMN subnode atlas. We hypothesized that many prior inconsistencies in DMN findings can be explained by the reliance on simple linear correlations between node pairs. We therefore exploited novel machine-learning techniques that are able to incorporate all node-node relations, thereby accounting for third-party influences on each coupling relation. Our methodology further enabled quantifying the structure-function correspondence by analogous analyses on resting-state connectivity fluctuations and brain volume variability.


This systems neuroscience approach reveals that the backbone of the DMN does not drive brain dysfunction in schizophrenia.


![Aberrant structural covariation and dysfunctional connectivity across network in schizophrenia](/images/results.png)


Instead, our results highlight dysregulated coupling between the highly associative DMN and the multi-modal dorsal attention (DAN) and saliency (SN) networks. Distinct disease mechanisms were identified by structural covariation analyses emphasizing aberrant DMN-SN coupling, whereas functional covariation analyses emphasized aberrant DMN-DAN coupling. Our computational investigation at increased spatial resolution proposes targeting the DMN in relation to other canonical networks to approach a future of personalized medicine in psychiatry.


*"Different shades of the default mode in schizophrenia, subnodal covariance estimation
in structure and function"*
[Link](https://onlinelibrary.wiley.com/doi/abs/10.1002/hbm.23870)

{% include base_path %}
{% include group-by-array collection=site.posts field="tags" %}

{% for tag in group_names %}
  {% assign posts = group_items[forloop.index0] %}
  <h2 id="{{ tag | slugify }}" class="archive__subtitle">{{ tag }}</h2>
  {% for post in posts %}
    {% include archive-single.html %}
  {% endfor %}
{% endfor %}
