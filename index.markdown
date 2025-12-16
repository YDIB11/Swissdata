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
  align-items: stretch;
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
          <div class="sdx-pill"><span>Event studies &bull; innovation &bull; stock markets</span></div>
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

  <p class="sdx-note">PLACEHOLDER: Add a combined timeline visualization of all analyzed events.</p>

The breadth of our investigation is intentional. Innovation takes many forms, and we wanted to understand whether the market recognizes different types of breakthroughs in different ways. A consumer gadget like the iPod is visible to everyone, millions saw the keynote, tried the product, formed opinions. But a computing platform like CUDA is invisible to most people, even as it quietly enables everything from video games to self-driving cars to ChatGPT.

| Domain            | Companies/Events                                                 | Time Period | Examples                                                             |
| ----------------- | ---------------------------------------------------------------- | ----------- | -------------------------------------------------------------------- |
| Consumer Tech     | Apple (8 events)                                                 | 2001-2023   | iPod, iPhone, iPad, AirPods, M1 Chip, Vision Pro                     |
| Compute Platforms | NVIDIA (8 events)                                                | 2007-2024   | CUDA, DGX-1, V100, Blackwell B200                                    |
| Electric Vehicles | Tesla (8 events)                                                 | 2014-2024   | Autopilot, Model 3, Cybertruck, FSD v12                              |
| Innovation Stack  | Top 25 market-cap leaders across the innovation stack (8 events) | 2006-2023   | AWS EC2, iPhone, App Store, Android, Azure, Touch ID, M1, Vision Pro |
| Healthcare        | Top 25 Healthcare Companies (10 events)                          | 2020-2024   | mRNA vaccines, GLP-1 drugs, CRISPR therapy                           |

Each event in this table represents a moment when _someone_ believed they were witnessing history. Our job is to determine whether Wall Street agreed, and when.

  </div>
<div class="sdx-panel" data-animate="fade-up">
<div class="flourish-embed flourish-timeline" data-src="visualisation/26798005"><script src="https://public.flourish.studio/resources/embed.js"></script><noscript><img src="https://public.flourish.studio/visualisation/26798005/thumbnail" width="100%" alt="timeline visualization" /></noscript></div>
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

We anchored this lens around **eight turning point innovations** that moved multiple companies at once:

| Event                       | Date         | What Happened                        | Expected Beneficiaries  |
| --------------------------- | ------------ | ------------------------------------ | ----------------------- |
| **AWS EC2 Launch**          | Aug 25, 2006 | Cloud compute becomes on demand      | AMZN, MSFT, GOOGL, ORCL |
| **iPhone Launch**           | Jun 29, 2007 | Mobile computing goes mainstream     | AAPL, GOOGL, QCOM, TSM  |
| **App Store Launch**        | Jul 10, 2008 | The app economy is born              | AAPL, GOOGL, ADBE, CRM  |
| **Android Launch**          | Sep 23, 2008 | Open mobile platform scales globally | GOOGL, QCOM, AMZN, META |
| **Microsoft Azure Launch**  | Feb 1, 2010  | Cloud becomes enterprise default     | MSFT, AMZN, ORCL, IBM   |
| **iPhone 5S Touch ID**      | Sep 20, 2013 | Biometrics becomes default UX        | AAPL, QCOM, GOOGL, MSFT |
| **M1 Chip Announcement**    | Nov 10, 2020 | Apple silicon breaks the Intel era   | AAPL, TSM, INTC, AMD    |
| **Vision Pro Announcement** | Jun 5, 2023  | Spatial computing arrives            | AAPL, TSM, QCOM         |

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

    <div class="sdx-panel sdx-formula-block" data-animate="fade-up">
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

      <h4 class="title is-5" style="margin-top:1.4rem;">Planned extension, market-adjusted impact</h4>
      <p class="sdx-note" style="margin-top:0.6rem;">
        PLACEHOLDER: Add a benchmark (market index) and compute abnormal returns and CAR.
      </p>
      <div class="sdx-formula-grid sdx-formula-grid-addon">
        <div class="sdx-formula-card">
          <h4>Abnormal return</h4>
          <div class="formula">\( AR_t = R_t - R_{m,t} \)</div>
          <p>The event-day surprise after subtracting the market's move (a simple market-adjusted baseline).</p>
        </div>
        <div class="sdx-formula-card">
          <h4>CAR</h4>
          <div class="formula">\( CAR_{[a,b]} = \sum_{t=a}^{b} AR_t \)</div>
          <p>Cumulative abnormal return, the footprint across the full window.</p>
        </div>
      </div>
    </div>

    <div class="sdx-panel" data-animate="fade-up">
      <div class="content" markdown="1">

