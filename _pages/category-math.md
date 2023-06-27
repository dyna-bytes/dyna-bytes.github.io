---
title: "Math"
layout: archive
permalink: /math/
author_profile: true  
sidebar:
    nav: "sidebar-category"
---
{% assign posts = site.categories.math %}
{% for post in posts %} {% include archive-single.html type=page.entries_layout %} {% endfor %}
