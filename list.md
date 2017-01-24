---
layout: null
---
<style>
table, th, td {
    border: 1px solid black;
    border-collapse: collapse;
}
th, td {
    padding: 5px;
}
th {
    text-align: left;
}
</style>
<body>
<table style="width:100%">
  <tr>
    <th>Page Url</th>
    <th>Redirect</th> 
  </tr>

{% if site.href %}
<tr>
    <th><a href="{{ site.url }}{{ page.url }}">Default</a></th>
    <th>{{ site.href }}</th>
  </tr>
{% endif %}
{% for page in site.pages %}
{% if page.href %}
<tr>
    <th>[{{ site.url }}{{ page.url }}]({{ site.url }}{{ page.url }})/th>
    <th>{{ page.href }}</th>
  </tr>
{% endif %}
{% endfor %}
</table>
</body>
