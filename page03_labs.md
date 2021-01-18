---
layout: page
title: Labs
img: code.jpg # Add image post (optional)
permalink: labs
sidebar: true
---

---

To run a lab on Google colaboratory:

1. Download the `.ipynb` file for the lab `right-click` --> `save link as` 
2. Open a new instance of Colaboratory ([link here](https://colab.research.google.com/notebooks/intro.ipynb))
3. Goto `File` --> `Upload Notebook`
4. Click `Browse` and upload the downloaded `.ipynb` lab to run your own private instance of the notebook

{% if site.data.code %}
## Labs 
{% for script in site.data.code %}
* [**{{script.name}}**]({{site.url}}/{{site.baseurl}}/software/{{script.name}})
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
