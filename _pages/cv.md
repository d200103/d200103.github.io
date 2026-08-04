---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

教育经历 （Education）
======
* 2025.03——至今     哈尔滨工业大学数学学院 数学         博士在读研究生(硕博连读)
* 2023.09——2025.03 哈尔滨工业大学数学学院 应用数学      硕转博
* 2019.08——2023.06 哈尔滨工业大学数学学院 信息与计算科学 学士

工作经历 （Work experience）
======
* 2024: 
  * 职责：助教
  * 课程：压缩感知
  * 时间: 2024.10.28——2024.12.08
  * 优秀助教

* 2025:
  * 职责：助教 (暑期学校)
  * 课程：数学与人工智能
  * 时间: 2025.07.13——2025.07.26
  
  * 职责：助教
  * 课程：压缩感知
  * 时间: 2025.09.20——2025.12.01

  * 职责：助教
  * 课程：常微分方程（中外合作）
  * 时间: 2025.10.10——2025.12.19
  
* 2026:
  * 职责：助教
  * 课程：实变函数（中外合作）
  * 时间：2026.03.09——2026.07.12
    
论文与专利（Publications）
======
{% for category in site.publication_category %}
  {% assign category_posts = site.publications | where: "category", category[0] %}

  {% if category_posts.size > 0 %}
    <h2>{{ category[1].title }}</h2><hr />

    {% assign item_number = 0 %}
    {% for post in category_posts reversed %}
      {% assign item_number = item_number | plus: 1 %}

      <p class="archive__item-excerpt publication-list-item">
        [{{ item_number }}] {{ post.citation }}
      </p>
    {% endfor %}
  {% endif %}
{% endfor %}
  
会议（Talks）
======
  <ul>{% for post in site.talks reversed %}
    {% include archive-single-talk-cv.html  %}
  {% endfor %}</ul>
  
