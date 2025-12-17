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
    tex: { inlineMath: [["\\(", "\\)"]], displayMath: [["$$", "$$"], ["\\[", "\\]"]] },
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

.title,
.subtitle {
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

/* Chapters modal */
.sdx-modal .modal-card {
  width: min(780px, calc(100vw - 2rem));
  background: radial-gradient(circle at 18% 22%, rgba(159, 176, 255, 0.14) 0, transparent 45%),
              radial-gradient(circle at 88% 10%, rgba(255, 196, 106, 0.10) 0, transparent 40%),
              linear-gradient(180deg, rgba(13, 16, 36, 0.96) 0%, rgba(7, 10, 26, 0.96) 100%);
  border: 1px solid var(--border);
  border-radius: 16px;
  box-shadow: 0 35px 80px rgba(0, 0, 0, 0.62);
  overflow: hidden;
}

.sdx-modal .modal-card-head,
.sdx-modal .modal-card-foot {
  background: rgba(10, 12, 28, 0.8);
  border-color: rgba(255, 255, 255, 0.08);
}

.sdx-modal .modal-card-title {
  color: #f7f9ff;
  font-family: "Space Grotesk", "Source Sans 3", sans-serif;
  font-weight: 700;
  letter-spacing: -0.02em;
}

.sdx-modal .modal-card-body {
  background: transparent;
}

.sdx-modal-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 1rem;
}

@media (max-width: 768px) {
  .sdx-modal-grid {
    grid-template-columns: 1fr;
  }
}

.sdx-modal-box {
  border: 1px solid rgba(255, 255, 255, 0.08);
  border-radius: 14px;
  background: rgba(13, 16, 36, 0.55);
  padding: 0.9rem 1rem;
}

.sdx-modal-links {
  display: grid;
  gap: 0.5rem;
  margin-top: 0.65rem;
}

.sdx-chapter-link {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 0.75rem;
  padding: 0.65rem 0.75rem;
  border-radius: 12px;
  border: 1px solid rgba(255, 255, 255, 0.08);
  background: rgba(255, 255, 255, 0.03);
  color: var(--text) !important;
  text-decoration: none !important;
  transition: background 0.2s ease, transform 0.2s ease, border-color 0.2s ease;
}

.sdx-chapter-link:hover {
  background: rgba(159, 176, 255, 0.10);
  border-color: rgba(159, 176, 255, 0.24);
  transform: translateY(-1px);
}

.sdx-chapter-link .sdx-kicker {
  color: var(--muted);
  font-weight: 700;
  letter-spacing: 0.02em;
  text-transform: uppercase;
  font-size: 0.72rem;
}

.sdx-chapter-link .sdx-label {
  color: #f7f9ff;
  font-weight: 700;
  letter-spacing: -0.01em;
}

