---
layout: archive
title: "✍️ Other"
permalink: /other/
author_profile: true
---

{% if site.posts.size > 0 %}
  {% for post in site.posts %}
    <article style="margin-bottom: 2.5em; border-bottom: 1px solid #eee; padding-bottom: 2em;">
      <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
      <p style="color: grey; font-size: 0.9em;">
        {{ post.date | date: "%B %d, %Y" }}
        {% if post.tags %} · {{ post.tags | join: ", " }}{% endif %}
      </p>
      {% if post.excerpt %}
        <p>{{ post.excerpt }}</p>
      {% endif %}
      <a href="{{ post.url }}">Read more →</a>
    </article>
  {% endfor %}
{% else %}
  <p>No articles yet. Check back soon.</p>
{% endif %}
