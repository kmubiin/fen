---
published: true
title: debug.md
---

Defined links are:  
site.url: <span class="code">{{ site.url }}</span>  
site.baseurl: <span class="code">{{ site.baseurl }}</span>  
page.url: <span class="code">{{ page.url }}</span>  

Link made by site.url, site.baseurl, page.url:  
[{{ site.url }}{{ site.baseurl }}{{ page.url }}]({{ site.url }}{{ site.baseurl }}{{ page.url }})  

Link made by site.baseurl and page.url:  
[{{ site.baseurl }}{{ page.url }}]({{ site.baseurl }}{{ page.url }})  

Link made by page.url only:  
[{{ page.url }}]({{ page.url }}) (need `jekyll-relative-link`
plugin outside localhost)

Link made by link tag and page.path:  
{% link {{ page.path }} %} (need Jekyll 4.0+ without baseurl)  
{% link {{ site.baseurl }}{{ page.path }} %}
