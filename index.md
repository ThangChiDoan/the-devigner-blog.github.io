---
layout: default
title: The Devigner Blog
permalink: /
---

<section class="hero">
    <h1>{{ site.title }}</h1>
    <p class="tagline">{{ site.description }}</p>
    <a href="{{ '/blog' | relative_url }}" class="btn btn-primary">Read Our Blog</a>
</section>

<section class="featured-posts">
    <h2>Latest Posts</h2>
    <div class="posts-list">
        {% for post in site.posts limit: 3 %}
        <article class="post-preview">
            <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
            <div class="post-meta">
                <time>{{ post.date | date: "%B %d, %Y" }}</time>
            </div>
            <p>{{ post.excerpt | strip_html }}</p>
            <a href="{{ post.url | relative_url }}" class="read-more">Read More →</a>
        </article>
        {% endfor %}
    </div>
</section>
