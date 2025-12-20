---
layout: page
title: "About the project"
subtitle: "Data, methods and results"
permalink: /about/
---

<section class="section sdx-section" id="about">
  <div class="container">
    <div class="sdx-hero-panel sdx-hero-panel--spaced" data-animate="scale">
      <div class="sdx-hero-grid">
        <div data-animate="fade-up">
          <span class="sdx-pill">About</span>
          <h1 class="sdx-hero-title">The Team Behind <span>SwissDataExplorers</span></h1>
          <p class="sdx-hero-body">
            This project turns market history into a readable story. We study how stocks respond when innovation hits,
            sometimes instantly, sometimes weeks later, and sometimes not at all.
          </p>
          <div class="sdx-hero-actions">
            <a class="sdx-btn sdx-btn-primary" href="#team">Meet the team</a>
            <a class="sdx-btn sdx-btn-ghost" href="{{ '/' | relative_url }}">Back to home</a>
            <a class="sdx-btn sdx-btn-ghost" href="{{ '/references/' | relative_url }}">References</a>
          </div>
        </div>

        <div class="sdx-hero-media" data-animate="fade-up">
          <img
            class="sdx-hero-media-img"
            src="{{ '/assets/img1.png' | relative_url }}"
            alt="Abstract visualization for innovation footprints and markets"
            loading="lazy"
            decoding="async"
          />
          <div class="sdx-hero-media-overlay">
            <div class="sdx-hero-media-card">
              <h4>What this page covers</h4>
              <p>Team, datasets, and a quick walkthrough of the method behind the site.</p>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="sdx-panel" data-animate="fade-up">
      <h2 class="title is-4">Project overview</h2>
      <div class="content">
        <p>
          We asked a simple question with a complicated answer: when a breakthrough happens, does the market price it immediately,
          or only after the meaning becomes obvious?
        </p>
        <p>
          To find out, we ran an event-study style analysis across dozens of innovation moments and translated the results into the narrative
          you see on the homepage. The goal is not to predict the future. It is to measure <strong>market recognition</strong>.
        </p>
      </div>
    </div>

    <div class="sdx-panel sdx-team-panel" id="team" data-animate="fade-up">
      <h2 class="title is-4">Meet the team</h2>
      <p style="margin: 0.35rem 0 0; color: rgba(159, 176, 255, 0.95);">
        Photos are placeholders for now.
      </p>

      <div class="sdx-team-grid">
        <div class="sdx-team-card" data-animate="fade-up">
          <img class="sdx-team-avatar" src="{{ '/assets/team_pics/youssefdib.jpeg' | relative_url }}" alt="Portrait of Youssef Dib" loading="lazy" decoding="async" />
          <div class="sdx-team-meta">
            <h3 class="sdx-team-name">Youssef Dib</h3>
            <p class="sdx-team-role">SwissDataExplorers2025</p>
          </div>
        </div>

        <div class="sdx-team-card" data-animate="fade-up">
          <img class="sdx-team-avatar" src="{{ '/assets/team_pics/ramiaschkar.jpg' | relative_url }}" alt="Portrait of Rami Aschkar" loading="lazy" decoding="async" />
          <div class="sdx-team-meta">
            <h3 class="sdx-team-name">Rami Aschkar</h3>
            <p class="sdx-team-role">SwissDataExplorers2025</p>
          </div>
        </div>

        <div class="sdx-team-card" data-animate="fade-up">
          <img class="sdx-team-avatar" src="{{ '/assets/team_pics/kevinabj.jpeg' | relative_url }}" alt="Portrait of Kevin Abou Jaoude" loading="lazy" decoding="async" />
          <div class="sdx-team-meta">
            <h3 class="sdx-team-name">Kevin Abou Jaoude</h3>
            <p class="sdx-team-role">SwissDataExplorers2025</p>
          </div>
        </div>

        <div class="sdx-team-card sdx-team-card-wide" data-animate="fade-up">
          <img class="sdx-team-avatar" src="{{ '/assets/team_pics/chloeabouhalka.jpeg' | relative_url }}" alt="Portrait of Chloe Abou Halka" loading="lazy" decoding="async" />
          <div class="sdx-team-meta">
            <h3 class="sdx-team-name">Chloe Abou Halka</h3>
            <p class="sdx-team-role">SwissDataExplorers2025</p>
          </div>
        </div>

        <div class="sdx-team-card sdx-team-card-wide" data-animate="fade-up">
          <img class="sdx-team-avatar" src="{{ '/assets/team_pics/michelbassil.jpeg' | relative_url }}" alt="Portrait of Michel Bassil" loading="lazy" decoding="async" />
          <div class="sdx-team-meta">
            <h3 class="sdx-team-name">Michel Bassil</h3>
            <p class="sdx-team-role">SwissDataExplorers2025</p>
          </div>
        </div>
      </div>
    </div>

    <div class="sdx-panel" data-animate="fade-up">
      <h2 class="title is-4">Data and method</h2>
      <div class="content">
        <h3 class="title is-5">Data sources</h3>
        <ul class="sdx-list">
          <li><strong>Kaggle Stock Market Dataset (1962-2020)</strong> for long-run historical prices</li>
          <li><strong>Yahoo Finance (2020-2024 extension)</strong> to bring the analysis into the recent AI era</li>
          <li><strong>Official company newsrooms</strong> to validate dates and align the narrative with real announcements</li>
        </ul>

        <p>
          The whole site is built to make one idea tangible: markets do not react to innovation in a single universal way.
          They react based on visibility, timing, uncertainty, and whether a binary gate exists (like regulatory approval).
        </p>

        <h3 class="title is-5">Tools</h3>
        <ul class="sdx-list">
          <li>Python for data processing and event-study metrics</li>
          <li>Plotly for interactive figures</li>
          <li>Flourish for animated rankings and flow diagrams</li>
          <li>Jekyll (Bulma Clean Theme) for the website layer</li>
        </ul>
      </div>
    </div>

    <div class="sdx-panel" data-animate="fade-up">
      <h2 class="title is-4">Explore the work</h2>
      <div class="sdx-hero-actions" style="margin-top: 0.8rem;">
        <a class="sdx-btn sdx-btn-primary" href="{{ '/' | relative_url }}#prologue">Start the story</a>
        <a class="sdx-btn sdx-btn-ghost" href="{{ '/' | relative_url }}#case-files">Jump to chapters</a>
      </div>
    </div>

  </div>
</section>
