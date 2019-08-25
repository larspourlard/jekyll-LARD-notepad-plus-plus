---
title: With Markdown
layout: demo
---

# {{page.title}}

{% assign thisMonth = "now" | date: '%B' %}

{% if thisMonth == site.data.reviews.checkedFor %}
  {% assign state = 'is up to date' %}
{% else %}
  {% assign state = 'should be checked (last review was before ' | append: site.data.reviews.checkedFor | append: ')' %}
{% endif %}
*Data on this page {{state}}*


## ! New in {{thisMonth}}

{% comment %} TODO
  Do we have content?
{% endcomment %}