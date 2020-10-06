---
title: /
layout: home
permalink: /
---
<html lang="{{ page.lang | default: site.lang | default: "en" }}">

  {%- include head.html -%}
 
 {% for post in site.posts %}
  <article>
    <h2>
      <a href="{{ site/post.url }}">
        {{ post.title }}
      </a>
    </h2>
    <time datetime="{{ post.date | date: "%Y-%m-%d" }}">{{ post.date | date_to_long_string }}</time>
    {{ post.content }}
  </article>
  
{% endfor %}