### The Mathematics of Market Footprints

The checklist above is the compact version. This panel shows the exact math we compute in code, with plain-language interpretation.

#### 1) Return and log return

$$R_t = \left(\frac{P_t - P_{t-1}}{P_{t-1}}\right) \times 100$$

Daily return is the percentage move from yesterday's close \(P\_{t-1}\) to today's close \(P_t\).

Log return is a closely related measure that adds cleanly across time:

$$r_t = \ln\!\left(\frac{P_t}{P_{t-1}}\right) \times 100$$

Example: if a stock closed at $150 yesterday and closes at $153 today, the daily return is:

$$\frac{153 - 150}{150} \times 100 = 2\%$$

#### 2) Planned extension, abnormal return and CAR

To isolate the event from the market's noise, we can add a market-adjusted baseline (next upgrade on our roadmap):

$$AR_t = R_t - R_{m,t}$$

Here, \(R\_{m,t}\) is the benchmark return (a broad market index) on the same day.
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

In plain English: compare average volume after the event \(\bar{V}_{post}\) to average volume before \(\bar{V}_{pre}\), expressed as a percentage.

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

<iframe
  id="innovation-score-iframe"
  src="{{ '/assets/ipod_launch_plotly_dark.html' | relative_url }}"
  title="Innovation score explorer"
  width="100%"
  height="950"
  frameborder="0"
  scrolling="no"
  style="display:block; border:0; overflow:hidden;"
  loading="lazy"
></iframe>

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

<p class="sdx-note">PLACEHOLDER: Insert Apple iPhone Launch cumulative return chart (apple_event_analysis.ipynb, Step 5 visualization).</p>

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

<p class="sdx-note">PLACEHOLDER: Insert Apple M1 Chip cumulative return chart (apple_event_analysis.ipynb, Step 5 visualization).</p>

The M1 story shows that markets _can_ recognize platform shifts, it just takes time for the implications to sink in. The event-day return was essentially zero. But over the following month, as investors digested what Apple Silicon meant for margins, performance, and competitive positioning, a substantial revaluation occurred.

---

### Apple Event Summary: All 8 Events Compared

When we step back and look at all eight Apple events together, a striking pattern emerges:

<iframe src="assets/apple_cumulative_returns_interactive.html" width="100%" height="600" frameborder="0"></iframe>

<iframe src="assets/apple_plotly_05_30day_cumulative_returns.html" width="100%" height="600" frameborder="0"></iframe>

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

<p class="sdx-note">PLACEHOLDER: Flourish - Apple Events Line Chart Race (data/apple_event_exports/09_flourish_line_race.csv).</p>
</div>
    </div>

    <div class="sdx-panel" id="chapter-nvidia" data-animate="fade-up">
      <h2 class="title is-4">Chapter 2 - NVIDIA: The Infrastructure Play</h2>
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

<iframe src="assets/cuda_launch_plotly_dark.html" width="100%" height="950" frameborder="0"></iframe>

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

  <iframe
  id="innovation-score-iframe"
  src="{{ '/assets/tesla_v100_launch_plotly_dark.html' | relative_url }}"
  title="Innovation score explorer"
  width="100%"
  height="1000"
  frameborder="0"
  scrolling="no"
  style="display:block; border:0; overflow:hidden;"
  loading="lazy"
></iframe>

This is what we call an **"Instant Footprint"**, immediate, sustained, unmistakable recognition. The market understood that NVIDIA had created the essential hardware for the AI revolution. No slow burn, no gradual awakening. The footprint was there on day one.

