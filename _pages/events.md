---
permalink: /events/
title: "Events"
layout: single
---

{% assign upcoming_posts = site.posts | where_exp: "post", "post.date > site.time" %}
{% if upcoming_posts.size > 0 %}
## Upcoming Events
{% for post in upcoming_posts %}
{% include post-card.html post=post %}
{% endfor %}
{% endif %}

## Past Events
{% assign past_posts = site.posts | where_exp: "post", "post.date <= site.time" %}
{% for post in past_posts %}
{% include post-card.html post=post %}
{% endfor %}
