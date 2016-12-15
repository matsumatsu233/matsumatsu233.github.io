---
layout: default
permalink: /gsv/
---
<div class="home">
  <div class="gsv-title">
    Gitadora Skill Viewer
  </div>
  <div class="gsv-desc">
    <a href="http://gitadora-skill-viewer.herokuapp.com">http://gitadora-skill-viewer.herokuapp.com</a>
  </div>
  <div class="post-list-fixed">
    {% for post in site.posts %}
      {% if post.category == "gsv" and post.fixed == "true" %}
        <div class="post-list-item">
          <a href="{{ post.url | prepend: site.baseurl }}">
            <div>
              <div class="post-link-title" >
                <i class="fa fa-thumb-tack fixed-icon" aria-hidden="true" style="font-size:70%"></i>
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
  <div class="post-list">
    {% for post in site.posts %}
      {% if post.category == "gsv" and post.fixed != "true" %}
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