Why the difference between CUDA (ignored) and V100 (celebrated)? Context. In 2007, deep learning didn't exist as a commercial force. In 2017, it was the hottest technology in the world, and demand for AI computing was exploding. The market could see the V100's value because it could see the demand.

---

### DGX-1 Launch (April 5, 2016): When GPUs Become a Product

By 2016, deep learning had escaped the lab, but building the hardware stack was still a craft project. If you were a researcher or a startup, you needed GPUs, drivers, CUDA libraries, frameworks, and a lot of time making everything work together.

DGX-1 was NVIDIA's attempt to productize the whole thing. Not a single chip, but a deep learning system in a box, built for one job, train neural networks fast.

The market reaction was understated on day one:

**Event day return: -0.14%**  
**30-day return: +18.27%**

  <iframe
  id="innovation-score-iframe"
  src="{{ '/assets/dgx_1_launch_plotly_detailed.html' | relative_url }}"
  title="Innovation score explorer"
  width="100%"
  height="1000"
  frameborder="0"
  scrolling="no"
  style="display:block; border:0; overflow:hidden;"
  loading="lazy"
></iframe>

This is a different kind of footprint. Not a loud spike, but a quiet pivot, NVIDIA signaling that it was not just selling gaming parts anymore, it was building an AI platform.

---

### H100 Hopper Launch (March 22, 2022): Right Chip, Wrong Tape

In March 2022, NVIDIA introduced Hopper, the H100, a GPU designed to be the workhorse of modern AI training. On paper, this should have been another clean, instant footprint.

Instead, the market did the opposite:

**Event day return: -0.79%**  
**30-day return: -23.34%**

  <iframe
  id="innovation-score-iframe"
  src="{{ '/assets/h100_hopper_launch_plotly_detailed.html' | relative_url }}"
  title="Innovation score explorer"
  width="100%"
  height="1000"
  frameborder="0"
  scrolling="no"
  style="display:block; border:0; overflow:hidden;"
  loading="lazy"
></iframe>

The explanation is not that the innovation was weak. It is timing. 2022 was a brutal tech drawdown. Rates were rising, growth multiples were compressing, and investors were de-risking. Even a real breakthrough had to fight for oxygen.

Hopper matters in hindsight because it shows a hard truth about market recognition. Sometimes the market sees the future, and still refuses to pay for it, because the present is on fire.

---

### NVIDIA Event Summary: All 8 Events Compared

<iframe src="assets/nvidia_cumulative_returns_interactive.html" width="100%" height="600" frameborder="0"></iframe>
<iframe src="assets/nvidia_plotly_05_30day_cumulative_returns.html" width="100%" height="800" frameborder="0"></iframe>

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

</div>
</div>

    <div class="sdx-panel" id="chapter-tesla" data-animate="fade-up">
      <h2 class="title is-4">Chapter 3 - Tesla: Hype, Skepticism, and Spectacle</h2>
      <div class="content" markdown="1">

Tesla defies easy categorization. It's not just a car company, it's a phenomenon, a cultural touchstone, a perpetual drama playing out in real-time across social media, financial news, and Elon Musk's Twitter feed.

This creates unique challenges for understanding market recognition. With Apple, we're analyzing how markets respond to technology. With NVIDIA, we're analyzing how markets respond to infrastructure demand. With Tesla, we're analyzing how markets respond to **narrative, spectacle, and the complex psychology of believing in the future.**

---

### Autopilot Announcement (October 10, 2014): When Tesla Starts Selling Software

Tesla's Autopilot announcement was not a new car, it was a new identity. The company was asking investors to see Tesla as more than an automaker, a sensor stack, a computer on wheels, and a software roadmap that could compound over time.

The market was not impressed on day one:

**Event day return: -7.82%**  
**30-day return: +2.48%**

  <iframe
  id="innovation-score-iframe"
  src="{{ '/assets/tesla_event_exports/autopilot_announcement_plotly_detailed.html' | relative_url }}"
  title="Innovation score explorer"
  width="100%"
  height="1000"
  frameborder="0"
  scrolling="no"
  style="display:block; border:0; overflow:hidden;"
  loading="lazy"
