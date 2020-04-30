---
layout: page
---

{{ content }}

{% capture index %}{% include content-index.md group=page.category_id %}{% endcapture %}
{{ index | markdownify }}


