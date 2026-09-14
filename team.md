---
layout: page
title: Team
permalink: /team/
---


## Students

{% assign phd_students = site.team | where: "membership", "phd_student" | where: "current", true | sort: 'sort_name' %}
{% if phd_students.size > 0 %}
### PhD
{% include team-list.md members=phd_students %}
{% endif %}

{% assign ms_students = site.team | where: "membership", "ms_student" | where: "current", true | sort: 'sort_name' %}
{% if ms_students.size > 0 %}
### MS
{% include team-list.md members=ms_students %}
{% endif %}

{% assign ug_students = site.team | where: "membership", "undergrad_student" | where: "current", true | sort: 'sort_name' %}
{% if ug_students.size > 0 %}
### BS
{% include team-list.md members=ug_students %}
{% endif %}

<div style="margin-top: 4rem;"></div>
## Faculty
### Director
{% assign mattr = site.team | where: "membership", "faculty" | where: "name", "Matt Revelle" %}
{% include team-list.md members=mattr %}

{% assign aff_facultys = site.team | where: "membership", "faculty" | where_exp: "member", "member.name != 'Matt Revelle'", | where: "current", true | sort: 'sort_name' %}
{% if aff_facultys.size > 0 %}
### Affiliate
{% include team-list.md members=aff_facultys %}
{% endif %}

{% assign facultys = site.team | where: "membership", "faculty" | where: "current", true | sort: 'sort_name' %}

<!-- {% assign aff_facultys = site.team | where: "membership", "affiliated_faculty" | where: "current", true | sort: 'sort_name' %} -->
<!-- {% if aff_facultys.size > 0 %} -->
<!-- ## Affiliated Faculty -->
<!-- {% include team-list.md members=aff_facultys %} -->
<!-- {% endif %} -->

{% assign affiliates = site.team | where: "membership", "affiliate" | where: "current", true | sort: 'sort_name' %}
{% if affiliates.size > 0 %}
<div style="margin-top: 4rem;"></div>
## Research Affiliates
{% include team-list.md members=affiliates %}
{% endif %}

<div style="margin-top: 4rem;"></div>
---
<div style="margin-top: 4rem;"></div>

{% assign alumni = site.team | where: "current", false | sort: 'sort_name' %}
{% if alumni.size > 0 %}
## Alumni
{% include team-list.md members=alumni %}
{% endif %}
