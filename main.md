---
published: true
title: main.md
---

Theme is <span class="code">{% if site.theme %}
{{ site.theme }}{% else %}empty{% endif %}</span>.

Layout is <span class="code">{% if page.layout %}
{{ page.layout }}{% else %}empty{% endif %}</span>.

Test relative link: [Go to sub](sub.md)

Test static link: [Go to index](index.html)
