---
layout: home
title: Home
nav_exclude: true
permalink: /:path/
seo:
  type: Course
  name: {{ site.title }}
---

# {{site.title}}



# Recent Announcements

{% assign announcements = site.announcements | reverse %}
{% assign announcement_count = announcements | size %}

<div class="announcements-list">
{% for announcement in announcements limit:5 %}
  {{ announcement }}
{% endfor %}
</div>

{% if announcement_count > 5 %}
  <a href="/announcements" class="see-all-link">See All Announcements</a>
{% endif %}
