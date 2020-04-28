---
layout: page
---

{% assign path = page.url |split: "/" %}
{% assign category = path[1] %}

{% capture index %}{% include content-index.md group=category %}{% endcapture %}
{{ index | markdownify }}


{{ content }}