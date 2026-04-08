---
layout: default
---

<div class="notion-header">
  <img src="https://www.notion.so/images/page-cover/met_bruegel_1565.jpg" class="notion-cover">
  <div class="notion-icon-container">
    <img src="https://em-content.zobj.net/source/apple/354/cat_1f408.png" class="notion-profile-icon">
  </div>
</div>

<div class="notion-main-layout">
  
  <div class="notion-column-left">
    <h1 style="font-size: 40px; margin-bottom: 10px;">Tarot Cathedral</h1>
    
    <div class="notion-callout">
      <span>💡</span>
      <div>
        Welcome on my blog about <strong>Tarot and numerology</strong>. Here I share my historical research, thoughts and some art.
      </div>
    </div>

    <h3 style="border-bottom: 1px solid #eee; padding-bottom: 8px; margin-top: 40px;">Entries</h3>
    
    <div class="notion-gallery">
      {% for post in site.posts %}
      <a href="{{ post.url | relative_url }}" class="notion-card">
        {% if post.image %}
          <img src="{{ post.image | relative_url }}" class="notion-card-cover">
        {% else %}
          <div style="width:120px; height:100px; background: #f7f7f5;"></div>
        {% endif %}
        <div class="notion-card-content">
          <h4 class="notion-card-title">{{ post.title }}</h4>
          <span class="n-tag">history</span>
        </div>
      </a>
      {% endfor %}
    </div>
  </div>

  <div class="notion-column-right">
    <div class="notion-callout" style="flex-direction: column; background: #f7f7f5;">
      <strong style="margin-bottom: 10px; font-family: serif; font-style: italic; font-size: 1.2em; text-align: center;">Navigation</strong>
      <div style="border-top: 1px solid #ddd; padding-top: 10px;">
        <a href="/" class="notion-nav-item">🏠 Home</a>
        <a href="/about" class="notion-nav-item">🐱 About me</a>
        <a href="/art" class="notion-nav-item">🎨 My Art</a>
        <a href="/links" class="notion-nav-item">🔗 Links</a>
      </div>
    </div>
  </div>

</div>
