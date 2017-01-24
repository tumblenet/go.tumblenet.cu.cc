---
layout: null
---
<body>
{% if site.href %}
<p><a href="{{ site.url }}">Default</a> ==> {{ site.href }}</p>
{% endif %}
{% for page in site.pages %}
{% if page.href %}
<p><a href="{{ page.url }}">{{ site.url }}{{ page.url }}</a> ==> {{ page.href }}</p>
{% endif %}
{% endfor %}
</body>
