---
layout: archive
title: "Teaching"
permalink: /teaching/
author_profile: true
---

{% include base_path %}
> PDF version of my CV can be found [here](/files/ASIC_Design.pdf).

{% for post in site.teaching reversed %}
  {% include archive-single.html %}
{% endfor %}
