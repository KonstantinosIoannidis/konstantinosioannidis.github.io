---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
---

{% include base_path %}

<!-- Check <a href="/coauthors">a list of my coauthors</a>. -->

<h2>Working papers</h2>
<ul>
{% assign working_papers = site.research | where: "category", "working" %}

{% for post in working_papers %}

<li>
  <a href="{{post.permalink}}">
      <b>{{ post.title }}</b>
  </a><br>
  <i>{{ post.stage }}.</i>

    {% if post.coauthors != "" %}
    <br>
    (with {{ post.coauthors }})
    {% endif %}

  <br>

  {{ post.summary }}

    {% if post.paperurl %}
        <a href="{{ post.paperurl }}" target="_blank" class="btn">{{ site.data.ui-text[site.locale].pdf_link_label | default: "PDF" }}
        </a>
    {% endif %}

</li>

{% endfor %}
</ul>

<h2>Working in progress</h2>
<ul>
{% assign working_progress = site.research | where: "category", "progress" %}

{% for post in working_progress %}

<li>
  <a href="{{post.permalink}}">
      <b>{{ post.title }}</b>
  </a>
  <i>{{ post.stage }}.</i>

    {% if post.coauthors != "" %}
    <br>
    (with {{ post.coauthors }})
    {% endif %}

  <br>

  {{ post.summary }}

    <!-- {% if post.paperurl %}
        <a href="{{ page.paperurl }}" target="_blank" class="btn">{{ site.data.ui-text[site.locale].pdf_link_label | default: "PDF" }}
        </a>
    {% endif %} -->

</li>

{% endfor %}
</ul>
