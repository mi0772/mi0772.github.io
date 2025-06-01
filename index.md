---
layout: default
title: Home
---

# Benvenuto su Carlo's Dev Blog

{% for post in site.posts %}
## [{{ post.title }}]({{ post.url }})
🕒 {{ post.date | date: "%d/%m/%Y %H:%M" }}
{{ post.excerpt }}
---
{% endfor %}
