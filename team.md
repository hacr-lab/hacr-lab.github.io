---
layout: page
title: Team
permalink: /team/
---


## Students

### PhD

{% assign phd_students = site.team | where: "membership", "phd_student" | sort: 'date' %}

{% for member in phd_students %}
{% if member.handle %}
### [{{ member.name }} ({{ member.handle }})]({{ member.url }})
{% else %}
### [{{ member.name }}]({{ member.url }})
{% endif %}
{% endfor %}

### MS

{% assign ms_students = site.team | where: "membership", "ms_student" | sort: 'date' %}

{% for member in ms_students %}
{% if member.handle %}
### [{{ member.name }} ({{ member.handle }})]({{ member.url }})
{% else %}
### [{{ member.name }}]({{ member.url }})
{% endif %}
{% endfor %}

### BS

{% assign ug_students = site.team | where: "membership", "undergrad_student" | sort: 'date' %}

{% for member in ug_students %}
{% if member.handle %}
### [{{ member.name }} ({{ member.handle }})]({{ member.url }})
{% else %}
### [{{ member.name }}]({{ member.url }})
{% endif %}
{% endfor %}

## Faculty

{% assign facultys = site.team | where: "membership", "faculty" | sort: 'date' %}

{% for member in facultys %}
{% if member.handle %}
### [{{ member.name }} ({{ member.handle }})]({{ member.url }})
{% else %}
### [{{ member.name }}]({{ member.url }})
{% endif %}
{% endfor %}
