---
layout: default
---

<div class="header-bar">
    <h1>jmsweb</h1>
    <h2>A good way to code <em>flexibly</em> is to write less and unit-tested code.</h2>
    <br/>
    <hr>
    <br/>
</div>

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