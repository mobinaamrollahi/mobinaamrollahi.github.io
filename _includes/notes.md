---
layout: page
title: Notes
permalink: /notes/
---

<div class="container">
  <ol class="list-unstyled">

  {% for link in site.data.notes.main %}
  <li>
    <div class="pub-row row" style="margin-bottom:1rem;">
      <div class="col-sm-3 abbr" style="position: relative; padding-right: 15px; padding-left: 15px;">
        {% if link.image %}
          <img src="{{ link.image }}" alt="{{ link.title | escape }}"
               class="teaser img-fluid z-depth-1" style="width:100%; height:auto;">
          {% if link.conference_short %}
            <abbr class="badge">{{ link.conference_short }}</abbr>
          {% endif %}
        {% endif %}
      </div>

      <div class="col-sm-9" style="position: relative; padding-right: 15px; padding-left: 20px;">
        <div class="title">
          {% if link.pdf %}
            <a href="{{ link.pdf }}" target="_blank" rel="noopener">{{ link.title }}</a>
          {% else %}
            {{ link.title }}
          {% endif %}
        </div>

        {% if link.authors %}
          <div class="author">{{ link.authors }}</div>
        {% endif %}

        {% if link.conference %}
          <div class="periodical"><em>{{ link.conference }}</em></div>
        {% endif %}

        <div class="links" style="margin-top:6px;">
          {% if link.pdf %}
            <a href="{{ link.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" rel="noopener" style="font-size:12px;">PDF</a>
          {% endif %}
          {% if link.code %}
            <a href="{{ link.code }}" class="btn btn-sm z-depth-0" role="button" target="_blank" rel="noopener" style="font-size:12px;">Code</a>
          {% endif %}
          {% if link.page %}
            <a href="{{ link.page }}" class="btn btn-sm z-depth-0" role="button" target="_blank" rel="noopener" style="font-size:12px;">Project Page</a>
          {% endif %}
          {% if link.bibtex %}
            <a href="{{ link.bibtex }}" class="btn btn-sm z-depth-0" role="button" target="_blank" rel="noopener" style="font-size:12px;">BibTeX</a>
          {% endif %}
          {% if link.notes %}
            <strong><i style="color:#e74d3c">{{ link.notes }}</i></strong>
          {% endif %}
          {% if link.others %}
            {{ link.others }}
          {% endif %}
        </div>
      </div>
    </div>
  </li>
  {% endfor %}

  </ol>
</div>
