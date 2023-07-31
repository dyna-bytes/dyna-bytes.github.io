---
title: "Algorithm"
layout: archive
permalink: /categories/algo/
author_profile: true  
sidebar:
    nav: "sidebar-category"
---
{% assign posts = site.categories.algo %}
{% for post in posts %} {% include archive-single.html type=page.entries_layout %} {% endfor %}
