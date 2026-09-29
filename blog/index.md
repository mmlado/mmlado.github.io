---
layout: default
title: Writing
description: Posts by Mladen Milankovic (mmlado), walleteer.
---

<p class="tag"><a href="/">mmlado</a> - <span class="sc">walleteer</span></p>

# Writing

{% for post in site.posts -%}
- [{{ post.title }}]({{ post.url }}), {{ post.date | date: "%-d %B %Y" }}<br>
  {{ post.subtitle }}
{% endfor %}
