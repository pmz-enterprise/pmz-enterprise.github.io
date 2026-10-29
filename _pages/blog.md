---
layout: default
title: blog
permalink: /blog/
nav: true
nav_order: 3
---

<div class="post">
  <header class="post-header">
    <h1 class="post-title">Blog</h1>
    <p class="post-description">Notes on research, ideas, and experiments.</p>
  </header>

  <article class="post-content">
    {% assign posts = site.posts %}
    {% if posts.size > 0 %}
      <div class="table-responsive">
        <table class="table table-sm table-borderless">
          {% for post in posts %}
            <tr>
              <th scope="row" style="width: 20%; white-space: nowrap;">{{ post.date | date: '%b %d, %Y' }}</th>
              <td>
                <a class="post-link" href="{{ post.url | relative_url }}">{{ post.title }}</a>
                {% if post.excerpt %}
                  <div class="post-description">{{ post.excerpt | strip_html | strip_newlines | truncate: 180 }}</div>
                {% endif %}
              </td>
            </tr>
          {% endfor %}
        </table>
      </div>
    {% else %}
      <p>No posts yet. Add a Markdown file to <code>_posts/</code> to publish your first post.</p>
      <p>Use the filename format <code>YYYY-MM-DD-title.md</code> and start it with:</p>
      <pre><code>---
layout: post
title: Your post title
date: YYYY-MM-DD
description: A short description
tags: [research]
categories: [notes]
---

Write your post here.</code></pre>
    {% endif %}
  </article>
</div>
