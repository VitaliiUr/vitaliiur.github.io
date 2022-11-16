---
layout: page
permalink: /teaching/
title: teaching
show_title: false
# description: Materials for courses you taught. Replace this text with your description.
nav: true
horizontal: false
display_categories: [22/23Z]
---

<!-- For now, this page is assumed to be a static description of your courses. You can convert it to a collection similar to `_teaching/` so that you can have a dedicated page for each course.

Organize your courses by years, topics, or universities, however you like! -->

<div class="teaching">
 {% for category in page.display_categories %}
      <h2 class="category">{{category}}</h2>
      {% assign categorized_teaching = site.teaching | where: "category", category %}
      {% assign sorted_teaching = categorized_teaching | sort: "importance" %}
      <!-- Generate cards for each project -->
        <div class="container">
          <div class="row row-cols-1">
          {% for project in sorted_teaching %}
            {% if project.show%}
                {% include teaching.html %}
            {%endif%}
          {% endfor %}
          </div>
        </div>
    {% endfor %}
</div>