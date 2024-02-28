---
published: true
title: sub.md
---

Prepare a markdown file with front matter.  
Then, try Liquid code at here instead:

Title is <span class="code">{% if site.theme %}
{{ site.title }}{% else %}empty{% endif %}</span>.
 
Theme is <span class="code">{% if site.theme %}
{{ site.theme }}{% else %}empty{% endif %}</span>.

Layout is <span class="code">{% if page.layout %}
{{ page.layout }}{% else %}empty{% endif %}</span>.

Test relative link: [Return to index](index.md)
