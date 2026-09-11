---
layout: archive
title: "Curriculum Vitae"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

<p><a href="{{ base_path }}/files/Sahar-Rahimi-resume.pdf">Download as PDF</a></p>

PhD researcher in computer vision and machine learning, with publications at
CVPR, ECCV and WACV and industry experience at CCC Intelligent Solutions and
Mayo Clinic. I work on representation learning, generative modeling, and
real-world vision systems at scale.

Education
======
* **Ph.D. in Electrical Engineering**, West Virginia University — Morgantown, WV, USA
  <br>Aug 2021 – present · GPA 4.0/4.0 · Advisor: [Prof. Nasser Nasrabadi](https://nassernasrabadi.faculty.wvu.edu/)
* **M.Sc. in Biomedical Engineering**, K. N. Toosi University of Technology — Tehran, Iran
  <br>Sep 2017 – Sep 2020 · GPA 4.0/4.0
* **B.Sc. in Electrical Engineering**, K. N. Toosi University of Technology — Tehran, Iran
  <br>Sep 2012 – Sep 2016 · GPA 3.5/4.0

Experience
======
* **Data Science Intern**, CCC Intelligent Solutions — Chicago, IL, USA
  <br>Sep 2025 – Dec 2025
  * Flow-matching generative modeling; synthetic data generation
  * Vehicle image classification; gradient-informed representation learning
  * Adaptation of vision foundation models

* **Data Science Intern**, Mayo Clinic (AI & Informatics) — Rochester, MN, USA
  <br>Jan 2025 – Aug 2025
  * Adaptation of vision foundation models to histopathology image analysis
  * Self-supervised, weakly supervised and representation learning
  * Cancer detection and subtyping; diffusion-based data augmentation
  * LLM-based information extraction from unstructured clinical text

Selected publications
======
{% assign selected = site.data.publications | slice: 0, 7 %}
{% for p in selected %}
* {% if p.arxiv %}[{{ p.title }}]({{ p.arxiv }}){% elsif p.link %}[{{ p.title }}]({{ p.link }}){% else %}{{ p.title }}{% endif %} — *{{ p.venue | split: "(" | first | strip }}*, {{ p.year }}
{% endfor %}

[See the full publication list →](/publications/)

Skills
======
* **Learning paradigms:** supervised, self-supervised, weakly supervised and unsupervised learning; deep representation and metric learning
* **Generative modeling:** diffusion models, flow matching
* **Computer vision:** classification, retrieval and recognition — face recognition, medical imaging, vehicle imagery
* **Data at scale:** large-scale, long-tail and noisy real-world datasets
* **Engineering:** distributed multi-GPU training with PyTorch; end-to-end ML pipelines; Python, PyTorch, Git

Projects
======
See [Projects](/portfolio/) for research tools and side projects I build and maintain.

References
======
Available upon request.
