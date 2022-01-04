---
layout: default
title: Lectures
permalink: /lectures/
---

This is a test for using json to specify lecture content. This page is generated using a loop in the Liquid language used by Jekyll. It reads from the file in `data/lectures.json`.

Todo: factor this out into a layout and make customizable, so that content and structure are decoupled and this can apply to other pages.

<table>
<tr>
<th>Date</th>
<th>Topic</th>
<th>Video</th>
<th>Handout</th>
<th>Files</th>
</tr>

{% for lecture in site.data.lectures %}
<tr>
  <td>
  {{ lecture.first }}
  </td>
  <td>
  {{ lecture.last.Topic }}
  </td>
  <td>
  {{ lecture.last.Video }}
  </td>
  <td>
  {% if lecture.last.Handout.size == 1 %}
  {{ lecture.last.Handout }}
  {% else %}
  <ul>
    {% for member in lecture.last.Handout %}
    <li>{{ member }}</li>
    {% endfor %}
  </ul>
  {% endif %}
  </td>
  <td>
    {% if lecture.last.Files.size == 1 %}
    {{ lecture.last.Files }}
    {% else %}
    <ul>
    {% for member in lecture.last.Files %}
    <li>{{ member }}</li>
    {% endfor %}
    </ul>
    {% endif %}
  </td>
</tr>
{% endfor %}
</table>
