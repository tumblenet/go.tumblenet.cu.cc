---
layout: null
---
<body>
{% for page in site.pages %}
{% if page.href %}
<p>{{ site.url }}{{ page.url }} ==> {{ page.href }}</p>
{% endif %}
{% endfor %}
</body>
