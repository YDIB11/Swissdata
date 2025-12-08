---
layout: page
title: "SwissDataExplorers"
subtitle: "Can the market see the future?"
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

.navbar {
  background: var(--panel) !important;
  box-shadow: 0 10px 40px rgba(0, 0, 0, 0.35);
}

.navbar a.navbar-item,
.navbar .navbar-item,
.navbar a.navbar-item:visited {
  color: var(--text) !important;
  font-weight: 600;
}

.navbar .navbar-item.is-active {
  color: var(--accent) !important;
}

.hero.is-primary {
  background: linear-gradient(135deg, #111a38 0%, #0b2847 50%, #0b0f26 100%);
  border-bottom: 1px solid var(--border);
  position: relative;
  overflow: hidden;
}

.hero.is-primary::after {
  content: "";
  position: absolute;
  inset: 0;
  background: radial-gradient(circle at 30% 20%, rgba(93, 240, 255, 0.16), transparent 35%),
              radial-gradient(circle at 80% 10%, rgba(255, 196, 106, 0.2), transparent 30%);
  pointer-events: none;
}

.hero .title,
.hero .subtitle {
  font-family: "Space Grotesk", "Source Sans 3", sans-serif;
  letter-spacing: -0.02em;
}

.hero .title {
  color: #f7f9ff;
}

.hero .subtitle {
  color: var(--muted);
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
}

.sdx-hero-panel::after {
  background: #ffc46a;
  bottom: -80px;
  left: -80px;
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
}

.sdx-card h3 {
  color: #f7f9ff;
  font-weight: 700;
  margin-bottom: 0.25rem;
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
}

.sdx-case-card h3 {
  margin-bottom: 0.35rem;
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
}

.sdx-cta-panel .title {
  margin: 0;
}

.sdx-cta-actions {
  display: flex;
  gap: 0.75rem;
}

a {
  color: var(--accent);
}

a:hover {
  color: #7ef7ff;
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
    <div class="sdx-hero-panel">
      <div class="sdx-hero-grid">
        <div>
          <div class="sdx-pill"><span>Innovation x Markets</span></div>
          <h2 class="sdx-hero-title">Can the market see the future?</h2>
          <p class="sdx-hero-body">
            This is our ADA 2025 data story. We explore whether stock markets react
            to innovation events (product launches, keynotes, major announcements)
            in a systematic and predictable way.
          </p>
          <div class="sdx-hero-actions">
            <a class="sdx-btn sdx-btn-primary" href="#charts">Explore reactions</a>
            <a class="sdx-btn sdx-btn-ghost" href="#team">Team and resources</a>
          </div>
        </div>
        <div class="sdx-hero-badge">
          <h4>How we approach it</h4>
          <p class="sdx-hero-body">
            We quantify how markets price innovation events and look for consistent
            reaction patterns across companies and event types.
          </p>
          <div class="sdx-hero-stats">
            <div class="sdx-mini-stat">
              <div class="label">Trading days</div>
              <div class="value">10k+</div>
            </div>
            <div class="sdx-mini-stat">
              <div class="label">Tech companies</div>
              <div class="value">100+</div>
            </div>
            <div class="sdx-mini-stat">
              <div class="label">Events</div>
              <div class="value">500+</div>
            </div>
            <div class="sdx-mini-stat">
              <div class="label">ML models</div>
              <div class="value">4</div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- WHY THIS MATTERS -->
<section class="section sdx-section" id="why">
  <div class="container">
    <h2 class="title is-3">Why this matters</h2>
    <div class="sdx-grid-cards">
      <div class="sdx-card">
        <h3>Markets are messy</h3>
        <p>
          Innovation drives long-term value, but markets do not always react
          in a clean, textbook way. Sometimes they anticipate, sometimes
          they overreact, and sometimes they ignore news that looks important on paper.
        </p>
      </div>
      <div class="sdx-card">
        <h3>Our angle</h3>
        <p>
          Our goal is to quantify how markets price innovation events and to see
          whether we can detect consistent reaction patterns across companies
          and event types.
        </p>
      </div>
      <div class="sdx-card">
        <h3>Questions we ask</h3>
        <ul class="sdx-list">
          <li>Do "big launches" always yield positive abnormal returns?</li>
          <li>Is the reaction symmetric for good vs. bad surprises?</li>
          <li>Are some companies systematically overhyped?</li>
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
      <div class="sdx-stat-card">
        <div class="label">Trading days</div>
        <div class="value">10k+</div>
      </div>
      <div class="sdx-stat-card">
        <div class="label">Tech companies</div>
        <div class="value">100+</div>
      </div>
      <div class="sdx-stat-card">
        <div class="label">Events</div>
        <div class="value">500+</div>
      </div>
      <div class="sdx-stat-card">
        <div class="label">ML models</div>
        <div class="value">4</div>
      </div>
    </div>
  </div>
</section>

<!-- STORY OVERVIEW -->
<section class="section sdx-section alt" id="overview">
  <div class="container">
    <h2 class="title is-3">Our main question</h2>
    <p>
      When a company announces a major innovation (for example a new device, a breakthrough
      product, or a strategic shift), does the market:
    </p>
    <ul class="sdx-list">
      <li>React instantly on the announcement day?</li>
      <li>Anticipate the news before it happens?</li>
      <li>Underreact and adjust over the next few days?</li>
    </ul>
    <p>
      We combine daily stock prices with a curated set of innovation-related events
      and analyze abnormal returns around each event.
    </p>
  </div>
</section>

<!-- PIPELINE / METHOD -->
<section class="section sdx-section" id="pipeline">
  <div class="container">
    <h2 class="title is-3">From raw data to insight</h2>
    <div class="sdx-timeline">
      <div class="sdx-step">
        <div class="pill">Step 1</div>
        <h4>Collect</h4>
        <p class="is-small">
          Stock prices (NASDAQ), innovation events (product launches, announcements),
          and market benchmarks.
        </p>
      </div>
      <div class="sdx-step">
        <div class="pill">Step 2</div>
        <h4>Align</h4>
        <p class="is-small">
          Match each event to the corresponding ticker and trading days,
          and build event windows.
        </p>
      </div>
      <div class="sdx-step">
        <div class="pill">Step 3</div>
        <h4>Model</h4>
        <p class="is-small">
          Estimate expected returns using market models, compute abnormal returns,
          and feed them to machine learning models.
        </p>
      </div>
      <div class="sdx-step">
        <div class="pill">Step 4</div>
        <h4>Explain</h4>
        <p class="is-small">
          Visualize how reactions differ by company, event type, and time horizon.
        </p>
      </div>
    </div>
  </div>
</section>

<!-- CASE STUDIES -->
<section class="section sdx-section" id="cases">
  <div class="container">
    <h2 class="title is-3">Case studies (teaser)</h2>
    <div class="sdx-case-grid">
      <div class="sdx-case-card">
        <div class="sdx-tag"><span>Example 1</span><span>Big device launch</span></div>
        <h3>Fast spike, mild correction</h3>
        <p>
          Strong positive reaction on day 0, followed by a mild correction.
        </p>
        <ul class="sdx-list">
          <li>Company: <strong>Apple-like</strong></li>
          <li>Peak abnormal return: <strong>+2.0%</strong></li>
          <li>Drift over 5 days: <strong>+0.5%</strong></li>
        </ul>
        <p class="sdx-note">
          In the final version, this card will show a real event from our dataset.
        </p>
      </div>
      <div class="sdx-case-card">
        <div class="sdx-tag"><span>Example 2</span><span>Overhyped keynote</span></div>
        <h3>Anticipation then disappointment</h3>
        <p>
          Strong run-up before the event, flat or negative abnormal return on day 0.
        </p>
        <ul class="sdx-list">
          <li>Pattern: <strong>anticipation then disappointment</strong></li>
          <li>Pre-event drift: <strong>+3%</strong></li>
          <li>Event-day abnormal: <strong>-1%</strong></li>
        </ul>
      </div>
      <div class="sdx-case-card">
        <div class="sdx-tag"><span>Example 3</span><span>Under-the-radar update</span></div>
        <h3>Slow burn</h3>
        <p>
          No big move on day 0, but slow positive drift over the next week.
        </p>
        <ul class="sdx-list">
          <li>Market initially ignores the news</li>
          <li>Post-event drift: <strong>+1.5%</strong></li>
        </ul>
      </div>
    </div>
  </div>
</section>

<!-- HOW TO READ -->
<section class="section sdx-section alt" id="how-to-read">
  <div class="container">
    <h2 class="title is-3">How to read our charts</h2>
    <div class="sdx-feature-list">
      <div class="sdx-feature-item">
        <p class="heading">Event window</p>
        <p>
          We center each chart on day <strong>0</strong>, the event day. Negative
          values on the x-axis are days before the event, positive values are
          days after.
        </p>
      </div>
      <div class="sdx-feature-item">
        <p class="heading">Abnormal returns</p>
        <p>
          Returns are adjusted for overall market movements. A value of
          <strong>+1%</strong> means the stock outperformed our benchmark by 1%
          on that day.
        </p>
      </div>
      <div class="sdx-feature-item">
        <p class="heading">Aggregation</p>
        <p>
          Curves represent averages over many events of the same type
          (for example product launches for a given company).
        </p>
      </div>
    </div>
  </div>
</section>

<!-- INTERACTIVE CHART #1 -->
<section class="section sdx-section" id="charts">
  <div class="container">
    <h2 class="title is-3">How does the market react around an event?</h2>
    <p>
      Explore the average abnormal return around a hypothetical innovation event.
      Use the buttons to switch between example companies. Later we will plug in our
      real estimated abnormal returns.
    </p>
    <div class="sdx-chart-block">
      <div class="sdx-toggle-group">
        <button class="sdx-toggle" data-company="apple">Apple</button>
        <button class="sdx-toggle" data-company="microsoft">Microsoft</button>
        <button class="sdx-toggle" data-company="tesla">Tesla</button>
      </div>
      <canvas id="eventReactionChart" style="max-height: 380px; margin-top: 1rem;"></canvas>
    </div>
  </div>
</section>

<!-- INTERACTIVE CHART #2 -->
<section class="section sdx-section" id="surprise">
  <div class="container">
    <h2 class="title is-3">Surprise vs. reaction by event type</h2>
    <p>
      A toy example of how <em>innovation surprise</em> (how unexpected the event is)
      could relate to average abnormal returns on the announcement day. Use the buttons
      to switch between different event types.
    </p>
    <div class="sdx-chart-block">
      <div class="sdx-toggle-group">
        <button class="sdx-toggle" data-event-type="product">Product launches</button>
        <button class="sdx-toggle" data-event-type="keynote">Keynotes</button>
        <button class="sdx-toggle" data-event-type="ma">M&amp;A / strategic deals</button>
      </div>
      <canvas id="surpriseChart" style="max-height: 320px; margin-top: 1rem;"></canvas>
    </div>
  </div>
</section>

<!-- TEAM / LINKS -->
<section class="section sdx-section" id="team">
  <div class="container">
    <h2 class="title is-3">Team and resources</h2>
    <div class="sdx-team">
      <div class="sdx-panel">
        <p><strong>Team:</strong> SwissDataExplorers</p>
        <ul class="sdx-list">
          <li>Rami -- data pipelines and modeling</li>
          <li>Team member -- event curation and labeling</li>
          <li>Team member -- visualization and narrative</li>
        </ul>
        <p>
          Code, notebooks and the full report are available on our GitHub repo:
        </p>
        <p>
          <a href="https://github.com/USERNAME/REPO" target="_blank">
            View project on GitHub
          </a>
        </p>
      </div>
      <div class="sdx-panel">
        <p class="heading">Deliverables</p>
        <ul class="sdx-list">
          <li>Exploratory notebooks</li>
          <li>Cleaned event and price datasets</li>
          <li>Model comparison (baseline vs ML)</li>
          <li>Final report and slides</li>
        </ul>
      </div>
    </div>
    <div class="sdx-cta-panel">
      <div>
        <p class="title is-5">Want to dive deeper?</p>
        <p class="sdx-note">Reach out for the data, model details, or the full slide deck.</p>
      </div>
      <div class="sdx-cta-actions">
        <a class="sdx-btn sdx-btn-primary" href="#charts">See charts</a>
        <a class="sdx-btn sdx-btn-ghost" href="https://github.com/USERNAME/REPO" target="_blank">Open GitHub</a>
      </div>
    </div>
  </div>
</section>

<!-- JS and Chart.js -->
<script src="https://cdn.jsdelivr.net/npm/chart.js"></script>

<script>
document.addEventListener("DOMContentLoaded", function () {
  const palette = {
    line: "#5df0ff",
    bar: "#ffc46a",
    grid: "rgba(255,255,255,0.08)",
    text: "#d9e2ff"
  };

  // Data for interactive chart #1 (toy data to start with)
  const days = [-5, -4, -3, -2, -1, 0, 1, 2, 3, 4, 5];

  const eventData = {
    apple:     [-0.2, 0.1, 0.0, 0.2, 0.3, 1.5, 0.8, 0.3, 0.1, 0.0, -0.1],
    microsoft: [-0.1, 0.0, 0.1, 0.1, 0.2, 0.9, 0.5, 0.2, 0.1, 0.0, 0.0],
    tesla:     [-0.5, 0.0, 0.3, 0.5, 0.8, 2.0, 1.2, 0.6, 0.2, 0.0, -0.2]
  };

  const ctx1 = document.getElementById("eventReactionChart").getContext("2d");

  const eventChart = new Chart(ctx1, {
    type: "line",
    data: {
      labels: days,
      datasets: [
        {
          label: "Average abnormal return (%)",
          data: eventData.apple,
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
          text: "Abnormal return around event day (day 0)",
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
          title: { display: true, text: "Abnormal return (%)", color: palette.text },
          grid: { color: palette.grid },
          ticks: { color: palette.text }
        }
      }
    }
  });

  // Buttons to switch company on chart #1
  const companyButtons = document.querySelectorAll("[data-company]");
  companyButtons.forEach(function (btn) {
    btn.addEventListener("click", function () {
      const company = this.getAttribute("data-company");
      eventChart.data.datasets[0].data = eventData[company];
      eventChart.update();
    });
  });

  // Data for interactive chart #2 (toy data per event type)
  const surpriseLevels = ["Low", "Medium", "High"];

  const surpriseData = {
    product:  [0.2, 0.8, 1.5],
    keynote:  [0.1, 0.5, 0.9],
    ma:       [-0.3, 0.4, 1.2]
  };

  const ctx2 = document.getElementById("surpriseChart").getContext("2d");
  const surpriseChart = new Chart(ctx2, {
    type: "bar",
    data: {
      labels: surpriseLevels,
      datasets: [
        {
          label: "Average abnormal return on day 0 (%)",
          data: surpriseData.product,
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
          text: "Event surprise vs. market reaction (toy example)",
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
          title: { display: true, text: "Abnormal return (%)", color: palette.text },
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
