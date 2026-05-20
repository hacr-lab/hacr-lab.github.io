{% for member in include.members %}
<div class="team-member">
{% if member.image %}<img class="team-portrait" src="{{ member.image | relative_url }}" alt="{{ member.name }}">{% endif %}
<div class="team-member-info">
{% if member.handle %}
<h3><a href="{{ member.url | relative_url }}">{{ member.name }} ({{ member.handle }})</a></h3>
{% else %}
<h3><a href="{{ member.url | relative_url }}">{{ member.name }}</a></h3>
{% endif %}
</div>
</div>
{% endfor %}
