---
layout: page
title: Blog
permalink: /blog/
---

# Research Blog

기후과학, 대기역학, 재생에너지 예측에 관한 연구 일기와 학습 노트입니다.

---

## 📝 Latest Posts

{% for post in site.posts %}
### [{{ post.title }}]({{ post.url }})
**{{ post.date | date: "%Y-%m-%d" }}** • {% for tag in post.tags %}`{{ tag }}`{% if forloop.last %}{% else %} {% endif %}{% endfor %}

{{ post.excerpt | strip_html | truncatewords: 20 }}

[Read more →]({{ post.url }})

---

{% endfor %}

## 🏷️ Categories

{% assign categories = site.posts | map: "categories" | join: "|" | split: "|" | uniq %}
{% for category in categories %}
- `{{ category }}`
{% endfor %}

## 🎯 Blog Purpose

이 블로그는 다음을 목적으로 합니다:

- 연구 진행과정 기록
- 학습 내용 정리
- 기술 팁 공유
- 커뮤니티와의 소통

---

**최신 포스팅부터 시작해서 읽어보세요!**
