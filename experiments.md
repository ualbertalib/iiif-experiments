---
title: Experiments
layout: default
---

## Experiments

{% for manifest in site.data.manifests %}

{% capture manifesturl %}
    {{ site.url }}{{ site.baseurl }}/manifests/{{ manifest.filename }}
{% endcapture %} 

<h3>{{ forloop.index }}. {{ manifest.title }}</h3>

[{{ manifesturl | strip }}]({{ manifesturl | strip }})<br/>
&gt; <a href="http://universalviewer.io/uv.html?manifest={{ manifesturl | strip | url_encode }}">Universal Viewer</a>

{% endfor %}

