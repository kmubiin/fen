---
published: true
title: main.md
---

Theme is <span class="code">{% if site.theme %}
{{ site.theme }}{% else %}empty{% endif %}</span>.

Layout is <span class="code">{% if page.layout %}
{{ page.layout }}{% else %}empty{% endif %}</span>.

Test link:  
[Go to sub (relative)](sub.md) (requires plugin)  
[Go to sub]({% link sub.md %}) (requires Liquid tag)

Test static link:  
[Go to index](index.html)
