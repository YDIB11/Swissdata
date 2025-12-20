---
layout: page
title: "References"
subtitle: "Sources, datasets, and asset credits"
permalink: /references/
---

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;600;700&family=Source+Sans+3:wght@400;600;700&display=swap" rel="stylesheet">

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
.content h6,
.title,
.subtitle {
  color: #f7f9ff;
}

.footer { display: none !important; }


a {
  color: var(--muted);
}

a:hover {
  color: #d9e2ff;
}

/* Hide theme hero so we can use our own. */
body > section.hero.is-primary {
  display: none !important;
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

hr {
  border: none;
  border-top: 1px solid var(--border);
  margin: 2.25rem 0;
}

.content table {
  width: 100%;
  border-collapse: separate;
  border-spacing: 0;
  margin: 1rem 0;
  border-radius: 14px;
  overflow: hidden;
  border: 1px solid var(--border);
  background: rgba(13, 16, 36, 0.55);
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

.sdx-panel table a {
  display: inline-flex;
  align-items: center;
  padding: 0.25rem 0.65rem;
  border-radius: 999px;
  border: 1px solid var(--border);
  background: rgba(5, 8, 20, 0.45);
  font-weight: 700;
  text-decoration: none;
}

.sdx-panel table a:hover {
  border-color: rgba(159, 176, 255, 0.45);
  background: rgba(15, 21, 48, 0.72);
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

.sdx-panel {
  background: rgba(13, 16, 36, 0.72);
  border: 1px solid var(--border);
  border-radius: 18px;
  padding: 1.5rem;
  box-shadow: 0 16px 40px rgba(0, 0, 0, 0.3);
}

.sdx-panel + .sdx-panel {
  margin-top: 1.25rem;
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
  background: linear-gradient(145deg, rgba(15, 21, 48, 0.9), rgba(13, 16, 36, 0.85));
  border: 1px solid var(--border);
  border-radius: 24px;
  padding: 2.25rem;
  box-shadow: 0 30px 80px rgba(0, 0, 0, 0.45);
  position: relative;
  overflow: hidden;
}

.sdx-hero-panel::before {
  content: "";
  position: absolute;
  inset: -40% -20%;
  background: radial-gradient(circle at 30% 30%, rgba(159, 176, 255, 0.18) 0, transparent 40%),
              radial-gradient(circle at 70% 40%, rgba(255, 196, 106, 0.16) 0, transparent 40%);
  filter: blur(18px);
  animation: refsDrift 14s ease-in-out infinite;
  pointer-events: none;
}

@keyframes refsDrift {
  0% { transform: translate3d(0,0,0) scale(1); opacity: 0.55; }
  50% { transform: translate3d(18px, -12px, 0) scale(1.04); opacity: 0.65; }
  100% { transform: translate3d(0,0,0) scale(1); opacity: 0.55; }
}

.sdx-hero-title {
  font-family: "Space Grotesk", "Source Sans 3", sans-serif;
  font-size: clamp(2.1rem, 4vw, 3.1rem);
  line-height: 1.08;
  margin: 0.6rem 0 0.7rem;
  position: relative;
}

.sdx-hero-body {
  font-size: 1.08rem;
  line-height: 1.65;
  color: var(--muted);
  max-width: 70ch;
  position: relative;
}

.sdx-hero-actions {
  display: flex;
  flex-wrap: wrap;
  gap: 0.7rem;
  margin-top: 1.25rem;
  position: relative;
}

.sdx-btn {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  gap: 0.5rem;
  padding: 0.7rem 1.05rem;
  border-radius: 14px;
  border: 1px solid var(--border);
  background: rgba(13, 16, 36, 0.6);
  color: #f7f9ff;
  font-weight: 700;
  text-decoration: none;
  transition: transform 0.25s ease, background 0.25s ease, border-color 0.25s ease;
}

.sdx-btn:hover {
  transform: translateY(-2px);
  border-color: rgba(159, 176, 255, 0.45);
  background: rgba(15, 21, 48, 0.72);
  color: #f7f9ff;
}

.sdx-btn-primary {
  background: linear-gradient(135deg, rgba(159, 176, 255, 0.35), rgba(255, 196, 106, 0.25));
  border-color: rgba(159, 176, 255, 0.32);
}

.sdx-btn-ghost {
  background: rgba(13, 16, 36, 0.42);
}

.sdx-note {
  color: var(--muted);
  font-size: 0.95rem;
  margin-top: 0.85rem;
}

.sdx-list {
  padding-left: 1.1rem;
  margin: 0.6rem 0;
}

.sdx-list li {
  padding: 0.12rem 0;
}

@media (max-width: 980px) {
  .sdx-section.alt {
    padding: 1.9rem;
    margin: 1.35rem 0;
  }
}
</style>

<section class="section sdx-section" id="refs-intro">
  <div class="container">
    <div class="sdx-hero-panel">
      <div class="sdx-pill"><span>Sources and credits</span></div>
      <h1 class="sdx-hero-title">References</h1>
      <p class="sdx-hero-body">
        This page lists the main sources used to define innovation dates, collect market data, and credit visual assets.
      </p>
      <div class="sdx-hero-actions">
        <a class="sdx-btn sdx-btn-primary" href="#datasets">Datasets</a>
        <a class="sdx-btn sdx-btn-ghost" href="#event-sources">Event sources</a>
        <a class="sdx-btn sdx-btn-ghost" href="#images">Images</a>
        <a class="sdx-btn sdx-btn-ghost" href="#logos">Logos</a>
      </div>
      <p class="sdx-note">
        Note: All trademarks and logos are the property of their respective owners. This project is educational and non-commercial.
      </p>
    </div>
  </div>
</section>

<section class="section sdx-section alt" id="datasets">
  <div class="container">
    <h2 class="title is-3">Datasets and data access</h2>
    <div class="sdx-panel content" markdown="1">

**Market data dataset**

- Kaggle, Stock Market Dataset: [kaggle.com/datasets/jacksoncrow/stock-market-dataset](https://www.kaggle.com/datasets/jacksoncrow/stock-market-dataset)

**Dataset extension (Yahoo Finance via yfinance)**

- yfinance tutorial reference: [pythonfintech.com/articles/how-to-download-market-data-yfinance-python](https://pythonfintech.com/articles/how-to-download-market-data-yfinance-python/)

</div>
  </div>
</section>

<section class="section sdx-section alt" id="event-sources">
  <div class="container">
    <h2 class="title is-3">Innovation date sources</h2>
    <div class="sdx-panel">
      <p>
        Each event date in the project is anchored to a public reference, typically an official newsroom post, a regulatory
        press release, or a reputable reporting source. The links below are the primary references used to define dates.
      </p>
    </div>

    <div class="sdx-panel content" markdown="1">

### Apple, consumer tech

| Event                         | Source                                                                                                                     |
| ----------------------------- | -------------------------------------------------------------------------------------------------------------------------- |
| iPod Launch                   | [Apple Newsroom](https://www.apple.com/newsroom/2001/10/23Apple-Presents-iPod/)                                            |
| iPhone Launch                 | [Apple Newsroom](https://www.apple.com/newsroom/2007/06/28iPhone-Premieres-This-Friday-Night-at-Apple-Retail-Stores/)      |
| iPad Launch                   | [Apple Newsroom](https://www.apple.com/newsroom/2010/03/05iPad-Available-in-US-on-April-3/)                                |
| iPhone 5S Touch ID            | [Apple Newsroom](https://www.apple.com/newsroom/2013/09/16iPhone-5s-iPhone-5c-Arrive-on-Friday-September-20/)              |
| Apple Pay Launch              | [Apple Newsroom](https://www.apple.com/newsroom/2014/10/16Apple-Pay-Set-to-Transform-Mobile-Payments-Starting-October-20/) |
| AirPods Launch                | [Apple Newsroom](https://www.apple.com/newsroom/2016/12/apple-airpods-are-now-available/)                                  |
| M1 Chip Announcement          | [Apple Newsroom](https://www.apple.com/newsroom/2020/11/apple-unleashes-m1/)                                               |
| Apple Vision Pro Announcement | [Apple Newsroom](https://www.apple.com/newsroom/2023/06/introducing-apple-vision-pro/)                                     |

</div>

    <div class="sdx-panel content" markdown="1">

### NVIDIA, compute platforms

| Event                        | Source                                                                                                                                                       |
| ---------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| CUDA Launch                  | [NVIDIA CUDA Programming Guide (PDF)](https://developer.download.nvidia.com/compute/cuda/1.0/NVIDIA_CUDA_Programming_Guide_1.0.pdf)                          |
| DGX-1 Launch                 | [NVIDIA Newsroom](https://nvidianews.nvidia.com/news/nvidia-launches-world-s-first-deep-learning-supercomputer)                                              |
| Tesla V100 Launch            | [NVIDIA Newsroom](https://nvidianews.nvidia.com/news/nvidia-launches-revolutionary-volta-gpu-platform-fueling-next-era-of-ai-and-high-performance-computing) |
| RTX 2080 Ti Launch           | [NVIDIA Newsroom](https://nvidianews.nvidia.com/news/10-years-in-the-making-nvidia-brings-real-time-ray-tracing-to-gamers-with-geforce-rtx)                  |
| A100 Ampere Launch           | [NVIDIA Newsroom](https://nvidianews.nvidia.com/news/nvidia-announces-nvidia-ampere-architecture)                                                            |
| Arm Acquisition Announcement | [NVIDIA Newsroom](https://nvidianews.nvidia.com/news/nvidia-announces-agreement-to-acquire-arm-limited)                                                      |
| H100 Hopper Launch           | [NVIDIA Newsroom](https://nvidianews.nvidia.com/news/nvidia-announces-next-generation-accelerated-computing-platform-nvidia-hopper-architecture)             |
| NVIDIA Blackwell B200        | [NVIDIA Newsroom](https://nvidianews.nvidia.com/news/nvidia-blackwell-platform-arrives-to-power-new-era-of-computing)                                        |

</div>

    <div class="sdx-panel content" markdown="1">

### Tesla, EVs and robotics

| Event                           | Source                                                                                                                      |
| ------------------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| Autopilot Announcement          | [Reuters](https://www.reuters.com/article/business/tesla-unveils-all-wheel-drive-model-s-autopilot-features-idUSKCN0HZ07N/) |
| Model 3 First Deliveries        | [TechCrunch](https://techcrunch.com/2017/07/02/tesla-to-deliver-the-model-3-to-its-first-batch-of-customers-on-july-28/)    |
| Cybertruck Reveal               | [CNBC](https://www.cnbc.com/2019/11/21/tesla-cybertruck-unveiled.html)                                                      |
| Dojo Supercomputer Announcement | [YouTube](https://www.youtube.com/watch?v=j0z4FweCy4M)                                                                      |
| Tesla Bot Announcement          | [Wikipedia](<https://en.wikipedia.org/wiki/Optimus_(robot)>)                                                                |
| Cybertruck Deliveries Begin     | [Tesla](https://www.tesla.com/event/cybertruck)                                                                             |
| Optimus Gen 2 Reveal            | [X](https://x.com/Tesla_Optimus/status/1734759309077344737)                                                                 |
| FSD v12 Wide Rollout            | [Electrek](https://electrek.co/2024/03/18/tesla-starts-rolling-out-fsd-v12-to-more-owners/)                                 |

</div>

    <div class="sdx-panel content" markdown="1">

### Innovation Stack Shockwaves, multi-company events (Chapter 4)

| Event                         | Source                                                                                                                     |
| ----------------------------- | -------------------------------------------------------------------------------------------------------------------------- |
| Amazon S3 Launch              | [AWS Blog](https://aws.amazon.com/blogs/aws/amazon_s3/)                                                                    |
| ASML First EUV Tools          | [ASML Backgrounder](https://medium.com/@ASMLcompany/a-backgrounder-on-extreme-ultraviolet-euv-lithography-a5fccb8e99f4)    |
| iPhone Launch                 | [Apple Newsroom](https://www.apple.com/newsroom/2007/06/28iPhone-Premieres-This-Friday-Night-at-Apple-Retail-Stores/)      |
| Google Chrome Beta Launch     | [Google Blog](https://googleblog.blogspot.com/2008/09/fresh-take-on-browser.html)                                          |
| Microsoft Azure Launch        | [Forbes](https://www.forbes.com/sites/janakirammsv/2020/02/03/a-look-back-at-ten-years-of-microsoft-azure/)                |
| iPhone 5S Touch ID            | [Apple Newsroom](https://www.apple.com/newsroom/2013/09/16iPhone-5s-iPhone-5c-Arrive-on-Friday-September-20/)              |
| TensorFlow Open-Sourced       | [Wikipedia](https://en.wikipedia.org/wiki/TensorFlow)                                                                      |
| Armv9 Architecture Introduced | [Arm Newsroom](https://www.arm.com/company/news/2021/03/arms-answer-to-the-future-of-ai-armv9-architecture)                 |
| Meta LLaMA Release            | [Meta AI](https://ai.meta.com/blog/large-language-model-llama-meta-ai/)                                                    |
| GPT-4 Release                 | [OpenAI](https://openai.com/index/gpt-4/)                                                                                  |
| Microsoft Copilot Announcement | [Microsoft Blog](https://blogs.microsoft.com/blog/2023/03/16/introducing-microsoft-365-copilot/)                           |
| Apple Vision Pro Announcement | [Apple Newsroom](https://www.apple.com/newsroom/2023/06/introducing-apple-vision-pro/)                                     |

</div>

    <div class="sdx-panel content" markdown="1">

### AI shockwaves, OpenAI, Google, Meta, Microsoft

| Event                          | Source                                                                                           |
| ------------------------------ | ------------------------------------------------------------------------------------------------ |
| ChatGPT Launch                 | [OpenAI](https://openai.com/blog/chatgpt)                                                        |
| GPT-4 Release                  | [OpenAI](https://openai.com/index/gpt-4/)                                                        |
| GPT-4 Medical AI Release       | [OpenAI](https://openai.com/index/gpt-4/)                                                        |
| Meta LLaMA Release             | [Meta AI](https://ai.meta.com/blog/large-language-model-llama-meta-ai/)                          |
| Microsoft Copilot Announcement | [Microsoft Blog](https://blogs.microsoft.com/blog/2023/03/16/introducing-microsoft-365-copilot/) |
| Google Bard Launch             | [Google Blog](https://blog.google/technology/ai/try-bard/)                                       |

</div>

    <div class="sdx-panel content" markdown="1">

### Biotech and healthcare, regulation-gated innovation

| Event                            | Source                                                                                                                                                                  |
| -------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| AlphaFold 2 Breakthrough         | [DeepMind Blog](https://deepmind.google/discover/blog/alphafold-a-solution-to-a-50-year-old-grand-challenge-in-biology/)                                                |
| First mRNA Vaccine (Comirnaty)   | [FDA Press Release](https://www.fda.gov/news-events/press-announcements/fda-takes-key-action-fight-against-covid-19-issuing-emergency-use-authorization-first-covid-19) |
| Wegovy GLP-1 Weight Loss Launch  | [FDA Press Release](https://www.fda.gov/news-events/press-announcements/fda-approves-new-drug-treatment-chronic-weight-management-first)                                |
| Paxlovid Oral Antiviral Launch   | [FDA Press Release](https://www.fda.gov/news-events/press-announcements/coronavirus-covid-19-update-fda-authorizes-first-oral-antiviral-treatment-covid-19)             |
| Mounjaro (Tirzepatide) Launch    | [Eli Lilly Investor Relations](https://investor.lilly.com/news-releases/news-release-details/us-fda-approves-novel-once-weekly-incretin-therapy-mounjaror)              |
| Leqembi Alzheimer Approval       | [Biogen Investor Relations](https://investors.biogen.com/news-releases/news-release-details/fda-grants-accelerated-approval-leqembir-lecanemab-irreversible)            |
| Zepbound Obesity Drug Launch     | [FDA Press Release](https://www.fda.gov/news-events/press-announcements/fda-approves-new-drug-treatment-chronic-weight-management)                                      |
| Casgevy CRISPR Therapy Approval  | [FDA Press Release](https://www.fda.gov/news-events/press-announcements/fda-approves-first-gene-therapies-treat-patients-sickle-cell-disease)                           |
| Da Vinci 5 Surgical Robot Launch | [Intuitive Newsroom](https://www.intuitive.com/en-us/about-us/newsroom/press-releases/intuitive-receives-fda-clearance-for-da-vinci-5)                                  |

</div>
  </div>
</section>

<section class="section sdx-section alt" id="images">
  <div class="container">
    <h2 class="title is-3">Images and design assets</h2>

    <div class="sdx-panel content" markdown="1">

### Canva elements

Canva Elements, by Flixx Studio, by jittawit21, by monsitj, by pixelshot, by Aviavlad from Getty Images and by TEDWIP from Stock Dignity, accessed on 13 Dec 2025, via Canva.

</div>

    <div class="sdx-panel content" markdown="1">

### Website imagery

| Asset        | Source                                                                                                                                                    |
| ------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| NVIDIA image | [Outlook Business](https://media.assettype.com/outlookbusiness/import/uploadimage/library/16_9/16_9_5/nvidia_1651928213.webp)                             |
| Apple image  | [bernardmarr.com](https://bernardmarr.com/wp-content/uploads/2024/08/Apples-New-AI-Revolution-Why-Apple-Intelligence-Could-Change-Everything-scaled.jpeg) |
| Tesla image  | [vynmsa.com](https://vynmsa.com/wp-content/uploads/2024/02/tesla-mexico.jpg.webp)                                                                         |

</div>
  </div>
</section>

<section class="section sdx-section alt" id="logos">
  <div class="container">
    <h2 class="title is-3">Company logos</h2>
    <div class="sdx-panel">
      <p>
        Logos are used as lightweight visual identifiers in plots and UI sections. Sources are listed below.
      </p>
    </div>

    <div class="sdx-panel content" markdown="1">

### Healthcare and biotech logos

| Company                             | Logo source                                                                                                                                                    |
| ----------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Eli Lilly and Company               | [Logo](https://upload.wikimedia.org/wikipedia/commons/thumb/2/2b/Eli_Lilly_and_Company.svg/2560px-Eli_Lilly_and_Company.svg.png)                               |
| Johnson and Johnson                 | [Logo](https://companieslogo.com/img/orig/JNJ-5579062e.png?t=1720244492)                                                                                       |
| AbbVie Inc.                         | [Logo](https://companieslogo.com/img/orig/ABBV_BIG.D-c64c1359.png?t=1720244490)                                                                                |
| UnitedHealth Group Incorporated     | [Logo](https://upload.wikimedia.org/wikipedia/de/thumb/4/4e/United-health-group.svg/1200px-United-health-group.svg.png)                                        |
| AstraZeneca PLC                     | [Logo](https://cdt.sensors.cam.ac.uk/sites/default/files/media/astrazeneca-logo-png-astrazeneca-logo-astra-zeneca-4902.png)                                    |
| Novartis AG                         | [Logo](https://www.novartis.com/sites/novartis_com/files/2021-10/novartis-logo-transparent.png)                                                                |
| Merck and Company, Inc.             | [Logo](https://upload.wikimedia.org/wikipedia/commons/b/b7/Merck_Logo.png)                                                                                     |
| Novo Nordisk A/S                    | [Logo](https://upload.wikimedia.org/wikipedia/en/thumb/b/b1/Novo_Nordisk_-_Logo.svg/1200px-Novo_Nordisk_-_Logo.svg.png)                                        |
| Thermo Fisher Scientific Inc        | [Logo](https://upload.wikimedia.org/wikipedia/commons/thumb/5/50/Thermo_Fisher_Scientific_logo.svg/1200px-Thermo_Fisher_Scientific_logo.svg.png)               |
| Abbott Laboratories                 | [Logo](https://companieslogo.com/img/orig/ABT_BIG.D-da982f7c.png?t=1720244490)                                                                                 |
| Intuitive Surgical, Inc.            | [Logo](https://upload.wikimedia.org/wikipedia/commons/thumb/0/01/Intuitive_Surgical_logo.svg/2560px-Intuitive_Surgical_logo.svg.png)                           |
| Amgen Inc.                          | [Logo](https://upload.wikimedia.org/wikipedia/commons/thumb/a/ab/Amgen.svg/2560px-Amgen.svg.png)                                                               |
| Danaher Corporation                 | [Logo](https://companieslogo.com/img/orig/DHR_BIG.D-c31b05a9.png?t=1720244491)                                                                                 |
| Gilead Sciences, Inc.               | [Logo](https://www.logo.wine/a/logo/Gilead_Sciences/Gilead_Sciences-Logo.wine.svg)                                                                             |
| Pfizer, Inc.                        | [Logo](https://upload.wikimedia.org/wikipedia/commons/8/8b/Pfizer_%282021%29.png)                                                                              |
| Boston Scientific Corporation       | [Logo](https://upload.wikimedia.org/wikipedia/commons/thumb/0/02/Boston_Scientific_Logo.svg/1200px-Boston_Scientific_Logo.svg.png)                             |
| Stryker Corporation                 | [Logo](https://download.logo.wine/logo/Stryker_Corporation/Stryker_Corporation-Logo.wine.png)                                                                  |
| Medtronic plc                       | [Logo](https://download.logo.wine/logo/Medtronic/Medtronic-Logo.wine.png)                                                                                      |
| Sanofi                              | [Logo](https://1000logos.net/wp-content/uploads/2020/03/Sanofi-Logo-2011.png)                                                                                  |
| Vertex Pharmaceuticals Incorporated | [Logo](https://upload.wikimedia.org/wikipedia/commons/thumb/d/d9/Vertex_logo.svg/1200px-Vertex_logo.svg.png)                                                   |
| HCA Healthcare, Inc.                | [Logo](https://companieslogo.com/img/orig/HCA_BIG.D-75cfa1ae.png?t=1720244492)                                                                                 |
| Bristol-Myers Squibb Company        | [Logo](https://upload.wikimedia.org/wikipedia/commons/thumb/c/c6/Bristol-Myers_Squibb_logo_%282020%29.svg/2560px-Bristol-Myers_Squibb_logo_%282020%29.svg.png) |
| CVS Health Corporation              | [Logo](https://www.cvshealth.com/content/dam/enterprise/cvs-enterprise/media-library/logos/migratedcontent/cvs-health-logo-stacked.png)                        |
| GSK plc                             | [Logo](https://upload.wikimedia.org/wikipedia/en/thumb/a/a6/GSK_logo_2014.svg/1189px-GSK_logo_2014.svg.png)                                                    |
| Regeneron Pharmaceuticals, Inc.     | [Logo](https://upload.wikimedia.org/wikipedia/commons/thumb/4/48/Regeneron_logo.svg/2560px-Regeneron_logo.svg.png)                                             |

</div>

    <div class="sdx-panel content" markdown="1">

### Tech and AI tickers

| Ticker | Logo source                                                                                                                   |
| ------ | ----------------------------------------------------------------------------------------------------------------------------- |
| NVDA   | [Logo](https://upload.wikimedia.org/wikipedia/sco/thumb/2/21/Nvidia_logo.svg/1280px-Nvidia_logo.svg.png)                      |
| AAPL   | [Logo](https://upload.wikimedia.org/wikipedia/commons/thumb/3/31/Apple_logo_white.svg/1724px-Apple_logo_white.svg.png)        |
| GOOGL  | [Logo](https://png.pngtree.com/png-vector/20230817/ourmid/pngtree-google-internet-icon-vector-png-image_9183287.png)          |
| MSFT   | [Logo](https://companieslogo.com/img/orig/MSFT-a203b22d.png?t=1722952497)                                                     |
| AMZN   | [Logo](https://uxwing.com/wp-content/themes/uxwing/download/brands-and-social-media/amazon-white-icon.png)                    |
| AVGO   | [Logo](https://companieslogo.com/img/orig/AVGO-ceb477a4.png?t=1722952492)                                                     |
| META   | [Logo](https://crystalpng.com/wp-content/uploads/2025/02/meta_logo.png)                                                       |
| TSM    | [Logo](https://upload.wikimedia.org/wikipedia/en/thumb/6/63/Tsmc.svg/1200px-Tsmc.svg.png)                                     |
| TSLA   | [Logo](https://upload.wikimedia.org/wikipedia/commons/e/e8/Tesla_logo.png)                                                    |
| ORCL   | [Logo](https://upload.wikimedia.org/wikipedia/commons/thumb/5/50/Oracle_logo.svg/2560px-Oracle_logo.svg.png)                  |
| PLTR   | [Logo](https://companieslogo.com/img/orig/PLTR_BIG.D-38de5db6.png?t=1720244493)                                               |
| ASML   | [Logo](https://upload.wikimedia.org/wikipedia/en/thumb/6/6c/ASML_Holding_N.V._logo.svg/1065px-ASML_Holding_N.V._logo.svg.png) |
| NFLX   | [Logo](https://upload.wikimedia.org/wikipedia/commons/7/7a/Logonetflix.png)                                                   |
| AMD    | [Logo](https://cdn.worldvectorlogo.com/logos/amd-advanced-micro-devices-white.svg)                                            |
| IBM    | [Logo](https://upload.wikimedia.org/wikipedia/commons/thumb/5/51/IBM_logo.svg/2560px-IBM_logo.svg.png)                        |
| MU     | [Logo](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTxBUXCu90HT_uorTSEicRRQCGu3KO-26cRnQ&s)                          |
| CRM    | [Logo](https://upload.wikimedia.org/wikipedia/commons/thumb/f/f9/Salesforce.com_logo.svg/1280px-Salesforce.com_logo.svg.png)  |
| AMAT   | [Logo](https://download.logo.wine/logo/Applied_Materials/Applied_Materials-Logo.wine.png)                                     |
| SHOP   | [Logo](https://img.icons8.com/ios_filled/512/FFFFFF/shopify.png)                                                              |
| QCOM   | [Logo](https://upload.wikimedia.org/wikipedia/commons/thumb/f/fc/Qualcomm-Logo.svg/1280px-Qualcomm-Logo.svg.png)              |
| INTC   | [Logo](https://pngimg.com/d/intel_PNG20.png)                                                                                  |
| UBER   | [Logo](https://www.edigitalagency.com.au/wp-content/uploads/new-Uber-logo-white-png-large-size.png)                           |
| NOW    | [Logo](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSX8q-fnKZogmH7Gh2W_4XXr4Z3tm0RBbP5Cw&s)                          |
| ARM    | [Logo](https://download.logo.wine/logo/Arm_Holdings/Arm_Holdings-Logo.wine.png)                                               |
| ADBE   | [Logo](https://ik.imagekit.io/kkbzr2uz4cp/stock/nasdaq/adbe.png)                                                              |

</div>
  </div>
</section>
