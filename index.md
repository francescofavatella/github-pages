<ul>
  {% for page in site.folder1 %}
    <li>
      <a href="{{ page.url | relative_url }}">{{ page.title }}</a>
    </li>
  {% endfor %}

{% for page in site.pages %}
{% unless page.title == nil %}

<li>
<a href="{{ page.url | relative_url }}">{{ page.title }}</a>
</li>
{% endunless %}
{% endfor %}

</ul>

{% for collection in site.collections %}

  <h2>Items from {{ collection.label }}</h2>
  <ul>
    {% for item in site[collection.label] %}
      <li><a href="{{ item.url | relative_url }}">{{ item.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}
