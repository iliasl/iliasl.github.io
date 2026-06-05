---
layout: default
title: Publications
permalink: /publications/
---

<div class="stats-container">
  <div class="stat-item">
    <span class="stat-value">{{ site.data.publications.stats.citations | divided_by: 1000.0 | round: 1 }}k+</span>
    <span class="stat-label">Citations</span>
  </div>
  <div class="stat-item">
    <span class="stat-value">{{ site.data.publications.stats.h_index }}</span>
    <span class="stat-label">h-index</span>
  </div>
  <div class="stat-item">
    <span class="stat-value">15+</span>
    <span class="stat-label">Years Exp</span>
  </div>
</div>

<p style="text-align: center; color: #666; font-size: 0.9em; margin-bottom: 40px;">
  Latest updates from <a href="https://scholar.google.es/citations?user=HAOtV_AAAAAJ&hl=en" target="_blank">Google Scholar</a>. 
  Last synced: {{ site.data.publications.stats.last_updated | date: "%Y-%m-%d" }}
</p>

{% assign publications_by_year = site.data.publications.publications | group_by: "year" %}
{% assign sorted_years = publications_by_year | sort: "name" | reverse %}

{% for year_group in sorted_years %}
  <h2 class="year-heading">{{ year_group.name }}</h2>
  <div class="pub-list">
    {% for pub in year_group.items %}
      <div class="pub-item">
        <div class="pub-title">
          <a href="{{ pub.url }}" target="_blank">{{ pub.title }}</a>
        </div>
        <div class="pub-authors">{{ pub.authors }}</div>
        <div class="pub-venue">
          <em>{{ pub.venue }}</em>, {{ pub.year }}
          {% if pub.citations > 0 %}
            <span class="pub-citations"> — Cited by {{ pub.citations }}</span>
          {% endif %}
        </div>
      </div>
    {% endfor %}
  </div>
{% endfor %}

<style>
.stats-container {
  display: flex;
  justify-content: center;
  gap: 40px;
  margin: 40px 0 20px;
  padding: 20px;
  background: #f8f9fa;
  border-radius: 12px;
  border: 1px solid #eee;
}

.stat-item {
  text-align: center;
}

.stat-value {
  display: block;
  font-size: 2.5em;
  font-weight: 700;
  color: #204a87;
  line-height: 1;
}

.stat-label {
  display: block;
  font-size: 0.9em;
  color: #666;
  text-transform: uppercase;
  letter-spacing: 1px;
  margin-top: 5px;
}

.year-heading {
  margin-top: 50px;
  margin-bottom: 20px;
  border-bottom: 2px solid #204a87;
  padding-bottom: 5px;
  color: #333;
}

.pub-list {
  margin-bottom: 40px;
}

.pub-item {
  margin-bottom: 25px;
  padding-left: 15px;
  border-left: 3px solid #e9ecef;
}

.pub-title {
  font-weight: 600;
  font-size: 1.1em;
  margin-bottom: 4px;
}

.pub-title a {
  color: #204a87;
  text-decoration: none;
}

.pub-title a:hover {
  text-decoration: underline;
}

.pub-authors {
  color: #444;
  font-size: 0.95em;
  margin-bottom: 2px;
  display: -webkit-box;
  -webkit-line-clamp: 4;
  -webkit-box-orient: vertical;
  overflow: hidden;
}

.pub-venue {
  color: #666;
  font-size: 0.9em;
}

.pub-citations {
  color: #28a745;
  font-weight: 600;
}

@media (max-width: 600px) {
  .stats-container {
    gap: 20px;
    flex-wrap: wrap;
  }
  .stat-value {
    font-size: 1.8em;
  }
}
</style>
