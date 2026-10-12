# CAKE project page

Interactive summary page for the paper
**CAKE: Cloud Architecture Knowledge Evaluation of Large Language Models**
(Adam, Konrad, Terrenzi, Lukas, Yilmaz, Sierszecki, Ayvaz · Centre for Industrial Software, University of Southern Denmark).

- Paper: https://arxiv.org/abs/2604.05755
- Dataset: https://github.com/timadam03/CAKE-benchmark

The page covers the benchmark design, a few real CAKE-Core questions to try, the scoring pipeline, and results for all 22 model configurations (leaderboard, per-level rankings, +think / +tool effects, per-topic heatmap, speed vs quality).

## Structure

The site is a single static file, `index.html`, with inline CSS and JavaScript. It has no build step and no dependencies. Fonts load from Google Fonts.

## Run locally

Open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000
```

Then visit http://localhost:8000.

## Data sources

All numbers come from the paper:

- Table II: MCQ accuracy, free-response overall score, seconds per question.
- Fig. 3: per-level free-response scores, read at one decimal.
- Fig. 5: CAKE-Core vs Full MCQ deltas.
- Fig. 7: per-topic MCQ and free-response scores.
- Example questions: `CAKE-Core.json` from the dataset repository.

Augmentation deltas and the "3B+ spread" values are computed from Table II.

## Deployment

Served with GitHub Pages from the repository root. Any push to the Pages branch redeploys the site.
