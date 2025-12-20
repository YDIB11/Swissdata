![Jekyll](https://img.shields.io/badge/Jekyll-GitHub%20Pages-1f425f?logo=jekyll&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)
![Plotly](https://img.shields.io/badge/Plotly-3F4F75?logo=plotly&logoColor=white)

# SwissDataExplorers - Innovation Footprints in Tech Stock Markets

Website for EPFL Applied Data Analysis (ADA), 2025. We study how public markets "recognize" innovation: immediately on day 0, slowly over weeks, or not at all.

- Rendered data story: https://ydib11.github.io/Swissdata/
- Main Repository: https://github.com/epfl-ada/ada-2025-project-swissdataexplorers2025
- About (team): https://ydib11.github.io/Swissdata/about/
- References & sources: https://ydib11.github.io/Swissdata/references/

## Team

- Youssef Dib:Wrote and structured the website (Jekyll/GitHub Pages), edited for clarity for non-technical readers, and handled final integration + reproducibility checks.
  
- Rami Aschkar: Collected and cleaned the stock dataset (missing values, outliers) and prepared the final analysis tables.
  
- Kevin Abou Jaoude: Produced the main figures with consistent styling (annotations, comparable scales) and made the summary tables used in the write-up.
  
- Chloe Abou Halka: Built the innovation event list (dates + sources), checked dates against trading days, and maintained the references.
  
- Michel Bassil: Worked on the methods side (defined outcome measures and key parameters), and did quality checks on the results (sanity checks, edge cases), fixing issues during integration.

## What is inside this repo

- `index.markdown`: the main story page (acts + chapters)
- `about.markdown`: team page
- `references.markdown`: event sources + credits
- `assets/`: plots (Plotly HTML), images, and the SDX theme (`assets/css/sdx.css`)

## Run locally

```bash
bundle install
bundle exec jekyll serve
```
