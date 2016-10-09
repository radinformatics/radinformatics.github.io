---
title: "Deep learning"
layout: single
sitemap: true
permalink: /deep-learning/
author_profile: false
sidebar:
  nav: "docs"
---

{% include base_path %}
{% include group-by-array collection=site.projects field="categories" %}

## Goals
Deep learning introduces a family of powerful algorithms that can help to discover features of disease in medical images, and assist with decision support tools. In the context of medical imaging, there are several interesting challenges:

### Challenges

 - ~1500 different imaging studies
   - Many distinct imaging modalities (e.g., DR, CT, MR, US, NM)
   - Visualizing a variety of body regions (e.g., head, chest, extremities, abdomen)
   - Each containing dozens of organs and body parts (e.g., liver, pancreas, kidney)
   - Each affected by hundreds of diseases (Total: ~23,000 conditions)
 - Typically 12- or 16-bit gray scale, rather than color images. 
 - 3D volumetric data sets, sometimes time as 4th dimension.
 - Multi-channel data (e.g., MR T1-weighing, T2-weighting, flow-sensitive, post-contrast).  
 - Differential diagnosis varies by anatomic structure, requiring anatomic segmentation.

These challenges are further complicated by the sheer size of the data that is available at Stanford Medicine (2016):

<figure class="align-left">
  <img src="/images/projects/deep-learning/radiology-data-2016.png"/>
</figure> 

### Projects

The Langlotzlab has several projects that are testing these algorithms to assist with tasks relevant to diagnostic radiology:

{% for category in group_names %}
  {% assign posts = group_items[forloop.index0] %}
  {% if category == "deep-learning" %}
    {% for post in posts %}
<a href="{{ base_path }}{{ post.url }}" rel="permalink">{{ post.title }}</a>
    {% endfor %}
  {% endif %}
{% endfor %}
