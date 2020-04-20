---
permalink: /blog/
title:     MANOOL Blog
---

<header>
  <h1>{{page.title|smartify|escape_once}}</h1>
</header>

{%for post in site.posts%}<section>
  <h2>{{post.title|smartify|escape_once}}</h2>
  <p markdown="1">{{post.excerpt}} ...</p>
  <p><a href="{{post.url}}">Complete article</a></p>
  <div class="right"><small>Published: <time datetime="{{post.date|date:'%F'}}">{{post.date|date:'%B %-d, %Y'}}</time></small></div>
  <div class="right"><small>Updated: <time datetime="{{post.updated|date:'%F'}}">{{post.updated|date:'%B %-d, %Y'|default:'never'}}</time></small></div>
</section>{%endfor%}