></iframe>

That combination is classic Tesla. The headline triggers fear, regulation risk, liability, execution, but the idea lingers, and the stock drifts back as investors reprice the narrative.

---

### Model 3 First Deliveries (July 28, 2017): Proof, and the Start of Production Hell

The Model 3 was Tesla's make or break product. Deliveries meant the promise was real, but they also opened the harder question, can Tesla scale without breaking?

The footprint was subtle:

**Event day return: +0.18%**  
**30-day return: +8.54%**

  <iframe
  id="innovation-score-iframe"
  src="{{ '/assets/tesla_event_exports/model_3_first_deliveries_plotly_detailed.html' | relative_url }}"
  title="Innovation score explorer"
  width="100%"
  height="1000"
  frameborder="0"
  scrolling="no"
  style="display:block; border:0; overflow:hidden;"
  loading="lazy"
></iframe>

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

  <iframe
  id="innovation-score-iframe"
  src="{{ '/assets/tesla_event_exports/cybertruck_reveal_plotly_dark.html' | relative_url }}"
  title="Innovation score explorer"
  width="100%"
  height="1000"
  frameborder="0"
  scrolling="no"
  style="display:block; border:0; overflow:hidden;"
  loading="lazy"
></iframe>

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

  <iframe
  id="innovation-score-iframe"
  src="{{ '/assets/tesla_event_exports/tesla_bot_announcement_plotly_detailed.html' | relative_url }}"
  title="Innovation score explorer"
  width="100%"
  height="1000"
  frameborder="0"
  scrolling="no"
  style="display:block; border:0; overflow:hidden;"
  loading="lazy"
></iframe>

  <iframe
  id="innovation-score-iframe"
  src="{{ '/assets/tesla_event_exports/dojo_supercomputer_announcement_plotly_detailed.html' | relative_url }}"
  title="Innovation score explorer"
  width="100%"
  height="1000"
  frameborder="0"
  scrolling="no"
  style="display:block; border:0; overflow:hidden;"
  loading="lazy"
></iframe>

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

<iframe src="assets/tesla_cumulative_returns_interactive.html" width="100%" height="600" frameborder="0"></iframe>

<iframe src="assets/tesla_plotly_05_30day_cumulative_returns.html" width="100%" height="600" frameborder="0"></iframe>

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

</div>
</div>

    <div class="sdx-panel" id="chapter-ai" data-animate="fade-up">
      <h2 class="title is-4">Chapter 4 - Innovation Stack: When Everything Moves Together</h2>
      <div class="content" markdown="1">

This chapter is where our method stops being a single-company microscope and becomes a wide-angle lens.

Until now we followed protagonists, Apple on a stage, NVIDIA in the datacenter, Tesla in the spotlight. In this chapter, the protagonist is the whole industry. The camera pulls back.

When an innovation hits the innovation stack, it rarely stays inside one ticker. It spreads. Partners, suppliers, competitors, and the platforms that will be disrupted all move, sometimes in opposite directions. That is what makes this chapter different. We stop asking, "did one stock jump?" and start asking, "did the market move together?"

To measure that, we track a basket of the **25 largest, most liquid market-cap leaders** across the innovation stack around the same milestone dates and look at two signals:

- the sector average return over the event window
- the <a href="#winner-ratio-definition"><strong>Winner Ratio</strong></a>, how many of the 25 finish the window positive

<div class="flourish-embed flourish-network" data-src="visualisation/26742106"><script src="https://public.flourish.studio/resources/embed.js"></script><noscript><img src="https://public.flourish.studio/visualisation/26742106/thumbnail" width="100%" alt="network visualization" /></noscript></div>

---

Most of the chapter specific numbers below are still being computed. Where you see **(N/A)**, treat it as a placeholder that tells you exactly what metric belongs there.

---

### AWS EC2 Launch (August 25, 2006): The Cloud Becomes a Utility

Before EC2, compute was something you bought. After EC2, compute became something you rented by the hour. That single shift rewired the stack, startups could scale without owning servers, enterprises could move workloads without building data centers, and software companies could sell subscriptions instead of boxes.

