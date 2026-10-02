---
layout: default
title: Home
---
<section class="hero">
  <div class="hero-copy">
    <p class="eyebrow"><span class="status-dot" aria-hidden="true"></span> A PERSONAL SITE, ALWAYS IN PROGRESS</p>
    <h1>Stay curious.<br>Build with<br><em>purpose.</em></h1>
    <p class="hero-intro">I'm Jose — a quality engineer, pilot, bassist, and follower of Christ. I like understanding how things work. Then making them work better.</p>
    <div class="hero-actions"><a class="button" href="{{ '/blog/' | relative_url }}">Read the journal <span aria-hidden="true">↗</span></a><a class="text-link" href="{{ '/about/' | relative_url }}">A little about me →</a></div>
  </div>
  <aside class="lab-card" aria-labelledby="lab-title">
    <div class="lab-top"><span>FIELD NOTES / 001</span><span aria-hidden="true">● ● ●</span></div>
    <div class="lab-body">
      <p class="eyebrow">CURRENT EXPLORATION</p><h2 id="lab-title">A little lab.<br>A lot to learn.</h2>
      <div class="lab-diagram" aria-label="Planned home lab: UniFi network connects to an AtomMan G7 Pro running Proxmox, hosting Home Assistant, Jellyfin, and Immich.">
        <div class="network-node"><span class="node-icon" aria-hidden="true">↔</span><div><strong>UniFi</strong><small>THE NETWORK</small></div></div>
        <div class="diagram-line" aria-hidden="true"></div>
        <div class="server-node"><span class="node-icon" aria-hidden="true">▤</span><div><strong>AtomMan G7 Pro</strong><small>PROXMOX / FIRST SERVER</small></div><span class="server-lights" aria-hidden="true">•••</span></div>
        <div class="diagram-line" aria-hidden="true"></div>
        <div class="service-nodes"><span>Home<br>Assistant</span><span>Jellyfin</span><span>Immich</span></div>
      </div>
      <p class="lab-caption">Next up: self-hosting, GPU experiments,<br>and learning by doing.</p>
    </div>
    <div class="lab-bottom"><span>PROJECT STATUS</span><strong>GETTING STARTED ↗</strong></div>
  </aside>
</section>
<div class="interest-strip"><span>01 / FAITH</span><span>02 / FLIGHT</span><span>03 / CODE</span><span>04 / MUSIC</span></div>
<section class="journal-section" aria-labelledby="journal-title">
  <div class="section-heading"><div><p class="eyebrow">NOTES FROM THE WORKBENCH</p><h2 id="journal-title">The latest chapter.</h2></div><a class="text-link" href="{{ '/blog/' | relative_url }}">All entries ↗</a></div>
  {% assign latest = site.posts.first %}{% if latest %}
  <article class="featured-post"><div class="feature-index" aria-hidden="true">01<span>JOURNAL<br>ENTRY</span></div><div><p class="post-meta"><time datetime="{{ latest.date | date_to_xmlschema }}">{{ latest.date | date: '%b %-d, %Y' }}</time> / {{ latest.categories | join: ' + ' | escape }}</p><h3><a href="{{ latest.url | relative_url }}">{{ latest.title | escape }}</a></h3><p>{{ latest.description | default: latest.excerpt | strip_html }}</p><a class="text-link" href="{{ latest.url | relative_url }}">Read the story →</a></div></article>
  {% endif %}
</section>
<section class="values-section" aria-labelledby="values-title"><div><p class="eyebrow">THE THREAD THROUGH IT ALL</p><h2 id="values-title">Different interests.<br>Same intention.</h2></div><div><p>At GE Aerospace, I work on software quality. In the cockpit, I practice precision. On bass, I listen and serve the song. And in my faith, I find the foundation for all of it.</p><p>This is a place to share what I'm building, what I'm learning, and the things that give the work meaning.</p><a class="text-link" href="{{ '/about/' | relative_url }}">Get to know me →</a></div></section>
<blockquote class="faith-note"><p>“I can do all things through Christ who strengthens me.”</p><cite>PHILIPPIANS 4:13</cite></blockquote>
