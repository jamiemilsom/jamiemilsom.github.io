---
layout: splash
permalink: /
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: /assets/images/half_dome.jpg
excerpt: "A passionate Data Scientist specialising in machine learning, computer vision, and multidisaplinary problems."
---

<div class="feature__wrapper">
  {% assign posts = site.posts | slice: 0, 3 %}
  {% for post in posts %}
    <div class="feature__item">
      <div class="archive__item">
        {% if post.header.teaser %}
          <div class="archive__item-teaser">
            <img src="{{ post.header.teaser | relative_url }}" alt="{{ post.title }}">
          </div>
        {% endif %}
        <div class="archive__item-body">
          <h2 class="archive__item-title">{{ post.title }}</h2>
          {% if post.excerpt %}
            <div class="archive__item-excerpt">
              {{ post.excerpt | markdownify }}
            </div>
          {% endif %}
          <p><a href="{{ post.url | relative_url }}" class="btn btn--primary">Read More</a></p>
        </div>
      </div>
    </div>
  {% endfor %}
</div>

<div class="pagination">
  {% for post in site.posts offset: 3 limit: 1 %}
    <a href="/page2/" class="pagination--pager">Older Posts</a>
  {% endfor %}
</div>