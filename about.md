---
title: About the task force
permalink: /about/
kicker: About
lead: >-
  The IEEE CIS Task Force on High Dimensional Data Analysis brings together researchers
  working on the theory, methods and applications of data whose dimensionality is large,
  often far larger than the number of available samples.
---

## Our mission

High dimensional data now arise in almost every area of science, engineering and business,
from genomics and biomedical imaging to astrophysics, finance and social networks. Such data
defeat intuitions built on low dimensional experience: distances concentrate, noise
accumulates, spurious correlations appear, and computation becomes expensive.

The task force works to understand these *curses*, to exploit the *blessings* of high
dimensionality, and to connect researchers across data mining, machine learning, statistics
and the application domains. See [Topics]({{ '/hdda-topics/' | relative_url }}) for the
questions we care about.

## What we do

- **HDM workshop series.** We organise the International Workshop on High Dimensional Data
  Mining, held with the IEEE International Conference on Data Mining (ICDM). The
  [13th edition, HDM'26]({{ '/2026/11/06/hdm26-high-dimensional-data-mining-workshop/' | relative_url }}),
  takes place in Shenyang, China.
- **Special sessions and tutorials** at IEEE conferences, such as the
  [special session at IEEE CIDM 2014]({{ '/2014/03/26/special-session-at-ieee-cidm-2014-on-high-dimensional-data-analysis-theoretical-advances-and-applications/' | relative_url }})
  and the [IJCNN 2015 tutorial on embedding methods]({{ '/2015/05/05/tutorial-at-ijcnn-on-embedding-methods/' | relative_url }}).
- **Seminars** that bring the community together, including the
  [Shonan seminar on data-dependent dissimilarity measures]({{ '/2017/08/28/shonan-seminar-scheduled-15-10-18-10-2018/' | relative_url }}) (2018).
- **A shared [reading list]({{ '/materials/' | relative_url }})** of influential material on
  high dimensional data analysis.

## Leadership

<div class="leaders">
{% assign leads = site.members | where_exp: "m", "m.role" %}
{% for r in site.data.leadership.current %}{% assign m = leads | where: "role", r.role | first %}
  <a class="leader" href="{{ m.url | relative_url }}">
    <span class="badge">{{ r.role }}{% if r.since %} · since {{ r.since }}{% endif %}</span>
    <span class="member-name">{{ m.name }}</span>
    <span class="member-inst">{{ m.institute }}, {{ m.country }}</span>
  </a>
{% endfor %}
</div>

### Former leadership

<ul class="former">
{% for f in site.data.leadership.former %}{% assign m = site.members | where: "name", f.name | first %}
  <li><a href="{{ m.url | relative_url }}">{{ f.name }}</a><span>{{ m.institute }}, {{ m.country }}{% if f.note %} · {{ f.note }}{% endif %}</span></li>
{% endfor %}
</ul>

## Get involved

We welcome researchers interested in high dimensional data. To join the task force, propose a
special session or workshop, or suggest additions to the reading list, please get in touch
with the [Chair]({{ '/members/jakramate-bootkrajang/' | relative_url }}).
