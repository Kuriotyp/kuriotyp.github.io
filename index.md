---
layout: default
title: Kuriotyp
---
<p class="lead">Felietony technologiczno-kulturowe Marcina Zręda.</p>

<ul class="archiwum">
{% assign wpisy = site.posts | sort: "numer" | reverse %}
{% for p in wpisy %}
  <li>
    <span class="nr">#{{ p.numer }} · {% include data.html d=p.date %}</span>
    <a class="tytul" href="{{ p.url | relative_url }}">{{ p.title }}</a>
    {% if p.opis %}<p>{{ p.opis }}</p>{% endif %}
  </li>
{% endfor %}
</ul>
