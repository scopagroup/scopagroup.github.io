---
layout: default
title: "Publications"
permalink: /publications/
---

# Publications & Presentations

Below you can find the publications, talks, and posters of members of the SCOPA lab. A more complete list of publications can be found on the [Google Scholar profile](https://scholar.google.com/citations?user=CJc0_msAAAAJ) of the lab director.

<div class="pub-filters">
  <div class="pub-filter-group" role="group" aria-label="Filter by type">
    <button type="button" class="pub-filter active" data-filter-type="all" aria-pressed="true">All</button>
    <button type="button" class="pub-filter" data-filter-type="journal" aria-pressed="false">Journal</button>
    <button type="button" class="pub-filter" data-filter-type="preprint" aria-pressed="false">Preprint</button>
    <button type="button" class="pub-filter" data-filter-type="conference" aria-pressed="false">Conference</button>
    <button type="button" class="pub-filter" data-filter-type="book" aria-pressed="false">Book</button>
    <button type="button" class="pub-filter" data-filter-type="bookchapter" aria-pressed="false">Chapter</button>
    <button type="button" class="pub-filter" data-filter-type="talk" aria-pressed="false">Talk</button>
    <button type="button" class="pub-filter" data-filter-type="poster" aria-pressed="false">Poster</button>
  </div>
</div>

<section class="output-section" id="section-publications">
<h2>Publications</h2>
<ul class="pub-list">
{%- for pub in site.data.publications %}
  <li class="pub-item" data-category="{{ pub.category }}">
    <div class="pub-title">{{ pub.title | escape }}</div>
    <div class="pub-meta">{{ pub.authors | escape }}{% if pub.venue != "" %}. {{ pub.venue | escape }}{% endif %}.</div>
    <div class="pub-links">
      {%- if pub.category == "bookchapter" %}<span class="pub-category bookchapter">chapter</span>
      {%- else %}<span class="pub-category {{ pub.category }}">{{ pub.category }}</span>
      {%- endif %}
      {%- if pub.doi %}<a href="{{ pub.doi }}">doi</a>{% endif %}
      {%- if pub.arxiv %}<a href="{{ pub.arxiv }}">arXiv</a>{% endif %}
    </div>
  </li>
{%- endfor %}
</ul>
</section>

<section class="output-section" id="section-talks">
<h2>Talks</h2>
<ul class="pub-list">
{%- for talk in site.data.talks %}
  <li class="pub-item" data-category="talk">
    <div class="pub-title">{{ talk.title | escape }}</div>
    <div class="pub-meta">{{ talk.speaker | escape }}. {{ talk.kind | escape }}{% if talk.host %} (host: {{ talk.host | escape }}){% endif %} at {{ talk.venue | escape }}{% if talk.acronym or talk.session %} ({% if talk.acronym %}{{ talk.acronym | escape }}{% if talk.session %}; {% endif %}{% endif %}{% if talk.session %}Session: {{ talk.session | escape }}{% endif %}){% endif %}, {{ talk.location | escape }}, {{ talk.year }}.</div>
    <div class="pub-links"><span class="pub-category talk">talk</span></div>
  </li>
{%- endfor %}
</ul>
</section>

<section class="output-section" id="section-posters">
<h2>Posters</h2>
<ul class="pub-list">
{%- for poster in site.data.posters %}
  <li class="pub-item" data-category="poster">
    <div class="pub-title">{{ poster.title | escape }}</div>
    <div class="pub-meta">{{ poster.speaker | escape }}. Poster at {{ poster.venue | escape }}{% if poster.acronym %} ({{ poster.acronym | escape }}){% endif %}, {{ poster.location | escape }}, {{ poster.year }}.</div>
    <div class="pub-links"><span class="pub-category poster">poster</span></div>
  </li>
{%- endfor %}
</ul>
</section>

<p class="pub-empty" hidden>No entries match the selected filter.</p>

<script>
(function () {
  var typeBtns = Array.prototype.slice.call(document.querySelectorAll('.pub-filter'));
  var sections = Array.prototype.slice.call(document.querySelectorAll('.output-section'));
  var items = Array.prototype.slice.call(document.querySelectorAll('.pub-item'));
  var empty = document.querySelector('.pub-empty');
  var curType = 'all';

  function apply() {
    var visible = 0;
    items.forEach(function (it) {
      var show = curType === 'all' || it.getAttribute('data-category') === curType;
      it.hidden = !show;
      if (show) { visible++; }
    });
    sections.forEach(function (sec) {
      var shown = sec.querySelectorAll('.pub-item:not([hidden])').length;
      sec.hidden = shown === 0;
    });
    if (empty) { empty.hidden = visible !== 0; }
  }

  typeBtns.forEach(function (btn) {
    btn.addEventListener('click', function () {
      curType = this.getAttribute('data-filter-type');
      typeBtns.forEach(function (b) {
        var active = b === btn;
        b.classList.toggle('active', active);
        b.setAttribute('aria-pressed', active ? 'true' : 'false');
      });
      apply();
    });
  });
})();
</script>
