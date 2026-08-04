---
layout: archive
title: "Research Themes"
permalink: /research/
author_profile: true
---

{% include base_path %}

My research spans a range of species, methods, and ecosystems, but is connected by four broad themes.

<style>
.research-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 1.75em 1.5em;
  margin-top: 1.5em;
}
@media (max-width: 600px) {
  .research-grid { grid-template-columns: 1fr; }
}
.research-card {
  display: block;
  text-decoration: none;
  color: inherit;
}
.research-card img {
  width: 100%;
  height: 200px;
  object-fit: cover;
  display: block;
  border-radius: 4px;
}
.research-card .research-card__title {
  font-size: 1.1em;
  font-weight: 700;
  line-height: 1.3;
  margin: 0.6em 0 0;
}
.research-card:hover .research-card__title {
  text-decoration: underline;
}
</style>

<div class="research-grid">
{% for post in site.portfolio %}
<a class="research-card" href="{{ base_path }}{{ post.url }}">
{% if post.header.teaser %}{% if post.header.teaser contains "://" %}<img src="{{ post.header.teaser }}" alt="">{% else %}<img src="{{ post.header.teaser | prepend: '/images/' | prepend: base_path }}" alt="">{% endif %}{% endif %}
<p class="research-card__title">{{ post.title }}</p>
</a>
{% endfor %}
</div>
