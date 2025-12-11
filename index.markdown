---
layout: page
title: "SwissDataExplorers"
subtitle: "Innovation Footprints in Tech Stock Markets"
---

<!-- Custom fonts and styling to modernize the page without removing content -->
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;600;700&family=Source+Sans+3:wght@400;600;700&display=swap" rel="stylesheet">

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
  background: rgba(255, 255, 255, 0.05);
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

hr {
  border: none;
  border-top: 1px solid var(--border);
  margin: 2.5rem 0;
}

.sdx-hero-panel {
  margin-top: -60px;
  background: linear-gradient(145deg, rgba(255, 255, 255, 0.03), rgba(255, 255, 255, 0.01));
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
  background: rgba(255, 255, 255, 0.04);
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
  background: rgba(255, 255, 255, 0.03);
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
  background: rgba(255, 255, 255, 0.02);
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
  background: rgba(255, 255, 255, 0.03);
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
  background: rgba(255, 255, 255, 0.02);
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
  background: linear-gradient(180deg, rgba(93, 240, 255, 0.06), rgba(255, 255, 255, 0.02));
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
  background: rgba(255, 255, 255, 0.01);
  border: 1px solid var(--border);
  border-radius: 18px;
  padding: 2.8rem;
}

.sdx-timeline {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  gap: 1rem;
}

.sdx-step {
  position: relative;
  padding: 1.2rem 1.1rem 1.1rem 1.1rem;
  border-radius: 14px;
  border: 1px solid var(--border);
  background: rgba(255, 255, 255, 0.02);
  transition: transform 0.25s ease, border-color 0.25s ease;
}

.sdx-step .pill {
  font-size: 0.85rem;
  color: var(--muted);
}

.sdx-step h4 {
  font-family: "Space Grotesk", "Source Sans 3", sans-serif;
  color: #f7f9ff;
  margin: 0.35rem 0;
}

.sdx-step:hover {
  transform: translateY(-3px);
  border-color: rgba(93, 240, 255, 0.35);
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
  background: rgba(255, 255, 255, 0.05);
}