- Winner Ratio: **(N/A)**
- Sector average 30-day return: **(N/A)**

<p class="sdx-note">PLACEHOLDER: Insert 25-company cumulative return overlay for the EC2 launch window.</p>
<p class="sdx-note">PLACEHOLDER: Insert cloud cohort breakdown (AMZN, MSFT, GOOGL, ORCL, IBM) vs the rest of the basket during the EC2 window.</p>

---

### iPhone Launch (June 29, 2007): The Pocket Computer Era Begins

The iPhone did not just improve a phone. It turned the phone into a computer you carry. That changed consumer behavior, ad distribution, chip demand, and the competitive map for an entire decade.

- Winner Ratio: **(N/A)**
- Sector average 30-day return: **(N/A)**

<p class="sdx-note">PLACEHOLDER: Insert 25-company return dispersion plot for the iPhone launch window (who got pulled up, who got left behind).</p>

---

### App Store Launch (July 10, 2008): Software Becomes a Marketplace

The App Store turned software into an economy. It created the idea that distribution is a platform advantage, not a marketing problem. It also created a new kind of company, one that lives entirely inside someone else's ecosystem.

- Winner Ratio: **(N/A)**
- Sector average 30-day return: **(N/A)**

<p class="sdx-note">PLACEHOLDER: Insert a platform vs tools comparison for the App Store window (AAPL, GOOGL, ADBE, CRM) to show who benefited from the new software distribution model.</p>

---

### Android Launch (September 23, 2008): The Open Mobile Stack

Android made smartphones a volume market. By being open, it scaled. By scaling, it forced every platform, chip, and app business to adapt to a world where mobile is the default surface.

- Winner Ratio: **(N/A)**
- Sector average 30-day return: **(N/A)**

<p class="sdx-note">PLACEHOLDER: Insert iPhone vs Android era split analysis across platforms and chip suppliers (GOOGL, QCOM, AAPL, TSM) around the Android launch.</p>

---

### Microsoft Azure Launch (February 1, 2010): Cloud Goes Enterprise

Azure made the cloud safe for corporate IT. It is the moment cloud stopped being a startup story and became a boardroom story. Once enterprises move, the whole stack moves, databases, operating systems, security, and productivity software.

- Winner Ratio: **(N/A)**
- Sector average 30-day return: **(N/A)**

<p class="sdx-note">PLACEHOLDER: Insert enterprise software cohort comparison (MSFT, ORCL, IBM, CRM, NOW) for the Azure launch window.</p>

---

### iPhone 5S Touch ID (September 20, 2013): Security Becomes Frictionless

Touch ID is a small sensor with a big effect. It made biometrics mainstream, which made payments, authentication, and mobile trust easier. The market impact is subtle, because it is less about one product and more about what becomes possible afterwards.

- Winner Ratio: **(N/A)**
- Sector average 30-day return: **(N/A)**

<p class="sdx-note">PLACEHOLDER: Insert post-event slow-burn chart for Touch ID (does the footprint show up over weeks rather than day 0).</p>

---

### M1 Chip Announcement (November 10, 2020): A Platform Shift Hidden Inside a Laptop

Apple's M1 was not a spec sheet update. It was a break with Intel and a bet that control of the stack, from silicon to software, beats buying performance from someone else. For markets, this is the kind of event where the footprint should show up across a mini supply chain, Apple as the integrator, TSM as the foundry, Intel as the displaced default.

- Winner Ratio: **(N/A)**
- Sector average 30-day return: **(N/A)**

<p class="sdx-note">PLACEHOLDER: Insert 25-company heatmap for the M1 window (winners vs losers across chips, platforms, and software).</p>
<p class="sdx-note">PLACEHOLDER: Insert a focused comparison panel for AAPL, INTC, AMD, TSM around M1 (price, volume, cumulative return).</p>

---

### Vision Pro Announcement (June 5, 2023): A New Interface, a Big Question Mark

Vision Pro is the rare product launch that tries to create a new category. Markets like categories, but only when they turn into ecosystems. The early footprint here is less about day 0 hype and more about whether the stack believes spatial computing becomes a platform, or stays a premium niche.

