---
layout: page
permalink: /journey
title: my journey
description: from Chemistry to Education to AI - sharing a little to support other inter-disciplinary researchers getting into AI
nav: true
---

An interview where I share some of my inspirations and motivations on this journey! Feel free to listen as podcast.

<iframe width="560" height="315" src="https://www.youtube.com/embed/URU4iAzacT4?si=dyCAt-Z29CbqTUCI" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>


<div class="news">
  <h2>Milestones</h2>
  {% if site.news  %}
    <div class="table-responsive">
      <table class="table table-sm table-borderless">
      {% assign news = site.news | reverse %}
      {% for item in news limit: 100 %}
        <tr>
          <th scope="row">{{ item.date | date: "%b %Y" }}</th>
          <td>
            {% if item.inline %}
              {{ item.content | remove: '<p>' | remove: '</p>' | emojify }}
            {% else %}
              <a class="news-title" href="{{ item.url | relative_url }}">{{ item.title }}</a>
            {% endif %}
          </td>
        </tr>
      {% endfor %}
      </table>
    </div>
  {% else %}
    <p>No news so far...</p>
  {% endif %}
</div>