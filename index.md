---
layout: default
title: Home
---

# {{ site.title }}
_Data science, ML, and MLOps projects_

<p style="margin-top:0.75rem;">I am a growing data scientist graduating from UC Berkeley in December 2025. My interest lies in implementing the agentic model framework in tax automation and retrieval based tax research engine.</p>

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

<a id="about"></a>
## About
I’m Wendy (Xueying). I design data/ML pipelines end-to-end—ingestion, training, eval, and serving—with a focus on clarity and reproducibility. Interests: agentic AI for tax workflows, RAG quality, K8s deployments, and graph ML for fMRI.

<a id="contact"></a>
## Contact
- Email: {{ wendytian.usc@gmail.com }}
- GitHub: [@{{ Wendy0756 }}](https://github.com/{{ site.author.github }})
- LinkedIn: [{{ wendytian2024ds }}](https://www.linkedin.com/in/{{ site.author.linkedin }}/)

<!-- lightweight page styles -->
<style>
/* page width */
.main-content { max-width: 980px; }
/* project grid */
.grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(260px, 1fr));
  gap: 16px;
  margin: 10px 0 24px 0;
}
.card {
  border: 1px solid #e6e8eb;
  border-radius: 14px;
  background: #fff;
  overflow: hidden;
  display: flex;
  flex-direction: column;
}
.thumb {
  width: 100%;
  height: 160px;
  object-fit: cover;
  background: #f6f8fa;
}
.card-body { padding: 14px; display: flex; flex-direction: column; gap: 10px; }
.card-title { display: flex; align-items: center; gap: 8px; }
.card-title h3 { margin: 0; font-size: 1.05rem; }
.pill { font-size: .75rem; background: #eaf5ff; color: #0969da; padding: 2px 8px; border-radius: 999px; }
.desc { margin: 0; color: #4b5563; }
.tags { display: flex; flex-wrap: wrap; gap: 6px; }
.tag { font-size: .72rem; background: #f2f4f7; padding: 2px 8px; border-radius: 999px; }
.links { display: flex; gap: 12px; }
.links a { text-decoration: none; border-bottom: 1px dotted; }
@media (prefers-color-scheme: dark) {
  .card { border-color: #2d333b; background: #0d1117; }
  .thumb { background: #161b22; }
  .desc { color: #9aa4ad; }
  .tag { background: #1f242d; }
  .pill { background: #13233a; color: #58a6ff; }
}
</style>
