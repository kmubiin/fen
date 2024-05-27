---
published: true
title: debug.md
---

Predefined variables (from layout file themes):
site.github.is_project_page: <span class="code">{{ site.github.is_project_page }}</span>  
site.github.repository_name: <span class="code">{{ site.github.repository_name }}</span>  
site.github.owner_url: <span class="code">{{ site.github.owner_url }}</span>  
site.github.owner_name: <span class="code">{{ site.github.owner_name }}</span>  
site.github.project_tagline: <span class="code">{{ site.github.project_tagline }}</span>  
site.github.zip_url: <span class="code">{{ site.github.zip_url }}</span>  
site.github.tar_url: <span class="code">{{ site.github.tar_url }}</span>  

Defined variables are:  
site.url: <span class="code">{{ site.url }}</span>  
site.baseurl: <span class="code">{{ site.baseurl }}</span>  
page.url: <span class="code">{{ page.url }}</span>  
page.path: <span class="code">{{ page.path | default: "missing?" }}</span>  

Link made by site.url, site.baseurl, page.url:  
[{{ site.url }}{{ site.baseurl }}{{ page.url }}]({{ site.url }}{{ site.baseurl }}{{ page.url }})  

Link made by site.baseurl and page.url:  
[{{ site.baseurl }}{{ page.url }}]({{ site.baseurl }}{{ page.url }})  

Link made by page.url only:  
[{{ page.url }}]({{ page.url }}) (need `jekyll-relative-link`
plugin outside localhost)

Link made by link tag (need absolute path, it seems):  
[index.html]({% link index.html %})  (Jekyll 4.0+)  
[prefix baseurl to index.html]({{ site.baseurl }}{% link index.html %})  
[prefix . to index.html](.{% link index.html %})

Note:  
The prefix `.` itself seems to include `baseurl` already,
so no need to prefix both together;
otherwise appears relative or indifferent on localhost.

Link made by link tag (raw code):  
{% raw %}
Build with success:  
{% link index.html %}  (Jekyll 4.0+)  
{{ site.baseurl }}{% link index.html %}

Build with errors:  
{% link {{ site.baseurl }}/index.html %}  
{% link {{ page.path }} %}  
{% link {{ site.baseurl }}{{ page.path }} %}

    Liquid syntax error (line 41): Tag '{% ... %}' was not
    properly terminated with regexp: /\\%\\}/
    (Liquid::SyntaxError)

    Liquid Exception: Could not find document
    '{{ site.baseurl }}/index.html' in tag 'link'. Make sure
    the document exists and the path is correct. in debug.md

Verdict:  
`{% ... %}` can't be nested with `{{ ... }}`
{% endraw %}
