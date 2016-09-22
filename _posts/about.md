---
title: "About"
layout: archive
sitemap: false
permalink: /about
author_profile: false
sidebar:
  nav: "docs"
---

{% include base_path %}

<div class="grid__wrapper">
  {% for post in site.portfolio %}
    {% include archive-single.html type="grid" %}
  {% endfor %}
</div>
