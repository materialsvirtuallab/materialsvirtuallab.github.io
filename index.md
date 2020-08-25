---
# You don't need to edit this file, it's empty on purpose.
# Edit theme's home layout instead if you wanna make some changes
# See: https://jekyllrb.com/docs/themes/#overriding-theme-defaults
layout: home
title: home
---

# Welcome

This is a collaborative public guide to the [Materials Virtual Lab](www.materialsvirtuallab.org). It is meant to serve as an onboarding document for newcomers, as well as for prospective students and postdocs to understand the way we work. New group members should start with the [orientation guide](/orientation).

Group members are welcome to help maintain these pages by directly cloning the page and pushing changes.

# Guides

{% assign default_paths = site.pages | map: "path" %}
{% assign page_paths = site.header_pages | default: default_paths %}
<ul>
{% for path in page_paths %}
  {% assign my_page = site.pages | where: "path", path | first %}
  {% if my_page.category and my_page.category == "Guides" %}
  <li><a class="page-link" href="{{ my_page.url | relative_url }}">{{ my_page.title | escape }}</a></li>
  {% endif %}
{% endfor %}
</ul>

Not all information is available on this public guide. Some sensitive information, e.g., contact information, cluster setups, etc., are available on our group's [internal wiki](https://www.materialsvirtuallab.org/wiki).

# Links

* [Leave of absence form](https://airtable.com/shrXVPLJbBSnMH6gN)
