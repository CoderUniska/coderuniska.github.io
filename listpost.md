---
layout: page
title: Blog
permalink: /blog/
---

<h1 class="page-title">Postingan Terakhir</h1>

<div class="container last-post">
    <section>
        <ul class="collection">
        {% for post in site.posts %}
        <li class="collection-item avatar">
          {% assign date_format = site.minima.date_format | default: "%m/%y" %}
          <div class="date-post">{{ post.date | date: date_format }}</div>
          <span class="title"><a class="post-link" href="{{ post.url | relative_url }}">{{ post.title | escape }}</a></span>
          <p>
             {{ post.content | truncatewords: 8 }}
          </p>
          <a href="{{ post.url | relative_url }}" class="secondary-content"><i class="material-icons">navigate_next</i></a>
        </li>
        {% endfor %}
        </ul>  
    </section>
</div>
</div>