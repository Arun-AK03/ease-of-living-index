# reports

Generated figures (PNG) produced by the notebooks in `notebooks/`. These are the
charts that appear in, or support, the paper. Nothing here is hand-drawn — every
image is regenerable by re-running the corresponding visualisation notebook.

## Top-level figures
- `framework diagram.png` — overview of the four-pillar EoLI methodology.
- `ease_of_living_plot.png` / `ease_of_living_line_plot.png` — the composite
  index over countries / time.
- `Heatmaps_Fig15.png` — figure 15, correlation / index heatmaps.
- `Ease of Living Index Voilion_Fig16.png` — figure 16, violin plot of the index
  distribution. *(filename misspells "Violin")*

## Per-pillar subfolders
- `Economic Index/` — GDP growth, cost of living, KDE, economic index values.
- `Institutional Index/` — freedom-of-speech and institutional index charts.
- `Quality of Life/` — crime index, imputed distributions, QoL index.
- `Sustainability/` — greenhouse-gas emissions (Fig 14), imputed distributions.

## Regenerating
Re-run the matching notebook in `notebooks/` (e.g. `Ranking_Visualisation.ipynb`
for the composite-index and heatmap figures).
