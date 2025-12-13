---
layout: page
title: "SwissDataExplorers"
subtitle: "Innovation Footprints in Tech Stock Markets"
---

<!-- Custom fonts and styling to modernize the page without removing content -->
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;600;700&family=Source+Sans+3:wght@400;600;700&display=swap" rel="stylesheet">
<script>
  // MathJax renders the inline LaTeX formulas used in the recipe cards.
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
  --card: rgba(255, 255, 255, 0.04);
  --border: rgba(255, 255, 255, 0.08);
  --accent: #5df0ff;
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

strong {
  color: #8cdcff;
}


@keyframes floatPulse {
  0% { transform: translateY(0); }
  50% { transform: translateY(-8px); }
  100% { transform: translateY(0); }
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
  border-bottom: 1px solid rgba(255, 255, 255, 0.08);
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
  background: linear-gradient(120deg, #5df0ff, #7ef7ff);
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
  color: var(--accent) !important;
}

.navbar .navbar-item.is-active::after,
.navbar .navbar-link.is-active::after {
  opacity: 1;
  transform: translateY(0);
}

.hero.is-primary {
  background:
    linear-gradient(140deg, #030c20 0%, #051838 55%, #020812 100%),
    radial-gradient(circle at 15% 10%, rgba(93, 240, 255, 0.15), transparent 55%),
    radial-gradient(circle at 82% -5%, rgba(255, 196, 106, 0.12), transparent 50%);
  border: none;
  position: relative;
  overflow: hidden;
  padding: 4rem 0 4.5rem;
  min-height: 360px;
  box-shadow: inset 0 -35px 60px rgba(0, 0, 0, 0.45);
}

.hero.is-primary::before,
.hero.is-primary::after {
  content: "";
  position: absolute;
  inset: 0;
  pointer-events: none;
}

.hero.is-primary::before {
  background: radial-gradient(circle at 50% -20%, rgba(93, 240, 255, 0.2), transparent 60%);
}

.hero.is-primary::after {
  background:
    radial-gradient(circle at 85% 20%, rgba(255, 196, 106, 0.1), transparent 60%);
  opacity: 0.85;
  mix-blend-mode: screen;
}

.hero.is-primary .hero-body {
  padding: 0 1.5rem;
  display: flex;
  justify-content: center;
  position: relative;
}

.hero-chart-bg {
  position: absolute;
  top: 1.25rem;
  left: 0;
  right: 0;
  width: 100%;
  height: 260px;
  opacity: 0.7;
  z-index: 0;
  pointer-events: none;
}

.hero.is-primary .hero-body > *:not(.hero-chart-bg) {
  position: relative;
  z-index: 1;
}

@media (max-width: 768px) {
  .hero-chart-bg {
    top: 1rem;
    height: 200px;
  }
}

.hero.is-primary .container {
  width: 100%;
  max-width: 1100px;
  padding: 3rem 3rem 3.25rem;
  border-radius: 32px;
  background:
    linear-gradient(130deg, rgba(12, 29, 60, 0.96), rgba(6, 23, 46, 0.9)),
    radial-gradient(circle at 80% 20%, rgba(93, 240, 255, 0.25), transparent 60%);
  border: 1px solid rgba(255, 255, 255, 0.08);
  box-shadow: 0 40px 100px rgba(0, 0, 0, 0.6);
  position: relative;
  overflow: hidden;
}

.hero.is-primary .container::after {
  content: "";
  position: absolute;
  width: 240px;
  height: 240px;
  background: radial-gradient(circle, rgba(93, 240, 255, 0.3), transparent 65%);
  top: -70px;
  right: -80px;
  filter: blur(3px);
}

.hero.is-primary .container::before {
  content: "";
  position: absolute;
  width: 200px;
  height: 200px;
  background: radial-gradient(circle, rgba(255, 196, 106, 0.25), transparent 65%);
  bottom: -90px;
  left: -70px;
}

.hero.is-primary .container > * {
  position: relative;
  z-index: 1;
}

.hero.is-primary .title,
.hero.is-primary .subtitle {
  font-family: "Space Grotesk", "Source Sans 3", sans-serif;
  letter-spacing: -0.02em;
  text-align: left;
}

.hero.is-primary .title {
  color: #f7f9ff;
  font-size: clamp(2.2rem, 4vw, 3.3rem);
  margin: 0;
  text-shadow: 0 15px 45px rgba(0, 0, 0, 0.45);
}

.hero.is-primary .subtitle {
  color: rgba(222, 232, 255, 0.92);
  font-size: clamp(1.1rem, 2vw, 1.35rem);
  margin-top: 0.85rem;
  margin-bottom: 0;
  max-width: 620px;
}

.hero-pill {
  display: inline-flex;
  align-items: center;
  gap: 0.4rem;
  padding: 0.35rem 0.85rem;
  border-radius: 999px;
  font-size: 0.9rem;
  font-weight: 600;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  border: 1px solid rgba(255, 255, 255, 0.18);
  color: rgba(222, 232, 255, 0.85);
  background: rgba(13, 16, 36, 0.55);
  margin-bottom: 0.8rem;
}

.hero-head-actions {
  display: flex;
  gap: 0.85rem;
  margin-top: 1.8rem;
  flex-wrap: wrap;
}

.hero-head-actions .sdx-btn {
  padding: 0.95rem 1.4rem;
}

body > section.hero.is-primary {
  display: none !important;
}

hr {
  border: none;
  border-top: 1px solid var(--border);
  margin: 2.5rem 0;
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
  opacity: 0.3;
}

.sdx-hero-panel::before {
  background: #5df0ff;
  top: -80px;
  right: -80px;
  animation: slowDrift 18s ease-in-out infinite;
}

.sdx-hero-panel::after {
  background: #ffc46a;
  bottom: -80px;
  left: -80px;
  animation: slowDrift 22s ease-in-out infinite reverse;
}

.sdx-hero-grid {
  display: grid;
  gap: 1.8rem;
  grid-template-columns: 1.1fr 0.9fr;
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

.sdx-hero-title {
  font-family: "Space Grotesk", "Source Sans 3", sans-serif;
  font-weight: 700;
  letter-spacing: -0.02em;
  font-size: 2.25rem;
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
  background: linear-gradient(120deg, #5df0ff, #6ae4c8);
  color: #041022;
  box-shadow: 0 12px 30px rgba(93, 240, 255, 0.2);
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

.sdx-section {
  padding: 3rem 0 2.5rem;
}

.sdx-section h2 {
  font-family: "Space Grotesk", "Source Sans 3", sans-serif;
  color: #f7f9ff;
  margin-bottom: 1.2rem;
  letter-spacing: -0.02em;
}

.sdx-section p {
  color: var(--text);
}

.sdx-grid-cards {
  display: grid;
  gap: 1rem;
  grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
}

.sdx-card,
.sdx-panel {
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

.sdx-panel .title.is-5,
.sdx-panel .title.is-6 {
  color: var(--accent);
}

.sdx-formula-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
  gap: 1rem;
  margin-top: 1rem;
}

.sdx-formula-card {
  border: 1px solid rgba(255, 255, 255, 0.12);
  border-radius: 16px;
  padding: 1rem 1.1rem;
  background: linear-gradient(140deg, rgba(93, 240, 255, 0.08), rgba(13, 16, 36, 0.72));
  box-shadow: 0 25px 45px rgba(0, 0, 0, 0.35);
  position: relative;
  overflow: hidden;
}

.sdx-formula-card::after {
  content: "";
  position: absolute;
  width: 80px;
  height: 80px;
  top: -30px;
  right: -30px;
  border-radius: 50%;
  background: rgba(93, 240, 255, 0.18);
  filter: blur(20px);
}

.sdx-formula-card h4 {
  margin: 0;
  font-size: 0.95rem;
  text-transform: uppercase;
  letter-spacing: 0.1em;
  color: var(--accent-2);
}

.sdx-formula-card .formula {
  font-family: "Space Grotesk", "Source Sans 3", sans-serif;
  font-size: 1rem;
  margin: 0.45rem 0;
  color: #f7f9ff;
}

.sdx-formula-card p {
  margin: 0;
  font-size: 0.85rem;
  color: var(--muted);
}

.sdx-story-body {
  position: relative;
  line-height: 1.7;
}

.sdx-story-body::after {
  content: "";
  display: block;
  clear: both;
}

.sdx-panel-summary {
  float: right;
  width: min(340px, 40%);
  margin: 0 0 1.5rem 1.5rem;
}

@media (max-width: 980px) {
  .sdx-panel-summary {
    float: none;
    width: 100%;
    margin: 1.5rem 0 0;
  }
}

.sdx-card h3 {
  color: #f7f9ff;
  font-weight: 700;
  margin-bottom: 0.25rem;
}

.sdx-card:hover,
.sdx-panel:hover {
  transform: translateY(-4px);
  border-color: rgba(93, 240, 255, 0.4);
  box-shadow: 0 22px 50px rgba(0, 0, 0, 0.35);
}

.sdx-card .meta {
  color: var(--muted);
  font-size: 0.9rem;
}

.sdx-list {
  padding-left: 1.1rem;
  margin: 0.6rem 0;
}

.sdx-list li {
  padding: 0.12rem 0;
}

.sdx-feature-list {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
  gap: 1rem;
}

.sdx-feature-item {
  border-radius: 16px;
  padding: 1.25rem;
  background: rgba(13, 16, 36, 0.6);
  border: 1px solid var(--border);
}

.sdx-feature-item .heading {
  color: var(--muted);
  letter-spacing: 0.01em;
}

.sdx-stats-row {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
  gap: 1rem;
}

.sdx-stat-card {
  border-radius: 14px;
  padding: 1.4rem 1.5rem;
  background: linear-gradient(180deg, rgba(93, 240, 255, 0.06), rgba(13, 16, 36, 0.62));
  border: 1px solid var(--border);
  text-align: left;
  transition: transform 0.3s ease, border-color 0.3s ease;
}

.sdx-stat-card .label {
  color: var(--muted);
  font-size: 0.95rem;
}

.sdx-stat-card .value {
  font-size: 2rem;
  font-family: "Space Grotesk", "Source Sans 3", sans-serif;
  color: #f7f9ff;
}

.sdx-stat-card:hover {
  transform: translateY(-4px);
  border-color: rgba(93, 240, 255, 0.4);
}

.sdx-section.alt {
  background: rgba(13, 16, 36, 0.55);
  border: 1px solid var(--border);
  border-radius: 18px;
  padding: 2.8rem;
}

.sdx-case-grid {
  display: grid;
  gap: 1rem;
  grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
}

.sdx-case-card {
  border-radius: 16px;
  padding: 1.3rem 1.4rem;
  background: linear-gradient(150deg, rgba(93, 240, 255, 0.05), rgba(255, 196, 106, 0.08));
  border: 1px solid var(--border);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.sdx-case-card h3 {
  margin-bottom: 0.35rem;
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
  background: radial-gradient(circle at 10% 20%, rgba(93, 240, 255, 0.08), transparent 55%),
              radial-gradient(circle at 90% 10%, rgba(255, 196, 106, 0.12), transparent 45%),
              rgba(13, 16, 36, 0.7);
  border: 1px solid var(--border);
  position: relative;
  box-sizing: border-box;
  overflow: hidden;
}

.sdx-chart-block .flourish-embed {
  width: 100% !important;
  max-width: 100% !important;
  border-radius: 12px;
  position: relative;
  display: block;
}

.sdx-chart-block .flourish-embed iframe {
  width: 100% !important;
  max-width: 100% !important;
  display: block;
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

.sdx-chart-note {
  background: rgba(13, 16, 36, 0.72);
  border: 1px solid var(--border);
  border-radius: 16px;
  padding: 1.6rem 1.4rem;
  box-shadow: 0 15px 35px rgba(0, 0, 0, 0.3);
}

.sdx-chart-note h4 {
  margin-top: 0;
  font-size: 1rem;
  color: #f7f9ff;
}

.sdx-chart-note p {
  margin-top: 0.5rem;
  color: var(--text);
}

.sdx-chart-note ul {
  margin: 0.6rem 0 0;
  padding-left: 1.1rem;
  color: var(--muted);
  font-size: 0.95rem;
}

.sdx-chart-note ul li {
  margin-bottom: 0.35rem;
}

.sdx-toggle-group {
  display: inline-flex;
  gap: 0.65rem;
  flex-wrap: wrap;
}

.sdx-toggle {
  border-radius: 999px;
  padding: 0.55rem 1.1rem;
  border: 1px solid var(--border);
  background: rgba(13, 16, 36, 0.6);
  color: var(--text);
  font-weight: 700;
  letter-spacing: -0.01em;
  transition: transform 0.2s ease, box-shadow 0.2s ease, border-color 0.2s ease;
}

.sdx-toggle:hover {
  transform: translateY(-2px);
  border-color: rgba(93, 240, 255, 0.4);
  box-shadow: 0 8px 20px rgba(93, 240, 255, 0.2);
}
.sdx-note {
  color: var(--muted);
  font-size: 0.9rem;
  margin-top: 0.8rem;
}

.sdx-team {
  display: grid;
  grid-template-columns: 1.1fr 0.9fr;
  gap: 1.25rem;
}

.sdx-cta-panel {
  margin-top: 2rem;
  padding: 1.5rem;
  border-radius: 16px;
  border: 1px solid var(--border);
  background: linear-gradient(120deg, rgba(93, 240, 255, 0.08), rgba(13, 16, 36, 0.62));
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 1rem;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.sdx-cta-panel .title {
  margin: 0;
}

.sdx-cta-actions {
  display: flex;
  gap: 0.75rem;
}

.sdx-cta-panel:hover {
  transform: translateY(-4px);
  box-shadow: 0 24px 60px rgba(0, 0, 0, 0.35);
}
a {
  color: var(--accent);
}

a:hover {
  color: #7ef7ff;
}

.sdx-highlight {
  cols */
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
  .sdx-team {
    grid-template-columns: 1fr;
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
          <h2 class="sdx-hero-title">Do markets price breakthroughs on impact?</h2>
          <p class="sdx-hero-body">
            Innovation shows up as dates you can point to: CUDA and the iPhone, Apple’s M1 transition,
            and the GenAI shockwave of ChatGPT and GPT-4.
            We align those moments with market data and ask one question:
            <strong>does price move before the headline, on day 0, or only after the world catches up?</strong>
            Biotech approvals are on the roadmap and come last.
          </p>
          <div class="sdx-hero-actions">
            <a class="sdx-btn sdx-btn-primary" href="#cases">Jump to event types</a>
            <a class="sdx-btn sdx-btn-ghost" href="#pipeline">See the methodology</a>
          </div>
        </div>
        <div class="sdx-hero-badge" data-animate="fade-up">
          <h4>Innovation Footprints in Tech Stock Markets</h4>
          <p class="sdx-hero-body">
            We turn innovation headlines into a consistent event-study workflow (returns, volume, volatility, later: abnormal returns).
            This site is a living draft: some sections are complete, others are explicit “add plot here” placeholders.
          </p>
          <div class="sdx-hero-stats">
            <div class="sdx-mini-stat">
              <div class="label">Event types</div>
              <div class="value">GPUs &bull; GenAI &bull; Apple &bull; Biotech</div>
            </div>
            <div class="sdx-mini-stat">
              <div class="label">Signals</div>
              <div class="value">Returns &bull; Volume &bull; Volatility</div>
            </div>
            <div class="sdx-mini-stat">
              <div class="label">Window</div>
              <div class="value">&plusmn;30&nbsp;days</div>
            </div>
            <div class="sdx-mini-stat">
              <div class="label">Status</div>
              <div class="value">In progress</div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- LONG-FORM INTRO /<!-- LONG-FORM INTRO / STORY -->
<section class="section sdx-section alt" id="story">
  <div class="container">
    <div class="sdx-story-body">
      <div class="sdx-panel sdx-panel-summary" data-animate="fade-up">
        <h3 class="title is-5">In one paragraph</h3>
        <p>
          We treat landmark innovations as "exam questions" for financial markets. For each event, we anchor a
          fixed window of trading days around the announcement and measure returns, volume, volatility, and
          (later) abnormal returns relative to a benchmark. The story is organized by four event families:
          GPUs, GenAI milestones, Apple product/silicon pivots, and (last) biotech approvals.
        </p>
        <hr>
        <h4 class="title is-6">What we test</h4>
        <ul class="sdx-list">
          <li>Do markets <strong>anticipate</strong> big innovations?</li>
          <li>Do they <strong>jump</strong> on the announcement day?</li>
          <li>Do they <strong>under-react</strong> and drift afterwards?</li>
          <li>Do reactions spill over to the broader <strong>ecosystem</strong>?</li>
        </ul>
        <p class="sdx-note">
          Status: work in progress — sections include explicit “add plot here” placeholders while the analysis is still being built.
        </p>
      </div>

      <!-- Main narrative -->
        <h2 class="title is-3">Can the market see the future?</h2>
        <p>
          Every finance textbook repeats the same mantra: markets are
          <em>forward-looking</em>. Prices today, we are told, already reflect
          everything that matters tomorrow. In that story, tech investors react the
          instant a breakthrough is announced, and by the time the rest of us
          understand what CUDA or the iPhone really mean, the opportunity is
          already gone.
        </p>
        <p>
          But if you scroll back through the last twenty years of technology,
          that neat narrative starts to crack.
        </p>
        <p>
          In June 2007, NVIDIA quietly launched <strong>CUDA</strong>, a software
          layer that turned GPUs from glorified graphics cards into programmable
          computing engines. A few days later, the first <strong>iPhone</strong>
          went on sale, an odd-looking phone without buttons. In 2008, Apple
          flipped the switch on the <strong>App Store</strong>, inventing the
          app economy. In 2014, it launched <strong>Apple Pay</strong> and decided
          that your phone should also be your wallet. Years later, NVIDIA’s
          <strong>Tesla V100</strong> and <strong>RTX 2080 Ti</strong> GPUs would
          fuel the deep learning boom and real-time ray tracing; H100 and Blackwell
          would make “AI chips” a household phrase.
        </p>
        <p>
          Looking back, it’s obvious that these were turning points. The question
          we ask in this project is brutally simple:
        </p>
        <p>
          <strong>
            When those breakthroughs happened, did the market see them coming,
            recognize them on impact, or mostly realize their importance in hindsight?
          </strong>
        </p>

        <h3 class="title is-4" style="margin-top:2rem;">The myth of instant recognition</h3>
        <p>
          Imagine the stock market as a huge, noisy crowd of traders, algorithms
          and index funds, all staring at the same stream of news. An innovation
          headline drops:
        </p>
        <p>
          “CUDA released for general programming on NVIDIA GPUs.”<br>
          “Apple announces App Store.”<br>
          “NVIDIA introduces Tesla V100 with Tensor Cores.”<br>
          “Apple Pay goes live in the US.”
        </p>
        <p>
          If markets are truly as efficient as we like to believe, the crowd
          should not consistently “miss” these moments. Prices should already
          whisper that something is coming (subtle drift and volume before the
          announcement), or they should jump decisively when the news hits
          (clean abnormal returns on day 0). A decade later, when everyone agrees
          that these events were historic, the charts should show that the market
          behaved like it.
        </p>
        <p>
          But that’s not obvious from casual eyeballing. Sometimes stocks rally
          hard before an event and then barely move on the announcement. Sometimes
          they do nothing when the news drops and only start drifting upward
          quietly afterwards. Sometimes an entire ecosystem of suppliers and
          competitors reacts more aggressively than the company that made the
          announcement.
        </p>
        <p>
          Our goal is to stop arguing in anecdotes and turn this into a systematic test.
        </p>

        <h3 class="title is-4" style="margin-top:2rem;">
          Turning innovations into exam questions for the market
        </h3>
        <p>
          We treat each major breakthrough as a <strong>question on an exam</strong>
          that the stock market has to answer in real time.
        </p>
        <p>
          For each event, we write down a precise question:
        </p>
        <ul class="sdx-list">
          <li>
            On and around this date, did the stock of the announcing company earn
            <strong>abnormal returns</strong> relative to a broad market benchmark?
          </li>
          <li>
            Did trading <strong>volume spike</strong> compared to its usual range,
            signalling unusual attention or information flow?
          </li>
          <li>
            Was there a <strong>drift before the announcement</strong> that suggests
            anticipation or leakage?
          </li>
          <li>
            Did <strong>related firms</strong> (suppliers, competitors, partners)
            move in the same direction, indicating that the market understood the
            broader implications?
          </li>
        </ul>
        <p>
          To build the exam, we start with a carefully curated calendar of
          innovation events: CUDA’s first release, major AI GPU launches like
          Tesla V100 and RTX 2080 Ti, the H100 and Blackwell announcements,
          the first iPhone, the App Store launch, Apple Pay, and other
          well-documented milestones in tech and biotech. For each of them,
          we align the exact announcement timing to US trading days (after-close
          news is anchored to the next day’s open) so we are grading the market
          on the days when it actually had a chance to react.
        </p>
        <p>
          On the data side, we work with decades of daily stock information
          (open, high, low, close and volume) for US-listed technology and biotech
          companies. We extend this history to the present using publicly available
          historical price feeds and enforce a consistent OHLCV structure across
          all tickers. Before we look at any event window, we run a battery of
          cleaning checks: filtering obvious outliers, adjusting for stock splits
          and corporate actions, aligning calendars, and handling missing observations
          in a controlled way. When a spike shows up in a chart, we want to be as
          confident as possible that it reflects a genuine market reaction, not a
          formatting issue or bad tick.
        </p>
        <p>
          Then, for each stock and event, we build a simple market model that
          predicts what the stock would have done if nothing special had happened.
          The difference between reality and this baseline is our
          <strong>abnormal return</strong>. Aggregating those differences over a
          window around the announcement gives us <strong>cumulative abnormal
          returns (CAR)</strong> and a clean way to say: “the market behaved
          unusually around this innovation” or “the event disappeared into the noise”.
        </p>

        <h3 class="title is-4" style="margin-top:2rem;">What you’ll see on this page</h3>
        <p>
          This website is the story of what happens when you replay landmark
          innovations through the lens of an event study.
        </p>
        <p>
          First, we walk through a few iconic case studies where everyone already
          knows the ending (NVIDIA in the AI era, the iPhone and the App Store
          for Apple) and show how the price and volume behaved around those dates.
          These are our front-row seats: if the market ever had a chance to show
          off its clairvoyance, it was here.
        </p>
        <p>
          Then we zoom out. Using the same machinery, we compare reactions across:
        </p>
        <ul class="sdx-list">
          <li><strong>Types of innovation</strong> – devices vs platforms vs AI chips vs fintech layers,</li>
          <li><strong>Company size</strong> – mega-caps versus smaller, more speculative firms,</li>
          <li><strong>Time periods</strong> – early smartphone era vs cloud era vs the recent AI wave,</li>
          <li><strong>Ecosystems</strong> – whether suppliers, competitors and partners move with or against the innovator.</li>
        </ul>
        <p>
          Along the way, we will show you plots of cumulative returns, volatility and
          volume that behave like tiny cardiograms around each announcement: sometimes
          flat, sometimes erratic, sometimes spiking exactly when the textbook says
          they should.
        </p>
        <p>
          Our aim is not to produce a secret trading strategy. It is to answer a more
          fundamental question: when we look at the tape around real innovations that
          changed how we compute, pay and build AI, does the stock market look like
          a sharp, forward-looking judge of technology or more like a distracted
          student who only realizes what was on the exam after the results come out?
        </p>
      </div>

  </div>
</section>
<section class="section sdx-section" id="why">
  <div class="container">
    <h2 class="title is-3">Why this matters</h2>
    <div class="sdx-grid-cards">
      <div class="sdx-card" data-animate="fade-up">
        <h3>Innovation is the story, prices are the verdict</h3>
        <p>
          Tech history is written through breakthrough launches: CUDA turning GPUs into
          compute engines, the App Store creating the app economy, Apple Pay making
          phones into wallets. But stock prices are noisy. We want to know whether the
          market actually <em>recognizes</em> those moments as they happen.
        </p>
      </div>
      <div class="sdx-card" data-animate="fade-up">
        <h3>Our angle</h3>
        <p>
          We run a classic event study on a modern set of tech innovations.
          Around each announcement we track cumulative returns, volatility and volume,
          compare them to a market model, and ask whether innovation leaves a clear,
          repeatable footprint in the data.
        </p>
      </div>
      <div class="sdx-card" data-animate="fade-up">
        <h3>Questions we ask</h3>
        <ul class="sdx-list">
          <li>Do breakthrough announcements trigger immediate excess returns and volume spikes?</li>
          <li>Is there systematic <strong>pre-announcement drift</strong>, hinting at anticipation or leakage?</li>
          <li>Do reactions spill over to suppliers, competitors or partners?</li>
          <li>Does the pattern depend on the type of innovation or the time period?</li>
        </ul>
      </div>
    </div>
  </div>
</section>

<!-- KEY NUMBERS -->
<section class="section sdx-section" id="numbers">
  <div class="container">
    <h2 class="title is-3">The scope at a glance</h2>
    <p class="sdx-note">We separate what is implemented (pilot) from what is targeted (roadmap).</p>

    <h3 class="title is-5" style="margin-top:1.2rem;">Current pilot (implemented)</h3>
    <div class="sdx-stats-row">
      <div class="sdx-stat-card" data-animate="fade-up">
        <div class="label">Tickers</div>
        <div class="value">1 (pilot)</div>
      </div>
      <div class="sdx-stat-card" data-animate="fade-up">
        <div class="label">Innovation events</div>
        <div class="value">8</div>
      </div>
      <div class="sdx-stat-card" data-animate="fade-up">
        <div class="label">Window length</div>
        <div class="value">61 days</div>
      </div>
      <div class="sdx-stat-card" data-animate="fade-up">
        <div class="label">Outputs</div>
        <div class="value">Plots + exports</div>
      </div>
    </div>

    <h3 class="title is-5" style="margin-top:1.4rem;">Target scope (in progress)</h3>
    <div class="sdx-stats-row">
      <div class="sdx-stat-card" data-animate="fade-up">
        <div class="label">Horizon (target)</div>
        <div class="value">1965-2025</div>
      </div>
      <div class="sdx-stat-card" data-animate="fade-up">
        <div class="label">Tickers (target)</div>
        <div class="value">100+</div>
      </div>
      <div class="sdx-stat-card" data-animate="fade-up">
        <div class="label">Event families</div>
        <div class="value">GPUs &bull; GenAI &bull; Apple &bull; Biotech</div>
      </div>
      <div class="sdx-stat-card" data-animate="fade-up">
        <div class="label">Curated events (target)</div>
        <div class="value">50+</div>
      </div>
    </div>
  </div>
</section>

<!-- STORY OVERVIEW -->
<section class="section sdx-section alt" id="overview">
  <div class="container">
    <h2 class="title is-3">From headline to price chart</h2>
    <p>
      For each major innovation, we build an <strong>event calendar</strong> with precise
      dates (and timing: pre-open, intraday, after-close). Around each event we create a
      symmetric window of trading days and (where appropriate) compare what actually happened to what a
      simple market model would have predicted.
    </p>
    <p style="margin-top:0.8rem;">
      Concretely, we ask whether markets:
    </p>
    <ul class="sdx-list">
      <li><strong>React instantly</strong> on day 0 or +1 (announcement-day jump),</li>
      <li><strong>Anticipate</strong> the news with a run-up and volume spikes before day 0,</li>
      <li><strong>Under-react</strong> and keep drifting in the same direction over the next days.</li>
    </ul>
    <p>
      This is the classic event-study playbook applied to CUDA, the iPhone, the App Store,
      Apple Pay, AI GPUs, GenAI milestones, and biotech platform breakthroughs.
    </p>
  </div>
</section>

<!-- PIPELINE / METHOD -->
<section class="section sdx-section" id="pipeline">
  <div class="container">
    <h2 class="title is-3">The recipe behind every chart</h2>
    <p>
      No flowcharts here, just a simple ritual repeated for every innovation. We line up the event date with
      clean OHLCV history, cut a window of trading days around it, and ask “what actually happened versus what
      the market model predicted?” The ingredients below are the entire toolkit: once you see them, every plot
      on this page becomes a remix of the same math.
    </p>
    <p>
      Think of them as a mise en place. Returns tell us the daily heartbeat, log returns keep compounding honest,
      cumulative returns reveal the story arc, volatility flags when the crowd panics, and volume pulses show
      whether attention really piled in. Mix, compare pre vs. post, and you get the innovation footprint.
      If you have never coded an event study, the cards below spell out exactly how to read each number.
    </p>
    <div class="sdx-formula-grid" style="margin-top:1.4rem;">
      <div class="sdx-formula-card">
        <h4>Return</h4>
        <div class="formula">\( R_t = \left(\frac{P_t}{P_{t-1}} - 1\right) \times 100 \)</div>
        <p>Divide today’s price by yesterday’s, subtract one, and turn it into a percentage. Positive means the stock gained that day; negative means it slipped.</p>
      </div>
      <div class="sdx-formula-card">
        <h4>Log return</h4>
        <div class="formula">\( r_t = \ln\!\left(\frac{P_t}{P_{t-1}}\right) \times 100 \)</div>
        <p>The natural log ratio of today’s price to yesterday’s. It stacks nicely across many days, so it is perfect when we want to add returns over long stretches.</p>
      </div>
      <div class="sdx-formula-card">
        <h4>Cumulative return</h4>
        <div class="formula">\( CR_t = \left(\frac{P_t}{P_0} - 1\right) \times 100 \)</div>
        <p>Compare the current price to the price on event day. This tells a simple story: buy on the announcement and hold for t days, did you gain or lose?</p>
      </div>
      <div class="sdx-formula-card">
        <h4>Volatility</h4>
        <div class="formula">\( \sigma = \sqrt{\mathrm{Var}(R_t)} \)</div>
        <p>Take the standard deviation of the daily returns in the window. Bigger values mean the ride was choppier, even if the average move was flat.</p>
      </div>
      <div class="sdx-formula-card">
        <h4>Volume pulse</h4>
        <div class="formula">\( \Delta \mathrm{Vol} = \mathrm{avg}_{\text{post}} - \mathrm{avg}_{\text{pre}} \)</div>
        <p>Average the trading volume before and after the event and look at the difference. Positive numbers tell us more shares changed hands once the news hit.</p>
      </div>
    </div>

    <div class="sdx-panel" data-animate="fade-up" style="margin-top:1.8rem;">
      <p class="heading">Current implementation (pilot workflow)</p>
      <p class="sdx-note">
        Below is the workflow currently implemented for the first pilot and being generalized across all event families
        (GPUs, GenAI, Apple, and biotech).
      </p>
      <ul class="sdx-list">
        <li><strong>Predefine events:</strong> curate a dated innovation calendar for each family (e.g., CUDA, V100, RTX 2080 Ti, A100, Arm, H100, ChatGPT, Blackwell for the GPU set).</li>
        <li><strong>Pull OHLCV:</strong> fetch full price/volume history (current source: yfinance) and normalize dates.</li>
        <li><strong>Align dates:</strong> if an event date is not a trading day, shift to the next available session and tag relative time \(t\) with \(t=0\) on the event day.</li>
        <li><strong>Compute footprints:</strong> daily returns, log returns, cumulative returns from \(t=0\), pre/post means, pre/post volatility, and pre/post volume plus % change.</li>
        <li><strong>Export for visuals:</strong> save event-window tables and summary metrics for Plotly/Flourish and website figures.</li>
        <li><!-- TODO: Add benchmark model + AR/CAR + statistical significance. --><strong>TODO:</strong> add abnormal returns (AR/CAR) vs a benchmark model + significance tests.</li>
        <li><!-- TODO: Add overlap/confounder labeling (earnings, macro, leaks). --><strong>TODO:</strong> add overlap/confounder handling (earnings, macro, multi-day news).</li>
      </ul>
      <!-- TODO: Add a short paragraph on why we do not "discover" events automatically (measurement vs discovery). -->
    </div>
  </div>
</section>

<!-- CASE STUDIES / PILOTS -->
<section class="section sdx-section" id="cases">
  <div class="container">
    <h2 class="title is-3">Event types (in progress)</h2>
    <p>
      This project is still under construction. It is organized around four event families:
      GPUs, GenAI ecosystem milestones, Apple product/platform/silicon pivots, and (last) biotech approvals.
      Each family below has an event list, the analysis goals, and explicit placeholders like:
      <strong>“HERE add cumulative return plot for (this stock)”</strong>.
    </p>

    <div class="sdx-panel" data-animate="fade-up" style="margin-top:1.4rem;">
      <p class="heading">What is done vs. what is planned</p>
      <ul class="sdx-list">
        <li><strong>Done (core pipeline):</strong> event-day alignment, window extraction, returns/volume/volatility metrics, and export-ready tables for visuals.</li>
        <li><strong>In progress:</strong> benchmark-adjusted abnormal returns (AR/CAR), timing tags (pre-open/intraday/after-close), and robustness checks (overlaps/confounders).</li>
        <li><strong>Planned:</strong> multi-ticker ecosystem spillovers and cross-family comparisons (biotech comes last).</li>
      </ul>
    </div>

    <h3 class="title is-4" style="margin-top:2.4rem;">1) GPU platform &amp; hardware launches</h3>
    <p class="sdx-note">
      GPU “launch” dates are rarely clean. Announcements can happen at keynotes, in blog posts, or through staged embargoes;
      availability may lag by weeks; and rumor cycles can leak information into the pre-window.
      The goal here is not to claim one perfect date — it is to document what we treat as \(t=0\), then measure
      pre-drift, day-0 reaction, and post-drift in a consistent way.
    </p>

    <div class="sdx-grid-cards" style="margin-top:1.2rem;">
      <div class="sdx-card" data-animate="fade-up">
        <h3>Define \(t=0\)</h3>
        <ul class="sdx-list">
          <li><strong>Announcement vs availability:</strong> pick one and justify it.</li>
          <li><strong>Timing:</strong> pre-open / intraday / after-close determines the tradable session.</li>
          <li><strong>Alignment:</strong> if the date is not a trading day, shift to the next session.</li>
        </ul>
      </div>
      <div class="sdx-card" data-animate="fade-up">
        <h3>What to measure</h3>
        <ul class="sdx-list">
          <li><strong>Anticipation:</strong> drift and volume build-up in \(t=-30..-1\).</li>
          <li><strong>Impact:</strong> returns on day 0 / +1 and immediate volatility spikes.</li>
          <li><strong>Under-reaction:</strong> drift in \(t=+2..+30\) after the headline.</li>
        </ul>
      </div>
      <div class="sdx-card" data-animate="fade-up">
        <h3>What to add here</h3>
        <ul class="sdx-list">
          <li><strong>TODO:</strong> HERE add cumulative return windows for <em>(this stock)</em> around each GPU event.</li>
          <li><strong>TODO:</strong> HERE add volume + volatility footprints for <em>(this stock)</em>.</li>
          <li><strong>TODO:</strong> HERE add benchmark-adjusted AR/CAR + significance tests.</li>
        </ul>
      </div>
    </div>

    <div class="sdx-panel" data-animate="fade-up" style="margin-top:1.2rem;">
      <p class="heading">Reference event list (8)</p>
      <ul class="sdx-list">
        <li><strong>CUDA launch</strong> - June 23, 2007</li>
        <li><strong>Tesla V100 launch</strong> - May 10, 2017</li>
        <li><strong>RTX 2080 Ti launch</strong> - August 20, 2018</li>
        <li><strong>A100 Ampere launch</strong> - May 14, 2020</li>
        <li><strong>Arm acquisition announcement</strong> - September 13, 2020</li>
        <li><strong>H100 Hopper launch</strong> - March 22, 2022</li>
        <li><strong>ChatGPT / AI boom catalyst</strong> - November 30, 2022</li>
        <li><strong>Blackwell B200 announcement</strong> - March 18, 2024</li>
      </ul>
      <!-- TODO: Add a small table with event timing (pre-open/intraday/after-close) once curated. -->
    </div>

    <div class="sdx-chart-block" data-animate="fade-up" style="margin-top:1.8rem;">
      <h3 style="font-family:'Space Grotesk',sans-serif; margin-bottom:0.6rem;">
        HERE add cumulative return windows for (this stock)
      </h3>
      <p class="sdx-note">
        Add a grid of cumulative returns in a symmetric window around each GPU event (e.g., \(t=-30..+30\)).
        Mark \(t=0\) clearly and keep axes fixed so events are visually comparable.
      </p>
      <!-- TODO: Replace this block with an embed or exported figure. -->
      <!-- TODO: HERE add a second grid for volume and volatility footprints, event-aligned. -->
    </div>

    <div class="sdx-chart-block" data-animate="fade-up" style="margin-top:1.8rem;">
      <h3 style="font-family:'Space Grotesk',sans-serif; margin-bottom:0.6rem;">
        HERE add a long-horizon context view for (this stock)
      </h3>
      <p class="sdx-note">
        Add a multi-year view (price + cumulative return) with vertical lines for the major events above.
        Annotate obvious confounders (earnings, macro prints, overlapping news) so interpretation stays honest.
      </p>
      <!-- TODO: Replace this block with an embed or exported figure. -->
    </div>

    <h3 class="title is-4" style="margin-top:2.4rem;">Event deep dives (fill-here blocks)</h3>
    <p class="sdx-note">
      Each card below is intentionally unfinished. It’s a checklist for what to add per event once the analysis is finalized.
    </p>

    <div class="sdx-case-grid" style="margin-top:1.2rem;">
      <div class="sdx-case-card" data-animate="fade-up">
        <div class="sdx-tag"><span>NVIDIA</span><span>CUDA (2007)</span></div>
        <h3>CUDA: platform launch</h3>
        <ul class="sdx-list">
          <li><!-- TODO: Insert 3-panel plot (price, daily returns, cumulative returns) for CUDA window. --><strong>TODO:</strong> add per-event 3-panel plot.</li>
          <li><!-- TODO: Insert abnormal returns vs benchmark (AR, CAR). --><strong>TODO:</strong> add abnormal returns (AR/CAR) vs market model.</li>
          <li><!-- TODO: Write a 3-sentence interpretation: pre-drift, day-0 jump, post-drift. --><strong>TODO:</strong> write interpretation (pre / day 0 / post).</li>
        </ul>
      </div>

      <div class="sdx-case-card" data-animate="fade-up">
        <div class="sdx-tag"><span>NVIDIA</span><span>V100 (2017)</span></div>
        <h3>Tesla V100: AI hardware launch</h3>
        <ul class="sdx-list">
          <li><strong>TODO:</strong> add per-event plots (price/returns/cumulative returns).</li>
          <li><strong>TODO:</strong> add volume pulse and volatility shift panels.</li>
          <li><strong>TODO:</strong> document event timing + next trading-day alignment.</li>
        </ul>
      </div>

      <div class="sdx-case-card" data-animate="fade-up">
        <div class="sdx-tag"><span>NVIDIA</span><span>RTX 2080 Ti (2018)</span></div>
        <h3>RTX 2080 Ti: consumer GPU breakthrough</h3>
        <ul class="sdx-list">
          <li><strong>TODO:</strong> add per-event plots and summary metrics table.</li>
          <li><strong>TODO:</strong> check overlap with earnings/news cycle (confounders).</li>
          <li><strong>TODO:</strong> compare “consumer launch” vs “datacenter launch” archetypes.</li>
        </ul>
      </div>

      <div class="sdx-case-card" data-animate="fade-up">
        <div class="sdx-tag"><span>NVIDIA</span><span>A100 (2020)</span></div>
        <h3>A100: datacenter acceleration step</h3>
        <ul class="sdx-list">
          <li><strong>TODO:</strong> add AR/CAR vs benchmark (and robustness window sizes).</li>
          <li><strong>TODO:</strong> add volume/volatility comparison pre vs post.</li>
          <li><strong>TODO:</strong> note pandemic-era regime effects.</li>
        </ul>
      </div>

      <div class="sdx-case-card" data-animate="fade-up">
        <div class="sdx-tag"><span>NVIDIA</span><span>Arm (2020)</span></div>
        <h3>Arm acquisition announcement: corporate shock</h3>
        <ul class="sdx-list">
          <li><strong>TODO:</strong> add CAR decomposition (day 0 vs drift).</li>
          <li><strong>TODO:</strong> add peer/competitor spillover check (ARM ecosystem).</li>
          <li><strong>TODO:</strong> flag regulatory timeline confounders.</li>
        </ul>
      </div>

      <div class="sdx-case-card" data-animate="fade-up">
        <div class="sdx-tag"><span>NVIDIA</span><span>H100 (2022)</span></div>
        <h3>H100: AI training infrastructure launch</h3>
        <ul class="sdx-list">
          <li><strong>TODO:</strong> add per-event plots + benchmark-adjusted returns.</li>
          <li><strong>TODO:</strong> add “supply chain” spillover plots (planned).</li>
          <li><strong>TODO:</strong> clarify what counts as “launch” vs “availability”.</li>
        </ul>
      </div>

      <div class="sdx-case-card" data-animate="fade-up">
        <div class="sdx-tag"><span>Ecosystem</span><span>ChatGPT (2022)</span></div>
        <h3>ChatGPT: ecosystem shock</h3>
        <ul class="sdx-list">
          <li><strong>TODO:</strong> justify why <em>(this stock)</em> is the "treated" firm (and define peers).</li>
          <li><strong>TODO:</strong> add multi-ticker overlay (<em>(this stock)</em> + suppliers + hyperscalers).</li>
          <li><strong>TODO:</strong> add discussion of diffuse/slow information diffusion.</li>
        </ul>
      </div>

      <div class="sdx-case-card" data-animate="fade-up">
        <div class="sdx-tag"><span>NVIDIA</span><span>Blackwell (2024)</span></div>
        <h3>Blackwell B200: next-gen architecture announcement</h3>
        <ul class="sdx-list">
          <li><strong>TODO:</strong> add per-event plots + AR/CAR summary.</li>
          <li><strong>TODO:</strong> compare with H100: does the market “learn”?</li>
          <li><strong>TODO:</strong> add supplier constellation reaction (planned).</li>
        </ul>
      </div>
    </div>

    <h3 class="title is-4" style="margin-top:2.6rem;">2) GenAI ecosystem milestones</h3>
    <p class="sdx-note">
      GenAI events are not clean single-firm shocks. They spread across an ecosystem (model builders, cloud platforms,
      chip suppliers, apps). The hard part is defining what we mean by “the market reaction”: one ticker, a basket,
      or a spillover map.
    </p>

    <div class="sdx-grid-cards" style="margin-top:1.2rem;">
      <div class="sdx-card" data-animate="fade-up">
        <h3>Define the ecosystem</h3>
        <ul class="sdx-list">
          <li><strong>Treated set:</strong> which tickers are direct beneficiaries?</li>
          <li><strong>Spillover set:</strong> suppliers/partners/competitors that should react too.</li>
          <li><strong>Benchmark:</strong> tech sector ETF vs broad market vs factor model.</li>
        </ul>
      </div>
      <div class="sdx-card" data-animate="fade-up">
        <h3>Define \(t=0\)</h3>
        <ul class="sdx-list">
          <li><strong>Release vs announcement:</strong> public availability can matter more than press.</li>
          <li><strong>Timing:</strong> after-close news often shows up on \(t=+1\).</li>
          <li><strong>Leakage:</strong> rumors/teasers can create real pre-drift.</li>
        </ul>
      </div>
      <div class="sdx-card" data-animate="fade-up">
        <h3>What to add here</h3>
        <ul class="sdx-list">
          <li><strong>TODO:</strong> HERE add cumulative return windows for <em>(each ecosystem stock)</em> around each GenAI event.</li>
          <li><strong>TODO:</strong> HERE add treated-vs-spillover basket returns and compare.</li>
          <li><strong>TODO:</strong> HERE add a spillover heatmap around \(t=0\) (correlation / abnormal returns).</li>
        </ul>
      </div>
    </div>

    <div class="sdx-panel" data-animate="fade-up" style="margin-top:1.2rem;">
      <p class="heading">Reference event list (5)</p>
      <ul class="sdx-list">
        <li><strong>ChatGPT launch</strong> - November 30, 2022</li>
        <li><strong>Meta LLaMA release</strong> - February 24, 2023</li>
        <li><strong>GPT-4 release</strong> - March 14, 2023</li>
        <li><strong>Microsoft Copilot announcement</strong> - March 16, 2023</li>
        <li><strong>Google Bard launch</strong> - March 21, 2023</li>
      </ul>
      <!-- TODO: Add per-event timing tags and a short “why this date” citation for each. -->
    </div>

    <div class="sdx-chart-block" data-animate="fade-up" style="margin-top:1.8rem;">
      <h3 style="font-family:'Space Grotesk',sans-serif; margin-bottom:0.6rem;">
        HERE add GenAI ecosystem overlays (basket + spillovers)
      </h3>
      <p class="sdx-note">
        Add (1) a treated-vs-spillover basket plot around each event and (2) one ecosystem heatmap view that shows
        which tickers co-move most strongly in the event window.
      </p>
      <!-- TODO: Replace this block with an embed or exported figure. -->
    </div>

    <h3 class="title is-4" style="margin-top:2.6rem;">3) Apple product/platform/silicon pivots</h3>
    <p class="sdx-note">
      Apple events are famous for rumor cycles. That makes them perfect for testing anticipation (pre-drift), but it also
      makes \(t=0\) ambiguous: keynote announcements, preorder opens, and first-day sales are different “information moments”.
      This section treats that ambiguity as part of the analysis, not something to hide.
    </p>

    <div class="sdx-grid-cards" style="margin-top:1.2rem;">
      <div class="sdx-card" data-animate="fade-up">
        <h3>Define \(t=0\)</h3>
        <ul class="sdx-list">
          <li><strong>Keynote vs release:</strong> decide which is “the event” (or test both).</li>
          <li><strong>Timing:</strong> Apple keynotes often occur during market hours.</li>
          <li><strong>Leakage:</strong> separate “expected refresh” from true surprise pivots.</li>
        </ul>
      </div>
      <div class="sdx-card" data-animate="fade-up">
        <h3>What to measure</h3>
        <ul class="sdx-list">
          <li><strong>Anticipation:</strong> pre-window drift and volume.</li>
          <li><strong>Impact:</strong> day-0/+1 reaction (announcement-day jump).</li>
          <li><strong>Spillovers:</strong> suppliers/partners that should react alongside Apple.</li>
        </ul>
      </div>
      <div class="sdx-card" data-animate="fade-up">
        <h3>What to add here</h3>
        <ul class="sdx-list">
          <li><strong>TODO:</strong> HERE add cumulative return windows for <em>(this stock)</em> around each Apple event.</li>
          <li><strong>TODO:</strong> HERE add “announcement vs availability” sensitivity plots.</li>
          <li><strong>TODO:</strong> HERE add supply-chain spillover plots (supplier basket).</li>
        </ul>
      </div>
    </div>

    <div class="sdx-panel" data-animate="fade-up" style="margin-top:1.2rem;">
      <p class="heading">Reference event list (8)</p>
      <ul class="sdx-list">
        <li><strong>iPod launch</strong> - October 23, 2001</li>
        <li><strong>iPhone launch</strong> - June 29, 2007</li>
        <li><strong>iPad launch</strong> - April 3, 2010</li>
        <li><strong>iPhone 5S with Touch ID</strong> - September 20, 2013</li>
        <li><strong>Apple Watch launch</strong> - April 24, 2015</li>
        <li><strong>AirPods launch</strong> - December 13, 2016</li>
        <li><strong>M1 chip announcement</strong> - November 10, 2020</li>
        <li><strong>Vision Pro announcement</strong> - June 5, 2023</li>
      </ul>
      <!-- TODO: Add timing tags and clarify which date is announcement vs first-availability per event. -->
    </div>

    <div class="sdx-chart-block" data-animate="fade-up" style="margin-top:1.8rem;">
      <h3 style="font-family:'Space Grotesk',sans-serif; margin-bottom:0.6rem;">
        HERE add Apple windows + supply-chain overlays
      </h3>
      <p class="sdx-note">
        Add (1) a grid of cumulative return windows for the Apple events and (2) a companion panel that shows how
        key suppliers/partners move in the same windows (spillover).
      </p>
      <!-- TODO: Replace this block with an embed or exported figure. -->
    </div>

    <h3 class="title is-4" style="margin-top:2.6rem;">4) Biotech approvals &amp; treatment breakthroughs (kept for the end)</h3>
    <p class="sdx-note">
      Biotech is last on purpose: these events are messy and confounder-heavy. Trial readouts, FDA decisions,
      labeling changes, and reimbursement news can all hit the tape with different “information content”.
      If we don’t define \(t=0\) and the benchmark cleanly, we will fool ourselves.
    </p>

    <div class="sdx-grid-cards" style="margin-top:1.2rem;">
      <div class="sdx-card" data-animate="fade-up">
        <h3>Define \(t=0\)</h3>
        <ul class="sdx-list">
          <li><strong>Regulatory decisions:</strong> FDA approval dates are cleanest.</li>
          <li><strong>Trial readouts:</strong> preprints/press releases can leak before “official” news.</li>
          <li><strong>Availability:</strong> commercial launch may matter separately from approval.</li>
        </ul>
      </div>
      <div class="sdx-card" data-animate="fade-up">
        <h3>What to measure</h3>
        <ul class="sdx-list">
          <li><strong>Impact:</strong> large day-0 moves are common — consider shorter windows too.</li>
          <li><strong>Benchmarking:</strong> sector index/factor model matters more than in megacap tech.</li>
          <li><strong>Confounders:</strong> competing trial news, safety signals, and policy headlines.</li>
        </ul>
      </div>
      <div class="sdx-card" data-animate="fade-up">
        <h3>What to add here</h3>
        <ul class="sdx-list">
          <li><strong>TODO:</strong> HERE add cumulative return windows for <em>(this stock)</em> around each biotech event.</li>
          <li><strong>TODO:</strong> HERE add AR/CAR vs a biotech benchmark and discuss confounders.</li>
          <li><strong>TODO:</strong> HERE add a short “event definition” note with citations for every date.</li>
        </ul>
      </div>
    </div>

    <div class="sdx-panel" data-animate="fade-up" style="margin-top:1.2rem;">
      <p class="heading">Reference event list (7)</p>
      <ul class="sdx-list">
        <li><strong>First mRNA vaccine (Comirnaty)</strong> - December 11, 2020</li>
        <li><strong>Wegovy GLP-1 weight loss launch</strong> - June 4, 2021</li>
        <li><strong>Paxlovid oral antiviral launch</strong> - December 22, 2021</li>
        <li><strong>Mounjaro (Tirzepatide) launch</strong> - May 13, 2022</li>
        <li><strong>Leqembi Alzheimer’s approval</strong> - January 6, 2023</li>
        <li><strong>Zepbound obesity launch</strong> - November 8, 2023</li>
        <li><strong>Casgevy CRISPR therapy</strong> - December 8, 2023</li>
      </ul>
      <!-- TODO: Decide the ticker universe (originator + competitors) and add it here. -->
    </div>
  </div>
</section>

<!-- HOW TO READ -->
<section class="section sdx-section alt" id="how-to-read">
  <div class="container">
    <h2 class="title is-3">How to read our charts</h2>
    <div class="sdx-feature-list">
      <div class="sdx-feature-item" data-animate="fade-up">
        <p class="heading">Event windows</p>
        <p>
          Each plot is centered on day <strong>0</strong>, the trading day that reflects
          the announcement. Negative values on the x-axis are trading days before the event,
          positive values are trading days after. Most windows span 30 days before to
          30 days after the announcement.
        </p>
      </div>
      <div class="sdx-feature-item" data-animate="fade-up">
        <p class="heading">Cumulative vs. daily returns</p>
        <p>
          We show both daily percentage returns and <strong>cumulative returns from the
          event day</strong>. Cumulative returns answer questions like:
          “how much would you have gained or lost if you bought on the announcement day
          and held for 30 days?”
        </p>
      </div>
      <div class="sdx-feature-item" data-animate="fade-up">
        <p class="heading">Abnormal returns &amp; volume</p>
        <p>
          To isolate the innovation effect, we compare stock moves to a market benchmark.
          An abnormal return of <strong>+1%</strong> means the stock outperformed the
          market by 1% on that day. We also track changes in trading volume to detect
          whether attention and liquidity jump around events.
        </p>
      </div>
    </div>
  </div>
</section>

<!-- INTERACTIVE CHART #1 -->
<section class="section sdx-section" id="charts">
  <div class="container">
    <h2 class="title is-3">Typical reaction shapes around innovation events</h2>
    <p>
      Not every announcement looks the same. Some behave like classic "platform
      launches", others like hardware hype cycles or broad ecosystem shocks.
      The interactive chart below is a <strong>placeholder sketch</strong> (hard-coded toy curves).
      Once archetypes are finalized, we will replace this with averages computed from real event windows.
    </p>
    <div class="sdx-chart-block" data-animate="fade-up">
      <div class="sdx-toggle-group">
        <button class="sdx-toggle" data-archetype="platform">Platform launch (CUDA / App Store)</button>
        <button class="sdx-toggle" data-archetype="hardware">Hardware launch (V100 / RTX 2080 Ti)</button>
        <button class="sdx-toggle" data-archetype="ecosystem">Ecosystem shock (ChatGPT wave)</button>
      </div>
      <canvas id="eventReactionChart" style="max-height: 380px; margin-top: 1rem;"></canvas>
      <p class="sdx-note">
        Placeholder only. <strong>TODO:</strong> compute archetype-average cumulative returns from the real event window dataset and replace the toy values.
      </p>
    </div>
  </div>
</section>

<!-- INTERACTIVE CHART #2 -->
<section class="section sdx-section" id="surprise">
  <div class="container">
    <h2 class="title is-3">How surprise links to market reaction</h2>
    <p>
      Some events are expected (annual refresh cycles), others catch everyone off guard
      (a new AI architecture or a payment product out of nowhere). Below we sketch how
      the <em>surprise level</em> of an innovation relates to its average announcement-day
      abnormal return, for different types of events. This is currently a schematic placeholder.
    </p>
    <div class="sdx-chart-block" data-animate="fade-up">
      <div class="sdx-toggle-group">
        <button class="sdx-toggle" data-event-type="device">Device launches (iPhone-like)</button>
        <button class="sdx-toggle" data-event-type="ai-gpu">AI GPU launches (V100 / H100 / Blackwell)</button>
        <button class="sdx-toggle" data-event-type="fintech">Fintech moves (Apple Pay)</button>
      </div>
      <canvas id="surpriseChart" style="max-height: 320px; margin-top: 1rem;"></canvas>
      <p class="sdx-note">
        <strong>TODO:</strong> replace the toy bars with measured surprise proxies (pre-drift, pre-volume) and real day-0 abnormal returns.
      </p>
    </div>
  </div>
</section>

<!-- FLOURISH EMBEDS -->
<section class="section sdx-section" id="flourish">
  <div class="container">
    <h2 class="title is-3">Innovation timeline &amp; market overlays</h2>
    <p>Interactive views for the GPU pilot (currently NVIDIA).</p>
    <div class="sdx-chart-block" data-animate="fade-up">
      <div class="flourish-embed flourish-timeline" data-src="visualisation/26738865"></div>
      <div class="flourish-embed flourish-chart" data-src="visualisation/26723505" style="margin-top: 1.2rem;"></div>
      <div class="sdx-dual-panel" style="margin-top:1.2rem;">
        <div class="sdx-chart-block">
          <div class="flourish-embed flourish-chart" data-src="visualisation/26745064">
            <script src="https://public.flourish.studio/resources/embed.js"></script>
            <noscript><img src="https://public.flourish.studio/visualisation/26745064/thumbnail" width="100%" alt="chart visualization" /></noscript>
          </div>
        </div>
        <div class="sdx-chart-note">
          <h4>Innovation races</h4>
          <p>This animated scoreboard shows eight NVIDIA catalysts and how their share prices behaved from 30 days before the headline to 30 days after it.</p>
          <ul>
            <li>Each colored line tracks a different launch or ecosystem shock.</li>
            <li>The axes stay fixed, so you can compare the size and speed of each rally at a glance.</li>
            <li>Toggle “Scores” versus “Ranks” to switch between raw performance and a simple leaderboard.</li>
          </ul>
          <p style="margin-top:0.8rem;">It is the quick pulse-check before diving into the deeper event windows further down the page.</p>
        </div>
      </div>
    </div>
    <div class="sdx-dual-panel" data-animate="fade-up" style="margin-top:1.5rem;">
      <div class="sdx-chart-block" style="margin-top:0;">
        <div class="flourish-embed flourish-hierarchy" data-src="visualisation/26702135" style="width: 100%; height: 520px;">
          <noscript><img src="https://public.flourish.studio/visualisation/26702135/thumbnail" width="100%" alt="hierarchy visualization" /></noscript>
        </div>
      </div>
      <div class="sdx-chart-note">
        <h4>Supplier constellation</h4>
        <p>The bubble map reveals which sectors cradle NVIDIA’s GPU engine. Larger circles mark bigger slices of the supply pie, while colors group related functions.</p>
        <ul>
          <li><strong>Yellow:</strong> ETF and broad equity exposure. These investors transmit NVIDIA shocks to the rest of the market.</li>
          <li><strong>Blue/green:</strong> Infrastructure partners such as financial services, communication networks, and power utilities that keep data centers alive.</li>
          <li><strong>Purple/pink:</strong> Precision manufacturers providing memory, substrates, cooling hardware, and other components.</li>
        </ul>
        <p style="margin-top:0.8rem;">Most innovation stories are systems stories. This map shows where the ripple travels once NVIDIA announces a new chip.</p>
      </div>
    </div>
  </div>
</section>

<!-- FINDINGS (PLACEHOLDER) -->
<section class="section sdx-section alt" id="findings">
  <div class="container">
    <h2 class="title is-3">Findings (draft / fill-here)</h2>
    <p class="sdx-note">
      This is where the story should land: clear answers to the research questions above. It is intentionally unfinished
      until the benchmark model and robustness checks are finalized.
    </p>
    <div class="sdx-grid-cards" style="margin-top:1.2rem;">
      <div class="sdx-card" data-animate="fade-up">
        <h3>1) Pre-announcement drift</h3>
        <ul class="sdx-list">
          <li><strong>Goal:</strong> test whether prices/volume move before the “official” event day (anticipation or leakage).</li>
          <li><!-- TODO: Add plot of cumulative returns for t=-30..-1 and distribution across events. --><strong>TODO:</strong> add pre-window cumulative return plots + summary stats.</li>
          <li><!-- TODO: Add significance tests and multiple-comparisons note. --><strong>TODO:</strong> add significance tests + multiple-testing control.</li>
        </ul>
      </div>

      <div class="sdx-card" data-animate="fade-up">
        <h3>2) Announcement-day reaction (day 0 / +1)</h3>
        <ul class="sdx-list">
          <li><strong>Goal:</strong> measure the immediate reaction once the headline is tradable (timing-aware).</li>
          <li><!-- TODO: Add AR(0) and AR(+1) by event, with confidence intervals. --><strong>TODO:</strong> add AR(0), AR(+1), and confidence intervals.</li>
          <li><!-- TODO: Separate after-close vs pre-open events. --><strong>TODO:</strong> split by event timing (after-close vs pre-open).</li>
        </ul>
      </div>

      <div class="sdx-card" data-animate="fade-up">
        <h3>3) Post-event drift (under-reaction)</h3>
        <ul class="sdx-list">
          <li><strong>Goal:</strong> test whether the market keeps drifting after the headline (slow information diffusion).</li>
          <li><!-- TODO: Add CAR(0, +30) and CAR(+2, +30) and compare. --><strong>TODO:</strong> add CAR summaries and compare immediate vs delayed components.</li>
          <li><!-- TODO: Compare “platform” vs “product” vs “ecosystem” events. --><strong>TODO:</strong> compare drift by event archetype.</li>
        </ul>
      </div>

      <div class="sdx-card" data-animate="fade-up">
        <h3>4) Attention signals (volume &amp; volatility)</h3>
        <ul class="sdx-list">
          <li><strong>Goal:</strong> measure whether attention/uncertainty spikes around innovations, even when price barely moves.</li>
          <li><!-- TODO: Add volume and volatility deltas, pre vs post. --><strong>TODO:</strong> add pre/post volume and volatility deltas for each event.</li>
          <li><!-- TODO: Add spillover analysis for supplier/competitor sets. --><strong>TODO:</strong> add spillover plots (ecosystem tickers).</li>
        </ul>
      </div>
    </div>
  </div>
</section>

<!-- LIMITATIONS / ROBUSTNESS (CHECKLIST) -->
<section class="section sdx-section" id="robustness">
  <div class="container">
    <h2 class="title is-3">Limitations &amp; robustness (checklist)</h2>
    <div class="sdx-panel" data-animate="fade-up" style="margin-top:1.2rem;">
      <p class="heading">What can break an event study</p>
      <ul class="sdx-list">
        <li><strong>Confounders:</strong> earnings, guidance, macro prints, and multi-day news cycles near the event window.</li>
        <li><strong>Date ambiguity:</strong> “announcement” vs “launch” vs “availability” vs “leak”.</li>
        <li><strong>Overlapping events:</strong> clustered innovations can make attribution impossible without extra structure.</li>
        <li><strong>Benchmark choice:</strong> market vs sector vs factor model changes what “abnormal” means.</li>
        <li><strong>Selection bias:</strong> picking only famous successes inflates perceived footprints.</li>
      </ul>
      <ul class="sdx-list" style="margin-top:0.8rem;">
        <li><!-- TODO: Add a robustness table per event: timing, overlap, confounders, benchmark used. --><strong>TODO:</strong> add a per-event robustness table (timing, overlaps, confounders, benchmark).</li>
        <li><!-- TODO: Add a short ethics/disclaimer paragraph. --><strong>TODO:</strong> add ethics note + “not investment advice” disclaimer.</li>
        <li><!-- TODO: Add references/data sources section with links. --><strong>TODO:</strong> add references + data sources (APIs, filings, press releases).</li>
      </ul>
    </div>
  </div>
</section>

<!-- TEAM / LINKS -->
<section class="section sdx-section" id="team">
  <div class="container">
    <h2 class="title is-3">Team and resources</h2>
    <div class="sdx-team">
      <div class="sdx-panel" data-animate="fade-up">
        <p><strong>Team:</strong> SwissDataExplorers</p>
        <ul class="sdx-list">
          <li><strong>Rami</strong>: data pipelines, event study implementation, NVIDIA case study</li>
          <li><strong>Teammate 1</strong>: event curation, Apple ecosystem timeline, documentation</li>
          <li><strong>Teammate 2</strong>: visualization, narrative and website integration</li>
        </ul>
        <p>
          All code, notebooks and the full report are available on our GitHub repository:
        </p>
        <p>
          <a href="https://github.com/YDIB11/Swissdata" target="_blank">
            View project on GitHub
          </a>
        </p>
      </div>
      <div class="sdx-panel" data-animate="fade-up">
        <p class="heading">What you’ll find there</p>
        <ul class="sdx-list">
          <li><strong>Data loaders &amp; cleaning:</strong> robust OHLCV pipelines with split detection.</li>
          <li><strong>Event calendar:</strong> curated CSV of innovation milestones with timing tags.</li>
          <li><strong>Analysis notebooks:</strong> event windows, AR/CAR, volume &amp; volatility.</li>
          <li><strong>Visualization tools:</strong> candlestick dashboards, correlation heatmaps, and the charts used here.</li>
        </ul>
      </div>
    </div>
    <div class="sdx-cta-panel" data-animate="fade-up">
      <div>
        <p class="title is-5">Want to go beyond the headline plots?</p>
        <p class="sdx-note">
          Reach out if you’d like to reuse our event calendar, replicate the event-study
          code or plug your own innovation stories into the framework.
        </p>
      </div>
      <div class="sdx-cta-actions">
        <a class="sdx-btn sdx-btn-primary" href="#cases">Revisit case studies</a>
        <a class="sdx-btn sdx-btn-ghost" href="https://github.com/YDIB11/Swissdata" target="_blank">Open GitHub</a>
      </div>
    </div>
  </div>
</section>

<!-- JS and Chart.js -->
<script src="https://public.flourish.studio/resources/embed.js"></script>
<script src="https://cdn.jsdelivr.net/npm/chart.js"></script>

<script>
document.addEventListener("DOMContentLoaded", function () {
  const palette = {
    line: "#5df0ff",
    bar: "#ffc46a",
    grid: "rgba(255,255,255,0.08)",
    text: "#d9e2ff"
  };

  // Scroll-triggered reveal animations
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

  // Data for interactive chart #1 – stylized cumulative reaction shapes
  const days = [-5, -4, -3, -2, -1, 0, 1, 2, 3, 4, 5];

  const archetypeData = {
    platform: [-1.0, -0.8, -0.5, -0.3, -0.2, 1.2, 1.8, 2.1, 2.3, 2.4, 2.5],
    hardware: [-0.5, -0.3, -0.1, 0.0, 0.2, 1.8, 2.4, 2.9, 3.1, 3.2, 3.3],
    ecosystem: [-0.2, -0.1, 0.0, 0.1, 0.3, 0.6, 1.1, 1.7, 2.4, 3.0, 3.5]
  };

  const ctx1 = document.getElementById("eventReactionChart").getContext("2d");

  const eventChart = new Chart(ctx1, {
    type: "line",
    data: {
      labels: days,
      datasets: [
        {
          label: "Cumulative return from event day (%)",
          data: archetypeData.platform,
          borderColor: palette.line,
          backgroundColor: "rgba(93, 240, 255, 0.15)",
          tension: 0.35,
          borderWidth: 3,
          pointRadius: 4,
          pointBackgroundColor: "#0d1024",
          pointBorderColor: palette.line
        }
      ]
    },
    options: {
      responsive: true,
      maintainAspectRatio: false,
      plugins: {
        legend: { display: false },
        title: {
          display: true,
          text: "Stylized cumulative returns around innovation events (day 0 = announcement)",
          color: palette.text,
          font: { family: "Space Grotesk", weight: "600" }
        }
      },
      scales: {
        x: {
          title: { display: true, text: "Days relative to event", color: palette.text },
          grid: { color: palette.grid },
          ticks: { color: palette.text }
        },
        y: {
          title: { display: true, text: "Cumulative return (%)", color: palette.text },
          grid: { color: palette.grid },
          ticks: { color: palette.text }
        }
      }
    }
  });

  // Buttons to switch archetype on chart #1
  const archetypeButtons = document.querySelectorAll("[data-archetype]");
  archetypeButtons.forEach(function (btn) {
    btn.addEventListener("click", function () {
      const archetype = this.getAttribute("data-archetype");
      eventChart.data.datasets[0].data = archetypeData[archetype];
      eventChart.update();
    });
  });

  // Data for interactive chart #2 – toy relation between surprise and reaction
  const surpriseLevels = ["Low", "Medium", "High"];

  const surpriseData = {
    "device":  [0.2, 0.8, 1.4],
    "ai-gpu":  [0.3, 1.2, 2.0],
    "fintech": [0.1, 0.6, 1.1]
  };

  const ctx2 = document.getElementById("surpriseChart").getContext("2d");
  const surpriseChart = new Chart(ctx2, {
    type: "bar",
    data: {
      labels: surpriseLevels,
      datasets: [
        {
          label: "Average abnormal return on day 0 (%)",
          data: surpriseData["device"],
          backgroundColor: [
            "rgba(93, 240, 255, 0.5)",
            "rgba(93, 240, 255, 0.7)",
            "rgba(93, 240, 255, 0.9)"
          ],
          borderRadius: 8,
          borderSkipped: false
        }
      ]
    },
    options: {
      responsive: true,
      maintainAspectRatio: false,
      plugins: {
        legend: { display: false },
        title: {
          display: true,
          text: "Innovation surprise vs. announcement-day reaction (schematic)",
          color: palette.text,
          font: { family: "Space Grotesk", weight: "600" }
        }
      },
      scales: {
        x: {
          title: { display: true, text: "Innovation surprise", color: palette.text },
          grid: { color: palette.grid },
          ticks: { color: palette.text }
        },
        y: {
          title: { display: true, text: "Abnormal return on day 0 (%)", color: palette.text },
          grid: { color: palette.grid },
          ticks: { color: palette.text }
        }
      }
    }
  });

  // Buttons to switch event type on chart #2
  const eventTypeButtons = document.querySelectorAll("[data-event-type]");
  eventTypeButtons.forEach(function (btn) {
    btn.addEventListener("click", function () {
      const eventType = this.getAttribute("data-event-type");
      surpriseChart.data.datasets[0].data = surpriseData[eventType];
      surpriseChart.update();
    });
  });
});
</script>
