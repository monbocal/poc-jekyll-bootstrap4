---
layout: default
title: Home
permalink: /
sections:
  - 00-jumbotron
  - 01-three-cols
---

{% for section in page.sections %}
  {% capture target %}/sections/fr/00-home/{{ section }}{% endcapture %}
  {% assign this_section = site.sections | where: "id", target | first %}
  {% assign target-design = this_section.design %}
  {% include {{ this_section.design }} section = this_section %}
{% endfor %}
