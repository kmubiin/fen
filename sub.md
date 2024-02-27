---
published: true
title: sub.md
layout: manual
---

Prepare a markdown file with front matter.  
Then, try Liquid code at here instead:

Title is <span class="code">{% if site.theme %}
{{ site.title }}{% else %}empty{% endif %}</span>.
 
Theme is <span class="code">{% if site.theme %}
{{ site.theme }}{% else %}empty{% endif %}</span>.
