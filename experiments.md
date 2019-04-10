---
title: Experiments
layout: default
---

## Experiments

{% for manifest in site.data.manifests %}
<h3>{{ forloop.index }}. {{ manifest.title }}</h3>

[{{ site.url }}{{ site.baseurl }}/manifests/{{ manifest.filename }}]({{ site.url }}{{ site.baseurl }}/manifests/{{ manifest.filename }})
{% endfor %}

