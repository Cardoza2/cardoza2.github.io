---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

<!-- TODO: replace placeholders with your real CV details. To offer a PDF,
     upload it to /files/ (e.g. /files/adam-cardoza-cv.pdf) and uncomment: -->
<!-- <a href="{{ base_path }}/files/adam-cardoza-cv.pdf">Download as PDF</a> -->

Education
======
* Ph.D. in Mechanical Engineering, Brigham Young University, _expected 20XX_
* B.S. in Mechanical Engineering, _University_, _year_

Research interests
======
* Aeroelastic design optimization of wind turbines
* Gradient-based optimization &amp; efficient gradient computation (adjoint / AD)
* Deep-learning surrogate models for engineering design

Experience
======
* _Year–Year_: Graduate Research Assistant
  * Brigham Young University
  * _One line on what you worked on._
  * Advisor: _Name_

Skills
======
* Numerical analysis and scientific computing
* Programming: Julia (primary), Python, MATLAB, Fortran, C++, C#
* Gradient-based optimization, automatic differentiation, adjoint methods
* Deep learning / surrogate modeling

Publications
======
  <ul>{% for post in site.publications reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>

Teaching &amp; resources
======
  <ul>{% for post in site.teaching reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>

Awards and service
======
* _Awards, fellowships, reviewing, leadership, etc._
