---
published: true
title: debug.md
---

Defined variables are:  
site.url: <span class="code">{{ site.url }}</span>  
site.baseurl: <span class="code">{{ site.baseurl }}</span>  
page.url: <span class="code">{{ page.url }}</span>  
page.path: <span class="code">{{ page.path }}</span>  

Link made by site.url, site.baseurl, page.url:  
[{{ site.url }}{{ site.baseurl }}{{ page.url }}]({{ site.url }}{{ site.baseurl }}{{ page.url }})  

Link made by site.baseurl and page.url:  
[{{ site.baseurl }}{{ page.url }}]({{ site.baseurl }}{{ page.url }})  

Link made by page.url only:  
[{{ page.url }}]({{ page.url }}) (need `jekyll-relative-link`
plugin outside localhost)

Link made by link tag:  
[index.html]({% link index.html %}) (need Jekyll 4.0+ without baseurl)  
[{{ site.baseurl }}/index.html]({% link {{ site.baseurl }}/index.html %})  
[{{ site.baseurl }}{{ page.path }}]({% link {{ site.baseurl }}{{ page.path }} %})

Errors previously seen:
{% raw %}
    Liquid Exception: Could not find document '{{ page.path }}' in tag 'link'. Make sure the document exists and the path is correct. in debug.md
{% endraw %}
