---
layout: default
---

<div class="notion-header">
  <img src="https://www.notion.so/images/page-cover/met_bruegel_1565.jpg" class="notion-cover">
  <div class="notion-icon-container">
    <img src="https://em-content.zobj.net/source/apple/354/cat_1f408.png" class="notion-profile-icon">
  </div>
</div>

<div class="notion-content">

# Tarot Cathedral
Welcome to my blog about **Tarot and numerology**. This is an experimental Notion-style layout.

<div class="notion-gallery">
  {% for post in site.posts %}
  <a href="{{ post.url | relative_url }}" class="notion-card">
    
    {% if post.image %}
      <img src="{{ post.image | relative_url }}" class="notion-card-cover">
    {% else %}
      <div style="height:160px; background: #f7f7f5; display: flex; align-items: center; justify-content: center; color: #ccc;">No Image</div>
    {% endif %}
    
    <div class="notion-card-content">
      <h3 class="notion-card-title">{{ post.title }}</h3>
      
      <div>
        {% for tag in post.tags %}
          <span class="n-tag tag-{{ tag | slugify }}">{{ tag }}</span>
        {% endfor %}
      </div>
    </div>
  </a>
  {% endfor %}
</div>

</div>
