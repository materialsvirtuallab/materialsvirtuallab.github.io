---
# You don't need to edit this file, it's empty on purpose.
# Edit theme's home layout instead if you wanna make some changes
# See: https://jekyllrb.com/docs/themes/#overriding-theme-defaults
layout: home
title: home
---

# Welcome

This site provides a collaborative guide to the Materials Virtual Lab. It is meant to serve as an onboarding document for newcomers, as well as for potential recruits to understand the way we work.

# Table of Contents
{% assign default_paths = site.pages | map: "path" %}
{% assign page_paths = site.header_pages | default: default_paths %}
<ul>
{% for path in page_paths %}
  {% assign my_page = site.pages | where: "path", path | first %}
  {% if my_page.title %}
  <li><a class="page-link" href="{{ my_page.url | relative_url }}">{{ my_page.title | escape }}</a></li>
  {% endif %}
{% endfor %}
</ul>