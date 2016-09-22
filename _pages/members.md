---
layout: archive
title: "Members"
permalink: /members/
author_profile: false
sidebar:
  nav: "docs"
---

{% include base_path %}

<div class="grid__wrapper">
  {% for post in site.members %}
    {% include member-single.html type="grid" %}
  {% endfor %}
</div>
