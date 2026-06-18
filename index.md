---
layout: default
---

<div class="home">
  <ul class="post-list">
    {% for post in site.posts reversed %}
    <li>
      <!-- Невидимая ссылка на всю карточку -->
      <a class="post-card-link" href="{{ post.url | relative_url }}" aria-label="{{ post.title }}"></a>
      
      <!-- Просто картинка без рамки и обрезки -->
      {% if post.image %}
      <img class="post-image" src="{{ post.image | relative_url }}" alt="{{ post.title }}">
      {% endif %}
      
      <!-- Название — просто текст -->
      <h3>{{ post.title }}</h3>
      
      <!-- Описание -->
      <p class="post-excerpt">{{ post.excerpt | strip_html | truncate: 160 }}</p>
    </li>
    {% endfor %}
  </ul>
</div>
