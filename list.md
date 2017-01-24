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
    <th>
        {% unless site.href == site.comingSoon %}<a href="{{ site.url }}">{% endunless %}
            Default
        {% unless site.href == site.comingSoon %}</a>{% endif %}
    </th>
    <th>
    {% if site.href == site.comingSoon %}
    Coming Soon
    {% else %}
        {{ site.href }}
    {% endif %}
    </th>
  </tr>
{% endif %}
{% for item in site.pages %}
{% if item.href %}
<tr>
    <th>
        {% unless item.href == site.comingSoon %}<a href="{{ site.url }}{{ item.url }}">{% endunless %}
            {{ site.url }}{{ item.url }}
        {% unless item.href == site.comingSoon %}</a>{% endif %}
    </th>
    <th>
    {% if item.href == site.comingSoon %}
    Coming Soon
    {% else %}
        {{ item.href }}
    {% endif %}
    </th>
  </tr>
{% endif %}
{% endfor %}
</table>
</body>
