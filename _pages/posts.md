---
permalink: /posts
# layout: default
excerpt: "Blogs"
---

<h1>My Blog Posts</h1>
<ul>
  {% for post in site.posts %}
  <article>
    <h2>
      <a href="{{ post.url | relative_url }}">
        {{ post.title }}
      </a>
    </h2>
    <time datetime="{{ post.date | date: "%Y-%m-%d" }}">{{ post.date | date_to_long_string }}</time>
    {{ post.excerpt }}
  </article>
{% endfor %}
</ul>