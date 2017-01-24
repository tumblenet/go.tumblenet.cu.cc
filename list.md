---
layout: default
title: list
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
<table style="width:100%">
  <tr>
    <th>Page Url</th>
    <th>Redirect</th>
    
  </tr>

{% if site.href %}
<thead>
<tr>
    <th>
        {% unless site.href == site.comingSoon %}<a href="{{ site.url }}">{% endunless %}
            Default
        {% unless site.href == site.comingSoon %}</a>{% endunless %}
    </th>
    <th>
    {% if site.href == site.comingSoon %}
    Coming Soon
    {% else %}
        {{ site.href }}
    {% endif %}
    </th>
  </tr>
  </thead>
{% endif %}
<thbody>
{% for item in site.pages %}
{% if item.href %}

<tr>
    <td>
        {% unless item.href == site.comingSoon %}<a href="{{ site.url }}{{ item.url }}">{% endunless %}
            {{ site.url }}{{ item.url }}
        {% unless item.href == site.comingSoon %}</a>{% endunless %}
    </td>
    <td>
    {% if item.href == site.comingSoon %}
    Coming Soon
    {% else %}
        {{ item.href }}
    {% endif %}
    </td>
  </tr>
{% endif %}
{% endfor %}
</tbody>
</table>
