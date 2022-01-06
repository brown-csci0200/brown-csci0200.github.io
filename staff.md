---
layout: default
title: Staff
---

# {{ page.title }}

## Professors

{% assign professors = site.staff | where: 'role', 'Professor' %}
{% for staffer in professors %}
{{ staffer }}
{% endfor %}

{% assign HTAs = site.staff | where: 'role', 'HTA' %}
{% if HTAs.size != 0 %}
## HTAs

{% for staffer in HTAs %}
{{ staffer }}
{% endfor %}
{% endif %}

{% assign STAs = site.staff | where: 'role', 'STA' %}
{% if STAs.size != 0 %}
## STAs

{% for staffer in STAs %}
{{ staffer }}
{% endfor %}
{% endif %}

{% assign UTAs = site.staff | where: 'role', 'UTA' %}
{% if UTAs.size != 0 %}
## UTAs

{% for staffer in UTAs %}
{{ staffer }}
{% endfor %}
{% endif %}