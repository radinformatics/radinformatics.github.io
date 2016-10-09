---
title: "Machine learning"
layout: single
sitemap: true
permalink: /machine-learning/
author_profile: false
sidebar:
  nav: "docs"
---

{% include base_path %}
{% include group-by-array collection=site.projects field="categories" %}

## Goals
Machine learning introduces a framework that can help with everything from automated diagnosis to information extraction and organization. The Langlotzlab has a series of projects that work with medical images and or data, and the following are a few high level examples of what machine learning can offer...

 - diagnostic features, sometimes with human interpretability
 - dimensionality reduction of images and reports
 - generalization across modalities and body parts

For example, a standard pipeline for an "automated radiologist" might aim to use annotations of radiologist reports with a supervised algorithm to intelligently summarize the report, and possibly provide real-time decision support for radiologists:

<figure class="align-left">
  <img src="/images/projects/informatics/info-extraction.png"/>
</figure> 

You might also want to distinguish different components of images, as is nicely illustrated in the images below:

<figure class="align-left">
  <img src="/images/projects/machine-learning/machine-learning-haha.png"/>
</figure> 

### Projects

{% for category in group_names %}
  {% assign posts = group_items[forloop.index0] %}
  {% if category == "machine-learning" %}
    {% for post in posts %}
<a href="{{ base_path }}{{ post.url }}" rel="permalink">{{ post.title }}</a>
    {% endfor %}
  {% endif %}
{% endfor %}
