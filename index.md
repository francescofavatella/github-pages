<ul>
  {% for page in site.folder1 %}
    <li>
      <a href="{{ page.url | relative_url }}">{{ page.title }}</a>
    </li>
  {% endfor %}

{% for page in site.pages %}
<li>
<a href="{{ page.url | relative_url }}">{{ page.title }}</a>
</li>
{% endfor %}

</ul>
