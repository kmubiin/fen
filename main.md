---
published: true
title: main.md
---

Test link:  
[Go to sub (relative)](sub.md) (requires plugin)  
[Go to sub 1]({% link sub.md %}) (link tag)
[Go to sub 2]({{ site.baseurl }}{% link sub.md %}) (link
tag, with baseurl workaround)

Test static link:  
[Go to index](index.html)
