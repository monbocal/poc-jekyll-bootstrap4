---
layout: default
title: Home
permalink: /en/
sections:
  - 00-jumbotron
  - 01-three-cols
---

{% for section in page.sections %}
  {% capture target %}/sections/{{ page.lang }}/00-home/{{ section }}{% endcapture %}
  {% assign this_section = site.sections | where: "id", target | first %}
  {% assign target-design = this_section.design %}
  {% include {{ this_section.design }} section = this_section %}
{% endfor %}
