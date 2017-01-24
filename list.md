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
    <th><a href="{{ site.url }}">Default</a></th>
    <th>{{ site.href }}</th>
  </tr>
{% endif %}
{% for item in site.pages %}
{% if item.href %}
<tr>
    <th><a href="{{ site.url }}{{ item.url }}">{{ site.url }}{{ item.url }}</a></th>
    <th>{{ item.href }}</th>
  </tr>
{% endif %}
{% endfor %}
</table>
</body>
