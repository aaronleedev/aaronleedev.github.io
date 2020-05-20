---
layout: page
title: Posts
subtitle: 
---

{% for category in site.categories %}
  {% capture cat %}{{ category | first }}{% endcapture %}
  {% for desc in site.descriptions %}
    {% if desc.cat == cat %}
  <h2 id="{{cat}}" style="color: {{ desc.catcolor }}">{{ cat | capitalize }}</h2>
  <p class="desc" style="margin: -4px 0px 12px 10px;font-size: 18px;font-weight: bold;color: {{ desc.desccolor }}">{{ desc.desc }}</p>
    {% else %}
  <h2 id="{{cat}}" style="">{{ cat | capitalize }}</h2>
    {% endif %}
  {% endfor %}
  <ul class="posts-list">
  {% for post in site.categories[cat] %}
    <li>
      <strong>
        <a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
      </strong>
      <span class="post-date">- {{ post.date | date_to_long_string }}</span>
    </li>
  {% endfor %}
  </ul>
  {% if forloop.last == false %}<hr>{% endif %}
{% endfor %}
<br>
