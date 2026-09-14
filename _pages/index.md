---
layout: splash
permalink: /
hidden: true
image: /assets/images/adventist-symbol-tm-circle--black.png
header:
  overlay_color: "#5e616c"
  overlay_image: /assets/images/banner.jpg
excerpt: >
  <br /><br /><br /><br />
directions_gallery:
  - url: /assets/images/announcements/Directions.jpeg
    image_path: /assets/images/announcements/Directions.jpeg
    alt: "Directions"
    title: "Directions"
feature_row:
  - alt: "SATURDAY WORSHIP"
    title: "<i class='fa fa-users' aria-hidden='true'></i> SATURDAY WORSHIP"
    excerpt: "10:30AM - Worship & Bible Study<br/>12:30PM - Lunch Fellowship & Social Activities"
  - alt: "LOCATION"
    title: "<i class='fas fa-map-signs'></i> LOCATION"
    excerpt: "226 Yio Chu Kang Rd, Singapore 545664"
  - alt: "CONTACT US"
    title: "<i class='fas fa-envelope'></i> CONTACT US"
    excerpt: "Elder - Phyllisity Liang @ 9877 1806<br/>Elder - Janie Foo @ 9099 3072<br/><a href='fb://group/chuanhoesdac' onclick=\"setTimeout(function(){ window.location='https://www.facebook.com/groups/chuanhoesdac/'; }, 500);\">Facebook page - Message for Details</a>"
---


<div class="home-posts">
  {% assign upcoming_posts = site.posts | where_exp: "post", "post.date > site.time" %}
  {% if upcoming_posts.size > 0 %}
  <h2 class="home-posts-heading">Upcoming Events</h2>

  {% for post in upcoming_posts limit:3 %}
  {% include post-card.html post=post %}
{% endfor %}
  {% endif %}

  {% assign latest_posts = site.posts | where_exp: "post", "post.date <= site.time" %}
  <h2 class="home-posts-heading">Latest Updates</h2>

  {% for post in latest_posts limit:3 %}
  {% include post-card.html post=post %}
{% endfor %}
</div>

## Directions
{% include gallery id="directions_gallery" %}
{% include feature_row %}
