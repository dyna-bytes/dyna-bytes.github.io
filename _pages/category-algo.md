---
title: "Algorithm"
layout: archive
permalink: /algo/
---
{% assign posts = site.categories.algo %}
{% for post in posts %} {% include archive-single.html type=page.entries_layout %} {% endfor %}
