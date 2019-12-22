---
layout: page
title: blog
permalink: /blog/
description: From time to time, I am blogging about things I find interesting. Mainly data-related topics but not always.
---

<ul class="post-list">
    {% for post in site.posts reversed %}
      <li>
        <h2><a class="post-title" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a></h2>
        <p class="post-meta">{{ post.date | date: '%B %-d, %Y — %H:%M' }}</p>
        <p>{{ post.description }}</p>
        <br/>
        <hr/>
      </li>
    {% endfor %}
</ul>