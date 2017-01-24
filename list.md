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
<table class="mdl-data-table mdl-js-data-table mdl-data-table--selectable mdl-shadow--2dp">

<thead>
  <tr>
    <th>Page Url</th>
    <th>Redirect</th>
    
  </tr>
  
  </thead>
<tbody>
{% if site.href %}
<tr>
    <td>
        {% unless site.href == site.comingSoon %}<a href="{{ site.url }}">{% endunless %}
            Default
        {% unless site.href == site.comingSoon %}</a>{% endunless %}
    </td>
    <td>
    {% if site.href == site.comingSoon %}
    Coming Soon
    {% else %}
        {{ site.href }}
    {% endif %}
    </td>
  </tr>
{% endif %}
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
