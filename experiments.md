---
title: Experiments
layout: default
---

## Experiments

<style>
    .manifestlink { padding-left: 2em; }
</style>
{% for manifest in site.data.manifests %}

{% capture manifesturl %}
    {{ site.url }}{{ site.baseurl }}/manifests/{{ manifest.filename }}
{% endcapture %} 

<h3>{{ forloop.index }}. {{ manifest.title }}</h3>

<div class="links">
<a href="{{ manifesturl | strip }}">{{ manifesturl | strip }}</a><br/>
<span class="manifestlink">&gt; <a href="http://universalviewer.io/uv.html?manifest={{ manifesturl | strip | url_encode }}">Universal Viewer</a></span>
<span class="manifestlink">&gt; <a href="{{ site.url }}{{ site.baseurl }}/?manifest={{ manifesturl | strip | url_encode }}">Mirador</a></span>
</div>

<div class="description">{{ manifest.description | markdownify }}</div>

{% endfor %}

