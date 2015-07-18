---
layout: page
title: Archive
permalink: /archive/
---

{% for post in site.posts %}
  {% assign curr_post_date = post.date | date: "%B %Y" %}
  {% assign next_post_date = post.next.date | date: "%B %Y" %}
  
  {% if curr_post_date != next_post_date %}<h2>{{ curr_post_date }}</h2>
  {% endif %}

  <p>
    <a href="{{ post.url | prepend:site.baseurl }}">{{ post.title }}</a>
    <small>{{ post.date | date_to_string }}</small>
  </p>
{% endfor %}