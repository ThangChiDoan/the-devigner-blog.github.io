---
layout: default
title: Blog
permalink: /blog/
---

# Blog

<div class="posts-list">
    {% for post in site.posts %}
    <article class="post-preview">
        <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
        <div class="post-meta">
            <time>{{ post.date | date: "%B %d, %Y" }}</time>
        </div>
        <p>{{ post.excerpt | strip_html | truncatewords: 30 }}</p>
        <a href="{{ post.url | relative_url }}" class="read-more">Read More →</a>
    </article>
    {% endfor %}
</div>
