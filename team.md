---
layout: page
title: Team
permalink: /team/
---


## Students

{% assign phd_students = site.team | where: "membership", "phd_student" | sort: 'sort_name' %}
{% if phd_students.size > 0 %}
### PhD
{% include team-list.md members=phd_students %}
{% endif %}

{% assign ms_students = site.team | where: "membership", "ms_student" | sort: 'sort_name' %}
{% if ms_students.size > 0 %}
### MS
{% include team-list.md members=ms_students %}
{% endif %}

{% assign ug_students = site.team | where: "membership", "undergrad_student" | sort: 'sort_name' %}
{% if ug_students.size > 0 %}
### BS
{% include team-list.md members=ug_students %}
{% endif %}

{% assign facultys = site.team | where: "membership", "faculty" | sort: 'sort_name' %}
{% if facultys.size > 0 %}
## Faculty
{% include team-list.md members=facultys %}
{% endif %}

{% assign alumni = site.team | where: "membership", "alumnus" | sort: 'sort_name' %}
{% if alumni.size > 0 %}
## Alumni
{% include team-list.md members=alumni %}
{% endif %}
