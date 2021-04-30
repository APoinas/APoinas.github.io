---
permalink: "/publications/"
layout: home
classes: wide
author_profile: true
title: "Publications"
---

{% if site.author.academic_profiles.google-scholar %}
  <a href="{{ site.author.academic_profiles.google-scholar }}">
    <i class="ai ai-google-scholar" aria-hidden="true"></i>Scholar
  </a>
{% endif %}
{% if site.author.academic_profiles.orcid %}
  <a href="{{ site.author.academic_profiles.orcid }}">
    <i class="ai ai-orcid" aria-hidden="true"></i>Orcid
  </a>
{% endif %}
{% if site.author.academic_profiles.hal %}
  <a href="{{ site.author.academic_profiles.hal }}">
    <i class="ai ai-hal" aria-hidden="true"></i>HAL
  </a>
{% endif %}
{% if site.author.academic_profiles.arxiv %}
  <a href="{{ site.author.academic_profiles.arxiv }}">
    <i class="ai ai-arxiv" aria-hidden="true"></i>Arxiv
  </a>
{% endif %}

<!-- See also https://github.com/inukshuk/jekyll-scholar to customize your references -->

<!-- Journal articles -->
{% capture counter_article %}
  {% bibliography_count --query @article %}
{% endcapture %}
{% if counter_article != "0" %}
  <h2>Journal articles</h2>
  {% bibliography --query @article %}
{% endif %}

<!-- Preprints -->
{% capture counter_preprints %}
  {% bibliography_count --query @unpublished %}
{% endcapture %}
{% if counter_preprints != "0" %}
  <h2>Preprints</h2>
  {% bibliography --query @unpublished %}
{% endif %}

<!-- Thesis -->
{% capture counter_thesis %}
  {% bibliography_count --query @thesis %}
{% endcapture %}
{% if counter_thesis != "0" %}
  <h2>Thesis</h2>
  {% bibliography --query @thesis %}
{% endif %}
