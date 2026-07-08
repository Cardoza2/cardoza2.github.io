---
permalink: /
title: "Adam Cardoza"
excerpt: "PhD candidate in Mechanical Engineering — aeroelastic analysis, gradient-based design optimization, and deep-learning surrogates."
layout: splash
author_profile: false
redirect_from:
  - /about/
  - /about.html
header:
  overlay_color: "#1b3a5b"
  overlay_filter: "0.05"
  overlay_image: hero_watertunnel.jpg   # just the filename — the theme prepends /images/
  # cta_label: "Read my research"
  # cta_url: "/research/"
---

<!--
  Custom landing page. No sidebar (author_profile: false), a hero banner above
  (from the `header:` front matter), then the section cards below.
  Swap `overlay_image` for your own hero image when ready.
-->

<style>
  /* ── Hero text position knobs ─────────────────────────────────────────
     Tweak these four values by hand; save and the browser reloads.        */
  .page__hero--overlay {
    display: flex;
    flex-direction: column;
    justify-content: flex-end;  /* VERTICAL anchor: flex-start=top, center=middle, flex-end=bottom */
    min-height: 70vh;           /* HERO HEIGHT: smaller (e.g. 45vh) = shorter banner, larger = taller */
    padding-bottom: 1em;        /* GAP from the bottom edge (raise the text off the bottom) */
  }
  .page__hero--overlay .wrapper {
    width: 100%;
    padding-left: 1em;          /* HORIZONTAL: increase to push text right, off the left edge */
  }

  .landing-intro { max-width: 760px; margin: 1.5em auto 0; text-align: center; }
  .landing-intro p { font-size: 1.15em; line-height: 1.6; }
  .section-cards {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    gap: 1.1em;
    max-width: 1000px;
    margin: 2.2em auto 1em;
    padding: 0 1em;
  }
  .section-card {
    display: block;
    padding: 1.4em 1.3em;
    border: 1px solid #e2e8ee;
    border-radius: 10px;
    text-decoration: none !important;
    color: inherit;
    transition: transform .12s ease, box-shadow .12s ease, border-color .12s ease;
    background: #fff;
  }
  .section-card:hover {
    transform: translateY(-3px);
    box-shadow: 0 8px 24px rgba(27,58,91,.12);
    border-color: #2a6f97;
  }
  .section-card .card-title { font-size: 1.2em; font-weight: 700; color: #1b3a5b; margin-bottom: .35em; }
  .section-card .card-desc  { font-size: .95em; color: #5a6b7b; line-height: 1.45; }
</style>

<div class="landing-intro" markdown="1">

I design aeroelastic analysis software for design optimization. I specialized in using
large-scale gradient-based optimization and deep-learning surrogates. 
I love food, hiking, dancing, and my family (shoutout to my wife and 2 daughters). 

</div>

<div class="section-cards">
  <a class="section-card" href="{{ '/research/' | relative_url }}">
    <div class="card-title">Research →</div>
    <div class="card-desc">Aeroelastic design optimization, gradient computation, and ML surrogates.</div>
  </a>
  <a class="section-card" href="{{ '/publications/' | relative_url }}">
    <div class="card-title">Publications →</div>
    <div class="card-desc">Papers, preprints, and conference work.</div>
  </a>
  <a class="section-card" href="{{ '/portfolio/' | relative_url }}">
    <div class="card-title">Projects →</div>
    <div class="card-desc">Research software and tools I've built.</div>
  </a>
  <a class="section-card" href="{{ '/cv/' | relative_url }}">
    <div class="card-title">CV →</div>
    <div class="card-desc">Education, experience, and skills.</div>
  </a>
  <a class="section-card" href="{{ '/teaching/' | relative_url }}">
    <div class="card-title">Resources →</div>
    <div class="card-desc">Teaching and educational material.</div>
  </a>
</div>
