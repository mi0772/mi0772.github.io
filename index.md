---
layout: default
title: Home
---

# Benvenuto su Carlo's Dev Blog

Un blog dedicato allo sviluppo software, alle tecnologie web e ai trucchi del mestiere.

## Ultimi Post

<div class="post-list">
{% for post in site.posts %}
  <article class="post-item">
    <h2 class="post-title">
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </h2>
    <div class="post-meta">
      <time datetime="{{ post.date | date_to_xmlschema }}">
        {{ post.date | date: "%d %B %Y" }}
      </time>
    </div>
    <div class="post-excerpt">
      {{ post.excerpt | strip_html | truncate: 200 }}
    </div>
  </article>
{% endfor %}
</div>

{% if site.posts.size == 0 %}
<div style="text-align: center; padding: 40px; color: #656d76;">
  <p>Non ci sono ancora post pubblicati.</p>
  <p>Torna presto per nuovi contenuti!</p>
</div>
{% endif %}
