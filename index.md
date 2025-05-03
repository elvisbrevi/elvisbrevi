---
layout: default
title: "Elvis Brevi's Blog"
---

# Welcome to My Blog

Here you'll find all my latest posts and updates.

## Latest Posts

<div class="posts-list">
  {% for post in site.posts %}
    <div class="post-item">
      <h2>
        <a href="{{ post.url }}">{{ post.title }}</a>
      </h2>
      <p class="post-date"><small>{{ post.date | date: "%B %d, %Y" }}</small></p>
      <div class="post-excerpt">
        {{ post.excerpt }}
      </div>
      <p class="read-more">
        <a href="{{ post.url }}">Read more...</a>
      </p>
    </div>
    {% unless forloop.last %}
    <hr>
    {% endunless %}
  {% endfor %}
</div>

<style>
  .posts-list {
    margin-top: 2rem;
  }
  .post-item {
    margin-bottom: 2rem;
  }
  .post-date {
    color: #6c757d;
    margin-bottom: 1rem;
  }
  .post-excerpt {
    margin-bottom: 1rem;
  }
  .read-more {
    text-align: right;
  }
</style>
