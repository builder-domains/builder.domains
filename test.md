---
title: List of all posts
permalink: /api/posts
---
[
  {% for post in site.posts %}
    {
      "date": "{{ post.date }}",
      "title": "{{ post.title }}",
      "content": "{{ post }}",
      "tags": "{{ post.tags | jsonify }}",
      "categories": "{{ post.categories | jsonify }}",
      "url": "{{ post.url }}",
      "slug": "{{ post.slug }}"
    }
    {% unless forloop.last %},{% endunless %}
  {% endfor %}
]
