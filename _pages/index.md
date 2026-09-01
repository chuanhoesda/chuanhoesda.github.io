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
gallery:
  - url: /assets/images/announcements/resistanceband1.jpeg
    image_path: /assets/images/announcements/resistanceband1.jpeg
    alt: "Resistance band exercise class 1"
    title: "Resistance band exercise class 1"
  - url: /assets/images/announcements/resistanceband2.jpeg
    image_path: /assets/images/announcements/resistanceband2.jpeg
    alt: "Resistance band exercise class 2"
    title: "Resistance band exercise class 2"
  - url: /assets/images/announcements/resistanceband3.jpeg
    image_path: /assets/images/announcements/resistanceband3.jpeg
    alt: "Resistance band exercise class 3"
    title: "Resistance band exercise class 3"
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
    excerpt: "Elder - Phyllisity Liang @ 9877 1806<br/>Elder - Janie Foo @ 9099 3072<br/>[Facebook page - Message for Details](https://www.facebook.com/groups/chuanhoesdac/)"
---




<div style="margin-top: 3rem;">
  <h2 style="border-bottom: 1px solid #e0e0e0; padding-bottom: 0.5rem;">Latest Updates</h2>

  {% for post in site.posts limit:3 %}
<div class="list__item">
  <article class="archive__item">
    <h2 class="archive__item-title no_toc">
      <a href="{{ post.url | relative_url }}" rel="permalink">{{ post.title }}</a>
    </h2>
    {% if post.date %}
      <p class="archive__item-excerpt" style="margin-top: 0; font-size: 0.75em;">
        <time datetime="{{ post.date | date: "%Y-%m-%dT%H:%M:%S%z" }}">{{ post.date | date: "%B %d, %Y" }}</time>
      </p>
    {% endif %}
    {% if post.excerpt %}
      <p class="archive__item-excerpt">{{ post.excerpt }}</p>
    {% endif %}
    {% if post.gallery %}
      <div class="gallery" style="display: grid; grid-template-columns: repeat(3, 1fr); gap: 1rem; margin-top: 1rem;">
        {% for image in post.gallery limit:3 %}
          <a href="{{ image.url | relative_url }}" class="image-popup">
            <img src="{{ image.image_path | relative_url }}" alt="{{ image.alt }}" style="width: 100%; height: auto; border-radius: 4px;">
          </a>
        {% endfor %}
      </div>
    {% endif %}
  </article>
</div>
{% endfor %}
</div>

## Directions
{% include gallery id="directions_gallery" %}
{% include feature_row %}