- Winner Ratio: **(N/A)**
- Sector average 30-day return: **(N/A)**

<p class="sdx-note">PLACEHOLDER: Insert Vision Pro window heatmap (AAPL, QCOM, TSM and the full basket) with cumulative returns.</p>
<p class="sdx-note">PLACEHOLDER: Insert a small multiples grid of suppliers vs platforms around the Vision Pro announcement.</p>

---

### Innovation Stack Summary: Eight Events, One Map

| Event      | Date     | Sector Return | Winner Ratio |
| ---------- | -------- | ------------- | ------------ |
| AWS EC2    | Aug 2006 | (N/A)         | (N/A)        |
| iPhone     | Jun 2007 | (N/A)         | (N/A)        |
| App Store  | Jul 2008 | (N/A)         | (N/A)        |
| Android    | Sep 2008 | (N/A)         | (N/A)        |
| Azure      | Feb 2010 | (N/A)         | (N/A)        |
| Touch ID   | Sep 2013 | (N/A)         | (N/A)        |
| M1         | Nov 2020 | (N/A)         | (N/A)        |
| Vision Pro | Jun 2023 | (N/A)         | (N/A)        |

The point of this chapter is not to crown a single winner. It is to show that when the stack is hit, the footprint is usually distributed, and often asymmetric.

Next, we leave the innovation stack and enter a domain where the rules are even stricter, healthcare, where a single approval can rewrite the future overnight.

</div>
    </div>

    <div class="sdx-panel" id="chapter-biotech" data-animate="fade-up">
      <h2 class="title is-4">Chapter 5 - Healthcare: The Power of Regulatory Moments</h2>
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

<p class="sdx-note">PLACEHOLDER: Insert Healthcare Sector mRNA approval visualization (healthcare_sector_event_analysis.ipynb, Step 6 visualization).</p>

The returns look modest, but context matters. This was during the chaotic post-election, mid-pandemic market. Vaccine optimism was already partially priced in. And the impact wasn't uniform: Pfizer saw different movement than surgical device makers.

---

### The GLP-1 Revolution: A New Category Emerges

Perhaps no healthcare innovation has reshaped markets more dramatically than GLP-1 drugs for weight loss. Drugs like Wegovy, Mounjaro, and Zepbound didn't just help diabetics manage blood sugar, they produced unprecedented weight loss in clinical trials.

The implications extend far beyond pharmaceuticals. Food companies must reconsider their futures. Weight Watchers restructured its entire business model. Fitness chains adjusted projections. Medical device makers serving obese patients reconsidered long-term demand.

**Zepbound Obesity Launch (November 8, 2023):**

- Sector average 30-day return: **+7.73%**
- Sector median 30-day return: **+7.71%**

<p class="sdx-note">PLACEHOLDER: Insert Healthcare Sector GLP-1 impact visualization (healthcare_sector_event_analysis.ipynb, Step 6 visualization).</p>

The GLP-1 revolution creates clear footprints, not just for drug makers like Eli Lilly and Novo Nordisk, but for entire adjacent industries.

---

### CRISPR Approval (December 8, 2023): Gene Editing Becomes Real

For decades, CRISPR existed in science fiction and research labs. The ability to edit genes precisely, to potentially cure genetic diseases at their source, seemed perpetually futuristic.

On December 8, 2023, the future arrived. The FDA approved Casgevy, the first CRISPR gene-editing therapy, for treating sickle cell disease. A technology that had won Nobel Prizes was now helping actual patients.

Sector average 30-day return: **+6.37%**

<p class="sdx-note">PLACEHOLDER: Insert Healthcare Sector CRISPR impact visualization (healthcare_sector_event_analysis.ipynb, Step 6 visualization).</p>

The market recognized CRISPR's approval as transformative, not just for Vertex (which partnered on Casgevy) but for the entire biotechnology sector. Gene editing had crossed from possibility to reality.

---

### Healthcare Event Summary

