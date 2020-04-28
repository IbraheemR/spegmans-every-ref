
<div class="ref-index" markdown="1">

{% assign group = include.group |default: "all" %}


{% for cat in site.categories %}
{% if group == "all" or cat.category_id == group %}
{% if group == "all" %}
- ## [{{cat.title}}]({{cat.url}})
{% endif %}

{% for page in {{site.content | where:"category",cat.category_id }} %}
{% if page.category == cat.category_id %}
  - [{{page.title}}]({{page.url}})
{% endif %}
{% endfor %}

{% endif %}
{% endfor %}

</div>

<hr />

