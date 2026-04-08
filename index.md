---
layout: default
---

<div class="notion-header">
  <img src="https://images.pexels.com/photos/36116194/pexels-photo-36116194.jpeg" class="notion-cover">
  <div class="notion-icon-container">
    <img src="/assets/img/avatar-icon2.png" class="notion-profile-icon">
  </div>
</div>



<div class="notion-title-section">
  <h1 style="font-size: 32px; margin-bottom: 15px; font-weight: 700;">Tarot Cathedral</h1>
  
  <div class="notion-callout">
    <span>✨</span>
    <div>
      Welcome on my blog about <strong>Tarot and numerology</strong>. Exploring the mysteries through art and history.
    </div>
  </div>
</div>

<div class="notion-main-layout">
  
  <div class="notion-column-left">
    <h3 style="font-size: 18px; color: rgba(55, 53, 47, 0.5); border-bottom: 1px solid #eee; padding-bottom: 8px; margin: 0 0 20px 0;">Entries</h3>
    
    <div class="notion-gallery">
      {% for post in site.posts %}
      <a href="{{ post.url | relative_url }}" class="notion-card">
        {% if post.image %}
          <img src="{{ post.image | relative_url }}" class="notion-card-cover">
        {% else %}
          <div style="width:100%; height:120px; background: #f7f7f5;"></div>
        {% endif %}
        <div class="notion-card-content">
          <h4 class="notion-card-title">{{ post.title }}</h4>
          
          <div style="font-size: 12px; color: rgba(55, 53, 47, 0.5); margin-top: 4px;">
            {{ post.date | date: "%B %d, %Y" }}
          </div>

          <div style="margin-top: 8px;">
             {% for tag in post.tags %}
               <span class="n-tag tag-{{ tag | slugify }}">{{ tag }}</span>
             {% endfor %}
          </div>
        </div>
      </a>
      {% endfor %}
    </div>
  </div>

  <div class="notion-column-right">
    <div style="background: #f7f7f5; padding: 20px; border-radius: 8px;">
      <h3 style="font-family: serif; font-style: italic; text-align: center; margin-top: 0;">Navigation</h3>
      <div style="margin-top: 15px;">
        <a href="/" class="notion-nav-item">🗂 Tarot Cathedral</a>
        <a href="/" class="notion-nav-item">📖 Blog</a>
        <a href="/" class="notion-nav-item">🖼 My Art</a>
        <a href="/" class="notion-nav-item">🎓 Links</a>
        <a href="/" class="notion-nav-item">👤 About me</a>
      </div>
    </div>
  </div>

</div>

<footer class="notion-footer">
  <hr style="border: none; border-top: 1px solid rgba(55, 53, 47, 0.09); margin-bottom: 20px;">
  <div style="display: flex; justify-content: space-between; align-items: center; font-size: 13px; color: rgba(55, 53, 47, 0.5);">
    <p><em>All rights reserved. 2026.</em></p>
    <a href="{{ '/' | relative_url }}" style="color: inherit; text-decoration: none; border-bottom: 1px solid rgba(55, 53, 47, 0.2);">Tarot Cathedral Home</a>
  </div>
</footer>