<p class="sdx-note">PLACEHOLDER: Insert Healthcare Events comparison chart showing all 10 events (healthcare_sector_event_analysis.ipynb, comparison visualization).</p>

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

<p class="sdx-note">PLACEHOLDER: Insert Event Day vs 30-Day Return scatter plot (data/pattern_01_event_day_vs_30d.png).</p>

**When it happens:** Instant footprints appear when an innovation **confirms what sophisticated investors already suspected.** The V100 didn't surprise anyone tracking AI research, it just provided the hardware that everyone knew was needed. The market was primed to price it immediately.

---

### 2. The Slow Burn

Other innovations are initially dismissed or ignored, only to be recognized weeks later. The event-day return is weak or negative, but by day 30, the cumulative return is strongly positive. The market misses the significance at first, then gradually catches on.

**Classic Examples:**

- Apple iPod: -4.63% day-0, +30.98% over 30 days
- Apple M1 Chip: -0.30% day-0, +12.93% over 30 days
- NVIDIA CUDA: -2.64% day-0, years of delayed recognition

**When it happens:** Slow burns appear when an innovation is **too different to understand immediately.** The iPod wasn't just a better MP3 player, it was the beginning of Apple's transformation into a consumer electronics company. CUDA wasn't just faster graphics, it was the foundation of modern AI. These implications take time to become clear.

---

### 3. The Mirage

Some events create immediate excitement that fades away. Strong initial reaction that reverses over the following weeks, leaving little or negative cumulative return. The market overreacts to spectacle or hype.

**Classic Examples:**

- Tesla Optimus Gen 2 Reveal: +0.96% day-0, -20.21% over 30 days
- Tesla Cybertruck Deliveries Begin: -1.66% day-0, -8.40% over 30 days
- Overhyped competitor announcements

<p class="sdx-note">PLACEHOLDER: Insert three-archetype comparison plot (Instant / Slow Burn / Mirage).</p>

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

Based on our pattern analysis, we built an **Innovation Signature Score** framework, a systematic way to measure how strongly the market recognized any given innovation.

---

## The Innovation Signature Score Formula

For single-company events, we score innovations on five components:

### Component 1: Return Magnitude (0-30 points)

$$\text{Score}_1 = \min(\max(R_{30d}, -15), 30)$$

The 30-day cumulative return, capped to prevent outliers from dominating. Big returns suggest the market eventually recognized value.

### Component 2: Positive Return Bonus (20 points)

If the 30-day return is positive, add 20 points. Direction matters more than magnitude, being positive signals success.

### Component 3: Momentum Sustained (15 points)

If the 30-day return exceeds the event-day return, add 15 points. This captures the Slow Burn pattern, innovations that build momentum over time.

### Component 4: Volatility Stabilization (0-10 points)

If post-event volatility is lower than pre-event volatility, add points. True innovations **resolve uncertainty**, the market figures out what something is worth.

### Component 5: Volume Conviction (0-10 points)

If trading volume increased by more than 20%, add 10 points. Sustained attention suggests genuine interest rather than noise.

---

## Innovation Categories

| Score    | Category          | Interpretation                          |
| -------- | ----------------- | --------------------------------------- |
| 60+      | Transformative    | Clear, sustained market recognition     |
| 40-59    | Strong innovation | Solid recognition with some uncertainty |
| 20-39    | Moderate          | Mixed signals, partial recognition      |
| Under 20 | Weak/Negative     | Market rejected or ignored              |

---

## Top Innovations by Score

<p class="sdx-note">PLACEHOLDER: Insert Innovation Signature Scores bar chart (data/pattern_06_innovation_scores.png).</p>

### Transformative innovations (Score 60+):

| Event                  | Company | Score | 30-Day Return |
| ---------------------- | ------- | ----- | ------------- |
| Cybertruck Reveal      | Tesla   | 80    | +32.19%       |
| Tesla V100 Launch      | NVIDIA  | 75    | +30.71%       |
| iPod Launch            | Apple   | 75    | +30.98%       |
| A100 Ampere Launch     | NVIDIA  | 64    | +14.05%       |
| RTX 2080 Ti Launch     | NVIDIA  | 61    | +15.65%       |
| Tesla Bot Announcement | Tesla   | 60    | +15.11%       |

