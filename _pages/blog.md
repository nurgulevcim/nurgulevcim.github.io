---
title: "Blog"
layout: single
permalink: /blog/
author_profile: false
---

## Ekonomi

{% assign ekonomi_posts = site.categories.Ekonomi | sort: "date" | reverse %}

{% for post in ekonomi_posts %}
- [{{ post.title }}]({{ post.url }})
  <small>{{ post.date | date: "%d %B %Y" }}</small>
{% endfor %}

---

## Piyasa Araştırmaları

{% assign piyasa_posts = site.categories.Piyasa_Arastirmalari | sort: "date" | reverse %}

{% for post in piyasa_posts %}
- [{{ post.title }}]({{ post.url }})
  <small>{{ post.date | date: "%d %B %Y" }}</small>
{% endfor %}
