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
[Go to sub 1]({% link sub.md %}) (link tag)
[Go to sub 2]({{ site.baseurl }}{% link sub.md %}) (link
tag, with baseurl workaround)

Test static link:  
[Go to index](index.html)