**The key insight:** The iPod and CUDA, two innovations that seemed minor on announcement day, score as highly as the hyped Cybertruck reveal. Our framework captures both immediate blockbusters and slow-burn transformations.

---

## The Volatility Pattern: A Counterintuitive Finding

One of our most surprising discoveries: **successful innovations tend to reduce post-event volatility.**

<p class="sdx-note">PLACEHOLDER: Insert Volatility Analysis chart (data/pattern_02_volatility_analysis.png).</p>

For events with positive 30-day returns:

- Pre-event volatility: 2.38%
- Post-event volatility: 2.26%
- Change: **-0.12%**

**Interpretation:** True innovations **resolve uncertainty**. Before an announcement, the market doesn't know what to expect. After a successful innovation, price discovery occurs, investors converge on a valuation, and volatility decreases.

</div>

  </div>
</section>

<section class="section sdx-section alt" id="act-vi">
  <div class="container">
    <h2 class="title is-3">Act VI - Test Your Own Innovation</h2>

    <div class="sdx-panel" data-animate="fade-up" markdown="1">

We've built a framework. Now let's make it actionable.

---

## The Innovation Score Calculator

For any innovation event, collect:

- Event-day stock return
- 30-day cumulative return
- Pre-event volatility
- Post-event volatility
- Volume change percentage

Then score:

| Component        | Max Points |
| ---------------- | ---------- |
| Return magnitude | 30         |
| Positive bonus   | 20         |
| Momentum         | 15         |
| Volatility       | 10         |
| Volume           | 10         |
| **Total**        | **85**     |

---

## Validation Results

<p class="sdx-note">PLACEHOLDER: Insert out-of-sample validation results (data/innovation_patterns/out_of_sample_validation.png).</p>

We tested our framework on **13 events** not used in building the model. It successfully identified the category for **11 of 13** test events.

  <iframe
  id="innovation-score-iframe"
  src="{{ '/assets/innovation_score_explorer.html' | relative_url }}"
  title="Innovation score explorer"
  width="100%"
  height="1400"
  frameborder="0"
  scrolling="no"
  style="display:block; border:0; overflow:hidden;"
  loading="lazy"
></iframe>

</div>
  </div>
</section>

<section class="section sdx-section alt" id="ai-era">
  <div class="container">
    <h2 class="title is-3">The AI Era: A Special Section</h2>

    <div class="sdx-panel" data-animate="fade-up" markdown="1">

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
            <a class="sdx-chapter-link" href="#act-vi"><span><span class="sdx-kicker">Act VI</span><br><span class="sdx-label">Test Your Own Innovation</span></span><span class="sdx-kicker">#act-vi</span></a>
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
      { threshold: 0.1, rootMargin: "0px 0px -5% 0px" }
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

  const scoreIframe = document.getElementById("innovation-score-iframe");
  if (scoreIframe) {
    let resizeObserver;
    const resizeScoreIframe = () => {
      try {
        const doc = scoreIframe.contentDocument || scoreIframe.contentWindow.document;
        if (!doc) return;
        const height = Math.max(
          doc.documentElement ? doc.documentElement.scrollHeight : 0,
          doc.body ? doc.body.scrollHeight : 0
        );
        if (height) scoreIframe.style.height = `${height}px`;
      } catch (error) {
        // Cross-origin, ignore.
      }
    };

    scoreIframe.addEventListener("load", () => {
      resizeScoreIframe();
      try {
        if ("ResizeObserver" in window) {
          const doc = scoreIframe.contentDocument || scoreIframe.contentWindow.document;
          if (doc && doc.documentElement) {
            resizeObserver = new ResizeObserver(resizeScoreIframe);
            resizeObserver.observe(doc.documentElement);
          }
        }
      } catch (error) {
        // Cross-origin or unsupported, ignore.
      }
      setTimeout(resizeScoreIframe, 300);
      setTimeout(resizeScoreIframe, 1200);
    });

    window.addEventListener("resize", resizeScoreIframe);
  }
});
</script>
