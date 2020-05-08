---
layout: default
title: ddkto's ramblings
regenerate: true
---
# {{page.title}}

{% for post in site.posts limit:5 %}
## <a href="{{ post.url }}">{{ post.title }}</a>

{{ post.excerpt }}

{% endfor %}
          
## [Click here for older posts...](/archive/)


