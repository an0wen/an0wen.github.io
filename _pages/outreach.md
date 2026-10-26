---
layout: page
title: Outreach
permalink: /outreach/
description:
nav: true
nav_order: 3.5
display_categories: # e.g. [outreach] to group cards by category
horizontal: false
---

<!-- pages/outreach.md -->
<div class="outreach">
{% if site.enable_outreach_categories and page.display_categories and page.display_categories != empty %}
  <!-- Display categorized outreach -->
  {% for category in page.display_categories %}
  <a id="{{ category }}" href=".#{{ category }}">
    <h2 class="category">{{ category }}</h2>
  </a>
  {% assign categorized_outreach = site.outreach | where: "category", category %}
  {% assign sorted_outreach = categorized_outreach | sort: "importance" %}
  <!-- Generate cards for each outreach -->
  {% if page.horizontal %}
  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for outreach in sorted_outreach %}
      {% include outreach_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for outreach in sorted_outreach %}
      {% include outreach.liquid %}
    {% endfor %}
  </div>
  {% endif %}
  {% endfor %}

{% else %}

<!-- Display outreach without categories -->

{% assign sorted_outreach = site.outreach | sort: "importance" %}

  <!-- Generate cards for each outreach -->

{% if page.horizontal %}

  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for outreach in sorted_outreach %}
      {% include outreach_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for outreach in sorted_outreach %}
      {% include outreach.liquid %}
    {% endfor %}
  </div>
  {% endif %}
{% endif %}
</div>
