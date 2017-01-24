---
layout: null
---
<body>
{% if site.href %}
<p><a href="{{ site.href }}">Default ==> {{ site.href }}</a></p>
{% endif %}
{% for page in site.pages %}
{% if page.href %}
<p><a href="{{ page.url }}">{{ site.url }}{{ page.url }} ==> {{ page.href }}</a></p>
{% endif %}
{% endfor %}
</body>