.sdx-chart-block {
  margin-top: 1.5rem;
  padding: 1.6rem;
  border-radius: 16px;
  background: radial-gradient(circle at 10% 20%, rgba(93, 240, 255, 0.08), transparent 55%),
              radial-gradient(circle at 90% 10%, rgba(255, 196, 106, 0.12), transparent 45%),
              rgba(255, 255, 255, 0.03);
  border: 1px solid var(--border);
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
  background: rgba(255, 255, 255, 0.04);
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
  background: linear-gradient(120deg, rgba(93, 240, 255, 0.08), rgba(255, 255, 255, 0.02));
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

<!-- LONG-FORM INTRO /<!-- LONG-FORM INTRO / STORY -->
<section class="section sdx-section alt" id="story">
  <div class="container">
    <div class="sdx-story-body">
      <div class="sdx-panel sdx-panel-summary" data-animate="fade-up">
        <h3 class="title is-5">In one paragraph</h3>
        <p>
          We turn landmark tech innovations into “exam questions” for the stock market.
          By aligning precise event dates with decades of daily price and volume data,
          building market models and computing abnormal returns, we measure how quickly
          markets recognize breakthroughs in GPUs, smartphones, app ecosystems and
          fintech rails.
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
          The rest of the page walks through case studies (NVIDIA &amp; Apple) and
          aggregate patterns built on this framework.
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
          To build this exam, we start with a carefully curated calendar of
          innovation events: CUDA’s first release, major AI GPU launches like
          Tesla V100 and RTX 2080 Ti, the H100 and Blackwell announcements,
          the first iPhone, the App Store launch, Apple Pay, and other
          well-documented milestones in tech and biotech. For each of them,
          we align the exact announcement timing to US trading days—after-close
          news is anchored to the next day’s open—so we are grading the market
          on the days when it actually had a chance to react.
        </p>
        <p>
          On the data side, we work with decades of daily stock information—open,
          high, low, close and volume—for US-listed technology and biotech
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
          knows the ending—NVIDIA in the AI era, the iPhone and the App Store
          for Apple—and show how the price and volume behaved around those dates.
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
          a sharp, forward-looking judge of technology—or more like a distracted
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
    <div class="sdx-stats-row">
      <div class="sdx-stat-card" data-animate="fade-up">
        <div class="label">Years of daily data</div>
        <div class="value">1965–2025</div>
      </div>
      <div class="sdx-stat-card" data-animate="fade-up">
        <div class="label">Listed firms in universe</div>
        <div class="value">100+</div>
      </div>
      <div class="sdx-stat-card" data-animate="fade-up">
        <div class="label">Curated innovation events</div>
        <div class="value">50+</div>
      </div>
      <div class="sdx-stat-card" data-animate="fade-up">
        <div class="label">Days per event window</div>
        <div class="value">61</div>
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
      symmetric window of trading days and compare what actually happened to what a
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
      Apple Pay, AI GPUs and more.
    </p>
  </div>
</section>

<!-- PIPELINE / METHOD -->
<section class="section sdx-section" id="pipeline">
  <div class="container">
    <h2 class="title is-3">From raw OHLCV to innovation footprints</h2>
    <div class="sdx-timeline">
      <div class="sdx-step" data-animate="fade-up">
        <div class="pill">Step 1</div>
        <h4>Collect</h4>
        <p class="is-small">
          Load decades of daily OHLCV data from the course dataset and extend it to today
          with Yahoo Finance. Build a compact CSV of innovation events with
          <code>Ticker</code>, <code>Event_Date</code>, <code>Type</code>, and source links.
        </p>
      </div>
      <div class="sdx-step" data-animate="fade-up">
        <div class="pill">Step 2</div>
        <h4>Align</h4>
        <p class="is-small">
          Map each event to the correct trading day (shifting after-close announcements
          to the next day) and slice event windows, typically 30 days before to
          30 days after the announcement.
        </p>
      </div>
      <div class="sdx-step" data-animate="fade-up">
        <div class="pill">Step 3</div>
        <h4>Model</h4>
        <p class="is-small">
          Estimate a market model for each stock on a pre-event estimation window.
          Compute daily returns, log returns, volatility and <strong>abnormal returns</strong>
          relative to the predicted benchmark.
        </p>
      </div>
      <div class="sdx-step" data-animate="fade-up">
        <div class="pill">Step 4</div>
        <h4>Aggregate &amp; compare</h4>
        <p class="is-small">
          Turn abnormal returns into cumulative returns (CAR), compare pre- and post-event
          behavior, and group results by innovation type, firm size, sector and time period.
        </p>
      </div>
    </div>
    <p class="sdx-note" style="margin-top:1.2rem;">
      Under the hood we use standard formulas for percentage returns
      <code>R<sub>t</sub> = (P<sub>t</sub> / P<sub>t-1</sub> - 1) × 100</code>,
      log returns <code>r<sub>t</sub> = ln(P<sub>t</sub> / P<sub>t-1</sub>) × 100</code>,
      cumulative returns
      <code>CR<sub>t</sub> = (P<sub>t</sub> / P<sub>0</sub> - 1) × 100</code>,
      volatility (standard deviation of returns), and volume changes
      comparing pre- vs post-event average volume.
    </p>
  </div>
</section>

<!-- CASE STUDIES -->
<section class="section sdx-section" id="cases">
  <div class="container">
    <h2 class="title is-3">Headliner case studies: NVIDIA &amp; Apple</h2>
    <p>
      Before aggregating over dozens of firms, we zoom in on a few iconic stories.
      NVIDIA’s AI GPU roadmap and Apple’s ecosystem launches give us a front-row view
      of how markets digest truly transformative news.
    </p>
    <div class="sdx-case-grid" style="margin-top:1.4rem;">
      <div class="sdx-case-card" data-animate="fade-up">
        <div class="sdx-tag"><span>NVIDIA</span><span>Platform launch</span></div>
        <h3>CUDA: when GPUs became general-purpose</h3>
        <p>
          On <strong>June 23, 2007</strong> NVIDIA launched CUDA, turning the GPU from a
          graphics card into a programmable compute platform. Our 30-day window shows a
          deep pre-event drawdown followed by a slow, hesitant recovery.
        </p>
        <ul class="sdx-list">
          <li>Event type: <strong>Platform launch</strong></li>
          <li>30-day cumulative return from event: <strong>+2.6%</strong></li>
          <li>Pattern: pain before the breakthrough, modest relief after.</li>
        </ul>
      </div>
      <div class="sdx-case-card" data-animate="fade-up">
        <div class="sdx-tag"><span>NVIDIA</span><span>AI GPUs</span></div>
        <h3>Tesla V100 &amp; RTX 2080 Ti: AI goes mainstream</h3>
        <p>
          The <strong>Tesla V100</strong> (May 2017) brought Tensor Cores to data centers,
          while the <strong>RTX 2080 Ti</strong> (August 2018) put real-time ray tracing
          into gamers’ rigs. Both launches show clear positive momentum after the event,
          with 30-day returns above <strong>+15%</strong> in some windows.
        </p>
        <ul class="sdx-list">
          <li>Event type: <strong>Product launches</strong></li>
          <li>Post-event behavior: strong, sustained rally.</li>
        </ul>
      </div>
      <div class="sdx-case-card" data-animate="fade-up">
        <div class="sdx-tag"><span>Apple</span><span>Device &amp; ecosystem</span></div>
        <h3>iPhone, App Store, Apple Pay: building a platform</h3>
        <p>
          Apple’s story is a sequence: the <strong>iPhone</strong> launch in 2007,
          the <strong>App Store</strong> opening in 2008, and
          <strong>Apple Pay</strong> in 2014. Together they turn a device into a
          network of developers and payments. Our event windows track whether the
          market prices each step or only the long-run arc.
        </p>
        <ul class="sdx-list">
          <li>Events: device, marketplace, and fintech launch.</li>
          <li>Key question: does the market react more to the gadget or to the ecosystem?</li>
        </ul>
      </div>
    </div>

    <!-- Static NVDA plots -->
    <div class="sdx-chart-block" data-animate="fade-up" style="margin-top:2rem;">
      <h3 style="font-family:'Space Grotesk',sans-serif; margin-bottom:0.6rem;">
        NVIDIA innovation windows
      </h3>
      <p class="sdx-note">
        Cumulative returns over a 30-day window around eight NVIDIA innovation events.
        Each panel is centered on the announcement day (vertical line), with pre- and
        post-event periods shaded.
      </p>
      <!-- Replace src with the actual path to your 8-panel figure -->
      <img src="assets/nvidia_event_windows.png"
           alt="Eight NVIDIA innovation events with 30-day cumulative returns around each announcement."
           style="width:100%; border-radius:12px; margin-top:1rem;">
    </div>

    <div class="sdx-chart-block" data-animate="fade-up" style="margin-top:2rem;">
      <h3 style="font-family:'Space Grotesk',sans-serif; margin-bottom:0.6rem;">
        NVIDIA in the AI era
      </h3>
      <p class="sdx-note">
        NVIDIA stock price and cumulative return since early 2022, with vertical lines
        marking the H100 launch, the public release of ChatGPT, and the Blackwell B200
        announcement. This is what an innovation wave looks like when it hits the market.
      </p>
      <!-- Replace src with the actual path to your AI-era figure -->
      <img src="assets/nvidia_ai_era.png"
           alt="NVIDIA stock price and cumulative return since 2022 with key AI events highlighted."
           style="width:100%; border-radius:12px; margin-top:1rem;">
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
      Not every announcement looks the same. Some behave like classic “platform
      launches”, others like hardware hype cycles or broad ecosystem shocks.
      The interactive chart below shows stylized average <strong>cumulative returns</strong>
      for three archetypes over an 11-day window.
    </p>
    <div class="sdx-chart-block" data-animate="fade-up">
      <div class="sdx-toggle-group">
        <button class="sdx-toggle" data-archetype="platform">Platform launch (CUDA / App Store)</button>
        <button class="sdx-toggle" data-archetype="hardware">Hardware launch (V100 / RTX 2080 Ti)</button>
        <button class="sdx-toggle" data-archetype="ecosystem">Ecosystem shock (ChatGPT wave)</button>
      </div>
      <canvas id="eventReactionChart" style="max-height: 380px; margin-top: 1rem;"></canvas>
      <p class="sdx-note">
        These curves are schematic summaries based on our event windows; the static charts
        above show the full event-level detail.
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
      abnormal return, for different types of events.
    </p>
    <div class="sdx-chart-block" data-animate="fade-up">
      <div class="sdx-toggle-group">
        <button class="sdx-toggle" data-event-type="device">Device launches (iPhone-like)</button>
        <button class="sdx-toggle" data-event-type="ai-gpu">AI GPU launches (V100 / H100 / Blackwell)</button>
        <button class="sdx-toggle" data-event-type="fintech">Fintech moves (Apple Pay)</button>
      </div>
      <canvas id="surpriseChart" style="max-height: 320px; margin-top: 1rem;"></canvas>
      <p class="sdx-note">
        In the full analysis, we quantify “surprise” using pre-event drift and volume,
        then compare it to actual abnormal returns on day 0.
      </p>
    </div>
  </div>
</section>

<!-- FLOURISH EMBEDS -->
<section class="section sdx-section" id="flourish">
  <div class="container">
    <h2 class="title is-3">Innovation timeline &amp; market overlays</h2>
    <p>Interactive views for Nvidia.</p>
    <div class="sdx-chart-block" data-animate="fade-up">
      <div class="flourish-embed flourish-timeline" data-src="visualisation/26738865"></div>
      <div class="flourish-embed flourish-chart" data-src="visualisation/26723505" style="margin-top: 1.2rem;"></div>
      <div class="flourish-embed flourish-hierarchy" data-src="visualisation/26702135" style="margin-top: 1.2rem; max-width: 900px; height: 520px; margin-left: auto; margin-right: auto;">
        <noscript><img src="https://public.flourish.studio/visualisation/26702135/thumbnail" width="100%" alt="hierarchy visualization" /></noscript>
      </div>
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
          <li><strong>Rami</strong> — data pipelines, event study implementation, NVIDIA case study</li>
          <li><strong>Teammate 1</strong> — event curation, Apple ecosystem timeline, documentation</li>
          <li><strong>Teammate 2</strong> — visualization, narrative and website integration</li>
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
  const heroContainer = document.querySelector(".hero.is-primary .container");
  if (heroContainer) {
    const existingPill = heroContainer.querySelector(".hero-pill");
    const titleNode = heroContainer.querySelector(".title");
    if (!existingPill && titleNode) {
      const pill = document.createElement("div");
      pill.className = "hero-pill";
      pill.textContent = "Innovation intelligence • Event-study research";
      heroContainer.insertBefore(pill, titleNode);
    }
    if (!heroContainer.querySelector(".hero-head-actions")) {
      const actions = document.createElement("div");
      actions.className = "hero-head-actions";
      actions.innerHTML = `
        <a class="sdx-btn sdx-btn-primary" href="#cases">Explore case studies</a>
        <a class="sdx-btn sdx-btn-ghost" href="#pipeline">See the workflow</a>
      `;
      heroContainer.appendChild(actions);
    }
  }

  const heroBody = document.querySelector(".hero.is-primary .hero-body");
  if (heroBody && !heroBody.querySelector("#heroChartBg")) {
    const canvas = document.createElement("canvas");
    canvas.id = "heroChartBg";
    canvas.className = "hero-chart-bg";
    canvas.height = 260;
    heroBody.prepend(canvas);

    const ctxHero = canvas.getContext("2d");
    const heroLabels = ["-30d", "-25d", "-20d", "-15d", "-10d", "-5d", "0", "+5d", "+10d", "+15d", "+20d"];
    const heroPrice = [92, 94, 91, 95, 99, 102, 107, 111, 115, 118, 122];
    const heroVolume = [12, 15, 10, 16, 13, 18, 22, 19, 17, 20, 18];
    const areaGradient = ctxHero.createLinearGradient(0, 0, 0, canvas.height);
    areaGradient.addColorStop(0, "rgba(93, 240, 255, 0.35)");
    areaGradient.addColorStop(1, "rgba(4, 17, 35, 0)");

    new Chart(ctxHero, {
      type: "line",
      data: {
        labels: heroLabels,
        datasets: [
          {
            type: "bar",
            data: heroVolume,
            backgroundColor: "rgba(255, 196, 106, 0.25)",
            borderRadius: 20,
            barPercentage: 0.45,
            categoryPercentage: 1,
            order: 1
          },
          {
            type: "line",
            data: heroPrice,
            borderColor: "#5df0ff",
            borderWidth: 3,
            fill: true,
            backgroundColor: areaGradient,
            tension: 0.38,
            pointRadius: 0,
            order: 2
          }
        ]
      },
      options: {
        responsive: true,
        maintainAspectRatio: false,
        animation: false,
        plugins: {
          legend: { display: false },
          tooltip: { enabled: false }
        },
        scales: {
          x: {
            display: false,
            grid: { display: false }
          },
          y: {
            display: false,
            grid: { display: false }
          }
        }
      }
    });
  }

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