.sdx-modal-hint {
  color: rgba(232, 237, 255, 0.78);
  margin-top: 0.75rem;
  font-size: 0.95rem;
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

.content table {
  width: 100%;
  border-collapse: separate;
  border-spacing: 0;
  margin: 1rem 0;
  border-radius: 14px;
  overflow: hidden;
  border: 1px solid var(--border);
  background: rgba(13, 16, 36, 0.72);
}

.content table th,
.content table td {
  padding: 0.65rem 0.8rem;
  border-bottom: 1px solid rgba(255, 255, 255, 0.08);
  border-right: 1px solid rgba(255, 255, 255, 0.08);
  vertical-align: top;
}

.content table th:last-child,
.content table td:last-child {
  border-right: none;
}

.content table tr:last-child td {
  border-bottom: none;
}

.content table th {
  background: rgba(15, 21, 48, 0.75);
  color: #f7f9ff;
  font-weight: 700;
  font-family: "Space Grotesk", "Source Sans 3", sans-serif;
}

.content table td {
  color: var(--text);
}

.content table tr:nth-child(even) td {
  background: rgba(13, 16, 36, 0.55);
}

.sdx-section {
  padding: 3rem 0 2.5rem;
}

.sdx-section.alt {
  background: rgba(13, 16, 36, 0.55);
  border: 1px solid var(--border);
  border-radius: 18px;
  padding: 2.8rem;
  margin: 2.25rem 0;
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

.sdx-back-to-top {
  position: fixed;
  right: 1.25rem;
  bottom: 1.25rem;
  z-index: 40;
  width: 46px;
  height: 46px;
  display: grid;
  place-items: center;
  border-radius: 14px;
  border: 1px solid var(--border);
  background: rgba(13, 16, 36, 0.78);
  color: var(--text);
  box-shadow: 0 18px 45px rgba(0, 0, 0, 0.45);
  cursor: pointer;
  backdrop-filter: blur(14px);
  -webkit-backdrop-filter: blur(14px);
  opacity: 0;
  pointer-events: none;
  transform: translateY(10px) scale(0.98);
  transition: opacity 0.2s ease, transform 0.2s ease, border-color 0.2s ease, background 0.2s ease, box-shadow 0.2s ease, color 0.2s ease;
}

.sdx-back-to-top::after {
  content: "Back to top";
  position: absolute;
  right: calc(100% + 0.75rem);
  top: 50%;
  transform: translateY(-50%) translateX(10px);
  padding: 0.35rem 0.6rem;
  border-radius: 999px;
  border: 1px solid var(--border);
  background: rgba(13, 16, 36, 0.9);
  color: var(--text);
  font-weight: 700;
  letter-spacing: 0.02em;
  font-size: 0.8rem;
  opacity: 0;
  pointer-events: none;
  transition: opacity 0.2s ease, transform 0.2s ease;
  white-space: nowrap;
}

.sdx-back-to-top.is-visible {
  opacity: 1;
  pointer-events: auto;
  transform: none;
}

.sdx-back-to-top:hover {
  border-color: rgba(159, 176, 255, 0.45);
  color: #f7f9ff;
  box-shadow: 0 22px 55px rgba(0, 0, 0, 0.55);
  transform: translateY(-2px);
}

.sdx-back-to-top:hover::after,
.sdx-back-to-top:focus-visible::after {
  opacity: 1;
  transform: translateY(-50%) translateX(0);
}

.sdx-back-to-top:focus-visible {
  outline: 2px solid rgba(255, 196, 106, 0.9);
  outline-offset: 3px;
}

.sdx-back-to-top svg {
  width: 20px;
  height: 20px;
  transition: transform 0.2s ease;
}

.sdx-back-to-top:hover svg {
  transform: translateY(-1px);
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

.sdx-formula-grid {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 0.9rem;
  margin-top: 1.1rem;
}

.sdx-formula-grid.sdx-formula-grid-core .sdx-formula-card:last-child {
  grid-column: 1 / -1;
}

.sdx-step-grid {
  display: grid;
  gap: 1rem;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  margin-top: 1.25rem;
}

.sdx-step-card {
  border-radius: 16px;
  padding: 1.2rem 1.25rem;
  background: linear-gradient(150deg, rgba(159, 176, 255, 0.07), rgba(255, 196, 106, 0.08));
  border: 1px solid var(--border);
  box-shadow: 0 18px 40px rgba(0, 0, 0, 0.28);
  position: relative;
  overflow: hidden;
}

.sdx-step-card::after {
  content: "";
  position: absolute;
  inset: -40% -20% auto auto;
  width: 180px;
  height: 180px;
  border-radius: 50%;
  background: rgba(159, 176, 255, 0.08);
  filter: blur(30px);
  pointer-events: none;
}

.sdx-step-head {
  display: flex;
  align-items: center;
  gap: 0.7rem;
}

.sdx-step-num {
  width: 34px;
  height: 34px;
  border-radius: 999px;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  border: 1px solid rgba(255, 255, 255, 0.14);
  background: rgba(5, 8, 20, 0.55);
  color: #f7f9ff;
  font-family: "Space Grotesk", "Source Sans 3", sans-serif;
  font-weight: 700;
}

.sdx-step-card .title {
  margin: 0;
}

.sdx-step-card p {
  margin: 0.65rem 0 0;
  color: var(--muted);
}

.sdx-formula-card {
  border: 1px solid rgba(255, 255, 255, 0.12);
  border-radius: 16px;
  padding: 1rem 1.1rem;
  background: rgba(13, 16, 36, 0.78);
  box-shadow: 0 18px 40px rgba(0, 0, 0, 0.32);
  position: relative;
  overflow: hidden;
}

.sdx-formula-card::after {
  content: "";
  position: absolute;
  width: 90px;
  height: 90px;
  top: -35px;
  right: -35px;
  border-radius: 50%;
  background: rgba(159, 176, 255, 0.12);
  filter: blur(22px);
}

.sdx-formula-card h4 {
  margin: 0;
  font-size: 0.9rem;
  text-transform: uppercase;
  letter-spacing: 0.1em;
  color: var(--accent-2);
}

.sdx-formula-card .formula {
  margin-top: 0.55rem;
  padding: 0.65rem 0.8rem;
  border-radius: 14px;
  background: rgba(5, 8, 20, 0.55);
  border: 1px solid var(--border);
  color: #f7f9ff;
  text-align: center;
  overflow-x: auto;
  overflow-y: hidden;
  scrollbar-width: none;
  -ms-overflow-style: none;
  font-family: "Space Grotesk", "Source Sans 3", sans-serif;
}

.sdx-panel[id^="chapter-"] { padding: 2rem; }
.sdx-panel[id^="chapter-"] + .sdx-panel[id^="chapter-"] { margin-top: 2.5rem; }

.sdx-chapter-hero {
  position: relative;
  margin: 1.15rem 0 1.6rem;
  height: 240px;
  border-radius: 18px;
  overflow: hidden;
  border: 1px solid var(--border);
  background: rgba(13, 16, 36, 0.55);
  box-shadow: 0 18px 40px rgba(0, 0, 0, 0.28);
}

.sdx-chapter-hero-img {
  position: absolute;
  inset: 0;
  width: 100%;
  height: 100%;
  object-fit: cover;
  object-position: center;
  transform: scale(1.06);
  opacity: 0.32;
  filter: saturate(1.05) contrast(1.06);
}

.sdx-chapter-hero--top .sdx-chapter-hero-img {
  object-position: center top;
}

.sdx-chapter-hero::after {
  content: "";
  position: absolute;
  inset: 0;
  background:
    radial-gradient(circle at 18% 20%, rgba(159, 176, 255, 0.22), transparent 55%),
    radial-gradient(circle at 82% 10%, rgba(255, 196, 106, 0.18), transparent 55%),
    linear-gradient(180deg, rgba(5, 8, 20, 0.25), rgba(5, 8, 20, 0.95) 82%);
  pointer-events: none;
}

.sdx-chapter-hero-caption {
  position: relative;
  z-index: 1;
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: flex-end;
  gap: 0.25rem;
  padding: 1rem 1.1rem;
}

.sdx-chapter-hero-kicker {
  display: inline-flex;
  align-items: center;
  gap: 0.4rem;
  font-weight: 700;
  letter-spacing: 0.12em;
  text-transform: uppercase;
  font-size: 0.72rem;
  color: rgba(232, 237, 255, 0.82);
}

.sdx-chapter-hero-title {
  margin: 0;
  font-family: "Space Grotesk", "Source Sans 3", sans-serif;
  font-weight: 700;
  letter-spacing: -0.02em;
  font-size: 1.15rem;
  color: #f7f9ff;
}

@media (max-width: 980px) {
  .sdx-chapter-hero {
    height: 200px;
  }
}


.sdx-formula-card .formula::-webkit-scrollbar {
  width: 0;
  height: 0;
}

.sdx-formula-card .formula mjx-container {
  overflow: visible !important;
}

.sdx-formula-card p {
  margin: 0.55rem 0 0;
  font-size: 0.88rem;
  color: var(--muted);
}

.sdx-list {
  padding-left: 1.1rem;
  margin: 0.6rem 0;
}

.sdx-list li {
  padding: 0.12rem 0;
}

.sdx-case-grid {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-items: stretch;
  gap: 1rem;
  margin-top: 1.25rem;
  margin-bottom: 1.5rem;
}

.sdx-case-grid + .sdx-panel {
  margin-top: 1.25rem;
}

.sdx-case-grid .sdx-case-card {
  flex: 1 1 280px;
  max-width: 360px;
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
  margin-bottom: 0.2rem;
}

.sdx-case-card-wide {
  flex-basis: 100%;
  max-width: 760px;
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
  margin: 1.5rem 0 1.25rem;
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

.sdx-embed-block {
  margin: 1.75rem 0 1.75rem;
}

.sdx-embed-block.is-tight {
  margin-bottom: 0.85rem;
}

.sdx-embed-stack {
  display: grid;
  gap: 1.35rem;
}

.sdx-embed-grid {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 1.35rem;
  align-items: stretch;
}

.sdx-embed-card {
  border-radius: 18px;
  border: 1px solid var(--border);
  background: rgba(13, 16, 36, 0.68);
  box-shadow: 0 16px 40px rgba(0, 0, 0, 0.3);
  overflow: hidden;
  transition: transform 0.3s ease, box-shadow 0.3s ease, border-color 0.3s ease;
}

.sdx-embed-card:hover {
  transform: translateY(-2px);
  border-color: rgba(159, 176, 255, 0.32);
  box-shadow: 0 20px 50px rgba(0, 0, 0, 0.36);
}

.sdx-embed-head {
  display: flex;
  align-items: baseline;
  justify-content: space-between;
  gap: 0.75rem;
  padding: 0.75rem 0.9rem;
  background: rgba(5, 8, 20, 0.12);
  border-bottom: 1px solid rgba(255, 255, 255, 0.06);
}

.sdx-embed-title {
  margin: 0;
  font-family: "Space Grotesk", "Source Sans 3", sans-serif;
  font-weight: 700;
  letter-spacing: -0.02em;
  font-size: 1rem;
  color: #f7f9ff;
}

.sdx-embed-kicker {
  color: rgba(232, 237, 255, 0.8);
  font-weight: 700;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  font-size: 0.72rem;
  white-space: nowrap;
}

.sdx-embed-body {
  padding: 0.55rem;
  background: rgba(5, 8, 20, 0.28);
}

.sdx-embed-body iframe {
  width: 100%;
  height: 780px;
  display: block;
  border: 0;
  overflow: hidden;
  border-radius: 14px;
  background: rgba(13, 16, 36, 0.55);
}

.sdx-formula-block {
  background: rgba(13, 16, 36, 0.82);

}

.sdx-placeholder {
  border-style: dashed;
  border-color: rgba(159, 176, 255, 0.45);
}

.sdx-window-visual {
  margin-top: 1.15rem;
  border-radius: 16px;
  border: 1px solid var(--border);
  background: radial-gradient(circle at 20% 20%, rgba(159, 176, 255, 0.10), transparent 55%),
              rgba(5, 8, 20, 0.35);
  padding: 1.1rem 1.1rem 0.9rem;
  overflow: hidden;
}

.sdx-window-svg {
  width: 100%;
  height: auto;
  display: block;
}

.sdx-window-axis {
  stroke: rgba(255, 255, 255, 0.24);
  stroke-width: 4;
  stroke-linecap: round;
  stroke-dasharray: 1200;
  stroke-dashoffset: 1200;
}

.sdx-window-tick {
  stroke: rgba(255, 255, 255, 0.20);
  stroke-width: 2;
  opacity: 0.9;
}

.sdx-window-label {
  fill: rgba(232, 237, 255, 0.92);
  font-size: 14px;
  font-weight: 600;
  opacity: 0;
}

.sdx-window-label-muted {
  fill: rgba(159, 176, 255, 0.95);
  font-size: 13px;
  font-weight: 700;
  letter-spacing: 0.03em;
  text-transform: uppercase;
}

.sdx-window-pre,
.sdx-window-post {
  stroke-width: 1;
  opacity: 0;
  transform: scaleX(0);
  transform-box: fill-box;
}

.sdx-window-pre {
  fill: rgba(159, 176, 255, 0.16);
  stroke: rgba(159, 176, 255, 0.42);
  transform-origin: 100% 50%;
}

.sdx-window-post {
  fill: rgba(78, 205, 196, 0.14);
  stroke: rgba(78, 205, 196, 0.38);
  transform-origin: 0% 50%;
}

.sdx-window-event {
  stroke: rgba(255, 196, 106, 0.95);
  stroke-width: 4;
  stroke-linecap: round;
  stroke-dasharray: 300;
  stroke-dashoffset: 300;
  opacity: 0;
}

.sdx-window-glow {
  fill: rgba(255, 196, 106, 0.85);
  opacity: 0;
}

.sdx-window-glow-soft {
  fill: rgba(255, 196, 106, 0.20);
  filter: blur(10px);
  opacity: 0;
}

.sdx-window-steps {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 0.9rem;
  margin-top: 1.1rem;
}

.sdx-window-step {
  border-radius: 16px;
  border: 1px solid var(--border);
  background: rgba(13, 16, 36, 0.62);
  padding: 1rem 1.05rem;
  opacity: 0;
  transform: translateY(10px);
}

.sdx-window-step h4 {
  margin: 0;
  font-family: "Space Grotesk", "Source Sans 3", sans-serif;
  font-size: 0.95rem;
  letter-spacing: 0.01em;
}

.sdx-window-step p {
  margin: 0.55rem 0 0;
  color: var(--text);
  font-size: 0.95rem;
}

.sdx-window-step .sdx-chip {
  display: inline-flex;
  align-items: center;
  gap: 0.4rem;
  margin-bottom: 0.55rem;
  padding: 0.25rem 0.7rem;
  border-radius: 999px;
  border: 1px solid var(--border);
  font-weight: 700;
  font-size: 0.78rem;
  letter-spacing: 0.06em;
  text-transform: uppercase;
}

.sdx-window-step-pre .sdx-chip {
  color: rgba(159, 176, 255, 0.95);
  background: rgba(159, 176, 255, 0.10);
}

.sdx-window-step-event .sdx-chip {
  color: rgba(255, 196, 106, 0.95);
  background: rgba(255, 196, 106, 0.10);
}

.sdx-window-step-post .sdx-chip {
  color: rgba(78, 205, 196, 0.9);
  background: rgba(78, 205, 196, 0.09);
}

.sdx-window-block.animate-in .sdx-window-axis {
  animation: sdxDrawAxis 1.2s ease forwards;
}

.sdx-window-block.animate-in .sdx-window-pre {
  opacity: 1;
  animation: sdxGrowBand 1s ease 0.75s forwards;
}

.sdx-window-block.animate-in .sdx-window-event {
  opacity: 1;
  animation: sdxDrawEvent 0.75s ease 1.55s forwards;
}

.sdx-window-block.animate-in .sdx-window-post {
  opacity: 1;
  animation: sdxGrowBand 1s ease 2s forwards;
}

.sdx-window-block.animate-in .sdx-window-glow,
.sdx-window-block.animate-in .sdx-window-glow-soft {
  opacity: 1;
  animation: sdxPopGlow 0.8s ease 1.65s both;
}

.sdx-window-block.animate-in .sdx-window-label {
  animation: sdxFadeIn 0.7s ease 2.55s forwards;
}

.sdx-window-block.animate-in .sdx-window-step:nth-child(1) {
  animation: sdxPopStep 0.7s ease 2.9s forwards;
}

.sdx-window-block.animate-in .sdx-window-step:nth-child(2) {
  animation: sdxPopStep 0.7s ease 3.15s forwards;
}

.sdx-window-block.animate-in .sdx-window-step:nth-child(3) {
  animation: sdxPopStep 0.7s ease 3.4s forwards;
}

@keyframes sdxDrawAxis {
  to { stroke-dashoffset: 0; }
}

@keyframes sdxGrowBand {
  to { transform: scaleX(1); }
}

@keyframes sdxDrawEvent {
  to { stroke-dashoffset: 0; }
}

@keyframes sdxPopGlow {
  0% { transform: scale(0.85); }
  55% { transform: scale(1.08); }
  100% { transform: scale(1); }
}

@keyframes sdxFadeIn {
  to { opacity: 1; }
}

@keyframes sdxPopStep {
  to { opacity: 1; transform: none; }
}

@media (prefers-reduced-motion: reduce) {
  .sdx-window-axis,
  .sdx-window-event {
    stroke-dasharray: none;
    stroke-dashoffset: 0;
  }
  .sdx-window-pre,
  .sdx-window-post {
    opacity: 1;
    transform: none;
  }
  .sdx-window-label,
  .sdx-window-step {
    opacity: 1;
    transform: none;
    animation: none !important;
  }
}

.sdx-dual-panel {
  display: grid;
  grid-template-columns: minmax(0, 0.7fr) minmax(0, 0.3fr);
  gap: 1.25rem;
  margin-top: 1.2rem;
  align-items: start;
}

.sdx-dual-panel .sdx-chart-block {
  margin: 0;
}

.sdx-note {
  color: var(--muted);
  font-size: 0.9rem;
  margin-top: 0.8rem;
}

/* Scroll-triggered reveal animations */
[data-animate] {
  opacity: 0;
  transform: translateY(12px);
  transition: opacity 0.35s ease, transform 0.35s ease;
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

  .sdx-formula-grid {
    grid-template-columns: 1fr;
  }

  .sdx-step-grid {
    grid-template-columns: 1fr;
  }

  .sdx-case-grid {
    justify-content: stretch;
    margin-bottom: 1.25rem;
  }

  .sdx-case-grid .sdx-case-card {
    max-width: none;
  }

  .sdx-hero-media {
    min-height: 300px;
  }

  .sdx-section.alt {
    padding: 1.9rem;
    margin: 1.35rem 0;
  }

  .sdx-embed-grid {
    grid-template-columns: 1fr;
  }

  .sdx-window-steps {
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
          <h1 class="sdx-hero-title">Innovation Footprints in Tech Stock Markets</h1>
          <p class="sdx-hero-body"><em>Can Wall Street smell the future, or only read the headlines afterwards?</em></p>
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
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<section class="section sdx-section alt" id="prologue">
  <div class="container">
    <h2 class="title is-3">Prologue, The Problem with "Obvious" Innovation</h2>
    <div class="sdx-panel" data-animate="fade-up">
      <p>
        There's a peculiar comfort in hindsight. Standing in 2025, we can look back at the last two decades and
        confidently point to the moments that changed everything: the iPhone launch in 2007, the emergence of CUDA
        that made GPU computing possible, the mRNA vaccines that ended a pandemic, and ChatGPT's explosion onto the
        scene.
      </p>
      <p>
        These innovations feel almost predestined now, obvious turning points in the long arc of technological progress.
        But here's the uncomfortable truth that every investor, analyst, and curious observer must confront:
        <strong>on the day these innovations were announced, they didn't feel obvious at all.</strong>
      </p>
      <p>
        When Steve Jobs unveiled the iPhone, critics complained about the price tag and the lack of a physical keyboard.
        When NVIDIA released CUDA in 2007, it was a technical curiosity that most investors ignored entirely. When Tesla
        revealed the Cybertruck, the "unbreakable" windows shattered on live television and Twitter exploded with mockery.
        History's turning points, it seems, rarely announce themselves with fanfare.
      </p>
      <p>
        This creates a fascinating puzzle: if the stock market is supposed to be a forward-looking machine, pricing in
        future expectations, aggregating the wisdom of millions of investors, why does it so often miss the importance of
        transformative innovations?
      </p>
      <p>Or does it?</p>
      <p>
        Perhaps the market <em>does</em> recognize breakthrough innovations, just not in the way we expect. Perhaps the signal
        is there, hidden in the noise of daily price movements, waiting to be decoded by those patient enough to look.
      </p>
      <p>That's what this investigation is about.</p>
    </div>
    <div class="sdx-panel" data-animate="fade-up">
      <h3 class="title is-4" style="margin-top:0;">The Footprint Metaphor</h3>
      <p>
        Imagine innovation as an animal walking through fresh snow. If the animal is real, if it truly passed through, it should
        leave footprints. Traces. Evidence of its passage that a careful tracker can detect and follow.
      </p>
      <p>In financial markets, these footprints take specific forms:</p>
      <ul class="sdx-list">
        <li><strong>Sudden abnormal returns</strong>, moments when a stock moves far more than you'd expect based on normal market conditions.</li>
        <li><strong>Unusual trading volume</strong>, evidence that investors are paying attention and repositioning around the news.</li>
        <li><strong>Anticipation before the event</strong>, gradual drift in prices in the weeks before the announcement.</li>
        <li><strong>Long, slow-burning revaluation</strong>, weak day 0 reaction, followed by rising conviction over weeks.</li>
      </ul>
      <p>Our mission is to search for these footprints across two decades of innovation history.</p>
      <blockquote>
        <strong>When history happens, does the market react right away, or only once everyone knows it was history?</strong>
      </blockquote>
    </div>
    <div class="sdx-panel" data-animate="fade-up" markdown="1">

## A Timeline of Turning Points

Before we dive into the data, let's set the stage with the full scope of our investigation. We analyzed **42 innovation events** spanning two decades and five domains of human progress. These aren't just any product launches or press releases, they're moments that, in retrospect, fundamentally changed their industries.

  <div class="sdx-panel" style="margin: 2rem 0;" data-animate="fade-up">
<div class="flourish-embed flourish-timeline" data-src="visualisation/26798005"><script src="https://public.flourish.studio/resources/embed.js"></script><noscript><img src="https://public.flourish.studio/visualisation/26798005/thumbnail" width="100%" alt="timeline visualization" /></noscript></div>
</div>

The breadth of our investigation is intentional. Innovation takes many forms, and we wanted to understand whether the market recognizes different types of breakthroughs in different ways. A consumer gadget like the iPod is visible to everyone, millions saw the keynote, tried the product, formed opinions. But a computing platform like CUDA is invisible to most people, even as it quietly enables everything from video games to self-driving cars to ChatGPT.

| Domain            | Companies/Events                                                  | Time Period | Examples                                                      |
| ----------------- | ----------------------------------------------------------------- | ----------- | ------------------------------------------------------------- |
| Consumer Tech     | Apple (8 events)                                                  | 2001-2023   | iPod, iPhone, iPad, AirPods, M1 Chip, Vision Pro              |
| Compute Platforms | NVIDIA (8 events)                                                 | 2007-2024   | CUDA, DGX-1, V100, Blackwell B200                             |
| Electric Vehicles | Tesla (8 events)                                                  | 2014-2024   | Autopilot, Model 3, Cybertruck, FSD v12                       |
| Innovation Stack  | Top 25 market-cap leaders across the innovation stack (12 events) | 2006-2023   | S3, EUV, iPhone, Chrome, Azure, TensorFlow, LLaMA, Vision Pro |
| Healthcare        | Top 25 Healthcare Companies (10 events)                           | 2020-2024   | mRNA vaccines, GLP-1 drugs, CRISPR therapy                    |

Each event in this table represents a moment when _someone_ believed they were witnessing history. Our job is to determine whether Wall Street agreed, and when.

  </div>

  </div>
</section>

<section class="section sdx-section alt" id="cast">
  <div class="container">
    <h2 class="title is-3">Act I - Meet the Cast</h2>
    <div class="sdx-panel" data-animate="fade-up">
      <p>
        Innovation doesn't wear a single costume. It arrives in many forms, each with its own personality, its own audience,
        and its own relationship with the stock market. Before we can understand how markets recognize innovation, we need
        to understand the different types of innovation we're studying.
      </p>
      <p>
        Think of this chapter as meeting the characters in our story. Each company and sector brings something unique to our
        investigation. They come with different patterns of market recognition, different investor expectations, and
        different relationships between hype and substance.
      </p>
    </div>
    <div class="sdx-case-grid">
      <div class="sdx-case-card" data-animate="fade-up">
        <h3 class="title is-5">1. Consumer Tech (e.g., Apple)</h3>
        <p>
          The spotlight category. Highly visible launches where everyone has an opinion within hours.
        </p>
        <p class="sdx-note"><strong>Question:</strong> does visibility help the market understand, or just amplify noise?</p>
      </div>
      <div class="sdx-case-card" data-animate="fade-up">
        <h3 class="title is-5">2. Compute Platforms (e.g., NVIDIA)</h3>
        <p>
          Invisible infrastructure. Platforms most people never see, yet they power everything from AI to medicine.
        </p>
        <p class="sdx-note"><strong>Question:</strong> can markets price value that the public can't experience directly?</p>
      </div>
      <div class="sdx-case-card" data-animate="fade-up">
        <h3 class="title is-5">3. EVs &amp; Robotics (e.g., Tesla)</h3>
        <p>
          Innovation performed live. A mix of engineering, hype cycles, and very public execution risk.
        </p>
        <p class="sdx-note"><strong>Question:</strong> are investors pricing engineering, or belief?</p>
      </div>
      <div class="sdx-case-card" data-animate="fade-up">
        <h3 class="title is-5">4. AI Shockwaves (e.g., OpenAI, Google, Meta, Microsoft)</h3>
        <p>
          Ecosystem events. One breakthrough can rerate dozens of companies at once, even if the innovator isn't tradable.
        </p>
        <p class="sdx-note"><strong>Question:</strong> who captures the footprint when the "main" innovator isn't tradable?</p>
      </div>
      <div class="sdx-case-card" data-animate="fade-up">
        <h3 class="title is-5">5. Biotech &amp; Health (e.g., mRNA, GLP-1, CRISPR)</h3>
        <p>
          Innovation behind a regulatory gate. Uncertainty collapses when approval arrives.
        </p>
        <p class="sdx-note"><strong>Question:</strong> do binary "yes/no" moments create the cleanest footprints?</p>
      </div>
    </div>

    <div class="sdx-panel" data-animate="fade-up">
      <div class="content" markdown="1">

### 1. Consumer Tech, Apple: When Innovation Is Visible to Everyone

There's something almost theatrical about Apple product launches. The hushed anticipation as Tim Cook, or before him, Steve Jobs, walks onto a stage. The carefully choreographed "one more thing" moments. The live blogs updating second by second as journalists race to describe what they are seeing. Within hours, millions of people have formed opinions. Some are enthusiastic, some are skeptical, and many land somewhere in between.

Apple events are perhaps the most public innovations on Earth. They happen in broad daylight, under the glare of media attention. Financial analysts publish instant takes. Twitter erupts with hot takes and memes. The stock moves in real time as traders try to price in what they are seeing.

And yet, this visibility creates a paradox: **does being able to see an innovation clearly help the market understand it?**

Consider the skepticism that greeted some of Apple's most successful products. When the iPod launched in October 2001, Apple was struggling. The dot com bust had devastated tech stocks. The company was known for expensive computers that few people bought. And now they wanted $399 for an MP3 player, during a recession. The market's initial verdict was a yawn, or worse.

The iPhone faced similar skepticism. "No physical keyboard," critics complained. "$600 is too expensive for a phone." "It only works on AT&amp;T." These were not fringe opinions. They were mainstream analyst takes.

We analyzed **eight landmark Apple events** spanning 22 years to understand how markets process highly visible consumer innovation:

| Event                       | Date         | What It Was                    | The Skeptic's Take                              |
| --------------------------- | ------------ | ------------------------------ | ----------------------------------------------- |
| **iPod Launch**             | Oct 23, 2001 | "1,000 songs in your pocket"   | An overpriced MP3 player in a recession         |
| **iPhone Launch**           | Jun 29, 2007 | Phone + iPod + Internet device | Too expensive, no keyboard, carrier locked      |
| **iPad Launch**             | Apr 3, 2010  | A tablet computer              | Just a bigger iPod Touch, no laptop replacement |
| **iPhone 5S Touch ID**      | Sep 20, 2013 | Fingerprint authentication     | Nice feature, but not a selling point           |
| **Apple Pay Launch**        | Oct 20, 2014 | Tap to pay with your iPhone    | Too early, nobody will change how they pay      |
| **AirPods Launch**          | Dec 13, 2016 | Truly wireless earbuds         | They look ridiculous, easy to lose              |
| **M1 Chip Announcement**    | Nov 10, 2020 | Apple's own silicon            | Can they really beat Intel? Risky bet           |
| **Vision Pro Announcement** | Jun 5, 2023  | Spatial computing headset      | $3,500, no killer app, VR has failed before     |

Notice the pattern? The market, the media, and often the public were skeptical on day one. The iPhone was "overpriced." The AirPods looked "weird." The M1 seemed like a dangerous bet against decades of Intel partnership.

What makes Apple's story particularly instructive is that we know how it ends. These doubts turned into successes. The "overpriced" iPhone generated more revenue than any product in human history. The "weird" AirPods created an entirely new product category. Apple Silicon delivered exactly what Apple promised.

So the question for our investigation becomes: **did the stock market share the skeptic's doubts, or did it see through the noise to recognize value?**

</div>
    </div>

    <div class="sdx-panel" data-animate="fade-up">
      <div class="content" markdown="1">

### 2. Compute Platforms, NVIDIA: Innovation Beneath the Surface

If Apple innovations happen in the spotlight, NVIDIA innovations happen in the shadows, invisible to most people, yet profoundly shaping the technology they use every day.

Consider this: when you ask ChatGPT a question, you are using NVIDIA hardware. When a Tesla navigates traffic using Autopilot, NVIDIA chips process the camera feeds. When a hospital uses AI to detect tumors in medical images, NVIDIA GPUs do the heavy lifting. The company's technology is everywhere, and yet most people have never thought about it.

This creates a fascinating market puzzle. **How do investors price innovations that most people can't see, touch, or directly experience?**

NVIDIA's story spans three distinct eras. In the early 2000s, it was a gaming company, a maker of graphics cards that rendered video game worlds in ever more realistic detail. In the 2010s, it became a deep learning company, its GPUs turned out to be unexpectedly perfect for training neural networks. In the 2020s, it became the AI company, the essential infrastructure provider for the entire artificial intelligence revolution.

Each transition was driven by specific product launches and platform innovations. We analyzed **eight NVIDIA milestones** that marked these pivotal moments:

| Event                       | Date         | The Innovation                     | Why It Mattered (In Hindsight)                      |
| --------------------------- | ------------ | ---------------------------------- | --------------------------------------------------- |
| **CUDA Launch**             | Jun 23, 2007 | GPU computing becomes programmable | Enabled the deep learning revolution a decade later |
| **DGX-1 Launch**            | Apr 5, 2016  | Deep learning system in a box      | Turned NVIDIA GPUs into an AI platform              |
| **Tesla V100 Launch**       | May 10, 2017 | First Tensor Cores for AI          | Purpose built AI hardware changes the game          |
| **RTX 2080 Ti Launch**      | Aug 20, 2018 | Real time ray tracing              | New visual computing paradigm for games and beyond  |
| **A100 Ampere Launch**      | May 14, 2020 | 20x AI performance leap            | The engine that would power ChatGPT training        |
| **Arm Acquisition Attempt** | Sep 13, 2020 | $40B semiconductor empire bid      | Audacious reach for chip industry dominance         |
| **H100 Hopper Launch**      | Mar 22, 2022 | The AI training workhorse          | Every AI lab in the world would want these          |
| **Blackwell B200**          | Mar 18, 2024 | 208 billion transistor monster     | Next generation of AI infrastructure                |

The CUDA story is particularly instructive. In June 2007, NVIDIA announced that programmers could now write general purpose code that would run on graphics cards. At the time, this seemed like a niche feature, interesting to researchers, perhaps, but hardly earth shattering for the gaming focused company.

Nobody imagined that this technical capability would become the foundation of modern artificial intelligence. Nobody foresaw that CUDA would power the training of AlexNet in 2012, igniting the deep learning revolution. Nobody predicted that a decade later, the entire AI industry would depend on NVIDIA hardware.

**Did the market see it coming? Did anyone?** That's what we set out to discover.

</div>
    </div>

    <div class="sdx-panel" data-animate="fade-up">
      <div class="content" markdown="1">

### 3. Electric Vehicles and Robotics, Tesla: Innovation Performed Live

Tesla exists in a category entirely its own. It's not just a car company. It's a narrative, a movement, a perpetual drama that plays out on social media, in stock trading apps, and on stages designed for maximum impact.

When Elon Musk walks onto a Tesla stage, he's not just announcing a product. He's putting on a show. And sometimes the show goes spectacularly wrong, like when the "unbreakable" Cybertruck windows shattered on live television, sending social media into a frenzy and creating one of the most memorable product demonstration failures in corporate history.

But here's the thing: **the Cybertruck reveal, despite the broken windows, generated over 200,000 reservations in less than 48 hours.** The spectacle worked, even when it failed.

This creates unique challenges for understanding market recognition. With Apple or NVIDIA, we're analyzing how markets respond to technology. With Tesla, we're analyzing how markets respond to theater, and trying to separate genuine innovation recognition from hype cycles, cult of personality effects, and meme stock dynamics.

We analyzed **eight Tesla moments** that capture this unique dynamic:

| Event                           | Date         | The Story                      | The Drama                           |
| ------------------------------- | ------------ | ------------------------------ | ----------------------------------- |
| **Autopilot Announcement**      | Oct 10, 2014 | Autopilot hardware announced   | Suddenly competing with Google      |
| **Model 3 First Deliveries**    | Jul 28, 2017 | First Model 3 deliveries begin | "Production hell" nightmares start  |
| **Cybertruck Reveal**           | Nov 21, 2019 | Electric truck unveiled        | Broken windows, polarized reactions |
| **Tesla Bot Announcement**      | Aug 19, 2021 | Optimus revealed at AI Day     | Dancing human in robot costume      |
| **Dojo Supercomputer**          | Aug 19, 2021 | Dojo unveiled at AI Day        | Tesla wants its own AI factory      |
| **Cybertruck Deliveries Begin** | Nov 30, 2023 | First Cybertruck deliveries    | Four years of waiting ends          |
| **Optimus Gen 2 Reveal**        | Dec 13, 2023 | Second gen Optimus update      | Better demo, timeline still unclear |
| **FSD v12 Wide Rollout**        | Mar 16, 2024 | End to end neural FSD rollout  | Autonomy meets reality              |

Tesla's relationship with expectations is complicated. The Model 3 deliveries proved the product was real, but they also triggered the harder question, can Tesla scale without breaking? The Cybertruck reveal went viral for the wrong reasons and still created demand. At AI Day, Tesla unveiled both Optimus and Dojo, two bets that pushed the story beyond cars and into robots and compute.

The Tesla Bot announcement perfectly encapsulates the company's unique position. Elon Musk announced that Tesla would build humanoid robots to perform dangerous or boring tasks. The company's credentials, experience with AI, sensors, motors, manufacturing, made the idea at least plausible. But the presentation featured a human dancer in a robot costume, inviting mockery. Was this visionary innovation or tech hype theater?

The later updates, Optimus Gen 2 and the FSD v12 rollout, show the same pattern at a different intensity. Each step forward is real, but the market keeps asking whether the timeline is finally catching up to the story.

**When spectacle and substance blur together, how does the market respond?** Tesla gives us the perfect laboratory to find out.

</div>
    </div>

    <div class="sdx-panel" data-animate="fade-up">
      <div class="content" markdown="1">

### 4. Innovation Stack Shockwaves, When One Innovation Moves Everything

Some innovation footprints do not belong to one company. They belong to a stack.

When a platform shift happens, the market does not move one ticker. It reprices a web of suppliers, customers, competitors, and complements.

That is why this project includes a different kind of case file, a basket view of the innovation stack. Instead of tracking one stock, we track a basket of the **25 largest, most liquid market-cap leaders** across semiconductors, cloud, platforms, and enterprise software, and we ask a wider question.

When the stack is hit by a turning point, do stocks move together, or does the market split into winners and losers?

We anchored this lens around **twelve turning point innovations** that moved multiple companies at once:

| Event                              | Date         | What Happened                              | Expected Beneficiaries  |
| ---------------------------------- | ------------ | ------------------------------------------ | ----------------------- |
| **Amazon S3 Launch**               | Mar 14, 2006 | Cloud storage becomes a utility            | AMZN, MSFT, GOOGL, ORCL |
| **ASML First EUV Tools**           | Aug 29, 2006 | EUV lithography enables leading edge chips | ASML, TSM, INTC, NVDA   |
| **iPhone Launch**                  | Jun 29, 2007 | Mobile computing goes mainstream           | AAPL, QCOM, TSM, AVGO   |
| **Google Chrome Beta Launch**      | Sep 2, 2008  | The modern web runtime arrives             | GOOGL, MSFT, AAPL, META |
| **Microsoft Azure Launch**         | Feb 1, 2010  | Cloud becomes enterprise default           | MSFT, AMZN, GOOGL, ORCL |
| **iPhone 5S Touch ID**             | Sep 20, 2013 | Biometrics becomes default UX              | AAPL, QCOM, TSM, AVGO   |
| **TensorFlow Open Sourced**        | Nov 9, 2015  | AI tooling becomes a platform              | GOOGL, NVDA, AMD, MSFT  |
| **Armv9 Architecture Introduced**  | Mar 30, 2021 | Next gen CPU era, security plus efficiency | ARM, AAPL, QCOM, TSM    |
| **Meta LLaMA Release**             | Feb 24, 2023 | Open source LLM shockwave                  | META, NVDA, AMD, GOOGL  |
| **GPT-4 Release**                  | Mar 14, 2023 | Capability leap accelerates AI adoption    | MSFT, NVDA, GOOGL, META |
| **Microsoft Copilot Announcement** | Mar 16, 2023 | Enterprise AI goes mainstream              | MSFT, NVDA, CRM, ORCL   |
| **Vision Pro Announcement**        | Jun 5, 2023  | Spatial computing arrives                  | AAPL, TSM, QCOM, AVGO   |

<div class="flourish-embed flourish-cards" data-src="visualisation/26799327">
  <script src="https://public.flourish.studio/resources/embed.js"></script>
  <noscript><img src="https://public.flourish.studio/visualisation/26799327/thumbnail" width="100%" alt="cards visualization" /></noscript>
</div>

The choice to analyze 25 market-cap leaders, rather than focusing on obvious winners like NVIDIA or Apple, was deliberate. We wanted to answer a more nuanced question: when a turning point hits the stack, does value concentrate in a few winners, or spread broadly across the ecosystem?

The "winner ratio", the percentage of companies that end up with positive returns 30 days after an event, became our key metric. A high winner ratio suggests a broad repricing across the stack. A low winner ratio suggests a selective move, a few winners and many laggards.

</div>
    </div>

    <div class="sdx-panel" data-animate="fade-up">
      <div class="content" markdown="1">

### 5. Biotech and Healthcare, Innovation With a Regulatory Gate

Healthcare innovations operate under rules fundamentally different from anything in technology. When Apple announces an iPhone, customers can buy it within weeks. When NVIDIA launches a GPU, data centers can order them immediately. The path from announcement to adoption is relatively smooth.

In healthcare, a massive gate stands between announcement and reality: **regulatory approval.**

Consider the journey of a new drug. A pharmaceutical company might announce promising trial results, but that drug won't help any patients until the FDA, or equivalent regulators elsewhere, grants approval. That approval might come quickly, or it might take years. It might come with conditions, or it might not come at all. The uncertainty is enormous.

This creates something unique in markets: **binary events with massive stakes.** The day an FDA approval is announced, a treatment goes from "might work" to "will work" in a single moment. Uncertainty collapses. Billions of dollars in value can be created or destroyed overnight.

The COVID 19 pandemic brought this dynamic into sharp focus. On December 11, 2020, the FDA granted emergency use authorization to Pfizer BioNTech's Comirnaty vaccine, the first mRNA vaccine ever approved for human use. It wasn't just a drug approval. It was validation of an entirely new platform technology that had been in development for decades.

We analyzed **ten healthcare breakthroughs** that represent different types of medical innovation:

**Drug and Treatment Innovations:**

| Event                              | Date         | The Stakes                    | The Promise                            |
| ---------------------------------- | ------------ | ----------------------------- | -------------------------------------- |
| **First mRNA Vaccine (Comirnaty)** | Dec 11, 2020 | Revolutionary platform        | New way to build vaccines forever      |
| **Wegovy GLP 1 Weight Loss**       | Jun 4, 2021  | Obesity treatment             | First true weight loss drug            |
| **Paxlovid Oral Antiviral**        | Dec 22, 2021 | At home treatment             | Turn COVID into a manageable disease   |
| **Mounjaro (Tirzepatide)**         | May 13, 2022 | Diabetes breakthrough         | Dual hormone approach changes outcomes |
| **Leqembi Alzheimer's Approval**   | Jan 6, 2023  | First disease slowing drug    | Proof Alzheimer's can be treated       |
| **Zepbound Obesity Launch**        | Nov 8, 2023  | Massive blockbuster potential | GLP 1 competition accelerates          |
| **Casgevy CRISPR Therapy**         | Dec 8, 2023  | Gene editing becomes real     | Cure genetic diseases at the source    |

**Technology and AI Innovations:**

| Event                         | Date         | The Stakes               | The Promise                            |
| ----------------------------- | ------------ | ------------------------ | -------------------------------------- |
| **AlphaFold 2 Breakthrough**  | Nov 30, 2020 | Protein folding solved   | Accelerate drug discovery dramatically |
| **GPT 4 Medical AI Release**  | Mar 14, 2023 | Medical AI advances      | Better diagnosis and imaging analysis  |
| **Da Vinci 5 Surgical Robot** | Mar 14, 2024 | Next gen robotic surgery | Precision surgery advances             |

<div class="flourish-embed flourish-cards" data-src="visualisation/26830826">
  <script src="https://public.flourish.studio/resources/embed.js"></script>
  <noscript><img src="https://public.flourish.studio/visualisation/26830826/thumbnail" width="100%" alt="cards visualization" /></noscript>
</div>

The GLP 1 story is particularly remarkable. Drugs like Wegovy and Mounjaro haven't just helped diabetics control their blood sugar. They've produced unprecedented weight loss in clinical trials. This has created ripple effects far beyond the pharmaceutical companies making them. Food companies have seen their stocks affected. Weight Watchers restructured its business. Fitness chains adjusted their projections. Medical device companies serving obese patients reconsidered their futures.

**Healthcare gives us something tech rarely provides: clean, binary moments where we can measure market recognition with precision.** When the FDA says yes, there's no ambiguity. The footprint should be unmistakable.

</div>
    </div>
  </div>
</section>

<section class="section sdx-section alt" id="method">
  <div class="container">
    <h2 class="title is-3">Act II - The Detective Method</h2>

    <div class="sdx-panel" data-animate="fade-up">
      <h3 class="title is-4" style="margin-top:0;">The Event Study Method</h3>
      <p>
        We've met our cast of innovations. Now we need a way to detect, and measure, their footprints in market data.
        In finance, the standard tool for this is an <strong>event study</strong>.
      </p>
      <p>
        Looking at the event day alone is not enough. Stocks move for countless reasons, market drift, macro surprises,
        competitor news. An event study focuses on the window around an announcement to separate signal from noise.
      </p>
      <p><strong>We run the same three-step workflow for every domain:</strong></p>

      <div class="sdx-step-grid">
        <div class="sdx-step-card" data-animate="fade-up">
          <div class="sdx-step-head">
            <div class="sdx-step-num">1</div>
            <h4 class="title is-5">Pin the event day</h4>
          </div>
          <p>
            Define the innovation date. If it lands on a weekend or holiday, shift to the next trading day.
          </p>
        </div>
        <div class="sdx-step-card" data-animate="fade-up">
          <div class="sdx-step-head">
            <div class="sdx-step-num">2</div>
            <h4 class="title is-5">Extract a window</h4>
          </div>
          <p>
            Pull price and volume for 30 trading days before and after, so we can see anticipation, reaction, and digestion.
          </p>
        </div>
        <div class="sdx-step-card" data-animate="fade-up">
          <div class="sdx-step-head">
            <div class="sdx-step-num">3</div>
            <h4 class="title is-5">Measure the footprint</h4>
          </div>
          <p>
            Compute returns, cumulative returns, volatility, and volume changes, then compare pre vs post behavior.
          </p>
        </div>
      </div>

      <p class="sdx-note">
        We reuse the same pipeline across domains. Only the ticker list and event calendar change.
      </p>
    </div>

    <div class="sdx-chart-block sdx-window-block" data-animate="fade-up" id="event-window-diagram">
      <h3 class="title is-4" style="margin-top:0;">Event window, 61 trading days</h3>
      <p class="sdx-note" style="margin-top:0.6rem;">
        We center each event at <strong>t = 0</strong>, then watch 30 trading days before and after to separate anticipation, reaction, and digestion.
      </p>

      <div class="sdx-window-visual">
        <svg class="sdx-window-svg" viewBox="0 0 920 220" role="img" aria-label="Event window diagram with pre-event, event day, and post-event segments">
          <defs>
            <linearGradient id="sdxAxisGlow" x1="0" x2="1" y1="0" y2="0">
              <stop offset="0%" stop-color="rgb(159,176,255)" stop-opacity="0"></stop>
              <stop offset="50%" stop-color="rgb(159,176,255)" stop-opacity="0.18"></stop>
              <stop offset="100%" stop-color="rgb(78,205,196)" stop-opacity="0"></stop>
            </linearGradient>
          </defs>

          <rect x="86" y="92" width="330" height="36" rx="14" class="sdx-window-pre"></rect>
          <rect x="504" y="92" width="330" height="36" rx="14" class="sdx-window-post"></rect>

          <line x1="86" y1="110" x2="834" y2="110" class="sdx-window-axis"></line>
          <line x1="86" y1="110" x2="834" y2="110" stroke="url(#sdxAxisGlow)" stroke-width="10" opacity="0.35"></line>

          <line x1="460" y1="62" x2="460" y2="158" class="sdx-window-event"></line>
          <circle cx="460" cy="110" r="18" class="sdx-window-glow-soft"></circle>
          <circle cx="460" cy="110" r="6" class="sdx-window-glow"></circle>

          <line x1="86" y1="110" x2="86" y2="140" class="sdx-window-tick"></line>
          <line x1="273" y1="110" x2="273" y2="140" class="sdx-window-tick"></line>
          <line x1="460" y1="110" x2="460" y2="140" class="sdx-window-tick"></line>
          <line x1="647" y1="110" x2="647" y2="140" class="sdx-window-tick"></line>
          <line x1="834" y1="110" x2="834" y2="140" class="sdx-window-tick"></line>

          <text x="86" y="168" text-anchor="middle" class="sdx-window-label">-30</text>
          <text x="273" y="168" text-anchor="middle" class="sdx-window-label">-15</text>
          <text x="460" y="168" text-anchor="middle" class="sdx-window-label">0</text>
          <text x="647" y="168" text-anchor="middle" class="sdx-window-label">+15</text>
          <text x="834" y="168" text-anchor="middle" class="sdx-window-label">+30</text>

          <text x="251" y="78" text-anchor="middle" class="sdx-window-label sdx-window-label-muted">Pre event</text>
          <text x="460" y="46" text-anchor="middle" class="sdx-window-label sdx-window-label-muted">Event day</text>
          <text x="669" y="78" text-anchor="middle" class="sdx-window-label sdx-window-label-muted">Post event</text>
        </svg>

        <div class="sdx-window-steps">
          <div class="sdx-window-step sdx-window-step-pre">
            <div class="sdx-chip">t = -30 to -1</div>
            <h4>Pre-event</h4>
            <p>Positioning, leaks, and anticipation drift if investors expected the news.</p>
          </div>
          <div class="sdx-window-step sdx-window-step-event">
            <div class="sdx-chip">t = 0</div>
            <h4>Event day</h4>
            <p>Headlines hit, the first repricing shows up in returns, volume, and volatility.</p>
          </div>
          <div class="sdx-window-step sdx-window-step-post">
            <div class="sdx-chip">t = +1 to +30</div>
            <h4>Post-event</h4>
            <p>Digestion phase, does the move stick, reverse, or slowly build after the story spreads.</p>
          </div>
        </div>
      </div>
    </div>

    <div class="sdx-panel sdx-formula-block" data-animate="fade-up" style="margin: 2rem 0;">
      <h3 class="title is-4" style="margin-top:0;">Key formulas, the footprint checklist</h3>
      <p>
        These are the metrics we compute for every event window today. The panel below expands the same ideas with examples.
      </p>

      <h4 class="title is-5" style="margin-top:1.2rem;">Core metrics</h4>
      <div class="sdx-formula-grid sdx-formula-grid-core">
        <div class="sdx-formula-card">
          <h4>Return</h4>
          <div class="formula">\( R_t = \left(\frac{P_t}{P_{t-1}} - 1\right) \times 100 \)</div>
          <p>The daily percentage move, the basic unit behind every footprint.</p>
        </div>
        <div class="sdx-formula-card">
          <h4>Log return</h4>
          <div class="formula">\( r_t = \ln\!\left(\frac{P_t}{P_{t-1}}\right) \times 100 \)</div>
          <p>A return measure that stacks cleanly across days, useful for long windows.</p>
        </div>
        <div class="sdx-formula-card">
          <h4>Cumulative return</h4>
          <div class="formula">\( CR_t = \left(\frac{P_t}{P_0} - 1\right) \times 100 \)</div>
          <p>The buy-and-hold story inside the window: buy on event day and hold for t days.</p>
        </div>
        <div class="sdx-formula-card">
          <h4>Volatility</h4>
          <div class="formula">\( \sigma = \sqrt{\mathrm{Var}(R_t)} \)</div>
          <p>Uncertainty proxy. Breakthroughs can increase volatility, or reduce it once uncertainty collapses.</p>
        </div>
        <div class="sdx-formula-card">
          <h4>Volume change</h4>
          <div class="formula">\( VC = \left(\frac{\bar{V}_{post}}{\bar{V}_{pre}} - 1\right) \times 100 \)</div>
          <p>Attention proxy, average volume after vs before, expressed as a percentage.</p>
        </div>
      </div>


      </div>
    </div>

    <div class="sdx-panel" data-animate="fade-up">
      <div class="content" markdown="1">

### The Mathematics of Market Footprints

The checklist above is the compact version. This panel shows the exact math we compute in code, with plain-language interpretation.

#### 1) Return and log return

$$R_t = \left(\frac{P_t - P_{t-1}}{P_{t-1}}\right) \times 100$$

Daily return is the percentage move from yesterday's close $$P_{t-1}$$ to today's close $$P_t$$.

Log return is a closely related measure that adds cleanly across time:

$$r_t = \ln\!\left(\frac{P_t}{P_{t-1}}\right) \times 100$$

Example: if a stock closed at $150 yesterday and closes at $153 today, the daily return is:

$$\frac{153 - 150}{150} \times 100 = 2\%$$

#### 2) Planned extension, abnormal return and CAR

To isolate the event from the market's noise, we can add a market-adjusted baseline (next upgrade on our roadmap):

$$AR_t = R_t - R_{m,t}$$

Here $$R_{m,t}$$ is the benchmark return (a broad market index) on the same day.
We then sum abnormal returns across a window to get cumulative abnormal return:

$$CAR_{[a,b]} = \sum_{t=a}^{b} AR_t$$

Interpretation: positive CAR means the stock outperformed the market across the window, negative CAR means it underperformed.

#### 3) Cumulative return (simple buy-and-hold)

Sometimes the cleanest story is also the simplest: buy on event day and hold.

$$CR_t = \left(\frac{P_t}{P_0} - 1\right) \times 100$$

#### 4) Volatility, how uncertain was the market?

Volatility measures how wildly returns jump around. High volatility means investors disagree, so prices swing dramatically from day to day.

$$\sigma = \sqrt{\frac{1}{n-1}\sum_{i=1}^{n}(R_i - \bar{R})^2}$$

For innovation, volatility can spike on surprise, then fall once uncertainty resolves through price discovery.

#### 5) Volume change, how much attention did it get?

Trading volume measures attention. When something important happens, more investors trade. They buy if they are excited, sell if they are skeptical, and reposition either way.

$$VC = \left(\frac{\bar{V}_{post}}{\bar{V}_{pre}} - 1\right) \times 100$$

In plain English: compare average volume after the event $$\bar{V}_{post}$$ to average volume before $$\bar{V}_{pre}$$, expressed as a percentage.

Interpretation: high volume plus positive returns suggests informed enthusiasm. High volume plus negative returns can indicate informed concern, or messy disagreement.

</div>
    </div>

    <div class="sdx-panel" data-animate="fade-up">
      <h3 class="title is-4" style="margin-top:0;">From One Company to Many</h3>
      <p>
        Single-stock event studies make sense for Apple, NVIDIA, and Tesla. For ecosystem shocks like ChatGPT, the point is not
        one ticker. It is the <em>breadth</em> of the reaction.
      </p>
      <p>
        For AI and healthcare events, we track multiple companies simultaneously and measure how many finish the window
        positive, the <strong>Winner Ratio</strong>:
      </p>
      <p class="sdx-note" id="winner-ratio-definition">\( \text{Winner Ratio} = \frac{\text{Number of companies with positive 30-day return}}{\text{Total companies}} \times 100 \)</p>
      <p class="sdx-note">High winner ratio = broad transformation; low winner ratio = selective winners and losers.</p>

  </div>
</section>

<section class="section sdx-section alt" id="case-files">
  <div class="container">
    <h2 class="title is-3">Act III - Case Files Across the Innovation Landscape</h2>
    <div class="sdx-panel" data-animate="fade-up" markdown="1">
The stage is set. You understand our method. Now comes the exciting part: **what did we actually find?**

Rather than marching through companies one by one, we've organized our findings by **what they teach us about market recognition.** Each chapter that follows reveals a different facet of how markets process innovation, and each tells a story that challenges conventional wisdom about the efficiency of financial markets.

</div>

    <div class="sdx-panel" id="chapter-apple" data-animate="fade-up">
      <h2 class="title is-4">Chapter 1 - Apple: The Slow Recognition of Visible Innovation</h2>
      <div class="sdx-chapter-hero sdx-chapter-hero--top" aria-hidden="true">
        <img
          class="sdx-chapter-hero-img"
          src="{{ '/assets/images/Apples-New-AI-Revolution-Why-Apple-Intelligence-Could-Change-Everything-scaled.webp' | relative_url }}"
          alt=""
          loading="lazy"
          decoding="async"
        />
        <div class="sdx-chapter-hero-caption">
          <span class="sdx-chapter-hero-kicker">Chapter 1</span>
          <span class="sdx-chapter-hero-title">Apple Intelligence</span>
        </div>
      </div>
      <div class="content" markdown="1">

Apple's innovations are the most watched, most analyzed, most debated product launches on Earth. Millions tune in to keynotes. Thousands of articles appear within hours. Every financial analyst in tech has an opinion.

And yet, perhaps _because_ of all this attention, Apple innovations reveal something profound about how markets process information: **visibility doesn't guarantee understanding.**

---

### The iPod Paradox (October 23, 2001)

Picture the scene: October 2001. The dot-com bubble has burst. The tech industry is in shambles. Apple is a struggling computer company with a cult following but shrinking market share. Into this gloom, Steve Jobs walks onto a stage and announces... an MP3 player.

"1,000 songs in your pocket," he proclaimed, unveiling the iPod. Price tag: $399. In a recession. For a music player, when you could buy a Sony Walkman for $50.

The market's verdict on announcement day was clear: **Apple stock fell 4.63%.**

Wall Street saw an overpriced gadget. Analysts questioned whether anyone would pay $399 for a device that played music. The skeptics made compelling arguments: MP3 players already existed, Apple had no experience in consumer electronics beyond computers, and the economy was terrible.

But then something remarkable happened. Over the next 30 days, as people actually saw the iPod, as the elegance of the click wheel and the iTunes integration became clear, the market quietly changed its mind.

**30-day cumulative return: +30.98%**

<div class="sdx-embed-block">
  <div class="sdx-embed-card" data-animate="fade-up">
    <div class="sdx-embed-head">
      <h4 class="sdx-embed-title">iPod Launch</h4>
      <span class="sdx-embed-kicker">Interactive window</span>
    </div>
    <div class="sdx-embed-body">
      <iframe
        class="sdx-embed-iframe"
        src="{{ '/assets/apple_event_exports/ipod_launch_plotly_dark.html' | relative_url }}"
        title="iPod Launch innovation footprint explorer"
        loading="lazy"
      ></iframe>
    </div>
  </div>
</div>

The iPod story is the perfect example of what we call the **"Slow Burn"** pattern, an innovation that looks unremarkable on day one but proves transformative over time. The market's initial skepticism wasn't irrational; it was based on reasonable concerns about price and competition. But as more information emerged, early reviews, initial sales figures, the experience of actually using the device, the market gradually recognized what it had missed.

The iPod wasn't just a music player. It was Apple's entry into consumer electronics, the first step in a journey that would lead to the iPhone, the iPad, and Apple's transformation into the most valuable company on Earth. But on October 23, 2001, that future was invisible to almost everyone, including, seemingly, Wall Street.

---

### The iPhone: A Revolution Hiding in Plain Sight

If any product launch should have produced an instant footprint, it was the iPhone. Steve Jobs called it "a revolutionary product that changes everything." He unveiled it on January 9, 2007, and for the next six months, the tech world debated whether he was right.

The critics had plenty of ammunition:

- "No physical keyboard. How can you type on glass? BlackBerry will crush this."
- "$600 is absurd for a phone. Most phones are free with contract."
- "Exclusive to Cingular? In the US only? This limits the market dramatically."

Microsoft's CEO Steve Ballmer famously laughed at the iPhone on television: "$500? Fully subsidized? With a plan? That is the most expensive phone in the world!"

On launch day, June 29, 2007, Apple's stock rose a modest **1.23%**. Respectable, but hardly earth-shattering for what would become the most successful product in consumer technology history.

The 30-day cumulative return? **+4.71%**. Decent, but not revolutionary.

<div class="sdx-embed-block">
  <div class="sdx-embed-card" data-animate="fade-up">
    <div class="sdx-embed-head">
      <h4 class="sdx-embed-title">iPhone Launch</h4>
      <span class="sdx-embed-kicker">Interactive window</span>
    </div>
    <div class="sdx-embed-body">
      <iframe
        class="sdx-embed-iframe"
        src="{{ '/assets/apple_event_exports/iphone_launch_plotly_detailed.html' | relative_url }}"
        title="iPod Launch innovation footprint explorer"
        loading="lazy"
      ></iframe>
    </div>
  </div>
</div>

Why didn't the market immediately recognize what the iPhone would become? The answer reveals something important about innovation: **the iPhone we know today is not the iPhone that launched in 2007.**

The original iPhone had no App Store. No third-party apps. No copy-paste. No GPS navigation. It was, essentially, a very pretty phone that could browse the web and play music. Revolutionary? Perhaps. But the _transformative_ part, the App Store, the ecosystem, the platform, didn't exist yet.

The market's moderate response wasn't wrong, exactly. It was pricing what it could see, not what would come. The iPhone's true footprint would take years to fully materialize.

---

### The M1 Chip: When Platform Shifts Get Noticed

Not all Apple innovations follow the slow-burn pattern. The M1 chip announcement in November 2020 tells a different story, one of almost immediate recognition.

For 15 years, Apple had built its Mac computers around Intel processors. The switch to Intel in 2006 had been a major strategic decision, and the partnership seemed stable. Then, at WWDC 2020, Apple announced it was leaving Intel behind entirely, building its own processors for Mac, the same approach it had pioneered with the iPhone and iPad.

This was risky. Intel chips were the industry standard. Countless software applications were optimized for Intel architecture. Developers would need to rewrite their code. The transition could have been a disaster.

On announcement day (November 10, 2020), Apple's stock barely moved: **-0.30%**. The market wasn't sure what to make of the news.

But as the M1's performance benchmarks leaked out, dramatically outperforming Intel while using a fraction of the power, the market started to pay attention. And as reviewers got their hands on M1 Macs and confirmed the remarkable performance, conviction grew.

**30-day cumulative return: +12.93%**

<div class="sdx-embed-block">
  <div class="sdx-embed-card" data-animate="fade-up">
    <div class="sdx-embed-head">
      <h4 class="sdx-embed-title">M1 Chip Annoucement</h4>
      <span class="sdx-embed-kicker">Interactive window</span>
    </div>
    <div class="sdx-embed-body">
      <iframe
        class="sdx-embed-iframe"
        src="{{ '/assets/apple_event_exports/m1_chip_announcement_plotly_detailed.html' | relative_url }}"
        title="iPod Launch innovation footprint explorer"
        loading="lazy"
      ></iframe>
    </div>
  </div>
</div>

The M1 story shows that markets _can_ recognize platform shifts, it just takes time for the implications to sink in. The event-day return was essentially zero. But over the following month, as investors digested what Apple Silicon meant for margins, performance, and competitive positioning, a substantial revaluation occurred.

---

### Apple Event Summary: All 8 Events Compared

When we step back and look at all eight Apple events together, a striking pattern emerges:

<div class="sdx-embed-block">
  <div class="sdx-embed-stack">
    <div class="sdx-embed-card" data-animate="fade-up">
      <div class="sdx-embed-head">
        <h4 class="sdx-embed-title">Apple: Cumulative returns</h4>
        <span class="sdx-embed-kicker">Interactive window</span>
      </div>
      <div class="sdx-embed-body">
        <iframe
          class="sdx-embed-iframe"
          src="assets/apple_event_exports/apple_cumulative_returns_interactive.html"
          title="Apple cumulative returns explorer"
          loading="lazy"
        ></iframe>
      </div>
    </div>

    <div class="sdx-embed-card" data-animate="fade-up">
      <div class="sdx-embed-head">
        <h4 class="sdx-embed-title">Apple: Day 0 vs 30-day returns</h4>
        <span class="sdx-embed-kicker">Interactive window</span>
      </div>
      <div class="sdx-embed-body">
        <iframe
          class="sdx-embed-iframe"
          src="assets/apple_event_exports/apple_plotly_05_30day_cumulative_returns.html"
          title="Apple day 0 vs 30-day returns explorer"
          loading="lazy"
          data-sdx-height="600"
        ></iframe>
      </div>
    </div>

  </div>
</div>

| Event              | Day-0 Return | 30-Day Return | The Pattern                      |
| ------------------ | ------------ | ------------- | -------------------------------- |
| iPod Launch        | -4.63%       | +30.98%       | Classic slow burn                |
| iPhone Launch      | +1.23%       | +4.71%        | Muted, waiting for App Store     |
| iPad Launch        | +1.07%       | +6.60%        | Quiet, steady adoption           |
| iPhone 5S Touch ID | -1.04%       | +11.26%       | Security innovation rewarded     |
| Apple Pay Launch   | +2.14%       | +15.40%       | Services flywheel gets priced in |
| AirPods Launch     | +1.67%       | +5.87%        | Surprise hit                     |
| M1 Chip            | -0.30%       | +12.93%       | Platform shift recognized        |
| Vision Pro         | -0.76%       | +8.64%        | Spatial computing bet            |

**The key insight:** For Apple, **event-day returns are nearly useless** for predicting 30-day outcomes. The iPod dropped 4.6% on announcement day but became Apple's turnaround story. The correlation between day-0 and 30-day returns is essentially zero.

This tells us something profound about consumer innovation: **the market's first reaction is often noise.** The signal emerges over weeks, not hours.

<div class="sdx-embed-block">
  <div class="sdx-embed-card" data-animate="fade-up">
    <div class="flourish-embed flourish-chart" data-src="visualisation/26748328"><script src="https://public.flourish.studio/resources/embed.js"></script><noscript><img src="https://public.flourish.studio/visualisation/26748328/thumbnail" width="100%" alt="chart visualization" /></noscript></div>
  </div>
</div>

</div>
    </div>

    <div class="sdx-panel" id="chapter-nvidia" data-animate="fade-up">
      <h2 class="title is-4">Chapter 2 - NVIDIA: The Infrastructure Play</h2>
      <div class="sdx-chapter-hero" aria-hidden="true">
        <img
          class="sdx-chapter-hero-img"
          src="{{ '/assets/images/nvidia_1651928213.webp' | relative_url }}"
          alt=""
          loading="lazy"
          decoding="async"
        />
        <div class="sdx-chapter-hero-caption">
          <span class="sdx-chapter-hero-kicker">Chapter 2</span>
          <span class="sdx-chapter-hero-title">NVIDIA Compute Stack</span>
        </div>
      </div>
      <div class="content" markdown="1">

If Apple represents visible consumer innovation, products you can hold, use, show your friends, NVIDIA represents something entirely different: **invisible infrastructure** that powers the digital world.

You've probably never thought about NVIDIA while using ChatGPT. But tens of thousands of NVIDIA GPUs trained the model you're talking to. When a Tesla navigates traffic, NVIDIA chips process the camera feeds. When a pharmaceutical company uses AI to discover new drugs, NVIDIA hardware runs the calculations.

This invisibility creates a fascinating market dynamic. **How do investors price innovations that most people can't see, touch, or directly experience?** The answer, it turns out, depends enormously on timing.

---

### CUDA Launch (June 23, 2007): The Most Important Innovation Nobody Noticed

In June 2007, NVIDIA announced something that sounded deeply technical: CUDA, the "Compute Unified Device Architecture." In essence, CUDA let programmers write general-purpose code that would run on graphics cards, not just the specialized rendering instructions that GPUs were designed for.

At the time, this seemed like a niche feature. Graphics cards were for gaming. Who would want to run regular programs on them?

On announcement day, NVIDIA's stock fell **-2.64%**. The market shrugged.

The 30-day return was a modest **+2.61%**, essentially noise.

<div class="sdx-embed-block">
  <div class="sdx-embed-card" data-animate="fade-up">
    <div class="sdx-embed-head">
      <h4 class="sdx-embed-title">CUDA Launch</h4>
      <span class="sdx-embed-kicker">Interactive window</span>
    </div>
    <div class="sdx-embed-body">
      <iframe
        class="sdx-embed-iframe"
        src="assets/nvidia_event_exports/cuda_launch_plotly_dark.html"
        title="CUDA launch innovation footprint explorer"
        loading="lazy"
      ></iframe>
    </div>
  </div>
</div>

What nobody understood in 2007, what _couldn't_ be understood, was that CUDA would become the foundation of modern artificial intelligence. Neural networks, it turned out, were perfectly suited for GPU computing. The same parallel processing that rendered video game graphics could train deep learning models thousands of times faster than traditional processors.

But that realization wouldn't come for years. AlexNet, the deep learning breakthrough that ignited the AI revolution, used CUDA to train its neural network, in 2012, five years after CUDA's launch. The full implications of what NVIDIA had built in 2007 didn't become clear until more than a decade later.

CUDA is the ultimate **slow-burn story**. The innovation footprint was invisible for years, not because the market was stupid, but because the application that would make CUDA revolutionary didn't exist yet.

---

### Tesla V100 Launch (May 10, 2017): The Market Gets It

Fast forward ten years. By 2017, deep learning had exploded. Every tech giant was racing to build AI capabilities. The demand for GPU computing had gone from academic curiosity to industrial necessity.

Into this environment, NVIDIA launched the Tesla V100, the first GPU with "Tensor Cores," specialized circuits designed specifically for the matrix math at the heart of neural networks. This wasn't a gaming card that happened to be good at AI; it was a purpose-built AI accelerator.

The market's response was immediate and unmistakable:

**Event day return: +17.83%**  
**30-day return: +30.71%**

  <div class="sdx-embed-block">
    <div class="sdx-embed-card" data-animate="fade-up">
      <div class="sdx-embed-head">
        <h4 class="sdx-embed-title">Tesla V100 Launch</h4>
        <span class="sdx-embed-kicker">Interactive window</span>
      </div>
      <div class="sdx-embed-body">
        <iframe
          class="sdx-embed-iframe"
          src="{{ '/assets/nvidia_event_exports/tesla_v100_launch_plotly_dark.html' | relative_url }}"
          title="Tesla V100 launch innovation footprint explorer"
          loading="lazy"
        ></iframe>
      </div>
    </div>
  </div>

This is what we call an **"Instant Footprint"**, immediate, sustained, unmistakable recognition. The market understood that NVIDIA had created the essential hardware for the AI revolution. No slow burn, no gradual awakening. The footprint was there on day one.

Why the difference between CUDA (ignored) and V100 (celebrated)? Context. In 2007, deep learning didn't exist as a commercial force. In 2017, it was the hottest technology in the world, and demand for AI computing was exploding. The market could see the V100's value because it could see the demand.

---

### DGX-1 Launch (April 5, 2016): When GPUs Become a Product

By 2016, deep learning had escaped the lab, but building the hardware stack was still a craft project. If you were a researcher or a startup, you needed GPUs, drivers, CUDA libraries, frameworks, and a lot of time making everything work together.

DGX-1 was NVIDIA's attempt to productize the whole thing. Not a single chip, but a deep learning system in a box, built for one job, train neural networks fast.

The market reaction was understated on day one:

**Event day return: -0.14%**  
**30-day return: +18.27%**

  <div class="sdx-embed-block">
    <div class="sdx-embed-card" data-animate="fade-up">
      <div class="sdx-embed-head">
        <h4 class="sdx-embed-title">DGX-1 Launch</h4>
        <span class="sdx-embed-kicker">Interactive window</span>
      </div>
      <div class="sdx-embed-body">
        <iframe
          class="sdx-embed-iframe"
          src="{{ '/assets/nvidia_event_exports/dgx_1_launch_plotly_detailed.html' | relative_url }}"
          title="DGX-1 launch innovation footprint explorer"
          loading="lazy"
        ></iframe>
      </div>
    </div>
  </div>
This is a different kind of footprint. Not a loud spike, but a quiet pivot, NVIDIA signaling that it was not just selling gaming parts anymore, it was building an AI platform.

---

### H100 Hopper Launch (March 22, 2022): Right Chip, Wrong Tape

In March 2022, NVIDIA introduced Hopper, the H100, a GPU designed to be the workhorse of modern AI training. On paper, this should have been another clean, instant footprint.

Instead, the market did the opposite:

**Event day return: -0.79%**  
**30-day return: -23.34%**

  <div class="sdx-embed-block">
    <div class="sdx-embed-card" data-animate="fade-up">
      <div class="sdx-embed-head">
        <h4 class="sdx-embed-title">H100 Hopper Launch</h4>
        <span class="sdx-embed-kicker">Interactive window</span>
      </div>
      <div class="sdx-embed-body">
        <iframe
          class="sdx-embed-iframe"
          src="{{ '/assets/nvidia_event_exports/h100_hopper_launch_plotly_detailed.html' | relative_url }}"
          title="H100 Hopper launch innovation footprint explorer"
          loading="lazy"
        ></iframe>
      </div>
    </div>
  </div>

The explanation is not that the innovation was weak. It is timing. 2022 was a brutal tech drawdown. Rates were rising, growth multiples were compressing, and investors were de-risking. Even a real breakthrough had to fight for oxygen.

Hopper matters in hindsight because it shows a hard truth about market recognition. Sometimes the market sees the future, and still refuses to pay for it, because the present is on fire.

---

### NVIDIA Event Summary: All 8 Events Compared

<div class="sdx-embed-block">
  <div class="sdx-embed-stack">
    <div class="sdx-embed-card" data-animate="fade-up">
      <div class="sdx-embed-head">
        <h4 class="sdx-embed-title">NVIDIA: Cumulative returns</h4>
        <span class="sdx-embed-kicker">Interactive window</span>
      </div>
      <div class="sdx-embed-body">
        <iframe
          class="sdx-embed-iframe"
          src="assets/nvidia_event_exports/nvidia_cumulative_returns_interactive.html"
          title="NVIDIA cumulative returns explorer"
          loading="lazy"
        ></iframe>
      </div>
    </div>
    <div class="sdx-embed-card" data-animate="fade-up">
      <div class="sdx-embed-head">
        <h4 class="sdx-embed-title">NVIDIA: Day 0 vs 30-day returns</h4>
        <span class="sdx-embed-kicker">Interactive window</span>
      </div>
      <div class="sdx-embed-body">
        <iframe
          class="sdx-embed-iframe"
          src="assets/nvidia_event_exports/nvidia_plotly_05_30day_cumulative_returns.html"
          title="NVIDIA day 0 vs 30-day returns explorer"
          loading="lazy"
          data-sdx-height="800"
        ></iframe>
      </div>
    </div>

  </div>
</div>

| Event           | Day-0 Return | 30-Day Return | Pattern Type           |
| --------------- | ------------ | ------------- | ---------------------- |
| CUDA Launch     | -2.64%       | +2.61%        | Decade-long slow burn  |
| DGX-1 Launch    | -0.14%       | +18.27%       | Quiet platform shift   |
| Tesla V100      | +17.83%      | +30.71%       | Instant recognition    |
| RTX 2080 Ti     | +1.23%       | +15.65%       | Strong innovation      |
| A100 Ampere     | +3.22%       | +14.05%       | Datacenter bet pays    |
| Arm Acquisition | +5.82%       | +2.09%        | Deal skepticism        |
| H100 Hopper     | -0.79%       | -23.34%       | Bear market overwhelms |
| Blackwell B200  | +0.70%       | -2.32%        | High expectations      |

**The key insight:** NVIDIA's story reveals that **timing is everything** for infrastructure innovation. The same company can release equally important innovations and see completely different market responses, depending on whether the demand for that innovation is already visible.

CUDA in 2007 was a solution looking for a problem. DGX-1 in 2016 was NVIDIA packaging the solution before the world fully understood the scale of the problem. The V100 in 2017 was a solution to a problem everyone was desperately trying to solve. Same company, same engineering excellence, vastly different market recognition.

<div class="sdx-embed-block">
  <div class="sdx-embed-card" data-animate="fade-up">
    <div class="flourish-embed flourish-chart" data-src="visualisation/26811097"><script src="https://public.flourish.studio/resources/embed.js"></script><noscript><img src="https://public.flourish.studio/visualisation/26811097/thumbnail" width="100%" alt="chart visualization" /></noscript></div>
  </div>
</div>

</div>
</div>

    <div class="sdx-panel" id="chapter-tesla" data-animate="fade-up">
      <h2 class="title is-4">Chapter 3 - Tesla: Hype, Skepticism, and Spectacle</h2>
      <div class="sdx-chapter-hero" aria-hidden="true">
        <img
          class="sdx-chapter-hero-img"
          src="{{ '/assets/images/tesla-mexico.webp' | relative_url }}"
          alt=""
          loading="lazy"
          decoding="async"
        />
        <div class="sdx-chapter-hero-caption">
          <span class="sdx-chapter-hero-kicker">Chapter 3</span>
          <span class="sdx-chapter-hero-title">Tesla Narrative Machine</span>
        </div>
      </div>
      <div class="content" markdown="1">

Tesla defies easy categorization. It's not just a car company, it's a phenomenon, a cultural touchstone, a perpetual drama playing out in real-time across social media, financial news, and Elon Musk's Twitter feed.

This creates unique challenges for understanding market recognition. With Apple, we're analyzing how markets respond to technology. With NVIDIA, we're analyzing how markets respond to infrastructure demand. With Tesla, we're analyzing how markets respond to **narrative, spectacle, and the complex psychology of believing in the future.**

---

### Autopilot Announcement (October 10, 2014): When Tesla Starts Selling Software

Tesla's Autopilot announcement was not a new car, it was a new identity. The company was asking investors to see Tesla as more than an automaker, a sensor stack, a computer on wheels, and a software roadmap that could compound over time.

The market was not impressed on day one:

**Event day return: -7.82%**  
**30-day return: +2.48%**

  <div class="sdx-embed-block">
    <div class="sdx-embed-card" data-animate="fade-up">
      <div class="sdx-embed-head">
        <h4 class="sdx-embed-title">Autopilot Announcement</h4>
        <span class="sdx-embed-kicker">Interactive window</span>
      </div>
      <div class="sdx-embed-body">
        <iframe
          class="sdx-embed-iframe"
          src="{{ '/assets/tesla_event_exports/autopilot_announcement_plotly_detailed.html' | relative_url }}"
          title="Autopilot announcement innovation footprint explorer"
          loading="lazy"
        ></iframe>
      </div>
    </div>
  </div>

That combination is classic Tesla. The headline triggers fear, regulation risk, liability, execution, but the idea lingers, and the stock drifts back as investors reprice the narrative.

---

### Model 3 First Deliveries (July 28, 2017): Proof, and the Start of Production Hell

The Model 3 was Tesla's make or break product. Deliveries meant the promise was real, but they also opened the harder question, can Tesla scale without breaking?

The footprint was subtle:

**Event day return: +0.18%**  
**30-day return: +8.54%**

  <div class="sdx-embed-block">
    <div class="sdx-embed-card" data-animate="fade-up">
      <div class="sdx-embed-head">
        <h4 class="sdx-embed-title">Model 3 First Deliveries</h4>
        <span class="sdx-embed-kicker">Interactive window</span>
      </div>
      <div class="sdx-embed-body">
        <iframe
          class="sdx-embed-iframe"
          src="{{ '/assets/tesla_event_exports/model_3_first_deliveries_plotly_detailed.html' | relative_url }}"
          title="Model 3 first deliveries innovation footprint explorer"
          loading="lazy"
        ></iframe>
      </div>
    </div>
  </div>

This is a slow-burn pattern. The market did not celebrate the first cars, it waited to see whether the factory could keep up.

---

### Cybertruck Reveal (November 21, 2019): When Spectacle Wins

The Cybertruck reveal was the most viral product unveiling in automotive history, and not entirely for the reasons Tesla intended.

When Elon Musk invited his lead designer to throw a metal ball at the truck's "unbreakable" windows, the window shattered. On live television. In front of a cheering crowd. The designer threw a second ball at the rear window. It shattered too.

Twitter exploded. Memes proliferated. "Cybertruck fail" trended worldwide.

And then something remarkable happened: **200,000+ reservations in the first 48 hours.**

The spectacle _worked_, not despite the failure, but perhaps because of it. The broken windows made the event unforgettable. The polarizing design sparked endless debate. Everyone was talking about Tesla.

Event day return: **+0.74%**. Surprisingly muted given the viral explosion.  
30-day return: **+32.19%**

  <div class="sdx-embed-block">
    <div class="sdx-embed-card" data-animate="fade-up">
      <div class="sdx-embed-head">
        <h4 class="sdx-embed-title">Cybertruck Reveal</h4>
        <span class="sdx-embed-kicker">Interactive window</span>
      </div>
      <div class="sdx-embed-body">
        <iframe
          class="sdx-embed-iframe"
          src="{{ '/assets/tesla_event_exports/cybertruck_reveal_plotly_dark.html' | relative_url }}"
          title="Cybertruck reveal innovation footprint explorer"
          loading="lazy"
        ></iframe>
      </div>
    </div>
  </div>

The Cybertruck reveal shows something important about Tesla's relationship with markets: **spectacle can create sustained momentum, even when the spectacle includes embarrassing failures.** The event generated attention, attention generated interest, interest generated reservations, reservations suggested demand, and demand supported stock price.

Whether this represents "real" innovation recognition or hype-driven speculation is still debated. But the footprint is undeniable.

---

### AI Day (August 19, 2021): Optimus and Dojo, Vision Meets Skepticism

Tesla AI Day was a perfect example of why Tesla is hard to analyze. On one stage, Tesla revealed two ambitious bets:

- **Optimus (Tesla Bot)**, a humanoid robot vision that pushed the story beyond cars
- **Dojo**, a custom supercomputer designed to train autonomy models at scale

Both announcements landed on the same trading day, so they share the same footprint:

**Event day return: -2.25%**  
**30-day return: +15.11%**

  <div class="sdx-embed-block">
    <div class="sdx-embed-grid">
      <div class="sdx-embed-card" data-animate="fade-up">
        <div class="sdx-embed-head">
          <h4 class="sdx-embed-title">Optimus (Tesla Bot)</h4>
          <span class="sdx-embed-kicker">Interactive window</span>
        </div>
        <div class="sdx-embed-body">
          <iframe
            class="sdx-embed-iframe"
            src="{{ '/assets/tesla_event_exports/tesla_bot_announcement_plotly_detailed.html' | relative_url }}"
            title="Optimus (Tesla Bot) innovation footprint explorer"
            loading="lazy"
          ></iframe>
        </div>
      </div>

      <div class="sdx-embed-card" data-animate="fade-up">
        <div class="sdx-embed-head">
          <h4 class="sdx-embed-title">Dojo (Training Supercomputer)</h4>
          <span class="sdx-embed-kicker">Interactive window</span>
        </div>
        <div class="sdx-embed-body">
          <iframe
            class="sdx-embed-iframe"
            src="{{ '/assets/tesla_event_exports/dojo_supercomputer_announcement_plotly_detailed.html' | relative_url }}"
            title="Dojo supercomputer innovation footprint explorer"
            loading="lazy"
          ></iframe>
        </div>
      </div>

    </div>

  </div>

Day one looked like doubt. The robot reveal included a human dancer in a costume. The Dojo story was technical and easy to dismiss as a slide deck promise. But over the next month, the stock rallied anyway. Tesla was still being priced as a company that might become more than a car company.

---

### Shipping the Future (Late 2023 to 2024): Reality Checks, and One Big Jump

By late 2023, Tesla was under pressure, margins were tightening, and the market wanted evidence, not just narratives. The next three events are the same story in three different moods:

- **Cybertruck Deliveries Begin (Nov 30, 2023):** -1.66% day-0, -8.40% over 30 days (reality arrives, the stock sells the news)
- **Optimus Gen 2 Reveal (Dec 13, 2023):** +0.96% day-0, -20.21% over 30 days (a better demo, but the market keeps de-risking)
- **FSD v12 Wide Rollout (Mar 16, 2024):** +6.25% day-0, +5.45% over 30 days (a rare clean headline pop, modest follow-through)

Tesla is not one company in markets. It is three, and the stock swings between them: automaker, software bet, and moonshot lab.

---

### Tesla Event Summary: All 8 Events Compared

<div class="sdx-embed-block">
  <div class="sdx-embed-stack">
    <div class="sdx-embed-card" data-animate="fade-up">
      <div class="sdx-embed-head">
        <h4 class="sdx-embed-title">Tesla: Cumulative returns</h4>
        <span class="sdx-embed-kicker">Interactive window</span>
      </div>
      <div class="sdx-embed-body">
        <iframe
          class="sdx-embed-iframe"
          src="assets/tesla_event_exports/tesla_cumulative_returns_interactive.html"
          title="Tesla cumulative returns explorer"
          loading="lazy"
        ></iframe>
      </div>
    </div>
    <div class="sdx-embed-card" data-animate="fade-up">
      <div class="sdx-embed-head">
        <h4 class="sdx-embed-title">Tesla: Day 0 vs 30-day returns</h4>
        <span class="sdx-embed-kicker">Interactive window</span>
      </div>
      <div class="sdx-embed-body">
        <iframe
          class="sdx-embed-iframe"
          src="assets/tesla_event_exports/tesla_plotly_05_30day_cumulative_returns.html"
          title="Tesla day 0 vs 30-day returns explorer"
          loading="lazy"
          data-sdx-height="600"
        ></iframe>
      </div>
    </div>
  </div>
</div>

| Event                           | Day-0 Return | 30-Day Return | What Happened               |
| ------------------------------- | ------------ | ------------- | --------------------------- |
| Autopilot Announcement          | -7.82%       | +2.48%        | Skepticism to acceptance    |
| Model 3 First Deliveries        | +0.18%       | +8.54%        | Execution beats fears       |
| Cybertruck Reveal               | +0.74%       | +32.19%       | Viral over rational         |
| Tesla Bot Announcement          | -2.25%       | +15.11%       | Skepticism to curiosity     |
| Dojo Supercomputer Announcement | -2.25%       | +15.11%       | Big ambition, same day      |
| Cybertruck Deliveries Begin     | -1.66%       | -8.40%        | Reality arrives late        |
| Optimus Gen 2 Reveal            | +0.96%       | -20.21%       | Demo improves, stock slides |
| FSD v12 Wide Rollout            | +6.25%       | +5.45%        | Big jump, modest drift      |

**The key insight:** Tesla events are **highly unpredictable**. The correlation between day-0 reactions and 30-day outcomes is essentially random, weaker than for Apple, weaker than for NVIDIA, close to zero.

This reflects Tesla's unique position in markets: it's priced on **belief in the future**, not analysis of the present. And belief is volatile. It can surge on spectacle and crash on disappointment. The footprints exist, but they're chaotic, reflecting the chaotic nature of narrative-driven investing.

<div class="sdx-embed-block">
  <div class="sdx-embed-card" data-animate="fade-up">
    <div class="flourish-embed flourish-chart" data-src="visualisation/26811111"><script src="https://public.flourish.studio/resources/embed.js"></script><noscript><img src="https://public.flourish.studio/visualisation/26811111/thumbnail" width="100%" alt="chart visualization" /></noscript></div>
  </div>
</div>

</div>
</div>

    <div class="sdx-panel" id="chapter-ai" data-animate="fade-up">
      <h2 class="title is-4">Chapter 4 - Innovation Stack: When Everything Moves Together</h2>
      <div class="sdx-chapter-hero" aria-hidden="true">
        <img
          class="sdx-chapter-hero-img"
          src="{{ '/assets/images/innovation.png' | relative_url }}"
          alt=""
          loading="lazy"
          decoding="async"
        />
        <div class="sdx-chapter-hero-caption">
          <span class="sdx-chapter-hero-kicker">Chapter 4</span>
          <span class="sdx-chapter-hero-title">Innovation Stack</span>
        </div>
      </div>
      <div class="content" markdown="1">

This chapter is where our method stops being a single-company microscope and becomes a wide-angle lens.

Until now we followed protagonists, Apple on a stage, NVIDIA in the datacenter, Tesla in the spotlight. In this chapter, the protagonist is the whole industry. The camera pulls back.

When an innovation hits the innovation stack, it rarely stays inside one ticker. It spreads. Partners, suppliers, competitors, and the platforms that will be disrupted all move, sometimes in opposite directions. That is what makes this chapter different. We stop asking, "did one stock jump?" and start asking, "did the market move together?"

To measure that, we track a basket of the **25 largest, most liquid market-cap leaders** across the innovation stack around the same milestone dates and look at two signals:

- the sector average return over the event window
- the <a href="#winner-ratio-definition"><strong>Winner Ratio</strong></a>, how many of the 25 finish the window positive

<div class="flourish-embed flourish-network" data-src="visualisation/26742106"><script src="https://public.flourish.studio/resources/embed.js"></script><noscript><img src="https://public.flourish.studio/visualisation/26742106/thumbnail" width="100%" alt="network visualization" /></noscript></div>

---

Most of the visuals in this chapter are still being built. The metric bullets below use the 30-day window; the **PLACEHOLDER** callouts mark where charts and heatmaps will land. In the narrative, we zoom in on three stack shocks; the full event list is summarized at the end of the chapter.

---

### ASML First EUV Tools (August 29, 2006): The Chokepoint in Modern Chips

EUV is one of those breakthroughs that does not look like a consumer moment, but becomes a bottleneck for the entire industry. If you want leading edge chips, you need EUV. That means a single supplier milestone can ripple into foundries, designers, and eventually every company that depends on faster compute.

- Winner Ratio: **88%**
- Sector average 30-day return: **+8.93%**

It is a quiet kind of turning point, but the footprint is loud: the basket averages **+8.93%** over 30 days, and **88%** of names finish green.

<div class="sdx-embed-block">
  <div class="sdx-embed-card" data-animate="fade-up">
    <div class="sdx-embed-head">
      <h4 class="sdx-embed-title">ASML EUV: Sector-wide impact</h4>
      <span class="sdx-embed-kicker">Interactive window</span>
    </div>
    <div class="sdx-embed-body">
      <iframe
        class="sdx-embed-iframe"
        src="{{ '/assets/innovation_sector_exports/plotly_event_ASML_First_EUV_Tools_sector_average_and_event_day_30d.html' | relative_url }}"
        title="ASML EUV sector-wide impact analysis"
        loading="lazy"
      ></iframe>
    </div>
  </div>
</div>

---

### Meta LLaMA Release (February 24, 2023): Open Source as a Shockwave

LLaMA is a reminder that not every turning point is a product you can buy. Sometimes it is a capability that becomes broadly accessible. By pushing frontier-grade models into the open-source ecosystem, LLaMA changed developer expectations and accelerated demand for training, inference, and tooling across the stack.

- Winner Ratio: **92%**
- Sector average 30-day return: **+10.30%**

That is what an open-source shockwave looks like on a price chart: **+10.30%** on average, with **92%** of the basket positive.

<div class="sdx-embed-block">
  <div class="sdx-embed-card" data-animate="fade-up">
    <div class="sdx-embed-head">
      <h4 class="sdx-embed-title">LLaMA: Sector-wide impact</h4>
      <span class="sdx-embed-kicker">Interactive window</span>
    </div>
    <div class="sdx-embed-body">
      <iframe
        class="sdx-embed-iframe"
        src="{{ '/assets/innovation_sector_exports/plotly_event_Meta_LLaMA_Release_sector_average_and_event_day_30d.html' | relative_url }}"
        title="Meta LLaMA sector-wide impact analysis"
        loading="lazy"
      ></iframe>
    </div>
  </div>
</div>

---

### Vision Pro Announcement (June 5, 2023): A New Interface, a Big Question Mark

Vision Pro is the rare product launch that tries to create a new category. Markets like categories, but only when they turn into ecosystems. The early footprint here is less about day 0 hype and more about whether the stack believes spatial computing becomes a platform, or stays a premium niche.

- Winner Ratio: **83%**
- Sector average 30-day return: **+10.67%**

Even with all the "VR has failed before" skepticism baked in, the stack leans in: **+10.67%** on average, and **83%** of names end the window up.

<div class="sdx-embed-block">
  <div class="sdx-embed-card" data-animate="fade-up">
    <div class="sdx-embed-head">
      <h4 class="sdx-embed-title">Vision Pro: Sector-wide impact</h4>
      <span class="sdx-embed-kicker">Interactive window</span>
    </div>
    <div class="sdx-embed-body">
      <iframe
        class="sdx-embed-iframe"
        src="{{ '/assets/innovation_sector_exports/plotly_event_Vision_Pro_Announcement_sector_average_and_event_day_30d.html' | relative_url }}"
        title="Vision Pro sector-wide impact analysis"
        loading="lazy"
      ></iframe>
    </div>
  </div>
</div>

---

### Innovation Stack Summary: Twelve Events, One Map

| Event      | Date     | Sector Return | Winner Ratio |
| ---------- | -------- | ------------- | ------------ |
| Amazon S3  | Mar 2006 | +4.77%        | 65%          |
| ASML EUV   | Aug 2006 | +8.93%        | 88%          |
| iPhone     | Jun 2007 | -0.30%        | 59%          |
| Chrome     | Sep 2008 | -24.72%       | 6%           |
| Azure      | Feb 2010 | +8.77%        | 89%          |
| Touch ID   | Sep 2013 | +2.70%        | 71%          |
| TensorFlow | Nov 2015 | +1.42%        | 64%          |
| Armv9      | Mar 2021 | -2.34%        | 50%          |
| LLaMA      | Feb 2023 | +10.30%       | 92%          |
| GPT-4      | Mar 2023 | +3.17%        | 63%          |
| Copilot    | Mar 2023 | +3.23%        | 67%          |
| Vision Pro | Jun 2023 | +10.67%       | 83%          |

Two final lenses make the "distributed footprint" concrete:

- **Cross-sectional dispersion:** how spread out returns are across the 25 companies. Higher dispersion means clearer winners and losers.
- **Return range (best vs worst):** the gap between the strongest and weakest names in the basket for each event. It shows how brutal the tails can be even when the average looks fine.

<div class="sdx-embed-block">
  <div class="sdx-embed-card" data-animate="fade-up">
    <div class="sdx-embed-head">
      <h4 class="sdx-embed-title">Breadth vs Spread: Dispersion &amp; Return Range</h4>
      <span class="sdx-embed-kicker">Interactive windows</span>
    </div>
    <div class="sdx-embed-body">
      <div class="sdx-embed-stack">
        <iframe
          class="sdx-embed-iframe"
          src="{{ '/assets/innovation_sector_exports/plotly_04_cross_sectional_dispersion.html' | relative_url }}"
          title="Innovation stack cross-sectional dispersion"
          loading="lazy"
        ></iframe>
        <iframe
          class="sdx-embed-iframe"
          src="{{ '/assets/innovation_sector_exports/plotly_06_return_range_dumbbell.html' | relative_url }}"
          title="Innovation stack return range dumbbell"
          loading="lazy"
        ></iframe>
      </div>
    </div>
  </div>
</div>

The point of this chapter is not to crown a single winner. It is to show that when the stack is hit, the footprint is usually distributed, and often asymmetric.

Next, we leave the innovation stack and enter a domain where the rules are even stricter, healthcare, where a single approval can rewrite the future overnight.

</div>
    </div>

    <div class="sdx-panel" id="chapter-biotech" data-animate="fade-up">
      <h2 class="title is-4">Chapter 5 - Healthcare: The Power of Regulatory Moments</h2>
      <div class="sdx-chapter-hero" aria-hidden="true">
        <img
          class="sdx-chapter-hero-img"
          src="{{ '/assets/images/healthcare.png' | relative_url }}"
          alt=""
          loading="lazy"
          decoding="async"
        />
        <div class="sdx-chapter-hero-caption">
          <span class="sdx-chapter-hero-kicker">Chapter 5</span>
          <span class="sdx-chapter-hero-title">Regulatory Moments</span>
        </div>
      </div>
      <div class="content" markdown="1">

Healthcare innovations operate under different rules than anything in technology. A drug that shows promising results in trials might never help a single patient, until regulators say yes.

This creates something unique in markets: **binary events with massive stakes.** An FDA approval transforms "might work" into "will work" in a single moment. Billions of dollars in value can appear, or vanish, overnight.

---

### mRNA Vaccine Approval (December 11, 2020): A Historic Day

December 11, 2020, was one of the most important days in medical history. The FDA granted emergency use authorization to Pfizer-BioNTech's Comirnaty vaccine, the first mRNA vaccine ever approved for human use.

This wasn't just a new vaccine. It was validation of an entirely new platform technology. mRNA vaccines had been theoretical for decades. Suddenly, they were real, and proving themselves against a pandemic that had killed millions.

How did the healthcare sector respond?

Sector average 30-day return: **+2.48%**  
Sector median 30-day return: **+0.48%**

<div class="sdx-embed-block">
  <div class="sdx-embed-card" data-animate="fade-up">
    <div class="sdx-embed-head">
      <h4 class="sdx-embed-title">First mRNA Vaccine (Comirnaty)</h4>
      <span class="sdx-embed-kicker">Interactive window</span>
    </div>
    <div class="sdx-embed-body">
      <iframe
        class="sdx-embed-iframe"
        src="{{ '/assets/healthcare_sector_exports/plotly_event_First_mRNA_Vaccine_Comirnaty_sector_average_and_event_day_30d.html' | relative_url }}"
        title="First mRNA Vaccine (Comirnaty) healthcare sector window"
        loading="lazy"
      ></iframe>
    </div>
  </div>
</div>

The returns look modest, but context matters. This was during the chaotic post-election, mid-pandemic market. Vaccine optimism was already partially priced in. And the impact wasn't uniform: Pfizer saw different movement than surgical device makers.

---

### The GLP-1 Revolution: A New Category Emerges

Perhaps no healthcare innovation has reshaped markets more dramatically than GLP-1 drugs for weight loss. Drugs like Wegovy, Mounjaro, and Zepbound didn't just help diabetics manage blood sugar, they produced unprecedented weight loss in clinical trials.

The implications extend far beyond pharmaceuticals. Food companies must reconsider their futures. Weight Watchers restructured its entire business model. Fitness chains adjusted projections. Medical device makers serving obese patients reconsidered long-term demand.

**Zepbound Obesity Launch (November 8, 2023):**

- Sector average 30-day return: **+7.73%**
- Sector median 30-day return: **+7.71%**

<div class="sdx-embed-block">
  <div class="sdx-embed-card" data-animate="fade-up">
    <div class="sdx-embed-head">
      <h4 class="sdx-embed-title">Zepbound Obesity Drug Launch</h4>
      <span class="sdx-embed-kicker">Interactive window</span>
    </div>
    <div class="sdx-embed-body">
      <iframe
        class="sdx-embed-iframe"
        src="{{ '/assets/healthcare_sector_exports/plotly_event_Zepbound_Obesity_Drug_Launch_sector_average_and_event_day_30d.html' | relative_url }}"
        title="Zepbound obesity drug launch healthcare sector window"
        loading="lazy"
      ></iframe>
    </div>
  </div>
</div>

The GLP-1 revolution creates clear footprints, not just for drug makers like Eli Lilly and Novo Nordisk, but for entire adjacent industries.

---

### CRISPR Approval (December 8, 2023): Gene Editing Becomes Real

For decades, CRISPR existed in science fiction and research labs. The ability to edit genes precisely, to potentially cure genetic diseases at their source, seemed perpetually futuristic.

On December 8, 2023, the future arrived. The FDA approved Casgevy, the first CRISPR gene-editing therapy, for treating sickle cell disease. A technology that had won Nobel Prizes was now helping actual patients.

Sector average 30-day return: **+6.37%**

<div class="sdx-embed-block">
  <div class="sdx-embed-card" data-animate="fade-up">
    <div class="sdx-embed-head">
      <h4 class="sdx-embed-title">Casgevy CRISPR Therapy Approval</h4>
      <span class="sdx-embed-kicker">Interactive window</span>
    </div>
    <div class="sdx-embed-body">
      <iframe
        class="sdx-embed-iframe"
        src="{{ '/assets/healthcare_sector_exports/plotly_event_Casgevy_CRISPR_Therapy_Approval_sector_average_and_event_day_30d.html' | relative_url }}"
        title="Casgevy CRISPR therapy approval healthcare sector window"
        loading="lazy"
      ></iframe>
    </div>
  </div>
</div>

The market recognized CRISPR's approval as transformative, not just for Vertex (which partnered on Casgevy) but for the entire biotechnology sector. Gene editing had crossed from possibility to reality.

---

### Healthcare Event Summary

<div class="sdx-embed-block">
  <div class="sdx-embed-card" data-animate="fade-up">
    <div class="sdx-embed-head">
      <h4 class="sdx-embed-title">Healthcare Events Comparison (10 Events)</h4>
      <span class="sdx-embed-kicker">Interactive window</span>
    </div>
    <div class="sdx-embed-body">
      <iframe
        class="sdx-embed-iframe"
        src="{{ '/assets/healthcare_sector_exports/plotly_07_avg_30d_return_by_event.html' | relative_url }}"
        title="Healthcare events comparison chart (10 events)"
        loading="lazy"
      ></iframe>
    </div>
  </div>
</div>

| Event            | 30-Day Return | Type                |
| ---------------- | ------------- | ------------------- |
| mRNA Vaccine     | +2.48%        | Platform technology |
| Wegovy Launch    | +4.10%        | Drug launch         |
| Paxlovid Launch  | -2.26%        | COVID treatment     |
| Mounjaro Launch  | -1.35%        | Diabetes/obesity    |
| Leqembi Approval | -3.33%        | Alzheimer's         |
| Zepbound Launch  | +7.73%        | GLP-1 blockbuster   |
| Casgevy CRISPR   | +6.37%        | Gene therapy        |
| AlphaFold 2      | +5.51%        | AI breakthrough     |
| GPT-4 Medical    | +8.02%        | Medical AI          |
| Da Vinci 5       | -3.54%        | Surgical robotics   |

**The key insight:** Healthcare innovations show **stronger immediate recognition** than many tech innovations. When the FDA says yes, uncertainty collapses instantly. The footprint is clearer because the event is binary.

<p class="sdx-note">PLACEHOLDER: Flourish - Healthcare Innovations Line Chart Race (data/healthcare_sector_exports/flourish_long_format/01_all_innovations_all_companies_long.csv).</p>
</div>
    </div>

  </div>
</section>

<section class="section sdx-section alt" id="archetypes">
  <div class="container">
    <h2 class="title is-3">Act IV - The Three Archetypes of Market Recognition</h2>

    <div class="sdx-panel" data-animate="fade-up" markdown="1">

After analyzing 42 innovation events across five domains, clear patterns emerge. Markets don't recognize all innovations the same way. Instead, we found **three distinct archetypes** of market response:

---

### 1. The Instant Footprint

Some innovations are recognized immediately and sustainably. The event-day return is strong and positive, and that strength continues through the 30-day window. The market sees the innovation, understands its value, and prices it accordingly.

**Classic Examples:**

- NVIDIA V100 Launch: +17.83% day-0, +30.71% over 30 days
- Healthcare regulatory approvals with clear commercial potential
- Infrastructure plays when demand is already visible

<div class="sdx-embed-block">
  <div class="sdx-dual-panel">
    <div class="sdx-embed-card" data-animate="fade-up">
      <div class="sdx-embed-head">
        <h4 class="sdx-embed-title">Apple Pay Launch (90-Day Window)</h4>
        <span class="sdx-embed-kicker">Interactive window</span>
      </div>
      <div class="sdx-embed-body">
        <iframe
          class="sdx-embed-iframe"
          src="{{ '/assets/act_4/apple_pay_90day_window.html' | relative_url }}"
          title="Apple Pay launch 90-day window"
          loading="lazy"
        ></iframe>
      </div>
    </div>

    <div class="sdx-embed-card" data-animate="fade-up">
      <div class="sdx-embed-head">
        <h4 class="sdx-embed-title">Plot Read: Instant Footprint</h4>
        <span class="sdx-embed-kicker">Why it fits</span>
      </div>
      <div class="sdx-embed-body">
        <p style="margin: 0; color: rgba(232, 237, 255, 0.9); line-height: 1.55;">
          Apple Pay is what immediate recognition looks like: after day 0, the curve climbs into a clean uptrend, reaching <strong>+15.4% by day 30</strong> and continuing to build through the rest of the window. No long wait-and-see period; investors price the wedge into payments and ecosystem lock-in with visible conviction.
        </p>
      </div>
    </div>

  </div>
</div>

**When it happens:** Instant footprints appear when an innovation **confirms what sophisticated investors already suspected.** The V100 didn't surprise anyone tracking AI research, it just provided the hardware that everyone knew was needed. The market was primed to price it immediately.

---

### 2. The Slow Burn

Other innovations are initially dismissed or ignored, only to be recognized weeks later. The event-day return is weak or negative, but by day 30, the cumulative return is strongly positive. The market misses the significance at first, then gradually catches on.

**Classic Examples:**

- Apple iPod: -4.63% day-0, +30.98% over 30 days
- Apple M1 Chip: -0.30% day-0, +12.93% over 30 days
- NVIDIA CUDA: -2.64% day-0, years of delayed recognition

<div class="sdx-embed-block">
  <div class="sdx-dual-panel">
    <div class="sdx-embed-card" data-animate="fade-up">
      <div class="sdx-embed-head">
        <h4 class="sdx-embed-title">Blackwell B200 Announcement (90-Day Window)</h4>
        <span class="sdx-embed-kicker">Interactive window</span>
      </div>
      <div class="sdx-embed-body">
        <iframe
          class="sdx-embed-iframe"
          src="{{ '/assets/act_4/blackwell_b200_90day_window.html' | relative_url }}"
          title="Blackwell B200 announcement 90-day window"
          loading="lazy"
        ></iframe>
      </div>
    </div>

    <div class="sdx-embed-card" data-animate="fade-up">
      <div class="sdx-embed-head">
        <h4 class="sdx-embed-title">Plot Read: Slow Burn</h4>
        <span class="sdx-embed-kicker">Why it fits</span>
      </div>
      <div class="sdx-embed-body">
        <p style="margin: 0; color: rgba(232, 237, 255, 0.9); line-height: 1.55;">
          The first month barely rewards the headline: by <strong>day 30 it's still about -2.3%</strong>. Then the story flips: the back half of the window rerates sharply as the implications sink in, pushing the curve far higher later on. That delay is the slow-burn signature: digestion first, conviction later.
        </p>
      </div>
    </div>

  </div>
</div>

**When it happens:** Slow burns appear when an innovation is **too different to understand immediately.** The iPod wasn't just a better MP3 player, it was the beginning of Apple's transformation into a consumer electronics company. CUDA wasn't just faster graphics, it was the foundation of modern AI. These implications take time to become clear.

---

### 3. The Mirage

Some events create immediate excitement that fades away. Strong initial reaction that reverses over the following weeks, leaving little or negative cumulative return. The market overreacts to spectacle or hype.

**Classic Examples:**

- Tesla Optimus Gen 2 Reveal: +0.96% day-0, -20.21% over 30 days
- Tesla Cybertruck Deliveries Begin: -1.66% day-0, -8.40% over 30 days
- Overhyped competitor announcements

<div class="sdx-embed-block">
  <div class="sdx-dual-panel">
    <div class="sdx-embed-card" data-animate="fade-up">
      <div class="sdx-embed-head">
        <h4 class="sdx-embed-title">Cybertruck Deliveries Begin (90-Day Window)</h4>
        <span class="sdx-embed-kicker">Interactive window</span>
      </div>
      <div class="sdx-embed-body">
        <iframe
          class="sdx-embed-iframe"
          src="{{ '/assets/act_4/cybertruck_deliveries_90day_window.html' | relative_url }}"
          title="Cybertruck deliveries begin 90-day window"
          loading="lazy"
        ></iframe>
      </div>
    </div>

    <div class="sdx-embed-card" data-animate="fade-up">
      <div class="sdx-embed-head">
        <h4 class="sdx-embed-title">Plot Read: Mirage</h4>
        <span class="sdx-embed-kicker">Why it fits</span>
      </div>
      <div class="sdx-embed-body">
        <p style="margin: 0; color: rgba(232, 237, 255, 0.9); line-height: 1.55;">
          The dashed line is delivery day. The curve pops briefly (peaking around <strong>day 11 ~ +5.6%</strong>), then rolls over; by <strong>day 30 it's -8.4%</strong>, and the rest of the window bleeds toward roughly <strong>-30%</strong> by day 90. That is the mirage signature: attention on launch, but no durable repricing once the story meets reality.
        </p>
      </div>
    </div>

  </div>
</div>

**When it happens:** Mirages appear when **expectations exceed reality**, or when an event is more show than substance. Tesla events are particularly prone to mirages because they blend genuine innovation with theatrical presentation. The spectacle creates immediate attention, but sustained analysis reveals less than advertised.

---

### Archetype Distribution

Of 24 single-company events analyzed:

- **Instant Winners** (+day, +30d): 37.5%
- **Slow Burn** (day 0, +30d): 29.2%, the surprise finding.
- **Double Losers** (-day, -30d): 12.5%
- **False Starts** (+day, -30d): 20.8%

<p class="sdx-note">PLACEHOLDER: Insert quadrant distribution chart (innovation_pattern_identification.ipynb, Step 2 visualization).</p>

The **Slow Burn** category, nearly 30% of events, is the most fascinating finding. These are innovations the market initially rejected but later embraced. They represent opportunities that patient investors could have captured while others panicked over negative event-day returns.

</div>

  </div>
</section>

<section class="section sdx-section alt" id="what-prices">
  <div class="container">
    <h2 class="title is-3">Act V - Building the Innovation Signature Framework</h2>

    <div class="sdx-panel" data-animate="fade-up" markdown="1">

Patterns are interesting. But can we turn them into something actionable? Can we **quantify** what makes an innovation truly transformative versus merely hyped?

Based on our pattern analysis, we built an **Innovation Signature Score** framework—a systematic way to measure how strongly the market recognized any given innovation.

---

## From Patterns to Predictors

Before building the score, we needed to identify which signals actually matter. Our correlation analysis revealed the answer.

<div class="sdx-embed-block">
  <div class="sdx-embed-card" data-animate="fade-up">
    <div class="sdx-embed-head">
      <h4 class="sdx-embed-title">Feature Correlation Heatmap</h4>
      <span class="sdx-embed-kicker">Interactive window</span>
    </div>
    <div class="sdx-embed-body">
      <iframe
        class="sdx-embed-iframe"
        src="{{ 'assets/act_5/plotly_correlation_matrix.html' | relative_url }}"
        title="Innovation signature feature correlation heatmap"
        loading="lazy"
      ></iframe>
    </div>
  </div>
</div>

**The striking finding:** Event Day Return and 30-Day Return have only **r = 0.22 correlation**. The market's immediate reaction has almost no predictive power for sustained performance. Event day is theater. The 30-day window is where recognition actually happens.

But one relationship stood out: **successful innovations decrease volatility** (r = -0.25). True breakthroughs don't just move prices—they resolve uncertainty.

---

## The Four Archetypes

<div class="sdx-embed-block">
  <div class="sdx-embed-card" data-animate="fade-up">
    <div class="sdx-embed-head">
      <h4 class="sdx-embed-title">Event Day vs 30-Day Scatter</h4>
      <span class="sdx-embed-kicker">Interactive window</span>
    </div>
    <div class="sdx-embed-body">
      <iframe
        class="sdx-embed-iframe"
        src="{{ 'assets/act_5/plotly_event_day_vs_30d_combined.html' | relative_url }}"
        title="Event day vs 30-day returns scatter"
        loading="lazy"
      ></iframe>
    </div>
  </div>
</div>

Plotting all 24 single-company events revealed four distinct patterns:

| Archetype           | Pattern    | Share | Key Examples           |
| ------------------- | ---------- | ----- | ---------------------- |
| **Instant Winners** | +Day, +30d | 37.5% | V100 (+17.8% → +30.7%) |
| **Slow Burn** 🔥    | −Day, +30d | 29.2% | iPod (-4.6% → +31.0%)  |
| **False Starts**    | +Day, −30d | 20.8% | Arm Acquisition        |
| **Double Losers**   | −Day, −30d | 12.5% | H100 Hopper            |

**The surprise:** Nearly 30% of innovations showed the "Slow Burn" pattern—initially doubted, then embraced. A negative event day does not mean failure.

---

## The Volatility Signature

<div class="sdx-embed-block">
  <div class="sdx-embed-card" data-animate="fade-up">
    <div class="sdx-embed-head">
      <h4 class="sdx-embed-title">Volatility vs Returns</h4>
      <span class="sdx-embed-kicker">Interactive window</span>
    </div>
    <div class="sdx-embed-body">
      <iframe
        class="sdx-embed-iframe"
        src="{{ '/assets/act_5/plotly_volatility_comparison.html' | relative_url }}"
        title="Volatility change vs returns"
        loading="lazy"
      ></iframe>
    </div>
  </div>
</div>

One of our most counterintuitive discoveries: **successful innovations REDUCE post-event volatility.**

| Outcome             | Pre-Event Vol | Post-Event Vol | Change     |
| ------------------- | ------------- | -------------- | ---------- |
| Positive 30d Return | 2.38%         | 2.26%          | **−0.12%** |
| Negative 30d Return | 2.74%         | 3.06%          | **+0.32%** |

**Interpretation:** True innovations resolve uncertainty. Before an announcement, the market doesn't know what to expect. After a successful innovation, price discovery occurs—investors converge on a valuation, and volatility decreases.

---

## The Innovation Signature Score Formula

We synthesized these patterns into a single composite metric with five components:

### Component 1: Return Magnitude (0-30 points)

The 30-day cumulative return, capped to prevent outliers from dominating. Big returns suggest the market eventually recognized value.

### Component 2: Positive Return Bonus (20 points)

If the 30-day return is positive, add 20 points. Direction matters more than magnitude—being positive signals success.

### Component 3: Momentum Sustained (15 points)

If the 30-day return exceeds the event-day return, add 15 points. This captures the **Slow Burn** pattern—innovations that build momentum over time.

### Component 4: Volatility Stabilization (0-10 points)

If post-event volatility is lower than pre-event volatility, add points. True innovations **resolve uncertainty**—the market figures out what something is worth.

### Component 5: Volume Conviction (0-10 points)

If trading volume increased by more than 20%, add 10 points. Sustained attention suggests genuine interest rather than noise.

---

## Innovation Categories

| Score  | Category                 | Interpretation                          |
| ------ | ------------------------ | --------------------------------------- |
| ≥60    | 🌟 **Transformative**    | Clear, sustained market recognition     |
| 40-59  | ✅ **Strong Innovation** | Solid recognition with some uncertainty |
| 20-39  | 🔶 **Moderate**          | Mixed signals, partial recognition      |
| &lt;20 | ❌ **Weak/Negative**     | Market rejected or ignored              |

---

## Top Innovations by Score

<div class="sdx-embed-block">
  <div class="sdx-embed-card" data-animate="fade-up">
    <div class="sdx-embed-head">
      <h4 class="sdx-embed-title">Innovation Scores Ranking</h4>
      <span class="sdx-embed-kicker">Interactive window</span>
    </div>
    <div class="sdx-embed-body">
      <iframe
        class="sdx-embed-iframe"
        src="{{ 'assets/act_5/plotly_innovation_scores_ranking.html' | relative_url }}"
        title="Innovation signature scores ranking"
        loading="lazy"
      ></iframe>
    </div>
  </div>
</div>

### 🌟 Transformative (Score ≥60):

| Event                  | Company | Score | 30-Day Return |
| ---------------------- | ------- | ----- | ------------- |
| Cybertruck Reveal      | Tesla   | 80    | +32.19%       |
| Tesla V100 Launch      | NVIDIA  | 75    | +30.71%       |
| iPod Launch            | Apple   | 75    | +30.98%       |
| DGX-1 Launch           | NVIDIA  | 64    | +18.27%       |
| A100 Ampere Launch     | NVIDIA  | 64    | +14.05%       |
| RTX 2080 Ti Launch     | NVIDIA  | 61    | +15.65%       |
| Tesla Bot Announcement | Tesla   | 60    | +15.11%       |

**The key insight:** The iPod (-4.6% on day 0) scores as highly as the hyped Cybertruck reveal (+0.7% on day 0). Our framework captures both immediate blockbusters and slow-burn transformations—because it rewards **sustained momentum**, not initial hype.

</div>

  </div>
</section>

<section class="section sdx-section alt" id="act-vi">
  <div class="container">
    <h2 class="title is-3">Act VI - Validation: Does It Actually Work?</h2>

    <div class="sdx-panel" data-animate="fade-up" markdown="1">

A framework is only valuable if it works on data it wasn't trained on. We tested on **13 out-of-sample events**—different companies, different industries, different time periods.

---

## The Test Events

| Category            | Events                                                      |
| ------------------- | ----------------------------------------------------------- |
| **AI/ML**           | AlphaGo, Microsoft OpenAI $10B, Meta Llama 2, Google Gemini |
| **Cloud/Dev Tools** | AWS Lambda, GitHub Copilot GA                               |
| **Biotech**         | Moderna mRNA 94.5%, CRISPR Casgevy, AlphaFold 2             |
| **Consumer**        | Netflix Streaming, Amazon Echo/Alexa                        |
| **Other**           | Adobe Firefly, Bitcoin ETF                                  |

---

## The Results

<div class="sdx-embed-block">
  <div class="sdx-embed-card" data-animate="fade-up">
    <div class="sdx-embed-head">
      <h4 class="sdx-embed-title">Out-of-Sample Validation</h4>
      <span class="sdx-embed-kicker">Interactive window</span>
    </div>
    <div class="sdx-embed-body">
      <iframe
        class="sdx-embed-iframe"
        src="{{ '/assets/act_6/plotly_out_of_sample_validation.html' | relative_url }}"
        title="Out-of-sample innovation score validation"
        loading="lazy"
      ></iframe>
    </div>
  </div>
</div>

| Event                 | Score | Category    | 30-Day Return |
| --------------------- | ----- | ----------- | ------------- |
| Moderna mRNA 94.5%    | 58    | ✅ Strong   | +13.5%        |
| Google Gemini         | 57    | ✅ Strong   | +12.3%        |
| GitHub Copilot GA     | 56    | ✅ Strong   | +11.3%        |
| Microsoft OpenAI $10B | 55    | ✅ Strong   | +5.0%         |
| Bitcoin ETF           | 45    | ✅ Strong   | +3.8%         |
| AlphaFold 2           | 25    | 🔶 Moderate | -0.4%         |
| Netflix Streaming     | 19    | ❌ Weak     | -0.9%         |
| AlphaGo               | 6     | ❌ Weak     | -3.9%         |
| Meta Llama 2          | -4    | ❌ Weak     | -4.5%         |

---

## Does Score Predict Returns?

| Group              | N   | Avg 30-Day Return           |
| ------------------ | --- | --------------------------- |
| High Score (≥40)   | 5   | **+9.2%**                   |
| Low Score (&lt;40) | 8   | **-1.9%**                   |
| **Separation**     |     | **+11.1 percentage points** |

**The framework works.** High-scoring events averaged +9.2% returns. Low-scoring events averaged -1.9%. The model successfully identified the category for **11 of 13 test events**.

---

## Visualizing the Test Events

<div class="sdx-embed-block">
  <div class="sdx-embed-card" data-animate="fade-up">
    <div class="sdx-embed-head">
      <h4 class="sdx-embed-title">Average Cumulative Return (Test Events)</h4>
      <span class="sdx-embed-kicker">Interactive window</span>
    </div>
    <div class="sdx-embed-body">
      <iframe
        class="sdx-embed-iframe"
        src="{{ '/assets/act_6/plotly_average_cumulative_return.html' | relative_url }}"
        title="Average cumulative return for out-of-sample events"
        loading="lazy"
      ></iframe>
    </div>
  </div>
</div>

Plotting the ±30 day cumulative return windows reveals how differently the market processes each innovation:

- **High scorers** (Moderna, Copilot, Gemini) show steady upward trajectories—conviction building over time
- **Low scorers** (AlphaGo, Llama 2) flatline or drift negative—the market never found a reason to reprice

The average curve across all test events mirrors what we saw in training: a slight dip around event day (uncertainty), followed by gradual separation as winners pull away from losers.

---

## Case Studies: What the Framework Reveals

**✅ Moderna mRNA (Score: 58)** — Efficacy data eliminated uncertainty. Volatility dropped. Momentum sustained. Framework correctly identified Strong Innovation.

**✅ GitHub Copilot GA (Score: 56)** — When AI-assisted coding went mainstream in June 2022, our framework flagged it as Strong Innovation. The 30-day return (+11.3%) confirmed it. This wasn't hype—it was a real product shipping to real developers.

**❌ AlphaGo (Score: 6)** — Arguably the most important AI milestone of the decade. But it was a _research demonstration_, not a product. No revenue, no commercial application. The market shrugged.

> This validates our logic: the framework measures **market recognition**, not historical importance. Some innovations matter enormously for technology's arc while leaving no immediate stock footprint.

**❌ Netflix Streaming (Score: 19)** — We know now it was the beginning of the streaming revolution. In 2007? The market didn't care. The ultimate slow-burn—too slow for even our 30-day window.

<div class="flourish-embed flourish-gauge" data-src="visualisation/26749201"><script src="https://public.flourish.studio/resources/embed.js"></script><noscript><img src="https://public.flourish.studio/visualisation/26749201/thumbnail" width="100%" alt="gauge visualization" /></noscript></div>

---

## Test Your Own Innovation

  <div class="sdx-embed-block">
    <div class="sdx-embed-card" data-animate="fade-up">
      <div class="sdx-embed-head">
        <h4 class="sdx-embed-title">Innovation Score Explorer</h4>
        <span class="sdx-embed-kicker">Interactive window</span>
      </div>
      <div class="sdx-embed-body">
        <iframe
          class="sdx-embed-iframe"
          src="{{ '/assets/act_6/innovation_score_explorer.html' | relative_url }}"
          title="Innovation score explorer"
          loading="lazy"
        ></iframe>
      </div>
    </div>
  </div>

We packaged everything into an interactive dashboard. Enter any ticker and date—the system fetches real data from Yahoo Finance and calculates the Innovation Score with full breakdown.

The next time a major innovation is announced, you can run it through the framework and get an objective assessment of market recognition.

---

## What We Built

From 46 training events + 13 test events, we constructed and validated a quantitative framework:

**The Innovation Signature Score:**

- Synthesizes return magnitude, momentum, volatility, and volume
- Successfully separates transformative innovations from noise
- Works across companies, industries, and time periods

**The Core Insight:** Event day reactions are noise. Sustained patterns are signal.

**The Three Archetypes:**

- **Instant Winners** — Immediate and sustained recognition
- **Slow Burns** — Initial doubt, then gradual acceptance
- **False Starts** — Early hype, fading conviction

Markets don't see the future perfectly. But they leave footprints—traces that a careful analyst can learn to read. We built a framework for reading them.

</div>
  </div>
</section>

<section class="section sdx-section alt" id="ai-era">
  <div class="container">
    <h2 class="title is-3">The AI Era: A Special Section</h2>

    <div class="sdx-panel" data-animate="fade-up" markdown="1">

<div class="sdx-chapter-hero" aria-hidden="true">
  <img
    class="sdx-chapter-hero-img"
    src="{{ '/assets/images/AI_1.png' | relative_url }}"
    alt=""
    loading="lazy"
    decoding="async"
  />
  <div class="sdx-chapter-hero-caption">
    <span class="sdx-chapter-hero-kicker">AI Era</span>
    <span class="sdx-chapter-hero-title">The Great Repricing</span>
  </div>
</div>

No analysis of innovation footprints would be complete without examining **the most transformative period in recent technology history**, the AI era that became impossible to ignore after ChatGPT in November 2022.

This era is recent and still unfolding. We can tell it is a huge innovative moment, but we do not yet know how big it is. Ten years from now, people may look back and say, that was the turning point. Or they may say it was one milestone in a longer sequence that started earlier and matured later.

If you said "AI started in 2022", that is not quite right. AI has decades of research behind it. What happened in late 2022 is the public inflection point, when capabilities became visible to millions overnight, and markets were forced to price the consequences.

So in this section we do something different. We take a step back and study AI as a multi-year repricing, not only a collection of 30-day windows.

<p class="sdx-note">PLACEHOLDER: Add a long-horizon AI timeline view from 2022 to 2024, with key events annotated (H100, ChatGPT, LLaMA, GPT-4, Copilot, Blackwell).</p>

---

## Before and After: The Great Reshuffling

The AI era did not just create winners, it restructured the entire technology landscape.

<p class="sdx-note">PLACEHOLDER: Insert Before/After AI Era comparison chart.</p>

### Companies That Exploded:

| Company   | Pre-ChatGPT | Current | Growth |
| --------- | ----------- | ------- | ------ |
| NVIDIA    | ~$350B      | $3T+    | ~9x    |
| Microsoft | ~$1.8T      | $3T+    | ~1.7x  |
| Meta      | ~$300B      | $1.3T+  | ~4x    |

### Companies That Struggled:

| Company | Challenge                      |
| ------- | ------------------------------ |
| Intel   | Missed AI chip transition      |
| IBM     | Legacy overhang despite Watson |

---

## The AI Footprint Problem: The Innovator Is Not Tradable

The company that triggered the public shockwave is not publicly traded, so the market expressed recognition through second-order exposures.

That is why we track the AI footprint across a basket of 25 market-cap leaders and measure both:

- the average return for the group
- how many finish positive, the **Winner Ratio**

<p class="sdx-note">Winner Ratio definition: see <a href="#winner-ratio-definition">Act II</a>.</p>

<p class="sdx-note">PLACEHOLDER: Insert Innovation Sector cumulative returns comparison chart showing all tracked companies during the ChatGPT launch window (innovation_sector_event_analysis.ipynb, sector-wide visualization).</p>

---

## AI Events: Cumulative Impact

<p class="sdx-note">PLACEHOLDER: Insert AI Events Impact Timeline (innovation_sector_event_analysis.ipynb, combined timeline visualization).</p>

| Event       | Date     | Sector Return | Winner Ratio |
| ----------- | -------- | ------------- | ------------ |
| H100 Launch | Mar 2022 | -12.33%       | 8%           |
| ChatGPT     | Nov 2022 | -2.51%        | 40%          |
| LLaMA       | Feb 2023 | +9.04%        | 88%          |
| GPT-4       | Mar 2023 | +2.20%        | 60%          |
| Copilot     | Mar 2023 | +2.26%        | 64%          |
| Blackwell   | Mar 2024 | -6.09%        | 24%          |

The pattern is clear. The first public AI moment, ChatGPT, produced mixed returns because macro context was hostile. Subsequent AI events produced clearer positive responses as the market learned to price AI infrastructure, and as the demand signal stopped being theoretical.

<p class="sdx-note">PLACEHOLDER: Flourish - interactive AI Era timeline with stock performance overlays.</p>

---

## Winners and Losers: The AI Shakeout

Not every company benefited equally from the AI repricing. Our sector-wide analysis is more nuanced than the simplistic view that AI lifts everything.

**ChatGPT (November 30, 2022)**

- Companies with positive 30-day returns: **10/25 (40%)**
- Sector average 30-day return: **-2.51%**

This looks wrong if you expect markets to celebrate breakthroughs immediately, but the context explains it. ChatGPT launched during a brutal tech bear market. The Federal Reserve was aggressively raising interest rates to fight inflation. Growth stocks were under pressure. The AI narrative was competing with recession fears.

**Meta LLaMA (February 24, 2023)**

- Companies with positive 30-day returns: **22/25 (88%)**
- Sector average 30-day return: **+9.04%**

By early 2023, the market had digested ChatGPT's implications. Investors started treating AI as a durable shift, not a single product demo. When Meta released LLaMA and accelerated open model adoption, nearly the whole ecosystem benefited.

<p class="sdx-note">PLACEHOLDER: Insert Winner Ratio comparison across all Innovation Sector events (innovation_sector_event_analysis.ipynb, Step 6 visualization).</p>

---

## Why We Zoom Out

Event windows show the first reaction, but the AI era is a compounding repricing that plays out over quarters:

- capability shocks changed what software could do
- infrastructure roadmaps changed what compute was worth
- competitive responses changed who captured the value

This is why we complement short windows with a long-horizon view. The footprint of AI is not only day 0, it is the slope of belief over time.

</div>

  </div>
</section>

<section class="section sdx-section alt" id="conclusion">
  <div class="container">
    <h2 class="title is-3">Conclusion, What the Market Really Prices</h2>

    <div class="sdx-panel" data-animate="fade-up" markdown="1">

<div class="sdx-chapter-hero" aria-hidden="true">
  <img
    class="sdx-chapter-hero-img"
    src="{{ '/assets/images/AI_2.png' | relative_url }}"
    alt=""
    loading="lazy"
    decoding="async"
  />
  <div class="sdx-chapter-hero-caption">
    <span class="sdx-chapter-hero-kicker">Final</span>
    <span class="sdx-chapter-hero-title">What the Market Really Prices</span>
  </div>
</div>

We started with a question: **When history happens, does the market react right away, or only once everyone knows it was history?**

After analyzing 42 innovations across 50+ companies, we have an answer:

## **It depends.**

---

### The Five Laws of Innovation Footprints

**1. Compute infrastructure is priced early, but only when demand is visible.**

NVIDIA's V100 produced instant footprints because AI demand was already growing. CUDA produced almost nothing, because in 2007, no one knew what to do with it.

**2. Consumer products are priced slowly, even when everyone is watching.**

The iPhone, iPod, and AirPods all faced skepticism on launch day. Consumer adoption takes time to prove itself.

**3. Healthcare innovations depend on binary regulatory gates.**

FDA approvals create clear footprints. When regulators say yes, uncertainty collapses instantly.

**4. AI shocks move whole ecosystems, not individual stocks.**

ChatGPT reshaped the valuation of every AI-adjacent company. The "winner ratio" is the best measure of transformative AI events.

**5. Hype and substance produce different patterns.**

Tesla events show that spectacle can create short-term volatility without sustained recognition.

---

### The Final Insight

<p class="sdx-note">PLACEHOLDER: Insert Combined Framework visualization (data/pattern_07_combined_framework.png).</p>

Markets are not oracles. They don't see the future clearly. But they're not blind either.

Innovation leaves footprints, some instant, some slow, some illusory. The key is knowing which type you're looking at.

> **Some futures are priced in hours. Others take quarters. And some are never priced at the moment you'd expect.**

Innovation walks through the snow of market prices, leaving footprints. Our job is to learn to read them.

---

## Thank You for Reading

**Team:** SwissDataExplorers 2025 | **Course:** Applied Data Analysis, EPFL

**Data Sources:** Kaggle Stock Market Dataset (1962-2020), Yahoo Finance (2020-2024 extension), Official company newsrooms

---

## Interactive Appendix

**FLOURISH VISUALIZATIONS:**

1. Timeline of All Innovation Events
2. Apple Events Line Chart Race
3. Innovation Sector Bar Chart Race
4. Healthcare Innovations Comparison
5. Innovation Score Explorer
</div>

  </div>
</section>

<div class="modal sdx-modal" id="sdx-chapters-modal" aria-hidden="true">
  <div class="modal-background" data-sdx-modal-close></div>
  <div class="modal-card" role="dialog" aria-modal="true" aria-label="Chapter navigation">
    <header class="modal-card-head">
      <p class="modal-card-title">Jump to a section</p>
      <button class="delete" aria-label="close" data-sdx-modal-close></button>
    </header>
    <section class="modal-card-body content">
      <div class="sdx-modal-grid">
        <div class="sdx-modal-box">
          <h4 class="title is-6" style="margin:0;">Acts</h4>
          <div class="sdx-modal-links">
            <a class="sdx-chapter-link" href="#intro"><span><span class="sdx-kicker">Act 0</span><br><span class="sdx-label">Intro</span></span><span class="sdx-kicker">#intro</span></a>
            <a class="sdx-chapter-link" href="#cast"><span><span class="sdx-kicker">Act I</span><br><span class="sdx-label">Meet the Cast</span></span><span class="sdx-kicker">#cast</span></a>
            <a class="sdx-chapter-link" href="#method"><span><span class="sdx-kicker">Act II</span><br><span class="sdx-label">The Detective Method</span></span><span class="sdx-kicker">#method</span></a>
            <a class="sdx-chapter-link" href="#case-files"><span><span class="sdx-kicker">Act III</span><br><span class="sdx-label">Case Files</span></span><span class="sdx-kicker">#case-files</span></a>
            <a class="sdx-chapter-link" href="#archetypes"><span><span class="sdx-kicker">Act IV</span><br><span class="sdx-label">Archetypes</span></span><span class="sdx-kicker">#archetypes</span></a>
            <a class="sdx-chapter-link" href="#what-prices"><span><span class="sdx-kicker">Act V</span><br><span class="sdx-label">Signature Framework</span></span><span class="sdx-kicker">#what-prices</span></a>
            <a class="sdx-chapter-link" href="#act-vi"><span><span class="sdx-kicker">Act VI</span><br><span class="sdx-label">Validation</span></span><span class="sdx-kicker">#act-vi</span></a>
            <a class="sdx-chapter-link" href="#conclusion"><span><span class="sdx-kicker">Final</span><br><span class="sdx-label">Conclusion</span></span><span class="sdx-kicker">#conclusion</span></a>
          </div>
        </div>

        <div class="sdx-modal-box">
          <h4 class="title is-6" style="margin:0;">Chapters</h4>
          <div class="sdx-modal-links">
            <a class="sdx-chapter-link" href="#chapter-apple"><span><span class="sdx-kicker">Chapter 1</span><br><span class="sdx-label">Apple</span></span><span class="sdx-kicker">#chapter-apple</span></a>
            <a class="sdx-chapter-link" href="#chapter-nvidia"><span><span class="sdx-kicker">Chapter 2</span><br><span class="sdx-label">NVIDIA</span></span><span class="sdx-kicker">#chapter-nvidia</span></a>
            <a class="sdx-chapter-link" href="#chapter-tesla"><span><span class="sdx-kicker">Chapter 3</span><br><span class="sdx-label">Tesla</span></span><span class="sdx-kicker">#chapter-tesla</span></a>
            <a class="sdx-chapter-link" href="#chapter-ai"><span><span class="sdx-kicker">Chapter 4</span><br><span class="sdx-label">Innovation Stack</span></span><span class="sdx-kicker">#chapter-ai</span></a>
            <a class="sdx-chapter-link" href="#chapter-biotech"><span><span class="sdx-kicker">Chapter 5</span><br><span class="sdx-label">Biotech and Health</span></span><span class="sdx-kicker">#chapter-biotech</span></a>
            <a class="sdx-chapter-link" href="#ai-era"><span><span class="sdx-kicker">Appendix</span><br><span class="sdx-label">Interactive Appendix</span></span><span class="sdx-kicker">#ai-era</span></a>
          </div>
          <p class="sdx-modal-hint">
            Tip: click a section, the modal closes and the page scrolls there.
          </p>
        </div>
      </div>
    </section>

</div>
</div>

<div>
  <button class="sdx-back-to-top" id="sdx-back-to-top" type="button" aria-label="Back to top" title="Back to top">
    <svg viewBox="0 0 24 24" aria-hidden="true" focusable="false">
      <path fill="currentColor" d="M12 5.5l7 7-1.4 1.4L13 9.3V20h-2V9.3L6.4 13.9 5 12.5l7-7z"></path>
    </svg>
  </button>
</div>

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
      { threshold: 0.01, rootMargin: "0px 0px 12% 0px" }
    );
    animated.forEach((el) => obs.observe(el));
  } else {
    animated.forEach((el) => el.classList.add("animate-in"));
  }

  const backToTop = document.getElementById("sdx-back-to-top");
  if (backToTop) {
    const prefersReducedMotion =
      window.matchMedia && window.matchMedia("(prefers-reduced-motion: reduce)").matches;

    const updateBackToTop = () => {
      if (window.scrollY > 700) {
        backToTop.classList.add("is-visible");
      } else {
        backToTop.classList.remove("is-visible");
      }
    };

    let ticking = false;
    window.addEventListener(
      "scroll",
      () => {
        if (!ticking) {
          ticking = true;
          window.requestAnimationFrame(() => {
            ticking = false;
            updateBackToTop();
          });
        }
      },
      { passive: true }
    );

    backToTop.addEventListener("click", () => {
      window.scrollTo({ top: 0, behavior: prefersReducedMotion ? "auto" : "smooth" });
    });

    updateBackToTop();
  }

  const chaptersModal = document.getElementById("sdx-chapters-modal");
  const navbarStart = document.querySelector(".navbar .navbar-menu .navbar-start");
  if (chaptersModal && navbarStart && !document.getElementById("sdx-chapters-trigger")) {
    const trigger = document.createElement("a");
    trigger.id = "sdx-chapters-trigger";
    trigger.className = "navbar-item";
    trigger.href = "#chapters";
    trigger.textContent = "Chapters";
    const navItems = navbarStart.querySelectorAll("a.navbar-item");
    if (navItems.length >= 2) {
      navbarStart.insertBefore(trigger, navItems[1]);
    } else {
      navbarStart.appendChild(trigger);
    }
  }

  const openChaptersModal = () => {
    if (!chaptersModal) return;
    chaptersModal.classList.add("is-active");
    document.documentElement.classList.add("is-clipped");
    const closeBtn = chaptersModal.querySelector("button[data-sdx-modal-close]");
    if (closeBtn) closeBtn.focus({ preventScroll: true });
  };

  const closeChaptersModal = () => {
    if (!chaptersModal) return;
    chaptersModal.classList.remove("is-active");
    document.documentElement.classList.remove("is-clipped");
  };

  const chaptersTrigger = document.getElementById("sdx-chapters-trigger");
  if (chaptersModal && chaptersTrigger) {
    chaptersTrigger.addEventListener("click", (e) => {
      e.preventDefault();
      openChaptersModal();
    });

    chaptersModal.addEventListener("click", (e) => {
      const closeTarget = e.target.closest("[data-sdx-modal-close]");
      if (closeTarget) {
        e.preventDefault();
        closeChaptersModal();
        return;
      }

      const link = e.target.closest("a[href^=\"#\"]");
      if (link) {
        e.preventDefault();
        const hash = link.getAttribute("href");
        closeChaptersModal();
        const target = hash ? document.querySelector(hash) : null;
        if (target) {
          target.scrollIntoView({ behavior: "smooth", block: "start" });
          history.replaceState(null, "", hash);
        }
      }
    });

    document.addEventListener("keydown", (e) => {
      if (e.key === "Escape" && chaptersModal.classList.contains("is-active")) {
        closeChaptersModal();
      }
    });
  }

  const scoreIframes = Array.from(document.querySelectorAll("iframe.sdx-embed-iframe"));
  const iframeResizers = [];
  const MIN_IFRAME_HEIGHT = 420;
  const HEIGHT_EPSILON = 8;

  const getIframeDocument = (iframe) =>
    iframe.contentDocument || (iframe.contentWindow && iframe.contentWindow.document);

  const getExplicitHeight = (iframe) => {
    const raw = iframe.getAttribute("data-sdx-height");
    const value = raw ? parseInt(raw, 10) : NaN;
    return Number.isFinite(value) && value > 0 ? value : 0;
  };

  const getBodyMargin = (doc) => {
    try {
      if (!doc || !doc.body || !doc.defaultView) return 0;
      const style = doc.defaultView.getComputedStyle(doc.body);
      const top = parseFloat(style.marginTop) || 0;
      const bottom = parseFloat(style.marginBottom) || 0;
      return top + bottom;
    } catch (error) {
      return 0;
    }
  };

  const computeEmbedHeight = (doc) => {
    const bodyMargin = getBodyMargin(doc);
    const plotlyDivs = doc.querySelectorAll(".plotly-graph-div");
    if (plotlyDivs.length) {
      let maxBottom = 0;
      let hasFluidPlotly = false;
      plotlyDivs.forEach((el) => {
        const inlineHeight = el && el.style ? String(el.style.height || "").trim() : "";
        if (inlineHeight && inlineHeight.includes("%")) {
          hasFluidPlotly = true;
          return;
        }

        let height = el.offsetHeight || 0;
        const pxMatch = inlineHeight.match(/^(\d+(?:\.\d+)?)px$/);
        if (pxMatch) height = parseFloat(pxMatch[1]);

        const bottom = (el.offsetTop || 0) + height;
        if (bottom > maxBottom) maxBottom = bottom;
      });
      if (maxBottom) return maxBottom + bodyMargin;
    }

    const body = doc.body;
    if (!body) return 0;

    const scrollHeight = Math.max(
      doc.documentElement ? doc.documentElement.scrollHeight : 0,
      body.scrollHeight || 0
    );
    if (scrollHeight) return scrollHeight;

    const children = Array.from(body.children || []);
    if (children.length) {
      let maxBottom = 0;
      children.forEach((el) => {
        const bottom = (el.offsetTop || 0) + (el.offsetHeight || 0);
        if (bottom > maxBottom) maxBottom = bottom;
      });
      if (maxBottom) return maxBottom + bodyMargin;
    }

    return 0;
  };

  const setupIframeAutoResize = (iframe) => {
    let resizeObserver;
    const explicitHeight = getExplicitHeight(iframe);
    if (explicitHeight) {
      iframe.style.height = `${explicitHeight}px`;
      return;
    }

    const resize = () => {
      try {
        const doc = getIframeDocument(iframe);
        if (!doc) return;

        let nextHeight = computeEmbedHeight(doc);
        if (!nextHeight) return;
        nextHeight = Math.max(nextHeight, MIN_IFRAME_HEIGHT);

        const currentHeight = Math.round(iframe.getBoundingClientRect().height);
        if (Math.abs(nextHeight - currentHeight) <= HEIGHT_EPSILON) return;

        iframe.style.height = `${Math.round(nextHeight)}px`;
      } catch (error) {
        // Cross-origin or blocked (e.g., file://), ignore.
      }
    };

    const scheduleResizes = () => {
      [0, 120, 300, 700, 1200, 2000].forEach((delay) => setTimeout(resize, delay));
    };

    iframe.addEventListener("load", () => {
      scheduleResizes();
      try {
        if ("ResizeObserver" in window) {
          const doc = getIframeDocument(iframe);
          if (!doc) return;
          const plotlyDiv = doc.querySelector(".plotly-graph-div");
          const isFluidPlotly =
            plotlyDiv && plotlyDiv.style && String(plotlyDiv.style.height || "").includes("%");
          const target = isFluidPlotly ? doc.body : plotlyDiv || doc.body;
          if (!target) return;
          resizeObserver = new ResizeObserver(() => window.requestAnimationFrame(resize));
          resizeObserver.observe(target);
        }
      } catch (error) {
        // Cross-origin or unsupported, ignore.
      }
    });

    iframeResizers.push(resize);
    scheduleResizes();
  };

  scoreIframes.forEach(setupIframeAutoResize);

  window.addEventListener("resize", () => {
    iframeResizers.forEach((resize) => resize());
  });
});
</script>
