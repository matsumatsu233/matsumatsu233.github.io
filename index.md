---
layout: default
---

<div class="home">

  <div class="post-list">
    {% for post in site.posts %}
      {% if post.category == "blog" %}
        <div class="post-list-item">
          <a href="{{ post.url | prepend: site.baseurl }}">
            <div>
              <div class="post-link-title" >
                {{ post.title }}
              </div>
            </div>

            {% if post.description %}
              <div class="list-post-desc">
                {{ post.description }}
              </div>
            {% endif %}

            <div class="post-meta">
              <span class="post-meta-date">{{ post.date | date: "%Y.%m.%d" }}</span>
              <span>
                {% for tag in post.tags %}
                  <a href="tags#{{ tag }}" class="tags">{{ tag }}</a>
                {% endfor %}
              </span>
            </div>

          </a>
        </div>
      {% endif %}
    {% endfor %}
  </div>
</div>
