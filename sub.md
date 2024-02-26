---
published: true
title: sub.md
layout: manual
---

Prepare a markdown file with front matter.

Try Liquid code at here instead:
{% if site.title %}
Title is <span class="code">{{ site.title }}</span>
{% else %}
Title not found
{% endif %}

Generated <span class="code">{{ site.time }}</span>
