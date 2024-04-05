---
published: true
title: sub.md
---

Theme is <span class="code">{% if site.theme %}
{{ site.theme }}{% else %}empty{% endif %}</span>.

Layout is <span class="code">{% if page.layout %}
{{ page.layout }}{% else %}empty{% endif %}</span>.

Test link:  
[Go to main (relative)](main.md) (requires plugin)  
[Go to main]({% link main.md %}) (requires Liquid tag)
