---
layout: page
title: "SwissDataExplorers"
subtitle: "Innovation Footprints in Tech Stock Markets"
---

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;600;700&family=Source+Sans+3:wght@400;600;700&display=swap" rel="stylesheet">

<script>
  window.MathJax = {
    tex: { inlineMath: [["\\(", "\\)"], ["$", "$"]] },
    options: { skipHtmlTags: ["script", "style", "noscript", "textarea"] }
  };
</script>
<script defer src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>

<style>
:root {
  --bg: #050814;
  --panel: #0d1024;
  --panel-alt: #0f1530;
  --border: rgba(255, 255, 255, 0.08);
  --accent-2: #ffc46a;
  --muted: #9fb0ff;
  --text: #e8edff;
}

html {
  background: var(--bg);
}

body {
  background: radial-gradient(circle at 20% 20%, #0f1a3d 0, transparent 30%),
              radial-gradient(circle at 80% 10%, #0c3650 0, transparent 24%),
              radial-gradient(circle at 40% 70%, #1b1645 0, transparent 24%),
              #050814;
  color: var(--text);
  font-family: "Source Sans 3", "Helvetica Neue", Arial, sans-serif;
}

/* Bulma sets titles to dark gray by default; override for our dark theme. */
.content {
  color: var(--text);
}

.content .title,
.content .subtitle,
.content h1,
.content h2,
.content h3,
.content h4,
.content h5,
.content h6 {
  color: #f7f9ff;
}

strong {
  color: var(--muted);
}

a {
  color: var(--muted);
}

a:hover {
  color: #d9e2ff;
}

@keyframes slowDrift {
  0% { transform: translate3d(0,0,0) scale(1); opacity: 0.35; }
  50% { transform: translate3d(12px, -10px, 0) scale(1.05); opacity: 0.45; }
  100% { transform: translate3d(0,0,0) scale(1); opacity: 0.35; }
}

.navbar {
  background: rgba(5, 8, 20, 0.78) !important;
  backdrop-filter: blur(16px);
  -webkit-backdrop-filter: blur(16px);
  border-bottom: 1px solid var(--border);
  box-shadow: 0 20px 45px rgba(0, 0, 0, 0.45);
  position: sticky;
  top: 0;
  z-index: 20;
  padding: 0.35rem 0;
}

@supports not ((-webkit-backdrop-filter: blur(0)) or (backdrop-filter: blur(0))) {
  .navbar {
    background: rgba(5, 8, 20, 0.95) !important;
  }
}

.footer {
  display: none !important;
}

.navbar .navbar-brand .navbar-item {
  font-family: "Space Grotesk", "Source Sans 3", sans-serif;
  font-weight: 700;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  color: #f7f9ff !important;
}

.navbar a.navbar-item,
.navbar .navbar-item,
.navbar a.navbar-item:visited,
.navbar .navbar-link {
  color: var(--muted) !important;
  font-weight: 600;
  letter-spacing: -0.01em;
  position: relative;
  transition: color 0.2s ease, transform 0.2s ease;
  padding: 0.75rem 0.95rem;
}

.navbar .navbar-item::after,
.navbar .navbar-link::after {
  content: "";
  position: absolute;
  left: 0;
  bottom: 0.4rem;
  width: 100%;
  height: 2px;
  background: linear-gradient(120deg, var(--muted), #d9e2ff);
  border-radius: 999px;
  opacity: 0;
  transform: translateY(6px);
  transition: opacity 0.2s ease, transform 0.2s ease;
}

.navbar .navbar-item:hover,
.navbar .navbar-link:hover {
  color: #f7f9ff !important;
  transform: translateY(-1px);
}

.navbar .navbar-item:hover::after,
.navbar .navbar-link:hover::after {
  opacity: 1;
  transform: translateY(0);
}

.navbar .navbar-item.is-active,
.navbar .navbar-link.is-active {
  color: var(--muted) !important;
}

.navbar .navbar-item.is-active::after,
.navbar .navbar-link.is-active::after {
  opacity: 1;
  transform: translateY(0);
}

/* Hide theme hero so we can use our own. */
body > section.hero.is-primary {
  display: none !important;
}

hr {
  border: none;
  border-top: 1px solid var(--border);
  margin: 2.5rem 0;
}

blockquote {
  margin: 1.2rem 0;
  padding: 1.05rem 1.2rem;
  border-radius: 16px;
  border: 1px solid var(--border);
  border-left: 4px solid rgba(159, 176, 255, 0.7);
  background: radial-gradient(circle at 10% 20%, rgba(159, 176, 255, 0.12), transparent 55%),
              radial-gradient(circle at 90% 10%, rgba(255, 196, 106, 0.12), transparent 45%),
              rgba(13, 16, 36, 0.74);
  box-shadow: 0 16px 40px rgba(0, 0, 0, 0.32);
  color: var(--text);
}

blockquote p {
  margin: 0.6rem 0;
}

/* Bulma styles `.content blockquote` with a light background; override it explicitly. */
.content blockquote {
  margin: 1.2rem 0;
  padding: 1.05rem 1.2rem;
  border-radius: 16px;
  border: 1px solid var(--border);
  border-left: 4px solid rgba(159, 176, 255, 0.7);
  background: radial-gradient(circle at 10% 20%, rgba(159, 176, 255, 0.12), transparent 55%),
              radial-gradient(circle at 90% 10%, rgba(255, 196, 106, 0.12), transparent 45%),
              rgba(13, 16, 36, 0.74);
  box-shadow: 0 16px 40px rgba(0, 0, 0, 0.32);
  color: var(--text);
}

.content blockquote strong,
blockquote strong {
  color: #f7f9ff;
}

.sdx-section {
  padding: 3rem 0 2.5rem;
}

.sdx-section.alt {
  background: rgba(13, 16, 36, 0.55);
  border: 1px solid var(--border);
  border-radius: 18px;
  padding: 2.8rem;
}

.sdx-pill {
  display: inline-flex;
  align-items: center;
  gap: 0.4rem;
  padding: 0.4rem 0.85rem;
  border: 1px solid var(--border);
  border-radius: 999px;
  background: rgba(13, 16, 36, 0.6);
  font-weight: 600;
  color: var(--muted);
  font-size: 0.9rem;
}

.sdx-hero-panel {
  margin-top: -60px;
  background: linear-gradient(145deg, rgba(15, 21, 48, 0.9), rgba(13, 16, 36, 0.85));
  border: 1px solid var(--border);
  border-radius: 24px;
  padding: 2.5rem;
  box-shadow: 0 30px 80px rgba(0, 0, 0, 0.45);
  position: relative;
  overflow: hidden;
}

.sdx-hero-panel::before,
.sdx-hero-panel::after {
  content: "";
  position: absolute;
  width: 220px;
  height: 220px;
  border-radius: 50%;
  filter: blur(50px);
  opacity: 0.32;
}

.sdx-hero-panel::before {
  background: var(--muted);
  top: -80px;
  right: -80px;
  animation: slowDrift 18s ease-in-out infinite;
}

.sdx-hero-panel::after {
  background: var(--accent-2);
  bottom: -80px;
  left: -80px;
  animation: slowDrift 22s ease-in-out infinite reverse;
}

.sdx-hero-grid {
  display: grid;
  gap: 1.8rem;
  grid-template-columns: 1.1fr 0.9fr;
}

.sdx-hero-title {
  font-family: "Space Grotesk", "Source Sans 3", sans-serif;
  font-weight: 700;
  letter-spacing: -0.02em;
  font-size: 2.35rem;
  color: #f7f9ff;
  margin: 0.75rem 0;
}

.sdx-hero-body {
  color: var(--text);
  opacity: 0.94;
  font-size: 1.05rem;
}

.sdx-hero-actions {
  display: flex;
  flex-wrap: wrap;
  gap: 0.8rem;
  margin-top: 1.6rem;
}

.sdx-btn {
  border-radius: 12px;
  padding: 0.85rem 1.25rem;
  font-weight: 700;
  letter-spacing: -0.01em;
  border: 1px solid transparent;
}

.sdx-btn-primary {
  background: linear-gradient(120deg, var(--muted), #d9e2ff);
  color: #041022;
  box-shadow: 0 12px 30px rgba(159, 176, 255, 0.25);
  border: none;
}

.sdx-btn-ghost {
  background: transparent;
  border: 1px solid var(--border);
  color: var(--text);
}

.sdx-hero-badge {
  display: grid;
  gap: 1rem;
  padding: 1.4rem;
  border-radius: 16px;
  background: rgba(13, 16, 36, 0.72);
  border: 1px solid var(--border);
}

.sdx-hero-badge h4 {
  font-family: "Space Grotesk", "Source Sans 3", sans-serif;
  font-weight: 700;
  letter-spacing: -0.02em;
  margin: 0;
  color: #f7f9ff;
}

.sdx-hero-media {
  position: relative;
  border-radius: 18px;
  overflow: hidden;
  border: 1px solid var(--border);
  min-height: 380px;
  box-shadow: 0 30px 80px rgba(0, 0, 0, 0.45);
  background: rgba(13, 16, 36, 0.72);
}

.sdx-hero-media-img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  display: block;
  transform: scale(1.04);
  filter: saturate(1.05) contrast(1.05);
}

.sdx-hero-media::after {
  content: "";
  position: absolute;
  inset: 0;
  background: linear-gradient(135deg, rgba(5, 8, 20, 0.22), rgba(5, 8, 20, 0.86) 66%);
  z-index: 0;
}

.sdx-hero-media-overlay {
  position: absolute;
  inset: 0;
  padding: 1.25rem;
  display: flex;
  align-items: flex-end;
  z-index: 1;
}

.sdx-hero-media-card {
  width: 100%;
  border-radius: 16px;
  border: 1px solid var(--border);
  background: rgba(13, 16, 36, 0.78);
  box-shadow: 0 16px 40px rgba(0, 0, 0, 0.32);
  padding: 1.15rem 1.15rem 1.1rem;
  backdrop-filter: blur(10px);
  -webkit-backdrop-filter: blur(10px);
}

.sdx-hero-media-card h4 {
  margin: 0;
  font-family: "Space Grotesk", "Source Sans 3", sans-serif;
  font-weight: 700;
  letter-spacing: -0.02em;
  color: #f7f9ff;
}

.sdx-hero-media-card p {
  margin: 0.55rem 0 0;
  color: var(--text);
}

.sdx-hero-meta {
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
  margin-top: 0.85rem;
}

.sdx-hero-media-card .sdx-note {
  margin: 0.8rem 0 0;
}

.sdx-hero-stats {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
  gap: 0.75rem;
}

.sdx-mini-stat {
  border-radius: 12px;
  border: 1px solid var(--border);
  padding: 0.8rem 0.9rem;
  background: rgba(15, 21, 48, 0.65);
}

.sdx-mini-stat .label {
  font-size: 0.85rem;
  color: var(--muted);
}

.sdx-mini-stat .value {
  font-family: "Space Grotesk", "Source Sans 3", sans-serif;
  font-size: 1.4rem;
  color: #f7f9ff;
}

.sdx-panel,
.sdx-card {
  background: rgba(13, 16, 36, 0.72);
  border: 1px solid var(--border);
  border-radius: 18px;
  padding: 1.5rem;
  height: 100%;
  box-shadow: 0 16px 40px rgba(0, 0, 0, 0.3);
  transition: transform 0.3s ease, box-shadow 0.3s ease, border-color 0.3s ease;
}

.sdx-panel {
  height: auto;
}

.sdx-panel + .sdx-panel {
  margin-top: 1.25rem;
}

.sdx-panel:hover,
.sdx-card:hover {
  transform: translateY(-4px);
  border-color: rgba(159, 176, 255, 0.45);
  box-shadow: 0 22px 50px rgba(0, 0, 0, 0.35);
}

.sdx-grid-cards {
  display: grid;
  gap: 1rem;
  grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
}

.sdx-list {
  padding-left: 1.1rem;
  margin: 0.6rem 0;
}

.sdx-list li {
  padding: 0.12rem 0;
}

.sdx-case-grid {
  display: grid;
  gap: 1rem;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  align-items: stretch;
  margin-top: 1.25rem;
}

.sdx-case-card {
  border-radius: 16px;
  padding: 1.3rem 1.4rem;
  background: linear-gradient(150deg, rgba(159, 176, 255, 0.08), rgba(255, 196, 106, 0.09));
  border: 1px solid var(--border);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  gap: 0.75rem;
  position: relative;
  overflow: hidden;
}

.sdx-case-card .title {
  margin: 0;
}

.sdx-case-card p {
  margin: 0;
}

.sdx-case-card .sdx-note {
  margin-top: auto;
}

.sdx-case-card-wide {
  grid-column: 1 / -1;
}

.sdx-case-card:hover {
  transform: translateY(-4px);
  box-shadow: 0 24px 60px rgba(0, 0, 0, 0.35);
}

.sdx-tag {
  display: inline-flex;
  align-items: center;
  gap: 0.35rem;
  padding: 0.25rem 0.65rem;
  border-radius: 999px;
  border: 1px solid var(--border);
  color: var(--muted);
  font-size: 0.9rem;
  background: rgba(13, 16, 36, 0.55);
}

.sdx-chart-block {
  margin-top: 1.5rem;
  padding: 1.6rem;
  border-radius: 16px;
  background: radial-gradient(circle at 10% 20%, rgba(159, 176, 255, 0.12), transparent 55%),
              radial-gradient(circle at 90% 10%, rgba(255, 196, 106, 0.14), transparent 45%),
              rgba(13, 16, 36, 0.7);
  border: 1px solid var(--border);
  position: relative;
  box-sizing: border-box;
  overflow: hidden;
}

.sdx-placeholder {
  border-style: dashed;
  border-color: rgba(159, 176, 255, 0.45);
}

.sdx-dual-panel {
  display: grid;
  grid-template-columns: minmax(0, 0.7fr) minmax(0, 0.3fr);
  gap: 1.25rem;
  margin-top: 1.2rem;
  align-items: stretch;
}

.sdx-dual-panel .sdx-chart-block {
  margin-top: 0;
}

.sdx-note {
  color: var(--muted);
  font-size: 0.9rem;
  margin-top: 0.8rem;
}

/* Scroll-triggered reveal animations */
[data-animate] {
  opacity: 0;
  transform: translateY(16px);
  transition: opacity 0.7s ease, transform 0.7s ease;
  will-change: opacity, transform;
}

[data-animate="scale"] {
  transform: scale(0.97);
}

[data-animate].animate-in {
  opacity: 1;
  transform: none;
}

@media (max-width: 980px) {
  .sdx-hero-grid,
  .sdx-dual-panel {
    grid-template-columns: 1fr;
  }

  .sdx-case-grid {
    grid-template-columns: 1fr;
  }

  .sdx-hero-media {
    min-height: 300px;
  }
}
</style>

<!-- HERO / INTRO -->
<section class="section sdx-section" id="intro">
  <div class="container">
    <div class="sdx-hero-panel" data-animate="scale">
      <div class="sdx-hero-grid">
        <div data-animate="fade-up">
          <div class="sdx-pill"><span>Event studies &bull; innovation &bull; stock markets</span></div>
          <h1 class="sdx-hero-title">Innovation Footprints in Tech Stock Markets</h1>
          <p class="sdx-hero-body"><em>Can Wall Street smell the future… or only read the headlines afterwards?</em></p>
          <div class="sdx-hero-actions">
            <a class="sdx-btn sdx-btn-primary" href="#prologue">Start the story</a>
            <a class="sdx-btn sdx-btn-ghost" href="#case-files">Jump to chapters</a>
          </div>
        </div>
        <div class="sdx-hero-media" data-animate="fade-up">
          <img
            class="sdx-hero-media-img"
            src="{{ '/assets/img1.png' | relative_url }}"
            alt="Abstract visualization for innovation footprints and markets">
          <div class="sdx-hero-media-overlay">
            <div class="sdx-hero-media-card">
              <h4>Project snapshot</h4>
              <p>Event-study narratives across Apple, NVIDIA, Tesla, AI, and biotech.</p>
              <div class="sdx-hero-meta">
                <span class="sdx-tag">&plusmn;30 trading days</span>
                <span class="sdx-tag">Returns</span>
                <span class="sdx-tag">Volume</span>
                <span class="sdx-tag">Volatility</span>
                <span class="sdx-tag">Spillovers</span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<section class="section sdx-section alt" id="prologue">
  <div class="container">
    <h2 class="title is-3">The Problem with “Obvious” Innovation</h2>
    <div class="sdx-panel" data-animate="fade-up">
      <p>Some innovations feel inevitable <em>in hindsight</em>.</p>
      <p>
        The first iPhone. CUDA. mRNA vaccines. ChatGPT.<br>
        The Model 3. The H100. The Cybertruck. CRISPR therapy.
      </p>
      <p>
        Today, they look like turning points.<br>
        But on the day they happened, they were just… <em>days</em>.
      </p>
      <p>This project asks a deceptively simple question:</p>
      <blockquote>
        <strong>Did the stock market recognize these breakthroughs immediately or only after the world proved they mattered?</strong>
      </blockquote>
      <p>
        To answer this, we treat innovation like an animal crossing fresh snow. If the market recognizes a breakthrough,
        it should leave <strong>footprints</strong>:
      </p>
      <ul class="sdx-list">
        <li>abnormal returns,</li>
        <li>unusual volume,</li>
        <li>pre‑announcement anticipation,</li>
        <li>or slow-burning revaluation afterward.</li>
      </ul>
      <p>
        Our goal isn't to predict the future.<br>
        It’s to measure how markets <em>digest</em> innovation in real time.
      </p>
    </div>
    <div class="sdx-panel" data-animate="fade-up">
      <div class="flourish-embed flourish-timeline" data-src="visualisation/26798005"><script src="https://public.flourish.studio/resources/embed.js"></script><noscript><img src="https://public.flourish.studio/visualisation/26798005/thumbnail" width="100%" alt="timeline visualization" /></noscript></div>
    </div>
  </div>
</section>

<section class="section sdx-section" id="cast">
  <div class="container">
    <h2 class="title is-3">Act I — Meet the Cast</h2>
    <p>Innovation does not come from one world, it comes from many:</p>

    <div class="sdx-case-grid">
      <div class="sdx-case-card" data-animate="fade-up">
        <h3 class="title is-5">1. Consumer Tech (e.g., Apple)</h3>
        <p>
          Products that reshape everyday life:<br>
          the iPhone, iPad, Apple Watch, AirPods, Vision Pro, and the M1 chip.
        </p>
        <p class="sdx-note">These reveal how markets respond to <strong>visible</strong>, widely understood innovations.</p>
      </div>

      <div class="sdx-case-card" data-animate="fade-up">
        <h3 class="title is-5">2. Compute Platforms (e.g., NVIDIA)</h3>
        <p>CUDA, V100, A100, H100, Blackwell — the engines of modern AI.</p>
        <p class="sdx-note">Here the question is: <strong>do markets detect a platform shift before the public does?</strong></p>
      </div>

      <div class="sdx-case-card" data-animate="fade-up">
        <h3 class="title is-5">3. EVs &amp; Robotics (e.g., Tesla)</h3>
        <p>Tesla innovates <em>live</em>: Model 3 lines, cracked Cybertruck windows, Battery Day, the Tesla Bot.</p>
        <p class="sdx-note">These events test whether markets respond to <strong>technology</strong> or <strong>theater</strong>.</p>
      </div>

      <div class="sdx-case-card" data-animate="fade-up">
        <h3 class="title is-5">4. AI Shockwaves (e.g., OpenAI, Google, Meta, Microsoft)</h3>
        <p>ChatGPT, GPT‑4, LLaMA, Copilot, Bard — events that shift entire industries at once.</p>
      </div>

      <div class="sdx-case-card sdx-case-card-wide" data-animate="fade-up">
        <h3 class="title is-5">5. Biotech &amp; Health (e.g., mRNA, GLP‑1, CRISPR)</h3>
        <p>Here innovation is gated by regulation — which creates powerful, binary event days.</p>
      </div>
    </div>

  </div>
</section>

<section class="section sdx-section alt" id="method">
  <div class="container">
    <h2 class="title is-3">Act II — The Detective Method</h2>

    <div class="sdx-dual-panel">
      <div class="sdx-panel" data-animate="fade-up">
        <p>
          We construct an event calendar, align each event to the nearest trading day, and extract a window of
          <strong>±30 days</strong> around each milestone.
        </p>
        <p>We compute:</p>
        <ul class="sdx-list">
          <li><strong>daily returns</strong>,</li>
          <li><strong>abnormal returns</strong> (market‑adjusted),</li>
          <li><strong>cumulative abnormal returns (CAR)</strong>,</li>
          <li><strong>volume z‑scores</strong>,</li>
          <li><strong>pre/post volatility changes</strong>,</li>
          <li>and <strong>spillovers</strong> across related companies.</li>
        </ul>
        <p>Footprints can be:</p>
        <ol class="sdx-list">
          <li><strong>Instant</strong> — a sudden jump.</li>
          <li><strong>Slow-burning</strong> — a delayed realization.</li>
          <li><strong>Mirage</strong> — a spike that fades.</li>
        </ol>
      </div>

      <div class="sdx-chart-block sdx-placeholder" data-animate="fade-up">
        <h3 class="title is-5">PLACEHOLDER: Event Window Diagram</h3>
        <p class="sdx-note">t = 0 at the innovation date</p>
        <p class="sdx-note">Instruction: add an event-window diagram (±30 trading days) here.</p>
      </div>
    </div>

  </div>
</section>

<section class="section sdx-section" id="case-files">
  <div class="container">
    <h2 class="title is-3">Act III — Case Files Across the Innovation Landscape</h2>
    <p>
      Each chapter below treats <strong>every company equally</strong> — Apple = NVIDIA = Tesla = AI = Biotech.<br>
      Same tone, same depth, same structure.
    </p>

    <hr>

    <div class="sdx-panel" id="chapter-apple" data-animate="fade-up">
      <h2 class="title is-4">Chapter 1 — Apple: When Innovation Is Visible to Everyone</h2>
      <div class="sdx-grid-cards">
        <div class="sdx-card">
          <h3 class="title is-5">iPhone Launch (June 29, 2007)</h3>
          <p>The moment that reshaped mobile computing — yet the market did not necessarily understand the scale immediately.</p>
          <p><strong>Expected footprints:</strong></p>
          <ul class="sdx-list">
            <li>muted day‑0 reaction due to execution uncertainty</li>
            <li>strong <em>slow-burn</em> CAR as adoption grows</li>
            <li>volume spikes around early earnings</li>
          </ul>
          <p class="sdx-note">PLACEHOLDER: add AAPL CAR plot (±30 trading days).</p>
        </div>

        <div class="sdx-card">
          <h3 class="title is-5">iPad, Apple Watch, AirPods</h3>
          <p>These were not “shockwaves,” but expansions of Apple's ecosystem.</p>
          <p><strong>Expected footprints:</strong></p>
          <ul class="sdx-list">
            <li>small or neutral event-day reaction</li>
            <li>long-term CAR increasing as ecosystem value compounds</li>
          </ul>
          <p class="sdx-note">PLACEHOLDER: add multi-event overlay for Apple.</p>
        </div>

        <div class="sdx-card">
          <h3 class="title is-5">M1 Chip Announcement (Nov 2020)</h3>
          <p>A platform shift — independence from Intel.</p>
          <p><strong>Expected footprints:</strong></p>
          <ul class="sdx-list">
            <li>moderate abnormal return</li>
            <li>strong post-event CAR reflecting margin optimism</li>
          </ul>
          <p class="sdx-note">PLACEHOLDER: add AAPL CAR plot around M1.</p>
        </div>

        <div class="sdx-card">
          <h3 class="title is-5">Vision Pro Announcement (2023)</h3>
          <p>A frontier technology with uncertain adoption.</p>
          <p><strong>Expected footprints:</strong></p>
          <ul class="sdx-list">
            <li>high volatility</li>
            <li>CAR direction revealed over months</li>
          </ul>
          <p class="sdx-note">PLACEHOLDER: add AAPL CAR plot around Vision Pro.</p>
        </div>
      </div>
    </div>

    <div class="sdx-panel" id="chapter-nvidia" data-animate="fade-up">
      <h2 class="title is-4">Chapter 2 — NVIDIA: Innovation Beneath the Surface</h2>
      <div class="sdx-grid-cards">
        <div class="sdx-card">
          <h3 class="title is-5">CUDA (2007)</h3>
          <p>A foundational shift that consumers never saw — but developers understood.</p>
          <p><strong>Expected footprints:</strong></p>
          <ul class="sdx-list">
            <li>weak immediate reaction</li>
            <li>powerful long-term CAR as AI/ML emerge</li>
          </ul>
          <p class="sdx-note">PLACEHOLDER: add NVDA CAR plot around CUDA.</p>
        </div>

        <div class="sdx-card">
          <h3 class="title is-5">V100, A100, H100, Blackwell</h3>
          <p>These GPUs are the infrastructure of AI.</p>
          <p><strong>Expected footprints:</strong></p>
          <ul class="sdx-list">
            <li>strong day‑0 abnormal returns</li>
            <li>spillovers into AMD, TSMC, MSFT, GOOG</li>
            <li>massive volume z‑scores in the AI boom</li>
          </ul>
          <p class="sdx-note">PLACEHOLDER: add multi-GPU CAR comparison.</p>
        </div>

        <div class="sdx-card">
          <h3 class="title is-5">Arm Acquisition Attempt (2020)</h3>
          <p>More regulatory and strategic than technological.</p>
          <p><strong>Expected footprints:</strong></p>
          <ul class="sdx-list">
            <li>volatility</li>
            <li>ambiguous CAR</li>
            <li>correlation changes with peers</li>
          </ul>
          <p class="sdx-note">PLACEHOLDER: add NVDA event window + correlation/spillover view.</p>
        </div>
      </div>
    </div>

    <div class="sdx-panel" id="chapter-tesla" data-animate="fade-up">
      <h2 class="title is-4">Chapter 3 — Tesla: Innovation Performed Live</h2>
      <div class="sdx-grid-cards">
        <div class="sdx-card">
          <h3 class="title is-5">Model S Deliveries (2012)</h3>
          <p>The birth of credible EV mass adoption.</p>
          <p><strong>Expected footprints:</strong></p>
          <ul class="sdx-list">
            <li>modest immediate reaction</li>
            <li>strong slow-burn CAR</li>
            <li>short-covering volume spikes</li>
          </ul>
          <p class="sdx-note">PLACEHOLDER: add TSLA price + volume window (±30 days).</p>
        </div>

        <div class="sdx-card">
          <h3 class="title is-5">Autopilot Announcement (2014)</h3>
          <p>A shift toward autonomy.</p>
          <p><strong>Expected footprints:</strong></p>
          <ul class="sdx-list">
            <li>revaluation of Tesla as tech + auto</li>
            <li>spillovers to sensor and chip suppliers</li>
          </ul>
          <p class="sdx-note">PLACEHOLDER: add TSLA CAR + supplier spillover view.</p>
        </div>

        <div class="sdx-card">
          <h3 class="title is-5">Model 3 Reveal (2016)</h3>
          <p>Mass-market shockwave.</p>
          <p><strong>Expected footprints:</strong></p>
          <ul class="sdx-list">
            <li>anticipation drift</li>
            <li>high volume</li>
            <li>CAR shaped by production belief</li>
          </ul>
          <p class="sdx-note">PLACEHOLDER: add TSLA CAR around Model 3 reveal.</p>
        </div>

        <div class="sdx-card">
          <h3 class="title is-5">Cybertruck Reveal &amp; Delivery (2019–2023)</h3>
          <p>Spectacle meets fundamentals.</p>
          <p><strong>Expected footprints:</strong></p>
          <ul class="sdx-list">
            <li>reveal: volatility + sentiment whiplash</li>
            <li>delivery: margin-driven CAR</li>
          </ul>
          <p class="sdx-note">PLACEHOLDER: add separate event windows for reveal vs delivery.</p>
        </div>

        <div class="sdx-card">
          <h3 class="title is-5">Battery Day (2020)</h3>
          <p>Tesla’s version of a compute roadmap.</p>
          <p><strong>Expected footprints:</strong></p>
          <ul class="sdx-list">
            <li>muted immediate reaction</li>
            <li>CAR depending on credibility</li>
          </ul>
          <p class="sdx-note">PLACEHOLDER: add TSLA CAR around Battery Day.</p>
        </div>

        <div class="sdx-card">
          <h3 class="title is-5">Tesla Bot (2021)</h3>
          <p>High speculation, low clarity.</p>
          <p><strong>Expected footprints:</strong></p>
          <ul class="sdx-list">
            <li>volatility</li>
            <li>sentiment-driven return, not fundamentals</li>
          </ul>
          <p class="sdx-note">PLACEHOLDER: add TSLA CAR and sentiment proxy notes.</p>
        </div>
      </div>
    </div>

    <div class="sdx-panel" id="chapter-ai" data-animate="fade-up">
      <h2 class="title is-4">Chapter 4 — AI Shockwaves</h2>
      <div class="sdx-grid-cards">
        <div class="sdx-card">
          <h3 class="title is-5">ChatGPT Launch (Nov 2022)</h3>
          <p>A cultural and technological explosion.</p>
          <p><strong>Expected footprints:</strong></p>
          <ul class="sdx-list">
            <li>strong cross-market spillovers</li>
            <li>high volume across AI tickers</li>
            <li>rising CAR for compute providers</li>
          </ul>
          <p class="sdx-note">PLACEHOLDER: add heatmap of abnormal returns for the AI ecosystem.</p>
        </div>

        <div class="sdx-card">
          <h3 class="title is-5">GPT‑4, Copilot, Bard, LLaMA</h3>
          <p>Capability announcements that shift expectations.</p>
          <p><strong>Expected footprints:</strong></p>
          <ul class="sdx-list">
            <li>infrastructure winners (NVDA, AMD, TSMC)</li>
            <li>mixed reactions for content platforms</li>
          </ul>
          <p class="sdx-note">PLACEHOLDER: add multi-event overlay + spillover comparison.</p>
        </div>
      </div>
    </div>

    <div class="sdx-panel" id="chapter-biotech" data-animate="fade-up">
      <h2 class="title is-4">Chapter 5 — Biotech &amp; Health: Innovation With a Regulatory Gate</h2>
      <div class="sdx-grid-cards">
        <div class="sdx-card">
          <h3 class="title is-5">mRNA Vaccine Approval (2020)</h3>
          <p>A historic biomedical milestone.</p>
          <p><strong>Expected footprints:</strong></p>
          <ul class="sdx-list">
            <li>large positive abnormal return</li>
            <li>extreme volume z‑scores</li>
            <li>spillovers across biotech index</li>
          </ul>
          <p class="sdx-note">PLACEHOLDER: add approval-day CAR and volume z-score plots.</p>
        </div>

        <div class="sdx-card">
          <h3 class="title is-5">GLP‑1 (Wegovy, Mounjaro, Zepbound)</h3>
          <p>A metabolic revolution.</p>
          <p><strong>Expected footprints:</strong></p>
          <ul class="sdx-list">
            <li>strong CAR for Eli Lilly, Novo Nordisk</li>
            <li>negative reactions for food &amp; health-adjacent sectors</li>
          </ul>
          <p class="sdx-note">PLACEHOLDER: add sector rotation / spillover plot.</p>
        </div>

        <div class="sdx-card">
          <h3 class="title is-5">CRISPR Therapy Approval (2023)</h3>
          <p>Gene-editing becomes real.</p>
          <p><strong>Expected footprints:</strong></p>
          <ul class="sdx-list">
            <li>sharp, concentrated jumps</li>
            <li>volatile multi-week CAR</li>
          </ul>
          <p class="sdx-note">PLACEHOLDER: add CAR window around approval date.</p>
        </div>
      </div>

      <div class="sdx-chart-block sdx-placeholder" data-animate="fade-up">
        <h3 class="title is-5">PLACEHOLDER: Sector-wide biotech CAR plot</h3>
        <p class="sdx-note">Instruction: compare biotech/index reaction vs specific names around approvals.</p>
      </div>
    </div>

  </div>
</section>

<section class="section sdx-section alt" id="archetypes">
  <div class="container">
    <h2 class="title is-3">Act IV — Archetypes of Market Recognition</h2>
    <p>Across all events, three patterns dominate:</p>

    <div class="sdx-grid-cards">
      <div class="sdx-card" data-animate="fade-up">
        <h3 class="title is-5">1. The Instant Footprint</h3>
        <p>AI launches, biotech approvals, major GPU announcements.</p>
      </div>
      <div class="sdx-card" data-animate="fade-up">
        <h3 class="title is-5">2. The Slow Burn</h3>
        <p>iPhone, CUDA, Model S, M1 chip.</p>
      </div>
      <div class="sdx-card" data-animate="fade-up">
        <h3 class="title is-5">3. The Mirage</h3>
        <p>Cybertruck reveal, Tesla Bot, early AI competitors.</p>
      </div>
    </div>

    <div class="sdx-chart-block sdx-placeholder" data-animate="fade-up">
      <h3 class="title is-5">PLACEHOLDER: Three example CAR plots</h3>
      <p class="sdx-note">Instruction: insert one example for each archetype (Instant / Slow burn / Mirage).</p>
    </div>

  </div>
</section>

<section class="section sdx-section" id="what-prices">
  <div class="container">
    <h2 class="title is-3">Act V — What the Market Really Prices</h2>

    <div class="sdx-panel" data-animate="fade-up">
      <p>Innovation is not priced the same way across domains:</p>
      <ul class="sdx-list">
        <li><strong>Compute</strong> is priced early.</li>
        <li><strong>Consumer tech</strong> is priced gradually.</li>
        <li><strong>Biotech</strong> is priced at the regulatory moment.</li>
        <li><strong>AI events</strong> move entire ecosystems.</li>
        <li><strong>Tesla</strong> prices <em>the crowd</em> as much as the technology.</li>
      </ul>
      <blockquote>
        <strong>Some futures are priced in hours. Others take quarters.<br>And some are never priced at the moment you’d expect.</strong>
      </blockquote>
    </div>

  </div>
</section>

<script>
document.addEventListener("DOMContentLoaded", function () {
  const animated = document.querySelectorAll("[data-animate]");
  if ("IntersectionObserver" in window) {
    const obs = new IntersectionObserver(
      (entries) => {
        entries.forEach((entry) => {
          if (entry.isIntersecting) {
            entry.target.classList.add("animate-in");
            obs.unobserve(entry.target);
          }
        });
      },
      { threshold: 0.15, rootMargin: "0px 0px -10% 0px" }
    );
    animated.forEach((el) => obs.observe(el));
  } else {
    animated.forEach((el) => el.classList.add("animate-in"));
  }
});
</script>
