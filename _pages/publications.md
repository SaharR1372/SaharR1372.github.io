---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% include base_path %}

For the most current list, see my
[Google Scholar profile]({{ site.author.googlescholar }}).

{% assign pubs = site.data.publications %}
{% assign years = pubs | map: "year" | uniq | sort | reverse %}

{% for year in years %}
  <h2 id="y{{ year }}" style="margin-top:1.6em">{{ year }}</h2>
  <ul style="list-style:none; padding-left:0">
  {% for p in pubs %}{% if p.year == year %}
    <li style="margin-bottom:1.1em">
      <strong>
        {% if p.arxiv %}<a href="{{ p.arxiv }}">{{ p.title }}</a>
        {% elsif p.link %}<a href="{{ p.link }}">{{ p.title }}</a>
        {% else %}{{ p.title }}{% endif %}
      </strong>
      {% if p.me %}<span title="First author" style="font-size:.75em; vertical-align:middle; border:1px solid #bbb; border-radius:3px; padding:0 .35em; margin-left:.3em; color:#666">first author</span>{% endif %}
      <br>
      <span style="font-size:.92em">
        {{ p.authors | replace: "Sahar Rahimi Malakshan", "<b>Sahar Rahimi Malakshan</b>" | replace: "Sahar Rahimi Malekshan", "<b>Sahar Rahimi Malekshan</b>" }}
      </span>
      <br>
      <em style="font-size:.92em">{{ p.venue }}</em>, {{ p.year }}
      {% if p.arxiv or p.link or p.code %}
      <span style="font-size:.88em">
        &nbsp;·&nbsp;
        {% if p.arxiv %}<a href="{{ p.arxiv }}">arXiv</a>{% endif %}
        {% if p.link %}{% if p.arxiv %} · {% endif %}<a href="{{ p.link }}">publisher</a>{% endif %}
        {% if p.code %} · <a href="{{ p.code }}">code</a>{% endif %}
      </span>
      {% endif %}
    </li>
  {% endif %}{% endfor %}
  </ul>
{% endfor %}
