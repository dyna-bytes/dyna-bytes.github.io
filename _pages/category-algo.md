---
title: "Algorithm"
layout: archive
permalink: /algo/
sidebar:
    nav: "sidebar-category"
author_profile: true
---
{% assign posts = site.categories.algo %}
{% for post in posts %} {% include archive-single.html type=page.entries_layout %} {% endfor %}
