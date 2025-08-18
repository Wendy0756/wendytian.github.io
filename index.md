---
layout: default
title: Home
---

# Wendy Tian
_Data science, ML, and Tax Automation projects_

<p style="margin-top:0.75rem;">I am a growing data scientist graduating from UC Berkeley in December 2025. My interest lies in implementing the agentic model framework in tax automation and the retrieval-based research engine in specialized topics.</p>

<a id="projects"></a>
## Projects

<div class="grid">
  {% for p in site.data.projects %}
  <div class="card">
    {% if p.image %}
      <img src="{{ p.image | relative_url }}" alt="{{ p.title }} screenshot" class="thumb">
    {% endif %}
    <div class="card-body">
      <div class="card-title">
        <h3>{{ p.title }}</h3>
        {% if p.timeframe %}<span class="pill">{{ p.timeframe }}</span>{% endif %}
      </div>
      <p class="desc">{{ p.description }}</p>
      {% if p.tech %}
      <div class="tags">
        {% for t in p.tech %}<span class="tag">{{ t }}</span>{% endfor %}
      </div>
      {% endif %}
      <div class="links">
        {% if p.repo %}<a href="{{ p.repo }}" target="_blank">GitHub ↗</a>{% endif %}
        {% if p.demo %}<a href="{{ p.demo }}" target="_blank">Live Demo ↗</a>{% endif %}
      </div>
    </div>
  </div>
  {% endfor %}
</div>

<a id="education"></a>
## Education
- Jan 2024 - Present: University of California, Berkeley | Master of Information and Data Science
- Jun 2016 - May 2017: University of Southern California | Master of Business Taxation
- Aug 2013 - Dec 2015: University of Illinois at Urbana-Champaign | Bachelor of Arts in Economics
- Aug 2011 - May 2013: Sun Yat-sen University | International Business School

<a id="contact"></a>
## Contact
- Email: wendytian.usc@gmail.com
- GitHub: [@ Wendy0756](https://github.com/Wendy0756)
- LinkedIn: [ wendytian2024ds ](https://www.linkedin.com/in/wendytian2024ds/)
