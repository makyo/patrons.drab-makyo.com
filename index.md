---
layout: default
title: Welcome
---

This site is primarily for [patrons](https://patreon.com/makyo) who would like to see advance copies of my works. I'll post snippets or full stories here for patrons to see.

-----

# Recent Posts

{% for post in site.posts limit: 3 %}
<div class="post-listing">
    <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
    <p><strong>{{ post.date | date: "%a, %b %d, %y" }}</strong></p>
    {% if post.layout == 'encrypted' %}
        <p><em>This post is encrypted and viewable to patrons only</em></p>
    {% else %}
        {{ post.excerpt }}
    {% endif %}
</div>
{% endfor %}

[More posts](/posts)
