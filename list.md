---
layout: null
---
<body>
<table style="width:100%">
  <tr>
    <th>Page Url</th>
    <th>Redirect</th> 
  </tr>

{% if site.href %}
<tr>
    <th><a href="{{ site.url }}">Default</a></th>
    <th>{{ site.href }}</th>
  </tr>
{% endif %}
{% for page in site.pages %}
{% if page.href %}
<tr>
    <th><a href="{{ page.url }}">{{ site.url }}{{ page.url }}</a></th>
    <th>{{ page.href }}</th>
  </tr>
{% endif %}
{% endfor %}
</table>
</body>
