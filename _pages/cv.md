---
layout: archive
title: "Curriculum Vitae"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

*This is a template CV. Replace the entries below with your own education, appointments, and academic service.*

## Education

- **Ph.D. in Mathematics**, Your Institution, Your City, 20XX–present.
- **M.S. in Mathematics**, Your Institution, Your City, 20XX–20XX.
- **B.S. in Mathematics**, Your Institution, Your City, 20XX–20XX.

## Research Interests

Complex geometry, deformation theory, Hodge theory, and Calabi–Yau manifolds.

## Publications and Preprints

<ul>{% for post in site.publications reversed %}
  {% include archive-single-cv.html %}
{% endfor %}</ul>

## Academic Activities

<ul>{% for post in site.talks reversed %}
  {% include archive-single-talk-cv.html %}
{% endfor %}</ul>

## Teaching

- **Course title**, Your Institution, term and year.

## Academic Service

- Seminar or reading-group organization, Your Institution, year.

## Languages and Skills

- Add your languages, technical skills, or other relevant information here.
