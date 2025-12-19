

# SwissDataExplorers — Innovation Footprints in Tech Stock Markets

**Data story (website):** https://ydib11.github.io/Swissdata/  
**Repository:** https://github.com/YDIB11/Swissdata

>  We analyze how stock markets react to major innovation events using an event-study style workflow (returns, cumulative returns, volatility, and volume).

---

## 1) Project overview

This project explores whether public markets **immediately price innovation** or whether the impact becomes visible only **days/weeks later**.

**What we cover (as described in the story):**
- **~45 innovation events**
- **50+ companies**
- Case studies around: **Apple, NVIDIA, Tesla, Innovation Stack, Healthcare**  
  *(Edit these labels if your final story uses different names.)*

**Main questions**
- Do markets react **on the event date**, or is the reaction **delayed**?
- Are reactions different across **consumer tech vs infrastructure vs healthcare**?
- Are there signs of **anticipation** before the event?

---

## 2) Deliverables (what to grade)

- **Data story (public):** https://ydib11.github.io/Swissdata/
- **Single graded notebook:** `[[PATH_TO_FINAL_NOTEBOOK.ipynb]]`  
  Example: `notebooks/final.ipynb`

> Note: The course expects **one notebook** (extending P2) that produces the results and contains the main narrative of the analysis, while core logic can be in external scripts/modules.

---

## 3) Repository structure (edit if yours differs)

- `index.markdown` — main story page  
- `about.markdown` — about / team page  
- `references.markdown` — data + sources + credits  
- `assets/` — images / CSS / visuals  
- `[[notebooks/]]` — notebooks (including the graded one)  
- `[[src/]]` — code modules used by the notebook (recommended)  
- `_config.yml`, `Gemfile`, `Gemfile.lock` — Jekyll/GitHub Pages config

---

## 4) Data

**Market data**
- Primary dataset: `[[KAGGLE_DATASET_NAME + LINK OR SHORT DESCRIPTION]]`
- Local location expected by the notebook: `[[data/...]]`

**Extra data access (optional)**
- We may use `yfinance` to validate or extend market data when needed.

**Innovation event dates**
- Event dates come from public sources (press releases, reputable reporting, regulatory announcements, etc.).  
  Full source list is available on the website: https://ydib11.github.io/Swissdata/references/

> If your notebook stores the event list in a file, link it here: `[[path/to/events.csv]]`

---

## 5) Method (high-level)

We treat each innovation announcement as an “event” and measure its market footprint around the event date.

**Typical workflow per event**
1. Choose an **event date** (and shift to the next trading day if needed).
2. Extract an **event window** (commonly ±30 trading days).
3. Compute consistent metrics:
   - returns / log returns
   - cumulative return (buy-and-hold within the window)
   - volatility over the window
   - volume changes (attention proxy)

> The exact definitions, parameters (window sizes, filters), and implementation details are in the notebook.

---
## 6) Team contributions (required)

- **Kevin:** Collecting and cleaning the stock dataset, handling missing values/outliers, building the final analysis-ready tables
- **Youssef:** Building the innovation event list (dates + sources), validating event dates vs trading days, maintaining the references/sources list
- **Rami:** Implementing the event-study pipeline (window extraction, returns/cumulative returns/volatility/volume metrics), writing reusable code modules
- **Chloe:** Creating the main figures and visual consistency (plot styling, annotations, comparability across cases), preparing summary tables for the story
- **Michel:** Writing and structuring the data story website (Jekyll/GitHub Pages), improving clarity for non-technical readers, final integration + reproducibility checks




