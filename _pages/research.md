---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
---

{% include base_path %}

{% assign categories = site.research_category %}

{% for category in categories %}

{% assign papers = site.research | where: "category", category[0] %}

{% if papers.size > 0 %}

  <h2>{{ category[1].title }}</h2>

  <ul>
  {% for post in papers %}
  <li>
    <a href="{{ post.permalink | default: post.url }}"><b>{{ post.title }}</b></a><br>
    {% if post.stage %}<i>{{ post.stage }}.</i>{% endif %}
    {% if post.coauthors != nil and post.coauthors != "" %}
    <br>(with {{ post.coauthors }}){% endif %}
    <br>
    {{ post.summary }}
    {% if post.paperurl %}
      <a href="{{ post.paperurl }}" target="_blank" class="btn">{{ site.data.ui-text[site.locale].pdf_link_label | default: "PDF" }}</a>
    {% endif %}
  </li>
  {% endfor %}
  </ul>

{% endif %}
{% endfor %}
