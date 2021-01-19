---
layout: page
title: Labs
img: code.jpg # Add image post (optional)
permalink: labs
sidebar: true
---

---

{% if site.data.code %}
## Labs 
{% for script in site.data.code %}
* [**{{script.name}}**](https://colab.research.google.com/github/shih-lab/BIS198/blob/main/software/{{script.name}})
  \| {{script.desc}}
{% endfor %}
{% endif %}

{% if site.data.datasets %}
## Data Sets
{% for ds in site.data.datasets %}
* [{{ds.name}}]({%if ds.storage !=
  'remote'%}{{site.url}}/{{site.baseurl}}/datasets/{{ds.link}}{%
  else%}{{site.link}}{% endif %}) \| {% if ds.filetype %}(filetype:
  {{ds.filetype}}){%endif%}{% if ds.filesize %}({{ds.filesize}}){%endif%}{%
  if ds.storage == remote %} DOI: {{ds.DOI}}{%endif%}
{% endfor %}
{% endif %}
