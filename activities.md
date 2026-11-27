---
title: Activities
permalink: /activities/
kicker: What we do
lead: >-
  Workshops, special sessions, tutorials and seminars organised by the task force,
  newest first.
---

{% comment %}Entries live in _data/activities.yml; this page only lays them out.{% endcomment %}
{% assign sections = "Workshops|Special sessions|Tutorials|Seminars" | split: "|" %}
{% for s in sections %}
{% assign items = site.data.activities | where: "type", s | sort: "year" | reverse %}
{% if items.size > 0 %}
<h2 id="{{ s | slugify }}">{{ s }}</h2>
{% if s == "Workshops" %}<p>The <strong>HDM workshop series</strong> (High Dimensional Data Mining) is held with the
IEEE International Conference on Data Mining (ICDM).</p>{% endif %}
<ul>
{% for a in items %}{% if a.url contains "://" %}{% assign href = a.url %}{% else %}{% assign href = a.url | relative_url %}{% endif %}
  <li><strong>{{ a.year }} · <a href="{{ href }}">{{ a.title }}</a></strong>{% if a.venue %}, {{ a.venue }}{% endif %}.{% if a.note %} {{ a.note }}{% endif %}</li>
{% endfor %}
</ul>
{% endif %}
{% endfor %}

## Propose an activity

Members are welcome to propose a workshop, special session or tutorial under the task force.
Please get in touch with the [Chair]({{ '/members/jakramate-bootkrajang/' | relative_url }}).
