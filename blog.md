---
layout: default
title: blog
permalink: /blog/
---

<div class="posts">
    {% for post in site.posts %}
        <article class="post">
            <h2><a class="post-title" href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></h2>
            <p class="post-meta">{{ post.date | date: '%B %-d, %Y — %H:%M' }}</p>
            <div class="entry">{{ post.excerpt }}</div>
            <a href="{{ site.baseurl }}{{ post.url }}" class="read-more">Read More</a>
        </article>
    {% endfor %}
</div>