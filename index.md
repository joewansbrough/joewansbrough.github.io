---
layout: default
title: Home
---

# Welcome to Joltin' Joe's Hot Sauce

Add your homepage content here!

## About Our Sauces

This is where you can describe your hot sauce products, philosophy, and what makes them special.

## Latest Blog Posts

{% for post in site.posts limit:3 %}
  <article>
    <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
    <p class="post-meta">{{ post.date | date: "%B %-d, %Y" }}</p>
    <p>{{ post.excerpt }}</p>
  </article>
{% endfor %}

<p><a href="{{ '/blog' | relative_url }}">View all posts →</a></p>
